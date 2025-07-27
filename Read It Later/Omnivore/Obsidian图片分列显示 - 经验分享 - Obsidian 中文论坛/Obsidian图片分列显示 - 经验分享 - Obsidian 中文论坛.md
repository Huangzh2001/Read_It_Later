---
id: 59fab06e-31a2-44e6-a2a8-76daa8db4e68

url: https://forum-zh.obsidian.md/t/topic/3963
---


tags:: 

# Obsidian图片分列显示 - 经验分享 - Obsidian 中文论坛
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-obsidian-190e397216f)
[Read Original](https://forum-zh.obsidian.md/t/topic/3963)

Obsidian 常规的图片都是一张图片显示一行，可以通过自定义 CSS 代码片段的方式实现美化。效果如下：

[![[Omnivore/Obsidian图片分列显示 - 经验分享 - Obsidian 中文论坛/attachments/1df1276c25a44909cb7346f04ffd84e4_MD5.jpg]]](https://forum-zh.obsidian.md/uploads/default/original/2X/3/37c220528ee914ac1ae69a0ade7e5fafef4c9a74.jpeg "obsidian_img_2columns")

[![[Omnivore/Obsidian图片分列显示 - 经验分享 - Obsidian 中文论坛/attachments/9e19a325d5eb55fe81d156d2911d7c66_MD5.jpg]]](https://forum-zh.obsidian.md/uploads/default/original/2X/6/6a55620b86d63ffa5ae74bad6e34535216501793.jpeg "obsidian_img_3columns")

[![[Omnivore/Obsidian图片分列显示 - 经验分享 - Obsidian 中文论坛/attachments/9ec8a6d102c7414b85b3e38fc10006a4_MD5.jpg]]](https://forum-zh.obsidian.md/uploads/default/original/2X/4/4a3d0b22bef17ab15639cdcd68c5c37a5fb18831.jpeg "obsidian_img_4columns")

实现方式如下：

1、增加代码片段

```css
/* For Obsidian 0.9.22 and up */

.img-grid .markdown-preview-section img:not([width]),
.img-grid .markdown-preview-section video {
   width:100%;
}
.img-grid .markdown-preview-section > div {
   display:flex;
}
.img-grid .markdown-preview-section > div > .internal-embed {
   flex:1;
   margin-left:-0.5rem;
   padding:0 0.5rem 0.5rem 0.5rem;
}
.img-grid .markdown-preview-section > div > *:not(div) {
   margin-block-start: 0rem;
   margin-block-end: 1rem;
}
.img-grid .markdown-preview-section > div hr {
   width:100%;
}
/* These lines make every image the same height */
.img-grid .markdown-preview-section > div > .internal-embed img:not(:active) {
   object-fit:cover;
   height:100%;
}

```

2、在文档头部 front-matter 区写上 `cssclass: img-grid`

3、用换行控制图片是否在同一行，图片间没有换行的话，图片默认在同一行。

以上的方案来自官方论坛，参考链接附上： [Display side by side image grid 200](https://forum.obsidian.md/t/display-side-by-side-image-grid/9359)

* [最后回复](https://forum-zh.obsidian.md/t/topic/3963/6)  
[](https://forum-zh.obsidian.md/t/topic/3963/6)23 年 10 月
* 4.2k  
#### 浏览量
* 5  
#### 用户
* 8  
#### 赞
* 3  
#### 链接

在Blue Topaz主题中使用后，图片无法自动居中了，尝试使用其他CSS片段对图片进行居中，但是好像和img-grid冲突，请问有什么好的解决办法吗？

###  想阅读更多？请浏览[经验分享](https://forum-zh.obsidian.md/c/8-category/8)中的其他话题或[查看最新话题](https://forum-zh.obsidian.md/latest)。

