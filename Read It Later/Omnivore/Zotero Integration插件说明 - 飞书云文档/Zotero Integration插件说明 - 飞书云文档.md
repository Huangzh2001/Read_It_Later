---
id: 2c02d355-419e-47e9-8bc6-b0f9a9e887e7

url: https://f8lfn9zs2l.feishu.cn/docx/doxcno0YluQMgtsNTj3SsaOr9Sd
status:
---


tags:: 

# Zotero Integration插件说明 - 飞书云文档
#Omnivore

[Read on Omnivore](https://omnivore.app/me/zotero-integration-190b97e27f5)
[Read Original](https://f8lfn9zs2l.feishu.cn/docx/doxcno0YluQMgtsNTj3SsaOr9Sd)

​

{% for annotation in annotations %}​

{% if annotation.color == '#a28ae5' %}## {{annotation.annotatedText}}{{annotation.comment}}{% endif %}​

​

​

{% for annotation in annotations %}​

{% if annotation.color == '#a28ae5' %}## {{annotation.annotatedText}}{{annotation.comment}}{% endif %}​

{% if annotation.imageBaseName %}!\[\[{{annotation.imageBaseName}}\]\]{% endif %}​

​

由于\`data exploer\`内没有跳转链接的信息，我们需要通过不同的数据来生成我们需要的链接​

zotero自带的导出markdown笔记会包含跳转链接，我们以此观察跳转链接的组成形式为\[文本\](zotero://open-pdf/library/items/附件编号?页码&注释编号)​

所以我们可以在数据中找到拥有类似信息的内容加以删减、组合​

​

{% for annotation in annotations %}​

{% if annotation.color == '#a28ae5' %}## {{annotation.annotatedText}}{{annotation.comment}}{% endif %}​

{{pdfZoteroLink|replace("//select/", "//open-pdf/")|replace(")", "")}}?page={{annotation.page}}&annotation={{annotation.id}})​

​

或者采用（需attachments占位符内的第一个附件为注释的PDF）：​

​

{% for annotation in annotations %}​

{% if annotation.color == '#a28ae5' %}## {{annotation.annotatedText}}{{annotation.comment}}{% endif %}​

\[随便写啥\](zotero://open-pdf/library/items/{% for t in attachments %}{% if loop.first %}{{t.itemKey}}{% endif %}{% endfor %}?{{annotation.page}}&annotation={{annotation.id}})​

​

你可以选择将条目信息与注释的模板进行拆分、排列组合，进一步拓展插件的使用情境​

​

{% include "\[\[模板文件名\]\]" %}​

​

通过\`persist\`可以实现分节的效果，使得多次导入同一条目时之前的信息不会被覆盖​

