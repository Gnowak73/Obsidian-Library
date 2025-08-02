---
tags: Math, Complex, theorem, equation, Cauchy_integral, Contour, Liouville, analytic, bounded, entire, complex_plane
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Liouville's Theorem_
Applications: _Theorem stating that if a function is bounded and entire then it is constant_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Cauchy Integral Formula]],[[Contour Integrals]]_
Cont.\_ of: _None_ 
_
_

**Theorem 1.**  If a function $f$ is entire and bounded in the complex plane, then $f(z)$ is constant throughout the plane. 

**Proof:**  This proof is started with the assumption that $f$ is is as stated and note that since $f$ is entire, we can apply the [[Cauchy Integral Formula#Extension of the Cauchy Integral Formula#Cauchy Integral Bounded Moduli Theorem|Cauchy Integral Bounded Moduli Theorem]] with any choice for a circle centered at $z_{0}$ and with radius $R$. In particular, we know that for the $n=1$ scenario:
$$
|f'(z_{0})| \leq \frac{M_{R}}{R}.
$$
The bounded condition for $f$ ensures that a constant $M$ exists on the entire complex plane such that $|f(z)| \leq M$ for all $z$. Because the constant $M_{R}$ (maximum of $|f(z)|$ **on the contour**) will always be $\leq M$, we can then state that 
$$
|f'(z_{0})| \leq \frac{M}{R}
$$
where $R$ can be arbitrarily large. The number $M$ in this inequality is independent of the value of $R$ that is taken. Hence the inequality holds for arbitrarily large values of $R$ only if $f'(z_{0})=0$. Since the choice of $z_{0}$ is arbitrary, this means that $f'(z)=0$ everywhere in the complex plane. Consequently, $f$ is a constant function. 


##### Fundamental Theorem of Algebra
Another theorem follows from Liouville's theorem called the *fundamental theorem of algebra*. 

**Theorem 2.**  Any polynomial
$$
P(z) = a_{0}+a_{1}z+a_{2}z^{2}+\ldots +a_{n}z^{n} \quad (a_{n}\neq 0)
$$
of degree $n$ where $n \geq 1$, has _at least_ one zero. That is, there exists at least one point $z_{0}$ such that $P(z_{0})=0$.

**Proof:**  The proof here is by contradiction. Suppose that $P(z)$ is _not_ zero for any value of $z$. Then the quotients $\frac{1}{P(z)}$ is clearly entire. It is also bounded in the complex plane. 

To see that is is bounded, we first recall (proof in [[Complex Variables Textbook.pdf]] Sec. 5.) that there is a positive number $R$ such that 
$$
\left|\frac{1}{P(z)}\right| < \frac{2}{|a_{n}|R^{n}} \quad \text{whenever} \ |z|> R
$$
So $\frac{1}{P(z)}$ is bounded in the region _exterior_ to the disk $|z| \leq R$. But $\frac{1}{P(z)}$ is continuous on that closed disk, and this means that $\frac{1}{P(z)}$ is bounded there too. Hence $\frac{1}{P(z)}$ is bounded in the entire plane. It now follows from Liouville's theorem that $\frac{1}{P(z)}$, and consequently $P(z)$, is constant. But $P(z)$ is not constant, and now we have thus reached a contradiction. 


**Remark.**  It now follows from the _fundamental theorem of algebra_ that any polynomial can be expressed as a product of linear factors 
$$
P(z) = c(z-z_{1})(z-z_{2})\ldots(z-z_{n})
$$
where $z_{1},z_{2},\ldots,z_{n}$ are distinct zeros. More precisely, the theorem ensures that $P(z)$ has a zero $z_{1}$. Then, we should be able to write 
$$
P(z) = (z-z_{1})Q_{1}(z)
$$
---
The proof for being able to write this comes from the fact that if we have the polynomial 
$$
P(z) = a_{0}+a_{1}z+a_{2}z^{2}+\ldots+a_{n}z^{n}
$$
we can write 
$$
z^{k}-z_{0}^{k} = (z-z_{0})(z^{k-1}+z^{k-2} \ z_{0}+\ldots+z \ z_{0}^{k-2}+z_{0}^{k-1})
$$
Then using factorization we can show that 
$$
P(z)-P(z_{0}) = (z-z_{0})Q(z)
$$
where $Q(z)$ is a polynomial of degree $n-1$. 

---
Now, we should be able to write, using the ensured $z_{1}$ zero from the _fundamental theorem of algebra_, 
$$
P(z) = (z-z_{1})Q_{1}(z)
$$
Then, using the fundamental theorem of algebra on $Q_{1}(z)$, we have a guaranteed zero $z_{2}$ such that we can write 
$$
P(z) = (z-z_{1})(z-z_{2})Q_{2}(z)
$$
and we keep doing this until we have a polynomial $Q_{n}(z)$ of $n=0$ which is $Q_{n}(z)=c$ for some constant $c$. It is clear that we can only have $n$ distinct zeros since we cannot do this procedure past a polynomial $Q(z)=1$. Thus, proving our statement along with the important fact that _a polynomial of degree n has only n distinct zeros_. 