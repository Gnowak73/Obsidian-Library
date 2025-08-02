---
tags: Fourier_Series, Math, Linear_Algebram Inner_Product
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Functional Linear Algebra_
Applications: _QM, ODEs, mechanical systems_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]] _
Closely\_Related\_To: _[[Vector Linear Algebra]]_
_
_

An extension of [[Vector Linear Algebra]] to infinite dimensions. 

An N-dimensional vector $\pmb{x} = (x_{1},x_{2},\ldots,x_N)$ is an object with N components. A <mark style="background: #ABF7F7A6;">sequence</mark> $\{a_n\}_{n=1}^{\infty}$ can be viewed as an "infinite-dimensional vector" with a countable number of components. We can then think of a <mark style="background: #FFF3A3A6;">function</mark> $f(x)$ as an infinite-dimensional vector with a <mark style="background: #ADCCFFA6;">continuum</mark> of components, where the output value of $f(x)$ is the component of $f$ corresponding to the "index" $x$. 

---
### Inner Product (Real Euclidean Space)
The inner-product traditionally is multiplying the respective components of two vectors and added them. Similarly, we now would define an infinite sum over all indices for these two functions, say $f$ and $g$, now we define
$$
\boxed{(f,g) \equiv \int\limits_{a}^{b}f(x)g(x) \ dx}
$$
#### Length of Functions
With the notion of vector length, we define 
$$
||f||^{2}\equiv (f,f) = \int\limits_{a}^{b}f^{2}(x) \ dx
$$
#### Orthogonality of Functions
We now can define orthogonality by 
$$
(f,g) = 0
$$
#### Projections and angles
The inner product can also be used for the notion of angles and projection, we define the project in a similar fashion to traditional vector linear algebra once more:
$$
Proj_{g}f \equiv \frac{(f,g)}{||g||^{2}}g = (f,\hat g)\hat g
$$
#### Linear Transformations
Linear transformations can be called "operators" (just like in [[Operators]]) which can act on a space of vectors. Operators such as differentiation and integration are linear and can be seen as such operators too!  

An interesting operator we can define is $A \equiv \frac{d^{2}}{{dx^{2}}}$, which actually shows up when using [[Separation of Variables (PDE technique)]]  in an Eigenvalue Problem but with derivatives! 

#### Basis Algebra
As we did in [[Vector Linear Algebra#Basis Linear Algebra]], we can apply the same methods here!

If we have an orthogonal basis $\{X_n\}_{n=1}^{\infty}$, which spans the vector space, we should be able to write any function $\phi(x)$ as
$$
\phi(x) = \sum\limits_{n=1}^{\infty}A_{n}X_{n}(x)
$$
If we take the [[#Inner Product (Real Euclidean Space) |Inner Product]] with an arbitrary basis vector function $X_j$
$$
(\phi, X_{n}) = \left(\sum\limits_{i=1}^{\infty}A_{i}X_{i},X_{n}\right)=\sum\limits_{i=1}^{\infty}(A_iX_{i},X_{n}) =\sum\limits_{i=1}^{\infty}A_i(X_i,X_{n}) = A_n(X_n,X_n)
$$
Thus,
$$
\boxed{\frac{(\phi, X_{n})}{||X_{n}||^{2}} = A_{n}}
$$
Similar results can be used once more for non-orthogonal basis. One problem with this calculation does show up: can we just switch the integral and the sum like that? We are assuming that the integral of an infinite sum is the infinite sum of an integral. This is not always true (same with changing differentiation and summation), and examples can be seen in <mark style="background: #FFF3A3A6;">Section 11.6.1</mark> of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]]. An important theorem for this is also [[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember#Fubini Tonelli Theorem]].

Also, an important theorem to remember is Bessel's Inequality. And another way to prove completeness of a basis (or proving that the coefficients $A_{n}$ are uniquely determined, is that if
$$
\left<g, \phi_{j} \right> = 0
$$
for all $j$, then $g=0$. This holds if and only if each $A_{n}$ are uniquely determined and the basis is complete.

**Remark.**  If a function or vector cannot be written in terms as a projection onto a basis as expressed before then we say the basis is incomplete. If we can, though, then we say the basis is complete if and only if each $A_{n}$ is uniquely defined. If there exists more than one possible set of $A_{n}$, then the basis is overcomplete.

### Fourier Series
Since we know that $\{1,\{\sin(nx),\cos(nx)\}_{n=1}^{\infty}\}$ creates an orthogonal basis, thus we should be able to apply our knowledge form basis algebra for functions to the <mark style="background: #ABF7F7A6;">Sine and Cosine</mark> functions. Doing this results in what we call: the Fourier Series, which postulates that any function can be written as the linear combination of sine and cosines as their frequencies go to infinity. 

For a Fourier Series to converge, the function in question has to follow some conditions. The most simple proof is for $L^2$ functions. All of these can be seen in section 11 of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]]. Other methods can also be seen in [[Fourier Series Convergence Conditions]].

If our basis is of sines and cosines, we can write that a function which follows these convergence conditions can be written as:
$$
\phi(x) = \frac{1}{2}A_0+\sum\limits_{n=1}^{\infty}\left[A_{n} \cos\left(\frac{n\pi x}{l}\right)+B_{n}\sin\left( \frac{n\pi x}{l}\right)\right]
$$
where $A_n$ and $B_{n}$ can be determined by 
$$
\frac{(\phi, \cos(\frac{n \pi x}{l}))}{||\cos\left(\frac{n \pi x}{l}\right)||^{2}} = A_{n}
$$
The same is true for the Sine function part $B_{n}$.

---

### Complex Plane
#### Inner Product, Basis Algebra and Fourier Series
It is worth noting, that all previous calculations can be done on the complex plane with the caveat: the inner product is 
$$
(f,g) \equiv \int\limits f(x)g^{*}(x) \ dx 
$$
and we also assume that the [[#Fourier Series]] can have <mark style="background: #ABF7F7A6;">Complex Coefficients</mark>.

Let us apply similar methods to [[#Basis Algebra]].

If we have an orthogonal basis $\{X_n\}_{n=1}^{\infty}$, which spans the vector space, we should be able to write any function $\phi(x)$ as
$$
\phi(x) = \sum\limits_{n=1}^{\infty}c_{n}X_{n}(x)
$$
If we take the [[#Inner Product (Real Euclidean Space) |Inner Product]] with an arbitrary basis vector function $X_j$
$$
\begin{gathered}
(\phi, X_{m}) = \left(\sum\limits_{n=1}^{\infty}c_{n}X_{n}, X_{m}\right) = \sum\limits_{n=1}^{\infty}c^{*}_{n}(X_{n},X_{m}) \\
=c^{*}_{m}(X_{m},X_{m}) = c^{*}_{m}||X_{m}||^{2}, \quad \text{or} \\ \quad \boxed{c^{*}_{m}= \frac{(\phi,X_{m})}{||X_{m}||^{2}} = \frac{1}{||X_{m}||^{2 }}\int\limits \phi^{*}(x)X_{m} \ dx  }

\end{gathered} 
$$
where $\{X_{m}\}_{n=1}^{\infty}$ can still be the traditional Fourier basis: $\{1,\{\sin(nx),\cos(nx)\}_{n=1}^{\infty}\}$. We can take the complex conjugate of this equation to get:
$$
\boxed{c_{m}= \frac{\overline{(\phi,X_{m})}}{||X_{m}||^{2}} = \frac{1}{||X_{m}||^{2 }}\int\limits \phi(x)X^{*}_{m} \ dx  }

$$
Once again, we are assuming that the integral of an infinite sum is the infinite sum of an integral. This is not always true (same with changing differentiation and summation), and examples can be seen in <mark style="background: #FFF3A3A6;">Section 11.6.1</mark> of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]]. Also keep in mind [[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember#Fubini Tonelli Theorem]]

Once again, for Fourier Series to be used, we must have a function that will converge, so it has to follow some conditions. The most simple proof is for $L^2$ functions once again. All of these can be seen in section 11 of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]]. Other methods can also be seen in [[Fourier Series Convergence Conditions]].

It is worth noting that all wave functions have to be $L^{2}$ functions for normalization.

##### Symmetry of Complex Inner Product
The above result was obtained using the required axiom for the complex inner product:
$$
\overline{(x,y)} = (y,x)
$$
The conjugate is necessary because you want to define a norm $\|\cdot\|: V \to \Bbb R_{\geq 0}$ by using that inner product, putting
$$
\|x\| = \sqrt{\langle x,x\rangle},
$$
and for this you need $\langle x,x\rangle$ to be real. The conjugation gives $\langle x,x\rangle = \overline{\langle x,x\rangle} \in \Bbb R$. 

	It is also worth noting that for convergent series, the conjugate of the series is the series of the conjugates!

This does seem to bring about a question: [[Does the Complex Conjugate of an Integral Equal the Integral of the Conjugate...]]?

Well, we actually have the formulation that 
$$
\overline{\int\limits f(z)g(z) dz} = \int\limits \overline{f(z)g(z)} \ \overline{dz}
$$
Since we aren't working with complex variables as the input for these functions: we then have the result:
$$
\overline{\int\limits f(x)g(x)dx} = \int\limits \overline{f(x)g(x)} \ dx
$$
since $\overline{dx}=dx$. How does this apply to the inner product?  Well, it means that
$$
\boxed{\overline{(f,g)} = \overline{\int\limits f^{*}(x)g(x) \ dx} = \int\limits f(x)g^{*}(x) \ dx = (g,f)} 
$$
Thus, when working with [[The Wave Function|wave functions]] and inner products, we can use this!
