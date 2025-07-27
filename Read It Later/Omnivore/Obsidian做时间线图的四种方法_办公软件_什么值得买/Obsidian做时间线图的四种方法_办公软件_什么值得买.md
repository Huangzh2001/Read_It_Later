---
id: c869b0c1-f564-4c14-8462-48e7963c0d1a

url: https://post.smzdm.com/p/a0xerdd8/
status: readed
---


tags::  #Readed 

# Obsidian做时间线图的四种方法_办公软件_什么值得买
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-19236b58140)
[Read Original](https://post.smzdm.com/p/a0xerdd8/)

9点赞 102收藏 4评论 

[![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/a67d1e72011812383e2a7b1319a3751a_MD5.png]]](https://post.smzdm.com/p/a0xerdd8/pic%5F2/)

前阵子看《翦商》的时候就在想，看这些历史相关的书，能不能把时间节点做成一张时间线图？这个想法就挥之不去了。后来看《戏很多的医学史》的时候这个想法更加强烈了，于是在Obsidian里折腾了一波，今天跟大家分享一下，在Obsidian里通过Mermaid和插件，制作时间线图的方法。

第一种是用Marmaid做甘特图，甘特图的做法我上次已经发过一篇长文了，不再赘述。

[![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/56c375b5bd60fe87dab9006436612a2e_MD5.png]]](https://post.smzdm.com/p/a0xerdd8/pic%5F3/)

文章

![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/0747f02f76592b715f35a2ea0142d210_MD5.png]]

简单、方便的流程图、甘特图做法——Mermaid作图教程

## mermaid 时间线图

mermaid除了甘特图以外，还有名称就是timeline的时间线图。  
与甘特图相比，mermaid的时间线图更强调的是事件发生的具体时间点的顺序，甘特图更强调的是事件的持续时间，表现在图上来看，甘特图每个事件都有一个持续时间的柱子，而时间线图上，每个事件都是一个点。

## 基本语法

mermaid的时间线图语法很简单。

用timeline来激活时间线图。

titile代表图名。

可选的section 在图表的最上方，代表整个时代的名称。随后记录具体时间，以时间:事件的形式记录。如果一个时间点上有多个事件要记录，中间用:分隔即可。

需要注意的是，在mermaid的时间线图中，时间的位置不一定就是时间，也可以是某个“时代”，mermaid也不会按照你的时间替你排序，就按照输入顺序进行排序。

举个例子：

>  
> timeline  
> title Timeline of Industrial Revolution  
> section 17th-20th century  
> Industry 1.0 : Machinery, Water power, Steam  
> power  
> Industry 2.0 : Electricity, Internal combustion engine, Mass production  
> Industry 3.0 : Electronics, Computers, Automation  
> section 21st century  
> Industry 4.0 : Internet, Robotics, Internet of Things  
> Industry 5.0 : Artificial intelligence, Big data,3D printing

[![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/980ba5e1e0b94930ac1882765f259318_MD5.png]]](https://post.smzdm.com/p/a0xerdd8/pic%5F4/)

mermaid的甘特图与时间线图都有一个非常明显的缺陷，他们都是横向表格，不能设置纵向，有没有滚轮设置，因此事件稍微一多，几乎就没法看，必须另谋出路。第三方插件中，相关的有三款，分别是timeline，timelines和timelines（Revamped），timelines（Revamped）是timelines断更后其他作者的改进版，两者大同小异。

## timeline 插件

timeline插件安装后，与mermaid类似，以代码形式制作时间线。在\`\`\`后输入timeline或者timeline-labeled均可。

timeline 激活后每一个事件需要三个+，分别代表时间、标题、内容。与之相对应的，如果用timeline-labeled 激活，就是把加号内容明确掉,date: xxx, title: xxx ,content: xxx。

```` ```timeline + 2021.1.1 + 元旦 + 过元旦节  ````[![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/737cf6cf163b090a6727aa0660079661_MD5.png]]](https://post.smzdm.com/p/a0xerdd8/pic%5F5/)

在阅读模式下显示效果如图。  
需要注意的是，这个的时间与mermaid的timeline图时间一样，并不作为排序依据，同样依靠输入前后顺序来排序。

## timelines 插件

如果一定要找一个终极解决方案，目前来说是timelines插件。

首先要说明的是timelines的使用相比前三种要复杂很多。但是功能上来说要棒很多。在timelines可以将分布在不同文件中，带有timeline的标签的信息整合起来，并从中筛选你设定的特定标签事件，按你的需求做成横向或者纵向的时间线。

timelines插件中记录事件有两种形式：使用HTML语言记录，或者设置在obsidian的文档属性中。HTML语言记录可以在同一个md文件中记录多个事件，适合新建事件记录，当一个事件的内容越来越多，你就可以把他改成一个单独的md文件，设置他的文档属性，方便在timelines中检索。

> HTML格式记录属性如下：  
> class='ob-timelines'  
> data-start-date='2000-10-10-00'  
> data-end-date='2000-10-20-00'  
> data-title='Time Period Event'  
> data-color='orange'  
> data-img='absolute/path/to/image.png'  
> data-type='background'  

其中data-color和data-img为可选项。不填也可以。其他几项为必填项。

发现插入后就不见了？不要急，在设置-外观-css片段中，打开css片段的路径，在其中新建一个css文件，输入以下代码。并启用，你会发现可以正常显示了。

> .ob-timelines {  
> display: inline-block !important;  
> font-style: italic;  
> }  
> / 使用before伪元素显示span或div的属性 /  
> .ob-timelines::before {  
> content: "🔖 " attr(data-date) ": " attr(data-title) ". ";  
> color: lilac;  
> font-weight: 500;  
> }

属性中data-start-date 为事件起始日期，data-end-date为结束日期，需要注意日期需要为YYYY-mm-DD-HH，必须精确到小时，哪怕写成00也行，不然无法正确显示。

data-title是事件名称。data-img是先是在时间线图上的图像，data-type按照解释有point、box、range、background四类，我实际使用感觉没有明显区别，同样目前存在问题的还有data-color，也有问题。

如果把属性做到文档属性里，就是把标签前面的data-拿掉就可以。

更简单的办法是使用ctrp+p，在其中输入timelines，使用其中的两个命令来添加事件。

[![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/f0299aff1f3db8b7ce5838ca0fde8860_MD5.png]]](https://post.smzdm.com/p/a0xerdd8/pic%5F6/)

完成事件添加后，在任意文件中，使用代码，代码中使用ob-timeline就可以显示你的时间线图表。

[![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/4f28a58285db8733dca9c947d92fb8ea_MD5.png]]](https://post.smzdm.com/p/a0xerdd8/pic%5F7/)

今天的分享就到这里啦。目前来说我最满意的还是timelines，但是之前安装的是timelines，没有发现还有后来的修改版，修改版感觉功能更完善，但是在语法细节上有点小不同，只能重新回头去修改之前的记录啦。  
你觉得哪个方法做的时间线图更好呢？

作者声明本文无利益相关，欢迎值友理性交流，和谐讨论～

![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/9ce01f1c0ef1206e27af2288317a05f5_MD5.png]]

* 相关商品推荐

![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/c502cad248a873f2c28ebd6ae19fe1b6_MD5.jpg]]

ihuman 洪恩 识字子集拼音思维ABC会员永久包3-6岁儿童早教启蒙礼物玩具 识字会员终身包

ihuman 洪恩 识字子集拼音思维ABC会员永久包3-6岁儿童早教启蒙礼物玩具 识字会员终身包

_268元起_

![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/294fdae18719e8565891c0c4934403c6_MD5.jpg]]

【买一得二】WPS联合会员 超级会员年卡+网易云音乐年卡 WPS超级会员年卡（赠7天）+网易云音乐年卡

【买一得二】WPS联合会员 超级会员年卡+网易云音乐年卡 WPS超级会员年卡（赠7天）+网易云音乐年卡

_暂无报价_

![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/e3d2350821ebdd7c815e4fefb8f96b01_MD5.jpg]]

WPS 金山软件 超级会员15个月卡+哔哩哔哩大会员年卡

WPS 金山软件 超级会员15个月卡+哔哩哔哩大会员年卡

_暂无报价_

![[Omnivore/Obsidian做时间线图的四种方法_办公软件_什么值得买/attachments/70abc194be455e968b7736691d8beee7_MD5.jpg]]

Microsoft 微软 在线发 office365个人版续费新订microsoft365个人版

Microsoft 微软 在线发 office365个人版续费新订microsoft365个人版

_229元起_

#### 相关文章推荐

