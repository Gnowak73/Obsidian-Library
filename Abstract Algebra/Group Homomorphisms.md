---
tags:
  - Math
  - Isomorphic
  - Isomorphism
  - homomorphic
  - homomorphism
  - groups
  - group
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Group Homomorphisms_
Applications: _Group Theory_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[Group Isomorphism]]_
Cont.\_ of: _None_ 
_
_

We will now consider one of the most fundamental ideas of algebra$-$homomorphisms. The term _homomorphism_ comes from the Greek words _homo_, meaning "like" and _morphe_, meaning form. We will see that a homomorphisms is a natural generalization of an [[Group Isomorphism|isomorphism]] and that there is an intimate connection between [[Normal Subgroups and Factor Groups|factor groups]] of a group and homomorphisms of a group. This concept was first introduced by Camille Joran in 1870. 

```ad-Definition
A **homomorphism** $\phi$ from a group $G$ to a group $\overline{G}$ is a mapping from $G$ to $\overline{G}$ that preserves the group operation; that is, $(ab)\phi=(a \phi)(b \phi)$ for all $a,b$ in $G$. 
```

Before giving examples and stating numerous properties of homomorphisms, it is convenient to introduce an important subgroup that is intimately related to the image of a homomorphism. 

```ad-Definition
The _kernel_ of a homomorphism $\phi$ from a group $G$ to a group with identity $e$ is the set $\{x \in G \vert \ x \phi = e\}$. The kernel of $\phi$ is denoted by $Ker \ \phi$.
```

**Remark.**  Any isomorphism is a homomorphism that is 1:1 and onto. The kernel of an isomorphism is the identity. 

**Example.**  The mapping of $\phi$ from $Z$ to $Z_{n}$, defined by $m \phi=r$ where $r$ is the remainder of $m$ when divided by $n$, is a homomorphism. The kernel of this mapping is $\left<n \right>$. 

The natural homomorphism from $Z$ to $Z_{n}$ has many applications in number theory. Lagrange used it to prove that every positive integer can be written as the sum of four squares. 

When defining a homomorphism from a group in which there are several ways to represent the elements, caution must be exercised to ensure that the correspondence is a function. (the term _well defined_ is often used in this context). For example, one might believe that the correspondence $x \rightarrow 3x$ from $Z_{3}$ to $Z_{6}$ is a homomorphism. But it is not a function since $0=3$ in $Z_{3}$, but $3 \cdot 0 \neq 3 \cdot 3$ in $Z_{6}$. 

##### Properties of Homomorphisms
**Theorem 11.1**  Let $\phi$ be a homomorphism from a group $G$ to a group $\overline{G}$. Let $g$ be an element of $G$ and $H$ a subgroup of $G$. Then 
1. $\phi$ carries the identity of $G$ to the identity of $\overline{G}$. 
2. $g^{n}\phi=(g \phi)^{n}$
3. $H \phi = \{h \phi \vert \ h \in H\}$ is a subgroup of $\overline{G}$. 
4. If $H$ is [[Cyclic Groups|cyclic]], then $H \phi$ is cyclic. 
5. If $H$ is Abelian, then $H \phi$ is Abelian.
6. If $H$ is normal in $G$, then $H \phi$ is normal in $G \phi$.
7. If $|g|=n$, then $|g \phi|$ divides $n$.
8. If $g \phi = g'$, then $g' \phi^{-1} = \{x \in G \vert x \phi = g'\} = g \ Ker \ \phi$
9. If $|H|=n$, then $|H \phi|$ divides $n$.
10. If $|Ker \ \phi|=n$, then $\phi$ is an n-to-1 mapping from $G$ onto $G \phi$.
11. If $\overline{K}$ is a subgroup of $\overline{G}$, then $\overline{K}\phi^{-1}=\{k \in G \vert \ k \phi \in \overline{K}\}$ is a subgroup of $G$. 
12. If $\overline{K}$ is a normal subgroup of $\overline{G}$, then $\overline{K}\phi^{-1}$ is a _normal subgroup_ of $G$.
13. If $\phi$ is onto and $Ker \ \phi=\{e\}$, then $\phi$ is an isomorphism from $G$ to $\overline{G}$. 

**Proof:**  The proof can be seen in Chapter 11 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]].

A few remarks about Theorem 11.1 are in order here. Typically, one should remember the various parts of the theorem in works. For example, part 4 says the homomorphic image of a cyclic group is cyclic. Part 6 says that the homomorphic image of a normal subgroup of $G$ is normal in the image of $G$. The set $g'\phi^{-1}$ defined in part 8 is called the _inverse image_) of $g'$ (or _pullback_) of $g'$. Note that the inverse image of an element is a coset of the kernel. Similarly, the set $\overline{K}\phi^{-1}$ defined in part 11 is called the _inverse image_ of $\overline{K}$ (or _pullback_ of $\overline{K}$). Part 8 is reminiscent of something from linear algebra and differential equations. Recall that if $x$ is a particular solution to a system of linear equations and $S$ is the entire solution set of the corresponding homogenous system of linear equation, then $x+S$ is the entire solution set of the nonhomogeneous systems. In reality, this statement is just a special case of part 8. 

**Corollary.**  Let $\phi$ be a group of homomorphism from $G$ to $\overline{G}$. Then $Ker \ \phi$ is a normal subgroup of $G$. 

#### The First Isomorphisms Theorem
**Theorem 11.2**  (Jordan 1870)  Let $\phi$ be a group homomorphism from $G$ to $\overline{G}$. Then the mapping from $G/Ker \ \phi$ to $G \phi$, given by $g \ Ker  \ \phi \rightarrow g \phi$ is an isomorphism. In symbols, $G/Ker \ \phi\approx G \phi$. 

**Proof:**  The proof can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]] on Chapter 11. 

**Theorem 11.3**  Every [[Normal Subgroups and Factor Groups|normal subgroup]] of a group $G$ is the kernel of a homomorphism of $G$. In particular, a normal subgroup $N$ is the kernel of the mapping $g \rightarrow gN$ from $G$ to $G/N$.

**Proof:**  Define $\phi:G \rightarrow G/N$ by $g \phi = gN$. (This mapping is called the natural homomorphism from $G$ to $G/N$) Then, $(xy) \phi = (xy)N = xNyN=x \phi y \phi$. 







