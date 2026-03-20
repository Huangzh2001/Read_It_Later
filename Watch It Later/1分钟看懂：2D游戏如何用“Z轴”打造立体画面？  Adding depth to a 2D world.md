---
url: https://www.bilibili.com/video/BV1Lk2rBZEcT/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2026-03-20T16:01:25+08:00
---
![1分钟看懂：2D游戏如何用“Z轴”打造立体画面？ | Adding depth to a 2D world](https://www.bilibili.com/video/BV1Lk2rBZEcT/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
1分钟看懂：2D游戏如何用“Z轴”打造立体画面？ | Adding depth to a 2D world
https://www.bilibili.com/video/BV1Lk2rBZEcT/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
奶茶味的香草 2025-12-08 11:13:19

尽管2D视频游戏完全扁平，仍需考虑第三个维度，例如，如果我走到这棵树后面，玩家会被遮挡，但如果走到前面，玩家会遮住树干部分，如果这个逻辑被破坏，看起来会像这样，玩家始终被树遮挡，这种设置通过改变2D游戏中精灵的绘制顺序实现，每一帧都像一张空白画布供你绘制，你首先绘制背景，然后是玩家，接着是树木，但如果先画背景，再画树木，最后画玩家，玩家现在位于最顶层，这就是绘制顺序的重要性，游戏中每个精灵都需要按垂直位置顺序绘制，后方物体被前方物体遮挡，设置起来非常繁琐，但我的游戏中每个精灵都遵循这种方式，甚至单根草叶也是如此。



--- 由 vCaptions 生成 ---