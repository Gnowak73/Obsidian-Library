---
tags: Math, D'Alambert, theorem, PDE, technique
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _Duhamel's Principle_
Applications: _Solving PDEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]_
Closely\_Related\_To: _[[Variation of Parameters]]_
_
_

Duhamel's principle shows how we can solve PDEs with a source involved, and is used to solve inhomogeneous linear PDEs with a time evolution involved. It is also akin to a generalization from [[Variation of Parameters]], a pretty interesting result.

Let us say our PDE is the [[Wave Equation D'Alambert|Wave Equation]] 
$$
\cases{u_{tt}-c^{2}u_{xx}=f(x,t), \quad -\infty<x<\infty, \ t>0,\\
u(x,0) = 0, \quad -\infty<x<\infty, \\
u_{t}(x,0)=0, \quad -\infty<x<\infty.}
$$
Now, Duhamel states that if we introduce an additional temporal parameter $s \in [0,\infty]$. For each <mark style="background: #FFB8EBA6;">fixed</mark>  $s$, we consider an indexed solution $\omega(x, t;s)$ to
$$
\cases{\omega_{tt}(x,t;s) = c^{2} \omega_{xx}(x,t;s), \quad -\infty<x<\infty, \ t>s, \\
\omega(x,s;s)=0,\quad -\infty<x<\infty \\
\omega_{t}(x,s;t)=f(x,s), \quad -\infty<x<\infty}
$$
Now, the solution will be:
$$
\boxed{u(x,t) = \int\limits_{0}^{t}\omega(x,t;s) \ ds}
$$
We add this solution to the homogenous one to get our final answer now.

To adapt this to other PDEs, remember that the source function is placed wherever the time derivative one less than the highest time derivative in the equation shows up.

```ad-warning
This solution from Duhamel's Principle does **NOT** account for superposition and acts like a particular solution from ODEs. This particular solution **MUST** be added to the homogeneous [[Wave Equation D'Alambert|D'Alambert Solution]] for the general solution!
```