---
url: https://www.youtube.com/watch?v=UavoVWHrebM
tags:
  - video
status: readed
date: 2026-08-10T16:08:59+08:00
---
![Creating 3D Lighting for my 2D Game](https://www.youtube.com/watch?v=UavoVWHrebM)
Creating 3D Lighting for my 2D Game
https://www.youtube.com/watch?v=UavoVWHrebM
无作者 

00:03 hi so recently I decided to pick back up a game that I started about a year ago, 
00:09 but I quickly lost an arrest on that was until I recently discovered, 
00:13 this channel by a very talented guy who is developing a beautiful 3D Pixel art, 
00:18 game this gave me the idea to do something, 
00:22 similar with my game and give it a little glow up, 
00:26 so for a little context my game has been a 2d isometric pixel art game on a, 
00:31 grid-based world which means that all the Sprites are two-dimensional and it, 
00:35 makes the game look a little flat and boring so let's change that with some 3D, 
00:40 lights well kind of it is obviously not possible to use a real 3D lighting, 
00:45 system on two-dimensional Sprites however this is where a little trick, 
00:50 called normal Maps comes in a normal map is basically just a second, 
00:54 texture that gets slapped onto the original but it contains information, 
00:58 about which part of this Sprite is facing into which direction, 
01:02 this is done by just taking the Sprite and coloring the certain areas with.

01:06 these colors now that the engine knows where each part of the Sprite is facing, 
01:10 we can use this in combination with the 2D lighting system which Unity, 
01:14 thankfully already comes with and as you can see now the light does, 
01:18 not illuminate the entire Sprite smoothly but actually creates a, 
01:21 three-dimensional effect for the nighttime setting this works, 
01:25 perfectly but during the day I use something called a global light this, 
01:29 type of light does not have an origin and by that illuminates all the Sprites, 
01:33 in the scene equally so I had to come up with a little trick to achieve the, 
01:37 effect of sunlight I created an extra rendering layer which only targets the, 
01:41 objects of the world now I created a sprite light which, 
01:45 rotates around the camera to highlight the object in sight so the only thing, 
01:49 missing now are shadows for that I created a prefab that I could attach to, 
01:53 every object that I wanted to cast a shadow this prefab then just gets the, 
01:57 Sprite of the object as soon as the scene starts rotates it by 45 degrees on.

02:01 the x-axis makes it black and turns the opacity down now the only thing to do is, 
02:06 update the position and the rotation based on the sprite light that we've, 
02:10 created earlier so finally here's a little comparison for the before, 
02:14 and the after, 
02:25 thanks for watching foreign.



--- 由 vCaptions 生成 ---