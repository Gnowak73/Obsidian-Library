---
tags: complex, Math, green, greens_theorem, theorem, complex_plane, multivariable, cauchy, goursat
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Green's Theorem on the Complex Plane_
Applications: _Contour Integration_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Green's Theorem (circulation)]],[[Contour Integrals]]_
Cont.\_ of: _None_ 
_
_
If we had the [[Contour Integrals|contour integral]] on the Complex Plane:
$$
\int\limits_{C}f(z) \ dz
$$
and if 
$$
f(z) = u+iv, \quad z=x+iy
$$
Then the integrand in our contour integral is the product 
$$
\int\limits_{C}(u+iv)(dx+idy)
$$
such that we get
$$
\int\limits_{C} u \ dx - v \ dy + i \int\limits_{C}v \ dx + u \ dy
$$

Now, as we remember from [[Green's Theorem (circulation)]]:
$$
\int\limits_{C} M \ dx + N\ dy = \int\limits\int _{R} N_{x}-M_{y} \ dA
$$
So, we can write our contour integral as 
$$
\int\limits\int_{R}(-v_{y}-u_{y}) \ dA + i \int\limits\int_{C}(u_{x}-v_{y}) \ dA
$$

```ad-note
If we use the Cauchy-Riemann equations, these integrals become $0$, and we end up with Cauchy's Theorem (later advanced into [[Cauchy Goursat Theorem]]). 
```
