---
layout: post

title: Faraday's Law of Electromagnetic Induction, derivation and misconceptions.

author: Michael Huang

description: An intuitive derivation of Faraday's Law of Electromagnetic Induction, and some explanations of its difference from Maxwell-Faraday's Equation.

tags:
    - electromagnetism
    - faraday
    - maxwell
    - lorentz
    - derivation
    - misconception

excerpt: The only fundamental theorem of electromagnetims we used above is the Lorentz Force Law. So, in other words, this Motional Faraday's Law should have equal predictive power to the Lorentz Force Law...

redirect_from:
    - /2021/05/08/Faradays-Law,-derivation-and-misconceptions.html
    - /electromagnetism/Faradays-Law,-derivation-and-misconceptions/
---

### Part 1

This is part 1 of two articles on Faraday's Law. In the first part, I attempt to clear up some confusions about the different forms of Faraday's Law and provide a simple derivation of Faraday's Law. In the second part, we explore some quirks and "exceptions" of Faraday's Law.

### Contents

#### Part 1

1. The 3 confusing forms of [_Faraday's Law_](#faradays-law)
2. [Derivation](#derivation-of-faradays-law) of Faraday's Law and motional EMF
3. Grand [Conclusion](#conclusion) and last thoughts

#### Part 2

1. Several exceptions to Faraday's Law and why they are exceptions
2. Final Puzzle

### Faraday's Law

See [Maxwell's Equations](/maxwell-equations-overview) for a brief and intuitive intro to all Maxwell's Equations and Lorentz force law.

I've read 3 different textbooks on electromagnetism. Each provided a different description of what it defines as Faraday's Law.

#### Definitions

##### First Definition:

$$\mathcal{E}=-\frac{\partial \phi_{B\space{swept}}}{\partial t}$$, or in other words, the **net EMF** equals the negative of the amount of **"magnetic field lines"** swept across by the "wire" per unit time.



##### Second Definition:

$\mathcal{E}=-\frac{\partial \phi_{B\space enclosed}}{\partial t}$, or the **net EMF** equals the negative of the amount of **magnetic flux** change per unit time in some **"enclosed surface"**.



##### Third Definition:

This is similar to the first. $\mathcal{E_{motional}}=-\frac{\partial \phi_{B\space{swept}}}{\partial t}$, or in other words, the **motional EMF** equals the negative of the amount of **"magnetic field"** swept across by the "wire" per unit time.



##### Fourth Definition:

This is actually called Maxwell-Faraday's Law, which is a separate thingy, but people still mix it with Faraday's Law. $\nabla \times E=-\frac{\partial B}{\partial t}$, or in more familiar integral form $\oint\limits_{\partial \sigma}E\cdot dl=-\iint\limits_{\sigma} \frac{\partial B}{\partial t}\cdot dA$. Notice that it's a statement **regarding $B$ field, and $E$ field themselves**, and has nothing to do with the shape of the wire or the velocity of the wire.



All these seem confusing. And to confuse you more, the four definitions are not equivalent. Some are applicable in more cases than others.



For example, the first definition is extremely hand-wavy (though it might be the most original to what Faraday came up with). It's flawed in many cases. The second definition holds in general, until the concept of "enclosed surface" loses its meaning. The third definition holds unless the concept of "wire" is undefined. The fourth is again, a separate law. It's one of the four Maxwell's Equations. Therefore, it's fundamental and works in all cases (where Maxwell's electromagnetism works). I will explain all these later.



#### Motional EMF vs Induced EMF

EMF is defined as follows:

$\mathcal{E}_s = \frac{1}{q}\int\limits_s F\cdot dl$

The electromotive "force" (a bad name) a long a path $s$ is defined as the work per unit charge along that path. In other words, if you move an imaginary charged particle of charge $q$ along the path $s$, compute the work done on the charge $q$ by the **electromagnetic force**, then you can divide it by $q$ to get the EMF along that path.



The electromotive force (EMF) we defined here is the **net EMF**.



Since there're two parts to $F$, specifically $F=F_E+F_B$, we can separate the electromagnetic force into electrostatic force and magnetic force.

$\mathcal{E}_s = \frac{1}{q}\int\limits_s F\cdot dl$
$=\frac{1}{q}\int\limits_s F_E\cdot dl + \frac{1}{q}\int\limits_s F_B\cdot dl$

Recall Lorentz force law, $F_B=qv\times B, \space F_E=qE$ (note $v,B,E$ are all vectors, so are $F_B, F_E$). We plug that in, notice the $q$ cancels (it should, because that's the point of the $\frac{1}{q}$ in the definition)

$\mathcal{E}_s = \int\limits_s E\cdot dl + \int\limits_s (v\times B)\cdot dl$

The first part, $\int\limits_s E\cdot dl$ is called the **induced EMF**, the second part $\int\limits_s (v\times B)\cdot dl$ is called the **motional EMF**.



Apparently, the $E\cdot dl$ can only be generated (assuming it's all due to magnetic interactions) if there's a changing $B$ field. This is because changing $B$ field creates a curl in $E$, without it, and without any charge present (as in a circuit), $E=0$. So **induced EMF** is named so because it's induced by a changing magnetic field.



On the other hand, the second half has nothing to do with a changing magnetic field. Instead, it requires motion of the **path or wire**, which is why it's named **motional EMF**.



The first part also gives you the electrostatic voltage across path $s$. As you can see, the form of the **induced EMF** is close to the form of Maxwell-Faraday's Law, so we can use Maxwell-Faraday's Law to compute the induced EMF for a **closed loop** (because Maxwell-Faraday's Law integral form only works in a closed loop).



The second part is trickier, we will derive directly from it what I called the Motional Faraday's Law, basically the [third definition of Faraday's Law](#third-definition)



### Derivation of Faraday's Law

We want to derive $\mathcal{E}=-\frac{\partial \phi_{B\space enclosed}}{\partial t}$ (our second definition). Let's first derive the motional EMF and combine with the induced EMF to obtain net EMF.

#### Motional part of Faraday's Law derivation

We wish to derive $\mathcal{E_{motional}}=-\frac{\partial \phi_{B\space{swept}}}{\partial t}$.

Let's start with the definition of motional EMF

$\int\limits_s (v\times B)\cdot dl$

At first sight, it seems this must evaluate to 0, because $v\parallel dl$, right?

$v\parallel dl$ when the wire/path is stationary! But the whole point of motional EMF is that now the wire and the path are not stationary.

For example, the wire can be moving rightward while the charged particle is traveling up in the wire.



$v$ denotes the total motion relative to the magnetic field (right and up). $dl$ just points up. The same can be said of the concept of **path**, while the path relative to magnetic field is right and up, we are only concerned about the EMF along the upward direction (we will explore why is that in later articles), so the $dl$ points up, again.



Therefore $v=v_{along}+v_{of}$, or the net velocity = velocity along the wire or the predefined direction of the path + velocity of the wire or the predefined path at that point.



$v_{along}\parallel dl$, but $v_{of}\not\parallel dl$!



we only need to consider $v_{of}$, so $\mathcal{E_{motional}}=\int\limits_s (v_{of}\times B)\cdot dl$



Notice that $(v_{of}\times B)\cdot dl$ is a [box product](https://mathinsight.org/scalar_triple_product).

It represents the volume of the parallelepiped formed by the three vectors $v_{of}, B, dl$; so a natural question to ask is what is the physical significance of this volume? I will leave that for the readers to juggle with.



To compute the same volume, we can also swap the order of the vectors a bit.

$(v_{of}\times B)\cdot dl=(dl\times v_{of})\cdot B$



Now, this quantity is much earsier to understand. $(dl\times v_{of})$ represents the rate at which area is swept by the segment $dl$ when it moves at velocity $v_{of}$! So $dl\times v_{of}=-d\frac{dA_{of \space dl}}{dt}$. There's a little $d$ in the front to denote that this rate of area-sweep is infinitesimally small because $dl$ is infinitesimally small. The negative sign is of little importance. It's due to the definition of the direction of area using righthand rule.

If you prefer, we can stay away from calculus notations, and use $\Delta l \times \frac{\Delta x}{\Delta t}=\frac{\Delta l \times \Delta x}{\Delta t}=-\frac{\Delta^2 A}{\Delta t}=-\Delta \frac{\Delta A}{\Delta t}$. Again, the double $\Delta$ is to indicate the smallness of the area.



Apparently, $-\frac{dA_{of \space dl}}{dt}\cdot B=-\frac{dA_{of\space dl}\cdot B}{dt}=-\frac{d\phi_B}{dt}$, or in other words, the rate at which we sweep area times the $B$ field equals the rate at which we sweep magnetic flux.



So plugging it back in to the integral,

$\mathcal{E_{motional}}=\int\limits_s -d \frac{d\phi_B}{dt} = -\frac{d\phi_{B\space swept \space by \space s}}{dt}$

Thus we have derived the [third definition of Faraday's Law](#third-definition), which I like to call Motional Faraday's Law.

One last note: The only fundamental theorem of electromagnetims we used above is the Lorentz Force Law. So, in other words, this Motional Faraday's Law should have equal predictive power to the Lorentz Force Law. All things predictable by Motional Faraday's Law should be predicted by Lorentz Force Law, and vice versa. In some cases, Lorentz force law is much easier (as in the "exceptions" of Motional Faraday's Law)



#### Derivation of Loop form of Faraday's Law

Now, we can easily derive the loop form of the Faraday's Law from this "sweeping" form. This is included in many textbooks. The basic idea is to note that when we sweep $s$, all the $\phi_B$ we sweep across either moves from $\phi_{inside\space loop}\rightarrow \phi_{outside \space loop}$ or $\phi_{outside\space loop}\rightarrow \phi_{inside \space loop}$

So if $s$ is part of a loop, the $\frac{d\phi_{B\space swept \space by \space s}}{dt}$ just goes into $\frac{d\phi_{B\space inside\space loop\space due\space to\space change\space in\space \sigma}}{dt}$; the deduction of the sign requires some care, and so I will not bore you with that. The importance of "due to change in $\sigma$" will be evident later.



Now we arrive at:

$\mathcal{E_{motional\space in\space \sigma}}= -\frac{d\phi_{B\space inside\space loop\space due\space to\space change\space in\space \sigma}}{dt}$

Which is close to the complete Loop version of Faraday's Law ([definition 2](#second-definition))



To obtain the complete loop version of Faraday's Law, we must analyze $\mathcal{E}_{induced}$, or the **induced EMF**.

Luckily, that's given simply by the [Maxwell-Faraday's Law](#fourth-definition).

Recall	$\mathcal{E_{induced}}=\oint\limits_{\partial \sigma}E\cdot dl$

$=-\iint\limits_{\sigma} \frac{\partial B}{\partial t}\cdot dA$

$=-\frac{\partial \phi_{B\space due \space to \space change\space in\space B}}{\partial t}$

Now we add $\mathcal{E_{motional}}, \space \mathcal{E_{induced}}$.

$\mathcal{E_{net}}=\mathcal{E_{motional}}+\mathcal{E_{induced}}$

$=-\frac{\partial\phi_{B\space inside\space loop\space due\space to\space change\space in\space \sigma}}{\partial t}-\frac{\partial \phi_{B\space due \space to \space change\space in\space B}}{\partial t}$

Notice two subtleties:

I changed the full derivative to partial derivative to make it more accurate, since other variables like location can influence $\phi_B$ as well. If you don't know what I'm talking about, don't let it bother you.

The two $\frac{\partial \phi_B}{\partial t}$ are mutually exclusive because they are due to different causes. In fact "change in $B$" and "change of $\sigma$" are the only possible causes of a changing flux. Change in "angle" is part of either changing $B$ or changing $\sigma$. So they add together to $\frac{\partial \phi_{B\space net}}{\partial t}$



Great, now **behold the full glamour of Faraday's Law as we have derived it**:

$\mathcal{E_{net}}=-\frac{\partial \phi_{B\space net}}{\partial t}$



### Conclusion

To recap what just happened. We first explained the difference of motional EMF and induced EMF. Motional EMF is EMF created due to movement of wire/path in the magnetic field. Induced EMF is EMF created due to change of magnetic field.

Another way to think of it is, Motional EMF is due to $v\times B$ part of the force, while Induced EMF is due to $E$ part of the eletromagnetic force.

There are several definitions of Faraday's Law. The [fourth definition](#fourth-definition) we gave is actually called Maxwell-Faraday's Law. It should not be confused with Faraday's Law, for it's more fundamental and only deals with induced EMF.

Some versions of Faraday's Law deal with motional EMF as in the [third definition](#third-definition). Faraday's Law dealing with Motional EMF can come in 2 flavors: "sweeping wire flavor" and "closed loop flavor." They are effectually equivalent. Other versions combine the third version with Maxwell-Faraday's Law to create a statement that handles both motional EMF and induced EMF. This version is in "closed loop flavor," because Maxwell-Faraday's Law is hard to manipulate when there isn't a closed loop.

The [first definition](#first-definition) involving magnetic field line is problematic (explored in part 2), but is probably closer to what Faraday originally proposed.

Last but not least, I offered a simple proof of Faraday's Law using Lorentz Force Law and Maxwell-Faraday's Law. Because of this proof, we can conclude that **Faraday's Law has the same predictive power as Lorentz Force Law + Maxwell-Faraday's Law**.



See part 2 for examples of spectacular failures of Faraday's Law (mostly provided by Feynman) and why they make sense (according to me, at least)!





