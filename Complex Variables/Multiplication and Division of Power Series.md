---
tags: Math, contour, series, division, multiplication, Complex, series, Taylor, Laurent
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Multiplication and Division of Power Series_
Applications: _Contour Integration, Taylor and Laurent Series_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Series]]_
Cont.\_ of: _None_ 
_
_

Suppose that each of the power series 
$$
\sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n} \quad  \sum\limits_{n=0}^{\infty}b_{n}(z-z_{0})^{n}
$$
converges within some circle $|z-z_{0}|=R$. Their sums $f(z)$ and $g(z)$ respectively, are then analytic functions in the disk $|z-z_{0}|<R$, and the product of those sums has a Taylor series expansion which is valid there: 
$$
f(z)g(z) =  \sum\limits_{n=0}^{\infty}c_{n}(z-z_{0})^{n} \quad (|z-z_{0}|<R).
$$
According to **Theorem 1.** in [[Properties of Complex Series#Integration and Differentiation of Power Series|integration and differentiation of power series]], the series $f(z)$ and $g(z)$ are themselves [[Taylor Series]]. 

The general expression for any coefficient $c_{n}$ is easily obtained by referring to **Leibniz's Rule** which states that 
$$
[f(z)g(z)]^{(n)} = \sum\limits_{k=0}^{n} {n \choose k} f^{(k)}(z)g^{(n-k)}(z) \quad (n=1,2,\ldots)
$$
where 
$$
{n \choose k} = \frac{n!}{k!(n-k)!} \quad (k=0,1,2,\ldots, n),
$$
for the nth derivative of the product of two differentiable functions. Evidently, 
$$
c_{n} = \sum\limits_{k=0}^{n}\frac{f^{(k)}(z_{0})}{k!} \cdot \frac{g^{(n-k)}(z_{0})}{(n-k)!} = \sum\limits_{k=0}^{n}a_{k}b_{n-k}
$$
Which looks like 

![[Pasted image 20230724211800.png|center]]

This is the same as the series obtained by formally multiplying the two series term by term and collecting the resulting terms in like powers of $z-z_{0}$; it is called the **Cauchy Product** of the two given series. 