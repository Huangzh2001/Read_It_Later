---
date: "2025-08-10T22:08:45+08:00"
url: "https://www.physicswithelliot.com/hamiltonian-noether-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=uncm8DChdhc)

A couple of lessons ago, we learned about [Noether's theorem](https://www.physicswithelliot.com/noether-mini-notes), one of the most profound results in all of physics, that says that for every continuous symmetry of your Lagrangian there will be a corresponding conservation law. But that's only half the story. To fully appreciate this connection, we need to look at things from the perspective of Hamiltonian mechanics, where the relationship between symmetries and conservation laws takes on its most beautiful form.

In particular, you might have wondered if the connection goes both ways—does a conservation law conversely imply a corresponding symmetry? In the Hamiltonian formulation of Noether's theorem, we'll see that the answer is, quite generally, yes; continuous symmetries and conservation laws go hand-in-hand.

It's hard to overstate the importance of this relationship, both in classical mechanics and in quantum mechanics, where many of the classical results have close quantum analogues. It's a little more mathematically advanced than the Lagrangian version of Noether's theorem—but stick with me, because the payoff is absolutely worth it, and in my opinion it's the most beautiful result in classical mechanics.

Let's think about a particle of mass $m$ moving in one dimension with coordinate $x$ . According to Newton's second law, the rate of change of the particle's momentum is equal to the total force that's acting on it, and the force can alternatively be expressed as minus the slope of the potential energy function,

$$
dpdt=−dUdx.
$$

The momentum here is of course defined as the mass times the velocity of the particle, or in other words

$$
dxdt=pm.
$$

[[Read It Later/attachments/4c21b4d8fd419834d00f078bd336bd77_MD5.png|Open: 4c21b4d8fd419834d00f078bd336bd77_MD5.png]]
![[Read It Later/attachments/4c21b4d8fd419834d00f078bd336bd77_MD5.png]]

We can describe what the particle is doing at any instant in time by giving its position and velocity, or equivalently its position and momentum. Then the state of the particle is specified by a point in the $(x,p)$ plane, which is called the **phase space** of the system. As time goes on, the particle moves around and accelerates, and so the corresponding point in phase space also changes. The curve that's traced out as this point moves around with time is called a **flow** on phase space.

Think of it literally like the flow of a bit of water along the current in a river. We start at some initial point $(x0,p0)$ , and then the equations for $dxdt$ and $dpdt$ tell us how the current carries this point along through the phase space, giving us a curve $(x(t),p(t))$ that we call the flow.

I also showed you in [another recent lesson](https://www.physicswithelliot.com/poisson-mini-notes) that we can rewrite these equations in a very compact way using **Poisson brackets**, which are in turn essential for understanding the parallels of these classical ideas in quantum mechanics. We defined the **Hamiltonian** $H$ , which in simple circumstances is just the total energy, and showed that we could express the equations of the flow as

$$
dxdt={x,H} dpdt={p,H}.
$$

In fact, we proved something more general: that for *any* function $Q(x,p)$ on phase space, its rate of change with time is given by the Poisson bracket with the Hamiltonian,

$$
dQdt={Q,H}.
$$

You can choose any quantity $Q$ that you like here—the position $x$ , the momentum $p$ , the Hamiltonian $H$ , or whatever else—and this formula tells you how it will change as you follow along the flow.

This gives us a simple condition for determining if a quantity $Q$ is conserved: its Poisson bracket with the Hamiltonian must vanish,

$$
dQdt=0⟺{Q,H}=0.
$$

We say that conserved quantities *Poisson commute* with the Hamiltonian.

That tells us how to understand conservation laws in Hamiltonian mechanics. Now the question is how does all this relate back to symmetries? To understand it, we have to break down what the heck it really means, physically, for "a function on phase space to Poisson commute with the Hamiltonian."

The fact is, the mathematical framework of Hamiltonian mechanics in terms of flows on phase space is much more general. The flow equations $dxdt={x,H}$ and $dpdt={p,H}$ determine how the phase space point $(x,p)$ moves around with time. But mathematically, there's nothing particularly special about the Hamiltonian—it's just some function $H(x,p)$ on this space. *Physically*, of course, it's very significant, but my point is that mathematically we can just as well define a flow associated to *any* function, call it $G(x,p)$ , say, on phase space:

$$
dxdλ={x,G} dpdλ={p,G}.
$$

We call the function $G$ the **generator** of the flow that's obtained by solving these equations. I've replaced $t$ with some arbitrary parameter $λ$ here to emphasize that this flow doesn't have anything to do with how things are changing with time, in general. These equations just define some curve in phase space parameterized by $λ$ that's determined by our choice of $G$ .

This is getting a little abstract, so let's quickly get back down to Earth with an example. Again, $G(x,p)$ here can be any function on the $xp$ -plane, and then solving this pair of equations defines a curve $(x(λ),p(λ))$ in the plane. If we choose $G=H$ to be the Hamiltonian, then we just get back our old $F=ma$ equations, and the resulting flow $(x(t),p(t))$ describes how our initial point moves around with time. In the lingo, we say that *the Hamiltonian is the generator of time translations*.

But let's try a different choice: set $G=p$ to the momentum, for example. Then what flow is defined by the corresponding equations,

$$
dxdλ={x,p} dpdλ={p,p},
$$

and more importantly, what is the physical significance of it?

Remember that the Poisson bracket was defined by

$$
{A,B}=∂A∂x∂B∂p−∂A∂p∂B∂x.
$$

Then if we plug in the two brackets that show up on the right-hand-side of our flow equations, we get ${x,p}=1$ and ${p,p}=0$ . So these are actually very simple, as far as differential equations go:

$$
dxdλ=1 dpdλ=0.
$$

Again, picture the flow of a bit of water along the current of a river. We start with some initial point $(x0,p0)$ , and then this pair of equations tells us how the current carries it around as we evolve the parameter $λ$ , $(x(λ),p(λ))$ .

The second equation just says that $p$ is *constant* along the flow: $p(λ)=p0$ . So whatever point $(x0,p0)$ in the $xp$ plane that we started at when $λ=0$ , the $p$ coordinate doesn't change at all.

The first equation, meanwhile, says that $x(λ)$ is a straight line with slope one, $x(λ)=x0+λ.$ So we start at position $x0$ , and then get shifted over by $λ.$

[[Read It Later/attachments/bc35aa409cb33d648fb6a6829bc8b1f2_MD5.png|Open: bc35aa409cb33d648fb6a6829bc8b1f2_MD5.png]]
![[Read It Later/attachments/bc35aa409cb33d648fb6a6829bc8b1f2_MD5.png]]

Therefore, the flow from a starting point $(x0,p0)$ generated by the momentum $G=p$ is given by

$$
x(λ)=x0+λ p(λ)=p0.
$$

The position coordinate $x$ is translated by $λ$ , and the momentum coordinate $p$ doesn't change at all. Then this "flow on phase space generated by $p$ " isn't such an abstract mathematical curiosity after all! It just describes a *spatial translation* that picks up the particle and shifts it over a bit. We say that *momentum is the generator of spatial translations*.

So, in the same way that the Hamiltonian $H$ generates *time* translations, we've learned that the momentum $p$ generates spatial translations. And likewise, when we step up to more than one dimension, the *angular* momentum will generate *rotations*.

But we saw when we learned about Noether's theorem that when these transformations are *symmetries*, they lead to corresponding conservation laws. Time translation invariance leads to energy conservation, space translation invariance to momentum conservation, and rotation invariance to angular momentum conservation.

And now we're ready to bring it home and understand these relationships in Hamiltonian mechanics—and in fact to discover that the connection goes both ways: the symmetry implies a conservation law and the conservation law implies a symmetry.

We've seen that any function $G(x,p)$ defines a flow on phase space, and likewise that the rate of change of any *other* function $Q(x,p)$ *along* that flow is given by

$$
dQdλ={Q,G}.
$$

Now let's go back to $G=H$ , so that this equation says how $Q$ changes with time, and let's pick our quantity $Q=p$ to be the momentum, as a concrete example. Suppose we have a system where the momentum is conserved (which, for a single particle, would require that it's free, but all this of course generalizes to systems with multiple particles in multiple dimensions). Then

$$
dpdt={p,H}=0.
$$

In our fancy new language, we'd say that $p$ is invariant under the flow generated by $H$ . But we've learned that we can just as well consider the flow generated by $p$ : it's simply a spatial translation. And the rate of change of $H$ along the flow generated by $p$ is given by

$$
dHdλ={H,p}.
$$

Poisson brackets are anti-symmetric, meaning that ${A,B}=−{B,A}$ , as you can check from the definition. In particular, if ${p,H}=0$ , as it must be if $p$ is a conserved quantity, then likewise ${H,p}=0.$ Which in turn means that $H$ is invariant under the flow generated by $p!$ In other words, the Hamiltonian is invariant under spatial translations: we have a symmetry!

This is the Hamiltonian version of Noether's theorem: *a quantity $Q$ is conserved if and only if the transformation that it generates is a symmetry of the Hamiltonian.*

That was the punchline, and I think it's a challenging one to wrap your head around the first time you see it, so let me say it again. A quantity $Q$ will be conserved in time if its Poisson bracket with the Hamiltonian vanishes,

$$
dQdt={Q,H}=0.
$$

But there are two ways of interpreting this bracket ${Q,H}$ . First, like we have here: as the rate of change of $Q$ along the flow generated by $H$ . But second, up to a minus sign, ${Q,H}$ is likewise the rate of change of $H$ along the flow generated by $Q$ . So $Q$ will be conserved if and only if the Hamiltonian is invariant under the transformation that $Q$ generates—in other words, if the transformation generated by $Q$ is a symmetry.

In this way, we see that the class of symmetries that we've talked about here (which are a type of transformation called a *canonical* transformation) come in one-to-one correspondence with conservation laws. The key examples are again the connections between spatial translation invariance and momentum conservation, between rotation invariance and angular momentum conservation, and between time translation invariance and energy conservation. In general, the symmetry transformation that we get from a conserved quantity may be more complicated than the transformations we usually consider in the Lagrangian form of Noether's theorem, in that the position and momentum coordinates can get mixed up, though.

I'll wrap up by mentioning a couple of tidbits that we might get to explore more in future lessons. The Poisson bracket is a very special operation, and it defines a mathematical structure called a **Lie algebra** on the set of functions on phase space. Among other properties, that means that the Poisson bracket satisfies the **Jacobi identity**,

$$
{H,{Q1,Q2}}+{Q1,{Q2,H}}+{Q2,{H,Q1}}=0.
$$

$H,Q1,$ and $Q2$ can be any functions on phase space here, but if like the notation suggests we choose $H$ to be the Hamiltonian, and $Q1$ and $Q2$ to be conserved quantities, then the second two terms vanish because ${Q1,H}={Q2,H}=0.$ Then the Jacobi identity implies that ${{Q1,Q2},H}$ also vanishes, and therefore ${Q1,Q2}$ is itself conserved.

Therefore the set of conserved quantities themselves form a Lie algebra called the **symmetry algebra** of the theory. The classic example is the rotation algebra that's generated by the components of the angular momentum,

$$
Lx=ypz−zpy,Ly=zpx−xpz,Lz=xpy−ypx.
$$

Each of these is an example of a function on phase space, and we can determine the flow that each generates just like we saw that the momentum $pj$ generates a translation in $xj$ . $Lj$ , meanwhile, generates a rotation around the $j$ th axis.

Plugging them into the Poisson bracket, you'll find that the angular momentum components obey the symmetry algebra

$$
{Lx,Ly}=Lz {Ly,Lz}=Lx {Lz,Lx}=Ly,
$$

and it's denoted as $so(3)$ (for reasons I won't get into now). It shows up all over the place.

In *quantum* mechanics, I told you in the previous mini-lesson about how the Poisson bracket gets replaced by the operator commutator divided by $iℏ$ ,

$$
{⋅,⋅}→1iℏ[⋅,⋅].
$$

Then our classical condition ${Q,H}=0$ for a quantity to be conserved in time turns into the quantum condition

$$
[Q^,H^]=0,
$$

that the corresponding operator $Q^$ commutes with the Hamiltonian operator $H^.$

Similarly, our classical rotation algebra becomes

$$
[L^x,L^y]=iℏL^z [L^y,L^z]=iℏL^x [L^z,L^x]=iℏL^y.
$$

In a quantum mechanics problem with rotational symmetry, the space of states can be organized in collections known as *representations* of this algebra.

---

See also:

- [Demystifying Poisson Brackets](https://www.physicswithelliot.com/poisson-mini-notes)
- [Noether's Theorem](https://www.physicswithelliot.com/noether-mini-notes)
- [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).