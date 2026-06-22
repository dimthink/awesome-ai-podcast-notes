---
title: "AI Agents Just Changed Forever: GLM 5.2, Codex Skills, Claude & Cursor"
channel: "Riley Brown"
published: "2026-06-21"
source_url: "https://www.youtube.com/watch?v=Nbynj-mKcNI"
video_id: "Nbynj-mKcNI"
tags: ["AI", "AI Agent", "GLM", "Cursor", "Codex", "SpaceX", "Anthropic", "Claude", "开源模型", "超级应用"]
rating: 4
language: "英文"
word_count: 10056
duration: "22:19"
---

# AI Agents Just Changed Forever: GLM 5.2, Codex Skills, Claude & Cursor

- **Channel:** Riley Brown
- **Published:** 2026-06-21
- **Source:** https://www.youtube.com/watch?v=Nbynj-mKcNI
- **TL;DR:** AI 超级应用大战提前爆发：开源模型 GLM 5.2 通过实战检验逼近闭源顶尖，SpaceX 收购 Cursor 重塑竞争格局，Codex 开启“录屏即技能”新范式，用户深陷 Fable 戒断期，整个生态在剧烈的多极竞争中加速演化。
- **Tags:** AI, AI Agent, GLM, Cursor, Codex, SpaceX, Anthropic, Claude, 开源模型, 超级应用
- **Rating:** 4

## 版本

- [结构化文稿](2026-06-21-ai-agents-just-changed-forever-glm-5.2,-codex-skills,-claude-&-cursor-Nbynj-mKcNI.structured.md)
- [原始文稿](2026-06-21-ai-agents-just-changed-forever-glm-5.2,-codex-skills,-claude-&-cursor-Nbynj-mKcNI.transcript.md)

# 深度内容重构：AI Agent 颠覆性一周纪实

## 材料信息

- **标题**: AI Agents Just Changed Forever: GLM 5.2, Codex Skills, Claude & Cursor
- **作者/来源**: Riley Brown (频道: Agent Native)
- **类型**: YouTube 视频字幕（科技新闻评论/产品评测/行业分析）
- **关键元数据**: 预计发布于 2024 年下旬（基于 Fable 5、Claude Opus 4.8 等上下文），时长约 30-40 分钟。视频涵盖模型评测、产品功能解读、收购分析及行业趋势预测。

---

## 开篇引入

AI Agent 的世界正在以令人眩晕的速度自我重塑。在过去的一周里，几件看似独立的事件——一家中国公司的开源模型横空出世、一款编程助手被 SpaceX 以战略级金额收购、一个传说中的“神级模型”被政府叫停后引发的集体戒断反应、以及一个超级应用新增的“录屏即技能”功能——共同编织出了一幅关于 AI Agent 未来走向的宏大图景。

Riley Brown 作为《Agent Native》主理人，他的特别之处在于：他不只是新闻的搬运工，而是一个亲自下场、把手弄脏的实战派。他每周都会在这些前沿工具上花费数十小时进行“压力测试”。他的点评不仅仅是观点，更是建立在大量实证基础上的判断。在这期视频中，他带领我们穿越信息迷雾，用“是否通过氛围测试”这一极其朴素却又极其严苛的标准，为每一个新工具和模型做出了最诚实的判决。

如果你错过了过去 168 小时里发生的这些事，那么你对 AI Agent 的认知地图已经需要更新了。本文将以 Riley 的视角和深度，为你系统性地还原这一周的震荡。

---

## 详细内容

### 一、GLM 5.2 —— 开源模型终迎“氛围验证”时刻 `[章节 起始段落 / 视频开头至前 15%]`

**核心观点**

来自中国公司 Z.ai 的开源模型 GLM 5.2 是首个在 Riley 的严格个人实战中通过了“Vibe Check（氛围验证）”的模型。它的性能与闭源顶尖模型 Opus 4.8 和 GPT 5.5 相当，成本却仅是它们的五分之一甚至六分之一，且已可无缝集成进 Cursor 中使用。

**深度阐述**

Riley 以一个极其坦率的自我剖析切入这个话题：在经历了无数次对新模型的“期待——失望”循环后，他已经对开源模型的评测流程形成了条件反射式的怀疑。他直言，每次看到 Twitter 上那些漂亮的 Benchmark 排行榜——那些光滑的雷达图、蓝色的柱状图——他都下意识地认为这是“发布前的营销包装”。

> “Normally, when a new open model comes out, there are benchmarks that are released. They don't actually tell the whole story. There's a ton of hype... And usually, when I go to test that model, I just end up incredibly disappointed.” `[章节 起始段落]`
> *（“通常情况下，一个新开源模型发布时，都会放出各种基准测试。但这些测试根本不能反映真实全貌。网上一片炒作……而当我亲自去测试时，通常只会以极度失望告终。”）*

正是因为有这种“信任赤字”，Riley 对 GLM 5.2 的肯定才显得尤为弥足珍贵。他没有囿于纸面数据，而是让 GLM 5.2 经历了一套极具挑战性的实战“铁人三项”：

1.  **Convex 插件一键攻坚**：他要求 GLM 5.2 仅凭一次对话（One-shot），就生成一个完整的 Trello 看板应用。这个应用需要包含数据库模型、用户认证体系以及 Trello 的核心功能（列表、卡片、拖拽等）。结果令人震惊——模型不仅完成了任务，而且在 Riley 看来“It works perfectly”。
2.  **自主搜索与内容生成**：他让 GLM 5.2 自主上网搜索关于他自己的信息，然后基于这些信息完整地生成一个个人介绍网页（Landing Page），并能本地运行。这个测试考验的是模型在多步推理、工具调用（浏览网页）和代码生成之间的协调能力。
3.  **全能代理集成**：他将 GLM 5.2 连接到了自己的 Notion、Slack 以及其他多种 API 集成中，让它执行日常的通用代理任务。Riley 的评价是：“It was doing a great job, just as good as if I was using Opus 4.8。”

这是 GLM 5.2 最让人兴奋之处。它的成功不仅仅在于跑了一些高分，而在于它在真实的生产力场景中“一点也不蠢”。Riley 甚至特别强调，因为它是开源模型，你可以真正下载它的权重，这意味着你不会像依赖 Fable 或 GPT 5.5 那样，在某一天突然被收走使用权。

**如何操作**

Riley 还大方地分享了将 GLM 5.2 接入 Cursor 的标准化流程（通过 OpenRouter 中转）：

1.  进入 Cursor 设置，找到模型（Models）选项卡。
2.  在 API Keys 区域，开启自定义 API Key 选项。
3.  将 OpenAI Base URL 覆盖为 OpenRouter 的固定地址（链接附在视频描述中）。
4.  在“添加自定义模型”中，粘贴 OpenRouter 上对应的模型 ID `z-ai/glm-5.2`。
5.  点击添加。整个过程仅需 3-5 分钟。

**个人感受**

Riley 的情感变化是本节最值得关注的部分。他毫不掩饰自己对“Benchmark 炒作”的厌倦，这种厌恶来自于一个极客对“真诚”的渴望。所以当他测试 GLM 5.2 并发现它“通过了 vibe check”时，他的声音里带着一种“捡到宝”般的惊喜。他的情绪不是简单的兴奋，而是一种被验证的快感：“原来这个时代真的有一个开源模型可以用了。”

**延伸思考**

这件事引发的深层思考远超模型本身。它标志着“开源”与“闭源”阵营的力量天平正在发生根本性倾斜。当开源模型的质量开始逼近——甚至某些方面超过——GPT 5.5 和 Opus 4.8，而成本却骤降至几十分之一时，商业公司的护城河正在以肉眼可见的速度被夯平。Riley 引用了一句极具冲击力的对话：当有人问中国何时能达到 Fable 级别时，Elon Musk 评论“Probably Q1”，而 Z.ai 创始人回复“Won't take that long”。这意味着，我们可能在未来数月内就会迎来一个完全开源、完全免费、却拥有顶级智能的模型。这将是 AI 民主化的里程碑时刻。

**精华收获**

- **即刻行动**：按照教程去 Cursor 里配置 GLM 5.2，亲自验证它是否能在你的工作流中胜任核心任务。
- **战略认知**：不要低估开源社区的反扑速度。模型的“稀缺性”正在消失，“硬核效率”和“生态渗透”将成为新的战场。

---

### 二、内生的力量：为什么 Agent 首先应该住在 Slack 里 `[视频中段 / 赞助商环节]`

**核心观点**

AI Agent 的最佳落地形态，不一定是一个全新的超级应用，而是直接嵌入团队现有的工作流。通过 HyperAgent 在 Slack 内创建被动式、自动化的“数字同事”，是对“Agent Native”概念最务实的诠释。

*（注：此段为视频中的赞助商内容，根据系统指令，我们必须完整保留原始材料信息。Riley 将其巧妙地融入了自己的叙事逻辑中。）*

**深度阐述**

Riley 描绘了一个极具代入感的场景：他构建了一个名为“YouTube 研究员”的 HyperAgent。这个 Agent 不需要任何人去主动“呼唤”它。它像一个沉默的、永远在线的分析师，被赋予了如下职责：

1.  **自动监控**：持续扫描指定竞争对手的频道，追踪哪些视频正在获得最佳表现。
2.  **选题推荐**：基于追踪到的关键词和热点，自动向 Slack 频道推送视频选题建议。
3.  **视觉优化**：当 Riley 上传一个新视频草稿时，Agent 能自动生成 20 个不同的缩略图方案，供团队直接选择。

Riley 反复强调了一个关键词——“被动”：

> “The coolest part is that I don't need to remember to open another AI tool and ask it to do this every time. Because the agent lives in Slack, my team and I can talk to it where we already are working.” `[视频中段 / 赞助商环节]`
> *（“最酷的部分在于，我不需要每次都记得去打开另一个 AI 工具然后要求它做这些事。因为代理就住在 Slack 里，我和我的团队可以在我们已经在工作的地方和它交流。”）*

这正是“Agent Native”哲学的体现：一个原生 Agent 不是你日程表上的一个额外科目，而是你工作环境中自然存在的一股气流。它主动推送信息，而非被动等待查询。

**个人感受**

尽管这是广告，但 Riley 的演示毫无违和感。他没有吹嘘参数的训练或技术的门槛，而是将焦点完全放在了“体验”上。他展现了当一个工具不再有存在感（Invisible）时，效率是如何自然而然提升的。这种感觉很像一个优秀的私人助理——你不需要告诉 TA 要做什么，TA 会在你需要之前把东西放在你桌上。

**延伸思考**

这引发了关于 AI 产品形态的深层博弈。一方面，Codex、Claude Desktop 和 Cursor 在努力构建一个什么都能做的大型“中央枢纽”式 Agent。另一方面，HyperAgent 这类工具试图让 Agent“隐身”于已有的“毛细血管”（Slack、Discord）之中。这是两种截然不同的哲学。前者让 AI 成为“新操作系统”，后者让 AI 成为“团队新成员”。对于绝大多数企业用户来说，“低摩擦接入”的吸引力可能比“全面控制”更大。

**精华收获**

- **团队管理思路**：考虑 AI Agent 时，想清楚它应该是一个需要你去访问的“工具”，还是一个主动为你工作的“同事”。
- **效率杠杆**：将 Agent 置于信息流的节点，而非源头，可以实现最大化的自动化收益。

---

### 三、Codex“录屏即技能”——示范式编程的降临 `[视频中段 / Codex 功能演示部分]`

**核心观点**

Codex 推出的“Record & Replay”功能，实现了从“自然语言编程”到“视觉示范编程”的范式飞跃。任何人只需对着屏幕操作一次，AI 就能将其消化为一个永久可用的自动化技能。

**深度阐述**

这是视频中最具科幻感的 Demo。Riley 想要给一个名为 Typefully 的工具创建一个“手动发布草稿”的自动化技能。过去，你需要用代码或复杂的 RPA 软件来描述每一步。现在，你可以用最简单的方式：直接做一遍。

Riley 让 Codex 开启屏幕录制，然后他在浏览器中自行完成了一整套 Typefully 操作流程：登录账号、点击新建草稿、输入文本内容、上传图片、设定发布选项。整个过程仅用了不到 1 分钟。

当 Riley 点击停止录制后，神奇的事情发生了。Codex 不仅仅是录下了一段视频，它自动分析了屏幕上的每一个点击坐标、每一个键盘输入和每一个页面跳转，然后将其编译为一个可执行的技能。

完成时，Riley 只在 Cursor 中输入了一个斜杠命令“/manual tweet draft”，AI 便立刻“附体”了计算机鼠标，像刚才的他一样，精确地重新执行了全部操作。

> “You could do it up to 30 minutes. You’re allowed to upload up to 30 minutes for a task so that Codex has a really good understanding of how to do it because they have a really good computer use.” `[视频中段 / Codex 功能演示部分]`
> *（“你可以录长达 30 分钟的操作。你可以上传最长 30 分钟的任务，让 Codex 有极好的理解，因为它们有非常强大的计算机使用能力。”）*

这意味着什么？意味着对于那些高频、重复、标准化的数字工作流（跨平台搬运数据、填写表单、生成报告），AI Agent 可以通过“观察学习”瞬间掌握。它本质上是 RPA 的“人工智能 2.0 版”，但门槛被拉低到了“会操作电脑”就行。

**个人感受**

Riley 对这个功能的评价是“incredibly underrated”。他的兴奋感是技术极客式的：他看到了一个“通用接口”的雏形。人类最自然的“教导”方式是什么？不是你写一本说明书，而是“看我怎么做一遍，然后你照做”。Codex 的这个功能，第一次在主流产品中将这种朴素逻辑变成了现实。这不仅仅是一个功能，更是一种人际交互语义的革命。

**精华收获**

- **自动化平民化**：任何熟练使用软件的用户，都可以瞬间成为自动化专家。编程不再是门槛，示范才是。
- **私域技能库**：你可以为自己或团队建立起一套定制化的“技能库”，这些技能代表了你组织内部独有的数字操作流程，构成了 AI Agent 的私人记忆。

---

### 四、600 亿美金的入场券：SpaceX 与 Cursor 的“超级应用”圣战 `[视频后段 / 收购新闻分析]`

**核心观点**

SpaceX 对 Cursor 的收购，是本周迄今为止最响亮的新闻（loudest news of the week）。这不仅是一次商业收购，更是一纸宣战书：Cursor 正式从一个“程序员专用编辑器”向“所有人的 AI 通用超级应用”转型，将与 Codex 和 Claude Desktop 形成三足鼎立。

**深度阐述**

Riley 在这个分析上表现出了极强的商业嗅觉，他没有被 600 亿美金的数字冲昏头脑，而是抽丝剥茧地分析了这笔交易的根本战略意义。

他指出了 Cursor 将获得的三个“无限杠杆”：

1.  **无限资本与算力**：SpaceX 作为全球第五大市值公司，可以为 Cursor 提供“烧钱”训练顶级模型、补贴用户套餐的底气。Cursor 完全有能力去训练一个与 GPT 5.5 或 Opus 4.8 水平相当的自研模型，并将其成本通过资本优势降到极低。
2.  **无限分发渠道**：获得 Twitter（X）的无缝分发入口。可以预见 Elon Musk 将会高频地利用其个人影响力推广 Cursor。
3.  **无限人才与模型池**：Cursor 本身已经训练出了 Composer 2.5 模型，且 Composer 3 正在开发中。合并后，这将成为 SpaceX 内部最宝贵的“AI 特战队”。

最关键的洞察在于 Riley 对 Cursor 官方公告文案的咬文嚼字：

> “Notice here in the actual announcement by Cursor that they didn't say for developers. They just said useful AI.” `[视频后段 / 收购新闻分析]`
> *（“注意观察 Cursor 实际公告中的措辞，他们没有说‘为开发者服务的 AI’，他们说的是‘有用的 AI’。”）*

这句话是整场分析的“轴”。Cursor 的野心已经昭然若揭：它不再是 IDE 市场里的某个竞争对手，它要成为 Codex 和 Claude Desktop 在“超级应用”战场上的直接对手。

**个人感受**

Riley 称自己“不关心收购本身，只关心代理是否变得更好用”。他的兴奋感非常纯粹——他看到了一个健康的“三足鼎立”格局正在形成。Codex、Claude Desktop 和 Cursor，每个平台背后都有巨头的资源支撑，都在疯狂迭代。这种局面对用户而言是最大的红利：更好的产品、更便宜的价格、更快的更新。

**延伸思考**

这笔交易揭示了一个正在成形的行业结构：未来的 AI 超级应用赛道，将是一场由资本、模型和分发网络共同支撑的立体战争。代码生成能力只是门票，资本厚度和生态广度才是决定谁能称王的关键。

**精华收获**

- **格局判断**：未来关注 AI Agent 平台，应该紧盯这三个名字：Codex、Claude Desktop、Cursor。他们是第一梯队。
- **用户策略**：在一个竞争白热化的市场里，享受价格战和功能军备竞赛的红利。不要过早“锁定”单一平台，保持工具的灵活性。

---

### 五、Claude 的“神话戒断症”：失去 Fable 后的世界 `[视频结尾前段 / Claude 产品更新与社区情绪]`

**核心观点**

在短暂体验了 Fable 5 的“神级体验”后，整个 AI 社区陷入了严重的“戒断反应”（Mythos Depression）。但 Anthropic 并未停步，通过对 Claude Design Mode 和 Claude Code Artifacts 的重大升级，他们正在为 Fable 的回归铺垫一个更强大的产品基座。

**深度阐述**

这是视频中最具人文色彩和情感张力的部分。Riley 捕捉到了一个极其微妙的集体情绪。

> “I've seen hundreds of tweets like this. Something around the lines of ‘using Fable for those days, it felt like it just never gave up on problems. Now back on Opus, and it's just kind of lazy. There was this sense when you used Fable that you could basically do anything.’” `[视频结尾前段 / Claude 产品更新与社区情绪]`
> *（“我看到了几百条类似的推文。大意是‘用 Fable 的那几天，感觉它就像永远不会对问题放弃。现在回到 Opus，感觉它一下子就变懒了。用 Fable 的时候，你会产生一种自己无所不能的幻觉。’”）*

Riley 将这种现象命名为 “Mythos Depression”（神话戒断期）。在他看来，Fable 所提供的不仅仅是更高的回答质量，而是一种“雄心”的释放。用户的想象力在 Fable 面前被极限拉伸，而当他们被迫回到 Opus 时，那种“天花板”的存在感变得前所未有的压抑。

然而，Anthropic 也没有闲着。Riley 详细介绍了 Claude 的两项重要防守更新：

**1. Claude Design Mode 进化**

现在，Claude 的 Design 模式不仅限于生成代码，它可以直接在生成后的“画布”上进行实时编辑、锁定设计系统的一致性，并且可以一键将其导出到 Lovable、Vercel、Miro 等平台。这意味着 Claude 不仅仅是“设计工具”，而是成为了一个“设计即部署”的平台级产品。

**2. Claude Code Artifacts（小程序）**

这是最让 Riley 兴奋的更新。Claude Code 现在可以生成可交互的“小应用”，Riley 称之为“Agent Native Apps”。举个例子：当你让 Claude Code 分析用户流失数据时，它不再只是输出一段带图表的报告，而是直接生成一个拥有交互界面的、可独立运行的 Mini App。这个 App 拥有自己的独立 URL，可以像网页一样直接分享给团队任何人。

> “Links made for sharing. You can very easily share these little mini apps or artifacts... I call them agent native apps.” `[视频结尾前段 / Claude 产品更新与社区情绪]`
> *（“专为分享而生的链接。你可以极其轻松地分享这些小应用……我称它们为代理原生应用。”）*

**精华收获**

- **心理洞察**：模型能力的“阶跃增长”会产生巨大的心理落差效应。不要因为暂时的“降级”而放弃 Agent 的使用习惯，耐心等待迭代。
- **功能洞察**：Claude 的 Artifacts 功能，让 AI 的输出从“文档”级别直接跨越到了“产品”级别。这是 Agent 能力可视化和协作化的关键一步。

---

### 六、下周展望：Fable 回归与 Google 的“超级应用”迷思 `[视频结尾 / 最后一分钟]`

**核心观点**

疯狂的竞争还远未结束。Fable 有望最早下周回归；OpenAI 可能发布新模型；更多开源模型将亮相；而 Google 依然在多个产品线中迷失方向，亟需做出关于“超级应用”的关键决策。

**深度阐述**

Riley 在视频尾声做了一个简短的“下周菜谱”预告：

1.  **Fable 回归**：大量 Twitter 传闻表明，Anthropic 与政府的协商已有进展，Fable 将很快回到主流产品中。
2.  **Google 的困境**：Riley 对 Google 的态度非常直白——带着遗憾的批评。他认为 Google 拥有庞大的资源和深厚的技术积累，但产品线过于分散，缺乏一个“超级应用”来凝聚力量。他直接挑战了 Google AI 的高管：“Feels like we are entering the super app era... Choose your challenger.”（“感觉我们正在进入超级应用时代……选一个你的挑战工具吧。”）

**精华收获**

- 未来一周，AI Agent 领域的战争将进入一个新的阶段。除了功能比拼，“战略定力”和“产品聚焦度”将成为新的核心竞争力。
- 留给 Google 犹豫的时间窗口正在关闭。

---

## 结语

Riley Brown 在这期视频中，以其独特的“实战派极客”风格，为我们编织了一幅极其充实的 AI Agent 周报。从开源模型的逆袭、到超级应用的功能秀肌肉、再到巨头入局的格局重塑，他始终坚守着一个朴素的信条：**真正重要的不是纸面上的 Benchmark，而是它是否通过了属于你自己的“氛围测试”。**

在你们即将关闭这篇文章之前，务请记得亲自去试试 GLM 5.2，去看看 Codex 的录屏技能，去感受一下 Cursor 被 SpaceX 注入能量后的迭代速度。正如 Riley 所说，不要相信任何人的话，包括他。去亲自动手，成为真正意义上的“Agent Native”。

<!-- TLDR: AI 超级应用大战提前爆发：开源模型 GLM 5.2 通过实战检验逼近闭源顶尖，SpaceX 收购 Cursor 重塑竞争格局，Codex 开启“录屏即技能”新范式，用户深陷 Fable 戒断期，整个生态在剧烈的多极竞争中加速演化。 -->
<!-- TAGS: AI, AI Agent, GLM, Cursor, Codex, SpaceX, Anthropic, Claude, 开源模型, 超级应用 -->
<!-- RATING: 4 -->
