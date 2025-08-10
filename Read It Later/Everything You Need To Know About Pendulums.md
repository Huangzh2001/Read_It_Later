---
date: "2025-08-10T22:16:03+08:00"
url: "https://www.physicswithelliot.com/pendulum-help-room-notes"
status:
---
## Everything You Need To Know About Pendulums: Physics Help Room

![](https://www.youtube.com/watch?v=0q0L7Fj4dk8)

Pendulums are really fascinating systems for learning about a lot of physical principles. They can come in all kinds of shapes and sizes, but I'm going to focus on the *simple* pendulum, which means that we have a ball of mass $m$ attached to a rod of length $l$ , which is pivoted at its other end so that the pendulum is free to rotate around. We'll treat the ball as a point particle, and we'll assume that the rod is much lighter than the ball, so that we can effectively treat it as being massless.

![](https://www.physicswithelliot.com/s/pendulum-coordinates.png)

We want to learn how to predict the motion of the pendulum. So say if you were to pull it up to some initial angle and then let it go, or if you were to give the ball a kick to set it moving, what's the resulting motion going to look like?

The first thing we should do is to set up some coordinates that specify the position of the pendulum. We can make different choices here, but I think the simplest coordinates to use would either be the angle $θ$ that the rod makes with the vertical, or the arc length coordinate $s$ that's traced out along the circle that the particle is stuck on. Either one will do the job, and the relation between them is the definition of an angle in radians—it's the arc length divided by the radius:

$$
θ=sl.
$$

Note that $θ=s=0$ is the **equilibrium** position of the pendulum, where it will happily sit at rest at the very bottom.

The basic procedure for predicting motion that we learn about in our first physics class is

1. Draw the **free-body diagram** that shows all of the forces $F→$ acting on a mass
2. Add up all the forces $∑F→$ , and write down Newton's 2nd law: $∑F→=ma→$
3. Solve $∑F→=ma→$ for the trajectory $r→(t)$

That's what we'll do step-by-step for the pendulum. First, the free-body-diagram:

![](https://www.physicswithelliot.com/s/pendulum-fbd-plain.png)

There are only two forces acting on the particle. We've got gravity 
$$
mg
$$
 pulling straight down, and we've got the tension $T$ in the rod pulling back toward the center of the circle.

Step two is to add up all the forces and write $∑F→=ma→$ . This is a vector equation, but because the particle is stuck moving around on a circle, we really only care about the component of the force and acceleration that point along the circle:

![](https://www.physicswithelliot.com/s/pendulum-circle.png)

The tension points radially inward toward the center of the circle, which is perpendicular to the tangent direction that we're actually interested in. So the tension doesn't contribute anything to the tangent direction. The only thing that actually contributes is the component of gravity that points along the circle.

We need to do a tiny bit of geometry to figure out what this force is:

![](https://www.physicswithelliot.com/s/pendulum-geometry.png)

First of all, we can see from the pair of opposite angles that the angle that the tension arrow makes with the vertical is also 
$$
θ
$$
. Then since the tension makes a right angle with the tangent direction, the gravity arrow makes an angle $π2−θ$ with the tangent. So we have a little right triangle with the gravity arrow making the hypotenuse, one leg pointing tangent to the circle and the other leg pointing perpendicular to the circle. The tangent component is what we're after: it's $mgsin⁡θ$ pointing back toward $θ=0.$ 

In practice, there's a faster way to figure out the tangent force. We know it's going to be either $mgsin⁡θ$ or $mgcos⁡θ$ , but how do we pick the right one without going through all this geometry work? The trick is to think about *limiting cases*. For example, when $θ=0$ —so that the pendulum is all the way at the bottom of its arc—the tangent direction to the circle is horizontal, and gravity is of course still pointing straight down. So gravity is perpendicular to the tangent direction, and the component of gravity along the circle is *zero*. That rules out $mgcos⁡θ$ , since that would have given us $mgcos⁡(0)=mg$ when $θ=0$ . It's $mgsin⁡θ$ that correctly vanishes when $θ=0.$

Now we can write down the component of $∑F→=ma→$ along the circle. We have the one force $−mgsin⁡θ$ (minus because it points back toward equilibrium) and the acceleration $s¨$ :

$$
ms¨=−mgsin⁡θ.
$$

I'm using dots here to denote rates of change with respect to time. So if $s(t)$ is the position as a function of time, then

$$
v=s˙=dsdt
$$

is the velocity (the first derivative of $s(t)$ ), and

$$
a=s¨=d2sdt2
$$

is the acceleration (the second derivative).

Let's write everything in terms of $θ$ by remembering that $s=lθ$ . $l$ is a constant, so this equation also implies $s˙=lθ˙$ and $s¨=lθ¨$ . Then we get

$$
mlθ¨=−mgsin⁡θ.
$$

Finally, we can simplify this to

$$
θ¨=−glsin⁡θ.
$$

That was step two of Newton's procedure. Step three is to solve this equation for $θ(t)$ . That's actually pretty hard to do. The factor of $sin⁡θ$ on the right-hand-side makes this a complicated equation—too complicated for us to be able to write down a simple solution, in general.

But there's one special case where we can write down a simple solution, and that's when $θ$ is small, meaning that the pendulum never gets very far away from equilibrium. This would be the case if you pulled the pendulum up to some small initial angle and then let it go, or if you only gave it a gentle tap to set it oscillating slightly back and forth. In this special case, we can apply what's known as the **small angle approximation**. This is the fact that $sin⁡θ$ and $θ$ very closely approximate each other when $θ$ is small:

$$
sin⁡θ≈θθ≪1.
$$

The easiest way to see this is just to plot $sin⁡θ$ and $θ$ on the same graph:

![](https://www.physicswithelliot.com/s/small-angle.png)

In general the two curves look nothing like each other. But near the origin, where 
$$
|θ|<0.5
$$
 radians or so, they're right on top of each other. If you're familiar with Taylor series, $sin⁡θ=θ+⋯$ is just the first term in the expansion of $sin⁡θ$ around $θ=0$ .

Then provided the pendulum never gets very far away from equilibrium, we can approximate the $F=ma$ equation as

$$
θ¨=−glθ.
$$

It's going to be convenient to define $Ω=g/l$ , so that the factor in front of $θ$ is $−Ω2$ :

$$
θ¨=−Ω2θ.
$$

This is a much simpler equation. We just have to ask ourselves what kind of function $θ(t)$ , when I take its second derivative, gives me back the same function times a negative number. The answer is a sine or cosine!

Recall that the derivative of $sin$ is $cos$ , and the derivative of $cos$ is $−sin$ . Then notice that

$$
ddtsin⁡(Ωt)=Ωcos⁡(Ωt)
$$

and

$$
ddtcos⁡(Ωt)=−Ωsin⁡(Ωt).
$$

The factors of $Ω$ on the right come from the chain rule: the derivative of $sin⁡(Ωt)$ with respect to its argument is $cos⁡(Ωt)$ , and then we multiply by the derivative of $Ωt$ with respect to $t$ , which contributes a factor of $Ω$ .

Alternatively, this factor had to be there by considering the units. $g$ has units of $meters/second2$ and $l$ is in $meters$ , so that $Ω=g/l$ has units of $1/seconds.$  $sin⁡(Ωt)$ and $cos⁡(Ωt)$ are both unitless—the $d/dt$ on the left makes those units $1/seconds$ , and we likewise get $1/seconds$ on the right thanks to the factors of $Ω$ .

Now taking the second derivative, we get

$$
d2dt2sin⁡(Ωt)=−Ω2sin⁡(Ωt)
$$

and

$$
d2dt2cos⁡(Ωt)=−Ω2cos⁡(Ωt),
$$

which is exactly what we wanted: the second derivative is $−Ω2$ times the function that we started with.

So, the general solution to our $F=ma$ equation when $θ$ is small is

$$
θ(t)=Acos⁡(Ωt)+Bsin⁡(Ωt).
$$

$A$ and $B$ here are two constants that depend on the initial conditions: where was the pendulum and how fast was it moving at $t=0$ ? If we plug in $t=0$ we get

$$
θ(0)=A,
$$

so that $A$ corresponds to the initial angle $θ0$ of the pendulum. $B$ , meanwhile, is related to the initial angular velocity:

$$
θ˙(t)=−ΩAsin⁡(Ωt)+ΩBcos⁡(Ωt)⟹θ˙(0)=ΩB.
$$

So we could alternatively write the general solution as

$$
θ(t)=θ0cos⁡(Ωt)+θ˙0Ωsin⁡(Ωt).
$$

There we have it! We've solved for the trajectory of the pendulum given whatever the initial conditions $θ0$ and $θ˙0$ are, provided that we don't stray too far away from equilibrium. For example, if we release the pendulum from rest from a small initial angle $θ0$ , the motion is given by

$$
θ(t)=θ0cos⁡(Ωt),
$$

where again $Ω$ was defined as the square root of $g/l$ .

There's a lot of interesting physics to notice here. What we've found is that the pendulum oscillates back-and-forth around equilibrium in a sinusoidal pattern. That certainly sounds reasonable—if you pull a pendulum up to a starting angle and let it go, it will oscillate back-and-forth between that angle and the same angle on the opposite side (ignoring things like air resistance and friction from the pivot point). In other words, the motion is **periodic**.

The speed of the oscillations is characterized by $Ω$ , which is called the **natural frequency** of the pendulum. The bigger $Ω$ is, the faster the oscillations will be. Notice that it only depends on the strength of gravity $g$ and the length of the pendulum $l$ : the longer the pendulum, the slower the oscillations, and the stronger gravity is, the faster the oscillations. But it doesn't depend on the mass $m$ of the particle. Two pendulums, identical except that one has mass $m$ and the other mass $2m$ , will oscillate at the same rate. This is reminiscent of the fact that the acceleration of a falling projectile is always $g$ , regardless of its mass.

The time it takes the pendulum to complete one full oscillation is called the **period** $T$ (not to be confused with the tension). $cos$ and $sin$ complete a full oscillation when their arguments increase by $2π$ . So for example

$$
cos⁡(Ωt)=cos⁡(Ωt+2π).
$$

We can alternatively write the right-hand-side as $cos⁡(Ω(t+2πΩ))$ . So the pendulum comes back to its starting configuration after time

$$
T=2πΩ=2πlg
$$

has elapsed.

We again could have guessed this by thinking about the units: the only way to get something with units of $seconds$ out of $l,g,$ and $m$ is the combination $l/g$ . The period couldn't depend on $m$ because there's nothing to cancel out that factor of $kilograms.$ That doesn't tell us anything about additional unitless factors that multiply $l/g$ , though, like the $2π$ that actually came out in the answer. But thinking about units in physics often gets us 90% of the way there with very little effort!

Also notice that the period doesn't depend on the initial angle $θ0$ : if we pull two identical pendulums up to initial angles $θ0$ and $2θ0$ , they'll swing back to where they started at the same time, as long as $θ0$ is small. That didn't have to be the case— $θ0$ is unitless, so we could have multiplied $l/g$ by any function of $θ0$ without changing the units. And in fact at larger angles, the period *does* depend on the initial angle, as you'll discover if you complete the problem sheet linked at the top of the page.

Here's an animation that plots $θ(t)$ for initial conditions of your choosing:

θ <sub>0</sub> = 0.40

ω <sub>0</sub> = 0.00

t

θ

You can drag the sliders to set the initial angle and angular speed, and then press start to watch what happens. Notice that when you release the pendulum from rest close to equilibrium, the oscillation indeed looks sinusoidal. But when you release it from a big angle it doesn't. The motion is still *periodic* —meaning that it repeats itself over and over again—it's just not as simple as a cosine; the peaks and troughs of the graph are much flatter.

On the other hand, if you kick the pendulum very hard by giving it a big initial speed, it doesn't oscillate back-and-forth at all—it swings all the way around the pivot!

---

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).