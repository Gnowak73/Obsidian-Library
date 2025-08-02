---
tags:
  - Math
  - group
  - groups
  - subgroup
  - finite
  - theorem
  - modular
  - centers
  - centralizers
  - centralizer
dg-publish: true
mathLink:
---
Subject: _Algebraic Systems_
Main\_Topic: _Finite Groups, Subgroups_
Applications: _Group Theory, symmetries_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[Cyclic Groups]],[[Permutation Groups]]_
Cont.\_ of: _None_ 
_
_

As we will soon discover, finite groups---that is, groups with finitely man elements---have interesting arithmetical properties. To facilitate the study of finite groups, it is convenient to introduce some terminology and notation. 

```ad-Definition
The **Order** of a group (finite or infinite) is the number of elements, usually denoted by $|G|$. 
```

Thus, the group $\mathbb{Z}$ of integers under addition has infinite order, while the group $U(10)=\{1,3,7,9\}$ under multiplication modulo $10$ has order $4$. 

```ad-Definition
The **Order** of an element $g$ in a group $G$ is the smallest positive integer $n$ such that $g^{n}=e$. If no such integer exists, we say $g$ has _infinite order_. The order of an element $g$ is denoted by $|g|$. 
```

So, to find the order of a group element $g$ you need to only compute the sequence of products $g,g^{2},g^{3},\ldots$, until you reach the identity for the first time. The exponent of this product (or coefficient if the operation is addition) is the order of $g$. If the identity never appears in the sequence, then $g$ has infinite order.

We may notice that among examples in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|Algebraic Systems Textbook]], that some some groups are subsets of others with the same binary operation. This situation arises so often that we introduce a special term to describe it.

```ad-Definition
If a subset $H$ of a group $G$ is itself a group under the operation of $G$, we sa $H$ is a _subgroup_ of $G$. 
```

We use the notation $H\leq G$ to mean $H$ is a subgroup of $G$. If we want to indicate that $H$ is a subgroup of $G$, but not equal to $G$ itself, we write $H<G$. Such a subgroup is called a _proper subgroup_. The subgroup $\{e\}$ is called a _nontrivial subgroup_ of $G$. 

**Remark.**  Notice that $Z_{n}$ under addition modulo $n$ is _not_ a subgroup of $Z$ under addition, since addition modulo $n$ is not the operation of $Z$.

### Subgroup Tests
When determining whether or not a subset $H$ of a group $G$ is a subgroup of $G$, one need not directly verify the group axioms. The next three results provide simple tests that suffice to show a subset of a group is a subgroup. 

**Theorem 3.1**  Let $G$ be a group and $H$ a nonempty subset of $G$. Then, $H$ is a subgroup of $G$ if $H$ is _closed under division_; that is, if $ab^{-1}$ is in $H$ _whenever_ $a$ and $b$ are in $H$. 

**Proof:**  Since the operation of $H$ is the same as that of $G$, it is clear that this operation is associative. Next, we show that $e$ is in $H$. Since $H$ is nonempty, we may pick some $x$ in $H$. Then, letting $a=x$ and $b=x$ in the hypothesis, we have $e=xx^{-1}=ab^{-1}$ is in $H$. To verify that $x^{-1}$ is in $H$ whenever $x$ is in $H$, all we need to do is choose $a=e$ and $b=x$ in the statement of the theorem. Finally, the proof will be complete when we show that $H$ is closed; that is, if $x,y$ belong to $H$, we must show $xy$ is in $H$ also. Well, we have already shown that $y^{-1}$ is in $H$ whenever $y$ is; so letting $a=x$ and $b=y^{-1}$, we have $xy=x(y^{-1})^{-1}=ab^{-1}$ is in $H$. 

1. Find the defining property $P$ of $H$ and use it to show that $H$ is nonempty
2. _Assume_ that two elements $a$ and $b$ have this property $P$.
3. Use the assumption to show that $ab^{-1}$ has property $P$. 

```ad-note
Notice that we can prove a subset of a group is _not_ a subgroup by three possible ways:

1. Show that the identity is not in the set.
2. Exhibit an element of the set whose inverse is not in the set.
3. Exhibit two elements of the set whose product is not in the set. 
```


---

**Theorem 3.2**  Let $G$ be a group and $H$ a _nonempty subset_ of $G$. Then, $H$ is a subgroup of $G$ if $ab \in H$ whenever $a,b \in H$ (closed under multiplication), _and_ $a^{-1} \in H$ whenever $a \in H$ (closed under inverse).   

**Proof:**  By the Theorem 3.1, it suffices to show that $a,b \in H$ implies $ab^{-1}\in H$. So, we suppose that $a,b \in H$. Since $H$ is closed under inverse, we also have $b^{-1}\in H$. Thus $ab^{-1} \in H$ by closure under multiplication. 

---

**Theorem 3.3**  Let $H$ be a _nonempty finite subset_ of a group $G$. Then, $H$ is a subgroup of $G$ if $H$ is _closed under the operation_ of $G$. 

**Proof:**  In view of Theorem 3.2, we need only prove that $a^{-1}\in H$ whenever $a \in H$. If $a=e$, then $a^{-1}=a$ and we are done. If $a\neq e$, consider the sequence $a,a^{2},a^{3}\ldots$. Since $H$ is finite and closure implies that all positive powers of $a$ are in $H$, not all of these elements are distinct. Say, $a^{i}=a^{j}$ and $i>j$. Then $a^{i-j}=e$; and since $a\neq e, i-j>1$. Thus, $a^{i-j}=a\cdot a^{i-j-1}=e$ and, therefore, $a^{i-j-1}=a^{-1}$. But, $i-j-1\geq 1$ implies $a^{i-j-1} \in H$ and we are done.

---

**Theorem 3.4**  Let $G$ be a group, and let $a$ be any element of $G$. Then 
$$
\left< a \right> = \{a^{n} \vert \ n \in Z\}
$$
is a subgroup of $G$. ($a^{0}$ is defined to be the identity)

**Proof:**  Let $a^{n},a^{m} \in \left<a \right>$. Then, $a^{n} \cdot (a^{m})^{-1} = a^{n-m} \in \left<a \right>$; so, by Theorem 3.1, $\left<a \right>$ is a subgroup of $G$. 

**Remark.**  The subgroup $\left<a \right>$ defined in this Theorem 3.4 is called the _cyclic subgroup_ of $G$ _generated_ by $a$.  Also note that $a^{i}a^{j}=a^{j+i}=a^{j}a^{i}$, which means that **every cyclic group is Abelian**. 

#### Centers
We next consider one of the most important subgroups.

```ad-Definition
The center $Z(G)$ of a gorup $G$ is the subset of elements in $G$ that commute with every element of $G$. In symbols, 
$$
Z(G) = \{a \in G \ \vert \ ax=xa \ \forall x \in G\}
$$
```

**Theorem 3.5**  The center of a group $G$ is a subgroup. 

**Proof**  For variety, we shall use Theorem 3.2 to prove this result. Clearly, $e \in Z(G)$, so $Z(G)$ is nonempty Now, suppose that $a,b \in Z(G)$. Then $(ab)x=a(xb)=(ax)b=x(ab)$ for all $x \in G$; and, therefore, $ab \in Z(G)$. 

Next, assume that $a \in Z(G)$. Then, we have $ax=xa$ for all $x$ in $G$. What we want is $a^{-1}x=xa^{-1}$ for all $x$ in $G$. Informally, all we need to do is obtain the second equation from the first one is to simultaneously bring the $a$'s across the equal sign. Thus, we have $xa^{-1}=a^{-1}x$. 

The $a$ on the left comes across as $a^{-1}$ on the left and the $a$ on the right comes across as an $a^{-1}$ on the right.) Formally, the desired equation can be obtained from the original one by multiplying it on the left and right by $a^{-1}$ like so 
$$
\begin{gathered}
a^{-1}(ax)a^{-1} = a^{-1}(xa)a^{-1}, \\
exa^{-1} = a^{-1}xe, \\
xa^{-1}=a^{-1}x
\end{gathered}
$$
This shows that $a^{-1} \in Z(G)$ whenever $a \in Z(G)$.

###### Centralizer
```ad-Definition
Let $a$ be a fixed element of a group $G$. The _centralizer_ of $a$ in $G$, $C(a)$, is the set of all elements in $G$ that commute with $a$. In symbols, $C(a)=\{g \in G \rvert \ ga=ag\}$
```

**Theorem 3.6**  $C(a)$ is a subgroup of $G$. This can be shown in a proof similar to **Theorem 3.5**. 