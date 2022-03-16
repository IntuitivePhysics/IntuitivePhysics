---
layout: post

title: General Inverse Force Laws with spherical symmetries. 

author: Michael Huang

description: Generalizing beyond Inverse Square Law to Inverse Laws of any power in any hyper-spherical symmetry. The derivation is partly based upon the Mean Value Theorem of Harmonic Functions.

tags:
    - electromagnetism
    - harmonic
    - inverse
    - square
    - law
    - charge
    - stability
    - spherical
    - symmetry

excerpt: It will basically help us derive that the force produced by any spherically symmetric charge distribution can be equated to the force produced by a point charge located at its center...

---

You probably have heard of the infamous Inverse Square Law, which gives electrostatic and gravitational forces their various properties. But did you know that there exists an Inverse Cube Law, which describes magnetic fields? In this post, we will analyze the inverse $n^{th}$ law given a spherically symmetric "charge" distribution. As a bonus, we can extrapolate our analyzes to any hyper-spherically symmetric "charge" distribution, such as a ring, a 4D hypersphere, and etc. 

### Content

* But [what exactly is the problem](#what-exactly-is-the-problem)?
* What does the force look like [inside the “charge” distribution](#inside-the-charge-distribution)?
* What does the force look like [outside the "charge" distribution](#outside-the-charge-distribution)?

### What exactly is the problem

##### Generalizing the Concept of Charge

Imagine there is a matter with infinitesimal volume and a quantity $q$ called charge. Let's call a unit charge such a matter with $q=1$. Great! As we can see, a normal electric charge, a mass, and a magnetic point dipole all fall into our definition of a generalized charge. We deal with this generalized concept of a charge throughout the post for maximal mathematical generality. 

##### Generalizing Force Law

Assume that our charge exerts a force on a unit charge some location $\vec{r}$ away and the magnitude of this force $F$ is proportional to $\frac{1}{r^n}$ for some $n$. In the case of electric charge and gravitational mass, we have $F\propto \frac{1}{r^2}$. In the case of magnetic point dipole, we have $F\propto \frac{1}{r^3}$. 

##### Generalizing the Entire Problem

Now, consider we have a spherically symmetric distribution of these charges–––a hollow sphere for example---we want to find the force of this spherically symmetric "charge" distribution on a unit charge some location $\vec{r}$ away. 

##### For the Special Case of Electric Charge

To make our problem concrete, let's remind ourselves of the solution to this problem in the case of a spherical shell of electric charge with uniform charge density. In that case, we know that force exerted on a unit charge inside the sphere is $\bold{0}$. We further know that the force on a unit charge outside of the sphere **exactly equal** to the force that would be exerted if we had a singular point charge at the center of the sphere, with the same charge as the entire spherical shell! 

##### What We Will Try to Achieve

Now, these two consequential results are given by Gauss's Law. And these two results are what we want to generalize/extend to the case where the force exerted by the charge no longer falls off as $1/r^2$ but instead falls off as $1/r^n$. We can then also generalize those results further to arrive at the case of a general hyper-spherically symmetric charge distribution.

### Inside the Charge Distribution

For starters, let's consider a 3D hollow spherical charge distribution. We can always generalize to 3D ball distribution by considering as a stacking of hollow spherical shells. 

##### So For General $\frac{1}{r^n}$ Force What does the Force Inside A Charge Distribution Look Like?

Spoilers!!! It looks ugly. So ugly in fact I've decided to spare you of its specific mathematical ugliness. We do will discuss its general structure.

##### What is the Direction of the Force?

This is easy and has an elegant answer. We will use an approach termed "differential method." It's really just a fancy way of saying let's take a look at the very small interval $dx$ or $\Delta x$ if you prefer.

So, let's place a unit charge $\vec{d}$ away from the center of the hollow sphere. Now, consider projecting a cone of opening angle $d\theta$ in an arbitrary direction, intersecting with one side of the spherical shell. Then, we project a similar cone with the same opening angle $d\theta$ towards the opposite direction, intersecting the opposite side of the spherical shell. 

These two cones are geometrically similar. Why? Consider the fact that 2 intersecting lines in a circle segments the region into 2 pairs of similar triangles. 

Let one cone has radius $r_1$ and the other has radius $r_2$. Say $r_1< r_2$, meaning that cone 1 is on the side of the sphere that we moved towards. 

Now, to understand whether the force is in the direction $\vec{d}$ or $-\vec{d}$, we can simply compare the force $F_1, F_2$ generated respectively by the attraction (flip the sign of everything if it's repulsion) of charges on the surface of the hollow sphere.   

The areas these two cones cover, $A_1, A_2$, follows that $\frac{A_1}{A_2} = \frac{r_1^2}{r_2^2}$. Thus, the charge these two cones cover are $C_1 = \rho A_1, C_2 = \rho A_2$. And they satisfy $\frac{C_1}{C_2} = \frac{r_1^2}{r_2^2}$. Now, remember that $F_1 \propto \frac{C_1}{r_1^n}$ and $F_2 \propto \frac{C_2}{r_1^n}$? We can now compare $F_1, F_2$. We have 

$$
\frac{F_1}{F_2} = \frac{C_1/r_1^n}{C_2/r_2^n} = \frac{r_1^{2-n}}{r_2^{2-n}}
$$

Since $r_1 < r_2$, we know

$F_1 < F_2$, or the unit charge is forced towards direction of $-\vec{d}$ when $n<2$

$F_1=F_2$, or when there's **no** force on the unit charge at all when $n=2$

$F_1>F_2$, or when the unit charge is forced towards direction of $\vec{d}$ when $n>2$

##### Generalizing to Hyper-spherically Symmetric Distribution

We love generalizing. So, what if we are dealing with a circular ring of charge (2D sphere) instead? What about a 4D sphere of charge (though that may be an unlikely engineering problem)? 

Say the sphere is $kD$. We note that the surface area of the sphere grows with respect to radius $r$ with the proportion $r^{k-1}$. That means $C_1\propto r_1^{k-1}$ and similarly for $C_2$. 

Thus, 

$$
\frac{F_1}{F_2} = \frac{r_1^{k-n-1}}{r_2^{k-n-1}}
$$

Nice! So next time your teacher asks you whether the equilibrium of a point mass located at the center of a ring of uniform mass is stable or unstable, you can just recognize that as a subcase of this generalized direction problem with $n=2$ (because it's gravitation) and $k=2$ because a ring is a 2D sphere. In that case, because $k-n-1=-1<0$, we know the force is in the direction of $\vec{d}$ for any displacement $\vec{d}$ from the center. So, we know that the equilibrium at the center is unstable. 

One final thing we can derive from our analysis is the approximate magnitude of the force (or at least its proportions). We note that $F_\text{net} \propto \Delta F$ where $\Delta F = F_1 - F_2$. 

Since $F_1 \propto r_1^{k-n-1}$, and similarly for $F_2$, we may derive

$$
F_\text{net} \propto r_1^{k-n-1} - r_2^{k-n-1} \\
\approx (r-d\cos(\theta))^{k-n-1} - (r+d\cos(\theta))^{k-n-1} \\
\approx r^{k-n-1} -(k-n-1)r^{k-n-2}d\cos(\theta)\\ - r^{k-n-1}-(k-n-1)r^{k-n-2}d\cos(\theta) \\
= 2(n+1-k)d\cos(\theta) r^{k-n-2}
$$

That means, $F_\text{net} \propto (n+1-k) r^{k-n-2}$ when the displacement $\vec{d}$ is relatively small. Of course, when we plug in $n=2$ and $k=3$ as in the case of a normal spherical shell and the electric/gravitational force, we know that $F_\text{net} = 0$.  

### Outside the Charge Distribution

Placing the unit charge outside of the distribution gives us an entirely different picture, quite a beautiful one indeed. 

To understand that, we need to understand a mathematical concept: the mean value theorem of a a harmonic function. I will explain that now.

##### Mean Value Theorem of a Harmonic Function

To keep the math short and simple, let's start from the beginning. The laplacian of a function $f$, denoted by $\nabla^2 f$, is the sum of its second partial derivatives in all directions:

$$
\nabla^2 f = \frac{\partial^2 f}{ {\partial x}^2 } + \frac{\partial^2 f}{ {\partial y}^2 } + \frac{\partial^2 f}{ {\partial z}^2 }
$$

Great! What does that value tell us about $f$? Well, a single second derivative tells us about the concavity of the function along that direction. So $\nabla^2 f$ really stands for the average concavity of the function along all directions. 

For example, $f = x^2 + y^2 + z^2$ is convex everywhere, so it has a very positive $\nabla^2 f$, indicating positive concavity (convexity). 

So, what does concavity/convexity tell us about a function? Well, let's recall the geometric definition of convexity. 

A polygon is called convex at a region if we pick two points and look at their midpoint, then the midpoint is guaranteed to be outside of the line connecting the two points. 

We can generalize that definition to a function. A 1D function is convex around a region if we pick two points in the region, their midpoint is above the line connecting the two points. Or in other words, their midpoint $>$ the average of their values. 

What about for 2D function? Instead of picking two points, we pick a circle. If the center of the circle exists above the plane defined by the circle, the function is convex! If below, then it's concave down. To be more mathematical, we are comparing the center of the circle on the function with the average value of all points on the circle. 

Thus, we know that if $\nabla^2 f > 0$ or $f$ is concave up/convex, then, given $x_\text{center}$ and defining the set of all points distance $r$ from $x_\text{center}$ to be $R$, we have

$$
f(\vec{x}_\text{center}) < avg_R(f)= \frac{\int_{\vec{x}\in R} f(\vec{x}) dx^k}{\int_{\vec{x}\in R} dx^k}
$$

The right hand side simply stands for the average of $f$ over $R$, which is computed by the integral given. $dx^k$ stands for an infinitesimal volume with dimension $k$ where $k$ is the number of independent variables $f$ has. I borrowed this symbol from the famous physicist [Scott Dodelson](https://www.cmu.edu/physics/people/faculty/dodelson.html). 

If $\nabla^2 f < 0$, we reversely have

$$
f(\vec{x}_\text{center}) > avg_R(f)= \frac{\int_{\vec{x}\in R} f(\vec{x}) dx^k}{\int_{\vec{x}\in R} dx^k}
$$

The curious case occurs when $\nabla^2 f = 0$, then we have

$$
f(\vec{x}_\text{center}) = avg_R(f)= \frac{\int_{\vec{x}\in R} f(\vec{x}) dx^k}{\int_{\vec{x}\in R} dx^k}
$$

$f$ is called a harmonic function when $\nabla^2 f = 0$. And this identity we have up here is called the [Mean Value Theorem of a Harmonic Function](https://en.wikipedia.org/wiki/Harmonic_function).

I will explain its value for us now. It will basically help us derive that the force produced by any spherically symmetric charge distribution can be equated to the force produced by a point charge located at its center.

How? Read on. 

##### The Force of Unit Charge on Spherically Symmetric Charge Distribution

Say, we have a spherically symmetric charge distribution we call $S_1$ and a point charge $P_2$. We are interested in $F_{12}$, the force on $S_1$ produced by $P_2$. If $P_2$ produces a force field that is $=\frac{k}{r^n}$, then the total force on $S_1$, letting $\rho$ be its charge density is
$$
F_{12} = \int_{S_1} \frac{k}{r^n} (\rho \cdot dV) \\
= k\rho \int_{S_1} \frac{1}{r^n} dV
$$
Now great! We arrived at an intractible multi-dimensional integral! 

Except for the fact that $\frac{1}{r^n}$ is a harmonic function when $n\ge 1$, when $r\not=0$! We can easily check that by taking $\nabla^2 \frac{1}{r^n}$ but I will spare you the mathematical pain. 

By the [Mean Value Theorem](#mean-value-theorem-of-a-harmonic-function), we know 

$$
\int_{\vec{x}\in R} f(\vec{x}) dx^k = f(\vec{x}_\text{center}) \int_{\vec{x}\in R} dx^k
$$

For our case, $R=S_1$, $f(\vec{x}) = \frac{1}{r^n}$ and $dx^k = dV$. So we have

$$
F_{12} = k\rho \int_{S_1} \frac{1}{r^n} dV \\
= k\rho f(\vec{x}_\text{center}) V 
$$


$f( \vec{x} _ \text{center})$ is the value of $\frac{1}{r^n}$ when we are at the center of $S_1$. If we let the separation between the center of $S_1$ and $P_2$ be denoted by $d$, we have $f(\vec{x} _ \text{center}) = \frac{1}{d^n}$. 

So collecting everything, our final formula for $F_{12}$ is 

$$
F_\text{12} = \frac{k\rho V}{d^n}
$$

Recognizing that $\rho V$ gives the total charge of the distribution, which we may call $Q$, we have

$$
F_{12} = \frac{kQ}{d^n}
$$

which is equivalent to the force exerted on a charge located at the center of $S_1$ with the same total charge as $S_1$! 

We are not done yet. We need to find $F_{21}$ the force caused by a spherical charge distribution not one received by it. For that we use a quick Newton's 3rd Law argument.

##### Newton's 3rd Law to the Rescue

We know $F_{21} = F_{12}$ in magnitude. Great! Now we replace $S_1$ with $P_1$, a point charge with the same charge as $S_1$ located at the center of $S_1$. By our arguments in the last section, $F_{12}$ remains unchanged. Therefore, $F_{21}$ mustn't change either. We can therefore conclude that the force exerted on $P_2$ by $P_1$ is the same as that exerted by $S_1$. In other words, a spherical charge distribution exerts the same force as a point charge located at its center.

##### A Final Question...

All these arguments using the Mean Value Theorem...seem to work no matter where $P_2$ is located with respect to $S_1$. What if $P_2$ is within $S_1$? Would that not mean a spherical charge distribution exerts a force on a point charge within it with the same magnitude as the force exerted by a point charge at the center of the sphere with the same total charge? Doesn't that nullify our discussion of the force laws inside a spherical shell and other spherically symmetric shapes? 

That's really confusing!!! 

Since this is a crucial question for understanding our entire analysis, I will just leave it to the readers to figure out!

### Acknowledgement

This post doesn't contain all original ideas. 

The second part of the post using the harmonic function idea to derive force laws originate from 2021's [Young Physicist Tournament](http://www.usaypt.org/) problem "The Attraction Between Magnetic Balls." The work was done with William Yue, and several other folks. 

The intuition regarding understanding the laplacian as an indicator of concavity is built upon Grant Sanderson's [lecture](https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/laplacian/v/laplacian-intuition) on the said topic. 

The idea of applying the harmonic function to understanding force laws is suggested by Kirk T. McDonald in [this paper](https://www.hep.princeton.edu//~mcdonald/examples/twomagspheres.pdf).

The idea of using Newton's 3rd Law for the final argument is presented by Boyd F. Edwards et al. in [their paper](http://www.physics.usu.edu/riffe/bio/AJP%2085%20130.pdf)





 