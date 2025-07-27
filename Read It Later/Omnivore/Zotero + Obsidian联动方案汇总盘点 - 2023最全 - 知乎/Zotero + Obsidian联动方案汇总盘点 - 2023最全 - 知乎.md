---
id: 609a0669-0a63-4a02-93c9-ee6e7b737685

url: https://zhuanlan.zhihu.com/p/651144180
status:
---


tags:: 

# Zotero + Obsidian联动方案汇总盘点 - 2023最全 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/zotero-obsidian-2023-190b964095b)
[Read Original](https://zhuanlan.zhihu.com/p/651144180)

> 写在前面：论文阅读过程中的批注本质是fleeting notes，所以重要的不是阅读批注如何做如何导出，重要的是对批注的进一步处理，使之成为permanent notes。

Obsidian与Zotero联动根据Zotero的批注笔记是否导出分为两个流派。我将两个流派的最优解决方案列在二级标题，同时列了其他次优方案并给出个人观点评价。其中部分次优方案本人未实际实践体验，可能描述有误，欢迎讨论补充指正。个人使用的是Zotero笔记导出最优方案。

## Zotero批注笔记不导出

### Zotero (ZotFile, Mdnotes, Better BibTeX) + Obsidian (Annotator)

* 参考资料：
   * [如何用obsidian+zotero搞科研？](https://zhuanlan.zhihu.com/p/489713119)
   * [Zotero -> zotfile -> mdnotes -> obsidian -> dataview Workflow](https://link.zhihu.com/?target=https%3A//forum.obsidian.md/t/zotero-zotfile-mdnotes-obsidian-dataview-workflow/15536)
* 特点：
   * 在Obsidian做PDF文献笔记，Zotero管理文献及其元信息。
   * Zotero和Obsidian共用PDF存储
   * 支持Zotero中条目中包含Obsidian对应笔记
   * [如何用obsidian+zotero搞科研？](https://zhuanlan.zhihu.com/p/489713119)的作者开源了相应的Obsidian Vault，Obsidian侧的折腾成本较低
* 缺点：
   * Annotator批注对markdown原文的修改非常丑陋（只有阅读视图看得可以）
   * Annotator不支持在批注中直接用双链
   * Mdnotes导出使用的模板由Mdnotes决定（语法不丰富），文件名无法自定义
   * 不支持对Zotero中笔记的链接（只支持到文件/条目），对Zotero笔记导出的支持较差（用Zotfile导出或者用Mdnotes导出也是可以的）
   * 不支持在Zotero直接打开对应的Obsidian笔记 （[修改.md的默认应用也无法直接打开](https://link.zhihu.com/?target=https%3A//forum.obsidian.md/t/opening-md-file-with-obsidian-instead-opens-most-recent-file/9211/6)），后续提到的Zotero MarkDBConnect可以解决

### 类似不导出方案

* Annotator 替换为 MarkMind (闭源付费) 以集成思维导图功能
   * 参考资料：[Jason Liang：Zotero 和 obsidian 联动，无需 mdnotes、无需导出 markdown 实现原子化笔记、思维导图、pdf 跳转](https://zhuanlan.zhihu.com/p/439177612)
   * 个人观点：思维导图基本可以被双链笔记+检索式复习（主动复习）替代（而且思维导图也可以用Enhancing Mindmap / Excalidraw 以及自带的白板实现）
      * 相关文献："Comparing and Combining Retrieval Practice and Concept Mapping" （从小红书[MrCoffeeTalker](https://link.zhihu.com/?target=http%3A//xhslink.com/NIS2zt)博文中了解的）
* Zotero专职PDF笔记(不导出)，Obsidian结合DataView做文献关系管理
   * 参考资料：[Obsidian+Zotero打造最强科研工具链](https://zhuanlan.zhihu.com/p/639325772)
   * 个人观点：[Zotero Style](https://link.zhihu.com/?target=https%3A//github.com/MuiseDestiny/zotero-style)已经支持文献的关系图谱管理，层级标签的筛选功能可以通过自带的Advanced Search的Tag Contains实现。而Obsidian更适合笔记/已吸收消化的文献的关系梳理。
* Zotero + Obsidian Citations
   * 参考资料：
      * [Obsidian+Zotero，通过citation plugin实现文献阅读工作流](https://zhuanlan.zhihu.com/p/478591089)
      * [Citations Plugin in Obsidian - How to use](https://link.zhihu.com/?target=https%3A//www.youtube.com/watch%3Fv%3DTQXkbITDyGg)
      * [My academic workflow (2022)](https://link.zhihu.com/?target=https%3A//www.youtube.com/watch%3Fv%3DHxaGi9BG0zU)
   * 个人观点：Obsidian Citations的模板单一，而且无法建立从Zotero到Obsidian的联系，但支持非Zotero的文献管理器，没法做PDF批注
* [Zotero Better Notes 单向导出到 Obsidian](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s%3F%5F%5Fbiz%3DMzg5Njk3MDUyMQ%3D%3D%26mid%3D2247487449%26idx%3D1%26sn%3D5d658fdb0445c69356faef03173c4e55%26source%3D41%23wechat%5Fredirect)
   * 个人观点：除了在Zotero中能看到Better Notes外没有优点

## Zotero批注笔记导出

* 感谢评论区  补充提到一个新方案 [Obsidian ZotLit](https://link.zhihu.com/?target=https%3A//zotlit.aidenlx.top/zh-CN)
   * github链接： [https://github.com/PKM-er/obsidian-zotlit](https://link.zhihu.com/?target=https%3A//github.com/PKM-er/obsidian-zotlit)
   * 此方案的特点：
      * 摘录视图：可以在obsidian侧看到zotero的注释看板，并能够拖动导入注释。
      * 支持ETA的模板语法
      * 通过块标识完成增量更新

### Zotero (Better BibTeX) + Obsidian (Zotero Intergration)

* 参考资料：
   * [科研生产力：一个比Mdnotes更丰富的Zotero&Obsidian协同插件| Zotero integration |支持图片与跳转链接](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1jF411A7d6)
   * [https://www.youtube.com/watch?v=CGGeMrtyjBI](https://link.zhihu.com/?target=https%3A//www.youtube.com/watch%3Fv%3DCGGeMrtyjBI)
   * [https://dannyhatcher.com/zotero\-obsidian-integration/](https://link.zhihu.com/?target=https%3A//dannyhatcher.com/zotero-obsidian-integration/)
   * [Obsidian插件-Obsidian-Zotero-Integration](https://zhuanlan.zhihu.com/p/553864286)
* 特点：
   * 支持框选笔记导出成图片
   * 支持Obsidian侧跳转到对应的注释
   * 支持Obsidian侧的导入笔记 （可以同时导入多条）
   * 支持Nunjucks的模板语法（非常丰富，而且和微信读书插件一样）
      * 使用Zotero Integration插件自带Data Explorer可视化地编辑模板
   * Zotero中注释更新后，Obsidian中不会自动更新注释，需要重新导入
      * 但无需像只用Obsidian Citations插件一样需要删除导入, 支持增量导入. 而且支持persist保留对markdown中非zotero批注内容的修改 （目前仅不支持frontmatter的保留）
         * [https://github.com/mgmeyers/obsidian-zotero-integration/blob/main/docs/Templating.md](https://link.zhihu.com/?target=https%3A//github.com/mgmeyers/obsidian-zotero-integration/blob/main/docs/Templating.md)
         * [https://dannyhatcher.com/zotero\-obsidian-integration/](https://link.zhihu.com/?target=https%3A//dannyhatcher.com/zotero-obsidian-integration/)
* 缺点：
   * 无法从Zotero直接跳转到Obsidian的对应批注
      * 解决方案：用类似导出方案中提到的Zotero MarkDBConnect（曾用名 Zotero Obsidian Citations） 插件才能支持从Zotero自动跳转到Obsidian侧的markdown笔记 （但条目并不包含该markdown链接，需要右键条目）

### 类似导出方案

* 使用[Obsidian Bibnotes Formatter](https://link.zhihu.com/?target=https%3A//github.com/stefanopagliari/bibnotes)导入
   * 参考资料：
      * [科研文献阅读——Zotero和Obsidian联动最优解决方案：Better BibTex+BibNotes Formatter+Zotero Obsidian Citations](https://www.zhihu.com/column/c%5F1488931395854168064)
      * [香，Zotero和Obsidian双向联动实时更新方法，利用bibnotes和zotero-obsidian-citations实现](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1R44y137ci)
      * [Zotero (Better BibTeX, MarkDBConnect) + Obsidian (Bibnotes Formatter)](https://link.zhihu.com/?target=https%3A//blog.csdn.net/qq%5F43309940/article/details/125150487)
   * 个人观点：
      * Obsidian Bibnotes Formatter比Obsidian Zotero Integration的唯一优势似乎就是增量更新批注时多了一种格式选项
      * Obsidian Bibnotes Formatter没法保留非Zotero批注外的文本修改？
         * 这点未尝试，关系到是否能够直接在导出的md文件中直接做笔记，同时还能增量导入批注不修改笔记内容
      * Obsidian Bibnotes Formatter的模板语法不如Nunjucks丰富
         * 仅支持对Highlight的颜色筛选以及一些固定转换（另一方面上手可能更容易）
* 使用[Obsidian Zotero Annotations](https://link.zhihu.com/?target=https%3A//github.com/anoopkcn/obsidian-zotero-annotations)导入
   * 参考资料: [维客笔记：Ob插件 | 又一zotero与Obsidian联用方案，解决了我的一个问题](https://zhuanlan.zhihu.com/p/594271898)
   * 个人观点: 插件开发者已经废弃该插件，并推荐使用Obsidian Zotero Integration

## 半成品方案

* Zotero ZotSever + Obsidian [Zotero Bridge](https://link.zhihu.com/?target=https%3A//github.com/vanakat/zotero-bridge) \+ [Obsidian Zotero](https://link.zhihu.com/?target=https%3A//github.com/vanakat/zotero-link)
   * 个人观点：目前Zotero Link只支持输入不同样式的Link，Link的文字部分可以用给定模板。但Zotero Bridge插件确实提供了更多后续开发可能，目前自动化程度还是太低。
   * 参考资料： [https://www.youtube.com/watch?v=44vV7Tr484Q](https://link.zhihu.com/?target=https%3A//www.youtube.com/watch%3Fv%3D44vV7Tr484Q)

> 本文使用 [Zhihu On VSCode](https://zhuanlan.zhihu.com/p/106057556) 创作并发布

