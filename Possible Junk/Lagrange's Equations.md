---
tags: 
dg-publish: true
mathLink: 
---
Subject: _None_
Main\_Topic: _None_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

Armed with the ideas of the [[Calculus of Variations]], we are ready to set up the version of mechanics published in 1788 by the Italian-French astronomer and mathematician Lagrange. The Lagrangian formulation has two important advantages over the earlier Newtonian formulation. First, Lagrange's equations, unlike Newton's, take the same form in any coordinate system. Second, in treating constrained systems, such as a bead sliding on a wire, the Lagrangian approach eliminates the forces of constraint (such as the normal force of the wire, which constrains the bead to remain on the wire), This greatly simplifies most problems, since the constraint forces are usually unknown, and this simplification comes at almost no cost, since we usually do not want to know these forces anyway. 

We shall see that Lagrange's equations are equivalent to Newton's second law for a particle moving unconstrained in three dimensions. The extension of this result to $N$ unconstrained particles is straightforward. 

**Remark.**  Throughout this article, except in one specific part, we treat only the case that all non-constraint forces are conservative or can, at least, be derived from a potential energy function. This restriction can be significantly relaxes, but already includes most of the applications likely to be met in practice. 

##### Lagrange's Equations for Unconstrained Motion
Consider a particle moving unconstrained in three dimensions, subject to a conservative net force $\pmb{F}(\pmb{r})$. The particle's kinetic energy is, of course, 
$$
T = \frac{1}{2}mv^{2}=\frac{1}{2}m\dot{\pmb{r}}^{2} = \frac{1}{2}(\dot{\pmb{x}}^{2}+\dot{\pmb{y}}^{2}+\dot{\pmb{z}}^{2})
$$
and its potential energy is 
$$
U = U(\pmb{r}) = U(x,y,z)
$$
The **Lagrangian function** or just the **Lagrangian**, is defined as 
$$
\mathcal{L} = T-U
$$
Notice first that the Lagrangian is the Kinetic Energy _minus_ the Potential Energy. It is _not_ the same as the total energy. You are certainty entitle to ask why the quantity $T-U$ should be of any interest. There seems to be no simple answer to this question except that it is, as we shall see directly. Notice also that we are using a script $\mathcal{L}$ for the Lagrangian (to distinguish it from the angular momentum $\pmb{L}$ and a length $L$) and that $\mathcal{L}$ depends on the particle's position $(x,y,z)$ and its velocity $(\dot{x},\dot{y},\dot{z})$; that is, $\mathcal{L} = \mathcal{L}(x,y,z,\dot{x},\dot{y},\dot{z})$. Let us consider the two derivatives 
$$
\frac{\partial \mathcal{L}}{\partial x} = - \frac{\partial U}{\partial x} = F_{x}
$$
and 
$$
\frac{\partial \mathcal{L}}{\partial \dot{x}} = \frac{\partial T}{\partial \dot{x}} = m \dot{x} = p_{x}
$$
Differentiating the second equation with respect to time and remembering Newton's second law, $F_{x}=\dot{p}_{x}$ (we are taking for granted that our coordinate frame is inertial), we see that 
$$
\frac{\partial \mathcal{L}}{\partial x} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{x}}
$$
In exactly the same way we can prove corresponding equations in $y$ and $z$. Thus we have shown that Newton's second law implies the three _Lagrange equations_ (in Cartesian coordinates so far):
$$
\frac{\partial \mathcal{L}}{\partial x} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{x}}, \quad \frac{\partial \mathcal{L}}{\partial y} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{y}}, \quad \frac{\partial \mathcal{L}}{\partial z} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{z}}
$$
We can easily check that the argument just given works equally well in reverse, so that (for a single particle in Cartesian coordinates, at least) Newton's second law is exactly equivalent to the three Lagrange equations. The particle's path as determined by Newton's second law is the same as the path determined by the three Lagrange equations. 

Our next step is to recognize that the three equations have exactly the form of the **Euler-Lagrange equations** in [[Calculus of Variations]]. Therefore, they imply that the integral $S = \int\limits \mathcal{L} dt$ is stationary for the path followed by the particle. That this integral, called the action integral, is stationary for the particle's path is called Hamilton's principle and can be restated as follows: 

```ad-Definition
**Hamilton's Principle**: The actual path which a particle follows between two points $1$ and $2$ in a given time interval, $t_{1}$ to $t_{2}$, is such that the action integral
$$
S = \int\limits_{t_{1}}^{t_{2}} \mathcal{L} \ dt
$$
is stationary when taken along the actual path. 
```

Although we have so far proved this principle only for a single particle and in Cartesian coordinates, we are going to find that it is valid for a huge class of mechanical systems and for almost any choice of coordinates. 

So far we have proved for a single particle that the following three statements are exactly equivalent: 
1. A particle's path is determined by Newton's Second Law $\pmb{F}=m\pmb{a}$
2. The path is determined by the three Lagrange equations, at least in Cartesian coordinates
3. The path is determined by Hamilton's principle

Hamilton's principle has found generalizations in many fields outside classical mechanics and has given a unity to various diverse areas of physics. In the twentieth century it has played an important role in the formulation of quantum theories. However, for our present purposes its great important is that it lets us prove that Lagrange's equations hold in more-or-less any coordinate system:

Instead of the Cartesian coordinates $\pmb{r} = (x,y,z)$, suppose that we wish to use some other coordinates. These could be spherical polar coordinates $(r, \theta, \phi)$ or cylindrical polars $(\rho,\phi,z)$, or any set of "generalized coordinates" $q_{1},q_{2},q_{3}$, with the property that each position $\pmb{r}$ satisfied a unique value of $(q_{1},q_{2},q_{3})$ and vise versa; that is, 
$$
q_{i} = q_{i}(\pmb{r}) \quad \text{for} \ i=1,2,3
$$
and 
$$
\pmb{r} = \pmb{r}(q_{1},q_{2},q_{3})
$$
these two equations guarantee that for any value of $\pmb{r}=(x,y,z)$ there is a unique $(q_{1},q_{2},q_{3})$ and vice versa. Now we can rewrite $(x,y,z)$ and $(\dot{x},\dot{y},\dot{z})$ in terms of $(q_{1},q_{2},q_{3})$ and $(\dot{q_{1}},\dot{q_{2}},\dot{q_{3}})$. Next, we can rewrite the Lagrangian $\mathcal{L} = \frac{1}{2}m \dot{\pmb{r}}^{2} - U(\pmb{r})$ in terms of these new variables as 
$$
\mathcal{L} = \mathcal{L}  (q_{1},q_{2},q_{3},\dot{q_{1}},\dot{q_{2}},\dot{q_{3}})
$$
and the action integral as 
$$
S = \int\limits_{t_{1}}^{t_{2}} \mathcal{L} (q_{1},q_{2},q_{3},\dot{q_{1}},\dot{q_{2}},\dot{q_{3}}) \ dt
$$
Now, the value of the integral $S$ is unaltered by this change in variables. Therefore, the statement that $S$ is stationary for variations of the path around the correct path must still be true in our new coordinate system, and, by the results of [[Calculus of Variations]], this means that the correct path must satisfy the three Euler-Lagrange equations,
$$
\frac{\partial \mathcal{L}}{\partial q_{1}} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{q_{1}}}, \quad \frac{\partial \mathcal{L}}{\partial q_{2}} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{q_{2}}}, \quad \frac{\partial \mathcal{L}}{\partial q_{3}} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{q_{3}}}
$$
with respect to the new coordinates $q_{1},q_{2},$ and $q_{3}$. Since these new coordinates are _any_ set of generalized coordinates, the qualification "in Cartesian coordinates" can be omitted from the statement (2) prior. This result$-$that Lagrange's equations have the same form for any choice of generalized coordinates$-$is one of the two main reasons that the Lagrangian formalism is so useful. 

There is one point about our derivation of Lagrange's equations that is worth keeping at the back of your mind. A crucial step in our proof was the observation that $\frac{\partial \mathcal{L}}{\partial q_{1}} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{q_{1}}}$ was equivalent to Newton's second law $F_{x}=\dot{p}_{x}$, which in turn is true only if the original frame in which we wrote down $\mathcal{L}=T-U$ is inertial. Thus, although Lagrange's equations are true for any choice of generalized coordinates $q_{1},q_{2},q_{3}$ $-$and these generalized coordinates may in fact be the coordinates of a noninertial reference frame$-$we must nevertheless be careful that, when we first write down the Lagrangian $\mathcal{L}=T-U$, we do so in an inertial frame. 

We can easily generalize Lagrange's equations to systems of many particles. However, before we move on let us make a simple remark. Notice how when writing Lagrange's equations and equating them to Newton's second law, the derivative of $(\partial \mathcal{L})/(\partial x)$ is the $x$ component of the force, and $\frac{\partial \mathcal{L}}{\partial \dot{x}}$ is the $x$ component of the momentum (and similarly with all other components $y,z$, etc.). When we use generalized coordinates $q_{1},q_{2},\ldots,q_{n}$, we shall find that $\frac{\partial \mathcal{L}}{\partial q_{i}}$, although not necessarily a momentum component, acts very like a momentum. For this reason we shall call these derivatives the **generalized force** and **generalized momentum** respectively; that is,
$$
\frac{\partial \mathcal{L}}{\partial q_{i}} = \text{i-th component of generalized force}
$$
and 
$$
\frac{\partial \mathcal{L}}{\partial \dot{q}_{i}} = \text{i-th component of generalized momentum}
$$
With these notations, each of the Lagrange equations 
$$
\frac{\partial \mathcal{L}}{\partial q_{i}} = \frac{d}{dt} \frac{\partial \mathcal{L}}{\partial \dot{q_{i}}}
$$
takes the form 
$$
\text{generalized force} = \text{rate of change of generalized momentum}
$$


