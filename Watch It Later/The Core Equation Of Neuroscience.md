---
url: https://www.youtube.com/watch?v=zOmhHE2xctw
tags:
  - video
status: reading
date: 2025-10-29T11:05:24+08:00
---
![The Core Equation Of Neuroscience](https://www.youtube.com/watch?v=zOmhHE2xctw)
0:00
the human brain remains one of science's greatest Mysteries while we have mastered the art of creating computers by arranging transistors into logical circuits understanding how neurons

0:10
compute is a lot more challenging after all we did not engineer them ourselves in an attempt to unravel this scientists have created mathematical models simplified descriptions that capture the

0:23
essence of how neurons work in this video we will explore the hkin Hawley model a Nobel winning breakthrough that many consider to be the most important equation in computational Neuroscience

0:36
in their pioneering work alen hodkin and Andrew hoxley gave the first mathematical description of how neurons generate and propagate electrical signals in fact these equations are so

0:48
fundamental that I have them tattooed on my forearm in this video we will build an intuitive understanding of the biophysics behind neuronal computations from the ground up our primary to rules

1:00
will be derivatives and differential equations that we covered in the previous video in the series today we will take the framework of dynamical systems and apply it to neurons to

1:11
describe how cells change their states over time enabling such a rich variety of computations if you're interested stay tuned to begin describing a neuron's behavior we need to clarify what exactly

1:32
we want to model a living cell is an incredibly complex system so we will have to make significant simplifications using the terminology from the previous video we need to pick State variables

1:43
let's start with the most crucial one the membrane voltage imagine a neuron as a tiny bag filled with water and various dissolved particles floating in a sea of similar

1:54
fluid the thin barrier separating these two environments called the cell membrane is where all the action happens the particles dissolved in the water both inside and outside the cell are

2:07
called ions and they carry electric charge some are positive and some are negative now here's the key fact the composition of ions on both sides of the membrane is different crucially for our

2:20
discussion the inside of the cell contains more negative charge than the outside this separation of charges creates what is known as electrical part potential or voltage you can think of

2:32
voltage as a measure of potential energy arising from the imbalance of charges across the membrane it is similar to the potential energy of water held behind the dam just as water has the potential

2:45
to flow down hill and do work the separated charges have the potential to flow and create the electrical current if given a path to do so if the membrane were freely permeable to ions this

2:58
energy would get get converted into the kinetic energy of ions flowing through the barrier dissipating the charge imbalance however when the membrane is impermeable excess charge has nowhere to

3:12
flow and this potential energy remains stored the amount of energy stored depends on both the magnitude of the charge difference and the physical properties of the membrane such as its

3:23
thickness and area this ability to store electric charge is called capacitance the behavior of a capacitor is described by a fundamental equation that relates the stored charge to the voltage across

3:37
the membrane to understand neuronal Dynamics we need to consider how this equation changes over time taking the time derivative or the rate of change of both sides gives us the following equation it

3:51
describes how the voltage changes as charges redistribute across the membrane however real neurons are more more complex than perfect capacitors the membrane isn't completely impermeable it

4:04
has specialized protein channels that open and close allowing specific ions to flow across the membrane these Pathways for ION flow can be thought of as resistors working

4:18
alongside our capacitor when ions physically cross the membrane through these Pathways they create electrical currents that alter the distribution of charge since current is defined as the rate of

4:33
change of the electric charge we can rewrite our final equation in the following way where the right hand side represents the sum of all ionic currents flowing through the membrane this

4:45
equation marks our first crucial step in understanding neuronal Dynamics it links the rate of change of membrane voltage to the various currents flowing across the membrane before we talk about the

4:57
underlying differential equations let's get a rough sketch of what's going on when a neuron fires there are two types of ions that play The crucial role and whose Dynamics we will describe sodium

5:09
and potassium think of an action potential as a brief electrical pulse caused by a precisely coordinated way of how these ions flow through channels in the membrane it starts when the membrane

5:22
voltage Rises slightly above its resting level crossing a certain threshold this depolarization causes sodium channels to begin opening allowing sodium ions which

5:33
carry positive charge to flow into the cell and thus cause even more depolarization after a brief period of opening sodium channels close blocking the influx of positive charge at the

5:46
same time channels of Another Kind open allowing positively charged potassium ions to leave the cell driving the membrane voltage back down to its resting level the entire sequence takes

5:59
just just a few milliseconds but it's the fundamental signal that neurons use to transmit information this conceptual description makes intuitive sense but it's unclear

6:11
how do channels coordinate to ensure that they're opening in a proper sequence after all there is no dorment that would open and close channels when required so how is this dance

6:22
orchestrated biophysically we'll Begin by discussing what exactly makes ions move across the membrane the rate at which ions flow through the channels depends on two key factors how many

6:33
channels are open and how strong the driving force is there are two physical processes that determine this driving force first there is diffusion the tendency of particles to spread from

6:45
areas of high concentration to low concentration you can think of it as a purely statistical process if you have more particles on one side by random motion they are more likely to bump into

6:57
channels from that side and pass through this is the same reason why a drop of food coloring spreads through water second there is the electrical force since ions carry charge they are

7:10
attracted to opposite charges and repelled by like charges remember that in the intact physiological condition there is an excess of negative charge inside the neuron this means positive

7:23
ions are attracted inward while negative ions are pushed outward now here's where it gets interesting these two forces often oppose each other let's take potassium as an example there

7:38
are more potassium ions inside the cell than outside so diffusion tries to push them out but since potassium is positively charged it is electrically attracted to flow into the cell to

7:50
neutralize the excess negative charge which force wins depends on both the concentration ratio of ions and the m voltage for any given concentration ratio there exists a special value of

8:05
membrane voltage known as the equilibrium potential where the electrical force exactly balances the diffusion Force at this voltage even though individual ions are still moving

8:18
back and forth through open channels there is no net flow for every ion that moves in One Direction another one moves in the opposite direction when the membrane voltage differs from this

8:30
equilibrium potential there is a net flow of ions that tends to drive the membrane potential towards the equilibrium let's make this more concrete with an example in a typical

8:42
neuron there are about 30 times as many potassium ions inside the cell as outside creating a strong outward diffusive Force the corresponding equilibrium potential is about - 90 M if

8:56
the membrane potential is less negative let's let's say- 50 m the electrical force is too weak and the diffusion dominates causing potassium to flow outwards this removes positive charge

9:10
from the cell making the membrane potential more negative until it reaches minus 90 conversely if the membrane voltage is more negative than the equilibrium potential let's say minus

9:22
120 Mills the electrical attraction becomes so strong that it causes a net influx of potassium ions reducing the excess negative charge until the membrane voltage settles back around

9:36
minus 90 we can express this mathematically for each ion the current flow through open channels is proportional to the difference between the actual membrane voltage and the

9:48
equilibrium potential this difference is what we call the driving force the proportionality constant is called conductance which represents how many channels are open

9:59
and how easily ions flow through them if you remember Ms law from physics this is exactly that with conductance being the inverse of resistance so far we have treated the

10:12
conductance as a fixed property of the membrane as if ion channels were simply holes that were permanently open but real neurons are far more interesting many of the ion channels are voltage

10:24
dependent meaning that they open and close depending on the membrane volt voltage itself thus our Quest until the end of the video would be to arrive at the expression for G as a function of

10:35
voltage completing our description despite the drastically different roles of sodium and potassium in generating the action potential the underlying formalism or describing voltage

10:46
dependent conductance is basically the same for different ions apart for a few technical details let's first Express the conductance to be the product of two factors here G bar represents the

11:00
maximum conductance hypothetically possible if all of the ion channels were open this is a constant determined by the total number of channels present in the membrane and the conductance of each

11:12
Channel when it's open thus it does not change with time the second Factor p is a number between zero and one representing the fraction of ion channels that are open at any given time

11:27
which depends on the membrane voltage the fraction of open channels is basically the same thing as the probability that a channel is found in an open State how can we think about

11:39
this probability of a channel being open for that let's Zoom even closer each ion channel is a complex protein machine that changes its shape in response to membrane voltage either allowing or

11:52
blocking iron flow there are various molecular mechanisms of how that might happen and the details are not fully resolved but broadly channel proteins have charged parts let's call them Gates

12:05
that move in response to the electrical field across the membrane each such gate can exist in one of two positions permissive and non-permissive whether the channel as a

12:17
whole allows ions to flow depends on whether all the gates inside it are in the correct permissive States kind of how inside a lock multiple pins need to be in the correct position for the door

12:29
to open let's call the probability of finding a given gate in its permissive position as n we are looking to arrive at a differential equation for n how fast does the number of permissive Gates

12:44
change well let's think about it in terms of transitions Between the States since there are only two possible configurations n can increase if a gate that was in a non-permissive position

12:56
moves there are one minus n Gates that are nonpermissive and let's say they are opening with a certain rate Alpha alternatively n can decrease if one of the gates that is currently in

13:11
the permissive position changes its state to non-permissive by definition at a given moment there are n permissive Gates and we can denote the rate of closing as beta this results in the following

13:24
differential equation where both opening and closing rates depend on voltage in their original work hodkin and Hawley determined the equation for Alpha and beta empirically through

13:38
careful experimental measurements the voltage dependence of these rate factors reflects a complex physical process of charged amino acid residues moving within the membrane under the influence

13:50
of electric field while there isn't any elegant closed form expression that can be intuitively derived to describe this hkin and Hawley found that certain mathematical forms involving combination

14:04
of linear terms and exponentials could fit their data remarkably well with these empirical expressions for Alpha and beta as functions of voltage we can numerically solve the differential

14:16
equation that governs the fraction of individual gates in the permissive state but what about channels that require multiple gates to be in the correct configuration to allow ion flow here are

14:28
the probab ility Theory gives us a simple answer if the probability of a single gate being in its permissive state is n then for a Channel with four independent gates for example the

14:41
probability of all Gates being permissive and thus the channnel being open must be and raised to the fourth power this is precisely what hodkin and hoxley found for potassium currents the

14:54
conductance was proportional to the fourth power of n what makes this finding truly remarkable is that at the time of these experiments the molecular structure of potassium channels was

15:05
completely unknown the fourth power emerged purely from fitting curves to their experimental data decades later when researchers could finally examine Channel structures using x-ray

15:19
crystallography they confirmed that each potassium Channel indeed contains four identical subunits that work together to control ion flow so far we have a description of a cell that only contains

15:34
voltage gated potassium Channels with the following two differential equations one expressing changes in the membrane voltage as a function of potassium current and one for potassium

15:45
conductance as a function of membrane voltage but potassium alone is not enough to make neuron generate an action potential the formalism for describing sodium currents is exactly the same but

15:58
in instead of four identical Gates each sodium channel has Gates of two different kinds with the conductance following a different pattern here M represents one type of gate analogous to

16:11
n for pottassium channels but we need three of them hence the cubic power there is also an additional Factor H representing a completely different type of gate with its own distinct properties

16:25
while the M gates open in response to increased voltage Vol making the channel more likely to conduct the H gate does the opposite it closes with sustained depolarization in a process known as

16:39
inactivation but the differential equations for M and H have similar flavor to potassium Gates just with different constants in the alpha and beta functions this concludes our description

16:51
of voltage dependent ionic conductance now I realized that this is a lot of information so let's step back and review the journey that we've taken we started with a fundamental question

17:01
how can we describe the neurons electrical Behavior mathematically our first key Insight was that the most important variable to keep track of is membrane voltage the difference in

17:11
electrical potential between inside and outside the cell this voltage arises due to the charge separation across the cell membrane which acts as a leaky capacitor

17:21
storing electrical energy this led us to the first equation relating the rate of change of membrane voltage to various currents flowing across the membrane to understand these currents we found that

17:34
the behavior of each ion follows a similar pattern given by Oh's law here e is the equilibrium potential determined by the concentration ratios of a given Ion on both sides of the membrane the

17:47
real complexity and the beauty of the model lies in how these conductances depend on voltage hodkin and Hawley experimentally discovered that we need two types of ionic currents to explain

17:59
the neuronal Dynamics a pottassium current with conductance proportional to n 4th where n represents a probability of a single gate being in the permissive position and a sodium current with

18:13
conductance proportional to M cubed * H where M and H represent two different types of gates each of the three gating variables follows its own differential equation in this form where X represents

18:28
any of these variables and Alpha and beta are voltage dependent rate constants determined experimentally to allow for more realistic Dynamics we often include a

18:39
small leak current into the equation for voltage which corresponds to various ions moving through the channels that are permanently open and thus have a constant conductance there is one more

18:51
important point to clarify everything we have discussed so far treats the neuron as a single point assuming the membrane voltage is the same everywhere in the cell this approximation works well for

19:05
small neurons or when we primarily interested in what happens near the cell body however real neurons have complex branching structures Dent rites that receive inputs and axons that transmit

19:18
signals and the membrane voltage can vary significantly across these different locations to handle this spatial complexity we essentially divide divide the neuron into many small segments and

19:32
apply the hodkin Hawley equations to each segment adding terms that describe how current flows between neighboring segments this gives us a system of coupled differential equations where

19:44
each segment's voltage depends on both its local ion channels and on current flows from Neighbors the resting mathematics becomes more complex but the core principles remain the same

19:57
everything is still governed by ions flowing through voltage dependent channels just with the added consideration of how these currents spread through the neurons elaborate

20:07
morphology what we talked about today is the most complete mathematical description of how neurons generate electrical signals capturing the intricate dense of ion Channels with

20:17
remarkable accuracy however this completeness comes at a cost our model consists of four coupled differential equations one for voltage and three for different gauges variables while we can

20:30
easily solve those equations numerically and simulate a neuron on a computer the high dimensionality makes it very difficult to gain intuitive understanding with four equations we

20:41
cannot directly visualize the system state in the phase space a powerful geometric tool that would allow us to see how neurons transition between resting and firing states in the

20:53
following video we will see how we can strategically simplify the full hkin Hawley model to just two variables while preserving the essential features this reduction will allow us to directly

21:04
visualize systems Dynamics in a two-dimensional face plane revealing beautiful geometric insights into neuronal excitability we will explore why exactly neurons behave the way they

21:14
do and how subtle changes in parameters can lead to dramatically different patterns of electrical activity in the meantime if you're interested to dive even deeper into the fundamentals of

21:25
neural computation our today's sponsor has exactly what you need brilliant.org is an Innovative online platform offering engaging courses across stem Fields what sets brilliant apart is

21:38
their unique focus on Hands-On learning rather than just reading textbooks you'll develop intuitive understanding and problem solving skills through bite-sized interactive lessons two

21:50
courses primarily relevant to today's topic are electricity and magnetism and classical mechanics the first one covers the foundational physics of charged particles exploring Concepts like kum's

22:02
law and electric Fields essential principles behind neural Dynamics the classical mechanics course complements this perfectly helping you master crucial Concepts like forces work and

22:13
forms of energy brilant also offers an extensive collection of courses in math programming and related fields whether you're just starting out and want to build a strong Foundation or if you're

22:24
looking to expand your knowledge into new domains brilant is an valuable resource if you're ready to embrace your curiosity head to brilliant.org Aram konov to get a 30-day free trial of

22:38
everything brilliant has to offer plus a 20% discount on annual subscription if you enjoyed the video share it with your friends subscribe to the channel if you haven't already and

22:49
press the like button also consider supporting me on patreon where you can vote for video topics and get access to bonus content like the written versions of the video scripts containing math

23:00
details stay tuned for more interesting topics coming up goodbye and thank you for the interest in the brain