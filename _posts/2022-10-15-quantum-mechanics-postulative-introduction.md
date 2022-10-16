---
layout: post

title: Terse Postulative Introduction to Quantum Mechanics

author: Michael Huang

description: Let me reorganize and summarize Griffith's Chapter 1 to 4 in a couple of pages for you. 

tags:
    - quantum
    - mechanics
    - griffith
    - postulate
    - schrodinger
    - hilbert space

excerpt: Let me reorganize and summarize Griffith's Chapter 1 to 4 in a couple of pages for you.
---

This is essentially a brief postulative reformulation of the theoretical content of quantum mechanics; it covers most of the theory in Griffith's Chapter 1 to 4. 

### Content

1. [Hilbert Space](#hilbert-space)
2. [Generalized Statistics Interpretation](#generalized-statistics-interpretation)
3. [Schrodinger's Equation](#schrodinger-equation)
4. [How to apply Quantum Mechanics](#how-to-apply-quantum-mechanics)

### Hilbert Space

##### Vectors can be infinite dimensional

Vectors are usually represented by a finite dimensional tuple $(a_1, a_2, a_3)$. It is more general to represent a vector with an integer valued function $f$ such that $f(1)=a_1$, $f(2)=a_2$, $f(3)=a_3$. In other words, the function $f$ takes as input an index and output the value corresponding to that index for the vector. 

Thus, vectors can be generalized to infinite dimensions $ (a_1,a_2,a_3,\cdots) $ by extending the domain of $f$ to all natural numbers $\mathbb{N}$. We can further generalize infinite dimensional vectors by making the number of dimensions uncountable--we can allow an index to the vector to be any real number (or even complex number). Thus, any function $f$ could be perceived as a representation of a vector whereby the value corresponding to the $x^\text{th}$ index is $f(x)$. We will henceforth use $|f\rangle$ to denote a vector that is represented by the function $f$. 

##### Inner product

The **inner product** of two countable vectors $|a\rangle$, $|b\rangle$ is represented by,

$$
\langle a | b\rangle = \sum_i a_i^\star b_i.
$$

This weird $\langle a | b\rangle$ notation is called the **bracket notation**. It should be conceived of as an operator $\langle a|$ operating upon a vector $|b\rangle$ whereby the operation is performing inner product between $|a\rangle$ and $|b\rangle$. 

For uncountable vectors $|f\rangle$ and $|g\rangle$, the inner product is defined by,

$$
\langle f | g\rangle = \int f(x)^\star g(x) dx.
$$

The norm of a vector $|f\rangle$ is $\langle f | f\rangle$. Notice that the norm is always a positive number. 

A discrete set of vectors $\{|a_1\rangle,|a_2\rangle,\cdots,|a_n\rangle\}$ is **orthonormal** if $\langle a_i | a_j\rangle = \delta_{ij}$, where $\delta_{ij}$ is a shorthand notation that basically means the value is $1$ if $i=j$, otherwise the value is $0$. 

A continuous set of vectors $\{|x\rangle \mid x\in \mathbb{R}\}$ is **orthonormal** if $\langle x' | x\rangle = \delta(x-x')$, where $\delta$ is the Dirac delta function. Basically, $\delta(x-x')=0$ if $x\not=x'$ and satisfies the property that $\int_x \delta(x-x') dx = 1$ (when $x=x'$, $\delta(x-x')$ is technically infinite/undefined).  

##### Hilbert space definition


In physics, **Hilbert space** is an infinite dimensional vectorspace over the scalar field of complex numbers. If that sentence confused you, I recommend that you take a look at [linear algebra](https://jeremykun.com/2011/06/19/linear-algebra-a-primer/). Hilbert space further satisfies the property that the norm of any vector is finite. 

An infinite dimensional vectorspace requires an infinite set of basis. Let $\{|x\rangle \mid x\in \mathbb{R}\}$ be a set of orthnormal basis. To clarify, there's a unique vector $|x\rangle$ corresponding to each real scalar $x$. Any vector $|\psi \rangle$ can be represented as a linear combination of $|x\rangle$. Clearly, $\langle x| \psi\rangle$ picks out the component of $|x\rangle$ in $|\psi \rangle$. Therefore, we can rewrite,

$$
|\psi \rangle = \int dx |x\rangle \langle x| \psi \rangle.
$$

For this reason, $\int dx |x\rangle \langle x|$ as a whole is called a unit operator. 

##### Operator, eigenstates, and eigenvalues

It may appear that all this discussion of vectors in Hilbert space is irrelevant to physics. The reason we spent some time treating the subject of a Hilbert space is because the physical state of particle can be represented as a vector in the Hilbert space. We will use $|S\rangle$ to denote a Hilbert space vector that represents the physical state of a particle.

To obtain some observables (position, momentum, energy, etc) from this physical state, we need to operate on the state $|S\rangle$ using linear operators. Each physical observable corresponds to a linear operator. 

The position operator is denoted by $\hat{x}$, the momentum $\hat{p}$, and the Hamiltonian/energy $\hat{H}$. So what does the operator do? Can we write it out? Nope. Operator is an abstract thing like a vector. It is possible to write out the representation of a vector on a basis, but the vector is the vector itself. Similarly, it is possible to explain what an operator do to the different components of a representation of a vector in a certain basis, it is not possible to abstractly define what an operator does. 

These operators all have eigenstates and corresponding eigenvalues. The eigenstates of $\hat{x}$ are defined to be the set of vectors $\{|x\rangle \mid x\in \mathbb{R}\}$ and the corresponding eigenvalue for an eigenstate $|x\rangle$ is the scalar $x$. The eigenstates of $\hat{x}$ form an orthonormal basis. 

Similarly, the eigenstates of $\hat{p}$ are defined to be the set $\{|p\rangle \mid p \in \mathbb{R}\}$ where each eigenstate $|p\rangle$ has an eigenvalue $p$. 

For any operator that corresponds to a physical observable, it turns out that its eigenstates necessarily form an orthonormal basis of the Hilbert space. This interesting result is because of the fact that operators that correspond to physical observables are **Hermitian**, which you may take as a postulate. 

So, at this point, we have, 

$$
|S\rangle = \int dx |x\rangle \Psi(x) \\
= \int dp |p\rangle \Phi(p)

$$

Reversedly, 

$$

\Psi(x) = \langle x|S\rangle \\
\Phi(x) = \langle p|S\rangle

$$

##### Relationship between position and momentum operator

These variables are what represent the vector $|S\rangle$ in different basis. Our next enterprise is to relate them to each other by relating the basis $|x\rangle$, $|p\rangle$. The relation between the operators and basis is significant because it turns out that the law of quantum physics (Schrodinger's Equation) is written in terms of the Hamiltonian operator. Thus, an operator is quite useless if we cannot relate it to the Hamiltonian operator. Further, it turns out that we need to first establish a connection between $\hat{x}$ and $\hat{p}$ in order to properly introduce the Hamiltonian operator. 

To relate the operators, we need two more postulates. First, we take as postulate the **position momentum operator relation**,

$$
\langle x|\hat{p}|\psi \rangle = -i\hbar \frac{\partial}{\partial x} \langle x|\psi\rangle.
$$

It should be noted that most people would start with the postulate $\langle x|p\rangle - \langle p | x\rangle = i\hbar$, but we will not since Griffith doesn't. 

Let me explain this postulate more intuitively. It is essentially saying that the $\hat{p}$ operator, when projected along $\langle x|$, is essentially taking the derivative of the $|x\rangle$ component of $|\psi\rangle$. 

$$

\langle x|\hat{p}|\psi \rangle = -i\hbar \frac{\partial}{\partial x} \langle x|\psi\rangle \\
\langle x|\hat{p}|p \rangle = -i\hbar \frac{\partial}{\partial x} \langle x|p\rangle \\
p \langle x|p \rangle = -i\hbar \frac{\partial}{\partial x} \langle x|p\rangle.

$$

This can be solved as a differential equation, viewing $\langle x|p\rangle$ as a function of $x$, giving,

$$
\langle x | p\rangle = Ae^{ipx/\hbar}.
$$

$|p\rangle$ is orthonormal. This fact may help us determine $A$. 

$$

\langle p|p'\rangle = \left( \int dx |x\rangle \langle x| p\rangle \right)^\dagger \left( \int dx |x\rangle \langle x|p'\rangle \right) \\
= \left( \int dx |x\rangle^\dagger \langle x| p\rangle^\star \right) \left( \int dx |x\rangle \langle x|p'\rangle \right) \\
= \iint dx dx' \langle x | x'\rangle \langle x| p\rangle^\star \langle x'|p'\rangle \\
= \iint dx dx' \delta(x-x') \langle x| p\rangle^\star \langle x'|p'\rangle \\
= \int dx \langle x|p\rangle^\star \langle x|p'\rangle \\
= |A|^2\int dx \langle x e^{ix (p'-p)/\hbar } \\
= |A|^2 2\pi \hbar \delta(p-p').

$$

The last step is due to the fourier decomposition of $\delta$ function. Thus, we may let $A = \frac{1}{\sqrt{2\pi \hbar}}$.

We have therefore derived that,

$$

    \langle x | p \rangle = \frac{1}{\sqrt{2\pi \hbar}}e^{ipx/\hbar} \text{  and }\\
    \langle p | x \rangle = \frac{1}{\sqrt{2\pi \hbar}}e^{-ipx/\hbar}.

$$

We may henceforth take these as fundamental theorems.

Now, given the relation between these two basis, we may represent one basis in terms of another, which will aid us in transforming between basis. 

$$

    |x \rangle  = \int dp \langle p | x \rangle | p \rangle \\

$$

A vector $|S\rangle$ may thus be represented in two manners,

$$

    |S\rangle = \int dp |p \rangle \Phi(p)  = \int dx  |x \rangle \Psi(x)\\
    = \iint dx dp \langle p | x \rangle | p \rangle \Psi(x)\\
    = \int \left(dp |p \rangle \int dx \langle p | x \rangle \Psi(x) \right). \\

$$

Thus, the equivalence of,

$$

    \Phi(p) = \int dx \langle p | x \rangle \Psi(x) \\
    = \int dx \frac{1}{\sqrt{2\pi \hbar}} e^{-ipx /\hbar} \Psi(x)

$$

can be established in an intuitive fashion. The symmetric reverse is,

$$

    \Psi(x) = \int dp \langle x | p \rangle \Phi(p)

$$

We have now derived the relation between $\{|x\rangle\}$ and $\{|p\rangle\}$. We also obtained from that the relation between $\Psi$ and $\Phi$, the two representations of a wavefunction $|S\rangle$ in the position basis and the momentum basis. Now, time is ripe to introduce the Hamiltonian operator. 

 ##### Other operators

Notice that any classical observable $Q$ can be represented as a combination of $x$ and $p$ via a function $Q(x,p)$. We take as the third postulate that the operator corresponding to $Q$ results from the same combination of $\hat{x}$ and $\hat{p}$. In other words, $\hat{Q} = Q(\hat{x}, \hat{p})$. Thus, following this postulate, the Hamiltonian operator is defined as,

$$
\hat{H} = \frac{\hat{p}^2}{2m} + V(x).
$$

Hamiltonian operator is most commonly expressed in the $\{|x\rangle\}$ basis, so let's do that,

$$

\langle x| \hat{H} |\psi \rangle = \frac{1}{2m}\langle x|\hat{p}^2 |\psi\rangle + V(x) \langle x |\psi\rangle \\
= \left(-\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V \right)\langle x|\psi\rangle

$$

You would recognize this as the familiar form of the Hamiltonian operator if you have exposure to quantum mechanics before. An interesting insight can be obtained if we let $|\psi\rangle$ equal to the eigenstate of the Hamiltonian operator. Let the eigenstate be $|n\rangle$ and the eigenvalue be $E_n$, the equation becomes,

$$
\langle x|\hat{H}|n\rangle  = \left(-\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V \right)\langle x|n\rangle \\
E_n \langle x|n\rangle = \left(-\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V \right)\langle x|n\rangle
$$

This can be perceived as a differential equation, whereby $\langle x|n\rangle$ is a function of $x$. This differential equation is known as the time-independent Schrodinger's Equation. It's given a fancy name although it follows trivially from the definition of the Hamiltonian operator. Solving this equation gives us $\langle x|n\rangle$ which finally connects all three basis $\{|x\rangle\}$, $\{|p\rangle\}$ and $\{|n\rangle\}$. 

### Generalized Statistics Interpretation

So now we know $|S\rangle$ is a vector that corresponds to a physical state, and that $\hat{x} |S\rangle$ somehow tells us something about the positional information of a particle at physical state $|S\rangle$, how do we exactly know the position of the particle? 

The generalized statistics interpretation is what connects the mathematics with physics. Let $\{|x\rangle\}$ be an orthonormal basis that are the eigenstates of $\hat{x}$ with corresponding eigenvalues $\{x\}$. We know that,

$$
|S\rangle = \int dx |x\rangle \Psi(x)
$$

where $\Psi(x) = \langle x|S\rangle$ is just a scalar valued function. Then, the generalized statistics interpretation states that the probability density of measuring the eigenvalue $x$ is $\Psi(x)^2$. In other words, the only values we can possibly measure are the eigenvalues of $\hat{x}$; the probability of measuring each eigenvalue is the square of the component of that eigenvalue's eigenstate in the state the particle is in. The general statistics interpretation is the fourth postulate of quantum mechanics. 

From this definition, we can readily derive that the expected observed position $\langle x\rangle$ satisfies,

$$
\langle x \rangle = \int x |\langle x| S\rangle|^2 dx = \int x \Psi^\star \Psi dx \\
= \int dx \langle x|S\rangle^\star \langle x|\hat{x}|S\rangle \\
= \int dx \langle S|x\rangle \langle x|\hat{x}|S\rangle \\
= \langle S| \left(\int dx |x\rangle \langle x|\right)\hat{x}|S\rangle \\
= \langle S| \hat{x}|S\rangle 
$$

By the same reasoning, any general observable $\hat{Q}$ has expected value $\langle S| \hat{Q} |S\rangle$. 

### Schrodinger Equation

The first section of this article is on the mathematics of quantum mechanics. The second section is on the connection between the math to physics. This final one is about physics. Physics is all about predicting the future state of a particle/system based on its past. And that's what Schrodinger's Equation does--you can take it as the fifth postulate. It's deceptively simple:

$$
i\hbar\frac{\partial |S\rangle}{\partial t} = \hat{H} |S\rangle
$$

We may also write it in terms of the $\{|x\rangle\}$ basis, which is what most introductory textbooks do,

$$
 \langle x| i\hbar \frac{\partial |S\rangle}{\partial t} = \langle x|\hat{H}|S\rangle \\
 i\hbar \frac{\partial \langle x|S\rangle}{\partial t} = \left(-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2} +V\right) \langle x | S\rangle \\
 i\hbar \frac{\partial \Psi(x)}{\partial t} = \left(-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2} +V\right) \Psi(x)
$$

### How to apply Quantum Mechanics

The great thing of a postulative introduction is that it is very terse and gives somewhat of a big picture without glossing over too much details. But a problem with it is that you can totally read the first 3 parts of this article and walk away with no clue at all about how to apply quantum mechanics. That is what this final section addresses--for those petty engineers who care about applications. 

Usually, in a quantum mechanics problem (as in any other physics problem), you are given an initial state $|S(0)\rangle$ and you want to find the state at time $t$, $|S(t)\rangle$. 

Or more realistically, you are given an initial state's representation in some basis. Usually it is the position basis. So, in most cases, you start with $\Psi(x,0)$. You with to derive $\Psi(x,t)$ or $\Phi(p,t)$ or $E_n(t)$. It doesn't matter. You can always convert between them based on what we learned in the [first part](#hilbert-space) of the article. 

The magic formula is always the same:

##### Part 1

Find the eigenstates and eigenvalues of the Hamiltonian operator $\bar{H}$ in the basis in which the initial state $|S(0)\rangle$ is given. We need to find it each time because it is dependent on the potential function $V$. This is done by solving the so-called time-independent Schrodinger's equation,

$$
E_n\langle x|n\rangle = \left(-\frac{\hbar^2}{2m} \frac{\partial^2}{\partial x^2} + V \right)\langle x|n\rangle
$$

because $\langle x|n\rangle $ gives us a representation of eigenstate $|n\rangle$ in the $\{|x\rangle\}$ basis. Note that if you are given $\Phi(x,0)$ instead of $\Psi(x,0)$, you should solve for $\langle p|n\rangle$ instead.

##### Part 2

Represent the original state $|S(0)\rangle$ in terms of the Hamiltonian eigenstates $|n\rangle$. 

$$
|S(0)\rangle = \sum_n c_n(0) |n\rangle \\
$$

So, we essentially want to transform the position basis wavefunction representation $\Psi(x,0)$ to the Hamiltonian basis. 

$$
|S(0)\rangle = \int dx |x\rangle \Psi(x,0) \\
= \int dx \Psi(x,0) \sum_n \langle n|x\rangle |n\rangle \\
= \sum_n |n\rangle \int dx \langle x|n\rangle^\star\Psi(x,0)
$$

Clearly, 

$$
c_n(0) = \int dx \langle x|n\rangle^\star\Psi(x,0)
$$

##### Part 3

Plug $|S(0)\rangle$ back into the Schrodinger's Equation. 

$$
i\hbar\frac{\partial}{\partial t}\sum_n c_n |n\rangle = \hat{H} \sum_n c_n |n\rangle \\
i\hbar \sum_n |n\rangle\frac{\partial c_n}{\partial t} = \sum_n c_n E_n |n\rangle
$$

Because $\{|n\rangle\}$ are linearly independent, it must be that each component of $|n\rangle$ must equal for the overall equality to hold,

$$
i\hbar\frac{\partial c_n}{\partial t} = c_n E_n \\
c_n = c_n(0) e^{\frac{E_nt}{i\hbar}}
$$

Now, $c_n$ is found, thus $|S\rangle$ is found in terms of energy basis. It can be translated into other basis easily. 
