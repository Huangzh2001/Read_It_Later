---
id: 8c95904a-66ae-4709-8aa7-88dae8ca7622

url: https://zhuanlan.zhihu.com/p/649017215
---


tags::  #Readed 

# Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsdian-18f6826d52e)
[Read Original](https://zhuanlan.zhihu.com/p/649017215)

众所周知Obsdian附件和链接管理不好会把自己的文件目录搞得异常混乱，这里提供一种解决方案

最终文件结构是把note中的附件放在与note同级的attachments文件下

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/81a4dd13bbfb2ca89f31faad0516facc_MD5.jpg]]

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/1dd90fdc5d2136fc56dbb58e7ce446cb_MD5.jpg]]

该设置使写笔记时添加附件，将附件自动存到同级的attachments文件夹中

## 插件

### 1.Local images plus

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/178e83c699f8effffc9c14ccbff59fb7_MD5.jpg]]

该插件会自动将网络文章中的web图片下载到本地，为了保存路径与上述一致，需要修改设置

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/29311943770246d087a6e96830785527_MD5.jpg]]

用相对路径引用附件

### 2.Consistent atttachments and links

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/34bc1c23966287c9bfe32d7fdc18af17_MD5.jpg]]

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/1806f43152b666bdd45f8bfe719c01c3_MD5.jpg]]

设置如上

该插件主要解决的是文件在移动过程中的附件的跟随问题，设置完成后能使文章中引用的附件跟随文件一起移动，在移动后将未被引用的附件自动删除，并更改笔记中的引用链接

## 关于obsdian的引用的小科普

obsdian的比较常用的引用有两种：

一种为markdown引用，即!\[\]()和\[\]()形式

一种为wiki引用，即!\[\[\]\]和\[\[\]\]形式

markdown引用是比较严格的，想要正确引用需要把附件和笔记的相对位置关系写清楚，

而wiki引用比较随意，只要库里没有重名文件就可以随意引用

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/c3e04bb05c92d121b2de9fe27276027e_MD5.jpg]]

wiki引用比较方便随意，不用考虑相对位置

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/107f342829c54850ebae9c7c928a4fcb_MD5.jpg]]

一个图片文件

![[Omnivore/Obsdian文件附件下载、管理与移动的插件解决方案 - 知乎/attachments/4cb65021d3da78043428b16981214010_MD5.jpg]]

同一个文件，wiki引用比较随意，但对markdown引用格式来说只有引用形式1是严格正确的

但是obsdian比较智能，会自动以wiki引用的模式识别markdown引用，所以看到后面三个每个都有效

所以综上要点是，我们在写笔记互相引用时，可以使用wiki引用比较方便，但是在添加图片等附件时最好还是保持一个统一的格式,即本文使用的/folder/note,/folder/attachments/{附件文件}

## 完

如果有什么内容上的问题欢迎纠正，写的时间很短没有严格查资料，如果有其他需求我也会更新本文

