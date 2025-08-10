---
date: "2025-08-10T22:15:52+08:00"
url: "https://www.physicswithelliot.com/block-ramp-help-room-notes"
status:
---
## Blocks Sliding Down Ramps, and All That: Physics Help Room

![](https://www.youtube.com/watch?v=zHSOKywdvjw)

I know—it's not the most exciting system in the world. So why does seemingly every physics teacher in every intro physics class make their students study a block sliding down a ramp? The fact is that it's a great problem for learning to apply Newton's laws in a setup that's not too complicated, but also not totally trivial.

![](https://www.physicswithelliot.com/s/block-ramp.png)

The setup is that we've got a block of mass $m$ , which we've set down on a ramp that's inclined at an angle $θ$ . Say we release the block from rest at the top of the ramp at $t=0$ , and it starts to slide down the ramp. If the length of the ramp is $l$ , then when will the block hit the ground?

In Newtonian mechanics, we follow a three step procedure to answer these kinds of questions:

1. Draw the free-body diagram that shows all of the forces acting on the mass.
2. Add up the forces and write $∑F→=ma→$ .
3. Solve this equation for the position as a function of time.

So here's the free-body diagram:

![](https://www.physicswithelliot.com/s/block-fbd-help-room.png)

There are three forces acting on the block:

1. Gravity $mg$ pulling straight down
2. The normal force $N$ from the ramp pushing on the block. It points perpendicular to the surface of the ramp.
3. Friction $Ff$ pointing back up the ramp.

Okay great, we're already done with step one. Step two is to add up the forces and write $∑F→=ma→$ . This is a vector equation, which means that it's secretly two equations packaged into one. In other words, $F→$ and $a→$ have $x$ components and $y$ components, and each one has its own equation: $∑Fx=max$ , $∑Fy=may$ .

Actually, we can break up the vectors into whatever components that we like. And in this case, since the block is moving along the surface of the ramp, instead of using horizontal and vertical coordinates it makes more sense to use coordinates that run parallel and perpendicular to the the ramp. So let's define a coordinate $q$ that measures the position of the block along the ramp, measured from the top:

![](https://www.physicswithelliot.com/s/inclined-ramp.png)

We want to find $q(t)$ , because if we know that we can figure out when the block will hit the ground just by setting $q(t)=l$ and solving for $t$ .

So what are the forces in the $q$ direction? Well, we've got friction pointing back up the ramp. As for the normal force, it's pointing perpendicular to the ramp, so it doesn't contribute anything at all in the parallel direction. But what about gravity, which is pulling straight down?

Just like we can break a vector up into $x$ and $y$ components, we can break the gravity vector up into parallel and perpendicular components with respect to the ramp:

![](https://www.physicswithelliot.com/s/parallel-perp-components.png)

Note first of all that the angle with the ramp on the right side of the gravity vector is $π2−θ$ , because we have a right triangle with $θ$ in the bottom right corner and therefore $π2−θ$ is in the top corner. Now draw the component of the gravity arrow that points perpendicular to the ramp. Since this arrow makes a 90 degree angle with the ramp, it has to make an angle $θ$ with the original gravity arrow, since $θ+(π2−θ)=π2$ .

Now we can draw another little right triangle, with gravity $mg$ along the hypotenuse pointing straight down, the perpendicular component making an angle $θ$ with the vertical, and the parallel component on the opposite leg. The perpendicular component is therefore $mgcos⁡θ$ , and the parallel component is $mgsin⁡θ$ .

It's easy to get the parallel and perpendicular components of gravity $mgsin⁡(θ)$ and $mgcos⁡(θ)$ mixed up here. A trick for getting them straight is to think about what happens when $θ=0$ . In that case, the "ramp" is just a flat table. Gravity is already pointing entirely perpendicular to the table, and the parallel component is zero. So for general $θ$ the parallel component must be $mgsin⁡(θ)$ , because that's what correctly vanishes for $mgsin⁡(θ=0)=0.$

So, the forces pointing parallel to the ramp are the parallel component of gravity $mgsin⁡θ$ pointing down the ramp and the friction force $Ff$ pointing up the ramp. Then the $F=ma$ equation for $q$ is

$$
ma=mgsin⁡(θ)−Ff,
$$

where $a$ is the acceleration of $q$ .

In the perpendicular direction, meanwhile, we have the normal force $N$ and the perpendicular component of gravity $mgcos⁡(θ)$ :

$$
N−mgcos⁡(θ)=0.
$$

This we set equal to zero because the block is not accelerating *off* the surface of the ramp—it's sliding along it. So the perpendicular equation just tells us what the normal force has to be to keep the block from falling through the ramp:

$$
N=mgcos⁡(θ).
$$

It's the parallel equation that's more interesting here. To unpack that equation, we need to know what the friction force $Ff$ is. Anytime you're dealing with friction forces, the first thing you should ask yourself is whether you're talking about a *static* friction force or a *kinetic* friction force. Friction is static when two objects are pushed up against each other but not sliding—if the block were just sitting at rest on the ramp then we'd have a static friction force. Kinetic friction comes in when two objects are sliding against each other.

Since we're assuming here that the block starts to slide as soon as you set it down, we're dealing with kinetic friction. Now, the actual microscopic details of the kinetic friction force are going to be *very* complicated; it's due to all the little atoms in the ramp bumping up against the atoms in the block. But when we zoom out and look at the macroscopic picture, we don't have to worry about all that. Experimentally, we find that for common materials, the kinetic friction force is proportional to the normal force between the two objects:

$$
|Ff|=μK|N|.
$$

$μK$ is called the **coefficient of kinetic friction**. It's something you measure experimentally, and it characterizes the strength of the kinetic friction force between two materials. The fact that $Ff$ is proportional to the normal force means that the harder two surfaces are pressed against each other, the more friction there is, which makes sense.

Since we've already determined the normal force $N=mgcos⁡(θ)$ between the block and the ramp, we therefore find that the friction force is $μKmgcos⁡(θ)$ pointing back up the ramp. Then the $F=ma$ equation for $q$ becomes

$$
ma=mgsin⁡(θ)−μKmgcos⁡(θ).
$$

Simplifying a little bit, we find that the acceleration of the block down the ramp is

$$
a=g(sin⁡(θ)−μKcos⁡(θ)).
$$

Let's do some checks. First of all, the units look good, because $g$ has units of acceleration, while $θ$ and $μK$ are unitless. When $θ=π2$ , the ramp is a vertical wall, and the block will just be in free fall. And indeed, since $sin⁡(π2)=1$ and $cos⁡(π2)=0$ , we find $a=g$ —the same as for any falling object. If we start to dial down the angle, the acceleration of the block is reduced compared to a projectile, first to $gsin⁡(θ)$ due to the geometry of the ramp, and furthermore by $gμKcos⁡(θ)$ due to the friction with the ramp.

(When $θ=0$ , the ramp is flat, and so the block should just be sitting at rest on top of it. Why does our formula seem to say $a=−gμK$ then? Remember we assumed that the block was moving, so that it's subject to a *kinetic* friction force. If you kick a block along a flat table, it will decelerate at $a=−gμK$ until it comes to a stop, and then the friction force will vanish and the block will remain at rest.)

Note that the acceleration $a=g(sin⁡(θ)−μKcos⁡(θ))$ is *constant*, just like for a projectile, but smaller. Then just like you learned that the trajectory of a ball thrown up in the air is

$$
y(t)=12at2+vy0t+y0,
$$

where $a=−g$ is the acceleration, $vy0$ is the initial velocity, and $y0$ is the initial position, then likewise the trajectory of our sliding block is

$$
q(t)=12g(sin⁡(θ)−μKcos⁡(θ))t2,
$$

where, since the block was released from rest from the top of the ramp at $t=0$ , the initial position and velocity are both zero.

Now that we have the trajectory, we can answer whatever questions we want about the motion of the block! In particular, to find the time $T$ that it takes to hit the ground, we just need to set $q(T)$ equal to the length $l$ of the ramp, and then solve for $T$ :

$$
12g(sin⁡(θ)−μKcos⁡(θ))T2=l⟹T=2lg1sin⁡(θ)−μKcos⁡(θ).
$$

Done! Now if you want to make sure you really understand all this, open up the [problem sheet](https://www.physicswithelliot.com/s/block-ramp-problem-sheet.pdf) and give those questions a try.

And if you really want to stretch yourself and try a much tougher version of this problem, consider the case where the ramp itself has mass $M$ and is free to slide across the ground. I've posted another video about that problem [here](https://www.physicswithelliot.com/icy-ramp-classic-notes).

---

See also:

- [What Happens When a Block Slides Down a Sliding Ramp? Classic Physics Problem](https://www.physicswithelliot.com/icy-ramp-classic-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).