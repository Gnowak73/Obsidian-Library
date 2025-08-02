---
tags:
  - Math
  - topology
  - Set
  - sets
dg-publish: true
mathLink:
---
Subject: _Real Analysis, Topology, Mathematical Analysis_
Main\_Topic: _Basic Topology_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Principles of Mathematical Analysis.pdf]]_
Closely\_Related\_To: _[[Countable Base]],[[Hausdorff]],[[Manifolds]],[[Submanifolds]],[[Properties of Integers, Algebra, and Functions]]_
Cont.\_ of: _[[Countable Base]],[[Hausdorff]]_ 
_
_

We begin with a definition of the function concept.
#### Mappings 
```ad-Definition
Consider two sets $A$ and $B$, whose elements may be any objects whatsoever, and suppose that with each element $x$ of $A$ there is associated, in some manner, an element of $B$, which we denote by $f(x)$. Then, $f$ is said to be a _function_ from $A$ to $B$ (or a _mapping_ of $A$ into $B$). The set $A$ is called the _domain_ of $f$ (we also say $f$ is defined on $A$), and the elements $f(x)$ are called the _values_ of $f$. The set of all values of $f$ is called the _range_ of $f$. 
```

```ad-Definition
Let $A$ and $B$ be two sets and let $f$ be a mapping of $A$ into $B$. If $E \subset A$, $f(E)$ is defined to be the set of all elements $f(x)$, for $x \in E$. We call $f(E)$ the _image_ of $E$ under $f$. In this notation, $f(A)$ is the range of $f$. It is clear that $f(A) \subset B$. If $f(A)=B$, we say that $f$ maps $A$ _onto_ $B$. (Note that _onto_ is more specific than _into_).

If $E \subset B, f^{-1}(E)$ denotes the set of all $x\in A$ such that $f(x) \in E$. We call $f^{-1}(E)$ the _inverse image_ of $E$ under $f$. If $y \in B, f^{-1}(y)$ is the set of all $x \in A$ such that $f(x)=y$. If, for each $y \in B, f^{-1}(y)$ consists of at most one element of $A$, then $f$ is said to be a 1-1 (one-to-one) mapping of $A$ into $B$. 
```

##### Equivalence
```ad-Definition
If there exists a 1-1 mapping of $A$ _onto_ $B$, we say that $A$ and $B$ can be put in 1-1 _correspondence_, or that $A$ and $B$ have the same _cardinal number_, or briefly, that $A$ and $B$ are _equivalent_, and we write $A \sim B$. This relation clearly has the following properties:

1. It is reflexive: $A \sim A$
2. It is symmetric: If $A \sim B$, then $B \sim A$
3. It is transitive: If $A \sim B$ and $B \sim C$, then $A \sim C$

Any relation with these three properties is called an _equivalence relation_ (other article: [[Properties of Integers, Algebra, and Functions#Equivalence Relations|Equivalence Relations in Abstract Algebra]]).
```

##### Countable and Finite Sets 
```ad-Definition
For any positive integer $n$, let $J_{n}$ be the set whose elements are the integers $1,2,\ldots,n$; let $J$ be the set consisting of all positive integers. For any set $A$, we say:

1. $A$ if _finite_ if $A \sim J_{n}$ for some $n$(the empty set is also considered to be finite).
2. $A$ is _infinite_ if $A$ is not finite.
3. $A$ is _countable_ is $A \sim J$.
4. $A$ is _uncountable_ if $A$ is neither finite nor countable.
5. $A$ is at _most countable_ if $A$ is finite or countable 

Countable sets are sometimes called _enumerable_, or _denumerable_. For two finite sets $A$ and $B$, we evidently have $A \sim B$ if and ony if $A$ and $B$ contain the same number of elements. For infinite sets, however, the idea of "having the same elements" becomes quite vague, whereas the notion of 1-1 correspondence retains its clarity.
```

**Remark.**  A finite set cannot be equivalent to one of its proper subsets. That this is however, possible for infinite sets. In fact, we could replace the definition in (2) by the statement: $A$ is infinite if $A$ is equivalent to one of its proper subsets. 

##### Sequences
```ad-Definition
By a _sequence_, we mean a function $f$ defined on the set $J$ of all positive integers. If $f(n)=x_{n}$, for $n \in J$, it is customary to denote the sequence $f$ by the symbol $\{x_{n}\}$, or sometimes by $x_{1},x_{2},x_{3},\ldots$. The values of $f$, that is, the elements $x_{n}$, are called the _terms_ of the sequence. If $A$ is a set and if $x_{n}\in A$ for all $n \in J$, then $\{x_{n}\}$ is said to be a _sequence_ in $A$, or a _sequence of elements_ of $A$.  
```

Note that the terms $x_{1},x_{2},x_{3}\ldots$ of a sequence need not be distinct. Since every countable set is the range of a 1-1 function defined on $J$, we may regard every countable set as the range of a sequence of distinct terms. Speaking more loosely, we may say that the elements of any countable set can be "arranged in a sequence". 

Sometimes it is convenient to replace $J$ in this definition by the set of all nonnegative integers, i.e., to start with $0$ rather than with $1$. 

###### Infinite Subset of Countable Set is Countable
**Theorem 2.8.**  Every _infinite subset_ of a countable set $A$ is countable. 

**Proof:**  Suppose that $E \subset A$, and $E$ is infinite. Arrange the element $x$ of $A$ in a sequence $\{x_{n}\}$ of distinct elements. Construct a sequence $\{n_{k}\}$ as follows: 

Let $n_{1}$ be the smallest positive integer such that $x_{n_{1}} \in E$. Having chosen $n_{1},\ldots,n_{k-1}$, let $n_{k}$ be the smallest integer greater than $n_{k-1}$ such that $x_{n_{k}} \in E$. Putting $f(k)=x_{n_{k}}(k=1,2,3,\ldots)$, we obtain a 1-1 correspondence between $E$ and $J$. 

The theorem shows that, roughly speaking, countable sets represent the "smallest" infinity: No uncountable set can be a subset of a countable set. 

##### Union and Intersection of Sets
```ad-Definition
Let $A$ and $\Omega$ be sets, and uppose that with each element $\alpha$ of $A$ there is associated a subset of $\Omega$ which we denote by $E_{\alpha}$. 

The set whose elements are the sets $E_{\alpha}$ will be denoted by $\{E_{\alpha}\}$. Instead of speaking of sets of sets, we shall sometimes speak of a collection of sets, or a family of sets. 

The _union_ of the sets $E_{\alpha}$ is defined to be the set $S$ such that $x \in S$ if and only if $x \in E_{\alpha}$ for at least one $\alpha \in A$. We use the notation
$$
S = \bigcup_{\alpha \in A} E_{\alpha}
$$
If $A$ consists of the integers $1,2,\ldots,n$, one usually writes 
$$
S = \bigcup_{m=1}^{n} E_{m}
$$
or 
$$
S = E_{1} \cup E_{2} \cup \ldots \cup E_{n}.
$$
If $A$ is the set of all positive integers, the usual notation is 
$$
S = \bigcup_{m=1}^{\infty}E_{m}
$$
```

**Remark.**  The symbol $\infty$ merely indicated that the union of a _countable_ collection of sets is taken, and should not be confused with the symbols $+\infty$ or $-\infty$. 

```ad-Definition
The _intersection_ of the sets $E_{\alpha}$ is defined to be the set $P$ such that $x \in P$ if and only if $x \in E_{\alpha}$ for every $\alpha \in A$. We use the notation 
$$
P = \bigcap_{\alpha \in A} E_{\alpha},
$$
or 
$$
P = \bigcap_{m=1}^{n}E_{m} = E_{1} \cap E_{2} \cap \ldots \cap E_{n}
$$
or 
$$
P = \bigcap_{m=1}^{\infty} E_{m} 
$$
as for unions. If $A \cap B$ is not empty, we say that $A$ and $B$ _intersect_; otherwise, they are _disjoint_. 
```

**Remark.**  Many properties of unions and intersections are quite similar to those of sums and products; in fact, the  words sum and product were sometimes used in connection, and the symbols $\sum\limits$ and $\Pi$ were written in place of $\cup$ and $\cap$. 

The commutative and associative laws are trivial:
$$
A \cup B = B \cup A; \quad A \cap B = B \cap A.
$$
$$
(A \cup B) \cup C = A \cup (B \cup C); \quad (A \cap B) \cap C = A \cap (B \cap C)
$$

Thus, the omission of parenthesis is justified. The distributive law also holds:
$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C)
$$
**Proof:**  To prove this let the left and right members be denoted by $E$ and $F$, respectively. 

Suppose that $x \in E$. Then $x \in A$ and $x \in B \cup C$, that is, $x \in B$ or $x \in C$ (possible both). Hence, $x \in A \cap B$ or $x \in A \cap C$, so that $x \in F$. Thus $E \subset F$. 

Next, suppose that $x \in F$. Then $x \in A \cap B$ or $x \in A\cap C$. That is, $x \in A$, and $x \in B \cup C$. Hence $x \in A \cap (B \cup C)$, so that $F \subset E$. 

It follows that $E=F$. 

---
We list a few more relations which are easily verified:
$$
\begin{gathered}
A \subset A \cup B \\
A \cap B \subset A
\end{gathered}
$$
If $0$ denotes the empty set, then 
$$
A \cup 0 = A, \quad A \cap 0 = 0.
$$
If $A \subset B$, then
$$
A \cup B = B, \quad A \cap B = A
$$

###### Sequence of Countable Sets is Countable
**Theorem 2.12.**  Let $\{E_{n}\}, \ n=1,2,3,\ldots$ be a _sequence of countable sets_, and put 
$$
S = \bigcup_{n=1}^{\infty}E_{n}
$$
Then $S$ is countable. 

**Proof:**  Let every set $E_{n}$ be arranged in a sequence $\{x_{nk}\},k=1,2,3,\ldots$ and consider the infinite array 

![[Pasted image 20230909202904.png|center]]

in which elements of $E_{n}$ form the $n$th row. The array contains all elements of $S$. As indicated by the arrows, these elements can be arranged in a sequence
$$
x_{11}; \ x_{12},x_{12}; \
 x_{31},x_{22},x_{13};\ldots
$$
If any two of the sets $E_{n}$ have elements in common, these will appear more than once in the sequence. Hence there is a subset $T$ of the set of all positive integers such that $S \sim T$, which shows that $S$ is at most countable (Theorem 2.8). Since $E_{1} \subset S$, and $E_{1}$ is infinite, $S$ is infinite, and thus countable. 

**Corollary.**  Suppose $A$ is at most countable, and, for every $\alpha \in A, B_{\alpha}$ is at most countable. Put 
$$
T = \bigcup_{\alpha \in A} B_{\alpha}
$$
then $T$ is at most countable. 

**Proof:**  $T$ is equivalent to a subset to $S$ in Theorem 1.12.

###### N-Tuples of Countable Sets is Countable

**Theorem 2.13.**  let $A$ be a countable set, and let $B_{n}$ be the set of all n-tuples $(a_{1},a_{2},\ldots,a_{n})$, where $a_{k} \in A(k=1,\ldots,n)$, and the elements $a_{1},\ldots,a_{n}$ need not be distinct. Then $B_{n}$ is countable.

**Proof:**  That $B_{1}$ is countable is evident, since $B_{1}=A$. Suppose that $B_{n-1}$ is countable $(n=2,3,4,\ldots)$. The elements of $B_{n}$ are of the form 
$$
(b,a) \quad (b \in B_{n-1}, a \in A)
$$
For every fixed $b$, the set of pairs $(b,a)$ is equivalent to $A$, and hence countable. Thus, $B_{n}$ is the union of a countable at of countable sets. By theorem 2.12, $B_{n}$ is countable. 


**Corollary.**  The set of all rational numbers is countable. 

**Proof:**  We apply Theorem 2.13, with $n=2$, noting that every rational $r$ is of the form $\frac{b}{a}$, where $a$ and $b$ are integers. The set of pairs $(a,b)$ and therefore the set of fractions $\frac{b}{a}$, is countable. We can show that $Q \sim B_{2}$, and $B_{2} \sim J$, so $Q \sim J$. 

**Remark.**  In fact, even the set of all algebraic numbers is countable. Not all infinite are, however, countable, is shown by the next theorem.

###### Set of Sequences Whose Elements are 0 and 1
**Theorem 2.14.**  let $A$ be the set of all sequences whose elements are the digits $0$ and $1$. This set $A$ is uncountable.

**Proof:**  Let $E$ be a countable subset of $A$, and let $E$ consist of the sequences $s_{1},s_{2},\ldots$. We construct a sequence $s$ as follows. If the $n$th digit in $s_{n}$ is $1$, we let the $n$th digit of $s$ be $0$, and vise versa. Then the sequence $s$ differs from every member of $E$ in at least one place; hence $s \notin E$. But clearly $s \in A$, so that $E$ is a proper subset of $A$. 

We have shown that every countable subset of $A$ is a proper subset of $A$. It follows that $A$ is uncountable (for otherwise $A$ would be a proper subset of $A$, which is absurd).  

```ad-warning
We **CANNOT** use Theorem 2.12 for this problem. The notation for 
$$\bigcup^{\infty}_{n=1}
$$
is the union of a countable collection of sets. **BUT**, only a finite union of infinite sets, **NOT** an infinite union of infinite sets. In this problem, we would have an infinite number of countable sets since there are an infinite number of ways to arrange $0$ and $1$ in a sequence. Therefore, we must employ other methods!
```

### Metric Spaces

```ad-Definition
A set $X$, whose elements we shall call _points_, is said to be a _metric space_ if with any two points $p$ and $q$ of $X$ there is associated a real number $d(p,q)$, called the _distance_ from $p$ to $q$, such that 
1. $d(p,q)>0$ if $p\neq q; d(p,p)=0$;
2. $d(p,q)=d(q,p)$;
3. $d(p,q)\leq d(p,r)+d(r,p)$, for any $r \in X$. 

Any function with these three properties is called a _distance function_, or a _metric_. 
```

**Remark.**  The most important examples of metric spaces, from our standpoint, are the Euclidean spaces $R^{k}$, especially $R^{1}$(the real line) and $R^{2}$ (the complex plane); the distance in $R^{k}$ is defined by 
$$
d(\bf{x},\bf{y}) = |\bf{x}-\bf{y}| \quad (\bf{x},\bf{y} \in R^{k})
$$
It is important to observe that every subset $Y$ of a metric space $X$ is a metric space in its own right, with the same distance function. For it is clear that if conditions (1) to (3) hold for $p,q,r \in X$, they also hold if we restrict $p,q,r$ to lie in $Y$.

Thus, every subset of a Euclidean space is a metric space. 

##### Basic Definition: Segments, Open/Closed Sets, Convex
```ad-Definition
By the _segment_ $(a,b)$ we mean the set of all real numbers $x$ such that $a<x<b$. 

By the _interval_ $[a,b]$ we mean the set of all real numbers $x$ such that $a\leq x\leq b$. 

Occasionally we shall also encounter "half-open intervals" which consist of a mix of both.

If $a_{i}<b_{i}$ for $i=1,\ldots,k$, the set of all points $\bf{x} = (x_{1},\ldots,x_{k})$ in $R^{k}$ whose coordinates satisfy the inequalities $a_{i}\leq x_{i}\leq b_{i} (1 \leq i \leq k)$ is called a $k$-cell. Thus a 1-cell is an interval, a 2-cell is a rectangle, etc. 

If $\bf{x}\in R^{k}$ and $r>0$, the _open_(or _closed_) ball $B$ with center at $\bf{x}$ and radius $r$ is defined to be the set of all $\bf{y} \in R^{k}$ such that $|\bf{y}-\bf{x}|<r$(or $|\bf{y}-\bf{x}|\leq r$). 

We call a set $E \subset R^{k}$ _convex_ if 
$$
\lambda \bf{x} + (1- \lambda)\bf{y} \in E
$$
whenever $\bf{x}\in E, \bf{y}\in E$, and $0<\gamma<1$. 

For example, _balls are convex_. For if $|\bf{y}-\bf{x}|<r, |\bf{z}-\bf{x}|<r$, and $0<\lambda<1$, we have 
$$
|\lambda\bf{y} + (1-\lambda)\bf{z} - \bf{x}| = |\lambda(\bf{y}-\bf{x})+(1-\lambda)(\bf{z}-\bf{x})|
$$
$$
\leq \lambda|\bf{y}-\bf{x}| + (1-\lambda)|\bf{z}-\bf{x}| < \lambda r + (1-\lambda)r = r
$$

This same proof applies to closed balls. It is also easy to see tha $k$-cells are convex. 
```

##### Subsets and Elements of Metric Spaces
**Remark.**  The definitions below are similar to [[Regions in the Complex Plane]]. 

```ad-Definition
Let $X$ be a metric space. All points and sets mentioned below are understood to be elements and subsets of $X$.
1. A _neighborhood_ of $p$ is a set $N_{r}(p)$ consisting of all $q$ such that $d(p,q)<r$, for some $r>0$. The number $r$ is called the _radius_ of $N_{r}(p)$
2. A point $p$ is a _limit point_ of the set $E$ is _every_ neighborhood of $p$ contains a point $q \neq p$ such that $q \in E$. 
3. If $p \in E$ and $p$ is not a limit point of $E$, then $p$ is called an _isolated point_ of $E$. 
4. $E$ is _closed_ if every limit point of $E$ is a point of $E$.
5. a point $p$ is an _interior point_ of $E$ if there is a neighborhood $N$ of $p$ such that $N \subset E$. 
6. $E$ is _open_ if every point of $E$ is an interior point of $E$. 
7. The _complement_ of $E$ (denoted by $E^{c}$) is the set of all points $p \in X$ such that $p \notin E$. 
8. $E$ is _perfect_ if $E$ is closed and if every point of $E$ is a limit point of $E$. 
9. $E$ is _bounded_ if there is a real number $M$ and a point $q \in X$ such that $d(p,q)<M$ for all $p \in E$. 
10. $E$ is _dense_ in $X$ is every point of $X$ is a limit point of $E$, or a point of $E$ (or both). 
```

Let us note that in $R^{1}$ neighborhoods are segments, whereas in $R^{2}$ neighborhoods are interiors of circles. 

**Theorem 2.19.**  Every neighborhood is an open set. 

**Proof:**  Consider a neighborhood $E=N_{r}(p)$, and let $q$ be any point of $E$. Then there is a positive real number $h$ such that $d(p,q)=r-h$. For all points $s$ such that $d(q,s)<h$, we have then $d(p,s)\leq d(p,q)+d(q,s)<r-h+h=r$, so that $s \in E$. Thus, $q$ is an interior point of $E$. 

**Theorem 2.20.**  If $p$ is a limit point of a set $E$, then every neighborhood of $p$ contains infinitely many points of $E$. 

**Proof:**  Suppose that there is a neighborhood $N$ of $p$ which contains only a finite number of points of $E$. Let $q_{1},\ldots,q_{n}$ be those points of $N \cap E$, which are distinct from $p$, and put 
$$
r = \min_{a\leq m\leq n} d(p,q_{m})
$$
The minimum of a finite set of positive numbers is clearly positive, so that $r>0$. The neighborhood $N_{r}(p)$ contains no point $q$ of $E$ such that $q \neq p$, so that $p$ is not a limit point of $E$. This contradiction establishes the theorem. 










