---
tags: zeros, Math, Complex, poles, residues, cauchy, theorem, analytic
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Zeros and Poles_
Applications: _Contour Integration_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Residues, Zeros, and Poles]]_
Cont.\_ of: _None_ 
_
_

Zeros and poles are closely related. First, we will need some preliminary knowledge: [[Zeros of Analytic Functions]]. Now, we establish our first theorem:

**Theorem 1.**  Suppose that 

(a) two function $p$ and $q$ are analytic at a point $z_{0}$;
(b) $p(z_{0})\neq0$ and $q$ has a zero of order $m$ at $z_{0}$.

Then the quotient $\frac{p(z)}{q(z)}$ has a pole of order $m$ at $z_{0}$. 

**Proof:**  The proof is easy. Let $p$ and $q$ be as in the statement of this theorem. Since $q$ has a zero of order $m$ at $z_0$, we know from **Theorem 2** of [[Zeros of Analytic Functions]] that there is a deleted neighborhood of $z_{0}$ throughout which $q(z)\neq0$; and so $z_{0}$ is an isolated singular point of the quotient $\frac{p(z)}{q(z)}$. **Theorem 1** of [[Zeros of Analytic Functions]] tells us, moreover, that 
$$
q(z) = (z-z_{0})^{m}g(z),
$$
where $g(z)$ is analytic and nonzero at $z_{0}$. Consequently,
$$
\frac{p(z)}{q(z)} = \frac{\phi (z)}{(z-z_{0})^{m}} \quad \text{where} \quad \phi(z) = \frac{p(z)}{q(z)}
$$
Since $\phi(z)$ is analytic and nonzero at $z_{0}$, it now follows from the theorem in [[Residues at Poles]] that $z_{0}$ is a pole of order $m$ of $\frac{p(z)}{q(z)}$. 

---
Now, we can connect this statement from **Theorem 1** to the method in [[Residues at Poles]] to create our next theorem

**Theorem 2.**  Let two function $p$ and $q$ be analytic at a point $z_{0}$. If 
$$
p(z_{0})\neq0, \quad q(z_{0})=0, \quad \text{and} \quad q'(z_{0})\neq 0,
$$
then $z_{0}$ is a simple pole of the quotient $\frac{p(z)}{q(z)}$ and 
$$
Res_{z=z_{0}} \  \frac{p(z)}{q(z)} = \frac{p(z_{0})}{q'(z_{0})}
$$

**Proof:**  The proof of this theorem directly follows from **Theorem 1** for the case of a $m=1$ zero which results in a $m=1$ pole. More can be seen on <mark style="background: #D2B3FFA6;">page 252</mark> of [[Complex Variables Textbook.pdf]]. In short, according to **Theorem 1** of [[Zeros of Analytic Functions]]we have 
$$
q(z) = (z-z_{0})g(z)
$$
where $g(z)$ is nonzero and analytic at $z_{0}$. Now, we can use our theorem from [[Residues at Poles]] and get 
$$
Res_{z=z_{0}} \ \frac{\phi (z)}{z-z_{0}} = Res_{z=z_{0}} \ \frac{p(z)}{q(z)} = \frac{p(z_{0})}{g(z_{0})}
$$
and if we take $q(z)=(z-z_{0})g(z)$ and take the derivative and set $z=z_{0}$ we get
$$
q'(z) = g(z_{0}) + (z_{0}-z_{0})g'(z_{0}) = g(z_{0})
$$
Thus,
$$
Res_{z=z_{0}} \ \frac{p(z)}{q(z)} = \frac{p(z_{0})}{q'(z_{0})}
$$
##### Example
Let us find the residue of the function
$$
f(z) = \frac{z-\sinh(z)}{z^{2}\sinh z}
$$
at the zero $z=\pi i$. Now, if $p(z) = z-\sinh z$ and $q(z) = z^{2}\sinh z$, then 
$$
p(z_{0}) = p(\pi i) = \pi i \neq 0 \quad \text{and} \quad q(\pi i) = 0 \quad \text{and} \quad q'(\pi i) = \pi^{2}\neq 0,
$$
**Theorem 2** tells us that $z=\pi i$ is a simple pole of $f$ and that the residue there is 
$$
B = \frac{p(\pi i)}{q'(\pi i)} = \frac{\pi i}{\pi^{2}} =\boxed{ \frac{i}{\pi}}
$$
