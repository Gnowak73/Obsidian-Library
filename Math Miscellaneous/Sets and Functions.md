---
tags:
  - Real
  - Real_analysis
  - Set
  - sets
  - function
  - functions
  - Operator
  - operations
  - Math
dg-publish: true
mathLink:
---
Subject: _Real Analysis_
Main\_Topic: _Sets and Functions_
Applications: _Elementary Proofs and set Theory_
Examples: _None_
Class: _Elements of Real Analysis_
Exam: _Exam 1_
Textbook: _[[Steven R. Lay - Analysis with an introduction to proof.-Pearson (2014).pdf]]_
Closely\_Related\_To: _[[Complex Numbers Algebraic Properties]],[[Math Miscellaneous/The Real and Complex Number Systems]]_
Cont.\_ of: _None_ 
_
_

## Basic Set Operations 
The idea of a set or collection of things is a common in our everyday lives. For example, we speak of a _team_ of players, a _flock_ of geese, or a _committee_ of people. Each of these refers to a collection of distinguishable objects that is thought of as a whole. 

In spite of the familiarity of this idea, it is essentially impossible to give a definition of "set" except in terms of synonyms that are also undefined. Thus, we shall be content with the informal understanding that a set if a collection of objects characterized by some defining property that allows us to think of the objects as a whole. The objects in a set are called **elements** or **members** of the set. 

**Notation:**  the symbol $\in$ denotes membership in a set, and $\notin$ denotes non-membership in a set. 

---
To say that a set must be characterized by some defining property is to require that is be a clear question of fact whether a particular object does or does not belong to a particular set. We do not, however, demand that the answer to the question of membership be known. Another way to say this is to require that for any element $a$ and any set $A$ the sentence "$a \in A$" be a statement; that is, it must be true or false, and not both. 

To define a particular set, we have to indicate the property that characterizes its elements. For a finite set, this can be done by listing its members. 

```ad-note
Let us distinguish that an element is **not** the same as a set with one element. $B=\{b\}$ and $b \in B$ are not the same!
```

For an infinite set we cannot list all of the members, so a defining rule must be given. It is customary to set off the rule within braces, as in 
$$
C = \{x:x \ \text{is prime}\}.
$$
In other words, "C is the set of all prime numbers." When considering two sets, say $A$ and $B$, if every element of $A$ is also an element of $B$, we say that $A$ is a subset of $B$. This is denoted $A \subset B$. 

---
```ad-Definition
Let $A$ and $B$ be sets. We say that $A$ is a **subset** of $B$ (or $A$ is **contained** in $B$) if every element of $A$ is an element of $B$, adn we denote this by writing $A \subseteq B$. (This can also be written the other way around).

If there also exists an element in $B$ that is not in $A$, then $A$ is called a **proper** subset of $B$. 
```

This definition tells us what we must do if we want to prove $A \subseteq B$. We must show that 
$$
\text{if} \ x \in A, \text{then} \ x\in B
$$
is a true statement. That is, we must show that teach element of $A$ satisfies the defining condition that characterizes set $B$. 

---
```ad-Definition
Let $A$ and $B$ be sets. We say that $A$ is **equal** to $B$, written $A=B$, if $A \subseteq B$ and $B \subseteq A$. 
```

When this definition is combined with the definition of subset, we see that proving $A=B$ is equivalent to proving 
$$
x \in A \rightarrow x \in B \quad \text{and} \quad x \in B \rightarrow x\in A
$$
It is important to note that, in describing a set, the order in which the elements appear does not matter, nor does the number of times they are written. Thus the following sets are all equal: 
$$
\{1,2,3,4\} = \{2,4,3,1\} = \{1,2,3,2,4,2\}
$$
Since the repeated $2$'s in the last set are unnecessary, it is preferable to omit them. Although we cannot give a formal definition of them now, it is convenient to name the following sets, which should already be familiar to the reader. 

![[Pasted image 20240118133808.png|center]]

In constructing sets it is often helpful to indicate a larger set from which the elements are being chosen. We indicate this by a slight change in our set notation. For example, instead of having to write
$$
\{x:x \in \mathbb{R} \ \text{and} \ 0<x<1\}
$$
we may write 
$$
\{x \in R: 0<x<1\}
$$
---

the set $[a,b]$ is called a **closed interval** and the set $(a,b)$ is called an **open interval**. And we can create mixed sets or **half-open**/**half-closed** intervals/sets. Additionally, the **empty** set, denoted $\emptyset$, is a set with no members. 

**Theorem 1.7**  Let $A$ be a set. then $\emptyset \subseteq A$. 

**Proof:**  To prove this, we must establish that the implication: if $x \in \emptyset$, then $x\in A$, is true. Since $\emptyset$ has no members, the antecedent "$x \in \emptyset$" is false for all $x$. Thus, according to our definition of implies, the implication is always true. 

---
There are three basic ways to form new sets from old ones. These operations are called union, intersection, and complementation. 

```ad-Definition
Let $A$ and $B$ be sets. The **union, intersection**, and **complement** are given by 
$$
A \cup B \equiv \{x:x\in A \ \text{or} \ x\in B\}
$$
$$
A \cap B \equiv \{x:x\in A \ \text{and} \ x\in B\}
$$
$$
A\backslash B \equiv \{x:x\in A \ \text{and} \ x\notin B\}
$$
```

If $A \cap B = \emptyset$, then $A$ and $B$ are said to be **disjoint**. 

As we see all over mathematics, mathematical concepts and proofs always occur within the context fo some mathematical system. It is customary for the elements of the system to be called the **universal set**. Then any set under consideration is a subset of this universal set. This set is typically denoted by $U$.  

---
**Theorem 1.13**  Let $A,B$ and $C$ be subsets of a universal set $U$. Then the following statements are true:

![[Pasted image 20240118140022.png|center]]

**Proof:**  The proof for this is much more complicated, and can be seen in [[Steven R. Lay - Analysis with an introduction to proof.-Pearson (2014).pdf|Real Analysis Textbook]].

---
```ad-Definition
If for each element $f$ in a nonempty set $J$ there corresponds a set $A_{j}$, then 
$$
\mathcal{A} = \{A_{j}:j \in J\}
$$
is called an **indexed family** of sets with $J$ as the index set. THe union of all the sets in $\mathcal{A}$ is defined by 
$$
\bigcup_{j \in J} A_{j} = \{x:x \in A_{j} \ \text{for some} \ j \in J\}
$$
The intersection of all the sets in $\mathcal{A}$ is defined by 
$$
\bigcap_{j \in J} A_{j} = \{x:x \in A_{j} \ \text{for all} \ j \in J\}
$$
Other notations for $\bigcup_{j \in J} A_{j}$ include $\bigcup \mathcal{A}$.

If $J=\{1,2,\ldots,n\}$ we may write 
$$
A_{1}\cup A_{2} \cup \ldots \cup A_{n} = \bigcup_{j=1}^{n}A_{j} \quad
$$
and if $J=\mathbb{N}$, the common notation is 
$$
\bigcup_{j=1}^{\infty}A_{j}
$$
Similar variations of the notation apply to intersections. 

There are some situations where a family of sets has bot been indexed but we still wish to take the union or intersection of all the sets. If $\mathcal{B}$ is a nonempty collection of sets, then we let 
$$
\bigcup_{B \in \mathcal{B}} B = \{x:x \in B \ \text{for some} \ B \in \mathcal{B}\}
$$
and 
$$
\bigcap_{B \in \mathcal{B}} B = \{x:x \in B \ \text{for all} \ B \in \mathcal{B}\}
$$
```

## Relations 

#### Ordered Pairs 
In our discussion of sets we noted that the order of the elements is not important. Thus the set $\{a,b\}$ is the same as the set $\{b,a\}$. There are times, however, when order _is_ important. For example, ordered pairs in geometry and coordinates. When we wish to indicate that a set of two elements $a$ and $b$ is _ordered_, we enclose the elements in parenthesis: $(a,b)$.

```ad-Definition
The **ordered pair** $(a,b)$ is the set whose members are $\{a\}$ and $\{a,b\}$. In symbols we have 
$$
(a,b) = \{\{a\},\{a,b\}\}.
$$
the acceptability of this definition depends on the ordered pairs actually having the property expected of them. This we prove in the following theorem. 
```

**Theorem 2.2**  $(a,b)=(c,d)$ iff $a=c$ and $b=d$. 

**Proof:**  The proof can be seen on page 55 of [[Steven R. Lay - Analysis with an introduction to proof.-Pearson (2014).pdf]]

---
#### Cartesian Products and Relations  

```ad-Definition
If $A$ and $B$ are sets, the nthe **Cartesian product**(or **cross product**) of $A$ and $B$, written $A \times B$, is the set of all ordered pairs $(a,b)$ such that $a \in A$ and $b \in B$. In symbols,
$$
A \times B = \{(a,b): a\in A \ \text{and} \ b\in B\}
$$
```

---
Intuitively, a relation between two objects $a$ and $b$ is a condition involving $a$ and $b$ that is either true or false. When it is true, we say $a$ is related to $b$; otherwise, $a$ is not related to $b$. 

```ad-Definition
Let $A$ and $B$ be sets. A **relation between $A$ and $B$** is any subset $R$ of $A \times B$. We say that an element $a$ in $A$ is **related** by $R$ to an element $b$ in $B$ if $(a,b)\in R$, and we odten denote this by writing "$aRb$." The first set $A$ is referred to as the **domain** of the relation and denoted by $dom \ R$. If $B=A$, then we speak of a relation $R \subseteq A \times A$ being a **relation on $A$**. 
```

---
Certain relations are singled out because they possess the properties naturally associated with the idea of equality. They are called equivalence relations, ads we see in the following definition. 

```ad-Definition
A relation $R$ on a set $S$ is an **equivalence relation** if it has the following properties for all $x,y,z$ in $S$:
1. $xRx$ (reflexive property)
2. If $xRy$, then $yRx$ (symmetric property)
3. If $xRy$ and $yRz$, then $xRz$. (transitive property)
```

Given an equivalence relation $R$ on a set $S$, it is natural to group together all the elements that are related to a particular element. More precisely, we define the **equivalence class** (with respect to $R$) of $x \in S$ to be the set 
$$
E_{x} = \{y \in S: yRx\}.
$$
Since $R$ is reflexive, each element of $S$ is in some equivalence class. Furthermore, equivalence classes must be disjoint. That is, if two equivalence classes overlap, they must be equal. The explanation for such can be seen in [[Steven R. Lay - Analysis with an introduction to proof.-Pearson (2014).pdf| Real Analysis Textbook]].

---
```ad-Definition
A **partition** of a set $S$ is a collection $\mathcal{P}$ of nonempty subsets of $S$ such that 
1. Each $x \in S$ belongs to some subset $A \in \mathcal{P}$
2. For all $A,B \in \mathcal{P}$, if $A\neq B$, then $A \cap B = \emptyset$
```

For example, let us look at possible partitions of $S=\{1,2,3\}$

![[Pasted image 20240124120203.png|center]]

Not only does an equivalence relation on a set $S$ determine a partition of $S$, but the partition can be used to determine the relation. We formalize this in the following theorem.

**Theorem 2.17**  Let $R$ be an equivalence relation on a set $S$. Then $\{E_{x}:x \in S\}$ is a partition of $S$. The relation "belongs to the same piece as" is the same as $R$. Conversely, if $\mathcal{P}$ is a partition of $S$, let $P$ be defined by $xPy$ iff $x$ and $y$ are in the same piece of the partition. Then $P$ is an equivalence relation and the corresponding partition into equivalence classes is the same as $\mathcal{P}$. 

**Proof:**  This proof can be seen in [[Steven R. Lay - Analysis with an introduction to proof.-Pearson (2014).pdf]]

---
## Functions 
We now turn our attention to the concept of a function. The reader no doubt thinks of a function $f$ as a formula or a rule that enables us to compute the function value $f(x)$ given any specific value for $x$. In a sense, we think of functions as establishing a corresponding between certain sets (typically real numbers and other real numbers). 

This is helpful in many cases, but is inadequate for the things we wish to do in analysis. In searching for a more general understanding of a function, we need to hold on to the idea of a correspondence between sets, but not require that it be described by a formula. What is important is that a given element in the first set cannot correspond to two different elements in the second set. Thus we see that a function is a special kind of relation. We make this precise in the following definition.  

```ad-Definition
Let $A$ and $B$ be sets. A **function** from $A$ to $B$ is a nonempty relation $f \subseteq A \times B$ that satisfies the following two conditions:
1. _Existence_: For all $a$ in $A$, there exists a $b$ in $B$ such that $(a,b) \in f$.
2. _Uniqueness_: If $(a,b) \in f$ and $(a,c) \in f$, then $b=c$.

That is, given any element $a$ in $A$, there is one and only one element $b$ in $B$ such that $(a,b) \in f$. Set $A$ is called the **domain** of $f$ and is denoted by $dom \ f$
. Set $B$ is referred to as the **codomain** of $f$. We say write $f:A\rightarrow B$ to indicate $f$ has domain $A$ and codomain $B$. The **range** of $f$, denoted $rng \ f$, is the set of all second elements of members of $f$. That is, 
$$
rng \ f = \{b \in B: \exists \ a \in A \ni (a,b) \in f\}
$$
```

```ad-note
$\ni$ means "such that" and it was originally establish by Peano, one of the founders of set logic and notation.
```

If $(x,y)$ is a member of $f$, we often say that $f$ maps $x$ onto $y$ or that $y$ is the image of $x$ under $f$. It is also customary to write $y=f(x)$ instead of $(x,y) \in f$. This agrees with the familiar usage when $f$ is described by a formula, but also applies in more general settings. 

When a function consists of just a few ordered pairs, it can be identified simply by listing them. Usually, however, there are too many to list, so the function is identified by specifying the domain and giving a rule for determining the unique second element in the ordered pair that corresponds to any particular first element. When this rule is a formula, we are back to the intuitive notion of a function that we are used to. 

The domain of the function would be obtained wither from the context or by stating it explicitly. Unless told otherwise, when a function is given by a formula, the domain is taken to be the largest subset of $\mathbb{R}$ for which the formula will always yield a real number. 

Having defined a function to be a set of ordered pairs satisfying the existence and uniqueness conditions, we should note that the notation $f:A \rightarrow B$ is slightly more restrictive than the ordered pair definition because it specifies a particular codomain. This subtle difference between the ordered pair definition and the $f:A \rightarrow B$ notation will be significant later, where we may want to consider the functions 
$$
f:\mathbb{R} \rightarrow \mathbb{R} \ \text{such that} \ f(x)=x^{2} \ \text{and}
$$
$$
g:\mathbb{R} \rightarrow [0,\infty) \ \text{such that} \ g(x)=x^2 
$$
to be different functions (with different properties) even though their ordered pairs are identical. 

---
#### Properties of Functions 
Now let us look at some properties of these functions.

```ad-Definition
A function $f:A \rightarrow B$ is called **surjective** (or is said to map $A$ **onto** $B$) if $B = rng \ f$. A surjetive funtion is also referred to as a **surjection**. 
```

The question of whether or not a function is surjective depends on the choice of codomain. A function can always be made surjective by restricting the codomain to be equal to the range, but sometimes this is not convenient. 

If it happens that no member of a codomain appears more than once as a second element in one of the ordered pairs, then we have another important type of function. 

```ad-Definition
A function $f:A \rightarrow B$ is called **injective** (or **one-to-one**) if, for all $a$ and $a'$ in $A$, $f(a)=f(a')$ implies that $a=a'$. An injective function is also referred to as an **injection**.  
```

If a function is both surjective and injective, then it is particularly well behaved. 

```ad-Definition
A function $f:A \rightarrow B$ is called **bijective** or a **bijection** if it is both surjective and injective.
```

---

#### Functions Acting on Sets 
When thinking of a function as transforming its domain into its range, we may wish to consider what happens to certain subsets of the domain. Or we may wish to identify the set of all points in the domain that are mapped into a particular subset of the range. To do this we use the following notation: 

**Notation 3.13**  Suppose that $f:A \rightarrow B$. If $C \subseteq A$, we let $f(C)$ represent the subset $\{f(x):x \in C\}$ of $B$. The set $f(C)$ is called the **image** of $C$ in $B$. If $D \subseteq B$, we let $f^{-1}(D)$ represent the subset $\{x \in A: f(x) \in D\}$ of $A$. The set $f^{-1}(D)$ is called the **pre-image** of $D$ in $A$ or $f$ inverse of $D$.  

![[Pasted image 20240124230705.png|center]]

Before illustrating these ideas further, we should comment that the symbol $f^{-1}$ is not to be thought of as an inverse function applied to points in the range of $f$. in particular, given a point $y$ in $B$ it makes no sense to talk about $f^{-1}(y)$ as a point in $A$, since there may be several points in $A$ that are mapped to $y$. We shall see a bit later how this idea can be made meaningful _in some cases_; but for now we an apply $f^{-1}$ only to a subset of $B$, and by so doing we obtain a subset of $A$. 

Given a function $f:A \rightarrow B$, there are many relationships that hold between the images and pre-images of subsets of $A$ and $B$. In the following theorem we state a number of relationships like this that apply to images and preimages. 

**Theorem 3.16**  Suppose that $f:A \rightarrow B$. Let $C,C_{1},$ and $C_{2}$ be subsets of $A$ and let $D,D_{1}$, and $D_{2}$ be subsets of $B$. Then the following hold:

![[Pasted image 20240130130701.png|center]]


While this theorem states the strongest results that hold in general, if we apply certain restrictions on the functions involved, then the containment symbols in a, b, and c may be replaced by equality. 

**Theorem 3.18**  Suppose that $f:A \rightarrow B$. Let $C,C_{1},$ and $C_{2}$ be subsets of $A$ and let $D$ be a subset of $B$. Then the following hold:
1. If $f$ is injective, then $f^{-1}[f(C)]=C$
2. If $f$ is surjective, then $f[f^{-1}(D)]=D$
3. If $f$ is injective, then $f(C_{1} \cap C_{2}) = f(C_{1}) \cap f(C_{2})$

---
#### Composition of Functions 
If $f$ and $g$ are functions with $f:A \rightarrow B$ and $g:B \rightarrow C$, then for any $a \in A$, $f(a) \in B$. But $B$ is the domain of $g$, so $g$ can be applied to $f(a)$. This yields $g(f(a))$, an element of $C$. Thus we have established a correspondence between $a$ in $A$ and $g(f(a))$ in $C$. This correspondence is called the **composition** function of $f$ and $g$ denoted by $g \circ f$. It defined a function $g \circ f :A \rightarrow C$ given by 
$$
(g \circ f)(a) = g(f(a)) \ \forall a \in A
$$
In terms of ordered pairs we have 
$$
g \circ f = \{(a,c) \in A \times C : \exists \ b \in B \ni (a,b) \in f \ \text{and} \ (b,c) \in g\}
$$

**Theorem 3.20**  Let $f:A \rightarrow B$ and $g:B \rightarrow C$. Then 
1. If $f$ and $g$ are surjective, then $g \circ f$ is surjective
2. If $f$ and $g$ are injective, then $g \circ f$ is injective
3. If $f$ and $g$ are bijective, then $g \circ f$ is bijective

---
#### Inverse Functions 
Given a function $f:A \rightarrow B$, we have seen how $f$ determined a relationship between subsets of $B$ and subsets of $A$. Now, we can extend this idea so that $f^{-1-}$ can be applied to a point in $B$ to obtain a point in $A$. 

```ad-Definition
Let $f:A \rightarrow B$ be bijective. The **inverse function** of $f$ is the function $f^{-1}$ given by 
$$
f^{-1} = \{(y,x) \in B \times A: (x,y) \in f\}
$$

```

![[Pasted image 20240130131733.png|center]]

If $f:A \rightarrow B$ is bijective, then it follows that $f^{-1}:B \rightarrow A$ is also bijective. Indeed, since $dom \ f = A$ and $rng \ f=B$ ,we have $dom \ f^{-1} = B$ and $rng \ f^{-1}=A$. Thus $f^{-1}$ is a mapping from $B$ onto $A$. Since $f$ is a function, a given $x$ in $A$ can correspond to only one $y$ in $B$. This means that $f^{-1}$ is injective, and hence bijective. 

When $f$ is following by $f^{-1}$, the effect is to map $x$ in $A$ onto $f(x)$ in $B$ and then back to $x$ in $A$. That is, $f^{-1}\circ f)(x)=x$, for every $x \in A$. A function defined on a set $A$ that maps each element in $A$ onto itself if called the **identity function** on $A$, and is denoted by $i_{A}$. Thus we can say $f^{-1} \circ f = i_{A}$. Furthermore, if $f(x)=y$, then $x=f^{-1}(y)$, so that 
$$
(f \circ f^{-1})(y) = f(f^{-1}(y)) = f(x)=y
$$
Thus $f \circ c^{-1} = i_{B}$. 

**Theorem 3.24** Let $f:A \rightarrow B$ be bijective. Then 
1. $f^{-1}:B \rightarrow A$ is bijective
2. $f^{-1}\circ f = i_{A}$ and $f \circ f^{-1} = i_{B}$

We also have another important theorem to take note of:

**Theorem 3.28**  Let $f:A \rightarrow B$ and $g:B \rightarrow C$ be bijective. Then the composition $g \circ f:A \rightarrow C$ is bijective and $(g \circ f)^{-1} = g^{-1}\circ f^{-1}$.

## Cardinality 
The properties of cardinality come from trying to compare the sizes of two set. 

```ad-Definition
Two sets $S$ and $T$ are called **equinumerous**, and we write $S \sim T$, if there exists a bijective function from $S$ onto $T$. 
```

```ad-Definition
A set $S$ is said to be **finite** if $S = \emptyset$ or if there exists $n \in \mathbb{N}$ and a bijection $f:\{1,2,\ldots,n\} \rightarrow S$. If a set is not finite, it is said to be **infinite**. 
```

It will be convenient to abbreviate the set $\{1,2,\ldots,n\}$ by $I_{n}$. This we can say that $S$ is finite iff $S=\emptyset$ or $S$ is equinumerous with $I_{n}$ for some $n \in \mathbb{N}$. 

```ad-Definition
The **cardinal number** of $I_{n}$ is $n$, and if $S \sim I_{n}$, we say that $S$ has **n elements**. The cardinal number of $\emptyset$ is taken to be $0$. IF a cardinal number is not finite, it is called **transfinite**. 
```

```ad-Definition
A set $S$ is said to be **denumerable** if there exists a bijection $f: \mathbb{N} \rightarrow S$. IF a set is finite or denumerable, it is called **countable**. If a set is not coutnable, it is **uncountable**. The cardinal number of a denumerable set is denoted by $\aleph_{0}$. 
```

In other words, a set is denumerable iff it is equinumerous with the set of natural numbers $\mathbb{N}$. The relationships between the various "sizes" of sets are illustrated below. The cardinal number of a denumerable set is denoted by $\aleph_{0}$.

![[Pasted image 20240130134331.png|center]]

**Theorem 4.9**  Let $S$ be a countable set and let $T \subset S$. Then $T$ is countable. 

**Theorem 4.10**  Let $S$ be a nonempty set. The following three conditions are equivalent:

1. $S$ is countable
2. There exists an injection $f:S \rightarrow \mathbb{N}$
3. There exists a surjection $g:\mathbb{N}\rightarrow S$

---
**Theorem 4.12**  The set $\mathbb{R}$ of real numbers is uncountable. 

**Remark.**  For a better proof look at Rudin's PMA

---
It would seem at first glance that the set $\mathbb{N}$ of natural numbers should be "bigger" than the set $E$ of even natural numbers. Indeed, this must be true. But that is half of $\aleph_{0}$? Our experience with finite sets is a poor guide here, for $\mathbb{N}$ and $R$ are actually equinumerous! The function $f(n)=2n$ is a bijection from $\mathbb{N}$ onto $E$, so $E$ also has cardinality $\aleph_{0}$. 

---
### Ordering of Cardinal Numbers
We conclude this article by returning to our original question about comparing the size of two sets. We would like to make some sense out of the notion that one set is "bigger". For finite sets, this is easy. However, such simplicity does not hold for infinite sets. 

A more fruitful approach is built on our definition of functions. Intuitively, if $f:S\rightarrow T$ is injective, then $S$ can eb no larger than $T$. Not only is this true for finite sets, but we have observed that it also holds for countable sets. Since we think of cardinal numbers as representing the size of a set, we shall use them when comparing sets. 

```ad-Definition
We denote the cardinal number of a set $S$ by $|S|$, so that we have $|S|=|T|$ iff $S$ and $T$ are equinumerous. That is, $|S|=|T|$ iff there exists a bijection $f:S\rightarrow T$. We define $|S|\leq |T|$ to mean that there exists an injection $f:S \rightarrow T$. As usual, if $|S|<|T|$, then $|S|\leq |T|$ and $|S|\neq |T|$.
```

**Theorem 4.15**  Let $S,T$, and $U$ be sets. Then
1. If $S \subseteq T$, then $|S|\leq |T|$. 
2. $|S|\leq |S|$
3. If $|S| \leq |T|$ and $|T| \leq |U|$, then $|S| \leq |U|$. 
4. If $m,n \in \mathbb{N}$ and $m \leq n$, then $|\{1,2,\ldots,m\}| \leq |\{1,2,\ldots,n\}|$. 
5. If $S$ is finite, then $|S|\leq \aleph_{0}$. 

```ad-Definition
Given any set $S$, let $P(S)$ dnote the collection of all subsets of $S$. The set $P(S)$ is called the **power set** of $S$. 
```

**Theorem 4.18**  For any set $S$, we have $|S|<|P(S)|$. 