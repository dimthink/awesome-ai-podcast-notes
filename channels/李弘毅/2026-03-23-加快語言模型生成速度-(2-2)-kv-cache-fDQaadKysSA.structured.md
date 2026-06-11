---
title: "加快語言模型生成速度 (2/2)：KV Cache - 结构化文稿"
channel: "李弘毅"
published: "2026-03-23"
source_url: "https://www.youtube.com/watch?v=fDQaadKysSA"
video_id: "fDQaadKysSA"
variant: "structured"
---

# 加快語言模型生成速度 (2/2)：KV Cache - 结构化文稿

- **Channel:** 李弘毅
- **Published:** 2026-03-23
- **Source:** https://www.youtube.com/watch?v=fDQaadKysSA
- **Main:** [加快語言模型生成速度 (2/2)：KV Cache](2026-03-23-加快語言模型生成速度-(2-2)-kv-cache-fDQaadKysSA.md)

# 深入理解 KV Cache：加速语言模型生成的关键技术

## 引言：KV Cache 是什么？

今天我们要介绍一个叫做 **KV Cache** 的技术。KV Cache 的发音跟“现金”（Cash）是一样的，而它确实也和钱有一定的关联性。那么，它和钱到底有什么样的关联性呢？我们接下来就会看到。

## 语言模型的生成过程：Prefill 与 Decode

在正式介绍 KV Cache 之前，我们先来回顾一下语言模型的整个生成过程。

语言模型的生成过程是这样的：

1. 首先，有一个来自人类的 **Prompt** 输入给语言模型。
1. 语言模型会进行文字接龙。例如，你输入“李宏毅几班”，模型就会输出“大”。
1. 然后，模型会把“大”再作为输入，输出“金”。
1. 再把“金”作为输入，去输出“结束”的符号。
整个过程可以分为两个阶段：

- **Prefill（预填充）阶段**：处理输入的一个非常长的 Sequence。
- **Decode（解码）阶段**：逐个输出 Token 的过程。
## Prefill 阶段：KV Cache 的诞生

我们首先来看 Prefill 阶段发生了什么。

在 Prefill 阶段，一次输入了大量的 Token，我们需要为每一个 Token 计算出它的 **Q、K、V**。例如，假设输入有三个 Token，它们会分别得到各自的 Q、K、V。接下来，我们会用这些 Q、K、V 去计算 **Attention**。

这个过程可以抽象地描述如下：

- **Q1** 与 **K1** 计算 Attention Weight，然后乘上 **V1**，得到 **O1**。
- **Q2** 与前面的两个 K（K1、K2）计算 Attention Weight，再对 V1、V2 做加权求和，得到 **O2**。
- **Q3** 也进行同样的操作，与 K1、K2、K3 计算 Attention Weight，再对 V1、V2、V3 做加权求和，得到 **O3**。
需要注意的是，计算 Q1、Q2、Q3 得到 O1、O2、O3 这三件事，是可以**并行运算**的。

### 什么是 KV Cache？

在这些计算完成后，我们会把 **K 和 V 存下来**，而 Q 则会被丢掉（稍后会解释为什么）。对于这个例子来说，就是 **K1、K2、K3** 和 **V1、V2、V3** 会被保存。**把 V 和 K 存下来这件事情，就叫做 KV Cache。**

### 为什么要存 K 和 V？

当我们模型开始生成（Decode）时，假设刚才的三个 Token 输入后，模型生成了第四个 Token。这个新的 Token 会被作为新的输入，我们得到 **Q4、K4、V4**。

如果每次生成新 Token 时，都需要把前面的所有 Token 重新输入模型，再重新计算一次它们的 V 和 K，那将非常耗时。因此，我们将之前计算好的 V 和 K 直接存下来，就不用再算第二次了。

具体操作如下：

- **Q4** 直接与之前存下来的 **K1、K2、K3** 以及它自己的 **K4** 计算 Attention。
- 得到 Attention Weight 后，再与 **V1、V2、V3、V4** 做加权求和，得到 **O4**。
这样，我们就节省了重复计算 V1、V2、V3 和 K1、K2、K3 的时间。因为计算这些 K 和 V 也需要将输入乘以一个矩阵，这是需要花费时间的。

所以，我们会把已经算出来的 K 和 V 存下来，留待日后使用。当第五个 Token 进来时，前面四个 Token 的 V 和 K 就不需要重算了。第五个 Token 只需要计算它自己的 **Q5、V5、K5**，然后去计算 Attention 得到 O5 即可。

这就是 **KV Cache** 的概念。虽然这是一个非常简单的概念，但在实际实现中，它可能会遇到巨大的问题。

## KV Cache 的内存压力：仓库可能被撑爆

我们刚才提到有一个很大的“仓库”（GPU 内存），好像什么都可以放。但 KV Cache 这个东西，是可能直接撑爆这个你以为非常大的仓库的。为什么？

1. **存储的 K 和 V 数量巨大**：每产生一个 Token，你就需要存储一组 K 和 V。如果输入或输出的 Sequence 很长，就会撑爆你的内存。
1. **K 和 V 不止一组**：模型通常有多个 Attention Head，每个 Head 都有自己对应的 K 和 V。在 **Multi-Head Attention** 机制下，K 和 V 有很多组。
### 实际计算示例：Gemma 2 27B 模型

我们以 **Gemma 2** 的 **27B** 模型为例，来实际看看 KV Cache 对 GPU 内存造成的压力有多大。根据模型的架构表格：

- 它有 **46 个 Layer**。
- 使用 **Grouped-Query Attention (GQA)**，但我们先假设它就是普通的 Attention。
- 假设有 **30 个 Head**。
- 每个 QKV 向量的维度是 **128 维**。
我们来计算一下，每产生一个 Token，需要存储一组 Key 和一组 Value，会占用多少内存：

- 计算方式：46 层 × 30 个 Head × 128 维 × 2 Bytes（FP16） × 2（Key 和 Value）
- 结果约为 **736 KB**，也就是 **0.72 MB**。
听起来不到 1 MB，似乎不大。但这只是一个 Token！假设你使用的是 **A100** 显卡，它有 **80 GB** 的内存，也只够存储大约 **114k**（约 10 万）个 Token 的 KV Cache。

然而，现在很多场景对 Context 的需求远远超过 10 万。所以你会发现，当模型的输入或输出 Sequence 太长时，就会出现 **CUDA Out of Memory** 错误。你本以为的巨大仓库，也是可以被撑爆的。

## 缓解内存压力的技术：让仓库装下更多东西

为了避免仓库被撑爆，让它可以存更多东西，出现了各种各样的技术。下面我们来介绍几种。

### 1. Multi-Query Attention 和 Grouped-Query Attention

传统的 **Multi-Head Attention** 有多组 Value 和 Key，非常占用空间。于是有人提出：

- **Multi-Query Attention**：可以有多个 Query，但**所有的 Query 共享同一组 Value 和 Key**。因为 Value 和 Key 才是会被存下来的东西，Query 不会被存，所以共享 Value 和 Key 可以大大减少内存占用。不过，这种方法的实际表现并不好。
- **Grouped-Query Attention (GQA)**：这是一种介于 Multi-Head Attention 和 Multi-Query Attention 之间的方法。它的想法是，仍然可以有多组 Value 和 Key，但**每组 Value 和 Key 可以分配给多个 Query**。也就是说，Query 的数量比 Key 和 Value 的数量多。例如，一组 Value 和 Key 可以配两个 Query，那么四个 Query 实际上只有两组 Value 和 Key。这正是 Gemma 等知名模型（如 LLaMA）所采用的方法，主要就是为了处理 KV Cache 问题。
### 2. Multi-Head Latent Attention

**Multi-Head Latent Attention** 的核心思想是：将多组 Query 和 Key **压缩成一个低维向量**，在存到仓库里时，只存这个压缩后的向量。

这个向量怎么来呢？在计算 Query 和 Key 时，输入向量 x 会先通过一个 Bottleneck 层，变成一个维度较小的向量（图中桃红色部分），然后再通过不同的变换得到不同的 Query 和 Key。这种方法需要在训练模型时就引入，让模型学会压缩。

神奇的是，在计算 Attention 时，我们**不需要将压缩的向量解压回原来的多组 Value 和 Key**，而是可以直接在压缩的维度上进行运算，从而节省大量的计算和内存。

为什么不需要解压？

- **计算 Attention Weight**：原本需要计算 Q 和 K（K = WK × C）的点积。这可以等价于将 Q 压缩后（Q‘ = WK^T × Q），再与压缩后的 C 做点积。这样，我们只需要对每个 Q 做一次压缩，而无需对每个 C（数量与序列长度相关）进行解压。
- **计算 Weighted Sum**：原本需要将 C 解压成 V，再对 V 做加权求和。这可以等价为先对压缩后的 C 做加权求和，然后再将结果解压一次。这样，我们只需要做一次解压，而不是对序列中每一个 C 都进行解压。
因此，这是一个非常有效的方法，甚至在某些情况下，其结果比原始的 Multi-Head Attention 还要好。

### 3. Sliding Window Attention

**Sliding Window Attention** 的精神很简单：每次做 Attention 时，我们只关注前面一个固定窗口（Window）范围内的 Token，而不是整个 Sequence。

例如，只关注前面 4096 个 Token。这样就能确保 KV Cache 的大小有一个固定的上限。

这个方法的潜在问题是，Query 能关注到的范围变小了，模型可能无法考虑非常长的 Sequence。但这个问题可能没那么严重，因为模型通常有多层。虽然最上面一层只看前面几个 Key，但下层看到的范围会通过多层累积而扩大。因此，如果 Transformer 的层数足够多，Sliding Window Attention 实际能看到的范围仍然可以非常大。这种方法曾被用在 **Mistral 7B** 的某个版本中。

### 4. Streaming LLM

**Streaming LLM** 也是一种基于 Sliding Window Attention 的方法。它发现，如果 Attention 的范围不仅包括滑动窗口内的 Token，还包含整个 Sequence **最开头的几个 Token**，那么模型的性能会大幅提升，尤其是在输入 Sequence 非常长的时候。

而且，这一招甚至**不需要额外的训练**。你可以在 Inference 时，直接在你的滑动窗口里额外加上最前面的几个 Token，就能让 Sliding Window 的表现大增。

为什么加上开头几个 Token 效果这么好？

模型有一个默认行为：如果没什么好关注的，它就会把 Attention 的权重集中在**第一个 Token** 上。如果在推理时不给它第一个 Token，模型就会“世界崩溃”，不知道怎么处理，导致表现变差。一旦给了它第一个 Token，它就能恢复原有的行为。这就是为什么 Streaming LLM 如此有效。

### 5. Pruning KV Cache

这个方法更直接：**把没用的 KV 直接从数据库中丢掉**。一系列研究（如 2023 年的 Scissorhands 和 H2O）发现，多数的 Key 和 Value 其实并没有被用到。

这些论文指出，只有非常少部分的 Token 会被频繁地关注。而大多数 Token 的 Key 和 Value 从来没人去关注，存着它们只是占用空间。那些被反复关注的 Token 的 KV 才应该被保留下来。

这些方法的基本精神是：如果一个 KV 一直没被用到，就把它丢弃。在有些任务上，这种方法可以压缩 5 倍（只保留 20% 的 KV），而模型表现仍然相近。不过，对于非常难的任务，随意丢弃 KV 还是会影响性能。

## KV Cache 的跨对话共享：Cache Input 与省钱

刚才讲的 KV Cache 都是针对同一个对话内的。其实，KV Cache 也有可能在跨对话中共享。

假设有两条不同的对话，但它们有**完全相同的前缀**（Prefix），那么前面的 Token 对应的 Key 和 Value 是可以直接拿来共用的。例如，一个 AI Agent 的 System Prompt 很长，但内容通常是固定的。如果每次对话都重复输入这个 System Prompt，那么它的 KV 就可以被缓存并重复使用。

### 缓存输入带来的商业折扣

如今，多数语言模型服务（如 ChatGPT、Gemini、Claude、DeepSeek）都提供了 **Cache Input** 的折扣方案。以 GPT-4o 为例，如果输入有 Cache Hit，价格可以低至十分之一。这是因为对于平台来说，这部分内容几乎不需要额外计算。

需要注意的是，**只有前缀相同才能命中缓存**。如果改变了前缀，就会破坏整个 Cache 的结果，无法获得折扣。因此，在设计 AI Agent 的 Prompt 时，内容的摆放顺序很有讲究：

- **越稳定不动的内容（如可用工具）应放在越前面**。
- **越可能变动的内容（如日期、变量）应放在越后面**。
甚至，同样的输入用不同的写法，也可以获得不同程度的 Cache Hit。比如：

- **效率低的写法**：`帮我订从台北到波士顿的班机` 和 `帮我订从旧金山到纽约的班机`，只能命中“帮我订从”几个字。
- **效率高的写法**：`帮我订从 X 到 Y 的班机`，然后把 `X=台北，Y=波士顿` 放在序列最后。这样就能命中更长的前缀，节省更多钱。
一篇今年 1 月的论文对 Cache Input 的效果进行了实测。他们发现，在 Gemini 2.5 Pro 和 GPT-4o 等模型上，通过优化 Cache 策略，至少可以达到 **50% 甚至更多的成本节省**。

## 总结：各种加速技术一览

最后，我们来总结一下今天学到的各种方法及其特点：

以上就是今天想跟大家分享的内容。
