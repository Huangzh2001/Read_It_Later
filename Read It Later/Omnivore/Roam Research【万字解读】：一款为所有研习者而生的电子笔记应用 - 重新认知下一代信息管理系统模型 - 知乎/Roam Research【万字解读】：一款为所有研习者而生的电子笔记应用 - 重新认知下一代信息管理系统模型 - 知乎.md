---
id: a946bd80-e40d-459c-8353-057699acdda4

url: https://zhuanlan.zhihu.com/p/708786002
---


tags:: 

# Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 | 重新认知下一代信息管理系统模型 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/roam-research-190b9e10c42)
[Read Original](https://zhuanlan.zhihu.com/p/708786002)

## 仙那度计划 (Project Xanadu) | 双链简史

> _本文正式开始之前，让我们回到故事的原点——追溯双向链接的历史，找寻永恒记忆宫殿的遗址_

### _上都启示录：超链接（Hypertext）缘起_

_一切的一切，始于信息技术先驱 Ted Nelson（泰德 · 尼尔森）内心深处的愿景——**一个能够在数字世界关联一切事物的电脑文件系统**。最初，Nelson 的构思是建造一个数字资源库——以承载全世界范围内的所有电子出版物。_

_那之后，他将心目中关于这一想法的企划正式命名为**Project Xanadu**「上都计划」。_

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/f346c1b8123d81c2f12ae1b6ab6e4297_MD5.jpg]]

尼尔森最初定义了「超文本」的概念

> _1965 年，Nelson 把他的想法诉诸于论文之上，并提交给了计算机协会（ACM）。_

###   _范式：Xanadoc | Xanadu Space_

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/994b643a70ade225d7982fa6303b75a0_MD5.jpg]]

这是一篇关于宇宙学的文档，由其他文献中的段落共同组成

> _感兴趣的朋友可自行访问_ _[Xanadoc](https://link.zhihu.com/?target=https%3A//sspai.com/link%3Ftarget%3Dhttps%253A%252F%252Fxanadu.com%252Fxanademos%252FMoeJusteOrigins.html)_ 或者观看 Nelson 发布的示范 [Demo](https://link.zhihu.com/?target=https%3A//sspai.com/link%3Ftarget%3Dhttps%253A%252F%252Fwww.youtube.com%252Fwatch%253Fv%253DEn%5F2T7KH6RA)

### _失落的仙那度 | 万维网（World-Wide-Web）远非世外桃源_

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/40fdbbe510d4dd44ea03be404a4ad1f2_MD5.jpg]]

尼尔森不认同多数人对于「所见即所得」的看法

不难看出，Nelson 本人并不认可如今的万维网——他认为所谓的「所见即所得」，不过是局限在传统打印文件里的说法。

也就是说，一切计算机文档都是无互动性可言的，既不能被标注，也不允许插入（外部链接）——好比压在玻璃下的报纸，是可望而不可即的。

> 因此，当下的人们亟需一个可以关联所有文档的笔记工具，以满足信息时代下日益增长的个人知识储备。

---

### Roam Research：属于前方朝圣者的福音 | Project Xanadu 原教旨之十二

**1.每一位用户都是独一无二且属安全认证的：**

在 Roam 里，每一个云端库（Hosted Graph）都是独有且私有的。

_ps：仅在创建图库阶段，可以将其设置为独立加密类型_

**2.每一位用户可自行搜索，检索，创建以及存储文档**

每一位用户（编辑权限）可自行搜索，检索，创建以及存储区块（Block）和页面（Page）。

**3.每一份文档可由任何数据类型的任意数量部分组成**

Roam 的 Block 可由相当数量的不同数据文件组成，类型如下：

* 文本（text）、图像（image），音视频（audio/video）
* PDF文件、网页（web page）
* 看板（kanban）、表格（table）
* 画板（drawing board）
* 白板工具（excalidraw）
* 思维导图（diagram）

**4.每一份文档可包含任意类型的链接，包括系统所有者可访问的任何文档的虚拟拷贝（转包）**

* 每一个区块可包含任意类型块的引用，包括图库所有者可访问的任何区块的虚拟拷贝（嵌入）

**5.链接是可见，且可从所有端点处出发跟踪**

* 块引用是公开的，且能从所有引用过原区块的区块处反向跟踪

**6.每一份文档都是独一无二且安全认证的**

* 每一个区块都是独一无二且由双重标识（Private ID/Public ID）进行识别——每一页 Page 在命名空间（Namespace）的标题（Title）都是唯一的
* 对于云端加密库而言，每一个块（页面）引用都经由自动加密处理
* _特殊地，桌面端应用上的离线本地库无法加密由用户上传的图像等媒体附件_

**7.每一份文档都具备安全的访问控制**

* 每一份页面都可以被共享给任何人，或具备阅读/编辑（read/edit）的账号邮箱
* _特殊地，共享独立页面将加载部分图库（Graph）的数据到任何一位访问者的浏览器上_

> _因此，**对于一位别有用心且精于钻研的人来说，他将可以从某一页面访问图库**_

**8.每一份文档都可以进行快速搜索，存储以及检索，并且无须考虑其物理意义上的存储位置**

* 每一个区块（文本/字符串）都可以进行快速搜索，存储（仅限于 Page）以及检索，并且无须考虑后端数据库的存储问题

**9.每一份文档根据来自任意地点的访问频率，自动迁移到最合适的物理存储区**

* 每一个区块涉及到的最近编辑数据，都以 EDN 格式扁平化存储为一系列简易数据集，并储存在本地缓存中
* 除此之外，对于无加密的云端库来说，还能够以离线的形式直接访问
* 警告：删除本地缓存将导致尚未同步的数据丢失
* 而对于任何共享了访问权限（阅读/编辑）的人来说，图库数据将加载至他们的浏览器上

**10.每一份文档都有作自动冗余存储，即使在意外情况下也能保持可用性**

* **_仅对本地库而言，如果尝试清除本地存储，那么此举将即刻删除掉该浏览器上的所有图库_**
* _建议：用户方应自行设置好定期备份，以避免重要数据的损失_
* 对于任何共享了访问权限（阅读/编辑）的人来说，都可以将图库整体导出为以下格式
* MarkDown
* MarkDown
* JSON
* EDN

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/eb5caf029551e6ff881f936f2c1d01eb_MD5.jpg]]

Roam 支持 4 种格式的整库导出

**11.每一项事务都是保密且可由组成事务的部分（文档源）进行单独审计的**

* 每一项事务都默认存储在与之对于的属性列表当中；每一项事务都仅可由共享相同事务ID的区块进行审计查询
* 此外，仅限于云端库而言，所有区块的类型内容（含图像等媒体附件）同数据集（非必要的元数据外）一样——均可经由加密处理
* 常见的上传附件 (Uploads)：图像、音视频、还有 PDF 文件；一些非必要元数据 (Non-Necessary Metadata) 不会被加密：
* 节点形式（无序/有序/文档）
* 标题水平以及文本调整情况（居左/居中/居右）等
* 所有 Blocks 的关键数据将被加密：
* 各个用户的昵称/邮箱
* 以及创建该区块的用户信息（昵称/邮箱）
* 还有页面标题，图像链接等

**12.Xanadu 客户端通讯协议是符合开源公布标准的；因此，涉及到第三方软件的开发与集成是被允许且支持的**

* 在 Roam 中，涉及到第三方插件的开发和集成式被允许且支持的

> 用户方甚至可以直接在特定的页面或区块下方，自行修改定义图库样式 (Graph's CSS)， 以及 JS

举例来说：油管视频（嵌入式）的 Comment Button 的样式修改

```css
{
  background-color: white;
    right: 0;
    left: 98%;
    top: 95%;
    bottom: 0;
    z-index: 2;
    opacity: .8;
    position: absolute;
    border-top-left-radius: 7px;
}
```

_类似的设置，都是可以直接在 Graph 里由用户方自行定义的_

---

> 知识图谱 Roam Graph：非线性大纲笔记——打破传统文件柜的桎梏

对于非线性的网状形成，不只是页面与页面之间的联系，更要有任意段落的粒度参与。

## 跳出文档柜的层级藩篱，打造第二大脑的数字城堡

每一页 Page 都是 Graph 这座森林中的一棵树，而所有的 Blocks 则充当枝干和树叶的形式。

```markdown
[[Page]]
* Branch
  * Branch
    * Leaf
    * Leaf
  * Leaf
  * Branch
    * Branch
      * Leaf
* Branch
  * Leaf
...
```

事实上，Page 和 Block 并没有本质上的区别，Page 只不过是一类特殊的 Block ——作为视图 (Graph Overview) 上独立且直观的节点；换句话说，Page 即是不存在父级节点 (Parent Node) 的区块。

> 更形象地说，Pages 与 Blocks 之间的关系基本可视作为正方形与长方形（前者为独立的个体，通常由后者组成）。

### 不只是树叶的繁荣，也要有花朵般的点缀

* **标题树** \[\[title\]\]

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/970183a6e9ea3a40caa3768544b6a06d_MD5.jpg]]

标题粒度

 使用\[\[\]\]（双中括号）引用的 Pages，具备相对宽泛的节点粒度；如同森林里的树木，高矮胖瘦，各有不同。

> 顺便说一句，区块 (Blocks) 在粒度的定义上理应是“最自由自在的”。

* **标签垛** #tag

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/4ad778574e6b66196ddf26751d44b8af_MD5.jpg]]

标签粒度

紧挨着 #（井号）的 Page 引用通常具备较小的节点粒度，这类标签常用于标记 Block(s) 在内容上可能涉及到的概念/范畴。

* **堆垛** #tag/sub-tag

对于递进式的标签链接，它们更接近于「堆垛」的状态。

> _只有当该标签（含子标签）相对于独立标签是不可分割的，才以“多步标签 (Multi-step label)”的形式引用_。

如果还是不能很好的 Get 到这一块的内容，可通过以下内容来理解：

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/807921a1a55873cfdda50e9eaa75995f_MD5.jpg]]

上图为O2（氧分子），下图为O3（臭氧分子）

> 如图，两种分子都属于是氧元素的单质类型。不同的点在于臭氧分子比之氧分子多出了一个氧原子——因此说臭氧在形态上更进一步。

* **属性核** attribute::

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/e5d0ac2fbe9c7ed9f29599e536d42bd9_MD5.jpg]]

属性粒度

attribute:: 与 #tag 相似，但在细粒程度上更加具体，普遍用来概括（涵盖）一类拥有共同特征（特性）的的人/事/物。

例如：作者/邮箱 (Author/Email)

```less
Author:: Mac Arthur
Email:: macarthur@gmail.com
```

* **种子**/**果核**

> 简单来说，attribute::不仅可以用于描述一类具体的属性，还能用来概括具备同一特点的不同事物。

```mizar
Forest
* Apple:: This is an apple
  * AppleCore:: An apple core

* Banana::
  * BananaSeed:: A banana seed
  * BananaSeed:: A banana seed
  * BananaSeed:: A banana seed

* Pear:: This is a pear
```

通用格式：

```mizar
- attribute:: outline 
    - sub-attr-1:: detail
    - sub-attr-2:: detail
    - sub-attr-3:: detail
```

> 简而言之，一切与属性相关的数据，更接近于“元数据 (Metadata)”的概念。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/370b9f6b8eeac267ee24818ed159d89b_MD5.png]]

可见，该集合{1,2,3,4}中的各元素均满足同一特征 φ∈N\*

用集合表达式来理解的话，attribute::更接近于左侧对于 φ 的属性定义（特点/类别）；右侧则是双冒号::之后的具体（多数）对象。

而在 Roam 中，具备相同（近似）属性/属于相同（近似）类型，则可由 attribute:: 来定义或包含。

* **内联标题**\[\[\[\[inline\]\]outline\]\]

> 标题中的标题：洋葱头，番石榴，柚子

_除了上述三类引用，Page 还可以作为任意粒度的独立节点（相对于 Block 而言）——此类 Page 可以在标题的命名空间 (Namespace) 处内联其他 Page 的 Title，来进一步「增殖」该 Page 的节点粒度_。

```markdown
Guava: [[[[seed]][[flesh]]]]
```

可见，Guava 通过前后内联其他 Page，使得原本的节点粒度进一步「增生」。

---

## 根系发达，枝头发芽

ps：枝头即 Headings，需要区别于页面标题 Title

### 世界上不存在两片完全相同的叶子

_如果说，每一页 Page 都是一棵树，那么它的根须将可以与不同的 Pages 相连——**它们之中的 Blocks 既是具备营养的花蜜果肉；也是充当养分的化肥颗粒；更是洞见灵感 (Insight) 的花种果核**。_

而为了保证这样一幅“营养-养分”网络系统的自身稳定，Roam 不仅为每一个 Block (包括 Page 在内) 分配有独一无二的双重 ID，还在页面标题的命名上，采取了「非唯一则合并」的维稳手段。

对于页面标题的（重）命名，Roam 只允许同时存在一份同名 Page，并在内容上合并二者。

### 良好的开端，是成功的一半

> _每一页 Page 下的 Top-level Blocks，通常作为 Headings 存在_。

正如本章开头所提及的，Graph 本身像是一座大林场。每一页 Page 即是一棵 Tree，而这些 Top-level Blocks 则是树上的主要枝干，起到统领全文，提纲挈领的重要作用。

它们常以各级标题的形式出现，如一级/二级/三级标题：

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/6984e9425a53fd88afff8b9f5d136aa8_MD5.png]]

Roam 仅支持三级标题

而这些 Top-level Blocks 都将 Page 视作唯一的父级节点；且 Top-level Blocks 不只是作为 Page 的直属（后代）节点，同时还是各段落的起首节点。

> 尽管标题水平 (Heading Level) 与节点当前所处的层级无关，但还是十分建议将 Heading Blocks 与线性的层级关系相匹配。

注：heading 仅作为一个 Blocks 的可选项（相对于 Pages 的 Title）

## 附庸的附庸不是我的附庸

一般来说，当把 ((block ref)) 置于某处时，该引用仅显示当前块的命名空间 (Namespace) 里的内容。

> 那么块引用 ((block ref)) 与嵌入 {{embed:((block ref))}} 间的区别又何在呢？

### 全文式索引的块引用

通俗地说，块引用是仅包含自身的；除非嵌入该引用，否则节点将视作从原本的层级关系中「抽离」出来而变得无法展开的。

_只有当块引用被置于嵌入块内，即_ _{{embed:((block ref))}}，才能够展开/收缩其下属的后代节点——**之所以将块引用称作【全文式索引】的缘故，正是因为**_ _((block ref))_ _**总是指向被引用块的位置以及包含一个直属子级节点的属性列表**_。

> 换句话说，只有被嵌入的 Block(s)，才能「串联」起各个层级的后代节点，进而形成完整的 Branches 系列。

### 定位原区块的导航栏

左键位于左侧的 Bullet Node，将 Zoom-in 到当前区块（段落），或者在按住 Shift 键的同时左键节点，则可在右侧 Sidebar 处打开当前区块的“视窗口”；

而不管使用哪一种方式打开，都始终存在一个 Breadcrumb 导航栏指向当前节点的先代节点——这是因为所有节点的 ((block ref)) 都将默认存储在其所有后代的属性列表当中。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/2f957514f4a0e2b1568cd55053aeb2cb_MD5.png]]

Breadcrumb 导览器

### 引用上下文的位置框

同样，左键位于视窗口顶部的（任一）先代节点，即可展示对应层级的上下文内容——此时，会出现一个“黄色边框的盒子”来「突出」原区块的位置。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/aa14227e5315f59768a11a95c2a15e2f_MD5.jpg]]

在右侧 Sidebar 处 Zoom in 当前区块

> 简而言之，你进入的层级越高，那么你将看到越多的上下文。

---

## 半场总结

综上所述，Roam 的双向链接 (Bi-Directional Liking) 足以证明涉及到整个 Graph 中的不同 Page/Block(s) 之间的链接是高度可靠的，且能在足够宽泛的粒度范畴内深度「反向追踪」。

> 【可溯源性】在设计上应当高于【延展性】

### 前段概要

> _现在，让我们再次回顾一下目前提及的**功能特性**_

1. Page 对应不同节点粒度区间的基本引用形式：\[\[title\]\]/#tag/attribute::
2. Page Title 命名的全局唯一性——Block Ref 同样具有潜在的唯一性
3. Block Ref 引用的全文式索引
4. 任一 Block 的 Breadcrumb 导航栏

可以说，Roam 在节点内容的粒度上没有任何限制，也支持上传各种类型的资源文件——除了文本，块引用本身还能展示图像，音视频等外部链接的内容。

> 在下文中，我们将继续探索 Roam 中的功能块 (Func-Blocks)。

---

## _奥林匹克格言：更快，更高，更强_

> _前端式数据处理_

### _Embedding：嵌入在 Graph | 跃然于纸上_

**镜像** {{embed: ((block ref))}

在 Roam 里，可以通过复制粘贴的形式，将块引用嵌入到 Graph 中的任何一个 Block 内。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/d6173fc9ca05c929fa672708c3f54cda_MD5.jpg]]

复制该 block ref 的 embed 形式

通过粘贴该嵌入块 {{embed: ((block ref))}} 到任何一处，即可复现与原区块完全一致的“镜像版本”。

**镜中镜**

> **_嵌入，嵌入，再嵌入_**

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/6889f55ac351077f7b5290760a1dbf05_MD5.jpg]]

对于原区块的重复嵌入（区别于同一区块的多次嵌入）

> 涉及到对同一区块的「多重引用」，Roam 同样能够保证 100% 的同步率以及近乎 0ms 延迟的编辑体验。

**任意门** {{embed: \[\[title\]\]}}

将嵌入块 (Embed-Block) 中的 ((block ref)) 替换成 \[\[title\]\]，以实现对于整一页 Page 的嵌入——这样一来，被嵌入的 Page 将看起来不再那么“独立”，而是变成了某一个区块的子级节点 (Children Node)。

> 实际上，对于 Page 的嵌入形式并不会使其原本“独立”的节点关系发生任何改变——你可以将这类嵌入页面 (Embed-Page) 仅看作是某种伪类的子级节点 (Pseudo-Children Node)

### Searching 或 Querying：这是一个 Mention

> 无论是搜索 (Searching) 还是查询 (Querying)，都应该以「可检索 (Retrieving) 原文并提供上下文背景」为标准来衡量返回结果 (Returns)。

**搜索** {{\[\[search\]\]: {keyword}}} 

> 搜索包含输入（关键词）的一切区块

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/5c357ffed5f71669be5c1b998a8232d5_MD5.png]]

Search-Block | 嵌入式的搜索框

在 Roam 中，你可以在某一页 Page 任意一处 Block 嵌入搜索块 (Search-Block)；然后输入关键词，即可返回所有包含「此关键词」的 Block(s)。

你还可以按一下 Show More，以展示更多返回的内容。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/78e62210af1658e9a5e33eba7889717a_MD5.jpg]]

搜索块 - 展示更多（结果）

> 理论上说，Search Block 能够返回该 Graph 中所有涉及到「此关键词」的 Block(s)

**查询** {{\[\[query\]\]: {and/or:\[\[title\]\]/((block ref))}}}

> 查询与之相关的一切区块

查询块 (Query-Block) 的功能类似，但查询的形式比起单纯的关键词搜索更加精确。

只需设置几个简单的查询条件，即可轻易返回与之相关的 Block(s)；

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/24f1d89269ed66fed6240e2935e1639d_MD5.jpg]]

通过 / 斜杠即可调出 Query 命令

* 下面来简单说明一下 Query-Block 的四类基本条件：
1. Query (and): 包括 A，B
2. Query (or): 包括 A 或 B
3. Query (and or): 包括A，包括 B 或 C
4. Query (and not): 包括A，不包括 B

1、2 命令很好理解：如果说 Query (and) 条件是要求 A 与 B 位于同一 Block 中；那么 Query (or) 则只要求二者中的一个位于某一 Block 中，即可返回满足条件的 Block(s)。

3、4 命令类似，其中 Query (and or) 比较特殊：它要求 A 位于某一 Block 的前提下，B 或 C 两者之一也位于该 Block；而 4 命令 Query (and not) 里的 not 则是把 B 设置成排除项。

> 感兴趣的朋友可以自行了解：**[How Queries Work in Roam Research](https://link.zhihu.com/?target=https%3A//www.youtube.com/watch%3Fv%3DlBmklV0n8D0%26t%3D345s)**

不难发现，Query-Block 内输入的正是 \[\[title\]\] 形式的 Page 引用。

> 当我们把标题引用 \[\[title\]\] 替换为块引用 ((block ref)) 时，Query-Block 的查询返回将同样有效！

**提及** {{\[\[mentions\]\]: \[\[title\]\]/((block ref))}} 

> 返回提及某一引用的一切区块

如果说，Search-Block 是内嵌了一个搜索框 (Search Box) 在某一 Page 内，那么 Mention-Block 则是拓展了关于其他 Page(Block) 的引用联系。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/d4f772107d1d283002d90adcf388ac12_MD5.jpg]]

\[\[@\[\[Roam Research\]\]: An Application for ALL Learner&Researcher in Contemporary to Recognizing the Next Generation of the MIS Models\]\]

> 与 Query-Block 类似，Mention-Block 也可以通过输入 ((block ref))，用作「针对」Block 级别的查询返回。

---

## **_原生应用的备份导出_** _\-_ **_简约主义的资源管理_**

### EDN: 充分完备的导出格式

对于那些习惯 All-in-One 的个人来说，无论是面对跨笔记库 (Cross-Graph) 时的数据迁移；还是为了避免云端（本地）存储遇到意外而导致的数据损失——EDN 格式的备份导出，几乎成了唯一的最佳选项！

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/5361666161655cb81e0c8beca99c7d22_MD5.jpg]]

Windows 系统中，各时间（日期）导出的 EDN 文件均可视作各个时刻的 Graph 版本

于 Roam 而言，包含 Graph 所有笔记的数据信息，全部被存储在同一份 EDN 格式文件当中——这也就意味着，最近时间的 EDN 文件即包含 Graph 在导出时刻的完整备份；至于之前时间（日期）的，则可看作是该 Graph 的历史版本。

> 也就是说，仅需导入最近时间的那一份 EDN 备份文件，即可复原整个 Graph 的全部数据信息。

**即导即出 | 镜像迁移**

EDN 作为应用程序的原生格式，无论是本地库还是云端库（包括加密库类型在内）的数据存储，都会加载到当前 Browser 的存储 (Storage) 内——真正做到了「存储在本地」的“就近原则”；因此，在导出 EDN 格式备份时，桌面端 (Desktop App) 和网页端 (Web App) 都能实现「即导即出」的即时备份。

反过来说，在新建的 Graph 中导入其他 Graph 的完整备份（仅支持 EDN 格式）时，仅有 EDN 格式的备份文件能做到最大程度上的数据复原——即在保真度上，EDN 格式备份不但可重建 Graph 整体的关系结构（各 Page/Block 之间的引用关系），还能够保留所有 Blocks 的非必要元数据 (Non-Necessary Metadata)。

> 整个导入三个数量级（100＜N＜1000）的笔记 (Page) 节点来算，所需的时间通常在一分钟以内——甚至不到 30 秒。

**全自动备份 | 历史版本**

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/466e019fc6d6f26d48d7a11b51f7e709_MD5.jpg]]

在 Roam 内，允许自行设置定期 (Every Day/Hour) 备份导出

> 通过 Roam Depot 里的插件 Page History，甚至而且更进一步的实现对单一 Page 的历史版本保留。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/02f5e883ebf872dfaa426c74d5202f69_MD5.jpg]]

右侧为版本列表，可精确到日期-时刻

### Hosting | 图床托管的灵活性

Roam Graph 通过对节点数据 (Page/Blocks) 与资源文件 (Uploads) 的分离式存储，既保证了 Graph 在加载到本地时不受媒体附件的影响，又维持了 Graph 自身数据结构的简致性——即无论上传或引入的媒体附件多少，都不会影响到 Graph 整体的结构关系。

Roam 本身提供创建本地库和云端库 (Local Graph/Hosted Graph)：

* Local Graph 支持 Uploads 存储到本地目录文件下方；

> _对于 Hosted Graph 而言，挂载在 Google Cloud 的资源文件（即媒体附件）必须在联网的前提下才能下传到本地展示；Roam 则在设置 (Settings) 处提供了后台式的图床管理服务_。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/c9b892693010ecde91fcd57e3b8ddef5_MD5.jpg]]

在 Files 界面即可统一查看所有 Uploads——在此处删除 Files 资源文件，即可将相应地删除掉云端上的备份文件

**一次外链，多处引用**

> 在 Roam 里，你只需上传一次资源文件，即可在异地 Block(s) 引用同一份附件并实现无损化复现。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/d2af68ac74f9bc8d0f17687f7feffff6_MD5.jpg]]

如果我不说，你能看出来那个是 URL 吗？

**扁平化的资源管理**

在各种资源文件的页面!\[/video/audio/PDF下方 (Linked References) 即可查看到所有对应类型的资源文件。

!\[ 是 image 类 URL 用作「展示」的<充分文本>；实际应用上，则可通过创建 .jpg/.png/.gif 等更精确的 Page 来统一查看相应格式的媒体附件。

事实上，Roam 对于文本（字符串）以外的数据均作区分化存储，使得资源文件（媒体附件）的上下传几乎不受 Graph 自身的任何影响。

> 任何挂载在线托管网站的可访问资源文件，Roam 都能快速加载至本地浏览；配合 Roam Depot 插件 Query Builder 设置简单的语法条件，甚至还能建立起高效的查询块（机制）——可锚定该资源 URL 的<网址域名>作更精细化的检索（如：查询挂载在 XX 图床上的所有图像）。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/30e2073e23b3d69c3d783e48576bf44c_MD5.jpg]]

左侧为图像显示，右侧为用作外链的 URL

> 可以说，Roam 在节点内容的粒度上没有任何限制，也支持上传各种类型的资源文件——除了文本，块引用本身还能展示图像，音视频等外部链接的内容；也就是说，对于同一份媒体文件的「复现」，Roam 能做到百分之百的利用率，进而使得整个 Graph 高度「精简」。

---

## 展望未来：一个更大的愿景 | 人人为之贡献的社区型知识图谱

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/63217e1a5e0dd30fa20de366a7922e83_MD5.jpg]]

Block 将显示最近编辑的用户名称 | Created - 创建时间 | Last-Edited 最近编辑的时刻

在 Roam 中，每一个 Block 都会保存与之相关的编辑信息。

> 在导出的 JSON 文件里，甚至可以查看到「创建账户-创建时间/编辑账户-最近编辑时刻」的相关信息；从软件开发的角度来看，存储这类数据似乎并没有什么意义——在 Graph 里的数据不都是属于用户（订阅邮箱）本人的吗？

让我们换个角度思考，Graph 何必拘泥于个人笔记内容，一个真正有助于实现个人/他人价值的社区型 Graph 应该是可以共享的，且满足于多人协作的编辑场景。

### 协作者的充分编辑权限

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/dc28a6384a51f931fd28725f04cf4738_MD5.jpg]]

在 Shared with 处添加/移除共享邮箱

**全权编辑许可**

设置为 edit 权限的共享（协作）邮箱若默认不启用 Immutable blocks 选项，协作者（编辑邮箱）将可以随意编辑/删除由 Graph 所有者（订阅邮箱）创建的全部 Blocks。

**限定导出授权**

关于导出权限，Graph 所有者（订阅邮箱）还可以设置为仅限于协助者（编辑邮箱）。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/37de57710f9c5341180683bc4f540630_MD5.jpg]]

仅限于编辑邮箱可导出 Graph 数据

> 在「全权编辑许可」与「限定导出授权」的双重加持下，协作者（编辑邮箱）可被视作 Graph 所有者以外访问权限最高的用户。

### 信任与非信任协作

**信任协作场景下的版本控制**

在共享（编辑权限）用户可信任的协作场景下，各用户可自行添加当前块的版本 (Add version)，以实现对同一位置的 Block 进行多版本编辑。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/20c0b2235240fd5ba78ee9dcbb983755_MD5.jpg]]

在同一位置添加 Block 的不同版本

**基于不可变动块的非信任协作**

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/37de57710f9c5341180683bc4f540630_MD5.jpg]]

Settings - Immutable blocks: 每一位编辑者仅可以对各自创建的 Blocks/Pages 进行（修改）操作

在启用 Immutable blocks 的前提下，各个用户（包括订阅邮箱）都不可以编辑或移除由其他人创建的 Blocks/Pages；但能在 Immutable block 下方创建 Block(s) 并通过缩进，或直接拖动至该区块下方，使其作为附属的（后代）节点。

> 除此之外，用户之间可正常引用（相对于自己）不可变动的 Blocks。

### 基于 Query Builder 的内容审计

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/64a4fcca2456839d4f3aab1fcdfd1cc3_MD5.jpg]]

该 Query Block 的条件可大致理解为「在本页面中，最近由 Shammer 用户编辑过的块」

> 还可以通过添加查询选项 (Add Selection) 来进一步查询关于编辑的时间信息：

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/b30fea1af3d03e37a73b9de7fb40f91a_MD5.jpg]]

左侧为查询对象 Node(s)；右侧为最近的（距离当前时刻）编辑时间

### 协作者的参与度

在 Roam 里，协作者除了可以参与到 Graph 内容上的创作，还能通过 Slider 功能块 {{\[\[slider\]\]}} 与内置的评论页面 \[\[roam/comments\]\] 体现用户的活跃程度。

**Slider 评分机制**

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/5ac7d8430d6a50e3bc9868439c3429dc_MD5.jpg]]

用 Slider 来表达上述结论的认可程度

**Comment 评论**

每一位（编辑邮箱）用户都可以对某一特定的区块内容作出评论，Roam 会自动为每一位用户生成对应的评论块 (Comment-Block)。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/9393ea8cb680c672fce322abaf66a46c_MD5.jpg]]

评论格式：评论页 \[roam/comments\] &gt; 当天日期 (Current Date) &gt; 用户名页面 \[User Name Page\]

---

## 结尾

> 至此，关于 Roam Research 主要内容的介绍就基本完毕了。

### 总结

在关系结构上，Graph 能够高效联络起各 Page 之间的 Blocks；而从数据存储的角度出发，Roam 对资源文件 (Files) 的管理又是相当明智的——将用户上传的媒体附件作分离式存储，且允许对同一份 Upload 的引用复现；最终在实现 Graph 内部高度维稳的同时，还保证了应用程序在数据处理方面的高效运行。

### 感言

诚然，入门 Roam 是存在一定门槛的，无论是（对于国内用户）全英界面带来的「不适感」；还是初见 Roam 时的异常「空旷感」；又或是在第一次面对 Sidebar 时的不知所措——以上种种，都有可能成为新人「自我劝退」的缘由。

> _而当你真正上手后，便会不自觉的陷入其中——**对于 Roam Research 的使用场景也会随着时间的推移，自然而然迎来新的开拓与发掘**_。

_可令人遗憾的是，Roam 官方高昂的订阅价格实在是令人望而却步的——几乎成为了大多数人放弃（或离开） Roam 的主要原因_。

> _对此，笔者想说：**无论怎样优秀的笔记工具，最终都是要由人去使用的**_。

不过笔者始终坚信，Roam 真正要做的绝不只是一个 Note-taking tool 那么简单，而是要让人们在创建/编辑的过程中尽可能得跳脱出"盲目的整理怪圈"。

> 人们应当认识到这一点：关于信息的分类本应是多维度，多模态的。

与其事先定义好一个个「层层嵌套的文件柜」去收纳文档；倒不如让笔记在输入-输出的过程中“自行生长”——以实现对知识图谱的网络模型整合，最终建立起长期的思维认知体系。

![[Omnivore/Roam Research【万字解读】：一款为所有研习者而生的电子笔记应用 - 重新认知下一代信息管理系统模型 - 知乎/attachments/09ea97a6d47485940aac280983b9c984_MD5.jpg]]

正如 Roam 团队在官网介绍的那样：

> 一款为网状思维而生的笔记工具 像文档一样简单易用，与图数据库一样强大 Roam 帮助你长期组织你的研究

最后的最后，请允许笔者用一句话作为全文的总结：

> 人类的生命是短暂的，但知识却是永恒的，让我们在有限的人生里致力于无限的事业！

