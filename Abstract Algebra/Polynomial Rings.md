---
tags:
  - polynomial
  - rings
  - factor
  - factor_rings
  - factorization
  - polynomial_rings
  - Math
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Polynomial Rings_
Applications: _None_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 2_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Introduction to Rings]],[[Factorization of Polynomials]]_
Cont.\_ of: _None_ 
_
_

###### Notation and Terminology
One of the mathematical concepts that people are most familiar with and most comfortable with is that of a polynomial. In high school, students study polynomials with integers coefficients, rational coefficients, or real coefficients, and perhaps, even complex coefficients. In earlier chapters of this book, we introduced something that was probably new$-$polynomials are rings and, in each case, the set of coefficients is also a ring. We shall abstract all of these concepts into one.

```ad-Definition
Let $R$ be a commutative ring. The set of formal symbols
$$
R[x] = \{a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots + a_{1}x + a_{0} \vert a_{i}\in R, \ \text{$n$ is a nonneegative integer}\}
$$
is called the _ring of polynomials over_ $R$ _in the indeterminate $x$_. Two elements 
$$
a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots + a_{1}x+a_{0}
$$
and 
$$
b_{m}x^{m}+b_{m-1}x^{m-1}+ \ldots + b_{1}x +b_{0}
$$
of $R[x]$ are considered equal if and only if $a_{i}=b_{i}$ for all nonnegatie integers $i$. (Define $a_{i}=0$ when $i>n$ and $b_{i}=0$ when $i>m$.)
```

In this definition, the symbols, $x,x^{2},\ldots,x^{n}$ do not represent "unknown" elements or variables from the ring $R$. Rather, their purpose is to serve as convenient placeholders that separate the rings elements $a_{n},a_{n-1},\ldots,a_{0}$. We could have avoided the $x$'s by defining a polynomial as in _infinite_ sequence $a_{0},a_{2},\ldots,a_{n},0,0,0,\ldots$, but our method takes advantage of the students experience in manipulating polynomials where $x$ does not represent a variable. The disadvantage of our method is that one must be careful not to confuse a polynomial with the function determined by a polynomial. For example, in $Z_{3}[x]$, the polynomials $f(x)=x^{3}+2x$ and $g(z) = x^{5}+2x$ determine the same function from $Z_{3}$ to $Z_{3}$ since $f(a)=g(a)$ for all $a$ in $Z_{3}$. But $f(x)$ and $g(x)$ are different elements of $Z_{3}[x]$. Also, in the ring $Z_{n}[x]$, be careful to reduce only the coefficients and not the exponents modulo $n$. For example, in $Z_{3}[x], 5x=2x$ but $x^{5}\neq x^{2}$. 

To make $R[x]$ into a ring, we define addition and multiplication in the usual way.

```ad-Definition
Let $R$ be a commutative ring and let 
$$
f(x) = a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots+a_{1}x+a_{0}
$$
and 
$$
g(x) = b_{m}x^{m}+b_{m-1}x^{m-1}+\ldots + b_{1}x + b_{0}
$$
belong to $R[x]$. Then 
$$
f(x)+g(x) = (a_{s}+b_{s})x^{s}+(a_{s-1}+b_{s-1}x^{s-1}+\ldots+(a_{1}+b_{1})a_{0}+b_{0}
$$
where $a_{i}=0$ for $i>n$ and $b_{i}=0$ for $i>m $. Also,
$$
f(x)g(x) = c_{m+n}x^{m+n}+c_{m+n-1}x^{m+n-1}+\ldots +c_{1}x + c_{0}
$$
where 
$$
c_{k}=a_{k}b_{0}+a_{k-1}b_{1}+\ldots + a_{1}b_{k-1}+a_{0}b_{k}
$$
for $k=0,\ldots,m+n$
```

Although the definition of multiplication might appear complicated, it is just a formalization of the familiar process of using the distributive property and collecting like terms. So, just multiply polynomials over a commutative ring $R$ in the same way that polynomials are always multiplied.

Our definitions for addition and multiplication of polynomials were formulated so that $R[x]$ is commutative and associative, and so that multiplication is distributive over addition. After all, $R[x]$ is called the "ring of polynomials over $R$." We leave the verification that $R[x]$ is a ring for later. 

It is time to introduce some terminology for polynomials. If 
$$
f(x) = a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots+a_{1}x+a_{0}
$$
where $a_{n}\neq 0$, we say that $f(x)$ has degree $n$; the term $a_{n}$ is called the _leading coefficient_ of $f(x)$; and, if the leading coefficient is the multiplicative identity element of $R$, we say that $f(x)$ is a _monic_ polynomial. Ver often properties of $R$ carry over to $R[x]$. Our first theorem is a case in point. 

**Theorem 18.1**  If $D$ is an integral domain, then $D[x]$ is an integral domain.

**Proof:**  Since we already know that $D[x]$ is a ring, all we need to show is that $D[x]$ is commutative with a unity and has no zero-divisors. Clearly, $D[x]$ is commutative whenever $D$ is. If $1$ is the unity element of $D$ it is easy to check that $f(x)=1$ is the unity element of $D[x]$. Finally, suppose that 
$$
f(x) = a_{n}x^{n}+a_{n-1}x^{n-1}+\ldots+a_{0}
$$
and 
$$
g(x) = b_{m}x^{m}+b_{m-1}x^{m-1}+\ldots+b_{0}
$$
where $a_{n}\neq 0$ and $b_{m} \neq 0$. Then, by definition, $f(x)g(x)$ has leading coefficient $a_{n}b_{m}$ and since $D$ is a integral domain, $a_{n}b_{m}\neq 0$. 

#### The Division Algorithm and Consequences
One of the properties of integers that we have used repeatedly is the division algorithm: if $a$ and $b$ are integers and $b \neq 0$, then there exists unique integers $q$ and $r$ such that $a=bq+r$ where $0 \leq r < |b|$. The next theorem is the analogous statement for polynomials over a field. 

**Theorem 18.2**  Let $F$ be a field and let $f(x)$ and $g(x) \in F[x]$ with $g(x)\neq 0$. Then there exists unique polynomials $q(x)$ and $r(x)$ such that $f(x)=g(x)q(x)+r(x)$ and either $r(x)=0$ or $\deg r(x) < \deg g(x)$. 

**Proof:**  The proof is quite complicated, so we leave it to be read on page 236 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

Let $D$ be an integral domain. If $f(x)$ and $g(x)$ $\in D[x]$, we say that $g(x)$ _divides_ $f(x)$ in $D[x]$ (and write $g(x) \vert f(x)$) if there exists an $h(x) \in D[x]$ such that $f(x)=g(x)h(x)$. In this case, we also call $g(x)$ a _factor_ of $f(x)$. An element $a$ is a _zero_ (or _root_) of a polynomial $f(x)$ if $f(a)=0$. When $F$ is a field, $a\in F$ and $f(x) \in F[x]$, we say $a$ is a _zero of multiplicity $k$_ if $(x-a)^{k}$ is a factor of $f(x)$, but $(x-a)^{k+1}$ is not a factor of $f(x)$. With these definition, we may now give several important corollaries of the Division Algorithm. All proofs will be omitted and can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]].

**Corollary 1.**  Let $F$ be a field, $a \in F$, and $f(x) \in F[x]$. Then $f(a)$ is the remainder in the division of $f(x)$ by $x-a$. 

**Corollary 2.**  Let $F$ be a field, $a \in F$, and $f(x)\in F[x]$. Then $a$ is a zero of $f(x)$ if and only if $x-a$ is a factor of $f(x)$. 

**Corollary 3.**  A polynomial of degree $n$ _over a field_ has at most $n$ zeros counting multiplicity.

**Remark.**  We remark that Corollary 3 is not true for arbitrary polynomial rings. For example, the polynomial $x^{2}+3x+2$ has four zeros in $Z_{6}$. Lagrange was the first to prove Corollary 3 for polynomials in $Z_{p}[x]$. 

We shall conclude with an important theoretical application of the Division Algorithm, but first an important definition. 

```ad-Definition
A principle ideal domain is an integral domain $R$ in which every ideal has the form $\left<a \right>=\{ra \vert \ r\in R\}$ for some $a$ in $R$. 
```

**Theorem 18.3**  Let $F$ be a field. Then $F[x]$ is a principle ideal domain. 

**Proof:**  The proof will be provided along with the next proof on page 239 in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

**Theorem 18.4**  Let $F$ be a field, $I$ an ideal in $F[x]$, and $g(x)$ an element of $F[x]$. Then, $I = \left<g(x) \right>$ iff $g(x)$ is a nonzero polynomial of minimum degree in $I$. 


