---
url: "https://www.bilibili.com/video/BV1v7YL6QEwJ/?vd_source=06168f390bae49c4867767c52a20e87c"
tags:
  - "video"
status: "readed"
date: "2026-09-12T19:31:28+08:00"
---
![用普通机械键盘反映AI的运行状态](https://www.bilibili.com/video/BV1v7YL6QEwJ/?vd_source=06168f390bae49c4867767c52a20e87c)
用普通机械键盘反映AI的运行状态
https://www.bilibili.com/video/BV1v7YL6QEwJ/?vd_source=06168f390bae49c4867767c52a20e87c
打包不要带走 2026-09-11 15:46:43

Note65，AI agent状态运行AI后，键盘自动进入思考状态，彩虹外圈慢速旋转，反应思考过程，初设计支持七种状态，可以监控AI在干什么，可以知道AI是否在等待交互，防止AI后台摸鱼，AI每次调用工具成功会有一个白色转圈效果，本项目的host端代码开源，提供完整的通信协议文档和接入实例，代码实现原理如图给AI agent工具注册hook事件，hook把事件转发到demon进程，demon进程把事件通过heap写到键盘，这样就实现了由键盘，实时反映agent工作状态的效果，键盘把动画都做好了，主要的工作在于适配不同的AI agent id，1clean，未来也会考虑实现codex micro的特殊按键支持，比如允许禁止查看等按键操作，现在来使用仓库的代码演示动画，运行代码模式是金king状态，等待permission时，外圈呼吸提示，贝利亚报错时显示红色闪烁，好，complete的状态会退出到键盘原始状态，VC流效果同金king，notification是等待用户选择时的外圈闪烁效果，金king是外圈彩虹慢跑动思考，running是外圈彩虹快速跑动，网友可以自行接入你的AI或者重定义，不同状态对应的灯效代码不会改，就让AI改，最后运行结束了，键盘自动恢复原来的动画状态。



--- 由 vCaptions 生成 ---