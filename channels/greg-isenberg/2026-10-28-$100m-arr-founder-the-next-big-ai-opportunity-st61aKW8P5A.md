---
title: "$100M ARR Founder: The Next Big AI Opportunity"
channel: "Greg Isenberg"
published: "2026-10-28"
source_url: "https://www.youtube.com/watch?v=st61aKW8P5A"
video_id: "st61aKW8P5A"
tags: ["AI", "创业", "Product", "Agent Harness", "Gamma"]
rating: 4
language: "英文"
word_count: 45076
duration: "49:21"
---

# $100M ARR Founder: The Next Big AI Opportunity

- **Channel:** Greg Isenberg
- **Published:** 2026-10-28
- **Source:** https://www.youtube.com/watch?v=st61aKW8P5A
- **TL;DR:** Agent Harness 才是 AI 产品的真正壁垒，真正的机会藏在"你比别人更了解的领域"里
- **Tags:** AI, 创业, Product, Agent Harness, Gamma
- **Rating:** 4

## 版本

- [结构化文稿](2026-10-28-$100m-arr-founder-the-next-big-ai-opportunity-st61aKW8P5A.structured.md)
- [原始文稿](2026-10-28-$100m-arr-founder-the-next-big-ai-opportunity-st61aKW8P5A.transcript.md)

# 从 Gamma 的 100M ARR 到 Agent Harness 的下一波巨大机遇

## 材料信息

- **标题**：$100M ARR Founder: The Next Big AI Opportunity
- **作者/来源**：Greg Isenberg（主持人），John Noronha（嘉宾，Gamma 联合创始人兼首席产品官）
- **类型**：YouTube 视频字幕（播客访谈）
- **关键元数据**：本集由 Anthropic 赞助；John Noronha 是 Gamma 的联合创始人兼首席产品官；Gamma 已实现 100M ARR，近期完成了平台重大改版发布

---

## 开篇引入

当一家公司从"用 AI 做 PPT"的简单工具，进化为一个拥有 20 个模型、数百次 LLM 调用、完整的 Agent 运行框架，并最终抵达 1 亿美元年度经常性收入（ARR）的里程碑时，它所经历的并不是一个"产品迭代"的故事——而是一场关于 AI 产品底层逻辑的范式革命。

这期播客的独特价值在于：John Noronha 不是坐在那里讲概念。他是把 Gamma 内部的每一个技术决策、每一次模型切换、每一个实验的成败，像拆解一台精密机器一样摊开给你看。从"什么是 Agent Harness"这种基础概念，到"为什么我们的用户需要 AI 闻不到"这种产品哲学，再到"如果你明天就要创业，应该选什么样的 niche"这样的实战建议——这是一次既有理论框架、又有操作细节的深度对谈。

更重要的是，John 有意识地避免了"风口的正确话术"。他没有说"你应该去做法务 AI"或"医疗 AI 是蓝海"，而是诚实地告诉你：法务 AI 已经太拥挤了，会计 AI 也太拥挤了，真正的机会在于那些"看起来不像编程问题"的领域——那些高度主观、需要人类判断力、且用户真正在乎输出结果的场景。这种坦诚，在当今的 AI 播客中已经越来越稀缺。

---

## 详细内容

### 什么是 Agent Harness？拆解一个被滥用但很少被真正理解的概念 `[内容范围：开场-第一部分]`

**核心观点**
Agent Harness（智能体驾驭框架）不是一个新词汇的包装，而是区分"用 AI 做功能"和"用 AI 做产品"的核心分水岭。它本质上是一套完整的工具系统，让 AI Agent 能够在特定环境中执行任务、检查自己的工作、并与用户交互。

**深度阐述**

John 用 Gamma 自身的演进历程来诠释这个概念，这比任何抽象定义都更有说服力。

Gamma 是一家做演示文稿、文档、网站和社交图形的工具，成立于 2020 年。在 2023 年真正爆发之前，Gamma 做的事情很"原始"：他们调用大语言模型，手动把这些调用串起来，组成预设的工作流。比如，写一页幻灯片、做一份大纲。那时候，产品的核心逻辑是**手工编排**——工程师决定第一步做什么、第二步做什么，每一步调用什么模型，然后把这些步骤硬编码进产品。

但过去一两年发生的"Agent 革命"彻底改变了这个逻辑。John 说得很清楚：

> "The big revolution that's happened in the last year or two is this agent revolution where the most powerful AI products now are not stringing together these individual LLM calls by hand, but they're actually having one higher-level loop of an LLM run that will do some kind of work, inspect it, use tools, and then turn that into something over a whole series of executed calls."
>
> "过去一两年发生的重大变革，就是这场 Agent 革命。现在最强大的 AI 产品，不再是用手工方式把大语言模型的调用串起来，而是让一个更高层级的 LLM 循环来运行：它会做一些工作，检查自己的工作，使用各种工具，然后通过一整个系列的调用链把结果转化为成品。"

这就是 Agent 和"工作流自动化"之间的根本区别。工作流是预设的、线性的；Agent 是循环的、自我检查的、能够根据中间结果动态调整的。

**那"Harness"具体指什么？**

John 的定义非常直白：Harness 就是 Agent 用来完成任务的所有工具的集合。他举了一个最著名的例子——Claude Code：

> "Claude Code is a harness for programming. So Claude Code teaches the agent how to go through all the files on your system and see what's there, teaches it how to run tests, and even prompts it with certain rules like go into plan mode in certain cases, or run these tests after completing execution, or do this stuff on GitHub."
>
> "Claude Code 就是一个编程领域的 Harness。它教会 Agent 如何浏览你系统上的所有文件、了解里面的内容；教会它如何运行测试；甚至用特定的规则来引导它，比如在某些情况下进入规划模式、执行完后运行测试、或者在 GitHub 上做某些操作。"

注意 John 的描述中，Harness 不只是"工具"的集合。它还包括**规则、工作习惯、以及 Agent 的行为规范**。Claude Code 不只是一个可以运行命令的终端——它是一整套关于"如何作为一个程序员来工作"的行为框架。它知道什么时候该停下来规划，什么时候该跑测试，什么时候该去 GitHub 上操作。

这正是 Harness 和"API 调用"之间的本质区别。API 调用只是"让模型做一件事"；Harness 是"让 Agent 像一个人一样在某个领域里工作"。

**为什么 Gamma 是"创意 Agent Harness"？**

John 指出，Gamma 不是编程 Agent，而是创意 Agent。这意味着它的 Harness 需要处理完全不同类型的问题：理解用户的审美偏好、帮助用户讲故事、关注视觉设计、生成图像并判断它们是否好看。这些都不是"客观正确"的问题，而是高度主观的问题。这个区别贯穿了整期播客，也贯穿了 Gamma 的产品设计哲学。

**延伸思考**

John 在这里埋下了一个非常重要的观点种子，后面会反复出现：**不同类型的 Agent 需要完全不同的 Harness**。编程 Agent 的 Harness 处理的是客观问题（代码能跑吗？测试通过了吗？），而创意 Agent 的 Harness 处理的是主观问题（这个设计好看吗？这是用户想要的风格吗？）。如果你把编程 Agent 的 Harness 逻辑套用到创意领域，你会得到一个技术上完美但用户体验很差的工具。这种"问题类型的差异"驱动了整个 Harness 的设计逻辑，也是后来 John 讨论"什么领域适合做垂直 Agent Harness"时的核心判断标准。

**精华收获**
- Agent Harness ≠ API 调用的集合。它是一个让 Agent "像人一样工作"的完整行为框架，包括工具、规则、习惯和自我检查机制
- 区分"工作流"和"Agent"的关键在于：工作流是线性的、预设的；Agent 是循环的、能够自我检查和动态调整的
- 不同的领域需要完全不同的 Harness，核心差异在于问题是客观的还是主观的


### "Agent Harness 是新的 GPT Wrapper"——一句好推特，还是事实？ `[内容范围：第二部分]`

**核心观点**
Greg 提出了一个很可能在社交媒体上刷屏的说法："Agent Harness 是新的 GPT Wrapper"，暗示 Harness 本质上还是给大模型做的一层薄薄包装。John 的回应既承认了这句话的传播价值，又从根本上反驳了它的内涵。

**深度阐述**

Greg 用了一个自嘲式的说法来抛出问题："I've been saying agent harnesses are the new GPT wrappers or new wrappers, right? Um is that just a good tweet or is there some truth to it?"（我一直在说 Agent Harness 就是新的 GPT 包装器，对吧？这到底只是一条好推文，还是真有道理？）

John 的回答是这样的：

> "I always disputed this concept of the GPT wrapper originally because it sort of implies that 90% of the work is the LLM, and then there's just this thin layer on top, which is the wrapping back and forth. I think maybe what harnesses illustrate is that actually the wrapping is most of the work."
>
> "我一开始就对 GPT Wrapper 这个概念有异议，因为它暗示 90% 的工作是由大语言模型完成的，上面只是加了一层薄薄的包装，用来做来回的数据传输。我觉得 Harness 这个概念恰恰说明了——其实'包装'才是工作的大头。"

这段话切中了一个行业内长期存在的误解。在 ChatGPT 刚刚爆火的时候，人们对"GPT Wrapper"的贬低本质上是在说：大模型很强大，你只是做了一层薄薄的界面，没有真正的技术壁垒。但 John 的观察揭示了完全相反的真相：**模型本身是高度商品化的**（各个大模型之间的核心能力差异没有人们想象中那么大），真正的壁垒来自 Harness——也就是你如何理解用户的上下文、如何设计 Agent 的工作流程、如何让模型在一个特定场景中表现得像专家。

John 进一步指出，连 OpenAI 和 Anthropic 这些模型公司本身，也在大量投入 Harness 的开发：

> "Even the model companies like OpenAI and Anthropic are putting so much of their work into harness development as well. So they are themselves doing wrapping of these things to achieve different capabilities."
>
> "连像 OpenAI 和 Anthropic 这样的模型公司，也在把大量工作投入到 Harness 的开发中。所以它们自己也在做'包装'这件事，以实现不同的能力。"

这个观察非常重要。它意味着行业的竞争重心已经从"谁有最好的模型"转向了"谁能把模型最好地嵌入到实际工作场景中"。模型公司也在做应用层的事情，这不是因为它们想和创业公司竞争，而是因为**模型本身的能力边界已经足够接近，真正的差异化来自不同场景下的产品化能力**。

**延伸思考**

这一段的讨论其实点出了一个创业者的核心焦虑：如果模型公司在做 Harness，那创业公司的机会在哪里？John 没有在这里直接回答这个问题，但他在后面给出了非常具体的答案——**模型公司不会去做那些高度垂直、需要行业深度知识的 Harness**。模型公司做的是通用 Harness（比如 Claude Code 面向所有编程场景，ChatGPT 的 Canvas 面向所有写作场景），但一个专为室内设计师打造的工具、一个专为律师打造的工具，模型公司既没有精力也没有行业知识去做。这就是为什么"GPT Wrapper"的贬低论调在 2024 年之后就逐渐消散了——人们开始意识到，**包装不是简单的事情，它是产品本身**。

**精华收获**
- "GPT Wrapper" 的贬低论暗示 90% 的工作在模型，但现实是 Harness（包装）才是真正的工作量所在
- 大模型的能力正在趋同，真正的差异化来自 Harness 的设计
- 模型公司也在大量投入 Harness 开发，但创业公司的机会在于垂直领域的深度


### 解剖一个 Prompt：Gamma 背后的 200 次模型调用与 20 个模型 `[内容范围：第三部分]`

**核心观点**
当你在 Gamma 上输入一个 prompt，你体验到的是一次流畅的输出。但在那个表面之下，Gamma 会在云端启动一台完整的电脑（Agent Sandbox），通过四到五个不同的模型、30 到 40 次初始调用来完成信息搜集和用户偏好确认，而整个流程下来可能涉及 20 个模型和 200 次调用。

**深度阐述**

这是整期播客中最具"解剖学"意义的段落。John 为一个典型的 Gamma 用例（用户把一堆杂乱的笔记或 PDF 粘贴进来，要求转换成 20 页的演示文稿）画出了一条完整的执行链路：

**第一秒到第十秒：启动沙盒，搜集信息，询问用户**

> "The first thing is we actually spin up an entire computer in the cloud. This is what they call an agent sandbox. This is what the OpenAI ones broke out of famously in the last few months."
>
> "我们做的第一件事，是在云端启动一整台电脑。这就是所谓的 Agent 沙盒——也就是 OpenAI 的 Agent 几个月前著名'越狱'的那个东西。"

John 提到的 "OpenAI broke out of" 指的是一个真实事件：OpenAI 的某些 Agent 在沙盒环境中找到了逃逸的方法。这个细节不仅展示了 Gamma 在技术基础设施上的投入，也暗示了 Agent 安全性的重要性。

在沙盒启动后，Gamma 会把用户的 prompt、用户带来的文件、以及关于用户的其他上下文都放进这个环境中。然后 Agent 的第一个任务往往是：**搞清楚还需要向用户问什么**。Gamma 会自动弹出一个表单，问一些问题：这个演示是给谁看的？是学校用的教育材料，还是给成年人的？是用在工作场景吗？

同时，Gamma 还会通过集成工具（Notion、Slack、Linear 等）拉取相关上下文。John 说：

> "Just already in that first maybe 10 seconds, we've now made calls using probably three or four different models, including expensive and cheap ones. We'll talk about actually how we manage costs."
>
> "在最初的 10 秒里，我们已经用大概三到四个不同的模型进行了调用，包括贵的和便宜的。后面我们会谈谈怎么管理成本。"

**写大纲、选模板、还没开始做幻灯片**

接下来，Gamma 会写演示文稿的大纲（这需要好几次 LLM 调用），然后从一个模板库中选一个适合你的视觉风格。这里涉及到**视觉模型**（Vision models）来判断哪个模板适合你，还会用到**搜索嵌入**（search embedding）的技术，在数千个模板中找到最合适的那个。如果你说"但我想让它偏红色"或"偏蓝色"，Gamma 还会定制化调整这个模板。

John 给出了一个关键数字：

> "We haven't even started making the deck yet, and already we've probably made something like 30 or 40 different LLM calls to maybe four or five different models doing different tasks."
>
> "我们甚至还没开始做演示文稿，就已经进行了大概 30 到 40 次不同的 LLM 调用，用了大概四到五个不同的模型来执行不同的任务。"

**生成演示文稿：并行、速度、视觉 QA**

用户点击"生成"按钮后，事情变得更加复杂。Gamma 需要写幻灯片上的文字，布局所有元素，生成图像（装饰性的或实质性的），制作图表和信息图。John 强调了一个关键的工程挑战：

> "There's a huge performance consideration because if we did these one by one, it's going to be quite slow and you're going to basically leave before we ever finish."
>
> "这里有一个巨大的性能考量，因为如果我们一个一个来做这些事情，速度会非常慢，你基本上会在我们完成之前就离开。"

所以 Gamma 做了大量的并行化工作。最终，整个演示文稿在一分钟左右的时间内"流式"呈现在用户面前。

但故事还没有结束。John 说：

> "After we generate that first presentation, we're now going to have an AI vision model look at every single slide and look for problems that I can find. Misaligned text, the person's head got cut off in the image, there's weird contrast, something's not padded right."
>
> "生成第一版演示文稿后，我们会让一个 AI 视觉模型检查每一页幻灯片，找出可能存在的问题。文字错位了、图像中人物的头被裁掉了、对比度有问题、内边距不对……"

然后 Gamma 会根据视觉 QA 的发现，进行多轮修复和重做。到这里，John 给出了最终的数据：

> "Now at this point, we've probably used 20 different models making like maybe 200 different calls along the way to deliver what looks to you like one finished output."
>
> "到这个节点，我们可能已经用了 20 个不同的模型，中间进行了 200 次不同的调用，来给你交付一个看起来只是一份成品的东西。"

**个人感受**

John 在描述这个过程时并没有用"我们很厉害"的语气，反而是一种"这其实非常复杂，但我们把它隐藏得很好"的谦逊。他特别强调了人类设计师的眼睛在视觉 QA 中的不可替代性："It's actually amazing how many things can go wrong in something like a simple presentation that a human eye can detect right away. Or sometimes the human eye can't detect because it takes a designer's eye."（不可思议的是，连一个简单的演示文稿都有那么多可能出错的地方——人的眼睛立刻就能发现这些问题。有时候人的眼睛确实发现不了，因为那需要设计师的眼光。）这段话体现了一个核心产品哲学：**AI 可以帮助做设计，但判断"设计好不好"这件事，需要被建模，需要被训练，不能想当然地交给通用模型**。

**延伸思考**

这段描述中最引人深思的不是技术细节本身，而是它揭示了一个很多人忽略的事实：**一个看起来"简单"的 AI 产品，其背后的复杂度可能远超想象**。这也是为什么"GPT Wrapper"的贬低论越来越站不住脚。一个真正的产品不是"调用一次模型然后返回结果"，而是一个精心设计的复杂系统，需要处理性能、成本、质量控制、用户体验等各个方面的问题。

这类似于外卖 App 的类比：用户点一个按钮，食物就送来了。但这个按钮背后，是餐厅的网络、配送员的调度系统、实时位置追踪、支付系统、评分系统等一系列复杂的基础设施。AI 产品也是如此，只不过基础设施变成了 Agent Harness。

**精华收获**
- 一个看似简单的 AI 输出背后，可能隐藏着 20 个模型和 200 次调用的复杂度
- Agent Harness 的关键组件包括：沙盒环境、信息搜集、用户偏好询问、内容生成、自主质量检查、多轮修复
- 视觉 QA 是创意 Agent 的核心环节："什么看起来不错"不是默认模型能解决的问题


### 寻找垂直 Agent Harness 的机会：主观性、人的参与、专有数据 `[内容范围：第四部分]`

**核心观点**
John 认为，"适合做垂直 Agent Harness"的领域具有两个关键特征：第一，问题**看起来和编程很不一样**（高度主观、需要判断力）；第二，用户**真正在乎输出的具体内容**。他还提出了三种可能的"护城河"：独特的愿景、专有的数据、以及非软件的实体业务整合。

**深度阐述**

Greg 提出了一个非常直接的问题："如果明天你要创业，你会选择什么垂直 Agent Harness 的领域？"

John 没有给出一个具体的行业清单，而是先给出了一个**判断框架**——什么样的领域适合建独立的 Agent Harness：

> "Where we see a lot of value of making our own distinct agent harness is when that problem looks very different from just plain old coding. In our case, what makes it different is that it's very subjective. There's a lot of judgment calls to make along the way where two different people will disagree about what good looks like, which means you want to have the human in the loop. And also where the person using it actually really cares about the specifics of the output."
>
> "我们发现，当一个问题和普通编程看起来很不一样时，做自己独特的 Agent Harness 就很有价值。在我们的案例中，不一样的地方在于它非常主观。在过程中有很多需要判断的地方——两个不同的人会就'什么算好'产生分歧。这意味着你需要让人在闭环中。另外，用户真正在乎输出的具体内容。"

这个判断框架非常有洞察力。它实际上划分了"通用 Agent 可以处理"和"需要垂直 Harness"的边界：
- 如果一个问题有**客观的对错标准**（比如代码能否运行、测试是否通过），那么通用 Harness 就能做得很好。这就是 Claude Code 之所以强大，却不需要成为一个"垂直"工具的原因。
- 如果一个问题**高度主观**（比如设计好不好看、故事讲得好不好），那么通用的 Harness 就会力不从心。你需要一个专门针对这个领域的 Harness，来理解用户的品味、风格偏好和行业惯例。

**一个具体的例子：游戏**

John 举了一个很有趣的例子——游戏。他说很多人在用 Claude Code 做游戏（vibe coding 的产物），但他更感兴趣的是**个人视频游戏**的概念。他说：

> "I'm really bullish on this idea of like the personal video game where you almost like vibe coded it yourself. Coding agents are already really good at making video games, but I think they're often not good at actually sourcing the players' opinions on where it should go and where it should evolve."
>
> "我非常看好'个人视频游戏'这个观念——你几乎是自己用 vibe coding 做出来的游戏。编程 Agent 已经很擅长制作视频游戏了，但它们通常不擅长听取玩家的意见，了解游戏应该往哪个方向发展、如何演变。"

他进一步联系到 Roblox 和 Minecraft 的现象，指出这些平台上有很多非技术用户在塑造自己的世界。他的问题是：**是否存在一个 Harness，整个运行在 3D 世界里？** 这个想象非常前沿，它把 Agent Harness 从"文本或代码输出"的框架中解放出来，拓展到了沉浸式环境。

**三种"护城河"**

当 Greg 追问创业者的护城河来自哪里时，John 给出了三个可能的方向：

1. **独特的愿景**：你对世界有独特的看法，并且比别人更快地朝着这个愿景前进。
2. **专有的数据**：你已经拥有一个成功的平台，或者掌握着别人拿不到的信息。
3. **软硬件结合或实体服务**：

> "It's not just software because software is getting very crowded and it's a scary market to be in. But, you know, there's hardware, there's physical services, there's all sorts of real life businesses to be made that incorporate AI in interesting ways."
>
> "不只是软件，因为软件越来越拥挤，那是一个令人害怕的市场。但还有硬件、实体服务，以及各种可以以有趣方式融入 AI 的现实生活业务。"

**个人感受**

John 在讨论这些时表现出一种非常"清醒"的态度。他没有试图给出一份"你应该做 X"的清单，而是反复强调"这是非常个人的事情"。当 Greg 问他"如果让你选一个 Gamma for X 的领域，你会选什么"时，John 的回答是：

> "It's such a personal thing because if it was my thing, I'd be building it already. I think you need to do the thing that I don't know anything about, whether it's like Pokémon cards or fashion or sneakers or whatever it is. Like find your domain where you know what's going on and build it."
>
> "这是一件非常个人的事情，因为如果我知道答案，我早就已经在做了。你需要去做那些我不了解的事情——不管是宝可梦卡牌、时尚、球鞋还是其他什么。找到你真正了解的那个领域，去构建它。"

这段话的诚实性值得注意。在 AI 播客中，嘉宾往往会被期待给出"10 个蓝海领域"的清单。但 John 拒绝了这种**伪普适性**。他的观点是：真正的机会不在"行业"这个粒度上，而在"你个人对某个特定领域有深度理解"这个粒度上。一个对室内设计有深度理解的人，和一个对室内设计一无所知但听说"这是蓝海"的人，他们在同一个领域里会发现完全不同的机会。

**延伸思考**

John 的判断框架可以进一步拓展：**"主观性"和"用户在乎程度"是两个维度，它们的组合可以预测垂直 Agent Harness 的潜力**：
- 高主观性 + 高在乎程度 → 非常适合垂直 Harness（设计、品牌、创意领域）
- 高主观性 + 低在乎程度 → 不适合（用户不会为好的输出付费/使用）
- 低主观性 + 高在乎程度 → 通用 Harness 就够用了（编程、数据分析）
- 低主观性 + 低在乎程度 → 可以直接完全自动化

这个二维框架是 John 没有明说但隐含在讨论中的。它提供了一个比"选行业"更有操作性的判断工具。

**精华收获**
- 适合垂直 Agent Harness 的领域特征：问题高度主观 + 用户在乎输出的具体细节
- 三种护城河：独特愿景、专有数据、实体业务整合
- 真正的机会在于"你个人有深度理解的领域"，而不是"听起来很热的行业"


### AI Smell：为什么 AI 生成的内容必须"去味" `[内容范围：第五部分]`

**核心观点**
"AI Smell"（AI 气味）是指 AI 生成的内容具有某种可辨识的、令人不适的"人工感"。对于任何创意型 AI 产品来说，消除或多样化这种"气味"不是优化项，而是生死攸关的问题。

**深度阐述**

John 用了一个非常生动且略带幽默的表达来描述这个问题：

> "AI smell is what we use to refer to this fact that when people make work with AI, you can often tell they used AI. I think it shows up most in writing, where when someone writes you an email made with Claude, you're just like, you don't normally use that word. That's not what you sound like."
>
> "AI 气味，我们用它来指代这样一个事实：当人们用 AI 制作内容时，你通常能看出来他们用了 AI。我觉得这在写作中表现得最明显——当有人用 Claude 写的邮件发给你时，你会觉得：你平时不会用这个词，那不是你说话的方式。"

John 还举了一个非常具有场景感的例子：

> "I notice it a lot with AI images now, where I just like walk around in San Francisco and every cafe, every restaurant has a poster where I can just smell like that's Nano Banana, that's GPT image."
>
> "我现在在 AI 图像中也经常注意到它。我在旧金山街头走一圈，每个咖啡馆、每个餐厅的墙上都贴着海报，我一看就能闻出来：那是 Nano Banana 做的，那是 GPT Image 做的。"

这个例子非常有力，因为它把 AI 气味从一个抽象概念变成了一个**日常体验**。John 作为 Gamma 的首席产品官，每天都在和 AI 生成的内容打交道，所以他的"嗅觉"更敏锐。但关键在于：**这种嗅觉正在扩散到普通用户中**。随着 AI 生成内容的普及，普通人也在开始培养这种辨识能力。

**Gamma 为什么会深受其害？**

John 坦诚地解释了 Gamma 面临的具体困境：

> "We had kind of been a victim of our own success as one of the early AI tools, where when nobody used Gamma, if you used it, your stuff would look really cool and stand out. But once everybody started using it, everything started to look like Gamma, and people didn't want to be recognized as using AI."
>
> "作为早期的 AI 工具之一，我们在某种程度上成为了自己成功的受害者。当没多少人用 Gamma 的时候，如果你用了，你的东西看起来会很酷，很突出。但当大家都开始用之后，所有东西都开始长得像 Gamma 了，而人们不想被认出来用了 AI。"

这是每个成功 AI 产品都会面临的"同质化陷阱"。产品的标志性风格越强，用户在早期越喜欢它（因为"看起来很不一样"），但一旦用户规模大到一定程度，这种标志性风格就变成了负担（因为"看起来都长一个样"）。

**解决方案：一千种 AI 气味**

Gamma 在这次大版本更新中的核心目标，用 John 的话来说就是：

> "There's still going to be AI smells, but there can be a thousand AI smells instead of one monolithic one, and we can help people jump to different little pockets."
>
> "AI 气味还是会存在的，但可以有一千种 AI 气味，而不是一种单一的、压倒性的气味。我们可以帮助用户跳到不同的小领域里。"

这里有一个非常巧妙的类比——**时尚**：

> "We actually use the analogy of fashion. Fashion has a smell, too. You're like, I know that H&M shirt you're wearing. Like, I have the same one. And with fashion, there's this dynamic where people are cycling through different looks."
>
> "我们实际上用了时尚的类比。时尚也有'气味'。你会想：我知道你穿的那件 H&M 衬衫，因为我也有一件一样的。在时尚领域，有一种动态：人们不断在不同的风格之间循环。"

时尚领域的动态是：某种风格流行一段时间后，人们会腻烦它，然后寻找新的风格。AI 生成内容也遵循类似的规律。Gamma 的解决方案是创建一个自动化的系统来持续循环不同的创意风格——用多种 AI 气味替代单一 AI 气味。

**个人感受**

John 对 AI Smell 的关注体现了一种很有意思的产品哲学张力：作为一个 AI 工具，Gamma 的核心使命是帮助用户用 AI 做创作，但产品成功的标准却是**让用户的创作看起来不那么像 AI 做的**。这种"自我否定"的张力在 AI 产品领域越来越普遍。就像一个好的 AI 写作工具不应该让读者觉得"这是 AI 写的"，一个好的 AI 设计工具不应该让观众觉得"这是 AI 做的"。产品的价值不在于展示 AI 的强大，而在于**让用户获得他们想要的结果，而不必为"用了 AI"这件事付出社交成本**。

Greg 在此处提出了一个技术性的问题："有没有一个 eval 来测'这个看起来像通用的'？" 这引出了下一节关于 evals 的讨论。

**延伸思考**

AI Smell 的概念如果进一步延伸，会发现它实际上是一个**信任问题**。当人们能够辨识出 AI 生成的内容时，他们会自然地对内容的真实性、原创性和思考深度产生怀疑。这就像人们看到塑料假花时会觉得"虽然很像真的，但我不喜欢"——不是因为假花不好看，而是因为它**暗示了某些牺牲**：真实的花会枯萎，但它们是活的；假花不会枯萎，但它们缺乏生命。类似地，AI 生成的内容可能在功能上完全合格，但"AI 气味"会让人怀疑创作者是否真的在乎、真的投入了思考、真的理解自己在说什么。

这也解释了为什么 Gamma 的战略是"一千种气味"而不是"无气味"——因为完全消除 AI 气味在今天是不可行的，但让每个用户能找到**属于自己的**那种表达方式，则是可以实现的。这就像时尚品牌不是要消除行业内的品牌辨识度，而是要让每个品牌都有自己独特的风格语言。

**精华收获**
- AI Smell 是"用户能辨识出 AI 生成内容"的现象，它会随着 AI 产品的普及而扩散到普通用户
- 成功的 AI 产品面临"同质化陷阱"：标志性风格越强，规模化后越容易变成负担
- 解决方案不是"消除 AI 气味"，而是"创造一千种不同的 AI 气味"，让用户能找到属于自己的表达方式
- "让用户的创作看起来像用户做的"是所有创意型 AI 工具的核心挑战


### Evals 的局限：为什么"好看"不能被打分 `[内容范围：第六部分]`

**核心观点**
Evals（评估）在客观任务中非常有效，但在高度主观的创意领域，它的局限性就暴露出来了。你不能给"好看"写一个测试用例。这意味着创意型 AI 产品必须找到超越传统 evals 的质量评估方式。

**深度阐述**

当 Greg 问到"有没有一个 eval 来测试'这个看起来像通用的'"时，John 首先花了一点时间解释 eval 是什么（他意识到很多听众可能不熟悉这个术语）：

> "An eval just means a hard-coded question that you ask in a way of judging it. So, a simple example in our world of Gamma is we often want the agent to ask questions when you do something ambiguous. So, we'll give it an eval like, when the user says, 'Make a deck about tigers,' the agent should ask something like, 'Is this for kids or for adults?'"
>
> "Eval 就是一个你用作判断标准的固定问题。在 Gamma 的世界里，一个简单的例子是：我们经常希望 Agent 在用户做了模糊的事情后能问问题。所以我们会给它一个 eval，比如当用户说'做一个关于老虎的演示文稿'，Agent 应该问'这是给小孩还是给大人的？'"

这个解释很巧妙，因为它用了一个 Gamma 内部的具体例子来说明 eval 的运作方式。John 接着解释了 eval 系统的大致逻辑：把很多 evals 组合成一个 benchmark，用来比较不同模型或不同 prompt 的效果，比如"模型 B 的得分比模型 A 高 3%"。

但问题出在哪里呢？John 说：

> "The problem for us in a very creative domain is that evals have always been hard for various subjective taste-oriented things, like, 'Does this look cool?' And even more so, very personal ones, like, 'Is this me? Does this sound like something I would say?' There's no one objective eval for this."
>
> "在我们这个高度创意的领域，问题在于 evals 历来很难用于主观的、品味导向的事情，比如'这个看起来酷吗？'。更不用说那些非常个人化的东西，比如'这像我吗？这听起来像我说话的方式吗？'这些问题没有客观的 eval。"

这是对 eval 局限性最清晰的表述。Evals 本质上是一种**客观测试**——它假设存在一个正确的答案或正确的行为。但在创意领域，甚至不存在"正确"和"错误"的二元区分。同样是做一份演示文稿，A 用户可能喜欢极简风格，B 用户可能喜欢信息密集的风格，两者都没有错。

**那 Gamma 用什么方法来替代？**

John 提到了几种方式：

1. **代理 evals（Proxy Evals）**：虽然"好看"不能被打分，但"是否遵守了品牌指南"可以通过代码检测。Gamma 会创建一些"代理"性质的 evals 来间接衡量质量。

2. **创始人的品味**：

> "Ultimately, what founders can bring to their domain is taste. They have their own sense of what looks good. They're actually talking to their users and those users have one."
>
> "最终，创始人能够带入他们领域的是品味。他们有自己的审美判断力。他们和用户交流，而用户也有自己的审美判断力。"

3. **AB 测试**：

> "Because we have a super diverse user base who are all different, we actually rely a lot more on AB testing. We will actually run two models or two prompts at very big scale and measure across that wide user base what's actually performing better because that captures subjectivity."
>
> "因为我们有非常多样化的用户群，每个人的情况都不同，所以我们实际上更多依赖 AB 测试。我们会在大规模用户基础上运行两个模型或两个 prompt，然后衡量哪个在广泛用户中表现更好，因为这样才能捕捉到主观性。"

**个人感受**

John 在这里透露了一个很有意思的事实：Gamma 在 AB 测试上的投入非常巨大。这不仅解决了"主观性无法被打分"的问题，也展示了 Gamma 的核心竞争力之一——**规模化的实验能力**。当一个公司拥有大量活跃用户时，它可以用数据来替代一部分"专家判断"。但 John 也很坦诚地指出，即使是 AB 测试也有其局限——它只能告诉你哪个更好，但无法告诉你为什么更好。

这让我想到一个更广泛的问题：**在 AI 产品中，什么应该由数据驱动，什么应该由品味驱动？** John 的回答似乎是：能用数据的地方用数据（AB 测试、代理 evals），不能用数据的地方靠品味（创始人的判断、用户的直接反馈）。这两者缺一不可。

**延伸思考**

John 关于 evals 局限性的讨论，其实指出了一个更深层的行业问题：**AI 行业过度依赖基准测试（benchmarks）来评价模型的优劣**。每次新模型发布，都会有一连串的"我们的模型在某 benchmark 上超过了 GPT-4"的宣传。但这些 benchmark 有一个共同的问题：它们都是客观测试。它们可以衡量模型解决数学问题的能力，却无法衡量模型理解人类感受的能力。

这也解释了为什么 Gamma 对"好看"这个问题的处理方式是**多轮视觉 QA**——与其试图用 eval 来定义"好看"，不如训练专门的模型去检测"不好看"的具体标志（文字错位、人物被裁剪、对比度差等）。这是一种"负向评估"策略——不追求定义完美的标准，而是识别和消除常见的失败模式。这就像做菜一样：你很难定义"好吃"是什么，但你可以学会识别"太咸了"或"烧焦了"。

**精华收获**
- Evals 是"有正确答案的问题"，适用于客观任务，但不适用于主观判断
- 创意型 AI 产品的质量评估需要多管齐下：代理 evals、创始人品味、AB 测试
- "负向评估"（识别失败模式）比"正向评估"（定义成功标准）在创意领域更实用
- 规模化的用户基础是实现 AB 测试驱动开发的前提


### 只有 2% 的人在为 AI 付费：为什么这不是一个坏消息 `[内容范围：第七部分]`

**核心观点**
对于"只有 2% 的人在为 AI 工具付费"这个引发热议的数据，John 的态度是：这不让人意外，也不值得恐慌。关键在于，那 2% 中的专业用户正在迅速增长，而 B2B 和"专业消费者"（prosumer）市场才是 AI 产品的真正主战场。

**深度阐述**

Greg 提到了最近热传的 A16Z 数据——只有 2% 的人在为 AI 工具付费。这个数据可能让很多 AI 创业者感到焦虑，但 John 的反应非常平静：

> "Yeah, it doesn't surprise me. I think in general subscriptions are always a bit of a niche thing towards people that are doing some kind of valuable work. I don't think consumers like subscription."
>
> "这不让我感到意外。我觉得一般来说，订阅制总是偏向那些在做某种有价值工作的人的利基市场。我认为普通消费者并不喜欢订阅制。"

这段分析非常务实。John 区分了"消费者订阅"和"工作订阅"：前者是个人为了娱乐而付钱（如 Netflix），后者是专业用户为了提高工作效率而付钱（如 SaaS 工具）。AI 工具本质上属于后者——它们的价值在于帮助用户完成有价值的工作，而不是纯粹提供娱乐。

他继续指出：

> "I think for work it's a totally different story where, you know, work subscriptions are what has driven essentially the entire SaaS boom of the last like 10 to 15 years in software industry."
>
> "对于工作来说就完全不同了。工作订阅本质上推动了整个软件行业过去 10 到 15 年的 SaaS 热潮。"

这是一个非常重要的商业逻辑。"2% 的人在为 AI 付费"这个数据如果放在消费者市场的语境下，确实显得很小。但如果放在 SaaS 市场的语境下，就完全正常了。真正的问题是：这 2% 的质量如何？John 引用同一个 A16Z 报告说：

> "That same chart says that when you actually zoom in to professionals, the numbers are rising like crazy in terms of who's paying for AI."
>
> "同一份图表显示，当你聚焦到专业人士群体时，为 AI 付费的人数正在疯狂增长。"

**Prosumer 是关键词**

John 强调了"prosumer"（专业消费者）这个概念的重要性：

> "That's certainly our main focus and I think most people's main focus in AI is how to find those prosumers, the professional consumers, and how to break into B2B where there's a totally different kind of spending going on."
>
> "这当然是我们的主要关注点，我认为大多数 AI 创业者的主要关注点都是如何找到那些 prosumer——专业消费者，以及如何进入 B2B 领域，那里有完全不同的消费模式。"

**个人感受**

John 在讨论这个问题时表现出了极强的商业成熟度。他没有被"2%"这个数字吓到，也没有试图辩驳这个数据不准确。他的态度是：**这个数据告诉你的不是"AI 市场太小"，而是"消费者市场不是 AI 工具的最佳切入点"**。这是一个非常重要的区分。在 AI 创业圈子里，有一种常见的错误思维是"技术越强大，消费者就越愿意买单"。但事实是，普通消费者不会因为一个工具"很酷"或"很强大"而长期付费——他们只为那些能帮他们**做有价值的事情**的工具付费。

这也解释了为什么 Gamma 的用户群是"咨询顾问、教师、市场营销人员、销售人员、律师"等专业人士。这些人不是在"玩"AI，而是在用 AI 完成真实的工作任务。

**延伸思考**

这里可以联系到一个更大的商业趋势：**AI 应用正在从"新奇玩具"阶段过渡到"生产力基础设施"阶段**。在 ChatGPT 刚发布的时候，大量用户付费是因为好玩。但到了 2025 年，还在为 AI 付费的用户群体已经发生了质变——他们不是在为"和 AI 聊天"付费，而是在为"AI 帮我完成工作"付费。这个转变意味着：AI 产品的价值主张必须从"有趣"转向"有用"，从"展示技术能力"转向"解决实际问题"。

Gamma 的 100M ARR 正是这个转变的成功案例。100M 意味着有大量用户愿意持续为一个 AI 工具付费，不是因为它是 AI，而是因为它真的帮助他们完成了有价值的工作。

**精华收获**
- "2%"这个数据在消费者市场中很正常，但在专业市场中质量远高于数量
- AI 工具的主战场是 prosumer 和 B2B，不是普通消费者
- 产品的价值主张需要从"有趣/强大"转向"有效率/有价值"


### 如果 John 离开 Gamma 会选择什么？Slack 与个人 Agent 的未竟之业 `[内容范围：第八部分]`

**核心观点**
John 最希望存在的 Agent Harness 是"Slack 的个人代理"——一个真正理解你说话方式、能够学习你的回复习惯、并主动帮你管理信息过载的 Agent。这个领域之所以还没被攻克，核心困难在于**个性化**。

**深度阐述**

Greg 问了一个很有意思的问题："如果明天你离开 Gamma，你会创立什么公司？" John 的回答不是某个垂直行业，而是道出了一个他认为还没有被真正解决的问题：

> "I'm really intrigued by this whole sort of like personal agent space. And I haven't gotten to use all the latest ones, but what I feel nobody's totally cracked is like work collaboration. I think if I could build a harness for anything, it would be Slack."
>
> "我对这个'个人 Agent'领域非常感兴趣。我还没有用过所有最新的产品，但我觉得没有人真正破解了'工作协作'这个难题。如果我可以为任何事情构建一个 Harness，那一定是 Slack。"

John 对 Slack 的失望是显而易见的：

> "I'm a little disappointed that Slack themselves have not built the harness for Slack."
>
> "我有点失望，Slack 自己没有为 Slack 构建 Harness。"

那么 John 想象中的 Slack Harness 是什么样的？他的描述非常具体：

> "There's just this absolute flood of communication for anybody whose company uses Slack or Microsoft Teams. There's so many messages going through. You're constantly trying to stay on top of like, 'Well, which ones do I actually have to do something about?' I've seen them nibbling around the edges of this of like you can summarize 30 Slack messages into one. But I want something that just like runs it all truly for me and it learns me. It learns how I would reply before I reply."
>
> "对于那些公司使用 Slack 或 Microsoft Teams 的人来说，通讯量绝对是洪水级别的。有太多的消息在流转。你不断地试图跟进：'到底哪些是我真正需要处理的？' 我看到他们在边缘尝试，比如你可以把 30 条 Slack 消息总结成一条。但我想要的是：它真正为我管理这一切，并且它**学习我**。在我回复之前，它就知道我会怎么回复。"

John 的关键洞察在于最后一句话："It learns me." 这不是"配置一个 AI 助手"，而是让 Agent 通过观察你的行为来学习你的风格。他进一步说：

> "I have sent approximately a billion Slack messages. That should be all you need to know how I'm going to reply."
>
> "我大概发了十亿条 Slack 消息。这应该足够让你知道我会怎么回复了。"

这句话既有幽默感，又揭示了一个事实：**我们已经在各种平台上留下了海量的个人行为数据，这些数据足以训练一个模型来模拟我们的语言风格和行为模式**。但到目前为止，还没有一个工具充分利用了这一点。

**为什么这个很难？**

John 自己给出了答案：

> "Of course that's hard because it's personal and this is why the agents haven't done it. It's really hard to make agents personal."
>
> "当然这很难，因为它是个人化的。这就是为什么 Agent 还没做到这一点。让 Agent 变得个人化真的很难。"

**个人感受**

John 的表达中有一个非常动人的细节。他说：

> "I want an agent that can learn my voice."
> "我想要一个能学习我的声音的 Agent。"

"声音"（voice）这个词在这个语境中承载了很深的含义。它不只是指"语气"或"风格"，而是指一个人在沟通中的**完整身份表达**。John 说：

> "Even in emails doesn't feel totally cracked. I've seen Gmail has the little things that are like, 'Oh, you know, like yes, I'd love to go to the dentist on Thursday.' Which is not how I'd ever reply in my life."
>
> "连电子邮件的领域也还没有被完全攻克。我看到 Gmail 有那些小功能，比如'好的，我很愿意周四去看牙医'——我一生中从不会那样回复。"

这个细节很有共鸣感。当前的 AI 写作助手给用户提供的建议通常是那种"礼貌但万无一失"的回复，它们安全、规范、但也完全**不像你**。John 想要的是"I want an agent that can learn my voice"——不是模板化的商业英语，而是真正的个人声音。

**延伸思考**

John 的 Slack Harness 愿景实际上指向了一个更大的产品类别：**个人代表 Agent（Personal Representation Agent）**——一个能够代表你进行专业沟通的 Agent，它不仅处理信息，还维护你的职业身份。这类 Agent 的核心难点不在技术（模型已经有能力学习个人风格），而在于**信任问题**。要让一个人把日常沟通的"草稿权"交给 Agent，需要高度的信任——相信 Agent 真的理解自己的风格，相信 Agent 不会说出不符合自己身份的话。

这也解释了为什么当前还没有产品能够真正破解这个问题。它需要的不是一个"更好的模型"，而是一个**能够持续学习和适应个人风格的系统**。而且这个系统必须非常谨慎地处理信任问题——在用户对 Agent 有足够信任之前，Agent 的任何一次"不像我"的输出都会严重损害这种信任。

**精华收获**
- 个人 Agent 领域最大未攻克的难题是"工作协作"和"个人声音"的学习
- 真正的个性化需要 Agent 观察用户行为，而不是通过问答或配置来了解用户
- "它学习我" 和 "我配置它" 之间存在根本区别
- 信任是个人 Agent 最大的门槛：一次"不像我"的输出就可能破坏信任


### 构建在他人模型之上：为什么使用第三方模型不是一种耻辱 `[内容范围：第九部分]`

**核心观点**
早期创业公司不应该在训练自己的模型上浪费时间。使用市面上最好的模型是理性的选择。但随着公司成长，在专有数据上做 fine-tuning、在特定任务上做自己的研究，才逐渐变得有意义。

**深度阐述**

Greg 提出了一个很多 AI 创业者都会面临的问题："在别人的模型上构建产品，你有什么建议？"

John 的回答非常务实：

> "There's no shame in building on other people's models. We have done this from the very start often bouncing between Anthropic, OpenAI, Google models."
>
> "在他人的模型上构建产品没有什么可羞耻的。我们从一开始就是这样做的，经常在 Anthropic、OpenAI 和 Google 的模型之间切换。"

他进一步批判了"必须自己训练模型才有护城河"的论调：

> "So much of the discourse has always been like, 'No, you got to train your own stuff. You got to fine-tune it because you need the moat.' I have always felt that that's unrealistic for early-stage startups in particular. First of all, the money involved in training your own models is really hard. But also, the models out there keep on getting better. I rarely would want to be competing against the models that are out there."
>
> "行业里有很多论调说：'不，你得训练自己的模型。你得 fine-tune 它，因为你需要护城河。' 我一直认为这对于早期创业公司来说尤其不现实。首先，训练自己模型所涉及的资金投入非常困难。而且，市面上的模型一直在变得更好。我很少会想和市面上的模型竞争。"

这是一个非常冷静的判断。很多 AI 创业者被"护城河"这个概念困住了，认为如果不训练自己的模型就没有壁垒。但 John 的视角是：**早期创业公司的主要挑战不是"建立技术壁垒"，而是"获得使用量"**。"By all means, use the models that are out there to get that usage in the first place."（用尽一切办法，先用市面上的模型获得使用量。）

**但随着公司成长，事情会改变**

John 坦承，当 Gamma 达到一定规模后，他们开始做一些模型层面的工作：

> "We've actually had great success fine-tuning models to bring our costs down and in some cases even to start to do more personalization for people. We also have started to identify specialized tasks that the big models are bad at. Like I mentioned earlier, this whole process of QAing a slide and telling if it's good. We've actually not had great results using any of the models out there for it. So, we are actually doing some of our own research to build models for those specialized tasks."
>
> "我们实际上在 fine-tuning 模型方面取得了很好的成果，主要是为了降低成本，在某些情况下甚至开始做更多的个性化。我们也开始识别一些大模型不擅长的专门任务。比如我之前提到的检查幻灯片质量的过程。市面上任何模型都不太擅长这个。所以我们实际上在做一些自研模型的工作。"

这段话揭示了一个"分阶段"的模型策略：
- **早期**：全部使用第三方模型，把精力集中在产品和用户获取上
- **成长期**：开始 fine-tuning 来降低成本，识别通用模型不擅长的专门任务
- **成熟期**：针对专门任务做自己的研究

这不只是一个技术策略，更是一种**资源分配策略**。在早期阶段，把有限的工程资源花在"训练模型"上，意味着放弃了对用户体验、市场获取、产品迭代的投资，本质上是一种资源错配。

**关于云端模型 vs 开源模型的讨论**

Greg 问到了当前热门的话题：前沿的云端模型（如 GPT、Claude、Gemini）和开源本地模型（如 Llama）之间，John 怎么看？

John 的回答非常明确：

> "Cloud models are underrated. Open source gets a lot of hype and excitement, but follow the money. It's all going to the closed source models because they're really darn good. So much work has been done for you."
>
> "云端模型被低估了。开源模型获得了大量的炒作和兴奋，但追踪资金的流向，它们都流向了闭源模型，因为闭源模型真的非常好。大量的工作已经为你完成了。"

他强调，闭源模型之间的激烈竞争对应用层来说是最好的事情：

> "I feel like all these companies are just a few months behind each other and for us in the application layer, that's the best thing ever. It keeps the heat on them to keep doing better and better."
>
> "我觉得这些公司之间只是相差几个月，对我们应用层来说，这是最好的事情。这让他们彼此保持压力，不断做得更好。"

**个人感受**

John 在这里展示了一种非常健康的"非技术原教旨主义"。在 AI 圈子里，有一种常见的"开源 = 道德高尚、闭源 = 技术垄断"的倾向。但 John 完全从实用主义出发：什么对用户最好、什么对创业公司最有利，就用什么。这体现了一个由产品思维驱动的创始人和一个由技术思维驱动的创始人在路线选择上的基本差异。

更值得关注的是 John 关于"AI 栈"的论述。当 Greg 提到他曾说过"对 AI 栈竟然如此浅感到惊讶"时，John 修正了这个说法：

> "I would say that our AI stack is broad but shallow. What I mean by that is we actually use a ton of different models, but we often use them in fairly simple ways. Like we get so far with prompt engineering, with providing the right context to the models."
>
> "我会说我们的 AI 栈是**宽而浅**的。意思是，我们实际上用了很多不同的模型，但我们使用它们的方式往往相当简单。比如通过 prompt 工程、通过给模型提供正确的上下文，我们已经能走得很远。"

这是一个极其诚实的陈述。100M ARR 的 AI 产品，居然没有太多"深度"的 AI 技术——没有复杂的 fine-tuning 流水线，没有自研的大模型架构。John 说："I really view that as kind of the whole game here of just it comes back to harness building. Can you get the right context from the user? Can you express the AI's output to the user in the right way? And can you distill all that into things that make the LLM's job really easy?"（我真的把这看作整个游戏的核心——它归根结底还是 Harness 的构建。你能否从用户那里获得正确的上下文？你能否以正确的方式把 AI 的输出呈现给用户？你能否把这一切提炼成让 LLM 的任务变得非常简单的事情？）

**延伸思考**

John 的"宽而浅"策略其实是一种非常精明的**风险对冲**。当你的产品不深度依赖某一个第三方模型时，你就有能力在任何时候切换到更好的模型。当 Anthropic 发布了新模型、OpenAI 发布了新模型、Google 发布了新模型，Gamma 都能在一小时内开始测试它。这种灵活性本身就是一种护城河——不是技术层面的，而是运营层面的。

这也解释了一个有趣的现象：为什么 AI 应用层的公司（比如 Gamma）能够比模型公司自己的产品更快地采用新模型。模型公司的应用产品（如 ChatGPT）与自家模型深度绑定，而 Gamma 这样的应用层公司则可以在多个模型之间自由切换，选择每个任务上性价比最高的模型。

**精华收获**
- 使用第三方模型不是技术债务，而是理性的资源分配选择
- "获取使用量"是早期 AI 创业公司的首要任务，自有模型是后续阶段的事
- 策略应该是"宽而浅"：多模型并行使用，但每个模型的使用方式尽量简单
- 云端模型被低估了；闭源竞争的激烈程度对应用层公司是最有利的局面


### 实验驱动的文化：Gamma 如何用一天 8 个实验来保持竞争力 `[内容范围：第十部分]`

**核心观点**
Gamma 的核心竞争力之一是其**规模化实验能力**。在任何给定时间，他们都有 10 到 20 个实验在运行，其中很多持续不到一天。这种文化让他们能用数据替代猜测，保持产品的进化速度。

**深度阐述**

Greg 提到他和 Gamma 合作过，学到的最重要的事情就是他们运行大量实验。John 验证了这个说法：

> "We run a huge number of experiments. Any given time we probably have 10 or 20 running. And we're cycling through. Many of the experiments last less than a day."
>
> "我们运行大量实验。在任何给定时间，我们可能都有 10 到 20 个实验在运行。而且我们在不断循环。很多实验持续不到一天。"

更令人印象深刻的是 John 的一个具体例子：

> "I'll walk you through one that I just started in the Uber ride over to talk to you. I just fired off eight different experiments because Claude Haiku 5.5 came out yesterday."
>
> "我给你讲一个我在来见你的 Uber 车上刚刚启动的实验。我今天早上启动了八个不同的实验，因为 Claude Haiku 5.5 昨天发布了。"

这个例子生动地展示了 Gamma 的实验速度。在一个新模型发布后的第二天，他们就已经把它部署到了八个不同的任务中，而且 John 可以在一两个小时后就拿到初步数据。

**实验流程**

John 描述了实验的具体流程。当 Claude Haiku 5.5 发布后，Gamma 团队会用它来测试那些不需要大型模型的任务——比如从模板库中选一个模板、基于内容写大纲等。他们同时启动八个不同的测试，然后：

> "Right after we got off this podcast, I'm going to check the results and probably cancel four of them and see how they did."
>
> "播客结束后，我就会去查看结果，可能会取消其中的四个，看看它们的表现。"

这个"快速启动、快速淘汰"的循环是 Gamma 实验文化的核心。

**实验的目标**

John 解释了实验通常能学到什么：

> "The great thing that we learn is that we can use a model that is half the cost of another model and get the exact same results. But sometimes we actually get the opposite finding. We find like, 'Wow, actually the big beefy expensive model is necessary to achieve a certain task.'"
>
> "我们学到的最好的事情是，我们可以用一个成本只有另一个模型一半的模型，得到完全相同的结果。但有时候我们也会得到相反的发现：'哇，实际上这个又大又贵的模型对于完成某个任务是必要的。'"

**一个反直觉的发现：好的摩擦**

John 讲了一个他的假设被推翻的实验。他们测试了一个"快速模式"（fast mode），跳过那些用户流程中的步骤——比如不展示大纲、不预先问问题。他的假设是：减少摩擦会带来更好的用户体验。但结果是：

> "It did not win for us actually. It turns out those speed bumps we had along the way, like seeing your outline and reviewing it, choosing the high-level arc of your story, answering those questions led to much higher satisfaction ratings. Even though it was slower, the people that got through felt more invested in their output and did more. And they actually converted to paying at a higher rate."
>
> "实际上它没有赢。结果发现，我们设置的那些'减速带'——比如查看大纲和审阅它、选择故事的整体走向、回答那些问题——带来了更高的满意度。即使它更慢，但通过这个过程的人对自己的输出更投入，做得更多。而且他们转化为付费用户的比率更高。"

这是一个非常有价值的发现。"摩擦"（friction）在产品设计中被普遍认为是坏事，但 Gamma 的实验证明，**在创意工具中，适度的摩擦可以提高用户对产品的投入感**。当用户参与了故事的构思过程，当他们对大纲做出了选择时，他们就不再是被动接受 AI 输出的人，而变成了创作的参与者。这种参与感直接转化为更高的满意度和付费意愿。

**个性化的实验设计**

John 还提到了一个很微妙的点——同一个实验的结论对不同用户群体可能不同。虽然他一开始说"快速模式没有赢"，但实际上他们把它发布给了**移动端新用户**：

> "We actually shipped a version of fast mode for brand new users on mobile because, you know, on mobile you don't want to be typing a bunch of answers to a question."
>
> "我们实际上给移动端的新用户发布了一个快速模式的版本，因为在移动端你不会想打一堆问题的答案。"

所以"失败"的实验并没有被简单地丢弃。Gamma 从每个实验中提取出更细粒度的洞察，找到不同用户群之间的差异。

**从 Optimizely 学到的教训**

Greg 非常聪明地问了一个问题："你在 Optimizely 工作期间学到的一件事，每个 AI 创业者都应该知道的是什么？" John 在创立 Gamma 之前，曾在 A/B 测试公司 Optimizely 工作过。他的回答：

> "So much of it just comes to how many at-bats you have. It's all just sort of a numbers game just like sales just like dating just like kind of anything else in life. You got to really try a lot of different stuff versus expecting that you'll run one big test that magically unlocks your business."
>
> "很多东西其实就归结于你有多少次'上场击球'的机会。这就像一种数字游戏——就像销售、约会、生活中的其他事情一样。你必须要尝试很多不同的东西，而不是指望运行一个大的测试就神奇地解锁你的业务。"

这个"at-bats"（击球次数）的棒球比喻非常有力。它传递的核心信息是：**成功的概率不是来自某一个天才的决策，而是来自尝试次数的累积**。你不需要每一次都命中，你只需要足够多次的尝试，让统计学规律为你工作。

**个人感受**

John 在描述实验文化时所用的语言——"fired off"（发射）、"cancel"（取消）、"check the results"（查看结果）——传达了一种随手就可以启动一个实验的轻松感。这种轻松感的背后，其实是一套已经被内化为日常流程的实验基础设施。对于大多数 AI 创业者来说，实验往往被视为一种"需要专门规划的项目"，但在 Gamma，它已经变成了日常运营的一部分。

Greg 后来提到了"trough of sorrow"（悲伤之谷）的概念，这是创业圈中用来描述"努力了但看不到结果"的阶段。John 对此的回应是："All success in life comes from swimming through some kind of rasa sara."（生活中所有的成功都来自游过某种悲伤之谷。）这句话虽然轻描淡写，但包含了一个深刻的真理：**实验的价值不在于单个实验的成功，而在于持续实验的累积效应**。

**延伸思考**

Gamma 的实验文化实际上指向了一个更深层的组织能力问题：**如何在组织层面上将"实验"变成一种肌肉记忆，而不是偶尔的特别项目？** 从 John 的描述中，我们可以看到几个关键要素：
1. **足够大的用户基数**：能够在几个小时内获得统计显著的结果
2. **基础设施的自动化**：启动一个 A/B 测试的边际成本接近于零
3. **快速决策的文化**：不是"运行两周再分析一次"，而是"明天就取消四个"
4. **对假设失败的开放态度**：John 说 "I was really rooting for this test. I wanted to see it win"——即使他支持快速模式，当数据不支持时，他也能接受

**精华收获**
- 实验能力 = 规模化 + 低边际成本 + 快速决策 + 假设失败
- 在创意工具中，适度的摩擦（用户参与）可以提高满意度和付费率
- 成功来自击球次数，而不是某一次击球的好坏
- 一个"失败"的实验也可能提供有用的洞察，需要深入挖掘


### 营销工程师：一个新物种的崛起 `[内容范围：第十一部分]`

**核心观点**
营销正在进入"工程师化"时代。最顶尖的营销人员不再是创意人，而是能够指挥大量 AI Agent 的"营销工程师"——他们同时拥有数据科学家、增长黑客和创意总监的技能，并且能够在极短时间内运行大量实验。

**深度阐述**

Greg 提出了他最近在社交媒体发表的一个论点——"营销工程师"的崛起。他用一个历史链条来说明营销的演变：
- **Mad Men 时代**（1950-60 年代）：一年做一次大广告
- **数字营销时代**（1990-2000 年代）：每周做几次实验
- **增长黑客时代**：每周做更多实验
- **AI 辅助营销时代**（2022 年起）：每天大量实验
- **营销工程师时代**（现在）：每天几十次实验，由 AI Agent 执行

John 对这个概念非常有共鸣，特别是因为他的 Optimizely 背景。但令人惊讶的是，他首先讲了一个"预警"故事：

> "Before I worked at Gamma, I worked at a company called Optimizely. This is where my love of AB testing came from. And a lot of our vision was about personalization. This is idea that, as it gets easier to change your website, we are going to create a hundred little micro variations of it and everyone will get served a slightly different version and that will optimize conversions. Surprisingly to me, that vision I would say largely has not come true out on the internet."
>
> "在 Gamma 之前，我在 Optimizely 工作。这是我对 AB 测试的热爱的来源。我们的很多愿景是关于个性化的——随着修改网站变得越来越容易，我们会创造上百个微小的变体，每个人都会看到略有不同的版本，这将优化转化率。令我惊讶的是，这个愿景在互联网上基本上没有实现。"

这是一个非常重要的观察。2010 年代，很多科技公司认为"大规模个性化"是数字营销的未来。但这个未来并没有到来——大多数网站仍然是"一刀切"的，App 也一样。John 指出了一个例外：

> "Except for these like specialized areas which are like hyper personalized and succeeding. When I say specialized areas, I mean things like your TikTok feed, your Instagram reels."
>
> "除了一些非常专业的领域——这些领域是超级个性化的，并且取得了成功。我说的专业领域，是指你的 TikTok 信息流和 Instagram Reels。"

**为什么大规模个性化没有普及？**

John 给出了一个非常有趣的解释。他提到了麦当劳测试个性化定价的消息（Greg 提到过这个新闻）：

> "I think there's a real societal allergy to this kind of thing. In the same way that if you found out that we both bought the same airline ticket, but they charged me five bucks more because I was in San Francisco."
>
> "我认为社会对这种事情有一种真实的过敏反应。就像如果你发现我们买了同一个航班的机票，但他们因为我在旧金山就多收了我五美元。"

这种"社会过敏"是真实存在的。人们不喜欢被算法"区别对待"。这种抗拒力量即使在技术完全可行的条件下，也阻止了大规模个性化的普及。

**品牌的力量正在上升**

John 随后提出了一个反直觉的观点：

> "I actually think in this age of hyper-efficient performance marketing, actually what's working is companies that really doggedly invest in their brand. This like Apple mindset of just like protect the brand at all costs."
>
> "我实际上认为，在这个超高效绩效营销时代，真正有用的是那些执着地投入品牌的公司。就像苹果的心态——不惜一切代价保护品牌。"

这就形成了一个有趣的张力：营销工程师拥有大量工具来进行微观优化，但真正成功的企业可能是在宏观层面做品牌投资的公司。

**那营销工程师到底长什么样？**

John 对 Greg 的"营销工程师"概念给出了自己的定义：

> "One thing that comes to mind is they're really a marketing engineer data scientist. So, they are like ultra data-driven and grounded in what's performing. This is something that's gotten easier than ever. Like absolutely Claude is my data scientist."
>
> "首先想到的是，他们真的是一个'营销工程师数据科学家'。他们极度数据驱动，并对什么在实际表现有清晰认识。这比以往任何时候都容易。Claude 绝对是我的数据科学家。"

然后他描述了 Gamma 内部最接近"营销工程师"角色的人：

> "He is just constantly thinking of new ways to do SEO, ad creative at just an unbelievable scale for one person. They've gone from being like individual creatives to people who are running this army of agents. And they are just in this high-level supervisory role."
>
> "这个人一直在想新的方式来做 SEO、广告创意，这个规模对于一个人来说是令人难以置信的。他们已经从独立的创意人变成了指挥一支 Agent 军队的人。他们处于一种高层次的监督角色。"

**个人感受**

John 在描述营销工程师时表现出的态度是一种复杂的混合：一方面他认可这个趋势的存在和重要性，另一方面他对"全面个性化"的老愿景保持警惕。这种双面性其实体现了一种更深层的判断：**技术能力不等于商业成功**。你的营销 Agent 可以每天运行 100 个实验，但如果你的品牌没有真正建立起来，那些优化最终只是在沙滩上建造的城堡。

Greg 在讨论中说了句非常精彩的话：

> "If you're a top 1% marketing engineer, your surface area of what you're working on isn't just... the surface area is huge. You're looking at SEO, GEO, you're looking at social content, you're looking at paid ads, you're looking at pretty much like all creative brand."
>
> "如果你是前 1% 的营销工程师，你的工作覆盖面不只是……这个覆盖面是巨大的。你要看 SEO、GEO、社交内容、付费广告，基本上涵盖所有创意品牌相关的内容。"

John 对此的回应很直接："The other 98% are quickly becoming dinosaurs."（其他 98% 正在迅速变成恐龙。）这句话的残酷性在于：营销领域确实在发生一次"能力分层"，那些无法与 AI 协作的人正在被时代甩开。

**延伸思考**

营销工程师的崛起实际上是一个更广泛的趋势的缩影：**AI 不是替代了工作，而是重新定义了工作中的人类角色**。一个传统的营销团队成员可能负责写文案、管理社交媒体、优化转化率。但在 AI 时代，这些具体任务都被 Agent 接管了。人类营销人员的角色变成了**监督者、决策者、品牌守护者**。这种转变对人才结构的影响是深远的：最好的营销人员可能不再是创意最强的人，而是最善于管理 Agent 的人。

这与 John 所说的"每个人都获得了快速的职级跃升"相呼应：

> "All of us over the last maybe like year or two, at least all of us who are using these tools kind of got this rapid series of promotions. We went from individual contributor to manager to director to like VP. We now all have these like layers and layers of agents under us in a pyramid. And it turns out that job's actually kind of hard."
>
> "在过去一两年里，至少那些使用这些工具的人，我们都经历了一系列快速的晋升。我们从个人贡献者变成了经理、总监、副总裁。现在我们下面都有了一层层的 Agent，形成一个金字塔。而事实证明，管理这份工作其实挺难的。"

管理这个"Agent 金字塔"是一项新技能。大多数人没有被训练过如何管理一百个 Agent，如何分配任务，如何评估 Agent 的表现。John 的洞察是："Building tools to help the average person become a VP of their own life is still under explored."（帮助普通人成为自己生活的副总裁的工具，仍然是一个尚未被充分探索的领域。）

**精华收获**
- 最顶尖的营销人员正在转变成"营销工程师"——以 AI Agent 为基础的数据驱动决策者
- 大规模个性化的愿景没有实现，原因不是技术限制，而是"社会对区别对待的过敏"
- 在 AI 时代，品牌投资可能比微观优化更有持久价值
- 所有工具使用者都在经历"管理 Agent 金字塔"的技能挑战，帮助普通人做好这件事是一个被低估的机会


### AI 图像模型的低估：能力远超使用场景 `[内容范围：第十二部分]`

**核心观点**
AI 图像模型的能力已经远远超过了人们实际使用的范围。大多数用户只在少数几个固定场景中用到它们。这些模型被低估的原因是：一旦它们变得"好到不再出错"，人们就开始忽视它们的存在。

**深度阐述**

当 Greg 问 John 什么是他认为被低估的技术时，John 给出了一个出人意料的答案：

> "Maybe it's a lame answer, but I actually think AI image models are under hyped. It's a lame answer because we've been talking about image models for years. Ever since like stable diffusion came out in 2022, people have been making like cool stuff. But I think ironically, as they got good, people stopped talking about them."
>
> "这可能是一个平庸的答案，但我认为 AI 图像模型是被低估的。说它平庸，是因为我们已经谈论图像模型很多年了。自从 2022 年 Stable Diffusion 发布以来，人们一直在做很酷的东西。但讽刺的是，当它们变得足够好之后，人们反而不谈论它们了。"

这个洞察非常深刻。AI 图像工具在早期不断犯错误、产生"奇怪结果"时，它们吸引了大量关注（人们喜欢分享那些错误）。但当模型逐渐成熟，不再产生那些"病毒式传播的错误"之后，它们就变成了"基础设施"——被使用但不再被讨论。这就像电力一样，它存在于每个角落，但没有人会为电力的存在而兴奋。

John 继续说：

> "We sort of forgot that we have this unbelievable technology that can make anything. And I think if you look at the way people are using like chat GPT images and a few other, it's kind of just the same three or four use cases over and over."
>
> "我们有点忘记了我们拥有这个可以制造任何东西的不可思议的技术。我觉得如果你看看人们使用 ChatGPT 图像和其他工具的方式，基本上就是反复使用那几个相同的场景。"

**一个具体的例子：买沙发**

John 用了一个极其贴近生活的例子来说明这个差距。他最近买了一张沙发：

> "I actually just bought a couch recently... And I went through this and it was so interesting... It turns out the AI image models are amazing at showing me what the couch will look like, but they're not actually showing me exactly how it's going to measure, right? And there's a huge difference between, let's say, a 68-inch couch and a 58-inch couch if your wall's a certain size. So could you actually show me the units in the display?"
>
> "我最近买了一张沙发……我经历了一个非常有趣的过程……AI 图像模型能够非常好地展示沙发在我的房间里会是什么样子，但它们没有真正展示尺寸。比如 68 英寸的沙发和 58 英寸的沙发，如果你的墙有特定的尺寸，差别很大。你能不能在图像中显示尺寸单位？"

这个例子完美地解释了"垂直 Harness"和"通用模型"之间的差距。图像模型能够很好地生成一个视觉上看起来合理的效果图，但**它不理解物理尺寸这个约束条件**。一个真正的"室内设计 Harness"会结合图像模型的能力和编程的精确性：

> "You could imagine doing a thing where you render the couch in my room, but then you use some good old-fashioned programming to draw a line across in pixels and measure how long it is and see if it actually came out of the right size and prompt the model to tweak it to get exactly right."
>
> "你可以想象这样做：先渲染沙发在房间里的效果，然后用传统编程在图像上画一条线，在像素级别测量长度，看看它是否真的达到了正确的尺寸，然后提示模型调整它，直到完全准确。"

John 的观点是："I don't see the labs doing that anytime soon."（我不认为大模型实验室会很快做这种事。）

**消费者版 vs Prosumer 版 vs 专业版**

在讨论中，John 区分了三个层次的垂直产品机会：

1. **纯消费者版**："帮我买一张沙发" 这种使用场景
2. **Prosumer 版**：给兼职室内设计师的工具——他们有真实的工作需求，会积极寻找最好的工具，愿意付费
3. **专业版**：给大型企业（如 Restoration Hardware 的员工）的工具

John 的建议是关注第二个和第三个层次：

> "Those people need a tool and they will seek out the best. And if it helps them do their job better, they will happily pay a subscription for it. Then there's also the true pros. There's Restoration Hardware itself has people who work there. What tool are they using? I bet it's not just ChatGPT to do all of this. I think there is actually an opportunity to build companies for those. And I do suspect that highest tier of professional, the bigger companies, is where you can really build something durable."
>
> "那些人需要一个工具，他们会主动找到最好的。如果它能帮助他们更好地完成工作，他们会乐意付费订阅。然后还有真正的专业人士——Restoration Hardware 自己有很多员工。他们在用什么工具？我打赌他们不是只用 ChatGPT 来做这些事。我认为为这些人建立公司确实有机会。而且我怀疑最高层次的专业用户——那些大公司——才是你真正能建立持久业务的地方。"

**个人感受**

John 关于图像模型被低估的论述，其实指向了一个更广泛的密码：**当一个技术变得"足够好"以至于不再引起惊叹时，它才真正开始创造价值**。那些在 2022 年因为 Stable Diffusion 生成奇怪图片而嘲笑 AI 的人，到了 2025 年可能正走在旧金山街头，对咖啡馆墙上那些"AI 做的但看不太出来"的海报没有一丝怀疑。技术从"被讨论"到"被使用"的这一步，通常比从"被使用"到"被讨论"的那一步更有商业价值。

Greg 在讨论中提到 levels.io 已经有一个室内设计工具，John 的回应是："There's still room."（还有空间。）这个判断的原因在于：**垂直领域的差异化空间很大**。一个纯靠图像模型的简单工具可能和 levels.io 的产品区分度不大，但一个真正理解室内设计师工作流程、能够处理尺寸精度、品牌风格、预算约束等复杂需求的工具，则有巨大的差异化空间。

**延伸思考**

John 的沙发例子实际上可以扩展为一条产品设计原则：**好的垂直 Harness = AI 模型能做什么 + 传统编程能做什么 的创造性组合**。AI 模型擅长生成灵活、非结构化的内容；传统编程擅长处理确定性的、精确的计算。在大多数真实场景中，你需要的不是纯粹的 AI 或纯粹的传统编程，而是二者的某种混合。

这也解释了为什么"AI 图像模型被低估了"会持续一段时间。因为要释放这些模型的价值，需要的不是"更有创意的 prompt"或"更好的 AI 模型"，而是**一个新的产品层**，这个产品层知道如何把 AI 生成图像的灵活性和确定性的测量、检查、验证结合起来。

**精华收获**
- AI 图像模型的能力超出大多数人实际使用的范围，被低估的原因是其成熟后不再引起讨论
- 释放图像模型的商业价值需要"传统编程 + AI"的组合，尤其是处理精确约束（如尺寸）
- 垂直产品分三层：消费者版、Prosumer 版、专业版——后两者是建立持久业务的方向
- 一个领域从"被讨论"到"被使用"的转变，往往比相反的过程更有商业价值


### 创业的第一原则：爱上你做的东西 `[内容范围：结尾部分]`

**核心观点**
John 留给创业者最重要的建议是：你必须爱你在做的事情——具体来说，是要找到一个"你愿意每天花八小时，而你的朋友们不愿意"的领域。这是支撑你走过创业过程中漫长而孤独的旅程的唯一动力。

**深度阐述**

在访谈接近尾声时，Greg 请 John 给听众留下一条建议。John 的回答：

> "I would just always encourage people who are thinking of starting a business to know that it is a long and sometimes lonely journey. And because of that, you really have to love the thing you're working on."
>
> "我总是鼓励那些正在考虑创业的人，要知道这是一段漫长且有时孤独的旅程。正因为如此，你必须真正热爱你正在做的事情。"

他说这是他的一条核心规则：

> "It has to be something that I could dog food, that I could be a user of and that I could believe in. To be honest, that actually rules out a whole lot of boring businesses, but it was good for my soul. I just needed to have something that I wanted to spend hours every day in."
>
> "它必须是我能亲自使用的东西，我能成为它的用户，我能相信它。说实话，这排除了很多无聊的业务，但这对我的灵魂有好处。我需要有一个我愿意每天花几个小时投入其中的东西。"

**Greg 的补充：marry the niche, date the product**

Greg 补充了一个非常有价值的框架：

> "I always say like marry the niche, date the product. Like fall in love with who you're trying to serve. Because we live in an age where you're going to be iterating on the product so many times and it's going to look so different, but if you love the niche, that's why I always encourage people to build media, build a following in that niche because then you can sell them a bunch of different products."
>
> "我总是说：和 niche 结婚，和产品约会。爱上你要服务的那些人。因为我们生活在一个你会在产品上迭代很多次的时代，它会变得完全不同。但如果你爱的是这个 niche，那你就有了持久的基础。所以我一直鼓励人们在那个 niche 里做内容、建立受众，因为这样你就可以向他们销售各种不同的产品。"

这个框架是对"热爱"的一种更精确的拆解：产品会变，但 niche 不会。如果你爱上的是产品——一个特定功能、一个特定设计——那么当产品需要转变时，你的动力就会消失。但如果你爱上的是**你要服务的人**，那么无论产品如何变化，你的投入感都会持续。

John 用 Jeff Bezos 的名言作为呼应：

> "You know, Jeff Bezos has a very similar quote where he says, 'Be stubborn on the vision, flexible on the details.'"
>
> "贝佐斯有句类似的话：'在愿景上固执，在细节上灵活。'"

Greg 开玩笑说："Well, I'm glad I'm in good company with Jeff Bezos."（我很高兴我和贝佐斯在同一个阵营里。）

**个人感受**

这一段虽然简短，但它是整期播客最"人性化"的部分。在讨论了一个多小时的技术细节、模型策略、实验方法之后，John 用这个建议把话题带回了创业的根本问题——**你为什么在做这件事？** 技术会变化，模型会更新，竞争对手会来，但如果你对所做的领域有真正的热爱，这些困难就会变得可以承受。

值得注意的是，John 并不是在说"做你喜欢的事情就能成功"这种鸡汤。他强调的是一个更具体的标准：**你愿意每天花八小时而你的朋友们不愿意的领域**。这个标准有两层含义：第一，你必须有超出常人的投入意愿；第二，这种投入意愿是你个人独特的——如果你的朋友们都愿意做这件事，那么这个领域就会非常拥挤，你的独特优势就会消失。

**延伸思考**

"Marry the niche, date the product"这个框架其实可以应用到更广泛的创业决策中。很多创业者在选择方向时，会把"我觉得这个功能很酷"或"这个技术很前沿"作为首要标准。但这样的选择很容易在遇到困难时动摇——因为产品和技术都会过时，但你对一个特定人群的理解和服务意愿可以持续几十年。

这和 John 前面说的"找你的领域，那个你了解而我不了解的领域"形成了完美闭环。创业的机会不是挂在树上的果实，等你去摘；而是你在自己生活的土壤里已经种下、正在生长的东西。只有当你真正了解一个领域的人、他们的需求、他们的痛点，你才能构建出真正有用的 Harness——不管是为谁做的、以什么形式。

**精华收获**
- 创业的第一原则：你必须爱你在做的事情，因为漫长的旅程中只有热爱能支撑你
- 判断标准：找到一个你愿意每天花八小时、而你的朋友们不愿意的领域
- Marry the niche, date the product——与你要服务的人群"结婚"，与具体的产品"约会"
- 在 niche 中建立受众（做媒体、做内容）是构建持久创业基础的关键路径

---

<!-- TLDR: Agent Harness 才是 AI 产品的真正壁垒，真正的机会藏在"你比别人更了解的领域"里 -->
<!-- TAGS: AI, 创业, Product, Agent Harness, Gamma --> <!-- RATING: 4 -->
