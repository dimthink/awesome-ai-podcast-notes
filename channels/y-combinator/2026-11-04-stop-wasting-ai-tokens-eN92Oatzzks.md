---
title: "Stop Wasting AI Tokens"
channel: "Y Combinator"
published: "2026-11-04"
source_url: "https://www.youtube.com/watch?v=eN92Oatzzks"
video_id: "eN92Oatzzks"
tags: ["AI编码", "模型路由", "软件工程", "Weave Router", "工程生产力"]
rating: 4
language: "英文"
word_count: 40722
duration: "28:37"
---

# Stop Wasting AI Tokens

- **Channel:** Y Combinator
- **Published:** 2026-11-04
- **Source:** https://www.youtube.com/watch?v=eN92Oatzzks
- **TL;DR:** AI 编码的核心从写码转向路由——选对模型、优化并行化、确保质量，才能在 token 经济中胜出。
- **Tags:** AI编码, 模型路由, 软件工程, Weave Router, 工程生产力
- **Rating:** 4

## 版本

- [结构化文稿](2026-11-04-stop-wasting-ai-tokens-eN92Oatzzks.structured.md)
- [原始文稿](2026-11-04-stop-wasting-ai-tokens-eN92Oatzzks.transcript.md)

# Stop Wasting AI Tokens：从模型路由到软件工厂——AI 编码的下一场革命

## 材料信息

- **标题**：Stop Wasting AI Tokens
- **作者/来源**：Y Combinator（YC 官方频道访谈节目）
- **类型**：YouTube 视频字幕（访谈对话形式）
- **关键元数据**：访谈嘉宾为 Weave 公司联合创始人（Andrew 及另一位联合创始人），YC Winter 2025 批次项目；视频主题围绕 Weave Router 新品发布、AI 编码代理优化、软件工厂构建方法论；公司近期完成由 Sander Capital 等机构参与的 Series A 融资

---

## 开篇引入

想象一下，你每个月花 200 美元订阅 Anthropic 的 Claude 计划，又花 200 美元订阅 OpenAI 的计划，然后你发现自己仍然频繁撞上使用限额——这种挫败感几乎是每一个"重度 AI 编码用户"的共同体验。你不得不在不同模型之间手动切换：这个任务用 Opus，那个任务用 DeepSeek，再换一个用 GLM……每个模型都有自己的脾气、自己的擅长领域、自己的成本曲线。你变成了一个"人工路由器"，在模型的海洋里疲于奔命。

但如果有这么一层智能，它能像一位深谙每个模型脾气的老工程师一样，自动把你的每一个 prompt 送到最合适的模型那里——既能保持顶尖的编码质量，又能让你的订阅额度翻倍使用，甚至还能把成本砍半——你会不会觉得这才是 AI 编码该有的样子？

这就是 Weave 正在做的事情。作为从 YC Winter 2025 批次走出来的明星项目，Weave 最初做的事情是"测量工程师的工作"——这是一个曾经被认为几乎不可能完成的任务。而在 AI 编码爆炸式增长的 2025 年，他们意外地发现，他们积累的能力恰好可以解决一个更大的问题：如何让每一个 AI token 都花在刀刃上。

这场对话发生在 Weave 完成 Series A 融资并发布新产品 Weave Router 的时间节点。它不仅仅是关于一个产品的发布，更是关于 AI 编码正在经历的一场深刻转变：从"拼谁用的模型最贵"到"拼谁的路由最聪明"，从"人类工程师写代码"到"人类工程师调度 AI 集群写代码"。如果你对 AI 编码的未来感到好奇，这场对话提供了来自最前沿的观察。

---


## 一、Weave 是什么：从"测量工程"到"优化人机协作"

### 核心观点
Weave 的定位是"把任何软件公司变成软件工厂"——通过构建模型来测量工程工作，进而优化人类工程师与 AI 代理的协作方式。

### 深度阐述

Weave 的联合创始人（以下称 Andrew 和他的合伙人）在访谈开场就给出了一个极具野心的定义："Weave 是一个将任何软件公司转变为软件工厂的工具。"*（"So Weave is a tool to turn any software company into a software factory."）* 这句话背后隐含着一个关键信念：软件开发正在从一种"手艺活"变成一种"制造流程"，而制造流程的核心特征就是可测量、可优化、可规模化。

要理解 Weave 的独特之处，需要回到一个看似朴素的问题：**软件工程的工作到底怎么被测量？** 在工业制造领域，你可以数一数生产了多少个零件、检查次品率、计算单位成本。但在软件工程领域，长久以来人们只能依赖一些极其粗糙的替代指标——代码行数、PR 数量、Door Metrics（一种基于代码评审的度量体系）。Andrew 在访谈中毫不客气地评价这些指标："这些都是非常花哨的指标，试图让高管们感觉良好。" *（"Lines of code or number of PRs. PRs, door metrics, like these are all very fancy kind of metrics to try to make executives feel good."）*

这些指标的问题在于：一个工程师可能写了 500 行代码却解决了一个极其简单的问题；另一个工程师可能只改了 3 行代码就修复了一个严重的生产事故。代码行数完全无法反映工作的真实价值和复杂度。更糟糕的是，当一个团队用这些指标来做决策时，他们实际上是在激励工程师写出更多冗长、重复的代码，而不是写出更优雅、更高效的解决方案。

Weave 的突破在于，他们利用 LLM 来"阅读"代码，真正理解代码在做什么、改了什么、影响是什么，从而构建出比代码行数精确得多的度量模型。这本质上是用 AI 来理解 AI 时代之前无法量化的工程工作。用 YC 合伙人在访谈中的话来说："这是历史上第一次，我们有可能真正理解工程师的工作——他们有多高产，他们制造了多少 bug。" *（"This was historically like impossible to do to actually understand the work that engineers do, how productive they are, how many bugs they're creating."）*

### 个人感受
访谈中能明显感受到，Weave 团队对于"代码行数"这类传统指标有一种几乎是不屑的态度。这种情绪其实在工程文化中有着深厚的根基——优秀的工程师常常讽刺"用代码行数衡量生产力"就像"用重量衡量飞机的质量"。当 Andrew 用那种近乎嘲弄的语气说出"让高管们感觉良好"时，你能感觉到他们的产品使命里带着一种为工程师正名的热情。

### 延伸思考
这里有一个有趣的悖论：在过去，测量工程师的工作是"不可能的任务"，因为代码的语义信息过于复杂。但恰恰是 LLM 的出现，让这种测量成为可能。换句话说，**AI 不仅改变了工程师写代码的方式，也改变了我们理解工程师工作的方式**。这种"测量能力"的跃迁，本身就是 AI 带来的二阶效应——它影响的不仅是生产力本身，还有我们对生产力的认知框架。

### 精华收获
- 传统工程度量指标（代码行数、PR 数量）本质上是"认知错觉"，它们让管理者以为自己掌握了情况，实际上可能误导决策
- AI 的核心价值之一，是让之前无法量化的复杂工作变得可观测、可度量
- Weave 的战略定位在于抓住了一个根本性的转变：当代码由 AI 生成时，"测量工程"和"优化 AI 代理"变成了同一件事


## 二、从测量人类到测量 AI 代理：Weave 的转折点

### 核心观点
Weave 最初的业务是测量人类工程师的工作表现，但 2025 年 AI 编码的爆发让他们发现，同样的技术可以直接应用于编码代理的测量与优化，这成为了公司增长爆发的关键引擎。

### 深度阐述

2025 年初，Weave 进入 YC Winter 25 批次。当时他们的产品聚焦于"理解和测量工程工作"。但就在这个时间窗口，一件改变一切的事情发生了：**Cursor 开始爆发**。YC 合伙人在对话中回忆道："这是第一个批次，我们调查了批次中的公司，有相当数量的人说他们的大部分代码是由 LLM 而不是人类写的。" *（"It was the first batch where we surveyed the batch and a significant number of people said that most of their code was being written by LLMs instead of by humans."）* 这条推文当时在 Twitter 上引发了巨大的争议——"什么？他们在做什么？" *（"What? They're doing what?"）*

这场争议本身就是一个时代转折的标志。在 2025 年初，"AI 写代码"还是一件让不少传统工程师感到愤怒甚至觉得"不道德"的事情。但 Weave 团队和 YC 从中看到的是完全不同的东西：如果代码现在是由 AI 写的，那么"测量工程工作"就不再只是测量人类了——你需要测量 AI 代理。

Andrew 描述了这种需求的出现过程："在批次期间，我们很快意识到，这是第一个 Cursor 开始起飞的批次。人们第一次用 Cursor 写他们所有的代码。人们开始要求我们展示 Cursor 对他们的生产力产生了什么影响。" *（"During the batch what we realized very quickly it was the first batch where Cursor was just starting to take off. People were writing all of their code with Cursor for the first time and people started asking us to show us what is the impact that Cursor is having on their productivity."）*

这段话揭示了一个非常关键的商业洞察：**当工具链发生剧变时，测量和优化的需求总是首先出现在最前沿的采用者群体中**。那些在 YC 批次中的早期创业公司，恰恰是第一批大规模使用编码代理的人群。他们比大公司更早地遇到了"AI 写代码效率如何"这个问题，而 Weave 就在那里，用他们的测量能力精准地接住了这个需求。

YC 合伙人在对话中进一步点出了两个同时发生的转变："第一件事是由 AI 引起的——这是第一次有可能测量人类表现，因为你们不只是数代码行数。你们会让 AI 模型去看代码，真正读懂代码，理解那个人实际在做什么……与此同时，那些让你们做到这一点的 LLM，也在改变工程师们写代码的方式。" *（"The first thing that was happening caused by AI was for the first time it was possible to measure human performance... And at the same time the same LLMs that enabled you to do that were also changing the way that those engineers were writing code."）*

这段话值得反复咀嚼。它揭示了一个极不寻常的历史巧合：**AI 既是测量工具的提供者，又是被测量对象本身的创造者**。Weave 用来理解代码的 LLM，和生成代码的 LLM，是同一种技术。这意味着 Weave 的测量能力天然地可以"平移"——昨天你用它来理解人类写的代码，今天你就可以用它来理解 AI 写的代码。这种技术上的连续性，是很多竞争对手无法复制的。

### 个人感受
访谈中 Andrew 说"回到 2025 年 1 月，感觉像是几个世纪以前" *（"Back in all the way January 25 feels like worlds ago."）* 这句话里有一种不易察觉的沧桑感。18 个月的时间，对于一个身处技术风暴中心的创始团队来说，足以让人感觉像经历了整整一个时代。这种感受对于那些亲身经历了 Cursor 爆发、Claude Code 发布、GPT-4 到 o1 再到 Claude Opus、Astra 等模型不断迭代的人来说，是共同的。技术的演进速度让"几个月前"的经验都可能在今天变得过时。

### 延伸思考
一个值得深思的历史类比：当商业互联网在 1990 年代中期开始普及时，首先受益的公司是那些提供"测量工具"的——比如分析网站流量、测量广告效果的工具。因为当一个新的范式出现时，人们最迫切的需求就是理解"这到底有没有用"。Weave 在 AI 编码时代扮演的，正是类似的角色。但不同的是，互联网时代的测量工具是确定性的（计数、追踪转化），而 AI 时代的测量工具本身就需要 AI——这使竞争壁垒更高，因为你需要持续迭代你的测量模型来追上被测量对象的进化速度。

### 精华收获
- 技术基础设施的变化（如 Cursor 的兴起）会创造新的"可测量性缺口"，填补这个缺口就能找到产品的市场契合点
- Weave 的竞争优势在于：他们用 LLM 来测量和理解代码，而代码现在由 LLM 生成，所以他们的技术栈天然适配于 AI 时代
- 2025 年初的"AI 写代码"争议现在看来像是一个历史奇点——在那之后，关于"AI 写代码是否正当"的辩论迅速消解，变成了"AI 写代码如何做得更好"


## 三、Weave Router：把每个任务路由到最适合的模型

### 核心观点
Weave Router 是一个智能模型路由系统，它通过训练有素的路由模型，自动为每个编码任务选择最优的模型——在保持 Astra 级别性能的同时，实现成本减半、速度翻倍。

### 深度阐述

如果说 Weave 的"测量层"是公司的护城河，那么 Weave Router 就是他们推出的第一把由这条护城河支撑的利剑。Andrew 如此解释 Router 的核心逻辑："Weave Router 做的是把每个任务送到最适合那个任务的模型那里。你把它接入你的编码代理，所有请求都经过路由器。路由器为每一个独立的 prompt 或任务决定使用哪个模型，然后把请求路由到那个模型。" *（"What Weave Router does is it sends every task to the best model for that task. You plug it into your coding agent, it sends everything to the router. The router decides the best model for any individual prompt or task to go to and it routes it to that model."）*

这意味着用户不需要再手动思考"这个该用 Opus 吗？该用 Astra 吗？该用 DeepSeek 吗？" *（"So you don't have to think about should this go to Opus? Should this go to Astra? Should this go to DeepSeek? It all is handled for you."）* 所有的模型选择决策都被自动化了。

但这里有一个必然会被问到的问题：**我怎么知道你不会把任务路由到一个更差的模型上？** 在访谈中，YC 的采访者几乎毫不犹豫地问出了这个问题："Yeah, that's a great question. it to like a dumb model that's just going to like write bugs."（"它会不会把任务路由到一个比较蠢的模型，然后写出一堆 bug？"）

Andrew 的回答从数据出发，而非从直觉出发："这是我们最大的潜在问题之一。但我们有一个有趣的能力来确保这不是正在发生的事——因为我们的整个产品都专注于理解工程团队如何工作，以及理解速度和质量两个方面。" *（"This is, you know, our entire products is focused on understanding how engineering teams are working and understanding both the velocity and the quality."）* 他接着用 Weave 自己的团队作为证据："我们所有人都在使用路由器，我们的产出持续加速。基于我们自己的数据，我们在所有团队中处于前 1%，而且我们引入的 bug 数量没有增加。" *（"We're all using the router and our output only continues to accelerate. We're in the top 1% of all teams based on our own data and there's no increase in the amount of bugs we're introducing."）*

这段话的重要性在于，它将 Weave 的产品逻辑闭环了：**Weave 用它的测量能力来证明 Weave Router 的有效性**。如果你相信 Weave 的度量系统是准确的，那么你就应该相信他们的路由器确实不会降低质量——因为他们自己就在用，而且用数据证明了这一点。

在性能数据上，Andrew 给出了一个极具冲击力的说法："在最近的基准测试中，我们能够以一半的成本和两倍的速度达到 Astra 级别的表现。" *（"On recent benchmarks we're able to hit astro level performance at half the cost and twice the speed."）* 这几乎是一个在商业上不可能被拒绝的提案：同样的性能，一半的价格，两倍的产出速度。

**集成方式**方面，Router 支持所有在 CLI 环境下工作的编码代理："Claude Code、Codex、Open Code、Py……基本上任何你在 CLI 里工作的东西，你都可以通过一条命令直接接入。" *（"Claude code, Codex, Open Code, Py, really anything where you're working in the CLI you can plug it directly in with one command."）* Router 还是完全开源的，"任何人都可以去尝试" *（"Anyone can go and try it out."）*，同时提供托管版本和自托管选项，以及 Max 和 Boost 订阅计划。

### 个人感受
访谈中有个细节很值得玩味。当被问到"我怎么知道它不会让我的编码代理变得更糟"时，Andrew 的回答不是给出一个技术性的解释，而是先承认"这是一个非常好的问题，这也是做这件事最大的潜在问题之一"。这种不回避核心质疑的态度，在创始人访谈中并不常见。大多数创始人会在这种时刻给出一个听起来很光鲜的答案，而 Andrew 选择的是把这个问题当成他们产品存在的基础来认真对待。这种诚实建立了一种信任感——他们在做这个路由器之前，先想清楚了"路由器做错了怎么办"这个问题。

### 延伸思考
模型路由本质上是一个**信息不对称问题**。用户知道自己的任务需要什么，但往往不知道哪个模型最适合；模型提供方知道自己的模型擅长什么，但不知道用户的具体任务。路由器的价值就在于弥合这个信息差。但更深层的问题是：**随着模型能力的趋同，路由的价值会减小吗？** Weave 的回答显然是否定的——因为在他们看来，模型之间的能力差异不会消失，而只会变得更加细粒化。一个模型可能在"理解大型代码库结构"上更强，另一个可能在"生成简洁的 CRUD 代码"上更高效。这些差异对于普通用户来说几乎不可能手动追踪，但对于一个持续学习的路由模型来说，正是发挥价值的空间。

### 精华收获
- 智能路由的核心逻辑：不是"选择一个最佳模型"，而是"为每个任务选择最适合的模型"
- 产品自我验证的重要性：Weave 用自己的测量产品来验证自己的路由产品，这比任何外部背书都更有说服力
- 关键性能指标：Astra 级别的性能，一半的成本，两倍的速度——这三个数字构成了 Weave Router 的核心价值主张
- 开源策略降低了用户的尝试门槛，这在"模型路由"这种需要信任的品类中非常重要


## 四、订阅计划优化：如何最大化"补贴红利"

### 核心观点
对于已经在使用 Anthropic 和 OpenAI 的 200 美元订阅计划的重度用户，Weave Router 可以在保持输出质量的前提下，让同样的花费"走两倍远"，通过智能地在不同订阅账户之间、以及订阅额度与开源模型之间进行分配。

### 深度阐述

访谈中有一段非常实战性的对话，涉及一个每个重度 AI 用户都关心的问题：**我已经付了每个月 200 美元给 Anthropic 和 OpenAI，我已经用满了这两个计划，我现在想更进一步——用 Weave 到底能帮我省多少？**

Andrew 的回答非常直接："首先，你在那些计划上花同样的钱，你能走两倍远。" *（"First of all, for the same amount that you're spending on those plans, you'll go like twice as far."）* 然后他解释了这个节省的核心逻辑："如果你是这样的人，你可能会把一切都发给最大的模型之一。这可以理解——如果全都是补贴的，你不如就追求最聪明的那个。但问题是，你不需要总是用火箭筒，有时候手枪就够了。" *（"The thing is, you know, you don't always need a bazooka where a handgun will do."）*——这句"火箭筒vs手枪"的比喻是整个访谈中最引人注目的金句之一。

他举了一个具体的例子："比如你在探索一个代码库，你只需要一个轻量级的模型来搞清楚——哦，这里是这个代码库中实现认证（auth）的地方。那个子代理或者这部分对话会转到一个更便宜的模型。这完全不影响你。你在一天结束时还是得到同样的结果，甚至更快。但它消耗的额度更少。" *（"For example, you're exploring a codebase, you only need like Luna in order to figure out like, oh, this is where auth is implemented in this codebase. And so that sub agent or this portion of the conversation will go off to that cheaper model."）*

这里引出的一个重要概念是：**子代理级别的路由**。在一段复杂的编码对话中，有些子任务极其简单——比如"找到认证逻辑在哪里"——这种任务用一个轻量级模型就能做得很好，根本不需要动用 Opus 或 Astra 级别的模型。Weave Router 能识别这种差异，将重资源消耗的打探任务分配给轻量模型，将真正困难的推理任务留给顶尖模型。

还有一个非常实用的功能：Router 可以在多个订阅账户之间智能切换。"你可以用多个不同的账户登录，然后我们在这些不同的订阅之间路由，利用所有的补贴，同时在那些即使有补贴也值得使用开源模型的场景中，掺入开源模型来获得最佳性能。" *（"You can log in with a bunch of different accounts and we'll route between those different subscriptions using all the subsidy while we can and then sprinkling in open source models where it's going to be the best performance even with the subsidy."）*

这听起来可能有些"灰色地带"——在多个订阅账户之间分配使用，最大化补贴额度。但 Andrew 的态度相当坦然："这是一个巨大的事情，我认为大量尤其是早期创业公司都非常热衷于最大化这些补贴。趁能用就用。" *（"This is a huge thing that I think like a ton of especially like early stage startups are really into maximizing these subsidies. You know, use it while you can."）* 这反映了一种非常务实的创业心态：当前的 200 美元/月订阅计划所提供的"无限使用"（实际上是有速率限制的）本质上是一种市场教育期的补贴，聪明的用户应该尽可能充分地利用它们。

### 个人感受
"你不需要总是用火箭筒，有时候手枪就够了"*（"You don't always need a bazooka where a handgun will do."）* 这句话之所以有力量，不仅仅是因为它的比喻生动。更深层的原因是，它点出了 AI 编码中的一个普遍心理：因为模型订阅计划是"包月"的，边际成本看起来是零，于是人们倾向于把最贵、最聪明的模型用在所有事情上，好像在享受"被补贴的奢侈"。但问题在于，这会加速撞上速率限制，导致在真正需要顶尖模型能力的时候——比如解决一个复杂的并发问题、设计一个精巧的架构——反而没有额度可用了。好的路由策略不是"省着用"，而是"该用到刀刃上时就该用，不该用到的地方就果断降级"。这是一种反直觉的资源管理智慧。

### 延伸思考
这里其实涉及到一个更深层的问题：**当工具的边际成本看起来为零时，人们会做出什么行为？** 包月订阅的商业模式创造了一种"感知免费"的心理，这通常会导致过度消费。但在 AI 编码的场景下，"过度消费"的代价不是钱包缩水，而是在关键时刻失去工具的使用权——因为速率限制是隐性的、不确定的。Weave Router 的市场定位恰好建立在这种"隐性稀缺"之上：它帮助用户在一个看似无限但实际受限的资源池中做出最优分配。这也解释了为什么它的核心用户群是"token maxers"——那些已经用满了所有订阅额度、依然觉得不够用的人。

### 精华收获
- "火箭筒 vs 手枪"原则：不要把最强大的模型浪费在琐碎任务上，绝大多数简单任务轻量模型一样能做
- 智能路由可以在不降低输出的前提下，有效规避速率限制，让同样的订阅费"走两倍远"
- 在多账户之间分配使用、最大化补贴窗口期，是早期创业公司的一种理性生存策略
- Router 的核心价值不在于"用最便宜的模型"，而在于"在不牺牲质量的前提下，把简单任务和复杂任务分配给正确层级的模型"


## 五、开源模型的崛起：为什么 DeepSeek、Kimi 和 GLM 不可忽视

### 核心观点
开源模型虽然尚未追平最前沿的闭源模型，但在成本性能比上具有无可匹敌的优势。对于大量"足够简单"的编码任务，开源模型完全可以胜任，甚至做得比用户预期的更好。

### 深度阐述

Weave Router 之所以能实现"一半成本、两倍速度"，很大程度上是因为它将大量中低复杂度任务路由到了开源模型上。Andrew 对开源模型生态的看法非常清晰："开源模型的爆发反映了一个事实：它们不在最前沿，但它们也离最前沿不远。成本性能比基本上是无与伦比的。" *（"The explosion of open source models has been I think reflective of the fact that they are not at the frontier, but they are not that far behind the frontier either. And the cost performance is basically unparalleled."）*

他使用了帕累托曲线的概念来解释这种关系："如果你想到一个帕累托曲线，它们位于便宜得多的那一侧，但以它们如此便宜的成本能获得那样的性能，这是相当令人难以置信的。" *（"If you think about a Pareto curve, right, they're on the much cheaper side, but it's pretty incredible the level of performance they get for how cheap they are."）*

在具体的模型上，Andrew 提到了三个名字："目前最大的几个是 DeepSeek、Kimi 和 GLM 模型。这些在我们的内部测试和基准测试中表现最好。" *（"The biggest ones are DeepSeek, Kimi and GLM models. These are the ones that have done the best on our own internal testing and benchmarking."）*

但 Andrew 也清楚地指出了开源模型的边界："你不想给 DeepSeek 一个任务是构建一个 ML 系统来分类十亿张图片，那种东西你可能希望 Astra 来看。但要做什么'居中这个按钮'，或者甚至'实现一个做 CRUD 操作的后端'，DeepSeek 会做得很好。" *（"You don't want to give DeepSeek a task of building an ML system to classify a billion images... But to do something like center this button, or even implement this backend that returns this CRUD operation, DeepSeek is to do great at that."）*

这段话的核心洞察在于：**任务复杂度是连续的**。一个巨大的产品开发过程由成千上万个不同复杂度的子任务组成。在"居中按钮"到"构建分布式 ML 系统"之间，存在着一个广阔的任务地带——开源模型在这个地带中拥有大量"甜蜜点"。Weave Router 的价值就在于精确地找到这些甜蜜点，把每一种任务分发给在其上性能成本比最优的模型。

Andrew 还分享了一个个人观察，其结论相当惊人："对于几乎任何爱好项目，你真的不需要超越开源模型。至少在我个人的经验中，只用开源模型就能走非常非常远。" *（"For pretty much any hobby project, you don't really need to go beyond open source models. At least in my own experience, doing a bunch of things on the side with this, the open source models only will get you very very far."）* 这意味着，对于大量非生产级、非关键任务的开发场景来说，开源模型已经构成了一个充分可用的替代方案——这在 18 个月前还被认为是不可想象的。

### 个人感受
访谈中有一个瞬间很细微但值得一提：当 Andrew 说到开源模型的能力时，他用了"相当令人震惊"（"pretty shocking"）这样的表述。对于一个每天跟踪模型性能的人来说，这种惊讶感本身就传递了一个信号：**开源模型的进步速度超出了最前沿从业者的预期**。在很多人的心智模型中，开源模型还停留在"能用但不够好"的阶段，但实际上，以 DeepSeek 为代表的一批开源模型已经在相当广泛的编码任务中展现了逼近前沿的能力。这个心智落差本身就是一种信息不对称——那些能更快更新认知的人，就能在成本上获得巨大的优势。

### 延伸思考
开源模型的崛起对 AI 行业的影响远不止"节省成本"这一层。一个更深层的效应是：**它为模型路由提供了存在的基础**。如果只有两三个前沿闭源模型，路由的价值是有限的——可选的路径太少。但当一个中等复杂度的任务可以在"顶级闭源模型（贵但保证质量）"和"开源模型（便宜且质量通常足够）"之间做出选择时，路由就成为一个真正有意义的优化问题。开源模型的丰富性，让"路由"从一个简单的 if-else 逻辑变成了一个需要训练 ML 模型来解决的复杂决策问题。在这个意义上，开源模型的爆发和智能路由的爆发是一枚硬币的两面。

### 精华收获
- 开源模型（DeepSeek、Kimi、GLM）在成本性能比上"无与伦比"，它们虽未追平前沿但已足够接近
- 大量简单至中等复杂度的编码任务（如按钮居中、CRUD 后端）并不需要顶尖闭源模型，开源模型完全能胜任
- 对于个人爱好项目或非关键任务，开源模型已经可以"走得很远"
- 路由的核心价值在于：在人手难以追踪的模型差异空间中，精确匹配每个任务与最优的模型选择


## 六、Weave Router 与其他路由器（如 OpenRouter）的本质区别

### 核心观点
OpenRouter 本质上是一个"网关"——让用户能方便地访问多种模型，但选择权在用户手中；而 Weave Router 是一个真正的"路由器"——它自动分析任务内容，基于训练数据智能决策模型分配，尤其在编码代理场景下拥有 OpenRouter 难以比拟的优势。

### 深度阐述

当被问到"Weave Router 和 OpenRouter 有什么不同"时，Andrew 给出了一个非常精准的区分。他指出，OpenRouter 本质上应该被称为"OpenGateway"（开放网关），因为"他们的游戏规则是让你尽可能容易地访问更多模型，你来选择使用哪个模型。" *（"OpenRouter you know maybe would be better referred to as OpenGateway. Their whole game is they let you access as many different models as possible and you choose which model you're using."）*

而 Weave Router 做的是完全不同的事情："我们在做的是自动为你选择模型。而且具体来说，我们是在编码代理的使用场景中做这件事。" *（"What we're doing is we're automatically choosing the model for you. Um, and specifically we're doing this in the coding agent use case."）* 他进一步明确表示，OpenRouter 也有自动路由功能，但"它表现得不是很好，这不是他们的重点。" *（"They have an auto router. It doesn't work very well. It's not really their focus."）*

这种区别看似微妙，实则至关重要。OpenRouter 解决的是"接入"问题——你可以通过一个统一的 API 访问几十上百个模型。但你仍然需要自己知道该用哪个模型。Weave Router 解决的是"判断"问题——你不需要知道哪个模型好，系统会根据任务内容自动选择。这就像旅行社和司机之间的区别：旅行社帮你找到所有可用的车辆（OpenRouter），而司机帮你决定哪条路最快、哪辆车最适合当前的路况（Weave Router）。

那么 Weave Router 是怎么做到这一点的？Andrew 在访谈中披露了其训练方法论。

**训练数据来源**："我们在数十万个编码代理会话上训练了我们的路由模型。" *（"We have trained our routing model on hundreds of thousands of coding agent sessions."）* 这些会话数据的重要之处在于，它不仅仅是"模型 A 完成了任务 X"这样简单的成败标记。Weave 的独特优势是它可以追踪下游效应："我们不仅看编码代理会话本身以及什么有效什么无效，我们还能看到所有的下游效应——这如何反映在结果性的 PR 中？当它被合并到生产环境时如何反映？一个月之后又如何反映？" *（"We're looking not just at the coding agent session itself and what's working and what's not, but also all the downstream effects because we can see all this like how does this reflected in the PR that results? How is this reflected when it gets merged to production? How is it reflected a month down the line?"）*

这是一个巨大的数据优势。大多数路由系统只能看到"任务是否完成"这种即时信号，但 Weave 能看到"这个任务的完成质量如何"这种长期信号。一个模型可能能够快速完成一个任务，但引入了一个三个月后才爆发的潜在 bug；另一个模型可能稍慢一些，但产出的代码在长期运行中表现更稳定。这种长期反馈对于训练一个可靠的路由模型来说，是极其宝贵的数据。

**训练方法**还包括强化学习："我们做了大量的额外训练，在其中测试了把它送到这个模型的路径还是那个模型的路径。如果它成功完成了任务，我们就给它奖励。通过这种组合——从大量真实会话中训练，以及做大量测试来看不同模型在哪里表现突出——我们能够对每个模型的强项有更清晰的了解，并自动学习。" *（"We do a bunch of additional training on top of that where we tested out sending it down this model's path or this model's path. And we give it a reward if it accomplishes the task successfully... It's a machine learning model that we're training."）*

最后一句话特别值得注意——"这不是我们在说'嗯，我们认为这个对 DeepSeek 来说会很好'，它是一个我们在训练的机器学习模型。" *（"It's not us saying like hmm we think this would be good for DeepSeek. It's a machine learning model that we're training."）* 这强调了路由器本身就是一个 AI 产品，它不依赖于人工经验法则，而是在持续学习和进化。

### 个人感受
Andrew 在回答这个问题时透露出的自信来自一个非常具体的地方：**数据闭环**。他说"Weave 能看到下游效应"——这不是一个模糊的陈述，而是对他们核心产品能力的自信延伸。在 AI 领域，拥有独特数据的人往往拥有最大的护城河。Weave 从测量产品中积累的"真实会话 + 下游结果"数据，正是训练路由模型所需要的、别人难以获取的资产。这个逻辑链——测量数据 -> 路由模型 -> 更好的路由器 -> 更多用户数据 -> 更好的测量——构成了一个自我强化的飞轮。

### 延伸思考
"网关 vs 路由器"的区别反映了一个更广泛的行业趋势：**AI 应用的竞争正在从"提供访问"转向"提供判断"**。在 AI 生态的早期阶段，最大的瓶颈是"能不能接入足够多的模型"，因此 OpenRouter 这样的基础设施服务具有很高价值。但随着模型数量爆发式增长，用户的瓶颈从"能用什么"变成了"该用什么"。在这个新阶段，提供"判断力"的产品比提供"接入力"的产品具有更大的价值。我们可以类比搜索引擎的演变：早期雅虎目录帮你"找到"网站，而谷歌帮你"判断"哪个网站最相关。历史总是押韵的。

### 精华收获
- OpenRouter 是"开放网关"——解决"接入"问题；Weave Router 是"智能路由器"——解决"判断"问题
- Weave 的核心数据优势：不仅追踪"任务是否完成"，还追踪"PR 是否合并、生产环境是否稳定、一个月后是否出现问题"
- 路由器本身是一个训练出来的 ML 模型，而非人工规则，这意味着它可以随着模型生态的演化持续学习
- 测量数据 -> 路由模型 -> 更好的路由 -> 更多数据，构成了 Weave 的飞轮效应


## 七、从 Cursor 到 Claude Code：18 个月内的 AI 编码代际更迭

### 核心观点
2025 年初，Cursor 是 AI 编码的主流工具，Claude Code 还只是研究预览版本；18 个月后，整个生态已经发生了翻天覆地的变化。Weave 之所以能在这个过程中保持领先，是因为他们始终与前沿用户群体保持紧密联系，始终比市场需求提前约 6 个月。

### 深度阐述

访谈中有一段历史回顾非常有价值，它帮我们梳理了 AI 编码工具在过去 18 个月中的快速演进。当 YC 合伙人在对话中提到"2025 年初是 Claude Code 刚上线的时候——实际上应该是研究预览版本——没人真正在使用它，所有人都在用 Cursor" *（"This is before Claude Code. I think Claude Code had just launched and no one was using it and everyone was using Cursor."）*，我们能看到 AI 编码工具领域的代际更迭速度是惊人的。

在当时的市场上，Weave 面临着一个独特的销售环境。Andrew 回忆说："这真的非常有趣，因为很明显有很多人想要测量软件工程，但我们接到的每一个电话都充满了纯粹的怀疑。我不相信你真的能做到这一点。" *（"There is clearly a lot of demand that people wanted to measure software engineering, but every single call we got on was pure skepticism. I don't believe that you can actually do this."）*

面对这种系统性怀疑，Weave 的策略不是辩解，而是**用客户自己的数据来证明**。"我们必须用他们的数据来证明给他们看。我们会接入他们的数据，向他们展示——这是它实际上在如何运作。这符合你的预期吗？" *（"We had to actually prove it to them with their data. We would connect their data and show them here's how it's actually working. Does this match your expectations?"）* 当客户在自己的数据中看到可信的测量结果时，怀疑就转化为了信任。"那是我们巨大的起飞时刻，当我们开始能够证明它的时候。" *（"That was the kind of huge lift-off moment when we started being able to prove it."）*

更重要的是，Weave 与最早期创业公司的紧密关系给了他们一种**时间差优势**。Andrew 如此解释："我们与很多增长最快的创业公司合作，因为他们就是那些用编码代理编程的人。所以这给了我们始终能走在曲线前面的优势。我们总是比市场提前 6 个月知道最前沿的人在做什么。" *（"We were working with a lot of the fastest growing startups because they were the ones coding with coding agents. So that gave us this always advantage of being ahead of the curve. We were always 6 months ahead of the curve because we knew exactly what the people at the forefront were doing."）*

YC 合伙人对这一点的总结非常精准："早期阶段的公司，比如 YC 批次中的公司，也许他们不在乎测量工程师的表现，因为他们还没有工程师。但他们生活在最前沿——用编码代理来写他们所有的代码。而你要卖给的那些公司，那些有庞大工程师团队的公司，他们可能在使用编码代理上落后 6 个月到一年。" *（"The early stage companies, like the batch companies, maybe they didn't care as much about measuring engineer performance because they didn't have any engineers. But they were living at the edge in terms of using coding agents to write all their code versus the companies that you were selling to who were maybe a couple years ahead, who had big engineering teams to really have the problem, they were 6 months or a year behind at using the coding agents."）*

这种"前沿用户走在规模客户前面 6 个月"的模式，对 Weave 来说是一个极为有利的市场位置。他们可以从那些最激进的编码代理采用者身上提前看到下一波需求是什么，然后在主流市场产生同样需求的时候，恰好已经准备好了解决方案。

### 个人感受
Andrew 说"我们总是比市场提前 6 个月知道最前沿的人在做什么"时，那种从容的语气让我想起了一个经典的投资原则：**信息的时间差就是 alpha**。对于 Weave 来说，这种信息优势不是从市场调研报告中得来的，而是从产品使用数据中自然涌现的。看到最优秀的团队如何使用编码代理，这本身就是一种极其稀缺的洞察来源。更有趣的是，这种优势是自我强化的——越多的前沿用户使用 Weave，Weave 就越早看到下一波趋势，就越能提前准备产品，就越能吸引更多前沿用户。

### 延伸思考
18 个月的时间之内，AI 编码工具的主流从 Cursor 切换到 Claude Code、Codex、Open Code、Py 等多工具共存的状态。这种演进速度对企业决策提出了巨大的挑战：今天投资学习的工具，明天可能就被取代。但对 Weave 这样的"测量层"产品来说，工具的快速更迭反而是一种竞争优势——因为无论你用什么工具，你都需要知道它的效果如何。**工具层一直都在变，但"测量和优化"的需求始终不变**。这就像淘金热中，挖金子的工具在不断更新换代，但卖铲子的人——以及那些衡量铲子效率的人——总是有钱赚的。

### 精华收获
- AI 编码工具的更迭速度极快（18 个月内从 Cursor 独大到多工具共存），押注单一工具的平台面临更大风险
- 面对系统性怀疑时，最有效的销售策略是"用客户自己的数据证明"——这比任何宣传都更有说服力
- Weave 的"6 个月领先优势"来自与前沿创业公司的紧密嵌入——他们是编码代理最激进的使用者
- 工具会变，但测量需求不变；做"不可变需求"的生意比做"可变工具"的生意更持久


## 八、工程管理者问题的演变：从"AI 有用吗"到"如何高效使用 AI"

### 核心观点
工程管理者向 Weave 提出的核心问题经历了三个阶段的变化：最初是"我们有多快"，然后是"AI 真的让我们更快吗"，现在则是"我们如何更高效地使用 AI"。这标志着 AI 编码正在从"要不要采用"向"如何优化"的阶段转变。

### 深度阐述

在访谈中，YC 的合伙人问了 Andrew 一个极具洞察力的问题："工程管理者向你们提出的问题，从 2025 年初到现在是怎么变化的？" *（"How have the questions that those engineering managers are asking you and asking your product changed from early 2025 to now?"）*

Andrew 给出的答案是三阶段演变：

**第一阶段："我们移动得有多快？和我们与基准相比如何？"** *（"It very much started off with just like how fast are we moving and how is that compared to the general benchmark."）* 这是测量需求的起点——人们想要了解自己团队的整体表现水平。

**第二阶段："AI 实际上让我们更快了吗？"** *（"Then it was is AI actually making us faster?"）* 随着 Cursor 等工具的普及，管理者开始追问 AI 工具的投资回报率。和早期阶段一样，这是一个"验证"期——人们需要用数据来判断 AI 是否真的值得投入。

**第三阶段（当前阶段）："我们如何开始更高效地使用 AI？"** *（"Then it's okay, how can we start to use AI more and more efficiently? That's kind of where we're at today."）*

Andrew 继续解释说，到了今天，"每个人都在用 AI 写他们所有的代码。也许不是每个人，但大多数我们合作的人至少是这样的。现在的问题是，如何开始优化这些。" *（"Everyone is writing all of their code with AI. Maybe not everyone, but most people hopefully that we work with at least. And now it's figuring out how do we start to optimize this."）* 他进一步指出，"这正是把我们引向路由器的原因。因为优化的一种方式就是为每个任务选择正确的模型。" *（"This is exactly what brought us to the router because that's one way to optimize is pick the right model for each task."）*

但优化不仅仅关乎模型选择。Andrew 补充了其他维度："这还包括你怎么做提示词、怎么做代理并行化、你的代理如何处理任务。这些是我们帮助团队真正理解和看到的东西。" *（"But it's also just like how are you prompting? How are you doing agent parallelization? How are your agents task handling?"）*

而当 YC 合伙人进一步追问："团队更关心的是如何提高生产力、让人们更多采用 AI、更多写代码，还是更关心如何确保人们不会只是在写 AI 垃圾、搞坏代码库、或者花了一大笔钱却没有实际 ROI？" *（"Are teams more excited about how do I increase productivity... or are they more concerned about other stuff? Like how do I make sure that people aren't just writing AI slop and wrecking my codebase?"）*

Andrew 给出了一个"转型曲线"的框架来描述这种变化："在开始时，人们非常关心如何获得 AI 采用率。然后进入'代币最大化'阶段——就是尽可能多地花、花、花。然后进入优化层面——现在每个人都在使用 AI，他们是 AI 原生的、AI 优先的，我们需要精细调优，确保我们没有在不必要的事情上烧 token。" *（"At the start, people very much care about just getting AI adoption... It goes into this token maxing phase, which is just let's spend, spend, spend as much as we possibly can and then it goes into that optimization layer."）*

他特别指出了一个有趣的市场分割："对于创业公司来说，他们通常还处于那种'代币最大化'阶段。他们不太关心成本优化，更关心生产力优化。我们也有很多晚期公司，包括一些私募股权拥有的公司，他们更处于优化曲线的层面。" *（"Startups are typically in that kind of still token maxing phase... We also have a lot of late-stage companies, some private equity owned companies that are much more on the optimization layer of the curve."）*

这个市场分割的意义在于：**不同成熟度的企业对 AI 编码的需求点是不同的**。初创公司愿意为生产力不惜成本，而成熟企业则更关注单位产出的成本效率。Weave 的产品需要同时服务这两种需求。

### 个人感受
这段三阶段演变的描述——从"我们有多快"到"AI 有用吗"到"如何优化"——读起来像是一部 AI 编码的微型采纳史。每一个新技术的大规模采用似乎都会遵循类似的轨迹：首先是好奇（"它能做什么"），然后是验证（"它值得吗"），最后是优化（"怎么做最有效"）。Weave 的独特之处在于，它在一个产品中同时覆盖了这三个阶段的需求——测量、验证、优化——这使得它能够在市场的不同阶段都保持相关性。这种产品设计的"跨度"在 B2B SaaS 中并不常见。

### 延伸思考
"代币最大化"这一阶段的存在揭示了一个重要的经济学现象：**当一种新生产工具的成本看起来低于其潜在收益时，人们会不加节制地使用它**。这就像早期的电力使用——工厂在引入电力后很长一段时间内都在"浪费电"，因为电费相对于人力成本的节省来说微不足道。只有当使用量增长到一定程度后，优化才开始变得有意义。在 AI 编码的语境下，"代币最大化"阶段可能不会持续太久——因为随着使用量的飙升，成本（或者速率限制）会变得不可忽视，届时优化需求会急剧上升。Weave 的 Router 正好卡在了这个拐点上。

### 精华收获
- AI 编码采纳的三阶段：测量 → 验证 → 优化
- 当前行业正处于"优化阶段"的早期，这正是模型路由等效率工具的市场窗口
- 初创企业处于"代币最大化"阶段（重视生产力），成熟企业处于"优化阶段"（重视效率），产品需要同时覆盖两种心态
- 优化不仅是"选对模型"，还包括提示词质量、代理并行化策略、任务分配方式等多个维度


## 九、成本产出的黄金指标：Weave 如何用数据诊断 ROI

### 核心观点
Weave 的核心指标是"单位产出的成本"——每个 AI 生成的"有效工作小时"花费了多少美元。这个指标能让管理者一目了然地识别出谁在高效使用 AI、谁在浪费 token。

### 深度阐述

访谈中一个极为精确的分析工具被提了出来——"每个产出的成本"（Cost per Output）。Andrew 解释了为什么这是他最看重的指标之一："我们展示的主要指标之一是每个产出的成本。就是你在 AI 上花了多少美元，产出了多少单位的产出。当我们说产出时，把它想象成一个人类工程师实际做的一个小时的工作。" *（"One of the main metrics we show is cost per output. So it's how many dollars are you spending on AI for unit of output. And when we talk about output, think of it as an hour of work for a human engineer to actually do."）*

这个指标为什么如此重要？因为它可以直接回答"这个人的 token 消费是值得还是浪费"这个问题。Andrew 用两个极端案例来说明：

**高效案例**："有人可能花了 1 万美元，但如果他们从中获得了 1 万个小时的工作量，那你每个工作小时只花了一美元。这是一笔非常好的交易。" *（"Someone could be spending $10,000 but if they're getting 10,000 hours of work out of it, you're only spending a dollar per hour of work. That's a really good deal."）*

**低效案例**："但另一种情况是，有人花了 1 万美元，但他们只得到 10 个小时的工作量。那你每个工作小时花了 1000 美元。这是一笔非常糟糕的交易。" *（"But there's the other case where somebody's spending $10,000 and they're still getting 10 hours of work. Now you're spending $1,000 per hour of work. That's a really bad deal."）*

这个对比清晰地展示了：**花多少钱不是问题，花了钱得到了什么才是问题**。如果有人一个月在 AI 上花了 1 万美元，很多管理者会本能地感到震惊。但如果这笔钱买来了 1 万个小时的有效工作量，那实际上是一个惊人的投资回报率。相反，同样的花费如果只买来了 10 个小时的工作量，那就是巨大的浪费。

Andrew 特别指出，当出现低效案例时，通常有两种原因："你在使用错误的模型，或者你有一个奇怪的代理循环在运行，它只是在燃烧 token 而没有产生真正的生产力。" *（"You're using the wrong models or you have this weird agent loop going on that's just burning tokens and giving us no real productivity."）* 换言之，有了这个指标，管理者就能精确地知道问题出在哪里，而不是模糊地感觉"我们的 AI 开销好像有点高"。

在访谈的稍早部分，YC 合伙人问到了一个非常实际的问题："当人们发现团队中有人的 token 消费是巨大的异常值时，他们的结论一般是'哇，这些是我们最好的表现者，我很高兴有他们在团队中，我想让每个人都像他们一样'，还是'哇，这个人花了 10 万美元，我应该和他谈谈如何更智能地使用模型？'" *（"When people see people who are huge outliers as the biggest spenders of tokens and therefore the most expensive people on the team, is the conclusion typically, wow, these are our best performers... or wow, this person just blew $100,000?"）*

Andrew 的回答再次指向了那个指标："这就是为什么'每个产出的成本'如此重要——它直接回答了这个问题。" *（"The reason that's so important it answers that question directly."）* 如果没有这个指标，高消费的人会被简单地视为"贵的负担"；有了这个指标，管理者才能区分"高成本高效率"和"高成本低效率"这两种完全不同的情况。

### 个人感受
这个指标的设计展示了 Weave 团队在"如何让数据有用"上的深度思考。很多数据分析产品的问题是，它们能展示大量指标，但用户不知道哪个重要。"每个产出的成本"之所以是一个好指标，是因为它天然地融合了"投入"和"产出"两个维度，让用户一眼就能看到效率。更重要的是，它避免了"省钱"这个常见但错误的优化目标——在 AI 编码中，过度节省 token 可能反而降低产能。用"成本效率"替代"成本总量"作为优化目标，是一个根本性的视角转变。

### 延伸思考
这个指标背后隐含着一个重要的管理哲学：**在评估员工的 AI 使用时，不要问"花了多少钱"，而要问"投入产出比如何"**。这种思想在投资领域早已是常识——没有人会单纯因为一笔投资的金额大就认为它不好，关键看回报率。但在工程管理中，"token 消费"往往被简单地视为成本来削减，而不是投资来优化。这可能反映了更深层的心态差异：在很多组织中，AI 工具的费用仍然被归类为"IT 支出"而非"生产力投资"。改变这种认知，可能是工程管理领域下一个需要跨越的障碍。

### 精华收获
- "每个产出的成本"= AI 花费 ÷ 有效工作小时数，是判断 AI 使用效率的关键指标
- 高 token 消费本身不是问题，高消费低产出才是问题
- 低效的常见原因：使用了不匹配的模型、存在无效的代理循环
- 用好这个指标，管理者可以从"凭感觉判断"转向"凭数据决策"，精准识别该奖励还是该纠正


## 十、顶级工程师的秘密：并行化的艺术

### 核心观点
使用 AI 编码工具最优秀的工程师，其最大的优势不在于"写得快"，而在于"并行化"的能力。并行化的难点不在于同时启动多个代理，而在于设计正确的护栏和框架，让人在最高杠杆的时刻介入。

### 深度阐述

访谈中有一个问题直击 AI 编码时代的关键技能：当你发现团队中有一两个顶级表现者时，如何把他们的能力扩散给整个团队？Andrew 的回答指向了一个具体的技能——**并行化**（Parallelization）。*（"I think the highest leverage single thing that we see is somebody's ability to parallelize."）*

Andrew 描述了这个技能的核心："如果你在单线程工作，你能完成的事情是有限的。如果你在多线程工作，你能完成更多的事情。" *（"If you are single threading, then there's only so much you can get done. If you're multi-threading, there's a lot more you can get done."）* 这听起来似乎很显而易见。但他立刻补充了一个关键的复杂性："问题在于，并行化不是简单地说'让我启动 10 个 Cloud Code 会话然后让它们自己跑'。" *（"The problem is that parallelization is not just so simple as like let me kick off 10 cloud code sessions and just let them cook."）*

真正的并行化挑战在于："你如何创建正确的护栏、正确的框架，来确保那些代理在做正确的工作，并且你在正确的时间介入，而不是在错误的时间被拉进来。" *（"What makes it harder to do well is how do you actually create the right guardrails, the right frameworks to make sure that those agents are doing the right work and that you're getting pulled in at the right times and not at the wrong times."）*

Andrew 称这是一个"不断演进的艺术" *（"This is an evolving art."）*，因为它随着每个新模型的发布而变化——"每当一个新模型发布，模型的能力改变了，人类注意力需要在哪里的位置也改变了。" *（"Every time a new model releases and the capabilities of the model change and where the human attention is necessary changes."）* 这意味着，没有一套固定的并行化技巧是可以永远有效的。模型越强，人类需要在某处介入的时刻就越少；模型在某一类任务上的表现好转，人类的注意力就可以转移到另一类任务上。

当谈到如何把优秀个体的并行化技能扩散给全团队时，Andrew 提到了一些具体的做法："分享护栏、分享某种技能，或者重构代码库的某些部分以匹配一个对代理来说更熟悉的架构。" *（"Sharing the kind of guardrails... maybe it's sharing a skill. Maybe it's refactoring some part of the code base to match a certain architecture that's much more familiar and comfortable for agents."）* 这些做法"因人和公司而异"。

更有趣的是，Weave 的产品本身在某种程度上自动化了这种知识扩散。正如访谈中另一位创始人补充的："我们的产品实际上做的就是这个。它查看你所有的 prompt，查看什么被发布到了生产环境，然后给你具体的技能建议，告诉你如何更好地使用这些工具。它还有一个'教练'来做这件事。" *（"Our product actually does exactly this. It looks at all of your prompts and it looks at what's landing in production and it gives you specific skills that you could equip on how to use these tools better. And it has like a coach to actually do this."）*

这个"教练"功能可以给出什么样的建议呢？Andrew 举了一个例子："它可能会告诉你如何用代理来处理任务，或者如何更好地反驳你的代理——因为现在人们做得不够的一件事就是告诉你的代理'不，你错了'。" *（"How to push back on your agent better because that's something people don't do enough now — tell your agent that no you're wrong."）* 另一个例子是："它可能会说，你应该更频繁地重启会话，而不是继续在当前的会话中运行。" *（"Hey actually you should be restarting sessions more often as opposed to just continuing to run with the current session."）* 这个建议的技术原因在于，随着会话继续，上下文窗口越来越大，成本也越来越高，而且过长的上下文可能导致模型性能下降。

### 个人感受
"告诉你的代理'不，你错了'"这个建议尤其有趣。它揭示了一种默认的心理惯性：人类在使用 AI 辅助工具时，很容易滑入一种"接受模式"——因为 AI 产出了看起来合理的内容，所以就不加质疑地接受了。但真正高水平的 AI 协作恰恰需要人类保持"怀疑模式"，在恰当的时候对代理说"你错了"。这不是对 AI 的不信任，而是对人类判断力价值的重新确认。在 AI 编码的时代，"知道什么时候该反驳你的工具"正在成为一种核心技能。这种技能的本质是：**AI 让你有更多的时间，但你不应该把所有这些时间都用来"接受"，而应该把一部分用来"质疑"**。

### 延伸思考
并行化这个概念背后隐藏着一个深刻的转变：**工程师的角色正在从"执行者"变成"管理者"**。在传统模式下，一个工程师的价值主要在于他/她能写多少代码。但在 AI 编码模式下，一个工程师的价值越来越多地取决于他/她能"指挥"多少 AI 代理并行工作，以及他/她能在什么时机、以什么方式介入。这本质上是一种管理技能——分配任务、设置约束、在关键节点检查、在方向偏离时纠正。一个优秀的"AI 原生工程师"，实际上是一个优秀的"微型项目经理"，管理着一个由 AI 代理组成的虚拟团队。这个转变对于工程师的职业发展有着深远的影响——那些拥有良好判断力和协调能力的人，将在 AI 时代获得远超技术能力的优势。

### 精华收获
- 并行化是 AI 编码时代最高杠杆的技能，但它的难点不是"多开几个会话"，而是"在正确的时间介入正确的会话"
- 没有固定的并行化技巧——每次新模型发布，并行化的策略都需要重新调整
- Weave 的"AI 教练"功能通过分析每个会话，给出个性化建议，如"更频繁地重启会话"、"学会反驳你的代理"
- AI 原生的高效工程师本质上是一个"微型项目经理"，管理的对象是 AI 代理团队


## 十一、软件工厂：当编码代理在深夜无人值守时运行

### 核心观点
"软件工厂"是 AI 编码的进阶形态——多个代理在无人值守的情况下持续产出代码。其核心挑战不在于产能，而在于验证和质量控制——如何确保自主运行的代理代码真正可交付。

### 深度阐述

当 YC 合伙人问起"软件工厂"这个概念的实践细节时——"如果会用好 AI 编码的基本盘是学会并行运行 10 个 Claude Code 会话，那么下一个层级就是搭建一个在你工程团队睡觉时依然在写代码的软件工厂" *（"Maybe the next level is learning how to set up software factories that are coding while your engineering team is asleep."）*——Andrew 的回答聚焦在一个最关键的痛点上：**验证**。

"我认为所有尝试过使用编码代理的人都知道，它们能吐出你要求的任意多的代码。所以真正重要的不是测量输出。" *（"I think everyone who's ever tried to use a coding agent knows that they can spit out as much code as you ask them to. And so it's not really about measuring just the outputs."）* ——这句话击中了 AI 编码的一个核心误区。很多人以为 AI 代理的挑战是"让它写出足够多的代码"，但真正的挑战是"让它写出值得进入生产环境的代码"。

"理解如何正确地验证，是构建软件工厂最困难的部分。" *（"Understanding how to correctly validate this is the hardest part of building a software factory."）* Andrew 的这句话应该被刻在每个试图大规模采用 AI 编码的团队墙上。

那么 Weave 自己是怎么做的？Andrew 分享了两个关键实践：

**点击并替换**（原文为"clique and replace"可能指某个具体工具，根据上下文可能是某种自动化代码评审工具）——他首先提到了一系列代码审查工具："有很多现成的审查工具在这方面做得很好。我们在每个 PR 上使用了四个工具，其中两个是 YC 系公司——Cryptile 和 Parameter。我们还使用 Cursor Bug Bot。实际上，每个 PR 上有四分之三是 YC 系公司。" *（"We use four of them at Weave, two of which are YC companies, Cryptile and Parameter. And then we also use Cursor Bug Bot. Actually, three of them yeah and Cubic. So three out of four YC companies on every single PR."）* 当被问到"每个 PR 的美元成本是多少"时，Andrew 的回答体现了创始人的计算逻辑："基本上只要每一个都能发现其他几个没发现的问题，那就值得。" *（"Basically it's worth it as long as each one is finding things the other ones aren't."）*

这些审查工具解决的是"单个 PR 内部"的问题——这个 PR 里有没有 bug、逻辑错误、不良实现等。但 Andrew 指出了一个更微妙的问题："除了单个 PR 这个相对狭窄的目标之外，我们如何确保这个 PR 会很好地融入系统？确保它具有可扩展的架构？确保它容易进行未来的贡献？我认为这是轻量级软件工厂方法失败的最主要地方。" *（"Aside from just the single myopic goal of this one PR, how do we make sure that this is going to fit into the system well, that it's going to be a scalable architecture, it's going to be easy for future contributions. I think this is the biggest place where the light software factory approach fails."）*

Andrew 用一句话总结了这种系统性失败的根源："每个 PR 在局部上都是合理的，但你把它放在一起看，全局上就是疯狂的——充满了各种糟糕的一次性变通方案。" *（"Every PR is locally logical and then you put it all together and it's something that's globally insane with all kinds of terrible one-off workarounds."）*

为了解决这个问题，Weave 团队构建了自己的"检查系统"，可以被视为"软件工厂的 QA"。Andrew 解释了这个系统的运作方式："我们定义了所有 Weave 团队中资深软件工程师真正关心的事情——那些如果我们对每一个 PR 做人工审查时会经常被指出的问题。然后我们把这些放进对每个 PR 运行的检查中。" *（"We define all the things that an expert software engineer on the Weave team might really care about, the type of things that if we were doing human reviews on every single PR, they would commonly be calling out... And then we put these into these checks that are run on every single PR."）*

一个具体的检查例子是**过度抽象**（Over-abstraction）："编码代理经常会做的一件事是过度抽象。它只有一个需要做的事情，但它做了整个疯狂的抽象系统，而且永远不会被使用。所以我们有一个检查来防止过度抽象，带有好的例子和坏的例子的上下文。" *（"The type of thing that a coding agent will often do is over abstraction. It has a single thing it needs to do and it makes this entire crazy abstract system that will never be used. And so we have a check that prevents over abstraction with context and examples of what good looks like, what bad looks like."）*

### 个人感受
"每个 PR 局部合理，但全局疯狂"*（"Every PR is locally logical and then you put it all together and it's something that's globally insane."）* 这句话可能是整个访谈中最精辟的一句。它精准地描述了 AI 代理工作方式的核心缺陷——缺乏全局视野。人类工程师在写代码时，脑子里始终有一个"系统的整体图景"。他们知道这个模块和另一个模块之间的关系，知道哪些抽象是有意义的、哪些是过度设计。而 AI 代理——至少在当前——主要基于局部上下文来做决策。它们可以看到一个 PR 涉及的所有代码，但它们看不到这个 PR 将如何与其他 PR 相互作用、在六个月内会演变成什么。这个限制是根本性的，短期内不太可能被消除。因此，软件工厂的成功关键就在于如何"补足"这个局部推理的缺陷——通过系统级的检查、架构约束和人工审查的恰当介入。

### 延伸思考
这个讨论揭示了一个对于 AI 时代软件开发至关重要的区分：**"正确性"与"适应性"是两个不同的问题**。现有的 AI 代码审查工具主要解决"正确性"问题——这段代码能不能正确地完成它的功能？但 Weave 的自建检查系统解决的是"适应性"问题——这段代码是否适合这个系统的整体架构？是否便于未来的演进？

这两个问题的性质截然不同。正确性是局部的、可穷举的——可以通过测试用例、静态分析、类型检查来验证。而适应性是全局的、不可穷举的——需要判断力、审美和长期视野。在 AI 编码的早期阶段，人们的注意力主要集中在正确性上，因为这是更紧迫的问题。但随着软件工厂的规模扩大，适应性问题会变得越来越突出，因为成百上千个"局部正确但全局不协调"的代码片段聚积起来，会创造出一个无法维护的代码库。这个问题的本质是：**AI 代理需要被嵌入到一个架构治理框架中，而不仅仅是和一个任务配对**。

### 精华收获
- 软件工厂的核心挑战不是"写更多的代码"，而是"确保写出的代码是正确的和可用的"
- 多个 AI 代码审查工具并用是值得的——只要每个工具都能发现其他工具遗漏的问题
- AI 代理最大的系统缺陷是"局部合理但全局疯狂"——缺乏对系统整体架构的视野
- 解决这个问题的有效方式：将资深工程师的审查标准提炼为可自动执行的检查清单，如"防止过度抽象"
- 软件工厂的真正考验在于"验证系统"的质量，而非"生成系统"的速度


## 十二、AI 编码的未来：从"人写代码"到"人分配 token"

### 核心观点
未来工程团队管理的核心将不再是"谁写代码写得好"，而是"谁能最有效地分配 AI 资源"。优秀的 AI 时代工程师将凭借"品味、判断力和驾驭代理的能力"脱颖而出。

### 深度阐述

访谈接近尾声时，YC 合伙人问了一个带有远见色彩的问题："AI 编码在接下来一年半会是什么样子？" *（"What is AI coding going to look like in another year and a half?"）*

Andrew 的回答给出了一个极具启发性的框架："我们认为，广义上，管理一个工程团队将成为一种 token 分配的练习。" *（"We think that broadly running an engineering team will be an exercise in token allocation."）* 在这个未来图景中，工程团队的核心任务变成了："找到那些最善于向外看世界、感知机会的人，然后部署他们的 AI 集群来抓住这个机会。他们有品味、有判断力，能够非常有效地驾驭这些代理。" *（"You find the people who are the best at looking out in the world, sensing the opportunity and deploying their swarm of AIs to take advantage of that opportunity. They have taste, they have sense, whatever it is, and they're able to harness these agents really effectively."）*

这段话中最值得注意的是 Andrew 对"未来顶级工程师"特质的重新定义。他明确指出，"在极限情况下，如果你把模型持续改进的曲线延伸出去，它很可能不会是那些最擅长反转二叉树的人。" *（"In the limit where you trace out the curve of how the models continue to improve, it's probably not going to be necessarily the people who are the best at inverting a binary tree."）* ——他指的是传统工程面试里典型的技术能力测试——"它更可能是那些最善于向外看世界、看到这里有一个需要解决的问题、以及我该如何构建解决方案的人。" *（"It probably is going to be the people who are the best at looking out into the world and seeing that here's a problem that needs a solution and here's how I'm going to build this solution."）*

这个预判有着深远的意义。传统上，软件工程的核心技能是"实现"——把一个已经定义好的需求转化为可工作的代码。但在 AI 编码时代，"实现"正在被代理自动化，而"定义"——理解世界的问题在哪里、什么样的解决方案是有价值的——正在成为人类工程师最稀缺的能力。换句话说，**工程师的价值链正在从"执行端"向"发现端"转移**。

在这个未来中，工程师的角色更像是一个"机会识别器"和"资源分配器"，而不再是一个"代码实现者"。他们的核心技能变成了：判断哪些问题值得解决、用什么样的方式解决最有效、如何协调一群 AI 代理来实施解决方案。

这与 Andrew 在另一个问题中提出的观点形成了呼应。当他回答"如何成为团队中最厉害的 AI 编码者"时，他的建议可能听起来有些出人意料："不要忘记你实际上在做什么。" *（"Don't lose track of what you're actually doing."）* 他解释说："我们不断看到的是，最擅长使用这些工具的工程师，同时也是那些最理解自己实际在做什么的人，因此他们能最好地驾驭和引导这些工具。" *（"What we constantly see is the engineers that are the best at using these tools are also the ones who understand the best what they're actually doing and therefore they can steer them and guide them the best."）*

他用了一个非常精妙的比喻："有一个人我非常尊重，他曾经告诉我，最好的工程师理解他们当前工作内容之下两层的抽象和之上两层的抽象。我认为这在 AI 时代仍然是 100% 真实的。只是你默认工作的抽象层级往上升了一到两级。" *（"Someone I really respect once told me is the best engineers understand everything two levels of abstraction below and two levels of abstraction above whatever they're currently working on. And I think that's still 100% true in the world of AI. It's just that the default level of abstraction you're working on has moved up like a level or two."）*

但他警告说："当你失去对实际发生的事情的接触时，那就是你很难避免被'垃圾代码的浪潮'卷走的时候。" *（"When you lose touch with what's actually happening, that is where it becomes hard to avoid being swept up in the tidal wave of slop."）* 这里的"slop"（垃圾代码）是 AI 编码时代的一个新词汇，指那些由 AI 生成但质量低劣、缺乏深思熟虑的代码。

### 个人感受
Andrew 关于"两层抽象之上、两层抽象之下"的说法，在整个访谈中给我留下了最深刻的印象。这句话最初来自于一位他尊重的前辈，但 Andrew 在 AI 编码的语境中赋予了它全新的含义。在传统工程中，"理解两层抽象之下"意味着你了解底层系统的工作原理；"理解两层抽象之上"意味着你了解业务需求和产品方向。在 AI 编码时代，这个原则依然成立，但"默认的抽象层级"发生了位移——你可能不再需要理解具体语法细节，但你仍然需要理解系统架构；你可能不再需要手动实现每个功能，但你仍然需要知道一个功能应该长什么样、和系统的其他部分如何交互。

最具力量的警告是"当你失去对实际发生的事情的接触时，那就是你很难避免被垃圾代码浪潮卷走的时候。"这句话的意义在于，它指出了一条**危险的捷径**：在 AI 编码的时代，看起来你可以在不理解系统的情况下让 AI 帮你干活。但这样做等于是把自己所有的判断力都外包给了一个"局部合理但全局可能疯狂"的系统。那些理解得最多的人，恰恰是那些能从 AI 中获得最大价值的人。

### 延伸思考
"工程团队管理将成为 token 分配的练习"*（"Running an engineering team will be an exercise in token allocation."）* 这一预判背后的经济逻辑是什么？当我们从"人写代码"转向"AI 写代码"时，工程团队的主要瓶颈从"人力资源"变成了"token 资源"。管理一个团队的核心问题由此变为：如何在这些 token 资源中做出最优分配——哪些项目值得投入 tokens？每个项目应该用什么质量的模型？如何在速度和成本之间找到平衡？

这个转变的影响比表面上看起来的要深远得多。它意味着工程管理者的技能集需要从"人员管理"扩展到"资源优化"。一个优秀的工程管理者需要同时具备：识别高价值机会的能力、判断模型适用性的能力、设计验证系统的能力、以及持续调整资源分配策略的能力。这本质上是一个投资组合管理者的角色——把你的 token 预算分配到最有价值的机会上，同时管理风险。

### 精华收获
- AI 编码的未来核心转变：工程团队管理从"人力管理"变为"token 分配"
- 顶级 AI 时代的工程师不再以"写码速度"取胜，而以"识别机会、驾驭代理、保持全局理解"取胜
- "两层抽象之下、两层抽象之上"原则在 AI 时代依然有效，但默认抽象层级更高了
- 最大的风险是"失去对实际发生的事情的接触"——那会导致被 AI 生成的垃圾代码浪潮吞噬
- 人类工程师在 AI 时代的最核心价值：品味、判断力、以及知道"什么值得被构建"的能力


## 十三、当模型路由成为未来：为什么你不必再手动切换模型

### 核心观点
随着模型生态的持续复杂化，手动追踪每个模型的优势和劣势正变得不可持续。智能路由将取代手动选择，成为 AI 编码的默认模式——不仅能省钱，还能超越任何单一模型的能力。

### 深度阐述

当被问到"今天大多数人设置一个模型（比如 Claude Code 或 Codex），然后一直用它直到手动切换。你觉得未来会是什么样？" *（"Today most people the way they write code is they set a model and then that's the model that they use... How do you think it's going to work in the future?"）*，Andrew 给出了一个直截了当的答案。

他认为，手动模型选择已经"累人了"——"你总要跟上每一个模型擅长什么、不擅长什么、它们的优势和劣势。这就是为什么我认为每个人都会走向这种路由器方法。" *（"At this point it's getting exhausting to always keep up to date with what every single model is good at... And that's why I think everyone's going to be moving towards this router approach."）*

这个论述背后有一个非常朴素但强有力的逻辑：**模型的数量和复杂度正在以指数级增长，而人类的认知能力是固定的**。没有人能同时追踪 Opus、Astra、DeepSeek、GLM、Kimi 以及其他几十个模型的最新能力变化。即使你能在今天做到这一点，下个模型版本发布时，一切都会改变。手动切换模型在这个生态中注定是一种不可持续的行为。

但 Andrew 进一步指出了一个更有趣的观点："如果你真正理解了每个模型的优势，你实际上可以开始构建一个比任何单个模型都更强大的路由器——你可以汲取每一个的优势，实际上超越真正的前沿。" *（"If you actually understand what every single model strengths are, you can actually start to build this router that is stronger than any individual model. So you can pull the strengths of each of them and actually outperform whatever the frontier truly is."）*

这是一个重要的观点：智能路由不仅仅是"节省成本"的手段，它还能**超越任何单一模型**。因为不同的模型在本质上有着不同的"性格"和"优势"。一个模型可能在算法设计方面表现卓越，另一个可能在调试复杂系统方面更胜一筹。通过智能地组合这些模型，理论上可以实现比任何一个单独模型都更好的整体性能。这类似于"集体智慧"的概念——由多个不同视角的模型组合成的系统，其判断力可以超过任何一个单一的专家。

### 个人感受
当 Andrew 说"超越任何单个模型"时，我能感受到这个话题正在从"省钱小技巧"升级为一个"产品哲学"。路由器的意义从来不只是"用便宜的东西替代贵的东西"。如果路由器只是这样，它充其量是一个成本优化工具。但 Weave 的愿景要宏大得多——他们希望构建的是一个"模型之上的模型"，一个能够理解所有模型并调配它们的"元模型"。在这个图景中，路由器就不再是一个简单的分发器，而是一个真正的智能层，它比它所管理的任何一个模型都知道得更多。

### 延伸思考
从更宏观的视角来看，"智能路由"的理念正在超越 AI 编码的边界，出现在越来越多 AI 应用的架构中。在 LLM 推理方面，我们有模型集成技术；在 Agent 系统中，我们有任务路由；在企业 AI 治理中，我们有策略路由。这种模式的核心逻辑是相通的：**当你有多个不同优势的 AI 能力时，把它们视为一个可调度的资源池，由一个更高层的智能来负责分配，通常比重度依赖单一能力更有优势**。如果这个趋势持续下去，"路由"将成为 AI 基础设施中不可或缺的一个层级——就像操作系统中的调度器之于计算资源一样。Weave 正在试图成为 AI 编码领域的那个"调度器"。

### 精华收获
- 手动追踪和选择模型是不可持续的——模型数量太多、能力变化太快
- 智能路由器不只是"省钱"，它还能通过组合不同模型的优势来超越任何单一模型
- "模型之上的模型"是 AI 基础设施中一个重要的概念——路由器的本质是一个元模型，负责调度其他模型
- "路由"作为 AI 系统架构中的一个独立层级，正在获得与"存储"、"计算"等基础概念同等的重要性


## 综合洞察：重新思考 AI 编码的"效率"叙事

把所有这些片段放在一起看时，一个更宏大的叙事浮现出来。AI 编码正在经历的不是一次单纯的技术升级，而是一场**生产力管理范式的根本转变**。

表面上看，Weave Router 解决的问题是"如何不浪费 token"——一个听起来相当具体的优化问题。但在更深层面，它触及的是一个系统性问题：**当生产工具从"人类"变成了"人类 + AI 代理"时，我们该如何衡量、管理和优化产出？**

在传统软件工程中，管理者依赖的是一套历史悠久但不精确的指标体系——代码行数、PR 数量、故事点。这些指标的问题不只是"不准确"，而是它们**测量的是错误的东西**。它们测量的是活动的数量，而不是结果的品质。

AI 编码的本质意义在于，它让"结果"第一次成为可能被精确度量的对象。因为当代码由 AI 生成时，每一行代码都带上了可追踪的语义信息，可以分析它的目的、质量、影响和后果。这使得一种全新的工程管理方式成为可能：**不再是"你写了多少代码"，而是"你的代码实现了什么"**，以及更进一步的——"你花了多少资源来实现它"。

Weave 在这个转变中的位置是独特的。他们既有测量能力（理解发生了什么），又有优化能力（做出更好的资源分配决策）。这两个能力的结合使他们能够提供一个完整的闭环：测量 → 诊断 → 优化 → 再测量。在 AI 编码领域，很少有其他公司同时覆盖这个闭环的两个端点。

而更值得关注的是，这个闭环正在将他们引向一个更大的愿景：软件工厂。在这个愿景中，工程部门不再是一群人在键盘前写代码，而是一个持续运行的智能系统，由人类工程师设定方向和质量标准，由 AI 代理集群执行具体工作，由路由系统优化资源分配，由验证系统确保产出质量。

当 Andrew 在访谈最后说"运行一个工程团队将成为 token 分配的练习"时，他并不是在做一个夸张的预言。他是在描述一个已经在他眼前展开的、且正在急剧加速的现实。对于每一个在这个行业中工作的人来说，那些理解这一转变的人，将比那些仍然固守传统工程管理范式的人拥有巨大的阶段性优势。

这也是为什么这场访谈的核心信息——"Stop Wasting AI Tokens"——远不止是一个产品宣传口号。它是一句箴言，提醒我们：**在 AI 时代，效率不再只是"做得快"，而是"做得对——用对的资源，在对的时机，以对的方式。"**


<!-- TLDR: AI 编码的核心从写码转向路由——选对模型、优化并行化、确保质量，才能在 token 经济中胜出。 -->
<!-- TAGS: AI编码, 模型路由, 软件工程, Weave Router, 工程生产力 -->
<!-- RATING: 4 -->
