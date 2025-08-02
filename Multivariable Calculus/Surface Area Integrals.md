---
tags: Math, Multivariable, theorem, Integrals, Line_Integrals, Surface_Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Surface Area Integrals_
Applications: _Surface Area, [[Surface Integral]]_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Surface Integral]], [[Line Integrals]] _
_
_
For all cases, assume that the surface is Smooth.

> Remember: $\nabla F$ is normal to the surface $F$.

#### Implicit Case
Lets say we have a surface $F(x,y,z)=C$.

If we have a surface above a the $xy$ plane such that $\nabla F \cdot \hat k \neq 0$, in other words, the surface has some upwards slope component at all times. We also assume that $\nabla F \neq 0$. Then,

$$
SA = \int\int_{R}\frac{|\nabla F|}{|\nabla F \cdot\hat k|}dA
$$
The $xy$ plane can be switched out for any plane, and $\hat k$ could have been $\hat i$ or $\hat j$. 

#### Explicit Surface
If we have an explicit scenario where $z=f(x,y)$, we can use our implicit formula where $F(x,y,z) = f(x,y)-z=0$. Plugging this in we can prove that for explicit cases,
$$
SA = \int\int_{R} \sqrt{f_{x}^{2}+f_{y}^{2}+1} \ dA
$$

#### Parametric Surface
If we have a parametric surface $r(u,v) = f(u,v)\hat i + g(u,v) \hat j + h(u,v)\hat k$, we can add up infinitesimal parallelograms (remember that parallelograms have area $|\vec{a} \times \vec{b}|$), we can assume there is a stretch factor to make sure that our parallelogram length vectors overlap the surface. We also note that for a parallelogram we want vectors that are orthogonal. Lucky for us, the partial derivatives should be orthogonal since the other variable is constant when take one partial derivative. This leads us with an area of a parallelogram with a stretch factor from the partial derivatives: $|\vec{r}_{u}\times \vec{r}_{v} \Delta u \Delta v|$. If we let $\Delta u, \Delta v$ go infinitesimal and add them, we get the integral formula: 

$$
SA = \int\int_{R}|\vec{r}_{u}\times\vec{r}_{v}| \ dudv
$$