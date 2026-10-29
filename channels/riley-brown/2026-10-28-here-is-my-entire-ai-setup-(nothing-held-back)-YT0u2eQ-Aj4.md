---
title: "Here Is My ENTIRE AI Setup (Nothing Held Back)"
channel: "Riley Brown"
published: "2026-10-28"
source_url: "https://www.youtube.com/watch?v=YT0u2eQ-Aj4"
video_id: "YT0u2eQ-Aj4"
tags: ["AI agents", "工具栈", "Claude Code", "Codex", "Composio", "内容创作", "工作流自动化"]
rating: 4
language: "英文"
word_count: 20196
duration: "31:28"
---

# Here Is My ENTIRE AI Setup (Nothing Held Back)

- **Channel:** Riley Brown
- **Published:** 2026-10-28
- **Source:** https://www.youtube.com/watch?v=YT0u2eQ-Aj4
- **TL;DR:** 多 agent 时代真正的优势来自自由切换的架构和共享的插件/技能，而非对单一平台的忠诚。
- **Tags:** AI agents, 工具栈, Claude Code, Codex, Composio, 内容创作, 工作流自动化
- **Rating:** 4

## 版本

- [结构化文稿](2026-10-28-here-is-my-entire-ai-setup-(nothing-held-back)-YT0u2eQ-Aj4.structured.md)
- [原始文稿](2026-10-28-here-is-my-entire-ai-setup-(nothing-held-back)-YT0u2eQ-Aj4.transcript.md)

# AI Agent 工具栈的深度重构：一位内容创作者的完整工作流拆解

## 材料信息

- **标题**: Here Is My ENTIRE AI Setup (Nothing Held Back)
- **作者/来源**: Riley Brown（YouTube 频道）
- **类型**: YouTube 视频字幕
- **关键元数据**: 内容创作类 AI 工具测评视频，作者声称自费 10,000 美元测试各类 AI agent 工具，拥有超过 200 万粉丝，同时也是 AI 初创公司 Agent Native 的创始人

---

## 开篇引入

过去一年里，AI agent 工具遍地开花，从 Manus 到各种 Claude Code 包装器，每一位效率博主都在喊"我的最强工具栈"。但很少有人愿意把自己的全部细节——包括那些不适合展示的内部工具、插件配置、技能管理方式——毫无保留地摊开给观众看。

Riley Brown 的这期《Here Is My ENTIRE AI Setup》有点不同。他不仅展示了自己日常使用的三大 agent 平台（Claude Code、Codex/Dots、Grokbot），更关键的是揭示了一个大多数人忽略的核心问题：**当你同时使用多个 agent 平台时，你如何让它们之间的技能、插件和数据流通？** 以及——他花了 10,000 美元测试后得出的结论——**为什么你需要的不是单个"最强"工具，而是一个以协调器为中心的架构**。

这篇文章的价值不在于告诉你"用哪个工具"，而在于展示一个重度 AI 用户如何在现实业务中让 agent 真正替代人类助理的工作。他会用几分钟的视频编辑来生成短视频，用语音指令运筹帷幄，甚至能同时调度本地会话和云端会话。这已经不只是效率技巧了，这是一套完整的**人机协作工作流**。

---

## 详细内容

### Claude Projects：AI 协调器的核心枢纽 `[视频开头-中段]`

**核心观点**
Claude Code 不只是命令行工具，它的"Projects"功能可以把多个本地/云端会话整合到一个协调器下面，让你从手机或电脑统一调度所有 AI 工作。这是 Riley 整个工具栈的基石。

**深度阐述**

Riley 开门见山地指出了一个困惑很多人的问题：Claude Code 和 Codex 到底该怎么选？他的回答是——**前八个使用场景中，他选择 Claude Code，原因只有一个：Claude Projects 是最好的协调器**。

对于不熟悉的人来说，Claude Code 最初是 Anthropic 推出的命令行 AI 编程工具，它的强大之处在于可以访问你电脑上的所有文件，并执行"端到端"的复杂任务。Riley 举了一个例子：你只需要说——

> "Hey, there's a folder in my downloads called October 26th vlog. Please edit the video and post it on YouTube."（"嘿，我下载文件夹里有个叫 October 26th vlog 的文件夹。请编辑这个视频并发布到 YouTube。"）`[视频开头演示部分]`

——Claude Code 就能完成整个任务。这听起来像科幻，但 Riley 实际上每天都在做类似的事情。

但很多人不知道的是，Claude Code 除了可以在本地运行，还有一个**云端会话模式**。它会"旋转起来一台小电脑"（spin up a cloud session），执行任何你需要做的任务，而不用占用你的本地资源。Riley 强调这个区分非常重要："你并不总是需要你的电脑来完成所有任务。"

这就是 Claude Projects 发挥作用的地方。在 Claude 网页或 iOS 应用里，Projects 允许你创建不同的"协调器线程"（coordinator session）。以 Riley 的"Editor"（编辑器）Project 为例：当他发送一条指令——

> "Hello, I need you to please look at my latest videos in my downloads and I want you to make three clips and edit these locally on my computer and upload them to drive and give me a link to all three."（"你好，我需要你查看我下载文件夹里最新的视频，制作三个片段，在本地电脑上编辑，上传到云端硬盘，然后给我所有三个片段的链接。"）`[视频中段 Claude Projects 演示]`

——协调器会自动判断这个任务需要本地会话还是云端会话，然后把指令分配给正确的线程。Riley 展示了他的工作台：一些线程带有"电脑图标"（表示在本地运行），另一些没有（表示在云端运行）。他可以在 coordinator 线程里同时发起多个任务：一个在本地编辑视频，另一个在云端创建网页 artifact。

这里有一个特别震撼的细节：**他从手机完成了所有这些操作**。打开 Claude iOS 应用，进入侧边栏的 Projects，点击 "Editor" Project，所有运行中的会话一目了然。他甚至在从健身房走回家的路上，用语音创建了一份关于 Anthropic S1 文件的幻灯片演示文稿。

> "I created this presentation this morning using Claude Projects from my phone walking back from the gym."（"我今天早上从健身房走回来的时候，用手机上的 Claude Projects 创建了这份演示文稿。"）`[视频中段 Clade Projects 手机使用演示]`

这种"移动端 AI 协调"的模式，是 Riley 工作流的核心心智模型：**你不需要在电脑前才能调度 AI agent**。

**个人感受**

Riley 对这个功能的热情是显而易见的。他反复强调"这非常有用"、"我一直在用"，并且展示了他的工作台里同时运行着多个本地和云端会话。透过他的演示，你能感受到一种真正的解脱感——之前用 Claude Duet（Anthropic 的实验性 agent）无法启动本地会话让他很不满，而现在 Projects 补齐了这个缺口。这种兴奋不是表演出来的，而是来自一个重度用户找到了真正解决方案后的自然流露。

**延伸思考**

Riley 的"协调器模式"实质上是在重新定义人与 AI 的关系。传统上，我们用 AI 是"人在工具面前操作"，但 Projects 模式下，人是站在调度台后面的导演，只是给出模糊的意图（"把这个视频剪辑出来"），agent 自己决定用哪些工具、在哪些环境执行、如何分配资源。这种从"操作者"到"指挥者"的角色转变，可能是未来五年知识工作最重要的变革之一。

另外，Riley 提到他把自己创建的 Project——比如 "Rick Cra Claude project"（一个定制的个人 agent，类似于 Claude Duet）——视为最佳实践。这暗示了一种新的软件开发范式：你不再需要用传统方式构建内部工具，而是直接在 AI 平台上定制自己的 agent 角色。

**精华收获**
- Claude Projects 是连接本地和云端 agent 会话的协调器
- 同一个 Project 可以管理多个并发的本地/云端任务
- 手机上的 iOS 应用能完整控制所有会话
- 你可以从手机发起本地任务，只要你的电脑开机并登录 Claude Code
- 语音输入可以完全替代打字指令

---

### 用 Claude Code 构建应用：从设计到部署的全流程 `[视频中段]`

**核心观点**
Claude Opus 5.5 在前端设计上具有显著优势，配合 Claude Projects 的"随时随地迭代"能力，Riley 将所有内部工具的开发、部署和管理都迁移到了这个平台上。

**深度阐述**

Riley 是 AI 初创公司 Agent Native 的创始人，但他不只是一个"把工具推荐给用户"的博主。他确实在用自己的 AI 工具栈**构建真正的产品**。他展示了一个名为 "Native Note" 的内部工具——这个工具是他"10 个不同 SaaS 应用的混合体"，包含了 Excalidraw 的克隆版（白板绘图工具）、自己的书签存储系统、YouTube 数据分析仪表盘、甚至一个视频编辑平台。

他说了一个很重要的点：**这个内部工具的每一次迭代，都是从手机上的 Claude Projects 发起的**。他演示了一个真实的会话：

> "Hey, what I need you to do right now is I actually don't like how on native note it has my pinned videos. Can you please remove that? And then also move the conbon title to the top. We also don't need that little subtitle or this like horizontal line. And please make the filter by title thing pinned to the left instead of on the right. And yeah, please make the background have a little bit more texture to it, almost like it's like a white board."（"嘿，我现在需要你做的事是，我不喜欢 Native Note 上的置顶视频。请移除它，然后把 conbon 标题移到顶部。我们也不要那个小标题或这条横线。请把按标题过滤的功能固定到左边而不是右边。还有，请让背景多一点质感，几乎像一块白板。"）`[视频中段 Native Note 迭代演示]`

注意这段指令的自然程度——他没有用"请修改 CSS 文件的第几行"，而是用**产品经理式的模糊描述**（"多一点质感"、"几乎像一块白板"）。Claude 成功地解读了这些模糊意图，并发起了一个本地会话来执行。几分钟后，任务完成了四分之三，只需要刷新页面就能看到更新。

为什么他选择 Claude Code 而不是 Codex 来构建应用？他的理由非常明确：

> "Claude Opus 5.5 right now, in my opinion, at least for the things that I'm doing, it is the best at coding. Especially if it is very front-end focused. It's just very good at front-end. And GPT 6.1 Soul is also frontier and it's amazing. It's just not the best at like front-end design."（"就目前而言，至少就我做的事情来说，Claude Opus 5.5 是最好的编程工具，特别是在前端方面。GPT 6.1 Soul 也是一流的，但在前端设计上不如 Claude。"）`[视频中段 Claude vs Codex 编程对比]`

这是整个视频最重要的对比之一：**虽然两者都是顶级模型，但 Claude Opus 5.5 在视觉/前端设计上有明显的优势**，而 Codex 的强项在别处（后面会详细讨论）。对于需要大量视觉资产的内容创作者来说，这个差异决定了工具选择。

**精华收获**
- Claude Opus 5.5 是前端设计最强的模型
- Claude Projects 让"从手机发起部署指令"成为可能
- 模糊的、人类化的描述（如"多一点质感"）也能被 agent 正确理解
- 内部工具可以完全用 AI agent 来构建和迭代

---

### 设计与幻灯片：Claude 的可视化超能力 `[视频中段]`

**核心观点**
Claude Opus 5.5 擅长将复杂、数据密集的信息转化为视觉化、易理解的形式，这让 Riley 能把任何 PDF、Excel 或研究材料快速变成精心设计的幻灯片。

**深度阐述**

就在视频发布的前一天，Anthropic 发布了他们的 S-1 文件（IPO 招股书）。Riley 从手机上用 Claude Projects 和语音对话，将这个"数据和文字密集"的 S-1 文件转化为了一份精心设计的幻灯片演示文稿。

> "Yo, this S1 came out. It's very text heavy and data heavy. I need to properly visualize it, organize it how we normally organize my videos and create a slide deck."（"嘿，这份 S1 发布了，文字和数据都很密集。我需要你把它可视化，按我们平时组织视频的方式组织，然后创建一份幻灯片。"）`[视频中段 Anthropic S1 可视化演示]`

结果令人印象深刻：Claude 创建了包含收入流向图、运营成本分析、客户集中度可视化（"大约 250 个客户每年消费 1000 万美元以上，1900 人消费 100 万美元以上"）的完整演示，还包含了"收入扩张"漏斗图——展示了一个客户从第一年消费 1 美元发展到第九年消费 9 美元的过程。Riley 形容这种增长速度"绝对前所未闻"。

更关键的是，Riley 没有把这个功能当作"制作精美 PPT"的工具，而是把它作为**学习机制**。他说：

> "This is how I learned about everything on the S1 was just with this slide deck."（"我就是通过这份幻灯片学到了 S1 里的所有内容。"）`[视频中段 学习方法论]`

这句话揭示了一个重要的心智转变：**可视化不再是"输出"，而是"输入"**。让 agent 为你提炼复杂信息并转化为视觉形式，本身就是一种深度理解的过程。这远比直接读原始 PDF 更高效。

他还在 Claude Projects 中使用了 **Claude Design Mode**（设计模式），这是与 Projects 集成的功能。他展示了如何用它来"创建 Figma 风格的设计板"，可以生成多个选项，选择想要的，然后直接让 agent "把他推送到生产环境"或"把这些设计实现到我们正在构建的应用里"。设计在云端进行，实现则在本地会话中完成——用户不需要知道这个切换过程的细节。

> "It may design it in the cloud and may implement it using your computer and you don't even need to like know that. You can just let your agent do its thing."（"它可能在云端设计，可能用你的电脑实现，你甚至不需要知道这些。你只需要让你的 agent 做它该做的就好。"）`[视频中段 设计与实现分离]`

**延伸思考**

这里有一个容易被忽略的洞察：Riley 提到他创建这份 S1 幻灯片"只用了三个提示"。这暗示 Claude 对信息组织和视觉表达的强大能力——通常需要几小时的设计工作现在可以在三次对话中完成。这不仅是效率的问题，它改变了"理解复杂信息"的方式。传统的学习路径是"读原始材料 → 做笔记 → 理解"，现在变成了"让 AI 把信息可视化 → 通过视觉形式吸收 → 用 AI 迭代改进理解"。这种认知捷径的效率提升是数量级的。

**精华收获**
- 让 Claude 把任何复杂数据（PDF/Excel/S1 文件）转化为视觉化幻灯片
- 三个提示就可以完成一个完整的、设计精良的演示文稿
- 可视化是学习的最佳方式——让 agent 为你提炼信息比直接阅读更高效
- Claude Design Mode 可以在云端设计、本地实现，用户无需关心切换

---

### 视频编辑：AI Agent 最激动人心的应用场景 `[视频中段]`

**核心观点**
视频编辑是 Riley 目前使用最频繁、也最看好未来发展前景的场景。Claude 可以端到端完成视频编辑——从理解需求到生成最终成片——并且他正在开发一个开源工具让这项能力普惠化。

**深度阐述**

Riley 直接展示了两个"完全由 AI 编辑"的视频——"How Smart People Are Using AI"和"How I've Been Using Claude Duet"。他明确说：

> "I've been using Claude non-stop to edit my videos... both of these videos were fully edited by AI. Now, there was some iteration, but they were edited by AI."（"我一直在不停地用 Claude 编辑视频……这两个视频完全由 AI 编辑。当然有迭代，但确实是 AI 编辑的。"）`[视频中段 视频剪辑演示]`

他演示了如何用 Claude Projects 创建"动画解释器视频"。这是一个以特定风格解释 Andrey Karpathy 推文的动画视频（Karpathy 是 OpenAI 联合创始人之一）。Claude 创建了 V1 版本（画面太近），然后通过几次提示迭代到 V2 版本（画面更宽敞、效果更好）。这个视频在 Twitter 上获得了 **2000 个点赞和 16 万次观看**。

> "And I posted this video on Twitter and it actually got 2,000 likes and 160K views. And many people were commenting asking me about the skills. They're like, 'Yo, share how you made it and do you mind sharing the prompt that led to the graphics.'"（"我把这个视频发到 Twitter 上，获得了 2000 个赞和 16 万次观看。很多人评论问我技能是什么，问我是用什么提示词来生成图表的。"）`[视频中段 Twitter 反馈]`

这引出了他正在构建的 **V2** 项目——一个被他称为"视频编辑界的 GitHub"的开源工具。他解释了这个想法：

> "This is an app that I'm working on that will be free and open source. It is the GitHub for video editing. It will allow your agents to create versions of the app that you create. And you'll be able to track all of the prompts and all of the different files that you use to create each video. People on your team will be able to fork your video. You'll be able to share your videos and make them public."（"这是我在开发的一个应用，免费且开源。它是视频编辑的 GitHub。它允许你的 agent 创建多个版本，你能追踪每个视频的所有提示词和文件。团队成员可以 fork 你的视频，你可以分享和公开视频。"）`[视频中段 V2 项目介绍]`

这个项目的核心创新是**版本控制**——GitHub 为代码解决的问题（版本追踪、协作、fork、公开分享）现在被应用到了视频领域。而且它是"视频编辑器无关的"（video editor agnostic）：你可以用任何工具栈、任何 agent 平台来使用它。

Riley 非常强调这个项目的免费性和开放性："This is free and this will always be free."（"这是免费的，而且永远免费。"）`[视频中段 V2 免费承诺]`

**延伸思考**

V2 项目的出现传递了一个信号：当 AI 视频编辑的提示词变得越来越复杂（不只是"剪掉这段"，而是包含完整的叙事逻辑、视觉风格、节奏控制），这些"提示词资产"本身就变得有价值。创作者会想要共享、迭代、协作这些提示词，就像开发者共享代码一样。Riley 看到了这个未来的雏形，正在用基础设施的方式提前布局。

更深一层看，这反映了 AI 时代的一个本质问题："提示词"正在成为新的"代码"。在代码时代，GitHub 解决了代码的版本管理和协作问题；在 AI 创作时代，需要一个类似的东西来解决提示词和创作资产的管理问题。Riley 的 V2 项目正是这种趋势的早期预警。

**精华收获**
- Claude 可以端到端完成视频编辑，包括动画效果
- 优秀的 AI 视频编辑需要迭代（V1→V2 的改进是常态）
- 视频编辑正从"工具操作"转向"提示词资产"
- "视频编辑的 GitHub"是尚未被填补的巨大空白

---

### Codex/Dots：以语音为中心的业务管理平台 `[视频中后段]`

**核心观点**
Claude Code 负责创建资产（应用、设计、幻灯片、视频），而 Codex 负责管理业务（邮件、日历、消息、电脑操作）。Riley 通过 Dots 的语音功能，实现了一种"行走工作法"——在散步中完成所有的协调和运营任务。

**深度阐述**

在视频的中后段，Riley 揭示了两个平台之间的明确分工：

> "Cloud code is creating assets for my content business... Codex I use for my personal assistant administrator, and it keeps track of my calendar, my emails, all the messages in Slack."（"Claude Code 为我的内容业务创建资产……Codex 适用于个人助理和管理工作，它跟踪我的日历、邮件和 Slack 上的所有消息。"）`[视频中后段 Claude vs Codex 分工]`

这个分工听起来简单，但它是整个工具栈的核心逻辑：**Claude 是"生产部门"，Codex 是"运营部门"**。作为一个内容创作者，Riley 的日常工作是"创建视频、设计、应用"（Claude 的领域），但还有大量时间是"回复邮件、安排日程、协调团队"（Codex 的领域）。前者用 Claude Code，后者用 Codex。

而 Codex 最大的优势是**电脑使用能力**（computer use）。Riley 描述了一个典型的工作流：

> "Whenever I edit a video and I really like the video and I get to my final version, I just asked my dot. I said, 'Hey, the video's ready, post it on YouTube.' And what it'll do is it'll analyze the transcript of the video. It will go through in Chrome, upload the YouTube video there, fill out all of the details, get the description ready, look at my emails, if it's a sponsored video and I need to include a link in the description, it'll add it there automatically and then it will save it as a draft."（"每当我编辑好视频，到了最终版本，我就对我的 Dot 说：'嘿，视频好了，发布到 YouTube。' 它会分析视频文字稿，打开 Chrome，上传视频，填写所有细节，准备描述，查看邮件，如果是赞助视频需要在描述里加链接，它会自动添加，然后保存为草稿。之后 Dot 会发消息说草稿好了，让你检查后再发布。"）`[视频中后段 电脑使用工作流]`

这种"让 agent 替你操作电脑"的能力是 Codex 的核心优势。Riley 提供了一个简单的建议："下次你在手机上，笔记本电脑开着，就去找你的 Dot，说'启动一个 Codex 会话，在电脑上做任何事，边做边截图'，然后你就能看到你的 agent 在怎么用你的电脑。"

但他强调，**最主要的使用方式是通过 Dots 的语音功能**。他展示了一个完整的语音交互：

> **Riley**: "Hey pal, I need you to check the recent changes that I've made to native note. Can you spin up a new codex session? Investigate it. And I actually want you to add that same background that we added to native note to the other pages like to the background of the list view and in the calendar view as well. Can you spin up a new codex session and then push your changes to prod."
> **Dot**: "On it. I'll open a fresh Codex session and dig through those recent changes now. I'm getting a new session ready for that background update now, including a prod push once it's checked."
> **Riley**: "Thank you buddy."（"谢谢你，伙计。"）
> **Dot**: "Of course."（"当然。"）

然后 Dot 自动创建了 Codex 会话（"Unify Native Note Backgrounds"），并在云端会话和本地会话之间协调。

这个交互格外引人注目的地方在于它的**自然性**。Riley 跟 Dot 说话的方式就像跟一个真实的人类助理说话一样。他叫它 "buddy" 和 "pal"（伙计、伙伴），语气随意而友好，而 Dot 的回应也带着类似的人格化温度。这不仅是技术进步，更是一种新型的人机关系的雏形：agent 不再是一个工具，而是一个具有个性的协作者。

Riley 还提到他"90% 的邮件"是通过这种方式处理的：

> "Every morning there's probably 20-25 emails that I need to hear and I just talk to my dot. I said, 'In order of importance, please read me my emails.' And then my DOT will talk to me and be like, 'This one's from this person and they said this.' And then it'll read the email and I'll be like, 'Okay, dot, I want you to respond with something like blah blah blah.' And then it'll read it out to me and I'll be like, 'Send it.' And then I'll do that on a walk."（"每天早上大概有 20-25 封需要处理的邮件，我就跟 Dot 说'按重要性排序，读给我听'。然后 Dot 会读邮件内容，我口述回复，Dot 读给我确认，我说'发送'。这些我都走在路上完成。"）`[视频中后段 语音邮件工作流]`

**个人感受**

Riley 对"行走工作法"的热爱是显而易见的。他反复提到"我讨厌坐在电脑前处理邮件"，"只要有机会走路，我都会去走"。他甚至早上会提前一个半小时出门，在去健身房之前先走一小时，边走边用语音和 Dot 对话，处理邮件和 Slack 消息。这已经不只是工具推荐了，而是一种生活方式的宣言：AI agent 让他可以离开桌面，在移动中获得生产力。这种从"被束缚在电脑前"到"随处可工作"的转变，可能是 AI 工具给人的最大解放。

**精华收获**
- Codex 的电脑使用能力是 Claude 无法替代的核心优势
- 语音 + 行走 = 高效邮件和消息处理的新模式
- Dot 是 Codex 的"协调器"，可以启动云端或多会话的 Codex 会话
- 和 agent 像人类助手一样对话，是最高效的交互方式

---

### Superhuman：赞助商插播 `[视频中段广告插播]`

**核心观点**
Superhuman 的 AI 连接器可以让邮件和文档协同工作，与 ChatGPT 连接后能自动把邮件转化为可执行计划。

**深度阐述**

这期视频中途插播了 Superhuman 的赞助内容。Superhuman 是一款主打高速体验的邮件客户端，Riley 不仅作为赞助方展示产品，还提到自己已经用它很久。

他展示的工作流是：通过 Superhuman 的 Mail 连接器，在 ChatGPT 中询问"关于我即将发布的视频的邮件有哪些？交付截止日期和最新反馈是什么？"然后使用 Superdocs 连接器把这些信息转化为内容日历，为每个视频生成下一步行动项，并标记缺失的信息。当情况变化时，他可以直接让 AI 更新文档。

虽然这是赞助商内容，但它恰好验证了 Riley 前面阐述的核心思想：**连接器的根本价值在于让数据在不同系统之间流动，而不是被锁定在各自的孤岛里**。这和后面即将讲到的 Composio 工具形成了呼应。

---

### Composio：agent 的"护照"和中心化插件系统 `[视频后段]`

**核心观点**
Composio 是 Riley 工具栈中被忽视但至关重要的部分。它像一张"agent 护照"，允许所有 agent 平台共享同一套插件、技能和 API 连接，让用户不再被绑定在任何一个平台。

**深度阐述**

Riley 在这段内容里描述了一个困扰所有多平台 agent 用户的问题：每个 agent 平台都有自己的插件系统。ChatGPT 有一套插件，Claude Code 有另一套插件，Grokbot 有第三套。每次切换平台，你都要重新配置。这不仅繁琐，还让你被锁定在某个平台的生态里。

Composio 解决了这个问题。Riley 把它称为 **"agent passport"**（agent 护照），因为它让所有 agent 平台都能共享同一套插件和技能。

> "Once you create your account, all you have to do is go to apps and you have literally every plugin you've ever created. Claude and GPT have no built-in YouTube plugin... They have that on Composio. So all you have to do is plug in your Composeio and then you get access to all 30 of these apps that I've added."（"一旦你创建账户，进入应用页就能看到所有你创建的插件。Claude 和 GPT 没有内置的 YouTube 插件…… 但 Composio 有。你只需要在 agent 平台里接入 Composio，就能使用全部 30 个应用。"）`[视频后段 Composio 介绍]`

他列出了自己的 Composio 应用列表：
- **ClickUp**：管理品牌合作合同
- **Convex**：存储所有应用的数据
- **Gmail**：邮件
- **Calendar**：日历
- **Superhuman**：主要使用的邮件客户端
- **Notion**：存储有用信息
- **Vercel**：托管应用
- **Exa**：比内置搜索引擎更好的网页搜索
- 以及更多...

他说："如果每次测试新的 agent 平台都要重新登录所有应用，那会非常烦人。"

Composio 的另一个杀手级功能是 **Instant**。它在技术上相当于一个 API 聚合器，让用户可以直接访问 Tavi、Exa、11 Labs、FAL 等热门 API 服务，而无需单独设置每个 API 密钥。Riley 特别提到，通过 FAL 可以访问"所有流行的视频模型，而且比 Higsfield 便宜得多"（FAL 是一个 AI 模型聚合平台，提供多个图像/视频生成模型）。

此外，Composio 还管理着 Riley 的 **技能库**（skills）——他在那里存储了 20 个高频使用的技能。Riley 的核心观点是：

> "I don't want to have to set up skills on Claude Code and then tell Claude Code to send the skills to Codex or send them to Grokbot. I just centralize them. All of my skills are in one place and all I need to do is connect the Composio integration and it has all of these skills."（"我不想在 Claude Code 上设置技能，然后再告诉 Claude Code 把技能发给 Codex 或 Grokbot。我只需要把它们中心化。所有技能都在一个地方，我只需要接入 Composio 集成，就能获得全部技能。"）`[视频后段 技能中心化理念]`

**精华收获**
- Composio 让所有 agent 平台共享同一套插件和 API 连接
- 它解决了"切换平台时重新配置"的痛点
- Instant 功能聚合了所有主流 API，消除了繁琐的密钥设置
- 技能中心化让 agent 之间的能力可移植

---

### 记忆：尚未解决的难题 `[视频后段]`

**核心观点**
虽然技能和插件可以中心化，但 **记忆** 仍然是最大的痛点。Riley 还没有找到简单的方法让所有 agent 平台共享同一个记忆系统。

**深度阐述**

这是整个视频最诚实的时刻之一。Riley 已经解决了插件、技能和流程的中心化问题，但还有一个更大的问题悬而未决：

> "The same way I centralize my skills and plugins, I want to centralize my memory. Codex, Claude Code, Grokbot, Muse, Claude Duet, all of these platforms keep a memory on you, but when you switch from platform to platform, the memory does not persist."（"像我中心化技能和插件一样，我也想中心化记忆。Codex、Claude Code、Grokbot、Muse、Claude Duet，所有这些平台都会存储关于你的记忆，但切换到不同平台时，记忆无法持久保留。"）`[视频后段 记忆问题]`

他尝试过将 SuperMemory 连接到 Composio，但发现"无法让它足够频繁地更新记忆"，导致切换平台时上下文丢失。他的问题很明确：有没有一个简单的工作流，能让 agent 之间的记忆像技能和插件一样无缝共享？

> "Let me know in the comments."（"请在评论区告诉我。"）`[视频后段 开放性求助]`

**延伸思考**

Riley 的"记忆"问题触及了 AI agent 领域最深层的矛盾：每个平台为你构建的记忆都是私有的。你用了 Claude 三年，Claude 了解你的全部偏好、工作方式、决策历史——但当你切换到 Codex 时，一切归零。这不仅是技术问题，也是数据主权问题：你的 AI 记忆应该属于谁？

有一种可能的解决方向是"外部记忆系统"——比如一个专门的向量数据库或知识图谱，所有 agent 都可以读写。但这里的问题（正如 Riley 发现的）是更新频率和同步机制。如果 SuperMemory 每天只更新一次，那么当你早上用 Claude 开会、中午切到 Codex 处理邮件时，记忆已经过时了。未来的解决方案可能需要更实时的同步机制，或者一个开放标准的 agent 记忆协议。

这值得每一个 AI 重度用户关注：**你的 agent 记忆是一个竞争优势，而不能被锁定在任何一个平台里。**

**精华收获**
- 记忆无法跨平台持久化是多 agent 的致命痛点
- 目前的解决方案（如 SuperMemory）更新频率不够实时
- 这个问题涉及数据主权和平台锁定
- 需要一个开放标准的"agent 记忆协议"

---

### Grokbot：Twitter 的专用 agent `[视频末段]`

**核心观点**
Grokbot 并不是 Riley 日常交互的主要平台，但它的 Twitter 访问能力让它成为重要的补充工具。他通过 Webhook 让其他 agent 可以调用 Grokbot 来执行 Twitter 相关的任务。

**深度阐述**

Riley 的态度很明确："I don't actually go to the Grokbot UI ever really."（"我几乎从不打开 Grokbot 的用户界面。"）Grokbot 在工具栈中扮演的是**专家角色**：它负责所有和 Twitter 相关的事情，这是它的独特优势。

他的使用方式相当巧妙：在 Claude Projects 里设置一个 "Grokbot webhook" 技能，当 Claude 需要 Twitter 相关的研究时，它会自动向 Grokbot 发送请求。Grokbot 收到请求后开始工作，完成后返回结果。这意味着 Claude 可以"借用"Grokbot 的 Twitter 访问权限，而用户只需要在一个界面操作。

> "I can basically just interface with my favorite agent platforms which is codecs or dots and clawed with projects and they can send requests to Grokbot. I don't actually use the Grokbot UI. I just basically have my agents delegate to Grokbot because Grokbot has full access to Twitter."（"我基本上只用我最喜欢的 agent 平台——Codex/Dots 和 Claude Projects——它们可以给 Grokbot 发请求。我不用 Grokbot 的界面，只是让我的 agents 委托给 Grokbot，因为它有完整的 Twitter 访问权限。"）`[视频末段 Grokbot 使用方法]`

他还提到一个使用场景：可以直接让 Claude Code 通过 Grokbot 检查自己的 Twitter 私信（DMs），而不需要切换界面。

**精华收获**
- Grokbot 是"Twitter 专家"，但不值得单独使用
- "Webhook 委托"模式让多平台协作成为可能——Claude 可以调用 Grokbot
- 一个 agent 可以成为另一个 agent 的"工具"
- 最佳架构不是"选择一个最好的"，而是"让每个 agent 做它最擅长的"

---

### 工具栈全景总结 `[视频末段]`

**核心观点**
Riley 的完整 AI 工具栈是一个以 Claude Projects 和 Dots 为前端、以 Composio 为中心化枢纽、以 Grokbot 为补充专家的三层架构。

**深度阐述**

在视频尾声，Riley 做了简洁的总结：

> "I use cloud code specifically projects to coordinate all of the assets that I need to create apps, designs, slides and video editing. I use codecs for its computer use. All business and coordination tasks... And then obviously plug this into all of the other tools that I use. And the way that I centralize that is through Composio. And then Twitter is such a large part of my business... I connect it to Grokbot because it has full access to my Twitter account and doing research on Twitter."（"我用 Claude Code，特别是 Projects，来协调所有需要创建的资产——应用、设计、幻灯片和视频编辑。我用 Codex 来做电脑操作、所有业务和协调任务。然后通过 Composio 中心化所有插件。Twitter 是我业务的重要部分，所以我连接 Grokbot，因为它有完整的 Twitter 访问权限。"）`[视频末段 工具栈总结]`

这基本复盘了三个核心工具的分工：

1. **Claude Code + Projects**：资产的创造者。前端设计最强，视觉呈现最佳。负责构建应用、设计幻灯片、编辑视频。
2. **Codex + Dots**：业务的运营者。电脑使用能力无与伦比。负责邮件、日历、消息、电脑操作。
3. **Grokbot**：Twitter 的专家。通过 Webhook 被其他 agent 调用，做 Twitter 研究和 DM 管理。

而 **Composio** 是贯穿三个平台的底层基础设施，让它们共享插件、技能和 API。

Riley 还提到他"可能每两个月会重做一次这个视频"，因为 agent 平台"会进化"，"也许 Meta 会发布新模型，Google 会发布更好的 agent 平台"，"可能有人会发布比 Composio 更好的竞争对手"。这种持续的适应性是这个快节奏领域的关键。

**个人感受**

Riley 的整个叙述透露出一种 **"开放心态"** 和 **"工具不可知论"**（tool-agnosticism）。他并不忠诚于任何一个 AI 平台——他测试过 10,000 美元的各类工具，最终选择的是一套能让他自由切换的架构。这种态度在当前 AI 圈尤为重要：今天的最强工具可能在三个月后过时，而真正重要的不是工具本身，而是你如何设计工作流程来最大化工具的协同效应。

Riley 最后说："Thank you guys so much for watching this video. I hope you guys got a lot of value."（"非常感谢大家观看这个视频，希望你们获得了很多价值。"）这句话虽然简单，但从上下文来看，他是真诚的。他确实在分享自己"实验室"里最核心的东西——不只是工具名称，还有使用方法、分工逻辑，甚至说"Nothing Held Back"（毫无保留）。

**延伸思考**

如果你把 Riley 的架构抽象出来，它其实是在构建一个**通用 agent 操作系统**。就像传统的操作系统有文件系统（相当于 Composio 的插件中心）、调度器（相当于 Projects/Dots 的协调器）、设备驱动（相当于各平台的插件）一样，Riley 在 AI 领域正在做类似的事情。不同之处在于，传统操作系统由一家公司提供（微软、苹果），而 agent 时代的操作系统可能是开放的、组合式的，由用户自己拼装。

这也引发了一个更深层的问题：**当我们拥有了这些工具，我们的角色是什么？** Riley 的答案很清楚：你变成了导演，而不是操作员。你给出方向，agent 去执行。这需要一种不同的技能——不是"知道怎么操作工具"，而是"知道怎么清晰地表达意图"。这是一种全新的素养，目前还没有被广泛教授。

**精华收获**
- Claude 负责创造（前端设计 + 视频编辑），Codex 负责运营（电脑使用 + 消息管理），Grokbot 负责 Twitter 研究
- Composio 是打通所有平台的"共享层"
- 真正的强大不是选择最好的工具，而是设计开放、可组合的架构
- AI 时代的核心技能：用自然语言清晰地表达意图，让 agent 去执行
- 你的 AI 记忆是你的资产，不应该被平台锁定

---

## 整体核心洞察

Riley Brown 的 AI agent 工具栈本质上是构建了一套"以协调器为核心、以共享层为枢纽"的开放架构。他没有被任何一个 AI 平台的生态锁定，而是通过 Composio 和 Webhook 让不同平台的能力自由流通。这代表了一种未来的工作方式：你会像导演一样，通过自然语言向 agent 描述意图，agent 自动决定使用什么工具、在什么环境执行、如何把结果传递给你。工具本身会不断迭代，但架构的核心理念——**自由切换、能力共享、语音优先**——才是持久的资产。

---

<!-- TLDR: 多 agent 时代真正的优势来自自由切换的架构和共享的插件/技能，而非对单一平台的忠诚。 -->
<!-- TAGS: AI agents, 工具栈, Claude Code, Codex, Composio, 内容创作, 工作流自动化 -->
<!-- RATING: 4 -->
