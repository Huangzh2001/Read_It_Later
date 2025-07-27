---
id: ae98600d-ba11-48f6-a2e9-df21cfaa1549

url: https://zhuanlan.zhihu.com/p/675034211
---


tags::  #Readed 

# 还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎
#Omnivore

[Read on Omnivore](https://omnivore.app/me/omnivore-obsidian-18f3f125cf1)
[Read Original](https://zhuanlan.zhihu.com/p/675034211)

作者 | 致九

日期 | 2023.11.03

小提示：全文约 1300 字

在以往的文章中提到了 Omnivore 来收藏网页文章、在其中阅读批注。

* [Obsidian搭配sioyek，技术大佬的阅读工作流](https://link.zhihu.com/?target=http%3A//mp.weixin.qq.com/s%3F%5F%5Fbiz%3DMzkzMDAwMTA4MA%3D%3D%26mid%3D2247484436%26idx%3D1%26sn%3Dce156d35f564659e6b12dcaeb033549e%26chksm%3Dc201bdc3f57634d5e4b8c73f572f3d74d08ac9c7b14f4f79dee60feeef27fbfe1b5cbce75eb9%26scene%3D21%23wechat%5Fredirect)
* [多种方法，帮你剪藏网页文章到obsidian中](https://link.zhihu.com/?target=http%3A//mp.weixin.qq.com/s%3F%5F%5Fbiz%3DMzkzMDAwMTA4MA%3D%3D%26mid%3D2247484401%26idx%3D1%26sn%3Ddf5e301d94ac8c7341a390f18bcbb478%26chksm%3Dc201ba26f576333085ce9ecf80728d15b15db356c9f627b684b6ba967d20b97ac112d2bee994%26scene%3D21%23wechat%5Fredirect)

值得称道的是，Omnivore 提供了专属的插件支持，方便一键将收藏的内容和批注同步到 Obsidian 的笔记仓库中。

但是，很多朋友在使用的时候，会发现同步的时候只同步了网页的链接，而没有将收藏的网页内容同步过来。

今天的更新将仔细讲讲如何设置 Omnivore，让它在同步的时候可以将全文同步到本地的 Obsdian 仓库。

## 1 申请 API Key

通过在 Ominvore 申请账号并登陆后，在右上角的头像处，点击头像，并选择「API Keys」选项。

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/2231efe0b8970dccb08c7e886e757a40_MD5.png]]

API key 是用来验证我们身份的，来使其他程序能够通过 API Key 与 Omnivore 交互，并获取到私人的数据，请保存好个人的 API Key。

最开始你这里是干净的，一个 API key 都没有，需要通过小猴子旁边的「Create an API Key」按钮生成一个 API key，输入一个便于分辨的名字后，点击 Generate，然后点击 Copy，复制生成的 API key。

注意⚠️：这里 API key 只会出现一次，不复制的话只能再重新生成一个了。

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/f5be5e41e25717ce2787424a82c9d4a8_MD5.png]]

接下来，你需要在 Obsidian 的第三方插件市场中安装 Omnivore 官方开发的 Omnivore->Obsidian 的同步插件。 

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/3476113ba4c1f65858b74c842541b3a6_MD5.png]]

在 Omnivore 插件设置中，首先需要在「API Key」处粘贴上我们之前生成的 API Key。 

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/45568c6ee3c5e41708528b904d0bee93_MD5.png]]

先不急着同步，我们再看下另外一个设置项目：「Article Template」文章模板。这个选项可以控制被同步的文章以什么样的格式存储在本地文件中。

默认的模版其实并没有包含文章的全部内容，只是包含了标题、高亮、批注等内容。 

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/f911daee70e061b372847b5bf752a759_MD5.png]]

想要包含内容，我们只需要在模板中加上官方给出的模板字符串就行 ，通过点击该设置项目下方蓝色的链接，可以跳转到官方文档，文档右上方有切换语言的选项。

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/e5375d4785064118730ea8d75c0d3ff9_MD5.png]]

可以看到，这里的模板功能非常灵活和强大，支持非常多的元数据，变量多到我一张图截不完，多阅读官方文档，按照自己的习惯，大家也能写出适合自己的内容模板 。 

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/462a03e557e6a6091d4d67ce18e30993_MD5.png]]

在其中，有专门教授如何导入完整文章内容的小节。 

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/9d10e61b54cde67854d67814908d8fad_MD5.png]]

当然，也可以直接复制我这里的模板：

```handlebars
#Omnivore
OmnivoreURL: {{{omnivoreUrl}}}
OriginURL: {{{originalUrl}}}

{{{ content }}}

{{#highlights.length}}
## 高亮

{{#highlights}}
> {{{text}}} [⤴️]({{{highlightUrl}}}) {{#labels}} #{{name}} {{/labels}} ^{{{highlightID}}}
{{#note}}

{{{note}}}
{{/note}}

{{/highlights}}
{{/highlights.length}}
```

搞定了同步什么内容后，值得关注的还有存储到哪里。下面两个设置可以让你自定义文件、附件被存储到的位置。 

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/7015e02b62ca3ebc3b57534f063c8e05_MD5.png]]

基础的设置选项都完成后，点击左侧边栏的小图标或者命令面板中的 「Omnivore:sync」，就能一键同步所有 Omnivore 中剪藏、批注的内容了。

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/2b102bce79e304681ae26f3757616819_MD5.png]]

![[Omnivore/还不知道Omnivore可以全文同步到Obsidian吗？ - 知乎/attachments/d893957e831c64c166b9e98e37e640f4_MD5.png]]

Omnivore 配合它的浏览器插件，以及高颜值的阅读、批注界面，还有 RSS、Newsletter 的订阅功能，再搭配 Obsidian 同步插件，这过程非常丝滑。

稍后读、批注、存储……，在 Omnivore 中阅读的体验感觉非常好，推荐大家试用下这个清新、小众、免费、开源的好工具。

OK，就这样，其他的相关知识大家可以通过 Omnivore 的官方文档中进行学习与实践。 \[欢迎来到 Omnivore | Omnivore 使用文档\]([https://docs.omnivore.app/zh/](https://link.zhihu.com/?target=https%3A//docs.omnivore.app/zh/)) 

