---
title: "Building Legal Agents When You Can't See the Data — Jacob Lauritzen, CTO of Legora"
channel: "Latent Space"
published: "2026-11-02"
source_url: "https://www.youtube.com/watch?v=bJBEFzlKPoQ"
video_id: "bJBEFzlKPoQ"
tags: ["法律科技", "AI代理", "产品架构", "数据隐私", "垂直SaaS", "评估系统"]
rating: 5
language: "英文"
word_count: 34517
duration: "1:07:22"
---

# Building Legal Agents When You Can't See the Data — Jacob Lauritzen, CTO of Legora

- **Channel:** Latent Space
- **Published:** 2026-11-02
- **Source:** https://www.youtube.com/watch?v=bJBEFzlKPoQ
- **TL;DR:** 法律 AI 的未来在于用少数核心原语支撑无限产品，同时学会在数据不可见的世界中构建有效的评估系统。
- **Tags:** 法律科技, AI代理, 产品架构, 数据隐私, 垂直SaaS, 评估系统
- **Rating:** 5

## 版本

- [结构化文稿](2026-11-02-building-legal-agents-when-you-can't-see-the-data-—-jacob-lauritzen,-cto-of-legora-bJBEFzlKPoQ.structured.md)
- [原始文稿](2026-11-02-building-legal-agents-when-you-can't-see-the-data-—-jacob-lauritzen,-cto-of-legora-bJBEFzlKPoQ.transcript.md)

# 当你看不到数据时，如何构建法律智能代理？——Legora CTO Jacob Lauritzen 深度访谈

---

## 材料信息

- **标题**：Building Legal Agents When You Can't See the Data — Jacob Lauritzen, CTO of Legora
- **频道/来源**：Latent Space
- **类型**：YouTube 视频（播客访谈）
- **关键嘉宾**：Jacob Lauritzen（Legora CTO，丹麦裔，公司最初在斯德哥尔摩起步）
- **背景元数据**：Legora 是 YC 2024 年冬季批次的成员，被认为是历史上增长最快的法律科技公司之一。公司最初名为 Leia（后来被西班牙报纸杜撰为"Legally Efficient Yoda Assistant"的缩写），目前已扩展到纽约、旧金山、斯德哥尔摩和伦敦，工程团队约 100 人。

---

## 开篇引入

法律行业，可能是世界上最古老、最保守、最抗拒技术变革的行业之一。几百年来，它的核心资产始终只有一个：**人**。律所的价值完全建立在律师的大脑和工时的计算之上——"按小时收费"的模式铁板一块，像是刻在行业 DNA 里的某种不可动摇的秩序。

但现在，这个行业第一次真正遇到了一个变量：AI 代理不仅在做法律研究、起草合同、审阅百万级文件，更重要的是——它让"数据不可见"这个独特约束变成了产品设计和公司战略的核心张力。当你的客户是律所，而律所的数据不是他们自己的数据、而是他们客户的机密数据时，你如何在完全看不到真实使用轨迹的情况下，构建一个真正有效的代理系统？

这期 Latent Space 的访谈里，Legora 的 CTO Jacob Lauritzen 深入探讨了他如何在这条"盲飞"的航线上领导一家百人规模的工程团队，构建第一代法律代理。他谈到了从"20 人斯巴达工程师"到 100 人的战略纠葛、为什么电子表格是法律审查的最佳形态、如何用"法律工程师"这个几乎不可能雇到的人才类别撬动产品开发、以及——最核心的——**当你连用户正在做什么都不知道时，你如何做评估？**

---

## 详细内容

### 欧洲基因与"永远的弱者"文化

**核心观点**
Legora 的欧洲血统塑造了一种特有的谦逊文化和作为"弱势方"的战斗心态，但在进入美国市场的过程中，他们不得不学会更激进地自我推销。

**深度阐述**

Jacob 的姓氏 Lauritzen 本身就带着欧洲的根源——"sen" 在丹麦语中意味着"son of"，所以他的名字字面意思是"Lauritz 之子"。这种深厚的欧洲底蕴也反映在 Legora 的公司文化中。

Jacob 描述这种欧洲性时用了"underdog"（弱者、后来者）这个核心概念：

> "We are just at the core probably very humble about what we're doing because we've always been the underdog from the very very beginning. No one believed that small startup in a basement in Stockholm was going to out compete this huge [company] that was like way ahead of us in the US."（我们的核心就是对我们正在做的事情非常谦逊，因为我们从最开始就一直是弱势方。没有人相信斯德哥尔摩地下室里的一个小创业公司能够超越美国那个远远领先我们的巨头。）

这种"从地下室开始、不被人看好"的起点，奠定了一种持续战斗、始终需要证明自己存在价值的心态。但正如 Jacob 坦诚的那样，随着进入美国市场，这种文化也需要有意识地调整：

> "We've had to learn as we've become more and more... as we've entered the US and been in the US a lot more is to be a little bit more bold and tell the world how great we are cuz it doesn't come naturally to some of us."（随着我们越来越多地进入美国，我们不得不学会更大胆一点，去告诉世界我们有多棒，因为这对我们有些人来说并不自然。）

**个人感受**

Jacob 在描述这段文化差异时，语调里既有对欧洲式含蓄的自豪，也有一种几乎是不情愿的认可——在美国市场，"产品好"本身是不够的，你还需要愿意站出来说"我们很棒"。对于习惯了北欧"少说多做"价值观的技术团队来说，这是一种反向的文化学习。

**延伸思考**

这种文化差异其实反映了一个更广泛的现象：不同地域的创业公司拥有不同的"默认姿态"。欧洲创业公司往往在产品工程层面非常扎实，但在商业攻势和叙事能力上相对保守。当竞争跨越了地理边界，文化的自我调适本身就成了一种战略能力。

---

### 产品之旅：从瑞典法律 ChatGPT 到全栈法律操作系统

**核心观点**
Legora 最初只是一个带有瑞典法律搜索功能的 ChatGPT，经过四年的演进，已经扩展成一个包含法律代理、批量审查表格、工作流编排、协作门户和邮件/Word 插件的综合平台。

**深度阐述**

Legora 的原点极其简单——Jacob 明确表示："The way everything started was chat GPT with Swedish laws search tool in it. That was literally the entire everything."（一切的起点就是一个带有瑞典法律搜索工具的 ChatGPT，真的就是那一切。）

这个初始形态很聪明：法律研究是一个巨大的全球市场，律师需要花大量时间弄清楚"之前的类似案件是怎么判的""法律先例是什么""之前的人在这些情况下怎么做的"。用一个代理来查询法律条文，这是最低成本的起步方式。

但接下来，产品在四个维度上不断扩展：

1. **能力扩展**：代理现在可以起草文件、编辑 Word 文档、组织文件、运行复杂分析。
2. **Tabular View（表格视图）**：一个革命性的理念——用电子表格的形态来批量提取和审查成千上万份协议。Jacob 骄傲地提到："One of our features called tabular view... is now a name that's being used in industry, and we're very happy to see Claude for Legal using our terminology."（我们的一个功能叫 Tabular View...现在这个名称已经在行业内被使用了，我们非常高兴看到 Claude for Legal 在用我们的术语。）主持人听到后直接说："We got to talk about that. We got to talk about that."（我们必须聊聊这个。）——这部分在后面的章节会深入展开。
3. **工作流编排**：Lists（类似 Linear 的任务管理）、Intake（与客户的协作方式）、Portal（律师对律师、客户对律师、律师对代理、代理对代理的协作层）。
4. **外围工具**：Word 插件和 Outlook 插件，因为很多律师实际上是在 Word 里工作的。

Jacob 将产品的整体逻辑归纳为两件事：

> "It's doing the work and it's also like orchestrating the work."（它在做工作，同时也在编排工作。）

这种"工具 + 平台"的双重定位，使得 Legora 不仅仅是一个更聪明的搜索引擎，而是真正试图成为法律工作的基础设施层——让律师在其中完成工作、与同事协作、与客户沟通，并且代理可以在其中自动执行大量任务。

**延伸思考**

这种从单一智能搜索工具到全栈平台的产品演进路径，与 Cursor、Replit 等编码工具的发展轨迹惊人相似。编码工具也经历了"从自动补全到全栈 IDE+ 代理协作平台"的过程。法律和编码作为知识工作最集中的两个领域，正在以平行的方式被 AI 改造。而 Jacob 的产品哲学——将工作执行与工作编排放在同等重要的位置——其实在暗示一个更深的趋势：AI 代理不仅仅是"做得更快"，它正在改变整个"工作的组织方式"本身。

---

### 模型策略与用户控制的悖论

**核心观点**
Legora 采用多模型路由策略，但创始团队一开始强烈反对给用户提供模型选择器。最终他们"投降"了，但发现模型选择在法律领域远不如工程领域那么重要——因为律师根本不知道什么是 Sonnet 什么是 Opus。

**深度阐述**

当被问到模型底层架构时，Jacob 的态度非常务实："We're using a bunch of different ones depending on task."（我们根据任务使用不同的模型。）在代理中有一个模型选择器用于主模型，但某些工具内部会使用不同的模型，例如 Tabular View。他的做法是"subdivide the problem and route"——把问题切分，然后按子任务路由到不同的模型。

然后发生了一个很有意思的对话。主持人 Swyx 提到自己作为 Cognition 的顾问加入时的一个核心命题——"an agent lab is a domain specific GPT wrapper"（代理实验室就是一个领域特定的 GPT 外包装）。他的论点是：领域专家应该为用户决定用哪个模型，因为律师的职责不是去了解模型之间的差异。

于是就有了这段极生动的对话：

> "If you go to a lawyer and you ask them 'oh you're going to draft this contract based on this precedent, do you think that's a Sonnet high or an Opus mid task?' They won't know. Just give me this."（如果你去问一个律师："你要基于这个先例起草合同，你觉得这是 Sonnet 高级别还是 Opus 中等级别的任务？"他们根本不知道。直接给我用就好。）
>
> "Exactly. Like 'just make it work.' Hourly rate is $1,000 an hour."（对，就像"管它呢，让它能用就行。我的时薪是 1000 美元一小时。"）

Jacob 最初的立场和 Swyx 完全一致——他不想提供模型选择器。"I originally came in with that. I was like 'oh yeah this is what Devon does differently' and now we have five things in the model picker including [Gemini] Fable and Opus and Astra and people want to experiment with the fancy new model."（我最初就是这个想法。我当时想的是"对，这就是 Devin 做得不一样的地方"，但现在我们在模型选择器里有五个选项，包括 Fable、Opus、Astra，人们想要实验那些花哨的新模型。）

关键转折：法律领域和工程领域对模型选择的需求完全不同：

> "I think it's [demand for model choice] definitely way less in legal than it is in engineering. But there are definitely people that just want [new model] right away and people were asking us about [Mythos] and everything. Even though I think realistically a lot of legal work does not require Mythos level intelligence."（法律领域对模型选择的需求绝对比工程领域少得多。但确实有些人就是想要最前沿的模型。人们会问我们关于 Mythos 的事情，尽管我觉得现实地说，很多法律工作根本不需要 Mythos 级别的智能。）

Jacob 坦言他们"fought introducing it for a very long time and then in the end we just kind of caved in"（我们反对引入它很久了，最后我们就是投降了）。但他警告说，"you're going to run down your credits like 10x faster"（你会以 10 倍的速度烧掉你的积分）。

**精华收获**

模型选择器看起来是一个小产品决策，但它折射出了一个重要的产品哲学张力：创始人需要抵抗"给用户一切他们要求的"这种冲动，同时又要保持足够的灵活性来满足需求。最有趣的洞察是：**模型选择需求与用户的领域专业程度成反比**。在工程领域，用户知道模型之间有什么区别，所以他们要选择权。在法律领域，用户根本不在乎，他们只关心结果。这个差异意味着，未来垂直领域代理工具应该给不同用户群体提供不同层级的模型控制粒度。

---

### 评估团队、能力热力图与"盲飞"的评估难题

**核心观点**
Legora 建立了由工程师和律师混合组成的评估团队，按法律实践领域和任务类型构建了一个"模型能力热力图"。但最大的挑战是：由于客户数据的绝对机密性，他们无法查看任何真实的用户使用轨迹，只能通过模拟数据来做评估。

**深度阐述**

Legora 有一个专门的评估团队。Jacob 描述了它的构成："It's a mix. We have engineers and then we have lawyers and it's one team. So there's like three engineers and like three lawyers right now."（这是一个混合团队。我们有工程师和律师，是同一个团队。现在大概三个工程师三个律师。）

但更关键的是他们还有一个更大的人才池叫 **法律工程师（Legal Engineers）**：

> "We have a pool of what we call legal engineers which is people that have worked in big law for like three or four years typically maybe they have a CS degree and like they're very tech forward."（我们有一个我们称之为法律工程师的人才池，这些人通常在大律所工作了三四年，可能有计算机科学学位，非常技术导向。）

这个人才群体极其稀缺。主持人惊呼："Oh my god. It's a Venn diagram. That's like our hardest person to hire for."（天哪，这是一个文氏图交集，那一定是最难招的人。）但 Jacob 强调了他们的价值："They're also such a force multiplier"（他们是一个巨大的力量倍增器）——因为这些法律工程师能够同时做评估、产品开发、客户沟通，并且"用产品每一天"。

评估方法的构建很有意思。Jacob 描述他们的评估环境几乎像是一个"RL 环境"（强化学习环境）：

> "Lawyers work in projects always more or less. So it's like here's 10,000 file data room. You're doing a due diligence. In the end a [target] report looks like this. It contains all these red flags and like it doesn't contain whatever weird stuff."（律师总是或多或少在项目中工作。所以是："这是一个 10000 文件的数据空间，你在做尽调。最终的报告应该长这样，包含所有这些红旗标志，不应该包含某些奇怪的东西。"）

然后他们在不同法律实践领域和不同任务上运行评估，生成一个"big heat map"（大的热力图），用来追踪模型能力的变化。这里有一个很重要的观察：

> "Usually they improve most stuff, but there's actually a lot of model releases where they improve some and regress in others. And that actually happens a lot more than you'd think."（通常它们会改进大多数事项，但确实有很多模型发布中，它们会在某些方面改进，在其他方面退化。这种情况发生得比你想象的要多得多。）

**但真正让 Legora 的评估工作与众不同、也格外困难的是数据的绝对不可见性。**

这是这期访谈中最核心、也可能是最被低估的洞察。Jacob 毫无保留地说：

> "One thing that's difficult for our business is we can't look at any traces basically. We can't look at any data cuz it's all super confidential and that's like extremely frustrating to work with... It's like here's an agent and it can do so many amazing things and I have no idea what people are actually doing."（我们业务中最困难的一件事是，我们基本上无法查看任何使用轨迹。我们无法查看任何数据，因为那都是高度机密的，这对工作来说极其令人沮丧。就像一个代理可以做那么多令人惊叹的事情，但我完全不知道人们实际上在用它做什么。）

主持人 Swyx 提出一个合理的疑问：你们难道不能和律所签署某种协议来查看数据吗？Jacob 的回答揭示了法律行业的特殊性：

> "The thing is like a lot of the data that they have is not even theirs. It's their clients' and it's super confidential so we can't look at it."（问题是，很多时候他们拥有的数据甚至不是他们自己的。那是他们客户的，是高度机密的，所以我们不能看。）

这就创造了一个**"盲飞"的评估困境**：你构建了一个极其强大的代理系统，但你无法看到用户如何使用它、在哪里失败、在哪里成功。这意味着评估团队必须通过模拟数据来猜测用户实际在做的事情。

对于可能的解决方案，Jacob 描述了他们的折中策略：

> "We have an eval team that's trying to approximate what we think everyone is doing and build that into eval sets... We can classify it into one of those [failure modes] and that's a helpful signal. We can classify it into the types of tasks and the practice areas also."（我们的评估团队试图接近我们想象中每个人在做的事情，然后构建评估集...我们可以将数据分类到这些失败模式中的一种，那是一个有用的信号。我们也可以分类到任务类型和实践领域。）

但即使是"改写数据"这种方案也有问题。当 Swyx 提出可以用 LLM 将真实案例改写成合成案例时，Jacob 承认存在一个区间："If you paraphrase all the way down to like three values and you pick one of them then obviously that's fine. If you just remove the names then that's maybe maybe not fine."（如果你把它改写到只剩下三四个值，然后你选其中一个，那显然是没问题的。如果你只是把名字去掉，那可能可以，也可能不行。）他们的默认做法是"pick the most safe way... we restrict ourselves as most possible because there should be no risk at all"（选择最安全的方式...尽可能地限制自己，因为不应该有任何风险）。

**延伸思考**

这个"数据不可见"的约束，是很多 B2B AI 公司——尤其是在医疗、金融、法律等高度监管行业——共同面临的困境。但它也催生了一个有趣的战略可能性：如果真实数据无法获取，那么**谁能够更好地模拟真实使用场景，谁就拥有更强的评估优势**。Legora 的做法——用法律工程师团队的领域经验来构建模拟评估集——实际上是在用人力资本替代数据资本。这在短期内可以奏效，但长期来看，随着 AI 能力的提升，"模拟数据的质量上限"可能成为瓶颈。这也是为什么 Jacob 会认真思考"购买一家律所来获取数据"这个想法——尽管他指出还存在"数据是律所的还是客户的"这个法律问题。

---

### Azure 为什么成了唯一的选择

**核心观点**
早期律所对 AWS 和 Google Cloud 完全不信任，只有 Microsoft 因为已经掌握了他们的 Office 365 和 Word 文档而被视为"可信供应商"。Legora 为了打入市场，不得不把所有基础设施都建在 Azure 上。

**深度阐述**

这一段听起来几乎有点好笑，但它极其真实地反映了法律行业对"云"的态度。Jacob 回忆起早期的情况：

> "Law firms were like AWS? No. Like no way. We don't trust AWS."（律所就像是在说"AWS？不可能。绝对不可能。我们不信任 AWS。"）

关键原因在于 Microsoft 的既有优势：

> "They were like Amazon, Google, we can't trust them with any of our data. So we basically had to host everything on Microsoft cuz they already have 365... Microsoft is an approved vendor in their mind and so we had to host everything on Azure."（他们就像在说："亚马逊、谷歌，我们不能信任他们处理我们的任何数据。"所以我们基本上必须把所有东西都托管在 Microsoft 上，因为他们已经有 365...Microsoft 在他们心中是一个经过批准的供应商，所以我们不得不把所有东西建在 Azure 上。）

律师们已经对 Word 和 Outlook（Office 365 生态）进行了安全审查，如果 Legora 建在 Azure 上，就可以搭这个信任的便车。Jacob 说这种状况在过去两三年里发生了很大变化："People understand okay we need to get on cloud... it's safe and it's probably safer than what you're doing."（人们现在理解了我们确实需要上云...它是安全的，而且可能比你自己做得更安全。）

以及一个值得注意的细节："There was also a lot more people talking about on-prem back then that's also disappeared completely."（当时还有更多人在谈论本地部署，现在完全消失了。）

**延伸思考**

这是一个典型的企业销售"准入壁垒"案例。对于任何面向高度监管行业的 AI 公司来说，基础设施的信任背书是一个必须提前解决的问题。Legora 的 Azure 选择表面上是技术选型，实际上是**市场准入策略**。它说明了一个更广泛的规律：在合规要求极高的行业，"你的技术栈是什么"可能比"你的产品有多好"更重要。而对于云计算供应商之间的竞争来说，Microsoft 在企业端的存量信任优势是一个非常被低估的护城河。

---

### OpenAI 与 Anthropic 的 DPA 难题

**核心观点**
数据保护协议（DPA）的法律约束让 Legora 只能使用极少数供应商，Gemini 因为"一站式"的多种能力（转录、语音识别等）而变得非常有价值，即使它并非最先进的。

**深度阐述**

Jacob 在解释为什么使用 Gemini 早期版本时，提到了一个非常重要的商业视角。当被问及是否使用 11 Labs 时，他明确回答："No 11 Labs for DPA reasons."（因为数据保护协议的原因不能用 11 Labs。）

DPA 就是 Data Processing Agreement（数据处理协议），它规定了哪些供应商可以处理客户数据。Jacob 的解释非常有力：

> "Our data processing agreement has very few vendors on it cuz we need to keep it super tight on where any data goes... That is one of the benefits of like a Gemini and OpenAI where they're like 'you come to us we have most of the things that you need' and that is actually very valuable."（我们的数据处理协议上只有极少数供应商，因为我们需要非常严格地控制数据流向哪里...这就是 Gemini 和 OpenAI 的一个优势，他们就像在说"来找我们吧，我们拥有你需要的大部分东西"，这实际上非常有价值。）

换句话说，即使 Gemini 的语音转录模型不是绝对最好的，但因为 Google 是一个已经通过安全审查的大型供应商，而且它提供了"一站式"的多种 AI 能力（文本、语音、转录等），所以使用它意味着你不需要把 DPA 扩展到一大堆小供应商。这大大简化了合规成本。

Jacob 还特别推荐了 Microsoft 的 Scribe 模型："They made one... Scribe. It's great. It's better than the old Gemini."（他们做了一个叫 Scribe 的模型，很棒，比老的 Gemini 要好。）

对于转录的准确性，他分享了一个令人忍俊不禁的案例：

> "There's like a certain name for a person in court and it would consistently transcribe it as condom."（法庭上有某个特定的人名/称谓，模型一直把它转录成"避孕套"。）

这个错误凸显了通用语言模型在法律领域术语识别上的不足——尤其是对于澳大利亚等地的特殊法庭用语。他的解决方案："Run an LM layer on top of it, and then you extract some keywords and then you run the transcription model again with the keywords."（在上面跑一个 LM 层，提取关键词，然后用这些关键词重新运行转录模型。）

**延伸思考**

这一节揭示了一个很深的战略洞见：**对于 B2B AI 工具来说，"够用"可能比"最好"更重要，如果"最好"意味着需要在 DPA 上增加更多供应商的话。** 因为每一个新供应商都意味着客户需要做额外的安全审查，这在法律行业可能意味着数月的延迟。Gemini 和 OpenAI 的一站式优势——即使某些能力不是最先进的——对于合规敏感型企业来说是一个巨大的竞争壁垒。这也是为什么小型专业 AI 工具（比如 11 Labs 的语音克隆）很难进入企业市场的原因之一：它们的最优性能被合规成本抵消了。

---

### Tabular View：为什么电子表格是法律 AI 的最佳形态？

**核心观点**
Tabular View 是 Legora 的核心创新之一——用电子表格的形式，将每一行对应一份文件，每一列对应一个问题，批量提取和审查成千上万份文件。这种形态让律师能够极快地获得全局视野，并且可以逐层追溯到原始文档。

**深度阐述**

这是访谈中最具产品洞察力的部分之一。主持人 Swyx 直接表示，他注意到电子表格形态在某些领域有巨大吸引力，但"somehow hasn't really spread"（不知为何并未真正扩散开来），而 Legora 是少数真正做好这一形态的公司之一。

Jacob 用一个最典型的场景来解释 Tabular View 的用途——**尽职调查（Due Diligence）**：

> "We need to review all employment contracts, all the supply contracts, all of whatever. And so employment contracts, you put 10,000 employment contracts in there... Each row is one employment contract. And then for cells, you ask questions basically... The first question, the first column might be 'what's the termination period?' And then it's going to fill out for everyone. It's 30 days or whatever it is. The next question is like 'is there an IP assignment clause or whatever.' Next one is like 'how much are we paying them?'"（我们需要审查所有雇佣合同、所有供应合同，所有这些东西。比如雇佣合同，你放进去 10000 份...每一行是一份雇佣合同。然后对单元格，你问问题。第一个问题、第一列可能是"终止期是多久？"然后它会给所有人填上——30 天或者别的什么。下一个问题是"有没有知识产权转让条款"等等。下一个问题是"我们付他们多少薪水？"）

这个系统最吸引人的地方在于，代理可以自动驱动整个流程：

> "You can also just ask the agent to do this. If you just drop 10,000 files into the agent and say like 'do a due diligence on this' it will spin up a tabular review and run all of them and wait for it to be done."（你也可以直接让代理来做这件事。如果你把 10000 个文件丢进代理说"做个尽调"，它会启动一个 Tabular Review，把所有文件跑一遍，等它做完。）

然后代理会分析结果并标出红旗——"OK，这个 CEO 的薪水高得离谱"或"有这个奇怪的奖金结构"——甚至可以进一步起草给客户的备忘录。

**为什么选择电子表格形态？** Jacob 的回答关键在于"可审查性"：

> "It's super easy to work with... it's really easy to get an overview super quickly... All of the stuff that we produce also has citations back to source documents and so you can basically review it super easily."（用它工作非常容易...你可以非常快速地获得全局视野...我们所有产出的内容都有回到源文档的引用，所以你可以非常轻松地审查它。）

在一个对准确性要求极高、错误成本巨大的行业里，这种"点击即可验证"的能力至关重要。Jacob 还提到这个系统可以扩展到**一百万个单元格**——这是一个极其惊人的技术壮举。

产品设计方面，还有一个非常巧妙的功能：**先跑前 10 行**。

> "Our tabular view actually will run the first 10 rows just check... 'Does this make sense? Did it show us what we thought it was going to show us?'... It's just really good for them to iterate quickly on the first 10 rows until they have a they're getting the results that they want and then they can go ham."（我们的 Tabular View 实际上会先跑前 10 行，让你检查一下..."这有意义吗？它展示的是我们预期的东西吗？"...前 10 行的快速迭代真的很好用，直到他们得到想要的结果，然后就可以放手去做了。）

这种"谨慎验证-大规模执行"的设计思路，完美契合了法律行业对准确性和稳健性的需求。

**延伸思考**

电子表格作为 AI 输出形态的优势，其实超越了法律领域。在金融尽职调查、医疗记录审查、政府合规审计等领域，任何需要"大量文件 + 标准问题 + 可追溯记录"的工作流，都可能受益于类似的形态。但为什么电子表格形态没有更广泛地传播？一个可能的原因是，构建一个高性能的百万规模表格系统存在显著的工程门槛——网络性能、单元格渲染、异步计算、版本管理都需要专门的优化。这使得它成为一个"看起来简单但做起来难"的产品形态，实际上构成了一个隐性的竞争壁垒。

---

### Lists 作为核心原语：可组合的产品架构

**核心观点**
Legora 的核心产品架构是建立在一组"原语"（primitives）之上的，其中最重要的是 Lists——一个类似 Notion 数据库的数据结构，它连接了代理执行、工作流自动化和协作。这种可组合的架构使得产品团队可以在极短时间内构建出定制化的新产品。

**深度阐述**

当 Swyx 问及 Tabular View 和 Agent 是否是两大核心组件时，Jacob 补充了一个关键的底层元素：

> "I probably say the big two: agent and tabular review, plus our Word add-in is also huge... But then there's this Lists thing which is like Linear for us."（我会说两大核心是：Agent 和 Tabular Review，另外 Word 插件也很重要...但还有 Lists，这就像是我们的 Linear。）

Jacob 深入解释了 Lists 的架构哲学：

> "It's a great primitive because it's essentially extremely flexible. It's like a Notion database. And so you can basically configure it for whatever you want... You can have triggers on them, automations on them. It's like a great glue to glue everything together."（它是一个很棒的原语，因为本质上它非常灵活。就像一个 Notion 数据库。你可以把它配置成任何你想要的样子...你可以在上面设置触发器和自动化。它就像一个很好的胶水，把所有东西粘合在一起。）

更值得关注的是 **Lists 让"代理群体"活了过来的能力**：

> "It's like just how you might coordinate a bunch of coding agents with Linear or some sort of task management tool. We can do it similarly with Lists and so like agents can create lists and lists can create agents and agents can read lists. And so it's like the agent swarm comes alive."（就像你会用 Linear 或某种任务管理工具来协调一堆编码代理一样，我们用 Lists 做类似的事情——代理可以创建列表，列表可以触发代理，代理可以读取列表。于是那个代理集群就活了过来。）

当主持人问人们是否对此感到兴奋或不知所措时，Jacob 的回答揭示了更深层的重要性：

> "We need the flexibility even if we don't actually expose it to the end user... it's a really fast way for us to utilize our legal engineers to basically build a lot of products extremely fast."（即使我们不把它暴露给最终用户，我们也需要这种灵活性...这是一个非常快速的方式，让我们的法律工程师来极快地构建大量产品。）

这个架构理念带来的实际成果——**法律工程师可以在客户现场即时构建定制化解决方案**：

> "You can build custom like fund management dashboards... You can basically build that on Lists with like your own generative UI and then you basically have a new product that some people are going to love."（你可以构建定制的基金管理仪表板...你可以基于 Lists 构建它，有自己的生成式 UI，然后你就有了一个新产品，有些人会真的很喜欢。）

Jacob 还讨论了一个很有意思的收购案例——他们收购英国公司 Wexler，做的是"fact intelligence"（事实智能），主要用于诉讼场景：

> "They're doing fact intelligence which is for litigation mostly... you upload a million documents for a lawsuit or whatever and then we extract facts from those with like named entities and dates... then when you have all the facts you can basically hold them up against each other and see which ones are corroborated and which ones are disagreement."（他们做的是事实智能，主要用于诉讼...你上传一个百万文件的资料库，然后提取其中带有命名实体和日期的事实...然后你可以把所有事实放在一起比对，看哪些得到佐证，哪些互相矛盾。）

这个功能和 Lists 原语的关系很明确："That's how we think about it. We have to solve so many things and so I think a lot about how do we build a core primitive that we can scale to many different end products."（这就是我们思考的方式。我们需要解决太多问题了，所以我想了很多关于如何构建一个核心原语，将其扩展到许多不同终端产品的问题。）

**核心原语清单**（Jacob 归纳）：
- **Lists**：灵活的数据结构（类似 Notion 数据库）
- **Agent**：可配置地运行在不同配置中的代理
- **Tabular View**：批量审查和提取
- **Projects**：文件容器和项目

**延伸思考**

Lists 作为核心原语的架构哲学，其实本质上是一种**平台策略**。通过保持足够的底层灵活性，Legora 能够快速构建出售给客户的新产品，甚至在客户现场进行定制。这种策略的威力在于，它把"一个产品"变成了"一个产品的生成器"。这与 Linear、Salesforce 等公司采取的"平台化"策略有相似之处，但在 AI 时代有一个新的维度：当代理可以读写这些原语时，产品本身具备了**自扩展**的能力。Jacob 甚至提出了一个更大的愿景——"Agent 作为 API"，即代理本身成为一种可以触发的执行接口，这暗示了未来产品可能走向**智能体驱动的可编程平台**。

---

### 法律工程师：最稀缺的人才类型

**核心观点**
"法律工程师"——拥有 CS 学位、在大律所工作多年、技术导向的律师——是 Legora 最难雇佣但也最具杠杆效应的人才。这类人才连接了法律领域深度和技术能力，成为产品开发和客户成功的核心力量。

**深度阐述**

Jacob 在描述法律工程师时用了一个很形象的词——"force multiplier"（力量倍增器）。这个人才群体的画像非常具体：

> "People that have worked in big law for like three or four years typically maybe they have a CS degree and like they're very tech forward and then they come to us because they want to help change the industry."（这些人通常在大律所工作了三四年，可能有计算机科学学位，非常技术导向，他们来我们这里是因为他们想帮助改变这个行业。）

当主持人 Swyx 吃惊地说这是最难的雇佣时，Jacob 补充道：

> "But they're also such a force multiplier because we can pull on them for the eval stuff and for the product development... they live this and have lived this."（但他们又是如此强大的力量倍增器，因为我们可以拉他们来做评估工作和产品开发...他们就在这里生活，并且亲身经历过这些。）

法律工程师的职责边界非常清晰——他们**不写代码**，但可以配置产品到"超级用户"级别。Jacob 对比了两类角色：

> "Legal engineers configure the product as a power user would. They don't write code. And a forward deployed engineer writes code into production basically."（法律工程师像超级用户那样配置产品。他们不写代码。而向前部署工程师基本上是在生产环境中写代码。）

这个"法律工程师"的岗位，Jacob 甚至说她/他们的价值还被低估了——当主持人在讨论"AI 初级律师"这一新角色应该被称为什么时，Jacob 提到：

> "The derogatory term of 'meat proxy' where you just like sit in front of the machine and type in something that someone else tells you to type... But I do think a very good meat proxy is just like 'well I know agents very well and I know Lora very well and I know how to... use my tools to do the thing that you need me to do. But I guess then you're not really a proxy, right? You're actually just doing meaningful work.'"（有一个贬义的词叫"肉代理"，就是你坐在机器前面，别人告诉你打什么你就打什么...但我确实认为，一个很好的"肉代理"其实是说："我很懂代理，我很懂 Lora，我知道如何...用我的工具去做你需要我做的事。"但我想，那样的话你就不再是代理了，对吧？你实际上在做有意义的工作。）

**延伸思考**

法律工程师这个角色的出现，实际上揭示了一个更广泛的行业趋势：**AI 时代正在创造一类"领域技术翻译者"的新岗位**。他们不需要写生产级代码，但需要足够的技术素养来理解并配置复杂的 AI 系统。在医疗（临床信息学家）、金融（量化分析师）、建筑（BIM 专员）等领域，类似的人才缺口正在出现。对于垂直 AI 公司来说，这类人才是"领域护城河"的重要组成部分——因为他们既是专家又是超级用户，这是通用的 AI 平台（如 ChatGPT 或 Claude）很难快速培养的。

---

### 计费模式、合伙制与法律行业的未来

**核心观点**
法律行业正在经历根本性的商业模式变革——从按小时计费向按项目计费转变。合伙制存在的原因是律所只有人力资本而无其他可累积的资产，而 Legora 的使命之一就是帮助律所"编码"其专业知识和判断力，从而建立可持续的无形资产。这将迫使激励结构发生改变。

**深度阐述**

Jacob 对法律行业未来的洞察是这期访谈中最有深度、最值得反复阅读的部分。他从一个简单的问题切入：**为什么律所采用合伙制？**

> "The partnership model kind of exists because the only type of capital that these companies have is human capital... You can't really own human capital. You can't, you know, slavery is abolished. You can't own people, but you can rent them. You can pay them money. And so partnerships essentially is a structure where you make the human capital the owners of the company so that they stay."（合伙制存在的原因，本质上是因为这类公司拥有的唯一资本就是人力资本...你不能真正拥有人力资本。你不能，你知道的，奴隶制已经废除了。你不能拥有一个人，但你可以租他。你可以付给他钱。所以合伙制本质上是一种结构，让这种人力资本成为公司的所有者，这样他们才会留下来。）

这句话相当精彩——它剥开了法律行业长期以来的神秘面纱，用最朴素的逻辑解释了合伙制的根源：既然你无法"拥有"人，那就只能通过让他们成为所有者来"留住"人。

但与制造业或科技公司不同，律所缺乏**可累积的无形资产**——因为知识和方法论存在律师的大脑中，随着他们的离开而流失。

Legora 想要改变的正是这一点：

> "What we really want to do with Lora is we actually want law firms to be able to build some sort of intangible capital, some durable capital... You can build a system that learns of how you work... A way of working that produces a really good output and that can be their IP. So it's like a way to codify the human expertise and judgment into a system."（Lora 真正想做的，是让律所能够构建某种无形资产、某种持久的资本...你可以构建一个系统，它学习你的工作方式...一种能产生非常好产出的工作方式。这可以成为他们的 IP。这就像一种将人类专业知识和判断力编码为系统的方式。）

但这会引发激励结构的问题——正如 Swyx 犀利指出的：

> "In the partnership model you just got to bring more clients and you don't want to take away time from bringing in clients to codify your information basically... partners are incentivized to codify things to build an asset for the company but right now they aren't cuz as soon as they leave the partnership they don't get any dividends from the assets that they built."（在合伙制模式下，你只需要带来更多客户，你不想从开发客户的时间中抽时间来编码你的知识...从逻辑上讲，合伙人被激励去编码知识来为公司构建资产，但目前他们没有被激励这么做，因为一旦他们离开合伙制度，他们无法从自己构建的资产中获得任何红利。）

Jacob 坦率地承认："The whole business model is all in question right now."（整个商业模式现在都处于质疑之中。）

关于计费模式的转变，Jacob 也分享了正在发生的变化，特别是美国市场：

> "We're already seeing that particular in the US that a bunch of stuff is actually being priced on a project fee and not on an hour fee. Particularly the lower end stuff... Some of it honestly is being done for free and some of it is just being priced on a flat rate."（我们在美国已经看到，很多东西实际上按项目费用而不是按小时费来计价。尤其是低端工作...有些工作实际上免费做，有些按固定费率计价。）

**关于初级律师的困境**

主持人和 Jacob 讨论了一个敏感话题——初级律师和律师助理（paralegals）是否正在消失：

> "Paralegals gone. Junior lawyers gone. I don't need them."（律师助理没了，初级律师没了，我不需要他们了。）

但 Jacob 的看法更加细致：

> "That's actually not what we're seeing... I think it's more that really good lawyers or junior lawyers are worth a lot more... A good engineer today is worth a lot more even than they were 2 years ago cuz they can produce so much more stuff. If they're good. And I think it's the same thing in legal where they can actually do a lot of really good work if they're good."（这实际上不是我们看到的...我认为真正优秀的律师或初级律师的价值要大得多...一个优秀的工程师今天的价值比两年前大得多，因为他们能产出更多东西。前提是他们优秀。我认为法律领域也是一样的，如果初级律师优秀的话，他们实际上能做出非常出色的工作。）

换句话说，AI 并没有消灭初级律师的需求，而是**加剧了人才的两极分化**——优秀的初级律师变得更有价值，因为他们能够在 AI 的帮助下扩大自己的产出；而不那么优秀的则可能面临被替代的风险。

**延伸思考**

这段讨论之所以格外有价值，是因为它触及了 AI 对职业结构更深层次的影响。在编码领域，人们看到的是类似的分化——优秀的初级工程师"提前变成高级工程师"，而平庸的初级工程师则被 AI 取代。法律领域正在经历同样的转变，但有一个额外的维度：法律工作的最终产出——判断力、策略、客户关系——恰恰是最难被 AI 替代的部分。因此，AI 加速了法律行业向"更高层次工作"的迁移，但这同时会动摇合伙制的基础，因为当律师的工作不再依赖于大量低层级人力时，"吃你猎的东西"的合伙模式就会面临根本性的挑战。

---

### 他用 Legora 做 Legora 自己的 M&A 交易

**核心观点**
Legora 用自己的产品做自身的并购尽职调查。这种"吃自己的狗粮"（dog fooding）不仅验证了产品能力，还为公司节省了大量成本，并且帮助他们发现了真正的红旗。

**深度阐述**

当 Swyx 问到 Legora 收购 Cura 公司时是否用自家产品做交易时，Jacob 的回复非常直接：

> "We do that all the time. Our legal team is... intake has been built with our legal team cuz right now we have a Slack workflow where everyone throws their stuff in."（我们一直都在这么做。我们的法律团队...Intake 就是和我们的法律团队一起构建的，现在我们有一个 Slack 工作流，每个人把东西丢进去。）

他描述了一个很有意思的内部产品演化路径：Intake 功能正是从公司内部法律团队的需求中生长出来的——工程师们在 Slack 里把东西丢出去，然后说"这很烦人"，于是他们就把这个流程产品化了。

在并购尽调方面：

> "We do a lot of the due diligence ourselves because we can do it with tabular review and other tools... We do still have counsel coming in to assess certain risk... a lot of the more menial stuff we could actually just do ourselves."（我们自己做了很多尽调工作，因为我们可以用 Tabular Review 和其他工具来完成...我们仍然会让外部律师来评估某些风险...但很多比较琐碎的工作我们实际上可以自己完成。）

最有趣的是：

> "We have had cases where we found something that's been like a red flag and then we've pulled the brakes."（我们确实遇到过这样的情况，我们发现了一些红旗，然后我们就踩了刹车。）

但当 Swyx 问是否能透露具体是什么时，Jacob 简洁地回答："No, I don't think so."（不，我觉得不行。）

**延伸思考**

这对垂直 AI 公司来说是最好的产品验证。Legora 不仅仅是把产品卖给客户，而且把它作为自己业务运营的核心工具。这产生了一个良性的反馈循环：内部使用发现产品缺陷 → 迭代改进 → 客户从中受益。但这里也隐含了一个有趣的信号：当一家 AI 公司的律师团队能够用 AI 完成大部分尽调工作时，那些传统上依赖大量初级律师进行文件审查的律所，其业务模式的可持续性确实值得重新思考。

---

### 赋能与部署："向前部署工程师"的起源与未来

**核心观点**
Legora 采用了类似 Palantir 的"向前部署工程师"（Forward Deployed Engineers）模式，帮助大型客户快速获得价值。但相比 Palantir 的经典模式，Jacob 的愿景更偏向"让法律工程师自己完成大部分定制化"的两层防御结构。

**深度阐述**

Legora 的第一位向前部署工程师是他们在纽约的第一位招聘，同时也是一位 YC 创始人。这个人才的选择标准很高：

> "Our first forward deployed engineer... was YC founder... two YC companies and worked on search at Meta."（我们的第一个向前部署工程师...是 YC 创始人...做过两家 YC 公司，在 Meta 做过搜索。）

这个角色在 Legora 的架构中扮演着关键的角色，但 Jacob 强调了两层结构的差异：

> "Legal engineers configure the product as a power user would. They don't write code. And a forward deployed engineer writes code into production basically."（法律工程师像超级用户那样配置产品。他们不写代码。而向前部署工程师基本上在生产环境写代码。）

这种分工让 Legora 能够以非常灵活的方式服务客户：

> "If it's a big client and they're super engaged... they already have tried to build something and it's failed... We'll basically staff them with legal engineers and a forward deployed engineer... They will sit with all your lawyers and teach them how to use it and figure out all the workflows."（如果是一个大客户，他们非常投入...他们已经尝试过自己构建什么东西但失败了...我们会基本配置法律工程师和一个向前部署工程师...他们会和你的律师坐在一起，教他们如何使用，搞清楚所有工作流程。）

一个有趣的细节是，这些向前部署工程师有时甚至会**被客户公司正式录用**，拿到客户公司的笔记本电脑——虽然 Jacob 说这种情况"not very often"（不经常）。不过这种灵活性意味着，当客户的数据保密要求极高时，Legora 的人员需要被纳入客户的安全边界才能工作。

关于量化规则，当被问及是否像 Palantir 那样有"四天客户现场、一天回公司贡献"的纪律时，Jacob 承认：

> "It's still early days in a lot of this... I think we will have a larger in constant circulation group of forward deployed engineers that maybe we sit with a client for like two months or whatever to build out this one thing and then they go to the next one."（在很多方面这仍然是早期...我认为我们会有一个更大的、持续流动的向前部署工程师团队，他们可能会和客户坐一两个月，把这一个事情建出来，然后再去下一个。）

**延伸思考**

"向前部署"模式的本质是**用人力来弥补产品灵活性不足**的阶段性问题。随着产品原语（如上文讨论的 Lists）变得更加灵活，法律工程师能够自己完成越来越多的定制化，这时候向前部署工程师的角色会越来越依赖。Jacob 的两层防御结构——法律工程师配置 + 向前部署工程师写代码——其实是在构建一个"从高接触、高成本到低接触、低成本"的迁移路径。这是一种相对于 Palantir 模式的演化：Palantir 的向前部署工程师几乎参与了每个项目，而 Legora 试图让这个角色逐步淡出，将定制化能力下沉到产品本身和法律工程师层面。

---

### 我们能否"只用代理"来构建产品？

**核心观点**
Jacob 提出了一个非常有趣的产品哲学问题："Can the agent be the API?"（代理能否成为 API？）他承认这还不是现实，但作为一种思考实验非常诱人：它意味着客户不需要学习你的 API 接口，只需要用自然语言告诉你的代理要做什么。

**深度阐述**

这个问题出现在讨论 API 策略的背景下。Legora 在历史上对开放 API 一直非常犹豫：

> "We've tried not to do it. We fought it for a very long time... When we're 20 engineers, it's just like we move so quickly that we can't do this."（我们一直试图不做 API。我们反对了它很长时间...当我们只有 20 个工程师时，我们移动得太快了，我们无法维护 API。）

作为 CTO，Jacob 深知维护 API 的代价："I just don't want to be slowed down by having to maintain old API versions for like a data model that we've changed."（我就是不想因为必须维护旧版 API 版本而放慢速度，尤其是对应那些我们已经改变的数据模型。）

但现在的团队规模约 100 人，情况有所不同。他开始思考更大胆的问题：

> "One thing that we're toying with is like can the agent be the API? I know it's sounds weird, but like for some of this stuff, what they actually want to do is they want to trigger certain things to happen. It could just be like, okay, you trigger the agent and ask it to do this thing. Like obviously it's way less efficient than if you just had like an API that you always hit and it's like you know but it's something that I'm toying with is like how much of our product can just be the agent versus all the other stuff."（我们在思考的一个想法是：代理能否成为 API？我知道这听起来很怪，但对于某些事情，他们实际上想要做的就是触发某些事情。你可以直接触发代理让它去做这件事。显然，这比拥有一个你一直可以调用的 API 要低效得多。但我在思考的是，我们的产品有多少可以只是代理，而不需要其他所有外围的东西。）

主持人 Swyx 指出了这个想法面临的现实挑战："Unbounded execution and cost and latency."（无限制的执行、成本和延迟。）以及确定性问题："Two out of 100 times it's going to do something whack that we didn't want it to do."（100 次中有 2 次它会做一些我们没有预料到的呆事情。）

**延伸思考**

"Agent as API"的概念其实是对软件交互模式的一种根本性挑战。传统上，API 意味着确定性和效率——你精确控制参数，获得精确结果。代理作为 API 则是将不确定性引入系统。但有一种可能的妥协方式：代理理解用户意图后生成一个结构化的确定性调用，然后在执行前先让用户确认。这可能是未来"自然语言接口"和"可靠执行"之间的桥梁。在法律的场景中，这种确认步骤实际上已经存在——律师总是会审查代理的产出。

---

### 模型评估、微调与 embedding 的 alpha

**核心观点**
Legora 在模型微调和 embedding 优化方面有巨大的潜力待挖掘。他们发现了默认 embedding 模型的不足，并建议在 RAG 重负载工作流中使用 Voyage 等定制 embedding 模型。他们还计划对开源模型进行特定任务的微调，特别是法律研究中的检索类任务。

**深度阐述**

关于模型微调，Jacob 的立场很务实。他坦承 Legora 历史上没有做过微调，但现在开源模型变得非常有能力，所以会在特定子任务上做微调：

> "We haven't fine-tuned any models up until now. I think now in the past few months open weights models have become extremely capable and so we will do it for certain tasks where we think there's a huge delta between what a frontier model can do at the cost and latency versus what we think a post-trained model can do."（到目前为止我们还没有微调过任何模型。我觉得在过去几个月，开源权重模型变得非常有能力了，所以我们会为某些任务做微调，这些任务中我们能看到前沿模型在成本和延迟方面的能力和微调后的模型之间存在巨大差距。）

一个具体的例子是**法律研究**：

> "Legal research is a great example... It's a fan out retrieval problem and you can make a really effective model do that those queries super quickly and super cheaply at low latency."（法律研究是一个很好的例子...它是一个分散检索的问题，你可以让一个高效的模型以极低的延迟、极快的速度、极低的成本来执行这些查询。）

但 Jacob 也非常清醒——他不试图和 Anthropic 竞争主力模型：

> "We're not trying to like train our own [frontier model] to like be the main agent. I don't think that's like a we won't win that, versus Anthropic. Most likely."（我们并不是试图训练自己的前沿模型来担任主力代理。我觉得相对于 Anthropic，我们不会赢。很可能不会。）

对于 embedding 优化，Jacob 的态度更加积极。当 Swyx 提到"default embeddings... you're leaving a lot on the table"（默认的 embedding...你还留下了很多可以优化的空间）时，Jacob 完全赞同：

> "Basically don't take default embeddings even like open embeddings, Gemini embeddings doesn't matter. Customize your embeddings."（基本上不要用默认的 embedding——无论是 open embedding 还是 Gemini embedding 都不行。定制你的 embedding。）

唯一需要注意的是多语言支持："We serve so many languages... Europe is the king of this."（我们服务很多语言...欧洲在这方面是王者。）

**延伸思考**

这段关于 embedding 的讨论很重要，因为它提醒我们：即使在大模型的进步呈指数增长的今天，RAG 系统中的基础组成部分（如 embedding 和检索策略）仍然是高度可优化的。许多公司过度关注模型前沿能力的提升，而忽视了检索质量对最终产出的巨大影响。对于法律这种对精确度要求极高的领域，embedding 质量的差异可能是致命的——一个错误的检索结果可能导致完全错误的法律解读。Legora 对这些基础层的关注，正是成熟垂直 AI 公司和"简单套壳"之间的关键区别。

---

### 引用系统：如何让律师信任 AI 的输出

**核心观点**
Legora 构建了一个多层次的引用系统，使所有产出都可以追溯到确切的源文档位置（甚至包括 PDF 中的边界框定位），从而在最大程度上减少幻觉并建立用户信任。

**深度阐述**

幻觉（hallucination）是法律领域最致命的 AI 失败模式。Jacob 描述了他们解决这个问题的方式：

> "We have a system of a citation system where we basically check what they're writing has a link. So the user has a link they can click and it highlights with a bounding box like in the PDF or wherever where this information was taken from."（我们有一个引用系统，基本上检查他们写的内容是否都带有链接。用户可以点击链接，它会在 PDF 中用边界框高亮显示原始位置，你就能知道信息来自哪里。）

这个系统最强大的是**多层级追溯**能力：

> "If the agent writes something based on a tabular review, it can cite the cell in the tabular view or the row in the tabular view. So you can actually click multiple layers down and find sort of validate it all the way up."（如果代理基于 Tabular Review 写了某些东西，它可以引用 Tabular View 中的特定单元格或特定行。所以你实际上可以逐层向下点击，一路追溯来验证所有信息。）

当 Swyx 问律师是否真的在验证这些引用时，Jacob 的回答很坦率：

> "Initially work, but now exactly like hallucinated links to Supreme Court. They don't care. That happens."（最初他们确实会去验证。但现在，像那些指向最高法院的虚构链接，他们根本不在乎了。这种事确实发生了。）

他将这个现象类比于编程领域：

> "It's like coding, you know? You have engineers that just don't give a [care] and just like send agents and you have people that like sit and read every comma. Same."（这就像编程，你知道的？有些工程师根本不在乎，直接把代理发出去；也有些人会坐下来读每一个逗号。一样的。）

但关键的是，律师知道哪些地方应该重点检查：

> "They probably just know, 'This is the thing. These are the things that are important. Let me just double check these things. And these sound reasonable, so it's probably fine.'"（他们可能知道："这些是关键的事情。让我来核对这些。这些听起来合理，应该没问题。"）

**延伸思考**

引用系统的设计是一个很好的"技术信任"案例。它说明了一个重要原则：在 AI 输出中使用**结构性保障**——例如强制引用、可追溯链路——可能是比"更好的模型"更有效的方式来建立用户信任。因为模型能力的提升并不能消除幻觉，而一个可验证的结构性保障能让用户快速发现和纠正错误。对于法律这类高风险领域，"可验证"甚至比"更准确"更重要。因此，垂直 AI 产品的核心竞争力之一，就是理解其领域中"验证"的特殊语义和方法，并据此设计产品。

---

### "20 人斯巴达"vs 100 人现实：规模化的悖论

**核心观点**
Jacob 曾经有过一个强烈的愿景——用 20 个工程师永远保持精简，以少胜多。但现实让他明白，在竞争激烈的市场中，必须扩张到 100 人甚至更多。他的核心任务是找到一种方法，在看似做很多事情的同时，只构建少数核心原语。

**深度阐述**

这是 Jacob 个人反思最深刻的部分之一。他描述了自己心态的演变：

> "I pulled up this slide of the 300 Spartans and like from the movie and I was like 'we're just going to be 20 engineers for the rest of the company's history and like we're going to beat everyone who's much bigger' and we're 100 engineers now and it feels like we're way too small."（我调出了一页 PPT，是《300 勇士》里的斯巴达战士，我当时说："我们要以 20 个工程师的规模度过公司整个历史，我们要打败那些大得多的对手。"而现在我们有 100 个工程师了，感觉还是太小了。）

这段话透露出创始人在增长和克制之间的撕扯。他最初想保持"puritan"（清教徒）式的克制：

> "I could be a Puritan and just be like 'no we have to stay 20 people and we can only build whatever' but then we just lose and people would go elsewhere."（我可以做一个清教徒式的人，说"我们必须保持 20 个人，我们只能做这些"，但那样我们就会输，人们就会去别的地方。）

于是他的角色转变成：

> "My job is to figure out how do I build a system where we can build a lot but actually only... where the customer feels like we've built so much stuff but we've actually only built a few things."（我的工作是如何构建一个系统，让我们实际上只构建了很少的东西，但客户觉得我们构建了非常多的东西。）

**延伸思考**

这是每个快速增长的技术公司都会遇到的问题：如何在"保持产品焦点"和"满足市场多样化需求"之间取得平衡。Jacob 的答案是回归原语策略——用几个灵活的基础组件构成一个产品平台，让用户感觉到丰富性，但保持底层架构的简洁。这与亚马逊早期的 API 化转型、以及现代流行的"可组合架构"理念一脉相承。但从更深层次来说，这是一个关于**如何保持工程速度为战略优势**的问题：若你只有 20 人，你可以在产品内快速迭代；若你有 100 人，你需要确保基础设施足够灵活，让并行开发不产生冲突。100 人的挑战是保持 20 人的敏捷性。

---

## 精华收获

1. **数据不可见是最大的难题，也是最大的机遇**。法律行业的数据是"客户的数据"，不是"律所的数据"。这意味着 AI 工具提供商无法访问真实的用户使用轨迹，必须完全依赖模拟数据做评估。谁能构建更接近真实场景的模拟评估，谁就在这个无法直接观测的市场中获得优势。

2. **原语 > 功能**。通过构建 Lists 这一灵活的核心数据结构，Legora 用少数几个原语支撑起大量产品功能。客户感受到的是丰富性，背后其实是极简的架构。在 AI 时代，产品的可组合性比功能数量更重要。

3. **电子表格是强大却被低估的 AI 输出形态**。当需要大量文件 + 标准问题 + 可追溯验证时，电子表格形态具有天然优势。它提供了全局视野、易于评审、支持协作，并且能通过引用逐层追溯。

4. **"一站式"的能力比"最优"的能力更重要**。在合规敏感的 B2B 市场，DPA 约束意味着减少供应商数量本身就是巨大的价值。Gemini 的转录模型不是最好的，但如果它让你不需要增加额外的数据处理协议，那它就是更好的选择。

5. **法律工程师是最稀缺但最有杠杆效应的人才**。拥有 CS 学位的律师，既能做评估、又能做产品、还能与客户深度协作。对于垂直 AI 公司来说，这类"领域技术翻译者"是护城河的重要组成部分。

6. **AI 加剧了初级人才的两极分化**。优秀的初级律师（工程师同理）因为 AI 的放大效应而变得更有价值，而不那么优秀的则面临更大的替代风险。AI 不是消灭了初级岗位，而是重新定义了"优秀"的标准。

7. **合伙制的本质是"用所有权留住人力资本"**。AI 使得知识可以被编码为系统，从而开始创造律所历史上从未有过的无形资产。这将对法律行业的商业模式产生深远影响。

8. **保持小团队的战略性价值**。Jacob 的"20 人斯巴达"梦想虽然被现实修正，但其背后的核心原则——通过原语设计保持产品的可扩展性——仍然是他领导 Legora 的核心策略。

---

<!-- TLDR: 法律 AI 的未来在于用少数核心原语支撑无限产品，同时学会在数据不可见的世界中构建有效的评估系统。 -->
<!-- TAGS: 法律科技, AI代理, 产品架构, 数据隐私, 垂直SaaS, 评估系统 -->  <!-- RATING: 5 -->
