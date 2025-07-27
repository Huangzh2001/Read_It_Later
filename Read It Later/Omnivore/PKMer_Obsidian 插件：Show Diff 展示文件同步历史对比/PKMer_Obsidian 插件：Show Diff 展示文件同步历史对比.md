---
id: 87ee09e7-d5d9-4645-bb2d-7ea2a09bb025

url: https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/show-diff/
status: readed
---


tags::  #Readed 

# PKMer_Obsidian 插件：Show Diff 展示文件同步历史对比
#Omnivore

[Read on Omnivore](https://omnivore.app/me/pk-mer-obsidian-show-diff-191e6382625)
[Read Original](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/show-diff/)

* [回到顶部](#回到顶部)
* [概述](#概述)
* [效果&特性](#效果特性)
* [使用](#使用)  
   * [dates](#dates)  
   * [commits](#commits)  
   * [路径](#路径)  
   * [exclude](#exclude)  
   * [命令：生成今天的差异代码块](#命令生成今天的差异代码块)

obsidian社区插件

Obsidian 插件：Show Diff 展示文件同步历史对比 

---

 插件ID：show-diff show-diff show diff：在Obsidian文件中呈现Git差异

这个插件可以在Obsidian笔记中渲染Git diff输出，让你可以方便地查看代码变动。你可以使用它结合obsidian-git来查看自己在某一天的工作内容，也可以指向文件系统中的任何仓库。插件会渲染带有`show-diff`语言标记的Markdown代码块。你可以通过指定日期、提交、路径和排除项来定制显示内容。此外，插件还提供了一个命令，可以快速在笔记中插入当天的diff代码块。如果你发现了bug或有改进的想法，可以在GitHub上创建issue或者提出pull-request。你也可以通过购买咖啡来支持插件的开发者。

 这个插件可以在Obsidian笔记中渲染Git diff输出，让你可以方便地查看代码变动。你可以使用它结合obsidian-git来查看自己在某一天的工作内容，也可以指向文件系统中的任何仓库。插件会渲染带有\`show-diff\`语言标记的Markdown代码块。你可以通过指定日期、提交、路径和排除项来定制显示内容。此外，插件还提供了一个命令，可以快速在笔记中插入当天的diff代码块。如果你发现了bug或有改进的想法，可以在GitHub上创建issue或者提出pull-request。你也可以通过购买咖啡来支持插件的开发者。

## 概述

将其与 obsidian-git 组合使用，以便在给定的一天中对所做的工作进行修订，就像自动生成的更改日志一样，但您可以将其指向文件系统中的任何存储库。

即有了这个插件，你可以精准控制你编辑的变动历史。

> **插件名片**
> 
> * 插件名称：Show Diff
> * 插件作者：Ivan Lednev
> * 插件说明：在 Obsidian 文件中呈现 Git 差异
> * 插件分类：\[‘obsidian 插件 ‘\]
> * 项目地址：[点我访问](https://github.com/ivan-lednev/obsidian-automatic-changelog)
> * 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?show-diff)

## 效果&特性

![[Omnivore/PKMer_Obsidian 插件：Show Diff 展示文件同步历史对比/attachments/e9ea601a4104a2631230f1fb6d4b4208_MD5.png]]

## 使用

要使插件在您的 vault 上工作，它应该是一个 git 仓库。您可以使用 [obsidian-git](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/obsidian-git) 为您的 vault 添加自动 git 备份。

该插件使用 `show-diff` 语言标签来渲染 Markdown 代码块。一个空的代码块将显示今天和昨天之间的差异：

### dates

使用 `dates` 可以指定一个日期范围来显示更改：

### commits

使用 `commits` 可以指定一个提交范围来显示更改：

```sql
```show-diff
commits:
  from: HEAD^
  to: HEAD
```
```

### 路径

默认情况下，该插件会指向您所在的保险库，但您可以将插件指向文件系统中的任何存储库：

```sql
```show-diff
路径：/path/to/my-pet-project
```
```

### exclude

默认情况下，`.obsidian`（Obsidian 的设置和缓存）被排除在外。您可以使用单个路径覆盖此设置：

```arcade
```show-diff
exclude: trash
```
```

或者使用路径列表覆盖：

```markdown
```show-diff
exclude:
  - trash
  - archive
  - .obsidian
```
```

### 命令：生成今天的差异代码块

该插件提供了一个命令，可以快速在笔记中插入一个类似于以下的代码块：

> **讨论**
> 
> 若阁下有独到的见解或新颖的想法，诚邀您在文章下方留言，与大家共同探讨。

obsidian-gitObsidian社区插件show-diff

