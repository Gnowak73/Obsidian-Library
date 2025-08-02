---
tags: convergence, Math, series, pointwise, uniform
dg-publish: true
mathLink: 
---
Subject: _Real Analysis_
Main\_Topic: _Uniform and Pointwise Convergence_
Applications: _Fourier Series, Differentiation, Integration theorems and so on_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Cauchy Criterion]],[[Real Series Convergence Tests]],[[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember]]_
Cont.\_ of: _None_ 
_
_

```ad-Definition
For the convergence of a sequence of function on a domain $D$,
$$
|f_{n}(x) - f(x)| < \epsilon \quad \text{whenever} \quad n>N
$$

---
**Pointwise Convergence**
If, $\forall \epsilon>0, \forall x \in D, \exists N \in Z^{+}$ such that $\forall n>N$,
$$
|f_{n}(x) - f(x)| < \epsilon
$$

Note that $N$ can depend on $x$ and $\epsilon$, so there are different rates of convergence depending on where you are in the domain $D$.

---
**Uniform Convergence**
If, $\forall \epsilon>0, \exists N \in Z^{+}$ such that $\forall n>N$, $\forall x \in D$,
$$
|f_{n}(x) - f(x)| < \epsilon
$$

When the choice of $N$ depends only on the value of $\epsilon$ and is independent of the point $x$ taken, the convergence is said to be **Uniform** in that region since there is a uniform rate of convergence on the domain.
```
