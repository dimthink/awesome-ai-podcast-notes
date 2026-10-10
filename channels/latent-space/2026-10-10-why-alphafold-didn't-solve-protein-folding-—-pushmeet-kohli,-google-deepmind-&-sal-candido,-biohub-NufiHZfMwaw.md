---
title: "Why AlphaFold Didn't Solve Protein Folding — Pushmeet Kohli, Google DeepMind & Sal Candido, Biohub"
channel: "Latent Space"
published: "2026-10-10"
source_url: "https://www.youtube.com/watch?v=NufiHZfMwaw"
video_id: "NufiHZfMwaw"
tags: ["AI for Science", "蛋白质折叠", "AlphaFold", "数据规模化", "可解释性"]
rating: 4
language: "英文"
word_count: 19936
duration: "32:42"
---

# Why AlphaFold Didn't Solve Protein Folding — Pushmeet Kohli, Google DeepMind & Sal Candido, Biohub

- **Channel:** Latent Space
- **Published:** 2026-10-10
- **Source:** https://www.youtube.com/watch?v=NufiHZfMwaw
- **TL;DR:** AlphaFold 解决的是 PDB 复现任务，而非蛋白质动力学——真正的科学才刚开始。
- **Tags:** AI for Science, 蛋白质折叠, AlphaFold, 数据规模化, 可解释性
- **Rating:** 4

## 版本

- [结构化文稿](2026-10-10-why-alphafold-didn't-solve-protein-folding-—-pushmeet-kohli,-google-deepmind-&-sal-candido,-biohub-NufiHZfMwaw.structured.md)
- [原始文稿](2026-10-10-why-alphafold-didn't-solve-protein-folding-—-pushmeet-kohli,-google-deepmind-&-sal-candido,-biohub-NufiHZfMwaw.transcript.md)

# 为什么 AlphaFold 没有解决蛋白质折叠问题——深度重构

## 材料信息

- **标题**：Why AlphaFold Didn't Solve Protein Folding — Pushmeet Kohli, Google DeepMind & Sal Candido, Biohub
- **频道/来源**：Latent Space
- **类型**：YouTube 视频字幕（播客/对谈节目）
- **关键元数据**：对话嘉宾为 Google DeepMind 的 Pushmeet Kohli 与 Chan Zuckerberg Biohub 的 Sal Candido；场景为某生物科学大会的 "Modeling Session"（建模分会场）；话题覆盖 AI for Science、蛋白质折叠、数据规模化、可解释性、转化医学；节目末尾有"2 分钟警告"，提示这是一场限时对谈


## 开篇引入

在 AI for Science 的叙事中，AlphaFold 几乎是一个神话级的存在。2020 年 CASP14 的横空出世，让"蛋白质折叠问题已被解决"成为媒体头条和公众共识。然而，在这期 Latent Space 的对谈中，Google DeepMind 的 Pushmeet Kohli——AlphaFold 项目的核心人物之一——却亲手拆解了这个神话。他坦率地承认：**"我们并不知道蛋白质真正的基态是什么，也不知道蛋白质结构的真实分布。我们所做的，只是复现别人已经解析并存入 PDB 的那个结构。"**

这句话的分量，堪比当年 Feynman 说"我无法创造的东西，我就还没有理解"。因为对谈的两位主角——一位来自全球最顶尖的 AI 实验室，一位来自以"治愈所有疾病"为使命的 Biohub——他们共同指向一个更清醒的真相：**AI 在生物学上的胜利，目前仍是一座精致的脚手架，而非一栋竣工的大厦。** 

这场对话的价值，不在于又一次的 AI 乐观主义宣言，而在于它以罕见的诚实，讨论了一个被媒体叙事掩盖的核心问题：当我们在说"AI 解决了 X"的时候，我们究竟在解决什么？剩下的那些"没被解决的部分"，才是真正值得下注的地方。而对于任何关注 AI 与科学交叉领域的人来说，这场对谈提供了三个层面的洞察——**数据哲学、建模方法论、以及"理解 vs 设计"的认知张力**。


## 详细内容

### 一、"蛋白质折叠已解决"是一个修辞，而不是事实 `[00:00-01:30]`

**核心观点**
AlphaFold 所做的是"从 PDB 到 PDB"的结构复现任务，而不是对蛋白质动力学的理解。蛋白质不是静态的"积木"，而是动态、无序、依赖上下文变化的复杂系统。

**深度阐述**

对谈一开场，Pushmeet Kohli 就抛出了一个反直觉的论断——这几乎是对他自己参与创造的 AlphaFold 神话的一次自我纠正。他说：

> "When people sort of say the protein folding problem has been solved, like at the conceptual level, yes, there might be sort of yes, there has been some advances."
> ——"当人们说蛋白质折叠问题已经被解决时，在概念层面，是的，确实取得了一些进展。" `[00:03]`

但紧接着，他揭示了真相的另一半：

> "We don't know what is the actual true ground state that protein state and what is the actual distribution of structure that proteins take. What we are trying to do is basically someone got a structure, deposited it in the PDB, and we are trying to replicate and get the same structure. That's what we did, right? And it just so happens that it's useful."
> ——"我们并不知道蛋白质真正的基态是什么，也不知道蛋白质结构的真实分布。我们所做的，本质上只是：有人解析了一个结构并存进了 PDB，而我们尝试复现并得到相同的结构。这就是我们做的事，对吧？而它恰好是有用的。" `[00:15-00:45]`

这里有一个极其重要的方法论区分。**科学传播语言中"问题被解决"（solved）** ，通常意味着一个完整现象的理论和预测能力已经建立。但 AlphaFold 解决的，是一个**工程意义上的模式匹配任务**——给定氨基酸序列，预测出与 PDB 数据库中已知结构一致的三维构象。这是一个极其有用、甚至革命性的工具，但它并不等同于"理解了蛋白质折叠"。

Pushmeet 进一步用一个日常比喻戳破了"蛋白质是积木"的流行说法。他说：

> "Proteins are not blocks and they're not sort of they don't act as blocks, right? I say proteins are the building blocks all the time, but actually like I don't believe in it, right? Proteins are extremely complex. They are disordered. Their shape might change depending on the context."
> ——"蛋白质不是积木，它们的行为也不像积木。我一直说蛋白质是生命积木，但实际上我并不真的相信这句话。蛋白质极其复杂，它们是无序的，形状会随上下文变化。" `[01:05-01:25]`

这是理解 AlphaFold 局限性的关键。在细胞中，蛋白质并不是一张静态的"三维照片"，而是一个**动态的、会呼吸的、随环境变化的机器**。同一个蛋白质在不同 pH、不同结合伙伴、不同翻译后修饰下可能呈现完全不同的构象。AlphaFold 输出的是"某一种被解析出来的构象"，而不是"蛋白质在活细胞中的所有可能状态"。

**延伸思考**
这种"已解决"的误读，在 AI 领域极其常见。自动驾驶、通用翻译、代码生成……都曾被宣布"被解决"。但科学问题的真正难点，往往不在于**在标准基准上达到高分**，而在**在真实世界的开放分布中保持稳健**。AlphaFold 在 PDB 上的高精度，本质上是一道"考试题已被标准化"的任务；而蛋白质在活细胞中的动态行为，才是一道"考试题目本身还在变化"的开放世界问题。

**精华收获**
- 看到一个 AI 里程碑时，第一问应该是：**训练目标是什么？它对应的真实问题是什么？两者之间的 gap 有多大？**
- "AI 解决了 X"这句话，往往隐藏着"AI 在 X 的某个子集上达标了"的缩略。


### 二、数据的"苦涩教训"：先找 scaling law，再谈 scale `[01:30-05:00]`

**核心观点**
Scaling law 并非天然存在，而是需要被"发现"的。真正的稀缺资源不是数据量，而是**包含正确信息统计量的数据**。模型开发者最大的偏差，是倾向于解决"现有数据能解决"的问题，而非"真正需要解决的问题"。

**深度阐述**

主持人抛出了一个精妙的改问：**既然有"苦涩教训"（The Bitter Lesson），那么数据层面是否也存在一个"苦涩教训"？**

这一问，引出了 Sal Candido 的一段极富实操洞察的回答：

> "I think one misconception of scaling laws is that scaling laws are everywhere and they always exist. I think a lot of the work is actually finding that scaling law. A lot of what we really do is trying to figure out what's the situation where if you put more compute into it, if you put more data into it, you actually get a better result out. And the reason that's a great situation is then once that happens, you can kind of just turn the crank, right? Like it becomes an engineering problem."
> ——"关于 scaling law 的一个误解是：它无处不在，而且天然存在。但实际上，很多工作的核心是**发现**这个 scaling law。我们真正做的，是找出在什么情况下，投入更多算力、更多数据会带来更好结果。一旦找到这种情况，你就可以拧动曲柄，它变成了一个工程问题。" `[02:00-02:40]`

这段话有极强的工程哲学意味。**Scaling law 不是宇宙给 AI 研究者的礼物，而是一个研究者用无数次失败换来的"开关"**。一旦被找到，研究就从"科学探索"变成"工程扩大"——这正是 AlphaFold、GPT 系列能够快速迭代的底层逻辑。

接着，Sal 对"数据可用性偏差"给出了极其诚实的自我剖析：

> "I'm lazy, so I'm going to work with what's available. […] There is actually like a good side and a bad side to this."
> ——"我很懒，所以我会选择用现成的数据。……这件事有好的一面也有坏的一面。" `[03:00-03:15]`

具体案例是蛋白质语言模型的训练。他提到：

> "When we train a protein language model we train on metagenomic sequences, which are not the highest quality data. In fact, much of that data I can guarantee you isn't even a real whole protein. And yet that makes the performance of the model go up for designing real proteins that work."
> ——"我们训练蛋白质语言模型时用的是宏基因组序列，这些并不是最高质量的数据。实际上，我可以保证其中很多甚至不是真正完整的蛋白质。但正是这样的数据，让模型在设计真实可用的蛋白质时表现更好。" `[03:30-04:00]`

这里有一个非常反直觉的洞察：**"脏数据"有时比"精炼数据"更有用**。因为宏基因组数据虽然嘈杂，却包含了进化过程中真实蛋白质分布的统计信息——而这些信息恰恰是"设计能工作的蛋白质"所必需的。这和传统机器学习中追求"最干净、最精选"的范式形成了鲜明对比。

但 Sal 也警告这种"懒"的负面效应：

> "That can lead you to a negative place where you say, 'Well, let's just scale up the data that we can generate easily.' And I think that's not the necessary way to do it."
> ——"这可能把你带到一个错误的方向：'好吧，我们就把容易生成的数据扩大规模吧。'我认为这不是必要的路径。" `[04:15]`

他随后指出解决之道在于**社区协作**：如果只由建模者组成团队，他们会倾向于已有的数据；如果只由数据生成者组成团队，他们会倾向于容易生成的数据。只有当两者**以开放的方式在整个过程中协同**，才能找到"问题真正需要的数据"，然后才能发现 scaling law。

**精华收获**
- 不要假设 scaling law 天然存在。**先做实验去发现它**，再all-in。
- 数据的"信息量"比"清洁度"更重要。宏基因组序列的案例告诉我们：**嘈杂但覆盖面广的数据可能优于干净但覆盖面窄的数据**。
- 团队构成决定了数据偏见。**建模者 + 数据生成者 + 领域专家的三角协作**，是避免"解决容易问题"的结构性解法。


### 三、跨学科第一性原理：Pushmeet 的"苦涩教训"再解读 `[05:00-08:30]`

**核心观点**
"苦涩教训"的真正含义不是"scale 无敌"，而是**不要用"我是建模者"或"我是数据生成者"的宗教式身份认同来解决问题**。问题优先，方案灵活。

**深度阐述**

这是整场对谈中最具哲学深度的一段。Pushmeet Kohli 亲历了 Rich Sutton 在 DeepMind 内部的"苦涩教训"讲座，但他给出的解读角度和大众理解非常不同：

> "The thing that I took from Rich's original lecture was not about the actual notion of whether data is useful. I think my take was that he was talking about something more conceptual. […] Sometimes when we are looking at problems, we think about solutions in a very religious way. I'm a modeler or I'm a data generation person. And I think that is the bitter lesson that if you approach the problem with that mindset, you might not succeed. The problem comes first."
> ——"我从 Rich 原始讲座中获得的，不是关于数据是否有用的具体论断。我的理解是，他谈的是更概念化的东西。……有时候我们看问题时，会用一种宗教式的方式来思考解决方案：'我是建模者'或'我是数据生成者'。我认为这才是真正的苦涩教训——如果你用这种心态去解决问题，你可能不会成功。**问题优先。**" `[05:30-06:20]`

这是一种对 "The Bitter Lesson" 的**方法论重读**。主流解读通常是"scaling 终将胜利，不要浪费时间做手工特征工程"。但 Pushmeet 认为，Sutton 真正想说是一种**智力上的谦卑与灵活性**——不要执着于某种方法论身份，而是让问题本身来决定用什么工具。

他接着用两个亲身案例来说明这种灵活性如何体现：

**案例一：AlphaFold 的选择**
> "With AlphaFold, we looked at what was possible with current existing data sets because we did not have the core expertise of now sort of going to or even the resources to say, 'Let's augment the PDB by a significant order of magnitude.' […] So, you have to focus on getting the biggest bang out of your buck by investing it in modeling."
> ——"在 AlphaFold 上，我们审视了现有数据集的可能性——因为我们既没有核心专长，也没有资源去说'让我们把 PDB 扩大一个数量级吧'。……所以你必须聚焦于把资源投入到建模上，以获取最大回报。" `[06:45-07:20]`

这里揭示了一个被忽视的事实：**AlphaFold 的成功部分源于"数据扩展不可行"这一约束**。正是因为扩充 PDB 的成本高不可攀，DeepMind 才被迫把全部筹码压在建模能力上。约束催生了创新。

**案例二：细胞基因组学的选择**
> "In other areas, with say cell genomics, we took the same approach and said, 'Well, what can you do with cell by gene?' And there it was very clear after a bunch of work that the data was not there yet to be able to go after that grand ambition of building the virtual cell."
> ——"在其他领域，比如细胞基因组学，我们采取了同样的方法：'用细胞×基因的数据能做什么？'经过一系列工作后非常清楚：数据还不够，无法去追求构建'虚拟细胞'这个宏大目标。" `[07:20-07:50]`

同一个方法论，得出完全相反的结论——AlphaFold 走建模路线，虚拟细胞则必须先去生成数据。这正是"问题优先"原则的具体体现。

**延伸思考**
这个框架可以泛化到任何 AI 应用领域。在创业和研究中，最常见的失败模式不是技术选错，而是**在错误的抽象层次上定义问题**。如果一家公司说"我们做数据标注"或"我们做大模型"，那它已经陷入了 Pushmeet 所说的"宗教式思维"。真正健康的问题定义应该是："我们要解决的现实问题是什么？它需要哪些数据、模型和领域的组合？"

**精华收获**
- **把"我是建模者/数据人"的身份标签撕掉。** 身份认同是创新的敌人。
- 约束不是障碍，而是**方向指示器**。资源限制反而能帮你做出更聚焦的选择。
- 用同一方法论去检验不同问题，允许得到不同答案。**方法论的一致性 ≠ 结论的一致性**。


### 四、手工艺 vs 规模化：一场被误读的对立 `[08:30-12:30]`

**核心观点**
"手工特征工程"与"规模化"不是二元对立。好的归纳偏置（inductive bias）让小数据场景可行；而当数据量足够时，不准确的归纳偏置反而会成为束缚。同时，"scale"本身就是一门手艺。

**深度阐述**

主持人提出了一个尖锐的问题：AlphaFold 2 是一件"艺术品"——大量精心设计的手工特征；但业界共识似乎在向更通用、更可扩展的策略演进。**我们是否还应该投入资源做"手工艺"？还是应该把有限资源投入 scale？**

Pushmeet 的回答再次回到第一性原理：

> "When you think about the arts and crafts of how do you construct a model to be better, I think it was not an accidental thing. We did a lot of experimentation, but there was a vision behind it. All this scientific intuition that came from biophysics and biochemistry—that those interactions of amino acid residues are not just doing their own thing, they are being influenced by other residues. So, let's bake that in. […] Use that information and try to give the model that unfair advantage."
> ——"当你思考如何手工构造一个更好的模型时，这不是偶然的。我们做了大量实验，但背后有愿景。来自生物物理和生物化学的科学直觉告诉我们：氨基酸残基的相互作用不是孤立的，它们相互影响。所以，让我们把这个先验'烘焙'进模型。……利用这些信息，给模型一种'不公平的优势'。" `[09:00-09:45]`

这里有一个关键的模型设计哲学：**科学先验知识作为归纳偏置，可以极大提升数据效率**。AlphaFold 2 之所以能用相对有限的数据达到惊人精度，正是因为它的架构中嵌入了"残基之间相互影响"这一来自结构生物学的先验。模型不需要从零开始学习"蛋白质是什么"，它只需要学习"在这些已知规则下如何组装"。

Pushmeet 随即抛出了一个更深刻的观点：

> "Curating good data is an art in itself. […] It's not just about big data, it's about good data. Actually understanding the coverage of what data is necessary for making progress in the problem is, in fact, I would say, a much more interesting and much more challenging problem in itself."
> ——"筛选好数据本身就是一门艺术。……这不仅仅是关于大数据，而是关于好数据。实际上，理解'解决这个问题需要什么样的数据覆盖'，我认为是一个更有趣、也更具挑战性的问题。" `[10:00-10:40]`

Sal 则从另一个角度补充，把这场对话推向高潮：

> "I kind of object to your question too because I think there actually is a lot of craft to the scaling part of things as well. […] Not only from an infrastructure perspective, but we're actually seeing things going beyond transformers to more bespoke architectures. I don't think we're in a post-transformer world in any way, shape, or form, but we're modifying those architectures in order to make them more fit for purpose."
> ——"我也对你的问题有异议，因为我认为规模化本身也需要大量的手艺。……不仅是基础设施层面，我们还看到架构正在超越标准 Transformer，走向更定制化的方向。我不认为我们在任何意义上处于后 Transformer 时代，但我们正在修改架构，让它们更适配目标。" `[11:00-11:45]`

Sal 这段话点破了一个流行谬误——**"scale"不是一个简单的按钮，而是一整套算法工程**。如何在更长的上下文、更大的模型、更多的数据下保持稳定性？如何设计更适配特定领域的架构？如何做数据选择（data selection）——即"下一批需要的信息是什么"？这些都是极难的研究问题。

**延伸思考**
在创业语境下，这个讨论对应一个经典战略问题："做垂直整合"还是"做通用平台"？Pushmeet 的答案是：**取决于数据量**。在数据稀缺的垂直领域，垂直整合（把领域知识"烘焙"进产品）是必要的；在数据丰沛的通用领域，通用平台可能更占优势。但两者都需要"手艺"——只是手艺的形态不同。

**精华收获**
- 归纳偏置和数据量之间存在**权衡曲线**：小数据→高偏置；大数据→低偏置。
- "好数据"的定义与具体问题绑定。**数据覆盖度分析**是一项独立且高价值的研究方向。
- **Scale 本身是手艺，不是魔法。** 微调架构、数据选择、稳定性工程，都是未被充分认知的硬研究。


### 五、功能、动力学、设计：下一个大跃进卡在哪里？ `[12:30-15:30]`

**核心观点**
AlphaFold 的下一个瓶颈不在算法，而在于是否愿意"回到源头"——直接操作冷冻电镜（cryo-EM）数据，而不是 PDB 的静态结构。同时，模型本身要从"轮辐"（spoke）升级到"轮子"（wheel），甚至"整辆自行车"。

**深度阐述**

主持人把话题引向具体的科学前沿：**功能、动力学、设计**——这三个方向中，哪个是最大的瓶颈？如果给你一根魔杖，能变出更多什么，会加速进展？

Pushmeet 给出的答案带着强烈的"计算机视觉学者"本色：

> "My computer vision researcher in me was super excited about cryo-EM micrographs. I was like, 'What is this PDB data? I should be working at the source, right? I should be looking at the cryo-EM micrographs. I don't want those structures. They must be missing out on all the data.' Now, getting models that can scale at that level with the right amount of data and can extract all the dynamics and distributional information that is captured there would be an amazing thing. I tried it, but it requires more work."
> ——"我内心那个计算机视觉研究者的部分对冷冻电镜显微图非常兴奋。我想：'这个 PDB 数据是什么？我应该直接在源头工作，对吧？我应该直接看冷冻电镜图像。我不想要那些已经解析好的结构——它们肯定丢失了大量信息。'如果能构建出可扩展的模型，从这些图像中提取出所有动力学和分布信息，那将是非常惊人的事。我尝试过，但这需要更多工作。" `[13:30-14:15]`

这是一个极具方向性的洞察。**PDB 是一个"已经过人类判断过滤"的数据层**。当科学家解析冷冻电镜图像时，他们通过平均化和建模，把动态的、分布的信息压扁成了单一静态结构。如果模型直接从原始图像学习，理论上可以保留**整个构象分布**——这才是真正的动态理解。Pushmeet 坦承他尝试过，但失败了；然而他认为这是一个值得后人继续的方向。

Sal 则用一个极其生动的比喻阐述了"当前模型的能力边界"：

> "You've got someone who's trying to understand how a bicycle works, and you're modeling a spoke on it. Those models can get better and better over time, but a lot of what you really need to do is you need to move from models of spokes to wheels to maybe whole bicycles. […] It seems like people want to use the model of the bicycle to design the part for a pickup truck."
> ——"有人试图理解自行车如何工作，而你建模的只是一个轮辐。这些模型可以越来越好，但你需要从轮辐模型，升级到车轮模型，再到整辆自行车模型。……而且看起来，人们想用自行车的模型，去设计一个皮卡车的零件。" `[14:30-15:10]`

这段比喻精妙地捕捉了 AI for Science 的一个根本性困境：**模型所捕捉的"科学对象"的粒度，与实际应用所需的粒度之间，常常存在巨大的鸿沟**。AlphaFold 建模的是"一个相对静态的蛋白质构象"，但药物设计者真正需要理解的，是"蛋白质在药物分子作用下的动态响应"——这是完全不同层次的问题。

**精华收获**
- **回到数据源头**（如冷冻电镜原图）可能是下一个 AlphaFold 级别的机会。
- 评估一个模型时，要问：**它在"科学粒度阶梯"上处于哪一级？** 离真实应用还差几级？
- 用自行车零件模型去设计皮卡零件——这是许多 AI 应用失败的隐喻。


### 六、理解 vs 设计：Feynman 的诅咒与 AI 的黑箱 `[15:30-20:00]`

**核心观点**
"我无法创造的东西，我就还没有理解"——但在 AI 时代，我们可以创造而不理解。Pushmeet 主张：**理解是必要的，但"理解"的定义应更务实**——不是"人类能解释内部机制"，而是"能对模型行为进行特征描述（behavioral characterization）"。

**深度阐述**

主持人引用了 Feynman 那句著名的"我无法创造的东西，我就还没有理解"，并抛出一个紧张的问题：**当 AI 可以一键设计出皮摩尔级结合力的分子时，"理解"还重要吗？**

Sal 第一个回应：

> "We were designing things with magical black boxes long before AI came around. […] But I think that the understanding is really important. There's so much for these models to learn, and as intelligence is getting cheaper, you can deploy it to learn more and more things. But then how do you actually pull that knowledge out of the machine, so to speak, and make it something that I can understand?"
> ——"在 AI 出现之前很久，我们就用神奇黑箱来设计东西了。……但我认为理解非常重要。这些模型能学到的东西太多了，随着智能越来越便宜，你可以部署它去学习越来越多东西。但然后呢？你怎么把知识从机器里'拉'出来，变成我能理解的东西？" `[16:00-16:50]`

Sal 随后透露了一个关键发现：**模型内部的信息量远大于我们知道的**。

> "We've worked a lot on interpretability. And you find a lot of information in there. People know that protein language models learn some notion of structure within their representations. But we find information about some functions. We find information about motions. And so I think there's a lot in there still to be unlocked even from the models that we have now. […] You expect a world model to come out of trying to compress all this information into the model. How does the model do its job? Well, it's compressed all the information from evolution into this model."
> ——"我们在可解释性上做了大量工作。你在里面能发现很多信息。人们知道蛋白质语言模型学到了结构的某种表征。但我们还发现了功能信息，发现了运动（motion）信息。所以我认为，即使是我们现在已有的模型，里面仍有大量信息等待解锁。……你期望一个世界模型出现——它是通过把所有信息压缩进模型而得到的。模型如何工作？它把进化过程中的所有信息压缩进了这个模型。" `[17:00-18:00]`

这是一个惊人的观点：**蛋白质语言模型是一个"进化压缩包"**。进化在数十亿年里试过的所有蛋白质序列、结构、功能的关联，都被压缩进了模型的权重中。因此，模型不只是"预测器"，而是**一个可以查询的进化知识库**——我们需要的是把它里面的信息解压出来的方法。

Pushmeet 则给出了一个更有争议、也更务实的框架。他首先区分了两种"理解"：

**第一层：行为理解（behavioral understanding）——必要**
> "AlphaFold actually is not perfect. It's 90 GDT. […] But even if it was 95 GDT, but the PLDDT score was completely uncalibrated, who would trust it? It would just magically give good answers, but suddenly tell you 'here's the answer, very confident', and you'll be working on it for the next one year and finding out it was completely wrong. The calibration of the uncertainty measure was extremely important."
> ——"AlphaFold 其实并不完美，是 90 GDT。……但即便它是 95 GDT，如果 PLDDT 分数完全没有校准，谁会信任它？它会神奇地给你好答案，但突然告诉你'这就是答案，非常自信'，然后你为此工作一年，才发现它完全错了。**不确定性度量的校准**极其重要。" `[18:20-19:00]`

这是 AlphaFold 从论文变成工具的关键一步——**让用户知道模型什么时候可以信任，什么时候不能**。Pushmeet 认为这属于"理解"的范畴：不是理解内部的每一步计算，而是理解模型的行为边界。

**第二层：机制理解（mechanistic understanding）——可以推后**
> "Interpretability asks the question, interpretable by whom? If you're saying interpretable by a human rational system with the cognitive and computational limitations of the human brain, then no, AlphaFold 2 is not interpretable. But if you are asking, is AlphaFold 2 interpretable to a much larger and more sophisticated model? Maybe it is. We just don't get it."
> ——"可解释性要问：对谁可解释？如果你说对人类理性系统（受限于人类大脑的认知和计算能力）可解释，那 AlphaFold 2 不可解释。但如果你问，AlphaFold 2 是否对一个更大、更复杂的模型可解释？也许是。只是我们人类理解不了。" `[19:00-19:40]`

这是整场对谈中最激进的论断之一。Pushmeet 提出了一种**"相对可解释性"（relative interpretability）** 的概念：也许未来的大型前沿模型可以直接读取 AlphaFold 的激活层，并生成关于其工作机制的理论——就像今天的 AI 帮人类分析复杂的物理模拟数据一样。这暗示了一种"AI 解释 AI"的认识论转向。

**个人感受**
这段对话充满了科学家面对自身创造物时的两难情绪。一方面，Pushmeet 和 Sal 都深知模型的局限，对"已解决"叙事保持警惕；另一方面，他们又都真诚地相信模型内部蕴含的宝藏远未被开采。这种张力——**既是批判者，又是建设者**——贯穿整场对谈。

**延伸思考**
"理解 vs 设计"的张力，其实是整个科学哲学的核心议题之一。古希腊人认为"掌握知识即掌握原因"，但 20 世纪的量子力学已经告诉我们：**很多现象可以被精确预测，却无法被"理解"成人类直觉可把握的图景**。AI 时代的到来，把这一矛盾从物理领域扩展到了生物、化学、医学——**我们可能必须在"能造"和"能懂"之间学会共存**。

**精华收获**
- **行为特征描述（behavioral characterization）比机制可解释性更务实、更紧急。** 先让用户知道模型的边界，再谈内部的"为什么"。
- 不确定性校准是 AI 工具化的生命线。**一个不告诉你"我可能错了"的模型，比一个精度略低的模型更危险。**
- "可解释性"是一个关系型概念——**对谁可解释？** 未来 AI 的"用户"可能是另一个 AI。


### 七、加速临床：10% 还是 10x？ `[20:00-结束]`

**核心观点**
"AI 结果进临床"是一个定义不清的问题——AI 已经进入药物发现全流程，真正的问题是**何时会出现 10x 级时间线加速**。而这需要理解生物学的"艰难挑战"，而非仅仅优化现有流程。

**深度阐述**

主持人的最后一个问题带着"量化预测"的诉求：**多久之后我们会看到 AI 结果进入临床？**

Pushmeet 首先解构了这个问题的模糊性：

> "AI is being used today already in every part of the drug discovery process. So, if from that perspective, it's already there. But if you are asking when will we see that 10x acceleration or 100x acceleration in the timelines, then the other question is: what are we accelerating? Is it lead optimization? Is it target discovery? Is it preclinical work?"
> ——"AI 今天已经被用在药物发现流程的每个环节。从这个角度讲，它已经在那里了。但如果你问的是，我们什么时候能看到时间线上 10x 或 100x 的加速——那另一个问题就是：我们在加速什么？先导化合物优化？靶点发现？临床前工作？" `[21:00-21:45]`

他的答案体现了一种科学家式的谨慎乐观：

> "Over the next few years—which is why this effort that we announced today is extremely important—we need to tackle some of these hard challenges of biology. And only then will we be able to get these true unlocks of acceleration that dramatically transform how drug discovery will happen. AI will be there in the clinic and will be impacting things that go into the clinic all the time, but the actual larger acceleration will be unlocked only with a better understanding of the biological models that this effort is trying to create."
> ——"在未来几年内——这就是我们今天宣布的这个项目极其重要的原因——我们需要攻克生物学的一些艰难挑战。只有那样，我们才能真正解锁那种戏剧性改变药物发现方式的加速。AI 会一直在临床和进入临床的环节发挥作用，但真正的大加速，只有通过更好地理解生物学模型才能解锁。" `[21:45-22:30]`

Sal 则给出了一个方法论层面的洞察，这是全场的点睛之笔：

> "One thing I learned a long time ago in my career, back at Google: sometimes it's easier to approach a problem by looking at what is it going to take to make a 10x improvement rather than a 10% improvement. And that's not because that's necessarily an easier path. It's because it allows you to take a broader view and see some solutions that you haven't been approaching."
> ——"我职业生涯早期在 Google 学到的一件事：有时候，通过思考'做出 10x 改进需要什么'，比思考'做出 10% 改进需要什么'，更容易接近问题。这不是因为 10x 更容易，而是因为它让你拥有更广阔的视野，看到一些你之前没有触及的解决方案。" `[22:40-23:20]`

他用这个框架解释了 Biohub 的使命选择：

> "I'm very happy that at Biohub we have a very beautiful and lofty mission statement: to cure all disease. If you want to do that, you really need to go and figure out what is the 10x approach. I think it's a really great opportunity to go through that."
> ——"我很高兴 Biohub 有一个非常美丽而崇高的使命：**治愈所有疾病**。如果你想做到这一点，你就必须去找出 10x 的路径。" `[23:20-23:50]`

**个人感受**
对谈以掌声结束。整个对话像一个精心编排的"反高潮"叙事——不是发出"AI 已解决一切"的欢呼，而是给出"我们才刚刚开始"的清醒与勇气。Sal 最后一句话尤其动人：治愈所有疾病，不是 10% 的改良，而是一个必须用 10x 思维才能接近的目标。

**延伸思考**
"10x vs 10%"是一个被低估的决策框架。它揭示了一个反直觉的真理：**宏大目标往往比小目标更容易实现**，不是因为目标本身简单，而是因为它迫使你**重新定义问题结构**。10% 的改进可以在现有框架内优化；10x 的改进则要求你跳出框架。这是 OpenAI、DeepMind、Biohub 这类机构在战略选择上的共同特征。

**精华收获**
- AI 已进入临床——但"加速"需要拆解到具体环节。**不要问"AI 何时进临床"，而要问"AI 在哪个环节能带来 10x"。**
- **10x 思维不是为了追求难度，而是为了获得视野。** 当 10% 的路径走不通时，把问题重新表述为 10x 目标。
- 宏大使命（如"治愈所有疾病"）不是营销口号，而是**方法论**——它迫使你寻找不同的路径。


## 精华收获

**1. 关于 AI 叙事的清醒剂**
"X 已被解决"几乎总是误导性的。真正的科学问题往往由**分布、动力学、上下文依赖性**组成，而 AI 通常只捕捉了其中一个切片。学会追问："被解决的是哪个子问题？剩下的是什么？"

**2. 数据哲学**
- Scaling law 不是被发现的，而是被**创造**的——它需要研究人员找到正确的数据-算力-架构组合。
- "脏数据"（如宏基因组序列）可能因为覆盖了进化的真实分布而优于"精炼数据"。
- 数据偏见的根源是**团队结构**——只有建模者会偏向现成数据，只有数据生成者会偏向易生成数据。解决方案是**全过程开放协作**。

**3. 方法论优先于身份**
"我是建模者/数据科学家"是宗教式思维。**问题优先，方案灵活。** 同一方法论在 AlphaFold 上得出了"建模优先"的结论，在虚拟细胞上得出了"数据优先"的结论——这正是健康的科学方法。

**4. 模型设计的权衡曲线**
- 归纳偏置（来自领域先验）→ 数据效率提升，但可能在数据量大时成为枷锁。
- Scale 本身是一门手艺——不是按按钮，而是架构创新 + 数据选择 + 稳定性工程。

**5. 下一个前沿**
- **回到源头**：直接建模冷冻电镜图像，而非依赖 PDB 的静态结构。
- **粒度升级**：从"轮辐模型"到"车轮模型"再到"整辆自行车模型"。用户的真实需求恰好在更高粒度。
- **可解释性作为关系概念**：对谁可解释？人类还是更大的 AI？行为表征比机制解释更紧急。

**6. 10x 思维**
宏大目标不是野心，而是**方法论工具**。它迫使你放弃局部优化，重新从第一性原理设计路径。这适用于科学研究、创业战略和个人职业选择。


<!-- TLDR: AlphaFold 解决的是 PDB 复现任务，而非蛋白质动力学——真正的科学才刚开始。 -->
<!-- TAGS: AI for Science, 蛋白质折叠, AlphaFold, 数据规模化, 可解释性 -->
<!-- RATING: 4 -->
