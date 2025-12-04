---
date: 2025-12-04T23:53:27+08:00
url: https://zhuanlan.zhihu.com/p/1908807507461252811
status: readed
---
![[Read It Later/attachments/771be27478181f46769f1688e245175c_MD5.png]][

关注

](https://www.zhihu.com/follow)[

推荐

](https://www.zhihu.com/)[

热榜

](https://www.zhihu.com/hot)[

专栏

](https://www.zhihu.com/column-square)[

圈子

New

](https://www.zhihu.com/ring-feeds)

[

付费咨询

](https://www.zhihu.com/consult)[

知学堂

](https://www.zhihu.com/education/learning)

[直答](https://zhida.zhihu.com/)

[

创作中心

](https://www.zhihu.com/creator)

真零门槛实现 Obsidian 多端实时同步：坚果云官方插件实测体验

首发于[构建个人知识库](https://www.zhihu.com/column/c_1886339293426983713)

![[Read It Later/attachments/ade0b444cb21f698131ac9489f512c48_MD5.png]]

# 真零门槛实现 Obsidian 多端实时同步：坚果云官方插件实测体验

[![[Read It Later/attachments/13ac595fc6b1c21933f00cc2aaf6a1ae_MD5.jpg]]](https://www.zhihu.com/people/geosmartx)

[极客工具](https://www.zhihu.com/people/geosmartx)

共享开源力量，成就超级个体

[

收录于 · 构建个人知识库

](https://www.zhihu.com/column/c_1886339293426983713)

16 人赞同了该文章

![[Read It Later/attachments/305559fc38a488f5470528bc182eb332_MD5.jpg]]

obsidian坚果云插件同步 image 20250520

Obsidian 多端同步方案不少，但真正丝滑又靠谱的，没那么多。我分别实测了 Git、LiveSync、WebDAV（坚果云）三种方式，最终选择主库用 Git 做版本控制，移动端用坚果云插件做实时同步。两者搭配，一周体验下来稳定高效，还免费。本文将分享完整配置流程、遇到的问题与避坑建议，助你快速找到适合自己的同步组合。

## **真零门槛实现 Obsidian 多端实时同步：坚果云官方插件实测体验**

## **Why｜为啥还要自己折腾同步方案？**

对于 Obsidian 用户来说，**「同步」** 永远是刚需：

- 想在手机上随时记录灵感、剪藏内容
- 想在电脑上整理、加工、建构知识
- 想避免误操作、文件冲突、数据丢失

官方 Obsidian Sync 虽好，但年费不低，对轻度用户性价比不高。我试过 LiveSync、Syncthing、WebDAV、Git，踩了不少坑，最后总结出这样一个组合：

> ❝  
> ✅ 主库走 Git，稳如老狗  
> ✅ 移动端走 WebDAV（坚果云插件），轻巧丝滑  
> ✅ 分两个 vault，互不干扰，各司其职  
> ❞

尤其是在媳妇同步配置遇阻之后，我意识到：**「易用性和低门槛也很重要。」** 这也是我选择坚果云作为**「移动端同步方案」**的主要原因。

坚果云，在国内 13 年的云存储运营经验、传输不限速、对**「WebDAV」**的支持良好，全平台兼容

![[Read It Later/attachments/a783e76f0e1f733ff809f06c9e0ef1d9_MD5.jpg]]

obsidian坚果云插件同步 image 20250517 5

## **What｜三种方案对比，我为何选择「双库同步」？**

| 同步方式 | 适配场景 | 优势亮点 | 潜在问题 |
| --- | --- | --- | --- |
| 「Git 同步」 | 主库（重度编辑） | 完整版本控制、安全回滚 | 手机端配置复杂，非实时同步 |
| 「坚果云插件」 | 移动端轻量记录 | 实时双向同步、界面可视化 | 请求频率有限，不适合大库 |
| 「LiveSync」 | 多端频繁改动同步 | 端到端加密 | 服务搭建门槛高，维护成本大 |

我最终的结构是这样的：

### **Vault 1 - 主库（Git 同步）**

- 用 Git 管理，支持版本快照与回滚
- 适合深度写作、资料整理、大量结构化内容
- 每次提交都有记录，AI 自动处理笔记也能溯源

### **Vault 2 - 移动端库（坚果云同步）**

- 安装坚果云官方发布的 Obsidian 同步插件
- 通过坚果云 webdav 实现安卓/iOS 手机与电脑的轻量双向同步
- 适合灵感记录、剪藏、日记类笔记，免费 5G 空间，上传流量1G/月

这样做有几个好处：

1. **「安全性高」**：重要笔记可回滚，移动笔记也不易丢
2. **「同步快」**：小 vault 实时同步，不用整库上传下载
3. **「维护成本低」**：不用搭建服务器、不怕版本冲突

> ❝ 专业用户也可以使用NAS部署自己的webdav服务  
> ❞

## **How｜配置步骤总结**

### **Git 同步配置（主库）**

详见我的文章 [Obsidian Git 同步方案详解](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/CfEvY0HOgwSHx3lKC4GD8w)

核心要点：

- 配置 [SSH Key](https://zhida.zhihu.com/search?content_id=258036681&content_type=Article&match_order=1&q=SSH+Key&zhida_source=entity)（电脑 + 手机）
- 使用 GitSync / MGit（安卓）连接仓库
- Obsidian 安装 Git 插件，定时自动提交

### **坚果云插件配置（移动库）**

### **服务端配置流程**

坚果云创建应用,准备 webdav 密码：打开坚果云网页版，点击右上角昵称—账户信息，然后选择安全选项，在安全选项页面拉到最底，添加应用，输入 Obsidian，生成密码（这个密码待会儿是要填写到 `坚果云的obsidian插件` 的 `帐号设置-凭证` 中），这样坚果云盘就配置好了

![[Read It Later/attachments/6e76281b6b168333cbe311d89f8f0058_MD5.jpg]]

  

### **Obsidian 坚果云插件下载**

下载地址：`https://github.com/nutstore/obsidian-nutstore-sync/releases` 可以直接手动从 release 下载 zip 包，手动安装 obsdian 插件。

> ❝ 离线插件安装方法见：[Obsidian 社区插件安装终极指南](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/GJqeaSc50TlwTGWaZFibGw)  
> ❞

### **Obsidian 坚果云同步插件配置**

Obsidian 安装坚果云同步插件，设置远程地址、凭据、本地同步路径，将数据同步到坚果云 （此处的凭证就是你的 `第三方应用管理` 里面新增应用的 `应用密码`）

![[Read It Later/attachments/ecac0f8daf58808fe8cfc2a40683f98d_MD5.jpg]]

![[Read It Later/attachments/9f3c4f0d33320633e9b0b210dc68a966_MD5.jpg]]

![[Read It Later/attachments/bc4df5cad1cead6710280d7d01cbdd0e_MD5.jpg]]

  

坚果云上同步后的文件结构和本地一致

![[Read It Later/attachments/b14ffcc06af2934a79ab630f85df91f2_MD5.jpg]]

  

### **手机端操作**

### **使用 webdav 客户端初始化同步目录**

1. webdav 客户端安装：mixplorer，下载地址: [https://mixplorer.com](https://link.zhihu.com/?target=https%3A//mixplorer.com)
2. mixplorer 添加 webdav 存储，配置坚果云帐号
3. webdav 客户端，复制同步目录到本地目录，比如: `1/sync/mobile`

> ❝ PS 我习惯定义 `1` 为自己的工作目录，在安卓系统排在靠前的位置，比较容易找到  
> ❞

### **obsidian 客户端打开 vault**

1. obsidian 中打开 vault,选择 `1/sync/mobile`
2. 修改一些文件
3. 点击右下角的操作按钮，弹出工具栏，点击 `开始同步`

### **微信小程序端**

坚果云收藏小程序：可以将微信聊天文件直接收藏到 obsidian 的指定目录

> ❝ 可惜暂时不支持文章转发到坚果云盘  
> ❞

## **⚠ 实践中遇到的问题**

### **同步频率限制**

![[Read It Later/attachments/480e9ab0f4ca7b30ad860026fb10868e_MD5.jpg]]

obsidian坚果云插件同步 Screenshot from 2025 05 17 16 53 42 20250517

![[Read It Later/attachments/1aff29e97c004cadb3ff5661fd8b9230_MD5.jpg]]

obsidian坚果云插件同步 Screenshot from 2025 05 17 16 53 59 20250517

尽管坚果云号称不限速，但服务端对 `请求频率` 有控制。笔记库较大时，会出现同步中断的情况：

> ❝ 所以坚果云更适合 " 轻量 vault"，用于灵感记录而非完整知识库。  
> ❞

但是，我的笔记是分 2 个库的，移动端笔记少，实时性要求高，5g 免费空间的临时笔记也足够用，坚果云完全满足需求。

建议：由于obsidian的文件修改特别频繁，坚果云同步插件配置关闭`实时同步`，需要同步时手动触发，避免达到`请求频率`限制

![[Read It Later/attachments/dc19de0449307804e7c28c92314bf0ed_MD5.jpg]]

obsidian坚果云插件同步 image 20250517 6

同步指令

![[Read It Later/attachments/f5762ad3aee75dbcfc514256b2d017dc_MD5.jpg]]

  

移动端同步

![[Read It Later/attachments/9ad5fc62164c5bbc983f0020263d9483_MD5.jpg]]

  

### **冲突自动合并体验**

坚果云插件内置冲突检测与字符级自动合并，体验优于 LiveSync。大多数情况无需手动干预。

电脑端同步，检测到冲突，自动合并，自己手动处理下就行。与 git 方案相比，不需要额外安装一个 `gitsync` 客户端，同步操作都在 obsidian 软件内点击，体验更好。

![[Read It Later/attachments/2d98099b985169f7b4dd5a22e43a6b33_MD5.jpg]]

  

## **总结｜选择组合而非纠结唯一**

很多人问我：**「到底选 Git 还是 WebDAV 还是 LiveSync？」** 我的建议是：**「按场景选工具，组合更灵活。」**

- 需要 `版本历史、回滚、安全`？➡️ 用 Git
- 需要 `快速收集灵感、随手记录`？➡️ 用 WebDAV
- 对同步频率要求极高、有自建服务经验？➡️ 可试试 LiveSync

**「同步不求一步到位，但求各尽其用。」** 我这套 `Git + 坚果云 的双 vault 同步结构`，推荐给同样想兼顾安全与便捷的你。

## **麦冬的实战建议**

1. **「Git 与 WebDAV 不建议混用同一个 Vault：」** 避免潜在的冲突和复杂性。
2. **「定期手动归档：」** 将移动端库（坚果云同步）中的内容定期归档到主库（Git 同步），保持移动端库的清爽和高效。
3. **「强烈建议备份！备份！备份！」** 无论您选择哪种同步方案，多一份备份，多一份安心。
4. **「善用自动化：」** 充分利用 Git 插件的自动 commit + pull 功能，省心省力。

欢迎在留言你的同步实践，也欢迎分享给还在折腾 Obsidian 同步的朋友。

**「更多延伸阅读，按需探索：」**

1. 搞好了同步，闪念笔记走起 [零延迟捕捉灵感！Markor + 微信语音 + Obsidian 手机端笔记三步攻略](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/VOuxZiNc-F-oYHntIdbP-w)
2. 可组合Git作为备份 [零门槛实现 Obsidian 多端实时同步：非开发人士也能轻松上手](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/JoJ6JNAofNDsWYG9DKd0xA)
3. Obsidian附件太多，需要整理 [Obsidian附件管理最佳实践](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/RXmbeZcucbDWbrDsm7Ah6A)

[所属专栏 · 2025-10-02 08:18 更新](https://zhuanlan.zhihu.com/c_1886339293426983713)

[![[Read It Later/attachments/90c20a09e7b0bccc02d7837cdbbbb623_MD5.webp]]

构建个人知识库

![[Read It Later/attachments/13ac595fc6b1c21933f00cc2aaf6a1ae_MD5.jpg]]

极客工具

36 篇内容 · 545 赞同

](https://zhuanlan.zhihu.com/c_1886339293426983713)

[

最热内容 ·

我的 Obsidian 插件 - 2025

](https://zhuanlan.zhihu.com/c_1886339293426983713)

发布于 2025-05-22 08:56・浙江

[

坚果云

](https://www.zhihu.com/topic/19682895)

[

Obsidian

](https://www.zhihu.com/topic/21349840)

[

Markdown

](https://www.zhihu.com/topic/19590742)

![[Read It Later/attachments/26725aa9602db156eaafd2cb68a4a816_MD5.jpg]]

理性发言，友善互动

  

9 条评论

默认

最新

[![[Read It Later/attachments/b072105671ac47ac1e98f4f5a5824c8b_MD5.jpg]]](https://www.zhihu.com/people/b07975a8e3df85852329859fb265944d)

[Aether](https://www.zhihu.com/people/b07975a8e3df85852329859fb265944d)

livesync的冲突处理真的一言难尽，误操作直接心脏骤停

09-27 · 内蒙古

[![[Read It Later/attachments/3aa7213865a3542f6bc04ac9bbae23e8_MD5.jpg]]](https://www.zhihu.com/people/c1785800ac216901262d09c67ce0d0b3)

[卡卡西](https://www.zhihu.com/people/c1785800ac216901262d09c67ce0d0b3)

[Aether](https://www.zhihu.com/people/b07975a8e3df85852329859fb265944d)

不用手机端最简单，直接用把目录放网盘，用手机的话，我用的onedirve加remote-s什么的插件，同步没问题

10-27 · 北京

[![[Read It Later/attachments/b072105671ac47ac1e98f4f5a5824c8b_MD5.jpg]]](https://www.zhihu.com/people/b07975a8e3df85852329859fb265944d)

[Aether](https://www.zhihu.com/people/b07975a8e3df85852329859fb265944d)

[卡卡西](https://www.zhihu.com/people/c1785800ac216901262d09c67ce0d0b3)

之前obsidian同步不稳定就是

10-16 · 内蒙古

[![[Read It Later/attachments/9c8d61aabbe3ceba141fba1cace1c893_MD5.jpg]]](https://www.zhihu.com/people/56f9b4539f22dab71bccd10853385d9f)

[姜饼](https://www.zhihu.com/people/56f9b4539f22dab71bccd10853385d9f)

“webdav 客户端，复制同步目录到本地目录，比如: 1/sync/mobile”请问这个是啥意思，同步目录指的是哪个？没看懂。如果是把坚果云里的文件复制到本地就不叫同步了吧

11-17 · 湖南

[![[Read It Later/attachments/54ac3008df32b0fc432fd8bd3f71f143_MD5.jpg]]](https://www.zhihu.com/people/aedddd3c2544112b9d83b06d7c5cbdb6)

[蟑螂不死我死](https://www.zhihu.com/people/aedddd3c2544112b9d83b06d7c5cbdb6)

用坚果云WebDAV插件和直接用坚果云客户端相比，有什么优势吗？

10-22 · 浙江

[![[Read It Later/attachments/05f3604a915c319ff3f6c929f2e7e4d1_MD5.png]]](https://www.zhihu.com/people/435e14ffe8ab3c154e7e7db5ade0642f)

[duiyakid](https://www.zhihu.com/people/435e14ffe8ab3c154e7e7db5ade0642f)

电脑端可以直接用坚果云同步文件夹，但是手机端必须通过webdav实现

11-15 · 陕西

关于作者

[![[Read It Later/attachments/13ac595fc6b1c21933f00cc2aaf6a1ae_MD5.jpg]]](https://www.zhihu.com/people/geosmartx)

[极客工具](https://www.zhihu.com/people/geosmartx)

共享开源力量，成就超级个体

[

回答

**110**

](https://www.zhihu.com/people/geosmartx/answers)[

文章

**55**

](https://www.zhihu.com/people/geosmartx/posts)[

关注者

**634**

](https://www.zhihu.com/people/geosmartx/followers)

### 推荐阅读

[

![[Read It Later/attachments/1724191e02e9dbb47a772398f27c62fa_MD5.png]]

# 免费搭建Obsidian多端同步！Docker部署LiveSync全攻略

二冰

](https://zhuanlan.zhihu.com/p/1921717015615349802)[

![[Read It Later/attachments/43701fb1d911a01713a3596e791b448f_MD5.png]]

# Remotely Save实现Obsidian坚果云同步（安卓+Win）

咔咔琳呐

](https://zhuanlan.zhihu.com/p/547381761)[

![[Read It Later/attachments/b875a9338156ca4d12addcdb3b903ce1_MD5.jpg]]

# Obsidian 多端同步方案及R2图床

银之

](https://zhuanlan.zhihu.com/p/664006937)[

![[Read It Later/attachments/a4b36c3db90202c6e74cda8296a88799_MD5.png]]

# Obsidian笔记同步方案

强哥笔记

](https://zhuanlan.zhihu.com/p/17440261603)

❌ 未收藏