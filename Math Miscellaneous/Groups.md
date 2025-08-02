---
tags: Math, algebraic, systems, groups, sets,
dg-publish: true
mathLink: 
---
Subject: _Algebraic Systems_
Main\_Topic: _Groups_
Applications: _Group Theory and Symmetry_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf]]_
Closely\_Related\_To: _[[Properties of Integers, Algebra, and Functions]],[[Finite Groups, Subgroups]],[[Group Isomorphism]],[[External Direct Product]],[[Permutation Groups]],[[Cyclic Groups]],[[Normal Subgroups and Factor Groups]],[[Group Homomorphisms]],[[Cosets and Lagrange's Theorem]]_
Cont.\_ of: _None_ 
_
_

The study of groups arises from symmetries of objects. Suppose we remove a square from a plane, move it in some way, then put the square back into the space it originally occupied. Our goal is to describe in some reasonable fashion all possible ways this can be done. More specifically, we want to describe the possible relationships between the starting position of the square and tis final position in terms of motions.

Let us set up this notion of "movement" through rotations:

![[Pasted image 20230901092756.png|center]]

Let's investigate some consequences of the fact that every motion is equal to one of the eight listed above. Suppose that a square is repositioned by a rotation of $90^{\circ}$ followed by a rotation of $180^{\circ}$ about the horizontal axis of symmetry. In pictures, 

![[Pasted image 20230901092950.png|center]]

Thus, we see that this pair of motions-taken together- is equal to the single motion $D$. This observation motivates us to define an algebraic operation "followed by" on the set of motions. 

```ad-Definition
We say a motion $A$ _followed by_ a motion $B$ (written $AB$) is equal to the motion $C$ if, upon performing the motion $A$ and then the motion $B$, the net effect is the same as that produced by performing $C$ alone.
```

With this definition, we may now write $R_{90}H=D$. The eight motions above, together with the operation "followed by," for a mathematical system called the _dihedral group of order 8_ (the order of a group is the number of elements it contains). It is denoted by $D_{4}$. Rather than introduce the formal definition of a group here, let's look at some properties of groups by way of example $D_{4}$.

To facilitate future computations, we construct an _operation table_ or a _Caley table_ for $D_{4}$. The circled entry represents the fact that $D=R_{90}H$.

![[Pasted image 20230901093643.png|center]]

Notice how beautiful this table looks! Perhaps the most important feature is that it is completely filled in without introducing any new motions since, of course, any movement is just a combination of one of these eight. Algebraically, this says that if $A$ and $B$ are in $D_{4}$, then so is $AB$. This property is called _closure_ and it is one of the requirements for a mathematical system to be a group. 

Next, notice that if $A$ is any element in $D_{4}$, then $AR_{0}=R_{0}A$. Thus, we can say that $R_{0}$ can the property of _identity_. Another feature is that every element of $D_{4}$ appears exactly once in each row and column. This feature is something that all groups must have, and, indeed, it is quite useful to keep this fact in mind. As a consequence of this condition, we see that for each element $A$ in $D_{4}$, there is exactly one element $B$ in $D_{4}$ so that $AB=BA=R_{0}$. In this case, $B$ is said to be the _inverse_ of $A$ and vice versa. 

Another property of $D_{4}$ deserves special comment. Observe that $HD\neq DH$ but $R_{90}R_{180}=R_{180}R_{90}$. Thus, in a group, $AB$ may or may not be the same as $BA$. If it happens that $AB=BA$ for _all_ choices of group elements $A$ and $B$, we say the group is _commutative_ or, better yet, **Abelian**. Otherwise, we say the group is **non-Abelian**. 

Thus far, we have illustrated, by the way of $D_{4}$, three of the four conditions that define a group; namely, closure, existence of an identity, and existence of inverses. The remaining conditions required is _associativity_; that is, $(ab)c=a(bc)$ for all $a,b,c$ in the set. To be sure that $D_{4}$ is indeed a group, we should check this equation for each of the $8^{3}=512$ possible choices of $a,b,$ and $c$ in $D_{4}$. In practice, however, this is rarely done! Here, for example, we simply observe instead that each of the eight motions defines a function from the plane to itself, and the operation "followed by" is nothing other than function composition. Then, since function composition is associative, so is "followed by".  

###### Dihedral Group
The analysis carried our for the square can similarly be done for an equilateral triangle or a regular polygon. The corresponding group is denoted by $D_{n}$ and is called the _dihedral group_. The dihedral group is the group of symmetries and reflections for all polygons of sides $n \geq 1$.

These basic symmetric and properties of our operation is an example of what we call a group.

---
### Groups
The term _group_ was coined by Galois to describe sets of one-to-one functions on finite sets that could be group together to form a closed set.

```ad-Definition
Let $G$ be a set. A _binary operation_ on $G$ is a function that assigns each ordered pair of elements of $G$ an element of $G$. 
```

A binary operation on a set $G$, then, is simple a method (or formula) by which an ordered pair from $G$ combine to yield a new member of $G$. The most familiar binary operations are ordinary addition, subtraction, and multiplication of integers. Division of integers is not a binary operation on the integers (because an integer divided by an integer need not be an integer). 

The binary operations addition $\mod n$ and multiplication $\mod n$ on the set $\{0,1,2,\ldots,n-1\}$, which we denote by $Z_{n}$, play an extremely important role in abstract algebra. In certain situations we will want to combine the elements of $Z_{n}$ by addition $\mod n$ only; in other situations we will want to combine the elements of $Z_{n}$ by addition $\mod n$ only; in other situations we will want to use both addition $\mod n$ and multiplication $\mod n$ to combine the elements. It will be clear from the context whether we are using addition only or addition and multiplication. For example, when multiplying matrices with entries from $Z_{n}$, we will need both addition $\mod n$ and multiplication $\mod n$. 


```ad-Definition
Let $G$ be a nonempty set together with a binary operation that assigns to each ordered pair $(a,b)$ of elements of $G$ an element in $G$ denoted by $ab$. We say $G$ is a _group_ under this operation if the following three properties are satisfied:

1. $a(bc)=(ab)c$ (**associativity**)
3. there is some $1 \in G$ such that $a\cdot 1=a, \  \forall a \in G$ (**identity**)
3. For every $a \in G$, there is an $a^{-1} \in G$ such that $a \cdot a^{-1} = 1$. (**inverses**)
```

In words, then, a group is a set together with an associative operation such that every element has an inverse and any pair of elements can be combined without going outside the set. This latter condition is called _closure_. 

If a group has the property $ab=ba$ for every pair of elements $a$ and $b$, we say that the group is _Abelian_. 

##### Elementary Properties of Groups

###### Uniqueness of the Identity
**Theorem 1.**  In a group $G$, there is only one identity element.

**Proof:**  Suppose that both $e$ and $e'$ are identity elements of $G$. Then,
1. $ae=a, \ \forall a\in G$ 
2. $e'a=a, \ \forall a \in G$

The choice of $a=e'$ in (1) and $a=e$ in (2) yields $e'e=e$ and $e'e=e'$. Thus, $e$ and $e'$ are both equal. 

**Remark.**  Because of this theorem, we may unambiguously speak of "the identity" of a group and denote it by "$e$".

###### Cancellation
**Theorem 2.**  In a group $G$, the right and left cancellation laws hold; that is, $ba=ca$ implies $b=c$ and $ab=ac$ implies $b=c$. 

**Proof:**  Suppose that $ba=ca$. Let $a'$ be an inverse of $a$. Then, multiplying on the right by $a'$ gives $(ba)a' = (ca)a'$. Associativity yields $b(aa')=c(aa')$. Then, $be=ce$ and, therefore, $b=c$. Similarly, one can prove that $ab=ac$ implies that $b=c$ by multiplying $a'$ on the left. 

---

A consequence of the cancellation property is the fact that in a Caley table for a group, each group element occurs exactly once in each row and column. Another consequence of the cancellation property is the uniqueness of inverses. 

###### Uniqueness of Inverses
**Theorem.**  For each element $a$ in a group $G$, there is a unique element $b$ in $G$ such that $ab=ba=e$. 

**Proof:** Suppose that $b$ and $c$ are both inverses of $a$. Then $ab=e$ and $ac=e$ so that $ab=ac$. Now cancel $a$. 

---
As was the case with the identity element, it is reasonable, in view of this theorem, to speak of "the inverse" of an element $g$ of a group; and, in fact, we may unambiguously denote it by $g^{-1}$. This notation is suggested by that used for ordinary real numbers under multiplication. Similarly, when $n$ is a positive integer, $g^{n}$ is used to denote the product $gg\ldots g$; we may define $g^{0}=e$; when $n$ is negative, we define $g^{n}=(g^{-1})^{-n}$. 

With this notation, the familiar laws of exponents hold for groups; that is, for all integers $m$ and $n$ in any group element $g$, we have $g^{m}g^{n}=g^{m+n}$ and $(g^{m})^{n}=g^{mn}$. Although the way one manipulates these expressions coincides with the laws of exponents for real numbers, the law of exponents fail to hold for expressions involving two group elements. Thus, for groups in general, $(ab)^{n}\neq a^{n}b^{n}$. 

**Remark.**  It is important to not let the notation confuse you when working with an addition operation. Since $g^{3}=g+g+g$ if $+$ is our binary operation; and $g^{-3} = (-g)+(-g)+(-g)$. 

**Theorem (Shoes and Socks):**  For $a,b\in G$, $(ab)^{-1}=b^{-1}a^{-1}$.

**Proof:**  $(ab)(b^{-1}a^{-1})=abb^{-1}a^{-1}=aea^{-1}=aa^{-1}=e$, such that $(ab)(b^{-1}a^{-1})=e$, then $b^{-1}a^{-1}=(ab)^{-1}.$ 





 