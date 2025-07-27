---
id: f4a8f15a-2c0f-4f0c-80c4-c75154353eef

url: https://zhuanlan.zhihu.com/p/436281730
status:
---


tags:: 

# 【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/selection-bias-190496f6dff)
[Read Original](https://zhuanlan.zhihu.com/p/436281730)

上一篇文章讲了 Bias 存在的原因并介绍了 Confounding ，Confounding 出现的原因，通常都是因为 treatment 与 outcome 之间存在共因而导致了伪路径的出现，进而导致了伪相关性，这是由于数据本身的生成机制而出现的 Bias 。

而这篇文章介绍的另一种 Bias ，则常常不是来自数据的生成机制，而是由于在收集过程中由于某些原因而出现数据不全的情况，从而只有部分个体的数据被选择作为实验结果，因此这类 Bias 被称为 Selection Bias 。

这一小节主要介绍 Selection Bias 的概念，在因果结构模型中，Selection Bias 是由 treatment 和 outcome 的共果（共同结果）被控制住造成的。

### Selection Bias 的结构

让我们思考这一一个例子，现在我们需要估计，为孕妇在怀孕后不久服用叶酸补充剂 AA （1：是, 0：否）对胎儿在怀孕前两个月发生心脏畸形的风险 YY （1：是, 0：否）的影响。另外，用变量 CC 表示在出生前死亡（1：是, 0：否），心脏畸形 YY 会增加死亡率 CC ，同时服用叶酸补充剂 AA 能减小除心脏畸形外的其他畸形的风险，从而降低死亡率。这一例子用因果图表示如下

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/d84a99c2d2f5f440f61af4db004ffa9a_MD5.png]]

Image

假设不存在未观测的 Bias ，此时，AA 与 YY 之间不存在 Confounding ，因此存在 Exchangeability Ya⊥⊥AY^a\\perp\\!\\!\\!\\!\\perp A ，可以认为关联风险比 Pr\[Y\=1|A\=1\]Pr\[Y\=1|A\=0\]\\frac{Pr\[Y=1|A=1\]}{Pr\[Y=1|A=0\]} 等于因果风险比 Pr\[Ya\=1\=1\]Pr\[Ya\=0\=1\]\\frac{Pr\[Y^{a=1}=1\]}{Pr\[Y^{a=0}=1\]} 。于是，我们可以直接通过计算不同治疗组 outcome 均值的差来计算平均因果效应估计 AA 与 YY 的因果效应，即

E\[Ya\=1\]−E\[Ya\=0\]\=E\[Y|A\=1\]−E\[Y|A\=0\]E\[Y^{a=1}\]-E\[Y^{a=0}\]=E\[Y|A=1\]-E\[Y|A=0\]

但，在生活中，总会存在意外，假设现在由于客观原因无法观测到出生前死亡胎儿的数据，所以研究被限制在存活的胎儿（C\=0C=0​）身上，由此 CC​ 被控制住，由于是 AA​ 与 YY​ 之间的共果， A→C←YA\\rightarrow C\\leftarrow Y​ 的通路被打开，新的 Bias 由此产生。由于 treatment 和 outcome 的共果被控制住，而有部分数据无法被观测（Censoring），这种 Bias 就是 Selection Bias。

由于 Selection Bias 的存在，我们计算得到的关联风险比变为 Pr\[Y\=1|A\=1,C\=0\]Pr\[Y\=1|A\=0,C\=0\]\\frac{Pr\[Y=1|A=1,C=0\]}{Pr\[Y=1|A=0,C=0\]} ，不再等于因果风险比 Pr\[Ya\=1\=1\]Pr\[Ya\=0\=1\]\\frac{Pr\[Y^{a=1}=1\]}{Pr\[Y^{a=0}=1\]}​ ，此时无法由相关性推及因果性。

### Selection Bias 的例子

下面介绍几个 Selection Bias 的例子。

如图 8.2 所示，我们在上一个例子的基础上加入一个 CC 的子结点 SS ，表示父母的悲伤（1：是, 0：否），我们认为胎儿出生时的存活状态 CC 是导致父母是否悲伤的原因，而悲伤的父母会拒绝调查，所以 S\=1S=1 这部分数据缺失，我们只能收集到 S\=0S=0 的数据，这将导致 A→C←YA\\rightarrow C\\leftarrow Y 的路径被打开，从而产生 Bias 。

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/fd342cdbe826aa7356ff604bffc0670f_MD5.png]]

Image

如图 8.3、8.4 所示，即使 AA 与 YY 不存在因果效应，也可能会产生 Selection Bias 。

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/76ac62cccd47373f90af3480fc677119_MD5.png]]

Image

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/cbe661a807c41e309bd47ca661aaa25f_MD5.png]]

Image

## Selection Bias 与 Confounding

我们知道，通常控制组和对照组不满足 Exchangeability 的原因通常有：

* cause 和 treatment 共因的存在（confounding），打开了伪路径；
* cause 和 treatment 共果被控制（selection bias），部分数据未被观测，打开了伪路径；

这一定义描述了两类 Bias 的形成原因以及区别，两者即使在零因果效应的情况下也可能存在。

通常，对于一些研究人员来说，区分 confounding 和 selection bias 是没有实际意义的，所以有些研究员会直接调整 confounding ，而不管是否会导致共果被控制而产生 selection bias。

但事实上，引入 Selection Bias 可以使我们避免可能会产生 selection bias 的 confounding 调整操作，帮助我们更好地设计研究，同时也有助于我们讨论和解释 Confounding 产生的原因。

## Selection Bias 与 censoring

Selection Bias 通常是由 censoring （部分个体由于各种原因而未被纳入统计）造成的，由于 censoring ，只针对特定群体进行实验，而导致存在 Bias 。

如图 8.3 的例子，调查芥末摄入 A\=1A=1 和死亡 Y\=1Y=1 的实验中，摄入芥末 A\=1A=1 和心脏病 L\=1L=1 更容易被踢出调查或丢失数据 C\=1C=1 ，而心脏病的人更容易死亡，从而存在 selection bias ，导致出现 A→YA\\rightarrow Y 的假象。

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/76ac62cccd47373f90af3480fc677119_MD5.png]]

Image

对于这个问题， treatment 和 outcome 的共因 UU 也是原因之一，我们可以通过调节 LL 来阻断后门路径 C←L←U→YC\\leftarrow L\\leftarrow U\\rightarrow Y ，这也是消除 selection bias 的方法之一。

在前面，我们用因果风险比来衡量真实世界和反事实世界的不同

Pr\[Ya\=1\=1\]Pr\[Ya\=0\=1\]\\frac{Pr\[Y^{a=1}=1\]}{Pr\[Y^{a=0}=1\]}

但这一表达不包含 CC ，所以这一结果不等于关联风险比。虽然 CC 对 YY 没有直接的因果效应，但因为 CC 的存在会对 YY 的分布造成影响，所以我们也可以将 CC **当作 treatment 看待**，前面我们假设不存在未观测的 Confounding ，于是我们可以得到另一个关联风险比与因果风险比的等式

Pr\[Ya\=1,c\=0\=1\]Pr\[Ya\=0,c\=0\=1\]\=Pr\[Y\=1|A\=1,C\=0\]Pr\[Y\=1|A\=0,C\=0\]\\frac{Pr\[Y^{a=1,c=0}=1\]}{Pr\[Y^{a=0,c=0}=1\]}=\\frac{Pr\[Y=1|A=1,C=0\]}{Pr\[Y=1|A=0,C=0\]}

通过这一等式可以估计 AA 和 CC 对 YY 的联合因果效应。

CC 被当作 treatment 对待，我们需要确保 exchangeability（可交换性）、positivity（积极性）和 consistency（一致性）的可识别性条件适用于 CC 和 AA 。同时，为了估计 censoring CC 的效应，必须使用与估计 treatment 对 outcome 因果效应的方法。

## Selection Bias 的调整

这一小节简要介绍如何调节 Selection Bias 。

**基于 IPW 的方法**

对于 Selection Bias 的调整，可以采用 IPW（一种基于 Propensity Score 的加权方式）。

通过为每个被选择个体（ C\=0C=0 ）分配一个权重 WCW^C ，从而使得这些被选中的个体不但考虑到其自身的影响，还考虑到与她相同（ AA 与 LL ）的个体。

这种方法本质上是一种对已有样本的扩充和补全，得到一个伪全体样本（ pseudo-population），拥有和全体样本近似的性质。权重 WCW^C 为该个体被选择概率 Pr\[C\=0|L,A\]Pr\[C=0\\,|\\,L,A\] 的倒数。

具体过程《Causal Inference: What If》中的图 8.10 的例子

一个伪全体样本（pseudo-population）要得到与原全体样本相同的效应估计，需要满足以下三个条件：

* **exchangeability** 。被选择个体（ C\=0C=0 ）的平均结果必须等于未观测的（ C\=1C=1 ）、具有相同 AA 和 LL​​ 值的平均结果。换句话说，AA 和 LL 中的变量足够阻断 CC 到 YY​​ 的所有后门路径。
* **positivity** 。IPW 要求，给定 LL 和 AA ，所有被选择的条件概率必须大于 0 ，即 Pr\[C\=0|L,A\]\>0Pr\[C=0\\,|\\,L,A\]>0 。注意这一条件是针对未排除的 C\=0C=0 而不是未观测的 C\=1C=1​ ，我们需要基于被选择的条件概率的倒数来构建一个伪总体。
* **consistency** 。IPW 被用于构造伪全体样本，在其中，所有删减个体（ C\=1C=1 ）被排除，但 treatment 的因果效应与原全体样本的一样，同理 treatment 的因果效应与被删减样本的一样。

**其他方法**

除了 IPW ，分层法也可以用于 selection bias 的消除，如图 8.3

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/76ac62cccd47373f90af3480fc677119_MD5.png]]

Image

只要控制住 LL ，就可以阻断 CC 与 YY 的路径，而这一步可以由分层法来完成。但这要求控制 LL 不会产生 AA 与 YY​ 之间新的开放路径，而如图 8.4

![[Omnivore/【因果系列】Selection Bias：消失的样本带来了麻烦 - 知乎/attachments/cbe661a807c41e309bd47ca661aaa25f_MD5.png]]

Image

若控制 LL ，虽然能阻断 CC 与 YY 之间的后门路径，但也打开了 AA 与 YY 之间的新路径，势必造成估计的偏差。可见，分层法的应用并没有 IPW 那么宽泛。

> 本文使用 [Zhihu On VSCode](https://zhuanlan.zhihu.com/p/106057556) 创作并发布

