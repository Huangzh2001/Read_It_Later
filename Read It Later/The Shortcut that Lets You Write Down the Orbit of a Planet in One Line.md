---
date: "2025-08-10T22:10:31+08:00"
url: "https://www.physicswithelliot.com/runge-lenz-mini-notes"
status:
---
## The Shortcut that Lets You Write Down the Orbit of a Planet in One Line: Physics Mini Lesson

![](https://www.youtube.com/watch?v=KOek-B3Rvmg)

In my [last video](https://www.physicswithelliot.com/orbits-mini-notes), I showed you how you can derive the orbit of a planet around a star by solving the differential equations that came from the conservation of energy and conservation of angular momentum. It wasn't *too* complicated, but it certainly took a fair bit of work to solve those equations and figure out the orbit. Now I'm going to show you a shortcut that makes it possible to write down the orbit equation in one line. The trick comes from a special symmetry of Newton's gravitational force law, which leads to an additional conserved quantity called the Runge-Lenz vector.

![](https://www.physicswithelliot.com/s/earth-sun.png)

The setup just like last time is that we have a star of mass $M$ fixed at the origin, and a planet of mass $m$ a distance $r$ away. We set up our coordinates so that the planet is in the $xy$ plane. Then last time we saw that the energy and the angular momentum of the planet are both constant. The energy was

$$
E=12m(drdt)2+12mr2(dθdt)2−kr,
$$

where we defined $k=GMm$ for short. $drdt$ is the radial velocity of the planet, and $rdθdt$ is the angular velocity. The angular momentum is meanwhile

$$
L→=mr→×v→=mr2dθdtz^.
$$

We saw that it's a constant vector, of magnitude $mr2dθdt$ and pointing in the $z$ direction. That's what the $z^$ symbol means here—it's a unit vector pointing along the $z$ axis.

Last time, we combined these two equations for $E$ and $L$ to get rid of all the $dt$ 's. That gave us an equation for $drdθ$ , which we were then able to solve for $r(θ)$ :

$$
r(θ)=L2km11+ϵcos⁡θ.
$$

This is the equation of a conic section of eccentricity $ϵ$ , where

$$
ϵ=1+2EL2mk2.
$$

ε = 0.70

Now I want to show you the shortcut to deriving $r(θ)$ . The gravitational potential energy function is very special. In addition to the energy $E$ and angular momentum vector $L→$ , there's *another* conserved vector. It's called the **Runge-Lenz** vector, and here's the definition:

$$
ϵ→=1kv→×L→−r^.
$$

I'm calling it $ϵ→$ because, as we'll see shortly, the magnitude of $ϵ→$ is none other than the eccentricity $ϵ$ from earlier. $r^$ here is the unit vector in the *radial* direction; it's the vector of length 1 that's pointing from the origin in the direction of the planet. We can alternatively write it in terms of the position vector $r→$ as

$$
r^=r→r.
$$

Likewise $θ^$ would be the unit vector pointing counterclockwise along the direction of increasing $θ$ .

So what is this vector $ϵ→$ ? Let's evaluate it at the moment when the planet is at its point of closest approach to the star. We can always arrange our coordinates so that the planet is on the $x$ axis when that happens. Then at that instant $r^=x^$ is just the unit vector pointing along the $x$ direction. Meanwhile the velocity of the planet is all along the angular direction, which coincides with the $y$ axis at this moment, so $v→=rdθdty^$ . $L→$ , of course, is always pointing in the $z^$ direction.

Remember that $×$ denotes the cross product, which we talked about a bit in the [last video](https://www.physicswithelliot.com/orbits-mini-notes). It gives a vector that points perpendicular to both $v→$ and $L→$ . Since $v→$ is pointing in the $y$ direction at this moment and $L→$ points in the $z$ direction, their cross product points along the $x$ axis. Then since $r^$ is also pointing along the $x$ axis, we learn that, at least at the moment when the planet is closest to the star, $ϵ→$ is a vector that points along the $x$ axis:

$$
ϵ→∝x^.
$$

The claim is that $ϵ→$ is in fact a *constant* —it's always given by the same arrow pointing along the $x$ axis. I'll prove that to you in just a minute, but first I want to jump to the punchline and show you how that fact lets us very quickly write down the orbit equation. Take the dot product of $ϵ→$ with $r^$ :

$$
ϵ→⋅r^=1kr^⋅(v→×L→)−1.
$$

We can simplify this with the help of a vector identity:

$$
A→⋅(B→×C→)=C→⋅(A→×B→).
$$

This allows us to write

$$
r^⋅(v→×L→)=L→⋅(r^×v→).
$$

But $r^×v→=1mr(mr→×v→)=1mrL→$ , and so $r^⋅(v→×L→)=L2mr$ . So we learn that

$$
ϵ→⋅r^=L2kmr−1.
$$

If it's true that $ϵ→=ϵx^$ is indeed a constant pointing along the $x$ axis, then $ϵ→⋅r^=ϵcos⁡(θ),$ and so we find

$$
ϵcos⁡(θ)=L2kmr−1.
$$

Now solve for $r$ :

$$
r=L2km11+ϵcos⁡(θ).
$$

Just as before, with no nasty differential equations to solve!

There are two things left to check. One, that it's actually true that $ϵ→$ is a constant, and two, that its magnitude coincides with our previous expression for the eccentricity.

First let's get the magnitude. By squaring $ϵ→$ we get

$$
ϵ→⋅ϵ→=1k2(v→×L→)⋅(v→×L→)−2kr^⋅(v→×L→)+1.
$$

We already learned that $r^⋅(v→×L→)=L2mr$ . As for the first term, we need another vector identity:

$$
(A→×B→)⋅(A→×B→)=A2B2−(A→⋅B→)2.
$$

Then we get $(v→×L→)⋅(v→×L→)=v2L2,$ because $v→⋅L→=0$ . Thus,

$$
ϵ2=v2L2k2−2L2kmr+1.
$$

We can write this more conveniently as

$$
ϵ2=2L2k2m(12mv2−kr)+1.
$$

The quantity in parentheses is the energy $E$ , and so we find

$$
ϵ=1+2EL2k2m,
$$

just as before!

Lastly, we need to prove that $ϵ→$ is a constant. Taking its time derivative, we get

$$
dϵ→dt=1ka→×L→−dr^dt,
$$

remembering that $L→$ is itself a constant.

The second term here is just the angular velocity of the planet,

$$
dr^dt=dθdtθ^,
$$

where again $θ^$ stands for the unit vector pointing counterclockwise along the direction of increasing $θ$ .

![](https://www.physicswithelliot.com/s/rhat-derivative.png)

To see why, suppose the unit vector $r^(t)$ moves to $r^(t+dt)$ after a time $dt$ has passed. Both vectors lie on the unit circle, so the displacement between them is just given by $dr^=dθθ^$ . Now divide both sides by $dt$ .

As for the $a→×L→$ term, note from Newton's law that

$$
ma→=−kr2r^,
$$

and therefore

$$
1ka→×L→=−r^mr2×mr2dθdtz^=−dθdtr^×z^.
$$

Then we find that

$$
dϵ→dt=−(r^×z^+θ^)dθdt.
$$

The last thing is to figure out what to do with this cross product $r^×z^$ . It points perpendicular to both $r^$ and $z^$ , which means it goes along the $θ$ direction. But does it point along $+θ^$ or $−θ^$ ? The answer is part of the definition of the cross product, called the "right-hand-rule": point your fingers along the first vector ( $r^$ in this case), curl them towards the second vector ( $z^$ ), and then your thumb points along the direction of the cross product. So that means $r^×z^=−θ^$ , and we find

$$
dϵ→dt=0.
$$

So the Runge-Lenz vector is indeed a constant!

So there we have it! Once one establishes the fact that the Runge-Lenz vector is a constant, the equation for the orbit follows in just one line of math by taking the dot product with the position vector. One never has to solve a differential equation to figure out the orbit!

Now, is this the most efficient way to compute the orbit of a planet? Well, it depends what you mean exactly. The most likely reason you would think to write down the Runge-Lenz vector in the first place is by first solving the differential equation for the orbit like we did last time, and then noticing that it can be rearranged into a conservation law for a new vector. You'd have to be a *very* sharp cookie to conjure up the Runge-Lenz vector from thin air. But once we've got it hand, it makes quick work of solving for the orbit equation.

---

See also:

- [Deriving the Orbit of Our Home Planet: Physics Mini Lesson](https://www.physicswithelliot.com/orbits-mini-notes)
- [The Trick That Makes Understanding Physics as Simple as Drawing a Picture: Physics Help Room](https://www.physicswithelliot.com/potential-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).