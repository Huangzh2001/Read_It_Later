---
id: 7616cb8a-dd5e-487c-894f-444b143d8e30

url: https://zhuanlan.zhihu.com/p/359570642
status:
---


tags:: 

# 从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-191daf6b361)
[Read Original](https://zhuanlan.zhihu.com/p/359570642)

> 转载自[吕立青](https://zhida.zhihu.com/search?q=%E5%90%95%E7%AB%8B%E9%9D%92&zhida%5Fsource=entity&is%5Fpreview=1)\_JimmyLv [https://sspai.com/post/60802](https://link.zhihu.com/?target=https%3A//sspai.com/post/60802)

最近 Roam Research 开放注册，虽然订阅价格高达 165 美元 / 年，但还是有不少人被这款笔记以及它背后的笔记方法——[卡片盒笔记法](https://zhida.zhihu.com/search?q=%E5%8D%A1%E7%89%87%E7%9B%92%E7%AC%94%E8%AE%B0%E6%B3%95&zhida%5Fsource=entity&is%5Fpreview=1)所吸引。其实卡片盒笔记法已经出现了很久，和 Roam Research 相似的双向链接笔记应用也并不少见，今天我要介绍的 Obsidian 就是其中一款。

在这篇文章中，我将介绍自己基于 Obsidian 对卡片盒笔记法的实践。在考虑使用什么工具之前，你或许可以再仔细了解一下自己是否真的适合这种笔记方法\~

## Zettelkasten 卡片盒笔记法是什么？

简单来说，Zettelkasten 是一种比标签更高级的卡片笔记方法，开智部落王浚宇在《[卡片大法的神奇之处](https://zhida.zhihu.com/search?q=%E5%8D%A1%E7%89%87%E5%A4%A7%E6%B3%95%E7%9A%84%E7%A5%9E%E5%A5%87%E4%B9%8B%E5%A4%84&zhida%5Fsource=entity&is%5Fpreview=1)》提到：

> 卡片是精致小巧的万用盒子：卡片就像生活中我们都会需要的盒子一样，也许男生更倾向于放一些自己珍藏的小物件，姑娘直接当成了首饰盒。和硕大的背包比起来，盒子的容量是有限的，需要想清楚自己要放什么样的东西进去，这样就会降低负荷，并且放进去的东西质量也更高，我们的卡片有些类似，容量小的好处是负荷降低，放进去的是线索、是高质量的内容。

德国社会学者 Niklas Luhmann（[卢曼](https://zhida.zhihu.com/search?q=%E5%8D%A2%E6%9B%BC&zhida%5Fsource=entity&is%5Fpreview=1)）使用 Zettelkasten 卡片盒笔记法写了 70 多本书和 400 多篇学术文章。在 [Zettelkasten — How One German Scholar Was So Freakishly Productive](https://link.zhihu.com/?target=https%3A//writingcooperative.com/zettelkasten-how-one-german-scholar-was-so-freakishly-productive-997e4e0ca125) 这篇文章当中详细介绍了他的写作方法的机理（本节配图均来自这篇文章）。

用文件或文件夹来组织笔记的方式会导致笔记形成僵硬的结构，我们只能通过书本目录组织它，或随着时间不断新增按照时间线组织，而如果我们将每个块（chunk）打散，笔记变得[自由浮动](https://zhida.zhihu.com/search?q=%E8%87%AA%E7%94%B1%E6%B5%AE%E5%8A%A8&zhida%5Fsource=entity&is%5Fpreview=1)，但问题也随之而来：我们很难再追踪到它们之间的相互关系了。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/5584c39c6d180bf2f8e6c0b0bf5e35b4_MD5.jpg]]

接着我们尝试体现知识点之间的关系：大部分人都采用了文件夹或者列表的方式，把这些卡片分门别类归档到不同的文件夹里面，比如[印象笔记](https://zhida.zhihu.com/search?q=%E5%8D%B0%E8%B1%A1%E7%AC%94%E8%AE%B0&zhida%5Fsource=entity&is%5Fpreview=1)的笔记本，或笔记本组。但现实世界的复杂问题，其实不可能只在某一个领域（即文件夹）内找到合适的答案，领域的划分也会限制「创意」或「灵感」的产生。

标签的发明大大改进了笔记系统，但按标签查看笔记也很局限：我们一次只能看到几个标签内的内容，此外的内容则被遮蔽了，因此在组织信息和资料方面实用性并不很高。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/40ae882174cfb8d6165eaa5aba442e56_MD5.jpg]]

所以更好的办法是：我们应该用网络结构（web）来组织我们的笔记 —— 不仅仅依靠标签，还要把所有笔记连接在一起。我们可以每次只关注在这张网络的某个连接点上，但更重要的是，我们同时也能看到更多的联结发生在背后。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/c5f886516b232bbc7ab07a438e796859_MD5.jpg]]

虽然没有学术写作的需求，但除了工作中用到的知识需要保持更新之外，我还有许多其他的项目需要维护，这也要求我不停地迭代更新自己的知识库，并让不同领域的知识、不同渠道收集的知识之间发生关联，因此我入坑了 Zettelkasten 卡片盒笔记法，用它来组织自己的知识。

关联阅读：

* [《如何快速上手卡片笔记法？你想了解的都在这本书里》](https://link.zhihu.com/?target=https%3A//sspai.com/post/60466)
* [《想到写长文就头疼？试试用卡片式写作「拼」一篇文章》](https://link.zhihu.com/?target=https%3A//sspai.com/post/59109)
* [《在这个时代我们该怎样组织知识，又该怎样思考？》](https://link.zhihu.com/?target=https%3A//sspai.com/post/60770)

## Zettelkasten 本质上是一种[渐进式总结方法](https://zhida.zhihu.com/search?q=%E6%B8%90%E8%BF%9B%E5%BC%8F%E6%80%BB%E7%BB%93%E6%96%B9%E6%B3%95&zhida%5Fsource=entity&is%5Fpreview=1)

卡片盒笔记法突出了「建立联系」的重要性，其实有刻意区分了三种类型的卡片笔记，分别如下：

* 文献笔记（Literature Notes）是指 a) 简短地 b) 用自己的话（而非「复制粘贴」）记录你在看的文献笔记，迫使你真正理解原文的意思。
* [书目笔记](https://zhida.zhihu.com/search?q=%E4%B9%A6%E7%9B%AE%E7%AC%94%E8%AE%B0&zhida%5Fsource=entity&is%5Fpreview=1)（Bibliographical Notes）则需要你添加参考信息，将上面的文献笔记跟原文联系起来。而这一步，恰恰是 Roam Research 或 Obsidian 工具发挥价值最大的地方，甚至做到了完全自动化（稍后会进一步解释我的工作流）。
* 永久笔记（Permanent Notes）是最重要的一步，回顾每一个卡片笔记，同时思考它们与你所学的内容、你的兴趣、思考或研究的关系。你的目标不是收集尽可能多的笔记，而是为你现有的想法、论点和讨论增加新的价值。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/cf05f0fc37f7b3c8d739e30ef4e3ad70_MD5.jpg]]

至此，你才算是真正增加了所谓「知识」，这儿会有个 [re-read](https://zhida.zhihu.com/search?q=re-read&zhida%5Fsource=entity&is%5Fpreview=1) 的陷阱：当你回看之前的「收藏」的已读内容时，大脑会因为熟悉感而误以为自己「学到了」，而这恰恰是你之前所有「复制粘贴」的文字最大的问题。

## 哪些笔记值得进入到 Zettelkasten 阅读工作流？

结合 Zettelkasten 卡片盒笔记方法，我在阅读时会遵循这样的工作流：

1. 原文（或书籍），一边阅读一边划线「高亮」
2. 保存所有「高亮」部分（含链接）至笔记文件
3. 新建文献笔记，用自己的话解释「高亮部分」
4. 增加书目笔记，跟原文「高亮」或书籍页码关联起来
5. 创建永久笔记，跟「卡片盒」中已存在的卡片笔记融合起来
6. 当然，最后更重要的是要重复 Review 卡片笔记，能够通过 Anki 间隔重复加强记忆

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/ad4cd08c700427c58c475d81092dce27_MD5.jpg]]

当然，**不是每一条笔记都需要进行 1\~5 所有的步数**，因为不是所有笔记的都有这样的价值。遵循「二八原则」，真正有价值的东西，才会让你有欲望去做完整个流程。我执行中的体验如下：

* 阅读内容来源的 50% 可能会有价值，值得「保存」
* 25% 值得「精读」，进入下一层
* 20% 能被「高亮」
* 只有 5% 才会再次总结和「解释」
* 最初的阅读内容中大概只有 1%，能进入第五层的融合，因为这需要大量的时间和精力。

## 提高认知能力的外部辅助器

唐·诺曼，全球最具影响力的设计师，《[设计心理学](https://zhida.zhihu.com/search?q=%E8%AE%BE%E8%AE%A1%E5%BF%83%E7%90%86%E5%AD%A6&zhida%5Fsource=entity&is%5Fpreview=1)》的作者，苹果的前用户体验[架构师](https://zhida.zhihu.com/search?q=%E6%9E%B6%E6%9E%84%E5%B8%88&zhida%5Fsource=entity&is%5Fpreview=1)，在他的《Things That Make Us Smart 让我们变聪明的事情: 在[机器时代捍卫人类属性](https://zhida.zhihu.com/search?q=%E6%9C%BA%E5%99%A8%E6%97%B6%E4%BB%A3%E6%8D%8D%E5%8D%AB%E4%BA%BA%E7%B1%BB%E5%B1%9E%E6%80%A7&zhida%5Fsource=entity&is%5Fpreview=1)》一书中提到：「人们高估了独立思考的能力。 没有外部帮助，记忆、思维和推理都会受到限制... ...真正的力量来自于设计能够提高认知能力的外部辅助设备。」

所以接下来，我来介绍一款神器，[Obsidian.app](https://link.zhihu.com/?target=https%3A//obsidian.md/) [编辑器](https://zhida.zhihu.com/search?q=%E7%BC%96%E8%BE%91%E5%99%A8&zhida%5Fsource=entity&is%5Fpreview=1)，它就是这样一款能帮我提高认知能力的外部辅助设备。Obsidian 是一款支持 macOS、Windows、Linux 多平台的 Markdown 编辑器，同时也支持双向链接，带有效果相当惊艳的网状笔记视图，它还支持标签管理、多种插件（例如日记、实时预览、星标、自定义 CSS 样式等）。

相较于将服务存储在云端的 Roam Research，Obsidian 最大的好处就是：**它能够跟我基于文件系统的本地化任务管理和[知识管理系统](https://zhida.zhihu.com/search?q=%E7%9F%A5%E8%AF%86%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F&zhida%5Fsource=entity&is%5Fpreview=1)相结合。**我原本的笔记就全部是 Markdown 格式，用 Obsidian 打开后就可以重新对这些笔记进行梳理；即便未来软件停止开发，文件也还在本地，只是在文档中增加了一些双向链接符而已，不会影响文档的正常使用。

不过和 Roam Research 相比，Obsidian 也有缺失的重要功能：[引用区块](https://zhida.zhihu.com/search?q=%E5%BC%95%E7%94%A8%E5%8C%BA%E5%9D%97&zhida%5Fsource=entity&is%5Fpreview=1)（block reference），关于引用区块具体可以参看 [这个视频](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV1X54y197wz%3Fzw) 的 7:00，感谢评论区@[zwithz](https://link.zhihu.com/?target=https%3A//sspai.com/u/zwithz/updates) 的补充。

注：Obsidian 有收费机制，不过无需付费也可正常使用全部功能。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/a18f9c72daf9aac3ab22e7fe26225385_MD5.jpg]]

关联阅读：[《Roam Reasearch 开发注册，年费 1000 元的笔记应用好在哪？》](https://link.zhihu.com/?target=https%3A//sspai.com/post/60787))

这篇文章的写作就全程用 Obsidian 完成，具体步骤大致分为以下四步：

### 1️⃣ 先用自己的话写笔记

首先，使用 Zettelkasten 方法**迫使**你写作。 特别是，根据这种方法，你必须用自己的话写笔记，以确保你将来能够理解它们。 任何一个写过东西的人都知道，把东西写下来会迫使你把模糊的概念变成清晰的想法。

在写作这篇文章时，我先在 Obsidian 中创建了一个卡片笔记 `[[提高认知能力的外部辅助设备]]`，摘录了原文英文部分，底下的中文则是我的[文献笔记](https://zhida.zhihu.com/search?q=%E6%96%87%E7%8C%AE%E7%AC%94%E8%AE%B0&zhida%5Fsource=entity&is%5Fpreview=1)（Literature Notes）。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/403eca493ff9c6a875c5c3f1ae7b38c0_MD5.jpg]]

### 2️⃣ 迫使自己建立笔记链接

其次，无论何时添加新笔记，使用 Zettelkasten 方法要迫使自己查找可以链接到的已有笔记。 这样可以拓宽你的思维，迫使你去思考新的想法和你以前遇到过的其他想法之间的关系。

在记录这段材料时，我知道`[[唐·诺曼]]` 和 `[[Zettelkasten]]`是需要和其他笔记发生关联的概念，因此用[双向链接符](https://zhida.zhihu.com/search?q=%E5%8F%8C%E5%90%91%E9%93%BE%E6%8E%A5%E7%AC%A6&zhida%5Fsource=entity&is%5Fpreview=1)`[[]]` 框起来，它们就显示为紫色，成为了一个可点击的链接。

因为此时写作刚刚开始，还没有其他卡片与之相连，因此右侧的「[双向链接](https://zhida.zhihu.com/search?q=%E5%8F%8C%E5%90%91%E9%93%BE%E6%8E%A5&zhida%5Fsource=entity&is%5Fpreview=1)（Backlinks）」区还没有与之关联的笔记。再接下来，我就可以通过点击紫色链接来创建名为`[[唐·诺曼]]` 和 `[[Zettelkasten]]` 的卡片，然后不同卡片中的概念就连接在了一起。

### 3️⃣ 形成网状结构

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/a924f3415716f5afe569153c92119604_MD5.jpg]]

当我完成建立卡片和建立双向链接的工作，再回到原来的 `[[Zettelkasten]]` 卡片笔记时，我能够看到：

1. `[[Zettelkasten]]` 在整个卡片网络中的位置，以及其相互关联的卡片
2. 卡片主体
3. 则是跟这张卡片相关的双向链接（Backlinks），从而这就触发了笔记的第三步

Zettelkasten 就是关于连接一系列想法的工具。因此，今天你可以有一系列的想法，把它们作为一系列相互联系的记录存储在你的卡片盒当中；然后，在未来的任何时候，你可以通过添加新的记录并将它们与以前的记录联系起来，延续这一系列的思考。

而且，除了我在第二步当中已经绑定好的 `[[]]` 双向链接，它还能发现未未主动链接的想法（Unlinked mentions），从而我可以选择是否主动双向链接。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/91bdee2dc1dca1b1e0ea41fa091dc393_MD5.jpg]]

当然这个时候是最有趣的，因为这主动触发了我之前的卡片笔记，从而以一种新的方式链接到了一起，有一种 大脑被联通的感觉，类似神经元的连接方式。

### 4️⃣ 使用 Anki 间隔重复增强复现几率

其实我还有 Anki 处理的第四步，刚刚描述的是新建卡片和如何链接卡片，其实对于卡片本身来说，我会用 Anki 来特意间隔重复加深记忆，从而在写卡片时能够更加主动地由大脑（而不是由 Zettelkasten 编辑器）来触发我的联想。

[间隔重复](https://zhida.zhihu.com/search?q=%E9%97%B4%E9%9A%94%E9%87%8D%E5%A4%8D&zhida%5Fsource=entity&is%5Fpreview=1)绝对是被认知科学证明是有效的，而对于一个笔记系统来说意料之外的不断重复即 see-also 其实就是一个概念的社交场，我们寄希望于不同的知识点能够相互关联又相互碰撞，在合适的时候出现在我们的面前，唤起或发现可能潜在的一些联系。

通过 [mdanki](https://link.zhihu.com/?target=https%3A//github.com/ashlinchak/mdanki) 自动把卡片笔记转化为 `anki.apkg` 格式并自动打开，即可导入 Anki，然后就可以尽情重复和背诵啦\~ ✌️

```jboss-cli
cdd #alias "cdd=cd ~/Library/Mobile\ Documents/iCloud~co~fluder~fsnotes/Documents"
mdanki Zettelkasten.md ~/Desktop/Anki\ QA\ 笔记本/mdanki.apkg && open ~/Desktop/Anki\ QA\ 笔记本/mdanki.apkg
```

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/06b96d199be55d968dec7cc32e7f25a9_MD5.jpg]]

## 最后也最重要的是：从中找到一个写作的主题

最后呢，找到一个主题来写。其实重复以上这些步骤一段时间后，你就拥有了一张巨大的卡片知识网。现在，每当你需要找一个话题来写的时候，翻出你的卡片盒，就能很快拼装出一篇文章或回答来，写作时完全不必从头开始。

你唯一要做的就是将你的笔记重新组合成一个逻辑顺序，并将它们转化为连贯的东西，即[史蒂芬 · 平克](https://zhida.zhihu.com/search?q=%E5%8F%B2%E8%92%82%E8%8A%AC+%C2%B7+%E5%B9%B3%E5%85%8B&zhida%5Fsource=entity&is%5Fpreview=1)（Steven Pinker）在《风格感觉》所指出的：「写作是将网状的思想，通过树状的句法，组织为线状展开的文字。」

并且在这个过程中，也许你会发现还缺少了什么，或出现了什么新的问题。然后，你就可以进一步阅读并做卡片笔记，进一步完善你的想法和论点，输出倒逼输入，也就是我现在正在做的事情：找一个「卡片盒」方法实践的主题，然后围绕它写了一篇少数派文章，并且在评论中跟大家交流，在分享中继续学习（Learning by Teaching），[费曼](https://zhida.zhihu.com/search?q=%E8%B4%B9%E6%9B%BC&zhida%5Fsource=entity&is%5Fpreview=1)给你听。

最后，再回顾一下我在本文中的四步实践：

1️⃣ 第一步：必须用自己的话写笔记卡片，以确保你将来能够理解。\[\[Literature Notes\]\]

2️⃣ 第二步：无论何时添加新笔记，主动查找可链接到的已有笔记。\[\[Bibliographical Notes\]\]

3️⃣ 第三步：通过添加新笔记并联系旧笔记，延续之前的连续性思考。\[\[Permanent Notes\]\]

4️⃣ 第四步：使用 Anki 间隔重复加深记忆，主动由大脑触发[远程联想](https://zhida.zhihu.com/search?q=%E8%BF%9C%E7%A8%8B%E8%81%94%E6%83%B3&zhida%5Fsource=entity&is%5Fpreview=1)。\[\[Spaced Repetition\]\]

## 下载地址

以往大家好像习惯了整理是基于分类，但其实那仍然是没有整理的笔记，不是有连接的笔记。而 [Zettelkasten 卡片盒笔记法](https://zhida.zhihu.com/search?q=Zettelkasten+%E5%8D%A1%E7%89%87%E7%9B%92%E7%AC%94%E8%AE%B0%E6%B3%95&zhida%5Fsource=entity&is%5Fpreview=1)确实是构建了一个类似互联网的 Web 网状结构，不断点链接了解更多。在大脑中穿梭，好像很神奇的感觉，期待你的亲自体验。

来，[Obsidian.app](https://link.zhihu.com/?target=https%3A//github.com/obsidianmd/obsidian-releases/releases/download/v0.6.5/Obsidian-0.6.5.dmg) 安装包（macOS）给到，你可以尝试一下。也可以直接在 [官网](https://link.zhihu.com/?target=https%3A//obsidian.md/) 下载使用。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/3ae4f0b1b7d9505f8e8c4cff6622110c_MD5.jpg]]

当然，除了 Obsidian 外，你也可以试一下 Roam Research 的 online 编辑器：[https://roamresearch.com/#/app/Note-Tasking](https://link.zhihu.com/?target=https%3A//roamresearch.com/%23/app/Note-Tasking)

还有国内同款：[https://roamedit.com/jx/home.php?plugin=outline/sandbox](https://link.zhihu.com/?target=https%3A//roamedit.com/jx/home.php%3Fplugin%3Doutline/sandbox)

## 结语：自我管理的终点是什么？

在跟朋友聊天时发现一个很好的问题：什么情况下，你不会再继续研究新的自我管理方式了呢？着重指知识管理 + 时间管理这对好兄弟。

Hum 曾经在某一期播客里面提到过 **「[提升阶级](https://zhida.zhihu.com/search?q=%E6%8F%90%E5%8D%87%E9%98%B6%E7%BA%A7&zhida%5Fsource=entity&is%5Fpreview=1)」** 是时间管理最重要的事情，也许吧。之前看[物品整理](https://zhida.zhihu.com/search?q=%E7%89%A9%E5%93%81%E6%95%B4%E7%90%86&zhida%5Fsource=entity&is%5Fpreview=1)，书中提到物品整理是有终点的，只要将每类物品确定了摆放位置，物体移动完毕，用完放回原位，就不需要无限学整理收纳了。

那么我进行知识管理的重点会在哪里？关于这一点，我更愿意按照[稻和盛夫](https://zhida.zhihu.com/search?q=%E7%A8%BB%E5%92%8C%E7%9B%9B%E5%A4%AB&zhida%5Fsource=entity&is%5Fpreview=1)的方式去思考，就是在「修行」中找到自己真正的志向。而这一点，也可以和 [P.A.R.A](https://link.zhihu.com/?target=https%3A//www.notion.so/P-A-R-A-Notion-19909e5aac3049d887197dcfb1e97fd5) 方法相结合，我们要去主动匹配 Project 和 Goal 清单。

因为一个没有相应目标的项目被称为 hobby「兴趣爱好」。如果你没有承诺或还没有完全阐明你想要的结果，那你一定只是为了好玩而随便搞搞；而如果你有了目标而没有相应的项目，那就只能叫 dream「[白日梦](https://zhida.zhihu.com/search?q=%E7%99%BD%E6%97%A5%E6%A2%A6&zhida%5Fsource=entity&is%5Fpreview=1)」，你可能会非常渴望达到这个目标，但如果没有一个一个项目来完成，实际上也不会有任何进展。

![[Omnivore/从卡片链接到大脑联想，基于 Obsidian 的卡片盒笔记法实践 - 知乎/attachments/7d6fc0c362d8982537359c5c8ae1cf69_MD5.jpg]]

## 参考资料  

* [真正的思考技术：来自德国社会学 Niklas Luhmann 的 Zettelkasten 方法](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/XveXTT8GDjFv2rt9iMU2RQ)
* [How to take smart notes，方法及工具 - 少数派](https://link.zhihu.com/?target=https%3A//sspai.com/post/60466)
* [Zettelkasten — How One German Scholar Was So Freakishly Productive](https://link.zhihu.com/?target=https%3A//writingcooperative.com/zettelkasten-how-one-german-scholar-was-so-freakishly-productive-997e4e0ca125)
* [一个笔记系统——如何把 MarginNote3, DEVONThink3, TheBrain11 和 nvALT 当一个 App 使用](https://link.zhihu.com/?target=https%3A//www.bilibili.com/video/BV147411A7CP)

> 转载自吕立青\_JimmyLv [https://sspai.com/post/60802](https://link.zhihu.com/?target=https%3A//sspai.com/post/60802)

