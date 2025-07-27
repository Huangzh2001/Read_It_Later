---
id: 0e4c279f-ca5c-4bbe-b95a-75588c976abf

url: https://zhuanlan.zhihu.com/p/679988388
---


tags:: 

# 因果推断的效应：ATE、ATT、ITT、LATE - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/ate-att-itt-late-19038939f89)
[Read Original](https://zhuanlan.zhihu.com/p/679988388)

最近《世界经济》期刊线上活动讲座上，刘若鸿老师介绍了他的论文《工业用地价格与企业产能利用率》[\[1\]](#ref%5F1)。分析框架借鉴了陈钊老师等人（2021）发在AER上的论文《Notching R&D investment with corporate income tax cuts in China》[\[2\]](#ref%5F2)——使用聚束（bunching）方法研究经济现象。

> 《世界经济》官网已经可以下载论文代码数据量。手把手活动系列视频也可以在B站找到录播。听论文作者讲诉自己在选题、文献阅读、方法选择、修改稿件的心路历程，确实受益匪浅！

![[Omnivore/因果推断的效应：ATE、ATT、ITT、LATE - 知乎/attachments/b0bc91eaf1482721914204dc28bed531_MD5.jpg]]

左刘若鸿老师论文截图，右陈钊老师论文截图。有点类似RDD，但是因为这类政策样本不满足随机干预，是一种政策集聚现象，所以采用群聚分析

刘若鸿老师提到学习这部分代码时最好了解下因果推断识别效应。附件的do文件也取名ITT。我发现我竟然对“因果推断方法识别效应”这部分知识印象不深，因此在这里记录下学习过程。

![[Omnivore/因果推断的效应：ATE、ATT、ITT、LATE - 知乎/attachments/0a318be850a018a7ba415880ccd8007d_MD5.jpg]]

图片来自直播时刘若鸿老师PPT（世界经济手把手第二期）

## 一、因果框架有哪些？

今因果框架众多，群雄并起，统计学（本家之外，药物学、心理学也各有自家统计理解）、经济学、计算机皆有流派，交错纵横，我也不清楚整个体系到底如何。

个人接触比较多的是Judea Pearl的**结构因果模型**（Structural Causal Model,简称SCM）。对于他的著作《为什么》[\[3\]](#ref%5F3)，我个人理解是，关联-干预-反事实就是三个因果层级。控制变量的选用就是控制后门，工具变量的设置就是控制前门。

![[Omnivore/因果推断的效应：ATE、ATT、ITT、LATE - 知乎/attachments/10da98bd3a1480673fe7774cb53011f0_MD5.jpg]]

相关不等于因果，相关性并不讨论方向。因果性是单向的，因此我们要有单向路径图指导。寻找路径后，再通过分析想像出“反事实”的世界。

ATE、ATT、ITT、LATE这部分知识在《基本无害的计量经济学》[\[4\]](#ref%5F4)中零散出现。整个框架是基于Donald Rubin提出的**潜在结果框架**(Potential Outcome Framework[\[5\]](#ref%5F5)，也叫Rubin Causal Model，简称RCM)**。**

> 有趣的是，Judea Pearl（在《为什么》中）提出因果路径下的反事实就是Rubin提出的"潜在结果"，不过Rubin回应两者完全不是一回事，并且不赞成路径图的分析方法[\[6\]](#ref%5F6)。  
> （个人不太能理解rubin的回应，在我个人看来SCM的路径箭头方向对应的就是RCM的加减符号方向）。

据我所知，目前因果分析在统计学中还分为频率学派、贝叶斯学派，研究通过马尔科夫链去理解因果推断。这方面个人就完全知之甚少了。个人对这块知识的了解完全来自于B站up——Fmajor的科普视频。

## 二、细说RCM因果效应

> ATE、ATT、ITT、LATE是不同的统计估计量。

### 1、从ATE到ATT

从小学开始，我们就接触了使用各个数组的均值来进行比较分析。不过这种分组对比只是因果讨论的起点，需要进一步对这种分组差异进行分解，进而探讨因果关系。

\\boxed{平均处理效应} （average treatment effect，简称ATE）：**直接用两组数据均值之差**作为估计量。既可以看作总体均值相减，又可以看作分组相减的均值（例如双胞胎数据估计）：

\\bar Y\_1-\\bar Y\_0=\\sum\_{i=1}^{N}\\frac{Y\_{i}(1)-Y\_{i}(0)}{N}\\\\将 D\_i 视为处理行为。 DiD\_i 为1为实验组，为0为对照组。产生线性方程如下：

\\begin{aligned} \\mathbf{Y}\_{i}& \\left.=\\left\\{\\begin{matrix}{Y\_{1i}}&{\\mathrm{if}D\_{i}=1}\\\\{Y\_{0i}}&{\\mathrm{if}D\_{i}=0}\\\\\\end{matrix}\\right.\\right. \\\\ &=Y\_{0i}+(Y\_{1i}-Y\_{0i})D\_{i} \\end{aligned}\\\\

 分组相减，可得如下式子（注意红色部分）：\\begin{aligned} &\\mathbf{E}\[Y\_{i}\\mid D\_{i}=1\]-\\mathbf{E}\[Y\_{i}\\mid D\_{i}=0\]\\\\& =\\color{red}{\\underbrace{\\mathbf{E}\\lfloor Y\_{1i}\\mid D\_{i}=1\\rfloor-\\mathbf{E}\[Y\_{0i}\\mid D\_{i}=1\]}\_{\\text{处理的平均处理效应ATT}} }\\\\ &+\\underbrace{\\operatorname{E}\[Y\_{0i}\\mid D\_{i}=1\]-\\operatorname{E}\[Y\_{0i}\\mid D\_{i}=0\]}\_{\\operatorname\*{\\text{选择性偏误}}} \\end{aligned}\\\\

 其中 E\[Y0i∣Di\=1\]\\mathbf{E}\[Y\_{0i}\\mid D\_{i}=1\] 是我们主动添加的，是想要却无法直接找到的另一个”平行宇宙“——**假如**E\[Y1i∣Di\=1\]\\mathbf{E}\[Y\_{\\color{blue}{1i}}\\mid D\_{i}=1\] 部分群体，在平行世界没有没有接受处理，他们的状态表示为 E\[Y0i∣Di\=1\]\\mathbf{E}\[Y\_{\\color{blue}{0i}}\\mid D\_{i}=1\] ，也就是Rubin想找到的"潜在结果"。

\\color{red}{\\mathbf{E}\\lfloor Y\_{1i}\\mid D\_{i}=1\\rfloor-\\mathbf{E}\[Y\_{0i}\\mid D\_{i}=1\]} 代表着 \\boxed{处理组平均处理效应} （Average Treatment Effect on Treated，简称ATT）。

同理， E⁡\[Y0i∣Di\=1\]−E⁡\[Y0i∣Di\=0\]\\operatorname{E}\[Y\_{0i}\\mid D\_{i}=1\]-\\operatorname{E}\[Y\_{0i}\\mid D\_{i}=0\] 代表 \\boxed{实验组平均处理效应} （Average Treatment Effect on Untreated，简称ATU）。采用同样的构造，构造出新的平行宇宙情况

E\[Yi∣Di\=1\]−E\[Yi∣Di\=0\]\=E⌊Y1i∣Di\=0⌋−E\[Y0i∣Di\=0\]⏟对照组的平均处理效应ATU+E\[Y1i∣Di\=1\]−E\[Y1i∣Di\=0\]⏟选择性偏误

\\begin{aligned} &\\mathbf{E}\[Y\_{i}\\mid D\_{i}=1\]-\\mathbf{E}\[Y\_{i}\\mid D\_{i}=0\]\\\\ & ={\\underbrace{\\mathbf{E}\\lfloor Y\_{1i}\\mid D\_{i}=0\\rfloor-\\mathbf{E}\[Y\_{0i}\\mid D\_{i}=0\]}\_{\\text{对照组的平均处理效应ATU}} }\\\\ &+\\underbrace{\\operatorname{E}\[Y\_{1i}\\mid D\_{i}=1\]-\\operatorname{E}\[Y\_{1i}\\mid D\_{i}=0\]}\_{\\operatorname\*{\\text{选择性偏误}}} \\end{aligned}\\\\ 再没有比“**一个二项选择分裂出两个平行宇宙”**更好的对照试验了，然而没有人能真正获得这种数据！因此，经济学家的做法是想通过ATE来估计ATT，于是引入了随机试验（RCT）。 

### 2、RCT：让ATE趋近ATT。

RCT全称为Randomized controlled trial，代表 \\boxed{随机试验} ，**在随机试验条件下，ATE=ATT**，接下来展开介绍：

平行世界分裂出的这部分群体 \\mathbf{E}\[Y\_{0i}\\mid D\_{i}=1\] 和现实一开始就没有接受过处理的群体 \\operatorname{E}\[Y\_{0i}\\mid D\_{i}=0\] 相减，如果不为0，就产生了选择性偏差。

> 原因可能是**样本选择偏差**：例如我们做健身相关的调查，但只去健身馆收集数据，肯定不能实现有效对比；例如美军著名的飞机幸存者偏差，飞回来的飞机是活下来的飞机，通过他们身上的损伤估计需要加强的部位也是不可靠的；  
> 也可能是**自选择偏差**：例如入学性别比不均不代表歧视，因为这种分析忽略了性别比的申请倾向，某种性别的人更倾向于申请难度更高的，淘汰率也就更高；警察执法更关注某个种族也不代表就是歧视，看看那个种族犯罪频率是不是相对就高一些。  
> **遗漏变量、模型错误、测量错误、样本不足**都可能导致。

**如果我们采用随机试验的方法，样本是随机分布的**。我们希望这种随机试验能把一些我们没观察到的影响变量给平均掉，进而使得 D\_i 和 Y\_{0i} 具有独立性，这意味着 \\mathbf{E}\[Y\_{0i}\\mid D\_{i}=1\]=\\mathbf{E}\[Y\_{0i}\\mid D\_{i}=0\]=\\mathbf{E}\[Y\_{0i}\] 。

此时ATE估计得到了有效的简化：

\\begin{aligned} &\\mathbf{E}\[Y\_{1i}\\mid D\_{i}=1\]-\\mathbf{E}\[Y\_{0i}\\mid D\_{i}=1\]\\\\&=ATT =\\mathbf{E}\[\\mathbf{Y}\_{1i}-\\mathbf{Y}\_{0i}\\mid D\_{i}=1\] \\\\ &=ATE=\\mathbf{E}\[Y\_{1i}-Y\_{0i}\] \\end{aligned}\\\\ 进一步通过**回归式子**来估计：

\\begin{aligned} \\mathbf{Y}\_{i}& \\left.=\\left\\{\\begin{matrix}{Y\_{1i}}&{\\mathrm{if}D\_{i}=1}\\\\{Y\_{0i}}&{\\mathrm{if}D\_{i}=0}\\\\\\end{matrix}\\right.\\right. \\\\ &=Y\_{0i}+(Y\_{1i}-Y\_{0i})D\_{i} \\\\ &=\\alpha+\\rho D\_i+\\eta\_i \\end{aligned}\\\\

由于 \\begin{aligned}&\\operatorname{\\mathbf{E}}\[Y\_i\\mid D\_i=1\]=\\alpha+\\rho+\\operatorname{\\mathbf{E}}\[\\eta\_i\\mid D\_i=1\]\\\\&\\operatorname{\\mathbf{E}}\[Y\_i\\mid D\_i=0\]=\\alpha+\\operatorname{\\mathbf{E}}\[\\eta\_i\\mid D\_i=0\]\\end{aligned}\\\\ 可以得到两者相减\\begin{aligned}&\\operatorname{\\mathbf{E}}\[Y\_i\\mid D\_i=1\]-\\operatorname{\\mathbf{E}}\[Y\_i\\mid D\_i=0\]\\\\&=\\underbrace{\\rho}\_\\text{处理效应}+\\underbrace{\\operatorname{\\mathbf{E}}\[\\eta\_i\\mid D\_i=1\]-\\operatorname{\\mathbf{E}}\[\\eta\_i\\mid D\_i=0\]}\_\\text{选择性偏误}\\end{aligned}\\\\ 选择偏差 \\eta\_i\\ne0 时，意味着残差和 D\_i 相关。  我们强调随机试验，就是希望随机干预试验能够使得二者无关，消除这种选择偏差。所以当满足随机试验时，\\eta\_i=0， ATE\\xrightarrow{RCT}ATT 。

> 这也告诉了我们为什么要重视残差分析。

### 3、从ITT到LATE

\\boxed{意向性分析} （Intention to treat，简称ITT）。虽然随机干预试验很有用，但我们要研究的变量不总是随机分布的。例如刘若鸿老师的《工业用地价格与企业产能利用率》——研究工业用地集聚在某一档土地等级周围。此时买家们不讲武德，是有备而来，也就不是随机分布的。此时我们考虑其他随机分布的变量会影响他们的决策。

先使用SCM的路径图来理解会更加形象：

![[Omnivore/因果推断的效应：ATE、ATT、ITT、LATE - 知乎/attachments/aa6ee83eeebe47438b7f2ffaea25c8f1_MD5.jpg]]

图源：《因果推断实用计量方法 》(邱嘉平)我们想研究的变量D并不随机，于是我们找到了一个随机变量Z，同时Z和D之间具有因果关系。

再举例Angrist（2011）的一篇论文，研究参加越南战争对收入的影响[\[7\]](#ref%5F7)，里面参军变量不好使，就使用了入伍资格作为工具变量。（怀念短短6页的计量论文时代）

![[Omnivore/因果推断的效应：ATE、ATT、ITT、LATE - 知乎/attachments/a36946cb0523c6d45bf8a36fdc7317e3_MD5.jpg]]

论文其实就是用了2SLS

显然，存在这样一个过程，一个人先被告知有没有入伍资格，然后他决定是否进入军队。

ITT式子如下所示：ITT=\\mathbf{E}\[Y\_i|Z\_i=1\]-\\mathbf{E}\[Y\_i|Z\_i=0\]\\\\ 可以看出ITT估计和 \\mathbf{E}\[Y\_{i}\\mid D\_{i}=1\]-\\mathbf{E}\[Y\_{i}\\mid D\_{i}=0\] 相当类似，也就是说，**当** Z\_i **和** D\_i 一一对应时**，**也就是 z=d 时，**ITT=ATE**。

但是为什么要进行区分？因为很多时候，Z\_i **和**D\_i并不一一对应。于是分成了**四类博弈决策**：

此时 Z\_i 依旧是随机分布，但 Z\_i \\ne D\_i 。

* \\pi\_N ：无论我有没有资格，我最终都不会参军。
* \\pi\_D ：逆反心态，有参军资格我偏不去，没有参军资格我偏要去。
* \\pi\_A ：无论我有没有资格，我最终都会去参军。
* \\pi\_C ：服从安排，有资格我就去，没资格我就不去。

![[Omnivore/因果推断的效应：ATE、ATT、ITT、LATE - 知乎/attachments/19effd5ad9706683797903ba3f130974_MD5.jpg]]

图源牛津课件（w4节)：https://andy.egge.rs/teaching/causal\_inference/

同时由于我们本来就是基于军人样本进行统计， D\_i 并非随机分布，因此只有如下式子：  
\\begin{aligned} \\mathbf{E}\[D\_i=1|Z\_i=0\]=\\pi\_A+\\pi\_D\\\\ \\mathbf{E}\[D\_i=1|Z\_i=1\]=\\pi\_A+\\pi\_C \\end{aligned}\\\\ 如此一来肯定不能单独估计出 \\pi\_i(i\\in{A,C,D,N}) 了。

不过由于随机分布，结果会成比例，可以变形出线性方程：

ITT=\\pi\_CITT\_C+\\pi\_AITT\_A+\\pi\_NITT\_N+\\pi\_DITT\_D\\\\ **解决办法是增加假设——** \\pi\_D=0 [\[8\]](#ref%5F8)，既决策函数具有单调性，**同时假设** Z\_i**和** D\_i **间没有混杂因子**，这意味着 ITT\_A=ITT\_N=0 。

> **解决办法是增加假设——**很有经济学笑话味道了。  
> 插入笑话原文：一个物理学家、一个化学家和一个经济学家漂流到孤岛上，十分饥饿。这时海面上漂來一个罐头。物理学家说：“我们可以用岩石对罐头施以动量，使其表层疲劳而断裂。”化学家说：“我们可以生火，然后把罐头加热，使它膨胀以至破裂。”经济学家则说：“假设我们有一个开罐头的起子……。”  
> 更多经济自嘲笑话参见：

加入假设后，我们就直接得到了LATE：

\\mathrm{LATE}=\\mathrm{CATE}\_{\\mathcal{C}}=\\frac{\\mathrm{ITT}}{\\pi\_{\\mathcal{C}}}\\\\ 此时估计如下：\\small \\hat{\\mathbf{CATE}\_C}=\\frac{\\mathbf{E}\\Big\[Y\_i|Z\_i=1\\Big\]-\\mathbf{E}\\Big\[Y\_i|Z\_i=0\\Big\]}{\\mathbf{E}\\Big\[D\_i|Z\_i=1\\Big\]-\\mathbf{E}\\Big\[D\_i|Z\_i=0\\Big\]}=\\frac{\\mathrm{effect\~of\~}Z\_i\\text{ on }Y\_i}{\\mathrm{effect\~of\~}Z\_i\\text{ on }D\_i}=\\frac{\\operatorname{ITT}\_Y}{\\operatorname{ITT}\_D}\\\\ 

**LATE部分**重点参考了[牛津的课件](https://link.zhihu.com/?target=https%3A//andy.egge.rs/teaching/causal%5Finference/)，如果想看相对代数化的说明可以参考[哈佛的课件](https://link.zhihu.com/?target=https%3A//scholar.harvard.edu/files/apassalacqua/files/section8%5FATE%5Fvs%5FLATE.pdf)和《基本无害的计量经济学》。

### 4、数理经济中的社科属性？

直接说"解决办法是添加几个假设"未免有些太经济学地狱笑话了。从经济含义看更加直观，如果我们研究的政策足够独特，我们需要论述政策对每个人都有影响，也就是假设中的单调性。在使用工具变量时，也需要介绍工具变量和解释变量之间的社会关系。所以为何经济学计量区别于数学？这些假设就是对社会现象的描述总结，就是其社科属性的鲜明体现。

最近学习高级宏观也有所体悟。高宏的方法非常单调，变分法加拉格朗日基本解决了所有经典模型的最优化。难点在于每个高宏模型飞来飞去的假设条件和阴间变形。无论是公式变形还是突然施加的假设，都是提炼经济现象的一个特征，然后加以数学化，这才是最大的难点。例如知识生产函数（知识作为全要素）、科夫道格拉斯生产函数（规模报酬）、家庭约束（消费贴现小于财富贴现）、家庭效用函数（风险规避）。

我开始认为——以怎样的框架挖掘均衡；通过经济现象构建具有特性的函数；总结出最优化约束条件才是经济学区别数理复合人才的“经济思想与直觉”。

顺便插入下高宏笔记：

## 三、总结

进一步举例子说明，DID估计是ATT；RDD估计是LATE[\[9\]](#ref%5F9)；聚束分析是LATE。

ATT和LATE是我们所求的，是我们渴望平行世界那样完善的对照试验，但我们有的只是ATE和ITT。

当D满足RCT时，ATE=ATT。

当D不满足RCT，但Z满足时，同时基于单调性和限制约束造出工具变量(IV）或者RDD，此时ITT=LATE。

当D不满足RCT，Z也找不到时，就采用其他方法估计反事实情况，例如群聚分析(通过残差分析变形直接估计反事实的分布和当前集聚现象形成对比)、合成控制.......

> 教材一般也会引入匹配论来实现这些估计假设。

综上，计量模型就是基于这样的潜在结果框架分析因果关系，宣扬自己研究的是因果科学。

如此一看，是否颇有"无中生有","由果索因"之妙也？

---

SCM因果推断相关的体悟笔记，参见：

## 参考

1. [^](#ref%5F1%5F0)刘若鸿,许晏君.工业用地价格与企业产能利用率\[J\].世界经济,2023,46(11):103-127.DOI:10.19985/j.cnki.cassjwe.2023.11.004.
2. [^](#ref%5F2%5F0)Chen Z, Liu Z, Suárez Serrato J C, et al. Notching R&D investment with corporate income tax cuts in China\[J\]. American Economic Review, 2021, 111(7): 2065-2100.
3. [^](#ref%5F3%5F0)Pearl J, Mackenzie D. The book of why: the new science of cause and effect\[M\]. Basic books, 2018.
4. [^](#ref%5F4%5F0)乔舒亚·安格里斯特,约恩-斯特芬·皮施克.基本无害的计量经济学\[M\].格致出版社,2012.
5. [^](#ref%5F5%5F0)Rubin D B. Causal inference using potential outcomes: Design, modeling, decisions\[J\]. Journal of the American Statistical Association, 2005, 100(469): 322-331.
6. [^](#ref%5F6%5F0)https://statmodeling.stat.columbia.edu/2009/07/05/disputes\_about/
7. [^](#ref%5F7%5F0)Angrist J D, Chen S H, Song J. Long-term consequences of Vietnam-era conscription: New estimates using social security data\[J\]. American Economic Review, 2011, 101(3): 334-338.
8. [^](#ref%5F8%5F0)有经济学笑话那味道了，解决办法是“假设”
9. [^](#ref%5F9%5F0)https://clas.ucdenver.edu/marcelo-perraillon/sites/default/files/attached-files/week\_10\_rdd\_perraillon.pdf

