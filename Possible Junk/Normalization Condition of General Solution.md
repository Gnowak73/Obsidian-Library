---
tags: derivation, QM, Fourier_Series, Normalization, Schrodinger_Equation
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Normalization Condition of General Solution_
Applications: _Normalizing the general Schrodinger Equation Solution_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

If we have a general wave function solution (assume $\psi_{n}$ are orthonormal)
$$
\Psi(x,t) = \sum\limits_{n=1}^{\infty}c_{n}\psi_{n}(x)e^{\frac{-iE_{n}t}{\hbar}}
$$
and you need this wave function $\Psi$ to be normalized, then we have 
$$
\begin{gathered}
\int\limits_{-\infty}^{+\infty} \Psi^{*}(x,t) \Psi(x,t) \ dx = \int\limits_{-\infty}^{+\infty} \left(\sum\limits_{m=1}^{\infty} c_{m}\psi_{m}e^{\frac{-iE_{m}t}{\hbar}} \right)^{*} \left(\sum\limits_{n=1}^{\infty}c_{n}\psi_{n}e^{\frac{-iE_{n}t}{\hbar}}\right) \ dx = 1\\
\end{gathered}
$$
Because we are assuming that $\psi_{n}$ are orthogonal, then we should be able to create a basis which spans a functional vector space such that these infinite sums will converge under the condition the function represented by them is $L^{2}$. Thus, we assume $\Psi(x,t)$ is $L^{2}$ such that by [[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember#Bessel's Inequality|Bessel's Inequality]] we end up with Parseval's equality, this infinite series converges. If these infinite sums converge, then we can move the conjugate inside of the summation too. 

To combine these two series together though, requires that both of them converge along with their product or one of them is uniformly convergent. If we look at their product:
$$
\sum\limits_{m=1}^{\infty}\sum\limits_{n=1}^{\infty}c^{*}_{m}c_{n}\psi^{*}_{m}\psi_{n}
$$
This series must converge in order to have the normalization condition. 


If we also assume that this integral of these sums are finite, which is also required for the normalization condition, then we can change the order of summation and integration by the [[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember#Fubini Tonelli Theorem|Fubini Tornelli Theorem]]. Now, we can write (remember that $\psi$ is orthonormal)
$$
\sum\limits_{m=1}^{\infty}\sum\limits_{n=1}^{\infty}c^{*}_{m}c_{n}\int\limits_{-\infty}^{+\infty} \psi^{*}_{m}\psi_{n} \ dx = \sum\limits_{m=1}^{\infty}\sum\limits_{n=1}^{\infty}c^{*}_{m}c_{n}\delta_{mn} = \sum\limits_{m=1}^{\infty}|c_{m}|^{2}
$$
And if we remember before, this must equal $1$, so
$$
\boxed{\sum\limits_{m=1}^{\infty}|c_{m}|^{2} = 1 }
$$
This condition must hold for normalization.