---
title: "Building a Mobile App with OpenAI Codex (Better than Claude Code)"
channel: "Riley Brown"
published: "2026-03-24"
source_url: "https://www.youtube.com/watch?v=eoEsVQJruow"
video_id: "eoEsVQJruow"
rating: 4
language: "英文"
word_count: 7731
duration: "27:29"
---

# Building a Mobile App with OpenAI Codex (Better than Claude Code)

- **Channel:** Riley Brown
- **Published:** 2026-03-24
- **Source:** https://www.youtube.com/watch?v=eoEsVQJruow
- **TL;DR:** 从不满到创造，用 AI 几十分钟构建一个能构建应用的应用，展示人机协同的新范式
- **Rating:** 4

## 版本

- [结构化文稿](2026-03-24-building-a-mobile-app-with-openai-codex-(better-than-claude-code)-eoEsVQJruow.structured.md)
- [原始文稿](2026-03-24-building-a-mobile-app-with-openai-codex-(better-than-claude-code)-eoEsVQJruow.transcript.md)

# 内容深度重构与阐述

## 材料信息

- **标题**：Building a Mobile App with OpenAI Codex (Better than Claude Code)
- **作者/来源**：Riley Brown
- **类型**：YouTube 视频字幕
- **关键元数据**：视频记录了作者使用 OpenAI Codex 从零构建一个 iOS 应用的完整过程，时长约 30-40 分钟的开发实录，涉及 Swift、Claude Agent SDK、Vibe Code CLI 等多个技术栈
## 开篇引入

想象一下这样的场景：你打开一个号称“让零代码经验者也能构建应用”的平台，却发现界面拥挤、体验混乱，完全不是想象中那个让创意自由流淌的地方。大多数人会选择抱怨几句然后离开，但 Riley Brown 做了一个更疯狂的决定——他要“vibe code”一个属于自己的版本，而且这个版本要具备一个超能力：它能构建其他应用。更令人兴奋的是，他全程不写一行代码。

这不是一个普通的开发教程。这是一个人与 AI 协同工作的真实记录，充满了探索、试错、迭代和惊喜。在这篇文章中，我们将跟随 Riley 的视角，深入体验他如何用 OpenAI Codex 这个桌面应用，在短短几十分钟内，构建出一个名为“Jerry”的 iOS 应用——一个能通过自然语言对话来生成网页应用和移动应用的平台。这不仅仅是一个技术实现的故事，更是一个关于“如何与 AI 共舞”的思维过程实录。让我们一起走进这个充满创造力的开发之旅。

## 详细内容

### 缘起：为什么我要重新造轮子？ `[00:00-01:30]`

**核心观点**

Riley 决定构建自己的应用开发平台，源于对现有工具 Replet 的不满——界面拥挤、体验混乱，这促使他产生了“做一个更好的版本”的冲动。

**深度阐述**

Riley 的旅程始于一个简单而强烈的动机：对 Replet 移动应用的不满。在视频开头，他直言不讳地表达了自己的感受：“Everything is just really small. Everything is really cluttered. And I really don't like the experience of this app.” [00:45] 他形容主屏幕“confusing and boring”，这种体验上的不适感成为他创造的动力。

但更值得玩味的是他的解决思路。大多数人遇到不满意的产品，要么选择忍受，要么寻找替代品。Riley 的选择是：“I'm going to make my own version of Replet without writing a single line of code.” [00:20] 这句话道出了当前时代的重要转变——创造的门槛正在急剧降低。当“不写一行代码”也能构建应用时，每个人都可以成为创造者。

他的目标清晰而具体：构建一个更简单的体验，让它“like Replet except it's going to be a lot more like iMessage” [01:15]。这是一个非常巧妙的定位——将复杂的应用开发流程，简化为像给朋友发短信一样自然的对话。这种“对话式开发”的构想，预示了未来人机交互的一个重要方向。

**个人感受**

Riley 在描述 Replet 时的用词透露出强烈的情感色彩：“I might sound a little harsh. I don't think it's really bad. I just really don't like the UI.” [01:20] 这种带着抱歉却坚定的态度，真实地反映了一个创作者对体验的执着。他不是在否定别人的努力，而是在表达一种对“更好可能”的追求。这种情感是驱动创新的核心动力。

**延伸思考**

Riley 的选择引发了一个更深层的问题：当我们有能力轻松创造工具时，“不满意”是否应该成为行动的起点？在 AI 时代，从消费者到创造者的转变路径正在缩短，每个人都可以对自己不满意的产品说“我可以做一个更好的”。这种民主化的创造力，可能是 AI 带来的最深远影响之一。

### 创意蓝图：Jerry 的诞生 `[01:30-04:00]`

**核心观点**

Riley 将应用命名为 Jerry，构想为一个“智能开发者”形象，通过类似 iMessage 的对话界面，让用户像与朋友聊天一样构建应用。

**深度阐述**

Riley 的创意构想充满了人性化的巧思。他没有把应用设计成一个冰冷的工具，而是赋予了它一个亲切的身份——Jerry。“It's going to feel like texting a really smart vibe coder or a really smart developer named Jerry.” [02:10] 这个命名策略本身就蕴含着深刻的产品思维：通过拟人化，降低用户的心理门槛。

整个工作流程被设计成一个自然的对话循环：

1. 用户发送消息（如“Build me a fitness tracker”）
1. Jerry（由 Claude Agent SDK 驱动）通过多轮对话了解需求细节
1. Jerry 使用 Vibe Code CLI 生成并托管应用
1. 返回应用链接，在应用内预览
1. 用户继续与 Jerry 对话，迭代改进
“The whole process will be a lot more simple, almost like you're texting a friend.” [02:05] 这种设计理念触及了人机交互的本质——最自然的交互方式往往是最简单的。当复杂的技术流程被隐藏在“对话”这一人类最熟悉的形式背后，创造的门槛就真正降低了。

技术层面，Riley 明确规划了三个核心组件：

- **Swift 应用**：前端界面，保存所有消息到本地
- **Claude Agent SDK**：驱动 Jerry 的智能对话能力
- **Vibe Code CLI**：负责沙箱环境和实际的应用生成
**个人感受**

Riley 在描述 Jerry 时，语气中透露出一种孩子般的兴奋。“This is going to be a really fun one.” [01:45] 这种兴奋不是技术宅的炫耀，而是创造者面对一个有趣想法时的纯粹热情。他不仅是在构建工具，更是在创造一个“伙伴”——一个有名字、有性格的智能体。

**延伸思考**

“给 AI 起个名字”这个看似简单的行为，实际上触及了人机关系的核心。当我们与一个叫“Jerry”的智能体对话时，我们的心智模式会不自觉地把它当作一个协作伙伴，而不是一个冷冰冰的工具。这种心理暗示对用户体验的影响可能远超我们的想象。随着 AI 越来越深入地融入生活，这种“拟人化设计”可能会成为产品设计的重要方向。

### 并行工作流：与 Codex 共舞 `[04:00-09:00]`

**核心观点**

Riley 展示了与 AI 协同工作的“并行模式”——同时进行设计、规划、代码生成和调试，充分利用 AI 的并发能力加速开发进程。

**深度阐述**

这是整个视频中最具启发性的部分——Riley 展示了一种全新的工作方式。传统的开发是线性的：先规划，再设计，然后编码，最后测试。而 Riley 的做法是：“When I use Codex, I'm often doing many things in parallel, whether that's research, design, and building the app.” [05:30]

他同时开启多个线程：

- **规划线程**：让 Codex 制定详细的技术方案
- **设计线程**：使用 Paper（一个 AI 友好的设计工具）生成界面设计
- **代码生成线程**：让 Codex 直接生成 Swift 代码
- **调试线程**：随时处理出现的问题
“The better you get with these tools, the more you can work in parallel.” [06:00] 这句话道出了 AI 时代生产力的核心——不是更快地完成一件事，而是同时推进多件事。当你不再需要亲自编写每一行代码时，你的角色从“执行者”转变为“指挥者”，管理多个并行进行的任务成为核心能力。

**视觉/结构信息描述**：

Riley 展示了 Codex 的界面布局，左侧是对话线程列表，每个线程可以独立运行不同的任务。他创建了一个新线程专门处理设计，另一个线程处理代码生成，还有一个线程处理调试。这种多线程架构允许 AI 代理在后台持续工作，而人类可以同时向前推进其他任务。

**个人感受**

Riley 承认这种并行工作方式可能让观众感到困惑：“If I'm moving a little fast, that's just because that's how I work now.” [06:15] 这句话透露出一个重要的信息：人机协同的工作方式正在改变我们对“效率”的认知。当 AI 能够独立完成许多任务时，人类的节奏反而成为瓶颈。适应这种新节奏，需要全新的思维模式和技能组合。

**延伸思考**

并行工作流带来的是一个更深层的转变：从“做”到“指挥”。在 AI 时代，生产力不再取决于你能写多少行代码，而取决于你能同时管理多少个 AI 线程。这类似于一个管弦乐指挥家——不是自己去演奏每种乐器，而是协调各个声部共同完成一首交响乐。这种“指挥者思维”可能是未来工作者的核心素养。

### 调试与迭代：人机协同的精髓 `[09:00-18:00]`

**核心观点**

Riley 展示了与 AI 协同调试的完整流程——遇到错误时，直接将日志和截图反馈给 Codex，让它理解和解决问题，形成高效的迭代闭环。

**深度阐述**

开发过程中必然遇到问题，Riley 的处理方式展示了人机协同的最佳实践。当首次运行应用时，遇到了“data couldn't be read because it's missing”的错误。他没有花时间去解读错误日志，而是：“I'm just going to copy this. We're going to go to Codex and say, I got this message. Please, let's fix this.” [10:30]

这种“将错误交给 AI”的调试方式，体现了对 AI 能力的信任和合理分工。人类负责识别问题和设定方向，AI 负责具体的技术实现。当修复完成后，立即重新运行测试，形成快速迭代循环。

更重要的是，Riley 不仅提供错误信息，还会提供上下文。当遇到“Jerry is thinking through the build”但一直没有实际响应时，他直接截图并描述：“I'm not seeing any response by the agent. And so this should just be like a chat response.” [12:45] 这种“截图+描述”的反馈方式，让 AI 能够准确理解界面状态和预期行为。

**关键迭代过程记录**：

1. **第一次迭代**：解决基础通信问题，让 Jerry 能够响应
1. **第二次迭代**：修复界面格式问题，让消息显示更美观
1. **第三次迭代**：集成 Vibe Code CLI，让 Jerry 具备构建应用的能力
1. **第四次迭代**：解决链接预览问题，让应用链接在应用内打开
1. **第五次迭代**：优化预览界面，让用户可以在预览时同时输入
**个人感受**

Riley 在整个调试过程中展现出的耐心和探索精神令人印象深刻。当遇到问题时，他的第一反应不是沮丧，而是“让我们看看 Codex 怎么解决”。当修复成功时，他会发出“Amazing”这样的赞叹 [14:30]。这种态度反映了与 AI 协作的最佳心态——把 AI 当作伙伴，共同面对挑战，一起庆祝成功。

**延伸思考**

这种“截图+日志+描述”的调试方式，实际上是建立了一种新型的人机沟通语言。我们不再需要精确描述技术细节，而是可以通过最自然的方式（截图、自然语言）来传达问题。这种沟通方式的发展，可能会进一步降低技术门槛，让更多人能够参与创造。

### 最终成果：一个能构建应用的应用 `[18:00-视频结束]`

**核心观点**

Riley 成功构建了一个完整的 iOS 应用，用户可以通过自然语言对话让 Jerry 生成应用，并在应用内直接预览和迭代。

**深度阐述**

经过多轮迭代，Jerry 应用终于成型。Riley 展示了最终成果：

**核心功能演示**：

1. **对话式应用创建**：用户输入“Please create a mobile app that is a todo list app in the style of notion. Make it cool.” [20:00]，Jerry 通过 Vibe Code CLI 开始构建
1. **应用内预览**：生成的链接在应用内自动打开，无需跳转外部浏览器
1. **对话式迭代**：在预览的同时，用户可以通过底部输入框继续提出修改要求
1. **语音输入**：Riley 集成了 OpenAI Whisper，用户可以用语音发送指令
**创新设计点**：

- 将复杂的技术流程包装成“与 Jerry 聊天”的自然体验
- 应用预览和聊天界面融合，用户可以边看边改
- 项目自动命名，降低用户认知负担
- 语音输入让交互更加自然
“We can look at the app, direct the changes, submit the prompt. We see it in this chat like experience. This is a Swift app. We can ship this to the app store.” [最后部分] Riley 的这句话点明了最终成果的完整性和实用性——这不是一个概念验证原型，而是一个可以实际发布的应用。

**视觉/结构信息描述**：

最终界面的核心是双区域设计：上半部分展示应用预览（WebView），下半部分保留聊天输入框。当用户在预览中点击链接时，新的预览内容会在同一区域打开，输入框始终保持可见，允许用户持续对话。底部还集成了语音输入按钮，点击后显示声波动画，记录语音并转文字。

**个人感受**

视频结尾处，Riley 的语气中充满了成就感和兴奋。“Go crazy. Add like 30 features. Do some crazy stuff.” [最后部分] 这已经不是一个开发者的技术展示，而是一个创造者向观众分享自己作品的喜悦。从最初对 Replet 的不满，到最终拥有一个属于自己的、能构建应用的应用，这段旅程本身就是对“创造者时代”的最佳诠释。

**延伸思考**

Jerry 应用的完成，展示了一个重要的趋势：元应用（构建应用的应用）正在成为可能。当 AI 能够帮助构建应用时，这些应用又可以进一步用于构建其他应用，形成创造力的递归循环。这种“应用构建应用”的能力，可能会极大地加速软件创造的民主化进程。

## 精华收获

**核心洞察**

1. **并行工作是 AI 时代的核心生产力**：Riley 同时管理多个 Codex 线程进行规划、设计、编码和调试，这种“指挥者思维”比单纯的“写代码速度”更重要。未来的高效工作者将是那些能够同时协调多个 AI 代理的人。
1. **对话式交互是降低创造门槛的关键**：通过将复杂的应用开发流程包装成“与 Jerry 聊天”的自然对话，Riley 创造了一个任何人都能使用的开发平台。最强大的工具往往看起来最简单。
1. **反馈循环的质量决定迭代速度**：Riley 的快速迭代得益于高质量的反馈——截图、错误日志、清晰的描述。在 AI 时代，提供良好上下文的能力与提出好问题的能力同等重要。
1. **从“不满”到“创造”的路径正在缩短**：Riley 对 Replet 的不满没有停留在抱怨，而是转化为行动。当创造工具的门槛降低时，每个人都可以从消费者转变为创造者。
**可行动的建议**

1. **拥抱并行工作**：尝试同时开启多个 AI 任务，学会管理和协调它们，而不是等待一个任务完成再开始下一个。
1. **优化反馈机制**：当与 AI 协作时，多用“截图+错误日志+清晰描述”的方式提供反馈，这能大幅提升解决问题的效率。
1. **为 AI 设计人设**：在构建 AI 应用时，考虑赋予 AI 一个亲切的身份（如 Jerry），这能显著提升用户体验的友好度。
1. **从小处着手，快速迭代**：Riley 从最简单的聊天功能开始，逐步添加复杂功能。不要试图一步到位，而是通过快速迭代逐步完善。
1. **拥抱“vibe coding”**：不要过度纠结技术细节，相信 AI 能处理好底层实现，把注意力集中在产品体验和创意上。
**改变认知的关键点**

- **AI 不是工具，而是伙伴**：Riley 与 Codex 的关系不是使用工具，而是协同工作。他把问题交给 Codex，与它对话，共同解决问题。这种伙伴关系才是人机协同的正确打开方式。
- **“不写代码”也能创造**：全程不写一行代码，却能构建出功能完整的 iOS 应用。这证明代码只是手段，创造才是目的。当代码不再是障碍时，每个人都有机会成为创造者。
- **创造的门槛正在消失**：从想法到实现的路径正在急剧缩短。Riley 从对 Replet 不满到拥有自己的 Jerry，只用了几十分钟。这种速度意味着“创意”将成为最稀缺的资源。
- **未来属于“指挥者”**：当 AI 能够执行具体任务时，人类的角色从“执行者”转向“指挥者”。懂得如何协调 AI 完成任务的人，将拥有最大的创造力。
---

<!-- TLDR: 从不满到创造，用 AI 几十分钟构建一个能构建应用的应用，展示人机协同的新范式 -->

<!-- TAGS: AI编程, 人机协同, 产品设计, Swift, vibe coding, 创造力 -->

<!-- RATING: 4 -->

---
