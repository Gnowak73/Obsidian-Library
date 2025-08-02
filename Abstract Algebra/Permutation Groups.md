---
tags:
  - Math
  - Permutation
  - group
  - groups
  - permute
  - ruffini
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Permutation Groups_
Applications: _Group Theory_
Examples: _None_
Class: _None_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[Finite Groups, Subgroups]],[[Cyclic Groups]]_
Cont.\_ of: _None_ 
_
_

We will now focus on studying certain groups of functions, called permutation groups, from a set $A$ to itself.

```ad-Definition
A _permutation_ of a set $A$ is a function from $A$ to $A$ that is both 1:1 and onto. A _permutation group_ of a set $A$ is a set of permutations of $A$ that forms a group under function composition. 
```

Although groups of permutations of any nonempty set $A$ of objects exists, one is usually only interest in the case where $A$ is finite. Furthermore, it is customary, as well as convenient, to take $A$ to be a set of the form $\{1,2,3,\ldots,n\}$ for some positive integer $n$. Unlike in calculus, where most functions are defined on infinite sets and are given by formulas, in algebra, permutations of finite sets are usually given by explicit listing of each element of the domain and its corresponding functional value. In practice, the sets that are permuted are fairly small, so listing the elements and the values they are assigned is reasonable. For example, we define a permutation $\alpha$ of the set $\{1,2,3,4\}$ by specifying 
$$
1 \alpha = 2, \quad 2 \alpha = 3, \quad 3 \alpha=1, \quad 4 \alpha=1 
$$
A more convenient way to express the correspondence is to write $\alpha$ in array form as 
$$
\alpha = \begin{bmatrix} 1 & 2 & 3 & 4 \\ 2 & 3& 1&4 \end{bmatrix}
$$
Here $j \alpha$ is placed directly below $j$ for each $j$. Similarly, the permutations $\beta$ of the set $\{1,2,3,4,5,6\}$ is given by 
$$
1 \beta = 5, \quad 2 \beta = 3,\quad 3 \beta = 1,\quad 4 \beta = 6,\quad 5 \beta = 2, \quad 6 \beta = 4
$$
is expressed in array form as 
$$
\beta = \begin{bmatrix} 1&2&3&4&5&6 \\ 5&3&1&6&2&4 \end{bmatrix}
$$
Composition of permutations expressed in array notation is carried out from left to right by going from top to bottom, then top to bottom. For example, let 
$$
\sigma = \begin{bmatrix}1&2&3&4&5 \\ 2&4&3&5&1 \end{bmatrix}
$$
and 
$$
\gamma = \begin{bmatrix} 1&2&3&4&5 \\ 5&4&1&2&3 \end{bmatrix}
$$
then 
$$
\sigma \gamma = \begin{bmatrix} 1&2&3&4&5 \\ 2&4&3&5&1 \end{bmatrix}\begin{bmatrix} 1&2&3&4&5 \\ 5&4&1&2&3 \end{bmatrix} 
$$
$$
= \begin{bmatrix} 1&2&3&4&5\\4&2&1&3&5 \end{bmatrix}
$$
On the right, for example, we have $4$ under $1$. This is because $1(\sigma \gamma)=(1 \sigma \gamma) = 2 \gamma = 4$, so $\sigma \gamma$ sends $1$ to $4$. The remainder of the bottom row of $\sigma \gamma$ is obtained in a similar fashion. 

**Example:**   Say we have an $S_{n}$ symmetric group. The set of all permutations will have the form 
$$
\alpha = \begin{bmatrix}1&2 & \ldots & n \\ 1 \alpha & 2 \alpha & \ldots & n \alpha \end{bmatrix}$$
It is easy to compute the order of $S_{n}$. There are $n$ choices for $1 \alpha$, there are $n-1$ possibilities are $2 \alpha$ (since $\alpha$ is 1:1). And so on. We see that $S_{n}$ must have $n(n-1)\ldots3\cdot 2\cdot 1 = n!$ elements. 

##### Cycle Notation
There is another notation commonly used to specify permutations. it is called cycle notation and was first used by Cauchy. As an illustration of cycle notation, let us consider the permutation 
$$
\alpha = \begin{bmatrix}1&2&3&4&5&6\\2&1&4&6&5&3 \end{bmatrix}
$$
this assignment of values could be presented schematically as follows:

![[Pasted image 20230913103817.png|center]]

Although mathematically satisfactory, such diagrams are cumbersome. Instead, we leave out the arrows and simply write $\alpha = (1,2)(3,4,6)(5)$. As a second example, consider 
$$
\beta = \begin{bmatrix}1&2&3&4&5&6\\5&3&1&6&2&4 \end{bmatrix}
$$
In cycle notation $\beta$ can be written $(2,3,1,5)(6,4)$ or $(4,6)(3,1,5,2)$, since both of these unambiguously specify the function $\beta$. An expression of the form $(a_{1},a_{2},\ldots,a_{m})$ is called a _cycle of length_ $m$ or an $m$-cycle. 

A multiplication of cycles can be introduced by thinking of a cycle as a permutation that fixes any symbol not appearing in the cycle. In this way, we can multiply cycles by thinking of them as permutations given in an array form. Typically, we like to express a permutation in a _disjoint cycle_; that is, the various cycles have no member in common. 

##### Properties of Permutations
We are now ready to state a number of theorems about permutations and cycles. All proofs are presented in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

**Theorem 5.1**  Every permutation can be written as a cycle or a product of disjoint cycles.

**Theorem 5.2**  If the pair of cycles $\alpha=(a_{1},a_{2},\ldots,a_{m})$ and $\beta = (b_{1},b_{2},\ldots,b_{n})$ have no entries in common, then $\alpha \beta = \beta \alpha$. 

**Corollary.**  (Ruffini-1799) The order of a permutation written in disjoint cycle form is the least common multiple of the lengths of the cycles. 

**Theorem 5.3**  Every permutation in $S_{n}, n>1$, is a product of $2$-cycles.

**Lemma.**  If $\epsilon=\beta_{1} \beta_{2}\ldots \beta_{r}$, where the $\beta$'s are $2$-cycles, then $r$ is even.

**Theorem 5.4**  If a permutation $\alpha$ can be expressed as a product of an even number of $2$-cycles, then every decomposition of $\alpha$ into a product of $2$-cycles must have an even number of $2$-cycles. In symbols, if 
$$
\alpha = \beta_{1} \beta_{2} \ldots \beta_{r} \quad \text{and} \quad \alpha=\gamma_{1} \gamma_{2} \ldots \gamma_{s}
$$
where the $\beta$'s and the $\gamma$'s are $2$-cycles, then $r$ and $s$ are both even or both odd. 

###### Even and Odd Permutations 
```ad-Definition
A permutation that can be expressed as a product of an even number of $2$-cycles is called an _even_ permutation. A permutation that can be expressed as a product of an odd number of $2$-cycles is called an _odd_ permutation. 
```

**Theorem 5.5**  The set of even permutations in $S_{n}$ forms a subgroup of $S_{n}$

**Remark.**  The group of even permutations of $n$ symbols is denoted by $A_{n}$ and is called the _alternating group of degree_ $n$. 