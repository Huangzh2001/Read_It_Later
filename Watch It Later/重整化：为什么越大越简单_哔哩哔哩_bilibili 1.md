---
url: https://www.bilibili.com/video/BV1d14y117k3/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2025-11-20T21:25:54+08:00
---
![重整化：为什么越大越简单_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1d14y117k3/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
重整化：为什么越大越简单
https://www.bilibili.com/video/BV1d14y117k3/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
墨子数学研究所 2023-08-25 20:05:08

00:00 Today i would like to discuss for normalization
00:03 Normalization is a set of techniques used all over in physics
00:06 From particle physics to material science to fluid mechanics
00:10 Which allows us to understand how the behavior of matter changes between different length scales
00:15 In particular it can help us answer two very deep questions
00:19 The first is despite the substantial complexity and diversity of molecules and interactions that hold matter together
00:25 We can usually describe the macroscopic properties of materials with only a few numbers
00:30 In order to describe the properties of even a simple molecule like water
00:33 Requires a significant amount of information
00:35 And the interactions between molecules add an additional layer of complexity and variability
00:40 Meanwhile you have a fairly good description of a material
00:43 If you know its density
00:44 A handful of thermodynamic properties such as conductivity
00:48 And a few mechanical properties
00:49 Such as viscosity for liquids or yield strength for solids
00:52 Why is that the second question i want to try to answer
00:56 Is why the properties of the material can change very suddenly
00:59 When its environment changes
01:01 Ice melts
01:02 Water boils
01:03 Metals become superconductors
01:05 All at precise and specific temperatures
01:07 Pressures or magnetic fields
01:09 Why are these boundaries sharp rather than gradual
01:11 In order to answer these questions
01:13 We need some way to figure out how complicated microscopic interactions average out at larger scales
01:18 To determine a material's properties
01:20 This process is called for normalization
01:24 Essentially the process looks something like this start
01:27 With some model of our material describing how its smallest components interact
01:31 In theory
01:31 This model includes all of the information needed to describe the material
01:35 But it is not easy to work out what its properties are at larger scales from it
01:39 Since this model is made up of an extremely large number of microscopic components
01:43 That we cannot see
01:44 It's going to be a statistical rather than deterministic
01:48 Average out the smallest scale behavior to get a model that is valid at some intermediate scale
01:52 This is called coarse graining
01:54 Since we are redefining our system in terms of larger scale coarser variables
01:58 And therefore losing information about the smaller scale
02:01 Repeat this process until we reach the scale
02:03 We would like to understand
02:09 In order to figure out what we mean by averaging
02:11 We first need to define what it is we are averaging over
02:14 We are averaging over states
02:16 The system can be in weighted by the probabilities of those states
02:20 If we have some closed system
02:21 Let's say
02:22 A gas
02:22 We might know things like its volume
02:24 Temperature and pressure
02:26 But
02:26 We generally do not know what the precise location and velocity of every molecule in the system
02:30 Is instead based on the gse's macroscopic properties
02:33 We know what the probability is of the molecules being in any particular configuration
02:38 For example
02:39 It is much more likely that the molecules are spread out throughout the container
02:42 Than that they are tightly packed into a corner
02:44 Both because it takes much more energy to pack them together
02:47 And because there are more ways for the molecules to be spread out in general
02:53 We are going to denote the set of variables we use to describe the particular state
02:56 Our system is in with the letter phi for a gas
02:59 This might be the position and velocity of every molecule for a chemical solution
03:03 It might be the concentration of each reactant at each point in space
03:07 Or for a magnet
03:08 It might be the degree of magnetization of the material
03:10 At each point in the magnet
03:12 Probability of any particular state or value of phi
03:16 It's given by a distribution called a gibbs distribution
03:18 The probability of a state phi is proportional to e to the power minus h over t
03:24 Where h is the energy of that particular configuration called the hamiltonian
03:29 And t is the temperature
03:31 The sum is taken over all possible configurations
03:33 So that the probabilities sum to one
03:36 This can be made somewhat more intuitive
03:38 By noting that lower energy states are much more likely than higher energy ones
03:42 And that high energy states become relatively likely as the temperature increases
03:46 Since the denominator is just some constant that is the same
03:49 Regardless of what state we are looking at
03:51 We will ignore it and just focus on this exponential
03:56 Now we can be much more specific about what we mean by averaging or course graining
04:01 Let's say
04:01 We have some state phi that we split into a large scale part that we call phi bar
04:06 And some small scale part we will call delta phi
04:09 For now the sum is purely symbolic
04:11 We will not be very rigorous about how we go about making this split
04:15 But you can think of phi bar as varying slowly and delta phi as encoding
04:19 Whatever quickly varying information is lost in phi bar
04:24 We can now say that the probability of being in some coarse grain state
04:27 Phi bar is equal to the sum of the probabilities of being
04:30 In any of the regular states that become phi bar when coarse grained
04:34 We can sum over delta phi instead
04:36 Since any phi that goes to phi bar can be specified by the difference between the two
04:41 Which is delta phi
04:44 The whole point of this process
04:46 Is to figure out how our system behaves at this larger scale
04:49 So we would like to get rid of the smaller scale
04:51 By evaluating the sum over delta phi
04:54 We want to get a result that looks like a gibbs distribution
04:57 This time with some new definition of the energy of i r
05:01 This is the hard part
05:04 So what does the h mean anyway
05:07 H stands for hamiltonian
05:08 Which is just a fancy word for the total energy in the system in a particular state
05:12 For example
05:13 For a gas
05:14 This could just be the sum of the kinetic energies of each molecule
05:18 Generally
05:18 Though when performing where normalization
05:21 It is best to work with a total energy
05:22 That is in terms of an energy density
05:24 A function we will denote with a script h
05:27 Which just tells us the concentration of energy at each point in space
05:30 We get the total energy by summing this function over every point in space
05:34 Which is called an integral
05:36 And it's written like this
05:38 A commonly used example
05:40 Which happens to be a fairly good model
05:41 For how metals such as iron become magnetized
05:44 Looks like this
05:45 This might look complicated
05:46 But we don't really need to know what it means
05:48 The relevant point is that it is a sum of a few terms
05:51 Each of which is some function of our state
05:53 Variable m of x
05:54 Which again for a magnet
05:56 Represents the magnetization of the material at each point
05:59 And each of which has some coefficient in front of it
06:02 The sizes of these coefficients is what determines the energy
06:05 The system has in different states
06:07 And the resulting behavior of the system overall
06:10 Adding in additional terms adds additional behavior to the system
06:13 For example
06:14 Our magnet might respond to being placed in an external magnetic field
06:18 I want to make things simple for our example calculation
06:21 Though
06:21 So we're going to stick with just these two terms
06:24 And ignore the dependence of m on position
06:26 Writing h simply as this
06:30 Now let's get back to our calculation
06:33 We have a way of calculating the probability of our system being in any state
06:36 In this case described by the magnetization m
06:39 In terms of an expression describing the energy of that state
06:42 Which is made of a couple of terms
06:43 Each with a coefficient in front
06:45 We split m into small and large scale parts
06:48 And we would like to calculate the probability of the coarse grain state
06:51 Described by m bar
06:53 Which we know how to write
06:54 In terms of the sum of probabilities of non coarse grain states
06:57 But we would like to do away with the small scale
06:59 And write this in terms of a new hamiltonian called h bar
07:02 We expect the physics of our system to change somewhat as we zoom out
07:05 But we don't expect anything really new to show up
07:08 So we want our new hamiltonian to look like our old one
07:10 Just in terms of m bar instead of m
07:12 And with coefficients
07:13 A bar and b bar instead of a and b
07:15 How do we do that
07:17 This is going to take a decent amount of algebra to work out
07:20 But i wanted to include it both
07:22 To give a taste of what the normalization calculations look like
07:24 To make the answer
07:25 We get seem less mysterious
07:27 Feel free to skip ahead a couple of minutes
07:29 If that doesn't interest you
07:31 Also it's already
07:32 If you don't quite follow every step along the way
07:34 It will not matter much later
07:36 Now
07:37 Back to the video
07:38 So we can solve this equation for h bar
07:40 But we somehow need to evaluate this pesky sum
07:43 And it isn't obvious what to do with this exponential
07:46 What would be really nice is if instead of a sum of exponential functions
07:50 We had each element in the sum being itself
07:52 A sum of terms
07:53 Each term being delta m to some power times
07:56 Some expression involving m bar
07:58 Then we can distribute the sum
08:00 And find that we can isolate each one of them
08:02 A neat trick we can use to simplify this
08:04 A little is to note that the odd terms equals zero
08:07 We can see this by noticing that the sum includes both positive and negative values
08:11 Of delta m in a symmetric fashion
08:13 Then every positive value will be cancelled by a negative value
08:22 So we end up with only the even terms
08:24 Since what these sums evaluate to
08:26 Depends on the details of our course grading procedure
08:28 Which we have been deliberately vague about
08:30 We'll just name them and move on going back to our problem
08:34 We can actually get this sum into the form
08:36 We want using a little trick
08:38 There's a simple series representation for exponential functions that looks like this
08:42 This is of course
08:43 An infinite series
08:44 Which can make it a little messy to work with
08:46 When actually doing a calculation in detail
08:48 There are various tricks to approximate the answer
08:50 With only the first few terms for now
08:53 Let's consider the case where the temperature t is very large
08:56 So the first couple terms is a fairly good approximation on its own
09:01 So let's solve this first
09:04 We plug in our expression for h
09:07 Now we split m and expand
09:12 Now
09:12 As we said before
09:13 Terms with an odd power of delta m will vanish
09:18 And then we take the sum over the evens
09:20 Now we arrange this
09:24 And find some new variables
09:30 Dropping that factor in front the same way
09:32 We ignored the denominator earlier and finally plugging in h bar
09:39 We use our approximation of the exponential again
09:41 This time in reverse
09:42 And we now have what we are seeking
09:46 Starting from our original description of our system
09:48 We calculated a new model valid for a larger scale
09:51 This is what we mean by the normalization
09:53 And we call h bar
09:54 The normalized hamiltonian
09:56 A bar and b bar
09:58 The normalized coefficients
09:59 It's interesting that the expressions for both of the normalized coefficients
10:03 Depend on both a and b
10:05 And in particular that b shows up in the numerator of a bar
10:08 There's an intuitive explanation for this
10:10 The term h that has b in it has m to the fourth power
10:13 When we split m into m bar and delta m
10:16 One of the terms we get has m bar squared
10:19 So that when we put everything together
10:21 This ends up in the term with a bar
10:23 What this means is that the interaction of the large scale magnetic field
10:27 M bar with the small scale magnetic field
10:29 Delta m caused by this m to the fourth term creates an effect on the large scale field
10:35 That looks like the effect of an m r squared term
10:37 Once you average out delta m
10:39 And therefore adds to that term
10:45 What's nice about having these expressions for the normalized coefficients
10:49 In terms of the originals is that it lets us repeat this process indefinitely
10:53 Each time taking the new set of normalized coefficients as the starting point
11:00 So as we repeatedly coarse grain and zoom out
11:03 The effective values of our coefficients will change
11:05 If we make the amount by which we zoom out small
11:08 Then each iteration will only move our coefficients a little
11:11 We see that if we zoom out smoothly instead of in jumps
11:14 That our position in parameter space flows smoothly
11:17 If we see how this flow moves from any initial value of our coefficients
11:21 We get a vector field
11:23 We call this the normalization group flow
11:26 The word group is usually thrown in there as a mathy way of saying that
11:30 If we zoom out by a factor of a and then by a factor of b
11:33 It's the same as zooming out by a times b
11:39 Going back to the normalization flow
11:42 Streamlines can't pass through one another
11:44 Since the vector field can only have one value at each point
11:47 This means that the streamlines have a tendency to converge to the same direction
11:50 When they get near each other
11:52 As a result
11:53 As we zoom out
11:54 We tend to find that we need fewer parameters to define our system in this two dimensional case
11:59 Rather than being anywhere on the plane
12:01 Requiring two parameters after zooming out for a long time
12:06 We can expect to be somewhere very near this line
12:08 Requiring only one parameter to define our position
12:13 In more than two dimensions
12:14 A similar process occurs
12:16 Although it is a little harder to visualize as we zoom out further
12:20 And further one of two things can happen
12:23 The streamlines can go out to infinity
12:25 Giving infinite values of our coefficients
12:27 But this is not reasonable from a physics perspective
12:29 And actually means that model is missing some effects that are important at large scale
12:33 The other option is that they can stop somewhere again
12:36 Because lines don't pass through each other
12:38 Many field lines will tend to stop on the same point or line or surface
12:43 If the fixed points form a line
12:45 Then we still have one free parameter that persists at the largest scales
12:49 And is determined by where we started finding where these fixed points are is very useful
12:54 Since it tells us what the coefficients defining our system are
12:57 When we zoom out arbitrarily far
13:00 It takes zooming out a few million times
13:02 To go from the atomic scale to the size of the smallest of everyday objects
13:07 So the material properties we see tend to lie very very near these fixed points and surfaces
13:12 This is why things are simpler at the largest scales
13:15 The more you zoom out
13:17 The more constrained the parameter space is
13:19 And the more likely we are to be at a fixed point
13:21 Even if we started with some very complicated theory with many coefficients
13:26 It is likely that only a few of them remain at the largest scales as a side note
13:31 This is also a source of difficulty for particle physicists
13:34 They also do a kind of a normalization
13:36 But their math looks a little different because they're doing quantum statistics
13:40 Their standard model of subatomic particles is very good
13:44 At the scales we are able to probe so far using particle accelerators
13:47 But if the normalization flow from even smaller scales has reduced the number of parameters
13:52 It is very hard to tell what direction we came from
13:54 And therefore what might be hiding at these smaller scales
13:58 This is what drives much of the theoretical work on
14:00 What might exist at ever smaller scales
14:03 Equivalent in their case to higher energies
14:05 Which gives the subfield the name
14:07 High energy physics
14:10 So we've answered our first question
14:12 But this still leaves the question of why the large scale properties of materials can change suddenly
14:17 What we call phase transitions
14:19 We can understand this schematically with this picture
14:22 Let's say
14:23 We have some substance
14:24 Whose microscopic structure can conveniently be described by only two parameters
14:29 And that the normalization flow leads to two separate fixed points
14:33 The parameters are going to vary
14:35 Depending on what temperature and pressure the substance is under
14:37 And let's say current conditions put us over here
14:41 If we raise or lower the temperature a bit
14:43 Maybe that shifts us this way and this way
14:46 And if we raise or lower the pressure
14:47 It moves us this way and this way
14:51 Now something interesting can happen here
14:53 See if you can spot it
14:56 Let's say we steadily increase the temperature
14:59 For a while
15:00 The renormalization flow will take us to the same fixed point
15:03 And the large scale properties of our system stay the same
15:06 However eventually we cross a boundary
15:09 And now suddenly the normalization flow takes us to a very different point in parameter space
15:14 Large scale properties of our system will abruptly change
15:17 This boundary defines a phase transition
15:19 And a similar boundary is what leads ice to suddenly melt
15:23 At a particular temperature and pressure for water to boil
15:26 And for basically any other phase transition seen in nature
15:32 Where this boundary line intersects different lines of constant temperature or pressure
15:36 Is what defines the shape of boundaries in phase diagrams
15:43 So to summarize
15:44 We defined
15:45 How to describe the probability of a thermodynamic system being in a particular state
15:49 In terms of the energy of that state and the temperature
15:52 We worked out
15:53 How to average out the smallest scale of our system
15:55 And how this changes our system's parameters
15:58 We saw that repeatedly re scaling our system
16:00 In this way induces a flow in parameter space
16:05 The existence of fixed points in this flow
16:08 Is what makes the properties of macroscopic materials simpler than their
16:11 Microscopic components
16:12 And boundaries between regions that flow to different fixed points are what produce the boundaries we see
16:17 Between phases of matter
16:19 Thank you for joining me in this introduction to our normalization
16:22 I hope you enjoyed it
16:24 I hope to be making more videos like this soon
16:27 And i plan to put a more detailed written version of this presentation on my blog link to
16:31 That will be in the video description when it is ready
16:34 So until next time

--- 由 vCaptions 生成 ---