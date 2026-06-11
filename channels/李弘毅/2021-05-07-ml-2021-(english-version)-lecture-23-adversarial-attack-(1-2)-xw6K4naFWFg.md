---
title: "[ML 2021 (English version)] Lecture 23:  Adversarial Attack (1/2)"
channel: "李弘毅"
published: "2021-05-07"
source_url: "https://www.youtube.com/watch?v=xw6K4naFWFg"
video_id: "xw6K4naFWFg"
rating: 5
language: "中文"
word_count: 21513
duration: "28:41"
---

# [ML 2021 (English version)] Lecture 23:  Adversarial Attack (1/2)

- **Channel:** 李弘毅
- **Published:** 2021-05-07
- **Source:** https://www.youtube.com/watch?v=xw6K4naFWFg
- **TL;DR:** 深度学习模型即使高准确率也极易受人眼不可察觉的微小扰动欺骗，对抗攻击通过梯度下降和L-infinity约束生成这些“隐形”恶意样本。
- **Rating:** 5

## 版本

- [原始文稿](2021-05-07-ml-2021-(english-version)-lecture-23-adversarial-attack-(1-2)-xw6K4naFWFg.transcript.md)

# 准确率的假象与AI的脆弱性：深度解析对抗性攻击

## 材料信息

- **标题**：[ML 2021 (English version)] Lecture 23: Adversarial Attack (1/2)
- **作者/来源**：李弘毅
- **类型**：YouTube 视频字幕
- **关键元数据**：发布日期不详 (2021年机器学习课程), 视频时长约25分钟（字幕内容覆盖前半部分）
## 开篇引入

在人工智能的璀璨星河中，深度学习模型以其在图像识别、自然语言处理等领域屡创佳绩的超凡能力，赢得了世人的瞩目。我们欣喜于模型在各种基准测试中展现出的高准确率，并满怀期待地将其应用于现实世界的复杂场景。然而，高准确率是否就等同于绝对的可靠性与智能？模型在“正常”环境下表现出色，是否意味着它能抵御一切挑战？

李弘毅教授的这堂课，以其一贯的深入浅出和生动比喻，为我们揭示了深度学习模型光鲜外表下隐藏的一个惊人脆弱性——**对抗性攻击（Adversarial Attack）**。这不仅仅是一个技术细节，它触及了我们对AI系统信任的根基，也迫使我们重新思考，在将AI应用于自动驾驶、医疗诊断、金融风控等关键领域时，除了追求性能指标，我们还需要模型具备怎样的“韧性”和“智慧”来抵御那些意想不到的“恶意”。

这篇深度重构的文章将带你走进对抗性攻击的奇妙世界，理解其原理、实现方式，以及它对AI安全和可靠性带来的深远影响。我们将看到，即使是人眼几乎无法察觉的微小扰动，也能轻易地欺骗一个强大的神经网络，使其给出荒谬而自信的错误判断。这不仅是对现有AI系统鲁棒性的严峻挑战，更是对未来AI发展方向的深刻启示。

## 详细内容

### 1. 准确率的假象：为什么高准确率还不够？ `[00:00-01:50]`

**核心观点**

在真实世界的应用中，仅仅依靠模型在常规条件下的高准确率是远远不够的；模型必须能够抵御来自“恶意”或“敌意”的干扰，否则其在实际场景中的可靠性和价值将大打折扣。

**深度阐述**

李弘毅教授在课程伊始便抛出了一个引人深思的核心问题：我们在机器学习作业中训练了大量神经网络，它们在测试集上取得了令人印象深刻的高准确率，但这是否就意味着这些模型已经足够成熟，可以投入到实际应用中了呢？教授给出了一个明确而警醒的答案：“不”。他指出，高准确率只是模型能力的一个侧面，在现实世界的复杂环境中，模型所面临的挑战远不止“正常”数据那么简单，它还必须能够抵御来自“敌意”（hostility）的蓄意干扰。

这种“敌意”并非抽象概念，而是指那些有目的地试图欺骗、规避或误导模型检测的行为。教授通过两个贴近生活的例子，生动地阐释了这种“敌意”的具象化表现：

1. **恶意行为检测系统**：设想我们开发了一个用于检测网络恶意行为的系统。一旦这个系统被部署，那些从事恶意活动的人（例如黑客、诈骗犯）自然会想方设法地“欺骗”这个系统，以避免自己的行为被识别和拦截。如果模型仅仅在“正常”流量或已知恶意模式上表现出色，而对这种蓄意伪装和规避行为束手无策，那么它的实际防御能力将大打折扣，形同虚设。
1. **垃圾邮件过滤**：这是一个我们日常生活中再熟悉不过的场景。神经网络被广泛应用于判断一封电子邮件是否为垃圾邮件。然而，垃圾邮件发送者（spammers）并非被动接受，他们也在不断进化。为了让自己的垃圾邮件能够成功送达收件箱，他们会持续修改邮件内容、格式，甚至嵌入特殊字符或图片，以试图规避现有的垃圾邮件过滤器。例如，他们可能会用“V!agra”代替“Viagra”，或者将文字嵌入图片中。此时，模型对这些细微但有目的性修改的**鲁棒性（robustness）**——即抵抗干扰的能力——就显得至关重要。如果模型无法有效抵御这些精心设计的规避策略，那么再高的初始准确率也无法阻止垃圾邮件的泛滥。
为了进一步强化“高准确率不等于高可靠性”这一观点，教授巧妙地引入了日本动漫《全职猎人》中的一个经典角色——嵌合蚁蚁王梅路艾姆（Meruem）的比喻。梅路艾姆拥有超越世间万物的力量，其个体战斗力达到了人类无法匹敌的巅峰，他试图将人类从地球上抹去。然而，人类并没有选择与他正面硬碰硬，而是“抛弃了自尊”，直接动用了原子弹这种非对称武器将其消灭。这个故事的寓意在于：即使一个系统（或个体）在某个特定领域表现得极其强大，拥有极高的“准确率”（即战斗力），但如果它无法抵御来自外部的、非传统的“敌意”或“恶意”攻击，那么其强大的表象也可能瞬间瓦解。对于神经网络而言，这意味着仅仅在“正常”数据上表现优秀是远远不够的，它必须能够抵御人类的恶意攻击，才能在真实世界中真正发挥作用。

**重要原话**：

- "a model that achieves high accuracy is not enough it is still far from real applications so what else do we need we need our model to be able to defend against hostility" `[00:20-00:35]` - 中文翻译：一个达到高准确率的模型是不够的，它离实际应用还很远。那么我们还需要什么呢？我们需要我们的模型能够抵御敌意。
- "it is not enough if a network achieves high accuracy in normal conditions it also needs to achieve high accuracy when someone tries to deceive it" `[00:50-01:00]` - 中文翻译：如果一个网络在正常条件下达到高准确率是不够的，当有人试图欺骗它时，它也需要达到高准确率。
- "humans discarded their self-esteem they just deployed an atom bomb to kill him that is the end of the story so what does this tell us it tells us that it is not enough for a network to achieve high accuracy it must defend against human hostility" `[01:30-01:50]` - 中文翻译：人类抛弃了自尊，他们只是部署了一颗原子弹来杀死他。故事就这样结束了。这告诉我们什么？它告诉我们，一个网络仅仅达到高准确率是不够的，它必须抵御人类的敌意。
**延伸思考**

这一部分不仅引出了AI安全和鲁棒性的核心议题，更强调了在AI系统设计中，除了追求性能指标外，对潜在威胁和恶意行为的预判与防御同样重要。在自动驾驶、医疗诊断、金融风控等高风险领域，模型的任何一点脆弱性都可能导致灾难性后果。因此，对抗性攻击的研究不仅仅是学术上的挑战，更是工程实践中不可回避的责任，它促使我们从“追求性能最优”转向“追求安全可靠”。

**精华收获**

高准确率不等于高可靠性。在实际应用中，AI模型必须具备抵御恶意攻击的“韧性”，这比单纯的性能指标更为重要。对抗性攻击是衡量AI系统在真实世界中鲁棒性的关键试金石，它迫使我们重新审视AI的“智能”定义。

### 2. 惊人的脆弱性：对抗性攻击的实际演示 `[01:50-06:50]`

**核心观点**

通过向原始图像添加人眼几乎无法察觉的微小噪声，可以轻易地欺骗一个高性能的深度学习模型，使其给出完全错误的、甚至是攻击者预设的分类结果，这揭示了模型决策机制的非直观性和脆弱性。

**深度阐述**

在理解了“敌意”的重要性之后，李弘毅教授通过一个具体的图像分类案例，直观且震撼地展示了对抗性攻击的惊人效果。他首先回顾了我们在作业中训练的图像分类模型，这些模型通常能够准确识别图像中的物体。然而，对抗性攻击的目标是：在原始图像（benign image）上添加一种**极其微小、人眼几乎无法察觉的“噪声”（noise）**，从而生成一张“攻击图像”（attacked image），使得模型对攻击图像的预测结果与原始图像的预测结果大相径庭，甚至完全错误。

教授特别强调，虽然在视频演示中，为了让观众能够看到“噪声”的存在，可能将其放大了一些，但理想的对抗性噪声应该是**“人眼不可察觉”（human imperceptible）**的。这意味着，人类观察者在看到原始图像和攻击图像时，几乎无法分辨出它们之间的差异，但模型却会给出截然不同的判断。

攻击可以大致分为两种主要类型：

1. **无目标攻击 (Targetless Attack)**：这种攻击的目标相对简单，仅仅是希望让模型的预测结果“不是”原始的正确类别。例如，如果原始图像被识别为“猫”，无目标攻击只是希望模型将其识别为“除了猫以外的任何东西”，具体是哪种错误类别并不重要。
1. **有目标攻击 (Targeted Attack)**：这是一种更具挑战性、也更具威胁性的攻击。攻击者不仅希望模型预测错误，还希望模型将图像识别为**特定的、预设的错误类别**。例如，攻击者希望将一张“猫”的图片，通过添加噪声，让模型坚定地认为它是一只“海星”。
教授随后展示了一个令人震惊的实验，使用的模型是一个拥有50层的ResNet，这在当时被认为是相当强大和先进的网络：

- **原始图像**：一张清晰的“虎斑猫”图片。当这张图片被输入ResNet时，模型对其的预测是“虎斑猫”，并给出了0.64的置信度。考虑到模型可能在2000个类别中进行选择，0.64的置信度已经算相当高了。
- **攻击过程**：向这张“虎斑猫”图片添加了人眼几乎无法察觉的微小噪声。
- **攻击结果1 (有目标攻击)**：将添加噪声后的图片输入ResNet，模型竟然以**高达100%的置信度**将其识别为“海星”！教授特意强调，最初模型对“猫”的识别置信度是0.64，而现在对“海星”的置信度却是100%，这表明模型对这个错误预测“深信不疑”，毫无犹豫。
- **视觉/结构信息描述**：为了证明原始图片和攻击图片确实存在差异，教授展示了将两张图片相减并放大50倍后的“差异图”。这张差异图清楚地显示了像素级别的微小变化，证明了攻击图像并非原始图像的简单复制，而是经过了精心构造的修改。尽管这些差异对人类来说微不足道，但对ResNet而言，却是天壤之别，足以彻底改变其判断。
- **攻击结果2 (有目标攻击)**：为了进一步证明这种脆弱性并非“猫”与“海星”之间的特殊关系，教授再次展示了将同一张“猫”的图片，通过添加不同的微小噪声，使其被ResNet以0.98的置信度识别为“键盘”！这种从“猫”到“键盘”的跳跃，彻底颠覆了我们对模型“智能”的认知，也排除了特殊类别关联的可能性。
教授还对比了**人眼可察觉噪声**对模型预测的影响，以区分对抗性攻击的特殊性：

- 当噪声明显可见时（例如，图像中出现大量肉眼可见的斑点），模型可能会将“虎斑猫”识别为“波斯猫”（因为噪声可能使其看起来更蓬松），甚至识别为“壁炉屏风”（fire screen）。在这种情况下，虽然模型预测错误，但我们人类可以理解其“错误”的逻辑——模型可能将噪声本身误认为是图像的一部分，例如将橙色的猫看作火焰，而噪声看作屏风。这种错误虽然是错，但至少在某种程度上是“可解释”的。
- 然而，当噪声人眼不可察觉时，模型给出的“海星”或“键盘”这样的预测，对人类而言是完全“无意义”且“不可解释”的。这种现象深刻揭示了深度学习模型决策过程的非直观性和深层脆弱性，表明模型可能在学习一些对人类来说不重要的、甚至是不稳定的特征，而这些特征却成为了攻击者利用的“后门”。
**重要原话**：

- "we can apply some noise a noise that is really small an image can be considered a very long vector and we can introduce some little noise to every dimension of the vector then we input this noise-added image to the network and observe what happens generally this noise is quite small it is too small that humans are not aware of it" `[02:00-02:25]` - 中文翻译：我们可以施加一些噪声，一种非常小的噪声。一张图片可以被视为一个非常长的向量，我们可以向向量的每个维度引入一些微小的噪声。然后我们将这张添加了噪声的图片输入网络，观察会发生什么。通常这种噪声非常小，小到人类无法察觉。
- "the attacked image which is perturbed by the bad guys can make the model prediction differ" `[02:50-03:00]` - 中文翻译：被“坏人”扰动的攻击图像可以使模型的预测结果不同。
- "we not only want the output of the model is not a cat but also is the desired class for example we hope that after adding noise the model prediction becomes a starfish" `[03:20-03:35]` - 中文翻译：我们不仅希望模型的输出不是猫，而且是期望的类别。例如，我们希望在添加噪声后，模型的预测变成海星。
- "the output of resnet becomes starfish with a confidence score of 100 initially res net was not so sure if it was a cat but now the model is 100 sure that it is a starfish" `[04:50-05:10]` - 中文翻译：ResNet的输出变成了海星，置信度为100%。最初ResNet对它是否是猫并不那么确定，但现在模型100%确定它是一只海星。
- "you can easily turn this cat into anything i can simply add another noise to make this cat a keyboard and the confidence score is as high as 0.98" `[05:50-06:10]` - 中文翻译：你可以轻易地把这只猫变成任何东西。我只需添加另一个噪声，就能让这只猫变成键盘，而且置信度高达0.98。
**个人感受**

看到这些演示，我作为学习者，内心充满了震撼和一丝不安。一个如此强大的ResNet，竟然能被如此微小的、人眼不可见的扰动所欺骗，而且是如此“自信”地给出荒谬的答案。这让我对AI模型的“智能”产生了更深层次的疑问：它们真的理解图像内容吗？还是仅仅在学习一些我们无法理解的、脆弱的模式？这种脆弱性在实际应用中是极其危险的，例如在自动驾驶中，一个微小的路标贴纸可能导致车辆识别错误；在医疗诊断中，微小的像素扰动可能让模型误判病情。

**延伸思考**

这种现象揭示了深度学习模型与人类感知之间存在的巨大鸿沟。模型可能在学习一些对人类来说不重要的特征，而这些特征却成为了攻击者利用的“后门”。这促使我们思考，如何才能让模型不仅在统计意义上准确，更能在语义和感知意义上鲁棒，从而真正值得信赖。

**精华收获**

对抗性攻击证明了深度学习模型在面对精心构造的微小扰动时，其鲁棒性远低于人类预期。人眼不可察觉的噪声可以导致模型输出完全错误的、甚至预设的分类结果，这暴露了模型决策机制的脆弱性和非直观性，对AI的可靠性提出了严峻挑战。

### 3. 对抗样本的生成原理：一个优化问题 `[06:50-10:50]`

**核心观点**

生成对抗样本本质上是一个优化问题：通过调整输入图像（添加噪声），在满足噪声人眼不可察觉的约束下，最大化模型对错误类别的预测概率（无目标攻击）或最大化对特定目标类别的预测概率（有目标攻击）。

**深度阐述**

在展示了对抗性攻击的惊人威力之后，李弘毅教授开始深入讲解如何从技术层面实现这种攻击。他指出，生成对抗样本的核心是一个精巧的优化问题。

首先，我们有一个已经训练好的神经网络，可以将其抽象为一个函数 `f`。这个函数接收一个输入图像 `x0`（原始图像），并输出其分类预测结果 `y0`。在整个攻击过程中，这个网络的**参数是固定不变的**，我们不会去修改它们。我们的核心目标是找到一个新的图像 `x`（攻击图像），使得网络 `f(x)` 的输出 `y` 能够达到我们预设的攻击目的。

**无目标攻击 (Non-targeted Attack) 的目标与损失函数**：

- 无目标攻击的目的是让 `f(x)` 的输出 `y` 与原始图像 `x0` 的正确标签 `y`*`hat`** 之间存在尽可能大的差异。换句话说，我们希望模型不再预测正确的类别。*
- 为了实现这一点，我们可以定义一个损失函数 `L`。在分类任务中，我们通常使用交叉熵（cross-entropy）来衡量预测 `y` 与真实标签 `y`*`hat`** 之间的距离。交叉熵越小，表示预测越接近真实标签。*
- 然而，我们的目标是让预测偏离真实标签，即最大化 `y` 与 `y`*`hat`** 之间的交叉熵。在优化问题中，最大化一个函数等价于最小化其负值。因此，无目标攻击的损失函数可以定义为：**`L = - CrossEntropy(y, y`*`hat)`。通过最小化这个 `L`，我们实际上是在最大化 `y` 与 `y`*`hat`** 之间的交叉熵，从而迫使模型预测结果偏离原始的正确标签。*
**有目标攻击 (Targeted Attack) 的目标与损失函数**：

- 有目标攻击更为复杂和精确。我们不仅希望 `y` 与 `y`*`hat`** 不同，还希望 **`y`** 尽可能接近我们预设的目标标签 **`y`*`target`。例如，将“猫”识别为“海星”。
- 此时的损失函数需要同时考虑两个相互关联的方面：
- 因此，有目标攻击的损失函数可以表示为这两项之和：`L = - CrossEntropy(y, y`*`hat) + CrossEntropy(y, y`*`target)`。通过最小化这个复合损失函数 `L`，我们既让模型远离原始标签，又让它靠近目标标签，从而实现精确的误分类。
然而，仅仅最小化损失函数是不足以生成有效对抗样本的。我们还有一个至关重要的**约束条件**：**新生成的攻击图像 ****`x`**** 必须与原始图像 ****`x0`**** 尽可能接近，以确保添加的噪声对人眼不可察觉。**

- 这个约束通常表示为：`d(x0, x) <= sigma`，其中 `d` 是一个衡量两张图片之间差异的距离函数，`sigma` 是一个预设的阈值，代表人类感知能力的极限。如果 `d(x0, x)` 超过 `sigma`，人类就能察觉到图像被修改了。这个约束是确保对抗样本“隐蔽性”的关键。
**重要原话**：

- "This is our network this is a function called f this function takes an image as input which is called x0 and output the prediction result of the classification the prediction result is called y0 then we assume that the parameters of the network here are fixed" `[07:00-07:25]` - 中文翻译：这是我们的网络，这是一个名为f的函数。这个函数接收一个图像作为输入，称为x0，并输出分类的预测结果，称为y0。然后我们假设网络的参数在这里是固定的。
- "the goal is to get a new image which is denoted as x then the network f output y when given the input x then correct label of the input x as y-hat we hope that the bigger the gap between y and y-hat the better that is the non-targeted attack" `[07:40-08:05]` - 中文翻译：目标是得到一个新图像，表示为x，然后网络f在给定输入x时输出y。输入x的正确标签为y-hat。我们希望y和y-hat之间的差距越大越好，这就是无目标攻击。
- "we want to maximize the cross-entropy accordingly we put a negative sign in front of cross-entropy then this negative cross-entropy is our loss and we minimize this loss" `[08:40-09:00]` - 中文翻译：我们希望最大化交叉熵，因此我们在交叉熵前面加上一个负号，然后这个负交叉熵就是我们的损失，我们最小化这个损失。
- "we now hope that y will be not only different from y hat but also be close to y target" `[09:40-09:55]` - 中文翻译：我们现在希望y不仅与y*hat不同，而且接近y*target。
- "we hope our newly found picture which could deceive the network is as close to the original picture as possible x and x0 should be as close as possible so when we solve this problem of optimization we add one more restriction which is d of x0 x less than or equal to sigma" `[10:20-10:50]` - 中文翻译：我们希望我们找到的能够欺骗网络的新图片尽可能接近原始图片。x和x0应该尽可能接近，所以当我们解决这个优化问题时，我们添加了一个限制，即d(x0, x)小于或等于sigma。
**延伸思考**

将对抗样本生成框架化为一个带约束的优化问题，是理解其核心机制的关键。这表明攻击者并非随机地添加噪声，而是通过一个有目的、有数学依据的过程来寻找最有效的扰动。这种方法论也为后续的防御研究提供了明确的方向：如何设计模型或训练策略，使其在满足这些优化目标时，仍然能够保持鲁棒性，不被轻易欺骗。

**精华收获**

对抗样本的生成是一个带约束的优化问题。其核心在于构建一个损失函数，引导模型预测错误（无目标）或特定目标（有目标），同时通过距离函数和阈值约束，确保添加的噪声对人眼不可察觉，从而实现隐蔽而有效的攻击。

### 4. 衡量“人眼不可察觉”：距离度量的重要性 `[10:50-15:40]`

**核心观点**

在衡量图像差异以确保噪声人眼不可察觉时，选择合适的距离度量至关重要。L-infinity范数通常比L2范数更能反映人类对图像局部最大变化的敏感性，因此在对抗性攻击中常被用作约束。

**深度阐述**

在上一节中，我们提到了一个关键的约束条件：`d(x0, x) <= sigma`，即攻击图像 `x` 与原始图像 `x0` 之间的差异必须小于人类可感知的阈值 `sigma`。那么，这个差异 `d(x0, x)` 应该如何计算，才能真实地反映“人眼不可察觉”这一特性呢？李弘毅教授详细介绍了两种常用的距离度量方法：L2范数和L-infinity范数，并通过一个直观的例子解释了它们之间的差异以及为何L-infinity范数在对抗性攻击中更受青睐。

首先，为了方便计算，我们将图像 `x0` 和 `x` 都视为一个很长的向量（将所有像素值按顺序排列）。那么它们之间的差异向量 `delta`*`x`** 就是 **`x - x0`**，其中每个元素 **`delta`*`xi` 代表对应像素的变化量。

1. **L2 范数 (L2 Norm)**：
1. **L-infinity 范数 (L-infinity Norm)**：
为了说明这两种范数与人类感知的关联，教授举了一个生动的4像素图像的例子：

- **原始图像**：一个由4个像素组成的简单图像。
- **改变方式1**：对这4个像素的颜色都进行**非常微小**的改变。
- **改变方式2**：只改变右下角一个像素的颜色，但改变的幅度相对**较大**。
教授指出，在这两种改变方式下，计算出的L2范数可能是相同的。这意味着从L2范数的角度看，这两种改变的“总差异能量”是等价的。

然而，如果从L-infinity范数的角度来看，情况则大相径庭：

- 对于改变方式1（所有像素微小变化），L-infinity范数会很小，因为它只取所有微小变化中的最大值，而这些变化本身就很小。
- 对于改变方式2（一个像素较大变化），L-infinity范数会相对较大，因为它直接取的是那个较大变化的像素值。
关键在于，人类的感知系统对“局部最大变化”更为敏感。在改变方式1中，所有像素都只有极其微小的变化，这些变化被均匀地分散开来，人类可能很难察觉到图像被修改了。但在改变方式2中，即使只有一个像素发生了相对较大的变化（例如，右下角出现了一块明显的暗绿色），这种集中式的、显著的变化会立即引起人类的注意，让人察觉到图像被修改了。

因此，教授得出结论：**L-infinity范数可能更符合人类的实际感知需求。**为了确保对抗性噪声对人眼不可察觉，我们更倾向于限制L-infinity范数，使其尽可能小。在实际的对抗性攻击研究和作业中，L-infinity范数通常被用作衡量噪声大小和隐蔽性的主要约束条件。

最后，教授强调了**领域知识 (domain knowledge)** 在选择距离度量时的重要性。

- 上述例子是针对图像的。但如果攻击目标是语音相关的系统，那么 `x` 和 `x0` 将是音频信号。此时，L2或L-infinity范数可能不再是衡量“人耳不可察觉”的最佳方式。人类听觉系统对声音的频率、音量、持续时间等变化有其独特的敏感性。因此，我们需要深入研究人类听觉系统对哪些类型的变化特别敏感（例如，掩蔽效应、响度感知），然后根据这些生理和心理声学知识来设计更符合人耳感知的距离度量方法，以确保生成的对抗性音频对人类听起来是正常的，但能欺骗模型。
**重要原话**：

- "how do we calculate the difference between x and x zero how do we calculate the distance between them d of x zero x represents the distance between them there are different algorithms for it" `[11:00-11:15]` - 中文翻译：我们如何计算x和x0之间的差异？我们如何计算它们之间的距离？d(x0, x)代表它们之间的距离，有不同的算法。
- "you can use l2 norm as their distance in other words you can calculate the l2 norm of delta x" `[11:40-11:50]` - 中文翻译：你可以使用L2范数作为它们的距离，换句话说，你可以计算delta x的L2范数。
- "what is l infinity it is taking this delta x seeing which dimension has the largest absolute value and that one is l infinity" `[12:15-12:30]` - 中文翻译：什么是L-infinity？它是取这个delta x，看哪个维度有最大的绝对值，那个就是L-infinity。
- "if you look at l infinity and l2 from this example which is closer to human perception maybe it should be l infinity because for you these two pictures i believe most of you may not be able to tell the difference between them" `[14:20-14:50]` - 中文翻译：如果你从这个例子来看L-infinity和L2，哪个更接近人类感知？也许应该是L-infinity，因为对于你来说，这两张图片，我相信你们大多数人可能无法分辨它们之间的差异。
- "so it seems that l infinity may be more in line with actual needs if we want to avoid being perceived by a human a small l2 is not enough we want to make l infinity the smaller the better to make it less likely to be perceived" `[15:10-15:40]` - 中文翻译：所以看起来L-infinity可能更符合实际需求。如果我们想避免被人类察觉，一个小的L2是不够的。我们希望L-infinity越小越好，以使其更不容易被察觉。
**延伸思考**

距离度量的选择直接影响了对抗样本的隐蔽性和攻击效果。L-infinity范数在图像领域之所以有效，是因为它与人类视觉系统对“最显著变化”的敏感性相吻合。这提醒我们，在设计AI系统时，不仅要考虑数学上的优化，更要深入理解人类的感知机制，才能构建出真正鲁棒和安全的系统。

**精华收获**

L-infinity范数因其关注局部最大变化的特性，在衡量图像差异以确保对抗性噪声人眼不可察觉方面，比L2范数更符合人类感知。选择合适的距离度量需要结合具体的领域知识，以确保攻击的隐蔽性和有效性。

### 5. 解决优化问题：基于梯度下降的对抗样本生成 `[15:40-20:50]`

**核心观点**

生成对抗样本的优化问题可以通过修改后的梯度下降算法来解决。核心思想是将输入图像视为可优化的参数，通过计算损失函数对输入图像的梯度来迭代更新图像，并结合投影操作来强制满足人眼不可察觉的噪声约束。

**深度阐述**

现在我们已经明确了对抗样本生成是一个带约束的优化问题：即最小化损失函数 `L(x)`，同时满足 `d(x0, x) <= sigma` 的约束。李弘毅教授接着解释了如何使用我们熟悉的梯度下降（Gradient Descent）算法来解决这个看似复杂的问题。

他首先提出了一个巧妙的简化思路：如果暂时忽略约束条件，我们是否知道如何解决最小化损失函数的问题？答案是肯定的。在传统的神经网络训练中，我们通过调整网络参数（权重和偏置）来最小化损失函数。现在，情况只是发生了转变：**网络的参数是固定不变的，我们需要调整的是输入图像 ****`x`**** 的像素值来最小化损失。** 这本质上与训练网络是相同的优化过程，只是优化对象从网络权重变成了输入图像的像素值。我们可以把输入图像的每个像素值看作是网络的“参数”，然后对这些“参数”进行优化。

**梯度下降生成对抗样本的详细步骤**：

1. **初始化 (Initialization)**：
1. **迭代更新 (Iterative Update)**：
**处理约束条件：投影梯度下降 (Projected Gradient Descent)**：

- 上述梯度下降过程在没有约束的情况下会一直进行。但现在，我们必须将 `d(x0, x) <= sigma` 这个约束重新引入，以确保生成的噪声人眼不可察觉。
- 教授提供了一个非常巧妙且实用的方法来处理这个约束：**投影操作**。
- 具体操作是：在每次梯度下降更新 `x` 之后，立即检查新的 `x` 是否满足约束条件。如果 `x` 超出了允许的范围（例如，L-infinity范数超过了 `sigma`），就将其“拉回”到允许范围内的最近点。
- 以L-infinity范数为例：如果 `x0` 是原始图像，那么所有满足 `||x - x0||`*`inf <= sigma`** 的 **`x`** 构成一个以 **`x0`** 为中心、边长为 **`2sigma`** 的超立方体（在二维空间中可以想象成一个正方形）。*
- 如果在梯度下降一步后，新的 `x` 落在了这个超立方体之外（例如，图示中的蓝色点跑出了方框），我们就找到超立方体上离这个蓝色点最近的点，并将 `x` 投影到那个点上。这个操作确保了每次更新后的 `x` 都满足噪声人眼不可察觉的条件。
教授总结道，虽然文献中存在各种各样的对抗性攻击方法，但它们的核心思想都是基于这种梯度下降和约束处理的结合。它们之间的差异主要在于损失函数的具体形式（例如，不同的交叉熵变体）、约束条件的选择（L2、L-infinity或其他更复杂的感知距离），以及优化器的具体实现细节，但其“精神”是相同的——通过优化输入来欺骗模型。

**重要原话**：

- "if there are no restrictions can we solve this problem well we actually know how to solve that as it's no different from training a normal model" `[16:10-16:25]` - 中文翻译：如果没有限制，我们能解决这个问题吗？嗯，我们实际上知道如何解决，因为它与训练一个普通模型没有什么不同。
- "now we're simply replacing the parameters with the input that's it just treat the input image as part of the network parameters and minimize the loss then we're done" `[16:40-17:00]` - 中文翻译：现在我们只是简单地用输入替换参数，就是这样。只需将输入图像视为网络参数的一部分，并最小化损失，然后我们就完成了。
- "we still need an initial value when doing gradient descent what kind of value is better for the initial value you might not start with a random image instead you might start with x0" `[17:20-17:40]` - 中文翻译：在进行梯度下降时，我们仍然需要一个初始值。什么样的初始值更好呢？你可能不会从随机图像开始，而是从x0开始。
- "it's just that it's not the gradient of the network parameters with regard to the loss we're now focusing on the gradient of the input image with regard to the loss" `[18:20-18:40]` - 中文翻译：只是它不是网络参数相对于损失的梯度，我们现在关注的是输入图像相对于损失的梯度。
- "we will add a module into the gradient descent procedure... after you finished updating the parameters and discovered that the difference between x t and x 0 is greater than epsilon just modify x t directly to satisfy the constraints" `[19:40-20:20]` - 中文翻译：我们将在梯度下降过程中添加一个模块……在你完成参数更新后，如果发现x*t和x0之间的差异大于epsilon，只需直接修改x*t以满足约束。
- "if you get the blue point and find it out of the box after this step what should we do find a position in the box that is closest to the blue point and then pull the blue point in done it's over" `[20:30-20:50]` - 中文翻译：如果你得到蓝点，并且发现它在这一步之后超出了方框，我们该怎么办？找到方框中离蓝点最近的位置，然后把蓝点拉回来，就完成了。
**延伸思考**

将输入图像视为可优化的参数，是理解对抗性攻击生成机制的关键洞察。这种“反向传播到输入”的思想，不仅用于生成对抗样本，也广泛应用于特征可视化、模型解释性等领域。投影梯度下降是一种通用的处理约束优化问题的方法，其思想在机器学习和优化领域具有广泛应用，为解决实际问题提供了强大的工具。

**精华收获**

对抗样本的生成是通过对输入图像进行梯度下降实现的。其过程包括初始化为原始图像，计算损失函数对输入图像的梯度，并迭代更新图像。为了满足人眼不可察觉的约束，每次更新后，如果图像超出了允许的范围，就必须将其投影回最近的合法区域，从而确保攻击的隐蔽性和有效性。

### 6. 快速梯度符号法 (FGSM) 及其变体 `[20:50-24:50]`

**核心观点**

快速梯度符号法（FGSM）是一种简单而高效的单步对抗性攻击方法，它通过对损失函数关于输入图像的梯度取符号，并乘以一个小的步长（epsilon），来生成对抗样本。通过迭代应用FGSM并结合投影操作，可以实现更强的攻击效果。

**深度阐述**

在介绍了梯度下降生成对抗样本的通用框架后，李弘毅教授引入了一种最简单、最基础但非常有效的攻击方法：**快速梯度符号法（Fast Gradient Sign Method, FGSM）**。这种方法因其简洁性和高效性而广受欢迎。

**FGSM 的核心思想**：

- FGSM 被教授形象地比喻为“一拳超人”（One-Punch Man），因为它只进行**一次更新**。与传统的梯度下降需要多次迭代更新参数不同，FGSM的强大之处在于，它试图通过一次“打击”就成功生成对抗样本。
- FGSM的更新公式是：`x = x0 + epsilon `*` sign(∇x L)`*
- 这意味着，`sign(∇`*`x L)`** 得到的向量 **`g`**，其每个维度上的值都只能是1或-1（或0）。*
- 因此，FGSM的更新操作就是：在原始图像 `x0` 的基础上，沿着梯度的“方向”（即每个像素是增加还是减少，而不是增加或减少多少）移动 `epsilon` 的距离。每个像素要么增加 `epsilon`，要么减少 `epsilon`。
**FGSM 的效果与特点**：

- 由于每个像素的变化量都是 `+epsilon` 或 `-epsilon`，这意味着攻击后的图像 `x` 相对于 `x0`，其L-infinity范数恰好等于 `epsilon`。这天然地满足了L-infinity范数约束。
- 在二维空间中，这意味着 `x` 将会落在以 `x0` 为中心、边长为 `2`*`epsilon`** 的正方形的四个角上。*
- 教授指出，这种单步攻击通常足以通过“简单基线”（simple baseline）的对抗性攻击挑战，证明了其基本的有效性。
**迭代式 FGSM (Iterative FGSM, I-FGSM)**：

- 一些学生可能会问：如果多攻击几次，效果会不会更好？答案是肯定的。
- I-FGSM（也称为Basic Iterative Method, BIM）就是将FGSM的单步更新扩展为多步迭代。
- 更新公式变为：`x`*`t+1 = x`*`t + alpha `*` sign(∇x L)`**，其中 **`alpha`** (**`α`**) 是一个比 **`epsilon`** 小的学习率。这意味着每次迭代只进行一小步的更新。*
- 在每次迭代后，仍然需要执行**投影操作**，将 `x` 投影回以 `x0` 为中心、L-infinity范数约束为 `epsilon` 的超立方体（即 `||x - x0||`*`inf <= epsilon`**）。这意味着即使在迭代过程中 **`x`** 暂时超出了这个范围，也会被拉回到最近的合法点，从而始终保持噪声的隐蔽性。*
- 通过多次迭代，I-FGSM可以生成更强大、更有效的对抗样本，通常能够通过“中等基线”（medium baseline）的攻击挑战。
教授在课程结束时强调，虽然还有许多其他变种的攻击方法（例如C&W攻击、DeepFool等），但它们都建立在今天讨论的这些基本原理之上。它们可能在损失函数的具体形式、优化器或约束条件上有所不同，但核心的梯度下降和投影思想是共通的。理解FGSM及其迭代变体，是掌握对抗性攻击领域其他更复杂方法的基础。

**重要原话**：

- "let's introduce one of the easiest methods of attack this should be the method that can pass the medium baseline what is this method this method is called fgsm can it pass the medium baseline oh it can't pass the medium baseline it can only pass the simple baseline" `[21:10-21:35]` - 中文翻译：让我们介绍一种最简单的攻击方法，这种方法应该能通过中等基线。这种方法叫什么？它叫FGSM。它能通过中等基线吗？哦，它不能通过中等基线，它只能通过简单基线。
- "its full name is fastgradientsign method how does it do it's like the one punch man it only takes one hit normally when you are doing gradient descent you have to update parameters many times but what makes fgsm powerful is that it decides to update the parameters only once and see if you can kill with one hit" `[21:45-22:15]` - 中文翻译：它的全名是快速梯度符号法。它是怎么做的？它就像一拳超人，只用一击。通常你在进行梯度下降时，你必须多次更新参数，但FGSM的强大之处在于它决定只更新一次参数，看看能否一击致命。
- "this sign means if the value in the brackets is greater than 0 the output is 1. if the value in the brackets is less than 0 the output is negative one so after adding a sign the element in vector g is either one or negative one" `[22:40-23:05]` - 中文翻译：这个符号意味着如果括号中的值大于0，输出是1。如果括号中的值小于0，输出是-1。所以在添加符号后，向量g中的元素要么是1，要么是-1。
- "after you attack you must fall on the four corners of this blue frame because you think about it this g is either one or negative one each dimension of it is either one or negative one then the front of it will be multiplied by epsilon so after multiplying epsilon your x zero today may move epsilon steps to the right or move epsilon steps to the left or move up epsilon steps or move down epsilon steps" `[23:30-24:10]` - 中文翻译：攻击后，你必须落在蓝色框架的四个角上，因为你想想，这个g要么是1要么是-1，它的每个维度要么是1要么是-1，然后前面会乘以epsilon。所以乘以epsilon后，你的x0今天可能会向右移动epsilon步，或者向左移动epsilon步，或者向上移动epsilon步，或者向下移动epsilon步。
- "if i attack a few more times wouldn't it be better after a few more iterations it will be better so you run a few more iterations then you pass the medium baseline that's it" `[24:20-24:40]` - 中文翻译：如果我多攻击几次，会不会更好？多迭代几次会更好，所以你多运行几次迭代，然后你就通过了中等基线，就是这样。
**延伸思考**

FGSM的简洁性使其成为理解对抗性攻击入门的绝佳方法。它揭示了模型对梯度方向的敏感性，即使是微小的、符号化的梯度信息也能产生显著的攻击效果。I-FGSM则展示了通过迭代和投影，可以在保持隐蔽性的同时增强攻击强度，这为更复杂的攻击方法奠定了基础，也为防御策略的开发提供了思路。

**精华收获**

FGSM是一种高效的单步对抗性攻击，通过对损失函数梯度取符号并乘以步长来生成对抗样本，其结果在L-infinity范数约束下。迭代式FGSM通过多次应用FGSM并结合投影操作，可以生成更强的对抗样本，从而通过更具挑战性的攻击基线。这些方法都利用了模型对输入梯度方向的敏感性，是理解对抗性攻击机制的基石。

<!-- TLDR: 深度学习模型即使高准确率也极易受人眼不可察觉的微小扰动欺骗，对抗攻击通过梯度下降和L-infinity约束生成这些“隐形”恶意样本。 -->

<!-- TAGS: 对抗性攻击, 深度学习, 机器学习安全, 梯度下降, L-infinity范数, FGSM, 模型鲁棒性, AI安全 -->

<!-- RATING: 5 -->

---
