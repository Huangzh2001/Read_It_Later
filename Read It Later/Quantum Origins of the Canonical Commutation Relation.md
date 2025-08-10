---
date: "2025-08-10T22:08:36+08:00"
url: "https://www.physicswithelliot.com/ccr-mini-notes"
status:
---
## The Symmetry at the Heart of the Canonical Commutation Relation

![](https://www.youtube.com/watch?v=_lz1VfI6Wxk)

The canonical commutation relation between the position operator $x^$ and momentum operator $p^$ is one of the most fundamental equations of quantum mechanics:

$$
[x^,p^]=iℏ.
$$

It’s what implies that you can’t precisely measure the position and momentum of a particle simultaneously. But where does it really come from? In this lesson, I want to explain the quantum origins of this equation based on *symmetry principles*.

Now, the world of quantum mechanics is very different from the classical mechanics that we’re all much more accustomed to. And we can’t *derive* quantum mechanics from classical laws like $F=ma$ . Quite the opposite: it’s quantum mechanics that is the more fundamental theory, and classical mechanics emerges from *it*.

But there are close parallels between many of the equations of quantum and classical mechanics, as I’ve told you about in the [last](https://www.physicswithelliot.com/poisson-mini-notes) couple of [mini-lessons](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes). For example, we’ve seen that the quantum commutator plays a similar role as a classical operation called the Poisson bracket, up to a factor of $iℏ$ :

$$
{⋅,⋅}→1iℏ[⋅,⋅].
$$

In particular, the Poisson bracket of the position $x$ and momentum $p$ in classical mechanics is ${x,p}=1.$ And if we apply the rule to turn this Poisson bracket into a commutator bracket divided by $iℏ$ we indeed get the canonical commutation relation, $[x^,p^]=iℏ.$

But in this lesson I want to do better than just replacing curly brackets with square brackets and declaring voila. I want to show you how the canonical commutation relation emerges from the symmetry principle we [recently discussed](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes): that *momentum is the generator of spatial translations*.

What we showed is that in classical mechanics the momentum defines a transformation that picks up our system and slides it over in space. And if this spatial translation is a symmetry, then the momentum is a conserved quantity.

I’m going to explain the quantum version of that same statement in this lesson, and show you how it essentially defines what we mean by momentum in quantum mechanics, and leads inevitably to the canonical commutation relation. To do that, I’m going to have to start with a whirlwind tour of the basics of quantum mechanics that we’ll need. If you haven’t seen much of it before, things are going to look a little strange, but I still think you’ll get a lot out of it, so stick with me! I’ll be making more lessons in time that flesh out all of these ideas.

In quantum mechanics, the state of a system, like a particle or atom or whatever else, is described by the **state vector** $|ψ⟩$ . $ψ$ is the Greek letter psi, and $|⋅⟩$ is the notation we usually use for vectors in quantum mechanics, called a “ket”. It’s a generalization of an ordinary column vector,

$$
V→=(V1V2⋮).
$$

The state vector $|ψ⟩$ contains all the information we can get about our particle. The things we measure, like its position or momentum, say, correspond to **operators** that act on the state— $x^$ for the position operator and $p^$ for the momentum operator, where I’ll use a hat symbol to indicate the operator corresponding to a given quantity:

$$
Position →x^|ψ⟩,Momentum→p^|ψ⟩.
$$

Whereas the state $|ψ⟩$ was analogous to a column vector, an operator is analogous to a matrix. It acts on a state and gives you a new state, similar to how a matrix can multiply a column vector and give you another vector:

$$
(⋱)(⋮)=(⋮).
$$

You can also act multiple operators on a state, like $x^p^|ψ⟩$ , but in general they don’t *commute* if we switch the order, meaning that $x^p^$ and $p^x^$ do different things. Their failure to commute is quantified by their **commutator**, defined by $[x^,p^]=x^p^−p^x^$ . The goal of this lesson is to show you how symmetry dictates that this particular commutator is just a number, $iℏ$ .

Another operation on regular old vectors that you’re probably familiar with is the dot product (also called the **inner product**), $V→⋅W→$ , which takes two vectors and returns a number. It essentially tells us how much the vectors overlap with each other, at least when one of them is a unit vector. The notation that we use for the analogous operation for two quantum states, $|ψ⟩$ and $|ϕ⟩$ say, is $⟨ϕ|ψ⟩$ . We call the state $|ψ⟩$ a “ket,” and the flipped object $⟨ϕ|$ a “bra,” so that when you put them together as $⟨ϕ|ψ⟩$ you get a bra-ket, or bracket. And yes, that’s a 100 year old physics pun from Paul Dirac, who introduced the notation.

Say we want to find out where the particle is. In general, even if we’re told the state $|ψ⟩$ of the particle, we can’t say for sure where it is until we make a measurement. In fact, the weirdness of quantum mechanics is that the particle typically didn’t even *have* a well-defined position before you measured it. All the state $|ψ⟩$ can tell us is the *probability* of finding the particle at position $x$ , say.

What we can do is define another state vector $|x⟩$ which describes a particle that *is* precisely at position $x$ . Then the probability of finding our particle with its state $|ψ⟩$ at that location is given by taking the bra-ket overlap between the two $⟨x|ψ⟩$ , and then squaring it:

$$
P(x)=|⟨x|ψ⟩|2.
$$

This is the probability of finding the particle at position $x$ . The overlap $⟨x|ψ⟩$ is called the **wavefunction** $ψ(x)$ of the state. So we can alternatively express the probability as $P(x)=|ψ(x)|2$ . Wherever this function is biggest, the more likely you’ll find the particle there when you make your measurement.

For example, the particle might be in a state where it will be found at point A with probability 1/3 or at point B with probability 2/3. We don’t know which value we’ll get until we make the measurement. And before we do measure, the particle isn’t really localized at one or the other. If we set up a bunch of identical copies of the system side-by-side, each in this particular state, and then measure the position of the particle in each, a third of the time you’ll find it at A, and two-thirds of the time you’ll find it at B.

That’s profoundly bizarre, however my aim for right now isn’t to dive into the rabbit hole of what it means to make a measurement in quantum mechanics, but just to tell you this basic fact: when you make a measurement corresponding to an operator like $x^$ , all you can report beforehand if you know the state $|ψ⟩$ are the probabilities of getting various values of the position. Therefore, you can’t in general say where the particle will be, but only the *average* value of where it *might* be. This average is called the **expectation value** of the operator, $x^$ in this case, and it’s given by sandwiching the operator between the bra and ket for the given state, $⟨ψ|x^|ψ⟩$ . This just means to act $x^$ on $|ψ⟩$ , which gives you another vector $x^|ψ⟩$ , and then to take the inner product of that state with $⟨ψ|$ .

Okay, those were the essential elements of quantum mechanics that we need to accomplish the current aim, which again is to explain what it means that momentum is the generator of spatial translation symmetry in quantum mechanics, and then to show how that implies the canonical commutation relation. That’s what we’ll do now.

First of all, what does it mean to have a symmetry in quantum mechanics? Like any other transformation, a symmetry will be represented by an operator, $U^$ say, that acts on the space of quantum states. And if this transformation is to be a symmetry, it had better not change any of our probabilities.

So, let an operator $U^$ act on our state $|ψ⟩$ , and turn it into a new state $U^|ψ⟩$ . Likewise, it turns $|x⟩$ into $U^|x⟩$ and, when we flip that around to make the corresponding bra, it becomes $⟨x|U^†$ , where $U^†$ (pronounced “U dagger”) is called the **adjoint** of $U^.$ Again that’s something you might have encountered before in studying matrices, where to find the adjoint you simply take the transpose of the matrix and then complex conjugate it.

If this transformation is going to be a symmetry, it has to leave our probability function $P(x)=|⟨x|ψ⟩|2$ unchanged. But it sends

$$
⟨x|ψ⟩→⟨x|U^†U^|ψ⟩.
$$

If this is to be invariant, then the operator should satisfy $U^†U^=1$ . In other words, the adjoint of $U^$ should be the same as its inverse, $U^†=U^−1$ , so that when you apply them in sequence you undo the transformation and get 1. Operators that satisfy this special property are called **unitary.**

We therefore learn that if our symmetry transformation is implemented by a unitary operator $U^$ , it will preserve the probability function $P(x)$ for the position $x$ , as well as the probability functions for any other variables, just like we wanted. Most symmetry transformations in quantum mechanics are therefore represented by unitary operators.

Classically, we learned in the [last lesson](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes) that momentum is the generator of spatial translations, meaning that $p$ defines a transformation that shifts the position $x$ of the particle over:

$$
x(λ)=x0+λ.
$$

In quantum mechanics, we’re therefore looking for a symmetry operator $U^(λ)$ whose effect is to shift the position operator $x^$ by $λ$ ,

$$
U^(λ):x^→x^+λ.
$$

To understand how this works, consider how a general transformation changes the expectation value of $x^$ :

$$
⟨ψ|x^|ψ⟩→⟨ψ|U^−1x^U^|ψ⟩.
$$

Notice, that as far as the expectation value is concerned, we can implement the transformation just as well by instead replacing the *operators* by

$$
x^→U^−1x^U^.
$$

Therefore, the translation symmetry we’re looking for is defined by

$$
U^−1(λ)x^U^(λ)=x^+λ.
$$

Now how does the momentum operator factor into all this? $U^(λ)$ defines a translation by $λ$ for any value of this parameter. In particular, we can take $λ$ to be really tiny, so that we’re talking about an infinitesimal shift. When $λ=0$ , we haven’t done anything at all, of course, and so $U^(λ=0)=1.$ Then when we turn on a small value for $λ$ , we’ll get some small transformation that’s only slightly shifted away from the identity operator, and we can write it as

$$
U^(λ)=1−iℏλG^+⋯,
$$

for some other operator $G^$ . The $⋯$ stands for higher powers of $λ$ that only become important when you make it a bigger number. $G^$ is called the quantum **generator** of the symmetry transformation $U^$ , and the factor of $−i/ℏ$ that we pulled out front is a matter of convention. The $ℏ$ ensures $G^$ has the units that we want, and the $i$ ensures that $G^$ itself is real, in an appropriate sense.

Based on our classical experience with momentum being the generator of translations, let’s now *define* the quantum momentum operator $p^$ to be the generator $G^$ of this transformation.

The inverse of this expression just flips the sign, $U^−1(λ)=1+iℏλp^+⋯$ , and so our definition of a spatial translation for small $λ$ becomes

$$
(1+iℏλp^)x^(1−iℏλp^)=x^+λ.
$$

If we multiply out the left-hand-side, we get

$$
x^+iℏλp^x^−iℏλx^p^,
$$

where I’ve dropped the $λ2$ term because we’re taking $λ$ to be infinitesimally small. Then we obtain

$$
x^−iℏλ(x^p^−p^x^)=x^+λ.
$$

Like we defined before, the difference $x^p^−p^x^=[x^,p^]$ is called the commutator of the operators $x^$ and $p^$ . Then simplifying this equation, we find

$$
[x^,p^]=iℏ.
$$

At last then, by defining the momentum operator as the generator of translations and looking at an infinitesimal symmetry, we have discovered the canonical commutation relation!

All this machinery is very general. For example, *time* translation symmetry, which we saw is classically generated by the Hamiltonian, is quantum mechanically described by the unitary transformation

$$
U^(t)=1−iℏtH^+⋯,
$$

where the infinitesimal generator is now defined as $H^$ , the Hamiltonian operator. Under this transformation, an operator like $p^$ transforms as

$$
p^→U^−1(t)p^U^(t),
$$

which, when $t$ is small, becomes

$$
(1+iℏtH^)p^(1−iℏtH^)=p^−iℏt[p^,H^].
$$

Thus, if the quantum momentum is to be constant in time, it must commute with the Hamiltonian operator:

$$
dp^dt=−iℏ[p^,H^]=0.
$$

Meanwhile, we can ask how the Hamiltonian operator transforms under our spatial translation from earlier:

$$
H^→U^−1(λ)H^U^(λ)=H^−iℏλ[H^,p^]+⋯,
$$

and so the Hamiltonian is in turn invariant under spatial translations if it commutes with $p^$ . (I'm using the same symbol $U^$ here to denote the spatial translation and time translation operator, and just letting the argument $λ$ or $t$ indicate which one I mean.)

Thus, the momentum will be constant in time if and only if spatial translations are a symmetry of the Hamiltonian. This is an example of the quantum version of the [Hamiltonian Noether theorem](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes).

If you’re new to quantum mechanics then all this information and notation was probably a little overwhelming, but it will make more and more sense the more you learn! I’ll be posting more lessons diving deeper into what some of the ingredients we talked about here mean, so stay tuned.

---

See also:

- [Demystifying Poisson Brackets](https://www.physicswithelliot.com/poisson-mini-notes)
- [The Hamiltonian Noether Theorem](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes)
- [Noether's Theorem](https://www.physicswithelliot.com/noether-mini-notes)
- [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).