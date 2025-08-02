---
tags: Math, Integrals, technique
dg-publish: true
mathLink: 
---
Subject: _Integrals_
Main\_Topic: _Integration Methods_
Applications: _Integration Techniques_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
This article will summarize the methods for solving integrals, not including [[Line Integrals]] or [[Contour Integrals]], since those pages already have all of their theorems already. 

```ad-Remember
don't forget [[Leibniz Integral Rule]]
```

##### General Univariate Methods
1. U-Substitution
2. Partial Fractal Decomposition
3. Trig Substitution (especially for integrals with radicals)
4. [[integration by parts]] to separate up an integral (useful to write integral in different variable terms or when a function goes to $0$ at a specific bounds.
5. [[Feynman Integration]] 
6. [[Laplace Transforms]] ([[Solving Improper Integrals with Laplace Transforms]])
7. Odd/Even Functions
8. Kings Property: $\int\limits_{a}^{b}f(x) \ dx = \int\limits_{a}^{b}f(a+b-x) \ dx$. 
9. Kings Property 2: $\int\limits_{a}^{b}f(x) \ dx = \frac{1}{2}\int\limits_{a}^{b}f(x)+f(x) \ dx = \frac{1}{2}\int\limits_{a}^{b} f(x)+f(a+b-x) \ dx$ 
10. Inversions: Suppose a function has a bounded antiderivative on $[0,\infty]$, then substitute $u\rightarrow \frac{1}{x}$: $\int\limits_{0}^{\infty}f(x) \ dx =\int\limits_{\infty}^{0}\frac{f(\frac{1}{x})}{-x^{2}} \ dx = \int\limits_{0}^{\infty}\frac{f\left(\frac{1}{x}\right)}{x^{2}} \ dx$
11. Inversions 2: Suppose we do the same thing as in Kings Property 2, $\int\limits_{0}^{\infty}f(x) \ dx = \frac{1}{2}\int\limits_{0}^{\infty}f(x) +f(x) \ dx = \frac{1}{2}\int\limits_{0}^{\infty}f(x)+\frac{f(\frac{1}{x})}{x^{2}} \ dx$
12. Weierstrass Substitution: $t\rightarrow \tan(\frac{\theta}{2})$, use trig manipulation to substitute values of $\sin$ and $\cos$ to transform trig integral into rational function 
13. [[Taylor Series]]
14. Changing to Double Integral
15. Harmonic Functions (typically used for exponential and trig integrals): if we have a multivariable [[Harmonic Functions|harmonic function]] ($\frac{\partial^{2}}{\partial x^{2}}f+ \frac{\partial^{2}}{\partial y^{2}}f = 0$), and $(a,b)$ is a point on the plane, then $\int\limits_{0}^{2\pi}f(a+r\cos \theta,b+r\sin \theta) \ d\theta = 2\pi f(a,b)$ 
16. [[Changing Indefinite Integral into a Definite One]]
17. [[Application of Residues]] (for difficult improper integrals, best if they are even functions or one sided improper integrals so the Cauchy principle value equals the regular improper integral). Also for definite trig integrals with $\sin$ and $\cos$ going from $0$ to $2 \pi$. Real definite integrals can also be done, but may be a bit harder to do than these other methods listed. 

##### More Multivariate Methods
1. [[Leibniz Integral Rule]] 
2. Separating one integral into two, like in [[Gaussian Integral]]
3. Change of coordinates, [[Jacobian]]
4. Switching order of Integration: [[Fubini's theorem]]