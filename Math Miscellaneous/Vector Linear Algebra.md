---
tags: Math, Linear_Algebra
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Vector Linear Algebra_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]] _
Closely\_Related\_To: _None_
_
_
If we recall that the dot product of two vectors in $\mathbb{R}^N$, 
$$
\pmb{x} \cdot \pmb{y} = \sum\limits_{i=1}^{N}x_{i}y_{i} \ 
$$
we also remember the relationship will a well-defined angle $\theta$ between these two vectors:
$$
\cos \theta = \frac{\pmb{x \cdot y}}{|x||y|}
$$
In particular, given two vectors $\pmb{x}$ and $\pmb{y}$, the vector projection of $\pmb{x}$ onto $\pmb{y}$ is 
$$
Proj_{\pmb{y}}\pmb{x} \equiv |x| \cos \theta \frac{y}{|y|} = \frac{\pmb{x \cdot y}}{|y|} \frac{y}{|y|} = (\pmb{x \cdot \hat y} )\pmb{\hat y}
$$
###### Basis
A set $\{x_{i}\}_{i=1}^N$ of $N$ vectors in $\mathbb{R}$ is called a <mark style="background: #ABF7F7A6;">basis</mark> if the following hold:
1. It is [[linear independence]]; i.e. if for some choice of real numbers $c_1,c_{2,}...,c_N$ we have
$$
c_{1}\pmb{x_{1}}+ \ldots+c_N\pmb{x}_{N}= \pmb{0}, \quad \text{then} \quad c_1=c_2=\ldots=c_N=0
$$

2. It spans all of $\mathbb{R}^N$, i.e. for every $\pmb{x} \in \mathbb{R}^N$ there exist real numbers $c_1,c_2,\ldots,c_N$ such that
$$
\pmb{x} = \sum\limits_{i=1}^{N}c_{i}x_{i}
$$

A basis $\{x_{i}\}_{i=1}^{N}$ is called an <mark style="background: #FFB8EBA6;">orthogonal basis</mark> if for each $i \neq j$ we have $\pmb{x}_{i}\ \cdot \pmb{x}_j=0$. We call it an <mark style="background: #FFF3A3A6;">orthonormal basis</mark> if, additionally, $|\pmb{x_i}|=1$ for all $i$.

###### Linear Transformation
A linear transformation is a mathematical object that is represented by a matrix such that 
$$
T(\pmb{x}) = \pmb{A}\pmb{x} 
$$
This transformation must also follow the [[linear independence#Linear Function|conditions for a linear function]].  

We say that $\pmb{A}$ is <mark style="background: #ADCCFFA6;">symmetric</mark> if it is an $N \times N$ matrix such that $a_{ij}=a_{ji}$.


### Eigenvalue Problem
An eigenvalue problem is an equation representing a linear transformation but the vector being transformed is only scaled by a constant factor $\lambda$: 
$$
\pmb{A v} = \lambda\pmb{v}
$$
This equation can be manipulated to get these two equations to solve such a problem:
$$
\boxed{
\begin{gathered}
 (\pmb{A}-\lambda\mathbb{I})\pmb{v}=\pmb{0} \\
 |\pmb{A}-\lambda\mathbb{I}|=0 
\end{gathered}
}
$$

##### Spectral Theorem 

Let $\pmb{A}$ be a symmetric $N \times N$ matrix. Then all eigenvalues of $A$ are <mark style="background: #FFB86CA6;">real</mark> and there exists an <mark style="background: #FF5582A6;">orthogonal basis</mark> of $\mathbb{R}^N$ consisting of eigenvectors of $\pmb{A}$. 

Let it also be known that for a symmetric matrix ($M=M^{T}$), eigenvectors corresponding to distinct eigenvalues are orthogonal. Also keep in mind that any symmetric matrix is diagonalizable. The diagonalization of matrices can be seen in [[diagonalization of matrices pdf.pdf]]. 


### Basis Linear Algebra
If we have an orthogonal basis $\{\pmb{v}_{i}\}_{i=1}^{N}$ such that $\pmb{v}_{i}\cdot \pmb{v}_{j}=0$ for each $i\neq j$, then we should be able to write any vector $\pmb{x}$, as 
$$
\pmb{x} = \sum\limits_{i=1}^{N}c_{i}\pmb{v}_{i}
$$
such that  if we take the dot product on both sides with an arbitrary vector basis $\pmb{v}_j$:
$$
\begin{aligned}
\pmb{x} \cdot\pmb{v}_{j} &= \left(\sum\limits_{i=1}^{N}c_{i}\pmb{x}_{i}\right)\cdot \pmb{v}_{j} \\
 &= \sum\limits_{i=1}^{N}(c_i\pmb{v}_{i}\cdot\pmb{v}_{j}) \\
 &= c_{j}|v_{j}|^{2}

\end{aligned}
$$
Hence, 
$$
\boxed{c_{i}= \frac{\pmb{x}\cdot \pmb{v}_i}{|\pmb{v}_{i}|^{2}}}
$$

This same method can be used for finding the coefficients in which a non-orthogonal basis spans a space too! You just don't get to rid of the summation part. 

We can now take this formula and write $\pmb{x}$ in terms of vector projections:
$$
\pmb{x} = \sum\limits_{i=1}^{N}Proj_{\pmb{v}_{i}}\pmb{x} = \sum\limits_{i=1}^{N}\frac{\pmb{x} \cdot \pmb{v}_i}{|\pmb{v}_{i}|^{2}}\pmb{v}_{i}

$$
Once again, similar procedures can be seen for non-orthogonal basis. 

A way to prove completeness of a basis (or proving that the coefficients $c_{n}$ are uniquely determined, is that if
$$
\left<\pmb{x}, \pmb{v}_{j} \right> = 0
$$
for all $j$, then $\pmb{x}=0$. This holds if and only if each $c_{n}$ are uniquely determined and the basis is complete.  This follows since if we have two sets of coefficients that work, then 
$$
\mathbf{x} - \mathbf{x} = \mathbf{0} =\sum\limits c_{n} \mathbf{v}_{n} - \sum\limits d_{n}v_{n}
$$
which by definition of linear dependence must be true as there are coefficients $c_{n}$ and $-d_{n}$ (rewriting the subtraction as a sum) such that the sum is $\mathbf{0}$ but $c_{n}\neq d_{n} \neq 0$. Thus, we check linear independence, by seeing that $c_{n}$ is **only** $0$ if the vector $\mathbf{x}$ is the zero vector. 

Another way of thinking about this is if we define $e_{n} = c_{n}-d_{n}$, such that we have an overcomplete basis, then 
$$
\mathbf{x} - \mathbf{x} = 0 = \sum\limits e_{n} \mathbf{v}_{n}
$$
By the definition of linear independence, $e_{n} = 0$ must be the only solution. So $e_{n}=0$ if the sum is $\mathbf{0}$. Another way of stating that is using the inner product as before (basically just checking for linear independence) of $\mathbf{v}_{n}$ with the definition of the projection coefficients. 

**Remark.**  If a function or vector cannot be written in terms as a projection onto a basis as expressed before then we say the basis is incomplete. If we can, though, then we say the basis is complete if and only if each $c_{n}$ is uniquely defined. If there exists more than one possible set of $c_{n}$, then the basis is overcomplete.








