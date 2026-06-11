---
title: "⚡️ Google's Open AI Strategy — Omar Sanseviero, Google DeepMind - 结构化文稿"
channel: "Latent Space"
published: "2026-05-24"
source_url: "https://www.youtube.com/watch?v=Hxlayqs-IAs"
video_id: "Hxlayqs-IAs"
variant: "structured"
---

# ⚡️ Google's Open AI Strategy — Omar Sanseviero, Google DeepMind - 结构化文稿

- **Channel:** Latent Space
- **Published:** 2026-05-24
- **Source:** https://www.youtube.com/watch?v=Hxlayqs-IAs
- **Main:** [⚡️ Google's Open AI Strategy — Omar Sanseviero, Google DeepMind](2026-05-24-⚡️-google's-open-ai-strategy-—-omar-sanseviero,-google-deepmind-Hxlayqs-IAs.md)

# 深入对话：Google DeepMind 的 Gemma 4 开源模型策略与多模态前沿

## Gemma 4 概览：最强大的开源模型

Gemma 4 刚刚发布，是迄今为止 Google DeepMind 开源模型中最强大的一个。团队致力于尽可能提高每参数的智能密度（intelligence per parameter），并引入了多模态能力。当被问及 TL;DR 时，Omar Sanseviero 确认这就是该模型的核心特点。

### 有效参数 vs 活跃参数：架构创新

在传统 Transformer 架构中，通常有一个大型的嵌入层（embedding layer）。Gemma 4 的架构在 Transformer 块中做了一个小改动：**每层添加一个嵌入表（per-layer embedding table）**。这样做的关键在于，你不需要进行完整的矩阵乘法——它更像一个查找表（lookup table）。

具体来说，Gemma 4 模型是 **E2B**，这意味着它实际加载到 GPU 的只有 **20 亿参数**，而模型本身近 **50 亿参数**——额外的 30 亿参数可以放在 CPU 甚至磁盘上。因此，推理速度极快，因为这只是个查找表操作。

**为什么不是所有情况下都这样做？** 这种设计是专门针对设备端（on-device）优化的，例如运行在手机、Android 设备、树莓派（Raspberry Pi）等。当模型规模更大时，通常希望更紧凑，倾向于密集架构（dense architecture）或混合专家架构（MoE）。所以，这类研究选择非常适合小规模使用场景。

**有趣的应用**：在中国，超级应用（super apps）会将模型直接打包进应用包（app bundle）中进行推理。Omar 表示，这也正是他们的目标用例之一。

## 设备端推理与 Gemma Nano

如果你购买一台 Pixel 手机或高端三星手机，它们会预装 **Gemini Nano**，并集成到操作系统中。而 **Gemini Nano 本质上是基于 Gemma 构建的**。去年团队发布了 Gemma 3N，该架构专为手机用例设计，再经过额外训练和适配，使其在传统设备端场景中表现出色。因此，购买这些高端手机时，开箱即可使用 Gemini Nano。

在较小的模型中，Gemma 4 系列也采用了类似的**参数卸载（parameter offloading）** 或**按需下载（download on demand）** 技术。例如，Gemma 4 的 2B、4B 版本都可以高效运行多模态任务。

### 型号与扩展性

Gemma 4 有两个主要型号：

- **29B/31B 密集型（Dense）**：追求原始的智能密度，其中 31B 是最大的版本，量化后可适配消费级 GPU。
- **27B 混合专家型（MoE）**：拥有 40 亿活跃参数，推理速度极快。
团队正在进行大量实验，探索能否将这类架构推向更大规模。

## 发布背后的团队与合作伙伴

Gemma 团队实际上规模相对较小：只有 2-3 位产品经理、1 位市场营销人员，以及负责工程和研究的同事。整个流程包括完整的训练、后训练（post-training）、蒸馏（distillation）和后训练技术等。

更令人兴奋的是，模型完成后，团队与**近 50 个外部开源合作伙伴**进行协作，例如：

- llama.cpp
- Ollama
- MLX
- Hugging Face
- vLLM
- Nvidia
- AMD
内部则与 Google Cloud、Vertex AI、Vertex Models as a Service、ADK 以及 Android 团队紧密合作。例如，随着 Gemma 4 的发布，**Android Studio 中集成了 Agent 模式**，开发者可以使用离线模型（通过 llama.cpp、vLLM 或任何 OpenAI 兼容端点）来辅助编写代码。这非常适合离线或注重隐私的开发场景，比如在长途飞机上完全本地化开发。

### 未来前景：小模型 vs 大模型

Omar 认为，未来的 1-2 年内，我们完全可能看到像 **Gemini 3 Pro 那样强大的模型在手机上本地运行**。但这并不意味着小模型会取代大模型：

- **本地模型** 适合智能体（agentic）能力，如函数调用（function calling）、系统指令、对话等。
- **知识层面** 仍然需要更大模型，因为知识来自海量数据，小模型无法存储所有事实。比如，Gemini 在知识和世界事实方面远超 Gemma。
两者是互补的，不会相互吞噬（cannibalize）。

## 多模态能力：音频、图像与视频

Gemma 4 基于与 Gemini 3 相同的研究构建，因此受益于后者在多模态上的所有改进。具体能力包括：

- **音频**：支持语音识别、语音到翻译文本（speech-to-translated text）以及一定程度的语音理解。你可以询问音频文件的相关问题，非常适合设备端电话用例。
- **图像与视频**：支持物体检测、指称（pointing）、字幕生成。支持约 30-60 秒的短视频和音频输入。
- **不支持的功能**：目前不支持图像分割（image segmentation），也不支持同时输入视频和音频（即同一提示中既有视觉部分又有音频部分）。团队认为通过更多数据或额外的微调可以改善这一点。
- **音频输出**：仍在探索中，目前无可分享信息。
多语言方面，Gemma 支持 **140 种语言**，其分词器（tokenizer）基于 Gemini 的分词器，非常高效。即使用户只取基础 Gemma 模型并针对某个语言额外微调，也能取得出色效果。

## AI 工程师大会：研究者的参与

这次是 DeepMind 首次将团队带到伦敦的 AI 工程师大会（AI Engineer Conference）。Omar 认为，**将研究者带到工程师面前非常重要**：

- 工程师希望了解模型是如何训练的，即使他们自己从不训练模型。
- 这样可以增加对模型的信任，同时工程师也能回家后更有深度地讨论技术。
团队带来了多位研究者，涵盖 Gemma 4 开发、**扩散 Transformer（Diffusion Transformer）用于文本生成**（不是图像生成）等主题。

### 扩散文本生成：速度优势与挑战

扩散模型用于文本生成的主要卖点是 **速度**。以往需要特殊标记的“填充中间（Fill-in-the-Middle，FIM）”任务，如今模型开箱即用便能完成。Omar 认为这仍处于实验阶段，质量略逊于标准自回归（auto-regressive）模型。但它可能成为“系统一”（快速响应），而自回归模型作为“系统二”（深度推理）。然而扩散模型在微调上存在困难，灵活度受限。未来可能会有一个强智能体管理器，配合扩散执行器完成特定编码任务。

## 微调趋势的变化

Omar 观察到：**2024 年以来，模型的整体能力大幅提升，开箱即用已经足够好**。因此，许多团队尝试对 Gemma 4 进行微调时发现不需要了——模型自身就胜任多数任务。尽管如此，**特定领域（金融、医疗等）仍有微调需求**，因为这些领域的数据是模型未曾见过的。

**Med-Gemma** 就是一个例子：它基于 Gemma 3，并加入了医疗数据集进行额外训练。

### 设备端多 LoRA 的挑战

假如手机上有 20 个应用，每个都带来自己的 LoRA（低秩适应模块），那么当基础模型更新时，所有 LoRA 都需要同步更新。这会导致非常复杂的开发者体验问题，因为 Android 和 iOS 的发布周期不同。这是一个需要行业共同解决的挑战。

## 密集模型 vs MoE 模型的抉择

当被问及为何在相似参数规模下提供两种版本时，Omar 解释：

- **31B 密集模型**：原始智能最高，是量产后能放入消费级 GPU（如 24GB）的最大尺寸。
- **27B MoE 模型**：推理速度极快，但 MoE 在微调时存在挑战。路由（routing）机制可能影响反向传播，导致标准微调配方不能直接适用。需要更多实验来确定是否冻结路由器等。
总的追求是：**尽可能低的稀疏度（sparsity）和尽可能高的“每字节 ELO（智力）”**，即最大化每参数的智能密度。以 Gemma 系列为例，相同参数规模（约 30B）下，Gemma 4 相比前代智能水平大幅提升。

不过，知识容量受限于信息论：模型本质上是一个数据库，有限参数只能存储有限事实。即使未来 30B 模型非常强大，也可能不知道某个冷门国家的总统。

## GemmaScope：模型可解释性

GemmaScope 允许分析模型在不同层上的激活（activations）。团队去年 12 月发布了**数太字节（TB）甚至近 1 PB 的数据**，覆盖 Gemma 3 所有层的所有 Token。这是一个非常完整的可解释性数据集，通过与社区协作（如 Neuropedia 等），工程师可以用较少算力入门，理解 Transformer 架构的工作原理。

## 研究与工程的融合

Omar 认为，研究和工程之间的界限比人们想象的要近。许多研究人员实际上在做大量的消融实验（ablations）——只是把不同组件拆解组合，观察效果。这本身就更接近工程研究。同时，工程师也可以通过 GemmaScope 等工具进入研究领域。

有趣的是，研究人员也开始采用智能体工具来做实验。例如，团队内部正在构建用于实验、消融和评估的智能体技能（Agent Skills），让研究过程更高效。

**自动化研究（Auto Research）** 在之前几波 AI 浪潮中曾以 AutoML 形式出现，但现在可能通过智能体实现实验的自动执行。但 Omar 认为，真正有影响力的突破需要模型做出人类没想到的“第 37 手”（Move 37）那样的发现。下一代的微调者可能完全不需要自己写代码，而只需通过自然语言提示智能体启动实验。

## 团队发展与扩张

Omar 领导的 DevRel/DevEx 团队正在招募**高能动性（high agency）** 的人员，他们对建设、与社区互动充满热情。团队目前正在以下地点扩张：

- **新加坡**：DeepMind 设有小型但高密度的办公室，团队希望成员能与本地研究者面对面交流。
- **印度**：另一个重要的人才区域。
全球分布包括巴黎、伦敦、苏黎世、旧金山、纽约等 DeepMind 研究枢纽，新加坡逐渐成为新的增长点。

### Kaggle 加入 DeepMind

几天前，Kaggle 正式加入 DeepMind。这对于评估和社区互动意义重大：Kaggle 基准测试（benchmarks）可以很好地融入 Gemini 的能力评估，帮助发现模型潜在的长处和短板。团队非常重视来自初创公司、社区和开发者的反馈，并反馈到模型改进中。

## 结语

Omar 最后强调，整个 Gemma 和 Gemini 系列的设计优先级，始终是**开发者真实需求**——团队持续与社区在社交媒体、论坛和活动中互动，收集反馈并迭代模型。期待未来能带来更多惊喜。

---

*以上内容基于 Google DeepMind 的 Omar Sanseviero 在 Latent Space 的采访整理，所有陈述均忠实于原始视频文稿。*
