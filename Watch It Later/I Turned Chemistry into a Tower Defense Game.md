---
url: https://www.youtube.com/watch?v=kaEGfuiSPjA
tags:
  - video
status: readed
date: 2026-06-17T17:07:37+08:00
---
![I Turned Chemistry into a Tower Defense Game](https://www.youtube.com/watch?v=kaEGfuiSPjA)
  
章节

转写文稿

## Intro

0:00

Ever since ancient times, there has been  the belief that matter is composed of tiny  

0:05

particles. It wasn’t until around the 1800s  that the modern theory of the atom emerged  

0:11

and presented the idea that atoms combine  in distinct ratios. But ratios means logic,  

0:18

and logic means it can be turned into a video  game, and that’s about all the motivation I needed  

0:23

to make this happen: here’s how it went. So to start this project the first thing we’ll  

## Atoms & Towers

0:29

need are some atoms. and atoms have electrons  as well so lets add some of those in. I’m pretty  

0:35

sure electrons move around a bunch--lets make  it happen. ok that’s a little excessive and on  

0:42

second thought, this isn’t that helpful, I’ll  just revisit it later. I think its a good idea  

0:47

to get the basic mechanics of the tower defense  down before expanding on the chemistry too much,  

0:53

so lets take care of that. The atoms are going  to act as towers, so first we need them to be  

0:59

able to shoot things. And the targets should  also have health be able to be destroyed. Now  

1:05

lets add a destination for the targets  that needs to be defended. Then we just  

1:09

need a spawner for the enemy targets,  and we have a basic gameplay loop.  

1:15

The idea from here is that each atom will  have different stats or properties, and the  

1:21

atoms should be able to combine into molecules or  compounds to create upgraded towers. It’s been a  

1:27

while since I’ve done much with chemistry, and I  naively thought I’d be able to come up with some  

1:33

dynamic code that could handle atom combination  automatically. For simple compounds that follow  

1:39

something called the octet rule, this task is  fairly easy. Atoms have different “shells” of  

1:45

electrons, and for fulfilling the octet rule I  just need to define the number of electrons in  

1:51

the outer shell for each atom and see if one atom  plus another equals 8 because in most cases this  

1:58

will form a stable compound. The group numbers on  a periodic table are convenient for this because  

2:04

the columns are generally ordered by how many  electrons are in the outer shell, so it’s just  

2:10

easy arithmetic to find some valid combinations  like magnesium oxide or sodium chloride.  

## Compounds

2:19

However, once we move into compounds with  more than two atoms, things get a bit more  

2:23

complicated. In addition to the outer shell  of the atom, factors like electronegativity,  

2:30

ionization energy, atomic size, and more can all  effect chemical combination. While some compounds  

2:37

can be created through generalized rules, at least  in my experimenting, it seemed like too many edge  

2:43

cases were needed to create a dynamic script-based  composition system. I ended up going with a more  

2:49

hard-coded approach where a I provided a list  of valid compounds that could be created with  

2:54

the atoms that I included in the game. But  I did try something a bit more dynamic with  

2:59

visually forming bonds which I’ll explain later  on. The hard-coded list is implemented as follows:  

3:07

there is both a shop and an inventory in the  game, and when you buy atoms from the shop,  

3:12

you can either place them directly on the field,  or click on existing atoms to compare them to the  

3:18

atoms in your inventory and see if any combination  can be formed. This was a little tricky to set up,  

3:24

but basically a button is created for every  possible compound with the available atoms,  

3:30

and you can click the button to upgrade the  atom into that molecule or compound.  

3:35

I started with just a couple atoms, then added the  rest to the game, and made it so that the atoms  

3:40

that are lower in the periodic table have a higher  rarity. Higher rarity means that they will have  

3:46

better stats but they will cost more and be less  likely to appear in the shop. The main stats for  

3:52

the atoms are damage, attack speed, and attack  range. I added a visual indicator to show the  

3:59

attack radius, and I also added a new damage type  that’s a laser instead of a projectile. The main  

4:05

thing that’s lacking at this point is visualizing  the compounds. There’s a type of diagram called a  

4:11

Lewis dot structure that is convenient for showing  the octet rule I mentioned earlier. Perhaps with  

4:17

the compounds predefined, it will be easier  to create a dynamic script for showing these  

4:22

Lewis structures. The basic rule I decided on is  this: if an atom can give an electron to either  

4:30

reach 0 electrons or give another atom a total  of 8 electrons, and both atoms have at least 1  

4:37

electron available, then both atoms will give  up an electron create a bond between them. In  

4:42

a compound with more than two atoms, each atom  will compare itself to every other atom in the  

4:48

list and follow that rule. And there are also edge  cases like hydrogen gas where both atoms should  

4:54

give up their electron to form a single bond. You  can see the new bonding structure in place with  

4:59

hydrogen sulfide in this clip. I didn’t have time  to create rules and conditions for multiple bonds,  

5:06

and some cases are still not covered in the simple  rules that I used, but it at least give a somewhat  

5:11

interesting visual basis to work with. I then added a few more mechanics such as a stat  

5:17

sheet to show the stats on current elements and  compounds, and I gave atoms that have available  

5:23

combinations a highlight to show that they  are ready to combine. For the enemies, I added  

5:29

a new pathing system as well as enemy types with  different speeds and health values. To make use of  

5:36

this, I drew up a map, and from here I added the  final polish onto the game. Here’s how it looks.  

## Final game

6:19

There are now a couple different turret types such  as trap turrets that place damaging traps along  

6:25

the track as well as buff turrets that increase  the damage of projectiles that pass through their  

6:30

field. There’s also a limit to how many atoms  or compounds can be on the field at one time,  

6:36

so you have to strategically make use of the  best compounds available. There’s a lot more I  

6:41

wanted to do with this project such as adding acid  damage to acid compounds or explosive effects to  

6:48

compounds like methane, or have a water compound  unlock new effects for surrounding turrets,  

6:54

but I’ve run out of time for this project for the  moment at least. If enough people seem interested  

6:59

in it, then I may revisit this to expand on the  mechanics more and give it a more interesting game  

7:05

loop. As it stands, after a few waves, the game  enters infinite mode with increasing numbers of  

7:11

the most difficult enemy. I really haven’t  had time to balance and playtest properly,  

7:16

so I’m not sure what the most powerful  compounds and effective tactics are. If  

7:21

you’d like to try out the game for free,  I’ve placed a link in the description-I’m  

7:25

curious to see how far people can make it into  infinite mode with the options available.  

7:31

Thank you all for watching the video and  supporting the channel. Until next time.