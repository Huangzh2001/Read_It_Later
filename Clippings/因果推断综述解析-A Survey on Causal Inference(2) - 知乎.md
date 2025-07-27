---
id: 7d5e142e-55db-4612-95c1-36d8728f9c97
created: 星期二, 六月 18日 2024, 9:54:12 晚上
updated: 星期五, 三月 7日 2025, 3:11:51 下午

url: https://zhuanlan.zhihu.com/p/363894736
---

# 因果推断综述解析|A Survey on Causal Inference(2) - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e)
[Read Original](https://zhuanlan.zhihu.com/p/363894736)

## Highlights

> 因果推断的任务是评估实施某种策略对我们关心的结果指标的影响。举例来说，对于一种疾病有两种治疗方案A和B，对于既定的患者群，治疗方案A的康复率是70%，治疗方案B的康复率是90%。那么，两种治疗方案的康复率的差值就是因果推断关心的指标。
> 上述的情况是理想的情况，我们可以获得同一患者群在治疗方案A和B的康复率。实际上，我们只能观测到一种情况。为了近似这种理想情景，我们只能使用随机试验；在治疗方案完全随机分配每一个患者时，我们可以近似的认为获取不同治疗方案的群体是一致的。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#493bfd13-0723-4e14-8374-4d8be0747123)  ^493bfd13

> 我们不知道每个个体与被分配的策略之间是否存在这特定的关系，即不知道是否某些特定属性的个体被分配了特定的策略。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#93c10d6b-0f86-4658-8425-9f0ed96e596c)  ^93c10d6b

> 作者首先就介绍了上述的三个基本概念：unit, treatment, and outcome。
> Unit：基本分析对象，可以是一个公司，一个患者，一个个人等等，ZZ习惯称呼为其样本。
> Treatment：对分析对象Unit可执行的策略，例如某个患者可以采用的治疗方案A和B，A和B都是策略。用 
> W
> (
> W
> ∈
> {
> 0
> ,
> 1
> ,
> 2
> ,
> ⋯
> ,
> N
> W
> }
> )W\left(W\in\left\{ 0,1,2, \cdots,N_{W}\right\}\right) 来表示策略，其中 
> N
> W
> +
> 1N_{W} + 1 表示策略的总数。对于二分类问题， 
> W
> =
> 1W=1 代表试验组， 
> W
> =
> 0W=0 代表对照组。
> Outcome：顾名思义，试验结果，但是在潜在因果框架下，我们需要细分一下不同的outcome。
> Potential outcome：潜在结果，对于任何一个样本，任何一个策略都存在一个潜在结果， 
> ww 策略下的潜在结果表示为： 
> Y
> (
> W
> =
> w
> )Y(W=w) 。
> Observed outcome：观测结果，即可观测到的结果，也称为真实结果，是潜在结果的一种实际表现。使用 
> Y
> FY^{F} 来表示观测结果，如果一个样本被实施了策略 
> ww ，那么它的的观测结果表示为： 
> Y
> F
> =
> Y
> (
> W
> =
> w
> )Y^{F}=Y(W=w) 。
> Counterfactual outcome：反事实结果，对于一个样本来说，除了它真正被实施的策略以外，所有其他策略的潜在结果都是反事情结果；反事实结果也是潜在结果的一种，可以简单理解为潜在结果=可观测结果+反事实结果。同样的，如果一个样本被实施了策略 
> ww ，那么它的的反事实结果表示为： 
> Y
> C
> F
> =
> Y
> (
> W
> =
> w
> ′
> )Y^{CF}=Y(W=w^{'}) ，其中 
> w
> ′
> ≠
> ww^{'}\ne w 。如果只有两个策略，那么反事情结果： 
> Y
> C
> F
> =
> Y
> (
> W
> =
> 1
> −
> w
> )Y^{CF}=Y(W=1-w) 。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#4e6384f2-3cf6-4526-89d6-7e18fb32af53)  ^4e6384f2

> pre-treatment variables：不受策略所影响的特征成为策略前特征，这个比较好理解，比如人的年龄，性别等等；也称为环境变量；
> post-treatment variables：与策略前特征相对应，策略后特征就是受策略影响的特征变量，举个例子就是患者服药之后的身体理化特征。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#2c6a624a-dfc7-44a3-9cb0-618e84a98b33)  ^2c6a624a

> 不同策略结果的差异，即策略效果Treatment Effect 。
> Treatment Effect：策略效果可以根据以上的概念计算，作者将策略效果分为了四个层次：
> 整体层次，策略效果称作平均策略效果（Average Treatment Effect (ATE)）：
> 其中， 
> Y
> (
> W
> =
> 1
> )Y(W=1) 和
> Y
> (
> W
> =
> 0
> )Y(W=0)分别代表整个群体的策略潜在结果和对照潜在结果。注意：这里不是我们AB实验中实验组与对照组的差值，而是整体群体，每一个个体都有两种潜在结果，进行相减求期望。
> 某策略组层次，策略效果称作策略组的平均策略效果（Average Treatment effect on the Treated group (ATT)）：
> 其中，
> Y
> (
> W
> =
> 1
> )
> |
> W
> =
> 1Y(W=1)|W=1 和
> Y
> (
> W
> =
> 0
> )
> |
> W
> =
> 1Y(W=0)|W=1分别代表在策略组样本上的（ 
> Y
> (
> ∗
> )
> |
> W
> =
> 1Y(*)|W=1 ）的策略潜在结果和对照潜在结果。这里 
> Y
> (
> W
> =
> 1
> )
> |
> W
> =
> 1Y(W=1)|W=1 是可观测结果。
> 某子群层次，即整体的某一个子集上的策略效果，称为条件平均效果（Conditional Average Treatment Effect (CATE)）：
> 其代表含义即在特定条件下（ 
> X
> =
> xX=x ）的集合的策略效果，有时也称为分层实验效果。
> 个体层次，称为个体策略效果（Individual Treatment Effect (ITE)），对于第 
> ii 个个体，其表示为： [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#c5da3b52-3d69-4a07-889d-ac98b459d16c)  ^c5da3b52

> 我们一旦可以评估个体水平的策略效果，那么任何层次的效果都可以看作是某些个体效果的加权平均值(期望值)而已。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#fabeb1de-246d-4324-813e-bb1aa7013884)  ^fabeb1de

> 重新定义了一些因果推断的目标：
> 给定数据集： 
> {
> X
> i
> ,
> W
> i
> ,
> Y
> i
> F
> }
> i
> =
> 1
> N\left\{ X_{i},W_{i},Y_{i}^{F} \right\}_{i=1}^{N} ， 
> NN 是样本数量；因果推断的目标是计算 
> A
> T
> E
> 、
> A
> T
> T
> 、
> C
> A
> T
> E
> 、
> I
> T
> EATE、ATT、CATE、ITE 。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#f08d9fed-1729-4d93-b216-bbcf9eba6cc9)  ^f08d9fed

> 另外，可忽略性和正向假设统称为强可忽略或者强可忽略策略分配假设。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#0dd993f2-7d1c-4df1-bd49-4ae0413788ef)  ^0dd993f2

> 在以上三个假设的前提下，我们推导出可观测结果与潜在结果的关系：
> 这个很容易理解，就是在以上三个假设之下，某策略下观测到的结果就是该策略的潜在结果。即以上三个条件保证观测结果与实际的潜在结果是无偏的。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#fdfbdcca-0410-47a7-861a-5c3434499c1a)  ^fdfbdcca

> 同时根据上面给出可观测结果与潜在结果的关系，我们重写
> A
> T
> E
> 、
> A
> T
> T
> 、
> C
> A
> T
> E
> 、
> I
> T
> EATE、ATT、CATE、ITE 指标如下：
> 公式看着很多，很长，但是小伙伴们不要被劝退，我们来解析一下：
> 公式(7)中我们可以发现，虽然
> A
> T
> E
> 、
> A
> T
> T
> 、
> C
> A
> T
> E
> 、
> I
> T
> EATE、ATT、CATE、ITE 都有，但是核心只有 
> I
> T
> EITE 一个指标，其他指标都是由 
> I
> T
> EITE 转化出来，所以我们一起来推导一下公式(7)中的 
> I
> T
> EITE 即可，首先我们把原始
> I
> T
> EITE公式和重写之后一起贴在下面：
> 首先我们知道，对于某个体 
> ii ，其真实分配的策略 
> W
> iW_{i} 只有一种情况，在只有两个策略的情况下(作者都是以两个策略为例给出的基本公式，后面不再强调)， 
> W
> i
> =
> 1W_{i}=1  或者 
> W
> i
> =
> 0W_{i}=0 ，那么对于
> W
> i
> =
> 1W_{i}=1 的情况：
> I
> T
> E
> i
> =
> Y
> i
> (
> W
> =
> 1
> )
> −
> Y
> i
> (
> W
> =
> 0
> )
> =
> Y
> i
> F
> −
> Y
> i
> C
> FITE_{i}=Y_{i}(W=1)-Y_{i}(W=0)=Y_{i}^{F}-Y_{i}^{CF}
> 那么对于
> W
> i
> =
> 0W_{i}=0的情况：
> I
> T
> E
> i
> =
> Y
> i
> (
> W
> =
> 1
> )
> −
> Y
> i
> (
> W
> =
> 0
> )
> =
> Y
> i
> C
> F
> −
> Y
> i
> FITE_{i}=Y_{i}(W=1)-Y_{i}(W=0)=Y_{i}^{CF}-Y_{i}^{F}
> 那么将两种情况合并在一起就是，无论
> W
> i
> =
> 1W_{i}=1  或者 
> W
> i
> =
> 0W_{i}=0：
> I
> T
> E
> i
> =
> W
> i
> Y
> i
> F
> −
> W
> i
> Y
> i
> C
> F
> +
> (
> 1
> −
> W
> i
> )
> Y
> i
> C
> F
> −
> (
> 1
> −
> W
> i
> )
> Y
> i
> FITE_{i}=W_{i}Y_{i}^{F}-W_{i}Y_{i}^{CF}+(1-W_{i})Y_{i}^{CF}-(1-W_{i})Y_{i}^{F}
> 那么公式(7)就推导完毕，很简单很常规的一个合并公式。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#cf5c7ee5-2a91-44d2-aef6-c67077a33ba6)  ^cf5c7ee5

> 那么介绍到这里，事情逐渐明了，在三个假设下，我们只需要使用公式(7)就能搞定需求了。那么对于公式(7)，我们只需要搞定 
> I
> T
> EITE 就行了。那么对于 
> I
> T
> EITE 中 
> W
> iW_{i} 和 
> Y
> i
> FY_{i}^{F} 我们都是可知的，只需要搞定 
> Y
> i
> C
> FY_{i}^{CF} 一个指标就齐活了，问题都简化到这种程度了。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#b6d3221d-3bbf-47b9-9eac-b191fcd2949c)  ^b6d3221d

> 接上面进展，对于 
> Y
> i
> C
> FY_{i}^{CF} 我们有一种最好用的估计方式，就是找到和第 
> ii 个样本的一样背景变量的样本 
> jj ，并且样本 
> ii 和样本 
> jj 的策略不一样，那么就有 
> Y
> i
> C
> F
> =
> Y
> j
> FY_{i}^{CF} = Y_{j}^{F}  ，就解决了这个问题。
> 有了上面ZZ的过度，就比较容易理解原文作者所说，衡量 
> A
> T
> EATE 时，在三个前提都满足的情况下，再利用上面ZZ解析说的估计思路时，直接用试验组的效果均值减对照组的效果均值就得到了ATE的估计值： [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#59f3660c-d301-4817-a718-016fe75f991f)  ^59f3660c

> 对于混杂带来的第一种现象辛普森悖论，一般的处理方法好多知乎应该知道，就是计算分层加权平均
> A
> T
> EATE ：
> 因为一旦直接估计出反事实
> Y
> i
> C
> FY_{i}^{CF}后，一切的问题都迎刃而解，所以接下来的因果推断主要围绕着这个方向展开。我们回到根源，想估计反事实
> Y
> i
> C
> FY_{i}^{CF}时，混杂带来的第二种现象：选择性偏差问题，我们一般有两类方法来解决。
> 1、生成近似无偏差的样本空间，有样本权重更新，基于匹配的方法，基于树的方法，混杂平衡方法，平衡表示学习方法和基于多任务学习的方法。
> 2、首先根据观测数据生成基本模型，然后对选择偏差造成的有偏估计进行矫正。代表方法是元学习。 [⤴️](https://omnivore.app/me/a-survey-on-causal-inference-2-1902b98080e#78853629-606f-4d00-b212-f71f06cf7e1a)  ^78853629

