---
id: 3aa3ac69-5c5b-4d7c-a5d0-6cfd8bc9a2e0

url: https://pkmer.cn/Pkmer-Docs/03-%E7%9F%A5%E8%AF%86%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7/%E8%87%AA%E5%8A%A8%E5%8C%96%E8%BD%AF%E4%BB%B6/quicker/quicker%E5%8A%A8%E4%BD%9C%E4%B9%8B%E8%87%AA%E5%AE%9A%E4%B9%89zotero%E6%A0%87%E6%B3%A8%E5%88%B0obsidian/
---


tags::  #Readed 

# PKMer_Quicker动作之自定义Zotero标注到Obsidian
#Omnivore

[Read on Omnivore](https://omnivore.app/me/pk-mer-quicker-zotero-obsidian-192900e5053)
[Read Original](https://pkmer.cn/Pkmer-Docs/03-%E7%9F%A5%E8%AF%86%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7/%E8%87%AA%E5%8A%A8%E5%8C%96%E8%BD%AF%E4%BB%B6/quicker/quicker%E5%8A%A8%E4%BD%9C%E4%B9%8B%E8%87%AA%E5%AE%9A%E4%B9%89zotero%E6%A0%87%E6%B3%A8%E5%88%B0obsidian/)

* [回到顶部](#回到顶部)
* [制作 Quiker 动作的思路](#制作-quiker-动作的思路)
* [第一步 获取标注信息和条目信息后正则匹配各个基本元素](#第一步-获取标注信息和条目信息后正则匹配各个基本元素)
* [第二步 根据匹配的元素判断标注类型](#第二步-根据匹配的元素判断标注类型)
* [第三步 通过正则匹配的元素自定义组合粘贴文本格式](#第三步-通过正则匹配的元素自定义组合粘贴文本格式)
* [Quicker 动作的小技巧](#quicker-动作的小技巧)
* [具体操作演示](#具体操作演示)

自动化软件

Quicker动作之自定义Zotero标注到Obsidian 

---

 插件ID：quicker%E5%8A%A8%E4%BD%9C%E4%B9%8B%E8%87%AA%E5%AE%9A%E4%B9%89zotero%E6%A0%87%E6%B3%A8%E5%88%B0obsidian quicker%E5%8A%A8%E4%BD%9C%E4%B9%8B%E8%87%AA%E5%AE%9A%E4%B9%89zotero%E6%A0%87%E6%B3%A8%E5%88%B0obsidian quicker%E5%8A%A8%E4%BD%9C%E4%B9%8B%E8%87%AA%E5%AE%9A%E4%B9%89zotero%E6%A0%87%E6%B3%A8%E5%88%B0obsidian：

> *** Quick 的动作分享：**

之前介绍了一篇 Zotero 无缝衔接 Excalidraw 画板的脚本，但是很多情况我们还是以 Markdown 为主的来记录 Zotero 的文献笔记，本文将介绍如何通过 Quicker 来制作 Zotero 到 Obsidian 的自动化动作，可以根据自己习惯选择性的自定义粘贴格式。

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/af615c315c24e4987a7634912170c30b_MD5.png]]

## 制作 Quiker 动作的思路

首先介绍一下 Zotero 的 Annotation 的组成部分，在 Zotero 设置中编辑器中搜索 `noteTemplates`，可以看到 Zotero 的标注信息组成部分：

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/6f0f85e8c9a9c2570de862e9c037e86d_MD5.png]]

Zotero 的 **标注信息** 部分主要有**高亮 + 引用 + 评论**组成，通过快捷键 `Ctrl + C`，来获取选中的标注信息。通过 `Ctrl + Shift + C` 可以获取当前**条目的基本信息**，包含文件名、条目链接等。

制作 Quicker 的动作的要素就是通过 **标注信息** \+ **条目信息** 拆分出几个基本元素，如：条目名称、外部回链、高亮区域、Comment、作者名等等，然后相互组合成粘贴格式。

## 第一步 获取标注信息和条目信息后正则匹配各个基本元素

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/8b4776826f94c07ce1bb832ba1b76297_MD5.png]]

> *** 注意 Zotero 6 和 Zotero 7 的匹配有点区别**
> 
> Zotero 6 的 RegZoteroComment 为：`annotation=.*\)\) +(.*$)`  
> Zotero 7 的 RegZoteroComment 为：`\)\) +(.*$)`

## 第二步 根据匹配的元素判断标注类型

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/baeaeaba060e17b6514b1d752336d713_MD5.png]]

默认的 Zotero 的框选区域的图片通过 `Ctrl + C` 只能获取外部回链和评论，其他的图片不管拖拽还是粘贴都无法在 Obsidian 正确显示，所以还是要提前复制图片 (Zotero 图片存储位置如下示意图) 到 Obsidian 的笔记库中，通过双链 `![[图片名]]` 来引用了。

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/f8d4035ad628ad7ae9ef8b264bde9943_MD5.png]]

## 第三步 通过正则匹配的元素自定义组合粘贴文本格式

匹配到的各个元素根据自己需求进行组合吧

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/1ccfa1bda628c0ed6cd418a8de1cacb2_MD5.png]]

> *** 在组合元素时，可以根据 ZoteroComment 是否存在来进行不同的组合形式：**
> 
> ![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/a26dd7cbd28ae844b8a9e0d445ccec23_MD5.png]]

## Quicker 动作的小技巧

由于这个 ZoteroToObsidian 的动作只针对 Zotero 就行了，所以在 Quicker 里面设置这个动作的快捷键，直接 `Shift + C` 之后粘贴到 Obsidian 文档中。

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/7a4fdcd28e42443d35b7ed11f40fbfbb_MD5.png]]

## 具体操作演示

![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/3e3283436ef914e674d59eabc0c47ccc_MD5.gif]]

> *** 利用 Zotero 7 来对离线的 HTML 网页进行标注：**
> 
> ![[Omnivore/PKMer_Quicker动作之自定义Zotero标注到Obsidian/attachments/c385ffa19bed974ae03131543a6d7c81_MD5.gif]]

> **讨论**
> 
> 若阁下有独到的见解或新颖的想法，诚邀您在文章下方留言，与大家共同探讨。

知识管理工具Quicker动作之自定义Zotero标注到Obsidian开始Quicker吧Obsidian自定义Excalidraw脚本汇总

