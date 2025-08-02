---
tags: superscripts, notation, Math, convention, einstein_notation, contraction, tensor, tensor_calculus
dg-publish: true
mathLink: 
---
Subject: _Tensor Calculus_
Main\_Topic: _Superscripts, Subscripts, Summation Convention_
Applications: _Summation Notation for Tensor Calculus, differential geometry, etc._
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

###### Summation Convention
Whenever we have a single term of an expression with any number of indices up and down, e.g., $T^{abc}_{de}$ if we rename one of the _lower_ indices, say $d$, so that it becomes the same as one of the _upper_ indices, say $b$, and if we then sum over this index, the result, call it $S$, is 
$$
\sum\limits_{b}T^{abc}_{be} = S^{ac}_{e}
$$
is called a **contraction** of $T$. The index $b$ has disappeared (it was a summation or "dummy" index on the left expression; you could have called it anything). This process of summing over a repeated index _that occurs as both a subscript and a superscript_ occurs so often that we shall omit the summation sign and merely write, for example, $T^{abc}_{de}=S^{ac}_{e}$. This "Einstein Convention" does _not_ apply to two upper or two lower indices. Here is why.

We have seen that if $\alpha$ is a covector, and if $\pmb{v}$ is a vector, then $\alpha(\pmb{v})=a_{i}v^{i}$ is invariant. But if we have another vector, say $\pmb{w}=\pmb{\partial}w$ then $\sum\limits_{i}v^{i}w^{i}$ will not be invariant since 
$$
\sum\limits_{i}v'^{i}w'^{i} = v'^{T}w' = \left[\left(\frac{\partial u'}{\partial u}\right)v\right]^{T}\left(\frac{\partial u'}{\partial u}\right)w = v^{T} \left(\frac{\partial u'}{\partial u}\right)^{T}\left(\frac{\partial u'}{\partial u}\right)w
$$
will not be equal to $v^{T}w$, for all $\pmb{w},\pmb{v}$ unless $\left(\frac{\partial u'}{\partial u}\right)^{T}=\left(\frac{\partial u'}{\partial u}\right)^{-1}$, i.e., unless the coordinate change matrix is an _orthogonal matrix_, as it is when $u$ and $u'$ are cartesian. 

Our conventions regarding the _components_ of vectors and covectors:
	(contravariant $\rightarrow$ index up) and (covariant $\rightarrow$ index down) 

helps us avoid errors. For example, in calculus, the differential equations for curves of _steepest ascent_ for a function $f$ are written in cartesian coordinates as 
$$
\frac{dx^{i}}{dt} = \frac{\partial f}{\partial x^{i}}
$$
but these equations cannot be correct, say, in spherical coordinates, since we cannot equate the _contravariant_ components $v^{i}$ of the velocity vector with the _covariant_ components of the differential $df$; they transform in different ways under a (nonorthogonal) change of coordinates. We shall see the correct equations in [[Riemannian Metrics]]. 

**Remark.**  Our convention applies only to _components_ of vectors and covectors. In $\alpha=a_{i}dx^{i}$, $a_{i}$ is a component of a covector $a$, while each individual $dx^{i}$ is a basis covector, _not_ a component. The summation convention, however, always holds.