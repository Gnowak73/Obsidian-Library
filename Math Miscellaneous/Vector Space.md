---
tags: Math, Linear_Algebra, Vectors
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Vector Spaces_
Applications: _Geometry, Functional Linear Algebra_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Dual Spaces]]_
_
_
A vector space is a linear space whose elements, called vectors, may be added together and scaled by numbers called "scalars". These vector spaces follow some specific conditions defined below:

##### Vector Space Conditions 
1. Commutativity: $u+v=v+u$
2. Associativity: $u+(v+w)=(u+v)+w$
3. Zero Element: $u+0=0+u=u$
4. Additive Inverse: $u+(-u)=(-u)+u=0$
5. Distributivity: $a(u+v)=au+av$
6. $(a+b)u=au+bu$
7. $a(bu)=(ab)u$
8. $(1)u=u$

### Subspace
Let $W$ be a nonempty subset of the vector space $V$. Then, $W$ is a subspace of $V$ provided that $W$ itself is a vector space with the operations of addition and multiplication by scalars as defined in $V$. 

In other words: 
1. If $u$ and $v$ are vectors in $W$, then $u+v$ is also in $W$
2. If $u$ is in $W$ and $c$ is a scalar, then $cu$ is also in $W$

### Solution Space
just like working with ODEs and PDEs( [[Superposition Linear ODE and PDE#Solution Space]]), if a linear system has a solution such that all solutions are some linear combination of specific vectors and an arbitrary constant, then those specific vectors (considering they are [[linear independence|linearly indepenedent]]) create a solution space. 


### Rank
Rank is the dimension of the vector space generated (or spanned) by the columns of a matrix $A$. For example, if we have the matrix 
$$
A = \begin{bmatrix}1&0&1\\-2&-3&1\\3&3&0\end{bmatrix}
$$
we can see that the first two columns are linearly independent, so the rank is at least 2, but since the third is a linear combination of the first two columns, then there are only two linearly independent vectors in $A$. Thus, the column vectors only span $R^{2}$, and so 2 is the Rank.  

```ad-Remember
A vector does not have a rank, it is an element of a vector space. 

A matrix represents a linear transformation between vector spaces. A linear transformation has a rank and that rank is the dimension of the image of the linear transformation. Since a vector is not a representation of a linear transformation, it makes no sense to ask "what is the rank of a vector".
```