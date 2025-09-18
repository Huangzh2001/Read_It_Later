---
date: 2025-09-18T11:41:17+08:00
url: https://forum-zh.obsidian.md/t/topic/48679
status: readed
---
- 在@aoout佬的这个脚本基础上修改： [写了一个官方 clipper 的知乎回答剪藏模板（去除知乎 ai 链接，获取作者和发布时间） 88](https://forum-zh.obsidian.md/t/topic/42472)
- 主要增加两个功能点：
	- 使用CSS选择器，剔除掉所有无关的内容比如多少人赞同、更多回答。专注于回答的内容本身
	- 使用CSS选择器，获取回答的发布时间，添加进属性变量
	- 使用CSS选择器，获取回答的赞同数量，添加进属性变量
	- 使用replace，替换掉标题中偶尔出现的（X封私信）
- 以下是配置JSON代码：
```swift
{
  "schemaVersion": "0.1.0",
  "name": "知乎回答 (2)",
  "behavior": "create",
  "noteContentFormat": "{{selectorHtml:.QuestionAnswer-content .RichText|markdown}}",
  "properties": [
    {
      "name": "source",
      "value": "{{url}}",
      "type": "text"
    },
    {
      "name": "author",
      "value": "{{selector:.UserLink-link|slice:1,2}}",
      "type": "multitext"
    },
    {
      "name": "publicTime",
      "value": "{{selector:.QuestionAnswer-content .ContentItem-time span}}",
      "type": "text"
    },
    {
      "name": "agreeCount",
      "value": "{{selector:.RichContent-actions .VoteButton--up}}",
      "type": "text"
    }
  ],
  "triggers": [
    "https://www.zhihu.com/question/*/answer"
  ],
  "noteNameFormat": "{{title|replace:\" - 知乎\":\"\"|replace:\"/\\(\\d+\\s*封私信\\)/g\":\"\"}}",
  "path": "Clippings"
}
```
- 上面配置的导入方式：  
	新用户只能上传一幅图，自己找吧（
- 效果展示图，原文章 [地址 49](https://www.zhihu.com/question/633390831/answer/3321321435) ：  
	[[[Read It Later/attachments/a23760523a9499f244753e817f8798f7_MD5.png|Open: a23760523a9499f244753e817f8798f7_MD5.png]]
![[Read It Later/attachments/a23760523a9499f244753e817f8798f7_MD5.png]]](https://forum-zh.obsidian.md/uploads/default/original/3X/f/2/f2cbd6f9583b3c14816e4236353d17fd55e9e9a9.png "image")

- [obsidian web clipper 无法剪藏知乎专栏内容 10](https://forum-zh.obsidian.md/t/topic/52527/2)

- 参考资料：
	- [Variables - Obsidian Help 13](https://help.obsidian.md/web-clipper/variables)
	- [Filters - Obsidian Help 8](https://help.obsidian.md/web-clipper/filters)

4 个月后

可以看看web clipper的文档，value那里应该是类似于css选择器的那种语法，format格式化那里用的是正则语法.

这是我之前改的知乎专栏的写法（元数据都改成符合我的习惯的了），不知道现在还有没有用你可以试试看（之前跟楼主这个知乎回答一起用好像会分不清优先级，还没解决这个问题，手动选吧）：

```swift
{
    "schemaVersion": "0.1.0",
    "name": "知乎专栏",
    "behavior": "create",
    "noteContentFormat": "{{content}}",
    "properties": [
        {
            "name": "source",
            "value": "{{domain}}",
            "type": "text"
        },
        {
            "name": "source-url",
            "value": "{{url}}",
            "type": "text"
        },
        {
            "name": "source-title",
            "value": "{{title|replace:\\\" - 知乎\\\":\\\"\\\"|replace:\\\"/\\(\\d+\\s*封私信\\)/g\\\":\\\"\\\"}}",
            "type": "text"
        },
        {
            "name": "author",
            "value": "{{selector:.UserLink-link|slice:1,2}}",
            "type": "multitext"
        },
        {
            "name": "publicTime",
            "value": "{{selector:.Post-Row-Content .ContentItem-time}}",
            "type": "text"
        },
        {
            "name": "agreeCount",
            "value": "{{selector:.RichContent-actions .VoteButton--up}}",
            "type": "text"
        },
        {
            "name": "description",
            "value": "{{description}}",
            "type": "text"
        },
        {
            "name": "tags",
            "value": "clippings",
            "type": "multitext"
        },
        {
            "name": "year",
            "value": "{{date|date:\\\"YYYY\\\"}}",
            "type": "text"
        }
    ],
    "triggers": [
        "https://zhuanlan.zhihu.com/p/"
    ],
    "noteNameFormat": "{{title|replace:\" - 知乎\":\"\"|replace:\"/\\(\\d+\\s*封私信\\)/g\":\"\"}}",
    "path": "你的仓库地址"
}
```

  

### 想阅读更多？请浏览经验分享中的其他话题或查看最新话题。

[由 Discourse 提供技术支持](https://discourse.org/powered-by)