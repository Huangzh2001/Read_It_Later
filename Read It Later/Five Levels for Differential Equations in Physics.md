---
date: "2025-08-10T22:17:16+08:00"
url: "https://www.physicswithelliot.com/odes-help-room-notes"
status:
---
![](https://www.youtube.com/watch?v=0kY3Wpvutfs)

### Introduction

Just about any time you want to solve a problem in physics, you’re going to wind up facing a differential equation. In Newtonian mechanics, that means adding up all the forces on an object, plugging that into $F=ma$ —or better yet,

$$
F=md2xdt2
$$

—and then solving this differential equation for the position as a function of time.

That’s not too hard for the simplest systems we all meet in our first physics classes, but as you study more and more physics, you’ll very quickly discover that the $F=ma$ equation can become extremely difficult to solve, even for setups that look like they should be fairly straightforward at first glance.

That’s because differential equations in general are *really* *hard*. But they’re also essential for understanding physics, because they’re by definition the equations that describe change, and physics is all about figuring out how things change with time.

So it’s hugely important to have a toolkit of strategies for tackling the many differential equations you’re going to meet throughout your physics studies. And that’s why you need to learn the five solution methods I’m going to tell you about in this lesson.

We’ll start off with some relatively basic strategies for solving differential equations, which will already take you a long way with lots of problems you’ll meet in classical mechanics and beyond. These include

1. Solving by making a substitution
2. Using energy conservation

But as we go along, I’m going to introduce you to some more sophisticated techniques, like

1. Using a series expansion to solve the equation
2. Using an integral transform like the Laplace transform
3. Using Hamilton’s equations, which also give us a new way of visualizing the solution as what’s called a flow on phase space.

We’ll see how all these methods work using one of the simplest, but also arguably the most important differential equation in classical mechanics: the equation of a simple harmonic oscillator,

$$
md2xdt2=−kx.
$$

Or, in other words, the $F=ma$ equation for a block attached to a spring.

There’s a good chance you’ve run into this equation before, and maybe you’ve already seen a couple of different ways of solving it. But what’s hopefully going to be fun about this lesson is that the five solution methods we’ll discuss will start from the most straightforward, and work our way up through increasingly advanced approaches.

### The Equation

![](https://www.physicswithelliot.com/s/spring-block.png)

First of all, let me quickly remind you where the simple harmonic oscillator differential equation comes from. Our setup is a block of mass $m$ , sitting on a frictionless table, and hooked up to a spring of stiffness $k$ .

In equilibrium, the spring isn’t stretched or compressed, and the block can sit happily at rest there. Let’s call that position $x=0$ .

But if we slide the block away from there, the spring will now exert a force, $F=−kx$ , trying to pull the block back toward equilibrium. Then the $F=ma$ equation is

$$
md2xdt2=−kx.
$$

Now let’s say we pull the block out to an initial position $x(0)=x0$ and then release it from rest.

The stretched spring pulls the block back toward equilibrium to the left. But then the block overshoots $x=0$ and moves to the left of equilibrium. The spring gets compressed and pushes the block back toward the right. And on and on it goes, making the block oscillate back and forth around equilibrium forever.

This is what we call **simple harmonic motion**. To understand why it plays such an important role in physics, make sure you’ve seen [my earlier lesson](https://www.physicswithelliot.com/oscillator-help-room-notes) about it.

To solve this equation, we’re looking for $x(t)$ —the position of the block as a function of time. And $F=ma$ is a differential equation, because it involves the derivatives of this function. And now we’re ready to start exploring the five methods for solving this equation.

### Method 1: Substituting an Ansatz

It might sound a little silly, but honestly the first thing you can do, especially with a relatively simple looking equation like this one, is to try to *guess* the solution. Except that “guessing” doesn’t sound very sophisticated, so instead you’ll often see textbooks call it making an “ansatz.”

All that means in this case is, we’re going to ask ourselves if we can think of a function, which, when we take its derivative two times, we get back the same function we started with, times some negative number:

$$
d2xdt2=−kmx.
$$

Using our physical intuition that the block is going to oscillate back and forth around equilibrium, functions like sine and cosine might come to mind.

So let’s make an ansatz, and write down a guess of the form

$$
x(t)=Acos⁡(Ωt),
$$

where $A$ and $Ω$ are some constants that we don’t know yet—the idea is to see if we can choose them to solve the equation.

We have to have *some* constants there just to get the units right. $x$ is supposed to a length, in meters, say. That means $A$ had better have units of meters. And inside the parentheses, $Ωt$ had better be measured in radians, which are dimensionless. So $Ω$ has to be something in radians per second in order to cancel out the seconds units from the $t$ .

Let’s substitute this guess into the equation and see if it actually works. The derivative of $cos$ is $−sin$ , and by the chain rule we also need to multiply by the derivative of the thing in parentheses with respect to $t$ , which gives us a factor of $Ω$ :

$$
dxdt=−ΩAsin⁡(Ωt).
$$

Now we do it again for the second derivative. This time, the derivative of $sin$ is $cos$ , and again we get an extra factor of $Ω$ from the chain rule:

$$
d2xdt2=−Ω2Acos⁡(Ωt).
$$

This looks promising, because it says that the second derivative of $x$ is indeed equal to $x$ again, times a constant, $−Ω2$ . Then all we need to do is pick this number $Ω2$ to be the same as the ratio $k/m$ that appeared in the differential equation:

$$
Ω2=km.
$$

And that’ll do it! If we choose this value for $Ω$ , then $x(t)=Acos⁡(Ωt)$ will indeed satisfy the equation.

So, are we done? Well, no. First of all, $sin⁡(Ωt)$ satisfies this property just as well as $cos⁡(Ωt)$ , and so we can add them together to write a general solution of this form:

$$
x(t)=Acos⁡(Ωt)+Bsin⁡(Ωt).
$$

That works because the differential equation is **linear**, meaning that we only have single powers of $x$ and its derivatives showing up.

But what are we supposed to do with these two constants $A$ and $B$ ? This expression solves the equation for *any* values of these numbers.

That brings us to a really important point about solving differential equations. The equation itself is only half the story! We also have to specify the **initial conditions** we want to satisfy in order to get the solution to a problem.

Physically, that makes total sense. When you throw a ball up in the air, we need to know the initial position you’re throwing it from and the initial velocity in order to be able to say what trajectory it will follow. Likewise, we need to know the initial position and velocity of the block in order to say what its position will be after that.

In this case, we released the block from rest at $x0$ , and that means our two initial conditions are

$$
x(0)=x0anddxdt(0)=0.
$$

Mathematically, the fact that we need two initial conditions comes from the fact that the differential equation is second order, meaning that the highest derivative that shows up is the second derivative of $x$ . Basically, we need to integrate the equation twice to go from $d2xdt2$ to $dxdt$ to $x(t)$ , and each of those two integrals comes with an integration constant.

When we plug $t=0$ into the general solution, we get

$$
x(0)=Acos⁡(0)+Bsin⁡(0)=A.
$$

Then we had better set $A=x0$ in order to coincide with the initial position:

$$
x(t)=x0cos⁡(Ωt)+Bsin⁡(Ωt).
$$

As for the initial velocity,

$$
dxdt(0)=−x0Ωsin⁡(0)+BΩcos⁡(0)=BΩ,
$$

and therefore we need to set $B=0$ .

That leaves us with

$$
x(t)=x0cos⁡(Ωt)
$$

where again, $Ω=k/m$ is fixed by the stiffness of the spring and the mass of the block:

x <sub>0</sub> (m) = 0.40

v <sub>0</sub> (m/s) = 0.00

L <sub>eq</sub>

t (s)

x (m)

It looks about like we’d expect. The block starts out at rest at the initial displacement $x0$ , and then when we let it go it oscillates back and forth around equilibrium at $x=0$ , where $Ω$ controls how fast it oscillates.

So there we have it, we’ve solved the differential equation—together with the initial conditions—by substituting in a guess with some constants in it, and seeing how to pick the constants in order to get a solution.

This strategy works in general for a linear equation like this:

$$
ad2xdt2+bdxdt+cx=0,
$$

where $a$ , $b$ , and $c$ are some constants. In general, you’d pick an exponential for your guess, $x(t)=AeΩt$ , substitute it in, and see what conditions come out on $A$ and $Ω$ .

This method is really all you need to solve the simple harmonic oscillator equation—it’s a really simple problem, after all! But as you progress through physics, you’re going to encounter much harder differential equations, and that’s why we’re going to keep going and explore more powerful solution methods in the rest of this lesson.

### Method 2: Energy Conservation

As you’ve hopefully learned before, if we take the kinetic energy of the block, $12m(dxdt)2$ , and add to it the potential energy in the spring, $12kx2$ , we’ll get a constant—the total energy:

$$
E=12m(dxdt)2+12kx2.
$$

That’s not at all obvious, because both $x$ and $dx/dt$ are changing with time as the block slides back and forth. But when we add them together in this special combination, the $t$ ’s drop out, and we get a constant.

The way to check that that’s true is to take the derivative of $E$ with respect to $t$ , and see that it’s equal to zero:

$$
dEdt=0.
$$

Let’s check. The derivative of the kinetic energy with respect to $t$ is $mdxdtd2xdt2$ , where the $mdxdt$ comes from the power rule and the extra factor of $d2xdt2$ comes from the chain rule. The derivative of the potential energy is similarly $kxdxdt$ . Together, we get

$$
dEdt=mdxdtd2xdt2+kxdxdt.
$$

Now pull out the common factor of $dxdt$ :

$$
dEdt=dxdt(md2xdt2+kx).
$$

The factor in parentheses is just the thing that vanishes when $F=ma$ is satisfied! Therefore, $dEdt=0$ along the trajectory of the block, and the energy is indeed a constant.

When we release the block from $x0$ , all of the energy is the potential energy stored in the stretched spring, $U=12kx02$ . There’s no kinetic energy because we’re releasing the block from rest.

Then when we let it go, the block starts to speed up, and the spring starts to relax. By the time it reaches $x=0$ , all the energy is kinetic. And on and on the energy cycles back and forth between kinetic and potential. But the *total* energy never changes—it’s always the same number we started with, $12kx02$ :

$$
12m(dxdt)2+12kx2=12kx02.
$$

And we can use this equation for energy conservation to solve for the trajectory of the block. It’s again a differential equation for $x(t)$ , but notice that it only involves the first derivative of $x(t)$ —not the second derivative that we had in $F=ma$ .

Let’s rearrange the equation to isolate $dxdt$ :

$$
(dxdt)2=km(x02−x2).
$$

I’ll use the same symbol $Ω2$ as before for the ratio $k/m$ . Remember, $Ω$ was what told us how fast the block would oscillate back and forth.

Then we can take the square root to get an equation for $dx/dt$ :

$$
dxdt=Ωx02−x2.
$$

Something really special has happened: this equation tells us the velocity of the block *as a function of its position* $x$ . The point is, if we know the position $x$ of the block, we know how stretched or compressed the spring is, and therefore how much potential energy is stored in it. Then conservation of the total energy tells us how much is left over for the kinetic energy of the block, and therefore how fast it’s moving.

So when the block starts off at $x=x0$ , we get $dxdt=0$ because we released it from rest. But by the time the spring pulls the block back to equilibrium at $x=0$ , it’s sped up to its maximum velocity, and we get $dxdt=Ωx0$ .

Actually, we should really get *minus* that because the block is initially moving to the left. So we ought to be a little more careful when we take the square root, since we can get either sign:

$$
dxdt=±Ωx02−x2.
$$

We take the minus when the block is moving to the left, and the plus when it turns around and goes back to the right.

And now we can solve for $x(t)$ by integrating one more time. Just divide the square root over to the LHS and multiply the $dt$ over to the right in order to separate the variables:

$$
dxx02−x2=±Ω dt.
$$

Next we integrate both sides of this equation:

$$
∫dxx02−x2=±Ω∫dt.
$$

The integral on the right is super easy: we just get $t$ , maybe plus some integration constant $c$ ,

$$
∫dxx02−x2=±Ω(t+c).
$$

The integral over $x$ is a little harder. You can do it with a trig substitution, or of course you can just look it up. It’s given by $−cos−1⁡(xx0)$ :

$$
−cos−1⁡(xx0)=±Ω(t+c).
$$

We could also add another integration constant on the left, but we can just absorb that into the other constant $c$ on the right.

Now we solve for $x$ . Flip the sign, take the cosine of both sides, and move the $x0$ over to the right:

$$
x(t)=x0cos⁡(∓Ω(t+c)).
$$

Cosine doesn’t care if you plug in + or - something—it’s an even function. So we can throw out the $∓$ . And as for the $c$ , remember that when we plug in $t=0$ , we want to get $x(0)=x0$ :

$$
x(0)=x0cos⁡(Ωc).
$$

And so we can just set $c=0$ . Then we at last get

$$
x(t)=x0cos⁡(Ωt),
$$

just like we found with method number one! So conservation of energy also lets us easily get to the solution of our differential equation.

And in fact this strategy can often be successful for harder problems, even when our first method doesn’t work. A great example is the simple pendulum, which is *supposed* to be so simple that it’s in the name, but actually it’s surprisingly tricky:

![](https://www.physicswithelliot.com/s/pendulum-coordinates.png)

The $F=ma$ equation for its coordinate $θ$ , which measures the angle of the pendulum, looks like this:

$$
d2θdt2=−glsin⁡θ.
$$

That’s due to the component of gravity $gsin⁡θ$ that points along the direction of the pendulum’s swinging. For a review of that, see [my lesson](https://www.physicswithelliot.com/pendulum-help-room-notes) all about pendulums.

And yet, this differential equation in general doesn’t have a simple solution for $θ(t)$ ! At least, not in terms of familiar functions like $sin$ ’s, $cos$ ’s, $12gt2$ ’s, and so on.

The reason for the difficulty is the factor of $sin⁡θ$ on the RHS, which makes this a **non-linear** differential equation. Our original harmonic oscillator equation was linear because it only involved single powers of $x$ and its derivatives. By contrast, if you were to expand out $sin⁡(θ)$ in a Taylor series,

$$
sin⁡(θ)=θ−θ33!+θ55!−⋯,
$$

you can see that it involves infinitely many powers of $θ$ , and so this is a non-linear equation.

So we can’t just substitute in a simple cosine function here anymore and expect to get a solution. (Except in the special case when $θ$ is small—again, see the lesson [all about pendulums](https://www.physicswithelliot.com/pendulum-help-room-notes).) But we can still use energy conservation!

With a little geometry, you can write the total energy as

$$
E=12ml2(dθdt)2−mglcos⁡θ.
$$

The first term is the kinetic energy written in terms of $θ$ , and the second term is the gravitational potential energy $mgy$ , where $y=−lcos⁡θ$ is the height of the pendulum below the pivot point.

If we release the pendulum from rest at an angle $θ(0)=θ0$ , then the energy conservation equation says that

$$
12ml2(dθdt)2−mglcos⁡θ=−mglcos⁡θ0.
$$

Once again, we can rearrange this equation to get the velocity $dθdt$ as a function of $θ$ :

$$
dθdt=±2gl(cos⁡θ−cos⁡θ0).
$$

Now we separate the variables and integrate:

$$
∫dθcos⁡θ−cos⁡θ0=±2gl(t+c).
$$

So far so good. At this point, however, the integral on the LHS is considerably harder than the one we saw before for the harmonic oscillator. It’s called an **elliptic integral**, and it doesn’t have a simple answer in terms of something like the $cos−1$ that we had before.

Fortunately, though, mathematicians a couple of centuries ago invested a huge amount of effort studying these kinds of integrals, and so a lot is known about their properties. The solution in this case can be written

$$
θ(t)=2sin−1⁡(sin⁡(θ02) cd(Ωt|sin2⁡(θ02))),
$$

where the devil is in that “ $cd$ ” function, called a [Jacobi elliptic function](https://en.wikipedia.org/wiki/Jacobi_elliptic_functions).

The result looks like a simple cosine function when $θ0$ is small, but for large initial angles it [changes dramatically](https://www.physicswithelliot.com/pendulum-graph).

So, this pendulum example shows how energy conservation can give us a different way to make progress with a challenging, non-linear differential equation, even when our first substitution method fails.

But now let’s get back to the harmonic oscillator equation,

$$
d2xdt2=−Ω2x.
$$

So far, we’ve seen two ways of solving it. And these will more or less do the job for most of the equations you’ll meet in your first mechanics class. But if you’re up for it, what I’d like to do now is show you some more powerful methods that will come in handy later on when you’re faced with harder equations.

### Method 3: Series Expansion

Using a series expansion is probably the most versatile of all the strategies I’ll show you in this lesson, and you can apply it to most any differential equation to get an exact, or even just an approximate solution.

The idea is, whatever the solution $x(t)$ to our differential equation might be, we can almost always expand it as a Taylor series in powers of $t$ —at least within a window where things are well-behaved:

$$
x(t)=a0+a1t+a2t2+a3t3+a4t4+a5t5+⋯.
$$

The question is, how do we figure out what these coefficients are supposed to be?

Let’s start off by imposing our initial conditions. When we plug $t=0$ into the series expansion, all of the $t$ ’s disappear, and we’re left with $x(0)=a0$ . So we want to set $a0=x0$ to coincide with the initial position of the block.

And to impose that the initial velocity is zero, we’ll take the derivative of the series:

$$
dxdt=a1+2a2t+3a3t2+4a4t3+5a5t4+⋯.
$$

Now when we plug in $t=0$ , we’re left with $a1$ , and so we want to set $a1=0$ .

Alright then, so far we’ve figured out $a0$ and $a1$ . But there are still infinitely many coefficients left to determine!

The next thing we need to do is actually plug the expansion into the differential equation,

$$
d2xdt2+Ω2x=0.
$$

We’ll need to take the derivative of the series one more time to get the acceleration:

$$
d2xdt2=2a2+3⋅2a3t+4⋅3a4t2+5⋅4a5t3+⋯.
$$

And now we add on $Ω2x$ and set the whole thing equal to zero. And we can pair up the corresponding terms:

$$
d2xdt2+Ω2x=(2a2+Ω2x0)+(3⋅2a3)t+(4⋅3a4+Ω2a2)t2+(5⋅4a5+Ω2a3)t3+⋯=0.
$$

All this needs to vanish if we want our series to solve the differential equation. And the only way that can happen for every time $t$ is if all the coefficients are separately equal to zero. Then the idea is to go term by term through this sum, and demand that each factor in parentheses is zero.

That second term with a single power of $t$ looks the simplest, so let’s start there. Its coefficient is $3⋅2a3$ . For that to vanish, we need to set $a3=0$ .

But notice that there’s also an $a3$ in the $t3$ term. And once we plug in $a3=0$ there, all that’s left of that coefficient will be $5⋅4a5$ . And so for that to vanish, we’ll also have to set $a5=0$ .

We’ve therefore found that $a1=a3=a5=0$ . And the same thing is going to happen for all of the odd terms. So we conclude that all the odd coefficients are equal to zero.

That’s already pretty nice, because it means we get to throw out half the terms in our expansion,

$$
x(t)=x0+a2t2+a4t4+⋯.
$$

Now on to the even terms. The 0th one says that

$$
2a2+Ω2x0=0,
$$

and so we can solve for $a2$ :

$$
a2=−12Ω2x0.
$$

Next, for the $t2$ term, we have

$$
4⋅3a4+Ω2a2=0.
$$

After plugging in our solution for $a2$ , we can again solve to get $a4$ :

$$
a4=+14!Ω4x0.
$$

We can already see the pattern that’s forming. The first few terms of our series solution are

$$
x(t)=x0−12x0Ω2t2+14!x0Ω4t4+⋯.
$$

Does that look familiar? Let’s simplify it a bit by pulling out the common factor of $x0$ , and we can also put together the $Ω$ ’s and the $t$ ’s like this:

$$
x(t)=x0(1−12(Ωt)2+14!(Ωt)4+⋯).
$$

How about now—does this thing look like the Taylor series for any function you know?

That’s right! The sum in parentheses is just the Taylor series for the cosine! And so, reassuringly, we’ve once again found that

$$
x(t)=x0cos⁡(Ωt).
$$

Series expansions like this are an extremely versatile method for solving all kinds of differential equations. You shouldn’t expect that they’ll always sum up to something simple and pretty like this one, though, unless you happen to be looking at a special differential equation with a simple solution. But even if you can’t sum up the infinite series into a familiar function, that doesn’t make it any less useful or valid as a solution to the equation—as long as you’re looking at a point where the series converges.

### Method 4: Integral Transforms

Let’s keep it going with our next method: using an integral transform to solve a differential equation.

Now, there are lots of kinds of integral transforms out there—including the Fourier transform, which [my last lesson was actually all about](https://www.physicswithelliot.com/fourier-mini-notes) —but the one that’s most useful for solving the problem we’re looking at today is called the **Laplace transform**.

And here’s what it is. The Laplace transform is an instruction to take our position function $x(t)$ , multiply it by $e−st$ with some new variable called $s$ , and then integrate that over $t$ from $0$ all the way to $t=∞$ :

$$
x^(s)=∫0∞dt e−stx(t).
$$

What’s left is a function of $s$ , that I’ll denote by $x^(s)$ .

Okay… well that sounds like a funny thing to do, especially if you’ve never seen it before. But we’ll see in a moment that this transformation has a magical property when it comes to differential equations.

But the way you should think about it, is that we have two “spaces” here: $t$ -space, where our original function $x(t)$ lives, and $s$ -space, where its Laplace transform $x^(s)$ lives.

To give a couple of examples, if $x(t)$ were a constant, like $x(t)=1$ , then it’s just a horizontal line in $t$ -space. And you can show pretty easily that its Laplace transform in $s$ -space, obtained by doing the above integral, is $x^(s)=1s$ :

![](https://www.physicswithelliot.com/s/Laplace-constant.png)

Or, for our block on a spring, we’ve found—and we’re about to find again—that $x(t)=x0cos⁡Ωt$ oscillates in $t$ -space. And in $s$ -space, the result of the integral is a rational function, $x^(s)=x0ss2+Ω2$ :

![](https://www.physicswithelliot.com/s/Laplace-cosine.png)

Alright, so we can do this integral to go from $t$ -space to $s$ -space. But why the heck would we want to do such a thing? How does it help us solve a differential equation like our harmonic oscillator,

$$
d2xdt2=−Ω2x.
$$

The reason is that the Laplace transform acts in a beautifully simple way on derivatives. Look at what happens when we plug $dxdt$ into the Laplace transform integral:

$$
dxdt^(s)=∫0∞dt e−stdxdt.
$$

We can simplify this by integrating by parts. In other words, we’ll use the product rule,

$$
ddt(e−stx)=e−stdxdt−se−stx,
$$

in order to rewrite the integrand as

$$
e−stdxdt=se−stx+ddt(e−stx).
$$

And now we do the integral over $t$ :

$$
dxdt^(s)=∫0∞dt (se−stx+ddt(e−stx)).
$$

The first term here is just $s$ times the Laplace transform of $x(t)$ . After all, $s$ is a constant as far as the integral over $t$ is concerned, and so we can pull it outside the integral to get $sx^(s)$ .

As for the second term, it’s the integral of a derivative, and so we can write down the result immediately:

$$
∫0∞dt ddt(e−stx)=(e−stx(t))|0t=∞.
$$

When we plug in $t=∞$ , $e−st$ goes to zero. ( $s$ has to be a positive number here for the Laplace transform integral to have a chance of making sense in the first place.) Then we’re simply left with $−x(0)$ from the other end of the integral.

And so, we’ve been able to simplify the Laplace transform of $dxdt$ as

$$
dxdt^=sx^(s)−x(0).
$$

This is the property that makes the Laplace transform so useful for solving differential equations. It says that taking a derivative in $t$ -space is the same as simply multiplying by $s$ in $s$ -space—up to a shift by $x(0)$ .

And that means the Laplace transform can turn a differential equation for $x(t)$ into an *algebraic* equation for $x^(s)$ , because all the derivatives disappear!

Let’s see how that works for our harmonic oscillator equation. We’ll take the Laplace transform of both sides:

$$
d2xdt2^=−Ω2x^(s).
$$

Since $Ω$ is a constant, the RHS is just $−Ω2$ times the Laplace transform of $x$ .

On the LHS, we need to use our derivative rule twice in a row in order to simplify the Laplace transform of $d2xdt2$ . If we plug that into our derivative rule, we get

$$
d2xdt2^=sdxdt^−dxdt(0).
$$

And now if we apply the rule a second time to simplify $dxdt^$ on the right, we get

$$
d2xdt2^=s2x^(s)−sx(0)−dxdt(0).
$$

When we plug in our initial conditions $x(0)=x0$ and $dxdt(0)=0$ , we find that the Laplace transform of our differential equation is

$$
s2x^(s)−sx0=−Ω2x^(s).
$$

As promised, there are no more derivatives! The Laplace transform took our differential equation for $x(t)$ and turned it into an algebraic equation for $x^(s)$ !

And this equation is much easier to solve. Just move the $x^$ ’s over to the LHS,

$$
(s2+Ω2)x^(s)=sx0,
$$

and then divide out the factor out front to get

$$
x^(s)=sx0s2+Ω2.
$$

And that’s the solution to our problem! In $s$ -space, anyway.

To finish the job, we just need to transform back to $t$ -space. There’s a general formula for doing that, but in practice it’s often faster to just pull up a table of Laplace transforms—there’s a nice one [on Wikipedia](https://en.wikipedia.org/wiki/List_of_Laplace_transforms) —and find the one you’re looking for.

In fact, I already mentioned that this rational function is the Laplace transform of

$$
x(t)=x0cos⁡Ωt.
$$

And therefore that’s the solution to our original equation.

So that’s method number 4. Starting from a linear differential equation, take the Laplace transform to try to turn it into an algebraic equation, which you can solve for $x^(s)$ . And finally, transform back to get your solution for $x(t)$ .

### Method 5: Hamiltonian Flow

Alright, we’re in the home stretch now! And I saved maybe the most fascinating of all for last: Hamilton’s equations and flows on phase space.

We started out with the $F=ma$ equation for a block on a spring:

$$
md2xdt2=−kx.
$$

Notice that the LHS is the same as $ddt(mdxdt)$ , since $m$ is a constant. In other words, it’s the derivative of the momentum, $p=mdxdt$ :

$$
dpdt=−kx.
$$

That’s just Newton’s second law: the force is the rate of change of the momentum.

But mathematically, what that enables us to do is replace the single, second-order differential equation that we started with, with a *pair* of *first* order equations:

$$
dxdt=pmdpdt=−kx
$$

These are called **Hamilton’s equations**. I haven’t done anything fancy—this pair of equations contains the exact same content as $F=ma$ —all I’ve done is split it up into two pieces. The first equation is the definition of the momentum, and the second is $F=dpdt$ . And if you take another derivative of the first equation and plug in $dpdt$ from the second, you’ll get back the same second order equation we’ve been studying all along,

$$
d2xdt2=−kmx.
$$

But working with the first-order equations has a couple of big advantages. To see why it’s helpful, let’s draw a picture with $x$ on the horizontal axis and $p$ on the vertical axis:

![](https://www.physicswithelliot.com/s/phase-space-coords.png)

This picture is called the **phase space**, and each point in this plane tells us where the block is and what its momentum—or equivalently its velocity—is at any given instant.

So, for example, when we pull the block out to its initial position and then release it from rest, that initial state corresponds to the point shown above on the horizontal axis, where $x=x0$ and $p=0$ .

After we let it go, the block is going to begin to move, and so these $x$ and $p$ coordinates are going to change with time. The corresponding point in phase space therefore moves around with time, and it traces out a curve, called a **flow**.

And flow really is a good name for it, because I want you to picture this plane like the surface of a pool of water with some current flowing around it. Then we take something like a ping-pong ball and set it down at the point for our initial conditions. Once we let it go, the current will carry the ball off, moving it around the surface of the water. The flow is the path that the ball follows through the water.

But what determines the shape and strength of the current that’s telling the ball where to move? Our differential equations, of course! We can write the pair of them as a single, vector equation:

$$
ddt(xp)=(p/m−kx).
$$

Again, $x$ and $p$ are the coordinates of the ping-pong ball on the surface of the water, and their time derivative is telling us the ball’s velocity vector at each point on this surface. So, over at our initial point, $x$ was positive and $p$ was zero. Then the horizontal component of the velocity vector is zero, and the vertical component is negative. So the velocity of the imaginary ping-pong ball points straight down at that point, as shown in the figure.

Likewise, we can go to each point $(x,p)$ in this plane and draw the velocity vector $(p/m,−kx)$ at that location. Those arrows are what tell us the “current” that’s swirling around this plane, and what dictates how the ping-pong ball will move:

![](https://www.physicswithelliot.com/s/sho-flow.png)

You can see that they’re swirling around the origin—that’s the equilibrium point. And I’m using the colors to indicate how strong the current is: it’s smallest for the yellow arrows near the middle, and gets bigger for the red arrows farther out.

By following those vectors starting from our initial conditions with $x=x0$ and $p=0$ , we can see that the flow is an ellipse that wraps around again and again as the block oscillates back and forth. And since we know the energy is a constant, these curves are just the contours of constant energy in the $xp$ -plane.

This is definitely a more abstract way of thinking about the solution to our differential equation. Remember, the physical system here is the block sliding back and forth on this one dimensional line. So obviously, there isn’t actually any pool of water or ping-pong ball. Those are just useful mathematical constructs for picturing what’s going on.

But what this picture buys us is that [we can very quickly understand](https://www.physicswithelliot.com/simple-pendulum-with-phase-space) what the motion of our system is going to look like without solving any differential equations. All we need to do is draw the arrows at each point in phase space that we get from the RHS of Hamilton’s equations, either by hand or better yet on a computer.

That’s already extremely useful. But Hamilton’s equations also give us a direct way of explicitly writing down the solution for a linear equation like the harmonic oscillator, and that’s the last thing I want to show you.

To see that, let’s express the pair of Hamilton’s equations as a matrix equation:

$$
ddt(xp)=(01m−k0)(xp).
$$

This looks reminiscent of a simple differential equation of the form

$$
ddtz(t)=αz(t),
$$

which says that when we take the derivative of a function $z(t)$ , we’re supposed to get back $z$ again, times a number $α$ . The solution is simple:

$$
z(t)=eαtz(0),
$$

as we can check:

$$
ddteαtz(0)=αeαtz(0)⏟z(t).
$$

Our matrix equation for the block on a spring is of essentially the same form, just with vectors and matrices now instead of single numbers:

$$
ddt(x(t)p(t))=M(x(t)p(t)).
$$

It says that the derivative of the vector $(x(t)p(t))$ is equal to itself, multiplied by a constant matrix

$$
M=(01m−k0).
$$

And the solution is just the matrix analogue of our simple equation for $z$ :

$$
(x(t)p(t))=etM(x(0)p(0)).
$$

That way, when we take the $t$ derivative, it brings down a factor of $M$ from the exponent, and we get back $M$ times the same vector again.

The catch is that $M$ , and therefore $etM$ , are now matrices instead of single numbers. But what does it even mean to take the exponential of a matrix? The answer is provided by the Taylor series for $e$ :

$$
etM=I+tM+12!(tM)2+13!(tM)3+14!(tM)4+⋯,
$$

where $I$ is the $2×2$ identity matrix.

That might look like a nasty thing to try to compute, and it certainly can be in general. But for our matrix $M$ in this problem the answer works out in a beautiful and simple way.

Let’s start off by seeing what $M2$ gives us:

$$
M2=(01m−k0)(01m−k0)=(−k/m00−k/m).
$$

That’s convenient! $M2=−kmI$ is just the constant $−Ω2$ times the identity matrix. That makes calculating the higher powers of $M$ very simple. For example, for $M3$ we get

$$
M3=M2⋅M=−Ω2M,
$$

for $M4$ we have

$$
M4=M2⋅M2=Ω4I,
$$

and so on.

Then the Taylor series for $etM$ is

$$
etM=I+tM−12!t2Ω2I−13!t3Ω2M+14!t4Ω4I+⋯.
$$

You can see that there are two kinds of terms: the odd powers of $t$ that multiply an $M$ , and the even powers that multiply the identity matrix $I$ . Let’s organize them together:

$$
etM=(1−12!(Ωt)2+14!(Ωt)4+⋯)I+1Ω(Ωt−13!(Ωt)3+⋯)M.
$$

To make the second line look nicer, I’ve also multiplied and divided by $Ω$ , so that the $t$ ’s and $Ω$ ’s show up with the same number of powers.

Now some beautifully simple sums are again staring us in the face. On the first line, the sum in parentheses is just $cos⁡(Ωt)$ , and on the second line the sum is $sin⁡(Ωt)$ . And so the matrix exponential simplifies to

$$
etM=cos⁡(Ωt)I+1Ωsin⁡(Ωt)M.
$$

Or, writing out the matrix,

$$
etM=(cos⁡(Ωt)1mΩsin⁡(Ωt)−mΩsin⁡(Ωt)cos⁡(Ωt)).
$$

Thus, to get the solution to Hamilton’s equations, we act this matrix on our initial condition vector,

$$
(x(t)p(t))=(cos⁡(Ωt)1mΩsin⁡(Ωt)−mΩsin⁡(Ωt)cos⁡(Ωt))(x00),
$$

and we find

$$
(x(t)p(t))=(x0cos⁡(Ωt)−mΩx0sin⁡(Ωt)).
$$

Lo and behold, we obtain $x(t)=x0cos⁡(Ωt)$ yet again! And of course the second line is the corresponding momentum, $m$ times the derivative of $x(t)$ .

So I hope I’ve convinced you of how powerful Hamilton’s method is, of converting a second-order equation into a pair of first-order equations. Both for explicitly solving the equation with the matrix exponential, but also for visualizing the behavior of the solution as a flow on phase space.

### Conclusion

We’ve now seen how to solve the harmonic oscillator equation with five different, increasingly sophisticated techniques!

Again, nobody’s saying you actually *should* use Laplace transforms or matrix exponentials to solve such a simple differential equation. But as you work your way up in physics, you’re quickly going to start running into more challenging differential equations where the methods you’ve gotten a glimpse of here become invaluable.

And it’s always a good idea to start learning advanced tools like these by first seeing how to apply them to a simple setup where you already know the solution, before you jump straight into trying to solve much more difficult problems where these tools *do* become essential.

Let me wrap up with a few last comments. First, this was hardly a complete list. There are many different strategies for solving differential equations that I didn’t cover here, and the best one to use depends on the equation you’re trying to solve. For example, one of the most ubiquitous in physics is the method of **Green functions**, which is also one of my favorites. But that really deserves a dedicated lesson.

Second, a really useful approach for solving hard differential equations is to try to tackle them in a special limit where they become simpler. I talked more about that in [my lesson about Taylor series](https://www.physicswithelliot.com/taylor-help-room-notes).

And third, remember that it’s not cheating to use a computer to help you solve a differential equation. Either by finding an exact solution, or a numerical approximation to the solution. There are lots of different tools for doing that, but one place to start is just to type your equation into [wolframalpha.com](https://www.wolframalpha.com/).

---

See also:

- [Simple Harmonic Motion](https://www.physicswithelliot.com/oscillator-help-room-notes)
- [All About Pendulums](https://www.physicswithelliot.com/pendulum-help-room-notes)
- [The Math and Physics of Taylor Series](https://www.physicswithelliot.com/taylor-help-room-notes)
- [The Trick That Makes Physics as Simple as Drawing a Picture](https://www.physicswithelliot.com/potential-help-room-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).