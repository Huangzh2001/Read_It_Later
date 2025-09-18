---
date: "2025-08-10T22:08:06+08:00"
url: "https://www.physicswithelliot.com/gr-limits-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=V8fSYnY9Bj0)

In the course of your physics education, you’ve likely heard about two radically different pictures of gravity due to the two greatest titans in history of physics: Isaac Newton and Albert Einstein. In the first case, Newton proposed a fairly straightforward universal law of gravitation: every pair of masses in the universe experience an attractive force between them that falls off as one over their separation squared. Einstein, on the other hand, saw gravity very differently. According to his general theory of relativity, massive objects warp the very geometry of spacetime, causing other particles nearby to deviate from the straight paths they would otherwise follow traveling through the empty void of outer space.

[[Read It Later/attachments/2361b1c4d60690678a8d0a17c6ad94d1_MD5.png|Open: 2361b1c4d60690678a8d0a17c6ad94d1_MD5.png]]
![[Read It Later/attachments/2361b1c4d60690678a8d0a17c6ad94d1_MD5.png]]

But here’s a question you may have wondered about: how do these two completely different descriptions lead to nearly the same predictions for, say, the orbit of our home planet around the Sun?

After all, Einstein’s theory is beautiful, but it’s also famously complicated. And yet over 200 years earlier, Newton, with his simple $1r2$ force law, already correctly predicted the motion of Earth around the Sun to remarkable accuracy, in what was arguably the most profound scientific achievement in the history of humanity up to that point. Simply by plugging Newton’s force into $F=ma$ , we’re able to derive the elliptical orbits of the planets in our solar system [with just a few lines of math](https://www.physicswithelliot.com/orbits-mini-notes), as [we’ve discussed](https://www.physicswithelliot.com/runge-lenz-mini-notes) in past lessons.

Einstein’s general relativity, meanwhile, launched gravity into the 20th century and beyond, leading to the discovery of incredible new features of gravitational physics like black holes, gravitational lensing, and cosmology that have completely reshaped the way we look at the universe. But back in the humble arena of predicting the orbits of planets around stars, we know that Newton’s law already did a remarkably competent job at the task, up to surprisingly small errors. To very good approximation, the equations for a planet traveling around a star obtained from $F=ma$ and Newton’s law of gravity are correct, and therefore Einstein’s far more elaborate description must reduce to the same simple equations when applied to the same problem.

So the question is, how does Einstein’s geometric theory of spacetime reduce to Newton’s comparatively simple theory in the limit where they’re both supposed to describe the same physics, like a planet circling a star? And in the opposite limit when gravity is taken to the extreme, how does Einstein's theory stretch beyond Newton's and predict the most powerful gravitational objects in the universe: black holes?

![[Read It Later/attachments/2c0df50072f5b9999f11d587ce331d7d_MD5.png]]

You’re hopefully familiar with the basics of Newton’s law of gravity. Given two particles of masses $M$ and $m$ , and separated by a distance $r$ , Newton says that there’s an attractive force between them given by

$$
F=−GMmr2,
$$

where $G$ is the gravitational constant—an experimentally measured number that characterizes how strong the gravitational force is. Equivalently, the gravitational potential energy is given by

$$
U=−GMmr,
$$

with the force is being minus the derivative of $U$ .

By plugging this into $F=ma$ for the Earth, we get a relatively simple equation that [we can solve](https://www.physicswithelliot.com/orbits-mini-notes) to figure out the shape of the Earth’s trajectory. The result is an ellipse, which agrees with experimental measurements to very good, though not perfect, accuracy.

Newton’s inverse-square law therefore does a good job describing the consequences of gravity in the typical circumstances that we encounter on a daily basis, from falling apples to the motion of our planet around the Sun. But it begins to fail when gravity is very strong or when it’s changing with time. For example, in the [field theory](https://www.physicswithelliot.com/fields-mini-notes) lesson I shared a couple of months ago, we discussed how if by some calamity the Sun were to suddenly vanish, according to Newton’s law the gravitational force on the Earth would go slack at the same moment. And despite being 92 million miles away, the trajectory Earth would instantaneously be altered. Einstein remedied this non-local, action-at-a-distance behavior of Newton’s law by replacing it with a gravitational field theory.

There’s one basic feature of Newton’s law that’s critical to notice to appreciate what lead Einstein on the road to his reimagined theory of gravity. The same $m$ that appears on the right-hand-side of $F=ma$ also appears in the gravitational force on that particle, and therefore the mass of a particle drops out entirely when we write down its $F=ma$ equation. *All* particles behave the same way in a given gravitational field, regardless of their mass. That’s the same underlying reason a bowling ball and a penny dropped off the side of the leaning tower of Pisa both fall at the same rate of about $9.8 m/s2$ , despite the fact that one is thousands of times heavier than the other.

This universality of gravity is what lead Einstein to the idea that gravity is a result of the curvature of spacetime, rather than a typical force. Since every particle regardless of its mass behaves the same way under the influence of gravity, Einstein reasoned that gravity must actually be a feature of the *background* along which all particles move. And since he had already discovered years earlier in his special theory of relativity that the background of non-gravitational physics is flat spacetime, Einstein conjectured that what we observe as gravity results from the curvature of spacetime in the presence of huge sources of mass and energy. He therefore generalized his special relativity theory to incorporate gravity, and the result, general relativity, was the crowning achievement of pre-quantum physics.

The basic picture goes like this. Already in special relativity, Einstein, as well as Minkowski and Lorentz and others, showed that the three dimensions of space and one of time are unified in a single, four-dimensional structure: spacetime. Out in the empty void of outer space, far away from any stars and planets and so on, spacetime is flat. This geometry is called **Minkowski spacetime**. An interstellar particle traveling along its merry way out here just cruises in a straight line with constant velocity. It’s taking the shortest and straightest possible path that it can through spacetime.

But if instead of empty outer space we look in the vicinity of a massive star like the Sun, the fabric of spacetime becomes curved, like the surface of a trampoline with a bowling ball placed in the middle of it. Then introducing a comparatively smaller object like a planet moving near the star is analogous to rolling a little marble around the valley of the trampoline that’s been formed by the much larger bowling ball. The planet is likewise traveling through the curved spacetime that’s been warped by the presence of the star, and as a result, the path that it follows is deformed away from the straight line that it would have traversed in empty outer space.

There’s no force acting on the planet per se though. It’s still just traveling along on the shortest and straightest possible path that it can, only now it’s charting out this path through a curved spacetime. The shortest and straightest path through a curved geometry like this is called a **geodesic**, and that’s the route the planet follows as it orbits around the star.

Thus, there are two sides to Einstein’s theory. Number one is how the presence of mass and energy causes the geometry of spacetime to become curved. This relationship is quantified by what are called, naturally enough, **Einstein’s equations**. They’re differential equations that determine the shape of spacetime that results from introducing massive objects like stars. The second half of the story is about how other, comparatively smaller objects move in this subsequent curved geometry. They follow these shortest and straightest paths called geodesics, and their motion is governed by the **geodesic equation**.

What we’re going to uncover in the rest of this lesson is how the geodesic equation in a warped geometry reduces to the inverse-square law in the circumstances where Newton’s law of gravity is an accurate description of nature. We’ll see that the conditions under which Newton’s law applies are where

1. Gravity is relatively weak, like when you’re far away from a star, as opposed to, say, inside the horizon of a black hole
2. Gravity is constant, again like the steady gravitational field produced by an isolated and stable star
3. The planet is moving slowly compared to the speed of light, as in the Newtonian limit of any relativistic theory

Let's dig into the details now. Since general relativity is at its core a geometric theory, we should start by learning a little bit of the necessary geometry. We covered a lot of this in the earlier lessons on the principle of least action in [special](https://www.physicswithelliot.com/special-relativity-action-mini-notes) and [general](https://www.physicswithelliot.com/gr-action-mini-notes) relativity, which you may want to look at as well.

![[Read It Later/attachments/5704d2c9ad69f23dd86a33d9e92d586b_MD5.png]]

Let’s begin by thinking about the regular old $xy$ plane. Say we have two points on the plane, and we want to find the distance between them. You’ve probably known since middle school that to find the answer we can just draw a triangle with the horizontal separation $Δx$ along the bottom leg and the vertical separation $Δy$ along the side leg. Then the length $Δs$ of the hypotenuse is given by the Pythagorean theorem,

$$
Δs2=Δx2+Δy2.
$$

But what if instead of this straight line between these two points, we’re handed some other curve connecting them; how do we find the length of that? To answer that question, all we need to do is zoom in and look at a pair of nearby points along the curve, which are *infinitesimally* separated by $dx$ and $dy$ . At such a tiny scale, this segment of the larger curve looks like a straight line again, and so its length is given by

$$
ds=dx2+dy2.
$$

$ds$ is called the **metric** on the flat plane, and it tells us how to measure distances in this space. In particular, to find the length of the whole curve, we just add up all these little segments by integrating over the path,

$$
l=∫ds.
$$

The curve might be given to us as a function $y(x)$ , in which case we could write the integral more transparently by pulling a $dx$ outside of the square-root:

$$
l=∫dx 1+(dydx)2.
$$

Then we’d just perform this integral from the starting $x$ to the final $x$ in order to compute the length of the curve.

Alternatively, our curve might better be described parametrically, meaning we’re given $x(λ)$ and $y(λ)$ as functions of some auxiliary parameter $λ$ . In that description, it’s more natural to multiply and divide the integrand by $dλ$ , and then bring the denominator inside the square-root like so:

$$
l=∫dλ (dxdλ)2+(dydλ)2.
$$

This integral, then, tells us how to compute the length of any curve in the $xy$ plane connecting our two given points.

A natural question to then ask is, which is of these many curves has the *shortest* length? The answer, of course, is a straight line; the same line segment of length $Δx2+Δy2$ as we started with. Actually proving that fact amounts to essentially the same math that we’ve talked about in past lessons on [the principle of least action](https://www.physicswithelliot.com/least-action-mini-notes).

All this of course generalizes straightforwardly to any number of dimensions. For example, 3D flat space with coordinates $x,$  $y$ , and $z$ is described by the metric

$$
ds2=dx2+dy2+dz2.
$$

This metric is pretty simple, but more general geometries can get a lot more complicated. So it’s convenient to have a more compact notation. We’ll write $Xi$ for the three coordinates of space, $X1=x$ , $X2=y$ , and $X3=z$ . Take note that those superscripts are labels for the three directions of space, not exponents.

Then we can likewise write $dXi=(dx,dy,dz)$ for the infinitesimal steps in each direction, and so put together the whole metric as a sum

$$
ds2=∑i,j=13gijdXidXj,
$$

where $gij$ is a $3×3$ matrix with components labeled by $i$ and $j$ . In this case it’s literally just the identity matrix:

$$
gij=(100010001).
$$

That way when we expand out the sum, the only terms that contribute are the diagonal ones,

$$
∑i,j=13gijdXidXj=g11dX1dX1+g22dX2dX2+g33dX3dX3,
$$

and we get back the same simple formula for $ds2=dx2+dy2+dz2$ as before. The matrix $gij$ itself is often referred to as the metric, too. This notation is complete overkill for a simple setup like this one, but trust me it’s essential for working with the equations of general relativity.

We also don’t even have to use Cartesian coordinates if we don’t want to. Back in 2D, for example, we could write the same metric $ds2=dx2+dy2$ as before in terms polar coordinates $r$ and $ϕ$ as

$$
ds2=dr2+r2dϕ2.
$$

In this case, $rdϕ$ is the arc length of a tiny segment of a circle extending between the angles of the two points (i.e. arc length = radius $×$ angle) and then $dr$ is the radial separation between them.

Or in 3D we might use spherical coordinates $r,ϕ$ , and $θ,$ in which case

$$
ds2=dr2+r2(dθ2+sin2⁡(θ)dϕ2).
$$

This one may look less familiar, but the idea is the same. We’ll stick to Cartesian coordinates for most of this lesson, except at the end when we deal with the Schwarzschild metric of general relativity.

Okay, all that was about how we measure distances in geometry. Now let’s see how it enters into the physics. Before Einstein came along, the way we thought about the world was as a great big 3D space with coordinates $x,$  $y$ , and $z$ , plus a totally independent time coordinate $t$ , and they don’t talk to each other. Einstein changed all that. He realized that the cutting-edge physics theory of the day—electromagnetism—was only self-consistent if space and time are unified into a single, four-dimensional geometric structure called **spacetime**.

And the geometry of spacetime isn’t just the obvious four dimensional version of the 2D and 3D spaces we were just talking about. Instead, it’s described by the **Minkowski metric**,

$$
ds2=−c2dt2+dx2+dy2+dz2.
$$

It’s that minus sign in front of the time term that’s responsible for most of the weird and wild features of special relativity that you might be familiar with. And that factor of $c$ is there so that this new term has the same units of length-squared as all the other terms in this formula. That’s because we Earthlings usually measure distances in meters and time in seconds, so we need to multiply $dt$ by something with units of meters per second in order to get a length. It follows that massive particles moving through this space must always travel slower than this maximum speed $c$ , and that massless particles always travel at precisely $c$ . Since photons, the particles of light, are the most familiar massless particles, we typically refer to $c$ as the “speed of light.”

Just like we defined $Xi=(x,y,z)$ as a shorthand to denote the coordinates of 3D space, we can define a four-component vector to denote a point in spacetime. We write it as $Xμ$ , where $μ=0,1,2,$ and $3$ is an index labeling the four components:

$$
Xμ=(X0X1X2X3)=(ctxyz).
$$

So $X1$ , $X2$ , and $X3$ are the spatial coordinates just like before, while $X0=ct$ is the new time coordinate that now gets tacked on in the $μ=0$ slot. The factor of $c$ in the first entry is again there so that all the components have the same dimensions of length.

Also notice that I’m using a Greek letter $μ$ (”mu”) here to denote the components of the spacetime point. It’s conventional to use Greek letters (like $μ,ν,ρ,σ,$ and so on) to label spacetime coordinates running over $0,1,2,3$ , and non-Greek letters like $i$ and $j$ to label spatial coordinates like we did a minute ago, which only run over $1$ , $2$ , and $3$ .

Now we can write the Minkowski metric using the same compact notation as before, only this time we sum over the four spacetime coordinates:

$$
ds2=∑μ,ν=03gμνdXμdXν.
$$

The $4×4$ matrix $gμν$ is still diagonal, but now its top left “00” entry is $−1$ instead of $+1$ , to take care of that pesky minus sign in the Minkowski metric:

$$
gμν=(−1000010000100001).
$$

Actually, this matrix for the Minkowski metric is so important that we usually reserve the special symbol $ημν$ to denote it, rather than the generic symbol $gμν$ that we might use for any spacetime metric.

As a particle lives out its days traveling around the universe, it traces out a curve $Xμ(λ)$ through spacetime called its **worldline**, where $λ$ is again a parameter. Notice that even if the particle is sitting still in space, it’s still traveling forward through *time*, and so we’d draw its worldline as a vertical line in a picture like this with time flowing up along the vertical axis. (For whatever reason it’s conventional to draw time on the vertical axis and space on the horizontal axis in pictures like these.) More generally, if the particle is moving around, its worldline will be a more interesting curve. Its slope can never dip below $45∘$ though, because that would mean that the particle is traveling faster than the speed of light.

We can define the length of a worldline through spacetime similarly to what we did at the start. The obvious thing to write down would be

$$
∫ds=∫−c2dt2+dx2+dy2+dz2,
$$

but that gets us into a little bit of trouble, again because of the minus sign in the Minkowski metric. For the particle that was just sitting at rest, $dx=dy=dz=0$ , and so the thing inside the square-root is negative. And in fact that’s always true along the worldline of a massive particle. So the more natural way to define the length of a worldline in spacetime is to flip the sign of the metric before we take the square-root:

$$
∫−ds2=∫c2dt2−dx2−dy2−dz2.
$$

And once again we can multiply and divide by $dλ$ to turn this into a more familiar looking integral:

$$
∫−ds2=∫dλ −∑μ,ν=03ημνdXμdλdXνdλ.
$$

Thus, as the particle travels through spacetime, it traces out a curve $Xμ(λ)$ , and this integral computes the length of the curve. But what the heck does that represent, physically? Notice again that if we look at a particle sitting at rest, we simply get

$$
∫−ds2=ct.
$$

That's $c$ times the amount of time that’s ticked off on a clock in the laboratory or on a wristwatch that you’ve strapped to the particle. But once the particle starts moving around, the time $τ$ on its wristwatch [will tick more slowly](https://www.physicswithelliot.com/special-relativity-action-mini-notes) than the time $t$ on the wall clock, and that’s precisely what length of the worldline (divided by $c$ ) measures:

$$
τ=1c∫−ds2.
$$

$τ$ is called the **proper time** of the particle, and again it’s the time that you’ll see on the particle’s watch as it carries on its business. In fact, it’s natural to replace the arbitrary parameter $λ$ that we used to parameterize the worldline $Xμ(λ)$ with $τ$ itself,

$$
Xμ=Xμ(τ),
$$

and just specify where the particle is as a function of the reading on its watch. From now on, we’ll make this choice.

Just like the shortest path connecting two points in the $xy$ plane was a straight line, a free particle in Minkowski spacetime also travels along a straight line. Except that again because of that minus sign in the metric, instead of minimizing the length between two spacetime points, a straight line *maximizes* it. Thus, the important physical takeaway here is that a particle follows the path through spacetime that maximizes its proper time (or, at least, extremizes it).

So far here, we’ve been working in flat, Minkowski spacetime. This is the domain of special relativity. But as we’ve discussed, in the general theory which incorporates gravity, spacetime becomes curved. What that means is that instead of the flat, Minkowski metric,

$$
ds2=∑μ,ν=03ημνdXμdXν,
$$

in a curved spacetime the constant matrix $ημν$ is replaced by a function $gμν(X)$ that depends on where you’re at in spacetime:

$$
ds2=∑μ,ν=03gμν(X)dXμdXν.
$$

The same tools that we’ve developed generalize straightforwardly to the curved case, though. A particle once again traces out a worldline $Xμ(τ)$ through the spacetime parameterized by its proper time,

$$
τ=1c∫−ds2,
$$

which is the time that’s ticked off on the particle’s watch.

What’s changed, though, is that the particle isn’t going to travel along a straight line anymore. In fact, now that it’s moving through curved spacetime, it’s not really clear what it even means for a line to be straight! But the underlying physical principle is the same: the particle follows the shortest and straightest route that it can through this curved geometry, which, more precisely, is to say that it takes the path that maximizes its proper time $τ$ .

Given a metric $gμν$ and our formula for $τ$ , it’s just a mathematical question now to determine the path of maximum proper time. I went through that calculation in the [previous](https://www.physicswithelliot.com/gr-action-mini-notes) general relativity lesson. For now I’ll just remind you of the answer: the condition for the worldline to maximize the proper time is that $Xμ(τ)$ must satisfy the **geodesic equation**,

$$
gμρd2Xρdτ2+(∂gσμ∂Xρ−12∂gρσ∂Xμ)dXρdτdXσdτ=0,
$$

and the solution is called a geodesic. This condition is generalization of Newton’s second law $F=ma=0$ for a free particle in curved spacetime.

So, according to Einstein, a planet like Earth orbiting around a star like the Sun follows a trajectory determined by solving the geodesic equation. But how in the heck does this complicated looking equation reproduce Newton’s inverse-square law of gravity? After all, despite its shortcomings, Newton’s theory does a very good job of predicting the elliptical orbit of the Earth. If Einstein’s theory is going to supplant Newtonian gravity, it had better reproduce the same equations in the appropriate limit where Newton’s theory made correct predictions.

So in what limit should we expect general relativity to reduce to Newtonian gravity? To start with, just like special relativity turns back into Newtonian mechanics when particles aren’t moving too quickly compared to the speed of light, likewise we should only expect Newtonian gravity to do a good job when the speed of the planet is small. And indeed, the average speed of the Earth is of order $30,000 m/s$ , a tiny fraction of the $300,000,000 m/s$ that light travels at. Our first requirement for the Newtonian limit of general relativity is therefore:

1. The speed of the particle is small compared to the speed of light,
	$$
	dXidt≪c.
	$$

Next, it’s only fair to expect Newton’s theory to apply when gravity is comparatively weak. Deep inside a black hole, for example, where the unimaginable density of a dying star has so warped the geometry of spacetime that even a ray of light can’t climb back out, we shouldn’t expect the inverse-square law to approximate the gravitational force. Therefore the geometry of spacetime should be fairly close to flat Minkowski spacetime as it would be in truly empty outer space, and only slightly perturbed away from it by the presence of something like star far away:

1. The metric near the particle differs from Minkowski spacetime by a small deviation,
	$$
	gμν(X)=ημν+εμν(X),
	$$
	where $|εμν|≪1$ is tiny.

Finally, thinking back to our thought experiment where the Sun suddenly vanished, and Newton’s law incorrectly predicted that the trajectory of the Earth would instantaneously change, we should only expect Newton’s theory to apply when the gravitational field is constant (or, at least, slowly varying):

1. The metric is independent of time,
	$$
	∂∂tgμν=0.
	$$

Under these three conditions, we know that Newton’s inverse-square law already does a good job predicting the orbit of a planet like Earth, and therefore Einstein’s equations had better reduce to Newton’s in this limit. Let’s uncover how that works.

Let’s start with the first condition, that the particle is moving slowly compared to the speed of light. If we move the $dt$ to the right-hand-side and then divide both sides by $dτ$ , we can write the same condition as

$$
dXidτ≪cdtdτ.
$$

And remembering that $X0=ct$ ,

$$
dXidτ≪dX0dτ.
$$

The second term of the geodesic equation contains a sum over the derivatives of $Xρ$ and $Xσ$ with respect to $τ$ ,

$$
∑ρ,σ=03(⋯)dXρdτdXσdτ.
$$

But because the $τ$ derivatives of the spatial coordinates are so small compared the derivatives of $X0$ , we can just drop them and approximate

$$
∑ρgμρd2Xρdτ2+(∂g0μ∂X0−12∂g00∂Xμ)dX0dτdX0dτ=0.
$$

And since moreover from condition 3 we’ve assumed that $∂∂X0gμν=0$ , we can further reduce this down to

$$
∑ρgμρd2Xρdτ2=12c2∂g00∂Xμ(dtdτ)2.
$$

That’s already looking way simpler!

Next up, let’s try to get rid of all these $dτ$ ’s, so that we can try to write down Newton’s law $md2Xidt2=Fi$ like we normally would, determining the second derivatives of the spatial coordinates with respect to $t$ . $dτ$ , remember, is defined by flipping the sign of the metric,

$$
c2dτ2=−∑μ,νgμνdXμdXν,
$$

or, dividing both sides by $dτ2$ ,

$$
c2=−∑μ,νgμνdXμdτdXνdτ.
$$

Now in the slow-moving limit we can again neglect the spatial derivatives with respect to $τ$ :

$$
c2≈−g00(dX0dτ)2.
$$

Then the proper time $τ$ on the particle’s watch and the coordinate time $t$ are simply related by

$$
dτ=dt−g00.
$$

This equation encapsulates **gravitational time dilation**, like when Matthew McConaughey drops down to a planet near the horizon of a black hole in Interstellar, and when he returns to his ship an hour later from his perspective, he finds that his crew mate back onboard has aged by 20 years!

But anyway, we can use this relation to convert the $τ$ derivatives in the geodesic equation into ordinary time derivatives $d2Xρdt2$ like we wanted just by applying the chain rule. For the first derivative, we get

$$
dXρdτ=dtdτdXρdt,
$$

where we’ve effectively just multiplied and divided by $dt.$ Then for the second derivative we similarly have

$$
d2Xρdτ2=dtdτddt(dtdτdXρdt).
$$

This is more complicated because the $ddt$ is going to hit both factors inside the parentheses by the product rule. But! We’ve seen that in the slow-moving approximation $dtdτ=1−g00,$ and moreover because we’ve also assumed $gμν$ is independent of $t$ , $ddtdtdτ$ is equal to zero! Then the derivative slides right through to hit $dXρdt$ , and we're left with

$$
d2Xρdτ2=(dtdτ)2d2Xρdt2.
$$

We couldn’t have asked for a simpler result! The factors of $(dtdτ)2$ on the two sides of geodesic equation simply cancel, and we’re left with

$$
∑ρgμρd2Xρdt2=12c2∂g00∂Xμ.
$$

That complicated equation that we started with keeps getting simpler and simpler. Lastly, let’s use the fact that gravity is weak, and we can expand $gμν(X)=ημν+εμν(X)$ around Minkowski spacetime, with a tiny perturbation $εμν.$ Plugging this into the geodesic equation gives

$$
∑ρ(ημρ+εμρ)d2Xρdt2=12c2∂ε00∂Xμ.
$$

We’re so close to the Newtonian equation of motion now. Notice that when $εμν=0$ , so that gravity is turned off and we’re literally looking at a free particle coasting through the empty void of outer space, we get $d2Xρdt2=0$ , just as we should. Then when we turn $εμν$ back on, the factor of $ε00$ on the right-hand-side already means that $d2Xρdt2$ will scale with at least one power of $ε$ . So in fact the $εμρd2Xρdt2$ term on the left is already at least second order in the tiny perturbation, and we can discard it:

$$
∑ρημρd2Xρdt2=12c2∂ε00∂Xμ.
$$

This is really four equations in one, remember, because $μ$ ranges over $0,1,2,$ and $3$ . The $μ=0$ term isn’t interesting; it just says that $0=0$ . What we really want are the spatial terms. And since $η$ is a diagonal matrix with $η11=η22=η33=1$ , we simply get

$$
d2Xidt2=12c2∂ε00∂Xi,
$$

Here at last is the equation of motion for a planet like Earth that’s moving slowly through a weak, constant gravitational field like what’s produced far away from the Sun.

Newton’s inverse-square law is meanwhile $F=−GMmr2,$ which corresponds to the gravitational potential energy $U=−GMmr$ . Force, remember, is given by minus the slope of the potential energy, or more precisely

$$
Fi=−∂U∂Xi.
$$

Then Newton’s second law can just as well be written

$$
md2Xidt2=−∂U∂Xi.
$$

But this is exactly the form of the equation of motion we got by taking the limit of the geodesic equation:

$$
md2Xidt2=−∂∂Xi(−12mc2ε00).
$$

Einstein’s theory will therefore reproduce what we already know about Newtonian gravity provided that

$$
−12mc2ε00=−GMmr,
$$

and therefore

$$
ε00=2GMrc2.
$$

The question is, is the metric that results from the warping of spacetime produced by the Sun’s presence indeed of the form $gμν=ημν+εμν,$ with $ε00$ given by this formula? That’s the other half of Einstein’s theory: massive objects like stars warp the geometry of spacetime according to Einstein’s equations, and then smaller objects like planets move through the warped geometry along the shortest and straightest paths they can, the geodesics that we’ve been investigating.

Einstein’s equations are famously difficult to solve, but in the special case of a single, spherically symmetric object of mass $M$ , like we can reasonably approximate our Sun as, the equations admit a simple solution. It’s called the **Schwarzschild metric**, and it’s most conveniently written in spherical coordinates

$$
ds2=−(1−2GMrc2)c2dt2+(1−2GMrc2)−1dr2+r2(dθ2+sin2⁡(θ)dϕ2).
$$

This is the metric produced by a star of mass $M$ at the origin of otherwise empty space. It’s certainly more complicated looking than the flat Minkowski metric that we started with, but on the whole it’s really quite remarkable how simple the answer is. Notice first of all that when you move very far away from the star by making $r$ large, the metric becomes

$$
ds2=−c2dt2+dr2+r2(dθ2+sin2⁡(θ)dϕ2)⏟dx2+dy2+dz2,
$$

which is nothing but Minkowski spacetime again, just written in spherical coordinates! That makes sense, because when you’re very far away from the origin you barely even know that there’s a star there, and when you look around all you see is flat Minkowski spacetime.

What the Schwarzschild metric shows us is that as you get closer to the star, the geometry gets modified by these corrections to the $dt$ and $dr$ terms specified by $2GMrc2.$ And that’s exactly the behavior we found that we need to reproduce Newton’s inverse-square law of gravity! In particular, the time component of the Schwarzschild metric is

$$
g00=−1+2GMrc2,
$$

which is precisely of the expected form $g00=η00+ε00$ with

$$
ε00=2GMrc2.
$$

And thus the geodesic equation for a planet like Earth moving in the Schwarzschild geometry of a star like the Sun is nothing but the $F=ma$ equation for Newton’s original inverse-square law of gravity, whose solutions we know are the elliptical orbits of the planets!

Of course, it was a *lot* more work to discover these elliptical orbits using general relativity rather than the $1/r2$ law. So why do we even need general relativity here at all? What we’ve uncovered is that Newton’s law is only an approximation to Einstein’s more precise theory, that holds when gravity is constant and relatively weak, and a planet is moving slowly. And indeed, the gravity produced by the Sun is certainly more-or-less constant on the time scale of a planetary orbit.

But on the other hand, how weak is the gravitational field produced by the Sun? In our analysis, it was essential that $ε00=2GMrc2$ was a very small number. For a given star of mass $M$ , that means that you’d better be far enough away so that

$$
r≫2GMc2,
$$

which ensures that $ε00≪1.$ The closer you get to the star, the stronger its gravity becomes, and the poorer the job Newton’s law does approximating it. In particular, the corrections from general relativity in our solar system are most pronounced for the closet planet to the Sun: Mercury. Einstein’s more precise theory explains why Mercury’s orbit is not a perfect ellipse, but instead precesses as it travels around the Sun, meaning that the point in space where Mercury gets closest to the Sun changes slightly with each revolution. The pull from the other planets in the solar system also contributes to this effect, but the contribution predicted from Einstein’s equations was one of the first experimental tests of his theory.

Finally, let's consider the opposite limit that we've been focusing on so far, where gravity is strong. You might have noticed something curious about the Schwarzschild metric:

$$
ds2=−(1−2GMrc2)c2dt2+(1−2GMrc2)−1dr2+r2(dθ2+sin2⁡(θ)dϕ2).
$$

As we’ve seen, it reduces to flat spacetime when $r$ is far away, but as you get closer to the origin the corrections from the $2GMrc2$ terms become more and more important. And if you decrease $r$ *all* the way to $r=2GM/c2$ , the time component of the metric vanishes and the $r$ component blows up! Something remarkable seems to be happening here.

This special radius

$$
Rs=2GMc2
$$

is called the **Schwarzschild radius** of the geometry. If you plug in the numbers, you’ll find that $Rs≈3000 m$ for a star like the Sun. The radius of the Sun itself, on the other hand, is vastly larger: $R≈7×108 m$ . An orbiting planet can never get any closer to the origin than the radius of the star, of course, without disastrous consequences, so the planets in our solar system never have to worry about crossing below the Schwarschild radius. And indeed our solution for the metric only applies *outside* the Sun anyway, since once you pass inside the star you’re confronted with a blazing hot gas of matter and energy that drastically changes the solution of Einstein’s equations.

But suppose that a massively powerful alien were to come along and grip the Sun so tightly that they compressed it into an incredibly small ball of radius less than $3000 m.$ The result would be an unimaginably dense sphere. And yet, the same Schwarzschild metric will describe the geometry of spacetime outside the star, since that was the unique spherically symmetric solution to Einstein’s equations. Now the Schwarzschild radius lies outside the radius of the ball itself, and a nearby planet—or a *very* intrepid astronaut—could approach it and cross inside this critical radius. What would they discover inside?

Alas, they would never be able to tell us the answer. By compressing the matter into such a profoundly dense pocket smaller than the Schwarzschild radius, a black hole is formed. Once the astronaut passes inside the Schwarzschild radius, called the event horizon, no signal that they send back out can ever escape the gravitational pull—not so much as a beam of their flashlight will ever make it out.

Nothing particularly dramatic happens to the astronaut as they cross the horizon, though. Even though it looked like the Schwarzschild metric is singular there, that's actually only because of a bad choice of coordinates. The geometry is perfectly well-behaved at the horizon, and you wouldn't even necessarily know once you've crossed it. As you fall deeper into the black hole, though, things get more unpleasant.

Needless to say, black holes are some of the most fascinating objects in physics. Newton’s theory of gravity is completely ignorant of their existence. It took Einstein’s radical reimagining of the fabric of spacetime to discover these utterly mysterious, and yet thoroughly ubiquitous features of the universe.

---

See also:

- [How Newton Derived the Orbit of Our Home Planet](https://www.physicswithelliot.com/orbits-mini-notes)
- [Field Theory Fundamentals](https://www.physicswithelliot.com/fields-mini-notes)
- [The Special Relativistic Action](https://www.physicswithelliot.com/special-relativity-action-mini-notes)
- [The General Relativistic Action](https://www.physicswithelliot.com/gr-action-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).