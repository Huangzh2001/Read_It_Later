---
id: 54e6d9fb-06d1-48e6-bb6b-7e79c8b242c4

url: https://cosx.org/2012/03/causality2-rcm/
---


tags:: 

# 因果推断简介之二：Rubin Causal Model (RCM) 和随机化试验 | 统计之都
#Omnivore

[Read on Omnivore](https://omnivore.app/me/rubin-causal-model-rcm-18f9b5a091e)
[Read Original](https://cosx.org/2012/03/causality2-rcm/)

[![[Omnivore/因果推断简介之二：Rubin Causal Model (RCM) 和随机化试验 - 统计之都/attachments/f8529d35b1270832b23a5e064bef885c_MD5.jpg]]](https://uploads.cosx.org/2012/03/Donald-Rubin.jpg)

因果推断用的最多的模型是 Rubin Causal Model (RCM; Rubin 1978) 和 Causal Diagram (Pearl 1995)。Pearl (2000) 中介绍了这两个模型的等价性，但是就应用来看，RCM 更加精确，而 Causal Diagram 更加直观，后者深受计算机专家们的推崇。这部分主要讲 RCM。

设 Zi 表示个体 i 接受处理与否，处理取 1，对照取 0 (这部分的处理变量都讨论二值的，多值的可以做相应的推广)；Yi 表示个体 i 的结果变量。另外记 {Yi(1),Yi(0)} 表示个体 i 接受处理或者对照的潜在结果 (potential outcome)，那么 Yi(1)−Yi(0) 表示个体 i 接受治疗的个体因果作用。不幸的是，每个个体要么接受处理，要么接受对照 {Yi(1),Yi(0)} 中必然缺失一半，个体的因果作用是不可识别的。观测的结果是 Yi\=ZiYi(1)+(1–Zi)Yi(0)。 但是，在 Z 做随机化的前提下，我们可以识别总体的平均因果作用 (Average Causal Effect; ACE):

ACE(Z→Y)\=E{Yi(1)–Yi(0)}

这是因为

ACE(Z→Y)\=E{Yi(1)}−E{Yi(0)}\=E{Yi(1)∣Zi\=1}−E{Yi(0)∣Zi\=0}\=E{Yi∣Zi\=1}–E{Yi∣Zi\=0}

最后一个等式表明 ACE 可以由观测的数据估计出来。其中第一个等式用到了期望算子的线性性 (非线性的算子导出的因果度量很难被识别！)；第二个式子用到了随机化，即 Z⊥⊥{Y(1),Y(0)} 其中， ⊥ 表示独立性。由此可见，随机化试验对于平均因果作用的识别起着至关重要的作用。

当 Y 是二值的时候，平均因果作用是流行病学中常用的 “风险差”（risk difference; RD）：

CRD(Z→Y)\=P(Y(1)\=1)–P(Y(0)\=1)\=P(Y\=1∣Z\=1)–P(Y\=1∣Z\=0)

当然，流行病学还常用 “风险比”（risk ratio; RR）：

CRR(Z→Y)\=P(Y(1)\=1)P(Y(0)\=1)\=P(Y\=1∣Z\=1)P(Y\=1∣Z\=0)

和 “优势比”（odds ratio; OR）：

COR(Z→Y)\=P(Y(1)\=1)P(Y(0)\=0)P(Y(0)\=1)P(Y(1)\=0)\=P(Y\=1∣Z\=1)P(Y\=0∣Z\=0)P(Y\=1∣Z\=0)P(Y\=0∣Z\=1)

上面的记号都带着 “C”，是为了强调 “causal”。细心的读者会发现，定义 CRR 和 COR 的出发点和 ACE 不太一样。ACE 是通过对个体因果作用求期望得到的，但是 CRR 和 COR 是直接在总体上定义的。这点微妙的区别还引起了不少人的研究兴趣。比如，经济学中的某些问题，受到经济理论的启示，处理的作用可能是非常数的，仅仅研究平均因果作用不能满足实际问题的需要。这时候，计量经济学家提出了 “分位数处理作用”（quantile treatment effect: QTE）：

QTE(τ)\=FY(1)−1(τ)–FY(0)−1(τ)

在随机化下，这个量也是可以识别的。但是，其实这个量并不能回答处理作用异质性（heterogenous treatment effects）的问题，因为处理作用非常数，最好用如下的量刻画：

Δ(δ)\=P(Y(1)–Y(0)≤δ)

这个量刻画的是处理作用的分布。不幸的是，估计 Δ(δ) 需要非常强的假定，通常不具有可行性。

作为结束，留下如下的问题：

1. “可识别性”（identifiability）在统计中是怎么定义的？
2. 医学研究者通常认为，随机对照试验（randomized controlled experiment）是研究处理有效性的黄金标准，原因是什么呢？随机化试验为什么能够消除 Yule-Simpson 悖论？
3. QTE(τ) 在随机化下是可识别的。另外一个和它 “对偶” 的量是 Ju and Geng (2010) 提出的分布因果作用（distributional causal effect: DCE）：DCE(y)\=P(Y(1)≥y)–P(Y(0)≥y) ，在随机化下也可以识别。
4. 即使完全随机化，Δ(δ) 也不可识别。也就是说，经济学家提出的具有 “经济学意义” 的量，很难用观测数据来估计。这种现象在实际中常常发生：关心实际问题的人向统计学家索取的太多，而他们提供的数据又很有限。

关于 RCM 的版权，需要做一些说明。目前可以看到的文献，最早的是 Jerzy Neyman 于 1923 年用波兰语写的博士论文，第一个在试验设计中提出了 “潜在结果”（potential outcome）的概念。后来 Donald Rubin 在观察性研究中重新（独立地）提出了这个概念，并进行了广泛的研究。Donald Rubin 早期的文章并没有引用 Jerzy Neyman 的文章，Jerzy Neyman 的文章也不为人所知。一直到 1990 年，D. M. Dabrowska 和 T. P. Speed 将 Jerzy Neyman 的文章翻译成英文发表在 Statistical Science 上，大家才知道 Jerzy Neyman 早期的重要贡献。今天的文献中，有人称 Neyman-Rubin Model，其实就是潜在结果模型。计量经济学家，如 James Heckman 称，经济学中的 Roy Model 是潜在结果模型的更早提出者。在 Donald Rubin 2004 年的 Fisher Lecture 中，他非常不满地批评计量经济学家，因为 Roy 最早的论文中，全文没有一个数学符号，确实没有明确的提出这个模型。详情请见，Donald Rubin 的 Fisher Lecture，发表在 2005 年的 Journal of the American Statistical Association 上。研究 Causal Diagram 的学者，大多比较认可 Donald Rubin 的贡献。但是 Donald Rubin 却是 Causal Diagram 的坚定反对者，他认为 Causal Diagram 具有误导性，且没有他的模型清楚。他与 James Heckman （诺贝尔经济学奖）， Judea Pearl （图灵奖） 和 James Robins 之间的激烈争论，成为了广为流传的趣闻。

参考文献：

1. Neyman, J. (1923) On the application of probability theory to agricultural experiments. Essay on principles. Section 9\. reprint in Statistical Science. 5, 465-472.
2. Pearl, J. (1995) Causal diagrams for empirical research. Biometrika, 82, 669-688.
3. Pearl, J. (2000) Causality: models, reasoning, and inference. Cambridge University Press。
4. Rubin, D.B. (1978) Bayesian inference for causal effects: The role of randomization. The Annals of Statistics, 6, 34-58.

### 关于作者

| 丁鹏2004-2011 年在北京大学概率统计系学习，获得学士和硕士学位；2011-2015 年在哈佛大学统计系学习，获得博士学位；2015 年在哈佛大学流行病学系做博士后；2016 年起任教于加州大学伯克利分校统计系，2021 年晋升为副教授。研究方向是因果推断。 | ![[Omnivore/因果推断简介之二：Rubin Causal Model (RCM) 和随机化试验 - 统计之都/attachments/43946198d2d7012e1228072fd9842304_MD5.jpg]] |
| ------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

敬告各位友媒，如需转载，请与统计之都小编联系（直接留言或发至邮箱：editor@cos.name），获准转载的请在显著位置注明作者和出处（转载自：统计之都），并在文章结尾处附上统计之都微信二维码。

[![[Omnivore/因果推断简介之二：Rubin Causal Model (RCM) 和随机化试验 - 统计之都/attachments/867ca7c34691fd206768905ca861ca30_MD5.png]]](https://uploads.cosx.org/images/wechat-qrcode.png)

[← 因果推断简介之三：R. A. Fisher 和 J. Neyman 的分歧](https://cosx.org/2012/03/causality3-fisher-and-neyman/ "按左右键可翻页") [因果推断简介之一：从 Yule-Simpson’s Paradox 讲起 →](https://cosx.org/2012/03/causality1-simpson-paradox/ "按左右键可翻页") 

