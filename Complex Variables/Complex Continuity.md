---
tags: Complex, math, continuity, limits, functions
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Continuity_
Applications: _Functional Analysis on the Complex Plane, Contour Integrals, Complex Derivatives_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Limits]],[[Complex Derivatives]]_
Cont.\_ of: _None_ 
_
_
```ad-Definition
A function $f$ is said to be _continuous_ at a point $z_{0}$ if
$$
\lim_{z\rightarrow z_{0}} f(z) = f(z_{0})
$$
This statement can be written more generally with the left and right hand [[Complex Limits|limits]]:
$$
\lim_{z\rightarrow z_{0}^{-}}f(z) = \lim_{z\rightarrow z_{0}^{+}}f(z) = f(z_{0})
$$

These limit definitions can be extended to the epsilon delta definitions in [[Complex Limits]].
```

A function of a complex variable is said to be continuous in a region $R$ is it is continuous at each point in $R$. If two functions are continuous at a point, their sum and product are also continuous at that point, and their quotient is too as long as the denominator isn't $0$. 

**Theorem 1.**  A composition of continuous functions is itself continuous 

**Theorem 2.**  If a function $f(z)$ is continuous and nonzero at a point $z_{0}$, then so are $u(x,y)$ and $v(x,y)$. Conversely, the same is true. 

**Theorem 3.**  If a function $f$ is continuous throughout a region $R$ that is both closed and bounded, there exists a nonnegative real number $M$ such that 
$$
|f(z)|\leq M \quad \text{for all points $z$ in $R$}
$$

**Theorem 4.**  If a function $f(z)$ is continuous and nonzero at a point $z_{0}$, then $f(z)\neq0$ throughout some neighborhood of that point. 
