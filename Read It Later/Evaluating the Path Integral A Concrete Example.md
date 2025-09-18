---
date: "2025-08-10T22:05:05+08:00"
url: "https://www.physicswithelliot.com/path-integral-part-3-mini-notes"
status:
---
## The Quantum Path Integral, Computed

![](https://www.youtube.com/watch?v=UWuhMJZaiZM)

## Introduction

**Path integrals** —aka **functional integrals** —are among the most essential mathematical tools used all across modern physics—from quantum mechanics to statistical mechanics to particle physics and more.

Unfortunately, they're also famously complex!

In this lesson, we'll discuss the original and most basic example: the Feynman path integral that describes the motion of a quantum mechanical particle,

$$
∫xixfDx eiS[x]/ℏ.
$$

I'll explain how it's defined mathematically, what it means physically, and how to actually compute it in an explicit example.

Despite the appearance of the familiar $∫$ symbol, a path integral is not like any integral you've seen before in, say, your intro calculus classes.

With an ordinary integral, we look at a function $f(t)$ that assigns a number to each point $t$ along a line.

![[Read It Later/attachments/c29611fec50549d165f5e260daa2b990_MD5.png]]

Then the integral of the function over some range computes the area under the curve in that region:

$$
Area=∫titfdt f(t).
$$
To work it out, we just imagine slicing the region up into lots of skinny rectangles, each one of width $dt$ and height $f(t).$ The area of a given rectangle is then the product $dt f(t),$ and by summing up those contributions from all the rectangles, and moreover letting their widths shrink down to be infinitesimally small, we obtain the total area under the curve.

To say it another way, all we're doing is looking at a range of points $[ti,tf]$ along a line. Each point $t$ in the range gets assigned a number $f(t).$ We take that number and multiply it by the **measure** factor $dt,$ and finally we sum over all the points.

But that's for an ordinary integral. A path integral is a different, and much more complicated beast. Instead of summing over a range of points on a line, we do a sum over every possible *path* connecting a given starting point and ending point:

![[Read It Later/attachments/ca33e2b38a56155e9b7039d579cf0469_MD5.png]]

To each path $x(t)$ we assign a corresponding complex number $Φ[x].$ By summing up those numbers for every possible path, again multiplied by a corresponding "measure" factor $Dx,$ we obtain the path integral of $Φ$ :

$$
∫xixfDx Φ[x]=sum over all paths x(t) connecting x(ti)=xi to x(tf)=xf.
$$

And if doing a sum over an infinite set of paths sounds complicated, well... it is!

I should say at the outset that defining the path integral in a mathematically rigorous way is a very subtle problem, and I’m not going to make any pretense about being especially rigorous here. The aim for this lesson is to show you how the path integral is constructed and applied by physicists.

And to begin to understand why it's so important for physics, imagine we have a quantum particle like an electron that starts out at position $xi$ at an initial time $ti.$ Then after waiting a little while, at a final time $tf$ we look for it at some other point $xf.$

![[Read It Later/attachments/0ef931d93058655b5fd090b5c2401102_MD5.png]]

Feynman showed that instead of moving along a single, classical trajectory that something like a baseball would have followed, for an electron we need to consider every possible trajectory that the particle could conceivably follow.

And only after summing over all those trajectories—in other words, by computing the path integral—can we obtain the quantum mechanical probability that we'll find the particle at that final point when we go to measure it:

$$
Prob(xf)∝|∫xixfDx Φ[x]|2.
$$

More precisely, the probability is proportional to the absolute-value-squared of the path integral.

This, schematically, is Feynman's path integral approach to quantum mechanics, and it's kind of a wild idea when you stop to really think about it—both physically and mathematically. Because again, it says that a quantum mechanical particle doesn't follow a single path like we're used to in classical mechanics—like, say, the parabolic arc of a baseball flying through the air.

Instead, the particle does a kind of statistical average of every possible trajectory between the endpoints—including paths that zig-zag to the moon and back before finally winding up at the ending position where we observe it.

That's what the path integral computes. And in this lesson, I'll show you how to unpack what it means, and how to evaluate it in the very simplest case of a quantum particle with no forces acting on it.

And in doing so, we'll discover the particle's quantum mechanical wavefunction without ever even writing down the central equation of quantum mechanics—the Schrödinger equation.

This is the third in a series of lessons I've shared about the path integral and Feynman's approach to quantum mechanics. In [Part I](https://www.physicswithelliot.com/wavefunction-mini-notes) and [Part II](https://www.physicswithelliot.com/path-integral-mini-notes), I explained some of the basic ideas of quantum mechanics, including why we need to sum over every possible path to understand the behavior of a quantum particle, starting from the famous double-slit experiment.

I'll begin here by briefly reviewing the main results we discovered before. And then we'll see how to put it all into practice by working through an actual path integral calculation.

## Review: The Many Paths of a Quantum Particle

The physics of quantum objects—that is, of very tiny things like electrons—is very different from what we're used to up here in our more familiar classical world.

Like I just mentioned, quantum particles don't move along the well-defined trajectories that we see for everyday objects like baseballs.

A baseball, if you throw it up in the air, will travel along a simple trajectory $x(t)$ —a parabola—that connects whatever initial height $xi$ where the ball started at the initial time $ti$ to the final height $xf$ where we find it at any later time $tf.$

![[Read It Later/attachments/0b9f44e2edb0e20e196f636432b84999_MD5.png]]

(Of course, we'd more often use the letter $y$ to denote the height of the ball above the ground. But I'll use $x$ to match up with the notation in what follows.)

That's the classical trajectory, and it's easy enough to work out by solving $F=ma$ with the force of gravity pulling down on the ball. Importantly, if we know what the ball was doing at the initial time $ti,$ we can predict precisely where we'll find it at any later time $tf.$

But quantum mechanics turns all that on its head. Even if we know exactly what a quantum particle was doing at the initial time, all we can predict for when we go to measure it again later on is the probability $Prob(xf)$ that we'll find it at some position. The particle *might* wind up there, or we might find it somewhere else.

And that means that in between, the particle doesn't follow a unique trajectory like the baseball did. Instead, Feynman showed—and we discovered in the [previous lesson](https://www.physicswithelliot.com/path-integral-mini-notes) —that the particle averages over *every* possible trajectory connecting the two endpoints.

And we saw how all that comes about by exploring the famous double-slit experiment, where we chuck quantum particles at a wall with two tiny holes cut into it, and see what comes out on the other side.

![[Read It Later/attachments/1bfd7dbc87ae1243aaa5a4b67b50ad87_MD5.png]]

If a quantum particle moved along a single trajectory like a baseball, we could say for certain whether the particle passes through the left slit or the right one. And then, we'd expect to find that most of the particles that make it through wind up somewhere in the middle—distributed with a broad bump around the center of the backstop.

![[Read It Later/attachments/73af0f7858919de7f7a880346eee527a_MD5.png]]

But that's not what we observe in practice. Instead, we wind up with a distribution called an interference pattern:

![[Read It Later/attachments/ac7c1d31c107b1695efa412106953d4d_MD5.png]]

There are peaks where we find lots of particles clustered together, separated by valleys where next to none arrive at all.

Somehow, each particle that travels through the barrier probes both slits at once and interferes with itself!

And as mind-bending as that fact may be, this simple experiment already leads to the basic idea of the path integral. Because if we imagine drilling a third hole in the barrier, we'd have to include trajectories that pass through that hole as well. And the same goes if we drill a fourth hole or a fifth hole, and so on.

Taking this idea to the extreme, Feynman imagined filling the entire region with barriers, and drilling lots of tiny holes through each of them. Then we'd need to consider every possible route the particle could follow, bouncing from one hole to the next on its way across the gap.

![[Read It Later/attachments/c52a71f827b595546969d08df6e61ee6_MD5.png]]

And eventually, we can imagine drilling *so* many holes that the barriers themselves effectively disappear, and we're led to the conclusion that the particle probes *every* possible path in getting from the initial point to whatever final point where we observe it at the detector, and we need to sum over all of them.

That's the physical motivation behind Feynman's path integral formulation of quantum mechanics: to determine the probability that the particle will be found at some final position $xf,$ we need to sum over every possible trajectory that it could have taken to get there:

$$
Prob(xf)↔∑paths x(t)
$$

But what exactly are we supposed to be adding up here in this sum?

In the [last lesson](https://www.physicswithelliot.com/path-integral-mini-notes), I explained that to each path we assign a certain complex number, $Φ[x]=eiS[x]/ℏ,$ where $ℏ$ is the fundamental constant of quantum mechanics, called Planck's constant, and $S[x]$ is a number called the **action** that we can compute for any given path.

The action is defined by taking the kinetic energy $K$ of the particle at any moment, minus the potential energy $U,$ and integrating that difference over time along the trajectory:

$$
S[x]=∫titfdt (K−U).
$$

We therefore pick any path $x(t)$ connecting the initial point $x(ti)=xi$ to the final point $x(tf)=xf.$ Then we perform this ordinary integral of the kinetic energy minus the potential energy along that path, and the result is a real number that we can assign to that trajectory—its action.

Different paths will have different values for the action, and therefore each will contribute with a different weight $eiS[x]/ℏ,$ which is a complex number that you can picture as an arrow in the complex plane pointing at the angle $S[x]/ℏ.$

And, according to Feynman, we need to add up all those contributions from all the possible paths in order to predict where we'll find the particle when we go to measure it again.

That's all very schematic, though. Now let's dig into the details of how we'd actually go about defining this sum over paths, what exactly it computes for us, and how to evaluate it in a concrete example.

## The Path Integral, Defined

We just reviewed how the double-slit experiment explains the intuition behind why we need to sum over all possible paths to understand the behavior of a quantum particle. But now let's see how to put that intuitive idea into practice.

First of all, let me state again precisely what it is that we want to calculate here.

We have a quantum particle which is starting out at position $xi$ at the initial time $ti.$ And the question is, if we wait a little while and measure its position again later on at time $tf,$ what's the probability that we'll find the particle at some other point $xf?$

And here again is the answer, according to Feynman.

![[Read It Later/attachments/cf4142c5b34ae93203c2efab12b586c4_MD5.png]]

As before, we consider every possible trajectory $x(t)$ that connects the initial and final points. For each path, we evaluate its action $S[x],$ and from there we write down the corresponding complex phase $eiS[x]/ℏ$ that it contributes.

Then we do the same thing for all the other paths, and we add up the complex phases that we get from each of them, along with an overall factor $A$ out front that we'll work out later:

$$
Kfi=A∑paths x(t)eiS[x]/ℏ.
$$

The result is called the **amplitude** $Kfi$ for the particle to propagate from point $i$ to point $f.$

It's not quite the probability that we're looking for yet— $Kfi$ is a complex number, after all. But in general in quantum mechanics, to go from an amplitude to a probability we just need to take the absolute value and square it:

$$
Prob(xf)∝|Kfi|2.
$$

Finally, what we're really looking for here is the probability that we'll find the particle within a little window of width $dxf$ around the given point.

![[Read It Later/attachments/95b87192280d7275277a5912939b01a7_MD5.png]]

And so the last thing we need to do is to multiply by that tiny width:

$$
Prob(xf)=|Kfi|2dxf,Kfi=A∑paths x(t)AeiS[x]/ℏ
$$

This is the central result of the path integral formulation of quantum mechanics. And of course, the hard part is how to actually evaluate the amplitude $Kfi$ by summing over all the possible paths between our initial and final points, and that's what we're going to tackle now.

First of all, the set of all possible paths isn't a discrete list, so we're not actually doing a discrete sum here. Instead, it's a path *integral*, which we'll write as

$$
Kfi=∫xixfDx eiS[x]/ℏ=integral over all paths x(⋅) with x(ti)=xi and x(tf)=xf.
$$

But if there's an infinite continuum of paths that go between our two points, how are we supposed to do a sum over all of them?

We can follow a very similar strategy to the way you learned to define an ordinary integral in your first calculus class. With an ordinary integral, we basically want to add up the values of a function $f(t)$ for each point $t$ in a given range on a line.

$$
I=∫titfdt f(t).
$$

But instead of jumping straight to summing over the continuum of points between $ti$ and $tf,$ we start by breaking it up into a series of discrete steps.

![[Read It Later/attachments/4a36ff93ecbe53a89300c7ba626c47ba_MD5.png]]

So let's say we divide it up into $N$ steps: from $ti$ to $t1,$ from $t1$ to $t2,$ and on and on, all the way up to $tN−1,$ and finally our last point $tf.$ In fact, I'll rename the initial point to $t0$ and the final point to $tN$ to really make that pattern clear.

The total width is $tN−t0,$ and so the width of each smaller interval is that total divided by $N,$ which I'll abbreviate as $Δt$ :

$$
Δt=tN−t0N.
$$

And now that we have a discrete list of points instead of a continuum, the problem becomes much simpler. For each point, we just write down the value of the function—the height, in other words—and we multiply it by the tiny width $Δt.$ That gives us the area of a rectangle under the curve at that point: $Δtf(t0)$ for the first rectangle, $Δtf(t1)$ for the next, and so on:

$$
I≈Δt f(t0)+Δt f(t1)+⋯+Δt f(tN−1).
$$

We can therefore write the total area of the rectangles as $Δt$ times each discrete value of $f,$ summed over all the individual steps:

$$
I≈∑j=0N−1Δt f(tj),
$$

and that gives us a discrete approximation to the actual area under the curve.

Finally, by letting the number of steps $N$ get really big, the rectangles get skinnier and skinnier, and our approximation gets better and better. In the limit $N→∞,$ we obtain the exact area under the curve:

$$
I=limN→∞∑j=0N−1Δt f(tj)=∫titfdt f(t).
$$

This limiting expression is what we mean when we write down the definite integral of a function, where the notation is meant to indicate that we're summing over the continuum of points between $ti$ and $tf,$ while letting the width $Δt$ shrink down to the infinitesimally small measure $dt.$

That was for an ordinary integral. But now we can apply a very similar procedure to understand the path integral. Returning to the amplitude

$$
Kfi=∫xixfDx Φ[x],
$$

we want to integrate the quantity $Φ[x]$ over all the trajectories $x(t)$ that connect $x(ti)=xi$ to $x(tf)=xf.$

$Φ[x]$ is called a **functional**, by the way, as opposed to an ordinary function. It takes in a whole curve as its input and assigns a number to it, compared with an ordinary function that simply takes in one number and returns another.

It's common to write functionals using square brackets, and the whole path integral is therefore also known as a functional integral.

But once again, instead of jumping straight to trying to sum over the continuum of all possible paths, we can start by turning this into a discrete problem.

![[Read It Later/attachments/9aa79729094448dbae8f95848d833d65_MD5.png]]

Consider some trajectory $x(t).$ Just like before, we can take the time interval from $ti$ to $tf$ and break it up into $N$ discrete steps, from $ti$ to $t1,$ from $t1$ to $t2,$ and so on, ending with $tN−1$ and the final time $tf.$

Then for each of those times, the trajectory assigns a corresponding point in space: $x1,x2,$ and so on, up to $xN−1.$ And by joining those points up with straight line segments, we can make a zig-zag approximation to our original path.

And the same goes for any other path we might draw. We just shift our points up or down to make a zig-zag version of any given curve, and in that way we can make a discrete approximation to any path that we like.

And so, if we want to sum over all those possible trajectories, we just need to sum over all the possible values of $x1,$ all the possible values of $x2,$ and so on, all the way up to $xN−1.$

In other words, we're going to integrate over the entire range of potential values for $x1,$ from $−∞$ to $+∞.$ And likewise we'll integrate over all the possible values of $x2,$ and $x3,$ and on and on and on, until we get to $xN−1:$

$$
∫xixfDx Φ≈A∫−∞∞dx1 ∫−∞∞dx2⋯∫−∞∞dxN−1 Φ.
$$

That's how we'll construct the sum over all paths: by integrating over all the possible positions of the intermediate points.

We *don't* integrate over the initial and final points $xi$ and $xf$ , however—those are fixed to the initial and final coordinates of the particle.

And as mentioned earlier, we'll also include an overall constant $A,$ which will be important for actually getting a sensible answer out when we take the limit. It's part of the definition of what we mean by " $Dx$ ."

Indeed, just like before, the last thing we want to do here is to take the limit as $N→∞,$ so that the time intervals between our steps become infinitesimally small, and we’re able to account for every possible continuous path between the endpoints.

This, at last, is how we'll define the path integral of our functional $Φ$ :

$$
∫xixfDx Φ=limN→∞A∫−∞∞dx1 dx2⋯dxN−1 Φ.
$$

Hopefully that idea makes some sense, but still, all this must still sound very formal. So let's make it totally concrete by working out an explicit example: the path integral for a free quantum mechanical particle.

## The Free Particle Path Integral

Consider again a quantum particle that starts out at position $xi$ at the initial time $ti.$ Our job is to figure out the probability of finding it at some other point $xf$ at a later time $tf.$

According to Feynman, the amplitude for the particle to propagate between these two points is given by the path integral of $eiS/ℏ:$

$$
Kfi=∫xixfDx eiS[x]/ℏ.
$$

And if we can work out this integral, we'll have answered our question, because the probability is then simply determined by the modulus of $K$ squared,

$$
Prob(xf)=|Kfi|2 dxf.
$$

To keep things as simple as possible in this example, let's suppose that we're dealing with a free particle—meaning that it doesn't have any forces like gravity or electromagnetism acting on it.

![[Read It Later/attachments/6b450f282c5de1104098dea6fa29d276_MD5.png]]

If it were a *classical* particle, then the solution to $F=ma$ with the force equal to zero would just be a straight line connecting the two endpoints,

$$
x(t)=xf−xitf−ti(t−ti)+xi.
$$

But as we've discussed, in quantum mechanics things aren't quite that simple.

Instead, to compute the amplitude $Kfi$ we need to sum over all paths from point $i$ to point $f,$ weighted by $eiS/ℏ$ —where the action $S,$ remember, is defined by

$$
S[x]=∫titfdt {12m(dxdt)2−U(x(t))}.
$$

For a *free* particle, though, the potential energy is zero, so we can throw the second term away, which is what makes this case so much easier to handle.

$$
S[x]=∫titfdt 12m(dxdt)2.
$$

And so, what we need to do is to write down the value of this action $S$ for each possible trajectory, raise it to $eiS/ℏ,$ and finally sum over all the paths.

![[Read It Later/attachments/2d4ad5e2d59c7c2b10bff51de97c604f_MD5.png]]

Consider again some arbitrary path. Like we just discussed, the way we're going to handle it is by breaking it up into $N$ discrete steps, and approximating the curve as a zig-zag. Each piece of the trajectory is then just a straight line, and so it's actually not hard at all to write down the action for each segment, and then add it all up to get the total.

Consider the first segment, where the particle moves from position $xi$ to $x1$ in time $Δt.$ Since the trajectory is a straight line, the speed $dx/dt$ is constant—it's just the change in position over the change in time:

$$
dxdt=x1−xiΔt.
$$

And constant speed means that the kinetic energy $12mv2$ is constant, too:

$$
K0=12m(x1−xiΔt)2.
$$

And so, when we integrate that constant over the little time interval to get the action, we just get the length of time $Δt$ times the constant value of the kinetic energy,

$$
S0=12m(x1−xiΔt)2Δt.
$$

The action for the first segment of the zig-zag trajectory is then

$$
S0=m2Δt(x1−xi)2.
$$

Now we just need to do the same thing for all the other line segments, and then add them all up to get the total action for the whole trajectory.

They all take the exact same form, though. The second one goes from $x1$ to $x2,$ and so it contributes

$$
S1=m2Δt(x2−x1)2.
$$

And likewise, we add on and on from there, resulting in the total action for our discretized path:

$$
S=m2Δt{(x1−xi)2+(x2−x1)2+⋯+(xf−xN−1)2}.
$$

Raising the action to $eiS/ℏ,$ we therefore obtain the total weight for the path integral:

$$
eiS/ℏ=eiℏm2Δt{(x1−xi)2+(x2−x1)2+⋯+(xf−xN−1)2}.
$$

Finally then, we're ready to take this weight and plug it into our limiting definition of the path integral, which remember is given by integrating over all the intermediate values of $x$ :

$$
∫xixfDxeiS/ℏ=limN→∞A∫−∞∞dx1dx2⋯dxN−1 eiℏm2Δt{(x1−xi)2+(x2−x1)2+⋯+(xf−xN−1)2}.
$$

This is a little scary looking! But it’s actually nowhere near as bad as it looks. Because at this point we’ve managed to boil the whole path integral down to a handful of *ordinary* integrals over $x1,x2$ and so on.

And, in this simple example, each of those integrals is something we can evaluate exactly. They’re called **Gaussian integrals**, and there’s a famous formula for them that you might have run into before,

$$
∫−∞∞dx eiax2=πia.
$$

So we basically just need to apply that formula $N−1$ times over for each of the integrals over $x1,$  $x2,$ and so on.

Let’s start with the $x1$ integral. $x1$ appears in two of the terms in the exponent:

$$
∫−∞∞dx1eiℏm2Δt{(x1−xi)2+(x2−x1)2}=eiℏm2Δt(xi2+x22)∫−∞∞dx1 eiℏmΔt{x12−x1(xi+x2)}.
$$

We can evaluate this using the above Gaussian integral identity, or better yet, a slightly more general version obtained by completing the square in the exponent:

$$
∫−∞∞dx eia(x2+bx)=πiae−iab24.
$$

With $a=mℏΔt$ and $b=−(xi+x2),$ we obtain the following for the integral over $x1:$

$$
∫−∞∞dx1 eiℏm2Δt{(x1−xi)2+(x2−x1)2}=πiℏΔtmeiℏm4Δt(x2−xi)2.
$$

Notice the result depends on $x2.$ So we feed that back in, and perform the next integral over $x2$ using the same identity:

$$
πiℏΔtm∫−∞∞dx2 eiℏm2Δt(x3−x2)2eiℏm4Δt(x2−xi)2=πiℏΔtm4πiℏΔt3meiℏm6Δt(x3−xi)2.
$$

A pattern is starting to emerge, but let’s do one more to make it clear. For the integral over $x3,$ we get

$$
πiℏΔtm4πiℏΔt3m∫−∞∞dx3 eiℏm2Δt(x4−x3)2eiℏm6Δt(x3−xi)2=πiℏΔtm4πiℏΔt3m6πiℏΔt4meiℏm8Δt(x4−xi)2.
$$

Continuing on, the pattern is:

$$
N=2:πiℏΔtmeiℏm4Δt(x2−xi)2N=3:43(πiℏΔtm)2eiℏm6Δt(x3−xi)2N=4:84(πiℏΔtm)3eiℏm8Δt(x4−xi)2N=5:165(πiℏΔtm)4eiℏm10Δt(x5−xi)2.
$$

Extrapolating to general $N$ , the result of the Gaussian integrals is therefore

$$
∫−∞∞dx1⋯dxN−1 eiℏm2Δt{(x1−xi)2+(x2−x1)2+⋯+(xf−xN−1)2}=1N(2πiℏΔtm)N−1eiℏm2NΔt(xf−xi)2.
$$

Multiplying by the overall factor of $A$ and rearranging a bit, we obtain

$$
∫xixfDx eiℏS=limN→∞A(2πiℏΔtm)Nm2πiℏ(tf−ti)eiℏ12m(xf−xi)2tf−ti,
$$

where I used the fact that $NΔt=tf−ti.$

The result is a little complicated, but we can’t complain! Path integrals are famously hard to compute, and the fact that we can do this one exactly is a rare exception.

And we’re almost done now. The very last thing we need to do is take the limit as the number of steps $N$ goes to infinity.

To do so, notice that all the dependence on $N$ is contained in the factor $2πiℏΔt/m N$ out front. The rest of the formula just depends on the initial and final endpoints that we fixed.

Therefore, in order for the $N→∞$ limit to make sense, the $N$ dependence in that factor has got to be cancelled out. Fortunately, we still have the as-yet-undetermined constant $A$ to play with, which we now see must be the inverse of the $N$ -dependent factor:

$$
A=(m2πiℏΔt)N.
$$

That way, all the $N$ ’s disappear, and at long last we’re left with the exact result for the free particle path integral,

$$
Kfi=∫xixfDx eiS/ℏ=m2πiℏ(tf−ti)eiℏ12m(xf−xi)2tf−ti.
$$

This is the quantum mechanical amplitude $Kfi$ for a free particle to propagate from position $xi$ to $xf$ in the time interval $tf−ti.$

(More precisely, the above argument only fixes the $N$ -dependence of $A$ —it could also potentially contain additional factors that don't depend on $N.$ We can fix the overall factor by looking at the limit when $tf→ti.$ In that case, the particle hasn't had time to move anywhere at all, and the amplitude had better approach the identity. By doing so, we can verify that the above choice of $A$ is in fact the correct normalization.)

Next, we should of course discuss what this expression actually means, physically. Because there's an important general lesson about quantum mechanics lurking in this formula—namely, the uncertainty principle.

Our original question here was to determine the probability of finding the particle at position $xf,$ within a little window of width $dxf.$ And to go from the amplitude to the probability, we just need to take the absolute-value-squared, times that little width:

$$
Prob(xf)=|Kfi|2 dxf.
$$

In other words, the square of $Kfi$ tells us the probability *density* of finding the particle at any given point:

$$
Prob(xf)dxf=|Kfi|2.
$$

Let's therefore see what we get when we take the modulus-squared of our result for $Kfi.$

The second factor $eiℏ12m(xf−xi)2tf−ti$ is of the form $e$ to the $i$ times something, so it has absolute value one. As for the first factor, its absolute-value-squared gives us

$$
Prob(xf)dxf=m2πℏ(tf−ti)
$$

This at last is the probability density for finding the particle at position $xf$ at the final time, given that it started out at position $xi.$

There's something really surprising about it, though: the answer doesn't actually depend on the position at all!

![[Read It Later/attachments/a0270578710a4a377841ffcdffd49d81_MD5.png]]

In other words, if we plot the probability as a function of the final position, we just get a constant, horizontal line. And that means that the particle apparently has an equal chance of being found *anywhere* in space. But how can that be?

The reason comes down to another fundamental principle of quantum mechanics: the Heisenberg uncertainty principle, which says that the more precisely we try to pin down the position of a particle in space, the wider the range of velocities it can have.

And since we assumed here that the particle starts off at exactly position $xi,$ its initial velocity could be absolutely *anything*. And therefore the particle can shoot off arbitrarily quickly from that initial position to any other point in space when we go to measure it again later.

Of course, in reality we can’t know the initial position of the particle *exactly*, and so a more realistic initial setup with a finite window for the starting location would give us a smaller range of possible final positions and a normalizable probability distribution.

![[Read It Later/attachments/8eebae95c0598bf565926728112235ce_MD5.png]]

## Mathematical Subtleties

We've successfully computed the path integral for a free quantum mechanical particle! And, if you've taken a quantum mechanics class before, you could crack open your old textbook and verify that our formula for $Kfi$ is exactly the same result you would have computed before using the Schrödinger equation (more on that in a moment).

So the result of our calculation certainly seems to make sense. There are, however, a number of mathematical subtleties that I've swept under the rug in this first pass through the calculation. Before we wrap up, I should at least briefly point out the most important of those issues. The discussion will be highly schematic, however.

#### 1: The "Measure" Dx is Infinite!

With an ordinary integral,

$$
I=∫titfdt f(t),
$$
we sum up the values of a function $f(t)$ for each point $t∈[ti,tf]$ in a given range on a line, multiplying each value by the measure factor $dt,$ which you can think of as the width of an infinitesimally skinny rectangle located at that point.

For a path integral on the other hand,

$$
Kfi=∫xixfDx Φ[x],
$$
the notation suggests that we're similarly writing down the value of the functional $Φ[x]$ for each trajectory $x(t),$ multiplying the result by an analogous measure factor $Dx,$ and finally summing over all the allowed trajectories.

But what is this "measure" $Dx?$ Recall that we defined the path integral as the following limiting expression:

$$
∫xixfDx Φ=limN→∞(m2πiℏΔt)N∫−∞∞dx1 dx2⋯dxN−1 Φ,
$$

where I've explicitly included the value of the overall constant $A$ that we just worked out.

We're therefore led to identify $Dx$ with the quantity

$$
Dx=limN→∞(m2πiℏΔt)Ndx1 dx2⋯dxN−1.
$$

There's a problem, though: our overall constant

$$
A=(m2πiℏΔt)N
$$
 is undefined in the limit $N→∞!$ Indeed, since $Δt=tf−tiN$ , the absolute value of $A$ scales as $|A|∝NN/2.$

The factor $Dx$ therefore doesn't make sense on its own, and we shouldn't really call it a measure at all. (Though physicists still do so.)

Our calculation of the free particle path integral already reveals the resolution of this problem, however. After all, recall that we *chose* $A$ in the first place so as to compensate for the corresponding inverse factor that emerged as a result of all of our Gaussian integrals:

$$
∫xixfDxeiℏS=limN→∞  A(2πiℏΔtm)N⏟1  Kfi
$$

It's the combination of this factor of $A,$ together with the $N$ -dependence of the Gaussian integrals that result from the free particle weight $eiSfree/ℏ,$ that gives us a sensible limit.

Thus, we should really include the contribution from the free particle action, and regard the whole integrand $Dx eiSfree/ℏ$ as the path integral measure, which is then multiplied by the additional weight that's contributed after turning on a potential energy function $U.$

#### 2: Wick Rotation

Actually, mathematicians still aren't quite satisfied with the above construction of the path integral measure, because the $i$ in $eiS/ℏ$ means that the integrand is oscillatory rather than exponentially damped, making it difficult to define a convergent integral. It would be nicer if we had an integrand of the form $e−SE/ℏ,$ with a minus sign instead of an $i.$

In fact, we can achieve precisely that effect by performing a maneuver known as a **Wick rotation**.

Recall that the action is defined by the following integral along a given trajectory:

$$
S=∫dt{12m(dxdt)2−U}.
$$
 $t$ here is of course the time coordinate—it's a real number ranging between the initial and final times $ti$ and $tf.$

Suppose, however, that we instead define an *imaginary* time coordinate, $τ=it.$ Replacing $t's$ with $τ's$ in the action integral, a short calculation reveals that

$$
iS=−∫dτ{12m(dxdτ)2+U}⏟SE,
$$

where the **Euclidean action** is defined by

$$
SE=∫dτ{12m(dxdτ)2+U}.
$$

A couple of very interesting things have happened here. First of all, the pesky minus sign that appeared in the original action $∫dt (K−U)$ has given way to a plus sign, reminiscent of the total energy!

Second, Feynman's original weight $eiS/ℏ$ for the path integral has now been replaced by $e−SE/ℏ.$ We've therefore successfully traded the oscillatory weight for an exponentially damped one. One can now attempt to define a better-behaved *Euclidean* path integral with an imaginary time parameter, and then continue the results back to the real time values that we care about.

Needless to say, I'm being very schematic about how all that works in this brief explanation. For further details about strategies to construct the path integral in a mathematically rigorous way, see Chapter 20 of Hall's "Quantum Theory for Mathematicians."

#### 3: Non-Differentiable Paths

Finally, I should comment about what sorts of trajectories we actually want to integrate over in the path integral.

From the very beginning, we've insisted that every trajectory begin and end on the specified endpoints: $x(ti)=xi$ and $x(tf)=xf.$ But what sorts of paths are allowed in between?

We can of course consider smooth trajectories, like the straight line or parabolic arcs we might see for a classical particle. But, as we discovered in our explicit construction of the path integral, we can also have paths that zig-zag back and forth between widely separated values.

Therefore, the trajectories that we include in the path integral aren't necessarily nice and smooth, differentiable curves. In fact, it's essential that we include non-differentiable trajectories in order to reproduce many of the key features of quantum mechanics, such as the fact that operators that act in different orders need not commute.

When we write down expressions like the free particle action

$$
Sfree=∫dt 12m(dxdt)2,
$$

that involve derivatives of $x(t),$ we should therefore interpret those derivatives as the slopes of line segments making up the path:

$$
Sfree=∑j=0N−1Δt⋅12m(xj+1−xjΔt)2.
$$

We did just that in our earlier calculation of the free particle path integral.

## The Schrödinger Equation

Finally, let me wrap up this lesson by coming back to something I mentioned at the beginning—the connection between Feynman's path integral approach to quantum mechanics and Schrödinger's formulation in terms of wavefunctions.

Because these are not two separate theories—they're just two different perspectives on the same underlying physics. In fact, the amplitude $Kfi$ that we've computed with the path integral *is* the wavefunction for a free particle that started out at position $xi:$

$$
Kfi=∫xixfDx eiS/ℏ=m2πiℏ(tf−ti)eiℏ12m(xf−xi)2tf−ti.
$$

To simplify the notation a little, let's suppose that the particle started out at the origin at time zero. Then we can set $xi$ and $ti$ to zero in our formula for $Kfi:$

$$
Kfi=m2πiℏtfeiℏ12mxf2tf.
$$

And we also don't really need the final $f$ subscripts anymore, so we can get rid of those as well. The resulting function of the final position and time is then the wavefunction for this particle after we release it from the origin:

$$
Ψ(x,t)=m2πiℏteiℏ12mx2t.
$$

As for any wavefunction, it had better satisfy the Schrödinger equation, which, for a free particle, says that taking the time derivative of $Ψ$ is the same as taking two derivatives with respect to $x,$ up to some constant factors:

$$
iℏ∂Ψ∂t=−ℏ22m∂2Ψ∂x2
$$

Let's see if it works. We just need to evaluate these two derivatives of our function $Ψ.$ I'll let you grab a piece of paper and compute those for yourself. You should get

$$
∂Ψ∂t=−12t(1+imℏtx2)Ψ
$$

for the derivative with respect to $t,$ and

$$
∂2Ψ∂x2=imℏt(1+imℏtx2)Ψ
$$

for the derivative with respect to $x.$

Then lo and behold, when we multiply the $t$ derivative by $iℏ,$

$$
iℏ∂Ψ∂t=−iℏ2t(1+imℏtx2)Ψ,
$$

and when we multiply the $x$ derivative by $−ℏ22m$ ,

$$
−ℏ22m∂2Ψ∂x2=−iℏ2t(1+imℏtx2)Ψ,
$$

we wind up with the exact same thing.

And so this wavefunction does in fact satisfy the Schrödinger equation, as promised. But using the path integral we were able to derive it without ever even talking about the Schrödinger equation, and just considering regular old particle trajectories—albeit an infinite number of them.

## More to Learn

To fully understand Feynman’s path integral formulation of quantum mechanics, you need to start with a strong foundation in the Lagrangian formulation of *classical* mechanics. I’ve created [an entire course](https://courses.physicswithelliot.com/lagrangian-fundamentals-page) covering the key ideas of Lagrangian mechanics—complete with lesson videos, practice problems, and detailed solutions.

[![[Read It Later/attachments/c335cea3752e0cf514b0516dff4cfc06_MD5.png]]](https://courses.physicswithelliot.com/lagrangian-fundamentals-page)

Enroll in [Fundamentals of Lagrangian Mechanics](https://courses.physicswithelliot.com/lagrangian-fundamentals-page) right now to start mastering a whole new way of thinking about physics!

---

See also:

- [Origins of the Quantum Wavefunction (Quantum Mechanics Part I)](https://www.physicswithelliot.com/wavefunction-mini-notes)
- [The Quantum Path Integral, Explained (Quantum Mechanics Part II)](https://www.physicswithelliot.com/path-integral-mini-notes)
- [The Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [Field Theory Fundamentals](https://www.physicswithelliot.com/fields-mini-notes)
- [Discovering the Fourier Transform Through Quantum Mechanics](https://www.physicswithelliot.com/fourier-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).