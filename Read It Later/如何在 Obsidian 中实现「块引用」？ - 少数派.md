---
date: 2026-04-16T11:16:43+08:00
url: https://sspai.com/post/61741
status: readed
---
[

共创

](/create)

[

PRIME

](/prime)

[

Matrix

](/matrix)

[

栏目

](/series)

Pi Store

无需申请，自由写作

任何用户都可使用写作功能。成功发布 3 篇符合基本规则的内容，可成为正式作者。[了解更多](https://manual.sspai.com/guide/init/)

    

![](https://cdnfile.sspai.com/2020/08/02/966fe4f30bc3a0d15b5e9a9fa3804d4e.jpg?imageMogr2/auto-orient/format/webp/ignore-error/1)

如何在 Obsidian 中实现「块引用」？

主作者

[![宽治](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!72x72r/gravity/center/crop/72x72/format/webp/ignore-error/1)](/u/hyd4bsqs/updates) [![](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!100x100r/gravity/center/crop/100x100/format/webp/ignore-error/1)](/u/hyd4bsqs) 

宽治

少数派作者

intheflux.substack.com

[

宽治

](/u/hyd4bsqs/updates)[![](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!100x100r/gravity/center/crop/100x100/format/webp/ignore-error/1)](/u/hyd4bsqs) 

宽治

少数派作者

intheflux.substack.com

联合作者

 [![宽治](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!72x72r/gravity/center/crop/72x72/format/webp/ignore-error/1)](/u/hyd4bsqs/updates) [![](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!100x100r/gravity/center/crop/100x100/format/webp/ignore-error/1)](/u/hyd4bsqs) 

宽治

少数派作者

intheflux.substack.com

[

宽治

](/u/hyd4bsqs/updates)[![](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!100x100r/gravity/center/crop/100x100/format/webp/ignore-error/1)](/u/hyd4bsqs) 

宽治

少数派作者

intheflux.substack.com

2020/08/02 00:36

## 引子

不少朋友都很喜欢 Roam Research 的 block reference（块引用）功能，而这也是那些使用 Obsidian 或其他基于纯文本的网络化笔记应用的朋友们一个不小的遗憾。（[什么是 block reference？](https://sspai.com/post/60588#:~:text=%E5%8F%8C%E5%90%91%E9%93%BE%E6%8E%A5%E2%80%94%E2%80%94%E4%B8%80%E7%A7%8D%E5%85%A8%E5%B1%80%E5%8F%98%E9%87%8F,%E6%88%91%E8%AE%A4%E4%B8%BA%EF%BC%8C%E8%BF%99%E6%89%8D%E6%98%AF%E5%8F%8C%E5%90%91%E9%93%BE%E6%8E%A5%E7%9C%9F%E6%AD%A3%E5%BC%BA%E5%A4%A7%E7%9A%84%E5%9C%B0%E6%96%B9%EF%BC%9A%E6%97%A2%E5%BB%BA%E7%AB%8B%E4%BA%86%E4%BF%A1%E6%81%AF%E7%9A%84%E5%85%B3%E8%81%94%EF%BC%8C%E5%8F%88%E5%8F%AF%E4%BB%A5%E8%BD%BB%E6%9D%BE%E5%9C%B0%E4%BF%9D%E6%8C%81%E4%BF%A1%E6%81%AF%E7%9A%84%E6%9B%B4%E6%96%B0%E3%80%82)）Roam Research 的 block reference 系统之所以如此强大，是因为它将每个 block 都视作了一个独立的、带有 id 的数据对象；而基于纯文本文件的笔记应用之所以做不到类似的功能，也正是因为这些文本文件内部的段落无法被识别为独立的对象。这是一种天生的差异。

但是话又说回来，Roam Research 中的 block reference 格式是专属性的，很难迁移到别的平台上使用。有没有什么办法可以在保持纯文本结构的前提下实现对部分内容块进行引用呢？

答案当然是肯定的。下面我就以 Obsidian 为例，介绍三种可行的方法。

## 方法一：重新理解 Block （最推荐的方法）

此法有点「无招胜有招」的意思，它也是我本人最推荐的方式，因为它很符合卡片系统的理念，也更具有通用性。

在拙文[《Roam Research Report——理念与功能》](https://sspai.com/post/60588)中，我曾提到「[页面就是大一点的 Block，而 Block 就是小一点的页面](https://sspai.com/post/60588#:~:text=%E7%94%9A%E8%87%B3%E6%9B%B4%E6%9E%81%E7%AB%AF%E4%B8%80%E7%82%B9%E6%9D%A5%E8%AF%B4%EF%BC%8C%E5%9C%A8%20Roam%20Research%20%E4%B8%8A%EF%BC%8C%E9%A1%B5%E9%9D%A2%E5%B0%B1%E6%98%AF%E5%A4%A7%E4%B8%80%E7%82%B9%E7%9A%84%20Block%EF%BC%8C%E8%80%8C%20Block%20%E5%B0%B1%E6%98%AF%E5%B0%8F%E4%B8%80%E7%82%B9%E7%9A%84%E9%A1%B5%E9%9D%A2%E3%80%82)」这么一个观点。当时我想要说明的是，block 可以像 page 那样被使用与引用，并分析了[实现这一功能的原理](https://sspai.com/post/60588#:~:text=%E4%B9%9F%E5%B0%B1%E6%98%AF%E8%AF%B4%EF%BC%8C%E6%AF%8F%E4%B8%80%E4%B8%AA%20block%20%E9%83%BD%E5%8F%AF%E4%BB%A5%E4%BF%9D%E5%AD%98%E4%BA%94%E9%A1%B9%E4%BF%A1%E6%81%AF%EF%BC%9A1.%20block%20%E6%9C%AC%E8%BA%AB%E7%9A%84%E5%86%85%E5%AE%B9%EF%BC%9B2.%20block,%E7%9A%84%E5%9C%B0%E5%9D%80%EF%BC%9B5.%20%E5%BC%95%E7%94%A8%E4%BA%86%E8%AF%A5%20block%20%E7%9A%84%E5%85%B6%E4%BB%96%20block%20%E7%9A%84%E5%9C%B0%E5%9D%80%E3%80%82)；但反过来讲，既然 page 就是大一点的 block，那么我们何不把 block 的内容直接以  page （也就是 Obsidian 的文档）的形式进行呈现及引用呢？

借用「卡片笔记」这个概念，那么其实每个可被引用的内容都可以被视作是一张卡片，不管它是 page（文档）还是 block （段落）。不要觉得用一个文档写一句话是一种「浪费」，想象一张纸质的卡片能记录的内容只会更少，不也一样能完成使命嘛？

对于在一个文档里只写一段话这种做法，也能会让不少人感到不适。但我们之所以会感觉有些别扭，只是因为我们习惯了把笔记写得很详细，而没有学会如何压缩信息。（这里推荐 Tiago Forte 的文章[《Progressive Summarization》](https://fortelabs.co/blog/progressive-summarization-a-practical-technique-for-designing-discoverable-notes/)  以及少楠非常优秀的[编译](https://index.pmthinking.com/Progressive-Summarization-3a8c5d77b5be42c58719d174bfbfa935)）。实际上，使用「卡片」这一类比，能够非常直接地提醒我们去对信息进行提纯。

当然，「一个文档一句话」也无法适应所有情况，这时我们可以使用 Obsidian 自带的标题引用的功能，通过 `[[title#heading]]`这个方法，在文档中插入其他文档某一级标题下的内容，或通过 `![[title#heading]]`进行嵌入。

![](https://cdnfile.sspai.com/2020/08/02/cb077b030e2d91c943378d27058bb6be.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

嵌入其他文档中标题下内容效果

虽然这种方法无法像 Roam Research 那样实现回车即生成新 block 的效果，**但这个方法让我们的关注点从功能转向了结果，**直接指向「撰写更好的笔记，并建立联系」这个更高一层的目标，并基本满足了块内容引用的需求。

## 方法二：用 Quicker 建立引文系统 （最直观的方法，但不推荐）

如果你安装了 Quicker 这款应用的话，那么可以通过[「引用块」](https://getquicker.net/Sharedaction?code=1ac2f804-1444-4897-72e8-08d8309f8f6f)这个脚本，建立引文系统来实现块引用。

第一次使用时，会需要选中 vault 文件目录进行关联。关联之后就会生成一个👉为标题的文件，里面将放置被引用的文本，并建立索引。

![](https://cdnfile.sspai.com/2020/08/02/075388d17f775d803fd09dbb73555559.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

会生成一个👉**文件**

![](https://cdnfile.sspai.com/2020/08/02/9cab0d6a38a6f628fb2164dcbfad191f.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

里面是引用的句子及文件名

每次使用时，只需要高亮需要引用的文字，然后选择引用块脚本，并在弹出的对话框中选择「>收藏『所选文本』」。在需要使用时，再次点击脚本，选择相应已收藏的引文即可。

![](https://cdnfile.sspai.com/2020/08/02/88a5d0067489756005e9203cc9c49d41.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

但是，这个引文系统非常的脆弱，基本经不起任何折腾，如果你删除了一些文件，或者是不小心修改了引文索引文件，都会导致整个系统出现混乱。

同时，这个引文系统需要先制作引文，再引用制作好的引文，与我们一般的写作流程不符。且一旦引文变多，搜索就变得比较麻烦。

因此，在这里并不推荐这种方法。

## 方法三：修改 CSS 样式 （对第一种方式的优化）

第一种方法会显示被引用内容的标题，有些人会觉得看着碍眼。那么我们其实可以通过修改 Obsidian 的主题，来隐藏嵌入内容的标题。

首先，打开 Obsidian 的设置菜单，选中 Custom CSS 选项。（可能需要再选中任何一个新的主题进行应用）

然后，打开 Vault 目录中新生成的 obsidian.css 文件，加入如下代码     

```
.markdown-embed-content>h1:first-child,
.markdown-embed-content>h2:first-child,
.markdown-embed-content>h3:first-child,
.markdown-embed-content>h4:first-child,
.markdown-embed-content>h5:first-child,
.markdown-embed-content>h6:first-child {
	display: none;
}
```

再次嵌入内容的时候，就会显示如下效果

![](https://cdnfile.sspai.com/2020/08/02/e342d0230731c42cf085a4bc7af30a09.png?imageView2/2/w/1120/q/90/interlace/1/ignore-error/1/format/webp)

嵌入不显示标题的段落

以上就是在 Obsidian 中（kinda）实现「块引用」的方法。

不过到头来，似乎「块引用」也并不是那么地重要，问题的根本解决还是得从笔记思维入手。24

14扫码分享

目录 0

讨论

发表评论

[#笔记应用](/tag/笔记应用)

24

等 24 人为本文章充电扫码分享举报本文章

[![宽治](https://cdnfile.sspai.com/2022/04/22/e0e8edb68cec0d346d48462f0fec062b.jpg?imageMogr2/auto-orient/thumbnail/!84x84r/gravity/center/crop/84x84/format/webp/ignore-error/1)](/u/hyd4bsqs/updates)

[

宽治

](/u/hyd4bsqs/updates)

intheflux.substack.com

全部评论(14)

![[Read It Later/attachments/84e04d9a6b34c9f4caa6066b9ef610a3_MD5.png]]

请在登录后评论...

更多

关联阅读

请绑定手机号码[

关注公众号 sspaime

![[Read It Later/attachments/e9cbb4a3eeabc4675b58906e427dacfe_MD5.png]]

](https://mp.weixin.qq.com/mp/profile_ext?action=home&__biz=MzU4Mjg3MDAyMQ==&subscene=0#wechat_redirect)[下载 App](https://sspai.com/page/client) [联系我们](mailto:contact@sspai.com) [商务合作](https://sspai.com/page/bussiness) [关于我们](https://sspai.com/page/about-us) [用户协议](https://sspai.com/page/agreement)

© 2013-2026 深圳市烧麦网络科技有限公司 - 少数派 [粤ICP备09128966号-4](https://beian.miit.gov.cn/) | [粤B2-20211534](https://dxzhgl.miit.gov.cn/)

- 
- [发送邮件](mailto:contact@sspai.com)
- [商务合作](https://sspai.com/page/bussiness)
- [少数派 App](https://sspai.com/page/client)

请用微信手机端扫码咨询客服

![[Read It Later/attachments/b2549debfd281666394d018b3d6d670b_MD5.png]]

  <iframe style="display: none;"></iframe>

❌ 未收藏