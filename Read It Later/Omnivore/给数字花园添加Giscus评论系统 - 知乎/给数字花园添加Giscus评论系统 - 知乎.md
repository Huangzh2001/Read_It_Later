---
id: 7ed47557-5d6d-4e56-8eb2-9903ceac5438

url: https://zhuanlan.zhihu.com/p/681343213
status: readed
---


tags::  #Readed 

# 给数字花园添加Giscus评论系统 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/giscus-18f96a9799e)
[Read Original](https://zhuanlan.zhihu.com/p/681343213)

本文首发地址为：[https://blog.rahc.top/article/tech-share-garden-giscus-comment.html](https://link.zhihu.com/?target=https%3A//blog.rahc.top/article/tech-share-garden-giscus-comment.html). 

##  前言

对于自己的数字花园，一开始并没有在评论区和自己的阅读者进行交流互动的打算，主要的原因是考虑到在数字花园中的想法并不成熟，加之数字花园现有的笔记基本是自己学习过程中的笔记，更多的是对自己所学知识的整理。直到昨天在完善自己博客的评论系统，突然想到一个评论系统更能拉近自己和读者之间的交流。面对同样的知识，读者可能会遇到各种各样的问题，希望能与作者进行交流，答疑。所以，决定也给自己数字花园加上一个评论系统。

##  评论系统的选择

在之前写的《[利用Obsidian搭建自己的Digital Garden](https://link.zhihu.com/?target=https%3A//blog.rahc.top/article/tech-share-mydigitalgarden.html)》中已经详细阐述了自己数字花园搭建的流程。数字花园的实现过程是采用了oleeskild开源的插件[obsidian-digital-garden](https://link.zhihu.com/?target=https%3A//github.com/oleeskild/obsidian-digital-garden)。关于评论系统在它的[官方文档](https://link.zhihu.com/?target=https%3A//dg-docs.ole.dev/advanced/guides-and-how-tos/adding-comments/)中，推荐了3种方案，分别是[giscus](https://link.zhihu.com/?target=https%3A//giscus.app/zh-CN)、[utterances](https://link.zhihu.com/?target=https%3A//utteranc.es/)和[disqus](https://link.zhihu.com/?target=https%3A//disqus.com/)。前两种评论都依赖于github账号，考虑到目前数字花园的笔记主要是后端开发和人工智能，受众是程序员，基本上都有github账号，所以选择了giscus进行配置和部署。

giscus是基于Github Discussions实现的评论系统，受utterances的启发。它会使用Github Discussions搜索API来搜索当前页面对应的discussions，即对于当前页面的评论。

1. 点击以下链接在github创建新仓库。

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/3d4122be6828c7214e108ee445dd2719_MD5.jpg]]

2\. 在新建的仓库的settings->general->Discussions ，中打开Discussions功能。

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/71bf0d27fe10b2860a5efff484acb958_MD5.jpg]]

3\. 点击该链接：[https://github.com/apps/giscus](https://link.zhihu.com/?target=https%3A//github.com/apps/giscus)，在github安装giscus插件。

4\. 点击该链接：[https://giscus.app/zh-CN](https://link.zhihu.com/?target=https%3A//giscus.app/zh-CN)，对giscus进行配置，把giscus关联到步骤1创建的新仓库

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/1f9107b174d807967ff27d73d592e319_MD5.jpg]]

5\. 复制以下代码，等待后续步骤的使用。

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/a245dfcc2d9e6de0e9633e8006647de3_MD5.jpg]]

6\. 配置数字花园仓库，这里我推荐用[GitHub Desktop](https://link.zhihu.com/?target=https%3A//desktop.github.com/)拉取数字花园仓库，再用[vscode](https://link.zhihu.com/?target=https%3A//code.visualstudio.com/)编辑，然后再用GitHub Desktop提交并推送到远程仓库的方式。

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/9a3d29902c5bfa9856d94b6ccea10dae_MD5.jpg]]

  
在`src/site/_includes/components/user` 目录下，我们可以给自己的数字花园添加自定义的组件。由于我们是给我们的每篇笔记页面都添加一个评论，所以在该目录下新建`notes/footer` 目录，在该目录下添加如下文件`001-giscus-comment.njk` ，文件名除了扩展名`.njk` 外，名字可以随意。文件内容为步骤5中的内容。

```haskell
<script src="https://giscus.app/client.js"
 data-repo="github用户名/步骤1创建的仓库名"
 data-repo-id="你的date-repo-id"
 data-category="Announcements"
 data-category-id="你的data-category-id"
 data-mapping="pathname"
 data-strict="0"
 data-reactions-enabled="1"
 data-emit-metadata="0"
 data-input-position="bottom"
 data-theme="preferred_color_scheme"
 data-lang="zh-CN"
 crossorigin="anonymous"
 async>
</script>

```

7\. 修改页面布局。编辑`src/_includes/layouts/note.njk` 文件。 默认的布局是如图所示，分为左、中、右：

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/f91376a456941af4fe61f04a7ed874a6_MD5.jpg]]

  
 如果不修改，它会在最底层生成一个横跨左、中、右的一个评论区域，影响美观。而我只是想在中间的底部，加上一个评论区域。在`note.njk` 文件的`<main>...</main>` 之间添加如下代码：

```django
<main>
 // 底部添加如下代码
 {% for imp in dynamics.notes.footer %}
   {% include imp %}
  {% endfor %}
</main>
```

  
 注释掉main之后，body内相同的代码：

```crystal
<body>
 {# {% for imp in dynamics.notes.footer %}
   {% include imp %}
  {% endfor %} #}
  {%include "components/lucideIcons.njk"%}
</body>
```

  
 现在的布局如图所示：

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/2588240431bf3a4f79dab53e0e497ef9_MD5.jpg]]

8\. 最终的效果如图所示：

![[Omnivore/给数字花园添加Giscus评论系统 - 知乎/attachments/4cd43dce65c419997d29c63848a26552_MD5.jpg]]

  
最后，欢迎您到[我的数字花园](https://link.zhihu.com/?target=https%3A//garden.rahc.top/)逛逛，一起进步成长，学有所成。

##  总结归纳

本文简单讲述了如何为自己的数字花园添加giscus评论系统。

##  引用或提到的资源

* Mr.Charley. 利用Obsidian搭建自己的Digital Garden. [https://blog.rahc.top/article/tech-share-mydigitalgarden](https://link.zhihu.com/?target=https%3A//blog.rahc.top/article/tech-share-mydigitalgarden).
* oleeskild. obsidian-digital-garden. [https://github.com/oleeskild/obsidian-digital-garden](https://link.zhihu.com/?target=https%3A//github.com/oleeskild/obsidian-digital-garden).
* giscus. [https://giscus.app/zh-CN](https://link.zhihu.com/?target=https%3A//giscus.app/zh-CN).
* utterances. [https://utteranc.es/](https://link.zhihu.com/?target=https%3A//utteranc.es/).
* disqus. [https://disqus.com/](https://link.zhihu.com/?target=https%3A//disqus.com/).
* GitHub Desktop. [https://desktop.github.com/](https://link.zhihu.com/?target=https%3A//desktop.github.com/).
* vscode. [https://code.visualstudio.com/](https://link.zhihu.com/?target=https%3A//code.visualstudio.com/).

​ 有关在数字花园中部署giscus上的问题，欢迎您在底部评论区留言，一起交流\~

