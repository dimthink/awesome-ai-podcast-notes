---
title: "🔬Generating Molecules, Not Just Models"
channel: "Latent Space"
published: "2026-02-12"
source_url: "https://www.youtube.com/watch?v=nP0N1kYLegc"
video_id: "nP0N1kYLegc"
duration: "1:41:26"
---

# 🔬Generating Molecules, Not Just Models

- **Channel:** Latent Space
- **Published:** 2026-02-12
- **Source:** https://www.youtube.com/watch?v=nP0N1kYLegc

# 内容深度重构与阐述

## 材料信息

- **标题**：🔬Generating Molecules, Not Just Models
- **作者/来源**：Latent Space (Gabriella Corso 和 Jeremy Vulvin)
- **类型**：YouTube 视频字幕
- **关键元数据**：视频访谈，讨论了AlphaFold 2/3、Boltz的创立、BoltzOne/BoltzGen模型及其在蛋白质结构预测和分子设计中的应用，以及开放科学与商业化之间的平衡。
## 开篇引入

在生物科学与人工智能的交汇点，一场静默而深刻的革命正在发生。曾几何时，预测蛋白质的复杂三维结构被视为计算生物学的“圣杯”，其难度堪比解决一个NP难题。然而，随着AlphaFold 2的横空出世，这一领域被彻底颠覆，为药物发现和生物工程开启了前所未有的可能性。但当AlphaFold 3选择闭源，将这项突破性技术束之高阁时，两位来自MIT的年轻博士——Gabriella Corso和Jeremy Vulvin，毅然决定挺身而出，创立Boltz，旨在将最前沿的分子生成能力重新带回大众，特别是科研人员和生物技术公司手中。这不仅仅是一场技术竞赛，更是一场关于开放科学精神与商业化壁垒的较量。本文将深入探讨这场由AlphaFold引发的结构生物学革命，以及Boltz如何通过其创新模型和社区建设，重新定义分子设计的未来。

## 详细内容

### AlphaFold 2：结构生物学的里程碑 `[04:40-08:00]`

**核心观点**

AlphaFold 2的发布是蛋白质折叠问题上的一个真正突破，它不仅在科学上具有深远意义，也激发了个人对机器学习在结构生物学中应用的极大热情，并促使研究人员重新思考应用型机器学习的潜力。

**深度阐述**

在访谈中，Gabriella Corso首先回顾了AlphaFold 2问世时的激动人心时刻。对于非结构生物学家而言，理解蛋白质结构的重要性是关键。蛋白质是细胞中的“机器”，它们通过复杂的相互作用驱动着生命活动。结构生物学的目标正是要理解这些微观结构如何形成、如何相互作用，以及它们如何影响细胞功能。传统上，解析蛋白质结构依赖于X射线晶体学等复杂且耗时的方法，而计算生物学的梦想一直是无需实验就能预测结构。

AlphaFold 2的出现，正是实现了这一梦想的重大突破，它解决了“蛋白质折叠”这一核心问题——即预测单个蛋白质的三维结构。Gabriella作为一名计算机科学家，对机器学习在解决长期科学难题上的巨大影响力感到震撼。她提到，看到模型能够“创造生命”般地呈现出蛋白质的精美结构，对她个人而言是极大的鼓舞，这促使她投身于机器学习与结构生物学的交叉领域。

Jeremy Vulvin补充说，AlphaFold 2的成功也促使他们团队将研究重心从理论方法论转向应用型机器学习，特别是生物大分子领域。AlphaFold 2不仅回答了许多问题，也提出了更多问题：这种能力能否扩展到其他分子（如小分子、核酸）？能否预测蛋白质与其他分子（如小分子、核酸）的相互作用？能否模拟更复杂的蛋白质系统？这些问题迅速成为AlphaFold 2之后领域内的主要研究方向，预示着机器学习将以截然不同的方式解决这些问题。

**重要原话**：

- "Alphafold was a real breakthrough in this problem of protein folding which is trying to understand the structure of a single protein." `[05:50]` - AlphaFold是蛋白质折叠问题上的一个真正突破，它试图理解单个蛋白质的结构。
- "The seeing kind of the structures coming out of these models where you know you see kind of this beautiful creation of life is something that was very inspiring to me." `[06:40]` - 看到这些模型生成的美丽生命结构，对我来说非常鼓舞人心。
**延伸思考**

AlphaFold 2的成功不仅是技术上的胜利，更是科学范式转变的标志。它证明了深度学习在解决复杂科学问题上的巨大潜力，并激发了跨学科研究的热潮。然而，它也揭示了模型在处理动态系统、多状态蛋白质以及缺乏共进化信息时的局限性，为未来的研究指明了方向。

### 核心概念澄清：蛋白质、小分子与核酸 `[08:00-10:50]`

**核心观点**

理解生物大分子（蛋白质、核酸）与小分子之间的区别及其在生物系统中的作用，是把握结构生物学和分子设计领域进展的基础。

**深度阐述**

为了确保听众对后续讨论有清晰的理解，访谈中对几个关键术语进行了澄清。

- **蛋白质 (Protein)**：被认为是生命中最基础的分子之一，由DNA编码而来。它们是氨基酸的序列，每个氨基酸可以被视为一个“小分子”。人体中存在20种常见的氨基酸，这些氨基酸以不同的序列组合，形成种类繁多的蛋白质。蛋白质的数量极其庞大，每种蛋白质都有其独特的结构和功能。
- **小分子 (Small Molecule)**：顾名思义，通常指原子数量较少的分子。与氨基酸相比，小分子中的原子种类通常更多样，这使得小分子的设计和预测更具挑战性。它们在药物发现中扮演着重要角色，因为许多药物都是小分子。
- **核酸 (Nucleic Acids)**：包括DNA和RNA，它们在结构上与蛋白质有相似之处，也是由重复的单元（核苷酸）组成序列。DNA和RNA的结构建模同样重要。每个“密码子”（由三个核苷酸组成）翻译成一个特定的氨基酸，这揭示了核酸与蛋白质之间的紧密联系。
最终，所有这些分子——蛋白质、小分子、核酸——都不过是原子通过化学键连接在一起的集合，而结构生物学的核心任务就是理解它们之间的相互作用。

**视觉/结构信息描述**：这段内容主要通过口头解释，没有直接的视觉信息，但其描述的分子构成和相互关系是理解后续模型设计和应用的基础。

**延伸思考**

对这些基本生物分子的清晰定义，有助于我们理解为何AlphaFold 2首先聚焦于蛋白质，以及后续模型如何尝试扩展到更广泛的分子类型和相互作用。不同分子类型的复杂性差异，也直接影响了模型设计和数据需求。

### CASP竞赛与AlphaFold 2的突破 `[10:50-13:50]`

**核心观点**

CASP（蛋白质结构预测关键评估）竞赛是结构生物学领域重要的基准测试，AlphaFold 2在CASP 14上的表现是前所未有的突破，但其成功主要局限于单链蛋白质的结构预测，且高度依赖共进化信息。

**深度阐述**

Jeremy Vulvin回忆起AlphaFold 2在NeurIPS会议上公布CASP竞赛结果时的情景，那是一个令人难忘的时刻。CASP竞赛每两年举办一次，其核心目标是寻找与已知结构有显著差异的蛋白质结构，以此来挑战和评估各种预测方法。CASP组织者投入大量精力从学术界和工业界收集结构数据，构建难以预测的测试集。

CASP 14是AlphaFold 2真正“一鸣惊人”的时刻。它在预测准确性上取得了巨大飞跃，远远超越了所有先前的竞争者和方法。然而，Jeremy也强调，尽管AlphaFold 2取得了巨大成功，但CASP竞赛仍在继续，如CASP 15和16，并且已经扩展到蛋白质-小分子、蛋白质-核酸等其他模态的预测。这表明，即使在蛋白质领域，仍有许多未解决的问题，例如多聚体（多个蛋白质链组成的复合体）的预测仍然非常困难。CASP竞赛的存在，持续推动着领域的发展，并提醒研究人员模型能力的边界。

**重要原话**：

- "CASP 14 was when Alpha 2 really blew everything out of the water." `[11:50]` - CASP 14是AlphaFold 2真正一鸣惊人的时刻。
- "While we're become really really good at proteins basically monomeic proteins, you know Adamal is remain pretty difficult." `[13:00]` - 尽管我们已经非常擅长预测单体蛋白质，但多聚体仍然相当困难。
**延伸思考**

CASP竞赛的持续性及其对新模态的扩展，凸显了结构生物学领域的复杂性和多样性。AlphaFold 2的成功并非终点，而是新一轮研究的起点，促使研究人员探索更广泛的分子系统和更复杂的生物过程。

### AlphaFold 2解决了什么问题，又留下了什么挑战？ `[13:50-19:50]`

**核心观点**

AlphaFold 2在“预测单链蛋白质的最终三维结构”方面取得了巨大进展，但并未解决“蛋白质折叠过程”本身，且其性能高度依赖于共进化信息。蛋白质的动态性、多状态性以及与疾病的关联，仍是亟待解决的难题。

**深度阐述**

Jeremy和Gabriella谨慎地指出，尽管AlphaFold 2取得了突破，但用“解决”一词来形容它所做的工作可能会引起争议。他们认为，AlphaFold 2在“预测单链蛋白质结构”方面取得了巨大进展。单链蛋白质由单一氨基酸序列组成，其预测之所以能取得成功，很大程度上得益于模型能够利用“共进化”信息。

**共进化信息**：如果一个动物体内的某种蛋白质发生突变，为了保持结构和功能，其在其他生物体中的相似蛋白质也可能发生相应的突变。通过分析大量不同物种的蛋白质序列，可以发现某些位置的氨基酸倾向于同时进化。这种相关性通常暗示着这些氨基酸在三维空间中是相互靠近的。AlphaFold 2能够非常有效地解码这些进化线索，从而推断出蛋白质的结构。然而，这也意味着在缺乏共进化信息的情况下，模型的表现会大打折扣。

**结构预测与折叠过程的区别**：Gabriella强调，需要区分“结构预测”和“折叠过程”。AlphaFold 2擅长的是直接给出最终的稳定结构，但它并没有揭示蛋白质如何从无序状态一步步折叠成最终结构的过程。理解这个动态过程至关重要，因为蛋白质的错误折叠与许多疾病（如阿尔茨海默病）相关。如果不能理解折叠过程，就难以干预这些疾病。

**蛋白质的动态性**：蛋白质并非静态的，它们会根据能量状态采取不同的形状，并在不同状态之间切换。AlphaFold 2在理解蛋白质的这些动态多态性方面仍有不足。

**为何关心蛋白质形状？**

蛋白质是身体的“机器”，细胞内的所有过程都通过蛋白质来完成。理解蛋白质的结构和相互作用，对于理解身体如何运作、疾病如何发生至关重要。这就像看到一辆车的最终形态，比只看到零件清单更能理解它的功能。

**蛋白质的折叠状态**：蛋白质在体内是始终处于折叠状态，还是在需要时才折叠？这取决于蛋白质的稳定性。有些蛋白质一旦生成就非常稳定，保持其折叠形状；而另一些则具有多态性，根据环境（例如是否有其他分子存在）切换形状，从而执行不同功能。还有一些蛋白质是完全无序的，它们在许多疾病中扮演重要角色，但我们对其了解最少。

**NP难题与机器学习的突破**：蛋白质折叠问题曾被视为一个NP难题，因为氨基酸序列可能采取的形状数量呈组合爆炸式增长。机器学习的成功表明，蛋白质序列中蕴含着人类难以理解的信号（通过进化或其他机制），而模型能够学习并利用这些信号。

**重要原话**：

- "The problem that a lot of progress was made on was the ability to predict the structure of single chain proteins." `[14:40]` - 取得巨大进展的问题是预测单链蛋白质结构的能力。
- "Part of the breakthrough has been like our ability to also decode that very very effectively." `[16:00]` - 突破的一部分在于我们能够非常有效地解码（共进化信息）。
- "Folding is the more complex process of actually understanding like how it goes from like this disordered state into like a structured like state and that I don't think we've made that much progress on." `[16:50]` - 折叠是一个更复杂的过程，它涉及理解蛋白质如何从无序状态转变为结构化状态，我认为在这方面我们没有取得太多进展。
- "Proteins are not static. They move, they take different shapes based on their energy states." `[17:50]` - 蛋白质不是静态的。它们会移动，根据能量状态采取不同的形状。
**视觉/结构信息描述**：访谈中提到了“三维谷地”的比喻，形象地描述了蛋白质寻找低能量稳定结构的过程，以及共进化线索如何将搜索范围缩小到“接近解决方案的区域”。

**延伸思考**

AlphaFold 2的成功是基于对进化信息的巧妙利用，但这也限制了其在全新序列或缺乏进化信息场景下的表现。未来的模型需要更深入地理解物理原理，才能在更广泛的生物学问题上取得突破。

### AlphaFold 3：从结构预测到相互作用预测 `[24:00-30:00]`

**核心观点**

AlphaFold 3将结构预测扩展到多分子相互作用，通过统一模型处理蛋白质-蛋白质、蛋白质-小分子、蛋白质-核酸等多种模态，并在架构上引入了生成式建模和简化的结构模块，实现了新的技术飞跃。

**深度阐述**

AlphaFold 2的成功激发了Jeremy和Gabriella以及许多其他研究人员的兴趣。在AlphaFold 2发布后，一个显而易见的问题是：能否预测不同分子之间的相互作用？蛋白质的功能往往通过与其他蛋白质或小分子的相互作用来实现。例如，许多生物机器由多个蛋白质链组成，它们还需要与其他分子相互作用才能发挥功能。在药物设计中，设计能够以特定方式与目标蛋白质相互作用的分子至关重要。

AlphaFold 3正是针对这一挑战迈出了重要一步，它在建模相互作用方面取得了显著进展。与领域内其他团队尝试分别建模不同相互作用（如蛋白质-小分子、蛋白质-蛋白质）不同，AlphaFold 3将所有这些模态整合到一个统一的模型中进行训练。通过引入大量架构改进和数据，它成功地在一个模型中实现了跨所有模态的SOTA（State-of-the-Art）性能，包括蛋白质-小分子（对药物开发至关重要）、蛋白质-蛋白质、蛋白质-RNA/DNA等。

**关键架构和数据变化**：

1. **从回归到生成式建模**：这是一个关键的转变。AlphaFold 2将结构预测视为回归问题，即寻找一个单一的“正确”答案。而AlphaFold 3转向了生成式建模，它预测的是可能结构的一个后验分布，并从中进行采样。
1. **简化的结构模块**：AlphaFold 3显著简化了最终模型（将成对表示转换为实际结构的部分）的架构，使其更像传统的Transformer模型，而非AlphaFold 2中高度专业化的等变架构。尽管如此，Jeremy强调，这并非完全的“苦涩教训”（bitter lesson，指通用模型最终超越专业模型），因为该领域仍然高度依赖专业化架构，其性能远超简单Transformer。
1. **专业化架构的持续重要性**：Jeremy解释说，AlphaFold 2和3的核心思想是基于氨基酸之间的“成对上下文”进行操作。多序列比对（MSA）提供了关于哪些氨基酸可能靠近的初步线索。模型就像运行Dijkstra算法一样，解码这些潜在的接触，构建一个成对距离矩阵，然后从这个粗略的距离矩阵中推断出实际结构。这种“三角层”操作在处理二维表示（如距离矩阵）时非常自然，并且在监督学习中也很强大，因为它直接告诉模型哪些部分是靠近的。这种归纳偏置（inductive bias）使得模型在参数量相对较小的情况下，能够实现极高的计算效率和性能。
1. **原子级与氨基酸级建模**：AlphaFold 3的另一个创新是从纯粹的氨基酸级别建模，转向在原子分辨率和氨基酸（token）级别之间交替建模。这种“粗粒度-细粒度”的建模方式，对于处理小分子等其他模态特别有用，因为小分子需要更精细的原子级表示。
**重要原话**：

- "AlphaFold 3 was a significant advancement on the problem of modeling interactions." `[26:00]` - AlphaFold 3在建模相互作用问题上取得了显著进展。
- "They put everything together and train a very large models with a lot of advances... and managed to get a single model that was able to set a new state-of-the-art performance across all of these different kind of modalities." `[27:00]` - 他们将所有东西整合在一起，训练了一个包含许多进步的超大模型……并成功地获得了一个单一模型，在所有这些不同模态上都达到了新的SOTA性能。
- "Moving from modeling structure prediction as a regression problem... to a generative modeling problem where you have a posterior distribution of possible structures and you're trying to sample this distribution." `[28:00]` - 从将结构预测建模为回归问题……转向生成式建模问题，即拥有可能结构的后验分布并尝试从中采样。
**视觉/结构信息描述**：Jeremy在访谈中展示了Boltz平台上的蛋白质分子图像，清晰地展示了“粗粒度”（如螺旋和箭头表示的二级结构）和“细粒度”（如小分子与蛋白质相互作用的原子级细节）的结合。他解释了α螺旋、β折叠和无序环区这三种主要的二级结构及其生物学意义，特别是无序环区在抗体等药物设计中的关键作用。

**延伸思考**

AlphaFold 3的成功展示了统一模型处理多模态生物学问题的潜力，生成式建模的引入也为探索蛋白质动态性和不确定性提供了新途径。然而，其闭源策略也引发了关于科学开放性和技术民主化的讨论，这正是Boltz诞生的背景。

### AlphaFold 3的“陷阱”与Boltz的诞生 `[35:00-40:00]`

**核心观点**

AlphaFold 3的闭源策略对学术界和工业界造成了巨大冲击，促使Boltz团队决定自主开发开源模型BoltzOne，以民主化访问这些关键技术。

**深度阐述**

AlphaFold 3的发布无疑是一项惊人的科学成就，发表在了顶级的《自然》杂志上。然而，它也带来了一个巨大的“陷阱”：DeepMind（通过其衍生公司Isomorphic Labs）决定不开源该模型。这与AlphaFold 2形成了鲜明对比，后者开源后被全球数百万科学家使用，极大地推动了研究进展。

AlphaFold 3的闭源意味着学术研究人员和生物技术公司无法再直接利用这一最先进的模型进行研究和药物开发。这对于依赖AlphaFold等基础模型进行创新的领域来说，是一个巨大的打击。

面对这一挑战，Jeremy和Gabriella决定“自己动手”。他们利用AlphaFold 3论文中公开的信息，着手构建一个具有相似准确度的模型。这就是BoltzOne的由来，它是第一个完全开源、能够接近AlphaFold 3准确度的模型。

**BoltzOne的开发过程**：

- **速度惊人**：从2023年5月开始，到11月发布，BoltzOne的开发速度非常快。这得益于团队在AlphaFold 2时代积累的经验，以及对扩散模型等相关技术的独立探索。
- **计算资源挑战**：开发过程并非一帆风顺。由于计算资源有限，他们只能对大型模型进行一次训练。在模型训练过程中，他们不得不“在飞行中”修复错误，暂停训练、打补丁、重新启动，而没有从头开始。这种“不可能重现”的训练过程，使得最终的模型具有独特的“学习曲线”，甚至可能学到一些“奇怪的东西”，但奇迹般地奏效了。
- **外部支持**：训练过程的另一个挑战是依赖共享计算集群，导致训练任务经常排队等待。最终，Genesis的CEO Deon提供了计算支持，帮助他们完成了模型的训练，否则可能需要额外数周时间。
**从学术项目到公司**：在开发BoltzOne的过程中，团队意识到，仅仅将模型放在GitHub上不足以实现其民主化生物技术工具的使命。要让化学家和生物学家真正将这些模型应用于治疗项目，还需要构建模型之上的完整生态系统，包括用户友好的工作流程、基础设施和优化。因此，他们决定成立一家公共利益公司（public benefit company）——Boltz，以推动这一使命。

**重要原话**：

- "The catch was that it was an amazing paper nature paper but unfortunately they decided not to release the model." `[35:00]` - 陷阱是，这是一篇了不起的《自然》论文，但不幸的是，他们决定不发布模型。
- "We decided that to take the matter in our own hands and decided to try to obtain a model that was of similar accuracy." `[37:00]` - 我们决定自己动手，尝试获得一个具有相似准确度的模型。
- "We only trained the big model once... while the model was training we were like finding bugs left and right... we just like kept training it with like the bug fixes along the way, which was impossible to reproduce now." `[39:00]` - 我们只训练了一次大模型……在模型训练过程中，我们不断发现错误……我们只是在训练过程中不断修复错误，现在已经无法重现。
**延伸思考**

AlphaFold 3的闭源策略引发了关于科学研究成果共享与商业利益之间的紧张关系。Boltz的创立不仅是对这一挑战的回应，也体现了开放科学和技术民主化的重要性，尤其是在对人类健康有重大影响的领域。

### BoltzOne与AlphaFold 3的比较及模型验证 `[40:00-48:00]`

**核心观点**

BoltzOne及其同期模型在准确性上已接近AlphaFold 3，但在某些特定任务（如抗体-抗原预测）上仍有差距。模型验证的关键在于建立清晰的基准测试，并持续通过实验反馈来改进模型，以应对泛化性挑战。

**深度阐述**

**BoltzOne与AlphaFold 3的比较**：

BoltzOne以及同期出现的其他开源模型，相较于之前的开源模型，取得了巨大的飞跃，在准确性上已经非常接近AlphaFold 3的水平。然而，Gabriella承认，即使到今天，AlphaFold 3在某些特定情况下仍然具有优势，例如在抗体-抗原相互作用预测方面。由于这些模型是不同的，运行结果也会有所不同，因此不能简单地说一个模型总是优于另一个，但在总体上，AlphaFold 3在当时仍略有优势。

**模型验证的重要性**：

如何判断一个模型是否优于另一个？在结构预测领域，验证相对直接。就像CASP竞赛一样，验证方法是：

1. **训练数据**：模型在截止某个日期之前发布的所有结构数据（主要来自蛋白质数据库PDB）上进行训练。PDB是一个公共数据库，所有生物学家都会在此发布其解析的结构。
1. **测试数据**：寻找近期发布的、与训练数据中已知结构差异很大的新结构。这有助于评估模型的泛化能力。
1. **评估**：在这些新结构上评估不同模型的性能。
这种方法使得模型之间的比较相对容易和标准化。

**开放科学与社区反馈**：

Gabriella强调，开源模型的一大优势是能够从社区获得大量反馈。虽然有时会收到对模型表现良好的赞扬，但更有价值的反馈是关于模型在哪些方面表现不佳。这种反馈对于改进模型至关重要。

**基准测试与泛化性**：

机器学习领域的进步离不开清晰的基准测试。随着模型在特定基准上取得进展，就需要不断改进基准，使其更具挑战性。Gabriella以她博士期间开发的DiffDock模型为例：

- DiffDock是早期预测蛋白质-小分子相互作用的模型之一，在当时的基准测试上表现出色，超越了传统的基于物理的方法。
- 然而，当将DiffDock提供给生物学家使用时，他们发现模型在预测与训练数据差异很大的蛋白质时表现不佳。
- 这促使他们与哈佛大学的Nick Pitsy团队合作，开发了新的基准测试，专门用于评估模型在泛化性方面的表现。然后，他们根据这个新基准改进了模型架构。
这种“发现模型不足 -> 建立新基准 -> 改进模型”的循环，是推动领域进步的关键。Jeremy补充说，尽管模型仍有不足，但该领域的发展速度是不可否认的，每年都在取得显著进步。

**重要原话**：

- "Bolts one but also kind of these other kind of set of models that came around the same time were kind of approaching were a big leap from you know kind of the previous kind of open source models and you know kind of really kind of approaching the level of alpha 3." `[40:00]` - BoltzOne以及同期出现的其他模型，相较于之前的开源模型，取得了巨大飞跃，在准确性上已经非常接近AlphaFold 3的水平。
- "The great thing about structure prediction... is that basically the way that you can evaluate them is that you train the model on a structure that was released across the field up until a certain time... and then we basically look for recent structures... and on this new structure we evaluate all these different models." `[41:50]` - 结构预测的伟大之处在于……评估它们的方法是：在截止某个时间点之前发布的所有结构上训练模型……然后我们寻找近期发布的新结构……并在这些新结构上评估所有不同的模型。
- "Most of the times and to be honest that's also maybe the most useful feedback is you know people sharing about where it doesn't work." `[44:00]` - 大多数时候，也是最有用的时候，是人们分享模型在哪里不起作用。
**延伸思考**

模型验证的严谨性是确保科学发现可靠性的基石。Boltz团队通过积极与社区互动、建立挑战性基准，并不断迭代模型，展示了开放科学和以问题为导向的研究方法在推动领域进步中的强大作用。

### 开放科学与商业化：Boltz的平衡之道 `[48:00-55:00]`

**核心观点**

Boltz通过开放源代码模型促进社区进步，同时通过构建用户友好的产品平台（Boltz Lab）提供增值服务，平衡了开放科学与商业化需求，旨在民主化分子设计工具。

**深度阐述**

**开放源代码的价值与挑战**：

Gabriella承认，开放源代码模型确实意味着任何人都可以复制他们的工作。然而，Boltz的核心使命是民主化这些工具。他们认为，开放源代码模型对于推动社区研究进步至关重要，因为研究人员可以基于这些模型进行创新，而Boltz也能从社区的反馈中学习。

**Boltz Lab的商业化策略**：

Boltz意识到，仅仅提供开源模型是不够的。要让化学家和生物学家在实际的治疗项目中有效使用这些工具，需要一个完整的产品生态系统。因此，Boltz Lab应运而生，它提供了超越模型本身的增值服务：

1. **工作流程和代理 (Agents)**：Boltz Lab将复杂的分子设计过程封装成“代理”，例如蛋白质代理和小分子设计代理。这些代理不仅仅是模型，更是一套完整的“配方”，包括数据预处理、高效搜索设计空间、确保分子可合成性等多个步骤。例如，小分子设计代理会使用生成模型来确保生成的分子可以使用合适的构建块进行合成。
1. **基础设施 (Infrastructure)**：运行这些模型需要巨大的计算资源。Boltz Lab提供了一个大规模的GPU集群，能够并行处理数万甚至数十万个设计任务。这使得用户可以高效地进行大规模筛选，而无需自行管理昂贵的计算资源。Jeremy指出，通过规模经济，Boltz可以分摊成本，使得在他们的平台上运行模型比个人自行部署更经济。他们还通过模型加速优化，将小分子筛选速度提高了10倍。
1. **用户界面 (Interface)**：Boltz Lab提供API和图形用户界面（UI）。API适用于希望将Boltz功能集成到现有工作流中的公司。UI则旨在扩大用户群体，让非计算背景的科学家也能轻松使用。UI还包括协作功能，例如多个药物化学家可以共同评估结果，进行共识构建。
**开放与商业的平衡**：

Boltz的理念是，即使模型是开源的，运行它们也需要成本。通过提供优化的基础设施和用户友好的产品，Boltz Lab能够以更低的成本提供更好的服务。他们将继续开源基础模型，以促进研究社区的进步，同时通过Boltz Lab提供卓越的产品体验，让科学家无需成为计算专家也能利用这些工具。这就像普通用户使用ChatGPT而不是自行部署开源LLM一样。

**重要原话**：

- "Putting a model on GitHub is definitely not enough to get chemists and biologists... to use your model to in their therapeutic programs." `[49:00]` - 将模型放在GitHub上绝对不足以让化学家和生物学家……在他们的治疗项目中使用你的模型。
- "A lot of what we think about at Bolts beyond kind of the just the models is thinking about all the layers that come on top of the models to get... from those models to something that can really enable scientists in the industry." `[49:30]` - 在Boltz，除了模型本身，我们更多地思考模型之上的所有层，以将这些模型转化为真正能够赋能行业科学家的东西。
- "We will continue to put a lot of our models open source because the critical kind of role I think of open source models is you know helping kind of the community progress on the research." `[52:00]` - 我们将继续开源我们的许多模型，因为我认为开源模型的关键作用是帮助社区在研究上取得进展。
**延伸思考**

Boltz的商业模式为开放科学项目提供了一个可持续发展的路径。通过将核心技术开源以促进创新和社区参与，同时通过提供商业产品解决实际应用中的痛点，Boltz有望在推动科学进步和实现商业价值之间找到最佳平衡点。

### Boltz社区的成长与贡献 `[55:00-59:00]`

**核心观点**

Boltz通过开源策略和对易用性的关注，迅速建立了一个活跃的社区，社区的贡献不仅包括技术优化，还包括创新的模型使用方法，这些都极大地推动了Boltz模型和平台的进步。

**深度阐述**

Boltz社区的成长速度令团队感到惊喜。每次发布新模型，社区成员数量都会大幅增长。他们拥有一个数千人的Slack社区，并且这个社区已经实现了“自我维持”——成员之间互相回答问题、提供帮助，减轻了Boltz团队的负担。GitHub上的社区也同样活跃，贡献了许多代码和想法。

**社区贡献的例子**：

1. **技术优化**：一位社区成员为架构中的某个部分编写了复杂的GPU内核，这部分代码自AlphaFold 2以来一直存在，但直到Boltz才有人对其进行优化，这极大地提升了性能。
1. **创新应用**：社区成员探索了模型的新用途，例如如何“破解”模型来设计环肽。
1. **推理时搜索策略**：Tim O'Donnell在Slack频道中提出了一个巧妙的策略，用于改进抗体-抗原相互作用预测。当模型在预测抗体与抗原的结合位点时出现偏差时，他尝试向模型提供随机提示，让模型预测抗体与抗原上不同残基（氨基酸）的结合。通过扫描抗原上的所有残基，并评估模型对每个结合位点的置信度，然后选择置信度最高的结合位点。这种“推理时搜索”的粗略方法，在抗体-抗原预测中取得了显著效果。这启发了Boltz团队思考如何更智能地进行这种搜索。
**易用性与社区增长**：

Jeremy认为，Boltz社区之所以能快速增长，很大程度上归因于他们对模型易用性的重视。尽管仍有改进空间，但相较于其他工具，Boltz的代码库更容易使用，这降低了用户的入门门槛。

**持续的开源承诺**：

Boltz不仅发布了BoltzOne，还陆续开源了BoltzTwo（改进结构预测并增加亲和力预测功能）和蛋白质设计模型BoltzGen。这种持续的开源策略，使得Boltz成为一个提供全面分子设计工具套件的平台，并建立了社区对其模型质量和领先地位的信任。

**重要原话**：

- "It's actually like self-sustaining now, which is like the really nice part because... people would answer each other's questions and like sort of like, you know, help one another." `[55:50]` - 它现在实际上是自我维持的，这是非常好的部分，因为……人们会互相回答问题，互相帮助。
- "There's a lot of papers also that have come out with like new evolutions on top of bolts." `[56:50]` - 也有很多论文在Boltz的基础上提出了新的进化。
- "I think it speaks also I think to the importance of like you know when when you put code out like to try to put a lot of emphasis in like making it like as easy to use as possible." `[57:00]` - 我认为这也说明了当你发布代码时，要非常重视使其尽可能易用。
**延伸思考**

Boltz社区的成功是开放科学精神的生动体现。通过积极的社区互动和对用户反馈的重视，Boltz不仅提升了自身模型的性能和应用范围，也为整个分子设计领域注入了新的活力。

### BoltzGen：从预测到生成 `[59:00-1:06:00]`

**核心观点**

BoltzGen将结构预测模型转化为生成式设计工具，能够从头设计新的蛋白质序列和结构，并通过创新的编码方式将结构和序列预测统一，并通过严格的实验验证确保其有效性。

**深度阐述**

**从预测到生成**：

BoltzGen是Boltz团队在分子设计领域迈出的重要一步。他们认为结构预测模型（如AlphaFold和BoltzTwo）是“基础模型”，它们学习了蛋白质和其他分子如何相互作用的规律。BoltzGen利用这些基础模型的学习能力，通过微调（fine-tuning）使其能够生成全新的蛋白质。

**BoltzGen的工作原理**：

1. **输入**：用户首先提供一个目标蛋白质（例如，希望新蛋白质与之结合的靶点）以及对新蛋白质的高级设计规范（例如，希望设计一个具有特定框架的抗体或肽）。
1. **提示与空白标记**：这些设计规范被转化为模型的“提示”，并结合一系列“空白标记”（blank tokens），表示待设计的蛋白质序列。
1. **扩散模型生成**：模型（基于扩散模型）解码生成新的结构和序列。它不仅预测新蛋白质的结构，还同时预测其氨基酸序列。
1. **评分与筛选**：生成的设计会通过BoltzTwo等模型进行评分，评估其与目标蛋白质的结合亲和力。
**结构与序列预测的统一**：

BoltzGen的一个关键创新在于将结构预测和序列预测合并为几乎相同的任务。传统上，这两个任务通常分开处理，一个涉及离散的序列，另一个涉及连续的结构。BoltzGen通过一种巧妙的编码方式解决了这个问题：

- 模型只进行结构预测，但由于结构是原子级的，并且不同的氨基酸具有不同的原子组成，因此从原子排列中可以同时推断出所需的结构和氨基酸的身份。
- 这种方法避免了处理离散和连续信号之间的不兼容性，使得模型能够利用与BoltzTwo（以及AlphaFold 3）相似的可扩展监督信号来设计新蛋白质。
**实验验证的挑战与方法**：

BoltzGen论文的一个重要部分是其严格的实验验证。由于Boltz团队本身不是生物实验室，他们与外部合作进行验证。Hannes Stark（团队成员）开创性地提出，不应只在特定系统上进行验证，而应在广泛多样的场景下测试模型，以确保其泛化能力。

**广泛的合作验证**：

- BoltzGen与约25个学术和工业实验室合作，共同测试模型的设计。
- 论文中展示了来自8-10个实验室的结果，涵盖了多种设计任务：
- 这些验证涵盖了广泛的目标和应用，为模型提供了强大的泛化性证据。
**重要原话**：

- "With BoltzGen what we did was taking kind of that kind of foundation models and then fine-tune it to predict kind of entire new proteins." `[1:00:00]` - 对于BoltzGen，我们所做的是利用这种基础模型，然后对其进行微调，以预测全新的蛋白质。
- "The only thing that you're doing is predicting the structure... because the structure is atomic and you know the different amino acids have a different atomic composition basically from the way that you place the atoms. We also understand not only kind of the structure that you wanted but also the identity of the amino acid." `[1:03:00]` - 你唯一要做的就是预测结构……因为结构是原子级的，并且不同的氨基酸具有不同的原子组成，所以从原子的排列方式中，我们不仅理解你想要的结构，还理解氨基酸的身份。
- "He basically put together I think it was something like 25 different academic and industry labs that committed to testing some of designs from the model." `[1:04:50]` - 他召集了大约25个学术和工业实验室，承诺测试模型的一些设计。
**延伸思考**

BoltzGen代表了分子设计领域从“预测已知”到“生成未知”的范式转变。其创新的结构-序列统一预测方法，以及对广泛实验验证的重视，为开发真正可用的生成式分子设计工具奠定了基础。

### 分子设计中的关键概念：肽、纳米抗体与制造挑战 `[1:06:00-1:10:00]`

**核心观点**

肽、迷你蛋白质和纳米抗体是分子设计中常见的治疗性分子类型，它们因尺寸、结构和制造便利性而受到关注，但设计和“人源化”仍是挑战。

**深度阐述**

为了非生物学背景的听众，访谈中进一步解释了BoltzGen设计的一些关键分子类型：

- **肽 (Peptides)**：本质上是小蛋白质。它们是常见的治疗药物，例如Ozempic和Wegovy（GLP-1受体激动剂）就是肽类药物。肽由规范和非规范氨基酸组成。
- **迷你蛋白质 (Mini-proteins)**：这是一个相对模糊的术语，泛指各种形状的小型蛋白质。
- **抗体 (Antibodies)**：是人体免疫系统中的一种特殊蛋白质，通常由四条蛋白质链（两条重链和两条轻链）组成，形成复杂的结构。它们是非常常见的治疗药物。
- **纳米抗体 (Nanobodies)**：是抗体的一种简化形式，存在于骆驼、羊驼和鲨鱼等动物中。与人类抗体复杂的四链结构不同，纳米抗体由单链蛋白质组成，因此结构更简单。近年来，它们也成为一种常见的治疗药物类型。尽管它们最初来源于动物，但需要经过“人源化”处理，以确保它们对人体无毒且有效。
**设计趋势与制造考量**：

Jeremy指出，分子设计领域有一个普遍趋势，即倾向于设计更小的分子（如迷你蛋白质、纳米抗体、小肽）。这主要是出于**制造便利性**的考虑。蛋白质越大，其制造过程通常越复杂、成本越高。然而，小型化也可能带来其他挑战，例如可能降低选择性（即分子结合特定靶点的能力），因为它们可能缺乏大型分子所拥有的更多“手”来精确结合。

**重要原话**：

- "Peptides is a small protein and is a relatively common type of of therapeutic." `[1:06:50]` - 肽是一种小蛋白质，是相对常见的治疗药物。
- "Nanobodies that I mentioned that are sort of like the equivalent of antibodies but on specific in specific animals... it's a single protein." `[1:08:00]` - 我提到的纳米抗体，它们类似于抗体，但存在于特定动物中……它是一种单一蛋白质。
- "There's a general pattern I think in like in trying to design things that are smaller... it's easier to manufacture." `[1:09:00]` - 我认为在设计更小的东西时有一个普遍模式……它更容易制造。
**延伸思考**

分子设计不仅是计算问题，更是工程问题。在设计新分子时，除了预测其结构和功能，还需要考虑其可制造性、稳定性和生物安全性等实际应用因素。BoltzGen等工具的价值在于，它们能够帮助研究人员在设计早期就考虑到这些因素。

### 蛋白质的构建与实验验证流程 `[1:10:00-1:14:00]`

**核心观点**

从计算设计到实验室验证，蛋白质的构建涉及DNA合成、蛋白质表达、纯化和结合强度测量等一系列复杂步骤，需要专业的湿实验室（wet lab）合作。

**深度阐述**

尽管Boltz团队不直接进行湿实验室工作，但Jeremy详细解释了从计算设计到实验验证的典型流程：

1. **设计输出**：BoltzGen等模型输出的是目标蛋白质的序列（例如，抗体或结合剂的氨基酸序列）以及靶点蛋白质的序列。
1. **DNA合成**：这些蛋白质序列首先需要转化为DNA序列。通常，这会委托给专门的DNA合成公司。
1. **蛋白质表达**：合成的DNA被引入生物体（如酵母或细胞系），“劫持”其细胞机制来生产蛋白质。这个过程称为“表达”。
1. **蛋白质纯化**：表达出来的蛋白质需要从细胞的其他成分中分离出来。通常，会在蛋白质上添加一个“标签”，以便通过亲和层析等方法进行纯化。
1. **结合测定 (Binding Assay)**：一旦获得纯化的目标蛋白质和结合剂，就可以进行结合测定，测量它们之间的结合强度。有多种实验方法可以完成这一步骤，例如在微孔板中进行测量。
1. **结果反馈**：实验结果会反馈给设计团队，包括是否成功结合以及结合强度（例如，纳摩尔级结合）。
**重要原话**：

- "We have to order the DNA that's yet another company that produces that DNA sends it over and then you have to like express the proteins." `[1:11:00]` - 我们必须订购DNA，这是另一家公司生产的，然后你必须表达蛋白质。
- "You're kind of like hijacking the yeast to create." `[1:11:50]` - 你有点像劫持酵母来创造。
- "Once you have like your pure target your pure binder you can then like run your binding assay." `[1:12:50]` - 一旦你有了纯化的靶点和结合剂，你就可以进行结合测定。
**延伸思考**

分子设计是一个多学科交叉的领域，计算工具的进步必须与实验验证紧密结合。理解湿实验室的复杂流程，有助于计算科学家设计出更具实验可行性和转化潜力的分子。

### BoltzGen的广泛验证与泛化能力 `[1:14:00-1:18:00]`

**核心观点**

BoltzGen通过与广泛的学术和工业实验室合作，在多样化的、具有挑战性的靶点上进行了严格的实验验证，特别关注模型在“未见过”靶点上的泛化能力，证明了其设计新颖分子的潜力。

**深度阐述**

Jeremy和Gabriella进一步详细阐述了BoltzGen的验证工作：

1. **多样化的应用场景**：验证工作涵盖了多种实际生物学问题。例如，他们设计了靶向RAC1（一种参与代谢的蛋白质）的肽，以及针对其他治疗相关靶点的肽和分子。
1. **超越已知相互作用的泛化性测试**：BoltzGen的一个关键验证目标是评估模型在泛化性方面的表现，即它能否设计出与训练数据中“未见过”的靶点结合的新分子。
**重要原话**：

- "One of the things that we found with the field was that a lot of the validation especially outside of the validation that was done on specific problems was done on targets that have a lot of known interactions in in the training data." `[1:16:00]` - 我们发现，该领域的大部分验证工作，尤其是在特定问题之外的验证，都是针对训练数据中已知相互作用很多的靶点进行的。
- "We took nine targets from the PDB filter into things where there is no known interaction... So there is no way that the model from its training set can sort of like say okay I'm just going to tweak something and and just imitate this particular kind of interaction." `[1:16:50]` - 我们从PDB中选择了9个靶点，这些靶点没有已知的相互作用……所以模型不可能从训练集中说“我只是要调整一些东西并模仿这种特定的相互作用”。
- "On two-thirds of those targets we were able to from these 15 designs get nanomolar binders." `[1:17:50]` - 在这些靶点中，有三分之二我们能够从这15个设计中获得纳摩尔级结合剂。
**延伸思考**

BoltzGen的验证策略强调了在分子设计中评估模型泛化能力的重要性。通过在“未见过”的靶点上进行测试，BoltzGen证明了其生成真正新颖、有效分子的潜力，这对于药物发现和生物工程领域具有里程碑意义。

### Boltz Lab：产品化与未来展望 `[1:18:00-1:30:00]`

**核心观点**

Boltz Lab是Boltz将分子设计工具产品化的努力，它通过整合代理、优化基础设施和提供用户界面，旨在为所有科学家提供易于访问、高效且可扩展的分子设计平台，并持续关注药物开发中的可开发性属性。

**深度阐述**

**Boltz Lab的三个核心组成部分**：

1. **代理 (Agents)**：这些代理是Boltz Lab的核心，它们将复杂的分子设计流程自动化。例如，蛋白质代理和小分子设计代理。这些代理不仅仅是模型，而是一套完整的“食谱”，指导用户完成从靶点准备到高效搜索设计空间，再到确保分子可合成性（通过生成模型使用合适的构建块）的全过程。
1. **基础设施 (Infrastructure)**：为了支持大规模的分子设计活动（例如，筛选10万个候选分子），Boltz Lab提供了强大的GPU集群。这种基础设施能够以并行方式运行计算，显著缩短设计周期，并分摊计算成本，使其比个人自行运行更经济。Boltz还通过模型加速优化，将小分子筛选速度提高了10倍。
1. **用户界面 (Interface)**：Boltz Lab提供API和图形用户界面（UI）。API适用于希望将Boltz功能集成到现有工作流中的公司。UI则旨在让更广泛的非计算背景科学家也能轻松使用，并支持协作功能，例如多个药物化学家可以共同评估设计结果，进行共识构建。
**可访问性与商业模式**：

Boltz Lab对所有人开放访问请求，并为学术界和初创公司提供免费积分。对于大型公司，他们提供定制化的部署和合作模式。Boltz的理念是服务所有用户，而不仅仅是大型企业，这与他们的开源精神一脉相承。

**验证代理系统**：

当模型开始设计新颖的、没有共进化数据的分子时，验证变得更具挑战性。Boltz团队强调，计算指标只能提供部分信息，最终的验证必须回到湿实验室。他们通过与CRO（合同研究组织）合作，进行大规模的实验验证，以统计学上显著的方式评估模型的命中率和结合强度。他们选择的靶点总是处于“可能性的前沿”，既不太容易也不太困难，以确保能够观察到模型改进的进展。

**不追求药物开发**：

Boltz明确表示，他们不打算成为一家治疗公司。他们的目标是构建工具，赋能科学家。他们设计的分子并非直接的药物，而是需要经过后续的开发阶段。他们希望通过提供更好的工具，帮助科学家在药物发现的早期阶段就考虑到可开发性（developability）和ADME（吸收、分布、代谢、排泄）等关键属性。

**与药物化学家的互动**：

药物化学家通常对机器学习模型持怀疑态度。Boltz通过将一位经验丰富的药物化学家Jeffrey引入团队，获得了宝贵的内部反馈。Jeffrey从最初的怀疑者变成了平台最活跃的用户之一，他利用Boltz Lab并行运行数百个GPU进行多重假设测试，并深入分析模型结果。这种“亲身体验”和“看到不可能”的时刻，是说服药物化学家的关键。

**未来方向**：

Boltz将继续深入改进模型，不仅关注结合亲和力，还关注药物开发中的其他关键属性，如可开发性。他们也在思考如何将实验结果反馈回模型，以更好地理解细胞内的生物物理和通路相互作用，尽管他们不打算构建一个“虚拟细胞”。

**重要原话**：

- "Boltz Lab is sort of combination of these three objectives into like one, you know, sort of cohesive platform." `[1:24:00]` - Boltz Lab是将这三个目标组合成一个内聚平台的产物。
- "Running bolts on our platform especially on in a large screen is like considerably cheaper than it would probably take anyone to put the open source model out there and run it." `[1:26:00]` - 在我们的平台上运行Boltz，尤其是在大规模筛选时，比任何人在开源模型上自行运行都要便宜得多。
- "You really got to go to the lab and test... how much better are we... how stronger are my binders?" `[1:27:00]` - 你真的必须去实验室测试……我们有多好……我的结合剂有多强？
- "We are not a biolab and you know we are not a therapeutic company... we see oursel as building tools for scientists." `[1:29:00]` - 我们不是生物实验室，也不是治疗公司……我们认为自己是为科学家构建工具。
- "When you bring them a machine learning model, it is sometimes quite tricky to get them to deal with it." `[1:31:00]` - 当你给他们一个机器学习模型时，有时很难让他们接受。
- "For people to be convinced you have to show them something that they didn't think was possible." `[1:33:00]` - 要说服人们，你必须向他们展示一些他们认为不可能的事情。
**视觉/结构信息描述**：访谈中提到了Boltz Lab的用户界面，以及药物化学家如何利用它进行并行筛选和结果分析，这暗示了平台在可视化和交互性方面的设计。

**延伸思考**

Boltz Lab的推出标志着分子设计领域进入了一个新的阶段，即从纯粹的研究工具向可扩展、用户友好的产品平台转变。这种转变对于加速药物发现和生物工程的实际应用至关重要，同时也强调了跨学科协作和用户反馈在产品开发中的核心作用。

## 精华收获

1. **AlphaFold的深远影响**：AlphaFold 2是蛋白质结构预测领域的里程碑，它不仅解决了单链蛋白质结构预测的难题，更激发了机器学习在结构生物学中的巨大潜力。然而，它也揭示了模型在处理蛋白质动态性、多状态以及缺乏共进化信息时的局限性。
1. **AlphaFold 3的创新与争议**：AlphaFold 3通过统一模型处理多分子相互作用，引入生成式建模和简化的结构模块，实现了新的技术飞跃。但其闭源策略引发了关于科学开放性与商业化之间平衡的讨论，直接促成了Boltz的诞生。
1. **Boltz的使命与策略**：Boltz致力于民主化分子设计工具。他们通过开源BoltzOne等模型，促进社区研究进步；同时，通过Boltz Lab平台提供产品化服务，解决实际应用中的计算资源、工作流程和用户体验痛点，实现开放科学与商业价值的平衡。
1. **BoltzGen的生成式设计能力**：BoltzGen将结构预测模型转化为生成式设计工具，能够从头设计全新的蛋白质序列和结构。其创新的结构-序列统一预测方法，以及在广泛、挑战性靶点上的严格实验验证，证明了其设计新颖分子的潜力。
1. **模型验证的关键性**：在分子设计领域，计算指标只是第一步，最终的验证必须通过湿实验室实验。Boltz通过与CRO和学术实验室合作，在多样化靶点上进行大规模实验验证，确保模型的泛化能力和实际有效性。
1. **跨学科协作与用户体验**：分子设计是一个多学科交叉的领域。Boltz通过将药物化学家引入团队，并关注用户界面和协作功能，成功地将复杂的机器学习工具转化为非计算背景科学家也能有效使用的产品。
1. **未来展望**：Boltz将继续深入改进模型，不仅关注结合亲和力，还将考虑药物开发中的可开发性、ADME等关键属性。他们致力于构建工具，赋能科学家，而非直接开发药物，旨在成为分子设计领域的“基础设施”提供者。
---
