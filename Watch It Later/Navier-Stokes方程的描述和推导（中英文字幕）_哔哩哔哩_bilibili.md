---
url: https://www.bilibili.com/video/BV1ty4y167jq/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
tags:
  - video
status: readed
date: 2026-01-19T12:01:59+08:00
---
![Navier-Stokes方程的描述和推导（中英文字幕）_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1ty4y167jq/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c)
Navier-Stokes方程的描述和推导（中英文字幕）
https://www.bilibili.com/video/BV1ty4y167jq/?spm_id_from=333.1387.favlist.content.click&vd_source=06168f390bae49c4867767c52a20e87c
bender2016 2020-11-19 18:15:11

Description and Derivation of the Navier-Stokes Equations
Navier-Stokes方程的描述和推导 these are the navier-stokes equations as they're commonly written
这是Navier-Stokes方程通常的写法 in this screencast we examine their physical meaning
在这个视频中，我们将考察它们的物理意义 and perform a simple mathematical derivation based on Newton's second law
并根据牛顿第二定律进行一个简单的数学推导 while these equations may look intimidating and complicated to a lot of people
虽然，对于许多人来说，这些方程看上去吓人和复杂 all they really are is a statement that the sum of forces is equal to the mass times the acceleration
它们其实是一个声明，即外力的总和等于质量乘以加速度 to make it a little bit more apparent let's flip the equations about the equal sign
为了让它更容易理解让我们将公式左右调换一下 so what we have in the first equation is the sum of forces in the x-direction
这样，我们在公式中首先得到的是x方向上的外力总和 

is equal to the mass times the acceleration in the x-direction
它等于质量乘以X方向上的加速度 in the second and third equations of the some forces in the Y and Z direction
在第二个和第三个方程中, 在Y和Z方向的这些外力 equal to their respective accelerations
分别等于它们的加速度 these equations are written for a differential element of fluid
这些方程表示流体的一个微元 which is infinitesimally small so as small as we can possibly imagine
它无穷小,小到我们难以想象 the three forces we're concerned with of forces due to gravity
我们所关心的外力是重力导致的外力 forces due to differences in pressure and forces due to the viscosity of the fluid
压力差导致的外力以及流体粘性导致的外力 keep in mind that each of these terms is on a per unit volume basis
注意，这些项都是以单位体积计算的 so typically we would say the force due to gravity might be the weight of something
所以，我们通常说由于重力产生的力可能是某物的重量 if I took the weight and divided by the volume
如果我们将重量除以体积 

what I'm left with is the density M over V times gravity
我们得到的就是密度M/V乘以重力 we see this occurring for gravity most explicitly
这个现象最明显的例子是重力 on the right-hand side of the equation
在这个方程的右边 if we have mass times acceleration
如果我们让质量乘以加速度 if we were to divide that by the volume of the fluid
如果我们将它除以流体的体积 we would be left with the density times the acceleration
我们会得到密度乘以加速度 so we're looking at the sum of forces is equal to MA on a per unit volume basis
所以，我们看到外力的总和等于MA除以一个每单位体积基 for this screencast let's deal only with the x-direction
在这个视频中，我们只处理X方向 the same mathematics would apply for the Y in the Z directions
这些数学推导也适用于Y和Z方向 but we'll leave it with the X direction to save time
但是，我们只处理X方向来节省时间 let's examine the right-hand side of the X component
让我们考察X分量方程的右边 

the X component of velocity for a fluid we'll call it lower case u
我们称一个流体速度的X分量为一个小写的u and strictly speaking you could be a function of X Y Z and time
严格来说，它是一个X，Y，Z和时间的函数 the X component of acceleration for the fluid is equal to the time derivative of u
流体加速度的X分量等于u的时间导数 is a derivative of u with respect to time
它是一个关于时间的u导数 but because u is not simply a function of time
但是，因为u不是一个简单的时间函数 it's also a function of X Y and Z
它还是X，Y和Z的函数 we need to use the chain rule to perform this differentiation
我们必须使用链式法则来执行这个微分。注：全微分链式法则为(du = ∂u/∂t*dt + ∂u/∂x*dx + ∂u/∂y*dy + ∂u/∂z*dz) so I'm going to do the partial u with respect to time plus ∂u/∂x times dx/dt
所以，我将得到∂u/∂t, 加上∂u/∂x乘以dx/dt。注：这里是u的偏导而不是导数 Plus ∂u/∂y times dy/dt Plus ∂u/∂z times dz/dt
加上∂u/∂y乘以dy/dt，加上∂u/∂z乘以dz/dt if I use the definition that dx/dt simply equal to u
如果我使用定义，dx/dt简单的等于u 

dy/dt is equal to lowercase v and dz/dt is equal to lowercase w
dy/dt等于小写的v以及，dz/dt等于小写的w we're left with something that looks an awful lot
我们得到了一些看上去有点复杂的东西 like the right-hand side of the equation above
就是上面公式的右边 the first term on the right hand side is known as a local acceleration
右边的第一项称为局部加速度 and the remaining three terms are known as the convective acceleration
剩下的三项被称为对流加速度 to think about what this means physically
想象一下它的物理意义 let's consider some fluid that's flowing steadily from left to right through this two dimensional constriction
让我们考虑一些流体它不断从左到右通过这个二维收缩体 and let's consider a differential element of fluid which will be infinitesimally small
同时，让我们考虑一个无穷小的微元 so I'll make it a real small cube and let's place it right here to begin with
所以，认为它是一个非常小的立方体，开始将它放在这里 if you think about the motion of this element to fluid
如果你想象一下这个流体元 

as it flows through it's flowing steadily from left to right
在流动时，它从左稳定的流到右边 it's slow in this region but then it begins to accelerate 
它在这个区域很慢，然后，开始加速 because of the constriction where the fluid is moving very rapidly here
因为流体在这个收缩区域移动非常快 and now when it reaches the right hand side it slows down again
现在，当它到达右边，它会再次减速 and it recovers to a steady velocity as it moves towards the exit
并且，当它会朝出口移动时，它会恢复到一个稳定的速度 if the flow of fluid is at steady state
如果流体的流动在稳定状态 then the velocity of the differential element to fluid at points one two and three
那么，流体微元在1，2，3点的速度 we'd see no change over time
我们会发现在时间上没有变化 but let's examine the constricting region
让我们看一下这个收缩区域 we've got u is a positive quantity it's moving from left to right 
我们得到的u是一个正值，它从左移动到右 and du/dx is also a positive quantity
 并且du/dx也是一个正值 

so this term of the convective acceleration is greater than zero
所以，这个对流加速度大于零 so we see in the highlighted region that the fluid element is accelerating from left to right
那么，我们看到高亮区域中，流体元从左到右在加速 conversely in the expanding region although u is positive du/dx is less than zero it's a negative quantity
在膨胀区域相反。虽然，u是正数，但是du/dx小于零, 它是一个负值 the fluid is slowing down within that region
流体在这个区域减速 so the convective acceleration term is less than zero
所以，对流加速度项小于零 or it would be the acceleration would be to the left in the highlighted read
或者它的加速度将会是高亮区域的左边 let's examine the forces acting on the differential element to fluid a little bit more carefully
让我们稍微仔细的考察一下作用在流体微元上的外力 call this point X Y Z in our differential element to fluid
将这一点称为流体微元中的X，Y和Z it has length dx a height dy and a depth dz
它的长度为dx，高度为dy，深度为dz 

the first force will consider is gravity 
我们要考虑的第一个外力是重力 and typically when you draw a free body diagram gravity will be acting downward in the Y direction
通常，当你绘制一个自由体受力图, 重力会沿着Y方向向下 but let's do an arbitrary case
但是，让我们假设一个任意的情况 where a component of gravity could for example could act in the X direction
例如，在这里，重力的一个分量可以沿着X方向 so the force due to gravity is the mass of our differential element to fluid
那么，由于重力产生的外力是我们流体微元的质量 times the X component of gravity
乘以重力的X分量 let's rewrite the mass is equal to the density times the volume of our differential element to fluid
让我们将质量重写为密度乘以我们流体微元的体积 dxdydz
它为dxdydz so again have the mass times gravity in the X direction
也是就是质量乘以在X方向上的重力 let's examine forces acting on the left and the right sides of our differential element
让我们考察一下作用在微元左边和右边上的外力 

we could have a normal stress acting directly to the right on the right face
我们可以有一个正应力直接作用在右边表面的右边 and a stress acting to the left outward from the left face 
还有一个应力向外作用在左边表面的左边 the notation we'll use for these stresses is σxx
我们为这些应力使用的符号是σxx and we're going to evaluate σxx at X plus a distance dx
并且，我们将在X加上一个dx距离的位置上评估σxx and on the left face we have σxx evaluated at X
在左边表面，我们在X处评估σxx on the top and the bottom faces
在顶部和底部表面 we could have a shear stress acting to the right on the top face
我们有一个剪应力向右作用在顶部表面 and a shear stress acting to the left on the bottom face
一个剪应力向左作用在底部表面 the notation we'll use for these stresses is τyx
这些应力，我们表示为τyx evaluated at y plus dy for the top of the cube
它在y+dy上评估，用于立方体顶部 and τyx evaluated at Y for the bottom of the cube
以及一个τyx在y上评估，用于立方体的底部 

and additionally we could have stresses acting to the right on the front of the cube
另外，我们还有作用在立方体前面的应力\N and a stress acting to the left at the back of the cube
和一个作用在立方体后面的应力 for the back of the cube we'll use the notation τzx evaluated at Z
对于立方体的后面，我们使用τzx在z上评估 and at the front of the queue we'll use the notation τzx evaluated at Z plus dz
在这个立方体的前面，我们使用τzx在z+dz上评估 so continue writing the sum forces in x-direction
那么，继续写出在x方向上的外力总和 I've got any X component of gravity plus a normal stress σxx evaluated at X
我们得到重力的一个x分量加上一个在x+dx上评估σxx的正应力 plus dx multiplied by the surface area of the right side of the cube
加上dx乘以立方体右边的表面面积 which is equal to dydz
它为dydz because it acts to the left I'll subtract σxx evaluated at X multiplied by the same area dydz
因为它作用在左边，我们将会减去在x处评估的σxx乘以相同的面积dydz 

then I'll add the force due to the shear stress at the top of the cube τyx evaluated at y plus dy
然后，我们将会添加立方体顶部y+dy处剪应力产生的外力τyx multiplied by its area which is dx times dz
乘以它的面积dxdz\N I'll subtract the shear stress acting on the bottom face multiplied by its area
我将会减去作用在表面底部的剪应力乘以它的面积 then I'll add the force due to the shear stress at the front of the face
然后，我添加前面剪应力产生的外力 and subtract off the shear stress acting at the rear face
然后减去作用在后面的剪应力 the sum of these forces will equal the mass times the acceleration in the X direction
这些外力的总和将会等于质量乘以X方向上的加速度 or I could write mass is equal to ρ times dxdydz times the acceleration in the X direction
或者，我可以将质量写成等于ρ乘以dxdydz乘以X方向的加速度 you have cleaned up that equation divided by the volume of the differential element
你可以通过除以微元体积清理这个公式 

and what I immediately see is that dxdydz was cancel out 
我们会马上看到dxdydz被抵消了 in some terms if I simplify a dy and dz will cancel out
在这一项中，dxdz也可以抵消 dx cancels out as well as dz in this term and so forth as I cancel out terms
在这项中，dx和dz也抵消了，等等 as I continue to simplify am left on the neck with this expression
我继续简化这个表达式的左边 and in the limit of dx dy and dz are approaching zero
当dx，dy和dz的极限接近零 this turns into a differential form
它变成一个微分形式 and the resulting equation represents the sum of forces in the x-direction
最后的方程表示为在X方向的外力的总和 due to gravity
它们是重力 due to the normal forces acting on the left and the right side of the differential element
在微元左边和右边作用的外力 the shear stresses acting on the top and the bottom of the element
在微元顶部和底部的剪应力 and the shear stresses acting in the front in the rear faces of the element
在微元前面和后面的剪应力 

so these are equal to the density times the acceleration of the differential element in the X direction
那么，它们等于密度乘以微元在X方向上的加速度 and if I expand the acceleration into its local and convective components
如果，我们将加速度扩展到它的局部和对流分量中 we left with the an expression on the right hand side
就会得到右边的表达式 if I did the same analysis for the Y and the Z directions
如果我为Y和Z方向做相同的分析 I would come up with these three equations which are known as the equations of motion for a fluid
我会得出这三个方程它们也称为流体运动方程 but to get from these equations to the navier-stokes equations
但是，要将这些方程变成navier-stokes方程 we need a way to relate the normal and the shear stresses to the viscosity of the fluid and the velocity profiles
我们需要一个方法将常规压力和剪应力和流体的黏度和速度剖面关联起来 and this is done using these equations which are the constitutive relations for a Newtonian fluid
可以使用这些方程来完成，它们是牛顿流体的本构关系 

which we won't get into here
我们不会深入这点 but if we accept them as being true for this screencast
但是，如果我们在这个视频中接受它的真实性。注：剪应力与流体的速度和粘度相关 it becomes a series of algebraic manipulations to arrive at the navier-stokes equation
这变成了一系列得到Navier-Stokes方程的代数操作 the first substitution into the left hand side
第一个替换出现在左边 gives me the expression at the bottom
得到底部的表达式 if I differentiate the three terms I'm left with this expression
如果我求导这3项，我会得到这个表达式 and some additional manipulations leaves me with this expression
以及一些附加变换会得到这个表达式 in which I've split this term into two parts I've switched the order
在这里，我将这项拆分成两个部分并交换顺序 in which I differentiate these two terms
在这里，我求导这2项 so I'm switching dy/dx and dd and this expression
那么，我交换dy/dx 和dd，这个表达式 so I continue to simplify and rearrange terms I'm left with this expression
我继续简化并重新排列这些项, 我会得到这个表达式 

but what's interesting is the sum of these three terms
但是，我关注的是这3项 du/dx plus dv/dy plus dw/dz is equal to zero
du/dx加上dv/dy，加上dw/dz等于零。注：在非压缩流体中 ∇∙u=0 by way of the continuity equation
因为它是连续性方程 so that whole term on the right is identically zero for an incompressible fluid
那么，在右边的整个项对于非压缩流体来说为零 so what I'm left with the sum is three forces the force
那么，我得到3个外力的总和 the force due to gravity
重力产生的外力 due to any pressure differences in the fluid
流体中压力差得到的外力 plus all the forces due to viscosity
加上粘性产生的外力 the sum of these three is equal to the density of the fluid multiplied by the X component of its acceleration
这3个外力的总和等于流体密度乘以它加速度的X分量 and expanding ax out into its local and convective components of acceleration
将X扩展为加速度的局部和对流分量 I've just arrived at the first the X component for the navier-stokes equation
我们得到了navier-stokes方程的X分量 

so we could do the exact same thing for the Y and the Z directions
那么，我们可以最Y和Z方向做相同的处理 it will arrive at the navier-stokes equations for those directions as well 
我们也会得到这些方向的navier-stokes方程 if I flip the order of the equations you're left with the navier-stokes equations as you'll commonly see them
如果我们调换方程的顺序, 你会得到通常所看到的navier-stokes方程 and although they may look intimidating and complicated to begin with 
虽然，它们最初看上去吓人和复杂 if someone asks you to sum up what the navier-stokes equations are
如果有人问你navier-stokes方程加在一起是什么 in words just simply tell them they're an expression of the sum of forces
你可以简单的告诉它们是一些外力总和 is equal to the mass times the acceleration
等于质量乘以加速度 



--- 由 vCaptions 生成 ---