---
date: "2025-08-10T22:14:43+08:00"
url: "https://www.physicswithelliot.com/third-law-help-room-notes"
status:
---
![](https://www.youtube.com/watch?v=A_79m5x0ucY)

In 1687, Isaac Newton published his now famous three laws of motion, and in doing so more-or-less founded modern physics:

1. Free particles move with constant velocity
2. $F=ma$
3. Forces between particles come in equal-but-opposite pairs

The first law says that a football flying through empty outer space will travel in a straight line with constant speed. It's actually essentially a definition of what we call an inertial frame. The second law is of course the most famous equation in physics, or maybe the second-most-famous next to $E=mc2$ .

But I want to focus on the third law here, which is also often quoted as "for every action there is an equal-but-opposite reaction." Disguised inside of this somewhat enigmatic statement is one of the deepest facts about the universe: the principle of **conservation of momentum**.

I'm going to explain what Newton's third law means, and how it secretly encodes momentum conservation. In fact, we'll see that the conservation of momentum is itself the deeper principle of the universe, whereas Newton's third law isn't always true!

![[Read It Later/attachments/ee24e99ca00313c191bb4640488c17c0_MD5.png]]

So let's say that we have two particles hanging out in otherwise empty space. What forces are acting on them? Well, again according to Newton, there'll be a gravitational force between them that goes like one over the distance squared that separates them:

$$
F=−Gm1m2r2.
$$

The gravitational force is attractive, so it pulls the left particle toward the right, and conversely the right particle toward the left. But, the *magnitude* of the force is the same in both cases—only the direction is reversed. That's what we mean by "equal-but-opposite."

Likewise, the particles might carry some electric charge, and then there will be an electric force acting on each of them according to Coulomb's law:

$$
F=kq1q2r2.
$$

As a matter of fact, Coulomb's law of static electricity is remarkably similar to Newton's law of gravity, again going like one over the distance squared between the particles. A key difference, though, is that the electric force is only attractive if one charge is positive and the other is negative; if the charges have the same sign then the force is repulsive. But either way the forces again point along the line that runs between the two particles: they point in opposite directions and are of the same strength.

This is the essence of Newton's third law: for any force we find acting on the left particle, Newton asserts that there will be another force acting on the right particle—of the same magnitude but pointing in the opposite direction.

Now what does this have to do with conservation of momentum? Remember that momentum is a mathematical way of quantifying how much "motion" an object has. And it's defined by multiplying the velocity of a particle by its mass, $p=mv$ . That way, we account for the fact that an 18 wheeler traveling down the street at 25 miles per hour should count for a much larger amount of motion than a bicyclist riding down the road at the same speed.

Now notice that if we take the rate of change of the momentum definition, assuming that the mass of our object is fixed, then we learn that the rate of change of momentum equals the mass times the acceleration:

$$
Rate of change(p)=ma,
$$

because $a$ is the rate of change of $v$ . But we recognize the right-hand-side from Newton's second law, $F=ma$ ! Therefore, *the rate of change of a particle's momentum is equal to the total force that's acting on it:*

$$
Force=RoC(p).
$$

This is actually the more general statement of Newton's second law. If you've learned some calculus, then by "rate of change" here I'm just talking about the derivative of $p(t)$ with respect to time.

We can treat the case with multiple particles similarly. We assign momentum $p1=m1v1$ to particle 1 and $p2=m2v2$ to particle 2, and define the total momentum by

$$
ptotal=p1+p2.
$$

Then the force on particle 1 is the rate of change of its momentum, $F1=RoC(p1)$ , and likewise for particle 2. If we add these together, we learn that the total force on the two-particle *system* is equal to the rate of change of the total momentum:

$$
Ftotal=RoC(ptotal).
$$

This is again Newton's second law, but now applied to the two-particle system instead of just one particle.

Now comes the key point: because Newton's third law assures that the force on particle 1 is equal-but-opposite to particle 2, when we add them together to find the total force on the system they cancel out and we get zero!

$$
Ftotal=F1+F2=0.
$$

Then the rate of change of the total momentum vanishes, and so the momentum is conserved! The same goes if we have many particles interacting with one another, as long as the forces between each pair of particles obey Newton's third law.

In this way, Newton's law of "action and reaction" is secretly all about momentum conservation! A system on which the total force vanishes is called *isolated*, and what we've therefore learned is that the momentum of an isolated system is a constant.

For a planet orbiting a star, for example, we have an isolated system as long as there are no other masses nearby. Then the total momentum will be a constant, independent of time, because there's no net force on the system.

Of course, if we're thinking of our own Earth and Sun, then there *are* other masses around—other planets, moons, and so on—and they exert *external* forces on the Earth+Sun system. Then the momentum of the Earth and Sun will no longer be constant. It's only *internal* forces—that is, forces between two components of the system—that cancel in pairs when we add them all up. On the other hand, we can always *enlarge* our definition of our system to include these additional masses, and then the total momentum of the larger system will be conserved.

![[Read It Later/attachments/3a9c0382dc474a7142af15a8f9aa1828_MD5.png]]

We believe that conservation of momentum is a deep property of the universe. Newton's third law, on the other hand, isn't always true! The classic example where it fails is in electromagnetism. Say we have two positively charged particles moving toward each other at a right angle—one could be heading leftward along the $x$ axis and the other downward along the $y$ axis, say. What are the forces on each particle?

Since their charges are the same sign, there will be a repulsive electric force between the two. That force isn't precisely given by Coulomb's law, since that's specific to *stationary* charges, whereas these are moving. As long as their speeds aren't too big though (compared to the speed of light), then Coulomb's law is still a pretty good approximation. Regardless, the electric forces between the particles will still be equal-but-opposite.

Because they're moving, each charge also creates a *magnetic* field that circles around it, and exerts a magnetic force on the other. The particle on the $x$ axis experiences a magnetic force pointing up, while the particle on the $y$ axis experiences a magnetic force to the right. They do not point in opposite directions! Newton's third law is therefore violated.

Does that mean that the physics of electricity and magnetism is inconsistent with the principle of conservation of momentum? In fact it does not! The reason is that *the electric and magnetic fields themselves carry momentum* (and energy), and it is only after accounting for the momentum of both the particles and the fields that we can consistently understand the flow of momentum in an electromagnetic system!

---

See also:

- [The Trick that Makes Physics as Simple as Drawing a Picture](https://www.physicswithelliot.com/potential-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).