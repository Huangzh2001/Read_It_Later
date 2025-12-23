---
url: https://www.youtube.com/watch?v=qNTv5SgM0BM&feature=youtu.be
tags:
  - video
status: readed
date: 2025-12-23T16:41:47+08:00
---
![I Built a Flying Umbrella](https://www.youtube.com/watch?v=qNTv5SgM0BM&feature=youtu.be)
This is an ordinary umbrella. And this  is a flying umbrella that follows me  around. Umbrellas haven't really changed  for the past 4,000 years. I mean, take a  look at these two pictures. The 

0:12fundamental design is exactly the same.  But it's 2024. I shouldn't even need to  hold my umbrella. So, today I'm going to  make the world's first umbrella that  flies. I mean, what could go  wrong? 

0:27In theory, this project should be pretty  simple. I reckon I can just slap some  propellers onto an umbrella so it flies  like a drone. But often theory can only  take you so far. Turns out people have 

0:37tried similar projects in the past, but  all of them are either fake or just  don't really seem to work. One of the  main problems has to do with the  placement of propellers. Propellers work 

0:47by sucking air from above and pushing it  downwards to generate thrust. If  we try placing propellers on top of the  umbrella, there's no space under for air  to flow. So, it doesn't work. And if we 

0:56try placing them beneath an  umbrella, the umbrella obstructs the air  intake, which reduces frost and also  doesn't work. If this is hard for you to  understand, take this car 

1:05analogy. If I place a piece of paper  here, it blocks the air flow, so  it stops working. But what if we made an  internal frame that allows the  propellers to stick out and be 

1:14positioned on the sides? Since there's  nothing above or below, this might  actually work. The propellers  can then be connected to motors like  this one here and controlled by various 

1:22electronics which will help the umbrella  stay stabilized while it's in  the air. I guess there still is a good  chance that this whole project just  isn't possible, but I suppose we'll have 

1:30to find out. Oh yeah, let's first go  find an umbrella.  I have a lot of different options, but  something about its bright yellow color  just makes this one stand out. Let's 

1:42remove the handle so nothing sticks out  the bottom during flight.  Now, here comes a pretty major problem.  This rod is the only point on umbrella I  can attach things to, which makes it 

1:53really hard to design a frame that  connects securely. I ended up creating  two different designs. This  simple practical design and this  slightly better looking but impractical 

2:01design. So, I decided to go with this  simp. Having these arms at an angle  tucks the electronics further into the  umbrella and makes the design much  cleaner. The only downside is that the 

2:10arms are much easier to break  upon future landings. But who cares  about the future when we live in the  present?  I actually have no experience with CAD  or 3D modeling, and it only looks like I 

2:21know what I'm doing because I  decided to speed this clip up by 2,000%.  But somehow I was able to learn quickly,  and only after a few hours of  It's currently day four, and that took 

2:32way longer than it should have. The  bright side is that we have all the  parts we need. So, here's the design. a  central hub with a hole for the umbrella  and four angle connection points for the 

2:41arms as well as four of these parts that  mount the motors onto the arms and a few  other parts as well. Now, let's just  have these parts 3D printed.  It seems like my 3D printer isn't really 

3:07working. Let's try that again.  For some reason, it's only printing in  2D.  Okay, now it's 3D, but not exactly. If  only if there was a way I could get  someone to print these parts for me. 

3:22Well, luckily, now I can. PCB Way offers  the best custom PCB prototyping  services, but they also offer 3D  printing. Just upload your files for an  instant quote. Choose from a variety of 

3:32materials and colors, and they take care  of everything so you can get the parts  shipped directly to your house. If  you're working on a project and need 3D  printing or any of these other services, 

3:41make sure to check them out. Thank you,  PCB Way, for sponsoring this video. It's  currently day 16. Yeah, let's start off  by connecting these motor mounts to the  arms. It seems like I accidentally made 

3:52these holes a bit too small, so now I  need to try and make them bigger. This  is probably going to be a pretty boring  process. So, let me try to make some  music.  Let's go. It fits. I had to do this for 

4:16all four parts, which ended up  taking an entire hour. This was actually  so painful. That took way too long. I'm  adding these pads, which should help  soften the landings.  Time to add the motors. 

4:30This is getting kind of annoying.  Now we can just painfully solder  20T wires, connect them to the motors,  slide them into the carbon fiber tubes,  and feed them into the central hub. 

4:48And boom. Now we have an  internal frame.  I think it's time to move on to  electronics. First, I solder the wires  to this ESC, which regulates the speed  of the motors. And then I connected to 

4:59this microcontroller that I can  program to keep the umbrella stabilized  when it's in the air.  All right, guys. I messed up. I  tried plugging in the lipo battery to 

5:09see if it would work. And yeah, the ESC  exploded and destroyed a lot of  the parts. I think it's because I  soldered these wires super badly, like  they might be touching each 

5:18other, but I don't really know.  I don't really want to spend 60 bucks  buying another ESC. So, let  There we go. Jokes aside, I had to take  everything apart and buy a lot of 

5:41replacement parts. At this point, I  started to question why I was even  putting all this effort into  something that probably wouldn't even  work. But maybe this mistake wasn't such 

5:50a bad thing after all, as I was able to  take this time to improve the design.  Since I was using over 7 m of wire,  switching them out for thinner  ones significantly reduced the weight. 

6:00And I also redesigned the wire  connections, making them non-permanent,  which allows the arms to now be  removable, so I can take things apart  for storage.  The large surface area of the umbrella 

6:12means that even a slight breeze  will cause it to be extremely unstable  and drift away. So, I'm hoping that a  GPS can help correct for this  and force them to hold position. And 

6:20then for control, I'll be using this  receiver and transmitter. Oh,  yeah. Let's see if anything explodes  again.  Let's go.  Nice.  Configuring and programming the drone  was kind of tough, but with a 

6:39bit of guesswork, self-intuition, and a  bit of help from Chat GPT, I'm pretty  sure this thing should now be able to  fly.  Why is that actually powerful?  All right, so the umbrella should 

7:06friction fit into this hoe and I can  wrap this around the arm so it stays  in place. And with the final  finishing touches, let's head out to see  if this sketchy project that took months 

7:15to make will actually work.    I don't know what I'm doing.  I decided to start off by just testing  the drone without the umbrella.  And somehow it actually worked.    But with the umbrella mess up the 

7:43aerodynamics, we were about to find out.  If this fails, that's like many months  of work just gone. All that is just  gone. But at the same time, on like the  grand scheme of things, it probably 

7:58doesn't even really matter. So, let's  just go for it. My heart is  actually racing, guys. All right, we're  going to start it. Start recording.  Ready? You ready?  Oh, I don't want to do this. Should I 

8:13just go for it?  Should I? I'm actually so scared, man.  Bro. Bro, that's crazy,  bro. That should not work. Oh my god.  All right, let's go.  The first flight went surprisingly well, 

8:48but things only started to go  downhill from there. During the second  flight, the umbrella started drifting  away and I barely caught up to it in  time before it smashed into the fence.  John. 

9:04And then the next day, this happened.  Oh no.  And then it started shaking super  violently. Yeah, there were a lot of  problems  instead of like lower. But after some  trial and error, I ended up fixing 

9:22things and now the umbrella is even more  stable than before. Now you might be  wondering, does it work in the rain? The  umbrella covers the electronics, but I  wrapped them up with plastic wrap just 

9:32in case.  Yo,  and yeah, this thing actually shields me  from the rain. It wasn't raining that  hard, but I reckon this thing  can withstand much harsher conditions,  just probably not stronger winds. 

9:51Currently, I can control the umbrella to  follow me around, but it doesn't do this  autonomously.  In the future, I could attach a camera  to the underside and write a program 

9:59that tracks my position and moves the  umbrella accordingly. So, 10,000 likes  and I'll try to make this work. With  that being said, thank you so much for  watching and see you next time.