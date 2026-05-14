---
url: https://www.youtube.com/watch?v=bMTeCqNkId8
tags:
  - video
status: readed
date: 2026-05-14T21:19:22+08:00
---
![Realtime shadow casting on 2D terrain](https://www.youtube.com/watch?v=bMTeCqNkId8)
Realtime shadow casting on 2D terrain
https://www.youtube.com/watch?v=bMTeCqNkId8
无作者 

[章节] Intro

a little while ago this image, was posted to Reddit by a user, called Sing is for Chad ignoring, the username, I think this image looks awesome and when I first saw it I recreated, it and while I did get it working it was really slow, even at super small resolutions, as you probably know I've been messing around with shaders a lot recently, and I figured it was time for, me to revisit this and get it, running in real time just a quick, disclaimer, this is just how I managed to do it there's probably a million, much better ways of doing this, but I think it's pretty cool, so I thought I'd share it with, you as always the code for this, demo ISE, available in the description, so you can follow along and run, this project for yourself in, the browser you'll also find, a link to the original Reddit, post down there as well so check.

[章节] Height maps

that out the terrain I use for, this comes from a height map, which is basically exactly what, it sounds like we can look up, a coordinate in the height map, and it'll tell us how tall the, terrain is at that point in the, past I've extruded, this height map to actual 3D geometry, but often like in this case height, maps are used in 2D terrain to, figure out which type of tile, should be placed where in such, a case there is no 3D geometry, to create lighting with just, a flat image of all the tiles, but you can still generate shadows, as you can see here to get started.

[章节] Generating the terrain

we obviously need some height, map terrain the terrain really, isn't the focus of this video, so I've kept it really basic, and I won't go into too much, depth on it in fact I've covered, this style of terrain generation, in a couple of old videos which, you can check out here but for, a quick refresher, here's what I'm doing I'm using, some pear in noise to generate, a random value between 0 and, 1 for each tile, this value is the height of the, terrain and I can use it to determine, the color or the type of each, tile to make sure we always get, Islands I'm washing the noise, values the further they get away, from the center which pushes, some of the terrain beneath the, water level creating islands, and that's basically all there, is to it I'm saving the height, values in an image with the minimum, height being black and the maximum, height being white and I'm saving, the colors of the terrain in, a separate image so that I can, pass them both to the GPU when, it comes time to figure out the, Shadows, which is what we're going to.

[章节] Shadows

do next to make the Shadows we, simply need to darken any region, of the image that isn't touched, by light the tricky bit is figuring, out if a region is touched by, light or not and we're going, to do that inside, a Shader if you haven't used, shaders before check out my introduction, to shaders video it covers all, the basics and teaches you everything, you need to know to follow along, with this video I promise they're, not as hard as you think our, Shader needs a few bits of information, and we'll pass it our two pieces, of terrain data the color map, and the height map, as well as a 3D Vector that will represent the sun's location, to figure out if the fragment, we're drawing is in a shadow, or not we need to know if there's, a direct line between the fragment, and the Sun that doesn't run, into any other terrain the way, I do this is create a 3D point, from, current pixels location for the, X and Y and I look up the height, for that position to get the, Zed I then find the vector that, goes from this point to the sun's, location.

and if we take small steps along, this Vector we'll eventually, reach the Sun what we can do, is check each step along the, way to see if we're inside the, terrain or not this is done by, simply sampling the height map, at our current X and Y position, and if the height is greater, than our current Point's height, stored in the Zed we're inside, the terrain, and we know that the pixel Weare rendering is in Shadow, and if that's the case we can, break out of the loop likewise, if our Point set is greater than, one we know that we're above, the highest terrain, since the height map is in the, range of 0 to 1 which means we, must be in full light letting, us break out of the loop as well, there's almost certainly a more, elegant way of doing this and, if you know it please let me, know in the comments, if you're enjoying the video, feel free to Chuck it a like, and maybe subscribe while you're, there cheers, so we now know if we're in a, shadow or not all that's left, to do is use that information, to make the image darker in the, shadowed regions.

and this is nice and easy I just, use a mix function to choose, between normal terrain color, and a dark conversion on it based, on if we're in a shadow or not, and that's all there is to it, we're using a height map to cast, Shadows on 2D Terrain in real, time obviously this method has.

[章节] Limitations

its limitations, since the height map data is in an image we can only get as much Fidelity, as the pixels, pixels are square and you can see that the Shadows look pretty blocky, especially when the sun's low in the sky casting Long Shadows, we can also see that some regions get a bit of a dithered texture, I actually think this looks pretty, cool but it's definitely an artifact, of how the Shadows are calculated, like I said at the start I'm, sure there's heaps of other much, better ways of achieving this, same effect but it's just what, I came up with and wanted to, share it with, you, I've actually recently just set, up a Discord server so if you, need help with some code want, to discuss a video in more detail, or just want to hang out with, other creative coders and Game, devs come and say hi there's, a link in the description.

[章节] Next steps

I think it might be fun to take, this demo a bit further and add, some more traditional lighting, models by calculating, the surface normals from the, height map I don't have time, for that today unfortunately, but let me know in the comments, if that's something you'd like, to see on that note thank you, so much for watching happy Coach, and I hope to see you again soon.



--- 由 vCaptions 生成 ---