---
tags: 
dg-publish: true
mathLink: 
---
Subject: _Topology_
Main\_Topic: _Topology_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Topologies]]_
Cont.\_ of: _None_ 
_
_

##### The Real Numbers
Mathematics involves logic and patterns, often in quantitative settings requiring numbers. The natural numbers $\mathbb{N}=\{1,2,3,4,5,\ldots\}$. Historically, 0 came much later than the counting numbers. We also have the set of integers, denoted $\mathbb{Z}$, which comes from the German word for numbers, Zahlen. Ratios give us the set of rational numbers $\mathbb{Q}=\{\frac{a}{b}:a,b \in \mathbb{Z}\}$. The Greeks were very adept at using positive integers and ratios of positive integers. They were not happy to discover that some numbers that they encountered, such as the length of the diagonal of a unit square, were not ratios of integers. Such numbers are _irrational numbers_. 

We list some well-known facts about rational and irrational numbers:
1. If $n \in \mathbb{N}$, then $\sqrt{n}$ is either an integer or irrational.
2. The product or quotient of two nonzero rational numbers is rational.
3. The product or quotient of a nonzero rational number and an irrational numbers is irrational.
4. The product or quotient of two irrational numbers may be rational or irrational.
5. Every nonempty open interval $(a,b)$ contains rational numbers and irrational numbers.

These can be proven quite easily. Try for yourself. 

---
##### Sets
Suppose we have several objects under consideration, we with to specify some list of these elements for further consideration. The objects under the consideration make up the _Universal Set_ $U$, and a well-defined list of selected objects gives a set $A$ in $U$. The objects included in a set $A$ are the _elements_ of the set $A$. If $a$ is a element of $A$, we denote it by $a \in A$. If $A$ and $B$ are two sets in $U$ and every element of $A$ is an element of $B$, then $A$ is a _subset_ of $B$ and $B$ is a superset of $A$, denoted $A \subseteq B$ or $B \supseteq A$. If $A\subseteq B$ and $A \neq B$, then we have a proper subset, $A \subset B$. The set of no elements is the empty set, denoted $\emptyset$. Note that the empty set is a subset of all sets. We can define the union and intersection of sets, which creates a set where we include all elements of both sets or find the overlap between sets. The set difference takes the elements in one set and not in the other set. For example, $A,B$ are sets, then $A-B =\{x:x\in A, x\notin B\} = A \cap B^{c} = A \cap (U-B)$. Note that $B^{c}$ is the complement of $B$, or the rest of $U$ that excludes $B$. Think of a square with an area, and we take a subset of that region. If the subset of the square is $B$, the rest of the area in the square excluding that region is $B^{c}$. A collection is a set whose elements are set themselves. A collection of the subsets for a set is called the **Power Set**, denoted $\mathcal{P}(A)$ for a set $A$. 

Often we will need to give each element of a collection $\mathcal{C}$ a label, and we may write $\mathcal{C}=\{A_{i}:i \in I\} = \{A_{i}\}_{i \in I}$. Then 
$$
\bigcup \mathcal{C} = \bigcup_{i \in I}A_{i} = \{x:x \in A_{i} \ \text{for some} \ i\in I\}
$$
The same is true for the intersection. 

If the index set $I$ is finite, then the intersection is called a finite intersection. That is, a finite intersection is an intersection of a finite collection of sets. Similarly, the adjectives in _infinite_ intersections, countable intersections, and countable intersections refer to the cardinality of the index set. If no restriction is given on the index set, we refer to an _arbitrary intersection_. In practice, arbitrary intersection should suggest intersecting a finite or infinite collection. Similar terminology applies to unions. Occasionally, we may consider a collection of subsets of a universal set $U$ indexed by the empty set. In this case, we take 
$$
\bigcap_{i \in \emptyset}A_{i}= U, \quad \bigcup_{i\in \emptyset}A_{i} = \emptyset
$$
Intuitively, the more sets you intersect, the smaller the intersection gets, so the fewer sets you intersect, the larger the intersection gets, so intersecting no sets gives the largest possible set $U$. Similarly, the fewer sets you union, the smaller the result, so unioning no sets gives the smallest possible set $\emptyset.$

A collection $\mathcal{C}=\{A_{i}\:i \in I\}$ is mutually disjoint if for $i\neq j \in I, A_{i}\cap A_{j} = \emptyset.$ The collection is _nested_ if for every $i,j \in I$, either $A_{i} \subseteq A_{j}$ or $A_{j}\subseteq A_{i}$. 

Rules for taking the unions or intersections are named for the British mathematician Augustus De Morgan. De Morgan's Laws state that the complement of an intersection is the union of the complements, and the complement of a union is the intersection of the complements. That is
$$
U - \bigcap_{i \in I}A_{i} = \bigcup_{i \in I} (U-A_{i}), \quad U- \bigcup_{i \in I}A_{i} = \bigcap_{i \in I} (U-A_{i}) 
$$
Another often used property involves containments. If $A_{i}\subseteq B_{i}$ for each $i \in I$, then $\cup_{i\in I}A_{i}\subseteq \cup_{i \in I}B_{i}$ and $\cap_{i \in I}A_{i}\subseteq \cap_{i\in I}B_{i}$. Given two sets $A$ and $B$, their **Cartesian Product** is the set $A \times B = \{(a,b):a \in A, b \in B\}$. 

**Remark.**  It may not be easy to recognize when a set is infinite or finite

---
##### Quantifiers and Logic
A statement is a sentence which is either true or false. If $S$ and $T$ are statements, the implication "S implies T" will be denoted $S \implies T$. The implication $S \implies T$ is true, if, whenever $S$ is true, $T$ is also true. If $S \implies T$ and $T \implies S$, then we write $S \iff T$ and say that $S$ and $T$ are logically equivalent statements, or $S$ occurs _if and only if_  $T$ occurs. In this case $S$ is a necessary and sufficient condition for $T$. 

The _negation_ of a statement, denoted $\sim S$, is the statement "not S." That is, $S$ is true and only true if $\sim S$ is false. 

The _converse_ of an implication $S \implies T$ is the implication that $T \implies S$. If an implication is true, its converse may be true or false. 

The _contrapositive_ of an implication $S \implies T$ is the implication $\sim T \implies \sim S$. An implication and its contrapositive are logically equivalent: either both are true or both are false.

The conjunction $S \wedge T$ of statements $S$ and $T$ is the statement "$S$ and $T$." The disjunction $S \vee T$ of statements $S$ and $T$ is the the statement "$S$ or $T$." The following facts are also called De Morgan's Laws:
$$
\sim (S \wedge T) =\ \sim S \ \vee \sim T
$$
$$
\sim(S \vee T) =\ \sim S \wedge  \sim T.
$$
The only way and implication $S \implies T$ fails is if $S$ occurs but $T$ does not. Thus, $\sim(S \implies T) = S \wedge \sim T$. 

The universal quantifier $\forall$ means "for every." The existential qualifier $\exists$ means "there exists." The only way the statement "there exists $x$ for which $S$ is true" could fail is if for every $x$, $S$ is false. Similarly, the statement "for every $x$, $S$ is true" fails if and only if there exists an $x$ for which $S$ fails. That is 
$$
\sim(\forall x, S) = \exists x \ \text{such that} \ \sim S,
$$
$$
\sim(\forall x \ \text{such that}\ S ) = \forall x, \sim S.
$$

##### Functions
If $X$ and $Y$ are sets, a _function_ is a mapping from $X$ to $Y$ which we write as $f:X \rightarrow Y$. The set $X$ is the domain and the set $Y$ is the codomain. If $f:X\rightarrow Y$ is a function and $x \in X$, then the unique element of $Y$ which $f$ assigns to $x$ is denoted $f(x)$ and is called the _value of $f$ at $x$_, or the image of $x$ under $f$. While $f$ must assign a value to each point $x$ of its domain, not every point in the codomain must be used as an output The set $\{f(x):x \in X\} = f(X)$ is called the _image_ or _range_ of $f$. 

A function is surjective or onto if $f(X)=Y$, or if for every $y \in Y$, there exists an $x\in X$ with $f(x)=y$.

A function is 1:1 or injective if $w \neq x \implies f(w) \neq f(x)$, or equivalently, $f(w) = f(x) \implies w=x$. Note that $f:X \rightarrow Y$ fails to be 1:1 if there exist two distinct elements $w \neq x$ in $X$ which map to the same one element.

A 1:1 onto function is called a **bijection.** If $f:X \rightarrow Y$ is a bijection, then, for any $y \in Y$, there exists $x \in X$ with $f(x)=y$ due to being onto and there are unique $x \in X$ with $f(x)=y$ due to being 1:1. Thus, $f:X\rightarrow Y$ is a bijection if and only if there exists a function $f^{-1}:Y \rightarrow X$ called the _inverse function_ of $f$ with $f^{-1}(y)=x$ if and only if $f(x)=y$. 

Functions are rules denoted by $f$ or by the rule of assignment $f(x)=y.$; technically, $f(x)$ represents the value of a function and not the function itself. By widespread abuse of notation, "the function $f(x)$" is sometimes used as a shortened version of "the function $y=f(x)$." Of course, it would be even shorter to say "the function $f$" but we would like to acknowledge the independent variable at play. 

Suppose $f:X \rightarrow Y$ is a function, $A \subseteq X$ and $B \subseteq Y$. The set $f(A)=\{f(a):a \in A\}$ is the _image of $A$ under $f$_. The set $f^{-1}(B) = \{x \in X: f(x) \in B\}$ is the _inverse image_ of $B$ under $f$. Note that the inverse image of a set $B$ is defined whether or not $f$ has an inverse function. In this notation, $f^{-1}$ denotes the inverse relation, which may or may not be a function.

**Theorem 0.4.1**  Suppose $f:X\rightarrow Y$ is a function.
1. $f(A \cup B) = f(A) \cup f(B)$ for all $A,B \subseteq X$. 
2. $f(A\cap B ) \subseteq f(A)\cap f(B)$ for all $A,B \subseteq X$ and $f(A \cap B) = f(A) \cap f(B)$ for all $A,B \subseteq X$ if and only if $f$ is one-to-one. 
3. $f(A-B) \supseteq f(A)-f(B)$ for all $A,B \subseteq X$ and $f(A-B) =f(A)-f(B)$ for all $A,B \subseteq X$ if and only if $f$ is one-to-one. 
4. $f^{-1}(C \cup D)=f^{-1}(C)\cup f^{-1}(D)$ for all $C,D\subseteq Y$.
5. $f^{-1}(C\cap D)=f^{-1}(C)\cap f^{-1}(D)$ for all $C,D \subseteq Y$.
6. $f^{-1}(C-D)=f^{-1}(C)-f^{-1}(D)$ for all $C,D \subseteq Y$.

If $f:A\rightarrow B$ and $g:B \rightarrow C$ are functions, then the _composition_ of $f$ and $g$ is $g \circ f:A \rightarrow C$ defined by $(g\circ f)(a)=g(f(a))$ for all $a\in A$. 

A **sequence** in $A$ is a function $f:\mathbb{N}\rightarrow A$. The nth term of the sequence is $f(n)$. If we write $a_{n}=f(n)$, then we may specify the sequence by $(f(n))_{n\in \mathbb{N}}$, or simply as $(a_{n})$. 

If $X$ and $Y$ are subsets of $\mathbb{R}$ a function $f:X\rightarrow Y$ is increasing if $a\leq b$ in $X$ implies $f(a)\leq f(b)$ in $Y$, and is _strictly increasing_ if $a<b$ in $X$ implies $f(a)<f(b)$ in $Y$. _Decreasing_ and strictly decreasing functions are defined dually. 

Intuitively, a subsequence of a sequence is obtained by omitting some terms.

---
##### Countable Sets 
To count the objects in a finite set, we set up a 1:1 correspondence (a bijection) between the objects and a set $\{1,2,3,\ldots,n\}$. We say sets $A$ and $B$ have the same cardinality, denoted $|A| = |B|$, if there exists a bijection from $A$ to $B$. A set $A$ is _countable infinite_ if it has the same cardinality as the set $\mathbb{N}$ of counting numbers. That is, $A$ is countable infinite if and only if there exists a bijection $f:\mathbb{N}\rightarrow A$. Thus, $A$ is countable infinite if and only if the elements of $A$ can be listed as a sequence $(a_{n})_{n \in \mathbb{N}}$ of distinct terms. A set is countable if and only if it is finite or countably infinite. A set is uncountable if it is not countable.

**Theorem 0.5.1**  
1. Every subset $A$ of a countable set $B$ is countable.
2. If $f:A\rightarrow B$ is 1:1 and $B$ is countable, then $B$ is countable. 
3. If $f:A\rightarrow B$ is onto and $A$ is countable, then $B$ is countable.
4. If $A$ and $B$ are countably infinite sets, then $A \cup B$ is countable infinite.
5. If $A$ and $B$ are countably infinite sets, $A \times B$ is countable infinite.
6. If $\{A_{n}\}_{n \in \mathbb{N}}$ is a countable collection of countable infinite sets $A_{n}$, then the union $\cup_{n\in \mathbb{N}}A_{n}$ is countably infinite.

**Theorem 0.5.2**  The set $\mathbb{Q}$ of rational numbers is countable. The set $\mathbb{R}$ of reals is uncountable.

---
##### Equivalence Relations and Partitions
If $A$ and $B$ are sets, a _relation_ from $A$ to $B$ is a subset $R$ of $A \times B$. If $(a,b)\in R$, we say $a$ is related to $b$ by the relation $R$, denoted $aRB$. Thus, a relation from $A$ to $B$ is just a set of ordered paris telling which elements of $A$ are related to which elements of $B$. A relation from a set $A$ to the same set $A$ is called a _relation on $A$_.  

```ad-Definition
An equivalence relation $R$ on a set $A$ is a relation which is
1. reflexive: $aRa$ for every $a\in A$
2. symmetric: $aRb \implies bRa$ for every $a,b\in A$
3. transitive: $aRb$ and $bRc$ implies $aRc$ for every $a,b,c \in A$
```

The prototype for an equivalence relation on a set $A$ is equality. For every $a,b,c \in A$, clearly $a=a$, if $a=b$, then $b=a$, and if $a=b$ and $b=c$, then $a=c$, so equality is an equivalence relation. In general, an equivalence relation on a set $A$ will be equality of some attribute of the elements of $A$. 

Given an equivalence relation, it is not always easy to recognize it as equality of some attribute. We may define and verify some relation $\approx$, but it may not be easy to see the equality of attributes that is going on in the background. 

A _partition_ of a set $A$ is a collection $\mathcal{P}=\{B_{i}\}_{i\in I}$ of nonempty, mutually disjoint subsets of $A$ whose union is $A$. The elements $B_{i}$ of a partition are called the _blocks_ of the partition. If $\mathcal{P}=\{B_{i}\}_{i\in I}$ is a partition of a set $A$ and some of the blocks $B_{i}$ are further partitioned into "subblocks", the resulting collection of subblocks is also a partition of $A$ called a _refinement_ of $\mathcal{P}$, or a finer partition of $\mathcal{P}.$ Formally, if $\mathcal{P}$ and $\mathcal{R}$ are partitions of set $A$, $\mathcal{R}$ is a refinement of $\mathcal{P}$ if for every block $B_{R \in}\mathcal{R}$, there exists $B_{P}\in \mathcal{P}$ with $B_{R}\subseteq B_{P}.$ If a partition $\mathcal{R}$ is finer than $\mathcal{P}$ and $\mathcal{R}\neq \mathcal{P}$, then we say $\mathcal{R}$ is _strictly finer_ than $\mathcal{R}$ (or $\mathcal{P}$ is _strictly coarser_ than $\mathcal{R}$). Subsets of $A$ which are unions of a partition of $A$ are said to be _saturated_ with respect to the partition. Thus, partition $\mathcal{R}$ is finer than partition $\mathcal{P}$ if and only if each block of $\mathcal{P}$ is $\mathcal{R}$-saturated. 

If $\approx$ is an equivalence relation on $A$ and $a \in A$, the _equivalence class_ of $a$ is the set $[a] = \{x \in A: x \approx a\}$ of all elements of $A$ which are equivalent to $a$. The following result shows the fundamental connection between equivalence relations and partitions:

**Theorem 0.6.3**  Every partition $\mathcal{P}$ of a set $A$ determined an equivalence relation $\approx_{P}$ on $A$ defined by $a \approx_P b$ if and only if there exists a block $B_{i}\in \mathcal{P}$ with $\{a,b\}\subseteq B_{i}.$

Every equivalence relation $\approx$ on set $A$ determined a partition $\mathcal{P}_{\approx}=\{[a]:a \in A\}$ whose blocks are the equivalence class. 

Furthermore, $\mathcal{P}_{\approx_{P}}=\mathcal{P}$ and $\approx_{P_{\approx}}=\ \approx$. 3

It is easy to transfer terminology about partitions into the language of equivalence relations. For example, if $\approx$ is an equivalence relation on set $A$, we say a set $B \subseteq A$ is _saturated_ with respect to $\approx$ if $x\in B$ implies $[x]\subseteq B$. 