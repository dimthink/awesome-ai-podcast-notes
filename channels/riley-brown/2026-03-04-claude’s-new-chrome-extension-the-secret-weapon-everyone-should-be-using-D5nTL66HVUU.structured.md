---
title: "Claude’s New Chrome Extension: The Secret Weapon Everyone Should be Using - 结构化文稿"
channel: "Riley Brown"
published: "2026-03-04"
source_url: "https://www.youtube.com/watch?v=D5nTL66HVUU"
video_id: "D5nTL66HVUU"
variant: "structured"
---

# Claude’s New Chrome Extension: The Secret Weapon Everyone Should be Using - 结构化文稿

- **Channel:** Riley Brown
- **Published:** 2026-03-04
- **Source:** https://www.youtube.com/watch?v=D5nTL66HVUU
- **Main:** [Claude’s New Chrome Extension: The Secret Weapon Everyone Should be Using](2026-03-04-claude’s-new-chrome-extension-the-secret-weapon-everyone-should-be-using-D5nTL66HVUU.md)

# Claude全新Chrome扩展：掌控浏览器的秘密武器

Anthropic刚刚发布了一款重磅产品——一个能让Claude完全控制你浏览器的Chrome扩展。许多人认为，它已经超越了OpenAI的Agentic浏览器和Perplexity的Comet。更令人兴奋的是，你还可以将它连接到Claude Code。

本文将完整记录我对这项新技术的首次实时测试，从基础功能到高级应用，带你一探究竟。

## 初见Claude Chrome扩展

### 安装与基本使用

这个扩展目前在Chrome商店的评分是2.8星，原因是早期版本只能配合之前的Claude模型使用，效果并不理想。但现在，Anthropic发布了新版本，可以访问其最强的Agentic模型——**Claude Opus 4.5**。

让我们看看它的实际表现。安装扩展后，我向它提出了一个简单的请求：

"请去Twitter上总结一下关于最新OpenAI模型的消息。"

扩展立刻给出了一个行动计划：

1. 首先导航到Twitter
1. 搜索关于最新OpenAI模型的消息
1. 查看搜索结果和相关推文
1. 总结找到的关键新闻和信息
批准计划后，浏览器边缘亮起了棕色的光，扩展开始执行任务。虽然过程中需要多次点击"允许"操作，但可以设置"始终允许当前网站"来简化流程。

很快，它自动切换到Twitter的最新标签页，在搜索框中输入"OpenAI's latest model"，然后截取了多张屏幕截图，并在侧边栏生成了一份简洁的报告。

### 启用高风险模式

基础示例比较简单，现在我们来点更有趣的——启用**高风险模式**。在这个模式下，Claude无需每次请求批准，可以直接执行操作，让整个过程更加流畅。

## 教Claude掌握新技能：Excalidraw绘图工具测试

接下来，我们要测试一个强大的新功能：**"教Claude你的工作流程"**。按照提示："像教新队友一样，一步步演示操作步骤"。我们决定用它来测试Excalidraw绘图工具的使用。

### 录制教学流程

点击"教Claude"并开始录制后，我演示了如何在Excalidraw中进行脑暴：

- 点击文本框并删除，即可移除文字
- 顶部工具栏包含了所有主要功能
- **特定的按钮**可以创建矩形框
- **双击画布**可以直接输入文字，例如"子想法"
- 调整矩形框的设置，例如改用实线描边
- **按数字键5**可以启用箭头工具
- 拖动箭头，将主要想法连接到子想法
整个演示过程被记录为61个步骤，Claude自动总结并生成了一个名为"绘图教程"的快捷指令。

### 执行教学任务

清空画布后，我下达了新指令："请搜索网上关于Claude新Chrome扩展的信息，列出它的功能，然后说明如何连接到Claude Code。要求简洁，不要太详细。"

令人惊叹的是，Claude立即开始行动：

- 打开了多个标签页
- 在Google上搜索相关信息
- 深入研究Chrome扩展文档
- 截取屏幕截图
更不可思议的是，它开始在Excalidraw画布上直接绘制信息图表！它添加了"Claude Chrome扩展"的文字框，画了一个箭头连接到"连接Claude Code"，还标注了操作步骤。

尽管整个过程比较缓慢（可能是使用了Opus 4.5而非Haiku或Sonnet的原因），在处理颜色更改等细节时也会卡住，但它展现出的**空间感知能力**确实令人印象深刻。

## 连接Claude Code：真正的杀手级功能

我最感兴趣的是如何将Chrome扩展与**Claude Code**连接起来。

### 建立连接

打开Cursor编辑器，创建一个新项目，在终端中输入`claude`启动Claude Code。然后，我向它提问："请搜索网络，告诉我如何将你（Claude Code）连接到Claude浏览器扩展。"

按照Claude的指导：

1. 将Chrome设为默认浏览器
1. 在Chrome上安装扩展
1. 在Claude Code中运行`/chrome`命令
1. 管理权限，重新连接扩展
1. 确认启用
就这么简单！通过`/chrome`命令，Claude Code和浏览器扩展就建立了连接。

### 协同工作演示

我让Claude Code创建一个简单的Hello World网页应用并在本地运行。接着，通过Claude扩展控制浏览器查看结果——浏览器自动打开，访问localhost，页面显示"Hello world"。

接下来，进行更复杂的测试：将Hello World页面改造成一个**潜在客户开发页面**，用于注册我的Claude Code使用教学 webinar。页面主题要求是"石墨灰混合 Teenage Engineering 风格"。

Claude立即添加了大量代码。更神奇的是，当页面完成改造后，它自动填写了所有表单字段进行测试。整个过程完美运行！

### 集成Firebase后端

现在，我们要进一步增加复杂度——添加Firebase后端。

在Firebase控制台创建新项目"data form"，设置Cloud Firestore数据库（测试模式）。然后回到Cursor，将配置信息提供给Claude Code，要求它：

- 添加Firebase后端功能，确保数据正确存入数据库
- 测试应用，验证数据是否在Firebase中显示
Claude Code迅速修改代码，刷新页面后，测试数据成功保存到Firestore数据库中。当我要求用"Johnny Smith"再次测试时，它打开Firebase控制台，确认了数据集合"webinar signups"的存在。

### 自动配置Google登录

最后也是最震撼的测试：添加用户认证功能。

要求："设置Google登录选项，让用户无需填写邮箱即可注册。先在Firebase中配置OAuth。"

只见Claude扩展在Firebase控制台中：

- 导航到Authentication（认证）部分
- 点击Google登录选项
- 点击启用按钮
- 添加必需的支持邮箱
完成配置后，刷新应用页面——Google登录按钮已经出现！它自动测试登录流程，用我的Google账号完成登录，填写经验等级，提交表单，然后返回Firebase数据库确认新数据成功存储。

**整个过程完全自动化**，我无需编写任何代码或手动配置任何设置。Claude通过扩展直接控制浏览器完成了所有操作！

## 总结与展望

在这次测试中，我们完成了两件大事：

1. **使用Chrome扩展**：让Claude代表我们在浏览器中执行任务，甚至通过"教Claude"功能赋予它新技能
1. **连接Claude Code**：通过简单的`/chrome`命令，让Claude Code能够控制Chrome浏览器，实现代码编写、应用测试、后端配置、数据库验证的全流程自动化
最令人震撼的是，Claude能够：

- 创建网站并测试功能
- 自动创建和配置Firebase项目
- 在浏览器中操作控制台开启认证功能
- 验证数据存储是否正确
- 整个过程无需人工干预
## 未来的可能性

这个功能的潜力是巨大的。结合我之前视频中提到的**Claude Skills**（通过在代码库中创建`claude.md`文件，给Claude提供特定指令），我们可以创造出更强大的工作流程。

例如，可以创建一个"竞争对手研究"技能，其中包含使用Chrome扩展浏览特定网站、收集信息、整理报告的完整指令。当Claude Code需要执行这类任务时，它就会自动调用浏览器工具完成工作。

**Skills + 浏览器控制 = 真正的自主智能体**

这实在是太疯狂了。接下来，我计划花更多时间测试这个功能，并尝试构建一个能处理大部分日常工作的通用智能体。

---

如果你对Claude Code的使用感兴趣，无论是构建移动应用、网页应用，还是将其作为通用智能体，我将在下个月举办一场4小时的直播活动，与我在旧金山的团队一起，分享我们日常使用Claude Code的所有经验和技巧。由于是实时互动并回答所有问题，本次活动将限制人数，先到先得。注册链接在视频描述中。

感谢观看，别忘了订阅和点赞！
