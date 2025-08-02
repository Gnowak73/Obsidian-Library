---
tags: Physics, Moment_of_Inertia, Inertia, COM, center_of_mass, mass, density
dg-publish: true
mathLink: 
---
Subject: _Classical Mechanics_
Main\_Topic: _Moment of Inertia and Center of Mass_
Applications: _Rotational Mechanics_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

Inertia is a property of matter describing the resistance to the movement of an object. The moment of inertia is defined as 
$$
I=\sum\limits_{i}mr^{2}
$$
which can then be written in terms of the integral 
$$
I=\int\limits r^{2}dm
$$
where $r$ is the distance from the particle or mass element to the axis of rotation.

**Remark.**  The distance from the element to the axis of rotation must be constant, if it is not, then we will use theorems such as the **Parallel Axis Theorem** and **Perpendicular Axis Theorem** to get around these issues. 

When finding the moment of inertia, we make identify the relationship between an element of mass and the volume. For uniform density this is:
$$
\rho = \frac{M}{V} = \frac{dm}{dV}
$$
for nonuniform density we employ a similar method, we instead just have a function for the density when putting $dm$ into our integral. 

##### Parallel Axis Theorem
**Theorem.**  Let us consider a scenario where we have a moment of inertia $I_{c}$. Now, if we were to consider the moment of inertia from a new axis of rotation that is parallel to the one used in $I_{c}$, then 
$$
I_{new} = I_{c} + md^{2}
$$
where $d$ is the distance from the old axis of rotation to the new axis of rotation. 

**Remark.**  This is simply just a shifting transformation on the axis of rotation, as we will see in the proof.

**Proof:**  To begin the proof of this theorem, we begin by stating that we define the origin to be at the center of mass of the moment of inertia calculation. Then, we start by noting that by using the Pythagorean Theorem:
$$
\int\limits r^{2} \ dm = \int\limits x^{2}+y^{2} \ dm
$$
now if we shift the $x$ by some constant $d_{1}$, and the $y$ by some $d_{2}$ 
$$
\int\limits (x-d_{1})^{2}+(y-d_{2})^{2} \ dm
$$
$$
\int\limits x^{2} + y^{2} \ dm + \int\limits d_{1}^{2} + d_{2}^{2} \ dm -2d_{1}\int\limits x \ dm - 2d_{2} \int\limits y \ dm
$$
Now, remember that we stated that the origin was the center of mass (i.e, $x_{cm}=0, \ y_{cm}=0$). The last two integrals are multiples of the center of mass, so they must equal zero (considering the definition of the center of mass). Now, we have that 
$$
\int\limits r^{2} \ dm = \int\limits x^{2}+y^{2} \ dm + (d_{1}^{2}+d_{2}^{2})\int\limits dm = I_{c} + md^{2}
$$
Thus proving our theorem.

##### Perpendicular Axis Theorem
**Theorem.**  Let us consider the scenario where we have a plane and a perpendicular axis. Now, if we consider the perpendicular axis, such that using the Pythagorean theorem we have 
$$
\int\limits r^{2} \ dm = \int\limits x^{2} + y^{2} \ dm = I_{x}+I_{y}
$$
Thus proving our theorem. 

##### Center of Mass
The coordinates for the center of mass are defined as 
$$
\bar{x} = \frac{I_{y}}{m}, \quad \quad \bar{y} = \frac{I_{x}}{m}
$$
which in vector form is 
$$
\vec{R} = \frac{\sum\limits_{i}m_{i}\vec{r_{i}}}{\sum\limits_{i} m_{i}} 
$$
We can then substitute the integral formulations for $I$ to get 
$$
\bar{x} = \frac{\int\limits r_{y}^{2} \ dm}{\int\limits dm}, \quad \bar{y} = \frac{\int\limits r_{x}^{2} \ dm}{\int\limits  dm}
$$






