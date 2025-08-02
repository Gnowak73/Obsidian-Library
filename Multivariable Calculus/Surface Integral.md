---
tags: Math, Multivariable, theorem, Integrals, Line_Integrals, Surface_Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Surface Integral_
Applications: _Value of Functions added along each point on a Surface_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Surface Area Integrals]], [[Line Integrals]]_
_
_
Surface Integrals are an extension of [[Surface Area Integrals]] . A smooth surface $S$ has surface area
$$
\int\int_{S} d\sigma
$$
where $d\sigma$ is a little piece of differential surface area. Surface areas are measuring the area of a differential surfaces across some space. Now, what if we want to add up the values of a function on such a surface? That is a surface integral.
$$
Surface \ Integral = \int\int_{S}G(x,y,z)\ d\sigma
$$
Our Formulas are very similar from [[Surface Area Integrals]]

##### Formulas:
###### Parametric
$r(u,v)=f(u,v)\hat i + g(u,v) \hat j +h(u,v) \hat k$,
$$
SI = \int\int_{R}G(f(u,v),g(u,v),h(u,v))|\vec{r}_{u}\times \vec{r}_{v}|\ dudv
$$
###### Implicit
$F(x,y,z)=C$
$$
SI = \int\int_{R} G(x,y,z) \frac{|\nabla F|}{|\nabla F \cdot \vec{p}|} \ dA
$$

###### Explicit
$z=f(x,y)$
$$
SI = \int\int_{R}G(x,y,f(x,y)) \sqrt{f_{x}^{2}+f_{y}^{2}+1} \ dA
$$


