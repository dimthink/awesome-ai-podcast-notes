---
title: "Devin AI: The Full Beginner’s Guide (Better Than Claude Code?)"
channel: "Riley Brown"
published: "2026-07-16"
source_url: "https://www.youtube.com/watch?v=Vyyrvna-hUY"
video_id: "Vyyrvna-hUY"
tags: ["AI", "无代码开发", "Devin", "营销自动化", "产品验证"]
rating: 4
language: "英文"
word_count: 11530
duration: "24:47"
---

# Devin AI: The Full Beginner’s Guide (Better Than Claude Code?)

- **Channel:** Riley Brown
- **Published:** 2026-07-16
- **Source:** https://www.youtube.com/watch?v=Vyyrvna-hUY
- **TL;DR:** Devin 让非程序员通过自然语言管理 AI 代理舰队，从着陆页到营销仪表板全功能应用一小时上线。
- **Tags:** AI, 无代码开发, Devin, 营销自动化, 产品验证
- **Rating:** 4

## 版本

- [结构化文稿](2026-07-16-devin-ai-the-full-beginner’s-guide-(better-than-claude-code-)-Vyyrvna-hUY.structured.md)
- [原始文稿](2026-07-16-devin-ai-the-full-beginner’s-guide-(better-than-claude-code-)-Vyyrvna-hUY.transcript.md)

# 材料信息
- **标题**：Devin AI: The Full Beginner’s Guide (Better Than Claude Code?)  
- **作者/来源**：Riley Brown（YouTube 频道）  
- **类型**：YouTube 视频字幕  
- **关键元数据**：无确切时长，内容围绕一次从零到部署的完整实战演示，覆盖 AI 驱动应用开发的完整流程  

---

# 开篇引入

想象这样一个场景：你有一个绝妙的商业构想——一个能自动收集客户信息、动态生成 PDF、并用实时数据仪表板展示营销成果的网站。但你不是程序员，一行代码都写不出来。按照以往的逻辑，这个想法只能停留在 PPT 里，或者你需要花大价钱去雇佣开发团队。然而，如果你有一台电脑，以及一个叫 Devin 的 AI 代码编辑器，这个构想就能在几十分钟内变成真正上线运行的产品。这就是 Riley Brown 在这段视频中展现的现实：一个从未写过代码的人，利用 Devin 的 AI 代理舰队，搭建了专业级个人落地页、配置了带数据库的铅磁铁（Lead Magnet）、生成动态 PDF，最后还做出一个全功能营销仪表板，并成功部署到公网。整个过程令人瞠目——不仅因为工具的强大，更因为它揭示了一个正在迫近的未来：软件开发正在从“编码”走向“委托与引导”。今天我们深度拆解这段演示，不只是还原每个操作步骤，更要去理解其中的思维范式——如何与 AI 沟通、如何分解任务、如何集成生态，以及这种新生产方式对你（无论你是技术背景还是纯业务背景）意味着什么。

---

# 详细内容

---

### 1. Devin 究竟是什么？ — 不只是代码编辑器，而是 AI 代理舰队 `[视频开场]`

**核心观点**  
Devin 是一个以多模型、多代理为核心的 AI 开发环境，允许用户用自然语言同时驱动多个代理完成不同任务，所有过程无需手写代码。

**深度阐述**  
Riley 的开场白直接定义了 Devin 的野心：“This is the complete guide to using Devin, an AI code editor that has access to every frontier model in the world.” 这不仅仅是一个代码补全工具，而是一个可以调用全球最前沿模型的平台——包括内置的 SW 1.7、Claude Fable 5、GPT 5.6 Luna，甚至开源模型。用户只需在输入框中打下一个想法，比如“landing page for Riley, search rileybrown.xyz, make a better version”，AI 就会自动去构思、编写、调试，最终生成可运行的应用程序。

但让 Devin 真正区别于其他 AI 助手的，是它的“会话（Sessions）”机制——一个类似于看板（Kanban board）的界面，用户可以同时启动多个 AI 代理，每个代理独立工作，彼此协作。Riley 说：“Devin not only allows me to just ask an agent to build an app, it actually allows me to ask a fleet of agents to do many tasks on many apps.” 这意味着你可以分配一个代理去构建着陆页，另一个去配置数据库，第三个去生成报表——就像管理一支小型开发团队，而所有“成员”都是 AI。这种“多代理并行”的架构，让个人能力被显著放大。

**个人感受**  
Riley 坦诚地透露自己的背景：“I have never written a single line of code.” 他说自己完全不写代码，但凭借 Devin 管理着 5 个个人应用、2 个有付费用户的产品，甚至在 GitHub 上拥有 139 个仓库。这段话充满了自豪与震撼，它向观众传递了一个强烈的信号：技术壁垒正在被打破，任何能够清晰表达需求的人，都可以成为“应用创造者”。

**延伸思考**  
多代理协作的模式可能重新定义软件工程的角色。未来的“开发者”不再需要精通语法，而需要精通“任务分解”和“提示工程”——能准确描述目标、设定边界、串联多个 AI 服务。这种“管理式创造”一旦成熟，软件开发的效率曲线将出现指数级跃升。

**精华收获**  
- Devin 不是一个只能写代码的工具，而是一个“AI 代理工作流平台”。  
- 多个代理可以并行工作，用户只需在会话面板监控和调度。  
- 即使没有任何编程背景，也可以利用 Devin 构建真实可用的产品。

---

### 2. 准备工作：下载、GitHub 与生态系统连接 `[设置阶段]`

**核心观点**  
开始使用 Devin 只需要下载客户端、用 GitHub 登录，并连接 Vercel（部署平台）和 Supabase（数据库），所有服务都有免费的入门方案。

**深度阐述**  
Riley 的步骤极其简洁：访问 devin.ai，下载对应客户端（Mac / Windows 均可）。安装后，最关键的一步是使用 GitHub 账号登录。“I think it’s incredibly important that you create a GitHub account and you attach your GitHub account to Devin。”GitHub 不仅是代码仓库，更是开发者身份的锚点——通过它，Devin 可以管理项目版本、备份代码。

接下来，他展示了 Devin 内置的“Open MCP Marketplace”。MCP（Model Context Protocol）是 Deutero 生态中的集成协议，让 AI 代理可以直接调用外部服务。他先后安装了 Vercel 和 Supabase 两个插件。Vercel 用于将应用部署到互联网，Supabase 作为数据库存储用户提交的数据。这两个插件的安装只需要点几下按钮，再在对应服务中生成 API token 并粘贴到 Devin 即可。Riley 反复强调：“Vercel is free to set up”，“Supabase is free to get started。” 整个生态的入门成本几乎为零，但提供了专业级的基础设施。

**个人感受**  
Riley 的语气里透着一股“这太简单了”的轻松感。他没有进入任何复杂的配置界面，甚至没有手动创建数据库表——所有的繁重工作都交给了 AI 代理。这种“即插即用”的体验，让人感觉像是在搭配乐高积木。

**延伸思考**  
这一步骤揭示了“AI 原生开发”的一个重要特征：集成能力成为核心技能。用户不必理解 HTTP 协议或 SQL 语法，只需要知道“我需要一个数据库”和“我需要一个部署平台”，剩下的细节由 AI 代理与 API 自动协商完成。未来的平台竞争，可能不是模型能力的竞争，而是生态整合度的竞争。

**精华收获**  
- Devin 通过与 Vercel 和 Supabase 的原生集成，实现了“存储 + 部署”的一站式能力。  
- 所有依赖服务都有免费入门方案，降低了尝试门槛。  
- 配置过程无需手写一行配置代码，仅需复制粘贴 API token。

---

### 3. 构建着陆页：从一句话指令到本地预览 `[核心演示：着陆页]`

**核心观点**  
通过一条自然语言指令，Devin 在几分钟内生成了一个包含图片、文案、按钮的专业着陆页，并运行在本地服务器上。

**深度阐述**  
Riley 打开 Devin 的“Agents”视图，输入了他的第一个主要指令：“Create a very beautiful personal landing page for me, Riley Brown. Search me on the internet and create a beautiful landing page that we’re going to build over the next few minutes, and we’re going to make it amazing. Please build it, then run it locally.” 这条指令包含了对个人身份的描述、对设计质量的要求、以及对运行方式的要求。Devin 启动了一个代理，开始执行任务。

几十秒到几分钟后，Devin 完成了工作。界面右侧是自动生成的代码（Riley 建议可以完全忽略它），左侧则是本地预览——一个浏览器窗口，显示着陆页已经可以访问。此时页面只在 Riley 的电脑上运行（localhost），但他可以随时查看效果。

随后 Riley 开始迭代：他在 Downloads 文件夹中放入了两张图片——一张是自己的照片（去掉背景），另一张是风格参考图。他告诉 Devin 使用这些图片更新页面，并调整整体风格。Devin 接收指令后，自动识别了本地文件并应用到正在运行的项目中。Riley 还使用截图功能，把页面上不喜欢的内容框选出来，粘贴到 Devin 的对话框里，加上文字：“Please fix it.” AI 随即进行了修改。这种“截图 + 文字描述”的交互方式，极大降低了沟通成本。

**个人感受**  
Riley 在演示过程中的兴奋溢于言表：“Look at this. Riley Brown, AI agents for creators, get the guide.” 他像一个艺术家在审视自己的作品，而不是一个程序员在调试代码。他关心的不是语法错误，而是“这个字体我不喜欢”、“这个颜色太丑了”。这种基于视觉反馈的迭代方式，非常符合非技术人员的直觉。

**延伸思考**  
这个环节展示了 AI 开发与传统开发最本质的区别：沟通方式从“编程语言”转向了“自然语言+视觉反馈”。未来设计的迭代速度将不再受限于修改代码的时间，而取决于你描述问题的清晰度。这也意味着，产品经理和设计师的个人审美判断力变得更加重要——因为 AI 可以快速执行，但方向需要人来把控。

**精华收获**  
- 用一句话就能生成完整的着陆页并本地运行。  
- 通过“本地文件引用”和“截图粘贴”可以快速修改设计。  
- 关注视觉结果，忽略代码细节，让非技术人员也能随心所欲地调整界面。

---

### 4. 铅磁铁 + 数据库：实现用户信息采集闭环 `[核心演示：数据收集]`

**核心观点**  
通过 Supabase 集成，Devin 自动创建数据库表，用户填写表单后数据被实时存储，且可以通过同一个应用内的密码保护仪表板访问。

**深度阐述**  
Riley 为他的产品构想“Agent Tree”（一个类似 Linktree 但用于 AI 技能的市场）设计了一个铅磁铁：一份免费的 PDF《How to Monetize Your Agent Skills》。他的目标很明确——用户在着陆页上点击按钮，填写姓名、邮箱、最大粉丝平台等字段，然后才能下载 PDF。这些信息必须被存储起来，以便未来的营销转化。

他首先让 Devin 创建了表单页面（PDF 下载页），但暂时没有连接数据库。然后他回到 Devin，添加了一条关键指令：“Please store all of this in a database using Supabase. And I want you to do this in such a way that we could create an admin dashboard that’s only accessible via password on this site.” 这意味着他要求 AI 自动完成三件事：创建数据库表、配置写入逻辑、设置密码保护的管理入口。

由于之前已经安装了 Supabase 插件，Devin 可以直接调用相关工具。Riley 甚至不需要手动去 Supabase 后台建表——Devin 自主完成了这一切。在后续测试中，Riley 在落地页上填写自己的信息（Riley Brown, riley@email.com, 10,000 粉丝, favorite platform: TikTok），点击提交后，他在 Supabase 的 table editor 中看到了刚录入的数据，表名为“guide_leads”。这证明数据库集成完全正常。

**个人感受**  
Riley 在验证数据成功存储时，语气里有种“果然如此”的满足感。他提到：“This is exactly what we just entered right here. We entered this, and we were able to successfully enter this in.” 对他来说，这不是理所当然的，而是一个值得庆祝的小里程碑——没有接触过数据库配置的人，通过几句自然语言就完成了后端搭建。

**延伸思考**  
很多业务人员最头疼的就是“后端逻辑”——如何存储、如何保护、如何查询。Devin + Supabase 的组合把这一切抽象成了“集成”和“指令”。未来的营销工具可能不再是购买 SaaS 产品，而是通过 AI 快速搭建一套完全定制的潜在客户管理系统。这不仅节省成本，还让数据所有权完全归自己。

**精华收获**  
- 数据库集成通过插件完成，不需要手动写 SQL 或配置连接。  
- AI 可以根据指令自动创建表结构，并确保前端表单与后端数据链路畅通。  
- 通过一条指令就实现了“密码保护”的管理权限控制。

---

### 5. 动态 PDF 生成：用户提交后秒获资料 `[核心演示：PDF分发]`

**核心观点**  
用户提交表单后，Devin 创建了一套带有交互动画的 PDF 生成与下载流程，用户能立即获得一份设计完整的指南。

**深度阐述**  
验证数据库正常工作后，Riley 要求 Devin 实现在线 PDF 生成：“Just create a PDF, take all the information that you know, make a PDF that after someone enters and says send me the free guide, it does like a cool animation, and then it shows the guide, and it says download now, and I click download, and it actually downloads to my computer, and there’s like a PDF that I can see.” 这条指令明确了交互细节：动画过渡 → 显示内容 → 下载触发 → PDF 落地到本地。

Devin 执行后，Riley 用新用户“Tim Johnson”进行了测试。他填写表单，点击“Send me the free guide”，页面出现“Download now”按钮，点击后一个 PDF 文件被保存到桌面。Riley 打开 PDF，评价道：“It’s okay that it’s not amazing. I do like this yellow. It’s very noticeable.” 他承认设计上并不惊艳，但功能完整可用。更重要的是，这个 PDF 是动态生成的，内容可以随模板变化，而不是一份静态文件。

**个人感受**  
Riley 对 PDF 的平淡反应反而很有价值——他并没有过度美化，而是实事求是地接受“初期版本不够精美，但可工作”。这种态度很务实：在快速验证阶段，功能优先于像素完美。他之后用同样的流程录入第二条数据，并验证了数据库增加了对应记录，说明整个“提交 → 存储 → 反馈”的闭环已经打通。

**延伸思考**  
动态 PDF 生成看似是个小功能，但它代表了一类重要的“营销自动化”场景。传统模式下，你需要开发团队编写后端 PDF 生成逻辑、配置 CDN 存储、处理下载请求。在 Devin 的世界里，你只需要说“生产一个 PDF，让人能下载”。这种能力的平民化，会让中小企业和个人创作者在营销物料分发上与大型公司站在同一起跑线上。

**精华收获**  
- AI 可以设计并生成可下载的 PDF 文件，支持动态内容。  
- 交互体验（动画、按钮）由 AI 自动实现，无需前端开发。  
- 即使生成的文件在美观上还有优化空间，但功能闭环已经形成，足以用于产品验证。

---

### 6. 全功能营销仪表板：数据可视化的终极呈现 `[核心演示：仪表板]`

**核心观点**  
Devin 基于数据库中的真实数据（含 115 条模拟数据）构建了一个带图表、筛选、搜索和导出功能的专业级仪表板，且随着新数据录入实时更新。

**深度阐述**  
Riley 进入仪表板页面（密码 3694 登录）时，里面还是空的。他发出了整个视频中最大胆的指令：“I want you to create the best dashboard ever for this. But I need you to create a ton of mock data. … I want you to make the best possible dashboard you could possibly think of for this data. And then I want you to add 115 entries to this.” 他不仅要求构建界面，还要求 AI 自动生成 115 条模拟记录来填充仪表板，以便直观地展示数据分析能力。

Devin 开始工作。Riley 同时要求修改一个字段名，将“favorite platform”改为“platform with most followers”，说明他意识到原字段设计的语义偏差——对于一个营销仪表板，“最喜欢的平台”远不如“最大关注者平台”有意义。Dev在生成过程中，数据被批量插入 Supabase。最终，仪表板呈现在面前时，Riley 惊叹：“I mean, look at this. So creator reach tiers nano, micro, mid-tier, and macro. Creator hotspot Seattle, Atlanta, Paris, Dallas, Phoenix, London. Highest reach Miles Taylor with 1.9. Submission momentum, the biggest platform. We can select creators. We can see all of them. We have analytics.”

整个仪表板包含：创作者分层（按影响力分为纳米/微小/中端/宏观）、创作者地理热点、最高触及率、提交趋势（Submission Momentum）、最大平台分布等模块。深度的交互功能——选择特定创作者查看详情、搜索、甚至导出数据——全部由 AI 自主设计实现。

Riley 随后现场提交了一条新数据（Jack Ripper, 4 million followers），仪表板立刻显示更新，验证了实时数据流。

**个人感受**  
这一段 Riley 的激动是最不加掩饰的。当看到仪表板从无到有、从空到丰富时，他的语调明显升高，语气中充满了惊喜与自豪。他说：“It even has export functionality which is really awesome.” 这超出了他最初的期待——他并没有要求导出功能，但 AI 主动添加了。这种“惊喜”恰恰体现了 AI 驱动的开发中，工具可能提供超出预期的增值功能。

**延伸思考**  
这个仪表板案例的价值远超演示本身。它揭示了“AI 应用开发”的一个核心优势：AI 可以基于上下文自动挖掘功能需求。当数据库中有用户信息和平台数据时，AI 会自主联想出“地理分析、分层统计、排名”等常见商业智能功能。未来的“应用生成”可能不再需要详尽的功能清单，只需给出核心业务指标，AI 会自动补全最佳实践。

**精华收获**  
- AI 能从零构建多维度、交互式仪表板，包含图表、表格、筛选器。  
- 批量生成模拟数据是测试和展示仪表板的关键技能。  
- AI 可能会增加你没有要求但合理的高级功能（如导出），提升产品的完整性。

---

### 7. 部署上线：从本地到公网的一键发布 `[部署阶段]`

**核心观点**  
通过 GitHub 和 Vercel，Devin 自动将项目推送到仓库并部署上线，生成可被任何人访问的公网 URL。

**深度阐述**  
完成所有功能开发后，Riley 的最终目标是让项目走出本地电脑，成为真正的互联网应用。他下达指令：“Create a new project on GitHub. This should be called Riley land lead dash on GitHub, a new public repo. Then I want you to deploy this to Vercel so it’s on the internet.”

Devin 自动在 GitHub 上创建了一个公开仓库，推送所有代码，然后触发 Vercel 的部署流程——因为之前已经配置了 Vercel 集成，整个流程完全是自动的。

最终结果是一个可直接访问的 URL：Riley Land Lead Dash.vercel.app。Riley 在浏览器中打开，验证了着陆页、铅磁铁、仪表板全部功能正常工作。他甚至演示了在公网环境中输入新的测试数据，仪表板同样实时更新。这意味着整个项目已经从“本地玩具”变成了“生产级应用”。

Riley 总结道：“GitHub, you can think of is like the Google Drive for developers. And I can just keep my project there. And what it’s going to do is any every time that we update the project on GitHub, it’s also going to redeploy to Vercel. So, it’ll stay updated.”

**个人感受**  
Riley 在展示上线后的页面时，语气平静而笃定。他没有兴奋地跳起来，而是用一种“任务完成”的沉稳口吻说：“We are live on the internet.” 这种平静反而让人对工具的可靠性更有信心——部署不再是让人紧张的环节，而是一个标准化的末尾步骤。

**延伸思考**  
传统开发上线通常需要配置域名、服务器、CI/CD 流水线等复杂操作。在 Devin 的流程中，这一切被封装成了“Vercel 集成”和一句指令。未来，上线的门槛会持续降低，最终可能变成品牌商家的日常操作：像发布一条社交媒体帖子一样发布一个应用。

**精华收获**  
- 通过一条指令即可完成 GitHub 仓库创建和 Vercel 部署。  
- 每次更新代码到 GitHub 会自动触发重新部署，实现持续迭代。  
- 部署后的应用是真实的互联网应用，所有人可访问，功能不受限。

---

### 8. 总结：一人公司时代的开启 `[视频尾声]`

**核心观点**  
Devin 让非技术人员能够独立完成从想法到部署的完整应用创建，这标志着“一人公司”的生产力工具已经成熟。

**深度阐述**  
视频最后，Riley 再次强调自己的背景——“I have never written a single line of code”——并补充说他已经用 Devin 管理了多个真实项目，包括有付费用户的应用。他把 Devin 定位为“创造者工具”，并感谢赞助商，特别提到“I have had a blast using this tool, and I’ve really been enjoying their in-app browser. It’s way better than I thought it was since the last time I used the product.”

更重要的是，他分享了一个潜在的成功模式：先快速构建一个 MVP（最小可行产品）来验证市场需求，而不是先闭门造车做完整产品。他构建 Agent Tree 的过程就体现了这一哲学——先创建一个着陆页和铅磁铁，看有多少人感兴趣，再决定是否继续开发完整的平台。

**个人感受**  
Riley 的总结带有强烈的个人色彩：他不是一个点评工具的技术博主，而是一个真实使用这个工具创造了商业价值的实践者。他的那句“I have 139 repositories on GitHub”对他的听众来说是一种标竿——他用行动证明，没有代码技能也能在 GitHub 上留下自己的项目清单。

**延伸思考**  
当开发工具的易用性达到“自然语言即代码”的程度，创业的机会将被重新分配。拥有深刻行业洞察但缺乏技术资源的创业者，现在可以自己动手验证想法、搭建原型、甚至运营初期的产品。这可能会催生一个“超级个体创业者”时代，他们同时兼任产品经理、设计师、后端开发、运维——但实际都是在用自然语言与 AI 代理团队协作。

**精华收获**  
- 从零到部署的完整流程只需不到一小时，且不需要写代码。  
- 快速验证（MVP）是 AI 时代的显著优势——你可以用铅磁铁测试市场兴趣，再决定是否开发完善产品。  
- Devin 的核心能力不在于“写代码”，而在于“协调各种 AI 代理集成外部服务”完成端到端交付。

---

# 精华收获一览

1. **无需代码，但需要清晰的表达**：命令 AI 的关键是将业务需求转化为可执行的指令，包括视觉参考、功能逻辑、集成服务。
2. **多代理并行思维**：Devin 的会话面板允许同时运行多个 AI 代理，应该学会将大任务拆分给不同代理并行处理。
3. **生态集成是核心杠杆**：Vercel（部署）、Supabase（数据库）等 MCP 插件让复杂项目快速落地。
4. **迭代从界面反馈开始**：截图 + 描述比命令行更直观，适合非技术用户参与设计修改。
5. **测试数据驱动可视化**：生成模拟数据是展示仪表板价值的关键技巧。
6. **部署一体化**：GitHub + Vercel 的组合让上线和持续更新变得极其简单。
7. **验证优先**：用最小可行产品快速测试市场，再决定是否投入更多资源。

Devin 向我们展示了一个新的软件开发范式：你不是在 coding，你是在 directing——成为一个 AI 代理团队的导演。而这个角色，不再受限于你会不会写代码，只受限于你能不能想清楚自己要什么。

<!-- TLDR: Devin 让非程序员通过自然语言管理 AI 代理舰队，从着陆页到营销仪表板全功能应用一小时上线。 -->
<!-- TAGS: AI, 无代码开发, Devin, 营销自动化, 产品验证 -->
<!-- RATING: 4 -->
