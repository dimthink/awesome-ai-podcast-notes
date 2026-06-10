---
title: "【機器學習2021】Transformer (下)"
channel: "李弘毅"
published: "2021-04-09"
source_url: "https://www.youtube.com/watch?v=N6aRv06iv2g"
video_id: "N6aRv06iv2g"
rating: 5
language: "中文"
word_count: 15912
duration: "1:00:34"
---

# 【機器學習2021】Transformer (下)

- **Channel:** 李弘毅
- **Published:** 2021-04-09
- **Source:** https://www.youtube.com/watch?v=N6aRv06iv2g
- **TL;DR:** Transformer Decoder通过自回归、Masked Attention和Cross Attention实现高效序列生成，并辅以多种训练技巧应对挑战。
- **Rating:** 5

## 材料信息

- **标题**：【機器學習2021】Transformer (下)
- **作者/来源**：李弘毅
- **类型**：YouTube 视频字幕
- **关键元数据**：视频时长约 1 小时 03 分钟
## 开篇引入

在深度学习的浩瀚星空中，Transformer模型无疑是一颗璀璨的明星，它以其独特的自注意力机制（Self-Attention）革新了序列建模领域。如果说Encoder是理解和编码输入序列的“大脑”，那么Decoder则是将这些深层理解转化为具体输出的“语言生成器”。本篇深度文章将带你深入探索Transformer Decoder的奥秘，从其核心的逐字生成机制，到非自回归（Non-Autoregressive）模型的速度优势，再到连接Encoder与Decoder的Cross Attention，以及一系列提升模型性能的训练技巧。我们将不仅还原李弘毅老师在视频中深入浅出的讲解，更会通过细致的阐述、生动的比喻和深度的思考，让你对Transformer Decoder的运作原理、挑战与前沿进展，获得比直接观看视频更全面、更深刻的理解。准备好了吗？让我们一同揭开Transformer Decoder的神秘面纱。

## 详细内容

### Autoregressive Decoder：逐字生成的智慧与挑战 `[00:00-00:15:00]`

**核心观点**

Autoregressive (AR) Decoder 是一种逐字生成输出序列的模型，它将前一个时间步的自身输出作为下一个时间步的输入，逐步构建完整的序列，这种机制虽然直观，但也带来了“错误传播”的挑战。

**深度阐述**

在Transformer的下半部分，我们首先聚焦于Decoder，特别是其最常见的“Autoregressive”（自回归）模式。为了更好地理解其运作，李弘毅老师以语音识别为例进行了详细阐述。

想象一下语音识别的流程：你对着机器说“机器学习”，这段声音信号首先被送入Encoder。Encoder的任务是将这段声音信号转化为一串向量序列，每个向量都编码了声音信号在不同时间步的特征。这个过程在上周的课程中已经详细讲解，其内部结构复杂，但核心功能是明确的：将一个向量序列转换为另一个向量序列。

接下来，就轮到Decoder登场了。Decoder的核心任务是根据Encoder的输出，生成对应的文字序列。那么，Decoder是如何“吐出”这些文字的呢？

1. **初始输入与BEGIN Token**：Decoder的生成过程并非凭空开始。它首先需要一个特殊的“开始”符号作为输入，这个符号通常被称为“Begin Of Sentence”（BOS），在助教的幻灯片中缩写为“BOS”。这个BOS是一个特殊的Token，它被添加到模型的词汇表（Lexicon）中，并像其他文字一样，用一个One-Hot Vector来表示。One-Hot Vector的特点是，在一个长向量中，只有一个维度是1，其他维度都是0，代表了该Token的唯一身份。
1. **首次输出与概率分布**：当Decoder接收到这个BEGIN Token作为输入后，它会处理这个输入（具体如何处理，我们稍后会讲到Encoder的输出如何被Decoder读取）。处理后，Decoder会吐出一个新的向量。这个向量的长度非常关键，它与模型预设的“Vocabulary Size”（词汇表大小）相同。词汇表包含了所有Decoder可能输出的文字。例如，如果我们在做中文语音识别，词汇表可能包含3000-5000个常用汉字。这个向量在经过Softmax函数处理后，会变成一个概率分布，向量中所有值的总和为1。每个值代表了词汇表中对应汉字被选为下一个输出的概率。
1. **贪婪解码（Greedy Decoding）**：在得到这个概率分布后，Decoder会选择概率最高的那个汉字作为它的第一个输出。例如，如果“机”字的分数最高，那么“机”就是Decoder的第一个输出。
1. **逐字生成与自回归特性**：生成第一个字“机”之后，这个“机”字并不会被丢弃，而是被重新编码成一个One-Hot Vector，并与之前的BEGIN Token一起，作为Decoder的*新的输入*。也就是说，现在Decoder的输入变成了“BEGIN”和“机”。基于这两个输入，Decoder再次生成一个概率分布，并选出分数最高的字，比如“器”。这个“器”字又会被加入到输入序列中，形成“BEGIN”、“机”、“器”作为Decoder的输入，以此类推，逐步生成“学”、“习”。
这个过程的关键在于，**Decoder会将自己前一个时间点产生的输出，作为下一个时间点生成时的输入**。这就是“Autoregressive”（自回归）的含义。它像一个接龙游戏，每一步都依赖于前一步的结果。

**个人感受**

李弘毅老师在讲解One-Hot Vector和Vocabulary Size时，特别提到了中文方块字的特点，以及不同语言（如英文的字母、词汇或Subword）在选择输出单位时的考量，这体现了在实际应用中对语言特性的细致思考。他用“助教的投影片”来指代具体的实现细节，让听众感受到课程与实践的紧密结合。

**错误传播（Error Propagation）的隐忧**

然而，这种自回归的机制也带来了一个潜在的问题：**错误传播（Error Propagation）**。如果Decoder在某个时间步不小心犯了错误，比如把“机器”的“器”识别成了“天气”的“气”，那么这个错误的“气”就会被当作后续生成的输入。Decoder将基于这个错误的输入继续生成，这很可能导致后续的生成也出现偏差，甚至整个句子都变得面目全非。李弘毅老师形象地称之为“一步错，步步错”。虽然这个问题在讲解初期被暂时搁置，但它揭示了自回归模型在鲁棒性方面的一个固有挑战。

**延伸思考**

Autoregressive Decoder的逐字生成方式，虽然在逻辑上与人类语言生成过程相似，但其串行特性也限制了生成速度。同时，错误传播问题也促使研究者探索更鲁棒的训练和推理策略，或者转向其他生成范式。

### Decoder的内部构造：Masked Self-Attention的奥秘 `[00:15:00-00:22:00]`

**核心观点**

Transformer Decoder的内部结构与Encoder高度相似，但其核心区别在于引入了“Masked Self-Attention”机制，确保在生成当前Token时，模型只能关注到其左侧（已生成）的信息，从而维持生成过程的因果性。

**深度阐述**

为了更深入地理解Decoder，我们需要剖析其内部结构。李弘毅老师首先将Encoder和Decoder的结构并置进行比较。乍看之下，Decoder的结构似乎比Encoder更为复杂，但如果我们将Decoder中间的一个特定区域暂时“遮盖”起来，我们会惊奇地发现，两者之间存在着高度的相似性。

**结构对比：Encoder与Decoder的相似之处**

Encoder的典型结构包含多个堆叠的层，每一层都由Multi-Head Attention、Add & Norm（残差连接与层归一化）以及Feed Forward Network（前馈神经网络）组成，并重复N次。令人意外的是，当Decoder的中间部分被遮盖后，它的结构也呈现出类似的模式：Multi-Head Attention、Add & Norm、Feed Forward、Add & Norm，同样重复N次。这表明Encoder和Decoder在处理序列信息的基本模块上是共享的。

**Masked Self-Attention：Decoder的独特之处**

然而，被遮盖的区域以及Decoder的Multi-Head Attention层上方额外标注的“Masked”字样，正是Decoder与Encoder的关键区别所在。这个“Masked”机制是Decoder能够实现逐字生成并保持因果关系的核心。

为了理解Masked Self-Attention，我们首先回顾普通的Self-Attention：

在Encoder的Self-Attention中，当模型要生成输出序列中的某个位置`b`*`i`**时，它会考虑输入序列中所有位置**`a`*`1`到`a`*`N`**的信息。也就是说，每个输出**`b`*`i`的计算都依赖于完整的输入序列。

而**Masked Self-Attention**则不然。它的核心限制是：**在生成当前位置的输出时，模型不能“看到”或“利用”当前位置及其右侧（未来）的信息**。

具体来说：

- 当生成`b`*`1`**时，只能考虑**`a`*`1`的信息。
- 当生成`b`*`2`**时，只能考虑**`a`*`1`和`a`*`2`**的信息。*
- 当生成`b`*`3`**时，只能考虑**`a`*`1`、`a`*`2`**和**`a`*`3`的信息。
- 以此类推，生成`b`*`i`**时，只能考虑**`a`*`1`到`a`*`i`**的信息。*
**为什么需要Masked？**

这个限制并非随意添加，而是源于Decoder的**逐字生成**特性。正如我们前面所讨论的，Decoder的输出是一个一个地产生的。当模型正在生成`b`*`2`**时，**`b`*`3`、`b`*`4`**等右侧的Token实际上还未被生成，它们根本不存在。因此，模型在计算**`b`*`2`时，自然无法将`a`*`3`**、**`a`*`4`等信息纳入考量。Masked Self-Attention正是通过在计算注意力分数时，将右侧（未来）位置的权重设置为负无穷（或一个非常小的数），使其在Softmax后变为0，从而强制模型只关注左侧信息。

**视觉/结构信息描述**

在Transformer的原始论文图中，Decoder的结构通常包含两个Multi-Head Attention层。第一个是Masked Multi-Head Self-Attention，它处理Decoder自身的输入序列（即已生成的Token）。第二个是Multi-Head Cross-Attention，它将Decoder的查询与Encoder的输出进行交互。这个“Masked”的标记就出现在Decoder的第一个Multi-Head Attention模块上，明确指出其与Encoder Self-Attention的不同。

**延伸思考**

Masked Self-Attention是Transformer Decoder能够实现因果生成（Causal Generation）的关键。它确保了模型在生成每个Token时，都严格遵循了从左到右的时间顺序，避免了“偷看未来”的问题，这对于语言生成、机器翻译等任务至关重要。

### 序列长度的终结：END Token与推文接龙 `[00:22:00-00:27:00]`

**核心观点**

在自回归生成过程中，Decoder需要一个明确的信号来判断何时停止输出，这个信号通过引入特殊的“END”符号实现，它让模型能够自主决定生成序列的长度。

**深度阐述**

在前面我们详细探讨了Decoder如何逐字生成序列，但一个核心问题仍然悬而未决：**Decoder如何知道它应该在何时停止生成？**输出序列的长度并非总是与输入序列的长度简单对应。例如，输入四个向量，输出不一定就是四个向量。在实际应用中，输入和输出的长度关系往往非常复杂，我们期望机器能够自主学习并决定输出序列的合适长度。

如果缺乏一个停止机制，Decoder在生成完“习”之后，可能会继续将“习”作为输入，然后生成“惯”，接着又生成其他字，如此循环往复，永不停止。李弘毅老师生动地将其比喻为台湾PTT论坛上古老的“推文接龙”民俗：一个人推一个字，另一个人接一个字，可以持续数月，直到有人推一个特殊的“断”字，整个接龙才宣告结束。

**引入END Token**

为了解决这个问题，Transformer Decoder引入了一个与BEGIN Token类似的特殊符号——**END Token**，代表“结束”（End Of Sentence）。这个END Token也被添加到模型的词汇表中，与所有中文方块字和BEGIN Token并列。在助教的程序中，BEGIN和END有时会用同一个符号表示，因为BEGIN只出现在输入端，END只出现在输出端，两者不会冲突。

**训练目标与停止机制**

在训练过程中，模型不仅要学习生成正确的文字序列，还要学习在适当的时机输出END Token。例如，在生成完“机器学习”的“习”之后，当“BEGIN”、“机”、“器”、“学”、“习”作为Decoder的输入时，我们期望Decoder能够输出一个概率分布，其中END Token的概率是最高的。一旦Decoder输出了END Token，整个序列的生成过程就宣告结束。

**个人感受**

李弘毅老师用PTT推文接龙的例子来解释END Token的必要性，这个比喻非常接地气且形象，让抽象的技术概念变得生动有趣。他提到“超人正大中天外飞仙草”这种无意义的接龙，幽默地展现了缺乏停止机制的后果。

**延伸思考**

END Token的引入是序列生成模型设计中的一个基本且关键的组成部分。它赋予了模型在没有外部干预的情况下，自主控制输出序列长度的能力，这对于各种生成任务（如机器翻译、文本摘要、对话系统）都至关重要。

### 非自回归解码器（NAT）：速度与控制的诱惑 `[00:27:00-00:36:00]`

**核心观点**

非自回归（Non-Autoregressive, NAT）模型旨在通过一次性生成整个输出序列来克服AR模型的串行生成限制，从而实现显著的并行化和更快的推理速度，并提供对输出长度的显式控制，尽管其性能通常仍需大量技巧才能与AR模型匹敌。

**深度阐述**

在理解了Autoregressive (AR) Decoder的逐字生成机制后，李弘毅老师简要介绍了另一种截然不同的解码范式：**Non-Autoregressive (NAT) Decoder**。NAT模型的核心理念是打破AR模型的串行依赖，实现**一次性生成整个输出序列**。

**NAT的工作机制**

与AR模型逐字生成不同，NAT模型在生成一个中文句子时，不再是先生成`w`*`1`**，再将**`w`*`1`作为输入生成`w`*`2`**。相反，它会一次性接收一整排的BEGIN Token作为输入，然后一次性地输出一整排的Token，从而形成完整的句子。例如，如果输入4个BEGIN Token，它就一次性生成4个中文字，构成一个句子，整个生成过程在一个步骤内完成。*

**如何确定输出长度？**

NAT模型面临一个显而易见的问题：既然是一次性生成，那么它怎么知道应该输出多长的序列呢？李弘毅老师提出了两种常见的解决方案：

1. **长度分类器（Length Classifier）**：训练一个独立的分类器，该分类器以Encoder的输出作为输入，然后预测Decoder应该输出的长度（例如，输出数字4）。NAT Decoder随后就接收相应数量的BEGIN Token（例如4个），并生成对应长度的序列。
1. **固定最大长度**：设定一个句子的最大长度上限（例如300个字）。NAT Decoder总是接收300个BEGIN Token，并生成300个字。然后，模型会在某个位置输出END Token，所有在END Token右侧的输出都会被视为无效或截断。
**NAT的优势**

NAT模型之所以成为一个热门研究主题，主要得益于其两大优势：

1. **并行化（Parallelization）**：这是NAT最显著的优势。AR模型需要进行N次解码（N为句子长度），而NAT模型无论句子多长，都只需一个步骤即可完成生成。这意味着在速度上，NAT Decoder通常比AR Decoder快得多。李弘毅老师指出，这种并行化的想法只有在Transformer引入Self-Attention之后才变得可行，因为传统的RNN/LSTM即使输入一排BEGIN，也无法同时生成所有输出。
1. **输出长度的显式控制**：在某些任务中，NAT模型能够提供对输出长度更精细的控制。以语音合成（Text-to-Speech, TTS）为例，著名的Tacotron模型是AR的，而FastSpeech模型则是NAT的。如果使用NAT模型，并且通过分类器显式地建模了输出长度，那么就可以通过调整分类器的输出（例如，除以2让语速变快，乘以2让语速变慢），来直接控制合成语音的语速。这种显式的控制能力在AR模型中很难实现。
**NAT的挑战与劣势**

尽管NAT模型拥有诱人的优势，但其最大的挑战在于**性能（Performance）**。李弘毅老师明确指出，NAT Decoder的性能往往不如AR Decoder。要让NAT模型达到与AR模型相当的性能，通常需要引入大量的“Trick”（技巧）。他甚至提到，NAT是一个“大坑”，助教也曾花费一个半小时来大致描述，可见其复杂性。其中一个未深入讨论的问题是**Multi-Modality问题**，这指的是NAT模型在面对多个可能的正确输出时，难以选择其中一个最优解。

**个人感受**

李弘毅老师在介绍NAT时，强调了其作为“热门研究主题”的地位，并直言其“大坑”的本质，这既展现了研究前沿的魅力，也提醒了其中的挑战。他通过Tacotron和FastSpeech的对比，具体说明了NAT在语音合成领域的应用价值和控制能力。

**延伸思考**

NAT模型代表了序列生成领域的一个重要研究方向，旨在平衡生成质量与效率。尽管目前性能仍是其主要瓶颈，但其并行化和可控性使其在对实时性要求高或需要灵活控制输出的任务中具有巨大潜力。未来的研究将继续探索如何弥合NAT与AR模型之间的性能差距。

### 跨注意力（Cross Attention）：连接编码器与解码器的桥梁 `[00:36:00-00:46:00]`

**核心观点**

Cross Attention是Transformer Decoder中连接Encoder输出的关键机制，它允许Decoder在生成每个Token时，从Encoder提供的完整上下文信息中选择性地提取最相关的特征，从而实现跨序列的信息融合。

**深度阐述**

在Transformer的架构图中，Encoder和Decoder之间存在一个被我们之前刻意“遮盖”起来的区域，这个区域正是连接两者的桥梁——**Cross Attention**。它在Decoder的内部结构中扮演着至关重要的角色，使得Decoder能够“读取”Encoder的输出。

**Cross Attention的工作原理**

Cross Attention的运作机制与Self-Attention类似，但其Query（Q）、Key（K）和Value（V）的来源不同：

1. **Query (Q) 来自Decoder**：当Decoder接收到其输入（例如BEGIN Token，或已生成的“机”字）并经过Masked Self-Attention处理后，会得到一个向量。这个向量经过一个线性变换（乘以一个矩阵），生成Query (q)。这个q代表了Decoder当前正在关注的信息。
1. **Key (K) 和 Value (V) 来自Encoder**：Encoder的最终输出是一排向量序列（例如`a`*`1, a`*`2, a`*`3`**）。这些向量经过各自的线性变换，分别生成Key (k) 和 Value (v) 序列（例如**`k`*`1, k`*`2, k`*`3`和`v`*`1, v`*`2, v`*`3`**）。Key代表了Encoder输出中每个位置的“索引”或“内容描述”，Value则包含了实际的信息。*
1. **计算注意力分数**：Decoder的Query (q) 会与Encoder的所有Key (k*1, k*2, k*3) 计算注意力分数（例如通过点积），得到**`α`*`1, α`*`2, α`*`3`。这些分数经过Softmax归一化后，表示Decoder在生成当前Token时，对Encoder输出中每个位置的关注程度。
1. **加权求和**：将这些注意力分数`α`与Encoder的Value (v*1, v*2, v*3) 进行加权求和，得到一个最终的上下文向量V。这个V向量包含了从Encoder输出中提取出的、与Decoder当前生成任务最相关的信息。*
1. **后续处理**：这个上下文向量V随后会被送入Decoder的Feed Forward Network（前馈神经网络）进行进一步处理，最终影响Decoder的输出。
简而言之，**Decoder通过生成一个Query，去Encoder的Key-Value对中抽取它所需要的信息**。这个过程在Decoder生成每一个Token时都会发生，确保Decoder始终能够访问并利用Encoder对输入序列的完整理解。

**历史回顾与视觉化解释**

李弘毅老师特别指出，Cross Attention的概念并非Transformer独有。他引用了一篇发表于ICASSP 2016的早期论文《Listen, Attend And Spell》（LAS），该论文首次成功地将Sequence-to-Sequence模型应用于语音识别。尽管LAS模型当时使用的是LSTM而非Transformer，但它已经包含了Cross Attention的机制。这表明**先有Cross Attention，后有Self-Attention**。

为了更直观地展示Cross Attention的效果，李弘毅老师描述了一个Attention分数的可视化图。在一个语音识别任务中，输入是声音信号（表示为一串向量），输出是英文单词（例如“How much wood would a woodchuck chuck”）。当Decoder生成“H”时，Attention分数会集中在声音信号中对应“H”发音的部分；生成“o”时，Attention会向右移动到“o”的发音部分。这个Attention权重图呈现出从左上到右下移动的对角线模式，直观地展示了Decoder如何随着生成进程，逐步关注输入声音信号的不同时间段。

**多层连接的探讨**

在原始的Transformer论文中，Decoder的每一层都只连接Encoder的最后一层输出。然而，李弘毅老师也提到，这并非唯一的连接方式。研究者们已经探索了各种不同的Cross Attention连接方式，例如让Decoder的不同层连接Encoder的不同层，这本身就是一个活跃的研究问题。

**个人感受**

李弘毅老师分享了他在ICASSP 2016现场亲耳聆听LAS论文报告的经历，以及当时对Sequence-to-Sequence模型在语音识别上潜力的惊叹，这为技术讲解增添了生动的人文色彩和历史厚重感。他对当时论文标题“三个动词”的幽默观察，也让人会心一笑。

**延伸思考**

Cross Attention是Transformer模型实现跨模态（如语音到文本）或跨序列（如机器翻译）信息传递的关键。它使得Decoder能够动态地聚焦于Encoder输出中最相关的部分，而不是简单地接收一个固定长度的上下文向量，从而极大地提升了模型的理解和生成能力。

### 解码器训练：Teacher Forcing与损失函数 `[00:46:00-00:52:00]`

**核心观点**

Transformer Decoder的训练采用“Teacher Forcing”策略，即在每个时间步都以正确的上一个Token作为输入，并通过最小化预测输出与真实标签之间的Cross Entropy损失来优化模型参数。然而，这种训练方式与测试时的实际情况存在“Exposure Bias”的不一致性。

**深度阐述**

在详细了解了Encoder、Decoder的运作机制以及它们之间的互动后，我们终于进入了Transformer模型训练的核心环节。在此之前，我们所讨论的都是模型在“测试”（Inference）阶段如何运作，即模型已经训练好并投入使用。现在，我们将探讨如何让模型学会这些复杂的生成能力。

**训练数据与目标**

以语音识别为例，训练Transformer Decoder需要大量的“声音-文字”对数据。例如，一段声音信号对应着“机器学习”这四个字。训练的目标就是让模型学会：当听到这段声音信号时，它的输出应该是“机器学习”。

**Cross Entropy损失函数**

训练过程可以被视为一系列分类任务的组合：

1. **第一个输出**：当Decoder接收到BEGIN Token作为输入时，它应该输出“机”。“机”字被表示为一个One-Hot Vector（正确答案）。Decoder的输出是一个概率分布。我们希望这个概率分布与“机”字的One-Hot Vector越接近越好。衡量这种接近程度的指标就是**Cross Entropy**。我们希望Cross Entropy的值越小越好。
1. **后续输出**：这个过程会重复进行。当Decoder接收到“BEGIN”和“机”作为输入时，它应该输出“器”。同样，计算“器”的One-Hot Vector与Decoder输出概率分布之间的Cross Entropy。
1. **总损失**：在训练时，对于一个完整的序列（例如“机器学习”），我们会计算每个时间步的Cross Entropy，并将它们加起来，形成一个总的损失函数。我们的目标是最小化这个总的Cross Entropy。
1. **END Token的训练**：不要忘记END Token。在生成完“机器学习”的“习”之后，模型还需要学习在下一个时间步输出END Token。因此，训练数据中也包含了在序列末尾输出END Token的正确标签。
**Teacher Forcing机制**

在训练Decoder时，有一个非常关键的策略叫做**Teacher Forcing**。它的核心思想是：**在训练过程中，Decoder的输入总是正确的上一个Token，而不是模型自己预测的Token。**

例如：

- 为了让Decoder输出“器”，我们会给它输入“BEGIN”和**正确的“机”**。
- 为了让Decoder输出“学”，我们会给它输入“BEGIN”、“机”和**正确的“器”**。
- 以此类推，直到输出END Token。
这种做法就像老师在教学生时，总是提供正确的答案作为参考，确保学生每一步都能站在正确的起点上学习。

**Exposure Bias：训练与测试的不一致**

然而，Teacher Forcing虽然有助于模型快速收敛和学习，但也引入了一个显著的问题，被称为**Exposure Bias**。

- **训练时**：Decoder总是看到**正确的**输入序列。它从未见过自己犯错后的输出。
- **测试时**：Decoder看到的是**自己的输出**。如果它在某个时间步犯了错误，这个错误就会被当作后续的输入，导致“一步错，步步错”的错误传播。
这种训练与测试之间的不一致性，意味着模型在训练时所处的环境与实际应用时所处的环境是不同的。如果Decoder在训练时从未见过错误，那么当它在测试时遇到自己的错误输出时，可能会感到“惊奇”，从而导致后续生成结果的严重偏差。

**个人感受**

李弘毅老师对“Teacher Forcing”这个名字的疑惑，以及将其比作分类问题的直观解释，都体现了他深入浅出的教学风格。他明确指出了Exposure Bias这个核心问题，为后续的训练技巧铺垫。

**延伸思考**

Exposure Bias是Sequence-to-Sequence模型训练中的一个长期挑战。虽然Teacher Forcing能够加速训练，但解决训练与测试不一致的问题对于提升模型在真实世界中的鲁棒性和泛化能力至关重要。

### 训练技巧：提升Seq2Seq模型性能的策略 `[00:52:00-01:03:00]`

**核心观点**

为了克服Seq2Seq模型在生成任务中的各种挑战，研究者们开发了一系列高级训练技巧，包括允许模型复制输入的Copy Mechanism、强制注意力对齐的Guided Attention、平衡探索与利用的Beam Search，以及解决Exposure Bias的Scheduled Sampling。

**深度阐述**

在Transformer Decoder的训练和应用中，除了核心机制外，还有许多实用的技巧可以显著提升模型的性能和鲁棒性。李弘毅老师详细介绍了以下几个关键策略：

1. Copy Mechanism (复制机制) `[00:52:00-00:56:00]`
**目的与应用场景**

在许多生成任务中，Decoder并非总是需要“创造”全新的词汇。有时，直接从输入中“复制”一些词汇会更合理、更高效。

- **聊天机器人**：当用户说“你好，我是库洛洛”时，机器回应“库洛洛你好”。“库洛洛”是一个专有名词，模型很难凭空生成，直接复制输入中的名字会更自然。
- **文本摘要**：在生成文章摘要时，很多关键信息和词汇可以直接从原文中提取和复制，而非重新措辞。
**实现方式**

这种复制能力可以通过Pointer Network或Copy Network等机制实现。它们允许Decoder在生成Token时，除了从词汇表中选择外，还可以选择从输入序列中“指向”并复制一个Token。这极大地简化了模型处理罕见词汇和关键信息复制的任务。

**个人感受**

李弘毅老师用“库洛洛”这个动漫角色来举例，生动地说明了复制机制在对话系统中的必要性。他提到“小杰不能用念能力了”的例子，也展现了模型在复述和理解用户意图时的复制需求。

2. Guided Attention (引导注意力) `[00:56:00-01:00:00]`

**问题背景**

Seq2Seq模型有时会犯“低级错误”，例如在语音合成中“漏字”（如“发财”只念“财”），或者在语音识别中“听漏”部分内容。这通常是由于Attention机制没有正确地对齐输入和输出。

**目的与应用场景**

Guided Attention旨在**强制Attention机制遵循预期的模式**，确保模型能够完整地处理输入信息。它特别适用于对输入输出对齐要求严格的任务：

- **语音识别 (ASR)**：确保模型听到并识别出输入语音的每一个部分。
- **语音合成 (TTS)**：确保模型完整地念出输入文本的每一个字。
**实现方式**

对于语音相关任务，我们通常期望Attention是从左到右、单调递增的。Guided Attention通过在训练时引入额外的损失函数或正则项，来“引导”Attention权重，使其偏向于这种单调的、由左到右的模式。例如，如果Attention分数出现跳跃或混乱，就会产生惩罚。具体的关键词包括“Monotonic Attention”或“Location-Aware Attention”。

**个人感受**

李弘毅老师分享了语音合成中“发财”的有趣案例，模型在重复四次时能有抑扬顿挫，但单次却漏掉“发”字，这揭示了模型在处理极端情况时的脆弱性。他强调了Guided Attention在语音任务中的重要性，因为“你很难接受说，你讲一句话，今天辨识出来，居然有一段机器没听到”。

3. Beam Search (集束搜索) `[01:00:00-01:03:00]`

**Greedy Decoding的局限**

我们之前讨论的Decoder每次都选择概率最高的Token作为输出，这被称为**Greedy Decoding**（贪婪解码）。然而，局部最优并不意味着全局最优。李弘毅老师用“天龙八部真龙棋局”和“签博”的例子形象地说明：有时第一步选择一个看似较差的选项，却能导向最终更好的结果。

**Beam Search的原理**

Beam Search是一种启发式搜索算法，它不像Greedy Decoding那样只保留一个最佳路径，而是**在每个时间步保留K个（Beam Size）最有可能的路径**。在生成下一个Token时，它会考虑这K条路径的所有可能扩展，然后从所有扩展中选出K个概率最高的路径继续前进。这样，Beam Search能在有限的计算资源下，找到一个近似全局最优的解。

**Beam Search的适用性**

Beam Search并非万能，其效果取决于任务特性：

- **有帮助的任务**：答案明确、唯一性强的任务，如语音识别（一句话的识别结果通常是唯一的）。
- **无帮助的任务**：需要创造性、答案多样性的任务，如Sentence Completion（补全句子）或文本生成。在这些任务中，Beam Search可能导致模型陷入“鬼打墙”，不断重复生成相同或相似的短语，因为模型倾向于选择高频、安全的词汇。
- **TTS中的随机性**：李弘毅老师分享了一个非常反直觉的例子：在语音合成（TTS）中，测试时**加入一些噪声（随机性）**，反而能合成出更自然、更像人声的语音。这与传统的机器学习理念（测试时不加噪声）相悖，但却揭示了在某些生成任务中，适度的随机性能够带来更好的结果，呼应了“真正的美也许就在不完美之中”的哲学思考。
**个人感受**

李弘毅老师用“天龙八部真龙棋局”和“签博”的例子来解释Greedy Decoding的局限性，非常生动且富有哲理。他分享了Google工程师关于TTS加噪声的建议，以及Beam Search在创造性任务中可能导致“鬼打墙”的现象，这些都揭示了机器学习实践中充满的经验主义和反直觉的发现。

4. BLEU Score与Cross Entropy的矛盾 `[01:03:00-01:06:00]`

**问题**

训练时我们优化的是Cross Entropy（逐Token的概率损失），但评估时（如机器翻译作业）我们使用的是BLEU Score（衡量整个句子与参考句子的相似度）。这两个指标并不完全一致，最小化Cross Entropy不一定能最大化BLEU Score。

**解决方案**

- **Validation Set评估**：在验证集上，应使用BLEU Score来选择最佳模型，而不是Cross Entropy。
- **强化学习（RL）**：对于像BLEU Score这样不可微分的损失函数，可以将其作为强化学习的奖励（Reward），将Decoder视为Agent，通过RL方法进行训练。但这通常是一个更复杂、更难实现的方法。
5. Exposure Bias的解决：Scheduled Sampling `[01:06:00-01:09:00]`

**问题回顾**

Exposure Bias指的是训练时Decoder总是看到正确的输入（Teacher Forcing），而测试时却要面对自己可能错误的输出，导致训练与测试环境不一致。

**Scheduled Sampling**

为了解决Exposure Bias，一种直观的方法是：**在训练时，偶尔也给Decoder看一些错误的输入**。Scheduled Sampling就是这样一种技术，它在训练过程中，以一定的概率（通常随训练进程逐渐增加）用模型自己生成的Token替换掉正确的Teacher Forcing Token作为Decoder的输入。这使得模型在训练时就能适应处理错误输入的情况，从而提高其在测试时的鲁棒性。

**Transformer上的挑战**

然而，传统的Scheduled Sampling方法可能会损害Transformer的并行化能力。因此，针对Transformer架构，研究者们开发了新的Scheduled Sampling变体。

**个人感受**

李弘毅老师再次强调了Exposure Bias的重要性，并指出Scheduled Sampling的直观性。他提及该技术在LSTM时代就已存在，但在Transformer上需要新的实现方式，展现了技术演进的复杂性。

**延伸思考**

这些训练技巧共同构成了提升Seq2Seq模型性能的工具箱。它们不仅解决了模型在生成过程中的具体问题，也反映了深度学习模型在理论与实践之间不断磨合、进化的过程。理解这些技巧，对于构建高效、鲁棒的生成模型至关重要。

### 精华收获

Transformer Decoder是序列生成任务的核心，其Autoregressive模式通过逐字生成，将前一个输出作为下一个输入，但面临错误传播的风险。Masked Self-Attention确保了生成过程的因果性，而END Token则赋予模型自主决定输出长度的能力。非自回归（NAT）模型通过并行化追求速度和长度控制，但通常牺牲了部分性能。Cross Attention是连接Encoder与Decoder的关键，使Decoder能从Encoder的完整语境中提取信息。训练时，Teacher Forcing加速学习但引入Exposure Bias，需通过Scheduled Sampling等技巧缓解。此外，Copy Mechanism、Guided Attention和Beam Search等高级策略，能针对特定任务提升模型在复制、对齐和搜索最优路径方面的能力。理解这些机制与技巧，是掌握Transformer生成能力的关键。

<!-- TLDR: Transformer Decoder通过自回归、Masked Attention和Cross Attention实现高效序列生成，并辅以多种训练技巧应对挑战。 -->

<!-- TAGS: Transformer, Decoder, Autoregressive, Non-Autoregressive, Cross Attention, Teacher Forcing, Scheduled Sampling, Beam Search, 机器学习 -->

<!-- RATING: 5 -->

---
