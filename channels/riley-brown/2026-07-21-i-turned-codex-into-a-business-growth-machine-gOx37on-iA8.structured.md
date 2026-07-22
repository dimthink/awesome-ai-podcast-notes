---
title: "I Turned Codex Into a Business Growth Machine - 结构化文稿"
channel: "Riley Brown"
published: "2026-07-21"
source_url: "https://www.youtube.com/watch?v=gOx37on-iA8"
video_id: "gOx37on-iA8"
variant: "structured"
---

# I Turned Codex Into a Business Growth Machine - 结构化文稿

- **Channel:** Riley Brown
- **Published:** 2026-07-21
- **Source:** https://www.youtube.com/watch?v=gOx37on-iA8
- **Main:** [I Turned Codex Into a Business Growth Machine](2026-07-21-i-turned-codex-into-a-business-growth-machine-gOx37on-iA8.md)

# 我将Codex变成了业务增长机器：九个高效营销工作流

**来源：Riley Brown | 翻译整理**

---

## 引言：用Codex驱动营销

如果你在使用ChatGPT、Claude、Claude Co‑work或Codex，却不知道如何利用AI智能体做营销，那么你来对地方了。Riley Brown（本片主讲人）和他的联合创始人Vashall一起演示了如何在Codex中运行整个初创公司的营销工作。Vashall正从软件工程转向营销，因为当前营销的增量价值已经高于工程。而Riley则使用Codex内部的新模型（接近Fable水平的5.6版本）处理几乎所有任务。今天他们将展示Codex中最关键的九个营销工作流，教你如何利用AI智能体高效获客。

## 什么是Codex？

在正式开始前，Riley快速介绍了Codex的界面：左侧是聊天区，可按项目组织；中间是智能体聊天区；右侧显示智能体的工作成果。你可以用Codex完成任何知识型任务，甚至创建应用。Vashall之前主要用Codex写代码，但现在营销成了新重点。

## 工作流一：刮取所有社交平台的创作者内容

第一个营销技能/工作流允许你**从任何平台刮取社交媒体内容**。Riley演示了如何使用自建的`scrapecreators`技能：

> 他输入指令：“请找到Instagram上的创作者Callaway，抓取他过去几个月最好的10个视频，获取脚本和原始视频，把它们放入一个新的Notion数据库（测试用），并告诉我他为什么是优秀的短视频创作者。”

他选择了Codex的5.6模型（中等智能），认为这是一个直接的任务。大约等待2–3分钟后，结果出现：

- 系统找到了Callaway的已验证主账号；
- 下载了10个源视频和脚本；
- 创建了包含视频时长、评论数、点赞数等详细数据的Notion数据库；
- 直接在Codex内打开了Notion，能看到每个视频的原始文件。

Riley解释：**AI写内容脚本的能力并不好，因为内容质量是主观的；但AI非常擅长通过优秀样例进行模仿。** 所以，提供高质量样例是生成好内容的关键。这个技能正是为AI提供了一个样例数据库，让它能随时调用最佳素材。

此外，这个技能对视频编辑也极其有用：比如可以指定搜索瑞士的风景视频，或寻找Alex Hormozi在户外走路的片段，直接下载为B‑roll。它支持任何平台。

### 额外资源：所有技能与Riley Brown智能体

Riley提示：本视频提到的每个技能都可以在描述中找到链接，他还附带了更多额外技能。更值得一提的是，你可以雇佣“Riley Brown智能体”——这是他在Chorus平台上创建的一个开放智能体平台（过去3个月开发）。你可以通过iMessage、Slack等渠道直接与它交互。智能体免费试用，拥有所有最佳模型。例如，你可以发短信“Hello, Riley agent. What skills do you have?”它就会回复技能列表；你也可以用`/model`切换模型。Riley欢迎大家反馈，链接在视频描述中。

（介绍完后，他继续进入第二个技能。）

## 工作流二：把任何创作者变成可调用的“技能”

在同一个聊天中，Riley使用`Whisper Flow`进一步挖掘Callaway的数据：

> 他要求系统：找出Callaway频道中除赞助内容外互动率最高的10个视频，更新到数据库，然后将这些最佳表现视频转化为一个名为“Callaway top performing”的技能。这样任何时候想用Callaway的风格写内容，只需调用这个技能即可。

系统开始工作，它过滤掉赞助帖子（因为付费推广的互动不真实），扫描到2023年的历史数据。最终找到了很多拥有上千评论的爆款视频，并创建了技能。

接着Riley新建了一个聊天，输入“Callaway top performing”并发出写作任务：

> “为Anthropic发布的J-Space新闻制作脚本。Callaway擅长把复杂事情解释得简单又紧迫。请按他的风格写出三个选项。”

瞬间，系统生成了类似Callaway风格的钩子：“Anthropic just found a hidden workspace inside Claude's brain.” 以及“Anthropic created something close to a lie detector for AI. It's called J‑Lens.” 三个选项都非常精准。Riley表示，就像这样，你可以把任意创作者的风格做成技能，随时调用。

## 工作流三：刮取竞争对手广告（Foreplay API + Paper + Firecrawl）

第三个核心技能是**利用Foreplay API刮取广告**。Foreplay是一个工具，可以搜刮所有历史广告。Riley演示了如何获取竞品（[Quill](https://Quill.ai)、Perplexity、ChatGPT、Replit）的长期运行广告：

> 他要求：“请刮取我竞争对手中运行时间最长的广告。用Ads库，获取视频和静态图片，放入Notion数据库，并为每个广告写一段分析文字，解释它们为什么奏效。每个竞品取前5个视频广告和前5个静态广告，仅限英文。”

由于任务包含大量分析和模式识别，Riley将模型调至“extra high”。任务用了10分钟完成。结果是一个完整的数据库，包含广告创意、CTA（如“注册”或“安装应用”）以及AI生成的分析评论。例如，“这个生日主题的促销让优惠显得更像庆祝而非降价”。

### 额外即兴流程：用Paper和Firecrawl进行视觉化广告优化

Riley突发奇想，进一步优化工作流：他让Codex使用`paper MCP`技能把所有静态广告放入一个类似Figma的在线设计板“Paper”中。瞬间，Codex控制Paper创建了一个包含20个静态广告的看板（Perplexity、Claude、ChatGPT、Replit各5个）。

接着，他用`firecrawl`技能刮取自家产品Chorus（一个AI智能体平台）的完整着陆页，并将所有页面元素和资源库也放入Paper。于是Paper上有了竞品广告区、Chorus网站参考区和Chorus素材库。

然后，他手动把Chorus的Logo、文字标志等拉到一个新区域，并让AI生成与竞品广告风格类似但品牌替换为Chorus的新广告：

- 选择Replet的广告模板，让AI保留构图，但Logo换成Chorus，文案改为“Built a $100,000 agent for $50. Built with Chorus.”
- AI使用OpenAI的Image 2生成了多个变体。Riley强调：我们并不会完全照搬，但这种方法能快速获得大量创意方向，让你可以低成本大量测试广告素材。

Riley说，这是一个非常实用且有趣的工作流，而且他是刚刚才想到连起来的。他希望观众能尝试并反馈。

## 工作流四：自动社交媒体排程（Buffer Publisher）

第四个技能是**用Buffer发布社交媒体帖子**。Riley将刚才在Paper上生成的Chorus广告图片直接粘贴，要求“在Buffer上把它排成Instagram和LinkedIn的帖子。并使用前期刮取的Greg Eisenberg的文案风格来写标题。”

系统调用`scrape creators`技能找到Greg的Instagram字幕风格，然后生成了如下帖子草稿：

> “A doctor built a $100,000 AI agent for $50. 😱”

然后通过Buffer API创建了草稿，Riley可以选择直接发布或稍后修改。同样，也可以使用Typefully专注管理Twitter账号，支持多账号排期。

## 工作流五：组织Google Drive（Agent Native Drive）

第五个非常实用但不太炫酷的技能是**管理Google Drive**。Riley有一个名为“agent native drive”的技能，它包含一份指导文档，告诉AI如何理解文件夹结构和命名习惯（例如按项目分块的视频文件夹）。

他演示：假设两个月后要和Gary Vee做播客，只需告诉Codex：

> “请为Gary Vee创建一个文件夹，并在其中创建一个视频文档，编写一个钩子（参考此文件夹下其他先例），然后列出几个可问Gary的问题，并给出所有文件的链接。”

系统在50秒内就完成了，创建了文件夹和文档，生成了一个简短的钩子，并提供了可直接打开链接。此外，Riley预先在技能中设定了：每次创建或编辑文件时，必须返回链接。

## 工作流六：灵活的日历链接发送（Cal.com）

第六个是高杠杆技能——**通过Cal.com发送智能日历链接**。Cal.com在Codex中没有官方插件，但只需获得API Key，然后让Codex创建一个“能完全控制Cal.com”的技能即可，一分钟就能搞定。

Riley以邀请Shaquille O’Neal为例：

> “我要邀请Shaq来聊AI。我需要时间准备，所以只开放9月和10月的周二/周四时间段。请为我创建一个专属日历链接，并在信件中附上链接，同时撰写一个标准的邀请邮件草稿。”

Codex自动生成了一个自定义Calendly链接（仅含9月和10月），并写好了邮件草稿，包含主题“Agent Native播客”和正文。Riley还强调，如果使用Calendly或Cal.com，都可以通过类似方法直接控制。

## 工作流七：高效邮件草稿（Email Drafts + 批量处理）

最后一个技能，也是Riley认为最实用的：**用Codex生成Gmail草稿**。它不仅能创建单封草稿，还能批量处理邮件。

### 单封邮件：给Shaq的邀请

延续上面的例子，Riley要求系统找到Shaq最合适的联系邮箱（系统找到了他合作媒体集团的公关负责人），然后直接在Gmail中生成草稿，返回一个链接。点击链接即可在浏览器中打开并发送。

### 批量响应：拒绝推广并反推自家产品

Riley进一步展示批量功能：

> “请找出过去两个月所有向我推荐产品、问我‘想试试吗’的邮件。对每个人礼貌地拒绝，但附带一句‘不过，你想试试我们的产品吗？’并附上我们的产品链接。请为这些邮件都生成Gmail草稿链接。”

系统扫描邮箱后，生成了5封草稿。Riley打开其中一封，发现AI写道：“Talia看起来不错，但我这次先不试了。那么，主角反转：要不你试试我们的产品？”等非常自然的语句。他评价说，虽然有些语句可能需微调，但整体节省了大量时间。尤其对于需要频繁联系创作者的营销人，可以批量个性化发送“我看了你的内容，特此邀请合作”的邮件。

### 记忆与持续改进

Riley强调，智能体可以记住你的偏好，如果你发现它反复犯同一错误，只需告诉它“更新邮件草稿技能，以后不要做XX”，它就会改进。

## 总结：九个被浓缩的核心技能

Riley与Vashall回顾了今天涉及的所有技能：

1. **刮取所有社交平台的创作者内容**（Scrape Creators）
2. **将创作者转化为可复用的内容技能**（Turn Creator into Skill）
3. **刮取竞争对手广告**（Foreplay API）
   - 其中包含了 **Firecrawl**（完整网页刮取）和 **Paper**（视觉化排版工具）的即席组合
4. **社交媒体自动排程**（Buffer Publisher / Typefully）
5. **Google Drive 文件组织与自动化**（Agent Native Drive）
6. **智能日历链接发送**（Cal.com / Calendly）
7. **Gmail 邮件草稿与批量处理**（Email Drafts）

Riley问Vashall哪个最有用，Vashall认为第3/4/5的组合（内容创作循环）威力很大，但也承认第1~5串起来几乎能覆盖所有内容操作；而第6~7则侧重于运营效率。总之，这些技能覆盖了营销的创意与执行两端。

最后，Riley再次提示：所有技能都在视频描述中，欢迎尝试并分享反馈。至此，完整的九个营销工作流演示结束。

---

*（全文基于 Riley Brown 原视频文稿整理，保留全部原始信息，仅调整结构以提升可读性。所有专有工具名、模型名等保留英文，首次出现时附中文说明。）*
