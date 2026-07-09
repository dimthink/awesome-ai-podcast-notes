---
title: "The 100,000 Sandbox Problem — Akshat Bubna, Modal CTO"
channel: "Latent Space"
published: "2026-07-08"
source_url: "https://www.youtube.com/watch?v=UwxxlTNPjWo"
video_id: "UwxxlTNPjWo"
tags: ["代理体验", "弹性计算", "GPU沙盒", "推测解码", "基础设施原语"]
rating: 4
language: "英文"
word_count: 15867
duration: "59:10"
---

# The 100,000 Sandbox Problem — Akshat Bubna, Modal CTO

- **Channel:** Latent Space
- **Published:** 2026-07-08
- **Source:** https://www.youtube.com/watch?v=UwxxlTNPjWo
- **TL;DR:** 代理基础设施应聚焦于弹性原例，让代理像开发者一样操作计算、存储和网络，Modal用沙盒和自动缩放提供了方案。
- **Tags:** 代理体验, 弹性计算, GPU沙盒, 推测解码, 基础设施原语
- **Rating:** 4

## 版本

- [结构化文稿](2026-07-08-the-100,000-sandbox-problem-—-akshat-bubna,-modal-cto-UwxxlTNPjWo.structured.md)
- [原始文稿](2026-07-08-the-100,000-sandbox-problem-—-akshat-bubna,-modal-cto-UwxxlTNPjWo.transcript.md)

# 材料信息

- **标题**：The 100,000 Sandbox Problem — Akshat Bubna, Modal CTO
- **作者/来源**：Latent Space 频道（主持人：Swyx，嘉宾：Akshat Bubna）
- **类型**：YouTube 视频字幕（深度技术与商业访谈）
- **关键元数据**：访谈时间约为2024年末至2025年初，嘉宾为Modal联合创始人兼CTO，对话围绕Modal从服务器容器平台到AI推理、训练、沙盒和代理基础设施的演进。

---

# 开篇引入

“为什么一个代理要读几百个Kubernetes文件、写连类型检查都没有的YAML，而它明明只需要改几行装饰器就能拥有一个自提运行环境？”这句话像一把手术刀，剖开了Modal过去两年最核心的转型：从开发者体验（DX）转向代理体验（AX）。当AI代理开始像人类一样使用基础设施时，你为人类设计的优雅CLI还管用吗？当强化学习训练需要同时启动十万个沙盒时，你的弹性调度扛得住吗？在Latent Space这期访谈中，Modal的CTO Akshat Bubna不仅直面了这些问题，还展示了一个正在自洽的逻辑：最好的AI基础设施，应该让代理和人类使用同一套原语——而Modal正在成为这套原语的铸造者。如果你觉得AI基础设施只是“租卡卖卡”的生意，这场对话会让你看到软件层如何在GPU短缺、代理爆炸和后训练狂热中重新定义价值。

---

# 详细内容

## 从DX到AX：开发者退场，代理登台 [章节 1：开场与核心转变]

**核心观点**

Modal将SDK团队的优化目标从“开发者体验”正式切换为“代理体验”，并认为DX与AX高度同构——好的基础设施原语应当同时服务人类和机器。

**深度阐述**

访谈一开场，Akshat就抛出了一个石破天惊的宣言：“We've actually changed our SDK team to think about agent experience instead of developer experience.”（我们实际上已经改变了SDK团队，让他们思考代理体验而非开发者体验。）这不是营销口号，而是整个产品哲学的迁移。Akshat紧接着解释了背后的逻辑：开发者体验（DX）所追求的简洁、可编程、低认知负荷，在代理体验（AX）中不仅依然成立，而且更为关键。因为代理没有人类那样的模糊容忍度，它不能“看文档猜用法”，它需要的是一组可预测、可操作、可调试的原语。

为什么一个代理需要读几百个Kubernetes文件、写YAML，而它只需要修改一个装饰器就能获得一个自动伸缩、自带观测、即时生效的运行环境？这背后是Modal坚持了近四年的设计理念：**将基础设施的需求与代码的声明放在同一位置**。当代理修改代码时，基础设施的变更自动跟随——这比让代理去理解YAML的层级和Kuberneties的RBAC模型要高效得多。

“same benefits that apply for DX also actually apply for AX”（适用于DX的好处同样适用于AX），Akshat强调。但这里有一个微妙的转折：当代理成为最终用户时，人类开发者反而变成了“监管者”——他们不再逐行阅读代码，而是通过仪表盘观察行为的可观测性。“I think actually think it takes a bit of restraint to not specialize to say I want to ship a new primitive and then just be general purpose.”（我认为需要一点克制，不去过度专业化，不去说‘我想推出一个新原语’，而是做一个通用平台。）这正是Modal的战略：不只为代理定制一个新API，而是把现有的计算、存储、网络原语打磨到代理可以原生使用的地步。

**个人感受**

主持人Swyx带着一贯的犀利追问：“The negative thesis now is that nobody’s looking at their code anymore. So there’s no point.”（现在有个负面论调：没人再看代码了，所以（标记基础设施的做法）没意义了。）Akshat的反应是一阵苦笑和沉默后的坦诚：“It’s so fucking obvious.”（这太他妈明显了。）他承认，当人类不再直接阅读代码时，观测和仪表盘变得比代码本身更重要。但他同时指出，代理仍然需要操作的基础设施原语——而可观测性则是人类介入判断的窗口。这种对话中流露出的不确定性，反而比任何信心满满的宣言更让人信服。

**延伸思考**

“代理体验”这个概念一旦成立，现有的CLI设计、文档结构、错误信息格式都要被重新审视。代理可以“读”文本，但它不会“浏览”UI；它需要结构化的输出（比如JSON）和确定的退出码。API的RESTful设计对代理是否依然友好？还是说，GraphQL式的一次返多才更适合？Modal的解法是将日志和指标也搬到了CLI上，让代理可以像人类一样“grep”和“curl”——这不是投机取巧，而是把AI视为另一种“开发者”。

**精华收获**

- **AX && DX**：好的基础设施原语应该同时服务人类和机器，二者并非对立。
- **装饰器即配置**：通过代码中的装饰器声明基础设施需求，让代理的修改产生连锁反应，避免YAML的脆弱性。
- **观测先行**：当人类不再遍览代码，观测性成了人机交互的界面。

## 起源：一个“反Kubernetes”的运行时 [章节 2：Modal的诞生与早期洞察]

**核心观点**

Modal最初不是GPU公司，甚至不是AI公司——它的起点是构建一个比Kubernete更好的服务器运行，而“自提运行时”和“装饰器优先”的哲学早在第一行代码时就已确立。

**深度阐述**

“I actually first met Eric who’s the CEO through an investor and um back then Eric was already thinking about building uh a new kind of runtime.”（我第一次见Eric（CEO）是通过一位投资人，那时Eric已经在思考构建一种新的运行环境。）Akshat讲述了Modal的起源：Eric之所以想建一个新运行时，源自一个朴素但痛苦的观察——工作流编排产品为什么那么难用？答案是：因为人们不得不在Kubernetes上运行它们。

Kubernetes的设计哲学是面向“缓慢扩展、类似Web服务器”的稳态场景，而AI工作负载的典型特征是**突发性**：需要瞬间飙升的算力，之后又立刻降为零。Kubernetes的Pod启动速度、YAML配置的复杂性、缺乏对加速器的原生优化，让它变成了AI团队的噩梦。

早期Modal虽然也看到数据工程和ETL的需求，但真正的引爆点是2022年11月ChatGPT发布前一年，他们就已经在平台上加了GPU。Akshat笑着回忆：“We added GPUs to the product a year before Chat GPT came out. We just didn’t think it would be that big of a deal.”（我们在ChatGPT发布前一年就加入了GPU，只是当时没觉得会搞这么大。）

主持人Swyx分享了另一个渊源：他在Temporal工作时写过一篇关于“自配置基础设施”的文章，结果被Modal放在了官网首页。那个核心洞察是：**所有基础设施的需求都应该用代码里的装饰器表达，与函数并列。** 这样写出来的配置是类型安全的、可操作的、可单元测试的，而不是悬浮在代码之外的YAML。Akshat确认：“That was always a very important part.”（那一直是极重要的一部分。）

当被问到外界是否质疑“这是否只是又一个DSL，你们会不会锁定用户”时，Akshat的回应很干脆：“You own the code.”（你永远拥有代码。）Modal的装饰器只是配置层，用户随时可以取出代码自己去运行——甚至Modal也提供了透明逃逸，让用户可以切到完整模式。

**个人感受**

Swyx提到自己三年前试用Modal时的体验：“It was pretty pleasant experience.”（体验非常愉悦。）他当时做的项目叫Small Developer，一个早期的编码代理原型——后来这个项目在Modal上催生了沙盒产品。Akshat对此有微妙的自豪：“You blew up on Hacker News and we got a big traffic spike.”（你在Hacker News上火了，给我们带来了一大波流量。）这种“用户自发带来惊喜”的叙事，贯穿了Modal的产品史。

**延伸思考**

Modal的“反Kubernetes”立场在今天看起来极具先见之明——但当时，Kubernetes已经是云原生的标准，去挑战它需要不小的勇气。更关键的是，他们没有试图替换Kubernetes，而是建了一个抽象层，让资源调度、网络、存储对用户隐去。这个设计在今天代理需要操作“自己的计算机”时，反而成了最合适的基础。

**精华收获**

- **起点是运行时，不是AI**：Modal的最初洞察是容器运行环境需要重新构想，先有好运行时，才能承载AI。
- **装饰器与代码共处**：基础设施的声明与代码合并，避开YAML陷阱，带来类型安全和动态性。
- **GPU是后来的“超预期”**：在AI爆发前一年就已经准备好基础设施，运气背后是洞察。

## 2000天前的沙盒：从代理循环到十万级训练 [章节 3：沙盒——代理的原生计算机]

**核心观点**

Modal在2023年5月推出了“沙盒”产品，最初只是为了让代理可以在循环中自我迭代；两年后，沙盒成为RL训练的核心基础设施，单次训练需要同时运行十万个。

**深度阐述**

沙盒的故事与Swyx的早期项目紧密纠缠。2023年，Swyx正在做Small Developer——一个能自我写代码、自己运行调试的代理。他需要一种环境：启动快、有GPU、用完即关、下次再开。Modal的GPU沙盒正好满足需求：“Spin up a GPU sandbox, throw it on there, it’ll take a Hugging Face link.”（启动一个GPU沙盒，丢进去，直接处理Hugging Face链接。）

Akshat回忆，当时他们正在和不少客户谈“沙盒”需求，于是2023年5月正式发布了沙盒API。第一个示例就叫**“Small Developer in a Loop”**——让代理自己生成代码、运行、得到反馈、再修改。当时的模型远不如今天聪明，工具调用还不成熟，“The models would just diverge after like 10 iterations and not produce anything meaningful.”（模型迭代10次后就会发散，产不出任何有意义的东西。）但Modal已经认定这是方向。

今天，情况已然天翻地覆。强化学习（RL）训练的核心是“策略评估+更新”循环，其中最具计算密度的是**策略展开**——让多个代理并行与环境交互，产生海量训练数据。这种场景需要的不是几十个沙盒，而是同时启动**十万个沙盒**。主持人Swyx精准提炼：“The 100,000 Sandbox Problem”正是这一集的标题。

为什么需要Modal而不是Docker Compose？Akshat列出了沙盒的进阶能力：可以配置sidecar容器、控制出站网络（例如中间人代理用于记录RL的log）、注入凭证、快照与恢复、甚至是跨节点的多沙盒通信—— “a sandbox is actually a pod of containers”（一个沙盒实际上是一组容器的组合）。这些对于需要模拟真实环境的代理训练而言，都不是可有可无的细节。

**个人感受**

Swyx讲述了一个充满宿命感的细节：他2023年在Small Developer项目上使用Modal，但当时没意识到这就是“Proto Cognition”——如果当时他沿着那条路深挖下去，也许就能更早看到今天的代理狂欢。Akshat笑着接话：“Collect all the failures, build benchmark, collect all the examples, build the eval environment, sell it for $10 billion to Meta… it’s actually not that hard in retrospect.”（收集所有失败、建测试基准、收样例、搭评估环境、卖给Meta赚100亿……事后看还真不难。）这既是对机遇的感慨，也是对先行者的致敬。

**延伸思考**

沙盒从“测试环境”进化为“训练环境”，改变了云基础设施的调度模式。以前是“一个用户创建一台虚拟机”，现在是“一个训练任务动态创建十万个沙盒”。每个沙盒需要独立的网络、文件系统、安全边界，生命周期可能只有几十秒。这是一场对调度器和网络层面的极致考验——传统云厂商的虚拟机环境根本无法承受这种频率的创建与销毁。

**精华收获**

- **沙盒是代理的“计算机”**：代理需要一台自己能随时启动、配置、销毁的电脑，沙盒就是抽象。
- **RL训练是沙盒杀手级场景**：策略展开需要大规模并行沙盒，对弹性伸缩提出了十万级要求。
- **快照、网络、sidecar是关键原语**：面向代理的沙盒不是简单的容器，而是完整的“计算机单元”。

## 弹性推理：为“怪异模型”准备的自动缩放引擎 [章节 4：推理的自动缩放与GPU快照]

**核心观点**

弹性推理是Modal目前最大的使用场景——专为自定义模型（非主流LM）的不规则流量设计，通过GPU快照和多提供商资源池实现真正的“从零到峰值”自动缩放。

**深度阐述**

当主持人问“Modal的PMF（产品市场匹配）是从哪里开始的”时，Akshat的回答很明确：“Our biggest use case actually is elastic inference… for custom models.”（我们最大的使用案例是弹性推理……为自定义模型服务。）他特意强调，Modal早期刻意避开了大型语言模型（LM）的推理，转而去服务那些“奇怪”的模型：Sunno（音频生成）、Runway（视频生成）、机器人公司、计算生物学公司。这些模型的特点是：**流量完全不可预测**——公司发布产品时，突然需要成百倍的GPU；而且常常是多个模型部署在不同区域，缩放周期彼此错开。

Kubernetes在这种场景下几乎无能为力。它基于CPU利用率的HPA设定在GPU场景下误报率高，而且Pod启动速度慢。Modal的做法是：**在软件层构建一个跨17家云提供商的资源池**。当用户流量暴涨时，Modal可以在不同提供商之间弹性分配实例，甚至在某个区域容量不足时自动路由到其他区域。

实现这一点的关键之一是**GPU快照**。Akshat解释：“We take the GPU state, like your torch compiler model snapshot it, and next cold start is way faster.”（我们获取GPU状态，比如对Torch编译后的模型做快照，下次冷启动就快得多。）这意味着即使是冷启动，也能在几秒内开始服务，这比其他服务商等待新实例启动要高效得多。

主持人追问：“如果我拿同一个模型，用你自己的推断引擎（比如vLLM、SGLang）在同样规格的GPU上跑，差距在哪儿？”Akshat坦承，他们把自己在推理内核上的改进都开源了，所以单论单机性能差距不大。但真正的差异在于**弹性**：“We are way more elastic… have true scaling to zero, true burstiness.”（我们弹性好得多……能够真正缩到零，真正处理突发。）对于大多数用户来说，折腾部署的运维成本远远高于内核微调——Modal把这部分打包成了自动端点（Auto Endpoints）。

**个人感受**

Swyx提到自己在小开发者项目时使用Modal的感受：“It was a pretty pleasant experience.” 这种“愉悦感”在Kubernetes生态中罕见。Akshat对此很重视：“We really didn't want people to spend so much time writing YAML.”（我们真的不想让人花那么多时间写YAML。）从那天到现在，这个理念从未改变。

**延伸思考**

弹性推理之所以成为AI Infra的硬骨头，不仅因为GPU是高价值资产，更因为**流量模式不符合任何经典统计分布**。一个机器人公司可能一天内的GPU需求从100到3000之间剧烈波动。传统云厂商的重资产模式无法提供这种弹性——客户被迫签年约、付预留实例费用，承受低负载时的浪费。Modal通过聚合多源GPU和精细的调度算法，把碎片化需求整合为可预测的调度流，从而既提供了弹性，又保持了合理的成本结构。

**精华收获**

- **自定义模型是弹性推理的首要场景**：主流LM API（如GPT）不需要Modal，但“奇怪”的模型需要。
- **GPU快照消灭冷启动**：模型状态快照使得弹性伸缩发生时，新节点能立即服务。
- **弹性不只是自动缩放**：涉及区域路由、多提供商资源池、调度策略和可靠性工程。

## 推测解码：从内核优化到乘法级性能 [章节 5：推测解码与Dflash——开源的信心]

**核心观点**

Modal在推测解码领域做出了关键性突破（Dflash块推测器），并选择完全开源——因为真正的护城河不在内核优化，而在全栈弹性。

**深度阐述**

主持人用一贯的方式引导：“I thought this was actually an interesting blog post… They make a claim that speculative decoding really gets you anything you want. What do people should know?”

Akshat首先简洁地解释了推测解码的原理：用小模型（草稿模型）推测未来几个token，再由大模型批量验证。由于大模型逐token生成时受限于内存带宽，而批处理可以更高效地利用计算资源，所以只要草稿模型的接受率足够高，就能获得**2-4倍的整体加速**，而且质量无损——因为大模型从不接受比自己更差的token。

“People talk a lot about we made these kernels faster… but improving kernels only gives you a few percentage points. Increasing accept length literally is a multiplicative decrease in latency.”（人们总在讲内核优化如何如何……但内核优化只能提升几个百分点。而提高接受延迟是字面上的乘法级效果。）这句话点明了直觉：端到端的性能瓶颈不在某一层的计算，而在于生成模式。

Modal团队在这个方向上走得更远：他们提出了**Dflash**，一种块级别推断器——不是一次预测一个token，而是一次预测一个块。这个突破被完全开源，并已成为vLLM的一部分。主持人追问：“你们的优化到底在哪？别人用同样的推理引擎在同样的GPU上跑，为什么选你们？”Akshat的回答很清醒：“We just want the improvements our team comes up with to be there for others to use outside of Modal… The benefit to us is our team can help you get performance first when something new comes out.”（我们只想让自己的改进能够被社区使用，即便不用Modal……但我们的优势在于，当新技术出现时，我们的团队可以最先帮你获得性能。）然后他再次强调，弹性才是感知中的核心差异。

**个人感受**

主持人对“Auto Endpoints”很感兴趣——这是Modal最近推出的功能，无需写代码就能创建一个带有所有优化（包括Dflash）的端点，对推理自动进行配置优化。而且Modal承诺完全透明：用户可以看到生成的代码，随时可以“弹出”到自己掌控。Akshat的语调里带着工程师的谨慎：“We want to make frontier-level performance available to everyone.”（我们希望让前沿水平的性能对每个人可及。）

**延伸思考**

推测解码的全链路优化正在改变推理经济学。对于部署规模较大的场景，2-4倍的延迟乘数意味着可以减半GPU用量，或提升用户体验的流畅度。Modal将这部分工作开源，一方面聚集了社区贡献，另一方面用软件工程和弹性的价值获取溢价，而不是藏着黑魔法。

**精华收获**

- **推测解码是免费的加速剂**：通过草稿+验证机制，在不牺牲质量的情况下获得2-4倍延迟提升。
- **块推测器（Dflash）更具潜力**：预测整个块匹配效率更高，Modal已开源。
- **真实差异不在内核，而在全栈**：Modal的竞争壁垒是弹性，不是单点加速。

## 多节点训练与Auto Research：后训练时代的服务器架构 [章节 6：后训练基础设施——多节点RDMA与Auto Research]

**核心观点**

Modal面向中小规模后训练场景构建了多节点训练能力（RDMA网络+I6PN覆盖网络），同时Auto Research（代理驱动的超参搜索）正在成为模态平台的新兴工作负载。

**深度阐述**

当主持人问到分布式训练时，他的怀疑很直接：“People spend a lot of money on cables to hook up GPUs, and even that is not fast enough. Is your networking fast enough?”（人们花好多钱买线缆连接GPU，带宽还是不够。你们的网络够快吗？）

Akshat没有正面挑战大规模预训练集群（比如万卡集群），而是明确指出Modal的目标是**中小规模后训练（post-training）**——比如RLHF、微调、适配器训练。这些场景需要小到中规模的GPU集群（如8-64卡），而且通常时间很短、频率很高。在这种情况下，“研究者的瓶颈是等不到集群”——大公司的集群被训练消耗，小公司则不得不浪费大量时间在调度上。Modal的多节点训练产品允许用户通过装饰器声明一个GPU集群，然后自动配置RDMA网络和文件系统，做到真正的**服务器化训练**。

支撑这一切的基础是他们内部的覆盖网络**I6PN**（IPv6 Private Network）。原本是为了分布式训练中RDMA的密钥交换而设计的TCP覆盖网络，但用户很快发现了其他用途——比如让沙盒间进行私有通信。Akshat笑称：“People are using it for something you never intended.”（人们在用你从没想过的方式使用它。）这正体现了Primitive的威力。

主持人接着聊到**Auto Research**（自动研究）——一个可能成为未来的大趋势：让代理Agent自动探索不同的模型配置、超参数甚至架构。他直言，目前Auto Research的状态就像“science fair”（科学展会），离真正改变科研范式还很远。但Akshat透露内部已经在使用类似工具：一个名为“Auto Inference”的内部系统，代理会自动跑不同配置、甚至调用Nvidia的Nsight Profiler，然后调整参数、切换GPU型号——最终找到最优推理方案。“It works really well.”（效果非常好。）他们甚至也用来辅助FDE（现场可靠性工程师）的工作。

**个人感受**

主持人提到RAMP的例子——一个在Modal上运行面向外部的会计代理的公司。他们不仅需要沙盒，还需要持久化文件系统、网络控制、区域要求等。Akshat描绘了一幅图景：代理不再只是写代码，而是在操作整个基础设施。对Modal而言，这既是挑战也是机会。

**延伸思考**

“Auto Research”这个术语在圈内争议很大。有人认为不过是超参搜索的自动版，有人相信它会演化成**“AI for AI Research”**——让Agent自己提出假设、设计实验、运行分析、得出结论。如果这件事真的发生，那么对基础设施的要求会极致化：一次性需要大量融合计算，且实验间需要高隔离度。Modal的多节点训练和沙盒组合看起来恰好为此准备。

**精华收获**

- **后训练是下一个基础设施浪潮**：微调、RL、适配器训练需要快速弹性的集群，而非大预训练集群。
- **覆盖网络（I6PN）是彩蛋式原语**：用户会用除了意图之外的方式使用它，这就是Primitive的魅力。
- **Auto Research已经内部落地**：自动推理优化证明了代理可以操作基础设施本身。

## 容量博弈：计算策略，还是金融工程？ [章节 7：GPU容量管理——从机场餐饮到航空燃料对冲]

**核心观点**

Modal组建了专职的“计算策略”团队，任务是跨不同GPU类型、不同地区、不同合约期限进行容量规划——相当于西南航空对燃油价格的对冲。

**深度阐述**

当主持人问到GPU短缺时，Akshat没有回避问题。“We've had to be much better about proactive capacity planning.”（我们必须更积极主动地规划容量。）他提到公司内部有一个团队，职务名称就叫“计算策略”（Compute Strategy）。他们的工作远不止扩缩容：需要在1年预留和3年预留之间权衡，需要预测不同GPU类型（如H100、H200、B200）在不同地区的供需曲线，还需要对供应链政见形成自己的观点并承担风险。

主持人用一个精彩的类比来理解这一切：“Airlines with fuel hedging. Southwest made a hero fuel bet and was super low cost for a long time.”（航空公司会用燃油对充，西南航空靠一次神级燃油赌注长期维持低成本。）Akshat笑着承认：“I had thought about that.” 的确，算力市场的本质就是：需求极度波动、供给受资本开支周期制约、合约结构复杂。Modal通过多提供商网络（17家云）对冲了部分供应短缺，但金融层面的决策依然挑战重重。

这个策略的一个副产品是**批处理层（Batch Tier）**：用户如果不在意延迟，可以提交一个批量计算请求，Modal在空闲时段执行并大幅降价。主持人感叹这种定价模式在业界还未被充分利用——“I feel like they're not as popular as they should be.”（我感觉它们没有受到应得的关注。）Akshat澄清，需求主要来自计算生物领域等做大批量编码工作的团队，而非主流语言模型。

**个人感受**

主持人强调自己是“infra person”，坦承基础设施领域向来枯燥，但如今变得令人兴奋：“It was boring actually for a while… and now everyone gives a crap.”（之前很无聊，现在人人都关心了。）这种从“没人管”到“热得发烫”的转变，在Akshat看来很自然：“It is a very exciting time and a lot of that’s driven by just the amount of scale all of this stuff needs.”（这是一个非常令人激动的时期，很大程度上是因为各种工作负载所需的规模。）

**延伸思考**

GPU容量管理正在成为AI公司的核心竞争力。能不能在价格波动中锁定成本，能不能在竞争对手缺卡时依然弹性供应，直接决定产品毛利率。Bubna透露出Modal正在进行的创新是：不仅管理自己的容量，还通过跨提供商资源池帮客户做“虚拟容量管理”——客户不需要签年约，也能在需要时获得自动的爆发性GPU。

**精华收获**

- **GPU容量管理是金融工程**：涉及长短约搭配、区域对冲、价格预判。
- **批处理层释放空闲容量**：极大降低成本，适合延迟不敏感的大规模任务。
- **容量本身就是差异化优势**：Modal的软件层通过多提供商池化，将弹性做到极致。

## 代理生态：Modal不做“赛车”，它造“赛道” [章节 8：平台生态——与所有代理框架共存]

**核心观点**

Modal专注于提供底层计算、存储、网络原语（尤其是沙盒），不与Anthropic/OpenAI的托管代理竞争，而是成为它们的“赛道”——任何代理框架都能在其上运行，Modal只需确保基础设施足够通用、可控。

**深度阐述**

主持人问道：“Agent everyone has one. Gemini, OpenAI, Codex… very useful for you but also like it is their way of starting to edge into your space.”（每个巨头都有自己的代理，Gemini、OpenAI、Codex…它们对你很重要，但也开始入侵你的地盘。）

Akshat的回应体现出典型的平台思维：Modal不介意哪家公司的代理框架获胜，只要它们都跑在Modal上。他提到与Anthropic的良好合作，以及对其他基础模型公司的开放态度。对Modal而言，真正的价值层是**控制平面**——用户（无论是人类还是代理）如何配置沙盒的网络、存储、安全策略、快照恢复、甚至是硬件加速器。当用户想做生产级代理（比如RAMP的会计代理），就需要更精细的控制：如何让代理访问特定文件？如何限制出站网络？如何在沙盒间共享上下文？这些东西无法在安一个“托管代理”的抽象层里解决，而需要直接操作原语。

主持人还问到了对GitPod（已转型为Ollama？实际是Warner？其实是GitPod被收购后变身OpenAI Codex Infra？从上下文看，主持人提到GitPod rebranded to “Owner”? 原字幕有“GitPod rebranded to owner. There was like this whole thing.”）的看法。Akshat很尊重GitPod团队的技术力，但指出Modal幸运地走对了市场：沙盒作为运行时环境，比开发环境（CI/CD）的粘性更强。从Docker Swarm到Modal沙盒，人们终于意识到“运行时沙盒”比“构建时沙盒”更重要。

**个人感受**

在讨论关于Agent信任边界时，主持人抛出了一个极具思辨性的观点：“Maybe the AIOS or the LLM OS is really the kernel is a goddamn LM. You make it feel uncomfortable, but that’s what frosting the LM is.”（也许AIOS或LLM OS的核心就是一个LM内核。这让你不安，但这就是LM的应用方向。）Akshat立刻接话：“You always need hard guardrails when you want to really trust it… you can pair those with softer guardrails.”（你需要硬性安全护栏，同时搭配软性护栏。）这对矛盾（硬隔离 vs LM软权限）将成为Agent基础设施的核心设计命题。

**延伸思考**

Modal没有选择做一个“Agent框架”，而是让所有Agent框架都能在它之上运行，并专门优化了CLI以供代理程序使用（例如，所有日志和指标既可读也可被程序解析）。他们甚至做了一个名为“Modal Bench”的基准测试，来发现代理在哪些地方犯错——然后以此为依据修正工具设计。这种“反身性”设计思路，也许才是代理时代基础设施的正确打开方式。

**精华收获**

- **不做代理框架，做所有代理的底层**：保持原语通用性，让市场决定哪种代理模式胜出。
- **代理需要硬安全边界**：LM软性权限还不够，硬性隔离仍是必须。
- **CLI也需为代理优化**：Modal将观测数据移到CLI层，使代理可以像人一样调试。

## 结语：回归原语，让未来自己出现 [章节 9：对未来与创始精神的反思]

**核心观点**

面对“预测代理未来会如何”的问题，Akshat的答案出奇朴素：坚持构建原语，让用户和代理自行发现用途——历史已经证明这是最好的策略。

**深度阐述**

访谈接近尾声时，主持人分享了他的观察：“You seem to have built the perfect primitive for agents to express themselves… and every extra development just involves more file system, more CPU, just the things you already have.”（你恰好为代理的自我表达构建了完美的原语……每进一步都只是更多文件系统、更多CPU——恰好是你已经有的东西。）Akshat微笑着证实：“We’re sort of just taking compute, storage, and networking and building stuff on that layer for again the stuff people need.”（我们只是用计算、存储、网络这些层来构建人们需要的东西。）

当被问及“你看到了什么别人没看到的趋势？”时，Akshat没有放出巨大的预言，而是说：“It’s clear that a huge shift is happening. One thing that’s not as obvious… the Chai Discoveries, drug discovery, computational bio, robotics…”（很明显一个大转变正在发生。一个不那么明显的趋势是……Chai Discoveries、药物发现、计算生物、机器人……）他相信这些领域会比LM本身产生更大的实际影响力。

最后他呼应了开场时提到的“开发者体验 vs 代理体验”。Modal已经推出了Modal Bench，专门针对代理使用Modal时遇到的阻力进行评估。他们发现，很多时候代理只是差一个CLI选项、一个更短的命名、或者一个更确定的错误码——而这些东西的修复，恰好和改善人类开发者体验是一致的。所以他们的结论很温和：“Same benefits apply for DX as AX.”（DX和AX享有同样的好处。）

**个人感受**

主持人最后总结：“It is really focus but also really good execution. All right. Thank you.”（你们既专注又执行得很好，谢谢。）Akshat谦逊地回应：“We have a long way to go.”（我们还有很长的路要走。）整场对话中，他的语气始终带着工程师的务实和对未知的好奇——既不夸大远景，也不回避挑战。

**延伸思考**

从“开发者体验”到“代理体验”的转变，很可能不仅影响Modal一家公司。整个云原生生态都将面临一个根本问题：当机器而非人类成为基础设施的主要使用者时，API设计、计费模式、安全模型、故障诊断工具都需要重新设计。Modal的实践给出了一条值得关注的路：承认人机并存，但遵循相同的原语。

**精华收获**

- **原语的力量**：构建通用、弹性、可组合的原语，让未来自行涌现。
- **前端性领域才是暗流**：药物发现、机器人、材料科学，比主流AI更能产生社会影响。
- **AX在细节中**：让代理也能通过CLI观测、调试、配置，这本就是对“开发者体验”的自然延展。

---

# 总结

这期Latent Space访谈，表面上是Modal CTO回顾公司的成长史，实际上是一部**AI基础设施从“容器”走向“代理原生”的思想宣言**。从自提运行时到十万沙盒问题，从推测解码开源到计算策略的金融工程，Akshat Bubna展现了一个顶级系统构建者对抽象层次和弹性之道的深刻理解。而那句“从DX到AX”的论断，很可能在几年后成为这一代云厂商兴衰的分水岭：谁能让代理像开发者一样（甚至更好地）操作基础设施，谁就能拿到未来的门票。

---

<!-- TLDR: 代理基础设施应聚焦于弹性原例，让代理像开发者一样操作计算、存储和网络，Modal用沙盒和自动缩放提供了方案。 -->
<!-- TAGS: 代理体验, 弹性计算, GPU沙盒, 推测解码, 基础设施原语 -->
<!-- RATING: 4 -->
