---
tags: series, Math, convergence, divergence, tests
dg-publish: true
mathLink: 
---
Subject: _Real Analysis_
Main\_Topic: _Real Series Convergence Tests_
Applications: _Convergence and Divergence of Series_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Complex Series]], [[Cauchy Criterion]],[[Uniform and Pointwise Convergence]]_
Cont.\_ of: _None_ 
_
_

##### Uniform and Pointwise Convergence
See [[Uniform and Pointwise Convergence]]. Proof of the rate of convergence. It allows us to know whether or not we can do things like differentiate term-by-term or use a [[Function Linear Algebra#Fourier Series|Fourier Series]] to represent a function on an interval and so on ([[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember]]). 

---
##### Cauchy Criterion
See [[Cauchy Criterion]]. Similar to epsilon delta limit proof. Proof of convergence for series without using the idea of a limit. 

---
##### Absolute Convergence
**Theorem.**  If a series is absolute convergence, then so is its regular series.

**Proof:**  First notice that $\left| {{a_n}}\right|$ is either ${a_n}$ or it is $- {a_n}$ depending on its sign. This means that we can then say,
$$
0 \le {a_n} + \left| {{a_n}} \right| \le 2\left| {{a_n}} \right|
$$
Now, since we are assuming that $\sum {\left| {{a_n}} \right|}$ is convergent then $\sum {2\left| {{a_n}} \right|}$ is also convergent since we can just factor the 2 out of the series and 2 times a finite value will still be finite. This however allows us to use the Comparison Test to say that $$\sum \left({{a_n} + \left| {{a_n}}\right|}\right)$$ is also a convergent series. Finally, we can write,

$$\sum {{a_n}} = \sum \left({{a_n} + \left| {{a_n}} \right|}\right) -\sum {\left| {{a_n}} \right|}
$$
and so $$\sum {{a_n}}$$ is the difference of two convergent series and so is also convergent.

**Remark.**  Another method to proving this is that we can use the [[Triangle Inequality (Euclidean Geometry)]] and [[Cauchy Criterion]].

---
##### Divergence Test
**Test:**  For any series 
$$
\sum\limits_{n=1}^{\infty}a_{n},
$$
evaluate $\lim_{n \rightarrow \infty} a_{n}$. 

**Conclusion:**  If $\lim_{n \rightarrow \infty} a_{n}=0$, the test is inconclusive. If $\lim_{n \rightarrow \infty} a_{n}\neq 0$, the series diverges.

---
##### Geometric Series
**Test:**  We have the series 
$$
\sum\limits_{n=1}^{\infty}a r^{n-1},
$$

**Conclusion:**  If $|r|<1$, the series converges to $\frac{a_{1}}{1-r}$. If $|r| \geq 1$, the series diverges. 

**Comments:**  Any geometric series can be reindexed to be in the form shown above where $a$ is the initial term and $r$ is the ratio.

---
##### P-Series
**Test:**  We have the series
$$
\sum\limits_{n=1}^{\infty} \frac{1}{n^{p}}
$$
**Conclusion:**  If $p>1$, the series converges. If $p<1$, the series diverges. 

**Comments:**  For $p=1$, we have the harmonic series. 

---
##### Comparison Test
**Test:**  We have the series 
$$
\sum\limits_{n=1}^{\infty} a_{n}
$$
with **nonnegative terms**, and we compare this series with a known series 
$$
\sum\limits_{n=1}^{\infty}b_{n}.
$$
**Conclusion:**  If $a_{n} \leq b_{n}$ for all $n\geq N$ and $\sum\limits_{n=1}^{\infty} b_{n}$ converges, the so does $\sum\limits_{n=1}^{\infty} a_{n}$.  If $a_{n}\geq b_{n}$ for all $n\geq N$ and $\sum\limits_{n=1}^{\infty} b_{n}$ diverges, then so does $\sum\limits_{n=1}^{\infty} a_{n}$. 

**Comments:**  Typically used for a series similar to a geometric or p-series. It can sometimes be difficult to find an appropriate series. 

---
##### Limit Comparison Test
**Test:**  For the series 
$$
\sum\limits_{n=1}^{\infty} a_{n}
$$
with **positive terms**, compare with a series 
$$
\sum\limits_{n=1}^{\infty} b_{n}
$$
by evaluating 
$$
L = \lim_{n \rightarrow \infty } \frac{a_{n}}{b_{n}}
$$
**Conclusion:**  If $L=0$, and $\sum\limits_{n=1}^{\infty} b_{n}$ converges, then $\sum\limits_{n=1}^{\infty} a_{n}$ also converges. If $L=\infty$ and $\sum\limits_{n=1}^{\infty} b_{n}$ diverges, then $\sum\limits_{n=1}^{\infty} a_{n}$ diverges.

**Comments:**  Typically used for a series similar to geometric or p-series. Often easier to apply than the comparison test. 

---
##### Integral Test
**Test:**  If there exists a **positive, continuous, decreasing** function $f$ such that $a_{n}=f(n)$ for all $n \geq N$, evaluate 
$$
\int\limits_{N}^{\infty} f(x) \ dx
$$
**Conclusion:**  The integral $\int\limits_{N}^{\infty} f(x) \ dx$ and the series $\sum\limits_{n=1}^{\infty} a_{n}$ either **both** converge or **both** diverge. 

**Comments:** Limited to series for functions that can easily be integrated.

---
##### Alternating Series Test
**Test:**  We have the series 
$$
\sum\limits_{n=1}^{\infty} (-1)^{n+1} b_{n}
$$
or 
$$
\sum\limits_{n=1}^{\infty} (-1)^{n}b_{n}
$$
**Conclusion:**  If $b_{n+1}\leq b_{n}$ for all $n\geq 1$ and $b_{n}\rightarrow 0$, then the series converges.

**Comment:**  Only applies to alternating series. 

---
##### Ratio Test
**Test:**  For any series 
$$
\sum\limits_{n=1}^{\infty} a_{n}
$$
with **nonzero** terms, let
$$
\rho=\lim_{n\rightarrow \infty} \left| \frac{a_{n+1}}{a_{n}}\right|
$$
**Conclusion:** If $0\leq \rho < 1$, the series converges absolutely. If $\rho>1$ or $\rho=\infty$, the series diverges. If $\rho=1$, the test is inconclusive.

**Comments:**  Often used for series involving factorials or exponentials. 

---
##### Root Test
**Test:**  For any series 
$$
\sum\limits_{n=1}^{\infty} a_{n}
$$
let 
$$
\rho=\lim_{n \rightarrow \infty} \sqrt[n]{|a_{n}|}.
$$
**Conclusion:**  If $0\leq \rho < 1$, the series converges absolutely. If $\rho>1$ or $\rho=\infty$, the series diverges. If $\rho=1$, the test is inconclusive.

**Comments:**  Often used for series where $|a_{n}|=b_{n}^{n}$. 