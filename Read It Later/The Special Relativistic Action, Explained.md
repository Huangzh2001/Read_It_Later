---
date: "2025-08-10T22:09:41+08:00"
url: "https://www.physicswithelliot.com/special-relativity-action-mini-notes"
status:
---
## The Special Relativistic Action, Explained: Physics Mini Lesson

![](https://www.youtube.com/watch?v=KVk1QNTWBxQ)

In this physics mini lesson, I'm going to explain the principle of least action that describes a particle in Einstein's theory of special relativity. In the [last mini lesson](https://www.physicswithelliot.com/least-action-mini-notes), we looked at the principle of least action for a particle in Newtonian mechanics, which says that of all the paths that a particle could take in traveling from point A to point B, the one that it actually chooses is the path for which this number called the action is minimized.

The action that we wrote down was the integral along the path of the kinetic energy minus the potential energy. That seemed like a sort of random definition, but we saw that minimizing this quantity indeed gave us the expected equation of motion for the trajectory.

Now we want to see if we can apply the same framework in special relativity, which describes the physics of things that are moving very quickly—meaning at a significant fraction of the speed of light. If you've learned some special relativity before, then you know that things get *weird* when objects are moving that fast relative to each other. We'll see that we can in fact understand the mechanics of a relativistic particle using the principle of least action, but that we have to write down a new formula for the action to do it.

As a matter of fact, we'll see that the action for a relativistic particle in a sense looks a lot more natural than the formula we wrote down for a Newtonian particle. It will be *geometric*, in fact. As the particle travels around and time goes by, it traces out a path in spacetime called the worldline of the particle. And the action will essentially just equal the length of the worldline, meaning that the particle will pick the straightest and shortest path that it can to get from point A to point B—with some caveats that we'll get to.

Where things get really interesting is in *general* relativity—Einstein's theory of gravity. According to Einstein, a massive object like a star warps the spacetime around it, deforming it from the flat spacetime of special relativity into a curved geometry. Then we have to ask ourselves what it even means for a particle's path to be "straight" in a curved space. I'll tell you a little bit more about that in a future lesson, where we'll see that the principle of least action for a particle in general relativity demands that it travels along a very special kind of curve called a geodesic.

![](https://www.physicswithelliot.com/s/paths.png)

Let's start with a very quick review of what we covered [last time](https://www.physicswithelliot.com/least-action-mini-notes). We had a particle of mass $m$ traveling from $x(t1)=x1$ to $x(t2)=x2$ , and we wanted to find the trajectory $x(t)$ that it follows in between. From Newton's second law, the trajectory will be given by the solution of the equation of motion,

$$
mx¨=−dUdx,
$$

where $F(x)=−dUdx$ is the force on the particle and $U(x)$ is the potential energy.

Newton gave us one way of getting at the equation of motion; the principle of least action gives us another. We defined the **Lagrangian** $L$ as the difference between the kinetic energy and the potential energy,

$$
L=12mx˙2−U(x),
$$

and we defined the **action** $S$ by integrating the Lagrangian over time:

$$
S=∫t1t2dt(12mx˙(t)2−U(x(t))).
$$

$S$ is a number that we can compute for any given path $x(t)$ connecting point 1 to point 2. Of all those possible paths, we showed last time that the one the particle actually follows is that path for which the action is minimized.

Now, that discussion was limited to *Newtonian* mechanics. In other words, we assumed that the particle wasn't moving anywhere close to the speed of light, $c≈3×108 m/s$ . One of Einstein's first great discoveries early in his career, was that physics looks radically different when things start approaching the speed of light.

I want to explain the fundamental idea here, without things getting overly complicated, so I'm going to focus on a *free* particle—meaning a particle with no forces acting on it. Essentially that means setting the potential $U$ to zero. A free particle travels along a straight line, because there aren't any forces pushing or pulling it in one direction or another. In space, a straight line between two given points is of course the route that minimizes the distance between them. In spacetime, a straight trajectory between two events *maximizes* what's called the **proper time**. Let me break down what this means.

![](https://www.physicswithelliot.com/s/pythagorean.png)

Let's first review some basic geometry; it might seem like I'm being a little pedantic here, but things are going to get weird in a moment when we start talking relativity, and so it's a good idea to refresh our memories about some fundamentals. Think about the $xy$ plane. Say we have two points on the plane that are separated by a distance $Δx$ in the $x$ direction and $Δy$ in the $y$ direction. Then Pythagoras taught us how to find the distance $Δs$ between the two points: it's given by

$$
(Δs)2=(Δx)2+(Δy)2.
$$

If we let the two points get really close to each other, so that the distance between them becomes infinitesimal, we usually indicate that by replacing these $Δ$ 's with $d$ 's,

$$
ds2=dx2+dy2.
$$

This expression defines what's called the **metric** of the $xy$ plane, which is just a fancy way of saying that it tells us how to measure distances.

![](https://www.physicswithelliot.com/s/curve-length.png)

If we have some curve $y(x)$ , we can measure it's length by splitting it up into lots of tiny line segments of length $ds=dx2+dy2$ , and then adding them all up to get the total:

$$
∫ds=∫dx2+dy2.
$$

To get this in a more familiar form, pull a factor of $dx$ out front of the square root. Then we get

$$
∫ds=∫dx1+y′(x)2,
$$

where $y′(x)=dydx$ is the slope of the curve $y(x).$ You may have learned this formula in your calculus class—I used it in a video from a couple of weeks ago when I showed you [how to find the shape of a hanging rope](https://www.physicswithelliot.com/hanging-rope-classic-notes).

Okay, that was the geometry I wanted to review. Now back to relativity. As our particle travels around in spacetime, it traces out a curve that we call the **worldline** of the particle, like the examples I've drawn here illustrating the $x$ and $t$ axes. So at any given moment, the particle might be found at position $(x,y,z)$ at time $t$ . That defines a point in spacetime $(t,x,y,z)$ , called an **event**. As the particle moves around, this spacetime point changes, and connecting up all the points gives us the worldline of the particle. I'll focus on the $t$ and $x$ coordinates for simplicity.

For whatever reason, when drawing pictures like this in spacetime, it's conventional to draw time flowing upward on the vertical axis and space on the horizontal axis. I've also multiplied the vertical axis by $c$ , so that both axes have units of distance. Notice that the slope of a worldline in this picture is one over the velocity of the particle (as a fraction of the speed of light), so that a light ray will travel along at a 45 degree angle. A massive particle must always move slower than the speed of light, so its worldline has to be steeper than that.

Note that even if the particle happens to be sitting still in *space*, it's still moving forward in *time*. So the worldline of a particle that's sitting still is just a straight vertical line, since its spatial coordinates aren't changing, but it's always advancing forward in time.

The claim is that the relativistic action will simply be given by the length of the particle's worldline, times some constant factors. How can we find the length of the worldline? This is where things start to get tricky. Spacetime is not like regular old space plus an extra $t$ coordinate tacked on. Mathematically, a lot of the bizarre relativistic physics that Einstein (and Lorentz, and Minkowski, and others) discovered comes from the fact that distances in spacetime are measured by

$$
ds2=−c2dt2+dx2,
$$

what we nowadays call the **Minkowski metric**. $c$ is again the speed of light, and yes that's a minus sign in front of the time term! That's what makes the geometry of spacetime so different (and confusing) compared to what we're all much more intuitively familiar with. If you've learned some special relativity before, you may recognize this expression as the "invariant interval" between two spacetime events. If not, for now you'll just have to take my word for it that this is how distances are measured in spacetime.

With the metric in hand, we can write down the length of a worldline through spacetime again by slicing it up into little segments and integrating. But that minus sign immediately starts making things awkward, even in the simplest case where our particle is just sitting at rest in space, so that the worldline is a vertical line going straight up through time. In that case $dx=0$ , and so $ds2=−c2dt2$ is a negative number.

In fact, that's always the case: $ds2$ will be negative along the path of any massive particle, not necessarily one that's just sitting still. The reason is that the speed of the particle $dxdt$ has to be less than the speed of light $c$ , the maximum speed in the universe. Then

$$
(dxdt)2<c2⟹−c2dt2+dx2<0.
$$

So $ds2$ is indeed going to be negative. That makes taking the square root awkward, so let's instead agree to flip the sign first:

$$
−ds2=c2dt2−dx2.
$$

Now we can define the length of the worldline analogous to how we did in the $xy$ plane by integrating,

$$
∫−ds2=∫c2dt2−dx2.
$$

Similar to before, it's convenient to pull out a factor of $dt$ so that we can write this as an integral over time of a function of $x(t)$ :

$$
∫−ds2=c∫t1t2dt1−x˙(t)2c2,
$$

where $x˙(t)=dxdt$ is the velocity of the particle, and I also pulled out a factor of $c$ .

The integral on the right-hand-side is called the **proper time** along the worldline:

$$
τ=∫t1t2dt1−x˙(t)2c2,
$$

i.e. the proper time is the length of the worldline divided by $c$ . Physically, the proper time is what would show up on a wristwatch strapped to the particle as it moves around in spacetime. For the particle that's just sitting at rest in space, $x˙=0$ , and so the time on the particle's watch just equals the given time interval between the events in this lab frame that we've set up:

$$
∫t1t2dt=t2−t1.
$$

But for a particle that's moving around on its way between the two events like the other worldline I drew in the picture, the time that elapses on its watch will be *smaller*. That's again because $x˙$ has to be less than $c$ , so the factor $1−x˙2/c2$ that's inside the integral is always going to be a fraction smaller than one. Then the proper time that elapses for the moving particle is going to be less than the proper time for the stationary particle between the events when they part ways and then reunite:

$$
∫t1t2dt1−x˙(t)2c2<t2−t1.
$$

This is the **time dilation** effect: in relativity, moving clocks run slow. What we've been talking about here is basically the setting for the famous twin paradox, where you sit still on Earth while your identical twin flies off around space in a rocket ship for a while before coming back to Earth. More proper time will have elapsed on your watch and less on your twin's watch. And we're not talking semantics here: when you reunite, your twin will be *younger* than you—like Matthew McConaughey at the end of Interstellar—potentially by a lot if they were gone long enough and travelled at a significant fraction of the speed of light!

I might make another mini lesson all about the twin paradox at some point in the future, for now the thing I wanted you to notice is that the proper time between two events—i.e. the length of the worldline—is *biggest* for the straight line trajectory going between them. In regular old space, of course, a line is the shortest distance between two points. In *spacetime*, because of that minus sign in the Minkowski metric, a straight line between two events maximizes the proper time.

Which brings us back to the principle of least action. A free particle going between two events travels along a straight trajectory in spacetime. And so what we've learned is that of all the paths that the particle might have taken, the one it follows is the path that maximizes the proper time. So we should choose our action to be proportional to the proper time!

Actually, we typically want the action to be *minimized* —that's why we call it the principle of *least* action, after all—so we'll make the action minus the proper time instead. And we also need to throw in some factors of $m$ and $c$ in order to get the units right:

$$
S=−mc∫−ds2.
$$

This is the action for a free particle in special relativity. In fact, it's also the appropriate action in *general* relativity, Einstein's theory of gravity, except that in that case the Minkowski metric of flat spacetime is replaced by the *curved* metric of a spacetime that's been warped by the presence of a massive object like a star. I hope to tell you a little more about that in a future post.

In either case, the action is about as simple as it could be! It just measures the length of the particle's worldline through spacetime, and so the particle follows the path that extremizes this length.

There are two more things I want to show you for right now. First, to take the variation of this action and actually show that it gives us the expected equation of motion, and second to show that it's consistent with the Newtonian action we wrote down before when the particle is moving slowly compared to the speed of light.

Expanding things out, we can write the action more explicitly as

$$
S=−mc2∫t1t2dt1−x˙2/c2.
$$

Like we learned last time, to apply the principal of least action we take a small variation $x(t)→x(t)+ε(t)$ of the trajectory and demand that the action stays the same at leading order in $ε$ . In practice, that just means taking the derivative—or really the differential—of the Lagrangian,

$$
L=−mc21−x˙2/c2.
$$

Just like the leading change in a function $f(x)$ is $df=f′(x)dx$ when you make a tiny deformation of $x$ , we get

$$
dL=−mc2⋅1211−x˙2/c2⋅(−2x˙/c2)⋅dεdt.
$$

Integrating by parts and throwing out the total derivative term because we demand $ε(t1)=ε(t2)=0$ , we find that the change in the action is

$$
dS=−m∫t1t2dt ε(t)ddt(x˙1−x˙2/c2).
$$

The combination $1/1−x˙2/c2$ shows up all the time in special relativity, it's usually denoted by $γ$ for short. Then since $dS$ needs to vanish for any deformation $ε(t)$ , the thing that it multiplies in the integrand has got to be zero—that gives us the equation of motion

$$
ddt(γmx˙)=0,
$$

where I've also brought along the constant mass $m$ .

In Newtonian mechanics, the analogous calculation would give us Newtons' second law:

$$
mx¨=ddt(mx˙)=0.
$$

In words, a free particle travels along a straight line with constant momentum $p=mx˙.$

For a relativistic particle, what we've discovered here is that the relativistic generalization of the Newtonian momentum is $p=γmx˙,$ and so a free particle travels along a straight line with constant momentum $γmx˙$ .

When $x˙$ is very small compared to $c$ , like for everyday objects that are well described by Newtonian mechanics, then $γ=1/1−x˙2/c2$ is very close to one, and so the relativistic momentum reproduces the more familiar expression at everyday speeds.

Along those same lines, the last thing I want to do is show that our relativistic action reproduces the Newtonian action when $x˙$ is small. To do that, think about the function $1+ε$ , where $ε$ is a small number. Let's expand this function in a Taylor series around $ε=0$ . When $ε$ is actually equal to zero, the function is equal to 1, so that's the leading term. Then the first correction is the first derivative evaluated at $ε=0$ , times $ε$ : that's $12ε$ . So we have to good approximation

$$
1+ε≈1+12ε
$$

for a tiny number $ε$ .

When the speed $x˙$ of our particle is small compared to the speed of light $c$ , we can apply this approximation to the integrand $1−x˙2/c2$ that appears in the action—in other words we're setting $ε=−x˙2/c2$ . That means that

$$
1−x˙2/c2≈1−12x˙2c2.
$$

Plugging this approximation into the action gives

$$
S=∫t1t2dt(12mx˙2−mc2).
$$

The first term is the Newtonian kinetic energy, just like we expected to get for the action of a free particle. The second term $mc2$ is just a constant—it doesn't affect any of the physics since adding a constant to the action doesn't change where the action is going to be minimized. So we can ignore it. Then our relativistic action correctly reproduces the original Newtonian action for particles that aren't moving very fast compared to the speed of light!

So, we've written down the action that describes a free particle in special relativity: it's just the length of the worldline that the particle traces out as it moves through spacetime. Roughly speaking, the particle takes the shortest and straightest path that it can—more precisely it takes the path that maximizes its proper time.

Einstein's special theory of relativity tells us about how to do physics for particles that are moving at speeds that get close to the speed of light. But about ten years after discovering special relativity, Einstein generalized his framework to incorporate the effects of gravity—we call that theory, well, *general* relativity. The basic idea is that a very massive object like a star dramatically warps the geometry of spacetime in its vicinity. Then the *flat* spacetime Minkowski metric $ds2=−c2dt2+dx2$ that we worked with here is replaced by a *curved* metric that describes this warped spacetime.

But, the *same* action principle that we discussed here still holds in general relativity—it's just that the length of the particle's worldline must be computed with the new, curved metric. Remember that it's the metric that tells us how to measure distances in the first place, and so by warping the metric the star changes the length we get for the worldline. Then the particle still follows the straightest and shortest path through spacetime that it can, except that in a curved space we need to generalize our notion of what it even means to be a "straight line." The resulting shape is called a **geodesic**. Stay tuned to hear more about that in the future.

---

See also:

- Part 1: [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- Part 3: [The Action for General Relativity](https://www.physicswithelliot.com/gr-action-mini-notes)
- Part 4: [The Action for String Theory](https://www.physicswithelliot.com/string-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).