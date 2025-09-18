---
date: "2025-08-10T22:13:41+08:00"
url: "https://www.physicswithelliot.com/orbits-mini-notes"
status:
---
## Deriving the Orbit of Our Home Planet: Physics Mini Lesson

![](https://www.youtube.com/watch?v=wLYZsO6lk0E)

Throughout human history, astronomers have been gazing up at the sky and trying to understand our place in the universe—or in the solar system, for that matter. It wasn't until the early 1600s, though, that Johannes Kepler showed that the planets in our solar system orbit the Sun in ellipses with the Sun at one focus, based on data collected by Tycho Brahe. And it was not until the end of that century that Isaac Newton showed how those elliptical orbits could be *predicted* from his inverse-square law of gravity.

In my [previous video](https://www.physicswithelliot.com/potential-help-room-notes), I showed you how we can understand the elliptical shape of a planet's orbit very quickly by sketching a picture called the **effective potential**, which you can see in this animation:

E

r

U <sub>eff</sub>

E

The plot shows the effective potential as a function of the distance $r$ between the planet and the star. If you think of the curve like a hill with a particle sliding along it, you can see that for a planet whose energy lies between the minimum of the hill and zero, the radial coordinate will rock back and forth between its maximum and minimum values—the points of farthest and closest approach to the star. You'll calculate those distances in the [problem sheet](https://www.physicswithelliot.com/s/orbits-mini-problem-sheet.pdf). All the while, the planet swings around the star in the angular direction. The resulting shape of the orbit is an ellipse, and you can see how the shape changes by dragging the slider in the animation that controls the energy of the planet. Press start to watch the orbit.

In that video I didn't *prove* to you that the shape of the orbit is an ellipse, though, or give you the mathematical function that describes the orbit. So right now we're going to learn how to derive the orbit of a planet around a star using Newton's law of gravity.

I think this is pretty incredible—with really just a few lines of math we're going to derive the orbit of our home planet around our star. So I hope you're excited to see this worked out, especially if you've never seen it before, and without further ado let's get into it.

![[Read It Later/attachments/2c0df50072f5b9999f11d587ce331d7d_MD5.png]]

Here's the setup. We've got a star like the Sun, which we'll say has mass $M$ , and a planet like the Earth of mass $m$ . And we'll treat them both as point particles for simplicity here. Let's put the star at the origin of our coordinate system, and say the planet is some distance $r$ away. Then according to Newton's law of gravitation, there's going to be a force on the planet given by

$$
F=−GMmr2.
$$

The force points back toward the star at the origin, which is why there's a minus sign. $G$ here is the gravitational constant, which measures the strength of the gravitational force. The quantity $GMm$ is going to show up a lot, so let's define $k=GMm$ for short.

Of course, there's also going to be an equal-but-opposite gravitational force on the star pulling *it* toward the planet. But assuming that the star is much more massive than the planet, the same force that causes a big acceleration of the planet doesn't have much effect at all on the star. For the Earth and Sun, for example, $Mm≈3×105$ , meaning that the Sun is around 300,000 times more massive than the Earth. So it's a good approximation to say that the star just remains at rest at the origin.

![[Read It Later/attachments/fff19693600a0a956921e65a5a812d64_MD5.png]]

Say that at $t=0$ the planet is at position $r0→$ and has velocity $v0→$ . Then the question we want to answer is: what path will it follow for $t>0$ ? Let's set up our coordinates so that $r0→$ and $v0→$ lie in the $xy$ plane. Then the first thing to notice is that *the motion will be confined to the $xy$ plane*. In other words, if the $z$ coordinate of the planet was zero at $t=0$ , then it will remain zero forever!

This remarkable property arises from the fact that the gravitational force only depends on how far the planet is from the origin. Beyond that, it doesn't matter if the planet's to the right or left or top or bottom of the star—only the distance $r$ matters. In other words, the force is *spherically symmetric*. The basic reason this means that the planet is stuck in the $xy$ plane is that, at $t=0$ , the position $r0→$ , the velocity $v0→$ , and the force on the planet $F0→$ are *all* pointing in the $xy$ plane—nothing points, or has any component at all, in the $z$ direction. Say the planet *did* leave the $xy$ plane after $t=0$ . Which direction would it go in: up or down? We have complete symmetry here between the $+z$ and $−z$ directions, so the planet *can't* pick one or the other. It has to stay in the $xy$ plane.

For a more mathematical proof of this fact, define the **angular momentum** vector $L→$ by

$$
L→=mr→×v→.
$$

The $×$ here stands for the **cross product** of the vectors $r→$ and $v→$ . It returns a new vector which points *perpendicular* to both $r→$ and $v→$ (i.e. along the $z$ direction in this case), and the magnitude is the length of $r→$ times the length of the *piece* of $v→$ which is perpendicular to $r→$ , call it $v⊥$ :

![[Read It Later/attachments/2d2029532dbe3de46b6e2d5a45dd211a_MD5.png]]

Notice that if two vectors are parallel, then there *is* no perpendicular component of one along the other, and so the cross product is *zero*.

If you've never encountered the angular momentum vector $L→$ before, it might seem like a peculiar definition. Why is it physically useful? For the moment, it's useful because it's *constant* for the planet. Let's check: we'll take the rate of change of $L→(t)=mr→(t)×v→(t)$ with respect to time. Since both $r→(t)$ and $v→(t)$ depend on $t$ , we need to remember to apply the product rule:

$$
dL→dt=mv→×v→+mr→×a→,
$$

where $v→=dr→dt$ is again the velocity, and $a→=dv→dt$ is the acceleration.

I claim that both terms vanish here. The first term is zero for the reason we just stated: the cross product vanishes when the two vectors are parallel. And of course $v→$ is parallel to itself, so $v→×v→$ = 0. As for the second term, note that $ma→$ is the force $F→$ on the planet. But $F→$ points along the same line as $r→$ , just in the opposite direction—it points back towards the origin. Then $F→$ and $r→$ lie along the same line, there is no perpendicular component of one along the other, and the cross product again vanishes.

Therefore $dL→dt=0$ , and the angular momentum is constant!

$$
L→=mrv⊥ in the z direction=constant.
$$

Now how does that fact show that the motion of the planet is confined to the $xy$ plane? Again, the definition of the cross product says that $L→=mr→×v→$ is perpendicular to both $r→$ and $v→$ . Then since $L→$ is permanently pointed along $z$ , both $r→(t)$ and $v→(t)$ always have to point in the $xy$ plane if they're to remain perpendicular to $L→$ !

This is a huge simplification: instead of having to solve a fully 3-dimensional problem, we only have to solve a 2D problem! Our job, then, is to figure out the curve $r(θ)$ traced out by the planet as it moves around the $xy$ plane. To do this, remember that the angular momentum $L→$ isn't the only quantity we know of that's constant in time as the planet travels around. The total *energy* is also constant:

$$
E=K+U=constant.
$$

From the gravitational force $F=−kr2$ , we get the gravitational potential energy

$$
U=−kr,
$$

where remember we defined $k=GMm$ . The kinetic energy, meanwhile, is

$$
K=12mv2,
$$

where $v$ is the speed of the planet. There's two components to the speed here; in $x$ $y$ coordinates, we'd have the velocity $dxdt$ in the $x$ direction and the velocity $dydt$ in the $y$ direction. In this case, though, it's more convenient to use polar coordinates $r$ and $θ$ . Then we have the radial component of the velocity $drdt$ and the angular component $rdθdt$ . This last is just like the usual relation $v=ωr$ for a particle moving around in a circle, where $ω=dθdt$ .

Then the kinetic energy of the planet is

$$
K=12m(drdt)2+12mr2(dθdt)2,
$$

and the constant, total energy is

$$
E=12m(drdt)2+12mr2(dθdt)2−kr.
$$

The constant magnitude of the angular momentum $L=mrv⊥$ is meanwhile

$$
L=mr2dθdt,
$$

since the component $v⊥$ of the velocity that's perpendicular to the radial direction is the angular component, $v⊥=rdθdt$ . The fact that $L$ is constant means that the larger $r$ is, the smaller the angular speed will be, and vice-versa. So the planet whips around in the angular direction fastest when it's closest to the star, and more slowly when it's far away.

We can flip this equation around to write

$$
dθdt=Lmr2.
$$

Now if we plug this into the energy equation, it enables us to write $E$ in terms of the radial coordinate alone:

$$
E=12m(drdt)2+L22mr2−kr.
$$

This looks like the energy of a particle moving in one dimension $r$ , with the effective potential

$$
Ueff=−kr+L22mr2
$$

that we talked about [last time](https://www.physicswithelliot.com/potential-help-room-notes). The effective potential lets you see the general shape the orbit will take depending on how much energy the planet has, which you can control with the slider in the animation at the top of the page.

Remember, our goal here is to solve for the equation of the orbit $r(θ).$ At this stage we have two equations, one for $dθdt=Lmr2$ from the angular momentum $L$ , and one for $drdt$ from the energy $E$ , which we can rearrange as

$$
(drdt)2=2Em−L2m2r2+2kmr.
$$

But we're not actually too interested in the $t$ dependence here, so let's take this equation for $(drdt)2$ and divide it by $(dθdt)2$ . Then the $dt$ 's cancel out, and we're left with

$$
(Lmr2)2(drdθ)2=2Em−L2m2r2+2kmr.
$$

That's looking better! Now we have a differential equation for $r(θ)$ , and we can try to solve it to figure out the orbit.

[Next Page →](https://www.physicswithelliot.com/orbits-mini-notes-page-2)

1 [2](https://www.physicswithelliot.com/orbits-mini-notes-page-2)

---

See also:

- [The Trick That Makes Understanding Physics as Simple as Drawing a Picture: Physics Help Room](https://www.physicswithelliot.com/potential-help-room-notes)
- [The Shortcut that Lets You Write Down the Orbit of a Planet in One Line: Physics Mini Lesson](https://www.physicswithelliot.com/runge-lenz-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).