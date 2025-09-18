---
date: "2025-08-10T22:07:36+08:00"
url: "https://www.physicswithelliot.com/fourier-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=W8QZ-yxebFA)

### Introduction

The Fourier transform has a million applications across physics, engineering, pure math, and more. Given a suitable function $ψ(x)$ , it enables us to decompose it as a sum of complex waves, $eikx$ ,

$$
ψ(x)=12π∫−∞∞dk eikxψ^(k),
$$

where the coefficients $ψ^(k)$ are similarly given by

$$
ψ^(k)=12π∫−∞∞dx e−ikxψ(x).
$$

If these formulas are new to you, they probably look a bit formidable! In this lesson, I want to explain what they mean by exploring how they arise in the context of quantum mechanics *—* where $ψ(x)$ is the wavefunction of a quantum particle. Because, as we’ll discover, the Fourier transform plays a critically important role in this subject.

Of course, the Fourier transform was first written down long before the beginnings of quantum mechanics—by Joseph Fourier in the early 1800s. But even if it hadn’t been, the transform still would have inevitably been discovered once we attempted to understand the strange laws of the quantum world. And in this lesson, we’re going to see how the Fourier transform appears so naturally in quantum mechanics, and to use the physics to build up an intuition for what these mathematical expressions mean.

Now, I want you to be able to appreciate all this even if you’re not already terribly familiar with the abstract rules of quantum mechanics. And so for the purposes of this lesson, you’ll mainly need to know two things going in, which we’ll basically take as axioms:

1. A quantum particle is described by its **wavefunction** $ψ(x)$ , which is a function that assigns a number to each point $x$ in space—a complex number, in general—and which tells us the probability of where we’ll find the particle when we go to measure its position. In particular, the probability of finding the particle at position $x$ , within a little window of width $dx$ , is given by the square of the wavefunction, times the little width $dx$ :
	$$
	Prob(x)=|ψ(x)|2dx.
	$$
	$$
	|
	$$
	 The wavefunction will generally also depend on time, but that won’t be important for this lesson.
2. Given a wavefunction, the momentum is described by an *operator* $P$ that acts on the wavefunction by taking its derivative, times an overall factor:
	$$
	Pψ(x)=ℏiddxψ(x).
	$$
	 $ℏ$ here is Planck’s constant, which is the fundamental physical constant of quantum mechanics. And $i=−1$ is the imaginary number. As we’ll see shortly, it’s there to ensure that the numbers we predict when we actually measure the momentum come out to be real—because again the wavefunction $ψ(x)$ itself is in general going to be complex.

We’ll better understand what these formulas mean as we go along. But for the moment, these are the two main facts about quantum mechanics that we need going into this lesson, and now we’re ready to begin to discover how all this is connected to the mathematics of the Fourier transform.

### The Fourier Series

[[Read It Later/attachments/559a284c5006352f2508bc381e6d857c_MD5.png|Open: 559a284c5006352f2508bc381e6d857c_MD5.png]]
![[Read It Later/attachments/559a284c5006352f2508bc381e6d857c_MD5.png]]

To understand the role of the Fourier transform in quantum mechanics, we’re actually going to start off by thinking about a particle living on a *circle* of radius $R$ instead of an infinite line. Living on a circle will make the math a little bit easier to begin with, and then later on we’ll see what happens when we go back to infinite space.

Here’s the difference between living on a circle versus an infinite line: if you start going for a walk, after you’ve traveled a distance of $2πR$ you look around and discover that you’re just back where you originally started!

As far as our quantum mechanics goes, now that any two points $x$ and $x+2πR$ are identified, the key implication is that our wavefunction has to take the same value at each one:

$$
ψ(x)=ψ(x+2πR).
$$

After all, $x$ and $x+2πR$ label the same point in space, so $ψ$ had better be the same when we plug in either coordinate.

In other words, the wavefunction has to be *periodic—* with period $2πR$ —in order for it to define a single-valued function on our circular space.

So, for example, $ψ(x)=x$ *wouldn’t* be allowed here, since when you take a walk over by $2πR$ , the value of the function changes. But if we took something like $ψ(x)=cos⁡(xR)$ we’re golden, because now shifting $x→x+2πR$ leaves the value of the function unchanged:

$$
cos⁡(x+2πRR)=cos⁡(xR+2π)=cos⁡(xR).
$$

Speaking of cosines, the fact that our wavefunction $ψ(x)$ is periodic means that under very general conditions we can expand it as a sum of cosines and sines using a **Fourier series**:

$$
ψ(x)=∑n=0∞Ancos⁡(nxR)+Bnsin⁡(nxR)
$$

This isn’t the Fourier transform yet—that’ll come soon. For now we’re just talking about the ordinary Fourier *series* that lets us expand most any periodic function as a sum of sines and cosines.

For instance, here’s a simple example of a wavefunction for a particle that’s localized in a little window:

[[Read It Later/attachments/05a2af5a272616dc41d2ac8801e668e3_MD5.png|Open: 05a2af5a272616dc41d2ac8801e668e3_MD5.png]]
![[Read It Later/attachments/05a2af5a272616dc41d2ac8801e668e3_MD5.png]]

Inside the window, $ψ(x)$ is just a constant, and so the particle has an equal chance of being found anywhere in that range. But outside, the wavefunction goes to zero, and so we’ll never find the particle there.

We can make this wavefunction periodic simply by demanding that it repeats itself over and over again with period $2πR$ , and that way we can write down its Fourier series. After we add up just a few terms in the sum, it quickly begins to close in on the precise shape of the wavefunction:

[[Read It Later/attachments/c3a3fe23fa769aabdc9ed9574f7af7f7_MD5.png|Open: c3a3fe23fa769aabdc9ed9574f7af7f7_MD5.png]]
![[Read It Later/attachments/c3a3fe23fa769aabdc9ed9574f7af7f7_MD5.png]]

This idea is really powerful, and it’s the foundation of everything we’re going to discuss in this lesson. Each term in the Fourier series is just a simple sinusoidal function—a wave that oscillates up and down forever. But when we add them together, the waves *interfere* with each other—constructively in some places and destructively in others—and the result quickly closes in on the wavefunction.

Here are the first five waves in the Fourier series, whose sum equals the approximation to the wavefunction drawn in the previous picture:

[[Read It Later/attachments/42adee57b946dec8293fffc522a7cf22_MD5.png|Open: 42adee57b946dec8293fffc522a7cf22_MD5.png]]
![[Read It Later/attachments/42adee57b946dec8293fffc522a7cf22_MD5.png]]

Actually, cosines and sines can be a little bit awkward to work with, and so for our purposes here it will be more convenient to write the Fourier series in terms of exponentials. We can do that thanks to **Euler’s identity**, which says that

$$
eiθ=cos⁡θ+isin⁡θ,
$$

and which therefore lets us go back and forth between sines and cosines and exponentials.

That lets us write the Fourier series much more conveniently as

$$
ψ(x)=∑n=−∞∞ψneinx/R.
$$

This is the same expansion, I’ve just rearranged it a bit using Euler’s identity, and now I’m writing the coefficients as $ψn$ . We’re summing over every integer, $n=0,±1,±2,±3,$ and so on.

Let’s take some time to unpack what’s going on here. Each term in the sum is a wave, called a **Fourier wave** or **Fourier mode**, which I’ll write as

$$
einx/R=eikx,
$$

with $k=n/R$ . In particular, it’s a *complex* wave, because Euler’s identity says that

$$
eikx=cos⁡(kx)+isin⁡(kx).
$$

So the real part is the wave $cos⁡(kx)$ , and the imaginary part is $sin⁡(kx)$ —which is the same wave, it’s just shifted over from the cosine by $90∘$ .

For each of these Fourier waves $eikx$ in the sum, this number $k$ is called the **wavenumber** of the wave—it’s analogous to frequency, except that here we’re talking about a wave that’s oscillating in *space*, not time. A big value of $k$ means a wave that’s oscillating very rapidly, and which therefore has a short wavelength. A small value of $k$ means a wave that’s oscillating very slowly, with a long wavelength.

The fact that the sum only includes the special values $k=n/R$ with $n$ an integer is critical here. We’ll come back to the significance of that in a moment, but first we need to appreciate the intimate connection between these Fourier waves and the quantum mechanical momentum operator that we talked about at the beginning.

Let’s see what happens when we apply the momentum operator, $P=ℏiddx$ , to one of our Fourier modes, $eikx$ :

$$
Peikx=ℏiddxeikx.
$$

The derivative will bring down a factor of $ik$ from the exponent, and the $i$ will cancel against the $i$ in the denominator, leaving

$$
Peikx=ℏkeikx.
$$

Something very special has happened here. When we apply the momentum operator to the Fourier mode, we get back the same function $eikx$ multiplied by a constant, $ℏk$ . $eikx$ is called an **eigenfunction** of the momentum operator, and $ℏk$ is called the corresponding **eigenvalue**. When you apply an operator to one of its eigenfunctions, by definition you get back the same function times the eigenvalue.

This is important, because in quantum mechanics the eigenvalues of an operator are the numbers that you can get back when you make a measurement of that quantity. And so when we measure the momentum of a particle whose wavefunction is a pure Fourier wave $eikx$ , the value we’ll find is Planck’s constant $ℏ$ times the wavenumber $k$ .

Notice that those values are real, by the way, as we’d of course expect since we’re talking about a physical measurement here. That’s why we divided by $i$ in the definition of the momentum operator—the $i$ in the denominator cancels against the $i$ that came down with the derivative of $eikx$ .

So these Fourier waves are very special. They’re the eigenfunctions of the momentum operator, and therefore each one describes a state with definite momentum. But in general the total wavefunction *won’t* be described by any single Fourier wave, and therefore it won’t have definite momentum. A general wavefunction will be given by a superposition of many such waves with those special wavenumbers $k=n/R$ . That’s what the Fourier series expressed,

$$
ψ(x)=∑k=n/Rψkeikx,
$$

where the coefficients tell us how much each individual Fourier wave is contributing to the total wavefunction.

(I’ll go back and forth between writing the Fourier series in terms of $n$ and in terms of $k=n/R$ . $ψn$ and $ψk$ refer to the same thing—the coefficient of the term $eikx=einx/R$ in the sum.)

When we go to measure the momentum of our particle, all those wavenumbers $k=nR$ appearing in the Fourier series are fair game, and therefore we can get back any of those potential values $ℏk=ℏnR$ for the momentum. The probability of each possibility is given by the square of its proportion of the total wavefunction,

$$
Prob(p=ℏk)∝|ψk|2.
$$

(I’m writing $∝$ instead of $=$ here just because we need to ensure that all the probabilities add up to a total of one. That means there’ll be an extra constant factor multiplying $|ψk|2$ , but that doesn’t matter right now.)

So that’s why the Fourier series is so closely connected to the momentum of our quantum particle. It tells us which momenta are contributing to the wavefunction, and therefore the probabilities of what we’ll find when we go to measure it.

I’ll explain how to actually compute the coefficients in just a minute, but first we skimmed over a really important point earlier: why are the wavenumbers—and therefore the values of the momentum—only allowed to take these special values $k=n/R$ ?

The reason comes back to the fact that we’ve put our particle on a circular space, where as we discussed the wavefunction has got to be periodic. Meanwhile, our Fourier waves are of course *also* periodic, but the periodicity of the waves has to be compatible with the periodicity of the circular space.

[[Read It Later/attachments/7d210fc934019dafd1b9ff1b1dee5ca9_MD5.png|Open: 7d210fc934019dafd1b9ff1b1dee5ca9_MD5.png]]
![[Read It Later/attachments/7d210fc934019dafd1b9ff1b1dee5ca9_MD5.png]]

In other words, we need to be able to fit a whole number of wavelengths into the circumference of our circle. They’re a little like the standing waves you may have learned about in high school physics when you pin down the two ends of a rope (except that these waves aren’t going to sit still, in general, as time goes on.)

If a whole number of wavelengths *didn’t* fit into the length of the circle, then when you take a walk all the way around and come back to where you started, the value of the wave will have changed, and the function won’t make any sense on our circle.

In particular, when we shift $x→x+2πR$ , corresponding to walking all the way around the circle, $eikx$ transforms as

$$
eikx→eikxe2πikR.
$$

So for arbitrary values of $k$ , that’s not going to be invariant. We only get a wave that’s well-defined on our circle when $e2πikR=1$ . And that’s where the condition that $kR$ has to be an integer, $n$ , comes in, because $e2πin$ is indeed equal to one.

You can see that again from Euler’s identity,

$$
e2πin=cos⁡(2πn)+isin⁡(2πn).
$$

The angles we’ve got here are $0,2π,4π$ and so on, all of which have $cos=1$ and $sin=0$ .

So that’s why the wavenumbers of our Fourier modes are restricted to be of this form, an integer divided by the radius of the circle. And correspondingly, that’s why the momentum of the particle is quantized as $ℏn/R$ .

Abstractly, what the Fourier series means is that the set of all the Fourier waves with these special values of $k$ forms a **basis** for the space of square-integrable functions on a circle. Where square-integrable means that

$$
∫−πRπRdx |ψ(x)|2<∞.
$$

And indeed, since the integral of $|ψ(x)|2$ is the total probability for finding the particle *somewhere* —which we want to be equal to one—the wavefunction will be square-integrable.

To say that the Fourier waves $eikx$ form a basis for this space means that we can expand any wavefunction as a superposition of them, with some appropriate coefficients, and that’s exactly what the Fourier series expresses. But we haven’t actually discussed yet how we’re supposed to figure out those coefficients, and there’s a beautiful trick for getting them.

To see how, we’ll start with the Fourier series again,

$$
ψ(x)=∑n=−∞∞ψneinx/R,
$$

and now multiply each side by $e−imx/R$ for some *other* integer $m$ :

$$
e−imx/Rψ(x)=∑n=−∞∞ψnei(n−m)x/R.
$$

What we’re going to do is integrate both sides of this equation over the circumference of the circle, from $−πR$ to $+πR$ :

$$
∫−πRπRdx e−imx/Rψ(x)=∑n=−∞∞ψn∫−πRπRdx ei(n−m)x/R.
$$

This looks a little complicated, but actually we get something very simple here. On the right-hand-side, we’re doing the integral of $ei(n−m)x/R$ over the circumference of the circle. But like we just discussed, we specifically chose these functions to ensure that a whole number of oscillations fit into this interval.

[[Read It Later/attachments/c25ce61a2e98cc158de5be2769eb1280_MD5.png|Open: c25ce61a2e98cc158de5be2769eb1280_MD5.png]]
![[Read It Later/attachments/c25ce61a2e98cc158de5be2769eb1280_MD5.png]]

Then when we do the integral of a periodic function like this over a whole number of periods, the positive parts where the wave is above the $x$ -axis precisely cancel the negative parts where it’s below, and we get zero!

Or at least, we *usually* get zero. There’s one exception, and that’s when $n$ and $m$ happen to be the same integer. Because in that special case, $n−m$ in the exponent vanishes, and we’re left with the integral of $e0=1$ . And that comes out to the circumference, $2πR$ :

$$
∫−πRπRdx ei(n−m)x/R={2πRn=m0n≠m
$$

So the complicated looking formula with the sum and the integral isn’t actually very complicated at all. Almost all the terms in the sum over $n$ are equal to zero. The only non-zero term is the special one where $n$ happens to coincide with this other integer $m$ that we chose. And so at the end of the day all we’re left with is

$$
∫−πRπRdx e−imx/Rψ(x)=2πRψm.
$$

And now we’ve got our Fourier coefficients! We just divide the $2πR$ over to the other side, and we find that all we need to do to compute each coefficient for a given wavefunction $ψ(x)$ is evaluate this integral

$$
ψn=12πR∫−πRπRdx e−inx/Rψ(x),
$$

where I’ve switched the label back to $n$ like we were using before.

In words, we take the wavefunction $ψ(x)$ , multiply it by the complex conjugate Fourier wave $e−inx/R$ , and then integrate that over the circle. And finally we divide by the circumference, and that gives the Fourier coefficient. Or, in terms of $k$ ,

$$
ψk=12πR∫−πRπRdx e−ikxψ(x),
$$

where again, in a slight abuse of notation, $ψk$ and $ψn$ refer to the same thing: the coefficient of $eikx=einx/R$ in the series.

So for our example of a wavefunction from earlier, you can evaluate those integrals and you’ll get a distribution of Fourier coefficients like this, for the first handful of terms:

[[Read It Later/attachments/6bbe28689ab3af2fde702f5da855844c_MD5.png|Open: 6bbe28689ab3af2fde702f5da855844c_MD5.png]]
![[Read It Later/attachments/6bbe28689ab3af2fde702f5da855844c_MD5.png]]

Each data point here is telling us how much the Fourier wave $eikx$ with that particular value of $k=n/R$ is contributing to the given wavefunction.

### The Fourier Transform

Okay, that was already a lot of information. And now we’re ready to see how what we’ve learned about the quantum mechanics of the Fourier *series* extends to the full-fledged Fourier transform. But first let’s quickly summarize the main things we’ve learned so far.

- First, a quantum mechanical particle is described by a wavefunction $ψ(x)$ , whose square $|ψ(x)|2$ tells us the probability density of finding the particle at position $x$ when we make a measurement,

$$
Prob(x)=|ψ(x)|2dx.
$$

- Second, for a particle that lives on a circle, we can expand the wavefunction as a sum over Fourier waves, $ψ(x)=∑kψkeikx$ , where $k$ is forced to take the discrete values $k=n/R$ for any integer $n$ .
- And third, each individual Fourier wave has definite momentum, $ℏk$ , and the probability of obtaining that value when we make a measurement is determined by that mode’s contribution to the Fourier series, squared:

$$
Prob(p=ℏk)∝|ψk|2.
$$

Notice, though, that there’s a strange sort of asymmetry here between the position and momentum. The particle can be found at any position $x$ along the circular space, while the momentum can only take these discrete values, like $0$ , $ℏ/R$ , $2ℏ/R$ , and so on.

The origin of the discrepancy comes back to making our space a circle. But now we’re prepared to investigate what happens when we go back to studying our particle on the infinite $x$ -axis, and in doing so we’re going to see that the Fourier transform falls out.

We constructed our circle of radius $R$ in the first place by identifying each pair of points on the real line that differed by a multiple of $2πR$ . But now we can go the other way if we like by sending $R$ out to infinity. In that sense, the problem of a particle on a line is just a special limit of a particle on a circle, and in fact we’ve really gotten most of the hard work out of the way already.

So let’s think about what happens in the $R→∞$ limit. First of all, we found that the allowed values for the momentum were

$$
p=ℏnR.
$$

They came in this discrete lattice of points, one for each integer $n$ , separated by $ℏ/R$ . But notice that in the limit $R→∞$ , that separation goes to zero. Then instead of a discrete lattice of possible momenta, we’ll find a continuous line. And therefore the particle in an infinite space can take any value for its momentum, just like it could for its position, eliminating the asymmetry between the two variables.

Now let’s see what happens to our Fourier series in the infinite radius limit. First I’m just going to relabel things a little bit. Let me rewrite the coefficients as

$$
ψk=12πRψ^(k),
$$

where as before $k=n/R$ are the discrete values of the wavenumber. Putting in the $1/R$ will help us keep control over the $R→∞$ limit, and the factor of $2π$ is just a matter of convention. Then the Fourier series is

$$
ψ(x)=∑k=n/R12πRψ^(k)eikx.
$$

And as for the coefficients $ψ^(k)=2πRψk$ , using our earlier result for $ψk$ we have

$$
ψ^(k)=12π∫−πRπRdx e−ikxψ(x).
$$

These are the exact same formulas as before, all I’ve done is change the notation a little bit to make it clearer how we’re going to take the $R→∞$ limit, which we’re now ready to do.

Let’s start with the sum over $k$ . Just like the momentum, our values of $k=n/R$ were originally spaced out on a discrete lattice, separated by $Δk=1R$ . Notice that we also have a $1/R$ in the Fourier series; let’s go ahead and replace that with this spacing $Δk$ :

$$
ψ(x)=∑k=n/RΔk⋅12πψ^(k)eikx.
$$

Now what is this sum telling us to do? It contains this function of $k$ : $12πψ^(k)eikx$ . Here’s a cartoon of what it might look like:

[[Read It Later/attachments/d0419f5effabaa05168187bbf33950aa_MD5.png|Open: d0419f5effabaa05168187bbf33950aa_MD5.png]]
![[Read It Later/attachments/d0419f5effabaa05168187bbf33950aa_MD5.png]]

It’s complex of course, so let’s say this picture is the real part, and you could draw a similar picture of whatever the imaginary part happens to look like.

Then what we’re told to do is take the value of this function at each of these special points $k=n/R$ . Then we multiply that by the width $Δk$ of each interval. That gives us the area of each rectangle aligned at those values of $k$ , as I've drawn above.

Finally, the sum instructs us to add all these areas up.

As we let $R$ get really big, though, the separation $Δk$ is going to zero, and the width of each rectangle is getting very skinny. Then as we add up all the areas of the skinny rectangles between the ever more finely spaced values of $k$ , we obtain the area under the curve.

In other words, in the $R→∞$ limit, the sum over the discrete values $k=n/R$ turns into an integral over the continuous variable $k$ :

$$
∑k=n/RΔk⟶R→∞∫−∞∞dk.
$$

And so the result of the Fourier series in the $R→∞$ limit is

$$
ψ(x)=12π∫−∞∞dk eikxψ^(k).
$$

As for our other formula for the components $ψ^(k)$ , that limit is even simpler. All that changes is that the bounds of the integral $∫−πRπRdx$ now extend out to $±∞$ ,

$$
ψ^(k)=12π∫−∞∞dx e−ikxψ(x).
$$

And there we have it! This pair of formulas defines the **Fourier transform** of the wavefunction, together with the inverse Fourier transform. And we’ve found that it simply emerges from the Fourier *series* for the wavefunction on a circle, in the limit where the circle becomes infinitely large.

But the understanding we developed by studying the quantum mechanics of a particle on a circle gives us a good intuition for understanding the Fourier transform in an infinite space, which I think otherwise might look a little imposing the first time you see it.

Because even though our discrete Fourier series from earlier has turned into an integral, the underlying idea is exactly the same as before. Each Fourier wave $eikx$ represents a state of definite momentum, $ℏk$ . And what we’re doing is writing a general wavefunction $ψ(x)$ as a superposition of these basic waves:

$$
ψ(x)∼∑keikxψ^(k).
$$

The only difference is that we had a discrete sum for a particle on a circle, whereas now we get a continuous integral when we put the particle on a line. That again was because for the circle we had to be able to fit a whole number of wavelengths inside the circumference, and that meant that $k$ could only take the discrete values $n/R$ . Whereas on an infinite line, there’s no constraint on the wavelength, and $k$ can take any value it wants—it’s a continuous parameter.

The coefficients $ψk$ or $ψ^(k)$ simply tell us how much of each individual wave we need to include in the sum in order to reproduce our given wavefunction. We wrote them as $ψk$ (or $ψn$ ) in the circle case because it was just a discrete list of numbers. But in the continuous case it’s a whole function of the continuous variable $k$ , which is why I wrote it as $ψ^(k)$ —and we throw the hat on there just so we don’t get it confused with the original wavefunction.

When it comes to the momentum, since a general wavefunction is going to be a superposition of many different Fourier waves, each with its own momentum $ℏk$ , when we go to measure the momentum of the particle, we can potentially find *any* of those individual values.

All we can predict ahead of time is the probability that we’ll find one value or another when we make a measurement. And as you might guess based on what we’ve discussed so far, the probability of finding $k$ in a little window of width $dk$ , is given by the proportion of that Fourier wave, squared, multiplied by that little width $dk$ :

$$
Prob(p=ℏk)=|ψ^(k)|2dk.
$$

This may sound familiar. In fact, we’ve found a striking parallel with our discussion of the position probability function from earlier: the probability of finding the position of the particle in a little window of width $dx$ around a point $x$ was given by

$$
Prob(x)=|ψ(x)|2dx.
$$

Therefore, whereas $|ψ(x)|2$ tells us the probability density for finding the particle at position $x$ , its Fourier transform squared is the probability density for finding the particle with momentum $ℏk$ .

We call $ψ(x)$ the **position space wavefunction** to emphasize this, and $ψ^(k)$ the **momentum space wavefunction.** They contain the same information about the system, since we can get either one from the other by applying the Fourier transform.

And so we could just as well write the fundamental rules of quantum mechanics in terms of the momentum space wavefunction—it’s just a different way of packaging the information about the state of the particle.

More abstractly, the quantum state is a vector called the **state vector**, denoted by $|ψ⟩$ . And similar to how you can represent an ordinary vector $v→$ in a Cartesian basis, $v→=vxx^+vyy^$ , just as well as you can write it in a polar basis, $v→=vrr^+vθθ^$ , we can likewise represent the state vector $|ψ⟩$ in the **position basis** or the **momentum basis**. $ψ(x)$ and $ψ^(k)$ are simply the components of this same vector in those two bases.

But unpacking all the details of that will have to wait for another lesson.

By the way, to further complete the parallel between position and momentum, it’s common practice in quantum physics to write the momentum space wavefunction as a function of $p$ rather than of $k$ , and to rescale the definition of the Fourier transform by a factor of $ℏ$ in the process:

$$
ψ~(p)=12πℏ∫−∞∞dx e−ipx/ℏψ(x).
$$

Aside from that extra factor of $ℏ$ , all we’ve done here is replace the variable $k$ with $p=ℏk$ :

$$
ψ~(p)=1ℏψ^(k=p/ℏ).
$$

The $ℏ$ is included so that

$$
|ψ^(k)|2dk=|ℏ ψ~(p)|2dpℏ=|ψ~(p)|2dp.
$$

That way, the momentum probability function is $Prob(p)=|ψ~(p)|2dp$ , just as the position probability function is $Prob(x)=|ψ(x)|2dx$ .

On the other hand, it’s also common practice to simply work in units where $ℏ→1$ , and then the distinction between $ψ^$ and $ψ~$ disappears.

Anyway, I think we’d better take a look at a concrete example at this point to get comfortable working with the Fourier transform. And it’s also going to lead us to a sneak peak at the uncertainty principle.

### An Example

Let’s go back to our earlier wavefunction that described a particle localized inside a region of space around the origin, let’s say from $−a$ to $a$ :

[[Read It Later/attachments/66ce7c5ce44548f32e2dec99d918b2ab_MD5.png|Open: 66ce7c5ce44548f32e2dec99d918b2ab_MD5.png]]
![[Read It Later/attachments/66ce7c5ce44548f32e2dec99d918b2ab_MD5.png]]

$$
ψ(x)={12a|x|<a0|x|>a
$$

I’ve set the height to $1/2a$ in order to ensure that the square of the wavefunction has got an area of one underneath it, since that’s the total probability of finding the particle anywhere.

With this wavefunction, the particle has an equal chance of being found at any point between $−a$ and $a$ , and zero probability anywhere else.

Now let’s see what the momentum space wavefunction looks like by taking the Fourier transform:

$$
ψ^(k)=12π∫−∞∞dx e−ikxψ(x).
$$

The integral’s actually not too bad. First of all, we don’t have integrate from $−∞$ to $∞$ because the wavefunction is *zero* everywhere except in the window from $−a$ to $a$ . And within that range, the wavefunction is a constant, $1/2a$ , so we can pull that straight outside of the integral:

$$
ψ^(k)=12π12a∫−aadx e−ikx.
$$

All that’s left is the integral of this exponential:

$$
∫−aadx e−ikx=1−ik(e−ika−eika).
$$

Plugging in Euler’s identity $eika=cos⁡(ka)+isin⁡(ka)$ and $e−ika=cos⁡(ka)−isin⁡(ka)$ , we can simplify that as $sin⁡(ka)$ times $2/k$ .

Then we’re left with

$$
ψ^(k)=1πasin⁡(ka)k.
$$

That’s the Fourier transform of this particular wavefunction $ψ(x)$ :

[[Read It Later/attachments/4cbfd598039755a9889fe70ebfdb2569_MD5.png|Open: 4cbfd598039755a9889fe70ebfdb2569_MD5.png]]
![[Read It Later/attachments/4cbfd598039755a9889fe70ebfdb2569_MD5.png]]

Earlier, when we considered the periodic version of this wavefunction on a circle, the Fourier coefficients were a discrete list of data points. But now that we’ve graduated to an infinite domain, we have to sum over all the continuous values of $k$ along this curve.

It’s oscillatory, because of the factor of $sin⁡(ka)$ , but notice that the amplitude decays because of the factor of $1/k$ . That means that when you go to measure the momentum of the particle, you’re most likely to find it in the window between the first zeros of $ψ^(k)$ , since that’s where $|ψ^(k)|2$ is going to be dominated. Those zeros occur at $k=±πa$ , since that’s where $sin⁡(ka)$ vanishes.

In particular, notice that whereas the position of the particle is guaranteed to be found in a window of radius $a$ around $x=0$ , the momentum is most likely to be found in a window of radius of order $1a$ around $p=0$ .

That’s our first glimpse of the uncertainty principle. To understand it better, let’s consider the two extreme limits: when $a$ is really tiny and when it’s huge.

[[Read It Later/attachments/7d1941532f227bdb3b3ae748e3e8c2a3_MD5.png|Open: 7d1941532f227bdb3b3ae748e3e8c2a3_MD5.png]]
![[Read It Later/attachments/7d1941532f227bdb3b3ae748e3e8c2a3_MD5.png]]

When $a$ is very small, the window in position space where the particle hangs out becomes very narrow—and correspondingly very tall, because remember the total area under the square of the wavefunction is fixed to one.

Then when we go to measure the position of the particle, in this limit we’re guaranteed to find it very close to $x=0$ .

But what about when we measure the momentum? When $a$ is small we can apply the small-angle approximation for $sin⁡(ka)$ , which means that the sine of $ka$ is very nearly equal to $ka$ again. Then the $k$ ’s cancel, and we’re simply left with a constant for the momentum space wavefunction,

$$
ψ^(k)≈aπ.
$$

A *small* constant, because we’re looking at the limit where $a$ itself is very small.

What’s happened is that by shrinking $a$ down so that the position space wavefunction becomes a very narrow spike, the momentum space wavefunction inversely gets stretched out and looks almost flat. It’ll eventually decay away to zero at a big value of $k$ of order $1/a$ , but in between it’s essentially constant over a huge range of wavenumbers.

And that means that when we go to measure the momentum of the particle, we have an equal chance of getting *any* of those values of $k$ , times $ℏ$ , since the probability function is likewise a constant, independent of $k$ .

In other words, by pinning down the location of the particle in space, we haven’t got a *clue* what value we’ll find when we measure the momentum: we could get any number $ℏk$ with equal probability.

You can guess what happens in the opposite limit, when $a$ is very large, meaning that the particle has room to spread out across a big region in position space. Now it’s the *momentum* space wavefunction that develops a very tall spike at $k=0$ , and quickly decays away on either side:

[[Read It Later/attachments/b3fedd0ce76ca955f6dc0a7b33c7505b_MD5.png|Open: b3fedd0ce76ca955f6dc0a7b33c7505b_MD5.png]]
![[Read It Later/attachments/b3fedd0ce76ca955f6dc0a7b33c7505b_MD5.png]]

This time, we can predict the momentum very precisely. But we have no idea what position we’ll find the particle at when we go to measure it.

This is a manifestation of the **uncertainty principle**. The better we can pin down the particle’s position in space, the less we can say about what its momentum will be, and vice-versa—if we know the momentum precisely, the position could be anywhere at all. This is a very general feature at the heart of quantum mechanics, and here we’ve seen how it emerges inevitably from the Fourier transform.

---

See also:

- [The Symmetry at the Heart of the Canonical Commutation Relation](https://www.physicswithelliot.com/ccr-mini-notes)
- [The Math and Physics of Taylor Series](https://www.physicswithelliot.com/taylor-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).