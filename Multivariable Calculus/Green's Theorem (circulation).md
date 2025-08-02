---
tags: Math, Multivariable, theorem, Integrals, Line_Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Green's Theorem_
Applications: _Line Integral Technique_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Green's Theorem (flux)]], [[Stokes' Theorem]]_
_
_

Green's Theorem relates the [[Line Integrals]] to the area of a 2d region. Let $C$ is a positively oriented, piecewise smooth, simple (non-overlapping) closed curve in a <mark style="background: #BBFABBA6;">plane (ONLY 2D)</mark>. Then,
$$
\int\limits_{C} \vec{F}\cdot d\vec{r} = \int_{C}(M,N)\cdot (dx,dy) = \int_{C} M\ dx + N \ dy=\int\int_{D}\vec{\nabla} \times \vec{F} \ dA  

$$
This is true as long as $M$ and $N$ along with their first partial derivatives, are continuous throughout the closed region $D$ consisting of all points interior to and on the simple closed contour $C$.

```ad-note
This can be used on the complex plane if you separate the contour integral similar to above. [[Green's Theorem on the Complex Plane]]
```
