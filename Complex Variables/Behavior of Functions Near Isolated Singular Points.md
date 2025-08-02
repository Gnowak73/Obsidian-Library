---
tags: Math, Complex, singularities, zeros, analytic, isolated, isolated_singular_points, residues, poles, functions,
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Behavior of Functions Near Isolated Singular Points_
Applications: _Function Behaviors on the Complex Plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Functions and Mappings]],[[Residues, Zeros, and Poles]],[[Three Types of Isolated Singular Points]]_
Cont.\_ of: _None_ 
_
_

For the sake of brevity, only the theorems will be here, all proofs can be found in <mark style="background: #BBFABBA6;">Section 84</mark> of [[Complex Variables Textbook.pdf]]. 

The behavior of a function $f$ near an isolated singular point $z_{0}$ varies, depending on whether $z_{0}$ is a removable singular point, and essential singular point, or a pole of some order $m$. In this section, we describe some of that behavior. 

---
#### Removable Singular Points
**Theorem 1.**  If $z_{0}$ is a removable singular point of a function $f$, then $f$ is bounded and analytic in some deleted neighborhood $0<|z-z_{0}|<\epsilon$ of $z_{0}$.

**Theorem 2.**  Suppose that a function $f$ is bounded and analytic in some deleted neighborhood $0<|z-z_{0}|<\epsilon$ of $z_{0}$. If $f$ is not analytic at $z_{0}$, then it has a removable singularity there. 

**Remark.**  Theorem 2 is often referred to as _Riemann's theorem_. 

---
#### Essential Singular Points

**Theorem 3.**  Suppose that $z_{0}$ is an essential singularity of a function $f$, and let $w_{0}$ be any complex number. Then, for any positive number $\epsilon$, the inequality 
$$
|f(z)-w_{0}|<\epsilon
$$
is satisfied at some point  $z$ in each deleted neighborhood $0<,|z-z_{0}|<\delta$ of $z_{0}$. 

**Remark.**  This is often referred to as the _Casorati-Weierstrass theorem_. 

---
#### Poles of Order m
**Theorem 4.**  If $z_{0}$ is a pole of a function $f$, then 
$$
\lim_{z\rightarrow z_{0}} f(z) = \infty.
$$


