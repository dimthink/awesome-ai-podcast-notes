---
title: "ML Lecture 2: Where does the error come from? - 结构化文稿"
channel: "李弘毅"
published: "2016-10-07"
source_url: "https://www.youtube.com/watch?v=D_S6y0Jm6dQ"
video_id: "D_S6y0Jm6dQ"
variant: "structured"
---

# ML Lecture 2: Where does the error come from? - 结构化文稿

- **Channel:** 李弘毅
- **Published:** 2016-10-07
- **Source:** https://www.youtube.com/watch?v=D_S6y0Jm6dQ
- **Main:** [ML Lecture 2: Where does the error come from?](2016-10-07-ml-lecture-2-where-does-the-error-come-from-D_S6y0Jm6dQ.md)

# 机器学习第2讲：误差从何而来？——偏差与方差（Bias and Variance）

## 引言：误差的来源与诊断的重要性

在上一节课中，我们看到：如果你选择不同的 function set（也就是选择不同的 model），在 testing data 上也会得到不同的 error。你会发现，越复杂的 model 不见得会给你越低的 error。以线性回归为例，考虑 input 的次方数从 1 次、2 次、3 次一直到 5 次，结果发现最复杂的 model 其实它的 performance 是最差的。

今天我们要讨论的问题就是：**这个 error 来自什么地方？** 其实 error 有两个来源：一个是来自 **bias**，一个是来自 **variance**。

了解 error 的来源非常重要。因为当你做完 machine learning 发现 error rate 是 60% 时，接下来要怎么 improve 你的 model 呢？如果没有方向，毫无头绪地乱做，效率就很低。如果你可以诊断 error 的来源（比如 error 分为 bias 和 variance），你就可以挑选适当的方法来 improve 你的 model。

## 偏差与方差的基本概念

### 以打靶比喻误差的来源

我们以宝可梦进化后的 CP 值估测为例。我们要找一个 function，输入一只宝可梦，输出它进化后的 CP 值。理论上存在一个最佳的 function，我们记作 **f̂**，但我们不知道它，只有 Niantic（宝可梦公司）知道，因为那是写进程序里的。

我们能做的是：收集一些 training data，实际抓一些宝可梦，然后根据 training data 学出一个最好的 function **f***。f* 并不等于 f̂，它就像 f̂ 的一个估计值。可以把这想象成打靶：f̂ 是靶心，你收集 data 训练后找到的 f* 是靶纸上的一个点。f* 与 f̂ 之间的距离来自两件事：**bias** 和 **variance**。

### 回顾统计中的均值与方差估计

在概率与统计中，我们学过如何估计一个随机变量的均值。假设一个变量 x 的均值是 μ，方差是 σ²。要估计均值，我们 sample N 个点 x¹, x², …, xᴺ，计算它们的平均值 m。这个 m 一般不会正好等于 μ，除非 sample 无穷多个点。

- 如果你做多次实验，每次 sample N 个点得到 m₁, m₂, …，这些 m 的期望值 E[m] = μ，所以 **m 是 μ 的无偏估计**。就像打靶时准心瞄准 μ，但由于机械故障或风速干扰，子弹会散落在瞄准点周围。
- 散落的程度由 m 的方差决定：Var[m] = σ²/N。N 越大，m 越集中；N 越小，m 越分散。
如果要估计方差 σ²，可以先估计 m，再计算 s² = (1/N) Σ (xⁿ - m)²。这个 s² 的期望值 E[s²] = (N-1)/N · σ²，所以 **s² 是 σ² 的有偏估计**，普遍比 σ² 偏小。当 N 增大时，偏差会减小。

## 不同模型复杂度下的偏差与方差

回到 regression 问题：靶心是 f̂，每次实验收集 data 得到 f*。f* 与 f̂ 的误差由两部分组成：

- **bias**：f* 的期望值 f̄（即多次实验的 f* 的平均）与 f̂ 的距离。
- **variance**：每次实验的 f* 与期望值 f̄ 的距离。*
理想的状况是 **bias 小且 variance 小**，这样每次找出的 f* 都很好。*

### 如何观察多个 f*？*

实际上我们只能做一次实验，怎么知道 variance 和 bias 呢？可以想象存在多个平行宇宙，每个宇宙里抓到的 10 只宝可梦不同，从而得到不同的 f*。通过在不同宇宙中重复实验，就能看到 f* 的分布。

下面用实验展示不同模型复杂度下的 variance：

- **简单模型（如 y = b + w·x*****cp）****：在 100 个平行宇宙中，每次抓 10 只宝可梦，得到的 100 条直线几乎都集中在一起，****variance 小****。*
- **复杂模型（如考虑 x*****cp, (x*****cp)², (x*****cp)³）****：100 条曲线像花一样散开，****variance 大****。*
- **更复杂模型（5 次式）**：100 条曲线极度分散，几乎覆盖整个空间，**variance 非常大**。
为什么简单模型 variance 小？因为简单模型受 data 影响小。极端例子：若 model 只有一个常数函数，无论 data 如何，f* 都一样，variance = 0。随着复杂度增加，variance 增大。*

### bias 的观察（需假设真实 f̂）

要测量 bias，必须先知道真正的 f̂。这里我们假设一个 f̂（比如一条直线），并从它 sample 出宝可梦 data。实验如下：

- **1 次式（简单模型）**：5000 次实验得到的 5000 条直线几乎重叠，它们的平均 f̄（蓝色线）与真正的 f̂（黑色线）有明显差距 → **bias 大**。
- **3 次式**：5000 条曲线头尾很散，但平均 f̄ 与 f̂ 比较接近 → **bias 小**。
- **5 次式**：5000 条曲线完全散开，但平均 f̄ 与 f̂ 非常接近 → **bias 很小**。
为什么会这样？因为 model 对应一个 function set：

- 简单 model 的 function set 较小，可能根本没有包含 target f̂，所以无论怎么平均都无法接近靶心 → bias 大。
- 复杂 model 的 function set 较大，可能包含 target，但由于 data 有限，每次找出的 f* 散落在 target 附近，平均后就能接近 target → bias 小。*
### 总结：模型复杂度与 bias/variance 的关系

- **简单 model**：bias 大，variance 小。
- **复杂 model**：bias 小，variance 大。
考虑 bias 和 variance 共同作用，testing error 会先下降后上升（如蓝色曲线），在某个复杂度点达到平衡。当 model 太复杂时，variance 增长过快，导致 overfitting；当 model 太简单时，bias 大，导致 underfitting。

## 如何判断问题是 bias 大还是 variance 大？

当你实现一个模型得到 error 后，需要诊断：

- **bias 大（underfitting）**：model 无法拟合 training examples（在 training data 上 error 就大）。
- **variance 大（overfitting）**：在 training data 上 error 小，但在 testing data 上 error 大。
知道是 bias 大还是 variance 大，才能选择合适的改进方向。

## 处理偏差大与方差大的方法

### 如果 bias 大（underfitting）

你需要 **redesign your model**，因为当前 model 可能根本没包含 target f̂。做法包括：

- 增加更多特征（例如不只考虑 CP 值，还考虑 HP 值等）。
- 让 model 更复杂（从 1 次式改为 2 次、3 次式等）。
> 注意：此时 **收集更多 data 没有用**，因为 model 本身就不包含 target，再多的 data 也无法让 f* 接近 f̂。*
### 如果 variance 大（overfitting）

1. 增加 data
增加 data 是控制 variance 的有效方法。例如 5 次式，原来每次抓 10 只宝可梦，100 次实验的 f* 非常分散；如果每次抓 100 只，f* 就会非常集中。data 越多，variance 越小。

但实际中可能无法收集更多 data（比如成本、资源限制）。此时可以尝试 **generate 假的 training data**（数据增强）：

- **图像识别**：将图片旋转、翻转（如将左行的火车图片左右颠倒得到右行的火车）。
- **语音识别**：用变声器将男声转为女声，或加入背景噪声模拟真实场景。
- **自然语言处理**：通过翻译扩充数据（如将英文数据硬翻成中文）。
2. Regularization（正则化）

在 loss function 中加入一项，希望参数越小越好，即让曲线更平滑。加了 regularization 后，所有曲线都会集中在平滑区域，从而 **降低 variance**。但同时可能 **伤害 bias**，因为 function space 被限制为平滑曲线，可能不再包含 target。因此需要调整 regularization 的 weight，在 variance 和 bias 之间取得平衡。

## 模型选择与交叉验证

通常我们有多个 model 可以选择（比如不同复杂度、不同 regularization weight），需要在 bias 和 variance 间 trade-off，找到 testing error 最小的 model。

### 不要直接用测试集选模型

**错误做法**：用 training data 分别训练 model 1、2、3，然后直接在 testing set 上比较 error（比如得到 0.9、0.7、0.5），选择 error 最小的 model 3。这样做的后果是：你手上的 testing set 本身有 bias，用它选出的 model 在真正的 testing data（未知）上 error 往往更大。就像 Kaggle 比赛，public leaderboard 的分数好，private leaderboard 可能就掉下来。

### 正确做法：使用验证集（Validation Set）

将 training set 分成两部分：

- **training set**：真正用来训练 model。
- **validation set**：用来选择 model（不参与训练）。
步骤：

1. 用 training set 训练 model 1、2、3。
1. 在 validation set 上评估它们的 performance，选择最好的 model（比如 model 3）。
1. 用全部 training data（training + validation）在选定的 model 3 上再训练一次。
1. 最后用测试集评估。
这样，你在 public set 上的 error 才能真实反映 private set 上的 error。

### 如果担心 validation set 划分不好：N-fold Cross Validation

如果不信任某一次划分，可以做 **N-fold 交叉验证**：

- 将 training set 分成 N 份（例如 3 份）。
- 每次取其中一份作为 validation，其余 N-1 份作为 training。
- 对每个 model，计算 N 次实验的平均 validation error。
- 选择平均 error 最小的 model。
- 最后用全部 training data 训练该 model，再应用到测试集。
> 记住：少根据 public set 的分数调整 model，这样你在 private set 上的结果与 testing set 的差距会更小。
---

**台湾大学人工智能中心**

科技部人工智能技术暨全幅健康照护联合研究中心

http://ai.ntu.edu.tw/
