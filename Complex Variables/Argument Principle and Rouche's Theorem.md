---
tags: Complex, Math, argument, principle, derivation, theorem, Rouche, argument_principle, winding, winding_number, transformation, complex,
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Argument Principle and Rouche's Theorem_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Application of Residues]]_
Cont.\_ of: _None_ 
_
_

### Winding Number and Argument Principle
```ad-Definition
A function is said to be **meromorphic** in a domain $D$ if it is analytic throughout $D$ except for poles.
```
Suppose now that $f$ is meromorphic in the domain interior to a positively oriented simple closed contour $C$ and that it is analytic and nonzero on $C$. The image $\Gamma$ of $C$ under the transformation $w=f(z)$ is a closed contour, not necessarily simple, in the $w$ plane. As a point $z$ traverses $C$ in the positive direction, its image $w$ traverses $\Gamma$ in a particular direction that determines the oriented of $\Gamma$ Note that since $f$ has no zeros on $C$, the contour $\Gamma$ does not pass through the origin in the $w$ plane. 

![[Screenshot 2023-08-07 181257.png|center]]

Let $w_{0}$ and $w$ be points on $\Gamma$, where $w_{0}$ is fixed and $\phi_{0}$ is a value of $\arg \ w_{0}$. Then let $arg \ w$ vary continuously, starting with the value $\phi_{0}$, as the point $w$ begins at the point $w_{0}$ and traverses $\Gamma$ once in the direction of orientation assigned to it by the mapping $w=f(z)$. When $w$ returns to the point $w_{0}$, where it started, $arg \ w$ assumed a particular value of $\arg \ w_{0}$, which we denote by $\phi_{1}$. Thus, the change in $\arg \ w$ as $w$ describes $\Gamma$ once in its direction of orientation is $\phi_{1}-\phi_{0}$. This change is, of course, independent of the point $w_{0}$ that is chosen to determine it. Since $w=f(z)$, the number $\phi_{1}-\phi_{0}$ is, in fact, the change in argument of $f(z)$ as $z$ describes $C$ once in the positive direction, starting with a point $z_{0}$; and we write 
$$
\Delta_{C} \arg \ f(z) = \phi_{1}-\phi_{0}
$$
The value of $\Delta_{C}\arg f(z)$ is evidently an integral multiple of $2 \pi$, and the integer 
$$
\frac{1}{2\pi} \Delta_{C} \arg f(z)
$$
represents the number of times the point $w$ winds around the origin in the $w$ plane. For that reason, this integer is called the **winding number** of $\Gamma$ with respect to the origin $w=0$.

The winding number is always zero when $\Gamma$ does not enclose the origin. The winding number can be determined by the number of zeros and poles of $f$ that are interior to $C$. The number of poles is necessarily finite. Likewise, with the understanding that $f(z)$ is not identically equal to zero everywhere else inside $C$, it is easily shown that the zeros of $f$ are finite in number and are all of finite order ([[Zeros of Analytic Functions]]).

---
**Remark.**  The only scenario where we don't have isolated zeros would be if there were infinite zeros converging close to one another such that they were always in the same neighborhood. We can see from **Theorem 2** and **Theorem 3** from [[Zeros of Analytic Functions]] that there must be finite zeros and $f(z)$ cant be identically zero elsewhere in $C$ or else it would have to be zero in the entire domain.

---

Suppose now that $f$ has $Z$ zeros and $P$ poles in the domain interior to $C$. We agree that $f$ has $m_{0}$ zeros at a point $z_{0}$ if it has a zero of order $m_{0}$ there; and if $f$ has a pole of order $m_{p}$ at $z_{0}$, that pole is to be counted $m_{p}$ times. The following theorem, which is known as the _argument principle_, states that the winding number is simply the difference $Z-P$.

**Theorem.**  Let $C$ denote a positively oriented simple closed contour, and suppose that 

(a) a function $f(z)$ is meromorphic in the domain interior to $C$; 
(b) $f(z)$ is analytic and nonzero on $C$;
(c) counting multiplicities, $Z$ is the number of zeros and $P$ is the number of poles of $f(z)$ inside $C$.

Then,
$$
\frac{1}{2\pi}\Delta_{C}\arg f(z) = Z-P
$$

---
**Proof:**  The full proof is on <mark style="background: #ADCCFFA6;">Pg. 289</mark> of [[Complex Variables Textbook.pdf]]. The proof of this theorem we first evaluating the integral $\frac{f'(z)}{f(z)}$ around $C$, one by parametrization $z(t)=r(t)e^{i \theta(t)}$ in which $w=\rho(t)e^{i \phi(t)}$, to get 
$$
\int\limits_{C} \frac{f'(z)}{f(z)} \ dz = i \Delta_{C}\arg f(z)
$$
and then use the [[Cauchy Residue Theorem]] by observing that $\frac{f'(z)}{f(z)}$ is analytic inside and on $C$ except for a finite number of points which the zeros and poles occur. If $f$ has a zero of order $m_{0}$ then we can write using **Theorem 1** from [[Zeros of Analytic Functions]] that $f(z) = (z-z_{0})^{m_{0}}g(z)$, from there we can take the derivative of $f$ and write out 
$$
\frac{f'(z)}{f(z)} = \frac{m_{0}}{z-z_{0}} + \frac{g'(z)}{g(z)}
$$
and then from here we know that the fraction $\frac{g'}{g}$ is analytic and must have a [[Taylor Series]], thus we know from $\frac{f'}{f}$ has a simple pole at $z_{0}$ with residue $m_{0}$. If, on the other hand, $f$ has a pole of order $m_{p}$ at $z_{0}$, we know from **Theorem 1** in [[Residues at Poles]] that we can write $f(z) = (z-z_{0})^{-m_{p}}\phi(z)$. Because this has the same expression as the one with the zeros, we can see this this must result in having a residue $-m_{p}$. Thus, if we have both a zero and a pole, we have the residues $m_{0}=Z$ and $-m_{p}=-P$ respectively. Applying the residue theorem we finally get
$$
\int\limits_{C} \frac{f'(z)}{f(z)} \ dz = 2 \pi i (Z-P)
$$
Plug this into our first integral and boom we are done with the proof.

##### Example.
The only zeros of the function 
$$
f(z) = \frac{z^{3}+2}{z} = z^{2} + \frac{2}{z}
$$
are exterior to the circle $|z|=1$, since they are the cube roots of $-2$; and the only singularity in the finite plane is a simple pole at the origin. Hence, if $C$ denotes the circle $|z|=1$ in the positive direction, our theorem tells us that 
$$
\Delta_{C}\arg f(z) = 2 \pi (0-1) = -2 \pi
$$
That is, the image $\Gamma$ of $C$ under the transformation $w=f(z)$ winds around the origin $w=0$ once in the clockwise direction. 

### Rouche's Theorem
The main result is known as **Rouche's Theorem** and is a consequence of the argument principle. It can be useful in locating regions of the complex plane in which a given analytic function has zeros.  

**Theorem.**  Let $C$ denote a simple closed contour; and suppose that 

(a) Two function $f(z)$ and $g(z)$ are analytic inside and on $C$;
(b) $|f(z)|> |g(z)|$ at each point on $C$.

Then $f(z)$ and $f(z)+g(z)$ have the same number of zeros, counting multiplicities, inside $C$. 

**Proof:**  The proof can be seen in <mark style="background: #BBFABBA6;">Pg. 291, Sec. 94</mark> of [[Complex Variables Textbook.pdf]]. 

**Remark.**  Rouche's Theorem can be used to give another proof of the fundamental theorem of algebra, ensuring the existence of $n$ zeros, counting multiplicities, while [[Liouville's Theorem]] only ensures the existence of at least one zero of a polynomial (but this can be extrapolated into $n$ distinct zeros as seen in [[Liouville's Theorem#Fundamental Theorem of Algebra]]). The proof can be seen on <mark style="background: #ABF7F7A6;">Pg. 292</mark> of [[Complex Variables Textbook.pdf]].

##### Example. 
In order to determine the number of roots, counting multiplicities, of the equation
$$
z^{4}+3z^{3}+6=0
$$
inside the circle $|z|=2$, write 
$$
f(z) = 3z^{3} \ \quad \text{and} \quad g(z) = z^{4}+6
$$
Then observe that when $|z|=2$,
$$
|f(z)| = 3|z|^{3} = 24 \quad \text{and} \quad |g(z)| \leq |z|^{4}+6 = 22
$$
The three conditions of Rouche's Theorem are satisfied. Consequently, since $f(z)$ has three zeros, counting multiplicities, inside the circle $|z|=2$, so does $f(z)+g(z)$.  