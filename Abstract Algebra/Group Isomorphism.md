---
tags:
  - Math
  - group
  - groups
  - Isomorphic
  - Isomorphism
  - automorphic
  - innerautomorphic
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Group Isomorphism_
Applications: _Group Theory_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[Finite Groups, Subgroups]],[[External Direct Product]]_
Cont.\_ of: _None_ 
_
_

```ad-Definition
An _isomorphism_ $\phi$ from a group $G$ to a group $\overline{G}$ is a 1:1 mapping (or function) from $G$ onto $\overline{G}$ that preserves the group operation. That is 
$$
(ab)\phi = (a \phi)(b \phi) \quad \forall \ a,b, \in G
$$
If there si an isomorphism from $G$ onto $\overline{G}$, we say that $G$ and $\overline{G}$ are _isomorphic_ and write $G \approx \overline{G}$
```

There are four main steps in proving that a group $G$ is isomorphic to a group $\overline{G}$. 

1. "Mapping".  Define a candidate for the isomorphism; that is, define a function $\phi$ from $G$ to $\overline{G}$. 
2. "1-1".  Prove that $\phi$ is 1:1; that is, assume that $a \phi = b \phi$ and prove that $a=b$.
3. "Onto".  Prove that $\phi$ is onto; that is, for any element $\overline{g}$ in $\overline{G}$, find an element $g$ in $G$ such that $g \phi=\overline{g}$. 
4. "O.P".  Prove that $\phi$ is operation preserving; that is, show $(ab)\phi=a \phi b \phi$ for all $a$ and $b$ in $G$. 

Note that none of these steps is unfamiliar. The only one that may appear novel is the fourth one It requires that one may be able to obtain the same result my multiply two elements and then mapping, or by mapping two elements and then multiplying. 

```ad-Remember
The 4th condition, which is for [[Group Homomorphisms]], can be explained as follows.

If you have two elements $g_1, g_2 \in G$, there are two ways to produce an element in $\bar{G}$

1. use the binary operation $\ast$ of $G$ to produce the element $g_1\ast g_2$ of $G$, then apply the map $\phi$ to obtain $\phi(g_1\ast g_2) \in \bar{G}$.

2. apply the map $\phi$ to both $g_1$ and $g_2$ to obtain $\phi(g_1), \phi(g_2) \in \bar{G}$, then use the binary operation $\cdot$ of $\bar{G}$ to produce the element $\phi(g_1)\cdot\phi(g_2) \in \bar{G}$.

The map $\phi$ is said to preserve the binary operation if it doesn't matter which of the above two processes we use. That is, $\phi$ satisfies $\phi(g_1\ast g_2) = \phi(g_1)\cdot\phi(g_2)$ for every $g_1, g_2 \in G$. In some sense, $\phi$ maps 'products' in $G$ to 'products' in $\bar{G}$.
```


##### Cayley's Theorem
**Theorem.**  Every group is isomorphic to a group of permutations. More specifically, a finite group $G$ is isomorphic to a subgroup of $Sym(G)$. 

**Proof:**  The long proof can be seen on page 103, and later on in Chapter 27. of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]

**Remark.**  Perhaps the most important aspect of Cayley's Theorem is that it shows the present-day set of axioms we have adopted for a group in the correct abstraction of its much earlier predecessor: a group of permutations. Indeed, Cayley's Theorem tells us that abstract groups are not different from permutation groups. 

#### Properties of Isomorphism
**Theorem 6.1**  Suppose that $\phi$ is an isomorphism from a group $G$ onto a group $\overline{G}$. Then 
1. $\phi$ carries the identity of $G$ to the identity of $\overline{G}$
2. For every integer $n$ and for every group element $a$ in $G$, $a^{n} \phi = (a \phi)^{n}$
3. For any elements $a,b$ in $G$, $a$ and $b$ commute if and only if $a \phi$ and $b \phi$ commute. 
4. $G$ is Abelian if and only if $\overline{G}$ is Abelian
5. $|a|=|a \phi|$ for all $a$ in $G$ (isomorphisms preserve orders)
6. $G$ is cyclic if and only if $\overline{G}$ is cyclic. 
7. For a fixed integer $k$ and a fixed group element $b$ in $G$, the equation $x^{k}=b$ has the same number of solutions in $G$ as does the equation $x^{k}=b \phi$ in $\overline{G}$. 
8. $\phi^{-1}$ is an isomorphism from $\overline{G}$ onto $G$. 
9. If $K$ is a subgroup of $G$, then $K \phi = \{k \phi \vert \ k \in K\}$ is a subgroup of $\overline{G}$. 

**Proof:**  We will restrict ourselves to proving only (1) and (5). Note that (4) follows directly from (3), (6) follows directly from (5). For convenience, let us denote the identity in $G$ by $e_{G}$, and the identity in $\overline{G}$ by $e_{\overline{G}}$. Then $e_{G}=e_{G}e_{G}$ so that 
$$
e_{G}\phi = (e_{G}e_{G})\phi = (e_{G}\phi)(e_{G} \phi)
$$
But $e_{G} \phi \in \overline{G}$ so that $e_{G} \phi = e_{\overline{G}}(e_{G} \phi)$, as well. Thus, by cancellation ([[Groups#Cancellation|Group Cancellation]]) we have $e_{\overline{G}}=e_{G}\phi$. This proves (1). 

To prove (5), we note that $a^{n}=e$ if and only if $a^{n}\phi=e \phi$. So, by parts (1) and (2), $a^{n}=e$ if and only if $(a \phi)^{n}=e$. Thus, $a$ has infinite order if and only if $a \phi$ has infinite order, and $a$ has finite order $n$ if and only if $a \phi$ has order $n$.

Property (7) is quite useful for showing that two groups are _not_ isomorphic. Often $b$ is picked to be the identity. 

Theorem 6.1 shows that isomorphic groups have many properties in common. Actually, the definition is precisely formulated so that isomorphic groups have _all_ group theoretic properties in common. Admittedly, calling such groups equivalent, rather than the same, might be more appropriate. 

#### Automorphisms
Certain kinds of isomorphisms are referred to so often that they have been given special names.

```ad-Definition
An isomorphisms from a group $G$ onto itself is called an _automorphism_ of $G$. 
```

##### Inner Automorphism Induced by $a$
```ad-Definition
Let $G$ be a group, and let $a \in G$. The function $\phi_{a}$ defined by $x \phi_{a}=a^{-1} x a$ for all $x$ in $G$ is called the _inner automorphism of_ $G$ induced by $a$. 
```

When $G$ is a group, we use $Aut(G)$ to denote the set of all automorphisms of $G$; and $Inn(G)$ the set of all inner automorphisms of $G$. The reason these sets are noteworthy is demonstrated in the next theorem. 

##### Aut(G) and Inn(G) are Groups 
**Theorem 6.2**  The set of all automorphisms of a group and the set of inner automorphisms of a group are both groups. 

**Proof:**  Can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]] on Ch. 6.

**Theorem 6.3**  For every positive integer $n$, $Aut(Z_{n})$ is isomorphic to $U(n)$. 

**Proof:**  The proof can be seen at the end of Ch. 6 in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|alstract algebra textbook]]. 


