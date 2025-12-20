---
url: https://www.bilibili.com/video/BV13w41197Jj/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2025-12-20T22:45:03+08:00
---
![开始使用ExcaliBrain-从一个空的Obsidian开始 Part 2|搬运 Zsolt's Visual Personal Knowledge Mana_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV13w41197Jj/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
1
00:00:00,000 --> 00:00:08,000
[由 vCaptions 生成] So welcome back, this is part two of the Excalibrain dialog mapping case study.

2
00:00:08,000 --> 00:00:20,000
And in today's video we're going to look at further configuring the relationships and the links in our Excalibrain.

3
00:00:20,000 --> 00:00:27,000
We're also going to be adding some new nodes and we're going to look at embedded nodes as well.

4
00:00:27,000 --> 00:00:39,000
So there's plenty to learn and then there's going to be still a part three where we're going to look at some additional things like weblinks and just polishing the whole thing up.

5
00:00:39,000 --> 00:00:50,000
So hopefully by the end of the third part you will have a good hands-on understanding of how to configure Excalibrain.

6
00:00:50,000 --> 00:01:02,000
So today let's continue from where we left off. So we have the remote work policy in the center and it defines the ontology for these two positions.

7
00:01:02,000 --> 00:01:08,000
But at the moment you don't yet see the position reflected on the links.

8
00:01:08,000 --> 00:01:16,000
So we're going to open plugin settings again and this time I'm going to scroll down.

9
00:01:16,000 --> 00:01:26,000
Before we scroll down. So what I want to show you is here at the top of the settings you have this section about ontology.

10
00:01:26,000 --> 00:01:32,000
I also have a bit of a description here that tries to explain what an ontology is.

11
00:01:32,000 --> 00:01:43,000
But here what I want to point out is we have the position. So this is what we added in part one to our ontology.

12
00:01:43,000 --> 00:01:53,000
We have position here as a next friend type. And then I'm going to scroll down all the way to styling.

13
00:01:53,000 --> 00:02:05,000
And I'm going to come to the link styles. Now link styles work very similar to how node styles work from the perspective of inheritance.

14
00:02:05,000 --> 00:02:17,000
So we have a base link style and then all of the different node types or link types that you have here are going to inherit this.

15
00:02:17,000 --> 00:02:26,000
And you can see that we have lots of different types. Many of these come prepackaged with Excalibrain.

16
00:02:26,000 --> 00:02:38,000
So you might want to delete these later on. I want to set up Excalibrain such that in every case the ontology is visible on the link.

17
00:02:38,000 --> 00:02:46,000
So I'm going to change the base link style for now. And I'm going to just scroll down here.

18
00:02:46,000 --> 00:02:56,000
And I'm going to turn on this link here to show label on link. And otherwise I think I'm going to leave it like this.

19
00:02:56,000 --> 00:03:07,000
If you want you can make the text slightly smaller or bigger. I like this relative sizing. That's why it comes with the base setup.

20
00:03:07,000 --> 00:03:24,000
So I'm going to leave it like this. Now additionally you might also want to display arrows. So here I'm going to say that I'm going to set the start arrow head to be an arrow.

21
00:03:24,000 --> 00:03:37,000
And then when we close our settings here. So now we did all of this setting for the base style. I didn't do any settings for the position type of style.

22
00:03:37,000 --> 00:03:51,000
We will see a different case a bit later on when I'm going to do settings. When I close settings then you will see that now the arrow is pointing from here to here.

23
00:03:51,000 --> 00:04:06,000
Because it is pointing to the start. Arrows can be a bit confusing. So depending on how you think about arrows and what's pointing from where to where.

24
00:04:06,000 --> 00:04:26,000
That depends on your internal dialog and logic. So you have couple of things that you can do around arrows. So first of all the base setting how ExcaliBrain comes is an inverse arrow direction.

25
00:04:26,000 --> 00:04:40,000
Which means that if I turn this off then automatically the arrows will change direction and then it will point the other way. What's considered a start and an end will be different.

26
00:04:40,000 --> 00:04:57,000
Or if I want to keep the inverse logic then I can come down here and instead of setting the start arrow head to be an arrow I can set the end arrow head to be an arrow.

27
00:04:57,000 --> 00:05:13,000
And when I do this then you can see that the end result is the same. So I have the remote work policy here. I have these arrows pointing to these two other nodes with the words position written on them.

28
00:05:13,000 --> 00:05:31,000
So now let's continue to build our graph but I'm going to do one thing here. So I'm going to first of all click on yes to remote work and here I'm going to turn on the embedded mode.

29
00:05:31,000 --> 00:05:48,000
When I turn on the embedded mode I can actually close this window so you will see here I have this button that synchronizes navigation between the leaf and the ExcaliBrain view.

30
00:05:48,000 --> 00:06:09,000
When I turn on the embedded mode then this connector got disconnected so if I now turn off embedded mode you will see that the connection is on and when I turn again to embedded mode then the connection is disconnected so I can close this.

31
00:06:09,000 --> 00:06:25,000
If you don't like this behavior again in ExcaliBrain settings you can scroll down all the way to behavior and you can click here to synchronize navigation with the in-bat toggle.

32
00:06:25,000 --> 00:06:44,000
If you turn this off then the two buttons will work independently from each other. Again you can play with this a bit later on to see the effects. I can show you the effects so right now if I click on remote work policy you can see nothing happens on the right hand side.

33
00:06:44,000 --> 00:07:01,000
If I turn this button on then when I click on remote work policy then that page on the left hand side changes as well. But now I'm going to turn that off I'm going to close this and actually I'm going to close this as well.

34
00:07:01,000 --> 00:07:17,000
So now we have the note here in the center. You will also notice, maybe you will maybe you not but I'm now going to highlight it to you so you will notice that this now has a light background.

35
00:07:17,000 --> 00:07:41,000
And that is because by default Excalibrain comes with the configuration that the style of the embedded node should follow the style of Excalibrain and now we're in a light Excalibrain drawing and therefore this is going to be light as well.

36
00:07:41,000 --> 00:07:56,000
So if I switch here to I turn ExcaliBrain off in a way so I'm going to turn off view mode then I can switch here to dark mode and you will see that this turns dark.

37
00:07:56,000 --> 00:08:14,000
The colors in this case look ugly so I don't recommend this. Now if you don't like this so if you would like to see dark colors here this is an example when you need to go to Excalibrain settings to do the changes.

38
00:08:14,000 --> 00:08:33,000
I'm going to click plugin settings and I'm going to make these changes. I need to click here on Excalibrain and then Excalibrain settings I need to scroll down to the display section and here at the top of the display section you will see that markdown

39
00:08:33,000 --> 00:08:47,000
and the inbats to match Excalibrain theme. If I turn this off then when I come back you will see that now the document follows a dark theme.

40
00:08:47,000 --> 00:09:03,000
If you have ExcaliBrain running then it might turn out that you need to close and open ExcaliBrain again for this change to take effect. That's normal but just letting you know that that's something that can happen.

41
00:09:03,000 --> 00:09:20,000
So now I'm going to again turn ExcaliBrain back on because you see now this is Excalibrain so this is now ExcaliBrain is not running. To turn ExcaliBrain back on I need to open the command palette and I just need to type in "brain normal"

42
00:09:20,000 --> 00:09:34,000
With this ExcaliBrain will recognize that this document is already open and it will turn to ExcaliBrain view mode. So let's continue editing our documents.

43
00:09:34,000 --> 00:09:53,000
So first of all I want to define here the supporting argument as an ontology as well. So again I have two options. I can either right click and click here add supporting argument to ExcaliBrain ontology.

44
00:09:53,000 --> 00:10:15,000
So that's a perfectly valid option. That's what we did in part one. This time around I'm going to press control or command P and I'm going to just type in "next" and here in the command palette I can choose ExcaliBrain add data view field to ontology as next.

45
00:10:15,000 --> 00:10:35,000
And when I click that then you will see in a second that ExcaliBrain will update and you will see that improves work-life balance moved from the bottom to the side and also now supporting argument as an ontology is displayed on this link.

46
00:10:35,000 --> 00:10:51,000
Now we are going to create improves work-life balance. The way to create the document is I'm going to hold down the shift key and click on the supporting argument and I'm going to create a markdown document.

47
00:10:51,000 --> 00:11:17,000
So with this now I have my markdown document right here and this is going to be a document type argument. So that's why here I have the argument tag at the top and it contains a question and this is the question how can remote work improve employee work-life balance.

48
00:11:17,000 --> 00:11:27,000
And to make this question again here right hand side or next type of ontology you already know the answer so what do I need to do.

49
00:11:27,000 --> 00:11:49,000
Yes you guessed it right I need to right click and I need to add question to ExcaliBrain ontology and I'm going to add this as a next friend and then ExcaliBrain will update and will add this question to the right hand side of my graph.

50
00:11:49,000 --> 00:12:09,000
Let's just do a final setting in today's session we're going to format the supporting ontology link because I think it would look nice if supporting arguments would be green and objecting arguments would be red.

51
00:12:09,000 --> 00:12:31,000
So how do I do that. I think you can also guess this by now you need to open ExcaliBrain settings and in ExcaliBrain settings we're going to scroll down to the very bottom and here we're going to select from the next relationships.

52
00:12:31,000 --> 00:12:51,000
We're going to select supporting argument. Yes so here's next supporting argument on the supporting argument. What I want to change is I want to change the color of this line I want this to be green.

53
00:12:51,000 --> 00:13:10,000
So a supporting argument should be green and I actually wanted to make this a bit thicker so I'm going to click this that I'm setting this property of the supporting argument link type different compared to the base link type.

54
00:13:10,000 --> 00:13:34,000
And I'm going to make this three thick so you can see now I have a nice thick green arrow right there and when I close settings, then you will see that here the remote work policy has this supporting argument with the work life balance here, and we can stop right here.

55
00:13:34,000 --> 00:13:47,000
Next time we're going to continue by adding some evidences as well that are going to be some web links and we'll see how you can embed links in here as well.

56
00:13:47,000 --> 00:14:06,000
Plus we're going to do some further formatting and settings. And hopefully, by the end of that, you'll have a pretty comfortable understanding of how ExcaliBrain works with the basics and then you can do your own settings as well.

57
00:14:06,000 --> 00:14:08,000
[由 vCaptions 生成]
