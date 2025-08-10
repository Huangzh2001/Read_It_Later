---
date: "2025-08-10T21:59:47+08:00"
url: "https://www.physicswithelliot.com/fields-mini-notes"
status:
---
## Field Theory Fundamentals

![](https://www.youtube.com/watch?v=13hCkUiu_mI)

In the three hundred and some years since the scientific revolution, the two deepest theories of nature that human beings have written down are the standard model of particle physics and Albert Einstein’s theory of gravity, general relativity. Both are examples of **field theories** —quantum in the first case and classical in the second—which describe the laws of nature in terms of fluctuating fields that permeate space and time. In this lesson, I'm going to give you an introduction to the fundamentals of classical field theory.

![](https://www.physicswithelliot.com/s/earth-sun.png)

First of all, what is field theory, and why do need it? We all start out in physics by looking at a bunch of particles, writing down the total force on each one, and then setting it equal to $ma$ . Think about the Sun and Earth, for example. According to Newton’s law of gravity, the Sun exerts a force on the Earth that pulls it toward it. The force is proportional to the mass of each, and goes as one over the distance squared between them:

$$
F=GMmr2.
$$

Then we can write down $F=ma$ for the Earth and solve for its orbit around the Sun. This was one of the first and most important accomplishments of modern physics.

But suppose that by some tragic calamity, the Sun suddenly exploded—or just mysteriously popped out of existence. What would happen? According to Newton’s theory, the gravitational force of the Sun on the Earth would suddenly vanish, and the Earth would veer off from its elliptical orbit along a straight line, like a spinning tetherball that shoots off when its string suddenly snaps. Apparently, the disappearance of the Sun would instantaneously cause a dramatic change in the motion of the Earth, 92 million miles away.

But that’s of course total nonsense. For example, the last rays of light emitted from the Sun before its disappearance would take about 8 whole minutes to travel that long distance to Earth and meet our eyes. As Einstein taught us about 200 years after Newton when he wrote down his special theory of relativity, nothing can travel faster than the speed of light, including the information that the gravitational pull of the Sun has gone slack. We would have no idea of our precarious condition until those 8 minutes had passed, and we were plunged into darkness.

This is where field theory comes in. Field theories build **locality** in from the beginning, so that the only points in space where you would even know the Sun had just vanished would be in its immediate vicinity. The data is stored in the **gravitational field**, $gμν(x,t)$ , which is a function of where you’re located in space ( $x$ ) and time $(t)$ . As time goes, the information about the Sun’s unfortunate demise would propagate outward like a shockwave through the gravitational field to farther and farther corners of the solar system and the universe. This was Einstein’s greatest achievement: constructing a relativistic field theory of gravity that reproduces Newton’s law in the circumstances when it holds, and completes it in a consistent way when it does not.

And the applications of field theory go way beyond gravity; it’s the framework we use to describe a huge range of phenomena in physics. Including, of course, the electromagnetic fields $E(x,t)$ and $B(x,t)$ that you’ve probably already encountered. Those rays of light traveling toward us from the Sun are ripples in the electromagnetic field, that likewise carry information along in a way consistent with relativity. And the standard model of particle physics—which is the most spectacularly predictive theory that physicists have ever come up with—is founded on field theory. The elementary particles like electrons, quarks, photons, and gluons, are all associated to fields, and the particles are interpreted as excitations of the fields.

But we’re getting ahead of ourselves. The standard model, general relativity, and even classical electromagnetism, are quite advanced examples of field theories. If you want to learn the subject, it’s better to start with a simpler example that illustrates the key ideas. The simplest example of a field theory is the theory of a single real field, denoted $ϕ(x,t)$ , called the **Klein-Gordon theory**.

In [previous lessons](https://www.physicswithelliot.com/least-action-mini-notes), I’ve told you about how instead of using $F=ma$ , we can formulate particle mechanics using a **Lagrangian** and applying the **principle of least action**. When it comes to solving classical mechanics problems with blocks and springs and so on, whether you use $F=ma$ or a Lagrangian is more or less a matter of convenience. But in field theory, the Lagrangian approach is fundamental. We *define* a field theory by writing down its Lagrangian.

So let’s quickly review how Lagrangians work for particles, and then we’ll generalize that for fields. Say we have a particle of mass $m$ with coordinate $x.$ We define the Lagrangian by taking the difference between the particle’s kinetic energy $K=12m(dxdt)2$ and its potential energy $U(x)$ :

$$
L=12m(dxdt)2−U(x).
$$

As the particle moves around with time, its kinetic energy and potential energy are changing, and so the Lagrangian is a function of time. We define the **action** by integrating the Lagrangian over time:

$$
S=∫titfdt L.
$$

![](https://www.physicswithelliot.com/s/paths.png)

Suppose the particle is traveling from starting point $xi$ at time $ti$ to another point $xf$ at time $tf$ . Then the question is: what trajectory $x(t)$ will it follow to get there? For any path connecting the two points, the action is a number that you get by integrating the Lagrangian over it. The principle of least action says that the particle is going to follow the path for which $S$ is smallest—or at least stationary.

And that’s not too hard to work out in practice. When you want to find the stationary points of an ordinary function, $f(x)$ , you just need to identify the points where its derivative vanishes, $f′(x)=0.$ Said differently, when you take a little step away from a minimum by shifting $x→x+ε$ for some little $ε,$ then the change in $f$ is zero to first order in $ε$ :

$$
df=f′(x)ε=0.
$$

That’s just because the tangent to $f$ at an extremum is a horizontal line, and when you take a step along a horizontal line the height of the function doesn’t change.

![](https://www.physicswithelliot.com/s/wiggles.png)

It’s the same with the action, except that now we want to find the *curve* $x(t)$ for which $S$ is minimized. So what we do is make a small variation of the curve by shifting $x(t)→x(t)+ε(t)$ , where $ε(t)$ is an infinitesimal function that adds little wiggles on top of our original curve, deforming it just a bit. If we indeed started at a minimum, then the action shouldn’t change under this shift.

First, let's figure out how the Lagrangian changes. Again, it’s just like taking the differential of a function, $df=f′(x)dx$ , except that now the Lagrangian is a function of both $x$ and $dxdt$ . From the kinetic energy term, we take the derivative and get $mdxdt$ , and then we multiply that by the change in $dxdt$ , which is $dεdt$ . And for the potential term we take its derivative and get $dUdx$ , times the change in $x$ , which is $ε$ :

$$
dL=mdxdtdεdt−dUdxε.
$$

Now let’s integrate the first term by parts, which just means to use the product rule

$$
ddt(mdxdtε)=md2xdt2ε+mdxdtdεdt
$$

to rewrite

$$
mdxdtdεdt=−md2xdt2ε+ddt(mdxdtε).
$$

Then the change in the Lagrangian is

$$
dL=−md2xdt2ε−dUdxε+ddt(mdxdtε).
$$

What integrating by parts bought us is that we can now pull out the common factor of $ε$ from the first two terms

$$
dL=−(md2xdt2+dUdx)ε+ddt(mdxdtε).
$$

So that’s how much the Lagrangian changes when we make a little change in the trajectory. The change in the action is the integral of this, and that’s what we want to vanish:

$$
dS=∫titfdt{−(md2xdt2+dUdx)ε+ddt(mdxdtε)}.
$$

The second term is easy, so let’s deal with that first. It’s the integral of a derivative, so we just get the difference between the endpoints:

$$
∫titfdt ddt(mdxdtε)=(mdxdtε)|titf.
$$

But we don’t want to allow just *any* $ε(t)$ ’s here. We’re looking at variations of the path *connecting* $(xi,ti)$ *to* $(xf,tf)$ , and so we don’t want the deformation $x(t)→x(t)+ε(t)$ to change the beginning and ending points of the curve. That means $ε(ti)=ε(tf)=0$ , and so this contribution to the change in the action is just zero!

So that leaves us with

$$
dS=−∫titfdt(md2xdt2+dUdx)ε(t),
$$

and the minimum trajectory is the one that makes this vanish for any little variation $ε(t)$ (that satisfies the boundary conditions). But the only way this integral can vanish for *any* $ε(t)$ is if the thing that it’s multiplying in the integrand is zero:

$$
md2xdt2=−dUdx.
$$

But that’s $F=ma$ ! Where remember the force is related to the potential energy by $F=−dUdx$ . So that’s how the principle of least action for a particle reproduces $F=ma$ , what we call the **equation of motion** for the particle.

Now we want to extend these ideas to field theory, where the central object isn’t the coordinate $x(t)$ of a particle, but a field $ϕ(x,t)$ that assigns a number to each point in space at each time. A simple example could be a temperature field $T(x,t)$ that tells you temperature at position $x$ at any time $t$ . It’s a function that takes a point in space and time and gives you back a number. Instead of the single degree of freedom we had corresponding to the position $x$ of the particle, we now have an *infinite* number of degrees of freedom for the field—one for each point in space. Field theories are complicated! But they’re commensurately powerful.

The Lagrangian is the starting point for a classical field theory—we write down an $L$ and take it as the definition of the theory. The action is again defined as the integral of the Lagrangian over time:

$$
S=∫titfdt L.
$$

We want the theory to be local—that was our main motivation for studying field theory in the first place—and so we’ll require that $L$ is itself the integral of a **Lagrangian density** over space:

$$
L=∫dx L(ϕ,∂ϕ∂x,∂ϕ∂t).
$$

In fact, in field theory we typically refer to $L$ itself as the Lagrangian. It’s a function of the field and its first derivatives at each point in space and time—that’s how writing the action in this way ensures we’ll get a local theory.

For a particle, we defined the Lagrangian as the kinetic energy minus the potential energy. We’ll define $L$ in essentially the same way:

$$
L=K−U,
$$

where $K$ and $U$ are the kinetic and potential energy *densities* of the field—in other words, energies per unit volume of space—since we’ll integrate this over space to get the full Lagrangian.

Analogous to $K=12m(dxdt)2$ , $K$ should go the like derivative of $ϕ$ with respect to time, squared:

$$
K=12c2(∂ϕ∂t)2.
$$

The speed of light squared $c2$ is there to get the units right, as well as to ensure our theory comes out consistent with relativity. Notice that there’s no $m$ here, unlike $12mv2$ . The field doesn’t have a mass like a particle, per se.

Next, what should we choose for the potential energy? Again, similar to a particle, where we can pick a potential $U(x)$ and it determines the kind of system that we’re studying, our choice for $U$ will depend on the theory we want to construct. But there is one contribution that we always want to appear. In relativity, time and space are supposed to enter on equal footing, and so since we have a term that goes like $∂ϕ∂t$ squared there should also be a term that goes like $∂ϕ∂x$ squared:

$$
U⊃12(∂ϕ∂x)2.
$$

This is sometimes called the gradient energy. In general, there will also be terms for the $y$ and $z$ directions, but I’ll mainly just write $x$ to keep things from getting too complicated. This is a very reasonable potential to include; it means that a field configuration with lots of wiggles in space will have a larger energy.

The rest of the potential depends on the theory we want to study. For a particle, the most fundamental potential energy function is probably the [harmonic oscillator](https://www.physicswithelliot.com/oscillator-help-room-notes) potential, $U=12kx2$ . Then likewise, a simple and important example of a field theory is obtained by choosing the rest of the potential to be quadratic:

$$
U⊃12κ2ϕ2,
$$

where $κ$ is a parameter that controls the strength of the potential, with dimensions of one over length.

This defines the **Klein-Gordon** **field theory**. All together, the Lagrangian density is

$$
L=12c2(∂ϕ∂t)2−12(∂ϕ∂x)2−12κ2ϕ2,
$$

plus the additional terms with $y$ and $z$ derivatives that I haven’t written. The minus signs are there for the same reason that $L=K−U$ in regular old particle mechanics. If we flip them to plus signs we’ll get the total energy density.

Again, this expression defines the Klein-Gordon field theory. And when we quantize it to make a *quantum* field theory, it describes the relativistic quantum physics of free, spin 0 particles of mass

$$
m=ℏκc.
$$

We’ll see where this mass comes from in a minute. Actually, particle physicists usually work in units where $ℏ$ and $c$ are both set to 1, so you’ll usually find the parameter $κ$ written as $m$ in textbooks, which is the mass of the particles that you get after quantizing the theory.

But let’s continue to work out the classical theory. All we’ve really done so far is define it. Next we want to figure out its equation of motion by applying the principle of least action, very similarly to what we did for a particle. We start with some field configuration $ϕ(x,t)$ , and then we make a little variation of it,

$$
ϕ(x,t)→ϕ(x,t)+ε(x,t),
$$

where $ε(x,t)$ is an infinitesimal field that deforms $ϕ$ a little bit. If $ϕ$ is going to be a stationary configuration of the action, then $S$ had better not change to first order in $ε$ when we make any such variation.

Let’s first work out the change in $L$ . In the first term, we take the derivative and get $1c2∂ϕ∂t$ , and then we multiply that by the change in $∂ϕ∂t$ , which is $∂ε∂t.$ Likewise, in the second term we get $∂ϕ∂x$ times $∂ε∂x$ , and in the last term we get $κ2ϕ$ times $ε$ :

$$
dL=1c2∂ϕ∂t∂ε∂t−∂ϕ∂x∂ε∂x−κ2ϕε.
$$

Just like before, we’ll integrate by parts, only now we have to do it twice:

$$
dL=−1c2∂2ϕ∂t2ε+∂2ϕ∂x2ε−κ2ϕε+∂∂t(1c2∂ϕ∂tε)−∂∂x(∂ϕ∂xε).
$$

Once again, the derivative terms are going to disappear when we integrate this over space and time to get the change in the action. The $t$ derivative term vanishes because we fix the configurations of the field at $ti$ and $tf$ , and so we only want to consider variations that preserve those boundary conditions. And the $x$ derivative term vanishes because we’re integrating it over all of space, and we also require $ε$ to go to zero at spatial infinity so that it doesn’t change the asymptotic behavior of the field.

And so, the leading change in the action when we make a small variation of the field configuration is

$$
dS=−∫titfdt∫dx(1c2∂2ϕ∂t2−∂2ϕ∂x2+κ2ϕ)ε(x,t).
$$

And finally, since we require this to vanish for any suitable variation $ε(x,t)$ , we conclude that in order for a field configuration $ϕ(x,t)$ to extremize the action, it has to satisfy

$$
−1c2∂2ϕ∂t2+∂2ϕ∂x2=κ2ϕ.
$$

This is the **Klein-Gordon equation**. It’s quite famous. It’s a generalization of the wave equation, since if you set $κ=0$ it becomes the equation of a wave traveling at the speed of light.

Since the Klein-Gordon equation is so similar to the wave equation, let’s try solving it by plugging in a simple wave:

$$
ϕ(x,t)=Acos⁡(kx−ωt).
$$

where $A$ , $k$ , and $ω$ are constants; the amplitude, wave number, and angular frequency of the wave. We want to see if we can choose them so that this guess actually solves the equation.

Actually, it’s a huge pain in the neck to deal with cosines and sines, so it’s much more convenient to work with complex exponentials:

$$
ϕ(x,t)=Aei(kx−ωt).
$$

At the end of the day you can just pick out the real part to get a real solution, remembering that $eiθ=cos⁡θ+isin⁡θ.$ These solutions are called **plane waves**, because the profile is constant in the $yz$ plane that’s perpendicular to the direction of motion along $x$ .

But again, this is just a guess. Let’s see what happens when we actually plug it into the Klein-Gordon equation. We get

$$
∂∂xϕ=ikϕ⟹∂2∂x2ϕ=−k2ϕ.
$$

Similarly,

$$
∂2∂t2ϕ=−ω2ϕ.
$$

Thus, the Klein-Gordon equation evaluated on this guess becomes

$$
ω2c2ϕ−k2ϕ=κ2ϕ.
$$

If we cross out the common factors of $ϕ$ , we find that we’ll indeed get a solution to the Klein-Gordon equation as long as the parameters $k$ and $ω$ are related by

$$
ω2c2−k2=κ2.
$$

These plane wave solutions are very simple and special. But the beauty of them is that the *general* solution to the Klein-Gordon equation may be written as a sum of plane waves over all possible values of $k$ .

In the quantum theory, each plane wave is identified with the wavefunction,

$$
ψ(x,t)∝ei(px−Et)/ℏ,
$$

of a single particle with momentum $p=ℏk$ and energy $E=ℏω$ . The condition relating $k$ and $ω$ then implies that $p$ and $E$ have to satisfy

$$
E2c2−p2=ℏ2κ2
$$

or, rearranging,

$$
E=(ℏκc)2c4+p2c2.
$$

That might look familiar! It’s the relativistic formula for the energy of a particle of mass $m$ and momentum $p$ :

$$
E=m2c4+p2c2
$$

where

$$
m=ℏκc
$$

like I mentioned before. When $p=0$ , this is the famous $E=mc2$ —the relativistic rest energy of a particle.

Speaking of relativity, the Klein-Gordon theory is totally compatible with special relativity, though it’s not totally obvious at first sight. But we can make it obvious by introducing some better notation, like you might have seen before if you’ve studied some special relativity. We combine the position coordinates $(x,y,z)$ and the time coordinate $t$ into a four component *spacetime* coordinate,

$$
Xμ=(X0X1X2X3)=(ctxyz).
$$

We include the factor of $c$ in $X0=ct$ so that all the components have the same dimensions of length. The derivatives with respect to $Xμ$ are therefore given by

$$
∂∂Xμ=(∂∂X0∂∂X1∂∂X2∂∂X3)=(1c∂∂t∂∂x∂∂y∂∂z).
$$

Next, let’s define a $4×4$ matrix $η$ with components

$$
ημν=(−1000010000100001).
$$

It’s very simple, as far as matrices go. The “time” component is $η00=−1$ , the “space” components $η11=η22=η33=1$ are all one, and all the other components are zero. $η$ is called the **Minkowski metric**, and it’s what tells us how to measure distances in spacetime, like I explained in the lessons on the action in [special](https://www.physicswithelliot.com/special-relativity-action-mini-notes) and [general](https://www.physicswithelliot.com/gr-action-mini-notes) relativity.

For present purposes, $η$ is useful because it lets us sum up the *pairs* of spacetime derivatives in the Klein-Gordon equation like so:

$$
∑μ,ν=03ημν∂∂Xμ∂∂Xν=η00∂∂X0∂∂X0+η11∂∂X1∂∂X1+⋯=−1c2∂2∂t2+∂2∂x2+⋯,
$$

where the $⋯$ are the $y$ and $z$ terms.

These are exactly the derivatives on the left-hand-side of the Klein-Gordon equation! So we can write it as

$$
∑μ,ν=03ημν∂∂Xμ∂∂Xνϕ=κ2ϕ.
$$

This equation is compatible with relativity because the $μ$ and $ν$ indices in the derivatives are paired up with the metric $ημν$ , and because $ϕ$ itself is a scalar. It's analogous to saying that the length-squared of a vector, $|V|2=V⋅V=∑i=13ViVi=∑i,j=13IijViVj$ is invariant under rotations in space, where $Iij$ is the $3×3$ identity matrix. $∑μ,ν=03ημν∂∂Xμ∂∂Xνϕ$ is invariant under rotations in *spacetime*, which are the symmetries of a relativistic theory.

This relativistic combination of second derivatives is called the **d’Alembertian** operator, and it’s often written simply as $∂2$ or $◻$ . And so you’ll often see the Klein-Gordon equation written even more compactly as

$$
◻ϕ=κ2ϕ.
$$

We can also use this relativistic notation in the Klein-Gordon Lagrangian that we started with, to write

$$
L=−12(∑μ,νημν∂ϕ∂Xμ∂ϕ∂Xν+κ2ϕ2),
$$

or, more simply

$$
L=−12(∂ϕ)2−12κ2ϕ2.
$$

Phew! That was a very rapid tour of the simplest example of a relativistic field theory, and it’s the best place to start learning field theory. Like I mentioned, in *quantum* field theory the counterpart of this Klein-Gordon system describes the physics of spin 0 particles—where the **spin** refers to how the particles and fields transform under the symmetries of spacetime. Most of the elementary particles of nature are *not* spin 0, however. The only spin 0 particle in the standard model of particle physics is the Higgs boson, which was finally discovered at the Large Hadron Collider in 2012, after its theoretical prediction almost 50 years earlier.

The more familiar particles have different spins, like electrons with spin $1/2$ and photons with spin 1. These are described by their own fields, with different Lagrangians and equations of motion. Spin 1/2 fields are described by the **Dirac** **Lagrangian**,

$$
L=i∑μΨ¯γμ∂∂xμΨ−mΨ¯Ψ,
$$

whose equation of motion is the **Dirac equation**

$$
i∑μγμ∂∂xμΨ=mΨ.
$$

Spin 1 fields like the photon are described by the **Maxwell Lagrangian**

$$
L=−14∑μ,νFμνFμν,
$$

whose equations of motion are **Maxwell’s equations**

$$
∑ν∂∂xνFμν=0,
$$

which you’ll learn about in a college class on electromagnetism—though probably using notation that makes them look much uglier! I won’t go into detail about these other Lagrangians and field equations right now; I just want to give you a sense of the lay of the land of field theories.

Finally, coming back to where we started at the beginning, gravity is described by a spin 2 field with the **Einstein-Hilbert Lagrangian**

$$
L=116πG∑μ,νgμνRμν
$$

whose equations of motion are **Einstein’s equations**

$$
Rμν=0.
$$

I hope to tell you more about these field theories in future lessons!

---

See also:

- [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [The Special Relativistic Action](https://www.physicswithelliot.com/special-relativity-action-mini-notes)
- [The General Relativistic Action](https://www.physicswithelliot.com/gr-action-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).