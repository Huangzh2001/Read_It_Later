---
date: "2025-08-10T22:14:52+08:00"
url: "https://www.physicswithelliot.com/buoyant-help-room-notes"
status:
---
## How Archimedes Cleverly Solved the Buoyant Force Puzzle 2000 Years Ago: Physics Help Room

![](https://www.youtube.com/watch?v=B8vYGd1kV-Q)

I think just about every kid in a swimming pool has tried to tackle something like a floating beach ball and force it all the way under the water. But the harder you try to force the ball underwater, the harder the water seems to want to force the ball out! What determines how much of the ball actually wants to sink below the surface? Likewise, how much of an iceberg lies above the surface of the ocean, and how much is lurking below? These questions come down to understanding the buoyant force: the force that a fluid like water exerts on an object that's floating in it. There's a beautiful and simple argument for figuring out the buoyant force that goes all the way back to the great Greek mathematician Archimedes over 2000 years ago, and is often called Archimedes' principle.

![](https://www.physicswithelliot.com/s/duck.png)

So let's say that we have a big pool of fluid. This could be something like a swimming pool, or the ocean, or a pot of cooking oil. And then suppose you rest an object on the surface of the fluid and it floats, like a rubber ducky on the surface of a bath. Say that the water is still, and the duck is floating at rest.

The duck of course has some weight $mg$ pulling it down. But since it's sitting at rest, there must be an opposite force from the water pushing up on it. That's what we call the **buoyant force** $FB$ . In equilibrium, the buoyant force must equal the weight of the duck. But how do we figure out how much of the duck has sunk below the surface of the water? And we know from experience that if you go and try to push the duck deeper down under the water, the buoyant force pushing back up is going to get even bigger. We want to be able to compute the buoyant force as a function of how deep underwater the duck is.

![](https://www.physicswithelliot.com/s/normal-force.png)

The buoyant force is a lot like the normal force that a table exerts on a block that's resting on it. The actual microscopic origins of the normal force are very complicated—it comes from all the little atoms in the table bumping up against all the little atoms in the block. But when we zoom out the macroscopic effect is very simple: there's a net upward force on the block that counteracts its weight, and keeps it from falling through the table.

Likewise, there are some very complicated interactions between the little atoms of the fluid which bump up against the atoms in the duck, but when we zoom out there's a simple net result. The fluid exerts a **pressure** on the surface of the duck—pressure meaning force per unit area—like the little red arrows in the first picture. And the sum of all those pressure forces equals the total buoyant force of the water on the duck.

Since we know the buoyant force gets bigger when we try to force the duck deeper underwater, we expect that the force will depend on how much of the volume of the duck is below the surface. So let's say the volume that's underwater is $VF$ , and try to figure out the total buoyant force. There's a beautiful argument for this that's due to Archimedes.

![](https://www.physicswithelliot.com/s/buoyant.png)

We consider the pool of fluid again, but this time *without* the duck in it. I've highlighted in dark blue the region of fluid where the duck *had* been submerged—that's the volume $VF$ ( $F$ for fluid). If the density of the fluid, i.e the mass per unit volume, is a constant $ρF$ , then the mass of this highlighted volume is $ρFVF$ , and its weight is $ρFVFg$ .

The fluid itself is at rest, so this weight of the highlighted region pulling down is counteracted once again by all the little pressure forces from the rest of the fluid, which add up to the total buoyant force pushing up. Then the sum of all the pressure forces must equal the weight of the highlighted volume of fluid, $ρFVFg$ , so that the total force on it vanishes.

So now we know that the little pressure forces represented by the red arrows add up to $ρFVFg$ —the weight of the region of fluid where the duck had been. Now put the duck back in the pool. The same total force will be exerted on *its* surface. So the buoyant force on the duck (or on any object of which a volume $VF$ is submerged in a fluid of density $ρF$ ) will be

$$
FB=ρFVFg.
$$

Again, $VF$ is the volume under the surface of the fluid that's occupied by the object, and $ρFVFg$ is the weight of the fluid that *would* have been there if you hadn't set the object down. In words then, the buoyant force equals *the weight of the fluid that's been displaced by the object*.

As we expected, the buoyant force gets bigger if you force the object deeper down, because $FB$ is proportional to the volume $VF$ that's under the surface. And we also see that the denser the fluid is, the bigger the buoyant will be.

Now say we just rest the object on the surface of the fluid and it floats—so we're not trying to force it under or anything like that. Then as we knew from the beginning, by demanding that the buoyant force upward must cancel the total weight $mg$ of the object downward, we find

$$
mg=ρFVFg.
$$

Thus, the volume of an object of mass $m$ that sits below the surface of the fluid is

$$
VF=mρF.
$$

Notice that we made an assumption here that $VF$ is *big* enough that the buoyant force $ρFVFg$ can offset the weight of the object $mg$ . $VF$ is the piece of the volume of the object that sits under the surface, though, and it of course can't get any larger than the *total* volume $VS$ of the solid object. Then if the mass $m$ of the object is too large while its volume $VS$ is too small, the maximum possible buoyant force will still be less than the weight of the object, and it will sink. In other words, if the *density* $ρS=mVS$ of the object is too big, it won't be able to float on the given fluid.

We'll assume that our object has *uniform* density $ρS$ . Rubber duckies don't really qualify—maybe it's a block of ice or wood instead. The ratio

$$
f=VFVS
$$

is the *fraction* of the object that lies below the surface. We can write the total mass of the object as $m=ρSVS$ , and so plugging into our equilibrium equation we find

$$
VF=ρSρFVS,
$$

or, solving for the fraction $f=VFVS$ that's below the surface,

$$
f=ρSρF.
$$

This is a beautiful result! It says that when you float an object of density $ρS$ on the surface of a fluid of density $ρF$ , the fraction of the object that will sink under is simply the ratio of the densities.

Notice that if $ρS$ is bigger than $ρF$ , we get $f>1$ , which is nonsense since $f$ was the fraction of the object's volume that falls below the surface. Then we again see that the object can't float on the fluid if its density is bigger than the fluid density.

Sailors of course know that when you see an iceberg above the surface of the ocean, it's only a tiny fraction of a potentially huge mountain of ice that's lurking out of sight under the water, hence the expression "the tip of the iceberg." Now we're in a position to understand why. When water freezes, it expands, and so the density of ice is smaller than the density of water—that's why the iceberg floats on the ocean and the ice cubes float in your drink.

The density of liquid water is about 1000 $kg/m3$ , whereas the density of ice is about 920 $kg/m3$ . (Actually, the density of ocean water is slightly different due to the salt content, but we're just making a rough estimate here.) Then if a block of ice floats on the surface of water, a fraction

$$
f≈9201000≈92%
$$

of the ice will lie below the surface.

Then the "tip of the iceberg" that you're seeing from the side of a ship is only around 10% of the whole structure by volume. So definitely steer clear!

Another related question you can ask yourself is, if you measure the water level in a glass of ice water, wait for the ice to melt, and then measure again, will the water level have gone up, gone down, or stayed the same? Head [here](https://www.physicswithelliot.com/melting-ice-classic-notes) to learn more.

---