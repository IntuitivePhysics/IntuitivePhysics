---
layout: post

title: How and why dimensional analysis works, a mathematical take

author: Michael Huang

description: Dimensional analysis is an engineering method to model relationship between variables. But why does it work? 

tags:
    - dimensional analysis
    - fluid mechanics
    - engineering
    - modeling
    - linear algebra
    - math
    - mechanics

excerpt: Therefore, dimensional-analysis is all about extracting relationships based on dimensional homogenity and reducing the equation down to only dealing with dimensionless constants that don't depend on the basis we choose...

---

Dimensional analysis is a method for modeling relationships between variables in all sciences, particularly in physics. 

This blog post is all about why dimensional analysis (aka. Buckingham Pi theorem, etc) work. It explains the mathematical principle behind this method. 

### Content

- Principle of [Dimensional Homogenity](#dimensional-homogenity)
- How and why of [Dimensional Analysis](#dimensional-analysis)
- [Buckingham Pi Theorem](#pi-theorem) brief explanation

### Dimensional Homogenity

Dimensional homogenity means that all additive terms in a legitimate physical equation should have the same dimensions. We can infer information about relationships between variables from it. 

For example, we know that $x = \frac{1}{2}gt^2$ can be a valid equation while $x = \frac{1}{2}g^2 t$ cannot be a valid equation. 

Dimensional analysis is about exploiting the information contained in the assumption of dimensional homogenity to establish certain relationships between variables without having to perform experiments on them in multiple settings. 

### Dimensional Analysis

Let's say we want to model the relation of drag force $F$ _w.r.t._ $\rho, v, L$ where $v$ is the velocity of air and $L$ is the length scale of the object. Without any experimentation we know that 

$$
F\propto \rho v^2 L^2 
\\
F = k \rho v^2 L^2
$$

is necessary for the dimensions to work out (assuming polynomial dependency).

There are 3 standard basis dimensions here $[L], [T], [M]$. Thus, for dimensional homogenity, we have 3 equations with 3 unkowns (the exponents of $\rho, v, L$). Since $\rho, v, L$ form a linearly independent basis, there's one unique solution.

In this way, we have modeled **all** of $F$'s dependence on $\rho, v, L$. In other words, let $F = k \rho v^2 L^2$, then $k$ has no dependence on $\rho, v, L$. Because $\rho, v, L$ are linearly independent in terms of dimensions, there's no combination of them that results in a dimension-less quantity (or more simply, we can understand it as in solving the exponents, there is one and only one solution). 

Therefore, dimensional-analysis is all about extracting relationships based on dimensional homogenity and reducing the equation down to only dealing with dimensionless constants that don't depend on the basis we choose (in this case, $\rho, v, L$ is our basis/repeating variable).

Once we consider $\rho, v, L$ as the basis, we may flip the equation to 
$$
k = \frac{F}{\rho v^2 L^2}
$$

In other words, $k$ is the magnitude of $F$ expressed in the basis of $\rho, v, L$. Or you can consider $k$ to be $F$ normalized by $\rho, v, L$. 

If we factor into consideration the effect of $\mu$, viscosity, then 
$$
F = f(\rho, v, L, \mu)
$$

Generally, dimensional analysis is applied in the following context:
Given certain fixed environmental independent variables $\rho, v, L$, we want to model $F\text{ vs } \mu$ (varying $\mu$ and measuring the corresponding $F$ values; since $\mu$ is independent, there's expectedly a legitimate function relationship that maps $\mu$ to $F$).

The gist is: if we model this relationship $F=g(\mu)$ directly, it's a function with coefficients dependent on $\rho, v, L$ and so need to be reperformed for each $\rho, v, L$ values (or the effect of $\rho, v, L$ must be determined). So, we want to model a relationship $F' = g(\mu')$ such that the function's coefficients have no dependency on $\rho, v, g$. The main idea is that if we let $F'$ equal to $F$ normalized by its dependency on $\rho, v, g$ and $\mu'$ equal to $\mu$ normalized by its dependency on $\rho, v, g$, we intuitively know that the function created should have no dependency on $\rho, v, g$. 

In multivariate setting, the intuition doesn't give the proof. How do we know $k$ has no dependency on $\rho, v, g$? Previously, we know $k$ cannot be a function $f(\rho,v,g)$ because they are linearly independent and cannot form a dimensionless quantity. Now, how do we know $k$ cannot be $f(\rho,v,g,\mu)$, which is not linearly independent? 

One way to think about this is to realize that for $\rho, v, g, \mu$ to form a dimensionless quantity, it has to be a scaled version of $\frac{\mu}{\rho v g} = \frac{1}{Re}$, the other dimensionless quantity in question. So therefore, we conclude that $k$ can only depend on $\frac{1}{Re}$. In other words, the normalized $F$ only depends on the normalized $\mu$. 

Is it true in general that a dimensionless quantity can only depend on other dimensionless quantities? Yes! Imagine if dimensionless quantity $x$ is a result of the multiplication of several dimensional variables. If we replace all non-basis dimensional variables with its representation in our chosen basis, then we get on the right hand side a formula with only the basis variables, which has to be equal to empty dimension as on the left hand side. This forces all the basis variables to have net exponent of $0$ and the only things that remain are dimensionless quantities. 

Therefore, to model $F \text{ vs } \mu$, we can model $F' \text{ vs } \mu'$ where the latter function is guaranteed to not be dependent on the basis $\rho, v, L$. 

### Pi Theorem

Given the interpretation of dimensionality analysis, the Buckingham Pi Theorem becomes easy to understand. 

The theorem states
_If an equation satisfies the principle of dimensional homogenity and has $n$ dimensional variables, it can be reduced to a relationship between $k$ dimensionless variables or $\Pi s$. Let $j=n-k$. $j$ is the max number of variables that don't form a pi among themselves and is always $\le$ the number of fundamental dimensions involved._

The "number of fundamental dimensions" is simply the maximum number of base-variables. Forming "a pi" basically indicates a group of variables is linearly dependent. So the statement becomes $j$ is the largest number such that there are $j$ variables that are linearly independent. In other words, $j$ is the number of base-variables in vectorspace formed by the span of all variables. With a basis with $j$ variables chosen, we can of course normalize the remaining $n-j=k$ variables and represent them _w.r.t._ the basis.  