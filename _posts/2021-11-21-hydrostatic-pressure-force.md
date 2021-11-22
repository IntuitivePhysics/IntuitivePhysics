---
layout: post

title: Hydrostatic Pressure Force on a Surface in Fluid

author: Michael Huang

description: Consider any surface submerged in a liquid. What is the pressure force and torque exerted by the liquid on the surface?

tags:
    - fluid mechanics
    - hydrostatics
    - engineering
    - pressure
    - force analysis
    - moment of inertia
    - mechanics

excerpt: Therefore, dimensional-analysis is all about extracting relationships based on dimensional homogenity and reducing the equation down to only dealing with dimensionless constants that don't depend on the basis we choose...

---

Consider any surface submerged in a liquid. What is the pressure force and torque exerted by the liquid on the surface? Force analysis on the liquid gives a simple solution to that! No experience with integral needed; I will give a physical explanation for everything in this post.

### Pressure Force on a Plane

First we consider the case of a plane, tilted at an angle from the surface of the liquid. The reason we first consider a plane is because we will eventually reduce any curved surface to planes through projection. OK, I lied before, we will need a tiny little bit of calculus to derive the formula for the plane. Before we begin, when we talk about force, there's really 3 parts: 1. Magnitude 2. Line of action; in this section we only find the magnitude and the direction of the force; we treat the line of action in the next section where it will be used to find the torque on the plane. 

![pressure](../assets/images/pressure.svg)

If we would like to find the pressure force exerted on the top part of the plane, we first note that the force is in the direction of $\vec{A}$, normal to the plane. We note also that the pressure force on the bottom of the plane cancels exactly with that of the top due to the fluid static equilibrium condition. Now, for an infinitesimal area $\vec{dA}$, the pressure force on it is $\vec{dF}=p \vec{dA}$. Taking the area integral
$$
\vec{F} = \iint_A \vec{dF} = \iint_A p\vec{dA} = \iint_A \rho g \Delta h dA = \rho g \iint_A \Delta h dA
$$
Notice that $\iint_A \Delta h dA$ is simply the the average $\Delta h$ over the entire area, which is $\Delta h_\text{CoA} A$ where CoA stands for the Center of Area. Thus $\vec{F} = \rho g \Delta h_\text{CoA} A$, or in other words the average of the pressure force times area. We can only take the average because the pressure force varies linearly across $A$.

### Pressure Torque on a Plane

What's the torque exerted about the CoA? Or more generally the CoP (Center of Pressure)? Let's say the plane forms an angle $\theta$ with the liquid surface. 

![pressure](../assets/images/pressure.svg)

Let's define a coordinate system at $CoA$ with $y$ axis pointing downward along the plane. Now we integrate the torque
$$
\tau=\iint_A \rho g \sin(\theta)  (y+\Delta y_\text{CoA}) y dA \\
=\rho g \sin(\theta) \left(\iint_A y^2 dA + \Delta y_\text{CoA}\iint_A y dA\right) \\
$$
Because $\iint_A y dA = y_\text{CoA} = 0$. 
$$
\tau=\rho g \sin(\theta) \iint_A y^2 dA \\
$$
Notice that $\iint_A y^2 dA$ is called the area moment (it appears in the integral when we compute moment of inertia). Assume the plane is length $l$ and width $b$, we perform the integration as follows
$$
\iint_A y^2 dA = \iint_{-l/2}^{l/2} by^2 dy = b \left.\frac{y^3}{3}\right|_{-l/2}^{l/2} \\
= \frac{bl^3}{12}
$$
This looks strikingly like the moment of inertia of a rod and a plane! Only that there's one more $l$ on the top! If only we can get rid of that somehow... If we plug it back in to $\tau$,
$$
\tau = \rho g \sin(\theta) l \frac{bl^2}{12} \\
= \rho g (\sin(\theta)l) \frac{bl^2}{12}
$$
Now it's clear that $\frac{bl^2}{12}$ represents the moment of inertia if the plane's density is $1$. $\sin(\theta) l = \Delta h_\text{over A}$, there fore $\rho g \Delta h_\text{over A}$ represents the change in pressure going from the top of the plane to the bottom. We call it $\Delta p$. 
$$
\tau = \Delta p I_\text{unit density} \\
= \frac{\Delta p}{\sigma} I
$$
where $\sigma$ is the density. Now this looks terribly familiar! If we recall Newton's 2nd law for rotation:
$$
\tau = \alpha I
$$
surely that rings a bell? Yes! The angular acceleration corresponds to $\frac{\Delta p}{\sigma}$, the change in pressure over the density, which makes sense because pressure difference is like a force on the unit width beam and over density is just over mass for unit width beam, giving you some kind of acceleration. This is much more intuitive than our original equation involving the 2nd integral!

One last comment: we can find the line of action of the pressure force by simply dividing the $\tau$ by the magnitude of the pressure force found in the first section, because it is defined that $F_\text{net}r_\text{to line of action} = \tau$. 

Try to derive the position of the line of action for the simplified case when the top part of the plane touches the surface of the liquid! Why is it this particular number? Is there a way to intuitively understand it? As a hint, consider the triangular prism of liquid right above the plane!

### On any Curved Surface

Ok, I lied, we are not ready to deal with **any** curved surfaces yet with the method that described in this section. Nonetheless, it simplifies any curved surface and is a crucial tool in fluid statics. Consider curved surface A below (simplified to 2D; it's represented by curve A). We can fill in a fluid element by constructing imaginary boundaries B, C, D. By fluid static equilibrium, the net force on the element is $0$. To simplify the problem, let B touch the surface of the liquid. We can ignore atmospheric pressure in many engineering applications (why?), so we do that here.

![pressure_curve1](../assets/images/pressure_curve1.svg) 

We can compute $F_C, F_D$ by the formula introduced in the last two sections. $G$ requires an often simple integral to compute. $F_A$ must balance the three out. So by $F_\text{net}=0$, we can obtain the $x,y$ components of $F_A$ and thus both its magnitude and direction. What remains is its line of action.



![pressure_curve2](../assets/images/pressure_curve2.svg)

If we consider the point of intersection of $F_C, F_D$ (you can use any other point), we need the net torque about this point to be $0$. Thus $F_A$'s torque cancels out with that of $G$'s and with this equation the precise location of the line of action of $F_A$ can be determined. 