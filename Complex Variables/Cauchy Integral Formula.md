---
tags: Cauchy, Integral, Math, Complex, Cauchy_Integral, theorem, equation, contour, derivative, analytic
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Cauchy Integral Formula_
Applications: _Contour Integrals, Expression of Derivatives as Contour Integrals and Vice Versa_
Examples: _[[MATH_450_Quiz_3.pdf]]_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Contour Integrals]],[[Cauchy Goursat Theorem]],[[Contour Integral Domains]],[[Analytic Functions]]_
Cont.\_ of: _None_ 
_
_

**Theorem.**  Let $f$ be _analytic everywhere inside and on_ a simple closed contour $C$, taken in the positive sense. If $z_{0}$ is any point interior to $C$, then 
$$
f(z_{0}) = \frac{1}{2 \pi i}\int\limits_{C} \frac{f(z) \ dz}{z-z_{0}}
$$

This expression is known as the **Cauchy Integral Formula**. It tells us that is a function $f$ is to be analytic within and on a simple closed contour $C$, then the values of $f$ interior to $C$ are completely determined by the values of $f$ on $C.$ 

**Proof.**  The proof is within [[Complex Variables Textbook.pdf]]. 

This theorem can be used to easily find the contour integral of functions that are analytic with either no singularities or one singularity in a contour/domain. 

```ad-Remember
One thing worth noting is that if we had a function with multiple singularities, we could use partial fraction decomposition and write it as the sum of fractions with only one singularity! Then we could apply the Cauchy Integral theorem on each part.

But there is also another thing we can do.... If we define functions $g_{n}(z)=f(z)(z-z_{n})$ where $z_{n}$ is the singularity, then we could create a clockwise contour $C_{n}$ around each of the singularities such that each function $g_{n}(z)$ is analytic on and within the contour $C_{n}$. We could then use the [[Cauchy Goursat Theorem]] to write our original contour integral as a sum of the contour integrals $C_{n}$ and use the Cauchy Integral theorem to evaluate each of them!!! 
```

Such techniques as described above can be seen in the examples for [[Contour Integrals]]. 

---
#### Extension of the Cauchy Integral Formula
The Cauchy Integral formula can be extended so as to provide an integral representation for derivatives $f^{(n)}(z_{0})$ of $f$ at $z_{0}$.

**Theorem.**  Let $f$ be an analytic function inside and on a simple closed contour $C$, taken in the positive sense. If $z_{0}$ is any point interior to $C$, then 
$$
f^{(n)}(z_{0}) = \frac{n!}{2 \pi i} \int\limits_{C}\frac{f(z) \ dz}{(z-z_{0})^{n+1}} \quad (n=0,1,2,\ldots)
$$
This theorem includes the original Cauchy Integral formula. 

**Remark.**  $z$ in this theorem represents points _ON_ the contour, and $z_{0}$ represents points _INTERIOR_ to the contour. We could even rewrite this formula for points $z$ interior to the contour and points $s$ on the contour:
$$
f^{(n)}(z) = \frac{n!}{2 \pi i} \int\limits_{C}\frac{f(s) \ ds}{(s-z)^{n+1}} \quad (n=0,1,2,\ldots)
$$

**Verification of this Extension:**  The verification of this extension can be seen in [[Complex Variables Textbook.pdf]] in <mark style="background: #BBFABBA6;">Chapter 4</mark>.

---
##### Consequences of this Extension

**Theorem 1.**  If a function $f$ is analytic at a given point, then its derivatives of all order are analytic there too.

**Proof:**  If $f$ is analytic at a point, then where must be a neighborhood $|z-z_{0}|<\epsilon$ where $f$ is analytic (definition of [[Analytic Functions]]). Consequently, there is a positively oriented circle $C_{0}$, centered at $z_{0}$ and with radius $\frac{\epsilon}{2}$, such that $f$ is analytic inside and on $C_{0}$. From the Cauchy Integral Theorem we know that 
$$
f''(z) = \frac{1}{\pi i }\int\limits_{C}\frac{f(s) \ ds}{(s-z)^{3}}
$$
at each point $z$ interior to $C_{0}$, and the existence of $f''(z)$ throughout the neighborhood $|z-z_{0}|<\frac{\epsilon}{2}$ means that $f'$ is analytic at $z_{0}$. One can apply this same argument to the analytic function $f'$ and so on. 

---
**Theorem 2.**  Let $f$ be continuous on a domain $D$. If 
$$
\int\limits_{C}f(z) \ dz = 0
$$
for every closed contour $C$ in $D$, then $f$ is analytic in $D$. 

**Proof:**  This is simply the converse of the theorems in [[Contour Integral Domains]] and [[Contour Integrals#Antiderivatives]]. We know that if the contour integral is zero no matter which path you take for every closed contour in a domain, then there must be an antiderivative at every point in that domain (since $F(z_{1})-F(z_{0})=0$). The derivative of this antiderivative is $f(z)$. We know that if a function is analytic, then its derivatives of all order are analytic too. Thus, since the antiderivative is analytic, then its derivative $f$ must also be analytic in $D$. 

---
###### Cauchy Integral Bounded Moduli Theorem
**Theorem 3.**  Suppose that a function $f$ is analytic inside and on a positively oriented circle $C_{R}$, centered at $z_{0}$ and with radius $R$. If $M_{R}$ denotes the maximum value of $|f(z)|$ on $C_{R}$, then 
$$
|f^{(n)}(z_{0})| \leq n! \frac{M_{R}}{R^{n}} \quad (n=1,2,\ldots)
$$
This inequality is knows as **Cauchy's Inequality** and is an immediate consequence of the expression 
$$
f^{(n)}(z_{0}) = \frac{n!}{2 \pi i} \int\limits_{C}\frac{f(z) \ dz}{(z-z_{0})^{n+1}} \quad (n=1,2,\ldots)
$$
where $n$ is a positive integer. 

**Proof:**  We get the proof for this theorem by applying the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Moduli Theorem]] which results in
$$
|f^{(n)}(z_{0})| \leq \frac{n!}{2 \pi} \frac{M_{R}}{R^{n+1}} 2 \pi R \quad (n=1,2,\ldots)
$$

**Remark.**  **Cauchy's Inequality** can actually be used to show that no entire function except a constant is bounded in the complex plane. This is known as [[Liouville's Theorem]], which states it in a slightly different way. 

###### Maximum Modulus Principle
We can derive an important result involving maximum values of the moduli of analytic function. We begin with the lemma

**Lemma.**  Suppose that $|f(z)| \leq |f(z_{0})|$ at each point $z_{0}$ in some neighborhood $|z-z_{0}|<\epsilon$ in which $f$ is analytic. Then $f(z)$ has the constant value $f(z_{0})$ throughout that neighborhood.

**Proof:**  We assume that $f$ satisfies the stated conditions and let $z_{1}$ be any point other than $z_{0}$ in the given neighborhood. We then let $\rho$ be the distance between $z_{1}$ and $z_{0}$. If $C_{\rho}$ denotes the positively oriented circle $|z-z_{0}|=\rho$, centered at $z_{0}$ and passing through $z_{1}$, the Cauchy Integral Formula tells us that 
$$
f(z_{0}) = \frac{1}{2 \pi i} \int\limits_{C_{\rho}} \frac{f(z) \ dz}{z-z_{0}}
$$
![[Pasted image 20230711190141.png|center]]
and the parametric representation 
$$
z=z_{0}+\rho e^{i \theta} \quad (0 \leq \theta \leq 2 \pi)
$$
for $C_{\rho}$ enables us to write this contour integral as 
$$
f(z_{0}) = \frac{1}{2 \pi}\int\limits_{0}^{2 \pi} f(z_{0}+\rho e^{i \theta}) \ d \theta. 
$$
We note from this expression that when a function is analytic within and on a given circle, its value at the center is the _arithmetic mean_ of its values on the circle. This result is called **Gauss's Mean Value Theorem**. 

From our integral equation and using the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds for Moduli Theorem]], we obtain the inequality
$$
\boxed{|f(z_{0})| \leq \frac{1}{2 \pi} \int\limits_{0}^{2 \pi} |f(z_{0}+ \rho e^{i \theta})| \ d \theta}
$$
One the other hand, since, from our stated condition $|f(z)| \leq |f(z_{0})|$,
$$
\tag{1} |f(z_{0}+ \rho e^{i \theta})| \leq |f(z_{0})| \quad (0\leq \theta\leq 2 \pi),
$$
we find that 
$$
\int\limits_{0}^{2 \pi} |f(z_{0} + \rho e^{i \theta})| \ d \theta \leq \int\limits_{0}^{2 \pi}|f(z_{0})| \ d \theta = 2 \pi|f(z_{0})|
$$
Thus 
$$
\boxed{|f(z_{0})| \geq \frac{1}{2 \pi} \int\limits_{0}^{2 \pi} |f(z_{0}+ \rho e^{i \theta})| \ d \theta}
$$
From these two inequalities it is evident that 
$$
|f(z_{0})| = \frac{1}{2 \pi} \int\limits_{0}^{2 \pi} |f(z_{0}+ \rho e^{i \theta})| \ d \theta
$$
or 
$$
\int\limits_{0}^{2 \pi} [|f(z_{0})| - |f(z_{0}+\rho e^{i \theta})|] \ d \theta = 0
$$
The integrand in this last integral is continuous in the variable $\theta$; and, in view of the condition (1), it is greater than or equal to zero on the entire interval $0\leq \theta\leq 2 \pi$. Because the integral is equal to $0$, then the integrand must be identically equal to $0$. That is,
$$
|f(z_{0}+\rho e^{i \theta})| = |f(z_{0})| \quad (0\leq \theta \leq 2 \pi)
$$
This shows that $|f(z)|=|f(z_{0})|$ _for all points $z$ on the circle_ $|z-z_{0}|= \rho$. Finally, since $z_{1}$ is any point in the deleted neighborhood $0<|z-z_{0}|<\epsilon$, we see that $|f(z)|=|f(z_{0})|$ is in fact, satisfied by all points $z$ lying on any circle $|z-z_{0}|= \rho$, where $0<\rho<\epsilon$. Consequently, $|f(z)|=|f(z_{0})|$ everywhere in the neighborhood $|z-z_{0}|< \epsilon$. 

We know that when the modulus of an analytic function is constant, that the function itself must be constant there (Proof Here: [[Analytic Functions#Constant Modulus of Analytic Function]]). Thus, $f(z)=f(z_{0})$ for each point $z$ in the neighborhood, and the proof of the lemma is complete! 

This lemma can be used to prove the following theorem, known as the **Maximum Modulus Principle**. 

---
**Theorem.**  If a function $f$ is analytic and not constant in a given domain $D$, then $|f(z)|$ has no maximum value in $D$. That is, there is no point $z_{0}$ in the domain such that $|f(z)| \leq |f(z_{0})|$ for all points $z$ in it.

**Proof:**  In Sec. 59. of [[Complex Variables Textbook.pdf]]