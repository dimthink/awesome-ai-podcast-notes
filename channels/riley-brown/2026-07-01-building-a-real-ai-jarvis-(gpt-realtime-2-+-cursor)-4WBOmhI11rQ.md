---
title: "Building a Real AI Jarvis (GPT Realtime 2 + Cursor)"
channel: "Riley Brown"
published: "2026-07-01"
source_url: "https://www.youtube.com/watch?v=4WBOmhI11rQ"
video_id: "4WBOmhI11rQ"
tags: ["AI代理", "Cursor", "GPT实时语音", "零代码构建", "桌面自动化"]
rating: 5
language: "英文"
word_count: 11263
duration: "21:09"
---

# Building a Real AI Jarvis (GPT Realtime 2 + Cursor)

- **Channel:** Riley Brown
- **Published:** 2026-07-01
- **Source:** https://www.youtube.com/watch?v=4WBOmhI11rQ
- **TL;DR:** 任何人都能用自然语言和零编程经验，在Cursor中构建一个桌面版AI贾维斯。
- **Tags:** AI代理, Cursor, GPT实时语音, 零代码构建, 桌面自动化
- **Rating:** 5

## 版本

- [结构化文稿](2026-07-01-building-a-real-ai-jarvis-(gpt-realtime-2-+-cursor)-4WBOmhI11rQ.structured.md)
- [原始文稿](2026-07-01-building-a-real-ai-jarvis-(gpt-realtime-2-+-cursor)-4WBOmhI11rQ.transcript.md)

# 深度重构文章

## 材料信息

- **标题**：Building a Real AI Jarvis (GPT Realtime 2 + Cursor)
- **作者/来源**：Riley Brown
- **类型**：YouTube 视频字幕
- **关键元数据**：发布于Riley Brown频道，是一次从零开始构建桌面端AI语音助手的完整实录，展示了GPT Realtime 2与Cursor的协同工作流

---

## 开篇引入

你可以想象一个场景吗？你对着电脑说一句话，屏幕上就出现了一个眨着眼睛的AI伙伴；你再对它说一句话，它就开始操控你的浏览器、打开编辑器、为你生成带有蓝框UI的应用截图，甚至能连续编辑16张图片。这不是科幻电影里的桥段，也不是某个封闭的实验室原型。这是Riley Brown用一个下午，三句提示词，和零基础写代码能力做出来的东西。

在这个视频里，Riley不仅拆解了如何利用OpenAI最新的GPT Realtime 2语音模型和Cursor编程助手打造一个名为"Ricky"的桌面AI代理，还暴露了整个过程中失败、调试、重来、再迭代的真实过程。它不只是展示了一个酷炫的Demo，更像是一部微型的"AI原生软件开发实录"——让人看见传统编程的门槛是如何被瓦解的，以及从有想法到有产品之间的路，现在可以有多短。

如果说Jarvis是钢铁侠的私人管家，那Ricky就是属于任何普通人的桌面灵魂。而这个灵魂，只需要几句话就能创造出来。

---

## 详细内容

### 💡 一、不只是Demo：一个会眨眼的灵魂诞生 `[00:00－02:00]`

**核心观点**
Riley用三句提示词就创造了一个完整的、具备情感的桌面语音AI代理，将实时对话从"一种交互方式"升级为"一种存在形式"。

**深度阐述**

视频的开头并不是枯燥地介绍背景，而是一段直接的、流畅的人机对话演示。Riley对着屏幕说了一句话，屏幕上一个叫做"Jary"的小角色立刻做出了反应。这个角色有眼睛、有嘴巴，可以打开菜单、改变心情、变换到"计算机控制模式"，甚至能够操控桌面打开其他软件。

这段看似简单的开场，埋下了一个巨大的伏笔：这不仅仅是语音输入/文字输出的老套路，而是基于OpenAI GPT Realtime 2模型构建的全新交互范式。当Riley说"Hey Jary, can you change to angry?"，Jary不仅完成了任务，还切换了一个带有情感色彩的动画——它的表情与语气都随之改变。

这里的核心冲击力，不在于代码的复杂程度，而在于整个过程的"轻松感"和"人性化"。

而这一切，Riley坦率地揭示道——是基于Cursor和GPT Realtime 2协同完成的。他花了三个Prompt，就把这个能说会笑、能看会做的AI伙伴做出来了。Riley强调：

> "How much coding experience is required? Well, the answer is 0 out of 10. You can be a complete novice to coding and you'll be able to create a voice agent for your personal use or for your business."

这句话的价值在于，它打破了AI应用构建的心理门槛。过去，任何AI应用的开发都需要前端、后端、API调用、语音处理等多门技术栈的协作；今天，所有这些被抽象成了"一个对话"：你跟Cursor对话，Cursor帮你写代码；你给AGENT一个API Key，它就能自己搜索网络，自己画图表。

**重要原话**：
> "The really magical technology behind Jarvis is OpenAI's brand new GPT real time 2. And it is so realistic to talk to."
> "让Jarvis背后的真正魔力，是OpenAI的全新GPT实时语音2代。跟它对话实在太逼真了。"

**视觉结构描述**：
视频最初展示了一个桌面小窗口，窗口内是一个简洁的卡通角色（Jary/Ricky）。它拥有黑色的大眼睛和简约的嘴巴，动画流畅自然，带有真实的眨眼行为。窗口两侧或底部配有功能按钮（如连接语音、显示、计算机控制、Artifacts面板等）。这就是该AI代理的本体——一个具象化的、活灵活现的数字存在。

**个人感受**
Riley的声音中透露出一种真实的自豪和兴奋。当他第一眼看到自己创造的Ricky时，那种语气就像看到一个婴儿第一次睁开眼睛："He blinks. Wait a sec. Wait for it. There he is." 这种情感赋予了这段技术内容一股人文的温度。他不是在用代码创造东西，而是在用语言孕育生命。

---

### 💡 二、你的第一句话：从零搭建一个AI代理 `[02:00－05:00]`

**核心观点**
构建AI代理的过程被简化为三个步骤：创建文件夹 -> 获取API Key -> 用自然语言注入命令。全部技术工作由Cursor和OpenAI的后端处理。

**深度阐述**

整个构建流程的开端，比大多数人的预期都要简单。Riley带领观众一步步操作：

1. **下载Cursor**：前往cursor.com，下载并安装Mac版。
2. **创建项目**：在桌面上创建一个名为"Riley Custom Jarvis"的文件夹，并通过Cursor打开。
3. **获取API Key**：登录OpenAI官网，在API Keys页面生成一个密钥命名为"Jarvis Key"。
4. **粘贴提示词**：将一段精心设计的提示词粘贴到Cursor的Agent窗口，然后回车让它开始工作。

这一段看起来极其简单，但每一步背后都承载着巨大的技术抽象。尤其是"粘贴提示词"这一步——当Riley把提示词粘贴进去时，他实际交付给Cursor的任务包括：构建一个桌面应用、接入GPT Realtime 2语音对话、加入Web搜索（通过Exa API）、图片生成功能（通过DALL-E）、Mermaid图表渲染、以及一个完整的前端动画系统。

> "Build a Jarvis-like desktop AI companion named Jary. ... Give Ricky a minimal animated face. I'm going to say high quality animations, but just eyes and mouth, nothing else. Natural blinking, expressive moods, and speech syncs mouth movement."

这段提示词本身就是一个微型的产品需求文档（PRD）。Riley用自然语言描述了产品愿景、功能范围、交互风格、UI要求——然后，Cursor在15分钟左右的时间内，将这些描述转化成了可运行的代码。

这个"等待的过程"在视频中被压缩成一个快进镜头，但Riley显然对它怀有极大的期待感："Okay so now cursor is probably going to take 10 to 15 minutes building this app. I'm going to go get a little bit of dinner and come back and we'll see what Cursor cooked up."

**延伸思考**
这个等待时刻，象征着一个时代的转变。过去，程序员在编译代码时等待，等待的是机器完成机械劳动；今天，非程序员在等待AI完成创意劳动——构建一个应用的结构、选择合适的技术栈、整合多个API。这种等待的"期望值"和"可能性"完全不同。

---

### 💡 三、Ricky的第一次"开口"：验证与惊喜 `[05:00－07:00]`

**核心观点**
AI代理第一次被运行时的兴奋感，以及对能力的初步验证，展示了AI原生应用与人之间的亲近感。

**深度阐述**

15分钟后，Riley回到屏幕前。一个名为Ricky的窗口已经建好，Riley轻轻呼唤它的名字：

> "Hey Ricky, how are you? Ricky, are you there?"
> "Yeah, I'm here. Loud and clear. What do you need?"

这个回应并非简单的文字输出——它是有语音的，是实时回应的，是在一个极低的延迟下发生的。Riley脸上的惊喜几乎溢出屏幕。

接下来，他要求Ricky列出自己能够做的所有事情，Ricky不仅说出了功能列表（Web搜索、图表、笔记、图片生成等），还成功将其转换成了一张Mermaid图表显示在Artifacts面板中。

**视觉结构描述**：
此处展示了ARTIFACTS面板的分屏效果。左侧是Ricky的头像和语音会话窗口，右侧是一片白板区域，Mermaid图表就在此渲染展示。图表本身是一个带有节点的箭头流程图，直观地展示了Ricky的能力结构。

**失败的必要性**：
值得注意的是，首次渲染的Mermaid图表出现了解析错误："parse error on line 8"。这是一个真实的、未加修饰的失败。Riley的应对方式很干脆——他立刻在提示中要求Ricky修正：

> "I'll simplify the node labels and re-render the diagram so it parses."

然后成功。这个过程看起来不算什么惊天动地的事，但实际上意义重大。它表明：**即使AI一次性生成的应用不完美，迭代修正的摩擦也已经低到几乎可以忽略不计。** 写代码、改BUG，全部变成了对话。

**个人感受**
当Ricky第一次开口说话，Riley的反应完全不像是在测试一台机器，更像在跟一个新认识的朋友聊天。他很自然地说"Very very cool. This is amazing."，仿佛不敢相信一个下午做出的东西能有这种完成度。

---

### 💡 四、从"粗糙"到"高级"：产品化的迭代艺术 `[07:00－12:00]`

**核心观点**
产品的真正价值不在于初版有多精致，而在于用户与开发AI之间形成高效迭代闭环。Riley展示了如何用自然语言做产品经理、设计师、测试工程师的工作。

**深度阐述**

Ricky的第一版虽然已经可以对话和生成图表，但Riley对它仍然很不满意——不是功能不够，而是**审美和交互体验**有待提升。

他直接打开Cursor，开始发出第二波指令。这段指令几乎可以说是一份完整的UI/UX评审报告，被封装成了自然语言：

1. **修复Mermaid解析错误**：确保不会再出现parse error。
2. **添加Exa Web Search**：让网络搜索正常运作。
3. **整体设计翻新**："I want the site to have less components... It's just kind of ugly. I want it to just have a simpler interface."
4. **布局修改**：这个要求非常具体——"左半屏放头像、右半屏放Artifacts面板"。而且因为动效僵硬，他要求"put some more time and effort into making the mouth move more realistically"。

**视觉结构描述**：
这里描述了一个重要的UI转型。初版的Ricky界面圆角元素过多，按钮分散（Connect、Voice、Display、Computer Use、Artifacts等各自独立）。Riley要求将这些全部精简成简洁的底部按钮，同时将Ricky头像从左上角的小角色放大到占据左半屏，右侧以一条竖线和Artifacts信息流分割，呈现简洁的50/50双栏布局。

结果怎样？在Riley粘贴了Exa API Key并发出指令后，Cursor理解了他的审美偏好、布局意图、交互逻辑——然后在一个迭代中重构了整个UI。

这个环节最值得注意的不是技术能力，而是**人与AI的关系**。在这段流程中，Riley扮演的是"产品负责人"的角色，而非"开发者"。他不用关心Mermaid是怎么渲染的，不用深掘前端JS代码，他只用描述需求、指出问题、设定审美标准——剩下的，Cursor全部消化并执行。

**延伸思考**
这不正是知识型工作者想要的未来吗？每个人都能管理自己的数字"员工"团队。产品经理可以用AI直接做出MVP，设计师可以直接实现交互原型，创业者可以直接把灵感变软件——语言正变成最高效的编程语言。

---

### 💡 五、控制权的让渡：从对话者到桌面操控者 `[12:00－15:00]`

**核心观点**
AI代理从信息提供者进化为行为执行者。Ricky进入Computer Use Mode后，可以直接操控用户的鼠标以及键盘，实现真正的"替人办事"。

**深度阐述**

这是整段视频中最令人惊艳的转折点。Riley对Ricky说：

> "Hey Jary, can you actually go into computer use mode?"
> "All right, switching into computer control mode now."

Ricky回答说它已经进入计算机控制模式。这一模式意味着AI不再只是对话和返回数据，它开始通过系统的辅助功能或自动化机制接管鼠标和键盘的控制权。

Riley决定测试这个能力的边界。他要求Ricky打开"Codex"（或同一段字幕中的"Codeex"，可能是一个本地开发IDE），Ricky照做了。紧接着，Riley要求它"type into Codeex to make the script better for the intro"——即直接在一个第三方应用内键入文本。

**安全验证机制**：
这里出现了一个非常真实、也相当合理的技术摩擦：Ricky每次执行敲击操作前，都要求获得用户的明确确认。

> "I can do that, but I need your explicit confirmation before typing into an app."

Riley在多次确认后顺利完成了操作，但同时他也提出了一个问题："When I go to use the computer use mode and I want it to type something, it asks me for approval every time. Is there a way to turn off that explicit approval mode?"

这段对话非常值得深入思考。它揭示了一个核心的矛盾：**自主性与安全性的博弈**。AI越有能力操控桌面，它就越需要权限；但权限越大，安全风险就越高。Riley找到这个安全选项并希望关掉的瞬间，实际上反映了高级用户的核心需求——在信任建立后，减少操作摩擦。这也暴露了AI工具在个人化使用场景中的伦理底线：如何在给予AI足够自由的同时，不交出系统控制权？

**UI的反馈式进化**：
更有趣的是，Riley接着要求Ricky在进入Computer Use Mode时，自动将窗口缩小为一个透明背景的小框，置于屏幕左下角。这样用户就能看到背后的全部桌面，而AI的头像仍可被看见和交互。

> "When I enter computer use mode, I want it to the window to get really small and take up the bottom left... background of the whole app should be translucent."

这不是AI自己提出的优化，而是用户基于使用体验制定的改进。Riley像一个真正的PM一样，不断向Cursor提出更精细的需求，然后Cursor执行。每次执行后的成果都会直接体现在Ricky的迭代版本中。

---

### 💡 六、杀手应用：语音驱动缩略图工厂 `[15:00－20:00]`

**核心观点**
Riley创造性地将一个常规的图片生成功能扩展为一个完整的语音驱动缩略图编辑流水线，展示了AI代理从通用工具走向垂直场景的潜力。

**深度阐述**

这是整段视频的技术高潮，也是最具产品价值的环节。在Ricky已经具备计算机控制、Web搜索和图表生成能力之后，Riley提出了一个大胆的想法：

> "I want you to be able to generate thumbnails of me using the GPT realtime image one. And then I want to be able to edit images... When I want to create a thumbnail, I want you to generate them in a grid."

这是一个极其精巧的功能设计：Riley上传了一张自己的照片作为参考，希望Ricky能利用这张照片，生成多个不同背景、不同道具、不同风格的视频缩略图——整个过程完全通过语音完成。

**网格与编号系统**：
Riley设计了一个"三列网格"布局。首张缩略图生成位置在左上角（位置一），后续每张图片依次编入网格。当用户说"Edit number two and make it do X"时，第二张图片会被选中并编辑，旧的版本被替换，新的版本自动填充到位置一。这样设计师就可以在同一个视觉空间中连续导航、编辑、迭代。

**实际交互展示**：
Riley用一系列连续的语音指令展示了这个系统的能力：

1. "Generate a thumbnail image of me standing in front of a tree. Cinematic view."
2. "Generate an image of me holding an iPhone... showing a really cool app."
3. "Generate an image of me holding a MacBook... showing a little blue character with cute white eyes."
4. "Can you pull up photo 13?"
5. "Can you please give him blue sunglasses?"
6. "Can you add text here that says cute character?"
7. "Can you please make the background outside like in the forest?"

这简直就是为内容创作者设计的完美工具。创作者不需要使用Photoshop、不需要画布、不需要界面，只需要声音——他们就能快速产出数十张具有差异化的缩略图，并反复精修其中的细节。

**个人感受**
当Riley看到这些缩略图在屏幕上生成、编号、被选中编辑时，他发出了由衷的感叹："This will be sick if we get it right." 这不是一个技术演示者的背诵台词，而是一个有真实需求的用户在测试自己亲手做出来的产品。他的兴奋是真实的，他的产品思维也是成熟的。

**延伸思考**
这个功能本质上是一个**"语音驱动的媒体管线"**。它把复杂的创意工作流程压缩成了"说一句话->看结果->再说一句话->看更新"的循环。对于需要大批量制作视觉素材的YouTuber、社交媒体经理、广告创意人员而言，这有可能大幅缩短从创意到成品的距离。

更重要的是，这个功能的全貌——包含网格系统、编号逻辑、编辑与替换逻辑、参考图管理——几乎全部都是通过自然语言对话传递给AI，并由AI自行编码实现的。这再次验证了该工作流的扩展性。

---

### 💡 七、开源与商业化：生态的双重逻辑 `[20:00－结尾]`

**核心观点**
Riley在完成全部演示后，将Ricky项目上传到GitHub，开放给所有人同步和克隆，并同步宣传自己团队的AI代理商业化咨询服务——形成开源社区+企业级服务的双重战略。

**深度阐述**

视频的最后五分钟，Riley从技术演示者转变为社区贡献者与创业顾问。

> "I'm going to take this entire project. I'm going to upload it on GitHub. And so you're going to be able to take the link, the GitHub link below and get feed it to cursor and say 'clone this' and you could create this exact Jarvis."

这步操作的意图非常清晰：降低入门门槛。任何人只要拿到GitHub链接，就可以一键复刻整个Ricky项目，在自己的电脑上运行和改造。

同时，Riley也放出了整个构建过程中使用的完整Prompt，他在文字描述中粘贴了这些文本，供创作者直接复制。这意味着：即使你不懂Git、Node.js、代码构建，你也可以复制Prompt，输入Cursor，然后等15分钟——你将获得一个与Ricky功能一致的AI代理。

在开源和普惠的基调之下，Riley也精准地做了自己的商业化转型宣传：

> "For the past few weeks, we've been helping companies get useful agents set up in their businesses. These are agents that can be shared with your entire team."

这里的逻辑衔接非常自然：个人用户可以免费构建自己的Ricky；企业用户如果有更深层次的需求（工作流自动化、团队共享Agent、接入企业内部系统），则可以寻求Riley工作室的专业服务。

**定位策略**：
"我们的团队可以入驻，分析你的所有工作流，找到Agent可以精简的地方，在广告、研究、内容、报告、内部文档等环节建立智能体。"

这段话暗示了Riley团队的业务模式，不是卖软件，不是卖SaaS，而是做"Agent原生组织转型的咨询/实施服务"。

**延伸思考**
这种"开源+企业咨询"的模式可能是AI时代技术创业的典型范式。个人开发者/小团队用生成式AI做出MVP并在社区公开（获取口碑和流量），同时利用企业级服务收费。开源代码解决"能不能用"的问题，企业服务解决"怎么用得好、用得安全"的问题。

---

## 精华收获

### 最有价值的洞察

1. **编程的壁垒正在瓦解**：你现在告诉一个AI你的想法，它就能为你构建应用。从想法到产品的过程精简为：描述+验证+迭代。Riley全程没有写一行代码，但完成了从设计到开发到产品的全部流程。

2. **AI代理不等于Chatbot**：真正的AI代理不仅仅是回答问题，而是能够感知环境、操作工具、执行动作。Ricky展示了从语音对话到桌面控制再到图像编辑的完整链条——AI从一个"信息提供者"进化为一个"数字劳动力"。

3. **产品化的核心在于迭代**：Ricky从首个粗糙版本到最后那个可以生成、编辑、管理16张缩略图的成熟应用之间，经历了至少4-5轮大幅迭代。每一轮迭代都是Riley对着Cursor"吐槽"，然后等待Cursor自行修改。失败和错误不是产品开发的障碍，而是产品迭代的燃料。

### 可行动的建议

- **不要等到学会编程再开始**：如果你有一个想法，直接下载Cursor，写一个清晰的产品需求文档式的Prompt，让AI帮你生成初版。等待成果，再基于观察到的不足继续对话修正。三个迭代以内，你可能就拥有了一个MVP（最小可行产品）。

- **善用"工具链Prompt"设计**：在给Cursor的Prompt中，不仅要说明功能需求，还要说清楚API密钥来源、UI风格偏好、交互逻辑细节。Riley的做法是："Look up the documentation" + "Read the docs on GPT Realtime 2" + "Design it like this"——把搜索和使用文档的任务也交给了AI。

- **关注安全与权限的边界**：当Agent获得计算机控制权后，安全验证机制是一把双刃剑。个人用户可能希望减少摩擦，企业部署则必须严格管控。在构建自己的Agent时，务必将权限控制设计成一个可选但默认开启的功能。

### 改变认知的关键点

- **"零编程"不是口号，是现实**：Riley用一个多小时的时间证明了这件事。从头到尾，他作为人类所做的唯一编程活动就是书写自然语言和粘贴API密钥。

- **AI代理不再只是概念，它可以很实用**：Ricky的缩略图工厂可能比很多现有的平面设计工具都更适合内容创作场景——因为它不需要任何界面交互，只需语音命令。这种交互方式可能重新定义创意软件的入口形态。

- **软件开发的"角色"正在被重新分配**：人类出想法、审美和策略，AI出编码和部署。这并非替代程序员，而是放大每个人的创造力。在一个AI可以完成60%-80%编程工作的世界里，真正稀缺的技能不再是如何敲代码，而是如何清晰地思考和表达。

---

Riley Brown在这段视频中没有空谈概念——他从第一行操作开始，完美展示了自己从一个账户登录到拥有一个完整桌面AI伙伴的全流程。他的兴奋、他对失败的坦然、他对产品的控制力、以及他最终将成果开源和商业化的双重逻辑，共同勾勒出了当前AI时代技术创作者的新画像。

如果你也想拥有一台属于你的桌面Jarvis（或者叫Ricky、Jary还是其他什么名字），现在你需要的不是数年的编程教育，而是一台下载好Cursor的电脑、50分钟晚餐等待时间、以及一个清晰的、有愿景的对话。

那句Riley笑着对Ricky说的话也完全可以用来形容整个视频带给观众的感觉：

> "This is pretty cool."

是的，确实如此。

---

<!-- TLDR: 任何人都能用自然语言和零编程经验，在Cursor中构建一个桌面版AI贾维斯。 -->
<!-- TAGS: AI代理, Cursor, GPT实时语音, 零代码构建, 桌面自动化 -->
<!-- RATING: 5 -->
