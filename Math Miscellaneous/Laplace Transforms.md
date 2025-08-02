---
tags:  Math, Laplace_Transform, ODE, PDE, Integrals, theorem, derivation
dg-publish: true
mathLink: 
---
Subject: _Laplace Transforms_
Main\_Topic: _Laplace Transforms_
Applications: _PDEs, ODE, steady state system analysis_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Fourier Transform]],[[Bromwich Integral]]_
_
_

Laplace transforms are integral transforms, similar to the [[Fourier Transform]], that allows us to analyze steady state systems and exponential decays unlike the [[Fourier Transform]]. The connection between the two is the variable substitution $s=i\omega$, where $s$ is the Laplace variable. 

The Laplace Transform is defined as follows:
$$
F(s) = \mathcal{L}\{f(t)\} = \int\limits_{0}^{\infty}e^{-st}f(t)dt
$$
for all values of $s$ for which the improper integral converges. The same requirements show up as with the [[Fourier Transform]], such as $f(t)$ being an $L^{1}$ function. 

#### Inverse Laplace Transform
The Inverse Laplace Transform is on the complex plane and is known as Mellin's inverse formula:
$$
f(t) = \frac{1}{2\pi i} \lim_{T\rightarrow\infty}\int\limits_{\gamma-iT}^{\gamma+iT}e^{st}F(s) \ ds
$$
which can usually be calculated using the [[Cauchy Residue Theorem]]. This integral is known as the [[Bromwich Integral]], this page also gives the insight to solving it and its nature. 

#### Convolution
Once again, like in [[Fourier Transform#Convolution]], we have the same properties. We can also get around the convolution by using the [[Heaviside Alternative to the Convolution]]. The convolution, though, for using Laplace Transform is usually defined as 
$$
(f*g)(t) \equiv \int\limits_{0}^{t}f(\tau )g(t-\tau )\ d\tau 
$$
when working with systems in time since $t\geq 0$ for an arbitrary time $t$ instead of over an entire space of $x$ like in the Fourier Transforms. 

#### Table of Transforms 
![[Pasted image 20230629171040.png]]