---
title: "How the most AI-pilled product team builds products | Fiona Fung (Claude Code and Cowork)"
channel: "Lenny's Podcast"
published: "2026-06-21"
source_url: "https://www.youtube.com/watch?v=Ybrl4FYM57c"
video_id: "Ybrl4FYM57c"
tags: ["AI", "工程管理", "产品思维", "Anthropic", "个人成长", "组织文化", "编程未来"]
rating: 5
language: "英文"
word_count: 9968
duration: "1:38:45"
---

# How the most AI-pilled product team builds products | Fiona Fung (Claude Code and Cowork)

- **Channel:** Lenny's Podcast
- **Published:** 2026-06-21
- **Source:** https://www.youtube.com/watch?v=Ybrl4FYM57c
- **TL;DR:** 编码非瓶颈，想象力与验证成新核心。Anthropic高管亲述AI原生团队构建与工程文化重塑法则。
- **Tags:** AI, 工程管理, 产品思维, Anthropic, 个人成长, 组织文化, 编程未来
- **Rating:** 5

## 版本

- [结构化文稿](2026-06-21-how-the-most-ai-pilled-product-team-builds-products-fiona-fung-(claude-code-and-cowork)-Ybrl4FYM57c.structured.md)
- [原始文稿](2026-06-21-how-the-most-ai-pilled-product-team-builds-products-fiona-fung-(claude-code-and-cowork)-Ybrl4FYM57c.transcript.md)

深度重构：Anthropic精英团队如何玩转AI时代的产品开发

---

## 材料信息

- **标题**：How the most AI-pilled product team builds products | Fiona Fung (Claude Code and Cowork)
- **作者/来源**：Lenny's Podcast（Lenny Rachitsky 采访 Fiona Fung）
- **类型**：深度访谈（YouTube 视频字幕/Podcast 文本）
- **关键元数据**：
  - 嘉宾：Fiona Fung，Anthropic 工程副总裁，负责 Claude Code 和 Co-work 团队
  - 职业履历：IBM（DB2）→ 微软（Visual Studio / TypeScript）→ Meta/Facebook（Marketplace、智能眼镜、AR眼镜Orion）→ Instagram（基础设施、增长、安全）→ Anthropic
  - 核心数据：团队工程师每季度代码产出是2025年的8倍
  - 采访话题：AI原生团队的组织架构、招聘标准、管理方法、工程文化及小企业AI普惠

---

## 开篇引入

2025年的某一天，Fiona Fung在Lenny's Podcast上扔出了一枚信息炸弹：她负责的Claude Code和Co-work团队，工程师每季度产出的代码量，是2025年的**整整8倍**。更令人震撼的不是这个数字本身，而是她谈到这一切时极度自然的语气——仿佛这只是这家全球最“AI-pilled”公司的日常标配。

Fiona身上有一种非常罕见的折叠感：她经历了IBM的大型机时代，用Vim写OS；她亲历了微软IDE的革命，在Visual Studio团队用编辑器去构建编辑器本身；她踏准了消费互联网的大爆发，在Facebook从零到一打造了年GMV超千亿美元的电商业务Marketplace；她还深度参与了Meta第一代智能眼镜和AR眼镜“Orion”的硬件探索。而现在，她正是全球最受关注的AI原生生产力工具Claude Code与Co-work的掌舵者。

这意味着，她的一只脚踩在软件工程最深厚的传统里，另一只脚已经踏入了未来。她带来的不是关于AI的模糊畅想，而是一份**已经在这家地表最激进AI公司里充分验证过的、关于“如何构建产品”和““如何引领团队”的完整操作系统。**

这篇文章将带你完整还原这次对话，深入解析当“编码不再是瓶颈”后，一个顶级AI产品团队的组织基因、招聘准则、管理方法以及跨越技术鸿沟的责任感。

---

## 详细内容

### 1. 瓶颈的转移：当编码被“解决”，什么成为了新核心？

`[开场/新瓶颈]`

**核心观点**：在Anthropic，编码（Coding）不再是工程中的稀缺环节。新的瓶颈已经转移到了“验证”（Verification）和“想象力”（Ambition）。工程师的核心技能包正在被彻底重写。

**深度阐述**

整个对话的起点，是一个语义极其强烈的论断。Fiona引用团队内部数据直言：“**Anthropic engineers on average have eight times as much code per quarter as they did compared to 2025. Coding is no longer the bottleneck.**”（Anthropic工程师平均每季度产出的代码量，是2025年的8倍。编码不再是瓶颈。）`[开场/核心数据]`

这个数字具有震碎一切旧框架的力量。过去几十年的软件工程管理——从需求估算、甘特图、到敏捷开发的站会——其底层逻辑全都建立在“一位优秀工程师的时间极其昂贵且有限”这一铁律之上。当这个前提崩塌时，旧的管理大厦也必须推倒重建。

Fiona清晰地指出，新的瓶颈有两个：

1.  **验证（Verification）**：当代码量呈指数级增长，质量控制的逻辑必须改变。如果人类工程师一天只能仔细审查几段代码，现在面对8倍于往日的流量，怎么办？
    -   **Fiona的解法**：把“**好的标准**”和“**检查框架（Framework）**”直接写进代码仓库。她举了一个例子：最近团队更新了内容设计（Content Design）的样式指南（Style Guide）。她强调：如果你的代码库里有清晰定义的“What Good Looks Like”（什么是好的）标准，Claude Code Review就能自动进行验证，确保输出与标准匹配。`[管理/代码审查]`
    -   **TDD的进化**：被无数人提倡却执行艰难的**测试驱动开发（TDD）**，在新的AI范式下迎来了重生。Fiona分享了她在Claude Code上修复第一个Bug时的经历。她直接让Claude先写一个会失败的测试，然后再去修复代码，直到测试通过。她笑着说：“过去我要自己写测试，感觉像‘必须先吃西兰花’。现在AI帮我先写好，我只管享受‘构建’的大餐。” `[管理/TDD演进]`

2.  **想象力与雄心（Ambition）**：
    Fiona引用团队中另一位非移动端工程师的故事，他用自己的语言表达了这种震撼：“以前，当听到一个跨平台功能时，我的第一反应是‘这太困难了，技术栈太复杂，做不了’。但现在，我的第一反应变成了‘太好了，我们来实现它！’”
    她对此的总结非常精辟：“**It‘s lifted the ceiling of what anyone is able to do. Everything is now possible in theory. Now it’s about how ambitious can you be？**”（它抬升了每个人能力的上限。理论上，一切皆有可能。现在的问题是你有多大的雄心？）`[团队DNA/雄心]`

**延伸思考：从“可行”到“值得”**

当“写代码”这个最大的执行障碍被移除，工程师工作的天平开始剧烈地向另一端倾斜。未来顶尖工程师的核心竞争力，不再是“阅读晦涩文档并写出精妙的算法”，而是**“提出一个值得构建的假设”、“定义什么是好的结果框架”，以及“对海量输出做出精准的判断和迭代”**。

---

### 2. 团队DNA：新物种的样子——“梦想家”与“深水专家”

`[团队DNA/招聘]`

**核心观点**：在新的生产力环境下，理想的团队由两类人构成：具有强烈产品直觉的创造性建设者（Creative Builders / Dreamers）和掌握核心原理的深度系统专家（Deep Systems Experts）。但驱动所有人的底层特质是“高能动性”（High Agency）。

**深度阐述**

Fiona明确提出了招聘的进化方向，她称之为“标准答案”：

> “The two profiles that I now look for are **creative builders with product sense** and **deep systems experts for the hard parts**.”（我招聘时只看两种人：有产品感的创造性建设者，以及解决核心难题的深度系统专家。）`[招聘]`

-   **类型一：创造性建设者（Creative Builders）**
    -   他们的核心是“**梦想家（Dreamers）**”。
    -   他们极度热爱产品，拥有极强的想法，并且有能力快速将其构建出来。
    -   他们的节奏是：产生想法 -> 快速构建 -> 观察反馈 -> 快速迭代 -> 打磨体验。
    -   他们端到端地拥有这个产品（Owning the product end-to-end）。
    -   在Fiona的框架里，这类人拥有无限的“Freedom to Cook”（自由去烹饪）。

-   **类型二：深度系统专家（Deep Systems Experts）**
    -   AI并非万能，在涉及核心系统、安全性、大规模分布式架构等需要大量人类经验做“Trust but Verify”（信任但验证）的领域，顶尖专家的深度推理是不可替代的。
    -   Fiona提到，当她刚加入Claude Code团队时，发现团队有很多优秀的产品通才（Product Generalists），但缺少拥有系统背景（Distributed Systems Expertise）的人。找到他们，团队的能力拼图才算完整。

**文化底色：高能动性与高问责**

Fiona在谈话中反复提及的一个词是“**Agency**”（主观能动性/主人翁意识）。她在回答Lenny关于“为何有些人如鱼得水，有些人痛苦挣扎”时，给了一个极富洞察力的答案：

> “The people that seem to be doing best are taking the most initiative, getting the most proactive, have the most agency.”（那些做得最好的人，都在主动揽活、极度主动、拥有最强的能动性。）`[团队文化]`

但是，她马上补充了这个概念的另一半：
> “We say with high agency also **high accountability**. So it‘s all about making sure folks have that freedom to cook. But then it’s also like, ‘What is the hypothesis of what you‘re trying to solve？’”（我们说，高能动性必须匹配高问责。所以关键在于确保大家有“烹饪”的自由，但同时也要问：你想解决什么的假设是什么？）`[团队文化]`

这个平衡极难把握，但也极其精妙。团队给你极大的自由去“烹饪”，但这道菜是否对味、是否解决了目标客群的饥饿感，也是你必须承担的责任。

**个人感受：跨越恐惧与那个银行出纳员的故事**

面对那些因为害怕掉队而“超级沮丧、抗拒”的同事，Fiona展现了惊人的共情与实用主义哲学。她说，很多沮丧的根源是恐惧。

> “For anything that there is a fear, my advice is：lean in and ask, what can I do about it？ What is within my control？”（对于任何让你恐惧的事，我的建议是：向前靠，问问自己，我能做什么？什么在我掌控之内？）`[恐惧与能动性]`

她分享了一段非常私人的经历来阐释这一点。她从小想学计算机，但家里没钱，对工程学院的昂贵学费充满恐惧。“到处都是未知。”当时加拿大国家银行恰好在她高中贴了一张招聘出纳员的传单。尽管那是她最讨厌的会计课相关的工作，但这就是“她可控的一小步”。她申请了，整个暑假和每周末去上班。这份工作成了她支付全部学费的“生命线”。

她说：“如果你感到恐惧和无力，找到一件你可控的事情去做。别让它定义你，而要问问自己：这件事是‘发生在我身上（happening to me）’，还是‘为我而发生（happening for me）’？”

---

### 3. 极简与自动化：AI原生管理者的工具箱

`[管理/全景洞察]` `[管理/Routines]`

**核心观点**：管理者是AI时代最大的受益者，也是最需要进化的角色。Fiona使用了一套完全不同的管理工具——全景AI工作区、夜间异步Agent、和极致精简的流程。

**深度阐述**

Lenny问了一个很实际的问题：当每个人的产出提升了8倍，你怎么保持对工作和质量的全盘把控？Fiona的答案极具启发性。

**工具一：全景Claude工作区（The Remote Session）**

她做了一个很多人没想到的事情。她启动了一个连接到团队所有代码仓库、Slack频道、监测数据的**持续Claude Code会话**。这成了她的“第二脑”。

> “I actually have a Claude Code remote session that I enlist in all of our repos... I‘ll have access to like how are the metrics of everything we track. And so every month, we’ll take a look back together... It‘s about, hey, what were the focus areas？ What were the products that got shipped？ How did it do？”（我有一个连接到所有Repo的Claude Code远程会话，我能看到所有追踪的指标。每个月我们会一起回顾……看重点是什么？发了什么产品？效果如何？）`[管理/全景洞察]`

这让她从阅读“这季度我发了10个PR”的静态清单，升级为动态审视“这里出现了Bug模式？那里有用户反馈的潜在机会？”的高级思考者。

**工具二：Routines——从同步Prompt到异步Agent**

这是Fiona认为的“下一件大事”。她分享了自己的晨间流程：
-   **过去**：早上喝咖啡，手动翻看所有反馈渠道（邮件、Twitter、Slack），记笔记，分配任务。
-   **现在**：她设置了一个“Routine”（可以理解为高级Cron Job + Agent组合）。这个Routine每天早上自动运行，去抓取反馈、分析主题、甚至直接生成修复PR。她醒来后，直接看AI生成的摘要和等待Review的PR。

> “It’s almost like I'm having an agent help me generate the prompts and the PRs... It‘s a higher level of abstraction... It’s asynchronous style of working.”（这就像是有一个Agent在帮我生成Prompt和PR……这是更高层次的抽象……这是异步的工作方式。）`[管理/Routines]`

**工具三：JIT规划（Just-in-Time Planning）与杀死猪流程**

Fiona 对自己早期加入Claude Code时试图推行“6个月路线图”的行为进行了公开反思。

> “The exercise was good to kick start conversations and ensure everyone‘s aligned. But three months in, I was like, wait, have we still referenced this？ Because so much has changed.”（这个练习对启动对话和确保对齐很好。但三个月后，我问，我们还在参考这个吗？因为变化太多了。）`[管理/JIT规划]`

现在的她是**JIT规划**（即时规划）的铁杆信徒：
-   **周期**：月度规划，极度轻量，甚至没有复杂的文档，只是一个电子表格，列出本月的最高优先事项。
-   **校准**：每周花非常短的时间确认：“这些是否仍是本月的优先事项？”
-   **核心理念**：Fiona提出了一条非常适用于今天的管理座右铭：“**Explicit permission to kill processes that no longer serve us.**”（我们拥有明确的许可，去杀死那些不再服务于我们的流程。）`[管理/杀死流程]`

**文化暗线：“狗叼咖啡杯”的管理者噩梦**

Fiona非常担心一种管理者形象：当你问他怎么样时，他强撑着说“一切都好”，但其实房子里已经着火了，他嘴角还挂着微笑，像极了那个“狗喝咖啡”的meme。她鼓励团队，尤其是管理者，要公开谈论“什么不顺利”（What‘s not going well）。因为只有暴露问题，才能一起解决问题。

---

### 4. 跨越鸿沟：技术领袖的责任感

`[小企业与普惠]`

**核心观点**：Fiona是对话中最鲜明的“技术普惠”倡导者之一。她把自己对小企业的热爱和帮助普通人跨越AI鸿沟，视为个人激情所在和一项重大责任。

**深度阐述**

这一部分极具情感张力。Fiona谈到了她的成长经历：她是香港移民，祖母为了照顾她来到加拿大，但不会英语，在新环境里非常孤立。后来她们找到了一家由会说粤语的女士开的毛线店。这家小店变成了祖母的社交圈（Knitting Circle）。

> “This little small business created this wonderful sense of community... That's probably where my love came from.”（这家小小的作坊创造了一种美好的社群感……这大概就是我爱意的来源。）`[小企业/情感来源]`

所以当Co-work出来后，看到它可以自动处理“商业旅行报销”这种她自己也讨厌的杂事时，她立刻想到了那些“坐在酒吧里面对着一堆收据和发票拼命算账”的小企业主朋友。她主动去帮助他们。

她讲了一个极其生动的例子。一位经营两家餐厅的朋友，把Co-work连到自己的文件夹里，想找一份丢失的菜单。Co-work不仅找到了菜单，这位朋友还进一步问：“看看我这个菜系和物价，相对于本地市场是否合理？”Claude立刻给出了一份市场分析，甚至提到了她曾去过的一家类似风格的餐厅。这不是一个“提示工程师”的高端访谈，这是AI“擦亮蒙尘的玻璃”、让普通人获得巨大赋能的真实写照。

**如何跨越鸿沟？**

Lenny问到了一个关键问题：技术圈外的人（你的祖父母、开餐厅的朋友、日常白领）要么没时间，要么就是讨厌AI，你怎么帮他们？

Fiona的建议非常务实：

> “Find something that has made a meaningful life change for you with the AI tools... And then see if that is a conversation starter... I would love for everyone‘s help to make sure we keep sharing the knowledge, because if not, the divide grows larger and larger.”（找到一个AI工具真正改变了你生活质量的例子，然后把它作为对话的起点……我希望每个人都来帮忙分享这份知识，因为如果不这样做，鸿沟会越来越大。）`[结尾/行动呼吁]`

她不是在呼吁复杂的公益项目，而是在呼吁一种“传火”的行为。如果你是完全“AI-pilled”的从业者，请弯下腰，握住身边人的手，用一个“生命体验被改善”的瞬间，点燃他们对技术的好奇心。

---

### 5. 轻盈的哲学：小王子、娜乌西卡与保持善良

`[个人哲学/灵感]`

**核心观点**：在极致的技术理解和严肃的管理哲学背后，Fiona的精神世界由一些跨越时空的美好事物支撑。它们定义了什么是她眼中“真正重要的东西”。

**深度阐述**

-   **反复推荐的书籍**：《小王子》（The Little Prince）
    -   理由：“我每年至少重读一次。它提醒我什么是真正重要的。”（To remind me to think about what‘s truly important.）她同时也推荐玛格丽特·阿特伍德（常读的加拿大作家，思辨小说）和村上春树（钟爱的魔幻现实主义）。

-   **手机里常驻的三部电影**：
    1.  **《天使爱美丽》（Amelie）**：年轻时去巴黎旅行的美好回忆，这部电影捕捉了巴黎的魔力。
    2.  **《千与千寻》（Spirited Away）**：最爱之一。
    3.  **《风之谷》（Nausicaä of the Valley of the Wind）**：这是最打动人的一个答案。Fiona说，她九岁时看了这部动画。女主角娜乌西卡（Nausicaä）——这位从漫画中走出的“女版施瓦辛格”式领导者——那种**充满韧性、同理心和对世界的悲悯**的领导方式，在她九岁时就“印在了她的心上”（Left such a thumbprint in my heart）。她坦言，娜乌西卡影响了她的许多领导力原则。`[个人哲学/灵感]`

-   **人生格言**：
    -   **工作中**：“Keep it simple.”（保持简单。）避免过度思考。
    -   **生活中**：“In a world where you can be anything, be kind.”（在一个你可以成为任何人的世界里，请保持善良。）微小善举可能对他人意味着整个世界。`[个人哲学/座右铭]`

---

## 精华收获

这场对话的信息密度极高，以下是你可以立即带走的、改变认知的行动纲领：

1.  **对开发者：重写你的技能树。**
    -   你的价值不再在于“写下代码”的能力，而在于对方向的想象力、对质量的验证判断力，以及利用Agent和Routines建立工作流自动化的能力。
    -   练习TDD 2.0：不是“我必须先写测试”，而是“我让AI帮我先写测试，我来设计逻辑”。

2.  **对管理者：重建你的操作系统。**
    -   **建立全景AI工作区**：不要只看PR清单。让AI帮你从宏观视角审视任务的模式和反馈热点。
    -   **从Synchronous到Async**：把重复的“晨间主动检查”行为变成定时的Routine（Agent），让它自动生成摘要，甚至修好Bug。
    -   **拥抱JIT规划**：放弃僵化的半年路线图。用月度方向图+每周校准清单代替。核心是“杀死不再服务于你的流程”。

3.  **对所有人：保持高能动性与行动。**
    -   如果感到恐惧，问自己：“什么是我能控制的一小步？” 然后立刻去做。
    -   理解“Agency”与“Accountability”是一体两面。拥有绝对的自由去探索，就必须承担绝对的责任去对结果负责。

4.  **传递火种：跨越鸿沟.**
    -   **不要只在技术圈内狂欢。** 花一点时间，找到一个让你生活变好的AI用例，分享给你关心的人——无论这是你的小企业主朋友、你的父母，或是你的长期客户。这是让他人超越恐惧的最好方式。

---

**结语**

Fiona Fung的这场对话，之所以值得被深度重构，是因为她成功地将“技术极端乐观主义”和“以人为本的务实哲学”结合在了一起。她既告诉你，未来已来，天花板已被AI彻底打破；又提醒你，作为一个技术圈的人，核心任务不仅仅是享受“8倍速”的快感，更要负责任地确保这份力量能被普惠地传递。

她就像一个现代版的娜乌西卡：深刻理解世界的风暴（AI的颠覆性力量），但始终坚持用一种极其温柔、坚定且充满智慧的方式去领导、去倾听、去照亮。

{% raw %}
<!-- TLDR: 编码非瓶颈，想象力与验证成新核心。Anthropic高管亲述AI原生团队构建与工程文化重塑法则。 -->
<!-- TAGS: AI, 工程管理, 产品思维, Anthropic, 个人成长, 组织文化, 编程未来 -->
<!-- RATING: 5 -->
{% endraw %}
