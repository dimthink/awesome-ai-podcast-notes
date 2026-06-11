---
title: "【機器學習2021】Transformer (上)"
channel: "李弘毅"
published: "2021-03-26"
source_url: "https://www.youtube.com/watch?v=n9TlOhRjYoc"
video_id: "n9TlOhRjYoc"
rating: 5
language: "中文"
word_count: 11615
duration: "32:48"
---

# 【機器學習2021】Transformer (上)

- **Channel:** 李弘毅
- **Published:** 2021-03-26
- **Source:** https://www.youtube.com/watch?v=n9TlOhRjYoc
- **TL;DR:** Transformer作为强大的Seq2Seq模型，以Encoder-Decoder架构和自注意力机制，解决了语音、文本等多种序列任务的输出长度不确定性问题，其设计仍在不断优化。
- **Rating:** 5

## 版本

- [原始文稿](2021-03-26-【機器學習2021】transformer-(上)-n9TlOhRjYoc.transcript.md)

# 深度解析Transformer：从Seq2Seq的普适性到Encoder的精妙设计

## 材料信息

- **标题**：【機器學習2021】Transformer (上)
- **作者/来源**：李弘毅
- **类型**：YouTube 视频字幕
- **关键元数据**：机器学习课程，2021年，Transformer系列讲座第一部分
## 开篇引入

在机器学习的浩瀚星空中，Transformer无疑是一颗璀璨的明星，它不仅彻底改变了自然语言处理（NLP）的格局，更以其强大的泛化能力，渗透到语音、图像乃至更广泛的序列建模领域。李弘毅教授的这堂课，正是带领我们深入探索Transformer奥秘的起点。它不仅仅是技术细节的罗列，更是一场思想的盛宴，揭示了Seq2Seq模型如何从一个朴素的概念，演变为解决无数复杂问题的“瑞士军刀”，以及Transformer如何在这一框架下，通过精巧的内部设计，将性能推向新的高度。如果你曾对BERT、GPT等模型感到好奇，那么理解Transformer，就是打开这些“变形金刚”核心秘密的钥匙。这篇深度文章将带你超越字幕的表层信息，沉浸于李教授富有洞察力的讲解中，感受其思考的脉络，领略Transformer的独特魅力。

## 详细内容

### Transformer的引言与核心定位 `[开篇介绍]`

**核心观点**

Transformer是机器学习领域中一个至关重要的模型，与BERT等前沿技术紧密相关，其本质是一个强大的Sequence-to-sequence（Seq2Seq）模型，能够处理输入和输出序列长度不确定的任务。

**深度阐述**

李弘毅教授开宗明义地指出，Transformer这个词在课程中已被提及不下N次，其重要性不言而喻。他幽默地提醒听众，Transformer的英文原意就是“变形金刚”，暗示了其在模型结构和应用上的强大“变形”能力。更重要的是，Transformer与后续将要深入探讨的BERT模型有着“非常强烈的关系”，甚至可以说BERT就是Transformer的Encoder部分，这预示着Transformer是理解当前许多先进NLP模型的基础。

那么，Transformer究竟是什么？教授给出了最核心的定义：它是一个**Sequence-to-sequence (Seq2Seq) 模型**。这个缩写“Seq2seq”在机器学习领域随处可见，它描述的是一类模型的通用能力：接收一个序列作为输入，并输出另一个序列。然而，Seq2Seq模型的独特之处在于，它能够处理**输出序列长度不确定**的任务。

为了更好地理解这一点，教授回顾了之前课程中涉及的序列处理任务：

- **作业二**：输入序列与输出序列长度相同（例如，对序列中每个元素进行分类）。
- **作业四**：输入序列，但只输出一个单一的结果（例如，对整个序列进行情感分类）。
- **作业五（当前）**：输入一个序列，输出另一个序列，但**输出序列的长度由机器自行决定**。这正是Seq2Seq模型的核心魅力所在，也是它能够解决更复杂、更开放性问题的关键。
这种“机器自行决定输出长度”的能力，使得Seq2Seq模型在许多实际应用中大放异彩，因为它摆脱了传统模型对输入输出长度严格匹配的限制，更贴近人类处理信息的方式。

**延伸思考**

这种对“输出长度不确定性”的强调，实际上触及了序列建模的本质挑战。在现实世界中，我们很少能预先知道一个问题的答案会有多长。例如，翻译一句话，摘要一篇文章，或者生成一段对话，其输出的长度都是动态变化的。Seq2Seq模型正是为了应对这种动态性而生，为后续的Transformer奠定了基础。

**精华收获**

Transformer是当前机器学习领域的核心技术之一，其作为Seq2Seq模型的身份，意味着它擅长处理输入和输出都是序列，且输出长度不确定的复杂任务，是理解BERT等模型的基础。

### Seq2Seq模型：从概念到广泛应用 `[Seq2Seq模型的核心与应用]`

**核心观点**

Seq2Seq模型以其“输入序列，输出序列，且输出长度由机器决定”的特性，成为解决语音识别、机器翻译、语音翻译、聊天机器人、甚至看似不相关的文法剖析和多标签分类等多种复杂任务的强大通用框架。

**深度阐述**

教授通过一系列生动的例子，详细阐述了Seq2Seq模型在不同领域的广泛应用，并强调了其核心能力——**机器自主决定输出长度**。

应用案例一：语音识别 (Speech Recognition) `[语音识别：01:10-02:10]`

- **核心观点**：将声音信号（向量序列）转换为文字序列，输出文字长度不确定。
- **深度阐述**：在语音识别中，输入是声音信号，这在机器学习中通常表示为一系列的向量。输出则是对应的文字序列。关键在于，一段声音信号的长度（大T）与它所对应的文字序列的长度（N）之间并没有固定的比例关系。例如，说“你好”可能声音很短，但文字是两个字；说“非常感谢”声音较长，文字也较多。Seq2Seq模型允许机器根据声音内容，自行决定需要输出多少个文字，从而准确地将语音转化为文本。
应用案例二：机器翻译 (Machine Translation) `[机器翻译：02:10-02:50]`

- **核心观点**：将一种语言的文字序列翻译成另一种语言的文字序列，输出长度不确定。
- **深度阐述**：机器翻译是Seq2Seq模型最经典的用例之一。输入是一个语言的句子（文字序列，长度N），输出是另一种语言的句子（文字序列，长度N'）。同样，N和N'之间没有简单的数学关系。例如，“机器学习”翻译成“machine learning”，中文四个字，英文两个词。机器必须自主判断目标语言的句子应该有多长。
应用案例三：语音翻译 (Speech Translation) `[语音翻译：02:50-08:50]`

- **核心观点**：直接将一种语言的声音信号翻译成另一种语言的文字，尤其适用于没有文字的语言，避免了中间的语音识别步骤。
- **深度阐述**：这是一个更复杂的应用。用户对着机器说一种语言（例如英文“machine learning”），机器直接输出另一种语言的文字（例如中文“机器学习”）。教授提出了一个关键问题：为什么不先做语音识别（英文声音转英文文字），再做机器翻译（英文文字转中文文字）？答案在于，世界上有超过7000种语言，其中超过半数没有文字系统。对于这些语言，根本无法进行语音识别，因为没有文字作为识别目标。但语音翻译提供了一种可能性，直接将这些无文字语言的声音翻译成有文字的语言，从而实现跨语言沟通。
教授以**台语**为例进行了深入探讨：

应用案例四：语音合成 (Speech Synthesis) `[语音合成：08:50-10:50]`

- **核心观点**：将文字序列转换为声音信号，是语音识别的逆过程，同样可由Seq2Seq模型实现。
- **深度阐述**：语音合成是语音识别的“反向操作”。输入是文字序列，输出是声音信号。教授展示了利用“台湾媠声”数据集进行台语语音合成的例子。虽然目前的端到端（End-to-End）模型尚未完全成熟，通常需要先将中文文字转换为台语的台罗拼音（类似KK音标），再将拼音转换为声音信号。但从拼音到声音的转换部分，本质上就是一个Seq2Seq模型（如Echotron，其内部也类似Transformer）。这再次证明了Seq2Seq模型在处理序列转换任务上的强大能力。
应用案例五：聊天机器人 (Chatbot) `[聊天机器人：10:50-12:00]`

- **核心观点**：将用户的文字输入转换为机器的文字回复，是典型的文字到文字的Seq2Seq任务。
- **深度阐述**：聊天机器人是Seq2Seq模型在NLP领域最直观的应用之一。输入是用户的文字序列，输出是机器的文字回复序列。由于文字本身可以被表示为向量序列，因此Seq2Seq模型能够完美地处理这类任务。训练聊天机器人需要收集大量的对话数据，例如电影、电视剧台词，通过学习“输入Hi”对应“输出Hello, how are you today”这样的模式来训练模型。
Seq2Seq的普适性：QA任务的视角 `[QA任务：12:00-15:50]`

- **核心观点**：许多NLP任务，即使表面上与问答无关，也可以被巧妙地转化为问答（QA）任务，进而利用Seq2Seq模型解决。
- **深度阐述**：教授提出了一个极具启发性的观点：**许多NLP任务都可以被视为Question Answering (QA) 任务**。QA任务的核心是：给定一段文章，提出一个问题，机器给出答案。
通过这种转化，所有这些任务都变成了“输入一个长序列（文章+问题），输出一个短序列（答案）”的Seq2Seq问题。这意味着，一个通用的Seq2Seq模型，只要经过适当的训练，理论上可以解决各种各样的NLP问题。

然而，教授也强调了一个重要的**警示**：

Seq2Seq的普适性：更“狂野”的应用 `[更狂野的应用：15:50-20:50]`

- **核心观点**：Seq2Seq模型甚至可以“硬解”那些看起来与序列无关的任务，如文法剖析和多标签分类，通过巧妙地将非序列结构转化为序列表示。
**个人感受**

李教授在讲解这些应用时，语气中充满了对Seq2Seq模型强大能力的赞叹，尤其是“硬train一发”、“很狂”、“上古神兽等级的文章”等词汇，生动地传达了科研人员在面对突破性技术时的兴奋和惊喜。他与Oriol Vinyals的对话更是点睛之笔，揭示了有时最直接、最朴素的方法，反而能带来意想不到的成功，也鼓励听众不要被固有思维所束缚。

**延伸思考**

Seq2Seq模型的这种普适性，以及将非序列问题转化为序列问题的能力，是深度学习领域一个非常重要的思想。它告诉我们，很多看似不同的问题，在抽象层面可能共享相同的结构，从而可以用统一的模型框架来解决。这极大地简化了模型设计，并加速了不同领域间的知识迁移。

**精华收获**

Seq2Seq模型的核心在于其处理“输出长度不确定”任务的能力，这使其成为语音、文本、甚至图像等多种模态下复杂序列转换问题的通用解决方案。通过巧妙的问题转化，Seq2Seq的适用范围远超想象，但同时也要认识到，针对特定任务的定制化模型往往能达到更优性能。

### Seq2Seq模型的内部结构：Encoder-Decoder架构 `[Seq2Seq架构：20:50-22:40]`

**核心观点**

所有Seq2Seq模型都遵循Encoder-Decoder架构，其中Encoder负责理解输入序列，Decoder负责生成输出序列，而Transformer正是这种架构的集大成者。

**深度阐述**

在介绍了Seq2Seq模型的广泛应用之后，教授开始深入探讨其内部工作原理。他指出，一个标准的Seq2Seq模型通常由两大部分组成：**Encoder（编码器）**和**Decoder（解码器）**。

- **Encoder**：负责处理输入的序列。它的任务是将整个输入序列的信息进行编码，将其转化为一种机器可以理解的、密集的表示形式（通常是一系列向量）。这个编码过程旨在捕捉输入序列的全部语义和上下文信息。
- **Decoder**：接收Encoder处理后的结果，并根据这些信息，逐步生成输出序列。Decoder的任务是根据Encoder提供的上下文信息，以及它自己已经生成的部分输出，来预测下一个输出元素，直到生成完整的输出序列。
这种分工明确的架构，使得Seq2Seq模型能够有效地处理输入和输出之间的复杂映射关系，尤其是在长度不匹配的情况下。

教授提到，Seq2Seq模型的起源可以追溯到2014年9月，当时就有一篇关于Seq2Seq模型应用于机器翻译的文章被发表。这表明Seq2Seq的概念并非新生事物，而是经过了多年的发展和演进。

而当我们今天谈论Seq2Seq模型时，最先浮现在脑海中的，往往就是**Transformer**。Transformer以其独特的Encoder-Decoder架构，以及内部复杂的“花花绿绿的block”（指其模块化的层级结构），成为了Seq2Seq模型家族中最具代表性和影响力的成员。接下来的部分，教授将详细剖析Transformer Encoder的内部结构，揭示这些“block”是如何协同工作，实现其强大功能的。

**延伸思考**

Encoder-Decoder架构是序列到序列任务的范式。Encoder将变长的输入序列压缩成一个固定长度（或固定数量的向量）的“思想向量”或“上下文表示”，Decoder再从这个表示中逐步解码出变长的输出序列。这种解耦设计是处理变长序列的关键。

**精华收获**

Seq2Seq模型普遍采用Encoder-Decoder架构，Encoder负责理解输入，Decoder负责生成输出。Transformer是这一架构的现代代表，其内部的模块化设计是其高性能的关键。

### Transformer Encoder的深度解析 `[Encoder内部结构：22:40-33:50]`

**核心观点**

Transformer的Encoder由多个相同的Block堆叠而成，每个Block的核心是Multi-Head Self-Attention和Feed Forward Network，并通过Residual Connection和Layer Normalization进行连接和稳定，同时结合Positional Encoding来捕捉序列的位置信息。

**深度阐述**

教授开始详细拆解Transformer Encoder的内部结构。

Encoder的核心功能与Self-Attention `[Encoder功能：22:40-23:40]`

Encoder的基本任务是：**输入一排向量，输出另一排向量**，且输入输出序列长度相同。许多模型都能做到这一点，如RNN、CNN，但Transformer的Encoder选择使用**Self-Attention**作为其核心机制。Self-Attention能够让模型在处理序列中的每个元素时，考虑到整个序列的所有其他元素，从而捕捉到全局的依赖关系。

Encoder Block的内部机制 `[Encoder Block：23:40-29:40]`

Transformer的Encoder并非一个单一的结构，而是由**多个相同的Block堆叠而成**。每个Block接收一排向量作为输入，输出另一排向量，然后将输出传递给下一个Block，直到最后一个Block输出最终的向量序列。教授强调，这里的“Block”并非传统意义上的“层”（Layer），因为每个Block内部包含了多个层的操作。

一个Transformer Encoder Block的简化流程如下：

1. **Self-Attention层**：接收输入向量序列，通过Self-Attention机制，让每个向量都融入了整个序列的上下文信息，输出一排新的向量。
1. **Fully Connected Feed Forward Network (FC Network)**：Self-Attention的输出再经过一个全连接的前馈网络，进一步处理这些上下文丰富的向量，输出最终的Block输出。
然而，原始Transformer论文中的设计更为复杂和精妙。它引入了两个关键的深度学习技术：**Residual Connection**和**Layer Normalization**。

- **Residual Connection (残差连接)**：
- **Layer Normalization (层归一化)**：
综合来看，一个完整的Transformer Encoder Block的内部流程是：

1. **Multi-Head Attention**：这是Self-Attention的增强版，同时进行多个Self-Attention操作，捕捉不同方面的依赖关系。
1. **Add & Norm**：将Multi-Head Attention的输出与原始输入进行Residual Connection（Add），然后进行Layer Normalization（Norm）。
1. **Feed Forward Network (FC Network)**：经过归一化后的结果输入到FC Network。
1. **Add & Norm**：FC Network的输出再次与FC Network的输入进行Residual Connection（Add），然后进行Layer Normalization（Norm）。
这个复杂的结构会重复N次，形成多层堆叠的Encoder。

Positional Encoding `[位置编码：29:40-30:20]`

教授提醒，在Self-Attention之前，输入的向量序列还需要加上**Positional Encoding（位置编码）**。由于Self-Attention本身是**位置无关**的（它平等地看待序列中的所有元素，不区分顺序），因此需要额外引入位置信息，让模型知道序列中每个元素的位置关系。

对Encoder设计的反思与优化 `[设计反思：33:50-37:00]`

教授强调，原始论文中的Transformer设计并非一成不变的“圣经”，而是可以被质疑和改进的。他通过两篇论文阐述了这一点：

- **Layer Normalization位置的探讨**：
- **Batch Normalization与Layer Normalization的比较**：
这些研究表明，即使是像Transformer这样具有里程碑意义的模型，其内部设计也仍然有优化和改进的空间，鼓励研究者不断思考和探索。

**个人感受**

教授在讲解Encoder的复杂结构时，清晰地拆解了每个组件的作用，并用“花花绿绿的block”来形容，既形象又生动。他对Residual Connection和Layer Normalization的解释，尤其是与Batch Normalization的对比，深入浅出，帮助听众理解了这些关键技术背后的原理。最后，他对Transformer设计并非“最优”的讨论，展现了严谨的科学态度，鼓励大家批判性思考，而不是盲目接受。

**延伸思考**

Encoder Block的这种模块化设计，结合了Self-Attention的全局感知能力、Residual Connection的深度训练稳定性、Layer Normalization的训练加速，以及Positional Encoding的位置感知，共同构成了Transformer强大的特征提取能力。这种设计思想对后续的深度学习模型产生了深远影响。

**精华收获**

Transformer Encoder通过堆叠包含Multi-Head Self-Attention、Feed Forward Network、Residual Connection和Layer Normalization的Block，有效地提取序列特征。Positional Encoding弥补了Self-Attention的位置无关性。同时，模型设计并非一成不变，对现有架构的批判性思考和优化是推动技术进步的关键。

<!-- TLDR: Transformer作为强大的Seq2Seq模型，以Encoder-Decoder架构和自注意力机制，解决了语音、文本等多种序列任务的输出长度不确定性问题，其设计仍在不断优化。 -->

<!-- TAGS: Transformer, Seq2Seq, 机器学习, 自然语言处理, 语音识别, 深度学习, Encoder-Decoder, Self-Attention, Layer Normalization -->

<!-- RATING: 5 -->

---
