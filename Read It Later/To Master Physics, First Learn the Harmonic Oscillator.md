---
date: "2025-08-10T22:14:25+08:00"
url: "https://www.physicswithelliot.com/oscillator-help-room-notes"
status:
---
![](https://www.youtube.com/watch?v=bmGqhM-tUk4)

Of all the systems you’re likely to meet in your first physics class, far and away the most important is the **simple harmonic oscillator** —in other words, the basic setup of a block attached to a spring. No other system so thoroughly permeates virtually every corner of physics, from classical mechanics to quantum mechanics to quantum field theory. It’s a setup that you are guaranteed to meet again and again throughout your physics education, and so it’s a good idea to learn it well from the get-go. But why is this seemingly innocuous problem so ubiquitous in so many areas of physics?

![](https://www.physicswithelliot.com/s/spring-block.png)

We’ll start by reviewing the basic setup, and after that we’ll get into why it is that it’s so important. We’ve got a block of mass $m$ sitting on a flat table, which we’ll take to be frictionless for simplicity. It’s hooked up to a spring, which is itself anchored to a wall on the other end. If you give the block a little kick, or if you pull it out a ways and then let it go, it will oscillate back and forth from side to side like a sine or cosine function. We call these sinusoidal oscillations **simple harmonic motion**.

Here’s how we understand all this using Newton’s laws. Whenever we move the block, we stretch or compress the spring, which therefore tries to pull or push the block back to its equilibrium position. The **equilibrium** is the position where the spring is happy and relaxed; it’s neither compressed nor stretched, and so it exerts no force on the mass. That position will depend on the spring we’re using, so let $l$ denote the equilibrium length of the spring.

Now suppose the system is *not* in equilibrium; for example, suppose that we pull the block over to the right by a distance $x$ . Now the spring is stretched, and so it’s going to try to pull the block back over to the left toward equilibrium. How hard it pulls will be proportional to how far we’ve moved the block, as well as how *stiff* the spring is. The stiffness is measured by another parameter called the **spring constant** $k$ , which determines how big a force the spring exerts when we’ve stretched it by a distance $x$ :

$$
F=−kx.
$$

Then the $F=ma$ equation for the block is

$$
ma=−kx.
$$

If you’ve learned some calculus, then you know that the acceleration $a(t)$ is nothing but the second derivative of the position $x(t)$ with respect to time. And so we can alternatively write this equation as

$$
d2xdt2=−Ω2x.
$$

I’ve also introduced another symbol here, capital omega $Ω=k/m,$ because this combination is so important, as we’ll see in a second.

So to solve for the trajectory of the block, we just have to ask ourselves what kind of function $x(t)$ , when we take its derivative twice in a row, gives us back the same function times this negative number $−Ω2$ . The answer is a sine or cosine!

Recall that the derivative of $sin$ is $cos$ , and the derivative of $cos$ is $−sin$ . Then we get

$$
ddtsin⁡(Ωt)=Ωcos⁡(Ωt)
$$

and

$$
ddtcos⁡(Ωt)=−Ωsin⁡(Ωt).
$$

Those factors of $Ω$ on the right come from the chain rule: the derivative of $sin⁡(Ωt)$ with respect to its argument is $cos⁡(Ωt)$ , and then we multiply by the derivative of $Ωt$ with respect to $t$ , which contributes the factor of $Ω$ .

Now taking the second derivative, we get

$$
d2dt2sin⁡(Ωt)=−Ω2sin⁡(Ωt)
$$

and

$$
d2dt2cos⁡(Ωt)=−Ω2cos⁡(Ωt),
$$

which is exactly what we wanted: the second derivative is $−Ω2$ times the function that we started with.

Then the general solution to the $F=ma$ equation is

$$
x(t)=x0cos⁡(Ωt)+v0Ωsin⁡(Ωt),
$$

where $x0$ and $v0$ are the initial position and velocity of the block—how far did we pull the mass out at $t=0$ and/or how fast did we kick it?

So we indeed find that the block sinusoidally oscillates back and forth around its equilibrium position in simple harmonic motion. The rate at which it oscillates is determined by $Ω=k/m$ , which we therefore call the **natural frequency** of the system. $Ω$ had better have dimensions of one over time since it’s supposed to be a frequency, so let’s check:

$$
km∼N/mkg=1s2=1s,
$$

where $k=−F/x$ has units of Newtons per meter, $k∼N/m=kg/s2.$

$Ω$ tells you how fast the block will oscillate once you set it moving. Notice that you don’t get to pick this oscillation speed! It’s fixed by the stiffness of the spring and the mass of the block, and it will always oscillate at this same rate. (Unless you do something like kick the block so hard that it breaks the spring or crashes into the wall.)

x <sub>0</sub> (m) = 0.40

v <sub>0</sub> (m/s) = 0.00

L <sub>eq</sub>

t (s)

x (m)

Here’s an animation you can play with to see how this works. Just drag the sliders to choose the initial position and velocity you want for the block, and then press start to see what its position versus time graph is going to look like.

---

See also:

- [The Trick that Makes Physics as Simple as Drawing a Picture](https://www.physicswithelliot.com/potential-help-room-notes)
- [All About Pendulums](https://www.physicswithelliot.com/pendulum-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).