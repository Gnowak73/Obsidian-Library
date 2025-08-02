---
tags: Dual Spaces, linear_algebra, algebra, vector, spaces, dual, dual_space, Math contravariant, Space, 
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Dual Spaces_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Linear Algebra]],[[Vector Space]],[[Vectors, 1-Forms]]_
Cont.\_ of: _None_ 
_
_

Every vector space has a dual, which we call $V^{*}$, which represents a space of linear transformations $T:V \rightarrow \mathbb{F}$, such that 
$$
V^{*} = \mathcal{L}(V,\mathbb{F})
$$
where $\mathbb{F}$ is some field (see [[Integral Domains#Fields]]). Usually this field is the real or complex numbers. So we have a set of functions that map from our vector space to a field, that is the essence of the dual space. 

Elements of the dual space $V^*$ are themselves linear maps that assign real numbers (or numbers from the underlying field) to vectors in $V$. Mathematically, if $\alpha$ is an element of $V^*$, it maps a vector $v$ in $V$ to a scalar $\alpha(v)$.

The dual space $V^*$ is also a vector space in its own right, with operations of addition and scalar multiplication defined in the natural way for linear functionals. It has the same dimension as $V$, and there is a one-to-one correspondence between $V$ and $V^*$.


---
In other words, a set of linear scalar functions from $V \rightarrow \mathbb{F}$ is a vector space called the _dual_ of $V$. Integrals, the derivative, summations, etc. are all linear scalar functions. 

If $\dim V = n$, then $V \cong \mathbb{F}^{n}$. Since the dimension of a vector space and its dual are equal, we can associate a vector $x \in V$ with an n-tuple $x=(x_{1},x_{2},\ldots,x_{n})$ of scalars. For any fixed $(a_{1},a_{2},\ldots,a_{n}) \in \mathbb{F}$, the function 
$$
l:V \rightarrow \mathbb{F}^{*}, \quad l(x) = a_{1}x_{1}+a_{2}x_{2}+\ldots+a_{n}x_{n}
$$
is linear, i.e., $l \in V^{*}$. If  the dimension $n<\infty$, then every $l \in V^{*}$ can be written as above.


---
Two vector spaces $V,V^{*}$ are said to be dual if there exists a non-degenerate bilinear form $\left<-, -\right>:V^{*} \rightarrow \Gamma$. The bilinear form is called the _scalar product_, which is denoted as $\left<x^{*},x \right>$. 

Dual vectors represent information of background interacting objects. 

