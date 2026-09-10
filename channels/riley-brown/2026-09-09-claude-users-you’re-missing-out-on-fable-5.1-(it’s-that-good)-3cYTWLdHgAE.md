---
title: "Claude Users: You’re Missing Out on Fable 5.1 (It’s That Good)"
channel: "Riley Brown"
published: "2026-09-09"
source_url: "https://www.youtube.com/watch?v=3cYTWLdHgAE"
video_id: "3cYTWLdHgAE"
tags: ["AI编程", "Vibe Coding", "Claude Code", "Agent原生应用", "实时数据库"]
rating: 4
language: "英文"
word_count: 30584
duration: "25:03"
---

# Claude Users: You’re Missing Out on Fable 5.1 (It’s That Good)

- **Channel:** Riley Brown
- **Published:** 2026-09-09
- **Source:** https://www.youtube.com/watch?v=3cYTWLdHgAE
- **TL;DR:** 复制一段技能粘贴给任何Agent，一个提示词生成实时协作看板
- **Tags:** AI编程, Vibe Coding, Claude Code, Agent原生应用, 实时数据库
- **Rating:** 4

## 版本

- [结构化文稿](2026-09-09-claude-users-you’re-missing-out-on-fable-5.1-(it’s-that-good)-3cYTWLdHgAE.structured.md)
- [原始文稿](2026-09-09-claude-users-you’re-missing-out-on-fable-5.1-(it’s-that-good)-3cYTWLdHgAE.transcript.md)

# 四条提示词造出一个实时协作看板：当 Claude 的编程能力遇到"Agent 原生"应用

## 材料信息

- **标题**：Claude Users: You're Missing Out on Fable 5.1 (It's That Good)
- **作者/来源**：Riley Brown（YouTube 频道）
- **类型**：YouTube 视频字幕（连续文本，未附带官方时间戳与章节划分）
- **关键元数据**：
  - 视频主题：用 Claude 桌面版 + Claude Code + Fable 5.1 模型，从零构建一个"Agent 原生"的类 Trello 业务看板，并部署到互联网
  - 涉及工具链：Claude Desktop、Claude Code、Convex（实时数据库，视频赞助商）、Vercel（部署）、GitHub
  - 涉及定价信息：Claude Max 计划 100 美元/月、Max 20X 计划（本视频作者使用的方案）
  - 模型时间点：作者称 Fable 5.1 是"截至 9 月 3 日全世界最好的编程模型"，同时提到 GPT-6 即将发布的传闻
  - 出现的人物/账号：Riley Brown（真人用户，riley@agentnative.inc）、Jacob（第二个人类测试账号）
  - 出现的 AI Agent：Grokbot、Codex（ChatGPT）、Claude、被含糊提到的"Jimmy bot"
- **转录说明（重要）**：本字幕为自动转录稿，存在若干明显的听写误差。例如"Jimmy bot"高度疑似为"Gemini bot"，"Fable 5.1"这一模型名称的拼写也存在转录不确定性（自动字幕对专有名词的识别常不稳定）。此外，字幕中没有可供精确引用的时间码，因此下文的"位置标识"均按**内容顺序划分的段落标记**给出，而非真实时间戳。文中所有数字、名称与说法均严格依据字幕原文，不确定处已明确标注。

---

## 开篇引入

这不是一期"AI 工具测评"，而是一场全程无剪辑感的**建造实录**。

作者 Riley Brown 在这段视频里做的事情，说起来简单、做起来惊悚：他不写一行代码，只靠打字，就让一个 AI 从零生成了一款**拥有前端界面、后端逻辑、实时数据库、用户登录系统，并且最终部署上线到公网的真实业务应用**。而且这款应用不是玩具——它是一个"Agent 原生的 Trello"，一个能让人类员工和多个不同平台的 AI 智能体**同时、实时、互不冲突地协作**的业务看板。他在视频结尾用自己的真实业务做了收尾演示：让 AI 把整个看板清空，然后根据它对作者业务的了解重新组织内容，并在笔记本里留下备注。

更让人坐不住的是开头的那个小炫技：他用**四个提示词**做出了一个《使命召唤》游戏——但随即话锋一转，"今天我们其实不聊游戏"。真正的野心在别处。

这段内容的价值，不在于"又一个 vibe coding 演示"，而在于它完整暴露了一套**可复制的工作流**：提示词怎么写、模型怎么选、失败怎么修、Agent 怎么接入、应用怎么上线。你会看到一个真实的、包含等待、卡壳、报错、返工的全过程——而不是剪辑掉一切痛苦的宣传片。这正是它比大多数"AI 编程"内容更有价值的地方。

下面，我们按内容推进的顺序，逐段还原这次建造的全部细节。

---

## 详细内容

### 一、开场：先亮出"最强大脑"，再宣布真正的目标 `[段落 1]`

**核心观点**
作者宣称 Anthropic 刚刚发布了"全世界最好的编程模型"，并用一个四提示词做出的游戏作为能力背书，但随即声明本期真正要做的是：为真实业务构建一个可部署上线的完整应用。

**深度阐述**

视频一开始，作者就抛出一个极具冲击力的论断：

> "Anthropic just released the best coding model in the world."
> （Anthropic 刚刚发布了全世界最好的编程模型。） `[段落 1]`

这个模型在字幕中被转录为 **"Fable 5.1"**。需要说明的是，这是自动字幕的拼写，作者实际所说的模型名称可能存在听写误差，但从上下文（Anthropic、9 月 3 日发布、被称为最强编程模型、需要付费额度）可以确定这是 Claude 家族的一个新版本。这一点请读者自行核实时效性——毕竟视频里的作者自己都在同一段话里承认，GPT-6 的传闻可能很快就会改写这个排名：

> "GPT-6 is rumored to come out very soon as I'm making this video, so they could be really close."
> （在我录制这个视频的时候，有传闻说 GPT-6 很快就会发布，所以两者可能非常接近。） `[段落 1]`

为了"快速证明这个新模型有多强"，作者做了一件很有视频博主风格的事：**只用了四个提示词，就做出了一个《使命召唤》游戏**。这是一个精心设计的开场钩子——它让观众在 30 秒内就建立起对模型能力的信心，同时也暗示了接下来的内容会更"实用"。

紧接着就是那个关键的转折句："But we're actually not talking about games today."（但我们今天其实不聊游戏。）

真正的目标是：**一个不需要任何编程经验就能构建的真实应用**。而且这个应用不是随便什么应用，作者对它的定义是野心勃勃的三层：

1. 一个**自主管理他整个业务**的仪表盘（dashboard）
2. 一个**实时更新**的系统
3. 一个**不只他自己能改、他的 AI Agent 也能改**的协作空间——具体点名了 Codex 和 Grokbot 这两个智能体

**延伸思考**

这个开场其实透露了一个正在发生的变化：AI 编程演示的"炫技门槛"正在飞速抬高。一年前，能生成一个可运行的贪吃蛇游戏就足够惊艳；今天，游戏已经沦落到"只配当开头 20 秒的暖场"。真正被视作能力证明的，是**能跑在公网、有数据库、有权限体系、能被多个智能体并发写入的生产级应用**。观众的胃口被养刁了，这是好事。

**精华收获**

- 看到任何"最强模型"的宣称，先看它被要求完成的任务难度；游戏 demo 和业务系统的难度不是一个量级。
- 作者在赞美新模型的同一句话里就承认了竞争模型即将到来的可能性——这种"不把话说死"的表述，比纯粹的吹捧更值得信任。

---

### 二、工具定位：桌面版、Claude Code 与"看起来很吓人"的界面 `[段落 2-4]`

**核心观点**
明确区分 Claude 的三种使用形态（Chat、Cowork、Claude Code），并安抚非技术用户：Claude Code 的界面虽然看起来专业晦涩，但所有必要的东西作者都会解释清楚。

**深度阐述**

作者首先做了一个对非技术观众非常友好的分层说明。他指出现有的 Claude 用户大概分成两类使用习惯：

- 使用**聊天版（Chat）**，或者**协作版（Cowork）**——字幕中为 "co-work version, Claude and Claude co-work"，这通常是面向非技术用户的产品形态；
- 而本期视频使用的是**Claude Code**，一个面向开发者的界面。

作者非常坦率地承认了这个界面的"劝退感"：

> "Claude Code seems a little bit intimidating at first, right? You see this stuff that you may not recognize. Local agent native landing, what is that? Main work tree, it's all good."
> （Claude Code 乍一看确实有点吓人，对吧？你会看到一些你根本不认识的东西。比如"local agent native landing"这是什么鬼？还有"main work tree"……别慌，都没问题。） `[段落 2]`

这段自嘲式的翻译极其重要——它暴露了 vibe coding 普及过程中最大的心理障碍：**不是能力问题，是界面陌生感带来的恐惧**。作者的处理方式是直接点破它："I'll explain everything that you need to know to get started vibe coding."（我会把开始 vibe coding 所需知道的一切都解释给你。）

**技术栈定位清晰**：Claude 桌面应用 → Claude Code → Fable 5.1 模型。这是一个"套娃"式的三层结构，作者特意把它讲清楚了，因为很多初学者搞不明白"我到底在用什么"。

**个人感受**

作者在这里表现出的是一种"过来人"的体贴。他没有假装这些术语不重要，也没有用术语来建立专业壁垒，而是主动站到观众的位置上："你看到这些会懵，我懂，因为我当初也是。"这种姿态在技术内容创作者中并不常见，却是让新手愿意留下来的关键。

**延伸思考**

一个耐人寻味的现象是：AI 工具正在快速"专业界面化"。当普通用户还在用聊天框的时候，真正能释放模型全部能力的入口，已经变成了带有文件树、终端、项目目录的**开发环境**。这意味着"AI 平权"可能并不是均匀发生的——它先让每个人都能"说"，但要让 AI 真的"做出一整个产品"，用户仍需跨越一道界面门槛。作者正在做的，就是搭一座桥。

**精华收获**

- 分清你在用 Claude 的哪种形态：聊天、协作、还是 Claude Code。它们的能力上限差别巨大。
- 不要被专业界面吓退。界面上 90% 的陌生词汇，对"完成一个应用"这件事来说都是无关信息。

---

### 三、成本与用量：Max 计划、每周配额与"75%" `[段落 3]`

**核心观点**
Fable 5.1 是一个昂贵的高端模型，只有 Max 及以上订阅套餐才包含用量额度，否则按量付费；作者使用的是 Max 20X 计划，并在视频进行到此处时已经用掉了 75% 的每周额度。

**深度阐述**

这是全片最"务实"、也最容易被观众忽略的关键段落。作者毫不含糊地把钱的问题摆到了台面上：

> "If you do not have at least the Max plan, which is $100 per month, it will be paid usage as soon as you start using it, and this model is pretty expensive."
> （如果你没有至少订阅每月 100 美元的 Max 计划，那你一开始使用它就会变成按量付费，而**这个模型相当贵**。） `[段落 3]`

接着他描述了自己的实际使用体验：

- 他使用的是 **Max 20X 计划**
- 在过去 3 天里**大量使用** Claude
- **尚未触达每周上限**

然后他打开用量指示器做了一次实时检查：**"75% of the way through my weekly Fable limits"**（每周 Fable 额度的 75% 已经被用掉了）。

并且，他做了一个非常"博主式"的承诺：

> "If we reach our limits in this video, I will pay for more Fable credits."
> （如果我们在视频里用超了额度，我会自己掏钱买更多 Fable 额度。） `[段落 3]`

因为"我们即将创造一个疯狂的应用"（we're about to create such an insane app）。这句话既是承诺，也是一个隐性的成本预告：**这个演示的代价可能不低**。

**关键数据完整呈现**

| 项目 | 内容 |
|---|---|
| 最低包含额度的套餐 | Max，100 美元/月 |
| 作者使用的套餐 | Max 20X |
| 使用模式 | 三天高频使用，触发每周额度上限机制 |
| 视频进行到此处时的额度消耗 | 每周 Fable 额度的 75% |
| 超额处理方式 | 按量付费 / 购买额外 credits |

**延伸思考**

这段内容其实揭示了一个常被"AI 编程狂欢"叙事掩盖的现实：**能力的定价正在分层**。同一个模型，付费用户拿到的是流畅的构建体验，免费或低配用户拿到的可能是"每次提示都要掂量一下"的稀缺体验。当"AI 帮你写一个完整应用"成为可能，它的隐含成本不再是一杯咖啡，而可能是一个月的生活费级别。

这也解释了为什么"提示词工程"在高端模型上反而变得更重要：既然每一次调用都昂贵，那么**一次说清楚所有要求**就变成了省钱技巧。这正好铺垫了后面作者那套"把所有问题塞进一个提示词"的方法论。

**精华收获**

- 在开始一个 vibe coding 项目之前，先确认你的套餐和额度，避免做一半被限额掐断。
- "把多个修改需求合并成一次提示"不只是效率技巧，在高端模型上更是成本控制手段。

---

### 四、需求定义：什么是"Agent 原生"的 Trello？ `[段落 5-6]`

**核心观点**
作者要构建的不是 Trello 的复制品，而是 Trello 的**Agent 原生版本**——一个让 AI 智能体成为一等公民、能自主添加卡片、留评论、并留下可追溯身份记录的业务看板，同时附带一个反映业务状态的侧边仪表盘。

**深度阐述**

这是全片思想含量最高的一段。作者非常清楚自己要解决的是什么问题：

> "Trello right now, you can use yourself. You can add your team members, but it's not meant to be used with agents."
> （现在的 Trello，你可以自己用，也可以把团队成员拉进来，但它**不是为与 Agent 协作而设计的**。） `[段落 5]`

这句话点出了一个极其重要的产品洞察：**现有一代 SaaS 工具的设计假设是"人类是唯一的操作者"**。所有的权限模型、通知机制、活动日志，都是围绕"张三改了这张卡片"设计的。但当你的团队里混进了一批 AI 智能体，这个假设就崩了。

于是作者列出了他要的核心功能：

1. **侧边仪表盘**：显示业务的"重要更新"（important updates for our business）
2. **任何 Agent 都能更新看板并添加评论**——他点名了 Grokbot 和他的"Jimmy bot"（极可能是 Gemini bot 的听写误差）
3. **所有操作全程可追溯**：

> "If Jimmy adds something to the board, it should say that Jimmy added it to the board."
> （如果 Jimmy 往看板上加了东西，那它就应该显示是 Jimmy 加的。） `[段落 5]`

4. **跨平台一致性**：无论是从 Claude、从 Codex，还是任何其他 Agent 操作，都应该能更新和编辑同一块看板

**这一段最关键的技术洞察，是作者对"Agent 有上下文"的论证**：

> "Because all of my agents are connected through these plugins up here, right? Connectors. My agent has context over my entire business. Email, Slack, text messages. Codex can read my text messages, calendar, everything. So, in theory, my agent should be able to keep a dashboard fully up-to-date."
> （因为我所有的 Agent 都通过上面这些插件——也就是 Connectors——连接起来了。我的 Agent 掌握着我整个业务的上下文：邮件、Slack、短信。Codex 能读我的短信、日历，一切。所以理论上，我的 Agent 应该能让这个看板始终保持最新状态。） `[段落 5]`

**这是一条完整的逻辑链**：

Agent 已接入我的全部业务数据源（邮件/日历/短信/Slack） → 因此 Agent 知道我的业务正在发生什么 → 因此 Agent 有能力自动维护一块业务看板 → 但问题是，**现有工具没有给 Agent 提供写入口** → 所以需要一个"Agent 原生"的看板。

这个论证的精妙之处在于：他没有在发明需求，而是在**补上一个已经被架好、只差最后一块拼图的链条**。Agent 们早就能"读"了，现在缺的是"写"。

**延伸思考**

"Agent 原生"（agent-native）这个词值得单独立碑。它对应着软件史上的几次范式转移：从 desktop-native 到 web-native，从 web-native 到 mobile-native。每一次转移都不是"给旧软件加个新外壳"，而是**重新假设谁是使用者、谁在什么场景下使用**。

如果 Agent 成为软件的常驻使用者，那么一整套设计原则都要重写：

- 身份系统要怎么处理"一个 Agent 属于一个人类"的归属关系？
- 活动日志要怎么区分人类操作和 Agent 操作？
- 冲突解决机制要如何设计（两个 Agent 同时修改一张卡片）？
- 权限要如何授予才能既安全又不需要人类逐个审批？

作者在这段视频里给出的，正是这些问题的一个早期答案。

**精华收获**

- 思考你的产品/工具时，问一句："如果我的用户里有 AI Agent，现在的设计还成立吗？"
- "Agent 原生"的核心不是加个 API，而是承认 Agent 是**有身份、有归属、有行为记录**的一等公民。

---

### 五、提示词解剖：一份可复用的 App 构建模板 `[段落 6-7]`

**核心观点**
作者完整展示了他构建任何应用时都会使用的提示词结构：平台 → 相似应用参照 → 用户流程 → 设计风格 → 数据库选择。这是一份可以直接抄走的模板。

**深度阐述**

作者一边念自己的提示词，一边点明"这是我做任何应用时都会加进来的东西"。我们把它拆解成五个模块，这是全片最可迁移的部分。

**模块一：平台（Platform）**

> "The first thing that I always include in the prompt is the platform. So, I want to build a web app. This is not a desktop app or an iOS app."
> （我放进提示词的第一件事永远是平台。所以，我要构建的是一个 Web 应用，不是桌面应用，也不是 iOS 应用。） `[段落 6]`

这是一个极容易被初学者忽略、但对结果影响巨大的约束。不说清楚，模型可能会给你生成一个 Electron 桌面应用，或者一个 React Native 移动端项目——然后你所有的后续努力都白费。

**模块二：参照物（Similar Apps）**

> "This app should feel like Trello with all the different fields."
> （这个应用的感觉应该像 Trello，有那些不同的字段。） `[段落 6]`

用"像 X 一样"来描述产品，是给模型最高效的信息压缩方式。一句话就传递了：看板结构、卡片、拖拽、列表、多列布局、卡片详情页……模型对 Trello 的理解，比任何一段形态学描述都精确。

作者甚至细化了参照的维度：

- 打开一张卡片时，评论要**按时间从新到旧排序**
- 评论要显示是谁留的
- **Agent 的评论也要显示 Agent 的名字**

**模块三：用户流程（Flow）**

> "User or someone from my team would sign in with their email. We want sign in. Users can add, move, delete, and edit items on the board. When they do, it's their name. They are the creator of that item."
> （用户或我的团队成员用邮箱登录。我们需要登录功能。用户可以添加、移动、删除、编辑看板上的条目。操作之后，显示的是他们的名字——他们就是那个条目的创建者。） `[段落 6]`

这段里藏着一个非常自然的"身份归属"设计：**谁创建，就记谁的名**。这看起来简单，但它正是"可追溯性"的最小实现。

接着是最关键的 **Agent 账号设计**：

> "This app will be agent-native. Each person will be able to copy a skill which will have the necessary keys to allow their agents to edit the board. Agents will be instructed to create an account on first try as like 'Riley's agent.' And I want to include 'Riley's agent' should be connected to Riley's agent account. So, there should be agent accounts and human accounts."
> （这个应用将是 Agent 原生的。每个人都能复制一个 skill，里面包含了允许他们的 Agent 编辑看板所需的密钥。Agent 会被指示在首次尝试时创建一个账号，比如叫"Riley 的 agent"。我还要求"Riley 的 agent"应该与 Riley 的账号相关联。所以，应该同时存在 **Agent 账号和人类账号**。） `[段落 6]`

**"Agent 账号 + 人类账号并存，且 Agent 归属于人类"**——这是一个可以直接被无数产品抄走的设计模式。它一次性解决了三个问题：权限隔离、行为归属、以及用"复制 skill 里的密钥"这种极简方式完成授权。

**模块四：设计风格（Design）**

> "For the design, we're going to make it minimal with a slight military vibe to it. I don't know what I mean by this. We can iterate on it later. It's just like what came to my mind here."
> （设计上，我们要做得极简，带一点点军事风。其实我自己也不知道我是什么意思，我们后面可以迭代。这只是我脑子里冒出来的东西。） `[段落 6]`

这段"我不知道我什么意思"极其真实，也极其有用。它示范了一个重要的 vibe coding 心态：**不要在设计阶段卡住**。先扔一个模糊的形容词进去，拿到第一版，再靠"我不喜欢这个"来迭代。作者在后来也确实把"军事风"亲手否掉了——这证明了"先模糊后修正"是完全可行的路径。

**模块五：实时与动画**

> "When something new gets added in real-time, please make a 5-second slight animation showing that it updated."
> （当有新东西被实时添加进来时，请做一个 5 秒的轻微动画，表示它更新了。） `[段落 6]`

作者解释了这个需求的来源：

> "I'm picturing like a military dashboard. As something happens, we see it show up on the board and that it should be cool-looking."
> （我脑子里的画面是这样的：像军事仪表盘一样，一有事情发生，我们就能看到它出现在看板上，而且看起来很酷。） `[段落 6]`

**模块六：数据库（Database）**

> "For the database, we are going to be using Convex. Convex updates the database in real-time."
> （数据库我们使用 Convex。Convex 会实时更新数据库。） `[段落 6]`

这一点是整条技术链的枢纽——**因为数据库是实时的，所以多 Agent 协作的体验才是无刷新、即时可见的**。

**精华收获（提示词模板）**

```
1. 平台：Web / 桌面 / iOS / 移动端
2. 参照物：像 XX 一样 + 具体到某个交互细节
3. 用户流程：谁能登录、能做什么操作、操作后如何署名
4. Agent 设计：Agent 账号如何创建、如何归属人类、如何授权（skill + key）
5. 设计风格：先用模糊形容词，后续迭代
6. 交互反馈：动画时长、音效、触发条件
7. 数据库：选型 + 明确它的关键特性（如实时同步）
```

---

### 六、开工：新建文件夹，粘贴提示词，二十分钟的等待 `[段落 7-8]`

**核心观点**
工作流的第一步极其朴素：在 Claude Code 里新建一个本地文件夹，粘贴提示词，运行，等待。

**深度阐述**

作者的操作步骤几乎是"反高潮"的简单：

1. 打开 Claude Code
2. 点击"打开文件夹"（open folder）
3. 在**下载文件夹**里新建一个文件夹，命名为 `Agent Native Trello`
4. 打开它——Claude Code 现在在这个文件夹里运行
5. 粘贴提示词
6. 运行

值得注意的细节：他把项目建在"下载文件夹"里。这说明**vibe coding 的第一步不需要任何工程化的目录结构规划**。项目就在你随手放的地方，模型会处理剩下的。

然后就是等待。作者在这个间隙说了一句：

> "It's still working. We're 20 minutes in, and it should be done soon. I'm really excited for this."
> （它还在工作。我们已经过了 20 分钟了，应该快好了。我真的很期待。） `[段落 8]`

**"20 分钟"**这个数字很有价值。它给了观众一个预期锚点：在这个模型上，从零构建一个带前后端和数据库的应用，**首次生成的时间量级是 10-30 分钟**——足够你去泡杯咖啡，但不足以去吃顿饭。

**个人感受**

作者在这里的语气是纯粹的孩子式兴奋——"I'm really excited for this."（我真的很期待这个。）他并没有把这段等待剪掉，反而保留了它。这是一种诚实：**AI 编程不是瞬时的魔法，它包含真实的等待**。而这种等待和人类程序员敲代码时的等待，在情绪上是完全不同的：不是焦虑，是期待。

**精华收获**

- 项目目录可以随手创建，不必纠结工程规范——把精力放在提示词上。
- 首次生成的等待时间属于正常范围，不要在 5 分钟没结果时就放弃。

---

### 七、广告插播：为什么是 Convex？ `[段落 7 中段]`

**核心观点**
Convex 作为实时数据库，解决了多 Agent 协作场景下"数据一致性 + 实时同步"的工程难题，并提供面向 AI Agent 的现成组件。

**深度阐述**

作者在等待期间自然地过渡到了赞助商段落，但这段内容本身含有真实的技术价值，值得完整还原。

先说的是一般性需求：

> "Every real business app that I make needs somewhere to store information and keep it accurate for everyone using it."
> （我做的每一个真实业务应用都需要一个地方来存储信息，并保证它对每个使用者来说都是准确的。） `[段落 7]`

然后是它在这个特定场景下的必要性：

> "For this dashboard, Claude Code and all the other agents write to the same database. And if I switch agent platforms, I can easily get that agent to write to the same database as well."
> （对于这个看板，Claude Code 和其他所有 Agent 写入的是同一个数据库。而如果我换了一个 Agent 平台，我也能让那个 Agent 轻松写入同一个数据库。） `[段落 7]`

**这正是"Agent 原生应用"的工程内核**：人类换工具、Agent 换平台，但**数据必须只有一个真相来源**（single source of truth）。

接着，他指出了一个普通开发者容易低估的工作量：

> "Normally, an agent would have to build a real-time syncing, caching, and rules to keep the data consistent. If you plug into Convex, it's much easier."
> （通常情况下，一个 Agent 得自己去实现实时同步、缓存，以及保持数据一致的规则。如果接入 Convex，这就容易多了。） `[段落 7]`

最后列出了 Convex 提供的**面向 AI Agent 的可复用组件**：

- 登录（login）
- 速率限制（rate limiting）
- 动作缓存（action caching）
- AI Agent 相关组件

以及一个对 Agent 来说特别有价值的特性：

> "The plugin can also see the app structure, logs, backend functions, so Claude Code can understand and maintain the entire app."
> （这个插件还能看到应用结构、日志、后端函数，所以 Claude Code 能理解并维护整个应用。） `[段落 7]`

**这一点是真正的关键**。它意味着 AI 不只是"生成一次代码就走人"，而是**能持续地理解自己造出来的东西**——这在后续迭代中至关重要，因为作者接下来要反复地"看一眼、提要求、改一版"。

**延伸思考**

这段广告揭示了一个不太被讨论的趋势：**AI 编程时代，基础设施的选择标准变了**。过去我们选数据库看性能、看成本、看生态；现在还要加一条——**看它对 AI Agent 是否友好**。一个需要人类写 500 行配置才能接通的数据库，和一个"Agent 读一眼就能理解并维护"的数据库，在新的开发范式里完全不是同一个物种。

**精华收获**

- 多 Agent 协作的前提是单一数据源 + 实时同步，不要指望 Agent 自己实现这套工程细节。
- 选技术栈时新增一个维度：这个工具/服务是否对 AI Agent 友好（可发现、可理解、可维护）。

---

### 八、验收第一版：数据库里都长出了什么 `[段落 9]`

**核心观点**
第一次生成完成后，作者的第一件事不是试用界面，而是**检查数据库**——确认模型是否真的建立了合理的表结构和权限体系。

**深度阐述**

生成完成后，作者看到的是一个登录页面，以及一个 Convex 的链接。他的第一反应是打开 Convex 的控制台，进入 **Data / Schema 标签页**，逐张表地检视。

这里必须完整还原他看到的东西，因为这是一份**模型自动设计的数据模型说明书**：

| 表名 | 包含字段（字幕中可见） | 说明 |
|---|---|---|
| **cards** | assignees（负责人）、comment count（评论数）、created by（创建者）、description（描述） | 看板卡片的完整实体 |
| **comments** | — | 评论 |
| **todos** | — | 待办事项 |
| **rate limits** | — | **速率限制**（作者特意称赞："It added rate limits, which is really cool."——它加了速率限制，这真的很酷。） |
| **notes** | 每一条都有 author（作者） | 笔记，即后文那个"笔记本"功能 |
| **agents** | name（名称）、owner ID（归属者 ID） | **每个 Agent 都有一个拥有者**——作者点评："This is looking good."（看起来不错。） |
| **users** | — | 人类用户 |
| **auth accounts** | — | 认证账号 |

作者的简短评价是：

> "It added a lot of things on the database side using Convex."
> （它在数据库层面用 Convex 加了很多东西。） `[段落 9]`

**值得注意**：**"rate limits"表的自动出现**是一个被作者特意点名的亮点。这说明模型不只是"实现你要求的功能"，它还主动补齐了生产能力——比如防止 Agent 疯狂写入拖垮系统。同时 **"agents 表带 owner ID"** 正是他提示词里"Agent 账号归属于人类账号"那一条需求的落地证明。

紧接着是**实测登录**：

1. 应用此时运行在本地
2. 作者创建账号：`Riley Brown` / `riley@agentnative.inc`
3. 设置密码
4. 登录成功
5. **验证数据库确实写入了**——他切回 Data 标签，看到 `users` 表里出现了 `riley@agentnative.inc`

> "We have one user of this app. It is entering the database. And it's doing so in real time."
> （这个应用现在有一个用户了。它正在进入数据库，而且是实时进入的。） `[段落 9]`

另外，作者提到"我们稍后可以加一个邮箱验证步骤"，说明当时的注册流程还是即时的、无需验证的。他还顺便吐槽了界面"有点难看清，我待会改"——这为后面的返工埋了伏笔。

**延伸思考**

这里有一个非常重要的**验收方法论**：作者检查 AI 产出的第一个动作不是点击界面，而是**直接查看数据层**。这背后是一种老练的判断——界面可以修，风格可以调，但如果数据模型设计烂了，后面所有的迭代都会建立在流沙上。

**精华收获**

- AI 生成应用后，先审数据库 schema，再审界面。
- 注意观察模型有没有"多做一步"：主动加上速率限制、归属关系这类你没明说但生产环境必需的东西——这是判断模型成熟度的好信号。

---

### 九、灵魂操作：复制一个 Skill，粘贴给另一个 Agent `[段落 10-11]`

**核心观点**
应用内置了一个 "agent.md" 技能文件，把它复制粘贴给任何其他平台的 AI Agent，该 Agent 就能自主注册账号并直接操作看板——无需任何额外配置。

**深度阐述**

这是整期视频里最有"啊哈时刻"的部分，也是"Agent 原生"这个概念从抽象变成现实的关键一步。

作者的操作流程：

1. 点击应用里的按钮，看到一个 **`agent.md`** 文件
2. **复制这个 skill**
3. 打开 Grokbot，新建一个机器人，命名为 `dashboard bot`
4. 直接把 skill 粘贴进去，告诉它"你来更新这个"
5. 然后说："When done, please add a card to the database which says hello and state your name."（完成后，请往数据库里添加一张卡片，说"你好"，并署上你的名字。）

**结果**：

> "Oh, wow, look at that. My agent added it. Let's go. Hello from dashboard bot."
> （哇，快看。我的 Agent 把它加进去了。太好了。来自 dashboard bot 的问候。） `[段落 10]`

**从数据库侧验证**：

作者切回 Convex 的 `agents` 表，发现确实新建了一条记录，但名字是 **"Riley's cursor"**——他解释说，因为 Grokbot 由 Cursor 提供，所以显示成这样，并认为这完全没问题。

紧接着作者做了一个很有洞察力的**设计取舍说明**：

> "Since all these agents share a skill, we don't really want to give them all different skills. So now any agent in here actually can leave a comment on the board. It just won't show up as dashboard bot, which I think for the sake of this is actually fine."
> （因为这些 Agent 共享同一个 skill，我们其实不想给它们每个都发不同的 skill。所以现在这里任何 Agent 都能在看板上留评论，只是不会显示成 dashboard bot —— 我觉得就这个场景而言完全没问题。） `[段落 11]`

**这段话暴露了一个真实的设计权衡**：共享 skill 意味着操作简便，但代价是**身份粒度变粗**。作者判断"这一个 Grokbot 就够了，我不需要多个 Grokbot 来更新它"——这是一个务实的、基于实际使用场景的取舍，而不是教条式地追求完美架构。

**接下来是一场真正的多 Agent 压力测试**：

1. 作者切到他的**主 Grokbot**，说："using agent native board, add the things I should be working on."（使用 agent native board，把我现在应该在做的事情加进去。）

2. 结果：

> "Oh, there we go. It just added all of these... It added these items to the board. Grok Bot long form, film, how ready is your site for AI agents, film agent email."
> （哦，来了。它把所有这些都加进去了……它把这些条目加到了看板上：Grok Bot 长视频、拍摄、你的网站对 AI Agent 有多友好、拍摄、Agent 邮件。） `[段落 11]`

3. 然后作者加了一个新列，说："Please take the key items from details and add it to the latest column that I created."（请把详情里的关键条目提取出来，加到我刚创建的那一列里。）

4. 结果：**"Oh, there it is. Here we go. This is awesome."**（哦，成了。来了。太棒了。）

5. 甚至连**分类标签**都被自动加上了："video, email deadline, email ops"（视频、邮件截止日期、邮件运营）

**个人感受**

作者在这几段里连续用了 "This is awesome"、"This is pretty cool"、"This is really cool"——他的兴奋是真实的、反复的、不克制的。而这种兴奋的源头值得玩味：**他兴奋的不是 AI 会写代码，而是 AI 之间能协作**。他刚刚亲眼看到两个不同平台的 Agent，通过一个自己敲了几行文字就生成出来的应用，实现了跨系统的业务协同。这是一个比"代码生成"更高维度的成就感。

**延伸思考**

"复制一个 skill 文件 → 粘贴 → 你的 Agent 就能接入了"——这个交互模式的美感在于它**把 API 集成这个传统的工程难题，压缩成了一次复制粘贴**。没有 OAuth 配置界面，没有 API 文档阅读，没有 SDK 安装。

但这也引出一个值得深思的安全问题：这个 skill 文件里包含了"允许编辑看板所需的密钥"。这意味着**任何拿到这个文件的人（或 Agent）都能写入你的业务数据库**。作者在视频里没有深入讨论这一点，但这是任何想把此模式投入生产的人必须自己回答的问题。

**精华收获**

- "Agent 接入"的终极形态可能不是 API 文档，而是**一段能被 Agent 自己读懂并执行的技能说明书**。
- 共享凭证 vs 独立身份，是一个需要根据场景权衡的取舍，不存在唯一正确答案。
- 真正的"Agent 原生"体验，是你可以用自然语言指挥 Agent 操作另一个系统，而它真的做到了。

---

### 十、六项自检清单与一次大型返工提示词 `[段落 12-13]`

**核心观点**
第一版跑通后，作者按一套固定的六项清单检视应用，然后把**所有问题塞进一个提示词**一次性交给模型——因为他认为模型在排序和解决顺序上比自己更聪明。

**深度阐述**

这是全片方法论密度最高的段落之一。

**先看他的核心理念**：

> "These are kind of the main six things that I look at after I've done my first prompt... And I will try and fit as many of them into a single prompt as possible because I found that Fable is much smarter than me at programming—or probably in everything. And so if I give it all the things I want it to fix, it'll actually fix it in the order that Fable deems as best, rather than me having them fix it one at a time."
> （这些是我在完成第一次提示后主要检查的六件事……我会尽量把尽可能多的条目塞进一个提示词里，因为我发现 **Fable 在编程上比我聪明得多——可能在任何事情上都比我聪明**。所以如果我把所有想修的东西都给它，它会按照它自己判断的最佳顺序来修，而不是我一条一条地让它修。） `[段落 12]`

**这段话是整期视频里最反直觉、也最值得琢磨的一条经验**：

- 传统软件工程里，你是老板，AI 是执行者，你拆任务、排优先级
- 而作者的建议是**反过来**：你把一堆目标丢过去，让 AI 决定先修哪个

他给出的理由是"模型比我聪明"。这个理由听起来像恭维，但从工程角度其实有扎实的依据：**多个修改之间往往存在依赖关系**（比如改了移动端布局可能影响桌面端样式），人类一次性排出的顺序很可能是错的，而模型能看到全部上下文，更可能排出合理顺序。

**现在完整还原那六项清单**（作者逐条列举 + 逐条演示）：

**第 1 项：功能（Function）**

> "It basically does function the way that we wanted it to."
> （它基本上按照我们想要的方式运行了。）

这是"过/不过"的判断，通过了才继续看其他。

**第 2 项：布局（Layout）**

> "The layout is not clean and I actually don't like some of the layout, so that will be what I try and fix first."
> （布局不干净，我确实不喜欢某些布局，所以这是我首先要修的东西。）

**第 3 项：移动端（Mobile）**

> "Does it fit well on a phone screen?"
> （它在手机屏幕上显示得好吗？）

作者用 Claude 的移动预览检查了一下，结论是"我不知道它在移动端表现如何，这可能是我们该尽快修的东西"。

**第 4 项：文字与颜色**

> "Please make all the text more white and vibrant. Like it's hard to see the title of the lists."
> （请把所有文字变得更白、更醒目。现在很难看清列表标题。）

**第 5 项：线条与边框**

> "Also, there's too many lines, right? I don't want the outer border around the list. I just need the list title and then the cards beneath it and then the add card at the bottom should be like a very subtle, mostly transparent thing that I can click that almost looks like another card. This is too much enclosed stuff."
> （线条太多了，对吧？我不要列表外面的边框。我只要列表标题，然后下面是卡片，然后底部的"添加卡片"应该是一个非常微妙、几乎透明、可以点击的东西，看起来就像另一张卡片。封闭的东西太多了。）

还有：

> "Get rid of the line below the top bar at the very top."
> （把顶部栏下面那条线去掉。）

**第 6 项：控件位置**

> "The agent notebook, please just make a little note icon at the top and make that the note icon. The exit button—okay, so that's sign out. Please get rid of that. Just put that in like a profile—if I click profile, that's where the sign out button should be."
> （Agent 笔记本，请在顶部做一个小小的笔记图标。那个退出按钮——好，那是登出——请去掉它，把它放到个人资料里：如果我点个人资料，登出按钮就应该在那里。）

**以及若干风格修正**：

- **放弃军事风**：

> "I actually don't like the war vibe. I like the more minimal vibe."
> （我其实不喜欢那种战争氛围，我喜欢更极简的氛围。）

这是对自己上一轮提示词里"slight military vibe"的一次公开推翻——**印证了"先模糊后修正"的工作流**。

- **动画升级**：

> "Make the animation cooler and it should make a sound. This is when things are added to the board by an agent or by anyone."
> （把动画做得更酷，而且**它应该发出声音**。触发时机是当 Agent 或任何人往看板上添加东西时。）

- **去掉卡片计数**：

> "Don't list the number of cards."
> （不要列出卡片的数量。）

**测试评论功能**：

作者让 Grokbot 在所有视频上留评论并给出建议：

> "Please leave some comments on all the videos and give me a pointer on all of them."
> （请在所有视频上留一些评论，给每一个都提一条建议。）

结果：

- 卡片上出现了 "opened by Riley's Grok Bot agent, updated by Riley's Grok Bot agent"（由 Riley 的 Grok Bot agent 打开，由 Riley 的 Grok Bot agent 更新）
- 评论内容成功写入：">> Riley's Grok Bot pointer: some shadow while building patterns as an agent. Walk a real site through this."
- **但评论的 UI 作者不满意**，于是加入到同一个提示词里：

> "Please make the UI of the comments look more like just a more relaxed message board. Too many like lines in general. There's just too many horizontal lines. Just don't have the vertical line between the two sides of the pane, like in the details of each card. Just minimalize it... it could just say Riley's Grok Bot and have a little icon there and then have the text beneath it."
> （请把评论的 UI 做得更像一个放松的留言板。线条太多了，横线太多了。不要卡片详情页两侧之间的那条竖线。把它极简化……它可以就显示"Riley's Grok Bot"加一个小图标，然后下面放正文。）

**延伸思考**

这段内容其实是一个**人类角色转变的宣言**。在这个工作流里，人类不再负责"实现"，也不再负责"排期"；人类负责的是**审美判断**和**问题发现**——"我不喜欢这个"、"这个看不清"、"线太多了"。而工程决策权被交还给了模型。

这对很多技术从业者来说是一个不舒服的转变，因为它把人的价值从"我能做出来"重新定义成了"我知道什么是对的"。前者是技能，后者是品味。当技能被自动化，品味就成了稀缺资源。

**精华收获（六项自检清单）**

```
1. 功能：它真的在做我要求的事吗？
2. 布局：整洁吗？我喜欢吗？
3. 移动端：在手机屏幕上崩了吗？
4. 文字：对比度够吗？看得清吗？
5. 线条：有没有多余的边框、分隔线、封闭框？
6. 控件：按钮位置符合直觉吗？（笔记图标、登出入口）
```

外加两条风格维度：**动画反馈**（有无、酷不酷、有没有声音）与**信息密度**（去掉不必要的数字与装饰）。

---

### 十一、第二版结果与跨平台测试：ChatGPT 接入 + 第二个真人用户 `[段落 14-16]`

**核心观点**
第二版应用明显更极简、更好看；随后作者用同一个 skill 让 ChatGPT/Codex 接入，并创建了第二个真人账号来验证多人协作与实时更新。

**深度阐述**

**第二版验收**：

> "It's done and it looks a lot more minimal... this is looking pretty good and these buttons here at the top are looking a lot better."
> （做完了，看起来极简多了……看起来相当不错，顶部这些按钮也好多了。） `[段落 14]`

**跨平台测试——把技能交给 ChatGPT**：

作者复制了 `skill.md`，要在 ChatGPT 上验证：

> "I want to make it work for ChatGPT. Please connect this, add the skill, then add 10 things to the board and add one column. Whatever you think is best."
> （我想让它在 ChatGPT 上也能用。请接入这个，把技能加上，然后往看板里加 10 样东西，再加一列，你觉得什么最合适就加什么。）

同时追加了一个更有意思的任务：

> "Find the comments from the cursor bot and make a comment responding beneath them."
> （找到 cursor bot 留下的评论，在它们下面回一条评论。）

**这是一个 Agent 之间的对话测试**——ChatGPT 读取另一个 Agent（cursor bot）的评论，并在其下回复。这是"Agent 协作"这个概念的具象化：**Agent 之间通过共享的工作空间进行异步对话**。

**ChatGPT 的执行过程与思考**（作者实时转述）：

> "The skill is now installed. I'm applying it now to Riley's Codex, first registering the agent's identity, then reading the live board before creating, so existing cards and replies aren't duplicated."
> （技能安装好了。我现在把它应用给 Riley 的 Codex：首先注册 Agent 身份，然后**在创建之前先读取实时看板，以免已有的卡片和回复被重复创建**。）

这段 Agent 的自述非常值得注意——它揭示了**一个好的 Agent 是如何避免多智能体协作中的经典问题（重复写入）的**：先读后写、先注册身份。

结果：

> "Oh, here we go. They're coming in. And there you go. It added them based on what ChatGPT knows about me."
> （哦，来了。它们在往里进。成了。它根据 ChatGPT 对我的了解把这些加了进去。）

卡片署名显示：**created by Riley's Codex**。

**然后出现了 bug**：

> "So we're running into one of these problems. So I think it's the apostrophe here."
> （我们遇到了这类问题之一。我觉得是那个撇号的问题。）

作者的处理方式极其干脆——**直接截图，粘贴，然后说**：

> "I think this is a formatting issue with the apostrophe. Please fix this and then take an in-depth look at this website. Please analyze everything and just make some adjustments for styling. Just use your best judgment, look at the app, and make some changes."
> （我认为这是撇号的格式问题。请修掉它，然后深入地看看这个网站，分析所有东西，做一些样式调整。**用你最好的判断力，看着这个应用，做点改动。**）

**"用你最好的判断力"**——这句话是整个 vibe coding 心法的浓缩。它不是放弃控制，而是**在明确的目标下把决策权交给更擅长的一方**。但同时他也给了具体的 bug 定位（撇号），体现了"精确问题精确说，模糊改进模糊说"的分层沟通技巧。

**第二个真人用户测试**：

作者创建了一个名为 **Jacob** 的新账号，并用它留言：

> "Hey, this is pretty cool. And so, Jacob left a comment. Oh, and so when there's comments, you can see it update live on the board."
> （"嘿，这挺酷的。"于是 Jacob 留了一条评论。哦，当有评论时，你能看到它在看板上**实时更新**。）

这次双线并行（一边 ChatGPT 在写入，一边真人在操作）恰好构成了一次**并发协作测试**，结果一切正常，且更新是实时的。

**延伸思考**

"先注册身份，再读取实时看板，避免重复创建"——这句话值得被所有做多 Agent 系统的人抄下来当作第一课。它说明了**多智能体协作的真正难点不在模型能力，而在并发控制与状态一致性**。而在这个场景里，解决方案不是由人类工程师写的，是 Agent 自己在执行任务时自然采取的谨慎策略。

另外，撇号 bug 也值得记一笔：**这是一个典型的"自动转录/编码/格式化"陷阱**——当 Agent 名字里带了 `'` 这样的特殊字符时，如果系统没有做好转义处理，就会出现渲染或存储错误。这是任何允许用户生成名字的系统都必须处理的边界情况。

**精华收获**

- 跨平台测试是验证"Agent 原生"承诺的唯一方法：换一个平台的 Agent，它还能操作吗？
- 报 bug 时给上下文（截图 + 你的判断），改样式时给自由度（用你的最佳判断，看着改）。
- 让多个 Agent 和真人同时操作，是发现一致性问题的唯一可靠手段。

---

### 十二、上线：把本地应用部署到互联网 `[段落 17]`

**核心观点**
应用在本地跑通、团队可用之后，最后一道关卡是部署——作者用 Vercel 完成，并同时同步到 GitHub，一次性拿到一个可以发给团队的公开 URL。

**深度阐述**

作者说得很直接：

> "The only thing that prevents my team from being able to use it is putting it on the actual internet. And for that, we're going to be using Vercel."
> （唯一阻止我团队用上它的东西，就是把它放到真正的互联网上。为此，我们要用 Vercel。） `[段落 17]`

**Vercel 的定位**：作者所有的应用都托管在 Vercel 上，包括他的官网 `agentnative.ink`。

**一次性的配置工作**：

> "All you need is to get an API key. And the first time you do it is you can just give the Vercel API key to Claude Code and just say, 'Please configure your Vercel so that we can build apps and deploy them to Vercel.'"
> （你需要的只是一个 API key。第一次做的时候，你只要把 Vercel 的 API key 交给 Claude Code，然后说："请配置好你的 Vercel，这样我们就能构建应用并部署到 Vercel 上。"）

**这一步之后，部署就变成了一句自然语言**：

> "Hey, once you're done, please make sure this is on GitHub and Vercel. I want you to create a new repo. Call this Agent Native Board... And then I want you to put it on Vercel once you're done. So that we have it on a real URL that I can send to my team."
> （嘿，做完之后，请确保它在 GitHub 和 Vercel 上。我想让你创建一个新仓库，叫 Agent Native Board……然后做完之后把它放到 Vercel 上，这样我们就有一个真正的 URL，可以发给我的团队。）

**结果**：

> "Look at that. We now have it on GitHub and it's also live on Vercel."
> （看这个。我们现在把它放到了 GitHub 上，同时也已经在 Vercel 上线了。）

最终 URL：**agentnative-board.vercel.app**（转录拼写）。作者用一种非常随意的方式验证了一下：

> "You could go to this website and you could contribute to this app. You could actually add your agent to this app if you sign up right here."
> （你可以访问这个网站，为这个应用做贡献。你甚至可以在这里注册，把你的 Agent 接入这个应用。）

**延伸思考**

这段内容里隐藏着一个被严重低估的能力跃迁：**部署，从一个需要懂 CI/CD、域名、环境变量、构建配置的专业任务，变成了一句自然语言指令**。

在传统流程里，"我做了个东西想给同事用"和"我做了个东西上线了"之间，隔着一条很多人一辈子都不去跨的河。而现在这条河被填平了——你只需要在首次配置好一个 API key，之后说一句"放到 Vercel 上"就够了。

这件事的真正意义不在于省了多少时间，而在于**它消灭了"从原型到可用产品"之间那道心理鸿沟**。当上线变得和保存文件一样简单，人们做产品的动机结构就会改变：更多人会愿意把"随便做的东西"真的发布出去。

**精华收获**

- 部署平台（如 Vercel）的 API key 是一次性配置，之后就是自然语言操作。
- 同时同步 GitHub + 部署平台，既拿到公开 URL，又保留了代码版本。

---

### 十三、终极演示：让 AI 清空并重建你的真实业务看板 `[段落 18-19]`

**核心观点**
最后，作者用一段自然语言指令，让 AI 把整个看板清空、按照它对作者业务的全部了解重新组织内容，并在笔记本里留下备注——完成了从"demo"到"真实业务工具"的最后一跃。

**深度阐述**

这是全片最有说服力的一个演示，因为它不再演示"技术能力"，而是演示**"业务能力"**。

指令如下：

> "Please remove everything from the entire board. I want you to reorganize it for my actual business based on everything you know about me. But first, leave a few notes in the notebook."
> （请把整个看板上的所有东西都删掉。我要你**根据你所知道的关于我的一切**，为我的真实业务重新组织它。但首先，在笔记本里留几条笔记。）

注意这里的关键链条：**AI 之所以能"为我的真实业务重新组织看板"，是因为它通过前面提到的 Connectors 掌握了作者的邮件、日历、短信、Slack 等全部上下文。** 这不是一个空的看板被随机填充，而是一个信息聚合的终端——所有分散在各系统的业务信号，第一次被汇聚到了一个可视化的、可协作的、可被人和 Agent 同时读写的地方。

作者的演示过程：

- 打开笔记本（notebook），可以留笔记，**也可以删除**
- 让 AI 清空看板并重新组织
- **"Here it is leaving things in the notebook."**（它正在往笔记本里放东西。）
- 作者随即关掉了笔记本视图，理由是：**"some of this might be sensitive info"**（其中一些可能是敏感信息）

这个小小的动作很有信息量——它暗示了 AI 写入的内容是**真实、具体、涉及商业机密的**，而不是演示用的假数据。

**最终总结（由作者亲口给出）**：

> "Our app is on the internet, fully deployed to Vercel. Any agent can add things to the board. It can edit. It can comment on everything. And it is like a full clone of Trello. And we created this in—well, we created the basics of it in one single prompt using Fable 5.1... And literally, it created a full back-end database, and we use Convex for this."
> （我们的应用在互联网上，完全部署到 Vercel。任何 Agent 都能往看板上加东西、能编辑、能对一切发表评论。它就像一个完整的 Trello 克隆。我们用——嗯，我们**用一个提示词就用 Fable 5.1 做出了它的基础版本**……而且它真的创建了一个完整的后端数据库，我们用的是 Convex。） `[段落 19]`

**作者的完整总结**：

- 这是一个类 Trello 的克隆
- **他本人（Riley）可以往看板加东西、可以评论**
- **GrokBot、Claude、Codex，或任何其他 Agent 也可以修改这块看板**
- 实现方式：用"世界上最好的模型"，让它几乎做了一切
- 它构建了前端、后端，用 Convex 做数据库，托管在 Vercel 上，所以它活在互联网上

结尾是一句非常标准的创作者落款："Thank you guys so much for watching. I hope you learned a ton. Let me know in the comments what video I should make next."

**个人感受**

从整段视频的语气线来看，作者的情绪走过了一条清晰的曲线：**期待（20 分钟等待）→ 惊喜（Agent 第一次写入成功）→ 熟练（六项清单式返工）→ 从容（跨平台测试）→ 满足（部署上线）→ 最终的业务价值确认（重建真实看板）**。

最后那个演示之所以动人，是因为它**从"我做了一个应用"变成了"这个应用正在为我的生意工作"**。前者的满足感是技术性的，后者的是存在性的。而作者用一句"some of this might be sensitive info"轻描淡写地带过了这一点——这是一种克制的自信：不用强调它有多真，因为关掉屏幕这个动作已经说明了一切。

**延伸思考**

最后一个问题值得留下来慢慢想：**当 AI 既能读你的全部业务上下文，又能写你的全部业务系统，你的"业务操作系统"应该长什么样？**

作者的答案是一块看板 + 一个笔记本。但这只是第一次尝试。更深的可能性在于——如果 Agent 能读能写，那么人类在看板上的角色可能逐渐从"操作者"变成"审阅者"，从"我安排任务"变成"我确认 Agent 的安排是否合理"。

而这也提出了一个新的风险：**当 Agent 自动维护你的业务状态时，你还能不能及时发现它搞错了？** 视频里作者在最后一刻关掉了笔记本，理由是"可能有敏感信息"——这个动作，或许是整期视频里最像"未来的人类"的一个瞬间：我们不是在看 AI 做事，我们是在决定**要不要看**。

---

## 全篇精华收获

**1. 一份可直接复用的提示词框架**

平台 → 参照物（"像 Trello 一样"）→ 用户流程（登录/操作/署名）→ Agent 账号设计（继承人类的归属关系 + 用 skill 文件授权）→ 设计风格（先模糊，后迭代）→ 交互反馈（动画 + 音效）→ 数据库选型（并明确它的关键特性）。

**2. 六项自检清单**

功能 → 布局 → 移动端 → 文字对比度 → 多余的线条/边框 → 控件位置。每次第一版生成后，按这个顺序扫一遍。

**3. 把多个修改合并成一个提示词，让模型决定顺序**

作者的理由是"模型在编程上比我聪明，可能在任何事情上都比我聪明"。这不只是省事，而是承认**模型能看到你看不到的依赖关系**。

**4. "Agent 原生"的三个核心设计**

- Agent 有独立账号，且归属于某个人类账号
- Agent 的每个操作都有人类可读的署名（"由 Riley 的 Grok Bot agent 更新"）
- 授权方式极简到"复制一个 skill 文件粘贴给 Agent"

**5. 多 Agent 协作的工程前提**

单一数据源 + 实时同步。选数据库时新增一条标准：**对 AI Agent 是否友好**（可读、可理解、可维护）。

**6. 一个 Agent 的好习惯**

ChatGPT 接入时自述的那句"先注册身份，再读取实时看板，避免重复创建"——这是多智能体系统里最基本的并发防御，也是判断一个 Agent 是否"开窍"的标志。

**7. 部署不再是门槛**

一次配置 API key，之后一句自然语言即可上线。"从原型到可用产品"的鸿沟被填平，这会改变很多人做产品的动机结构。

---

## 客观说明与局限

为避免误导，需明确以下几点：

1. **模型名称存疑**。字幕中的"Fable 5.1"为自动转录结果，作者实际所说的模型名称可能有出入，请以 Anthropic 官方发布信息为准。
2. **"Jimmy bot" 疑为 "Gemini bot"**，"Grokbot" 的准确身份（字幕中显示 Agent 名字为 "Riley's cursor"）也存在转录歧义。
3. **时效性极强**。视频作者自己都在同一段话里承认"GPT-6 传闻即将发布，排名可能很快改变"，因此本文中所有"最强者"的表述都应被视为**录制当时的状态快照**，而非永久结论。
4. **成本提示**。作者明确表示该模型"相当贵"，且演示开始时他的每周额度已消耗 75%。复现此实验前请评估预算。
5. **安全提示**。视频中的 skill 文件包含可直接写入业务数据库的密钥，作者未深入讨论其风险。若将此模式用于真实生产环境，强烈建议自行设计更严格的权限、轮换与审计机制。

---

<!-- TLDR: 复制一段技能粘贴给任何Agent，一个提示词生成实时协作看板 -->
<!-- TAGS: AI编程, Vibe Coding, Claude Code, Agent原生应用, 实时数据库 -->
<!-- RATING: 4 -->
