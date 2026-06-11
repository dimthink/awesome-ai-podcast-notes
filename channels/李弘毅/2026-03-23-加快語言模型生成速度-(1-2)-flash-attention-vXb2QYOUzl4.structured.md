---
title: "加快語言模型生成速度 (1/2)：Flash Attention - 结构化文稿"
channel: "李弘毅"
published: "2026-03-23"
source_url: "https://www.youtube.com/watch?v=vXb2QYOUzl4"
video_id: "vXb2QYOUzl4"
variant: "structured"
---

# 加快語言模型生成速度 (1/2)：Flash Attention - 结构化文稿

- **Channel:** 李弘毅
- **Published:** 2026-03-23
- **Source:** https://www.youtube.com/watch?v=vXb2QYOUzl4
- **Main:** [加快語言模型生成速度 (1/2)：Flash Attention](2026-03-23-加快語言模型生成速度-(1-2)-flash-attention-vXb2QYOUzl4.md)

# 加速语言模型生成 (1/2)：Flash Attention 深度解析

## 课程介绍与背景

大家好，那我们就来上课吧。今天的课呢，我们是想要跟大家讲，怎么加快语言模型的生成速度。那今天这一堂课呢，是预设你已经非常清楚语言模型内部的运作原理，你知道 Transformer 是怎么运作的。那这一堂课是要跟你讲说，在你已经知道 Transformer 是怎么运作的前提之下，我们怎么加快生成的速度。

所以今天这一堂课要讲的是生成的过程，今天这一堂课不是要讲训练的过程，而是假设一个语言模型已经被训练好以后，我们怎么加快它生成的速度。也就是在使用它的时候，你使用一个语言模型的时候又叫做**推论**，或者是又叫做 **inference**。在推论或者是 inference 的情况下，我们怎么加快语言模型生成的速度。

## Transformer 运作原理快速回顾

这边呢还是用两页投影片很快的讲一下语言模型的内部是怎麽运作的。那大家都知道说语言模型就是做文字接龙，你给它一个未完成的句子，它去预测接下来应该产生哪一个 token。那我们都知道说今天主流的语言模型的类神经网络架构就是 **Transformer**。那 Transformer 裡面有很多层，有很多个 layer，每个 layer 裡面呢，都有一个机制叫做 **self-attention**。Self Attention 让 Transformer 可以考量一整个输入的 Sequence 裡面所有的资讯。

那这个 Self Attention 这个 Layer 呢，它做的事情是这样的：输入一排向量，这边用 X1 到 X5 来表示，那它会做的事情就是输出另外一排向量 O1 到 O5。那这个 Self Attention 它是怎麽运作的呢？

- **产生 QKV 向量**：现在输入是 X1 到 X5，Self Attention 这个 Layer 做的事情是，首先先把 X1 到 X5 各乘上 3 个不同的 Transformation 的 Matrix，把 X1 变成 V1、K1、Q1，X2 变成 V2、K2、Q2，以此类推。那等一下在大多数的课堂裡面，我们都会省略叫这个从 X 变成 QKV 的过程，我们就假设说这个 Transformer 你已經知道输入的 X 就会变成 QKV 三个向量。
- **计算 Attention Weight**：那接下来怎麽做计算呢？我们用产生第 4 个位置的输出来作为例子，那其他位置也是用一样的计算方式。那你就把第 4 个位置的 query q4 跟前面所有的 key k1 到 k4 都去做 dot product，都去计算它的内积。这边计算出来的内积呢，我们写作 a1 到 a4。
- **Softmax 归一化**：这个内积计算出来以后呢，因为这个内积计算出来的数值它可能是负无限大到正无限大，所以我们会过一个叫做 **softmax** 的操作，把 a1 到 a4 做一下 normalization，让它变成数值介于 0 到 1 之间，然后合起来是 1。那我们把过 softmax 以后的这个 attention 叫做 a1 hat 到 a4 hat。我们用 a 代表做 dot product 以后算出来的数值，这个叫做 attention 的 weight，我们用一个 hat 代表说是经过 normalize，经过 softmax 以后的运算。
- **加权求和得到输出**：那有了这个 a1 hat 到 a4 hat 之后呢，每一个 a hat 都会去乘上它对应的 V 这个向量，然后做 weighted sum，那就是 Attention Layer 最终在第 4 个位置的输出。那这边这些都是假设你已經知道的事情。
## 加速方法的评估维度与课程大纲

那今天呢，就是会讲一系列加速 Transformer 运算的方法。那大家在看一个加速方法的时候，你要注意，你要问的事情是：**代价是什么？** 假设有一个人他跟你说他发明了一个加速的方法，那背后往往就是付出了某一些代价，他用一个你可能不太关心的资源来换取 Transformer 的加速。那这边通常会伴随什么代价呢？

- **改变计算精度**：有一些方法它伴随的代价是，它会改变 self-attention 的计算，也就是它不是真的计算 self-attention，它是一个 approximation，它是一个近似，你算出来的结果会跟原来的 self-attention 不一样。
- **模型绑定**：那有些方法的代价是，它是模型绑定的，也就是你要使用这个方法，你一定要训练特定的模型，你一定要对模型做客製化，才有办法使用这个方法，它不是一种随插即用的方法。
- **其他代价**：如果这两者都没有，那它其实可能还是付出了其他的代价，才有办法做到加速这件事情。
那今天呢，我们就是会完成这个表格。那今天其实会花最多时间讲的方法是在第一部分，我们会详细的解释 **Flash Attention** 这个技术。那其实今天多數的时候，你在使用语言模型的时候，你其实都已经有用到 Flash Attention，只是你不一定知道它是怎么做运算的。那第二部分呢，会讲一系列跟 **KV Cache** 有关的方法，那这个部分呢，虽然方法很多，但每个方法呢，就会用一两页投影片很快的带过去。

还有一个今天不会讲的方法叫 **Speculative Decoding**，那这也是一个非常有效的可以加快语言模型推论速度的方法。那之所以今天不講這個方法，是因为这个方法过去讲过了。那我们这一堂课呢，我们都主要讲新的内容，过去讲过的东西就留给大家自己再去看过去的上课录影。所以你可以在 2024 年生成式 AI 导论这门课的第 16 讲，找到有关 Speculative Decoding 的教学。那 Speculative Decoding 在我们的作业也是有的，所以你在做作业的时候，你还是需要知道什么是 Speculative Decoding。

---

## 第一部分：Flash Attention

好，那我们就开始讲 Flash Attention。

### Flash Attention 的核心优势

那 Flash Attention 最早的来源呢，是来自于这篇 22 年的 Paper，所以它也是一个上古时代的技術了。这个上古大神，它有什么样的威力呢？它非常的厉害：

1. **不会改变计算结果**：它不会改变 attention 的计算结果，所以它算出来的东西跟你知道的那个 attention 算出来的东西是一模一样的，它并不是一个近似。
1. **随插即用**：它是一个随插即用的方法，你可以直接把这一招套到任何有使用 self-attention 的 Transformer 上。所以它并没有绑定任何模型，它是一个可以直接套用在任何以 Transformer 为基础的语言模型上的方法。
1. **代价极小**：它的代价非常非常的小。
那我们就来看看 Flash Attention 是一个什么样厉害的技术。Flash Attention 最厉害的地方，它之所以能够达到加速的效果，它最核心的想法是：**它考量了 GPU 运算的底层逻辑**。所以我们需要先讲一下，当我们用 GPU 来运算的时候，背后发生了什么事，有什么是我们需要去关注的部分。

> **注**：以下并不是一个非常精确的说法，这边是为了让大家了解，是用比较简单的说法。而以下的说法也并不是 GPU 绑定的，很多高速运算应该都会有类似的概念。
### GPU 运算的底层逻辑

在 GPU 裡面呢，就是有一堆 **Execution Unit**，它们负责做运算。那这边就用一个小精灵当作 Execution Unit。那 Execution Unit 在 GPU 裡面呢，不是只有一个，而是有一把，所以这边用一个小精灵呢，它是三头六臂，代表说它有很多个分身，然后这些分身可以同时执行任务。

- **优势**：这些 Execution Unit 它厉害的地方就是，因为它们人多，所以它们运算呢，非常的快速。
- **限制**：但它们弱点是，它们的工作台太小了。所以它们工作台上能够存放的资料是有限的。如果你有一个非常大的矩阵，你有一个非常大的向量，你没办法直接摆上它的工作台。它每一次只能在工作台上放非常少量的数值来进行运算。
这个工作台呢，它就是 **SRAM**，或者是更精确的说，它是 **on-chip 的 SRAM**，这边我们直接叫它工作台。那在不同的高速运算裡面，其实这个名称可能会是不一样的。

既然工作台太小了，那如果今天有大量的资料，会被放在哪裡呢？会被放在一个**仓库**裡面。那这个仓库如果在 GPU 裡面，就是 **HBM**。有一个仓库它很大，它相对比较大，其实也不是无限的，它也不是可以放无限的内容。那即使在第二部分讲 KV Cache 的时候，我们会看到仓库的大小还是有限的，但是相较于工作台，仓库非常的大，可以放非常多的内容。

所以今天在真正做运算的时候，这一些小精灵它需要去仓库裡面，把资料搬到工作台上。它只能搬正好可以放得上工作台的资料，然后高速的做运算。东西一旦上了工作台之后，它们的速度是很快的，可以在一瞬间完成各式各样的运算，然后把运算的结果再搬回仓库。

所以整体而言，只要东西上了工作台，它就可以做高速运算，所以工作台上发生的一切，你就想成是在瞬间完成的。但是麻烦的地方是，**搬资料是花时间的**，搬资料是拖慢运算的瓶颈。

所以 Flash Attention 它想做的事情就是：我们能不能改变一下 self-attention 计算的演算法，算出来的内容是一样的，只是改变一些数值计算的顺序，**减少搬资料的次数**。让这个比较慢的瓶颈可以减少它发生的次数，那就可以让整体的运算更快一点。

### 一般 Attention 的计算流程

在讲 Flash Attention 之前呢，我们先讲如果是一般的 attention 是怎么做运算的。

今天我们已知有一个仓库，它可以放大量的数值，所以这些 query、这些 key 其实都是放在仓库裡面。那我们有一个工作台，我们用这个青色的区域代表是一个**非常小的工作台**。这边呢，我们要来做 attention。

> **注**：我们这边有一个 query，这个 query 要去跟一大排的 key 算 dot product。但實際上在运算的时候，GPU 可以同时处理多个 query。等一下在助教讲解裡面，助教的例子也是用多个 query 来跟大家解释的。那这边为了要让大家更容易了解这个演算法，所以我们就假设我们只考虑一个 query。但是有多个 query 的情况，其实也是可以直接从今天这一堂课裡面讲的内容去类推的。
1. 分块计算 dot product
我们不能够一次把所有的 key 都放到工作台上，因为这些 key 太多了。你要想像说，这个 key 的数量就是我们现在要处理的 sequence 的长度。今天这个语言模型，它如果当作一个 AI agent 来用，它的输入往往非常的長，可能是上万个、十万个、百万个 token，它的输入非常的長。所以你没有办法把所有的 key 通通放到工作台上。

所以你必须要**把这一整排 key**（我们把这一整排 key 的长度称之为大 L，代表现在输入的 sequence 的长度）**切成一个一个的 chunk**。那每一个 chunk，我们就假设裡面有 N 个 key。那这个 chunk 有多大，取决于你的 GPU 的工作台有多大，工作台大也许你可以切大一点，工作台小你就切小一点。

那这边呢 chunk 裡面有 N 个 key，这 N 个 key 呢，被放到工作台上，query 被放到工作台上。接下来一瞬間就完成了 query 跟所有 key 的 dot product。那这边用一个灰色的框框代表 Q 跟 K 的 dot product。算完以后，就把这一些 dot product 的数值再放回到仓库裡面。它们不能一直被存在这个工作台上，得清除空间，准备做其他的事情。

好，那第一个 chunk 读进来，算出 query 跟每一个 key 的 dot product，然后接下来再读第二个 chunk 进来，再读第三个 chunk 进来，以此类推。一次可以把一个 chunk 裡面所有 key 跟 query 的 dot product 都计算出来。

2. 计算归一化的 Attention Weight

那这边呢，这个每一个灰色的框框，我们称之为 **a*****i****，它是一个 attention 的 weight。那我们真正要的，拿来接下来运算的 Attention Weight 是有经过 normalized 的，我们加一个 hat 代表有经过 normalized。那这个 normalized 的算式是这个样子的：*

- 你要把这边的每一个 a*i 取 exponential，这是分子的地方。*
- 分母的地方，是把所有的 a*i 取 exponential 后的数值全部加总，放在分母的地方。*
- 然后你就可以得到 normalized 过的 Attention 的 Weight，也就是 a*i hat。*
**实际的运算细节与 Amax**：

这个是在理论上的计算方式，在实作上呢，你其实会再多加一个项叫做 **Amax**。在实际上取 exponential 之前，你会把 a*i 的数值减掉 Amax。那之所以要减掉 Amax，这个 Amax 是什么呢？Amax 是我们现在在做 dot product 的过程中，所有算出来的 dot product 的数值裡面最大的那一个。就我们所有算出来的 a*i 裡面最大的那一个，我们叫做 Amax。

我们把 a*i 减掉 Amax，就可以确保说 exponential 的这个指数项，它最大的数值是 0。因为 a*i 的数值到底有多大你不知道，它可以很大。那如果你在 exponential 指数项放一个很大的数值，你计算完之后可能会 overflow，可能会出各式各样的问题。所以把 a*i 减掉 Amax，然后确保指数项最大的数值就是 0。所以实际上运算的方法是用下面这个式子：*

\[

\hat{a}*i = \frac{e^{a*i - A*{\text{max}}}}{\sum*{j=1}^{L} e^{a*j - A*{\text{max}}}}

\]

等一下我们是假设我们使用下面这个式子，把 a*i 转成 a*i hat。

3. 分块计算 Softmax 的挑战与步骤

你可能想说，那我们就直接把一整排所有的 a*i，整个 sequence 裡面所有的 a*i，一次都放到工作台上。那工作台非常的 powerful，所以一瞬間可能就可以把这个 a*i hat 算出来，然后再把它读取出来就结束了。但你不可以做这样的操作，为什么不可以做这样的操作呢？你可能想说，这边是一些向量，我们都可以放一堆向量到工作台上了，这边这些只是 scalar，它只是一个一个数字，这边看起来只有 9 个数字，我应该可以放到工作台上吧？*

但你要注意，这边工作台上不能放任何跟长度 L，跟 sequence 的长度 L 有关的东西。你会觉得这些数值可以放到工作台上，是因为在这个例子裡面只放了 9 个数值。在实际上语言模型运算的时候，这个长度可能是 10 万，可能是 100 万，就算只是一个数值，100 万个数值你也是放不到工作台上面的。所以这边要注意，**工作台上不能放任何跟长度 L 有关系的东西**。

那既然不能够放跟长度 L 有关系的东西，要怎么从 a*i 变成 a*i hat 呢？那中间的过程就很繁琐了。

**第一步：找出 Amax**

我们怎么找出 Amax 呢？如果你只 load 一个 chunk 裡面的数值，你根本不知道谁是 Amax，因为你并没有把所有的数字都看过。所以找 Amax 的方法是這樣的：

1. 你一次先 load 一个 chunk 裡面的 a*i，然后看看这个 chunk 裡面的 a*i 谁最大。
1. 假设这个 chunk 裡面的 a*i 最大的数值是 D1，那就把这个 D1 的這個数字呢存在工作台上。你的工作台上呢，清出一个区间，这个区间呢叫做 D，这个 D 裡面呢存一个数值叫 D1。D1 就是在这个 chunk 裡面最大的那个 a，它不是全部最大的 a，它是这个 chunk 裡面最大的 a。*
1. 好，第一个 chunk 读完之后，接下来呢，把 D1 裡面存的数值留着，从第二个 chunk 裡面，再把 attention 的 weight 读进来。
1. 然后接下来看看这些读进来的 attention 的 weight 跟 D 谁比较大？跟 D 裡面放的数值（现在是 D1）谁比较大？也就是上一个 chunk 裡面最大的数值 D1 跟现在我们读进来的 attention 的 weight a*{n+1} 到 a*{2n}（我们假设一个 chunk 裡面有 n 个 a）谁比较大？把最大的那个存下来，叫做 D2。所以现在 D 这个区间裡面存的是 D2。
1. 这个过程就一直反复继续下去，那总共要做大 B 次。这个大 B 呢，是 L 除以 N，就是整个 Sequence 长度除以 Chunk 的大小。所以你要做大 B 次。
那做到最后第 B 次的时候，那你把存在 D 裡面的数值 D*{B-1} 跟现在在最后的 Chunk 读进来的这些 Attention Weight 比较大小，把最大的存到 D 裡面。最大的那个数值叫 D*B，把它存到 D 裡面。那现在 D 存的值就会是 Amax，因为我们每次都把我们看到目前为止最大的那个 a 放到 D 裡面。当我们把所有的 chunk 都读过一遍的时候，这个 D 这个区域裡面存的就是 Amax。所以我们找到 Amax 了。

**第二步：计算分子与分母**

找到 Amax 以后呢，你就把 Amax 那个数值仍然放在你的工作台上面，然后再从第一个 chunk 开始读起。

- **计算分子**：把裡面读进来的这个 a*i 呢，减掉 D，再取 Exponential。那我们就可以得到分子这一项：Exponential(a*i - Amax)。我们把它叫做 a*i prime。*
- **计算分母**：分母那一项是要把分子的每一项，也就是 a*i prime 通通都加起来。那找出总和的方法跟刚才取出最大值的方法其实是非常类似的，就是每次读一个 chunk 进来，然后把这一项裡面的数值全部加起来存到 S 裡面。*
**第三步：计算 Attention Weight**

我们现已经有分母这一项，又有 a*i prime 分子这一项，我们就把分子除上分母，然后再把除完的结果读出来，就得到 a*i hat。

经过这一番折腾以后，我们终于从 a*i 变成了 a*i hat，中间已经读写过好几次仓库，我们去仓库搬过好几次东西，把工作台上的东西放进仓库，这是一个很花时间的过程。

4. 加权求和得到最终输出 O

好，终于算出 a*i hat 以后，还没有到结束。这个时候呢，你要去仓库去搬 V，去搬那些 value 的向量。那把 a*i hat 跟 V 呢做 weighted sum。那一次一样一次，你只能够读一个 chunk 的资料上去工作台。那你就把这一堆 V 读上工作台，你把 a*i hat 读上工作台，然后把 V 呢跟 a*i hat 呢算 weighted sum，那你就得到 O。O 就是我们最重要的输出，也就是这个 V 对 a*i hat 的 weighted sum。*

- 一开始我们只能算第一个 chunk 的 O，那所以它还不是最终的答案。
- 好，那有第一个 chunk 的 O 以后呢，接下来就把第一个 chunk 的 O1 再加上第二个 chunk 裡面 a*i hat 乘上 V 的 weighted sum。那这边呢总共有 N 个数值，N 个 weighted sum 的结果，加上 O1 得到 O2。*
- 这个过程就反复继续下去，直到最后 O*{B-1} 加上这一个 chunk 裡面 a*i hat 跟 V*i 的 weighted sum 得到 O*B。这个 O*B 就是你最终 attention layer 在某一个位置的输出。这个就是 Q、K、V 做 attention 以后最终得到的结果。*
你可以观察到说，在整个过程中，我们对仓库做了多次的读写。所以 Flash Attention 要问的问题就是：真的需要读写这么多次吗？有没有减少读写次数的方法？

### Flash Attention 的核心优化思路

我们先讲一个 Flash Attention 的简化版，等一下再讲真正的 Flash Attention。这个简化版的想法是这个样子的：这 a*i 到 a*i hat 要读好几次，真的需要读那么多次吗？应该可以减少读取的次数。

怎么减少读取的次数呢？这个 Amax 跟分母这一项 summation 可以一次就被找出来。就是把这边的 a*i 读一次进去 memory，就同时算出 Amax 跟这一项 summation。那刚才我们必须要把这两项分开算，因为你看后面这一项是 dependent on 前面这一项的，你没找出 Amax，你没有办法算这个 summation。但是神奇的地方就是，其实是有办法把 Amax 跟这个 summation 的结果一次找出来的，就算后面这一项要 depend on Amax 的数值。*

技巧：动态更新最大值与总和

这边是怎么做的呢？这边是这样子的：

1. 先把一个 chunk 裡面的数值读进来，然后看看这个 chunk 裡面谁最大的数值，最大的数值呢我们把它叫做 D1。
1. 然后接下来呢，我们就假设 D1 就是最大的那一个 a*i。你想说怎么可能，它只是一个 chunk 裡面最大的 a*i，还不是整个 sequence 裡面最大的 a*i。那我们不管，我们就假设 D1 就是 Amax 来做接下来的操作。*
1. 好，所以我们取 Exponential(a*i - D1)，假设它就是 Amax，再把它全部通通都加总起来，得到 S1 = summation over i=1 to N Exponential(a*i - D1)。
这边我们假设说 D1 就是 Amax。那如果 D1 真的就是 Amax，那就没事，你算出来的值是对的。但是实际上并不是，那我们就来看看 Flash Attention 要怎么解套这个问题。

那我们现在呢算出了 D1，它是这一堆数值裡面最大的；我们算出来 S1，它是假设说我们把 Amax 取代成 D1 算出来的总和。接下来我们进入下一个 chunk。下一个 chunk 裡面会有上一个 chunk 在工作台上留下来的数值 D 和 S。

1. 我们把这个第二 chunk 的数值读进来，跟原来存在 D 裡面的值，也就是 D1，比一下大小。你可能会找到更大的数值，叫做 D2。
1. 那么这边就假设说，我们找到了一个不一样的数值叫做 D2。在这个 chunk 裡面有数值是比第一个 chunk 还要更大的。好，那显然我们应该把 D2 当作 Amax，前面把 D1 当作 Amax 是不对的，D2 至少它比 D1 大呢，所以它更接近 Amax。所以我们把 D2 当作 Amax。
1. 然后呢，我们就算 Exponential(a*i - D2)，然后呢，我们把 Exponential(a*i - D2) summation over i = N+1 to 2N。把这个 chunk 裡面每一个数值取 Exponential(a*i - D2)，把它加起来。*
1. 然后接下来要怎麼处理呢？也许直觉的方法是把它跟之前算出来的 summation S1 直接加起来变成 S2。但是问题是前面的这一项 S1，它是假设 D1 是 Amax 算出来的，后面这边我们是假设 D2 是 Amax 算出来的。我们现在已经知道 D1 是 Amax 这件事就是错的，因为 D2 是比 D1 大的。所以这个 S1 显然就是错的，在前一个 block 算出来的数值，前一个 chunk 算出来的数值是错的。
但是怎么办呢？你不能够把前一个 chunk 的这些数值再读进来重算，这是不可以的，这就是浪费读写的时间。所以要想个办法，直接根据现有的 S1 的数值，做一个调整，让错误变成正确了，好像那个错误从来没有发生过。

**关键的调整公式**：

所以这边就做了一个调整，这个调整说穿了也不值钱，就是一个式子：**把 S1 后面乘上 Exponential(D1 - D2)**，就好像什么事都没有发生，把刚才把 D1 当作 Amax 的痕迹直接抹掉，变成把 D2 当作 Amax。

为什么把 S1 后面乘上 Exponential(D1 - D2) 就可以把 D1 的影响移除，改成 D2 视为 Amax 呢？那如果你把 S1 带进去，你就可以很轻易地看出这件事来：

\[

S1 \times e^{(D1 - D2)} = \left( \sum*{i=1}^{N} e^{(a*i - D1)} \right) \times e^{(D1 - D2)} = \sum*{i=1}^{N} e^{(a*i - D2)}

\]

所以第一项 S1 乘上这些数值以后，你现在会变成 summation over Exponential(a*i - D2)。就跟我们这边在 N+1 到 2N 的 summation 算的一样，也是 Exponential(a*i - D2)。所以最终合起来，这个 S2 就变成了 summation over i=1 to 2N Exponential(a*i - D2)。你就好像是把 D2 当作 Amax 去计算 i=1 到 2N 的总和。*

所以我们其实可以在不看过去的这些数值的情况下，直接把 S1 做一个调整，就好像我们拿 D2 当作 Amax 来计算一样。所以这个就是 Flash Attention 核心的一个技巧。那等一下就是反复用这个技巧来减少读写的次数。

算法迭代过程总结

好，那我们现在呢，已经知道在一个 chunk 裡面要怎么做运作。那我们举了第一个跟第二个 chunk 的例子，那对接下来的 chunk 来说，它的算法是一模一样的。我这边只是把刚才讲过的事情再复述一次：

在第 k 个 chunk 的时候，我们做的事情就是：

1. 把第 k 个 chunk 裡面的 a*i 读进来，跟 D 裡面存的值比一下，看看谁最大，那就把最大的值取出来，叫做 D*k。
1. 然后接下来呢，我们算 Exponential(a*i - D*k)，并且把 Exponential(a*i - D*k) summation over 第 k 个 chunk 裡面所有的数值。
1. 之前存在 S 裡面的数值叫 S*{k-1}，它需要做一个变化，才能够让它配合新的这个 D*k。所以 S*{k-1} 要乘上 Exponential(D*{k-1} - D*k)，它才能够配上新的 Exponential(a*i - D*k) 这些项，然后就得到 S*k。
反复这个操作，直到你到达了最后一个 chunk（第 B 个 chunk）。然后接下来的操作都是刚才讲过的：读一串 a*i 进来，比比大小。那最大的东西呢就是 D*B，那这个 D*B 呢其实就****是 Amax****。在我們已经把所有 chunk 都扫过一遍以后，最终会放在这区域的这个数值，我们每次都会拿这个区域的数值去跟现在所有裡面这些 chunk 读进来的数值去比大小。那在所有的 chunk 都比较过以后，放在这个蓝色区域裡面的就是 Amax。*

我们已经有了 Amax 了。然后接下来 Exponential(a*i - D*B)，因为 D*B 已经等于 Amax，所以这样算出来的数值是正确的。然后接下来呢，我们 summation over 最后一个 chunk 的数值（指数 Exponential(a*i - D*B)），都拿出来。然后前面留下來的数值 S*{B-1} 乘上 Exponential(D*{B-1} - D*B)，做一个变化，做一个调整，再加上后面这一项得到 S*B。然后这个 S*B 呢，就是我们需要的分母这一项了，因为现在 D*B 已经是 Amax，所以这个计算会给我们 summation over i=1 to L Exponential(a*i - Amax)。

经过这一番操作，存在 S 裡面的数值就已经是分母这一项。所以我们现已有 Amax，有分母这一项。接下来要计算 a*i hat，感觉就是举手之劳。所以现在工作台上有 D 和 S，这个 D 就是 Amax，然后这个 S 就是分母这一项。接下来你要做的事情，就是把 a*i 的值读进来，然后取 Exponential(a*i - D)，这个 D 就是 Amax，然后再除掉分母这一项，除掉 S 就是这个 summation over i=1 to L。然后你就对每一个 chunk 的数值做反复一样的操作，你就得到 a*i hat。

所以经过刚才上述这一番操作之后，我们已经把从 a*i 到 a*i hat 这一连串本来要做多次读写的过程，变成就是**两次读写**。刚才只从这个仓库裡面搬两次 a*i 的数值进来，就把 a*i 变成 a*i hat。所以我们可以从多次的读写变成两次的读写。*

可能想说这样是挺不错的，所以前面要把 Q 跟 K 做一次 dot product 得到 a*i，然后两次读写就得到 a*i hat，然后做 weighted sum。那感觉是比原来完全没有想就直接 implement 的方法还要更有效率一点。

### 终极优化：直接计算 O，跳过 Attention Weight

但这并不是 Flash Attention 的全部。Flash Attention 最后神奇的地方就是，它问了一个关键的灵魂的拷问：**一定要算出 attention weight，你才能够计算最后的 weighted sum O 吗？**

它跳过了把 a*i hat 真正算出来这个步骤，最后直接得到 O。所以如果你用 Flash Attention，一个神奇的地方是你读不出 attention 的 weight。就很多人在分析 Transformer 的时候，你会想说我来画一个 attention 的 matrix，然后看说这个 attention weight 的数值。但假设你今天选择计算 attention 的方式是 Flash Attention，然后你用 Hugging Face 的模组，它就会报错给你，它会告诉你说没有 attention weight 可以读取。因为神奇的就是 Flash Attention 这个方法，它可以跳过计算真正的 attention weight a*i hat 这件事情，直接给你 O。而它得到的那个 O 的结果，跟有先算 a*i hat 再得到 O 的结果，是理论上一模一样的。*

一步到位的计算流程

好，那这个 Flash Attention 是怎么做的呢？Flash Attention 的做法是這樣，它想要做的事情是**一步到位**：Q、K、V 通通放到这个工作台上之后，我们做一次运算，就得到最终的结果。

那我们来看看这一连串的运算最终是怎么达成的。

1. **初始 chunk 的初步计算**：
前面的操作其实跟刚才差不多。Q 要跟一个 chunk 裡面的 K 都去算 dot product，然后找出 dot product 最大的那个数值叫做 D1，存到 D 裡面。然后取 Exponential(a*i - D1) 当作 S1，S1 就是 summation over i=1 to N Exponential(a*i - D1)。这里是我们刚才有看到的操作。最后它要做的事情是，我们直接把 V 在这个时间点就读进来，来计算 weighted sum。我们直接把 V*i 去乘 Exponential(a*i - D1) 除以 S1，然后 summation over i=1 to N 得到 O1。

你可以想说，这个 weighted sum 对吗？这个 weighted sum 的 weight 它根本就不是我们要的那个 attention，它根本就不是 a*i hat。那没有关系，等一下会想办法修补这个问题。所以这边是****将错就错****继续做下去。所以要记得，这边这一项的 attention weight 它是错的，它不是真正的 a*i hat。比如它分子的地方有错，因为 D1 不是真正的 Amax；它分母的地方有错，因为你看 S1 它是只有 summation over i=1 to N，它的 Amax 也是错的，它是 summation over 这个区间，它还没有 summation over 整个 sequence，但它就被当作分母来用了。

1. **后续 chunk 的修正与迭代**：
接下来我们就看这个 Flash Attention 怎么修补前面的错误。它的做法是这个样子的：

1. **修正 O1 并计算新的加权和**：
怎么把 O 算对呢？刚才我们已经算出 O1，它是前面这个 chunk 裡面的 weighted sum，是前面这个 chunk V 对一个错误的 attention weight 的 weighted sum。那现在我们算出 S2，这个 S2 虽然它可能仍然不是一個正確的分母，但它至少比 S1 更正確一点。所以我们现在新的 attention weight 可以写作 Exponential(a*i - D2) 除以 S2。虽然它不是很正确，但也许比这一项还要更正确一点。所以我们把第二个 chunk 裡面的 V 拿来对 Exponential(a*i - D2) 除以 S2 做 weighted sum。

那前面的 O1 怎么办呢？前面的 O1 已经算错了，所以我们要抹掉 S1 和 D1 存在的痕迹。我们想把 S1 想办法换成 S2，把 D1 想办法换成 D2。我们要做的事情就是把 (Exponential(a*i - D1) / S1)  vi 换成 (Exponential(ai - D2) / S2)  v*i。

这个置换要怎么做到呢？这个置换是这样的：

所以把 O1 乘上 (S1 / S2) 再乘上 Exponential(D1 - D2) 以后，这个本来 O1 跟这一项算的差异，这个 D1、D2、S1、S2 所造成的差异，就被弥平了。你得到的结果就是 summation over i=1 to 2N (Exponential(a*i - D2) / S2)  vi。所以这个就是 Flash Attention 的精神。*

1. **迭代至最终结果**：
那这个就反复继续下去。在第 k 个 chunk 做的事情就跟刚才一样：算 attention 的 weight。我们这边就没有把 query 画出来，你想像有个 query 进来，跟这个 chunk 裡面的 k 做 dot product 得到一團 dot product 以后，找出最大的那个就是 D*k。然后我们要取这个 summation，要把原来的 S*{k-1} 做一些修正，然后再加上新的 Exponential(a*i - D*k) 得到 S*k。然后接下来我们要算 O，O*k 是原来的 O*{k-1} 做修正（这个修正项），加上我们新得到的这个 chunk 裡面的 V 的 weighted sum。*

所以这边我们的过程就是不断的修正前面的错误，再加新的东西。前面有错没有关系，因为接下来总是能够修正回来。

所以在最后第 B 个 chunk 做的事情就是，一个 chunk 资料读进来，算 weighted sum，找出最大的就是 D*B，然后接下来呢再算 S*B，那要把前面的 S*{B-1} 呢做一个修正，再加上新的数值。O 也一样，最终算出来的 O*B 就是前面的 O*{B-1} 做一连串的修正，再加新的数值。*

最后 D 裡面存的就是 Amax，S 裡面存的是 a*i hat 的分母项，但这两项你根本就不在意，你根本就不要它。你要的是什么？你要的是 ****O****。这个 O 它是 summation over i=1 to L，也就是整个 sequence，然后所有的 v*i 前面乘上正确的 attention。就这一连串的修正会让我们得到正确的 attention 跟 v*i 的 weighted sum 的结果。虽然在整个过程计算的过程中，attention weight 从来没有被真正的算出来，但是我们最后得到了 weighted sum 的结果。这个就是 ****Flash Attention****。*

好，那这边就是简单的讲了 Flash Attention 的演算法。然后等一下在助教的讲解，还有在助教的那个作业中呢，其实还有更详尽的说明。

---

### 实验验证：Flash Attention 的速度优势

那这边呢，就是有一个範例程式，让大家感受一下 Flash Attention 真正用起来感觉是什么样子。好，那这边就是比较一下有 Flash Attention 跟没有 Flash Attention 速度的差异。

环境设定与参数初始化

我们先用 typical 的 Colab 的使用，先 import 一些东西。然后呢，我们先确认一下 GPU 的环境，看看现在这个 Colab 上面给我们什么样的 GPU。我们先跑一下前面这两段，这个起始的时候是需要花一点时间的。那这边呢，我们有 A100，然后这个 A100 呢，它的 memory 是 80GB。大家注意哦，这个所谓的 memory 80GB 是仓库有 80GB，工作台一直都是很小的，工作台通常都是比如说十几 MB 而已。

接下来就是实作一下两种不同的 attention：

1. **Naive Attention**：没有用 Flash Attention，就是一般你直觉上的那个算法。
1. **Flash Attention**：使用 Flash Attention 算法。
其实背后都去呼叫一个 PyTorch 的模组，PyTorch 裡面有一个东西叫做 `scaled`*`dot`*`product`*`attention`**。那这个 **`scaled`*`dot`*`product`*`attention` 你可以去设置说，你要用一般的 attention 的算法，还是用 Flash Attention。那其实如果没有做特别的设置，它一般就是直接用 Flash Attention。所以今天你一般在跑这个 Transformer 的时候，如果你没做什么特殊的处理，往往就是预设，其实你已经用了 Flash Attention 了。

这两个函式都是吃 QKV，然后 causal 的意思是，我们是一个 language model，这个 language model 只看前面的东西，它不是一個 bidirectional 的 attention。QKV 读进来以后，唯一不同的地方，只是在 run Naive Attention 裡面，我们设定一个叫做 math 的 figure，意思就是说我们算简单的 Naive Attention。然后这边设一个 Flash Attention，意思就是说我们要用 Flash Attention 来运算这个 QKV。

**数值验证**：

接下来就是做一下数值的验证，想要告诉大家说 Flash Attention 跟 Naive Attention 它算出来的数值是一模一样的，或几乎是一样的。

那这边就是初始化我们的 QKV。那这边就设定几个参数：

- B (batch size) = 4
- H (attention head 数量) = 8
- L (sequence 长度) = 256
- D (QKV 的 dimension) = 64
这个 sequence 的 256 其实是一个相对比较小的数值，你其实实际上用的时候，256 其实是太短了。好，这个接下来，就 random initialize QKV 这三个东西。这边并不是绑定某一个 language model，这个 QKV 它的数值就是随机设进去的，因为我们现在并不是要真的跑一个 language model，我们只在意计算的速度而已。

好，那我们就在量计算的速度之前，我们分别执行 Naive Attention 跟 Flash Attention，看看它们算出来的数值一不一样。它们算出来的数值一个存在 out naive 裡面，一个存在 out flash 裡面。然后我们看看这两个输出，它们最大的差异有多大。我们执行一下，最大的差异你会发现非常的小，是 **10 的 -7 次方**。它当然还是会有一點点的差异，你在做这种不一样运算的时候，因为背后运算机制的差别，所以总是会有一點点的差异。但这个差异你看不管怎麼算，它都非常的小，都在 10 的 -7 次方左右。

速度对比实验

接下来呢，我们就真的来比较一下有没有使用 Flash Attention 它时间的差异。我们这边先写一个函式叫 `benchmark`*`attention`**，它是为了要去计算不同的 attention 花的时间。它就是吃 QKV 当作输入，它还会吃一个 mode 当作输入，代表我们现在要跑 Naive Attention 还是 Flash Attention。那这边有另外两个参数 warm up 跟 repeat，你回去可以自己调这两个数值。*

- **warm up**：是说在真正开始计算之前，先试跑一次。因为你其实不知道那个 Colab 背后 GPU 是怎么被调度的，怎么被使用的。所以你先跑一次，然后让它如果要载入什么 library，先自己去载入一下。那至於要 warm up 几次才行，那这个你可以自己试试看。那我这边呢，为了加速，所以我就只跑一次。
- 接下来呢，我们就开始计时，然后呢，我们把同一种 attention 跑三次（但你可以跑更多次，计算的結果可能会更准一点）。然后呢，我们就结束计时，然后就计算看看说现在每一次的 attention 我们需要花多长的时间，那这边用毫秒作为单位。
那我們这边呢，就是不同的长度 64、128、一直到 4096，然后来看看在不同的长度之下，这些 Flash Attention 可以加速多少。

那我们就开始跑了。这个跑其实蛮快的，就不同的 sequence 长度 64、128、256、512... 如果是 Naive Attention 花了多少毫秒，如果是 Flash Attention 花了多少毫秒，然后把这两者相除，告诉你说 Flash Attention 相较于没有用 Flash Attention，它加速了多少。

你发现它加速可以加速到 **9 倍**左右，在 sequence 设为 4096 的时候。那 Flash Attention 呢，它光靠着这个减少搬运的次数，你看它可以加速到 8 到 9 倍左右，所以这是一个非常有用的招数。那它的代价很小，它的代价只有演算法复杂，然后它的演算法中为了要修正，所以做了一些额外的运算，但是瑕不掩瑜，这个减少搬运次数真的是非常划算，让你的速度能够增加很多。

### 在真实语言模型上的测试

好，那到目前為止，我们是一个 toy 的 example，只是拿假的 QKV 来进行计算。那接下来我们用一个真正的语言模型，来比较有没有装 Flash Attention 的时候它的差异。那我們这边呢，用这个 **Yi-34B**。那你用别的模型试出来的结果，其实也都是差不多的。

好，那我们先把这个模型呢，载下来。那载这个模型呢，从 Hugging Face 载这个模型呢，是要花一点时间的。好，这边呢，真的就需要让它跑一下。在它跑的过程中呢，我们来看看接下来我们会做什么。

那接下来我们会做的事情是，首先我们会先存一个非常长的字串，那这个等一下就是我们要丢给 language model 的 prompt。那我们这边写 `long text`，因为它非常非常的长。我们就是把一个无聊的句子反复反复很多次，然后看看会怎样。我们把这个句子反复个 100 次。那等一下我们是用 Hugging Face 上的 pipeline 来呼叫 language model，我们这个 sequence 它有 **7300** 个 token。

短序列测试 (7300 tokens)

接下来我们就来开始进行测试。首先先测试没有使用 Flash Attention 的状况。今天我們用的是 Hugging Face，所以我们是用一个叫做 `pipeline` 的函式来呼叫 language model。这边有一个 pipeline 叫做 `pipeline`*`eager`**，所谓 pipeline eager 的意思是，我们一开始在做这个设定的时候，这个 **`pipeline`*`eager` 的设定就告诉我们说这个 attention 的 implementation 要用 eager 这个方法。所以 eager 这个方法就是不用 Flash Attention。而 eager 它是着急的意思，但是这边反正就是 eager 代表没有用 Flash Attention。然后如果你没有做特别的设置，其实预设是用 Flash Attention。所以如果你不要用 Flash Attention，你其实是需要特别做设置的。

然后我们现在就用没有用 Flash Attention 的 pipeline 来做 inference。我们这边只让它 output 一个 token 而已，就输入一个非常长的 sequence，只 predict 下一個 token，来看看花了多少的时间。花了 **0.15 秒**。

然后我们接下来呢，换成用 Flash Attention。然后这边呢，`pipe`*`sdpa`** 就是有用 Flash Attention。如果有用 Flash Attention，同样只输出一个 token，你发现也没快上多少，为什么呢？因为我们的 sequence 太短了。因为其实在一个 language model 裡面，它有非常非常多不同的项，除了 attention 以外，你还有大量的 feed forward network，甚至刚才在计算的时候，光是把文字转成 embedding 也是需要时间的，embedding 转回文字也是需要时间的。有很多东西它其实都需要时间。所以如果是 sequence 太短的时候，Flash Attention 呢，也没有什么效果。*

长序列测试 (73,000 tokens)

那我们这个改成 1000 次（句子重复 1000 次），给它 **7 万**个 token 看看。好，这边花了 2 秒（没有用 Flash Attention 的情况下），有用 Flash Attention 呢，花了 1.3 秒。所以你看，有用 Flash Attention 还在 sequence 长的时候，它的速度是加快很多的。

极限测试与内存溢出

那你可能会想说，那再长一点行不行呢？再长一点，我们刚才呢用 1000（重复 1000 次，即 7.3 万个 token），如果我是 1 万（重复 10000 次）会怎么样呢？那这样就有这个 **73 万**个 token 了。

跑一下，看会发生什麼事。哇，没办法跑啊，这个 **CUDA out of memory**。它 out of memory 并不是工作台的 memory，而是那个仓库。所以我刚才说仓库虽然很大，它还是有极限的。当 sequence 太长的时候，你终究会把仓库撑爆。那 sequence 太长为什么会撑爆仓库，那就是我们下一堂课，讲 KV Cache 的时候，再跟大家讲。
