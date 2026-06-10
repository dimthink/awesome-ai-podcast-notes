---
title: "[ML 2021 (English version)] Lecture 25: Explainable ML (1/2)"
channel: "李弘毅"
published: "2021-05-13"
source_url: "https://www.youtube.com/watch?v=4rVD1EOaAX4"
video_id: "4rVD1EOaAX4"
rating: 5
language: "中文"
word_count: 50385
duration: "49:44"
---

# [ML 2021 (English version)] Lecture 25: Explainable ML (1/2)

- **Channel:** 李弘毅
- **Published:** 2021-05-13
- **Source:** https://www.youtube.com/watch?v=4rVD1EOaAX4
- **TL;DR:** 可解释机器学习不仅关乎信任与合规，更通过揭示模型“作弊”行为和内部机制，指导模型改进，其目标是提供令人满意的解释。
- **Rating:** 5

## 材料信息

- **标题**：[ML 2021 (English version)] Lecture 25: Explainable ML (1/2)
- **作者/来源**：李弘毅
- **类型**：YouTube 视频字幕
- **关键元数据**：机器学习系列讲座第25讲（共两部分中的第一部分），时长未知。
## 开篇引入

在人工智能日益渗透我们生活的今天，机器学习模型以其强大的预测能力改变了诸多领域。然而，这些模型，尤其是深度学习，往往被视为“黑箱”，其决策过程不透明，令人难以理解和信任。李宏毅教授的这堂精彩讲座，正是为了揭开这个“黑箱”的神秘面纱，深入探讨了“可解释机器学习”（Explainable Machine Learning, XAI）的核心议题。他不仅从哲学层面剖析了我们为何需要解释，更通过生动的案例和前沿的技术，为我们描绘了一幅理解AI决策机制的路线图。这篇深度重构的文章，旨在带领读者超越字幕的字面意义，沉浸于李教授富有洞察力的思考之中，感受XAI的独特魅力与深远影响，从而获得比直接观看视频更为系统和深刻的理解。

## 详细内容

### 可解释机器学习：为何它如此重要？ `[视频开头-05:30]`

**核心观点**

即使机器学习模型能给出正确答案，其“黑箱”特性也使其在信任、法律、伦理和模型改进方面面临严峻挑战，因此，可解释性不再是锦上添花，而是不可或缺的核心需求。

**深度阐述**

我们已经训练了无数的机器学习模型，它们在图像识别等任务上表现出色，能准确地给出答案。然而，仅仅得到一个正确答案，并不能完全满足我们的需求。我们真正渴望的是，机器不仅能给出答案，还能阐明其得出这个答案的“理由”。这正是“可解释机器学习”（Explainable Machine Learning, XAI）的核心所在。李教授开宗明义地指出，XAI之所以成为一个重要议题，其根本原因在于，即使机器今天能给出正确答案，也并不意味着它真正“聪明”或值得完全信任。

他以一个经典的例子——“神马汉斯”（God Horse Hans）的故事——生动地阐释了这一点。汉斯是一匹被誉为能解决数学问题的“神马”，当人们问它“9的平方根是多少”时，它会用马蹄敲击地面，如果答案是3，它就敲三下然后停下来，引来一片欢呼。然而，后来有人对此表示怀疑。经过调查发现，只要没有人看着，汉斯就无法回答数学问题。实际上，汉斯并非真的理解数学，它只是通过观察旁边人类细微的情绪变化，来判断何时停止敲击，从而获得食物奖励。这个故事深刻地揭示了一个道理：表面上的“正确答案”可能掩盖了其背后肤浅甚至错误的决策机制。这不禁引人深思：

重要原话："even if the machine can get the correct answer today it does not mean it must be very smart" `[00:30]`

中文翻译："即使机器今天能得到正确答案，也并不意味着它一定非常聪明。"

李教授进一步将这种担忧投射到当今人工智能的各种应用中。他提出，我们今天所见的AI应用，是否也可能陷入“神马汉斯”的困境？在许多真实世界的应用场景中，可解释性模型已成为强制性要求：

- **金融领域**：银行可能使用机器学习模型来决定是否向客户放贷。然而，法律规定，使用机器学习模型进行自动判断时，必须给出理由。这意味着，我们不能仅仅训练一个能预测的模型，还需要它能够解释其决策。
- **医疗诊断**：机器学习在医疗诊断中的应用关乎生命。如果一个模型只是一个“黑箱”，在没有给出诊断理由的情况下，我们如何能相信它的判断是正确的？
- **法律判决**：一些人希望将机器学习应用于法律领域，例如帮助法官决定是否假释囚犯。但我们如何确保模型是公平的？如何避免种族歧视等潜在问题？我们需要模型不仅提供答案，还能提供公正的理由。
- **自动驾驶**：未来的自动驾驶汽车将遍布街头。如果一辆自动驾驶汽车突然停车，甚至造成乘客受伤，我们必须知道其停车的原因。如果它是因为看到一位老太太过马路而停车，那可能是正确的；但如果它毫无理由地突然“发疯”急停，那模型就存在问题。我们需要了解自动驾驶汽车各种行为和决策背后的原因。
除了信任和合规性，可解释性对于模型本身的改进也至关重要。李教授指出，当前的深度学习技术，往往像是一个“黑箱”操作：

重要原话："someone says that this is your machine learning system yes i just throw the data into it there is a multiplication of many matrices next it will come up with the results if the result is not as expected what to do now everyone knows adjusting the hyperparameters right changing the learning rate right adjusting the architecture of the network right you don't know what you are doing right just adjust the network architecture i just mess this bunch of math this bunch of linear algebra up again and see if the result is better than others who have not done deep learning will be surprised how can this be done but in fact for today's deep learning model to improve the model you need to adjust some hyperparameters but we look forward to the future when the deep learning model makes mistakes we know where the mistakes are we know why it makes mistakes maybe we can have a better way a more efficient way to improve my model" `[04:00]`

中文翻译："有人说，这就是你的机器学习系统？是的，我只是把数据扔进去，然后进行大量的矩阵乘法，接着它就会给出结果。如果结果不符合预期，现在该怎么办？大家都知道调整超参数，对吧？改变学习率，对吧？调整网络架构，对吧？你并不知道自己在做什么，对吧？只是再次调整网络架构，把这些数学、这些线性代数搞乱，看看结果是否会更好。那些没有做过深度学习的人会感到惊讶，这怎么能行？但事实上，对于今天的深度学习模型来说，要改进模型，你需要调整一些超参数。但我们期待未来，当深度学习模型犯错时，我们知道错误在哪里，我们知道它为什么犯错，也许我们就能找到一种更好的、更有效的方法来改进我的模型。"

目前，当深度学习模型表现不佳时，我们通常只能通过调整超参数、学习率或网络架构来“碰运气”。这种试错式的改进方式效率低下，且缺乏理论指导。李教授展望未来，希望可解释机器学习能帮助我们理解模型出错的原因和位置，从而以更高效、更有针对性的方式改进模型。尽管这是一个长远目标，但其潜力巨大。

**精华收获**

可解释机器学习是构建可信赖、合规、公平且可有效改进的AI系统的基石。它帮助我们超越表面准确率，深入理解模型决策的本质，避免“神马汉斯”式的虚假智能。

### 解释性与可解释性：黑箱与路灯下的钥匙 `[05:30-09:30]`

**核心观点**

面对深度学习的“黑箱”特性，我们不应因其难以解释而放弃其强大能力，而应努力寻求方法使其变得可解释。解释性（explainable）和可解释性（interpretable）虽常混用，但前者侧重于为黑箱模型提供解释能力，后者则指模型本身就透明易懂。

**深度阐述**

有些人可能会问，既然深度神经网络是“黑箱”，难以解释，我们为何不直接使用那些本身就更容易解释的机器学习模型呢？例如，线性模型就具有较强的可解释性，通过其特征权重，我们可以清晰地理解模型如何生成结果。然而，线性模型最大的问题在于其能力有限，无法处理复杂的数据模式。为了追求更强大的性能，我们转向了深度模型，但其代价就是可解释性的丧失。

李教授指出，许多人因此得出结论：我们不应该使用深度模型，不应该使用这些更强大的“黑箱”模型。但他认为，这种想法无异于“削足适履”。

重要原话："in my opinion this kind of thinking is actually to cut the feet and fit the shoes do we discard a very powerful model because it is not easy to explain shouldn't we think of ways to make it interpretable" `[06:45]`

中文翻译："在我看来，这种想法实际上是削足适履。我们是否应该仅仅因为一个非常强大的模型不容易解释而将其抛弃？难道我们不应该想办法让它变得可解释吗？"

为了进一步阐明这个观点，李教授引用了Yann LeCun讲过的一个故事：一个醉汉在路灯下找钥匙。当别人问他钥匙是否掉在路灯下时，他说不是，只是因为这里有光。这个故事是一个绝妙的类比：

重要原话："we insist on using simple but easily explainable models it's like we insist on finding the key under the street light we insist on using more interpretable models although it's not good we still insist on using it it's like you must find the key under the street light you will never find a powerful model the powerful model may be outside the scope of the street light what we have to do now is to change the range of street lights can we change the direction of lighting and make these more powerful models to be placed under street lights make the powerful model more interpretable more explainable" `[07:30]`

中文翻译："我们坚持使用简单但易于解释的模型，就像我们坚持在路灯下找钥匙一样。我们坚持使用更容易解释的模型，尽管它可能不够好，我们仍然坚持使用它。这就像你必须在路灯下找钥匙，你永远找不到一个强大的模型。强大的模型可能在路灯的范围之外。我们现在要做的是改变路灯的范围，我们能否改变照明的方向，让这些更强大的模型被置于路灯之下，让强大的模型更具可解释性、更易于解释？"

这个故事告诉我们，仅仅因为某个模型容易解释就坚持使用它，即使它性能不佳，就像只在路灯下找钥匙一样，可能会错过真正强大的解决方案。我们应该做的，不是放弃强大的模型，而是努力“改变路灯的范围”，即开发新的方法，让这些强大的模型变得可解释。

李教授还对“解释性”（explainable）和“可解释性”（interpretable）这两个术语进行了区分，尽管它们在文献中常被交替使用：

- **解释性（Explainable）**：通常指为原本的“黑箱”模型赋予解释能力。模型本身是黑箱，但我们为其提供外部解释机制。
- **可解释性（Interpretable）**：通常指模型本身就不是黑箱，其内部机制是透明且易于理解的。有人已经深入研究过这个模型，我们已经理解了它的内容。
尽管存在细微差别，但李教授表示，在实际讨论中，这两个术语常常混用，因此不必过分强调其区别。重点在于，我们如何让强大的模型变得透明和可理解。

**视觉/结构信息描述**

此处李教授通过口头描述和类比（醉汉找钥匙）来阐释概念，没有直接的视觉图表，但其描述本身就构建了生动的心理图像。

**延伸思考**

这种“削足适履”的思维模式在技术发展中并不少见。当新技术出现时，其复杂性和不透明性常常引发担忧和抵触。然而，历史经验表明，真正的进步往往在于克服这些挑战，而非退回到舒适但受限的旧范式。XAI正是这种克服挑战的努力。

**精华收获**

不应因模型复杂而放弃其强大能力，而应积极探索使其可解释的方法。解释性是为黑箱模型提供解释，可解释性是模型本身透明。Yann LeCun的“路灯下找钥匙”类比深刻揭示了在追求可解释性时可能存在的思维误区。

### 决策树：看似完美的解决方案，实则不然 `[09:30-12:50]`

**核心观点**

决策树模型因其固有的可解释性和相对强大的能力，似乎是可解释机器学习的理想选择。然而，当决策树变得极其复杂或被集成到随机森林等模型中时，其可解释性会迅速丧失，表明它并非解决XAI问题的终极答案。

**深度阐述**

在探讨了“黑箱”模型的困境之后，李教授提出了一个自然而然的问题：既然我们既要强大的模型，又要可解释性，那么决策树（Decision Tree）是不是一个很好的选择呢？

重要原话："Speak of both interpretable and powerful model isn't decision tree a good choice decision tree is a more powerful model compared to linear model another benefit of decision tree is that it is very interpretable it is straightforward when looking at the structure of a decision tree we can know how every branch affects the final decision" `[09:30]`

中文翻译："说到既可解释又强大的模型，决策树不是一个好选择吗？决策树与线性模型相比是一个更强大的模型，决策树的另一个好处是它非常可解释。当我们查看决策树的结构时，我们可以直接知道每个分支如何影响最终决策。"

决策树相较于线性模型，确实更为强大，并且其最大的优点在于其固有的可解释性。通过观察决策树的结构，我们可以清晰地追踪从根节点到叶节点的每一个决策路径，了解每个问题（节点）如何影响最终的判断。例如，每个节点都会提出一个问题，根据答案决定走向左边还是右边，最终到达叶节点做出最终决策。这个过程是完全透明的，我们可以回溯所有问题和答案，从而理解模型做出特定决策的原因以及哪些特征导致了最终结果。从这个角度看，决策树似乎兼具强大和可解释性，堪称完美。

然而，李教授紧接着提出了一个反思：决策树真的是我们所需要的一切吗？

重要原话："well but as a decision tree all we need think about it again decision trees can also be very complicated for example i found someone asked a question on the internet he said he has such a complicated decision tree that he can't understand what the decision tree is doing he asked if anyone has any explainable machine learning methods to simplify this decision tree three or four years have passed and no one answered this question" `[10:40]`

中文翻译："嗯，但决策树就是我们所需要的一切吗？再想想看。决策树也可能非常复杂。例如，我发现有人在网上问了一个问题，他说他有一个如此复杂的决策树，以至于他无法理解这个决策树在做什么。他问是否有人有任何可解释的机器学习方法来简化这个决策树。三四年过去了，没有人回答这个问题。"

他举了一个在网上看到的例子：有人拥有一个极其复杂的决策树，以至于连他自己都无法理解其工作原理，甚至在网上求助是否有方法能简化这个决策树，但多年无人能解。这表明，即使是理论上可解释的决策树，在实际应用中也可能因为其复杂性而变得难以理解。

更重要的是，在实际的机器学习竞赛（如Kaggle）中，学生们常常发现，单一的决策树并非最强大的工具。他们真正使用的技术是“随机森林”（Random Forest）。

重要原话："when you are using decision trees are you using only one decision tree actually not the technique you really use is called random forest right the technique you use in fact is the result of the joint decision of many decision trees with one decision tree you can rely on the question and answer of each node to know how it makes the final judgment but when you have a forest when you have 500 decision trees it's hard for you to know how these 500 decision trees make a judgment together" `[11:40]`

中文翻译："当你使用决策树时，你只使用一个决策树吗？实际上不是。你真正使用的技术叫做随机森林，对吧？你使用的技术实际上是许多决策树共同决策的结果。对于一个决策树，你可以依靠每个节点的问题和答案来了解它是如何做出最终判断的。但是当你拥有一个森林，当你拥有500个决策树时，你很难知道这500个决策树是如何共同做出判断的。"

随机森林是由数百甚至数千个决策树组成的集成模型。虽然单个决策树是可解释的，但当500个决策树共同做出判断时，要理解它们的集体决策过程就变得极其困难。这使得随机森林，尽管其性能强大，但其整体解释性却大大降低，再次陷入了“黑箱”的困境。

因此，李教授总结道，决策树并非终极答案，可解释机器学习的问题并不会因为有了决策树而得到解决。这促使我们必须继续探索更深层次的解释方法。

**视觉/结构信息描述**

此处李教授通过口头描述决策树的工作原理（节点提问、左右分支、叶节点决策）来帮助听众理解其结构，并以随机森林的集成特性来对比其可解释性的丧失。

**延伸思考**

这个例子揭示了“局部可解释性”与“全局可解释性”之间的张力。单个决策树具有局部可解释性，但当它们组合成一个复杂的系统时，全局可解释性就丧失了。这与深度学习中单个神经元或层可能具有某种可解释性，但整个网络的行为难以解释的情况类似。

**精华收获**

决策树虽具可解释性，但其复杂版本或集成模型（如随机森林）会使其可解释性迅速下降。XAI的挑战在于如何解释复杂且强大的模型，而不仅仅是使用简单的模型。

### 解释的目标：模糊的边界与“让所有人满意” `[12:50-18:40]`

**核心观点**

与传统机器学习有明确的性能指标不同，可解释机器学习的“解释目标”是模糊的。李教授认为，一个好的解释并非要揭示模型的全部真相，而是要提供一个能让受众（客户、老板、甚至自己）感到满意和接受的理由。

**深度阐述**

在深入探讨可解释机器学习的技术之前，李教授提出了一个根本性的问题：可解释机器学习的目标到底是什么？在以往的机器学习任务中，我们总有明确的目标，比如降低错误率或提高准确率，并通过排行榜（leaderboard）来衡量进展。但对于“可解释性”而言，什么样的结果才算是“最好的解释”呢？

重要原话："what is the goal of explainable machine learning in each of our previous assignments we all have a leaderboard that means we have a clear goal either lower the error rate or improve accuracy we always have a clear goal but what exactly is the goal of being explainable what result can be considered as the best explanation the goal of explanation is actually very ambiguous" `[13:00]`

中文翻译："可解释机器学习的目标是什么？在我们之前的每个作业中，我们都有一个排行榜，这意味着我们有一个明确的目标，要么降低错误率，要么提高准确率。我们总有一个明确的目标。但可解释性的目标到底是什么？什么样的结果才能被认为是最好的解释？解释的目标实际上非常模糊。"

李教授坦言，解释的目标实际上非常模糊。正因为目标不明确，关于可解释机器学习的作业通常没有明确的排行榜来衡量。这反映出XAI领域的一个核心挑战：解释的“好坏”往往是主观的，而非客观的。

他分享了自己的个人观点，并强调这并非普适真理，但值得深思。许多人对可解释机器学习存在一个误解，认为一个好的解释应该告诉我们模型“完整”地在做什么，我们需要理解模型的一切，完全掌握它是如何做出决策的。然而，李教授反问：这真的有必要吗？

重要原话："many people have a misunderstanding about explainable machine learning they think a good explanation should tell us what the model is doing in its entirety we need to understand everything about the model we need to know what it is we have to fully understand how it makes a decision but think about it is this really necessary" `[14:00]`

中文翻译："许多人对可解释机器学习存在误解，他们认为一个好的解释应该告诉我们模型完整地在做什么。我们需要了解模型的一切，我们需要知道它是什么，我们必须完全理解它是如何做出决策的。但想想看，这真的有必要吗？"

他以人类大脑为例：

重要原话："isn't the human brain also a black box we don't know exactly how the human brain works yet we can trust a decision made by another person the human brain is also a black box and you can trust the human brain to make a decision why when the black box is a deep network you can't trust the decisions made by it why are you so scared of deep networks" `[14:30]`

中文翻译："人类大脑不也是一个黑箱吗？我们并不知道人类大脑具体是如何工作的，但我们却可以信任另一个人做出的决定。人类大脑也是一个黑箱，你可以信任人类大脑做出决定，为什么当黑箱是一个深度网络时，你就不能信任它做出的决定呢？你为什么如此害怕深度网络？"

人类大脑也是一个“黑箱”，我们并不完全了解其内部运作机制，但我们仍然信任他人做出的决定。那么，为什么面对深度网络这个“黑箱”时，我们就如此恐惧和不信任呢？李教授认为，对于人类而言，如果想要感到安心和接受，一个“理由”是非常重要的。

为了支持这个观点，他分享了一个与机器学习无关的心理学实验：

重要原话："The following is a psychology experiment completely unrelated to machine learning this experiment was done in the 1970s by a harvard university professor named ellen langer this experiment is very famous the experiment is like this it is an experiment related to printers the printer in the harvard university library often has a long queue many people are queuing to print at this time if someone tells the person in front of him please let me print first i just need to print five pages would people accept it will they let him print first 60 of people will let this person print first so it feels like the students at harvard are pretty nice this acceptance level is higher than i expected you told someone to let you print first 60 of people will say yes but this time if you change the wording of the question you only said if you could let me print first previously now you say can you let me print first i'm in a rush whether he is really in a rush no one knows but when you have a reason and ask others to let you print first the acceptance rate becomes 94 now in addition even if you slightly change your reason for example some people ask you to let him print first because he has to make copies even with this reason the acceptance rate also becomes 93 it is interesting that people just need a reason why do you want to print first you just have to give a reason even if your reason is that you have to make copies everyone will accept" `[15:00]`

中文翻译："下面是一个与机器学习完全无关的心理学实验。这个实验是哈佛大学教授艾伦·兰格在1970年代做的，这个实验非常有名。实验是这样的，它是一个与打印机相关的实验。哈佛大学图书馆的打印机经常排长队，很多人都在排队打印。这时，如果有人对前面的人说：‘请让我先打印，我只需要打印五页。’人们会接受吗？他们会让他先打印吗？60%的人会让他先打印。所以感觉哈佛的学生都挺好的，这个接受度比我预期的要高。你告诉别人让你先打印，60%的人会说‘是’。但这次如果你改变问题的措辞，你之前只说‘你能不能让我先打印’，现在你说‘你能不能让我先打印，我赶时间’。他是否真的赶时间，没有人知道。但当你有一个理由并要求别人让你先打印时，接受率变成了94%。此外，即使你稍微改变一下你的理由，例如，有些人要求你让他先打印，因为他必须复印。即使有这个理由，接受率也变成了93%。有趣的是，人们只是需要一个理由。你为什么要先打印？你只需要给出一个理由，即使你的理由是‘你必须复印’，大家也会接受。"

这个著名的哈佛大学打印机实验表明，人们仅仅需要一个“理由”就能接受请求，即使这个理由并不充分甚至有些牵强。当请求者说“我赶时间”时，接受率从60%飙升到94%；即使理由是“我需要复印”，接受率也高达93%。这说明，人类在决策时，对“理由”的需求远大于对“理由”真实性的严格审查。

李教授将这个心理学发现与可解释机器学习联系起来：

重要原话："is explainable machine learning the same as it that's why we need explainable machine learning this is my definition of a good explanation if there is an explanation that is acceptable for everyone then it is a good explanation people just need a reason to make themselves happy and who do we want to make happy this person may be your client because hearing that deep network is a black box will make him feel bad but if you tell him that it is explainable and give him a reason he will be happy also he might be your boss the boss may read a lot from content farms and thinks that deep learning is a black box which is not good if you tell him that it is explainable he would also be happy or today you want to convince yourself you think that it is a black box deep network is a black box you can't go over if it can give you a reason of its decision you will be happy so i think a good explanation is an explanation that makes everyone happy that is a good explanation" `[17:00]`

中文翻译："可解释机器学习和它一样吗？这就是我们为什么需要可解释机器学习。这就是我对一个好的解释的定义：如果有一个解释能让所有人接受，那么它就是一个好的解释。人们只是需要一个理由来让自己开心。我们想让谁开心？这个人可能是你的客户，因为听到深度网络是黑箱会让他感觉不好，但如果你告诉他它是可解释的并给他一个理由，他就会开心。他也可能是你的老板，老板可能从内容农场读了很多东西，认为深度学习是黑箱，这不好。如果你告诉他它是可解释的，他也会开心。或者今天你想说服自己，你认为深度网络是黑箱，你无法接受。如果它能给你一个决策的理由，你就会开心。所以我认为一个好的解释是能让所有人开心的解释，那就是一个好的解释。"

他个人对“好的解释”的定义是：如果一个解释能让所有人接受，那么它就是一个好的解释。人们只是需要一个理由来让自己感到满意。这个“所有人”可能包括你的客户（他们听到“黑箱”会不安，但有了理由就会安心）、你的老板（他们可能对深度学习的“黑箱”特性有所顾虑，但有了解释就会满意），甚至是你自己（如果你对深度网络是黑箱感到无法接受，有了理由你也会开心）。

因此，可解释机器学习的目标，在某种程度上，就是提供一个能让相关方感到满意和接受的理由，从而建立信任和共识。

**视觉/结构信息描述**

此处李教授通过口头描述哈佛打印机实验的场景和结果，以及对“黑箱”的心理接受度，来阐释解释的社会和心理功能。

**延伸思考**

这个观点挑战了我们对“解释”的传统认知，即解释必须是完全客观和真实的。在XAI领域，除了追求模型内部机制的“真相”，满足人类的心理需求和建立信任同样重要。这引出了一个伦理问题：如果一个“解释”只是为了“让所有人开心”，即使它不完全反映模型的真实决策过程，是否仍然是“好”的？这需要我们在实用主义和科学严谨性之间找到平衡。

**精华收获**

可解释机器学习的目标是模糊的，其核心在于提供一个能让受众接受和满意的“理由”，而非完全揭示模型的内部真相。哈佛打印机实验表明，人类对“理由”的需求是普遍存在的，这为XAI提供了心理学基础。

### 解释的分类：局部与全局 `[18:40-19:50]`

**核心观点**

可解释机器学习的解释可以分为两大类：局部解释（针对特定输入-输出对）和全局解释（针对模型整体行为）。

**深度阐述**

在明确了可解释机器学习的目标之后，李教授将解释方法划分为两大主要类别：

1. **局部解释（Local Explanation）**
1. **全局解释（Global Explanation）**
**局部解释**关注的是针对**特定输入**的模型决策。

重要原话："Local explanation is like this suppose we have an image classifier we give it a picture and it says that it is a cat then the question we want to ask or the machine has to answer is the reason why this picture is a cat if it answers questions based on a certain picture it is called local explanation" `[19:00]`

中文翻译："局部解释是这样的：假设我们有一个图像分类器，我们给它一张图片，它说这是一只猫。那么我们想问的问题，或者机器必须回答的问题是，为什么这张图片是一只猫？如果它基于某张特定的图片回答问题，这就叫做局部解释。"

例如，当我们给一个图像分类器一张图片，它识别出这是一只猫。局部解释就是要回答“为什么这张特定的图片被认为是猫？”这个问题。它专注于解释模型对单个数据点的预测。

**全局解释**则关注的是模型的**整体行为**或**一般规律**。

重要原话："There is another category which is global explanation global examination is like this without giving any picture to classifier we want to know that for a classify what kind of picture will be classified as a cat we are not using any specific image to analyze we want to know that when we have a model which has a lot of parameters for these parameters what kind of object is called a cat" `[19:20]`

中文翻译："还有另一类是全局解释。全局解释是这样的：在不给分类器任何图片的情况下，我们想知道对于一个分类器来说，什么样的图片会被分类为猫？我们不使用任何特定的图像进行分析。我们想知道，当我们有一个有很多参数的模型时，对于这些参数来说，什么样的对象被称为猫？"

全局解释不依赖于任何特定的输入图片。它试图理解模型作为一个整体，是如何定义“猫”这个概念的，或者说，什么样的图片特征会让模型将其分类为猫。这涉及到理解模型内部的通用模式和规则，而不是针对某一个具体案例。

李教授在本次讲座中主要聚焦于局部解释，并详细介绍了其具体技术。

**视觉/结构信息描述**

此处李教授通过口头描述将解释分为两个类别，并用图像分类的例子来区分两者的侧重点。

**延伸思考**

局部解释和全局解释各有其应用场景和挑战。局部解释对于理解单个决策的公平性、可靠性至关重要，例如在医疗或法律领域。而全局解释则有助于模型开发者理解模型的整体行为，发现潜在的偏差，并指导模型设计和改进。两者是互补的，共同构成了可解释机器学习的完整图景。

**精华收获**

可解释机器学习分为局部解释（针对特定输入）和全局解释（针对模型整体行为），两者在理解模型决策和行为上扮演不同但互补的角色。

### 局部解释技术（一）：组件重要性与灰度遮挡 `[19:50-24:40]`

**核心观点**

局部解释的核心在于识别输入数据中对模型决策影响最大的组件。通过修改或删除这些组件并观察模型输出的变化，可以量化其重要性。灰度遮挡（Gray Square Method）是一种直观的视觉方法，通过遮挡图像不同区域来判断模型关注点。

**深度阐述**

局部解释的核心问题是：为什么模型认为这张图片是一只猫？更具体地说，是这张图片中的哪些“组件”让模型做出了这个判断？是眼睛、耳朵，还是猫的爪子？

李教授将模型的输入（例如图像或文本）视为由多个组件（例如像素或单词）构成。局部解释的目标就是找出这些组件中，哪些对模型的最终决策最为关键。

重要原话："suppose the input of our model is called x this x may be an image or some texts an x can be split into multiple components from x1 to xn for an image each component could be a pixel and for text each component could be a word or a token then the question we want to ask is inside these tokens inside these components it is a token for texts and for an image it may be a pixel inside these components which one is the most important for the machine to make the final decision" `[20:20]`

中文翻译："假设我们模型的输入被称为x，这个x可能是一张图片或一些文本。一个x可以被分成多个组件，从x1到xn。对于一张图片，每个组件可能是一个像素；对于文本，每个组件可能是一个单词或一个标记。那么我们想问的问题是，在这些标记中，在这些组件中（对于文本是标记，对于图片可能是像素），哪一个对机器做出最终决策最重要？"

识别组件重要性的基本原则非常直观：

重要原话："The basic principle is like this we select each of the components and modify them or delete them if we modifying or deleting a component make the output of network change dramatically it shows that this component is critical it is important if a component was deleted the output of network has changed dramatically the phenomenon represents that this component is necessary to the network then this component is an important component" `[20:50]`

中文翻译："基本原则是这样的：我们选择每个组件并修改或删除它们。如果我们修改或删除一个组件，导致网络输出发生剧烈变化，这表明该组件是关键的、重要的。如果一个组件被删除后，网络输出发生了剧烈变化，这种现象表明该组件对网络是必要的，那么这个组件就是一个重要的组件。"

如果修改或删除某个组件，导致模型的输出发生显著变化，那么这个组件就是关键的、重要的。反之，如果变化不大，则说明该组件不那么重要。

李教授首先介绍了一种非常简单直观的方法——**灰度遮挡法（Gray Square Method）**。

重要原话："to be more specific if we want to know the importance of each area in the picture there is a very simple approach to deal with it we input a picture to the network end the network recognized this as a pomeranian next in this picture when we put this gray square in different positions your network will output different results look at this picture these colors represents that the probability of network outputting pomeranian the blue color means the probability of pomeranian is high oh i was wrong blue color means the probability of pomeranian is low red color means the probability of pomeranian is high and every position here represents that we put the gray square there in other words when we moving the gray square to the position of pomeranian's face your image classifier today do not think that the picture is related to pomeranian if you put the gray square around the pomeranian at this time the machine recognize it as a pomeranian so we know that the model do not recognize pomeranian by the ball or the pattern of floor or the pattern of wall so the model recognize pomeranian by the pattern of the dog's face" `[21:15]`

中文翻译："更具体地说，如果我们想知道图片中每个区域的重要性，有一种非常简单的方法来处理。我们将一张图片输入到网络中，网络将其识别为博美犬。接下来，在这张图片中，当我们把这个灰色方块放在不同的位置时，你的网络会输出不同的结果。看这张图片，这些颜色代表网络输出博美犬的概率。蓝色表示博美犬的概率低，红色表示博美犬的概率高。这里的每个位置都代表我们把灰色方块放在那里。换句话说，当我们把灰色方块移动到博美犬的脸部位置时，你的图像分类器今天就不会认为这张图片与博美犬有关。如果你把灰色方块放在博美犬周围，此时机器仍然将其识别为博美犬。所以我们知道，模型不是通过球、地板的图案或墙壁的图案来识别博美犬的，模型是通过狗脸的图案来识别博美犬的。"

**视觉/结构信息描述**

李教授描述了一个视觉实验：

1. **输入图片**：一张包含博美犬的图片，模型将其识别为“博美犬”。
1. **遮挡方块**：一个灰色方块被放置在图片上。
1. **移动方块**：将灰色方块在图片上不同位置移动。
1. **观察输出**：当灰色方块遮挡博美犬的脸部时，模型识别为“博美犬”的概率显著下降（颜色变为蓝色，表示概率低）。当灰色方块遮挡背景（如球、地板、墙壁）时，模型仍然能识别出博美犬（颜色保持红色，表示概率高）。
1. **结论**：这表明模型是通过狗的脸部特征来识别博美犬的，而不是通过背景信息。
他进一步展示了其他例子：

- **轮胎识别**：当灰色方块遮挡轮胎时，模型无法识别轮胎，说明模型确实通过轮胎的图案来识别，而不是随意猜测。
- **阿富汗猎犬识别**：一张图片中有人和一只阿富汗猎犬。当灰色方块遮挡人脸时，模型仍然认为看到了阿富汗猎犬；但当遮挡阿富汗猎犬的特征区域时，模型就无法识别了。这表明模型正确地通过阿富汗猎犬的图案来识别，没有将人的图案误认为是狗。
这种灰度遮挡法提供了一种直观的方式来可视化模型在图像中关注的区域，从而理解其决策的依据。

**个人感受**

李教授在描述这个方法时，语气中透露出对这种直观性的赞赏，以及对模型能够正确识别关键特征的欣慰。

**延伸思考**

灰度遮挡法虽然简单，但其背后蕴含的思想是“因果推断”的初步体现：通过干预（遮挡）输入的一部分，观察对结果的影响。这种方法为后续更复杂的局部解释技术奠定了基础。然而，它的缺点是计算成本较高（需要对每个遮挡位置重新运行模型），且遮挡本身可能会引入非自然的输入，影响模型的判断。

**精华收获**

通过系统地遮挡输入的不同部分并观察模型输出的变化，可以直观地识别出对模型决策至关重要的输入组件。灰度遮挡法是理解模型“看”到什么的有效且易于理解的初步方法。

### 局部解释技术（二）：梯度显著图（Saliency Map） `[24:40-29:50]`

**核心观点**

梯度显著图（Saliency Map）是一种更高级的局部解释技术，通过计算损失函数对输入像素的偏导数来量化每个像素的重要性。偏导数越大，表示该像素对模型决策的影响越大，从而可视化模型关注的关键区域。

**深度阐述**

在介绍了直观的灰度遮挡法之后，李教授引入了一种更高级、更精确的局部解释方法——**梯度显著图（Saliency Map）**。这种方法需要用到微积分中的梯度概念。

重要原话："there is a more advanced method it need to calculate gradient suppose we have a picture we write it as x1 to xn every x here represents a pixel next let's calculate the loss of this picture we use symbol of lowercase e here this symbol of lowercase e is that the distance of ground truth and the prediction of model when we input this picture the distance is related to cross-entropy the bigger the e is the worse the model prediction becomes now okay so now how to know the importance of a certain pixel in the image recognition task then you can input the value of a certain pixel and change the value a lit we add a delta x on the value then we can see how much does our loss value change if you're making a small change on the certain pixel today loss value has a huge change it means that this pixel is important for image recognition task otherwise if delta x is added this delta e approaches zero it means that the pixel in this position is not important for the image recognition task then we can use the ratio of delta e to delta x to represent the importance of pixel xn in fact the meaning of the term delta e divided by delta x is to do partial differentiation of x n on your loss it is ocot if you don't know what partial differentiation is anyway the ratio of delta x to delta e represents the importance of this xn the greater the ratio is the more important xn is" `[24:40]`

中文翻译："有一种更高级的方法，它需要计算梯度。假设我们有一张图片，我们将其写为x1到xn，这里的每个x代表一个像素。接下来，我们计算这张图片的损失，我们在这里使用小写字母e作为符号。这个小写字母e代表真实值与模型预测之间的距离。当我们输入这张图片时，这个距离与交叉熵有关。e越大，模型的预测就越差。好的，那么现在如何知道图像识别任务中某个像素的重要性呢？你可以输入某个像素的值，然后稍微改变这个值，我们在这个值上加上一个delta x。然后我们可以看到我们的损失值会改变多少。如果你今天对某个像素进行微小改变，损失值发生了巨大变化，这意味着这个像素对图像识别任务很重要。否则，如果delta x被添加后，这个delta e趋近于零，这意味着这个位置的像素对图像识别任务不重要。然后我们可以使用delta e与delta x的比率来表示像素xn的重要性。实际上，delta e除以delta x这个术语的含义是对你的损失函数进行关于xn的偏微分。如果你不知道什么是偏微分也没关系。总之，delta x与delta e的比率代表了这个xn的重要性，比率越大，xn就越重要。"

**核心思想**：

1. **定义损失**：首先，我们有一个损失函数（loss function），它衡量模型预测与真实标签之间的差距。损失值e越大，表示模型预测越差。
1. **微小扰动**：我们考虑对输入图片中的某个像素`xn`进行一个微小的改变（`delta x`）。
1. **观察损失变化**：观察这个微小改变如何影响损失值（`delta e`）。
1. **计算比率**：如果`delta x`导致`delta e`发生巨大变化，说明`xn`对损失函数（进而对模型决策）非常重要。这个`delta e`与`delta x`的比率，实际上就是损失函数对像素`xn`的偏导数（partial differentiation）。
1. **量化重要性**：偏导数的绝对值越大，表示该像素对模型决策的重要性越高。
通过对图片中的每个像素都计算这个偏导数，我们就可以得到一张新的图片，这张图片被称为**显著图（Saliency Map）**。在显著图中，颜色越亮（或越红），表示该位置的像素对模型决策越重要。

**视觉/结构信息描述**

李教授展示了显著图的实际应用：

- **水牛图片**：模型被给予一张水牛的图片。显著图显示，模型主要关注水牛的身体部分，而不是草地或竹子。这表明模型通过水牛的形状来识别它。
- **猴子图片**：模型被给予一张猴子在树顶的图片。显著图显示，模型关注的是猴子本身，而不是树叶。这说明模型知道在哪个位置出现什么特征是判断正确答案的关键。
这些例子都表明，显著图能够有效地揭示模型在做出预测时，究竟“看”到了输入图片中的哪些关键区域。

**个人感受**

李教授在讲解显著图时，语气中带着一种对这种技术能够揭示模型内部“思考”过程的兴奋和肯定。他强调了显著图在实际应用中的价值，例如在作业中学生将有机会绘制各种显著图。

**延伸思考**

梯度显著图是XAI领域一个里程碑式的技术，它将模型的内部数学运算与人类可理解的视觉信息联系起来。然而，它也有其局限性，例如，当模型对输入的变化不敏感时（梯度接近于零），显著图可能无法完全捕捉到特征的重要性。此外，梯度可能对噪声敏感，导致显著图不够平滑。

**精华收获**

梯度显著图通过计算损失函数对输入像素的偏导数，量化了每个像素对模型决策的重要性，并以可视化的方式呈现模型在图像中关注的关键区域。它提供了一种比简单遮挡更精确、更具数学基础的局部解释方法。

### 案例研究：宝可梦 vs. 数码宝贝——黑箱的欺骗性 `[29:50-37:00]`

**核心观点**

通过一个宝可梦与数码宝贝分类器的案例，李教授生动地展示了即使模型达到极高准确率，也可能基于错误的、虚假的关联进行决策，而非真正理解对象特征。可解释机器学习在此类场景中扮演着揭示模型“作弊”行为的关键角色。

**深度阐述**

为了进一步强调可解释机器学习的重要性，李教授分享了一个他亲自进行的、令人震惊的案例研究：宝可梦（Pokemon）与数码宝贝（Digimon）的分类。

**实验背景**：

李教授在网上发现了一个声称能以极高准确率分类宝可梦和数码宝贝的分类器。他决定自己动手复现并探究其背后的原理。他收集了大量的宝可梦和数码宝贝图片，并训练了一个简单的深度学习模型。

**人类识别的困难**：

在展示图片时，李教授首先让听众尝试区分宝可梦和数码宝贝。结果显示，即使是人类，也很难准确区分两者，因为它们在视觉上往往非常相似。

重要原话："honestly i don't know the answer either as you can see pokemon and digimon are hard to distinguish it is even hard for human beings like you to determine whether the picture is a pokemon or a digimon" `[32:00]`

中文翻译："老实说，我也不知道答案。正如你所看到的，宝可梦和数码宝贝很难区分，即使像你这样的人也很难判断图片是宝可梦还是数码宝贝。"

**模型惊人的准确率**：

然而，当他训练了一个只有几层的简单模型后，结果令人难以置信：

- **训练准确率**：98.9%
- **测试准确率**：98.4%
重要原话："the correct rate is 98.4 this is incredible all hail the powerful machine learning humans can't identify the difference between pokemon and digimon but the machine can with 98.4 correct rate" `[33:00]`

中文翻译："正确率是98.4%，这太不可思议了！强大的机器学习万岁！人类无法区分宝可梦和数码宝贝，但机器可以，正确率高达98.4%。"

如此高的准确率让人惊叹，机器似乎真的找到了人类无法察觉的区分特征。

**显著图揭示的真相**：

好奇心驱使下，李教授使用显著图来探究模型做出判断的依据。结果却令人大跌眼镜：

**视觉/结构信息描述**

李教授展示了数码宝贝和宝可梦图片的显著图：

- **数码宝贝显著图**：显著的亮点（重要区域）奇怪地分布在图片的四个角落。
- **宝可梦显著图**：更明显的是，模型关注的特征几乎完全远离宝可梦的身体，而是集中在图片的背景区域。
重要原话："you find that the features which machine cares about are basically away from the pokemon's body it's all on the background of the image why is it because the images of pokemon are all png files and the images of digimon are all jpeg files after the png file is read in the background will be all black so the machine only needs to look at the background to know if a picture is a pokemon or a digimon it's solved like this great" `[35:00]`

中文翻译："你会发现机器关注的特征基本上都远离宝可梦的身体，全部都在图像的背景上。为什么会这样？因为宝可梦的图片都是PNG文件，而数码宝贝的图片都是JPEG文件。PNG文件读取后，背景会全部是黑色。所以机器只需要看背景就能知道一张图片是宝可梦还是数码宝贝。它就是这样解决的，太棒了！"

原来，模型并非通过学习宝可梦和数码宝贝的视觉特征来区分它们，而是利用了一个**虚假的关联**：宝可梦的图片都是PNG格式，读取后背景是黑色；而数码宝贝的图片都是JPEG格式。模型仅仅通过识别图片背景的颜色（黑色或非黑色）就能达到高准确率。它根本没有“看”到图片中的生物是什么，而是“作弊”了！

**案例的启示**：

这个例子深刻地说明了可解释机器学习的极端重要性。一个看似表现优异的模型，其内部决策逻辑可能完全是错误的，甚至具有误导性。如果没有XAI，我们可能会盲目信任一个基于虚假关联做出决策的模型，并将其部署到实际应用中，带来不可预测的风险。

重要原话："so this example tells us that explainable ai is a very important technology you may feel a little bit ridiculous about the example i just gave to you maybe it won't happen in regular applications but will it really not happen" `[36:00]`

中文翻译："所以这个例子告诉我们，可解释AI是一项非常重要的技术。你可能会觉得我刚才给你的例子有点荒谬，也许它不会发生在常规应用中。但它真的不会发生吗？"

李教授强调，虽然这个例子听起来有些荒谬，但类似的“作弊”行为在真实世界中并不少见。

**个人感受**

李教授在揭示这个真相时，语气中带着一丝幽默和讽刺，但更多的是对这种现象的警示。他通过这个生动的案例，让听众深刻体会到XAI的价值，远不止于“让老板开心”，更是为了确保模型的鲁棒性和可靠性。

**延伸思考**

这个案例是数据偏见（data bias）和模型过拟合（overfitting）的典型体现。模型没有学习到泛化能力强的特征，而是学习了训练数据中存在的偶然性、非本质的关联。XAI不仅能揭示这种问题，还能帮助我们改进数据收集和模型训练策略，以避免此类“作弊”行为。

**精华收获**

高准确率并不意味着模型真正理解了任务。模型可能通过学习数据中的虚假关联（如文件格式导致的背景颜色差异）来“作弊”。可解释机器学习是揭示这些隐藏问题的关键工具，确保模型决策的可靠性和泛化能力。

### 真实世界的陷阱：Pascal VOC 2007数据集的马匹案例 `[37:00-38:20]`

**核心观点**

即使是广泛使用的基准数据集，也可能存在模型可以利用的虚假关联。一个在Pascal VOC 2007数据集上识别马匹的模型，被显著图揭示出它并非通过马匹特征，而是通过图片左下角的特定英文水印进行识别，再次印证了XAI在发现模型“作弊”行为上的关键作用。

**深度阐述**

为了进一步证明“宝可梦 vs. 数码宝贝”案例并非孤例，李教授提供了一个来自真实世界、更具说服力的例子，它发生在著名的基准数据集——**Pascal VOC 2007**上。

重要原话："There is a real example there is a benchmark corpus called pascal voc 2007. there are all kinds of objects inside machine needs to learn to classify images when the machine sees this picture it knows it's a picture of a horse but if you draw saliency map you will realize the result like this it only cares about the lower left corner of the horse why because that there is a string of english in the lower left corner pictures of horses in this gallery are from a certain website and the lower left corner of them all have the same string of english so when the machine sees this string of english in the lower left corner it will know it is a horse it doesn't have to learn what a horse looks like so in this real application today on benchmark corpus a similar situation will occur" `[37:00]`

中文翻译："有一个真实的例子，有一个基准语料库叫做Pascal VOC 2007。里面有各种各样的物体，机器需要学习分类图像。当机器看到这张图片时，它知道这是一张马的图片。但如果你绘制显著图，你会发现结果是这样的：它只关心马的左下角。为什么？因为左下角有一串英文。这个图库中的马匹图片都来自某个网站，它们的左下角都有相同的英文串。所以当机器看到左下角的这串英文时，它就会知道这是一匹马。它不必学习马长什么样。所以在今天的基准语料库的真实应用中，也会出现类似的情况。"

**案例描述**：

在这个数据集中，模型被训练来识别各种物体，包括马匹。当模型看到一张马的图片时，它能正确地识别出这是一匹马。然而，当研究人员绘制显著图时，他们发现了一个惊人的结果：模型几乎只关注图片左下角的一个区域，而不是马的身体特征。

**原因揭示**：

进一步调查发现，这个数据集中的所有马匹图片都来自同一个网站，并且这些图片在左下角都带有一串相同的英文水印。因此，模型并没有真正学习“马”的视觉特征，而是学会了识别这个特定的英文水印。只要看到这个水印，模型就判断这是一匹马，而无需理解马的形态。

**启示**：

这个例子比宝可梦案例更具冲击力，因为它发生在一个被广泛接受和使用的基准数据集上。它表明，即使是精心策划的数据集，也可能存在模型可以利用的“捷径”或虚假关联。如果没有可解释机器学习，这些隐藏的问题可能永远不会被发现，导致模型在真实世界中遇到没有这些水印的马匹图片时，表现会一落千丈。这再次强调了XAI在验证模型鲁棒性和泛化能力方面的不可替代性。

**视觉/结构信息描述**

李教授口头描述了马匹图片的显著图结果，强调了模型关注点集中在左下角英文水印的现象。

**延伸思考**

这个案例对数据集的质量提出了警示。在构建数据集时，我们不仅要关注标签的准确性，还要警惕数据中可能存在的非本质性、但模型容易利用的模式。XAI可以作为一种强大的诊断工具，帮助我们发现和纠正这些数据问题。

**精华收获**

即使在标准基准数据集上，模型也可能通过学习与任务无关的虚假关联（如图片水印）来“作弊”。XAI是揭示这些隐藏偏见和确保模型真正学习到有意义特征的关键工具。

### 改进显著图：SmoothGrad与“让老板开心” `[38:20-41:50]`

**核心观点**

原始的梯度显著图可能存在噪声。SmoothGrad通过对输入图片添加噪声并平均其显著图，可以生成更平滑、更清晰的显著图。然而，李教授质疑这种改进是否真的反映了模型更深层的理解，抑或只是为了“让人们感觉良好”。

**深度阐述**

在介绍了梯度显著图的原理和应用后，李教授指出，原始的显著图有时会显得比较嘈杂，不够清晰。为了解决这个问题，他提到了一个改进方法——**SmoothGrad**。

重要原话："is there any method to draw saliency map for explainable machine learning better the first method is the smooth grad just mentioned by the tas what does it mean this picture refers to a gazelle then you expect that when you are doing saliency map the machine will focus on the gazelle if you use the method we just mentioned to draw the saliency map directly the result you get may look like this indeed there are many bright spots near the gazelle but there are also some noises in other places to make people look a little uncomfortable so there is the smooth grad method smooth grad will make your saliency map with few noises if on this example you will find out that most of the bright spots concentrate on the gazelle" `[38:20]`

中文翻译："有没有更好的方法来绘制可解释机器学习的显著图？第一个方法就是助教刚才提到的SmoothGrad。这是什么意思呢？这张图片指的是一只瞪羚。那么你期望在绘制显著图时，机器会聚焦在瞪羚上。如果你直接使用我们刚才提到的方法绘制显著图，你得到的结果可能看起来像这样：确实在瞪羚附近有很多亮点，但在其他地方也有一些噪声，让人看起来有点不舒服。所以就有了SmoothGrad方法。SmoothGrad会使你的显著图噪声较少。如果在这个例子上，你会发现大部分亮点都集中在瞪羚上。"

**SmoothGrad的工作原理**：

SmoothGrad的原理非常简单：

重要原话："How does the smooth grad method work it's very simple to put it bluntly it's worthless it's that on your picture you add various noises pictures with different noises mean different pictures on each picture we calculate the saliency map then if you have 100 kinds of noises to add there will be 100 saliency maps by averaging them you can get the result of smooth grad that's it" `[39:40]`

中文翻译："SmoothGrad方法是如何工作的？说白了很简单，它就是：在你的图片上添加各种噪声。带有不同噪声的图片意味着不同的图片。在每张图片上，我们都计算显著图。然后，如果你添加了100种噪声，就会有100张显著图。通过对它们进行平均，你就可以得到SmoothGrad的结果，就是这样。"

简而言之，SmoothGrad通过以下步骤生成显著图：

1. 对原始输入图片添加多种不同的随机噪声，生成多个噪声版本的图片。
1. 对每个噪声版本的图片，分别计算其显著图。
1. 将所有这些显著图进行平均，得到最终的SmoothGrad显著图。
通过这种平均操作，可以有效地减少显著图中的噪声，使重要的区域更加突出和清晰。

**李教授的质疑**：

然而，李教授对SmoothGrad的深层意义提出了一个尖锐的质疑：

重要原话："of course someone might ask that how you know this smooth grad must give better result than the original one maybe for the machine it really thinks these grasses are very important it really thinks this sky is very important it really thinks this background is very important maybe it's like what i said at the beginning the most important goal of explainable machine learning is just to make people feel good when you draw this picture your boss will feel unpleasant he will feel that this model is a little bit suck this model seems to be hard to explain so you will draw it as smooth grad like this and then tell others that please look at this model it really knows the gazelle is the most important so this model is good and this explainable machine learning method is also good good" `[40:00]`

中文翻译："当然，有人可能会问，你怎么知道这个SmoothGrad一定比原始方法给出更好的结果？也许对于机器来说，它真的认为这些草很重要，它真的认为天空很重要，它真的认为背景很重要。也许就像我一开始说的，可解释机器学习最重要的目标只是为了让人们感觉良好。当你画出这张图片时，你的老板会感到不快，他会觉得这个模型有点糟糕，这个模型似乎很难解释。所以你会像这样画出SmoothGrad，然后告诉别人：‘请看这个模型，它真的知道瞪羚是最重要的，所以这个模型很好，这个可解释机器学习方法也很好。’"

他质疑SmoothGrad是否真的揭示了模型更“真实”的理解，还是仅仅通过平滑处理，使得显著图看起来更符合人类的直觉和期望，从而“让人们感觉良好”。如果原始的显著图显示模型关注了背景噪声，这可能确实是模型内部的真实情况。而SmoothGrad通过平均消除了这些噪声，虽然视觉上更美观，但可能掩盖了模型潜在的缺陷。这再次呼应了他之前提出的“解释的目标是让所有人满意”的观点。

**视觉/结构信息描述**

李教授描述了原始显著图可能出现的噪声（瞪羚图片中，除了瞪羚还有其他地方的亮点），以及SmoothGrad处理后显著图的改善（亮点更集中在瞪羚上）。

**延伸思考**

这个质疑触及了XAI的一个核心哲学问题：我们是追求模型“真实”的内部运作机制，即使它可能混乱且不直观；还是追求一个“令人满意”的解释，即使它可能经过了某种程度的“美化”？在实际应用中，两者之间往往需要权衡。一个过于嘈杂的解释可能无法被非专业人士理解和接受，而一个过于简化的解释又可能掩盖模型的真实问题。

**精华收获**

SmoothGrad通过对加噪输入求平均显著图来减少噪声，使显著图更清晰。然而，这种“美化”可能只是为了满足人类的直观感受，而非真正揭示模型更深层的理解，引发了对XAI目标是“真实”还是“满意”的哲学思考。

### 梯度的局限性：大象鼻子与饱和效应 `[41:50-45:00]`

**核心观点**

仅凭梯度（偏导数）来衡量特征重要性存在局限性。当特征对模型输出的影响达到饱和时，即使该特征仍然重要，其梯度也可能趋近于零，导致显著图无法准确反映其真实重要性。

**深度阐述**

尽管梯度显著图是一种强大的局部解释工具，但李教授紧接着指出了其固有的局限性。他通过一个生动的例子来阐释：

重要原话："but actually by just looking at gradient it could not fully reflect the importance of a component how should i say here is an example for your reference ok this horizontal axis represents the length of the nose of elephant or a certain creature the vertical axis represents the probability that this creature is an elephant we all know the characteristic of elephants is long nose so for a creature the longer its nose the more likely it is an elephant but when its nose is long enough to a limitation making it even longer won't make it more like an elephant elephant with long nose is just an elephant with a very long nose so when an elephant's nose gets longer beyond a certain range you won't think it becomes more like an elephant so the length of a creature's nose is irrelevant to the possibility that it is an elephant its relevance may be at first when the length is relatively short as the length gets longer there is a growing possibility that this creature is an elephant but when the length of the nose reaches a certain level even longer nose won't make it more like an elephant at this time if you calculate the length of the nose and do the partial differential of the probability of an elephant the partial differential you get in this place might approximate to zero so if you only look at gradient and only look at the saliency map you may come to a conclusion that the length of the nose has nothing to do with whether it's an elephant or not the length of the nose is not an indicator of whether it is an elephant because the change in the length of the nose with respect to changes in the possibility of being an elephant is close to zero so the nose is not an important indicator for judging whether it is an elephant at all is it reasonable actually you know it's not like this" `[42:00]`

中文翻译："但实际上，仅仅通过观察梯度并不能完全反映一个组件的重要性。我该怎么说呢？这里有一个例子供你参考。好的，这个横轴代表大象或某种生物的鼻子长度，纵轴代表这种生物是大象的概率。我们都知道大象的特征是长鼻子，所以对于一种生物来说，鼻子越长，它就越有可能是一头大象。但是当它的鼻子长到一定限度时，即使再长也不会让它更像一头大象。长鼻子的大象只是一头鼻子很长的大象。所以当大象的鼻子长到超过一定范围时，你不会认为它变得更像一头大象。所以生物鼻子长度与它是否是大象的可能性无关。它的相关性可能最初在长度相对较短时，随着长度的增加，这种生物是大象的可能性越来越大。但是当鼻子长度达到一定水平时，即使鼻子更长也不会让它更像一头大象。此时，如果你计算鼻子长度并对大象的概率进行偏微分，你在这个地方得到的偏微分可能接近于零。所以如果你只看梯度，只看显著图，你可能会得出结论，鼻子长度与它是否是大象无关。鼻子长度不是判断它是否是大象的指标，因为鼻子长度的变化对成为大象的可能性变化接近于零。所以鼻子根本不是判断它是否是大象的重要指标。这合理吗？实际上，你知道并非如此。"

**大象鼻子例子**：

1. **横轴**：生物的鼻子长度。
1. **纵轴**：该生物是“大象”的概率。
1. **曲线趋势**：当鼻子长度较短时，随着长度增加，是“大象”的概率会迅速上升。然而，当鼻子长度达到一定程度（例如，已经足够长到明确是大象的鼻子）时，即使鼻子再长，它仍然是一头大象，是“大象”的概率不会再显著增加，甚至可能趋于平稳。
**梯度的局限**：

在这种情况下，如果我们在鼻子长度已经很长、概率曲线趋于平稳的区域计算“大象概率”对“鼻子长度”的偏导数，这个偏导数将接近于零。

如果仅仅依赖这个接近于零的梯度值，我们可能会错误地得出结论：鼻子长度与是否是大象无关，或者鼻子长度不是判断大象的重要指标。但这显然是不合理的，因为我们都知道长鼻子是大象的标志性特征。

**原因分析**：

这个现象被称为**饱和效应（saturation effect）**。当某个特征对模型输出的影响达到饱和状态时，即使该特征本身非常重要，其微小变化对输出的影响（即梯度）也会变得很小。梯度只能反映局部线性变化，而无法捕捉特征的整体重要性，尤其是在非线性模型中。

**解决方案**：

为了解决梯度显著图的这个局限性，李教授提到了一个更先进的方法——**集成梯度（Integrated Gradients, IG）**。

重要原话："hence there are other ways there is a method called integrated gradient its abbreviation is called ig here i'm not going to elaborate on how ig works we just leave the file here there is also an ig implemented in the teaching assistance program then if you are interested you can study by yourself to see how ig works if you are not interested then you press enter and you get the result of the ig analysis" `[44:30]`

中文翻译："因此还有其他方法，有一种方法叫做集成梯度，它的缩写是IG。在这里我不会详细阐述IG是如何工作的，我们只是把文件留在这里。助教程序中也实现了IG。如果你感兴趣，你可以自己学习IG是如何工作的。如果你不感兴趣，那么你按下回车键，你就会得到IG分析的结果。"

集成梯度通过沿着从基线（baseline）到实际输入的路径上累积梯度，来解决饱和问题，从而更准确地反映特征的整体重要性。虽然李教授没有详细讲解IG的工作原理，但他强调了它的存在和重要性。

**视觉/结构信息描述**

李教授通过口头描述了一个二维图表，横轴为“鼻子长度”，纵轴为“是大象的概率”，并描述了曲线的形状（先上升后平稳），以此来解释梯度在饱和区域趋近于零的现象。

**延伸思考**

梯度的局限性提醒我们，任何一种解释方法都有其适用范围和盲点。在选择XAI技术时，我们需要理解其背后的数学原理和假设，并根据具体问题和模型特性进行选择。集成梯度等方法正是为了克服这些局限而诞生的。

**精华收获**

梯度显著图在特征对模型输出影响饱和时会失效，无法准确反映特征的重要性。集成梯度等更高级方法旨在克服这一局限，提供更全面的特征重要性评估。

### 深入网络内部：可视化神经元输出与注意力机制 `[45:00-53:00]`

**核心观点**

除了分析输入组件的重要性，我们还可以通过可视化网络中间层的神经元输出和注意力机制来理解模型如何处理输入并得出最终答案。

**深度阐述**

在探讨了局部解释中关于输入组件重要性的方法后，李教授将目光转向了更深层次的问题：当我们将一个输入（例如声音信号）提供给网络时，网络是如何处理这个输入并最终得出答案的？这需要我们深入到网络的内部机制。

**1. 可视化神经元输出**

最直观的方法是“亲眼”观察网络内部发生了什么。

重要原话："ok there are different ways the first method is most intuitive you see what happened in network with your own eyes in the homework i want you to see what happened in bert that is related to text for the example given in class let's take the voice for example in homework 2 you have trained a network this network is just inputting a short piece of sound and judging that this voice is belong to which phoneme and which kk phonetic and then suppose your first layer has 100 neurons the second layer also has 100 neurons the output of the first layer can be seen as a 100-dimensional vector the output of the second layer can also be seen as a 100-dimensional vector by analyzing these vectors maybe we can know that what happened in a network but a 100-dimensional vector is not easy to read not easy to observe and not easy to analyze so what to do you have many ways you can take a 100 dimensional vector and reduce it to two dimensions then what is the method we won't go into details here in short there is a basket of methods that can be used after reducing the 100 dimension to two dimensions you can draw on the picture then you can observe it carefully see what you can observe" `[45:30]`

中文翻译："好的，有不同的方法。第一种方法最直观，你可以亲眼看到网络中发生了什么。在作业中，我希望你们能看到BERT中与文本相关的事情。对于课堂上给出的例子，我们以语音为例。在作业2中，你们训练了一个网络，这个网络只是输入一小段声音，然后判断这个声音属于哪个音素和哪个KK音标。然后假设你的第一层有100个神经元，第二层也有100个神经元。第一层的输出可以看作是一个100维向量，第二层的输出也可以看作是一个100维向量。通过分析这些向量，也许我们能知道网络中发生了什么。但是一个100维向量不容易阅读，不容易观察，也不容易分析。那么该怎么办呢？你有很多方法。你可以把一个100维向量降维到两维。那么具体方法我们在这里就不详细介绍了，总之有很多方法可以使用。将100维降维到两维后，你可以在图上绘制出来，然后仔细观察，看看你能观察到什么。"

**方法**：

- **提取中间层输出**：获取网络中间层（例如，某个隐藏层）的神经元激活值。这些激活值通常是高维向量（例如100维）。
- **降维可视化**：由于高维向量难以直接观察和分析，需要使用降维技术（如t-SNE、PCA等，李教授在此处未详细展开具体方法）将其降到2维。
- **绘制散点图**：将降维后的2维数据点绘制在图上，每个点代表一个输入样本在中间层的表示。通过观察这些点的分布和聚类情况，可以推断网络学到了什么。
**语音识别案例**：

李教授以语音识别为例，展示了这种可视化方法的强大之处。这个例子来自一篇2012年的论文，其数据与学生作业2中使用的数据完全相同。

重要原话："what we are doing here is we get the input of the model first which is the acoustic feature which is mfcc then we reduce it to two dimensions and draw on a two-dimensional plane on this picture each point represents a small sound signal every color represents a speaker someone who speaks in fact the information we threw to this network has many sentences repeated someone said i said how are you b also said how are you c also said how are you many people said the same sentence but you can't tell from this picture from the acoustic feature we can see that the same sentence with the same content spoken by different people cannot be told apart sentences spoken by the same person were more similar to each other even if it's the same sentence as long as it's spoken by different people the results won't be aligned so judging from this result people will think that voice recognition is too difficult to be done since the features of the same sentence spoken by different people looks very different from one another how is the task of voice recognition possible to be done" `[48:00]`

中文翻译："我们在这里做的是，首先获取模型的输入，即声学特征，也就是MFCC。然后我们将其降维到两维，并绘制在二维平面上。在这张图片上，每个点代表一个小的声音信号，每种颜色代表一个说话者。事实上，我们输入到这个网络的信息中有很多重复的句子，有人说‘你好吗’，B也说‘你好吗’，C也说‘你好吗’，很多人都说了相同的句子。但是你无法从这张图片中看出，从声学特征来看，不同人说的内容相同的句子无法区分开来。同一个人说的句子彼此更相似。即使是相同的句子，只要是不同人说的，结果就不会对齐。所以从这个结果来看，人们会认为语音识别太难了，因为不同人说的相同句子的特征看起来彼此非常不同，语音识别任务怎么可能完成呢？"

**视觉/结构信息描述**

- **MFCC特征（输入层）可视化**：在二维平面上，每个点代表一个小的声音信号，不同颜色代表不同的说话者。
- **网络第八层输出可视化**：
**2. 分析注意力机制（Attention Layer）**

李教授还提到了分析注意力机制作为理解网络内部学习内容的方法。自注意力（Self-attention）在现代深度学习模型中广泛应用。

重要原话："we can also analyze the attention layer self-attention is widely used nowadays and we can also see what the network actually learned by looking at the result of the attention in the homework we also asked you guys to take a look at bert's attention" `[51:30]`

中文翻译："我们也可以分析注意力层。自注意力现在被广泛使用，我们也可以通过查看注意力的结果来了解网络实际学到了什么。在作业中，我们也要求你们看看BERT的注意力。"

通过观察注意力权重，我们可以了解模型在处理序列数据（如文本）时，哪些部分与哪些部分建立了关联。直观上，注意力机制应该具有很强的解释性，例如显示单词之间的相关性。

**注意力机制的争议**：

然而，李教授也指出，关于注意力机制是否真正具有解释性，目前学术界仍存在争议。

重要原话："However we can actually find papers like this one attention is not explanation attention isn't always explainable of course some people have published papers like this one attention is not not explanation so we can see that this field of research is progressing very fast soon maybe someone will publish a paper claiming attention is not not not explanation so the questions of whether attention is explainable or not when is it explainable or when is it not explainable are still problems that require further research" `[52:00]`

中文翻译："然而，我们实际上可以找到这样的论文：‘注意力不是解释’，‘注意力并非总是可解释的’。当然，也有人发表了这样的论文：‘注意力并非不是解释’。所以我们可以看到这个研究领域进展非常快，很快可能有人会发表论文声称‘注意力并非并非不是解释’。所以关于注意力是否可解释，何时可解释，何时不可解释的问题，仍然是需要进一步研究的问题。"

一些论文认为“注意力不是解释”，因为它可能只是模型内部的一种计算机制，不一定直接对应人类可理解的语义关联。而另一些论文则反驳说“注意力并非不是解释”。这表明注意力机制的解释性是一个复杂且仍在活跃研究中的领域。

**个人感受**

李教授在讲解语音识别案例时，流露出对深度学习模型能够从混乱的原始数据中提取出本质信息的惊叹。他用“时代变了”来感叹深度学习的进步，并鼓励学生们通过作业亲身体验这种变化。在讨论注意力机制时，他以幽默的方式描述了学术界关于其解释性的争论，展现了科学研究的动态性和不确定性。

**延伸思考**

可视化中间层输出和注意力机制是理解模型“如何思考”的重要途径。它们帮助我们从宏观（聚类）和微观（关联）两个层面洞察模型的学习过程。然而，这些方法也并非完美，高维数据的降维可能丢失信息，注意力权重也可能存在多种解释。

**精华收获**

通过降维可视化网络中间层神经元输出，可以观察模型如何对输入进行抽象和特征提取（如语音识别中消除说话者特征）。分析注意力机制有助于理解输入元素间的关联，但其解释性仍是活跃研究领域。

### 深入网络内部：探测（Probing）模型 `[53:00-1:05:00]`

**核心观点**

探测（Probing）是一种通过训练一个小型辅助分类器（探针）来推断网络内部表示中编码了哪些特定信息的技术。它能更系统地揭示模型各层学习到的语义或句法特征，但需要警惕探针本身的训练质量。

**深度阐述**

除了直接观察神经元输出和注意力机制，李教授介绍了另一种更系统、更量化的方法来理解网络内部发生了什么——**探测（Probing）**。

重要原话："In addition to observing with human eyes there is another technology called probing probing means using probes to probe into the network and see what happens for example suppose now we want to know what a certain layer of bert has learned observing with the naked eye has its limits there may be many phenomena that we didn't observe besides there is no way for us to look through a large amount of data at once so what should we do we can train a probe the probe is actually a classifier" `[53:00]`

中文翻译："除了用肉眼观察，还有一种技术叫做探测。探测意味着使用探针深入网络，看看发生了什么。例如，假设现在我们想知道BERT的某个层学到了什么。肉眼观察有其局限性，可能有很多我们没有观察到的现象，此外，我们无法一次性查看大量数据。那么我们该怎么办呢？我们可以训练一个探针。探针实际上是一个分类器。"

**探测的工作原理**：

探测的核心思想是训练一个“探针”（probe），这个探针通常是一个简单的分类器。

1. **提取内部表示**：从目标网络（例如BERT）的某个特定层提取其输出的嵌入（embedding），这些嵌入是该层对输入数据的内部表示。
1. **训练探针**：将这些嵌入作为输入，训练一个小型分类器（探针）来预测某种我们感兴趣的属性（例如，词性标注、命名实体识别等）。
1. **评估探针性能**：如果这个探针分类器能够以高准确率预测该属性，就说明目标网络的该层嵌入中包含了丰富的关于该属性的信息。反之，如果准确率很低，则说明该层嵌入中不包含或很少包含该属性的信息。
**探测的例子**：

- **词性标注（POS Tagging）**：
重要原话："for example we train a classifier that decides the pos tag of a phrase which is its part of speech according to a feature which is a vector we pass the embedding of bert to the pos classifier to train the pos classifier it will try to use these embeddings to decide the parts of speech of the embeddings if the pos classifier has a high accuracy it means that there's a lot of information regarding the parts of speech of the embeddings if the pos classifier has a low accuracy it means that there isn't much information regarding the parts of speech of the embeddings" `[54:00]`

中文翻译："例如，我们训练一个分类器，根据一个特征（一个向量）来决定一个短语的词性标签，也就是它的词性。我们将BERT的嵌入传递给词性分类器来训练它。它会尝试使用这些嵌入来决定嵌入的词性。如果词性分类器具有高准确率，这意味着嵌入中包含大量关于词性标签的信息。如果词性分类器具有低准确率，这意味着嵌入中没有太多关于词性标签的信息。"

通过训练一个词性分类器作为探针，我们可以判断BERT的某个层是否学习到了词性信息。

- **命名实体识别（NER）**：
重要原话："or utrain aner classifier which stands for name entity recognition then it determines whether the vocabulary it sees now is a name for a person a name for a place or not a proper noun at all through the accuracy of the ner classifier we can know whether these features contain names addresses or any information about the person's name etc" `[54:40]`

中文翻译："或者你训练一个NER分类器，它代表命名实体识别，然后它判断它现在看到的词汇是人名、地名还是根本不是专有名词。通过NER分类器的准确率，我们可以知道这些特征是否包含姓名、地址或任何关于人名的信息等。"

类似地，训练一个NER分类器可以揭示网络层是否编码了命名实体信息。

**使用探测技术的注意事项**：

李教授强调，在使用探测技术时，有一个非常重要的注意事项：要**警惕探针分类器本身的强度**。

重要原话："however there's one thing you have to be careful with when using this technique what is it be careful with the strength of the classifier you're using why is that suppose your classifier has a very low accuracy is it guaranteed that these features that we input which are the embeddings of bert contain no information that we want to classify not necessarily why is that because it's possible that your classifier wasn't trained correctly right you all have a lot of experience with training networks and we know we can't guarantee the classifier to be trained successfully perhaps the accuracy of the classifier is very low after training it's not owing to these features which don't contain the information we need but the learning rate which wasn't adjusted properly perhaps there's a mistake somewhere along the line that made the training fail could that be the case it might be sometimes so when using the probing model you have to be careful not to jump to conclusions too quickly sometimes you will get some conclusions just because your classifier is not well trained or your model is so good that the accuracy of your classifier cannot be treated as a basis for judgment" `[55:00]`

中文翻译："然而，在使用这项技术时，你必须小心一件事。那是什么？要小心你使用的分类器的强度。为什么呢？假设你的分类器准确率非常低，这是否能保证我们输入的这些特征（也就是BERT的嵌入）不包含我们想要分类的信息呢？不一定。为什么呢？因为你的分类器可能没有训练好，对吧？你们都有很多训练网络的经验，我们知道我们不能保证分类器能成功训练。也许训练后分类器的准确率非常低，并不是因为这些特征不包含我们需要的信息，而是学习率没有调整好，或者在某个环节出了错导致训练失败。这种情况可能发生吗？有时会。所以在使用探测模型时，你必须小心，不要过快下结论。有时你得出的一些结论仅仅是因为你的分类器没有训练好，或者你的模型太好了，以至于你的分类器的准确率不能作为判断依据。"

如果探针分类器的准确率很低，我们不能立即断定目标网络的嵌入中不包含相关信息。原因可能是：

- **探针训练不当**：探针本身可能没有被正确训练，例如学习率设置不当，或者训练过程中存在其他错误。
- **探针能力不足**：探针可能过于简单，无法从嵌入中提取出复杂的信息。
因此，在使用探测模型时，必须谨慎，避免过早下结论。有时，低准确率可能只是探针自身的问题，而非目标网络嵌入的缺陷。

**探测的更多可能性：语音合成案例**

李教授进一步展示了探测模型的广阔应用，不仅限于分类器。他以实验室的一个语音合成（Speech Synthesis）项目为例：

重要原话："the probing model does not have to be a classifier i will give you an example that probing has all kinds of possibilities for example one attempt in our laboratory is to train a speech synthesis model the input of general speech synthesis models is a paragraph of text and the model output the corresponding sound signal the input of our speech synthesis model is not a paragraph of text its input is the embedding of the network output it takes embedding of network output as input and then tries to output a sound signal in homework 2 you trained a classifier you trained a phoneme classifier we will take out your network get the output of a certain layer and input it to the tts model to train this tts model the goal of our training is to make the tts model have the ability to reproduce the network input the input of the network is this audio signal i hope that it can generate embeddings after passing these layers after inputting the embeddings to tts it can restore the original sound signal" `[57:00]`

中文翻译："探测模型不一定是分类器。我将给你们一个例子，说明探测有各种可能性。例如，我们实验室的一个尝试是训练一个语音合成模型。一般的语音合成模型的输入是一段文本，模型输出相应的声音信号。我们的语音合成模型的输入不是一段文本，它的输入是网络输出的嵌入。它将网络输出的嵌入作为输入，然后尝试输出声音信号。在作业2中，你们训练了一个分类器，你们训练了一个音素分类器。我们将取出你们的网络，获取某个层的输出，然后将其输入到TTS模型中，训练这个TTS模型。我们训练的目标是让TTS模型能够重现网络输入。网络的输入是这个音频信号，我希望它在经过这些层后能够生成嵌入，然后将嵌入输入到TTS中，它能够恢复原始的声音信号。"

**实验设置**：

1. **目标网络**：学生在作业2中训练的音素分类器（一个语音识别模型）。
1. **探针模型**：一个语音合成（Text-to-Speech, TTS）模型。
1. **探测过程**：
1. **目的**：通过观察TTS模型重构出的音频信号，来判断目标网络的该层嵌入中保留了哪些信息，又丢失了哪些信息。
**分析结果**：

- **消除说话者信息**：
重要原话："assuming this network is to remove information such as the speaker for this tts model the output of layer 2 has no speaker information no matter how hard it tries it cannot restore the characteristics of the speaker although the content is high with a boy's voice you will find that maybe after a few layers the output of the tts model which is the sound it produces will become high but you can't tell who said it you can know that this network a model for speech recognition learned to erase the characteristics of the speaker in the process of training it keeps the content it only keeps the content of the audio signal" `[59:00]`

中文翻译："假设这个网络是为了去除说话者等信息。对于这个TTS模型来说，第2层的输出没有说话者信息，无论它如何努力，都无法恢复说话者的特征。尽管内容是‘你好’，声音是男孩的声音，你会发现也许在几层之后，TTS模型输出的声音会变成‘你好’，但你无法分辨是谁说的。你可以知道这个网络，一个语音识别模型，在训练过程中学会了擦除说话者的特征，它只保留了音频信号的内容。"

实验发现，当从语音识别网络的某些中间层提取嵌入并用TTS模型重构时，重构出的声音可能保留了原始语音的内容（例如“你好”），但却丢失了说话者的个性特征（例如无法分辨是男孩还是女孩说的）。这表明，语音识别模型在训练过程中，学会了**擦除说话者特征**，只保留了音频信号的**内容信息**。

- **过滤背景噪声**：
李教授还展示了另一个例子：一个包含CNN和LSTM层的语音识别模型。

重要原话："the input audio signal is noisy with piano sound ok our network now has several layers of cnn in front there are several layers of bi-directional lstm behind after passing through the first cnn layer the sound signal becomes like this you can still hear the piano the sound in the last layer before the lstm layer is like this you still hear the piano but after passing the first layer lstm it's different it sounds like this you will find that the piano's voice suddenly became much lower so know that the noise of this piano which is the noisy sound signal is filtered out on the first layer of lstm the cnn layers in front do not seem to play a role in filtering out the noise this is what this analysis can tell us" `[1:03:00]`

中文翻译："输入音频信号带有钢琴噪声。好的，我们的网络现在前面有几层CNN，后面有几层双向LSTM。经过第一层CNN后，声音信号变成这样，你仍然能听到钢琴声。在LSTM层之前的最后一层，声音是这样，你仍然能听到钢琴声。但经过第一层LSTM后，就不同了，声音变成这样。你会发现钢琴的声音突然变得非常低，所以我们知道钢琴的噪声，也就是嘈杂的声音信号，在第一层LSTM上被过滤掉了。前面的CNN层似乎在过滤噪声方面没有起到作用。这就是这种分析能告诉我们的。"

实验发现，原始音频信号中包含钢琴噪声。经过前面的CNN层后，重构出的声音仍然能听到钢琴声。但在经过第一层LSTM后，重构出的声音中钢琴声突然变得非常微弱。这表明，模型在**第一层LSTM**中学会了**过滤掉背景噪声**，而前面的CNN层似乎没有起到这个作用。

**个人感受**

李教授在讲解探测模型时，语气中充满了对这种“听见”网络内部声音的兴奋和自豪。他强调了这种方法能够揭示模型在不同阶段对信息进行处理和转换的精妙之处，让人对深度学习的内部机制有了更直观的理解。

**延伸思考**

探测模型提供了一种强大的、可量化的方法来理解模型内部表示的语义内容。它不仅可以用于诊断模型，发现其学习到的特征，还可以指导模型设计，例如，如果某个层应该编码某种信息但探测结果显示没有，则可以调整网络结构或训练策略。这种方法在自然语言处理和语音处理等领域尤其有用。

**精华收获**

探测模型通过训练辅助模型（探针）来分析网络中间层的嵌入，从而揭示模型在不同阶段学习和保留了哪些信息（如语音识别中消除说话者特征、过滤背景噪声）。但需注意探针本身的训练质量，以避免误判。

---

<!-- TLDR: 可解释机器学习不仅关乎信任与合规，更通过揭示模型“作弊”行为和内部机制，指导模型改进，其目标是提供令人满意的解释。 -->

<!-- TAGS: 可解释机器学习, XAI, 深度学习, 模型解释, 显著图, 探测, 梯度, 神经网络 -->

<!-- RATING: 5 -->

---
