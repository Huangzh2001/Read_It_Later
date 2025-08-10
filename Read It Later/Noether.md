---
date: "2025-08-10T22:09:05+08:00"
url: "https://www.physicswithelliot.com/noether-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=O0NYaO_OnH4)

In this physics mini lesson I’m going to tell you about one of the most beautiful love stories in the universe. It’s about the relationship between symmetries and conservation laws in physics, and we call it Noether’s theorem.

But seriously, Noether’s theorem is one of the most profound results in physics, and it reflects a deep connection between these two separate concepts—symmetries of nature and conserved quantities—that isn’t at all obvious at first glance.

You probably encountered several examples of conserved quantities already in your very first physics class. When studying projectile motion, for example, you can show that the total energy $E$ —kinetic plus potential—is a constant, independent of time. That's what a conserved quantity is: a function that takes the same value at any instant along the trajectory of a particle (or system). Other examples you might have run into are the total momentum and total angular momentum of an isolated system.

On the other side of Noether's theorem are symmetries. For example, if you think about the gravity field of a pointlike star or the electric field of a charged particle, it appears the same no matter what direction you look at it from. That's an example of spherical symmetry. You can pick up the system and rotate it around anyway you like, but it won't change anything about the physics. We therefore call this kind of symmetry **rotation invariance**.

Other examples of symmetries are **spatial translation invariance**, meaning if you can pick your experiment up and move it over to another lab—or another corner of the universe if you like—without any consequences, and **time translation invariance**, meaning that the laws of physics look the same yesterday as they do today and as they will tomorrow.

Physicists are obsessed with symmetries. When you hand a physicist a new theory, the first thing they're likely to do is to try to find as many symmetries in it as they can. It's symmetry that enables us to solve the quantum mechanics of the hydrogen atom, to write down the spacetime geometry around a spherically symmetric black hole, to classify the kinds of particles that appear in the standard model of particle physics.

And in this enormously important subject of symmetry, the central pillar is this theorem, due to the German mathematician Emmy Noether from about a hundred years ago. Noether's theorem says that for every continuous symmetry you can find in a theory, there will be a corresponding conserved quantity. The two go hand-in-hand.

For example, the rotation invariance we were just talking about is what leads, by Noether's theorem, to the conservation of angular momentum. Likewise, spatial translation symmetry is what's responsible for momentum conservation. And time translation symmetry is the source of energy conservation.

In this lesson I'm going to show you how Noether's theorem works. It's easiest to understand in the Lagrangian formulation of mechanics, so you'll probably want to have seen at least [one](https://www.physicswithelliot.com/least-action-mini-notes) of my [earlier](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes) videos explaining how Lagrangians work. But you don't have to be an expert, and I'll try to make the lesson as accessible as possible.

Okay, let's start out by thinking about the simplest possible set up: a single particle moving in one dimension. We define the Lagrangian by taking the difference between the kinetic energy and potential energy:

$$
L=12mx˙2−U(x),
$$

and the action is the integral of the Lagrangian over time.

According to the principle of least action, the particle is going to choose the path $x(t)$ for which $S$ is minimized, or at least extremized. Let's quickly review how that works, since we're going to follow the same line of reasoning in a second to derive Noether's theorem.

![](https://www.physicswithelliot.com/s/wiggles.png)

If we take our path $x(t)$ and make a tiny deformation of it by adding some wiggles, $x(t)→x(t)+ε(t)$ , then if we're sitting at a minimum of $S$ it shouldn't change at all at leading order in $ε$ . That's the defining property of an extremal point—when you take a little step away your function is constant because you were sitting at a point where the rate of change of the function vanished.

When we make a little change in $x(t)$ we can first find the change in the Lagrangian by taking the differential, like we learned in the principle of least action video:

$$
dL=2⋅12mx˙⋅ε˙−U′(x)⋅ε.
$$

Then in our usual routine for finding the equation of motion, we integrate the first term by parts:

$$
mx˙ddtε=ddt(mx˙ε)−mx¨ε.
$$

That let's us pull out a common factor of $ε$ :

$$
dL=−(mx¨+U′(x))ε+ddt(mx˙ε).
$$

Now when we integrate this to get the change in the action, the second term doesn't contribute anything because we assume that $ε(t)$ vanishes at the initial and final times, so that the deformation doesn't change the endpoints of the trajectory. Then the fact that the integral of the first term must vanish for any $ε(t)$ means that the thing multiplying it has to be zero:

$$
mx¨+U′(x)=0,
$$

which we recognize as $F=ma$ for a particle in a potential $U$ , where $F=−U′(x).$ That's how we derive the equation of motion from the principle of least action.

But our formula above for the change in the Lagrangian is more general than that. We'd had in mind a deformation $x(t)→x(t)+ε(t)$ where $ε(t)$ is an infinitesimal function of $t$ which vanished at the starting and ending times. But we didn't make any assumptions in computing $dL$ (other than $ε$ being infinitesimal). $ε$ could have been any function in that formula—even a function of $x$ itself.

So to avoid confusion with the special case we had in mind for the principle of least action, let me rewrite the transformation as $x→x+η$ , where $η=η(x,t)$ is any infinitesimal function of $x$ and/or $t$ . Then the same argument as above shows that the resulting change in the Lagrangian takes the form

$$
dL=−(EOM)η+ddt(mx˙η),
$$

where by $EOM$ I mean $mx¨+U′(x)$ —the thing that vanishes when $x(t)$ is the physical trajectory.

Now this brings us to symmetries, conservation laws, and Noether's theorem. A **symmetry** is an infinitesimal transformation $x→x+η$ of the coordinates *that leaves the Lagrangian invariant*. (There are more general kinds of symmetries, but these are the simplest, so let's start here.) So for these very specific transformations, which will depend on the details of the Lagrangian for the problem at hand, we have $dL=0$ .

Again, our formula for $dL$ above holds for any deformation $x→x+η$ of any path $x(t)$ —not necessarily the actual physical solution. But if *$x(t)$ does* satisfy the equation of motion, then the first term on the right-hand-side is zero.

Therefore, for a symmetry transformation $x→x+η$ (meaning $dL=0$ ) of the trajectory that satisfies the equation of motion (meaning $EOM=0$ ), we learn that

$$
ddt(mx˙η)=0.
$$

The quantity $Q=mx˙η$ is therefore a constant, independent of time!

This is **Noether's theorem**. For every infinitesimal symmetry of the Lagrangian, we obtain a **conserved quantity** $Q$ : $dQdt=0.$

Let's start with the simplest example: a free particle. (Don't worry we'll get to more interesting examples in a second.) Then $U(x)=0,$ and the Lagrangian is just

$$
L=12mx˙2.
$$

Since it's only the derivative $x˙=dxdt$ of $x(t)$ that appears in the Lagrangian, there's one symmetry that's particularly easy to spot: we can shift $x$ by any constant without changing $L$ . This symmetry is called (spatial) **translation invariance**: $x→x+η0$ where $η0$ is a constant. It means that can pick up our particle and slide it over to a new point without changing anything significant. Noether's theorem tells us that $mx˙η0$ is therefore conserved, and since $η0$ is an arbitrary constant we can discard that factor and learn that $mx˙$ is itself a constant.

Thus, the spatial translation invariance of a free particle implies that the particle's momentum $mx˙$ is conserved. Momentum conservation is due to translation symmetry in space!

But okay, a free particle isn't all that interesting. What happens when we turn a potential $U(x)$ on? Now the change in the Lagrangian under a translation $x→x+η0$ is

$$
dL=−U′(x)η0,
$$

and so we only have a symmetry if $U′(x)=0$ —i.e. if the potential is a horizontal line. But that just gives us back a free particle, so we learn that translation invariance is broken if our single particle is moving in a non-trivial potential.

But that's exactly what we should expect! If we turn on a potential $U(x)$ , then our particle will be subject to a force $F=−dUdx$ , and Newton's second law says that the force on the particle equals the rate of change of its momentum. So the momentum isn't constant anymore because there's a force acting on the particle.

![](https://www.physicswithelliot.com/s/mass-spring.png)

For example, say that $U(x)=12k(x−l)2$ was the harmonic oscillator potential energy. Then the Lagrangian $12mx˙2−U(x)$ describes a particle attached to a spring. But of course this system is not translation invariant! If you pick up the mass and slide it around, you'll stretch or compress the spring and therefore change the system! So there's no translation symmetry, there's a force on the mass, and momentum is not conserved.

![](https://www.physicswithelliot.com/s/two-mass-spring.png)

On the other hand, say we had *two* masses connected by a spring. Now if we pick up the whole system—both masses, the spring, everything—and slide them around without changing their *relative* positions then nothing's really different. So the *system* is translation invariant. Then Noether's theorem says that the *total* momentum of the system is conserved, as you should show for yourself by a similar kind of reasoning like we went through above.

And again that's what we expect from Newton's law. Remember that Newton's second law for a system says that the total *external* force equals the rate of change of the total momentum. A system with no external force on it is called *isolated*, and therefore the total momentum of an isolated system is a constant. And indeed our two masses connected by a spring is an isolated system—the spring force is internal because it acts between two components of the system.

![](https://www.physicswithelliot.com/s/2d-mass-spring.png)

Let's go back to our one particle mass-on-a-spring example, but this time let's graduate to two dimensions. So now we have something like a hockey puck on a frictionless ice rink, attached to a spring that's fixed in the center of the rink.

Once again momentum is not going to be conserved because the system is not translation invariant. If you try to pick up the particle and slide it around, you'll stretch the spring and change the system. However, if you were to *rotate* the mass around on a circle, you would keep the length of the spring fixed. We therefore have *rotational* symmetry.

Let $(x,y)$ be the coordinates of the mass. Then the spring potential energy is $U=12k(x2+y2−l)2,$ since $r=x2+y2$ is the length of the spring. But that suggests that we might be better off using polar coordinates, $r$ and $θ$ . Then $U=12k(r−l)2.$

As for the kinetic energy $12m(x˙2+y˙2),$ that gets contributions now from the speed in both the $x$ and $y$ directions. Or in polar coordinates, we can write the same thing as $12m(r˙2+r2θ˙2).$ The first term comes from the speed in the radial direction, and the second term comes from the angular speed ( $rθ˙$ is just your old friend $v=ωr$ from circular motion, where $ω=θ˙$ ).

Then the Lagrangian is

$$
L=12m(r˙2+r2θ˙2)−12k(r−l)2.
$$

Remember how we saw for a free particle at the beginning that because the Lagrangian $12mx˙2$ only depended on the derivative of the coordinate, it was therefore invariant when we shifted $x$ by a constant.

Well this Lagrangian looks a little more complicated, but notice that there aren't any $θ$ 's anywhere—only $θ˙$ . Therefore we have a symmetry that shifts $θ$ by a constant, $θ→θ+η0.$ This is a rotation! And indeed we would find rotation invariance for *any* potential $U(r)$ that doesn't depend on $θ.$ If the potential is only a function of how far you are away from the origin, then you can rotate around it at will. The same goes for a particle orbiting a star or an electron in the electric field of a proton, for example.

You can find the conserved quantity that goes along with this symmetry in the same way we did for the free particle. Translation symmetry in $x$ meant that the momentum $mx˙$ was conserved. Rotation symmetry in $θ$ means that the *angular* momentum $mr2θ˙$ is conserved! You can also see that directly from the Euler-Lagrange equation:

$$
ddt∂L∂θ˙=∂L∂θ.
$$

Whenever a coordinate doesn't appear in the Lagrangian, the right-hand-side automatically vanishes. Then this equation says that $∂L/∂θ˙=mr2θ˙$ is automatically a constant. Remember that this quantity is what we called the generalized momentum corresponding to the given coordinate. So whenever a coordinate doesn't appear in the Lagrangian, the system is invariant under shifts of that coordinate, and the corresponding generalized momentum will be conserved.

You can likewise show that *time* translation invariance is responsible for *energy* conservation. And these relationships among spatial translations, rotations, and time translations with momentum, angular momentum, and energy conservation are very general.

This is the beautiful way of understanding the world that Noether's theorem grants us. Conserved quantities like energy and momentum aren't random coincidences that occasionally show up and just make it easier to solve problems. They reflect deep symmetry properties about whatever system we're studying.

If you keep studying physics, you'll find that symmetry principles play an ever more important role in our understanding of nature, and Noether's theorem is therefore a monumentally important result.

---

See also:

- [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)
- [The Hamiltonian Noether Theorem](https://www.physicswithelliot.com/hamiltonian-noether-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).