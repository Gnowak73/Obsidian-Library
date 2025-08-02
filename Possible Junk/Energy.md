---
tags:
  - energy
  - conservation_of_energy
  - CM
  - Physics
  - kinetic_energy
  - conservative
  - work
  - potential
  - potential_function
dg-publish: true
mathLink:
---
Subject: _CM_
Main\_Topic: _Energy_
Applications: _Classical Mechanics_
Examples: _None_
Class: _CM 1_
Exam: _Exam 2_
Textbook: _[[taylor-2005-classical-mechanics.pdf]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

You will see that the analysis of energy conservation is surprisingly more complicated than the corresponding discussion of linear and angular momenta in [[Momentum and Angular Momentum]]. The main reason for this is that there are different forms of energy along with various processes that transform energy from one kind into another. We shall see that conservation of energy is quite a subtle business, even for a system consisting of just a single particle. 

#### Kinetic Energy and Work
Perhaps the most basic energy is **kinetic energy**, which for a single particle of mass $m$ traveling with speed $v$ is defined to be 
$$
T = \frac{1}{2}mv^{2}
$$
The time derivative of $T$ is easily found by recognizing that $v^{2}=\pmb{v}\cdot \pmb{v}$:
$$
\frac{dT}{dt} = \frac{1}{2}m \frac{d}{dt}(\pmb{v} \cdot \pmb{v}) = \frac{1}{2}m(\dot{\pmb{v}}\cdot \pmb{v} + \pmb{v} \cdot \dot{\pmb{v}}) = m\dot{\pmb{v}} \cdot \pmb{v}
$$
By Newton's Second Law ([[Newton's Laws of Motion]]), the factor $m\dot{\pmb{v}}=\pmb{F}$ such that 
$$
\frac{dT}{dt} = \pmb{F} \cdot \pmb{v}
$$
If we multiply both sides by $dt$ (assuming we are working with differential 1-forms), 
$$
dT = \pmb{F} \cdot d\pmb{r}
$$
since $\pmb{v}= \frac{d\pmb{r}}{dt}$. The expression on the right, $\pmb{F}\cdot d\pmb{r}$, is defined to be the **work** done by the force $\pmb{F}$ in the displacement $d\bf{r}$. Thus we have proved the **Work-Energy Theorem**, that the change in the particle's kinetic energy between two neighboring points on its path is equal to the work done by the net force as it moves between the two points. 

So far we have proved that Work-Energy theorem only for an infinitesimal displacement $d\bf{r}$, but it generalizes easily to larger displacements. We can either take the sum $\sum\limits \pmb{f} \cdot d\pmb{r}$ and turn it into an integral or just simple integrate both sides of our differential 1-form relationship to get 
$$
\Delta T = \int\limits \pmb{F} \cdot d \pmb{r}
$$
Note that this is a [[Line Integrals|line integral]], and all the techniques to solve them can be used. It is important to remember that the work that appears on the right side is the work done by the _net force_ $\pmb{F}$ on a particle. In general, $\pmb{F}$ is the vector sum of various separate forces
$$
\pmb{F} = \pmb{F}_{1} + \ldots + \pmb{F}_{n} \equiv \sum\limits_{i=1}^{n}\pmb{F}_{i}
$$
(For example, the net force on a projectile is the sum of two forces, gravity and air resistance.) We can actually rewrite our formulation for the sum of forces as 
$$
\Delta T = \int\limits \sum\limits_{i=1}^{n}F_{i} \cdot d\pmb{r} = \sum\limits_{i=1}^{n} \int\limits F_{i}\cdot d\pmb{r}
$$
as long as [[Fubini's theorem]] is satisfied properly. In practice, one almost always uses the theorem this way: calculate the work done by each of the $n$ separate forces on the particle and then set $\Delta T$ equal to the sum of the work. If the net force on a particle is zero, then the Work-Energy theorem tells us that the particle's kinetic energy is constant. This simply says that the speed is constant, which, though true, is not very interesting, since it already follows from Newton's First Law. 

#### Potential Energy and Conservative Forces
The next step in the development of the energy formalism is to introduce the notation of potential energy corresponding to the forces on an object.  Not every force lends itself to the definition of a corresponding potential energy. Actually, potential energy is derived from the [[Fundamental Theorem of Line Integrals]] for a potential function. Thus, forces with a potential energy are _conservative_. We see that it is a necessity that these conservative forces only depend on the **position** of the object on which it acts; it must not depend on the velocity, the time, or any other variables. We call this the first condition, and it forces that mechanical energy is conserved.

We see that this brings about two conditions that can be said about a force if it is conservative: 
1. The work done in a closed loop is $0$
2. The work is done between two points is the same for all paths between those two points

The importance of conservative forces is that if all forces on an object are conservative, we can define a quantity called the potential energy, denoted by $U(\pmb{r})$, a function only of position, with the property that the total mechanical energy 
$$
E = T + U(\pmb{r})
$$
is constant; that is, $E$ is conserved. To define the potential energy corresponding to a given to a conservative force, we first choose a reference point $\pmb{r}_{0}$ at which $U$ is defined to be zero. We then define $U(\pmb{r})$, the **potential energy** at an arbitrary point $\pmb{r}$, to be 
$$
U(\pmb{r}) = -W \equiv - \int\limits_{\pmb{r}_{0}}^{\pmb{r}} \pmb{F} \cdot d \pmb{r}
$$
In words, the potential energy is the negative of the work done by a force if the particle moves from the reference point $\pmb{r}_{0}$ to some point of interest $\pmb{r}$. We will now show where this definition is derived from. If we have a force $\pmb{F}$ which is conservative, and we let $\pmb{r}_{1}$ and $\pmb{r}_{2}$ be any two points, and if $\pmb{r}_{0}$ is the reference point at which $U$ is zero, then it is clear that 
$$
W(\pmb{r}_{0} \rightarrow \pmb{r}_{2}) = W(\pmb{r}_{0} \rightarrow \pmb{r}_{1}) + W(\pmb{r}_{1}\rightarrow \pmb{r}_{2})
$$
since it doesn't matter the path we take. And hence 
$$
W(\pmb{r}_{1}\rightarrow \pmb{r}_{2}) = W(\pmb{r}_{0} \rightarrow \pmb{r}_{2}) - W(\pmb{r}_{0} \rightarrow \pmb{r}_{1}) 
$$
Each of the two terms on the right is (minus) the potential energy at the corresponding point. Thus we have proved that the work on the left is just the different of these two potential energies:
$$
W(\pmb{r}_{1} \rightarrow \pmb{r}_{2}) = -\Delta U
$$
The usefulness of this result emerges when we combine it with the Work-Energy theorem:
$$
\Delta T= W(\pmb{r}_{1} \rightarrow \pmb{r}_{2})
$$
We then see that 
$$
\Delta T = -\Delta U
$$
or 
$$
\Delta (T+U) =0
$$
That is, the **mechanical energy** 
$$
E=T+U
$$
does **not** change as the particle moves. Since the points $\pmb{r}_{1}$ and $\pmb{r}_{2}$ are _any_ two points, we have the important conclusion: if the force on a particle is conservative, then the particle's mechanical energy is conserved. If however, it is not conserved, then we can see that the Work due to non-conservative forces is simply equal to $\Delta E$. In other words, we can write $W_{total} = W_{nc} + W_{c}$, which is the same thing as saying $\Delta T = \Delta E - \Delta U$. 

###### Several Forces and Nonconservative Forces 
So far we have established the conservation of energy for a particle subject to a single conservative force. If the particle is subject to several forces, and all of them are conservative, our result generalizes easily. All of the forces and energies simply add together. For nonconservative forces, as explained before, we simply consider $\Delta E$ since the mechanical energy is no longer conserved. In many problems the only nonconservative force is the force of sliding friction, which usually does negative work, or in other words, it "steals" the mechanical energy. 

##### Force as Gradient of Potential Energy
We have seen that the potential energy $U(\pmb{r})$ corresponds to a conservative force $\pmb{F}(\pmb{r})$ from the [[Fundamental Theorem of Line Integrals]]. This suggests that we should be able to write the potential energy in some form of the force. Well, we can easily see from taking the gradient on both sides that 
$$
 F(\pmb{r}) = -\nabla \pmb{U}
$$
This important relation gives us the force $\pmb{F}$ in terms of derivatives of $U$, just as the definition gave $U$ as an integral of $\pmb{F}$. When a force $\pmb{F}$ can be expressed in the form above, we say that $\pmb{F}$ is **derivable from a potential energy**. Thus, we have shown that any conservative force is derivable from a potential energy. A useful application of the gradient can be seen in 
$$
df = \nabla f \cdot d\pmb{r}
$$

##### The Second Condition that F be Conservative
We have seen that one of the two conditions that a force $\pmb{F}$ is conservative is that the work between any two points is independent of the path followed. However, there is a better way to figure out if a force is conservative than looking at the line integrals. Using [[Stokes' Theorem]] or [[Green's Theorem (circulation)]], we can see that the line integral can be written as (for 2D specifically)
$$
\int\limits_{C} \pmb{F} \cdot d\pmb{r}=\int\limits_{C} \nabla \times \pmb{F} \cdot d\pmb{r}
$$
So if the curl, or $\nabla \times \pmb{F}$, is $0$, then the work is zero for any closed path, which means that the path doesn't matter, which means that the force is conservative. We could also use the [[Fundamental Theorem of Line Integrals]], where we take the condition 
$$
F = \nabla f
$$
and then take the cross of the gradient on both sides to get
$$
\nabla \times F = \nabla \times \nabla f = 0
$$
since the curl of the gradient is always $0$. 

##### Time dependent Potential Energy
We sometimes have occasion to study a force $\pmb{F}(\pmb{r},t)$ that satisfies the second condition to be conservative $\nabla \times F = 0$, but, because it is time-dependent, it does not satisfy the first condition. In this case, we can still define a potential energy $U(\pmb{r},t)$ with the property that $\pmb{F} = -\nabla U$, but it is no longer the case that the total mechanical energy is conserved. If we carefully review the argument at the beginning of [[#Potential Energy and Conservative Forces]] leading up the conservation of mechanical energy, you may be able to see that time is not taken into account when we sum the work done. In any case we can directly show that $E=T+U$ changes as the particle moves on its path. As before, we transform the potential energy by differential 1-forms to get 
$$
dT = \frac{dT}{dt}dt = \pmb{F} \cdot d\pmb{r}
$$
Meanwhile, $U(\pmb{r},t)=U(x,y,x,t)$ is a function of four variables and 
$$
dU = \frac{\partial U}{\partial x} dx + \frac{\partial U}{\partial y}dy + \frac{\partial U}{\partial z}dz + \frac{\partial U}{\partial t}dt
$$
You will recognize the first three terms on the right as $\nabla U \cdot d \pmb{r} = -\pmb{F} \cdot d\pmb{r}$. Thus 
$$
dU = -\pmb{F} \cdot d\pmb{r} + \frac{\partial U}{\partial t}dt
$$
When we add this to the equation with $dT$ the first two terms cancel and we are left with 
$$
d(T+U) = \frac{\partial U}{\partial t}dt
$$
Clearly it is only when $U$ is independent of $t$ that the mechanical energy is conserved. However, we can understand this conclusion by noting that while mechanical energy is not conserved, the **total energy is conserved**: the loss/gain of mechanical energy is exactly balanced by the gain/loss of energy elsewhere. 

#### Complete Solution of Motion
A remarkable feature of one-dimensional conservative systems is that we can in principle use the conservation of energy to obtain a complete solution of motion, that is, to find the position $x$ as a function of time. Since $E=T+U(x)$ is conserved, we can solve for $T = \frac{1}{2}m \dot{x}^{2} = E-U(x)$ to get 
$$
\dot{x}(x) = \pm \sqrt{\frac{2}{m}} \sqrt{E-U(x)}
$$
Notice that there is an ambiguity in the branch of the square root since energy considerations cannot determine the _direction_ of the velocity. For this reason, the method described here usually does not work in a truly three-dimensional problem. In one dimension, however, you can almost always decide the sign of $\dot{x}$ by inspection, though you must remember to do so. Knowing the velocity as a function of $x$, we can find $x$ as a function of $t$ by using the chain rule and finding that 
$$
dt = \frac{dx}{\dot{x}}
$$
as long as $\dot{x}\neq 0$. Next, we can integrate between any initial and final points to give 
$$
t_{f}-t_{i} = \int\limits_{x_{i}}^{x_{f}} \frac{dx}{\dot{x}} 
$$
this gives the time for travel between any initial and final positions of interest. If we substitute for $\dot{x}$ and assume, to be definite, that $\dot{x}$ is positive then the time to go from the initial $x_{0}$ at time $0$ to an arbitrary $x$ at time $t$ is 
$$
t = \int\limits_{x_{0}}^{x} \frac{dx'}{\dot{x}(x')} = \sqrt{\frac{m}{2}}\int\limits_{x_{0}}^{x} \frac{dx'}{\sqrt{E-U(x)}}
$$
As usual, we've renamed the variable of integration to avoid confusion with the upper limit. Note that this integral depends on the particular form of $U(x)$ in the problem at hand. Assuming we can do the integral, it gives us $t$ as a function of $x$. If we're lucky, we can then solve to give $x$ as a function of $t$. 

```ad-warning
We can always map $x$ as a function of $t$, but we cannot always map $t$ as a function of $x$. 
```

```ad-note
The procedures in this entire article can be used for curvilinear coordinates, we just have to be much more careful about the forces and the work being done. 
```

#### Central Forces
A three-dimensional situation that has some of the simplicity of one-dimensional problems is a particle that is subject to a central force, that is, a force that is everywhere directed toward or away from a fixed "force center". If we take the force center to be the origin, a central force has the form 
$$
\pmb{F}(\pmb{r}) = f(\pmb{r}) \hat{\pmb{r}}
$$
where the function $f(\pmb{r})$ gives the magnitude of the force (and is positive if the force is outward and negative if it is inward). We notice that central forces are _spherically symmetric_, or _rotationally invariant_. Note that a central force that is spherically symmetric is automatically conservative. We can see this from spherical coordinates and the curl. To find the curl in any coordinate system we simply use the definition of the gradient from [[Riemannian Metrics]] and find the metric. Taking the curl we can then see it is always zero. 

```ad-note
For central forces, only the **radial component** of the force can be nonzero.
```

We we wanted to find the force from the gradient we would simple have 
$$
\pmb{F}(\pmb{r}) = -\nabla U = -\hat{\pmb{r}} \frac{\partial U}{\partial r} - \hat{\pmb{\theta}} \frac{1}{r} \frac{\partial U}{\partial \theta} - \hat{\pmb{\phi}} \frac{1}{r \sin \theta} \frac{\partial U}{\partial \phi} = -\hat{\pmb{r}} \frac{\partial U}{\partial r}
$$
As states before, only the radial component can be nonzero, so we get 
$$
\pmb{F}(\pmb{r}) = -\hat{\pmb{r}} \frac{\partial U}{\partial r}
$$
since $U$ is spherically symmetric.
