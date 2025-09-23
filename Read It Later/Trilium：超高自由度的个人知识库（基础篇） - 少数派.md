---
date: 2025-09-23T12:36:04+08:00
url: https://sspai.com/post/59739
status: readed
---
![](https://cdnfile.sspai.com/2020/03/30/ca91504d98e2129dd5315a34244569aa.png?imageMogr2/auto-orient/thumbnail/!1420x708r/gravity/center/crop/1420x708/format/webp/ignore-error/1)

Trilium：超高自由度的个人知识库（基础篇）

[![idelem](https://cdnfile.sspai.com/2022/04/01/8458898619fdabafee62acae1b14ce3f.jpeg?imageMogr2/auto-orient/thumbnail/!72x72r/gravity/center/crop/72x72/format/webp/ignore-error/1)](https://sspai.com/u/idelem/updates)

[

idelem

](https://sspai.com/u/idelem/updates)

2020/03/30 21:22

### 简介

不久前，我在 Github 上乱逛的时候偶然发现了 [Trilium](https://github.com/zadam/trilium)，根据主页的介绍，这是一个基于 electron、跨平台的分层级笔记应用，主要使用场景是建立个人知识库，或者说个人维基。

「噢，分层级的知识库啊，估计又是一个印象笔记吧……」

这么说着，我还是打开 release 页面喜加一了，毕竟作为这个网站的用户，怎么可能不喜欢玩弄新工具呢。

然而，那天就是沉沦的开始。及至今日，我不仅把个人知识库搬了进来，甚至手头的创作项目也迁移到 Trilium，还亲手搭建了自己的同步服务器；眼下，更是在 Trilium 的笔记编辑界面上，写下了这篇安利文章。

因为，Trilium 远不止一个合格的笔记应用。正如标题所说，它的美妙之处，可以让我不吝用「超高自由度」来形容。Trilium 在国内似乎知者寥寥，未免太可惜了一点，因此就动了写文章介绍的念头。我觉得，它应该可以满足你们当中最变态的工具控对笔记应用的一切狂想。

### 基础

由于 Trilium 的功能和使用细节相当多，不得不把介绍文章拆成几部分。在深入窥探那些美妙的扩展功能之前，本篇将介绍 Trilium 最基础的笔记功能。

初次下载后，打开应用，看到的是这样一个界面——开发者准备的示例文档：

![](https://cdnfile.sspai.com/2020/10/06/aadc7c6158f53e6c7da360b13d69bb6c.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

Trilium 的界面并不是最让人惊艳的，但足够轻盈简洁，能让信息不受阻碍直接呈现在眼前。

左边是一棵无限嵌套的文档树，中间是笔记编辑区域，右边则是当前笔记的信息，包括笔记标签和关联笔记图表等。

### 结构：文档树、分支和笔记

对文档树的管理，应该算是 Trilium 的特色功能之一了。和一些大纲应用类似，它没有「文件夹」的概念，一切节点只是不同类型的「笔记」。如果一则笔记内容空白，就会在页面上显示所有属于它的「子笔记」，看起来确实很适合作为知识库的结构：

![](https://cdnfile.sspai.com/2020/03/30/86d697bdd97cd42e993f4d75ebbfa10a.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

请输入图片标题

当然，无限层级文档树的概念并不新鲜，像 Workflowy 等大纲笔记应用和 Scrivener这样的写作软件早就实现过了。于是 Trilium 又提出了「克隆」和「分支」——同一则笔记可以被「克隆」到不同的父节点下面，拥有多条路径，每条路径就被称作一个「分支」。

这样一来，在构筑知识库时，一个知识点也可以归属于多个分类，不用非此即彼，也不用复制一份到别处。开发者在 Github Wiki 上放了个 gif 来说明：

![](https://cdnfile.sspai.com/2020/10/06/15717b98de2f426f475023f0d7aae9b6.gif)

实际应用中，更是可以**把资料存档于一个节点下，然后在别的节点引用资料随时参考**。Trilium 里的 `Ctrl+C` 复制操作默认就是克隆笔记，如果要制作独立的副本，需要用到 Duplicate。

### 内容：富文本加 Markdown

Trilium 的笔记编辑部分用的是富文本编辑器 [CKEditor](https://ckeditor.com/)，但也支持粘贴 Markdown 为富文本格式，可导出 Markdown，还可以使用部分 Markdown 语法作为快捷输入方式。对我这个 Markdown 多年老用户来说，可以说是相当友好，几乎没感到转换的痛苦。所见即所得有什么不好，只要能无缝和别的笔记应用交互就可以。

只是 CKEditor 有个硬伤：还不支持输入数学公式。所以我到目前为止都是在别的地方截图或导出 svg 凑合一下。

在其他方面，如表格、上下标、高亮等格式的处理上，富文本还是略胜 Markdown 一筹，比如可以用上不同颜色的高亮，修改字体颜色等，满足基本的笔记编辑需求应该不成问题。

### 多媒体和文件管理

Trilium 的文件管理并不依赖外部目录，而是统一整合在一个数据库里，所以支持在笔记下嵌套图片、文件和其他多媒体资源。这种管理方式有利有弊，不过带来了一个显著的好处，那就是在不同平台间同步时，完全不用顾虑引用资源的路径问题。而这个设计在接下来要谈到的插件系统中发挥了至关重要的作用。

### 备份和版本历史记录

为防止笔记丢失，每过一段时间（具体间隔可以自行设置），Trilium 会保存一份当前笔记的快照，可以通过右侧边栏的 Note Revisions 查看。

笔记的历史版本可能会占据较大空间，所以支持删除单个版本，或彻底关掉历史版本功能——在笔记的 attributes 里加入 `disableVersioning` 这个标签即可。有关 attributes 的详细解释将在「进阶篇」中说明。

除此之外，Trilium 也会对整个数据库进行定期备份，保存在数据目录里。各个操作系统上数据目录的路径如下：

- Linux: `/home/[user]/.local/share`
- Windows Vista 及以上: `C:\Users\[user]\AppData\Roaming`
- MacOS: `/Users/[user]/Library/Application Support`
- 如果以上路径不存在，就在用户的主目录里，也就是 `~`
![](https://cdnfile.sspai.com/2020/10/06/4f9ae444e385c3a6c1fda0136ac90214.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

### 加密笔记

笔记默认是不加密的，要给单篇笔记加上密码，可以点击标题栏的「盾牌」图标进入 Protected Session。弹出的对话框会要求你输入一个密码，之后访问该笔记就都需要密码才能继续。

Trilium 会用这个密码**对笔记全文进行加密**，也就是说，就算有人拿到了笔记数据库，在不知道密码的情况下，也无法查看内容。

![](https://cdnfile.sspai.com/2020/10/06/a05eb860c8650bff65c3774800e01476.gif)

### 网页剪辑插件

在基础篇的最后，要介绍一下通过 Trilium API 实现的 Chrome 和 Firefox 插件：[Trilium Web Clipper](https://chrome.google.com/webstore/detail/trilium-web-clipper/dfhgmnfclbebfobmblelddiejjcijbjm)（[源码](https://github.com/zadam/trilium-web-clipper)）。

![](https://cdnfile.sspai.com/2020/10/06/ed17b21ec5bfdcafc23ad455547b6554.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

这个插件可以做到：

- 截图
- 保存整个网页包括图片
- 快速创建文本笔记
- 选中网页文字剪藏

新创建的笔记默认放在当日日记（在进阶篇中会介绍）下面，但也可以建立一个新笔记并带上 `@clipperInbox` 标签，该笔记就会变成剪藏笔记的根目录。同一天在同一个网址剪藏的文字都会放在同一个笔记下。

### 接下来……

预计会在进阶篇介绍的内容：

- 笔记之间的关系和链接图谱（思维导图、相似笔记）
- 自托管同步和 web 客户端（可在移动端使用）
- 强大的 attributes 系统
- 日记/日报/任务管理系统
- 自定义 javascript 插件
- 静态页面应用部署（如统计图表）
- 自定义 API76

34

[#笔记应用](https://sspai.com/tag/%E7%AC%94%E8%AE%B0%E5%BA%94%E7%94%A8)

[#知识管理](https://sspai.com/tag/%E7%9F%A5%E8%AF%86%E7%AE%A1%E7%90%86)

[#应用推荐](https://sspai.com/tag/%E5%BA%94%E7%94%A8%E6%8E%A8%E8%8D%90)

76

等 76 人为本文章充电

[![idelem](https://cdnfile.sspai.com/2022/04/01/8458898619fdabafee62acae1b14ce3f.jpeg?imageMogr2/auto-orient/thumbnail/!84x84r/gravity/center/crop/84x84/format/webp/ignore-error/1)](https://sspai.com/u/idelem/updates)

[

idelem

](https://sspai.com/u/idelem/updates)

还没有介绍自己

全部评论(34)

![[Read It Later/attachments/84e04d9a6b34c9f4caa6066b9ef610a3_MD5.png]]

请在登录后评论...

更多

推荐阅读[

](https://mp.weixin.qq.com/mp/profile_ext?action=home&__biz=MzU4Mjg3MDAyMQ==&subscene=0#wechat_redirect)[下载 App](https://sspai.com/page/client) [联系我们](https://sspai.com/post/) [商务合作](https://sspai.com/page/bussiness) [关于我们](https://sspai.com/page/about-us) [用户协议](https://sspai.com/page/agreement)

© 2013-2025 深圳市烧麦网络科技有限公司 - 少数派[粤ICP备09128966号-4](https://beian.miit.gov.cn/) | [粤B2-20211534](https://dxzhgl.miit.gov.cn/)

 

❌ 未收藏