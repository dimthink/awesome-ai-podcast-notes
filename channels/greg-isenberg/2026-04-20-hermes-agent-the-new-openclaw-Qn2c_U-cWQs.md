---
title: "Hermes Agent: The New OpenClaw?"
channel: "Greg Isenberg"
published: "2026-04-20"
source_url: "https://www.youtube.com/watch?v=Qn2c_U-cWQs"
video_id: "Qn2c_U-cWQs"
rating: 4
language: "英文"
word_count: 10331
duration: "37:01"
---

# Hermes Agent: The New OpenClaw?

- **Channel:** Greg Isenberg
- **Published:** 2026-04-20
- **Source:** https://www.youtube.com/watch?v=Qn2c_U-cWQs
- **TL;DR:** Hermes Agent 通过内置记忆、稳定性和 Open Router 省钱方案，将个人 AI 代理的 token 成本降低 90%，并可在安卓手机上运行。
- **Rating:** 4

# Hermes Agent: The New OpenClaw? —— 深度安装指南与个人AI代理的未来

## 材料信息

- **标题**：Hermes Agent: The New OpenClaw?
- **作者/来源**：Greg Isenberg（频道），嘉宾 Imran
- **类型**：YouTube 视频字幕（对话式技术教程）
- **关键元数据**：发布日期未知，时长约 30-40 分钟（根据字幕长度估算），主要涵盖：Hermes Agent 的安装、与 OpenClaw 的对比、Android 部署、Obsidian 集成、GStack 技能、省钱技巧、提示词范例等
---

## 开篇引入

你有没有遇到过这样的情况：你满怀热情地安装了一个 AI 代理，结果发现它没有记忆，每次都要重复相同的指令；或者它动不动就崩溃，让你花在重启上的时间比真正使用的时间还多；又或者你月底一看账单，发现自己不知不觉花了几百美元在 token 上？如果你点头了，那么今天这篇文章就是为你准备的。

最近在技术圈里，一个名叫 **Hermes Agent** 的工具正在病毒式传播。人们称它为“OpenClaw 杀手”。但“杀手”这个标签往往意味着炒作，不是吗？为了搞清楚它到底是真材实料还是又一个昙花一现的项目，Greg Isenberg 请来了他的朋友 Imran——一位能将复杂技术概念讲得极其清晰的极客。Imran 不仅自己从 OpenClaw 迁移到了 Hermes，还在安卓手机上跑起了代理，甚至让代理帮他整理冰箱里的食材来规划每日食谱。

本文将带你完整还原这场对话的核心内容。你将学到：Hermes Agent 到底比 OpenClaw 强在哪三步？如何用一行命令安装它？怎么通过 Open Router 把 token 费用降低 90%？如何在便宜的安卓手机上部署一个永远在线的个人代理？以及最重要的——**你应该问你的代理哪些问题，才能让它真正改变你的工作和生活**。读完这篇文章，你不仅会拥有一个可落地的安装指南，更会获得一种全新的思维模式：在 AI 时代，使用代理不再是技能，而是基本要求。

---

## 详细内容

### 一、为什么从 OpenClaw 迁移到 Hermes？——三个致命的痛点 `[开头部分 - 对话早期]`

**核心观点**

Imran 在使用 OpenClaw 时遇到了三大问题：无内置记忆、频繁崩溃、token 消耗不透明。Hermes 正是为解决这三点而设计的。

**深度阐述**

在技术社区中，OpenClaw 曾是一个颇受欢迎的个人代理项目。但当 Imran 真正尝试将它融入日常工作流时，他遭遇了令人沮丧的体验。他直言不讳地指出了三大“致命伤”：

**第一个问题：没有内置记忆系统。** 这意味着每次你给代理分配任务，它都像是一个失忆的人。你需要反复告诉它同样的背景信息、同样的偏好、同样的工作流程。Imran 的原话是：“I kept having to tell it to do the same things over and over again because there was no built-in memory system.” `[对话早期]` 这不仅浪费时间，更让代理无法随着使用次数的增加而变得更聪明——而“越用越聪明”本应是个人代理的核心价值。

**第二个问题：网关频繁崩溃。** Imran 回忆道，有一天他不得不每小时重启一次 OpenClaw 的网关。他说：“I felt like I spent more time setting up OpenClaw than I was actually using it to make my life better.” `[对话早期]` 这是一个致命的体验问题：如果一个工具的存在本身就是为了节省时间，却让你花费更多时间在维护上，那它就失去了存在的意义。

**第三个问题：token 消耗完全不可见。** 你无法知道代理到底在后台做了多少次 API 调用，也无法追踪哪些任务消耗了最多的计算资源。Imran 的描述很直接：“it was eating up tokens and I had no visibility into how or why.” `[对话早期]` 对于个人用户或小型团队来说，这种不透明性很容易导致月底收到远超预期的账单。

**个人感受**

Imran 在描述这段经历时，语气中带着明显的挫败感。他不是在批评一个项目，而是在分享一个真实用户从满怀希望到失望的过程。他说自己“quickly migrated” —— 快速迁移了。这种果断的背后，是对时间成本和效率的极度敏感。

**延伸思考**

这三个问题其实揭示了当前个人 AI 代理领域的普遍困境：**记忆、稳定性和成本可见性**。很多开源项目专注于展示“能做什么”，却忽略了“长期使用的可行性”。如果你正在评估任何代理工具，不妨先用这三个维度去衡量：它能记住我吗？它能稳定运行一周不重启吗？我能清楚地知道每一分钱花在哪里吗？

**精华收获**

- **记忆是智能的基础。** 没有持久记忆的代理，本质上只是一个带 API 调用的脚本。
- **稳定性比功能数量更重要。** 一个能稳定运行一周的工具，比一个每天崩溃但功能花哨的工具更有价值。
- **成本透明是信任的前提。** 如果一个工具不能让你看到 token 消耗的细节，你就无法做出理性的使用决策。
---

### 二、Hermes 的核心优势：记忆、稳定、省钱 `[中期对话]`

**核心观点**

Hermes 通过 SQLite 数据库实现长期记忆，稳定性远超 OpenClaw，并且通过与 Open Router 集成大幅降低 token 成本。

**深度阐述**

Imran 在对比中明确指出，Hermes 并非只是“另一个代理”，而是对上述三大痛点的针对性解决方案。

**优势一：内置的、可搜索的长期记忆**

Hermes 的记忆机制非常巧妙。它使用标准的 SQLite 数据库 —— 这和大多数网页应用使用的数据库类型相同。每当你成功完成一个任务，Hermes 会自动将这次经验写入记忆。更强大的是，即使某次操作没有被显式保存，Hermes 也能实时搜索所有历史日志来找到相关信息。Imran 举了一个令人印象深刻的例子：“even things like API keys. If you forget to save them to an environment variable, but you kind of passed it to the agent, it can actually search through and find it for you.” `[中期对话]`

这意味着什么呢？意味着 Hermes 不仅能记住你教它的事情，还能在你犯错时帮你补救。你不需要像对待其他代理那样小心翼翼，它会像一个细心的助手一样在你身后默默记录。

**优势二：稳定性大幅提升**

Imran 说：“I haven’t had to restart it in like over a week.” `[中期对话]` 相比之下，OpenClaw 曾让他每小时重启一次。这种稳定性的提升，将一个“玩具”变成了一个可以依赖的生产力工具。对于想要 24/7 运行的自动化任务（比如每天早上自动整理邮件），这种稳定性是必不可少的。

**优势三：40+ 内置工具 + 可选的 Open Router 省钱方案**

Hermes 开箱即带有超过 40 种工具，涵盖浏览器操作、网页搜索、定时任务（cron jobs）、图像生成、Home Assistant 智能家居控制等。你不需要像使用 OpenClaw 那样去四处寻找和安装工具。

而真正让 Imran 兴奋的是省钱策略。他展示了自己在 Hermes 中使用 Open Router 的画面。Open Router 是一个模型聚合平台，上面有各种模型的实时价格，甚至还有免费模型（比如某个时段 Nvidia 的 Neotron 是免费的）。Imran 对比了价格：使用 Claude Sonnet 和使用 Qwen 3.6 Plus，输入 token 的价格相差近 10 倍。他做了一个具体的计算：

- 之前使用 OpenClaw，每 5 天花费约 **130 美元**。
- 迁移到 Hermes 并配合 Open Router 后，每 5 天花费降至约 **10 美元**。
- **降幅超过 90%。**
他的核心省钱方法论是：**对于重复性任务，让代理先写一次代码（确定性的自动化），而不是每次都让 LLM 参与推理。** 比如，如果你每天都要生成一份销售报告，你可以让 Hermes 写一个脚本，然后把它设为一个 cron job 定时运行。这样，第一次可能消耗一些 token，但之后每次运行几乎不消耗任何 token。Imran 用软件工程中的“DRY (Don‘t Repeat Yourself)”原则来类比这一思路。

**精华收获**

- **记忆 + 稳定性 + 成本控制 = 可长期使用的个人代理。** 三者缺一不可。
- **Open Router 是降低 token 成本的关键工具。** 学会在免费模型、低成本模型和高性能模型之间切换。
- **用确定性代码替代每一次的 LLM 调用。** 这是从“玩代理”到“用代理”的核心思维转变。
---

### 三、安卓手机上的 Hermes：低功耗、永远在线、传感器访问 `[对话中后期]`

**核心观点**

通过 Termux 和 Termux API，你可以在便宜的安卓手机上运行 Hermes，访问手机传感器数据，实现真正的“随身代理”。

**深度阐述**

当 Greg 问 Imran 为什么要在安卓手机上安装 Hermes 时，Imran 给出了一个极具想象力的回答。

**技术实现路径：**

1. 在安卓手机上安装 **Termux** —— 一个终端模拟器，让你的手机像电脑一样拥有命令行环境。
1. 安装 **Termux API** 应用（可通过 F-Droid 开源应用商店获取）。这个 API 让你能够访问手机的所有传感器数据：电池电量、Wi-Fi 网络、音量、摄像头、屏幕亮度、振动马达，甚至短信。
**为什么这样做？**

Imran 给出了几个非常实际的场景：

- **低功耗、永远在线的专属代理设备**：Mac Mini 经常缺货且价格不菲，而便宜的安卓手机（甚至旧手机）加上一张 SIM 卡，就能成为一个随身携带的、始终在线的代理。
- **短信自动化**：代理可以读取发送到该手机号的短信，甚至可以自动处理两步验证（2FA）的验证码。这对于自动化登录流程非常有用。
- **真实设备发帖**：社交媒体调度工具（如 Hootsuite、Buffer）通过 API 发帖往往会降低自然 reach，因为平台能识别出这是第三方工具。而如果让 Hermes 直接在安卓手机上模拟真实用户操作（点击屏幕、发送通知、发布内容），平台会认为这是来自真实设备的操作，保留完整的 reach。Imran 说：“you can post the content directly from the device. … it will still show that it came from a device with like a real MAC address.” `[对话中后期]`
**个人感受**

Imran 在展示他的“Cookie Monster”代理（运行在 Solana Seeker 安卓手机上）时，语气中带着一种孩子般的兴奋。他把自己的代理都命名为《芝麻街》中的角色，这种幽默感让技术演示不再枯燥。他说：“I still have a lot of room for expansion if I need to add more agents. There’s still a bunch more muppets I can go through.” `[对话中后期]`

**延伸思考**

安卓部署的可能性远不止于此。想象一下：你可以把手机放在车里，让代理监控 GPS 并自动记录停车位置；你可以把它放在厨房，让它通过摄像头识别冰箱里的食材并给出食谱；你甚至可以运行多个手机，每个手机负责一个社交媒体账号，构建一个去中心化的内容发布网络。这种“设备级”的自动化，是纯云端 API 无法实现的。

**精华收获**

- **安卓手机 + Termux + Hermes = 一个低于 100 美元的随身超级代理。**
- **真实设备操作比 API 调用更有“真实性”**，在社交媒体自动化等领域具有独特优势。
- **传感器数据是新的输入维度**：电池、位置、短信、摄像头……这些是电脑代理无法触及的领域。
---

### 四、GStack 与 Obsidian：从个人助手到创业导师 `[对话后期]`

**核心观点**

GStack 将 Y Combinator 的创业方法论封装成一个技能，Obsidian 则成为代理为你自动整理知识库的绝佳载体。

**深度阐述**

**GStack：YC 风格的创业代理**

Greg 问 Imran 什么是 GStack，Imran 解释道：GStack 由 Y Combinator 总裁 Garry Tan 创建，它将 YC 加速器的核心方法论——每周找出什么有效、什么无效，提出正确的问题，然后将其转化为代码和决策——变成了一个开源的技能。以前，这些知识只对 YC 内部的创业者开放；现在，你可以直接把它“拧”到你的 Hermes 代理上。

Imran 甚至提前将 GStack 移植到了 Hermes（在官方广泛支持之前）。对于不在硅谷、没有创业网络但正在开发产品的个人开发者或小团队来说，这相当于拥有了一位虚拟的 YC 合伙人，每周帮你审视产品方向。

**Obsidian：代理自动整理的第二大脑**

Imran 坦言自己以前并不是 Obsidian 的用户，他一直用 Apple Notes 并“听天由命”。但 Obsidian 基于 Markdown 文件的特性，让代理可以极其方便地读取和修改。现在，他的 Hermes 代理每天自动生成一个“home.md”文件，里面包含：

- 本周重要事项
- 今日待办
- 即将到来的旅行
- 日间工作相关事项
- 个人事务
全部由代理自动整理。Imran 说：“I would not have been able to go through the painstaking effort of putting this together by myself every single morning.” `[对话后期]`

**个人感受**

Imran 在展示他的 Obsidian 文件时，突然意识到屏幕上的内容过于私人化，连忙让 Greg 模糊处理。他说：“This knows way too much.” `[对话后期]` 这一幕非常真实——当一个代理真正开始了解你的生活、你的习惯、你的拖延事项时，那种亲密感既是强大的体现，也带来了隐私方面的警觉。但正如 Greg 所说，这种亲密感是你“投入工作”的结果，如果你从零开始，它一开始不会知道那么多。

**精华收获**

- **GStack 将顶级创业方法论民主化了。** 如果你在做产品，不要错过这个免费技能。
- **Obsidian 是代理的理想知识库**，因为 Markdown 是机器可读的纯文本格式。
- **让代理帮你整理，而不是自己手动整理。** 这是从“使用工具”到“拥有数字管家”的质变。
---

### 五、如何提问？——七个改变你使用习惯的提示词 `[对话结尾部分]`

**核心观点**

使用代理的核心技能不是安装和配置，而是知道该问什么问题。Imran 分享了七个能真正提升代理价值的提示词。

**深度阐述**

Imran 认为，学习如何使用 Hermes 本身不是技能——它正在成为一个基本要求。真正稀缺的能力是：**你知道该让代理为你做什么。** 他当场分享了自己每天使用的几个关键提示词：

1. **“What have I been procrastinating on?”**（我在拖延什么？）
代理可以访问你的待办列表，找出那些被你忽略但重要的事情。

1. **“What is the most important thing to work on today?”**（今天最重要的工作是什么？）
帮助你在每天开始时聚焦优先级。

1. **“What are some tasks that I’m doing every single day that I could or should automate?”**（我每天做的哪些任务可以或应该被自动化？）
这是从“手动”到“自动”的关键追问。

1. **“What is a tool that you can build me tonight that would make my life easier tomorrow?”**（你今晚能为我构建什么工具，让我明天过得更轻松？）
这个提示词鼓励代理主动创造，而不仅仅是响应指令。

1. **“Is there anything important today that I missed?”**（今天我有没有错过什么重要的事情？）
作为每日复盘。

1. **“What is something you should build for the work I do?”**（你应该为我的工作构建什么？）
让代理站在你的角度思考效率提升点。

1. **“What is one way that you can set up as a cron job?”**（哪一件事情可以设置为定时任务？）
专门针对重复性任务的自动化。

此外，Imran 还展示了一个极其有趣的例子：他找到了一个 MIT 在 1960 年代开发的早期自然语言处理心理治疗程序（ELIZA 风格的“Weizenbaum”程序），然后直接将维基百科文件丢给 Hermes，说“把这个变成技能”。结果，他的代理拥有了一个可以每天对话、帮助他自我实现的“心理顾问”技能。这个例子完美诠释了 Imran 的核心观点：**过去需要三年时间构建的 NLP 系统，现在你可以在几分钟内通过一个提示词复现。**

**个人感受**

Imran 在分享这些提示词时，语气中带着一种“这难道不是显而易见吗”的轻松，但同时又意识到对很多人来说这是一种全新的思维方式。他说：“This does kind of seem obvious to me. But to many people, it’s kind of a new way of thinking.” `[对话结尾部分]`

**精华收获**

- **提示词的质量决定了代理的价值。** 不要只问“帮我做X”，而是问“我应该做什么”“我忽略了什么”“什么可以被自动化”。
- **把整个互联网当作你的技能库。** 任何有趣的文章、论文、工具，都可以尝试“喂”给代理，让它变成你的专属能力。
- **每天花 5 分钟问这 7 个问题**，一个月后你的代理会变得完全不一样。
---

### 六、安全、更新与最终建议 `[对话结尾]`

**核心观点**

Hermes 仍是 beta 软件，需要每日更新；安全可以通过 Tailscale 和主动审计来加强；最终建议是：专注于“用代理做事”而非“定制代理本身”。

**深度阐述**

**关于更新：** Imran 诚实地指出，Hermes 仍然是 beta 软件。他展示了自己的一个实例，9 天没更新，落后了 535 个提交。他建议：“You do still have to update it every night.” `[对话结尾部分]` 这是一个现实：开源项目迭代速度快，不更新可能会错过修复或新功能。

**关于安全：** Greg 提出了一个关键问题：那些预装的技能（如 iMessage、Find My）安全吗？Imran 给出了几个应对方案：

- **主动审计**：你可以直接问代理“Is this a secure setup? Tell me why or why not.” 代理会检查你的电脑上是否有明文存储的密钥、防火墙配置是否薄弱等。
- **Docker 隔离**：Hermes 支持在 Docker 容器中运行，将代理与主机文件系统隔离。
- **Modal 无服务器部署**：作为另一种隔离选项。
- **Tailscale 虚拟网络**：Imran 强烈推荐安装 Tailscale，让你的所有设备（手机、电脑、安卓手机）处于同一个虚拟网络中，然后你可以通过 SSH 从任何地方安全地访问和监控你的代理。
**关于最终建议：** 当 Greg 问“应该迁移到 Hermes 吗？”时，Imran 没有简单回答“是”或“否”。他提出一个更重要的观点：**定制代理本身不是技能，真正重要的是你用代理完成了什么。** 他见过太多人沉迷于调整配置、美化界面、寻找完美工具，却从未真正用代理完成一件实际工作。他引用了一个比喻：“It’s like 90s tuner car culture … you can go find the parts you want and you can put them on, but … customizing is not the skill.” `[对话结尾部分]`

**个人感受**

Imran 自己在一家基金工作。他分享了一个真实的价值量化：“I’m able to talk to more founders and have better conversations with them because a lot of the background work is now handled by my personal agent. … If we can talk to 20% more companies or 30% more companies, we have better signal. … It just makes me better at my job.” `[对话结尾部分]` 他把自己节省下来的时间转化为具体的商业结果——更多的创始人对话、更好的投资信号、更高的基金回报。这种务实的视角，值得每一个技术爱好者深思。

**精华收获**

- **每日更新是 beta 软件的常态**，不要抱怨，把它变成习惯。
- **安全不是自动的**，主动询问代理来审计你的配置。
- **Tailscale + SSH = 远程访问代理的最佳组合。**
- **永远不要忘记：代理是手段，完成工作是目的。** 如果你发现自己花了 10 小时配置代理只为了节省 1 小时的工作，你需要重新评估优先级。
---

## 总结：在 AI 时代，使用代理是基本要求

这场对话最打动人的地方，不是 Hermes 的技术细节，而是 Imran 和 Greg 反复强调的一个观念转变：

> “Learning how to use Hermes agent is not actually the skill. It’s going to become the requirement.” —— Imran
在不久的将来，会使用个人代理就像今天会用搜索引擎一样平常。真正拉开差距的，是你能否提出正确的问题，能否识别出生活中哪些重复性任务值得被自动化，能否把代理从一个“玩具”变成你工作中不可或缺的“同事”。

Imran 最后留下了一个邀请：他的基金叫 Alif（alif.build），他也在社交媒体上以“Imran”的身份分享更多教程。但他真正的期待是——你从这里离开后，不再只是“阅读”关于代理的内容，而是真正去安装、去提问、去让它改变你的每一天。

---

<!-- TLDR: Hermes Agent 通过内置记忆、稳定性和 Open Router 省钱方案，将个人 AI 代理的 token 成本降低 90%，并可在安卓手机上运行。 -->

<!-- TAGS: AI代理, 自动化, 开源工具, 生产力, 个人知识管理 -->

<!-- RATING: 4 -->

---
