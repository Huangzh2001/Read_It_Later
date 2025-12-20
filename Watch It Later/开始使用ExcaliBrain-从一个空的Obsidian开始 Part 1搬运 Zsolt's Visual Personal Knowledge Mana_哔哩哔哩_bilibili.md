---
url: https://www.bilibili.com/video/BV1xu411J7XC/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2025-12-20T22:45:34+08:00
---
![开始使用ExcaliBrain-从一个空的Obsidian开始 Part 1|搬运 Zsolt's Visual Personal Knowledge Mana_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1xu411J7XC/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
1
00:00:00,720 --> 00:00:02,439
[由 vCaptions 生成] Hey everyone joel here

2
00:00:02,439 --> 00:00:05,339
Collibrain is an obsidian plugin that

3
00:00:05,339 --> 00:00:10,619
I've built to visualize connections described in your markdown documents

4
00:00:10,619 --> 00:00:12,679
In a structured graph

5
00:00:13,359 --> 00:00:17,919
I realized that setting up collibrain can be a bit intimidating

6
00:00:17,919 --> 00:00:21,719
And there are many settings that you need to get your head around

7
00:00:21,719 --> 00:00:25,780
So i thought i would create this video that will take you through

8
00:00:25,780 --> 00:00:29,059
From a completely empty vault

9
00:00:29,059 --> 00:00:32,969
All the way to having something that looks like this

10
00:00:32,969 --> 00:00:35,030
Take you through a use case

11
00:00:35,030 --> 00:00:39,890
The use case is going to be a relatively silly simple example

12
00:00:39,890 --> 00:00:42,649
It's going to be an argument mapping

13
00:00:42,649 --> 00:00:45,469
Or rather a dialogue mapping example

14
00:00:45,950 --> 00:00:53,500
Exploring the pros and cons of setting up a remote work policy at a company

15
00:00:53,859 --> 00:00:55,859
So to give you a bit of frame

16
00:00:55,859 --> 00:00:58,820
I think it's important to understand the framework that

17
00:00:58,820 --> 00:01:00,649
We're going to be applying here

18
00:01:00,649 --> 00:01:06,090
I'm going to be using the issue based information systems framework

19
00:01:06,090 --> 00:01:09,620
Which is a dialogue mapping approach

20
00:01:09,620 --> 00:01:12,959
And it consists of a couple of different components

21
00:01:12,959 --> 00:01:18,299
It consists of issues that are typically phrased as questions

22
00:01:18,299 --> 00:01:21,340
And this is how this is a dialogue mapping

23
00:01:21,340 --> 00:01:22,899
Because it

24
00:01:26,728 --> 00:01:32,509
And then there are positions which are positions in response to these issues

25
00:01:32,509 --> 00:01:40,049
And then there are supporting and objecting arguments that support or object the positions

26
00:01:40,049 --> 00:01:45,250
And finally there are evidences that you can attach to various nodes

27
00:01:45,250 --> 00:01:48,789
As well as in the end you reach a conclusion

28
00:01:48,789 --> 00:01:52,159
Which you can call a decision now

29
00:01:52,159 --> 00:01:54,879
If you're interested in learning more about ibis

30
00:01:54,879 --> 00:01:59,019
I have a video on it with another case study

31
00:01:59,060 --> 00:02:05,950
And also you might want to take a look at the visualizing argumentation book

32
00:02:05,950 --> 00:02:08,110
Which is the source of this

33
00:02:08,110 --> 00:02:09,060
It

34
00:02:09,060 --> 00:02:10,860
It's a bit of an old book

35
00:02:10,860 --> 00:02:12,139
So it might be hard to find

36
00:02:12,139 --> 00:02:15,479
But anyway this is the book that you can look for

37
00:02:15,479 --> 00:02:19,879
And that discusses the topic of argument mapping

38
00:02:19,879 --> 00:02:22,259
You using ibis

39
00:02:22,259 --> 00:02:23,520
So let's dive in

40
00:02:23,520 --> 00:02:29,389
We're going to start by creating a brand new empty obsidian vault

41
00:02:29,389 --> 00:02:31,969
I'm going to click here create

42
00:02:31,969 --> 00:02:35,449
And i'm going to type in the name x colly brain

43
00:02:35,449 --> 00:02:38,870
And we're going to pick a location for this

44
00:02:38,870 --> 00:02:41,590
Which is this right here

45
00:02:41,590 --> 00:02:44,189
And then i'm going to click create

46
00:02:44,189 --> 00:02:51,239
And with this we have a new vault now to get ollibrain working

47
00:02:51,239 --> 00:02:54,199
You need to install three different plugins

48
00:02:54,199 --> 00:02:57,199
So we'll go ahead and start with that

49
00:02:57,199 --> 00:03:00,569
So i'm going to click here on obsidian settings

50
00:03:00,569 --> 00:03:04,389
And here i'm going to click on community plugins

51
00:03:04,389 --> 00:03:06,270
And in community plugins

52
00:03:06,270 --> 00:03:08,129
The first time you start obsidian

53
00:03:08,129 --> 00:03:15,020
You need to accept the risks and consequences of turning on community plugins

54
00:03:15,020 --> 00:03:17,110
So i'm going to do that

55
00:03:17,110 --> 00:03:21,639
And i'm going to browse for the different plugins that we need

56
00:03:21,639 --> 00:03:25,599
So first of all you need to install x call it raw

57
00:03:25,599 --> 00:03:30,409
Because x call it brain is built on top of x colored raw

58
00:03:30,409 --> 00:03:33,879
Which is another plug in that i've developed here

59
00:03:33,879 --> 00:03:35,219
After you've installed it

60
00:03:35,219 --> 00:03:37,580
You need to click enable

61
00:03:38,459 --> 00:03:40,959
And you can just close this message

62
00:03:40,959 --> 00:03:44,799
Then next we are going to click on data view

63
00:03:44,799 --> 00:03:48,030
And i'm going to install data view as well

64
00:03:48,030 --> 00:03:53,870
Collibrain uses data view to extract the structure of documents

65
00:03:53,870 --> 00:03:58,409
So data view is an essential component for ex collibrain to work

66
00:03:58,409 --> 00:04:02,490
And finally we're going to search for call it brain

67
00:04:02,490 --> 00:04:05,389
And i'm going to click install as well

68
00:04:05,389 --> 00:04:07,370
And once it's installed

69
00:04:07,370 --> 00:04:11,669
I'm going to click enable on this plugin as well

70
00:04:11,669 --> 00:04:15,979
So with this we have the basic plugins installed

71
00:04:15,979 --> 00:04:19,160
And we can take a look at our plug in

72
00:04:19,160 --> 00:04:21,100
So you can see that we have data view

73
00:04:21,100 --> 00:04:22,699
We x call it brain

74
00:04:22,699 --> 00:04:25,019
And we have x call it draw now

75
00:04:25,019 --> 00:04:26,800
It's important to keep in mind

76
00:04:26,800 --> 00:04:31,800
That ex coli brain builds on top of x call draw

77
00:04:31,860 --> 00:04:37,259
One consequence of this is some of the settings in x collibrain

78
00:04:37,259 --> 00:04:40,939
Will depend on settings in ex collidraw

79
00:04:40,939 --> 00:04:44,259
I'll show you one example when we get to that point

80
00:04:44,259 --> 00:04:47,220
But this is something good to keep in mind

81
00:04:47,220 --> 00:04:52,089
And maybe this is also a bit difficult at first to understand

82
00:04:52,089 --> 00:04:56,209
What is coming from x color draw and what's coming from x color brain

83
00:04:56,209 --> 00:04:59,620
But hopefully you'll get the hang of it

84
00:04:59,620 --> 00:05:01,000
So to get us started

85
00:05:01,000 --> 00:05:04,740
I'm going to create a first document in the vault

86
00:05:04,740 --> 00:05:08,959
I'm just simply going to click here to create a new node

87
00:05:08,959 --> 00:05:11,339
And i'm going to title this note

88
00:05:11,339 --> 00:05:13,180
Remote of our policy

89
00:05:13,180 --> 00:05:19,319
This is going to be the central question in our graph

90
00:05:19,319 --> 00:05:21,500
In our dialogue map

91
00:05:21,538 --> 00:05:24,858
And i'm going to just close this one right here

92
00:05:24,858 --> 00:05:27,819
Once i've created this document

93
00:05:27,819 --> 00:05:30,639
I can now open a collibrain

94
00:05:30,639 --> 00:05:33,560
It's very easy to start the collibrain

95
00:05:33,560 --> 00:05:35,959
You need to open the command palette

96
00:05:35,959 --> 00:05:37,920
I'm going to press ctrl p

97
00:05:37,920 --> 00:05:39,000
If you're on a mac

98
00:05:39,000 --> 00:05:43,019
This is command p and i'm going to type in brain

99
00:05:43,019 --> 00:05:45,980
And i'm going to choose brain normal

100
00:05:45,980 --> 00:05:51,689
Now brain normal opens in a new window within your workspace

101
00:05:51,689 --> 00:05:54,620
And a brain pop out

102
00:05:54,620 --> 00:05:56,920
Will open in a pop out window

103
00:05:56,920 --> 00:06:00,779
But for now we're going to be happy with brain normal

104
00:06:00,779 --> 00:06:03,639
So when i click enter

105
00:06:03,639 --> 00:06:07,160
Then you can see that now escalate brain is open

106
00:06:07,160 --> 00:06:12,189
And of course right now we have a single document in the vault

107
00:06:12,189 --> 00:06:15,168
And that is reflected here

108
00:06:15,168 --> 00:06:22,079
Now you might also notice that here i have a second document that was created ex cola brain

109
00:06:22,079 --> 00:06:24,180
You don't need to worry about it

110
00:06:24,180 --> 00:06:29,800
This is the file that's underneath the brain file

111
00:06:29,800 --> 00:06:32,259
Or view that you have here

112
00:06:32,259 --> 00:06:34,199
You have not to worry about it

113
00:06:34,199 --> 00:06:38,240
But that's a file that's always going to be overwritten by

114
00:06:38,240 --> 00:06:39,240
Ex coli brain

115
00:06:39,240 --> 00:06:42,699
So i recommend not editing that file

116
00:06:42,920 --> 00:06:46,350
So now that we have this node here

117
00:06:46,350 --> 00:06:50,149
We need to start to add children and items to it

118
00:06:50,149 --> 00:06:52,129
To help us move quicker

119
00:06:52,129 --> 00:06:54,189
I'm going to use my cheat sheets

120
00:06:54,189 --> 00:06:55,548
I'm going to now

121
00:06:58,220 --> 00:07:00,040
Question the initial question

122
00:07:00,040 --> 00:07:04,230
So should the company implement a remote work policy

123
00:07:04,230 --> 00:07:07,899
And i'm going to add the two positions here

124
00:07:08,480 --> 00:07:11,800
One position is a yes to a remote work

125
00:07:11,800 --> 00:07:15,920
The other position is a no to remote work

126
00:07:16,038 --> 00:07:17,459
And you can see that

127
00:07:17,459 --> 00:07:18,639
As i did this

128
00:07:18,639 --> 00:07:24,249
The graph on the right hand side started to develop now

129
00:07:24,249 --> 00:07:26,720
If i click on yes

130
00:07:26,779 --> 00:07:30,459
The company should implement a remote work policy

131
00:07:30,459 --> 00:07:31,379
Just to show you

132
00:07:31,379 --> 00:07:33,730
So this here is a wiki link

133
00:07:33,730 --> 00:07:36,110
So i have the first part of the link

134
00:07:36,110 --> 00:07:37,310
Is the file name

135
00:07:37,310 --> 00:07:39,870
And then after the pipe character

136
00:07:39,870 --> 00:07:42,860
I have the alias for this file

137
00:07:42,860 --> 00:07:45,019
What's being displayed right there

138
00:07:45,019 --> 00:07:47,240
If i click on this link

139
00:07:47,240 --> 00:07:50,250
Then that creates this new file

140
00:07:50,250 --> 00:07:52,420
So this is now created

141
00:07:52,420 --> 00:07:55,300
This is yes to remote work policy

142
00:07:55,300 --> 00:07:57,500
You can see on the right hand side

143
00:07:57,500 --> 00:07:59,240
The diagram has changed

144
00:07:59,240 --> 00:07:59,920
So yes

145
00:07:59,920 --> 00:08:03,149
Do remote work is now in the center

146
00:08:03,149 --> 00:08:06,980
It has a parent which is remote or policy

147
00:08:06,980 --> 00:08:10,779
And it also has a distant relation

148
00:08:10,779 --> 00:08:14,019
Which is this other position here

149
00:08:14,019 --> 00:08:17,480
Which is the node to remote work now

150
00:08:17,480 --> 00:08:23,560
If i'm just going to copy this material over here as well to fill this in

151
00:08:23,560 --> 00:08:28,750
So this is going to be a position and notice what i'm doing here

152
00:08:28,750 --> 00:08:30,369
So at the top

153
00:08:30,369 --> 00:08:32,649
I'm adding this tag

154
00:08:32,649 --> 00:08:33,969
So i'm going to zoom in

155
00:08:33,969 --> 00:08:35,249
So you can better see

156
00:08:35,249 --> 00:08:37,048
So i have a tag here

157
00:08:37,048 --> 00:08:39,480
Which is called position

158
00:08:39,480 --> 00:08:41,299
And here as well

159
00:08:41,299 --> 00:08:44,039
When i clicked the remote work policy

160
00:08:44,039 --> 00:08:49,240
You can see that this had a tag question at the top

161
00:08:50,279 --> 00:08:53,779
We are going to use these to format the nodes

162
00:08:53,779 --> 00:08:56,919
Also what you will notice is yes

163
00:08:56,919 --> 00:09:01,578
To remote work now looks different compared to node to remote work

164
00:09:01,700 --> 00:09:05,259
The difference is that this node has been created

165
00:09:05,259 --> 00:09:08,659
And this doesn't yet exist in the world

166
00:09:08,960 --> 00:09:12,460
And x cola brain can format it differently

167
00:09:12,460 --> 00:09:14,859
This is actually a super good feature

168
00:09:15,460 --> 00:09:24,659
Because this way you can also see connections between nodes that are not yet in your world

169
00:09:26,159 --> 00:09:32,299
But you also notice that this now looks different compared to the example i showed in the beginning

170
00:09:32,299 --> 00:09:39,590
First of all you see the dashed line and the items are under the central item

171
00:09:39,590 --> 00:09:41,100
Not to the right

172
00:09:41,100 --> 00:09:45,179
And also the coloring and the look and feel is different

173
00:09:45,179 --> 00:09:47,779
So what do we do about this

174
00:09:47,779 --> 00:09:50,220
We're going to come to plug in settings

175
00:09:50,220 --> 00:09:54,980
And we are going to start to play a bit with x alibrain settings

176
00:09:54,980 --> 00:09:58,320
So you can see how you can format this

177
00:09:58,320 --> 00:10:01,799
So first of all i'm going to click here on settings

178
00:10:01,799 --> 00:10:05,740
And i'm going to click here on x colly brain

179
00:10:06,539 --> 00:10:08,200
You have lots of settings here

180
00:10:08,200 --> 00:10:09,559
For the time being

181
00:10:10,080 --> 00:10:12,039
We are not going to touch these

182
00:10:12,039 --> 00:10:16,519
I'm going to come all the way down to styling

183
00:10:16,519 --> 00:10:17,500
And first of all

184
00:10:17,500 --> 00:10:20,539
We're going to add these two tags that we've created

185
00:10:20,539 --> 00:10:25,979
So one was the question and the other one was the position

186
00:10:26,879 --> 00:10:30,580
So we need to manually add the tags

187
00:10:30,580 --> 00:10:34,289
That we want to use for formatting purposes

188
00:10:34,289 --> 00:10:37,039
And once i've added the tax here

189
00:10:37,039 --> 00:10:40,458
Then i can choose here in this

190
00:10:40,580 --> 00:10:43,919
And i need to add a comma in between

191
00:10:44,039 --> 00:10:45,299
So it's question

192
00:10:45,299 --> 00:10:47,450
Comma position

193
00:10:47,450 --> 00:10:49,190
And once i've added them

194
00:10:49,190 --> 00:10:51,490
Then the items will appear here

195
00:10:51,490 --> 00:10:55,839
So if you noticed when i don't have a comma

196
00:10:55,839 --> 00:10:59,239
Then these two items appear in a single row

197
00:10:59,239 --> 00:11:00,440
That's not good

198
00:11:00,440 --> 00:11:04,019
You need to add your comma right here

199
00:11:04,220 --> 00:11:06,600
And once i have the comma there

200
00:11:06,600 --> 00:11:11,479
Then i can start to format this for the question

201
00:11:11,679 --> 00:11:16,799
All i want is a question mark at the beginning of the question

202
00:11:16,799 --> 00:11:19,318
So the way this works

203
00:11:19,460 --> 00:11:23,960
And this might be a bit hard to comprehend

204
00:11:23,960 --> 00:11:30,679
At the beginning is everything is inherited from the bass note style

205
00:11:30,679 --> 00:11:35,860
So the bass note style you can see all the settings of the base node style

206
00:11:35,860 --> 00:11:37,779
Lots of different settings

207
00:11:38,340 --> 00:11:40,799
If i create a new node type

208
00:11:40,799 --> 00:11:41,820
For example

209
00:11:41,820 --> 00:11:44,210
Position by default

210
00:11:44,210 --> 00:11:46,549
Everything is inherited

211
00:11:46,549 --> 00:11:48,389
If i turn this switch

212
00:11:48,389 --> 00:11:51,559
Then i'm only going to see the

213
00:11:53,850 --> 00:11:56,070
Items which in this case is nothing

214
00:11:56,070 --> 00:11:58,419
Because this is already the next section

215
00:11:58,419 --> 00:12:00,200
So to customize the position

216
00:12:00,200 --> 00:12:05,698
I first need to flip the switch to customize the prefix

217
00:12:05,899 --> 00:12:08,899
So i'm going to flip the switch with this

218
00:12:08,899 --> 00:12:10,419
I tell x call a brain

219
00:12:10,419 --> 00:12:16,259
That the position will look exactly the same as the bass note style

220
00:12:16,820 --> 00:12:20,220
Except that the prefix is going to be different

221
00:12:20,220 --> 00:12:23,929
And i'm going to bring up the emoji toolbar

222
00:12:23,929 --> 00:12:26,850
And i'm going to choose this light bulb

223
00:12:26,850 --> 00:12:27,929
So for me

224
00:12:27,929 --> 00:12:32,210
A position is represented by an idea

225
00:12:32,210 --> 00:12:39,019
And i also want to change the background color of the idea node

226
00:12:39,019 --> 00:12:44,099
So i'm going to turn the background color switch on as well

227
00:12:44,220 --> 00:12:46,419
I'm going to change the opacity

228
00:12:46,419 --> 00:12:50,980
So this is the transparency of the node to a hundred percent

229
00:12:50,980 --> 00:12:54,559
And i'm going to choose a different color

230
00:12:54,559 --> 00:12:59,940
I'm going to try to choose a nice dark yellow color

231
00:12:59,940 --> 00:13:01,559
Somewhere like this

232
00:13:02,559 --> 00:13:05,340
I'm happy with this color

233
00:13:05,340 --> 00:13:08,438
Maybe a bit bit yellow or like that

234
00:13:08,940 --> 00:13:14,240
So there you can see how the new format or new node looks like this

235
00:13:14,240 --> 00:13:16,159
Actually doesn't look that very good

236
00:13:16,159 --> 00:13:19,559
So we're going to look for a darker yellow

237
00:13:19,559 --> 00:13:23,399
Maybe maybe even yellow and ah

238
00:13:23,399 --> 00:13:24,879
This is going to be good

239
00:13:24,879 --> 00:13:29,639
So i'm going to choose this orange red color

240
00:13:30,059 --> 00:13:32,980
So with this i formatted the position

241
00:13:32,980 --> 00:13:37,210
And then i'm also going to format the question node

242
00:13:37,210 --> 00:13:38,970
And for the question node

243
00:13:38,970 --> 00:13:41,149
I'm only going to add a prefix

244
00:13:41,149 --> 00:13:46,599
And the prefix is going to be this question mark like this

245
00:13:47,960 --> 00:13:50,919
And now when i close settings

246
00:13:50,919 --> 00:13:59,299
Then what you will see is the formatting for the remote work policy

247
00:13:59,299 --> 00:14:01,610
Is now indeed a question

248
00:14:01,610 --> 00:14:06,309
I wonder why we have an issue with the position

249
00:14:06,309 --> 00:14:09,450
So this is spelled correctly

250
00:14:09,450 --> 00:14:14,820
Maybe i have an issue here with the letter case

251
00:14:16,419 --> 00:14:16,879
Oh no

252
00:14:16,879 --> 00:14:18,419
It's with the spelling

253
00:14:20,120 --> 00:14:23,320
So now i corrected the spelling

254
00:14:23,320 --> 00:14:24,470
Unfortunately

255
00:14:24,470 --> 00:14:26,549
After i correct the spelling

256
00:14:26,549 --> 00:14:29,629
I need to redo my settings

257
00:14:29,629 --> 00:14:33,659
So the position is going to be this light bulb

258
00:14:33,659 --> 00:14:36,839
And i'm going to set the color to

259
00:14:38,179 --> 00:14:42,679
Again this orange red like actually

260
00:14:42,679 --> 00:14:47,379
I'm going to set it like this to this orange red

261
00:14:49,919 --> 00:14:51,179
Like this

262
00:14:51,240 --> 00:14:52,879
And now when i close this

263
00:14:52,879 --> 00:14:57,820
Then you can see that now we have the formatting like this

264
00:14:57,820 --> 00:14:58,399
Yeah

265
00:14:58,399 --> 00:15:01,450
So this is not an ideal formatting

266
00:15:01,450 --> 00:15:07,009
Maybe we should change the font color of the position item as well

267
00:15:07,009 --> 00:15:11,049
So here i can again scroll down to styling

268
00:15:11,049 --> 00:15:13,009
I can choose a position

269
00:15:13,009 --> 00:15:16,799
And i also want to change the text color

270
00:15:16,799 --> 00:15:19,359
And i wanted the text color to be

271
00:15:20,139 --> 00:15:24,919
And i think with that now the position looks much nicer

272
00:15:24,919 --> 00:15:31,460
Now you can also notice that no to remote work is still not yellow

273
00:15:31,460 --> 00:15:33,519
And that's because there is no document

274
00:15:33,519 --> 00:15:35,019
So there's no tag

275
00:15:35,019 --> 00:15:36,580
And if there's no tag

276
00:15:36,580 --> 00:15:38,519
Then there's no style

277
00:15:39,740 --> 00:15:41,539
But we can do something about it

278
00:15:41,539 --> 00:15:45,169
So we are going to create this document right here

279
00:15:45,169 --> 00:15:48,690
What i'm going to do is here in x colbrain

280
00:15:48,690 --> 00:15:52,568
If i hold down the shift key and click on a node

281
00:15:52,568 --> 00:15:54,849
Then i'm prompted with this question

282
00:15:54,849 --> 00:16:00,009
If i want to create a new markdown document or a new collateral file

283
00:16:00,009 --> 00:16:04,090
So i'm going to say i want to create a new markdown document

284
00:16:04,090 --> 00:16:09,139
So this not to remote work file was now created

285
00:16:09,139 --> 00:16:14,568
And i'm going to just copy in the contents of noto remote work

286
00:16:14,568 --> 00:16:16,908
So we're going to have the position

287
00:16:16,908 --> 00:16:22,009
Then the title of the question and then the supporting argument

288
00:16:22,139 --> 00:16:26,620
And now you can see that at least we got the colors right

289
00:16:26,620 --> 00:16:29,600
But the locations are still not good

290
00:16:29,600 --> 00:16:35,299
I mean the positions are under the central question

291
00:16:35,299 --> 00:16:38,519
And i want them to be on the right hand side

292
00:16:38,519 --> 00:16:41,818
So we still need to do some things

293
00:16:41,818 --> 00:16:44,418
So you can see here in this row

294
00:16:44,418 --> 00:16:46,879
That i have something that's going on here

295
00:16:46,879 --> 00:16:49,759
So i have here position

296
00:16:49,759 --> 00:16:53,919
And i have double double columns here

297
00:16:53,919 --> 00:16:56,769
And then i have the name of the file

298
00:16:56,769 --> 00:17:05,039
This right here this position double colon is called an data of view field

299
00:17:05,039 --> 00:17:12,549
And coli brain is using these fields to understand the ontology

300
00:17:12,549 --> 00:17:16,849
Which is the description of connections between items

301
00:17:16,849 --> 00:17:21,900
So this is what describes the relationship between this document

302
00:17:21,900 --> 00:17:25,429
The question and this item here

303
00:17:25,429 --> 00:17:26,848
Which is a position

304
00:17:26,848 --> 00:17:29,079
So to make

305
00:17:35,339 --> 00:17:36,599
You have two options

306
00:17:36,599 --> 00:17:40,099
So first of all i'm going to just right click here

307
00:17:40,099 --> 00:17:41,319
So in this line

308
00:17:41,319 --> 00:17:42,809
If i right click

309
00:17:42,809 --> 00:17:47,880
Then you will see this menu item in the context menu

310
00:17:47,880 --> 00:17:51,740
Add position to escala brain ontology

311
00:17:51,740 --> 00:17:53,130
When i click this

312
00:17:53,130 --> 00:18:00,990
Then i can choose what sort of relationship this is going to have with the central node now

313
00:18:00,990 --> 00:18:06,398
I don't want to go into the details of these different type of nodes

314
00:18:07,039 --> 00:18:09,240
Later on we can touch on it

315
00:18:09,240 --> 00:18:13,378
And also i have other videos that will explain for now

316
00:18:14,119 --> 00:18:18,588
I just believe me that this should be a next friend

317
00:18:18,588 --> 00:18:22,108
The nature of a next and previous friend is

318
00:18:22,108 --> 00:18:25,509
It's a relative position compared to the center

319
00:18:25,509 --> 00:18:32,299
Because the next is to the right of the central node

320
00:18:32,299 --> 00:18:33,720
When it's still next

321
00:18:33,720 --> 00:18:37,619
But when they move and it becomes it comes to the left

322
00:18:37,619 --> 00:18:40,220
Because then for the next node

323
00:18:40,220 --> 00:18:41,720
It's the previous

324
00:18:42,400 --> 00:18:45,180
While the left side and right side

325
00:18:45,180 --> 00:18:49,589
Friends always stay on the right and the left side

326
00:18:49,589 --> 00:18:54,339
Regardless of the two nodes moving to the center

327
00:18:55,339 --> 00:18:58,480
I'm sure that this was complete gibberish to you

328
00:18:58,480 --> 00:19:01,420
But i think let me show you how next works

329
00:19:01,420 --> 00:19:05,900
And then later on we can also look at left side friends and right side friends

330
00:19:05,900 --> 00:19:08,039
A good example for that

331
00:19:08,039 --> 00:19:12,329
And i'm going to include that in the video description

332
00:19:12,329 --> 00:19:14,690
Is the compass of etal constant

333
00:19:14,690 --> 00:19:17,589
And i have an ex collibrain video about that

334
00:19:17,589 --> 00:19:23,200
And that explains i think much better the right and left side friends

335
00:19:23,259 --> 00:19:27,019
But for now i'm going to click here on next friends

336
00:19:27,180 --> 00:19:29,140
And when i do that

337
00:19:29,140 --> 00:19:36,460
You see that ex oli brain already recognized that these should be on the right hand side

338
00:19:36,460 --> 00:19:41,900
And you can also see that the line is now a solid line

339
00:19:41,900 --> 00:19:43,400
Not a dashed line

340
00:19:43,400 --> 00:19:48,720
And that's because the dashed line means it's an inferred relationship

341
00:19:48,720 --> 00:19:50,799
I infer the relationship

342
00:19:50,799 --> 00:19:53,440
Because there's a link in the document

343
00:19:53,519 --> 00:19:59,559
And then i infer that the two have some relationship with one another

344
00:19:59,559 --> 00:20:04,019
The moment i explicitly state in the ontology

345
00:20:04,140 --> 00:20:06,039
What the relationship is

346
00:20:06,039 --> 00:20:13,419
So it's a position from that moment on this comes to the right hand side

347
00:20:14,819 --> 00:20:20,160
So i think we're going to stop here for part one

348
00:20:20,160 --> 00:20:23,119
I'm going to continue on with part two

349
00:20:23,119 --> 00:20:25,319
And you can tune in to part two

350
00:20:25,319 --> 00:20:30,409
But i think so far i've already shared enough video that

351
00:20:30,409 --> 00:20:33,779
I recommend that you create a new obsidian vault

352
00:20:33,900 --> 00:20:36,220
You download these three plugins

353
00:20:36,220 --> 00:20:40,599
And you play with these settings that we've looked at until now

354
00:20:40,599 --> 00:20:43,359
And then you come back for part two

355
00:20:43,359 --> 00:20:50,079
Where we are going to continue with the customization of the settings

356
00:20:50,079 --> 00:20:55,259
As well as we're going to continue to build this x color brain

357
00:20:55,440 --> 00:20:56,279
Thank you

358
00:20:56,279 --> 00:20:58,279
[由 vCaptions 生成]
