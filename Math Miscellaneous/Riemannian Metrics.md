---
tags: riemannian, Math, metric, tensor, calculus, vector, covector, tensor
dg-publish: true
mathLink: 
---
Subject: _Differential Geometry, Tensor Calculus_
Main\_Topic: _Riemannian Metrics_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _[[Vectors, 1-Forms]],[[Tensor Examples]]_
Cont.\_ of: _None_ 
_
_

One _can_ identify vectors and covectors by introducing an _additional_ structure , but the identification will depend on the structure chosen. The metric structure of ordinary Euclidean Space $\mathbb{R}^{3}$ is based on the fact that we can measure angles and lengths of vectors and scalar products $\left<, \right>$. The arc length of a curve $C$ is
$$
\int\limits_C ds
$$
where $ds^{2}=dx^{2}+dy^{2}+dz^{2}$ in _cartesian_ coordinates. In curvilinear coordinates $u$, we have, putting $dx^{k}=\left(\frac{\partial x^{k}}{\partial u^{i}}\right)du^{i}$, and then 
$$
ds^{2} = \sum\limits _{k}(dx^{k})^{2}=\sum\limits_{i,j} g_{ij} du^{i}du^{j} = g_{ij} du^{i}du^{j}
$$
where 
$$
g_{ij} = \sum\limits_{k} \left(\frac{\partial x^{k}}{\partial u^{i}}\right)\left(\frac{\partial x^{k}}{\partial u^{j}}\right) = \left< \frac{\partial \pmb{p}}{\partial u^{i}}, \frac{\partial \pmb{p}}{\partial u^{j}}\right> \quad \text{since the $x$ coordinates are cartesian}
$$
**Remark.**  We can only write the inner product since we know that $x^{k}$ are cartesian coordinates and thus follow our formal Euclidean Space definition of the dot product. 

Now,
$$
g_{ij} = \left<\pmb{\partial}_{i}, \pmb{\partial}_{j} \right> = g_{ji}
$$
and generally, 
$$
\left<\pmb{v}, \pmb{w} \right> = g_{ij}v^{i}w^{j}
$$
**For Example:**  consider the plane $\mathbb{R}^{2}$ with cartesian coordinates $x^{1}=x, x^{2}=y$, and polar coordinates $u^{1}=r, u^{2}= \theta$. Then,
$$
\begin{bmatrix} g_{xx} = 1 & g_{xy} = 0  \\ g_{yx} = 0 & g_{yy} = 1 \end{bmatrix} \quad \text{i.e.} \quad g_{xy} = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
$$
Then, from $x=r\cos \theta$ and $y = r \sin \theta$, we have 
$$
\begin{bmatrix} g_{rr} = 1 & g_{r \theta} = 0  \\ g_{\theta r} = 0 & g_{\theta \theta} = r^{2} \end{bmatrix} \quad \text{i.e.} \quad g_{r \theta} = \begin{bmatrix} 1 & 0 \\ 0 & r^{2} \end{bmatrix}
$$
which is evident from the figure 

![[Screenshot 2023-08-10 202825.png|center]]

We can see similar results for spherical or cylindrical coordinates. 

Let us look back at our expression for $ds^{2}$. If $\alpha$ and $\beta$ are 1-forms ([[Vectors, 1-Forms]]), i.e., linear functionals, _define_ their **Tensor Product** $\alpha \otimes \beta$ to be the function of (ordered) **pairs** of vectors defined by 
$$
\boxed{\alpha \otimes \beta (\pmb{v}, \pmb{w}) \equiv \alpha(\pmb{v}) \beta(\pmb{w})}
$$
In particular 
$$
\boxed{(du^{i} \otimes du^{k})(\pmb{v},\pmb{w}) \equiv v^{i}w^{k}}
$$
Likewise $(\pmb{\partial}_{i} \otimes \pmb{\partial}_{j})(\alpha, \beta) = a_{i}b_{j}$ (such a proof of this can be seen at the end of [[Vectors, 1-Forms]]).

$\alpha \otimes \beta$ is a _bilinear_ function of $\pmb{v}$ and $\pmb{w}$, i.e., it is linear in each argument separately. A **second rank covariant tensor** is just such a bilinear function and in the coordinate system $u$ it can be expressed as
$$
\boxed{\sum\limits_{i,j} a_{ij} \ du^{i}\otimes du^{j}}
$$
where the coefficient matrix $(a_{ij})$ is written with indices down. Usually the tensor product sign $\otimes$ is omitted (in $du^{i} \otimes du^{j}$ but _not_ in $\alpha \otimes \beta$). For example, the metric 
$$
ds^{2} = g_{ij} \ du^{i}\otimes du^{j} = g_{ij} du^{i}du^{j}
$$
is a second rank covariant tensor that is **symmetric**, i.e., $g_{ij}=g_{ji}$. We may write 
$$
ds^{2}(\pmb{v},\pmb{w}) = \left<\pmb{v},\pmb{w} \right>
$$
It is easy to see that under a change of coordinates $u'=u'(u)$, demanding that $ds^{2}$ be independent of coordinates, $g_{ab}'du'^{a}du'^{b}=g_{ij}du^{i}du^{j}$, yields the transformation rule that 
$$
g'_{ab} = \left(\frac{\partial u^{i}}{\partial u'^{a}}\right)g_{ij}\left(\frac{\partial u^{j}}{\partial u'^{b}}\right)
$$
for the components of a second rank _covariant_ tensor. 

**Remark.**  When we are dealing with something like $dx dy$, we are not actually multiplying $dx$ and $dy$, but taking the tensor product $dx \otimes dy$. This allows us to be consistent with previous mathematics while also solidifying that $dx$ and $dy$ are covectors! Also, we cannot actually cancel out derivatives, but the chain rule's notation just looks very suggestive and it happens to work, fortunately enough. But, remember that differentials are covectors, they cannot genuinely be multiplied or divided! 

**Remark.**  We have been using the Euclidean metric structure to construct $g_{ij}$ in any coordinate system, but there are times when other structures are more appropriate. For example, when considering some delicate astronomical questions, a metric from Einstein's general relativity yields more accurate results. When dealing with complex analytic functions in the upper half plane $y>0$, Poincare found that the planar metric $ds^{2} = \frac{dx^{2}+dy^{2}}{y^{2}}$ was very useful. In general, when some second rank covariant tensor ($g_{ij}$) us used in a metric $ds^{2}=g_{ij}du^{i}du^{j}$ (in which case it must be symmetric and positive definite), this metric is called a **Riemannian metric**, after Bernhard Riemann, who was the first to consider this generalization of *Gauss'* thoughts. 

Given a Riemannian metric, one can associate each (contravariant) vector $\pmb{v}$ to a covector $v$ by 
$$
\boxed{v(\pmb{w}) = \left<\pmb{v}, \pmb{w} \right>}
$$
for _all_ vectors $\pmb{w}$, i.e.,
$$
v_{j} w^{j} = v^{k}g_{kj}w^{j} \quad \text{and so} \quad v_{j} = v^{k}g_{kj} = g_{jk}v^{k}
$$
In _components_, it is traditional to use the same letter for the covector as for the vector 
$$
v_{j} = g_{jk}v^{k}
$$
**Remark.**  This operation is akin to projecting a vector onto a new basis, except that new basis is the dual vector basis. Thus, we are projecting a vector from our original vector basis to its dual basis, transforming a vector into a dual vector.

to prevent confusion since the covector has the subscript. We say that "we lower the contravariant index" by means of the covariant metric tensor $g_{jk}$. Similarly, since $g_{jk}$ is the matrix of positive definite quadratic forms $ds^{2}$, it has an inverse matrix, $g^{jk}$, which can be shown to be a _contravariant_ second rank symmetric tensor (a bilinear function of pairs of covectors given by $g^{jk}a_{j}b_{k}$). Then, for each covector $\alpha$ we can associate a vector $\pmb{a}$ by $a^{i}=g^{ij}a_{j}$, i.e., we _raise the covariant index_ by means of the contravariant metric tensor $g^{jk}$. 

The **gradient vector** of a function $f$ is defined to be the vector $\text{grad} \ f = \nabla f$ associated to the covector $df$, i.e., $df(\pmb{w})=\left<\nabla \pmb{f}, \pmb{w} \right>$ 
$$
(\nabla f)^{i} \equiv g^{ij} \frac{\partial f}{\partial u^{j}}
$$
Then the correct version of the equation of steepest ascent considered at the end of [[Superscripts, Subscripts, Summation Convention]], is 
$$
\frac{du^{i}}{dt} = (\nabla f)^ {i}= g^{ij} \frac{\partial f}{\partial u^{i}}
$$
in _any_ coordinates.



