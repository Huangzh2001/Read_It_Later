---
id: dfa48533-f242-4325-9042-71087703e1db

url: https://sspai.com/post/82279
---


tags::  #Readed 

# OB-ZO 联动：一键把 Zotero 摘录以特定格式粘贴到 Obsidian - 少数派
#Omnivore

[Read on Omnivore](https://omnivore.app/me/ob-zo-zotero-obsidian-18f6356be51)
[Read Original](https://sspai.com/post/82279)

OB-ZO 联动：一键把 Zotero 摘录以特定格式粘贴到 Obsidian

在我的生产力流程中，Obisidian 和 Zotero 都是不可缺少的一环。市面上关于二者联动的文章和视频非常多，但实际上仍然有空间不断优化，客制化为自己的流程。这里，我想介绍下如何一键把 Zotero 高亮摘录到 Obisidian 中，并且遵循我需要的 markdown 语法格式。

![](https://proxy-prod.omnivore-image-cache.app/0x0,s7ImcLS-arXxwxCtXuy5bMNBknP9hmDaPGG0jklFtw5g/https://cdn.sspai.com/2023/08/22/7d4145797f6a79236b0d9bd0b0f940d6.gif)

录屏看起来我输入了很多，其实只按了一个大写锁定加 C

需要准备的工具：

* Zotero
* Obisidian
* Keyboard Maestro

## 实现流程

### 首先更改 Zotero 的复制粘贴格式

进入 Zotero 设置，点击「高级——编辑器」，搜索 `annotations`，选择 `extensions.Zotero.annotations.noteTemplates.highlight`，即可修改。1

![](https://proxy-prod.omnivore-image-cache.app/0x0,sECqX7tERxRlcyJWrFLDiZK115eyF-59WT_Du4SWjwn8/https://cdn.sspai.com/2023/08/22/2f004bacccc2805f76d3d8b56f7466f0.png?imageView2/2/format/webp)

![](https://proxy-prod.omnivore-image-cache.app/0x0,sUu1TVBioOlSVwToueu9WG2nWoGbYvYgvSVJeDZiCZOY/https://cdn.sspai.com/2023/08/22/df8da5a13cf7d473943ec14915d29d1f.png?imageView2/2/format/webp)

修改摘录格式

修改代码也非常简单易懂，各种参数请参考官方文档，最直观的是更改之后自己看看效果，多试几次就明白了。

我的需求是实现评论作为 markdown 的四级标题，下面分行引用摘录的部分，代码如下。

```django
<p>##### {{comment}} </p>> {{highlight}} {{citation}} </p>
```

到这里，我们已经可以实现 Zotero 和 Obisidian 的引文联动了，只需要在 Zotero 里面点击高亮，用 ⌘C 复制，再到 Obisidian 里，用 ⇧⌘V 就可以以刚刚设置的格式粘贴了。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sT6In07weHQQEeojQ3roo1Rino3T9KWDu4-C2Yyd6CuM/https://cdn.sspai.com/2023/08/22/2106838d345e7377c06d8b2001392049.gif)

Zotero和Obisidian之间复制粘贴

Zotero 6 就加入了回链功能，在本地软件里粘贴，自带一个跳转回 Zotero 界面的链接，加上白板就能实现 MarginNote 的效果。更新 Zotero 7 之后，这一切更加顺滑。

遗憾的是，因为某种原因，Zotero 在每行前给生成的摘录加上了一个 "" 符号，让 Obisidian 不能渲染，需要查找替换，才能成功。于是我们用 Keyboard Maestro 弥补这个缺陷，并且让整个流程更加地自动化，实现一键复制粘贴。

### Keyboard Maestro 设置

网络上有不少 Keyboard Maestro 的流程介绍，我的流程也是在参考他人的基础上摸索出来的。2

以下是我的流程：

![](https://proxy-prod.omnivore-image-cache.app/0x0,sAQ_biAwJ-FA0haO_MDqB_fqTkcWV0wVDSbRShV1D38U/https://cdn.sspai.com/2023/08/22/d44468e7a23922b53e21b2b73e0bbdf4.png?imageView2/2/format/webp)

Keyboard Maestro 设置截图

使用自己设置的快捷键触发指令，指令按次序为：

1. Type the ⌘C Keystroke：复制
2. Activate Obisidian：打开 Obisidian
3. Type the ⇧⌘V Keystroke：按处理过的格式粘贴在 Obisidian 中
4. Type the ⌥⌘F Keystroke：这是 Obisidian 的查找替换快捷键
5. Set Keyboard Layout to “ABC”：把输入法改成系统自带 ABC，这一步是为了避免中英文符号混乱
6. Type the Keystroke\\：实际上是在查找 Zotero 多出来的符号\\
7. Type the Tab Keystroke：进入替换的输入框，因为只需要把符号删掉，所以不用输入
8. Type the ⌥⌘Return Keystroke：这是 Obisidian 自带的全部替换快捷键
9. Type the Escape Keystroke：退出查找替换
10. Type the ⌘Down Arrow Keystroke：把光标固定在文档最下方
11. Set Keyboard Layout to “鼠须管”：设置回我自己常用的输入法
12. Notification “处理成功”：通知：处理成功
13. Activate Zotero：回到 Zotero

## 尾声

不管是 Obisidian、Zotero 还是 Keyboard Maestro ，都有非常高的自由度，各自都能实现丰富的功能，最后能做到什么程度，只看想象力是丰富还是贫乏，爱折腾的人有福了。

\> 下载少数派 [客户端](https://sspai.com/page/client)、关注 [少数派公众号](http://sspai.com/s/KEPQ) ，让你的工作更有效率 ⏱

\> 特惠、好用的硬件产品，尽在 [少数派 sspai 官方店铺](https://shop549593764.taobao.com/?spm=a230r.7195193.1997079397.2.2ddc7e0bPqKQHc) 🛒

* 1Zotero 官方文档见 https://www.Zotero.org/support/note\_templates，视频讲解见 https://www.bilibili.com/video/BV1bF411W7ma/?vd\_source=62d26317551d657a5b49bd466a26aeb9
* 2https://www.bilibili.com/video/BV1Sz4y1U7NT/?vd\_source=62d26317551d657a5b49bd466a26aeb9

[![](https://proxy-prod.omnivore-image-cache.app/0x0,sYafv6i3BXj_CVI8z8HC6jzQ2dVDx3HNevY5n-3X0P_I/https://cdn.sspai.com/2023/2/7/article/c8656602-8fa9-e7d4-2c78-767c454bfce8.jpg?imageMogr2/auto-orient/thumbnail/!1096x252r/gravity/center/crop/1096x252/format/webp/ignore-error/1)](https://sspai.com/a/XJRq3n)

