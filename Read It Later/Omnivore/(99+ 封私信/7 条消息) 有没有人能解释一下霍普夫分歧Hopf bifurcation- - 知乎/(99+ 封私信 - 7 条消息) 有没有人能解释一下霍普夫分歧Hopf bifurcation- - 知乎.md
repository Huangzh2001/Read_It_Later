---
id: 7369605d-257a-4f85-8c33-b2b64b90561e

url: https://www.zhihu.com/question/26359793/answer/133232527
status: reading
---


tags::  #Reading 

# (99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation? - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/99-7-hopf-bifurcation-1911cb2abac)
[Read Original](https://www.zhihu.com/question/26359793/answer/133232527)

关注者

**86**

被浏览

**134,610**

[![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/6efbb89056ecfd1287f24c8f8bda1794_MD5.png]]](https://www.zhihu.com/people/hun-dun-xun-yang-jian)

[许铁-巡洋舰科技](https://www.zhihu.com/people/hun-dun-xun-yang-jian)

[​](https://www.zhihu.com/question/48509984)

神经科学等 2 个话题下的优秀答主

​ 关注

243 人赞同了该回答

作者：许铁-巡洋舰科技

链接：

[知乎专栏](https://zhuanlan.zhihu.com/p/22467021)

来源：知乎

著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

 **Bifurcation 与相变**

我们用Bifurcation研究一个动力学系统的演变。动力学系统由[状态变量](https://www.zhihu.com/search?q=%E7%8A%B6%E6%80%81%E5%8F%98%E9%87%8F&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)（系统可以自由变化的量）和控制变量（参数）组成。在初步讨论一个动力学系统性质的时候，我们先假设参数不变，因此可以得到系统动力学在[相平面](https://www.zhihu.com/search?q=%E7%9B%B8%E5%B9%B3%E9%9D%A2&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)的拓扑图，然后求定点和轨道。 在二维的情况下，参数给定，[动力学流型](https://www.zhihu.com/search?q=%E5%8A%A8%E5%8A%9B%E5%AD%A6%E6%B5%81%E5%9E%8B&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)得出，则一切皆可精确预测。 

**真实的世界里从来没有一程不变的参数，真正不变的只有变化，而有的时候参数和变量甚至难以区分彼此。** 因此，[非线性动力学](https://www.zhihu.com/search?q=%E9%9D%9E%E7%BA%BF%E6%80%A7%E5%8A%A8%E5%8A%9B%E5%AD%A6&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)给出的对世界的最精密的描述，不是确定参数下的流行，而是在参数空间里对应的不同相平面流型。 **简单的讲，动力学不仅感兴趣我们现在所在的那个世界，而是[所有可能的世界](https://www.zhihu.com/search?q=%E6%89%80%E6%9C%89%E5%8F%AF%E8%83%BD%E7%9A%84%E4%B8%96%E7%95%8C&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)（每个参数就是一个世界）。** 参数的空间好比[小径分叉的花园](https://www.zhihu.com/search?q=%E5%B0%8F%E5%BE%84%E5%88%86%E5%8F%89%E7%9A%84%E8%8A%B1%E5%9B%AD&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)（无限可能性的博物馆），每一点上你都有一扇窗户， 打开可以看到那个世界的可能性。 在这个花园里走路，你将看到一种可能性是如何演化成另一种可能性的。

下面我们就到[二维世界](https://www.zhihu.com/search?q=%E4%BA%8C%E7%BB%B4%E4%B8%96%E7%95%8C&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)里去玩一玩，请看下图， 你一定看到了十字架和一个抛物线。这是最简单的线性二维动力学系统，完全可以通过求解[系数矩阵](https://www.zhihu.com/search?q=%E7%B3%BB%E6%95%B0%E7%9F%A9%E9%98%B5&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)（对应于一维情况下的单一系数）的特征值解决。 首先看这个系统的定点，即发现（0，0），好简单（带入[方程微分](https://www.zhihu.com/search?q=%E6%96%B9%E7%A8%8B%E5%BE%AE%E5%88%86&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)为0）。 但是系统是被这个定点牢牢抓住， 还是围绕它振动， 还是远离它而去，确取决于系统的参数。 

而这个平面的横轴和纵轴就代表这一[矩阵特征值](https://www.zhihu.com/search?q=%E7%9F%A9%E9%98%B5%E7%89%B9%E5%BE%81%E5%80%BC&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)的实部和虚部。 当系统的参数变化， 表现为系数矩阵的[特征值](https://www.zhihu.com/search?q=%E7%89%B9%E5%BE%81%E5%80%BC&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)在这一平面上的运动。 [特征根](https://www.zhihu.com/search?q=%E7%89%B9%E5%BE%81%E6%A0%B9&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)的实数部分的正负决定系统是趋于稳定的定点还是发散。 为负的话你将收敛到到她身边， 为正你将远离她而去。 而如果实数部分为0 ，特征根只有虚部，那么系统意味着系统既要远离定点又出不去她的引力范围， 最后就成围绕她绕转，即振动的情况。虚部的正负决定系统围绕[定点转动](https://www.zhihu.com/search?q=%E5%AE%9A%E7%82%B9%E8%BD%AC%E5%8A%A8&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)的方向，在此不多叙述。

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/8d52d07717aae2f13ee69d6450b4f505_MD5.png]]

**图，最简单的二维动力学系统-由一个[线性微分方程](https://www.zhihu.com/search?q=%E7%BA%BF%E6%80%A7%E5%BE%AE%E5%88%86%E6%96%B9%E7%A8%8B&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)组给出。** 

**那么什么是Bifurcation呢？ 它就是参数空间里系统动力学流的性质发生质变的点。**例如上图里的那个抛物线， 当系统的参数变化越过抛物线的时候，系统就从稳定吸引变成了发散远离定点，这个过程就是Bifurcation.

而在抛物线一侧的变化只是定量的变化，却无定性改变，这就是普通的变化。Bifurcation标志系统的动力学性质就发生彻底的变化。好比两个人在一条路上走着走着，突然到了岔路口，从此[南辕北辙](https://www.zhihu.com/search?q=%E5%8D%97%E8%BE%95%E5%8C%97%E8%BE%99&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)。

在动力学家的眼里，只有那个bifurcation point 具有关键意义，起到区分不同系统的作用。 其它小的变化都忽略了（这恐怕是他们不好找女朋友的原因）。

另一种典型的[bifurcation](https://www.zhihu.com/search?q=bifurcation&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)情况：

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/c5998eeb50935f8d6d6c1d5acc96ff24_MD5.png]]

图中的小球一开始在谷底，处于稳定平衡。这个谷就代表系统的参数，当参数固定，山谷的形状就是确定的。当我们改变参数，山谷的形状发生变化，谷底逐步被拉平，而最后隆起出一个小山。在这个过程里，中心点的稳定性丧失，小球将面临一次全新的选择，是向左还是向右？ 这个谷底变成小山的过程就叫Bifurcation，而谷和丘的临界点，就是Bifurcation Point。

**从此图可见，Bifurcation的本质是系统反馈性质的变化。**当小球在谷底，一个负反馈保证它不离开（稳），而当谷底逐步变平突起的过程，[负反馈](https://www.zhihu.com/search?q=%E8%B4%9F%E5%8F%8D%E9%A6%88&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)演化成离开谷底的正反馈。

**Bifurcation Point上的小球具有“[自由意志](https://www.zhihu.com/search?q=%E8%87%AA%E7%94%B1%E6%84%8F%E5%BF%97&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)”，或者说非常敏感，一个随机的扰动都可以被放大（正反馈的作用），使它向左或向右。这就是历史的转折点。而当Bifurcation的过程结束，小球就落入了新的平衡点。**此时的它，已经被一个负反馈束缚住，非有强大的能量，是不会离去了。

Bifurcation， 正是物理里相变的化身。 在动力学的世界观里，那些定量的改变等于没变，而只有Bifurcation-分道扬镳，才是真正的变化。物理，化学，生物一切最有趣的现象，都在[Bifurcation点](https://www.zhihu.com/search?q=Bifurcation%E7%82%B9&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)上，因为它的敏感，它的无限可能。

\* Bifurcation Point，就是我们所说的决定性瞬间。在这个时候，系统的前途未卜，而有任何一个风吹草动都可能使它转左或转右而走向截然不同的未来。 如同高考考场上的同学，蒙对蒙错一个选择题就去往了截然不同的城市，遇到了截然不同的爱情。

还有历史上的关键期。 如同姜文新片《一步之遥》主角[马走日](https://www.zhihu.com/search?q=%E9%A9%AC%E8%B5%B0%E6%97%A5&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)的故事，作为满清贵族的他，被[老佛爷](https://www.zhihu.com/search?q=%E8%80%81%E4%BD%9B%E7%88%B7&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)赋予下达全国男人剪辫子的命令，那天他跑出去下达谕旨， 天却下起大雪，他躲进一个小酒吧喝了两桶酒睡到天亮，没想到天下已经民国了....他那个哭啊。。

这个故事看似荒唐却很真，因为1911年就是中国历史的Bifurcation Point，只有在Bifurcation Point -相变点上， 一个人的小事才能左右国运，一个小时就是一世纪。

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/604d59111611aa03117c7e4c3478a30b_MD5.png]]

**君主立宪还是走向共和？ To be or Not to be，That is a Bifurcation ！**

**Hopf-Bifurcation : 沟通平衡与振动的世界。**

用一句话说， Hopf-Bifurcation 描述一个系统定点失去吸引力并最终产生闭合轨道的过程。 这与我开头引题的抛物线那个图其实是一回事，我们把[非线性系统](https://www.zhihu.com/search?q=%E9%9D%9E%E7%BA%BF%E6%80%A7%E7%B3%BB%E7%BB%9F&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)在定点附近进行[线性近似](https://www.zhihu.com/search?q=%E7%BA%BF%E6%80%A7%E8%BF%91%E4%BC%BC&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)就可以沿用上面的分析。 

[BZ反应](https://www.zhihu.com/search?q=BZ%E5%8F%8D%E5%BA%94&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D) (Belousov Zhabotinsky 化学反应)

我们高中课本有个东西叫化学平衡， 说的是化学过程最终都导致平衡，该反应的反应过了，我们就得到一堆万年不变的反应产物。 但是1950年代的一个苏联科学家[belousov](https://www.zhihu.com/search?q=belousov&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)却在它的反应里发现了一个十分惊人的现象， 他发现他手里的[混合物反应](https://www.zhihu.com/search?q=%E6%B7%B7%E5%90%88%E7%89%A9%E5%8F%8D%E5%BA%94&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)后还会在一段时候回到原来的状态，然后又重新反应，如此周期反复。这一现象一出，他就被封杀了。因为他的结果不符合[热力学第二定律](https://www.zhihu.com/search?q=%E7%83%AD%E5%8A%9B%E5%AD%A6%E7%AC%AC%E4%BA%8C%E5%AE%9A%E5%BE%8B&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)（根据热力学第二定律，自发状态下系统必须趋于平衡），又加上适逢冷战，他到死也没看到他的成果被承认，成为科学史上几个重大悲剧之一。

但是它的发现却开拓了一个全新的领域-化学振荡，而他的发现也成为复杂性可以从简单系统中诞生的典型例子，与[图灵](https://www.zhihu.com/search?q=%E5%9B%BE%E7%81%B5&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)对生物斑图的研究一起，开拓了复杂科学的先河。

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/ae2ba10b51c908631509fb31e4dc75e0_MD5.png]]

**周期振荡的化学反应，红变蓝又变红。**  

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/4ce35310792e0c6f354f1886ab622b86_MD5.png]]

**Belousov的[化学振荡](https://www.zhihu.com/search?q=%E5%8C%96%E5%AD%A6%E6%8C%AF%E8%8D%A1&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)可以自发产生美丽复杂的斑图（上图），被认为是复杂性从简单系统产生的典范。 对生命起源等问题都很有启发。**

**如果我们给这个化学反应写出[热力学方程](https://www.zhihu.com/search?q=%E7%83%AD%E5%8A%9B%E5%AD%A6%E6%96%B9%E7%A8%8B&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)，我们就可以发现，循规蹈矩的化学平衡和“异常”的化学振荡可以完全统一在一个系统里，只是根据反应物浓度不同而不同。 它的本质即Hopf Bifurcation。**

[Belousov反应](https://www.zhihu.com/search?q=Belousov%E5%8F%8D%E5%BA%94&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)具有众多反应物和接近20个步骤，但是可以简化为一个二维动力学系统（内容繁杂在此不续）：

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/6ba7790da874cff8039d5b41d5334cc2_MD5.png]]

随着参数a，b的变化系统具有完全不同的[动力学模型](https://www.zhihu.com/search?q=%E5%8A%A8%E5%8A%9B%E5%AD%A6%E6%A8%A1%E5%9E%8B&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)，见下图：

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/c417745f1efadfee5fb1a730f3b5c866_MD5.png]]

Hopf Bifurcation， 左图是一个具有静止平衡态（定点）的系统，动力学流从不同的位置旋入这个系统。 右图为振动解（[limit cycle](https://www.zhihu.com/search?q=limit%20cycle&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)）的诞生， 事实上，**两张图描述的是一个系统的连续变化，开始那个稳定的平衡点失去稳定属性，流行从旋入这个点变为旋出，而归于确定的闭合轨道。这就是Hopf Bifurcation的范式。**

**Hopf Bifurcation 作为阐述振动和[静态平衡](https://www.zhihu.com/search?q=%E9%9D%99%E6%80%81%E5%B9%B3%E8%A1%A1&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)互相演化的基本手段， 在生物，经济等领域反复出现。**

甚至我们的生命过程本身也可以理解为一个大的Hopf Bifurcation。 心脏的跳动和新陈代谢的循环伴随我们一生，这是系统的[振动解](https://www.zhihu.com/search?q=%E6%8C%AF%E5%8A%A8%E8%A7%A3&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)。 我们死的那一刻，振动停止我们步入了静态平衡。这就是Bifurcation Point，from live to death。

中国历史的演变可以看做一个大Hopf Bifurcation。 从中国历史的初始阶段-[东周列国](https://www.zhihu.com/search?q=%E4%B8%9C%E5%91%A8%E5%88%97%E5%9B%BD&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)（不考虑部落传说时代的夏商）到大秦帝国的诞生，可谓经历了Bifurcation。因为动力学系统的性质前后发生了根本变化， 从之前小邦国的平衡状态发展到[帝国循环](https://www.zhihu.com/search?q=%E5%B8%9D%E5%9B%BD%E5%BE%AA%E7%8E%AF&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)的动力学模型。 春秋战国可谓中国历史的关键期（critical period）。 但即使在秦帝国初建的时候，前一个动力学模型依然没有完全结束，两个模型依然在竞争（Bifurcation point）。 所以秦帝国才只持续那么短，因为邦国并立的组织虽已破坏，但其“鬼影”还在，新帝国的形式并不稳定。 

所以陈胜之后，才有六国后人的争相复辟， 而项羽则作为旧的动力学模型的最后惊魂一瞥划过天空，作为楚国贵族的他，夺了天下，却只想分封诸侯，回到六国旧梦。而也因如此，注定他只是一颗流星，他终是敌不过作为新帝国模型代言的刘邦。他的失败，根本是他所代言的动力学模型的失败， 而非孤勇。 汉帝国能够成为中国第一个持续两百年以上的帝国， 也是因为因为汉初皇帝彻底瓦解了邦国的旧动力学体系。他们所做的分封刘氏皇族，进一步加强[大一统](https://www.zhihu.com/search?q=%E5%A4%A7%E4%B8%80%E7%BB%9F&search%5Fsource=Entity&hybrid%5Fsearch%5Fsource=Entity&hybrid%5Fsearch%5Fextra=%7B%22sourceType%22%3A%22answer%22%2C%22sourceId%22%3A133232527%7D)，都彻底瓦解了旧的社会组织。 旧贵族的梦是在几千年都兴不起来了。

（注： 虽然中国历史也多次经历分裂诸侯并立的时代，但那都是作为帝国循环的某个特殊转化期而存在，而非稳定的状态。）

[发布于 2016-11-27 16:43](https://www.zhihu.com/question/26359793/answer/133232527)

​赞同 243​​15 条评论​收藏​喜欢

​

收起​

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/308453475b628a4834dd69c54dd1c78d_MD5.jpg]]

匿名用户

最近在做这方面的期末展示，我就不自量力地来抛砖引玉一下吧～

所谓分岔，指的是在参数变化时，动力系统轨线在不动点附近的拓扑性质发生的变化。

具体一点说，Hopf分岔发生的条件是参数在某区间变化时，在不动点附近做线性近似时的Jacobi矩阵存在一对共轭虚特征值，且参数u在us附近变化时，这两个特征值实部从负变正穿过虚轴。在加上一些技术性的条件（比如光滑性等等）后，不动点会从稳定吸引子变化成不稳定不动点。具体又细分为supercritical与subcritical（当然，还有degenerate case）的情况，前者在u越过分岔点us后轨线会吸引到一个从不动点处“生成”的稳定极限环中，后者会伴随着一个不稳定极限环消失，轨线趋向远处的吸引子。它有可能是远处的不动点、半径很大的极限环或者（在高维情况下）混沌吸引子。

建议对动力系统方面有兴趣的初学者读一下Strogatz写的《Nonlinear Dynamics and Chaos》。

[编辑于 2015-06-15 23:44](https://www.zhihu.com/question/26359793/answer/51336196)

​赞同 30​​1 条评论​收藏​喜欢

​

![[Omnivore/(99+ 封私信 / 7 条消息) 有没有人能解释一下霍普夫分歧Hopf bifurcation- - 知乎/attachments/308453475b628a4834dd69c54dd1c78d_MD5.jpg]]

匿名用户

霍普夫分岔是指系统参数变化经过临界值时，平衡点由稳定变为不稳定并从中生长出极限环。它是一种比较简单而又重要的动态分岔问题，不仅在动态分岔研究和极限环研究中有理论价值，而且与工程中自激振动的产生有着密切联系，是工程中常见的现象。

知网上有相关博士论文。

[发布于 2014-12-08 21:07](https://www.zhihu.com/question/26359793/answer/34778487)

​赞同 10​​添加评论​收藏​喜欢

​

