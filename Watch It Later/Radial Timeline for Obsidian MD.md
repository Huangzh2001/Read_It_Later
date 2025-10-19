---
url: https://www.youtube.com/watch?v=7noTSFaj8Eo
tags:
  - video
status: readed
date: 2025-10-19T18:12:28+08:00
---
![Radial Timeline for Obsidian MD](https://www.youtube.com/watch?v=7noTSFaj8Eo)
0:00
Stories are like puzzles, and every scene is a small piece of that puzzle. The radio timeline makes that puzzle manifest. Your story unfolding until the final piece clicks into place. In this

0:16
introduction, I'll show you how to install and use the radial timeline plugin for the Obsidian Notetaking app. We'll explore the different modes, see how it works across projects using the

0:30
metadata you curate at the beginning of every scene, and learn how to customize it in settings. Chapters are included so you can jump to what you need. I'm Eric. I love writing sci-fi and for

0:47
the longest time have been looking for a better way to view all my scenes. Tables and spreadsheets are great, but I thought something that provides the big picture at a glance would be even

1:00
better. So, I built this plug-in after being inspired by the incredible data visualizations over at d3js.org. With its compact size, multiaceted design, and expressive color palette,

1:18
you have everything you need at a glance with the radio timeline. The radio timeline is organized around an outer perimeter marked by the months of the year, act labels, and if enabled, plot

1:33
beats. The first ring displays either just the main plot scenes or optionally all subplot scenes. Moving inward, each subplot is assigned its own ring. Subplots with the most

1:49
scenes are placed closer to the outer perimeter where there's more room. At the center, we have the data grid, which tracks status and publish stage. Using the metadata at the beginning of

2:03
each note, the timeline places scenes and plot beats into three acts. On the left side, subplot names are labeled in large arcing text. In my current book one project, I have

2:18
around 50 scenes packed into act one. Even when it's dense like this, just hover over a scene to enlarge the full title. The opposite quadrant displays metadata fields for the scene, including the

2:34
scene title, date, synopsis, AI beats optionally, as well as all characters and subplots. If the scene is edits pending or overdue, that is noted as well. The plug-in supports two

2:52
display modes. In all scenes mode, every scene is shown in the outer ring. When you hover over a scene, it will highlight in every subplot where it appears. There are unique colors for each subplot

3:08
ring, which can be customized in settings. Your plot system only appears in the outer ring. Unlike scenes, plots are fixed width, but their full title text is written around the perimeter. If beat

3:26
titles potentially overlap, formatting automatically stacks them neatly one after the other. As with scenes, you can hover over a beat to see its synopsis. Plot beats are created just like scene

3:40
notes, but with metadata class plot instead of class scene. Now, if I go into settings and turn off show all scenes in outer ring, the timeline switches to main plot mode. In

3:56
this mode, the outer ring only shows main plot scenes. Subplot colors are removed. Save the cat beats are hidden and instead each scene is colored by its publish stage. Zero draft, author,

4:12
house, or press. This simplifies the timeline, especially the outer ring, and emphasizes your overall progress toward getting the book ready for publication. Installation is simple. In Obsidian, go

4:30
to the settings, then community plugins, search for radio timeline, install, and enable. If it's not yet in the community plugins browser, you can use BRAT, another community plugin.

4:48
BRAT installs beta plugins or ones pending approval. You paste in the GitHub URL for radio timeline and BRAT handles installation. One benefit of using BRAT is that it

5:01
lets you choose which version to run. You can select the latest version and it will always keep the plug-in up to date. Or you can keep using an older version so nothing changes.

5:15
In a new vault, setup is easy for radio timeline. You don't have to type metadata manually to create your scenes. Just click the timeline button in the toolbar. If no scenes exist, the plug-in

5:30
will prompt you to create a template note. The template comes with all required front matter fields pre-filled. This template prefills fields so you get a sense of how a new project will look.

5:45
The plug-in defaults are assumed if left blank. Subplot defaults to main plot. Publish stage defaults to zero and act defaults to one. So in this example, you'll see two rings, two subplots. The

6:02
single scene has an index of one. If I click that scene, the number square turns to the theme accent color, showing it's open in Obsidian. If I mark pending edits, the number

6:18
square turns red, reminding me to revise. And if I advance this publish stage from zero to author, both the scenes color and the center info grid update instantly.

6:34
Now I'll switch to my other book which has a few more scenes. It's still in the early stages. To do that, we'll go to the radio timeline plug-in settings and change the source path. It's easy to

6:48
switch back and forth between the books with the help of the drop- down suggestions. This is my prequel project. Three subplots, a handful of scenes. I quickly see how the story is shaping up, how

7:04
subplots are developing, and how acts are filling out. Clearly, I have a lot of work to do, but I made progress on theme and some early key plot beats. Now, let's look at the features in more

7:21
detail. Each scene displays with a square prefix showing its scene number ordering notes in the right order. Number squares change color based on metadata status. As we've discussed,

7:36
scenes themselves also have conditions. If a scene is overdue, the entire slice fills red. If it's marked to-do, it has a gray plaid pattern. If it's working, the background is a sine wave with a pink

7:54
fill. The center info grid tracks progress across published stages and states. It's a 4x4 matrix. Rows are publish stages, zero, author, house, and press, and columns are

8:12
states, to-do, working, overdue, and complete. Squares fade out if no scenes match. Completed scenes display a count. An arrow shows which row is currently active.

8:30
Once a row is complete, the row changes to completed and the next row activates. Similarly, when all four rows are complete, the grid signals that your manuscript is ready for publication.

8:45
There's also a rotate timeline arrow button on the bottom right. Clicking this rotates the timeline counterclockwise. So, act two, normally at the bottom, shifts up into the top right for better

9:00
readability. Outer ring months are faded for past months and brighter for upcoming months. The inner rainbow ring shows where you are in the current year. This helps you

9:19
stay aware of how much time you have left before your writing year is up. A red tick mark projects when you'll finish based on your drafting pace. You can also set a custom target date

9:35
shown with a green tick instead of the default January 1st. If the estimated completion date is more than one year, the prefix number increments to show year two or three, etc.

9:50
Let's take a look at the AI beats analysis in the hover info. When you execute the console command to update, the scenes will be compared in sets of three for every flag scene.

10:04
As you can see in this example, the lines are color-coded green, red or gray, which correspond to a rating of good, neat work, or neutral. The middle scene, which is the flag scene, gets a

10:19
letter grade. This grade is also represented in the scene number squares. A key aspect of the venerable Nanorimo of Yore was good writing hygiene. And the reason I included zero as a publish

10:35
stage first it emphasizes the very rough sketchy nature of the author's initial attempt at their story and it recognizes that the first draft is a no revision stage. Just remember zero revisions for

10:52
zero draft. Scene front matter can be used to track the revision count and pending edits. When ideas come up, enter them in the pending edits field. Come back when you're ready for the next

11:06
publish stage to revise a scene using the pending edits notes you've already made. To help with this, I created a special zero draft mode, further explained in the settings segment later,

11:21
that prevents you from opening scenes that are marked complete while in the zero draft mode. In settings, the first field is the source path. This tells the plug-in which folder contains your

11:34
manuscript. The input field uses predictive text, which makes it easy to switch between valid paths. Next is the target completion date. Further down, you'll see the show all

11:49
scenes and plot beats toggle, which switches between all scenes mode and main plot mode. Below that is the zero draft mode which discourages editing a scene once it's

12:03
marked complete. Instead, when you click on a scene, a modal appears that allows you to update your revision ideas and save them without opening the scene. Next, we have AI analysis settings.

12:19
Enable the beats will reveal the AI analysis for scene hover and show the command pallet options. Disabling hides all AI related functions. Choose your provider. You must generate

12:34
an API key and set up billing with the provider. You can turn on AI response logs to track the details, including the prompt that radio timeline is using and the send and receive text.

12:49
Below that, you can customize colors for publishing stages and subplot rings. You can have more than 16 subplots, but the colors loop. All settings can be reset to default.

13:04
Finally, the readme at the bottom explains all features in detail, provides a front matter copy feature so that you can paste fields directly into notes. Since metadata is the backbone of radio

13:21
timeline, let's look more closely at it. Every scene note begins with front matter fields like title, act, subplot, status, and publish stage. These fields determine where the scenes appear and

13:36
how it's colored and what conditions it shows. The AI response is also included in the metadata fields as beats 1, 2, and three. You can always review these fields and

13:50
make adjustments to the text as needed. To make this easier, I rely on several plugins, data view, metadata menu, and templater. Any metadata can be automatically

14:05
included by creating a template scene, streamlining the process dramatically. Please see YouTube for many videos on these plugins. In the command pallet, typing radial shows all available commands.

14:21
You can open a timeline, same as clicking on the button on the interface. You can search the timeline, which highlights matching search terms in scenes by making the number squares

14:36
yellow and showing in the scene details highlights over the keywords. You can clear the search. You can also update flag beats either by subplot order or manuscript order. For

14:54
subplot order, adjacent scenes are taken from that subplot. For the manuscript order, the previous and following scenes of the flag scene may be from other subplots. So keep that in mind.

15:08
Clear AI cache allows you to reanalyze scenes. After analyzing a scene, a timestamp is placed in Beats update metadata field indicating when the scene was last processed and it won't be

15:23
processed again. Replace the timestamp with yes and clear cache. Then update flag beats. That's radio timeline for Obsidian. Install it, try both modes, and watch your story evolve into a personal

15:41
masterwork. Take screenshots along the way to capture your journey. The GitHub link is in the description. If this walkthrough helped, please like, subscribe, and

15:53
share it with your writing friends. I'd love to hear your thoughts in the comments. Thanks for watching, and as always, keep your timeline radial and happy writing.