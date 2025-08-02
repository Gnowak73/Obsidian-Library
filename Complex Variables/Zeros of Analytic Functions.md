---
tags: Complex, Math, zeros, analytic, functoin, isolated, singularity,
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Zeros of Analytic Functions_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Analytic Functions]],[[Uniquely Determined Analytic Functions]]_
Cont.\_ of: _None_ 
_
_

Suppose that a function $f$ is analytic at a point $z_{0}$. We know that all of the derivatives $f^{(n)}(z_{0}) \ (n=1,2,\ldots)$ exist at $z_{0}$. If $f(z_{0})=0$ and if there is a positive integer $m$ such that 
$$
f(z_{0}) = f'(z_{0}) = f''(z_{0}) =\ldots f^{(m-1)}(z_{0}) = 0 \quad \text{and} \quad f^{(m)}(z_{0}) \neq 0
$$
where $m$ is a positive integer, $f$ is said to have a _zero of order m_ at $z_{0}$. Our first theorem here provides a useful alternative definition of zeros of order $m$. 

**Theorem 1.**  Let $f$ denote a function that is analytic at a point $z_{0}$. The following two statements are equivalent:

(a) $f$ has a zero of order $m$ at $z_{0}$;
(b) there is a function $g$, which is analytic and nonzero at $z_{0}$, such that 
$$
f(z) = (z-z_{0})^{m}g(z)
$$

**Proof:**  The proof of this theorem has two parts. First, we need to show that the truth of (a) implies the statement (b). Once that is accomplished, we need to show that if statement (b) is true, then so is statement (a). Both parts use the fact that if a given function is analytic at a point $z_{0}$, then it must have a [[Taylor Series]] representation in powers of $(z-z_{0})$ that is valid throughout some neighborhood $|z-z_{0}|<\epsilon$ of $z_{0}$. This full proof can be seen in <mark style="background: #FFB86CA6;">Sec. 82, page 248</mark> of [[Complex Variables Textbook.pdf]]. 

---
##### Example. 
If we have the polynomial $f(z)=z^{3}-1$, which has a zero of order $m=1$ at $z_{0}=1$ since 
$$
f(z) = (z-1)g(z)
$$
where $g(z)=z^{2}+z+1$, and because $f$ and $g$ are entire and $g(1)=3\neq0$.

---
##### Isolated Zeros
Our next theorem is a precise statement of the fact that an analytic function $f(z)$ has only **isolated zeros** when it is not identically equal to zero. This means that if $z_{0}$ is a zero of such a function $f(z)$, there is a deleted neighborhood $0<|z-z_{0}|<\epsilon$ of $z_{0}$ in which $f(z)$ is nonzero. (Compare with the definition of an isolated singularity in [[Residues, Zeros, and Poles]]). 

**Theorem 2.**  Given a function $f$ and a point $z_{0}$, suppose that 

(a) $f$ is analytic
(b) $f(z_{0})=0$ but $f(z)$ is not identically equal to zero in any neighborhood of $z_{0}$.

Then $f(z)\neq0$ throughout some deleted neighborhood $0<|z-z_{0}|<\epsilon$ of $z_{0}$. 

**Proof:**  To prove this, let $f$ be as stated and observe that not all of the derivatives of $f$ at $z_{0}$ are zero. If they are, all of the coefficients in the [[Taylor Series]] for $f$ about $z_{0}$ would be zero; and that would mean that $f(z)$ is identically equal to zero in some neighborhood of $z_{0}$. So it is clear from the definition of zeros of order $m$ at the beginning that $f$ must have a zero of some finite order $m$ at $z_{0}$. According the **Theorem 1.**, then we have 
$$
f(z) = (z-z_{0})^{m}g(z)
$$
where $g(z)$ is analytic and nonzero at $z_{0}$. Now, $g$ is continuous, in addition to being nonzero, at $z_{0}$ because it is analytic there. Hence there is some neighborhood $|z-z_{0}|<\epsilon$ in which this equation for $f(z)$ holds and in which $g(z)\neq0$. Consequently, $f(z)\neq0$ in the _deleted_ neighborhood $0<|z-z_{0}|<\epsilon$. This concludes our proof. 

---
##### Case of Not all Isolated Zeros
Our final theorem here concerns functions with zeros that are not all isolated. It is referred to in [[Uniquely Determined Analytic Functions]]. 

**Theorem 3.** Given a function $f$ and a point $z_{0}$, suppose that 

(a) $f$ is analytic throughout a neighborhood $N_{0}$ of $z_{0}$;
(b) $f(z)=0$ at each point $z$ of a domain $D$ or line segment $L$ containing $z_{0}$

Then $f(z)\equiv0$ in $N_{0}$; that is, $f(z)$ is identically zero throughout the neighborhood $N_{0}$.  

![[Screenshot 2023-07-31 171237.png|center]]

**Proof:**  We begin the proof with the observation that under the stated conditions, $f(z)\equiv0$ in some neighborhood $N$ of $z_{0}$. For, otherwise, there would be a deleted neighborhood of $z_{0}$ throughout which $f(z)\neq0$ according to **Theorem 2.**; and that would be inconsistent with the condition that $f(z)=0$ everywhere in a domain $D$ or on a line segment $L$ containing $z_{0}$. Since $f(z)\equiv0$ in the neighborhood $N$, then it follows that all of the coefficients 
$$
a_{n}=\frac{f^{(n)}(z_{0})}{n!} \quad (n=0,1,2,\ldots)
$$
in the Taylor Series for $f(z)$ about $z_{0}$ must be zero. Thus, $f(z)\equiv0$ in the neighborhood $N_{0}$, since the Taylor Series also represents $f(z)$ in $N_{0}$. This completes the proof. 

