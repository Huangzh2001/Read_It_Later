---
date: "2025-08-10T22:17:25+08:00"
url: "https://www.physicswithelliot.com/taylor-help-room-notes"
status:
---
![](https://www.youtube.com/watch?v=HQsZG8Yxb7w)

Math is the language that we use to describe the laws of nature as physicists. And there’s no way around it: if you want to understand physics, you’re going to have to learn a lot of math. Whether that’s calculus for understanding $F=ma$ , linear algebra for quantum mechanics, or differential geometry for general relativity. But there are certain mathematical results that you will meet time and again throughout your physics education. And if I had to pick one formula that’s the most important for understanding physics, it would be this one, **Taylor’s formula**:

$$
f(x+ε)=eεddxf(x).
$$

It shows up in virtually everything we do in physics. And in this lesson I want to explain how it works, and give you a few examples of its importance in different corners of physics.

You’ve probably learned this theorem before if you’ve taken a calculus class, though you might not have written it in this nice and compact way. I’ll show you that it’s equivalent to the **Taylor series**:

$$
f(x)=f(x0)+f′(x0)(x−x0)+12f″(x0)(x−x0)2+⋯,
$$

that lets us expand any smooth function $f(x)$ in powers of $x$ .

In the first half of the lesson, I’m going to explain where this incredibly important formula comes from and what it means. And then in the second half I’ll tell you about three applications in physics where it shows up—though you’d be hard pressed to find a chapter of any physics textbook where it’s *not* applied.

First, we’ll look at how the Taylor series enables us to understand the complicated equations that we often need to solve in order to understand some physical system by studying a limit where the equations simplify.

Second, I’ll show you how Einstein’s $E=mc2$ , or actually his more general formula $E=m2c4+p2c2$ for the energy of a relativistic particle of mass $m$ and momentum $p$ correctly reproduces the more familiar kinetic energy $12mv2$ for particles that aren’t moving too close to the speed of light. And also how the same Taylor series leads to the fine-structure correction to the energy levels of the hydrogen atom.

And third, we’ll look at how Taylor’s formula leads directly to the definition of the momentum operator in quantum mechanics.

So let’s start with the math, and understand what this formula is all about. And after that we’ll see how it applies to these three physics examples.

![](https://www.physicswithelliot.com/s/function.png)

Say we have some function, $f(x)$ . Here’s a random example. It looks really complicated. But instead of trying to understand the whole complicated function at once, let’s zoom in and look at it in a smaller region where it’s a lot simpler. Take this red point, for example. I've chosen the origin so that this is the point $x=0$ , so the height of the function is $f(0)$ there.

Let’s imagine that we’re explorers living on the graph of this function. We start out at this point $(0,f(0))$ , and we want to understand the shape of the whole function by venturing out in either direction from there. Before we start exploring, all we can say is that the height of the function is this number, $f(0)$ , at our starting point. For all we know, the whole function might just be a constant, $y=f(0)$ —in other words, a horizontal line.

But now we take a little step away from our starting point. We discover that the height of the function has changed, so it’s not actually a horizontal line. Instead, it now looks like a sloped line: the tangent line to the point where we started. The slope of that tangent line is the derivative of the function at $x=0$ . We write it either as

$$
f′(0)=dfdx|x=0,
$$

where the notation $dfdx$ stands for the rise over run: the tiny change $df$ in the height of the function when we take a tiny step $dx$ to the right.

So now that we’ve explored this little neighborhood of $x=0$ , as far as we know our function is a straight line going through $(0,f(0))$ with slope $f′(0).$ The equation of this line is

$$
f(x)≈f(0)+f′(0)x.
$$

This is indeed a good approximation to the actual function $f(x)$ as long as $x$ is tiny, so that we haven’t strayed too far away from $x=0.$

But now we explore a little farther. We discover that the height of the function is deflected away from this sloped line. It’s actually starting to look more like a parabola! So we record on our map that a better approximation would be

$$
f(x)≈f(0)+f′(0)x+Ax2,
$$

for some number $A$ .

And as we venture farther still out into the wilderness, we discover that the function isn’t actually a parabola, and we ought to add $x3$ and $x4$ and $x5$ terms in order to maintain a good approximation to it.

This is the idea behind the Taylor series. We take our function and try to expand it in powers of $x$ :

$$
f(x)=C0+C1x+C2x2+C3x3+⋯,
$$

where the coefficients $C0,C1,C2,C3,$ and so on, are numbers that depend on the function $f$ . All we need to do is figure out how to choose them so that the right-hand-side here coincides with our function.

We’ve already seen what the first couple of coefficients are. When we plug in $x=0$ , we get

$$
f(0)=C0,
$$

so that first number is just the value of the function at our starting point $x=0.$ As for $C1$ , that term and everything else disappears when we plug in $x=0.$ But let’s take the derivative of this whole equation:

$$
f′(x)=C1+2C2x+3C3x2+⋯,
$$

remembering the rule that the derivative of $xn$ is $nxn−1.$ Now when we plug in $x=0,$ the $C1$ term survives!

$$
f′(0)=C1.
$$

So, like we already knew, we should set this first coefficient $C1$ to be the derivative of $f$ at $x=0.$

But now we’ve got the idea. If we take the derivative again, we get

$$
f″(x)=2C2+3⋅2C3x+⋯,
$$

and so when we plug in $x=0$ we learn

$$
f″(0)=2C2.
$$

Then we should choose $C2=12f″(0)$ to be half the second derivative of $f$ at $x=0.$ And on and on it goes. The next term is

$$
f‴(0)=3⋅2C3,
$$

and so we set $C3=16f‴(0).$

Hopefully you see the pattern. For the $n$ ’th term in the series,

$$
f(x)=⋯+Cnxn,
$$

we need to take the derivative $n$ times, until this is the only term that’s around when we plug in $x=0:$

$$
f(n)(0)=n(n−1)(n−2)⋯2⋅1Cn,
$$

where $f(n)$ stands for the $n$ ’th derivative of $f$ . So the $n$ ’th coefficient is

$$
Cn=1n!f(n)(0),
$$

where $n!=n(n−1)(n−2)⋯2⋅1.$

Now we’re in business! The farther away from $x=0$ we get, the more terms we need to include in our series in order to get a good description of the function. But now that we have the general formula for the coefficients, we can include as many terms as we like:

$$
f(x)=f(0)+f′(0)x+12f″(0)x2+13!f‴(0)x3+⋯+1N!f(N)(0)xN.
$$

And here’s the kicker: when we include *all* the terms by summing up the infinite series over all powers of $x$ , we reproduce the *exact* function that we started with, as long as the function was sufficiently well-behaved. This is truly remarkable. It says that if we know all the derivatives of a function at a single point, we can reconstruct the rest of the function everywhere else.

![](https://www.physicswithelliot.com/s/sin.png)

Let’s do some examples. How about $f(x)=sin⁡x$ ? Let’s write down its Taylor series around $x=0.$ All we need to know are the derivatives evaluated there. So let’s make a little table:

$$
f(n)(x)f(n)(0)1n!f(n)(0)xnn=0f(x)=sin⁡(x)f(0)=010!f(0)=0∫n=1f′(x)=cos⁡(x)f′(0)=111!f′(0)x=x∫n=2f″(x)=−sin⁡(x)f″(0)=012!f″(0)x2=0∫n=3f‴(x)=−cos⁡(x)f‴(0)=−113!f‴(0)x3=−13!x3∫n=4f⁗(x)=sin⁡(x)f⁗(0)=014!f⁗(0)x4=0∫
$$

$sin⁡(x)$ passes through the origin, so we start off with $f(0)=0$ . $0!$ is defined as 1 by the way, so our formula for the coefficients still makes sense there. Next up, we need the derivative of $sin⁡(x)$ —that’s $cos⁡(x)$ . Now when we plug in $x=0$ we get $f′(0)=1$ , and so the first interesting term here is just $x$ : a straight line through the origin with slope 1. That’s already a very good approximation to $sin⁡(x)$ when $x$ is a small number, and so we use the approximation $sin⁡(x)≈x$ often in physics.

But once $x$ gets a little bigger, clearly the straight line isn’t going to cut it anymore. So let’s keep going. For the next term, we need the derivative of $cos⁡(x)$ , which is $−sin⁡(x)$ . But that vanishes again when $x=0$ , so the $x2$ term disappears. That’s part of the reason the linear approximation was so good to begin with.

Now for $f‴(x),$ we need the derivative of $−sin⁡(x)$ , and we get $−cos⁡(x)$ . Then $f‴(0)=−1$ , and so the cubic term is $−13!x3.$ Then so far we’ve got

$$
sin⁡(x)≈x−13!x3.
$$

Now we’ve got to do it again—but don’t worry, this will be the last derivative we have to take. For $f⁗(x)$ , we want the derivative of $−cos⁡(x)$ , which is $sin⁡(x)$ . In particular, $f⁗(0)=0$ , and there’s no $x4$ term.

Notice that this fourth derivative brings us back to where we started with $sin⁡(x)$ . So this sequence of derivatives, $0,1,0,−1,$ is just going to repeat over and over again. And now we can just write down the whole series if we want without any more work:

$$
sin⁡(x)=x−13!x3+15!x5−17!x7+19!x9+⋯.
$$

When we add up the whole series, we get back the exact function, $sin⁡(x)$ . Notice that only *odd* powers of $x$ show up on the right hand side. That’s because $sin⁡(x)$ is an odd function: when you compare it on the right and left sides of the $y$ axis, it looks the same except that it’s been flipped over. In other words, $sin⁡(−x)=−sin⁡(x).$ Then we can’t get any even powers in the Taylor series because they wouldn’t respect this property.

But oftentimes in physics we’re not interested in the whole series; what we really want is a good approximation to a function that makes a problem simpler to solve. I’ll show you examples of what I mean in a minute. In this case, we might stop with the first term and just apply the fact that $sin⁡(x)≈x$ when $x$ is small. This is called the **small-angle approximation**, and you may have run into it when you learned about the simple pendulum.

The key point here is that when $x$ is small, like, say, $x=0.1$ , when we take larger powers of $x$ in the successive terms in the Taylor series, they get even *smaller*: $x3=0.001,$  $x5=0.00001$ , and so on, not to mention the huge factorials in the denominators. That’s why we can ignore the higher order terms for small $x$ , and get a good approximation to our function by keeping only the leading term.

![](https://www.physicswithelliot.com/s/exp.png)

Let’s do another quick example: $f(x)=ex$ . This one’s easy because the derivative of $ex$ is just $ex$ again. Then all the derivatives that we need to calculate the Taylor series are the same:

$$
f(n)(x)=ex⟹f(n)(0)=1.
$$

So we don’t even need to make a table for this one, we can just jump right to the Taylor series:

$$
ex=1+x+12x2+13!x3+14!x4+⋯.
$$

This time none of the coefficients vanish. We get every power $xn$ , divided by $n!$ . As a matter of fact, this infinite series is often take as the *definition* of $ex$ . And once again, if $x$ is tiny then we can get a good approximation by stopping at the linear term,

$$
ex≈1+x.
$$

We were able to reproduce the full functions $sin⁡(x)$ and $ex$ by summing up their infinite Taylor series. But a word of warning: this isn't always possible. For example, another function that often shows up in physics is

$$
f(x)=11−x.
$$

Try computing its Taylor series for practice: it's given by

$$
f(x)=1+x+x2+x3+⋯.
$$

You might recognize this sum: it's the geometric series, and $f(x)$ is what you get when you add it all up. But notice that there are no $n!$ factors in the denominators here, like there were for, say, $ex$ . Then if $x$ is bigger than 1, the terms in this series just get larger and larger as the powers grow. That means the sum *diverges* for $x>1.$

What went wrong? $f(x)$ is misbehaving! When $x=1$ , the denominator goes to zero, and the function blows up. Then the Taylor series breaks down beyond this point.

Now before we get to the physics examples, the last thing I want to do is show you a few convenient ways of writing Taylor’s formula. Spelling out the whole sum

$$
f(x)=f(0)+f′(0)x+12f″(0)x2+13!f‴(0)x3+⋯
$$

isn’t very concise, but we can write the same thing much more compactly using summation notation:

$$
f(x)=∑n=0∞1n!f(n)(0)xn.
$$

This is the Taylor series for $f(x)$ , expanded around $x=0.$ But come to think of it, there was nothing special about $x=0$ here; that’s just where we happened to put the origin when we drew the graph of $f(x).$ We could just as well write the expansion around any other point, call it $x0$ , like this:

$$
f(x)=∑n=0∞1n!f(n)(x0)(x−x0)n.
$$

Now we’re writing the series in powers of $x−x0$ —which measures how far away you are from the starting point $x0$ —and the coefficients are determined by the derivatives of $f$ at $x0.$

Another convenient way to write the same thing is to define $ε=x−x0$ as the distance away from $x0.$ So when $ε$ is small you’re looking at the function near the starting point and as $ε$ gets bigger you get farther away. Then by plugging in $x=x0+ε$ here, we could just as well write

$$
f(x0+ε)=∑n=0∞1n!f(n)(x0)εn.
$$

This way of writing things makes it really clear that we can think of the Taylor series as starting out at the point $x0$ and then expanding out away from there, by evaluating $f$ at $x0+ε$ in powers of the displacement.

But that’s not even the slickest way to write the Taylor series, which is the formula I showed you at the very beginning. Remember our other notation for the derivatives,

$$
f(n)(x)=dnfdxn.
$$

Moreover, we can think of $dndxn$ as an operator that takes a function, and then applies the derivative to it $n$ times:

$$
dndxn=ddxddx⋯ddx⏟n times=(ddx)n.
$$

Then we can also write the Taylor series as

$$
f(x+ε)=∑n=0∞1n!(ddx)nf(x)εn.
$$

I’ve dropped the $0$ subscript on $x$ now to keep things from getting cluttered, because that was just an arbitrary label. Dragging that $ε$ to the left inside the parentheses, we get

$$
f(x+ε)=∑n=0∞1n!(εddx)nf(x).
$$

Now this looks really interesting. It says that if we want to know the value of our function $f$ at a point that’s shifted away from $x$ by an amount $ε,$ what we should do is apply this special combination of derivatives to it:

$$
∑n=0∞1n!(εddx)n.
$$

But hang on a second—that looks familiar! Remember that the Taylor series we found for $ez$ a minute ago was

$$
ez=1+z+12!z2+13!z3+⋯,
$$

or, in sum notation,

$$
ez=∑n=0∞1n!zn,
$$

where I’ve written the variable with a new label $z$ so we don’t get it confused with $x.$ But that’s exactly what this differential operator looks like, with $z=εddx$ . Therefore, at least formally, we can express the full Taylor expansion in the form

$$
f(x+ε)=eεddxf(x).
$$

This is the most compact, convenient, and beautiful way of writing Taylor’s formula. Just to make sure it’s clear how this works, let’s try applying it to a really simple function: $f(x)=mx+b.$ Obviously the Taylor series for this one is going to be really boring—it already *is* its own Taylor series! But let’s see what the formula says.

$$
eεddx(mx+b)=(1+εddx+12ε2d2dx2+⋯)(mx+b).
$$

First we expand out the derivatives by remembering the definition of the exponential as an infinite series. But most of the terms here aren’t going to contribute anything at all: our function is a straight line, and so everything from the second derivative on up will just give zero when it acts on $mx+b$ .

So, from the “ $1$ ” acting on $f$ we get $mx+b$ . And from the $εddx$ , we get $εm$ . Then adding them up we find

$$
mx+b+mε=m(x+ε)+b.
$$

Which is precisely $f(x+ε)$ , just as expected!

One last beautiful thing about this way of writing Taylor’s formula. It makes the generalization to the *multi* -variable Taylor expansion really straightforward. In other words, say we have a function $f(x,y,z)=f(r)$ of three variables, where $r=(x,y,z)$ is the position vector. For example, this might be the potential energy function of a particle moving around in three-dimensional space. Then what’s the Taylor expansion of *this*?

One way to approach it is to take $f(x+εx,y+εy,z+εz)$ and expand it, one variable at a time. For example, applying the Taylor expansion in $x$ we get

$$
f(x+εx,y+εy,z+εz)=f(x,y+εy,z+εz)+εx∂∂xf(x,y+εy,z+εz)+12εx2∂2∂x2f(x,y+εy,z+εz)+⋯.
$$

$∂∂x$ here stands for the **partial derivative** with respect to $x$ . All it means is that we should take the derivative of $f(x,y,z)$ with respect to $x$ like we normally would, treating the other variables $y$ and $z$ as constants.

But now we have to do the same expansion over again in each of these terms for $y,$ and then again in each of *those* terms for $z$ . It’s a bit of a mess. But our exponential formula makes the whole thing incredibly simple. All we need to do to generalize

$$
f(x+ε)=eεddxf(x)
$$

to multiple dimensions, is to replace $x→r=(x,y,z)$ with the position vector, $ε→ε=(εx,εy,εz)$ with the displacement vector, and $εddx$ with the sum over all three directions:

$$
εx∂∂x+εy∂∂y+εz∂∂z.
$$

We can write that more compactly as the dot product $ε⋅∇$ between $ε$ and the “vector” of partial derivatives

$$
∇=(∂∂x,∂∂y,∂∂z),
$$

which is called “del.”. Then the multi-variable Taylor series is simply

$$
f(r+ε)=eε⋅∇f(r).
$$

Okay, that’s enough math. Now let’s get to the physics. I promised to show you three applications:

1. “Linearizing” complicated equations of motion
2. The non-relativistic limit of $E=m2c4+p2c2$ and the fine structure of hydrogen
3. Defining the momentum operator in quantum mechanics

Let’s go one by one. You don’t necessarily need to know anything going in about relativity or quantum mechanics, by the way. The point is just to see how Taylor’s formula appears in several very different areas of physics.

Starting with number one. The basic procedure to solve a problem in classical mechanics is to write down all the forces on a particle, add them up and write $F=ma$ , and then solve this equation for the position of the particle as a function of time.

That’s easier said than done, though. Especially the last step—solving $F=ma$ —because for all but the simplest systems, this equation quickly becomes too hard to solve exactly. $F=ma$ is a **differential equation**, which just means that it contains derivatives of the function that you’re trying to solve for. And differential equations are much harder to solve than the algebraic equations that we all first learn in middle school and high school.

![](https://www.physicswithelliot.com/s/pendulum-fbd.png)

A simple example that [I’ve told you about](https://www.physicswithelliot.com/pendulum-help-room-notes) in a few past lessons is the pendulum. When solving for the motion of a pendulum, the main force we’re interested in is the component of gravity that points along the tangent direction to the circle where the particle is constrained to move. That’s $mgsin⁡θ$ , where $θ$ is the angle that the pendulum makes with the vertical axis. Then the $F=ma$ equation for $θ$ reads

$$
mld2θdt2=−mgsin⁡θ,
$$

or

$$
d2θdt2=−glsin⁡θ.
$$

Simple as this physical setup looks, this equation is already very complicated because of that factor of $sin⁡(θ)$ on the right-hand-side. It makes this what we call a **non-linear** differential equation, which can be very nasty to try to solve.

On the other hand, when $θ$ is small, [you can picture](https://www.physicswithelliot.com/pendulum-graph) a pendulum gently rocking back and forth like a grandfather clock. And that motion certainly doesn’t seem very complicated. Is it possible then that we can simplify this equation when $θ$ is relatively small?

The Taylor series lets us do just that. Like we worked out before, the Taylor series for $sin$ is

$$
sin⁡θ=θ−13!θ3+15!θ5+⋯.
$$

But if $θ$ is a small number, then the successive terms get tinier and tinier because we’re raising the already tiny number $θ$ to a positive power. Then for tiny $θ$ ’s, we can apply our small-angle approximation from earlier by keeping only the linear term, and so our $F=ma$ equation becomes

$$
d2θdt2≈−glθ.
$$

That’s vastly simpler! There’s no $sin⁡θ$ factor here anymore making this equation complicated and non-linear. By applying the Taylor series, we’ve been able to **linearize** the differential equation, to turn it into a problem we can solve much more easily in the limit when the pendulum isn’t too far away from equilibrium.

This is just the equation of a simple harmonic oscillator now, like a mass on a spring, and the general solution is

$$
θ(t)=Acos⁡(glt)+Bsin⁡(glt).
$$

So the pendulum indeed rocks gently back and forth from side-to-side.

If you’ve been watching my most recent videos and all this looks familiar, it’s no accident. [I told you](https://www.physicswithelliot.com/oscillator-help-room-notes) a few weeks ago about how the first thing we should do in any physics problem is expand the potential energy function around a stable equilibrium point in a Taylor series:

$$
U(x)=U(0)+U′(0)x+12U″(0)x2+⋯.
$$

I chose my coordinates here so that the equilibrium point is at $x=0.$

The first term, $U(0)$ , is a constant, and doesn’t matter; you’re always allowed to change what you call the “ground level” of your potential energy function and shift this constant away. The second term, meanwhile, vanishes because we’ve chosen to expand around a minimum of the potential, where $U′(0)=0$ . So, typically, the first interesting term in the Taylor expansion of a potential around equilibrium is the quadratic term, which is just like the potential energy $U=12kx2$ of a block on a spring. This is why [systems oscillate](https://www.physicswithelliot.com/simple-pendulum-with-energy-graph) back and forth around their equilibrium position.

As for the force, that’s related to the potential energy by

$$
F=−dUdx,
$$

and therefore the Taylor series for the force on a particle near equilibrium starts with

$$
F=−U″(0)x+⋯,
$$

just like the spring force $F=−kx.$ In particular, the force is linear! So the trick I taught you about the simple harmonic motion you’ll discover when you expand the potential energy around a stable equilibrium point is secretly the same thing as linearizing the $F=ma$ equation!

Next, let’s look at the Newtonian limit of Einstein’s theory of special relativity. In Newtonian mechanics, a free particle has energy

$$
E=12mv2.
$$

Alternatively, if we plug in the momentum $p=mv$ , we can write the same thing as

$$
E=p22m.
$$

This is the energy of a non-relativistic free particle with momentum $p$ . Non-relativistic means that the particle isn’t moving very fast compared to the speed of light. When particles due approach the speed of light, some weird and wild things happen, that were discovered by Einstein one hundred and some years ago when he wrote down his special theory of relativity.

In special relativity, the energy of a free particle of mass $m$ and momentum $p$ is given by

$$
E=m2c4+p2c2,
$$

where $c$ is the speed of light.

You’ve run into this before even if you’ve never studied special relativity. If the particle is at rest, so that $p=0$ , we get

$$
E=m2c4=mc2,
$$

which might be the most famous equation in physics.

But when the particle is moving, we need this more general formula including the momentum $p$ . This formula holds even if the speed of the particle approaches the speed of light (though the definition of $p$ is modified from the Newtonian formula). But on the other hand, we know what the energy is supposed to be when $p$ is small, $p22m,$ so how do we see that Einstein’s formula correctly reproduces Newton’s formula for a slow moving particle?

The idea is of course to apply the Taylor expansion of Einstein’s energy when $p$ is small. Let’s first of all rewrite the formula a little bit to make it more convenient by pulling the $m2c4$ outside the square root:

$$
E=mc21+p2m2c2.
$$

This makes it clear that what we want to do is compute the Taylor series for $f(x)=1+x$ , when $x=p2m2c2$ is small.

Actually, let’s go ahead and work out a slightly more general Taylor series for

$$
f(x)=(1+x)q,
$$

where $q$ is some power. Our case with the square root is then $q=1/2.$ Let’s make a table again to work out the first few terms of the Taylor series:

$$
f(n)(x)f(n)(0)1n!f(n)(0)xnn=0f(x)=(1+x)qf(0)=110!f(0)=1∫n=1f′(x)=q(1+x)q−1f′(0)=q11!f′(0)x=qx∫n=2f″(x)=q(q−1)(1+x)q−2f″(0)=q(q−1)12!f″(0)x2=12q(q−1)x2∫
$$

The first term is always just what you get by plugging in $x=0$ ; that’s just $f(0)=1$ . Then for the next term, we take the derivative, which brings down a factor of $q$ , and when we evaluate that at $x=0$ we get the linear term, $qx.$ Then we take the second derivative, which brings down an additional factor of $q−1$ , and so the quadratic term is $12q(q−1)x2$ .

Then we have

$$
f(x)=1+qx+12q(q−1)x2+⋯.
$$

The first pair of terms,

$$
(1+x)q≈1+qx,
$$

is another very useful approximation that comes up a lot in physics.

Now back to the relativistic energy, we just plug in $q=12$ and $x=p2m2c2$ . To first order we get

$$
E=mc2(1+12p2m2c2+⋯).
$$

Expanding it out, we’ve got

$$
E=mc2+p22m+⋯.
$$

The first term is $E=mc2$ again; that’s what we get by evaluating the energy of a particle at rest in relativity, called the relativistic rest energy of the particle. It doesn’t have an analogue in Newtonian mechanics, but on the other hand it’s just a constant. And you’re always free to add a constant to the total energy without changing anything, just like you get to pick what you want to call ground level when you’re defining a potential energy. Different choices just shift the total energy by a constant.

As for the second term, there we see how the Taylor series reproduces precisely the kinetic energy $p22m=12mv2$ that we expect in Newtonian mechanics. Actually, I’m being slightly sloppy here because the definition of the momentum $p$ gets modified in relativity, and we should Taylor expand that as well. But in the non-relativistic limit we of course get back the Newtonian momentum $p≈mv$ .

So that’s how Einstein’s formula connects to $E=mc2$ and what we’re used to thinking of as kinetic energy. But what about the next term in the Taylor series? That one comes from

$$
12q(q−1)x2=−18p4m4c4,
$$

so that the energy is

$$
E=mc2+p22m−p48m3c2+⋯.
$$

Newtonian mechanics is a good description of the world for particles that aren’t moving anywhere close to the speed of light. But, like any theory of physics, it’s only an approximation to nature. This next term in the Taylor series is the *leading relativistic* *correction* to the Newtonian energy. When $pmc≈vc$ is tiny, meaning that the speed of the particle is much less than the speed of light, then this additional term gives a very small correction to Newton’s result, and we can ignore it without losing much accuracy. But as the speed gets larger, this correction becomes increasingly important.

One place we can see this correction in action is in the **binding energy** of a hydrogen atom. That’s the amount of energy you would need to kick the electron out of its “orbit” around the proton at the center of the hydrogen atom. In a [lesson](https://www.physicswithelliot.com/dimensional-analysis-help-room-notes) from a couple of months ago, I showed you how we can get 90% of the way to the answer for the binding energy just by applying dimensional analysis: in other words, by making a list of the parameters we have available to play with and their units, and seeing how we can combine them to get something with the units that we want. In this case, we saw that we can combine the electron mass $m$ , its electric charge $e$ , Coulomb’s constant $k$ (which sets the strength of the electric force), and Planck’s constant $ℏ$ (which sets the scale of quantum mechanics),

$$
m∼kg,e∼C,k∼N⋅m2C2,ℏ∼kg⋅m2s,
$$

to get units of energy like so:

$$
E∝m(ke2)2ℏ2.
$$

Just by thinking about the units like this gets us almost all the way to the answer. The actual formula for the binding energy comes with a factor of half, which we can’t get by only thinking about units, because “2” doesn’t have any units:

$$
E=m(ke2)22ℏ2+⋯.
$$

This is **Bohr’s formula** for the binding energy of hydrogen, and it was one of the first great accomplishments of quantum mechanics. Its numerical value, about $13.6 eV$ , matches very closely to the experimental value of the binding energy.

And yet, Bohr’s formula is only an approximation: it neglects the small, but fascinating and experimentally observable, effects of special relativity. But where did we go wrong in our dimensional analysis argument? We wrote down the only possible way to combine $m,e,k,$ and $ℏ$ to make units of energy.

Well, it’s not that we went wrong, per se, it’s that in writing down the non-relativistic approximation to the binding energy, we omitted the speed of light $c$ from our list of parameters. So if we want to consider the effects of special relativity, we need to consider how $c$ can enter the formula for the energy.

But something remarkable happens when we add $c$ to the list of parameters: we can form a *dimensionless* combination by

$$
α=ke2ℏc.
$$

This combination $α$ is called the **fine-structure constant**. I’ll leave it for you to check that all the dimensions really do cancel out here when you plug in the units. If you put in the numbers you’ll find that $α≈0.0073$ , or a little more memorably,

$$
α≈1137.
$$

Since $α$ is unitless, dimensional analysis doesn’t tell us anything about how it appears in the formula for the energy—no more than dimensional analysis could tell us about the factor of 2 in the denominator. *Any* function of $α$ can multiply our expression for the energy without spoiling the units. This is how relativity allows small corrections to Bohr’s formula—which, remember, was itself already an excellent approximation to the experimental value of the Hydrogen binding energy. But we can get an even better theoretical prediction by considering the relativistic corrections.

With the leading relativistic correction $−p48m3c2$ that we derived by applying the Taylor series to Einstein’s formula, we can determine the small modification that relativity makes to Bohr’s formula. The details require quantum mechanics, so I won’t go into that here, but the result is that

$$
E=EBohr(1+54α2+⋯),
$$

where $EBohr$ is Bohr’s original formula for the binding energy that ignored relativity. That’s what the first term here reproduces. The second term gives a very small correction to it, because $α$ is a tiny number. It’s therefore called a fine-structure correction.

There are in fact further corrections to this formula, both at order $α2$ , as well as even smaller corrections at higher orders in $α,$ due to various interesting effects.

Finally, while we’re on the subject of quantum mechanics, let’s finish by seeing how Taylor’s formula is related to the definition of momentum in quantum mechanics. In classical mechanics, the main question is to solve for the trajectory $x(t)$ of a particle as a function of time. In quantum mechanics, on the other hand, the goal is to find the **wavefunction** $Ψ(x)$ describing the particle, and how it evolves with time. Where the (square of the) wavefunction is bigger, the more likely you are to find the particle at that location when you make a measurement.

The things that we measure about the particle, like its position and momentum, are represented by **operators** that act on the wavefunction. We write $x^$ for the operator that measures the position and $p^$ for the operator that measures the momentum. The goal isn't to learn quantum mechanics right now, but I gave you a bit of a crash course in the [lesson](https://www.physicswithelliot.com/ccr-mini-notes) about symmetries in quantum mechanics, if you're interested in learning more.

Classically, [I’ve told you about](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes) how momentum is the **generator** of spatial translations, meaning that momentum defines a classical operation that picks up a particle and shifts it over a bit:

$$
p:x→x+ε.
$$

Quantum mechanically, we therefore expect the momentum to be related to an operator, call it $U^(ε)$ , that shifts the wavefunction over by $ε$ :

$$
U^(ε)Ψ(x)=Ψ(x−ε).
$$

Don’t sweat the minus sign. It’s there because of the distinction between shifting the operator $x^→x^+ε$ , which is like picking up your coordinate system and moving it to the left, and shifting the wavefunction $Ψ(x)→Ψ(x−ε)$ to the right. But let’s not worry about it right now, and just take this as the definition of the translation operator in quantum mechanics.

Well that looks familiar! Physics aside, $Ψ(x)$ is just a function, and this formula tells us that we’re looking for an operator that shifts the position where $Ψ$ is evaluated over by $ε$ . That’s just what Taylor’s formula does!

$$
e−εddxΨ(x)=Ψ(x−ε).
$$

Therefore, we identify the translation operator $U^(ε)$ with

$$
U^(ε)=e−εddx.
$$

In quantum mechanics, we usually write operators like this as

$$
U^(ε)=e−iℏεQ^,
$$

where $Q^$ is called the generator of the transformation. The $ℏ$ is there so that $Q^$ comes out with the right units, and the $i$ is there so that $Q^$ is real in an appropriate sense (called Hermitian). It's analogous to writing a complex number as $eiθ.$

Then in the case of the momentum operator, Taylor’s formula can equivalently be written

$$
e−iℏε(ℏiddx)Ψ(x)=Ψ(x−ε).
$$

Thus, the generator of translations is

$$
Q^=ℏiddx,
$$

and this is the definition of the momentum operator $Q^=p^$ in quantum mechanics.

This is just a small selection of physics applications where Taylor’s formula shows up. But again, you’d really be hard-pressed to find any chapter of any physics textbook where Taylor’s formula *isn’t* applied. Keep your eyes open, and you’ll see it everywhere!

---

See also:

- [All About Pendulums](https://www.physicswithelliot.com/pendulum-help-room-notes)
- [Dimensional Analysis is Your Physics Superpower](https://www.physicswithelliot.com/dimensional-analysis-help-room-notes)
- [To Master Physics, First Learn the Harmonic Oscillator](https://www.physicswithelliot.com/oscillator-help-room-notes)
- [Quantum Origins of the Canonical Commutation Relation](https://www.physicswithelliot.com/ccr-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).