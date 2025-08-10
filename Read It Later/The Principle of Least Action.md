---
date: "2025-08-10T22:10:20+08:00"
url: "https://www.physicswithelliot.com/least-action-mini-notes"
status:
---
## Explaining the Principle of Least Action

![](https://www.youtube.com/watch?v=sUk9y23FPHk)

The **principle of least action** is one of the most profound and far-reaching ideas in physics. It's a different way of looking at things that underlies a huge amount of what we humans have learned about the world in the last few hundred years—from Newtonian mechanics, to relativity, to quantum mechanics, and quantum field theory.

![](https://www.physicswithelliot.com/s/paths.png)

The basic idea goes like this: say you have a particle that travels from point 1 to point 2. What trajectory is it going to follow to get there? Newton gave us one approach to answering this question, but beginning in the 17 and 1800s Lagrange and Hamilton and others developed a different strategy. They assigned a number to each possible path called the **action**, and showed that the path the particle actually takes is the one that *minimizes* the action. Actually, in *quantum* mechanics, Feynman showed that the particle in a sense traverses *all* the possible paths, and the classical path that minimizes the action is the one that dominates.

But we're getting ahead of ourselves. What I want to do here is explain the principle of least action and show how it reproduces the equations you already know and love from Newton's laws. This is the first in a series I'm working on in which I hope to show you the action principle not only in Newtonian mechanics, but in special relativity and general relativity, and even in string theory too, in as accessible a way as possible. For right now I'll just assume that you're familiar with Newton's law $F=ma$ , potential energy, and some basic calculus.

So let's say we have a particle of mass $m$ that travels from the point $x1$ at time $t1$ to $x2$ at time $t2$ . What trajectory $x(t)$ is it going to follow to get there? I'm going to work with one spatial dimension $x$ here to keep things from getting unnecessarily complicated, but of course all of this discussion will generalize to three dimensions.

Newton told us that to answer this question we should write down all the forces on the particle, add them up, and then set that equal to the mass times the acceleration:

$$
F=mx¨.
$$

The dots here stand for rates of change—so $x(t)$ is the trajectory that we're looking for, $x˙(t)$ denotes the velocity function, and $x¨(t)$ is the acceleration.

This equation is called the **equation of motion**. It's a second order differential equation that we would then need to solve to figure out $x(t)$ . But that's a math problem—the physics is about how we write down this differential equation in the first place, and Newton gave us one way to do it. The principle of least action is going to give us another way.

You've hopefully learned about how the force $F(x)$ is related to the potential energy function $U(x)$ ; if not you can check out [this earlier video](https://www.physicswithelliot.com/potential-help-room) I made. The relation is that the force is *minus the slope* of the potential energy:

$$
F(x)=−dUdx.
$$

For example, for gravity acting on a projectile the potential is $U=mgx$ (or $mgy$ , if you prefer to use the name $y$ to label the height of the particle), which is a straight line with slope $mg$ . Then the force is minus that, $F=−mg$ . Or for a mass on a spring, the potential energy is $U=12k(x−l)2$ , whose slope is $k(x−l)$ , from which we get the spring force $F=−k(x−l)$ .

In terms of the potential energy then, we can write the equation of motion as

$$
mx¨=−dUdx.
$$

Now I want to show you the new route to this equation. $U$ is the potential energy of the particle, and of course we can also write down the kinetic energy $K=12mx˙2$ . Their sum $E=K+U$ is the total energy. But actually, right now we want to write down their *difference,* $K−U$ :

$$
L=12mx˙2−U(x).
$$

This combination is called the **Lagrangian** function, and right now it might look like it's coming out of left field, but let's see where it leads us. For any path $x(t)$ between the particle's starting position $x(t1)=x1$ and its ending position $x(t2)=x2$ , define a number $S$ by integrating the Lagrangian along the curve:

$$
S=∫t1t2dt(12mx˙(t)2−U(x(t))).
$$

$S$ is called the **action** of the path. So far $x(t)$ can be any curve connecting the two given endpoints. We want to use the action to figure out the actual trajectory that the particle will follow.

And here's the claim: *the trajectory that the particle follows is the one for which the action $S$ is minimized*. It's therefore called the **principle of least action**. Actually, minimized is too strong a word here—there can be situations where the solution is a saddle instead of a minimum. But let's focus on the typical case here.

So how do we see that this claim is true? Think back to your calculus classes, where you have some function $f(x)$ and you want to find its minima, maxima, or saddle points. These are called extremal or critical points. They're the points where the slope of the function vanishes: $f′(x)=0$ . In other words, say we look at the function at a tiny distance $ε$ away from a minimum. We can Taylor expand it like so:

$$
f(x+ε)=f(x)+f′(x)ε+12f″(x)ε2+⋯
$$

where the $⋯$ stand for higher powers of $ε$ . But if $ε$ is tiny, so that we're near the minimum, then these corrections get tinier and tinier and are unimportant. But if $x$ is a minimum, then $f′(x)=0$ , and so the leading term in the displacement $ε$ vanishes. That means that when you take a little step $ε$ away from an extremum, to leading order the value of the function doesn't change at all! This can in fact be taken as the defining property of an extremal point.

![](https://www.physicswithelliot.com/s/wiggles.png)

The same idea goes for our action $S$ and the critical *path* $x(t)$ . If we successfully find the trajectory $x(t)$ that minimizes the action, then for any nearby path $x(t)+ε(t)$ , the value of $S$ should be unchanged, where $ε(t)$ is a deformation that can add little "wiggles" to the original curve $x(t)$ . So, let's expand our Lagrangian in powers of $ε(t)$ :

$$
L(x+ε)=12m(x˙+ε˙)2−U(x+ε).
$$

In the first term, we get $(x˙+ε˙)2=x˙2+2x˙ε˙+ε˙2$ , but remember we don't care about things with more than one power of $ε$ here, so we'll forget about the $ε˙2$ . And in the second term we'll apply our usual Taylor series, $U(x+ε)=U(x)+U′(x)ε+⋯$ . So we get

$$
L(x+ε)=12m(x˙2+2x˙ε˙)−U(x)−U′(x)ε
$$

to leading order in $ε$ . Remember $x˙(t)$ stands for the derivative of $x(t)$ with respect to $t$ , and I'm using $U′(x)$ to denote the derivative of $U(x)$ with respect to $x$ .

We can rearrange this a bit like so:

$$
L(x+ε)=(12mx˙2−U(x))+(mx˙ε˙−U′(x)ε).
$$

The reason I did that is that now the first term in parentheses is the original Lagrangian $L(x)$ , and then the second term is the first correction when you take a little step $ε$ away. At a minimum of the action, the value is supposed to be unchanged to leading order, and so the contribution from the second piece should vanish:

$$
∫t1t2dt(mx˙(t)ε˙(t)−U′(x(t))ε(t))=0,
$$

for *any* little deformation $ε(t)$ . How can we ensure that this happens? Let's use integration by parts to rewrite the first term as

$$
mx˙(t)ddtε(t)=−mx¨(t)ε+ddt(mx˙(t)ε(t)).
$$

When we take the integral from $t1$ to $t2$ , the second term is just going to give

$$
∫t1t2dt ddt(mx˙(t)ε(t))=mx˙(t2)ε(t2)−mx˙(t1)ε(t1).
$$

Remember that we're considering all the paths here that go from $x(t1)=x1$ to $x(t2)=x2.$ Our deformation $x(t)→x(t)+ε(t)$ is a tiny variation of such a path, but we don't want it to change the boundary conditions. So we're only going to allow $ε$ 's that vanish at the boundaries, $ε(t1)=ε(t2)=0$ . Then the contribution from this second term vanishes!

The leading change in the action is then

$$
∫t1t2dt(−mx¨−U′(x))ε=0,
$$

where I've pulled out the factor of $ε$ that's now common to both terms after we've integrated by parts. Since this is supposed to vanish for any deformation $ε$ , we conclude that *a trajectory $x(t)$ that minimizes the action must satisfy*

$$
−mx¨−U′(x)=0.
$$

But that's just our equation of motion from before!:

$$
mx¨=−dUdx.
$$

So that proves our claim: of all the paths $x(t)$ that the particle could follow to get from point 1 to point 2, the one it actually takes is the path for which the action $S$ is minimized!

The principle of least action is an extremely powerful way of looking at physics, though if this is your first time encountering it I imagine you might think it looks more complicated than $F=ma$ . But actually it's very often the most straightforward way to write down the equations of motion for a system. We computed the leading order change in the action pretty systematically just now, but there's a faster way to get to it once you know the deal: we're essentially taking a derivative of $L=12mx˙2−U(x)$ . Under the variation $x(t)→x(t)+ε(t)$ , the change in $L$ from the first term is $2⋅12mx˙ε˙$ , just like taking a derivative, and from the second term it's $U′(x)ε$ . Then the change in the Lagrangian is $mx˙ε˙−U′(x)ε$ , like we found before. Now we just integrate the $ε˙$ term by parts, pull out the common factor of $ε$ , and then we arrive at the equation of motion $−mx¨−U′(x)=0.$ With a little practice you'll be able to do all that in your head and go straight from the Lagrangian to writing down the equation of motion.

Another awesome feature of the action approach is that we don't have to deal with any of the annoying vectors that show up in Newton's law. We just pick whatever coordinates we want to describe our system, write the Lagrangian $L=K−U$ , and then take its derivative and set it equal to zero. For an explicit example, take a look at the [mini-lesson](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes) I posted showing how to derive the equation of motion for a pendulum using the Lagrangian.

Of course, all this generalizes to systems with multiple particles in multiple dimensions. You can find the general minimization condition once and for all by taking the variation of the action for a general Lagrangian $L(xi,x˙i)$ with coordinates $xi$ for any number of particles. We want to compute the change in $L$ when we vary $xi(t)→xi(t)+εi(t)$ . First we take the derivative of $L$ with respect to $xi$ , and then multiply by the change in $xi$ ; that gives us

$$
∂L∂xiεi.
$$

The $∂$ 's here denote partial derivatives, which just means that we pretend everything in $L$ is a constant except for the variable that we want to take the derivative with respect to. Then we also have to account for the change in $x˙i.$ So we take the derivative of $L$ with respect to $x˙i$ , and then multiply by its change $ε˙i.$ So we add on

$$
∂L∂x˙iε˙i.
$$

Lastly, we want to integrate this by parts again so that we can pull the $εi$ out. That gives us the change in the action:

$$
∑i∫t1t2dt(∂L∂xi−ddt∂L∂x˙i)εi=0.
$$

Requiring that this vanishes implies

$$
ddt∂L∂x˙i=∂L∂xi
$$

for each coordinate. This is called the **Euler-Lagrange** equation. In our example with $L=12mx˙2−U(x)$ , we have

$$
∂L∂x=−U′(x)
$$

and

$$
ddt∂L∂x˙=ddt(mx˙)=mx¨.
$$

Then the Euler-Lagrange equation gives $mx¨=−U′(x)$ , just like we found by explicitly taking the variation of the action and setting it equal to zero. As a matter of fact, most of the time physicists compute the equations of motion like I showed by taking the variation of the action rather than having to remember the form of the Euler-Lagrange equation.

All this might seem a little mysterious or even miraculous if this is your first time learning about the principle of least action. Where is this coming from? The last thing I want to do is briefly describe how the principle of least action arises from the classical limit of a more precise *quantum mechanical* treatment of the motion. Although, if you haven't learned quantum mechanics before I suppose this will be even more mysterious! But hopefully it'll make you curious to go off and keep learning more.

In quantum mechanics, all we can say is that the particle has a certain *probability* of traveling from its initial point $x(t1)=x1$ to its final point $x(t2)=x2.$ The rules of quantum mechanics tell us how to compute the **transition amplitude**, denoted $⟨x2,t2|x1,t1⟩$ , and then the probability is given by the *square* of this. The famous physicist Richard Feynman showed (in his PhD thesis!) that this amplitude is related to the action as follows.

Consider the possible paths from the starting point to the end point. Assign a complex number to each path given by $eiS/ℏ$ , where $S$ is the action of the path and $ℏ$ is Planck's constant, which characterizes the scale of quantum mechanical effects. Then the particle takes *all* the possible paths from point 1 to point 2, and if we add up these weights $eiS/ℏ$ for each path we get the transition amplitude:

$$
⟨x2,t2|x1,t1⟩∝∫Dx eiS/ℏ.
$$

The integral here stands for the sum over all the paths from $(x1,t1)$ to $(x2,t2)$ . It's therefore called the **path integral**. It's more complicated than the ordinary integrals you're familiar with, because we're not just summing over a regular variable, we're summing over *functions* $x(t)$ .

Now, what does this have to do with the principle of least action? These weights $eiS/ℏ$ are *phases*, meaning that they're complex numbers of absolute value one. In other words, they're like arrows pointing on a circle of radius one. When you add up all the phases $eiS/ℏ$ for all the paths the particle can take, these arrows mostly point at random directions all around the circle, and they add up to zero. The *exception* is for the paths near the one that minimizes the action. Because for those paths the action is nearly a constant, as by definition the action doesn't change to leading order around the minimum. Then these contributions near the classical path have approximately the same weight $eiS/ℏ$ , and those arrows add *constructively* instead of cancelling out!

The result is that the path integral is dominated by the trajectory that minimizes the action, which as we've seen yields the classical solution, $⟨x2,t2|x1,t1⟩∼eiSclassical/ℏ$ ! So this is how the principle of least action emerges from quantum mechanics. But of course, now you should ask why the heck this path integral computes this probability like I claimed. But that will have to wait for another day.

---

See also:

- Part 2: [The Special Relativistic Action, Explained](https://www.physicswithelliot.com/special-relativity-action-mini-notes)
- Part 3: [The Action for General Relativity](https://www.physicswithelliot.com/gr-action-mini-notes)
- Part 4: [The Action for String Theory](https://www.physicswithelliot.com/string-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).