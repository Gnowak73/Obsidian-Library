---
tags: bromwich, Math, theorem, integral, Laplace, transform, Complex, contour
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Bromwich Integral_
Applications: _Laplace Transforms_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Laplace Transforms]]_
Cont.\_ of: _None_ 
_
_

Suppose that a function $F$ of the complex variable $s$ is analytic throughout the finite $s$ plane except for a finite number of isolated singularities. Then let $L_{R}$ denote a vertical line segment from $s=\gamma-iR$ to $s=\gamma+iR$, where the constant $\gamma$ is positive and large enough that the singularities of $F$ all lie to the left of that segment. 

![[Screenshot 2023-08-07 202836.png|center]]

A new function $f$ of the real variable $t$ is defined for positive values of $t$ by means of the equation
$$
f(t) = \frac{1}{2 \pi i} \lim_{R \rightarrow \infty} \int\limits_{L_{R}} e^{st} F(s) \ ds \quad (t>0)
$$
provided this limit exists. This expression is usually written as 
$$
f(t) = \frac{1}{2\pi i} \ \text{P.V.} \int\limits_{\gamma-i \infty }^{\gamma+i\infty } e^{st}F(s) \ ds \quad (t>0)
$$
and such an integral is sometimes referred to as a _Bromwich Integral_. 

It can be shown that when fairly general conditions are imposed, the function $f(t)$ is the Inverse [[Laplace Transforms|Laplace Transform]] of the function
$$
F(s) = \int\limits_{0}^{\infty}e^{-st}f(t) \ dt,
$$
This can be seen with the aid of the [[Cauchy Residue Theorem]], which tells us that 
$$
\int\limits_{L_{R}}e^{st}F(s) \ ds = 2 \pi i \sum\limits_{n=1}^{N}Res_{s=s_{n}}[e^{st}F(s)] - \int\limits_{C_{R}}e^{st}F(s) \ ds
$$
where $C_{R}$ is the semicircle shown in the figure above. Then, if we assume that 
$$
\lim_{R \rightarrow \infty } \int\limits_{C_{R}} e^{st} F(s) \ ds = 0
$$
it follows that 
$$
f(t) = \sum\limits_{n=1}^{N}Res_{s=s_{n}}[e^{st}F(s)] \quad (t>0)
$$
In many applications of [[Laplace Transforms]], such as the solutions of partial differential equations, the function $F(s)$ is analytic for all values of $s$ in the finite plane except for an _infinite_ set of isolates singular points $s_{n}$ that lie to the left of some vertical line $Re \ s = \gamma$. Often the method just described for finding $f(t)$ can be then modified in such a way that the finite sum is replaced by an _infinite series_ of residues:
$$
f(t) = \sum\limits_{n=1}^{\infty}Res_{s=s_{n}}[e^{st} F(s)] \quad (t>0)
$$
---
Using [[Application of Residues#Jordan's Lemma|Jordan's Lemma]], which we can generalize to the second and third quadrants, we can prove that 
$$
\lim_{R \rightarrow \infty} \int\limits_{C_{R}} e^{st}F(s) \ ds = 0
$$
Now, we know that 
$$
e^{st} = e^{s_{R}t}e^{is_{I}t} 
$$
so 
$$
\int\limits_{C_{R}}e^{s_{R}t}e^{is_{I}t}F(s) \ d s
$$
If $t>0$, then $s_{R}$ has to be less than $0$ in order to make $e^{s_{R}t}F(s)$ to be bounded from decay as $R \rightarrow \infty$. This is why our contour must be closed to the left. Now, we can take this one step further and know that 
$$
\left|\int\limits_{C_{R}}e^{s_{R}t}e^{is_{I}t}F(s) \ d s \right| \leq \int\limits_{C_{R}} \left| e^{s_{R}t}e^{is_{I}t}F(s)\right| \ d s = M_{R} R \int\limits_{C_{R}}e^{Rt \cos \theta} \ d \theta
$$
where $R>0$ and $\cos \theta < 0$. And if we take Jordan's lemma but do it for cosine, 
$$
-\cos \theta \geq \frac{2 \theta}{\pi} -1 \quad \left(\frac{\pi}{2}\leq \theta\leq \pi\right)
$$
Thus,
$$
e^{R\cos \theta} \leq e^{R(-2 \frac{\theta}{\pi} + 1)}
$$
Such that 
$$
\int\limits_{\frac{\pi}{2}}^{\pi}e^{R \cos \theta} d \theta \leq \int\limits_\frac{\pi}{2}^{\pi}e^{R(\frac{-2 \theta}{\pi}+1)} \ d \theta = \frac{\pi}{2 R}(1-e^{-R}) < \frac{\pi}{R}
$$
Thus, 
$$
\left|\int\limits_{C_{R}}e^{s_{R}t}e^{is_{I}t}F(s) \ d s \right| <  M_{R} R \frac{\pi}{R} = M_{R} \pi
$$
Thus, if $M_{R} \rightarrow 0$ as $R \rightarrow \infty$, then 
$$
\lim_{R \rightarrow \infty} \int\limits_{C_{R}}e^{st}F(s) \ ds = 0
$$
Thus, as long as $F(Re^{i \theta})$ is bounded and 