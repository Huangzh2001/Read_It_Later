---
date: "2025-08-10T22:05:57+08:00"
url: "https://www.physicswithelliot.com/path-integral-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=Sp5SvdDh2u8)

## Introduction

Richard Feynman won the Nobel prize in 1965 for understanding the quantum physics of light and how it interacts with matter.

But long before he was a famous Nobel prize winner—as a matter of fact, when he was just a 20-something year old graduate student—Feynman’s first great discovery was an entirely new way of thinking about quantum mechanics, which in the 80 years since has proven essential to our modern understanding of quantum physics.

It’s called the **path integral formulation** of quantum mechanics. And once you understand it, Feynman’s approach will give you a huge amount of insight into the strange way that things behave in the quantum world. And at the same time, it will explain the origins of the much more familiar laws of classical physics like $F=ma$ , as we zoom out from studying tiny things like electrons to everyday objects like baseballs.

Quantum physics is all about the laws of nature on the smallest scales—the physics of atoms and protons and electrons and so on. And to give you an idea of just how different it is compared to classical physics, let’s start by comparing and contrasting the classical and quantum versions of a very simple problem.

Say we’ve got a particle that starts out at some position $xi$ at an initial time $ti$ .

In classical mechanics, our job would be to figure out where the particle is going to be at any later time. Newton gave us a systematic way to do that. We add up all the forces, set that equal to the mass of the particle times its acceleration,

$$
md2xdt2=F,
$$

and then solve this equation for the position $x(t)$ as a function of the time $t$ . That gives us the trajectory of the particle, and it tells us precisely where it will be at any time.

If it’s a free particle, meaning that there are no forces acting on it, then the solution to this equation is just a straight line:

![[Read It Later/attachments/6b450f282c5de1104098dea6fa29d276_MD5.png]]

Here, I’m plotting the position $x$ of the particle on the vertical axis, and the time $t$ on the horizontal axis.

Or if it’s a baseball that we’re throwing up in the air with the force of gravity pulling it back down, the trajectory would be a parabola:

![[Read It Later/attachments/0b9f44e2edb0e20e196f636432b84999_MD5.png]]

(And in that case we’d more often use the letter “ $y$ ” for the vertical coordinate.)

Either way, we can predict the final position $xf$ where we’ll find the particle when we go to measure it at a later time $tf$ .

Quantum mechanics is fundamentally different, though. If we’re told that a quantum particle was found at position $xi$ at the initial time $ti$ , then all we can predict for when we measure its position again later is the *probability* that we’ll find it at position $xf$ . If you do the same experiment many times over, sometimes you’ll find the particle around there, and sometimes you’ll find it somewhere else. In fact, the particle generally doesn’t even have a well-defined position until we go to measure it.

This probabilistic nature of quantum mechanics is one of the most counterintuitive aspects of the laws of physics at such tiny scales. It means that a quantum particle doesn’t follow a single, well-defined trajectory anymore in getting from one point to another.

And in fact, the incredible thing that Feynman discovered is that instead of following a single trajectory like in classical mechanics, a quantum particle weighs *all* the conceivable paths connecting the first point to the second, and it does a kind of sum over all those possibilities:

![[Read It Later/attachments/ca33e2b38a56155e9b7039d579cf0469_MD5.png]]

That sum over all trajectories is what we call the path integral, and it’s pretty mind-boggling, to say the least. We’ll be seeing what it means in detail as we go along, but this basic fact that we have to consider every possible trajectory for a microscopic particle was Feynman’s key insight into the nature of quantum mechanics.

The original approach to quantum mechanics, as it was formulated by people like Schrödinger and Born and many others back in the 1920s, is to describe the particle not by its trajectory $x(t)$ , but by a **wavefunction**, $ψ(x,t)$ , which is a function of space and time that tells us how likely we are to find the particle at a given position at any given moment. And in the [previous lesson](https://www.physicswithelliot.com/wavefunction-mini-notes), we saw how this idea of the wavefunction comes about.

For example, when the particle is initially located near position $xi$ , the wavefunction would look something like this, sharply peaked around that position:

[[Read It Later/attachments/47c83ece016d773f99a78a3c506cae92_MD5.png|Open: 47c83ece016d773f99a78a3c506cae92_MD5.png]]
![[Read It Later/attachments/47c83ece016d773f99a78a3c506cae92_MD5.png]]

And the rules of quantum mechanics say that *square* of the wavefunction tells us the probability of finding the particle at that position when we go to make a measurement:

$$
Prob(x,t)∝|ψ(x,t)|2.
$$

In the lingo of quantum mechanics, $ψ$ is called a **probability amplitude**. And we take the modulus-squared of the amplitude to get the actual probability.

If you’ve taken a class on quantum mechanics before—and I’m not assuming that you have for this lesson—but *if* you have, then you almost certainly learned about this Schrödinger approach in terms of wavefunctions, and the Schrödinger equation, and so on.

That’s all well and good, but Feynman’s path integral gives us another way of approaching quantum mechanics. It’s completely equivalent to the Schrödinger formulation, but it provides a powerful new perspective and intuition for the physics.

I’ll give you a quick sketch of how the path integral works right at the beginning here, just so you have a rough idea of where we’re going, and then we’ll spend the rest of the lesson unpacking where it all comes from and what it means.

What we’re interested in is the probability amplitude for a particle that started at position $xi$ at time $ti$ to be found at position $xf$ at a later time $tf$ . This amplitude is actually one of the central mathematical objects of quantum mechanics, so we give it a special name. It’s called the **propagator**, and I’ll write it as $Kfi$ , to stand for the amplitude for the particle to start from point $i$ and “propagate” onward to point $f$ . (The $K$ stands for "kernel," by the way, for reasons we don't need to get into right now.)

And here’s Feynman’s path integral prescription for computing the propagator. Again, classically, the particle would follow a single, unique trajectory between those points. But in quantum mechanics, Feynman discovered that we need to consider every possible trajectory that passes between them.

Each of those possible paths contributes with a particular weight, which is written as $eiS/ℏ$ . $ℏ$ is **Planck’s constant**, which is the fundamental physical constant of quantum mechanics. And $S$ is a certain number that’s associated to each trajectory, called its **action**.

If you’ve studied some [upper-level classical mechanics](https://courses.physicswithelliot.com/lagrangian-fundamentals-page) before—or if you’ve watched some of the [previous lessons](https://www.physicswithelliot.com/least-action-mini-notes) I’ve posted—you may have encountered this action quantity before, because it’s something that's already very important in what’s called the **Lagrangian formulation** of classical mechanics. I’ll explain precisely how it’s defined later on, but again $S$ is just a number that we can compute for each trajectory.

And now to find the total amplitude for the particle to propagate from point $i$ to point $f$ , we add up these contributions from all the possible paths:

$$
Kfi=∑pathseiS/ℏ.
$$

This is Feynman’s procedure for computing the quantum mechanical amplitude. It’s really kind of incredible when you stop and think about it. Instead of following a single path like in classical mechanics, a quantum particle does a kind of statistical average of every conceivable path.

Of course, the set of all these paths isn’t a discrete list, so this isn’t really a discrete sum. It’s a sort of integral, called a **path integral**, and so we more often write it using a notation like this:

$$
Kfi=∫Dx eiS/ℏ.
$$

And that’s why this is called the path integral formulation of quantum mechanics.

How we actually go about mathematically *defining* a "sum over all paths" is a tricky subject that we'll take up in the [next lesson](https://www.physicswithelliot.com/path-integral-part-3-mini-notes). For this lesson, we'll focus on understanding the physical idea behind the sum over paths.

If you’re sitting there thinking: “How the heck can the particle be taking an average of every possible path? When I throw a baseball up in the air, it most definitely follows a single, well-defined trajectory.”

Well, stay tuned. Because the answer to that question is one of the deepest lessons that the path integral reveals about the connection between quantum and classical mechanics. The short answer is that for a baseball, only one contribution to this sum over paths survives: and that’s the path that obeys $F=ma$ . That’s how quantum mechanics “predicts” Newton’s law.

It’s a good story how Feynman came up with the idea of the path integral in the first place. He talks about it in his [Nobel prize speech](https://www.nobelprize.org/prizes/physics/1965/feynman/lecture/). First of all, he had a huge hint thanks to an [earlier paper by Dirac](https://www.worldscientific.com/doi/10.1142/9789812567635_0003) from 1932, where Dirac realized that the quantum mechanical amplitude somehow corresponds to this quantity $eiS/ℏ$ .

Feynman tells the story of how he was at a bar in Princeton, when he ran into a visiting professor who told him about this paper of Dirac’s. And the next day they went to the library together to find the paper, and then Feynman derived the basic idea of the path integral on a blackboard right in front of the astonished visiting professor.

But anyway, now we need to actually understand what the heck all this means. And the intuitive idea behind Feynman’s sum over paths starts from the double-slit experiment that we discussed in the last lesson.

## Beyond the Double-Slit Experiment

In the [last lesson](https://www.physicswithelliot.com/wavefunction-mini-notes), we learned about the unexpected way that quantum particles behave by discussing a famous experiment called the double-slit experiment.

![[Read It Later/attachments/1bfd7dbc87ae1243aaa5a4b67b50ad87_MD5.png]]

We took a solid wall, and punched out two holes or slits in it. Then we chucked different things at the wall and recorded what made it through to the other side, and where. The results varied depending on whether we sent in classical particles (like BB pellets), classical waves (like light waves), or quantum particles (like electrons).

And the surprising thing we discovered is that a quantum particle doesn't move along a single, well-defined trajectory in the way we're used to for classical particles. A quantum particle fired at the double-slit apparatus somehow probes both holes at once, resulting in an interference pattern for the distribution of where we detect the particles that make it through to the opposite side.

[[Read It Later/attachments/ac7c1d31c107b1695efa412106953d4d_MD5.png|Open: ac7c1d31c107b1695efa412106953d4d_MD5.png]]
![[Read It Later/attachments/ac7c1d31c107b1695efa412106953d4d_MD5.png]]

Last time we saw how to describe what’s going on mathematically using Schrödinger’s idea of the wavefunction. For each particle, we wrote down a wavefunction $ψinc$ that described the incoming wave. After the wave strikes the barrier, two spherical waves $ψ1$ and $ψ2$ emerge from the holes on the other side. Those wavefunctions were of the form $eiϕ(r)$ , where the phase $ϕ(r)$ was proportional to the distance from the hole to the detector.

![[Read It Later/attachments/5a67736ca13fd49525002c5470876088_MD5.png]]

But there’s another way of thinking about all this that lets us phrase things in terms of regular old particle trajectories $x(t)$ , instead of jumping straight to this new idea of a wavefunction $ψ$ . The catch is that a single trajectory passing through one hole won’t cut it anymore. We have to consider trajectories that pass through each hole in order to understand the interference pattern that we observe.

[[Read It Later/attachments/4d0c36dbefebaf258eebbeb8a123ddd8_MD5.png|Open: 4d0c36dbefebaf258eebbeb8a123ddd8_MD5.png]]
![[Read It Later/attachments/4d0c36dbefebaf258eebbeb8a123ddd8_MD5.png]]

But now let’s push that idea a little further. If we drill a third hole in the barrier, we’ll have to include trajectories that pass through that hole, as well. And the same goes if we drill a fourth hole, or a fifth and sixth, and so on.

While we're at it, let’s go ahead and add another solid barrier in between, and drill a few holes in that. Then we have to consider all the possible combinations: the particle might pass through the first hole of the first barrier and then the first hole of the next barrier, or it could go from the second hole to the third, and all the other possibilities.

Now take this idea to the logical extreme. We completely fill the region with parallel barriers, and through each one we drill many, many little holes. Then we need to account for all the possible routes the particle could take, traveling from any one hole to any other on its way across.

![[Read It Later/attachments/c52a71f827b595546969d08df6e61ee6_MD5.png]]

In fact, we can imagine drilling *so* many holes that the barriers themselves effectively disappear. (We used a very similar argument when we talked about Huygen’s principle last time.) We drill through all the barriers until we’re effectively left with empty space again.

Then what this reasoning suggests is that to find the total amplitude for the particle to propagate from its initial point to some final point at the detector, we need to add up the individual amplitudes from each and every possible path that the particle might follow in traveling between those two endpoints.

And that’s how what we learned from the double-slit experiment leads us to the idea that we need to sum over all paths to compute the quantum mechanical amplitude.

Let’s suppose, much like in our discussion of waves, that each of those trajectories contributes to the sum with a particular complex phase:

$$
Kfi=∑pathseiϕ,
$$

where $ϕ$ is some number that we assign to each path which determines how it contributes to the total amplitude.

This is the core idea of the path integral. And it’s pretty incredible compared to our usual experience. We’re used to finding a single classical trajectory, for, say, the position $x$ as a function of the time $t$ . Maybe it’s a straight line, or a parabola, or whatever.

But in quantum mechanics we need to count every possible trajectory that the particle could conceivably follow. For each path, we write down the phase $eiϕ$ that it contributes, and then add them all up to find the total amplitude.

Strange as it sounds, this prescription is at least totally “democratic,” in the sense that each term in the sum is a complex number with the same magnitude: one.

You can picture $eiϕ$ as an arrow in the complex plane. In other words, we draw a picture with the real direction along the horizontal axis and the imaginary direction along the vertical axis. Then $eiϕ$ is an arrow of length one, that points at an angle $ϕ$ .

[[Read It Later/attachments/6da0aa337a4148259f91d922bb264668_MD5.png|Open: 6da0aa337a4148259f91d922bb264668_MD5.png]]
![[Read It Later/attachments/6da0aa337a4148259f91d922bb264668_MD5.png]]

That follows from Euler’s identity, $eiϕ=cos⁡ϕ+isin⁡ϕ$ . The real (i.e. horizontal) component is $cos⁡ϕ$ and the imaginary (i.e. vertical) component is $sin⁡ϕ$ . And those are the two legs of a right triangle whose hypotenuse has length 1 and is inclined at the angle $ϕ$ .

Different trajectories will contribute arrows pointing at different angles, but they all have the same length of one.

The question is, what angle $ϕ$ should we pick for each possible path? Well, I already mentioned the answer back at the beginning. For each trajectory, the complex phase it contributes is given by $eiS/ℏ.$

$ℏ$ is the quantum mechanical constant, called Planck’s constant. $S$ , meanwhile, is the **action**, which is a particular number that we can compute for any given trajectory.

Here’s how it’s defined. We take the kinetic energy of the particle at each moment, $12mv2,$ subtract from that the potential energy $U,$ and then we integrate that quantity over the time interval from $ti$ to $tf$ ,

$$
S=∫titfdt (K−U).
$$

The result is a number that we can compute for any given trajectory, and that’s its action.

The quantity $K−U$ that we’re integrating here gets its own special name, by the way: it’s called the **Lagrangian**, $L=K−U$ , so that the action is defined by integrating the Lagrangian over time. And yes, that really is a minus sign in the middle—more on that in a minute.

Depending [how much classical mechanics](https://courses.physicswithelliot.com/lagrangian-fundamentals-page) you’ve studied before, seeing the action and Lagrangian appear here might be ringing enormous bells in your head—or these formulas might look totally out of left field!

So let me try to motivate where this weight $eiS/ℏ$ for the different paths is coming from.

First of all, let’s just think about the units we have to play with here. Planck’s constant $ℏ$ , in SI units, is given approximately by

$$
ℏ≈10−34 Joule⋅second.
$$

In particular, it has units of energy (in Joules) times time (in seconds).

We certainly expect $ℏ$ to appear in our weight factor $eiϕ$ , since again it’s the fundamental constant of quantum mechanics. But $ϕ$ is an angle, remember—it’s measured in radians, say, and doesn’t have any dimensions. So we’ll have to pair the $ℏ$ up with something else with those same units of energy times time in order to cancel them out. The simplest thing we could write is a ratio:

$$
ϕ=Sℏ.
$$

And the action $S=∫dt (K−U)$ indeed has those units we’re looking for. $K$ and $U$ are the kinetic and potential energies of the particle, and they get multiplied by time when we integrate over $t$ .

So the units at least work out correctly, otherwise it wouldn’t even make sense to write down this quantity $eiS/ℏ$ . You might be wondering, though, why the heck are we taking the *difference* between the kinetic and potential energy? Wouldn’t it seem more natural to write the *total* energy like we’re much more accustomed to working with in classical mechanics?

$$
S=?∫titfdt (K+U).
$$

That’s certainly what I imagine *I* would have probably tried first if I’d been working on this problem a hundred or so years ago.

But that’s wrong. It’s most definitely a minus sign that appears in this formula for the action. And we’ll see why after we’ve talked about the second key piece of motivation for where this weight $eiS/ℏ$ comes from: it ensures that the unique, classical trajectory emerges when we zoom out from studying tiny, quantum mechanical particles to bigger, everyday objects.

It’s not at all obvious how that works at first glance at Feynman’s formula,

$$
Kfi=∑pathseiS/ℏ.
$$

If this is telling us to sum over all paths that the particle could follow—each with the same magnitude and just different phases—how could that possibly be consistent with what we observe in our daily lives, where a baseball thrown up in the air most definitely follows a single, parabolic trajectory? After all, quantum mechanics is the more fundamental theory, and our everyday laws of classical mechanics must emerge from it in the appropriate limit.

The answer to this question is one of the most profound insights the path integral reveals about the laws of physics. It will show us how $F=ma$ follows from this more fundamental quantum mechanical description.

## The Classical Limit

What happens is that, for the motion of a classical object like a baseball, almost all the terms in the sum over paths cancel each other out and add up to nothing—all except one, and that’s the classical path. And here’s why.

Each term $eiS/ℏ$ in the sum corresponds to an arrow in the complex plane. It has length one, and points at an angle set by $S/ℏ$ . So we pick any trajectory connecting the initial point to the final point. We compute the action $S$ for that path, divide by $ℏ$ , and then we draw the corresponding arrow at that angle.

If we pick a different trajectory, we’ll get some other value for the action, and that will give us another arrow at some other angle. And what we need to do is add all the arrows up.

Here’s the thing, though: $ℏ$ is really, really, *really* tiny. Again, in SI units, its value is of order $10^{-34} ~~\\mathrm{J\\cdot s} $.Bycomparison,atypicalactionforabaseballwillbesomethinglike$ 1~~ \\mathrm{J\\cdot s} $—maybegiveortakeafewordersofmagnitudeineitherdirection—butit′svastlylargerthanthevalueof$ \\hbar$.

And so the angle $S/ℏ$ will be an *enormous* number for a typical path for a baseball—on the order of $1034$ radians. Starting from $ϕ=0$ , it’s like we flicked the arrow so hard that it spins around and around a bajillion times, until it lands in some random direction.

But now let’s pick a slightly different trajectory and consider what that contributes to the sum. Suppose it’s a very similar path to the one we started with, so that its action will only be slightly different from the first one. Maybe the first path had an action of $1 ~~\\mathrm{J\\cdot s} $andthisnewonehas$ 1.01~~ \\mathrm{J\\cdot s} $,say,sothatthechangeinthevalueoftheactionbetweenthemis$ 0.01 ~\\mathrm{J\\cdot s} $.Itdoesn′tmatterwhattheprecisenumbersare,becausewhenwedividebytheincrediblytinyvalueof$ \\hbar$, even that small change in the action at the *classical* scale will produce a massive change in the angle—in this case something of order $1032$ radians.

[[Read It Later/attachments/5d0c1ba0bad9a63aa28726be809e9e16_MD5.png|Open: 5d0c1ba0bad9a63aa28726be809e9e16_MD5.png]]
![[Read It Later/attachments/5d0c1ba0bad9a63aa28726be809e9e16_MD5.png]]

Then even though the two trajectories were only slightly different, their corresponding arrows point in random different directions in the complex plane. And as we include more and more curves, each of them will give us an arrow in some other random direction, too. We’ll get an incredibly dense array of arrows pointing in all directions around the unit circle.

![[Read It Later/attachments/8418f56d3095aeb7eaabae4679824bfc_MD5.png]]

According to Feynman’s formula, what we’re supposed to do is add up all these arrows for all the different paths, just like you’d add vectors together. But since they’re all pointing in random directions, when we add them all up, they simply cancel each other out, and seemingly give us nothing!

Thus, for a classical object where the actions involved are much bigger than $ℏ$ , almost all the terms in the sum over paths add up to zero.

*Almost*. There’s one crucial exception. Again, the reason a generic path doesn’t wind up contributing anything is that its neighbors, which differ from it only very slightly in shape, have significantly different actions, at least on the scale set by $ℏ$ . Then the corresponding arrows point in random different directions, and they tend to cancel out when we sum over many paths.

But suppose that there is some special trajectory for which the action is approximately the same for it and for any nearby path. Then the arrows for *those* nearby trajectories would point in very nearly the same direction, and those wouldn’t cancel out. Trajectories near such a path would add up coherently and survive, whereas everything else in the sum cancels out.

![[Read It Later/attachments/e543983787b481856a78064e75165ed1_MD5.png]]

A special path like that, where the action is approximately constant for any nearby trajectory, is called a **stationary path**, and those are the only contributions that survive in the limit when $ℏ$ is very small compared to the action.

What that means is, if you start from a stationary path $x(t)$ , and you make a tiny variation of it, by adding some little wiggles, say, then the value of the action is the same for the new curve as it was for the old one—at least to first order:

$$
S[x+δx]=S[x]+O(δx2).
$$

That might sound like something fancy, but it’s just like finding the stationary points of an ordinary function, like a minimum, say. When you take a tiny step away, the value of the function is constant to first order because the slope vanishes at that point. Finding the stationary trajectory is totally analogous, it’s just a little harder since we’re looking for a whole path now instead of a single point.

But at last, what we’ve discovered is that in the classical limit the only trajectory that actually winds up contributing to the sum over paths is the path of stationary action. And yes, the stationary path *is* the classical trajectory.

In particular, when we plug the definition of the action $S=∫dt (K−U)$ into the stationary path condition, we'll find that a trajectory will be stationary if and only if it satisfies

$$
md2xdt2=−dUdx.
$$

And that’s nothing but $F=ma$ , because remember the force on a particle and the potential energy are related by

$$
F=−dUdx.
$$

Let's prove it.

Consider a trajectory $x(t)$ , and any nearby trajectory $x(t)+δx(t)$ , obtained by adding some little wiggles described by a tiny function $δx$ . What we need to do is compare the action $S[x+δx]$ for the new curve to the value of the action $S[x]$ for the original curve. $x(t)$ will be a stationary path if these actions agree to first order in $δx$ for any such tiny variation.

The original action was

$$
S[x]=∫titfdt (12m(dxdt)2−U(x)).
$$

To write the action for the wiggly path, just substitute $x→x+δx$ :

$$
S[x+δx]=∫titfdt (12m(dxdt+ddtδx)2−U(x+δx)).
$$

Let’s work on the two terms one at a time. For the kinetic energy, we expand out

$$
(dxdt+ddtδx)2=(dxdt)2+2dxdtddtδx+(ddtδx)2.
$$

But remember, $δx(t)$ is tiny, by assumption. And we only need the two actions to agree to first order in $δx$ . So we don’t need to keep track of the last term that’s proportional to $(δx)2$ . That leaves us with

$$
S[x+δx]≈∫titfdt (12m(dxdt)2+mdxdtddtδx−U(x+δx)).
$$

Now for the potential energy term, we likewise want to expand $U(x+δx)$ to first order in $δx$ . And for that we just need to apply the [Taylor series](https://www.physicswithelliot.com/taylor-help-room-notes):

$$
U(x+δx)=U(x)+U′(x)δx+12U″(x)(δx)2+⋯.
$$

Once again, we’ll drop everything proportional to $(δx)2$ and above, leaving

$$
S[x+δx]≈∫titfdt (12m(dxdt)2+mdxdtddtδx−U(x)−U′(x)δx).
$$

This looks a little complicated, but we can simplify it quite a bit. First of all, let’s organize it into two pieces—the terms with a factor of $δx$ and the ones without:

$$
S[x+δx]≈∫titfdt (12m(dxdt)2−U(x))+∫titfdt (mdxdtddtδx−U′(x)δx).
$$

The first integral here—without any $δx$ ’s—is just the original action $S[x]$ . And that’s what we want to reproduce for the new action $S[x+δx]$ . Which means that the second integral had better vanish:

$$
∫titfdt (mdxdtddtδx−U′(x)δx)=0.
$$

Thus, in order for $x(t)$ to be stationary, this integral must equal zero for any tiny variation $δx(t)$ we make to the path.

Or rather, not quite *any* variation. Remember that we fixed the endpoints $(ti,xi)$ and $(tf,xf)$ of the path. We don’t want to change those when we vary $x(t)→x(t)+δx(t)$ , so we’ll only allow for variations that don’t affect the endpoints:

$$
δx(ti)=δx(tf)=0.
$$

That’s not just some technical assumption—we can use it to dramatically simplify the integral.

Right now, the integral expression is a little awkward, since there’s a $ddt$ acting on the $δx$ in the first term, but not the second. What we’d like to do is pull out a common factor of $δx$ . And we can do that by integrating-by-parts on the first term:

$$
dxdtddtδx=−d2xdt2δx+ddt(dxdtδx),
$$

which you can check using the product rule for derivatives.

That lets us rewrite our integral as

$$
∫titfdt (−md2xdt2−U′(x))δx+∫titfdt ddt(mdxdtδx)=0.
$$

We’re almost there! Do you see $F=ma$ peeking out of that first set of parentheses?

To bring it home, we need to get rid of the second integral. It’s easy enough to evaluate, since it’s the integral of a derivative:

$$
∫titfdt ddt(mdxdtδx)=(mdxdtδx)|titf.
$$

But remember, $δx(t)$ vanishes at $ti$ and $tf$ ! Thus, this integral indeed disappears.

Then at last, what we’re left with is the condition

$$
∫titfdt (md2xdt2+U′(x))δx=0.
$$

$x(t)$ will be a stationary path if and only if this integral vanishes for any variation $δx(t)$ we might make.

But the only way this thing can vanish for *any* $δx$ is if the quantity that’s multiplying $δx$ in the integrand is itself equal to zero! Therefore, the condition for $x(t)$ to be stationary is that

$$
md2xdt2=−U′(x).
$$

And that, as promised, is $F=ma$ .

This is how the path integral predicts $F=ma$ . It’s not that the classical trajectory makes some huge contribution to the sum that dominates over all the other terms. Every term $eiS/ℏ$ in the sum has the same magnitude: one. The classical path wins out because that’s where the action is stationary, and so the arrows near that trajectory all point at the same angle, and they add together instead of getting canceled out.

What I’m describing here—the way the stationary contribution dominates the sum over $eiS/ℏ$ —is called the **stationary phase approximation**, by the way. You might even have seen the same idea before in a calculus class, in the context of ordinary integrals.

But that was for a classical object like a baseball. For something like an electron, on the other hand, the size of the action will be much smaller—close to the scale of $ℏ$ . So the angles $S/ℏ$ won’t be such huge numbers anymore. And that means that the arrows for non-classical paths don’t necessarily cancel out.

Then in the quantum regime it’s not true that only the single, classical trajectory survives—there can be a wide range of paths that contribute, and $F=ma$ therefore isn’t very relevant when it comes to understanding the behavior of quantum particles. That’s why we observed interference when we fired electrons at our double-slit apparatus, but not when we fired BB gun pellets.

And like I promised to explain before: when we defined the action, if we had flipped the sign and used $K+U$ instead of $K−U$ , like we might have at first guessed, the equation for the stationary path would have come out the same but with the sign of $U$ flipped,

$$
md2xdt2=+dUdx.
$$

But that would have said that $ma=−F$ instead of $F=ma$ ! So we indeed need to take the difference $K−U$ in order to get the correct predictions for classical physics.

The fact that the trajectory of a classical particle makes the action stationary is called the principle of stationary action. Actually, more often than not, the classical trajectory comes out to be a *minimum* of the action, and so it’s more common to call this the principle of least action. It’s one of the most fundamental principles in physics, much more fundamental than $F=ma$ , and now we’ve seen how it emerges from quantum mechanics.

## Conclusion

Hopefully you now understand how the intuitive idea behind the path integral emerges from the double-slit experiment, and how it explains the origin $F=ma$ in the classical limit.

But I’ve been very vague so far about how we’re actually supposed to define and compute this sum over the space of all possible paths. And if you’re mathematically-minded, you’ve probably been squirming a little in your chair wondering how the heck to make sense of this formula.

Like I mentioned at the beginning, the set of all these paths isn’t a discrete list, and so we’re not actually talking about a standard sum here. Instead, it’s a kind of integral—a **path integral**. And in the [next lesson](https://www.physicswithelliot.com/path-integral-part-3-mini-notes), I’m going to show you how we’d actually go about defining and evaluating this thing in a simple example.

Meanwhile, there’s a ton more to explore here if you’re interested in learning more. To learn from the man himself, you can read the book “Quantum Mechanics and Path Integrals” by Feynman and Hibbs. The approach to the path integral that I’ve taken here was very much inspired by what’s described in that book.

If you're interested in the history, you can find Feynman's PhD dissertation [published here](https://www.worldscientific.com/worldscibooks/10.1142/5852#t=aboutBook) and his follow-up paper introducing the path integral [here](https://www.semanticscholar.org/paper/Space-Time-Approach-to-Non-Relativistic-Quantum-Feynman/312c23a35beb067492b21d1ad5b04570485a00a3).

To really understand all this, though, you need to start with a strong foundation in the Lagrangian formulation of classical mechanics and the principle of least action. And to master that, you can enroll in my online course, [Fundamentals of Lagrangian Mechanics](https://courses.physicswithelliot.com/lagrangian-fundamentals-page):

[[[Read It Later/attachments/c335cea3752e0cf514b0516dff4cfc06_MD5.png|Open: c335cea3752e0cf514b0516dff4cfc06_MD5.png]]
![[Read It Later/attachments/c335cea3752e0cf514b0516dff4cfc06_MD5.png]]](https://courses.physicswithelliot.com/lagrangian-fundamentals-page)

---

See also:

- [Origins of the Quantum Wavefunction (Quantum Mechanics Part I](https://www.physicswithelliot.com/wavefunction-mini-notes))
- [The Quantum Path Integral, Computed (Quantum Mechanics Part III)](https://www.physicswithelliot.com/path-integral-part-3-mini-notes)
- [The Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [Field Theory Fundamentals](https://www.physicswithelliot.com/fields-mini-notes)
- [Discovering the Fourier Transform Through Quantum Mechanics](https://www.physicswithelliot.com/fourier-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).