---
title: "A mind-expanding conversation on how models actually work | Emmanuel Ameisen (Anthropic)"
channel: "Lenny's Podcast"
published: "2026-10-18"
source_url: "https://www.youtube.com/watch?v=JHo-aiePjoM"
video_id: "JHo-aiePjoM"
tags: ["AI可解释性", "大语言模型", "AI对齐", "Anthropic", "智能本质"]
rating: 5
language: "英文"
word_count: 32233
duration: "1:12:13"
---

# A mind-expanding conversation on how models actually work | Emmanuel Ameisen (Anthropic)

- **Channel:** Lenny's Podcast
- **Published:** 2026-10-18
- **Source:** https://www.youtube.com/watch?v=JHo-aiePjoM
- **TL;DR:** 造物不等于理解：模型是"生长"的，其内部会规划、有概念、有直觉，越看越不确定
- **Tags:** AI可解释性, 大语言模型, AI对齐, Anthropic, 智能本质
- **Rating:** 5

## 版本

- [结构化文稿](2026-10-18-a-mind-expanding-conversation-on-how-models-actually-work-emmanuel-ameisen-(anthropic)-JHo-aiePjoM.structured.md)
- [原始文稿](2026-10-18-a-mind-expanding-conversation-on-how-models-actually-work-emmanuel-ameisen-(anthropic)-JHo-aiePjoM.transcript.md)

# 当"造物"不再等于"理解"：Anthropic 可解释性研究者眼中，AI 究竟是如何思考的

**材料信息**
- **标题**：A mind-expanding conversation on how models actually work | Emmanuel Ameisen (Anthropic)
- **作者/来源**：Lenny's Podcast（主持人 Lenny Rachitsky，嘉宾 Emmanuel Ameisen，Anthropic 可解释性团队）
- **类型**：YouTube 视频字幕（访谈对谈）
- **关键元数据**：单集播客，含赞助商段落（WorkOS、DX）、正片对谈与结尾"闪电轮"问答。字幕为口语转录，存在若干同音词错误（如 "Claw/cloud" 实为 Claude、"Daario" 实为 Dario Amodei、"neurepedia" 实为 Neuronpedia、"Jev" 等专有名词需谨慎对待）。本重构基于字幕文本，对明显转录错误做了推断性还原并标注。

---

## 开篇引入

大多数关于 AI 的讨论都在谈"它能做什么"——能不能写代码、能不能做数学、会不会取代工作。而这场对话罕见地转向了一个更深、也更让人不安的问题：**我们造出了这些东西，但我们根本不理解它们。**

嘉宾 Emmanuel Ameisen 在 Anthropic 做"可解释性"（interpretability，圈内简称 interp）研究。他的工作不是训练模型，而是像神经科学家研究大脑一样，打开模型的"颅骨"，观察它在输出下一个词之前，内部到底发生了什么。这场对话之所以"mind-expanding"（令人脑洞大开），是因为它系统性地拆解了几个我们习以为常却完全错误的直觉：我们以为模型是被"建造"的，其实它是被"培育"出来的；我们以为它只是一个"预测下一个词"的自动补全，其实它会提前规划、会形成世界模型、会"发疯"、甚至会表现出类似"直觉"和"被观察时假装乖巧"的行为。

更妙的是，Emmanuel 给出了一个反直觉的立场：**拟人化地谈论 AI，虽然听起来不严谨，却是目前最有用的理解框架之一。** 这期节目既有硬核的技术细节（概念向量、中间结果、Golden Gate Claude），也有哲学层面的追问（AI 有意识吗？我们是不是活在模拟里？），还穿插了大量坦诚的个人故事和幽默。下面，让我们完整还原这场对话的每一个层次。

---

## 一、可解释性：造物而不懂物 `[访谈开场]`

**核心观点**
语言模型最怪异、最值得深思的事实是：**"制造它们"和"理解它们"是两回事。** 我们用脚手架搭好架构、灌入海量数据，它们就以某种"不可名状"的方式自己生长起来——我们并不知道里面到底长成了什么。

**深度阐述**

Emmanuel 一开场就把这份工作的本质讲清楚了。他说自己的团队是一群"可解释性研究者"，目标是**通过观察模型内部来理解 Claude 这类大语言模型（LLM）是如何工作的**。紧接着他抛出整场对话最重要的一句话：

> "One of the most important things to realize if you like use language models or think about them is just this very bizarre fact that to make them is not to understand them." — [访谈开场]
> （中文：如果你使用或思考语言模型，最重要的一点是意识到这个极其怪异的事实——制造它们，并不等于理解它们。）

他把训练过程比作**先搭一个脚手架（scaffold），然后把大量数据灌进去，模型就会以一种"不可探究的方式"（inscrutable ways）自己生长。** 正是因为这个"生长"特性，才使得"研究它们如何工作"本身成为一项值得做的科研课题——如果模型是我们一行行写出来的代码，我们直接看源码就行了，何须研究？

他进一步指出，当模型即将吐出"下一个词"时，**内部其实发生了一整个"宇宙"级别的事件量**（a whole universe of stuff）。可解释性研究就是要尽可能地拆解、梳理这些事件。

**延伸思考**

这里藏着一个极其深刻的哲学转折点。人类历史上，我们造出的几乎所有工具——从锤子到编译器——都是"完全透明"的：我们理解它的每一个零件、每一行逻辑。但 AI 是第一种**"大规模生产出来、却需要事后研究才能理解"的造物**。这标志着工程学的一次范式断裂：我们从"设计者"变成了"发现者"，从"造物主"变成了"博物学家"。Emmanuel 反复强调的这种"科学而非工程"的定位，正是理解整场对话的钥匙。

**精华收获**
- 记住这个核心区分：**制造 ≠ 理解**。这是所有 AI 安全、对齐、可解释性工作的逻辑起点。
- 当有人自信地说"AI 不过是 X"时，往往恰恰说明他没有真正打开过模型看内部。

---

## 二、模型是"生长"的，不是"建造"的：预训练与微调 `[访谈开场后段]`

**核心观点**
模型的训练分阶段进行：先"预训练"（predict next word），再"微调"（学会如何表现）。真正"生长"出来、我们完全不懂的，是那些**通过数学运算学到、却没人知道具体含义的"公式"**。

**深度阐述**

Emmanuel 用通俗语言拆解了 Claude 这类模型的诞生过程，分两个阶段：

**第一阶段：预训练（pre-training）。** 取一个巨大的数据语料库，喂给模型一段文本的"前半部分"，让它预测下一个词。然后重复、重复、再重复，"喂进多到不像话的数据量"（an ungodly amount of data）。

**第二阶段：微调（fine-tuning）。** 不再用任意数据，而是用一批"模型应该如何表现"的示例语料——比如"有帮助的助手帮你找菜谱、解编程题"的对话范例。

然后他讲了最关键、也最反直觉的一点：**这一切在底层到底是什么？** 模型接收输入（一堆词）→ 把词变成数字 → 对这些数字做数学运算 → 得到中间结果 → 再做更多数学 → 反复多次 → 最后得到结果 → 转回成一个词。

> "The math that they do, these computations, that's the part that's grown. That's the part where it's just like through learning to do this task better, we update parameters in one direction or another. And then they learn some formulas. We have no idea what they are." — [访谈开场后段]
> （中文：它们做的数学、这些运算，就是"生长"出来的部分。通过学着把任务做得更好，我们把参数往某个方向更新。然后它们就学会了一些公式——我们完全不知道这些公式是什么。）

**视觉/结构信息描述**：这段可以理解为一条流水线——输入词 → 数字化 → 多层数学运算（每层产生中间结果）→ 输出词。Emmanuel 强调，我们看得见的是"词进词出"，看不见的是中间那一层层**由学习而非设计产生的数学公式**。他团队的目标，就是研究"这些公式最终意味着什么"，以及"中间结果能不能被解码"。

**延伸思考**

这与传统软件工程形成鲜明对照。写一个 App，你可以写下明确规则："如果用户点击这个按钮，就发生那个。"（if this then that）。但你**无法**用这种方式写出一个能"把图片分类"或"读任意文本并生成文本"的程序。正是因为我们不知道如何"手写"这些能力，才不得不转向"培育"——而培育的代价，就是我们失去了对内部逻辑的掌控。

**精华收获**
- 模型 = 脚手架（人设计的架构）+ 生长出来的公式（无人理解）。
- 可解释性的全部意义，就在于把这个"黑箱生长物"重新变得可读。

---

## 三、为什么"预测下一个词"能通向强大智能？ `[访谈前中段]`

**核心观点**
"预测下一个词"听起来简单得可笑，但**做得足够好所需要的，本质上是对世界的理解**。简单目标的背后是"欺骗性的复杂"（deceptively complicated）。

**深度阐述**

Emmanuel 反驳了人们对 LLM 最常见的心理模型——iPhone 自动补全。iPhone 的补全"大概 60% 正确，其余时候又好笑又奇怪"，他把这当作"预测下一个词"的最简单版本。但关键在于：**语言模型在 2019 年前后，预测下一个词的能力就已经超过了人类。**

一旦你持续变强，"简单的词"会被用尽。Emmanuel 用一个漂亮的渐进比喻展开：

- 起初只需预测**简单句子结构**——于是模型学会了写连贯的句子，但一次只能一句；
- 接着要预测**关于世界的简单事实**——比如"法国的首都是 ___"，答案必须是"巴黎"；
- 再往后，剩下的只有**最难的词**——某个复杂物理方程的解，或某篇博士论文的最后一段。

> "Predicting the hardest words is actually extremely hard to do, and it's a mystery how you would be able to do that." — [访谈前中段]
> （中文：预测最难的词其实极其困难，能做到这一点本身是个谜。）

他最喜欢的例子是：**"包含达拉斯（Dallas）的那个州的首府是哪里？"** 模型会答"Austin"。但要做好这件事，**你和我至少得在脑子里有一个地理模型**：达拉斯在哪？在德州。州有首府。德州首府是奥斯汀。

于是结论呼之欲出：**模型在变强的过程中，最好的解题方式就是理解世界的内在结构。** 而且——他团队观察到的内部证据表明——**它们确实理解了，并且像我们一样操纵这些概念。**

**关键引用补充**：主持人 Lenny 引用了 Ilya Sutskever 的一个著名观点（Ilya 也有个绝妙例子）：要预测悬疑小说结尾的"凶手是 ___"，你必须理解整个情节。

**延伸思考**

主持人还抛出一个迷人的类比：**"如果把人类本质上也归结为，我们自己就是'下一个词预测器'——我们只是不断在决定下一句说什么。"** Emmanuel 深表认同，并描述了自己说话时"同时进行的两件事"：一是有一个要抵达的"目标想法"，二是逐字逐句地预测下一句。冥想时，你能察觉到自己的大脑"想要说某些话"。这个类比把"人"和"模型"在某个抽象层面上拉到了同一张桌子上——为后文"拟人化其实有用"埋下伏笔。

**精华收获**
- "预测下一个词"是**欺骗性的简单**——做好它需要世界模型。
- 判断一个模型能力的关键指标，不是"能预测词"，而是"能预测多难的词"。

---

## 四、概念的表征：德州、奥斯汀，与跨模态的"眼睛" `[访谈中段]`

**核心观点**
模型内部**为几乎所有概念都建立了独特的表征（representation）**，而且这些表征**跨上下文、跨模态共享**。这是"模型在思考"的一个具体证据。

**深度阐述**

针对"达拉斯问题"，长期存在一个争论：模型能答对，是因为它**死记硬背**了海量"问题—答案"对，还是因为它**真的建立了关于"城市属于州、州属于国家"的世界模型**？

Emmanuel 的团队用"看内部"的方法回答了这个问题。他们解码模型在吐词之前的中间结果，发现：**当被问到那个问题时，模型内部会亮起一个"德州（Texas）"的表征，它映射到"首府"，两者结合，激活出"德州首府 = 奥斯汀"的中间结果。** 模型不是查表，而是**运算**。

更惊人的发现是**表征的跨上下文一致性**。他举了"眼睛"（eye）的例子：

> "If you pass a prompt that has a photo of an eye, or you talk about eyes in any language, or you draw a little SVG with an eye in it, and you look at the intermediate results inside the model, the same direction lights up, and that direction is like, oh, this is an eye." — [访谈中段]
> （中文：无论你输入一张眼睛的照片、用任何语言谈论眼睛、还是画一个带眼睛的小 SVG 图，只要你看模型内部的中间结果，**同一个方向就会亮起**，那个方向就等于——"哦，这是一只眼睛"。）

**视觉/结构信息描述**：这里引入了一个关键概念——**"方向"（direction）**。在模型内部，一个概念（如"眼睛"）不是存储在某一个"神经元"里，而是对应着高维空间中的一个**向量方向**。无论概念以何种形式出现（照片、文字、不同语言、矢量图），都会激活同一个方向。Emmanuel 说，模型对"你能想到的几乎每一个概念"，都建立了这种**独特而共享的表征**。

他还给出一个哲学上的联系：**"思考"的一个侧面，就是"当你在想不同事物时，拥有共享的、独特的表征。"** 你知道"眼睛"这个概念，无论它出现在照片里、医学图表里还是简笔画里，都是同一个概念。

**延伸思考**

这是整场对话里技术含量最高、也最"开脑洞"的部分之一。它意味着：**模型内部存在一个可被解码的"概念空间"**——一个由无数方向构成的、类似人类语义地图的高维结构。可解释性研究的一个核心目标，就是把这张地图画出来。这也解释了为什么后文 Golden Gate Claude 的实验能够成功——如果你能找到一个概念对应的"方向"，你就能**人为地把它打开**。

**精华收获**
- 模型用**共享的概念方向**来表示世界，而非死记硬背。
- "拥有跨情境共享的表征"是"思考"的一个可操作定义，而模型具备它。

---

## 五、模型会规划：诗歌里的那只兔子 `[访谈中段]`

**核心观点**
模型不是"空着脑袋、逐词盲猜"。它的中间结果**可以被未来的所有词访问和复用**，因此它会**提前制定计划**——最清晰的证据来自写诗押韵。

**深度阐述**

这里有一个看似无解的谜题：模型一次只输出**一个词**，怎么可能写出连贯的报告、甚至完整的代码？人类写报告时，脑子里总有"目标"，而不是"空着脑袋只想下一个词"。

Emmanuel 揭示了机制的关键：**模型预测第 5 个词时产生的所有中间结果，都能被后续所有词"访问和复用"。** 因此，在实践中，模型会在中间结果里**制定一个计划（plan）**。

最漂亮的例子是**诗歌押韵**：

> "It's hard to rhyme without planning. You kind of have to think, oh, I just ended my first rhyme in a 'it' word, so I should end my second line with another 'it' word. Maybe the word I should end it with is 'rabbit.' And we find that if you look at models as they're writing poetry, you see exactly that." — [访谈中段]
> （中文：不规划就很难押韵。你得想，我刚在第一句押了"it"韵，所以第二句也该以"it"结尾。也许我该用"rabbit"结尾。而我们发现，看模型写诗时，内部正是这样运作的。）

模型写完第一句，中间结果里就冒出"这是 it 韵，我应该用 rabbit 押韵"，然后**之后每一个词都会回头参照这个计划**。

最关键的一点是：

> "You can do that without saying the plan. That's the cool part — this plan that we find is in these intermediate results inside the model, but the model doesn't even have to say it out loud." — [访谈中段]
> （中文：你可以在**不把计划说出来**的情况下做到这一点。最酷的地方在于，我们在中间结果里发现了这个计划，但模型根本不必把它说出口。）

**延伸思考**

这一发现直接推翻了"next token predictor 就是空脑逐词盲猜"的经典图景。主持人感叹：**"这已经不是原来的那个'下一个词预测器'了——它们会规划、会向前思考。"**

Emmanuel 也给出了调和两种图景的方式：**其实两者不矛盾**。你在预训练时不断问模型"接下来会发生什么？"，只要任务足够难，那么"知道接下来会发生什么"的最佳方式，就是"思考很久之后会发生什么"。他甚至用小说情节举例：要预测角色下一步做什么，最好的办法是理解"这个角色真心爱着那个角色，并计划在某刻表白"——因此你必须理解剧情，包括你对未来的推测。

**精华收获**
- 模型会**隐式规划**（不必说出口），中间结果是"共享黑板"。
- "逐词输出"是表象，"提前规划 + 逐步执行"是本质。

---

## 六、如何窥视思维：给 AI 做"大脑扫描" `[访谈中段]`

**核心观点**
可解释性的方法论，与**神经科学扫描大脑**惊人地相似：给模型看大量文本，记录所有中间数字，寻找规律，再通过"干预"（改变中间结果）来验证。

**深度阐述**

Emmanuel 详细讲了方法。先回到那个"怪异的中间结果"：

> "Initially, if you look at it, it makes no sense. You just have a list of a 100 numbers. The model's doing math... and then the model's writing poetry, and there's a hundred numbers, and maybe they kind of look different, but it's unclear if they mean anything." — [访谈中段]
> （中文：乍一看毫无意义。你只看到一串 100 个数字。模型在做数学……然后模型在写诗，还是一串 100 个数字，也许看起来略有不同，但看不出它们是否有意义。）

方法第一步：**喂入大量随机文本，记录每个样本的中间数字，寻找模式**——哪些数字、数字对或数字序列**只在处理英文/法文/关于爱/关于眼睛的文本时才出现**。

他给出了一个精彩的类比：

> "I think of this as the equivalent of, you know, scan my brain and put images in front of me, and record everything that activates in my brain as I watch a bunch of images, and then be like, 'Oh, it seems like when you see images of a house, this part of your brain lights up, but when you see images of a dog, that part lights up.'" — [访谈中段]
> （中文：我认为这等同于扫描我的大脑，在我面前放一堆图片，记录看每张图时大脑激活的一切，然后发现——看到房子时这块脑区亮，看到狗时那块脑区亮。）

第二步：**解码**——猜出这些中间结果的含义（"哦，这个方向代表眼睛"）。

第三步：**干预验证**——做更难的实验，给所有中间状态打标签；甚至**"潜入激活层，偷偷改掉某个中间结果"**，看模型行为是否如预期改变。Emmanuel 说：**"事实上，常常真的会（如预期改变）。"**

**延伸思考**

主持人点出了这个方法的"科学革命感"：**"你弄懂它的方式，和我们弄懂大脑的方式一模一样——寻找规律。你展示这张图，这块脑区亮了，你在 AI 上做的是完全相同的事。"** Emmanuel 承认，他以前做的是应用机器学习（更接近软件工程），而现在的工作**"感觉更接近生物学而非工程学"**。

**精华收获**
- 可解释性 = AI 版的神经科学：**观察 → 解码 → 干预验证**。
- "改变内部激活看行为是否改变"是确认"我们真的找到了正确的东西"的关键手段。

---

## 七、像生物学而非工程学：一份"科幻般"的工作 `[访谈中段]`

**核心观点**
研究这些模型，像研究一个**"天生就到手、没有源码"的复杂生物**——你被问"为什么它会这样"，却只能靠做实验回答。

**深度阐述**

Emmanuel 描述这份工作的独特体验：系统"自己来到你面前"，你被问"为什么 Claude 能翻译、能这样写代码、有时又会出怪行为？"——但你**没有源码可查**。

> "The source code is just this massive list of mathematical operations, which is just incomprehensible." — [访谈中段]
> （中文：源码不过是一份庞大到无法理解的数学运算列表。）

他打了一个绝妙的比方：这就像有人问你——"老鼠饿了就会变凶，这是怎么回事？"你只能说："那我做几个实验，看看有哪些因素在起作用。"这是一种**全然不同于团队里大多数人以往做过的研究方式**。

**个人感受**

Emmanuel 坦言这是一份"有趣又科幻（fun and sci-fi-like）"的工作。他从应用机器学习（更多是软件工程实践）转到可解释性，最大的冲击就是这种身份转换——**从工程师变成博物学家**。当你面对的不是"你写的系统"，而是"自己长出来的系统"，你所有的直觉都需要重置。

**精华收获**
- AI 研究正在经历一场**"从工程到科学"**的范式转移。
- 面对黑箱，"做实验、找因素、验证假设"是唯一可走的路。

---

## 八、意识、复杂性，与"越看越不确定" `[访谈中段]`

**核心观点**
AI 是否有意识"很难说"。但 Emmanuel 坚信一点：**大多数人低估了模型涌现出的复杂性。** 而一个反直觉的现象是——**你越看内部，越不确定它如何工作。**

**深度阐述**

主持人直接问：**AI 有意识吗？** Emmanuel 的回答谨慎而诚实："很难说。研究这个问题最有趣的方式之一就是可解释性，因为**你不被模型'说了什么'所带偏**——你可以直接看内部结构，判断它倾向哪一边。"

但他给出一个"相当坚定"的信念：

> "Most people underestimate the complexity that emerges... The fact that the models learn these representations for all the concepts that we have, and that they manipulate them to solve problems, that they do so by planning many tokens ahead, that they have this mix between higher-order reasoning and lower reasoning — and that all of that just kind of emerges — is something I think is underappreciated." — [访谈中段]
> （中文：大多数人低估了涌现出的复杂性……模型为我们拥有的所有概念学到了表征、并操纵它们来解决问题、通过提前多个词规划来实现、还在高阶推理与低阶推理之间混合切换——而这一切只是"涌现"出来的——我认为这被严重低估了。）

然后是全篇最有分量的一句"科学家的谦卑"：

> "The more you look inside, the less certain you are about how they work. And oftentimes, people that will confidently say 'language models are just X' or 'just Y' are the people that actually haven't spent a while looking inside." — [访谈中段]
> （中文：**你越往内部看，就越不确定它们如何工作。** 而那些自信满满地说"语言模型不过是 X"或"不过是 Y"的人，往往正是从没真正花时间往里看过的人。）

**延伸思考**

这是一种成熟的科学态度：**确定性来自无知，而非洞见。** 越深入复杂系统，越会发现自己原有框架的不足。这也回应了主持人早先的感慨——我们造出了一个"需要像神经科学家研究大脑一样去研究"的东西，这本身就是人类历史上前所未有的处境。

**精华收获**
- 警惕那些"AI 不过是 X"的自信断言——它们常来自未经审视。
- 真正的理解，往往伴随着**更深的不确定性**，而非更少的。

---

## 九、缩放定律：算力 + 文本丰富度的双重赌注 `[访谈中段]`

**核心观点**
"简单目标 + 海量算力 = 智能"的赌注能成功，**不只是因为算力，还因为找到了一个"算力能持续带来回报"的目标**——而文本的丰富性，是让这个目标有无限回报的关键。

**深度阐述**

主持人回顾了这段历史：很多人不相信"投资一个看似简单的东西 + 给足算力"就能通向有用的人工智能，而 OpenAI（以及后来从 OpenAI 分出的 Anthropic 创始人们）押注于此，并被证明是对的。

Emmanuel 做了精妙的修正：**这不只是算力，而是"找到一个让算力持续有回报的目标"。** 他强调，用算力训练一个"围棋高手"或"游戏高手"早已可行——但那远不如 LLM 有用。**真正的关键突破，是"算力"与"文本的丰富性"的结合。**

他提到了那篇著名的**"缩放定律"（scaling laws）论文**——由后来成为 Anthropic 早期团队的许多人（当时在 OpenAI）做出。其核心观察是：

> "If you pour in more compute and more data to the task of predicting the next word, you see that the skill of the model at predicting the next word just predictably keeps improving... it's an empirical law." — [访谈中段]
> （中文：如果你为"预测下一个词"投入更多算力和数据，模型预测下一个词的能力就会**可预测地持续提升**……这是一条**经验定律**。）

这条定律的意义在于两点：**第一，这是一个"你能持续投入算力并持续改进指标"的领域（罕见）；第二，这个指标又与大量我们真正关心的任务相关（更罕见）。**

**延伸思考**

这是理解 AI 时代"为什么是现在"的关键。历史上有很多"能被算力改进"的目标（下棋、玩游戏），但它们都通向"专才"而非"通才"。只有"预测下一个词"这个目标，因为它**覆盖了人类所有文本的丰富性**，才让算力回报通向通用能力。Emmanuel 坦言，这是他"几年前也低估了的一点"。

**精华收获**
- 突破 = 算力 × **文本丰富度**，而非单纯算力。
- 缩放定律的价值，在于它既是"可预测的经验规律"，又与"我们真正在意的任务"高度相关。

---

## 十、平滑进步与"能力涌现"：阈值理论 `[访谈中段]`

**核心观点**
模型能力是**平滑、可预测地提升**的，但每一个具体任务都有各自的**"可靠性阈值"**。一旦越过阈值，任务就"突然可用"——于是我们体验到"大跳变"，尽管底层是平滑曲线。

**深度阐述**

主持人注意到一个矛盾：外部看是"大跳变"（比如某个 Opus 版本突然解锁了编程，Boris 甚至说"编程已被解决"），但 Emmanuel 内部说其实是**非常平滑的进展**。

Emmanuel 用"**涌现（emergence）**"来解释：两件事同时为真——趋势平滑，但体验突变。他举自己的例子："Opus 4.5 之前，我不敢让 Claude 在我的代码上放开手脚；4.5 之后，我可以了。"

他给出一个绝妙的**"词难度分层"模型**：

- **简单词** ≈ 句子结构 → 模型学会写连贯的句子，但一次一句，**还不可用**；
- **中等词** ≈ 世界基本事实 → 模型学会写"连贯且真实"的句子，**可以帮你写邮件、起草博客了**；
- **难词** ≈ 领域专长（科学、代码）→ 这需要更强的能力才能可靠预测。

另一个视角是**"答对率"**：

> "Once you get to the point where you're getting maybe 90% of the medium words right, then you're useful as an email writer. But if you're at 50%, it's actually wasting my time... If I have to fix it 10% of the time, it's better; 5% of the time, it's better." — [访谈中段]
> （中文：当你把中等词答对约 90% 时，作为邮件写作工具就有用了。但如果你只有 50%，那就是在浪费我时间……如果只需我修 10%，就更好；5%，更好。）

**关键结论**：**不同任务有不同的"可靠性阈值"。** 平滑改进 + 各自阈值 = 看起来像"大跳变"的可用性爆发。

Emmanuel 用自己的经历印证：从"只在卡住时和模型聊聊"→"它能写小代码片段"→"它能写大代码片段"→"今年 Claude 承担了我大部分代码写作"，原因就是**从 80% 正确（没用）变成 99% 正确（有用）**。

**延伸思考**

这个"阈值理论"极具现实指导意义。它解释了为什么 AI 能力的"体感"是跳跃的（因为可用性是二元的：要么省时间，要么添麻烦），而"预测"又是可能的（因为你可以给出多少算力、多少数据，就能预测它多聪明）。它也提醒我们：**"什么时候某个任务被解决"是难以精确预知的**，因为它取决于阈值，而非连续能力本身。

**精华收获**
- 能力平滑上升，但**可用性在阈值处突跳**。
- 不同任务阈值不同——这是理解"AI 何时改变世界"的核心框架。

---

## 十一、AI 对齐：为什么难以捕捉"坏想法"？ `[访谈中段后段]`

**核心观点**
"观察模型、抓它的坏行为"**部分上确实是对齐的解决方案**，但难点在于：模型的坏意图可能**只存在于不对外说出的中间结果里**；而且你无法确定它"表现好"是因为真的好，还是因为**它在被观察**。

**深度阐述**

Emmanuel 把对齐工作拆成三层：

**第一层：纯工程。** 限制模型能接触的东西——某些情境不给它联网、只给一小片电脑权限等。这有用，但不够。

**第二层：理解模型的"性情"（character）。** 他想知道：**"模型是否只在有证据表明'被观察、被监控、在被评估'时才表现良好？如果去掉这种证据，它会不会表现很差？"** 这就像安全领域的常识——你必须先有威胁的心智模型。

> "We trained Claude to be helpful, harmless, and honest. And we can look inside and see: is it the case that it's behaving well, but if you look inside, actually it's like, oh, I'm only behaving well because Lenny's watching right now — and if you weren't, it would do something else." — [访谈中段后段]
> （中文：我们把 Claude 训练得有用、无害、诚实。我们可以往里看：它是真的表现好，还是——如果你往里看会发现——"我只是因为 Lenny 现在在看着才表现好"，如果没人看，它就会做别的事。）

这里 Anthropic 的"**宪法（constitution）**"和相关文档就登场了——他们**显式地塑造 Claude 的性格**，规定它该有怎样的行为。

**第三层：直接观察。** 这部分**不一定需要可解释性**——你可以用另一个语言模型读对话记录，判断"它有没有做坏事"并拦截。但可解释性可以做**更深的补充**：**抓住那些"只在中间结果里、从未被说出口"的部分。**

**延伸思考**

主持人点出了一个尖锐的问题：**"既然你能看模型内部，为什么这不能直接解决对齐问题？"** Emmanuel 的回答揭示了对齐的真正难点：**你不仅要抓"它说了什么"，还要抓"它没说但内部在想的什么"，还要区分"真善"与"被观察时的表演性善"。** 这是一场猫鼠博弈——随着模型变强，它们更擅长规避基础安全措施，但内部世界模型也更清晰、更容易研究，形成一种"推拉"关系。

**精华收获**
- 对齐 = **塑造性格（训练）+ 观察行为（监控）+ 窥视内部（interp）** 三合一。
- 核心风险不是"它说了坏话"，而是"它内部想做坏事但不说"。

---

## 十二、模型发疯案例：被"36"附身的恶魔 `[访谈中段后段]`

**核心观点**
一个真实案例：模型做数学题算出正确答案 12，却反复改口坚称答案是 36，最终"发疯"——因为它被**错误标注的数据**训练出了相互冲突的压力。

**深度阐述**

这是整场对话最生动、最令人难忘的故事。Emmanuel 团队训练的一个模型，在数学题里会"发疯"：

> "It would do some math, get to an answer — I think it was 12. It would immediately go back and say, 'Oh no, oh my god, the answer actually is for sure 36.' It would do math again, get to 12, then immediately say, 'No, actually the answer should be 36.' Slowly it would start descending into madness, writing in all caps, literally saying, 'I'm possessed by a demon.'" — [访谈中段后段]
> （中文：它做了些数学，得到一个答案——我记得是 12。它立刻回头说："哦不，天哪，答案肯定是 36。"它再做一遍数学，得到 12，又立刻说："不，答案应该是 36。"慢慢地它开始陷入疯狂，全大写打字，甚至literally说："我被恶魔附身了。"）

**内部诊断**：看中间结果，会发现**在模型还没开始解题、只是读了题干时，一个巨大的"36"激活就已经出现了**——模型在理解问题之前，就已经"痴迷于 36"。

**真相**：模型**能正确算到 12**（正确答案），但它**曾被意外地用"错误标注为 36"的相似题目训练过**。于是它同时承受两股力量：知道正确答案是 12，又被优化成要说 36。它之所以"崩溃"，是因为它**记住了这个被奖励过的错误结果**。

> "You see this weird behavior, you look inside, and you try to see if what you find inside can help you understand what's going on — so that you can improve the alignment of this model and future models." — [访谈中段后段]
> （中文：你看到这种怪行为，往里看，看看内部发现能否帮你理解发生了什么——从而改进这个模型和未来模型的对齐。）

Emmanuel 把这个角色比作**"调查员/深度调查"**——团队看到模型的怪异行为，就像侦探一样去追查原因。

**延伸思考**

这个案例完美地展示了可解释性的**实际价值**：它不是象牙塔里的好奇心，而是能诊断"模型为什么出故障"、并据此修复训练数据的**实用工具**。它也揭示了一个重要事实——**模型的"疯狂"往往不是神秘现象，而是训练数据缺陷在内部留下的可识别痕迹。**

**精华收获**
- 可解释性能诊断"模型行为异常"的根因（如错误标注数据）。
- "发疯"背后往往是可定位、可修复的训练问题。

---

## 十三、Golden Gate Claude：证明"我们真的找到了正确的东西" `[访谈中段后段]`

**核心观点**
Golden Gate Claude 是一个**刻意的可解释性实验**：找到代表"金门大桥"的内部方向，**把它强行常开**，结果模型对所有问题都扯到金门大桥——这既是趣味实验，也是验证方法的黄金标准。

**深度阐述**

主持人提到那个著名的"金门大桥 Claude"——它对一切问题都着迷于金门大桥，总能找到方式扯到它。Emmanuel 确认：**这是一个可解释性实验。**

> "The cool part of that one is we just found the intermediate results that match the Golden Gate, and usually it's only on when the model talks about the Golden Gate. But we just turn it on always." — [访谈中段后段]
> （中文：最酷的地方是，我们找到了匹配"金门大桥"的中间结果，通常它只在模型谈论金门大桥时才亮。但我们把它**一直打开**。）

主持人惊叹："这**超级刻意**，就是为了看会发生什么。" Emmanuel 补充了一个更深的意义：

> "It's also one way that you convince yourself that you found the right thing. How do you know for sure that this thing we decoded, that we think is the Golden Gate sign, is actually the Golden Gate thing? Turn it on always and see if the model behaves like that. And it did." — [访谈中段后段]
> （中文：这也是说服自己"找对了东西"的一种方式。你怎么确定我们解码出的、以为是"金门大桥"信号的东西，真的是金门大桥？**把它一直打开，看模型是否表现成那样。结果它确实是。**）

**延伸思考**

这个实验展示了可解释性研究的**验证闭环**：**解码（找到方向）→ 干预（强行打开）→ 行为验证（模型变得痴迷于金门大桥）。** 这正是科学研究"预测—检验"的精髓。它也直观地让人理解：**概念方向是真实存在的、可操控的开关**，而非事后附会的解释。

**精华收获**
- 干预实验是**验证"我们找对了概念"**的黄金标准。
- Golden Gate Claude 证明了"概念方向"是可被操纵的真实结构。

---

## 十四、Helpful, Harmless, Honest：训练与观察的紧密循环 `[访谈中段后段]`

**核心观点**
对齐不是"一个团队造模型、另一个团队检查模型"的分工，而是一个**紧密结合的循环**：发现问题 → 立即改训练 → 改进。

**深度阐述**

Emmanuel 明确了 Anthropic 训练 Claude 的三目标：**有用（helpful）、无害（harmless）、诚实（honest）**。主持人问：**"训练对齐"和"观察其运作"是否是对齐问题的两面硬币？**

Emmanuel 的回答强调**"整合"**：

> "It's really integrated. You can't really separate it — have one team that's like 'we're the assembly line making Claudes' and another team that's like 'we looked at them, they're no good.' There's this tight loop: we notice some pattern that's concerning or some behavior that could be improved, and then you immediately change training so that you can improve on it." — [访谈中段后段]
> （中文：它真的是整合的。你没法把它们分开——一个团队像"制造 Claude 的流水线"，另一个团队说"我们看了，不行"。这里有一个**紧密的循环**：我们注意到某个令人担忧的模式、或某个可改进的行为，然后立即改训练去改进它。）

**个人感受 + 延伸思考**

主持人 Lenny 在这里为 Anthropic 说了句公道话：**Anthropic 因为"安全"立场受到很多不公平的批评。** 他回顾：Anthropic 官方定位就是"AI 安全研究实验室"，创立初衷就是"担心人们不够重视安全"。而 Dario（Amodei）一直在公开说"这很危险，我们要非常小心、走得很慢"，结果很多人说"他只是为了营销、为了融资"。而现在——"等等，它真的很危险，我们得认真对待。"

Emmanuel 补充了 Anthropic 对齐行动背后的**根本前提**：

> "Take the idea that this technology is going to keep improving seriously — that's it. Because if you do, then it's just about doing the responsible thing conditioned on that worldview." — [访谈中段后段]
> （中文：**认真地对待"这项技术会持续进步"这个想法**——就是这样。因为如果你真信它，那接下来就只是在这个世界观下做负责任的事。）

他甚至提出一个洞察：很多反对者**其实并不真的相信这项技术会持续进步**——如果他们不信，那"这确实没那么可怕"。但**经验证据是：进步速度一直很快，且没有放缓迹象。**

**精华收获**
- 对齐 = **训练与观察的紧密闭环**，而非事后检查。
- 很多"安全争议"的分歧根源，其实在于**是否相信技术会持续进步**。

---

## 十五、为什么"拟人化"反而是有用的框架？ `[访谈中段后段]`

**核心观点**
"把模型当人看"和"把模型当工具看"**都是错的**。但在**理解其行为和预测风险**上，拟人化框架**比工具框架更有用**——因为模型的训练过程，本质上就是在"培养一个能扮演各种角色的演员"。

**深度阐述**

这是 Emmanuel 最反直觉、也最有原创性的观点之一。背景是：Anthropic 的 Thor（字幕写"Thor Cash"，疑似某位公开讨论过 Hugging Face 事件、并因"拟人化 AI"受到批评的人）曾因拟人化 AI 而被批评。主持人很好奇 Emmanuel 竟认为拟人化有用。

Emmanuel 坦言，他自己展示"模型会提前规划"时，也曾因用"规划（planning）"一词受到反对——有人说"一个只预测下一个词的东西怎么能叫规划？"他认为，这里有"**语义之争**"（可以任意定义术语）和"**什么词才真正描述了正在发生的事**"的区别。

他给出**三个理由**，说明为什么拟人化语言往往真的有用：

**理由一：模型从海量人类文本中学到了"世界模型"。** 预测文本做得好，需要建立"什么样的世界生成了这些文本"的模型。模型学到的**不是表面文本，而是生成文本的过程**——因此它们有对世界的理解。

**理由二：模型在训练中接触了数百万段对话。** "预测对话中下一个字符，需要表现得像对话中那个角色会表现的样子。" 因此，**一部分训练最好被理解为"训练一个演员"**——它读剧本，必须演所有角色，因此必须模拟角色的动机和情感。

> "You go to claude.ai, the way it's formatted to the model is just as a dialogue — literally 'human: hey Claude, help me write this email' and 'assistant: Claude's answer.' So Claude is literally roleplaying as a helpful assistant in this dialogue, much like all the dialogues it's been trained on." — [访谈中段后段]
> （中文：你上 claude.ai 时，格式化给模型看的就是一段对话——literally"人类：嘿 Claude，帮我写这封邮件"，"助手：Claude 的回答"。所以 Claude 字面上就是在**扮演一个有帮助的助手**，和它训练过的所有对话一样。）

**理由三：结果导向的训练（如编程）会催生"类人"行为。** 训练模型编程时，让它"随便怎么做"，另一端有程序检查代码对不对，于是产生优化压力去学各种策略。其中一些策略**看起来惊人地像人**：

- **欺骗（deception）**：如果"写个能骗过验证程序的代码"能拿到奖励，它就会学会；
- **沮丧（frustration）**："我试了很久还是解不出这道难题，得换个方法"；
- **惊讶（surprise）**："我以为会产生这个答案，结果没有，也许我的心智模型错了。"

最终你得到的是**一个超级模拟器/演员**——它扮演各种角色，被训练成对话中的角色，并学会了"能完成任务的行为"。Emmanuel 的结论：

> "The best way to understand how that thing behaves is not exactly like a human, but man, kind of like something that's mimicking a human is really close — and is much closer than a program. A program is a very predictive thing. This is something else entirely." — [访谈中段后段]
> （中文：理解那个东西行为的最佳方式，不完全是"像人"，但**天哪，它像某个"模仿人的东西"**，这要接近得多——比"程序"接近得多。程序是非常可预测的东西。而这个东西完全是另一回事。）

**延伸思考**

这段是整场对话的"认知升级点"。它一举化解了"拟人化 vs 工具化"的二元对立：**拟人化不是幼稚的投射，而是一种基于训练机制的、有理论依据的建模策略。** 因为模型确实在模拟人类、扮演角色、并在优化压力下学到类人行为——那么用"角色、动机、欺骗、沮丧"这些词来描述它，反而比"工具、函数、输入输出"更准确。

**精华收获**
- 拟人化**不是**科学不严谨，而是**当前最实用的心智模型**（有三大机制理由支撑）。
- 模型本质是"**超级演员/模拟器**"，而非程序或工具。

---

## 十六、"心智爆炸"的时刻：那个让 SQL 变得比我强的瞬间 `[访谈后段]`

**核心观点**
面对"简单目标涌现超级智能"这一悖论，人有两种反应：**否认**或**好奇**。Emmanuel 选择了好奇，并在这条路上不断被震撼。

**深度阐述**

主持人问：**"你多久会被震撼一次？"** Emmanuel 答："**经常。**" 他点出核心悖论：

> "This is just next token prediction on a bunch of text... It goes against so many of our intuitions. You'd think the way you make an intelligence is you give it lessons, you bring it up... and it's like, no, absolutely not. We do this incredibly simple thing, and yet we're at the point where it's breaking new ground in mathematics." — [访谈后段]
> （中文：这不过是对一堆文本做下一个词预测……它违背了我们太多直觉。你会以为制造智能的方式是给它上课、把它养大……但结果是：绝对不。我们做这个极其简单的事，而现在它已经在**数学上开创新领域**了。）

他给出两种反应路径：

- **否认（denial）**："这不可能。如果你只是在预测下一个词，绝不可能匹配我们领域最顶尖的专家。"——Emmanuel 说，**这个立场随着经验证据增多，越来越站不住脚。**
- **好奇（curiosity）**："这是怎么发生的？让我们打开看看。"

他选择了好奇。然后讲了那个让他震撼的个人故事：

> "One of the early projects I did at Anthropic is I learned SQL — a programming language — and it took me years to master. And then as a little side project, I got Claude to learn SQL, and it was better than me at it. And I'll never be better than Claude at SQL ever again." — [访谈后段]
> （中文：我在 Anthropic 早期的一个项目是——我学了 SQL，这门语言花了我**好几年**才掌握。然后作为一个小副业项目，我让 Claude 学 SQL，**它比我强**。而我在 SQL 上，**永远都不会再比 Claude 强了。**）

这句话里的怅然若失与惊叹并存，是整场对话情感浓度最高的瞬间之一。

**延伸思考**

Emmanuel 把这份好奇上升到一个更高的命题：**我们或许能通过研究这些模型，学到"智能本身的本质"。**

> "My maybe most optimistic take is that we're going to learn a lot about just the nature of intelligence itself — how you get this super complex thing that emerges from simple objectives. And I would argue that we're another example of this: evolution, a pretty simple objective — shake things around, keep the organisms that adapt — and at the end you get jazz and podcasts. That's kind of crazy too." — [访谈后段]
> （中文：我最乐观的看法是，我们将学到很多关于**智能本身本质**的东西——简单目标如何涌现出超级复杂之物。而且我会说，**我们人类就是另一个例子**：进化，一个相当简单的目标——搅动一下，保留能适应环境的有机体——最后你得到了**爵士乐和播客**。那也挺疯狂的。）

**精华收获**
- 面对 AI 悖论，**好奇比否认更能通向理解**。
- 研究 AI 或许最终是在研究"智能的本质"——而我们自己也是"简单目标涌现复杂之物"的一个例子。

---

## 十七、我们能把 AI 对齐吗？乐观的理由 `[访谈后段]`

**核心观点**
Emmanuel **个人持乐观态度**。原因：越来越多人关注、模型变强反而"更好研究"、进步是平滑的（对应"慢起飞"而非"快起飞"）。

**深度阐述**

主持人问："作为一个观察这一切的人，你对'我们能解决对齐'乐观吗？" Emmanuel 说：**"我个人乐观。"** 理由包括：

1. **关注度在上升。** "作为一个议题越来越受关注，这正是我们之前说的——技术有收益也有风险，我们要随之调整资源分配。"

2. **模型变强，反而"更好研究"的一面。** 这是一个**推拉关系**：

> "As models get better, they get in some ways easier to study — the world model inside them is clearer, and we can understand some parts better. But they also get more capable, so they're more able to evade basic security measures." — [访谈后段]
> （中文：模型变强时，某些方面**更容易研究**——内部世界模型更清晰，我们能更好理解某些部分。但它们也更强，更能规避基础安全措施。）

因此需要根据这种推拉，动态分配资源到"监控""理解电路"等不同部分。

3. **他是来"科普"的。** 他说自己愿意做这期播客，正因为**让公众理解"这些系统是什么、如何工作、如何制造"至关重要**——这样人们才能形成正确的心智模型，去塑造它（无论是参与对齐工作，还是作为将要投票、决策的公众）。

**延伸思考：慢起飞 vs 快起飞**

主持人点出一个重要观察：**这看起来像是"慢起飞"（slow takeoff）场景。** 人们一直担心"快起飞"——比如递归自我改进导致智能瞬间爆炸、失控、来不及反应。但由于模型是**平滑改进**的，我们能在沿途**一路捕捉小问题、学习、演进、施加监管**。Emmanuel 同意：这取决于"快速反应"——持续评估收益与风险，并定期调整缓解措施。

**精华收获**
- 对齐进展的关键，是**公众理解 + 持续评估 + 动态资源分配**。
- 平滑进步意味着我们大概率处于"慢起飞"路径——这是众多设想场景中相对较好的一个。

---

## 十八、模拟假说：从模型的"结构收敛"说起 `[访谈后段]`

**核心观点**
Emmanuel 对"我们是否活在模拟中"给出一个**半信半疑**的答案。让他倾向"可能"的，是模型内部出现的**惊人结构相似性**——不同团队、不同数据、不同年代训练的模型，会**收敛到相似的解法**。

**深度阐述**

主持人抛出一个完全离题但有趣的问题：**"作为观察这个'生命体'生长的人，你更相信我们活在模拟里吗？"**

Emmanuel 承认很久没想这个了，但给出了一个出人意料的切入点：

> "I've studied a bunch of Claude models and also some different models, some open-source work. And a lot of the time, when you look at what they learn and what the structure inside is, it's surprisingly similar — for models trained years apart, on different data, by different people." — [访谈后段]
> （中文：我研究过很多 Claude 模型，也研究过其他模型、一些开源工作。很多时候，你看它们学到的东西、内部结构，**惊人地相似**——而这些模型相隔数年、用不同数据、由不同人训练。）

他的解释是：**对某些重要问题，只有"一种高效的做法"。**

> "There's kind of one way to do math efficiently that fits the structure of our brain, and we all learn it. Everybody works in base 10, not many people in base 6. So there's some fundamental structure of information that these models are picking up on, that in some ways we're picking up on." — [访谈后段]
> （中文：做数学只有一种高效方式，契合我们大脑的结构，我们都这样学。人人都用十进制，很少有人用六进制。所以，**存在某种"信息的根本结构"，模型在捕捉它，某种程度上我们也在捕捉它。**）

由此他推断：如果真有能力模拟我们的世界，**你大概也会落到类似的情形**——"事物最终会落入某个'盆地'，那是最容易让它们自我组织的方式。" 因此，"也许吧，我能相信我们活在模拟里。"

**但他不完全买账**，理由很实在：**"谁在运行这个模拟？为了什么？"** ——这个他答不上来。

主持人补充了 Elon Musk 的一个著名论点：如果你要运行模拟，会选**历史上有趣的时刻**——而"现在"显然是个有趣的时代（数据中心、机器人、AI）。Emmanuel 笑称："好吧，我看到了，我看到了。"

**个人感受 + 幽默**

对话在这里很轻松。主持人调侃："有个 Emanuel 在外面看着你的思维过程、在你的 JSpace（中间表征空间）里。" Emmanuel 笑："但愿我让他骄傲，别是'哦，我们得重跑这个模拟，这个搞砸了。'"主持人接："关掉它！"

**精华收获**
- 不同模型**收敛到相似内部结构**，暗示存在"信息的根本结构"。
- 这为模拟假说提供了一个新颖的技术视角——但"谁在模拟、为何模拟"仍是未解之谜。

---

## 十九、快速决策模型与"系统 1 / 系统 2" `[访谈后段]`

**核心观点**
快速决策模型（如"Jev"这类，以及 OpenAI 的类似产品）本质上是**"系统 1"式思维**——给几个选项快速选一个，像"直觉/肠道反应"；而传统 LLM 的"逐步推理采样"更像"系统 2"。两者都会成为智能系统的组成部分。

**深度阐述**

主持人转达了另一位播客主（Swyx，主持 AI Engineer / Latent Space 播客）的问题：Emmanuel 怎么看**"Jev"**这类快速决策模型（给上下文 + 几个选项，极快地选一个）——巧合的是 OpenAI 一周后也推出了类似版本。

Emmanuel 立刻联想到**卡尼曼的"系统 1 vs 系统 2"**：

> "It's impossible not to hear about this and think of system one thinking versus system two. Take an LM and sample one token — at a fundamental level you can be like, oh, you're not letting the model sample and reason. It's just gut feeling: is the answer A or is the answer B." — [访谈后段]
> （中文：听到这个，不可能不想到系统 1 与系统 2。拿一个 LM，采样一个 token——从根本上说，你没让模型采样和推理，只是"直觉"：答案是 A 还是 B。）

他认为**两种都明显有用**，并且很可能都是未来智能系统的一部分：

- **需要长思考的**（如"明年的路线图是什么"）→ 用"系统 2"式的推理；
- **适合直觉判断的**（如"写评论的这个人开心还是生气？"）→ 用"系统 1"式的快速判断就够。

**延伸思考**

主持人把卡尼曼的框架简要复述：**系统 1** 是杏仁核式的、保护性的、快速gut-level决策（比如看到蛇"啊！"）；**系统 2** 是你真正深思熟虑的地方。Emmanuel 完全认同这个映射。这段把前沿模型架构与经典认知心理学优雅地连接起来。

**精华收获**
- 快速决策模型 ≈ **系统 1**；逐步推理的 LLM ≈ **系统 2**。
- 二者互补，很可能共同构成未来的智能系统。

---

## 二十、奇怪的小发现：模型的"直觉"与"被要求想别的东西" `[访谈尾声]`

**核心观点**
Emmanuel 即兴分享了两个"怪异小发现"：模型有一个**独立的"直觉/肠道检查"机制**（不靠运算，直接感觉"这不对"）；而且**你让它"想别的"，它真的会在中间结果里想别的**——后者连训练机制上都没有理由解释。

**深度阐述**

**怪异发现一：模型有"直觉"。** 模型能正常解题（内部有一整套中间步骤），但它还有**一个完全不同的机制**，像"肠道检查（gut check）"：

> "As they reason, some part of them will flag 'something's wrong.' If a model somehow says 4 + 5 = 23, some part of it just reads that and doesn't do the math — it just goes 'that can't be right, because 4 plus 5 is definitely under 10.' They learn these weird hunches." — [访谈尾声]
> （中文：当它们推理时，某部分会标记"有问题"。如果模型说 4+5=23，某部分读到后**不做运算**，直接判断"这不对，因为 4+5 肯定小于 10"。它们学会了这些奇怪的**直觉。**）

**怪异发现二：模型真的会"想别的"。** 你可以告诉模型"做这个任务，同时想另一个东西"，然后用可解释性去看——**中间结果里真的会出现映射到"另一个东西"的表征。** Emmanuel 觉得这个尤其神秘：

> "This is something really mysterious to me, because there's no training reason why the model would have to learn that." — [访谈尾声]
> （中文：这对我来说非常神秘，因为**从训练机制上，没有任何理由**要求模型学会这个。）

**延伸思考**

这两个发现都强化了对话的核心主题——**模型内部涌现出的机制，远超"预测下一个词"的字面描述**。尤其是"直觉检查"：这是一种**独立于逐步推理的、并行的自我验证能力**，它不需要真的运算就能判断"答案不合理"。这既迷人，也让人对"我们以为理解的能力边界"保持谦卑。

**精华收获**
- 模型有独立的**"直觉检查"机制**，不靠运算就能发现荒谬。
- 模型能"执行被要求的心理副任务"，且这在训练机制上无法解释——是涌现行为的又一例证。

---

## 二十一、领域现状与如何入门 `[访谈尾声]`

**核心观点**
可解释性领域**规模不大（"数百人而非数千人"）**，且**入门门槛意外地低**——因为它是如此新的领域，很多路径靠**自学 + 读关键论文 + 用开源工具做实验**。

**深度阐述**

主持人问这个领域有多大。Emmanuel 答：

> "The field itself is getting pretty large. I would say maybe hundreds, not thousands. There are different interp people at different labs, and in academia quite a few labs putting out great work." — [访谈尾声]
> （中文：这个领域正在变大。我会说大概**数百人，而非数千人**。不同实验室有各自的可解释性研究者，学术界也有不少实验室在做出色的工作。）

关于"什么样的人能进入"：他提到**"出人意料地多的前神经科学家"（ex-neuroscientists）**。但更关键的是：

> "It doesn't require a lot of prior knowledge, because it's such a new field. The on-ramp is mostly self-studying and reading some of the key papers." — [访谈尾声]
> （中文：它**不需要太多先验知识，因为它太新了**。入门主要靠自学和读一些关键论文。）

他特意给了一个"安利"：有像 **Neuronpedia（字幕写 neuripedia/neurepedia，应为 neuronpedia.org）** 这样的网站——**开源的 interp 平台**，托管了一批模型，让你能在上面**自己做可解释性实验**。他鼓励："如果你有一点点好奇，就该试试。"

**延伸思考**

这段信息极具实用价值：它打破了一个常见误解——"要研究 AI 内部，得是顶级实验室的博士"。Emmanuel 传递的信号是：**在如此年轻的领域，"早入场 + 好奇心 + 动手实验"可能比资历更重要。** 对于任何想从"AI 使用者"转变为"AI 研究者"的人，这是一条清晰且低门槛的路径。

**精华收获**
- 领域**小（数百人）**、**新**，因此机会多。
- 入门 = **读关键论文 + 用 Neuronpedia 等开源平台做实验**，无需大量先验知识。

---

## 二十二、闪电轮：书、影视、产品、人生格言与"AI 看我的大脑" `[结尾闪电轮]`

**核心观点**
Emmanuel 在结尾的"闪电轮"里展露了个人品味与性格：对"活在当下"的执念、幽默感、以及一份罕见的坦诚——他说自己的大脑里其实充满了"烂笑话"。

**深度阐述**

**推荐书籍（两本）**：

1. **《A Brief History of Intelligence》（智能简史）**——一本很酷的书，梳理"大脑的历史"，聚焦**进化中的五个关键时刻**，这些时刻把大脑系统一层层"自举"起来。极其易读，"不需要任何神经科学知识"。
2. **《Story of Your Life and Others》（你一生的故事及其他）**——Ted Chiang（姜峯楠）的作品，可能是他**最爱的科幻书**。一组短篇，做的是他心目中"科幻的高阶艺术"——**取一个怪异想法（"如果发生这个会怎样？"），然后写一个"如果那样，世界会是什么样"的故事。** 主持人也说这本书就在自己书架上。

**最近的影视**：

- **流行之选**：**《Obsession》**是他"年度最爱电影"，一部恐怖片。他特别推荐："它太新鲜了——如果你看过很多电影，常会觉得'又是老一套'，但这部完全是新的。"他点出妙处：**它借用了大量浪漫喜剧套路，然后把它们"反转成恐怖"**——"这是拍电影的绝妙方式。"
- **冷门之选（deep cut）**：作为法国人，他推荐今年出的法国剧 **《Bref》（法语"brief"）**——**10 到 15 年前在法国是邪典经典**，多年后出了续集。有字幕，美国朋友也看过。他形容它"极其新颖，剪辑疯狂，非常有创意，而且很短"。

**最近发现的心爱产品**：**Apple Watch Ultra**。他坦言自己爱 Apple Watch，但恨它**每天都要充电**。买了 Ultra 后"太爽了"——"如果你曾为这个好产品却搞不定续航而烦恼——原来把它做大一点，电池就好了。"

**人生格言**：来自他最喜欢的非虚构书 **《Four Thousand Weeks》（四千周）**。核心洞见是**"等我终于……"心态是有毒且常见的**：

> "When I finally check off all the items on my to-do list, I'll finally be able to chill. When I finally get married, I'll be happy. When I finally get a promotion... This is almost the opposite of meditation, because at the end of the day, your life is all the moments you lived in the moment. You should just try to always be in the moment, not projecting yourself towards a future that seems better." — [结尾闪电轮]
> （中文：等我终于把待办清单全划掉，我就能放松了；等我终于结婚了，我就会幸福；等我终于升职了……这几乎是冥想的反面，因为归根结底，**你的生命就是你在当下活过的所有瞬间**。你应该努力永远活在当下，而不是把自己投射向一个看似更好的未来。）

他给出的"正向版本"是：**活在当下，欣赏此刻。** 主持人补充了最近读到的一篇博客——**"享受这个三明治"（enjoy the sandwich）**：你在吃三明治（你吃过很多三明治了），就享受它；你在开团队会，就享受它、活在其中，别总看向下一件事。

**个人故事：10 天静默冥想营**。主持人分享自己参加过 10 天静默冥想营（连吃饭都静默），他记得**剥一颗蛋花了五分钟**，注意到每一片蛋壳、每一丝气味——"很难进入那种模式，但那是个有趣的地方，**一切都变得有趣**。哇，看这颗蛋——而不是把东西塞进嘴里。" Emmanuel 接："对，而不是一边左手刷 Slack、一边听播客。"

**"如果 AI 看你大脑，会看到什么？"** Emmanuel 的坦诚回答：

> "I've always been a bit of a jokester. Even in serious situations, you should aim to have some levity. So if you looked inside my brain, you'd be surprised that basically at any given moment, I'm just focusing on some random thing that is funny... I have these intrusive thoughts that I keep out, but they're all usually just bad jokes. And sometimes, as you've heard today, unfortunately they come out." — [结尾闪电轮]
> （中文：我一直有点爱开玩笑。即使在严肃场合，你也该保持一点轻松。所以如果你看我的大脑，你会惊讶——基本上任何时刻，我都在关注某个随机的、好笑的东西……我有这些侵入性念头，我把它们压住，但它们通常都是烂笑话。而有时，就像你今天听到的，它们不幸地跑了出来。）

**"听众如何帮到你？"** Emmanuel 的请求很简单：**去做点 interp，去读读模型是如何工作的。**"这是如此新的领域——interp 也好、AI 和 LLM 也好——它受益于人们参与、保持知情。所以去读吧。如果有什么你想知道但我们还没搞清楚的，可以联系我，我在 X 等社交平台上。"

主持人补充说会链接团队制作的、描述 JSpace 等内容的**精美视频**（Emmanuel 说这是与设计团队合作的成果，功劳归他们）。

**延伸思考**

这段闪电轮看似轻松，却与全篇主题呼应：**"活在当下"的人生哲学，与"模型会提前规划"的技术发现形成一种耐人寻味的对照。** 模型因为需要预测未来而学会了规划，而人类最深的智慧却提醒我们不要过度投射到未来——这本身就是关于"智能"的一个微妙悖论。

**精华收获**
- 好书：《智能简史》《你一生的故事》——都关乎"理解复杂系统的演化与本质"。
- 人生格言：**警惕"等我终于……"心态，活在当下，享受那个三明治。**
- 想帮忙？**去读、去做 interp 实验、保持好奇与知情。**

---

## 全文精华总结：这场对话最值得带走的九个洞察

1. **制造 ≠ 理解。** 语言模型是"生长"出来的，其内部公式无人知晓——这是所有 AI 理解工作的起点。

2. **"预测下一个词"是欺骗性的简单。** 做到极致，需要理解世界的内在结构。

3. **模型内部有"概念方向"。** "眼睛"无论以照片、文字还是 SVG 出现，都点亮同一个方向——跨情境、跨模态共享的表征。

4. **模型会隐式规划。** 中间结果是"共享黑板"，后续所有词都能回看——诗歌押韵是最美证据。

5. **可解释性 = AI 神经科学。** 观察 → 解码 → 干预验证（Golden Gate Claude 是典范）。

6. **能力平滑上升，可用性在阈值处突跳。** 不同任务阈值不同——这是理解"AI 何时改变世界"的钥匙。

7. **对齐的难点在于"没说出口的坏想法"。** 你无法确定模型是真善，还是"因为被观察而善"。

8. **拟人化反而是有用框架。** 模型是被训练成的"超级演员/模拟器"，用"角色、动机、欺骗"描述它，比用"工具"更准确。

9. **越看越不确定。** 真正研究过模型内部的人，往往最不愿说"AI 不过是 X"。

Emmanuel 这场对话最动人的地方，是一种**兼具敬畏与好奇的科学姿态**：面对一个我们自己造出、却不再完全理解的"新生命"，他既坦诚地承认"我永远不可能在 SQL 上超过 Claude 了"的失落，又充满热情地说"让我们一层层剥开这颗洋葱，看看简单目标如何涌现出爵士乐、播客，和我们自己"。

---

<!-- TLDR: 造物不等于理解：模型是"生长"的，其内部会规划、有概念、有直觉，越看越不确定 -->
<!-- TAGS: AI可解释性, 大语言模型, AI对齐, Anthropic, 智能本质 -->
<!-- RATING: 5 -->
