---
title: "⚡️Context Graphs: according to the authors — Jaya Gupta, Ashu Garg, Foundation Capital"
channel: "Latent Space"
published: "2026-02-04"
source_url: "https://www.youtube.com/watch?v=zP8P7hJXwE0"
video_id: "zP8P7hJXwE0"
duration: "33:44"
---

# ⚡️Context Graphs: according to the authors — Jaya Gupta, Ashu Garg, Foundation Capital

- **Channel:** Latent Space
- **Published:** 2026-02-04
- **Source:** https://www.youtube.com/watch?v=zP8P7hJXwE0

## 版本

- [原始文稿](2026-02-04-⚡️context-graphs-according-to-the-authors-—-jaya-gupta,-ashu-garg,-foundation-capital-zP8P7hJXwE0.transcript.md)

# 内容深度重构与阐述

## 材料信息

- **标题**：⚡️Context Graphs: according to the authors — Jaya Gupta, Ashu Garg, Foundation Capital
- **作者/来源**：Latent Space (YouTube 频道), Jaya Gupta, Ashu Garg (Foundation Capital)
- **类型**：YouTube 视频字幕
- **关键元数据**：视频时长约 30 分钟
## 开篇引入

在人工智能飞速发展的今天，我们正站在一个新时代的门槛上。AI Agent，这些能够自主执行任务的智能体，正从概念走向实际应用。然而，当它们真正进入企业生产环境时，一个核心问题浮出水面：如何让这些智能体不仅能“做什么”，更能理解“为什么”？这正是“上下文图谱”（Context Graphs）这一概念诞生的核心驱动力。本文将深入探讨由 Foundation Capital 的 Jaya Gupta 和 Ashu Garg 提出的上下文图谱理论，揭示它如何成为下一代企业AI应用的核心，以及它将如何重塑我们对数据、决策和自动化模式的理解。通过对原始材料的深度解读，我们将超越表层信息，探寻这一创新框架背后的深刻洞察和未来潜力。

## 详细内容

### 早期AI浪潮与上下文图谱的萌芽 `[00:00-03:40]`

**核心观点**

三年前的AI领域尚处于Langchain、Llama Index和Perplexity等工具兴起的初期，关注点主要集中在基础的AI应用和Agent概念的萌芽，而“上下文”的概念在当时并未被明确提出。然而，随着AI Agent在企业生产环境中的应用日益深入，人们逐渐意识到，缺乏对人类决策背后“为什么”的理解，是Agent无法可靠执行复杂企业任务的关键瓶颈，这促使了上下文图谱概念的诞生。

**深度阐述**

视频开篇，主持人与Jaya Gupta和Ashu Garg回顾了三年前AI领域的景象。Jaya提到，大约三年前，她参加了Langchain的黑客马拉松，当时Factory项目刚刚诞生。那个时期，AI领域的主要焦点是Chat GPT的出现，以及Langchain、Llama Index和Perplexity等早期工具的兴起。这些工具主要致力于将“上下文”信息输入到大型语言模型（LLMs）中，但当时对“上下文”的理解还停留在相对基础的层面，例如如何有效地将文本信息传递给模型。Agent的概念虽然有所讨论，但尚未像今天这样成为主流。Jaya强调，当时的AI黑客马拉松更多是关于如何利用这些新工具进行实验，而不是深入思考“上下文”的复杂性。

Ashu Garg则分享了他更早期的AI经历，他曾在2006年领导微软的机器学习团队进行广告定位。这段经历让他意识到，在完成“为灵魂更好的事情”后，他转向了应用AI领域。他与Yan Stoka共同创立了Canviva，一家专注于应用AI的公司。然而，他们很快遇到了数据基础设施的挑战，这促成了Databricks和AnyScale等公司的诞生，也为后续一系列应用AI公司奠定了基础。这表明，在AI发展的早期，数据管理和基础设施一直是核心挑战，而上下文图谱正是试图在更高维度上解决这一挑战。

随着时间的推移，特别是在过去6到12个月里，Foundation Capital与他们的投资组合公司紧密合作，开始深入思考一个关键问题：当AI Agent进入生产环境时，究竟缺少了什么？尽管2023年被认为是Agent之年，涌现了Cloud Code、Devin、Sierra、Decagon等Agent产品，并且模型能力也大幅提升，但这些Agent在执行企业级任务时仍然不够可靠。Ashu和Jaya意识到，这些Agent缺乏对人类决策背后“为什么”的理解。它们能够执行任务，但无法捕捉到诸如“为什么会批准例外情况”、“冲突是如何解决的”以及“哪些先例被应用”等关键信息。正是这种对人类推理和决策逻辑的缺失，促使他们在2023年12月开始撰写关于上下文图谱的文章，并在年底前发布。

**重要原话**：

- "I cannot say I was thinking about context things at that time. I was just thinking about like and I think it was actually like before even agents took off like it was like literally right after chat PT and I think the only things that really existed were Langchain, Llama Index and like Perplexity were like sort of the three companies that came out right after." - Jaya Gupta `[01:00]` (我当时并没有考虑上下文的事情。我只是在思考，那甚至是在Agent兴起之前，就在Chat GPT之后，当时真正存在的只有Langchain、Llama Index和Perplexity这三家公司。)
- "What is actually missing as AI agents move into production? Like if you think back like everyone said 2025 would be the year of agents and and in some ways it was... but I think you know we when you think deeply about like what is missing you you kind of realize like you know that they still can't reliably do enterprise work some of these agents." - Jaya Gupta `[03:00]` (当AI Agent投入生产时，究竟缺少了什么？如果你回想一下，每个人都说2025年将是Agent之年，在某些方面确实如此……但当你深入思考缺少什么时，你会意识到这些Agent仍然无法可靠地完成一些企业工作。)
- "One of the reasons is that because they don't actually capture like why we do certain things like and the human reasoning behind decisions. And so like specifically what do we mean like why exceptions are granted, how conflicts are resolved, what precedents are applied." - Jaya Gupta `[03:20]` (其中一个原因是它们实际上没有捕捉到我们做某些事情的“为什么”，以及决策背后的人类推理。具体来说，我们指的是为什么会批准例外情况，冲突是如何解决的，以及哪些先例被应用。)
**延伸思考**

从早期AI工具的“上下文输入”到上下文图谱的“决策为什么”，这反映了AI从“执行”到“理解”的进化需求。这不仅仅是技术上的进步，更是对AI在复杂人类社会和企业环境中扮演角色的深刻反思。

### 上下文图谱的定义与核心构成 `[03:40-08:45]`

**核心观点**

上下文图谱（Context Graph）被定义为企业中所有决策背后“为什么”的机构记忆，其核心单元是“决策轨迹”（Decision Trace）。它是一种中间抽象层，旨在捕捉Agent或Agent系统执行业务流程时，包括人类参与在内的所有决策步骤、例外、覆盖和跨系统上下文，从而为Agent提供学习和改进的依据。

**深度阐述**

Ashu Garg进一步阐述了上下文图谱的战略意义。他指出，在过去一年中，随着大量知识产权被封装在模型本身中，应用AI公司、Agent系统公司和记录系统公司面临着一个关键问题：它们的可防御性护城河在哪里？通过与Animesh（PlayerZero）、Ishan（Olive）、Kabir等创始人进行深入讨论，他们发现大家都在用不同的语言描述同一个问题，最终洞察到存在一个“中间抽象层”，即上下文图谱。他们认为，这个中间抽象层——决策轨迹的积累——将在未来十年中变得至关重要，成为最成功的应用公司或Agent系统公司的持久层。更重要的是，他们相信上下文图谱是独特且新颖的，并且不适合现有巨头来主导。

随后，视频深入探讨了上下文图谱的具体定义。Ashu强调，上下文图谱是“所有决策背后‘为什么’的机构记忆”。这个核心单元被称为“决策轨迹”（Decision Trace）。当一个Agent或Agent系统执行业务流程时，它会经历一系列步骤，其中可能多次涉及人类参与。决策轨迹就是追踪这些步骤、例外情况、覆盖（overrides）以及跨系统上下文（这些上下文可能存在于结构化数据、非结构化数据甚至人类的头脑中）的过程。当这些决策轨迹被聚合起来，并能够被Agent学习和利用以改进其性能时，这个“织物”就形成了上下文图谱。

Jaya补充道，上下文图谱是由大量的决策轨迹组成的，并且在实现时，必须能够从中提取洞察力，使其能够被机器（Agent）使用。主持人提出疑问，这听起来像是一个非常宏大的概念，目前是否已经有公司成功实现？Jaya坦言，在Twitter和LinkedIn上，有成千上万的人声称已经实现，但她认为真正实现的公司可能只有几十家。她特别提到了PlayerZero，认为他们是少数几个拥有某种版本上下文图谱的公司之一。她还指出，未来会有多种不同的实现方式，例如Glean、Atlan（数据目录公司）、Harvey（应用层公司）、Octa（安全公司）等都在尝试构建自己的版本。然而，她强调，目前真正大规模部署的例子非常少，因为这是一个非常新的概念。

**重要原话**：

- "There is an intermediate abstraction which we call context graphs which is the accumulation of decision traces and this intermediate abstraction in our opinion will be the one that will matter the most over the next decade it's the enduring layer for the most successful application companies or systems of agents companies." - Ashu Garg `[04:20]` (我们称之为上下文图谱的中间抽象层是决策轨迹的积累，我们认为这个中间抽象层将在未来十年中变得最重要，它是最成功的应用公司或Agent系统公司的持久层。)
- "At its essence, a context graph is the institutional memory of all the why behind the set of decisions. And we think of that core unit as a decision trace." - Ashu Garg `[06:00]` (从本质上讲，上下文图谱是所有决策背后“为什么”的机构记忆。我们认为其核心单元是决策轨迹。)
- "When you aggregate decision traces in a way that you can then learn from them as an agent and you can use them to make the agent better, that's that fabric or becomes what we call the decision graph." - Ashu Garg `[06:30]` (当你以一种Agent可以从中学习并利用它们来改进Agent的方式聚合决策轨迹时，那个“织物”就变成了我们所说的决策图谱。)
- "I would say that if you look at Twitter today and you look at LinkedIn, thousands of people claim to have it working. I've had like maybe 30." - Jaya Gupta `[07:40]` (我想说，如果你今天看Twitter和LinkedIn，成千上万的人声称已经实现了。我大概只见过30个。)
**视觉/结构信息描述**

在讨论上下文图谱的定义时，视频中可能展示了幻灯片，其中包含“Context Graph”和“Decision Trace”的文字定义，并可能通过箭头或层级结构图示了它们之间的关系，例如上下文图谱由多个决策轨迹组成。

**延伸思考**

上下文图谱作为一种“中间抽象层”，其价值在于连接了底层的执行动作（how）和上层的决策意图（why）。这使得AI Agent能够从简单的任务执行者转变为能够理解并适应复杂业务逻辑的智能伙伴。

### 上下文图谱的实现与技术考量 `[08:45-14:30]`

**核心观点**

上下文图谱并非单一的技术架构，而是一个框架，其具体实现方式将因用例和场景而异。它将涉及跨职能、跨流程的数据整合，并专注于捕获实际操作性决策的“正确路径”。现有Agent系统初创公司在业务流程自动化中的“编排路径”上具有独特优势，能够更好地捕获决策轨迹并构建上下文图谱。

**深度阐述**

Ashu强调，不应将上下文图谱视为一种特定的技术架构，而应将其视为一个框架。这意味着会有多种技术实现方式，并且这些实现会随着时间演进。不同的公司会根据其用例和具体情况，采用不同的组件、数据库和数据结构来构建上下文图谱。他们观察到，在那些正在进行革命性工作的Agent系统公司中，构建上下文图谱是一个共同的主题，尽管它们仍处于早期阶段，并且复杂程度各不相同。

主持人询问，上下文图谱是否存在理想的数据结构，例如是否类似于知识图谱中的三元组实体。Jaya认为目前没有单一的理想数据结构，因为这更多是一个框架。她预测，未来会有许多公司围绕“决策轨迹”的概念进行创新，例如在安全治理领域，以及重新构想各种应用，如CRM系统。她还提到，图数据库领域的人可能会认为这正是他们一直在做的事情。

Ashu进一步指出，构建上下文图谱的公司有一些共同点：

1. **跨职能、跨流程**：决策轨迹往往需要整合来自多个现有记录系统的数据。
1. **专注于“正确路径”（Right Path）**：上下文图谱捕获的是实际的操作性决策，而不是分析性决策。它关注的是业务流程中实际发生的每一步，包括人类的干预和例外情况。
1. **现有Agent系统初创公司的优势**：这些公司不受现有业务流程或数据存储的束缚，它们处于业务流程自动化的“编排路径”上。这种位置使它们能够独特地捕获决策轨迹，进而构建上下文图谱。
主持人对“系统Agent”这一术语的广泛性提出疑问，并询问其起源。Ashu解释说，“系统Agent”是指拥有Agent集合的公司，这些Agent旨在自动化一个或一组业务流程。这个术语最初是为了区分更基础的聊天机器人系统。当一个系统是多Agent、多玩家模式，涉及人类参与，并驱动整个业务流程中的决策时，他们称之为“系统Agent”。这些系统Agent构建的底层护城河就是上下文图谱，它们通过捕获自身执行的决策轨迹来构建图谱。

随后，讨论转向了“读路径”（Read Path）与“写路径”（Right Path）的区别。主持人提到，他理解的“读路径”更多是关于数据读取的性能和延迟，而“写路径”则涉及数据写入。Ashu澄清说，当他们谈论“读路径”与“写路径”时，指的是分析系统（如数据仓库和记录系统）通常捕获的是决策的“终点”——即“发生了什么”（例如公司收入、交易规模、折扣等）。它们知道结果，但不知道过程。而Agentic系统或Agent系统则捕获的是“步骤序列”——即“做了什么”。

他以PlayerZero为例，详细解释了“写路径”：一个支持工单进来，Agent首先进行分析，运行查询。如果需要，人类会被拉入循环，进行进一步查询。所有这些查询最终导致一个决策或假设，例如问题的根本原因和修复方案。这个从工单开始，经过自动分类、假设生成、修复，最终转化为代码并部署到生产环境的整个循环，就是他们所说的“写路径”。这与数据库中狭义的“读/写路径”有所不同，因为这里涉及的是代码的生成和部署，是实际的业务操作。

**重要原话**：

- "Don't think of context graphs as a technology architecture, think of it as a framework and there will be multiple technology implementations and those will evolve over time." - Ashu Garg `[09:00]` (不要将上下文图谱视为一种技术架构，而应将其视为一个框架，将会有多种技术实现，并且这些实现会随着时间演进。)
- "The common theme across these systems of agent companies that we think are doing revolutionary stuff is they are building a context graph." - Ashu Garg `[09:40]` (我们认为正在进行革命性工作的这些Agent系统公司的一个共同主题是它们正在构建上下文图谱。)
- "Existing systems of agents, startups actually have a very unique advantage because they're not bound by a business process. They're not bound by an existing uh data store. They're in the orchestration path." - Ashu Garg `[12:00]` (现有的Agent系统初创公司实际上拥有非常独特的优势，因为它们不受业务流程的束缚，也不受现有数据存储的束缚。它们处于编排路径上。)
- "Analytical systems which are in the read path are ultimately and you ultimately have to write to an analytical system... What they don't know so that's because that's ultimately stored in some analytical system whatever that system might be. And to that extent systems of records are more analytical in nature than they are in the right path where aentic systems or systems of agents actually capture the sequence of steps. What did you do?" - Ashu Garg `[13:30]` (处于读路径的分析系统最终，你最终必须写入分析系统……它们不知道的是，因为那最终存储在某个分析系统中，无论那个系统是什么。从这个角度来看，记录系统本质上更具分析性，而不是处于写路径，而Agentic系统或Agent系统实际上捕获的是步骤序列。你做了什么？)
**视觉/结构信息描述**

在讨论“读路径”与“写路径”时，幻灯片可能通过对比图或流程图清晰地展示了两种路径的不同，例如“读路径”指向数据仓库和分析系统，而“写路径”则描绘了从工单到代码部署的完整业务流程。

**延伸思考**

“读路径”与“写路径”的区分是理解上下文图谱核心价值的关键。它强调了从仅仅记录结果到记录完整决策过程的转变，这对于AI Agent的自主学习和决策至关重要。

### 上下文图谱与现有系统的共存及挑战 `[14:30-20:00]`

**核心观点**

上下文图谱的实现将需要新的平台，但这些平台必须与现有系统（如Slack、GitHub）共存。现有系统往往无法有效编排整个业务流程，且大量有价值的非结构化数据（如邮件、Slack对话、Zoom会议）分散其中。构建上下文图谱的关键挑战在于如何从这些非结构化数据中提取有价值的洞察，并解决数据治理和隐私问题。

**深度阐述**

主持人提出一个关键问题：人们是否愿意为上下文图谱使用一个独立的平台，还是会继续依赖GitHub、Slack等现有工具？Ashu认为，新的平台是必然的，但它们必须与现有系统共存。例如，用户可以通过Slack与PlayerZero进行交互，因为不可能一夜之间取代所有现有系统。他指出，现有系统（如Slack、邮件）虽然承载了大量数据，但它们无法有效编排整个业务流程。即使是像Salesforce这样的记录系统，也主要为结构化数据设计，而实际的业务数据往往分散在邮件、Slack等非结构化渠道中。Ashu甚至认为，邮件是大多数组织中排名第一的记录系统。

然而，邮件和Slack只是以“数据块”（blob）的形式捕获数据，这些数据是“暗数据”（dark data）。一个拥有真正上下文图谱的Agentic系统，将能够从邮件、Salesforce、账户管理系统、对话和Zoom会议等所有来源中捕获适当的数据片段，无论是结构化还是非结构化。他强调，大部分价值实际上存在于非结构化数据中。

构建上下文图谱的挑战在于如何解析这些非结构化数据，以捕获价值和洞察。如果仅仅上传所有的Zoom会议记录，只会产生大量噪音。因此，上下文图谱很可能由小型模型组成，利用这些数据训练一系列模型，使其成为上下文图谱的一部分。例如，PlayerZero的数据集更多是半结构化的，如代码、工单和可观测性数据，这些数据具有更多的隐含结构。在这种情况下，上下文图谱的实现可能更接近传统的图结构，或者是在关系型数据库之上构建一个图层。

视频随后讨论了社区对上下文图谱的一些“反驳”或不同意见。Jaya指出，一个常见的观点是，我们无法真正捕获决策的“为什么”，只能捕获“如何”——即一系列动作和交互。Glean公司就明确表示他们只捕获“如何”。Jaya承认在某些情况下这是事实，但她也认为存在一种方法可以重建“为什么”，即使是“部分的为什么”。她提到Animesh的博客文章中也讨论了这一点。她认为，在AI Agent出现之前，人类做出决策，现在Agent需要访问这种记忆。此外，LLMs的出现使得这种捕获变得更加可行。在LLMs之前，需要人类手动结构化每个决策，但没有人愿意做这项繁琐的工作（例如Salesforce中的笔记框通常是空的）。

主持人开玩笑说，未来可能需要让员工佩戴BCI设备来读取思想。Jaya分享了一个投资组合公司CEO的例子，他的团队佩戴一种手表，可以自动记录数据并连接到日历。这引出了数据隐私和治理的关键问题。Ashu强调，数据治理和敏感数据管理是构建上下文图谱成功的关键。他提到了Skyflow这家投资组合公司，他们正在开创性地解决PII（个人身份信息）和敏感数据管理问题。

另一个常见的“反驳”是，上下文图谱不过是“元数据3.0”或“数据网格”（Data Mesh）的又一个新版本。Jaya认为，新的类别之所以出现，是因为出现了值得存储的新价值单元。上下文图谱的不同之处在于，决策轨迹是在执行路径中捕获的，而不是预先定义或事后通过ETL重建的。它们是Agent工作过程中自然产生的副产品，这在架构上与传统的元数据层有所不同。此外，传统的元数据和本体论需要大量的前期建模工作和咨询，而上下文图谱则更加有机。

**重要原话**：

- "These new platforms whether it's player zero or or olive or tar or pick pick your favorite one they will have to coexist with existing systems and so the system of engagement may end up being Slack." - Ashu Garg `[15:00]` (这些新平台，无论是PlayerZero、Olive还是其他你喜欢的，都必须与现有系统共存，因此交互系统最终可能是Slack。)
- "Most of the value is actually in the unstructured data. And this is part of why s context graphs are so hard to build that you have to figure out how to parse the unstructured data in a way that you capture value and insight." - Ashu Garg `[16:40]` (大部分价值实际上存在于非结构化数据中。这也是为什么上下文图谱如此难以构建的部分原因，你必须弄清楚如何解析非结构化数据，以捕获价值和洞察力。)
- "One of the things that we keep hearing is like well you actually can't capture the real why and like you can and you can only capture the how." - Jaya Gupta `[18:00]` (我们一直听到的一种说法是，你实际上无法捕捉到真正的“为什么”，你只能捕捉到“如何”。)
- "New categories I think they emerge when there's a new unit of value worth you know storing and I think the difference here is that decision traces are sort of captured as part of the execution path and not sort of defined up front in all these is like workshops and reconstructs it after the fact via ETL and they're more like emerging as a byproduct of agents doing work." - Jaya Gupta `[19:30]` (我认为新类别的出现，是因为出现了值得存储的新价值单元。这里的区别在于，决策轨迹是在执行路径中捕获的，而不是在所有这些研讨会中预先定义，或事后通过ETL重建的，它们更像是Agent工作过程中产生的副产品。)
**个人感受**

关于“为什么”和“如何”的讨论，以及数据治理和隐私的挑战，触及了AI伦理和实际应用的核心。这不仅仅是技术问题，更是社会和组织层面的复杂考量。

**延伸思考**

如何有效地从非结构化数据中提取“为什么”的洞察，是上下文图谱技术实现的关键突破口。这可能需要结合更先进的自然语言处理、知识图谱构建和因果推理技术。

### 上下文图谱的未来展望与预测 `[20:00-26:00]`

**核心观点**

上下文图谱将以有机、垂直的方式在企业中涌现，而非通过一个统一的、解决所有问题的“通用上下文图谱”来实现。未来一年内，我们将看到数百个上下文图谱投入生产，并形成明确的“上下文图谱技术栈”。届时，讨论的重点将从“是什么”转向“如何从上下文图谱中提取价值”。

**深度阐述**

主持人提到“数据网格”的概念，并询问上下文图谱是否与之类似。Ashu认为，数据网格的定义非常宽泛，上下文图谱可以被视为数据网格的一种形式。然而，他不同意“一个大型企业拥有一个通用数据网格”的观点。他坚信，上下文图谱将有机地涌现，因为它们必须从特定任务或业务流程的自动化中产生。没有人能够或愿意去捕获组织中所有的决策轨迹，并将其放入一个通用的上下文图谱中，这就像“解决世界饥饿问题”一样，想法很好但难以实现。

他们的核心论点是，上下文图谱将有机地出现，因为随着流程自动化，人类作为“循环中的人”（human in the loop）被激励去提供大量的训练数据。决策背后的“为什么”来自于人类在现有业务流程自动化中采取的行动。例如，PlayerZero为从代码测试到生产部署的整个代码流程构建上下文图谱；Olive为销售流程构建上下文图谱。这些是公司中不同的业务流程，没有理由将它们的数据或上下文图谱放入一个通用的图谱中。

Ashu还提到了Glean的Arvin的观点，Glean是一个强大的聊天机器人，允许人们在其之上构建Agentic应用。但他认为，真正深层次的跨职能、跨流程自动化问题将由专注于解决这些问题的公司来解决，这些公司可以被称为“垂直特定”的公司。他以其合伙人Joanne的公司Tenor为例，该公司正在自动化专业医疗保健诊所的患者入院流程，这本质上是为专业医疗保健诊所构建的“CRM”，但它捕获了这些决策轨迹并构建了上下文图谱。Ashu和Jaya每天都在思考如何识别哪些用例、业务流程和垂直领域将在未来十年拥有最深的护城河。他们希望通过投资组合中的一百家拥有上下文图谱的公司，来构建一个“通用上下文图谱”。

在视频的最后，主持人要求Jaya和Ashu对未来一年做出可证伪的预测。Jaya开玩笑说这是“Alpha信息”，不确定是否能透露。Ashu则给出了三个大胆的预测：

1. **上下文图谱的普及**：一年后，将有数百个上下文图谱在生产环境中大规模运行。
1. **技术栈的标准化**：上下文图谱的底层基础设施技术栈将得到明确定义，尽管会有不同的变体和风味。就像曾经的“现代数据栈”一样，未来将出现“上下文图谱栈”，并且其重要性和价值将是前者的十倍。
1. **价值提取成为焦点**：关于“什么是上下文图谱”和“决策轨迹为何重要”的争论将消失，取而代谱，问题将变为“如何从上下文图谱中提取价值”。一旦拥有上下文图谱，公司将开始思考如何利用它来进一步自动化。自动化是一个螺旋上升的过程：从上下文图谱中提取的价值越多，就能实现更多的自动化；自动化越多，捕获的决策轨迹就越多，从而进一步丰富上下文图谱。最优秀的公司将在12个月后讨论如何加速这个飞轮。
**重要原话**：

- "We don't actually believe that that will be the case. We think context graphs because they have to emerge from the automation of a specific set of tasks or business processes like no one's going to do or can do the work to say let me capture all the decision traces in organization and put them in one universal context graph sounds a little bit like solving world hunger and it's a good idea but very hard to implement." - Ashu Garg `[21:00]` (我们不认为会是那样。我们认为上下文图谱必须从特定任务或业务流程的自动化中涌现，没有人会或能够去做这项工作，说让我捕获组织中所有的决策轨迹，并将它们放入一个通用的上下文图谱中，这听起来有点像解决世界饥饿问题，是个好主意，但很难实现。)
- "Our core thesis is these context graphs will emerge organically and they'll emerge organically because just as as as processes get automated and human beings are incentivized through be humans in the loop because really they are providing a lot of the training data." - Ashu Garg `[21:30]` (我们的核心论点是这些上下文图谱将有机地涌现，它们之所以有机地涌现，是因为随着流程自动化，人类被激励成为循环中的人，因为他们确实提供了大量的训练数据。)
- "A year from now you will actually have hundreds of context graphs in production at scale." - Ashu Garg `[24:30]` (一年后，你将实际拥有数百个大规模投入生产的上下文图谱。)
- "The enabling infrastructure stack for context graphs will be well defined and and there will be variations and flavors but you know I totally anticipate that this time next year we'll be writing Okay, here's here's the way here's the best practice stack." - Ashu Garg `[24:50]` (上下文图谱的底层基础设施技术栈将得到明确定义，并且会有不同的变体和风味，但我完全预计明年这个时候我们将会写出“好的，这就是最佳实践栈”。)
- "The debate about what is a context graph and what are decision traces and what they why they matter will go away and the question will be how do we extract value from context graphs?" - Ashu Garg `[25:20]` (关于什么是上下文图谱、什么是决策轨迹以及它们为何重要的争论将消失，问题将变为我们如何从上下文图谱中提取价值？)
**个人感受**

Ashu的预测充满了远见和信心，特别是关于“上下文图谱栈”的出现，这预示着一个全新技术生态系统的形成。将讨论焦点从“是什么”转向“如何提取价值”，也体现了从概念到实践的成熟。

**延伸思考**

如果上下文图谱真的成为新的“现代数据栈”，那么围绕其构建的工具、平台和服务将迎来爆发式增长。如何设计一个灵活且可扩展的上下文图谱架构，以适应不同垂直领域的需求，将是未来研究和开发的关键。

### 精华收获

1. **AI Agent的“为什么”缺失是核心痛点**：当前AI Agent在企业级应用中面临的挑战，在于它们只能执行“如何做”，而无法理解决策背后的“为什么”（如例外批准、冲突解决、先例应用等人类推理）。上下文图谱正是为了解决这一根本性问题而生。
1. **上下文图谱是决策的机构记忆**：它被定义为企业中所有决策背后“为什么”的机构记忆，其核心单元是“决策轨迹”（Decision Trace）。决策轨迹捕获了Agent或Agent系统执行业务流程时，包括人类参与在内的所有决策步骤、例外、覆盖和跨系统上下文。
1. **中间抽象层与可防御性护城河**：上下文图谱被视为一个关键的“中间抽象层”，它将成为未来十年最成功的应用公司或Agent系统公司的持久层，并为它们提供独特的、难以被现有巨头复制的竞争优势。
1. **框架而非单一技术架构**：上下文图谱并非一种固定的技术实现，而是一个灵活的框架。其具体实现将因用例和场景而异，涉及多种技术组件和数据结构。
1. **“写路径”的价值**：上下文图谱关注的是业务流程中实际操作性决策的“写路径”，即捕获从任务开始到最终结果的完整步骤序列，包括人类干预和例外情况，而非仅仅记录决策的最终结果（“读路径”）。
1. **初创公司的独特优势**：处于业务流程自动化“编排路径”上的Agent系统初创公司，因不受现有业务流程或数据存储的束缚，在捕获决策轨迹和构建上下文图谱方面具有独特优势。
1. **非结构化数据是金矿，也是挑战**：大部分有价值的决策信息存在于非结构化数据（如邮件、Slack、Zoom会议）中。如何从这些数据中有效提取洞察，并解决数据治理和隐私问题，是构建上下文图谱的关键挑战。
1. **有机、垂直化涌现**：上下文图谱将以有机、垂直的方式在企业中涌现，而非通过一个统一的“通用上下文图谱”来解决所有问题。不同业务流程和垂直领域将拥有各自的上下文图谱。
1. **未来预测**：
这些洞察共同描绘了AI Agent未来发展的蓝图，强调了从“执行”到“理解”的范式转变，以及在复杂企业环境中实现真正智能化的关键路径。

---
