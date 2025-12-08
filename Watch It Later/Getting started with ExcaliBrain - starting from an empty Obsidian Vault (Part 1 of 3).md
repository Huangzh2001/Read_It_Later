---
url: https://www.youtube.com/watch?v=8LE_QdYQZVk&t=749s
tags:
  - video
status: readed
date: 2025-12-08T12:16:00+08:00
---
![Getting started with ExcaliBrain - starting from an empty Obsidian Vault (Part 1 of 3)](https://www.youtube.com/watch?v=8LE_QdYQZVk&t=749s)
0:00
hey everyone jolt here ex-coli brain is an obsidian plugin that I've built to visualize connections described in your markdown documents in a structured graph I realized that setting up excalibrane

0:16
can be a bit intimidating and there are many settings that you need to get your head around so I thought I would create this video that will take you through from

0:27
a completely empty volt all the way to having something that looks like this take you through a use case the use case is going to be a relatively silly simple example it's going to be an argument

0:42
mapping or rather a dialog mapping example exploring the pros and cons of setting up a remote work policy at a company so to give you a bit of frame I think it's important to understand the

0:58
framework that we're going to be applying here I'm going to be using the issue based Information Systems framework which is a dialog mapping approach and it consists of couple of

1:11
different components it consists of issues that are typically phrased as questions and this is how this is a dialogue mapping because it drives a conversation about issues and then there

1:27
are positions which are positions in response to these issues and then there are supporting and objecting arguments that support or object the positions and finally there are evidences that you can

1:43
attach to various nodes as well as in the end you reach a conclusion which you can call a decision now if you're interested in learning more about Ibis I have a video on it with another case study

1:59
and also you might want to take a look at the visualizing argumentation book which is the source of this it's a bit of an old book so it might be hard to find but anyway this is the book that

2:14
you can look for and that discusses the topic of argument mapping using Ibis so let's dive in we're going to start by creating a brand new empty obsidian Vault I'm going to click here create and

2:32
I'm going to type in the name X call it brain and we're going to pick a location for this which is this right here and then I'm going to click create and with this we have a new Vault now to get

2:50
excalibrane working you need to install three different plugins so we'll go ahead and start with that so I'm going to click here on obsidian settings and here I'm going to click on community

3:03
plugins and in community plugins the first time you start obsidian you need to accept the risks and consequences of turning on community plugins so I'm going to do that and I'm going to browse

3:18
for the different plugins that we need so first of all you need to install excellent raw because it's called it brain is built on top of X colored raw which is another plugin that I've developed

3:33
here after you've installed it you need to click enable and you can just close this message then next we are going to click on data View and I'm going to install data view as well

3:48
scholarly brain uses data view to extract the structure of documents so data view is an essential component for xcoli brain to work and finally we're going to search for excellent brain and

4:02
I'm going to click install as well and once it's installed I'm going to click enable on this plugin as well so with this we have the basic plugins installed and we can take a look at our plugin so

4:19
you can see that we have data view VX call it brain and we have X call it raw now it's important to keep in mind that excalib brain Builds on top of X column draw one consequence of this is some of

4:35
the settings in excalib brain will depend on settings in X call it raw I'll show you one example when we get to that point but this is something good to keep in mind and maybe this is also a bit

4:50
difficult at first to understand what is coming from scholar draw and what's coming from a scholar brain but hopefully you'll get the hang of it so to get us started I'm going to create a first

5:03
document in the vault I'm just simply going to click here to create a new node and I'm going to title this note remote work policy this is going to be the central question in our graph in our

5:20
dialog map and I'm going to just close this one right here once I've created this document I can now open excoli Brain it's very easy to start excoli brain you need to open the command

5:35
palette I'm going to press Ctrl P if you're on a Mac this is command p and I'm going to type in brain and I'm going to choose brain normal now brain normal opens in a new window within your

5:50
workspace and a brain pop out will open in a pop-out window but for now we're going to be happy with brain normal so when I click enter Then you can see that now excalib

6:06
brain is open and of course right now we have a single document in the vault and that is reflected here now you might also notice that here I have a second document that was created let's call it

6:21
brain you don't need to worry about it this is the file that's underneath the brain file or view that you have here you have not to worry about it but that's a file that's always going to be

6:37
overwritten by x-coli brain so I recommend not editing that file so now that we have this node here we need to start to add children and items to it to help us move quicker I'm going to use my

6:53
cheat sheet so I'm going to now paste here the question the initial question so should the company Implement a remote work policy and I'm going to add the two positions here

7:08
one position is a yes to remote work the other position is a no to remote work and you can see that as I did this the graph on the right hand side started to develop now if I click on yes the

7:27
company should Implement a remote work policy just to show you so this here is a Wiki link so I have the first part of the link is the file name and then after the pipe character I have the Alias for

7:42
this file what's being displayed right there if I click on this link then that creates this new file so this is now created this is yes to remote work policy you can see on the right hand

7:57
side the diagram has changed so yes to remote work is now in the center it has a parent which is remote or policy and it also has a distant relation which is this other position here which is the

8:15
node to remote now if I'm just going to copy this material over here as well to fill this in so this is going to be a position and notice what I'm doing here so at the top

8:30
I'm adding this tag so I'm going to zoom in so you can better see so I have attack here which is called position and here as well when I clicked the remote work policy you can see that this had a

8:46
tag question at the top we are going to use these to format the nodes also what you will notice is yes to remote work now looks different compared to node to remote work the

9:02
difference is that this note has been created and this doesn't yet exist in the vault and X call your brain can format it differently this is actually a super good feature because this way you can

9:19
also see connections between nodes that are not yet in your vault but you also notice that this now looks different compared to the example I showed in the beginning first of all you

9:33
see the dashed line and the items are under the central item not to the right and also the coloring and the look and feel is different so what do we do about this we're going to come to plug-in

9:49
settings and we're going to start to play a bit with excalibrain settings so you can see how you can format this so first of all I'm going to click here on settings and I'm going to click here on

10:04
excali brain you have lots of settings here for the time being we are not going to touch these I'm going to come all the way down to styling and first of all we're going to

10:18
add these two tags that we've created so one was the question and the other one was the position so we need to manually add the tags that we want to use for formatting purposes and once I've

10:35
added the text here then I can choose here in this and I need to add a comma in between so it's question comma position and once I've added them then the items will

10:50
appear here so if you noticed when I don't have a comma then these two items appear in a single row that's not good you need to add your comma right here and once I have the comma there then I

11:07
can start to format this for the question all I want is a question mark at the beginning of the question so the way this works and this might be a bit hard to comprehend at the beginning is

11:26
everything is inherited from the base note style so the base note style you can see all the settings of the bass notes style lots of different settings if I create a new node type for example

11:41
position by default everything is inherited if I turn this switch then I'm only going to see the non-inherited items which in this case is nothing because this is already the

11:57
next section so to customize the position I first need to flip the switch to customize the prefix so I'm going to flip the switch with this I tell let's call it brain that the

12:11
position will look exactly the same as the base note style except that the prefix is going to be different and I'm going to bring up the Emoji toolbar and I'm going to choose this light bulb so

12:27
for me a position is represented by an idea and I also want to change the background color of the idea node so I'm going to turn the background color switch on as well

12:44
I'm going to change the opacity so this is the transparency of the node 200 percent and I'm going to choose a different color I'm going to try to choose a nice dark yellow color

12:59
somewhere like this I'm happy with this color maybe a bit bit yellower like that so there you can see how the new format or new node looks like this actually doesn't look that very good so we're

13:16
going to look for a darker yellow Maybe maybe even yeah ah this is going to be good so I'm going to choose this orange red color so with this I formatted the position

13:32
and then I'm also going to format the question node and for the question node I'm only going to add a prefix and the prefix is going to be this question mark like this and now when I close

13:50
settings then what you will see is the formatting for the remote work policy is now indeed a question I wonder why we have an issue with the position so this is spelled correctly maybe I have an

14:10
issue here with the letter case oh no it's with the spelling so now I corrected the spelling unfortunately after I collect correct the spelling I need to redo my settings so the position

14:30
is going to be this light bulb and I'm going to set the color to again this orange red like I set it like this to this orange red like this and then when I close this then you can

14:53
see that now we have the formatting like this yeah so this is not an ideal formatting maybe we should change the font color of the position item as well so here I can again scroll down to

15:10
styling I can choose position and I also want to change the text color and I wanted the text color to be black and I think with that now the position looks much nicer now you can also notice that

15:27
no to remote work is still not yellow and that's because there is no document so there is no tag and if there is no tag then there's no Style but we can do something about it so we

15:42
are going to create this document right here what I'm going to do is here in excali brain if I hold down the shift key and click on a node then I'm prompted with this question if I want to

15:55
create a new markdown document or a ux collateral file so I'm going to say I want to create a new markdown document so this node to remote work file was now created and I'm going to just copy in

16:11
the contents of node to remote work so we're going to have the position then the title of the question and then the supporting argument and now you can see that at least we got

16:25
the colors right but the locations are still not good I mean the positions are under the central question and I want them to the beat on the right hand side so we still need to do some things so

16:42
you can see here in this row that I have something that's going on here so I have here position and I have double double columns here and then I have the name of the file this right here this position

16:59
double colon is called an data view field and excally brain is using these fields to understand the ontology which is the description of connections between items so this is

17:18
what describes the relationship between this document question and this item here which is a position so to make X call the brain recognize this ontology there's you have two options so first of

17:37
all I'm going to just right click here so in this line if I right click then you will see this menu item in the context menu add position to x-color brain ontology when

17:52
I click this then I can choose what sort of relationship this is going to have with the central node now I don't want to go into the details of these different type of nodes

18:06
later on we can touch on it and also I have other videos that will explain for now I just believe me that this should be a next friend the nature of a next and previous friend is it's a relative

18:23
position compared to the center because the next is to the right of the central node when it's still next but when they move then it becomes it comes to the left because then

18:39
for the next node it's the previous while the left side and right side friends always stay on the right and the left side regardless of the two nodes moving to the center

18:55
I'm sure that this was completely gibberish to you but I think let me show you how next works and then later on we can also look at left side friends and right side friends a good example for

19:07
that and I'm going to include that in the video description is the compass of zettel cost and I have an ex-coli brain video about that and that explains I think much better the right and left

19:22
side friends but for now I'm going to click here on next friends and when I do that you see that x-coli brain already recognized that these should be on the right hand

19:36
side and you can also see that the line is now a solid line not a dashed line and that's because the dashed line means it's an inferred relationship I infer the relationship because there is a link

19:52
in the document and then I infer that the two have some relationship with one another the moment I explicitly state in the ontology what the relationship is so it's a position

20:08
from that moment on this comes to the right hand side so I think we're going to stop here for part one I'm going to continue on with part two and you can tune into part

20:25
two but I think so far I've already shared enough video that I recommend that you create a new obsidian vault you download these three plugins and you play with these settings that we've

20:39
looked at until now and then you come back for part two where we are going to continue with the customization of the settings as well as we're going to continue to build this x color brain thank you