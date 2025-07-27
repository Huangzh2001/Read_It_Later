---
id: c857a69d-d0f1-4580-a424-7530db3748db

url: https://sspai.com/post/63100
---


tags:: 

# 10 种联动+10 个场景，我的 Tasker 自动化实例分享 - 少数派
#Omnivore

[Read on Omnivore](https://omnivore.app/me/https-sspai-com-post-63100-1904b262787)
[Read Original](https://sspai.com/post/63100)

10 种联动+10 个场景，我的 Tasker 自动化实例分享

### Matrix 首页推荐

[Matrix](https://sspai.com/matrix) 是少数派的写作社区，我们主张分享真实的产品体验，有实用价值的经验与思考。我们会不定期挑选 Matrix 最优质的文章，展示来自用户的最真实的体验和观点。

文章代表作者个人观点，少数派仅对标题和排版略作修改。

---

几个月前看到了 [从通知实现钱迹 Tasker 自动化记账](https://sspai.com/post/61292)，想起来了之前购买即遗忘于角落的 Tasker……心有戚戚焉。加之自动化记账这件事确实 get 到我了，于是籍此开始折腾 Tasker 的自动化之路。

经过几周的折腾，混迹于各论坛，参考各种文章后魔改，目前实现的部分功能如下：

* 通话后自动同步录音到坚果云、fooview 截图后自动同步到电脑桌面
* 地图应用开启关闭与 GPS 同步
* 视频应用开启关闭与自动锁定同步
* 息屏下连接特定耳机自动播放微信通知
* 除特定应用连接耳机后自动播放听力
* 钱迹自动化记账（带备注、可选账本、延后记账、免密支付自动记账）
* 点击手环、摇动手机、Quicker 实现管理智能家居
* 手机充电至 95% ，手环提醒
* Keep 开始运动后，小米手环自动开始记录
* 控制另一部手机实现通知转发、播放控制等功能
* 利用小爱同学执行 Tasker 任务
* 扫描特定 NFC 卡片，打开体重秤连接界面
* ……

下面会介绍这些自动化的使用场景和配置思路，部分复杂的配置会提供导入，希望对你有所帮助。

## 1、Tasker + FolderSync

[FolderSync - Google Play 上的应用](https://sspai.com/link?target=https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Ddk.tacit.android.foldersync.lite%26hl%3Dzh)

## 1.1 通话录音自动同步到云盘

### 功能描述

以防不时之需，我希望我的录音至少可以同步到云盘，最好后面还可以 **同步到其他设备** 或 **分享给家人** 。小米自带的云服务其实是可以将通话录音同步到小米云服务里面的，但是小米云服务毕竟不是专业做网盘的，多设备同步和分享控制相对不如 Dropbox/坚果云这类网盘专业。

所以我需要找到一个桥梁，将手机本地的录音文件夹和云盘建立链接，实现双向同步。

FolderSync 就是这样一款用于云盘、本地间同步的应用，支持 Google Drive、Dropbox、OneDrive、MEGA 等常见网盘，也支持通过 FTP、SMB、WebDAV 等协议连接到其他存储空间。

最后我选择利用 FolderSync 通过 WebDAV 协议将本地文件夹和坚果云文件夹链接在一起，因为坚果云的通话录音文件夹可以同步到多个设备上，并且它的分享权限控制也相对完善。

这样通话结束后，录音会自动同步到坚果云上，然后坚果云也会将文件同步到电脑上。

### 配置思路

在 FolderSync 中配置好某个同步项目后，在 Tasker 中进行以下设置。

```gauss
if (监测到通话结束):

调用 Tasker 中 FolderSync 插件同步特定项目
Endif
```

### 依赖配置

* 无需 Root、adb
* 下载 FolderSync 需连接至 Google Play
* 若网盘为 Google Drive、Dropbox 等国外产品，则需要处理网络问题

## 1.2 FV 悬浮球截图后自动同步到电脑桌面

[FV 悬浮球-fooView(com.fooview.android.fooview) - 1.4.4.1 - 应用 - 酷安网](https://sspai.com/link?target=https%3A%2F%2Fwww.coolapk.com%2Fapk%2Fcom.fooview.android.fooview)

[FV 悬浮球 - fooView，文件浏览，手势截图 - Google Play 上的应用](https://sspai.com/link?target=https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Dcom.fooview.android.fooview%26hl%3Dzh)

### 功能描述

写这些手机上的教程免不了做截图演示，「截图-分享到电脑-电脑保存」这个流程上还是有些繁琐。我希望能够尽量简化截图上传至电脑的流程。

所以我将手机截图保存的文件夹和电脑上的目标文件夹通过坚果云和 FolderSync 建立了双向同步，一旦监测到有新截图生成，FolderSync 同步本地文件夹到坚果云，坚果云再同步该文件夹到电脑。最终流程就可以被简化到「截图-电脑自动出现结果」。

那怎么监测什么时候有新截图产生呢？

这就要用到 Tasker 的 Logcat Entry 功能，关于它的具体说明可以查看 [Logcat Entry 官方文档 ](https://sspai.com/link?target=https%3A%2F%2Ftasker.joaoapps.com%2Fuserguide%2Fen%2Fhelp%2Feh%5Flogcat%5Fentry.html)。简单讲就是应用完成不同的操作时会留下不同的痕迹，Tasker 可以监测这些痕迹来反推应用完成了什么操作。

至此，只要在 FolderSync 里面配置好一个新的同步项目，这个动作就算是完成了。

### 配置思路

```awk
if (通过 Logcat Entry 监测到 fooview 保存了截图):
调用 Tasker 中 FolerSync 插件同步特定项目
Endif

# 我的 Logcat Entry 设置-Mi10-MIUI12，仅供参考。此部分配置会因为设备、默认保存文件夹不同而不同
Component：MiuiGallery2_SaveToCloudUtil
Filter：[thread-pool-0] insert /storage/emulated/0/Pictures/Screenshots/
```

### 依赖配置

* 无需 Root，但 [Logcat Entry](https://sspai.com/link?target=https%3A%2F%2Fwww.reddit.com%2Fr%2Ftasker%2Fcomments%2Fdsf5gj%2Fdev%5Ftasker%5F59beta8%5Fthe%5Fgame%5Fchanger%2F) 功能需要 adb 授权（当你添加这个功能的时候，Tasker 会告诉你怎么做）；
* 下载 FolderSync 需连接到 Google Play；
* 网盘推荐使用坚果云，不过 Windows 使用 OneDrive 也能有相同的效果；如果不使用网盘，局域网下也可直接通过 FTP、SMB 协议同步到电脑。

## 2、Tasker + Notify&Fitness for Mi Band

## 2.1 充电至 95% 手环发送电量充满提醒

[Notify & Fitness for Mi Band - Google Play 上的应用](https://sspai.com/link?target=https%3A%2F%2Fplay.google.com%2Fstore%2Fapps%2Fdetails%3Fid%3Dcom.mc.miband1%26hl%3Dzh)

NF for Mi Band 是小米手环的一款第三方客户端，相较于官方的小米运动，NF 会更干净、可玩性更高。关于 NF 的具体介绍，可以查看 [告别广告，让小米手环在 Android 上更好用：Notify & Fitness ](https://sspai.com/post/56954)。

## 功能描述

为了手机电池的长久健康，我平时会尽量避免将电池充满。

当手机充电电量达到 95% 时，一种思路是通过控制智能插座实现断电，不过问题在于不知道通过什么触发给插座发指令恢复供电，不然可能插上去半天才发现插座忘记打开了。

另外一种思路就是此时给手环发通知，手动拔掉充电器 🤔

最初是通过 Tasker 来配置的，但后来发现 NF 也自带了电量充满提醒。Anyway，这个动作的意义在于你现在可以通过 Tasker 将手机和手环连接起来了，手环的玩法也籍此变得更为丰富。

## 配置思路

```gauss
if (电池电量 =95) And (在充电)：
手环发送通知
Endif
```

## 依赖配置

* 无需 Root、adb
* 需要安装第三方小米手环应用 Notify&Fitness for MiBand，如果从 Google Play 下载需要网络条件和 Google 套件，利用 [Notify & Fitness for Mi Band APKs - APKMirror](https://sspai.com/link?target=https%3A%2F%2Fwww.apkmirror.com%2Fapk%2Fonezerobit%2Fnotify-fitness-for-mi-band%2F) 或可避开 Google 套件

## 3、Tasker+ 钱迹

### 功能描述

这个自动化主要是受 [从通知实现钱迹 Tasker 自动化记账](https://sspai.com/post/61292) 这篇文章影响，之前尝试了很多方式，但还是经常忘记记账。而通过 Tasker 和钱迹的联动，则可以付款后立即快速记账，并且支持这些功能：

* 有通知（有金额）可以从通知捕获金额
* 支持添加备注
* 支持选择账户
* 支持延迟记账（会在通知栏中创建一条不会被误清除的通知）
* 支付宝免密支付项目可以自动记账

具体可以参照这条演示视频：

美中不足的一点是还没找到 **怎么用 Tasker 直接唤起输入法的数字输入模式** ，在输入小数点的时候多一步感觉不太方便。如果有知道的朋友，还望在评论区指出，感谢。

### 配置思路

```perl
# 两个 Profiles、两个 Scenes、16 个 Tasks

#变量说明
%ACCOUNTNAME #记录存入账户
%Accountname1 #银行卡账户 1
%Accountname2 #银行卡账户 2
%Accountname_hb #花呗在钱迹中的名称，默认「花呗」
%Accountname_wechat #微信余额在钱迹中的名称，默认「微信」
%Accountname_yeb #余额宝在钱迹中的名称

%Choice #记录是支付宝系 (余额宝、花呗、银行卡们) 还是微信系 (微信钱包、银行卡们)，1 支付宝 2 微信
%Evtprm #因为 %evtprm() 是局部变量，存储通知文本在不同 task 之间传递
%If_have_unrecord_bills #记录是否有需要延后记录的账单 (0 无 1 有)
%Notification_to_cancel #记录要清除的延后通知文本
%QJURL #钱迹记账的 Link
%Tag #记录是否选择了账本，未选择账本则取消记账 
```

![](https://proxy-prod.omnivore-image-cache.app/0x0,swd-6xHApjDenbV5BT8LpRMXWUsQQEcIEAvQQyPtAorA/https://cdnfile.sspai.com/2020/10/19/8f20cde2a86a72ef27eab3bc6dce3e71.png?imageView2/2/format/webp)

### 依赖配置

* 无需 Root、无需 adb
* 需安装 [钱迹](https://sspai.com/link?target=https%3A%2F%2Fqianjiapp.com%2F)

### 参考信息

[从通知实现钱迹 Tasker 自动化记账 - 少数派](https://sspai.com/post/61292)

[自动化记账接口 · 钱迹用户指南](https://sspai.com/link?target=http%3A%2F%2Fdocs.qianjiapp.com%2Fplugin%2Fauto%5Ftasker.html)

### 导入说明

1. 长按左下角小房子图标，导入项目
2. 在「支付记账」项目中切换到「任务」界面，点击进入「初始化命令」
3. 根据自己钱迹账本中账户的名称修改对应的账户名称
4. 点击左下角，运行此任务
5. (可选) 到 [Iconfont-阿里巴巴矢量图标库 ](https://sspai.com/link?target=https%3A%2F%2Fwww.iconfont.cn%2F)搜索对应账户的图标，在「场景」中修改对应账户的图标和背景
6. 支付宝免密支付的通知需要自行修改记账账户、通知文本清理、消费类别等设置

PS：华为手机需 EMUI 10 或 Magic UI 3.0 以上才能使用钱迹的自动化记账接口，目前还不清楚低版本系统有无解决方案。

## 4、Tasker + [HomeAssistant](https://sspai.com/link?target=https%3A%2F%2Fwww.home-assistant.io%2F)

尽管米家 App 其实通过一直在努力通过快捷方式、Widget、锁屏划入、通知栏控制等方式简化智能设备的操作流程，但一来我是真的懒，这些方式我还得动脑找设备；二来，米家 App 也没办法利用手机更多样的传感器玩联动，差了点意思。但这些设备接入 HA 后，那真就是人有多大胆，地就有多大产了。

另外，尽管小爱同学控制家电也就一句话的事，但如果有其他人在场，我总觉得喊小爱同学好羞耻……

基于这两个原因，我选择将智能家居接入 HA，多一个控制渠道，多一些场景玩法。

## 4.0 安装 HomeAssistant 与接入米家设备

### 安装 Home Assistant

> Home Assistant 是一个免费的开源家庭自动化软件，用 Python 编写，重点关注本地控制和隐私。它有非常广泛的设备支持，截至 2020 年 5 月，它支持超过 1600 个模块化插件或附加组件与不同的物联网技术的系统集成，系统和服务作为「集成组件」可用。通过自动，语音命令，移动应用或 Home Assistant 基于 Web 的前端用户界面上的控件来触发诸如打开 / 关闭灯之类的操作。
> 
> [Home Assistant - Wikipedia](https://sspai.com/link?target=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FHome%5FAssistant)

Home Assistant 作为智能家居的中控中心需要 24 小时运行，所以通常会被安装在功耗比较小的 [树莓派 ](https://sspai.com/link?target=https%3A%2F%2Fwww.zhihu.com%2Fquestion%2F20859055)上

但我手里面并没有树莓派，所以我先后尝试过安装在 Windows 和 Android 手机上，都能使用。如果没有树莓派、Nas 等设施的话，推荐安装在老旧 Android 手机上。

#### Windows 安装 HA

教程：[homeassistant 安装与启动 - HAChina 中文网](https://sspai.com/link?target=https%3A%2F%2Fwww.hachina.io%2Fdocs%2F330.html)

几个避坑的点如下：

* 截止至 2020.8.12，HA 需要 Python 版本大于等于 3.7
* 因为有些 pip3 工具下载的库是源码形式的，在 pip3 工具执行安装的过程中会需要调用本机的 C++ 编译器，所以需要安装 [MicrosoftVisual C++Build Tools](https://sspai.com/link?target=https%3A%2F%2Fblog.csdn.net%2Fbbhdeal%2Farticle%2Fdetails%2F81144783)
* 如果遇到了 `Stuck at INFO:homeassistant.core:Timer:starting` ，可以通过 `pip install home-assistant-fronted` 解决
* 如果想设置 Home Assistant 开机自启动，可以 [制作 ](https://sspai.com/link?target=https%3A%2F%2Fjingyan.baidu.com%2Farticle%2F0bc808fc2e37871bd485b9f7.html)`.bat` 脚本后 [添加到自启动 ](https://sspai.com/link?target=https%3A%2F%2Fblog.csdn.net%2Fyanchenyu365%2Farticle%2Fdetails%2F88732646)，以下代码可供参考 (无黑窗口常驻)

```dos
@echo off
if "%1" == "h" goto begin
mshta vbscript:createobject("wscript.shell").run("""%~nx0"" h",0)(window.close)&&exit
:begin
REM

hass
```

#### Android 安装 HA

先后在 红米 Note 4x (已 Root，MIUI11-9.10.10，Android 7) 和华为 Nova 2s(未 Root，EMUI8.0，Android 8) 成功安装了 HA，不过两者安装时遇到的问题并不相同，命令仅供参考。

以下操作需要设备安装 Termux 后完成，Termux 是 Android 上的一个终端模拟器，开源并且无需 Root。关于它的具体教程，可以参考 [Termux 高级终端安装使用配置教程 | 国光 ](https://sspai.com/link?target=https%3A%2F%2Fwww.sqlsec.com%2F2018%2F05%2Ftermux.html)。

这里也假定你有一定的命令行基础并且擅于搜索，其实核心思想基本可以总结为四个字： **缺啥装啥** 。

Root 的设备可以直接进入文件夹编辑文件；未 Root 的设备则需使用 Vim 这种编辑器来编辑相关配置，此处请自行搜索 Vim 的相关用法。

参考的教程：

[在 Andorid 使用 Termux 安装 HomeAssistant 以作为家庭的 HomeKit 中枢](https://sspai.com/link?target=https%3A%2F%2Fgist.github.com%2FCaldis%2F7646df406de43e6c6581ff491dfd8afe)

[闲置 Android 手机变身 Homeassistant 家庭助理 HAChina 中文网](https://sspai.com/link?target=https%3A%2F%2Fwww.hachina.io%2F7656.html)

[Androidr 手机或盒子通过 Termux 安装 Home assistant+homekit+MQTT+Node-red - 「HomeAssistant」](https://sspai.com/link?target=https%3A%2F%2Fbbs.hassbian.com%2Fthread-7167-1-1.html)

踩坑信息：

1. 根据 [No more -dev packages - Termux Wiki](https://sspai.com/link?target=https%3A%2F%2Fwiki.termux.com%2Fwiki%2FNo%5Fmore%5F-dev%5Fpackages) 所言，Termux 从 2019.7.28 起停止支持 xx-dev 的包，所以以上教程中的 python-dev、openssl-dev 等包都不必安装了。
2. 可能需要补充的安装包的命令有 `pip install Pillow`、`pip install aiohttp_cors`、`pip install home-assistant-fronted`

### 接入米家设备

> 以小米智能插座 WIFI 版为例

* 最好有已 Root 的 Android 设备
* 米家 app 5.0.19 前版本
* 最好安装 Google Play

[获取小米 WIFI 设备 token 方法](https://sspai.com/link?target=https%3A%2F%2Fhome-assistant.cc%2Fcomponent%2Fxiaomi%2Fwifi%2F%23token-%25E8%258E%25B7%25E5%258F%2596)

注意 `yaml` 配置文件所有的 `:` 后面都应该跟一个 **空格** 。

```routeros
switch:
- platform: xiaomi_miio
name: Original Xiaomi Mi Smart WiFi Socket #给你的插座起个名字
host: # 插座的 ip 地址
token: # 你获取的 token
model: chuangmi.plug.m3
```

[为 hass 添加小米的智能插座基础版](https://sspai.com/link?target=https%3A%2F%2Fgist.github.com%2Fwillwhui%2Fd499629ca6c46aaf29ba2a06c2ad209d)

[ha 接入小米 wifi 插座 , 附 miio 安装](https://sspai.com/link?target=https%3A%2F%2Fbbs.hassbian.com%2Fthread-1238-1-1.html)

可能会漏掉的命令：

`pip3 install python-mirobo`

`npm install miio`

### 参考信息

[Home Assistant 中文文档](https://sspai.com/link?target=https%3A%2F%2Fhome-assistant.cc%2F)

[Documentation - Home Assistant](https://sspai.com/link?target=https%3A%2F%2Fwww.home-assistant.io%2Fdocs%2F)

[Xiaomi Smart WiFi Socket and Smart Power Strip - Home Assistant](https://sspai.com/link?target=https%3A%2F%2Fwww.home-assistant.io%2Fintegrations%2Fswitch.xiaomi%5Fmiio%2F)

[REST API | Home Assistant Developer Documentation](https://sspai.com/link?target=https%3A%2F%2Fdevelopers.home-assistant.io%2Fdocs%2Fapi%2Frest%2F)

## 4.1 特定位置摇晃手机开关灯

### 功能描述

这里只是举个例子来说明你可以利用手机的传感器作为触发条件控制智能家居。

* 手机在特定角度摇晃一定时间，小米插座会打开 / 关闭。
* 当你手机放到无线充电座，姿势传感器维持 5 秒不变，打开无线充电插座。
* 手机放到某支架 5 秒以上 / 扫描到支架上 NFC，蓝牙连接音响，关灯进入影院模式

手机在特定角度摇晃一定时间，小米插座会打开 / 关闭。

### 配置思路

Tasker 更新至 5.9.3 后，新增了 [Any Sensor](https://sspai.com/link?target=https%3A%2F%2Ftasker.joaoapps.com%2Fuserguide%2Fen%2Fhelp%2Fany%5Fsensor%5Fbase.html) 功能，意味着 Tasker 可以使用你手机上很多没列出的传感器了。可以参考这个 [Live Creations #42 - New Sensor State, Event and Actions - YouTube](https://sspai.com/link?target=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Ftime%5Fcontinue%3D1%26v%3D766S-KRnaiE%26feature%3Demb%5Flogo) 演示视频。

```gauss
if (左右摇晃，低敏感，长时间) And (gravity 传感器在特定区间内)：
向 HA 发送开关灯的命令
Endif
```

至于怎么利用 Tasker 向 HA 发送请求，可以参考 [⚙️ Using Tasker with Home Assistant (V2) - Share your Projects! - Home Assistant Community](https://sspai.com/link?target=https%3A%2F%2Fcommunity.home-assistant.io%2Ft%2Fusing-tasker-with-home-assistant-v2%2F149366) 这篇文章，说得非常清楚。

我仍然以小米智能插座 WIFI 版为例展示我的配置 ( **需提前导入 HA call-service 这个任务** )：

```llvm
# 关闭小米智能插座
Tasker 选择「执行任务」，具体参数如下
Name: HA call-service
Priority: %priority
Parameter1(%par1): switch.turn_off
Parameter2(%par2):{"entity_id":" 我设置的小米插座名字 "}
```

## 4.2 手环单击开关灯

### 功能描述

这个例子用于说明手环也可以作为触发条件控制智能家居。

* 晚上不拿手机上床，通过手环关闭所有灯光：在小米手环心率界面，长按震动后单击，小米智能插座会打开 / 关闭。
* 进入浴室后通过手环控制手机连接浴室的音箱，播放 / 暂停音乐。

### 配置思路

这部分实际上是 Tasker + Notify&Fitness For Mi Band 的进一步应用。

```css
If 接收到 intent(com.mc.miband.buttonPressed1):
向 HA 发送开关灯的命令
Endif
```

当然，NF for Mi Band 还可以接收 / 发送更多的 Intent，你可以在 [Notify&Fitness for MiBand ，intent 参考文档 ](https://sspai.com/link?target=http%3A%2F%2Fwww.mibandnotify.com%2Fhelp%2Ftasker%5Fsend%5Fintent.php)找到具体的参考说明。

## 4.3 Quicker 管理 HA 家居

### 功能描述

这部分其实有点跑题 .. 不过这确实是我折腾 HA 的初衷之一——实现在电脑上操控智能家居。之前开关灯、空调还需要拿起手机-解锁-点击桌面快捷方式，这样的步骤对于我这样一个懒人实在是太麻烦了。。

现在在 Windows 上直接唤起 Quicker 面板，鼠标点击就可以开关灯、空调设置温度，全程无手机介入，非常舒服。

比如「我出门了」这个命令，运行后台灯、饮水机、空调会自动关闭，电脑也会锁屏并息屏。

![](https://proxy-prod.omnivore-image-cache.app/0x0,sIqeBn_cbk1WZX6q3GYoXjm67d4fubMWAXiNHkFiKYEY/https://cdnfile.sspai.com/2020/10/19/3b6c7178cea72991bccdaf802110dab1.png?imageView2/2/format/webp)

### 配置思路

本质上就是通过 Quicker 向 HA 发 Post 请求实现相关操作，具体的细节需要参考 [REST API | Home Assistant Developer Documentation](https://sspai.com/link?target=https%3A%2F%2Fdevelopers.home-assistant.io%2Fdocs%2Fapi%2Frest%2F) 这个官方文档。

我同样以小米智能插座 WIFI 版本展示 Quicker 发 HTTP 请求关闭插座的相关配置：

* 网址：`http://IP_ADDRESS:8123/api/services/switch/turn_off`
* 方法：`POST`
* 请求头：`Authorization: Bearer ｛你生成的 token｝`
* 请求体类型：`JSON`
* 请求体：`{"entity_id":" 在 ‘服务中’ 找 "}`

其他可供参考的 API：

* 米家台灯一代开关灯：`http://{IP}:8123/api/services/light/toggle`
* 米家空调伴侣 2 代设定温度：`http://{IP}:8123/api/services/climate/set_temperature`

### 参考信息

[小米空调伴侣 2 插件接入 HA](https://sspai.com/link?target=https%3A%2F%2Fbbs.hassbian.com%2Fthread-10763-1-1.html)

## 4.4 手机自动保持电量在 40%-80%

### 功能描述

上文提到的两台手机都是常年放在家里面，兼具短信转发和 HA 中心的功能。为了尽量保证电池的健康和安全，两台手机充电到 80% 会自动断开充电插座，电量降到 40% 会自动打开充电插座。

PS：iOS 其实也可以利用「自动化」和米家场景实现同样的效果。

### 配置思路

```angelscript
if (电量到达 40/80 %):
打开 / 关闭 充电插座
Endif
```

## 5、Tasker + Join

[Join](https://sspai.com/link?target=https%3A%2F%2Fjoaoapps.com%2Fjoin%2F) 是 Tasker 作者的另一款产品，用于将 Windows、Android、浏览器、IFTTT 打通的一款工具。

我比较喜欢的几点功能如下：

* Win10 上 Chrome 打开的网页可以直接投在手机上打开，反之手机打开的网页也可以直接分享到 Chrome 上打开
* 剪贴板自动同步
* 多设备之间互相发送通知 +Tasker 联动

当然，Join 还有更多的功能，比如电脑控制手机截屏到电脑、录屏到电脑、定位手机、让手机响铃……

此部分无需 Root，adb。

## 5.1 控制另一台手机播放 / 暂停音乐、调整音量

### 功能描述

最近在根据 [人人都能用英语-语音篇 ](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fxiaolai%2Feveryone-can-use-english%2Fblob%2Fmaster%2Fchapter3.md)尝试重建自己的语音过滤系统，所以需要听很多英语材料。可手头又没个音箱外放，于是我把目光投向了我闲置已久的短信转发手机——红米 Note 4x。

因为它平时所在的位置比较奇怪，拿起来操作不太方便，所以我希望它除了能够长久播放，还可以通过另一台手机远程控制播放暂停音量。甚至进一步可以实现主力手机有电话进来，它自动停止播放；电话挂掉，它恢复播放这种功能。

在红米上安装完 Tasker 之后，我找到了 [Poweramp – Music Player for Android](https://sspai.com/link?target=https%3A%2F%2Fpowerampapp.com%2F) 这款本地音乐播放器支持通过 Intent 控制播放 / 暂停、上一曲、下一曲等操作。所以此部分实际上是 Tasker+Join+Poweramp 。

### 配置思路

* 在 Mi10 上的 Tasker 创建一个任务，通过 Join 在 Tasker 上的插件向红米上的 Join 发送一条特定文本
* 红米上的 Tasker 通过 Join 的插件检测到接收到特定文本，通过 Intent 执行命令以控制 Poweramp 播放

值得注意的一点是，如果你是通过参考文档中 Reddit 网友提供的 [链接 ](https://sspai.com/link?target=https%3A%2F%2Ftaskernet.com%2Fshares%2F%3Fuser%3DAS35m8l%252B3zs0BR1AZDj4AuATCi6sHXkf5gWIgaHE4nGBxoUJYqGDo%252FdXDzy829iShgNjLWU%253D%26id%3DProject%253APA%2BCtrl)下载的 Poweramp(intents) v1.1 这个「任务」，它默认的 Intent 的 `Target` 是 `Service`，如果测试控制不成功的话，可能需要将其改成 `Activity` 才能正常使用。你也可以在后面导入我修改好的「任务」。

### 参考文档

* [\[PROJECT SHARE\] PowerAmp control panel to control media function :) : tasker](https://sspai.com/link?target=https%3A%2F%2Fwww.reddit.com%2Fr%2Ftasker%2Fcomments%2Fi26864%2Fproject%5Fshare%5Fpoweramp%5Fcontrol%5Fpanel%5Fto%5Fcontrol%2F)
* [powerampapi/PowerampAPI.java at master · maxmpz/powerampapi](https://sspai.com/link?target=https%3A%2F%2Fgithub.com%2Fmaxmpz%2Fpowerampapi%2Fblob%2Fmaster%2Fpoweramp%5Fapi%5Flib%2Fsrc%2Fcom%2Fmaxmpz%2Fpoweramp%2Fplayer%2FPowerampAPI.java)

## 5.2 另一台手机接收的短信通过 Join 直接转发

### 功能描述

其实这台手机本身已经配置了 [通过 IFTTT 转发到 TG 了 ](https://sspai.com/link?target=https%3A%2F%2Fiamcristye.github.io%2FSMS-forwarding-using-IFTTT)，添加这个 Tasker Profile 算是多一重保险吧。

如标题所言，红米接收的短信会通过 Join 直接转发到我的 Mi10 上。

不过后来发现，对于经常使用电脑的人而言，还是将短信转发到微信上更方便一些……

### 配置思路

* Tasker 检测到短信，通过 Join 将短信内容、发信人、发信时间发送到 Mi10 上；

其中可能会用到的变量名称及含义如下

* `%SMSRB`：短信文本
* `%SMSRF`：发信人
* `%SMSRD`：发送日期
* `%SMSRT`：发送时间

### 参考信息：

[用 Tasker 实现收到 Android 手机短信自动转发到微信-Tasker 配置教程站](https://sspai.com/link?target=http%3A%2F%2Ftaskerm.com%2F2018%2F12%2F22%2Fforwarded-sms-to-wechat%2F)

## 6、Tasker + Keep

## 6.1 Keep 开始运动后小米手环开始记录

### 功能描述

因为 Keep 并不支持连接小米手环，所以手环上的很多传感器在 Keep 的运动场景上毫无用武之地。每次想在 Keep 记录运动时，还需要手动打开 NF for Mi Band 创建运动，然后再切回 Keep，非常麻烦。

设置 Tasker 之后可以实现在 Keep 点击「开始运动」后，小米手环自动以「跑步」模式创建运动开始监测数据。

同样这里也用到了 Tasker 的 Logcat Entry 功能作为监测条件。

### 配置思路

```armasm
if (Logcat Entry 捕捉到 Keep 开始运动的日志):
通过 NF for Mi Band 的 Tasker 插件创建某一模式的运动
Endif

# 参考的 Logcat Entry 配置
Component: ActivityTaskerManager
Filter: START u0 {cmp=com.gotokeep.keep/.tc.business.training.core.activity.TrainingActivity (has extras)} from uid 10086
```

### 依赖配置

* 需要安装 Notify&Fitness for Mi Band
* 无需 Root，但开启 Logcat Entry 功能需要 adb 授权

## 7、其他

## 7.1 息屏下连接 Airpods 时自动朗读微信通知

### 功能描述

见名达意，还可以把 Airpods 换成车载蓝牙，也算变相地实现了微信收消息的车载模式吧。

比如开车、骑车这类场景不方便打开手机看消息、看手环也会影响注意力，利用耳朵则是一个很好的方法。

简单实现的功能如下：

* 同一个人多次发送消息只会说一次姓名
* 多条消息的「\[n 条\]」不会被播报
* 群聊中的「@ 微信名」会被替换为「@ 我」

推荐更进一步的操作：[Tasker 一个配置实现微信朗读，微信消息播报 + 基础版的防撤回-CSDN 博客 \_tasker 获取通知内容](https://sspai.com/link?target=https%3A%2F%2Fblog.csdn.net%2Fh137242126%2Farticle%2Fdetails%2F81235926)

### 配置思路

主要介绍一下通知文本的处理过程 (Mi10 调用的小爱同学发音引擎，其他型号手机需要自行设置)

```perl
# 变量说明
%Wechat_sender #存储微信发信人，由 %evtprm2 赋值
%say_text #存储通知文本，由 %evtprm3 赋值

If (两次发信人不相同):
存储发信人姓名到 %Wechat_sender
文字转语音：「%Wechat_sender 说」
Endif
存储通知文本到 %say_text
正则搜索替换「.*:」, 去除多条信息的 "[n 条]:"
If(通知文本中有 「@ 微信名」)
搜索「@ 微信名」为「@ 我」
文字转语音：「@ 我」
Endif
文字转语音：「%say_text」
```

## 7.2 连接 AirPods 后且前台非音视频应用自动播放听力

### 功能描述

和 5.1 一脉相承，同样是为了磨耳朵，主要用于出门在外的场景。

连接 AirPods 后，只要前台不是电话和音视频应用，就自动控制 Poweramp 开始播放，反之停止播放。

### 配置思路

```gauss
If (连接了 Airpods) And (前台不是某些应用):
Poweramp 开始播放
Else:
停止播放
Endif
```

### 依赖配置

* 需要安装 Poweramp，地址参考 5.1

## 7.3 通过小爱同学执行 Tasker 命令

### 功能描述

因为手机上的小爱同学进行理解时，可以通过 Logcat Entry 功能监测到语音生成的文本。所以，我们可以向手机的小爱同学说特定文本，执行 Tasker 某条「任务」。

### 配置思路

以下配置基于 Mi10，MIUI12，其他手机或需要另行修改。同时建议给小爱添加自定义回复，避免小爱回复「听不懂，请重说一遍」。

通过 Logcat Entry 检测小爱同学转换的文本

* Component：`XmodeTextView`
* Filter：`setTextWithAnimation｛要转换的文本｝`

### 依赖配置

* 无需 Root，但 Logcat Entry 需要 adb 开启

## 7.4 扫描特定 NFC 卡片打开体重秤连接界面

### 功能描述

每天早上我会测量记录体重体脂状况，而每次「打开手机-找到 NF-切换 Tab-点击体重 」实在是太麻烦了 ...

利用 Tasker 则可以极大地简化这个流程，起床后把手机放在桌面特定的位置 (下面有 NFC Tag)，然后站到体重秤上，体重体脂数据就会自动同步到手机。

NF For Mi Band 支持的体重秤版本如下：

> Since 7.3.6 Notify app version these scales are supported
> 
> Please notice, if you are using also the official app of the scale there could be some conflicts. We suggest use only one app (notify or the official app)
> 
> **Xiaomi Mi Scale 1**Full support
> 
> **Xiaomi Mi Scale 2**Full supportBody values (fat, water, ...) are calculated by cloud notify server. We never save / redistribute any user data on cloud server.
> 
> **Yunmai Scale Mini**Does not support offline data sync. Can measure values only when is connected.
> 
> **Yunmai Scale SE**Does not support offline data sync. Can measure values only when is connected.
> 
> **Beurer BF700 & BF800**Full support
> 
> **Beurer BF710**Full support
> 
> **Runtastic Libra**Full support
> 
> **Sanitas SBF70**Full support
> 
> **SilverCrest SBF75**Full support

### 配置思路

```css
# 类别是 Send Intent，下面是具体参数设置
Package: com.mc.miband1 # NF 的包名
Class: com.mc.miband1.ui.main10.health.WeightActivity # NF 里面体重秤的 Activity
Target：Activity
```

包名、当前页面的 Activity 都可以通过 [开发者助手 (com.toshiba\_dealin.developerhelper) - 1.2.1 - 应用 - 酷安网 ](https://sspai.com/link?target=https%3A%2F%2Fwww.coolapk.com%2Fapk%2Fcom.toshiba%5Fdealin.developerhelper)获取。

### 依赖配置

* 手机支持 NFC(或者你采用其他触发条件也行)
* 需要安装 Notify&Fitness for Mi Band，并且自己有支持的体重秤

---

## 结语

我曾经在知乎搜索过「Tasker 有什么有趣的玩法」这个问题，不过下面的回答多是 2015、2016 年的，时效性大打折扣。

在国内平台上，受制于 Google 套件和 kx 网络，Tasker 的相关资料比较少，这里要特别感谢少数派 @Fairyex 等几位作者写的 Tasker 分享，比较受启发；在国外的平台上，则要感谢 Reddit 上的作者和热心网友了，提供了很多资料与思路。

随着 Tasker 自身的更新和第三方应用的完善，相信 Tasker 会有更多的可能。非常希望大家能够在评论区分享出自己的玩法，供更多朋友参考！

配置链接：[https://www.jianguoyun.com/p/Ddu1CC8QyODhBxiB1sID](https://sspai.com/link?target=https%3A%2F%2Fwww.jianguoyun.com%2Fp%2FDdu1CC8QyODhBxiB1sID)

**拓展阅读：**

* [记账总是半途而废？用 Tasker + 钱迹实现自动记账](https://sspai.com/post/61292)
* [被誉为 Android 效率利器的 Tasker，生活中究竟可以怎么用？](https://sspai.com/post/58457)
* [如何让 Android 10 拥有不输 iOS 的暗色模式体验？](https://sspai.com/post/56905)

\> 下载少数派 [客户端 ](https://sspai.com/page/client)、关注 [少数派公众号 ](https://sspai.com/s/J71e)，了解更妙的数字生活 🍃

\> 想申请成为少数派作者？[ 冲！](https://sspai.com/apply/writing)

2、Tasker + Notify&Fitness for Mi Band

4.0 安装 HomeAssistant 与接入米家设备

5.1 控制另一台手机播放 / 暂停音乐、调整音量

5.2 另一台手机接收的短信通过 Join 直接转发

7.1 息屏下连接 Airpods 时自动朗读微信通知

7.2 连接 AirPods 后且前台非音视频应用自动播放听力

© 本文著作权归作者所有，并授权少数派独家使用，未经少数派许可，不得转载使用。

