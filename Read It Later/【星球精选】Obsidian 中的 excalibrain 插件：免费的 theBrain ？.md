---
date: 2025-12-20T18:26:20+08:00
url: https://mp.weixin.qq.com/s?__biz=MzIyODI1MzYyNA==&mid=2653542976&idx=1&sn=8b69cfb8b684f67850e3dbd98e927b70&chksm=f389b097c4fe398197ad4e9cdde5a427f0ba3613776dd8d3ea097f63c0ce3033e23edc31cb4c&scene=27
status: readed
---
原创 王树义老师 [玉树芝兰](https://mp.weixin.qq.com/)

*2022年5月17日 11:43* *天津*

本文选自知识星球「玉树芝兰」精华文章列表，分享给你。部分内容有改动。  
![[Read It Later/attachments/de57ea067a9c2c3ae4fa44df27acb119_MD5.webp]]

本星球嘉宾之一**永锡老师**总是爱给我安利新的应用。有一款应用不是很新，可他还是不止一次撺掇我去买，那就是 theBrain 。

其实，theBrain 我还真尝试过，那是在 2020 年的 6 月。当时有读者在我的文章后面留言，推荐过这款工具。

下图是我当时尝试的效果。

![[Read It Later/attachments/529e816a1f2c0f51056634dfbb492f6d_MD5.webp]]

这种动态展示局部网状链接图的能力，让我爱不释手。不过很快我就决定弃用了。

最重要的原因，当然是**缺钱**。

![[Read It Later/attachments/87ef5b8f0011f1c6f07497a10420de07_MD5.webp]]

除了价格高昂以外，更要命的问题在于彼时 theBrain **导入导出格式受限**。我对于导出格式要求比较高。因为你要是真的想重器轻用，就必须得保证一款应用和其他软件应用之间能够通过**标准化的格式进行数据的交换**。

根据我那时测试的结果，theBrain 导出格式可以是 txt，可惜导出的效果是这个样子的。

![[Read It Later/attachments/365c584b00808ac093b8cc12e99599d4_MD5.webp]]

这样一来，如果我需要和其他工具交互，还得对格式进行脚本调整。实在有些麻烦。

不过最近看到许多朋友，都很喜欢用 theBrain，包括张玉新老师和 pimgeek 等人在 直播视频里面的演示，不免又蠢蠢欲动。

![[Read It Later/attachments/11136b4656c14731dc66311a9c1c4125_MD5.gif]]

当我听说，Zsolt Viczián 做了个 Obsidian 上的插件，可以实现类似于 theBrain 效果的时候，不由得非常欣喜。

![[Read It Later/attachments/2b6bd3af4851810411a25d4ee05b3a4a_MD5.webp]]

这款插件的名称，叫做 excalibrain，github 页面在这里。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这篇文章，我来带你看看，它好不好使。

先来看看安装的方式。

首先，你需要到 community plugin 里面下载安装以下几个插件：

- obsidian42 BRAT
- Dataview
- Excalidraw

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

依次安装后，通过 Cmd + p 快捷键呼叫命令菜单，选择下面这个 `Add a beta plugin for testing`。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

然后 Obsidian 会有提示，问你安装哪个测试插件。输入 `zsviczian/excalibrain` 即可。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

安装成功之后，提示是这样的。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

因为是社区插件，所以你**需要手动开启它**。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

为了避免麻烦，我干脆选择重启了一遍 Obsidian，然后呼叫菜单，选择 Open ExcaliBrain 。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

此时 excalibrain 的界面就出现了。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

注意如果你跟我一样，是全新安装，那么可能会遇到一个问题，就是你每次在这个网状图上点击节点，都会新开一个页面 (Pane)，导致你的浏览过程伴随着大量笔记充斥屏幕，同时网状图被压缩再压缩直到看不清内容，观感很糟糕。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

解决办法嘛，一开始我绕了点儿弯路，选择了 hover editor，把 excalibrain 作为悬浮窗口处理。后来发现，其实根本不需要安装这个东西。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

点击节点链接，是否在新页面打开，设置不在 excalibrain 里，而是 excalidraw 插件当中。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

如图所示，上面这个开关默认关闭，只需要把它开启就行。

此时咱们来看看效果。

我们点击某个节点，对应的页面就可以显示出来。由于网状链接绘图使用的是 excalidraw ，因此你可以非常容易对这张图进行缩放、拖动等操作。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

这里你可以注意到，左上角菜单栏有个「附件」按钮，一旦点按下去，就可以把某则笔记里面的全部附件都显示出来。当然，你如果觉得这样太乱，可以保持该选项的关闭。

同样的设定，还包括了若干种其他节点类型是否显示。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

我们还可以从页面这一端进行操作，跳转到其他其他笔记之后，相应的 excalibrain 视图也会改变。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

如果你很熟悉 Obsidian ，可能会疑惑，这种网状链接结构图，和 Obsidian 自带的 local graph 不是一码事吗？

下面咱们就来对比一下，二者的区别。

我们可以打开某篇笔记（此处的例子是笔记库中的 Obsidian 图片的处理 这一则）。我们同时开启 excalibrain 和 local graph，这是默认视图下，两者的对比。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

可以看到，excalibrain 的内容，比 local graph 要丰富许多。

但是，这种对比显然并不公平。因为默认的状态下，Obsidian 其实只显示了某则笔记最紧密链接的那些节点。这是可以调整的。

下面我们调整 depth 参数，你可以看到 local graph 里，更多关联笔记显现出来了。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

然而可以看到，local graph 里面的节点排布只是显示出来链接关系，却没有能够对节点的关联类别进行自动梳理。

excalibrain 则不然。下面这张图，展现了黄色主节点的几种关联关系。我为你圈出来了 3 个框。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

左上方是 parents ，父节点。也就是这些节点里面，具有指向当前节点的链接；

左下方是 children，子节点。这些链接出现在当前节点笔记中；

右侧的是 sibiling ，兄弟节点。这些节点与当前笔记「本是同根生」，共同出现在了某个父节点里面。至于是哪个，都有具体的链接作为线索。

从结构上来讲，excalibrain 这种表示方法，更能够让用户区分清楚节点之间的关联，并且在进行跳转的时候有章可循。

Zsolt 自己的视频，把这个节点链接类型问题讲得很详细。你可以 点击这个链接查看。

虽然比起来 theBrain，excalibrain 非常稚嫩。目前的版本还在 0.0.x 阶段，功能上与成熟的商业化软件 theBrain 相差很远。例如缺乏更多的视图，也没能在链接上提供属性值...... 但是无可否认，excalibrain 也有自己独特的优势。

最大的优势，在于**开放和免费**。这款插件代码，你可以直接在 Github 上查看代码。如果你自己有编程能力，那么可以魔改出各种独有的功能，适应自己的场景。

其次，因为底层基于 Obsidian，所以你不用担心它的基础和开放性。毕竟，Obsidian 就是一堆 Markdown ，和其他工具交互起来，已经是最为简单省事了。  

  

如果你正在用 Obsidian，在知识网络中跳转的时候，也感受过迷茫，或者羡慕 theBrain 的功能，那不妨也来尝试一下，这款有趣的插件。

篇幅所限，就连 excalibrain 目前已有功能，我也有许多没有介绍到。例如说对 Tag 的支持，以及 Folder 节点的显示 / 隐藏等。插件的设置中，有很多都是可以调整的。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

你可以在 看过 Zsolt 最新的这个介绍视频后，自己尝试一下调整不同标签颜色等设置，看看效果。就当成一次有趣的探险吧。

你觉得这款向 theBrain 致敬的 Obsidian 插件怎么样？是否能满足你游览「数字花园」的需求？欢迎你把自己尝试的结果，在留言区分享给大伙儿。咱们一起交流讨论。

感觉有用的话，**点赞 +「在看」**，把它**转发**给你身边有需要的朋友。

请**订阅**我的微信公众号，**加星标**，避免错过新推送提示。

欢迎关注我的视频号，时常更新。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

欢迎来知识星球，查看已经积累下的数十篇精华帖子。更欢迎你提出自己的好问题。

![图片](https://mp.weixin.qq.com/www.w3.org/2000/svg'%20xmlns:xlink='http://www.w3.org/1999/xlink'%3E%3Ctitle%3E%3C/title%3E%3Cg%20stroke='none'%20stroke-width='1'%20fill='none'%20fill-rule='evenodd'%20fill-opacity='0'%3E%3Cg%20transform='translate(-249.000000,%20-126.000000)'%20fill='%23FFFFFF'%3E%3Crect%20x='249'%20y='126'%20width='1'%20height='1'%3E%3C/rect%3E%3C/g%3E%3C/g%3E%3C/svg%3E)

由于微信公众平台的限制，文中部分链接可能无法正常显示与跳转。如需访问，请点击文末「阅读原文」链接，查看链接齐备的版本。 

## 延伸阅读

- [如何在 Python 绘图中正常显示中文？（视频教程）](https://mp.weixin.qq.com/s?__biz=MzIyODI1MzYyNA==&mid=2653542359&idx=1&sn=9514976495b2365f7ce0e679338d96e4&scene=21#wechat_redirect)
- [如何更高效用 Roam？免费分享 Roam Untangled 作者 Jamie Miles 的几个小技巧](https://mp.weixin.qq.com/s?__biz=MzIyODI1MzYyNA==&mid=2653541855&idx=1&sn=2e0eb37bfcd0a9d1f03d2b80fec571f9&scene=21#wechat_redirect)
- [如何用 Python 和 BERT 做多标签（multi-label）文本分类？](http://mp.weixin.qq.com/s?__biz=MzIyODI1MzYyNA==&mid=2653540586&idx=1&sn=6f32b5dd3e8104dc48832b09e8ab7d91&chksm=f389ba3dc4fe332b3af6591cbe4d5eefeb2ac28bdfc16adc79a6fd652c71ffa1de24aba08333&scene=21#wechat_redirect)
- [如何安装 Python 运行环境 Anaconda？（视频教程）](https://mp.weixin.qq.com/s?__biz=MzIyODI1MzYyNA==&mid=2653540340&idx=1&sn=cf1a9b6de29183e6bc3a62b2e7a5e2b6&scene=21#wechat_redirect)
- [如何用 Python 可视化《三国》人物与兵器出现频率？（视频教程）](http://mp.weixin.qq.com/s?__biz=MzIyODI1MzYyNA==&mid=2653540413&idx=1&sn=f2fcbb2d632022bd563bd30bb6225259&chksm=f389baeac4fe33fc8e215a00e47212f08ff3f06b7698c5871aeb084097737b649d38824e1eea&scene=21#wechat_redirect)