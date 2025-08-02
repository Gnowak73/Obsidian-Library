---
tags:
  - factorization
  - polynomial
  - Math
  - ring
  - rings
  - factor
  - eisenstein
  - irreducibility
  - reducibility
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Factorization of Polynomials_
Applications: _None_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 2_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Polynomial Rings]],[[Introduction to Rings]],[[Integral Domains]]_
Cont.\_ of: _None_ 
_
_

Because of the precedingly cumbersome proof, we shall leave all proofs in this article in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 
##### Reducibility Tests
In high school, students spend much time factoring polynomials and finding their roots. In this chapter, we consider the same problems in a more abstract setting. To discuss factorization of polynomials, we must first introduce the polynomial analog of a prime devisor. 

```ad-Definition
Let $D$ be an [[Integral Domains|integral domain]]. A polynomial $f(x)$ from $D[x]$ that is neither the zero polynomial nor a unit in $D[x]$ is said to be _irreducible over $D$_ if, whenever $f(x)$ is expressed as a product $f(x)=g(x)h(x)$ with $g(x)$ and $h(x)$ from $D[x]$, then $g(x)$ or $h(X)$ is a unit in $D[x]$. A nonzero, nonunit element of $D[x]$ that is not irreducible over $D$ is called _reducible_ over $D$. 
```

Note that in the case that $D$ is a field, a nonconstant $f(x) \in D[x]$ is irreducible over $D$ if and only if $f(x)$ cannot be expressed as a product of two polynomials in $D[x]$ of lower degree. 

In general, it is a difficult problem to decide whether or not a particular polynomial is reducible over an integral domain but there are special cases when it is easy. Our first theorem is a case in point. It applies to the three preceding examples.

---
**Theorem 19.1**  Let $F$ be a field. If $f(x) \in F[x]$ and $\deg f(x)=2$ or $3$, then $f(x)$ is reducible over $F$ if and only if $f(x)$ has a zero in $F$. 

---
Theorem 19.1 is particularly easy to use when the field is $Z_{p}$ for, in this case, we can check for reducibility of $f(x)$ by simply testing to see if $f(x)=0$ for $x=0,1,\ldots,p-1$. 

Note that polynomials of degree larger than $3$ may be reducible over a field, even though they do not have zeros in the field. For example, in $Q[x]$, the polynomial $x^{4}+2x^{2}+1=(x^{2}+1)^{2}$, but has no zeros in $Q$. 

Our next three tests deal with polynomials with integer coefficients. To simplify the proof of the first of the these, we introduce some terminology and isolate a portion of the argument in the form of a lemma. 

```ad-Definition
The _content_ of a polynomial $a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots+a_{0}$ where the $a$'s are integers is the greatest common divisor of the integers $a_{n},a_{n-1},\ldots,a_{0}$. A _primitive polynomial_ is an element of $Z[x]$ with content 1.
```

**Gauss's Lemma.**  The product of two primitive polynomials is primitive. 

Remember that the question of reducibility depends on which ring of coefficients one permits. Thus, $x^{2}-2$ is irreducible over $Z$ but reducible over $Q[\sqrt{2}]$. Later on, we will prove every polynomial of degree greater than $1$ with coefficients from an integral domain is reducible over some field. Theorem 19.2 shows that in the case of the integers, this field _must be_ larger than the field of rational numbers. 

**Theorem 19.2**  Let $f(x)\in Z[x]$. If $f(x)$ is reducible over $Q$, then it is reducible over $Z$. 

##### Irreducibility Tests
Theorem 19.1 reduces the question of irreducibility of a polynomial of degree 2 or 3 to one of finding a zero. The next theorem often allows us to simplify the problem even further. 

**Theorem 19.3**  Let $p$ be a prime and suppose $f(x) \in Z[x]$ with $\deg f(x) \geq 1$. Let $\overline{f(x)}$ be the polynomial in $Z_{p}[x]$ obtained from $f(x)$ by reducing all the coefficients of $f(x)$ modulo $p$. If $\overline{f(x)}$ is irreducible over $Z_{p}$ and $\deg \overline{f(x)} = \deg f(x)$, then $f(x)$ is irreducible over $Q$. 

**Remark.**  Be cautious not to use the converse of this theorem. If $f(x) \in Z[x]$ and $\overline{f(x)}$ is reducible over $Z_{p}$ for some $p$, $f(x)$ may still be irreducible over $Q$. The Mod $p$ irreducibility test can also be helpful in checking for irreducibility of polynomials of degree greater than $3$ and polynomials with rational coefficients. 

---
Another important irreducibility test is the following one, credited to Ferdinand Eisenstein, a student of Gauss. 

**Theorem 19.4**  Let $f(x) = a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots+a_{0} \in Z[x]$. If there is a prime $p$ such that $p \ \not{\vert} \ a_{n},\ p \ \vert \ a_{n-1},\ldots, \ p \ \vert \ a_{0}$ and $p^{2} \ \not{\vert} \ a_{0}$, then $f(x)$ is irreducible over $Q$. 

**Corollary.**  For any prime $p$, the $p$th cyclotomic polynomial 
$$\Phi_{p}(x) = \frac{x^{p}-1}{x-1} = x^{p-1}+x^{p-2}+\ldots + x + 1$$ is irreducible over $Q$. 

The principle reason for our interest in irreducible polynomials stems from the fact that there is an intimate connection between them, maximal ideas, and fields. This connection is revealed in the next theorem and its first corollary. 

**Theorem 19.5**  Let $F$ be a field and let $p(x) \in F[x]$. Then $\left<p(x) \right>$ is a maximal ideal in $F[x]$ if and only if $p(x)$ is irreducible over $F$. 

**Corollary 1.**  Let $F$ be a field and $p(x)$ an irreducible polynomial over $F$. Then $\frac{F[x]}{\left<p(x)\right>}$ is a field. 

The next corollary is a polynomial analog of Euclid's Lemma in [[Properties of Integers, Algebra, and Functions]]. 

**Corollary 2.**  Let $F$ be a field and let $p(x), a(x), b(x) \in F[x]$. If $p(x)$ is irreducible over $F$ and $p(x) \ \vert \ a(x)b(x)$, then $p(x) \ \vert \ a(x)$ or $p(x) \ \vert \ b(x)$. 

#### Unique Factorization in $Z[x]$ 
As a further application of the ideas presented before, we next show that $Z[x]$ has an important factorization property. Later on, we will show that every principle ideal domain has the same factorization property. The case $Z[x]$ is handled separately because it is not a principle ideal domain. The first proof of Theorem 19.6 was given by Gauss. In the following theorem and its proof, keep in mind that the units in $Z[x]$ are precisely $f(x)=1$ and $f(x)=-1$, and every polynomial from $Z[x]$ that is irreducible over $Z$ is primitive. 

**Theorem 19.6**  Every polynomial in $Z[x]$ that is not the zero polynomial or a unit in $Z[x]$ can be written in the form $b_{1}b_{2}\ldots b_{s}p_{1}(x) \ldots p_{m}(x)$ where the $b$'s are prime (that is, irreducible polynomials of degree $0$), and the $p_{i}(x)$'s are irreducible polynomials of positive degree. Furthermore, if 
$$
b_{1}b_{2}\ldots b_{s}p_{1}(x)p_{2}(x) \ldots p_{m}(x) = c_{1}c_{2}\ldots c_{t}q_{1}(x)q_{2}(x) \ldots q_{n}(x)
$$
where the $b$'s and $c$'s are irreducible polynomials of degree $0$, and the $p(x)$'s and $q(x)$'s are irreducible polynomials of positive degree, then $s=t$, $m=n$, and, after renumbering the $c$'s and $q(x)$'s, we have $b_{i} = \pm c_{i}$ for $i=1,\ldots,s$; and $p_{i}(x) = \pm q_{i}(x)$ for $i=1,\ldots,m$. 

