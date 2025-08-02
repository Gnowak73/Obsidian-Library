---
tags: contour, Math, Complex, integral, simple, multiply, domains, contour_domains, cauchy-goursat, goursat, cauchy, contour_domains, simply_connected, multiply_connected
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Contour Integral Domains_
Applications: _Contour Integrals_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Cauchy Goursat Theorem]], [[Contour Integrals]], [[Analytic Functions]]_
Cont.\_ of: _None_ 
_
_

##### Simply Connected Domains
```ad-Definition
A _simply connected_ domain $D$ is a domain such that every simple closed contour within it encloses only points of $D$. 
```
The closed contour in the [[Cauchy Goursat Theorem]] doesn't need to be simple when the theorem is adapted to simply connected domains. More precisely, the contour is allowed to cross itself. The following theorem allows for this possibility.

**Theorem.**  If a function $f$ is analytic throughout a simply connected domain $D$, then
$$
\int\limits_{C}f(z) \ dz = 0
$$
for every closed contour $C$ lying in $D$.

**Proof:**  The proof for this theorem comes from the fact that if $C$ is a _simple_ closed contour or if it is a closed contour that intersects itself a _finite_ number of times. For if $C$ is simple and lies in $D$, the function $f$ is analytic at each point interior to and on $C$; and the [[Cauchy Goursat Theorem]] ensures that the contour integral is $0$. Furthermore, if $C$ is closed but intersects itself a finite number of times, it consists of a finite number of simple closed contours, and the [[Cauchy Goursat Theorem]] can be applied again. 

---
**Remark.**  Subtleties arise if the closed contour has an _infinite_ number of self-intersection points. More can be seen on this in [[Complex Variables Textbook.pdf]]. 

It is worth noting though that one main method used to show that the Cauchy-Goursat theorem still holds is by creating a third contour that doesn't intersect the two infinitely intersecting contours except for at the end points of the contours. We can then use the fact the Cauchy Goursat theorem says that any closed contour is $0$ to show that the 
$$
\int\limits_{C_{1}}f(z) \ dz - \int\limits_{C_{3}} f(z) \ dz = 0
$$
and 
$$
\int\limits_{C_{2}}f(z) \ dz + \int\limits_{C_{3}} f(z) \ dz = 0
$$
Thus,
$$
\int\limits_{C}f(z) \ dz = \int\limits_{C_{1}} f(z) \ dz + \int\limits_{C_{2}} f(z) \ dz = \int\limits_{C_{3}} f(z) \ dz - \int\limits_{C_{3}} f(z) \ dz = 0
$$
We can see such a method for a graph like the one below:
![[Pasted image 20230710171649.png|center]]

---


**Corollary.**  A function $f$ that is analytic throughout a simply connected domain $D$ must have an antiderivative everywhere in $D$.

This Corollary follows from the fact that if $f$ is analytic then the contour integral is $0$ for any closed contour, that means that antiderivatives exist such that there is no path dependence. Since this is true for **ANY** contour, and any point in the domain can be the beginning and end of a contour, then for every point in the domain $D$ there must exist an antiderivative. Thus, $f$ has an antiderivative at every point in $D$. 

---
##### Multiply Connected Domains
A domain that is not simply connected is said to be _multiple connected_. The following theorem is an adaptation of the Cauchy-Goursat theorem to multiply connected domains. 

**Theorem**  Suppose that 
a)  $C$ is a simply closed contour, described in the counterclockwise direction;
b)  $C_{k}$ are simple closed contours interior to $C$, all described in the _clockwise direction_ (considered a negative contour), that are disjoint and whose interiors have no points in common.

If a function $f$ is analytic on all of these contours and throughout the multiply connected domain consisting of the points inside $C$ and exterior to each $C_{k}$, then
$$
\int\limits_{C}f(z) \ dz + \sum\limits _{k=1}^{n}\int\limits_{C_{k}} f(z) \ dz = 0
$$
![[Pasted image 20230710011527.png|center]]

Note that the direction of each path of integration is such that the multiply connected domain lies to the _left_ of that path. 

**Proof:**  The proof of such a theorem is explained in [[Complex Variables Textbook.pdf]]. 

We can expand this theorem into a principle known as **the principle of deformation of paths** since we see from the theorem that we can write the contour integral of any path as the contour integral of a contour interior or exterior to our original one. 