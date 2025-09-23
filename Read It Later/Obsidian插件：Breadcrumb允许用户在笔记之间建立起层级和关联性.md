---
date: 2025-09-23T12:32:34+08:00
url: https://zhuanlan.zhihu.com/p/672016144?utm_id=0
status: readed
---
[

关注

](https://www.zhihu.com/follow)[

推荐

](https://www.zhihu.com/)[

热榜

](https://www.zhihu.com/hot)[

专栏

](https://www.zhihu.com/column-square)[

圈子

New

](https://www.zhihu.com/ring-feeds)

[

付费咨询

](https://www.zhihu.com/consult)[

知学堂

](https://www.zhihu.com/education/learning)

[直答](https://zhida.zhihu.com/)

[

创作中心

](https://www.zhihu.com/creator)

Obsidian插件：Breadcrumb允许用户在笔记之间建立起层级和关联性

首发于[obsidian教程](https://www.zhihu.com/column/c_1688254260465414144)

![[Read It Later/attachments/757255c3aa9e39862586a524f8905630_MD5.png]]

# Obsidian插件：Breadcrumb允许用户在笔记之间建立起层级和关联性

[![[Read It Later/attachments/52fac3ff9ac7e2caa9e9f125ee64a6eb_MD5.png]]](https://www.zhihu.com/people/yrzx404)

[程序员老鬼](https://www.zhihu.com/people/yrzx404)

​![[Read It Later/attachments/5745a448859ae36ec06cc04d38e7b515_MD5.png]]

公众号：程序员老鬼

[

收录于 · obsidian教程

](https://www.zhihu.com/column/c_1688254260465414144)

2 人赞同了该文章

Obsidian是一款极具灵活性的笔记软件，而其众多插件更是为用户提供了额外的便利和功能。其中，[Breadcrumb](https://zhida.zhihu.com/search?content_id=237466608&content_type=Article&match_order=1&q=Breadcrumb&zhida_source=entity)插件就是一个强大的工具，它允许用户在笔记之间建立起层级和关联性。

![[Read It Later/attachments/3371e4fc0e5eb2cbe9c0e9e6b6677ccd_MD5.jpg]]

接下来，我将为你详细介绍Breadcrumb插件的功能、使用方法和实际应用场景。

## **1Breadcrumb插件简介**

Breadcrumb插件为Obsidian添加了多种新视图，允许用户以层级元数据的方式组织笔记。这种层级结构的建立，依赖于特定的元数据标记，包括但不限于上级（parent）、同级（sibling）、下级（child）等关系。通过这些关系，用户可以清晰地理解和管理笔记之间的关系。

## **3安装与设置**

**1.在线安装（需要科学上网）：**  

点击“社区插件”下的“浏览”按钮，在左上角的搜索框中搜索“Breadcrumb”，然后点击“安装”按钮。  
启用插件：安装成功后，点击“启用”以启用插件。

![[Read It Later/attachments/34432e580f79d44b639faa6c3f863e48_MD5.jpg]]

  
**2.离线安装：**  
**因为网络原因很多同学无法直接在线安装obsidian插件，这里我已经把obsidian所有热门插件下载好了**  
查看这篇文章：  
**配置元数据：**Breadcrumb插件需要用户在笔记中设置特定的元数据来表示层级关系。这些元数据可以通过两种方式添加：

[Frontmatter](https://zhida.zhihu.com/search?content_id=237466608&content_type=Article&match_order=1&q=Frontmatter&zhida_source=entity)字段：在笔记顶部以YAML格式添加，如下例所示：

```
---
```

内联元数据（需要Dataview插件支持）：在笔记正文中添加，例如：

```
这是一篇关于金融的笔记。（parent:: [[金融基础]]）
```

## **4Breadcrumb的主要功能**

### **1\. 层级关系视图**

- 列表/矩阵视图：显示当前笔记的上级、同级和下级笔记。可以在侧边栏打开，操作方式是通过命令面板（Ctrl+P）运行「Breadcrumbs: Open View」命令。
- Breadcrumb Trail视图：显示从你的知识库顶部到当前笔记的路径。这有助于理解笔记之间的关联和路径。
![[Read It Later/attachments/18c013556cc5a2c38839cacacce3bb95_MD5.jpg]]

### **2\. Juggl集成**

Breadcrumb与Juggl插件紧密集成。Juggl视图可以自动添加到当前笔记之上，展示笔记之间的关系图。

## **5实际应用案例**

**课程笔记组织：**

- 假设你正在学习金融课程，你可以创建多个笔记，如「金融基础」、「金融高级」等，并通过Breadcrumb插件建立它们之间的层级关系。
- 例如，在「金融基础」笔记中，可以设置下级笔记为具体的课程内容，如讲座、小组工作等。

**项目管理：**

在管理一个项目时，你可以为每个项目阶段创建一个笔记，并使用Breadcrumb插件来表示它们之间的顺序和依赖关系。

比如，你可以将设计阶段设置为开发阶段的上级笔记。

**知识框架构建：**

对于复杂的知识体系，例如编程语言或历史事件，你可以通过Breadcrumb插件建立它们之间的层级和逻辑关系，以便更好地理解和记忆。

## **6结语**

Breadcrumb插件是Obsidian用户的强大助手，能够有效地帮助你管理和理解笔记之间的层级关系。无论是学习、工作还是个人知识管理，利用好这个插件，都能大大提升你的笔记效率和质量。

更多内容查看这篇文章：[所属专栏 · 2023-12-13 15:16 更新](https://zhuanlan.zhihu.com/c_1688254260465414144)

[![[Read It Later/attachments/e540cfa8277e66ea6e338f492f7cdd09_MD5.png]]

obsidian教程

![[Read It Later/attachments/52fac3ff9ac7e2caa9e9f125ee64a6eb_MD5.png]]

程序员老鬼

80 篇内容 · 394 赞同

](https://zhuanlan.zhihu.com/c_1688254260465414144)

[

最热内容 ·

彻底解决！obsidian 多设备同步难题

](https://zhuanlan.zhihu.com/c_1688254260465414144)

发布于 2023-12-13 15:14・四川

[

Obsidian

](https://www.zhihu.com/topic/21349840)

[

插件

](https://www.zhihu.com/topic/19561210)

[

Obsidian记录

](https://www.zhihu.com/topic/26573377)

![[Read It Later/attachments/26725aa9602db156eaafd2cb68a4a816_MD5.jpg]]

发首评

  

还没有评论，发表第一个评论吧

关于作者

[![[Read It Later/attachments/52fac3ff9ac7e2caa9e9f125ee64a6eb_MD5.png]]](https://www.zhihu.com/people/yrzx404)

[程序员老鬼](https://www.zhihu.com/people/yrzx404)​![[Read It Later/attachments/5745a448859ae36ec06cc04d38e7b515_MD5.png]]

公众号：程序员老鬼

[

回答

**819**

](https://www.zhihu.com/people/yrzx404/answers)[

文章

**610**

](https://www.zhihu.com/people/yrzx404/posts)[

关注者

**10,843**

](https://www.zhihu.com/people/yrzx404/followers)

### 推荐阅读

[

![[Read It Later/attachments/ade1a9d8f4cd5be5579a732bb1f1e5af_MD5.png]]

# Obsidian插件：Various Complements让你的笔记体验更加流畅

程序员老鬼发表于obsid...

](https://zhuanlan.zhihu.com/p/666832898)[

![[Read It Later/attachments/61116e17f47d75f4fcacda11ee481dd6_MD5.jpg]]

# 体验更佳，这款插件优化了Obsidian的PDF阅读、批注功能

致九

](https://zhuanlan.zhihu.com/p/708953949)[

# obsidian适合你使用吗？一篇文章搞清楚

obsidian官网： 黑曜石 - 磨砺你的思维 (obsidian.md) obsidian是一款笔记软件，首先，千万不要觉得这个软件复杂，你不一定要用到它的所有功能，你可以像使用备忘录、Word一样无门槛地直接…

莫奈

](https://zhuanlan.zhihu.com/p/787788653)[

![[Read It Later/attachments/2beb678c36c9554ec4f62a85a938dad6_MD5.png]]

# Obsidian进阶必备！这5个插件让你的笔记效率飞起！

旷野发表于Obsid...

](https://zhuanlan.zhihu.com/p/31310864072)

❌ 未收藏