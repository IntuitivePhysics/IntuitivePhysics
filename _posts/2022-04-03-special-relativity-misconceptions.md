---
layout: post

title: How NOT to Understand Spacetime in Special Relativity 

author: Michael Huang

description: There're a lot of bad ways to understand spacetime in special relativity. They exist because we don't need to understand spacetime properly to solve most simple problems in SR.

tags:
    - special relativity
    - length contraction
    - time dilation
    - simultaneity
    - misconception
    - mechanics

excerpt: Time Dilation means we measure time-wise separation of events occuring on moving objects to be longer. WRONG!...


---

Special Relativity's spacetime concerns with several major effects: 1. time dilation, 2. length contraction, 3. simultaneity. This post aims to address several misconceptions about them without much of the mathematics of Lorentz Transformation or the aid of spacetime diagram (which is basically a cheat code). 

### Content

1. [Basics](#basics)
2. [Time Dilation](#time-dilation)
3. [Distance Dilation / Length Contraction](#length-contraction)
4. How to conceptualize [spacetime](#how-to-conceptualize-spacetime)

### Basics

In special relativity, instead of speaking of objects, we should prefer to speak of events. An event is defined by $(x,t)$, a $x$ coordinate value and a $t$ coordinate value. Given two events, $(x_1,t_1)$, $(x_2,t_2)$, we denote their spatial separation as $x_2-x_1$ and time-wise separation as $t_2-t_1$. Events are absolute (they either happened or didn't happen; causation between events is preserved. That is $A\rightarrow B$, denoting $A$ causes $B$ is absolute across all reference frames). Finally, to simplify the math, we take $c=1$. 

With that out of the way, let's jump into some misconceptions.

### Time Dilation

**Time Dilation means we measure time-wise separation of events occuring on moving objects to be longer by $\gamma$**

**WRONG!**

First events cannot be "moving". 

Second, time dilation, and the factor $\gamma$ deals specifically with the time-separation of two very specific events $A,B$: the time separation between $A,B$ is measured to be $\gamma \Delta t_0$ where $\Delta t_0$ is the time-separation of $A,B$ in a reference frame such that $A,B$ occur at the same location! $\Delta t_0$ is called the proper time interval.

What that means is: if you have a moving ladder crossing over a stationary point $P$. You are standing at that point and you denote the event of the front of the ladder crossing $P$ to be $A$ and the back crossing to be $B$. It is wrong to think that your measured time-separation between $A,B$ would be longer than that measured by the person holding the ladder (let's call him Farmer John). The reason is, in Farmer John's reference frame, $A,B$ occur at different spatial locations and thus the time-interval he measures is not the $\Delta t_0$. In this specific case, in fact, you measure the $\Delta t_0$, so your measured time interval is shorter than Farmer John's, although he is moving with the ladder.

**So how to understand time dilation properly?**

**Approach 1: time travels slower for a moving observer**

An observer always measure their own proper time (if they are looking at a clock traveling with them). What does that mean? It means in terms of events? If we take them measuring the first time as event $A$, measuring the second time as event $B$, then since both measurements occur at the same location for the observer, their time-separation is the proper time separation. For any other outside observer who has non-zero relative motion, they measure a larger time-separation between event $A, B$ because they don't measure the proper-time separation. Therefore, a traveling observer measures smaller time interval and thus slower time passage rate. To take that further: **an observer moving faster through space is moving slower through time, according to us**. 

Question: what the heck do we mean an observer "moving through time"? Are we taking the derivative of time with respect to time...? (answer at the end)

**Approach 2: forget about traveling through time, focus on the events and their spatial/time separation**

Just consider two events $A,B$. Given two observers $S, S'$. If $S'$ measures $A,B$ to have a larger spatial separation, they are sure to measure $A,B$ to have a smaller time separation (as compared to $S$). This is in fact the same principle as observer moving faster through space is moving slower through time (which is just a time derivative of the former).  

### Length Contraction

**Length contraction states that the spatial separation between two events $A,B$ is observed to be shorter for stationary observer compared to moving observer by $\gamma$**

**WRONG!!**

$$\text{Length} \not = \text{Spatial Separation}$$

In fact, if you compare the $\Delta x$ measured by stationary observer to that measured by an observer moving in a certain direction, you may find the $\Delta x$ measured by the moving observer to be shorter than that measured by the stationary observer (sometimes even $0$ when the moving observer moves from $A$ towards $B$).

**So what is length?**

Length is a concept about an object, not two events. Consider two points $P_1,P_2$ and we want to measure their length. If each point moves with a certain velocity $v_1, v_2$, then each $P_1, P_2$ traces out a sequence of events through space-time. To measure $\text{dist}(P_1, P_2)$ with respect to an observer $S$, we find two **simultaneous** events that $P_1, P_2$ traces out and measure their spatial separation. That is length. So if you are measuring the spatial separation of two non-simultaneous events, you are certainly **not** measuring length of anything.

Because changing the frame of reference changes the definition of what is simultaneous, it also changes the definition of which two events' spatial separation gives the length of an object. 

So, $\Delta x$ actually dilates and doesn't contract. We may call that **distance dilation** (I didn't introduce this terminology. I believe it's minutephysics that did). We only observe length **contraction** because our definition of which two events' $\Delta x$ to measure causes it to contract rather than dilate.

### How to Conceptualize Spacetime

**Approach 1: Keep everything separate**

This is the common, easy, but confusing approach. **Time dilation**, **length contraction**, and **simultaneity difference** are three separate but interrelated concepts. Time dilation deals with the correlation between $v, t$. Length contraction deals with the correlation between $v,x$. Simultaneity deals with the correlation between $x,t$.

They are clearly encoded in Lorentz Transformations:

$$
\frac{x'}{\gamma}=x+vt \\
\frac{t'}{\gamma}=t+vx
$$

Consider $x,t$ as measured from $S$, which is moving with respect to $S'$ at velocity $v$. Let's call $S'$ our stationary frame. Then, $\frac{t'}{\gamma}$ means that the stationary frame's measured time separation is $\gamma$ larger than that measured in the moving frame $S$. Similarly, $\frac{x'}{\gamma}$ indicates that distance separation is $\gamma$ larger in the stationary frame $S'$. The simultaneity difference is accounted for by $vx$. 

**Approach 2: How I sometimes like to think about it**

Everything we've talked about so far is, IMHO, not the best way to understand space-time. 

**How dare you make this absurd accusation?**

At this point, we've somewhat viewed time as a unique/separate dimension from space. We talk about "time passes". Instead what we should say instead is we are moving through time, not time is passing through us. I mean it doesn't make much sense to talk about "space passes". 

We developed our idea of a reference frame under this unfair treatment of the time dimension. When we say a reference frame $S$ is moving with $A$. We mean that $A$ always measures its $x=0$ in $S$. However, $t$ still "passes" at the proper-time rate and increases all the time. If we truly attach $S$ to $A$ and $A$ is moving through spacetime, shouldn't $A$ measure its $x=0$ and $t=0$? 

**So what do we do?**

Abandon the concept of motion. Don't think about $A$ undergoing a motion as in there is a change of $x$ as $t$ changes. Think of $A$ as    moving through the grid of spacetime, tracing out a worldline. If we let $S$ be our reference frame, $t_S$ be time in our reference frame and use that as the standard for measuring the time passage of other observers. Then, we can speak of the rate at which $A$ moves through time $\frac{d\tau_A}{dt_S}$ ($\tau_A$ is $A$'s proper time) and the rate at which it moves through space $\frac{dx_A}{dt_S}$ ($x_A$ is $A$'s position with respect to $S$). Then, the statement of time-dilation and distance-dilation is captured in the statement:

$$
\left(\frac{d\tau_A}{dt_S}\right)^2 + \left(\frac{dx_A}{dt_S}\right)^2 \\= \left(\frac{dt_S}{dt_S}\right)^2 = 1
$$

 If one interprets $S$ as the standard reference frame. The statement means:

$$
\text{rate at which A travels through time}^2 + \text{rate at which A travels through space}^2 = 1
$$

The first is measured by how fast $A$'s clock ticks compare to $S$'s; the second is measured by $A$'s $v$ w.r.t. $S$. 

Clearly, when $v$ is high, $\frac{d\tau_A}{dt_S}$ is low, meaning it travels through time slower (slower clock tick rate). 

We don't even need to consider the distance-dilation. Because $x,t$ are two completely symmetric axis like $x,y$, distance-dilation is just the symmetric effect of time-dilation. 

The complete symmetry in Lorentz Transformation also makes sense now:

$$
\frac{x'}{\gamma}=x+vt \\
\frac{t'}{\gamma}=t+vx
$$

The $vx$ simultaneity difference term is not as dark magic, because it's just the symmetric effect of $vt$ (there's a bit complication here that is hidden because I set $c=1$). 

**Final note about spacetime coordinate**

Throughout this post, I've indulged a lot of imprecise languages about the spacetime coordinates we are using (and lots of other materials do too). I've been using languages such as "let's put the coordinate frame on $A$" or let "$S$ follow $A$". That is wrong. The coordinate doesn't really "follow" $A$ in most cases. If they do undergo the same motion as $A$ in spacetime (again we have to abandon our dogma about time being a separate thing), then $A$'s $x=0,t=0$ at all time, which is not the case for most of our use cases. So what are these coordinates? They are merely the standard coordinates boosted by velocity $v$. In Galilean transform, the boost is characterized by a horizontal (along $x$-axis) shift of the spacetime coordinate such that the $t$-axis aligns with the velocity of $A$. In Lorentz transform, the boost is a stretch along the two diagonals of spacetime (the velocity of light) such that the $t$-axis aligns with $v$. 

Welp. That's why spacetime diagram is just a simpler way to look at special relativity's spacetime.   

