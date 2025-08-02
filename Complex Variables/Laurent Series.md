---
tags: Laurent, Math, Complex, Series, Taylor_series, Laurent_Series, contour, integration
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Laurent Series_
Applications: _Power Series, Contour Integration_
Examples: _[[MATH_450_Quiz_4.pdf]]_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Taylor Series]],[[Complex Series]]_
Cont.\_ of: _None_ 
_
_

```ad-Definition
A traditional power series, including **Taylor Series**, are only defined for positive exponents. We can extend this notion of a power series to positive **AND** negative exponents called **Laurent Series** ([[Laurent Series]]).
```

**Theorem.**  Suppose that a function $f$ is analytic throughout an annular domain $R_{1}<|z-z_{0}|<R_{2}$, centered at $z_{0}$, and let $C$ denote any positively oriented simple closed contour around $z_{0}$ and lying in that domain. Then, at each point in the domain, $f(z)$ has the series representation
$$
\boxed{f(z) = \sum\limits_{n=0}^{\infty}a_{n} (z-z_{0})^{n} + \sum\limits_{n=1}^{\infty} \frac{b_{n}}{(z-z_{0})^{n}} \quad (R_{1} < |z-z_{0}|<R_{2})},
$$
where 
$$
\boxed{a_{n} = \frac{1}{2 \pi i} \int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{n+1}} \quad (n=0,1,2,\ldots)}
$$
and 
$$
\boxed{b_{n} = \frac{1}{2 \pi i} \int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{-n+1}} \quad (n=1,2,\ldots)}
$$
![[Pasted image 20230724023717.png|center]]

---
Note how replacing $n$ by $-n$ in the second series in this representation enables us to write that series as 
$$
\sum\limits_{n=-\infty}^{-1} \frac{b_{-n}}{(z-z_{0})^{-n}},
$$
where 
$$
b_{n}= \frac{1}{2 \pi i} \int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{n+1}} \quad (n=-1,-2,\ldots)
$$
Thus,
$$
f(z) = \sum\limits_{n=-\infty}^{-1} b_{-n}(z-z_{0})^{n} + \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n} \quad (R_{1}<|z-z_{0}|<R_{2})
$$
If 
$$
c_{n} = \cases{b_{-n},\quad \text{when} \ n\leq -1 \\
a_{n},  \ \ \quad \text{when} \ n\geq 0}
$$
this becomes 
$$
\boxed{f(z) = \sum\limits_{n=-\infty}^{\infty}c_{n}(z-z_{0})^{n} \quad (R_{1}<|z-z_{0}|<R_{2})}
$$
where 
$$
\boxed{c_{n} = \frac{1}{2 \pi i} \int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{n+1}} \quad (n=0,\pm 1, \pm 2,\ldots)}
$$
Either one of these representations is called a **Laurent Series**. 

---
**Remark.**  We can observe from the integrand that if $f(z)$ is analytic at $z_{0}$, then we can use the [[Cauchy Integral Formula]] such that  
$$
a_{n} = \frac{1}{2 \pi i} \int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{n+1}} = \frac{f^{(n)}(z_{0})}{n!} \quad (n=0,1,2,\ldots) 
$$
and then, due to the [[Cauchy Goursat Theorem]]:
$$
b_{n} = \frac{1}{2 \pi i} \int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{-n+1}} = 0 \quad (n=1,2,\ldots)
$$
Now, we can see that the Laurent Series simply converges to the [[Taylor Series]] when $f(z)$ is analytic throughout an open disk instead of an annulus. 

**Proof of Laurent's Theorem:**  The proof can be found in [[Complex Variables Textbook.pdf]], where similar work is done with the proof of the Taylor Series. The [[Cauchy Integral Formula]] is once again used except with the additional use of [[Contour Integral Domains]]. Then, the [[Complex Series#Remainders|remainder]] of the series is shown to approach $0$. This result is then extended for any $z_{0}$. 

---
##### Example 
The function 
$$
f(z) = \frac{1}{z(1+z^{2})} = \frac{1}{z} \cdot \frac{1}{1+z^{2}}
$$
has singularities at $z=0$ and $z=\pm i$. Let us find the Laurent series representation of $f(z)$ that is valid in the punctured disk of $0<|z|<1$. 

Since $|-z^{2}|<1$ when $|z|<1$, we may substitute $-z^{2}$ for $z$ in the Maclaurin Series
$$
\frac{1}{1-z} = \sum\limits_{n=0}^{\infty}z^{n}\quad (|z|<1)
$$
The result is 
$$
\frac{1}{1+z^{2}} = \sum\limits_{n=0}^{\infty} (-z^{2})^{n} = \sum\limits_{n=0}^{\infty}(-1)^{n}(z)^{2n} \quad (|z|<1)
$$

and so,
$$
f(z) = \frac{1}{z} \cdot \frac{1}{1+z^{2}} = \frac{1}{z}\sum\limits_{n=0}^{\infty}(-1)^{n}(z)^{2n} = \sum\limits_{n=0}^{\infty}(-1)^{n}z^{2n-1} \quad (0<|z|<1)
$$
That is,
$$
f(z) = \frac{1}{z} + \sum\limits_{n=1}^{\infty}(-1)^{n}z^{2n-1} \quad (0<|z|<1)
$$
