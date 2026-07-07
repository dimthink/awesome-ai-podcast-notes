---
title: "Claude Fable 5 Just Changed Design Forever"
channel: "Riley Brown"
published: "2026-07-06"
source_url: "https://www.youtube.com/watch?v=COh_cjrDOzc"
video_id: "COh_cjrDOzc"
tags: ["AI", "设计自动化", "Claude Code", "Fable 5", "Paper"]
rating: 4
language: "英文"
word_count: 11753
duration: "23:59"
---

# Claude Fable 5 Just Changed Design Forever

- **Channel:** Riley Brown
- **Published:** 2026-07-06
- **Source:** https://www.youtube.com/watch?v=COh_cjrDOzc
- **TL;DR:** AI 代理 Fable 5 + Claude Code + Paper 实现从缩略图到网站的全自动化设计，工作流效率提升百倍
- **Tags:** AI, 设计自动化, Claude Code, Fable 5, Paper
- **Rating:** 4

## 版本

- [结构化文稿](2026-07-06-claude-fable-5-just-changed-design-forever-COh_cjrDOzc.structured.md)
- [原始文稿](2026-07-06-claude-fable-5-just-changed-design-forever-COh_cjrDOzc.transcript.md)

# Claude Fable 5 Just Changed Design Forever

**材料信息**

- **标题**：Claude Fable 5 Just Changed Design Forever
- **作者/来源**：Riley Brown
- **类型**：YouTube 视频字幕
- **关键元数据**：视频发布于2024年；时长约15分钟；涉及工具：Claude Code、Fable 5（AI设计代理）、Paper（AI原生设计应用）；作者使用Fable 5约4-5天。

---

## 开篇引入

想象这样一个场景：你只需输入一段自然语言，一个 AI 代理就能在你的设计画布上实时创建演示文稿、社交媒体图形、甚至完整网站并部署上线。这不再是科幻概念，而是 YouTube 创作者 Riley Brown 在最新视频中真实展示的工作流。通过 Anthropic 的 Claude Code 与新兴设计代理 Fable 5 的结合，加上专为 AI 代理设计的画布应用 Paper，他构建了一个从灵感到交付全由 AI 驱动的设计系统。这篇文章将带你深入解析这个工作流的每一个环节，理解它为什么可能改变设计行业的底层逻辑，以及你如何能立即开始使用这些工具，将创意生成的速度推向极致。

---

## 详细内容

### 欢迎来到智能体设计新时代 `[转录：引言]`

**核心观点**  
Riley Brown 通过实时演示证明：AI 代理（Fable 5 + Claude Code）可以完全控制设计画布（Paper），自动完成从演示文稿到复杂图形的高质量创作，标志着设计范式从“手动操作工具”向“指挥智能代理”的转变。

**深度阐述**  
视频一开始就直接进入核心——Claude Code（Anthropic 的命令行编程代理）正在运行 Fable 5，而 Fable 5 正控制着一个名为 Paper 的类 Figma 画布应用。关键区别在于，Paper 是“agent-native”（代理原生）的，即其交互界面和底层架构都围绕 AI 代理而非人类操作设计。作者输入一个简单提示：“创建一个关于如何使用 Paper 的演示文稿”。接下来我们看到 AI 代理开始在画布上构建演示文稿：自动创建幻灯片、放置文本、生成图形，甚至从互联网抓取相关资产插入其中。他兴奋地指出：“Look at this. Fable 5 is literally designing this presentation right here.”（看这个，Fable 5 正在直接设计这个演示文稿）`[转录]`。

背后的技术流程是：Claude Code 通过 MCP（Model Context Protocol，模型上下文协议）服务器与 Paper 通信。Claude Code 理解用户的自然语言指令，将其转化为一系列设计操作，写入 Paper 的 MCP 服务器；Paper 实时渲染出界面。在这个过程中，Fable 5 扮演了“设计代理”的角色，负责具体的图形生成和布局决策（作者后来提到“Fable tokens”和设置不同 effort 级别，暗示 Fable 5 可能是运行在 Claude Code 上的专门模型或技能）。作者随后通过一个简洁的原理解释图（“Claude Code writes designs to the paper MCP server, reads context, passes to design file”）总结了这个架构。整个演示在几秒内完成，从空白画布到内容丰富的演示文稿。

**个人感受**  
Riley Brown 的兴奋感贯穿全片。他不断用感叹句和夸奖表达对工具能力的痴迷：“That was a really useful graphic actually.”（那真是一个非常有用的图形）`[转录]`。这种热情不是表演，而是亲身经历技术突破后的真实反应，他乐于分享每一个让他惊叹的瞬间。

**延伸思考**  
AI 代理控制设计工具的模式，可能从根本上重塑设计师的日常。传统上，设计师必须精通 Figma、Sketch 等复杂工具；现在，只要能用自然语言清晰描述需求，就能产出专业级设计。这意味着设计的“技术门槛”急剧降低，但“创意策划”和“提示工程”（prompt engineering）能力变得至关重要。同时，MCP 作为开放协议，标准化了 AI 与工具之间的交互，未来类似集成可能迅速扩展到视频编辑、3D 建模等领域，形成一个“通才 AI 代理 + 专业工具”的生态。

**精华收获**  
- AI 代理可以完全控制设计画布，从零开始构建复杂设计作品。  
- Claude Code、Fable 5、Paper 三者构成高效的设计自动化流水线。  
- 代理能联网获取资产，实现多媒体集成，远超静态模板生成。  
- 实时观察代理操作过程，用户可以及时干预和调整方向。

---

### 快速上手：设置 Paper 与 Claude Code 的连接 `[转录：设置 MCP]`

**核心观点**  
从安装 Paper 到建立 AI 代理与控制画布的连接，整个过程仅需几分钟：下载 Paper、获取 MCP 配置链接、在 Claude Code 中一句指令完成设置，然后通过测试确认连接成功。

**深度阐述**  
Riley 详细演示了初始设置步骤。首先，访问 paper.design 下载 Paper 桌面应用，它支持 Mac 和 Windows。安装完成后打开 Paper，界面底部有一个“using agents”（使用代理）的按钮，点击“get started”（开始），你会获得一个 MCP 配置链接，类似于 `paper.design/doccks/mcp`。作者强调：“you can just literally copy this link”（你可以直接复制这个链接）`[转录]`。

接下来，在 Claude 桌面应用中建立新对话（也支持 Cursor 等其他支持 MCP 的 AI 编程工具），输入以下提示：“I want to set up the MCP server to control my paper.design”，并粘贴链接。Claude 会自动解析并配置 MCP 连接，不需要手动编辑 JSON 文件或编写代码。配置完成后，作者建议立即测试。他在 Paper 上新建一个文件，命名为“Riley site”，并输入“hello”在画布上作为标记。在 Claude Code 中，他发出测试指令：“Hey there, cloud code. I want you to tell me what board do I have open on paper. Tell me the answer to that. And then I want you to create a single simple graphic just so I know that you can control my paper.design.”（嘿，Claude Code，我想让你告诉我我当前在 Paper 上打开了哪个板。告诉我答案，然后创建一个简单的图形，好让我知道你能控制我的 Paper.design。）`[转录]` 同时，他将 Fable 的 effort 设置为“low”，因为测试不需要高质量图形。运行后，Claude Code 识别出当前 board，创建了一个名为“Hello from Claude Code”的 frame，在 fram 内画了一条蓝色波浪线并写上“Hello, Riley”。测试无误，连接成功。作者评论：“it really is that easy.”（真的就这么简单）`[转录]`。

**个人感受**  
作者演示设置时语气轻松自信，强调流程的无缝性。测试成功后，他幽默地吐槽波浪线“Not quite sure why I did that, but that's kind of cute”（不太确定为什么它画了那个，但还挺可爱的），显示出对 AI 不可预测性的包容和幽默感。这种态度鼓励观众不要对 AI 的输出过分严苛，而是享受探索过程。

**延伸思考**  
MCP 是 Anthropic 推出的开放工具集成协议，目标是让 AI 代理以统一、安全的方式与外部软件交互。Paper 的案例展示了 MCP 在创意工具中的典型应用：代理可以读取画布状态（内容、位置、样式），并在画布上创建、修改、删除元素。这种“双向读写能力”是实现自动化设计的核心。随着更多工具（如 Webflow、Canva、Blender）支持 MCP，一个通用的“AI 控制层”正在形成，用户只需一种接口（自然语言）就能操控整个数字创作工具链。

**精华收获**  
- 下载 Paper 桌面应用，在设置中获取 MCP 链接。  
- 在 Claude Code 中用一句自然语言指令配置 MCP 服务器。  
- 通过“告诉我当前板的信息并画个图形”测试连接是否成功。  
- 整个过程无需编码，几分钟完成，极大降低上手门槛。

---

### 用例一：YouTube 缩略图——从灵感采集到智能混搭 `[转录：YT 缩略图]`

**核心观点**  
利用 Paper 内置的图像生成和 Claude Code 的采集技能，用户可以快速导入其他创作者的最优缩略图，通过 AI 替换人物、文字、背景，在数分钟内生成多个高质量概念版本，实现高效迭代。

**深度阐述**  
Riley 展示了 YouTube 缩略图创作的全新工作流。第一步，使用一个免费提供的技能“youtube-thumbnails”（作者将技能链接放在了视频描述中），让 Claude Code 从 YouTube 上抓取指定创作者的最佳缩略图。他指示：“I want you to find his 10 best thumbnails and actually his 12 best thumbnails and import them in a frame inside paper.”（我想让你找到他表现最好的 12 个缩略图，导入到 Paper 的一个 frame 里）`[转录]`。Claude Code 执行后，Paper 画布上出现了一个包含 12 个缩略图的精美网格，作为灵感板。

接着，他将自己的照片复制到画布上，与目标缩略图并排放置。选择目标缩略图后，通过 Paper 的 AI 图像编辑功能（点击图像后出现“replace this with...”的选项），用自然语言指示：“Replace the man, the guy holding the phone with this guy. Make the text say addicting apps. And on the phone it should be the same but with an app store icon.”（把这个拿手机的人换成这个人。把文字改成“Addicting Apps”。手机上的内容保持不变但添加一个 App Store 图标。）`[转录]` 运行后，Paper 生成多个版本，作者从中挑选最满意的。他特别展示了多参考图像编辑：选择目标图，按住 Shift 点击多个参考图（如自己的照片和三个图标），然后指示“replace the guy with the other guy, replace the icons with these three icons, change the text to You're Still Early”。代理理解多个参考的意图，生成对应的变体。虽然可能因光照不一致导致背景变暗，但通过追加提示“keep the same white background”可以快速修正。

作者总结工作流的优势：“I can just rapidly iterate. And I don't pull from other people's thumbnails all the time. Often times I'm using previous thumbnails.”（我可以快速迭代。我并不总是从别人那里取图，更多时候使用自己过去的缩略图。但这种方式让我能快速探索直到找到想要的概念。）`[转录]`

**个人感受**  
作者对这个工作流的热爱溢于言表，直言“I love this workflow.”（我爱这个工作流）`[转录]`。他提到过去曾与专业缩略图设计师合作，而现在他自己就能在短时间内生成大量概念，创作效率提升了几个量级。他特别高兴于工具的迭代速度：“of that just like seven different options to choose from”（一下就有七个不同选项可以选择）`[转录]`。

**延伸思考**  
这个用例体现了 AI 在“参考与合成”上的强大能力。创作者不再从空白画布出发，而是基于成功案例进行“改编”，这极大提升了创意起点。但这也引发版权伦理问题：使用他人缩略图作为生成基础是否构成衍生作品？除了意识问题，技术上已经可以指定使用自己的历史作品作为主参考，规避版权风险。另外，多参考同时编辑的能力表明 AI 能理解“保留部分元素、替换其他元素”的复合意图，这是传统模板工具无法实现的。

**精华收获**  
- “youtube-thumbnails”技能可快速批量导入目标创作者的最佳缩略图。  
- 选中目标图，用自然语言指示替换人物、图标、文字，AI 保留构图风格。  
- 多图像参考（多张照片+多个图标）可一次替换多个元素，复杂编辑一步到位。  
- 生成多个版本后，可以通过追加提示精修细节（如背景颜色）。  
- 迭代速度远超人工作业，极大扩展创意探索空间。

---

### 用例二：Instagram 图形——风格迁移与文本可编辑 `[转录：IG 图形]`

**核心观点**  
从一个参考 Instagram 图形出发，AI 代理能精确复刻其设计风格（渐变、布局），并应用到用户自己的照片上；生成结果中的文本是实时可编辑元素，而不是锁定图像，方便后期调整。整个过程支持多版本快速产出。

**深度阐述**  
Riley 首先从 Instagram 账号“wealth”截图了一个图形作为风格参考——其特点是黑色渐变背景，白色文字居中布局。他把自己的一张照片放在参考图旁边。然后在 Claude Code 中指示：“Please create an Instagram graphic of the man. … take the image of the guy and add the black gradient effect that you can see… and add the text overlay… white text, have it say Riley Brown.”（请创建这个人的 Instagram 图形。……用这个人的图像，加上你能看到的黑色渐变效果……添加文字覆盖……白色文字，内容写“Riley Brown”）`[转录]`。代理按照步骤操作：先放置照片，再叠加渐变，最后添加文本。作者实时看到进度，感到满意。

接着，他又要求生成另一个版本，使用不同的文字：“Please make another version that says ‘This is how you get Claude to control paper’ … and use one of the other images of me that I generated.”（请创建另一个版本，文字是“This is how you get Claude to control paper”……并使用我生成的其他图像）`[转录]`。为了精确指定图像，他利用 Paper 的“copy link”功能：右键图像获得一个唯一链接，在 Claude Code 中指示“please use this image for this”（请使用这个图像）`[转录]`。代理随后使用指定图像生成新版本。

作者进一步要求更复杂的指令：“Make a version with this one as well. Except come up with a few variations of the text. … change the paper like have paper be blue in the text and the Riley Brown be red same size and then make three more versions and use the other images that I’ve created.”（也写一个版本用这个图像。但文本做几种变体。……文字中的‘paper’用蓝色，‘Riley Brown’用红色，保持不变的大小，再生成三个版本，用我创建的其他图像。）`[转录]` 代理依言生成多个版本，颜色、文字和照片各不相同。

作者特别强调：“you can directly edit all of this text by the way… this is not generating an image where the text is an image where you have to edit it like you just edit it directly.”（你们可以直接编辑所有这些文字……这不是把文字当图像生成，你必须像这样直接编辑它）`[转录]`。这意味着生成后，用户可以随意点击并修改文字内容，字体、大小、颜色均可调整，无需重新生成整个图形。

**个人感受**  
作者感叹：“it's actually kind of hard to get this effect. I've tried to do this manually. It's kind of annoying. But here you can just ask for these graphics and you can basically do anything.”（这个效果其实挺难做到的。我试过手动做，很烦人。但在这里你只要说一下就能得到，基本什么都能做）`[转录]`。他对 AI 轻松解决过去棘手问题感到兴奋，称整个过程“so much fun”（太好玩了）。

**延伸思考**  
这个用例展示了“模板化创作”的终极形态：用户只需提供一个风格参考，AI 就能自动提取设计语言（渐变、排版、空间布局）并应用到新内容上。结合文本可编辑特性，创作者可以建立一套品牌模板，每次只需更换照片和文字，就能批量生成风格一致的社交媒体内容。这是内容创作者梦寐以求的“生产资料”：从一次设计到无限复用。但风险是容易导致视觉同质化，需要人为增加差异点（如不同的渐变颜色、补充图形元素）。

**精华收获**  
- 通过参考图引导 AI 复刻完整设计风格（精确到渐变效果和文字样式）。  
- 使用“copy link”指定特定图像，可精细控制代理使用的资产。  
- 生成的图形文本是原生可编辑元素（非图像），支持后续直接修改。  
- 可要求生成多个文字/布局变体，一次获得大量候选内容。  
- 这个工作流解决了手动叠加渐变等烦琐操作，效率显著提升。

---

### 用例三：演示文稿与网站——从照片到互联网的全自动发布 `[转录：演示文稿与网站]`

**核心观点**  
在同一个 Paper 画布上，将多张照片组合成一个框架，一个提示即可生成完整演示文稿；接着在同一对话中，要求基于该文稿创建响应式网站并部署到 Vercel，实现从灵感物料到可公开访问网站的全自动化。

**深度阐述**  
Riley 继续使用之前的画布，现在准备创建演示文稿。他将在用例二中已经生成的多张个人照片放入一个框架（frame），并命名为“photos of me”，这样代理可以整体引用。他将 Fable 的 effort 调为“high”，然后向 Claude Code 发出详细指示：“create a six slide high quality pitch deck... pitching on my creator business... I want this brand to look like Perplexity... keep it simple, don't have footers, crisp headers, cool graphics, explain things simply... each one of the slide should have one of these images of me on it.”（创建一个六页的高质量 pitch deck……推演我的创作者业务……我希望品牌风格像 Perplexity……保持简洁，不要页脚，清晰的标题，酷的图形，简单解释……每一页放一张我的这些图像）`[转录]`。

代理开始构建。它使用了一个“scraper skill”（抓取技能），该技能通过 Firecrawl API 搜索互联网，自动提取指定品牌（Perplexity）的视觉风格（颜色、字体），并应用到演示文稿中。过程中，作者发现第一版有些文字覆盖在图像上，立刻叫停：“you have some text over the image, so don't do that again.”（文字覆盖了图像，不要再这么做）`[转录]`。代理听从反馈并调整。最终生成的演示文稿每一页使用不同照片，配色干净（白色和蓝色），内容扎根于作者的业务领域。作者赞许：“I love decks like these. I do not like it when they make it cluttered.”（我喜欢这样的 deck，不喜欢做得拥挤杂乱的）`[转录]`。

然而，演示还没有结束。在同一对话中，作者进一步指示：“create a website, a landing page that's optimized for web and mobile that allows people to just see Riley Brown at the top... below it it has like one cool line and beneath it, it has the slide deck where people can toggle which slide... deploy it to Vercel and send me the link.”（创建一个网站，一个优化了网页和移动端的落地页……顶部显示‘Riley Brown’，下方有一句酷的文字，再下面是幻灯片，用户可以切换……部署到 Vercel 并把链接发给我）`[转录]`。代理依言构建了一个响应式网站，将幻灯片嵌入为可切换的轮播组件，并成功推送到 Vercel 上线。作者打开链接 `rile-sponsor-site.cell.app`，看到完整的幻灯片在网页中流畅运行，体验良好。

**个人感受**  
作者看到最终网站时发出惊叹：“I like this more than my existing website. So, I might use this.”（这个比我现在的网站还好看，我可能会用它）`[转录]`。从几张照片到可以分享给赞助商的完整网站，全程通过自然语言完成，这种速度和完整性让他自己都感到不可思议。

**延伸思考**  
这个用例将“设计生产”推向了极致：它模糊了设计、开发、部署的边界。以往个人创建演示文稿需要 Keynote/PPT，转化为网站则需要前端开发者。现在，创作者可以直接用自然语言要求代理完成整个流程。对于自由职业者、初创公司、内容创作者，这可能意味着“一人公司”的技术栈——一个精通提示工程的人可以独立完成以前需要一个多角色团队的工作。当然，这也意味着对 AI 输出质量的更高要求，以及对品牌一致性的仔细审查。不过，随着技术的成熟，这很可能会成为内容生产的新标准。

**精华收获**  
- 将相关素材放入框架（frame）并命名，方便代理整体引用。  
- 通过天然语言指定品牌风格（如“像 Perplexity”），代理能从互联网自动采集并应用设计语言。  
- 用户在生成过程中可以实时纠正问题（如文字覆盖），人机协同完善作品。  
- 基于同一个对话无缝衔接：从演示文稿到网站再到部署，一步到位。  
- 直接获得可分享的互联网链接，完成从创意到交付的闭环。

---

### 总结：拥抱 AI 驱动的设计未来 `[转录：结论]`

**核心观点**  
Riley Brown 通过 YouTube 缩略图、Instagram 图形和演示文稿/网站三个真实用例，展示了 AI 代理（Fable 5 + Claude Code + Paper）如何显著加速设计工作流，从几天的工作量压缩到几分钟。他鼓励观众立即开始尝试，并承诺将持续分享进阶使用。

**深度阐述**  
视频结尾，作者回顾了演示的核心功能：你可以直接指示 Claude Fable 创建一个图形，它就会出现在 Paper 画布上，包括缩略图、社交媒体图片、演示文稿和网站。他提醒使用 Claude Code 操作 Paper 会消耗积分（可能是 Anthropic 的使用额度或 Fable token），当使用量增加后会出现收费。但他明确表态：“This video is not sponsored by Claude, nor is it sponsored by paper. I just really genuinely use these tools a lot especially for thumbnails and Instagram graphics.”（这个视频不是 Claude 赞助的，也不是 Paper 赞助的。我只是真心并大量使用这些工具，尤其是缩略图和 Instagram 图形）`[转录]`。他坦诚自己只使用 Fable 5 大约四到五天，仍在学习阶段，因此视频只是早期实践分享。他承诺未来会随着工作流成熟，分享更多进阶技巧。

**个人感受**  
作者在结尾的真诚令人好感顿生。他没有包装自己是专家，而是以“早期用户”的身份分享新鲜体验。这种谦逊和热情在技术圈里尤其珍贵——他不是在推销，而是在邀请别人一起探索一个激动人心的新领域。

**延伸思考**  
Riley Brown 的视频和本文重构的内容，清晰地展示了一个正在发生的变革：设计从“操作工具”走向“指挥代理”。虽然当前工具还有不稳定之处（如偶尔色彩偏移、需要人工纠正），但其潜力已经足够让人震撼。可以预见，未来数月将涌现大量基于相似模式的工作流和技能生态。设计师的核心竞争力将不再是软件熟练度，而是“创意方向”和“提示设计（prompt design）”的能力。同时，这些工具将设计民主化，让没有接受过正式设计训练的人也能产出专业级作品。

**精华收获**  
- 现在就可以开始使用 Paper + Claude Code + Fable 5 组合进行实战设计。  
- 技能（Skills）是扩展代理设计能力的核心，社区应积极贡献新技能。  
- 工作流已可实际应用于内容生产，但仍需要人类在关键环节把关和调整。  
- 早期使用者可以显著领先于行业，但要保持对工具迭代速度的跟进。  
- 这个范式变革才刚刚开始，拥抱它的人将定义下一代设计方式。

---

<!-- TLDR: AI 代理 Fable 5 + Claude Code + Paper 实现从缩略图到网站的全自动化设计，工作流效率提升百倍 -->
<!-- TAGS: AI, 设计自动化, Claude Code, Fable 5, Paper -->
<!-- RATING: 4 -->
