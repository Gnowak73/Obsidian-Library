---
tags: Math, Complex, pole, residue, theorem,
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Residues at Poles_
Applications: _The Theory of Residues and the Cauchy Residue Theorem_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Residues, Zeros, and Poles]]_
Cont.\_ of: _None_ 
_
_

When a function $f$ has an isolated singularity at a point $z_{0}$, the basic method for identifying $z_{0}$ as a pole and finding the residue there is to write the appropriate [[Laurent Series]] and to note the coefficient of $\frac{1}{z-z_{0}}$. The following theorem provides and alternative characterization of poles and a way of finding residues at poles that is often more convenient. 

---
**Theorem.**  Let $z_{0}$ be an isolated singular point of a function $f$. The following two statements are equivalent:

(a) $z_{0}$ is a pole of order $m \ (m=1,2\ldots)$ of $f$;
(b) $f(z)$ can be written in the form 
$$
f(z) = \frac{\phi(z)}{(z-z_{0})^{m}} \quad (m=1,2,\ldots)
$$
where $\phi(z)$ is analytic and nonzero at $z_{0}$. 

Moreover, if statements (a) and (b) are true (they are indeed also equivalent), 
$$
Res_{z=z_{0}} \ f(z) = \phi(z_{0}) \quad \text{when} \quad m=1
$$
and 
$$
Res_{z=z_{0}} \ f(z) = \frac{\phi^{(m-1)}(z_{0})}{(m-1)!} \quad \text{when} \quad m=2,3,\ldots
$$

**Remark.**  Observe that these two expressions for residues need not have been written separately. Also, it is worth noting that while this theorem is extremely useful, the identification of an isolated singular point as a pole of a certain order is sometimes done most efficiently by appealing directly to a [[Laurent Series]]. 

**Proof:**  The proof can be seen on <mark style="background: #ABF7F7A6;">page 243</mark> of [[Complex Variables Textbook.pdf]]. It begins by defining a function similar to the method in [[Cauchy Integral Formula]] where we let $g_{n}(z)=f(z)(z-z_{n})$ such that we can separate a contour integral into analytic parts. From this representation, we can see that $\phi(z)$ is analytic and can thus be represented by a [[Taylor Series]]. Plugging this Taylor Series back into $f(z)=\frac{\phi(z)}{(z-z_{0})^{m}}$, we can expand the series to see when we get the fraction $1/(z-z_{0})$. Looking at the conditions for this coefficient we can get the previous formulation for the residue. 

---
##### Example 1. 
The function
$$
f(z) = \frac{z+4}{z^{2}+1}
$$
has an isolated singular point at $z=i$ and can be written as 
$$
f(z) = \frac{\phi(z)}{z-i} \quad \text{where} \quad  \phi(z) = \frac{z+4}{z+i}.
$$
Since $\phi(z)$ is analytic at $z=i$ and $\phi(i)\neq0$, that point is a simple pole of $f$; and the residue there is 
$$
B_{1} = \phi(i) = \frac{i+4}{2i} = \frac{1}{2}-2i 
$$
The point $z=-1$ is also a simple pole of $f$ with the residue
$$
B_{2}=\frac{1}{2}+2i 
$$

##### Example 2. 
If 
$$
f(z) = \frac{z^{3}+2z}{(z-i)^{3}}
$$
then 
$$
f(z) = \frac{\phi(z)}{(z-i)^{3}} \quad \text{where} \quad \phi(z) = z^{3}+2z.
$$
The function $\phi(z)$ is entire, and $\phi(i)=i\neq0$. Hence $f$ ahs a pole of order $3$ at $z=i$, with residue 
$$
B= \frac{\phi''(i)}{2!} = \frac{6i}{2!} = 3i
$$

##### Example 3.
This theorem can also be used when branches of multiple-valued functions are involved. Suppose that 
$$
f(z) = \frac{(\log  z)^{3}}{z^{2}+1},
$$
where the branch
$$
\log z = \ln r + i \theta \quad (r>0, \ 0<\theta<2 \pi)
$$
of the logarithmic function is used. To find the residue of $f$ at the singularity $z=i$, we write 
$$
f(z) = \frac{\phi(z)}{z-i} \quad \text{where} \quad \phi(z) = \frac{(\log z)^{3}}{z+i}
$$
The function $\phi(z)$ is clearly analytic at $z=i$; and, since 
$$
\phi(i) = \frac{(\log i)^{3}}{2i} = \frac{(\ln 1+ i \frac{\pi}{2})^{3}}{2i} = \frac{-\pi^{3}}{16}\neq0,
$$
$f$ has a simple pole there. The residue is 
$$
B = \phi(i) = \frac{-\pi^{3}}{16}
$$






