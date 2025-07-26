---
id: be71d74a-a82b-4cdc-85ff-9fc4f997125f
---


tags::  #Readed 

# Obsidian 中图片加说明文字 image caption - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-image-caption-190e4db2dff)
[Read Original](https://zhuanlan.zhihu.com/p/662633596)

## 效果

![](https://proxy-prod.omnivore-image-cache.app/653x527,sebTFqaBiPNi4sMqQp4J8eWSDWywQsNYnlNWLXL-pJ20/https://pic1.zhimg.com/v2-f9f6bdaf7b615a17cee40202aace6f04_b.jpg)

Obsidian 中带说明文字的图片。上方为图片，下方为说明文字（caption）。

说明文字是图片的替代文本（alt text)，即

```markdown
![This is the caption](image.png)
```

或者

```lua
![[image.png|This is the caption]]
```

## 方法

* 新建一个 .txt 文件，并插入下面的代码；
* 修改文件后缀名 txt 为 css；
* 将 css 文件放到路径 `your vault/.vault/snippet` ，也可以在 `设置-外观-CSS snippets` 中打开；
* 在 `设置-外观-CSS snippets` 激活这个 `css` 脚本

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

## 参考

[https://forum.obsidian.md/t/adding-caption-to-images/16431/22#possible-solution-editor-mode-preview-mode-1](https://link.zhihu.com/?target=https%3A//forum.obsidian.md/t/adding-caption-to-images/16431/22%23possible-solution-editor-mode-preview-mode-1)

