---
tags: Math, Multivariable, derivation, Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Gaussian Integral_
Applications: _QM, Statistics, Integral Techniques_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
The Gaussian integral is a problem as below:
$$
\int\limits_{-\infty}^{+\infty} e^{-x^{2}} \ dx
$$
which cannot be solved unless you go to polar coordinates and do some mathematical trickery!

Let us define this integral above as 
$$
I = \int\limits_{-\infty}^{+\infty} e^{-x^{2}}\ dx
$$
Now, if we were to change $x$ to $y$ and $dx$ to $dy$, this integral should not change. We can use this trickery to write $I^{2}$ as
$$
I^{2} = \left(\int\limits_{-\infty}^{+\infty} e^{-x^{2}}dx\right) \times \left(\int\limits_{-\infty}^{+\infty} e^{-y^{2}} \ dy \right) = \int\limits_{-\infty}^{+\infty} \int\limits_{-\infty}^{+\infty} e^{-(x^{2}+y^{2})} dxdy
$$
We can transform this integral into polar coordinates (where the determinant of the [[Jacobian]], $J$, is just $r$) to get:
$$
\int\limits_{0}^{2\pi}\int\limits_{0}^{\infty}e^{-r^{2}} |J(r,\theta)| d(r,\theta) = \int\limits_{0}^{2\pi}\int\limits_{0}^{\infty}e^{-r^{2}}r \ drd\theta 
$$
The reason the limits of integration changed is because $2\pi$ is an entire rotation about the entire polar plane, so we are going from $0 \rightarrow \infty$ from $r$ while rotating around the entire plane which covers the entire space, the equivalent of $x$ and $y$ covering their entire plane which would be from $-\infty \rightarrow \infty$. We can easily solve this integral as 
$$
\int\limits_{0}^{2\pi} \frac{1}{2} e^{-r^{2}}dr^{2}d\theta = \frac{2\pi}{2} \left[-e^{-r^{2}}\right\rvert_{0}^{\infty} = \pi(0-(-1)) = \pi
$$
Remember, this is still $I^{2}$ though, so to get $I$ we take the square root:
$$
\boxed{I=\sqrt{\pi}}
$$