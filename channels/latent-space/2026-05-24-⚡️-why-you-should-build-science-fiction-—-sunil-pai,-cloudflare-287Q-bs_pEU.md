---
title: "⚡️ Why you should build Science Fiction — Sunil Pai, Cloudflare"
channel: "Latent Space"
published: "2026-05-24"
source_url: "https://www.youtube.com/watch?v=287Q-bs_pEU"
video_id: "287Q-bs_pEU"
rating: 4
language: "中文"
word_count: 9508
duration: "14:47"
---

# ⚡️ Why you should build Science Fiction — Sunil Pai, Cloudflare

- **Channel:** Latent Space
- **Published:** 2026-05-24
- **Source:** https://www.youtube.com/watch?v=287Q-bs_pEU
- **TL;DR:** 别再造Agent框架了，用Cloudflare原语去构建让基础设施“吃力”的科幻级原创应用。
- **Rating:** 4

# 材料信息

- **标题**：⚡️ Why you should build Science Fiction — Sunil Pai, Cloudflare
- **作者/来源**：Latent Space
- **类型**：YouTube 视频字幕
- **关键元数据**：发布日期不详（推测为2025年上半年），对话时长约30-40分钟；Sunil Pai 是 Cloudflare 的开发者体验及 AI 基础设施方向的核心工程师，也是 Code Mode / Agent SDK 的创建者。
---

# 开篇引入

在 AI Agent 框架如雨后春笋般涌现的今天，Cloudflare 的工程领导者 Sunil Pai 带来了一段既充满技术硬核、又交织着个人戏剧与深刻反思的对话。这不仅是 Cloudflare 产品能力的巡礼，更是一场关于底层原语设计哲学、开源社区信任危机、以及开发者原创性灵魂拷问的当面对谈。Sunil 直言不讳地表示要“竞争”Anthropic 的 Agent 平台，分享一次因 fork 项目险些断送职业生涯的争议，最终以几乎恳求的语气呼吁所有人：别再写另一个 Agent 框架了——去构建科幻。这篇文章将逐层拆解这段对话的核心思想，让你获得比直接观看字幕更深刻的理解。

---

# 详细内容

## 一、从竞争切入：Cloudflare 的 Agent 原语，凭什么挑战 Anthropic 的平台 `[核心技术讨论部分]`

### 核心观点

Sunil 认为 Cloudflare 的 **Durable Objects**（有状态持久对象）与 **Dynamic Workers**（动态工作器）两个底层原语组合，能够构建出比 Anthropic 新发布的 Cloud management agents 平台更高效、更灵活的 AI Agent 基础设施。

### 深度阐述

对话一开始，主持人提及 Anthropic 在前一天刚刚发布了 Cloud management agents 平台。Sunil 先礼貌地称赞了 Anthropic 团队的野心与平台设计的亮点，然而他话锋一转，毫不犹豫地抛出一句重量级宣言：**“I think I want to compete. I think we can do something better with workers and durable objects.”**（我想参加竞争。我认为用 Workers 和 Durable Objects 我们能做出更好的东西。）

这句话的底气来自两个被他称为“关键创新”的底层能力。

**第一层：Durable Objects 是基础设施层的 Actor 模型。** Sunil 将其定义为“stateful serverless programming”（有状态的无服务器编程），并强调这是**全球第一次在基础设施层（而非用户空间）实现 Actor 模式**。这意味着开发者可以启动数百万个独立维护状态的后台对象，它们运行在 Serverless 的计费与伸缩模型之下，却无需为整个虚拟机的生命周期买单。这个原语让长时间运行、需要持久记忆的 Agent 任务有了天然的主场。

**第二层：Dynamic Workers 则解决了 AI 时代最关键的安全与执行效率问题。** Sunil 透露，这项功能刚刚发布几周，其核心价值在于：**可以在安全隔离环境下运行用户或 LLM 生成的代码，且启动时间为零。** 安全到什么程度？默认配置会阻止所有对外流量，开发者只能通过显式暴露的 API 与外界交互。这种设计让“LLM 写代码并执行”从危险操作变成常规架构决策。

他接着用 Cloudflare 的 MCP（Model Context Protocol）服务器作为实战案例。Cloudflare 的 Open API 一共包含 **2600 个端点**，如果按常规思路为每个端点生成一个工具函数，LLM 会立即被工具列表淹没。他们的方案非常激进：**只暴露两个工具调用——一个是“搜索”，一个是“执行”。**

当你想要操作时，会向隔离环境提交一段 JavaScript 代码，让代码去解析 OpenAPI JSON 并执行实际请求。Sunil 举例道：**“You can say, ‘Here’s some JavaScript code that searches the entire Open API JSON.’ And the second time you can say, ‘Here’s some code to actually run that. Hey, find all my workers, find the DNS things they’re used in, and if it starts with the letter Z, then apply DOS protection for it’ — in one tool call.”**（你可以说，“这是一段搜索整个 OpenAPI JSON 的代码。”第二次可以说，“这是一段真正执行它的代码，找出我所有 Workers 以及其使用的 DNS 记录，如果它以字母 Z 开头，就为它应用 DOS 保护”——这一切都在一次工具调用中完成。）

他兴奋地强调：**“This is fundamental capabilities. It’s not something you can patch on and use.”**（这是基础能力，不是事后可以修补上去的功能。）这种设计避免了 LLM 在多步调用中的往返延迟和上下文遗忘，让代码即工具，工具即代码。

### 个人感受

Sunil 在描述这些技术时，语速加快，语气中带着毫不掩饰的骄傲。他反复使用“true innovation”“fundamental”这类词汇，不只是在推销公司产品，更像是一个发明家在展示自己最得意的作品。尤其是讲到 Dynamic Workers 时，他几乎是在“炫耀”——而听众能感受到这份自信来自实实在在的架构洞察。

### 延伸思考

对比 Anthropic 的新平台，Sunil 的策略是一种完全不同的哲学：不给开发者一个封装好的“框架”，而是提供两个超级原语——状态化持久计算（Durable Objects）与安全动态执行（Dynamic Workers）。这种从底层出发的设计，可能催生出远超现有框架想象力的 Agent 应用，也提出了一个关键问题：当你面对一场技术浪潮时，是等待框架帮你标准化，还是先拥有积木再自由搭建？

---

## 二、眺望“React 时刻”：Skills 可能是尚未到来的大一统标准 `[对未来的讨论]`

### 核心观点

Sunil 认为 Agent 领域还没有出现类似 React 那样决定性的抽象；用自然语言描述的“Skills”很有潜力成为跨语言、跨平台的翻译层，但仍需原创性突破来解决抽象粒度问题。

### 深度阐述

主持人追问 Sunil 如何看待 Agent 领域的标准化趋势——Cloudflare 是否会主动支持某种统一层？Sunil 没有给出肯定的回答，而是先由衷称赞了 Anthropic 平台中一个设计细节：**将运行环境与 Harness 框架分离。** 他说：**“They’re preparing for a world of software that hasn’t existed in the past.”**（他们在为过去从未存在过的软件世界做准备。）他认为这种面向未来的思维方式非常出色。

但他随即话锋一转，抛出了一个贯穿整场对话的核心比喻：**“No one has built the React yet.”**（还没有人做出那个 React 时刻。）他回忆 2013 年 React 发布时，许多人因 XML 式的组件描述而离场抗议，但正是这种反直觉的原创性奠定了未来所有前端框架的范式。今天的 Agent 领域到处都是 Harness 和 API，这个形状、那个形状，但还没有出现一个跨语言、跨公司、跨基础设施的、可复制的原创抽象。

他提出了一个让自己感到兴奋的候选——**Skills**。他解释道：Skills 本质上就是用自然语言（英语）描述的能力单元，它们天然具有多语言可读性和可伸缩性，并且可以打包代码。**“They scale well. It’s English. You can abstract it down. You can create skills on their own.”**（它们扩展性很好。就是英语。你可以向下抽象，也可以创造独立的技能。）他甚至口吻轻松地打趣说：“I’d be so happy if you say the future of software is Markdown files. Beautiful. Instantly accessible. A multi-language bridges the world.”（如果有人告诉我软件的未来就是 Markdown 文件，我会很高兴。美妙，真正零门槛，一座连接世界的多语言桥梁。）

但他也立刻指出了 Skills 的当前天花板：当你需要极度精确时，描述会变得和代码一样具体。**“When you have to start getting more and more specific, at which point you’re like I might as well just express it as code.”**（当你必须越来越具体时，你会想，我还不如直接用代码表达。）这个矛盾意味着，真正的突破还需要更原创的思考。

### 个人感受

话题从技术炫耀转向抽象思考时，Sunil 的语气明显放沉了。他不再斩钉截铁，而是带着一种谨慎的乐观和“我们在迷雾中”的诚实。他欣赏 Skills 的潜力，但更清楚它远非终点。这种发自内心的谦逊，反而比任何自信宣言都更具感染力。

### 延伸思考

当前大量创业公司和开源项目蜂拥推出 Agent 框架、代理协议、工具编排层。Sunil 的观察是一种及时的冷静剂：当所有人都忙着构建自己的“协议”时，是否已经忽略了那个真正破局者的到来？所谓“React 时刻”，可能需要一个足够陌生、足够反直觉的原创抽象才能触发——而在此之前，最重要的可能不是站队，而是保持对“可能性”的开放。

---

## 三、Slop Forks：一次善意 fork 引发的公关危机，以及开源社区的新伤口 `[Slop Forks 事件]`

### 核心观点

Sunil 在 JSCON 会议期间基于 Vercel 的 Just Bash 项目进行了一次友善的 fork 适配，却被 Vercel CTO 公开指责为恶意竞争，但他最终在社区声援中化解了危机。然而，这起事件的背后是开源社区正面临 AI 生成代码泛滥与虚假安全报告攻击的双重困境。

### 深度阐述

这是整场对话中最具戏剧性的部分。Sunil 的故事从一次美好的旅行开始。他在西班牙 JSCON 期间，看到一个令他兴奋的开源项目 “Just Bash”——这是 Vercel Labs 刚刚发布的、用 JavaScript 完整实现 Bash 的项目。他说：**“I loved it. What a great idea. A pure implementation of bash in JavaScript.”**（我很喜欢它。多么棒的想法。用纯 JavaScript 实现了 Bash。）

出于兴趣，他决定将它适配到 Cloudflare 环境。他让 AI 模型（Opus）为他工作，等他吃了一顿午餐回来，AI 已经生成了大约 **5000 行代码**。Sunil 想当然地把代码上传到 GitHub，并且有一个非常友好的计划：在西班牙好好度假，回家后仔细打磨，然后周一给 Vercel 提交一个标准的 Pull Request——就像他对待任何其他开源仓库那样。

然而事情完全超出预期。他回到酒店倒头就睡，一觉醒来发现手机里全是来自 Cloudflare 管理层的 DM：**“Have you checked Twitter?”**（你看推特了吗？）

他打开 Twitter 后，看到的是 Vercel 的 CTO 在公开抨击他的工作，暗示这是 Cloudflare 官方计划的恶意竞争。Sunil 坦言那一刻的感受：**“I saw my career fall apart with that message.”**（看到那条消息时，我感觉职业生涯要完蛋了。）他没有愤怒还击，而是做出了最真诚的回应：“Bro, I wanted to talk to you. I came back and napped.”（老兄，我想和你聊聊。我回来就去睡了。）

但接下来发生的事让他既意外又感动。**“Half the internet decided to stand up for me.”**（半个互联网都站出来为我说话。）人们自发地为他辩护，强调“Sunil 是最好的人”。整整 24 小时，他沉浸在从未体验过的社区温暖中。

这次经历也促使 Sunil 重新审视 Fork 在开源中的本质。他强调：**“Forking is a great sign of prestige, respect in my culture.”**（在我的文化里，Fork 是一种极高的尊重和荣誉。）他回顾开源历史：在 npm 和现代包管理器出现之前，软件通过 Usenet 和电子邮件分发，拿来、修改、再分享是最自然的工作流。他甚至在管理自己的 Agent SDK 仓库时，也遵循同样的理念：**“Every time someone tells me it’s kind of we think we can build something better, I’m like go for it.”**（每次有人告诉我他们觉得能做得更好时，我都说：放手去做。）

但现实远比理想复杂。Sunil 揭露了一个许多人不愿公开谈论的残酷现状：**开源仓库正在变成对抗性战场（adversarial grounds）。** 以 Agent SDK 为例，他们已经被迫关闭 Pull Request 通道，只允许提交 Issue。原因很简单：AI 让贡献代码的门槛降到零，仓库充斥着大量低质量、甚至恶意植入后门的生成代码。Sunil 无奈地笑道：**“The end result is I’m going to take a resolution and paste it into Opus. Whether you’re burning your tokens or my tokens, well, I prefer my tokens.”**（最终结果是我会拿着解决方案描述，贴到 Opus 里让它写。不管浪费的是你的 Token 还是我的 Token，我宁愿花我自己的 Token。）

最令人心惊的是**虚假安全报告**问题。Sunil 透露，当天早上他和 OpenClaw（一个关键安全项目）的创始人 Peter 交流后确认：**虚假安全报告已成为目前第一大攻击手段。** 攻击者精心伪造出看起来极为真实的安全漏洞报告，一旦维护者处理不当，就可能远程攻破核心仓库。Sunil 感叹：**“It’s really bad out there right now.”**（现在的处境真的很糟糕。）

### 个人感受

Sunil 在讲述整个事件时，一会无奈地笑，一会又陷入严肃。他对 Vercel CTO 没有任何恶意，反而多次强调自己和 Vercel 的团队成员私交甚好，当晚还约好一起喝啤酒。他用“旋转门的森林”来形容这个行业，强调保持友善和坦诚才是长存之道。而说到开源社区的反击时，他语调里带着无尽的感激。这是一个资深从业者在风云变幻中保持本真的珍贵切片。

### 延伸思考

Sunil 的故事揭示了一个深层矛盾：AI 极大地加速了开源协作的效率——fork、修改、适配变得前所未有地简单——但同时也摧毁了信任的基石。低质量贡献和恶意攻击正在迫使维护者关闭贡献通道，这实际上是对开源精神的回归还是背叛？从 Sunil 的经历中可以看到，未来开源项目的维护模式可能需要根本性变革：从“欢迎一切 PR”转向“维护者为核心的小团队+高质量的 Issue 驱动+AI 辅助审查”。而那些伪造安全报告的攻击，也将倒逼整个行业建立新的验证基础设施。

---

## 四、最终的召唤：原创，勇气，以及构建科幻 `[结尾呼吁部分]`

### 核心观点

Sunil 用充满激情的口吻恳求开发者：不要去做增量改进的重复工作，不要只追逐企业级大单，去构建那种基础设施和 LLM 现在几乎跑不动的“科幻级”东西——因为只有那样的原创，才能定义软件的下一次跃迁。

### 深度阐述

对话接近尾声时，主持人抛出常规的 “CTAs” 问题。Sunil 没有给出“下载 SDK 加入社区”这类套路话，而是说出了整场对话中最具升华意义的一段话。

他首先提到自己从 2018 年就开始倡导的一个概念：**Alpha Thought Leading（阿尔法思想引领）**。当时他在 React Rally 上尝试了 VR 测试工具，并自嘲地称其为“alpha thought leading”。多年后，他认为这个理念在当下变得比任何时候都重要。

**“In such a crazy world where any idea seems to work now like the clanker like will make it work for you. Don’t even try to do something incrementally better. Build sci-fi stuff.”**（在这个疯狂的世界里，任何想法似乎都能奏效，就连“Clanker”（指低质量套壳项目）也能帮你赚到钱。但请你连尝试增量改进都不必——去构建科幻级的东西吧。）

他用“sci-fi”（科幻）来定义那种让人眼前一亮、甚至有点不真实的概念。他鼓励人们用他提供的 Agent SDK（或其他工具）去做让自己家人惊叹的产品，而不是反复去做已经验证过的 CRUD 或聊天机器人模板。他特别强调：**“Don’t build it because you think you’re going to get a big enterprise deal. You own so much agency in changing the world.”**（不要因为你认为它能拿到大企业订单才去做。你拥有如此巨大的改变世界的力量。）

接着，他几乎是以恳求的语气说：**“I want people to just be original. I want them to try the wild stuff for which infrastructure and LLM almost fail you at this moment.”**（我希望人们原创。我希望他们去尝试那些基础设施和 LLM 几乎支撑不了的疯狂东西。）因为只有这种近乎不可能的尝试，才能推动平台进化到下一个阶段。

说到最后，Sunil 忍不住又补了一句经典的黑色幽默：**“I don’t need another agent framework. Nobody needs it. You should use Agents SDK.”**（我不需要另一个 Agent 框架。没人需要。你应该用 Agent SDK。）——当然，他马上开玩笑般补正：“Except yours. Except yours.”（除了你的，除了你的。）

### 个人感受

这是 Sunil 整场对话中最不像工程师、最像诗人的时刻。之前的技术讨论里他是冷静的分析师，Slop Forks 事件里他是无奈的亲历者，但此刻他变成了一个恳切的传教士。反复出现的“I’m begging you”（我恳求你们），不仅仅是一句综艺效果，而是包含了一种发自内心的焦虑和热情——他见过太多重复的轮子，见过太多被企业合同绑架的产品，他真心渴望看到意想不到的东西从开发者手中诞生。

### 延伸思考

在 AI Agent 创业极度泡沫化的今天，Sunil 的号召触及了一个核心问题：**原创性正在变成最稀缺的资源。** 当所有人在用同样的模型、相似的架构、互相抄袭的产品概念时，真正的突破一定来自那些“当前做起来很难、很愚蠢”的方向。比如：让 Agent 依靠 Durable Objects 持续运行一个月；让 Dynamic Workers 去探测未知的私有 API 并将结果反哺给模型。这些事现在做起来很别扭、很容易失败，但正是这种“不舒适感”才是通往下一个时代的钥匙。Sunil 用一整段对话在构建一个信念：**工具已经就位，剩下的只差你的一点点疯狂。**

---

# 精华收获

1. **Cloudflare 的 Agent 原语组合（Durable Objects + Dynamic Workers）不是功能插件，而是新一代 Agent 基础设施的 DNA。** 有状态的 Actor 模型与安全的动态代码执行能力，可以大幅简化和加速需要长期运行和复杂工具调用的 Agent 应用开发。如果你正在设计 Agent 架构，值得超越“框架思维”，直接思考如何利用这两个原语。
1. **开源环境正在经历 AI 带来的结构性危机：** 善意 fork 可能被误解为企业攻击；AI 生成的贡献泛滥反而催生“关闭 PR”的反现象；伪造安全报告已成为主流攻击手段。这对开源维护者提出的新要求是：提前设计贡献机制与验证流程，必要时宁可牺牲 PR 数量也要保护项目安全。
1. **最重要的一条行动建议：不要做增量改进，构建科幻。** Sunil 的呼吁不是空泛的理想主义，而是一个深耕行业多年、亲自经历过舆论漩涡的实干家发自内心的判断。在当前 AI 应用严重同质化的阶段，唯一有长期价值的事，就是去尝试那些让现有基础设施感到“吃力”的原创想法——即使它们现在看起来不像一个合格的市场需求。
---

<!-- TLDR: 别再造Agent框架了，用Cloudflare原语去构建让基础设施“吃力”的科幻级原创应用。 -->

<!-- TAGS: Cloudflare, AI Agents, 开源, 原创性, Durable Objects -->

<!-- RATING: 4 -->

---
