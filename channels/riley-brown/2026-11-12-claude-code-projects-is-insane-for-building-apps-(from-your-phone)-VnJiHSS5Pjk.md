---
title: "Claude Code Projects is INSANE for Building Apps (From Your Phone)"
channel: "Riley Brown"
published: "2026-11-12"
source_url: "https://www.youtube.com/watch?v=VnJiHSS5Pjk"
video_id: "VnJiHSS5Pjk"
tags: ["AI开发", "Claude", "无代码", "产品发布", "工作流自动化"]
rating: 4
language: "英文"
word_count: 20431
duration: "24:36"
---

# Claude Code Projects is INSANE for Building Apps (From Your Phone)

- **Channel:** Riley Brown
- **Published:** 2026-11-12
- **Source:** https://www.youtube.com/watch?v=VnJiHSS5Pjk
- **TL;DR:** 一个人+一部手机+Claude Code，一晚完成从应用到视频的全栈产品发布
- **Tags:** AI开发, Claude, 无代码, 产品发布, 工作流自动化
- **Rating:** 4

## 版本

- [结构化文稿](2026-11-12-claude-code-projects-is-insane-for-building-apps-(from-your-phone)-VnJiHSS5Pjk.structured.md)
- [原始文稿](2026-11-12-claude-code-projects-is-insane-for-building-apps-(from-your-phone)-VnJiHSS5Pjk.transcript.md)

# Claude Code Projects 深度重构：一部手机如何在一夜之间构建完整产品生态

## 材料信息

- **标题**: Claude Code Projects is INSANE for Building Apps (From Your Phone)
- **频道/来源**: Riley Brown (YouTube)
- **类型**: YouTube 视频字幕（实操演示/教程）
- **关键元数据**: 单集视频，内容涉及 Claude Code、Claude Projects、macOS 应用开发、iOS 应用开发、Blender 3D渲染、UGC视频生成、AI辅助产品发布全流程

---

## 开篇引入

想象一下：你坐在餐厅里，手里拿着手机，对着它说了几句话。几个小时后，你拥有了一个功能完整的 macOS 桌面应用、一个 iOS 移动应用、一个专业级的产品落地页、一段 37 秒的 3D 产品发布视频、以及一条用户生成内容（UGC）风格的广告片。这不是科幻小说的情节，而是 Riley Brown 在这段视频中真实展示的工作流。

Riley 通过 Claude 手机应用，利用 Claude Code Projects 配合 Opus 5.5 和 Fable 5.2 模型，在短短几小时内完成了从产品构思到完整发布素材的全过程。他构建的应用叫 Glaze——一个 Screen Studio 的克隆产品，主打屏幕录制和美化功能。但真正疯狂的不是这个产品本身，而是整个创作过程的范式转移：**你不再需要坐在电脑前写代码、画设计、剪辑视频，你只需要用自然语言描述你想要什么，然后不断给予反馈。**

这个视频的价值在于，它展示的不是一个精心策划的 Demo，而是一个真实、混乱、充满迭代和修正的创作过程。你会看到 Riley 如何管理并行任务、如何给 AI 精准反馈、如何在对 AI 生成结果不满意时逐步调整，以及最终如何在一个晚上完成了一个小型团队可能需要数周才能完成的工作。对于任何对 AI 辅助开发、无代码/低代码创作、或未来工作方式感兴趣的人来说，这是一个值得深入了解的案例。

---

## 详细内容

### 项目的启动：从手机到多线程并行的工作流 `[阶段 1：项目初始化]`

**核心观点**

Riley 通过手机上的 Claude 应用创建了一个名为"Screen Studio 2"的 Claude Project，用自然语言向 AI 下达了复杂的多任务指令：研究参考产品、设计产品方案、在多个设备上并行构建应用。

**深度阐述**

这是整个视频最基础也最重要的部分。Riley 首先在手机上打开 Claude 应用，创建了一个新的项目（Project），并命名为"Screen Studio 2"。这个命名的含义很明确——他要克隆的是 Screen Studio，一款广受好评的 macOS 屏幕录制工具。但他并不是要做简单的复制，而是要扩展它：**同时构建 macOS 桌面版和 iOS 移动版，并且放在一个 mono repo（单一代码仓库）中管理。**

Riley 的第一个 Prompt 非常关键，因为它展示了一种与 AI 协作的最佳实践——**先让 AI 做研究和规划，再批准执行**。他这样对 Claude 说：

> "Hey there Claude, we are going to basically fully clone Screen Studio directly from my phone and we're going to make a desktop app version and an iOS app version. I want these to be in a mono repo and what I want you to do is really quickly research all of the different features of Screen Studio and I want you to outline those features and then what would a mobile version of this look like?" `[阶段 1：项目初始化]`

这段话包含了几个关键要素：明确的目标（克隆 Screen Studio）、明确的产品形态（桌面版 + iOS 版）、明确的技术约束（mono repo）、明确的任务要求（研究 → 概述 → 提出移动端方案）。值得注意的是，Riley 还特别强调了他对移动端录屏的具体期望：**"I want to be able to record my screen and I want it to look really cool and have a nice outline around the phone when I do it."**（我希望能够录制我的屏幕，并且在录制时手机周围有一个好看的边框。）这为后续 iOS 应用的核心功能定下了方向。

当研究结果返回后，Riley 展现了他的工作风格——**快速审阅并授权执行**。他看了 Claude 生成的功能清单（桌面版 MVP 和 iOS 版 MVP 的功能列表），简短地评价"those features look good. I like that plan"（这些功能看起来不错，我喜欢这个计划），然后立即下达了执行指令。

但这里有一个非常重要的方法论细节：**并行工作流的启动**。Riley 要求 Claude：
1. 在他的 MacBook Pro 上开启一个**新会话**构建桌面版和 iOS 应用（聚焦核心功能，设计稍后处理）
2. **同时在另一个会话**中使用设计模式（design mode）来设计桌面版和 iOS 应用的界面
3. **又在另一个会话**中创建落地页（landing page）并部署到 Vercel

这种并行工作流是 Claude Projects 的核心优势之一——你可以在同一个项目上下文中同时管理多个独立的会话，每个会话都互不干扰地处理不同的任务。对于传统开发流程来说，这相当于同时有多个开发者在不同领域并行工作：一个负责底层功能实现，一个负责 UI/UX 设计，一个负责营销页面。而 Riley 只是一个人，拿着手机，就完成了这样的多线管理。

**个人感受**

Riley 在整个过程中的语气透露着一种从容和兴奋。他说"I'm going to fire off this prompt here"（我要发出这个提示了）的方式，像是一个指挥家在调动他的团队。然后他说"I'm just going to let AI work for 20 30 minutes. I'm going to go grab a bite to eat and I'll be back in about 30 minutes."（我就让 AI 工作 20 到 30 分钟，我去吃点东西，大约 30 分钟后回来。）这是他管理 AI 的一个核心理念：**设定好任务边界，给予充分的时间，然后离开，回来检查结果并给出反馈。**

**延伸思考**

Riley 的工作方式揭示了一个重要的趋势：AI 时代的创作者正在从"执行者"变成"创意总监"。他不再亲自写代码或画设计图，而是制定愿景、评审产出、给予方向性反馈。这种转变要求的能力不是技术实现能力，而是**系统思维、审美判断力和反馈精准度**。真正的难点不在于让 AI 工作，而在于当 AI 产出不够好时，你能否准确描述出问题所在并给出改进方向。

**精华收获**

- **先研究后执行**：在让 AI 构建之前，先让它研究参考产品并制定计划，避免方向性错误
- **并行管理多个会话**：充分利用 Claude Projects 的能力，同时推进不同维度的工作
- **设定明确的任务边界和时限**：告诉 AI 做什么、不做什么、要在什么设备上做，然后给它足够的时间独立工作

---

### 设计迭代：从 Figma 式设计板到精准的视觉反馈 `[阶段 2：设计评审与迭代]`

**核心观点**

Riley 使用 Claude 的"设计模式"（design mode）在云端设计板中查看应用的设计稿，然后给出了非常具体、可操作的视觉反馈：减少圆角、降低蓝色饱和度、增加灰色调。

**深度阐述**

在应用构建进行的同时，Riley 回到了另一个会话检查设计成果。Claude 的设计模式提供了一个类似 Figma 的设计板界面，AI 可以在这个设计板上展示它设计的桌面端和 iOS 端界面。Riley 打开设计稿后，给出了这样的评价：

> "This is looking pretty good. I like these designs here. So this is what's going to look like on desktop. You can full screen what it's going to look like on iOS. The designs are really good. Just make it slightly more minimal and make the corner radii is not as intense. It was just there's a lot of like really rounded edges. Tone that down a little bit. And then a little too much blue. I want it to be a little bit more gray, but other than that really nice job on the designs." `[阶段 2：设计评审]`

这段话是整段视频中关于设计反馈最为具体的一段。Riley 给出了三个精准的修改方向：
1. **圆形半径（corner radii）不要太极端**——让设计更简约
2. **蓝色太多了**——需要添加更多灰色调
3. 总体方向是对的，但需要调低"设计感"的强度

这种反馈方式对于 AI 协作来说非常重要。模糊的反馈（"让它更好看"）会导致 AI 做出不可预测的调整，而精准的反馈（"圆角太大，蓝色太多"）则能让 AI 明确知道要改变什么、方向是什么。

Riley 还提出了一个深层次的设计指令：让 Claude 去研究 Screen Studio 和 Rotato（另一款 3D 屏幕展示工具）的物理/光学原理。他特别提到了 Rotato 的工作方式：

> "Please do a deep research on the physics on how the designs look so good on Screen Studio. And then I also want you to look at Rotato, which is another tool. That's kind of how I want this to work. And when I record my screen on my phone, I want kind of the animation to kind of look like Rotato. It doesn't need to be as high definition. They use like 3D models or whatever. It can be like a light version of that, but that's kind of how I want it to work." `[阶段 2：设计迭代]`

这段话揭示了一个关键的工作方法：**让 AI 研究原理而非仅仅模仿表面**。Riley 不需要 AI 去复制 Rotato 的功能，而是要理解 Rotato 为什么看起来好——光线的物理表现、阴影的质感、模型的空间感——然后把这些原理应用到自己的产品中。这比简单的"让视频看起来像 Rotato"要深刻得多。

**视觉/结构信息描述**

设计板上展示的是 iOS 应用的全屏设计稿，包含手机框架、应用界面布局、以及录屏后的视频编辑界面。桌面端设计稿展示了应用在 Mac 上的全屏界面。设计稿的特点是：圆角非常明显（接近手机壳的圆润度）、蓝色调主导、整体风格偏向"现代 SaaS 应用"的典型审美。

**个人感受**

Riley 对设计的反馈展现了他对美学细节的敏感度。"Tone that down a little bit"（调低一点）、"a little too much blue"（蓝色太多了一点）——这些"一点点"的表述说明他有清晰的审美标准，知道目标应该是什么样子，而不是完全依赖 AI 的初始设计。他说"I know you're kind of working through it, but take what I said and I'm going to give you like 20 to 30 minutes to just work on this and create the app in full and make it incredibly amazing."（我知道你还在处理中，但记下我说的话，我接下来给你 20 到 30 分钟的时间把应用完整做出来，要做得极其出色。）这段话透露出他对 AI 能力的信任，也透露出一种管理者的语气。

**延伸思考**

这里有一个值得注意的细节：Riley 让 Claude 去"研究物理学"（research the physics），而不是简单地"参考 Rotato 的设计"。这种对原理的理解需求表明了 AI 辅助设计的一个重要方向：**好的设计不仅仅是视觉元素的排列组合，而是对物理规律、光学原理、用户感知等深层因素的理解**。当 Claude 理解了一束光是如何在玻璃屏幕上反射的，它才能生成真正自然的"手机屏幕反光"效果，而不是简单地叠加一个高光层。

**精华收获**

- **高质量反馈的三要素**：肯定方向、指出具体问题、给出明确的修改方向（"更少"、"更多"、"调低"）
- **要求 AI 研究原理而非模仿表面**：让 AI 理解工具为什么好，而不仅仅是好在哪里
- **给 AI 充足的时间做质量提升**：不是只给 5 分钟然后抱怨结果不好，而是给 20-30 分钟让 AI 真正深入思考和改进

---

### Convex 数据层：为什么 AI 构建的应用也需要专业的后端 `[阶段 3：赞助内容——Convex 数据库]`

**核心观点**

Riley 介绍了他构建所有 AI 应用时使用的后端基础设施——Convex，这是一个专为 AI Agent 构建应用设计的实时数据库和后端服务。

**深度阐述**

这是视频中的赞助内容部分，但 Riley 将其整合得相当自然。他的核心论点很简单：**当你用 AI 构建一个应用时，你会想要把它分享给其他人使用。这意味着数据需要在所有用户之间实时同步。** 而 Convex 正好解决了这个问题。

Riley 描述了他的典型工作流：

> "All I need to do is ask Claude Code to use the Convex plugin and ask it to build a shared dashboard that I can use on my phone and on the browser. Convex stores the data and runs the backend functions and everything is real time. So if I add something to the dashboard on my phone, it updates in the browser without me having to refresh the page." `[阶段 3：Convex 数据库介绍]`

他提到的关键优势包括：
- **实时数据同步**：手机端添加内容，浏览器端无需刷新即可看到变化
- **查询缓存**：自动处理数据查询优化
- **端到端类型安全**：帮助前端和后端之间的类型一致性，减少构建过程中的错误
- **开源组件库**：包括登录认证、AI Agent、限流等常见功能，避免从零构建

这些优势的核心价值在于：**AI Agent 可以专注于构建应用的核心功能，而不是花费大量精力搞清楚后端基础设施的配置。** Riley 特别指出："Normally, your agent would have to figure out a lot of this itself. With Convex, they can focus on the actual app."（通常，你的 Agent 需要自己搞清楚这些事情。有了 Convex，它们可以专注于实际的应用。）

**视觉/结构信息描述**

赞助内容以一段独立的段落呈现，有明确的广告标识。Riley 从应用开发的话题自然过渡到"每个 AI 构建的应用都需要一个数据库"的论点，然后介绍 Convex。结束时附带了注册链接的提示（"You can sign up with the link in the description"）。

**延伸思考**

这个赞助内容实际上揭示了一个更深层的行业趋势：**AI 原生开发工具链正在形成**。Claude Code 负责代码生成和逻辑实现，Convex 负责数据层和后端基础设施，Vercel 负责部署和托管。这些工具的组合让 AI Agent 可以像专业开发者一样使用现代技术栈来构建应用。AI 本身的编码能力固然重要，但决定 AI 构建应用质量的另一个关键因素是**它所使用的工具和基础设施的质量**。一个优秀的 AI 模型配上一个好的后端服务，能产出的结果远胜于一个模型力大但工具薄弱的组合。

**精华收获**

- **AI 构建应用也需要专业基础设施**：数据同步、类型安全、组件复用这些问题不会因为 AI 写代码就消失
- **好工具的叠加效应**：Convex + Claude Code 的组合让 AI 可以专注于应用逻辑而不是后端配置
- **Agent 友好性是下一代开发工具的关键竞争力**：工具如果能让 AI Agent 更容易使用，就比仅方便人类开发者的工具有更大的未来空间

---

### 应用测试与迭代：从"能用"到"好用"的漫长反馈循环 `[阶段 4-6：桌面应用测试、iOS 应用测试、图标设计]`

**核心观点**

Riley 测试了 Glaze 的桌面版和 iOS 版，发现了大量质量问题——低分辨率、缺乏录制悬浮层、过度光照、闪烁问题等。他通过一系列精准的反馈，逐步将应用从"勉强能运行"迭代到"真正好用"。

**深度阐述**

这部分是整个视频中最能体现 AI 应用开发现实的部分。当 Claude 首次构建完成应用后，Riley 打开了桌面版进行测试。他的第一反应相当直接：

> "My first impressions are that it looks really low quality. Like when I use Screen Studio, it's like in perfect resolution when I'm playing it back after I record. That's not the case. Also, when I record, there should be a little overlay, like showing me the time where I could actually stop it that's separate from the actual app. It's just like a little overlay. I'm sure you know what I'm talking about." `[阶段 4：桌面应用测试]`

这段反馈包含两个明确的问题：
1. **分辨率太低**：录制后的播放质量远低于 Screen Studio 的标准
2. **缺少录制悬浮层（overlay）**：这是一个独立的、浮在屏幕上方的控制栏，让用户可以在不切换到主应用的情况下查看录制时长并停止录制

这两个问题都非常具体，说明 Riley 对屏幕录制工具的实际使用体验有深刻理解。他知道一个真正的屏幕录制工具需要什么——不是花哨的设计，而是**录制过程中的控制便利性和输出质量**。

接下来他测试了 iOS 应用。这个测试过程显示了一个有趣的细节：Claude 已经将应用安装到了他的 iPhone 16 上，他只需要在主页面上找到 Glaze 图标就能使用。iOS 应用的功能是：录制手机屏幕 → 将录制导入 Glaze → 添加背景、调整内边距、控制阴影、改变帧色 → 导出到相册。Riley 第一次测试后的反馈是：

> "There's too much glare. Like the lighting effect that you have, there's just too much light and it's not super smooth. So please lower the amount of light that's being like shined on the screen. It's too much. But overall, good job. Just smooth it out. Just do a pass right now and iron it out for quality and make sure it's perfect. Really think deep. Search the internet to figure out how to do it better. Make sure it's great and then update it." `[阶段 5：iOS 应用测试]`

这个反馈再次展示了 Riley 的方法论：**肯定正确方向 + 指出具体问题 + 要求 AI 主动研究优化方案**。"Search the internet to figure out how to do it better"（搜索互联网找出更好的做法）这句话让 AI 知道它可以利用外部知识来解决问题，而不仅仅是基于已有的代码进行微调。

随着迭代的继续，Riley 发现了更多的问题：桌面应用的实时编辑会导致屏幕闪烁（"the screen flashes as I make changes"）、缩放的动态模糊太强烈（"the zoom is too intense...it does too much of a motion blur"）、iOS 应用的背景闪烁等。每一个问题他都用非常具体的描述反馈给 Claude。

在整个过程中，最有意思的是图标的迭代。Riley 让 Claude 设计一个"glazed donut"（糖霜甜甜圈）作为应用图标——这是一个巧妙的品牌命名联想（Glaze 本身就是"糖霜"的意思）。Claude 生成了四个选项，Riley 选择了第四个概念，然后要求：

> "I like the concept of four actually the most. Let's use that concept but make it better. Make like 10 variations of it. I want the edges to be rounded perfectly and and do different variations of the glaze. You're on the right track. I really like it. Make it more 3D and just got a little more zest to it, you know." `[阶段 6：图标设计迭代]`

最终他从 10 个变体中选择了"经典款"，并让 Claude 将这个图标同时更新到 macOS 应用和 iOS 应用中。

**视觉/结构信息描述**

图标设计的迭代过程展示了四个初始概念：不同设计的糖霜甜甜圈（有的带巧克力糖霜、有的带彩色糖屑等）。10 个变体在此基础上进行微调——不同的光泽度、圆润度、3D 效果强度等。最终选择的"经典款"是一个圆润的 3D 甜甜圈，带有糖霜的边缘完美圆滑。

**个人感受**

这部分展示了 Riley 这个"AI 产品经理"的真实工作状态：他发现一个又一个问题，然后不断反馈。但他始终保持着积极的态度——"Overall, good job"（总的来说做得不错）、"you're absolutely crushing it right now"（你现在做得太棒了）。在最后看到 iOS 应用导出效果时，他的兴奋是真实的：

> "Look at this. Look at how good this looks. It's a hovering phone. Absolutely insane. This like little light on the screen is not my favorite." `[阶段 6：iOS 应用最终测试]`

即使是在表达兴奋的同时，他依然没有停止发现问题（"little light on the screen is not my favorite"），这说明他对品质的要求是一种持续的状态，而不是阶段性的任务。

**延伸思考**

这个迭代过程揭示了一个重要的真相：**AI 构建的应用首次生成往往只是"能运行"的水平，距离"好用"和"精致"之间还有很大的差距。** 但关键在于，人类开发者通过传统方式填补这个差距需要数天甚至数周的调试和打磨，而 Riley 只需要用自然语言给出几轮精准的反馈就能实现。迭代速度的变化不仅仅意味着"更快"，还意味着**反馈循环的缩短让创作者能够进行更多轮的试错和优化**。当修改一个功能只需要说一句话并等待几分钟，而不是打开代码编辑器花几小时调试时，创作者会愿意把品质推向下一个层次。

**精华收获**

- **首轮产出通常只是原型水平**：不要期望第一次生成的产物就是完美可用的产品
- **问题反馈需要具体化**：低质量（分辨率不够）、缺失功能（悬浮层）、过度效果（光照太强）——每个反馈都要明确指向可操作的改进方向
- **保持积极的心态继续迭代**：每个 AI 生成的产物都有不完美之处，关键在于能否持续发现问题并有效沟通改进方向

---

### 3D 发布视频：用 Blender 和 Runpod 打造的视觉盛宴 `[阶段 7：发布视频的制作与迭代]`

**核心观点**

Riley 让 Claude 利用 Blender（本地 3D 建模与渲染软件）配合 Runpod（云端 GPU 渲染服务）创建了一段 30-40 秒的 3D 产品发布视频，展示了从 MacBook 到 iPhone 的产品使用场景。

**深度阐述**

在完成应用测试并开始第二轮迭代的同时，Riley 启动了一个全新类型的任务——3D 视频制作。他对 Claude 的指令非常详细：

> "I want you to use Blender local session on my MacBook Pro. And you can look through my recent files to see how I've done this before, but basically I want there to be like a fast movement up to a laptop to show how the app works. So like it should be a 3D render of a room that looks good and cinematic and amazing. And I actually want there to be like introducing glaze and then it should go into the MacBook and record the screen, show how you can edit it really easily. And then it is going to move over to the phone and we're going to show all of the the the main phone feature as well. And then have it end with glaze. This should be like a 30 to 40 second launch video. Make it really good and high quality and add some music to it." `[阶段 7：3D 发布视频制作]`

这段指令包含了多个层次的要求：
- **技术栈**：Blender 本地会话 + Runpod 云端渲染
- **参考素材**：让 Claude 查看 Riley 之前的 Blender 文件来了解风格偏好
- **叙事结构**：快速推进到笔记本电脑 → 展示录屏功能 → 展示编辑功能 → 转移到手机 → 展示手机端功能 → 以 Glaze 品牌结束
- **时长要求**：30-40 秒
- **质量要求**：电影感、高质量、添加音乐

当第一版视频完成后，Riley 详细审阅并给出了反馈：

> "In the beginning, like when it's doing the the screen recording, keep it a little more zoomed out, especially on the desktop app version. When I'm editing the video or recording the video and and editing the render of the video like in the demo. I want it to be a little bit more zoomed out, but the phone part looks good and then when it zooms out it looks great. Please use the icon that we used in the original one, you know, like the icon that we've come up with for our desktop app. Please use that icon instead of the like glaze icon that you have in the launch video." `[阶段 7：发布视频反馈]`

这里有两个关键问题：
1. **景别问题**：桌面应用展示部分的镜头太近（too zoomed in），需要拉远让观众看到完整的界面
2. **图标不一致**：发布视频中使用了一个通用的"glaze"图标，而不是 Riley 团队刚刚设计好的糖霜甜甜圈图标

第二个问题尤其重要，它反映了 AI 构建产品时的一个典型问题：**不同工作流之间的信息不同步**。图标是在另一个会话中设计的，而发布视频的会话可能没有访问到这个信息。这在传统团队中也是一个常见问题（设计部门和视频部门之间的沟通壁垒），但 Riley 作为项目经理通过一句简单的反馈就解决了。

最终版本的效果让 Riley 非常兴奋："Actually insane, bro"（真的太疯狂了，兄弟）。这简短的评价承载了他对整个 3D 视频视觉震撼的认可。

**视觉/结构信息描述**

视频的叙事结构：快速推进镜头进入一个电影质感的房间 → 展示 MacBook 上的 Glaze 桌面应用（使用正确的糖霜甜甜圈图标）→ 展示屏幕录制功能和编辑界面 → 镜头转移到 iPhone → 展示手机端的屏幕录制和美化功能 → 以 Glaze 品牌标识结束。视频配有背景音乐，整体风格偏向现代科技产品的广告片。

**延伸思考**

使用 Blender 进行 3D 产品视频制作是一个特别值得关注的趋势。传统上，这种高质量的 3D 动画需要专业的 3D 设计师花费数天甚至数周时间来建模、打光、动画和渲染。而通过 Claude Code 的 Blender 集成，AI 可以自动完成这些任务，Riley 只是描述了视频的叙事流程和风格要求。他特别提到了 Runpod——这是一个云端 GPU 渲染服务，用来加速渲染过程。这说明即使是 AI 生成的 3D 场景，渲染仍然是一个计算密集型任务，但 AI + 云端渲染的组合极大地减少了完成时间。

**精华收获**

- **视频制作的叙事结构需要明确描述**：从开头到结尾的镜头流程、每个部分的重点内容、品牌展示的方式
- **参考素材的重要性**：让 AI 查看你之前的文件，可以帮助它理解你的风格偏好
- **一致性管理是 AI 多任务协作的挑战**：不同会话之间需要确保关键视觉元素（如图标）的一致性

---

### UGC 广告视频：AI 化身营销专家的能力 `[阶段 8：UGC 视频创作]`

**核心观点**

Riley 要求 Claude 创建一个用户生成内容（UGC）风格的广告视频，使用 ElevenLabs 生成配音，包含字幕和关键点标注，模拟真实用户展示 Glaze 的使用场景。

**深度阐述**

在产品发布视频基本完成后，Riley 要求 Claude 再创建一个完全不同类型的营销内容——UGC 风格广告。他的指令同样非常具体：

> "This footage is actually great. Can you please use an ElevenLabs voice, just whatever ElevenLabs voice, and I want you to make a UGC video of a person reacting to it and showing a specific use case, like recording their screen on their computer and their phone and showing what they made and then come up with a good script and then create it. Use Blender as well. You can do this in a new session and then yeah, we'll be done with everything. We'll basically have our launch video and UGC video. So yeah, make this UGC video really good, fast paced, no music in the background, have subtitles and use like little arrows to point at the key parts of the video, but don't be too over the top. Make it look polished and amazing." `[阶段 8：UGC 视频创作]`

这段指令包含了 UGC 视频的所有关键要素：
- **配音**：使用 ElevenLabs 提供的 AI 声音生成
- **叙事视角**：第一人称，"一个使用者"分享他们的体验
- **具体场景**：在电脑和手机上录制屏幕，展示成果
- **技术工具**：Blender 用于可视化内容
- **风格要求**：快节奏、无背景音乐、带字幕、使用箭头标注关键部分、不过分夸张、要精致

当 UGC 视频完成后，Riley 在电脑上观看了它。视频的内容如下：

> "Okay. I just made my whole product launch video in like 5 minutes. Let me show you. This is glaze. I hit record on my Mac and just click through my site like normal. It zooms in on every click by itself. One click for a background and export. But this is the part that got me. It works on my iPhone too. I recorded my actual checkout, added a frame and a background, and it saved straight to my camera roll. Same polished look on both. It's called glaze for Mac and iPhone." `[阶段 8：UGC 视频内容]`

Riley 的反应非常强烈：

> "Oh my god, this this is crazy, dude. This is so good. Like and you know, that was one prompt, you know. I could make this really good in some in three iterations, but you know, it's 11:52. That's crazy." `[阶段 8：UGC 视频反应]`

这段话值得深读。"That was one prompt"（那只是一个提示）强调了 AI 生成内容的能力；"I could make this really good in some in three iterations"（我再用三步迭代就能让它变得非常好）说明 Riley 清楚地知道还有优化空间，但考虑到时间限制（"it's 11:52"——已经快午夜了），他对当前的结果感到满意。这展示了他作为创作者的一个务实态度：**在时间和质量之间找到平衡点**。

**视觉/结构信息描述**

UGC 视频的结构：以第一人称视角展示，开场白"我刚刚只用 5 分钟就做完了我的整个产品发布视频"——然后展示 Glaze 桌面版的录制功能（自动缩放到每次点击）、一键背景和导出、然后切换到 iPhone 端展示录屏 + 相册导出，最后以产品名称和平台信息结束。视频包含字幕和指向关键操作的箭头标注。

**延伸思考**

AI 生成 UGC 视频是一个特别有意思的现象。所谓的"用户生成内容"本来的意义是真实用户自发创建的内容，它之所以有效是因为它体现了真实性和社会证明。而 AI 生成的 UGC 视频模拟了这种真实性，但实际是由脚本和控制流程构成的。这引出了一个伦理和方法论上的问题：**当"用户生成内容"不再是真实的用户生成，它还能保留其营销效果吗？** 至少在 Riley 的演示中，这个视频的效果相当令人信服。也许我们正在进入一个"合成真实性"（synthetic authenticity）的时代，内容可以看起来非常真实并有效传递产品信息，但其"生成"过程与传统意义完全不同。

**精华收获**

- **给 AI 详细的风格指令**：快节奏、无背景音乐、有字幕、箭头标注、不过分夸张——这些细节决定了内容的风格走向
- **UGC 内容的叙事结构**：第一人称视角、具体使用场景、真实情感的模拟、产品名的清晰传达
- **接受"足够好"的产出**：当时间和资源的限制到达时，要判断当前产出的质量是否已经足够投入使用

---

### 总结与反思：手机驱动的完整产品发布 `[阶段 9：项目总结]`

**核心观点**

Riley 总结了整个项目的产出——一个功能完整的 macOS 应用、一个实用的 iOS 应用、一个产品落地页、一个 3D 发布视频、一个 UGC 广告视频——以及这些产出大约只用了 20 到 25 个提示（prompts），从一个晚上开始到午夜完成。

**深度阐述**

在视频的最后部分，Riley 将整个项目的成果做了系统的回顾。打开 Mac 上的 Glaze 应用后，他开始实际演示录制功能。桌面应用展示了跟随鼠标的缩放功能和实时编辑的界面（"It follows the mouse...it happens in real time now"）。他承认桌面应用不如 iOS 应用精致（"this is way less refined than the iOS app that we created"），但 iOS 应用的效果让他真正感到自豪：

> "This app, I would use this app unironically, especially if I need to record my screen because then we can export them and the videos look like this when they're exported. I mean, look at how they look like when they're exported here. Looks so good. Look at the animation here. Boom. Fire." `[阶段 9：iOS 应用总结]`

"Unironically"（毫无讽刺意味地）这个词非常重要——它说明 Riley 认为他所创造的是一款真正有用的产品，而不仅仅是一个技术演示。他从应用内部导出的视频展示了漂浮的手机效果、可自定义的背景、多种预设——这些功能对于一个内容创作者来说确实有实际价值。

他总结了整个过程：

> "Anyway, that's what we did in, you know, we just opened up our phone. We created a bunch of sessions in parallel using Claude code in Claude projects. This was a Claude project, and we just did this in one session. We started a few hours ago, and we just ran like, you know, I'd say like 20 to 25 prompts, and we have all of these different assets. We also created a landing page so that people could sign up. And there you go. That's what you can do now from your phone." `[阶段 9：项目总结]`

这个总结的关键数据：**一个手机、一个 Claude Project、几个小时的跨度、20-25 个提示、产出了 5 个完整的交付物。** 然后他补充了一个发人深省的观察：

> "Imagine if I spent an entire day refining all of these things. I bet you I could get that app to be very, very good. I just wanted to show you guys how powerful Claude code is right now in case any of you were skeptical about the power of these tools. I highly recommend trying Claude projects. It's just so good. Opus 5.5 just glides. It's so good. And we may get a new model soon." `[阶段 9：项目总结]`

这段收尾讲话包含了几个层次：
1. **完整性声明**：他在一个晚上做到了什么，以及如果投入更多时间能走多远
2. **说服目的**：他希望消除观众对 AI 工具能力的怀疑
3. **热情推荐**：他真诚地推荐 Claude Projects，特别称赞了 Opus 5.5 模型的流畅性
4. **期待未来**：暗示新的模型即将到来，意味着这些工具的潜力还会进一步提升

**视觉/结构信息描述**

最终展示的成品包括：
- **Glaze macOS 应用**：可以从 Spotlight 搜索打开，具备鼠标跟随缩放、实时编辑（如调整圆角半径、减少内边距、控制阴影）、光标涟漪效果、动态模糊控制、光标大小调整等功能
- **Glaze iOS 应用**：可以从应用内部直接开始录屏，导入录屏后可以调整背景色（包括紫色等）、1:1 或全屏比例、内边距、框架厚度、框架颜色、保存预设、导出到相册
- **产品落地页**：部署在 Vercel 上，以"Glaze"为品牌名，突出原始录屏和编辑能力
- **3D 发布视频**：37 秒，展示了从 MacBook 到 iPhone 的产品体验，配有音乐和品牌元素
- **UGC 广告视频**：使用 AI 配音，第一人称视角展示产品价值主张，包含字幕和视觉标注

**个人感受**

Riley 在这部分表露出了真实的满足感。他的最后一段话不仅仅是总结，还带有一种邀请："如果你们对这些工具的能力还有疑问的话，我强烈推荐试试 Claude Projects。" 这体现了整个视频的目的——不是卖课程或推广某个产品，而是分享一个让他真正兴奋的发现。从视频一开始的"we're going to be building a desktop app, an iOS app, a 3D video, a UGC video and more simply by talking to our phone"到最后"that's what you can do now from your phone"，Riley 完成了从演示到启发的完整叙事弧线。

**延伸思考**

Riley 的这个项目展示了一个重要的趋势：**"创作者经济"正在演变为"指挥官经济"**。在未来，个人能够完成的工作范围将不再受限于个人的技术技能（会写代码、会设计、会剪辑），而受限于个人的**愿景能力和管理能力**（能否清楚地描述目标、能否对产出进行准确的评价和指导、能否管理多个并行的工作流）。Riley 不是一个专业的 iOS 开发者、不是 3D 动画师、不是视频剪辑师，但他通过 Claude Projects 在几个小时内完成了所有这些角色的工作。这是一种全新的"通才"形态——不是通过掌握多门技术而成为通才，而是通过掌握与 AI 协作的能力而成为通才。

**精华收获**

- **20-25 个提示完成全栈产品发布**：从应用到视频到落地页，一个晚上可以产出一个小团队数周的工作
- **迭代能力比首轮产出更重要**：Riley 的产出物从初版到最终版经历了多次迭代，每次迭代都显著提升了质量
- **AI 工具的选择很关键**：Claude Code、Convex、Vercel、ElevenLabs、Blender、Runpod——这个工具链的组合让 AI 的产出质量得到了质的提升
- **保持好奇心和实验精神**：Riley 的核心动力是探索工具的边界，而非推出一个真正的商业产品。这种心态让他能够快速迭代并接受不完美

---

<!-- TLDR: 一个人+一部手机+Claude Code，一晚完成从应用到视频的全栈产品发布 -->
<!-- TAGS: AI开发, Claude, 无代码, 产品发布, 工作流自动化 -->
<!-- RATING: 4 -->
