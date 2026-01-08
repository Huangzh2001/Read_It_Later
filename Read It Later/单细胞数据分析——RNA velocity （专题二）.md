---
date: 2026-01-08T21:38:07+08:00
url: https://zhuanlan.zhihu.com/p/669786958
status: readed
---
[

关注

](https://www.zhihu.com/follow)[

推荐

](https://www.zhihu.com/)[

热榜

](https://www.zhihu.com/hot)[

专栏

](https://www.zhihu.com/column-square)[

圈子

New

](https://www.zhihu.com/ring-feeds)

[

付费咨询

](https://www.zhihu.com/consult)[

知学堂

](https://www.zhihu.com/education/learning)

[直答](https://zhida.zhihu.com/)

[

创作中心

](https://www.zhihu.com/creator)

单细胞数据分析——RNA velocity （专题二）

首发于[单细胞分析技术](https://www.zhihu.com/column/c_1702649426760507393)

![[Read It Later/attachments/0303c6ffdf54b3a452d0427765b5910c_MD5.jpg]]

# 单细胞数据分析——RNA velocity （专题二）

[![[Read It Later/attachments/5f955245f4be4ee77ee9602d3faa69e9_MD5.jpg]]](https://www.zhihu.com/people/sida-carol)

[达叔](https://www.zhihu.com/people/sida-carol)

​![[Read It Later/attachments/5745a448859ae36ec06cc04d38e7b515_MD5.png]]

站在数学，计算和生物的十字路口

[

收录于 · 单细胞分析技术

](https://www.zhihu.com/column/c_1702649426760507393)

5 人赞同了该文章

这篇文章中，我们将会介绍RNA velocity中的确定性模型的数学推理部分，请备好小板凳，慢慢体会推公式的奇妙~

![[Read It Later/attachments/bd5f5a9fc354a16a72df3c8be3b7052b_MD5.jpg]]

图1 RNA剪接过程

上文我们提到，依据图1的过程，我们可以建立如下的两个[微分方程](https://zhida.zhihu.com/search?content_id=236971959&content_type=Article&match_order=1&q=%E5%BE%AE%E5%88%86%E6%96%B9%E7%A8%8B&zhida_source=entity)：

$\frac{d u}{\&\text{nbsp}; d t} & = \alpha \left(\right. t \left.\right) - \beta u \left(\right. t \left.\right) \\ \frac{d s}{\&\text{nbsp}; d t} & = \beta u \left(\right. t \left.\right) - \gamma s \left(\right. t \left.\right)$\\begin{aligned} \\frac{\\mathrm{d} u}{\\mathrm{~d} t} & =\\alpha(t)-\\beta u(t) \\\\ \\frac{\\mathrm{d} s}{\\mathrm{~d} t} & =\\beta u(t)-\\gamma s(t)\\end{aligned}

  

在[velocyto](https://zhida.zhihu.com/search?content_id=236971959&content_type=Article&match_order=1&q=velocyto&zhida_source=entity)中，我们做出如下假设：假设各基因的剪接速率 $\beta \&\text{nbsp};$ \\beta\\ 都相同且为常数，为表方便，可设置成1，方便下文的公式推导，所以我们得到了下文的两个简化方程：

$\frac{d u}{\&\text{nbsp}; d t} & = \alpha \left(\right. t \left.\right) - u \left(\right. t \left.\right) \\ \frac{d s}{\&\text{nbsp}; d t} & = u \left(\right. t \left.\right) - \gamma s \left(\right. t \left.\right)$\\begin{aligned} \\frac{\\mathrm{d} u}{\\mathrm{~d} t} & =\\alpha(t)-u(t) \\\\ \\frac{\\mathrm{d} s}{\\mathrm{~d} t} & =u(t)-\\gamma s(t)\\end{aligned}

  

$\alpha$\\alpha 是[转录生成速率](https://zhida.zhihu.com/search?content_id=236971959&content_type=Article&match_order=1&q=%E8%BD%AC%E5%BD%95%E7%94%9F%E6%88%90%E9%80%9F%E7%8E%87&zhida_source=entity)，由生物学知识可知，DNA转录是一个间歇性的过程，有转录时间（on time）和未转录时间（off time），因此， $\alpha$\\alpha 应该为分段函数，如下面的公式所示：

$\alpha \left(\right. t \left.\right) = \left{\right. \alpha^{\text{on}\&\text{nbsp};} , & t \leq t_{s} \\ \alpha^{\text{off}\&\text{nbsp};} , & t > t_{s}$\\alpha(t)=\\left\\{\\begin{array}{ll}\\alpha^{\\text {on }}, & t \\leq t\_{s} \\\\ \\alpha^{\\text {off }}, & t>t\_{s}\\end{array}\\right.

  

$t_{s}$t\_{s} 是转录与未转录状态变化的临界时刻，在转录时，假设转录的速率是一个常数，记作 $\alpha^{\text{on}\&\text{nbsp};}$ \\alpha^{\\text {on }} ，转录关闭时， $\alpha^{\text{off}\&\text{nbsp};} = 0$\\alpha^{\\text {off }}=0

  

在上文中，我们定义了RNA velocity 为

$\mathbf{\mathit{v}} \left(\right. t \left.\right) = \frac{d s}{\&\text{nbsp}; d t} = u \left(\right. t \left.\right) - \gamma s \left(\right. t \left.\right)$\\boldsymbol{v}(t)=\\frac{\\mathrm{d} s}{\\mathrm{~d} t}=u(t)-\\gamma s(t)

  

假设在t=0时刻，未剪接的mRNA数量为 $u_{0}$u\_{0} ，剪接mRNA的数量为 $s_{0}$ s\_{0} ，我们可以用 $u_{0} , s_{0}$u\_{0},s\_{0} 和其他参数表示微分方程的解析解，由于转录状态有两种，由 $t_{s}$t\_{s} 时刻分隔，所以应该分两个阶段进行。

对于阶段1： $t \leq t_{s}$t \\leq t\_{s} ，我们可以以最初状态为计时开始状态， $u_{0} = 0$u\_{0}=0 ， $s_{0} = 0$s\_{0}=0 ，则

$u \left(\right. t \left.\right) = \alpha \left(\right. 1 - e^{- t} \left.\right) \\ \\ s \left(\right. t \left.\right) = \frac{\alpha}{\gamma} \left(\right. 1 - e^{- \gamma t} \left.\right) + \frac{\alpha}{\gamma - 1} \left(\right. e^{- \gamma t} - e^{- t} \left.\right)$\\begin{array}{l}u(t)=\\alpha\\left(1-e^{-t}\\right) \\\\\\\\ s(t)=\\frac{\\alpha}{\\gamma}\\left(1-e^{-\\gamma t}\\right)+\\frac{\\alpha}{\\gamma-1}\\left(e^{-\\gamma t}-e^{- t}\\right)\\end{array}

  

对于阶段2： $t > t_{s}$ t>t\_{s} ，此刻不论哪种mRNA，其数量肯定不为0，因此，设数量分别为 $u_{s} , s_{s}$u\_s,s\_s ，解析解可由下列式子表示：

$u \left(\right. t \left.\right) = u_{s} e^{\left(\right. t_{s} - t \left.\right)} \\ \\ s \left(\right. t \left.\right) = s_{s} e^{- \gamma \left(\right. t - t_{s} \left.\right)} - \frac{u_{s}}{\gamma - 1} \left(\right. e^{- \gamma \left(\right. t - t_{s} \left.\right)} - e^{- \left(\right. t - t_{s} \left.\right)} \left.\right)$\\begin{array}{l}u(t)=u\_{s} e^{\\left(t\_{s}-t\\right)} \\\\ \\\\s(t)=s\_{s} e^{-\\gamma\\left(t-t\_{s}\\right)}-\\frac{u\_{s}}{\\gamma-1}\\left(e^{-\\gamma\\left(t-t\_{s}\\right)}-e^{-\\left(t-t\_{s}\\right)}\\right)\\end{array}

  

在velocyto中，我们研究确定性模型，稳态。确定性模型已经解释清楚，那么什么是稳态(steady state)呢？具体而言，我们认为转录阶段(on stage)持续足够长时间，最后的状态接近于稳态(steady state)。在稳态中，剪接mRNA的产生速率等于降解速率，二者持平。因此，可以得到 steady state 的等式：

$\mathbf{\mathit{v}} \left(\right. \mathbf{\mathit{t}} \left.\right) = \frac{d s}{\&\text{nbsp}; d t} = u \left(\right. t \left.\right) - \gamma s \left(\right. t \left.\right) = 0$\\boldsymbol{v(t)}=\\frac{\\mathrm{d} s}{\\mathrm{~d} t}=u(t)-\\gamma s(t)=0

  

稳态如下图2中灰色对角线所示，落在此线上的点即达到了稳态。

![[Read It Later/attachments/c11704a8f5dc6c178cbd11398cb74c67_MD5.png]]

图2 稳态示意图

在稳态下，可以利用这个平衡条件来通过[最小二乘拟合](https://zhida.zhihu.com/search?content_id=236971959&content_type=Article&match_order=1&q=%E6%9C%80%E5%B0%8F%E4%BA%8C%E4%B9%98%E6%8B%9F%E5%90%88&zhida_source=entity)近似计算降解速率，即：

$\gamma^{*} = \underset{\gamma}{arg ⁡ min} \parallel \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \parallel^{2} = \frac{\mathbf{\mathit{u}}^{T} \mathbf{\mathit{s}}}{\parallel \mathbf{\mathit{s}} \parallel^{2}}$\\gamma^{\*}=\\underset{\\gamma}{\\arg \\min }\\|\\boldsymbol{u}-\\gamma \\boldsymbol{s}\\|^{2}=\\frac{\\boldsymbol{u}^{\\mathrm{T}} \\boldsymbol{s}}{\\|\\boldsymbol{s}\\|^{2}}

【详细推导过程】：

要推导这个最小二乘估计的解析解，我们首先需要定义我们的目标函数，也就是我们想要最小化的东西。在这个问题中，我们的目标函数是误差的平方和，即

$\parallel \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \parallel^{2}$\\|\\boldsymbol{u}-\\gamma \\boldsymbol{s}\\|^{2}

为了找到这个函数的最小值，我们需要对 γ 求导，并将导数设置为0。这就给了我们一个方程，我们可以从中解出 γ 的值。

目标函数是：

$f \left(\right. \gamma \left.\right) = \parallel \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \parallel^{2}$f(\\gamma)=\\|\\boldsymbol{u}-\\gamma \\boldsymbol{s}\\|^{2}

我们可以将这个函数写成更明确的形式：

$f \left(\right. \gamma \left.\right) = \left(\right. \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \left.\right)^{T} \left(\right. \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \left.\right)$f(\\gamma)=(\\boldsymbol{u}-\\gamma \\boldsymbol{s})^{\\mathrm{T}}(\\boldsymbol{u}-\\gamma \\boldsymbol{s})

然后，我们对 γ 求导。一般情况下，对于一个向量 $\mathbf{\mathit{v}}$\\boldsymbol{v} ，有

$\frac{d}{d x} \mathbf{\mathit{v}}^{T} \mathbf{\mathit{v}} = 2 \mathbf{\mathit{v}}^{T} \frac{d \mathbf{\mathit{v}}}{d x}$\\frac{d}{d x} \\boldsymbol{v}^{\\mathrm{T}} \\boldsymbol{v}=2 \\boldsymbol{v}^{\\mathrm{T}} \\frac{d \\boldsymbol{v}}{d x}

应用这个规则，我们得到:

$\frac{d}{d \gamma} f \left(\right. \gamma \left.\right) = 2 \left(\right. \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \left.\right)^{T} \left(\right. - \mathbf{\mathit{s}} \left.\right)$\\frac{d}{d \\gamma} f(\\gamma)=2(\\boldsymbol{u}-\\gamma \\boldsymbol{s})^{\\mathrm{T}}(-\\boldsymbol{s})

为了找到最小值，我们将导数设为0：

$0 = 2 \left(\right. \mathbf{\mathit{u}} - \gamma \mathbf{\mathit{s}} \left.\right)^{T} \left(\right. - \mathbf{\mathit{s}} \left.\right)$0=2(\\boldsymbol{u}-\\gamma \\boldsymbol{s})^{\\mathrm{T}}(-\\boldsymbol{s})

展开并重新排列得到：

$\gamma \mathbf{\mathit{s}}^{T} \mathbf{\mathit{s}} = \mathbf{\mathit{u}}^{T} \mathbf{\mathit{s}}$\\gamma \\boldsymbol{s}^{\\mathrm{T}} \\boldsymbol{s}=\\boldsymbol{u}^{\\mathrm{T}} \\boldsymbol{s}

最后，解出 γ：

$\gamma^{*} = \frac{u^{T} s}{\parallel s \parallel^{2}}$\\gamma^{\*}=\\frac{u^{\\mathrm{T}} s}{\\|s\\|^{2}}

<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="34.212ex" height="3.137ex" viewBox="0 -999.4 14729.9 1350.5" role="img" focusable="false" aria-hidden="true" style="vertical-align: -0.815ex;"><g stroke="currentColor" fill="currentColor" stroke-width="0" transform="matrix(1 0 0 -1 0 0)" data-darkreader-inline-fill="" data-darkreader-inline-stroke="" style="--darkreader-inline-fill: currentColor; --darkreader-inline-stroke: currentColor;"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">这</text><g transform="translate(816,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">里</text></g><use xlink:href="#MJMAIN-2225" x="1632" y="0"></use><use xlink:href="#MJMATHBI-73" x="2132" y="0"></use><g transform="translate(2664,0)"><use xlink:href="#MJMAIN-2225" x="0" y="0"></use><use transform="scale(0.707)" xlink:href="#MJMAIN-32" x="707" y="513"></use></g><g transform="translate(3618,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">是</text></g><use xlink:href="#MJMATHBI-73" x="4434" y="0"></use><g transform="translate(4966,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">的</text></g><g transform="translate(5782,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">点</text></g><g transform="translate(6598,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">积</text></g><g transform="translate(7414,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">自</text></g><g transform="translate(8212,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">身</text></g><g transform="translate(9011,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">，</text></g><g transform="translate(9809,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">也</text></g><g transform="translate(10625,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">就</text></g><g transform="translate(11441,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">是</text></g><g transform="translate(12257,0)"><use xlink:href="#MJMATHBI-73" x="0" y="0"></use><use transform="scale(0.707)" xlink:href="#MJMAIN-54" x="751" y="513"></use></g><use xlink:href="#MJMATHBI-73" x="13400" y="0"></use><g transform="translate(13931,0)"><text font-family="STIXGeneral,'Arial Unicode MS',serif" stroke="none" transform="scale(49.871) matrix(1 0 0 -1 0 0)" data-darkreader-inline-stroke="" style="--darkreader-inline-stroke: none;">。</text></g></g></svg>$这 里 \parallel \mathbf{\mathit{s}} \parallel^{2} 是 \mathbf{\mathit{s}} 的 点 积 自 身 ， 也 就 是 \mathbf{\mathit{s}}^{T} \mathbf{\mathit{s}} 。$这里 \\|\\boldsymbol{s}\\|^{2} 是 \\boldsymbol{s} 的点积自身，也就是 \\boldsymbol{s}^{\\mathrm{T}} \\boldsymbol{s} 。

这就是最小二乘估计的解析解的推导过程。

在未来的推文中，我们也会详细介绍矩阵求导以及最小二乘法的求解思路，敬请期待~

其中u、s是向量，其分量对应于图2中每个处于稳态的点，因此，速率可以估计为：

$\mathbf{\mathit{v}} = \mathbf{\mathit{u}} - \gamma^{*} \mathbf{\mathit{s}}$\\boldsymbol{v}=\\boldsymbol{u}-\\gamma^{\*} \\boldsymbol{s}

需要注意的是，在速率估计时，需要用处在稳态的细胞，也即取图2中的两端的点，如下图3所示：

![[Read It Later/attachments/d25bb161388e4a343d5a39151fde3e78_MD5.jpg]]

![[Read It Later/attachments/a77afd2f79480c9dd6e738711eab33cc_MD5.jpg]]

图3 估计情况

我们只使用实心绿色圆点估计的情况如紫色线所示，使用全部圆点估计的情况如黑色线所示，可见不论是哪种情况，采用两端的点估计总能达到准确的效果。

  

作者：武汉大学 董弘禹

顾问：叶思达

编辑排版：陆思陶，黄仰含，秦志高

还没有人送礼物，鼓励一下作者吧

[所属专栏 · 2025-04-27 00:26 更新](https://zhuanlan.zhihu.com/c_1702649426760507393)

[![[Read It Later/attachments/e540cfa8277e66ea6e338f492f7cdd09_MD5.png]]

单细胞分析技术

![[Read It Later/attachments/5f955245f4be4ee77ee9602d3faa69e9_MD5.jpg]]

达叔

6 篇内容 · 38 赞同

](https://zhuanlan.zhihu.com/c_1702649426760507393)

[

最热内容 ·

单细胞数据分析——RNA velocity（专题一）

](https://zhuanlan.zhihu.com/c_1702649426760507393)

编辑于 2023-12-01 10:39・江苏

[

单细胞测序

](https://www.zhihu.com/topic/21604647)

[

生物信息

](https://www.zhihu.com/topic/19661993)

[

RNA

](https://www.zhihu.com/topic/26322931)

![[Read It Later/attachments/26725aa9602db156eaafd2cb68a4a816_MD5.jpg]]

理性发言，友善互动

  

2 条评论

默认

最新

[![[Read It Later/attachments/5f955245f4be4ee77ee9602d3faa69e9_MD5.jpg]]](https://www.zhihu.com/people/57bda892c31aa756dd97458599dc08be)

[达叔](https://www.zhihu.com/people/57bda892c31aa756dd97458599dc08be)

作者![[Read It Later/attachments/5745a448859ae36ec06cc04d38e7b515_MD5.png]]

Q交流群101345341

2024-01-04 · 美国 · 作者置顶

[![[Read It Later/attachments/13d402f2826e778e3d0a8e0f7890c0cf_MD5.jpg]]](https://www.zhihu.com/people/2cd9d91b28f49cb6c22ec26304e1e783)

[白头翁](https://www.zhihu.com/people/2cd9d91b28f49cb6c22ec26304e1e783)

再讲讲随机模型呗，求后续

2023-12-26 · 北京

关于作者

[![[Read It Later/attachments/5f955245f4be4ee77ee9602d3faa69e9_MD5.jpg]]](https://www.zhihu.com/people/sida-carol)

[达叔](https://www.zhihu.com/people/sida-carol)​![[Read It Later/attachments/5745a448859ae36ec06cc04d38e7b515_MD5.png]]

站在数学，计算和生物的十字路口

[

回答

**241**

](https://www.zhihu.com/people/sida-carol/answers)[

文章

**80**

](https://www.zhihu.com/people/sida-carol/posts)[

关注者

**1,657**

](https://www.zhihu.com/people/sida-carol/followers)

大家都在搜

换一换

[商务部加强对日两用物项出口管制395 万](https://www.zhihu.com/search?q=%E5%95%86%E5%8A%A1%E9%83%A8%E5%8A%A0%E5%BC%BA%E5%AF%B9%E6%97%A5%E4%B8%A4%E7%94%A8%E7%89%A9%E9%A1%B9%E5%87%BA%E5%8F%A3%E7%AE%A1%E5%88%B6&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[长生种短命种理论349 万](https://www.zhihu.com/search?q=%E9%95%BF%E7%94%9F%E7%A7%8D%E7%9F%AD%E5%91%BD%E7%A7%8D%E7%90%86%E8%AE%BA&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[女子以油养肤导致面部疯狂掉皮348 万](https://www.zhihu.com/search?q=%E5%A5%B3%E5%AD%90%E4%BB%A5%E6%B2%B9%E5%85%BB%E8%82%A4%E5%AF%BC%E8%87%B4%E9%9D%A2%E9%83%A8%E7%96%AF%E7%8B%82%E6%8E%89%E7%9A%AE&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[雄霸为什么一定要杀掉风云338 万](https://www.zhihu.com/search?q=%E9%9B%84%E9%9C%B8%E4%B8%BA%E4%BB%80%E4%B9%88%E4%B8%80%E5%AE%9A%E8%A6%81%E6%9D%80%E6%8E%89%E9%A3%8E%E4%BA%91&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)

[日本梅毒感染扩散328 万](https://www.zhihu.com/search?q=%E6%97%A5%E6%9C%AC%E6%A2%85%E6%AF%92%E6%84%9F%E6%9F%93%E6%89%A9%E6%95%A3&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[日本年轻人聚众晒梅毒320 万](https://www.zhihu.com/search?q=%E6%97%A5%E6%9C%AC%E5%B9%B4%E8%BD%BB%E4%BA%BA%E8%81%9A%E4%BC%97%E6%99%92%E6%A2%85%E6%AF%92&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[跨境赌诈集团头目陈志被押解回国318 万](https://www.zhihu.com/search?q=%E8%B7%A8%E5%A2%83%E8%B5%8C%E8%AF%88%E9%9B%86%E5%9B%A2%E5%A4%B4%E7%9B%AE%E9%99%88%E5%BF%97%E8%A2%AB%E6%8A%BC%E8%A7%A3%E5%9B%9E%E5%9B%BD&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[多地裁判文书隐去法官姓名和案号316 万](https://www.zhihu.com/search?q=%E5%A4%9A%E5%9C%B0%E8%A3%81%E5%88%A4%E6%96%87%E4%B9%A6%E9%9A%90%E5%8E%BB%E6%B3%95%E5%AE%98%E5%A7%93%E5%90%8D%E5%92%8C%E6%A1%88%E5%8F%B7&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

[医生提醒秒睡可能是身体在报警312 万](https://www.zhihu.com/search?q=%E5%8C%BB%E7%94%9F%E6%8F%90%E9%86%92%E7%A7%92%E7%9D%A1%E5%8F%AF%E8%83%BD%E6%98%AF%E8%BA%AB%E4%BD%93%E5%9C%A8%E6%8A%A5%E8%AD%A6&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)热

[美 ICE 执法人员当街射杀女子306 万](https://www.zhihu.com/search?q=%E7%BE%8E+ICE+%E6%89%A7%E6%B3%95%E4%BA%BA%E5%91%98%E5%BD%93%E8%A1%97%E5%B0%84%E6%9D%80%E5%A5%B3%E5%AD%90&search_source=Trending&utm_content=search_hot&utm_medium=organic&utm_source=zhihu&type=content)新

### 推荐阅读

[

![[Read It Later/attachments/b8e65fa84494142de9b7ec44660de353_MD5.jpg]]

# 每天一篇单细胞56-RNA 速率-1

今晚的月色真好

](https://zhuanlan.zhihu.com/p/180253811)[

# RNA-seq 分析流程 —— 概述

前言 接下来我们要介绍的是 RNA-seq 数据的处理分析流程，根据 RNA-seq 测序技术的不同，可以分为三种：short-readlong-readdirect RNA-seq而我们一般的 RNA-seq 测序数据分析流程算法，基…

名本无名

](https://zhuanlan.zhihu.com/p/393674599)[

# 准确、快速地从头预测RNA 3D结构，港中大、复旦等深度学习方法RhoFold+登Nature子刊

编辑 | KX RNA 分子在分子生物学中心法则中起关键作用，RNA 结构如何影响基因调控和功能一直是研究的热门话题。准确预测 RNA 三维 (3D) 结构仍是一个难题。RNA 的结构灵活性导致实验确定的…

机器之心发表于Scien...

](https://zhuanlan.zhihu.com/p/9773513998)[

# 2020-011 RNA velocity of single cells

文献阅读篇 1 RNA丰度是单个细胞状态的有力指标。单细胞RNA测序可以显示RNA丰度，这种方法定量准确性高，灵敏度高，通度高。但是，这种方法只能在某个时间点捕获静态快照，这对分析时间层级…

SSSimon Yang

](https://zhuanlan.zhihu.com/p/423678934)

❌ 未收藏