---
date: "2025-08-10T22:06:25+08:00"
url: "https://www.physicswithelliot.com/wavefunction-mini-notes"
status:
---
## Origins of the Quantum Wavefunction

![](https://www.youtube.com/watch?v=Se-CpexiJLQ)

## Introduction

When you start out studying physics, you learn about the motion of things like baseballs and pendulums and even planets. All that falls into the category of classical mechanics. And our basic job in classical mechanics is to figure out the position of a particle as a function of time, or in other words its trajectory $x(t)$ .

![[Read It Later/attachments/0b9f44e2edb0e20e196f636432b84999_MD5.png]]

About a hundred years ago, though, people discovered that the physics of tiny objects—like atoms and protons and electrons—is very different. They’re instead described by *quantum* mechanics. And quantum mechanical particles hardly behave at all the same as classical objects like baseballs.

For example, we’ll discover shortly that a particle like an electron doesn’t follow a single, well-defined trajectory when it travels between two points. Instead, it’s described by a **wavefunction** $ψ(x,t)$ , which is a function that’s spread out through space and which determines the probability of where we’d find the particle when we go to measure its position.

We’ll see in this lesson how that language of wavefunctions comes about by investigating a very simple setup called the double-slit experiment.

![[Read It Later/attachments/1bfd7dbc87ae1243aaa5a4b67b50ad87_MD5.png]]

The idea is basically to throw different things at a wall with two little holes cut into it and see what comes out on the other side. What we find will depend on whether we were throwing classical particles, classical waves, or quantum particles.

And what we’ll discover is that the quantum case exhibits a sort of mixture of the properties of classical particles and waves. That’s what textbooks sometimes give the fancy name “wave-particle duality.” But we’ll see how the consequences of this experiment lead us to the idea of the wavefunction, and how we’re supposed to interpret it.

You might wonder, though, if there’s a different way of approaching quantum mechanics that still describes things in terms of regular old particle trajectories, as opposed to this more abstract language of wavefunctions.

In fact, there is. It’s called the **path integral formulation** of quantum mechanics, and it was invented by Richard Feynman a couple of decades after Schrödinger and friends first worked out the wavefunction approach. The catch is, instead of following a single trajectory like in classical mechanics, a quantum particle does a kind of statistical average of every trajectory it could conceivably take between two points.

![[Read It Later/attachments/ca33e2b38a56155e9b7039d579cf0469_MD5.png]]

But [more on that later](https://www.physicswithelliot.com/path-integral-mini-notes). This is the first of a [series of lessons](https://www.physicswithelliot.com/qm-sequence) explaining Feynman’s way of looking at quantum mechanics, which provides an incredibly powerful intuition for understanding the way physics works at microscopic scales.

For now though, we need to start with the basics, and uncover how all this weirdness with probabilities and wave-particle duality comes about when we study the behavior of really tiny things.

## The Double-Slit Experiment

The setup for the double-slit experiment is a solid wall with two holes, or slits, cut into it. Again, what we're going to do is throw different things at the wall and see what comes out on the other side.

### Classical Particles

Let’s start with classical particles. So we’re going to forget all about quantum mechanics and just suppose that we shoot something like BB gun pellets at the wall, let’s say.

A lot of the pellets will hit the wall and bounce backwards, but some of them will get through one hole or the other. We'll keep track of where they end up by putting a backstop behind the barrier. It’s made of clay or something, so that when the pellets hit it they get stuck, and that way we can count how many hit and where.

If we only have the left hole open and the right one is closed up, and we make a histogram recording where each of the pellets hits the backstop, we’d expect to get a distribution that looks something like this, with most of the pellets hitting in the region behind the left hole:

[[Read It Later/attachments/a7ad4a3e54ec8c799e4583a8b19e2d1e_MD5.png|Open: a7ad4a3e54ec8c799e4583a8b19e2d1e_MD5.png]]
![[Read It Later/attachments/a7ad4a3e54ec8c799e4583a8b19e2d1e_MD5.png]]

Likewise, if we close up the left hole and only open up the right one, we’d see a similar distribution behind the right hole.

And of course when we open up both holes, the total distribution will look like the sum of those two individual distributions, because each pellet either goes through one hole or the other:

[[Read It Later/attachments/73af0f7858919de7f7a880346eee527a_MD5.png|Open: 73af0f7858919de7f7a880346eee527a_MD5.png]]
![[Read It Later/attachments/73af0f7858919de7f7a880346eee527a_MD5.png]]

There’s nothing mysterious going on here so far; we’re just talking about the regular old classical motion of these little pellets.

### Classical Waves

But now let’s suppose that instead of firing BBs at the wall, we send in waves instead. For example, say we shine a laser beam at the barrier. (With the holes resized appropriately, of course.)

[[Read It Later/attachments/e6ddfd5db49b40c5f3b6d755e91fad58_MD5.png|Open: e6ddfd5db49b40c5f3b6d755e91fad58_MD5.png]]
![[Read It Later/attachments/e6ddfd5db49b40c5f3b6d755e91fad58_MD5.png]]

We’re still in the realm of classical physics here, but this is a more interesting problem now because the waves coming out of the two holes will *interfere* with one another and produce what’s called an **interference pattern** (or **diffraction pattern**) on the back screen.

If we close up the right hole again and look at the intensity of the outgoing light on the observation screen, the shape will look fairly similar to what we drew a second ago for the BB pellets. And correspondingly, when you look at the screen you’ll see a band of light with that profile. Let’s call that $I1$ , the intensity of the light with only hole 1 open.

[[Read It Later/attachments/40920a4bf9dcf51c026979c5ae0fc9cb_MD5.png|Open: 40920a4bf9dcf51c026979c5ae0fc9cb_MD5.png]]
![[Read It Later/attachments/40920a4bf9dcf51c026979c5ae0fc9cb_MD5.png]]

Likewise if we close up that hole and open the other one, we’ll get a similar pattern $I2$ that’s shifted over slightly behind hole 2.

There are two key differences here compared to the BB pellets, though. First, there’s the obvious difference: the BBs were discrete particles. Each of them hit the backstop as individual lumps. The laser light, by contrast, is a wave—classically, anyway. It’s a *continuous* distribution of energy and momentum.

The second key difference comes when we open both holes. If light behaved like the BB pellets, we could just add together the two curves to find the total intensity we should get with both holes open, $I12=?I1+I2$ . And if that were true, the image on the back wall would be a wide band of light:

[[Read It Later/attachments/99ca587580fa888c1b99f5c4e17b76a1_MD5.png|Open: 99ca587580fa888c1b99f5c4e17b76a1_MD5.png]]
![[Read It Later/attachments/99ca587580fa888c1b99f5c4e17b76a1_MD5.png]]

But that’s not what you’ll see when you shine a laser beam on a pair of narrow slits. Instead, you’ll see an image with many little fringes of light separated by intervals of near total darkness:

[[Read It Later/attachments/193dcc42e3cd5571008559252cdaf6ac_MD5.jpg|Open: 193dcc42e3cd5571008559252cdaf6ac_MD5.jpg]]
![[Read It Later/attachments/193dcc42e3cd5571008559252cdaf6ac_MD5.jpg]] 
Source: \[Wikipedia\](https://en.wikipedia.org/wiki/Double-slit\_experiment#/media/File:Single\_slit\_and\_double\_slit2.jpg)

And that’s what we call an interference pattern.

The corresponding intensity curve with both holes open would have many alternating peaks and valleys corresponding to the bright and dark spots on the screen:

[[Read It Later/attachments/c49f7216980de5da9903eab2918f8cd6_MD5.png|Open: c49f7216980de5da9903eab2918f8cd6_MD5.png]]
![[Read It Later/attachments/c49f7216980de5da9903eab2918f8cd6_MD5.png]]

Clearly, it’s *not* simply the sum of the intensities $I1$ and $I2$ that we had when the individual holes were open, $I12≠I1+I2$ .

We call it an interference pattern because it arises from the two waves emanating from the holes interfering with one another. The bright spots appear where the waves interfere constructively, meaning that they've added together to make a bigger wave, and the dark spots are where the interference is destructive and the two waves have canceled each other out.

The physics going on here is absolutely fascinating. Take the dark spot on the screen that I’ve indicated with an arrow in the picture. With just one hole open, there was plenty of brightness all throughout that region, like in the earlier picture where the right hole was closed. But by opening up a second hole in the barrier and letting *more* light through, this spot that had been bright now gets dark. It’s kind of mind-bending, and we haven’t even gotten to quantum mechanics yet.

Indeed, the reason we’re talking about all this right now is that we’re about to see a very similar interference phenomenon in quantum mechanics. And so before we get there, let’s understand a little more about how this interference pattern comes about for classical waves.

To keep things simple, we’ll suppose that the gaps in the barrier are very narrow. That way, after the incoming plane wave $ψinc$ strikes the barrier, it breaks up into two *spherical* waves $ψ1$ and $ψ2$ . Then those spherical waves travel along until we intercept them far away on the observation screen.

![[Read It Later/attachments/5a67736ca13fd49525002c5470876088_MD5.png]]

The total outgoing wave is the sum of those two spherical waves. But because the holes in the barrier are separated a little bit apart, the two waves have to travel slightly different distances to arrive at the observation screen—call them $r1$ and $r2$ .

Right in the middle of the screen, $r1$ and $r2$ are the same, so the two waves arrive perfectly in sync, and they combine together constructively to make a bright spot.

Away from the middle, though, $r1$ and $r2$ will be different. Then the waves won’t necessarily be synced up when they arrive. One might be positive while the other is negative, and they can cancel each other out destructively. That’s what produces the dark spots.

But any time the extra distance $r1−r2$ that one wave has to travel comes out to a multiple of the wavelength $λ$ , the waves will sync up again, and we’ll get another bright spot. That’s why we see an alternating pattern of light and dark fringes.

Let’s put some equations to all this. We can write the incoming wave as

$$
ψinc(y,t)=Acos⁡ϕ(y,t).
$$

Here, $A$ is the amplitude of the wave and $ϕ(y,t)$ is the phase, which is a function of the vertical coordinate $y$ and the time $t$ given by

$$
ϕ(y,t)=2πλ(y−vt).
$$

This is the standard sort of form for a wave of wavelength $λ$ that’s traveling along in the $y$ direction at speed $v$ . If we draw it at a fixed instant in time, $λ$ is telling us how far apart the successive peaks are, and $A$ tells us how tall they are:

[[Read It Later/attachments/c4d2a3fbf9965d4bbd88d7e98ebf78fa_MD5.png|Open: c4d2a3fbf9965d4bbd88d7e98ebf78fa_MD5.png]]
![[Read It Later/attachments/c4d2a3fbf9965d4bbd88d7e98ebf78fa_MD5.png]]

In the case of light, $λ$ and $A$ would correspond to the color and brightness of the laser. Of course, a light wave is actually built up of electric and magnetic fields, which are vectors, but it’s enough to think about a simple scalar wave like this to illustrate the origin of the interference pattern.

Actually, if you’ve studied waves at all before, you might know that it can quickly become a bit of a pain to write things in terms of cosines like this. It’s much more convenient to write down a *complex* wave,

$$
ψinc=Aeiϕ(y,t).
$$

The idea here is that we’re using Euler’s identity,

$$
eiϕ=cos⁡ϕ+isin⁡ϕ.
$$

And so we can think of our original cosine wave as the real part of this complex wave:

$$
Acos⁡ϕ=Real part(Aeiϕ).
$$

The reason for doing this is that exponentials are much more convenient to work with than cosines, so this is a useful trick for dealing with classical waves. And it will be essential when we turn to quantum mechanics in a minute.

Meanwhile, on the opposite side of the barrier, we can write the outgoing waves in a similar way. But because those are spherical waves, they don’t vary just with the vertical coordinate $y$ anymore, but rather with the radial distances $r1$ and $r2$ from each hole:

$$
ψ1(r1,t)∝Aeiϕ(r1,t),ψ2(r2,t)∝Aeiϕ(r2,t).
$$

(I’m writing $∝$ instead of $=$ here because the spherical waves also fall off with a factor of $1r$ , but that won’t be important for the shape of the interference pattern in the limit that we’re interested in.)

The total outgoing wave is given by the sum of these two contributions,

$$
ψout=ψ1+ψ2.
$$

Finally, the thing we’re actually looking for is the **intensity** of the outgoing wave, which is what tells us how much energy is hitting the observation screen on average. That's a real number, of course, so we'll take the modulus of the complex wave, $|ψ1+ψ2|.$ And in fact the intensity is given by the square of that absolute value,

$$
I12=|ψ1+ψ2|2.
$$

The reason for the square is analogous to the fact that the kinetic energy of a particle is $12mv2$ rather than $12m|v|$ . For the precise definition of the intensity of an electromagnetic wave, see, for example, chapter 9 of Griffiths' Introduction to Electrodynamics.

We’ll plug in our formulas for the spherical waves and see what comes out in a second. But the algebra isn’t too important right now. The main thing I want you to take away from all this is that we obtained the total intensity by adding together the complex waves emanating from each hole, and then taking the modulus of that squared:

$$
I12∝|eiϕ(r1,t)+eiϕ(r2,t)|2.
$$

There are two terms in the sum because we assumed that each hole in the barrier was really tiny, so that one spherical wave emerged from each.

But here are the details. The total outgoing wave is

$$
ψout=Aei2πλ(r1−vt)+Aei2πλ(r2−vt),
$$

or, simplifying that a little bit,

$$
ψout=Ae−i2πλvt(ei2πλr1+ei2πλr2).
$$

And now to get the intensity, we take this formula and multiply it by its complex conjugate:

$$
I12=A2(ei2πλr1+ei2πλr2)(e−i2πλr1+e−i2πλr2).
$$

Expanding things out and using Euler’s identity to simplify, we get

$$
I12=4A2cos2⁡(πλ(r1−r2)).
$$

[[Read It Later/attachments/b313008112feadc01c01b47850dd2201_MD5.png|Open: b313008112feadc01c01b47850dd2201_MD5.png]]
![[Read It Later/attachments/b313008112feadc01c01b47850dd2201_MD5.png]]

Let's write $s$ for the separation between the holes and $d$ for the distance between the barrier and the observation screen. And let's label the points on the screen by a coordinate $x$ , measured from the center of the screen. Then with a little geometry you can show, approximately, that

$$
r1−r2≈sxd.
$$

To write this approximation, I've assumed that the distance $d$ to the screen is much bigger than the separation $s$ between the holes ( $d≫s$ ) and also much bigger than $x$ ( $d≫x$ ). In other words, we're looking at the light near the middle of a far away screen.

Then the intensity pattern becomes

$$
I12≈4A2cos2⁡(πsxλd),
$$

which is indeed an oscillating pattern of bright and dark fringes along the screen:

[[Read It Later/attachments/632b1998080dee3b19959c8ed36af64b_MD5.png|Open: 632b1998080dee3b19959c8ed36af64b_MD5.png]]
![[Read It Later/attachments/632b1998080dee3b19959c8ed36af64b_MD5.png]]

This is the interference pattern for two point-like holes in the barrier. The more intricate pattern I showed you earlier arises when you account for the fact that in reality the holes will have some finite width to them.

But we can also understand the interference pattern for finite-width holes—or for *any* shaped gap in the barrier—using the same basic strategy. Because whatever shape you want to punch out of the wall—like a wide slit, say—we can build it up by starting with a solid barrier and drilling out lots of little holes:

[[Read It Later/attachments/5af3e1a90c9d8025fc0c3375f70c1c57_MD5.png|Open: 5af3e1a90c9d8025fc0c3375f70c1c57_MD5.png]]
![[Read It Later/attachments/5af3e1a90c9d8025fc0c3375f70c1c57_MD5.png]]

Then each little hole acts as a source for a spherical wave that propagates outward toward the detector, and to construct the interference pattern all we need to do is add up the complex phases from all those individual waves (and square it):

$$
I∼|∑neiϕ(rn,t)|2.
$$

The slick part of this argument is that eventually, we’ll have drilled out *so* many little holes that that whole region of the barrier has disappeared entirely and left us with the gap we wanted. This is the idea behind **Huygens' principle**, and we’ll come back to a very similar argument in the next lesson when we discover the origins of Feynman's path integral approach to quantum mechanics.

That gives us enough of an idea of how things work with classical waves. Now it’s time to see how all this connects to quantum mechanics, which is where things are going to start to get a little strange, to say the least.

### Quantum Particles

Let’s run this experiment with the double slit one last time now, but this time by shooting tiny, quantum mechanical particles at the barrier, like electrons, instead of big, classical objects, like BB pellets or classical waves.

With only one hole open at a time, the story is similar to what we saw before. The distribution has a big bump in the region behind the open hole. And moreover, we find that the electrons hit the detector in distinct lumps of energy and momentum. That much is similar to the BB gun pellets. And likewise if we close that hole and open the other one, we’ll get a similar distribution.

Where things start to get weird is when we open both holes at once. If our everyday experience with pellets or baseballs or whatever else is our guide, we would expect that each particle either makes through one hole or the other, and so the two distributions would simply add together, like we drew earlier for the BB pellets. In other words, lots of particles would hit around the middle of the screen, with fewer and fewer hitting as you move away in either direction.

But that’s not what happens. When we fire electrons at the barrier with both holes open, the spots where they hit the backstop look like this:

[[Read It Later/attachments/b58aa68ab283ebe122522cc77b390dcf_MD5.jpg|Open: b58aa68ab283ebe122522cc77b390dcf_MD5.jpg]]
![[Read It Later/attachments/b58aa68ab283ebe122522cc77b390dcf_MD5.jpg]] 

Source: [Hitachi](https://www.hitachi.com/rd/research/materials/quantum/doubleslit/index.html)

There are dense fringes where many electrons hit, separated by gaps where relatively few hit. It’s another interference pattern! And the corresponding distribution is the same sort of oscillating curve we drew earlier.

[[Read It Later/attachments/ac7c1d31c107b1695efa412106953d4d_MD5.png|Open: ac7c1d31c107b1695efa412106953d4d_MD5.png]]
![[Read It Later/attachments/ac7c1d31c107b1695efa412106953d4d_MD5.png]]

This behavior is utterly baffling! Look at the region of the observation screen indicated by the arrow. With just one hole open in the barrier, plenty of electrons will make it through and hit right around there.

Now when we go and reopen up the second hole, you would think that that would simply let more electrons through the barrier, and therefore we’d find at least as many if not more particles hitting that same spot.

But no. By opening up a second hole and letting more particles through, we find that almost *no* electrons hit that spot on the observation screen. It becomes a dead-zone, at the bottom of an interference pattern that we would have expected for waves emanating from these two holes.

But the electrons are not classical waves either! Because again, they always hit the detector in discrete, individual lumps, not at all like a continuous wave.

This is completely at odds with our classical intuition about how particle-like objects should behave. And so we’ll start to try to come up with classical mechanisms to explain what’s going on. For example, you might wonder if the many electrons passing through the apparatus at any given moment are colliding with one another, and it’s those collisions that somehow conspire to produce this intricate interference pattern.

But that won’t cut it. Because we can turn down the power of our electron gun so that *just one particle at a time* is fired at the barrier. And yet, if we wait a while and record where all those isolated particles wind up hitting the detector, we’ll see that over time they build up the same distribution of fringes, matching the interference pattern we got for waves emanating from both slits.

Evidently, each electron is somehow probing both slits at once, and interfering with itself. In particular, an electron does not have a well-defined trajectory in the sense we’re familiar with from classical mechanics. If it did, an electron that’s en route to hole number one and happens to be headed for one of those interference dead spots shouldn’t give a hoot whether hole number 2 is open or not.

But it does. Because again, when only one hole is open lots of particles will hit right around that spot, whereas next to none will arrive there when both holes are open.

The fact that a quantum particle doesn’t follow a well-defined trajectory means that we can’t say for certain where the particle will wind up hitting the detector, even if we know everything there is to know about how the particle was fired at the barrier. All we can predict is the probability of where we’ll find the particle, according to the shape of the interference curve.

## Wave-Particle Duality

We’ve learned two key things from the double-slit experiment.

1. Electrons behave like particles in the sense we’re accustomed to, insofar as they always hit the detector in discrete lumps.
2. But an electron can also behave like a wave in that it exhibits interference.

And by the way, the same actually goes for our laser beam experiment as well. If we turn the intensity of the light way down, we’ll find that what looked like a continuous light wave hitting our detector was actually a stream of individual particles called photons. And if we send one photon through at a time, we’ll once again gradually build up the same interference pattern.

The fact that a quantum particle can exhibit both of these sorts of properties—sometimes like what we classically think of as a particle and sometimes like a classical wave—is what the fancy name “wave-particle duality” refers to. But the fact is, an electron is not a classical particle *or* a classical wave. It’s a *quantum* particle, which is something quite distinct of its own. And however counterintuitive it might seem to us humans, who live out our days playing with baseballs instead of electrons, there’s really no reason to expect a quantum particle to behave the same way.

So, we’ve seen now how the double-slit experiment leads us to the idea of wave-particle duality, however unfamiliar it might feel. But given that this is the way the world works, how do we as physicists describe what’s going on mathematically?

In light of the interference pattern, we introduce a new quantity for each particle that we fire at the barrier, called its **wavefunction**, $ψ(r→,t)$ . Then just like we had for classical waves, after the incoming wavefunction strikes the barrier, it diffracts, and two spherical waves $ψ1$ and $ψ2$ emerge from the holes on the opposite side.

The total outgoing wavefunction is their sum, $ψ1+ψ2$ . And just like before, the modulus of that total wave, squared, $|ψ1+ψ2|2$ , takes the shape of the interference curve.

That’s the “wave” side of wave-particle duality. But again, the thing we actually observe with our detector is always a localized lump on the backstop. And that’s where the particle side comes in.

What the interference curve is telling us in this case is not the intensity or brightness of some laser. It’s the *probability* of where we’ll find the particle when it hits the backstop. And after we’ve fired many, many quantum particles at the barrier, we therefore find that the spots where they end up are distributed according to that probability curve.

But what "wavelength" $λ$ are we supposed to assign to the particle when we write down its wavefunction? We can determine that experimentally by measuring the separation between the peaks of the interference pattern, which is proportional to $λ$ .

The result is called the **de Broglie wavelength**, and if we fired off particles with momentum $p$ , it’s given by

$$
λ=2πℏp,
$$

where $ℏ$ is a number called **Planck’s constant**, which is the fundamental physical constant of quantum mechanics.

In other words, the incoming electrons are described by the wavefunction

$$
ψinc(y,t)=Aeiϕ(y,t),
$$

where $ϕ(y,t)=2πλ(y−v2t)$ , similar to a complex classical wave, except that $λ$ is now given by de Broglie's formula (and $v$ has been replaced by $v/2$ , for reasons related to the difference between the classical wave equation and the quantum Schrödinger equation).

So, in summary, each quantum particle is described by a wavefunction, and the modulus-squared of that quantity tells us the probability of where we’ll find the particle when we go to measure its position,

$$
Prob∝|ψ(x,t)|2,
$$

or more precisely the probability per unit space.

That’s how the wavefunction formulation explains the distribution of particles we observe on the backstop of the double-slit experiment.

Like I mentioned at the beginning, though, there’s another way of looking at all this that lets us describe things in terms of regular old particle trajectories instead of wavefunctions. But as we’ve already seen, the catch is that the particle doesn’t follow any single trajectory anymore—we have to consider paths that pass through each hole in order to understand the interference pattern that we observe.

But now, if we push that further by drilling more holes in the barrier—and, for that matter, adding even more barriers in between— we’re lead to the idea that we actually need to consider *every* possible path that the particle could follow on its way across the gap.

![[Read It Later/attachments/c52a71f827b595546969d08df6e61ee6_MD5.png]]

That’s our first inkling of Feynman’s path integral formulation of quantum mechanics, which is also the most direct way of understanding how all this quantum weirdness connects back to what we observe day to day up here in the classical world. But we’ll take that topic up in [the next lesson](https://www.physicswithelliot.com/path-integral-mini-notes).

---

See also:

- [The Quantum Path Integral, Explained (Quantum Mechanics Part II)](https://www.physicswithelliot.com/path-integral-mini-notes)
- [The Quantum Path Integral, Computed (Quantum Mechanics Part III)](https://www.physicswithelliot.com/path-integral-part-3-mini-notes)
- [Discovering the Fourier Transform Through Quantum Mechanics](https://www.physicswithelliot.com/fourier-mini-notes)
- [The Symmetry at the Heart of Quantum Mechanics](https://www.physicswithelliot.com/ccr-mini-notes)
- [Five Levels for Differential Equations in Physics](https://www.physicswithelliot.com/odes-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).