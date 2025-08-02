---
tags: Complex, Math, Singularities, Poles, points, singular, Picards_theorem, theorem, picard, residue
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _The Three Types of Isolated Singular Points_
Applications: _Residues and Poles_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Residues, Zeros, and Poles]],[[Laurent Series]],[[Behavior of Functions Near Isolated Singular Points]]_
Cont.\_ of: _None_ 
_
_

We see in [[Residues, Zeros, and Poles]] and in [[Cauchy Residue Theorem]] that the theory of residues is based on the fact that we have a function $f$ that has an isolated singular point at some $z_{0}$, then $f(z)$ has the [[Laurent Series]]
$$
f(z) = \sum\limits _{n=0}^{\infty}a_{n}(z-z_{0})^{n} + \sum\limits_{n=1}^{\infty} \frac{b_{n}}{(z-z_{0})^{n}}
$$
in a punctured disk $0<|z-z_{0}|<R_{0}$. The portion of reciprocal terms with $b_{n}$ of the series is called the **principle part** of $f$ at $z$. We now use the principle part to identify the isolated singular point $z_{0}$ as one of three special types. This classification will aid us in the development of residue theory.

---
###### 1. Removable Singular Points
When every $b_{n}$ is zero, such that
$$
f(z) = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n} \quad (0<|z-z_{0}|<R_{0})
$$
then $z_{0}$ is known as a **Removable Singular Point**. Note that the residue at a removable singular point is _always_ $0$. If we define, or possibly redefine, $f$ at $z_{0}$ so that $f(z_{0})=a_{0}$, our expansion becomes valid throughout the entire disk $|z-z_{0}|<R_{0}$. Since a power series always represents an analytic function interior to its circle of convergence, it follows that $f$ is analytic at $z_{0}$ when it is assigned the value $a_{0}$ there. The singularity $z_{0}$ is, therefore, _removed_. 

---
###### 2. Essential Singular Points
If an infinite number of the coefficients $b_{n}$ in the principle part of the [[Laurent Series]] are nonzero, then $z_{0}$ is said to be an **essential singular point** of $f$

---
###### 3. Poles of Order m
If the principle part of $f$ at $z_{0}$ contains at least one nonzero term but the number of such term is only finite, then there exists a positive integer $m \ (m \geq 1)$ such that 
$$
b_{m}\neq 0 \quad \text{and} \quad b_{m+1}=b_{m+2}=\ldots=0
$$
That is, our Laurent Series expansion takes the form
$$
f(z) = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n}+ \frac{b_1}{z-z_{0}} + \frac{b_{2}}{(z-z_{0})^{2}} + \ldots + \frac{b_{m}}{(z-z_{0})^{m}} \quad (0<|z-z_{0}|<R_{0})
$$
In this case, the isolated singular point $z_{0}$ is called a **pole of order m**. A pole of order $m=1$ is typically referred to as a **simple pole**. 

---
##### Example 1.
The point $z_{0}=0$ is a removable singular point of the function 
$$
f(z) = \frac{1-\cosh z}{z^{2}}
$$
because 
$$
f(z) = \frac{1}{z^{2}}\left[1- \left(1+ \frac{z^{2}}{2!} + \frac{z^{4}}{4!}+\ldots\right)\right] = \frac{-1}{2!} - \frac{z^{2}}{4!} - \frac{z^{4}}{6!} -\ldots \quad (0<|z|<\infty)
$$
When the value $f(0)=\frac{-1}{2}$ is assigned, $f$ becomes entire. 


##### Example 2. 
We recall that 
$$
e^{\frac{1}{z}}= \sum\limits_{n=0}^{\infty} \frac{1}{n!} \frac{1}{z^{n}} = 1 + \frac{1}{1!} \cdot \frac{1}{z} + \frac{1}{2!} \cdot \frac{1}{z^{2}} +\ldots \quad (0<|z|<\infty) 
$$
and it follows that $e^\frac{1}{z}$ has an essential singularity at $z_{0}=0$, where the residue $b_{1}$ is unity. 

**Remark.**  This example can be used to illustrate an important result known as **Picard's Theorem**. It concerns the behavior of a function near an essential singular point.

```ad-Definition
**Picard's Theorem** states that in _each neighborhood of an essential singular point_, a function assumes every finite value, with one possible exception, an infinite number of times.
```

It is easy to see, for instance, that $e^\frac{1}{z}$ assumes the value of $-1$ an infinite number of times in each neighborhood of the origin. More precisely, since $e^{z}=-1$ when 
$$
z=(2n+1)\pi i \quad (n=0,\pm 1,\pm 2, \ldots)
$$
it follows that $e^{\frac{1}{z}} =-1$ when 
$$
z=\frac{1}{(2n+1) \pi i } = \frac{-i}{(2n+1)\pi} \quad (n=0,\pm 1,\pm 2,\ldots,)
$$
So if $n$ is large enough, an infinite number of such points lie in any given $\epsilon$ neighborhood of the origin. Zero is evidently the exceptional value when Picard's theorem is applied to $e^\frac{1}{z}$ at the origin. 

##### Example 3.
From the representation 
$$
f(z) = \frac{1}{z^{2}(1-z)} = \frac{1}{z^{2}}(1+z+z^{2}+\ldots) = \frac{1}{z^{2}} + \frac{1}{z} + 1 + z + z^{2}+\ldots \quad (0<|z|<1)
$$
one can see that $f$ has a pole of order $m=2$ at the origin and that 
$$
Res_{z=0} \ f(z) = 1.
$$
From the limit 
$$
\lim_{z\rightarrow 0} \frac{1}{f(z)} = \lim_{z\rightarrow 0} [z^{2}(1-z)] = 0
$$
it follows from [[Complex Limits#Limits Involving the Point at Infinity]] that
$$
\lim_{z \rightarrow 0} f(z) = \infty 
$$
Such a limit _always_ occurs at a pole. 

##### Example 4. 
Finally, we observe that the function
$$
f(z) = \frac{z^{2}+z-2}{z+1} = \frac{z(z+1)-2}{z+1} = z - \frac{2}{z+1} = -1+ (z+1) - \frac{2}{z+1} \quad (0<|z+1|<\infty)
$$
has a simple pole at $z_{0}=-1$. The residue there is $-2$. Moreover, we also see that 
$$
\lim_{z\rightarrow -1} \frac{1}{f(z)} = 0,
$$
such that
$$
\lim_{z\rightarrow -1} f(z) = \infty
$$
as before in [[#Example 3.]]

---

