---
id: d5cf42eb-e8cb-4f31-8a9f-8ab861c9d3d3
---


tags::  #Readed 

# Adding caption to images - Feature requests - Obsidian Forum
#Omnivore

[Read on Omnivore](https://omnivore.app/me/adding-caption-to-images-feature-requests-obsidian-forum-190e4da87a5)
[Read Original](https://forum.obsidian.md/t/adding-caption-to-images/16431/28)

Yessss! I never got “Obsidian Caption” plugin to work, but this “Obsidian Captions” finally does it for me, thank you

How would I center the caption if the images were centered?

They’re centered by default. You can make any changes you want via CSS.

It seems that both the image and caption are left-aligned by default. We can use the CSS like this to center the image.

```css
  /*center image*/
  img { 
    display: block !important; 
    margin-left: auto !important; 
    margin-right: auto !important; 
    } 
    

```

But I don’t know how to center the caption. I tried this, but it doesn’t work.

```css
  .image-captions-caption {
    text-align: center;
  }

```

You’ll want to use this to center the image:’

```css
.image-captions-figure { 
  margin-left: auto; 
  margin-right: auto; 
} 

```

It sounds like you have some other CSS affecting this. You can test this in the Sandbox vault and see that the captions are centered:

[![[Omnivore/Adding caption to images - Feature requests - Obsidian Forum/attachments/582684207e7b2c1a969a9fed2ea3abbc_MD5.jpg]]](https://forum.obsidian.md/uploads/default/original/3X/e/a/eae31887cf40273cff981a77fa4b47a4aed4510c.jpeg "image")

You just need to do some investigation to find out what other CSS is preventing the text from being centreed.

很抱歉造成混乱。我有两个黑曜石字幕插件。我拒绝了另一个。现在工作正常。

## [](#possible-solution-editor-mode-preview-mode-1)可能的解决方案，编辑器模式+预览模式

版本： 1.2.8 （Installer 1.1.16）  
 构建方式：

* 使用以下代码创建一个.css文件（我使用Mac的Textedit，不要留下.txt扩展名）
* 把它放在 snippet 文件夹中：`your vault/.vault/snippet`
* 使用命令打开文件夹。`.vault` `CMD OPT .`
* 请注意，我添加了标题居中，因为我使用了另一个片段来居中我的图像。如果您不想将图像居中，只需擦除这部分代码（用于阅读模式和源视图）。`text-align: center;`
* 不要忘记在黑曜石设置中激活这个新片段
* 不要犹豫，尝试不同的设置！

```css
/* reading mode */
.image-embed[alt]:after {
    content: attr(alt);
    display: block;
    margin: 0.2rem 1rem 1rem 1rem;
    font-size: 90%;
    line-height: 1.4;
    color: var(--text-faint);
    text-align: center;

}
/* source view and live preview */
.image-embed[alt]:after {
    content: attr(alt);
    display: block;
    margin: 0.2rem 1rem 1rem 1rem;
    font-size: 90%;
    line-height: 1.4;
    color: var(--text-faint);
    text-align: center;
}

```

如果您对此感兴趣，另一个片段可以居中我的所有图像：

```css
/* reading mode */
img {
        display: block !important;
        margin-left: auto !important;
        margin-right: auto !important;
}
    
 .markdown-source-view.mod-cm6 .cm-content > * {
        margin: auto auto !important;
}
/* source view and live preview */
img {
        display: block !important;
        margin-left: auto !important;
        margin-right: auto !important;
}
    
 .markdown-source-view.mod-cm6 .cm-content > * {
        margin: auto auto !important;
}

```

这很酷，可以消除对插件的需求。

你有没有运气让外部图像工作？

这种风格：

```markdown
![[Omnivore/Adding caption to images - Feature requests - Obsidian Forum/attachments/9861e11a693fb67d9b9815cd93563fe7_MD5.png]]

```

旧话题。但我的个人解决方案是使用标注来表示数字。必须对标准标注或自定义标注进行疤痕化。在我使用提示之后：

```lua
> [!tip] ![[my_figure.png]]
> *This is the caption* 

```

通过一些 css 杠杆，您可以自定义特定于提示（在本例中）标注的图标和标题。

我希望黑曜石可以原生支持一些 \[！figure\] \[！table\] \[！math\] 标注。

使用此技巧，您还可以制作一个带有标题的可折叠的更大人物：

```lua
> [!tip]- ![[my_figure.png|100]]
> ![[my_figure.png]]
> *This is the caption* 

```

## [](#this-would-be-a-snippet-like-this-one-1)这将是一个像这样的片段：

```scss
.callout[data-callout="figure"] {
  --callout-color: 100, 100, 100;
  --callout-icon: none;
  .callout-content {
      font-size: 0.5em; 
      text-align: center;
   }
 }

```

## [](#the-markdown-2)markdown ：

```livecodeserver
Normal text 

> [!figure] ![[two_noises.png]]
> Two signal measurement one has a SNR of 10 the other of 100. The signal average is however the same. 

Some normal text continue here 

```

## [](#how-it-looks-like-3)它看起来像：

[![[Omnivore/Adding caption to images - Feature requests - Obsidian Forum/attachments/047b2ce0cab483639ca37201bec2d62b_MD5.png]]](https://forum.obsidian.md/uploads/default/original/3X/c/b/cb91f890e288f694111d7983261631c53634c1c4.png "image")

我喜欢这个解决方案，因为它保持人类可读性，它不需要特殊的插件，而且我可以轻松地让它在我的 markdown 发布者 （quartz） 上运行。

[@slyg](https://forum.obsidian.md/u/slyg)我想对此提出一个反驳意见。

Markdown 已经有了图像描述的位置 （[规格在这里 83](https://spec.commonmark.org/0.30/#images)):

```markdown
![Image description](path/to/image.jpg)

```

或

```lua
![[path/to/image.jpg|Image description]]

```

这是上面字幕插件中文本的来源。

依赖黑曜石风格的标注与任何类型的标准 Markdown 都相去甚远。它可能在另一个 Markdown 渲染器上受支持，但可能不会。

使用符合规格的图像描述更有可能在未来得到另一个平台的支持，即使没有它，其他软件也更容易解析并完美地呈现为 HTML。

编辑：我要补充一点，以标注方式进行操作并没有错 - 这只是一个值得深思的食物，因为您考虑到您的保险库的寿命，以及如果黑曜石不再存在，它在其他平台上的交叉兼容性。

答案是肯定的。这只是关于这些主题的额外解决方案。

该解决方案非常适合长描述，其中可能包括粗体文本，LaTeX，交叉引用等...

在 Obsidian 和任何具有 Obsidian 标注味道的 Markdown 渲染中效果很好。

实际上，对于不处理标注（如 pandoc）的 Markdown 渲染，信息仍然存在。只在某处添加了一个奇怪的 \[！figure\]，但 figure 和 caption 在那里。

优点 - 我非常喜欢这种方法，尤其是能够在描述中添加其他 markdown。

我刚刚意识到这种方法的另一个用例。是否可以为两张图片添加一个标题。

```lua
> [!figure] ![[fig1.png|300]] ![[fig2.png|300]] 
> The two figures shows .... **when**  $\alpha  = \int_0^\infty f(t) dt$ 

```

使用 [@slyg](https://forum.obsidian.md/u/slyg) 的 Callout 选项，另一种在没有 CSS 的情况下将标题居中的方法是使用 html 标签。

```lua
> [!tip] ![[Black-Eyed Susans.png|256]]
> <center>Black-eyed Susans</center>

```

是不是说 3 年后，仍然没有好而简单的方法来在 Oblidian Publish 上呈现我的替代文本图像标题？

对于任何类型的“严肃写作工具”来说，这似乎是一个如此明显的特征

我通过使用一个简单的 markdown 表来实现这一点。

```gherkin
| ![](/path/to/image.ext)  |
| ------------------------ |
| <center>Caption</center> |

```

我使用以下代码在 Publish 中应用图像标题：`publish.css`

```css
img[alt] {
  margin : 0 auto;
  display: block;
}

span[alt]::after {
  content: attr(alt);
  display: block;
  text-align: center;
  margin-top: 8px;
  font-size: inherit;
  color: inherit;
}

```

