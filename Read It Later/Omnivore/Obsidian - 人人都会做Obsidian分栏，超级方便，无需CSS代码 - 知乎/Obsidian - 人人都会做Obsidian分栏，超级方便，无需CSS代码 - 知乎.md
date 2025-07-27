---
id: c122d456-f1bf-45dd-bf37-dc165edc1899

url: https://zhuanlan.zhihu.com/p/503562540
status:
---


tags::  #Readed 

# Obsidian | 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-obsidian-css-190a4ce595c)
[Read Original](https://zhuanlan.zhihu.com/p/503562540)

大家好！我是BCS\~

## 01 摘要

老规矩，先上图 

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/ad88bb5d1c17acee5d49b0c6cd03ccf3_MD5.jpg]]

如果感觉效果还可以，那就请往下看\~

> 另外，**一定要把推文看完（重要的内容都在最后），不要没看完推文就来问问题**

## 02 引言

昨天交流群里有小伙伴询问关于Obsidian分栏的问题，我很清楚的知道，ob论坛早已有帖子能够实现此需求了。

但是，今天我还是想要分享另外一种实现分栏的方法！

> 感觉要有自己的Slogan了：**寻求最简洁有效的方法来解决现有需求！**

## 03 方法

总之，还是需要借助插件（这是必须的，Ob就是因为有如此庞大的插件系统才能满足不同人的各种需求），此插件名为multi-column-markdown，已上架Ob第三方社区（下载量才1400+,希望今天过后，有个较大的增长），开发者是Cameron Robinson，致敬！

 **接下来简单来讲讲该如何使用此插件？**

### 3.1 安装

* 安装并启用此插件
* 无选项设置，只需设置快捷键（我就不设置了，本人喜欢将常用命令添加到cMenu工具栏），见下图
* 第一个是用来修复多栏区域的ID的，只要一篇笔记中多个多栏区域的ID不重复，一般用不到
* 第二个是用来快捷插入分栏代码的（别害怕，你无需了解此代码，只管运行此快捷键）

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/944f8cd75390c742c3cc1d1cd2c7cab2_MD5.png]]

### 3.2 添加你的一个分栏吧

* 此刻，你可以打开一篇空白文档

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/4b29a0ee310c3ae4570c928390a9e46a_MD5.png]]

* Ctrl+P打开命令窗口，检索co，点击Multi-column

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/a59d77ba5e41cfbe36a67396bba1a9ce_MD5.png]]

* 然后，在你的笔记中将会看到如下代码

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/4b1ccc83a8852ff426dd2b8f68b5bc90_MD5.png]]

看到这条`Number of Columns：2`语句了没，其中的`2`就代表你打算分两栏。如果你要想分3栏，将2改成3即可！

此演示，咱还是分两栏哈\~

* 下面咱们要输入内容了，相信你也看到上图中的`=== end-column ===`代码了，就在此行的**上上**一和下下一行输入你想输入的文字，看一下效果

我输入的是维客笔记1和维客笔记2 

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/0e97c661ec2d093849b256c23b4619db_MD5.png]]

切换为预览模式

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/5a6782a9f1f79f5d1f601c50eb4dbffc_MD5.png]]

不错，确实分成了两栏，但是，框线我觉得很ugly

* 去掉框线

想要去掉框线，咱们需要加一个冒号，两个单词，`border: off`，看下图

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/2ee9ff2fe6ee915f35ed4b78336e1b9f_MD5.png]]

board就是边界的意思，设为off就意味着去掉框线！

此时再切换为预览模式，看一下效果

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/1f48918a6d3df944cfe41f3121b689a1_MD5.png]]

* 还可以给每一栏设置标题，照着下图设置即可，想几级标题就几级标题哈（本人习惯设置二级标题）

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/f466d8b68e929668635413b7ed58bfab_MD5.png]]

预览模式

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/896704942c314a18e854950e7a1fe13b_MD5.png]]

试一下三级标题

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/e510efe2c10a6e40ad2cf7f5bd93aefd_MD5.png]]

* 想要看一下三栏怎么分？可\~

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/078a40334be098afed9008989c1f1411_MD5.png]]

预览模式

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/bf27549b8f151fe7b0f61da5a177d547_MD5.png]]

### 3.3 代码含义

代码含义我是一定要说的（emmm，不是我说的，是开发者说的）

在此插件的安装界面，就有此插件的使用说明和使用案例，请去翻\~

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/bddb7cc621cf2267d24385675a51cb13_MD5.png]]

一个分栏区域包含以下几点：

* 分栏开始语句`=== multi-column-start`：如果一篇笔记中你有多个分栏区域，切记不要有重复ID（有也没啥事，改成不一样的就可）
* 分栏设置区：就是要设置分几栏，要不要框线，其实还可以设置位置，左、右、居中啥的，这个自己看开发者文档哈
* 每一栏的内容：就按照平时输入笔记的方法输入内容就是了
* 每一栏后面都要跟一条结束语句`=== end-column ===`
* 最后一栏内容结束时没有此`=== end-column ===`语句，而是跟此`=== multi-column-end`语句

## 4 注意

相信你一定会遇到bug，此时你的解决方案有3条

* 缩减笔记栏宽
* 切换到另一笔记再切换回来即可
* **以上两条如不能解决，请去给开发者提issue**

## 5 总结

* 打开需要分栏的笔记
* 单击需要分栏的位置
* ctrl+P，检索co，运行Multi-column命令
* 设置栏数和添加去框线语句`board：off`
* 在每一栏中输入笔记内容
* 切换到预览模式，即可看到分栏效果
* 遇到渲染bug：缩减栏宽；切换一下笔记再切回来

**还可以调某一栏的大小**

![[Omnivore/Obsidian - 人人都会做Obsidian分栏，超级方便，无需CSS代码 - 知乎/attachments/882cf665815b69e82d15d863dfedde47_MD5.jpg]]

