---
date: "2025-08-10T22:16:45+08:00"
url: "https://www.physicswithelliot.com/icy-ramp-classic-notes"
status:
---
## What Happens When a Block Slides Down a Sliding Ramp? Classic Physics Problem

![](https://www.youtube.com/watch?v=CHWsI-RcSPQ)

Year after year, in intro physics classrooms all around the world, students learn to analyze the same problem: what happens when you put a block on top of an inclined ramp? It's not a terribly exciting system, but it is a useful setup for learning to predict motion by applying Newton's laws, so it's a worthwhile pedagogical exercise. I reviewed the details of that problem [here](https://www.physicswithelliot.com/block-ramp-help-room-notes).

Usually, we assume that the ramp itself is fixed in place—maybe it's nailed down into the top of a table. But what if the ramp is free to slide? Say if the ramp were a perfectly frictionless chunk of ice sitting on top of a table. That makes for a much more challenging and interesting problem, and that's what I'm going to talk about here.

![](https://www.physicswithelliot.com/s/ramp-block-setup.png)

So, let's say we have a ramp of mass $M$ that's inclined at an angle $θ$ . There is no friction between the ramp and whatever surface it's sitting on. We release a block of mass $m$ from the top of the ramp at $t=0$ . The question is: when will the block hit the ground? Let the length of the ramp be $l$ , and let's also suppose that there's no friction between the block and the ramp either, because things are already going to get complicated enough here.

We're actually going to answer this question in three different ways. First, we'll do it in the most straightforward approach using $F=ma$ . But after that, I'll show you two slicker approaches that get to the same answer with less work.

Let's start with a lightning-fast review of the simpler problem where the ramp is nailed down. Again, you can head [over here](https://www.physicswithelliot.com/block-ramp-help-room-notes) if you want to see a more detailed refresher on that problem. We start with the free-body diagram for the block:

![](https://www.physicswithelliot.com/s/block-fbd.png)

There are only two forces on the block: gravity $mg$ pulling down, and the normal force $N$ from the ramp pointing perpendicular to the surface. Now we add up the forces and write down $∑F→=ma→.$ This is a vector equation, but the block is only moving in one direction—along the length of the ramp. So let's define a coordinate $q$ that measures the position of the block with respect to the top of the ramp:

![](https://www.physicswithelliot.com/s/inclined-ramp.png)

The only force in the $q$ direction is the component of gravity that points parallel to the ramp, which with a bit of geometry you can see is $mgsin⁡θ$ . Then the $F=ma$ equation for $q$ is

$$
mq¨=mgsin⁡θ,
$$

where $q¨=aq$ is the acceleration of $q$ —the two dots stand for the second derivative of $q(t)$ . This is a nice and simple equation: it says that the block just slides down the ramp with constant acceleration,

$$
q¨=gsin⁡θ.
$$

Some checks: when $θ=0,$ the ramp is just a flat table, and so $q¨=0$ as expected. When $θ=π/2$ , we find $q¨=g$ because the block is now in free fall.

Since the block started at rest at $q=0$ at $t=0$ , the trajectory is

$$
q(t)=12gsin⁡(θ)t2.
$$

It hits the bottom when $q(T)=l$ :

$$
T=2lgsin⁡θ.
$$

Alright, that was our warm up. Now we want to figure out what happens when the ramp is also free to slide. By Newton's third law, whatever normal force $N$ that the ramp exerts on the block, the opposite force acts on the ramp itself and will push it to the left. So we expect that the ramp will slide to the left while the block is sliding down to the right.

Here are the free-body diagrams for the ramp and for the block:

![](https://www.physicswithelliot.com/s/ramp-block-fbds.png)

Once again, the block has got gravity $mg$ pulling down, and the normal force $N$ from the ramp pointing perpendicular to the surface. This time I've broken things up into the vertical and horizontal components of the force. The forces on the ramp are gravity $Mg$ , the opposite normal force $N$ , and lastly the normal force $Ngd$ from the ground pushing up on the ramp.

Since both the ramp and the block are moving now, we're going to need some more coordinates. Let's set the origin off to the left somewhere, at the height of the top of the ramp. Let $X$ denote the position of the top corner of the ramp, and let $(x,y)$ be the coordinates of the block:

![](https://www.physicswithelliot.com/s/ramp-block-coordinates.png)

Now let's write down the $∑F→=ma→$ equations. Starting with the block, the only horizontal force is the $x$ component of the normal force, $Nsin⁡θ$ , so we get

$$
Nsin⁡(θ)=mx¨.
$$

The vertical forces on the block are the $y$ component of the normal force $Ncos⁡θ$ pointing up and gravity pointing down:

$$
Ncos⁡(θ)−mg=my¨.
$$

Similarly for the ramp, we've got the horizontal equation

$$
−Nsin⁡(θ)=MX¨,
$$

and the vertical equation

$$
Ngd−Ncos⁡(θ)−Mg=0,
$$

which has to vanish because the ramp is stuck on the surface of the ground. We don't care too much about this last equation. All it tells us is that $Ngd$ will be whatever it needs to be to keep the ramp from falling through the ground.

Note that if we add the two horizontal equations together, the forces cancel out and we're left with

$$
MX¨+mx¨=0.
$$

What's going on here? Think about the block+ramp *system*. Newton's second law for a system says that the total external force equals the total mass times the acceleration of the center-of-mass: $∑F→ext=(M+m)a→CM$ . The only external forces on the system are gravity and $Ngd$ . The normal force $N$ between the ramp and the block is an *internal* force—meaning a force that acts between two pieces of the system—and by Newton's third law it cancels out when we write $F=ma$ for the system: whatever force $N$ is acting on the block, the opposite force $−N$ acts on the ramp.

In this case, there are no external horizontal forces on the block+ramp system, and the horizontal $F=ma$ equation says that the acceleration of the $x$ coordinate of the center-of-mass is zero:

$$
x¨CM=MX¨+mx¨M+m=0.
$$

That's what our total horizontal $F=ma$ equation is saying. It means that however much the block slides to the right, the ramp has to move proportionally to the left in order to keep the $x$ coordinate of the center-of-mass fixed in place.

The upshot is that we have three equations we need to solve:

$$
Nsin⁡(θ)=mx¨Ncos⁡(θ)−mg=my¨X¨=−mMx¨.
$$

If we solve the first equation for $N=mx¨ /sin⁡(θ)$ and plug it into the second equation, we can reduce these to

$$
cos⁡(θ)x¨−sin⁡(θ)y¨=gsin⁡(θ)X¨=−mMx¨.
$$

But we've got a problem because there are three unknowns here ( $x¨$ , $y¨$ , and $X¨$ ), but only two equations. What's missing? The thing we haven't accounted for yet is the fact that the block is stuck on the surface of the ramp, which means that $x$ and $y$ aren't independent.

![](https://www.physicswithelliot.com/s/parallel-ramp-coordinate.png)

We can take care of this by going back to our coordinate $q$ that's measured parallel to the ramp, which is related to $x$ and $y$ by

$$
q=x−Xcos⁡θ=−ysin⁡θ.
$$

Then we can rewrite our system of equations as

$$
cos⁡(θ)(cos⁡(θ)q¨+X¨)+sin2⁡(θ)q¨=gsin⁡(θ)X¨=−mM(cos⁡(θ)q¨+X¨).
$$

Simplifying, we get

$$
q¨+cos⁡(θ)X¨=gsin⁡(θ)(M+m)X¨=−mcos⁡(θ)q¨.
$$

Finally, we solve the second equation for $X¨=−mM+mcos⁡(θ)q¨$ , plug it into the first equation to find

$$
q¨−mM+mcos2⁡(θ)q¨=gsin⁡(θ),
$$

and then solve for $q¨$ :

$$
q¨=gsin⁡(θ)M+mM+msin2⁡(θ).
$$

Is this consistent with our earlier result $q¨=gsin⁡(θ)$ for the problem when the ramp was fixed in place? We can reproduce that special case by letting the mass of the ramp $M$ get really big, so that it effectively sits still. Then the ratio $M+mM+msin2⁡(θ)→MM=1$ , and we indeed find $q¨→gsin⁡(θ)$ once again. Other checks: when $θ=0$ so that the ramp is flat, we find $q¨=0$ , as expected because the block is just sitting on the "ramp," which is just sitting on the ground. And when $θ=π/2$ , we once again find $q¨=g$ because the block is now in free fall.

To actually answer the original question—when does the block hit the ground?—we write the trajectory

$$
q(t)=12q¨t2,
$$

which again is very simple because the acceleration is a constant, and then we find out when $q(T)=l$ :

$$
T=2lgsin⁡(θ)M+msin2⁡(θ)M+m.
$$

So there we have it!

Now, there's nothing wrong with that solution. It was totally systematic: we drew the free-body diagrams, wrote the $F=ma$ equations, applied the constraints, and then solved. But it's more work than we strictly needed to do to solve this problem. The basic point is that working with the $F=ma$ equations forced us to worry about the normal force $N$ between the ramp and the block. But we don't really care about $N$ —to answer the question we just wanted to find out the acceleration $q¨$ of the block. Is there another way to solve this problem that avoids needing to introduce the normal force in the first place?

In fact, I'll show you two other approaches right now! The first option is to make use of conservation of energy. The total energy of the ramp + block is

$$
E=12MX˙2+12m(x˙2+y˙2)+mgy.
$$

The first two terms are the kinetic energies of the ramp and the block, and the last term is the gravitational potential energy of the block. Replacing $x=cos⁡(θ)q+X$ and $y=−sin⁡(θ)q$ to write things in terms of $q$ , we get

$$
E=12MX˙2+12m((cos⁡(θ)q˙+X˙)2+sin2⁡(θ)q˙2)−mgsin⁡(θ)q.
$$

The form of the kinetic energy here comes from the fact that the velocity of the block written in terms of $q$ is the vector $(q˙cos⁡(θ)+X˙,−q˙sin⁡(θ))$ , where we need to add on the velocity $X˙$ of the ramp to the horizontal component to get the total velocity of the block. Simplifying a bit,

$$
E=12(M+m)X˙2+12mq˙2+mcos⁡(θ)X˙q˙−mgsin⁡(θ)q.
$$

The fact that there are no external horizontal forces means that the total horizontal momentum is zero:

$$
MX˙+mx˙=0,
$$

or again replacing $x˙=cos⁡(θ)q˙+X˙$ ,

$$
MX˙+m(cos⁡(θ)q˙+X˙)=0.
$$

If we solve this equation for $X˙$ ,

$$
X˙=−mM+mcos⁡(θ)q˙,
$$

and plug it into the energy, we can write the energy entirely in terms of $q$ :

$$
E=12m2M+mcos2⁡(θ)q˙2+12mq˙2−m2M+mcos2⁡(θ)q˙2−mgsin⁡(θ)q.
$$

Simplifying a little more, we get

$$
E=12m(M+msin2⁡(θ)M+m)q˙2−mgsin⁡(θ)q.
$$

Now we use the fact that the energy is constant: the time derivative of this equation is equal to zero:

$$
m(M+msin2⁡(θ)M+m)q˙q¨−mgsin⁡(θ)q˙=0.
$$

Cross out the $q˙$ 's, and solve for $q¨$ ! We get

$$
q¨=gsin⁡(θ)M+mM+msin2⁡(θ)
$$

just as before! This way of doing things, we never had to talk about the normal force at all.

Finally, let me mention how we could have solved this problem using the Lagrangian, which is probably the fastest way of all. If you haven't learned about Lagrangians yet, you should watch the mini-lesson I posted about them [here](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini), or read the notes [here](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes).

The Lagrangian $L$ is the *difference* between the kinetic and potential energies:

$$
L=12(M+m)X˙2+12mq˙2+mcos⁡(θ)X˙q˙+mgsin⁡(θ)q,
$$

where I've again written things in terms of $q$ . The only difference in this formula compared to the total energy above is the sign of the last term, which came from the potential energy. Now we write the *Euler-Lagrange equations* for the two coordinates $X$ and $q$ —again, watch the earlier video if you've never seen these before:

$$
ddt∂L∂X˙=∂L∂Xddt∂L∂q˙=∂L∂q.
$$

For the $X$ equation we get

$$
ddt((M+m)X˙+mcos⁡(θ)q˙)=0,
$$

which implies

$$
X¨=−mM+mcos⁡(θ)q¨.
$$

The $q$ equation is meanwhile

$$
ddt(mq˙+mcos⁡(θ)X˙)=mgsin⁡θ,
$$

which we can simplify to

$$
q¨+cos⁡(θ)X¨=gsin⁡(θ).
$$

Now plugging the first equation for $X¨$ into the second equation, we obtain

$$
q¨−mM+mcos2⁡(θ)q¨=gsin⁡(θ).
$$

Solving for $q¨$ , we learn one more time that

$$
q¨=gsin⁡(θ)M+mM+msin2⁡(θ).
$$

That was quite a bit quicker! You can see why the pros tend to prefer using Lagrangians over $F=ma$ to solve mechanics problems.

---

See also:

- [Blocks Sliding Down Ramps, and All That: Physics Help Room](https://www.physicswithelliot.com/block-ramp-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).