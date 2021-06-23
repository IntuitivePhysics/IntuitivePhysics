---
layout: post

title: Classical Physics, orbital, spin, total angular momentum, and hidden tricks

author: Michael Huang

description: Explains orbital angular momentum, spin angular momentum, and total angular momentum. Proves spin + orbital = total.

tags:
    - mechanics
    - angular momentum
    - momentum
    - spin
    - orbital
    - trick

excerpt: So adding spin angular momentum on top of orbital angular momentum is like composing these 2 angular motions about 2 different origins together...

---

### Content

* A very general definition of [angular momentum](#angular-momentum-definition)
* Orbital, spin, total angular momentum. [What are they](#orbital-spin-total-angular-momentum)?
* Spin + Orbital = Total, [why](#spin-plus-orbital-equals-total)?
* Further [extension](#intuition-for-why)



### Angular Momentum Definition

Angular momentum is a concept meaningless unless defined relative to a point. Let's call this point our origin $O$. Now, we will place our frame of reference on this point for all later discussions.

Angular momentum of a point particle relative to $O$ is $\bold{L}=\bold{r}\times \bold{p}$ where $\bold{r}$ points from $O$ to this point particle and $\bold{p}$ is the momentum of the particle relative to $O$.  Angular momentum of a system of point particles is just the summation of individual angular momentum.

Angular momentum is the rotational analogue of momentum.

#### Is Momentum more fundamental

while angular momentum can be written with respect to momentum, that doesn't mean momentum is more fundamental. Angular momentum deals with rotational motion while momentum deals with translational motion.

Then you might ask: isn't all rotational motion microscopically translational motions. That is true, but all translational motion can also be perceived as rotational motions if you insert the origin/center of rotation infinitely far away.

A more precise way to distinguish rotational motion vs translational motion and angular momentum vs momentum is to invalidate the question itself. There's only motion, no such a physical construct as translational motion which is fundamentally different from angular motion. They are all just motion.

Translational motion and angular motion are simply 2 ways to describe motions (instead of to classify them). If you use a cartesian coordinate, your motions are described in translational terms. If you use a polar coordinate, your motions are described in angular terms. In practice, it's often good to use both coordinates simultaneously for problem solving.

#### However, angular momentum and momentum are NOT 2 sides of the same coin

They are locally the same.

Consider a ball doing circular orbital around $O$, instantaneously in a time $dt$, it turns an angle $d\theta$. Its angular momentum $L$ is unchanged during $dt$. We can also argue, by ignoring the little $d\theta$ it turned, that its momentum is unchanged since it's pretty much continuing its original path. In this way, we could "derive" angular momentum conservation from momentum conservation. What is flawed in my argument? The flaw is that the error due to ignoring $d\theta$ accumulates, eventually becoming significant.

To further convince you that they are "2 sides of the same coin", I will provide another example. Consider a system of particles, let's put our origin infinitely far away from them. Now $L=\sum r_i\times p_i$ (note that these are all vectors!) We can treat $r_i$ to be the same because $O$ is infinitely far away. So we pull $r_i$ out of the sum. $L=r\times \sum p_i=r\times p_{total}$. Since $r$ is fixed, conservation of $L$ is the same as conservation of $p$.

These 2 examples demonstrate the equivalence of angular momentum and momentum. But they only happen in the limiting cases. We must take $\lim \limits_{\frac{d\theta}{dt}\rightarrow 0}=\lim \limits_{w\rightarrow 0}$ and make $r\rightarrow \infty$ relative to the size of the system or object we consider.

In these limiting cases, the equation given by the 2 conservation laws can be equated. Otherwise, they are 2 separate laws providing different informations.

The reason why conservation of angular momentum and momentum are locally equivalent is because they both can be derived from Newton's Laws, which are laws instantaneous and local laws of physics.

### Orbital, Spin, Total angular momentum

I digressed, now let's dive in.

#### Orbital angular momentum

Orbital angular momentum of a system of particle about point $O$ can be defined as $L_{orbital}=r_{to\space CoM}\times p_{CoM}$. In other words, it only concerns with the motion of the center of mass of the system of particles.

#### Spin angular momentum

Spin angular momentum is the opposite. It only concerns with the motion of particles relative to the system's center of mass. So spin angular momentum is defined **relative to the Center of Mass (CoM) of the system** instead of $O$! $L_{spin}=r_{from\space CoM}\times p_{about \space CoM}$.

#### Total angular momentum

This is the angular momentum we know and defined [above](#angular-momentum-definition). It's a summation of angular momentum of individual particles relative to $O$. So it accounts for all motions: internal motions of particles as well as the net motion of the Center of Mass of the system. $L_{net}=\sum r_i\times p_i$

As incredulous as it sounds, $L_{orbital}+L_{spin}=L_{net}$ although $L_{spin}$ isn't even defined about the same point as the other 2!

Here's a proof!

### Spin plus Orbital equals Total

$L_{net}=\sum r_i\times p_i$. Notice $r_i=r_{to\space CoM}+r_{i \space from \space CoM}$. $r_{to\space CoM}$ is same for all particles, pointing from $O$ to $CoM$.

So $L_{net}=\sum r_{to\space CoM}\times p_i+r_{i \space from \space CoM}\times p_i$

Note that I applied the distributive property of cross product.

Here comes the magic: Pull $r_{to\space CoM}$ out

$L_{net}=r_{to\space CoM}\times\sum p_i+\sum r_{i \space from \space CoM}\times p_i$

$L_{net}=r_{to\space CoM}\times p_{net}+\sum r_{i \space from \space CoM}\times p_i$

Remember by definition $p_{net}=p_{CoM}$. You can also think of it as all the internal momenta got cancelled out.

So

$L_{net}=r_{to\space CoM}\times p_{CoM}$
$+\sum r_{i \space from \space CoM}\times p_i$

Do you recognize the two terms? Yes, the first if $L_{orbital}$ and the second is $L_{spin}$!

So $L_{net}=L_{orbital}+L_{spin}$ although they are not even relative to the same point!

### Intuition for why

You can think of it as composition of angular motion. To see what that means, let's look at composition of momentum. It works a bit differently (mostly due to the definition of center of mass).

Imagine a cannon moving with a cannon round. Their combined mass is $M$. The cannon just fired. The cannon round/ball moves at speed $v_b$ while the cannon moves at $v_c$. You can say the momentum of the launching system is $p_l=Mv_c$. The momentum of the ball relative to the cannon is $p_b=m_bv_{b\space to \space c}$ where $v_{b\space to \space c}$ is the speed of the ball relative to the cannon. Apparently, the total momentum $p_{total}=p_l+p_b=\sum m_i v_i$ for each object $i$ in the system.

Now, angular motion is similar. The moon orbits around earth with $L_{orbit}$ while the moon spins about its center of mass with $L_{spin}$. Notice that CoM, about which $L_{spin}$ is defined, is undergoing the orbital angular motion. So adding $L_{spin}$ on top of $L_{orbit}$ is like composing these 2 angular motions about 2 different origins together. It's similar to composing the two linear motions together in the cannon example.

Of course, you cannot add any 2 angular momentum together. You add the 2 momentum together in the cannon case because 1 of the momentum $p_1$ is defined with its frame of reference moving at $p_2$. Or in other words, you can only compose 2 motions if the frame of reference of one is undergoing the other motion.





Happy reading!