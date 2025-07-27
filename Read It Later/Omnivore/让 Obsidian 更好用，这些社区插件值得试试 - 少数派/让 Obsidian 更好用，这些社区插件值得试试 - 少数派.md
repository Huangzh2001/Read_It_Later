---
id: cb7cea67-7171-423f-bd4d-952d29a74f18

url: https://ios.sspai.com/post/66094
---


tags:: 

# 让 Obsidian 更好用，这些社区插件值得试试 - 少数派
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-19178dfd4d5)
[Read Original](https://ios.sspai.com/post/66094)

**Matrix 首页推荐**

[Matrix](https://sspai.com/matrix) 是少数派的写作社区，我们主张分享真实的产品体验，有实用价值的经验与思考。我们会不定期挑选 Matrix 最优质的文章，展示来自用户的最真实的体验和观点。

文章代表作者个人观点，少数派仅对标题和排版略作修改。

---

去年在少数派上偶然发现了 Obsidian，那时候的它还只是一个相对简陋的带双向链接功能的本地笔记软件，我对此并没有多留意。但随着 Obsidian 在 2020 年下释出 v0.9.8 版本（该版本增加了官方支持的第三方插件市场）同时 Notion 出现了北墙风波后，我开始在 Obsidian 上投入时间精力（趁着它还比较简单的时候入手，及时适应以后更新带来的笔记方法上的变化）。

在深度使用后，我隐约觉得，当你把 Obsidian 简单看成支持双向链接的 markdown 编辑器和文档管理器，那么使用它并没有多大难度。但如果你想要求更多，不好意思，即使现阶段的本体（v0.11）也还是满足不了你。不过好消息是第三方社区插件已经极大地丰富了，你的个性化需求都可能在这找到解决方案。因此本人将解决了我记笔记过程中痛点的插件整理成此文，推荐给大家。

## 弱化文件夹和笔记的区别（必备）

### Folder Note

* 作者：xpgo
* 简介：为文件夹生成注释；为文件夹内的笔记生成卡片样式。

### Note Folder Autorename

* 作者：PJ Eby
* 简介：将笔记移入同名文件夹，保持笔记和文件夹在移动、重命名时一致。

我可以确切地说，这两个插件最终实现的效果是殊途同归的，一个是由文件夹创建同名笔记，一个是由笔记创建同名文件夹。不过由于 _Note Folder Autorename_ 没有插件选项，为了让两者融洽共处，需要在 _Folder Note_ 的插件选项中设置笔记生成在文件夹内部，并且关闭自动重命名。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sSwBKxFhcaI63BJw_1EByXyt1kubbkOE95Jp9XeieurU/https://cdnfile.sspai.com/2021/04/30/5d729fe8c42e549ee280471fe64ae250.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

两者结合之后使用方法非常简单，按住「Ctrl」单击文件夹（Mac按住「⌘」）或者在当前页面输入命令「Note Folder Autorename」都可以创建一个嵌套的同名文件夹加笔记。

![](https://proxy-prod.omnivore-image-cache.app/0x0,s27-vAGvLK7pO2nyj5QmtjOg3czoGUfoBET6x5Gs8v58/https://cdnfile.sspai.com/2021/04/30/5daa3ae23037c1b54082c977d20deb96.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

如果我们按照 xpgo 的思路，这个插件只是用作文件夹的注释，那么就被他带偏了。因为这个注释依然是个 markdown 文件，当然可以继续作为笔记。实际这两个插件的意义正是将 Obsidian 的文件列表结构给模糊化，摆脱了文件夹和页面之间的鸿沟。信息的组织结构虽然有「线状——树状——网状」，但表现出来的形式千差万别，比如我们知道 Notion 是数据库和页面的嵌套，却可以切换不同视图来观察笔记之间的结构和联系，而 Obsidian 的文件列表则是典型的树状层级结构。在这两个插件之前，Obsidian 的使用大体是：

1. 按照传统笔记的思维，层级结构基本为「笔记本组——笔记本——章节——页面」，文件列表内文件夹用来分类形成目录（为了有序还会使用编码系统），只有页面能承载笔记，还需要使用 Tag 插件与文件列表配合形成网状联系；
2. 按照 MOC 的思维，所有笔记不分权重全部放入一个 Content 文件夹，通过双向链接与文件夹外部的 Index 笔记来联系，使用关系图谱插件来观察网状联系。
3. 按照 DailyNote 的思维，所有笔记都记在每日日记里，使用卢曼序号或时间戳来标记每日日记里的笔记，最终形成的是以日期和笔记两种双向链接交织的网状联系。

使用这两个插件之后，文件夹和页面的区别已经没有那么严格了。这个文件夹加页面的一体化产物，你可以继续把它当文件夹看待，那么它确实是一个描述文件，你也可以把它当页面看待；那么现在是一个「页面——页面——页面」的层级结构了，每一个层级都可以作笔记的载体；当然你也可以把它当 Database 看待（配合查询插件），文件夹内的每条笔记都是数据的载体，那么我们可以把 Notion 的「database / page / block」的概念套用。

总之，它不仅让所提及的传统笔记法、MOC 笔记法和 DailyNote 笔记法的使用过程变得更简单，也让画册、看板、表格、列表等等组织方式和视图可以在 Obsidian 更容易实现，使我们组建自己的笔记体系有了更多的选择，能更顺应自己的直觉。

## 实现卡片、列表视图

_Folder Note_ 自带将文件夹内的笔记以卡片、列表的形式组织起来的视图。两者切换的方法为在「ccard」的代码块中添加或删去 `style: strip`，如图：

![](https://proxy-prod.omnivore-image-cache.app/0x0,s-CrCNCGh7oF8XI-6JHx0XMNmaRlq6DFVhQEvo7lAqx0/https://cdnfile.sspai.com/2021/04/30/8ea7670b91f835a4c27e48f465514066.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp) 

![](https://proxy-prod.omnivore-image-cache.app/0x0,sTvf5bRXThAYlAyWtOdLB8AYyFIBttInDxa4UIY7Pohk/https://cdnfile.sspai.com/2021/04/30/818606f1b782ee9f5a2acfef3d914ffd.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp) 

## 实现表格、清单、任务视图

### Dataview

* 作者：Michael Brenan
* 简介：用提供的查询语法动态查询库中的笔记，并且可以过滤、排序和提取笔记中的数据。

_Dataview_ 可以通过文件夹、标签、双向链接来查询库中的笔记。提取笔记数据时，主要通过笔记开头的 Front Matter 区域。等官方将来提供更好的 Front Matter 编辑和管理方式时，该插件的全部实力将会更大激发。而目前，它依然是最具潜力的插件之一。简单的查询语法如下：

```coq
```dataview
// dataview 不能缺，缺了识别不了

[list|table|task] field1, (field2 + field3) as myfield, ..., fieldN
// 可以选择 list 或 table 或 task 三种视图，选择 table 时可以填写每列也就是 field 的名称，field 需出现在正常显示的笔记的 Front Matter 区域。

from #tag or "folder" or [[link]] or outgoing[[link]]
// 查询的范围，可以使用标签，文件夹（可以用/进行嵌套），也可以使用双链,当前面加上 outgoing 表示从此链接发散。

where field [>|>=|<|<=|=|&|'|'] [field2|literal value] (and field2 ...) (or field3...)
// 根据 field 的值来进行过滤。

sort field [ascending|descending|asc|desc] (ascending is implied if not provided)
// 按照 field 排升降序。
```
```

由于 Dataview 默认查询的范围是整个库，具体实操还需要我们去考虑如何通过文件夹、标签和链接去获得我们想要的而不把无关的笔记也纳入。如果我们仅仅想要积累同一个主题的笔记，比如观影记录等等，那么可以通过与 _Folder Note_ 和 _Note Folder Autorename_ 联用，将 Dataview 的代码块放在文件夹同名笔记内，需要用来查询的笔记都放在同一文件夹内，这样就简单限制了查询的范围。实现的效果如图：

![](https://proxy-prod.omnivore-image-cache.app/0x0,si7dXHEFHHegV54akn9MdUGAMoMznRerUBtv0Z-3-mHg/https://cdnfile.sspai.com/2021/05/01/4970589f3b7ea805a523d05513479459.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

并且作者将来还会上线其他几种视图，我们可以期待下通过这种方法建立自己的数据库，比如建立自己的书籍库、阅读库等等。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sCUZ7paS4bqOhi0HVm87wv4PjOL_HTYVTe4bWykazx6M/https://cdnfile.sspai.com/2021/05/01/62830151c225bace8a6dda2cb3bc78b6.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

## 实现看板功能

### Kanban

* 作者：mgmeyers
* 简介：（顾名思义）看板。

如果你有用过 Notion 的看板或者 Trello 的看板，想要在 Obsidian 中也拥有看板的功能，似乎有点困难，变通的办法是并列 N 个窗格，每个窗格当成看板的列表，卡片的移动靠复制粘贴。现在，终于有插件作者对 Obsidian 的看板进行开发了。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sIdYeXsI08PMJCd1UAallo4QNVazEcTAoZOVFtpCw6lE/https://cdnfile.sspai.com/2021/05/01/2b4421c03032f9486ed4031d7912d244.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

_Kanban_ 目前的创建方式分两种，一是从文件夹的右键操作菜单创建，你可以提前安装 _Folder Note_ 和 _Note Folder Autorename_，之后直接更改看板的名称和文件夹一致，最终看板产生的卡片都能放置在这一个文件夹内。

二是通过命令面板创建，不过这种方法只能创建在库的根目录。如果想要在任意位置创建，可以将下方代码放在空模板笔记的 Front Matter ，以后要创建看板就可以用模板生成，再点击右上角「更多选项」内的「Open as kanban board」，也能创建看板。

```yaml
---
kanban-plugin: basic
---
```

![](https://proxy-prod.omnivore-image-cache.app/0x0,sFnwP2RzqSaaAhfdXfmREBSb-kA1KMsZ9kgPUBWuaZ7k/https://cdnfile.sspai.com/2021/05/01/330013ed0ec118b0368930982564c204.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

## 实现时间轴视图

### Timelines

* 作者：darakah
* 简介：通过标签创建时间轴视图。

通过这个插件，我们依据时间顺序，将一方面或多方面的事件串联起来。比如制作一份大事记或者以时间线索收集或分析某一主题。不过由于它是完全通过 Front Matter 的标签来筛选笔记的，如果我们建的主题比较多就容易污染全局标签，把不相干的笔记也提取进来。

我的解决方案是，先使用下方代码制作两个模板（需要用到 _Templater_ 插件），需要按照时间轴视图观察笔记时通过 _Folder Note_ 和 _Note Folder Autorename_ 创建一个主题文件夹笔记，将所有相关的笔记放入该文件夹，然后把左方代码插入文件夹同名笔记，把右方模板插入各个笔记的 Front Matter。「tp.file.folder」可以生成当前文件夹的标签，这样就提前限制了 Timeline 提取的范围。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sac5SBdjCLKI4ezs8iDplev1bCfdMOu4E5Gc_Mlg5TrE/https://cdnfile.sspai.com/2021/05/01/a91fec2e22d43fc45ea68b7772756e03.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

```yaml
```timeline
<% tp.file.folder() %>;
```

---
tags: [timeline, <% tp.file.folder() %>, ]
---

<span 
      class='ob-timelines' 
      data-date='<% tp.date.now("YYYY-MM-DD-HH") %>' 
      data-title='<% tp.file.title %>' 
      data-class='orange' 
      data-type='range' 
      data-end='<% tp.date.now("YYYY-MM-DD-HH") %>'> 
</span>
```

最终效果示例：

![](https://proxy-prod.omnivore-image-cache.app/0x0,stEFejoSSnfYvgqJPRLJ6qMja16QZpKBS4NXPH0VJh6o/https://cdnfile.sspai.com/2021/05/01/10c0e53519e0897f3c200688a36273a6.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

## 增强关系图谱

### Juggl

* 作者：Emile
* 简介：可交互、可样式、可拓展的图形关系视图。

前身是作者的另一款插件 _Neo4j Graph View_（现已退役），与 Obsidian 自带的关系图谱插件区别在于提供 4 种不同的关系图谱布局，不止可以使用样式窗格来调整节点的颜色、形状、大小和图标，还可以在连接线上标注。不过还处在开发阶段，超过 250 个笔记就会很卡，甚至是直接卡死。可以和自带的关系图谱搭配使用，4 种不同的布局还是很酷炫的。

![](https://proxy-prod.omnivore-image-cache.app/0x0,svwYetmKfgTseUYUPwK6GM-eime6ZKcerOzeHJnxnFnQ/https://cdnfile.sspai.com/2021/05/01/1107b358cb14db93c9113558d14b598e.gif)

作者的效果

![](https://proxy-prod.omnivore-image-cache.app/0x0,sAQ7CPQ8Q_CKv1eD2lkoZqYO5CYbVSmd8nvCYnvTWoDE/https://cdnfile.sspai.com/2021/05/01/6e1cea04cce0d6e3f49dd2fa60ca354c.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

我的（已卡死）

## 增强大纲功能

### Outliner

* 作者：Viacheslav Slinko
* 简介：（言简意赅）Work with your lists like in Workflowy or RoamResearch

虽然目前还不能拖动大纲的节点，不过这个插件已经通过快捷键来实现大纲的顺序更改、左右缩进更改，方法如下：

1. Tab 以及 Shift + Tab —— 更改大纲节点的缩进和升级
2. ⌘ / Ctrl + ⇧ + ↑ 以及 ⌘ / Ctrl + ⇧ + ↓ —— 上下移动当前节点
3. ⌘ / Ctrl + ↑ 以及 ⌘ / Ctrl + ↓ —— 收起或展开当前节点
4. ⌘ / Ctrl + a —— 选中当前节点
5. ⌘ / Ctrl + .（英文句号）以及 ⌘ / Ctrl + ⇧ + . —— 进入或退出当前节点

另外，点击前面的小点也可以进入大纲的节点，同时在上方有面包屑提示层级。不管你是否要完全使用大纲的方式来记录笔记，都可以使用该插件来提升大纲体验。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sGZvDex9izfOW6SO6e7TgFI9DW6QmWWGk0CMTY9-eptg/https://cdnfile.sspai.com/2021/05/01/6f446e76d0d1d6556d295d3586abcaeb.gif)

## 改进 Markdown 表格

### Advanced Tables

* 作者：Tony Grosinger
* 简介：改进 markdown 表格编辑，并通过面板管理。

### Table Extended

* 作者：AidenLx
* 简介：增加 markdown 表格合并单元格的语法

老实说，markdown 的表格已经背离了轻量级标记的原意。由于 _Advanced Tables_ 并不能创建表格，所以还需要提前在模板里准备一个空白简单表格，通常我只是使用它的工具栏来进行排序，如果使用它的函数语法为什么不打开 Number 呢？对吧。_Table Extended_ 是国人开发，现在终于可以在 Obsidian 的表格内合并单元格了。具体用法看下图：

![](https://proxy-prod.omnivore-image-cache.app/0x0,sYuIMHbCZMOWM7n9sf3RucsUQuyUuN5ySHq-1Qi_Fau4/https://cdnfile.sspai.com/2021/05/01/c10af83cddd7cefbf1977d624ee24948.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

## 增加图表功能

* 作者：Phibr0 / Rythm
* 简介：创建简单图表。

可以用 Charts 创建六种简单的图表，并且随着插件版本 2.0 的更新还有了全新的输入面板，可以提前预览。看截图，生成的图表还是比较精美的。

![](https://proxy-prod.omnivore-image-cache.app/0x0,ssn1u2vOLWsL1kVJb4RpidoY-mZnQ6pxvz5pmJsyZnMM/https://cdnfile.sspai.com/2021/05/01/7c1d4404b81836540d370ee9b9c009da.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

![](https://proxy-prod.omnivore-image-cache.app/0x0,s1qLcnZobzWBOSdR-R7P3K5vvn8TnP2T9gI2oyy0FPHU/https://cdnfile.sspai.com/2021/05/01/59a56fab1390ca488668e08eb67a560c.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

## 增加提示块功能

### Admonition

* 作者：Jeremy Valentine
* 简介：专属于 Obsidian 的提示 Block。

我在 Obsidian 页面内写自己的观点、评价时是先使用「==」高亮语法画线，再在段落下方用「%%」注释语法评论，但这样的结果就是预览时评论内容是不会被渲染的。所以有了这个插件我很开心，马上就做了一个专门用来评论的块。

进入 _Admonition_ 的插件设置，点击「Add」，按照下图就可以完成定制了。

![](https://proxy-prod.omnivore-image-cache.app/0x0,scr8cXZw-_3yrtNGlgKjo00t_YI89rAmN11Bim_rTA7M/https://cdnfile.sspai.com/2021/05/01/e495bcbfd71dea5b6170ac1d7b7199c4.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

具体使用，先制作成模板，在需要时直接插入。同时 _Admonition_ 还有许多默认支持的块可以使用，插入模板再将「ad-」后单词替换，就完成提示块类型转换啦。实际效果如下：

![](https://proxy-prod.omnivore-image-cache.app/0x0,sLEXy6mOfquh9NNP2PRBJa5O-ZOipTp_p2c8gIA-Pi3Y/https://cdnfile.sspai.com/2021/05/01/58a086ae70678d16611eb4a6a105c4cb.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

| **Type** | **Aliases**                 |
| -------- | --------------------------- |
| note     | note, seealso               |
| abstract | abstract, summary, tldr     |
| info     | info, todo                  |
| tip      | tip, hint, important        |
| success  | success, check, done        |
| question | question, help, faq         |
| warning  | warning, caution, attention |
| failure  | failure, fail, missing      |
| danger   | danger, error               |
| bug      | bug                         |
| example  | example                     |
| quote    | quote, cite                 |

## 万能模板

### Templater

* 作者：SilentVoid
* 简介：可将变量、函数和 JavaScript 代码处理结果插入笔记中。

Obsidian 自带的模板插件只有 `{{date}}` 和 `{{time}}` 可用，功能少的可怜。从最开始 _Templater_ 就展现了它的实力，它可以获取日期、时间、文件名、内容、路径，可以预设光标位置，可以自己添加命令等等。

而现在，随着插件作者对这个插件的重构（现在的分类更有条理），以及新命令的加入，_Templater_ 也变得越来越万能。最近加入了预设多个光标位置的变量，可以在插入模板后跳转到不同的光标位置进行填写（需要提前设置快捷键，如下）。

![](https://proxy-prod.omnivore-image-cache.app/0x0,s8_vMocOM0U2A1nrbpYhNS0aQrzaIyvRD9Mxi9jB1OKE/https://cdnfile.sspai.com/2021/05/01/60521b6a57ebb96dd1e6c6695ae996ec.png?imageView2/2/w/1120/q/40/interlace/1/ignore-error/1/format/webp)

![](https://proxy-prod.omnivore-image-cache.app/0x0,s3Dq0jGkM4-3iirVaXesCdoClh5EtyNtyMeHpfaqxF10/https://cdnfile.sspai.com/2021/05/01/35b695c16df15198a7d32528cc368070.gif)

然而，_Templater_ 看起来比较复杂的语法可能会令人产生劝退的感觉，考虑到在社区插件页面介绍不够详细，作者还提供了专门的介绍文档 [Templater Doc](https://silentvoid13.github.io/Templater/docs/) 供大家查看，举了丰富的例子帮助大家降低使用难度。

### 小结

当然，Obsidian 的社区插件市场还有很多优秀的插件，由于本文篇幅有限，我无法一一展开。就解决我需求的来讲，_Excalidraw_ 由 RR 的 Draw 插件作者 Zsolt Viczian 移植到 Obsidian，填上了 Obsidian 绘图的空白，相信会在移动端更出彩；_Tag Wrangler_ 对原标签插件加强，在原来标签面板上右键会出现新的操作命令，可以对标签重命名、设置在搜索中隐藏；_Word Splitting for Simplified Chinese in Edit Mode_ 解决了在 Obsidian 中双击选择文字时，只能选中一整个句子的问题。此外，_Note Refactor_ 可以方便地将笔记原子化、_Recent Files_ 展示历史打开文件、_Mind Map_ 可以生成脑图等等，数不胜数。

重要的是，随着插件开发的井喷以及插件 API 的日臻完善，在 Obsidian 中实现大家各自形态各异的工作流的机会已经越来越近。如果有发现能初步实现自己需求的插件，那不妨积极反馈到对应的插件作者，说不定他就帮你实现了更多更完整的需求了呢。

**特别提示**：非官方插件的使用有其安全性的考量。Obsidian 的社区插件大都使用 JavaScript 制作，不能排除插入恶意代码的可能性，使用前请考察其安全性。作者本人的推荐不包括对其安全性的承诺。

\> 下载 [少数派 2.0 客户端](https://sspai.com/page/client)、关注 [少数派公众号](https://sspai.com/s/J71e)，解锁全新阅读体验 📰

\> 实用、好用的 [正版软件](https://sspai.com/mall)，少数派为你呈现 🚀

[![[Omnivore/让 Obsidian 更好用，这些社区插件值得试试 - 少数派/attachments/985df22c44e64ec563aa540d2c322261_MD5.webp]]](https://ios.sspai.com/u/881170/updates)

