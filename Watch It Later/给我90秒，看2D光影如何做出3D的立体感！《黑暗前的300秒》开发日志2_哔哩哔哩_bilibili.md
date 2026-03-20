---
url: https://www.bilibili.com/video/BV1pfNTz9EWN/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2026-03-20T16:00:59+08:00
---
![给我90秒，看2D光影如何做出3D的立体感！《黑暗前的300秒》开发日志2_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1pfNTz9EWN/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
给我90秒，看2D光影如何做出3D的立体感！《黑暗前的300秒》开发日志2
https://www.bilibili.com/video/BV1pfNTz9EWN/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
小苏做游戏 2026-03-08 09:01:44

哈喽我是小苏，这期视频带大家看看，如何把2D光影从这样变成这样，首先3D游戏为何能呈现逼真的阴影，是因为在三维空间下，可以模拟现实世界的光线传播方式，然而在2D平面中，阴影与光照难以区分，那么问题来了，2D环境下真的无法实现动态阴影吗，我们首先设计图，然后是基本照明，我们会发现这个方法虽然又快又方便，但是缺少了很多的真实性，那加入unity自己的光影总行了吧，可是unity自己都搞不明白，已有的方法都试过了，现在怎么办，那只能自己造咯，首先二维空间中没有亮面，暗面之分，不过这里可以用到normal map，通过一些特定的颜色值，我们可以告诉系统，每个像素在3D的方位，系统就可以根据2D光源模拟出3D的效果，再说阴影，先用一点点的数学模拟光线投射，再换个颜色，然后再根据光源的远近调整透明度，近处阴影变深，反之变浅，最后为了让阴影看着不那么僵硬，再将边缘淡化，放入游戏，一个极为真实并且不被引擎所束缚的光影效果，就有了。



--- 由 vCaptions 生成 ---