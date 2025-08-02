---
tags: Math, theorem, Multivariable, Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Leibniz Integral Rule_
Applications: _[[Feynman Integration]], PDEs, Multivariable Calculus_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
This rule is for differentiation under the integral sign. It states that 

**Theorem.**  Let $f(x,t)$ be a function such that both $f(x,t)$ **and** its partial derivative $f_{x}(x,t)$ are _continuous_ in $t$ and $x$ in _some region_ of the $xt$-plane, including $a(x)\leq t\leq b(x), x_{0}\leq x\leq x_{1}$. Also suppose that the function $a(x)$ and $b(x)$ are both continuous and both have continuous derivatives for $x_{0}\leq x \leq x_{1}$. Then, for $x_{0}\leq x \leq x_{1},$
$$
\frac{d}{dx}\left(\int\limits_{a(x)}^{b(x)} f(x,t)dt\right) =f(x,b(x)) \ \frac{d}{dx}b(x) - f(x,a(x)) \ \frac{d}{dx}a(x) + \int\limits_{a(x)}^{b(x)}  \frac{\partial}{\partial x}f(x,t) \ dt
$$
This is commonly used in multivariable calculus and to evaluate integrals in PDE. 