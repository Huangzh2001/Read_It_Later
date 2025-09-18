---
date: "2025-08-10T22:11:01+08:00"
url: "https://www.physicswithelliot.com/string-action-mini-notes"
status:
---
## The First Thing You’ll Learn in a String Theory Class

![](https://www.youtube.com/watch?v=KpIaWiWvuRs)

String theory has a reputation for being a very challenging subject—and when you get deep into the details it is!—but the basic idea is very natural and is a fairly straightforward generalization of what you've been learning if you've been following along with the [last few lessons](https://www.physicswithelliot.com/least-action-mini-notes) I've shared about the [principle of least action](https://www.physicswithelliot.com/special-relativity-action-mini-notes) for a particle in Einstein's theory of [relativity](https://www.physicswithelliot.com/gr-action-mini-notes).

We've been learning that the action for a particle in Einstein's theory has a very simple and geometric interpretation. As a particle travels around through spacetime, it traces out a curve that's called its worldline. Then the action is equal, up to some factors, to the length of the worldline, and the principle of least action says that the particle will choose the shortest path that it can in traveling between two events.

[[Read It Later/attachments/d9f99578d864269af8c91df8dc0f9351_MD5.png|Open: d9f99578d864269af8c91df8dc0f9351_MD5.png]]
![[Read It Later/attachments/d9f99578d864269af8c91df8dc0f9351_MD5.png]]

*String* theory replaces the fundamental role of a particle with a tiny loop of string. Whereas a particle traces out a one-dimensional curve as it moves through spacetime, a string traces out a two-dimensional *surface*. The particle's curve we called the worldline; the string's surface we call the worldsheet.

Picture something like the surface of a bubble as you wave a bubble wand around through the air. The rim of the wand is the string in this analogy, and the bubble that's trailed out behind it as you wave the wand is the worldsheet.

Now we want to write down a principle of least action for this string. If the natural action for a particle was simply the length of its worldline, then the most obvious generalization for the string is the *area* of its worldsheet.

So in this lesson, I'll show you how we can express the action for a string as the area of the worldsheet that it traces out in spacetime, and we'll learn some very cool math about the geometry of surfaces along the way.

First of all, let's forget about string theory and Minkowski spacetime and all that, and just figure out the little bit of math that we need to compute the area of a surface. Picture that bubble wand again. As you wave it around through the air, the bubble that trails behind it is a 2D surface embedded in 3D space.

[[Read It Later/attachments/7a85ebf1d85277a5a905200b85e95e45_MD5.png|Open: 7a85ebf1d85277a5a905200b85e95e45_MD5.png]]
![[Read It Later/attachments/7a85ebf1d85277a5a905200b85e95e45_MD5.png]]

Let's write the coordinates of space as $X→=(x,y,z)$ . If we'd had a line in space instead of a surface, we would describe it by specifying a curve $X→(λ)$ , where $λ$ is some parameter along the curve. This function tells us how each point $λ$ in parameter space gets mapped to a point $X→(λ)$ in 3D space.

[[Read It Later/attachments/085759f6f2dc4e28c4d3cb6d7b5d32cf_MD5.png|Open: 085759f6f2dc4e28c4d3cb6d7b5d32cf_MD5.png]]
![[Read It Later/attachments/085759f6f2dc4e28c4d3cb6d7b5d32cf_MD5.png]]

Now when we graduate to our 2D surface instead of a curve, we need another parameter, call it $σ$ , say. Then we specify the surface by a function $X→(σ,λ)$ that tells us how each point $(σ,λ)$ in the now 2D parameter space gets mapped to a point $X→(σ,λ)$ in 3D space.

Think of the $σ$ direction as a circle and the $λ$ direction as a line, so that together the parameter space is the surface of a cylinder. When $X→(σ,λ)$ maps the cylinder into 3D space, it can get warped around to make a curvy surface like, well, a bubble.

So the question we need to answer is, if someone hands us a surface by writing down its function $X→(σ,λ)$ , how do we compute its area? Think about a little rectangular area of the parameter space, of width $dσ$ and height $dλ$ . That little region will map to another little region of the surface in 3D space, of some tiny area $da$ . This region doesn't have to be a rectangle anymore, since the map by $X→$ can distort the shape, so in general it will be some parallelogram.

[[Read It Later/attachments/a92ab9a705716e9bcb93aa0a4aa1a60a_MD5.png|Open: a92ab9a705716e9bcb93aa0a4aa1a60a_MD5.png]]
![[Read It Later/attachments/a92ab9a705716e9bcb93aa0a4aa1a60a_MD5.png]]

The length of the sides of this parallelogram should be fixed by the lengths $dσ$ and $dλ$ that we started with, along with the given map $X→$ . What are they? The bottom left corner of the rectangle was at $(σ,λ)$ , and gets mapped to $X→(σ,λ)$ . The bottom right corner was at $(σ+dσ,λ)$ , and gets mapped to $X→(σ+dσ,λ)$ . So we can draw a vector along the " $σ$ " side of the parallelogram from $X→(σ,λ)$ to $X→(σ+dσ,λ)$ :

$$
X→(σ+dσ,λ)−X→(σ,λ).
$$

If we divide this vector by $dσ$ , then we just get the derivative of $X→(σ,λ)$ in the direction of $σ$ :

$$
X→(σ+dσ,λ)−X→(σ,λ)dσ=∂X→∂σ.
$$

The curly $∂$ 's here stand for partial derivatives; if you haven't seen them in your math classes before don't worry too much about it. They're just like regular old derivatives, except that our function $X→(σ,λ)$ depends on more than one variable, so we use the partial symbol to indicate that we're only looking at the rate of change with respect to one of them.

So, we have a vector pointing along one side of the parallelogram given by

$$
dσ∂X→∂σ
$$

and likewise the vector along the other side will be

$$
dλ∂X→∂λ.
$$

And now we just have a little geometry problem. If you have two vectors, $A→$ and $B→$ , and you want to know the area of the parallelogram they make, how do you get it? It's the length of one side, $A$ say, times the height of the parallelogram, which is $Bsin⁡(θ)$ , where $θ$ is the angle between the two vectors. So the area of the parallelogram is

$$
area=ABsin⁡(θ),
$$

which you might recognize as the magnitude of the cross product $A→×B→$ . We can rewrite this more conveniently as

$$
area2=A2B2(1−cos2⁡(θ))=A2B2−(A→⋅B→)2,
$$

where I used the dot product $A→⋅B→=ABcos⁡(θ)$ . So, the area of a parallelogram spanned by two vectors $A→$ and $B→$ is

$$
area=|A→|2|B→|2−(A→⋅B→)2,
$$

where $|A→|2=A→⋅A→$ denotes the magnitude squared of $A→$ .

Back on our surface, the area of our little piece of the bubble spanned by $A→=dσ∂X→∂σ$ and $B→=dλ∂X→∂λ$ is

$$
da=|dσ∂X→∂σ|2|dλ∂X→∂λ|2−(dσ∂X→∂σ⋅dλ∂X→∂λ)2.
$$

This looks like a bit of a mess, but we can simplify it a lot. First of all, each term has a factor of $(dσdλ)2$ ; let's pull that outside the square-root:

$$
da=dσdλ|∂X→∂σ|2|∂X→∂λ|2−(∂X→∂σ⋅∂X→∂λ)2.
$$

Now let's define a $2×2$ matrix $h$ like so:

$$
h=(|∂X→∂σ|2∂X→∂σ⋅∂X→∂λ∂X→∂σ⋅∂X→∂λ|∂X→∂λ|2).
$$

Then notice that the quantity inside the square-root is nothing but the determinant of this matrix! So we can write our formula for the little bit of area $da$ much more compactly as

$$
da=dσdλdet(h).
$$

Areas (and volumes and so on) can always be written like this. $h$ is the *metric* on the surface, just like the metrics $ημν$ and $gμν$ that we encountered in the previous lessons on special and general relativity. Metrics, remember, tell us how to measure distances in a given space, so naturally they also tell us how to measure areas. The result is that the area is determined by the square-root of the determinant of the metric. To get the total area, we sum up all these little parallelograms:

$$
∫da=∫dσdλdet(h).
$$

Okay, that was the math that we needed to cover. Now let's get back to the physics. We were thinking here of a bubble getting traced out in 3D space as you wave the wand around. Now it's a short step to the worldsheet of a little loop of string that gets traced out as it evolves in *spacetime*.

We only need to make a couple of modifications here to write down the area of the worldsheet. First of all, instead of the 3-component vector $X→$ giving coordinates in 3D space, we need the 4-component vector $Xμ$ that gives coordinates on spacetime, just like we used in the previous mini lesson on relativity. Likewise, we need to replace the familiar "Pythagorean" notion of distance in regular space with the Minkowski metric $ημν$ in spacetime. (We could also pick a curved metric $gμν$ like in general relativity, to describe a string in a curved spacetime, but let's stick to flat spacetime here to keep things simple.)

That affects all the places we computed the magnitude and dot products of vectors. So our new matrix $h$ is

$$
h=(ημν∂Xμ∂σ∂Xν∂σημν∂Xμ∂σ∂Xν∂λημν∂Xμ∂σ∂Xν∂λημν∂Xμ∂λ∂Xν∂λ).
$$

One last thing: just like when we wrote down the length of the particle's worldline, $∫−ds2$ , we had to flip the sign of $ds2$ before we took the square-root because it was negative. The same goes for the determinant of $h$ in Minkowski spacetime. So our formula for the area of the worldsheet that the string sweeps out in spacetime is

$$
area=∫dσdλ−det(h).
$$

This is a generalization of what we learned before for the length of the worldline. In that case, we had a curve $Xμ(λ)$ instead of a surface $Xμ(σ,λ).$ Then the $2×2$ matrix $h$ is reduced to a single entry, $ημν∂Xμ∂λ∂Xν∂λ$ . The "determinant" of a $1×1$ matrix doesn't do anything at all, it just returns that same number. And so the length of the worldline was

$$
length=∫dλ−ημν∂Xμ∂λ∂Xν∂λ,
$$

just like we wrote down last time.

The action for our point particle was $−mc$ times this length. Those constants had to be there to get the units right: the action has units of energy times time, or $kg⋅m2/s$ . So $mc$ times the length of the worldline has units

$$
kg⋅ms⋅m=kg⋅m2s
$$

like we wanted.

As for our string, we can write the action as

$$
S=−Tc∫dσdλ−det(h),
$$

where $T$ is the *tension* in the string. The units are

$$
Nm/s⋅m2=N⋅m⋅s.
$$

Newtons times meters give us energy, and so we indeed get the right units for the action.

So there we have it! This is the action for a relativistic string. The principle of least action says that the string will evolve along the worldsheet with extremal area, similar to how a particle picks the worldline with extremal length.

You can derive the resulting equation of motion for the string in the usual way, by making a small variation of the surface $Xμ$ and demanding that the action doesn't change to leading order. The solutions are called *harmonic functions*, which are very special and show up in a wide variety of contexts.

So that's the beginning of string theory—it's called the Nambu-Goto action for a relativistic string. And it's safe to say that that's just the tip of the iceberg for string theory. But if you've stuck with me this far you've already got a good head start on the subject.

---

See also:

- Part 1: [Explaining the Principle of Least Action](https://www.physicswithelliot.com/least-action-mini-notes)
- Part 2: [The Special Relativistic Action, Explained](https://www.physicswithelliot.com/special-relativity-action-mini-notes)
- Part 3: [How Einstein Uncovered the Path a Particle Traces Through Spacetime](https://www.physicswithelliot.com/gr-action-mini-notes)
- [Lagrangian and Hamiltonian Mechanics in Under 20 Minutes](https://www.physicswithelliot.com/lagrangian-hamiltonian-mini-notes)

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).