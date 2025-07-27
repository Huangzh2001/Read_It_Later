---
id: 739becd3-650a-4074-85f8-1e2395d325d8

url: https://zhuanlan.zhihu.com/p/682079211
status:
---


tags:: 

# 因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/uplift-modeling-with-meta-learning-method-t-learner-s-learner-x--1904a85a7a3)
[Read Original](https://zhuanlan.zhihu.com/p/682079211)

## Uplift Model 概念

顾名思义，uplift 可以理解为增益或者增量，uplift model 即为**增量模型。**其通常用于评估某种干预对个体的状态/行为的因果效应，也就是 **Individual Treatment Effect，即 ITE。**

假设在某个 framework 下有 NN 个个体，个体 ii 在受到某个干预 WiW\_{i} 时的 outcome 是 Yi(1)Y\_{i}(1) ,未受到干预时的 outcome 是 Yi(0)Y\_{i}(0) ，那么对于个体 ii 来说，ITE或者 uplift 就可以表示为 Yi(1)−Yi(0)Y\_{i}(1) - Y\_{i}(0) 。

而通常研究者们更关心的不是某个干预对个体的因果效应，而是去更加全面的估计出某个干预对于社会中不同的人群（i.e.基于不同 XX ）的影响。因此，这里就引出了因果推断中的另一个核心概念：**Conditional Average Treatment Effect，即 CATE。**前面提到的 ITE 可以看作是 CATE的一种特殊情况，即整个样本集合中只有一个元素的场景。CATE 的具体表达式如下

CATE:τ(x)\=E\[Y(1)−Y(0)|X\=x\]CATE : \\tau(x) = E\\left\[ Y(1) - Y(0) | X = x\\right\] 

 uplift modeling 本质上就是通过训练样本去学习不同条件 XX 下某个干预 WW 的平均因果效应，去得到一个 CATE 的 estimator τ\\tau 。然后通过该模型（ τ\\tau ）的泛化能力，就可以对新的个体（ xx）进行干预效果的预测。

## Meta-Learning Method

meta-learning method（元学习方法）就是简单地使用已有的机器学习算法（e.g. 线性回归，树模型，神经网络）来完成 CATE 估计的一系列方法的总称。

但是因为存在**反事实（counterfactual）问题，**即对于每个样本 ii ，我们**无法同时知道**其接受干预情况下的响应值 Yi(1)Y\_{i}(1) 和不接受干预情况下的响应值 Yi(0)Y\_{i}(0) ，因此我们事实上无法得到每个样本 uplift 的真实值，也就意味着我们无法直接基于有监督方法训练一个模型对干预效果进行学习以及预测。所以在基于元学习方法进行 CATE 估计时，我们需要首先对样本进行分组，即随机（保证 XX 与干预 WW 相互独立，即满足 **Conditional Independence Assumption, CIA**）将样本分成 treatment / control 两组并对 treatment 组施加干预，control 组不施加干预后再进行后续的模型训练，具体算法会在后面的部分进行介绍。

下面我们就来逐一介绍下三种经典的元学习方法，它们分别是 T-Learner，S-Learner 以及 X-Learner。

### 1）T-Learner

首先我们来看 T-Learner，这里的 T 代表 Two，就是训练两个子模型的意思。具体来说就是，我们对于 treatment 组的样本和 control 组的样本分别**独立**训练一个响应模型 μ^1(x)\\hat\\mu\_{1}(x) 和 μ^0(x)\\hat\\mu\_{0}(x) 。其中 μ^1(x)\\hat\\mu\_{1}(x) 用于拟合在**施加干预**的情况下响应目标 YY 与特征XX 的关系，即 μ1(x)\=E\[Y|W\=1,X\=x\]\\mu\_{1}(x) = E\\left\[ Y|W=1,X=x \\right\] ；而 μ^0(x)\\hat\\mu\_{0}(x) 用于拟合在**未施加干预**的情况下响应目标 YY 与特征 XX 的关系，即 μ0(x)\=E\[Y|W\=0,X\=x\]\\mu\_{0}(x) = E\\left\[ Y|W=0,X=x \\right\] 。

之后我们拿训练好的两个模型对于同一个样本 xx 的预测结果做差，就得到了我们想要的 uplift 结果。

最终得到的 T-Learner 表达式为 τ^T(x)\=μ^1(x)−μ^0(x)\\hat\\tau\_{T}(x) = \\hat\\mu\_{1}(x) - \\hat\\mu\_{0}(x) 

下面是 T-Learner 算法的示意图（参考 **Causal Inference for The Brave and True** 这本书，因此该图部分 notation 与上文存在差异：图中的 T 对应上文的干预 WW ；图中的 M1 和 M0 对应上文的响应模型 μ^1\\hat\\mu\_{1} 和 μ^0\\hat\\mu\_{0} ）

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/88ee82e99226f0f3a2716e92dd341203_MD5.jpg]]

上面已经对 T-Learner 的思路与整体流程进行了说明，下面我们再来思考下 **a）为什么 T-Learner 可以用来估计 CATE** 以及 **b）它的优缺点分别是什么**。

**a）首先我们来看下为什么 T-Learner 可以用来估计 CATE。**

让我们来回顾下 CATE 的计算公式 CATE:τ(x)\=E\[Y(1)−Y(0)|X\=x\]CATE : \\tau(x) = E\\left\[ Y(1) - Y(0) | X = x\\right\] 

当满足干预 WW 与特征 XX 相互独立，即满足 CIA 时，我们可以将 CATE 公式进一步展开成为如下形式

τ(x)\=E\[Y(1)−Y(0)|X\=x\]\\tau(x) = E\\left\[ Y(1) - Y(0) | X = x\\right\] 

\=E\[Y|W\=1,X\=x\]−E\[Y|W\=0,X\=x\]\= E\\left\[ Y|W=1,X=x \\right\] - E\\left\[ Y|W=0,X=x \\right\] 

\=μ1(x)−μ0(x)\= \\mu\_{1}(x) - \\mu\_{0}(x) 

即 T-Learner 直接基于两组样本分别估计 μ1(x)\\mu\_{1}(x) 和 μ0(x)\\mu\_{0}(x) 来间接实现 τ(x)\\tau(x) 的估计。

**b）然后我们再来思考下 T-Learner 的优缺点。**

该算法的优点是：1\. 原理简单且十分容易理解。2\. 在训练两个响应模型时，可以灵活地使用已有的机器学习方法。3\. 对干预和非干预样本分别建模，充分考虑了干预因素的影响。

但是缺点就是：1\. T-Learner 并不是直接对 uplift 进行建模，因此对 uplift 的识别能力有限。2\. 考虑到其基于两个独立训练的模型进行二次处理后来对 uplift 进行预测，很容易产生两个独立模型的误差累积的问题。

此外在原始论文中还提到在 treatment 组样本量不足而 control 组样本量充足的情况下，为了防止过拟合的产生 μ^1(x)\\hat\\mu\_{1}(x) 的训练只能选择相对简单的算法比如线性回归，但是 μ^0(x)\\hat\\mu\_{0}(x) 却会更复杂。从机器学习的角度出发，这样的选择十分合理。但是从 CATE 估计的角度出发，因为样本原因导致学习程度不同的两个模型做差来进行 CATE 的估计显示是不合理的。作者在论文中举了一个例子来说明这一点

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/0af3d56383b8b253847cc2c82c68e06d_MD5.jpg]]

在上述场景中，真实的 CATE 是一个恒定的值1，但是因为 treatment 组样本过少， μ^1(x)\\hat\\mu\_{1}(x) 无法准确学习到 μ1(x)\\mu\_{1}(x) 的分布规律，而 μ^0(x)\\hat\\mu\_{0}(x) 却通过充足的样本量捕捉到 μ0(x)\\mu\_{0}(x) 的非线性规律。两者学习程度的差异使得在估计 CATE 时会出现巨大的误差。

### 2）S-Learner

接下来我们来看一下另一种元学习方法 S-Learner。这里的 S 代表 Single，意味着只训练一个单一模型用于预测 uplift。不像 T-Learner 那样对 Treatment 和 Control 组的样本单独进行训练，S-Learner 直接将干预 WW 当作是一个额外的特征，并和原始特征 XX 一起放入模型中进行训练。即我们的学习目标是下面这个组合响应函数。

μ(x,w):=E\[Yobs|X\=x,W\=w\]\\mu(x,w) := E\\left\[ Y^{obs}|X=x,W=w \\right\] 

然后在进行预测时，我们固定其余特征 XX ，然后得到模型 μ^\\hat\\mu 在 W\=1W = 1 和 W\=0W = 0 时的预测值的差值即为我们想要的 uplift 值或者说 CATE 估计结果。

即最终的 S-Learner 表达式为 τ^S(x)\=μ^(x,1)−μ^(x,0)\\hat\\tau\_{S}(x) = \\hat\\mu(x,1) - \\hat\\mu(x,0) 

下面是 S-Learner 算法的示意图（同样参考 **Causal Inference for The Brave and True** 这本书，图中 notation 与上文存在差异：图中的 T 对应上文的干预 WW ；图中的 M 对应前面的模型 μ^\\hat\\mu ）

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/00b875e2ec592ae01715e754071759e5_MD5.jpg]]

S-Learner 估计 CATE 的原理和 T-Learner 类似，只是在实现形式只用了单一模型去实现。那么**其优缺点又分别是是什么呢？**

首先该算法的优点有：1\. 原理简单，可以直接基于现有监督学习算法进行模型训练。2\. 充分利用训练数据（不需要像 T-Learner 那样划分数据），保证模型学习效果。3\. 有效避免双模型的误差累积问题。4\. 将干预作为特征直接放入模型可以有效应用在多干预（multiple-treatment）问题上。

但是 S-Learner 也有以下缺点：1\. 本质上还是不是对 uplift 直接进行建模，因此从效果上来说还是有提升空间。2\. **S-Learner 倾向于将干预效果趋近于0，尤其是特征 XX 的维度非常大的时候，模型在训练的过程中极容易忽略这个干预变量。同时模型中正则化的引入，也会带来干预变量的效果稀释，正则化越强，该问题就会越大。**

### **3）X-Learner**

最后我们来看下 X-Learner，这是一种在 T-Learner 基础上进行优化得到的元学习方法。因此相较于 T-Learner 和 S-Learner，其算法流程也更加复杂。这里取名为 X 的原因是该方法会在两个阶段中**交叉**利用两组样本（即 treatment / control 组）来保证每条样本的充分利用，具体我会在后面的部分进行说明。下图截取自论文中对 X-Learner 的介绍。

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/175759f21c0619c718f42ed4a30e1f46_MD5.jpg]]

下面我们来具体看一下 X-Learner 的具体算法流程，其主要可以分为3个阶段。

**阶段一：基于 treatment 样本和 control 样本分别训练响应模型 μ^1(x)\\hat\\mu\_{1}(x) 和 μ^0(x)\\hat\\mu\_{0}(x)** 

这个步骤和 T-Learner 完全一致，即获得在干预条件下和非干预条件下的两个响应模型。

 其中 μ1(x)\=E\[Y|W\=1,X\=x\]\\mu\_{1}(x) = E\\left\[ Y|W=1,X=x \\right\] ； μ0(x)\=E\[Y|W\=0,X\=x\]\\mu\_{0}(x) = E\\left\[ Y|W=0,X=x \\right\] 

**阶段二：使用阶段一获得的两个模型 μ^1(x)\\hat\\mu\_{1}(x) 和 μ^0(x)\\hat\\mu\_{0}(x) 去估计非干预样本和干预样本的干预效果（imputed treatment effect），再将估计的干预效果作为训练目标，对于 treatment 组和 control 组的样本分别训练干预效果预测模型** τ^1(x)\\hat\\tau\_{1}(x) 和 τ^0(x)\\hat\\tau\_{0}(x) **。**

在这个步骤中，我们需要注意模型和样本的**交叉**使用。具体来说就是对于第 ii 个非干预样本 Xi0X\_{i}^{0} ，我们使用干预响应模型 μ^1(x)\\hat\\mu\_{1}(x) 来预测该样本在受到干预时的响应结果 μ^1(Xi0)\\hat\\mu\_{1}(X\_{i}^{0}) ，然后减去未干预响应结果 Yi0Y\_{i}^{0} ，就得到该未干预样本的干预效果（imputed treatment effect）预测值 D\~i0\=μ^1(Xi0)−Yi0\\tilde{D}\_{i}^{0} = \\hat\\mu\_{1}(X\_{i}^{0}) - Y\_{i}^{0} 。同理对于第 ii 个干预样本 Xi1X\_{i}^{1} ，我们使用非干预响应模型 μ^0(x)\\hat\\mu\_{0}(x) 来预测该样本在未受到干预时的响应结果 μ^0(Xi1)\\hat\\mu\_{0}(X\_{i}^{1}) ，然后拿干预响应结果 Yi1Y\_{i}^{1} 去减去该预测值，就得到该干预样本的干预效果预测值 D\~i1\=Yi1−μ^0(Xi1)\\tilde{D}\_{i}^{1} = Y\_{i}^{1} - \\hat\\mu\_{0}(X\_{i}^{1})  。

现在我们已经有了 treatment 组每条样本 n\=1,2,3,...,Ntn= 1,2,3,...,N\_{t} 的干预效果预测值 D\~n1\\tilde{D}\_{n}^{1} 以及原始特征 Xn1X\_{n}^{1} 组成的数据集 ((D\~11,X11),(D\~21,X21),(D\~31,X31),...,(D\~n1,Xn1),...,(D\~Nt1,XNt1))((\\tilde{D}\_{1}^{1} , X\_{1}^{1}),(\\tilde{D}\_{2}^{1} , X\_{2}^{1}),(\\tilde{D}\_{3}^{1} , X\_{3}^{1}),...,(\\tilde{D}\_{n}^{1} , X\_{n}^{1}),...,(\\tilde{D}\_{N\_{t}}^{1} , X\_{N\_{t}}^{1})) 以及 control 组每条样本 n\=1,2,3,...,Ncn= 1,2,3,...,N\_{c} 的干预效果预测值 D\~n0\\tilde{D}\_{n}^{0} 以及原始特征 Xn0X\_{n}^{0} 组成的数据集 ((D\~10,X10),(D\~20,X20),(D\~30,X30),...,(D\~n0,Xn0),...,(D\~Nc0,XNc0))((\\tilde{D}\_{1}^{0} , X\_{1}^{0}),(\\tilde{D}\_{2}^{0} , X\_{2}^{0}),(\\tilde{D}\_{3}^{0} , X\_{3}^{0}),...,(\\tilde{D}\_{n}^{0} , X\_{n}^{0}),...,(\\tilde{D}\_{N\_{c}}^{0} , X\_{N\_{c}}^{0})) 。接下来就是基于这两个数据集再次训练两个干预效果预测模型 τ^1(x)\\hat\\tau\_{1}(x) 和 τ^0(x)\\hat\\tau\_{0}(x) 。

其中学习目标 τ1(x)\=E\[D\~1|X1\=x\]\\tau\_{1}(x) = E\\left\[ \\tilde{D}^{1} | X^{1} = x\\right\] ， τ0(x)\=E\[D\~0|X0\=x\]\\tau\_{0}(x) = E\\left\[ \\tilde{D}^{0} | X^{0} = x\\right\] 。

**阶段三：通过对阶段二获得的两个干预效果预测模型 τ^1(x)\\hat\\tau\_{1}(x) 和 τ^0(x)\\hat\\tau\_{0}(x) 进行加权融合即可得到最终的 CATE estimator。**

该融合步骤可以表示为如下

τ^(x)\=g(x)τ^0(x)+(1−g(x))τ^1(x)\\hat\\tau(x) = g(x)\\hat\\tau\_{0}(x) + (1-g(x))\\hat\\tau\_{1}(x) ，其中 g∈\[0,1\]g \\in \[0,1\] 即为权重函数。

该步骤中最核心的即为权重的选择。作者在论文中提到一种好的权重 g(x)g(x) 选择是**倾向性得分（propensity score）** e^(x)\\hat{e}(x) 。这里解释一下倾向性得分的概念：倾向性得分（propensity score）代表给定样本的 XX ,该样本被干预的概率，即 P(W\=1|X)P(W=1|X) 。

当然作者也提到如果 treatment 组样本的样本量非常大或者非常少，也可以直接将 gg 赋值为1或者0。

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/3a6b776d95c15eaf0f3f829b5f4d66d1_MD5.jpg]]

下面是 X-Learner 算法的示意图（同样参考 **Causal Inference for The Brave and True** 这本书，图中 notation 与上文存在差异：图中的 T 对应上文的干预 WW ；图中的 M0 和 M1 对应前面的模型 μ^0\\hat\\mu\_{0} 和 μ^1\\hat\\mu\_{1} ；图中的 MTAU0 和 MTAU1 对应前面的模型 τ^0\\hat\\tau\_{0} 和 τ^1\\hat\\tau\_{1} ）

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/72ef869b5d37f8ed1823c00a590ceaf5_MD5.jpg]]

在介绍 T-Learner 的时候，我们有提到 treatment 组和 control 组样本量差异会导致基于 T-Learner 训练的 uplift model 预测 CATE 时会产生很大的误差，比如 treatment 组样本量少会导致 T-Learner 学到的第一个响应模型 μ^1(x)\\hat\\mu\_{1}(x) 无法精确捕捉一些非线性关系。

对于 X-Learner 来说，在第二个阶段，其会利用第一阶段的两个响应模型 μ^1(x)\\hat\\mu\_{1}(x) 和 μ^0(x)\\hat\\mu\_{0}(x) 去分别得到非干预样本和干预样本的 imputed treatment effect 做为第二阶段模型训练的目标去得到 τ^0(x)\\hat\\tau\_{0}(x) 和 τ^1(x)\\hat\\tau\_{1}(x) 。假设还是基于前面的 treatment 组样本量很少多的场景，那么基于‘错误模型‘ μ^1(x)\\hat\\mu\_{1}(x) 得到的二阶段模型 τ^0(x)\\hat\\tau\_{0}(x) 也会是错误的，而将充分学习得到的模型 μ^0(x)\\hat\\mu\_{0}(x) 作为基础得到的二阶段模型 τ^1(x)\\hat\\tau\_{1}(x) 也会更加准确。即下图所示的那样

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/88391c82b46403ff3d53b92ed57a64f9_MD5.jpg]]

在模型融合阶段，当我们使用倾向性得分 e^(x)\\hat{e}(x) 作为权重时，干预样本量少意味着 e^(x)\\hat{e}(x) 也会十分接近于0，那么‘错误模型’ τ^0(x)\\hat\\tau\_{0}(x) 的权重自然就会很低，而准确的模型 τ^1(x)\\hat\\tau\_{1}(x) 会被赋予很高的权重。因此最终的 CATE estimator 会正确地倾向于更大样本训练得到的模型。下图展示了 T-Learner 和 X-Learner 的效果对比。

![[Omnivore/因果推断笔记(一) - Uplift Modeling with Meta-Learning Method（T-Learner/S-Learner/X-Learner) - 知乎/attachments/9c00a058a626a493fd3b952fa7af4530_MD5.jpg]]

与T-Learner 相比，X-Learner 在非线性的 CATE 估计校正上做得更好。一般来说，当 treatment 组和 control 组数据量相差很大时，X-Learner 表现得更好。当然必须承认的是 X-Learner 流程还是相对比较复杂，计算成本较高，还存在多模型误差累积等问题。

## 总结

在这篇文章中，我们介绍了 uplift model 的基本概念以及在 uplift modeling 中经典的元学习方法，具体包括 T-Learner，S-Learner 以及 X-Learner 三种算法。这几种方法（不包括 S-Learner）主要应用于 binary 或者 categorical 的干预场景。在后面的元学习方法相关文章中，我还会继续介绍一种可以应用于连续型干预场景的方法 R-Learner 以及一种特殊的元学习方法 The Class Transformation Method 。

## 参考

[Causal Inference and Uplift Modelling: A Review of the Literature](https://link.zhihu.com/?target=https%3A//proceedings.mlr.press/v67/gutierrez17a.html)

[Meta-learners for Estimating Heterogeneous Treatment Effects using Machine Learning](https://link.zhihu.com/?target=https%3A//arxiv.org/pdf/1706.03461.pdf)

[Causal Inference for The Brave and True](https://link.zhihu.com/?target=https%3A//matheusfacure.github.io/python-causality-handbook/21-Meta-Learners.html)

[【实践案例分享】阿里文娱智能营销增益模型 ( Uplift Model ) 技术实践-腾讯云开发者社区-腾讯云](https://link.zhihu.com/?target=https%3A//cloud.tencent.com/developer/article/1620903) 

