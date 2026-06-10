---
title: "【十字路口】人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy 【视频播客】"
channel: "Koji Yang"
published: "2026-05-20"
source_url: "https://www.youtube.com/watch?v=Kmpj5KUfIew"
video_id: "Kmpj5KUfIew"
rating: 5
language: "中文"
word_count: 13996
duration: "55:31"
---

# 【十字路口】人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy 【视频播客】

- **Channel:** Koji Yang
- **Published:** 2026-05-20
- **Source:** https://www.youtube.com/watch?v=Kmpj5KUfIew
- **TL;DR:** 21岁创业者挑战AI产品终极命题：持续学习型Agent将颠覆会话式交互，OS层面观测是实现真正个性化的唯一路径
- **Rating:** 5

# 人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy

## 材料信息

- **标题**：【十字路口】人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy 【视频播客】
- **作者/来源**：Koji Yang / 十字路口播客
- **类型**：YouTube 视频播客字幕
- **关键元数据**：嘉宾为 Paperboy 创始人江洋（21岁）及 Founding Engineer Jet Chen（19岁）；内容涉及 AI Agent 产品设计、人机协作范式、创业思考等；时长约 1.5-2 小时
---

## 开篇引入

想象一下这样的场景：你正在电脑前工作，不需要输入任何提示词，你的 AI 助手就知道你接下来要做什么。你在命令行里输入“@PB commit”，它自动帮你写好了完整的提交信息；你在微信里打了几个字，它猜到了你想表达的意思；你开了一天的会、浏览了无数网页、在多个工具之间来回切换，晚上它会给你一份报告，告诉你今天效率如何，甚至“骂”你什么时候分心了。

这不是科幻电影，而是一个 21 岁创业者正在尝试构建的现实。

江洋，04 年出生，这已经是他的第二家公司。他的第一家公司 Mellian 入选了 YC Winter 24，曾收到 Cognition（Devin 的母公司）等多家公司的收购邀约。而他现在创办的 Paperboy，正在试图回答一个根本性问题：**人类和 AI 配合工作的最佳方式是什么？**

他的答案可能会让你意外：这个最佳方式，**还没有被发明出来**。

在这场对谈中，江洋和 19 岁的 Founding Engineer Jet Chen 分享了他们对这个问题的深度思考——从为什么现有的“会话式”AI 产品注定失败，到如何通过操作系统层面的持续学习让 AI 真正理解你，再到一个 21 岁的年轻人如何管理 12 人的团队、如何做 CEO 决策、如何看待 OpenAI 和 Anthropic 的竞争。这不仅是关于一款产品的讨论，更是一场关于人机关系未来的深度探索。

---

## 详细内容

### 一、“人类和 AI 配合的最佳方式，还没有被发明” `[00:00-05:00]`

**核心观点**

当前所有 AI Agent 产品的设计范式都存在根本性缺陷。从 Cursor 到 Claude Code，它们都基于“会话”（session）和“提示词”（prompt），但这不是人类天然的工作方式。人类和 AI 的最佳配合方式，仍然是一个“不断移动的目标”（moving goal post）。

**深度阐述**

在 Paperboy 的第一次全员会议上（当时公司只有 4 个人，时间是 12 月 30 日），江洋写下了一句话作为公司的核心论题：“**the best way to work with AI hasn‘t been invented**”（和 AI 一起工作的最佳方式还没有被发明出来）。这不仅是产品方向，更是一种世界观。

他观察到，现有产品存在一系列根本性问题：

1. **会话式设计的局限**：现在的产品如 Claude Code、Cursor 都是“session based”——你在侧边栏有项目，项目下有一堆会话。每次想让模型做新事情，你就开启一个新会话。问题在于：**session 一丢，你就找不到过去要从哪个 context window 继续聊下去了**。那些会话中可能蕴含着极其宝贵的洞察，但如果你没有刻意保存，它们就永远丢失了。
1. **被动响应的模式**：你输入提示词，AI 等待，你再发一条消息，它再回复。这意味着你必须非常具体，你必须主动维护各种 skill 文档和 MD 文件来描述你在做什么。但无论你投入多少努力，**很难把你知道的所有品味、判断和对最佳实践的理解都转化为纯文本文件**。
1. **缺乏主动性和连续性**：如果 AI 知道了很多关于你的信息，它应该能够 proactively 提前帮你做事情。但现在的 context window 做不到这一点。
江洋将这个问题空间划分为三个维度：

- **技术层面**：Agent 必须能够从用户的环境中学习，集成到用户已有的工作流中
- **个性化层面**：你不需要频繁提示，可以信任它处理越来越复杂和高风险的任务，它需要更可靠
- **设计层面**：必须极其直观，你不应该把它当作新工具来学习
有趣的是，当 Koji 问“从写下这句话到现在有什么新学习”时，江洋给出了一个极具洞察力的回答：**这是一个移动的目标**。因为每次你推出新东西，其他人都会看到。如果其他团队有品味，用户有品味，他们就会感知到，就会看到摩擦点——而摩擦点永远存在。所以你唯一能做的就是不断变得更好。

> “The market’s expectation — you can’t really reach it, you can only keep getting better.“（市场的期望——你无法真正达到它，你只能不断变得更好。）`[05:00]`
**个人感受**

江洋对现有产品的不满不是理论层面的，而是来自亲身实践。从 Same.dev 到 Mellian，他一直在尝试与 AI 协作，但“用过的产品都有那么一些不爽”。这种不爽驱动他去寻找新的可能性。

**延伸思考**

这个“移动的目标”概念很有意思。它暗示了一个更深层的现实：**当产品本身在改变用户行为，用户的期望也在同时改变**。你推出的创新会立刻成为新的基准，然后被超越。这意味着在 AI 时代，产品的“护城河”可能不是某个具体功能，而是持续创新的能力和对用户需求演进的敏感度。

**精华收获**

- 不要假设当前的 AI 产品范式（会话式、提示词驱动）就是最终形态
- 摩擦点永远存在——你的目标不是消除所有摩擦，而是持续发现并解决更高级的摩擦
- 用户品味和团队品味是核心竞争力
---

### 二、三大问题域：环境、个性化与交互范式 `[08:00-15:00]`

**核心观点**

要构建下一代 AI Agent，必须解决三个核心问题：从操作系统层面持续学习用户行为、实现真正的个性化（减少提示）、创造极其直观的交互界面。这三个维度相互依赖，且都受限于人类团队的能力而非技术本身。

**深度阐述**

江洋和 Jet 详细阐述了他们对问题空间的拆解：

**第一，环境集成（Environment Integration）**

Jet 提出了一个关键洞察：**信息的浓度差异**。观察用户 60 分钟的电脑使用行为，可以学到极多的信息；但如果只看 60 分钟的微信聊天记录，几乎学不到什么。因此，最可扩展（scalable）的方式不是导出用户的聊天数据，而是在操作系统层面观测用户日常使用电脑的行为。

这意味着 Paperboy 会收集：屏幕截图、键盘敲击、鼠标移动、会议记录（包括视频和音频）、浏览历史、iMessage 等——当然，用户可以选择授权哪些数据。

**第二，个性化（Personalization）**

真正的个性化意味着：你不需要频繁提示；你可以信任它处理越来越复杂和高风险的任务；它可以持续运行更长时间而不出错。江洋直言：“**I hate prompting**”（我讨厌提示）。他认为人类不是用提示词思考的——我们发信息，期望对方知道我们在说什么。当沟通是高带宽的，我们享受这种关系。

> “We don’t think in prompts. We send texts, and we expect the other person to know what we’re talking about.“（我们不用提示词思考。我们发信息，期望对方知道我们在说什么。）`[12:00]`
他甚至说：“smart people enjoy being told what we don‘t know — especially what we don’t know we don‘t know”（聪明人喜欢被告知那些自己不知道的事——尤其是不知道自己不知道的事）。

**第三，交互范式**

现在的模型比人类聪明，江洋期待有一天可以“躺平”，让 Auto John（他的 Paperboy Agent 名字）这个更高 IQ 的存在来帮助他。但这种交互需要一个全新的形式——不是提示框，而是聊天窗口（literal chat window），就像 iMessage 或微信一样，有一堆对话，你可以持续与对话中的参与者交流。

**个人感受**

Jet 分享了一个非常人性化的使用场景：他怀疑自己有 ADHD，工作时容易分心——写代码时会看 Hacker News，点开一篇文章看 30 分钟，回来发现 Claude Code 已经结束十几分钟了。于是，他让 Paperboy 每天晚上给他一个报告，告诉他今天有多高效，“骂”他什么时候分心了。知道 Paperboy 在“盯着”他工作时，他效率更高。

这不是 Orwell 式的“Big Brother is watching you”，而是一种自我认知和外部监督的有趣结合。

**精华收获**

- 数据的“信息浓度”差异巨大——电脑使用行为的每分钟信息量远超聊天记录
- 真正的个性化不是“记住你的偏好”，而是“不需要你表达偏好”
- 交互设计的终极目标是让技术消失，而不是让用户学习新工具
---

### 三、Paperboy 的核心差异：持久化记忆与主动型 Agent `[15:00-25:00]`

**核心观点**

Paperboy 与现有产品的本质区别在于：**它是持续性的、主动的、基于完整 OS 上下文的**。不是会话式的，而是像 iMessage/微信一样的聊天列表；不是被动响应提示词的，而是主动学习你的行为模式并提供建议。

**深度阐述**

为了清晰对比，江洋指出现有产品（如 Claude Code、Cursor）的两个核心特征：

1. **Session based**：侧边栏有一堆 workspace，每个 workspace 下有一堆 session。每次想模型做新事就开新 session。
1. **One-to-one prompt based**：你提示 → 等待 → 再提示 → 再等待。
而 Paperboy 的处理方式是：

1. **Agent 通过观察你使用电脑的方式自主学习**：包括截图、键盘、鼠标、会议、浏览历史、iMessage 等。这不只是“接入 API”，而是持续的 OS 层面学习。
1. **持久化的对话历史**：超出单个 context window 的长度，可搜索，不会丢失。
1. **类 IM 的交互形态**：打开 Paperboy 就像打开微信或 iMessage，你看到一堆聊天。每个聊天是一个持续进行的对话，你可以随时继续。
**与现有“无限上下文”产品的区别**

Jet 补充了一个重要的技术区分：现在有些产品（如 Poke by Interaction、Open Interpreter）也声称有不基于 session 的持续聊天。但它们的 context 来源主要是过去的聊天历史。即使它们能接入你的邮件或信息，也只是通过“读取”来学习。

而 Paperboy 的核心假设是：**通过 OS 层面的观测是最 scalable 的方式**。这不是因为你不能导出微信聊天数据（他们做过这个 prototype），而是因为这种方式效率太低、不可扩展。

> “我们很快就发现这其实并不是一个非常 scalable 的方式。最 scalable 的方式是观测用户在日常使用电脑时，从 OS 层面收集用户数据。“`[20:00]`
**Aha Moment 实例**

Jet 分享了一个具体的使用场景：他在命令行里输入 `@PB commit`，Paperboy 就自动写完整个 commit message。这个功能看似简单，背后却是复杂的技术：Paperboy 有一个实时更新的 Markdown 文档，包含用户的职业、过去几天做了什么、过去几秒/几分钟做了什么——离当前时间越近，颗粒度越细（更高分辨率）。有了这个 context，你可以在操作系统的任何地方做 auto complete，无论是在微信里还是在 GitHub 上发 PR。

> “很多时候我发现它写的 PR description 比 Cursor 或 Claude Code 好很多。因为我在开发一个 feature 时，可能一会儿在和 Claude Code 打交道，一会儿在微信里和江发消息，一会儿在浏览器里做 research。Paperboy 可以把所有这些 context 聚合在一起。”`[22:00]`
**个人感受**

江洋分享了他使用 Paperboy 的经历：他现在大部分工作是使用不同产品、做研究、与人交流，没法像以前那样写很多代码。但 Paperboy 把不同粒度、不同来源的信息都“装在脑子里”。当他研究完微信历史和各种网络效应商业模式后，想把思考连接起来时，Paperboy 会提醒他：“等等，你有没有想过这个？你几个月前试过这个，当时的产品形态是 X，你识别出的问题是 Y。”

这种“连接点”的能力，是超越简单信息检索的更高阶智能。

**精华收获**

- “持续学习”不是“记住历史”，而是“理解模式”和“主动提醒”
- 最有效的用户数据采集方式不是 API 集成，而是 OS 级别的观测
- 交互界面应该像 IM 一样自然——你不需要学习新工具，工具应该适应你
---

### 四、竞争与护城河：品味、速度与企业市场 `[25:00-35:00]`

**核心观点**

在 AI 领域，真正的竞争对手只有 OpenAI 和 Anthropic。创业公司的生存之道不是试图在模型层面竞争，而是在品味（taste）、速度和特定应用场景上建立优势。Paperboy 最初想做的其实是“AI Slack”，但后来意识到更好的策略是把 Agent 带到用户已经在工作的地方。

**深度阐述**

当被问及竞争对手时，江洋的回答非常直接：

> “Only two that matters today are OpenAI and Anthropic. Everybody else is behind them.”（今天只有两家公司重要：OpenAI 和 Anthropic。其他所有人都在它们后面。）`[28:00]`
大模型公司拥有所有优势：他们拥有模型本身、有计算资源、有强大的分销渠道。创业公司能做的，是像“Crusoe”一样，在某些 edge 上有品味优势——在它们之前找到新的交互界面。

但这不意味着创业公司没有空间。关键在于：

1. **个人和产品体验的差异不会消失**：大公司可以做通用产品，但特定场景的深度打磨需要专注的团队。
1. **企业市场是另一条路径**：企业需要的是将 Agent 集成到现有工作流中，而不是抛弃 Slack 从头再来。
**关于“AI Slack”的思考**

Paperboy 最初的产品想法就是“AI Slack”。但经过思考，他们意识到进入企业市场的挑战：

- **切换成本极高**：企业 Slack 中有外部连接（external connections），公司和公司之间的交流很大程度上依赖这个网络效应。要让一个团队（尤其是超过 50 人的团队）从 Slack 切换过来，难度极大。
- **Slack 的产品体验并不完美**：江洋直言：“Slack is honestly not a great product.” 他并不享受使用 Slack，只是没有更好的选择。但正因如此，在 Slack 之上做 Agent layer 比重新造一个轮子更合理。
> “It makes more sense to bring the Agents to where people already work, instead of trying to replace and build everything from scratch.”（把 Agent 带到用户已经在工作的地方，比试图取代一切从头开始构建更有意义。）`[32:00]`
**Jet 的补充：网络效应是真正的护城河**

Jet 从技术角度分析了 Slack 的不可替代性：Slack 有 external connections 功能，所有认真的公司都用它，公司和公司之间的交流很大程度上已经不是通过邮件，而是通过这些连接。这和微信在中国的地位类似——让它们达到某种程度上的不可替代。

因此，Paperboy 的策略是：**做 Slack 的 complement（补充），而不是 competitor（竞争者）**。

**个人感受**

Koji 问江洋：“你觉得自己的成熟度超越了年龄，是怎么来的？” 江洋的回答很坦诚：“I think I‘m still a pretty childish person.”（我觉得自己还是蛮孩子气的。）他认为自己只是对商业有热情——在做一件非常难的事情，要在很短的时间内完成，所以 clarity（清晰）、efficiency（效率）和 focus（专注）是必需的。

他的学习方式也很有意思：不只是为了创业而学习，而是跨越不同商业规模去理解“founder market fit”和“team market fit”。他认为市场选择（market picking）是创始人早期最重要的能力——甚至是最重要的能力。

> “Market picking is one of the most important, if not the most important, trade of a founder early on.”（市场选择是创始人早期最重要，甚至是最重要的能力。）`[42:00]`
**精华收获**

- 在大模型公司面前，创业公司的竞争不是“更好的模型”，而是“更好的品味”和“更快的迭代”
- 企业市场的网络效应极其强大，与其对抗不如与之互补
- 市场选择能力比执行能力更重要——你得知道自己在进入什么样的战场
---

### 五、The Last Interface：五种速度与 Pace Layers `[35:00-40:00]`

**核心观点**

Paperboy 官网上的博客《The Last Interface》提出了一个核心框架：在 Agent 的世界里，需要不同“速度”（pace）的信息层来代表真实世界。这一灵感来源于 Stewart Brand 的 Pace Layers 理论——从快速变化的时尚到几乎不变的自然是六个不同速度的层级，它们共同构成社会。

**深度阐述**

江洋在高中的时候就接触到了 Long Now Foundation 创始人 Stewart Brand 提出的“pace layers”概念。这个理论描述了六个以不同速度变化的层级：

- 顶层：时尚（fashion）——变化最快
- 向下：商业（commerce）、政治/治理（governance）、基础设施（infra）
- 最底层：文明（civilization）、自然（nature）——几乎不变
这些层级之间相互影响、相互反射，共同构成社会。

江洋认为，在 Agent 的世界里，也需要类似的多层结构。Jet 进一步展开：

> “如果把用户做的 task 的长度做一个分类，会看到不同的 spectrum。一端是用户在微信上回一条消息，只需要 10 秒钟；另一端是用户读 10 个很长的 report 去做一个 business decision，可能花几个小时；再长的一端可能是超过一个月的项目。”
不同时间跨度的任务，需要不同的自动化形态：

- **短任务**（秒/分钟级）：如回复微信，最好的 form factor 是 auto complete——你点到输入框，它自动弹出建议。Paperboy 已经在做这个。
- **中等任务**（小时级）：自动化一个几小时的任务，最好的 form factor 是什么？这还是一个非常值得探索的区域。
- **长任务**（月级）：如完成一个项目、做出一项商业决策，需要完全不同的产品形态。
这就是为什么他们在博客中讨论“五种速度”——不是精确的五个层级，而是一种分类方式，强调：**不能以同一种方式压缩所有的活动流**。

**延伸思考**

Pace Layers 提供了一个思考 AI Agent 设计的框架：不同层级的任务需要不同层级的记忆、不同的交互频率、不同的自主程度。试图用一个统一的模型处理所有任务，就像试图用时尚的节奏来规划基础设施一样荒谬。

这也解释了为什么 Paperboy 要做多层记忆系统——从秒级的 auto complete 到月级的项目上下文，都需要不同的处理方式。

**精华收获**

- 任务的“时间尺度”决定了 AI 辅助的最佳形态
- 好的产品设计需要识别不同尺度的任务，并为每个尺度设计合适的交互
- 不能用一个“万能”的 context window 处理所有问题
---

### 六、管理、招聘与自我成长：21 岁 CEO 的挑战 `[40:00-52:00]`

**核心观点**

成为 CEO 后，江洋最大的感受是：“Man, it’s fucking hard.” 他必须 ownership of everything。作为联合创始人时也会感到 frustration，但作为 CEO，你的每一个决策都可能让公司损失最多的钱——因为你拥有最大的杠杆。管理技能需要从书本、前辈、CEO 教练那里学习，而 Paperboy 本身也在帮助他管理自己的管理过程。

**深度阐述**

**CEO 的艰难**

江洋坦承，这是他第一次做 CEO（上一家公司是 Co-founder）：“I got to own everything.”（我什么都要负责。）当一个工程师浪费了一个下午，他会感到 frustrated；但作为 CEO，他才是那个可能让公司损失最多钱的人。

> “If I say we go do this, and that is actually not a good idea — it’s the position where literally all of your ideas can have such a large cost and rewards.”（如果我说我们做这个，而那不是个好主意——这个位置就是你的每个想法都有巨大的成本和收益。）`[44:00]`
此外，他还要面对：选谁 hire？他们从哪里来？hire 之后如何持续提升个人和团队？每个人是否走在他们应得的道路上？如何做 performance review？如何开 one-on-one？如何确保自己与 team lead 沟通而不 micromanage 每个人？

**如何学习管理？**

江洋的学习来源有三个：

1. **前辈经验**：在上一家公司 Mellian 之前，他曾在一家叫 Minus 的公司实习，CTO Panpan 是位出色的 engineering manager。他利用 one-on-one 的机会问了所有关于“如何组织一切”的问题。
1. **阅读**：他认为最好的管理书是 Andy Grove 的《High Output Management》，还有 Ben Horowitz 的《The Hard Thing About Hard Things》，以及 Bill Campbell 的《Trillion Dollar Coach》。
1. **CEO 教练**：他找到了一位 CEO 教练，每周聊一小时。这位教练曾是多家大公司的 VC 高管，专门辅导首次做 CEO 的人。有趣的是，这位教练也是某位投资人的同一位教练。
> “I never tried getting a therapist before. I never believed in therapy. But a coach is so much better — you can talk about your emotions, but you can also talk about business.”（我从没试过心理治疗，也从没相信过它。但教练好多了——你可以谈情绪，也可以谈业务。）`[48:00]`
更妙的是，他可以用 Paperboy 来辅助教练对话——Paperboy 会听这些对话，帮他跟进在对话中承诺要做的事情，并组织一切。

**AI 时代的团队建设**

Koji 问：今天有这么多 AI 工具，团队建设有什么巨大变化？

江洋的回答出人意料地“传统”：要做严肃的 infra 搭建，你需要懂 infra 的人。团队需要两类工程师：一类是像 Jet 这样年轻、高 IQ、有创造力的人，可以快速 prototype 一切看到的问题；另一类是真正扎实、懂系统、懂 OS 的人——比如他们 hire 了一位曾在 AWS 做 Windows kernel 的工程师。

> “I don‘t think that’s going to go away anytime soon. The human experts.”（我不认为这会在短期内消失——人类专家。）`[50:00]`
**个人感受**

Jet 在被问到“为什么还要读大学”时，给出了一个既坦诚又有深度的回答：“It‘s got Chinese parents.”（因为我有中国父母。）然后他认真地说：对于大多数人来说，大学提供巨大的价值——尤其是当你还不确定未来想做什么的时候。四年时间去探索，对大多数人是有用的。但如果你已经很确定想做什么，并且有计划，辍学也是理性选择。

这段话背后是一个 19 岁少年的清醒：他知道自己是例外，但不会因此否定体制对大多数人的价值。

**精华收获**

- 成为 CEO 意味着你的每一个想法都有巨大的财务杠杆——好想法放大收益，坏想法放大损失
- 管理技能可以通过阅读、请教前辈、聘请教练来学习——不必自己发明一切
- AI 不会取代深度的领域专家（如 OS kernel 工程师），反而放大了他们的价值
- 大学对大多数人有价值，但知道自己要什么的人可以考虑其他路径
---

### 七、投资判断、模型竞争与未来展望 `[52:00-1:05:00]`

**核心观点**

如果必须投资，江洋会选 OpenAI（80%）和 Anthropic（20%），理由是 OpenAI 更“unopinionated”（不预设使用方式）且在 compute 上有优势。Jet 更偏爱 Anthropic 的安全承诺，但认为当前估值都不会买。模型不会吞噬一切——产品公司和模型公司的边界会模糊，Cursor 就是例子。

**深度阐述**

**OpenAI vs. Anthropic**

Jet 的分析非常技术化：

- **Codex vs. Claude Code**：Codex 的 Agent 是开源的，命令行和 Agent loop 都在 GitHub 上。他们收购了做 Apple Shortcuts 的团队 Sky，产品非常 polished（精致）。Codex Pets 就是一个例子——好玩又精致。Codex 也是第一个以高并发（多 Agent 同时工作）为主要 UI 的产品。
- **Infra 优势**：OpenAI 在 infra 层面的优势远大于 Anthropic。模型差不多，但 OpenAI 更稳定。OpenAI 可以 subsidize（补贴）更多的 compute，而 Anthropic 投资不足，没法补贴。这导致了一些奇怪的现象：如果你的 repo 里有 Open Interpreter 或 Hermes 这样的 Agent，Claude Code 可能会收你 10 倍的价格。
- **价值观差异**：Jet 认为 Anthropic 做得最好的是 interpretability（可解释性）和 social impact（社会影响），但他们在模型使用上过于 opinionated——无论道德上还是使用习惯上，都设定了很多限制。OpenAI 的理念是：在最小限制下，用户想怎么用模型就怎么用。Jet 说自己更 libertarian（自由意志主义），喜欢 OpenAI 这种 unopinionated 的价值观。
江洋的观点不同：如果现在要做投资决策，两家在当前估值下都不会买。但如果必须选，他更喜欢 Anthropic，因为对安全的承诺。

**模型会吞噬一切吗？**

Jet 的答案是：很多公司会提供差不多的模型，产品的差异性仍然在产品公司。Cursor 就是一个例子——他们一开始是产品公司，现在既是产品公司又是模型公司（用 xAI 的 compute 做 coding model）。公司不能把自己局限为“模型公司”或“产品公司”，通常是 both。

**如果他们有三百万美金可以投资三个团队**

江洋的选择：

1. Slack（是的，Slack 本身）
1. 机器人公司——虽然现在还没有确定的 big winner
1. 基础设施（infra）方向的人
1. 他相信最大的公司会来自消费市场（consumer），而不是企业 AI。Paperboy 就在这个市场。
Jet 的选择：

1. **机器人（Robotics）**：在自动化知识工作之后，最大的机会是用模型能力进化物理世界
1. **安全（Security）**：AI security 的需求几乎是无限的。模型越强，它的攻击和防御能力都越强。问题是：你怎么和 Anthropic 竞争？Jet 认为，即使 Anthropic 有最好的模型，下一步的优化层（harness、heuristics baking、multi-agent 系统）还有巨大空间。如果你的产品比另一个产品多挖出 10% 的漏洞，这就是一个非常有用的产品——这是一个 meritocratic 的市场。
1. 江洋提到的长期法律自动化（Long Horizon law，如 Harvey 和新的 sweep bench）
> “安全能力对国家安全极其重要。但模型最强的人有 incentive 说‘只有我们国家可以用’。那么其他国家怎么搞？很多国家和利基市场都需要这类模型，所以市场非常大。”`[1:02:00]`
**一年后的 Paperboy**

江洋的期待很朴素：

- “Hopefully not losing money every day anymore.”（希望不再每天都在亏钱。）
- 继续 hire 能找到的最好的人——人才密度需要比今天更高
- 需要有现金流，需要继续 building 更好的团队
**个人感受**

整场对话中最打动人的时刻之一，是江洋在最后说的那句“It‘s fucking hard.” 不是抱怨，而是一种清醒的认知。21 岁，第二家公司，12 人团队，每天亏钱，在做一个“还没有被发明出来”的产品——他知道自己在做什么，也知道这有多难。

**精华收获**

- OpenAI 和 Anthropic 的竞争不仅是模型能力，更是 infra、定价策略和价值哲学的竞争
- 产品公司不会被模型公司“吞噬”——两者边界会模糊，但不会消失
- AI 安全是一个 meritocratic 的巨大市场，不受模型公司的完全控制
- 找到好的 CEO 教练可以改变游戏规则——尤其当你不知道怎么管理的时候
---

## 总结：为什么 Paperboy 值得关注

这场对话不仅仅是关于一个创业公司的产品介绍。它是一场关于人机关系未来的深度探索。

江洋和 Jet 提出的核心问题——“人类和 AI 配合的最佳方式是什么？”——在今天比以往任何时候都更紧迫。我们有越来越强大的模型，但交互范式还停留在“聊天框 + 会话”的原始阶段。这就像有了内燃机，但还在用马拉车的框架思考。

Paperboy 的尝试——OS 级别的持续学习、持久化的对话历史、类 IM 的交互界面、多速度的记忆系统——至少提供了一个方向。也许他们不会成为最终的答案，但他们在问正确的问题。

而更令人印象深刻的是提问者本身：21 岁的 CEO，19 岁的 founding engineer，在硅谷和中国的交汇处，用跨文化的视角思考着技术的未来。他们身上有一种罕见的 clarity——知道自己要做什么，知道这有多难，也知道自己为什么在做。

正如江洋所说：“We are trying to do something very hard in a very short amount of time. And so clarity and efficiency and focus.”（我们试图在极短的时间内做一件极难的事情。所以需要清晰、效率和专注。）

这也许就是他们吸引人的原因——不是在谈论一个已经存在的未来，而是在创造它。

---

<!-- TLDR: 21岁创业者挑战AI产品终极命题：持续学习型Agent将颠覆会话式交互，OS层面观测是实现真正个性化的唯一路径 -->

<!-- TAGS: AI Agent, 人机交互, 创业方法论, 产品设计, 下一代界面 -->

<!-- RATING: 5 -->

---
