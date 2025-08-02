---
tags:
  - integral_domain
  - domain
  - domains
  - division
  - irreducibility
  - irreducibles
  - prime_ideals
  - primes
  - factorization
  - Math
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Divisibility in Integral Domains_
Applications: _None_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _None_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Introduction to Rings]],[[Factorization of Polynomials]],[[Integral Domains]]_
Cont.\_ of: _None_ 
_
_

##### Irreducibles, Primes 
In previous discussion, we focused on factoring polynomials over the integers or a field. Several of those results, unique factorization in $Z[x]$ and the division algorithm for $F[x]$, for instance, are natural counterparts to theorems about the integers. In this chapter and the next, we examine factoring in a more abstract setting. 

```ad-Definition
Elements $a$ and $b$ of an integral domain $D$ are called _associates_ if $a=ub$ where $u$ is a unit of $D$. A nonzero element $a$ of an integral domain $D$ is called _irreducible_ if $a$ is not a unit and, whenever $b,c \in D$ with $a=bc$, then $b$ or $c$ is a unit. A nonzero element $a$ of an integral domain $D$ is called _prime_ if $a$ is not a unit and $a \ \vert \ bc$ implies $a \ \vert \ b$ or $a \ \vert \ c$. 
```

Roughly speaking, an irreducible is an element that can be factored only in a trivial way. Notice that an element $a$ is prime if and only if $\left<a \right>$ is a prime ideal. 

Relating the above definition to the integers may seem a bit confusing since we defined an integer to be prime if it satisfies our definition of an irreducible, and we proved a prime integers satisfies the definition of a prime in an integral domain (Euclid's Lemma). the course of the confusion is that, in the case of the integers, the concepts of irreducible and prime are equivalent but, as we will soon see, in general, they are not. 

The distinction between primes and irreducibles is best illustrated by integral domains of the form $Z[{\sqrt{d}}] = \{ a + b \sqrt{d} \ \vert \ a,b \in Z \}$ where $d$ is not $1$ and is not divisible by the square of a prime. (These rings are of fundamental important in number theory.) To analyze these rings, we need a convenient method of determining their units, irreducibles, and primes. to do this, we define a function $N$, called the _norm_, from $Z[\sqrt{d}]$ into the nonnegative integers by $N(a+b\sqrt{d}) = |a^{2}-db^{2}|$. This satisfies the following four properties: $N(x) = 0$ if and only if $x=0$; $N(xy)=N(x)N(y)$ for all $x$ and $y$; $x$ is a unit if and only if $N(x)=1$; and, if $N(x)$ is prime in $Z$, then $x$ is irreducible in $Z[\sqrt{d}]$ (ONLY WORKS IF $xy \neq 0$!). 

**Theorem 20.1**  In an integral domain, every prime is irreducible.

**Proof:**  Suppose $a$ is a prime in an integral domain and $a=bc$. We must show that $b$ or $c$ is a unit. By definition of prime, we know $a \ \vert \ b$ or $a \ \vert \ c$. Say, $at=b$. Then $b \cdot 1 = b = at = (bc)t = b(ct)$ and, by cancellation, $1=ct$. Thus, $c$ is a unit. 

Recall that a principle ideal domain is an [[Integral Domains|integral domain]] in which every ideal has the form $\left<a \right>$. The next theorem reveals a circumstance in which primes and irreducible are equivalent.

**Theorem 20.2**  In a principle ideal domain, an element is irreducible if and only if it is prime. 

**Proof:**  The proof can be seen in Chapter 20 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]].

It is an easy consequence of the respective division algorithms for $Z$ and $F[x]$, where $F$ is a field, that $Z$ and $F[x]$ are principle ideal domains (see more online or in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|asbtract algebra textbook]]. However, note that $Z[x]$ is **not** a principle ideal domain. 

We have previously proved that the integral domains $Z$ and $Z[x]$ have important factorization properties: every integer greater than $1$ can be uniquely factored as a product of irreducibles (that is, primes), and every nonzero, nonunit polynomial can be uniquely factored as a product of irreducible polynomials. It is natural to ask whether all integral domains have this property. The question of unique factorization in integral domains first arose with the efforts to solve a famous problems that goes by the misnomer Fermat's Last Theorem. 

##### Unique Factorization Domains 
We now have the necessary terminology to formalize the idea of unique factorization. 

```ad-Definition
An integral domain $D$ is a _unique factorization domain_ if 
1. every nonzero element of $D$ that is not a unit can be written as a product of irreducibles of $D$, and 
2. the factorization into irreducibles is unique up to associates and the order in which the factors appear. 
```

Another way to formulate part 2 of this definition is the following. If $p_{1}^{n_{1}}p_{2}^{n_{2}}\ldots p_{r}^{n_{r}}$ and $q_{1}^{m_{1}}q_{2}^{m_{2}}\ldots q_{s}^{m_{s}}$ are two factorizations of some element as a product of irreducibles, where none of the $p_{i}$'s are associates and none of the $q_{j}$'s are associates, then $r=s$, and each $p_{i}^{n_{i}}$ is an associate of one and only one $q_{j}^{m_{j}}$. 

Of course, the Fundamental Theorem of Arithmetic tells us that the ring of integers is a unique factorization domain and Theorem 19.6 says that $Z[x]$ is a unique factorization domain. In fact, as we shall soon see, most of the integral domains we have encountered are unique factorization domains.

Before looking at our next theorem, we need the ascending chain condition for ideals.

**Lemma**   In a principle ideal domain, any strict increasing chain of ideals $I_{1} \subset I_{2} \subset \ldots$ must be finite in length.

**Proof:**  The proof can be seen in Chapter 20 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

**Theorem 20.3**  Every principle ideal domain is a unique factorization domain.

**Proof:**  The proof is too cumbersome to present here, see page 265 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

In the existence portion of the proof of Theorem 20.3, the only way we used the fact that the integral domain $D$ is a principal ideal domain way to say that $D$ has the property that there is no infinite, strictly increasing chain of ideals in $D$. An integral domain with this property is called a _Noetherian domain_, in honor of Emmy Noether, who inaugurated the use of chain conditions in algebra. Noetherian domains are of the utmost importance in algebraic geometry. One reason for thsi is that, for many important rings $R$, the polynomial ring $R[x]$ is a Noetherian domain, but not a principle ideal domain. One such example is $Z[x]$. In particular, $Z[x]$ shows that a UFD need not be a PID. As an immediate corollary of Theorem 20.3, we have the following fact. 

**Corollary.**  Let $F$ be a field. Then $F[x]$ is a unique factorization domain.

**Proof:**  Can be seen in the textbook. 

##### Euclidean Domains
Another important kind of integral domain is a Euclidean domain.

```ad-Definition
An integral domain $D$ is called a _Euclidean domain_ if there is a function $d$ from the nonzero elements of $D$ to the nonnegative integers such that 
1. $d(a) \leq d(ab)$ for all nonzero $a,b$ in $D$; and 
2. if $a,b \in D, b\neq 0$, then there exist elements $q$ and $r$ in $D$ such that $a=bq+r$ where $r=0$ or $d(r)<d(b)$.
```

See that by this definition, a Euclidean Domain is an integral domain with a **division algorithm**. Note that there is a remarkable similarity between the ring of integers and the ring of polynomials over a field.

![[Pasted image 20231205203858.png|center]]


**Theorem 20.4:**  Every Euclidean domain is a principle ideal domain.

**Proof:**  Can be seen in the textbook. 


And as an immediate consequence of Theorems 20.3 and 20.4, we have the following important result.

**Corollary.**  Every Euclidean domain is a unique factorization domain. 

We may summarize our theorems and remarks as follows: 

![[Pasted image 20231205204125.png|center]]

Now, let us make a generalization in our next theorem from our original discovery that $Z[x]$ is a unique factorization domain and $Z$ is a unique factorization domain.

**Theorem 20.5**  If $D$ is a unique factorization domain, then $D[x]$ is a unique factorization. 

