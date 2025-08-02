---
tags:
  - rings
  - Math
  - group
  - groups
  - ring
  - subring
  - unity
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Rings_
Applications: _Symmetries and Geometries_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 2_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[Integral Domains]],[[Ideals and Factor Rings]],[[Ring Homomorphisms]],[[Polynomial Rings]],[[Factorization of Polynomials]],[[Divisibility in Integral Domains]]_
Cont.\_ of: _None_ 
_
_

Many sets are naturally endowed with two binary operations: addition and multiplication. Examples that quickly come to mind are the integers, the integers modulo $n$, the real numbers, matrices, and polynomials. When considering these sets as groups, we simply used addition and ignored multiplication. In many instances, however, one wishes to take into account both addition and multiplication. One abstract concept that does this is a ring. This notion was originated in the mid-nineteenth century by Richard Dedekind. 

```ad-Definition
A ring $R$ is a set with two binary operations, addition $a+b$ and multiplication $ab$ such that for all $a,b,c \in R$ 
1. $a+b=b+a$
2. $(a+b)+c=a+(b+c)$
3. There is an element $0$ in $R$ such that $a+0=a$
4. There is an element $-a$ in $R$ such that $a+(-a)=0$
5. $a(bc)=(ab)c$
6. $a(b+c)=ab+ac$ and $(b+c)a=ba+ca$
```

**Remark.**  So, a ring is an Abelian group under addition, also having an associative multiplication that is left and right distributive over addition. Note that multiplication need not be commutative. When it is, we say that the ring is **commutative**. Also, a ring need not have an identity under multiplication. When a ring other than $\{0\}$ has an identity under multiplication, we say that the ring has a **unity** (or _identity_). A nonzero element of a commutative ring with unity need not have a multiplicative inverse. When it does, we say it is a _unit_ of the ring. Thus, $a$ is a unit if $a^{-1}$ exists. 

**Remark.**  By definition, the identity is defined such that $r=1r=r1$.

The following terminology and notation is convenient. If $a$ and $b$ belong to a commutative ring $R$ and $a$ is nonzero, we say that $a$ divides $b$ (or $a$ is a _factor_ of $b$) and write $a \vert \ b$, if there exists an element $c$ in $R$ such that $b=ac$. If $a$ does not divide $b$, we write $a \not{\vert} \ b$.

For an abstraction to be worthy of study, it must have many diverse concrete realizations. There are many examples that show the concept of a ring is pervasive. These examples can be seen on page 188 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

### Properties of Rings
Let us first show how the operations of addition and multiplication intertwine. 

**Theorem 14.1**  Let $a,b,c$ belong to a ring $R$. Then 
1. $a0=0a=0$
2. $a(-b)=(-a)b=-(ab)$
3. $(-a)(-b)=ab$
4. $a(b-c)=ab-ac$ and $(b-c)a=ba-ca$
Furthermore, if $R$ has a unity element $1$ then 
5. $(-1)a=-a$
6. $(-1)(-1)=1$

**Proof:**  The proofs can be seen in Page 193 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. However, most of these proofs are quite trivial. 

Recall that in the case of groups, the identity and the inverses are unique. What about rings? The same is true for rings, provided they exist. The proofs are identity to the ones given for groups are so we will omit them.

**Theorem 14.2**  If a ring has a unity, it is unique. If a ring element has an inverse, it is unique. 

```ad-Remember
Many have the mistaken tendency to treat rings as if it were a group under _multiplication_. It is not. The two most common errors are to assume ring elements have multiplicative inverses$-$they need not, and that a ring has a multiplicative identity$-$it need not. For example, if $a,b,c$ belong to a ring, $a\neq 0$ and $ab=ac$, we _cannot_ conclude that $b=c$. Similarly, if $a^{2}=a$, we _cannot_ conclude that $a=0$ or $a=1$. In the first place, the ring need not have multiplicative cancellation, and in the second place, the ring need not have a multiplicative identity. There is however an important class of rings where a multiplicative identity exists and multiplicative cancellation holds.
```

##### Subrings
In our study of [[Groups]], [[Finite Groups, Subgroups|subgroups]] played a crucial role. Subrings, the analogous idea in ring theory, play a much less important role than their counterparts in group theory. Nevertheless, subrings are important.

```ad-Definition
A subset $S$ of a ring $R$ is a _subring_ of $R$ is $S$ is itself a ring with the operations of $R$. 
```

Just as was the case for subgroups, there is a simple test for subrings. 

**Theorem 14.3**  A nonempty subset $S$ of a ring $R$ is a subring if $S$ is _closed under subtraction and multiplication_; that is, if $a-b$ and $ab$ are in $S$ whenever $a$ and $b$ are in $S$. 

**Proof:**  Since addition in $R$ is commutative and $S$ is closed under subtraction, we know by the one-step subgroup test (Theorem 3.1 in [[Finite Groups, Subgroups]]) that $S$ is an Abelian group under addition. Also, since multiplication in $R$ is associative as well as distributive over addition, the same is true for multiplication in $S$. Thus, the only condition remaining to check is that multiplication is a binary operation on $S$. But this is exactly what closure means. 