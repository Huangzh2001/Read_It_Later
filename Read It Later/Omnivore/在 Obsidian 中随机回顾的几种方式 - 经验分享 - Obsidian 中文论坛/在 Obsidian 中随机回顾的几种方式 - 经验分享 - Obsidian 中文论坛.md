---
id: 782e7b3d-2e86-4cf4-8c50-02302f375324

url: https://forum-zh.obsidian.md/t/topic/35076
status: readed
---


tags::  #Readed 

# 在 Obsidian 中随机回顾的几种方式 - 经验分享 - Obsidian 中文论坛
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-obsidian-191feecacc9)
[Read Original](https://forum-zh.obsidian.md/t/topic/35076)

笔记在记录之后，还需要不断回顾。

在 Obsidian 中随机回顾有这么几种方式，可以帮助我们重新遇见曾经写下的笔记。

### [](#h-1)核心插件：漫游笔记

最简单的方式就是启用 obsidian 自带的核心插件，在设置中开启后，工具栏会出现一个骰子图标，点击就会随机打开笔记库中的文件，很简单粗暴，也很好用。虽然是如此简单的功能，我发现很多笔记软件并不具备，不免有些可惜。

### [](#smart-random-note-2)第三方插件：Smart Random Note

这个插件其实就是加强版漫游笔记。除了随机打开库内笔记，还有另外两个新增的命令，一个是随机打开特定标签的笔记，另外一个在搜索面板搜索之后，从搜索结果当中随机打开笔记。  
这个插件也不错，你可以把需要回顾的笔记打上标签，就可以针对这些笔记进行回顾了。  
同时还可以利用搜索语法，筛选出特定范围的笔记，对它们进行随机浏览。

### [](#spaced-repetition-plugin-3)第三方插件：Spaced Repetition Plugin

这是一个按照遗忘曲线间隔复习的插件，它有两种模式，一种是对笔记间隔复习，另一种是对笔记内标记为复习卡片的内容进行间隔复习。

给笔记打上 `#review` 的标签，插件就会把这个笔记加入复习序列中，点开笔记右上角的三个点菜单，可以点击 eazy、good、hard，之后会根据你选择的掌握程度，决定下一次什么时候再给你看。

给笔记打上 `#flashcards` 的标签，再参照下面的格式添加内容，`:::` 和 `？` 之后的内容将会作为卡片的背面，符号之前的内容会作为卡片的正面，复习卡片的时候会显示卡片的正面，让你想卡片背面的内容，也可以点击 eazy、good、hard 标记你对卡片内容掌握的程度。

```livecodeserver
the question goes on this side:::answer goes here!

```

```armasm
Front of multiline
?
Backside of multiline card

```

除了正反面的卡片，还支持挖空的卡片，给笔记打上 `#flashcards` 的标签后，该笔记中高亮的部分就会导入为挖空卡片。

这个插件很好用，可以直接把笔记库里面的笔记制作成复习的内容，推荐大家都尝试使用一下。  
具体的用法可以看官方文档： [Index - Obsidian Spaced Repetition 17](https://www.stephenmwangi.com/obsidian-spaced-repetition/)

### [](#dataview-4)Dataview 查询

还有一种随机回顾的方式就是通过插件 Dataview 查询笔记库内容，并随机呈现。

下面这段查询代码是从有指定标签的无序列表中，随机抽取呈现，具体是否完成随机，我还不太确定。

```applescript
```dataview
List L.text
FROM #书籍
FLATTEN file.lists AS L
FLATTEN date(now) as Now
FLATTEN (file.mtime.year + file.mtime.hour + file.mtime.day + 
	     file.mtime.hour + file.mtime.minute + file.mtime.second + 
	     file.size + Now.hour + Now.minute + Now.second) * 15485863 / (L.line + 1) 
	     as Hash
FLATTEN ((Hash * Hash * Hash) % 2038074743) / 2038074743 as Rand
SORT Rand
LIMIT 5

```

查询笔记再随机呈现应该也是可以的，大家可以探索一下。

以上就是目前我了解到的随机回顾的方法，希望给大家以启发。

我还是很喜欢随机和间隔复习这种功能。不管笔记库中有多少笔记，也不需要管这些笔记是否整理得井井有条。只需要点击一下按钮，就可以与做过得笔记不期而遇，重新激发思考。间隔复习则是把需要掌握得内容在时间维度上平铺，也不是一下就全部都要掌握，在复习的过程中，按照遗忘曲线安排好再次出现的时间，而这些都不用我们操心，我们需要做的就仅仅是点击按钮，点一下弹出卡片，根据卡片内容加深记忆、增添笔记，点击掌握程度后滑到下一张卡片。

如此，记录内容之后也不用把庞大的笔记库作为一个负担，因为我们知道，笔记内容会在某一个时刻再次与我们相见。

