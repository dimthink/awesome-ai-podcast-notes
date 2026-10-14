---
title: "Robots That Predict the Future: Dyna-2 & Physical AI — Jason Ma, Dyna Robotics"
channel: "Latent Space"
published: "2026-10-13"
source_url: "https://www.youtube.com/watch?v=BHiYomkfoGQ"
video_id: "BHiYomkfoGQ"
tags: ["机器人", "世界模型", "物理AI", "强化学习", "创业"]
rating: 5
language: "英文"
word_count: 35902
duration: "1:21:06"
---

# Robots That Predict the Future: Dyna-2 & Physical AI — Jason Ma, Dyna Robotics

- **Channel:** Latent Space
- **Published:** 2026-10-13
- **Source:** https://www.youtube.com/watch?v=BHiYomkfoGQ
- **TL;DR:** 世界动作模型让机器人先预测未来再行动，用百万小时人类数据+少量机器人数据，实现真机多地点部署。
- **Tags:** 机器人, 世界模型, 物理AI, 强化学习, 创业
- **Rating:** 5

## 版本

- [结构化文稿](2026-10-13-robots-that-predict-the-future-dyna-2-&-physical-ai-—-jason-ma,-dyna-robotics-BHiYomkfoGQ.structured.md)
- [原始文稿](2026-10-13-robots-that-predict-the-future-dyna-2-&-physical-ai-—-jason-ma,-dyna-robotics-BHiYomkfoGQ.transcript.md)

# 能预测未来的机器人：Dyna-2 与物理 AI 的破晓时刻

**材料信息**

- **标题**：Robots That Predict the Future: Dyna-2 & Physical AI — Jason Ma, Dyna Robotics
- **作者/来源**：Latent Space 播客（主持人：swyx & Alessio）；嘉宾：Jason Ma（Dyna Robotics 联合创始人兼首席科学家）
- **类型**：YouTube 视频字幕（播客访谈 + 现场演示 B-roll 解说）
- **关键元数据**：Dyna Robotics 创立于 2024 年底；Dyna-2 世界动作模型训练数据超过 100 万小时；机器人已部署数十台，明年目标数百台；视频含现场演示（叠毛巾、洗衣全流程、取饮料、切食物等）

---

## 开篇引入

如果你关注机器人领域，你一定见过那些令人窒息的人形机器人视频：后空翻、跳舞、打拳击——然后在一个不起眼的台阶前摔倒。这些演示很酷，但它们掩盖了一个残酷的事实：**从“能在实验室做一次”到“能在真实商业场景中每天重复一万次并且创造价值”，中间隔着一道巨大的鸿沟。**

Jason Ma 和他的团队 Dyna Robotics 正在跨越这道鸿沟。这位宾夕法尼亚大学博士、前 NVIDIA 和 Google DeepMind 研究员，选择了一条与大多数同行截然不同的路线：不做炫技的人形机器人，而是做“半人形”实用机器人；不追求一次性 demo，而是让机器人真正在高档餐厅折叠数千张餐巾、在酒店洗衣房完成全流程洗衣工作。

他们的核心技术武器是**世界动作模型（World Action Model）**——一个能“预测未来”的 AI 系统。这个概念听起来很科幻，但本质上它做的事情非常朴素：像人类大脑一样，在行动之前先想象“如果我这样做，世界会变成什么样”，然后用这个想象来指导行动。

这篇深度重构将带你走进 Dyna Robotics 的技术内核、商业逻辑和哲学思考。从扩散 Transformer 到流匹配，从自我中心数据到合成环境生成，从机器人硬件设计到公司文化——无论你是 AI 研究者、创业者，还是单纯对物理 AI 的未来感到好奇，这个访谈都提供了极其丰富的第一手洞察。

---

## 一、世界动作模型：让机器人在“想象”中行动

### [00:05:00-00:12:00 / 访谈核心段落]

**核心观点**

Dyna-2 是首个在超过 100 万小时数据上训练的世界动作模型。它不仅能预测未来的视频画面（世界模型），还能基于这个预测生成机器人可执行的动作指令（动作模型）。这种架构让机器人更灵巧、更鲁棒、更能泛化到从未见过的场景。

**深度阐述**

Jason Ma 在访谈中详细拆解了世界动作模型的输入输出和运作原理。这个模型的核心理念来自于对人类认知的深刻观察：

**重要原话**：“If you think about how humans act in the physical world in our brain, we are implicitly thinking about how the world will evolve based on our actions. So now we have a model architecture that's able to do that to guide robot actions.” `[约 06:00]`
（中文翻译：如果你想想人类在物理世界中是如何行动的，我们的大脑其实在隐式地思考——基于我们的行动，世界会如何演变。所以现在我们有了一个能做这件事的模型架构，来指导机器人的动作。）

**输入层面**，模型接收三类信息：
1. **视觉输入**：机器人摄像头捕捉的视频或图像，涵盖过去数秒的画面
2. **本体感知输入**：机器人各关节编码器提供的关节角度数据（这是与纯视频模型的关键区别——机器人“知道自己身体的姿态”）
3. **语言指令**：用自然语言告诉机器人要做什么任务

**输出层面**，模型产生两类结果：
1. **动作指令**：机器人硬件可以执行的精确控制信号
2. **未来视频预测**：对未来世界状态的视觉预测

这里的关键洞察是：模型**先生成对未来世界的预测，然后用这个预测来指导动作生成**。Jason 把这种方式类比为语言模型中的“思维链”（Chain of Thought）——只不过这里机器人是在“视觉和物理空间中进行推理”，而非在文本空间中。

用更通俗的话说：传统机器人模型像是“条件反射”——看到什么就直接做什么；而世界动作模型像是在“脑内模拟”——先想象“如果我伸手去拿这个杯子，杯子会怎样移动，我的手会怎样变化”，然后再执行动作。这种“先想后做”的架构，让机器人的行为更加灵巧、鲁棒，并且能泛化到从未见过的环境和场景。

Jason 强调，这种“先预测后行动”的架构带来的提升是显著的：“the model is much more dextrous, much more robust and much more capable of generalizing to environments to scenarios is never seen before.” `[约 07:30]`

**延伸思考**

这个架构引发了一个深刻的哲学问题：**预测能力是否就是智能的核心？** 在认知科学中，“预测编码”（Predictive Coding）理论认为大脑本质上是一台预测机器——我们感知世界的方式，就是不断生成对感官输入的预测，并将预测误差最小化。Jason 的设计思路与此高度吻合。如果这一理论正确，那么世界模型可能不仅仅是机器人技术的一条路径，而是通向通用物理智能的核心范式。

**精华收获**

- 世界动作模型 = 世界模型（预测未来）+ 动作模型（生成控制），二者合一
- 核心优势：灵巧性、鲁棒性、泛化能力
- 类比：这是机器人在物理空间中的“思维链推理”
- 关键区别：输入不仅包括视频，还包括机器人自身的关节状态——机器人有“本体感知”

---

## 二、架构选择：扩散 Transformer 与流匹配

### [00:12:00-00:18:00 / 技术架构深度剖析]

**核心观点**

Dyna-2 底层采用扩散 Transformer（Diffusion Transformer）架构。Transformer 负责从海量数据中学习，扩散机制负责生成平滑、精确的动作输出。流匹配（Flow Matching）作为扩散的简化变体，大幅降低了调参难度，同时保持生成质量。

**深度阐述**

当主持人问到“如何从零开始构建一个机器人模型”时，Jason 给出了非常清晰的心智框架：**两个核心问题——数据，以及如何让模型从数据中学到尽可能多。**

**为什么是 Transformer？** Jason 解释说，Transformer 是当前唯一能“摄入最大量数据并进行学习”的架构。这与语言模型的逻辑一致——序列到序列的 decoder-only 架构。但机器人领域的特殊之处在于，视觉域（图像生成、视频生成、图像到动作的映射）中，扩散架构表现出色。

**重要原话**：“A diffusion model is a model that takes some random noise and through iterative computation can go from noise to something that's really high-dimensional, something really highly defined and have very fine-grain feature.” `[约 14:00]`
（中文翻译：扩散模型是一种从随机噪声出发，通过迭代计算，从噪声逐步生成非常高维、非常精细、具有极细微特征的东西的模型。）

Jason 用生成图像来类比：生成图像时需要锐利的边缘、清晰的角落、鲜明的色彩对比；生成机器人动作时，同样需要非常精确、非常平滑的控制信号。**从第一性原理出发，整个领域——不仅仅他们一家——都在使用扩散 Transformer 架构来训练机器人基础模型。**

**Transformer + Diffusion 的分工**：
- Transformer：负责摄入最大量的数据并从中学习（知识容量）
- Diffusion：负责将粗糙的输出逐步精炼为平滑、精确、细粒度的运动（输出质量）

**流匹配的角色**：主持人提到流匹配本质上是一个效率加速器——将传统扩散的 40-100 步推理压缩到 4 步。Jason 确认了这一点，并补充了更深层的优势：流匹配是扩散的一个特例，它让从噪声到输出的变换变得**更简单、更容易调参**。

**重要原话**：“Flow matching is kind of like a special case of diffusion that makes the transformation much simpler. In practice, you don't have to tune as much and it works just as well.” `[约 16:30]`
（中文翻译：流匹配是扩散的一个特例，它让变换过程简单得多。在实践中，你不需要调那么多参数，效果却一样好。）

Jason 指出，过去两三年，图像和视频生成领域已经从扩散模型大规模转向流匹配。概念本质相同，但流匹配是“更容易调参的简化变体”。

**一个有趣的对比**：主持人提出了一个敏锐的观察——流匹配在图像生成中可能有质量权衡（一次性生成，无法修正），但在机器人动作生成中特别适合，因为**你可以实时重新评估**。Jason 确认了这一观点。这意味着机器人领域的扩散/流匹配应用可能比图像生成领域更有优势——因为物理世界提供了一个天然的“反馈循环”。

**视觉/结构信息描述**：访谈中提到 Dyna-2 的博客文章有详细的架构说明，包括扩散 Transformer 的结构、流匹配的训练细节，以及模型如何从噪声逐步生成动作序列的可视化。主持人提到在播客中曾覆盖过流匹配话题，说明这是一个在 AI 工程社区中逐渐主流化的技术。

**延伸思考**

扩散模型与流匹配的关系，类似物理学中“复杂系统”与“简化模型”的关系。这体现了工程学的一个永恒智慧：**当一个方法过于复杂难以驾驭时，找到它的一个更简单但等价的特殊情形，往往是突破的关键。** 这让我想到深度学习中的许多进展——ReLU 简化了 sigmoid，Adam 简化了二阶优化，LoRA 简化了全参数微调。简化不是妥协，而是让技术真正可用的必要步骤。

**精华收获**

- 架构 = Transformer（学习能力）+ Diffusion（生成质量）
- 流匹配 = 扩散的简化变体，调参更少，效果相当
- 机器人场景天然适合扩散/流匹配：可实时重新评估
- 整个机器人基础模型领域正在收敛到这一架构

---

## 三、数据策略：没有互联网的机器人世界

### [00:18:00-00:28:00 / 数据问题深度讨论]

**核心观点**

机器人领域没有“互联网”这样现成的大规模数据集。数据是当前最重要的瓶颈。Dyna 的策略是：用大规模人类自我中心数据预训练，用少量机器人数据微调。数据质量是一个“非平稳问题”——随着模型能力变化，什么算“好数据”也在变化。

**深度阐述**

这是整个访谈中最有信息密度的部分之一。Jason 对机器人数据问题的分析极其透彻，值得完整展开。

**机器人数据的根本困境**：

**重要原话**：“Unlike language model, there is no internet, right? So every company that's building model, building hardware has to think about data.” `[约 19:00]`
（中文翻译：与语言模型不同，机器人领域没有“互联网”。所以每一家构建模型、构建硬件的公司都必须思考数据问题。）

Jason 用了一个精彩的类比：**试图靠单个公司收集的数据来构建机器人基础模型，就像试图只靠 Reddit 或只靠 Facebook 来构建整个互联网。** 它们是很棒的网站，有很多用户，但远远不够。

**数据来源的层级**：
1. **自采数据**：Dyna 在办公室部署了大量机器人，员工日常操作收集数据
2. **购买数据**：从数据供应商处获取
3. **公开数据**：利用已有的数据集

**什么是好数据？Jason 的核心回答**：

**最重要的一类**：人类执行任务的**自我中心（egocentric）数据**。Jason 解释说，人类数据极其多样——它覆盖了你所能想象的一切物理活动——这给机器人模型一个非常强的先验（prior），关于“世界如何围绕一个具身行动者演变”。

**但人类数据有 gap**：在机器人外形完全像人类之前，人类动作和机器人动作之间存在差距。单纯训练人类数据，不太可能直接执行机器人动作。所以还需要机器人自身数据的适配。

**Dyna 的数据配方**：
- 用最大规模的数据源（自我中心人类数据）给模型一个强大的基础
- 结合少量机器人数据，让机器人掌握特定任务

**数据质量的非平稳性**：

**重要原话**：“Data quality in robotics is a non-stationary problem in the sense that what is high quality data for your model changes over time. When your model doesn't know anything, when it's zero, any data is useful.” `[约 21:00]`
（中文翻译：机器人领域的数据质量是一个非平稳问题——对你模型而言什么是高质量数据，会随时间变化。当模型什么都不知道的时候，任何数据都有用。）

这是一个极其深刻的洞察。在语言模型领域，数据质量的判断相对稳定（语法正确、逻辑通顺、信息丰富）。但在机器人领域，随着模型能力提升，“什么样的数据最有价值”会不断变化。这要求数据策略必须是动态的、迭代的。

**数据合作伙伴招募**：Jason 在访谈中直接发出了“数据征集令”——Dyna-2 博客末尾有 data partnerships 邮箱（data partnerships at dyna.co），欢迎拥有高质量自我中心数据、机器人数据、视频数据的供应商联系。

**人类数据的局限与机器人数据的必要性**：Jason 强调，机器人自身数据收集更昂贵、更难，但必不可少。最终的配方是：**人类数据覆盖高层认知和物理操作的一般规律，机器人数据覆盖低层反射和灵巧操作。**

**关于定制数据的价值**：Jason 用了一个生动的类比——

**重要原话**：“If Sean or me go work at Rosewood Hotel tomorrow, we're not going to be able to make the bed the way they want. We need a lot of training. So that kind of data, special data, it's kind of like what Mercor is doing today for language model, I think will be very very valuable for robotics as well.” `[约 26:00]`
（中文翻译：如果 Sean（主持人）或我明天去 Rosewood 酒店工作，我们没法按他们要求的方式铺床。我们需要大量训练。所以那种特殊数据——就像 Mercor 今天为语言模型做的那样——我认为对机器人也会非常有价值。）

**视觉/结构信息描述**：访谈中描述了 Dyna 办公室的场景——到处都是机器人，员工在日常工作中收集数据。有一个有趣的细节：他们有一个“面试任务”——让应聘的工程师选一个任务，现场收集数据训练模型，看效果。切食物任务花了 45 分钟数据，开冰箱任务是某位工程师的入职任务。

**延伸思考**

数据问题揭示了机器人与语言模型的一个根本差异：**语言是人类已经数字化了数千年的产物，而物理操作从未被大规模数字化。** 这意味着机器人领域可能需要创造全新的数据基础设施——从可穿戴传感器到远程操作系统到合成数据生成。谁解决了数据问题，谁就解决了机器人问题。这也解释了为什么 Jason 如此看重“真机部署”——因为部署不仅是商业行为，更是数据收集行为。每一台在客户现场运行的机器人，都是一个数据采集终端。

**精华收获**

- 机器人没有“互联网”，数据必须从零构建
- 最佳预训练数据：人类自我中心数据（多样性极强）
- 最佳微调数据：机器人自身数据（弥合 embodiment gap）
- 数据质量是非平稳问题——随模型能力变化
- 真机部署 = 商业验证 + 数据收集，双重价值

---

## 四、合成数据与模拟：下一个前沿

### [00:28:00-00:34:00 / 模拟与合成数据讨论]

**核心观点**

合成环境生成和模拟数据是机器人领域的下一个前沿。前沿模型的视觉能力已经达到“临界点”——能进行真实到模拟的 CAD 转换、3D 重建。Dyna 同时探索两条路径：用前沿模型生成合成环境，以及用自己的世界模型生成训练数据（自我飞轮）。

**深度阐述**

Jason 在这部分分享了他个人研究历程中一个非常有趣的“回归”——他在博士期间就专注于基于模拟的机器人训练，当时模拟技术还不成熟，但他做了一个叫 Eureka 的项目，首次用大语言模型（当时是 GPT-4）来自我生成环境、生成强化学习的奖励函数。

**重要原话**：“Back then the model didn't really have good vision capability, didn't have innate 3D understanding. So it was basically just generating code and using very limited feedback from text to try to come up with new simulation environments. But today, the vision capability of these frontier models are crazy.” `[约 30:00]`
（中文翻译：当时模型没有好的视觉能力，没有内在的 3D 理解。所以基本上只是生成代码，用非常有限的文本反馈来尝试创造新的模拟环境。但今天，这些前沿模型的视觉能力简直疯狂。）

Jason 认为现在到了一个**临界点（tipping point）**：前沿模型可以做真实到模拟的 CAD 转换、3D 重建，这项技术可以真正加速机器人研发。

**Dyna 的两条合成数据路径**：

1. **用前沿模型生成合成环境**：为 Dyna 关心的环境和数据生成定制化的模拟场景
2. **用自己的世界动作模型生成训练数据**：因为世界动作模型不仅能生成动作，还能生成视频，所以模型可以生成自己的训练数据——形成一个**自我飞轮（self-fulfilling flywheel）**

**重要原话**：“The model can also generate its own training data. So that becomes a self-fulfilling flywheel that I think will also be powerful.” `[约 32:00]`
（中文翻译：模型也能生成自己的训练数据。所以这就变成了一个自我实现的飞轮，我认为这也会非常强大。）

**Eureka 项目的回忆**：Jason 提到他博士期间最自豪的 demo 之一——机器人转铅笔。当时这个 demo 很酷，但非常有限，因为模型没有视觉能力，没有 3D 理解。而今天，同样的思路（用 AI 生成模拟环境和奖励函数）因为前沿模型视觉能力的飞跃而变得真正可行。

**延伸思考**

合成数据与真实数据的辩证关系值得深思。在语言模型领域，合成数据已经被证明可以显著提升模型能力（如“教科书质量”的合成数据）。在机器人领域，合成数据的挑战更大——因为物理世界的“真实性”要求更高。但 Jason 的洞察是：**当生成模型本身足够强大时，它生成的“想象数据”可以反过来训练更好的模型。** 这形成了一个正反馈循环，可能是通向更高级机器人智能的关键路径。这也引出一个问题：如果世界模型足够好，我们是否还需要那么多真实数据？或者说，真实数据的价值是否会从“训练信号”转变为“验证信号”？

**精华收获**

- 合成数据是机器人 scaling 的新维度
- 前沿模型的视觉能力已达临界点，使 real-to-sim 真正可行
- 世界动作模型可以生成自己的训练数据——自我飞轮
- Jason 博士期间的 Eureka 项目思路在今天终于成熟

---

## 五、硬件哲学：半人形、轮式底座与执行器自研

### [00:34:00-00:48:00 / 硬件设计与供应链讨论]

**核心观点**

Dyna 选择“半人形”（上半身人形 + 轮式底座）而非全人形。核心逻辑：腿部能耗高、稳定性差、安全性难保证；轮式在实用性和性能之间取得更优平衡。Dyna 自研执行器，因为执行器的质量直接决定机器人建模的精度。硬件迭代必须采取渐进式策略，而非一步到位。

**深度阐述**

这部分是访谈中最具工程实践价值的内容之一，Jason 详细解释了 Dyna 的硬件设计决策。

**为什么是半人形？**

Dyna 的机器人上半身与人形一致——有肩膀、手臂，**腰部还有 4 个自由度**，可以完成人类上半身的所有动作。但下半身是轮子。

**重要原话**：“With legs the energy consumption will be a lot higher. You'll be a lot more unstable. Safety will be extremely extremely hard to guarantee. Right now for legged robots, there's actually no guarantee that the robot will stay upright, balanced the entire time.” `[约 40:00]`
（中文翻译：用腿的话，能耗会高很多，会不稳定得多，安全性将极其难以保证。目前对于足式机器人，实际上没有保证机器人能始终保持直立和平衡。）

Jason 对当前人形机器人演示的批评很直接：那些跳舞视频中的机器人很容易摔倒。即使有些 demo 展示了很好的平衡能力（可以推、可以打），那也只是“平衡能力好”，不代表能完成实际工作任务。

**腰部的 4 个自由度——一个精彩的设计洞察**：

Jason 用了一个非常个人化、非常生动的故事来解释为什么腰部自由度如此重要：

**重要原话**：“A couple years ago when I was exercising I accidentally pulled a muscle. Then the next few days you just couldn't move. We have all experienced that. Whenever you experience that you kind of realize wow, so many muscles, so many degrees of freedom that we use in our daily life that we take for granted.” `[约 42:00]`
（中文翻译：几年前我锻炼时不小心拉伤了肌肉。接下来几天你就是动不了。我们都经历过。每当你经历这个，你就会意识到——哇，我们在日常生活中使用了那么多肌肉、那么多自由度，而我们习以为常。）

Jason 进一步解释：人类在日常活动中大量使用腰部和躯干——即使只是拿一个瓶子，你也不是只动手臂，而是自然地转动身体。如果机器人只有一个上下升降的轴（如他们的 Mewtwo 原型），很多人类躯干运动就无法复现。而因为 Dyna 是用人类数据预训练的，**如果硬件形态不允许这些动作，迁移效果就会变差，机器人就会显得笨拙。**

**自研 vs 采购的决策逻辑**：

Jason 给出了非常清晰的原则：

**重要原话**：“If the input output of a component is very very clear and there's already extremely good mature solution, then there's no point to building it ourselves.” `[约 44:00]`
（中文翻译：如果一个组件的输入输出非常清晰，而且已经有极其优秀的成熟解决方案，那就没有理由自己造。）

- **不自研**：激光雷达（LiDAR）——成熟技术，已用于自动驾驶数十年；部分摄像头
- **自研**：执行器（actuator）——因为执行器的质量和设计直接决定机器人建模的精度。“Actuator is what drives the robot. To be able to model your robot very well in simulation, you need to select actuators that are very good, that can be easily modelable.”
- **自研**：机器人的比例——Dyna 的机器人比例是**对照真人测量**的，因为他们在人类数据上预训练，最佳迁移要求形态匹配。

**供应链的现实**：

主持人提出了一个尖锐的问题——美国不生产磁铁，只有两个国家生产（涉及稀土材料）。Jason 的回应非常坦诚：

**重要原话**：“Even now there isn't a company in the US that's truly building everything from scratch in the US. Even when they say they assemble robot in the US, they're still sourcing the raw materials from other places in the world.” `[约 47:00]`
（中文翻译：即使是现在，美国也没有一家公司真正从零开始在美国制造一切。即使他们说在美国组装机器人，他们仍然从世界其他地方采购原材料。）

Jason 强调，作为全栈机器人公司，他们深刻意识到供应链有多长、整个问题有多难。他认为，当前行业讨论过度集中在模型和数据上，而**硬件和构建好硬件的难度被严重低估了**。

**为什么必须全栈？**

Jason 分享了他之前在 DeepMind 和 NVIDIA 的经历——只做模型，不控制硬件，他看到了系统的上限。

**重要原话**：“I saw the upper bound of the system when you don't control the hardware, when you don't get to optimize that. If you want to solve physical tasks, you want to be able to optimize everything.” `[约 48:00]`
（中文翻译：当你不控制硬件、无法优化硬件时，我看到了系统的上限。如果你想解决物理任务，你需要能够优化一切。）

**渐进式硬件迭代哲学**：

**重要原话**：“The best way to actually build a human robot is to take an iterative approach. Hardware decision is much more expensive, much more costly, hardware iteration is a lot slower. You actually want to take an incremental iterative approach, not going all the way to the final form factor.” `[约 56:00]`
（中文翻译：真正构建人形机器人的最佳方式是采取迭代方法。硬件决策昂贵得多，硬件迭代慢得多。你实际上想采取渐进式迭代方法，而不是一路做到最终形态。）

Jason 引用了 Optimus 的例子——已经经历了多次迭代，不得不废弃一些设计。他认为，通过半人形形态先部署到真实客户，获取反馈循环，比花 5-10 年直接造一个完美人形机器人要更快接近最终目标。

**视觉/结构信息描述**：访谈中展示了 Dyna 的两代硬件——Mewtwo 原型（只有上下升降轴）和当前的新机器人（有腰部 4 自由度，可以倾斜、转动）。主持人特别提到，这是他们见过的**最平滑的机器人**——“每个你见过的人形机器人都是卡顿的，甚至人类走路都没有这么平滑。” Jason 解释，这是因为模型可以同时控制每一个电机，动作空间约 100 维，模型以每秒 10-20 次的频率输出 50 维以上的连续向量。

**延伸思考**

Dyna 的硬件哲学体现了一个更广泛的产品设计原则：**形态追随功能，而非追随形式。** 人形机器人的终极形态可能是人形，但通往人形的路径不一定是人形。这就像电动汽车的演进——早期电动车不是直接取代燃油车的所有功能，而是从特定场景（城市通勤）切入，逐步扩展。Dyna 的半人形 + 轮式方案，本质上是在“人类数据可迁移性”和“工程可行性”之间找到的最优平衡点。

另一个值得深思的点是：**硬件形态决定了数据策略的有效性。** Dyna 先决定用人类数据预训练，然后反推硬件应该长什么样（对照真人测量比例）。这种“数据优先”的硬件设计思路，与传统“硬件优先”的机器人公司形成鲜明对比。

**精华收获**

- 半人形 = 上半身人形（含腰部 4 自由度）+ 轮式底座
- 腰部自由度至关重要：人类大量使用躯干运动，硬件必须匹配
- 自研执行器：建模精度要求执行器“可建模”
- 供应链现实：美国没有公司能完全从零制造，供应链极长
- 全栈必要性：不控制硬件就看到系统上限
- 渐进式迭代 > 一步到位

---

## 六、部署与商业化：从餐巾折叠到洗衣全流程

### [00:48:00-01:02:00 / 客户案例与部署讨论]

**核心观点**

Dyna 的最大规模化客户是 Dentyon（高档餐厅），机器人每天折叠数千张餐巾，精度要求极高。真正的难点不是“在一个地点部署”或“做 pilot”，而是**客户相信你的机器人创造了足够价值，愿意在多个地点部署**。Dyna 已经实现了这一点，这是与其他通用机器人公司的关键区别。

**深度阐述**

主持人参观了 Dyna 的办公室，看到了大量 B-roll 素材——机器人拉饮料、使用刀具（第一次）、折叠衣物等。但 Jason 强调，真正的成就是商业化部署。

**重要原话**：“What's really hard is not putting your robot in one location or doing a pilot. What's really hard is that the customers believe or validate that your robot creates enough value that they want to deploy your robots across many of their sites. That's what's happened for us with Dentyon, which to the best of my knowledge hasn't really happened for other companies doing similar general purpose robots.” `[约 50:00]`
（中文翻译：真正难的不是把机器人放到一个地点或做个试点。真正难的是客户相信或验证你的机器人创造了足够价值，以至于他们想在多个地点部署你的机器人。这就是 Dentyon 发生在我们身上的事——据我所知，其他做类似通用机器人的公司还没有真正做到这一点。）

**Dentyon 案例细节**：
- 高档餐厅（如 Dentyon 等），桌上放餐巾
- Dyna 的机器人每天折叠数千张餐巾，服务美国多个地点
- **质量要求极高**：餐巾的第二道折缝只能在口袋下方几厘米——非常精细的高精度操作
- 人类员工在不同地点（LA、纽约、西雅图）折出的餐巾风格不同，但客户想要一致性——**这正是模型的优势**：一套权重可以部署到所有机器人，OTA 更新，保证一致性
- 机器人速度已达“人类水平”（human parity），且不会疲劳

**为什么通用机器人能做好折叠餐巾这种“专用任务”？**

**重要原话**：“The hard thing about manipulating deformable objects—napkin, towels, everything is deformable—there just infinitely many possible configurations. That's really hard for a specialized robot. By developing a general purpose model and adapting it to these use cases, you can actually get to production quality faster.” `[约 53:00]`
（中文翻译：操作可变形物体的难点在于——餐巾、毛巾，一切都是可变的——存在无限多种可能的构型。这对专用机器人来说非常困难。通过开发通用模型并适配到这些用例，你实际上可以更快达到生产质量。）

这是“机器人领域的苦涩教训”的一个具体体现：**专用机器人需要为每一种构型设计规则，而通用模型可以从数据中学习处理无限构型。**

**Dentyon 的扩展**：Jason 透露，Dentyon 已经签署了更大的合同，不仅想要折餐巾，还想要切食物——这就是为什么访谈中有切食物的演示。

**Best Western 案例**：酒店行业客户，Dyna 的机器人折叠大量毛巾/布草。每个酒店、每个健身房、每个健身中心都需要。

**主机人的“最终 Boss”玩笑**：主持人开玩笑说最终 Boss 是 Cheesecake Factory——因为他们要求所有地点、所有酱料完全一致，精确到克。这恰恰是机器人的优势。

**重要原话**：“One issue with Dentyon is their LA location, New York location, Seattle location—the folded napkin looks different. But from their perspective they want consistency. That's exactly what these models are good at because models are just a set of weights you can put the weights in different robots across the country, OTA update them as well.” `[约 55:00]`
（中文翻译：Dentyon 的一个问题是他们的洛杉矶、纽约、西雅图地点折出的餐巾看起来不同。但从他们的角度，他们想要一致性。这正是这些模型擅长的，因为模型只是一组权重，你可以把权重放到全国不同的机器人上，也可以 OTA 更新它们。）

**洗衣全流程演示（视频后半段）**：

访谈最后展示了 Dyna 2.1 的完整洗衣工作流程 Demo，这是机器人首次作为“完整员工”完成整个工作流：

1. **从洗衣机转移毛巾到烘干机**：机器人需要大幅移动身体，把手臂伸进洗衣机抓取所有毛巾，**不能碰到门**——极其困难，需要灵巧性和平滑运动。因为是单一模型控制每个关节，没有经典规划与执行的分离，所以运动非常平滑。

2. **处理掉落毛巾**：演示中故意掉落一条毛巾，机器人能识别掉落，捡起来，并且**意识到毛巾变脏了**，把它放进脏衣篮。

3. **关闭烘干机门并启动**：机器人需要转动旋钮（“像人类一样操作机器”）、选择正确的烘干模式、按下启动按钮。这里有一个技术细节——LED 屏幕会闪烁，所以机器人需要理解**数字帧的时序**，知道烘干机何时真正启动。

4. **完整工作流**：折叠、堆叠、转移、篮子——全部完成。Dyna 2.1 是“机器人首次成为工作场所的完整员工”，不需要人类或其他机器喂料或帮忙。

**重要原话**：“Dyna 2.1 is about a robot for the first time becoming like a whole employee at a workplace doing everything. Historically we think about robots as machines, but this is for the first time I think we can really see robots working alongside humans to really improve physical productivity in the world.” `[约 59:00]`
（中文翻译：Dyna 2.1 是关于机器人首次成为工作场所的完整员工，做所有事情。历史上我们把机器人视为机器，但这是第一次我认为我们真正能看到机器人 alongside 人类工作，真正提高世界上的物理生产力。）

**取饮料演示**：
- 用户屏幕上选择饮料（如香草奶昔）
- 机器人收到指令，走到冰箱，用世界动作模型 Dyna 2 控制整个机器人，取出正确的饮料，导航回来交付
- **两层架构**：推理层（高级推理模型规划步骤）+ 动作层（世界动作模型执行灵巧操作）
- 机器人需要“可操控”（steerable）——告诉它选六种饮料中的哪一种
- 视频动作模型帮助“想象”理解意图——想象机器人抓取饮料会是什么样
- 需要识别人类何时抓住饮料，精确时机释放——不能误判，不能把饮料掉地上

**延伸思考**

Dyna 的商业化路径揭示了一个反直觉的真理：**最难的商业化不是技术，而是信任。** 客户愿意在多个地点部署，意味着他们不仅验证了技术可行性，还验证了经济价值。这需要机器人创造的价值超过其成本（包括维护、监督、部署成本）。Jason 强调 Dentyon 案例的独特性，暗示许多机器人公司停留在 pilot 阶段——客户觉得“有趣，但不值得扩大部署”。这是机器人商业化最真实的门槛。

另一个洞察是：**可变形物体操作是通用机器人的“杀手级应用”。** 餐巾、毛巾、衣物——这些在传统工业机器人眼中是噩梦（无限构型），但通用模型可以处理。这可能是通用机器人相对于专用机器人的第一个明确优势领域。

**精华收获**

- 真正的商业化 = 客户愿意多地点部署，而非单点 pilot
- Dentyon（餐巾折叠）是最大规模化客户，质量要求极高
- 通用模型优势：处理可变形物体的无限构型
- 一致性是机器人 vs 人类的关键优势（OTA 统一更新）
- 洗衣全流程 = 机器人首次作为“完整员工”
- 两层架构：推理层（规划）+ 动作层（执行）

---

## 七、评估与迭代：机器人版的 RLHF

### [01:02:00-01:10:00 / 评估流程讨论]

**核心观点**

学习新任务的流程：收集少量机器人数据（数十分钟到数小时）→ 训练模型 → 真实世界部署 → 评估表现 → 收集更多数据迭代。这是“机器人版的 RLHF”。当前瓶颈：硬件（灵巧手不够耐用）和数据（缺乏触觉、听觉等多模态信息）。

**深度阐述**

主持人问到了非常实际的工程问题：如何评估、迭代、部署新任务？

**新任务学习流程**：

**重要原话**：“If we want to learn a new task, we basically do a little bit of robot data collection, then the model—like a couple hours. In some of the tasks, just tens of minutes. The chopping one was 45 minutes. The open the fridge was—that's like an onboarding task for one of your engineers.” `[约 62:00]`
（中文翻译：如果我们想学习一个新任务，我们基本上做少量机器人数据收集，然后模型——大概几个小时。有些任务只要几十分钟。切食物那个是 45 分钟。开冰箱那个——那是你们一个工程师的入职任务。）

**数据收集方式**：人类操作员远程遥控机器人执行任务一段时间，然后训练模型。

**评估方法**：
1. **训练阶段**：看模型是否收敛良好（常规 ML 指标）
2. **真实世界评估**：在数据收集的同一设置上运行模型，看表现
3. **有时模型开箱即用**：不需要更多工作
4. **当模型达到 70-80% 时**：观察模型行为，找出它不擅长的地方，收集更多数据，迭代

**重要原话**：“I think of this as the robotics version of reinforcement learning from human feedback. The robot rolls out, you can score it good, bad, somewhat good, and then that data—the robot's own experience—can be used to train the model.” `[约 64:00]`
（中文翻译：我把这个看作机器人版的 RLHF。机器人 rollout，你可以打分——好、坏、一般——然后这些数据，机器人自己的经验，可以用来训练模型。）

**新机器人 vs 旧机器人**：Dyna 的新机器人（有腰部自由度）数据量远少于固定臂机器人，但模型在预训练中没见过这个新形态，却能快速学习任务。Jason 将大部分功劳归于**在硬件准备好之前就承诺在人类数据上预训练**——因为知道机器人终将像人类，所以可以在硬件就绪时提前训练。

**当前任务的时间范围**：
- 洗衣 Demo 完整循环：**约 1 小时**
- 机器人能完成的最长完整工作：已经在小时级别

**瓶颈分析**：

**硬件瓶颈**：
- 设置空间等任务需要比平行夹爪更灵巧的手（如人类手）
- 但当前最好的灵巧手**不够耐用**，很快过热
- “你几乎需要放一个冰袋”
- 不能只做模型研究，还有硬件限制

**数据瓶颈**：
- 当前数据主要是视觉（视频流 + 手部运动编码）
- 人类有更多传感器：听觉、触觉、嗅觉
- 如果不捕捉这些，即使扩展到数百万小时，也可能**缺少关键维度**，永远无法解决某些任务
- 对于能用当前数据高保真收集的任务，没有根本性瓶颈
- 对于更通用的任务，最大瓶颈仍是硬件和数据

**延伸思考**

“机器人版 RLHF”这个概念值得深入。语言模型的 RLHF 依赖人类对文本输出的偏好评分，相对容易获得。机器人 RLHF 的挑战在于：**评分需要真实世界的 rollout，成本极高，且难以大规模并行。** 这可能是机器人领域需要创新的关键方向——如何低成本、高效率地获取机器人行为的偏好信号？也许可以通过世界模型在“想象”中评估，而不是每次都真实 rollout。这与世界动作模型的设计哲学形成闭环。

**精华收获**

- 新任务学习：数十分钟到数小时数据采集
- 迭代循环：部署 → 评估 → 找弱点 → 补数据
- 机器人版 RLHF： rollout 评分作为训练信号
- 当前瓶颈：灵巧手耐用性、多模态传感缺失
- 预训练先行：硬件未就绪时可先训练人类数据

---

## 八、智能体框架：不只是模型，而是系统

### [01:10:00-01:18:00 / Agentic Harness 讨论]

**核心观点**

Dyna 不只是构建模型，而是构建完整系统——包括围绕世界动作模型的**智能体框架（agentic harness）**。高层次推理（如“洗衣机在运行，我应该去做别的事”）由推理层处理，低层次灵巧操作由动作模型处理。这是分层架构，类似语言模型中的 agentic 系统。

**深度阐述**

主持人注意到取饮料 Demo 中有智能体规划（agentic planning）和两层架构，询问如何将模型输出包装成智能体框架。

**为什么需要智能体框架？**

**重要原话**：“For any real task, long task in the physical world, there's a lot of high-level decision-making you have to do. It's not just the robot only reasoning about the physical world in the action continuous trajectories—that's the low-level thing you're executing. When we are doing decision-making, we think about steps of a recipe. We think about—oh, I finished this, I need to do that, while I'm waiting for this part to finish I need to go somewhere else to do something else.” `[约 72:00]`
（中文翻译：对于任何真实任务、物理世界中的长任务，你需要做很多高层决策。不仅仅是机器人在动作连续轨迹中推理物理世界——那是低层执行。当我们做决策时，我们思考食谱的步骤。我们思考——哦，我完成了这个，我需要做那个，在等待这部分完成时我需要去别的地方做别的事。）

**具体例子**：洗衣任务中，机器人需要推理“洗衣机在运行，所以我应该去做别的事；现在洗衣机完成了，我应该立即把毛巾从洗衣机拿出来放进烘干机”——否则会成为整个工作流的瓶颈。

**为什么不用低层模型学习高层次推理？**

Jason 解释：理论上可以用低层动作模型学习这一切，但**极其低效**。分层系统允许模型组合不同能力、不同技能来解决更长时域的任务。

**类比语言模型**：
**重要原话**：“Two years ago, three years ago, the model was only good at autocomplete. Humans have to tap tap tap to get the model to keep spitting out code. But today, an agentic system just carries the end-to-end task. That's important because today in robotics people are still thinking about autonomy at the very task level—like a one minute 30 second task. But really the value is about tasks or workflows that go on unsupervised for hours.” `[约 74:00]`
（中文翻译：两三年前，模型只擅长自动补全。人类必须敲敲敲才能让模型继续输出代码。但今天，智能体系统可以端到端完成任务。这很重要，因为今天在机器人领域，人们仍然在非常任务级别思考自主性——像 1 分 30 秒的任务。但真正的价值在于**无监督运行数小时的任务或工作流**。）

**关键洞察**：Dyna 把机器人问题看作**系统问题**，而非单纯的建模问题。需要好的智能体、好的框架工程、好的模型、好的硬件——所有一切。

**语言模型编码工具的影响**：Jason 表示 Dyna 是极其 AI 原生的公司。编码智能体是工作的核心部分。每当有新模型发布，他们都是第一批测试者。GPT-6 发布时，他们同一周举办了公司黑客松，工程师构建的东西令人难以置信，很多功能已经进入生产环境。

**GPT-6 的惊喜**：Jason 认为最令人兴奋的是**构建虚拟环境、转化为模拟**的能力——正好与他们之前讨论的合成数据方向吻合。

**延伸思考**

分层智能体架构在机器人领域的必要性，揭示了一个更广泛的 AI 系统设计原则：**不同时间尺度需要不同抽象层次。** 低层动作需要毫秒级反应，高层规划可以秒级甚至分钟级。试图用一个模型端到端学习所有层次，不仅在计算上低效，在数据需求上也不可行。这与大脑的功能分区（小脑负责精细运动，前额叶负责规划）形成有趣对应。未来的机器人 AI 可能更像一个“认知架构”，而非单一模型。

**精华收获**

- 分层架构：推理层（高层规划）+ 动作层（灵巧执行）
- 智能体框架让模型组合技能，解决长时域任务
- 价值在“无监督运行数小时的工作流”，而非单次任务
- 机器人 = 系统问题，需要模型 + 硬件 + 智能体 + 框架工程
- 编码智能体加速机器人研发（GPT-6 黑客松）

---

## 九、行业格局与“机器人苦涩教训”

### [01:18:00-01:28:00 / 行业讨论]

**核心观点**

机器人领域的“苦涩教训”：算法保持简单，scale 对的数据，泛化行为会涌现。但机器人 scale 比语言模型难得多——没有互联网，必须自己构建硬件、选择传感器。Dyna 的差异化：全栈、人类数据 scaling、真机部署优先。

**深度阐述**

主持人提出了“机器人领域的苦涩教训”这个概念。

**Jason 的苦涩教训解读**：

**苦涩教训一**：机器人会像 ML 解决的其他领域一样 scale。尽可能多地获取数据。

**重要原话**：“What is the right data is much harder to figure out than other domains. In language, it's text. In video games, just video game data. But for robotics, what sensors you choose determine what kind of data you have.” `[约 80:00]`
（中文翻译：什么是正确的数据比其他领域难得多。语言是文本，视频游戏是游戏数据。但对于机器人，你选择什么传感器决定了你有什么数据。）

**苦涩教训二**：机器人领域有很多研究在提出非常具体的先验（priors）——比如“让机器人把物体看作物体的本来面目，画一些框，会给机器人更好的感知”。但苦涩教训是：**保持算法简单，scale 正确的数据，更好的泛化行为会涌现。**

**关键区别**：语言模型可以上网爬数据，机器人必须自己构建硬件、选择传感器、收集数据，**然后才能 scale**。这是机器人比语言模型难得多的原因。

**硬件迭代的哲学**（再次强调）：**最终极的通用机器人应该是人形**，因为世界是为人类建造的。但最佳构建方式是迭代式——因为机器人问题太难、全栈太长，硬件决策昂贵且迭代慢。

**重要原话**：“The best way to actually build a human robot is to take an iterative approach. By iterating with a semi-human form factor and actually putting them out to real customers, getting models really deployed, you get that feedback loop that you wouldn't get if you're just trying to build a warehouse humanoid and spend 5-10 years building it.” `[约 84:00]`
（中文翻译：真正构建人形机器人的最佳方式是迭代方法。通过半人形形态迭代，真正部署到真实客户，让模型真正部署，你获得反馈循环——如果你只是试图构建仓库人形机器人，花 5-10 年建造它，你不会有这个反馈循环。）

**行业格局**：

Jason 对同行表示尊重，认为有很多优秀公司在做前沿工作。当前有多种路径：
- **Dyna**：全栈、自研硬件、scaling 人类数据、真机部署
- **其他公司**：只做模型，部署到任何平台（如 Optimus）
- **其他公司**：scaling 机器人数据
- **其他公司**：构建中间数据收集设备

**重要原话**：“For people who are only working at one part of the problem, it's kind of like fog of war. You don't really see the whole picture and you might be building something that's extremely cool technologically but may not be what people need or want at the end. There's a whole graveyard of robotics companies, and all of them had very shiny, very cool robots, but figuring out what people actually want is actually very hard to execute.” `[约 86:00]`
（中文翻译：对于只在一个问题上工作的人，就像战争迷雾。你无法看到全貌，你可能在构建技术上极酷的东西，但最终可能不是人们需要或想要的。整个机器人公司墓地，所有公司都有非常闪亮、非常酷的机器人，但弄清楚人们真正想要什么，实际上非常难执行。）

**世界模型的技术路线差异**：

- **Dyna**：世界动作模型（World Action Model）——预测未来视频 + 动作
- **Runway 等**：视频世界模型适配机器人
- **其他公司**：视觉语言动作模型（VLA）——适配 VLM 到机器人

**为什么 Dyna 认为世界动作模型更好？**

**重要原话**：“Robotics is fundamentally about—based on the information you have at the present moment and before, what should you do next? It's about predicting what comes next. Robot is just a part of the world. Robot influences the world, but the world also influences how the robot should behave. The most first-principle thing you can do is predict as much of the world as you can possibly predict.” `[约 89:00]`
（中文翻译：机器人技术本质上关于——基于你当前和之前的信息，你下一步该做什么？这是关于预测下一步。机器人只是世界的一部分。机器人影响世界，但世界也影响机器人应该如何行动。最第一性原理的事情是预测尽可能多的世界。）

**VLA 的问题**：只预测机器人动作或世界的某种抽象表示。每当预测抽象表示时，你都在**编码自己对什么重要的偏见**。而苦涩教训告诉你：**去除人类偏见，用最原始的表示（相机输入），预测所有一切。**

**Jason 承认可能出错的地方**：

**重要原话**：“What that doesn't say is—does your sensor have everything about the world that you need to predict? If you train a world model that's purely based on videos, it may not be a sufficiently rich enough world model because you're missing critical aspects like sound, like touch.” `[约 92:00]`
（中文翻译：这没有说的是——你的传感器拥有你预测所需的世界的一切吗？如果你训练一个纯粹基于视频的世界模型，它可能不是足够丰富的世界模型，因为你缺少关键方面，比如声音、触觉。）

**可能的“错误”场景**：如果明天有人推出视觉 + 触觉世界模型，数据效率高 100 倍（因为视觉信息高度冗余，触觉信息密度更高），那么纯视觉世界模型可能不是终点。

**但 Jason 的自信来源**：如果触觉 + 视觉 + 听觉世界模型是最终解决方案，**机器人公司会比视频生成公司转型做机器人更有优势**——因为理解传感非常复杂，Dyna 从公司第一天就在构建这些，知道瓶颈在哪，知道如何组合。而视频模型公司如果纯视频不够，他们没有触觉的 know-how。

**延伸思考**

“苦涩教训”在机器人领域的应用引发了一个深刻问题：**机器人是否最终会像语言模型一样收敛到一个“scaling is all you need”的范式？** Jason 的回答是肯定的，但有一个关键前提——必须先解决“什么是正确数据”和“如何获取这些数据”。这暗示机器人领域的 scaling 可能不是简单的“更多数据”，而是“更多正确类型的数据”。传感器选择成为战略决策，而不仅仅是技术选择。这也解释了为什么 Dyna 如此重视全栈控制——只有控制硬件，才能控制传感器，才能控制数据。

**精华收获**

- 机器人苦涩教训：简单算法 + scale 正确数据 → 泛化涌现
- 机器人 scale 难度：没有互联网，必须自建硬件 + 传感器
- 世界动作模型 vs VLA：预测原始世界 vs 预测抽象表示
- 可能的错误：纯视觉世界模型不够丰富（缺少触觉、声音）
- 机器人公司的护城河：传感 know-how + 全栈控制

---

## 十、个人历程：从 AlphaGo 到 Dyna Robotics

### [01:28:00-01:38:00 / 个人背景讨论]

**核心观点**

Jason 的 AI 之路始于高中时目睹 AlphaGo 击败人类围棋冠军的震撼。宾大博士 → NVIDIA（Eureka 项目）→ Google DeepMind → 创立 Dyna。核心动机：不满足于学术研究“自己给自己打分”，想要真正影响数百万人的物理世界。

**深度阐述**

这部分是访谈中最具人文色彩的部分，Jason 首次详细分享了他的个人成长历程。

**AlphaGo 的震撼**：

**重要原话**：“As a kid, I spent time in Japan and China. I grew up playing Go. When AlphaGo came out, I was a senior in high school and I was mind-blown because I've been playing this game for many many years. It's so complicated. Before AlphaGo, people were like—Go is one of the games AI will never solve. The search space is larger than the total number of atoms in the world. Then RL just cracked it.” `[约 96:00]`
（中文翻译：小时候我在日本和中国待过。我从小下围棋。AlphaGo 出现时，我高三，我彻底震惊了，因为我玩这个游戏很多年了。它太复杂了。AlphaGo 之前，人们说——围棋是 AI 永远无法解决的游戏之一。搜索空间比世界上所有原子总数还大。然后 RL 就破解了它。）

这个经历点燃了 Jason 对 AI 的兴趣——**能自我改进的模型、系统、智能体**。

**宾大博士**：Jason 在宾大读博，两位导师都对他影响深远。其中一位在 Berkeley 机器人实验室做过博士后，这引导 Jason 进入机器人领域。宾大有 GRASP 实验室——最好的机器人研究地之一。Jason 在博士期间研究强化学习与人类数据的结合，以及非常严谨的 RL 理论。

**NVIDIA 与 Eureka 项目**：

**重要原话**：“At the time GPT-4 came out. We were very interested in solving pen spinning task. The initial idea was learning from human videos. But then I realized—today we don't have a dexterous hand that can spin a pencil at all. How would I even evaluate the algorithm? So we need to first try this in simulation. As soon as I tried to set up a simulated environment for a robot hand with a pen, I immediately saw the issue—if I had to come up with the reward function for RL to solve pen spinning, that's impossible. Then I thought—what if a model that can write code can do that? That's what became Eureka.” `[约 100:00]`
（中文翻译：当时 GPT-4 刚出来。我们对解决转笔任务非常感兴趣。最初想法是从人类视频学习。然后我意识到——今天我们没有能转笔的灵巧手。我怎么评估算法？所以需要先在模拟中尝试。当我为机器人手和笔设置模拟环境时，立刻看到问题——如果我要为 RL 想出让转笔成功的奖励函数，那是不可能的。然后我想——如果会写代码的模型能做呢？这就是 Eureka。）

**重要原话**：“We had the first recursive self-improving robotic agent in simulation because we used that to solve a new task that no one has demonstrated before. That allowed me to see the potential of using language model, using coding models to really accelerate robotics.” `[约 102:00]`
（中文翻译：我们在模拟中有了第一个递归自我改进的机器人智能体，因为我们用它解决了以前没有人展示过的新任务。这让我看到了使用语言模型、编码模型真正加速机器人的潜力。）

**Google DeepMind**：Jason 在 DeepMind 研究如何用 Gemini 做机器人。但他逐渐意识到一个问题——

**重要原话**：“There was always a question in the back of my mind—does any of this matter? When you're working on this kind of thing in the lab, you ask me how do we come up with so many interesting fun tasks—you're basically doing your own eval, you're grading your own homework. I wanted something more real. I wanted something that could actually be used by millions of people in the world.” `[约 104:00]`
（中文翻译：我内心深处总是有个问题——这些真的重要吗？当你在实验室做这类事情，你问我怎么想出这么多有趣的任务——你基本上在做自己的评估，在给自己批改作业。我想要更真实的东西。我想要真正能被世界上数百万人使用的东西。）

**创立 Dyna**：2024 年底，Jason 觉得时机到了——可以把一些技术真正带到现实世界。他与另两位联合创始人一起创立 Dyna。

**重要原话**：“Fast forward two years, we built our platform, our model, our robots are in Dentyon. Go check it out. Go eat.” `[约 106:00]`
（中文翻译：快进两年，我们构建了平台、模型，我们的机器人在 Dentyon。去看看。去吃饭。）

**未竟的梦想**：Jason 提到，很多在创立 Dyna 时暂时放弃的想法——比如模拟——现在因为前沿模型的新能力又变得可能，这让他非常兴奋。

**延伸思考**

Jason 的历程揭示了一个研究者的典型进化路径：**从纯学术好奇心（AlphaGo 震撼）→ 技术突破（Eureka 项目）→ 现实影响焦虑（“自己给自己打分”）→ 创业落地（Dyna）**。这条路径在 AI 领域越来越常见，但 Jason 的特别之处在于他的“物理世界”执念——从围棋（虚拟）到机器人（物理），他始终在追求“能自我改进的系统”，只是最终选择了物理世界作为舞台。这也解释了为什么 Dyna 如此强调真机部署——这不仅是商业策略，更是创始人的核心价值观。

**精华收获**

- AlphaGo 点燃 AI 热情：能自我改进的智能体
- 宾大博士：RL + 机器人 + 人类数据
- NVIDIA Eureka：首个递归自我改进机器人智能体（模拟中）
- DeepMind：看到用 Gemini 做机器人的潜力，但渴望真实世界影响
- 2024 年底创立 Dyna：“不想再自己给自己批改作业”

---

## 十一、公司文化与命名故事

### [01:38:00-01:48:00 / 文化与命名讨论]

**核心观点**

Dyna 是“研究 + 产品”公司，类似 OpenAI——前沿研究最终都进入产品。文化：自顶向下识别必须解决的问题，自底向上让工程师创建任务来压力测试能力。命名来自两个源头：Richard Sutton 的 Dyna 论文（强化学习自我改进）和 Jason 小时候看的 Ultraman Dyna。

**深度阐述**

**公司运作方式**：

**重要原话**：“We think of ourselves as eventually a research plus product company. It's kind of like OpenAI where you do frontier research but eventually all of them make their way into Codex or ChatGPT. We're not here to just do open-ended whatever thing that interests us at the time. We're always product-driven—we want to deploy our robots to a new customer. What are the technical problems we have to solve? Generalization, whole body control, quick adaptation, following language, dexterity. Once those problems are clear, our engineers—very capable, very smart—create instances of the task. They create tasks that would stress test those capabilities.” `[约 110:00]`
（中文翻译：我们认为自己最终是一家研究 + 产品公司。有点像 OpenAI——做前沿研究，但最终都会进入 Codex 或 ChatGPT。我们不是做开放式、当时感兴趣的任何东西。我们始终产品驱动——我们想把机器人部署到新客户。必须解决什么技术问题？泛化、全身控制、快速适配、语言跟随、灵巧性。一旦这些问题清晰，我们的工程师——非常能干、非常聪明——创建任务实例。他们创建会压力测试这些能力的任务。）

**“有趣的评估”文化**：主持人提到，Dyna 办公室有各种“趣味评估”——比如用橡皮筋把荧光笔绑在一起（测试某种能力）。工程师们非常有创意，很多侧边项目是工程师自发做的——“这个看起来好玩，就做了”。

**重要原话**：“The grabbing drink task is just how we test language following. You can just specify what you want. If the model follows intent, follows instruction, you should be able to do it.” `[约 112:00]`
（中文翻译：抓饮料任务就是我们测试语言跟随的方式。你可以指定你想要什么。如果模型遵循意图、遵循指令，就应该能做到。）

**公司规模**：硬件约 30-40%（硬件需要更多人）、模型约 10 人、软件工程师、机器人工程师、商务团队。

**Jason 的感悟**：

**重要原话**：“The most fun thing about building a robotics company is you see everything under the sun that could possibly be helpful will be helpful. When I was a researcher at a lab or a PhD student, I was talking to researchers every day. Now I also get to learn from so many different people from different walks of life. Some of our data collectors had no robotics experience—they were working retail, other jobs—and they came here, became very well trained in robotics. That's pretty amazing to see.” `[约 116:00]`
（中文翻译：构建机器人公司最有趣的事情是——你看到太阳底下的一切，一切可能有用的事情都会有用。当我在实验室做研究员或博士生时，我每天和研究员交谈。现在我也能从许多不同背景的人那里学习。我们的一些数据收集员没有机器人经验——他们在零售或其他行业工作——他们来到这里，在机器人方面训练有素。看到这些非常令人惊叹。）

**Dyna 的命名故事**：

**重要原话**：“Richard Sutton, the Turing Award winner, the pioneer of reinforcement learning, wrote a paper called Dyna many many years ago. It's about an agent that self-improves in a world model. Even when we started the company, we weren't doing world model yet, but I felt that's how robotics will get solved. Now our technology direction is converging to that. The second thing is a bit more personal—I grew up in Japan. The year I was born, there was a cartoon show called Ultraman Dyna. So it's a very subtle thing. Not many people know, but I guess now everyone will.” `[约 120:00]`
（中文翻译：Richard Sutton，图灵奖得主，强化学习先驱，很多年前写了一篇叫 Dyna 的论文。关于一个在世界模型中自我改进的智能体。即使我们创立公司时还没做世界模型，但我觉得机器人就是这样解决的。现在我们的技术方向正在收敛到那个。第二件事更个人——我在日本长大。我出生那年有一部动画叫《戴拿奥特曼》。所以这是很微妙的事情。没多少人知道，但现在大家都知道了。）

**视觉/结构信息描述**：访谈最后 Jason 透露，团队成员也是第一次听说 Ultraman Dyna 的故事。主持人开玩笑说要邀请 Richard Sutton 来 Dyna 看看。这个命名故事完美连接了 Jason 的学术偶像（Richard Sutton，强化学习先驱）和个人童年（日本 Ultraman）。

**延伸思考**

Dyna 的命名是一个绝妙的隐喻：**一个在世界模型中自我改进的智能体**——这不仅是 Richard Sutton 的 Dyna 论文的核心思想，也是 Dyna Robotics 的技术方向。从 1990 年代的 Dyna 论文到 2025 年的 Dyna-2 世界动作模型，强化学习的世界模型理念终于找到了在物理世界落地的形式。Jason 的个人故事（围棋 → RL → 机器人 → 世界模型）与公司命名形成完美闭环。这也暗示了一个更深层的愿景：**Dyna 可能不只是在解决机器人任务，而是在实现一个更宏大的 AI 梦想——能自我改进的物理智能体。**

**精华收获**

- 研究 + 产品公司：前沿研究最终进入产品
- 自顶向下识别问题，自底向上创建评估任务
- 文化：工程师自发创建趣味评估（橡皮筋、荧光笔）
- 规模：硬件 30-40%，模型约 10 人
- 命名：Richard Sutton 的 Dyna 论文 + Ultraman Dyna

---

## 十二、愿景与行动号召

### [01:48:00-End / 结尾讨论]

**核心观点**

Dyna 的愿景：真正将机器人和智能带入物理世界，部署到数千客户、数百万机器人。行动号召：行业需要更多“真正使命驱动”的人，不是做演示，而是不惜一切代价让机器人部署。Dyna 正在招聘（Bay Area）。

**深度阐述**

**6 个月到 1 年目标**：
- 扩展机器人和模型规模
- 真正部署
- 明年部署数百台机器人（当前数十台）

**2-5 年愿景**：

**重要原话**：“Our high-level mission is to truly bring robots and intelligence into the physical world. That means actually seeing our robots deployed—thousands of customers, even more, millions of robots. That's what we want to get to.” `[约 124:00]`
（中文翻译：我们的高层使命是真正把机器人和智能带入物理世界。这意味着真正看到我们的机器人部署——数千客户，甚至更多，数百万机器人。这是我们想达到的。）

**行动号召**：

**重要原话**：“I do feel like as an industry robotics is still very demo-oriented. I have done a lot of demos in the past in my lab. Even here we had to show some demos. I think we need more people that's truly mission-focused on doing whatever it takes to get robots deployed, get robotic foundation models truly integrated with hardware and seeing them at real customer sites. We're a pioneer in this regard and I want to see more in this field. For the audience watching, if this mission inspires you, if solving the hardest problems today is what makes you wake up every day and you want to contribute—we're always hiring.” `[约 126:00]`
（中文翻译：我确实觉得机器人行业仍然非常 demo 导向。我过去在实验室做过很多演示。即使在这里，我们也必须展示一些演示。我认为我们需要更多真正使命驱动的人，不惜一切代价让机器人部署，让机器人基础模型真正与硬件集成，并在真实客户现场看到它们。我们在这方面是先锋，我希望在这个领域看到更多。对于观看的观众，如果这个使命激励你，如果解决今天最难的问题是你每天醒来的动力，你想做出贡献——我们一直在招聘。）

**招聘地点**：Bay Area（目前），随着公司成长不排除其他地点。

**结语**：

**重要原话**：“I wanted to see more robots in the world.” `[约 128:00]`
（中文翻译：我想看到世界上更多机器人。）

**视觉/结构信息描述**：访谈以 Jason 和主持人的轻松对话结束。主持人感谢 Jason 的接待，Jason 表示“不后悔做这次现场访谈”——“机器人必须在现场做访谈”。主持人建议听众观看视频版本，因为有有趣的 B-roll 素材。

**延伸思考**

Jason 的“行动号召”实际上是对整个机器人行业的一个诊断：**行业过于 demo 导向，缺乏真正使命驱动的部署文化。** 这与许多 AI 领域的问题类似——论文和 demo 很多，真正改变世界的产品很少。Dyna 的差异化不仅在于技术，更在于这种“不惜一切代价部署”的文化。对于创业者来说，这是一个重要提醒：**技术领先不等于市场领先，真正的壁垒是执行力和使命驱动。**

**精华收获**

- 愿景：数千客户、数百万机器人，真正将智能带入物理世界
- 行动号召：需要更多使命驱动的人，而非 demo 导向
- 招聘：Bay Area，always hiring
- “我想看到世界上更多机器人”

---

## 全篇总结与精华收获

### 核心洞察

1. **世界动作模型 = 物理世界的思维链**：先预测未来，再生成动作。这是机器人从“条件反射”到“先想后做”的范式跃迁。

2. **机器人没有互联网**：数据是最大瓶颈。最佳策略：大规模人类自我中心数据预训练 + 少量机器人数据微调。数据质量是非平稳问题。

3. **扩散 Transformer + 流匹配**：当前机器人基础模型的标准架构。Transformer 负责学习，扩散/流匹配负责生成平滑精确动作。

4. **半人形 + 轮式 + 自研执行器**：硬件必须匹配数据策略（人类数据 → 人形比例）。执行器必须自研，因为建模精度要求。

5. **真正的商业化 = 多地点部署**：不是 pilot，而是客户愿意规模化部署。Dentyon（餐巾折叠）和 Best Western（毛巾折叠）是验证案例。

6. **系统问题而非模型问题**：需要智能体框架、推理层 + 动作层、全栈控制。价值在“无监督运行数小时的工作流”。

7. **机器人苦涩教训**：简单算法 + scale 正确数据 → 泛化涌现。但“正确数据”的定义比语言模型难得多。

8. **合成数据是下一个前沿**：前沿模型可以做 real-to-sim CAD 转换。世界动作模型可以生成自己的训练数据（自我飞轮）。

9. **行业格局**：世界动作模型 vs 视频世界模型 vs VLA。Dyna 认为预测原始世界（而非抽象表示）是第一性原理。

10. **使命驱动胜过 demo 导向**：行业需要更多真正让机器人部署的人，而非做酷炫演示的人。

### 可行动建议

- **对于 AI 研究者**：关注世界模型在物理世界的应用，这是下一个前沿。扩散/流匹配在机器人领域有独特优势（可实时重新评估）。

- **对于创业者**：全栈控制是机器人公司的护城河。数据策略必须动态迭代（非平稳性）。真机部署 = 商业验证 + 数据收集。

- **对于投资者**：关注有真机部署能力的机器人公司，而非只有 demo 的。多地点部署是商业化的关键验证信号。

- **对于工程师**：考虑加入 Dyna（Bay Area，always hiring）或类似使命驱动公司。“解决今天最难的问题”是核心驱动力。

- **对于数据供应商**：机器人数据需求巨大，egocentric 数据、机器人数据、视频数据都有价值。联系 data partnerships at dyna.co。

### 改变认知的关键点

- **“机器人是系统问题，不是模型问题”**：需要模型 + 硬件 + 智能体 + 框架工程 + 数据策略的协同优化。

- **“硬件形态必须匹配数据策略”**：Dyna 先决定用人类数据，然后反推硬件比例。这是“数据优先”的硬件设计。

- **“预测尽可能多的世界，而非抽象表示”**：这是苦涩教训在机器人领域的应用——去除人类偏见，预测原始输入。

- **“价值在无监督运行数小时的工作流”**：不是 1 分 30 秒的任务，而是完整工作流（如洗衣全流程 1 小时）。

---

<!-- TLDR: 世界动作模型让机器人先预测未来再行动，用百万小时人类数据+少量机器人数据，实现真机多地点部署。 -->
<!-- TAGS: 机器人, 世界模型, 物理AI, 强化学习, 创业 -->
<!-- RATING: 5 -->
