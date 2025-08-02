---
tags:
  - Math
  - groups
  - group
  - Normal
  - subgroup
  - factor
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Normal Subgroups and Factor Groups_
Applications: _Group Theory_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[Finite Groups, Subgroups]]_
Cont.\_ of: _None_ 
_
_

As we have seen in [[Cosets and Lagrange's Theorem]], if $G$ is a group and $h$ is a subgroup of $G$, it is not always true that $aH=Ha$ for all $a$ in $G$. There are certain situations where this does hold, however, and these cases turn out to be of critical important in the theory of groups. It was Galois, about 150 years ago, who first recognized such subgroups were worthy of special attention.

```ad-Definition
A subgroup $H$ of a group $G$ is called a _normal subgroup_ if $aH=Ha$ for all $a$ in $G$. We denote this by $H \triangleleft G$.
```

There are several equivalent formulations of the definition of normality. We have chosen the one that is the easiest to use in applications. However, to verify that a subgroup is normal, it is usually better to use the next theorem. It allows us to substitute a condition about two subgroups of $G$ for a condition about two cosets of $G$. The proof can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

**Theorem 10.1**  A subgroup $H$ of $G$ is normal in $G$ if and only if $x^{-1}Hx \subseteq H$ for all $x$ in $G$. 

---
Many make the mistake of thinking that $H$ is normal in $G$ means $ah=ha$ for $a \in G$ and $h \in H$. This is not what normality of $H$ means; rather, it means that if $a \in G$ and $h \in H$, then there exists some $h' \in H$ such that $ah=h'a$. 

**Remark.**  The [[Finite Groups, Subgroups#Centers|Center]] of a group is always normal. The subgroup of rotations in $D_{n}$ is also normal to $D_{n}$. 

```ad-Remember
If $H$ has only two left cosets in $G$, then $H$ is normal in $G$. 
```

---
#### Factor Groups
we have yet to explain why normal groups are of special significance. The reason is simple. When the subgroup $H$ of $G$ is normal, then the set of left(or right) cosets of $H$ in $G$ is itself a group$-$called the _factor group of_ $G$ by $H$ (or the _quotient group of_ $G$ by $H$). Quite often, once can obtain information about a group by studying one of its factor groups. This method will be illustrated here.

**Theorem 10.2**  (O. Holder, 1889)  Let $G$ be a group and $H$ an a _normal subgroup_ of $G$. The set $G/H=\{aH \vert \ a \in G\}$ is a group under the operation $(aH)(bH)=abH$. 

**Proof:** Our first task is to show that the operation is well defined; that is, we must show the correspondence defined above from $\frac{G}{H}\times \frac{G}{H}$ into $G/H$ is actually a function. To do this, assume $aH=a'H$ and $bH=b'H$. Then $a'=ah_{1}$ and $b'=bh_{2}$ for some $h_{1},h_{2}$ in $H$, and therefore, $a'b'H=ah_{1}bh_{2}H=ah_{1}bH=ah_{1}Hb=aHb=abH$. Here we have used part 2 of the lemma from [[Cosets and Lagrange's Theorem]] and the fact that $H \triangleleft G$. The rest is easy: $eH=H$ is the identity; $a^{-1}H$ is the inverse of $aH$; and $(aHbH)ch=(ab)HcH=(ab)cH=a(bc)H=aH(bc)H=aH(bHcH)$. This proves that $G/H$ is a group. 

Although it is merely a curiosity, we point out that the converse of Theorem 10.2 is also true; that is, if the correspondence $aHbH=abH$ defined a group operation on the sets of left cosets of $H$ in $G$, then $H$ is normal in $G$. 

##### Applications of Factor Groups
Why are factor groups important? Well, when $G$ is finite and $H \neq \{e\}$, $G/H$ is smaller than $G$, and its structure is usually less complicated than that of $G$. At the same time, $G/H$ simulates $G$ in many ways. In fact, we may think of a factor group of $G$ as a less complicated approximation of $G$ (similar to using the rational number 3.14 for the irrational number $\pi$). What makes factor groups important is that one can often deduce properties of $G$ by examining the less complicated group $G/H$ instead. 

**Theorem 10.3**  Let $G$ be a group and $Z(G)$ the center of $G$. If $G/Z(G)$ is cyclic, then $G$ is Abelian.

**Proof:**  The proof can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]] near the end of Chapter 10. 

**Theorem 10.4**  For any group $G$, $G/Z(G)$ is isomorphic to $Inn(G)$. 

**Proof:**  The proof can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]] at the end of Chapter 10.

