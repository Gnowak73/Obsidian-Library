---
tags: Complex, Math, series, properties, analyticity, convergence, continuous, absolute_and_uniform_convergence, continuity_of_power_series, integration_and_differentiation_of_power_series
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Properties of Complex Series_
Applications: _Analyticity, continuity, convergence, and uniqueness of series representations_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Taylor Series]]_
Cont.\_ of: _None_ 
_
_

##### Absolute and Uniform Convergence of Power Series 
We recall from [[Complex Series]] that a series of complex numbers _converges absolutely_ if the series of absolute values of those numbers converges. The following theorem concerns the absolute convergence of power series. 

---
**Theorem 1.**  If a power series 
$$
\sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n}
$$
converges when $z=z_{1} \  (z_{1} \neq z_{0})$, then it is absolutely convergence at each point $z$ in the open disk $|z-z_{0}|<R_{1}$, where $R_{1}=|z_{1}-z_{0}|$

![[Pasted image 20230724185014.png|center]]

**Proof:**  The proof for this theorem can be seen in [[Complex Variables Textbook.pdf]], <mark style="background: #FFB86CA6;">page 208</mark>. It starts by looking at the remainder and a _circle of convergence_ of the series. 

```ad-Definition
The _circle of convergence_ is the greatest circle centered at some point $z_{0}$ such that the series convergest at each ponit inside of this circle.
```

---
**Theorem 2.**  If $z_{1}$ is a point inside the circle of convergence $|z-z_{0}|=R$ of a power series
$$
\sum\limits _{n=0}^{\infty}a_{n}(z-z_{0})^{n}
$$
then that series must be _uniformly convergent_ in the closed disk $|z-z_{0}|\leq R_{1}$, where $R_{1}=|z_{1}-z_{0}|$. 

![[Pasted image 20230724185508.png|center]]

```ad-Definition
From [[Complex Series#Convergence of Sequences]], for the convergence of a sequence,
$$
|z_{n} - z_{0} | < \epsilon \quad \text{whenever} \quad n>n_{\epsilon}
$$
When the choice of $n_\epsilon$ depends only on the value of $\epsilon$ and is independent of the point $z$ taken in a specified region within the circle of convergence, the convergence is said to be **Uniform** in that region. [[Uniform and Pointwise Convergence]].
```

We can extend this notion of uniform convergence in order to write for a series 
$$
|S_{N} - S| < \epsilon \quad \text{whenever} \quad n>n_\epsilon
$$
when using [[Complex Series#Remainders|remainders]] such that 
$$
|\rho_{N}-0| = |\rho_{N }|< \epsilon \quad \text{whenever} \quad n>n_{\epsilon}
$$
**Proof:**  The construction of the proof follows the idea of using the remainder as above. It can be seen on <mark style="background: #ADCCFFA6;">page 211.</mark> in [[Complex Variables Textbook.pdf]]


##### Continuity of Sums of Power Series
Our next theorem is an important consequence of uniform convergence discussed before. 

**Theorem.**  A power series 
$$
\sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n}
$$
representants a continuous function $S(z)$ at each point inside its circle of convergence $|z-z_{0}|=R$. 

**Remark.**  Another way to state this theorem is to say that if $S(z)$ denotes the sum of series within its circle of convergence and if $z_{1}$ is a point inside that circle, then for each positive number $\epsilon$ there is a positive number $\delta$ such that 
$$
|S(z) - S(z_{1})| < \epsilon \quad \text{whenever} \quad |z-z_{1}|<\delta
$$
this is from the definition of [[Complex Continuity]] using the delta epsilon definition of the limit. 

**Proof:**  Proof can be seen in <mark style="background: #FFF3A3A6;">chapter 5, page 211</mark> of [[Complex Variables Textbook.pdf]]. One again, the remainder is used to prove the convergence. 


### Integration and Differentiation of Power Series
We have just seen that a power series 
$$
S(z) = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n}
$$
represents a continuous function at each point interior to its circle of convergence. We will now prove that the sum $S(z)$ is actually analytic within that circle. Our proof depends on the following theorem, which is of interest in itself.

---
**Theorem.**  Let $C$ denote any contour interior to the circle of convergence of the power series expressed above and let $g(z)$ be any function that is continuous on $C$. The series formed by multiplying each term of the power series by $g(z)$ can be integrated term by term over $C$; that is,
$$
\int\limits_{C}g(z)S(z) \ dz = \sum\limits_{n=0}^{\infty}a_{n}\int\limits_{C}g(z)(z-z_{0})^{n}\ dz
$$
**Proof:**  The proof once again is form using the remainder and and some trickery with the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Moduli Theorem]]. It can be seen in detail in [[Complex Variables Textbook.pdf]] on <mark style="background: #FF5582A6;">page 213</mark>. 

---

If we take this theorem and assume that we have $|g(z)|=1$ then we can see that due to $(z-z_{0})^{n}$ begin analytic in the entire domain, for any contour $C$ we would have
$$
\int\limits_{C}S(z) \ dz = 0
$$
proving that $S(z)$ is analytic. A more in depth explanation can be seen in [[Complex Variables Textbook.pdf]] on <mark style="background: #CACFD9A6;">page 213</mark>.

**Corollary.**  The sum $S(z)$ of a power series is analytic at each point $z$ interior to the circle of convergence of than series. 

This corollary is often helpful in establishing the analyticity of  functions and in evaluating limits. For example, if we have a function that is not analytic at that point, then we know we have the largest circle of convergence because if it could be bigger then the sum would need to be analytic there! 

In other words, if we see the convergence of the power series, we can then assume the analyticity of a function!

---
**Theorem 2.**  A power series can be differentiated term by term. That is, at each point $z$ interior to the circle of convergence of that series,
$$
S'(z) = \sum\limits_{n=0}^{\infty} n a_{n}(z-z_{})^{n-1}
$$
**Proof:**  The proof can be seen on <mark style="background: #D2B3FFA6;">page 215</mark> in [[Complex Variables Textbook.pdf]]. The proof starts by denoting some contour and using **Theorem 1.**  and since $S(z)$ is analytic, we can use the [[Cauchy Integral Formula]] to write the derivative of $S(z)$. 
