---
url: https://www.youtube.com/watch?v=9vFbyHNz-8g&t=70s
tags:
  - video
status: readed
date: 2025-11-20T21:26:29+08:00
---
![Renormalization: Why Bigger is Simpler](https://www.youtube.com/watch?v=9vFbyHNz-8g&t=70s)
0:00
today I would like to discuss renormalization renormalization is a set of techniques used all over in physics from particle physics to Material Science to fluid mechanics which allows

0:10
us to understand how the behavior of matter changes between different length scales in particular it can help us answer two very deep questions the first is despite the substantial

0:21
complexity and diversity of molecules and interactions that hold matter together we can usually describe the macroscopic properties of materials with only a few numbers

0:30
in order to describe the properties of even a simple molecule like water requires a significant amount of information and the interactions between molecules add an additional layer of complexity

0:39
and variability meanwhile you have a fairly good description of a material if you know it's density a handful of thermodynamic properties such as conductivity and a few mechanical properties such as

0:50
viscosity for liquids or yield strength for solids why is that the second question I want to try to answer is why the properties of the material can change very suddenly when its environment changes

1:01
ice melts water boils Metals become superconductors all at precise and specific temperatures pressures or magnetic fields why are these boundaries sharp rather than gradual

1:12
in order to answer these questions we need some way to figure out how complicated microscopic interactions average out at larger scales to determine a material's properties this

1:21
process is called reneormalization essentially the process looks something like this start with some model of our material describing how its smallest components interact in theory this model includes

1:33
all of the information needed to describe the material but it is not easy to work out what its properties are at larger scales from it since this model is made up of an extremely large number

1:42
of microscopic components that we cannot see is going to be a statistical rather than deterministic next average out the smallest scale Behavior to get a model that is valid at some intermediate scale

1:52
this is called coarse graining since we are redefining our system in terms of larger scale coarser variables and therefore losing information about the smaller scale

2:01
repeat this process until we reach the scale we would like to understand in order to figure out what we mean by averaging we first need to Define what it is we are averaging over we are

2:15
averaging Over States the system can be in weighted by the probabilities of those States if we have some closed system let's say a gas we might know things like its volume temperature and

2:25
pressure but we generally do not know what the precise location and velocity of every molecule in the system is instead based on the gases macroscopic properties we know what the probability

2:35
is of the molecules being in any particular configuration for example it is much more likely that the molecules are spread out throughout the container than that they are tightly packed into a

2:44
corner both because it takes much more energy to pack them together and because there are more ways for the molecules to be spread out in general we are going to denote the

2:54
set of variables we use to describe the particular State our system is in with the letter Phi for a gas this might be the position and velocity of every molecule for a

3:03
chemical solution it might be the concentration of each reactant at each point in space or for a magnet it might be the degree of magnetization of the material at each point in the magnet

3:12
probability of any particular state or value of Phi is given by a distribution called a Gibbs distribution the probability of a state Phi is proportional to e to the power minus H

3:23
over T where H is the energy of that particular configuration called the hamiltonian and T is the temperature the sum is taken over all possible configurations so the probabilities sum to one

3:36
this can be made somewhat more intuitive by noting that lower energy states are much more likely than higher energy ones and that high energy states become relatively likely as the temperature

3:45
increases since the denominator is just some constant that is the same regardless of what state we are looking at we will ignore it and just focus on this exponential

3:56
now we can be much more specific about what we mean by averaging or coarse graining let's say we have some State Phi that we split into a large scale part that we call 5r and some small scale part we

4:07
will call Delta Phi for now the sum is purely symbolic we will not be very rigorous about how we go about making the split but you can think of Phi bar as varying slowly and Delta Phi is

4:19
encoding whatever quickly varying information is lost in Phi bar we can now say that the probability of being in some coarse grain State Phi bar is equal to the sum of the probabilities

4:30
of being in any of the regular states that become Phi bar when coarse grained we can sum over Delta Phi instead since any Phi that goes to Phi bar can be specified by the difference between the

4:40
two which is Delta Phi the whole point of this process is to figure out how our system behaves at this larger scale so we would like to get rid of the smaller scale by

4:51
evaluating the sum over Delta Phi we want to get a result that looks like a Gibbs distribution this time with some new definition of the energy of Phi bar this is the hard part

5:05
so what does the H mean anyway H stands for hamiltonian which is just a fancy word for the total energy in the system in a particular state for example for a gas this could just be the sum of the

5:16
kinetic energies of each molecule generally though when performing renormalization it is best to work with the total energy that is in terms of an energy density a function we will denote

5:26
with a script H which just tells us the concentration of energy at each point in space we get the total energy by summing this function over every point in space which

5:35
is called an integral and is written like this a commonly used example which happens to be a fairly good model for how Metals such as iron become magnetized looks like this this might look complicated

5:46
but we don't really need to know what it means the relevant point is that it is the sum of a few terms Each of which is some function of our state variable M of X which again for a magnet represents

5:56
the magnetization of material at each point and Each of which has some coefficient in front of it the sizes of these coefficients is what determines the energy the system has in different

6:06
states and the resulting behavior of the system overall adding in additional terms adds additional Behavior to the system for example our magnet might respond to being placed in an external

6:17
magnetic field I want to make things simple for our example calculation though so we're going to stick with just these two terms and ignore the dependence of M on position writing H simply as this

6:30
now let's get back to our calculation we have a way of calculating the probability of our system being in any state in this case described by the magnetization m in terms of an

6:40
expression describing the energy of that state which is made of a couple of terms each with a coefficient in front we split M into small and large scale parts and we would like to calculate the

6:50
probability of the coarse grain State described by m bar which we know how to write in terms of the sum of probabilities of non-course grain States but we would like to do away with a

6:59
small scale and write this in terms of a new hamiltonian called h-bar we expect the physics of our system to change somewhat as we zoom out we don't expect anything really new to show up so we

7:08
want our new hamiltonian to look like our old one just in terms of M Bar instead of M and with coefficients a bar and B Bar instead of A and B how do we do that this is going to take

7:18
a decent amount of algebra to work out but I wanted to include it both to give a taste of what renormalization calculations look like and to make the answer we get seem less mysterious feel

7:27
free to skip ahead a couple of minutes if that doesn't interest you also it's all right if you don't quite follow every step along the way it will not matter much later now back to the video

7:38
so we can solve this equation for h-bar but we somehow need to evaluate this pesky sum and it isn't obvious what to do with this exponential what would be really nice is If instead of a sum of

7:49
exponential functions we had each element in the sum being itself a sum of terms each term being Delta M to some Power Times some expression involving M Bar and we could distribute the sum and find

8:00
that we can isolate each one of them a neat trick we can use to simplify this a little is to note that the odd terms equal zero we can see this by noticing that the sum includes both positive and

8:10
negative values of Delta m in a symmetric fashion and every positive value will be canceled by a negative value so we end up with only the even terms since what these sums evaluate to

8:26
depends on the details of our course grading procedure which we have been deliberately vague about we'll just name them and move on going back to our problem we can

8:35
actually get this sum into the form we want using a little trick there's a simple series representation for exponential functions that looks like this this is of course an infinite series

8:44
which can make it a little messy to work with when actually doing a calculation in detail there are various tricks to approximate the answer with only the first few terms for now let's consider

8:54
the case where the temperature T is very large so the first couple terms is a fairly good approximation on its own so let's solve this first we plug in our expression for H now we split M and expand

9:12
now as we said before terms with an odd power of Delta M will vanish and then we take the sum over the evens now we arrange this and Define some new variables dropping that factor in front the same

9:32
way we ignored the denominator earlier and finally plugging in h-bar we use our approximation of the exponential again this time in reverse and we now have what we are seeking

9:46
starting from our original description of our system we calculated a new model valid for a larger scale this is what we mean by over normalization and we call h-bar the normalized hamiltonian and a

9:57
bar and B Bar the normalized coefficients it's interesting that the expressions for both of the normalized coefficients depend on both A and B and in particular that b shows up in the numerator of a

10:08
bar there's an intuitive explanation for this the German H that has B in it has m to the fourth power when we split M into M Bar and Delta m one of the terms we get has n Bar squared so that when we

10:20
put everything together this ends up in the term with a bar what this means is that the interaction of the large-scale magnetic field M bar with a small scale magnetic field Delta

10:30
M caused by this m to the fourth term creates an effect on the large scale field that looks like the effect of an M Bar squared term once you average out Delta M and therefore adds to that term

10:45
what's nice about having these expressions for the normalized coefficients in terms of The Originals is that it lets us repeat this process indefinitely each time taking the new

10:54
set of normalized coefficients as the starting point so as we repeatedly coarse grain and zoom out the effective values of our coefficients will change if we make the

11:06
amount by which we zoom out small then each iteration will only move our coefficients a little we see that if we zoom out smoothly instead of in jumps that our position in parameter space

11:16
flows smoothly if we see how this flow moves from any initial value of our coefficients we get a vector field we call this the normalization group flow the word group is usually thrown in

11:28
there as a mathy way of saying that if we zoom out by a factor of a and then by a factor of B it's the same as zooming out by a times B going back to the renormalization flow

11:42
streamlines can't pass through one another since the vector field can only have one value at each point this means that the streamlines have a tendency to converge to the Same Direction when they

11:51
get near each other as a result as we zoom out we tend to find that we need fewer parameters to Define our system in this two-dimensional case rather than being anywhere on the plane requiring

12:02
two parameters after zooming out for a long time we can expect to be somewhere very near this line requiring only one parameter to Define our position in more than two dimensions a similar

12:15
process occurs although it is a little harder to visualize as we zoom out further and further one of two things can happen the streamlines can go out to Infinity giving infinite

12:25
values of our coefficients but this is not reasonable from a physics perspective and actually means our model is missing some effects that are important at large scale

12:33
the other option is that they can stop somewhere again because lines don't pass through each other many field lines will tend to stop on the same point or line or Surface

12:43
if the fixed points form a line then we still have one free parameter that persists at the larger scales and is determined by where we started finding where these fixed points are is

12:54
very useful since it tells us what the coefficients defining our system are when we zoom out arbitrarily far it takes zooming out a few million times to go from the atomic scale to the size

13:05
of the smallest of everyday objects so the material properties we see tend to lie very very near these fixed points and surfaces this is why things are simpler at the largest scales the more

13:16
you zoom out the more constrained the parameter space is and the more likely we are to be at a fixed Point even if we started with some very complicated Theory with many coefficients it is

13:27
likely that only a few of them remain at the largest scales as a side note this is also a source of difficulty for particle physicists they also do a kind of a normalization but their math looks

13:38
a little different because they're doing Quantum statistics their standard model of subatomic particles is very good at the scales we are able to probe so far using particle

13:46
accelerators but if there were normalization flow from even smaller scales has reduced the number of parameters it is very hard to tell what direction we came from and therefore

13:55
what might be hiding at these smaller scales this is what drives much of the theoretical work on what might exist at ever smaller scales equivalent in their case to higher energies which gives the

14:06
subfield the name high energy physics so we've answered our first question but this still leaves the question of why the large-scale properties of materials can change suddenly what we call phase

14:18
transitions we can understand this schematically with this picture let's say we have some substance whose microscopic structure can conveniently be described by only two parameters and that the

14:30
renewalization flow leads to two separate fixed points the parameters are going to vary depending on what temperature and pressure the substance is under and let's say current conditions put us over

14:40
here if we raise or lower the temperature a bit maybe that shifts us this way and this way and if we raise or lower the pressure it moves us this way and this way now something interesting can happen

14:53
here see if you can spot it let's say we steadily increase the temperature for a while the renormalization flow will take us to the same fixed point and the large scale properties that our

15:05
system stay the same however eventually we cross a boundary and now suddenly the renormalization flow takes us to a very different point in parameter space large-scale

15:14
properties of our system will abruptly change this boundary defines a phase transition and a similar boundary is what leads ice to suddenly melt at a particular temperature and pressure for water to

15:25
boil and for basically any other phase transition seen in nature to happen where this boundary line intersects different lines of constant temperature or pressure is what defines the shape of

15:38
boundaries in Phase diagrams so to summarize we defined how to describe the probability of a thermodynamic system being in a particular state in terms of the energy of that state and the temperature

15:52
we worked out how to average out the smallest scale of our system and how this changes our system's parameters we saw that repeatedly rescaling our system in this way induces a flow in parameter space

16:06
the existence of fixed points in this flow is what makes the properties of macroscopic materials simpler than their microscopic components and boundaries between regions that flow to different

16:15
fixed points are what produce the boundaries we see between phases of matter thank you for joining me in this introduction to our normalization I hope you enjoyed it

16:24
I hope to be making more videos like this soon and I plan to put a more detailed written version of this presentation on my blog the link to that will be in the video description when it is ready

16:34
so until next time