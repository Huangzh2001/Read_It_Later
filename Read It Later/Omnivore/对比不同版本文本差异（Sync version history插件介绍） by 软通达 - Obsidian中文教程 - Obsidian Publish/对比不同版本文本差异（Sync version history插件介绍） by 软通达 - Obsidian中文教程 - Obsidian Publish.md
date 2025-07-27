---
id: ea72528e-7e65-4060-bb30-328e56498a27

url: https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E5%AF%B9%E6%AF%94%E4%B8%8D%E5%90%8C%E7%89%88%E6%9C%AC%E6%96%87%E6%9C%AC%E5%B7%AE%E5%BC%82%EF%BC%88Sync+version+history%E6%8F%92%E4%BB%B6%E4%BB%8B%E7%BB%8D%EF%BC%89+by+%E8%BD%AF%E9%80%9A%E8%BE%BE
status: readed
---


tags::  #Readed 

# 对比不同版本文本差异（Sync version history插件介绍） by 软通达 - Obsidian中文教程 - Obsidian Publish
#Omnivore

[Read on Omnivore](https://omnivore.app/me/sync-version-history-by-obsidian-obsidian-publish-191e637b374)
[Read Original](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E5%AF%B9%E6%AF%94%E4%B8%8D%E5%90%8C%E7%89%88%E6%9C%AC%E6%96%87%E6%9C%AC%E5%B7%AE%E5%BC%82%EF%BC%88Sync+version+history%E6%8F%92%E4%BB%B6%E4%BB%8B%E7%BB%8D%EF%BC%89+by+%E8%BD%AF%E9%80%9A%E8%BE%BE)

对比不同版本文本差异（Sync version history插件介绍） by 软通达

## 引言 

对比不同版本间文本的差异是一项急需且常用的功能。一般纯文本的比较工具是git，除了git外，Beyond Compare等工具也能提供更为高级的对比。  
Sync version history则可以较好实现git中的对比功能（diff），对obsidian库中的文本进行对比。

## 插件名片 

Sync version history插件是由kometenstaub开发，目前版本1.2.0。

Github地址： <https://github.com/kometenstaub/obsidian-sync-version-history>

## 实际操作 

需要先了解的信息：

1. Sync version history插件需要搭配ob核心插件中的[同步（sync核心插件）](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E5%90%8C%E6%AD%A5%EF%BC%88sync%E6%A0%B8%E5%BF%83%E6%8F%92%E4%BB%B6%EF%BC%89)或者[文件恢复（File Recovery，核心插件）](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E6%96%87%E4%BB%B6%E6%81%A2%E5%A4%8D%EF%BC%88File+Recovery%EF%BC%8C%E6%A0%B8%E5%BF%83%E6%8F%92%E4%BB%B6%EF%BC%89)。
2. [文件恢复（File Recovery，核心插件）](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E6%96%87%E4%BB%B6%E6%81%A2%E5%A4%8D%EF%BC%88File+Recovery%EF%BC%8C%E6%A0%B8%E5%BF%83%E6%8F%92%E4%BB%B6%EF%BC%89)可以参考往期推文[obsidian内置文件恢复（File Recovery功能介绍） by 软通达](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/obsidian%E5%86%85%E7%BD%AE%E6%96%87%E4%BB%B6%E6%81%A2%E5%A4%8D%EF%BC%88File+Recovery%E5%8A%9F%E8%83%BD%E4%BB%8B%E7%BB%8D%EF%BC%89+by+%E8%BD%AF%E9%80%9A%E8%BE%BE)。
3. [文件恢复（File Recovery，核心插件）](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E6%96%87%E4%BB%B6%E6%81%A2%E5%A4%8D%EF%BC%88File+Recovery%EF%BC%8C%E6%A0%B8%E5%BF%83%E6%8F%92%E4%BB%B6%EF%BC%89)所备份的镜像仅限本机，且有一定时效性（以你设置为主）。[同步（sync核心插件）](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/%E5%90%8C%E6%AD%A5%EF%BC%88sync%E6%A0%B8%E5%BF%83%E6%8F%92%E4%BB%B6%EF%BC%89)的数据则可以联机。

安装并启动插件。因为我没有同步服务，所以只演示文件恢复的模式。

进入Crtl+P进入命令模式，进入“Version history diff:Show File Recovery diff view for active file”（注意不要进入sync的选项，如果没有同步如何就会是一个空白弹窗）。  
![[Omnivore/对比不同版本文本差异（Sync version history插件介绍） by 软通达 - Obsidian中文教程 - Obsidian Publish/attachments/244f6e2e63b8058942198c82209da944_MD5.png]]

然后就会弹出类似git的窗口  
![[Omnivore/对比不同版本文本差异（Sync version history插件介绍） by 软通达 - Obsidian中文教程 - Obsidian Publish/attachments/de0c4bb82a29406903fcd199378df341_MD5.png]]

建议可以在文件恢复中，将快照的保存时长设置长一些，例如30天。  
![[Omnivore/对比不同版本文本差异（Sync version history插件介绍） by 软通达 - Obsidian中文教程 - Obsidian Publish/attachments/90ec24aaf201d52ac711b694c6e6e3ac_MD5.png]]

[obsidian插件列表与教程（MOC）](https://publish.obsidian.md/chinesehelp/01+2021%E6%96%B0%E6%95%99%E7%A8%8B/obsidian%E6%8F%92%E4%BB%B6%E5%88%97%E8%A1%A8%E4%B8%8E%E6%95%99%E7%A8%8B%EF%BC%88MOC%EF%BC%89)

对比不同版本文本差异（Sync version history插件介绍） by 软通达

引言

插件名片

实际操作

