---
tags: Math, Complex, Series, Taylor, Taylor_Series, Laurent, analytic, function, power_series
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Taylor Series_
Applications: _Writing Functions as power Series, contour integration applications_
Examples: _[[MATH_450_Quiz_4.pdf]]_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Series]],[[ODE Power Series Solutions]],[[Laurent Series]]_
Cont.\_ of: _None_ 
_
_

**Important Remark.**  A traditional power series, including **Taylor Series**, are only defined for positive exponents. We can extend this notion of a power series to negative exponents called **Laurent Series** ([[Laurent Series]]).

---
We turn to **Taylor's Theorem**, which is one of the most important results in complex series:

**Theorem.**  Suppose that a function $f$ is analytic throughout a disk $|z-z_{0}|<R_{0}$, centered at $z_{0}$ and with a radius $R_{0}$. Then $f(z)$ has the power series representation
$$
f(z) = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n} \quad (|z-z_{0}|<R_{0}),
$$
where 
$$
a_{n}=\frac{f^{(n)}(z_{0})}{n!} \quad (n=0,1,2,\ldots)
$$

That is, this series representation of $f(z)$ converges to $f(z)$ when $z$ lies in the stated _open disk
_
![[Pasted image 20230723174410.png|center]]

This is the expansion of $f(z)$ into what is called a **Taylor Series** about the point $z_{0}$.

```ad-note
Any function which is analytic at a point $z_{0}$ must have a Taylor series about $z_{0}$. For, if $f$ is analytic at $z_{0}$, it is analytic throughout some neighborhood $|z-z_{0}|<\epsilon$ of that point; and $\epsilon$ may serve as the value of $R_{0}$ in the statement of Taylor's theorem. Also, if $f$ is entire, $R_{0}$ can be chosen arbitrarily large; and the condition of validity becomes $|z-z_{0}| < \infty$. The series then converges to $f(z)$ at each point $z$ in the finite plane. 
```

When it is known that $f$ is analytic everywhere inside a circle centered at $z_{0}$, convergence of its Taylor series about $z_{0}$ to $f(z)$ for each point $z$ within that circle is ensured; no test for the convergence of the series is even required. 

**Remark.**  According to Taylor's Theorem, the series converges to $f(z)$ within the circle about $z_{0}$ whose radius is the distance from $z_{0}$ to the nearest point $z_{1}$ at which $f$ fails to be analytic. 

```ad-info
It is also worth noting that a **Maclaurin Series** is a Taylor series where $z_{0}=0$. Such that 
$$
f(z) = \sum\limits_{n=0}^{\infty} \frac{f^{(n)}(0)}{n!}z^{n} \quad (|z|<R_{0})
$$
```

**Proof:**  The proof can be seen in [[Complex Variables Textbook.pdf]]. The beginning of such a proof starts by utilizing the [[Cauchy Integral Formula]]. We can then use the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Theorem]] to show how the remainder is $0$ and so the series holds. 

---
#### Table of Maclaurin Series

![[Pasted image 20230723195140.png|center]]

All Maclaurin Series can be used to make a Taylor series by assessing the circle which the function is analytic. 

##### Example 1
We have the function 
$$
f(z) = \frac{1}{1-z}
$$
about the point $z=i$.

If we want to find the Taylor Series representation, we first look for the circle in which $f$ is analytic. The distance between the singularity $z=1$ and the point we are expanding about $z=i$ is $|1-i|=\sqrt{2}$. Thus, the circle in which our function is analytic is $|z-i|<\sqrt{2}$. To find the power series, we first write 
$$
\frac{1}{1-z} = \frac{1}{(1-i) - (z-i)} = \frac{1}{1-i}\cdot \frac{1}{1-\frac{z-i}{1-i}}
$$
Now, we can check if $\frac{z-i}{1-i}$ fits the condition $|z|<1$ by seeing that 
$$
\left| \frac{z-i}{1-i} \right| = \frac{|z-i|}{|1-i|} = \frac{|z-i|}{\sqrt{2}}<1 
$$
since $|z-i|<\sqrt{2}$. Thus, we can write 
$$
\frac{1}{1-i}\cdot \frac{1}{1-\frac{z-i}{1-i}} = \frac{1}{1-i}\sum\limits_{n=0}^{\infty} \left( \frac{z-i}{1-i} \right)^{n} \quad (|z-i|<\sqrt{2})
$$
Thus, 
$$
\boxed{\frac{1}{1-z} = \sum\limits_{n=0}^{\infty} \frac{(z-i)^{n}}{(1-i)^{n+1}}  \quad (|z-i|<\sqrt{2})}
$$

##### Example 2 
If we take the function $f(z)=e^{z}$, $f(z)$ is entire. Thus, it has a Maclaurin series representation for all $z$. We can write using the Maclaurin series that 
$$
z^{3}e^{2z} = z^{3} \sum\limits_{n=0}^{\infty} \frac{(2z)^{n}}{n!} = \sum\limits_{n=0}^{\infty} \frac{2^{n}}{n!}z^{n+3} \quad (|z|<\infty) 
$$

---
#### Negative Powers of $(z-z_{0})$

If a function $f$ fails to be analytic at a point $z_{0}$, one cannot apply **Taylor's Theorem** there. It is often possible, however, to find a series representation for $f(z)$ involving both positive and negative powers of $(z-z_{0})$. These series ([[Laurent Series]]) can be found by manipulation of the elementary Maclaurin Series in: [[#Table of Maclaurin Series]]. 

##### Example 1
Using the series for $e^{z}$
$$
e^{z} = 1+\frac{z}{1!} + \frac{z^{2}}{2!} + \frac{z^{3}}{3!} +\ldots \quad (|z|<\infty)
$$
we can see that 
$$
\frac{e^{-z}}{z^{2}} = \frac{1}{z^{2}}\left(1 - \frac{z}{1!}+ \frac{z^{2}}{2!} - \frac{z^{3}}{3!} + \ldots \right) = \frac{1}{z^{2}} - \frac{1}{z} + \frac{1}{2!} - \frac{z}{3!} + \ldots
$$
when $0<|z|<\infty$.  

##### Example 2
Let us have the function 
$$
f(z) =  \frac{1+2z^{3}}{z^{3}+z^{5}} = \frac{1}{z^{3}} \cdot  \frac{2(1+z^{2})-1}{1+z^{2}} = \frac{1}{z^{3}} \left( 2- \frac{1}{1+z^{2}} \right)
$$
we can expend this into a series involving powers of $z$. We cannot find a Maclaurin series since $f(z)$ is not analytic at $z=0$. But we do know that 
$$
\frac{1}{1-z} = 1+ z + z^{2} + z^{3} + \ldots \quad (|z|<1);
$$
and, after replacing $z$ by $-z^{2}$ on each side here, we have 
$$
\frac{1}{1+z^{2}} = 1 - z^{2}+ z^{4} -z^{6}+\ldots \quad (|z|< 1).
$$
So when $0<|z|<1$, 
$$
f(z) = \frac{1}{z^{3}}(2-1+z^{2}-z^{4}+z^{6}+\ldots) = \frac{1}{z^{3}} + \frac{1}{z} - z + z^{3}-z^{5}+\ldots
$$

##### Example 3
We propose to expand the function 
$$
\frac{e^{z}}{(z+1)^{2}}
$$
in powers of $(z+1)$. We can start with the Maclaurin Series 
$$
e^{z} = \sum\limits_{n=0}^{\infty} \frac{z^{n}}{n!} \quad (|z|<\infty)
$$
and replace $z$ by $z+1$:
$$
e^{z+1} = \sum\limits_{n=0}^{\infty} \frac{(z+1)^{n}}{n!} \quad (|z+1|<\infty).
$$
Dividing through this equation by $e(z+1)^{2}$ reveals that 
$$
\boxed{\frac{e^{z}}{(z+1)^{2}} = \sum\limits_{n=0}^{\infty} \frac{(z+1)^{n-2}}{n!e} \quad (0<|z+1|<\infty)} 
$$


