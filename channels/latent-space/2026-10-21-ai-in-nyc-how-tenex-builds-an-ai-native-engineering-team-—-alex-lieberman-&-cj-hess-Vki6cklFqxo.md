---
title: "AI in NYC: How Tenex Builds an AI-Native Engineering Team — Alex Lieberman & CJ Hess"
channel: "Latent Space"
published: "2026-10-21"
source_url: "https://www.youtube.com/watch?v=Vki6cklFqxo"
video_id: "Vki6cklFqxo"
tags: ["AI原生工程", "按产出付薪", "企业AI落地", "Agent部署", "工程组织"]
rating: 4
language: "英文"
word_count: 40715
duration: "43:33"
---

# AI in NYC: How Tenex Builds an AI-Native Engineering Team — Alex Lieberman & CJ Hess

- **Channel:** Latent Space
- **Published:** 2026-10-21
- **Source:** https://www.youtube.com/watch?v=Vki6cklFqxo
- **TL;DR:** AI 是原始智能，最难的是把它扩散进企业的"最后一公里"。
- **Tags:** AI原生工程, 按产出付薪, 企业AI落地, Agent部署, 工程组织
- **Rating:** 4

## 版本

- [结构化文稿](2026-10-21-ai-in-nyc-how-tenex-builds-an-ai-native-engineering-team-—-alex-lieberman-&-cj-hess-Vki6cklFqxo.structured.md)
- [原始文稿](2026-10-21-ai-in-nyc-how-tenex-builds-an-ai-native-engineering-team-—-alex-lieberman-&-cj-hess-Vki6cklFqxo.transcript.md)

# 当"产出"取代"工时"成为薪酬单位：Tenex 如何建造一支 AI 原生的工程团队

**材料信息**

- **标题**：AI in NYC: How Tenex Builds an AI-Native Engineering Team — Alex Lieberman & CJ Hess
- **作者/来源**：Latent Space 播客（在 AI Engineer 大会现场录制）
- **类型**：YouTube 视频字幕（现场访谈对谈）
- **关键元数据**：嘉宾为 Tenex 联合创始人 Alex Lieberman 与"特殊项目负责人"CJ Hess；对谈发生在 AI Engineer（AIE）大会现场；对话时间背景设定在 2026 年，因此提到的模型版本（如 Opus 5.5、GPT-5.1、Gemini 2.5 Pro、Sonnet 3.5 等）需按此语境理解。字幕为语音自动转录，存在若干拼写误差（下文会标注）。

> **关于本材料的一处重要说明**：字幕中公司名在标题里写作 **Tenex**，而在正文里被反复转写为 "10X / 10x / 10x.co"。本文统一以 **Tenex** 指代该公司，并在引用中保留字幕原貌。此外，"Cloud Code / Cloud Tag / Claude" 等词系语音识别误差，实为 **Claude Code / Claude Tag / Claude**；"codeex/codecs" 实为 **Codex**；"Lean Space" 实为 **Latent Space**。这些修正不影响语义，但有助于读者准确理解。

---

## 开篇引入

如果要用一句话概括这场对谈的价值：**它记录了一家把"激进薪酬实验"真正跑了 18 个月的公司，回过头来交出的成绩单——包括哪些赌注赢了，哪些边界被撞到了。**

大多数关于"AI 会如何改变工程团队"的讨论停留在预测层面：AI 会让工程师更高效、会让某些岗位消失、会重塑组织形态。但很少有人真的把公司押上去、把薪酬制度改成"按产出付费"，然后运营两年、雇佣 75 人、服务一半《财富》2000 强客户，再回来说："我们错了哪里，对了哪里。"

Alex Lieberman 和 CJ Hess 做的就是这件事。他们在 AI Engineer 大会现场，和 Latent Space 主持人（swyx，字幕中未点名）展开了一场极其坦诚的对话——从"工程师产出翻倍但时薪反而下降"的个人困境，到"故事点该通胀还是通缩"的量化难题；从企业 AI 采用率的四道"里程碑"（其中一道只有 5% 的企业跨过），到"你无法自动化一个不存在的流程"这句被反复验证的管理箴言。

这场对话最迷人之处在于它的**双重视角**：Alex 站在 CEO 位置思考商业模式、客户扩散与市场结构；CJ 站在一线工程师位置思考工具、流程、模型与杠杆。两人对同一件事的看法时有分歧，这种张力本身就是最真实的行业切片。

如果你关心"AI 时代的工程组织到底长什么样"、"按产出付薪可行吗"、"企业 AI 落地的真实瓶颈在哪"，这份材料几乎每一段都值得细读。

---

## 一、Tenex 是谁：把"最后一公里"当作生意 `[对话开篇 / 嘉宾重新自我介绍]`

**核心观点**
Tenex 的定位不是做模型，也不是做通用工具，而是做"应用型 AI 合作伙伴"，帮全球最大的公司从"用 AI 应用"进化到"AI 原生"——它押注的命题是：AI 是原始智能，最难的是把它扩散进真实经济的"最后一公里"。

**深度阐述**

主持人开场就要求两位嘉宾"从零开始重新介绍自己"，因为"人们对 Tenex 的故事只是模糊地熟悉"。Alex 给出了一个极其精炼的自我定位：

> "10X is an applied AI partner for some of the biggest companies in the world to help them go from AI apps into AI native. Our belief is that AI is incredible but it is raw intelligence and the hardest problem to solve is the final mile to actually diffuse it through the economy."
> （Tenex 是全球一些最大公司的应用型 AI 合作伙伴，帮它们从"AI 应用"走向"AI 原生"。我们的信念是：AI 令人惊叹，但它只是**原始智能**，最难解决的问题是打通**最后一公里**，让它真正渗透到经济中去。）
> `[对话开篇]`

这段话是理解整场对话的钥匙。它包含两个层次的判断：

**第一，"原始智能"与"可用能力"之间存在巨大鸿沟。** 模型再强，也只是"原材料"；企业要把它变成生产力，需要有人解决集成、流程、权限、评估、变更管理等一系列"脏活"。Tenex 就是干这些脏活的。

**第二，"扩散"（diffusion）是核心动词。** 这个措辞非常关键——它暗示 Tenex 的自我认知不是"技术公司"，而是"技术扩散的催化剂"。Alex 后来说得更直白：纽约有海量商业，是"技术扩散能真正影响这个国家 GDP"的地方。换句话说，他们把自己看作经济结构转型的一环，而非单纯的软件供应商。

值得注意的是对谈的**氛围基调**：一开场就插科打诨地讨论"能不能爆粗口"、"Apple Podcast 有 explicit 标签但 YouTube 不喜欢 f 词"、主持人笑称"我们是给成年人做的节目"。这种轻松、甚至有点叛逆的语气贯穿全程——它透露出这家公司的文化气质：**直率、不装、成年人之间的坦诚交流**。这种文化底色在后面讨论"我们哪里错了"时体现得尤其明显。

**延伸思考**

"最后一公里"这个隐喻在科技史上反复出现：宽带入户、电商物流、SaaS 落地……每一次技术革命的价值实现，往往不取决于技术本身有多强，而取决于"最后一公里"能不能被打通。Alex 的判断意味着：**在 AI 时代，最稀缺的可能不是模型能力，而是"把能力装进组织"的工程与管理能力。** 这为后面所有关于流程、标准化、agent 部署的讨论埋下伏笔。

**精华收获**
- 判断一家 AI 公司时，关键问题不是"它用多强的模型"，而是"它解决哪一段最后一公里"。
- "原始智能"与"可用生产力"之间的鸿沟，本身就是一门生意的根基。

---

## 二、CJ 的加入：当"产出变好变快，收入反而下降" `[对话开篇 / CJ 自述]`

**核心观点**
CJ 的入职故事浓缩了整个行业的荒诞感——他做 AI 咨询后，产出越来越快、越来越好，但因为按时薪收费，收入反而下降。正是这个矛盾，把他推向 Tenex 的"按产出付薪"模式。

**深度阐述**

CJ 是 Tenex 的**第一位员工**——他加入时"甚至不确定 Alex 和 Arman 有没有起好 Tenex 这个名字"。他自嘲在 Tenex 之前有一座"创业坟场"（a graveyard of startups），最终汇聚成一个自己的工程咨询公司。

他的自述是全场最生动、最有共鸣的一段：

> "I'm a software engineer by trade and I just felt my output getting better and faster and ultimately getting paid less. Like I was charging hourly to my clients."
> （我是科班软件工程师，我眼看着自己的产出越来越好、越来越快，最终却赚得越来越少——因为我按时薪向客户收费。）
> `[对话开篇]`

这句话道出了 AI 时代一个深刻的悖论：**在"按时间付费"的旧契约下，效率提升反而是对生产者自己的惩罚。** 你越会用 AI，单位任务的耗时越短，按小时计费的收入就越低。这是 CJ 个人困境，也是整个专业服务业的集体困境。

他随后谈到自己被 Alex 吸引的原因——一条推特：

> "I really liked kind of the ethos of 10x that Alex had first posted... about looking to reward engineers for their output as opposed to rewarding them for their time."
> （我很喜欢 Alex 最早发的那条推特里 Tenex 的精神——奖励工程师的**产出**，而不是奖励他们的**时间**。）
> `[对话开篇]`

这里有一个重要的**时间线判断**。CJ 承认，在加入当时（他提到 Sonnet 3.5、Gemini 2.5 Pro 的时代），"工程师能大规模并行工作、产出暴增"这件事"可能还不是很明显"。他做了一个赌注：

> "I basically took the bet that I think with my skill set and leaning more into AI, I could have much higher output and ultimately have like a higher earning capacity... I think that's what the future of engineering really looks like."
> （我基本上是下了个赌注：凭借我的技能、更多地押注 AI，我能有更高的产出，最终有更高的赚钱能力……我认为这就是工程未来的样子。）
> `[对话开篇]`

这个"赌注"叙事非常关键。它不是事后诸葛亮式的成功学，而是一个**在趋势尚未明朗时押上职业生涯的决策**。CJ 特别强调了时间点的重要性——如果连他都在当时看不清楚，说明这不是一个"人人都懂"的机会，而是需要判断力的下注。

他的最后一句点明了整个薪酬哲学的经济学根基：

> "When AI is solving all these tech problems, companies are going to pay based on outcome and they're not going to want to pay based on the time that's required to build something."
> （当 AI 解决了所有这些技术问题，公司会按**结果**付费，而不会愿意按**建造所需时间**付费。）
> `[对话开篇]`

**个人感受**

CJ 的这段话带着一种"过来人"的真诚——他没有美化自己的创业失败（"坟场"），也没有夸大加入 Tenex 的必然性（"下了个赌注"）。这种坦诚让他的论点更有说服力：**这不是一个被证明后才被追随的真理，而是一个需要承担风险才能兑现的判断。**

**延伸思考**

"按时间付费"是工业时代的遗产——它假定产出与时间线性相关。但当 AI 让产出与时间脱钩，"时薪制"就成了效率的敌人。这不只影响工程师，也影响律师、设计师、咨询顾问、医生等所有"专业知识按小时出售"的职业。**如何为"杠杆化的人类智能"定价，可能是未来十年最重要的组织经济学问题。**

**精华收获**
- 效率提升 + 时薪制 = 自我惩罚。这个悖论会逼迫整个专业服务业重新设计薪酬契约。
- 真正的机会往往出现在"趋势尚不明显"之时——CJ 的下注之所以有价值，恰恰因为它当时并不显然。

---

## 三、按故事点付薪：一个"押注人类智力杠杆"的薪酬实验 `[关于薪酬模式]`

**核心观点**
Tenex 的薪酬模型是"按故事点付费"——工程师的产出被量化，收入与其挂钩。这个模型隐含一个激进判断：AI 是对"人的智力与工作伦理"的杠杆化押注，因此收入方差会前所未有地拉大。

**深度阐述**

主持人回忆了他们上一期播客的核心内容："你们字面上是按故事点给人付钱的，你只需要就故事点是什么达成一致。"这个模型有两个直接后果：**顶尖工程师可以年入百万美元，而效率较低的工程师收入会低得多。**

Alex 毫不避讳地把这个逻辑讲透：

> "The thesis is that AI is really just a leveraged bet on a human's intellect and work ethic. And so you're just going to have more variance than ever before in earning capacity."
> （这个论点是：AI 本质上只是对一个人**智力与工作伦理**的杠杆化押注。因此，赚钱能力的**方差**会比以往任何时候都大。）
> `[关于薪酬模式]`

这句话值得拆解。"杠杆化押注"意味着：AI 放大了个人能力的差异。一个本身基础扎实、又拼命善用前沿工具的工程师，其产出可能是普通人的数倍；反之，不会用 AI 的人会被甩开。结果是**收入分布的方差扩大**——不是所有人一起涨薪，而是头部极高、尾部相对低。

Alex 明确承认这个模型"不是给所有人的"：

> "Our model isn't for everyone, but for the person who basically wants to go along themselves, who has this incredible foundation in software engineering, but also is constantly pushing themselves to leverage the frontier to stretch their time as much as possible while having quality output. There's no better way to earn."
> （我们的模式不是给所有人的。但对于那种想靠自己往前冲、有极强软件工程基础、又不断逼自己利用前沿工具、在保证质量产出的同时尽量延展时间的人——没有比这更好的赚钱方式了。）
> `[关于薪酬模式]`

这是一个**自我筛选机制**：模型会主动吸引高自驱、高能力的人，筛掉追求稳定的人。Tenex 不是在"普惠地提高工程师收入"，而是在"为顶尖杠杆使用者提供溢价"。

主持人追问了一个具体数字：上次提到有"两三个人年入超过百万美元"，现在如何？Alex 给出了一个更系统的画像：

- 公司成立 **18 个月**，最初是"AI 驱动的开发外包店"（AI-powered dev shop）
- 起步的洞察来自联合创始人 Arman：他身边有人"还在往 IDE 里手动敲代码，完全不采纳新技术"
- 客户结构已经上移：**50% 是《财富》2000 强，50% 是营收 1-5 亿的中端市场公司**
- 今天 **75 人**，其中 **90% 是工程师或"AI 策略师"**（可理解为技术顾问）
- 最关键的数据：**最高薪与最低薪工程师的收入差距约为 4 倍**

**这个"4 倍"是全场的点睛之笔。** 主持人原本以为会听到"10 倍"，Alex 笑着纠正：

> "Not 10x difference... It's probably something around 4x difference."
> （不是 10 倍差距……大概是 4 倍左右。）
> `[关于薪酬模式]`

这个自我纠正极具信息量。它说明：**现实比"10x 工程师"的传说要温和得多。** 模型跑通了两年的结果是"显著但非极端的方差"，而非"赢者通吃"。这既是对过乐观叙事的降温，也是对模型可行性的验证——如果差距真是 10 倍，团队的公平感和协作性可能会崩溃。

**延伸思考**

"按产出付薪"在知识工作中一直是禁忌，因为产出难以度量、且容易导致内耗。Tenex 的贡献在于：**用 AI 时代的可量化性（故事点、可观测的交付）重新打开了这个潘多拉魔盒。** 但 4 倍而非 10 倍的现实，提示我们：即使有 AI 放大，人类能力分布本身也是有限的——**杠杆放大的是差异，不是差异的无限化。**

**精华收获**
- AI 是"对人类智力与工作伦理的杠杆"，所以收入方差扩大是结构性结果，而非管理失误。
- 但实测方差约 4 倍而非 10 倍——现实比传说温和，这对模型的可持性至关重要。

---

## 四、模型跑通了吗？两个"经典担忧"为何没有成真 `[关于薪酬模式的反思]`

**核心观点**
按产出付薪的两个经典担忧——"故事点主观、会被注水"和"会为了凑数交付烂代码"——在实践中都没有成为问题，因为 Tenex 用"AI 策略师"的角色设计形成了相互制衡的激励。

**深度阐述**

Alex 主动抛出了这个模型最常被质疑的两点：

> "The classic concerns are, well, story points are subjective. People are going to either sandbag story points or they're just going to ship a bunch of bad code... barely check the box... but not actually do the job."
> （经典的担忧是：故事点是主观的，人们要么会给故事点**注水**，要么就交付一堆**烂代码**……勉强打个勾……但并没有真正完成工作。）
> `[关于薪酬模式的反思]`

然后他给出了一个漂亮的答案：

> "Those two concerns have not been concerns at all because of our AI strategists. We incentivize, I think perfectly at odds with engineers, where AI strategists are incentivized for customer retention and growth."
> （这两个担忧根本不成问题，因为我们的 **AI 策略师**。我们把他们的激励设计成与工程师**恰好对立**——AI 策略师按客户留存和增长获得激励。）
> `[关于薪酬模式的反思]`

这是一个精妙的**机制设计**案例。工程师想多拿故事点，AI 策略师想让客户满意并续约。前者追求"多产出"，后者追求"产出被客户认可"。两个角色利益对立，自然形成制衡——工程师注水或交烂代码，AI 策略师会受损并施加压力。这是用**组织内部的对抗性激励**替代了自上而下的质量审查。

Alex 坦言，**真正的难点其实在别处**：

> "The biggest challenge has been how do you compensate engineers for all the time that's not spent coding, whether it's architecting, meeting with clients... That's where we've had to find nuance in the comp model."
> （最大的挑战是：如何为工程师**不写代码的时间**付酬——架构设计、见客户等等……这是我们必须找到微妙解法的地方。）
> `[关于薪酬模式的反思]`

CJ 补充了一个更深刻的观察，预示了模型未来的演进方向：

> "I was coding a lot, coding a lot, coding a little less and now we're kind of getting to the point where the models are more or less given the right context and can get you to 90% of the solution. The value is sitting down with a customer, hearing everything they can brain dump and then just providing that to the model to actually get closer to the solution."
> （我以前大量写代码，然后写少一点，现在我们快到了这样一个点：模型只要给定正确的上下文，就能把你带到解决方案的 90%。价值在于**坐下来听客户把脑子里的一切都倒出来，然后把它喂给模型**，从而更接近解决方案。）
> `[关于薪酬模式的反思]`

这段话揭示了薪酬模型的一个深层张力：**如果模型能完成 90% 的代码，那么"写代码"就不再是价值核心，"获取高质量上下文"才是。** 但"听客户倾诉"这种能力很难用故事点量化。CJ 预测未来会更关注"产出到底是什么、如何运作、长什么样"，但仍然"锚定故事点作为单位"。

**延伸思考**

这是一个典型的"**度量悖论**"：当一个指标（故事点）成为薪酬依据，它就会被博弈（古德哈特定律）。Tenex 的解法不是设计一个完美指标，而是**引入一个激励相反的制衡角色**。这提示我们：在复杂组织中，与其追求"完美度量"，不如设计"相互制衡的角色结构"。

**精华收获**
- 对抗性激励（工程师 vs. AI 策略师）比自上而下的审查更能防止指标博弈。
- 当模型能完成 90% 代码时，价值从"写代码"转移到"获取上下文"——而后者更难量化。

---

## 五、Meta Harness：把工程流程变成可复用的"元框架" `[关于 meta harness]`

**核心观点**
Tenex 把工程工作流标准化成一套"元框架"（meta harness）——一个结构化的文档仓库加 CLI，让模型驱动的长任务能自动、标准地运行。核心洞察是：**上下文不应存在人脑或对话里，而应存在于仓库中。**

**深度阐述**

Alex 主动提起一个他觉得"人们会觉得有意思"的话题——"元框架"（meta harness）。CJ 详细解释：

> "We basically started trying to standardize a set of skills... That grew into what is actually a very structured set of documentation within a repo and then a CLI around it that the models are using to actually drive the work... whether it's creating a plan, a visualization, creating some readout for a client."
> （我们开始尝试把一套技能标准化……它成长为一个仓库内**高度结构化的文档集**，外加一个围绕它的 **CLI**，让模型用它来驱动实际工作——无论是制定计划、做可视化，还是为客户生成一份说明。）
> `[关于 meta harness]`

这个 meta harness 有几个关键组件：

1. **一份"权威计划文档"（canonical plan document）**：有相似的结构，但"随着模型变强，我们实际上**减少了**对结构的强制要求"——这是一个重要的进化信号：当模型足够聪明，过度的脚手架反而成为负担。

2. **一个有主张的决策记录方式**：agent 如何记录决策、记录自己做了什么、追踪进展，"全部 check in 到 Git 里"。

3. **格式从 Markdown 转向 HTML**：CJ 说他现在"更喜欢 HTML 而非 Markdown，因为我喜欢看 agent 吐出来的**图画书**（picture books）"——这是一个生动细节，说明人机协作的界面正在变得更可视化。

CJ 道出了这套系统的哲学核心：

> "Not only do you have the code as the source... I think there's a debate on do you even need docs, the code can actually be the memory of a codebase. And I do think you do. You need to know **why** you made a decision. You need to know the context around the conversation that was had."
> （不仅代码是源头……我认为有个争论是"你到底需不需要文档，代码本身可以成为代码库的记忆"。我确实认为你需要。你需要知道**为什么**做某个决定，需要知道那次对话的上下文。）
> `[关于 meta harness]`

最后一句是整段最有力的收尾：

> "We just always have that in some durable record and it's never like in someone's head. It's always in the repo. So that just gives our agents and our tools these superpowers to have all the context that a lot of engineering teams still just have in conversations or have in their heads."
> （我们总是把它保存在某种**持久记录**里，从不放在某人脑子里，总是在仓库里。这赋予我们的 agent 和工具一种超能力——拥有那些很多工程团队仍然只存在于对话或脑子里的全部上下文。）
> `[关于 meta harness]`

**延伸思考**

"上下文存在于仓库而非人脑"这句话，是 AI 原生工程组织的一个关键原则。传统团队的知识是**隐性的、分散的、易流失的**（人一走，上下文就没了）；meta harness 把知识**显性化、集中化、可被 agent 消费**。这不仅提升 AI 效率，也提升人类协作效率——它是一个"双赢的副作用"。这也呼应了后文"你无法自动化一个不存在的流程"：**能被自动化的前提，是流程已经被显性化。**

**精华收获**
- 上下文应该在仓库里，不在人脑里——这既服务于 agent，也服务于人。
- 随着模型变强，脚手架应**减少**而非增加；过度结构化会成为负担。

---

## 六、故事点的"通胀 vs 通缩"：一个没有标准答案的校准难题 `[关于产出度量]`

**核心观点**
Tenex 用一个简单指标衡量流程是否有效——"每个工程师每月平均故事点是否上升"。今年产出大约翻倍，但"一个故事点是否还值同样的钱"成了一个类似"通胀/通缩"的校准难题，公司每季度都要重新评估。

**深度阐述**

主持人问：如何衡量这些流程是否有效？Alex 给出一个直白的指标：

> "Are we seeing an increase in trend in average story points per month of every engineer in the company?"
> （我们是否看到公司每位工程师的**月均故事点呈上升趋势**？）
> `[关于产出度量]`

当被问到与年初相比增长多少，CJ 先开了个生动的玩笑——他想起推特上一张图，"一个人悬在一个**巫师水晶球**上方，天上有各种东西飘着"，他说这就像他看到某些工程师"挥舞 agent"时的样子。然后给出数字：

> "I'd really say overall it's been like a **2x increase** this year in particular... If you think of December as the Opus 4.5 moment where the models really started to take on these long-running tasks, to today where we're back to Opus but Opus 5.5... over that period I've seen the actual output of engineers roughly **double**."
> （我可以说今年整体大约是**翻倍**……如果把 12 月看作 Opus 4.5 时刻——模型真正开始承担长任务——到今天我们又回到 Opus，但是 Opus 5.5……在这段时间里，我看到工程师的实际产出大约**翻了一倍**。）
> `[关于产出度量]`

这里 CJ 划出了一条清晰的技术时间线：**12 月的 Opus 4.5 是"模型开始能干长任务"的转折点，而 Opus 5.5 则把能力推到了新高度。** 这解释了为什么产出翻倍发生在"今年"。

然后是最精彩的一问一答。主持人问："**现在一个故事点还和一年前值一样多的钱吗？**"

CJ 笑着把问题比作通胀：

> "We're always trying to calibrate. It's a tricky equation... In theory, in theory, there should be deflation."
> （我们一直在校准。这是个棘手的方程式……理论上，理论上应该**通缩**。）
> `[关于产出度量]`

这个回答极有洞察力。逻辑是：如果同样的产出（故事点）现在更容易达成（因为模型更强），那么每个故事点的"含金量"应该下降——否则公司就是在为"更容易的事"付同样的钱。但 Alex 补充了另一半张力：

> "At least once a quarter we sit down and evaluate what is our criteria for these story points... There's a fine balance between still rewarding this output but also, as the models get better, we need to be able to calibrate the value that we're creating."
> （至少每季度我们会坐下来评估故事点的标准是什么……在"继续奖励产出"和"随着模型变好、需要校准我们创造的价值"之间，有一个微妙的平衡。）
> `[关于产出度量]`

**这是一场永无止境的博弈：公司想让工程师持续高产，工程师想保住单位产出的价值。** 模型越强，这个矛盾越尖锐——因为"同样的故事点"越来越容易赚到。

**延伸思考**

"故事点通胀/通缩"看似是内部管理细节，实则触及一个宏观问题：**当 AI 让生产力指数级提升，产出单位该如何定价？** 如果所有公司都面临这个校准难题，那么整个"按产出付费"的市场都需要一套新的定价协议。Tenex 的季度校准，是一个微观层面的"货币政策"实验。

**精华收获**
- 衡量流程有效性的简单指标：人均月均产出趋势。
- 模型变强会制造"故事点通缩压力"——这是按产出付费模式必须持续校准的核心矛盾。

---

## 七、模型偏好：Opus 5.5 的"大一统"与 AMP maxxing `[关于模型选择]`

**核心观点**
Tenex 让工程师自由选择工具，但当前团队高度趋同于 **Opus 5.5**（作为主力）搭配 **Codex**（用于审查）。CJ 坦言自己"AMP maxxing"，因为 AMP 把一切搬离本地电脑、提供云端"orbs"环境，并支持跨模型协作。

**深度阐述**

主持人切入"模型偏好"这个永恒话题。CJ 给出当前状态：

> "The vibe right now is Opus 5.5... Opus is so good. It's fast, it's cheap, it kind of hits all my check boxes. I previously have had like two to three models depending on whether they're cheap and fast, whether they're really smart... and now Opus is kind of covering my full range."
> （现在的氛围是 Opus 5.5……Opus 太好了。它快、便宜，几乎满足我所有条件。我以前要备 2-3 个模型——有的便宜快、有的聪明……现在 Opus 覆盖了我的全频段。）
> `[关于模型选择]`

这是一个"**模型收敛**"的信号：曾经需要多个专用模型（快而便宜 / 慢而聪明）的组合，现在被一个模型全覆盖。对用户是便利，对模型供应商则是残酷的赢家通吃。

团队的工作流是**双模型协作**：

> "Using both is still the best option. Whichever your driver is, which I think for most of our team is Opus 5.5, using a Codex to review and having them actually work back and forth on your machine, I think still produces the best results."
> （两个都用仍然是最好的选择。无论你的主力是什么——我们团队大多数人用 Opus 5.5——用 Codex 来**审查**，让它们在你机器上**来回协作**，我认为仍能产出最佳结果。）
> `[关于模型选择]`

**"一个写、一个审"的双 agent 模式**是这里最值得记下的工程实践。

接着 CJ 谈到他偏爱 AMP 的理由——**它把计算搬离本地**：

> "I love AMP because it takes everything off my computer. They have this cloud setup, the orbs... They recently launched the ability to hook in your Claude Code subscription, so that's been a pretty big game changer for me... it'll really cut your cost by like 80%."
> （我爱 AMP，因为它把所有东西搬离我的电脑。他们有云端设置，那些 **orbs**……他们最近推出了接入你 Claude Code 订阅的功能，这对我是个大变革……能砍掉大约 80% 的成本。）
> `[关于模型选择]`

主持人抛出一个尖锐的观察：**为什么 Anthropic 从未像 AMP 那样把"远程环境"这件事做透？** CJ 的回答很中肯：

> "There's a piece of that on the AMP side of them being very opinionated and not trying to build this general solution... part of the reason I love AMP is that it has all these **cross-model functionalities**."
> （一部分原因在于 AMP 非常**有主张**，不去做通用解决方案……我爱 AMP 的一部分原因是它有所有这些**跨模型功能**。）
> `[关于模型选择]`

他甚至描述了一个具体的协作场景：让 Opus 写，然后"跳到另一个 orb，说'看看那个 orb'，让它来审查"——**云端多 agent 协作**。而 Claude Code / Claude Tag 更适合"在非技术任务上协作的团队"，但在跨模型编排上"我到达不了那个程度"。

**延伸思考**

"AMP maxxing"和"orbs"揭示了一个趋势：**开发环境正在从"本地 IDE"迁移到"云端 agent 编排平台"**。当计算不再绑定于个人电脑，工程师的角色从"操作工具的人"变成"调度一组云端 agent 的指挥者"。这与后文"成为 agent 管理者"的主题直接呼应。

**精华收获**
- 主力模型正在收敛为单一强者（当前是 Opus 5.5），但"一个写、一个审"的双模型协作仍是最佳实践。
- 云端 agent 平台（orbs）的核心价值是跨模型编排与成本削减，而非单纯的本地替代。

---

## 八、Token 花费 vs. 员工花费：成本焦虑的"理性边界" `[关于成本与数据经济]`

**核心观点**
Tenex 的 token 花费与员工花费之比约为 1:1 到 2:1，属于偏高水平。但两人都认为，"token maxxing 会把公司搞垮"的时代（6-8 个月前）已经过去——因为单任务成本在快速下降，"理性使用"的边界越来越清晰。

**深度阐述**

主持人引入一个他今年开始追踪的指标：**token 花费占员工花费的比例**。他给出的行业基准：大多数公司每人 10-200 美元，AI 原生公司约 10%，平均 AI 创业公司约 1:1，最高到 5:1 到 10:1。Alex 回应：

> "I actually don't have a number off the top of my head. I'd say we're somewhere between... one and maybe like two to one. That's pretty high."
> （我手头没有确切数字。我猜我们在 1:1 到 2:1 之间。那是相当高的。）
> `[关于成本与数据经济]`

然后他谈到"**何时该动用最强模型**"的思考，并透露一个好消息：

> "Recently our costs have been driven just way down from Opus 5.5. We kind of had an era of like everyone was using Astra and Fable and they just gave the best results but ultimately those models are [expensive]."
> （最近我们的成本因为 Opus 5.5 而**大幅下降**。我们曾经历过一个时代，人人都用 Astra 和 Fable，它们给出最好的结果，但最终那些模型很贵。）
> `[关于成本与数据经济]`

主持人点出一个行业现象：**"token leaderboard"（token 排行榜）的狂欢之后，大家突然发现"成本太高了"**——"这是世界上最可预测的事"。Alex 承认他们确实担心过，尤其随着headcount增长：

> "Even though our team... I don't feel like anyone ascribed to the token maxxing zeitgeist... but it's like, well, if the boss is going to pay for it, I'm just going to go nuts, right? Because then you do the weird stuff so that you can scale back, but you have to do the weird stuff first to discover the lessons."
> （虽然我们团队……我不觉得有人信奉 token maxxing 的潮流……但问题是，如果老板付钱，我就放开手脚干，对吧？然后你做一些**奇怪的事**，以便之后能收敛——但你必须先做那些奇怪的事，才能学到经验。）
> `[关于成本与数据经济]`

**"必须先烧钱做奇怪的事，才能学到收敛的边界"**——这是对"探索期"最坦率的辩护。

接下来 Alex 展开了一段**关于数据公司未来的深度思辨**（他称之为与之前的对话相关）。他谈到 Micro1、Mercor、Handshake 这类数据公司：90% 以上收入来自实验室，但一些创始人认为未来会翻转为"企业驱动"。Alex 的推理链条是：

1. 如果企业成为数据核心买家，前提是企业要大量**自建微调模型**
2. 微调的理由要么是**质量**（但前沿模型的标杆一直在移动，是"硬赌"），要么是**价格**
3. 价格论证很难成立，因为"token 成本持续下降"

因此他的结论是：**"token maxxing 搞垮公司"的时代已经过去**：

> "It almost feels like we've hit this point where costs are coming down on a per-task basis that it is way harder today for someone to token max and really f the company in terms of cost than it was six to eight months ago."
> （几乎感觉我们已经到了一个点：单任务成本在下降，今天某人想靠 token maxxing 把公司成本搞垮，比 6-8 个月前难多了。）
> `[关于成本与数据经济]`

CJ 部分同意，但保留了一个"未来可能回摆"的情景：

> "If there's a world where there's an Astra 6.5, a Fable 5.5, and they're super expensive but they get the best results, I could see us trending back that direction."
> （如果出现一个 Astra 6.5、Fable 5.5，超级贵但结果最好，我能看到我们可能回摆到那个方向。）
> `[关于成本与数据经济]`

他最后用一句极精辟的话概括了"为什么不必恐慌"：

> "A lot of tasks that are economically valuable can be done with Opus 5.5... Would a 10 times smarter model really justify the cost of moving some cells in a spreadsheet? Probably not."
> （很多有经济价值的任务，用 Opus 5.5 就能做……一个聪明 10 倍的模型，真的值不值得为"在表格里挪几个单元格"付那个钱？大概不值得。）
> `[关于成本与数据经济]`

**延伸思考**

这里藏着一个重要的经济学判断：**"够用"（good enough）会压制"最好"（best）的溢价。** 对绝大多数有经济价值的任务，Opus 5.5 已经"够好"，10 倍智能无法带来 10 倍价值。这意味着前沿模型的军备竞赛，其商业回报可能存在天花板——**成本下降不是因为模型变弱，而是因为"够用"成了主导需求。**

**精华收获**
- Token 成本在单任务层面快速下降，使"失控烧钱"的时代基本结束。
- "10 倍智能值不值 10 倍价格"——对大多数任务，答案是"不值"，这是成本理性回归的根本原因。

---

## 九、企业 AI 的四级里程碑：从 90% 到 5% 的"扩散断崖" `[关于企业采用率]`

**核心观点**
Alex 把企业采用 AI 划分为四道"里程碑"：通用 LLM 部署（90%）、培训赋能（60%）、编码 agent（50%）、非工程生产级 agent（仅 5%）。**最大的扩散鸿沟在最后一档**——绝大多数千人以上企业，还没有一个真正在生产中干活的非工程 agent。

**深度阐述**

这是全场**信息密度最高、最颠覆认知**的一段。Alex 说他在 AIE 大会上分享这些数字时，人们"惊掉下巴"：

> "First milestone in the enterprise AI race is just rolling out a general purpose LLM to your people. Of the 100 enterprises we're talking to today, **90% have rolled out either Claude or Codex to their employees**."
> （企业 AI 竞赛的第一道里程碑，就是把通用 LLM 推广给你的员工。我们今天接触的约 100 家企业中，**90% 已经向员工部署了 Claude 或 Codex**。）
> `[关于企业采用率]`

第二道——培训赋能：

> "Actually teaching people how to use it, like training and enablement, which never gets the love that it should get but is arguably as important as the technology itself. I would say that's at like **60%**."
> （真正教人们怎么用——培训和赋能。这件事从没得到应有的重视，但它的重要性可能和技术本身一样。这个大概是 **60%**。）
> `[关于企业采用率]`

第三道——编码 agent，这里出现第一个反直觉数字：

> "I was asking a few people here, what percentage of enterprises do you think have rolled out coding agents to the engineering org? Most people were like it has to be 70 or 80%. **The number is closer to 50%.** Like every other enterprise we speak to either hasn't rolled out a coding agent, or what they are using is closer to not having a coding agent than having a coding agent."
> （我问了在场一些人：你认为多少企业把编码 agent 部署给了工程团队？大多数人觉得肯定有 70-80%。**实际数字接近 50%。** 我们每接触两家企业，就有一家要么没部署编码 agent，要么它用的东西**更接近'没有编码 agent'而非'有'**。）
> `[关于企业采用率]`

第四道——也是断崖所在：

> "The biggest diffusion gap is from raw intelligence to enterprise usage is agents in production for non-engineering work **drops to like 5%**... Most enterprises we talk to that have more than a thousand employees do not have an agent in production that is doing work that is not building software."
> （从原始智能到企业使用，最大的扩散鸿沟是"非工程工作的生产级 agent"——**掉到了大约 5%**……我们接触的大多数千人以上企业，都**没有一个在生产中干着非软件工作的 agent**。）
> `[关于企业采用率]`

**这四道里程碑构成了一条陡峭的衰减曲线：90% → 60% → 50% → 5%。** 最后一档的断崖（50% 跌到 5%）是整段的核心冲击。

Alex 给出了两个解释。第一，**这场浪潮由 FOMO 驱动**：

> "There's just this whole wave driven by a combination of some small group of people understanding what is possible... and a way larger group of people driven by FOMO. FOMO isn't bad. It creates forward momentum, but it also means people latch on to the things that are most in the zeitgeist."
> （整个浪潮由两部分驱动：一小群人真正理解这项技术的可能性，以及一大群人被 **FOMO** 驱动。FOMO 不是坏事，它制造前进动力，但它也意味着人们会抓住最时髦的东西。）
> `[关于企业采用率]`

第二，**"agent 之年"的承诺与现实的落差**：

> "People have been saying it's the year of the agent... every year is the year of the agent. Enterprises are like 'can you help build us an agent for some back office task'... it's why a lot of the work we're doing at 10x is deploying agents into production outside of engineering for repeatable work."
> （人们一直说这是"agent 之年"……每一年都是 agent 之年。企业说"你能不能帮我们为某个后台任务造个 agent"……这就是为什么我们在 Tenex 做的很多工作，是把 agent 部署到工程之外的生产环境中，处理可重复的工作。）
> `[关于企业采用率]`

主持人抓住核心矛盾：**"这不需要由那些整天在客户里打交道的人来告诉我们吗？"** Alex 确认：他们整天都在这些对话里，而现实就是——**大多数大企业根本没有生产级非工程 agent**。

**延伸思考**

这条 90→60→50→5 的曲线，是对"AI 已经无处不在"叙事的有力反驳。它区分了两个完全不同的概念：**"接入"（access）与"在生产中创造价值"（production value）**。前者的门槛很低（买个 license 就行），后者的门槛极高（流程、权限、评估、变更管理）。**"最后一公里"的生意之所以成立，正是因为这条曲线最后一段的断崖。**

**精华收获**
- 企业 AI 采用呈现"90-60-50-5"的断崖曲线，真正的价值创造集中在最难跨过的最后一档。
- "接入"不等于"落地"——从通用 LLM 到生产级非工程 agent，是一个数量级的跃迁。

---

## 十、权限治理与自建 Gateway：CIO/CISO 的噩梦 `[关于企业落地痛点]`

**核心观点**
当每个员工都用上 Claude 或 Codex，"数据权限"变成 CIO 和 CISO 的绝对噩梦——企业缺少一个简单的"数据权限控制面板"。Tenex 从为企业定制，走向产品化自己的 gateway 解决方案。

**深度阐述**

Alex 指出企业落地最普遍的痛点：

> "Permissioning and like RBAC. Basically as every employee in a company has Claude or Codex and they need access to certain data, it has turned into an absolute nightmare for CIOs and CISOs and they don't have a good gateway for easily doing almost like a control panel for data permissioning."
> （权限管理和 **RBAC**（基于角色的访问控制）。基本上，当公司里每个员工都有 Claude 或 Codex、都需要访问某些数据时，这变成了 CIO 和 CISO 的**绝对噩梦**，而且他们没有一个好的网关，来轻松实现一个几乎像**数据权限控制面板**的东西。）
> `[关于企业落地痛点]`

主持人用一句大白话翻译了这个问题："**字面意义上，就是'你能读什么、不能读什么'。**" Alex 确认"完全正确，这是个大问题"。

他随后解释了 Tenex 的应对路径——**从定制走向产品化**：

> "Basically we started by building bespoke for companies and now we actually productize that where we have our own gateway solution."
> （我们一开始是为企业**定制**，现在我们把它**产品化**了——我们有自己的 gateway 解决方案。）
> `[关于企业落地痛点]`

**这是一个值得注意的商业演进信号。** 一家"服务公司"（dev shop / 咨询）开始把内部能力沉淀为产品。它印证了后文 Alex 提到的"服务与软件正在收敛"（convergence of services and software）的判断——**当每个客户都要"一对一"体验时，纯软件公司被迫组建 FDE（前置部署工程师）团队，而纯服务公司则被迫产品化。**

**延伸思考**

权限治理看似枯燥，实则是 AI 落地的"隐形瓶颈"。它揭示了一个常被忽视的事实：**AI 的采用速度，往往不取决于模型能力，而取决于组织的"治理基础设施"。** 数据能不能安全地被 agent 读取、能不能被审计、能不能被撤销——这些"管道问题"决定了 agent 能否从"玩具"变成"生产系统"。

**精华收获**
- 数据权限治理是 CIO/CISO 的头号痛点，也是 agent 从实验走向生产的关键前提。
- Tenex 从定制到产品化 gateway 的路径，体现了"服务与软件收敛"的行业趋势。

---

## 十一、"你无法自动化一个不存在的流程" `[关于 agent 部署哲学]`

**核心观点**
Tenex 反复向客户强调的核心管理箴言：**你无法自动化一个不存在的流程。** 当 40 个人用 40 种方式做同一件事时，agent 无法知道什么是"对的"，也无法构建评估。因此正确的顺序是——先标准化流程，再把工作交给 agent。

**深度阐述**

Alex 把这句"被反复发现的痛点"总结成一句掷地有声的话：

> "I phrase it to the team as: **you can't automate a process that does not exist.** When you have 40 people that are all roughly doing the same function, but they're all doing it a little bit of a different way, there's actually — it's way harder to build an agent that's proactively doing that in the background."
> （我对团队的说法是：**你无法自动化一个不存在的流程。** 当你有 40 个人都在做大致相同的职能，但各自做法略有不同时——其实，要构建一个在后台主动干这活的 agent，要难得多。）
> `[关于 agent 部署哲学]`

他描述了正确的人机协作模式，并引出了"**agent 管理者**"这个角色：

> "You can totally sit down with them, give them the tools, walk them through how they could augment their own workflow. But when you really start to get the leverage is when you have these agents that are surfacing work to you, you're reviewing it, you're throwing it back, and you become more of this — everyone's been talking about becoming an **agent manager**."
> （你完全可以坐下来、给他们工具、带他们了解如何增强自己的工作流。但真正开始获得杠杆的时候，是这些 agent **把工作提交给你**，你审查、再扔回去——你变得更像是……大家都在说的**agent 管理者**。）
> `[关于 agent 部署哲学]`

然后给出了给企业的**行动顺序**：

> "Often times our recommendation to companies is: first we need to build a process around this organization within your company. And then here are the steps for us to actually hand off that work to an agent in the background. But if we don't have some form of **standardization**, it's going to be impossible for the agent to know whether it's doing it right, for us to build **evals** around this system, and actually deliver the value."
> （我们给企业的建议往往是：首先，我们需要在你们公司内部围绕这个职能**建立一个流程**。然后，这才是我们把工作**交给后台 agent** 的步骤。但如果我们没有某种形式的**标准化**，agent 就无从知道它做得对不对，我们也就无法围绕这个系统构建**评估（evals）**，无法真正交付价值。）
> `[关于 agent 部署哲学]`

这段话包含一个完整的方法论链条：**标准化 → 定义"对" → 构建 evals → 后台自动化。** 缺了第一步，后面全部塌方。

**延伸思考**

"你无法自动化一个不存在的流程"是对无数"agent 落地失败"案例的精准诊断。很多企业跳过标准化，直接要求"给我造个 agent"，结果 agent 面对的是混沌的、每个人做法都不同的现实，自然无法交付价值。**这提示我们：AI 落地最大的工作量不在模型，而在"把人的隐性流程显性化、标准化"。** 这与第五部分的 meta harness 是同一枚硬币的两面——对内，Tenex 自己把流程显性化；对外，它帮客户做同样的事。

**精华收获**
- 自动化的前提是标准化：先让 40 个人用同一种方式做事，agent 才可能接管。
- 正确的顺序是：标准化流程 → 定义"对" → 构建 evals → 后台 agent 自动化。

---

## 十二、对垂直 AI 的看空：当每个人都想要"一对一" `[关于垂直解决方案]`

**核心观点**
两位嘉宾对垂直 AI 解决方案（如 Harvey 之于律师、Open Evidence 之于医生）总体上持**看空**态度。理由有二：一是企业现实太复杂、惯性太大；二是"人人都想要一对一软件"的时代，纯垂直产品难以维持软件级利润率，且可能被前沿模型"吞掉"。但他们也承认"合理的人可以有分歧"。

**深度阐述**

Alex 主动抛出一个"也许有点辛辣"的观点——他们对垂直 AI 解决方案"总体上偏看空"：

> "Part of it is just from our vantage point of spending all day in the guts of enterprises. There is so much nuance and so much inertia and so many systems you have to wrangle and people you have to wrangle. And when a buyer of a vertical solution is expecting truly a one-of-one experience — we're in an age where people are expecting one-of-one software solutions."
> （一部分原因是，我们整天泡在企业的"内脏"里。那里有太多微妙之处、太多惯性、太多要驯服的系统和要说服的人。而当垂直解决方案的买家期待真正的**一对一体验**时——我们正处在一个人们期待一对一软件的时代。）
> `[关于垂直解决方案]`

他由此推导出一个关于**服务与软件收敛**的判断：

> "It's no wonder that every software company is basically building up a team of **FDEs** because there's just this convergence happening of services and software... How will they be able to do this at software margins if everyone expects a one-of-one solution? And also, why should we not expect frontier models to just gobble them up?"
> （难怪每家软件公司都在组建 **FDE（前置部署工程师）** 团队，因为服务与软件正在收敛……如果每个人都期待一对一解决方案，它们怎么可能以**软件的利润率**做到这一点？而且，我们凭什么不认为前沿模型会把它们**吞掉**？）
> `[关于垂直解决方案]`

**两个致命问题**：（1）一对一体验需要服务投入，但市场期待软件利润率——这是内在矛盾；（2）如果任务足够标准，前沿模型可以直接做，垂直产品凭什么存在？

主持人举例："Harvey 之于律师、Open Evidence 之于医生，这些是各自领域的经典赢家。而你**看空**它们。**到目前为止你错了。**"

Alex 给出了更平衡的回应，承认垂直玩家的**合理性**：

> "Access to data that ChatGPT is not going to have... obviously Anthropic and OpenAI are also acquiring those same data sources but they're just not as dedicated."
> （对 ChatGPT 拿不到的数据的访问权……显然 Anthropic 和 OpenAI 也在获取同样的数据源，但没那么**专注**。）
> `[关于垂直解决方案]`

主持人补上了关键论点——**专注带来"最后一公里"的优势**：

> "The pitch is focus... In a way that you care about the last mile for your customers, they care about their last mile in terms of the software. And as long as people train in that software, it never goes away."
> （卖点是**专注**……就像你关心你客户的最后一公里，他们关心他们软件的最后一公里。只要人们在那个软件里训练（形成习惯），它就永远不会消失。）
> `[关于垂直解决方案]`

主持人用 **Bloomberg 类比**说服 Alex：信息在 NASDAQ/NYSE 上人人都能拿到，但为什么交易员每年付 5 万美元用 Bloomberg？因为"所有同行都用它、一切为我整合、专为我定制"——Alex 承认"那是社交网络（DM 功能）"。这引出一个重要澄清：**垂直产品的护城河不只是数据，还有工作流整合与网络效应。**

最终两人达成一个更温和的共识：

> "Reasonable people can disagree how large each thing is... The total market's going to grow and all rising tide lifts all boats. Then you're just talking percentage of market share."
> （合理的人可以对每样东西有多大分歧……总市场会增长，水涨船高。然后就只是市场份额百分比的问题了。）
> `[关于垂直解决方案]`

**延伸思考**

这场辩论的核心张力是：**"专注"能否构成可持续的护城河，还是会被"通用模型的持续变强"侵蚀？** Bloomberg 的类比给出了部分答案——**当软件承载了"习惯 + 网络 + 工作流整合"时，它就超越了纯功能，形成黏性。** 但 CJ 的保留意见也很重要：如果一个垂直产品只是"把 agent 套在某个任务上"，没有战略性的数据/合规护城河，"那些会struggle"。区分点在于——**是"有 agent 的功能"，还是"有 agent 加工作流加习惯加网络"的系统。**

**精华收获**
- 垂直 AI 面临两难：一对一体验需要服务投入，但市场期待软件利润率。
- 护城河不在数据本身，而在"习惯 + 网络效应 + 工作流整合"（Bloomberg 模式）。

---

## 十三、Kill My SaaS：用 1,000 美元替换 40,000 美元的中端软件 `[关于 SaaS 颠覆]`

**核心观点**
主持人分享了自己的"Kill My SaaS"实验——花 1,000 美元替换一个年费 40,000 美元的中端 SaaS，即将投产。Alex 的回应区分了不同规模企业：**越往上走市场，"推倒重建"越难**；中端市场要看"机会大小是否值得投入工程资源"。

**深度阐述**

主持人（swyx）分享了他刚发布的实验：

> "I just released my results for my Kill My SaaS competition where we replace a mid-tier SaaS... We were quoted $40,000 a year. We spent $1,000 to replace it. It's going to production next for the next conference. We are that customer that says I want the one-on-one tool and I'm expecting all these things... Tell me where it's going wrong."
> （我刚发布了我"Kill My SaaS"竞赛的结果，我们替换了一个中端 SaaS……对方报价每年 **40,000 美元，我们花了 1,000 美元**就替换了。它下个月就要为一个会议投产……我们就是那种说"我要一对一工具、我期待所有这些"的客户……告诉我哪里会出问题。）
> `[关于 SaaS 颠覆]`

Alex 给出一个**分层判断**——越往高端市场，替换越难：

> "The more you move up market in business, the harder the proposition of ripping out and building from scratch gets. Part of the reason people have said Salesforce is really at risk, SAP is really at risk — I don't agree with that at all. Those businesses in my mind just accrue value in this moment in time... There's so much money at stake where if a company gets it wrong ripping them out, you're talking about potentially hundreds of millions or billions of dollars. You're going to be risk-averse."
> （在商业中越往高端市场走，"推倒重建"的命题就越难。有人说 Salesforce 很危险、SAP 很危险——我完全不同意。在我看来，这些生意在当下这个时刻只是在**累积价值**……因为牵扯的钱太多了，如果一家公司搞砸了替换，可能是数亿到数十亿美元的代价。你会**规避风险**。）
> `[关于 SaaS 颠覆]`

对中端市场，他提出一个务实的决策框架：

> "It really comes down to what is the size of the opportunity... Is that ever going to be the worthiest opportunity to rebuild inside of a company?... From a percentage of revenue or cost perspective, is that going to ever move the needle enough to allocate engineer resource? It's going to be case by case."
> （这真的取决于**机会有多大**……那会不会是公司内部值得重建的机会？……从营收或成本的百分比看，它是否足以值得分配工程资源？这要**具体案例具体分析**。）
> `[关于 SaaS 颠覆]`

Alex 透露 Tenex 自己也走这条路——**"我们从头建了自己的 CRM、自己的操作系统（OS）"**。CJ 补充了一个关键的**成本论**：自建软件真正的代价不是功能，而是**持续维护的心智负担**：

> "One thing every company realizes is one of the beauties of software is not just the utility you get from it, it is all of the **headaches you don't have to think about** in maintaining it and improving it when it's not in your core... Is the size of the prize big enough to justify the **cognitive load** that is going to take from some amount of resource in your company to nurture something that is not core to your business?"
> （每家公司都意识到的一件事是：软件的美妙之处不仅在于你获得的效用，还在于当它不是你的核心业务时，你**不必去想**的那些维护和改进的**头疼事**……奖品是否大到足以证明那份**心智负担**是值得的——用公司的一部分资源去养护一个非核心的东西？）
> `[关于 SaaS 颠覆]`

主持人强调，他的实验不只是省钱，还有"**进攻**"（offense）维度：

> "It is not just about costs. It's that... our experience could be a lot better for literally every party concerned... The product has been mediocre for a long period of time. What would the 10x better version of this product look like?"
> （不只是成本问题……我们的体验可以对每一个相关方都好得多……这个产品长期以来一直**平庸**。它好 10 倍的版本会是什么样？）
> `[关于 SaaS 颠覆]`

Alex 补充了**规模差异**：初创和高增长中型公司可以这样灵活，但"**大企业很少会这样做**"——它们太根植于某个能力，很少会说"我们能造个 10 倍好的版本并把它独立出来"。**这再次划出了"谁能颠覆 SaaS"的能力边界。**

**延伸思考**

"Kill My SaaS"实验与 Alex 的"越往上越难替换"形成了完整图景：**AI 让"重建"的技术成本骤降（40k → 1k），但"替换"的组织成本依然高昂（风险、心智负担、非核心维护）。** 这意味着 SaaS 的"死亡"不会均匀发生——**它更可能发生在中端、非核心、体验平庸、且买家足够灵活的场景**，而核心系统（Salesforce/SAP）反而会因"风险规避"而更稳固。

**精华收获**
- AI 大幅降低了"重建"的技术成本，但"替换"的组织成本（风险 + 心智负担）依然决定成败。
- 越往高端市场，SaaS 越安全；颠覆更可能发生在中端、非核心、体验平庸的领域。

---

## 十四、就业替代与人的能动性：拒绝把 AI 说成"发生在人身上的事" `[关于就业影响]`

**核心观点**
两位嘉宾拒绝把"就业替代"描述成"发生在人身上的事"（happening to people）。CJ 强调"再分配"（reallocation）——企业总有下一个问题要解决；Alex 则更尖锐：**人们对自己的生活有能动性（agency）**，把"AI 会取代人们不喜欢的工作"当作安慰，是一种"cope"（自我安慰）。

**深度阐述**

主持人把话题引向更辛辣的领域——"**它们是不是在自动化人类？**" CJ 先给出一个**乐观但清醒**的立场：

> "I really deeply believe that AI will produce good for humanity, it's going to augment people's jobs, it will absolutely change, displace... but I think it's more of a movement as opposed to just cutting off work."
> （我深深相信 AI 会为人类带来好处，它会增强人们的工作，它绝对会改变、会替代……但我认为这更像是一场**迁移**，而不只是"砍掉工作"。）
> `[关于就业影响]`

他举了 a16z 的数据——**呼叫中心正在衰退，AI 接手越来越多**，然后给出了极富同理心的表述：

> "If that is a skill you've built up your whole career, that is **devastating** to have something come in and take that function over."
> （如果那是你整个职业生涯积累的技能，有东西进来接管那个职能，那是**毁灭性的**。）
> `[关于就业影响]`

然后他转向 Tenex 的实践——**"再分配"（reallocation）**：

> "Part of what we do when we're talking to customers about 'an agent is now going to do this work' is actually around reallocation. I don't think any business would claim once we have this solved, there's nothing for this group of people to work on... There's always the next problem. **Infinite demand.**"
> （当我们和客户谈"一个 agent 现在要做这活"时，一部分工作其实是关于**再分配**。我不认为哪家企业会说"一旦这事解决了，这群人就没活干了"……总有下一个问题。**无限的需求。**）
> `[关于就业影响]`

他描绘了被解放的人可以做什么——**从"表格里的一个单元格"上升到"团队如何协作、钱如何分配"的战略层面**：

> "Taking those people that may have this super deep subject matter expertise and bringing them above water to work more across teams... how these teams are working together... elevate them to think strategically about the business and where money is allocated."
> （把那些有超深领域专长的人**从水下托举出来**，让他们跨团队工作……思考团队如何协作……把他们提升到战略性思考业务、思考钱如何分配的高度。）
> `[关于就业影响]`

**Alex 的回应则更尖锐、更具争议性**，也是整场对谈最有"锋芒"的一段：

> "When we have these conversations around job displacement or reallocation, we talk about it as this thing happening **to** people. One of the reasons I don't like that is it doesn't give enough credit to people to have **agency in their own lives**."
> （当我们讨论岗位替代或再分配时，我们把它说成是**发生在人身上**的事。我不喜欢这样，一个原因是：它没有充分认可人们对自己生活拥有**能动性**。）
> `[关于就业影响]`

他进一步挑战了那句流行的安慰：

> "When people say that AI is going to replace all the work that people don't enjoy doing, I think that's a little bit of like **cope** for the reality — just people are going to be put out of jobs, because a lot of people don't have the luxury of liking or not liking a job. They do a job to make money."
> （当人们说 AI 会取代所有人们不喜欢做的工作时，我认为那有点像对现实的**自我安慰**——现实就是有人会失业，因为很多人没有"喜欢或不喜欢一份工作"的奢侈。他们工作是为了赚钱。）
> `[关于就业影响]`

他的建议是**主动的**：

> "People, to the extent that it's possible, should have agency in saying to themselves: okay, what is the stability or replaceability of my job over the next few years? And if I am to try to skill up in a way that I'm better protected, what does that look like?"
> （在可能的情况下，人们应该对自己有能动性：好吧，未来几年我的工作的稳定性或可替代性如何？如果我要以某种方式提升技能、让自己更有保护，那是什么样？）
> `[关于就业影响]`

**个人感受**

Alex 这段话带有罕见的、不讨好的诚实。在一个普遍用"AI 会增强人类、解放你去追求热爱"来安抚听众的时代，他直接把它称为"cope"，并强调"很多人没有选择的奢侈"。这种不加修饰的直率，正是整场对谈"给成年人做节目"气质的体现。**它不温柔，但它尊重听众的判断力。**

**延伸思考**

"再分配"（CJ）与"能动性"（Alex）是两种互补的叙事：前者是**组织层面**的责任（企业应为被替代者找到新价值），后者是**个人层面**的责任（个人应主动评估并升级自己的可替代性）。两者缺一不可——**只谈组织责任会让人被动等待，只谈个人能动性会显得冷酷无情。** 这场对话同时给出了两者，是难得的平衡。

**精华收获**
- "再分配"是企业的责任：被替代的人应被"托举"到更高价值的工作上，因为"需求是无限的"。
- "能动性"是个人的责任：不要把"AI 会取代你不喜欢的工作"当作安慰，要主动评估自己的可替代性并升级技能。

---

## 十五、纽约 vs. 旧金山：一个"更小的气泡"与商业价值的"更大的池塘" `[关于纽约 AI 生态]`

**核心观点**
主持人问纽约的 AI 氛围。Alex 的回应是：**纽约有一个 AI 气泡，但比旧金山的小**；旧金山的 AI 是"无所不在、全 encompass 的"。但纽约在**商业价值**上是"同样大甚至更大的池塘"——这里有海量商业，是技术扩散真正影响 GDP 的地方。

**深度阐述**

主持人说自己在旧金山生活，"所有人整天泡在 agent 里，讨论的是 instinct 还是 grok 还是 muse，而不是'你喜不喜欢 AI'"。他想"跳出气泡"。Alex 的回应分两层。

**第一层——承认气泡更小**：

> "There's a bubble in New York that is a smaller bubble than exists in SF. If SF is like a big bubble... We at Tenex feel like we are in a microcosm of San Francisco because of the people that self-select to work at the company and the companies we're partnered with. But it is true that it is a smaller universe than in SF."
> （纽约有一个气泡，比旧金山的气泡小。如果旧金山是个大气泡……我们在 Tenex 感觉像处在一个**旧金山的缩影**里，因为自我选择来公司工作的人、以及我们合作的公司。但确实，这是一个比旧金山更小的宇宙。）
> `[关于纽约 AI 生态]`

他对比了旧金山的"**未来感**"：

> "When you go to SF it feels all-encompassing, where everyone everywhere you look is someone similar... AIE is like that on steroids. I feel like SF is similar to AIE. The overlap of AIE generally and people who have lived at some point in their life in SF is probably a very large overlap."
> （去旧金山会感觉无所不在……AIE 就像它的加强版。我觉得旧金山和 AIE 很像。AIE 的与会者和曾在旧金山生活过的人，重叠度大概非常高。）
> `[关于纽约 AI 生态]`

**第二层——强调纽约在商业上的分量**：

> "It is in the culture and DNA of SF where a very big population of people live in the future. I think you can find that group in New York and we at Tenex have found that... Part of our goal is to drive AI as a hub — New York as a hub for AI in the US — because there is so much commerce here that it is going to be a place where diffusion of the technology actually has such a meaningful impact on the GDP of this country. We take it almost as a charge of ours to increase our bubble."
> （"活在未来"是旧金山的文化和 DNA。我认为你在纽约也能找到那群人，我们在 Tenex 找到了……我们的部分目标是把纽约打造成美国 AI 的一个**枢纽**，因为这里有**如此多的商业**，技术扩散将在这里对这个国家的 GDP 产生真正有意义的影响。我们几乎把它当作自己的使命——**扩大我们的气泡**。）
> `[关于纽约 AI 生态]`

主持人注意到一个文化细节——**AI 广告牌正"悄悄爬进"纽约街头**：

> "There was the friend campaign where people would spray graffiti... a little bit of intentional rage bait, but now you have the **unironic AI billboards** and people are like 'I guess that's part of life now.'"
> （曾经有 friend 广告牌运动，人们会喷各种涂鸦……有点刻意的"愤怒钓鱼"，但现在你有了**不再反讽的 AI 广告牌**，人们会说"我猜这就是生活的一部分了"。）
> `[关于纽约 AI 生态]`

Alex 做了一个精彩的**仲裁总结**：

> "We're in a smaller pond for AI, but I would argue we're in as big of a pond, if not a bigger pond, for **commercial value**."
> （在 AI 上我们是个更小的池塘，但我会说，在**商业价值**上，我们处在同样大、甚至更大的池塘里。）
> `[关于纽约 AI 生态]`

主持人的收尾金句把两人的观点拧在一起：

> "The reason I do AI in New York is I bring all the people from San Francisco to come here and meet their customers, and also get a reality check. I actually think there's a really interesting **arbitrage** there."
> （我在纽约做 AI 的原因是：我把旧金山的人都带到这里来见他们的客户，也**接接地气**。我真的觉得这里有个非常有趣的**套利**机会。）
> `[关于纽约 AI 生态]`

**延伸思考**

"旧金山是未来，纽约是商业"——这个对比揭示了 AI 产业的一种**地理分工**：前沿研发与思想集中在西海岸（气泡大、未来感强），而价值落地与客户扩散在东海岸（商业密度高、现实感强）。主持人的"套利"洞察极为精准：**把旧金山的前沿能力带到纽约的商业现实面前，中间的价差就是机会。** 这也正是 Tenex 的定位——它做的"最后一公里"，本质上就是一种地理与认知的套利。

**精华收获**
- 旧金山是"活在未来"的大气泡，纽约是"更小的 AI 气泡"但"更大的商业池塘"。
- 两地之间存在"套利"：把前沿能力带到商业现实，就是价值创造的来源。

---

## 十六、招聘与收尾：部署工程师、AI 策略师，与"无限的问题" `[对话收尾 / 招聘信息]`

**核心观点**
Tenex 持续招聘，重点是**部署工程师**（deployed engineers）和**AI 策略师**（技术顾问）；CJ 尤其寻找工程师，围绕"元框架"和内部平台做特殊项目。整场对话以"总有下一个问题"的信念收尾。

**深度阐述**

主持人惯例性地问招聘。Alex：

> "We're hiring for **deployed engineers** at Tenex. Just go to **10x.co**. We're also always hiring **AI strategists**, which are basically technical consultants who are leading client engagements. The team is **75 strong in New York City**. We're continuing to make New York City our home."
> （我们在 Tenex 招聘**部署工程师**，去 **10x.co**。我们也一直招聘 **AI 策略师**——基本上是领导客户合作的技术顾问。团队在纽约有 **75 人**。我们继续把纽约当作自己的家。）
> `[对话收尾]`

他对企业客户喊话：

> "If you are an enterprise looking to actually get AI native and you've tried it, it's not working, hit us up. I promise we'll do better work than — not going to name them — but a lot of other traditional consultancies. **Spicy.**"
> （如果你是想要真正"AI 原生"、试过但没成功的企业，联系我们。我保证我们做得比——不点名了——很多其他传统咨询公司更好。**够辣。**）
> `[对话收尾]`

CJ 补充并解释了"**特殊项目**"是什么——这是全场最能揭示他工作本质的一段：

> "I'm particularly looking for engineers... A special project involves anything outside of our client work. My brain right now is building that **meta harness** and system internally — find the **bleeding edge** of what the models can do and give them tools to augment how well they can do it. And also internally working on the **platform** that Alex mentioned. Big goal there: diffuse these **background agents** and actually get them out to enterprises in a way that's truly helpful."
> （我尤其寻找工程师……**特殊项目**涉及客户工作之外的一切。我现在脑子里装的是：在内部构建那个 **meta harness** 和系统——找到模型能力的**最前沿**，给它们工具来增强它们做得有多好。同时也做 Alex 提到的那个**平台**。大目标：把这些**后台 agent** 扩散出去，真正以有帮助的方式交付给企业。）
> `[对话收尾]`

**这构成了一个完整的闭环**：对内，CJ 建 meta harness（第五部分）；对外，Tenex 把 background agents 扩散给企业（第九、十、十一部分）。**"找到最前沿 → 工具增强 → 标准化流程 → 部署到企业"——这就是 Tenex 的全部工作。**

主持人以邀请投稿收尾：

> "We take guest posts on the Latent Space blog. I'd love to welcome some sharing of knowledge."
> （我们在 Latent Space 博客接受客座投稿。欢迎分享知识。）
> `[对话收尾]`

**精华收获**
- Tenex 的招聘重点：部署工程师 + AI 策略师，全部围绕"把 AI 落地企业"。
- 特殊项目 = 内部 meta harness + 对外 background agent 平台，构成"前沿探索 → 工具增强 → 企业扩散"的闭环。

---

## 总结：这场对话真正告诉了我们什么

**关于 AI 工程组织**：Tenex 的实践证明，当模型能完成 90% 代码时，工程师的价值从"写代码"转移到"获取上下文、编排 agent、管理流程"。薪酬制度必须随之演化——按产出付费可行，但 4 倍（而非 10 倍）的方差才是现实，且"不写代码的时间如何付酬"是永恒的难题。

**关于企业 AI 落地**：最有冲击力的数据是那条 90-60-50-5 的曲线。**"接入"是廉价的，"落地"是昂贵的。** 真正的瓶颈不在模型，而在流程标准化、权限治理、评估构建——也就是"最后一公里"。

**关于个人**：CJ 的故事（产出变好、收入反降）和 Alex 的立场（人们对自己的可替代性有能动性）共同指向一个结论：**在 AI 时代，效率提升必须配合契约重构，否则效率会反噬生产者自己；而个人必须主动评估并升级自己的不可替代性。**

**关于地理与机会**：旧金山是未来，纽约是商业，两地之间的"套利"——把前沿能力带到商业现实——就是价值创造的空间。

**一句话收束**：Alex 那句"你无法自动化一个不存在的流程"，可能是整场对话最可迁移的洞察。它适用于任何想用 AI 改造业务的人——**在自动化之前，先让流程存在。**

<!-- TLDR: AI 是原始智能，最难的是把它扩散进企业的"最后一公里"。 -->
<!-- TAGS: AI原生工程, 按产出付薪, 企业AI落地, Agent部署, 工程组织 -->
<!-- RATING: 4 -->
