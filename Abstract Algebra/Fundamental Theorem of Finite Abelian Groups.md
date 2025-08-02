---
tags:
  - group
  - groups
  - finite
  - Abelian
  - fundamental_theorem_of_finite_abelian_groups
  - finite_abelian
  - theorem
  - Math
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Fundamental Theorem of Finite Abelian Groups_
Applications: _Group Theory_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]]_
Cont.\_ of: _None_ 
_
_

We will begin with the theorem that describes all finite Abelian groups in a standardized way. Before giving the proof, which is long and difficult, we discuss some consequences of the theorem and its proof. The first proof of the theorem was given by Leopold Kronecker in 1858.

**Theorem 12.1**  Every finite Abelian group is a direct product ([[External Direct Product]] and [[Internal Direct Products]]) of cyclic groups of prime-power order. Moreover, the factorization is unique except for rearrangement of the factors. 

---
Since a cyclic group of order $n$ is isomorphic to $Z_{n}$, Theorem 12.1 shows that every finite Abelian group $G$ is isomorphic to a group of the form 
$$
Z_{p_{1}^{n_{1}}} \oplus Z_{p_{2}^{n_{2}}} \oplus \ldots Z_{p_{k}^{n_{k}}}
$$
where the $p_{i}$ are not necessarily distinct primes and the prime-powers $p_{1}^{n_{1}},\ldots$ are uniquely determined by $G$. Writing a group in this form is called _determining the isomorphism class of_ $G$. 

##### The Isomorphism Classes of Abelian Groups
The fundamental theorem is extremely powerful. As an application, we can use it as an algorithm for constructing all Abelian groups of any order. Let's look at groups whose orders have the form $p^{k}$ where $p$ is prime and $k \leq 4$. 

![[Pasted image 20230926225836.png|center]]

In general, there is one group of order $p^{k}$ for each set of positive integers whose sum is $k$ (such a set is called a _partition_ of $k$); that is, if $k$ can be written as 
$$
k=n_{1}+n_{2}+\ldots n_{t}
$$
where each $n_{i}$ is a positive integer, then 
$$
Z_{p^{n_{1}}} \oplus Z_{p^{n_{2}}} \ldots \oplus Z_{p^{n_{t}}}
$$
is an Abelian group of order $p^{k}$. Furthermore, the uniqueness portion of the Fundamental Theorem guarantees that distinct partitions of $k$ yield distinct isomorphism classes. Thus, for example, $Z_{9}\oplus Z_{3}$ is not isomorphic to $Z_{3} \oplus Z_{3} \oplus Z_{3}$. A reliable mnemonic for comparing external direct products is the cancellation property: if $A$ if _finite_, then 
$$
A \oplus B \approx A \oplus C \quad \text{if and only if} \quad B \approx C.
$$
To fully appreciate the potency of the Fundamental Theorem, contrast the ease with which the Abelian groups of order $p^{k}, k\leq 4$, were determined with the corresponding problem for non-Abelian groups. Even a description of the two non-Abelian groups of order $8$ is a challenge, and a description of the nine non-Abelian groups of order 16 is well beyond the level of this text.

Now that we know how to construct all the Abelian groups of prime-power order, we move to the problem of constructing all Abelian groups of a certain order $n$ where $n$ has two or more distinct prime divisors. We begin by writing $n$ in prime-power decomposition form $n=p_{1}^{n_{1}}p_{2}^{n_{2}}\ldots p_{k}^{n_{k}}$. Next, individually form all Abelian groups of order $p_{1}^{n_{1}}$ and so on, as described earlier. Finally, form all possible external direct products of these. 

If we are given any particular Abelian group $G$ of certain order, where we have found all of the distinct isomorphism classes, how would we find out which class represents the structure of $G$? Again, we can answer this question by comparing the orders of the elements of $G$ with the orders of the elements in the distinct products, since it can be shown that two Abelian groups are isomorphic if and only if they have the same number of elements of each order. 

What if we have some specific Abelian group $G$ of order $p_{1}^{n_{1}}p_{2}^{n_{2}}\ldots p_{k}^{n_{k}}$ where the $p_{i}$'s are distinct primes? How can $G$ be expressed as an [[Internal Direct Products|internal direct product]] of the cyclic groups of prime-power order? For simplicity, let us say the group has $2^{n}$ elements. First, we must compute the orders of the elements. After this is done, pick an element of maximum order $2^{r}$, call it $a_{1}$. Then $\left<a_{1} \right>$ is one of the factors in the desired internal direct product. If $G \neq \left<a_{1}\right>$ chose an element $a_{2}$ of maximum order $2^{s}$ such that $s\leq n - r$ and none of $a_{2},a_{2}^{2},\ldots a_{2}^{2^{(s-1)}}$ is in $\left<a_{1}\right>$. Then $\left<a_{2}\right>$ is a second direct factor. If $n \neq r+s$, select an element $a_{3}$ of maximum order $2^{r}$ such that $t \leq n-r-s$ and.... continue the previous methods. We continue this fashion until our direct product has the same order as $G$. A formal presentation of this algorithm is as follows:

**Greedy Algorithm for an Abelian Group of Order $p^{n}$** 
1. Compute the orders of the element of the group $G$.
2. Select an element $a_{1}$ of maximum order and define $G_{1}=\left<a_{1}\right>$. Set $i=1$.
3. If $|G|=|G_{i}|$, stop. Otherwise, replace $i$ by $i+1$.
4. Select an element $a_{i}$ of maximum order $p^{k}$ such that $p^{k}\leq |G|/|G_{i-1}|$ and none of $a_{i},a_{i}^{p},\ldots,a_{i}^{p^{k-1}}$ is in $G_{i-1}$, and define $G_{i}=G_{i-1} \times \left<a_{i} \right>$
5. Return to step 3.

In the general case where $|G|=p_{1}^{n_{1}}p_{2}^{n_{2}}\ldots p_{k}^{n_{k}}$ one simply uses the algorithm to build up a direct product of order $p_{1}^{n_{1}}$, then another of order $p_{2}^{n_{2}}$, and so on. The direct product of all of these pieces is the desired factorization of $G$. 

**Corollary.**  If $m$ divides the order of a finite Abelian group $G$, then $G$ has a subgroup of order $m$.

#### Proof of the Fundamental Theorem
Because of the length and complexity of the proof for the Fundamental Theorem of Finite Abelian Groups, we will express the lemmas and leave the proofs to be seen in Chapter 12 of [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]].

**Lemma 1.**  Let $G$ be a finite Abelian group of order $mn$ where $m$ and $n$ are relatively prime. If $H=\{x\in G \vert \ x^{m}=e\}$, and $K=\{x\in G \vert \ x^{n}=e\}$, then $G=H \times K$. 

**Lemma 2.**  Let $G$ be an Abelian group of prime-power order and let $a$ be an element of maximal order in $G$. Then $G$ can be written in the form $\left<a \right> \times K$. 

**Lemma 3.**  A finite Abelian group of prime power order is a direct product of cyclic groups.

**Lemma 4.**  Suppose $G$ is a finite Abelian group of prime-power order. If $G=H_{1}\times H_{2}\ldots \times H_{m}$ and $G = K_{1}\times K_{2}\times\ldots \times K_{n}$, where the $H$'s and $K$'s are nontrivial cyclic subgroups with $|H_{1}|\geq|H_{2}|\geq \ldots\geq|H_{m}|$ and $|K_{1}|\geq|K_{2}|\geq \ldots \geq |K_{n}|$, then $m=n$ and $|H_{i}|=|K_{i}|$ for all $i$. 