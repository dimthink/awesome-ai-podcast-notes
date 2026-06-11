---
title: "AutoGen FULL Tutorial with Python (Step-By-Step) 🤯 Build AI Agent Teams!"
channel: "Matthew Berman"
published: "2023-10-10"
source_url: "https://www.youtube.com/watch?v=V2qZ_lgxTzg"
video_id: "V2qZ_lgxTzg"
rating: 4
language: "中文"
word_count: 11264
duration: "15:04"
---

# AutoGen FULL Tutorial with Python (Step-By-Step) 🤯 Build AI Agent Teams!

- **Channel:** Matthew Berman
- **Published:** 2023-10-10
- **Source:** https://www.youtube.com/watch?v=V2qZ_lgxTzg
- **TL;DR:** AutoGen让你用Python轻松构建多AI代理团队，通过配置模型、创建代理、定义任务，实现从代码生成到文件操作的自动化协作。
- **Rating:** 4

## 版本

- [结构化文稿](2023-10-10-autogen-full-tutorial-with-python-(step-by-step)-🤯-build-ai-agent-teams!-V2qZ_lgxTzg.structured.md)
- [原始文稿](2023-10-10-autogen-full-tutorial-with-python-(step-by-step)-🤯-build-ai-agent-teams!-V2qZ_lgxTzg.transcript.md)

# AutoGen 完全教程：用 Python 搭建你的 AI 代理团队

想象一下，你能够组建一支由多个 AI 智能体组成的团队，它们可以相互协作、编写代码、执行任务，就像 ChatGPT、代码解释器和插件的结合体，而且完全可定制化——你可以为每个代理赋予不同的角色（比如 CEO、CTO、数据分析师），让它们像人类团队一样分工合作，完成你下达的任何复杂指令。这不再是科幻电影中的场景，而是微软开源的 AutoGen 框架带给我们的现实。

在本教程中，AI 领域的资深探索者 Matthew Berman 将手把手带你走进 AutoGen 的世界。他本人毫不掩饰对这项技术的狂热：“我完全痴迷于 AutoGen，它是我自最初看到 ChatGPT 以来见过的最酷的 AI 技术。” 从环境配置到代码实现，从单代理到多代理协作，Matthew 会一步步拆解每一个细节。无论你是刚接触 AI 开发的初学者，还是希望扩展自动化能力的资深开发者，这篇文章都将为你提供一份清晰、可操作的指南，让你亲手搭建出属于自己的 AI 代理团队。

---

## 材料信息

- **标题**：AutoGen FULL Tutorial with Python (Step-By-Step) 🤯 Build AI Agent Teams!
- **作者/来源**：Matthew Berman
- **类型**：YouTube 视频字幕
- **关键元数据**：发布日期未知（推测为 2023 年底），视频时长约 18 分钟
---

## 开场与 AutoGen 概述 `[视频开头 0:00-2:30]`

**核心观点**

AutoGen 是一个允许多个 AI 代理协同工作的框架，它们能使用工具、编写并执行代码，堪称 ChatGPT + 代码解释器 + 插件的超集，且完全可定制，可直接嵌入你的应用程序。

**深度阐述**

Matthew 在视频开头就毫不掩饰他对 AutoGen 的兴奋：“I absolutely obsessed with autogen it is the coolest piece of AI technology that I've seen since I saw chat GPT originally.”（我对 AutoGen 完全着迷了，它是我自最初看到 ChatGPT 以来见过的最酷的 AI 技术。）这种热情贯穿了整个教程，也传递给了观众。

为了让大家快速理解 AutoGen 的定位，Matthew 给出了一个生动的类比：把它想象成 ChatGPT Plus，但你可以自由组合多个“大脑”（代理），每个大脑可以有不同的个性、角色和能力。其中一个代理可以专门负责写代码，另一个负责执行代码并返回结果，还有一个可以充当管理者，协调整个流程。这就像组建了一支 AI 特种部队，每个成员各司其职，共同完成你下达的指令。

更重要的是，AutoGen 不仅仅是概念演示，它已经是一个成熟的 Python 库，你可以将它直接集成到自己正在构建的应用中。这意味着你可以用几行 Python 代码，就能为你的软件增加一个由多个 AI 代理组成的协作层，自动处理那些原本需要人工介入的复杂任务。

Matthew 提到，他已经发布过一个面向初学者的 AutoGen 教程视频，概述了它的基本功能，而这次他准备深入一步，带大家在实际的电脑上一步一步搭建代码环境，并且计划推出一系列 AutoGen 相关的内容。他鼓励观众在评论区留言，提出想看的主题，这种互动姿态让教程更具社区感。

---

## 环境准备：安装 Anaconda、创建虚拟环境、安装 pyautogen `[视频 2:30-5:00]`

**核心观点**

要运行 AutoGen，你需要 Python 环境、代码编辑器（如 VS Code）、Anaconda（用于环境管理）以及一个 OpenAI 账号。通过创建独立的 Conda 虚拟环境，可以避免依赖冲突，确保项目干净可复现。

**深度阐述**

动手之前，Matthew 列出了必需的“装备”：

- **Visual Studio Code**（或其他代码编辑器）—— 用于编写和运行 Python 脚本。
- **Anaconda** —— 一个流行的 Python 环境管理工具，可以创建隔离的虚拟环境，防止不同项目之间的包版本冲突。
- **OpenAI 账号** —— 目前 AutoGen 主要依赖 OpenAI 的模型（如 GPT-3.5、GPT-4），因此你需要一个有效的 API key。Matthew 也提到他正在尝试集成开源模型，但现阶段仍以 OpenAI 为主。
在 VS Code 中，Matthew 创建了一个新文件并保存为 `app.py`，同时新建了一个名为 `autogen` 的文件夹作为项目根目录。他点击 VS Code 右上角的“打开终端”按钮，准备执行命令行操作。

接下来是创建 Conda 虚拟环境的关键步骤。Matthew 输入以下命令：

```bash
conda create -n autogen python=3.11.4
```

这条命令会创建一个名为 `autogen` 的新环境，并指定 Python 版本为 3.11.4。为什么强调版本？因为不同的 Python 版本可能导致某些库不兼容，统一版本可以避免这类问题。他提醒大家注意三处的 Python 版本一致性：Conda 使用的版本、系统 Python 版本、VS Code 引用的版本（可以在 VS Code 右下角查看）。确保三者一致（都是 3.11.4）能减少很多麻烦。

环境创建完毕后，需要激活它：

```bash
conda activate autogen
```

激活后，终端提示符会变成 `(autogen)`，表明当前处于该虚拟环境中。接下来，安装 AutoGen 库：

```bash
pip install pyautogen
```

Matthew 已经安装过，所以终端显示“Requirement already satisfied”。他顺便检查了 Python 版本，确认无误后，回到 `app.py` 开始编写代码。

**个人感受**

Matthew 在操作过程中非常注重细节，比如反复强调版本一致性和激活环境后的提示符变化。这种谨慎的态度反映出他作为技术布道者的严谨——他不仅要教会你步骤，还想让你理解每个步骤背后的原因，避免踩坑。当看到 `(autogen)` 提示符出现时，他那种“可以开始真正工作了”的满足感，相信每一位开发者都能感同身受。

**延伸思考**

为什么需要虚拟环境？想象一下，如果你同时参与多个 Python 项目，一个项目需要 Django 2.2，另一个需要 Django 3.0，全局安装必然导致冲突。虚拟环境就像每个项目独立的“小房间”，里面只有该项目需要的依赖。Anaconda 是管理这些“小房间”的得力工具。对于 AI 开发来说，环境隔离尤其重要，因为不同的 AI 框架（如 TensorFlow、PyTorch）经常对库版本有苛刻要求。

---

## 导入与配置：设置模型、API key、llm*config **`[视频 5:00-7:30]`*

**核心观点**

AutoGen 的核心配置是通过一个 `config`*`list`** 指定使用的模型和 API key，再通过 **`llm`*`config` 设置请求超时、缓存种子（seed）和温度等参数。合理配置这些参数可以平衡成本、速度和创造力。

**深度阐述**

打开 `app.py`，Matthew 首先导入 AutoGen 库：

```python
import autogen
```

他使用了 GitHub Copilot，所以编辑器会自动弹出预测代码，但他为了教程清晰，暂时关闭了 Copilot。

接下来是配置部分。AutoGen 使用一个配置列表来定义要调用的模型。Matthew 定义了 `config`*`list`**：*

```python
config_list = [
    {
        'model': 'gpt-3.5-turbo-16k',
        'api_key': 'sk-...'
    }
]
```

他解释，这里使用 GPT-3.5-turbo-16k 是为了演示，但强烈推荐使用 GPT-4，因为它的推理能力更强，尤其适合复杂任务。但为了先让代码跑通，GPT-3.5 足够。关于 API key，他现场在 OpenAI 平台创建了一个新 key（命名为 `autogen`），并提醒观众，视频发布后会撤销这个 key，确保安全。

有了 `config`*`list`**，下一步是构建 **`llm`*`config` 对象，它包含了所有与语言模型交互的通用设置：

```python
llm_config = {
    'request_timeout': 600,
    'seed': 42,
    'config_list': config_list,
    'temperature': 0
}
```

- `request`*`timeout`**：设置请求超时时间（秒）。如果 OpenAI API 响应过慢，超过这个时间就会终止请求，避免程序无限等待。*
- `seed`：用于缓存机制的“种子”。这是一个非常实用的功能——AutoGen 会缓存每次请求的响应，当相同的提示和相同的 seed 再次发起请求时，直接返回缓存结果，既节省时间又节省费用。Matthew 形象地说：“Once you run one of these tasks once with these agents it caches the response, so if you run the same task again it’s going to use the cached version.” 如果修改了 seed 或删除了缓存文件夹，才会重新调用 API。
- `temperature`：控制输出的随机性，取值范围 0 到 1。0 表示最确定、最保守的回答（适合代码生成等需要精确性的任务），1 表示最富创意、最多变的回答。Matthew 设置为 0，因为编码任务需要确定性，但他鼓励大家尝试调整这个值，看看效果有何不同。
**重要原话**

“For coding tasks we want pretty non-creative responses, so that's why we're going to keep it at zero but feel free to play around with this value.” `[视频 6:50]`（对于编码任务，我们想要相当不具创意的响应，所以我们将它保持为 0，但你可以随意调整这个值。）

**视觉/结构信息描述**

在 VS Code 中，Matthew 逐行键入上述代码，编辑器高亮显示关键字，代码结构清晰。他特意展示了 `config`*`list`** 和 **`llm`*`config` 两个字典的嵌套关系，让观众一目了然。

---

## 创建 AI 代理：AssistantAgent 和 UserProxyAgent `[视频 7:30-10:00]`

**核心观点**

AutoGen 中的核心角色是 AssistantAgent（助理代理）和 UserProxyAgent（用户代理代理）。AssistantAgent 负责生成回复（如写代码、提供建议），UserProxyAgent 代表用户执行操作（如运行代码、给出反馈）。你可以创建多个代理，并通过 system message 赋予它们不同的角色。

**深度阐述**

配置完成后，Matthew 开始创建第一个助理代理：

```python
assistant = autogen.AssistantAgent(
    name="assistant",
    llm_config=llm_config
)
```

这里只传入了名称和 llm*config，但 Matthew 指出，如果你创建多个助理代理，一定要为每个代理提供 **`system`*`message`，明确它们的角色。例如，你可以创建 “CTO” 代理，专门负责技术决策；“CEO” 代理负责整体协调。通过 system message，你可以精细定义每个代理的行为边界和职责。

接着是用户代理代理：

```python
user_proxy = autogen.UserProxyAgent(
    name="user_proxy",
    human_input_mode="TERMINATE",
    max_consecutive_auto_reply=10,
    is_termination_msg=lambda x: x.get("content", "").rstrip().endswith("TERMINATE"),
    code_execution_config={"work_dir": "web"},
    llm_config=llm_config,
    system_message="""A human admin."""
)
```

这里涉及几个关键参数，Matthew 逐一解释：

- **human*****input*****mode**：定义用户介入的程度。AutoGen 文档提供了三个选项：
本教程选择 `"TERMINATE"`，即代理自动执行任务，直到遇到终止消息才停下来征求用户意见。

- **max*****consecutive*****auto*****reply****：设置代理之间连续自动回复的最大次数。如果这个值设置得太高，代理们可能会陷入无限循环，来回对话，导致大量 API 调用和费用。Matthew 设为 10，既给任务足够多的交互机会，又避免失控。*
- **is*****termination*****msg**：一个函数，用于检测消息中是否包含终止关键词。这里设定为当消息内容以 “TERMINATE” 结尾时，就认为任务结束。这个终止词通常由助理代理在完成任务时返回。
- **code*****execution*****config**：配置代码执行的目录。这里指定 `work`*`dir`** 为 **`"web"`**，意味着所有生成的代码文件都将存放在项目根目录下的 **`web`** 文件夹中。这样可以将生成的代码与主脚本分离，保持整洁。*
- **system*****message****：给用户代理代理的指令，告诉它如何判断任务是否完成。Matthew 直接使用了 AutoGen 提供的默认消息。*
**个人感受**

Matthew 在讲解参数时，特别强调了 `max`*`consecutive`*`auto`*`reply`** 的重要性，因为他自己在测试 GPT-3.5 时就遇到过代理无限循环的情况。他半开玩笑地说：“好在我们设了 10，不然它们会永远说‘谢谢，我做不到’。” 这种从实际经验中得出的教训，让他的讲解更有说服力，也让观众意识到参数设置的必要性。*

**延伸思考**

为什么需要区分助理代理和用户代理代理？这种设计模仿了真实世界中人类与助手的协作模式：人类（用户代理）提供目标、执行实际操作（如运行代码），而 AI 助理提供智力支持（如写代码）。将两者分离，使得我们可以灵活地组合不同的助理（比如一个擅长写 Python，另一个擅长数据分析）与同一个用户代理协作，或者一个助理与多个用户代理交互。这种架构为构建复杂的多智能体系统奠定了基础。

---

## 定义任务与发起对话 `[视频 10:00-12:00]`

**核心观点**

要给代理团队下达任务，只需定义一个任务字符串，然后通过 `user`*`proxy.initiate`*`chat()` 发起对话，传入助理代理和任务消息。AutoGen 会处理后续的代理间通信。

**深度阐述**

任务的定义非常简单：

```python
task = """
Give me a summary of this article:
[此处粘贴一篇文章的URL或内容]
"""
```

Matthew 在视频中粘贴了一篇随机文章，但他也承认，硬编码 URL 不够灵活，更好的做法是让用户通过输入指定 URL。不过为了演示，暂时这样处理。

发起对话的代码只有一行：

```python
user_proxy.initiate_chat(assistant, message=task)
```

`user`*`proxy`** 作为对话的发起者，将任务消息发送给 **`assistant`**，然后两个代理开始互动。助理代理收到消息后，可能会要求用户代理执行某些操作（如运行代码），用户代理执行后，将结果返回给助理，如此往复，直到任务完成。*

Matthew 保存文件，准备运行。他点击 VS Code 右上角的“运行”按钮，期待看到结果。

---

## 测试运行与问题排查 `[视频 12:00-15:00]`

**核心观点**

第一次测试往往不会一帆风顺。Matthew 发现 GPT-3.5 在处理复杂任务时表现不佳，导致代理间陷入无意义的循环。改用 GPT-4 并简化任务后，系统成功生成了代码并存储了文件。这也印证了选择合适模型的重要性。

**深度阐述**

运行开始后，终端输出了代理间的对话。但很快 Matthew 发现不对劲：助理代理反复说“谢谢，我做不到”，用户代理则回复“感谢你的反馈，我们继续”。这样的对话一直持续，直到达到 `max`*`consecutive`*`auto`*`reply=10`** 才停止。Matthew 无奈地说：“So good thing that we set the max auto reply to be 10 because this would have just kept going indefinitely.”（好在我们设置了最大自动回复为 10，不然它会无限继续下去。）*

原因是什么？GPT-3.5 的推理能力有限，无法准确理解“总结文章”这样需要先获取文章内容的复杂指令。它不知道如何获取文章，只能反复道歉。

为了证明 AutoGen 本身是正常的，Matthew 决定换一个更简单的任务：“write python code to output numbers 1 to 100 and then store it in a file.”（写 Python 代码输出数字 1 到 100，然后存储在文件中。）同时，他把模型换成 GPT-4，因为 GPT-4 的推理能力更强，更适合代码生成。

在重新运行之前，Matthew 删除了缓存文件夹（`./cache`），以确保不使用之前的缓存。再次点击运行，这次代理们的表现好了很多：助理代理生成了 Python 代码，用户代理执行了代码，并在 `web` 文件夹下创建了 `numbers.txt`，里面包含数字 1 到 100。但 Matthew 发现，他本意是想让助理代理把代码本身保存到一个文件里，而不是运行代码生成数字。所以任务理解仍有偏差。

于是他利用 `human`*`input`*`mode="TERMINATE"` 的特性，在任务结束后，向助理代理提供反馈：“I accidentally quit out of here before giving it feedback so let's just run it again”（我意外退出了，所以没给反馈，我们重来一次）。他删除了缓存和 `web` 文件夹，修改提示为“and then store the code in a file”（并把代码存储在一个文件中）。再次运行，这次助理代理生成了代码，并指示用户代理将代码写入 `print`*`numbers.py`** 文件。成功！*

**重要原话**

“I think it misunderstood what I wanted… as the feedback I'm going to say…” `[视频 14:00]`（我觉得它误解了我的意思……作为反馈，我会说……）

**个人感受**

Matthew 在面对失败时没有气馁，而是理性分析原因：模型能力不足、提示词不够明确。他通过切换模型和优化提示词，最终让系统按预期工作。这种调试过程本身就是宝贵的经验——在实际开发中，我们也会遇到类似情况，耐心和细致是解决问题的关键。

**延伸思考**

这个测试过程揭示了 AI 应用开发的一个核心挑战：提示工程（Prompt Engineering）。同样的任务，用不同的表述方式，结果可能天差地别。而且，不同模型对提示的敏感度也不同。因此，在设计 AutoGen 任务时，我们需要像产品经理一样思考：如何清晰、无歧义地向 AI 表达需求，并考虑到 AI 可能产生的误解，从而设计出鲁棒的交互流程。

---

## 扩展任务与缓存机制 `[视频 15:00-17:00]`

**核心观点**

AutoGen 的缓存机制可以大幅节省成本和时间。通过定义第二个任务，Matthew 展示了如何让代理基于之前生成的文件进行修改，体现了多轮对话的连续性。同时，他演示了如何将 `human`*`input`*`mode` 改为 `"NEVER"`，实现完全自动化。

**深度阐述**

为了展示更复杂的场景，Matthew 添加了第二个任务：

```python
task2 = """
Change the code in the file you just created to instead output numbers 1 to 200.
"""
```

他希望通过一次运行，先完成第一个任务（输出 1-100 并存储代码），然后自动执行第二个任务（修改代码以输出 1-200）。为此，他需要两次调用 `initiate`*`chat`**：*

```python
user_proxy.initiate_chat(assistant, message=task)
user_proxy.initiate_chat(assistant, message=task2)
```

同时，他将 `human`*`input`*`mode` 改为 `"NEVER"`，这样整个过程完全自动化，无需人工干预。当然，他提醒观众，自动化有风险，但这里的任务简单，所以可以接受。

再次删除缓存和 `web` 文件夹后运行，代理们依次执行了两个任务。第一个任务创建了 `print`*`numbers.py`**，内容输出 1-100；第二个任务读取该文件，修改代码使其输出 1-200，并生成了 **`numbers.txt`** 包含 1-200。虽然最终结果与 Matthew 的预期略有出入（他原本希望只修改代码文件，但代理额外生成了 **`numbers.txt`**），但整体上系统理解了“修改代码”的意图，并成功完成了修改。*

Matthew 指出，这种基于文件的连续对话能力非常强大——代理们可以像人类同事一样，在同一个工作目录下迭代项目，逐步完善成果。

**视觉/结构信息描述**

在 VS Code 的文件资源管理器中，可以清楚地看到 `web` 文件夹下的文件变化：第一次运行后出现 `print`*`numbers.py`**，第二次运行后新增 **`numbers.txt`**。这种直观的文件变化让观众切实感受到代理的工作成果。*

---

## 代码优化建议与未来计划 `[视频 17:00-18:30]`

**核心观点**

生产级应用需要更好的代码组织：将 API key 和模型配置放在环境变量或 `.env` 文件中，分离配置与核心逻辑。Matthew 还计划推出更多 AutoGen 视频，特别是关于集成开源模型的教程。

**深度阐述**

演示接近尾声，Matthew 分享了一些改进代码的最佳实践：

- **敏感信息管理**：永远不要把 API key 直接写在代码里，尤其是要提交到 GitHub 的代码。应该使用环境变量或 `.env` 文件，并通过 `python-dotenv` 等库加载。
- **配置分离**：可以将 `llm`*`config`** 等配置放入单独的配置文件（如 **`config.py`**），保持主脚本简洁。*
- **代码重构**：将助理代理和用户代理的创建逻辑与任务执行逻辑分开，提高可读性和可维护性。
最后，Matthew 再次表达了对 AutoGen 的兴奋之情，并预告他将继续探索如何在 AutoGen 中使用开源模型，一旦成功就会发布新视频。他鼓励观众点赞、订阅，并在评论区提出想看的内容。

**个人感受**

Matthew 的热情感染了观众，他不仅满足于教会基本用法，还希望构建一个持续学习、共同进步的社区。他对开源模型的关注也反映了许多开发者的心声——降低对 OpenAI 的依赖，拥抱更多元化的模型选择。

---

## 精华收获

- **环境准备是关键**：使用 Conda 创建独立环境，确保 Python 版本一致，可以避免大量依赖问题。
- **配置决定行为**：通过 `seed` 开启缓存，能显著节省成本；`temperature` 控制创造力，编码任务建议设为 0。
- **代理角色的重要性**：合理设计 `AssistantAgent` 的 system message，让每个代理各司其职；`UserProxyAgent` 的 `human`*`input`*`mode` 决定了自动化程度。
- **模型选择至关重要**：GPT-3.5 适合简单任务，复杂任务应选用 GPT-4 或更强模型。
- **提示工程是艺术**：清晰、具体的任务描述能减少误解；通过多轮反馈可以迭代优化结果。
- **安全与可维护性**：永远不要硬编码 API key，使用环境变量管理敏感信息；分离配置与主逻辑，让代码更健壮。
AutoGen 为我们打开了一扇门：让多个 AI 代理像团队一样协作，完成从代码生成到文件操作的复杂任务。它不仅是工具，更是一种编程范式——未来的应用可能不再由单一 AI 驱动，而是由一群各怀绝技的 AI 代理共同构建。现在，你已经掌握了搭建这样一支“AI 梦之队”的基本功，接下来就是发挥创造力的时候了。

---

<!-- TLDR: AutoGen让你用Python轻松构建多AI代理团队，通过配置模型、创建代理、定义任务，实现从代码生成到文件操作的自动化协作。 -->

<!-- TAGS: AutoGen, AI代理, Python教程, 多智能体系统, 自动化 -->

<!-- RATING: 4 -->

---
