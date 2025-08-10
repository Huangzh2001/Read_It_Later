---
date: "2025-08-10T22:16:14+08:00"
url: "https://www.physicswithelliot.com/resistor-ladder-classic-notes"
status:
---
## The Infinite Resistor Ladder Puzzle: Classic Physics Problem

![](https://www.youtube.com/watch?v=rqckorUt2ck)

![](https://www.physicswithelliot.com/s/resistor-ladder.png)

You may have learned about combining resistors in series and in parallel when you covered circuits in your intro physics classes. But what if put together an *infinite* number of resistors? A classic physics puzzle is to consider an infinitely long chain of resistors, strung together to form a ladder shape like above. The question is to find the total, effective resistance of the whole ladder. In other words, if we hooked up a battery of voltage $V$ between the two left ends of the ladder and measured the current $I$ coming out of it, we want to figure out the resistance $Reff$ that would show up in Ohm's law for the circuit, $V=IReff.$

![](https://www.physicswithelliot.com/s/resistors.png)

To understand this problem we really just need to know the rules for adding resistors in series and in parallel. If we have two resistors $R1$ and $R2$ arranged back-to-back in a circuit, then they behave the same as if we had a single resistor with the "effective resistance" $Reff=R1+R2$ . We say that the resistors are "in series" with each other. The reason is that the same current $I$ is flowing through both resistors, and so the total voltage drop across the pair of them is

$$
V=IR1+IR2=I(R1+R2)=IReff,
$$

the same as if we only had one resistor $Reff=R1+R2$ .

On the other hand, if the two resistors are instead arranged side-by-side, the rule for combining them is different: their *reciprocals* add, meaning that $1Reff=1R1+1R2$ . We say that these resistors are "in parallel." This time it's the voltage across each resistor that has to be the same; the currents $I1$ and $I2$ don't have to be equal, they just have to add up to the total current $I$ flowing in from the top. Then

$$
I=I1+I2=VR1+VR2=VReff,
$$

and so the effective resistance obeys $1Reff=1R1+1R2$ like we claimed.

For identical resistors $R1=R2=R$ , in series we get an effective resistance of $2R$ and in parallel we get $R2.$ Notice that the effective resistance of the two in parallel is *smaller* than the original resistors, while in series the resistance gets larger.

In our problem, we have a bunch of resistors combined up in series and in parallel to form this infinite ladder shape. And we want to answer the same question as for these little two-resistor combinations: what is the total effective resistance $Reff$ of the whole chain?

First of all, what do we roughly expect to get for the total resistance? For one thing, it will of course be proportional to $R$ , because that's the only thing with units of resistance in the problem. Second, the two resistors at the far left of the ladder are in series with the rest of the circuit to the right. So the total resistance will be equal to the contribution $2R$ from those two resistors, plus the contribution from the rest. The "rest" is an infinite number of resistors in parallel with the remaining leftmost resistor $R$ , and so that will contribute something less than $R$ to the total. So, the effective resistance should be somewhere between $2R$ and $3R$ .

![](https://www.physicswithelliot.com/s/resistor-block-one.png)

When I look at this problem, my first inclination is to think iteratively: break up the ladder into three-resistor "blocks," and ask what happens when we have one block, or two blocks, or three blocks strung together. The whole ladder is built up out of an infinite number of these blocks.

Well, one block is of course very simple: we just have three identical resistors $R$ connected in series, and so the total resistance is $R+R+R=3R.$

![](https://www.physicswithelliot.com/s/resistor-block-two.png)

Now what about two blocks? This looks a little more complicated. Can we really understand it just using the series and parallel combinations we talked about before? We can! To make it more obvious though, it helps to bend the wires around to make the circuit look like a more straightforward arrangement of series and parallel resistors. The three rightmost resistors are in series, so they combine up into $3R$ . Then that $3R$ resistance is in parallel with a single resistor $R$ , and so they combine into

$$
13R+1R=43R⟹34R.
$$

Finally, this $34R$ resistance is in series with two $R$ 's,

$$
34R+R+R=114R.
$$

Let's let $RN$ denote the effective resistance of $N$ blocks connected together. So what we've found so far is that $R1=3R$ and $R2=114R.$

![](https://www.physicswithelliot.com/s/resistor-block-three.png)

Now what if we go up to three blocks? Think about adding on this third block to the left of our previous two-block circuit. It puts the two-block circuit in parallel with a single resistor $R$ , and then adds on two more resistors in series with that. So instead of calculating the whole three-block resistance from scratch, we can use what we already learned by writing

$$
R3=2R+(1R+1R2)−1.
$$

Plugging in $R2=114R$ , I get $R3=4115R$ . But those particular fractions don't matter too much to us here. The thing we wanted to notice is this recursive pattern, that lets us write the resistance for the ladder with $N$ blocks in terms of the resistance $RN−1$ with one less block, connected up with three more resistors:

$$
RN=2R+(1R+1RN−1)−1.
$$

This is called a **recursion relation**. It tells us how to get $RN$ from $RN−1$ , and likewise we could use it to get $RN−1$ in terms of $RN−2$ , and so on. And since we know the resistance of a single block, $R1=3R$ , we can use the recursion relation to go from $R1$ to $R2,$  $R2$ to $R3$ , $R3$ to $R4$ , and so on, all the way up to $RN$ . So it's a well-defined equation with a unique solution.

We're looking for the resistance of the infinitely long ladder, which means we want to set $N=∞$ ! How are we supposed to make sense of that though?

The key insight is that when you have an infinitely long ladder, you can add one more block to it and it will still be infinite! So adding one block doesn't change the total resistance of the infinite ladder. As another way of saying the same thing, if we plug $N=∞$ into our recursion relation, we get an equation relating $R∞$ to $R∞−1$ . But $∞−1$ is still infinity! So this equation relates $R∞$ to itself:

$$
R∞=2R+(1R+1R∞)−1.
$$

Rearranging a little bit, this gives us a quadratic equation for $R∞$ :

$$
R∞2−2RR∞−2R2=0.
$$

The solution is

$$
R∞=(1+3)R.
$$

There it is! That's the resistance of the infinite ladder. Numerically, $1+3≈2.73,$ which is consistent with our expectations from earlier that the total would be between $2R$ and $3R$ .

What if we want to know the resistance of the finite ladder with $N$ blocks? The solution to our recursion relation from earlier is

$$
RN=(1+3+23(2+32−3)N−1)R,
$$

as you can check. In the limit that $N→∞$ , the big fraction is going to zero, so we again find $R∞=(1+3)R.$

---

[↩ Back to all notes](https://www.physicswithelliot.com/all-notes)

If you encounter any errors on this page, please let me know at [feedback@PhysicsWithElliot.com](https://www.physicswithelliot.com/).