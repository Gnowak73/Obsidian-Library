---
tags: 
dg-publish: true
mathLink: 
---
Subject: _CM_
Main\_Topic: _Electrodynamics_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

We begin our discussion of electrodynamics with the subject or _electrostatics_, phenomena involving time-independent distributions of charge and fields. One point of physics should be mentioned. Historically, electrostatics developed as a science of macroscopic phenomena. Such idealizations as point charges or electric fields at a point must be viewed as mathematical constructs that permit a description of the phenomena at the macroscopic level, but that may fail to have meaning microscopically. 

##### Coulomb's Law
All of electrostatics stems from the quantitative statement of Coulomb's law concerning the force acting between charged bodies at rest with respect to each other. Coulomb, in an impressive series of experiments, showed experimentally that the force between two small charged bodies separated in air a distance large compared to their dimensions:

1. varies directly as the magnitude of each charge,
2. varies inversely as the square of the distance between them,
3. is directed along the line joining the charges, and 
4. is attractive if the bodies are oppositely charged and repulsive if the bodies have the same type of charge.

Furthermore it was shown experimentally that the total force produced on one small charged body by a number of the other small charged bodies placed around it is the _vector_ sum of the individual two-body forced of Coulomb. Strictly speaking, Coulomb's conclusions apply to charged in vacuum or media of negligible susceptibility.

##### Electric Field 
Although the thing that eventually gets measured is a force, it is useful to introduce a concept one step removed from the forces, the concept of an electric field due to some array of charged bodies. At the momentum, the electric field can be defined as the force per unit charge acting at a given point. It is a vector function of position, denoted $\mathbf{E}$. 

Be careful in this definition though. It is not necessarily the force that one would observe by placing one unit of charge on a pith ball and placing it in position. The reason is that one unit of charge may be so large that its presence alters appreciable the field configuration of the array. 

Consequently, one must use a limiting process whereby the ratio of the force on the small test body to the charge on it is measured for smaller and smaller amounts of charge. Experimentally, this ratio and the direction of the force will become constant as the amount of test charge is made smaller and smaller. These limiting values of magnitude and direction define the magnitude and direction of the electric field $\mathbf{E}$ at the point in question. 

In short, placing a test charge can itself change the field configuration, and so we need to use a process of smaller and smaller test charges such that the interference with the source becomes negligible.

In symbols we may write 
$$
\mathbf{F}=q \mathbf{E}
$$
where $\mathbf{F}$ is the force, $\mathbf{E}$ is the electric field, and $q$ is the charge. In this equation it is assumed that the charge $q$ is located at a point, and the force and the electric field are evaluated at that point. Coulomb's law can be written down similarly. If $\mathbf{F}$ is the force on a point charge $q_{1}$, located at $\mathbf{x}_{1}$, due to another point charge $q_{2}$, located at $\mathbf{x}_{2}$, then Coulomb's law is 
$$
\mathbf{F} = kq_{1}q_{2} \frac{\mathbf{x}_{1}-\mathbf{x}_2}{|\mathbf{x}_{1}-\mathbf{x}_{2}|^{3}}
$$
Note that $q_{1}$ and $q_{2}$ are algebraic quantities, which can be positive or negative. The constant of proportionality $k$ depends on the system of units used. The electric field at the point $\mathbf{x}$ due to a point charge $q_{1}$ at the point $\mathbf{x}_{1}$ can be obtained directly:
$$
\mathbf{E}(\mathbf{x}) = kq_{1} \frac{\mathbf{x}-\mathbf{x_{1}}}{|\mathbf{x}-\mathbf{x}_{1}|^{3}}
$$
The constant $k$ difference in different systems of units. In electrostatic units, $k=1$ and unit charge is chosen as that charge that exerts a force of one dyne on an equal point charge located one centimeter away. The esu unit of charge is called the _statcoulomb_, and the electric field is measured in statvolts per centimeter. In the SI system, we use $k = (4 \pi \epsilon_{0})^{-1}$ where $\epsilon_{0}=9.854 \times 10^{-12}$ and $k = 8.987 \times 10^{9}V/m$. One electron has a charge $q \approx 1.602 \times10^{-19} C$. 

The experimentally observed linear superposition of forces due to many charges means that we may write the electric field at $\mathbf{x}$ due to a system of point charges $q_{i}$ located at $\mathbf{x}_{i},i=1,2,\ldots,n$ as the vector sum
$$
\boxed{\mathbf{E}(\mathbf{x}) = \frac{1}{4\pi \epsilon_{0}} \sum\limits_{i=1}^{n}q_{i} \frac{\mathbf{x}-\mathbf{x}_{i}}{|\mathbf{x}-\mathbf{x}_{i}|^{3}}}
$$
If the charges are so small and so numerous that they can be described by a charge density $\rho(\mathbf{x}')$ (if $\Delta q$ is the charge in a small volume $\Delta x \Delta y \Delta z$), then we can replace the sum by an integral
$$
\boxed{\mathbf{E}(\mathbf{x}) = \frac{1}{4\pi \epsilon_{0}}\int\limits \rho(\mathbf{x}') \frac{\mathbf{x}-\mathbf{x}'}{|\mathbf{x}-\mathbf{x}'|^{3}} d^{3} x'}
$$
where $d^{3}x'=dx' dy' dz'$ is a three dimensional volume element at $\mathbf{x}'.$ 

At this point it is worthwhile to introduce the Dirac Delta Function. In one dimension, the delta function, written $\delta(x-a)$, is a mathematically improper function having the properties:

1. $\delta(x-a)=0$ for $x\neq a$, and 
2. $\int\limits \delta(x-a) dx = 1$ if the region of integration includes $x=a$ and is zero otherwise. 

The delta function can be given an intuitive, but non-rigorous, meaning as the limit of a peaked curve such as a Gaussian that becomes narrower and narrower, but higher and higher, in such a way that the area under the curve is always constant. Schwart'z theory of distributions is a comprehensive rigorous mathematical approach to delta functions and their manipulations. From the definitions above it is evident that, for an arbitrary function $f(x)$,

3. $\int\limits f(x) \delta(x-a) dx=f(a)$

The integral of $f(x)$ times the derivative of a delta function is simply understood if the delta function is thought of as a well-behaved, but sharply peaking, function. Thus, the definition is

4. $\int\limits f(x) \delta'(x-a) dx = -f'(a)$

where a prime denoted differentiation with respect to the argument. If the delta function has argument a function $f(x)$ of the independent variable $x$, it can be transformed according to the rule

5. $\delta(f(x)) = \sum\limits_{i} \frac{1}{\left|\frac{df}{dx}(x_{i})\right|}\delta(x-x_{i})$

where $f(x)$ is assumed to have only simple zeros, located at $x=x_{i}$. In more than one dimension, we merely take products of delta functions in each dimension. With cartesian coordinates

6. $\delta(\mathbf{x}-\mathbf{X})=\delta(x_{1}-X_{1})\delta(x_{2}-X_{2})\delta(x_{3}-X_{3})$ 

is a function that vanished everywhere except at $\mathbf{x}=\mathbf{X}$, and is such that 

7. $$\int\limits_{\Delta V}\delta(\mathbf{x}-\mathbf{X}) d^{3}x = \cases{1, \quad \text{if $\Delta V$  contains $\mathbf{x}=\mathbf{X}$} \\ 0, \quad \text{if $\Delta V$ does not contain $\mathbf{x}=\mathbf{X}$}}$$
A discrete set of point charges can be described with a charge density by means of delta functions. For example, 
$$
\rho(\mathbf{x})=\sum\limits_{i=1}^{n}q_{i} \ \delta(\mathbf{x}-\mathbf{x}_{i})
$$
represents a distribution of $n$ point charges $q_{i}$, located at the points $\mathbf{x}_{i}$. Substitution of this charge density into our integral and integration, yields the discrete sum form of the electric field. 

##### Gauss's Law
The integral form given for the electric field is not always the must suitable form for the evaluation of electric fields. There is another integral result, called Gauss's Law, which is sometimes more useful and furthermore leads to a differential equation for $\mathbf{E}(\mathbf{x})$. To obtain Gauss' law we first consider a point charge $q$ and a _closed_ surface $S$, as shown in the figure below. Let $r$ be the distance from the charge to a point on the surface, $\mathbf{n}$ be the outwardly directed unit normal to the surface at that point, $da$ be an element of surface area. 

![[Pasted image 20240903152441.png|center|400]]

If the electric field $\mathbf{E}$ at the point on the surface due to the charge $q$ makes an angle $\theta$ with the unit normal, then the normal component of $\mathbf{E}$ times the area element is 
$$
\mathbf{E} \cdot \mathbf{n} da = \frac{q}{4\pi \epsilon_{0}} \frac{\cos \theta}{r^{2}} da
$$
Since $\mathbf{E}$ is directed along the line from the surface element to the charge $q$, $\cos \theta da =r^{2} d \Omega$, where $d \Omega$ is the element of solid angle subtended by $da$ at the position of the charge. Therefore
$$
\mathbf{E}\cdot \mathbf{n} da = \frac{q}{4\pi \epsilon_{0}} d \Omega
$$
If we not integrate the normal component of $\mathbf{E}$ over the whole surface, it is easy to see that 
$$
\oint_{S} \mathbf{E} \cdot \mathbf{n} \ da = \cases{\frac{q}{\epsilon_{0}}, \quad \text{if $q$ lies inside $S$} \\ 0, \quad \text{if $q$ lies outside $S$}}
$$
This result is Gauss's law for a single point charge. For a discrete set of charges, it is immediately apparent that 
$$
\oint_{S}\mathbf{E}\cdot \mathbf{n} \ da = \frac{1}{\epsilon_{0}} \sum\limits_{i}q_{i}
$$
where the sum is over only those charges _inside_ the surface $S$. For a continuous charge density $\rho(\mathbf{x})$, Gauss's law becomes: 
$$
\boxed{\oint_{S}\mathbf{E}\cdot \mathbf{n} \ da = \frac{1}{\epsilon_{0}}\int\limits_{V} \rho(\mathbf{x}) \ d^{3}x}$$
where $V$ is the volume enclosed by $S$. This equation is one of the basic of electrostatics. Note that it depends upon the inverse square law for the force between chares, the central nature of the force, and the linear superposition of the effects of different charges. Clearly then, Gauss's law holds for Newtonian gravitational force fields, with matter density replacing charge density. 

It is interesting to note that, even before the experiments of Cavendish and Coulomb, Priestley, taking up an observation of Franklin that charge seemed to reside on the outside, but not the inside, of a metal sup, reasoned by analogy with Newton's law of universal gravitation that the electrostatic force must obey an inverse square law with distance.

##### Differential Form of Gauss's Law
Gauss's law can be thought of as being an integral formulation of the law of electrostatics. We can obtain a differential form by using the divergence theorem. The _divergence theorem_ [[Divergence Theorem]] states that for any well behaved vector field $\mathbf{A}(\mathbf{x})$ defined within a volume $V$ surrounded by the closed surface $S$ the relation 
$$
\oint_{S} \mathbf{A} \cdot \mathbf{n} \ da = \int_{V} \nabla \cdot \mathbf{A} \ d^{3}x
$$
holds between the volume integral of the divergence of $\mathbf{A}$ and the surface integral of the outwardly directed normal component of $\mathbf{A}$. The equation in fact can be used as the definition of the divergence. TO apply the divergence theorem we consider the integral relation expressed in Gauss's theorem:
$$
\oint_{S} \mathbf{E} \cdot \mathbf{n} \ da = \frac{1}{\epsilon_{0}} \int_{V}\rho(\mathbf{x}) \ d^{3}x
$$
Now the divergence theorem allows us to write this as 
$$
\int\limits_{V}\left(\nabla \cdot \mathbf{E} - \frac{\rho}{\epsilon_{0}}\right)\ d^{3}x = 0
$$
for an arbitrary volume $V$. We can, in the usual way, put the integral equal to zero to obtain 
$$
\boxed{\nabla \cdot \mathbf{E} = \frac{\rho}{\epsilon_{0}}}
$$
which is the differential form of Gauss's law of electrostatics. This equation can itself be used to solve problems in electrostatics. However, it is often simpler to deal with scalar rather then vector functions of position, and then to derive the vector quantities at the end if necessary.

##### Another Equation of Electrostatics and the Scalar Potential
The single equation above for Gauss's Law is not enough to specify completely the three components of the electric field $\mathbf{E}(\mathbf{x})$. Perhaps some readers know that a vector can be specified almost (up to the gradient of a scalar function that satisfies the Laplace equation) completely if its divergence and curl are given everywhere in space. Thus we look for an equation specifying $\text{curl} \ \mathbf{E}$ as a function of position. Such an equation, namely 
$$
\nabla \times \mathbf{E} = 0
$$
follows directly from our generalized coulomb's law:
$$
\mathbf{E}(\mathbf{x}) = \frac{1}{4\pi \epsilon_{0}} \int\limits \rho(\mathbf{x}') \frac{\mathbf{x}-\mathbf{x}'}{|\mathbf{x}-\mathbf{x}'|^{3}} \ d^{3}x'
$$
The vector factor in the integral, viewed as a function of $\mathbf{x}$, is the negative gradient of the scalar $\frac{1}{|\mathbf{x}-\mathbf{x}'|}$:
$$
\frac{\mathbf{x}-\mathbf{x}'}{|\mathbf{x}-\mathbf{x}'|^{3}} = - \nabla\left(\frac{1}{|\mathbf{x}-\mathbf{x}'|}\right)
$$
Since the gradient operation involved $\mathbf{x}$, but not the integration variable $\mathbf{x}'$, it can be taken outside the integral sign. Then the field can be written 
$$
\boxed{\mathbf{E}(\mathbf{x}) = \frac{-1}{4\pi \epsilon_{0}} \nabla \int\limits \rho\frac{\mathbf{x}'}{|\mathbf{x}-\mathbf{x}'|} d^{3}x}
$$
Since the curl of the gradient of any well-behaved scalar function of position vanishes ($\nabla \times \nabla \psi=0$ for all $\psi$), then we easily see that $\nabla \times \mathbf{E} = 0$. Note that the force is a function of relative distances only, but does not depend on the inverse square nature. We see that the electric field is derived from a scalar by the gradient operation. Since one function of position is easier to deal with than three, it is worthwhile concentrating on the scalar function and giving it a name. Consequently we define the _scalar potential_ $\Phi(\mathbf{x})$ by the equation:
$$
\mathbf{E} = - \nabla \Phi
$$
Then our equation shows that the scalar potential is given in terms of the charge density by 
$$
\boxed{\Phi(\mathbf{x}) = \frac{1}{4\pi \epsilon_{0}} \int\limits \frac{\rho(\mathbf{x}')}{|\mathbf{x}-\mathbf{x}'|} \ d^{3} x'}
$$
where the integration is over all charges in the universe, and $\Phi$ is arbitrary only to the extent that a constant can be added to the right-hand side of the equation above. 

The scalar potential has a physical interpretation when we consider the work done on a test charge $q$ in transporting it from one point $A$ to another point $B$ in the presence of an electric field $\mathbf{E}(\mathbf{x})$, as shown in the figure below. 