---
title: "【十字路口】人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy 【视频播客】 - 结构化文稿"
channel: "Koji Yang"
published: "2026-05-20"
source_url: "https://www.youtube.com/watch?v=Kmpj5KUfIew"
video_id: "Kmpj5KUfIew"
variant: "structured"
---

# 【十字路口】人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy 【视频播客】 - 结构化文稿

- **Channel:** Koji Yang
- **Published:** 2026-05-20
- **Source:** https://www.youtube.com/watch?v=Kmpj5KUfIew
- **Main:** [【十字路口】人类和 AI Agent 的最佳配合方式，还没被发明｜对谈 Paperboy 【视频播客】](2026-05-20-【十字路口】人类和-ai-agent-的最佳配合方式,还没被发明-对谈-paperboy-【视频播客】-Kmpj5KUfIew.md)

# 人类和 AI Agent 的最佳配合方式，还没被发明｜对话 Paperboy 创始人

## 开场与嘉宾介绍

嗨，我是 Koji。本周《十字路口》请到的嘉宾是 **Paperboy** 的创始人江洋，以及他们的一位 Founding Engineer，Jet 陈。

**Koji：** 你好二位，欢迎来到十字路口。

**江洋 & Jet：** Hello Koji，感谢。Hello。

在这里也给大家说明一下，因为江用英文表达会比较自然，所以我们这一期的内容会比较中英夹杂。我们同时有音频和视频，如果大家需要的话可以去看视频，看视频我们会配字幕和字幕翻译，帮助大家理解。

---

## 快问快答环节

我们还是从《十字路口》的传统快问快答开始。

### 年龄

**Koji：** 有请二位的年龄。

**江洋：** Oh, I'm 21.

**Jet：** 19.

### 毕业院校

**Koji：** 你们的毕业院校。

**江洋：** Maybe I'm Pratt Institute. I studied Architecture.

**Jet：** 我是上海星河湾双语学校高中毕业，然后现在在 **CMU**（卡内基梅隆大学）读大一，大一刚结束。

### MBTI 与星座

**Koji：** 你们的 MBTI 和星座是什么？

**江洋：** ISTJ，双子座。

**Jet：** INTJ，处女座。

### 创业之前的经历

**Koji：** 创业之前你们做了一些什么？

**江洋：** Paperboy 是我第二家公司。我的第一家公司叫 **Mellian**，我们是在 React ecosystem 做了很多开源的 dev tools。然后我们做了一个产品叫 **Same.dev**，普通人可以用一句话输入一个 URL，然后做出和任何网站一模一样的一个 UI。And Mellian was in **YC Winter 24**.

**Jet：** 我在 Paperboy 之前是个高中生。我比较喜欢做开源项目，然后我喜欢打 **CTF**（Capture The Flag，网络安全夺旗赛）。我做了一个东西叫 **Earthkit**：你拍一张照片，然后我用多模态去推测这个照片在哪里拍出来的，会比传统的卷积神经网络模型更好。

**Koji：** 那是哪一年？

**Jet：** 差不多一两年前。

---

## Paperboy 是什么？

**Koji：** 那我们来介绍一下，Paperboy 是一个什么样的产品？

**江洋：** Paperboy is a company just started broadly with the mission of——我正在试图找出**我最喜欢的和 AI 一起合作的方式**。我对去年做了 Same 以后，用过很多产品，都有那么一些不爽。

So yeah, Paperboy just started with me trying to hack around different approaches to try to figure out how to solve the technical problems here. But also form factor——我应该需要把自己的文件、还有 Email，还有 all this personal information，丢到一个聊天框里。

- 如果我需要和别人一起合作，同时跟一个 Agent 对话，there should be a very easy way for me and for us to collaborate within the same context window.
- Agents 如果知道了我很多信息以后，他应该可以 **proactive**（主动地）提前去帮我做一些事情。但是现在的 context window，you really can't do it.
- 还有就是，现在所有产品都是 **session based**（基于会话的）。So session 一丢，你就找不到过去要从哪个 context window 继续聊下去了。
So just all kinds of these problems——generally speaking, it's a gap between model capabilities and deployment. And I feel like there's still a large opportunity to explore and innovate on the product experience. And the name is Paperboy.

### 融资、收入与发布计划

**Koji：** 你们的融资情况是什么？

**江洋：** We raised **$4.7M at 25**（2500 万美元估值下融资 470 万美元）。

**Koji：** 收入和利润呢？现在还没有发布对吧？

**江洋：** Zero and negative gross margins, and we lose money every day.

**Koji：** 估计什么时候会发布产品让大家用到？

**江洋：** So we shipped the prototype to friends. That's like our agent that learns from OS activities, but there are cost issues——it's too expensive, it doesn't really work. So the next iteration of this product, we're trying to wrap it up by this month. And we're going to try to go to market again. 我发播客的时候会放一个链接在下面，大家感兴趣可以去 signup 一下。

**Jet：** Oh yeah, you guys will see it I think when this podcast comes out.

### 团队规模

**Koji：** 咱们目前团队规模呢？

**江洋：** 现在有 **12 个全职员工**，然后是 10 位 engineer。

---

## 核心理念：最佳人机协作方式尚未被发明

**Koji：** 我记得第一次见到江的时候，你给我看了一个文档，那是你写出来给内部开会用的会议文档。第一句话你说：**人类和 AI 配合工作的最佳方式很可能还没有被发明出来**。写这句话的时候你看到了什么？到今天，你觉得你看到的事情有发生一些变化吗？

**江洋：** Yeah, so that doc is the one I prepared for our very first all-hands. 那个时候公司就我、杜克、Jet，四位。And December 30th. And yeah, I think we just started working with one thesis, which is: **the best way to work with AI hasn't been invented**, and we have a shot at being the team that figures out that way.

So started really trying to figure out what's the best way to code with AI. And we have been largely successful, being I think the first company to really approach on that goal. And we figured out how important it was to focus on that goal post before everybody else.

你问我从那句话说到现在还有什么新的学习？I think what's cool is——这其实是一个 **moving goal post**（不断移动的目标）。The market's expectation——you can't really reach it, you can only keep getting better. Because every time you come out with something new, everybody else sees it. And if the other teams have taste, or users have taste, they will know. And they will see the friction points——there will always be frictions. So all you have to do is just keep getting better.

### 如何看待“王炸”频出的 AI 创业环境

**Koji：** 其实最近很多 founder 感到有一点绝望，因为在创业过程中不断有新的“王炸”出现。从你们创立公司到现在这半年，又是变化非常剧烈的半年——从 Claude Code 到 Open Claw，再到 Arms。你的感受是什么？一开始想象要做的东西，和今天在做的东西，有没有因为这些新的庞然大物出现而发生剧烈变化？

**江洋：** 还真没有什么剧烈的变化。Because I think the problem space comes from people. How I think about this problem space from a technical and product point of view is **three categories of problems**:

1. **Technology**：Agents 要能够 actually learn from the user's environment. It has to be integrated into what a user already works with. Where the data comes from——lots of files on your computer and integrations.
1. **Personalization**：Personalization means you don't really have to prompt it as much. You can trust it to work on more and more complex and difficult things. You can trust it to make more higher-stakes decisions. And it also means being more reliable. That means you can actually use the model and just keep running it for longer and longer periods.
1. **Intuitive design**：From a design point of view, it needs to be extremely intuitive to use. You shouldn't have to learn it as a new tool. If your agents are proactive, they can bring up new ideas by themselves. What is the form that holds all of these proactive outputs together? It has to be within the environment, and it needs to be personalized, and it needs to be collaborative with your existing team.
So when you look at new tools that have come out, there's not really a new dimension that's come out yet, because these three dimensions are limited by the human teams.

---

## 为什么要给 Paperboy 一次机会？

**Koji：** 我们要不要非常简单地安利一下大家，为什么要用 Paperboy？因为听我们播客的很多人可能已经是重度 **Claude Code** 或 **Minus** 或其他 Agent 的用户。为什么要在这个时候给 Paperboy 一次机会？

**江洋：** Yeah, so right now Claude Code and Minus, to me, they're kind of the most successful forms of agents out there. They are **session based** and they are **one-to-one**, prompt based. So there are two very important factors here:

### 现有产品的两个核心问题

**Session based** 意味着：在你的 sidebar 里，有一堆 workspaces（项目），每个 project 下面有一堆 sessions。每次你想让模型做新的事情，你就开始一个新的 session，然后它被归类到你的 workspace 里。

第二个问题是：你与模型互动的方式是——你输入 prompt，然后等待，然后你发送下一条消息，再来一个 turn，再来一条消息。

**问题在于**：

- 这个 agent 是 **reactive**（被动的）。你必须要非常具体。你可以创建一堆 skills 或 doc agent stock MD files 来描述你在做什么，但你必须主动维护它。
- 而且，无论你投入多少精力去维护，都很难把你所知道的关于自己的 taste、judgment 以及你认为的最佳做事方式，全部翻译到这些 raw text files 里。
- 另外，**sessions 不是连续的**。这很糟糕。很多人可能有几百甚至几千个 sessions。我知道过去有一些 session 的 context window 里可能包含了非常有价值的 insight，但如果我没有刻意保存——“这是这个项目所有 session 中最重要的部分，我们需要把它带到未来”——那么那个 session 就丢失了。
### Paperboy 的解决方案

So, to me, that's what Paperboy is. We handle these two problems head-on:

1. **Agents 必须通过观察你如何使用电脑来自主学习。** 这包括你所有的信息：screenshots、keystrokes、mouse movements、你的 meetings（包括视频和音频）、你的浏览历史、iMessage。当然，你可以选择给 Paperboy 访问哪些权限。
1. **需要存在于具有持久对话历史的聊天中**，这些对话历史要比一个 context window 长得多。而且这个 chat 需要是可搜索的。这个形式其实就是——像打开 iMessage、打开微信一样，你有一堆 chats，然后你进入某个 chat，与其中的参与者持续对话。
### 关于 Session 和 Context Window 的补充

**Jet：** 我觉得还有一点需要补充一下关于 session 和 context window 的事情。现在类似 Claude Code 这种产品，你可以 argue 说它们有无限的 context window，因为它们有 compaction。而且也有更新的产品，比如一家叫 Interaction 公司出的 **Poke**、**The Computer**，甚至 Open Claw，它们也是以“不存在 session，但你一直是一个 chat”的形式去做 Agent 和 Human 的 interaction。

但是对 Paperboy 来说，我们和这类产品的一个主要区分点是：

- 这类产品的 context 来源，主要是基于用户和 Agent 过去的 chat history，纯粹从这里去 learn。
- 还有一个是，如果用户给这些 Agent 比如你的 Email 或 Messages 之类，它们也可以通过读这些 Email 去逐渐更 personalized 地学习用户的更多信息。
但是我们一开始做的 prototype 也试图去导出用户所有的微信聊天数据或 iMessage 的所有聊天数据，但我们很快就发现这**并不是一个非常 scalable 的方式**。

最 scalable 的方式是：**通过观测用户在日常使用电脑时，从 OS 层面去 collect user data**。我们发现这样会对用户每天做什么事情有一个非常非常全面的了解。而且按照信息的浓度来说，用户一般的 computer use，信息浓度是非常高的——你只要观察用户用电脑差不多 60 分钟，就可以学习到用户很多的信息。但如果你只观察用户过去 60 分钟的微信聊天数据，其实学不到太多东西。所以我们很早就是 bet：通过 **OS 层面的 context** 去做 user adaptation。

---

## 关于 Context 收集的行业共识与差异

**Koji：** 其实《十字路口》之前有一些播客的嘉宾，**Airgyle** 的 founder，他们在做的也是一个 Mac 或 Windows 的桌面客户端，以此来 capture 用户尽可能多的上下文和电脑使用习惯。然后最近 OpenAI 应该也出了 **Chronicle**，其实也是类似的想法——用桌面客户端来抓尽可能多的上下文。所以你们在做的时候，和大家是类似的实践吗？还是有什么不一样的想法和做法？

**江洋：** 从 Mac 还有用户使用的电脑上抓取 raw data 并 processing it into memory，这是一个 general thing，未来都会发生。不只是 startups 在 deliberately focused 做这件事（比如 Airgyle），Codeacts、Claude Code 等等，它们都会做。这就像是**最明显的下一个 context 的前沿**。

But of course, **how people treat that raw stream and data, and how it gets processed, will happen very differently**. What you choose to structure and how you choose to structure that information is directly related to the application of the agents.

So, what every individual agent and what your application actually decides to help the user on——you shouldn't probably structure and compress the raw activity stream in the same ways.

So just that alone, you're probably going to have a company that's hyper focused, for example, on studying how a user replies to emails. Then they're probably going to have a different memory structure, a different way of compressing the raw emails that they learn from.

**The action space is big enough** that there is enough room right now to be the first to get to that——in terms of really understanding who the user is across all their application services and across their relationships, and then you can sort of model what the user actually does within a day.

**Jet：** 我也认为，现在通过收集用户屏幕数据或 computer use 去 build context，已经一定程度上成为了一个**行业共识**。然后后面更重要的是：**你在这个范式下具体去做什么事情**。

- 目前像是 Codex 或者说 Little Bird 这种，他们会把屏幕数据当做一个 context layer。就比如说对于 Codex Chronicle，它目前的 use case 是：你可以通过收集用户屏幕数据去学习用户一般是怎么 develop 这个 application 的。
- 如果你的 use case 不一样，你最后的 pipeline 也会不一样。
我觉得这是一个非常非常新的 domain。在你做好基础的收集用户屏幕数据和 computer use 的情况下，你其实还可以干非常非常多的其他事情，这需要非常多的 engineering 和 research。

比如说：**你如何做最好的 proactive Agents？** 你是该预测用户下一个 keystroke？还是预测用户每隔一个小时去干什么？还是去预测什么其他的事情？这些都是 relatively 没有被很好 explored 的 problem space。目前我也没有任何人发现一个绝对最好的 recipe 去干这件事情。所以说，目前对于一个公司来说，去探索这个 AI 还是一个非常好的选择。

---

## 用户第一小时的体验：Meeting Prep

**Koji：** 如果今天用户安装了 Paperboy，他立即会在第一个小时、甚至前面五分钟感受到的最大价值是什么？你们期待用户在第一时间感受到的差异和价值，从而能够留下来——就这一个 highlight 点是什么？

**江洋：** We're probably going to start with **meeting prep**. 一个小时很重要，就是你要 demonstrate 给用户一个框框 of what your product can do. You don't have to set expectation.

One thing with Paperboy: **it gets better the longer you use it**. So you need that initial period where the user trusts it to learn.

So you're going to open it up, you're going to see a chat box——not a prompt box, but a literal chat window. Once you give it permissions to say your calendar, emails, it's going to just start reading what you give it. Then it's going to ask a little bit of a question about who you are from the context of reading that. Then it's going to start giving you a couple of suggestions: "Hey, I see this meeting coming up. Do you want me to look into it for you?"

**Jet：** 这方面其实我觉得做的最好的是 **Poke by Interaction**。They sort of figured out the recipe here, which is: you just connect to the user's existing context, and you need to show the user you're an agent that can actually engage with the personality and proactively, in a non-annoying manner, to help the user. So you get the user into this expectation that we are the agent that can actually text you in a way that makes sense.

---

## 团队自己的 Aha Moment

**Koji：** 你们二位或者整个团队用 Paperboy 用了多久了？在你们自己用的过程中，有没有什么可以分享的 Aha moment？

### Auto John 与 Mini Vivian

**江洋：** Yeah, so Vivian is also here. Hello. Vivian is very funny. She joined from 小红书，之前她在红杉的 Yue.

So we have:

- **Vivian's Paperboy** is called **Mini Vivian**
- **My Paperboy** is called **Auto John**
And they exist in Slack right now. All the time, teammates on Paperboy would just ask Auto John questions. So it's able to handle all the incoming questions and help teammates——product team, design team——find the help that they need.

For Mini Vivian, for example, Vivian does a lot of recruiting work. So Mini Vivian is the recruiting intern for her on the team. Because Mini Vivian actually understands everything that I have ever said to it across meetings and Slack, which includes my judgment and taste on what kind of candidates we're trying to hire and where one source was from. It's able to actually help Vivian surface these candidates across GitHub, 小红书, Twitter. So I think that's saved her a lot of time.

I think Vivian since February has not used Claude. She can't use Claude because it just doesn't know. You can't use Claude to research candidates for you——there are so many things you would have to tell it about the judgment of the person.

**Koji：** 因为它有了更多的 context，所以你其实在给它 prompt 的时候，你甚至可以不 prompt？

**江洋：** Yeah, **I hate prompting**. From Same 开始，I just did not want to prompt. I think prompting is——I mean, you have to communicate. But people, we don't think in prompts. We send texts, and we expect the other person to know what we're talking about. And we enjoy a relationship when the communication is high bandwidth.

We also enjoy——I think smart people enjoy being told what we don't know. Especially what we don't know we don't know. And today's models are smarter than we are. So yeah, frankly, I look forward to the day when I can just lay back and Auto John is the smarter, higher-IQ existence than I am.

### Jet 的 Aha Moment

**Koji：** 那 Jet 呢？你有一些什么样的 Aha moment 在用 Paperboy 的过程中？

**Jet：** 首先就是，确实很多时候和江的那个 **Auto John** 聊天，会比和江聊天好。

**Koji：** 但你跟 Auto John（它的 Agent 替身）对话的时候，你会担心它的意志目前还不能完全地代表江，从而产生一些 misunderstanding？

**江洋：** So the way I look at it——not just because we are creators of this thing——but the user has to be responsible for their agent eventually.

So how Auto John gets set up: it's not like one day, boom, you have this existence that you can bring into Slack. There is an **onboarding process** where the agent does actually ask you questions. It asks questions like: "Okay, how much am I allowed to share to this specific person?" By default, it mirrors——for example, I share a lot with Jet. Maybe I don't share as much with a new engineering hire. And the agent actually knows that from observing all my chats.

**Jet：** 而且我觉得，和一个人 interact 其实有很多种方式：

- 有时候我纯粹就是和江在聊天。
- 或者说我希望去做一个事情，我没有权限，我希望江去 approve 一个东西。这些我觉得目前可能不会去跟 Auto John 说。
但是实际上在工作场景中，你很多时候和对方的 communication 是说：江它有整个对 Paperboy 一个公司的 context。然后我作为一个工程师或 IC，我每天需要的是：我如何能对这个公司产生最大价值？我去做什么 research 或做什么 engineering 是最有用的？

然后这个时候，因为这个 Agent：

1. **Factually**，它有江有的大部分 context
1. 它通过观测江工作的时候，它的 **heuristics** 其实和江的 heuristics 是比较类似的
所以说，在做决策的时候，关于 context 和 heuristics 方面的东西，我觉得 Auto John 是比较有用的。

### Text Completion 的 Aha Moment

**Jet：** 其他的 Aha moment 对我来说，第一个 Aha moment 其实比较早，就是我们做出 **text completion** 的时候，对我平常编程就已经挺有用的。

我平常使用——现在有很多 AI terminal 很火，AI 命令行很火，但实际上那些命令行不如很多传统的命令行做得流畅。但是传统的命令行很多时候并没有 AI integration，然后很多时候你去写脚本会很烦。

但是我们做出 text completion 的时候，我完全可以：写完一堆代码，然后我要去发一个 Git Commit 的时候，我直接在命令行里面输入 **@PB Commit**，它就会自动把整个 commit message 写好，然后我 Enter 就可以发一个 commit。

### 这个 Feature 展开讲讲

**Koji：** 这要不要稍微展开讲一讲？这是一个什么样的 feature？因为刚开始我们没有介绍到。

**Jet：** OK, OK。我们 Paperboy 的开发流程大概是：

1. 先把收集操作系统用户数据，到形成一个比较好的 memory system 这一套做出来。
1. 做出这套系统之后，我们在工程上有一个 framework。我们会有一个比较好的 **markdown document**，它是会实时更新的。它包括：
离用户现在在做的事情越近，它的 **granularity**（颗粒度）会更好，更细。

所以说，我们 Paperboy Agent 一直会有这个 context。我们有了这堆 context 之后，我们在做一件事：**寻找应用场景**。我们找到的第一个比较好的应用场景就是：**我们可以在操作系统任何一个地方做 auto complete**。

- 就比如说你在发微信的时候，你可以在文字框里面输入 **@PB**（激活词），然后后面输入一个比较简短的 instruction 或 prompt。
- 你也可以不输入。
**Koji：** 它就会猜——你在这个时候“@”我，找我了对吧？你不输入它也会猜一猜你此刻找我是要我来干嘛？

**Jet：** 对，因为它有这个 context。

**江洋：** 比如说有一个同事过来，可能我不需要对他说什么，就一个眼神，他就懂了为什么我去找他。That's a great analogy.

**Jet：** 就比如说你很多时候和你的工程师，你并不需要描述，你需要点一下屏幕，就指下屏幕，他就知道——“看这”。

**江洋：** 对，看这。看一看就哦，就这个问题。

**Jet：** 对。当时 Paperboy 已经差不多达到这个效果。

所以说，不管你在回微信的时候、做任何事情的时候，它都会实时地有这个 context。

然后对我来说 Aha 就是：在命令行里面，或者说甚至在 GitHub 里面我会发 PR，然后它可以直接把整个 PR description 都给你做出来。很多时候我发现，它那个 PR 实际上会比 Cursor 或传统 code 的更好。因为很多时候：

- 我开发一个比较大的 feature
- 一会和 Claude Code 打交道
- 一会我在微信里面和江发消息
- 一会我在浏览器里面做 research
我也可以把这所有的 context 都聚合在一起，并以一个 PR 的形式去给我做这个 draft。我会发现，它对我去做什么事情的理解程度，会比任何基于单一应用 context 的 Agent 或 AI 好很多。

### Paperboy 作为“效率监督员”

**Koji：** 还有吗？

**Jet：** 我自我怀疑我有 **ADHD**（注意缺陷多动障碍）。我在工作的时候很容易分心。我经常在写 code 的时候旁边会看 Hacker News，Hacker News 如果有什么比较有意思的文章，我可能点那个文章，看了 30 分钟回来，Claude Code 可能已经结束了十几分钟了。

对于这种情况，我记得我当时每天晚上会让 Paperboy 给我一个 report，说**我今天到底有多 efficient**。我让它去骂我——我什么时候不够高效，我什么时候分神了。对我来说，我平常工作的时候，当知道 Paperboy 在盯着我工作的时候，我会效率更高。

**Koji：** 哦，就不是 Big Brother is watching you？

### 江洋的 Aha Moment：连接点

**江洋：** A large portion of my job now is to use different products and also to do research and talk to people. Unfortunately, I can't code as much as I used to anymore.

But Paperboy is great because it actually keeps all of that different information granularity sources in its head. So when I want to go learn about something——for example, to learn about 微信的历史，还有各种不同的 network effects businesses，successes and failures——after I've done the research, I want to actually connect it back to Paperboy.

At that point, I really have a bunch of things just happening in my head, and I need something to help me write it through. It's like **connecting the dots**. And then be able to tell me: "Wait, have you thought about this real quick? You tried this a couple months ago, and this is the product form, and these are the problems that you recognized in the product."

I know about these things, but when you're doing that sort of thinking across different planes, you can do it manually——I should just sit myself in front of a piece of paper, I can sketch it out——but it's a lot faster to be able to have a very smart model that knows me to help me through that process.

**Koji：** 所以这里有一个例子吗？最近一次给你这样的 inspiration？

**江洋：** Yeah. Paperboy——we started working on this new, the latest interface two weeks ago.

I was talking a little bit about problems we had. For example, if you're shipping Paperboy to VC (VC is definitely part of our ICP):

- They want a personal CRM module.
- They want a "meetings coming up" module.
- They want a "deals of the quarter" or "deals through" module.
- They want to keep track of everything that's happening across all of the portfolio companies.
- They want to keep track of their relationships with LPs.
So maybe you can ship a sidebar where you have these existing modules in place. But then the question is: okay, we know this thing works for operators, for founders, for real estate salesmen. They all need a different sidebar. So what do we do? Do we ship these things as skills, as plugins, as recipes? And allow the user to pick which one they want to add into their product?

### 从 IM 获得的界面灵感

**江洋：** That didn't make a lot of sense to me. So Paperboy pointed out to me: what application do we use that is——well, it's obviously you're going to need a list, but it's an infinite list, but it's actually not annoying.

And then it came back to sort of the **IM idea**. When you think about what's going on in our iMessage and WeChat today——WeChat especially in China——there are contacts and there are a bunch of group chats. And then there are group chats where it's sort of like maybe you have three people, but your three people can have four group chats for different topics. And it's actually a very intuitive way for people to organize their topics and things that are going on.

**Koji：** 实际上我们每一期播客会拉一个新的 group。

**江洋：** Yeah. 每一个 group 里面是固定的那几个。因为江好几期播客在同时做后期的处理，一开始发现它在同一个群里面会超级混乱。所以每次我们开一个新的播客就开一个新的 group，大家同时进这个新 group。

And the great thing about IM is：你不在那个 group 里聊天了，它就被推掉了。你也可以选择右键或滑一下隐藏——I did that all the time. So my WeChat is sort of like an inbox.

So that was kind of the inspiration. We know we also need an inbox feature. So what if we don't design an inbox feature, we just turn what is the thing that itself is an inbox? It's IM. So that's kind of how the latest interface came about.

---

## 如何看待竞争？

**Koji：** 其实我们在讲的时候，如果大家没有用过 Paperboy，可能需要一些脑补。我们已经安利了非常多 Paperboy 与众不同的功能、特性，以及很独特的交互理念和设计。

正好也在这里讨论一下：像我们刚才讲到的，capture 所有的 context 是一个共识，大家都会做。然后我们刚才提到的一些新的交互范式或思考，我觉得如果它真的 make sense，大家也会很快地追上来、补上来。

所以想问问二位：**怎么看待竞争？** 你们觉得最主要的竞争对手是谁？以及你们如何在竞争里面保持持续的优势和差异？

**江洋：** Only two that matters today are **OpenAI and Anthropic**. Everybody else is behind them.

And they have all the advantages:

- They actually own the models.
- Anthropic got new compute now.
- They have great distribution.
All we can pray for is we're like **Crusoe**——where we have some edge in **taste**. Where we beat them to this new interface. And all of that is for individuals and product experience——that's not going to go away.

But then also a second thing is **enterprise**. They will definitely want to go into enterprise——it's where the money is.

Paperboy 其实最想做的第一个产品是 **AI Slack**。That was our answer initially to "what to build" if the best way to work with Agents hasn't been invented yet.

### 如何看待 AI Slack 赛道？

**Koji：** 对，所以这也是现在非常热门的一个赛道。有很多产品都在尝试解决：当 Agent 进入团队以后，我们应该 build 一个什么样的产品去工作？你怎么看现在市场上一些大家讨论比较多的产品？比如说 **Slack、Monki、Marks** 等等，有没有你想讲的？

**江洋：** First of all, I love Slack. I think Stewart is brilliant, he has great background, his co-founders are great, and now they're building up a product team as well.

The hard part about AI Slack——and this is from my personal POV——is: **how do you get enterprise to switch?**

- AI Slack's business model that makes sense is: you have to sell it to a team. It's the team that's paying for it.
- For enterprise, if there is a way to export all of the data from Slack and import it into AI Slack for a one-to-one experience, then maybe it can work. But you still have to build a bunch of connectors, integrators for all the other data that enterprise has. So that infra work is not going away.
The second thing is that **Slack is honestly not a great product**. If you just try to build an interface that's similar to Slack with channels and threads——to me, I don't enjoy using it. Obviously at scale you kind of have to switch to it because nothing better exists right now. But it's not an enjoyable product to use.

Then there's the Agents. As Jet said, we don't believe that the learning rate of the Agents——if the only sources that they get for understanding how to work with people comes from the messages you sent to them——is sufficient. People with jobs are busy. They do not have time to care about training Agents. They expect things to work for them out of the box. They expect the product to keep getting better.

And the reason we went away from Slack is that the Agents in Slack still need more context for them to learn naturally.

**Jet：** 我觉得 Slack 其实还是有蛮多 **network effect**（网络效应），就像前面江说的，来阻止它们被新的 player 替代掉。

就比如说 Slack 它还有一个功能叫 **external connections**。目前所有比较认真的公司其实都会用 Slack，然后公司和公司之间的交流现在很大程度上并不是 Email，而是通过 external connections 去进行。这个是很难被替代的。我觉得 Slack 肯定还有很多其他 integration 方面的 network effect，就和现在微信一样，让它们到了一个某种程度上不可替代的方式。

相比来说，如果你去把 Agent 作为一个 **layer above**，在 OS 层面或和 Slack 形成一个互补形式的东西，我觉得反而会有更好的 adoption story。

**Koji：** 所以这是你们在做的事情吗？尝试去和 Slack 有一些互补？

**江洋：** Yeah, we assumed that initially if you try to go into enterprise, they will be communicating on Slack. If you're building a Slack right now, you can't really try to sell it to a team larger than maybe 50 people——it would take too much work for them to switch off of Slack.

And it makes more sense to **bring the Agents to where people already work**, instead of trying to replace and build everything from scratch.

---

## The Last Interface：五种速度

**Koji：** 我有注意到 Paperboy 目前的官网，产品还没有发布，但你们放了一篇 blog post，标题叫 **"The Last Interface"**。在那篇 blog 里提到 **five kinds of speed**（五种速度），可不可以稍微展开一下？我理解这背后好像是在讲你们如何理解今天的 context layer 和整个 memory system 等等。

**江洋：** Yeah, I don't want to go into too much detail because actually the choice of saying "five" isn't because we only have five layers——it's just a sensible categorization.

The important thing is: if you think about——in SF, there is a nonprofit called the **Long Now Foundation**, and its founder Stewart Brand published something called **pace layers**. It's sort of like:

- At the top: fashion
- Then commerce
- Politics or governance
- Then infra
- Then civilization / nature
These are six paces that change at different velocities. Fashion obviously changes the fastest. Nature——our understanding is that it doesn't really change, right? Physics.

The world is made up of these different paces, and they all have a relationship with each other——reflexive relationships between every layer. And largely, that makes up our society. I have been kind of fascinated with that since high school, and it's influenced my worldview of what the world is, both the natural and social silos.

And when I think about what's actually efficient and what can scale for representing this world we live in in the Agents' world——you need these different pace layers too.

**Jet：** 我觉得对于产品来说，如果你把用户做的那些 task 的长度去做一个分类，其实会有蛮多不同的种类。

- spectrum 的一端：用户在微信上回一条消息，只需要一秒钟或十秒钟。
- spectrum 的另一端：用户去读 10 个非常长的 report，然后做一个 business decision，做一个决策，这可能要花几个小时。
- 更长的：over a month（超过一个月）。
基本上有一个 spectrum。我们认为这个 spectrum 的每一段都会去被某种 AI agent 去 augment 或自动化掉。但是每一段需要做的事情不一定是一样的。

- 如果你要去自动化用户回复微信的这个 task，你有可能最好的 form factor 是：你点到微信的回复界面，它会自动 pop 一个 auto complete。这个我们已经在做。
- 但随着时间的推移越来越长，产品形态就会越来越不确定。自动化用户一个几小时 task 的最好的 form factor 是什么？这个我觉得目前还是一个非常值得被探索的区域。
---

## 超越年龄的成熟：江洋的状态从何而来？

**Koji：** 其实在录这期播客之前，我和 Paperboy 的团队也有一些交流，然后我发现团队里面好几个成员都有讲说，他们认为每次和江沟通的时候，感觉不到他是 04 年的，觉得他有超越年龄的成熟。我其实也有这样的感觉。我想问一下江，你觉得自己的这个状态是怎么来的？是因为你过去做了什么，或者看了什么，或者被什么激发、激励？

**江洋：** I think I'm still a pretty childish person. Especially with Jet around——we have a lot of fun together.

**Jet：** I think you're old.

**江洋：** 我大你。

I think for the team at least, I definitely just have a **passion for business**. We are trying to do something very hard in a very short amount of time. So clarity, efficiency, and focus.

**Koji：** 那要怎么做到呢？这个是异形难。

**江洋：** Well, it starts from me. My number one job is to bring to the team what define what success looks like, and be able to make sure that the context every person has about their goals and how they're actually operating are complete and accurate.

Actually, even for me, the best part of being able to start a company is to get to learn so much of what I've always wanted to explore and to just understand about the world. And **that curiosity** has probably been the biggest driver for me since high school.

Between high school and college, I took a couple internships at different companies. I just do different types of problem-solving activities. And then Mellian——we started in the B2B business, selling web performance PR bots to large enterprises. And we learned that is a difficult business to scale——we as 20-year-olds are not good at scaling up our enterprise relationships.

So since then, I think I've been on this trajectory of just trying to learn about: what are the markets that actually make sense for different players? And the way I like to learn is not just for startups, but across different business scales——founder-market fit, team-market fit.

So I think **market picking is one of the most important, if not the most important, trade of a founder early on**. It's making sure that you understand what you are going into: where are all the leverage points? Where are all the challenges coming down on you? Then you can actually go build a team, and then it's a product experience, phoning customers, technology.

### 如何选择一个正确的市场？

**Koji：** 所以这里有什么可以分享的吗？如何去 choose a market, the right market？

**江洋：** Yeah, I think I'm about to say a bunch of common sense again but:

- It has to be **big enough**. And this "big" isn't just dollar sign, but **how sustainable is the market**? That scale has to keep increasing so your team can continuously develop your product and your market position across a decade.
- So when I look at the most successful products in history, it's never a single product. It's actually a product lineup where the expectation is: when you build this thing, it's going to take maybe a decade for it to get to a form where it's really mass consumer or everybody's using it.
- You got to start with a **problem close to you**.
- But then you need a lot of history to be able to understand if the business dynamics, the economics, are actually favorable and there have been success cases in the past or not.
There are so many details, and I think I am just barely scratching the surface. Paperboy is just my chance to kind of prove out what I know.

---

## 第一次做 CEO：最大的变化与挑战

**Koji：** 我觉得 Paperboy 应该是你第一次做 CEO（上一家公司是 Co-founder）。所以做 CEO 之后，你觉得自己最大的变化是什么？

**江洋：** Man, it's **fucking hard**. I got to own everything.

- As Co-founder, you definitely feel that too. I get frustrated when an engineer, for example, wastes an afternoon.
- But as CEO, **I am actually the person that can cause the company the most amount of money**, because I have so much leverage. If I say "we go do this" and that is actually not a good idea——it's the position where literally all of your ideas can have such a large cost and rewards.
- As the team scales, obviously, who do I choose to hire? Where do they come from? Once they're hired, how do you continuously improve together for the individual and for the team? Making sure every person is on the road that they deserve.
I feel like these are basic management skills. This is basically my first time as manager too. So a lot of that I have to figure out on the spot:

- How do you give performance reviews?
- How do you have one-on-ones?
- How do you make sure that sometimes I have to just talk to the team leader and not to every single one and micromanage?
### 从哪里学习管理技巧？

**Koji：** 那你是从哪里来学这些管理技巧？刚才提到怎么开会、怎么做 one-on-one、怎么做 performance review，你是用什么方式在学的？

**江洋：** Before Paperboy, the one stint I had where I actually stayed at a larger company was **Minus**. Minus——Panpan is an amazing CTO. I haven't worked with any other real engineering managers, but he is a great engineering manager. And we had the opportunity when I was at Minus to have a couple one-on-ones where I just asked him all the questions I wanted to ask about how to organize everything.

And also spent time just reading. I think the best management book I've ever read is still **"High Output Management" by Andy Grove**. And then Ben Horowitz's **"The Hard Thing About Hard Things"** . And then Bill Campbell's **"Trillion Dollar Coach"** ——great biography.

And I got myself a **CEO coach**. We meet weekly for like an hour. That's helped me a lot. Especially the first few calls, just helping me have a space to talk about all of the specific problems that I have.

**Koji：** 所以你什么时候找到他的？

**江洋：** An angel.

**Koji：** OK.

**江洋：** And it's actually the same coach for the investor too.

**Koji：** 可以大概介绍一下他是谁吗？

**江洋：** The coach herself——she was an ex-VC executive in large corporations for many years, and she's an expert for first-time CEO coaching.

I never tried getting a therapist before. I never believed in therapy. But a coach is so much better: you can obviously talk about your emotions, but you can also talk about business——everything that's happening in the business. And it's confidential.

Also, it's been really fun to use Paperboy with the coaching calls. Because Paperboy listens to the calls, and it can actually help me follow up on things that I committed to doing on calls and organizing everything.

---

## AI 时代如何组建团队？

**Koji：** 你们怎么看，在今天有那么多的工具、AI、Agent 的情况下，build 一个团队和过去我们做一个产业或产品团队，又有哪些特别大的变化在发生？

**江洋：** If you try to make a serious infra structure build-out, you need **people who understand infra**. I think we hired people on the engineering side:

1. One kind is like Jet——young, high IQ, creative, just prototypes the shit out of every problem that he sees.
1. The second kind is——you got to be real solid with what you do. You got to understand the systems, you got to understand the OS. So we hired this guy who at AWS worked on Windows kernels for the AWS infra for running Windows.
**I don't think that's going to go away anytime soon——the human experts.**

---

## 为什么 Jet 还在读大学？

**Koji：** 其实 Jet 现在大一对吧？我们看到硅谷有一些公司，比如 Palantir，直接给高中生 offer，让他们不要读大学了，直接工作，因为认为在 AI 时代不需要大学了。那很显然 Jet 也是优秀的大一学生，但你也在 Paperboy 做 founding engineer，那你为什么现在还要读大学？

**Jet：** It's got Chinese parents.

利益的话，其实对于大部分人来说，大学能提供非常大的意义。因为至少我在 CMU 这边看来，大部分和我同龄的人其实并不是很确定未来想要做什么事情。在你不确定的情况下，你可以做的是：**提升你自己的 technical ability**。上大学是一个比较好的选项。

- 学业只会占你相对比较少的时间。
- 你大部分其他时间是你自己决定的。
- 相当于四年的时间去 **explore**。这四年的时间对大部分人来说会是比较有用的。
但同时，如果你在上大学的时候已经很确定你想要做什么事情，并且你做事情这方面确实有计划，我觉得辍学也是一个理性的选择。

---

## 年轻的 Founder 如何吸引人才？

**Koji：** 江，你作为一个非常年轻的 founder，也是 first time founder，你怎么样吸引到同学们愿意加入你的？你怎么样说服大家的？

**Jet：** I'll answer that. 江什么方面吸引到我？

你选择加入一个人，职业选择是非常重要的人生投资。很多时候你选一个 founder，你有 intercept，你有 slope。然后很多时候 **slope 比 intercept 重要很多**。我觉得江是一个 **high slope 的 founder**。

怎么说？他现在的 track record——他现在差不多比我大一岁，相当于他是在很小的时间内实现了特别多比较厉害的事情。这一定程度上说明他比较有 **agency**，他可以很快地学习，并且可以做非常多新的事情。对于一个创业者来说，这个 arguably 是最重要的 quality——你要能从无到有，很快地去适应各种情况。

首先你得认为他是一个 good founder。对我来说，我和江已经工作得比较久，所以我和他合作我有比较高的 confidence，我们可以比较顺畅地合作。

江他也有不错的 research、engineering，甚至 product 的 taste。我觉得跟他工作过程中，我可以吸取很多这种经验，让我个人也有更好的成长。我个人觉得江还是比较 charismatic 的一个人。

**Koji：** 我大型表白现场。

**江洋：** Great to see you. Yeah.

### 江洋的招聘方法论

**Koji：** 所以江你自己怎么看？你有没有一些方法被抽象总结出来？比如你现在去 approach 一个新的 candidate，你会有什么样的方法去说服他？

**江洋：** I treat every candidate individually. There's not a script that I stick to. It has to be mutual. I never like to hard-sell the company to a candidate.

Recruiting is one thing, but what's more important is about **my reliability**. That's the thing I actually pay a lot of attention to. It's just like: after I recruit somebody, can I actually deliver what I tell them? Can I carry that and be able to make sure that I deliver on what the team needs, time and time again?

You got to pick people who are great. You can't talk to mediocre people. And you can tell that from the conversations, but also their past work. What's especially important is the **past life decisions**. I really like to learn about——if they're older, they have a decade of decisions behind them. You can really learn a lot——you just can't fake that.

---

## 最喜欢的 AI 产品

**Koji：** 你们可以分享一下最喜欢用的 AI 产品（除了 Paperboy）？

**江洋：** Yeah, still love **Cursor**. I still don't use Codex.

**Jet：** 我特别喜欢 **Codex**.

**江洋：** Cursor has always been a great inspiration to me. I'm really happy for them. I hope whatever acquisition that happens goes through.

### 为什么是 Codex 而不是 Claude Code？

**Koji：** 可不可以讲讲为什么是 Codex 而不是 Claude Code？

**Jet：** Claude Code 理论不一样。它以最 ambitious 的形式体现了未来 software engineer 会怎么工作。但我觉得 Claude Code 最重要的东西是体现 **open source 有多好**，不是说它的命令行有多好。我 appreciate 那个 open source 的模型，我不太 appreciate Claude Code 的 UI 本身。

Codex，我喜欢它几个点：

1. 它核心的 Agent 是 **开源的**。它的命令行和整个 Agent loop 都放在 GitHub 上。
1. 如果你用他们桌面端的 App，和 Claude Code 的桌面端 App 比，它整个 Craft 的水平非常好。
1. 他们前面买了一个团队叫 **Sky**，Sky 是做 Apple Shortcuts 的团队。OpenAI 会用这种人去做一个非常 polished 的产品。你去看 Codex，他们最近出了一个叫 **Codex Pets** 的东西，非常 polished，也很好玩。
1. Codex 的 computer use、browser use 都做得非常 polished。
1. Codex 也是第一个把 **高并行式**（不同 Agent 同时工作）作为主要 UI 的产品，并且 polish 出来了。
1. OpenAI 在 infra 层面比 Anthropic 优势大非常多。所以如果你用 Codex，模型大差不差，但是稳定很多。
Bias：OpenAI 在 infra 上面可以 subsidize 更多的 compute。Anthropic 他们现在投资不够，所以没法 subsidize，导致了一系列风波。比如说你的 repo 里有 Open Cloud 或 Hermes Agent，Claude Code 可能会直接收你 10 倍的价格。Anthropic 现在因为 compute 受限，去做很多奇怪的操作。

### 买股票：OpenAI 还是 Anthropic？

**Koji：** 如果可以买他们的 secondary（股票），你现在会买 OpenAI 还是买 Anthropic？还是你会三、七开？

**Jet：** 我感觉我会买 OpenAI——all in OpenAI。可能 OpenAI 80%，Anthropic 20%。

**Koji：** 什么原因呢？

**Jet：** 他们两个公司都会 do very well，但是我更**喜欢 OpenAI 在做的事情**。

- Anthropic 做得最好的事情是他们的 **interpretability**（可解释性）和 **social impact**。那两个部门做得非常好，我特别喜欢那两个东西。
- 但是 Anthropic 在很多模型上，我觉得他们 **过于 opinionated**——不管是道德上还是具体使用习惯上，他们非常 opinionated。
- 相比之下，OpenAI 的理念是：在最小的局限性之下，用户想要怎么用这个模型就怎么用。我个人比较 libertarian，我会喜欢 OpenAI 这种更加 unopinionated 的 values。
- 还有就是，我觉得 OpenAI 在 compute 上面会占优势。
**江洋：** I'm not going to——if I'm making investment decisions, I'm not going to buy either of them at their current valuation. But I actually **prefer Anthropic**. I think the safety commitment to safety.

---

## 模型吞噬一切？

**Koji：** 你怎么看“模型吞噬一切”这个说法？

**Jet：** 我觉得你完全可以 argue：很多公司会提供差不多的模型，然后产品的差异性还是在产品公司里面。这不一定会是真的，但我觉得这是一个 plausible 的。

**Cursor** 是一个不错的 example。他们一开始是产品公司，但是现在他们既是产品公司又是模型公司——他们现在可以用 **XAI** 的 compute 去做 coding model。所以我觉得，公司不能把自己局限为“模型公司”还是“产品公司”，usually both.

---

## 虚拟投资 300 万美金，投三个团队

**Koji：** 如果给你们一笔虚拟的资金去做投资，比如 300 万美金，可以投三个团队——身边认识的 3 个人。

**江洋：**

- Slack is good.
- Just bet on **Richard**.
- Robotics companies——there's nothing that's definitely going to be big.
- And infra——people who are focused on infra.
- And I believe the biggest company, similar to Cursor, is going to come out of **consumer**. It's not going to come out of enterprise AI. It's going to come out of consumer. And obviously Paperboy is in that market because I follow that belief. Consumer is just such a big market——there's so many opportunities.
**Jet：**

- 我觉得 **Robotics** 我也会特别讲通。因为我觉得在你去 automate knowledge work 的产品之后，很有可能最大的市场是用 model capability 去进化物理世界的这类 opportunity。
- 还有一个就是 **安全**。AI security 是个非常好的领域。这个 demand 基本上是 infinitesimal——只要模型越强，它的 takeoff 和 define 能力都会变强。这个 market 也非常大。
**Koji：** the problem with that is: how do you compete with Anthropic getting into that business?

**Jet：** Anthropic 肯定会有最好的模型。问题是：你有最好的模型之后，你下一个 optimization layer 是什么？

- 你是做比较好的 harness？
- 你是把人类 security researcher 的各种 heuristic bake 到 agent 里面？
- 还是你去做 infra，比如一个非常庞大的 multi-agent system 去不断地挖这些漏洞？
我觉得这个探索空间会非常大。如果你的产品挖的漏洞比另外一个产品多 10%，那么你这个产品就是非常有用的。这是一个非常 **meritocratic** 的市场。所以我觉得很不错。

**江洋：** We haven't talked about **Long Horizon**. Harvey ship the stain, right? Long Horizon law. And then the other John Young ship this new sweep bench recently——reproducing complete code bases from specs. That's not going to go away.

**Jet：** 我觉得安全能力对国家安全是非常非常重要的。但对于创业来说，这也是一个非常好的 opportunity。模型最强的人有 incentive 把这个模型说“只有我们自己国家可以用这个东西”，那么其他国家怎么搞？很多不同的国家或利基都需要这种模型。所以这个 market 非常大。

---

## 一年后的期待

**Koji：** 最后一个问题。你期待一年后的此刻，Paperboy 是一个什么样的状态？你有什么样的期待？或者你有什么害怕做错的事？

**江洋：** Well, hopefully not losing money every day anymore. I want to keep hiring the best people I can find. So the talent density needs to be higher than what we are today.

There are so many specifics we can talk about, but I think from a team and business point of view, it's just that: **we actually need cash flow, and we need to keep building a better team.**

**Koji：** 好，谢谢二位。

**江洋 & Jet：** 谢谢谢谢。非常开心。好。
