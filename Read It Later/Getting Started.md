---
date: 2026-07-17T20:00:12+08:00
url: https://github.com/dromse/obsidian-gamified-tasks/wiki/Getting-Started
status: readed
---
[跳转到内容](#start-of-content)   

   

Open menuHomepage (g then d) gGthen dD

1. [德罗姆斯](/dromse)
2. [黑曜石游戏化任务](/dromse/obsidian-gamified-tasks)
	Switch repository(alt shift r) altAlt shift⇧ rR

搜索类型/

Search or jump to…(forward slash) forward slash/

# Search code, repositories, users, issues, pull requests...

Search

Clear

0 suggestions.

[Search syntax tips](https://docs.github.com/search-github/github-code-search/understanding-github-code-search-syntax)

Give feedback

# Provide feedback

We read every piece of feedback, and take your input very seriously.

 Include my email address so I can be contacted

Cancel Submit feedback

# Saved searches

## Use saved searches to filter your results more quickly

Name  

Query 

To see all available qualifiers, see our [documentation](https://docs.github.com/search-github/github-code-search/understanding-github-code-search-syntax).

Cancel Create saved searchChat with Copilot

Create new...All issuesAll pull requestsAll repositoriesYou have no unread notifications(g then n) gGthen nN

![[Read It Later/attachments/aef39074106333faad7de2cf309de067_MD5.png]]Open user navigation menu

## 存储库导航

- [代码](/dromse/obsidian-gamified-tasks)
- [议题24 (24)](/dromse/obsidian-gamified-tasks/issues)
- [拉取请求1 (1)](/dromse/obsidian-gamified-tasks/pulls)
- [讨论](/dromse/obsidian-gamified-tasks/discussions)
- [行动](/dromse/obsidian-gamified-tasks/actions)
- [项目](/dromse/obsidian-gamified-tasks/projects)
- [维基](/dromse/obsidian-gamified-tasks/wiki)
- [安全性与质量](/dromse/obsidian-gamified-tasks/security)
- [见解](/dromse/obsidian-gamified-tasks/pulse)

More items

You signed in with another tab or window. Reload to refresh your session. You signed out in another tab or window. Reload to refresh your session. You switched accounts on another tab or window. Reload to refresh your session. Dismiss alert

# 入门指南

[Jump to bottom](#wiki-pages-box)

dromse 编辑了本页 2024年11月1日 ·[14次修订](/dromse/obsidian-gamified-tasks/wiki/Getting-Started/_history)

欢迎来到**游戏化任务**，尊敬用户！  
通过这个插件，你可以高效地管理各种手工艺标签的任务。让我们深入探讨如何通过实现插件提供的简化的Markdown任务和奖励系统来提升你的生产力。

## 如何创建任务？只需在你的保险库的任何备注中创建一个任务，就像下面的例子所示：

\- \[ \] markdown task

## 什么是手工标签以及如何使用它们？在插件里，用来创建你的任务。这里有一个你可以使用的示例：`#tags`

- **反驳**：（例如，|`#count/current/goal``#count/3``#count/1/4`)
- **复发**：（例如，|`#every/recurrence``#every/day``#every/week`)
- **难度**：（例如， | | |`#diff/difficulty``#diff/trivial``#diff/easy``#diff/medium``#diff/hard`)
- **绑定**：（例如， |`#bind/property``#bind/coding``#bind/pushUps`)
- **还有更多！**

## 什么是CompletedAt？为了显示完成日期，使用每日笔记链接：

- 维基链接：`✅ [[2024-03-13|2024-03-13 | 21:46]]`
- Markdown 链接：`✅ [2024-03-13 | 21:46](Everyday/2024-03-13.md)`

或者你可以在[设置里](https://github.com/dromse/obsidian-gamified-tasks/wiki/Settings#change-format-for-completedat-16)更改complatedAt标记

## 哪些状态可以使用？您可以使用以下状态：

- `- [ ] todo`\- 计划执行。
- `- [/] doing`\- 正在进行中。
- `- [x] done`\- 完成。
- `- [-] denied`\- 不感兴趣或其他原因。
- `- [?] delay`\- 正在进行中但暂停、审核中或委派。

\# Uncompleted task

\- \[ \] watch video about optimization #diff/easy

\# Task in progress

\- \[/\] watch video about optimization #diff/easy

\# Completed task

\- \[x\] watch video about optimization #diff/easy ✅ \[\[2024-03-13|2024-03-13 | 21:46\]\]

### 什么是难度，以及如何使用它？难度量化完成任务所需的努力，帮助优先排序工作并根据挑战追踪奖励。任务会被分配难度等级，决定其收益。

默认情况下，完成任务会奖励你以下金币：

- 琐碎 - 0.1
- 简单 - 1
- 中等 - 2.5
- 困难 - 5

或者你也可以在[设置](https://github.com/dromse/obsidian-gamified-tasks/wiki/Settings#difficulty)里自定义

## 如何使用反击？你可以用计数器来处理常见和重复任务。如果计数器有目标并达成了目标，任务自动完成。

### 计数器与其他标签之间的关系#### 其中`#bind`你可以把计数器绑定到每日注释中的前置物属性上。

注释

当你第二天点击计数器时，它开始计算新的数字。

- 前一天：`#count/3` + `#bind/coding` = `coding: 3`
- 第二天：`#count/5` + `#bind/coding` = `coding: 2`

#### 其中`#diff`如果任务有和，每增加一个计数器，你就会根据难度等级获得金币。`#diff``#count`

注释

如果你点击减少计数器，它会收回金币。

<!-- Difficulty usage \-->

\- \[/\] challange code everyday for 4 hours! #count/3/4 #diff/hard

<!-- In history file \-->

5 | challange code everyday for 4 hours! | 2024-03-13 21:46
5 | challange code everyday for 4 hours! | 2024-03-13 21:46
5 | challange code everyday for 4 hours! | 2024-03-13 21:46

<!-- If you click decrease one time \-->

-5 | challange code everyday for 4 hours! | 2024-03-13 21:50
5 | challange code everyday for 4 hours! | 2024-03-13 21:46
5 | challange code everyday for 4 hours! | 2024-03-13 21:46
5 | challange code everyday for 4 hours! | 2024-03-13 21:46

#### 其中`#every`在重复任务中，当你达到目标并到来展示目标的日子时，计数器会重置为零。

<!-- You're clicking on increase counter in UI \-->

\- \[/\] challange code everyday for 4 hours! #count/3/4 #every/day #diff/hard

<!-- It saves to history \-->

5 | challange code everyday for 4 hours! | 2024-03-13 21:46
5 | challange code everyday for 4 hours! | 2024-03-13 21:46
5 | challange code everyday for 4 hours! | 2024-03-13 21:46

<!-- Or without #diff \-->

0 | challange code everyday for 4 hours! | 2024-03-13 21:46
0 | challange code everyday for 4 hours! | 2024-03-13 21:46
0 | challange code everyday for 4 hours! | 2024-03-13 21:46

<!-- When you reach counter goal, counter set to completed \-->

\- \[x\] challange code everyday for 4 hours! #count/4/4 #every/day #diff/hard

<!-- Task resets to zeros and appears in UI when its time arrives \-->

\- \[ \] challange code everyday for 4 hours! #count/0/4 #every/day #diff/hard

## 什么是复发，以及如何使用它？对于复发，你需要使用标签。根据历史文件，一个重复任务再次出现。 这里有一次重复的持续时间列表（你可以用别的数字代替1）：`#every`

- 每天——一天、一天、两天等等。
- 每周——一周、1周、2周，等等。

如果任务历史中没有该标签，则通过平衡调整保存。`#diff``0`

<!-- Create recurring task \-->

\- \[ \] coding for 4 hours #every/day

<!-- Set in progress \-->

\- \[/\] coding for 4 hours #every/day

<!-- Complete task \-->

\- \[x\] coding for 4 hours #every/day

<!-- It saves in history and resets when the time arrives \-->

\- \[ \] coding for 4 hours #every/day

#### 简要列出它是如何运作的。- 你用标签创建任务;它会显示在界面上。`#every`
- 你完成了你的重复任务。
- 任务体被保存为历史。
- 任务计数器会重置为零，并在其时间到来时再次出现。

## 如何创建和购买奖励？- 你需要创建一个奖励文件。
- 你可以用赚到的金币购买奖励。
- 默认情况下，奖励文件是 ，但你可以在设置里更改。`rewards.md`
- 你需要在奖励文件中定义你的奖励。
- 奖励行的格式在奖励文件中。`reward name | price | description`
- 如果你想添加评论，可以使用符号，例如。`|``| my favorite rewards`
- 前置信息被忽略。

注释

Markdown 评论在奖励文件里无法使用。`<!-- comment -->`

| shows \`📺️ watch an episode\` for 1 coin
📺️ watch an episode

| shows \`🍦 Ice cream\` for 10 coins
🍦 Ice cream | 10

| shows \`🍬 candy\` with desc \`earn and eat it.\` for 1 coin
🍬 candy | earn and eat it.

| shows \`🌴 relax one day\` with desc \`you work hard you deserve it.\` for 1500 coins
🌴 relax one day | 1500 | you worked hard you deserve it.

## 插件中的历史是如何工作的？- 历史文件存储了你所有的收入和支出。
- 只有当任务具有 或 时，才被视为写入历史。`#diff``#every`
- 默认历史文件是 ，但你可以在设置里更改。`history.md`
- 默认情况下，你不需要对这个文件做任何操作。不过，如果你想纠正数据或偶尔作弊，欢迎......作弊者\*兄弟\*。
- 历史列的格式如下：`balance change | task body | date`

只有当以下情况才会保存到历史中：

- 该任务具有 。`#diff`
- 该任务具有 。`#every`
- 奖励被给予。

## 如何使用分组？想要轻松整理任务？只要加上标签！`#group`

注释

`#group`整个Vault都能用，所以你可以把不同笔记的任务分组到一个组里。

### Markdown 文件中的示例：\- \[ \] task 1 #group/test
\- \[ \] task 2 #group/test

### 插件界面的样子：![图片](https://private-user-images.githubusercontent.com/57846319/382134627-3f8ababf-2f8f-4a2c-be26-d5b4345e9012.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODQyODk1OTMsIm5iZiI6MTc4NDI4OTI5MywicGF0aCI6Ii81Nzg0NjMxOS8zODIxMzQ2MjctM2Y4YWJhYmYtMmY4Zi00YTJjLWJlMjYtZDViNDM0NWU5MDEyLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA3MTclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNzE3VDExNTQ1M1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPWY3ZDBkZDk1MjMzOTRkNjJmYzNiODlkNjRlNGU4MzZhOTdhOWU3MmI1Zjc4Mjg5MWI1ZDIyYjZkMWY1NGJkY2ImWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.dsFMSY57WPCCZy6c-wstlfjWab_s6mhRSpxpiaZQPQ0)

点击组后，你可以隐藏或显示任务：

![图片](https://private-user-images.githubusercontent.com/57846319/382134671-6211c434-cb6b-42ba-b083-78f2bb716eab.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3ODQyODk1OTMsIm5iZiI6MTc4NDI4OTI5MywicGF0aCI6Ii81Nzg0NjMxOS8zODIxMzQ2NzEtNjIxMWM0MzQtY2I2Yi00MmJhLWIwODMtNzhmMmJiNzE2ZWFiLnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNjA3MTclMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjYwNzE3VDExNTQ1M1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTQ1M2QwNTg1ZmM4OWZjN2EzZjFjODkxOTBlNjk1MTY2MDY3NWZiNmY1ZGJkODI4YjBkNTRhMmNjNWRiZWI0ZWQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JnJlc3BvbnNlLWNvbnRlbnQtdHlwZT1pbWFnZSUyRnBuZyJ9.lBs5X5nZgua7XB02wwKQUsCFq76Cu6Phu9CW2F-Ev7Q)

默认情况下，所有组在启动时都会打开，你可以在[设置里](https://github.com/dromse/obsidian-gamified-tasks/wiki/Settings#show-groups-collapsed-by-default-18)更改这个行为

## Wiki pages 页面5

- Loading[
	首页
	](/dromse/obsidian-gamified-tasks/wiki)
	### Uh oh!
	There was an error while loading. Please reload this page.
- Loading[
	缩写
	](/dromse/obsidian-gamified-tasks/wiki/Abbreviations)
	### Uh oh!
	There was an error while loading. Please reload this page.
- Loading[
	条件
	](/dromse/obsidian-gamified-tasks/wiki/Conditions)
	### Uh oh!
	There was an error while loading. Please reload this page.
- Loading[
	入门指南
	](/dromse/obsidian-gamified-tasks/wiki/Getting-Started)
	- [如何创建任务？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#how-to-create-task)
	- [什么是手工标签以及如何使用它们？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#what-are-craft-tags-and-how-to-use-them)
	- [什么是CompletedAt？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#what-is-completedat)
	- [哪些状态可以使用？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#which-statuses-are-available-for-use)
	- [什么是难度，以及如何使用它？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#what-is-difficulty-and-how-to-use-it)
	- [如何使用反击？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#how-to-use-counter)
	- [计数器与其他标签之间的关系](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#relations-between-counter-and-other-tags)
	- [与 #bind](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#with-bind)
	- [和 #diff](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#with-diff)
	- [与 #every](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#with-every)
	- [什么是复发，以及如何使用它？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#what-is-recurrence-and-how-to-use-it)
	- [简要列出它是如何运作的。](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#short-list-how-it-works)
	- [如何创建和购买奖励？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#how-to-create-and-buy-rewards)
	- [插件中的历史是如何工作的？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#how-does-history-work-in-the-plugin)
	- [如何使用分组？](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#how-to-use-groups)
	- [Markdown 文件中的示例：](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#example-in-a-markdown-file)
	- [插件界面的样子：](/dromse/obsidian-gamified-tasks/wiki/Getting-Started#how-it-looks-in-the-plugin-ui)
- Loading[
	背景设定
	](/dromse/obsidian-gamified-tasks/wiki/Settings)
	### Uh oh!
	There was an error while loading. Please reload this page.

### 本地克隆这个维基

## 页脚© 2026年GitHub公司

### 页脚导航

- [条款](https://docs.github.com/site-policy/github-terms/github-terms-of-service)
- [隐私](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement)
- [安全性](https://github.com/security)
- [现状](https://www.githubstatus.com/)
- [社区](https://github.community/)
- [文档](https://docs.github.com/)
- [联系方式](https://support.github.com?tags=dotcom-footer)
- 管理 Cookie
- 不要分享我的个人信息

You can’t perform that action at this time.