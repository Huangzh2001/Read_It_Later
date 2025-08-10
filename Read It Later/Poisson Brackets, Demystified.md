---
date: "2025-08-10T22:08:55+08:00"
url: "https://www.physicswithelliot.com/poisson-mini-notes"
status:
---
## Before You Start On Quantum Mechanics, Learn This

![](https://www.youtube.com/watch?v=Nd4b0_vJZUk)

If you've studied some quantum mechanics before, you've likely run into one or both of these key equations,

$$
[x^,p^]=iℏ,dQ^dt=1iℏ[Q^,H^].
$$

The first is called the **canonical commutation relation** between the position operator $x^$ and the momentum operator $p^$ . It's one of the defining equations of quantum mechanics, and it's what leads, for example, to the Heisenberg uncertainty principle that says you can't know the position and momentum of a particle at the same time.

The second is called the **Heisenberg equation of motion** for an operator $Q^$ . This is what tells us how operators in quantum mechanics change with time—it's equivalent to the Schrödinger equation for *states*. $H^$ here is the Hamiltonian operator, and in both of these equations the square brackets stand for the **commutator**, like you might have seen before for matrices: it just means to first act the operators in the forward order and then subtract the reverse order:

$$
[M^,N^]=M^N^−N^M^.
$$

But if you haven't studied much classical [*Hamiltonian* mechanics](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes) before you start on quantum mechanics, then these equations might look particularly out of left-field when you first see them. Not that quantum mechanics isn't still most definitely *strange*, just that most of the equations have close parallels in the much less confusing world of classical mechanics.

In particular, the commutator of operators in quantum mechanics is closely analogous in classical mechanics to what's called a **Poisson bracket.** So in this physics mini lesson I want to tell you a little bit about Poisson brackets, which will hopefully demystify some of these quantum relations—or will at least make them look a little more natural when you do start in on your study of quantum mechanics.

And Poisson brackets aren't just some curiosity of classical physics that only become interesting because of the parallels with their quantum counterparts. They are fascinating objects in their own right, and play a central role in the Hamiltonian formulation of classical mechanics.

So let's say we have a particle of mass $m$ with coordinate $x$ . It's equation of motion—in other words, the $F=ma$ equation—is given by

$$
md2xdt2=−dUdx,
$$

where $U(x)$ is the potential energy function, related to the force by $F=−dUdx.$

The Poisson bracket is going to enable us to rewrite this equation in a very nice way. Let's first of all write down the total energy of the particle:

$$
E=12m(dxdt)2+U(x).
$$

Actually, it's convenient to write this instead in terms of the momentum $p=mdxdt$ of the particle. Then the kinetic energy $12mv2$ can be rewritten $p22m$ , and so we get

$$
H(x,p)=p22m+U(x).
$$

$H(x,p)$ is called the **Hamiltonian** of the system. Notice that I've written it here as a function of $x$ and $p$ . The $xp$ -plane is called the **phase space** of our system, and specifying a point in the phase space tells us what the particle is doing at any given instant. After all, giving the position and momentum of the particle at a particular time is equivalent to giving its position and velocity. And those are the initial conditions that we need in order to solve the equations of motion and determine the subsequent trajectory of the particle as a function of time.

The quantities that we might like to measure about the particle are functions on this space of $x$ and $p$ ; let's denote a generic one by $Q(x,p)$ . For example, we might take $Q=x$ or $Q=p$ to be the position or momentum themselves, or the kinetic energy $Q=p22m$ , or the total energy $Q=H$ .

With all that in mind, I'm now going to write down the definition of the Poisson bracket. It might look like a totally random expression at first, but bear with me; we'll quickly see how useful it is. It's a sort of multiplication that takes two of these functions, $Q1$ and $Q2$ , say, and returns another. And here it is:

$$
{Q1,Q2}=∂Q1∂x∂Q2∂p−∂Q1∂p∂Q2∂x.
$$

I'm using partial $∂$ derivatives here because $Q1(x,p)$ and $Q2(x,p)$ depend on two variables, $x$ and $p$ , in general—the partial derivative symbol just means that we differentiate with respect to each variable separately.

Well, that looks a little odd, so let's quickly get at some specific examples to find out why the heck this thing is useful. Say we let $Q1=p$ be the momentum and $Q2=H$ be the Hamiltonian. Then their Poisson bracket is

$$
{p,H}=∂p∂x∂H∂p−∂p∂p∂H∂x.
$$

Right off the bat, the first term is zero: $p$ and $x$ are independent variables here, and so $∂p∂x=0$ . As for the second term, $∂p∂p$ is of course one, and so this Poisson bracket reduces to

$$
{p,H}=−∂H∂x.
$$

Now if we plug in $H=p22m+U(x)$ on the right-hand-side, then we get $−∂H∂x=−dUdx$ —i.e. the force on the particle! And the force is equal to the rate of change of the momentum, $dpdt=md2xdt2=F=−dUdx.$

Therefore, we learn that the rate of change of the momentum $p$ is equal to its Poisson bracket with the Hamiltonian $H$ :

$$
dpdt={p,H}.
$$

That's a cute way of rewriting Newton's second law. Maybe we're onto something here—or maybe it's just a fluke. Let's check another: what's the Poisson bracket of $x$ with $H$ ?

$$
{x,H}=∂x∂x∂H∂p−∂x∂p∂H∂x.
$$

This time it's the second term that vanishes, because the derivative of $x$ with respect to $p$ is zero. Then the first term is $∂H∂p=pm.$ But from the definition of momentum, $p=mdxdt$ , that's just equal to the rate of change of $x$ !

$$
dxdt={x,H}.
$$

Okay, this isn't looking like a coincidence anymore. So let's consider the Poisson bracket of a general function $Q(x,p)$ with the Hamiltonian. As time goes by, $Q(x(t),p(t))$ will in general be changing because $x(t)$ and $p(t)$ are changing. We can get the rate of change of $Q$ by applying the chain rule:

$$
ddtQ(x(t),p(t))=∂Q∂xdxdt+∂Q∂pdpdt.
$$

In other words, we take the derivative of $Q(x(t),p(t))$ with respect $x$ and multiply that by the rate of change of $x$ , then do the same for the $p$ dependence, and add it all up to get the rate of change of $Q$ with respect to $t$ .

As we already saw above, $dxdt=pm=∂H∂p$ and $dpdt=−dUdx=−∂H∂x.$ Thus, we can equivalently write

$$
dQdt=∂Q∂x∂H∂p−∂Q∂p∂H∂x.
$$

But now notice that the right-hand-side here is precisely the Poisson bracket of $Q$ and $H$ ! So we have discovered that this is a very general relationship: the rate of change of a measurable function $Q$ with respect to time is given by its Poisson bracket with the Hamiltonian:

$$
dQdt={Q,H}.
$$

This is a beautiful result! Notice as a special case, that for a quantity that's *conserved,* $dQdt=0$ and therefore the Poisson bracket of $Q$ and $H$ must vanish. This leads to the *Hamiltonian* version of [Noether's theorem](https://www.physicswithelliot.com/noether-mini-notes) —the connection between symmetries and conservation laws.

But thinking back to where we started a few of minutes ago, the thing that's hopefully jumping out at you is that this is equation is remarkably similar to the Heisenberg equation of motion for a quantum operator!

$$
dQ^dt=1iℏ[Q^,H^].
$$

We're not going to delve too deep into the general rules of quantum mechanics here, but the gist is that functions on the classical phase space like the position $x$ , momentum $p$ , and Hamiltonian $H$ , turn into **operators** acting on the quantum **wavefunction**. That's what the hat's indicate here— $Q^$ is the quantum operator corresponding to the classical function $Q$ . The square brackets, like I mentioned at the top, denote the **commutator** of two operators: $[Q^,H^]=Q^H^−H^Q^$ . The order matters here—these operators are like a generalization of matrices, and when you multiply matrices together you'll get different answers in general if you combine them in the opposite order. And $ℏ$ is **Planck's constant**, which characterizes the strength of quantum effects.

If you've never seen this equation before now, you will when you start studying quantum mechanics. For now I just want you to notice the remarkable parallel to our Poisson bracket equation for the rate of change of the classical function $Q$ . The classical and quantum equations appear to be related simply by replacing the Poisson bracket ${⋅,⋅}$ with the commutator $[⋅,⋅]$ divided by $iℏ$ , and of course simultaneously replacing the classical functions with their quantum operator counterparts:

$$
{⋅,⋅}→1iℏ[⋅,⋅].
$$

This relationship is in fact quite general! Let's look at another example. What is the Poisson bracket of $Q1=x$ and $Q2=p$ ?

$$
{x,p}=∂x∂x∂p∂p−∂x∂p∂p∂x.
$$

The second term is zero and the first term is one, and so we find

$$
{x,p}=1.
$$

Now what happens when we apply our proposed relation and replace the Poisson bracket ${x,p}$ with the commutator $1iℏ[x^,p^]$ ? Multiplying the $iℏ$ to the right-hand-side, we get another famous quantum equation: the canonical commutation relation between position and momentum,

$$
[x^,p^]=iℏ.
$$

Now, I'm not saying that this equation isn't mysterious anymore, but at least now you hopefully appreciate that it, as well as many other equations in quantum mechanics, are closely parallel to much more straightforward equations in classical mechanics! And with a firm grounding in the classical fundamentals, you'll be in a much stronger position to learn all about the weirdness of the quantum world.

---

See also:

- [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)
- [Symmetries & Conservation Laws: A (Physics) Love Story](https://www.physicswithelliot.com/noether-mini-notes)
- [The Hamiltonian Noether Theorem](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).