---
title: "How Jev Turns AI Into Software That Gets Things Done"
channel: "a16z"
published: "2026-09-28"
source_url: "https://www.youtube.com/watch?v=Ut3LOjKNJaE"
video_id: "Ut3LOjKNJaE"
tags: ["AI", "软件工程", "自动化", "创业", "大模型"]
rating: 4
language: "英文"
word_count: 25590
duration: "42:24"
---

# How Jev Turns AI Into Software That Gets Things Done

- **Channel:** a16z
- **Published:** 2026-09-28
- **Source:** https://www.youtube.com/watch?v=Ut3LOjKNJaE
- **TL;DR:** AI一直在聊天，却很少成事——Jev把大模型变成软件内部的"智能原语"，让自动化第一次真正落地。
- **Tags:** AI, 软件工程, 自动化, 创业, 大模型
- **Rating:** 4

## 版本

- [结构化文稿](2026-09-28-how-jev-turns-ai-into-software-that-gets-things-done-Ut3LOjKNJaE.structured.md)
- [原始文稿](2026-09-28-how-jev-turns-ai-into-software-that-gets-things-done-Ut3LOjKNJaE.transcript.md)

# 深度重构：AI的智能不该被困在聊天框里——TypeSafe创始人Diego谈Jev如何让AI真正"成事"

## 材料信息

- **标题**：How Jev Turns AI Into Software That Gets Things Done
- **作者/来源**：a16z（硅谷顶级风投）播客访谈
- **材料类型**：YouTube 视频字幕（对话访谈）
- **关键元数据**：a16z 播客节目，主持人为 Martine 与另一位主持人，嘉宾为 TypeSafe 创始人 Diego；无明确时长标注，内容为深度技术对话

---

## 开篇引入

"AI 如此惊人地聪明，却在实际工作中如此无用。"

这句话听起来像悖论，却是 TypeSafe 创始人 Diego 面对 a16z 镜头时抛出的第一颗炸弹。当整个 AI 行业都在追逐更聪明的模型、更宏大的 AGI 叙事、更炫酷的演示视频时，Diego 和他的团队选择了一条截然不同的路：不是让 AI 变得更聪明，而是让 AI 真正成为软件的一部分——成为程序员可以信赖、嵌入到代码内部的"智能原语"。

这场对话之所以值得深度关注，不仅仅因为它是一次产品发布访谈，更因为它是一场关于 AI 行业方向的真诚辩论。Diego 带着新模型 Jev——一个他声称能"让软件真正自动化"的 AI 组件——与 a16z 的两位合伙人展开了一场关于自动化困境、软件本质、以及 AI 行业"过度承诺、交付不足"现象的深入对话。在这场对话中，我们能看见一位真正的计算机科学家如何看待当前 AI 热潮，为什么他相信"构建产品而非造神"才是 AI 的正确道路，以及为什么他乐观地断言：AI 最终会创造更多、更好的工作，而不是终结它们。

---

## 第一章：灵魂拷问——"他妈的自动化都去哪儿了？"

### [章节 1：开场与电梯演讲]

**核心观点**

Diego 用一句粗粝却精准的话概括了他创办 TypeSafe 的初心："Where the f*** is all the automation?"（他妈的自动化都去哪儿了？）这不仅仅是一句宣泄，而是对整个 AI 行业的悲剧性诊断：我们拥有惊人的智能，却没能将其转化为现实世界的自动化能力。

**深度阐述**

当主持人问到"什么是 Jev？什么是 TypeSafe？为什么它很重要？"时，Diego 坦言自己不擅长电梯演讲，但他发现最喜欢的电梯演讲恰好就是那句灵魂拷问：

> "Where the f*** is all the automation? Like this is like so unbelievably tragic, you know, so much intelligence. AI is so unbelievably smart and yet so not that I hate on chat bots or coding agents. I love them myself, but it's like it's so useless at all other stuff and it's tragic."
> （"他妈的自动化都去哪儿了？这是如此令人难以置信的悲剧。如此多的智能。AI 如此惊人地聪明，我不是在贬低聊天机器人或编码代理——我自己就很喜欢它们——但它在其他所有事情上如此无用。这太可悲了。"）

Diego 用了一个极具画面感的比喻：我们有大量的"rough diamond"（璞玉），却无法为工作场景打磨它们。"It's tragic that we have so much diamond in the rough but not polished for work."——我们有太多未经打磨的钻石，却无法投入使用。

这句话揭示了当前 AI 行业最深层的矛盾：模型的智能水平在实验室里突飞猛进，从数学推理到代码生成，从图像识别到自然语言理解，各项基准测试不断刷新。但回到现实世界，我们日常生活中的大多数流程依然笨拙如故：客服系统需要人类排队等待，企业后台充斥着大量手动重复操作，软件之间的数据流转支离破碎。人工智能的"智慧"似乎被困在了聊天窗口里，无法渗透到软件系统的毛细血管中。

TypeSafe 的回应是："We want to make AI powerful not just for humans in the loop, but to actually build real software. And Jev is our first model in this whole space to make automation way, way better."（我们想让 AI 不仅对"人类介入"的场景有用，还能真正构建软件。Jev 是我们在这一领域推出的第一个模型，目的是让自动化变得好得多。）

**个人感受**

这段开场的情感冲击力在于 Diego 的表达方式。他不是在做冷静的技术分析，而是在表达一种近乎痛心的遗憾。对于一个毕生致力于计算机科学的人来说，看到人类最伟大的技术创造却"无用武之地"，这种感受是复杂的。他之后在访谈中补充说："It pains me when the world is discordant with reality"（当世界与现实脱节时，我感到痛苦），这种情绪贯穿了整个对话。

**延伸思考**

"自动化都去哪儿了"这个问题，实际上指向了一个长期的自动化悖论：尽管技术能力在指数级增长，被自动化的任务范围却增长缓慢。从 1990 年代的"信息高速公路"到 2020 年代的"AI 革命"，每一代技术都被寄予了自动化的厚望，但最终我们得到的不过是聊胜于无的辅助工具。Diego 的追问击中了一个盲点：当我们说"AI 很聪明"时，我们到底在衡量什么？如果智慧不能转化为行动，不能嵌入到系统中，那它对于改善世界的价值就极其有限。

**精华收获**

- TypeSafe 的创立动机源于一个简单却深刻的问题："自动化都去哪儿了？"
- AI 的智能必须被"打磨"才能在工作中发挥作用——这是 Jev 存在的理由
- 核心诉求不是更聪明的 AI，而是更有用的 AI

---

## 第二章：云代码 vs. 智能软件——两种截然不同的 AI 路线

### [章节 2：Cloud Code、Codex 与 Jev 的本质区别]

**核心观点**

Diego 区分了两种 AI 与软件结合的方式："即时软件"（in-time software）与"智能软件"（smart software）。前者是自动生成传统代码，后者是扩展软件本身的表达能力——让软件拥有超越逻辑门的"思考"能力。

**深度阐述**

主持人抛出了一个尖锐的问题："每个人都会想，我们已经有 Cloud Code、Codex 了，Jev 有什么区别？"

Diego 首先肯定了他对这些工具的欣赏，并引用了 Y Combinator CEO Gary Tan 的精彩描述——"in-time software"（即时软件）。Cloud Code 和 Codex 这类工具的美妙之处在于，它们能"即时生成软件"，你可以用自然语言编程，而它们输出的代码具有与传统软件相同的表达能力。这确实是一项了不起的成就。

但 Diego 想要的不是这个：

> "What I want instead is smart software. Instead of like automating software engineering, I want to expand what software itself can do such that things that should be automatable can then be automatable."
> （"我想要的是智能软件。不是自动化软件工程，而是扩展软件本身的能力，让那些本应可自动化的事情真正变得可自动化。"）

这番话值得反复咀嚼。今天讨论 AI 编程时，默认的框架是：AI 像一个更快的程序员，能写代码、能修复 bug、能生成函数。但 Diego 提出了另一个可能性：AI 不是替代程序员，而是成为软件内部的"新器官"——一个可以嵌入到任何程序中的智能组件，让程序本身获得以前不可能拥有的能力。

他继续展开这个愿景：

> "In a more flowery language, I want to express things like intent. I want to expand the vocabulary of what we can do... Programming is like hyper-specifying valuable things and then infinitely replicating them. It's so freaking cool and I want to just make that more."
> （"用更浪漫的语言说，我想表达意图。我想扩展我们能力表达方式的词汇量。编程的本质是超规格化有价值的事物，然后无限复制它们。这太酷了，我想让它变得更丰富。"）

主持人 Martin 敏锐地捕捉到了核心区别："所以不能把它理解为替代软件工程师的工具，而是让软件工程师变得更强大、能写出更好、更有趣的东西。"Diego 同意，并强调"太多人错过了这个点"——这个点如此微妙却如此重要。大多数讨论 AI 编程的人，都把 AI 当作"更好的打字员"，而 Diego 看到了 AI 作为"软件内部的决策单元"的可能性。

进一步的技术解释来自 Diego 对 Jev 接口的描述：

> "Think of it like a library that you can use natural language to describe what you want and you give it kind of a state machine and then it will choose what to do with some confidence levels which we kind of haven't really had before so ubiquitous."
> （"把它想象成一个库，你可以用自然语言描述你想要什么，然后给它一个状态机，它会带着某种置信度选择做什么——这种东西过去从未如此普及。"）

这段话揭示了 Jev 的核心设计哲学：它不是凭空生成整段代码，而是在一个状态机的约束下做出决策。它像一个传统软件库一样被调用，但与传统库不同，它接受自然语言输入，有自己的"判断力"，并且带着概率和置信度工作。这是一个全新的编程原语（primitive）——程序员可以在代码中嵌入一个"会思考的小组件"，而不是简单地调用一个确定性函数。

**个人感受**

当 Diego 说"太多人错过这个点"时，他的语气带着一种轻微的急切。这种急切不是傲慢，而是源于他看到了一种被广泛忽视的可能性时的兴奋与着急。这种"想要告诉全世界"的情绪非常有感染力——你几乎能感受到他对软件本身的热爱（他后来说："I love software so much. I wish I could be writing it all day."（我太爱软件了，真希望能整天写代码）），以及他对于 AI 行业"守着金山讨饭吃"的惋惜。

**延伸思考**

这一区分可以类比到计算机历史的两个方向：一种是用更好的工具做同样的事情（比如编译器优化），另一种是发明全新的抽象层（比如从机器语言到高级语言）。Cloud Code 属于前者——它让编写同样软件的速度更快；而 Jev 属于后者——它尝试创造一种软件组件，用自然语言描述**意图**，然后由 AI 决定如何执行。这不仅是效率的提升，而是表达能力的扩展。

Diego 还提到了一个重要的设计细节：Jev 的输入接口叫做"state"（状态），这是故意设计的——"it's meant to be the insides of programs"（它意味着程序内部的东西）。这个细节印证了他的哲学：Jev 从诞生之初就不是为了"与人类对话"，而是为了成为程序的一部分。

**精华收获**

- 用 AI 自动生成传统代码 ≠ 用 AI 扩展软件的能力边界
- "自然语言 + 状态机 + 置信度"是一个全新的编程原语
- Jev 的输入接口命名为"state"，揭示了它为程序而生，而非为人类对话而生

---

## 第三章：从数学小子到 OpenAI——Diego 的另类旅程

### [章节 3：个人背景故事]

**核心观点**

Diego 的 AI 之路充满"非主流"色彩：曾是获奖数学竞赛选手却讨厌数学，靠"系统化暴力解法"赢得 Kaggle 竞赛，被 SVM 联合发明人 Isabelle Guyon"收养"，随后经历了创业、Google Brain、OpenAI 的职业生涯。这段旅程塑造了他独特的身份认同："在成为 AI 研究者之前，我更是一个计算机科学家。"

**深度阐述**

主持人提出了一个非常有趣的问题："是什么炼金术造就了 Diego？你说话像 AI 研究者，又像系统专家，又像程序员——这些角色通常不怎么重叠。"

Diego 的回答始于自嘲。他坦白自己曾是一个"获奖数学选手"（award-winning mathlete），然后用了一个令人捧腹的方式描述这段经历："我数学好到能吸引女孩。"（"I was good enough at math to get girls."）另一位主持人立刻追问："那么好到什么程度？能吸引什么样的女孩？"这引发了全场笑声，Diego 慌忙劝告年轻人："孩子们，别这么做，不值得。还是做个酷一点、冷静一点、有趣一点的人吧……不要过度补偿。"（"Don't do it. Youth, don't do it. It's not worth it. Just be cool and chill and interesting and don't overcompensate."）

玩笑背后是真实的矛盾。Diego 坦言他"从未真正喜欢过数学"，也"从未真正努力过"，只是一个"小池塘里的大鱼"（big fish in little pond）。数学对他来说是一条被安排好的道路，但他讨厌它，因为数学总是与竞赛和胜负绑定在一起。直到他发现计算机科学——"数学基本上就是数学，但酷、有用、有趣"——他才找到了真正的热爱。他至今仍然喜欢出算法面试题："这是对我来说最棒的事情……它能让我很好地了解一个人的性格。"

后来的转折点来自 Kaggle。Diego 用一句话概括了他赢得 Kaggle 竞赛的方法："不是来自复杂的数学，而是来自把一切都自动化了"（"not from sophisticated math but from just automating the f*** out of it"）。他用更多的嵌套循环、更多的系统化工程方法解决了问题——"我像一个系统问题一样解决了它"。

这次获胜引起了组织者 Isabelle Guyon（SVM 的联合发明人）的注意。Diego 回忆说："她基本上看到了我这个人并不真正适合研究社区，然后收养了我，带我认识所有 AI 人物，我的职业生涯就被推向了那个方向。"从被迫在 NeurIPS（机器学习顶级会议）演讲——"通常是一种荣誉，但我讨厌它，因为我只想去'矿场'里干活"——到与 Jeremy Howard 一起创业，再到 Google Brain，最后进入 OpenAI。

**个人感受**

Diego 在讲述这段经历时的自嘲和坦率令人印象深刻。一个赢得 Kaggle 竞赛、在 NeurIPS 演讲、在 Google Brain 和 OpenAI 工作过的顶级 AI 研究者，却用"我从未真正喜欢数学""我总是被推着走"来形容自己的经历。这种不端着的态度与 AI 行业的"大人物文化"形成了鲜明对比。"我从不想站在台前"——当他这样说时，你能从他身上看到典型的系统工程师性格：喜欢解决问题本身，而不是谈论解决问题这件事。

**延伸思考**

Diego 的旅程展示了"偶然性"在职业发展中的作用：如果 Isabelle Guyon 没有"收养"他？如果他没有被推向 AI 研究的舞台中央？每一个偶然的转折都塑造了今天的 TypeSafe。这也启示我们：在 AI 这个充满不确定性的领域，最有趣的观点往往来自那些"不完全属于任何部落"的人——他们既理解研究，又理解工程，还能跳出来批判两种文化的盲点。他对自己身份的定位——"计算机科学家而非 AI 研究者"——决定了他后来对 AI 行业"重研究轻工程"倾向的批判视角。

**精华收获**

- "数学是数学，但计算机科学是数学但酷、有用且有趣"——找到热爱的关键在于发现"有用的数学"
- 用系统化工程思维解决机器学习问题，同样能赢得 Kaggle 竞赛
- 非典型路径（Kaggle → 创业 → Google Brain → OpenAI）塑造了 Diego 的独特视角

---

## 第四章：RLHF 时刻与"幻灭"

### [章节 4：OpenAI 岁月与通用性的发现]

**核心观点**

Diego 在 OpenAI 经历了从"认为该模型有相当机会成为 AGI"到"幻灭后重新定位"的思想转变。2017 年就提出"AI 模块化而灵活"的他，被 2021 年底 RLHF 展现的"通用性"震惊，但也因此看清了 AI 行业的根本问题：人类在优化"裁判"而不是优化"自动化"。

**深度阐述**

主持人提到，早在 2017 年他们与 Diego 聊过，当时他的很多想法——数据的重要性、专注于任务本身——就已经成形。Diego 回忆说，那年的演讲题目大约叫"AI modular in theory and flexible in practice"（AI 在理论上模块化，在实践中灵活），这与今天的 Jev 理念一脉相承。

真正的灵感火花出现在 ChatGPT 之前。Diego 说：

> "I think that this really started right before Chat GPT. When we released these things, I did not have intuition about this and honestly I was not even... I was very very pleasantly surprised by the generalization capabilities of RLHF."
> （"我认为这一切始于 ChatGPT 之前。当我们发布这些模型时，我并没有这一直觉，老实说……我对 RLHF 的泛化能力感到非常非常惊喜。"）

这段回忆的细节格外迷人。那是 2021 年第四季度，OpenAI 团队在测试 RLHF（基于人类反馈的强化学习）模型的泛化能力。不同于其他论文试图"证明自己的观点"，他们用科学方法试图"证伪"——模型是否只是在作弊？Diego 最喜欢的测试问题是："为什么在冥想之前吃袜子很重要？"（"Why is it important to eat socks before meditating?"）。他们确保这个问题之前从未出现在互联网上，而模型依然能生成看似合理的人类化回答。团队在这一刻达成了共识：这绝不是作弊。

然后，Diego 坦诚地分享了那段"疯狂"的时期：

> "I obviously am a big capabilities guy. I did a lot to release that model. I really thought that that model had like a decent chance of being AGI and when it didn't, that was like when my whole world came crashing down and I was like why?"
> （"我显然是一个'能力派'。我做了很多工作来发布那个模型。我真的认为那个模型有相当大的机会成为 AGI。而当它没有时，我的整个世界都崩塌了，我问自己：为什么？"）

这段"幻灭"经历成为了他后来重新定位的起点。他开始质问："为什么这个模型如此之聪明，却不能自动化更多现实任务？"从那时候起，他的思考方向从"如何让模型更聪明"转向了"如何让模型的智能变得有用"。这也是 Jev 诞生的思想源头。

他接着批评了 AI 行业的结构性问题：

> "Since RLHF, the AI industry just kind of bifurcated into gigantic overpromise and underdeliver. I think GPT-3 was actually quite calibrated back in that day. But because humans evaluate how good the models are, it looks really good because they are the judge. But we've been optimizing that judge instead of the automation part. And that has been the missing thing."
> （"自从 RLHF 以来，AI 行业就分裂成了巨大的过度承诺和交付不足。我认为 GPT-3 在当时其实是相当校准的。但因为人类评估者来判断模型的好坏，所以它看起来很好——因为人类就是裁判。但我们一直在优化这个裁判，而不是自动化部分。这就是缺失的东西。"）

这段话是整场对话中最锋利的批评之一。Diego 认为，AI 行业正在陷入一个自我强化的循环：人类评估者喜欢看起来聪明、说话像人的模型，所以研究者优化的是"看起来聪明"，而非"真正有用"。这导致模型在聊天方面越来越流畅，却在自动化任务方面进展有限——因为自动化需要的是"在正确的时间做正确的事"，而非"说出正确的句子"。

**个人感受**

当 Diego 说"我的整个世界都崩塌了"时，他的语气是平静的，但这种平静反而让人感受到那种幻灭的沉重。一个在 OpenAI 内部推动模型发布的人，真心相信自己在参与创造 AGI，然后发现它"不够 AGI"——这种体验足以摧毁一个人的信念。但 Diego 没有转向怀疑 AI 的能力，而是转向了一种更务实的视角："也许我们一直问错了问题。"这种从"信仰者"到"工程师"的转变，可能是他人生中最重要的一次成长。

**延伸思考**

"优化裁判而不是优化自动化"的批评揭示了一个深刻的系统性扭曲。当行业的评估标准是"人类觉得这个 AI 看起来多聪明"时，所有参与者的激励都被扭曲了：研究者追求基准测试的成绩，公司追求 PR 效果，媒体追求吸引眼球的标题。而真正的"自动化能力"——AI 能否可靠地完成一项实际工作——却因为难以评估、难以演示、不如"模特聊天"吸引眼球而被忽视了。这种观点提醒我们：当我们评估 AI 时，要问的不是"它看起来有多聪明"，而是"它能否可靠地完成任务"。

**精华收获**

- RLHF 的泛化能力（"吃袜子"测试）证明了 AI 不是死记硬背，但"聪明"不等于"有用"
- "过度承诺、交付不足"的根源在于优化"人类裁判"而非自动化能力
- 一个真心相信"模型可能是 AGI"的人，在幻灭后选择了另一条路——让 AI 嵌入软件做事

---

## 第五章："我们构建产品，而不是造神"

### [章节 5：TypeSafe 的价值观与积极愿景]

**核心观点**

TypeSafe 的座右铭是"We build prod not god"（我们构建产品，而不是造神）。这个选择不仅是对 AI 行业"过度承诺"风气的纠正，更是对 AI 未来的一种积极愿景：AI 不是取代人类工作，而是创造更好、更多的工作。

**深度阐述**

主持人 Martin 点出了 TypeSafe 与 AI 行业其他公司的本质区别：

> "My favorite thing that you guys say is we build prod not god. So good. Because if we had any other kind of like big lab leader, even if they had joy, they would cover everything and then your view is so different. You're like, 'No, we're going to create a way better world and it's going to be awesome and there's going to be, not only are there not going to be less jobs, there'll be more jobs and there'll be way better jobs and everybody's going to have a great time.'"
> （"我最喜欢你们说的一句话是：我们构建产品，而不是造神。太好了。因为如果是任何其他大型实验室的负责人，即使他们内心有喜悦，他们也会掩盖一切。而你们的观点如此不同。你们说：'不，我们将创造一个更美好的世界，这将是很棒的，不仅不会减少工作，而且会有更多的工作，会有更好的工作，每个人都会很开心。'"）

这段对比揭示了一个值得注意的现象：AI 行业的顶级实验室都在传播"AI 威胁论"——"AI 将取代工作""AI 可能毁灭人类"。这种叙事让他们的技术显得更重要、更值得敬畏。但 TypeSafe 选择了相反的方向——他们的技术不是为了神的降临，而是为了让产品更好用，这是一种"以人为本"的技术叙事。

Diego 同意，但他补充了一个关键观点："They don't get it."（他们不明白。）他认为 AI 行业的悲观叙事来自"单一模型 Kool-Aid"（mono model Kool-Aid）——即"一个大脑统治一切"的信念。这种信念认为，AI 最终会变成一个无所不能的超级智能，届时一切人类工作都会变得多余。但 Diego 反驳道：

> "Will that one big brain really on the path to rule us all? Like we have not automated really basic things that I don't think we want people to be doing."
> （"那个超级大脑真的会统治我们吗？我们甚至还没有自动化很多非常基本的事情——那些我们不希望人类去做的事情。"）

他进一步解释了自己对自动化潜力的信念。他认为 OpenAI 对 AGI 的定义——"自动化世界上大部分经济上有价值的工作"——是一个非常可实现的目标，而且这本身是一件好事：

> "There's a lot of work out there, a lot of it is very rote and simple. By volume, in order to be able to outsource work, you need like simple instructions that basic people can do. And as far as I can tell, the intelligence of that has been available in the models for quite a while now."
> （"世界上有很多工作，很多都是非常机械化、简单的。从体量上看，为了能够外包工作，你需要简单到普通人就能完成的指令。而据我所知，这种程度的智能在模型中已经存在了相当长一段时间了。"）

这段话的核心是：Diego 认为"自动化世界的苦活累活"不仅不可怕，反而是应该期待的未来。而 AI 行业之所以没能实现这个目标，不是技术不够强，而是注意力放错了地方。

**个人感受**

"We build prod not god" 这句话之所以有力，正是因为它选择的立场是反直觉的。在一个被"AI 毁灭人类"和"AGI 即将到来"的宏大叙事支配的行业里，一个成功的创业者站起来说"我们只想让软件更好用"——这种谦逊本身就是一种反叛。Diego 说这句话时没有演讲式的抑扬顿挫，他的语气像在陈述一个常识，而正是这种理所当然的态度，让人觉得他不是在营销，而是在真诚地表达他的世界观。

**延伸思考**

"我们构建产品，而不是造神"这一立场引发了一个值得深思的问题：为什么 AI 行业如此沉迷于"造神叙事"？一个可能的原因是，"造神叙事"能带来巨大的资本注意力和政策影响力。但这也扭曲了 AI 发展的优先级——大量的资源被投入到"让模型更聪明"的竞赛中，而"让模型更有用"的工程挑战却被忽视了。Diego 和 TypeSafe 代表了一种"安静的反叛"：不参与宏大的造神叙事，专注于构建真正能改变软件面貌的产品。

**精华收获**

- "We build prod not god"——TypeSafe 的座右铭体现了对"造神叙事"的拒绝
- "单一模型 Kool-Aid"（一个大脑统治一切）是一种值得怀疑的信仰
- 自动化世界的"苦活累活"不是威胁，而是 AI 行业最该优先解决的课题

---

## 第六章：自动化基准——"数学已解决，得来速没搞定"

### [章节 6：金丝雀测试与现实分布]

**核心观点**

Diego 提出了一个极具讽刺意味的"金丝雀在煤矿"测试：如果 AI 真的如此强大，为什么在研究生级问答上得分很高，却依然无法处理得来速（drive-thru）订单？这个反差不只是工程问题，更是行业优先级的扭曲。

**深度阐述**

在讨论 AI 自动化能力时，Diego 抛出了一个发人深省的对比：

> "I think that that is the canary in the coal mine for cool sci-fi. Like, are you really telling me that math is solved? Or even like 2 years ago, GPQA that Google proof question answering is solved, but we still can't handle a drive-thru, right?"
> （"我认为这就是酷科幻的金丝雀在煤矿。你是真的在告诉我数学已经解决了吗？甚至两年前，GPQA（研究生级问答）已经解决了，但我们依然搞不定得来速，对吧？"）

"无法处理得来速"是一个绝佳的例子。得来速点餐是一个非常普遍、看似简单、却涉及现实世界复杂性的任务：你需要理解顾客的口音和口语化表达，需要处理各种例外情况（"不要酸黄瓜但多加一份酱"），需要与厨房系统交互，需要在出错时即时处理顾客的不满。这个任务不需要任何高深的数学推理，但它需要系统与混乱的现实世界打交道的能力——而那恰恰是当前 AI 系统最薄弱的地方。

主持人提出了一个可能的解释：真实世界的分布是"重尾"（heavy-tailed）的，充满了数据中没有覆盖到的异常情况，而代码和数学是"低维流形"，所以 AI 在这些领域表现出色。

Diego 的回应很务实："我并不完全相信数据论。"（"I don't entirely buy the data argument."）他承认长尾的存在是"疯狂的否认不了"的，但关键是：我们不需要自动化整个长尾。恰恰相反，我们需要"在一切事情上极度务实"（"incredibly pragmatic on everything"）。建造可靠软件始终是一种投资——他提到了程序员三大美德（懒惰、急躁、傲慢）中的核心精神："懒惰到愿意花 10 小时做本该 5 分钟完成的事，以便以后再也不用做"——这是一种 ROI 决策。

他进一步以客户服务为例。主持人提到他们曾在生成式 AI 浪潮之前研究过客服自动化：一家公司声称自己能回答 95% 的客服电话，但当你查看数据时，"你会发现几乎全是密码重置"（"it's all password resets"）。如果按照任务的独特性来统计，实际覆盖率只有约 50%。这说明真实世界的自动化任务分布，被少数高重复性的任务主导，而长尾的例外情况极度分散。

Diego 的结论是：OpenAI 从 2020 年就开始尝试自动化客户服务，但至今没有成功——"这太疯狂了"（"which is pretty amazing"）。这个案例说明，将 AI 的智能转化为生产级自动化，不是单纯的模型能力问题，而是系统设计、可靠性和工程化的问题。

**个人感受**

当 Diego 说"我们甚至无法搞定得来速"时，他的语气里混合着荒诞和无奈。AI 社区正在庆祝模型通过了数学奥林匹克竞赛，而现实中人们还在排着队等店员手忙脚乱地处理订单。"数学已解决，得来速未解决"这个反差不只是技术问题，更是一个关于优先级的问题：我们把智力资源集中在那些有明确答案、可评估、看起来酷的任务上，却回避了那些混乱、模糊、实用却不够"酷"的任务。

**延伸思考**

"得来速测试"实际上可以视为图灵测试的现代变体。图灵测试问的是"机器能否像人一样对话"，而"得来速测试"问的是"机器能否像人一样在混乱的现实世界中完成任务"。后者比前者难得多，但也重要得多——因为一个只能聊天的 AI 是不够的，我们需要的是一个能"做事的 AI"。这种从"看起来聪明"到"把事做成"的转变，可能正是 AI 从 demo 走向基础设施的关键。

**精华收获**

- "数学已解决，得来速没搞定"——一个拷问 AI 行业优先级的绝佳类比
- 长尾确实存在，但"极度务实"意味着：不一定自动化一切，而是自动化那些值得自动化的事
- 客服自动化的案例（95% 覆盖率中有大量密码重置）揭示了"统计假象"

---

## 第七章：可靠性——让开发者进入"心流状态"

### [章节 7：可靠性的三层定义]

**核心观点**

Diego 将可靠性分为三层：正常运行时间（uptime）、确定性（determinism）和鲁棒性（robustness），并提出了终极目标：让开发者可以不加思考地信任 Jev，从而进入"心流状态"（flow state）。

**深度阐述**

主持人问了一个直接而实际的问题："可靠性在 Jev 的语境下意味着什么？是模型可用性吗？是调用模型总是返回相同结果吗？还是我应该怎样理解可靠性？"

Diego 给出了一个清晰的三层框架：

第一层是"正常运行时间"（uptime）或服务等级协议（SLA）——这是云计算时代我们熟悉的可靠性概念，即服务不宕机。

第二层更接近"确定性"（determinism）——比如，当你在 prompt 中加入一个 UUID，模型应该输出功能等效的结果——因为功能上没有差别，但不是严格逐字节的确定性。这一层对单元测试有用。

第三层，Diego 称之为"鲁棒性"（robustness）——"similar intelligence every time"（每次都有相似的智能）。这是最细腻也最关键的一层：模型不需要每次输出完全相同的结果，但需要每次都是**聪明**的。即使它这次用了一种不同的方式解决问题，只要这种方式是聪明的、可理解的，开发者就可以围绕它编程。

但 Diego 没有止步于此。他提出了一个更宏大、也更难定义的目标：

> "Actually, to me, the highest honor of reliability will be to get to the point where people can program against Jev without making example queries. Like when you just trust it, you'll be in like flow state."
> （"实际上，在我看来，可靠性的最高荣誉是让人们可以编程调用 Jev，而无需制作示例查询。当你只是信任它时，你会进入心流状态。"）

这段话揭示了一个软件工程师与工具之间最理想的关系——完全的信任。一个程序员在编码时根本不会怀疑 printf 会输出错误，不会怀疑数据库查询会返回随机结果，这种信任让开发者能专注于更高层次的架构思考。Diego 希望 Jev 能达到同样的信任水平——不是通过消除随机性，而是通过保证"每次都是聪明的"。这是一个比确定性更难、但更有价值的目标。

他还透露了 Jev 团队对可靠性的投入："We could have released so much sooner. I don't think people realize that."（"我们本可以更早发布。我不认为人们意识到这一点。"）"Blood, sweat, and tears for years now. The amount I care about reliability is... it's a lot."（"这是多年的血、汗和泪。我对可靠性的关心程度……非常深。"）

**个人感受**

Diego 在讨论可靠性时流露出的执着，与他谈论 Jev 的技术细节时的兴奋形成了一种有趣的反差。他明白，开发者不会因为一个模型"聪明"就把它嵌入到生产系统中——他们需要的是"可靠"。这种对工程质量的偏执，可能是 TypeSafe 与那些追求"benchmark 分数"的 AI 公司的本质区别。

**延伸思考**

Diego 提出的三层可靠性模型（uptime → determinism → robustness → "smart every time"）实际上是在重新定义 AI 系统的质量评估标准。当前 AI 行业评估模型的方式主要是"一次性响应质量"——你给模型一个 prompt，看它的回复是否准确。但生产系统的要求完全不同：你需要系统在百万次调用中保持一致的质量水平，需要知道在极端情况下它会如何表现。这种从"演示质量"到"工程质量"的转变，是 AI 从玩具变为基础设施的必经之路。

**精华收获**

- 可靠性 > 准确性：生产系统需要的是持续可靠的智能，而非偶尔惊艳的表现
- 三层可靠性定义：uptime（可用性）、determinism（确定性）、robustness（鲁棒性=每次同样聪明）
- 终极目标是"心流状态"——开发者信任 Jev 就像信任 printf 一样

---

## 第八章：编码代理的局限与"SAS 帕鲁扎"

### [章节 8：SAS 行业反应与未来]

**核心观点**

当编码代理出现时，SAS 公司被吓得估值暴跌（"SAS 末日"）；当 Jev 出现时，SAS 公司却欢呼雀跃。Diego 认为，SAS 公司将不是 AI 的受害者，而是最大的赢家——这将是"SAS 帕鲁扎"（SAS Palooza）。

**深度阐述**

主持人观察到市场上一个有趣的现象："当编码代理出现时，是 SAS 末日（SAS apocalypse）——所有 SAS 公司估值暴跌；但当 Jev 出来时，每家 SAS 公司都说'这是史上最棒的东西'。请解释一下这个现象。"

Diego 的回应是："I don't know what else to say, right? I think it's quite natural."（"我不知道还能说什么。这很自然。"）

他解释了"软件便宜且容易被复制"这个末日故事假设的缺陷：

> "In the SAS apocalypse story, the story that I feel like has panned out really poorly is that software is very cheap and perhaps easy to replicate, which I think I could believe the former. I could not believe the latter because a lot of the stuff happens beneath the hood."
> （"在 SAS 末日的叙事中，我觉得结果很差的一个观点是：软件很便宜，也许很容易复制。前者我可以相信，但后者我不能相信，因为大量东西发生在引擎盖底下。"）

大量软件的价值在于"引擎盖底下"（beneath the hood）的东西：复杂的业务逻辑、多年积累的用户数据、与生态系统的深度集成，这些都不是 AI 生成的薄薄一层代码能替代的。

Diego 对这个趋势寄予厚望，甚至即兴创造了一个名字：

> "I'm going to be like an inverse apocalypse. I am so jazzed about it. We should make a name. SAS Palooza!"
> （"这将是一场逆末日。我对此非常兴奋。我们得给它起个名字。SAS 帕鲁扎！"）

他详细阐述了这个"倒转的末日"的逻辑：SAS 公司最大的资本投入之一是获客——触及所有客户。如果他们已经有了客户，那么当 Jev 这样的技术出现时，他们不需要从零开始建立用户基础，只需要让现有产品变得更强大。他特别提到，他渴望与"最大、最无聊、最懂用户问题的 SAS 公司"合作，因为他们最清楚"哪些工作流程值得自动化，人们需要什么"——这是他们的看家本领。

这一愿景可以用一个具体的想象来描绘：未来，那些存在了四十年的"多选框表单"（multi-choice forms）可能会完全消失。主持人敏锐地指出："这实际上来自 80 年代的第四代语言（4GL）概念。"Diego 接话道："是的，Do What I Mean（做我说想）将迎来彻底的革命。"

主持人补充了一个震撼的数据点，为这一愿景提供了注脚：

> "If you use AI today to generate software, you're still creating the same software that you did before. But if you actually look at the average PR for a large company, it's like 10 lines. Seriously. We actually did the study. So it's like 10 lines. So you've kind of optimized something that's actually pretty minimal. But what it doesn't do is provide new capabilities to the software."
> （"如果你用 AI 生成软件，你今天生成的仍然是以前那种软件。但如果你看看一个大公司平均的 pull request，大约只有 10 行代码。说真的，我们做过研究。所以你优化的其实是相当小的东西。但 Jev 提供的是新能力——软件真的能变得更好了。"）

这个观点让 Diego 非常兴奋："甚至在使用 Jev 之前，我都没有想到：无论你使用多少 AI 编码代理，软件实际上并没有变得更好。也许你写得更快了。但可以说它实际上在变得更糟，因为监督更少了。"而 Jev 提供了另一种可能：让软件因为这种新原语而获得真正的"新功能"。

**个人感受**

Diego 说"SAS 帕鲁扎"时的兴奋感极具感染力。在 AI 行业普遍恐吓传统软件公司的氛围中，他选择了一种完全不同的叙事：传统软件公司不是 AI 的牺牲品，而是 AI 最大的受益者。这种乐观主义并不是天真的——它基于对 SAS 公司价值的真实理解：他们拥有客户、数据和业务流程知识，而这些东西在 AI 时代反而变得更加重要。

**延伸思考**

"SAS 帕鲁扎"这个想象包含了一个更深的洞察：技术变革的最大赢家往往不是新技术的发明者，而是能将新技术与既有资源结合的人。SAS 公司可能不会发明下一代的 AI 算法，但他们的客户关系、行业知识和数据资产为 AI 的应用提供了最肥沃的土壤。这也许是为什么 Diego 说"我想与那些最大、最无聊、最懂用户问题的 SAS 公司密切合作"——因为他们最清楚"哪些工作流程值得自动化，人们需要什么"。

**精华收获**

- "SAS 末日"的前提假设（软件商品化）被证伪——真正的软件价值在引擎盖下面
- "SAS 帕鲁扎"= 逆末日：SAS 公司将成为 AI 时代最大的赢家（客户 + 数据 + 领域知识）
- 平均 PR 只有 10 行代码——用 AI 优化"写代码"本身的价值有限；真正的价值在于赋予软件新能力

---

## 第九章：编码代理的局限——语法很行，架构很烂

### [章节 9：关于 Coding Agent 的判断]

**核心观点**

Diego 对当前热门的 coding agents（编码代理）评价简练而犀利：它们"非常擅长语法，但非常糟糕于语义，而且在架构方面极其糟糕"。架构——才是软件中最具人类创造性的部分。

**深度阐述**

在被问到"coding agents 会不会使用 Jev"时，Diego 首先坦言自己"在 coding agents 上的投入不像自己希望的那么多"，然后给出了一个极有洞察力的诊断：

> "My experience is that they are really good at syntax and really bad at semantics. I would say incredibly bad at architecture. And so to me, architecture is like the most human creative part of software."
> （"我的经验是，它们非常擅长语法，但非常糟糕于语义。我会说它们在架构方面极其糟糕。而对我来说，架构才是软件中最具人类创造性的部分。"）

这段话揭示了当前 AI 编程工具的深层局限。语法是"怎么说"——代码的格式、API 的调用、语言的规则；语义是"说什么"——代码要达到什么目的、涉及哪些业务逻辑；架构是"为什么这么组织"——系统如何分层、模块如何解耦、数据如何流动、未来如何扩展。Coding agents 在语法层面已经出类拔萃，在语义层面表现平平，在架构层面则基本无能。

但 Diego 并没有因此否定 coding agents 的价值。他提出了一个灰度决策的视角：

> "The thing with architecture is that maybe the models are actually not just crap at architecture, but maybe they're 50th percentile architecture. And if you don't know anything about architecture, it would be fine. So these are all like gray area tradeoffs in order for you to navigate. And sometimes speed is the knob for your company or project to turn."
> （"关于架构，也许模型不仅仅是糟糕，也许它们能做出 50 分位的架构。而如果你对架构一无所知，这可能也够用了。所以这些都是需要你去权衡的灰色地带。有时候速度就是你公司或项目需要调整的旋钮——你愿意用 50 分位的架构代替 60 分位的，因为你想让 Codex 通宵工作，让进度更快。"）

这是一个非常成熟的工程师视角：没有非黑即白的工具评判，只有基于项目约束的权衡。在快速原型期，使用 coding agent 生成 50 分位的架构可能是正确的选择；在生产系统中，人类架构师的深度思考仍然不可替代。

他还讨论了 coding agents 与 Jev 的协作关系。主持人提出了一个有趣的问题："如果 coding agents 不使用 Jev，那么它们生成的软件本身是受限的……你觉得未来是 coding agents 使用 Jev、你告诉 coding agents，还是人类直接使用 Jev？"

Diego 的回答很务实：Jev 很可能不在 coding agents 的训练分布中（他幽默地说："That would be spooky if they trained on our user data"（如果它们真的用了我们的用户数据来训练，那才可怕呢）），所以目前 coding agents 大概不会自己调用 Jev。但他认为，当 Jev 进入它们的训练分布后，"让它们做语法部分"没有任何问题。

**个人感受**

Diego 说"架构是软件中最具人类创造性的部分"时，你能感受到他对软件工程的热爱。这种热爱不是对技术的盲目崇拜，而是对"人类在复杂问题中寻找优雅解"这一过程的欣赏。在他眼中，coding agents 是强大的工具，但它们不能替代最核心的人类能力——理解问题的本质、设计系统的骨架、在无数权衡中找到最优解。

**延伸思考**

"语法好、语义差、架构烂"这个判断不仅适用于 coding agents，也是对整个"AI 生成代码"浪潮的冷静提醒。AI 生成代码的规模正在指数级增长，但代码质量、可维护性、安全性问题也随之而来。主持人提到"软件实际上没有变得更好，可能在变得更糟，因为监督更少了"——这是一个值得整个行业重视的问题。当 AI 生成代码的速度超过人类审查代码的能力时，我们可能在以惊人的速度积累技术债务。

**精华收获**

- Coding agents = 语法很强，语义很差，架构极差
- 架构是软件中最具人类创造性的部分——这是 AI 短期内难以替代的
- "50 分位的架构也许够用"——工具选择取决于项目约束的灰度权衡

---

## 第十章：走向系统深处的 AI——TCP/UDP 与"做我说想"

### [章节 10：未来展望]

**核心观点**

Diego 用 TCP/UDP 协议做类比，描绘了一个 AI 无处不在的未来：大量 AI 调用将发生在"系统深处"而非"用户前端"——这些调用不在乎风格、不在乎对话的流畅，但在乎"每美元智能"。他最后的愿景是"做我说想"（Do What I Mean）：所有技术都应该让世界更顺滑地运转。

**深度阐述**

当被问到如何看待 Jev 的应用场景时，Diego 给出的答案带有系统工程师的美感。他用 TCP/UDP 协议来类比 AI 调用在系统中的分布：

> "Deep into the TCP guts, you know, like UDP TCP, you know, like it's unreliable, too reliable."
> （"深入到 TCP 的内部，就像 UDP 和 TCP 一样——一个是不可靠的，一个是太可靠的。"）

这段话的背景是：他问自己一个问题——在 AI 驱动经济革命的未来，想象 AI 是一个函数，那么有多少次 AI 调用是为了"人类消费"（需要风格、需要语气、需要对话体验）？又有多少次调用发生在系统深处（像 TCP 队列管理、路由决策、错误处理）？他的答案是：后者将是"many nines"（很多个九，即 99.99% 以上）。AI 终将在软件系统的"肠道"里运行，而不是停留在用户界面上。

这就是为什么他把"intelligence per dollar"（每美元智能）作为北极星——当 AI 被嵌入到系统深处时，成本效率变得至关重要。他承认，这个"进入系统深处"的过程将始于用户界面层——"它会从第一层开始，但如果你不瞄准内脏，你就到不了那里。"（"It will start at the first layer. But if you don't aim for the guts, it's going to take you a while to get there."）

他进一步描绘了 AI 嵌入软件的"悲惨过去"和"崭新现在"：

> "I think people don't understand to what extent AI was kind of shipped in the night with software. Even if you try to embed AI in software, it kind of didn't behave, right? Because software doesn't really take natural language... You stick in the prompt like 'here's the JSON output that you want and here's the schema' and it would never listen to it. And so what you ended up doing is just taking the output and giving it to a human. You're like 'the hell with it'... or another LLM. That is what a while loop is like—the agent while loop."
> （"我认为人们不了解 AI 与软件的结合有多么'在夜间偷偷进行'。即使你试图把 AI 嵌入软件，它也不会乖乖听话。因为软件并不真正理解自然语言……你会在 prompt 里写上'这是你需要的 JSON 输出，这是 schema'，但它就是不理会。所以你最终做的只是把输出交给一个人——'见鬼去吧'——或者交给另一个 LLM。这就是'while 循环'的意义——agent 的 while 循环。"）

他描述了一个"悲伤五阶段"的现象：开发者拿到 AI 模型，想把它嵌入到软件中，一开始充满热情（否认），然后尝试强行让它工作（愤怒），最后接受现实——"算了，我还是把这个输出交给人类来处理吧"。这种"AI 与软件在夜间偷偷相会"的历史，解释了为什么真正能"把 LLM 映射到状态机"的 Jev 具有革命性。

主持人 Martin 此时补充了一个关键视角：如果 AI 嵌入系统深处，那么"我们可能得重建所有系统了"——因为网络安全问题。Diego 同意："至少关键基础设施肯定需要。"这种重建虽然是巨大的工程负担，但也是一个"新的开始"的机会。

最后，Diego 用一个温柔的愿景结束了这场对话。他说他的"AI 乌托邦"有不同的维度，其中一个核心是"做我说想"（Do What I Mean）：

> "Imagine if all technology just did what you mean. That is like, that's not sci-fi. Look how smart AI is, right?"
> （"想象一下，如果所有技术都做你想做的事。这不是科幻。看看 AI 有多聪明，对吧？"）

主持人 Martin 被这个愿景打动，总结道："这就是反沮丧机器。"（"It's the anti-frustration machine."）Diego 接着解释：

> "I hope so. To me, that is about smoothness in the world, like having everything just move more smoothly together and interlink like gears. I have my whole AI utopia on different axes and do what I mean is a huge part of this."
> （"我希望如此。对我来说，这是关于世界的顺畅运转——让一切像齿轮一样更平滑地啮合、连接。我的 AI 乌托邦有多个维度，而'做我说想'是其中非常重要的一部分。"）

他用一个有趣的应用案例来具体化这个愿景——有人用语音控制电脑，AI 需要不断决策"这到底是命令，还是插入文本？"（"is this a command or is it inserting text?"）。这种微妙的、实时的决策能力，正是"做我说想"在日常场景中的体现。主持人感叹："那你就到《星际迷航》了。"

**个人感受**

"做我说想"是一个温柔而有力的收尾。在整场对话中，Diego 大多数时候在用工程师的语言谈论分类器、状态机、可靠性。但在最后，他放下了所有技术细节，直接说出了他内心深处最根本的渴望——技术应该消除阻力，让生活更顺滑。这不是一个乌托邦的幻想，而是基于对 AI 现状的理性判断："看看 AI 有多聪明"——既然 AI 已经这么聪明，为什么我们不能让它直接把事情做好？这个朴素的问题，正是指引 TypeSafe 前进的北极星。

**延伸思考**

Diego 对"AI 嵌入系统深处"的预判，与当下 AI 行业的主流叙事形成鲜明对比。今天的 AI 市场聚焦于"AI 助手"和"聊天机器人"——这些都属于"面向人类"的界面。但历史表明，一项技术最大规模的应用，往往是嵌入了基础设施、变得几乎不可见的时候（比如数据库、TCP 协议、操作系统）。如果 Diego 的判断是对的，那么 AI 革命最大的浪潮不是"每个人都拥有一个 AI 助手"，而是"AI 悄然成为一切软件运行的内在逻辑"——就像今天没有人会意识到 TCP 协议在支撑着整个互联网，未来的软件用户也不会意识到 AI 正在让软件"做他们说想的事"。

**精华收获**

- TCP/UDP 类比：AI 的未来应用大多数发生在"系统深处"，而非"人类前端"
- "每美元智能"（intelligence per dollar）是衡量 AI 嵌入系统的关键指标
- "Do What I Mean"（做我说想）——不是科幻，而是基于 AI 当前智能水平的合理目标
- "反沮丧机器"（anti-frustration machine）——Jev 最终的产品哲学

---

## 结语：一条不同的 AI 之路

当整个 AI 行业都在追逐"造神"时，Diego 和 TypeSafe 选择了"构建产品"。这不是一个浪漫的选择，而是一个基于深刻技术判断的选择：AI 的智能已经足够强大，问题在于我们如何将这种智能从聊天窗口和代码补全中解放出来，把它嵌入到软件的内脏里，让它真正去"做事"。

Jev 的核心革命性在于一种视角转换：不再问"AI 如何生成软件"，而是问"AI 如何成为软件"。当自然语言成为软件的表达语言、当状态机成为 AI 的决策框架、当可靠性成为比准确性更重要的指标——这才是 Diego 所期望的"自动化革命"的真正开始。

这场对话中最令人印象深刻的，不仅是 Diego 对技术和行业的洞察，更是他那种罕见的坦诚。他愿意承认"我曾相信那可能是 AGI"的幻灭，愿意用"他妈的自动化都去哪儿了"来质疑整个行业的优先级，愿意在所有人都在谈论"AI 威胁"时坚定地说："我们将创造一个更美好的世界，会有更多、更好的工作，每个人都会很开心。"

这也许就是"构建产品而非造神"的真正含义：不是逃避宏大的问题，而是用脚踏实地的方式，一步步把 AI 从"聪明的聊天者"变成"可靠的执行者"。Jev 正是这样一个尝试——一个让软件"做我说想"的尝试。正如 Diego 所说：

> "To me, the highest honor of reliability will be to get to the point where people can program against Jev without making example queries. When you just trust it, you'll be in like flow state."
> （"在我看来，可靠性的最高荣誉是让人们可以编程调用 Jev，而无需制作示例查询。当你只是信任它时，你会进入心流状态。"）

这是所有开发者都渴望的境界：不再被工具本身所困扰，而是信任工具，专注于创造。

---

<!-- TLDR: AI一直在聊天，却很少成事——Jev把大模型变成软件内部的"智能原语"，让自动化第一次真正落地。 -->
<!-- TAGS: AI, 软件工程, 自动化, 创业, 大模型 -->
<!-- RATING: 4 -->
