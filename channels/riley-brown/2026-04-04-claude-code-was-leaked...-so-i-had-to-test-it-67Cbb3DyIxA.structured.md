---
title: "Claude Code Was Leaked… So I Had to Test it - 结构化文稿"
channel: "Riley Brown"
published: "2026-04-04"
source_url: "https://www.youtube.com/watch?v=67Cbb3DyIxA"
video_id: "67Cbb3DyIxA"
variant: "structured"
---

# Claude Code Was Leaked… So I Had to Test it - 结构化文稿

- **Channel:** Riley Brown
- **Published:** 2026-04-04
- **Source:** https://www.youtube.com/watch?v=67Cbb3DyIxA
- **Main:** [Claude Code Was Leaked… So I Had to Test it](2026-04-04-claude-code-was-leaked...-so-i-had-to-test-it-67Cbb3DyIxA.md)

# Claude Code 泄露事件：我下载源码并打造个性化 Riley Code

**视频标题**：Claude Code Was Leaked… So I Had to Test it

**频道/来源**：Riley Brown

---

昨天，**Anthropic 犯了一个大错误**——他们再次意外泄露了 Claude Code 的代码。随后，有人在 Twitter 上发布了下载链接。出于强烈的好奇心，我决定下载它、仔细研究，并开始在我的电脑上运行 Claude Code 进行实验。

> **免责声明**：本视频仅供娱乐用途。我将下载 Claude Code 的源代码，使用 **OpenAI Codeex** 分析其工作原理，并实际修改它。我会改变 Claude Code 中的动作动词（action verbs），改变它的“个性”，尝试打造一个更佳的交互界面。我将通过“氛围编程”（vibe code）为自己定制一个专属版本的 Claude Code，并看看最终效果如何。
>

> **完整声明**：我不会出售或商业化本视频中创建的任何内容——这纯粹是为了娱乐。Anthropic，请别追究我。
无论如何，让我们直接进入正题。

---

## 一、泄密事件与源码获取

今天早上，当我打开手机时，**这条推文正好出现在信息流的首位**：

> “Claude Code 源代码已通过 npm 注册表中的 map 文件泄露。”
我们只需简单下载代码，然后玩一玩。我们将通过研究这份代码来学习，并基于它构建属于我们自己的 Claude Code 版本。再次强调：**这纯粹是为了娱乐**。

这条推文最有趣的地方在于：**只需点击链接，它就会自动下载到你的电脑**。不过现在这个链接似乎已经失效了（可能已被屏蔽）。幸运的是，我早已提前下载好了。它现在放在我的 `source 2` 文件夹中，这就是所谓的 Claude Code 代码。

---

## 二、使用 OpenAI Codeex 分析源码

我首先复制了一份代码（点击“Duplicate”），得到 `source 2 copy`。然后在 **Codeex** 中添加新项目，并选择 `source 2` 文件夹。我向 Codeex 提问：

> “请告诉我这个项目里有什么？总结这个智能体（agent）。”
有趣的是：**修改 Claude Code 源码时，使用 Claude 本身会感觉很奇怪**（我担心会被记录到某个奇怪的数据库里）。因此，我选择使用 OpenAI Codeex 来分析代码。

### 分析结果摘要

Codeex 分析完成后，给出了以下信息：

- 这是 **Anthropic 的 Claude Code CLI** 的源代码树。
- CLI 入口点会打印“Claude code”，并包含远程控制、守护进程工作器（daemon workers）、后台会话、MCP 辅助工具以及其他智能体运行时模式的专用快速通道。
- 它拥有 **Claude Code 的一切功能**：内置的自定义插件智能体、**多智能体委托（multi-agent delegation）**——这确实非常酷。
---

## 三、本地运行代码并创建“Riley Code”

接下来，我希望像运行真正的 Claude Code 一样运行这份代码——但运行的是我自己的修改版本。为此，我可能需要 **Anthropic API 密钥**。

我向 Codeex 下达指令：

> “请执行一切必要操作，让这份代码在终端本地运行。我不想运行官方的 Claude Code，我想运行这份代码（它本质上就是 Claude Code，但我们将对其进行修改）。请运行它，并修改 UI，将其命名为 **Riley Code**。请告诉我运行命令。我会在下一条消息中提供 Anthropic 密钥。”
### 获取 API 密钥

我打开 Google Chrome，访问 **Anthropic Console**（控制台），创建了一个 API 密钥。出于安全考虑，我未在屏幕上展示密钥。

### 运行 Riley Code

Codeex 完成后，我获得了运行命令：在终端中输入 `Riley code`。

我打开终端，输入 `Riley code`，成功启动！终端显示：

> **Riley code. Say hello. How can I help you today?**
我问道：“你是 Claude Code 吗？”

---

## 四、修改动作动词（Action Verbs）

我想找到代码库中的“动词”（verbs）。例如：

- `spelunking`（探洞）
- `working`（工作中）
- `symbioting`（共生）——这是另一个例子。
我决定**将这些动词完全改成我想要的样式**，因为现在我可以完全自定义 Claude Code 了。

### 寻找更多有趣的动词

我在 Codeex 中开启新会话，并请求：

> “请查找类似 `maxing`、`jester maxing`、`frame mogging` 这样的动词，以及其他流行文化中有趣的动词。请列出 20 个。”
Codeex 给出了一个不错的列表。我复制了这 20 个动词，然后回到代码中进行替换。

### 修改后的效果

在终端中再次运行 `Riley code`，输入 `hello make an app`，然后看到：

- `Status maxing`
- `Clout maxing`
- `Mewing`
- `Aura farming`
- `Fire`
**非常有趣**——修改成功了。

---

## 五、改变智能体的“个性”（Personality）

我希望进一步修改智能体的个性：

- **全部使用小写字母**回复。
- **非常直接**，像一个 **19 岁的实习生**：非常聪明、通才型（不完全是程序员）、回复快速、有时会分多条消息发送，但整体风格像是群聊中的对话。
我向 Codeex 提问：

> “请弄清楚如何在代码库中修改智能体的个性。深入思考后，请进行修改。”
### Codeex 的解决方案

Codeex 创建了一个 `personality.txt` 文件，并解释道：

> “我将个性作为一个专用的提示文件（prompt file）添加，这样无需触碰主包（bundle）即可轻松调整。启动器（launcher）现在通过受支持的系统注入‘角色’（Persona）。”
### 验证修改结果

在终端中再次运行 `Riley code`，输入任务请求，智能体回复：

> “what it is, it's a coding, not just a chatbot.”（全小写，分块输出）
**成功修改了智能体的个性**。

---

## 六、创建桌面应用（Desktop App）

我询问如何让这个智能体更接近 **OpenClaw**。Codeex 给出了 8 个不同的建议。我选择了其中一个关于“工作区文件”（workspace files）的方案，并要求实现。

然后我请求：

> “请运行这个桌面应用。”
### 应用初始状态

桌面应用打开后，界面包含：

- 之前的聊天会话记录
- 输入框和交互区域
我输入：“Hello there. My name is Riley.” 智能体回复（使用我设置的动词）：`jester gooning`。然后它回复：“Hey Riley. Nice to meet you. What are we working on today?”

我要求它构建一个“Hello World”网页应用。智能体启动了本地技能（`Vibe Code CLI skills`），并开始工作。

### 权限问题处理

运行过程中出现了 Bash 命令被阻止的提示：“Looks like I need your approval.” 我要求它使用 `dangerously skip permissions` 模式。修改后，桌面应用默认以跳过权限的模式启动。

---

## 七、界面优化与功能调整

我口头描述了希望做出的界面修改：

- **工具调用指示器**：不显示绿色气泡，而是将技能名称、Bash 执行状态等放在三个点（`...`）的动画气泡内，仅显示当前正在使用的工具，并让动词（如“Status maxing”）更大显示在下方。
- **移除冗余文字**：删除“reply ready”等文字。
- **停止按钮**：放在屏幕底部。
- **支持在加载时输入提示词**：允许在智能体回复的同时输入下一个提示。
- **侧边栏优化**：仅显示聊天标题，移除圆角圆形组件，左侧字体调小。
- **顶部栏优化**：移除横向贯穿的分割线。
### 停止按钮功能验证

停止按钮工作正常。

---

## 八、增加持久化记忆与项目切换功能

我希望所有聊天会话都能包含一个 `soul.md` 文件，用于记住关于我的信息并自动存储。同时，在创建新聊天时，我希望能够创建新项目——就像 Codeex 中的“项目与线程”（projects and threads）那样，可以在一个新目录中开始，该目录拥有自己的文件。

我不确定当前终端会话是从哪个目录启动的，因此需要明确这一功能。

---

## 九、UI 视觉改造

我参考了一个名为 **Blueberry** 的应用，并上传了一张山峰图片作为背景。具体要求：

- 侧边栏和聊天区域不能太透明。
- 背景图片不要过度模糊，而是要看起来像 Blueberry 的样式。
### 修改后的视觉效果

我进行了一些调整，最终效果如下：

- 聊天界面更加美观。
- 工具调用显示在 `...` 动画气泡内。
- 背景为山峰图片，侧边栏和聊天区域透明度适中。
我测试了一下：输入“Please tell me who you are.”，智能体回复（全小写）：

> “hi, i'm riley code, anthropic's official cli for claude. basically, coding assistant that you can chat with. what are you working on?”
---

## 十、内置浏览器（类似 Claude Artifacts）

我要求增加一个功能：**在应用右侧内置一个小型浏览器**（默认关闭）。任何我点击的链接（包括本地 `localhost` 链接或生成的文件路径）都应该在该内置浏览器中打开。

具体要求：

- 每次生成内容时，**最后一条消息中的链接应自动打开该内置浏览器**。
- 文件路径也应该能在该区域中打开。
---

## 十一、后续优化（两小时后）

在停止拍摄后的两小时里，我继续做了一些优化：

- 让界面看起来更美观，动画效果更流畅。
- 可以**全屏显示正在开发的应用**。
- 清理了文件结构，使其更接近 **Codeex** 的样式（我从 Codeex 应用中获得了大量灵感）。
- 我的版本运行的是 **Riley Code**——也就是基于下载的 Claude Code 源码构建的个性化版本。
### 最终功能演示

- 可以在侧边视图中打开文件。
- 可以调整窗口大小或全屏。
- 可以查看**全局文件**（global files），例如 `tools.md`。
- 可以要求 Riley Code 编辑这些文件，从而轻松改变智能体的个性。
- 可以轻松创建新项目。
- 整个体验与 Codeex 非常相似：创建新会话、发送消息、要求智能体创建任何应用——就像使用原版 Claude Code 一样。
界面配上了漂亮的背景图片。

---

## 结语

我在这段视频中进行了一系列实验，希望大家能从中有所收获。无论如何，感谢观看！**请点击订阅**——这对我帮助很大。我们下个视频再见！

（视频文稿结束）
