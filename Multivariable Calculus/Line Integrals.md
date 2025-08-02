---
tags: Math, Multivariable, Integrals, Line_Integrals, theorem, Surface_Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Line Integrals_
Applications: _Work, Physics, Flux_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

Line integrals represent adding up the value of a function on a curve. Due to there being two different types of functions: scalar and vector, we have two different line integral definitions. The scalar one is simply adding the values of a function on a curve. The vector one is adding up the projection of a vector onto the curve at each point.

---
###### Vector Function
Line integrals represent the infinitesimal addition of the dot product between a differential along a curve and some vector, usually a force. For a vector field, they are represented as:

$$
\int_{C}\vec{F}\cdot d\vec{r}
$$
where $d\vec{r}$ can be separated into differential vectors depending on your coordinate system. For example, in cartesian, $d\vec{r}=(dx,dy,dz)$, we can actually expand this dot product if we wanted to. If we parametrize $r$ by $t$, we can also say that $d\vec{r} = \frac{d\vec{r}}{dt}dt$ such that 
$$\boxed{\int_{C}\vec{F}\cdot d\vec{r} = \int_{a}^{b}\vec{F}(\vec{r}(t)) \cdot \frac{d\vec{r}}{dt} \ dt}
$$
---
###### Scalar Function
For scalar fields, we are adding up the values of a function along a curve, which is represented as:
$$
\int\limits_{C}f(\vec{r})ds
$$
where $ds$ is the infinitesimal, differential [[Arclength]]. Now, we know from basic physics that $speed=|velocity|$ where $v=\frac{\Delta x}{\Delta t}$. We can imply from this, that the speed, $\frac{ds}{dt}$, is the norm of the velocity, $\frac{d\vec{r(t)}}{dt}$, where $r(t)$ parametrizes the curve. Thus,
$$
\frac{ds}{dt}=   \left|\frac{d\vec{r}}{dt} \right|
$$
And therefore:
$$
\boxed{\int_{C}f(\vec{r})ds = \int\limits_{a}^{b}f(\vec{r}(t))  \left| \frac{d\vec{r}}{dt} \right| \ dt}
$$
---
---
### Theorems:
1. [[Green's Theorem (circulation)]] Relation between Line Integrals and [[Surface Area Integrals]] in 2D. (Vector Field Line Integral and Curl)
2. [[Green's Theorem (flux)]] Relation between [[Surface Area Integrals]] with the curl and the [[Flux Integral]] in 2D. (Flux and Divergence)
3. [[Fundamental Theorem of Line Integrals]] Path Dependence and Conservative Forces to solve Line Integrals. (Conservative Force)
4. [[Stokes' Theorem]] relates the Line Integral and the Curl over a Surface in 3D in the form of a [[Flux Integral]]. (Vector Field Line Integral and Curl $\rightarrow$ Flux Integral)
5. [[Divergence Theorem]] relates the [[Surface Integral]] and the [[Flux Integral]] in 3D. (Flux and Divergence) 