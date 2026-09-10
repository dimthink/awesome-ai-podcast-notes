---
title: "How we built Grok Bot in a month | Roman Ugarte (SpaceXAI)"
channel: "Lenny's Podcast"
published: "2026-09-08"
source_url: "https://www.youtube.com/watch?v=maSdsTLaMuU"
video_id: "maSdsTLaMuU"
tags: ["AI Agent", "产品设计", "Grok Bot", "Cursor", "创业方法论"]
rating: 5
language: "英文"
word_count: 39200
duration: "1:22:43"
---

# How we built Grok Bot in a month | Roman Ugarte (SpaceXAI)

- **Channel:** Lenny's Podcast
- **Published:** 2026-09-08
- **Source:** https://www.youtube.com/watch?v=maSdsTLaMuU
- **TL;DR:** 一支被"关进洞穴"的小队一个月造出最火 AI 产品，成功源于"从零开始"和"把 AI 当同事"两条铁律
- **Tags:** AI Agent, 产品设计, Grok Bot, Cursor, 创业方法论
- **Rating:** 5

## 版本

- [结构化文稿](2026-09-08-how-we-built-grok-bot-in-a-month-roman-ugarte-(spacexai)-maSdsTLaMuU.structured.md)
- [原始文稿](2026-09-08-how-we-built-grok-bot-in-a-month-roman-ugarte-(spacexai)-maSdsTLaMuU.transcript.md)

# 一个月造出全球最火 AI 产品：Grok Bot 的诞生内幕

**材料信息**
- **标题**：How we built Grok Bot in a month | Roman Ugarte (SpaceX AI)
- **作者/来源**：Lenny's Podcast（主持人 Lenny Rachitsky，嘉宾 Roman Ugarte）
- **类型**：播客访谈（YouTube 视频，含自动生成字幕）
- **关键元数据**：访谈时长约 90 分钟；嘉宾 Roman Ugarte 是 Cursor 第 15 号员工，历任增长负责人、产品负责人，目前领导 Grok Bot 产品；播客录制于 Grok Bot 公开发布约 3 周后；字幕存在多处语音识别错误（如 Grokbot/Grockpot/Grogbot 均指同一产品，Kurser/Curser 指 Cursor，Codeex/co-work 指竞品），本文已根据语境校正

**开篇引入**

这是一个关于"一个月从零到一"的故事。当全世界最强大的 AI 实验室都在拼命往自己的旗舰产品里塞更多功能、更多标签、更多入口时，一支被"关进洞穴"的小团队却反其道而行——他们从零开始，砍掉了几乎所有能砍的东西，只为了让 AI 像一位真正的同事那样为你工作。

Roman Ugarte 是这场实验的亲历者。他是 Cursor 的第 15 号员工，见证了这家公司从 15 人扩张到上千人，又在最关键的时刻被派去孵化一个全新物种。一个月后，Grok Bot 内部上线；三周后，它面向全球发布。发布仅三周，它已经成为"全世界最热门、最令人兴奋的新 AI 产品"——连主持人 Lenny 自己都说，他把大量工作流从 Cursor 和 Codex 迁移到了 Grok Bot，"感觉像是一个非常重要的时刻"。

但这期访谈真正珍贵的，不是产品本身的光环，而是 Roman 罕见地、具体地拆解了那些"当时完全不显而易见、事后回看却至关重要"的决策：为什么不做进 Cursor？为什么每个 bot 要有一台自己的云电脑？为什么团队要亲手给两三百人做一对一 onboarding？为什么"下架功能"比"上线功能"更重要？

如果你正在思考 AI 产品应该长什么样、agent 的下一个形态是什么、或者在巨头夹缝中如何做出突破性产品，这场对话值得你逐字读完。以下是完整的深度重构。

---

## 一、起源：一支"洞穴小队"的疯狂实验 `[访谈段落 01-06，对应开场白与第一个问题]`

**核心观点**
Grok Bot 并非 Cursor 的自然延伸，而是一次彻底的"白纸实验"——一支不到十人的小队被物理隔离，目标只有一个：为知识工作者打造一个能真正把 agent 交付给全公司的产品。

**深度阐述**

访谈一开始，Lenny 就难掩兴奋。他说自己电脑窗口里常年开着 Grok Bot，日常使用 15 个不同的 bot，"一天用一百次"。几天前他去参加了一个 Grok Bot 的线下聚会，全场爆满、座无虚席，人们争先恐后分享自己如何使用它。在喧嚣的 AI 世界里，要穿透噪音成为"最热门的产品"是一条极高的门槛——而 Grok Bot 做到了。

Roman 则用一句反问奠定了整个故事的情感基调：他回忆起一个月前亲手为 Lenny 做 onboarding，那时 Lenny 还"带着怀疑"。而现在，看到这么多人真正用起来，"我们非常高兴"。

随后 Lenny 讲了一个细节，这个细节几乎就是 Grok Bot 成功的最佳注脚。在那次 onboarding 中，他没有提任何复杂需求，只是随口说了一句"帮我写条推文，推广我的最新一期播客"。Grok Bot 不仅自己判断出"最新一期"到底是哪期，还写出一条质量相当高的推文。那一刻，Lenny 心里冒出的念头是："哇，这真的很厉害。"

**原话引用**："So I'm just like uh come up with a tweet to promote my last episode... And it was actually very good. It figured out what the hell last episode was, how to promote it. So I actually remember in the moment being like wow this is really good." `[访谈段落 03]`
（我当时就说，帮我写条推文推广上一期节目……结果它写得非常好。它自己搞清楚了"上一期"到底是哪期、该怎么推广。我当场就惊了：这也太厉害了。）

Roman 于是给出了起源故事的完整版本：这从一开始就是一次"从零开始、白纸一张"的构建。团队长期以来一直有个感觉——他们擅长的是为开发者和工程师打造产品，在这个过程中积累了大量关于"如何做出好 agent"的直觉。但一个自然的问题浮现出来：**如果把这套直觉用到知识工作上，会是什么样子？**

答案就是组建一支极小的内部团队。Roman 特别强调"极小"这个词——只有一小撮人，被安排到办公室一个独立的角落，用私密的 Slack 频道，与公司其他人完全隔离，**像进了洞穴一样，目标只有一个：打造一个出色的知识工作产品，把 agent 带给公司里所有非工程岗位的人**。

**关键时间数据**：从第一行代码到内部可用的原型，只用了大约一个月。

Roman 的判断非常明确：**如果这个团队更大，这件事根本做不成**。因为产品需要每天做出大量的微观决策，其中一些决策——他预告"后面会细讲"——是过去在其他产品面上从未做过的、完全不显而易见的。如果是一个大团队，带着"6 到 12 个月长期愿景"的思维方式，他们根本走不到最终落脚的那个地方。

**延伸思考**

这里藏着一个反直觉的组织学洞见：**大团队倾向于做"安全的"决策，而突破性的产品往往诞生于"不安全的"微观决策中**。当一个团队被要求在大愿景下保持一致时，每个小决策都会被"是否契合长期规划"审视，从而趋向保守；而当一支小团队被物理隔离、只被赋予一个模糊而大胆的目标时，他们反而敢于在每一个细节上赌一把。这种"洞穴式隔离"不只是资源集中，更是一种**认知保护机制**——保护那些还没法被大组织理解的想法，免受"这不合理"的质疑。

---

## 二、从零开始，而非在 Cursor 里加一个标签页 `[访谈段落 07-09]`

**核心观点**
把知识工作能力"外挂"到现有编码产品上，是行业的默认选择，但 Grok Bot 团队选择了最"痛苦"的路——从零重做一个新产品，因为只有这样才能掌控每一个像素、保持单一而一致的产品愿景。

**深度阐述**

Lenny 抛出了一个几乎所有产品人都会问的问题。他观察到：Anthropic 从编码 agent 出发，发现"天啊这是个巨大的机会"，然后在自家产品里演化出知识工作的组件（Cowork）；OpenAI 则在 Codex 上投入，让它对各类任务都有用。**为什么 Cursor 的团队没有选择把知识工作能力直接做进 Cursor，而是另起炉灶做一个全新的产品？这个决定当时有多争议？**

Roman 的回答斩钉截铁："**这一点都不显而易见。**" 他承认，这正是那些"当时经过大量讨论、但现在我非常满意"的原始决策之一。

他给出的核心逻辑是：**一个新产品意味着你能掌控体验的每一个像素，并保持一个关于"知识工作将走向何方"的一致愿景**——这一切都包含在这个新事物里，而这正是成功的重要贡献因素。

但团队确实认真评估过"复用 Cursor"这条路。毕竟，人们本来就在拿编码产品做非编码任务。Roman 指出了这条路的三个"小伤口"（paper cuts）：

1. **产品本身对非技术用户有 intimidate（威慑感）**——一个为开发者设计的产品，对普通人来说天然有距离感；
2. **品牌联想**——"Cursor"这个名字本身就是给程序员用的；
3. **竞品路径的反面教材**——他观察到一些竞争对手的做法是"全都塞进一个界面"，每出现一种新形态就加一个新标签页，结果界面变得杂乱（cluttered）。

**原话引用**："And it feels a little cluttered and I think for users they can feel that this was not a single consistent vision of the way that work should work and instead it's three different visions that all kind of share a screen... it is kind of a shipping your org chart style thing that I think users are reacting negatively to." `[访谈段落 08]`
（它显得有点杂乱，用户能感觉到这不是一个关于"工作应该如何进行"的单一一致愿景，而是三个不同愿景共享同一个屏幕……这本质上是一种"把你的组织架构图直接上线"的做法，我认为用户对此反应负面。）

"**shipping your org chart**"（把你的组织架构图直接发布出去）是这段访谈中最锋利的一句表达。它精准描述了一种常见的产品病：每个团队都想在同一个界面里留下自己的痕迹，最终用户看到的是公司内部的权力结构，而不是一个为使用者思考的整体体验。

Roman 的结论是：那就**彻底从零开始**，看看能走到哪里。未来或许仍有机会把其他产品面的用户引到这个更"bot 原生"的体验中，但首要任务是让人们拥有一个"极其简单、又极其强大"的体验。

Lenny 顺着这个话题补了一个耐人寻味的观察：**Codex 走的是相反的路**——它本来分散，现在反而在往"一个东西"收敛。所以这个市场里"多种路径都能走通"，但**路径本身会反过来塑造你**，也许未来回头看会说："当初那个决定其实不是最好的。"

**精华收获**

- 当一项新能力天然需要一个"新受众"时，把它塞进老产品里通常是错误的——你会同时继承老产品的品牌包袱、认知负担和组织政治。
- 判断标准不是"技术上能不能复用"，而是"**能否给这个新用户群一个单一、一致、无妥协的愿景**"。
- 警惕"shipping your org chart"：如果一个界面上出现了彼此打架的多个入口，说明你在暴露内部结构，而不是在服务用户。

---

## 三、两百场手工 onboarding：把用户当成真人来对待 `[访谈段落 10-13]`

**核心观点**
核心团队亲手为 200-300 名早期用户做一对一 onboarding，这不仅是产品质量的打磨，更是一次"校准盲点"的认识论实验——他们故意不"引导证词"，让真实的用户行为塑造产品。

**深度阐述**

Lenny 提到一个在硅谷听起来很"反效率"的做法：Grok Bot 团队手工 onboarding 了两三百人，其中包括他自己。他问 Roman：**为什么觉得这有必要？从中学到了什么？这个阶段持续了多久？**

Roman 的坦诚令人印象深刻："**最开始几次 onboarding 相当痛苦**。幸好你那次是好的，Lenny（笑）。" 他特别强调，**核心团队必须亲自在场**——坐在一通 20 分钟的电话里，亲眼看着"电脑起不来"或者"用户完全懵了"。因为只有这样，你才会在挂掉电话的下一秒说："**这种事绝不能再发生，我们明天就得解决，因为明天我还要 onboarding 下一个人，必须变得更好。**"

这个阶段大约持续了**两周**，onboard 了几百人。Roman 说，他们学到的远不止产品本身。

**关于"不引导证词"的方法论**：

在下线之前，团队内部已经在使用 Grok Bot，而内部使用天然会产生一些"群体共识"——由于公司同事不断分享使用技巧，某些使用模式开始浮现。团队觉得这些模式对世界可能有用，但**不敢确定，更不想去引导外部用户**。

一个具体例子：内部上线后的一两周，最常见的模式是**一个人拥有 5-10 个 bot，每个 bot 被赋予不同的业务领域和职责边界**，像约定俗成的不同"泳道"。到了第二周末，内部 Slack 开始出现这样的消息——**有人把自己团队里表现突出的一个 bot 提拔成"首席助理"（chief of staff）**，然后自己主要跟这个"首席助理"对话，由它把任务分发给其他 bot，管理整个 bot 团队。

**原话引用**："And there are some funny screenshots of people like actually telling their uh you know the bot they're promoting that they're promoted and the bot is asking if they get a raise and you know is their token budget higher all of these things." `[访谈段落 11]`
（还有些特别搞笑的截图：人们真的在"通知"被提拔的 bot 它升职了，而 bot 居然会问是不是有加薪、token 预算是不是更高了之类的。）

这些有趣的画面背后，是一个正在浮现的新范式：**"bot 团队"结构**——一个 bot 像 chief of staff 一样协调其他 bot。团队注意到了这个方向，并且在公司里开始有更多人朝这个方向迁移，但**它从来不是公司里的多数派**——人们使用这个产品的方式千差万别。

正因为如此，在 onboarding 和早期访问计划中，团队刻意**不去"leading the witness"（引导证人）**——他们绝不会说"创建一个 chief of staff bot，让它这样管理其他 bot"。他们要让早期用户**自己走到那里**。而结果是，许多用户确实自己就走到了这个模式。**只有在那之后，产品里才有了一个略微表达观点的设计——"这似乎是个有效的模式，值得轻微鼓励，但绝不能是一扇单向门"。**

Roman 还提到了第二个观察：**用户到底想看多少内部细节**。这也是 Grok Bot 与其他"看起来相似"产品的关键差异。

**原话引用**："A lot of the internal mechanics of how Grok Bot works are not shown to the user. And the reason for that is we think as these models get smarter, the same way that your teammate, you know, you wouldn't ask for second-by-second updates of exactly all the buttons they're pressing and websites they're going to, I think it's too much to ask your bots to do that, too." `[访谈段落 12]`
（Grok Bot 内部运作的很多机制并不展示给用户。原因是：随着模型越来越聪明，就像你不会要求同事秒秒更新他按了哪些按钮、去了哪些网站一样，我认为要求 bot 这样做也太过分了。）

于是他们走向了完全相反的方向：你发送一条消息、告诉 bot 去做一件事，它就**直接开始做**，并在它认为合适的时候给你**递进式更新**——你只会看到那个像 Slack 一样的绿色"正在输入"圆圈在转动，表示它活跃着、在工作、很快会回复你。但你**看不到工具调用、看不到它在自己电脑上的每一次点击**。

团队对这个方向态度很坚决，但也收到了合理的反馈——"我很想看到我 bot 的待办清单，想知道它大概如何排列优先级"。这是很好的反馈。但最关键的是：**没有人想要那种又长又乱的文本流和思维链序列**。这反而进一步确认了他们的方向是对的。

**个人感受**

这段最打动我的是那种"**团队亲自坐进混乱里**"的态度。在今天这个讲究"规模化"、"自动化增长"的行业里，一群顶尖工程师愿意花两周时间、亲手做几百场 onboarding，是一种近乎固执的坚持。它背后是一种信念：**产品与真实人类之间那 20 分钟的摩擦，任何遥测数据都无法捕捉**。只有当工程师自己坐在那通电话里、看着用户彻底困惑的表情，他们才会产生"这必须明天就修好"的紧迫感——这是 A/B 测试和用户调研报告永远给不了的。

**延伸思考**

Roman 提到的"不引导证词"，其实是一种**刻意保护产品的可发现性**。如果团队直接把"chief of staff bot"的模式教会用户，他们能得到一屋子照做的用户，但会永久失去一个关键信息：**这个模式到底是客户自己想要的，还是被我们灌输的？** 只有让用户自己走到那个模式，团队才能确信这是产品的"自然形状"，而非"人工形状"。这是所有做新产品的人都该学习的方法论：**把最宝贵的内测阶段，用来发现用户会自发走到哪里，而不是验证你的假设。**

---

## 四、时间线：一个月构建，一周内测，三周公开发布 `[访谈段落 14-15]`

**核心观点**
Grok Bot 的整个开发周期极度压缩：一个月从第一行代码到内部 beta，三周从内部 beta 到公开发布，而录制时距离公开发布又只过了三周。

**深度阐述**

Lenny 特意让 Roman 把时间线讲清楚，因为这三个数字实在惊人。Roman 复盘如下：

- **一个月**：从第一行代码 → 内部 beta（一个可用、团队兴奋的产品）→ 公司全员 all-hands 上的正式推出；
- **三周**：从内部 beta → 公开发布（面向数百万用户需要大量工作）；
- **三周**：从公开发布 → 录制本访谈的当下。

Lenny 的反应堪称经典："从我的角度看，它已经改变了世界。" 他随即追问：**在那三周（内部 beta 阶段）里，变化最大的是什么？**

Roman 的回答只有三个字，却是本访谈最有分量的答案之一：**"我们大量地下架（unshipped）。"**

他坦承，如果在公开发布前两周看这个产品，你会看到一个完全不同的样子——里面塞满了核心团队想拿内部反馈的**实验性功能**，还有一堆**"伪开发者"式的可见性工具**：比如他们曾把模型的**内部思考过程**、它存储的**具体记忆**都暴露出来，用于调试。

**原话引用**："But we had to really aggressively trim what we think the user absolutely needs to see in the surface versus what they don't... how can we just ruthlessly simplify this product and abstract away anything the user doesn't need to actively be thinking about." `[访谈段落 16]`
（但我们必须非常激进地修剪：用户到底绝对需要看到什么、不需要看到什么……如何无情地简化这个产品，把所有用户不需要主动思考的东西抽象掉。）

第二个大动作，Roman 总结为"**让它真正能工作（just work）**"。他指出，人们想要的并不是一个布满下拉菜单和花哨功能的 AI，而是**一个你描述任务、它去执行、然后带着完整成果回来，或者带着一个可反馈的中间产物回来让你继续引导**的东西。

但要真正兑现这个承诺，**关键不在于做一堆"路线图式"的功能，而在于在后台攻下五个非常重要的问题**——这些问题大多数用户不会直接"看到"，但会**深深"感受到"**：当你的 bot 正在执行任务却点不对按钮，或者无法登录某个网站，你的任务就彻底卡住了。

因此在那几周里，团队收集了大量**"人们实际交给 bot 的真实任务"**，量化它们，并按周观察、在这些任务类别的重要维度上持续攀爬。

**精华收获**

- 内部 beta 阶段最该做的两件事：**狠下架**（砍掉调试用的可见性）和 **爬山**（攻下那些用户"看不到但感受得到"的后端难题）。
- "让它真正能工作"往往不是功能问题，而是**五个关键后端问题的登山问题**。
- 一个反直觉判断：**多数用户不想要"看得见的内部机制"**。他们想要的是一种"你放心交给它、它按时给你结果"的同事感。

---

## 五、爬山：当 agent 点不准 Salesforce 按钮时 `[访谈段落 17-18]`

**核心观点**
"让它能工作"的背后，是一条条具体的、可感知的技术解锁——特别是"电脑操作（computer use）"能力的提升，而销售团队成了最具代表性的验收官。

**深度阐述**

Lenny 请 Roman 举一个具体的"需要技术突破"的爬山例子。Roman 讲了一个极具画面感的故事。

公司里对 bot 最"上瘾"（botpilled）的群体之一，出人意料地是**销售/ go-to-market 团队**。原因很有启发性：销售每天用的工具里，**很多都缺乏良好支持的 MCP 或 API**。这恰恰是 bot 带来的"前后对比"如此强烈的原因——**这些活儿过去根本无法可靠地交给其他 AI 工具**，流程总会在某一步卡住。

但现在不同了：销售团队感觉自己**像是招进来了一个助理、给 TA 配了台笔记本电脑，TA 就能直接上岗**。

Roman 描述这一类问题的规模：大约有**10 到 20 个**具体场景，因为各种原因——比如鼠标精度不够，点不到 Salesforce 面板上那个精确的位置——导致任务卡死。团队会把这些"具体案例"带回负责基础设施的核心团队，说明"**agent 看不到浏览器里这个东西、看不到屏幕上这些像素，所以这个任务不可能完成**"。

**原话引用**："And that was just a lot more tangible than seeing a number on a dashboard slowly creep up. It was kind of like new chunks of work getting unlocked... you would ship an improvement that was kind of behind the scenes infrastructury and then the next day you would just get this outpour of love and appreciation from the sales team that now this workflow that was failing the last seven days finally works." `[访谈段落 18]`
（这比看着仪表盘上的数字慢慢爬升要具体得多。这更像是新的工作块被解锁了……你上线一个后台基础设施的改进，第二天就会收到销售团队铺天盖地的爱和感激——那个连续七天失败的工作流终于能跑了。）

这段描述生动展现了"爬山"的节奏：**找到下一个待解锁的任务 → 解决它 → 立刻感受到反馈 → 再找下一个。**

**延伸思考**

这是一个关于"**如何把基础设施工作变得可感**"的绝佳案例。后台工作最容易被团队忽视，因为它不直接影响用户体验、难以衡量。Roman 团队的做法是**把抽象的"性能提升"翻译成具体的"某个销售同事上班时不再卡壳"**——这让工程成果有了情绪、有了对象、有了速度感。对任何做 platform/infra 的团队，这都是一个可迁移的方法：**不要只看仪表盘，去看谁的工作流程被解锁了。**

---

## 六、两个决定成败的早期决策：云电脑 + 每个 Bot 一台电脑 `[访谈段落 19-22]`

**核心观点**
面对"很多人说用 Cursor/Codex 也能做同样的事"的质疑，Roman 指出 Grok Bot 的成功源自两个"当时不显而易见"的早期决策：**一切上云**，以及**每个 bot 拥有自己的电脑**。

**深度阐述**

访谈进入最核心的部分。Lenny 抛出了最尖锐的质疑：

**原话引用**："Wait, can't you just do all this with Codex and Cowork? And you can technically... everything as far as I know you can do with Grok Bot you can do with the other foundational models, the coding assistants." `[访谈段落 19]`
（等一下，这些用 Codex 和 Cowork 不也能做吗？据我所知，你在 Grok Bot 里能做的事，用其他基础模型、编码助手也能做。）

Roman 的回应，正是本访谈的核心洞察。他说这归结为**两个早期的、当时完全不显而易见、但回看至关重要的决策**。

**决策一：一切都在云端（everything in the cloud）**

Roman 说：**你永远不该思考"本地还是云端"、这些工作流跑在哪里、我的电脑是不是得开着、我从手机启动的话是不是得拴在家里的电脑上。** 这些"jank"（别扭的摩擦）在当下无处不在，因为人们在概念上纠缠"运行环境到底在哪里"。

团队很早就决定：**这一切都该在云端**。而一旦它在云端，它就是一个**持久的同事，拥有自己的电脑，能自己干活，无论你从哪个入口跟它交互，状态都一样**。这解锁了大量惊人的机会——你可以给 bot 发短信、从手机上启动它；未来，你应该可以从任何地方"呼叫"你的 bot，而它应该能进行真正的工作。**它是它自己的实体，独立于你的设备而存在。**

Roman 强调，这是一个非常重要的决策，**而现有产品大多没有做出同样的选择**，因此用户每天都在承受由此带来的摩擦。

**决策二：每个 bot 拥有自己的电脑**

Roman 把这个逻辑又推进了一步：不只是"在云端跑一个 agent 循环、通过多种方式交互"——更重要的是，**这些 bot 应该有自己的电脑**。

理由有两层。第一层是前面讲过的：大量任务没有良好支持的 MCP 和 API——**而人类自己也不是通过 MCP 和 API 工作的**，我们用电脑、点像素、在输入框里打字，所以 bot 也需要这些基线能力。

第二层是 Roman 眼中一个"我们未来回看会觉得很奇怪"的时代观察：

**原话引用**："I think we're in a really weird moment right now that I think we're going to look back on and be like, I'm surprised that this is the way that a lot of people worked with AI where you're onboarding these super intelligent new colleagues, these AI bots and you're asking them to share the same computer that you have. It's crazy. Like, if you were onboarding someone to your team and you said, 'It's your first day. I'm going to onboard you. You don't have your own laptop. You're going to sit next to me, we're going to share this laptop forever and constantly trip over each other. You're going to have access to my credentials. I'm going to have access to your credentials.'" `[访谈段落 21]`
（我们现在正处于一个非常奇怪的时代——未来回看时会想"我很惊讶很多人竟是这样与 AI 协作的"：你在给这些超级智能的新同事、这些 AI bot 做入职，却要求它们和你共用同一台电脑。这简直疯了。想象一下，如果你给团队新人做入职时说"第一天，你没有自己的笔记本，你坐在我旁边，我们永远共用这台电脑，不断互相绊脚，你能访问我的凭证，我也能访问你的"。）

**个人感受**

这段比喻极具冲击力，也非常真实。它揭示了一个我们习以为常的荒谬之处：**我们对待 AI 的方式，比我们对待任何一个新员工都不如**。我们不会要求新同事共用一台电脑，但我们却让最强大的 AI 与我们共用计算环境、共享凭证、互相干扰。这种"用办公桌隐喻来思考技术架构"的思维方式，本身就是一种强大的产品洞察工具——它把一个看起来是技术决策的问题（本地 vs 云端、共享 vs 独立），还原成了一个关于"人与协作者关系"的问题。

---

## 七、为什么其他公司没这么做？因为"从零开始"的自由 `[访谈段落 22-23]`

**核心观点**
这两件事看起来简单，但现有公司之所以难做，是因为被现有范式与沉没成本锁死；"从零开始"最大的价值，就是不受这些约束。

**深度阐述**

Lenny 好奇地追问：**为什么其他公司没这么做？** 他的猜测是——他们都是在既有的编码助手平台上、沿用它既有的方法和思路去搭建。

Roman 大量认同。他指出，**关键在于"从零开始"以及它所带来的自由**。他们自己就切身感受过这一点：Grok Bot 里的很多原语（primitives），他们过去在别的地方尝试过或搭建过——比如云基础设施，是给编码 agent 搭的；比如"给 agent 命名、把它当作离散实体来对话"，这也是他们已经见过的模式——开发者也正在把**具名的 agent 引入 Slack**。

但关键在于：**与其把这些概念"改造（retrofit）"进某个新结构或现有结构里**——Roman 认为这会是许多公司的"强默认选择"——他们选择了从零开始，把这两件事真正做对：第一，面向**一般知识工作**这个新受众；第二，面向**当下这个时刻**——模型已经非常有能力，如果你给它们正确的工具和基础设施，它们就能做很多事。

Roman 非常谦逊地补充：这些想法**并不是我们天才的灵光一现**。这些原语（如云上 agent、具名 agent）早就被其他产品验证过产品市场契合（他提到"OpenClaw 那个世界"），他们只是从中汲取灵感，**把它产品化成一个更紧凑、设置更少、对更多人更易用的表面**。

他的结论是：**所有玩家大概都看到了同一个机会，都收到了市场的反馈，但如果被现有范式和大量沉没成本困住，就很难行动。** "从头做一个全新的东西是非常痛苦的"——而这恰恰是让产品能"真正 work、真正 clicked（被点亮）"的原因。

**精华收获**

- 两个关键成功要素被 Lenny 总结得很清楚：**云端的电脑 + 具名的、按任务/用例划分的 bot（而非一个对话线程或一次性任务）+ "just works"**。
- 从"agents"到"bots"的命名转变本身就是团队推动的——Lenny 开玩笑说："干得漂亮，你们把它推过临界点了。好吧，现在我们都叫 bots 了。"
- **沉没成本是产品创新的头号敌人**。当你已经在一个范式里投入巨大时，任何与之冲突的新洞察都会让你痛苦到难以行动。

---

## 八、OpenClaw 的启示，与 Grok Bot 的超越 `[访谈段落 24-25]`

**核心观点**
OpenClaw 校准了两个关键问题——"给 AI 更大工具集能走多远"和"把 AI 当作同事来看待"，但它有一个致命缺陷：无法规模化。Grok Bot 的贡献是把这套理念产品化到"百万用户 + 企业可用"的层级。

**深度阐述**

Lenny 提到一个令人震撼的里程碑：**Claire Vo**——OpenClaw 最大的拥护者之一，曾把它深度嵌入到自己的工作、生活甚至和孩子的互动中——**最近把所有的 OpenClaw 都关掉了，全部迁移到了 Grok Bot**。Lenny 说这"听起来好笑，但其实是意义重大的里程碑"。

Roman 随后系统性地总结了 OpenClaw 做对的两件大事：

**第一，Harness（驾驭方式）的问题。** 模型很聪明、还会更聪明，但**即便在当前能力水平下，只要你给 bot 访问你所使用的那些工作工具的权限，它就能在很多人以为"AI 很笨"或"AI 不像宣传的那么有用"的地方走得很远**。Roman 认为，很多"AI 不够好"的抱怨，本质上是**"被以错误的方式驾驭了（harnessed in the wrong way）"**。所以 OpenClaw 真正做的是**逼着很多人问出这个问题**：如果你给它访问**大得多的东西集合**、如果它有自己的电脑——**它到底能走多远？**

**第二，心智模型的转变。** OpenClaw 真正改变的，是把 AI **更多地看作同事、队友、人**，把它拟人化为一个有生命的助手——**它能访问你的生活，把你进一步延展**。

**而 Grok Bot 在这之上延伸了什么？** Roman 给出两点：

1. **必须极其易于设置。** 那种"你家里有个 VPN、再配台 Mac mini"的极客做法，显然**无法规模化到百万用户**，更重要的，**绝不是企业利用这项技术的方式**。所以团队从设计之初就把这一点放在心上。
2. **磨平粗糙边缘，打造愉悦的产品体验，移除抽象概念。** Roman 特别提到像 **"skills"** 这样的东西——**AI 高级用户对这些东西非常熟悉，但 Grok Bot 用户根本不该需要知道 skill 是什么**。他们**永远不该输入 slash 命令**。这些应该作为有用的原语在后台被创建、供 bot 使用，但**用户不该被迫永远站在 AI 的最前沿**。

**延伸思考**

这是一段关于"**如何把极客工具民主化**"的教科书式论述。OpenClaw 证明了一个重要命题（给 AI 更大工具集、把它当同事看待），但它的**成功上限被"用户必须懂点技术"这一约束锁死**。Grok Bot 的贡献是**保留了洞见的本质，却剥离了实现的门槛**——这正是历史上所有"从小众到大众"的技术转型的共同特征：图形界面之于命令行，iPhone 之于 PDA。判断一个 AI 产品能否走向主流，关键问题不是"它能力多强"，而是"**它需要用户懂多少东西**"。

---

## 九、终极愿景：一支真正的 AI 同事团队 `[访谈段落 26-27]`

**核心观点**
Grok Bot 的终极愿景极其简单——每个人都该有一支 AI bot 团队，帮你工作、也帮你生活，而且**感觉上真的像一支团队**。

**深度阐述**

Lenny 直接问：**Grok Bot 的愿景是什么？理想的柏拉图版本是什么样子？**

Roman 的回答回到那句贯穿整个访谈的核心：

**原话引用**："The ultimate vision of Grok Bot is incredibly simple, which is you should have a team of AI bots that help you with your job and help you with your life. And it should really feel like a team. It should really feel like teammates that are autonomous, are helping you. You can steer them in various ways. You don't have to micromanage them. They have access to the tools necessary to do great ambitious work." `[访谈段落 26]`
（Grok Bot 的终极愿景极其简单：你应该拥有一支 AI bot 团队，帮你工作、也帮你生活。而且它应该真的感觉像一支团队、像队友——它们自主工作、帮助你；你可以用各种方式引导它们；你不需要微观管理它们；它们能接触到完成宏大野心工作所必需的工具。）

产品上的"北极星"是：**随着我们越来越接近这个'队友未来'，如何让每一个产品决策都从"我们在打造有用的 AI 队友"而非"我们在做一个 SaaS 产品"的角度出发？**

Roman 讲了一个他们内部常用的判断方法——**"colleague pill"（同事化）**：当团队就某个产品决策争论不休，两边都有道理、在"产品逻辑"里看不出明确答案时，就**跳出来，脱离"科技公司气味"，然后问：一个人类会怎么做？在这个具体情境里，你会希望你的队友怎样做？**

Roman 说，答案往往**非常清晰、而且几乎一致**——大家对一个"你更愿意与之共事的人类队友"应该怎样做，其实分歧很小。一旦答案浮现，**那就去把它做出来**。哪怕有些产品含义、模型含义需要很多事都对，才能兑现这个体验。

**原话引用**："But in some ways it's not rocket science. Doesn't require you being a genius. You just need to ask the question of what would you want from a human teammate and can we push AI to behave in a similar way." `[访谈段落 27]`
（但从某种角度说，这并不需要火箭科学。不需要你是天才。你只需要问："你会希望一个人类队友怎么做？我们能推动 AI 表现出类似的行为吗？"）

他强调了一个具体例子：**语音体验**。在人类协作中，他经常和队友 Slack 来回、共享上下文；**很多时候最简单的是打一个五分钟的 huddle（即时语音）——按一下、说说、共享屏幕、看对方分享的东西、跳出来、继续异步**。这在人类协作中是如此核心，而**目前没有任何 AI 产品真正做对了这件事**。所以他们想造出这样的东西。

**个人感受**

"colleague pill"和"你会希望一个人类队友怎么做？"这个方法论，是整期访谈中最朴素、也最深刻的洞察。它绕开了所有复杂的 AI 产品哲学争论，直接把问题**还原成人与人之间业已存在的关系模型**。它之所以有效，是因为人类对"好的协作关系"有着几十年、甚至几千年的直觉积累——**你不需要重新发明协作的伦理，你只需要把它应用到 AI 上**。

---

## 十、"同事化"的四个延伸：电脑、命名、语音、工作与生活 `[访谈段落 28-31]`

**核心观点**
从"同事隐喻"出发，团队做出了一系列反直觉决策：工作和个人的 AI 最终可能是一套系统，且"工具的人机界面"将从"旋钮座舱"演变为"意图 + 引导"。

**深度阐述**

Lenny 点出，"colleague pill"这个术语**贯穿了整场对话**——从"每个人该有自己的电脑"到"给 bot 命名"，都是它在起作用。他随后提出了一个更大的问题：**工作与个人的 AI，会分开还是合一？**

Roman 借这个问题的回答，进一步展开了一个重要的观点转变——**"未来时代的 power tool 会是什么样子"**。

他认为，过去一二十年糟糕的 B2B 软件给人们留下了"负担（baggage）"，导致人们看到一些**形式简单**的产品（他举了 ChatGPT，认为 Grok Bot 也有许多类似特征），就**误以为它不是工作产品、不是 power tool**。

而"power tool"这个词，在上一代人的脑海里，往往意味着**像 Photoshop 那样——有无数精确调节的旋钮**，使用者是**坐在驾驶舱里的终极飞行者，清楚每一个旋钮的作用**。

但 Roman 认为，**未来的 power tool 会完全不同**：

**原话引用**："where it is mostly just intent being expressed and good steering on the part of the human and these AI tools abstract away all of the knobs... it really is just working with a teammate and so the interface for that is quite conversational." `[访谈段落 29]`
（未来的工具主要是表达意图，配合人类良好的引导，而这些 AI 工具把所有旋钮都抽象掉了……它其实就是与一位队友共事，所以它的界面非常对话式。）

他进一步描述：当他走过同事的工位、瞥见 Grok Bot 打开着，一瞬间会以为"哦，他在用聊天 app 吗？"——但其实是那个人在用**最主要的工作工具**做大部分工作。

**关于工作与个人是否分开**，Roman 的判断是：

- **很多人会想要分开**——他们想在个人生活和工作之间划清界限，这是好事、很重要，从企业角度也有大量常识性理由；
- **但团队想要构建的方向是**：Grok Bot 应该成为你**工作中大部分日常事务**的委派对象（让你专注更高杠杆的事），**同样**也应该成为你**个人生活中低杠杆事务**的委派方式；
- **而这两个问题，本质上不是两套不同的难题**——从产品形态和解决方式上看，它们几乎是同一个东西；
- 因此**他的直觉是：一个产品将成为这两者最好的形态**，而这正是他们想做的。

Lenny 立刻抓住机会调侃："**Bam，这可是个巨大的 TAM（总可寻址市场）。**" 他接着提出了一个关键的隐忧：**如何避免跨界污染**——个人内容不会悄悄渗入工作，或工作内容不会外泄到个人。Roman 承认这就是方向，问题在于如何做到并让用户**感到绝对安全**、有恰当的防护，**同时还要很好玩**。

**精华收获**

- **"power tool"的定义正在被改写**：从"复杂的旋钮座舱"，变成"意图表达 + 好的引导 + 抽象掉的旋钮"。Grok Bot 想要的界面是对话式的。
- **工作与个人的 AI 可能是同一套系统**——因为两者的产品形态与解决方式高度同构。
- 但这也意味着**隐私边界**成为产品胜负的关键：如何让两套语境安全隔离、又让用户信任。

---

## 十一、抽象掉"电脑"：从 VM 到"隐形的基础设施" `[访谈段落 32-34]`

**核心观点**
关于技术架构，Roman 用"同事隐喻"再次给出了最简洁的答案：在成熟状态下，用户**不该点击进入远程虚拟机、不该接管控制**；电脑概念最终会像"队友的笔记本"一样被完全抽象掉。

**深度阐述**

Lenny 抛出一连串技术问题：账号提供的"电脑"到底是什么？是云端跑的 VM？每台机器多次登录？还是**每个 bot 一个独立的 VM 实例**？他让 Roman 尽可能透露一些。

Roman 没有给技术细节，而是**用同事隐喻做了漂亮的回答**：

**原话引用**："If we were on a team together, you and me, I think the number of times that you would have to manually take over my computer and start clicking on things... hopefully is pretty close to zero... And so similarly, I think right now we're in a place where computer use is good. It's getting much better. And in very short order, I think the computer concept will be completely abstracted away from the user." `[访谈段落 32]`
（如果我们是一支团队，你和我，你不得不手动接管我的电脑、开始点点点的次数，希望接近零……同样地，我认为现在 computer use 已经不错了，还会变得更好。很快，电脑这个概念就会从用户那里被完全抽象掉。你应该永远不需要点击进入一个远程虚拟机，永远不需要接管控制。）

他给出的"正确理解方式"是：**Grok Bot 是一支 bot 团队、一群替你工作的 agent**。它们接触到的是：

- **一组很长的记忆**：你与它们过去的全部交互历史——Roman 借此批评了"为每个独立工作单元开一个新对话"的范式（"我自己就经常在对话之间复制粘贴"）；他认为更好的方式是像团队一样，按**不同泳道/角色**组织工作，让 agent 从你身上学习、随时间变得更聪明。**这是长寿命的 agent，不是一次性的单次会话**；
- **所有人类同事该拥有的工具**：API、MCP，以及**一台能像你一样自由操作的自己的电脑**。

Roman 提了一个让他印象深刻的例子——**Lenny 去的那个线下聚会**上，一位市场团队的同事 **Shub** 演示了一个让全场炸裂的东西：因为每个 agent 里都有一台电脑，你可以**在 Grok Bot 内部运行 Grok Bot 本身**。Shub 用它来做测试、观察回归。Lenny 立刻接话："我自己也这么干。这其实非常有用——下载 Grok Bot 到你的某个 bot 里，我的那个叫'QA 测试员 bot'。"

Roman 详述了这个用法：**任何时候有 bug 报告、或者要测试新版桌面端 app，他就可以说"这里有 10 个流程，每次发布都要验证它们有没有变好，你去测试，写到这个 Notion 文档里，里面列有过去所有 client 版本的测试记录，然后做对比。"**

**原话引用**："Once you start breaking out of 'this is AI chat with a set of connections'—which is I think where most people are conceptually now—instead to 'this is a colleague with a computer and anything I would ask a colleague to do on a computer I can ask Grok Bot to do.' It just raises the ceiling of what you would think to give to AI." `[访谈段落 34]`
（一旦你跳出"这是一个带一组连接的 AI 聊天"——我认为这是大多数人在概念上所处的位置——转而认为"这是一个有电脑的同事，我在电脑上会让同事做的任何事，我都能让 Grok Bot 去做"，**这会抬升你愿意交给 AI 的东西的天花板**。）

**延伸思考**

"Grok Bot 运行 Grok Bot"的递归范例，是"**给 AI 一台完整的电脑**"这一决策的最美副产品。当一个 agent 能像人类一样操作电脑时，它就能操作**任何软件**——包括你自己公司的软件。这意味着产品的**能力上限不再由 API 生态决定，而是由"能不能用电脑"决定**。这是一个巨大的杠杆：传统的 agent 能力被"有人为你写了 API 吗"限制，而拥有电脑的 agent 则**不受此限**。

---

## 十二、"信息饕餮"：把认知负载交给 Bot `[访谈段落 35-36]`

**核心观点**
一个简单却极富深度的使用模式，是把 Grok Bot 变成你个人的"always-on chief of staff"——吸收海量信息、过滤噪音、只把重要的东西带给你，甚至能"page（呼叫）"你。

**深度阐述**

Lenny 请 Roman 分享其他"拓展心智"的用法。Roman 分享了他最沉迷的一个方向：**把 Grok Bot 当作一个 infovore（信息饕餮）**。

核心价值是：**吸收海量信息，把它们从你的认知负载中移除，给你平静，然后只把重要的东西带给你。**

**V1 实现（很多人已经在用）**：Grok Bot 坐在 Slack 和 email 之上，你告诉它你的角色、你关心什么，告诉它"在这些情况下通知我，在那些情况下不要直接 ping 我、但放进我每天读的 daily roundup 里"。

**Roman 说自己现在大概处在 V3 或 V4**：

- 他把 bot 连接到**X 上所有关于 Grok Bot 的提及**；
- 它**与内部上下文交互**；
- 它**与 QA 测试员 bot 交互**——看它能否复现收到的任何 bug 或反馈；
- 他还连接了自己的消息服务，**快速响应反馈、主动联系他人**。

他设想：这里有一个**always-on（永远在线）的 chief of staff 实体**，它能**保护你对真正重要事情的专注，同时永远在"巡视"是否有什么该引起你注意**。

Roman 还提到一个"好笑"的现象：有些人**真的给了他们的 Grok Bot "呼叫（page）自己"的能力**——如果发生超级紧急的事，哪怕他们在喝咖啡，也会被 Grok Bot 呼叫。当然，这**只有在你信任 Grok Bot 不会误报时才敢用**。目前，这些人反馈"非常有用、非常成功"。

**原话引用**："I think we're going to see more of that type of stuff where the agent or the bot should actually be more proactive to you than you reaching out to it. And I think that will be the next shift in AI." `[访谈段落 36]`
（我认为我们会看到更多这类东西——agent 或 bot 应该比你主动找它，更主动地来找你。我认为那将是 AI 的下一次转变。）

**个人感受**

"**下一波 AI 的转变是 bot 主动找你，而不是你主动找它**"——这是一个极具前瞻性的判断。它重新定义了人与 AI 的权力关系：从"工具等着你使用"，变成"同事主动帮你盯着"。这也解释了一个深层心理：真正让人放心的不是"我随时能问它"，而是"**它会在需要时提醒我**"。这种"主动式 AI"是同事隐喻的自然延伸，也把"信任"推到了前所未有的高度——因为一个会主动打扰你的 AI，只有在**几乎从不误报**时才是可贵的。

---

## 十三、招聘场景：让 AI 做"超人级"的工作 `[访谈段落 37-39]`

**核心观点**
招聘团队是 Grok Bot 最出人意料的重度用户之一，他们用它做"always-on sourcing"——这揭示了 AI 的真正价值不在于"帮你筛简历"，而在于做**人类根本做不到的超人级任务**。

**深度阐述**

Lenny 提到他节目里采访过的 SpaceX AI 招聘负责人 **Adam Ward**，听说他的团队是 Grok Bot 的顶级用户之一。

Roman 确认：招聘团队给了大量反馈，尤其是早期**一有 bug 就会 ping 他们**。

最有趣的用例是**sourcing（人才寻访）工具**。他引用了 Adam 在 Lenny 节目里谈过的 SpaceX AI 招聘哲学：

**原话引用**："Being on the market is not a precondition for us trying to hire you... the best way to hire is really just look at the biggest problems at the company that needs someone to own it or take it to the next level. Find out of the total universe of people in the world who would be best and then ruthlessly go after them and try to convince them to join." `[访谈段落 38]`
（"正在找工作"不是我们尝试招募你的前提条件……最好的招聘方式，其实是先看公司里那些最需要有人去拥有、或推到下一层级的大问题，然后从全世界所有人里找出最适合的人，无情地去追他们，说服他们加入。）

在这个哲学下，**最该自动化的招聘流程，不是"帮我读一堆简历、帮我排序"**——最有用的是：**"这是整个潜在人才的宇宙，帮我把它和这个非常具体的业务问题 / 岗位匹配起来，并帮我联系他们、约咖啡、全力以赴。"**

Roman 举了一个具体的、令人惊叹的用法：

**原话引用**："Who are the co-authors of this paper and the PDF doesn't exist on Google Scholar. It just exists on this conference website. I want you every morning to go to the conference website, download the PDFs, if there are any new ones. You should find every new name that we've not yet tracked. You should add that name to a spreadsheet. You should do research. You should look at everybody at SpaceX, see if there's anyone directly connected. If so, you should send them a Slack message asking for an introduction." `[访谈段落 39]`
（"这篇论文的合著者是谁？这个 PDF 在 Google Scholar 上都搜不到，只存在于某个会议网站上。我希望你每天早上都去那个会议网站下载 PDF——如果有新的。找到我们还没有追踪的每一个新名字，加到表格里，做研究，查一下 SpaceX 里所有人看有没有直接认识的人，如果有，就给他发 Slack 消息请求引荐。"）

**原话引用**："It's those types of always-on sourcing use cases that I think in the past were incredibly manual and now it's the type of thing AI is superhuman at. And our team can focus on closing great candidates and getting conversations with great candidates, not pulling these huge lists." `[访谈段落 39]`
（就是这种"always-on sourcing"用例——过去这些极其手工活，现在却是 AI 真正"超人"的地方。我们的团队可以专注于拿下优秀候选人、与他们对话，而不是去拉这些巨大的名单。）

Lenny 忍不住感慨："**有人现在肯定在说——我要把这段对话转录下来，扔进一个 bot，造出他们自己版本的这套东西。**" 他又补了一句："你们其实可以卖这套 bot 的模板卖到十亿美元。如果能把 Adam 团队找人策略变成一个 bot——天啊，这是**民主化招聘**。"

**延伸思考**

这个案例的价值在于它精准校准了"**AI 到底能把什么做到超人水平**"。不是"帮你读简历"（人类也能读），而是**"每天早上巡视整个会议网站，下载新 PDF、抽取新名字、交叉比对内部人脉、自动发消息"**——这类任务的特征是：**跨多个数据源、持续、细碎、重复**。人类做这些会崩溃，AI 做这些毫无负担。**AI 的杀手级用例，往往不是"做得比人好"，而是"做得比人不知疲倦、比人不知疲倦地细心"。**

---

## 十四、上市策略：从"夜周末"到"企业变革" `[访谈段落 40-43]`

**核心观点**
团队的打法是给尽可能多的人免费账号、聚焦用例，同时把长期赌注押在"企业"上——因为"一个人人都在用 AI 做个人的事"的时刻，会像编码时代一样，倒逼企业接受它。

**深度阐述**

Lenny 称赞团队在**上市策略**上的清晰度，并点出两个观察：一是**大量免费账号**、二是**对用例的极度专注**——因为在如此新颖的产品面前，用户打开它时会问"我拿这个干嘛？"，而这些"人们都拿它做什么"的示例正是在解决这个问题。他还表扬团队"懂分发的威力"。他直接请 Roman（前 Cursor 的 GTM 负责人）谈上市打法。

Roman 给出的框架来自**编码领域的经验**，他认为这与知识工作会相似：

**第一步，早期采用者阶段。** 有一群早期采用者，会把编码工具推到极限，主要用在**个人项目上、晚上和周末**。设想 2023 年那会儿：白天上班用基础 IDE（前 AI 时代），晚上回家做业余项目，用 Cursor 或最新最强的 AI 编码工具——**这给了他们极致的加速，让他们体验到未来**。

**第二步，倒逼企业阶段。** 然后他们回到工作中，开始**要求**：**"我没法想象用别的方式工作了，我现在感觉像在糖浆里走路，这必须改变。"**

Roman 认为知识工作会走出类似的曲线——**人们有时会先以个人身份体验到那个"aha 时刻"**。在 X 上你就能看到大量这样的例子：Grok Bot 控制家里的机器人电脑、控制扫地机器人、帮你在 Tesla 充电桩谈判上省钱……各种有趣的用例。

**原话引用**："I think the next step is going to be this is not a consumer product. We think this is going to transform businesses. We think this is going to transform teams and it will be bots coming into teams and contributing really economically valuable work especially as they get much smarter." `[访谈段落 42]`
（我认为下一步会是——这不是一个消费级产品。我们认为它将变革企业、变革团队，会有 bot 进入团队、贡献真正具有经济价值的工作，尤其在它们变得更聪明之后。）

因此在 GTM 上，团队**正大力押注企业市场**，并思考一系列新问题：不只"单人使用一个 bot"，而是**"一个 bot 如何在更大的团队里工作"、"bot 如何在复杂的、有大量上下文和历史的企业系统里工作"、"在更大的组织里，记忆应该是什么样子"**。Roman 承认这里有很多未解问题，但他相信 **Grok Bot 是把 agent 带到"编码之外的整个公司"的正确原语**。

**精华收获**

- **进入市场的最优路径可能是"绕道个人生活"**：让员工先在个人场景里体验到"未来"，再回头倒逼企业采购。
- 对知识工作产品而言，**"消费级易用性"和"企业级复杂度"是同一枚硬币的两面**——易用性是把人拉进来的钩子，企业能力是长期价值的落点。

---

## 十五、品牌架构：SpaceX AI 的三大支柱 `[访谈段落 44-45]`

**核心观点**
SpaceX AI 目前有三大支柱：编码产品（Cursor + Grok Build）、通用知识工作（Grok Bot）、通用模型研发。区别在于"目标是实用的有用 AI，而非追求模糊的超级智能理想"。

**深度阐述**

Lenny 请 Roman 梳理品牌关系——Grok Bot、Cursor、SpaceX AI 的收购与整合。Roman 描述了三个"大支柱"：

**第一支柱：编码产品。** 现在是 **Cursor 和 Grok Build**。团队坚信**为开发者、为组织里工程部分保留一个专业工作表面至关重要**。虽然人们目前有时会用 Grok Bot 启动云 agent、合并 PR、做 QA 等编码相邻任务，但 **"当你发布生产软件时，你必然需要一个每一个像素都为这个终端用户优化的产品"**。所以会在这里做重大投入。

**第二支柱：通用知识工作。** Grok Bot 是朝这个方向的令人兴奋的一步。还有很多工作要做——让它更有用、扩展到新界面、**让它真正感觉像你能委派工作的 AI 队友，尤其是在公司和业务内部**。

**第三支柱：通用模型研发。** "**我们想训练世界上最聪明的、真正有能力的模型。**"

他点出了 SpaceX AI 与其他 AI 实验室的一个区别：

**原话引用**："I think our goal is less to build chase super intelligence or some kind of vague aspirational ideal. And the goal is actually very practical which is to build useful AI... the group of people contributing to these models are engineers and people who kind of came into the model training effort from like a very applied mindset and I think that's what gets this company going." `[访谈段落 45]`
（我认为我们的目标不太是去追逐超级智能或某种模糊的、理想化的目标。目标其实非常务实——打造**有用的 AI**……为这些模型做贡献的人，是工程师、以及从非常应用型心态进入模型训练的人，我认为这正是驱动这家公司的东西，也是与其他一些竞争者略有不同的方向。）

**延伸思考**

"**目标是实用的有用 AI，而不是模糊的超级智能理想**"——这是一个罕见的、在 AGI 竞赛白热化时期仍然坚持端正姿态的表述。在基础设施（模型训练）与应用（产品）分层的公司结构里，Roman 明确指出了"应用心态"能带来什么优势：**当训练者本身就是应用者时，他们训练模型时脑海里想的会是"这个东西在真实工作流里该怎么用"**，而不是"它在 benchmark 上该有多强"。

---

## 十六、那条推文：100% 与 90% 是天壤之别 `[访谈段落 46-47]`

**核心观点**
Roman 置顶的那条推文——"一个能完成 100% 工作的 AI，感觉上与只能完成 90% 的 AI 有本质区别"——道出了他为何对 Grok Bot 如此兴奋：这是他第一次真正能把非编码任务**彻底委派出去**。

**深度阐述**

Lenny 提到 Roman 置顶（或近期）的那条推文，并发自内心地说："**我大幅更新了我对 AI 能力的认知。**"

**原话引用（Roman 的推文）**："An AI that does 100% of the job feels categorically different from one that gets you 90% there. I've significantly updated what I think AI is capable of." `[访谈段落 46]`

Roman 解释这条推文背后的感受：

**原话引用**："What made me so excited to work on Grok Bot is it was the first time for non-coding tasks that I felt like I could truly delegate work to AI and not have to think about it and I would come back and it's done." `[访谈段落 46]`
（真正让我对做 Grok Bot 如此兴奋的是——这是我第一次在**非编码任务**上感觉到，我可以**真正把工作委派给 AI，不必再想它，回来后它已经做完了**。）

他特别指出：**工程师们已经感受到这种感觉有一段时间了**——大约一年到一年半，开发者的工作已经**完全变了样，与两年前完全不可识别的**。但他认为，**大多数人现在对 AI 的体验**与此非常不同：仍然像两年前——为每个任务新开一个对话线程、输入文字、回车、看着它一步步跑、得到一个不太对的结果、继续和它纠缠。

**Grok Bot 短路了这个过程**。

**原话引用（"不看人传球"的比喻）**："When you have a teammate that you only 90% trust... you're like, I know I'm going to have to be thinking about this while you're doing it and I know it probably is not going to be quite there and I'm going to have intervene and kind of steer it slightly. That's not 90% task completion. You're still doing the thing and it feels that way and it's weighing on you in the same way. Versus like truly throwing a no-look pass to a colleague and being like 'you got this. Here's the context. Go off and run. I'm excited to see what you do.' Like that's a different category." `[访谈段落 46]`
（当你有一个只信任 90% 的队友……你心里想的是"我知道我在你做这件事的时候还得惦记着它，我知道它可能不会完全到位，我不得不介入、稍微引导它"。**这不是 90% 的任务完成度。你实际上还在做这件事，感觉一样，压力一样。** 与之相对，真正的"不看人传球"——你传给一个同事，想着"你搞得定。这是背景。去跑吧，我很期待看你做出什么"——**那是完全不同的一类体验。**）

**个人感受**

这段"90% 与 100%"的辨析，是整场访谈最深刻的一段。它其实在说：**信任不是连续的，而是断崖式的。** 一个你 90% 信任的同事，和 100% 信任的同事，给你的心理负担差异不是 10%，而是天壤之别。因为 90% 意味着**你依然被"牵挂"绑定**——你的大脑并没有真正解放，只是从一个直接的执行者变成了一个"监工"。而 Grok Bot 提供的，是那种**"不看人传球"式的解放感**——你可以把任务彻底扔出去、回来时它已经完成。这解释了为什么用户对它的情感如此炽热：**被真正减负的人，会产生极强的忠诚。**

---

## 十七、速度的秘密：初创冲动 + "去做那件事" `[访谈段落 48-53]`

**核心观点**
团队保持高速的秘密，是刻意维持"初创公司的冲刺能量"——一种定义不是靠人数或融资轮次，而是靠"你能在短时间内朝某个方向做出极端影响"的状态；它由两条价值观支撑：**"删除产品"和"去做那件事"**。

**深度阐述**

Lenny 罕见地坦承自己"被震撼到了"：他被拉进一个 Slack 群反馈产品，然后看到——"好的，明天我们给你一些免费码让你发出去"、"我们明天做这个"、"我们要上线一个带模板的 marketplace，两天后上线"。他惊呼："**我没时间反应。你们怎么在这么多事同时进行、还在持续高质量、还让人感觉方向明确地朝某个愿景前进？**"

Roman 首先回答：**保持'初创感觉'**，他称之为他最满意的一点。

**原话引用**："One thing I've been really happy has never changed is that startup feeling inside of the company... when I joined Cursor originally we were about 15 people. We scaled to over a thousand. And then now we're a part of SpaceX AI, which is kind of an even bigger organization." `[访谈段落 49]`
（一件让我非常高兴、从未改变的事，是公司内部那种初创公司的感觉……我最初加入 Cursor 时我们大约 15 人，后来扩张到一千多人，现在我们是 SpaceX AI 的一部分，那是一个更大的组织。）

他描绘了这个环境：**周围是一群极其有才华的人，每个人以 100 英里每小时的速度前进，你深深信任每个人都会完成自己的那一环，有一个清晰的愿景让所有人都为之兴奋、都知道要去执行。**

Roman 承认了残酷的现实：**随着公司成长、招来在大公司经历过超速增长的人，事情会慢下来，你会一直对自己说"我们还是初创公司，我们动作还是很快"，但其实并没有。大家都知道没有。说起来容易，做起来难。** 他坦言"祈祷这一点能继续为真"，因为这对成功至关重要。

他对"初创公司"下了一个极精彩的定义：

**原话引用**："I think if you define a startup by number of people or by like the funding round, none of those things really make any sense. The core thing that defines a startup is exactly what you're describing, which is this kind of scramble energy of things are kind of chaotic and kind of disorganized... it has these amazing properties of you can make extreme impact in a particular direction in a short amount of time. And you really do get out of a system what you put in." `[访谈段落 50]`
（如果你用人数或融资轮次来定义初创公司，这些都没有意义。定义初创公司的核心，正是你在描述的那种"冲刺能量"，事情有点混乱、有点失序……但它有这些惊人的特性：你能在短时间内朝特定方向做出极端的影响。而且**你真的能从一个系统里得到你投入的东西**。）

他还指出了这个环境的两面性：对很多人来说，**这种环境并不愉快**，但它有那些惊人的属性。因此作为文化、作为组织，他们**刻意地把这种属性保留下来**——而一些竞争对手和其他 AI 实验室已经变得很大，"你能感觉到"。

---

## 十八、Cursor 的护城河：每半年彻底重塑自己一次 `[访谈段落 54-57]`

**核心观点**
在"最卷的市场、站在最卷的平台上"活下来并大获成功的核心，是文化驱动的不自满——**AI 的能力在飞速变化，产品必须随之变化；如果一个公司不能每六个月彻底重塑自己，它就会输。**

**深度阐述**

Lenny 抛出了他"最期待问的问题"：从外部看，**Cursor 本不该成功**——它身处全球最卷的市场、面对史上增长最快的公司 OpenAI 和 Anthropic；它还建立在**这些平台之上**。然而它不但活了下来，还拿到了巨额退出、持续成功。**凭什么？**

他的答案是：**快速调整以适应市场现实**——从 autocomplete 到对话式 agent，到云端，再到 Grok Bot。**同时为那些别处也能做的东西打造最好的体验**——Grok Bot 就是最好的例子。

Roman 认同，并说这是一个"模糊的答案"——**很多东西都源于文化和人**。

**原话引用**："We have never been complacent. We've never felt like we've won and it's always been about the next thing... our goal is to translate those capabilities into amazing products for customers. But those products are going to change and they need to meet the moment as the capabilities get stronger. And what met the moment two years ago is completely different than what's meeting the moment today. And if we as a company can't completely reinvent ourselves every six months, which recently it's felt even shorter than that... we're going to lose." `[访谈段落 55]`
（我们从不自满。我们从没觉得自己赢了，永远想的是下一步……我们的目标是把这些能力转化为给客户的出色产品。但产品会变，它们需要随着能力增强去迎合那个时刻。两年前迎合时刻的东西，和今天迎合时刻的东西完全不同。如果一个公司不能**每六个月彻底重塑自己**——最近感觉甚至更短——我们就会输。）

**原话引用**："I think it's that spirit of always pushing to be on the frontier, never thinking it's over or that we've won or that we've gotten it right. And just constantly updating our beliefs that has gotten us to where we are now." `[访谈段落 55]`
（正是这种永远推动自己站在前沿、永不认为"结束了、我们赢了、我们做对了"，而是持续更新信念的精神，把我们带到了今天。）

Roman 补充了一个关键的历史观察：**AI 编码一直竞争激烈**，Cursor 刚出现时，对手是微软等一二十家公司。**而显著的是，这些对手中没有一个是今天 AI 编码前沿的公司**——很大程度上**不是因为决策失误或资源不足，而是因为文化上无法快速行动、无法在形势变化时随机应变**。

**精华收获**

文化价值落到具体表达上，Roman 给出了两条他反复回到的：

**第一，"删除产品（deleting the product）"**——回看 Cursor 的每个历史版本、Grok Bot 的每个历史版本，你都会看到：**消失的东西比新增的东西多**。那些因模型还不够聪明、而不得不存在的人工脚手架（scaffolding）、产品悬垂（product overhang），会随时间被移走。团队必须**能舒服地做那些可能惹恼一小撮用户或内部一小群人的困难决策，去换取更大的目标——让产品简单、强大、适应未来方向**。

**第二，"去做那件事（do the thing）"**——Roman 经常重复的一句。**这不是一个"请求许可"的文化**：如果你看到某件你认为需要发生的事，**你就去把它修好，并把需要的资源拉进来让它发生**。这让很多人在这里获得了成功，也是他们与 SpaceX AI 共享的东西。Lenny 补了一句："**agency（能动性）**，你可能也听说过。"

**延伸思考**

"**每六个月彻底重塑一次自己**"和"**删除产品**"，本质上说的是同一件事：**在一个能力飞速变化的市场里，公司唯一的竞争优势不是它当前的资产，而是它的"可变形能力"**。任何今天让你成功的功能，明天都可能成为过时的脚手架。那些曾经最成功的公司之所以失败，往往不是做错了什么，而是**无法删除那些让它们最初成功的东西**。

---

## 十九、关于护城河：它可能是"被发现的"，而非"被规划的" `[访谈段落 58-59]`

**核心观点**
Roman 不建议创始人从"战略图"倒推护城河；Cursor 的成功来自"把三个月后可能实现的事，努力拉进今天"的反复练习——**护城河是发现出来的，不是预先规划的。**

**深度阐述**

Lenny 抛出"护城河（moats）"这个大问题。他指出，Cursor 常被当作一个"技术上似乎没有护城河、却持续获胜"的案例。人们讨论的两大护城河是：(1) **数据反馈循环**——用户自动补全，模型从中学习；(2) **最好的体验 + 高日常活跃用户**——通过长期摸索什么有用、什么被人们需要。

Roman 承认现在"很多人都在谈护城河，创业公司在考虑 12、24 个月后是很有意义的"，但他给出了一个坦诚的回答：

**原话引用**："I will say that I think if Cursor and many other successful companies of this kind of vintage... if they had thought about moats slash kind of tried to work backwards from some strategy diagram or like you know a maybe more abstract notion of how a company should work, I don't think that would have created this outcome or this product. I think what really created the magic of Cursor uh was an obsession with building a useful thing today." `[访谈段落 58]`
（我想说的是，如果 Cursor 和许多同期成功的公司……如果它们当初去思考护城河、或者试图从一个战略图、或某种更抽象的公司应该如何运作的概念去倒推，我认为那不会创造出这个结果或这个产品。我认为真正创造 Cursor 魔力的，是**对"今天就构建一个有用的东西"的痴迷**。）

Roman 描述了一个持续的心智练习：**你能看到世界三个月后会走向哪里、六个月后会走向哪里——模型会变得更聪明，今天还不能解决的问题明天就能解决了。** 所以不断问："**我们如何把那东西'拉'到今天，哪怕需要在它上面叠加一些工程、或者需要以特定方式改变产品，让用户能与这个新能力交互？然后三个月后我们应该删掉那些代码——因为它会变得更好、更基础——所以我们应该去为'三个月后的那个东西'而构建。**" 就这样一遍又一遍地做。

**原话引用**："It was constantly just doing that over and over again that I think led to users really trusting us and placing their time inside of our product and trusting that we were kind of bringing things to this next frontier... And so I would really encourage many founders or people starting out today to be more grounded in that perspective of how can I make something that is not possible now possible." `[访谈段落 58-59]`
（正是不断这样做，让用户真正信任我们、把他们的时间放在我们的产品上、信任我们在把东西带向下一个前沿……所以我真心鼓励今天的许多创始人更脚踏实地地从这个角度出发：**我如何让一件现在不可能的事，变得可能。**）

Lenny 总结得非常漂亮：**"就是构建一些让人们痴迷的东西。别过度思考护城河那部分。如果你能持续这样做，你最终会找到护城河——在 Cursor 的案例里，它最终是好几样东西。"** Roman 补了一句：他最近在另一个播客上说过类似的话——**护城河是被"发现"的，而不是被提前"规划"的。**

---

## 二十、新用户建议与进阶玩法：别造糖衣，去委派真正的工作 `[访谈段落 60-63]`

**核心观点**
Roman 拒绝提供"hacky pro tip"，因为他认为这些东西"本不该存在"；他对新用户的建议是"给它上下文，然后问它能为你做什么"，对进阶用户的建议是"构建你 bot 之间的协作脚手架"。

**深度阐述**

Lenny 请 Roman 给新用户和进阶用户建议，Roman 首先声明了他的立场：

**原话引用**："I want to stay away from the you know super hacky pro tip stuff because I think our philosophy as a team and as a company is that those things really shouldn't exist. There shouldn't be all these crazy knobs. You should be able to delegate something to Grok Bot and they should do it." `[访谈段落 60]`
（我想避开那些超级 hacky 的 pro tip，因为我认为我们作为团队和公司的哲学是：这些东西本不该存在。不该有这些疯狂的旋钮。你应该能把某件事委派给 Grok Bot，它就该去做。）

**给新用户的建议**：

1. **给它成功所需的上下文。** 就像给团队新人做入职一样，让它访问你每天用的 Slack、email、公司记录。
2. **直接问 Grok Bot 它能为你做什么。** 让它基于你设置好的连接，走一遍。

Roman 分享了自己的 onboarding 体验（当时还没有任何 onboarding 界面），他给它的第一个任务是："**去翻我的 Slack、翻我的 email，建议 5 件你可以从我盘子里拿走的事，以及你需要什么才能做到。**" 它建议了 5 件，其中**2 件真正有用**——他立刻 spin off 了两个 bot 去解决那两件事。

**原话引用**："That was my big wow moment of feeling like no other AI tool in the past could have done those two things. It was not like draft an email. It was like do a chunk of work." `[访谈段落 61]`
（那是我最大的"wow 时刻"，感觉过去没有任何其他 AI 工具能做到那两件事。它不是"起草一封邮件"，而是**"完成一大块工作"**。）

**给进阶用户的建议**：Roman 说自己不断在发现"我的 bot 之间如何互相交互、协作"的新模式。他在**给自己创建一个"脚手架"，来安置 bot 产生的 artifacts**，让它能写到一个**对他而言非常易读**的地方。比如他有一些**每天都读的频繁 digest**，bot 把它推到一个数据库里，他就能轻松阅读。

**原话引用**："I would encourage power users to think about ways that Grok Bot can actually write to like a single store where you can organize a lot of its outputs much easier." `[访谈段落 62]`
（我会鼓励进阶用户思考：如何让 Grok Bot 真正写到一个**单一的存储库**里，让你能极容易地组织它的众多输出。）

Lenny 忍不住感叹："**妈呀，我们需要再做一期节目，深挖 Roman 的 Grok Bot 设置——虽然它可能包含太多隐私敏感信息，没法展示。但没关系。这是个了不起的技巧。**"

---

## 二十一、闪电问答：阅读、电影、AI 产品与人生准则 `[访谈段落 64-70]`

**核心观点**
Roman 的品味偏好：品钦之外他推荐冯内古特的《猫的摇篮》和 Pressfield 的《艺术之战》；每年重看《卡萨布兰卡》和《神探阿蒙》；他痴迷语义搜索产品 Exa；他的人生锚点是那首《Desiderata》。

**深度阐述**

**推荐书目**：
1. **《猫的摇篮》（Cat's Cradle）** by Kurt Vonnegut——他喜欢冯内古特，这本书是他买给很多朋友的一份"有趣的推荐"；
2. **《艺术之战》（The War of Art）** by Steven Pressfield——他常回看，哪怕一次只读一两页。Lenny 特意澄清："不是《孙子兵法》，人们有时会听混——它是 the war of **art**，是"art"的双关，**关于创造性、关于做一件新东西的挑战、以及如何克服阻力。**"

**近期电影/电视**：
- 他**每年都会重看《卡萨布兰卡》**——巧合的是，片中有一个**姓氏和他一样叫 Ugarte 的角色**，是他印象中唯一在媒体里出现的"Ugarte"。他补充说，这名字在《卡萨布兰卡》里由 Peter Lorre 演的。
- 电视方面，他偶尔会看一集**《神探阿蒙》（Monk）**——这是他儿时和家人在电视上看的侦探剧，现在住在旧金山后又回过头去看，觉得它"是 90 年代末、2000 年代初旧金山的一个伟大时代快照"。

**最喜欢的 AI 产品**：Roman 说"如果推荐 Grok Bot 得额外加分，但他要给别的"。他一直是 **AI 语义搜索**的爱好者，喜欢**任何语义搜索引擎，尤其是任何怪异的语义搜索**。他曾是很早期**Metaphor（后来变成 Exa）**的用户。他喜欢用 Exa 在互联网上做"也许更奇怪的查询"，也看到很多人在做"MoMA 嵌入图像库的语义搜索"之类的东西。他说："任何**覆盖奇怪数据集的语义搜索引擎**，我都玩得很开心。" Lenny 确认："**Exa 是你特别会推荐的那个？**" Roman："**我爱 Exa。**"

**人生格言**：Roman 没有给出单一格言，而是分享了一首诗——**《Desiderata》**。他把它贴在自己门上，**从十几岁起就有它**，每搬一次家就重新贴一遍。这是一首很短的诗，**但每次读他都能在其中发现新东西，觉得它非常"落地"（grounding）**。

**个人感受**

这一段闪回了 Roman 作为一个"人"的多面性——他不仅是产品人，还是一个**会每年重看《卡萨布兰卡》、从少年时代就贴着一首诗、痴迷于用语义搜索探寻世界上奇怪角落的、有精神内核的人**。特别动人的是《Desiderata》——一本贴了二十年的诗，一本在数字化浪潮里被反复粘贴的自然语言内容。也许他选择语义搜索作为最爱，与他是一个"信息饕餮"、一个想理解世界的人的性格，是同源的。

---

## 结语：感谢与一段未完成的旅程 `[访谈段落 71-73]`

Roman 在最后强调了两件事：

**第一，他请大家持续反馈。** "我认为我们还处在非常早期的阶段。三周前我们才发布 beta。而我们从这批早期用户收到的很多反馈，正在**直接转化为我们构建什么、如何构建**。所以真的很感谢大家给出的所有输入。"

**第二，也是整个访谈的基调**：Lenny 的收尾堪称完美——"**这是多么不可思议的一个时间点。Grok Bot、整个 AI 都在这个时刻。一年后回看会非常有趣，我们会说'哇，我们关于这么多事情的判断，既对得离谱，也错得离谱。'**"

---

## 精华收获

**关于产品构建**
1. **从零开始的自由是无可替代的**：如果新能力面向的是新受众、新场景，把它外挂进老产品通常代价巨大。警惕"shipping your org chart"。
2. **小团队 + 物理隔离 = 敢于做不显而易见的微观决策**。追求大愿景的大团队会天然趋向保守。
3. **删功能比加功能更重要**：反复做"删除产品"的练习，把为迁就模型能力不足而存在的脚手架及时移除。
4. **少即是多**：不要暴露内部机制、不要给出"疯狂的旋钮"、不要强制用户学会某个抽象概念（比如 skills）。

**关于 AI Agent 的产品设计**
5. **一切上云**：让 agent 成为独立于设备的、状态一致的持久同事。
6. **每个 bot 需要自己的电脑**——就像新员工需要自己的笔记本一样，这是最基本的尊重。
7. **让 AI 拥有"具名的、长寿命的"身份**：这不是一次性会话，而是会学习、会变聪明的队友。
8. **从"同事隐喻"出发做决策**：争论不清时问"你会希望一个人类队友怎么做？"答案往往一致且清晰。
9. **下一波 AI 的转变**：从"你主动找 AI"到"AI 主动找你"。

**关于信任与体验**
10. **100% vs 90% 是断崖式的差异**：一个你只信任 90% 的协作者，会持续消耗你的注意力；100% 则带来真正的解放——"不看人传球"式的委派。
11. **产品应当被设计成"完成一整块工作"，而不是"起草一封邮件"**。

**关于组织与文化**
12. **"初创"的定义不是人数或融资轮次，而是那种"你能在短时间内做出极端影响"的冲刺能量**。
13. **两条支撑高速的价值观**："删除产品"和"去做那件事"——不是请求许可的文化。
14. **能快速适应的公司才能活下来**：AI 能力每几个月就变一次，产品必须在"六个月彻底重塑一次"的节奏里进化。
15. **护城河是被发现的，不是被规划的**：痴迷于"让现在不可能的事变得可能"，让用户告诉你什么是重要的。

**关于用户研究**
16. **手工 onboard 用户不是成本，是最高回报的投资**：亲眼看到用户体验中的卡点，比任何数据都更紧迫。
17. **不"引导证词"**：让用户在不受暗示的情况下自己走到使用模式，才能确信这是产品的自然形状。

---

<!-- TLDR: 一支被"关进洞穴"的小队一个月造出最火 AI 产品，成功源于"从零开始"和"把 AI 当同事"两条铁律 -->
<!-- TAGS: AI Agent, 产品设计, Grok Bot, Cursor, 创业方法论 -->
<!-- RATING: 5 -->
