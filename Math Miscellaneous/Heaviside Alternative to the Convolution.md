---
tags: Math, Integrals, Fourier_Transform, Laplace_Transform, theorem, derivation, technique  
dg-publish: true
mathLink: 
---
Subject: _Operator Calculus_
Main\_Topic: _Heaviside Alternative to the Convolution_
Applications: _Solving Convolution Integrals, [[Laplace Transforms]]_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
If we take the [[Fourier Transform#Convolution|convolution]]/[[Laplace Transforms#Convolution|convolution]]:
$$
(f*g)=\int\limits_{-\infty}^{\infty}f(y)g(x-y)dy
$$
we can use the [[Exponential Shift Operator]] to write this as
$$
\int\limits_{-\infty}^{\infty}f(y)e^{-y D_{x}}g(x) \ dy
$$
where the exponential operator is acting on $g(x)$. Because everything in the integral is with respect to $y$, what if we take the $g(x)$ out of the integral, where the integral is still acting on $g(x)$? We get
$$
\int\limits_{-\infty}^{\infty}f(y)e^{-yD_{x}} \ dy \ g(x)
$$
We notice that this integral on the left can just be the [[Laplace Transforms|Laplace Transform]] from $y$ to $D_{x}$ (the differential operator with respect to $x$). Thus, this left side is an operator:
$$
\hat f(D_{x}) g(x)
$$
So, we can get around the convolution by using 
$$
\boxed{(f*g) = \hat f(D_{x})g(x)}
$$

This is particular useful with inverse Laplace Transforms, where 
$$
\mathcal{L}^{-1}\{\hat f_{1} \hat f_{2}\} = f_{1}*f_{2}= \hat f_{1}(D_{x})f_{2}
$$

