---
tags: theorem, Math, Complex_Analysis, Inner_Product, Fourier_Series, Integrals, Series, questions,
dg-publish: true
mathLink: 
---
Subject: _Important Theorems for Series, Integrals, and Fourier Series_
Main\_Topic: _List of Theorems_
Applications: _Manipulation of Series, Integrals, and Fourier Series to solve equations_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Uniform and Pointwise Convergence]]_
_
_

Absolute Convergence allows us to do A LOT: change integration, change summation, differentiate by series, integrate by series, etc. 

---
#### 1. Conjugate of Complex Series is the Series of the Conjugates 
If a series converges, then 
$$
\overline{\sum\limits_{k=1}^{\infty}z_{k}} = \sum\limits_{k=1}^{\infty}\overline{z_{k}} 
$$

---
#### 2. Complex Conjugate of Integral is Integral of Complex Conjugate and differential
$$
\overline{\int\limits f(z) dz} = \int\limits {\overline{f(z)}} \ \overline{dz}
$$
and $f(z)$ can be the product of any other functions. 

---
#### $L^{2}$ Functions' Fourier Series Converges
If we have an $L^{2}$ function (which is specifically notable because of wave function normalization condition), its [[Function Linear Algebra|Fourier Series]] converges.  Other convergence theorems these can be seen in section 11 of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]] and in [[Fourier Series Convergence Conditions]]. 

---
#### Switching Integration and Summation
Some theorems can be seen in section 11.6+ of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE textbook]], other than that the main important one is below. We can also know that pointwise convergence, and thus uniform convergence, allows this to happen.

##### Fubini Tonelli Theorem for Integrals and Series
This theorem is a statement about [[Fubini's theorem]] except generalized to include series. In other words, if $\int\limits \sum\limits |f_{n}| < \infty$ or if $\sum\limits \int\limits |f_{n}| < \infty$ (by Tonelli these two conditions are equivalent), so then
$$
\int\limits \sum\limits f_{n} = \sum\limits \int\limits f_{n} 
$$
---
#### Switching Summation and Differentiation
If the Series $\sum\limits f'_{n}$ converges [[Uniform and Pointwise Convergence|uniformally]], then yes the derivative of an infinite series is the series of differentiated terms. Uniform Convergence can easily be proven using M-weirstrass Theorem ([[Uniform and Pointwise Convergence]]). Once, again, more can be seen in [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE textbook]]. We can always switch a finite summation and differentiation. 

---
#### Switching Limit and Differentiation
If you have a sequence of functions that are differentiable, and converge [[Uniform and Pointwise Convergence|pointwise]] for some point $x_{0}$, and if their derivatives converge uniformly, say on a given interval $[a,b]$, supposing they are real valued functions, then the sequence of functions is uniformly convergence to $f$ and 
$$
\lim_{n \rightarrow \infty} \frac{\partial f_{n}(x)}{\partial x} = \frac{\partial f(x)}{\partial x}
$$

---
#### Bessel's Inequality 
Let $\phi \in L^{2}(a,b)$ and suppose that $\{X_{n}(x)\}$ is an orthogonal family of functions on $(a,b)$ and we define 
$$
A_{n} \equiv \frac{(\phi,X_n)}{||X_{n}|^{2}},
$$
then
$$
\sum\limits_{n=1}^{\infty}A^{2}_{n}\int\limits_{a}^{b}|X_{n}(x)|^{2} \ dx \leq \int\limits_{a}^{b}|\phi(x)|^{2} \ dx.
$$
If this inequality is an Equality (known as Parseval's equality, see [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE textbook]]) then we can say there is $L^{2}$ convergence resulting in convergence of the series 
$$
\sum\limits_{n=1}^{\infty}A_{n}X_{n}
$$
Bessel's Inequality comes from defining an error function which results in such an inequality. And thus if our function $\phi(x)$ is $L^{2}$, then the left-hand side would also converge and the error function would converge, resulting in our Fourier Series (or whatever orthogonal family we use) to exactly converge to our function.

**Remark.**  Parseval's Equality proves that a basis is complete. 

---
#### Multiplying Two Infinite Series(Mertens' Theorem)
We can have three series (either real or complex)
$$
\sum\limits a_{n} \sum\limits b_{n}= \sum\limits c_{n}
$$
if either all of these summations converge, OR at least $\sum\limits a_{n}$ or $\sum\limits b_{n}$ converges absolutely but both of them converge at bare minimum. In other words, if both series converge and one of them uniformly converges. If both series converge uniformly, so does their product. (Remember: if these two series are independent of each other, make them have different indexes when multiplying them conventionally). Also, this is **only** for the **Cauchy Product**, but also note that this same principle works if we don't consider the cauchy product since the result will be the same. In other words, if there is another way to write the infinite sum, not as a couchy product, this will still hold. 

**Theorem.**  Let $(a_n)_n$ and $(b_n)_{n}$ be real or complex sequences. It was proved by Franz Mertens that, if the series $\sum_{n=0}^\infty a_n$ converges to $A$ and $\sum_{n=0}^\infty b_n$ converges to $B$, _and at least one of them converges absolutely_, then their Cauchy product converges to $AB$.

It is not sufficient for both series to be convergent; if both sequences are conditionally convergent, the Cauchy product does not have to converge towards the product of the two series [...]

---
#### Proof that Fourier Series Converges for Piecewise Continuity(Dirichlet's Theorem)
This theorem is proof that a piecewise continuous function is enough to prove a function's [[Function Linear Algebra|Fourier Series]] will converge. See [[Dirichlet's theorem]]. 

---
#### Fourier and Laplace (most integral transforms) Require $L^{1}$
Most integral transforms require that there the function being transformed in an $L^{1}$ function, do not blindly apply integral transforms! Or any transforms of such matters!