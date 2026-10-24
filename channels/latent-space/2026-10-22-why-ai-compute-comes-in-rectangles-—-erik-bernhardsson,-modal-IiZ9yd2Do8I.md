---
title: "Why AI Compute Comes in Rectangles — Erik Bernhardsson, Modal"
channel: "Latent Space"
published: "2026-10-22"
source_url: "https://www.youtube.com/watch?v=IiZ9yd2Do8I"
video_id: "IiZ9yd2Do8I"
language: "英文"
word_count: 16800
duration: "1:25:33"
---

# Why AI Compute Comes in Rectangles — Erik Bernhardsson, Modal

- **Channel:** Latent Space
- **Published:** 2026-10-22
- **Source:** https://www.youtube.com/watch?v=IiZ9yd2Do8I
- **TL;DR:** 如果要用一句话概括这个时代最荒谬的错配，那就是：**所有人都在谈论 AI 的无限需求，但真正决定 AI 能走多远的，是硬件被切成"三年期长方形"出售这件事。**

## 版本

- [结构化文稿](2026-10-22-why-ai-compute-comes-in-rectangles-—-erik-bernhardsson,-modal-IiZ9yd2Do8I.structured.md)
- [原始文稿](2026-10-22-why-ai-compute-comes-in-rectangles-—-erik-bernhardsson,-modal-IiZ9yd2Do8I.transcript.md)

# 为什么 AI 计算是长方形的：Erik Bernhardsson 与 Modal 的基础设施革命

**材料信息**

- **标题**：Why AI Compute Comes in Rectangles — Erik Bernhardsson, Modal
- **作者/来源**：Latent Space 播客（采访者：swyx/Alessio，嘉宾：Erik Bernhardsson）
- **类型**：YouTube 视频字幕（访谈实录）
- **关键元数据**：约 60 分钟深度访谈；涉及 Modal 公司（AI 基础设施）、GPU 容量市场、Sandbox 产品、Agent 时代工程文化等核心议题

---

## 开篇引入

如果要用一句话概括这个时代最荒谬的错配，那就是：**所有人都在谈论 AI 的无限需求，但真正决定 AI 能走多远的，是硬件被切成"三年期长方形"出售这件事。**

Erik Bernhardsson 是极少数同时理解"软件之美"与"硬件之痛"的人。他曾在 Spotify 从零构建了音乐推荐系统（包括著名的 Discover Weekly），在 Better.com 做过 5 年 CTO 把技术团队从 2 人扩张到 400 人，如今他在 Modal 做的事情，用他自己的话说，是"把全世界分散的算力聚合成一个巨大的容量池，再把它切成任意粒度的方块"。

这场对话的价值不在于 Modal 又融了多少钱，而在于它罕见地揭开了一个平时被掩盖的真相：**生成式 AI 的繁荣，正在与一个由三年期合同、预付款、Spot 实例、二手 GPU 期货和"接近财务工程"的 neocloud 构成的真实物质世界激烈碰撞。** 在这个世界里，一个软件公司可能被迫变成一家类金融公司——仅仅因为拿不到 GPU。

这不是一篇关于"如何做 AI 产品"的访谈，而是一篇关于"AI 产品必须踩在什么地基上"的访谈。读完它，你会理解为什么"计算是长方形的"这个听起来古怪的命题，实际上是整个行业最大的结构性摩擦点。

---

## 详细内容

### 从 Spotify 推荐系统到 Modal：一条"基础设施之痛"的暗线 `[章节 1.1-1.4 / 00:00-03:30]`

**核心观点**
Erik 的职业路径表面是"Spotify → Better.com → 创业"，但内在逻辑是同一件事：他反复撞上"基础设施不够好"这堵墙，而 Modal 就是他自己在当时最想要的那把锤子。

**深度阐述**

访谈开场的寒暄几乎是速通式地展开的。Erik 先介绍了 Modal 的定位——"AI 基础设施公司"，提供计算平台和存储平台，客户名单里有 Decagon、Sunno（Suno）、Runway、Cognition。他强调 Modal 做的事情"in practice"是大量的推理（inference）、沙盒（sandboxes）、有时还有训练和微调以及批处理任务。而它的本质是一个**SDK**：让客户能把代码快速部署、扩展、在生产环境跑起来，底下所有的容量管理 Modal 都替你搞定。

访谈者（swyx）提到一个很有说服力的细节——他自己就在用 Modal 做一个侧项目，把 2D 图像转成 3D 模型，用来托管模型。当中问他反馈如何时，他说："I love it."，并补充说这正是他**放弃所有竞品**选择 Modal 的原因。这类第一手用户认可，比任何营销文案都更有分量。

回到增长数字。两年前 Erik 上过这档节目，被问及规模对比时，他说：

> "It's probably like at least like 50x in terms of like revenue and users and usage and stuff like that."
> ——"大概至少是 50 倍，无论是收入、用户还是用量。" `[章节 1.2]`

真正有趣的是他讲的个人史。他在 Spotify 待了约 **7 年**（2008/2009 年加入），主要贡献是**从零构建了音乐推荐系统**，并带起了一个小团队，上线了 related artists、Discover Weekly 等一大批功能。他的原话里点出了 Modal 的"创世胚胎"：

> "arguably like a lot of what sort of later became the genesis of modal was... just building AI applications and realizing like the infrastructure sucks like there's got to be a better way to do that."
> ——"可以说，后来成为 Modal 起源的很多东西，就是不断构建 AI 应用、然后意识到基础设施烂透了、一定有更好的办法。" `[章节 1.3]`

中间的插曲是 Better.com——一家做**按揭贷款（mortgages）**的公司。Erik 说是"有点绕路（side tour）"，他在那里做了 5 年 CTO，把技术团队从 2-3 人扩张到 **300-400 人**。他坦承在那里学到了大量关于**管理、团队建设、招聘和开发者生产力**的东西。"但那是一家过山车式的公司"，他说，长远故事"以后单独讲"。后来疫情后利率飙升，公司出了很多问题，但"那时我早就离开了"。

**延伸思考**

注意这条暗线的结构：Spotify 教会他**计算密集型的 AI 应用怎么做**（矩阵分解、推荐系统），Better.com 教会他**如何管理和规模化一个技术组织**，而 Modal 则是两者的合流——他既有想要的一种基础设施，又有能力把它构建成一家公司。这不是随机跳槽，而是为一个更大赌注蓄力了十几年。

**精华收获**

- Modal 的核心不是"卖 GPU"，而是**把底层基础设施复杂度封装成一个 SDK**，让客户不需要碰 Kubernetes、Docker、容量调度这些事。
- Erik 的创业动因是"痛点驱动"而非"风口驱动"——他在 Spotify 就想拥有这样一个工具，等了十年才自己做出来。

---

### Luigi、Web Scraping 与 Modal 的诞生：第 3 个才是对的 `[章节 2.1-2.3 / 03:30-08:00]`

**核心观点**
Modal 不是 Erik 的第一想法。他先做了个 web scraping 项目（无疾而终），又回想起了在 Spotify 时写的开源框架 Luigi（工作流编排），但最终意识到：**真正难的问题不是"编排"计算，而是"执行"计算。**

**深度阐述**

Erik 对"从 Better.com 到 Modal"这条路径的描述非常诚实，他说：

> "I wasn't sure if I wanted to start a company."
> ——"我不确定自己是不是想再创业。" `[章节 2.1]`

疫情初期他两个孩子分别只有 2 岁和 4 岁，他基本算是给自己放了个"长假"，一边带孩子，一边做点兼职 hacking，考虑过要不要去做咨询。他前两个想法"went nowhere"，第一个是某种 web scraping 的东西——"回头看也许本来能成"。

关键转折出现在他想起 Spotify 时期的开源框架 **Luigi**——这是一个和 Airflow、Prefect、Dagster 同一类别的**工作流编排（workflow orchestration）**框架。Erik 提到："这是个有点过时的品类，现在大家不太聊它了，但一度引起过很多关注。" 他从没把它变成生意。2021 年再想起它时，起初是回到工作流编排，做了一堆"在云端编排代码运行"的尝试。但随之而来的领悟是：

> "at the end of the day like core puzzle piece is not just like orchestrating the compute it's like executing the compute."
> ——"归根结底，核心的那块拼图不只是编排计算，而是执行计算。" `[章节 2.2]`

他把 Luig 式的工作流调度"放上货架"，说"我一会儿再回来搞工作流调度"——但再也没回去。这个细节对创业者极有启发：**想法会自我进化，而"更大的问题"一旦被看见，就很难装作没看见。**

值得注意的是时间线。Erik 说这些尝试发生在 **2021 年**，而 ChatGPT 是 2022 年底才发布的。也就是说——Modal 的核心洞察诞生于 LLM 时代真正开启之前。这是一个关键的认知型套利：他押注的是"把代码跑在云上应该变得极其容易"这件事的通用价值，而非某个具体应用。

**延伸思考**

这是典型的"底层抽象时刻"。每一波技术浪潮都会催生一批"重新打包基础设施"的公司：PC 时代有操作系统，Web 时代有云，移动时代有 App Store，而现在 AI 时代需要新的"执行层"。Erik 判断的是：**这个执行层必须从头重写，而不是在 Kubernetes 上加一层封装。** 这个判断在后续章节会被反复证明其正确与昂贵。

**精华收获**

- "编排"是一个老品类；"执行"才是新的基础设施战场。
- 好的创业想法往往来自你私人反复被折磨的痛点，而不是别人的 PPT。
- 时间点很重要：Modal 的核心洞察诞生在 ChatGPT 之前，这让它的先发优势带有"预知"的色彩。

---

### Stable Diffusion 成为 Modal 的第一个杀手级应用 `[章节 3.1-3.3 / 08:00-12:30]`

**核心观点**
ChatGPT 不是 Modal 的杀手级应用，**Stable Diffusion 才是**。收入从每月 100 美元到 2000、再到 30000 美元的爆发式增长，让 Erik"胸口一块巨石终于落地"，也让他确认自己"赌对了方向"。

**深度阐述**

Erik 承认 Modal 的初期增长靠的是他自己的"互联网人格"——他自称是"compulsive tweeter（强迫症式发推者）"，也一直写博客，有一点粉丝基础。他称之为"founder-led marketing（创始人主导的营销）"：

> "I always feel like you kind of have to lean into like what you're good at and like what I'm good at is like I guess like just posting and being terminally online."
> ——"我一直觉得你得顺着自己擅长的事情去做，我擅长的……大概就是发帖，以及永远在线。" `[章节 3.1]`

**"永远在线"在他这里不是贬义，而是核心竞争力。**

资金方面，他自筹资金了好一段时间，甚至连最初几名员工都是自己掏钱养的。这让他在花销上变得极其节俭，"非常在意 ROI"，甚至很长一段时间没给自己发工资。直到"某个时刻变成了问题，因为我需要钱"，才在 **2022 年初**融了种子轮——那时他已经独自开发了大约一年。Asha（联创兼 CTO）在约五年前（2021 年 8 月左右）加入。但真正意义上的"有意义收入（meaningful revenue）"要到 **2022 年底**才出现。

然后是爆发点。Erik 给了非常具体的数字：

> "we went from like $100 a month in like November 2022 and the next month we did like $2,000 a month and then like January 2023 we did like 30,000 all of a sudden."
> ——"2022 年 11 月我们一个月才 100 美元，下个月是 2000 美元，然后 2023 年 1 月突然就到 30000 美元了。" `[章节 3.2]`

这一段的情绪极有张力——他说那种感觉是"一块巨石从胸口卸下（massive anxiety thing off my chest）"，然后想："也许我们真的抓住什么了。"

那个 30000 美元的时刻，客户非常集中——主要是纽约一家叫 **Mage** 的公司（做 Stable Diffusion 相关）。2023 年第一季度，Mage 一家可能占了 Modal 80-90% 的收入。之后才开始多元化。**2023 年底，Suno 成为又一个大客户**，一度占据很大比例，再往后收入结构才真正健康起来。

一个有趣的细节：comfyUI 用户多不多？Erik 说"有一些，但用 Modal 的人更偏向底层/复杂用法"。因为 Modal 一直"hackable（可深度定制）"，用户往往部署自己的自定义工作流、适配器（adapters）、自定义推理和大量优化。而这恰好是后来 Modal 能承接生产工作负载的原因——**autoscaling 意外地是一个高度相通的问题**：你需要让容器极快地上下扩展。

**延伸思考**

Stable Diffusion 是"视觉、可分享、可被普通用户直接感知"的第一个 AI 原生应用，因此它带来的算力需求是爆炸式且广泛的。Modal 恰好在正确的时间拥有正确的抽象——不是给一个特定模型提供推理服务，而是给**一整类"跑自定义模型+自定义优化"的用户**提供机动能力。这解释了为什么 Modal 没有陷在"某个具体模型"上，而能持续吃到一波又一波应用的红利。

**精华收获**

- 杀手级应用常常出乎创始人意料（本来以为是 ChatGPT，实际是 Stable Diffusion）。
- "可 hack 性"是基础设施产品的长期护城河——它让早期用户成为深度用户。
- 收入结构的"单点依赖"是危险的，及时多元化才有稳健增长。

---

### 为什么必须重写一切：旧工具装不进新工作负载 `[章节 4.1-4.3 / 12:30-17:30]`

**核心观点**
每一代技术都会撞上上一代工具的天花板。Kubernetes 和 Docker 是为"稳定、低利用率、CPU 便宜"的后端负载设计的，而 GenAI 是"GPU 极贵、模型极大、需要跨网络加载、用量剧烈波动"的负载——**你不能在旧地基上盖新楼，必须从头重建。**

**深度阐述**

当被问"为什么 autoscaling 这类工具以前不存在，你要自己造"时，Erik 给出了他最具方法论色彩的一段阐述。他把历史拉长：

> "every new sort of era of like technology kind of runs up against limitations of tools... you look back like the web or the cloud or mobile or PCs or AI."
> ——"每一个新的技术时代，都会撞上既有工具的局限……回看 web、云、移动、PC 或者 AI，都是如此。" `[章节 4.1]`

他举了云时代的例子："我们不得不发明 Kubernetes 和 Docker 这些东西。" 而在 GenAI 身上，你当然可以"把新东西架在 Kubernetes 和 Docker 上"，但这些技术是为一种**截然不同的负载**设计的——稳定的后端工作负载、请求数恒定、利用率低，因为 CPU 便宜，所以没人在意成本。

而 GenAI 世界完全不同：
- **GPU 极其昂贵**，所以你必须管理容量和利用率；
- **模型极大**，需要通过网络从 CPU 加载到 GPU；
- 这两种特性让旧工具"根本不是为此而造"。

于是 Modal 不得不在过去几年里自己造了一堆东西：**自己的文件系统、CPU snapshotting、GPU snapshotting、自己的 autoscaler 和调度器**，以及各种容量管理工具。Erik 的结论极为干脆：

> "you can't build like a wrapper on top of the old stuff in order to do the new stuff you kind of need to start over a little bit from scratch."
> ——"你没法在旧东西上加一层封装来做新的事情，你得某种程度上从头重来。" `[章节 4.2]`

关于"扩展过程中是否遇到奇怪行为"，Erik 说容量始终是挑战——如何拿到几百、几千甚至几万个 GPU。他提到一个**事后看来非常关键的决定**：很早就做了**多区域（multi-region）**部署。不是把每个区域当独立集群看，而是：

> "we always thought of like our capacity management as like one big pool like it's like one big pool over the the entire world."
> ——"我们一直把容量管理看成一个巨大的池子，一整个覆盖全球的池子。" `[章节 4.3]`

他坦承这些年当然也遇到过 bug、掉线，尽管他希望 Modal 能 100% 在线，最近几个月也只接近四五个九（99.99x%）。

**个人感受**

Erik 说这些话时的语气是"基础设施极客"式的兴奋。他多次自称 "infra geek"，每次讲到自建文件系统、snapshot、调度器都会露出一种"这才是最好玩的部分"的感觉。这种对底层的热爱，恰恰是他能看穿"旧工具装不进新负载"的根本原因——**外行看 Kubernetes 已经够用，内行看它处处是错配。**

**延伸思考**

"你不能在旧工具上加一层包装"几乎是所有基础设施创业公司都必须回答的问题。Web 时代的答案是"不要用 CGI"，云时代是"不要自建机房"，AI 时代很可能就是"不要用 K8s 跑 GPU 推理"。识别"哪些旧工具会失效"其实就是识别"下一波基础设施公司的诞生地"。

**精华收获**

- 新负载需要新地基，封装旧工具在长期会输给从零重建。
- 多区域"一个大池子"的设计是一种战略选择，而非工程细节。
- 基础设施的"正确"，往往表现为"在别人手忙脚乱时你自动做对了事"。

---

### 算力的物质世界：从 Spot 到三年前签下的大合同 `[章节 5.1-5.4 / 17:30-25:30]`

**核心观点**
Modal 不拥有任何硬件，全部靠租。但过去一年，为了拿到足够的 GPU，它必须从一个"spot 实例拼装者"变成一家**同时跟 25 家云厂商谈判、预付数百万到上亿美元、签三年期合同**的公司。这是一次根本性的商业模式转变。

**深度阐述**

这是整场访谈信息密度最高的段落之一。Erik 回顾 Modal 的容量策略演变：

- **早期**：几乎全部容量来自**超大规模云厂商（hyperscalers）的 spot 和 on-demand**，主要是 spot，遍布所有区域，用 AWS、GCP，后来也用了 Azure。
- **稍早一点**：开始从 **Oracle** 租赁容量，因为想要 A100（访谈里口误为 810s/8100s），拿到了很好的价格。
- **再往后**：增加了几个云，并开始做预留（reservations）。

他说到 **2024 年底之前**，Modal 的大部分容量还是 spot 或**一年期预留**。而 spot 的本质是"可抢占（preemptable）"的——这需要专门应对，但因为**把成百上千个区域的容量聚合起来**，在总量层面"运作良好"。

然后市场变了。Erik 描述得非常直接：

> "the last year basically now in order to get the capacity we need we had to work with a much larger set of clouds. We actually work with almost 25 clouds at this point."
> ——"过去一年，为了拿到需要的容量，我们必须跟多得多的云合作。我们现在几乎跟 25 家云合作。" `[章节 5.2]`

而代价是：
- 很多情况下要**签三年以上的合同**；
- **提前支付一大笔钱（meaningful amount up front）**；
- **锁死三年期的价格**。

为此 Modal 做了两件事：一是**建了一个完整的采购团队**——"四个全职员工，基本上就只是采购容量、打电话给 neocloud、做交易、审查容量"；二是**组建了一个约 10 人的工程团队**，专门管理来自全球的**裸金属容量**，处理网络问题、坏盘、GPU 从总线上掉线等等。

**"我们不拥有容量，到目前为止全部是租的。"** Erik 明确强调。

关于"买 vs 租"，Erik 说他"并不教条主义（not mega dogmatic）"。租的好处是**资本效率**；买的话，既有**运营复杂性**（要处理供应商、电力、线缆），也有**财务复杂性**：你怎么融资？用股权融一个亿去买硬件，是"非常稀释的方式"；用债务融资，你通常需要**锁定的长期收入**来付利息。所以他反复权衡经济性、运营复杂度和风险，"这是个复杂的取舍，我们对买也持开放态度。"

更大的背景是，Erik 把 AI 投资放到宏观尺度：

> "AI investments starting to become like several percentage points of GDP of the US."
> ——"AI 投资正在开始占据美国 GDP 的好几个百分点。" `[章节 5.3]`

他还观察到美国利率最近几周在上升，并直言不讳地评价 neocloud：

> "these are very very sophisticated financial engineering companies."
> ——"这些是非常非常精密的金融工程公司。" `[章节 5.4]`

但他也清楚自己的偏好："我宁愿专注做一个精干的软件公司。我不认为软件公司拥有硬资产是好事——就像你该不该拥有自己的办公室一样。" 不过话音一转："当然，为了拿到想要的容量，一切都摆上桌面。"

**延伸思考**

这是一个罕见的截面：一个软件 CEO 被逼着谈"采购团队""债务融资""资产负债表"和"资产折旧"。当硬件成为稀缺资源时，"软件公司"的边界开始模糊——它被迫掌握供应链和金融工程的能力。**这不是 Modal 的选择，而是时代的强制。**

**精华收获**

- 云厂商的"spot + 一年期预留"模式曾完美支撑 Modal 的早期增长，但市场结构变了。
- neocloud 之所以能快速扩张，本质是"把尚未购买的容量预先卖出去"的金融构造。
- 软件公司是否该拥有硬件，是一个需要反复权衡资本效率、运营复杂性和风险的复杂问题。

---

### GPU 市场是"次要资源"还是"厕所纸式囤积"？ `[章节 6.1-6.4 / 25:30-32:30]`

**核心观点**
Erik 不认为 GPU 是"被完全垄断的资源"。只要出价够高就能拿到算力。他真正担心的不是价格暴涨，而是**价格崩塌**——那会杀死所有锁定了大量供应的人。

**深度阐述**

当被问"是否认同算力供应会长期受限"，Erik 给出了非常不主流的判断：

> "I don't necessarily agree with that. I mean like Nvidia is delivering, you know, several hundred thousand black walls, you know, a month."
> ——"我不一定同意。英伟达每月交付几十万块 Blackwell。" `[章节 6.1]`

（"black walls"是口误/听写错误，指 Blackwell。）他的逻辑很清晰：如果你愿意出比别人更高的价格，你就能拿到 GPU 容量。Anthropic 和 OpenAI 当然在尽可能扫货，但**供应持续在进入市场**，所以它"不是一个被完全垄断的资源"。

他还提出了一个更根本的观察——**硬件的常态是降价**：

> "the normal state of hardware is like it's like kind of like gravity like eventually hardware prices always go down so we're a little bit in like a weird sort of period of time where like hardware prices are going up."
> ——"硬件的常态就像重力——最终硬件价格总会下降。所以我们现在处于一个有点奇怪的时期，硬件价格在上涨。" `[章节 6.2]`

但涨多久？他坦承不知道，"可能再 6 个月，可能再 36 个月"。他把当前的"囤货潮"类比为**疫情期间的厕纸抢购**或"挤兑（run on the bank）"，是一种非理性的连锁反应。

然后是最反直觉的一段判断：

> "it's not even necessarily bad for us if prices go up cuz scarcity also means like we can charge more from our customers... I do worry more about actually prices collapsing."
> ——"价格上涨对我们未必是坏事，因为稀缺也意味着我们可以向客户收更多钱……我其实更担心价格崩塌。" `[章节 6.3]`

原因很直接：**对任何锁定了大量供应的人来说，价格崩塌是灾难**——你买在了最高点。"冒险在于买在顶部。" 在长期，硬件价格总是下降，所以这里存在一个"稀缺租（scarcity rent）"的问题：今天谁在享受这个租？他认为是**英伟达和大体上的 neocloud**——"任何拥有容量的人都享有更好的经济性，这在今天是不可否认的。"

至于竞争 OpenAI/Anthropic 抢 GPU，Erik 提供了几个有意思的观察：
- 价格上涨部分就是它们扫货的反映；
- 但**英伟达本身偏好一定程度的多元化**——它不想只服务少数大买家，愿意给 neocloud 和替代云更多配额；
- **OpenAI 和 Anthropic 偏好从"久经考验"的供应商批量购买**，因为他们要做大规模训练，需要非常大的连续块；
- 而这恰好给了 Modal 机会："你能在亚美尼亚搞到 32 个节点，在印度尼西亚搞到 128 个节点，我们喜欢这种。"

他还透露，Modal 对供应商有一套"规格表（spec sheet）"——需要多少 IOPS、CPU 至少要过某个 PassMark 分数、南北向带宽的最低要求等等。而且经常会做**验收测试期**：先拿一个节点跑一段时间。他也坦白，有时会签几千万到几亿美元的大单，但"对接的供应商我们其实还没完全了解"，所以"多少有点信仰之跃"。他甚至打趣说自己心里有一套"Modal max score"——类似 SemiAnalysis 的 ClusterMax，他知道自己更喜欢哪些供应商，以及**谁响应快、谁修问题快、谁宕机后修得快**。

**延伸思考**

"投资 GPU 也像买在顶部的风险"这个洞察，把 AI 基础设施和金融周期绑到了一起。这也解释了一个看似矛盾的现象：此刻所有人都在喊"算力荒"，但一旦新一轮产能上线或需求放缓，拥有大量长期锁定资产的公司可能一夜之间从英雄变成债务重负。

**精华收获**

- GPU 不是被绝对垄断的资源，价格是准入的钥匙。
- 真正的风险不是涨价，而是**降价**——买在顶部的人是最大输家。
- 稀缺租流失到英伟达和 neocloud，谁拥有容量谁享有更好的经济性——但这是否值得承担持有昂贵资产的风险，另当别论。

---

### "别去垄断市场"：Hunt 兄弟的银色教训 `[章节 7.1-7.3 / 32:30-37:30]`

**核心观点**
当被问"既然智能需求无限，为什么不干脆把能买的容量全都买下、多买的转卖出去"，Erik 用 **Hunt 兄弟垄断白银市场失败**的历史故事给出了否定回答。他不追求"蛇吞象"，而是让容量扩张**匹配需求增长**。

**深度阐述**

访谈者的问题很诱人：既然"对智能的需求几乎是无限的"，为什么不趁现在就尽可能地买下所有容量？如果买多了还能转卖给别人。

Erik 的回应很有层次：

首先，**即便今天买了也用不完**——"我们能利用其中很多，但用不完"。当对方追问"可以转卖给想用的人"，他点出关键风险：

> "if you know prices going down and utilization going down and the market for reselling capacity goes vanishes at the kind of the same time."
> ——"如果价格下跌、利用率下降、转卖容量的市场同时消失——它们是相关的。" `[章节 7.1]`

这些风险是**高度相关**的，不是独立事件。一旦尾部风险降临，可能"非常糟糕"。他坦承自己是"极度激进的人"——"我每天都在激进地买容量、为买容量而融资"——但他也要指出其中的**尾部风险（tail risks）**。

然后是那段极有分量的自白：

> "maybe I'm you know I'm just old and I've seen this in the past like I actually had my first job in 1999 so I saw the dotcom crisis and I've seen the great financial crisis."
> ——"也许我只是老了，以前见过这些。我 1999 年就参加工作了，所以亲眼见过互联网泡沫崩盘和金融危机。" `[章节 7.2]`

这解释了他为什么想建一家能"再活 20、30、50 年"的公司，而不是趁热"疯狂买容量、试图垄断市场"。他以**Hunt 兄弟（Hunt brothers）**的故事收尾——这是交易史上一个传奇案例：他们试图垄断白银市场，结果"以极其壮观的方式失败了"。Erik 的结论是：

> "cornering the market I think in general like can be not a good idea."
> ——"总的来说，垄断市场不是个好主意。" `[章节 7.3]`

但他的策略并非保守："我们总体上非常、非常有攻击性，但我们是按照一个激进但**与需求增长匹配**的计划来扩产，并匹配我们明年年底想达到的 run rate。"

**个人感受**

这一段是整场访谈里最能体现"成熟创业者 vs 赌徒"分野的地方。Erik 没有否定野心，而是用历史经验为野心装上安全阀。一个 1999 年入行、见过两次大崩盘的人，对"这次不一样"天然保持警惕——这恰恰是他在算力狂热中保持清醒的原因。

**精华收获**

- "需求无限"不等于"该无限囤货"——相关风险（价格+利用率+转售市场同时崩）是最大的杀手。
- 老一代创业者的历史记忆是一种稀缺资产，它让你在狂热中问出"如果这次也崩了会怎样"。
- 激进扩产但**匹配需求**，比"试图垄断"更可持续。

---

### 替代加速器、TPU 与"2027 会不会是那一年" `[章节 8.1-8.2 / 37:30-41:00]`

**核心观点**
Erik 自嘲每年都预测"明年是替代加速器之年"，每年都错，但他认为 **2027 年可能是真正的一年**。软件层一旦修好，非英伟达加速器会有巨大需求。

**深度阐述**

关于是否只用英伟达硬件，Erik 说 Modal 在看替代方案，并直言：

> "every year in the last five, maybe even 10 years, I've been saying, you know, like next year it's going to be the year of like non-Nvidia accelerators and and then I'm always wrong, but but I do think 2027 might be the year."
> ——"过去五年、甚至十年，我每年都说'明年会是替代加速器之年'，然后我总是错。但我确实觉得 2027 年可能是那一年。" `[章节 8.1]`

他点名了：
- **AMD** 在某些方面开始拿到非常好的分数；
- **TPU** 显然在 Google 内部被广泛使用，看起来运转良好；
- **Trainium** 他了解不多，但团队很强，在做很多软件工作。

他的核心论点是"硬件难，软件易"：

> "hardware is hard in a certain way... if we just fix the sort of software layer for these accelerators like I think there's going to be a lot of demand for them."
> ——"硬件在某一方面是难的……如果我们把这类加速器的软件层修好，会有大量需求。" `[章节 8.2]`

他也指出更深层的瓶颈：**台积电和 ASML** 可能是比英伟达更底层的卡点。长期来看，"垄断不会永远持续"，市场有多样性会更健康。他还提到 Cerebras、Groq 等玩家，并分享了一个前卫的实践——**混合、解耦式推理（hybrid/disaggregated inference）**：用**英伟达做 prefill，用 Cerebras 做 decode**。"有些东西是计算密集的，有些是内存密集的，你可以混搭。" 他认为这在实践中部署会变得很复杂，但**机会巨大**。

**延伸思考**

"某些负载计算受限，某些负载内存受限"这一观察，实际上是硬件多样性需求的根本来源。用于 prefill 和 decode 的最优硬件不同，意味着未来的 AI 服务器很可能是**异构拼装**的——这对编排层是巨大的挑战，也是新基础设施公司的机会。

**精华收获**

- 替代加速器的瓶颈主要在**软件层**，而不是硬件本身。
- 混合、解耦式推理（NVDA prefill + Cerebras decode）是值得关注的前沿方向。
- 长期看，垄断不会永久，市场会向多元加速器演化。

---

### Neocloud 的魔法：预售你还没买的东西 `[章节 9.1-9.3 / 41:00-46:00]`

**核心观点**
Neocloud 能极速扩张，靠的是一套精妙的金融构造：**先和大买家签 5 年合同，再拿着合同去华尔街融资，然后去买硬件、装机、交付。** 这套"预售未购之物"的机制，是 Modal 这种 PLG 公司无法直接复制的。

**深度阐述**

当被问"从 neocloud 学到什么"时，Erik 说最疯狂的例子是 **Nscale**——"从默默无闻，到拥有数百亿美元级别的 pipeline，尽管几乎没有多少容量"。他解释这套机制的运作方式：

> "they go out to like you know anthropic or or or opening eye some some big buyer... say like hey do you want to buy like 5 years of chips... and then they take that contract and then they go to you know Wall Street and say look we got this like you know big buyer... we just need the money right now."
> ——"他们去找 Anthropic 或 OpenAI 这样的大买家，说'要不要买五年的芯片，给你个好价'，然后拿着合同去华尔街说'看，我们有这个大买家，他们承诺了 100 亿美元的芯片，我们现在只是需要钱'。" `[章节 9.1]`

融到钱之后，他们去找超微（Supermicro）、戴尔、英伟达拿硬件，装好、交付。这是一套"先卖出尚未购买之物"的漂亮金融构造，让他们能够**极其快速地扩张**。

Erik 坦承 Modal 因为更偏向 **PLG（Product-Led Growth，产品驱动增长）**、没有能力"同样地锁定长期合同"，从财务角度看**扩张速度会慢一些**。但他认为长期会追上来。他对 neocloud（尤其是核心几家大厂）的评价是"非常、非常精于如何融资、如何把 GPU 当作贷款抵押品"。

问到"Nvidia 说要把 GPU 变成一种资产类别"，Erik 提到一批创业公司——**Silicon Data、Compute Exchange** 等——正在试图**建立价格指数/指数与衍生品交易**。他承认这很有意思，但指出天体特质障碍：

> "compute... is definitely not as homogeneous as other asset classes. you have different network and different locations and and and different discs and and CPUs... I mean that being said like you can say the same thing about oil."
> ——"算力绝对不像其他资产类别那么同质化。你有不同的网络、不同的位置、不同的硬盘和 CPU……不过话说回来，石油当初也是这样。" `[章节 9.2]`

封笔判断：他认为这个规模下行业确实需要更聪明的**风险对冲（risk hedging）和风险共担机制**，但他**不确信 GPU 会变成像布伦特原油（Brent crude）或亨利港天然气（Henry Hub）那样极度商品化、可交易的资产**。

**延伸思考**

"预售未购之物"这套构造本质上是把**未来现金流证券化**。它极其高效，但也意味着整个算力供应链的底层风险被层层打包，一旦需求或价格反转，传染性会很强。这与 2008 年金融危机前某些结构化产品的逻辑有相似之处——**当你可以提前把未来卖出去时，所有人都会忍不住多卖一点。**

**精华收获**

- Neocloud 的增速核心是"金融工程"，而非纯技术或运营。
- GPU 作为资产类别最大的障碍是**非同质化**（网络、位置、硬件配置各异）。
- PLG 模式扩张慢，但可能比"押注长期合同"更稳健、抗周期。

---

### 两个产品：Functions 与 Sandboxes `[章节 10.1-10.3 / 46:00-50:30]`

**核心观点**
Modal 有两大产品：**Modal Functions**（2021 年推出）和 **Modal Sandboxes**（2023 年推出）。Functions 占收入约三分之二，主要跑推理；Sandboxes 占约三分之一。Erik 反复强调：**Modal 不是 neocloud，也不想变成 neocloud。**
