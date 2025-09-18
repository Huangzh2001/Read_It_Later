---
date: "2025-08-10T22:12:24+08:00"
url: "https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes"
status:
---
![](https://www.youtube.com/watch?v=0DHNGtsmmH8)

Mechanics is the study of how things move, and a typical intro physics class is all about applying Newton’s second law $F=ma$ to simple systems like pendulums, blocks on inclined planes, springs, and so on in order to learn how to predict their motion. Isaac Newton (1642-1727) was the first person to write down a systematic procedure for predicting motion when he published his “Mathematical Principles of Natural Philosophy” treatise back in 1687.

But there's a whole lot more to mechanics than just $F=ma$ , and in the years after Newton's work, new approaches to mechanics were developed, most notably by Joseph-Louis Lagrange (1736-1813) in the late 1700s and William Rowan Hamilton (1805-1865) in the 1800s. Lagrange's and Hamilton's approaches offer new practical and theoretical insights into the structure of mechanics, and they're especially relevant in the study of *quantum* mechanics, meaning the physics of very small objects like atoms and elementary particles, as opposed to the *classical* mechanics that Newton, Lagrange, and Hamilton originally studied.

I'll illustrate each approach here using the simple pendulum as an example, which consists of a particle of mass $m$ hanging from a lightweight rod of length $l$ (that we'll treat as massless) attached to a pivot at the other end.

![[Read It Later/attachments/8f28feb3b7f962fa6285db15b082e5c5_MD5.png]]

We can specify the position of the mass either by the coordinate $s$ that measures the arc length traced out by the particle or by the angle $θ$ that it makes with the vertical. They’re related by $θ=s/l$ .

**Newton’s Approach:**

Let's first briefly review how to understand the pendulum using Newtonian mechanics (for additional details click [here](https://www.physicswithelliot.com/pendulum-help-room-notes)). We start by drawing a free-body diagram to keep track of all the forces acting on the particle:

![[Read It Later/attachments/76c0fa56e70165e5426d6da9537b5a82_MD5.png]]

There are only two forces: gravity $mg$ pulling straight down and tension $T$ pulling inward along the rod toward the center of the circle.

Then Newton tells us to add up all the forces and write the **equation of motion**: $∑F→=ma→$ . This is a vector equation, but what we're really interested in here is the tangential component—that is, the component of the force and acceleration along the circle where the particle is constrained to move. The tension doesn't contribute anything here—that's pointing radially toward the center of the circle. So the relevant force is the tangential component of gravity, which, with a little geometry work, you can see is $mgsin⁡θ$ pointing back toward the pendulum's equilibrium position.

Then the $F=ma$ equation for $s$ reads

$$
ms¨=−mgsin⁡θ,
$$

where $s¨=d2sdt2$ is the acceleration of $s(t)$ . Plugging in $s=lθ$ , where $l$ is the constant length of the rod, we can write

$$
θ¨=−glsin⁡θ.
$$

This is the equation of motion for $θ$ . It's the differential equation that governs the motion of the pendulum. And it's actually pretty complicated—too complicated to write down a simple expression for the solution $θ(t)$ , in general. When $θ$ is small, though, so that the pendulum is close to equilibrium, the solution is just a sine or cosine— [click here](https://www.physicswithelliot.com/pendulum-help-room-notes) for the details. You can see what $θ(t)$ will look like for initial conditions of your choosing in [this animation](https://www.physicswithelliot.com/pendulum-graph).

**Lagrange’s Approach:**

Let's look at the Lagrangian formalism next. Whereas Newton told us to start by writing down the total force $∑F→$ , Lagrange tells us to start by writing down the kinetic energy $K$ and potential energy $U$ , and then to take their *difference*:

$$
L=K−U.
$$

$L$ is called the **Lagrangian**. It is *not* the total energy $K+U$ because of that pesky minus sign.

Let's see what the Lagrangian is for our pendulum. The kinetic energy is just $K=12mv2$ , where $v=s˙$ is the speed of the particle. Or, in terms of $θ˙=s˙/l$ ,

$$
K=12ml2θ˙2.
$$

$U$ meanwhile comes from the gravitational potential energy, which is just $mgy$ where $y$ is the height of the particle with respect to some chosen ground level. I'll put the ground level at the height of the pivot: then $y=−lcos⁡θ,$ and so the potential energy is

$$
U=−mglcos⁡θ.
$$

Then the Lagrangian for the pendulum is

$$
L(θ,θ˙)=12ml2θ˙2+mglcos⁡θ.
$$

Newton told us to compute the total force $∑F→$ and then write the equation $∑F→=ma→$ . Lagrange instructs us to compute the Lagrangian $L$ , and then write down the **Euler-Lagrange equation**:

$$
ddt(∂L∂θ˙)=∂L∂θ.
$$

The curly $∂$ 's here stand for "partial" derivatives—if you haven't seen them before don't worry; for practical purposes they behave just like regular old derivatives.

I won't get into much detail as to where the Euler-Lagrange equation comes from right now; we'll just write it down and investigate the consequences. But the short answer is that the Euler-Lagrange equation is the condition for the **action** $S$ , which is the *integral* of the Lagrangian, to be minimized:

$$
minimizeS=∫dt L⟺Euler-Lagrange eqn
$$

The claim is that of all the paths a particle could follow, the one it actually chooses is the path that minimizes (or more precisely extremizes) the action. This is known as the principle of least action, and the implication is that the trajectory satisfies the Euler-Lagrange equation because that's the condition for extremizing the action. But there's a lot to unpack there—right now I just want to show you what happens when we plug the pendulum Lagrangian into the Euler-Lagrange equation. The right-hand-side is

$$
∂L∂θ=∂∂θ(mglcos⁡θ)=−mglsin⁡θ.
$$

The kinetic energy $12ml2θ˙2$ doesn't contribute anything here because it depends on $θ˙$ , not $θ$ itself, and we treat them as independent variables when we take these derivatives.

On the left-hand-side, we need

$$
∂L∂θ˙=ml2θ˙⟹ddt(∂L∂θ˙)=ml2θ¨.
$$

$∂L∂θ˙=ml2θ˙$ is called the momentum $p$ conjugate to $θ$ , and $∂L∂θ$ is called the generalized force, because the Euler-Lagrange equation then resembles Newton's second law: rate of change of momentum = force.

Together, then, the Euler-Lagrange equation for $θ$ reads

$$
ml2θ¨=−mglsin⁡θ,
$$

which is the same thing we found earlier from $F=ma$ ! So this procedure from Lagrange remarkably gives us the same result as Newton's approach.

The Lagrangian is a very useful way of quickly getting at the equations of motion for a system—in fact it's often easier than using $F=ma.$ If I'm faced with most any mechanics problem, I'll usually start by writing down the Lagrangian. For one thing, we don't have to deal with any of the annoying vectors that show up in $∑F→=ma→$ . We can just choose whatever coordinates we like to describe our system (including, potentially, non-inertial coordinates), write down the Lagrangian $L=K−U$ , and then write the Euler-Lagrange equation for each of the coordinates. It also makes it much easier to deal with constraints and to understand symmetries, but those are topics for another day.

In the problem sheet that I linked at the top of the page, you can test yourself on these concepts by solving a more challenging problem with a pendulum that's being shaken back and forth.

### Hamilton’s Approach:

Finally, let's look at the pendulum with Hamiltonian mechanics. Instead of the Lagrangian $L=K−U$ , this time let's write down the total energy $E=K+U$ :

$$
E=12ml2θ˙2−mglcos⁡θ.
$$

Remembering that the momentum is $p=ml2θ˙$ , we can rewrite this as

$$
H(θ,p)=p22ml2−mglcos⁡θ.
$$

$H$ is called the **Hamiltonian**, and it's the starting point for Hamiltonian mechanics just like the Lagrangian is the starting point for Lagrangian mechanics. For simple systems like our pendulum, the Hamiltonian is just the total energy. More generally, it's defined by

$$
H=θ˙∂L∂θ˙−L|θ˙→p,
$$

where at the end we use the definition of the momentum— $p=ml2θ˙$ in this case—to replace all the $θ˙$ 's with $p$ 's. You can check that this indeed gives you the total energy for the pendulum. You'll need this more general definition to evaluate the Hamiltonian in the problem sheet linked at the top of the page, though.

We used the Lagrangian to write down the Euler-Lagrange equation—we use the *Hamiltonian* to write down **Hamilton's equations**:

$$
θ˙=∂H∂p,p˙=−∂H∂θ.
$$

Whereas $F=ma$ and the Euler-Lagrange equation gave us a single 2nd order differential equation, Hamilton gives us a *pair* of *1st order* equations for $θ$ and $p$ . Let's see what we get: $∂H∂p$ is just $pml2$ , and $∂H∂θ$ is $mglsin⁡θ.$ So Hamilton's equations for the pendulum are

$$
θ˙=pml2,p˙=−mglsin⁡θ.
$$

The first equation is just the definition of the momentum again, $p=ml2θ˙$ . If we take the rate of change of this equation— $p˙=ml2θ¨$ —and then combine it with the second equation, we get

$$
ml2θ¨=−mglsin⁡θ,
$$

which is once again the original equation of motion! So Hamilton's equations are equivalent to $F=ma$ and the Euler-Lagrange equation; they just split the single 2nd order equation into a pair of 1st order equations.

But what does that buy us? Hamilton's 1st order equations aren't necessarily any easier to solve than the 2nd order equation of motion. What we gain, however, is new *geometric* perspective on the mechanics of the pendulum: as the pendulum moves, we trace out a curve in the $θp$ -plane known as a flow on phase space.

To specify what the pendulum is doing at any given instant, we just need to give its position and velocity—or equivalently its position and momentum $(θ0,p0).$ With this initial data we can figure out what the pendulum is doing at any later time by solving Hamilton's equations for $(θ(t),p(t))$ . So our solution to Hamilton's equations traces out a curve in the $θp$ -plane parameterized by $t$ that starts at our initial condition $(θ0,p0)$ .

The $θp$ -plane is called the **phase space** of the system, and the curve $(θ(t),p(t))$ is called a **flow** on the phase space. These flows are very special—they won't travel along any old curve in the $θp$ -plane. In particular, because the energy of the pendulum is conserved, if we evaluate the Hamiltonian at any time $t$ along the flow, we're guaranteed to always get the same number— $H$ is a constant of the flow.

That means that whatever the initial energy $H0=p022ml2−mglcos⁡θ0$ of our starting point was, the flow will be trapped on the curve in the $θp$ -plane where the energy is $H(θ,p)=H0$ . I've drawn a few of these lines of constant energy below:

θ <sub>0</sub> = 0.40

ω <sub>0</sub> = 0.00

Drag the $θ0$ and $ω0=θ˙0$ sliders here to set the initial angle and angular velocity for the pendulum. These pick out your starting point in the phase space on the right. Then press start to let the pendulum go, and watch the phase space flow. Notice that if you drag the sliders to start the point off on one of the lines of constant energy that are drawn here, it stays trapped on that line throughout the flow because the energy is conserved.

Notice that there are two qualitatively very different types of constant energy curves here: the closed loops near the middle and the wavy lines at the top and bottom. They're separated by the pointy football shaped curve in between. What's the physical difference between these two types of curves? Try dragging the sliders to set the initial point on one of the wavy lines and then press start to watch what happens.

This is only the tip of the iceberg for Lagrangian and Hamiltonian mechanics. Not only are these fascinating and extremely useful approaches to classical mechanics, they are fundamental to the way we think about quantum mechanics. For example, functions on phase space in classical mechanics turn into *operators* on the space of quantum states in quantum mechanics. If you know the state $|ψ⟩$ of a quantum system at $t=0$ , the Schrödinger equation says that the state at a later time $t$ will be $e−iℏHt|ψ⟩$ , where $H$ is the operator version of the classical Hamiltonian function. The Lagrangian, meanwhile, appears in the path-integral formulation of quantum mechanics.

If you keep studying physics you will see Lagrangians and Hamiltonians popping up all over the place!

---

See also:

- [Explaining the Principle of Least Action: Physics Mini Lesson](https://www.physicswithelliot.com/least-action-mini-notes)
- [Everything You Need To Know About Pendulums: Physics Help Room](https://www.physicswithelliot.com/pendulum-help-room-notes)
- [Pendulum with Angle Versus Time Graph](https://www.physicswithelliot.com/pendulum-graph)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).