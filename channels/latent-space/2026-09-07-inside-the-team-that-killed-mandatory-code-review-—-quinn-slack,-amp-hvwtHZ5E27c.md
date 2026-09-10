---
title: "Inside the Team That Killed Mandatory Code Review — Quinn Slack, AMP"
channel: "Latent Space"
published: "2026-09-07"
source_url: "https://www.youtube.com/watch?v=hvwtHZ5E27c"
video_id: "hvwtHZ5E27c"
tags: ["AI编程", "智能体", "工程管理", "云端开发", "创业组织"]
rating: 5
language: "英文"
word_count: 33311
duration: "40:14"
---

# Inside the Team That Killed Mandatory Code Review — Quinn Slack, AMP

- **Channel:** Latent Space
- **Published:** 2026-09-07
- **Source:** https://www.youtube.com/watch?v=hvwtHZ5E27c
- **TL;DR:** 小团队+高信任+云端智能体，正在让代码审查、本地开发和 GitHub 悄然死去。
- **Tags:** AI编程, 智能体, 工程管理, 云端开发, 创业组织
- **Rating:** 5

## 版本

- [结构化文稿](2026-09-07-inside-the-team-that-killed-mandatory-code-review-—-quinn-slack,-amp-hvwtHZ5E27c.structured.md)
- [原始文稿](2026-09-07-inside-the-team-that-killed-mandatory-code-review-—-quinn-slack,-amp-hvwtHZ5E27c.transcript.md)

# 当一支 20 人团队决定"杀死"代码审查：AMP 创始人 Quinn Slack 谈软件工程的范式转移

**材料信息**

- **标题**：Inside the Team That Killed Mandatory Code Review — Quinn Slack, AMP
- **作者/来源**：Latent Space 播客（主持人 swyx 与 Alessio 的访谈节目）；受访者为 Quinn Slack，Sourcegraph 联合创始人、AMP 联合创始人兼 CEO
- **类型**：YouTube 视频字幕（访谈播客实录）
- **关键元数据**：时长约 30–60 分钟（Latent Space 惯常时长），录制地点为慕尼黑远程演播室，录制时 Quinn 正参加 AMP 团队在慕尼黑的线下团聚；对话覆盖 2025 年前后 AI 编程工具与工程组织变革的最新实践

---

## 开篇引入

如果有一个软件团队公开宣称"强制代码审查已经死了"，并且不是作为一种叛逆姿态，而是在交付了真实产品、拥有真实付费客户、并且在持续盈利的基础上说出来的——你会怎么看？

这正是 AMP 团队正在做的事情。Quinn Slack 曾创办 Sourcegraph，为全球前十大科技公司中的九家提供代码搜索服务，客户遍及顶级银行和 Uber、Stripe 等公司。但在 2024–2025 年，他把 Sourcegraph 中孵化出的 AMP 产品线分拆成一家独立的 20 人公司，并做了一个激进的决定：不再要求任何代码在上线前必须经过人工审查。

这期 Latent Space 的访谈之所以值得深读，不仅因为它提出了一个冲击性的论断，更因为 Quinn 把支撑这个论断的整套工程系统、组织哲学、安全模型、工具链选择，乃至他对整个软件产业未来格局的判断，都摊开来讲了一遍。从他如何用云端智能体（orbs）替代本地开发，到他如何在飞越半个地球的航班上让智能体自动完成数据库迁移，再到他为什么认为"GitHub 会悄无声息地死去"——这是一份关于"当 AI 智能体真正成熟后，软件公司怎么运转"的第一手田野报告。

更重要的是，Quinn 描述的并不是未来某个时间点的理论构想。他和他的团队已经这样工作了好几个月。正如他说的："我们正在提前体验其他团队六个月后的工作方式。"

让我们跟着这场对话，一层一层地拆开这场正在发生的变革。

---

## 一、背景：一支分布在三大洲的 20 人全栈团队 `[00:00-01:30]`

**核心观点**
AMP 是一支完全远程、分布在全球三大洲的 20 人团队，所有人都像联合创始人一样思考和行动——这构成了后续所有激进工程决策的组织前提。

**深度阐述**

访谈一开始，主持人注意到 Quinn 又在"世界上的某个地方"。他们刚在慕尼黑办完一场全团队的线下聚会（offsite）。Quinn 介绍了团队的分布结构：三分之一在欧洲，三分之一在美国，三分之一在澳大利亚。

这里面藏着一个对远程公司的洞察，值得所有创业者记住。Quinn 说，当你经营一家远程公司时，一个基本原则是——**你本来要花在办公室上的钱，最终都得花在线下聚会（off-site）上**。这个逻辑很有意思：远程办公不是让你省下办公室租金，而是让你把这笔预算转移到让团队定期见面上。对一家分布在三大洲、跨越十几个时区的团队来说，线下聚会不是福利，而是维系信任和共识的必需品。

Quinn 提到他们也很喜欢在新加坡办聚会（顺带调侃了新加坡的空调比德国当时的天气舒服）。这个细节看似闲聊，实际上暗示了 AMP 在亚洲有重要的团队和业务布局。

**延伸思考**

远程团队的"办公室预算→线下聚会预算"转化逻辑，本质上是在回答一个更根本的问题：分布式组织的凝聚力从哪里来？当团队成员日常不见面时，信任、默契、共同品味这些东西无法通过 Slack 消息自动传递，必须通过高质量的面对面时间被"重新充电"。这也解释了为什么 AMP 后来敢于取消代码审查——因为团队已经建立起了足够的信任密度，这正是 Quinn 在后面会反复强调的"最重要的系统"。

---

## 二、orbs 的登场：为什么"砍功能"比"加功能"更重要 `[01:30-05:00]`

**核心观点**
在 AI 快速演进的时代，把用户留在旧工作方式上的价值是**负的**；AMP 的核心策略是主动砍掉过时功能，把用户"拽"到前沿，而 orbs 就是这一策略的集大成者。

**深度阐述**

主持人请 Quinn 介绍一下 AMP 最新的进展，尤其是最近热议的"orbs"。Quinn 的回答非常有哲学意味，值得逐层展开：

**第一层：AMP 的使命是"探索前沿"**

Quinn 说，AMP 想做的事是问自己一个疯狂的问题——"我们能做的最疯狂的事情是什么？我们如何砍掉那些旧功能，让 AMP 成为使用智能体的最佳方式？"这里的关键承诺是：如果你用 AMP，你就是在走"被祝福的路径"（happy path），你会走在最前沿。

**第二层：用"砍功能"来逼用户前进**

AMP 早期就杀掉了编辑器扩展（editor extension），之后陆续砍掉了大量功能。Quinn 坦言："过去几个月，比起增加功能，我们更以砍功能而闻名。"他承认有些人在开玩笑，但他坚信这是正确的决定。

为什么？因为他观察到一个 AI 时代特有的规律：

> "随着 AI 发展如此之快，把用户留在旧做法上的价值实际上是负的。"
> "With AI moving so fast, the value of keeping users on doing the old thing is actually negative." `[03:30 左右]`

他对比了两个时代：**过去**，技术周期是 5 到 10 年，你获取一个用户，他可能跟你十年。**现在**，如果你不推着、拽着用户跟你一起站在前沿，那么三个月后，用户会说："嘿，这些蠢货和他们的产品，已经过时了。"然后他们会因此看低你。

这是一个极其反直觉但可能确实正确的洞察。在慢速技术周期里，"稳定性"和"向后兼容"是美德；但在快速技术周期里，"让用户停留在旧体验上"反而会加速他们对你的不信任。

**第三层：orbs 是什么，以及承认前人功劳**

那么 orbs 到底是什么？根据 Quinn 的描述，它是**一种使用 AMP 的方式，让智能体远程运行在云端**。其核心体验是：你可以合上笔记本电脑，然后并行做 100 件事。

这里 Quinn 非常大方地致敬了先行者："我们不是第一个想到这个点子的人。Devon 得到了巨大的认可（massive props）——他们很早就做这件事了，当时还被嘲笑'这行不通'。而他们是对的，这件事很重要。"（Devon 是一家专注 AI 编程的产品公司。）这种公开承认前人贡献的态度，在竞争激烈的 AI 编程工具赛道里颇为难得。

**第四层：orbs 的关键不是"远程"，而是"一切都刚刚好"**

Quinn 强调，orbs 的价值不在于"智能体跑在云上"这个单一事实，而在于 AMP 把整套体验打磨到了"端到端开箱即用"：

- 你能在门户里看到你的 dev server，它会正常工作
- 你能访问桌面环境
- 你可以并行运行多个实例
- 一切都能顺畅运行

他给出的结论非常强势：**"本地开发在我们看来已死。"**（"Local dev in our opinion is dead."）`[04:30 左右]`

他还提到一个规模数据：**"我们的客户在过去三四周里使用 orbs 的增量，超过了过去一整年里软件构建方式变化的总和——而去年的变化可不少。"** 这个对比的力度很大，说明 orbs 带来的是一种"体验跃迁"式的采用，而非渐进式的改良。

**精华收获**

- 在快速技术周期中，主动"砍功能"和"逼迫用户前进"可能是比"堆功能"和"保兼容"更正确的产品策略。
- orbs 的启示是：判断一个新范式能否成立，不要只看它单个技术点有多强，要看整套体验是否被磨到"摩擦接近零"。用户不会为"更好的单点"迁移，只会为"整体上更省心"迁移。

---

## 三、"本地主机之死"：一个酝酿了四年的预判 `[05:00-07:00]`

**核心观点**
Quinn 早在 2021 年就写过"本地主机的终结"，但当年大公司的云端开发环境体验太差、代价太大；而在有 AI 智能体之后，云端开发的体验不但追平甚至超过了本地开发。

**深度阐述**

Quinn 在这里做了一件很漂亮的事：他把"本地开发已死"这个新判断，追溯到了自己四年前的思考。

> "我想我在 2021 年写过一些东西，关于'本地主机的终结'。"
> "I think I wrote something in like 2021 about the end of localhost." `[05:00 左右]`

他指出，**即使在 AI 之前**，大公司（Facebook、Google、Uber 等）早就有这样的模式：你主要通过 SSH 登进一台机器，或者在本地保留一个非常轻量的克隆，真正的计算发生在云端。他提到 Stripe 也是如此——一旦基础设施足够好，**你的笔记本电脑就变成了一个薄壳**，你甚至可以在 iPad 上写代码，因为它只是一个向云端基础设施输入的设备。

但随后，主持人（swyx）提出了一个非常关键的"但是"：

> "但即使在那时……我认识很多在那些公司工作过的人，他们会说：'是啊，但它更慢，你放弃了很多。在你的笔记本上工作其实感觉很好，一切都更快。'" `[05:40 左右]`

这个反驳极其重要，因为它揭示了当年云端开发为什么没能普及。Quinn 承认了这一点，但他给出了转折：

> "（过去）它更慢，你要牺牲很多。但当智能体能远程运行时，你不再觉得在牺牲任何东西。你不想用本地开发了。"
> "With agents when you can run them remotely, you don't feel like you're giving anything up. You don't want to use local dev." `[06:00 左右]`

他还强调了一个关键区别：**这不再是"公司安全部门强迫你用开发 VM"，而是开发者自己主动的选择**。

> "不是你的企业安全部门说'嘿，我们需要给开发用虚拟机'。而是你自己意识到：'嘿，我已经两周没启动我的本地开发服务器了。'"
> "Hey, I haven't run my local dev server in two weeks." `[06:30 左右]`

这句话是整段访谈里最有"现场感"的一句。它把"本地开发已死"从一个观点，变成了一个 Quinn 亲身体验到的事实。他最后补了一句非常重要的平衡话：你**确实**需要投资于云端环境搭建，但这并不像人们说的那么令人望而生畏，"而且现在你可以把智能体丢上去帮你搞"。

**延伸思考**

这里有一个"技术采用时机"的微妙洞察值得深挖：**一个想法对的时机，不一定等于它可行的时机**。Quinn 在 2021 年就看到了"localhost 的终结"这个方向，但当时只有大公司能承受云端开发的摩擦成本。直到 AI 智能体出现，云端开发才第一次同时满足了两个条件——**体验不低于本地（甚至更好），且能自动化搭建成本**。这对所有"提前太早"的创业者都是一个提醒：你可能方向是对的，但你需要等到某个关键技术补丁（这里是 AI 智能体）出现，才能把你的正确判断变成可规模化的现实。

**精华收获**

- 云端开发的分水岭不是"能不能做"，而是"是否感觉不到牺牲"。AI 智能体补上了这最后一块拼图。
- 判断一个新范式是否成熟，可以问自己："用户是**被迫**迁移，还是**主动**迁移？"Quinn 说的"我没有运行本地 dev server 两周了"就是主动迁移的信号。

---

## 四、为什么是现在？集体临界点的三个原因 `[07:00-09:30]`

**核心观点**
主持人观察到整个行业（OpenCode、Conductor、Claude、Cursor 等）几乎同时转向云端/远程智能体，Quinn 给出了三个原因：智能体在长任务上变强、停止审查代码释放了并行能力、以及 CLI 智能体在去年 12 月到 1 月的爆发。

**深度阐述**

主持人先描述了一个行业现象：Quinn 正在做的转型，很多人都在同时做——OpenCode 在做、Conductor 在做、Claude 做了很多、Cursor 也做了，甚至有点意外的是 Codeex 还没完全做。这引出一个"meta"层面的问题：**为什么这个转变恰好发生在现在？**

Quinn 给出了三条理由，层层递进：

**理由一：智能体在长周期任务上确实变强了**
> "智能体在更长的任务上确实变得更好了。"
> "The agents have gotten better for sure on longer horizon tasks." `[07:40 左右]`

**理由二：停止审查代码→释放时间→更多并行**

这是最精彩的一条。Quinn 说：

> "当你看到智能体足够可靠地做对足够多次，然后你开始停止审查所有代码，这就释放了你更多的时间去做更多的事。"
> "when you see the agent so reliably getting it right enough times and you start to stop reviewing all of the code then that frees up more of your time to run more things." `[07:50 左右]`

这句话揭示了"取消代码审查"和"更大并行度"之间的因果链。并行做事本身不产生价值，只有当你不再被"审查队列"卡住时，并行才真正变成生产力。

**理由三：CLI 智能体的爆发是前提条件**
> "我们大概在去年 12 月和 1 月经历了这个——那时候 CLI 里的智能体真正起飞了，而那只是下一步的前提。"
> "we had to over like uh December and January that's when really agents in the CLI took off and that is just a prerequisite for this next step." `[08:15 左右]`

**关于"采用速度"的观察与现实的阻碍**

Quinn 抛出一个判断：这个转变比任何他见过的技术采用都更快，**但它仍然以人类的速度推进**。他列举了现实中的两种阻力：

- 有人说："我为什么需要这个？我在笔记本上有本地开发环境，一切都设置好了。"
- 有人说："如果我的公司必须审查代码，那么我把 20 件事排队等审查有什么好处？我并不能从更大的并行度中获益。"

这个观察很清醒：**技术拐点在个人层面可能已经到来，但在组织层面还受制于流程、审查制度和信任结构**。这正是 AMP 团队的特殊之处——20 个人，全是联合创始人，思维高度一致，因此能真正享受到并行度带来的红利。

Quinn 最后用一句话概括了他们的位置：

> "我们正在体验其他团队六个月后将采用的工作方式。"
> "we are kind of getting to experience what other teams will be working like in 6 months." `[09:20 左右]`

**个人感受**

这段话透露出 Quinn 的一种"提前进入未来"的骄傲感，但又不显得傲慢——他承认自己的团队有特殊条件（全是联合创始人、高度同质化）。这种"我们很幸运能提前体验，但我们也知道这不是所有人都能复制的"态度，反而让他的判断更可信。

---

## 五、核心炸弹：强制代码审查已死 `[09:30-11:30]`

**核心观点**
AMP 团队彻底取消了"代码进入主干前必须人工审查"的强制要求。支撑这一点最重要的"系统"不是工具，而是一个高度被信任的团队；而取消审查带来的收益是"15 分钟内修复问题"的高响应速度。

**深度阐述**

主持人直接抛出问题："等等——代码审查在你们那儿死了？"Quinn 的回答干脆利落：

> "合并到 main 之前的强制代码审查？是的，它死了。从我们开始做 AMP 起就死了。"
> "Mandatory code review before it gets to main. Yeah, it's dead. It's been dead ever since we started working on AMP." `[09:40 左右]`

这是一个非常强的声明。主持人立刻追问：那你们一定投资了一些系统来弥补少了代码审查的缺位吧？

Quinn 的回答是全篇最核心的一句之一：

> "是的，没错。最重要的系统是拥有一支真正被信任的团队。"
> "the most important system is having a team that is really trusted." `[10:00 左右]`

然后他解释了这个"系统"如何与 AI 配合：

> "AI 做到的一件事是，它意味着你可以拥有一支更被信任的团队，他们有更多的利害相关（skin in the game），有更多的端到端所有权。他们不是从产品经理和某个 sprint 那里接收输入、然后输出给市场团队去发布的自动机器。人们有更多的利害相关，他们是被问责的，这是你避免代码审查所需要的最重要的东西。"
> "People have a lot more skin in the game. They're accountable and that's the most important thing you need to have to avoid code review." `[10:10 左右]`

这里有一个深刻的组织洞察：**AI 让"小规模高信任团队"变得可行，因为它允许你不必为了协作而雇佣大量你不完全信任的人**。当每个人都能对任何 bug、任何客户、任何决策负责时，代码审查这种"事后把关"机制的必要性就下降了——因为把关已经被前移到"招对人"这一步了。

**收益：从"天"到"分钟"的响应速度**

Quinn 给出了取消审查的具体收益：

> "你希望达到这样一个状态：当你在日志里或从客户那里收到问题时，你可以在 15 分钟后发布一个修复。"
> "you want to get to a place where you can ship a fix 15 minutes after you get, you know, something in the logs or something from a customer." `[10:30 左右]`

**它不是万能药：MTTR vs. MTBF**

但 Quinn 非常诚实地划定了适用边界。他用了一个工程术语来做对比：

> "这绝对不是适合所有软件的做法。它是'平均恢复时间（MTTR, meantime before recovery）'对'平均故障间隔时间（MTBF, meantime before failure）'的不同取舍。但对于移动如此之快的面向用户软件，这对我们是正确的做法。"
> "it's the meantime before recovery versus the meantime before failure approach, but for end user software that's moving so quickly, that's the right approach for us." `[10:50 左右]`

这个对比极其精准。传统上，代码审查是为了降低**故障发生的概率**（提高 MTBF）。而 AMP 的选择是接受可能更高的故障率，换取更快的**故障恢复速度**（降低 MTTR）。在高频迭代的面向用户产品里，这往往是一种更优的取舍——因为用户对"快速修复"的感知，往往优于对"从不失误但反应迟缓"的感知。

他最后补了一句很有意思的判断：

> "我认为这比我们不得不等上几天才能发布东西的质量更高。"
> "it's higher quality than if we had to wait, you know, days to ship something." `[11:20 左右]`

**延伸思考**

"代码审查已死"这个论断，如果被断章取义地传播，会非常危险。但 Quinn 的完整表述其实非常审慎：它建立在一支高信任团队之上，适用于快速迭代的面向用户软件，是一种**主动的 MTTR/MTBF 取舍**，而非"不需要质量"。这提醒我们，很多在社交媒体上看起来激进的论断，在原始语境里其实是高度条件化的。读这类内容时，**条件（context）比结论（conclusion）更重要**。

**精华收获**

- 取消代码审查的前提不是"AI 足够强"，而是"团队足够被信任、足够有所有权"。AI 是放大器，不是替代品。
- 当你能把响应时间从"天"压缩到"分钟"，用户感知到的质量反而可能更高。这是 MTTR 优先于 MTBF 的战略取舍。

---

## 六、智能体不止改变"构建软件"，更改变"使用软件" `[11:30-15:00]`

**核心观点**
智能体不仅改变了软件怎么被构建，也改变了软件怎么被使用和运行。AMP 的"apps"（迷你应用模式）展示了这样一个未来：你不再需要设置界面、集成、MCP，因为"智能体是任何软件的终极设置界面，而代码是任何软件的终极设置界面"。

**深度阐述**

Quinn 话锋一转，说他看到智能体不只是在改变**构建**软件的方式，也在改变**运行和使用**软件的方式。他展示了自己"非常凌乱的工作中版本"，然后亮出了一个叫 **apps** 的东西。

**apps 是什么？**

它让你可以**临时起意地（ad hoc）创建软件**，它在 orb 里运行，里面有一个智能体，你可以让智能体直接对它做即时修改（instant fixes）。

Quinn 现场演示：他打开一个应用，并解释底层发生了什么——这其实解决了一个 AMP 被抱怨最多的问题："你得等沙箱启动"。这个应用的底层逻辑是：启动沙箱，然后在上面跑一个讲 HTTP 的进程，于是他就能看到它了。

**这是什么东西？一个"临时仪表盘"**

Quinn 解释，这是团队里某人做的一个临时仪表盘。他做了一个历史对比：

> **两年前的做法**：某个人（大概在数据团队）会去往 Looker 之类的工具里加一个新的 SQL 查询。
> **中间演进**：有人会说，为什么不让我们的仪表盘工具有个 MCP（模型上下文协议），这样它就能和我们的智能体交互？
> **现在**：为什么还要有这些？

然后他抛出了全篇最犀利的一句论断：

> "当实际上智能体是任何软件的终极设置界面，代码是任何软件的终极设置界面时，你为什么要买一个现成的软件包来做仪表盘，承担它带来的所有开销（设置界面、复杂集成、MCP）？"
> "an agent is the ultimate settings screen for any software and code is the ultimate setting screen for any software." `[13:40 左右]`

他总结说，这只是一个开始——智能体正在改变你**使用**软件、**运行**软件、**分发**软件的方式。AMP 正试图弄清楚这一切会走向哪里。

**从"设置界面"到"可 fork 的软件"**

主持人接着把这个话题引向"内部工具"（internal tools），并补充了自己的观察：

> "我认为让人们拥有**可 fork 的软件（forkable software）**很重要，即使它不是完全开源的。只要前后端契约保持稳定、尊重安全与隐私，那么你想干什么都行，它只是 UI，我不在乎。"
> "I think it's important for people to have forkable software effectively even if it's not entirely open source... then do whatever you want like it's just UI don't care." `[14:30 左右]`

主持人还提到他看到一种"迷你应用模式（mini app pattern）"正在多家公司出现——你可以构建一个应用，它和公司数据之间有一些松散语义（less semantics），应用之间也有，为了可复用性；然后人们可以**fork 它**，就像你在 Replit 里那样。

**一个行业级观察："所有人都在造同一个东西"**

主持人有一段很有意思的感慨，值得完整保留：

> "对我这个企业主来说，感觉最终每个人都在造同一个东西。我们都在试图弄清楚这件事，而你把整个软件产业压缩进了这个小小的泡泡里，大家唯一给它起的名字就是'智能体'。但你知道它会再次膨胀开来，我们都会重新找到不同类别之间的分界线。而这正是令人兴奋的地方——没有人知道（会怎样）。"
> "you've taken like the entire software industry and you've compressed it into this tiny bubble that the only name that people have for it is like agents... Nobody knows." `[15:00 左右]`

**延伸思考**

"智能体是任何软件的终极设置界面"这句话，可能是这段访谈里对产品设计最有启发的判断。它意味着：传统 SaaS 之所以需要设置页、集成、插件、MCP，本质上是因为**软件无法理解你的具体意图，所以你必须手动配置它**。当智能体可以理解意图、修改代码、即时定制时，大量的"配置基础设施"就变得多余了。这直接动摇了传统 SaaS 的护城河逻辑——如果你的产品只是"一个 UI + 一堆设置"，那么用户可能宁愿自己用智能体生成一个。

---

## 七、Cloudflare OS、Sandstorm 与"拥有自己的软件" `[15:00-16:30]`

**核心观点**
Cloudflare 刚发布的"Cloudflare OS"被 Kenton Varda 称为"Sandstorm V2"，而 Sandstorm 正是十多年前一个"拥有你自己的软件/个人云"的先行者，理念超前于时代。

**深度阐述**

主持人问 Quinn 是否看到了 Cloudflare 刚发布的东西——那个"agent OS"。Quinn 说看到了，并指出 **Kenton Varda 基本上把它称为 "Sandstorm V2"**，指的是他之前的创业项目。

Quinn 说他记得 Sandstorm，而且**在过去几个月里，每当他们探索这些方向时，他每天都在想它**。

主持人坦白自己当年虽然在科技圈，但并不知道 Sandstorm，请 Quinn 复盘一下。Quinn 的复盘：

> "Sandstorm 就像一个自托管的 Web 应用，你可以把打包成容器、完全气隙隔离（airgapped）的应用拉进来。它们有几种方式可以互相通信，所以你可以在你自己的自托管单元里引入一套办公套件、一个邮件应用等等。它们有有限的 API 来完成需要做的事，就像一个操作系统。它是完全容器化的。所以这是'拥有你自己的软件、拥有你自己的内部个人云'的理念。它是超前于时代的。"
> "it was this idea of own your own software, own your own like internal personal cloud and it was ahead of its time." `[16:00 左右]`

**与当前的连接**

主持人把这个和 Quinn 前面说的"为什么要设置界面，当你可以自己定制应用"联系起来，认为两者很相似。Quinn 表示认同，并重申了"可 fork 软件"的理念。

这里其实形成了一个跨越十余年的呼应：**Sandstorm 在 2010 年代想做"每个人拥有并定制自己的软件"，当时失败了（太超前、体验太重）；而今天，同样的理念在智能体和云端沙箱的加持下，第一次变得可行**。这正是本场访谈反复出现的一个主题：**好想法往往需要等到正确的技术补丁出现才能落地**。

**延伸思考**

Sandstorm→Cloudflare OS→AMP orbs 这条线索，揭示了一个被长期忽视的产品哲学：软件不应该是一个"你要去适应它"的黑盒，而应该是"你可以拥有、可以修改、可以 fork 的"东西。云计算时代，这个理念一度被"everything as a service"淹没了——你并不拥有你的软件，你只是在租用。而智能体的出现，可能让"拥有软件"以新的形式回归。

---

## 八、Ops 的自动化：一次飞越半个地球的数据库迁移 `[16:30-19:30]`

**核心观点**
智能体不仅在写代码，还在做运维（ops）——它能分阶段部署、监控日志、校验数据库不变量，出错就回滚。Quinn 在飞往慕尼黑的航班上，让智能体自动完成了一次核心数据模型的迁移。

**深度阐述**

Quinn 说他看到的另一个大方向是：智能体能帮你做的不只是编程，还有真正的**运维（ops）**部分。他举了一个现场的例子。

**例子：AMP 的核心数据模型迁移**

他打开 AMP，展示了一个叫 **Phase 1 B2** 的东西。这是什么？是让 AMP 从"用户只能在一个工作区里"变成"可以在多个工作区里"。任何做过软件的人都知道，这种改动是**对最重要的数据模型的核心改动**。

> "这种改动完全是一团乱麻，你必须把它分成很多步骤来分阶段推进，才能让所有东西都向后兼容。"
> "that kind of change is like a change at the core of the most important data models. And that's totally messy and you have to stage it out over so many different steps." `[17:10 左右]`

**智能体做了什么？**

Quinn 描述说，让智能体逐步走完这些阶段是极其强大的。具体流程是：

1. 智能体部署一个阶段
2. 部署后，它去**监控日志**
3. 它去**监控数据库**，确认它预设的那些**不变量（invariants）**成立
4. 确认没有大量意外的错误
5. 如果一切正常，就进入下一个阶段；如果出问题，就**回滚**（roll back）

**最精彩的故事：飞机上的迁移**

然后 Quinn 讲了这段访谈里最具画面感的一个故事：

> "一周前我飞往慕尼黑。我当时在做这个迁移和其他一些事。在 12 小时的航班上，飞机 Wi-Fi，你永远不知道会怎样。我让它推送了几个相当安全的阶段并监控日志。如果一切正常，它就进入下一阶段；如果不行，它就回滚。最终飞机 Wi-Fi 表现得挺好的，但我在飞机上睡了一会儿。"
> "on a 12-hour flight with airplane Wi-Fi... I had it push out a few stages that were pretty safe and monitor the logs. And if everything was good, then it would go on to the next phase. And if not, then it would roll back." `[18:00 左右]`

**这解决了什么？**

Quinn 指出：

> "这是那种在过去会占用一个开发者、或者也许一群人加上运维人员全程盯着的事情。"
> "this is the kind of thing that in the past would occupy maybe a dev or maybe like a bunch of people and ops people just babysitting that the whole time." `[18:20 左右]`

**个人感受**

这个故事的力量在于它的"具体性"。它不是一个抽象的"智能体能做运维"的论断，而是一个具体的、可验证的场景：创始人躺在 12 小时航班的座位上睡觉，他的智能体在自动完成数据库迁移、监控、校验、回滚决策。这是"人们的工作方式真的变了"的最生动证据。

**精华收获**

- 智能体的价值正在从"写代码"扩展到"运维"——这是很多人还没有意识到的应用场景。
- "让智能体处理一个有序的阶段序列，每个阶段都自带监控和回滚" 是一个可复用的模式。它把高风险的大改动，分解成智能体可以自主决策的小步骤。

---

## 九、安全悖论：云端智能体比本地智能体更安全 `[19:30-21:30]`

**核心观点**
直觉上人们觉得"给智能体开放生产日志访问权限"很可怕，但 Quinn 指出：**在云端用 OIDC 给智能体限时的、只读的、最小化的访问权限，其实比让一个跑在开发者笔记本上、拥有开发者全部权限的智能体安全得多**。

**深度阐述**

Quinn 预判了人们会有的恐惧：

> "很多人会说：'你怎么能给智能体访问生产日志的权限呢？'这会让人们有点恐慌。"
> "how do you give your agent access to production logs, right?... that kind of freaks people out." `[19:00 左右]`

然后他给出了一个反直觉的对比论证：

**方案 A（云端，AMP 的方式）**：给运行在云端的 orb/智能体**有意限制的、最小化的访问权限**——通过类似 OIDC 的机制，拿到一个令牌，只允许它对 GCP 日志、或对生产数据库有 **30 分钟的只读访问权限**。

**方案 B（本地，现状）**：让一个运行在开发者笔记本上的智能体，**潜在地拥有开发者在这台机器上被授权访问的任何东西的无限访问权限**。

Quinn 指出，方案 B 才是真正危险的：

> "我们已经看到智能体非常擅长突破隔离（escaping containment）——整个 Hugging Face 的翻车事件等等。我们也从一些用 AMP 的客户那里听说，他们有另一个恰好被认证过的脚本，找到了通往生产控制台的路。我认为这在所有智能体里都会发生。"
> "we've seen that agents are very good at escaping containment with the whole like hugging face debacle... I think this happens in all agents." `[20:00 左右]`

他得出结论：

> "现在既然有了比'在开发者笔记本上跑一切'更好的替代方案——而这个笔记本就其本性而言几乎可以做任何事、可以打破玻璃进到生产——现在有了替代方案，我觉得 CLI 编程智能体是一件很不安全的东西，你会想要迁移到云端。"
> "it feels like a CLI coding agent is a really insecure thing and you want to be moving to the cloud." `[20:20 左右]`

**最反直觉的结论**

> "你可能以为最害怕迁移到云端的是安全人员，但我们已经看到，我们的一些大客户（也这么觉得），它看起来更安全。"
> "you might think that it's the security people that are most scared about moving to the cloud, but we've seen... it is seeming more secure." `[20:40 左右]`

**双重收益 = 更快的迁移**

Quinn 的收尾判断很有力：

> "不仅开发者的体验好得多（他们可以并行做很多事，不用做 worktree 那些舞蹈），而且它更安全。这意味着这个转变会比人们想的快得多，因为如果安全和开发者都从中受益，那么……我不知道，两个月后，我们可能就会看到 CLI 编程智能体基本死了。"
> "in 2 months, we could be seeing CLI coding agents is basically dead." `[21:10 左右]`

**主持人的补充：UX 上的根本张力**

主持人（swyx）提出了一个很重要的平衡观点。他说人们喜欢那种"无限制的访问"带来的通用智能和完全自主。他反思了 OpenClaw（可能是某个开源本地智能体）的情况：人们直接跑 OpenClaw，它并不安全，完全本地；而且有时你把它放进一个盒子反而更糟，因为你无法提前预料到自己的需求。

他点出了一个根本张力：

> "在 UX 上存在一个根本张力：'我拥有所有东西、我把你当作团队里的一个完整的人来对待' versus '因为你对我安全的担忧，你还被我紧紧牵着绳子'。"
> "there's a fundamental tension in the UX between you just have everything and you're I treat you as a full human that's on my team versus you're still on a tight leash." `[21:40 左右]`

但他认为这只是个人偏好问题，AMP 提供并解决这个问题仍是整个版图的重要部分。

**Quinn 的回应：真正的赢点是"摩擦归零"**

Quinn 承认，如果 orbs 的唯一卖点只是"更安全"，那它赢不了。真正的杀手是**把开发者的摩擦降到零**：

> "但还有一点是让开发者的摩擦归零——他们可以一次性启动 20 个东西，它们不冲突，都有正确的访问权限，这是一种非常神奇的感觉。"
> "there's something about getting that friction to zero for the developer where they can spin up like 20 things at once and they don't conflict and they all have the right access and it's just a really magical feeling." `[22:00 左右]`

他最后确认：**不只是安全，也是开发者推力（dev push）**。

**延伸思考**

这段"安全悖论"是整场访谈里最反直觉、也最有价值的论点之一。它提醒我们：**很多关于 AI 安全性的直觉判断，可能正好是反的**。人们害怕"云端智能体访问生产环境"，但真正的风险源其实是"本地智能体拥有开发者的全部权限"。Quinn 的建议——用 OIDC 给智能体限时的、只读的、最小化的权限——本质上是在把"最小权限原则（principle of least privilege）"应用到 AI 智能体上。这是一个可以直接借鉴的安全设计模式。

**精华收获**

- **最小权限 + 限时 + 只读**：给云端智能体的访问令牌应该是临时的、只读的、作用域最小的。
- 判断一个方案是否更安全，不要看直觉，要看"爆炸半径"（blast radius）——本地智能体的爆炸半径是开发者的全部权限，云端沙箱则小得多。
- 让用户迁移的最强动力不是"更安全"，而是"摩擦归零 + 更安全"的双重收益。

---

## 十、GitHub 的悄然死亡 `[21:30-24:30]`

**核心观点**
AMP 团队几乎不再访问 GitHub——不用 issue、不用 PR、很少用 Actions。他们转向 AMP 托管的临时仓库。Quinn 引用了那句经典判断："这些东西不会轰然倒塌，而是悄然消逝。"

**深度阐述**

Quinn 主动开启了这个话题：他们的主仓库仍在 GitHub 上，但——

> "我们基本上从不去 GitHub。我们唯一去 GitHub 的时候是 GitHub Actions 出问题的时候——这在过去 24 小时里发生了好几次，比如那好几小时的宕机。"
> "we basically never go to GitHub. The only time we go to GitHub is if there's like a problem with our GitHub actions." `[22:00 左右]`

**发生了什么变化？**

他们越来越多地使用**由 AMP 托管的临时仓库（ad hoc repositories）**。然后 Quinn 说出了那句极具传播力的判断：

> "这不是说 AMP 是 GitHub 杀手。它是**下一个 GitHub**。这些东西不会轰然倒塌，而是悄然消逝（they die with a whimper）。我们甚至不再想到 GitHub 了。我们不用 issues，不用 pull requests，我们几乎不用 GitHub Actions，而且我们正试图摆脱它。"
> "It's not like AMP is the GitHub killer. It's the next GitHub. These things don't die with a bang. They die with a whimper." `[22:40 左右]`

**一种"疯狂的感觉"**

Quinn 表达了一种近乎超现实的感受：

> "我们目前用它来推送我们的仓库，但某人可能会在我们不知情的情况下改变这一点，然后一周后说：'嘿大家，猜猜怎么着？'这是一种疯狂的感觉，因为从我记事起我就在用 GitHub。感觉就像一个所有人都在上面的地方。"
> "it's kind of a crazy feeling because I've been on GitHub for as long as I can remember." `[23:00 左右]`

他提到，他已经把自己所有的个人项目都迁移到了 AMP 托管的仓库（底层运行在 Pierre 的代码/后端上），并且**完全不想念 GitHub**。

**一段关于平台霸权的隐喻**

这里 Quinn 的观察非常值得玩味。社会学家曾描述权力更替往往是"bang"（轰然）还是"whimper"（悄然而逝）的差别——很多看似不可动摇的基础设施，不会在某个戏剧性时刻倒塌，而是在一个又一个人的日常习惯里慢慢被遗忘。GitHub 之于软件开发，就像当年的 SourceForge 之于开源——它没有"死"，但没人会再想起它。

**延伸思考**

"下一个 GitHub"这个表述耐人寻味。它暗示了一种可能性：AI 时代的代码托管基础设施，不是"更好的代码托管网站"，而是**编程智能体的附属物**。当智能体成为主要的代码生产者、审查者和部署者时，"托管代码"这件事会自然地融入到智能体工作流中，而不再需要一个独立的、以人为中心的网站。这是一个"基础设施消失于工作流"的经典模式——就像没人会专门"去用电",它只是插座里流出来的东西。

---

## 十一、代码存储、CI 与"编码 SaaS 将是世界上最后的 SaaS" `[24:30-28:30]`

**核心观点**
Quinn 高度评价他们家用的代码存储服务（Code Storage / Pierre），并抛出了一个宏大的判断："**编码 SaaS 将是世界上最后的 SaaS**"，因为其他所有 SaaS 都可以通过编码 SaaS 被构建出来。同时，他和主持人共同探讨了"CI 是否还有必要"这个问题。

**深度阐述**

**关于代码存储的评价**

主持人请 Quinn 以第三方身份评价代码存储服务。Quinn 的回答是好评：

> "它做到了我们想要它做的一切。它很可靠，我们非常了解这个团队，那里也有一些前 Sourcegraph 的人，所以是非常值得信任的人。每当我们有需求，他们都会完成。我希望他们能更快完成，但他们确实会完成。"
> "It has done everything that we've wanted it to do. It's been reliable and we know the team really well." `[24:30 左右]`

主持人提出了他的疑问：对于他这种"副业项目 vibe coding + 开源"的人来说，他看了 Pier（Pierre），觉得"他们做存储，但他们不做 Actions，不做 CI/CD，而这恰恰是我挣扎的部分。存储东西很简单，存储有什么难的？"

**"编码 SaaS 是最后的 SaaS"**

Quinn 承认存储大部分情况下很简单，然后引出了一个非常深刻的行业判断：

> "你自己构建一个只解决**一个人问题**的自托管的东西，要容易得多，而且可以做得非常健壮。但如果你试图构建多租户（multi-tenancy），复杂度会翻倍。"
> "It's so much easier for you to build something that's going to be self-hosted that just has to solve one person's problem... But if you're trying to build multi-tenency, I mean that doubles the complexity." `[25:40 左右]`

然后他抛出核心论断：

> "这种不对称性，我认为会是现在软件产业里最有趣的主题。但你说得对，归根结底就是：**编码 SaaS 将会是世界上最后的 SaaS，因为所有其他 SaaS 都可以通过编码 SaaS 被构建出来。所以你不如只做编码 SaaS。**"
> "coding SaaS will be the last SaaS in the world because all the other SaaS will just be buildable via coding SaaS. So you might as well just only do coding SaaS." `[26:00 左右]`

主持人半开玩笑地回应："是啊，对我（我们）来说这是美好愿望，但好吧。"但 Quinn 的这个判断其实很严肃：如果智能体可以让任何公司都"编码即服务"地自建内部工具，那么大量的垂直 SaaS 就面临被"自建"替代的风险，而提供"编码能力"本身才是最底层、最不可替代的 SaaS。

---

## 十二、"你为什么还需要 CI？"：一个正在松动的牙齿 `[28:30-31:00]`

**核心观点**
Quinn 提出了一个挑衅性的问题：如果智能体已经跑完测试做自我验证，为什么还需要 CI？他承认自己"像一颗摇摇欲坠的牙"，一半的 AMP 团队已经认为"我们不需要 CI"。主持人的反驳是：你不信任智能体能穷尽地跑完所有测试。

**深度阐述**

Quinn 抛出一个"挑衅线程"：

> "我的智能体知道要跑测试，它跑在一个沙箱环境里，这个环境和团队每个人一样，所以它有 CI 那种很好的可复现环境特性。而我讨厌等待。所以如果我的智能体已经跑了测试做自我验证，我为什么还需要 CI？为什么它不能说'智能体做完了，推到生产吧'？"
> "if my agent has run the tests for its own verification, why do I need CI? Why can't it just say the agent did it now? Let's push it to prod." `[28:40 左右]`

**主持人的反驳：穷尽性**

主持人给出了一个"简单但不太令人满意"的答案：

> "你不信任智能体会做得穷尽。它会跑它上下文里的东西，但如果你有一个大项目，你不知道它是否跑了它应该跑的一切。所以 CI 就是一个确定性的阶段，'嘿，在所有这些测试上跑一遍'。任何反馈、任何失败都会传回给智能体，智能体修复，再回来。像有时你做了一个改动，你不清楚'哦，那碰到了别的东西把它弄坏了'。"
> "you don't trust the agent to be exhaustive." `[29:10 左右]`

**Quinn 的反击：CI 本身就是启发式的**

Quinn 承认这个答案有一定道理，但他给出了一个很聪明的反驳：

> "我再跟你多站在一起三周吧。我就像一颗摇摇欲坠的牙。一半的 AMP 团队在说：'伙计们，我们不需要 CI。我们需要的是打包镜像然后推送部署，但我们不需要 CI。'" `[29:40 左右]`

他提出了两个关键论点：

1. **真正的 CI 已经很启发式了**：任何不必经历极其痛苦的 CI 的人，都已经有了一个只对**变更的文件**跑测试的东西，而这本身就是一种启发式。你通常不会在 CI 里一直跑整个测试套件。

2. **如果让智能体跑全部呢？**：
   > "如果你想让它跑所有东西，那么如果你说'跑全部'，它会相当可靠。然后如果你消除所有 flaky（不稳定）测试——那是一大头痛——如果它能自动修复 flaky，我认为你可能会处于一个更好的位置。"
   > "if you want the agent to run everything, then it's going to be pretty darn reliable if you say run everything." `[30:30 左右]`

主持人表示了有限度的同意，然后表达了一个更宏观的判断：

> "每次有人说'我不信任模型做 X 或 Y'，这都不会持续太久。所以感觉 CI 在我们认知中的日子是有限的。"
> "every time someone has said, oh, I don't trust the model to do X or Y, that doesn't last for that long. So, it just feels like the the days of of CI as we know it are numbered." `[30:50 左右]`

但他也承认一种有趣的悖论：**CI 本质上就是一个可复现的运行环境**——而"像 CI 一样的东西"正在爆发式增长（有些公司每天跑上千个 orb，E2B、Daytona 这些沙箱公司正在暴涨）。所以"CI 这个概念"在爆发，但"CI 作为一种独立阶段"在消亡。

**延伸思考**

这段对话精彩地展示了一个"过渡期认知"的典型特征：Quinn 自己都说"我像一颗摇摇欲坠的牙"——他既没有完全放弃 CI 的直觉，也已经被"智能体自我验证"的逻辑说服了一半。这种**"一半认同、一半怀疑"的中间状态**，恰恰是理解技术过渡期的最佳样本。很多时候，最诚实的人不是"确信未来"的人，而是像 Quinn 这样承认自己"正挂在一颗将落未落的牙上"的人。

**精华收获**

- 判断"CI 是否还有必要"的关键问题不是"要不要跑测试"，而是"谁来跑、跑什么、跑得多穷尽"。
- "CI 作为独立阶段"可能在消亡，但"CI 作为可复现环境"正在爆发——同一个概念的两个层面，命运截然不同。

---

## 十三、沙箱与 E2B：基础设施层的竞争与合作 `[31:00-33:00]`

**核心观点**
AMP 使用 E2B 作为沙箱基础设施，Quinn 高度评价了他们"抓住了沙箱所需原语"的能力，并尖锐批评了一些大云厂商"号称沙箱但缺乏关键能力（如恢复、网络访问）"。

**深度阐述**

主持人问 Quinn 用什么做沙箱，是否自研。Quinn 回答：

> "我们现在用 E2B。他们一直很棒。当我们看其他沙箱公司时，有些看起来也很好。我不觉得我们现在切换会有很大痛苦。"
> "we're using E2B right now. They've been really great." `[31:20 左右]`

他提了一个很实际的诉求：**希望成本能降下来**，因为他们不想让任何人在启动更多 orb 时有任何犹豫。他提到 AMP 现在推出了订阅计划（Megawatt 和 Gigawatt），给了"超级慷慨的 orb 配额"，99.9% 的人根本用不完。但他还是希望更便宜。

**对 E2B 的高度认可，以及对大厂的犀利批评**

> "看到 E2B 这样一家创业公司——我认为他们做得非常好，但它是一家创业公司——如何完全搞定了'沙箱需要哪些原语'，这真的很酷。而我看着其他大云厂商的产品，他们把它叫沙箱，以为在跟 E2B 竞争，但他们**缺乏恢复（resume）能力，或者沙箱没有网络访问**之类的。这很古怪。所以大大称赞 E2B 团队，但这是一个竞争非常激烈的领域了。我大概每周收到三四封邮件说'嘿，我看到你在做沙箱，要不要试试我的东西'。"
> "they like lack the ability to resume or like their sandboxes have no network access... it's just it's bizarre." `[32:00 左右]`

**主持人的补充：专注度决定成败**

主持人给出了一个很到位的补充：

> "我认为这只是取决于你有多认真对待它。它对你是个副业项目，还是你整个公司的存亡都系于成为世界上最好的沙箱公司？"
> "Is it a side project for you or do you is your entire company's existence dependent on being the best sandbox company in the world?" `[32:40 左右]`

他还提醒，人们对沙箱的需求差异很大，这个领域的完整需求还没有被完全探索出来，"人们在构建的过程中发现需求，非常混乱"。他举例说 RL（强化学习）沙箱的需求就完全不同，这解释了为什么有些产品会暴露那些看似古怪的原语。

**延伸思考**

这段对话触及了一个在 AI 基础设施圈反复出现的现象：**大厂"宣布支持"某个能力，和创业公司"真正做好"这个能力，是两回事**。Quinn 的批评——"他们叫它沙箱，但缺乏恢复能力、没有网络访问"——揭示了很多大厂产品只是"命名上对齐"了前沿概念，但在核心原语（primitives）上是缺失的。对于正在选择基础设施的团队来说，这是一个提醒：**不要看产品叫什么，要看它是否解决了你真正需要的原语问题**。

---

## 十四、从 Sourcegraph 到 AMP：一次罕见的创业公司"分拆" `[33:00-37:00]`

**核心观点**
Quinn 的创业历程从 Sourcegraph（代码搜索）开始，后来公司同时拥有两个产品（code search 和 AMP），最终决定分拆：20 人带着 AMP 独立出去，其他人留在 Sourcegraph，所有投资者和员工在两家公司都有股份。这对 Quinn 个人而言，是从"管 200 人的 CEO"回归到"20 人高信任团队"的能量回归。

**深度阐述**

Quinn 完整地讲述了他的创业脉络，这部分对公司组织研究极有价值。

**Sourcegraph 的成绩**

> "我的旅程始于创办 Sourcegraph，那是代码搜索。我们有排名前十的上市科技公司中的九家作为客户，六大银行中的四家，还有 Uber、Stripe 等等。这些公司都在用 Sourcegraph 做代码搜索。我得以看到一家伟大的软件企业是什么样子。"
> "We have like nine of the 10 top public tech companies as customers and like four of the six top banks." `[33:40 左右]`

**一个罕见的决定：公司分拆（spin-off）**

Quinn 说他和董事会、联合创始人 Beyang 一起决定把 Sourcegraph 里的两个产品分拆。他特意指出这种操作有多罕见：

> "这种分拆在创业公司和软件史上，自 2009 年左右 David Sacks 从 Genie 分拆出 Yammer 之后，基本上没怎么发生过。"
> "which has not been done really in like startups and software since David Saxs spun off Yammer from Genie in like 2009 or something." `[34:20 左右]`

他补充了一个有趣的细节：David Sacks 曾是他们的董事会成员，直到他去了白宫。（注：David Sacks 在 2025 年被任命为白宫 AI 与加密货币事务负责人。）

**分拆的具体结构**

- 20 人带着 AMP 向前走，其他所有人留在 Sourcegraph 团队
- 他们"对投资者做了正确的事"：所有投资者、所有员工，在两家公司都持有股份

Quinn 也提到了其他几种可能的路径——比如 Intercom 和 Finn（Intercom 是先有的业务，Finn 是 AI 的那个），他认为有很多种方式可以走通，但对他们来说，分拆是合适的选择。

**为什么分拆是对的**

Quinn 给出了两个原因：

1. **两个业务各自需要专注**：Sourcegraph 的代码搜索，鉴于代码量大幅增加，显然有光明的未来，它需要专注；AMP 也需要专注。

2. **个人层面：他更适合小团队**：
   > "作为 CEO，我热爱在一支 20 人的团队里。相比 200 人的公司……对于我认为自己擅长的东西，我不认为我在担任一家 200 人公司 CEO 时做得那么好。我从 20 人团队里获得更多能量。"
   > "I don't think I was that good or nearly as good at being CEO of 200 person company and I get a lot more energy from that." `[35:30 左右]`

**"信任"是核心**

他把这一点讲透了：

> "现在我有了这支 20 人的团队，每个人在每件事上都可以被信任。我可以完全自在地让团队里的任何一个人去和我们的任何客户交谈、修复任何 bug、做任何事。这太不可思议了。相比几年前，你不再需要去雇佣那些你不信任其高能动性（high agency）或技能的人，因为你可以用智能体来做这些事。而我们完全拥抱了这一点。"
> "you do not have the need to go and hire people that you do not trust... because you can use an agent to do those things." `[36:20 左右]`

**拒绝"旧式"增长**

Quinn 最后表达了对"旧式软件业务扩张方式"的批判：

> "我看到一些和我们规模相近的公司开始雇佣一个 PM 或一个市场人员，这感觉就像旧的构建软件业务的方式。最终会导致 10% 的人在思考如何做出伟大的产品，而其他 90% 的人在思考间接成本。我认为过去这是必要的，但我认为现在不再必要了。"
> "10% of the people are thinking about how to make a great product and the other 90% are thinking about the overhead... I don't think that's necessary anymore." `[37:00 左右]`

**个人感受**

这是全篇最有人情味、也最能体现 Quinn 价值观的一段。他的核心论点其实不是"小团队更省钱"，而是"**小团队 + 智能体 = 不需要雇佣你不完全信任的人**"。这背后是一种对"人的质量"的执着：与其扩张到需要管理大量你不完全信任的人，不如用智能体补足那些原本需要招人的能力。对他个人来说，这是一种能量的回归——从大公司的重行政管理，回到小团队的全情投入。

**延伸思考**

"10% 的人做产品、90% 的人做 overhead"这个描述，戳中了很多大公司的病。AI 时代的小团队模式提出了一个问题：**公司规模的经济学是否在改变？** 传统上，规模意味着更低的单位成本、更强的市场能力，但也意味着更多的协调开销。如果智能体能承担大量 coordination 和 overhead 工作，那么"小而全"可能重新成为最优解——这也许解释了为什么 Jeff Dean 离开 Google、选择"几个人在一个房间里"（访谈后段提到的新闻）。

---

## 十五、内部智能体、"果冻软件"与"新的开源" `[37:00-42:00]`

**核心观点**
Quinn 团队正在用智能体承担原本需要招人的职能（如市场营销）。他提出了"果冻软件（jellyware）"这个概念，以及"新的开源"——不是开源一个库，而是开源一些 markdown 文件加示例代码。

**深度阐述**

主持人问 Quinn 是否有"事实上充当市场人员、产品人员"的内部智能体。Quinn 回答说他们把一切都放在 AMP 里做——AMP 始于一个编码智能体，但"你不能把一个智能体关在一个贴着别的标签的盒子里，它现在就只是一个智能体"。

**"营销智能体"是什么？**

> "营销智能体是什么意思？一部分是构思点子并实现这些东西，另一部分是营销自动化之类。那是我们还没有的部分，但那是我们接下来想构建的众多应用之一。"
> "what does a marketing agent mean? Part of with the ideas and implementing the things and part of it is like the marketing automation... that's one of the next like many apps that we want to build." `[38:00 左右]`

**"果冻软件（jellyware）"**

Quinn 解释了他们的发布理念：他们构建的很多东西是 AMP 特有的，但如果做出真正好的通用东西——比如"监控网上（X、Discord、邮件）所有关于我们的讨论，让我们容易回应，并识别出合适的社区倡导者"——那其实相当通用，应该放出去。

他对比了两种旧模式：

- **旧的**：做一个开源项目，然后头疼地陷入开源维护
- **另一种旧的**：做设置和集成，然后卖钱

而新的方式是：

> "现在如果我们能把代码放出去，让任何其他人可以用他们自己的智能体来 remix（混编）和定制，那可能会相当有价值。所以我们会试试。我们会发布很多这样的小东西，我们叫它 **jellyware（果冻软件）**。它比软件更软，但不完全是 vibe coded（氛围编程），你可以用你自己的智能体来定制它。"
> "it's like softer than software but it's not totally vibe coded and you can customize it with your own agent... jellyware is what we're calling it." `[39:00 左右]`

主持人评价："它令人印象深刻。这正是你想要的。"并调侃"果冻软件"这个名字"有点太美味了，但任何能被记住的东西都是好的"。

**主持人的亲身经验：Codeex 当 CMO**

主持人分享了他自己的实践：

> "值得一提的是，Codeex 在过去大约 2 个月里一直是我的 CMO，基本上在运营我们的广告，并给我关于 AEO 和 SEO 的建议。我发现这比我与真正的人类顾问交谈更可取——我也做过后者。而且结果大致相同。我不知道这对 CMO 或 fractional CMO（兼职 CMO）咨询行业意味着什么，因为反正没人知道任何事。所以你不妨直接做大家都同意是真的那些事，不需要一个人类替你做。"
> "Codeex has been my CMO for the last like 2 months... I find it much more preferable to talking to a real human consultant... it's roughly the same results." `[40:00 左右]`

**"新的开源"**

Quinn 建议感兴趣的人去看他发布的"skills"（技能）——这基本上是他现在 GitHub 使用的主体。他提到他正准备把它迁移到 Forge（他的 GitHub 克隆），但目前还在 GitHub 上。

> "这是我在工作中使用的一切，包括市场营销，包括 AI devrel（最新的东西）。所以 Forge 的工程博客不是人类写的，但由我策展。我给它一些方向，它就写出整个东西。"
> "forg's engineering blog is not written by humans but it is curated by me." `[41:00 左右]`

他描述了具体流程：即使是图形也都是生成的，他大体上在文字稿里读一遍，说"这是个很酷的工程故事，请把它写出来"，然后给一些关于最终目标的指导，就这样。

> "我认为那可能**是新的开源**——你开源一些 markdown 文件和一些示例代码。我确实试着做得比 markdown 文件更多一点，但它真的意味着这是可移植到你想要的任何项目的，而在这个时候这可能比一个库更有价值。"
> "this is probably the new open source, which is you open source some markdown files with some sample code... that's probably more valuable than a library at this point." `[41:40 左右]`

**延伸思考**

"技能即开源（skills as the new open source）"和"果冻软件"这两个概念，指向一个更深层的转变：**在 AI 时代，可复用性的单位从"代码库"变成了"提示词 + 示例 + 可定制的工作流"**。一个库（library）需要你理解它的 API、集成它、处理它的依赖；而一套"技能"只需要你把它喂给你的智能体，让它 adapt 到你的场景。这可能确实是一种更轻、更可移植、更易扩散的复用方式。

---

## 十六、AI 视频编辑：一个"反共识"的选择 `[42:00-46:00]`

**核心观点**
在一片"用 AI 做视频编辑"的浪潮中，Quinn 是少数坚持"人类编辑足够便宜且足够好"的人。他做了成本对比：在 600 万美元的 AV 预算面前，几万美元的人类编辑成本不是问题。

**深度阐述**

主持人问 Quinn 如何用 AI 做视频编辑和剪辑。Quinn 的回答出人意料地"传统"：

- 他们不怎么剪片段（clips），因为做长视频（AIE 是 20 分钟到 3 小时，Latent Space 是 30–60 分钟）
- 他们试图深度、少标题党
- 人们试过用 Quad Code 剪片段、用 Hyperframes 做生成视觉的拼接，但他没怎么实验

**试过的工具**

> "我们试过 Overclip，我想那是 A16Z 投资的做剪辑的公司。不是很好。我们即将为纽约的 AIE 试另一个——Star Zero，它专注金融服务。那个看起来更有希望，但我还没试。"
> "We tried Overclip I think is the A16Z-backed company that does clipping. It wasn't very good." `[43:30 左右]`

他诚实地说，这只是"我是否优先做它"的问题，没有对技术是否成熟做评判。

**为什么坚持人类编辑？**

> "我认为编辑，人类编辑，仍然足够便宜，不成问题。它便宜且足够好，不是问题。而且我更愿意能够在一次编辑中说'嘿 Alejandro，记得做这个'，我知道 Alejandro 会接住它，因为我们已经有两年了的工作关系，我不需要去搞清楚 Quad 怎么做。"
> "human editing is still cheap enough where it's not a problem... I know Alejandro will pick it up and because we've had that working relationship for two years now." `[44:00 左右]`

**成本对比**

主持人称他是"这方面的顶级掠食者"（apex predator），因为"你是唯一一个告诉我你认为视频编辑由人类做足够好且便宜的人"。Quinn 给出了他的账本：

> "我经营一个媒体业务，我们制作高质量、高价值的视频。所以我不需要把制作成本降那么多。其他人（做视频）是副业，预算只有几百美元。但比如我的 AIE 预算，今年我在 AV 上花了约 600 万美元。那几万美元（的人类编辑成本）算什么？"
> "my AIE budget, I spent like $6 million on AV this year. What's a few tens of thousands?" `[45:00 左右]`

**延伸思考**

Quinn 这个选择提供了一个重要的反共识视角：**AI 替代的经济学是场景相关的，取决于你的成本结构和质量要求**。对于一个 AV 预算 600 万美元、追求高质量长视频的媒体业务，几万美元的人类编辑成本是可以忽略的，而 AI 编辑的体验和结果还不足以弥补与人类编辑长期协作关系的价值。这提醒我们，不要盲目追随"AI 替代一切"的浪潮——**先算清你自己的成本账和质量门槛**，再决定哪些环节该用 AI、哪些该保留人类。

**精华收获**

- AI 替代的决策，本质上是一道成本-质量的场景题：你的成本结构决定了 AI 的性价比。
- 长期的人机协作关系本身是一种价值——"我知道 Alejandro 会接住它"这种默契，是 AI 暂时难以替代的。

---

## 十七、收尾思考：小团队、Jeff Dean 与"我们正生活在 AGI 中" `[46:00-结束]`

**核心观点**
Quinn 的"离开大公司、组建小规模高信任团队"的模式，与 Jeff Dean 离开 Google（意图"几个人在一个房间里"）形成呼应。主持人的收尾判断是："时间线在缩短，我们正生活在 AGI 中。"

**深度阐述**

主持人在收尾时，把 Quinn 的模式上升到了一个更大的主题：创始人和人们是否应该离开大公司，去组建一支小规模的"特种部队（SWAT team）"，去追求他们认为重要和伟大的事。

> "我认为你（Quinn）的结果说明了这一点。我也认为你提到'你在盈利'很重要。"
> "I think you're having results. I think it's also important that you mentioned you're profitable." `[46:30 左右]`

**Jeff Dean 的离开**

主持人提到了一个重磅新闻：

> "Jeff Dean 刚刚离开了 Google。这不是我从来会想到自己会说的事。据我们所知，他意图是五个人在一个房间里工作。他离开 Google 时的使命宣言是：'一小群人能做到什么，而不是像成千上万人那样？'而他写下这句话，肯定是对 Gemini（有成千上万人在做）的挖苦。"
> "Jeff Dean just left Google... his mission statement when he left Google was like, what could a small handful of people do as opposed to like thousands of people?" `[47:00 左右]`

主持人提出了一个开放性问题：这会不会意味着"领域专业知识"没有空间了？"规模化多个人"没有空间了？他认为"人们现在如何运营公司"是一个完全开放的问题。

Quinn 的回应很简单：

> "感觉没人知道，我们都会弄清楚。这就是为什么最好的位置就是出去构建。"
> "It feels like nobody knows and we're all going to figure it out. That's why, you know, best place to be is just getting out there and building." `[47:40 左右]`

**另一个案例：Airtable 的 Howie**

主持人还提到了 Airtable 的 Howie Liu，说他实际上用 Hyper Agents 做了类似的事，只是没有那么多并行——他基本上是已经卖掉了公司，然后在一段时间里"双职"（double heading）。

**收尾**

> "这是一个勇敢的新世界。时间线在缩短。我们正生活在 AGI 中，谢谢你公开构建（building in public）。"
> "It's a brave new world. Timelines are shortening. We're living in AGI and uh thank you for building in public." `[48:00 左右]`

Quinn 简短回应："谢谢。聊得很好。"

**个人感受**

这场访谈的收尾有一种奇特的"时代感"。主持人用"我们正生活在 AGI 中"作为结束（半开玩笑、半认真），呼应了整场对话的核心感受：**变革的速度已经快到让"未来"变成了"现在"**。Jeff Dean 离开 Google 想要"几个人在一个房间里工作"，和 Quinn 从 200 人公司 CEO 回归到 20 人团队，这两个故事看起来完全不同，但它们指向同一个方向——**在 AI 时代，小规模、高信任、高能动性的团队，可能是最具杠杆效应的组织形式**。

**延伸思考**

"我们正生活在 AGI 中"这句话（原文是 swyx 的惯用梗，可能半开玩笑），配合前面的所有具体案例，构成了一个耐人寻味的观察：AGI 到来与否可能有争议，但"AI 已经在深刻改变软件公司怎么运转"这件事已经发生了。Quinn 描述的 orbs、智能体自动化运维、取消代码审查、不用 GitHub、用智能体当 CMO——这些不是未来的预言，而是他和他的客户此刻正在做的事。**真正的"未来"，往往不是某一天突然降临，而是在少数人的现在里，已经悄然发生。**

**精华收获**

- **小团队 + 高信任 + 高能动性**，可能是 AI 时代最具杠杆的组织形式。Jeff Dean 和 Quinn 都在往这个方向走。
- "最好的位置就是出去构建"——在一个没人知道答案的时代，行动本身比预测更有价值。
- 如果你想知道六个月后你的团队怎么工作，去看看像 AMP 这样已经"提前活在六个月后"的团队。

---

## 全文总结：这场对话真正在说什么

如果把这场近一小时的对谈压缩成一个核心命题，它大概是：**当 AI 智能体从"辅助编码"进化到"可以并行运行、自主运维、自我验证、并且更安全"时，软件公司的组织形态、工具链、产品策略和安全模型都必须被重新设计——而这套重新设计的核心，不是更强的 AI，而是更高的信任。**

Quinn Slack 和 AMP 团队给出的，不是一个"用 AI 提效"的平庸故事，而是一个**自洽的、系统性的新范式**：

| 维度 | 旧范式 | AMP 的新范式 |
|---|---|---|
| 开发环境 | 本地开发，一切在笔记本上 | orbs 云端远程，本地开发已死 |
| 代码质量 | 强制代码审查，MTBF 优先 | 取消审查，MTTR 优先（分钟级修复） |
| 组织信任 | 靠流程把关，雇佣大量不完全信任的人 | 靠招对人，20 人全员高信任 |
| 软件使用 | 设置界面 + 集成 + MCP | 智能体是终极设置界面，代码是终极设置界面 |
| 代码托管 | GitHub（issues/PR/Actions） | AMP 托管仓库，不用 issues/PR |
| CI | 独立的确定性测试阶段 | 智能体自我验证，CI 日子有限 |
| 安全 | 本地智能体拥有开发者全部权限 | 云端沙箱 + OIDC 限时只读访问 |
| 软件复用 | 开源库 / 卖设置和集成 | "新的开源"：markdown + 示例 + 可定制技能 |
| 软件交付 | 买现成 SaaS | "编码 SaaS 是最后的 SaaS" |

这套范式里最反直觉、也最值得记住的三个判断是：

1. **"把用户留在旧做法上的价值是负的"**——在快速技术周期中，逼用户前进比保兼容更重要。
2. **"最重要的系统是拥有一支真正被信任的团队"**——取消代码审查的前提不是 AI 强，而是团队值得信任。
3. **"云端智能体比本地智能体更安全"**——最小权限 + 限时 + 只读，才是正确的安全模型。

而这一切最终指向主持人那句收尾：**"时间线在缩短，我们正生活在 AGI 中。"** 无论这句话有多少玩笑成分，Quinn Slack 和他的 20 人团队用一整个产品、一整个客户群、一整套基础设施，证明了它至少有一半是真的。

---

*（本文基于 Latent Space 播客访谈字幕重构，所有观点、数据和引述均来自原始对话；部分时间戳为根据内容逻辑估算，用于辅助定位，非严格精确。）*

<!-- TLDR: 小团队+高信任+云端智能体，正在让代码审查、本地开发和 GitHub 悄然死去。 -->
<!-- TAGS: AI编程, 智能体, 工程管理, 云端开发, 创业组织 -->
<!-- RATING: 5 -->
