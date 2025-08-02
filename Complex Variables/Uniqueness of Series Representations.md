---
tags: series, convergence, uniqueness, Math, Complex
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Uniqueness of Series Representations_
Applications: _Taylor series and Laurent series_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Series]], [[Taylor Series]],[[Laurent Series]]_
Cont.\_ of: _None_ 
_
_

**Theorem 1.**  If a series
$$
\sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n}
$$
converges to $f(z)$ at all points interior to some circle $|z-z_{0}|=R$, then it is the [[Taylor Series]] expansion for $f$ in powers of $z-z_{0}$. 

**Proof:**  The proof can be seen in <mark style="background: #BBFABBA6;">Sec. 72. Page 217</mark> of [[Complex Variables Textbook.pdf]]. This proof once again uses **Theorem 1.** from [[Properties of Complex Series#Integration and Differentiation of Power Series|Differentiation of Power Series]]. 

---

**Theorem 2.**  If a series 
$$
\sum\limits_{n=-\infty}^{\infty}c_{n}(z-z_{0})^{n} = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n}+ \sum\limits _{n=1}^{\infty} \frac{b_{n}}{(z-z_{0})^{n}}
$$
converges to $f(z)$ for all points in some annular domain about $z_{0}$, then it is the Laurent series expansion for $f$ in powers of $z-z_{0}$ for that domain. 

**Proof:**  This proof is similar to the one for **Theorem 1.**, basically its just an extension to negative exponents using similar methods. 