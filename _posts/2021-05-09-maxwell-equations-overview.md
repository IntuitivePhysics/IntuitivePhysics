---
layout: post

title: Maxwell's Equations explained with Lorentz Force Law

author: Michael Huang

description: An intuitive explanation of Lorentz force law and Maxwell's Equations in integral form and differential force, with focus on their interconnections and individual roles.

tags:
    - electromagnetism
    - faraday
    - maxwell
    - lorentz
    - ampere
    - gauss
    - overview

excerpt: each law of electromagnetism governs 1 of the 6 directions of interactions between the 3 objects, the electric field, magnetic field, and charge...

redirect_from:
    - /electromagnetism/Overview-of-the-5-laws-of-electromagnetism,-and-their-interconnection/
    - /2021/05/09/Overview-of-the-5-laws-of-electromagnetism,-and-their-interconnection.html
---

Let's show the formula first...

### Formula

$$
\nabla\cdot \textbf{E}=\frac{\rho}{\epsilon_0}
\\
\nabla\cdot \textbf{B}=0
\\
\nabla\times \textbf{E} = -\frac{\partial \textbf{B}}{\partial t}
\\
\nabla\times \textbf{B} = \mu_0 \textbf{j} + \mu_0\epsilon_0 \frac{\partial \textbf{E}}{\partial t}
\\
\textbf{F}=q(\textbf{E}+\textbf{v}\times\textbf{B})
$$



### Why are these the fundamental equations of Electromagnetism?

Because electromagnetism is all about the interaction between 3 objects: electric field, magnetic field, and charge. These 5 formula gives the complete laws of interaction between these 3 objects, and so they're fundamental and constitute the entire theory of electromagnetism.
$$
\textbf{E} \Longleftrightarrow \textbf{B}
\\
\textbf{E},\textbf{B} \Longleftrightarrow Q
$$

#### sidenote:

Technically the equations presented above are not the most fundamental equations of electromagnetism. This is because we wrote the Maxwell's Equations in its differentiable, which presumes that discrete charges are small enough to be approximated by a continuum of charge. Technically, to get the most fundamental Maxwell's Equations in classical physics, we ought to write:
$$
\iint \limits_{\partial\sigma} \textbf{E}\cdot \textbf{dA} = \sum \limits_\sigma \frac{q}{\epsilon_0}
$$
And etc...

So, just remember that the premise of differential form of Maxwell's Equations is that charges are not discrete, but approximated as a continuum. So $\rho \lt \infty$ always.



### What does each equation do individually?

#### Gauss's Law

$\nabla \cdot \textbf{E}=\frac{\rho}{\epsilon_0}$ can be viewed as an equation governing how charge affects electric field. It says: a charge density of $\rho$ produces a divergence of magnitude $\frac{\rho}{\epsilon_0}$ in the electric field. (divergence just means how much electric flux density is generated at that point, or, to put in more common linguo, how much field line originate from that point per unit volume).

#### Gauss's Law for Magnetism

$\nabla \cdot \textbf{B}=0$ says pretty much the same thing. The divergence of magnetic field is always 0. If you think of the velocity field of any incompressible fluid, its divergence must also be zero (since 0 field line/fluid originate from a certain point). This governs how a static charge affects $\textbf{B}$ field: it does nothing to it (however, a moving charge does affect magnetic field).



So the two Gauss's Laws tells us how charge affects $\textbf{E}$ and $\textbf{B}$ fields. And colloquially,  they tell us that charges create "sinks" or "sources" in electric field, but they don't create "sources" and "sinks" in magnetic field.

They represent $Q_{positional}\rightarrow \textbf{E},\textbf{B}$ direction of interaction

#### sidenote:

To be more precise, we may separate the discussion of the divergence and curl of $\textbf{E}, \textbf{B}$ fields. The two Gauss's Laws gives us the divergence of the two fields. The divergences of the 2 fields are only affected by the location of charge, which is rather interesting.



#### Maxwell-Faraday's Law

$\nabla\times \textbf{E} = -\frac{\partial \textbf{B}}{\partial t}$

Note its difference from [Faraday's Law](https://intuitivephysics.me/faraday-derivation-part1). This law governs how a changing $\textbf{B}$ field affects $\textbf{E}$ field, or generate a curl, specifically. So, it represents $\textbf{B}\rightarrow \textbf{E}$ direction of the interaction.



#### Ampere's Law

$\nabla\times \textbf{B} = \mu_0 \textbf{j} + \mu_0\epsilon_0 \frac{\partial \textbf{E}}{\partial t}$

This is extremely similar to Maxwell-Faraday's Law. It's pretty much its opposite. It governs how a changing $\textbf{E}$ field affect $\textbf{B}$ field, or generate a curl in $\textbf{B}$ field. It gives the direction $\textbf{E}\rightarrow \textbf{B}$.

However, there's a bit more to it: the equation also involves $\textbf{j}$ current density. So the law also governs how **movement of charge** affects $\textbf{B}$ field. As a natural question: why is there this $\textbf{j}$ term, which seems to get in the way of the harmony of Maxwell's Equations? We will explore that in a later post.



Last but not least (in fact, perhaps most important)

#### Lorentz Force Law

$\textbf{F}=q(\textbf{E}+\textbf{v}\times\textbf{B})$

It gives how $\textbf{E}$ field and $\textbf{B}$ affect charge, so it provides this direction of interaction $\textbf{E},\textbf{B}\rightarrow Q$. It's not a Maxwell's Equation because, unlike the other four, it doesn't describe electromagnetic field (or $\textbf{E}$ and $\textbf{B}$). Instead, it describes how charges are affected by them.



### Conclusion

As we've seen, each law of electromagnetism governs 1 of the 6 directions of interactions between the 3 objects: electric field, magnetic field, and charge.
$$
\textbf{E} \Longleftrightarrow \textbf{B}
\\
\textbf{E} \Longleftrightarrow Q
\\
\textbf{B} \Longleftrightarrow Q
$$
A reason why there're only 5 equations instead of 6 is that Lorentz Force Law actually has 2 components separate components $\textbf{F}=q\textbf{E}$ and $\textbf{F}=q\textbf{v}\times \textbf{B}$. So it actually contains 2 pieces of information and 2 directions of the interactions.