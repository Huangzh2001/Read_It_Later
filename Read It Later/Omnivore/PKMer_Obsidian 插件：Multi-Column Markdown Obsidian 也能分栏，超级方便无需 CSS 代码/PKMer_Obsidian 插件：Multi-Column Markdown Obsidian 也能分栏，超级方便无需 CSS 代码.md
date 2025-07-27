---
id: 8ba118de-7e55-4c7e-898d-a2b199a97db3

url: https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/multi-column-markdown/
---


tags::  #Readed 

# PKMer_Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码
#Omnivore

[Read on Omnivore](https://omnivore.app/me/pk-mer-obsidian-multi-column-markdown-obsidian-css-190a4cf0965)
[Read Original](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/multi-column-markdown/)

* [回到顶部](#回到顶部)
* [概述](#概述)
* [效果&特性](#效果特性)
* [使用](#使用)
* [语法参考](#语法参考)  
   * [区域起始标签](#区域起始标签)  
   * [有效的语法标签](#有效的语法标签)
* [已知问题](#已知问题)  
   * [实时预览](#实时预览)  
   * [代码块开始标签](#代码块开始标签)  
   * [次要渲染问题](#次要渲染问题)  
   * [其他](#其他)

obsidian社区插件

Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码 

---

 插件ID：multi-column-markdown multi-column-markdown multi column-markdown：Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码

 该插件名为Multi-Column Markdown，可以在Obsidian的预览模式中创建具

 该插件名为Multi-Column Markdown，可以在Obsidian的预览模式中创建具有多列内容的Markdown文档。它允许用户定义自定义的列布局，并且能够定义列数、宽度、间距、文本对齐等。此外，它还支持Pandoc兼容的语法和完整文档多列自动重排。该插件解决了在Obsidian中创建多列布局的问题，使得用户可以更灵活地组织笔记和文档。插件的安装方式包括从Obsidian社区插件或GitHub仓库进行安装。该插件还存在一些已知问题和限制，例如在Live Preview模式下的一些兼容性问题，以及在文档中使用Pandoc列时的导出问题等。

## 概述

在 Obsidian 的预览模式下创建包含多列内容的 Markdown 文档。

> **插件名片**
> 
> * 插件名称：Multi-Column Markdown
> * 插件作者：ckRobinson
> * 插件说明：在 Obsidian 的预览模式下创建包含多列内容的 Markdown 文档。
> * 插件分类：\[’ 界面相关 ’, ’ 编辑工具 ’, ’ 美化 ’, ‘obsidian 插件 ‘\]
> * 插件项目地址：[点我跳转](https://github.com/ckRobinson/multi-column-markdown)
> * 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?multi-column-markdown)

## 效果&特性

![[Omnivore/PKMer_Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码/attachments/c9af5528765fdcf83d57d7c877c23de2_MD5.png]]

![[Omnivore/PKMer_Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码/attachments/42af847e13d9d4f014cb2b7f44d6c510_MD5.png]]

* 通过命令面板可以快速生成语法模板
* 语法模板里面进行配置，生成对应的填写空间
* 填写空间里面可以放入任意 Markdown 语法内容

## 使用

通过 命令面板，或者自定义快捷键方式，快速输入多栏语法

![[Omnivore/PKMer_Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码/attachments/37c830ef2e92617f054a5ae202a63355_MD5.png]]

* 选择后会自动插入对应的模板
* 代码域内 `star-multi-column` ,表示的是 ID，用于引用
* 代码域内 Number of Columns，代表你需要分栏的数量
* 代码域内 可通过 border 参数:  
   * on：开启多栏的边框  
   * off：关闭，不显示多栏的边框。
* 代码域内 可通过 Largest Column 参数，来控制分栏大小。  
   * 双列或三列布局  
         * Standard：平分  
         * Left：最左侧的大一些  
         * First：左数第一列大一些  
         * Right：最右侧的大一些  
         * Second：左数第二列大一些  
   * 仅使用三列布局  
         * Center：中间列大一些  
         * Third：左数第三列大一些  
         * Middle：中间列大一些
* 代码域内 Shadow 参数  
   * off ，关闭阴影  
   * on ，显示阴影
* 代码域 Column size 参数：控制单栏的大小，仅能用于单列  
   * Small  
   * Medium  
   * Large  
   * Full
* 代码域内 Column Position or Column Location: 参数：仅能用于单列，控制栏的对齐位置  
   * Left  
   * Right  
   * Center  
   * Middle
* 代码域内 Alignment 参数：控制栏内文本对齐方式 - Left (Default) - Center - Right![[Omnivore/PKMer_Obsidian 插件：Multi-Column Markdown Obsidian 也能分栏，超级方便无需 CSS 代码/attachments/11acb140f04dedda4ec88e89aa6ad8f8_MD5.png]]
* 每一栏的内容：就按照平时输入笔记的方法输入内容就是了
* 每一栏后面都要跟一条结束语句\= end-column \=
* 最后一栏内容结束时没有此\= end-column \=语句，而是跟此\=== multi-column-end语句

## 语法参考

### 区域起始标签

每个多列区域必须以以下之一开始：

> \`\`\`start-multi-column   
> ID: A\_unique\_region\_ID  
> \`\`\`

或

> \`\`\`multi-column-start   
> ID: A\_unique\_region\_ID\_1  
> \`\`\`

或

> ::::: {.columns id=A\_unique\_region\_ID\_2}  
> _(有关 Pandoc 的围栏 div 语法的更多信息，请参见下文。)_

在定义起始标签之后，必须为该区域声明一个 ID。如果同一文档中有多个区域，则使用 ID 来区分它们。

每个 ID 在同一文档中必须是唯一的，否则可能会出现意外的渲染问题。可以在多个文档中使用相同的 ID，以便例如在用于您的周期性笔记的模板中使用 ID“dailynote”。

通过使用“插入多列区域”命令（更多信息请参见下文），起始 ID 将预先设置为一个随机生成的 4 个字符的字符串。

您还可以使用“修复缺失的 ID”命令，在当前打开的文档中搜索并为所有缺少 ID 的区域附加随机 ID。

### 有效的语法标签

每种标签类型可以使用以下选项进行定义：

#### 开始多列区域

> \`\`\`start-multi-column  
> ID: A\_unique\_region\_ID  
> _任何其他设置标志（见下文）_  
> \`\`\`

> \`\`\`multi-column-start  
> ID: A\_unique\_region\_ID\_2  
> _任何其他设置标志（见下文）_  
> \`\`\`

> ::::: {.columns id=A\_unique\_region\_ID\_2 _任何其他设置标志（见下文）_}

#### 结束多列区域

\--- end-multi-column\\

\--- multi-column-end\\

> :::  
> _(只有在使用 Pandoc 围栏 div 语法开始一个区域时，此结束区域语法才有效。)_

#### 结束一列

\--- column-end ---\\

\--- end-column ---\\

\--- column-break ---\\

\--- break-column ---\\

> ::: columnbreak  
> :::  
> _(在列断点后需要换行。)_

## 已知问题

### 实时预览

* 任何文件交互都会导致嵌入内容重新加载。  
   * 所有这类问题都是由于 Obsidian 在每次文件交互（点击、按键等）时重新绘制整个编辑器引起的。重新绘制会导致所有嵌入内容重新加载，使它们在屏幕上闪烁。目前还没有解决这个问题的方法。
* 与其他插件的某些交叉兼容性不受支持，无法渲染。  
   * 大多数无法渲染的插件都是更高级的插件，它们会在渲染时逐步加载内容，而不是立即加载。
* 在文档内点击会导致文档在重新定位到光标位置之前闪烁。
* 在编辑器外点击，然后再点击回来，可能会在某些情况下导致视口跳到编辑器底部。

### 代码块开始标签

* 在同时打开同一文档的编辑视图和阅读视图时，使用代码块开始标签会导致渲染问题。

### 次要渲染问题

* 任何列中的一般渲染问题：  
   * 如果列以意外的方式呈现其内容，请尝试切换到一个新文件，然后再切换回来，这通常可以解决问题。
* 在多列区域中输入数据时，数据有时会在预览窗口中的预期位置的上方或下方呈现。当该行靠近列或区域的开头或结尾时，它可能会在错误的列或完全在区域之外呈现。
* 将文本复制并粘贴到区域内的新位置时，预览视图可能无法正确更新。
* 在自动布局或单列之间切换时，区域有时可能会卡在呈现旧布局的状态。
* 自动布局区域有时会卡在非等高状态。  
   * 解决方法：  
         * 切换到另一个文件然后再切换回来，或者关闭并重新打开文件将强制重新加载数据并修复渲染问题。

### 其他

* 使用 pandoc 列导出包含其他嵌入的围栏 div 的文档将无法正确导出。
* 对文档的更改可能需要重新加载文件才能正确更新多列重排。
* 在多列重排中，长段落的文本不会跨列分割，因为 Obsidian 将其呈现为单个内容块。

> **提示**
> 
> 这个方法，会引入一个插件，如果你担心插件的稳定性或是希望更加清爽，那么可以参考别的方法

> **讨论**
> 
> 若阁下有独到的见解或新颖的想法，诚邀您在文章下方留言，与大家共同探讨。

Obsidian如何制作多栏布局cm-editor-syntax-highlight-obsidianediting-toolbarhighlightr-pluginmulti-column-markdownobsidian-columnsobsidian-commentsObsidian社区插件remember-cursor-positiontypewriter-mode

