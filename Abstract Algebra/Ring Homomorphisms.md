---
tags:
  - ring
  - rings
  - homomorphic
  - homomorphism
  - Isomorphic
  - Isomorphism
  - field
  - kernel
  - Math
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Ring Homomorphisms_
Applications: _None_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 2_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Group Homomorphisms]],[[Group Isomorphism]].[[Introduction to Rings]]_
Cont.\_ of: _None_ 
_
_

In our work with groups, we saw that one way to discover information about a group was to examine its interaction with other groups by way of homomorphisms. It should not be surprising to learn that this concept extends to rings with equally profitable results. 

Just as a group homomorphism preserves the group operation, a ring homomorphism preserves the ring operations. 

```ad-Definition
A ring _homomorphism_ $\phi$ from a ring $R$ to a ring $S$ is a mapping from $R$ to $S$ that preserves the two ring operations; that is, 
$$
(a+b)\phi = a \phi + b \phi \quad \text{and} \quad (ab)\phi = (a \phi)(b \phi) \quad \forall a,b \in R
$$
```

A 1:1 ring homomorphism that is also onto is called a (ring) _isomorphism_. 

As was the case for groups, in the preceding definition the operations of the left of the equal signs are those of $R$, while the operations on the right of the equal sign are those of $S$. As with group theory also, the roles of isomorphism and homomorphism are entirely distinct.

![[Pasted image 20231018103913.png|center]]

An isomorphism is used to show two rings are algebraically identical; a homomorphism is used to simplify a ring while retaining certain of its features. 

A schematic representation of a ring homomorphism is given in the figure above. The dashed arrow indicate the results of performing the ring operations. 

---
#### Properties of Ring Homomorphisms

**Theorem 17.1**  Let $\phi$ be a homomorphism from a ring $R$ to a ring $S$. Let $A$ be a subring of $R$ and $B$ an ideal of $S$. 
1. For any $r \in R$ and any positive integer $n$, $(nr)\phi = n(r \phi)$ and $r^{n}\phi = (r \phi)^{n}$.
2. $A \phi = \{a \phi \vert \ a \in A\}$ is a subring of $S$.
3. If $A$ is an ideal and $\phi$ is onto $S$, then $A \phi$ is an ideal.
4. $B \phi^{-1} = \{r \in R \vert \ r \phi \in B\}$ is an ideal of $R$.
5. If $R$ is commutative, then $R \phi$ is _commutative_.
6. If $R$ has a unity $1$, $S \neq \{0\}$, and $\phi$ is onto, then $1\phi$ is the unity of $S$. 
7. $\phi$ is an isomorphism if and only if $\phi$ is onto and $Ker \ \phi = \{r \in R \vert \ r \phi = 0\} = \{0\}$. (See [[Group Homomorphisms]] for Kernel definition)
8. If $\phi$ is an isomorphism from $R$ onto $S$, then $\phi^{-1}$ is an isomorphism from $S$ onto $R$. 

**Proof:**  Most of these proofs can be directly seen from previous [[Group Isomorphism]] and [[Group Homomorphisms]], we shall leave them in the textbook to see on Page 225, [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

As with groups, one should learn in words the various parts of Theorem 17.1 in addition to the symbols. Part (2) says that the homomorphic image of a subring is a subring. Part (4) says that the pullback of an ideal is an ideal, and so on. 

**Theorem 17.2**  Let $\phi$ be a homomorphism from a ring $R$ to a ring $S$. Then $Ker \ \phi = \{r \in R \vert \ r \phi = 0\}$ is an ideal of $R$. 

---

**Theorem 17.3**  Let $\phi$ be a ring homomorphism from $R$ to $S$. Then the mapping from $R/Ker\ \phi$ to $R \phi$, given by $r+ Ker \ \phi \rightarrow r \phi$ is an isomorphism. In symbols, $R/Ker\ \phi\approx R \phi$. 

---

**Theorem 17.4**  Every ideal of a ring $R$ is the kernel of a ring homomorphism of $R$. In particular, an ideal $A$ is the kernel of the mapping $r \rightarrow r +A$ from $R$ to $R/A$. 

---

The homomorphism from $R$ to $R/A$ given in Theorem 17.4 is called the _natural homomorphism_ from $R$ to $R/A$. Theorem 17.3 is often referred to as the **Fundamental theorem of Ring Homomorphisms.** 

As a corollary to the next theorem, we see that a ring with unity contains a copy of $Z$ or $Z_{n}$. 

---
**Theorem 17.5**  Let $R$ be a ring with unity $e$. The mapping $\phi:Z \rightarrow R$ given by $n \rightarrow ne$ is a _ring homomorphism_. 

**Proof:**  For brevity, the proof will be omitted. It can be seen on page 226 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

---
**Corollary 1.**  If $R$ is a ring with unity and the characteristic of $R$ is $n>0$, then $R$ contains a subring isomorphic to $Z_{n}$. If the characteristic of $R$ is $0$, then $R$ contains a subring isomorphic to $Z$. 

**Proof:**  Once again, the proof an be seen on page 226 in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 


**Corollary 2.**  For any positive integer $m$, the mapping $\phi:Z\rightarrow Z_{m}$ given by $x \rightarrow x \mod m$ is a ring homomorphism. 

**Proof:**  This directly follows from the statement of Theorem 17.5, since in the ring $Z_{m}$, the integer $x \mod m$ is $x1$. 


**Corollary 3.**  If $F$ is a field of characteristic $p$, then $F$ contains a subfield isomorphic to $Z_{p}$. If $F$ is a field of characteristic $0$, then $F$ contains a subfield isomorphic to the rational numbers.

**Proof:**  By Corollary 1, $F$ contains a subring isomorphic to $Z_{p}$ if $F$ has characteristic $0$. In the latter case, let 
$$
T = \{ab^{-1} \vert \ a,b \in S, \ b\neq 0\}
$$
Then $T$ is isomorphic to the rationals. 

Since the intersection of all subfields of a field is itself a subfield, every field has a smallest subfield (that is, a subfield that is contained in every subfield). This subfield is called the _prime subfield_ of the field. It follows from Corollary 3 that the prime subfield of a field of characteristic $p$ is isomorphic to $Z_{p}$ while the prime subfield of a field of characteristic $0$ is isomorphic to $Q$.

##### The field of Quotients
Although the [[Integral Domains|integral domain]] $Z$ is not a field, it is at least contained in a field$-$the field of rational numbers. And notice that the field of rational numbers is nothing more than quotients of integers. Can we mimic the construction of the rationals from the integers for other integral domains? Yes.

**Theorem 17.6**  Let $D$ be an integral domain. Then there exists a field $F$ (called the field of quotients of $D$) that contains a subring isomorphic to $D$. 

**Proof:**  The proof is very long and meticulous, and thus will be left for further inquisition in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]] on page 228. 

In practice, it is customary to identify the equivalence class $[a/b]$ with the symbol $a/b$. This notation is less cumbersome and should not cause confusion. Again, the rational numbers provide a model, since we traditionally use $\frac{1}{2}$ in place of $[\frac{1}{2}]$, and so on. Just remember that $a/b$ and $c/d$ represent the same equivalence class if and only if $ad=cd$. 







