---
Archived: true
url: https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html?utm_source=chatgpt.com
---
[

runevision

Rune Skovbo Johansen

](https://runevision.com/)

- [Blog](https://blog.runevision.com/)
- [Games](https://runevision.com/multimedia/)
- [Articles](https://runevision.com/articles/)
- [Tools & Tech](https://runevision.com/tech/)
- [Graphics & Animations](https://runevision.com/graphics/)
- [About Me](https://runevision.com/about/)

  

## Procedural creature progress 2021 - 2024

Jan 10, 2025 in [game development](https://blog.runevision.com/search/label/game%20development), [procedural](https://blog.runevision.com/search/label/procedural), [The Big Forest](https://blog.runevision.com/search/label/The%20Big%20Forest), [video](https://blog.runevision.com/search/label/video)

For my game [The Big Forest](https://runevision.com/multimedia/thebigforest/) I want to have creatures that are both procedurally generated and animated, which, as expected, is quite a research challenge.

As mentioned in my [2024 retrospective](https://blog.runevision.com/2025/01/2024-retrospective.html), I spent the last six months of 2024 working on this – three months on procedural model generation and three months on procedural animation. My work on the creatures actually started earlier though. According to my commit history, I started in 2021 after shipping [Eye of the Temple](https://runevision.com/multimedia/eyeofthetemple/) for PCVR, though my work on it prior to 2024 was sporadic.

Though the creatures are still very far from where they need to be, I'll write a bit here about my progress so far.

### The goal

I need lots of forest creatures for the gameplay of *The Big Forest*, some of which will revolve around identifying specific creatures to use for various unique purposes. I [prototyped the gameplay](https://blog.runevision.com/2024/10/procedural-game-progression-dependency.html) using simple sprites for creatures, but the final game requires creatures that are fully 3D and fit well within the game's [forest terrain](https://www.youtube.com/watch?v=VxMwggFQRQM).

[![[Clippings/attachments/f592eb307709c61420b9378cd53a2e92_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh1UPpJ75QM7Xwsrvo0xIj0kez8I_P2AndgRJm0Ni5X-OIakCbGmOtmxB41rRByO6-ZueTWCjluFsRdukGS3pdEWYchfh1vtFMrqimIXPbYFQDDlg93HyHwR1pWhjksvCQO4qqGT1ER6MZ-dmB75ojV2dmvV7EyMD67dwZ-wE8LiweSFgELjVkt0tc7Nrk/s1600/CreaturesGoal.jpg)

I've seen a fair amount of projects with procedural creatures. It's not too hard to create a simple torso with legs, randomizing the configuration, and animating movement by transitioning the feet between footsteps in straight lines or simple arcs.

This works fine for bugs, spiders, lizards and other crawly critters, as well as for aliens and alien-like fantasy creatures. The project Critter Crosser is doing [very cool things with this](https://www.youtube.com/watch?v=a87tB__3KEs). While it features mammals too, I'm not sure they'd translate well outside the game's intentionally low-res, quirky aesthetic.

If we also consider games where only the animation is procedural, [Rain World](https://www.youtube.com/watch?v=sVntwsrjNe4) is another example where this works great for its low-definition but highly dynamic alien-like creatures. [Spore](https://www.spore.com/) is a classic example too, though its creatures often end up looking both alien and goofy.

For *The Big Forest* though, I want creatures that feel like they truly belong in a forest, with movement and design reminiscent of quadruped mammals like foxes, bears, lynx, squirrels, and deer. The way mammals look and move is far too distinct to simply "wing it" – at least in my game's aesthetic. Achieving realistic mammalian creatures requires thorough study, so although I also plan to include non-mammal creatures, I’m focusing primarily on mammals for now.

### Procedural generation of creatures

The basic problem is to generate forest creatures with plausible anatomy with a small set of parameters and ensure that:

1. The parameters are *meaningful* so I can use them to get the results I want.
2. Any random values for the parameters will always create valid creatures.

My main challenge is identifying what constitutes meaningful parameters. This is something I have to discover gradually, starting with a large number of low-level parameters based on minimal assumptions and eventually narrowing down to a smaller set of high-level parameters as I refine the logic.

From the beginning, I decided to focus on basic proportions for the foreseeable future, without worrying about more subtle shape details. For this reason I limited the generated meshes to extruded rectangles. I had to start somewhere, and here's the glorious first mesh:

[![[Clippings/attachments/8a2376bf092f858daedc1d56c4bcafb0_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgtXytqhyphenhyphen_a4t847yOVBqISeUAYnq142sqOI3W1rG93bj35inzVd2JPQwdihzHo2-J4ClKzFO1_fyfBGIceeG05dp7EqEimFbfuFubwFi-J9dhLi5NOtK7NYiLBPSDzfMW2j1PIxtw1fRsliwvlXUgiBIyMKiKLw79LqpAQ1wTjtbjjCqvhIYLJhnDoi1Y/s1600/CreatureBeginning.jpg)

Later I specified the torso, each leg, each foot, the neck, head, jaw, tail, and each ear as multi-segmented extruded rectangles. I found this approach easily sufficient for capturing the likeness of different animals. By the end of 2023, I had produced these three creatures and the ability to interpolate between them:

[![[Clippings/attachments/a9271e58a6a1ad9b127e7680a50cc6cc_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgqSYzXAl8cK0PjbxbihvcIChlvunZ0MNQakBBftgypmocql7oZFndVniCfL2HT-OPM8H3KwbQJJAGcrlgidcRJoD8pmASjODDIBSefK1F3Z1es82GUw_GgtKloRSRXmdGe6PKGgADloYfXk3NHolTQFfXhddj9dGPPxsXEBWdBUG5qzod5WxvmRhgTIzQ/s1600/ThreeCreatures.jpg)

This was based on very granular parameters, essentially a list of bones with alignment and thickness data. Each bone length, rotation values, and skin distance from the bone in various directions was an input parameter, totaling 503 parameters.

Creating creatures from scratch using these parameters was impractical, so I developed a tool to extract data from skinned meshes. The tool identified which vertices belonged to which bones and derived the thickness values from that. However, it was error-prone, partly due to inconsistent skinning of the reference models. For example, in the cat model, one of the tail bones wasn’t used in the skinning, which confused my script. This is why part of the cat’s tail is missing in the image above.

I tried to implement workarounds for such edge cases, and various ways to manually guide the script towards better results for each creature, but each new reference 3D model seemed to come with new types of quirks to handle. After resuming work in 2024, I had these seven creatures, with their reference 3D models shown below them:

[![[Clippings/attachments/13c172808aca13e412737f762790c89c_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgA8YIPRMFJ4YGFHJKBAVMZVnuzdO0H8BTyCkgysFDxfrgdVPeaaLqE6NnuQrFbAqv-VZ1f3m11yF8Twe5vYkB3BBwkyUCwp5FPrwFTkyTmeLKMww9Scoumvr2zbtaUJeH4TupIGT00epd40MHRW6aiHk2B8KFH29sU1j96IgXDOO3Ai1lf73hwTTm5DcE/s1600/SevenCreatures.jpg)

(I lost two of my original reference 3D models – the coyote and bull elk – because they were in Maya format. Since I don’t have Maya installed, when a project reimport was triggered, Unity couldn’t import the models, and they vanished. Since it's not standard practice to commit Unity’s imported data (the Library folder) to source control, I couldn’t recover them.)

Anyway, so far all my efforts had been focused on representing diverse creatures through a uniform structure that can be interpolated, but I hadn't yet made progress on defining higher-level parameters.

#### Failed attempts at automatic parametrization

Once I shifted my focus to defining higher-level parameters, the first thing I tried out was using Principal Component Analysis (PCA) ([Wikipedia](https://en.wikipedia.org/wiki/Principal_component_analysis)) to automatically identify these parameters based on my seven example animals. In technical terms, it worked. The PCA algorithm created a parametrization of seven parameters, and here's a video where I manipulate them one at a time:

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20240807_CreaturePrincipalComponentAnalysis.mp4#t=0.001" type="video/mp4"></video>

As I suspected though, the results weren't useful because each parameter influenced many traits at once, with lots of overlap, making the parameters *not meaningful*.

Why did it create seven parameters? Well, when you have X examples, it's easy to create a parametrization with X parameters that can represent all of them. You essentially assign parameter 1 to represent 'contribution from example 1', parameter 2 to represent 'contribution from example 2', and so on. This is essentially a weighted average or interpolation. While this isn't exactly what Principal Component Analysis does, for my purposes it was just as unhelpful. Manipulating the parameters still *felt* more like interpolating between examples than controlling specific traits.

When I talk about "meaningful parameters", I mean parameters I can understand – something I could use in a "character creator" to easily adjust the traits of a creature to achieve the results I want. Say, parameters such as:

- Bulkiness
- Tallness (relative to back spine length)
- Head length (relative to back spine length)
- How pointy the ears are
- Thickness of the tail at the base (relative to torso thickness)

However, PCA doesn’t work that way. Each parameter it produces influences many traits at once, making it impossible to control one trait at a time. I encountered the same issue in the academic research project [The SMAL Model](https://smal.is.tuebingen.mpg.de/). While this project is far more sophisticated than what I could do, and is based on a much larger set of example animals, their PCA-based parametric model ([which you can try interactively here](https://dawars.me/smal/)) suffers from the same problem. Even though it can represent a wide range of animals, I wouldn't know how to adjust the parameters to create a specific animal without excessive trial and error.

I'm also convinced that throwing modern AI at the problem wouldn't work either. Not only would it require far more example models (which I don't have) and AI training expertise (which I have no interest in acquiring); it still wouldn't address the fundamental issue: An automated process can't understand what correlations and parameters are meaningful to a human.

Another problem with automated parameters is that they don't seem to guarantee valid results. When experimenting with my own PCA setup, or with the *SMAL Model* I linked to, it's easy to come across parameter combinations that produce deformed glitchy models. Part of finding meaningful parameters is figuring out what constitutes meaningful ranges for them. For example, the parameter "Thickness of the tail at the base" might range from 0 (a minimal tail thickness, like a cow's) to 1 (a tail as thick as the torso, like a crocodile's or sauropod's).

This ensures that the tail thickness can't accidentally exceed the torso’s. It also means that changing the torso thickness may affect the tail thickness too. While this technically involves "affecting multiple things at once", it’s done in a way that’s sensible and meaningful to a human (specifically, me). An automated process can't know which of these "multiple things at once" relationships feel meaningful or arbitrary.

#### Manual parametrization work

Having concluded there was no way around doing a parametrization manually, I began writing a script with high-level parameters, which would produce the values for the low-level parameters (bone alignments and thicknesses) as output.

I made a copy of all my example creatures, so now I had three rows: The original reference models, the extracted creatures (automatically created based on analyzing the skinned meshes of the references) and the new sculpted creatures that I would try to recreate using high-level parameters.

[![[Clippings/attachments/c26d3a66e61be0d2a85557c4b754e908_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhweRQDbrL3Ia-804ASZtUgbwxzVn1CtB1qVw7I3hx0gaSkyBwnimdq-chw_nCxm322nX507yJBWwQfeaUZAsgm3l_4OijqwHCMgrw0rGNKDP3hJZNP-VvdIKD15DOufeNf8fV4HKGhyphenhyphenTluJYpNi4X3FBlHd_PMEilfeQpQtd40h2f_-uBSctCSvUWFlm4/s1600/ThreeRows.jpg)

Initially, the high-level parameters controlled only the torso thickness (both horizontal and vertical) and tapering, while the other features remained as defined by the extracted creatures. Gradually, I expanded the functionality of the high-level parameters, ensuring that the results didn't deviate too much from the extracted models – unless they were closer matches to the reference models.

Why keep the extracted models around at all instead of directly comparing with the original reference models? Well, I was still working with only extruded rectangles, and there's only so much detail that approach can capture compared to the high-definition reference models. The extracted models provided a realistic target to aim for, at least for the time being.

From there, my methodology for moving towards more high-level parameters was, and still is:

1. Gradually identify correlations between parameters across the example creatures, and encode those into the generation code. The goal is to reduce the number of parameters by combining multiple lower-level parameters into fewer higher-level ones, all while ensuring that all the example creatures can still be generated using these higher-level parameters.
2. As the parameters get fewer and more high-level, it becomes easier to add more example creatures, which provides more data for further study of correlations.

*I repeat these steps as long as rolling random parameter values still doesn't produce sensible results.*

Here's a messy work in progress:

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20240830_CreaturesWIP.mp4#t=0.001" type="video/mp4"></video>

To help me spot correlations between parameters, I wrote a tool that visualizes the correlation coefficients between all pairs of parameters, and shows the raw data in the corner when hovering the cursor over a specific pair. (In this video, the tool did not yet display all parameter types, so a lot of parameters are missing.)

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20240906_CorrelationTool.mp4#t=0.001" type="video/mp4"></video>

#### Focus on joint placement within the body

In 2024, most of my focus on parametrization revolved around the sensible placement of joints within creatures. For instance, in all creatures with knees, the knee joint is positioned closer to the front of the leg than the back. While the knee placement was fairly straightforward, determining the placement of hip, shoulder, and neck joints across creatures with vastly different proportions proved significantly more challenging.

Many of my reference 3D models looked sensible externally, but had questionable and inconsistent rigging (placement of joints) from an anatomical perspective.

[![[Clippings/attachments/0eb55219d0aaee945afc6e348ea2bd9b_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgiHHFFMVDAj-nKwCE9gLGD5qtVeftDIM4_4mounqUEpOIvCur-VVtLHo5gpzuMcVxPLl4q9iB_ZBy096YLLVwmulfcLpBANdm0t65Cy_jjpD9OquDcVfa-BjuIL_fnnAWvDvlUfr14p13K3oo4dxRl90tw_HTqSw-y_mJZSTQPc9RJelaE3dVadkogOPw/s1600/CatModelBadAnatomy.jpg)

Anatomical reference images of bones and joints in various animals were also frequently inconsistent. I could find detailed references from multiple angles for dogs, cats and horses, but not much else. For instance, depictions of crocodile anatomy varied greatly: Some showed the spine in the neck centered, while others placed it near the back of the neck.

[![[Clippings/attachments/6bac1342b517f6c33697633e5aaf3854_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjHx_buil4q3UP8IqXG76qtqzp7Hwc5hBQJ5vjL9GCoDQDWMDxwHcbPmN8rs-UVH3uklTzsoskDDNJ85y_VGv-vHxfkjDKpbBsYKn5FDDgB0hPzaZxlhRPCbm-gdBC3NyGEy_LFX3iuT-pBEWN55BSVHCppkV13MUIor4fFan0j_YSXwhOyPptvT7S4vMo/s1600/CrocodileComparison.jpg)

All of this uncertainty meant I was constantly second-guessing joint placement – both when contemplating how the procedural generation should work and when adding new example creatures. I wanted to solve this one and for all, so I could stop worrying about it.

Solving the joint placement would also simplify the process of adding additional example creatures, since I could just focus on making them look right "from the outside" without worrying about joints placement. Eventually, I did largely solve it. By this point, I had established 106 high-level parameters that controled all the 503 low-level parameters.

#### Speeding up creation of additional example creatures

Once joint placement was mostly automated, I come up with the idea of accelerating the creation of example creatures using Gradient Descent ([Wikipedia](https://en.wikipedia.org/wiki/Gradient_descent)). My goal was to implement a Gradient Descent-based tool that could automatically adjust creature parameters to make the creature match the shape of a reference 3D model.

To my surprise, the approach actually worked. In the video below, the tool I created adjusts the 106 parameters of a creature to align its shape with the silhouettes of a giraffe:

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20240913_GradientDescent.mp4#t=0.001" type="video/mp4"></video>

The tool works by capturing silhouettes from multiple angles of the reference model (once) and of the procedural model (at each step of the iterative Gradient Descent process). It calculates how different the procedural silhouettes are from the reference silhouettes, using this difference as the penalty function for the Gradient Descent.

To measure the difference between two silhouettes, the method creates a [Signed Distance Field](https://catlikecoding.com/sdf-toolkit/docs/texture-generator/) (SDF) from both silhouettes being compared. To speed up the process, I made my SDF-generator of choice Burst-compatible ([available here](https://gist.github.com/runevision/af22b9ea8dc5a9b432aa9af4924bc6c4)). For each pixel near the silhouette border (pixels with distance values close to zero) the process retrieves the corresponding pixel's distance value from the other SDF to determine how far away the other silhouette border is at that point. The penalty function sums these distances across all tested pixels in all silhouette pairs, yielding the overall penalty.

This explains why, in the video, the legs growing are the first feature to change. Increasing the leg lengths reduces the most distance penalties at once. After that, extending the neck length has the greatest impact.

Notably, the process doesn't get the ears of the giraffe right. The reference model has both ears and horns, while my generator can't create horns yet. So the Gradient Descent process, which aims to match the silhouettes as closely as possible, made the ears large and round so they effectively serve double duty as both ears and horns. I later worked around this by hiding the horns of the reference model.

I also experimented with a standard optimization method called the "Adam" optimizer, but the [results were not good](https://mastodon.gamedev.place/@runevision/113126701540691172). Ultimately, the automated process wasn't perfect, but it complemented my manual tweaks to speed up the creation of example creatures to some extent.

By this point, I had spent three months in 2024 working on procedural creature generation and had developed eleven example creatures covering a variety of shapes. I eventually scrapped the "extracted creatures" because the combination of high-level parametrization and Gradient Descent tooling made them unnecessary as an intermediate step.

[![[Clippings/attachments/469498d06905bd775df6934cf9faffa0_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEil-DDtRbH5oQ2oZKLeSpvLDuHSCFERINs6b2a1jo7zgNywAdWgtneTzY0jOE_dqml8HEeadJjyr9gKvu1JvOsGF5dEfCa8BHOa5NiP1gERJY8Fin7Yze6ExclRWaYLiBRx1Ve0p2j7bicYBIZ-UaBODF0ZUjONTfUG8j1525quhfkbWJ8haZIS5Oigw3w/s1600/ElevenCreatures.jpg)

However, I was not even close to a sufficient high-level parametrization yet. Feeling the need for a change of pace, I decided to shift my focus to the procedural animation of the creatures.

### Intermission

As I was writing this, I realized that while I’m convinced I haven’t yet achieved the goal of ensuring that "any random values for the parameters will always create valid creatures", I hadn’t actually put it to the test. So, I quickly wrote a script to assign random values to all the high-level parameters. These are the results:

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20250110_RandomCreatures_2024.mp4#t=0.001" type="video/mp4"></video>

While a few of the results look cool, most are not close to meeting my standards, as I expected. Still, this randomizer could prove useful going forward. It might help me identify which aspects of the generation are still insufficient and why, guiding my further refinement of the procedural generation.

Anyway, back to what happened in 2024.

### Procedural animation of creatures

When it comes to procedural animation, I have the advantage that I wrote my Master's Thesis in 2009 about [Automated Semi-Procedural Animation for Character Locomotion](https://runevision.com/tech/locomotion/), accompanied by an implementation called the *Locomotion System*. That was based on modifying hand-crafted animations to adapt to arbitrary paths and uneven terrain.

![](https://www.youtube.com/watch?v=v2q5kuic6HA)

Even before that, I implemented fully procedural (pre-rendered) animations as far back as in 2002 when I was 18.

![](https://www.youtube.com/watch?v=EehHVXjf1Sk)

In the summer of 2022, I tried to essentially recreate that, but this time in real-time and interactive. As a starting point, I used my 2009 Locomotion System, stripping out the parts related to traditional animation clips. Instead, I programmed the feet to simply move along basic arcs from one footstep position to the next. To test it, I manually created some programmer-art "creatures" with various leg configurations.

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20220817_CreatureAnimationMontage.mp4#t=0.001" type="video/mp4"></video>

In 2024, I resumed this work, now applying it to my procedurally generated creature models.

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20241024_DogWalkingStiff.mp4#t=0.001" type="video/mp4"></video>

The result looked somewhat nice but were rather stiff, and the approach only works for taking small steps. As I've touched on before, animating procedural, mammal-like creatures to look natural is a tough challenge:

- Quadruped mammals like cats, dogs, and horses move their limbs in more complex ways. Or at least, we're so familiar with their movements that any inaccuracies makes the movements look weird to us.
- Fast gaits, such as galloping, are more complicated than walking.
- The animation must control not only the legs, but also the spine, tail, neck, etc.
- Since the creatures are generated at runtime, the animation must work out of the box *without any manual tweaks* for individual creatures.

That's a tall order even with my experience, but hey, I like a good challenge.

My approach to procedural animation is purely kinematic, relying on forward kinematics (FK) and inverse kinematics (IK). This means I write code to directly control the motion of bodies and limbs without considering the forces that drive their movement. In other words, there’s no physics simulation involved and no training or evolutionary algorithms ([like this one](https://www.youtube.com/watch?v=pgaEE27nsQw)).

A training-based approach isn't viable for creatures generated at runtime, and frankly, I have no interest in pursuing it. The only way the animation interacts with the game engine’s physics system is by using ray casts to determine where footsteps should be placed on the ground.

#### Hilarity ensues

As an aside, one of the fun parts of working on procedural animation is that works in progress often look *goofy*. When I first applied the procedural animation to my procedurally generated creatures, I was impatient and ran it before implementing an interface to specify the timing of the different legs relative to each other. As I wrote on social media, *"It might be hard to believe, but this animation is actually 100% procedural."*

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20241024_JumpingDog.mp4#t=0.001" type="video/mp4"></video>

The system itself already supported leg timing, as it was inherited from the Locomotion System, where timing was automatically set based on analyzing animation clips. However, in the modified fully procedural version, I hadn't yet implemented a way to manually input the timing data. Once I did, things looked a lot more sensible, as shown in the previous video.

Other people's comments about the absurd animations sometimes inspire me to create more silly animations, just for fun. *"Somebody commented that the procedural spider and the procedural dog are destined to fight, but actually they are friends, they are best pals and like to go on adventures together."*

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20241025_SpiderAndDog.mp4#t=0.001" type="video/mp4"></video>

Around this time, I wanted to better evaluate my procedural animation by directly comparing it to hand-crafted animation. To do this, I applied the procedural animation to 3D models I had purchased from the Asset Store, comparing it to the included animation clips that came with those models.

Continuing the theme of goofiness, my first attempt at this comparison had a bug so hilariously absurd that it became my most viral post ever on [Twitter](https://x.com/runevision/status/1857823929575870911), [Bluesky](https://bsky.app/profile/runevision.bsky.social/post/3lb3cikpmzs2n) and [Mastodon](https://mastodon.gamedev.place/@runevision/113493586274443116). (The added music adds a lot to this one, so consider playing with sound on!)

![](https://www.youtube.com/watch?v=VxjwzIJghGs)

People would inevitably suggest, and sometimes even plead, that I bring this absurd silliness into the game I’m making, for fun and profit. While I understand the sentiment, the reality is that my vision for *The Big Forest* is not that kind of game. There's definitely room for some light-hearted moments, but that’s not the primary focus. For reference, think of a Ghibli movie – there’s a certain kind of silliness that would fit well there, but it would need to align with the overall tone.

#### Incremental progress and study

I started studying my procedural animation alongside the handcrafted animations to better understand the subtle but important differences. Here's the comparison tool I made again, this time without the hilarious bug.

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20241118_AnimalComparisonFixed.mp4#t=0.001" type="video/mp4"></video>

Even without the bug, it still looks very rough. At higher speeds, it becomes clear that the approach of simply moving the feet from one footstep position to the next doesn't work.

In real life (and in the reference animations), at high speeds like galloping, the feet don't stay in contact with the ground for most of their backward trajectories. They only touch the ground for short durations. My procedural animation didn't account for this yet. Instead, the hips got pulled down to be within distance of the feet, and that's what caused the torsos of the procedurally animated creatures to drag along the ground.

Once I tried to account for this, things improved slightly – at least in that the torsos no longer dragged along the ground.

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20241121_AnimationComparisonStepImprovement.mp4#t=0.001" type="video/mp4"></video>

To better make informed decisions about how far up the feet should lift, how much time they should spend touching the ground, and similar animation aspects, I developed a tool to plot various properties of the reference animations. For example, the plot below shows that as the stride distance (relative to the length of the leg) increases, the proportion of time the foot is in the air also increases. The white dotted curve represents my own equation that I attempted to fit to the data.

[![[Clippings/attachments/7b2645505047bf63b9c01f0e52faab3a_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj4hvpC9gl4OG7oNotQKC-A9m9aC2VKJgrcFHWrlG4xKW3UX7rbg5u7NrKIc9oIsZUk4AOy4z-Aomd5lfhBZ1LaT7get4i4uRpuozYud-gaG_sqf-iuSth3sodXos-ZHpGiFhYnBsaxdiBf9XJMILPYPiWbbnFSeSRl6k6MAHwoZQpXNpq726Ccz8s5oaU/s1600/FlightDurationNorm.jpg)

Below is another plot that shows the signed horizontal distance between the hip and the foot (actually, the *footstep position*) along the horizontal axis, and the foot's lift on the vertical axis. In the center, where the foot is directly below the hip, the lift is generally zero. Notably, the plot includes data from gaits at different speeds (walking, trotting, galloping), but the distance at which the foot lifts off the ground is fairly consistent across those speeds. So while higher speeds are associated with longer step lengths, the "distance" (relative to the creature) that a foot is in contact with the ground is not proportional to the step length. Instead, it it's closer to a constant value, relative to the leg length.

[![[Clippings/attachments/b015835cfcf98b61084b10e98b489591_MD5.jpg]]](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgiCdRVah6blNHFm0e2R4B1a1qZlgD6rxOGKhHlc8xDcvKhwyjb724g5QyUNA3mAWwgExZ7qyTrBl7zp5U8jXfOl1Ld7Sg0P0DlXqFKJ41RCl8gG_9Wj4Xhw7fMChuDEB506QycOBehUge4_mS0nwp46W_fMw77ju_7nJyhL03e4DdC_F3tQ6tmLASroAk/s1600/DistanceLift.jpg)

I made many plots with this tool, visualizing data from the reference animations in all kinds of ways. Some of the plots revealed clear trends, like the two above. Others resulted in a jumble of unrelated curves or dots that I couldn't use for anything. In this way, my process was (and is) very much a classic research approach: Formulating hypotheses, testing them, discarding those that don't pan out, and building upon the ones that do.

#### Inverse kinematics overhaul

I had noticed that many animals kind of bend or curl their feet – and sometimes the entire lower part of their front legs – when lifting them. However, my procedural animation didn't capture this behavior at all. I could hack around this by dynamically adjusting the foot rotations over the walk cycle, but it often resulted in unnatural poses.

Eventually, I concluded that I needed to revamp the inverse kinematics (IK) algorithm I was using, with focus on better handling foot roll and bending scenarios. My old Locomotion System employed a two-pass IK approach, where the foot rotation was given as input to the first IK pass. Based on the orientation of the lower leg found by the IK, the foot rotation would be adjusted – rotated around either the heel or toe – to ensure a more natural ankle angle, followed by a second IK pass to make the leg match the new ankle position. This two-pass approach worked all right for the Locomotion System, which was applied on top of hand-crafted animation. However, I found it insufficient for the fully procedural animation I was working on now.

In principle, this two-pass approach could be changed to run iteratively, rather than just twice. However, this would be computationally expensive, since the IK algorithm itself is already iterative. Instead, I implemented a new IK algorithm where the foot rotation is not a static input, but is controlled by the IK itself.

Having the IK handle the foot rotation is a bit tricky, as it must behave quite differently depending on how much weight is on the foot, ranging from none to full weight.

<video autobuffer="" loop="" controls="" playsinline="" data-vcaptions-target-video="1"><source src="https://runevision.com/blog/videos/20241213_IKHuman_SomeSnapping.mp4#t=0.001" type="video/mp4"></video>

I made significant progress with this approach, although there’s a tricky issue: There are edge cases where multiple solutions can satisfy the given constraints. This makes the leg poses, which are state-less, sometimes snap from one configuration to another based on even tiny changes in the input positions. I have some ideas on how to address this, but I haven't tested them yet.

After incorporating the new IK system and adding logic to make the feet bend when lifted, my results looked like this at the end of 2024:

<video autobuffer="" loop="" controls="" playsinline=""><source src="https://runevision.com/blog/videos/20241219_AnimationComparisonIKImprovements.mp4#t=0.001" type="video/mp4"></video>

While it's still a bit glitchy and far from perfect, the bending of the feet and legs is at least a step in the right direction.

### And that's how far I got so far

Both the procedural model generation and the procedural animation still have a long way to go, after spending around three months on each, and that can feel a bit demotivating. On the other hand, I've been making steady progress, even if it's slow. Writing this post has actually helped me realize just how much I've accomplished so far after all.

That said, I feel it's time for a break from the creatures. When I return to them later, I'll hopefully do so with renewed energy.

I wish I could have wrapped up this post with a satisfying milestone or a neat conclusion, but there was already so much to cover, and I didn't want to delay this write-up any further. I also think there's value in showing the messiness of creative processes and research. Let's see where I'm at when I write about the procedural creatures next time!

#### 5 comments:

[![[Clippings/attachments/1d4e8dd94bfb9469812a9e17a516b472_MD5.jpg]]

![](//blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgcdDQ0CG-RINbAQ9biRg3O2y5URplftGns0yrt1ytThD1qwTNOPqeTnIujoRIl7zv10VYj-BZk0miZY2YWCIcHA4r3WDTOvoVC0vuQPOehtgtkTU5K76bWn1HEWHzFDA/s45-c/frank_gennari_scaled2.jpg)

](https://www.blogger.com/profile/02815853731800103017)

[Frank Gennari](https://www.blogger.com/profile/02815853731800103017) said...

Wow, so much effort and so much progress! I'm really hoping that you can make some part of this a open project like your procedural world generation framework.  
  
I've experimented with procedural animations as well. I had success with insects, spiders, and that sort of thing. There are also many animated models of people and general bipedals that can be found online. But animals, in particular quadruped mammals, are definitely more challenging. They're familiar to most of us so it's more obvious when animations are wrong, but it's difficult to find good quality animated 3D models.  
  
I would love to have some animated cats and dogs to add to my projects though. Especially if I can get them in multiple species.

[January 11, 2025 at 2:19 AM](https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html?showComment=1736558340907#c7348016264533991679 "comment permalink") [![[Clippings/attachments/2e7aefe125fda9607507f2e7795eab19_MD5.gif]]](https://www.blogger.com/comment/delete/1667313809239009473/7348016264533991679 "Delete Comment") 

![](//resources.blogblog.com/img/blank.gif "Anonymous")

Anonymous said...

amazing work

[January 23, 2025 at 4:40 PM](https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html?showComment=1737646845705#c2873952208794442972 "comment permalink") [![[Clippings/attachments/2e7aefe125fda9607507f2e7795eab19_MD5.gif]]](https://www.blogger.com/comment/delete/1667313809239009473/2873952208794442972 "Delete Comment") 

![](//resources.blogblog.com/img/blank.gif "Anonymous")

Anonymous said...

Great work! I'm looking forward to the next progress update!

[February 10, 2025 at 12:09 PM](https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html?showComment=1739185781436#c7021270667009111924 "comment permalink") [![[Clippings/attachments/2e7aefe125fda9607507f2e7795eab19_MD5.gif]]](https://www.blogger.com/comment/delete/1667313809239009473/7021270667009111924 "Delete Comment") 

[![[Clippings/attachments/a9d5417aede27cc5533e9a5ee8ffe0c6_MD5.jpg]]

![](//blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhKT8WfAFa_IAhreHc8851dTi8OqJtnSbrTmrk0Ih16WO-WN-JmtecV0VGsJH-tV56lVRZ2oKPyYokPeO0Q_gFx5YDiMhJ_Rl7zWaCLOPbd9ZXp2rjZnCIt9QZYXzBuG6jisP8/s45-c/fantasy-planet-art.jpg)

](https://www.blogger.com/profile/06943966639483256507)

[JonathanCR](https://www.blogger.com/profile/06943966639483256507) said...

This is great stuff! Keep up the good work. I'll be really interested to see how this develops.

[April 9, 2025 at 5:06 PM](https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html?showComment=1744211185019#c5764912088925822436 "comment permalink") [![[Clippings/attachments/2e7aefe125fda9607507f2e7795eab19_MD5.gif]]](https://www.blogger.com/comment/delete/1667313809239009473/5764912088925822436 "Delete Comment") 

![](//resources.blogblog.com/img/blank.gif "Anonymous")

Anonymous said...

Adding movement to the spine & hips should get you pretty close to reference animations, keep up the good work.

[August 13, 2026 at 1:07 AM](https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html?showComment=1786576067302#c7968464637622927970 "comment permalink") [![[Clippings/attachments/2e7aefe125fda9607507f2e7795eab19_MD5.gif]]](https://www.blogger.com/comment/delete/1667313809239009473/7968464637622927970 "Delete Comment") 

[Post a Comment](https://www.blogger.com/comment/fullpage/post/1667313809239009473/4949056993255103046)

[« Newer Post](https://blog.runevision.com/2025/06/photos-from-inspiring-trip-in-japan.html "Newer Post") [Older Post »](https://blog.runevision.com/2025/01/2024-retrospective.html "Older Post")

Copyright 2026 Rune Skovbo Johansen

- [Bluesky](https://bsky.app/profile/runevision.bsky.social)
- [Mastodon](https://mastodon.gamedev.place/@runevision)
- [YouTube](https://www.youtube.com/c/runevision)

- [Blog](https://blog.runevision.com/)
- [Games](https://runevision.com/multimedia/)
- [Articles](https://runevision.com/articles/)
- [Tools & Tech](https://runevision.com/tech/)
- [Graphics & Animations](https://runevision.com/graphics/)
- [About Me](https://runevision.com/about/)

- [Bluesky](https://bsky.app/profile/runevision.bsky.social)
- [Mastodon](https://mastodon.gamedev.place/@runevision)
- [YouTube](https://www.youtube.com/c/runevision)

Blog Archive

- [►](javascript:void\(0\))  [2026](https://blog.runevision.com/2026/) (4)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2026/07/) (1)
		- [►](javascript:void\(0\))  [Jul 29](https://blog.runevision.com/2026_07_29_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2026/06/) (1)
		- [►](javascript:void\(0\))  [Jun 14](https://blog.runevision.com/2026_06_14_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2026/03/) (1)
		- [►](javascript:void\(0\))  [Mar 30](https://blog.runevision.com/2026_03_30_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2026/01/) (1)
		- [►](javascript:void\(0\))  [Jan 22](https://blog.runevision.com/2026_01_22_archive.html) (1)
- [▼](javascript:void\(0\))  [2025](https://blog.runevision.com/2025/) (5)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2025/10/) (1)
		- [►](javascript:void\(0\))  [Oct 23](https://blog.runevision.com/2025_10_23_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2025/06/) (2)
		- [►](javascript:void\(0\))  [Jun 29](https://blog.runevision.com/2025_06_29_archive.html) (1)
		- [►](javascript:void\(0\))  [Jun 27](https://blog.runevision.com/2025_06_27_archive.html) (1)
	- [▼](javascript:void\(0\))  [January](https://blog.runevision.com/2025/01/) (2)
		- [▼](javascript:void\(0\))  [Jan 10](https://blog.runevision.com/2025_01_10_archive.html) (1)
			- [Procedural creature progress 2021 - 2024](https://blog.runevision.com/2025/01/procedural-creature-progress-2021-2024.html)
		- [►](javascript:void\(0\))  [Jan 05](https://blog.runevision.com/2025_01_05_archive.html) (1)
- [►](javascript:void\(0\))  [2024](https://blog.runevision.com/2024/) (3)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2024/10/) (1)
		- [►](javascript:void\(0\))  [Oct 02](https://blog.runevision.com/2024_10_02_archive.html) (1)
	- [►](javascript:void\(0\))  [August](https://blog.runevision.com/2024/08/) (1)
		- [►](javascript:void\(0\))  [Aug 18](https://blog.runevision.com/2024_08_18_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2024/01/) (1)
		- [►](javascript:void\(0\))  [Jan 08](https://blog.runevision.com/2024_01_08_archive.html) (1)
- [►](javascript:void\(0\))  [2023](https://blog.runevision.com/2023/) (2)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2023/09/) (1)
		- [►](javascript:void\(0\))  [Sep 15](https://blog.runevision.com/2023_09_15_archive.html) (1)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2023/05/) (1)
		- [►](javascript:void\(0\))  [May 06](https://blog.runevision.com/2023_05_06_archive.html) (1)
- [►](javascript:void\(0\))  [2022](https://blog.runevision.com/2022/) (1)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2022/10/) (1)
		- [►](javascript:void\(0\))  [Oct 14](https://blog.runevision.com/2022_10_14_archive.html) (1)
- [►](javascript:void\(0\))  [2021](https://blog.runevision.com/2021/) (2)
	- [►](javascript:void\(0\))  [November](https://blog.runevision.com/2021/11/) (1)
		- [►](javascript:void\(0\))  [Nov 22](https://blog.runevision.com/2021_11_22_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2021/02/) (1)
		- [►](javascript:void\(0\))  [Feb 08](https://blog.runevision.com/2021_02_08_archive.html) (1)
- [►](javascript:void\(0\))  [2020](https://blog.runevision.com/2020/) (2)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2020/12/) (2)
		- [►](javascript:void\(0\))  [Dec 09](https://blog.runevision.com/2020_12_09_archive.html) (1)
		- [►](javascript:void\(0\))  [Dec 04](https://blog.runevision.com/2020_12_04_archive.html) (1)
- [►](javascript:void\(0\))  [2019](https://blog.runevision.com/2019/) (1)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2019/12/) (1)
		- [►](javascript:void\(0\))  [Dec 31](https://blog.runevision.com/2019_12_31_archive.html) (1)
- [►](javascript:void\(0\))  [2018](https://blog.runevision.com/2018/) (5)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2018/09/) (1)
		- [►](javascript:void\(0\))  [Sep 17](https://blog.runevision.com/2018_09_17_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2018/07/) (1)
		- [►](javascript:void\(0\))  [Jul 14](https://blog.runevision.com/2018_07_14_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2018/04/) (1)
		- [►](javascript:void\(0\))  [Apr 22](https://blog.runevision.com/2018_04_22_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2018/03/) (1)
		- [►](javascript:void\(0\))  [Mar 20](https://blog.runevision.com/2018_03_20_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2018/01/) (1)
		- [►](javascript:void\(0\))  [Jan 30](https://blog.runevision.com/2018_01_30_archive.html) (1)
- [►](javascript:void\(0\))  [2017](https://blog.runevision.com/2017/) (6)
	- [►](javascript:void\(0\))  [August](https://blog.runevision.com/2017/08/) (1)
		- [►](javascript:void\(0\))  [Aug 03](https://blog.runevision.com/2017_08_03_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2017/06/) (1)
		- [►](javascript:void\(0\))  [Jun 13](https://blog.runevision.com/2017_06_13_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2017/04/) (1)
		- [►](javascript:void\(0\))  [Apr 02](https://blog.runevision.com/2017_04_02_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2017/02/) (1)
		- [►](javascript:void\(0\))  [Feb 21](https://blog.runevision.com/2017_02_21_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2017/01/) (2)
		- [►](javascript:void\(0\))  [Jan 30](https://blog.runevision.com/2017_01_30_archive.html) (1)
		- [►](javascript:void\(0\))  [Jan 04](https://blog.runevision.com/2017_01_04_archive.html) (1)
- [►](javascript:void\(0\))  [2016](https://blog.runevision.com/2016/) (6)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2016/12/) (1)
		- [►](javascript:void\(0\))  [Dec 04](https://blog.runevision.com/2016_12_04_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2016/09/) (2)
		- [►](javascript:void\(0\))  [Sep 27](https://blog.runevision.com/2016_09_27_archive.html) (1)
		- [►](javascript:void\(0\))  [Sep 06](https://blog.runevision.com/2016_09_06_archive.html) (1)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2016/05/) (1)
		- [►](javascript:void\(0\))  [May 03](https://blog.runevision.com/2016_05_03_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2016/04/) (1)
		- [►](javascript:void\(0\))  [Apr 05](https://blog.runevision.com/2016_04_05_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2016/03/) (1)
		- [►](javascript:void\(0\))  [Mar 01](https://blog.runevision.com/2016_03_01_archive.html) (1)
- [►](javascript:void\(0\))  [2015](https://blog.runevision.com/2015/) (4)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2015/12/) (1)
		- [►](javascript:void\(0\))  [Dec 22](https://blog.runevision.com/2015_12_22_archive.html) (1)
	- [►](javascript:void\(0\))  [November](https://blog.runevision.com/2015/11/) (1)
		- [►](javascript:void\(0\))  [Nov 21](https://blog.runevision.com/2015_11_21_archive.html) (1)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2015/10/) (1)
		- [►](javascript:void\(0\))  [Oct 10](https://blog.runevision.com/2015_10_10_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2015/01/) (1)
		- [►](javascript:void\(0\))  [Jan 01](https://blog.runevision.com/2015_01_01_archive.html) (1)
- [►](javascript:void\(0\))  [2014](https://blog.runevision.com/2014/) (8)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2014/12/) (1)
		- [►](javascript:void\(0\))  [Dec 18](https://blog.runevision.com/2014_12_18_archive.html) (1)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2014/10/) (1)
		- [►](javascript:void\(0\))  [Oct 18](https://blog.runevision.com/2014_10_18_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2014/09/) (3)
		- [►](javascript:void\(0\))  [Sep 25](https://blog.runevision.com/2014_09_25_archive.html) (1)
		- [►](javascript:void\(0\))  [Sep 13](https://blog.runevision.com/2014_09_13_archive.html) (1)
		- [►](javascript:void\(0\))  [Sep 06](https://blog.runevision.com/2014_09_06_archive.html) (1)
	- [►](javascript:void\(0\))  [August](https://blog.runevision.com/2014/08/) (1)
		- [►](javascript:void\(0\))  [Aug 31](https://blog.runevision.com/2014_08_31_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2014/07/) (1)
		- [►](javascript:void\(0\))  [Jul 17](https://blog.runevision.com/2014_07_17_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2014/06/) (1)
		- [►](javascript:void\(0\))  [Jun 24](https://blog.runevision.com/2014_06_24_archive.html) (1)
- [►](javascript:void\(0\))  [2013](https://blog.runevision.com/2013/) (4)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2013/09/) (1)
		- [►](javascript:void\(0\))  [Sep 22](https://blog.runevision.com/2013_09_22_archive.html) (1)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2013/05/) (1)
		- [►](javascript:void\(0\))  [May 02](https://blog.runevision.com/2013_05_02_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2013/02/) (2)
		- [►](javascript:void\(0\))  [Feb 17](https://blog.runevision.com/2013_02_17_archive.html) (1)
		- [►](javascript:void\(0\))  [Feb 16](https://blog.runevision.com/2013_02_16_archive.html) (1)
- [►](javascript:void\(0\))  [2012](https://blog.runevision.com/2012/) (3)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2012/05/) (1)
		- [►](javascript:void\(0\))  [May 15](https://blog.runevision.com/2012_05_15_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2012/04/) (1)
		- [►](javascript:void\(0\))  [Apr 23](https://blog.runevision.com/2012_04_23_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2012/03/) (1)
		- [►](javascript:void\(0\))  [Mar 09](https://blog.runevision.com/2012_03_09_archive.html) (1)
- [►](javascript:void\(0\))  [2011](https://blog.runevision.com/2011/) (10)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2011/12/) (4)
		- [►](javascript:void\(0\))  [Dec 24](https://blog.runevision.com/2011_12_24_archive.html) (1)
		- [►](javascript:void\(0\))  [Dec 23](https://blog.runevision.com/2011_12_23_archive.html) (1)
		- [►](javascript:void\(0\))  [Dec 20](https://blog.runevision.com/2011_12_20_archive.html) (1)
		- [►](javascript:void\(0\))  [Dec 18](https://blog.runevision.com/2011_12_18_archive.html) (1)
	- [►](javascript:void\(0\))  [November](https://blog.runevision.com/2011/11/) (1)
		- [►](javascript:void\(0\))  [Nov 23](https://blog.runevision.com/2011_11_23_archive.html) (1)
	- [►](javascript:void\(0\))  [August](https://blog.runevision.com/2011/08/) (3)
		- [►](javascript:void\(0\))  [Aug 21](https://blog.runevision.com/2011_08_21_archive.html) (1)
		- [►](javascript:void\(0\))  [Aug 15](https://blog.runevision.com/2011_08_15_archive.html) (1)
		- [►](javascript:void\(0\))  [Aug 10](https://blog.runevision.com/2011_08_10_archive.html) (1)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2011/05/) (2)
		- [►](javascript:void\(0\))  [May 29](https://blog.runevision.com/2011_05_29_archive.html) (1)
		- [►](javascript:void\(0\))  [May 20](https://blog.runevision.com/2011_05_20_archive.html) (1)
- [►](javascript:void\(0\))  [2010](https://blog.runevision.com/2010/) (10)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2010/12/) (1)
		- [►](javascript:void\(0\))  [Dec 22](https://blog.runevision.com/2010_12_22_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2010/09/) (1)
		- [►](javascript:void\(0\))  [Sep 15](https://blog.runevision.com/2010_09_15_archive.html) (1)
	- [►](javascript:void\(0\))  [August](https://blog.runevision.com/2010/08/) (3)
		- [►](javascript:void\(0\))  [Aug 11](https://blog.runevision.com/2010_08_11_archive.html) (1)
		- [►](javascript:void\(0\))  [Aug 08](https://blog.runevision.com/2010_08_08_archive.html) (1)
		- [►](javascript:void\(0\))  [Aug 04](https://blog.runevision.com/2010_08_04_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2010/07/) (1)
		- [►](javascript:void\(0\))  [Jul 29](https://blog.runevision.com/2010_07_29_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2010/06/) (1)
		- [►](javascript:void\(0\))  [Jun 14](https://blog.runevision.com/2010_06_14_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2010/03/) (1)
		- [►](javascript:void\(0\))  [Mar 14](https://blog.runevision.com/2010_03_14_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2010/02/) (2)
		- [►](javascript:void\(0\))  [Feb 11](https://blog.runevision.com/2010_02_11_archive.html) (1)
		- [►](javascript:void\(0\))  [Feb 04](https://blog.runevision.com/2010_02_04_archive.html) (1)
- [►](javascript:void\(0\))  [2009](https://blog.runevision.com/2009/) (7)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2009/09/) (1)
		- [►](javascript:void\(0\))  [Sep 06](https://blog.runevision.com/2009_09_06_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2009/04/) (1)
		- [►](javascript:void\(0\))  [Apr 18](https://blog.runevision.com/2009_04_18_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2009/03/) (4)
		- [►](javascript:void\(0\))  [Mar 31](https://blog.runevision.com/2009_03_31_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 19](https://blog.runevision.com/2009_03_19_archive.html) (3)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2009/02/) (1)
		- [►](javascript:void\(0\))  [Feb 16](https://blog.runevision.com/2009_02_16_archive.html) (1)
- [►](javascript:void\(0\))  [2008](https://blog.runevision.com/2008/) (16)
	- [►](javascript:void\(0\))  [November](https://blog.runevision.com/2008/11/) (1)
		- [►](javascript:void\(0\))  [Nov 01](https://blog.runevision.com/2008_11_01_archive.html) (1)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2008/10/) (2)
		- [►](javascript:void\(0\))  [Oct 27](https://blog.runevision.com/2008_10_27_archive.html) (1)
		- [►](javascript:void\(0\))  [Oct 15](https://blog.runevision.com/2008_10_15_archive.html) (1)
	- [►](javascript:void\(0\))  [August](https://blog.runevision.com/2008/08/) (1)
		- [►](javascript:void\(0\))  [Aug 08](https://blog.runevision.com/2008_08_08_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2008/07/) (2)
		- [►](javascript:void\(0\))  [Jul 20](https://blog.runevision.com/2008_07_20_archive.html) (2)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2008/06/) (3)
		- [►](javascript:void\(0\))  [Jun 22](https://blog.runevision.com/2008_06_22_archive.html) (1)
		- [►](javascript:void\(0\))  [Jun 21](https://blog.runevision.com/2008_06_21_archive.html) (1)
		- [►](javascript:void\(0\))  [Jun 10](https://blog.runevision.com/2008_06_10_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2008/03/) (6)
		- [►](javascript:void\(0\))  [Mar 27](https://blog.runevision.com/2008_03_27_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 19](https://blog.runevision.com/2008_03_19_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 18](https://blog.runevision.com/2008_03_18_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 11](https://blog.runevision.com/2008_03_11_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 04](https://blog.runevision.com/2008_03_04_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 03](https://blog.runevision.com/2008_03_03_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2008/02/) (1)
		- [►](javascript:void\(0\))  [Feb 06](https://blog.runevision.com/2008_02_06_archive.html) (1)
- [►](javascript:void\(0\))  [2007](https://blog.runevision.com/2007/) (5)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2007/12/) (1)
		- [►](javascript:void\(0\))  [Dec 22](https://blog.runevision.com/2007_12_22_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2007/06/) (1)
		- [►](javascript:void\(0\))  [Jun 30](https://blog.runevision.com/2007_06_30_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2007/04/) (1)
		- [►](javascript:void\(0\))  [Apr 24](https://blog.runevision.com/2007_04_24_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2007/03/) (1)
		- [►](javascript:void\(0\))  [Mar 31](https://blog.runevision.com/2007_03_31_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2007/02/) (1)
		- [►](javascript:void\(0\))  [Feb 03](https://blog.runevision.com/2007_02_03_archive.html) (1)
- [►](javascript:void\(0\))  [2005](https://blog.runevision.com/2005/) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2005/04/) (1)
		- [►](javascript:void\(0\))  [Apr 12](https://blog.runevision.com/2005_04_12_archive.html) (1)
- [►](javascript:void\(0\))  [2004](https://blog.runevision.com/2004/) (10)
	- [►](javascript:void\(0\))  [November](https://blog.runevision.com/2004/11/) (1)
		- [►](javascript:void\(0\))  [Nov 01](https://blog.runevision.com/2004_11_01_archive.html) (1)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2004/10/) (1)
		- [►](javascript:void\(0\))  [Oct 05](https://blog.runevision.com/2004_10_05_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2004/09/) (1)
		- [►](javascript:void\(0\))  [Sep 08](https://blog.runevision.com/2004_09_08_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2004/07/) (1)
		- [►](javascript:void\(0\))  [Jul 03](https://blog.runevision.com/2004_07_03_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2004/04/) (2)
		- [►](javascript:void\(0\))  [Apr 27](https://blog.runevision.com/2004_04_27_archive.html) (1)
		- [►](javascript:void\(0\))  [Apr 04](https://blog.runevision.com/2004_04_04_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2004/03/) (2)
		- [►](javascript:void\(0\))  [Mar 09](https://blog.runevision.com/2004_03_09_archive.html) (1)
		- [►](javascript:void\(0\))  [Mar 07](https://blog.runevision.com/2004_03_07_archive.html) (1)
	- [►](javascript:void\(0\))  [February](https://blog.runevision.com/2004/02/) (1)
		- [►](javascript:void\(0\))  [Feb 27](https://blog.runevision.com/2004_02_27_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2004/01/) (1)
		- [►](javascript:void\(0\))  [Jan 29](https://blog.runevision.com/2004_01_29_archive.html) (1)
- [►](javascript:void\(0\))  [2003](https://blog.runevision.com/2003/) (4)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2003/12/) (1)
		- [►](javascript:void\(0\))  [Dec 03](https://blog.runevision.com/2003_12_03_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2003/09/) (1)
		- [►](javascript:void\(0\))  [Sep 28](https://blog.runevision.com/2003_09_28_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2003/07/) (1)
		- [►](javascript:void\(0\))  [Jul 25](https://blog.runevision.com/2003_07_25_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2003/06/) (1)
		- [►](javascript:void\(0\))  [Jun 24](https://blog.runevision.com/2003_06_24_archive.html) (1)
- [►](javascript:void\(0\))  [2002](https://blog.runevision.com/2002/) (8)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2002/10/) (1)
		- [►](javascript:void\(0\))  [Oct 19](https://blog.runevision.com/2002_10_19_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2002/09/) (1)
		- [►](javascript:void\(0\))  [Sep 08](https://blog.runevision.com/2002_09_08_archive.html) (1)
	- [►](javascript:void\(0\))  [July](https://blog.runevision.com/2002/07/) (1)
		- [►](javascript:void\(0\))  [Jul 12](https://blog.runevision.com/2002_07_12_archive.html) (1)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2002/05/) (1)
		- [►](javascript:void\(0\))  [May 20](https://blog.runevision.com/2002_05_20_archive.html) (1)
	- [►](javascript:void\(0\))  [April](https://blog.runevision.com/2002/04/) (1)
		- [►](javascript:void\(0\))  [Apr 14](https://blog.runevision.com/2002_04_14_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2002/03/) (1)
		- [►](javascript:void\(0\))  [Mar 19](https://blog.runevision.com/2002_03_19_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2002/01/) (2)
		- [►](javascript:void\(0\))  [Jan 20](https://blog.runevision.com/2002_01_20_archive.html) (1)
		- [►](javascript:void\(0\))  [Jan 12](https://blog.runevision.com/2002_01_12_archive.html) (1)
- [►](javascript:void\(0\))  [2001](https://blog.runevision.com/2001/) (8)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2001/12/) (1)
		- [►](javascript:void\(0\))  [Dec 19](https://blog.runevision.com/2001_12_19_archive.html) (1)
	- [►](javascript:void\(0\))  [November](https://blog.runevision.com/2001/11/) (1)
		- [►](javascript:void\(0\))  [Nov 05](https://blog.runevision.com/2001_11_05_archive.html) (1)
	- [►](javascript:void\(0\))  [September](https://blog.runevision.com/2001/09/) (1)
		- [►](javascript:void\(0\))  [Sep 26](https://blog.runevision.com/2001_09_26_archive.html) (1)
	- [►](javascript:void\(0\))  [June](https://blog.runevision.com/2001/06/) (1)
		- [►](javascript:void\(0\))  [Jun 26](https://blog.runevision.com/2001_06_26_archive.html) (1)
	- [►](javascript:void\(0\))  [May](https://blog.runevision.com/2001/05/) (1)
		- [►](javascript:void\(0\))  [May 10](https://blog.runevision.com/2001_05_10_archive.html) (1)
	- [►](javascript:void\(0\))  [March](https://blog.runevision.com/2001/03/) (1)
		- [►](javascript:void\(0\))  [Mar 29](https://blog.runevision.com/2001_03_29_archive.html) (1)
	- [►](javascript:void\(0\))  [January](https://blog.runevision.com/2001/01/) (2)
		- [►](javascript:void\(0\))  [Jan 28](https://blog.runevision.com/2001_01_28_archive.html) (1)
		- [►](javascript:void\(0\))  [Jan 06](https://blog.runevision.com/2001_01_06_archive.html) (1)
- [►](javascript:void\(0\))  [2000](https://blog.runevision.com/2000/) (2)
	- [►](javascript:void\(0\))  [December](https://blog.runevision.com/2000/12/) (1)
		- [►](javascript:void\(0\))  [Dec 17](https://blog.runevision.com/2000_12_17_archive.html) (1)
	- [►](javascript:void\(0\))  [October](https://blog.runevision.com/2000/10/) (1)
		- [►](javascript:void\(0\))  [Oct 09](https://blog.runevision.com/2000_10_09_archive.html) (1)