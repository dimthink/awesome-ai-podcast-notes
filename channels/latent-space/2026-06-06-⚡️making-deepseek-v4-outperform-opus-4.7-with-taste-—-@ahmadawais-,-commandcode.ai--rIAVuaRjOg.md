---
title: "⚡️Making DeepSeek v4 outperform Opus 4.7 with Taste — @AhmadAwais , CommandCode.ai"
channel: "Latent Space"
published: "2026-06-06"
source_url: "https://www.youtube.com/watch?v=-rIAVuaRjOg"
video_id: "-rIAVuaRjOg"
rating: 5
language: "英文"
word_count: 11914
duration: "40:41"
---

# ⚡️Making DeepSeek v4 outperform Opus 4.7 with Taste — @AhmadAwais , CommandCode.ai

- **Channel:** Latent Space
- **Published:** 2026-06-06
- **Source:** https://www.youtube.com/watch?v=-rIAVuaRjOg
- **TL;DR:** 通过确定性工具调用修复和品味系统，开源模型在编码代理中可以超越最强闭源模型；潜力藏在系统层而非模型本身。
- **Rating:** 5

## 版本

- [结构化文稿](2026-06-06-⚡️making-deepseek-v4-outperform-opus-4.7-with-taste-—-@ahmadawais-,-commandcode.ai--rIAVuaRjOg.structured.md)
- [原始文稿](2026-06-06-⚡️making-deepseek-v4-outperform-opus-4.7-with-taste-—-@ahmadawais-,-commandcode.ai--rIAVuaRjOg.transcript.md)

# 材料信息

- **标题**：⚡️Making DeepSeek v4 outperform Opus 4.7 with Taste — @AhmadAwais , CommandCode.ai
- **作者/来源**：Latent Space 访谈 Ahmad Awais
- **类型**：YouTube 视频字幕 / 深度访谈
- **关键元数据**：无确切录制日期（访谈中提到“今天是5月25日”，以此为参考点），访谈时长约20–30分钟
---

# 开篇引入

当开源模型被贴上“好用但不够好”“便宜但慢”“偶尔天才、经常固执”的标签时，大多数人选择忽略，或者把问题归结为模型本身的能力天花板。但 Ahmad Awais——这位拥有 300 多个开源项目、13 年 WordPress 核心贡献经历、在 COVID 期间就获得 GPT-3 早期访问的AI老兵——没有接受这个天花板。他带着一个看似微小却决定性的发现，重新定义了开源模型在编码代理中的表现：**工具调用困惑（Tool Confusion）**。他通过一套确定性修复逻辑和名为“品味（Taste）”的元神经符号系统，让 DeepSeek V4 不仅追平了行业顶尖的 Claude Opus 4.7，甚至在某些维度上实现了超越。这期访谈不仅是一次技术深潜，更是一次关于“如何真正让LLM理解并执行你的意图”的实战演练；它提醒我们：**模型的潜力，往往被我们自己的错误假设和开发环境的隐性摩擦所掩盖。**

---

# 详细内容

## 从开源到AI：Alias Awais 的旅程与 Command Code 的诞生 `[对话 开场 – 工具混淆前]`

**核心观点**

Ahmad Awais 的职业生涯始终围绕开源、DevRel 与开发者体验展开。COVID 期间的一次病毒式 CLI 项目，让他意外获得了 GPT-3 早期访问权，并促使他萌生了“代码补全”的想法——比 GitHub Copilot 早了整整一年。这个叫做 CLAI 的 CLI 项目，经过六年演变，最终化为专注编码代理的产品 Command Code。

**深度阐述**

访谈开篇，主持人 Swyx 与 Ahmad 回忆起两人在 AI 时代之前的交集——WordPress 社区。Ahmad 介绍自己曾在 Google、Airbnb 工作，担任过 RapidAPI 的 DevRel 副总裁，但最核心的身份是“开源人”。“Everything is semantics after that, you know, my open source work took me places.”（在那之后一切都变得次要了，我的开源工作带我走向了各个地方。）他的 300 多个开源仓库不仅带来声誉，更塑造了他对代码质量和模式的敏锐直觉。

真正的转折点发生在 COVID 高峰期。Ahmad 用 Node.js 写了一个 Corona CLI 生成器，结果迅速病毒式传播。这一项目引起了 OpenAI 联合创始人 Greg Brockman 和 Sam Altman 的注意，他们给予了 Ghada（Ahmad）GPT-3 API 的早期访问权限。Ahmad 回忆道：“那是 2020 年 7 月。Greg 发消息问我：‘你打算用这个 API 做什么？’我告诉他：‘我要用它来建议下一行代码，就像代码片段那样。’”——这比 GitHub Copilot 的首次亮相还要早一年多。于是他着手开发 CLI 工具 “CLAI”（CLI + AI 的俏皮组合），这个项目最后演变成了今天的 Command Code。

在此之后，团队构建了一个名为 LangBase 的 AI 云，达到了每月 12 亿次 agent 运行的规模，并积累了内存基础设施等核心能力。但在经历了六年的探索后，他们最终意识到一件事：“there is only one type of agent, and that is a coding agent. It can do it all.”（只有一种 agent 才是真正通用的，那就是编码 agent。）于是他们坚决地 pivot，将六年积累全部注入 Command Code，一个以 CLI 为核心、面向编码代理的产品。

**个人感受**

Ahmad 多次提到“Funny how things work out”——最初他告诉所有人 Command Code 绝不会成为他的产品，但最终它成为他倾注一切的焦点。这种从“小项目”到“全栈产品”的意外螺旋，充满了开发者独有的执着与自嘲。

**延伸思考**

这段历史提醒我们：AI 产品爆发最肥沃的土壤，往往是早期使用者（如 AI 工程师）在摸索中发现的“意外场景”。Ahmad 对 agent 类型的判断（“只有编码代理才是真正的万能 agent”）也折射出一个行业共识：代码生成是当前最具通用性和实用价值的 AI 场景，它涵盖了理解、规划、执行与调试的全链条。

## 发现工具调用困惑：当模型不再吸取错误教训 `[对话 工具混淆]`

**核心观点**

Ahmad 在处理大量 DeepSeek V4 调用日志时，发现一个反直觉的模式：开源模型（尤其是 DeepSeek V4 Pro）在工具调用出错后，会无视 Zod 错误反馈，顽固地重复同一错误调用平均 56 次。他将此称为“工具混淆（Tool Confusion）”，并认为这是导致很多开发者觉得开源模型“又慢又差”的真正隐性原因。

**深度阐述**

当编码 agent 执行读文件、运行 Shell 命令等工具调用时，如果返回的 Schema 不符合预期（例如错误的参数类型），按照设计，agent 应该根据错误信息自我修正。但 Ahmad 观察到：DeepSeek V4 Pro 拥有一种“alpha male energy”（雄性首领能量），它固执地认为自己的第一次输出才是正确的。即使你返回一个 Zod 验证错误，它也会完全相同地重试五六次甚至更多。平均在数十亿 token 的日志中，每个错误模式出现高达 56 次重复。

Ahmad 对此感到困惑：“作为程序员，我会认为如果我的工具调用失败，我只需把 Zod 错误发回给 LLM，它足够聪明就会纠正。但现实并非如此。” 他提出了一个充满 Vibe 的观点：“这些开源模型在训练过程中，很可能被灌输‘你所有输出都是高质量的’理念——因为它们从更强的模型中学习，并且被不断强化‘老师教我的就是对的’。所以当你给它们纠错时，它们的内在信念是‘我不需要被纠正’。” 这个“vibe”虽然非锐利科学，却与日志数据高度吻合。

更重要的是，Ahmad 发现这不是 DeepSeek 的专属问题。在检查过去 30 天的日志后，他发现 Kimi、MiniMax 等模型也存在完全相同的行为。于是团队开始系统性地对所有调用进行模式分类，最终积累了 **16,000 多个不同的修复变体**。

**个人感受**

Ahmad 在描述这个发现时带着一丝“终于被我抓到”的兴奋，也有对行业现状的戏谑：“很多编码工具隐藏了这些失败日志，所以用户只感觉模型慢，却不知道是工具调用不停重试浪费了 50 多次机会。” 他毫不客气地指出某些闭源工具故意不修复这类问题，因为他们 “don’t care about open models”（不在乎开源模型）。

**延伸思考**

这个发现对从事 agent 开发的人至关重要：模型的“固执”往往不是智力问题，而是训练分发中的“行为默认偏好”。如果你不拦截并施加强制修复，你的 agent 就会在同一个坑里反复掉入浪费时间。更重要的是，这也揭示了“强大即顽固”可能成为开源模型的一个普遍特征。

## 修复逻辑：像数据库迁移一样，确定性修复工具调用 `[对话 修复逻辑]`

**核心观点**

与其容忍 LLM 持续犯错，不如在 agent 层对失败调用进行“先拯救、再暗示”的确定性修复。Ahmad 借鉴数据库迁移的概念，为每一种错误模式编写修复文件（repair file）。每次检测到错误 Schema 时，agent 自动修正数据，返回正确结果，并附带一条“修复提示”。结果令人惊讶：只要模型接受了修复后的正确输出，而无需承受错误反馈的负面情绪，第三次工具调用就会自动变得正确。

**深度阐述**

Ahmad 将修复逻辑比喻为教人开车：当学生即将撞上另一辆车，你不是停下来解释该如何做，而是先救场（修正方向盘），然后再解释为什么救场。“Think of it like you're teaching somebody how to drive a car. And they're about to hit another car. Instead of telling them what to do correctly, you'll first try to save them and then you will explain.”

具体做法：每个修复文件就像一条数据库迁移规则。例如，当 LLM 发送的参数本应是数组类型，却传入了 JSON 字符串时，agent 不返回 Zod 错误，而是坚决将其转换为数组，再给出正确结果，并在后续消息中附加一条“修复提示”：你本应发送数据类型 X，但这里已帮你修正，请下次注意。

这种“先给甜枣再给巴掌”的策略竟然大幅提高了模型的长程稳定性。“The moment you send the result with the repair logic, right after that the third tool call is fixed.”（一旦你发送了带有修复逻辑的结果，之后的第三次工具调用就自动修复了。）模型仿佛突然变聪明了，因为它意识到自己的意图被理解并成功执行，自然愿意接受修正。Ahmad 认为这是因为成功返回的结果强化了正确的行为路径，而错误反馈只会激化它的固执。

这一修复已在 DeepSeek V4、V4 Flash、Kimi、MiniMax 等多个模型上验证成功。修复后，模型不仅错误率大幅降低，创造力和探索能力也随之增强：“Like if they are seeing a lot less tool call errors, they are much more creative. They can explore a lot and they can continue a lot longer.”（如果它们看到更少的工具调用错误，它们会变得更有创造力，探索范围更大，持续会话的时间也更长。）案例中，某用户在 Command Code 上使用 DeepSeek 完成了累计 700 亿 token 的 12 小时连续会话，甚至撑爆了团队的使用量统计页面。

**个人感受**

Ahmad 多次强调“I made a bunch of that completely open”（我已经将这部分完全开源了），体现了他作为开源践行者的本色。他不认为这种修复是独门秘诀，而是希望整个社区都能受益：“You can go and implement this in any coding harness.”（你可以在任何编码框架中实现这个方案。）

**延伸思考**

这一修复哲学值得所有 agent 构建者深思：**与其依赖 LLM 内化“不犯错”，不如在系统层面提供容错与修复层。** 这本质上是对“CoT + 纠错”范式的实用化替代：不需要模型变得更“听话”，而是让工具层变得更聪明。它把“模型灵活性”转化为“系统鲁棒性”，是 agent 工程中“确定性 vs 概率性”的一个优秀平衡点。

## 品味系统：从编码偏好到自动学习技能 `[对话 品味系统]`

**核心观点**

Command Code 的核心差异化之一是“Taste”（品味）——一个元神经符号系统，它能自动学习每个开发者在每个仓库中的编码偏好（例如“用 pnpm 但 CLI 链接用 npm”、“测试框架用 Vitest 不用 Jest”），并将其自动维护为轻量、透明的技能文件（Taste Files）。这些文件不只存在于仓库中，还会随着开发者行为变化自动更新，永不失效。这可以大幅减少开发者反复纠正 agent 所花费的“steer”时间。

**深度阐述**

Ahmad 解释了他的初心：“I have a lot of experience with code. After publishing 300 plus open source projects, you get to have a lot of opinions on things. And I find myself working on super cutting edge things where there are no docs that an AI agent can go read. So my opinions matter more than what an LLM can find with RAG or anything.”（我有超过 27 年编码经验，300 多个开源项目让我形成大量偏好。更何况我经常处理最前沿的问题，几乎没有文档可供 agent 查阅。因此，我自己的喜好比 LLM 通过 RAG 检索到的任何信息都重要。）

于是他设计了 Taste——一个隐喻为“meta-neuro-symbolic model”（元神经符号模型）的系统，它本质上是一组自动提取并由 confidence score 标记的技能规则。Taste 不是手动编写的规则列表（那种 grandiose 的大规则往往过时且无用），而是**自动学习的微观决策集合**。比如，当 agent 发现开发者在某仓库中每次提交前都先 fetch 最新主分支、rebase、创建 PR 再切回主分支，这个模式就被记录为一条技能，confidence 动态更新。

最关键的设计原则：**Taste 文件是透明的、存储于 git 仓库中的 Markdown 文件，每次 PR 都会参与代码审查**。“They're never stale. A lot of issues that people face are because their agent.md or CLOUD.md has some wrong information when they sat down.”（它们永远不会过时。很多人遇到的麻烦正是因为他们当初写的 agent.md 或 CLOUD.md 是错的。）而 Taste 由系统持续维护，用户可直接编辑，也可删除不想要的规则。团队早期曾尝试隐藏这些学习结果以制造“Wow Moment”，但发现这导致跨分支合并的严重冲突。“We cannot judge what you want to keep. So we made it very transparent.”（我们无法替你判断保留什么，所以它必须完全透明。）

在实践层面，Ahmad 展示了一个只有 20 行左右的 CLI 构建 Taste 文件，涵盖版本号起始、依赖管理、交互库偏好等。只需 `npx taste pull` 即可将 Taste 文件拉到任意仓库。之后只要对任何 agent 说“Follow my taste of building CLIs”，agent 就能自动遵守所有规则。同时，Taste 支持在不同仓库中生长不同版本，自动适应项目个性。

**个人感受**

Ahmad 在谈论 Taste 时流露出一种“终于可以少说废话了”的轻松感：“I tried to hide it very well in the docs somewhere, so developers don't have to go read those silly things.”（我尽量把它藏在了文档深处，这样开发者就不用读那些无聊的东西了。） 这是对繁重提示工程的一种幽默对抗。

**延伸思考**

Taste 系统是个人化 agent 智能的雏形。它不再依赖大而全的指令集，而是通过行为追踪进化成“代理版的 dotfiles”。随着 agent 成为开发者的第二大脑，这种自动化学习、去中心化存储的 taste 系统有望取代传统 prompt 模板，成为知识沉淀的新范式。它也可以看作是人类知识蒸馏到 agent 层的桥梁。

## 设计救赎：同样的修复逻辑如何破解 AI 设计俗套 `[对话 设计修复]`

**核心观点**

Ahmad 的团队发现，工具调用修复的逻辑完全可以迁移到设计领域。他们将 LLM 常见的设计恶习（如“靛蓝紫色渐变”、“无意图的卡片布局”）归因为“设计 slop”，并通过相同的方法——总结有限数量的设计模式与设计气味（design smells），再用确定性修复与引导框架来约束 LLM 的输出，使得工程设计质量大幅提升。

**深度阐述**

AI 生成的设计代码总带有一种“典型的 AI 感”——熟悉的靛蓝紫色渐变、顶部分割线、三卡片并排布局等等。Ahmad 称之为“design slop”。这并非 LLM 的能力不足，而是缺乏对“设计意图”的理解。Ahmad 与多位资深设计师进行了深度访谈，提取出一套只有 **7 种设计模式** 和 **10 个设计气味** 的极简框架。例如，设计仪表盘时，大部分设计师会首先思考“监控 surface 的意图”，而不是直接画三个卡片。把这套框架纳入 agent 的“设计技能”中，效果立竿见影。

具体做法：在 Command Code 中以 `/design skill` 形式提供打包技能，当 agent 被要求“设计更漂亮”时，内部触发一个组合框架——先判断意图，再挑选模式，最后在色板、间距、层次等方面遵守一系列规则。比如，“强迫 LLM 使用 OKLCH 替代 HSL 色彩模式，因为 HSL 在控制亮度时对 LLM 极不友好，而 OKLCH 能准确控制视觉一致性”。

Ahmad 强调“This is not a capability gap. It's more like a contract gap.”（这不是能力差距，而是合约差距。）所谓“合约”指的是开发环境（agent harness）与 LLM 之间的沟通方式。大多数设计失败是因为用户指令（“make it pop”）过于模糊，而 agent 又缺乏设计思考的框架。如果 harness 能提供这种框架，LLM 自己其实会设计得非常好。

**个人感受**

Ahmad 表达了他对设计的深厚感情：“I wanted to be a designer. I was never really good at it, like I couldn't sketch. But now everyone can build anything, and we differentiate between good and bad work based on design. Enabling every builder to design like a designer is very close to my heart.”（我过去一直想成为设计师，但我不擅长素描。现在每个人都能构建任何东西，而区分好作品和差作品的关键就在于设计。让每个构建者都能像设计师一样设计，这对我来说至关重要。）

**延伸思考**

这其实是工具调用修复逻辑的更大推广：**任何可模式化的“品味”都可以被工程化。** 当开发者从设计师那里总结出这 10 个设计气味时，它就变成了可复用的确定性规则。未来，代码、设计、安全、文档——甚至架构决策——都可以通过类似方法固化到 agent 的技能层。这是一种“人教 agent，agent 教人”的螺旋进化，也暗示着一种新的知识压缩方式：将人类直觉压缩为少数确定性规则，再赋予 agent 弹性执行。

## Command Code 的独特哲学与未来 `[对话 哲学与开源]`

**核心观点**

Ahmad 详细阐述了 Command Code 的产品哲学：不走“所有模型都支持”的 Windows 路线，也不走“完全自定义”的 Linux 路线，而是走“精选最佳模型、但保证高度可 hackable”的 Apple 路线。同时，团队决定将所有代码开源，让用户能修改任何部分，无论商业方向如何。

**深度阐述**

面对当前编码工具五花八门的局面，Ahmad 给出了一个精妙的比喻：“There are three philosophies. One is like Windows—every game works with it. I think Open Code is like that. One is like Linux—you build your own drivers like Pi. With Command Code what I'm thinking is like Apple—it will have the best of the best models, both open and closed. It will not have every model, but it will be hackable in any way.”（三种哲学：Windows——所有游戏兼容。我认为 Open Code 就是这种。Linux——你可以自己写驱动。我想把 Command Code 做成 Apple——它会精选最好的模型，既包括开源也包括闭源，同时任何部分都允许修改。）

这个定位意味着 Command Code 不会成为模型数量竞赛的参与者。它只支持经过验证、最能胜任任务的模型（DeepSeek 系列、Kimi、MiniMax 以及闭源模型）；但用户可以通过编写自己的适配器添加任何模型。这种“有限支持 + 高度可扩展”的模式兼顾了默认体验的一致性与高级用户的自由度。

另一个重磅消息是即将开源。Ahmad 提到“I've been working very hard on that. My background is also open source—I spent 13 years in WordPress core. Matt Mullenweg is actually one of our angels now. When he heard we are open sourcing Command Code, he reached out.”（我在这上面非常努力。我花了 13 年在 WordPress 核心。Matt Mullenweg 现在是我们的一位投资人。当他听说我们要开源 Command Code 时，主动联系了我们。）开源的目标是让 Command Code “completely hackable”（完全可 hack），从而消除用户的锁入担忧，并吸收社区贡献。

**个人感受**

Ahmad 对开源的选择充满感情，也带着一丝自嘲：“I told everybody and their mothers and brothers that this will never be my product. Funny how things work out.”（我曾告诉所有人这绝不会成为我的产品。世事难料啊。）这种从“副项目”到“主产品”再到“准备开源”的过程，折射出一个纯粹的开发者对开放生态的信仰。

**延伸思考**

Command Code 的开源将对编码代理市场产生连锁影响。目前大量工具依赖闭源 harness 来绑定特定模型；开源版本一旦放出，底层的高级修复（16,000+ 修复变体）和品味系统将成为公共基础设施，大幅降低其他 agent 开发者门槛。同时，它对应的是一个更公平的竞争环境：用户不必因为 harness 的偏见而低估开源模型的真实能力。这可能加速整个行业从“模型竞争”转向“系统竞争”。

## 开源计划与社区影响 `[对话 结语]`

**核心观点**

Ahmad 透露，开源 Command Code 的具体时间点定在即将到来的 AI Engineering 大会上，前提是能够处理好拥有六年历史的代码仓库的诸多 quirks。同时，团队预判这一举动会促使更多公司推出自己的编码代理（例如 DeepSeek 已在社区评论后宣布招聘以构建 DeepSeek Code），但 Ahmad 认为每个代理都会有各自专注的模型范围，Command Code 的多元模型支持仍将是其独特优势。

**深度阐述**

在评价开源计划时，Ahmad 分享了一个细节：“Six years old? Wait, hang on. Six years old? Oh, because it was a CLI before. Yeah, I get stuff.”（六年？等等，六年？哦，因为它在那之前就是个 CLI。是的，我明白了。）那段因 CLAI 开始、中途转向 LangBase、再 pivot 为 Command Code 的复杂历史，导致代码库积累了大量遗留代码，开源前必须进行一次重构。但他坚信这值得。

他还特别指出，DeepSeek 在被社区大量 @ 后，宣布了招聘以构建 DeepSeek Code 的消息。但 Ahmad 认为，这类专用代理只支持自身模型，而 Command Code 对多模型的支持（尤其是闭源与开源并重）会依然是很多开发者的首选。目前，DeepSeek V3 和 V4 是 Command Code 社区最常用的开源模型之一，GPT 继续保持领先，Claude 紧随其后。

**个人感受**

在访谈结尾，他再次强调了共享知识的重要性：“I think everybody can learn. It's not just for Command Code. You can just use it in any coding harness that you want, right? As far as we are all improving, right?”（我认为所有人都能从中学习。它不只能用在 Command Code 里，你可以在任何编码框架中使用它。只要我们大家都在进步，不就是好事吗？）这句话再次凸显了他作为开放社区的长期贡献者的内心准则。

**延伸思考**

这种大规模开源的举措，可能会催生新的 agent 治理规范：如果修复逻辑和品味系统成为开源标准，那么未来的 agent 工具将不再只是 LLM 评估的裁判，而是成为共享的“智能基础设施”。更重要的是，它向整个行业证明：**解码模型真实潜力的钥匙，并不总是在模型内部，而常常握在系统工程师的手中。**

---

# 精华收获

- **发现工具调用困惑**：开源模型（尤其是 DeepSeek）对错误反馈具有高度“顽固性”，会重复同样的错误平均 56 次。这不是能力问题，而是训练分发中的行为习惯。
- **确定性修复胜过概率性纠正**：与其纠错，不如在工具层直接修正数据，再返回成功结果并附带提示。这种“先救场再解释”的方法能调教模型变得更聪明。
- **Taste 系统：自动化且透明的技能学习**：不再是手写数百行 agent 规则，而是让系统自动从你的每一次选择中学习，形成存储于 git 仓库的轻量技能文件，永远不 stale。
- **设计 Slop 终结方案**：将设计直觉编码为 7 种模式、10 种设计气味的确定性框架，通过 agent 层的强制执行，使 LLM 输出超越“靛蓝紫渐变”的千篇一律。
- **可靠的开源工程哲学**：Command Code 选择 Apple 式精品模型 + 高度 hackable 的开源路线，放弃“一切兼容”的广度，换取深度优化和用户自主权。
- **正确的 agent 脚手架**：任何编码 harness 均可复制这套修复方法，提高开源模型的实用度，让“成本 + 质量”的平衡向开源倾斜。
---

<!-- TLDR: 通过确定性工具调用修复和品味系统，开源模型在编码代理中可以超越最强闭源模型；潜力藏在系统层而非模型本身。 -->

<!-- TAGS: 开源模型, 编码代理, 工具调用修复, 品味系统, 设计Slop -->

<!-- RATING: 5 -->

---
