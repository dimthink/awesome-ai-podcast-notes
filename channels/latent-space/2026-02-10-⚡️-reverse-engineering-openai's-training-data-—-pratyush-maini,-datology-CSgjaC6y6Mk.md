---
title: "⚡️ Reverse Engineering OpenAI's Training Data — Pratyush Maini, Datology"
channel: "Latent Space"
published: "2026-02-10"
source_url: "https://www.youtube.com/watch?v=CSgjaC6y6Mk"
video_id: "CSgjaC6y6Mk"
duration: "27:02"
---

# ⚡️ Reverse Engineering OpenAI's Training Data — Pratyush Maini, Datology

- **Channel:** Latent Space
- **Published:** 2026-02-10
- **Source:** https://www.youtube.com/watch?v=CSgjaC6y6Mk

## 版本

- [原始文稿](2026-02-10-⚡️-reverse-engineering-openai's-training-data-—-pratyush-maini,-datology-CSgjaC6y6Mk.transcript.md)

# 内容深度重构与阐述

## 材料信息

- **标题**：⚡️ Reverse Engineering OpenAI's Training Data — Pratyush Maini, Datology
- **作者/来源**：Latent Space (采访 Pratyush Maini, Datology 联合创始人)
- **类型**：YouTube 视频字幕
- **关键元数据**：视频时长约 25 分钟，本次重构内容涵盖视频前约 20 分钟。
## 开篇引入

在人工智能飞速发展的今天，模型的能力边界不断被拓宽，但其内部运作机制，尤其是训练数据的构成，却常常笼罩在神秘的面纱之下。我们常常惊叹于大型语言模型（LLM）的强大推理和生成能力，却很少有机会深入探究这些能力是如何从海量的训练数据中“习得”的。本次深度访谈，Latent Space 邀请到 Datology 的联合创始人 Pratyush Maini，一位深耕数据领域多年的博士研究员，他将带领我们进行一场精彩的“逆向工程”，揭示 OpenAI 等前沿模型训练数据中那些不为人知的秘密，特别是关于模型“自我修正”和“推理能力”的培养。这不仅是一次技术揭秘，更是一次对当前 AI 训练范式和未来发展方向的深刻反思。通过 Pratyush 的分享，我们将获得比直接观看视频更系统、更深入的理解，感受数据在 AI 时代的核心价值和无限魅力。

## 详细内容

### 1. Datology 的数据信仰与“数据很怪”频道 `[00:00-02:30]`

**核心观点**

Datology 团队坚信数据是 AI 系统的核心，并致力于推动数据在 AI 研发中的价值。他们甚至设立了一个名为“数据很怪”（Data is Weird）的内部 Slack 频道，专门分享数据中那些令人意想不到的奇特现象，这体现了他们对数据深入探索的激情和好奇心。

**深度阐述**

访谈伊始，主持人便开宗明义地指出，Datology 是一个“数据狂人”团队，他们对数据有着异乎寻常的热情。Pratyush Maini 作为 Datology 的联合创始人，同时也是卡内基梅隆大学（CMU）的博士生，他的研究方向和公司使命都聚焦于“数据中心化”的 AI 发展路径。他强调，尽管数据在 AI 系统中扮演着至关重要的角色，但它在研究领域却常常被低估。他的博士论文主题便是“负责任且高效地利用网络规模数据进行预训练”，这涵盖了如何从海量、混乱的网络数据中提取有价值的信息，同时确保数据的安全性和模型行为的负责任性，并对模型性能进行评估。

Pratyush 提到，Datology 团队内部有一个名为“数据很怪”的 Slack 频道，成员们会不断分享在数据集中发现的各种“奇怪现象”和“异常工件”。这些发现往往令人惊讶，因为互联网的深度和广度远超想象，其中包含着各种意想不到的内容，而这些内容最终都可能被用来训练模型。这种分享不仅是团队内部的乐趣，更反映了他们对数据进行“调查式”探索的共同热情。这种对数据细节的极致关注，正是 Datology 团队能够进行深入逆向工程分析的基础。

**个人感受**

Pratyush 描述“数据很怪”频道时的兴奋之情溢于言表，这不仅仅是技术人员的严谨，更是一种对未知世界探索的纯粹好奇。这种对数据“怪异”之处的欣赏，恰恰是发现深层规律、推动技术进步的源动力。它让人感受到，数据并非冰冷的二进制代码，而是充满生命力、等待被解读的宝藏。

**延伸思考**

一个专注于数据质量和数据洞察的团队，其内部文化必然会鼓励对数据进行深入的、甚至是“玩乐式”的探索。这种文化对于理解大型模型行为的细微之处至关重要。如果连训练者自己都无法完全理解数据，那么模型行为的不可预测性将成为常态。

### 2. 模型“过拟合”与“完美记忆”现象 `[02:30-06:50]`

**核心观点**

Pratyush 团队通过实验发现，当前许多大型语言模型在训练后期对特定考试（如印度 JEE 考试）题目存在“完美记忆”现象，这表明模型在训练的最后阶段可能被大量特定基准测试数据“过拟合”，从而影响其泛化能力。

**深度阐述**

主持人好奇“数据很怪”频道里最近有什么有趣的发现。Pratyush 分享了一个令人震惊的案例：他们发现，当向 Coher 等模型提问印度 JEE 考试（一项重要的奥林匹克竞赛级别考试）的问题时，模型不仅能正确完成问题，甚至能给出完整的选项。例如，当模型被提示“灯泡……”时，它能立即补全为一个完整的 JEE 考试问题，并提供正确答案。

这种现象在不同模型家族中普遍存在，并且在较新的模型版本（如 Coher 3）中尤为明显，而在早期版本（如 Coher 1.5 或 Coher 2）中则不常见。这表明，在这些模型的训练后期，可能存在对特定考试或基准测试数据的大量“加权”或“过拟合”。Pratyush 解释说，如果模型没有在训练后期多次看到这些考试题目，它不可能在行为上如此完美地完成这些问题，甚至给出选项。

这种“完美记忆”现象与模型大小和数据的新近度有关。更大的模型通常表现出更高程度的记忆能力。然而，Pratyush 也指出，随着模型能力的提升，即使是参数量相对较小的模型（例如，过去在 72B 模型上观察到的现象，现在在 20B 甚至 12B 模型上也能看到），也开始展现出这种精确的记忆能力。这暗示着模型架构和训练方法可能在不断优化，使其能够更有效地“记住”特定信息。

**视觉/结构信息描述**

此处描述了实验设置：向模型提供 JEE 考试问题的开头几个词（例如“灯泡”），观察模型如何补全问题并提供答案。

**延伸思考**

这种“完美记忆”现象引发了对模型泛化能力和训练数据构成的重要思考。如果模型在特定基准测试上表现出色仅仅是因为“记住”了答案，那么其真正的智能和推理能力就值得商榷。这对于评估模型性能和设计更有效的训练策略具有深远影响。

### 3. 海马表情符号之谜：模型自我修正行为的起源 `[06:50-14:50]`

**核心观点**

Pratyush 团队通过一个“海马表情符号是否存在”的简单问题，揭示了 OpenAI 等前沿模型在 GPT-4.1 和 GPT-5 系列中出现的显著“自我修正”行为。他们推测，这种行为源于训练数据中加入了大量的“推理痕迹”或“自我修正独白”，这表明自我反思能力已成为前沿模型基础能力的核心组成部分。

**深度阐述**

Pratyush 接着分享了另一个更具启发性的发现：去年十月，他注意到 Twitter 上有人发布了一个有趣的现象——当向 GPT 等前沿模型提问“海马表情符号是否存在？”时，模型会陷入一个无限循环的“是/否”自我修正模式。模型会先说“是”，然后开始“思考”，接着说“否”，然后又回到“是”，如此反复，永不停止。这种现象在 Grok、GPT 和 Gemini 等多个模型中普遍存在，即使是“非思考型”或较小的模型也未能幸免。

这种“自我修正”行为让 Pratyush 感到困惑，因为这些强大的模型本应能够解决更复杂的问题，却在一个简单的是非题上陷入“存在主义困境”。他最初猜测这可能与模型学习自我修正和自我反思行为有关，因为这在现代 AI 模型中越来越普遍，许多研究表明，如果模型能纠正自己的错误，其推理能力会显著增强。

为了探究这一现象的起源，Pratyush 绘制了一张图表，横轴是模型发布日期，纵轴是模型输出的 token 数量。他发现，在 2024 年 12 月之前发布的所有模型，对“海马表情符号”问题的回答都非常简短，要么直接说“是”，要么说“否”，但从未出现自我修正的循环。然而，在 2024 年 12 月 OpenAI 发布了第一个能够“思考”和“自我修正”的 O1 模型之后，仅仅四个月，GPT-4.1 系列模型就开始出现响应长度的显著增加，并展现出这种递归的自我修正行为。到 GPT-5 发布时，这种行为变得更加普遍。

Pratyush 强调，这种行为的出现与模型的“截止日期”（cutoff date）无关，而是与模型的“发布日期”紧密相关。例如，ChatGPT 4o 的原始版本在 2024 年 12 月发布时并未显示此行为，但在 5 月的更新后才出现。这表明 OpenAI 可能在模型发布后，通过后训练（post-training）的方式，加入了这些推理痕迹，从而使其展现出自我反思能力。

“海马表情符号”之所以能触发这种行为，是因为它是一个典型的“曼德拉效应”案例。许多人在 Reddit 等社交媒体上声称见过海马表情符号（例如，蓝色、马头朝左），但实际上并不存在。这种模棱两可的现实情况，为模型提供了一个完美的“触发器”，促使其进行思考和自我修正。

为了进一步验证这一假设，Pratyush 将目光转向了 Almo 系列模型，因为 Almo 团队以其开放性而闻名，他们会发布模型、数据，甚至提供 Almo Trace 工具，可以追溯模型响应与预训练数据之间的关联。他发现，Almo 2 模型（一年前发布）在面对相同问题时，只会给出错误的答案（例如“存在”），但不会自我修正。然而，Almo 3.1 32B 系列模型却展现出与 GPT 类似的自我修正行为，先说“是”，然后说“等等，没有”，形成一个完整的独白。

通过 Almo Trace 工具分析，Pratyush 发现这种自我修正行为并非简单地“复述”了某个特定的文本片段，而是一种模型内部的“能力”。更重要的是，Almo 团队在其报告中明确提到，他们在 Almo 3 的“中训练”（mid-training）阶段有意添加了“思考痕迹”（thinking traces）。这与 OpenAI 模型中观察到的现象高度吻合，即即使是非指令型（non-instruct）模型，也可能在预训练或中训练阶段被注入了自我修正的数据。

这一发现对前沿模型训练范式产生了深远影响。它表明，自我反思能力已经成为所有前沿模型训练的核心组成部分，而不再仅仅是后训练阶段的“锦上添花”。过去，人们认为基础模型（foundation model）只需提供通用能力，然后通过后训练或微调来获得特定能力。但现在看来，即使是基础模型本身，也需要预先具备某些核心能力（如自我反思），才能在后续的微调中发挥出最佳效果。

**视觉/结构信息描述**

- **图表描述**：一张横轴为模型发布日期，纵轴为输出 token 数量的图表，清晰展示了 GPT-4.1 和 GPT-5 系列模型在“海马表情符号”问题上响应长度的显著增长，以及自我修正行为的出现。
- **Almo Trace 工具**：描述了该工具如何帮助研究人员追溯模型响应与预训练数据之间的关联，从而验证模型行为是能力而非简单记忆。
**重要原话**：

- "The existence of the seahorse emoji is kind of called like a mandela effect where a lot of people on Reddit are saying that hey I have seen the seahorse emoji it looked blue in color and had a horse pointing to the left or something like that and so there is like enough doubt or like enough conversations on the internet that some people say yes and some people do say no and so it's kind of acting like a trigger to elicit that thinking response." `[09:50]`
- "This really shows us that even this foundation mod foundation needs to have the ingredients that of the capability that you desire at the end. And so putting thinking traces in the foundation is actually useful for the post- training or fine-tuning of uh the thinking models." `[13:30]`
**个人感受**

Pratyush 对“海马表情符号”的分析过程，从一个看似无厘头的现象出发，通过严谨的实验设计和跨模型对比，最终揭示了前沿模型训练数据中的核心秘密，这种侦探式的研究方法令人印象深刻。他对于模型内部“自我修正”机制的洞察，以及对“曼德拉效应”的巧妙运用，都展现了其作为数据科学家的敏锐和创造力。

**延伸思考**

如果自我反思能力已经成为基础模型的核心，那么未来的模型训练将更加注重“能力预埋”，而非仅仅是“知识灌输”。这对于模型设计、数据收集和训练策略都提出了新的要求。同时，这也引发了对模型“意识”或“思考”的哲学思考，尽管这可能只是模拟，但其行为模式已经越来越接近人类的认知过程。

### 4. “微调者谬误”与专业化预训练的兴起 `[14:50-17:30]`

**核心观点**

Pratyush 团队提出了“微调者谬误”（Finetuner's Fallacy）的概念，认为核心能力必须在基础模型中预先构建，而非仅仅通过微调获得。这预示着未来 AI 发展将走向专业化预训练，企业将为特定领域训练专属的基础模型，以实现更高的效率和性能。

**深度阐述**

Pratyush 提到，社区对他们的发现反响热烈，许多人认为这印证了他们此前的信念，或者提供了有趣的研究视角。他透露，Datology 团队正在进行一项名为“微调者谬误”的工作，预计在几周内发布。这项工作的核心论点与“海马表情符号”的发现不谋而合：如果存在一项核心能力是你真正关心的，那么这项能力应该成为基础模型的一部分，而不是仅仅通过微调来获得。

他们通过在不同领域展示这一观点，发现传统的“通用基础模型 + 微调”范式已经过时。随着 AI 在越来越多特定领域（domain-specific use cases）的应用，专业化预训练将成为未来的趋势。Pratyush 预测，2026 年和 2027 年将是企业开始进行专业化预训练的年份。

专业化预训练的优势在于，通过为特定领域定制预训练数据，可以训练出更小但能力与微调后的大模型相当的模型。这意味着预训练的成本将通过更高的效率和更小的模型尺寸得到快速摊销。例如，一个经过专业化预训练的 3B 模型，其性能可能与一个经过微调的 8B 模型相当。这对于 Datology 这样的数据公司而言，具有重要的战略意义。

**重要原话**：

- "If there is a core capability that you actually care about that capability should be part of the foundation and not a fine-tuned artifact." `[15:40]`
- "This really means there's going to be a lot of specialized pre-training going forward. So I think like 2026 and 227 are going to be the years where different enterprises start doing specialized pre-training because the cost of pre-training really amortizes itself very fast when you think of the fact that by doing specialized pre-training you can train a smaller model which is as capable as a much larger model when fine-tuned." `[16:20]`
**延伸思考**

“微调者谬误”的提出，是对当前 AI 训练范式的一次深刻挑战。它强调了数据和预训练阶段的重要性，预示着 AI 领域将从“大一统”的通用模型，走向“百花齐放”的专业化模型。这对于企业级 AI 应用、资源受限的场景以及追求极致性能的领域，都具有革命性的意义。

### 5. Beyond Web：合成数据与源重构范式 `[17:30-20:00]`

**核心观点**

Datology 通过其“Beyond Web”项目，展示了如何高效地利用合成数据进行模型训练。他们倡导“源重构范式”（Source Rephrasing Paradigm），即利用现有知识源（如互联网）并将其重构为高质量的训练数据，而非完全依赖大型模型生成数据，从而显著降低成本并提高数据质量。

**深度阐述**

Pratyush 接着介绍了 Datology 的另一个重要项目“Beyond Web”，该项目旨在展示如何将合成数据扩展到万亿规模的训练。他指出，当前合成数据主要有两种范式：

1. **生成器驱动范式（Generator-driven Paradigm）**：这种方法依赖于一个大型模型（如 GPT-4）来生成文本、文章或段落。其缺点是成本高昂，且严重依赖于生成模型的规模和提示词的质量，难以保证数据的多样性。早期的 Tiny Stories 和 Phi 模型家族采用了这种方法。
1. **源重构范式（Source Rephrasing Paradigm）**：这是 Pratyush 在苹果实习期间提出的替代方案。该范式认为，互联网上已经存在海量的知识，问题在于其质量不高。因此，我们可以利用一个小型模型，将这些现有知识“重构”成更高质量、更符合特定任务需求的数据。例如，将互联网上的信息重构为问答格式。这种方法的优势在于，合成数据生成的成本极低，因为即使是 1B 或 3B 的小型模型也能很好地完成数据转换任务，而无需包含整个互联网的知识。
Pratyush 强调，“源重构范式”已经成为 2026 年的主流，许多前沿模型（如 Kim K2、Grok 4、Nvidia 的 Neotron 数据集）都在使用这种方法。Datology 的“Beyond Web”项目进一步扩展了这一范式的优势，通过这种方法，他们训练出的 3B 模型能够达到 Nvidia 8B 模型的性能，并且训练时间缩短了 2.7 倍。这证明了高效利用合成数据和源重构范式在提升模型性能和降低训练成本方面的巨大潜力。

**视觉/结构信息描述**

- **图表描述**：展示了“Beyond Web”模型（蓝色线）在性能上与 Nvidia 模型相当，但在训练时间上显著缩短，并优于 Hugging Face 和 RedPajama 等其他模型。
**重要原话**：

- "The generative driven paradigm is exciting and doing well but it just does not scale. You need the model to be massive and generating data will be very expensive. Plus it really depends on you prompting in the right way..." `[19:00]`
- "The source rephrasing paradigm has actually become the dominant paradigm in 2026. Like even the Kim K2 model has like a long section of like how they do rephrasing of internet content. Then the even Gro 4 has been using the same source rephrasing paradigm." `[19:40]`
**延伸思考**

“源重构范式”的兴起，为合成数据的使用开辟了新的道路。它不仅解决了生成器驱动范式成本高昂、难以控制多样性的问题，更重要的是，它将数据处理的重点从“生成新知识”转向“优化现有知识”，这对于构建高质量、低成本的训练数据集具有革命性意义。

## 精华收获

1. **数据是 AI 的核心，而非次要因素**：Datology 团队的理念和实践深刻揭示了数据在 AI 训练中的决定性作用。对数据细节的深入挖掘和“侦探式”分析，是理解模型行为、推动技术进步的关键。
1. **模型存在“完美记忆”和“过拟合”风险**：大型模型在训练后期可能对特定基准测试数据产生“完美记忆”，这使得其在这些测试上的高分并不能完全代表其泛化能力。这提醒我们，在评估模型时需要更加谨慎，并关注训练数据的构成。
1. **自我修正能力已成为基础模型的核心**：通过“海马表情符号”实验，我们发现 OpenAI 等前沿模型在 GPT-4.1 和 GPT-5 系列中，已将“自我修正”和“推理痕迹”作为核心能力预埋在基础模型的训练数据中。这改变了传统上认为推理能力仅通过后训练获得的观念。
1. **“微调者谬误”预示专业化预训练的未来**：核心能力必须在基础模型中构建，而非仅仅通过微调。这意味着未来 AI 发展将走向专业化预训练，企业将为特定领域训练专属的基础模型，以实现更高的效率和性能。
1. **“源重构范式”是合成数据的高效路径**：Datology 的“Beyond Web”项目推广的“源重构范式”，通过将现有知识重构为高质量训练数据，显著降低了合成数据成本，并提高了数据质量，为大规模、高效的合成数据应用提供了可行方案。
这些洞察不仅加深了我们对当前大型语言模型训练机制的理解，也为未来的 AI 研究和应用指明了方向。数据不再仅仅是训练的“燃料”，更是塑造模型智能和行为的“基因”。

---
