---
date: "2025-08-10T22:16:53+08:00"
url: "https://www.physicswithelliot.com/hanging-rope-classic-notes"
status:
---
## How Do You Find The Shape of a Hanging Rope? Classic Physics Problem

![](https://www.youtube.com/watch?v=-vmVMTzbIxA)

When a rope is hung up with its two ends pinned down at some pair of points, it makes a shape called a **catenary**. How can we determine the shape of the rope?

Whenever we have a continuous object like this rope, we can imagine slicing it up into many little pieces. Since the rope is at rest, the total force on each little piece must be zero. Imposing this condition will tell us the shape that the whole rope must take.

![](https://www.physicswithelliot.com/s/string-fbd.png)

The forces on a bit of rope are gravity pulling straight down and two tension forces: one pointing forward along the rope and the other pointing backward. These three forces must add up to zero in order for the bit of rope to be in equilibrium. Note first of all that this means the horizontal component of the tension must be constant, so that the tension pointing to the right at one end cancels the tension pointing to the left at the other end:

$$
Tx(x)=C.
$$

The difference in the vertical components of the two tension forces must meanwhile cancel out the weight of the segment:

$$
Ty(x+dx)−Ty(x)=gdm,
$$

where the left end of the rope is at the horizontal position $x$ and the right end is at $x+dx.$

The rope is uniform, meaning it has constant mass per unit length $ml$ . Then the mass of the little piece of length $ds$ is

$$
dm=mlds.
$$

In the limit that the width $dx$ of the piece is very tiny, the length of the segment is just given by the Pythagorean theorem:

$$
ds=(dx)2+(dy)2=dx1+(dydx)2=dx1+y′(x)2.
$$

$y(x)$ is what we're looking for—the shape of the curve traced out by the hanging rope.

Now we can rewrite the equation for the vertical forces as

$$
Ty(x+dx)−Ty(x)dx=mgl1+y′(x)2.
$$

The left-hand-side is just the derivative of $Ty(x)$ with respect to $x$ . So thus far we've obtained two equations for the components of the tension:

$$
Tx(x)=CTy′(x)=mgl1+y′(x)2.
$$

The horizontal and vertical components of the tension aren't independent, though. Together they make a vector $T→=(Tx,Ty)$ that has to point along the tangent direction to the rope:

$$
ds→=(dx,dy)=dx(1,y′(x)).
$$

In particular, the ratio of the tension components $TyTx$ has to be the same as the ratio of the tangent vector components $dydx=y′(x)$ . So we learn that

$$
Ty(x)=y′(x)Tx(x).
$$

Combining these equations, we can eliminate $Tx$ and $Ty$ to get an equation for $y(x)$ alone:

$$
y″(x)=κ1+y′(x)2,
$$

where I've defined $κ=mglC.$ This is what we've been after: a differential equation whose solution will tell us the shape $y(x)$ of the rope. To solve it, note first of all that this second order equation for $y(x)$ is alternatively a first order equation for $u(x)=y′(x)$ :

$$
dudx=κ1+u2.
$$

We can separate variables here and integrate both sides to get $u(x)$ :

$$
∫du1+u2=κ∫dx.
$$

The integral on the left looks like something we might be able to do with a trig substitution. If we'd instead had the integral

$$
∫dv1−v2
$$

with a *minus* sign in the denominator, we could substitute $v=sin⁡θ.$ Then $dv=dθcos⁡θ$ in the numerator, and $1−v2=cos⁡θ$ in the denominator. The cosines cancel out, and we're left with

$$
∫dv1−v2=∫dθ=θ=sin−1⁡(v).
$$

Now what about the integral we actually wanted, with a plus sign in the denominator? By a change of variables $u=iv$ , we can write

$$
∫du1+u2=i∫dv1−v2=isin−1⁡(v)=isin−1⁡(ui).
$$

So the results of our integrals are

$$
isin−1⁡(ui)=κx+A,
$$

where $A$ is an integration constant. Solving for $u=y′$ , we get

$$
y′(x)=isin⁡(κx+Ai).
$$

But what's going on with these factors of $i$ ? Obviously the curve $y(x)$ and its slope $y′(x)$ should be real. In fact the above *is* a real function. The sine can be written in terms of exponentials as

$$
sin⁡θ=eiθ−e−iθ2i.
$$

This comes from Euler's identity, $eiθ=cos⁡(θ)+isin⁡(θ).$ Therefore,

$$
isin⁡(θi)=eθ−e−θ2,
$$

which is real. This function has a name: it's called the **hyperbolic sine**, $sinh⁡(θ)$ . So by integrating our differential equation for $y″(x)$ once, we've obtained

$$
y′(x)=sinh⁡(κx+A)=eκx+A−e−(κx+A)2.
$$

Now we just need to integrate once more to get $y(x)$ itself. The integral of $eκx+A$ gives back the same thing times $1/κ$ , and the integral of $e−(κx+A)$ is the same times $−1/κ$ . Then we find

$$
y(x)=1κ(eκx+A+e−(κx+A)2)+B,
$$

where $B$ is another integration constant. The function in parentheses again has a special name: it's the hyperbolic cosine, or $cosh.$ Then at last we've learned that

$$
y(x)=1κcosh⁡(κx+A)+B.
$$

So the shape of a hanging rope—aka a [catenary](https://en.wikipedia.org/wiki/Catenary) —is a hyperbolic cosine function!

The last thing to do is figure out the integration constants $A$ and $B$ , as well as the parameter $κ=mglC$ , since we never solved for the horizontal tension $Tx=C$ .

We're told where the ends of the rope are fixed, so let's set up our coordinates so that one end is at the origin $(0,0)$ and the other is at some point $(x0,y0).$ Then we get two conditions by requiring $y(0)=0$ and $y(x0)=y0$ :

$$
1κcosh⁡(A)+B=01κcosh⁡(κx0+A)+B=y0.
$$

Lastly, we have not yet imposed the fact that the rope is of length $l$ :

$$
l=∫ds=∫0x0dx1+y′(x)2,
$$

which implies

$$
1κ(sinh⁡(κx0+A)−sinh⁡(A))=l.
$$

This gives us three equations in the three unknowns $A,B,$ and $κ$ , which we can then solve for (numerically, in practice), to get the explicit curve $y(x)$ . You can see the results in the simulation below by dragging the red dot around to choose different endpoints $(x0,y0)$ for the rope.

---

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).