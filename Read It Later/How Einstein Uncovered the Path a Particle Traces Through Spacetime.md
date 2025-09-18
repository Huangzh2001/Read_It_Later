---
date: "2025-08-10T22:09:17+08:00"
url: "https://www.physicswithelliot.com/gr-action-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=h2SEK6Jjv3Y)

In this physics mini lesson, we're going to continue our discussion of the principle of least action, following up on the lessons about the action in [Newtonian mechanics](https://www.physicswithelliot.com/least-action-mini-notes) and in [special relativity](https://www.physicswithelliot.com/special-relativity-action-mini-notes). This time, we'll talk about the action for a particle in *general* relativity, Einstein's theory of gravity. We'll write down the action for a particle traveling through spacetime, and see how the particle is forced to traverse a very special kind of curve called a geodesic.

![[Read It Later/attachments/2361b1c4d60690678a8d0a17c6ad94d1_MD5.png]]

The basic idea of Einstein's theory is that a massive object like a star warps the geometry of spacetime around it. Then according to Einstein, something like a planet traveling along nearby doesn't really experience a gravitational force at all, it just keeps moving along the straightest and shortest path that it can through this curved geometry. And that's what a geodesic is: the straightest and shortest possible path through a curved space.

In special relativity, we learned about how as particle travels around, it traces out a path through spacetime called the worldline of the particle. And then we set the action to be proportional to the length of the worldline, $S=−mc∫−ds2$ . Then by minimizing the action, we saw that a free particle travels along the shortest and straightest path that it can through spacetime: which of course is just a straight line. More precisely, the particle follows the path that maximizes its proper time, which is the time that's ticked off on a watch strapped to the particle.

$ds2=−c2dt2+dx2$ here was the Minkowski metric—it's what tells us how to measure distances in spacetime. It's that minus sign in front of the time term that makes the geometry of spacetime so bizarre compared to ordinary space like we're used to.

This Minkowski metric tells us about the geometry of *flat* spacetime. So if we had a particle soaring through empty outer space, far away from any stars or other objects, it would travel along a straight line through this flat spacetime. But a few years after publishing his special theory of relativity, Einstein came back for the one-two punch and generalized his geometric framework for the universe by explaining the geometric origins of gravity. It's called general relativity, and it's probably the most beautiful physical theory that humans have ever written down.

Gravity is different than the other forces that we encounter. From Newton's law $F=ma$ , we expect that the acceleration of a particle will in general depend on its mass $m$ . But as you likely learned in the first week or two of your first physics class, a falling bowling ball drops at the same rate as a falling penny, despite the order of magnitude difference in their masses.

Gravity is therefore *universal*; it affects all particles in the same way regardless of their mass. Einstein reasoned that we therefore shouldn't think of gravity as a force at all, but as a feature of the background spacetime on which particles move, and which subsequently affects all particles in the same way.

A particle in a gravitational field isn't being accelerated at all, it's just traveling along on its merry way—it's the spacetime *around* the particle that has changed.

This is what lead Einstein to the idea that gravity could be attributed to the *shape* of spacetime. Like I mentioned at the top, the gist is that the presence of a massive object like a star warps the spacetime around it, deforming it from the flat, Minkowski spacetime of special relativity into a curved spacetime. Then a particle (or planet) passing nearby still does its best to keep traveling along the straightest and shortest line that it can, but now it's tracing out a path in the curved geometry. These paths are the geodesics.

In particular, the action for a particle in general relativity is still going to be given by the same formula we wrote down before: the length of the worldline. Only now we need to replace the flat space Minkowski metric $ds2$ of special relativity with the curved metric, and then applying the principal of least action produces the geodesic equation.

I'm going to tell you about how all this works in a little more detail. This is a pretty advanced subject though—physics students usually take their first general relativity class at the end of college or the beginning of grad school. But the ideas are so beautiful that I think it's definitely worth exploring a bit even if you're more of a beginner. So if you *are* a beginner, don't sweat the details of the equations too much—and *definitely* don't be scared away by them. If you keep studying physics then they'll make sense in time. For now I hope you'll at least come away with an appreciation for a few of the big ideas of general relativity, and the transformative way that Einstein reshaped the way we look at the universe.

Since general relativity is, like the name implies, a generalization of special relativity, let's start by reviewing what we learned about the action for a particle in special relativity last time. And we'll also introduce some new notation that will make the generalization from special relativity to general relativity more straightforward.

When we went to compute the length of the worldline of a particle in special relativity, we were confronted with the fact that the Minkowski metric $ds2$ is negative along the worldine of a massive particle. So instead of using $ds=ds2$ to measure the length of the worldline, we flipped the sign first, $−ds2$ . Then the length of the worldline is

$$
∫−ds2=∫c2dt2−dx2=c∫dt1−x˙2/c2,
$$

where $x˙=dx/dt$ . The integral on the right—i.e. the length of the worldline divided by $c$ —is called the proper time $τ$ of the particle. It's the time that's ticked off on the particle's watch as it moves through spacetime.

The length of the worldline is maximized along a straight line through spacetime—that it's a maximum instead of a minimum is one of those peculiar features of the Minkowski metric. That's why in the twin paradox, the twin who stays home on Earth winds up older than the twin who flies around outer space in a rocket ship before coming home. The worldline for the twin sitting at home is a straight line, and so the most time has elapsed on their watch. The twin in the rocket ship followed a curvy worldline through spacetime. So even though they begin and end at the same event, less proper time has elapsed on the rocket ship twin's watch, and when they get home they're younger.

That lead us to identify the action for a particle in special relativity with the length of the worldline, up to some factors:

$$
S=−mc∫−ds2.
$$

The $mc$ has to be there to get the units right. And the minus sign is there because we want the action to be *minimized*, whereas the proper time along a straight line is *maximized*.

Now we want to extend this to general relativity. In fact, we don't have to change our action formula at all. The particle is still going to follow the straightest and "shortest" path through spacetime that it can—where again "shortest" really means the maximum proper time. The difference is that the Minkowski metric that describes flat spacetime gets replaced with the curved metric of a spacetime that's been warped by the presence of something like a star.

To describe a curved metric, it's convenient to introduce some new notation. Let's write the spacetime coordinates of the particle as $xμ$ ( $μ$ is the greek letter "mu"). So $x1$ will stand for the $x$ component, $x2$ will stand for the $y$ component, and $x3$ will stand for the $z$ component. (We've mostly been ignoring the $y$ and $z$ components so far to keep things simple.) As for the time component, we'll write that as $x0=ct$ . So our spacetime coordinates are

$$
xμ=(x0x1x2x3)=(ctxyz),μ=0,1,2,3.
$$

Note that those superscripts are labels, not exponents. Likewise, we can write the displacement vector as

$$
dxμ=(cdtdxdydz).
$$

Next let's define a $4×4$ matrix with components $ημν$ ( $η$ is the Greek letter "eta" and $ν$ is the Greek letter "nu") by:

$$
ημν=(−1000010000100001),μ,ν=0,1,2,3.
$$

So in other words $η00=−1$ , and $η11=η22=η33=1$ , and all the other components of the matrix are zero. Note again that we're counting the components from 0 here instead of from 1; it's just a convention to call the time direction the 0th component.

Now we can write the Minkowski metric in a nice and compact form

$$
ds2=∑μ,ν=03ημνdxμdxν=η00(dx0)2+η11(dx1)2+η22(dx2)2+η33(dx3)2=−(cdt)2+(dx)2+(dy)2+(dz)2.
$$

All this notation might seem like overkill, since the Minkowski metric isn't all that complicated to begin with. But it's going to be very convenient for the generalization to curved spacetime in a minute.

With our new notation, we can write the length of the worldline like this:

$$
∫−ds2=∫−ημνdxμdxν.
$$

Notice that I didn't write the summation symbol $∑μ,ν=03$ here—sums like this appear so often in relativity that it's very convenient to just declare the convention that any time two indices show up in the same term, we sum over them. So $AμBμ$ is shorthand for $∑μ=03AμBμ$ , and likewise $ημνdxμdxν$ stands for $∑μ,ν=03ημνdxμdxν.$

Now remember, we're evaluating this integral along the worldline that the particle traces out through spacetime. We can specify the worldline by giving its coordinates $xμ(λ)$ as a function of some parameter $λ$ . The particular parameter you pick doesn't matter—you can use any $λ$ that you like. For example, you might pick $λ=t$ to coincide with the time in the coordinate system that you've set up. Or you might set $λ=τ$ equal to the proper time on the particle's watch.

Let's multiply and divide the integrand by $dλ$ to get a more standard looking integral:

$$
∫−ds2=∫dλ−ημνdxμdλdxνdλ.
$$

For example, if we pick $λ=t$ here, then we get

$$
∫dt−ημνdxμdtdxνdt=∫dt−η00(d(ct)dt)2−η11(dxdt)2=∫dtc2−(dxdt)2=c∫dt1−x˙2/c2,
$$

just like before. (I'm again dropping the $y$ and $z$ directions for simplicity here, but in general they contribute as well.)

This notation makes it really straightforward to go from the flat spacetime of special relativity to the curved spacetime of general relativity. We just replace the constant matrix $ημν$ with a general matrix $gμν(x)$ that's a function of the coordinates:

$$
ds2=gμν(x)dxμdxν.
$$

In general, this is going to be the metric of a *curved* space. Roughly, the reason is that the coefficients $gμν(x)$ depend on your position $xμ$ in spacetime. And so the distance between neighboring points $xμ$ and $xμ+dxμ$ varies depending on where you are in the space.

So what lead Einstein to think that gravity is related to the curvature of spacetime? Like I briefly mentioned in the introduction, the remarkable feature of gravity is that it's universal: it affects all particles in the same way, regardless of their mass. Galileo demonstrated this long ago for projectiles on Earth, supposedly by dropping balls of different masses from the top of the leaning tower of Pisa. They were all accelerated downward at the same rate and hit the ground at the same time, regardless of their mass.

So on Earth, we observe that the weight of an object is $F=−mg$ , where $g≈9.8 m/s2$ is a constant. And so $F=ma$ for a falling object implies that the acceleration $a=−g$ is always the same constant, independent of its mass. Likewise, if we write Newton's inverse square law of gravity, e.g. between a star $M$ and a planet $m$ , then $F=ma$ for the planet reads

$$
−GMmr2r^=ma→,
$$

and once again the mass $m$ cancels out. (The big $M$ of the star's mass doesn't cancel—that's what sets the strength of gravity around an object of mass $M$ . We're talking here about the acceleration of another object $m$ due to the presence of $M$ .)

The fact that gravity acts on all particles in the same way made Einstein suspect that it shouldn't really be attributed to a force at all in the sense of $F=ma$ . Instead gravity is a feature of the *background* on which all particles are traveling along—i.e. spacetime—and it's the *shape* of spacetime that produces the effects we observe as gravity. Any particle, regardless of its mass, just does its best to travel along a straight line through spacetime, but the presence of a big mass like a star warps the geometry and deforms the particle's trajectory away from what it would have been in empty outer space.

The conceptual framework here is very similar to electromagnetism, which you may be more familiar with. Electric charges and currents create electric and magnetic fields according to Maxwell's equations, which then influence the motion of charged particles according to the Lorentz force law, $F→=q(E→+v→×B→)$ . In general relativity, massive objects warp spacetime, and then the shape of the spacetime tells massive particles how to move.

The way that massive objects warp the shape of spacetime is described mathematically by what are called "Einstein's field equations." They're the analog of Maxwell's equations for electromagnetism. I'm not going to get into the details of those equations right now, but the point is that if somebody hands us some distribution of mass like a big star, then we can try to solve Einstein's equations to figure out the curved metric $gμν$ that results. After that, we write down the action for a particle traveling through this curved spacetime and minimize it to determine the trajectory that it will follow.

The action is just like we wrote down before, only this time we need to compute the length of the worldline using the curved metric:

$$
S=−mc∫dλ−gμνdxμdλdxνdλ.
$$

Again, the conceptual idea is more important than the detailed equation here: up to some factors, the action is just equal to the length of the particle's worldline through spacetime, which has been warped by the presence of e.g. a star. Then to minimize the action, the particle will take the shortest path that it can through spacetime—or more precisely it takes the path of maximum proper time.

Like we learned in the previous lessons, to apply the principle of least action we take a little variation of the trajectory $xμ(λ)→xμ(λ)+εμ(λ)$ and then insist that the action shouldn't change at leading order in $ε$ . That condition will give us the equation of motion. It takes a little effort so bear with me! Let

$$
l=−gμνdxμdλdxνdλ
$$

stand for the integrand of the action. Then when we make the little variation of $xμ(λ)$ , the change in $l$ is

$$
dl=−12l(2gμνdxμdλdενdλ+∂gμν∂xρερdxμdλdxνdλ).
$$

The first term comes from the change in the $dx/dλ$ factors—that's what we would have had even in flat space. The second term is new in curved space: when the metric $gμν(x)$ depends on $x$ , then it also changes when you make a variation of $x$ .

Now we integrate to get the change in the action, and we integrate by parts on the first term to pull out the common factor of $ε$ :

$$
dS=12mc∫dλ ερ(−ddλ(2lgμρdxμdλ)+1l∂gμν∂xρdxμdλdxνdλ).
$$

Since this is supposed to vanish for any variation $ε(λ)$ , the quantity it multiplies has to vanish—that's the equation of motion. Expanding out the derivative and doing a little simplifying, we get

$$
gμρd2xμdλ2+(∂gμρ∂xν−12∂gμν∂xρ)dxμdλdxνdλ=1ldldλgμρdxμdλ.
$$

We're looking for an equation for $d2xμ/dλ2$ , since that will be the generalization of Newton's second law $x¨=0$ for a free particle in Newtonian mechanics. Then we need to get rid of the $gμρ$ in front. To do that, we just need to multiply by the inverse matrix, which it's conventional to indicate by raising up the indices: $gνμgμρ=δνρ$ , where $δ$ denotes the identity matrix with 1's along the diagonal. Anyway, after multiplying by the inverse matrix we get

$$
d2xμdλ2+gμκ(∂gρκ∂xσ−12∂gρσ∂xκ)dxρdλdxσdλ=1ldldλdxμdλ.
$$

That's looking a little bit better—still complicated, but a little better. It would be even nicer if the right-hand-side vanished. And in fact we *can* make it vanish, by remembering that $λ$ was just an arbitrary parameter that we get to pick. In particular, if we choose $λ$ to be equal to the proper time—i.e. $dλ=dτ=1c−gμνdxμdxν$ —then we get

$$
l=−gμνdxμdτdxνdτ=c.
$$

So with this choice, $l$ is a constant, and so $dl/dλ=0.$ Convenient! Then our equation of motion simplifies to

$$
d2xμdτ2+gμκ(∂gρκ∂xσ−12∂gρσ∂xκ)dxρdτdxσdτ=0.
$$

This, at last, is the **geodesic equation**. Back in Minkowski spacetime, where the metric is constant, the second term vanishes. Then we're left with the equation of a straight line:

$$
d2xμdτ2=0.
$$

But in a curved space, the second term introduces a deformation of the straight line. A geodesic is as straight as you can *get* in a curved spacetime. By adding any wiggles to the curve, we would increase its length—or, rather, decrease the proper time—and therefore it wouldn't be an extremal path anymore.

There's one more manipulation we should make to put the equation of motion into the standard form that people usually write the geodesic equation. Notice that, in the second term, the combination of $dxρ/dτ$ and $dxσ/dτ$ is symmetric in $ρ$ and $σ$ —if you swap the two of them the equation doesn't change. That means in the thing in parentheses that's multiplying those derivatives, we can freely symmetrize in $ρ$ and $σ$ —effectively, take the average of that expression with the one we get by exchanging the two indices. Then we can write the same equation as

$$
d2xμdτ2+12gμκ(∂gσκ∂xρ+∂gρκ∂xσ−∂gρσ∂xκ)dxρdτdxσdτ=0.
$$

The combination that appears here is called the **Christoffel symbol**,

$$
Γρσμ=12gμκ(∂gσκ∂xρ+∂gρκ∂xσ−∂gρσ∂xκ).
$$

It's a very important object in the mathematics of a curved geometry, but for our purposes here we can just think of it as some matrix $Γμ$ for each coordinate $μ$ , with components $(Γμ)ρσ$ .

Anyway, at long last we wind up with the standard form of the geodesic equation,

$$
d2xμdτ2+Γρσμdxρdτdxσdτ=0.
$$

That calculation got a little hairy, which is why I didn't include it in the video itself. If you're new to all this curved geometry business, don't worry too much about the details of these equations for right now. You can learn to unpack them all later on if you're interested in properly studying GR.

The geodesic equation describes the motion of a free particle in the presence of some other much more massive objects that created the warped geometry. It's the generalization of Newton's second law for a free particle, $F=ma=0$ , to general relativity. Note that the equation doesn't depend on the mass $m$ of the particle. All particles travel along geodesics, regardless of their mass.

The last thing I want to do is give you an intuitive idea of what geodesics are all about by describing what's probably the simplest example of a curved space that we can all picture: the surface of a sphere. These aren't directly relevant to the geodesics in spacetime that we encounter in general relativity, but they'll at least give you an idea that you can picture in your head to understand what a geodesic is.

![[Read It Later/attachments/290fce135b3358d4fa3fe4c84f971653_MD5.png]]

So picture a sphere, and pick any two points on it. To find the geodesic between them, just draw an equator of the sphere that goes between the two endpoints. In other words, think of the sphere as an onion, and chop the onion in half so that your knife goes through both of the given points. Call one half the "northern" hemisphere and the other the "southern" hemisphere. The cut you made is along the "equator", and it defines a geodesic between the two points (two, actually, one going the short way around and the other the long way).

Okay, that was a very quick introduction to a bunch of very challenging, but also hopefully very interesting ideas. So let me quickly summarize the key things we learned about.

Spacetime is the stage on which physical processes play out, and Einstein's theory of relativity might better be called the theory of spacetime, because it tells us how to understand the structure of spacetime. It's a framework for doing physics, and we can build on top of it additional features like particles and forces and fields.

*Free* particles basically travel along the straighest and shortest paths through spacetime that they can—with the caveat that, in spacetime, "shortest" actually means maximizing the proper time, which is the time that's ticked off on a watch that's strapped to the particle.

In special relativity, we ignore the effect of gravity (or, at least, we assume that it's weak). Then spacetime is flat, and a free particle literally travels along a straight line.

General relativity builds gravity into the structure of spacetime by warping the metric into a curved geometry. The way that works is governed by Einstein's equations, which we didn't talk much about here. Then a free particle follows the next-best-thing to a straight line: what we called a geodesic.

The action for a free particle in either special relativity or general relativity is the same: it's simply equal to the length of the worldline that the particle traces out as it moves through spacetime, up to some constant factors. Then the principle of least action says that the particle indeed follows the shortest path that it can in getting from one point to another.

---

See also:

- Part 1: [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- Part 2: [The Special Relativistic Action, Explained](https://www.physicswithelliot.com/special-relativity-action-mini-notes)
- Part 4: [The Action for String Theory](https://www.physicswithelliot.com/string-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).