---
date: 2025-10-15T13:33:39+08:00
url: https://mp.weixin.qq.com/s/hjSeECYErd0DR8GFpV3ZSA
status: readed
---
原创 Moy [PKMer 知识社区](https://mp.weixin.qq.com/s/)

*2025年09月19日 19:30* *湖北*

![[Read It Later/attachments/205b8d3c0f6ad7ce9d6ad3b7e91d0e5b_MD5.gif]]

*由于微信限制，公众号文章内无法添加可跳转的链接，如果想要了解文内提到的更多信息，请点击文末的阅读原文，查看本期内容*

![[Read It Later/attachments/ed4c85a971d422a52d899467a59da6d0_MD5.gif]]

PKMer

![[Read It Later/attachments/ed4c85a971d422a52d899467a59da6d0_MD5.gif]]

Obsidian的CEO是怎么做笔记的？

  

Ob 的现任 CEO Kepano 在自己的 How I use Obsidian 一文中，阐述了自己如何使用 Obsidian 的方法论，并分享了自己的模板库。

关于 Kepano

原名 Steph Ango，网名 Kepano，现任的 Obsidian CEO；

或许你也用过他写的 Obsidian 主题：Minimal

  

初步研究之后，我做了一些基础的想法和要点记录，抱着“写都写了”的想法，遂分享之。

注：文章本身写得也很好，非常建议阅读原文——配合他的 示例库 一起查看效果更加！

  

**关于插件**

他文章里提到的插件很少，主要是使用了 **Dataview** 进行数据整合，用了另一个地图插件做地点记录。

  

结合他“只写纯文本”笔记的习惯，可以推测他库里**只会安装非常少量的插件**，并且基本只用原生 Markdown 语法。

  

**基本原则**

他在个人知识库中遵循的规则：

- 避免将内容拆分到多个知识库中（单一仓库）
- 避免使用文件夹进行组织（使用属性进行组织）
- 避免使用非标准的 Markdown 格式
- 命名时，始终使用复数形式的单词（例如只用 people 而不是 person），包括分类名称和标签（ [#tags](https://mp.weixin.qq.com/s/) ）
- 大量使用内部链接（最短路径的 Wikilink 形式，例如 \[\[链接\]\] ）
- 在所有地方使用 YYYY-MM-DD 格式的日期（这也是 DailyNote 默认的标题名称格式）
- 使用7分制进行评分

上面这段是原文摘录+补充说明，作为总纲，更多内容可以戳原始文章查看。

  

**关于结构**

- 他基本不用文件夹组织文件，更不用嵌套文件夹——**大部分笔记直接放在根目录**
- 但是有一个单独的 Categories 目录，里面放了各种分类（例如 电影 、游戏、 桌游 等等）的索引笔记
- 基于这样的结构，他主要使用快速切换（Quick Switcher）和链接关系来跳转笔记，而不是文件浏览器（File Explorer）

![[Read It Later/attachments/9cfc9369f64990f1df792d38ad7500f4_MD5.webp]]

*他的 Categories 目录中的 Books 笔记*

  

**关于属性**

- 笔记的元数据中会有一个类似 category: \[\[电影\]\] 的属性，与此对应的是 Category 目录下的 电影.md 笔记，这样一来，**通过 Dataview 能查询到所有类别为电影的相关笔记**
- 可以说，Kepano 使用这样的属性——而非文件夹——来组织笔记（既不是传统的文件夹结构，也不是标签结构，有趣）
- 同样的属性应该在不同类型的笔记间通用，例如所有的媒体笔记都可以用 genre 属性，不管它是电影、游戏还是动画

这里可以看到他的模板库中所有的属性： kepano-obsidian/.obsidian/types.json

- 属性名称保持尽量简短，例如用 created 而不是 created\_date
- 对于可能存在多个值的属性，类型选择 list （列表）而不是 text （文本）

可以看到，Kepano 库里很多笔记甚至是**纯数据笔记**，只写了属性，完全没有正文内容：

![[Read It Later/attachments/2afb8eccda49007a3c88f0ef45551389_MD5.webp]]

  

——简直就像是从 Notion 导出数据库之后，里面的项目转换成的笔记。

  

**关于笔记内容**

关于 Kepano 笔记里记录的内容，可以说是「包罗万象」，并且不拘一格。

  

什么东西都可以往里记，有一个专门的 References 参考文件夹用于存放这些（非自己笔记的）外部条目。比如电影、电影院、餐厅……

  

可以说就是“啥都往里记”。

  

比如他举例的一条日记条目：

I went to see the movie  \[\[Perfect Days\]\]  with  \[\[Aisha\]\]  at  \[\[Vidiots\]\]  and had Filipino food at  \[\[Little Ongpin\]\] . I loved this quote from Perfect Days:  \[\[Next time is next time, now is now\]\] . It reminds me of the essay ...

就……很普通的一个随笔记录？但也没问题！

具体可以看示例库，这里不多赘述。

  

**关于链接**

从上面的那个日记示例也可以看得出来，他大量地使用了双链（甚至看起来在滥用）。

  

短短一段话里：

- \[\[Perfect Days\]\] 是电影《完美的日子》
- \[\[Aisha\]\] 是人名
- \[\[Vidiotss\]\] 推测是电影院
- \[\[Little Ongpin\]\] 估计是餐厅
- \[\[Next time is next time, now is now\]\] 是这部电影里的一句台词摘录——是的，这个也有单独的一个链接！！

说实话第一次看到这么泛滥的内链使用我是很震惊的……

  
平时一篇笔记里可能也就三四个内链，他这一段话就5个了，甚至还有「把一整句句子作为内链」这种堪称离谱的用法！

  

但是转念一想，Obsidian 当年出圈主打的两个热门特性就是 知识图谱 和 双向链接，这种用法也算是完全挖掘出「双链」的特性了。

  

不过具体实践上，见仁见智，感觉可以适当参考，也不用真的给家附近的餐厅和电影院啥的都创建上双链……

  

**创建链接的技巧**

说到这里也补充两点：

  

善用「空链接」，也就是你可以写 \[\[这样一个完全没有同名笔记的链接\]\] ，Obsidian 也是会识别的，而且在下次输入 \[\[这样一个 的时候也能弹出对应的补全。

![[Read It Later/attachments/2dc97b1d7fab70911f228add2c8c28d9_MD5.webp]]

  

- 你可以先这样写着，直到它数量确实够多的时候，再创建链接实际指向的笔记
- 而当实际笔记创建的时候，它的反链就能显示出过往所有提及到自己的笔记

  

最常见的链接方式是输入两个 \[\[ 符号然后选择，在此基础上，有一些插件可以优化体验，例如：

- Easy Typing 插件可以把 「「 或者 【【 映射成链接符号，这样在中文输入法下也不用频繁切换中英文符号
- Various Completions 插件可以在你打字的时候，自动弹出同名笔记选项，这样甚至能直接省略输入符号的步骤，直接写笔记名然后选择即可

![[Read It Later/attachments/f03116c51b1742581c6b025cc40a8dea_MD5.webp]]

*通过 VariousCompletions 直接显示同名笔记*

  

**关于链接格式**

另外，你应该也看出来了，对于**链接格式**他选择的是：「尽可能简短的形式」+「Wiki 链接」选项。

![[Read It Later/attachments/e7c7c862a3a792a6b8e1fba8a6f08b2d_MD5.webp]]

  

我曾经为了像是和 Typora 之类软件的兼容性，类型会选择「相对链接」，但最终用下来发现「最短 wiki」确实是最适合 Obsidian 的链接形式，这样笔记的移动完全不会影响链接，是最省事儿的！

  

所以，我也推荐按这个配置来！很香的！（甚至更进一步，你可以把所有的图片也都塞进同一个附件文件夹里，讲究一个「大道至简，无为而治」）

  

**笔记属性内的链接**

这其实也是我看完他的示例库才开始大胆用的一个特性：**在笔记属性里写双链**。

![[Read It Later/attachments/d5ccbb2f722bdcdff5cb89c309c6b365_MD5.webp]]

  

源代码模式下查看：

\--- 

people: 

   - "\[\[Kepano\]\]"

 ---

  

Obsidian 原生就支持将它解析成链接，通过这个属性你可以直接点击跳转到对应的笔记，会很方便。

  

**关于一致性**

这点其实也是我学习到最多的一点。

保持 一致的风格 可以将数百个未来的决定合并为一个，并让我集中精力。例如，我总是将标签复数化，这样我就不必想如何命名新标签。  
选择让您感觉舒适的规则并将它们写下来。制作您自己的风格指南。您以后可以随时更改规则。

  

举几个关于“一致性”的例子：

- 总是选择单词的复数，这样就不用考虑 Category 还是 Categories ——直接选后者！用这个策略，应该创建像是 Clippings、Projects、Works 这样的文件夹！
- 总是使用7分评分制
- 所有用到日期的地方，统一使用 2025-05-11 这样的固定日期形式

首先，这样带来的好处是，每日笔记（DailyNotes，默认日期格式就是 yyyy-MM-DD）中可以通过反向链接查看到所有和当天有关的笔记

其次，这也能让你搜索的时候不用考虑搜 5月11日 或者 5.11 之类的变种格式，保持统一的情况下，你只需要搜索 05-11 一个关键字。

  

看完之后，我自己做的一些调整：

- 重命名了大量笔记——以前我会有一些 2025.05.11 格式的日期前缀，现在统一都改成了 250511\_ （嗯，这点算是我的坚持，因为笔记名不希望太长）
- 把输入法中快速输入的日期也从 2025.05.11 换成了 2025-05-11，兼容每日笔记基础格式
- 重命名了部分标签和文件夹名称，都按复数形式来命名

我获得的一个感受是：**需要想的规矩越少，记录的阻碍就越小**。

  

所以，一定形成了你自己的「固定一致性原则」，你在执行的时候就可以完全不去“重复思考”，直接按照既定规矩自动化执行即可。（而且，毕竟是自己的规矩，所以也不用拘泥于“祖宗之罚不可变”，哪天想要做出调整的话，调就是了）

  

**一些学到的经验**

大胆创**新**！  
——这里的新指“新笔记”、“新链接”以及“新模板”，反正都是纯文本文件，你怕什么！需要就创建新的！创！多创！

  
人家模板文件夹里有 57 个模板！！

  

你的笔记是非常私人且自由的：**不要怕记多，更不要怕记错**。

感觉一些同学（包括我自己）在记录之前会先想着“怎么组织结构”，“怎么分类”……等一些宏观的规矩，然后下手很谨慎  
但实际上，很多时候就是先埋头写，写够多了之后，结构关系会自己生长出来

  

而且对于“文件名”（链接）也不要墨守成规，纠结什么格式啊标点符号之类的。

  
只要文件系统允许的命名，都可以写！**保持灵活，保持开放**。

  

**总结**

以上，这就是我对于 Kepano 使用 Obsidian 的方式的拆解和思考，希望能给你带来一些新的构想。

  

不过也需要说一句，虽然他是“Obsidian 的 CEO”，但这不代表他使用 Obsidian 的方式就是「权威」和「标准」。

  
别人的做法是基于他们自己的人生经验得出来的，不一定适合自己。

  
可以借鉴的，学习之，同时也要保留自己的风格和坚持。

  

还是那句话：适合自己的，才是最好的。

**\- THE END -** 

<svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" style="transform: rotate(0deg);-webkit-transform: rotate(0deg);-moz-transform: rotate(0deg);-o-transform: rotate(0deg);box-sizing: border-box;" viewBox="0  0 349 31" role="img" aria-label="插图"><svg style="overflow: initial;box-sizing: border-box;" width="45.1776%" height="61.15%" x="-5.55034%" y="26.7512222195471%" role="img" aria-label="插图"><foreignObject width="100%" height="100%" style="transform-origin: center center;-webkit-transform-origin: center center;-moz-transform-origin: center center;-o-transform-origin: center center;transform: rotate(0deg);-webkit-transform: rotate(0deg);-moz-transform: rotate(0deg);-o-transform: rotate(0deg);box-sizing: border-box;"><section xmlns="http://www.w3.org/1999/xhtml" style="font-size: 7px;height: 100%;box-sizing: border-box;"><section style="font-size: 12px; color: rgb(52, 54, 60); text-align: center; word-break: break-word; box-sizing: border-box; --darkreader-inline-color: var(--darkreader-text-34363c, #c5c0b8);" data-darkreader-inline-color=""><p style="margin: 0px;padding: 0px;box-sizing: border-box;"><span style="color: rgb(255, 202, 0); box-sizing: border-box; --darkreader-inline-color: var(--darkreader-text-ffca00, #ffcf1a);" data-darkreader-inline-color=""><span leaf="">//</span></span><span style="color: rgb(255, 202, 0); box-sizing: border-box; --darkreader-inline-color: var(--darkreader-text-ffca00, #ffcf1a);" data-darkreader-inline-color=""><span leaf="">&nbsp;</span></span><span style="box-sizing: border-box;"><span leaf="">长按二维码·加入我们</span></span></p></section></section></foreignObject></svg></svg>

![[Read It Later/attachments/82e74864114fcf6e102465702a39fe62_MD5.webp]]

QQ群

![[Read It Later/attachments/48537bfeec10dd28af2f29214580c3f4_MD5.webp]]

微信群

![[Read It Later/attachments/8e4c3ec2461c4d85b23c25c6a3e100bf_MD5.webp]]

![[Read It Later/attachments/f2521ad0aca746361f14c3c29cb08df0_MD5.gif]]

<svg xmlns="http://www.w3.org/2000/svg" width="100%" height="100%" style="transform: rotate(0deg);-webkit-transform: rotate(0deg);-moz-transform: rotate(0deg);-o-transform: rotate(0deg);box-sizing: border-box;" viewBox="0  0 353 68" role="img" aria-label="插图"><svg style="overflow: initial;box-sizing: border-box;" width="42.1123%" height="84.43%" x="57.3167%" y="-1.91416364471241%" role="img" aria-label="插图"><foreignObject width="100%" height="100%" style="transform-origin: center center;-webkit-transform-origin: center center;-moz-transform-origin: center center;-o-transform-origin: center center;transform: rotate(0deg);-webkit-transform: rotate(0deg);-moz-transform: rotate(0deg);-o-transform: rotate(0deg);box-sizing: border-box;"><section xmlns="http://www.w3.org/1999/xhtml" style="height: 100%;font-size: 13px;box-sizing: border-box;"><section style="font-size: 12px; color: rgb(160, 160, 160); text-align: center; word-break: break-word; box-sizing: border-box; --darkreader-inline-color: var(--darkreader-text-a0a0a0, #aca59a);" data-darkreader-inline-color=""><p style="text-align: left;margin: 0px;padding: 0px;box-sizing: border-box;"><strong style="letter-spacing: 0px;box-sizing: border-box;"><span leaf="">作者</span></strong><span style="letter-spacing: 0px;box-sizing: border-box;"><span leaf="">：Moy</span></span></p><p style="text-align: left;margin: 0px;padding: 0px;box-sizing: border-box;"><strong style="box-sizing: border-box;"><span leaf="">来源</span></strong><span leaf="">：PKMer.cn</span></p><p style="text-align: left;margin: 0px;padding: 0px;box-sizing: border-box;"><strong style="box-sizing: border-box;"><span style="letter-spacing: 0px;box-sizing: border-box;"><span leaf="">排版</span></span></strong><span style="letter-spacing: 0px;box-sizing: border-box;"><span leaf="">：Wis_Ocean</span></span></p></section></section></foreignObject></svg></svg>

![[Read It Later/attachments/e1ec38eeba160023954b173118fdb9a3_MD5.webp]]

点击阅读原文查看更多