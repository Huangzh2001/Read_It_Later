---
date: "2025-08-10T22:00:09+08:00"
url: "https://www.physicswithelliot.com/noether-field-theory-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=I4CjewbJgRQ)

The relationship between symmetries of nature and conservation laws in physics is one of the most profound connections that human beings have understood about the universe since we started doing science. Symmetries are so fundamental that the standard model of particle physics, which is the most predictive theory that scientists have ever written down, is typically denoted simply by its symmetry group, called “ $SU(3)×SU(2)×U(1)$ ”. In this lesson, we’re going to explore the most basic symmetry at the heart of the standard model: the symmetry that underlies electromagnetism and the conservation of electric charge.

[We’ve seen](https://www.physicswithelliot.com/noether-mini-notes) in [past lessons](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes) how symmetries are tied together with conservation laws by Noether’s theorem. Translation symmetry in space, for example, is tied to momentum conservation, meaning that if you can pick your system up and slide it over without changing anything about the physics, then the total momentum in that direction is a constant. Rotational symmetry likewise leads to *angular* momentum conservation. And energy conservation follows from translation symmetry in *time*, meaning if the dynamics of your system looked the same yesterday as they will tomorrow.

What Noether’s theorem says is that if a system of particles described by a Lagrangian $L$ has a symmetry, then you’re guaranteed to find a corresponding conserved quantity $Q$ , meaning that if you evaluate $Q$ at any time $t$ , you’ll always get back the same number:

$$
dQdt=0.
$$

In the [last mini-lesson](https://www.physicswithelliot.com/fields-mini-notes), though, we started discussing field theory, where we’re not only interested in how the coordinates $x(t)$ of a bunch of particles move around, but in fluctuating fields $ϕ(t,x)$ that permeate space and time, interacting with particles and, potentially, with each other. The most intuitive examples to keep in mind are the electric and magnetic fields that propagate the electromagnetic forces between charged particles, and that are bouncing off your eyeballs at this very moment.

In a field theory like electromagnetism, the connection between symmetries and conservation laws becomes even deeper. You’re no doubt familiar with the conservation of electric charge, for example. But the conservation of charge isn’t simply a statement that the total amount of electric charge in the universe is a constant. For example, if an electron disappeared from Tokyo at the same moment a muon appeared next to Tau Ceti, the total amount of electric charge would not have changed. But a conservation law in field theory is stronger than that: charge is conserved *locally*, meaning that the only way the amount of charge can change inside any box, large or small, is if a **current** continuously carries charges in or out.

But if conservation laws result from symmetries of nature, then what symmetry is responsible for the conservation of electric charge?

That’s what I want to tell you about in this lesson. We’ll see how local conservation laws arise in field theory, and how they’re captured by the **continuity equation**

$$
∂ρ∂t+∂Jx∂x+∂Jy∂y+∂Jz∂z=0⟺∂μJμ=0,
$$

where $ρ$ is the charge density and $J$ is the current density. And we’ll identify the associated symmetry, known as “ $U(1)$ ”, in a theory like electromagnetism that’s tied to the conservation of electric charge by Noether’s theorem. This is the simplest component of the standard model of particle physics, although I should clarify that the $U(1)EM$ of electromagnetism is not literally the $U(1)$ in the $SU(3)×SU(2)×U(1)Y$ symmetry that labels the standard model. Instead, $U(1)EM⊂SU(2)×U(1)Y$ is a component sitting inside the standard model, that falls out after the Higgs mechanism and its famous Higgs particle do their business. That part of the story will have to wait for another day, though.

[[Read It Later/attachments/013ac7a6969f15e8b28713f3bbc4d41d_MD5.png|Open: 013ac7a6969f15e8b28713f3bbc4d41d_MD5.png]]
![[Read It Later/attachments/013ac7a6969f15e8b28713f3bbc4d41d_MD5.png]]

Let’s start off by understanding what it means for electric charge to be locally conserved, which you may or may not have learned about before in a class on E&M, and after that we’ll see how conservation laws like these arise naturally from Noether’s theorem for any field theory. Say we have some volume of space $R$ , and we count up the amount of charge $Q$ inside of it. $R$ might be the inside of a cubical box, for example, or it could be some complicated shape. To measure the amount of charge inside the box, we start from the charge density $ρ(t,r)$ , which represents the amount of charge per unit volume at any point $r=(x,y,z)$ in space at any time $t$ . In other words, if we look at an infinitesimally tiny box at a point $r$ , the amount of charge inside it is the charge per volume, $ρ$ , times the volume of the little box, $dxdydz$ , which I’ll write as $d3r$ for short. To find the total charge inside our actual box $R$ , we just dice it up into lots of little pieces like this, each with charge $ρd3r$ , and then add them all up by integrating over the region:

$$
Q(t)=∫Rd3r ρ(t,r).
$$

This is the total amount of charge in our box $R$ at time $t$ .

What charge conservation means is that the only way $Q$ can change with time is if some of the charges inside the box move outside through the surface, or if additional charged particles from outside make their way in. Let’s write $B$ for the boundary surface of the box. These moving charges would constitute an electric current, and so what we need to figure out is, given some current, how much charge is flowing into or out of the region through the boundary $B$ at any moment?

Similar to $ρ$ , which measured the charge density per volume of space, we measure the amount of current by the current density $J$ . But there are some important differences between $ρ$ and $J$ . Note first of all that $J=(Jx,Jy,Jz)$ is a vector, because a current can flow in any direction in space. Also, whereas $ρ$ was the amount of charge per unit volume, which we used to find the total amount of charge inside the volume of the box, with $J$ we want to find the amount of current flowing through the boundary surface $B$ . We therefore define $J(t,r)$ to be the current per unit *area*, rather than per unit volume.

Let’s look at the top surface of our box, for example, and see how much current is flowing out through it. Take a little patch of the surface at a point $r=(x,y,z)$ , of width $dx$ and length $dy$ . Since we want to know how much current is flowing out of the box, what we care about in this case is the $z$ component of $J$ at that point— $Jx$ and $Jy$ just measure the current flowing parallel to the surface. Then the amount of current passing through that little patch is given by its area $dxdy$ times $Jz$ , the current per unit area in the $z$ direction. We get the total current passing through the whole top surface of the box by integrating over it:

$$
Itop=∫dxdyJz(t,r).
$$

At any instant in time $t$ , this is the amount of charge per second leaving through the top surface of the box.

Of course, now we need to do the same to find the current passing through the other sides of the box, and then add them all up to get the total current going through the whole surface. In general, our region $R$ needn’t be a neat box and $B$ needn’t be a cubical surface. It could be some misshapen blob instead. But the idea is the same. We slice up the surface into many little patches, each of area $da$ . Then we multiply that by the current per area flowing out through the patch. That’s given by $J(t,r)$ at that point, but again we need to pick out the component that points perpendicular to the surface there in order to obtain the amount of current going out. Let’s write $n^$ for the unit vector that’s perpendicular to the surface at that point. For example, on the top surface of the box $n^=z^$ was a unit vector pointing up in the $z$ direction, on the right surface it would be $n^=y^$ pointing to the right in the $y$ direction, and so on. Then we can pick out the perpendicular component of $J$ by taking the dot product, $J⋅n^$ .

All together then, the total current passing out of the boundary surface $B$ is given by integrating over the area of the surface:

$$
I=∫Bda J⋅n^.
$$

Which brings us back to charge conservation. $I$ measures the amount of charge per unit time leaving the box (or entering it, if $I$ comes out negative). Local conservation of charge is the statement that if charge $I$ per unit time flows out through the boundary, then the amount of charge $Q$ inside the volume of the box goes down at that same rate:

$$
dQdt=−I.
$$

This is the mathematical statement of charge conservation. Again, the minus is there because we defined positive $I$ to mean that current is flowing out through the boundary, in which case the amount of charge inside the box is *decreasing* at that same rate.

Spelled out, the charge conservation equation says that

$$
ddt∫Rd3r ρ=−∫Bda J⋅n^.
$$

If, in particular, we took $R$ to encompass *all* of space, so that the boundary $B$ is going to infinity, the current density $J$ had better go to zero there in any physically reasonable setup since there’s nowhere left for the current to flow out to. Then the RHS vanishes, and this equation says that the total charge in all of space is a constant. That’s the statement of global charge conservation. But again, local conservation of charge is a stronger statement: that this equation must hold for any volume $R$ we like. That’s why a charge can’t disappear from Tokyo and reappear at Tau Ceti. Instead of choosing $R$ to fill all of space, just build a box around Tokyo. Then the total charge inside can only change if charged particles are continuously carried in or out through the surface along a current.

On the flip side, we can alternatively take our box $R$ to be an infinitesimally small cube, whose dimensions $Δx$ , $Δy$ , $Δz$ are going to zero. That lets us turn this integral equation into a differential equation. Let’s first of all bring the $ddt$ inside the integral on the left:

$$
∫Rd3r ∂ρ∂t=−∫Bda J⋅n^.
$$

The only change is that it turns into a partial derivative $∂∂t$ , because $ρ(t,r)$ is a function of both time and space.

Now when we shrink our volume down to a teeny, tiny cube surrounding a point $(x,y,z)$ , these integrals become pretty boring. On the left, we just get $∂ρ∂t$ times the volume of the box,

$$
∫Rd3r ∂ρ∂t=ΔxΔyΔz ∂ρ∂t,
$$

the reason being that $∂ρ∂t$ is essentially constant over this infinitesimally small region.

[[Read It Later/attachments/65693b6fdcec8993e0db24ff36c8fc75_MD5.png|Open: 65693b6fdcec8993e0db24ff36c8fc75_MD5.png]]
![[Read It Later/attachments/65693b6fdcec8993e0db24ff36c8fc75_MD5.png]]

The RHS is slightly more interesting. Take the top surface again, for example. The outward pointing perpendicular direction is going up, so we get $J⋅n^=Jz$ evaluated at the top of the box, and the area is $ΔxΔy$ . So the top surface contributes

$$
ΔxΔy Jz|top
$$

to the integral. For the bottom surface, on the other hand, the outward direction is pointing down, so for that piece of the integral we get $J⋅n^=−Jz$ , and the bottom surface contributes

$$
−ΔxΔy Jz|bottom.
$$

Together, we get

$$
ΔxΔy (Jz|top−Jz|bottom).
$$

In other words, it’s $ΔxΔy$ times $ΔJz$ —the change in $Jz$ between the top and bottom of the box.

We had a factor of $ΔxΔyΔz$ on the LHS of our equation that we’re going to want to cancel out, so let me go ahead and multiply by $ΔzΔz$ on the right. Then the contribution to the surface integral from the top and bottom of the box is

$$
ΔxΔyΔz ΔJzΔz.
$$

It’s the volume of our little bitty cube times $∂Jz∂z$ , the derivative of $Jz$ in the $z$ direction!

Of course, we also have to include the right and left, and “forward” and “back” surfaces of the box as well. Those give us the derivatives of $Jx$ in the $x$ direction and $Jy$ in the $y$ direction. All together, our charge conservation equation when we shrink the region $R$ down to be infinitesimally small becomes

$$
ΔxΔyΔz∂ρ∂t=−ΔxΔyΔz(∂Jx∂x+∂Jy∂y+∂Jz∂z).
$$

Cancelling out the volumes, we’re left with a differential relation

$$
∂ρ∂t+∂Jx∂x+∂Jy∂y+∂Jz∂z=0.
$$

This is the most direct, local statement of electric charge conservation. It’s called the **continuity equation**, and it’s the prototype for what it means to have a conservation law in any field theory. We usually shorten it by defining a “vector” with the $x$ , $y$ , and $z$ derivatives

$$
∇=(∂∂x,∂∂y,∂∂z),
$$

called “del.” Then the sum of the derivatives of $Jx,$  $Jy$ , and $Jz$ are just the dot product of $∇$ and $J$ , and we can express the continuity equation as

$$
∂ρ∂t+∇⋅J=0.
$$

By the way, what we basically did in our argument here was discover the **divergence theorem** (because $∇⋅J$ is called the **divergence** of $J$ ), which you’ll learn about in your math classes:

$$
∫Rd3r ∇⋅J=∫Bda J⋅n^.
$$

It lets us turn the integral of a function like $J$ over a surface into the integral of the derivatives of $J$ over the volume inside. Since $R$ was arbitrary for us, we can shrink it down and conclude that the integrands $∂ρ∂t$ and $−∇⋅J$ on the two sides have to be equal point by point.

Okay, now we’ve understood what it means for electric charge to be conserved in electromagnetism. Next we want to understand how all this extends to a more general field theory defined by its action

$$
S=∫titfdt∫spaced3r L,
$$

given by integrating the Lagrangian density $L$ over space and time. And most of all, we want to understand how these conservation laws are related to symmetries by Noether’s theorem. In particular, I hope you’re really curious at this point to discover what symmetry is responsible for the conservation of electric charge!

In the [last mini-lesson](https://www.physicswithelliot.com/fields-mini-notes), we started learning about field theory by studying the simplest example, called the Klein-Gordon theory. It consists of a single free field $ϕ(t,r)$ that assigns a number to each point $r$ in space at each time $t$ , and it’s a great example for learning the fundamentals of field theory. It’s defined by the Lagrangian density

$$
L=12c2(∂ϕ∂t)2−12(∂ϕ∂x)2−12κ2ϕ2,
$$

plus the $y$ and $z$ derivative terms, which I haven’t written out. $c$ here is the speed of light, and $κ$ is a parameter that we saw is related to the mass of the particles that you get when you turn this into a quantum theory. Actually, we usually just wind up calling $L$ the Lagrangian instead of the Lagrangian density, though strictly speaking the Lagrangian is what you get after you integrate $L$ over space.

By applying the principle of least action to this theory, we found that the equation of motion for $ϕ$ is the Klein-Gordon equation:

$$
−1c2∂2ϕ∂t2+∂2ϕ∂x2=κ2ϕ,
$$

which is a generalization of the wave equation, and we talked about how we can write the general solution of this equation as a sum of plane waves, $ei(kx−ωt)$ .

I also showed you last time how to write all this much more compactly using relativistic notation. It makes all the formulas involved in this subject much more neat and concise, but on the other hand, if it’s new to you, then it might backfire and make the equations seem mysterious. So first I’ll work things through with all the $t$ ’s and $x$ ’s spelled out, and then afterwards I’ll show you how much simpler things look with a better notation.

When we talked about [Noether’s theorem](https://www.physicswithelliot.com/noether-mini-notes) for regular old particle mechanics, what we discovered was that whenever we had a symmetry of the Lagrangian—meaning an infinitesimal transformation that left it invariant—there would be a corresponding conserved quantity that’s constant in time as the particle moves around.

[[Read It Later/attachments/570f52f58572023e551d9dbc2848ed0c_MD5.png|Open: 570f52f58572023e551d9dbc2848ed0c_MD5.png]]
![[Read It Later/attachments/570f52f58572023e551d9dbc2848ed0c_MD5.png]]

For example, we looked at one problem with a block sitting on a frictionless table attached to a spring that’s pinned down at the other end. This setup does *not* have translation symmetry: if you pick up the block and slide it over to the right, say, the spring gets stretched and so you’ve changed the system! Then the $x$ and $y$ momenta of the block aren’t conserved, as expected since the spring will pull on the block and accelerate it if you move it away from equilibrium.

On the other hand, the system does have rotational symmetry, because you can pick up the block and rotate it around without changing the length of the spring. The potential energy stored in the spring, $U=12k(r−l)2$ , only cares about how far away from the origin the block is, measured by $r=x2+y2$ , not the angle $θ$ that it makes in the $xy$ plane. We showed that this rotational symmetry implies by Noether’s theorem that the angular momentum of the block is conserved.

We’re going to discover a similar, and even stronger relationship in field theory between symmetries and conservation laws. In fact, the symmetry that’s tied to electric charge conservation is closely analogous to the symmetry of the block on a spring. It’s a rotational symmetry in *field* space that leads to electric charge conservation.

To see how this works, it’ll actually be more interesting, and more closely analogous to the field theory that describes the electron and electromagnetic force, to study a slight generalization of the Klein-Gordon theory. Instead of a real field $ϕ(t,r)$ that assigns a real number to each point in space at each time, let’s consider a *complex* field that assigns a complex number to each point, meaning a number $ϕ=a+ib$ with a real part and an imaginary part. We define the Lagrangian for the complex field by

$$
L=1c2∂ϕ¯∂t∂ϕ∂t−∂ϕ¯∂x∂ϕ∂x−κ2ϕ¯ϕ,
$$

where it’s conventional to leave out the factors of 1/2 for the complex version. $ϕ¯$ stands for the complex conjugate of $ϕ$ : $ϕ¯=a−ib$ . The Lagrangian is real, though, because

$$
ϕ¯ϕ=(a−ib)(a+ib)=a2+b2,
$$

which is real, and likewise for the other terms in the Lagrangian—all the imaginary cross terms cancel out. If you split up $ϕ$ into a real and imaginary part like this, then you can see that this theory is just two copies of our old real Klein-Gordon theory—one for the real part and one for the imaginary part. In the quantum version, we’ll therefore get *two* kinds of particles, corresponding to a particle and anti-particle pair.

The equation of motion for $ϕ$ is still the Klein-Gordon equation,

$$
−1c2∂2ϕ∂t2+∂2ϕ∂x2=κ2ϕ,
$$

and likewise we can write the same thing for $ϕ¯$ just by putting a bar on top,

$$
−1c2∂2ϕ¯∂t2+∂2ϕ¯∂x2=κ2ϕ¯.
$$

Now, what symmetries does this theory have? Like I mentioned, the one I want to focus on is closely analogous to our block-on-a-spring example from a minute ago. The real and imaginary parts of $ϕ=a+ib$ give us a point $(a,b)$ in a 2d plane. In other words, we can think of the complex number $ϕ$ like an arrow that goes over to the right by $a$ in the “real direction”, and up in the “imaginary direction” by $b$ .

[[Read It Later/attachments/8f16d70844fe931e88e213a27855f702_MD5.png|Open: 8f16d70844fe931e88e213a27855f702_MD5.png]]
![[Read It Later/attachments/8f16d70844fe931e88e213a27855f702_MD5.png]]

The length of the arrow is $|ϕ|=a2+b2$ , and it makes an angle $θ$ with the horizontal axis, so that the lengths of the two sides of the triangle are $a=|ϕ|cos⁡θ$ and $b=|ϕ|sin⁡θ.$ But just like the block-on-a-spring, our complex Klein-Gordon Lagrangian only depends on the length $|ϕ|$ of the arrow, not on the angle $θ$ that it makes in this plane.

The reason why is that $ϕ$ and $ϕ¯$ always show up paired together in each term of the Lagrangian. The last term, for example, is just $ϕ¯ϕ=a2+b2$ , i.e. the length-squared of the arrow, $ϕ¯ϕ=|ϕ|2$ . The same goes for the terms with the derivatives, because again $ϕ$ and $ϕ¯$ always appear together.

We therefore learn that this Lagrangian has rotational symmetry, in the sense of the complex $ϕ$ plane! This is the same kind of symmetry that leads to electric charge conservation in electromagnetism.

Another way to say the same thing is to use the fact that a complex number $ϕ=a+ib$ can equivalently be written as $ϕ=|ϕ|eiθ$ , where again $|ϕ|=a2+b2$ is the magnitude and $θ$ is the angle of the arrow. That’s thanks to Euler’s identity $eiθ=cos⁡θ+isin⁡θ,$ so that

$$
|ϕ|eiθ=|ϕ|cos⁡θ+i|ϕ|sin⁡θ.
$$

$|ϕ|cos⁡θ$ and $|ϕ|sin⁡θ$ are just the horizontal and vertical components $a$ and $b$ of our arrow, and so this is the same as writing $a+ib$ .

The reason writing things this way is convenient is that it makes it very simple to rotate $ϕ=|ϕ|eiθ$ to a new angle: just multiply it by $eiα$ for whatever angle $α$ you want to rotate by,

$$
ϕ→eiαϕ=|ϕ|eiαeiθ=|ϕ|ei(θ+α),
$$

thanks to the fact that $eAeB=eA+B$ . So after we multiply by $eiα$ , $ϕ$ gets rotated around to a new angle $θ+α$ , but the magnitude $|ϕ|$ doesn’t change.

The rotational symmetry of our Lagrangian is therefore simply the transformation

$$
ϕ→eiαϕ,ϕ¯→e−iαϕ¯.
$$

And in this notation it’s even easier to see why the Lagrangian is invariant: since each term has a $ϕ$ and a $ϕ¯$ , when we make the transformation one picks up a factor of $eiα$ and the other $e−iα$ , and when they’re multiplied together they cancel each other out!

This kind of symmetry is called $U(1)$ , where the $U$ stands for **unitary**. The terminology comes from the definition of a unitary matrix, which is a matrix $M$ that satisfies the property $M―TM=1,$ meaning that if you take the complex conjugate of $M$ and then its transpose, you should get the inverse matrix of $M$ . The space of $n×n$ matrices satisfying this property is called $U(n)$ . For $n=1$ , though, the “matrix” is just a single number, and it has to be of the form $eiα$ , just like our rotation factor. That’s because its complex conjugate is $e−iα$ , while the transpose doesn’t do anything at all, and indeed $e−iαeiα=1.$

By the way, the other symbols $SU(3)$ and $SU(2)$ in the standard model symmetry group $SU(3)×SU(2)×U(1)$ stand for similar, larger symmetries with $n=2$ and $n=3$ . The " $S$ " means that in addition to being unitary, these rotation matrices are required to have determinant equal to 1.

Now that we have the symmetry we’re interested in, let’s see how it leads to a conservation law by Noether’s theorem. Remember the basic way that Noether’s theorem worked when we studied it before in particle mechanics. The point was that under an arbitrary transformation with infinitesimal parameter $ε$ , the change in the Lagrangian always takes the form

$$
dL=(EOM)ε+ddtQ,
$$

where $EOM$ is the thing that vanishes when the equation of motion is satisfied. If we choose a specific $ε$ that gives us a symmetry of the Lagrangian, then $dL=0$ on the LHS. Then on the physical trajectory, where $EOM=0$ , this equation tells us that whatever quantity $Q$ appears under the $ddt$ is conserved, $dQdt=0$ .

We’ll discover a very similar relationship in field theory. The main difference is that $ϕ(t,r)$ now depends on both time and space, and so instead of just getting a $t$ derivative on the RHS, we’ll have a sum of time and space derivatives:

$$
dL=(EOM)ε+∂ρ∂t+∂Jx∂x+∂Jy∂y+∂Jz∂z,
$$

for some quantities $ρ$ and $J=(Jx,Jy,Jz)$ that depend on the transformation we’re making. If we choose a symmetry transformation for which $dL=0$ , then when the field satisfies the equation of motion we discover a continuity equation:

$$
∂ρ∂t+∇⋅J=0.
$$

A local conservation law! This is the way Noether’s theorem guarantees that symmetries lead to conservation laws in field theories.

Let’s work it out for our rotational symmetry of the complex Klein-Gordon Lagrangian,

$$
L=1c2∂ϕ¯∂t∂ϕ∂t−∂ϕ¯∂x∂ϕ∂x−κ2ϕ¯ϕ.
$$

Start with an arbitrary transformation of the field,

$$
ϕ→ϕ+ε,
$$

where $ε$ is an infinitesimal shift. $ε$ can be anything here, including a function of time and space and even $ϕ$ itself.

For any random choice of $ε$ , the Lagrangian certainly isn’t going to be invariant. Let’s see how it changes in general when we make this shift. When we make the substitution $ϕ→ϕ+ε$ in $L$ , leaving $ϕ¯$ alone for the moment,

$$
L→1c2∂ϕ¯∂t∂∂t(ϕ+ε)−∂ϕ¯∂x∂∂x(ϕ+ε)−κ2ϕ¯(ϕ+ε),
$$

we just get back the original Lagrangian we started with, plus three new terms with $ϕ$ replaced by $ε$ . (Again, I’m not bothering to write the $y$ and $z$ terms here since things are already getting complicated enough.)

Then the change in the Lagrangian under this transformation is

$$
dL=1c2∂ϕ¯∂t∂ε∂t−∂ϕ¯∂x∂ε∂x−κ2ϕ¯ε.
$$

Next up, just like when we learned to apply the principle of least action, we want to integrate by parts on the first two terms to rewrite them like so:

$$
1c2∂ϕ¯∂t∂ε∂t=−1c2∂2ϕ¯∂t2ε+∂∂t(1c2∂ϕ¯∂tε)
$$

and

$$
−∂ϕ¯∂x∂ε∂x=∂2ϕ¯∂x2ε−∂∂x(∂ϕ¯∂xε).
$$

Then we find that the leading change in the Lagrangian when we make a tiny variation $ϕ→ϕ+ε$ is

$$
dL=(−1c2∂2ϕ¯∂t2+∂2ϕ¯∂x2−κ2ϕ¯)ε+∂∂t(1c2∂ϕ¯∂tε)−∂∂x(∂ϕ¯∂xε).
$$

As promised, the first big quantity in parentheses is just the thing that vanishes when $ϕ¯$ satisfies its Klein-Gordon equation. Indeed, this was almost exactly the procedure we followed to *derive* the Klein-Gordon equation when we applied the principle of least action last time. The only difference was that in that case we required $ε$ to vanish at the boundaries of the integral: namely at the initial and final times $ti$ and $tf$ , and at spatial infinity. That’s because in that context we’re trying to find the field configuration that minimizes the action within the set of fields with fixed boundary conditions. Then when we integrate $dL$ to find the change in the action, the second pair of terms with the derivatives drop out—just like we saw with the divergence theorem, the integral basically kills the derivatives and leaves the things in parentheses evaluated at the boundaries, which vanish because $ε=0$ there.

But our identity here for $dL$ holds for any transformation $ϕ→ϕ+ε.$ Of course $ϕ¯$ will also transform as well, in general, by $ϕ¯→ϕ¯+ε¯$ where $ε¯$ is the complex conjugate of $ε.$ That works out in a totally analogous way, and when we add it all up to find the total change in the Lagrangian, we get an equation of the form

$$
dL=EOM′s+∂ρ∂t+∂Jx∂x+∂Jy∂y+∂Jz∂z,
$$

where I’ve defined

$$
ρ=1c2(ε∂ϕ¯∂t+ε¯∂ϕ∂t)
$$

and

$$
Jx=−(ε∂ϕ¯∂x+ε¯∂ϕ∂x),
$$

and similarly for $Jy$ and $Jz$ . There are also cross terms that go like $εε¯$ when we plug the transformed fields into $L$ , but remember that we’re only working with infinitesimal transformations here, and we don’t care about any terms with more than one power of $ε$ and/or $ε¯$ .

Noether’s theorem is now staring us in the face! This formula for $dL$ holds for any transformation $ε$ , $ε¯$ , but if we now choose a specific symmetry transformation for which $dL=0$ , then when the Klein-Gordon equations are satisfied we learn that the corresponding $ρ$ and $J$ define a conserved charge and current!

We’ve seen that $L$ is invariant under the rotation

$$
ϕ→eiαϕ,ϕ¯→e−iαϕ¯.
$$

It’s a symmetry for any angle $α$ , but to apply Noether’s theorem we only care about the infinitesimal version. So let’s apply the Taylor series

$$
eiα=1+iα+⋯,
$$

keeping only the first interesting term. Then our infinitesimal rotation symmetry is

$$
ϕ→ϕ+iαϕ,ϕ¯→ϕ¯−iαϕ¯.
$$

In other words, this is the transformation with $ε=iαϕ$ and $ε¯=−iαϕ¯.$ When we plug these into our formulas for $ρ$ and $J$ , we find that the rotation symmetry leads to a local conservation law with

$$
ρ=ic2(ϕ∂ϕ¯∂t−ϕ¯∂ϕ∂t)
$$

and

$$
J=−i(ϕ∇ϕ¯−ϕ¯∇ϕ),
$$

where I’ve dropped the overall factor of $α$ , which was just an arbitrary constant. Don’t sweat the $i$ ’s by the way—the things in parentheses are pure imaginary since they’re each a complex number minus its complex conjugate. Then multiplying by the $i$ out front gives us back a real number.

Then Noether’s theorem implies that $ρ$ and $J$ satisfy

$$
∂ρ∂t+∇⋅J=0,
$$

and we have a conservation law.

Notice how similar the formulas for $ρ$ and $J$ are here. It’s the same sort of expression, just with $t$ derivatives for $ρ$ and space derivatives for $J$ . Then there’s also an overall sign difference, and the couple of factors of $c$ in $ρ.$ These formulas are screaming out that they should be combined into a four-component spacetime vector.

Remember from last time that we introduced a notation for spacetime coordinates like this

$$
Xμ=(ctxyz),
$$

where $μ=0,1,2,3$ is an index. $μ=0$ is the “time component” $X0=ct$ , and $μ=1,2,3$ are the space components. The factor of $c$ is there so that all the entries have the same dimensions of length.

Then we can define the derivatives with respect to $Xμ$ by

$$
∂∂Xμ=(1c∂∂t∂∂x∂∂y∂∂z).
$$

We usually write this even more simply as $∂μ$ .

Now let’s put the charge density $ρ$ and spatial current $J$ together into the four-component **spacetime current**

$$
Jμ=(cρJxJyJz).
$$

The $c$ is again there so that each component has the same units.

This makes a lot of sense! $J$ is the amount of current flowing around through space, while $ρ$ is like a current flowing forward through time. For example, even if you just set a charged particle down at rest, so that $J=0$ , the particle is still moving forward through time, and $cρ$ is measuring the spacetime current in that direction.

In this notation, the current conservation law is simply

$$
∑μ=03∂μJμ=0,
$$

because if we expand out the LHS we get

$$
∂J0∂X0+∑i=13∂Ji∂Xi=1c∂∂t(cρ)+∇⋅J,
$$

and the $c$ ’s cancel.

Thus, in our first notation we got the slightly awkward equation that the divergence of $J$ in space, $∇⋅J$ , is equal to minus the rate of change of the charge density, $−∂ρ∂t$ . But in relativistic notation the conservation law is much simpler: the divergence of $Jμ$ in *spacetime* must vanish, $∑∂μJμ=0$ .

The divergence $∇⋅J$ measures how much $J$ spreads outward from a given point, like a water sprinkler spraying water out of a spigot. The conservation law says that $Jμ$ can't have any divergence in spacetime, meaning you're not allowed to simply pop out new charges at any spacetime point. (Or, rather, no *net* charge. One could have a positive and negative charge pop out of the vacuum, for example, as long as the total charge is balanced.)

In fact, we usually don’t even bother to write sums like $∑μ=03$ . We just adopt the convention that any time an index like $μ$ appears twice in any given term, as in $∂μJμ$ , we sum over all its values. When $∂μJμ=0$ , we say that we have a **conserved current**.

Putting together the $ρ$ and $J$ components we found for the rotation symmetry, the spacetime current is simply

$$
Jμ=iημν(ϕ¯∂νϕ−ϕ∂νϕ¯),
$$

where $η$ is the 4x4 diagonal matrix we defined last time:

$$
ημν=(−1111).
$$

It’s what takes care of the relative signs for us between the time and space terms. For example, we get

$$
J0=iη00(ϕ¯∂0ϕ−ϕ∂0ϕ¯)=−i(ϕ¯1c∂∂tϕ−ϕ1c∂∂tϕ¯)=cρ,
$$

with the same $ρ$ we found earlier.

Okay, these formulas are pretty, but you’re probably looking at them and wondering what the heck they mean. What’s the conserved quantity we’re talking about here? Remember that the conserved charge is defined by integrating the charge density $ρ$ over space,

$$
N=∫d3r ρ,
$$

which I’m calling $N$ now instead of $Q$ for the reason we’ll see in a second.

Also recall that last time we discussed that the general solution to the Klein-Gordon equation can be written as a sum of plane waves $ei(kx−ωt)$ , which turn into the wave functions for particles created by the field in the quantum theory. By plugging this expansion into $N$ , you can show that what it does is count the number of particles minus the number of anti-particles! This number is therefore a constant in time.

But what does all this have to do with conservation of electric charge, where we started at the beginning? Suppose these particles carry electric charge $q$ , and therefore the anti-particles carry electric charge $−q.$ Then the total electric charge of a bunch of $N+$ particles and $N−$ anti-particles is

$$
qN++(−q)N−=q(N+−N−)=qN.
$$

Thus, the same conserved charge $N$ coming from our rotation symmetry counts the total electric charge $Q=qN$ , once it’s multiplied by the unit of electric charge $q$ . After multiplying by $q,$ the densities $ρ$ and $J$ from the rotation symmetry become electric charge and electric current densities. (It's actually slightly more complicated than that in this particular example because the electromagnetic fields themselves modify the current, but let's not worry about that right now!)

Now that we’re talking about things with electric charge though, that means that in addition to our field $ϕ$ there are electric and magnetic fields floating around as well! And our Lagrangian had better incorporate all of them. In the last part of the lesson, I want to show you the Lagrangian for the full theory, including the electromagnetic fields. Exploring all the details will really require a separate lesson of its own—or several—so for now I’ll just give you a quick summary.

In our relativistic notation, we can write the Klein-Gordon Lagrangian much more compactly as

$$
L=−ημν∂μϕ¯∂νϕ−κ2ϕ¯ϕ.
$$

Remember that it’s implied that we’re summing over both $μ$ and $ν$ here. When we expand out the sum, we get the same Lagrangian as before, where $ημν$ gets all the signs to work out right. I’m also going to work in units where $c=1$ for the remainder, since that’s the standard convention in field theory and it makes the formulas look simpler.

As we’ve seen, $L$ is invariant under rotations:

$$
ϕ→e−iqαϕ,ϕ¯→eiqαϕ¯.
$$

I’ve rescaled the parameter $α$ here to $−qα$ , because $q$ is going to become the electric charge of $ϕ$ .

Electromagnetism, and the standard model as a whole, are examples of **gauge theories**, in which the defining symmetries are promoted to *local* transformations in spacetime. In other words, the gauge symmetry of electromagnetism is obtained by demanding that the Lagrangian is invariant under this rotation for any choice of $α(Xμ)$ , including one that depends on what point you’re at in space and time.

Our original Lagrangian is *not* invariant under rotations when $α$ is a function of $Xμ$ . The $ϕ¯ϕ$ term is still okay,

$$
ϕ¯ϕ→eiqα(X)ϕ¯e−iqα(X)ϕ=ϕ¯ϕ,
$$

because the factors of $e−iqα(X)$ and $eiqα(X)$ coming from $ϕ$ and $ϕ¯$ cancel each other out. But the terms with the derivatives are no longer invariant.

When $α$ was constant, we could pull the rotation right outside the derivative:

$$
∂μϕ→∂μ(e−iqαϕ)=e−iqα∂μϕ.
$$

That way the rotations canceled between $∂μϕ$ and $∂νϕ¯$ . But when $α(X)$ is a function of $Xμ$ , we’ll get additional terms from the product rule when the derivative hits the $α.$ These don’t cancel out.

The way to resolve this problem is to replace the derivative $∂μϕ$ with the **covariant derivative**,

$$
Dμϕ=∂μϕ+iqAμϕ,
$$

where $Aμ$ is a *new* field: the **electromagnetic potential**. And you’ve likely met at least its first component before:

$$
Aμ=(−V,Ax,Ay,Az).
$$

$V$ is the regular old **electric potential** —i.e. the voltage—and $A=(Ax,Ay,Az)$ is the **vector potential**, which is needed in addition to $V$ once magnetic fields are thrown into the mix. They’re related to the electric and magnetic fields by taking a few derivatives. I’ll hopefully go through those details in a later lesson.

What this covariant derivative does for us is restore the nice transformation property that leaves the Lagrangian invariant. If we require when our transformation rotates $ϕ→e−iqαϕ$ that the symmetry simultaneously acts on $Aμ$ as

$$
Aμ→Aμ+∂μα,
$$

then the covariant derivative transforms as

$$
Dμϕ→e−iqα(X)Dμϕ,
$$

just like we previously had with the regular derivative when $α$ was a constant! I’ll leave that as a little exercise for you to check. Then if we replace the ordinary derivatives with covariant derivatives in our original Lagrangian,

$$
L=−ημνDμϕ―Dνϕ−κ2ϕ¯ϕ,
$$

we get a theory that’s invariant even when $α(X)$ is a function of spacetime, because the rotations again come outside the derivatives and cancel against each other.

The result of this procedure, which just looks like a trick at first glance but has deep theoretical underpinnings, is that the field $ϕ$ now carries electric charge $q$ , and $ϕ¯$ carries charge $−q$ . The Noether current is now a source for the electromagnetic field, just like any electric charges and currents would produce electric and magnetic fields according to Maxwell’s equations.

But speaking of Maxwell’s equations, there’s still one thing missing from our Lagrangian. Maxwell’s equations determine how electric and magnetic fields are produced by charges and currents, and how they evolve with time. They’re the equations of motion for the electromagnetic potential $Aμ$ , just like the Klein-Gordon equation was the field equation for $ϕ.$ Then there should be terms for $Aμ$ in the Lagrangian that give us Maxwell’s equations when we apply the principle of least action.

Again, I’m just going to quickly tell you the answer right now, and we can explore it more in the future. The Lagrangian for pure electromagnetism is

$$
LEM=−14FμνFμν,
$$

where the electromagnetic **field strength** $Fμν$ is defined by

$$
Fμν=∂μAν−∂νAμ.
$$

It’s a 4x4 matrix that packages up the electric and magnetic fields in a particular way:

$$
Fμν=(0−Ex−Ey−EzEx0Bz−ByEy−Bz0BxEzBy−Bx0).
$$

And $Fμν$ with its indices up is another shorthand: it’s what we get by matrix multiplying with $η$ to “raise the indices,” $Fμν=ημρFρσησν.$ It looks like something fancy, but again the point is just to take care of those pesky relative minus signs between time and space terms that always come up in special relativity.

All together then, the Lagrangian for the electromagnetic potential $Aμ$ and our electrically charged field $ϕ$ is

$$
L=−Dμϕ―Dμϕ−κ2ϕ¯ϕ−14FμνFμν.
$$

If all this is new to you, then this is a lot of information to try to process at once. So just take it as a teaser for future lessons where we can dive into more of the details.

Speaking of which, let me finish with one last teaser. What we’ve been talking about this lesson by putting the Klein-Gordon theory together with electromagnetism is a good example for starting to learn the ideas of symmetries and gauge theory without too many extra technical complications. And it is physically relevant for the piece of the standard model Lagrangian that describes the Higgs boson, which is a generalization of this theory.

But the most fundamental theory of electromagnetism is quantum electrodynamics (QED), which was the first piece of the standard model to be constructed, and that’s the theory of the electron field and the electromagnetic potential. And the electron is not described by a scalar field $ϕ$ —it’s described by a **spinor** field $Ψ$ . The Lagrangian for QED is

$$
L=iΨ¯γμDμΨ−mΨ¯Ψ−14FμνFμν.
$$

The ideas we’ve learned here go over directly to QED. It starts with the theory of a free electron, which has a $U(1)$ rotation symmetry. We gauge the symmetry by replacing the ordinary derivative with a covariant one, which means that the field becomes electrically charged. And then we add on the Lagrangian for the electromagnetic field itself.

The other factors of the standard model generalize this procedure, with more fields and a larger gauge symmetry, $SU(3)×SU(2)×U(1).$ Things get quite a bit more complicated though when the symmetry gets bigger than $U(1)$ ! But the same basic principle of gauge symmetry persists and is fundamental to the construction of everything we know about particle physics.

---

See also:

- [Field Theory Fundamentals](https://www.physicswithelliot.com/fields-mini-notes)
- [Noether’s Theorem Explained](https://www.physicswithelliot.com/noether-mini-notes)
- [The Hamiltonian Noether Theorem](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes)
- [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [The Special Relativistic Action](https://www.physicswithelliot.com/special-relativity-action-mini-notes)
- [The General Relativistic Action](https://www.physicswithelliot.com/gr-action-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).