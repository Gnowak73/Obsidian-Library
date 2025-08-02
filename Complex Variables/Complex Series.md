---
tags: Math, Complex, Analytic, series, taylor, taylor_series, infinite_series, sum, limit 
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Series_
Applications: _Analytic Functions, Contour Integrals_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Taylor Series]]_
Cont.\_ of: _None_ 
_
_

##### Important Formulations
1. [[Taylor Series]]: writing analytic functions in terms of a power series in open disk domain
2. [[Laurent Series]]: writing analytic functions in terms of power series in annulus domain
3. [[Properties of Complex Series]]: Notes on the properties of Complex Series such as term-by-term differentiation, convergence, etc.
4. [[Uniqueness of Series Representations]]: Notes of the uniqueness of Taylor and Laurent series. 
5. [[Multiplication and Division of Power Series]] 


#### Convergence of Sequences
```ad-Definition
An infinite _sequence_ $z_{1},z_{2},\ldots z_{n}$  of complex numbers has a _limit_ of $z$ if, for each positive number $\epsilon$, there exists a positive integer $n_{0}$ such that
$$
|z_{n}-z|<\epsilon \quad \text{whenever} \quad n>n_{0}
$$
```

Geometrically this means that for sufficiently large values of $n$, the points $z_{n}$ lie in any given $\epsilon$ neighborhood of $z$. Since we can choose $\epsilon$ as small as we please, it follows that the points $z_{n}$ become arbitrarily close to $z$ as their subscripts increase. Note that the value of $n_{0}$ that is needed will, in general, depend on the value of $\epsilon$. 

A sequence can have at most one limit. That is, a limit $z$ is unique if it exists. When this limit $z$ exists, the sequence is said to _converge_ to $z$
$$
\lim_{n \rightarrow \infty} z_{n} = z.
$$
If a sequence has no limit, it _diverges_. 

---
**Theorem.**  Suppose that $z_{n}=x_{n}+iy_{n} \ (n=1,2,\ldots)$ and $z=x+iy$. Then
$$
\lim_{n \rightarrow \infty} z_{n} = z
$$
if and only if 
$$
\lim_{n \rightarrow \infty} x_{n}=x \quad \text{and} \quad \lim_{n\rightarrow \infty}y_{n}=y
$$

**Remark.**  Basically, we can separate a limit just like we do in real Calculus. The proof is based off of looking at the definition of a converging sequence. The proof an be seen in <mark style="background: #BBFABBA6;">Ch. 5, Sec. 60</mark> of [[Complex Variables Textbook.pdf]]. 

###### Example 1.
If we have the sequence
$$
z_{n}=-1+i \frac{(-1)^{n}}{n^{2}}
$$
we can take the limit 
$$
\lim_{n\rightarrow \infty} z_{n}=-1+0 =\boxed{-1}
$$
We can also use the convergence definition to get
$$
|z_{n}-(-1)| = \left|i \frac{(-1)^{n}}{n^{2}}\right| = \frac{1}{n^{2}}<\epsilon \quad \text{whenever} \quad n>\frac{1}{\sqrt{\epsilon}}
$$

**Remark.**  One must be careful when adapting our theorem to polar coordinates due to the periodicity of the argument $\theta$. Remember though, that the limit of the argument is found using $\arctan$ for the angle of the polar coordinate.

### Convergence of Series
An infinite _series_
$$
\sum\limits_{n=1}^{\infty}z_{n}=z_{1}+z_{2}+z_{3}+\ldots+z_{n}+\ldots
$$
of complex numbers _converges_ to the _sum_ $S$ if the sequence
$$
S_{N}=\sum\limits _{n=1}^{N}z_{n}=z_{1}+z_{2}+z_{3}+\ldots+z_{n} \quad (N=1,2,\ldots)
$$
of **partial sums** converges to $S$; we then write
$$
\sum\limits_{n=1}^{\infty} z_{n}=S.
$$
Note that since a sequence can have at most one limit, a series can have at most one sum. When a series **does not converge**, we say that it _diverges_. 

---
**Theorem.**  Suppose that $z_{n}=x_{n}+iy_{n} \ (n=1,2,\ldots)$ and $S=X+iY$. Then
$$
\sum\limits_{n=1}^{\infty}z_{n}=S
$$
if and only if 
$$
\sum\limits_{n=1}^{\infty}x_{n}=X \quad \text{and} \quad \sum\limits_{n=1}^{\infty}y_{n}=Y
$$

This theorem tells us that one can write
$$
\sum\limits_{n=1}^{\infty}(x_{n}+iy_{n}) = \sum\limits_{n=1}^{\infty}x_{n}+i\sum\limits_{n=1}^{\infty}y_{n}
$$
whenever it is known that the two series on the right converge or that the one on the left does. The proof of this theorem follow from the limits of the partial sum and can be seen in <mark style="background: #FF5582A6;">Sec. 61. Ch. 5</mark> of [[Complex Variables Textbook.pdf]].

---
#### Two Important Corollary's
**Corollary 1.**  If a series of complex number converges, the $nth$ term converges to zero as $n$ tends to infinity. 

The proof of this corollary can be seen from traditional Calculus about how the $nth$ term of a convergent series approaches 0.

It follows from this corollary that the terms of convergent series are _bounded_. That is, when a series converges, there exists a positive constant $M$ such that $|z_{n}|\leq M$ for each positive integer $n$.

For another important property of series of complex numbers that follows from Calculus, is **absolute convergence**.

```ad-Definition
An **Absolutely Convergent** series is a series in which 
$$
\sum\limits_{n=1}^{\infty}|z_{n}|= \sum\limits_{n=1}^{\infty}\sqrt{x_{n}^{2}+y_{n}^{2}}
$$
also converges.
```

**Corollary 2.**  The absolute convergence of a series of complex numbers implies the convergence of that series. 

**Proof:**  Let us assume that a series converges absolutely. Since 
$$
|x_{n}| \leq |z_{n}| = \sqrt{x_{n}^{2}+y_{n}^{2}} \quad \text{and} \quad |y_{n}| \leq |z_{n}| = \sqrt{x_{n}^{2}+y_{n}^{2}},
$$
we know from the [[Real Series Convergence Tests#Comparison Test|Comparison Test]] in calculus that the two series 
$$
\sum\limits_{n=1}^{\infty} |x_{n}| \quad \text{and} \quad \sum\limits_{n=1}^{\infty}|y_{n}|
$$
must converge. Moreover, $x_{n}$ and $y_{n}$ are real numbers. And since the absolute value of a series of _real_ numbers implies the convergence of the series itself (see either: [[Real Series Convergence Tests#Absolute Convergence|Absolute Convergence]] or [[Cauchy Criterion]]) it follows that 
$$
\sum\limits_{n=1}^{\infty}x_{n}\quad \text{and}\quad  \sum\limits_{n=1}^{\infty}y_{n}
$$
must also converge. 

---
#### Remainders
In establishing the fact that the sum of a series is a given number $S$, it is often convenient to define the _Remainder_ $\rho_{N}$ and $N$ terms, using the partial sums:
$$
\rho_{N}\equiv S-S_{N}
$$
Thus, $S=S_{N}+\rho_{N}$; and since $|S_{N}-S|=|\rho_{N}-0|$, we see that a series converges to a number $S$ **if and only if the sequence of remainders tends to zero**. This will become very important in our treatment of <mark style="background: #FFB86CA6;">power series</mark> of the form
$$
\sum\limits_{n=o}^{\infty}a_{n}(z-z_{0})^{n} = a_{0}+a_{1}(z-z_{0})+\ldots+a_{n}(z-z_{0})^{n}+\ldots
$$

##### Example
With the aid of remainders, we can take the series (same as the one from [[Complex Numbers Algebraic Properties#Lagrange's Trigonometric Identity|Lagranges Trig Identity]]: 
$$
1+z+z^{2}+\ldots +z^{n}= \frac{1-z^{n+1}}{1-z}
$$
to write the partial sums 
$$
S_{N}= \sum\limits_{n=0}^{N-1}z^{n} = 1+z+z^{2}+\ldots+z^{N-1}
$$
as
$$
S_{N}= \frac{1-z^{N}}{1-z}
$$
If we have 
$$
S = \frac{1}{1-z}
$$
then we can write the remainder as 
$$
\rho_{N}=S(z)-S_{N}(z) = \frac{z^{N}}{1-z} \quad (z\neq 1)
$$
Thus, 
$$
|\rho_{N (z)}|= \frac{|z|^{N}}{|1-z|}
$$
If we are to take the limit of this sum, we see that the remainder converges to $0$ when $|z|<1$ but does not when $|z|\geq 1$. Thus, we can state that 
$$
\boxed{\sum\limits_{n=0}^{\infty}z^{n} = \frac{1}{1-z} \quad (|z|<1)}
$$





