---
url: https://www.youtube.com/watch?v=JjyEicYtVcU&t=5s
tags:
  - video
status: readed
date: 2025-12-08T12:21:59+08:00
---
![Getting started with ExcaliBrain - starting from an empty Obsidian Vault (Part 1 of 3)](https://www.youtube.com/watch?v=JjyEicYtVcU&t=5s)
0:00
so welcome back this is part two of the excalibrain dialogue mapping case study and in today's video we're going to look at further configuring the relationships and the links in our

0:18
excalibrane we are also going to be adding some new nodes and we're going to look at embedded nodes as well so there's plenty to learn and then there's going to be still a part 3 where we are

0:32
going to look at some additional things like web links and just polishing the whole thing up so hopefully by the end of the third part you will have a good Hands-On understanding of how to

0:47
configure excalibrine so today let's continue from where we left off so we have the remote work policy in the center and we defined the ontology for these two positions but at the moment you

1:04
don't yet see the position reflected on the links so we're going to open plugin settings again and this time I'm going to scroll down well before we scroll down so

1:18
what I want to show you is here at the top of the settings you have this section about ontology I also have a bit of a description here that tries to explain what an ontology is but here

1:33
what I want to point out is we have the position so this is what we added in part one to our ontology we have position here as a next friend type and then I'm going to scroll down all

1:51
the way to styling and I'm going to come to the link Styles now link Styles work very similar to how node Styles work from the perspective of inheritance so we have a base link style and then all

2:09
of the different node types or link types that you have here are going to inherit this and you can see that we have lots of different types many of these come pre-packaged with x-coli

2:25
brain so you might want to delete these later on I want to set up excally brains such that in every case the ontology is visible on the link so I'm going to change the base link style for now and

2:42
I'm going to just scroll down here and I'm going to turn on this link here to show label on link and otherwise I think I'm going to leave it like this if you want you can make the text slightly

3:00
smaller or bigger I like this relative sizing that's why it comes with the base setup so I'm going to leave it like this now Additionally you might also want to display arrows so here I'm going to say

3:17
that I'm going to set the start Arrowhead to be an arrow and then when we close our settings here so now we did all of this setting for the base style I didn't do any settings for the position

3:35
type of style we will see a different case a bit later on where I'm going to do settings because when I close settings then you will see that now the arrow is pointing from here to here

3:51
because at this pointing to the start arrows can be a bit confusing so depending on how you think about arrows and what's pointing from where to where um that that depends on your internal

4:09
dialogue and logic so you have couple of things that you can do around arrows so first of all the bass setting how Excalibur comes or X holy brain comes is an inverse Arrow

4:24
Direction which means that if I turn this off then automatically the arrows will change direction and then it will point the other way what's considered the start and then end will be different

4:40
or if I want to keep the inverse logic then I can come down here and instead of setting the start Arrow Head To Be an Arrow I can set the end Arrowhead to be an arrow and when I do this then you can

4:58
see that the end result is the same so I have the remote work policy here I have these arrows pointing to these two other nodes that diverts position written on them

5:13
so now let's continue to build our graph but I'm going to do one thing here so I'm going to first of all click on yes to remote work and here I'm going to turn on the embedded mode when I turn on

5:32
the embedded mode I can actually close this window so you will see here I have this button that synchronizes navigation between the leaf and the excalibrain view then I turned on the embedded mode

5:51
then this connector got disconnected so if I now turn off embedded mode you will see that the connection is on and when I turn again to embedded mode then the connection is disconnected so I can

6:08
close this if you don't like this Behavior again in excali brain settings you can scroll down all the way to behavior and you can click here to synchronize navigation

6:23
with the in that toggle if you turn this off then the two buttons will work independently from each other again you can play with this a bit later on to see the effects I can show you the effect so

6:37
right now if I click on remote work policy you can see nothing happens on the right hand side if I turn this button on then when I click on remote for policy then that page on the left

6:51
hand side changes as well but now I'm going to turn that off I'm going to close this and actually I'm going to close this as well so now we have the note here in the center you will also

7:06
notice maybe you will maybe you're not but I'm now going to highlight it too so you will notice that this now has a light background and that is because by default X call it raw comes with the

7:23
configuration that the style of the embedded node should follow the style of X color draw and now we are in a light excalator drawing and therefore this is going to be light as well so if I switch

7:42
here to I turn X holy brain off in a way so I'm going to turn off View mode then I can switch here to dark mode and you will see that this turns dark the colors in

7:57
this case look ugly so I don't recommend this now if you don't like this so if you would like to see dark colors here this is an example then you need to go to xcolid Raw settings to do the changes

8:13
so I'm going to click plugin settings and I'm going to make these changes I need to click here on xcolor draw and the next color draw settings I need to scroll down to the display section and

8:29
here at the top of the display section you will see that markdown embeds to match excali draw theme if I turn this off then when I come back you will see that now the document follows a dark theme

8:47
if you have excally brain running then it might turn out that you need to close and open exhale brain again for this change to take effect that's normal but just letting you know that that's

9:01
something that can happen so now I'm going to again turn ex-coli brain back on because you see now this is X call it raw so this is now X call the brain is not running to turn X holy brain back on

9:14
I need to open the command palette and I just need to type in brain normal with this ex call the brain will recognize that this document is already open and it will turn to excalibrane view mode so

9:31
let's continue editing our documents so first of all I want to Define here the supporting argument as an ontology as well so again I have two options I can either right click and click here add

9:49
supporting argument to excolibrant ontology so that's a perfectly valid option that's what we did in part one this time around I'm going to press control or command B and I'm going to just type in

10:05
next and here in the common palette I can choose X call it brain add data view field to ontology as next and when I click that then you will see in a second that excalibrane will update and you

10:23
will see that improves work-life balance moved from the bottom to the side and also now supporting argument as an oncology is displayed on this link now we are going to create improved

10:38
work-life balance the way to create the document is I'm going to hold down the shift key and click on the supporting argument and I'm going to create a markdown document so with this now I

10:53
have my markdown document right here and this is going to be a document type argument so that's why here I have the argument tag at the top and it contains a question and this is the question how

11:12
can remote work improve employee work life balance and to make this question again here right hand side or next type of ontology you already know the answer so what do I need to do

11:27
yes you guessed it right I need to right click and I need to add question to excolibrian ontology and I'm going to add this as a next friend and then ex call your brain will update and we'll

11:43
add this question to the right hand side of my graph let's just do a final setting in today's session we're going to format the supporting ontology link because I think

12:00
it would look nice if supporting arguments would be green and objecting arguments would be red so how do I do that think you can also guess this by now you need to open x-coli Brain settings and

12:18
in excali brain settings we're going to scroll down to the very bottom and here we're going to select from the next relationships we're going to select supporting argument yes so here's next

12:36
supporting argument on the supporting argument what I want to change is I want to change the color of this line I want this to be green so a supporting argument should be

12:53
queen and I actually wanted to make this a bit thicker so I'm going to click this that I'm setting this property of the supporting argument link type different compared to

13:08
the base link type and I'm going to make this a three thick so you can see now I have a nice thick Green Arrow right there and when I close settings then you will see that here the remote work

13:25
policy has this supporting argument with the work life balance here and we can stop right here next time we are going to continue by adding some evidences as well that are going to be some web links

13:42
and we'll see how you can embed links in here as well plus we are going to do some further formatting and settings and hopefully by the end of that you will have a pretty comfortable

13:57
understanding of how X color brain works with the basics and then you can do your own settings as well thank you