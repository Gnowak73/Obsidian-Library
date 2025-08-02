---
tags: contour, Math, complex, cauchy, residue, integral, integration
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Cauchy Residue Theorem_
Applications: _Contour integrals_
Examples: _[[MATH_450_Quiz_4.pdf]]_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Residues, Zeros, and Poles]],[[Laurent Series]],[[Contour Integrals]],[[Application of Residues]]_
Cont.\_ of: _None_ 
_
_

If, except for a _finite_ number of singular points, a function $f$ is [[Analytic Functions|analytic]] inside a simple closed contour $C$, those singular points must all be isolated ([[Residues, Zeros, and Poles#Isolated Singular Points]]). The following theorem, which is known as **Cauchy's Residue Theorem**, is a precise statement of the fact that if $f$ is also analytic on $C$ and if $C$ is positively oriented, the the value of the integral of $f$ around $C$ is $2 \pi i$ times the sum of the residues of $f$ at the singular points inside of $C$. 

**Theorem.**  Let $C$ be a simple closed contour, described in the positive sense. If a function $f$ is analytic inside and on $C$ except for a finite number of singular points $z_{k} \ (k=1,2,\ldots,n)$ inside $C$, then 
$$
\boxed{\int\limits_{C}f(z) \ dz = 2 \pi i \sum\limits_{k=1}^{n}Res_{z=z_{k}} \ f(z)}
$$
![[Pasted image 20230727183236.png|center]]

**Proof:**  The proof of this theorem comes from the [[Cauchy Goursat Theorem]] extension to [[Contour Integral Domains#Multiply Connected Domains|multiply connected domain contour integrals]], which allows us to break up a contour integral of a multiply-connected domain into a sum of contour integrals. We know that each contour integral can then be expressed in terms of its residues from [[Residues, Zeros, and Poles]], so we get
$$
\int\limits_{C}f(z) \ dz - \sum\limits_{k=1}^{n}\int\limits_{C_{k}}f(z) \ dz = 0
$$
$$
\int\limits_{C_{k}}f(z) \ dz = 2 \pi i \ Res_{z=z_{0}} \ f(z)
$$
so 
$$
\int\limits_{C}f(z) \ dz = 2 \pi i \sum\limits_{k=1}^{n} Res_{z=z_{0}} \ f(z)
$$
and the proof is complete. Do realize that the contours $C_{k}$ were defined as CCW which is why the **negative sign** is there initially for the multiply connected domain Cauchy-Goursat Theorem. 

---
##### Example 1
Let us use this theorem to find the integral
$$
\int\limits_{C} \frac{4z-5}{z(z-1)} \ dz
$$
where $C$ is the circle $|z|=2$ in the CCW direction. Now, we have two isolated singularities $z=0$ and $z=1$, both of which are interior to $C$. We first find the residue at $z=0$ by considering the punctured disk $0<|z|<1$.
$$
\frac{1}{1-z} = \sum\limits_{n=0}^{\infty}z^{n} \quad (|z|<1)
$$
Now, 
$$
\frac{4z-5}{z(z-1)} = \frac{-(4z-5)}{z} \cdot \frac{1}{1-z} = \frac{-(4z-5)}{z}\sum\limits_{n=0}^{\infty}z^{n} = (4z-5)\sum\limits_{n=0}^{\infty}-z^{n-1} = \sum\limits_{n=0}^{\infty}-4z^{n} + \sum\limits_{n=0}^{\infty}5z^{n-1}
$$
From the scenario $n=0$ we can clearly see that $B_{1}=5$. Now, let us consider the punctured disk $0<|z-1|<1$. We now have 
$$
\frac{4z-5}{z(z-1)} = \frac{4z-5}{z-1} \cdot \frac{1}{1+(z-1)} = \frac{4(z-1)-1}{z-1}\sum\limits_{n=0}^{\infty}(z-1)^{n} = 4\sum\limits_{n=0}^{\infty}(z-1)^{n}-\sum\limits_{n=0}^{\infty}(z-1)^{n-1} \quad (0<|z-1|<1)
$$
which holds since $|z-1|<1$ when $0<|z-1|<1$. Now, from this we can easily see that the $n=0$ case results in $B_{2}=-1$. 

We can finally find the value of the contour integral to be 
$$
2 \pi i (B_{1}+B_{2}) = 2\pi i(4) = \boxed{8\pi i}
$$
![[Pasted image 20230727192744.png|center]]

---
### Residue at Infinity
Suppose that a function $f$ is analytic throughout the finite plane except for a finite number of singular points interior to a positively oriented simple closed contour $C$. Next, let $R_{1}$ denote a positive number which is large enough that $C$ lies inside the circle $|z|=R_{1}$. The function $f$ is evidently analytic throughout the domain $R_{1}<|z|<\infty$. And, as already mentioned in [[Residues, Zeros, and Poles#Isolated Singular Points]], the point at infinity is then said to be an isolated singular point of $f$. 

![[Pasted image 20230727193147.png|center]]

Now let $C_{0}$ denote a circle $|z|=R_{0}$, oriented in the _clockwise_ direction, where $R_{0}>R_{1}$. The _residue of $f$ at infinity_ is defined by means of the equation
$$
\int\limits_{C_{0}}f(z) \ dz = 2 \pi i \ Res_{z=\infty} \ f(z)
$$
and since $f$ is analytic throughout the closed region bounded by $C$ and $C_{0}$, the principle of deformation of paths ([[Contour Integral Domains#Multiply Connected Domains]]) tells us that 
$$
\int\limits_{C}f(z) \ dz = \int\limits_{-C_{0}}f(z) \ dz = -\int\limits_{C_{0}}f(z) \ dz
$$
So, in view of our definition for the residue at infinity,
$$
\int\limits_{C}f(z) \ dz = - 2 \pi i \ Res_{z=\infty} \ f(z)
$$
---
**Remark.**  The residue at infinity is defined to be the residue when there are no isolated singularities. We know that the Cauchy Residue Theorem must still hold even if there aren't any traditional singularities. Thus, the only other option for an isolated singularity would be the point at infinity.

```ad-Remember
Going Counter-Clockwise around $0$ is the _SAME_ as going Clockwise around $\infty$! Think of the riemann sphere and how clockwise on one pole is counter-clockwise on the other pole.

The interior of a contour is everything left of the contour. Thus, going the opposite way changes what we consider the _interior_ of the contour. 
```

---

To find this residue at infinity, we write the [[Laurent Series]]
$$
f(z) = \sum\limits_{n=-\infty}^{\infty}c_{n}z^{n}\quad (R_{1}<
|z|<\infty)
$$
where 
$$
c_{n}=\frac{1}{2 \pi i}\int\limits_{-C_{0}} \frac{f(z) \ dz}{z^{n+1}} \quad (n=0,\pm 1,\pm 2,\ldots)
$$
Replacing the $z$ by $\frac{1}{z}$ in the Laurent Series and then multiplying the result by $1/z^{2}$, we see that 
$$
\frac{1}{z^{2}}f\left(\frac{1}{z}\right) = \sum\limits_{n=-\infty}^{\infty} \frac{c_{n}}{z^{n+2}} = \sum\limits_{n=-\infty}^{\infty} \frac{c_{n-2}}{z^{n}}\quad \left(0<|z|<\frac{1}{R_{1}}\right)
$$
and we know that 
$$
c_{-1} = Res_{z=0} \left[\frac{1}{z^{2}} f\left(\frac{1}{z}\right)\right]
$$
Putting $n=-1$ into our integral expression, we now have that 
$$
c_{-1} = \frac{1}{2 \pi i} \int\limits_{-C_{0}} f(z) \ dz = Res_{z=\infty} \ f(z)
$$
Thus, we have the relationship
$$
\boxed{Res_{z=\infty} \ f(z) = - Res_{z=0}\left[\frac{1}{z^{2}} f\left(\frac{1}{z}\right)\right] }
$$
We can now establish the theorem for infinite residues:

**Theorem.**  If a function $f$ is analytic everywhere in the finite plane except for a finite number of singular points _interior_ to a **positively oriented simple closed** contour $C$, then
$$
\boxed{\int\limits_{C} f(z) \ dz = \  -2\pi i Res_{z=\infty} \ f(z) =  2 \pi i \ Res_{z=0}\left[\frac{1}{z^{2}}f  \left( \frac{1}{z}  \right) \right]}
$$

##### Example 
It is easy to see that the singularities of the function
$$
f(z) = \frac{z^{3}(1-3z)}{(1+z)(1+2z^{4})}
$$
all lie inside the positively oriented circle $C$ centered at the origin with radius $3$. In order to use the theorem in this section, we write
$$
f(z) = \frac{1}{z} \cdot \frac{z-3}{(z+1)(z^{4}+2)}
$$
Now, we see that the fraction $\frac{z-3}{(z+1)(z^{4}+2)}$ is analytic at the origin. Thus, it is represented by a Maclaurin Series whose first term is when $z=0$, which would be $\frac{-3}{2}$. This is the coefficient of the $\frac{1}{z}$ term since we would have the series 
$$
\frac{1}{z} \left(\frac{-3}{2} + a_{1}z^{1}+a_{2}z^{2}+\ldots\right) \quad (0<|z|<R_{0})
$$
where $R_{0}$ is the radius of until we hit another point of $f(z)$ that isn't analytic. But we do not need to know $R_{0}$ for this problem. Now, we know that $B_{1}=\frac{-3}{2}$, thus
$$
\int\limits_{C}f(z) \ dz = 2 \pi i \ Res_{z=0} \ f(z) = 2 \pi i \left(\frac{-3}{2}\right) = \boxed{-3\pi i}
$$
