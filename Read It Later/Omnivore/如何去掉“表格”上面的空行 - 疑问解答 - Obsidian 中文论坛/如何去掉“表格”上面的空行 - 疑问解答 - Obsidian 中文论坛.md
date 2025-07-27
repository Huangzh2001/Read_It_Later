---
id: 9ed846f2-5564-4664-aeee-39947d6526ca

url: https://forum-zh.obsidian.md/t/topic/31496
status:
---


tags::  #Readed 

# 如何去掉“表格”上面的空行 - 疑问解答 - Obsidian 中文论坛
#Omnivore

[Read on Omnivore](https://omnivore.app/me/obsidian-190e4f4a6bb)
[Read Original](https://forum-zh.obsidian.md/t/topic/31496)

新版Obsidian在表格的上面增加了一行空行，请问有什么方法可以去掉 ？

* [最后回复](https://forum-zh.obsidian.md/t/topic/31496/8)  
[](https://forum-zh.obsidian.md/t/topic/31496/8)3 月 17 日
* 471  
#### 浏览量
* 4  
#### 用户
* 2  
#### 赞

用css去掉前一行的行高，用 .cm-line 和 :has() 即可

.markdown-sourceview.is-live-preview .cm-line:has(+.table-wrapper) {  
line-height: 0;  
}  
类似这样

谢谢你的回复，我按你说的增加了这个css，但没有任何变化，表格上面的空行无法去掉

这个css只是一个一个举例，不是真的实现。用这个吧

.markdown-source-view.is-live-preview .cm-line:has(+ .cm-table-widget) {  
line-height: 0;  
}

.markdown-source-view.is-live-preview .cm-active.cm-line:has(+ .cm-table-widget) {  
line-height: var(–line-height-normal);  
}

这个css只是一个一个举例，不是真的实现。用这个吧

.markdown-source-view.is-live-preview .cm-line:has(+ .cm-table-widget) {  
line-height: 0;  
}

.markdown-source-view.is-live-preview .cm-active.cm-line:has(+ .cm-table-widget) {  
line-height: var(–line-height-normal);  
}

我刚发现，新版的Obsidian在表格的下方也增加了一个空行  
能否再发一段 “去掉表格下方空行”的代码 ？

感谢你的代码，解决了困扰我的问题，在表格上打字也不会出现跟多的行数 

我刚发现，新版的Obsidian在表格的下方也增加了一个空行  
能否再发一段 “去掉表格下方空行”的代码 ？

感谢你的代码，解决了困扰我的问题，在表格上打字也不会出现跟多的行数 

###  想阅读更多？请浏览[疑问解答](https://forum-zh.obsidian.md/c/6-category/6)中的其他话题或[查看最新话题](https://forum-zh.obsidian.md/latest)。

