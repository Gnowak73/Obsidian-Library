---
tags: Math, manifold, submanifold, vector, tensor, topology, SO(3), O(3)
dg-publish: true
mathLink: 
---
Subject: _Topology, Differential Geometry_
Main\_Topic: _Submanifolds_
Applications: _Applications to Differential Geometry and Tensor Calculus_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _[[Manifolds]]_
Cont.\_ of: _None_ 
_
_

Coordinate systems that are not defined everywhere are considered "local". Coordinates that are defined everywhere are considered "global". For example, latitude and longitude are local because they are not well defined at the poles of the Earth. Manifolds are the most general space we can use differential and integral calculus in, and can be covered by a family of local coordinate systems. But first we venture to submanifolds of $\mathbb{R}^{n}$, generalizing the notions of curves and surfaces in $\mathbb{R}^{3}$. 

#### Submanifolds of Euclidean Space
Euclidean space, $\mathbb{R}^{n}$, is endows with a global coordinate system $(x_{1},\ldots,x^{N})$ and is the most important example of a manifold. 

```ad-Definition
A subset $M=M^{n}\subset \mathbb{R}^{n+r}$ is said to be an n-dimensional **submanifold** of $\mathbb{R}^{n+r}$, if _locally_ $M$ can be described by giving $r$ of the coordinates differentiability in terms of the $n$ remaining ones. 
```

This means that given $p \in M$, a neighborhood of $p$ on $M$ can be described in _some_ coordinate system $(x,y)=(x^{1},\ldots,x^{n},y^{1},\ldots,y^{n})$ of $\mathbb{R}^{n+r}$ by $r$ differentiable functions. 
$$
y^{\alpha} = f^{\alpha}(x^{1},\ldots,x^{n}), \quad \alpha=1,\ldots,r
$$
We abbreviate this by $y=f(x)$, or even $y=y(x)$. We say that $x^{1},\ldots,x^{n}$ are **local (curvilinear) coordinates** for $M$ near $p$. 

**Example:**  $y^{1}=f(x^{1},\ldots,x^{n})$ describes an n-dimensional submanifold of $\mathbb{R}^{n+1}$

![[Screenshot 2023-08-14 151709.png|center]]

A subset $M=M^{n}\subset \mathbb{R}^{n+r}$ is said to be an n-dimensional **submanifold** of $\mathbb{R}^{n+r}$, if _locally_ $M$ can be described by giving $r$ of the coordinates differentiability in terms of the $n$ remaining ones. 

**Remark.**  A submanifold of dimension $(N-1)$ in $\mathbb{R}^{n}$, that is, of "codimension" 1, is called a **hypersurface**. 

#### Geometry of Jacobian Matrices: The "Differential"
The **tangent space** to $\mathbb{R}^{n}$ at the point $x$, written here as $\mathbb{R}^{n}_{x}$, is by definition the vector space of all vectors in $\mathbb{R}^{n}$ based at $x$ (i.e., it is a copy of $\mathbb{R}^{n}$ with origin shifted to $x$). Let $x^{1},\ldots,x^{n}$ and $y^{1},\ldots,y^{r}$ be coordinates for $\mathbb{R}^{n}$ and $\mathbb{R}^{r}$ respectively. Let $F: \mathbb{R}^{n} \rightarrow \mathbb{R}^{r}$ be a **smooth** map. ("Smooth" ordinarily means infinitely differentiable. For our purposes, however, it will mean differentiable at least as many times as is necessary in the present context). In coordinates, $F$ is described by $r$ differentiable functions of $n$ variables 
$$
y^{\alpha} = F^{\alpha}(x) \quad \alpha=1,\ldots,r
$$
or simply $y=F(x)$. We will frequently use the more dangerous notation $y=y(x)$. 

Let $y_{0}=F(x)$; the [[Jacobian|Jacobian Matrix]] $\left(\frac{\partial y^{\alpha}}{\partial x^{i}}\right)(x_{0})$ has the following significance. 

![[Screenshot 2023-08-14 153025.png|center]]

Let $\pmb{v}$ be a tangent vector to $\mathbb{R}^{n}$ at $x_{0}$. Take _any_ smooth curve $x(t)$ such that $x(0)=x_{0}$ and $\dot{x}(0)\equiv \left(\frac{dx}{dt}\right)(0)=\pmb{v}$, for example, the straight line $x(t)=x_{0}+t\pmb{v}$. The image of this curve 
$$
y(t)=F(x(t))
$$
has a tangent vector $\pmb{w}$ at $y_{0}$ given by the chain rule 
$$
w^{\alpha} = \dot{y^ {\alpha}}(0) = \sum\limits_{i}^{n}\left(\frac{\partial y^{\alpha}}{\partial x^{i}}\right)(x_{0})\dot{x^{i}}(0) = \sum\limits_{i}^{n}\left(\frac{\partial y^{\alpha}}{\partial x^{i}}\right)(x_{0})v^{i}
$$
The assignment $\pmb{v}\rightarrow \pmb{w}$ is, from the expression, independent of the curve $x(t)$ that is chosen and defines a [[Vector Linear Algebra#Linear Transformation|linear transformation]], the **differential** of $F$ at $x_{0}$,
$$
F_{*}: \mathbb{R}^{n}_{x_{0}} \rightarrow \mathbb{R}^{r}_{y_{0}} \quad F_{*}(\pmb{v}) = \pmb{w}
$$
whose matrix is simply the Jacobian matrix $\left(\frac{\partial y^{\alpha}}{\partial x^{i}}\right)(x_{0})$. This interpretation of the Jacobian matrix, as a linear transformation sending tangents to curves into tangents to the images curves under $F$, can sometimes be used to replace the direct computation of matrices. This philosophy will be expanded upon. 

#### The Main Theorem on Submanifolds
The main theorem is a geometric interpretation of what we have just discussed. Note that the statement "$F$ has rank $r$ at $x_{0}$", that is, $\left[\frac{\partial y^{\alpha}}{\partial x^{i}}\right](x_{0})$ has rank $r$, is geometrically the statement that the differential 
$$
F_{*}:\mathbb{R}^{n}_{x_{0}}\rightarrow \mathbb{R}^{r}_{y_{0}=F(x_{0})}
$$
is **onto** or "surjective"; that is, given any vector $\pmb{w}$ at $y_{0}$, there is at least one vector $\pmb{v}$ at $x_{0}$ such that $F_{*}(\pmb{v})=\pmb{w}$. We then have

---
**Theorem.**  Let $F:\mathbb{R}^{n+r} \rightarrow \mathbb{R}^{r}$ and suppose that the locus
$$
F^{-1}(y_{0}) \equiv \{ x \in \mathbb{R}^{r+n} | \  F(x) = y_{0} \}
$$
is _not_ empty. Suppose further that for all $x_{0} \in F^{-1}(y_{0})$
$$
F_{*}: \mathbb{R}^{n+r}_{x_{0}} \rightarrow \mathbb{R}^{r}_{y_{0}}
$$
is onto. Then $F^{-1}(y_{0})$ is an n-dimensional submanifold of $\mathbb{R}^{n+r}$

![[Screenshot 2023-08-14 172027.png|center]]

---
The best example to keep in mind is the linear "projection" $F: \mathbb{R}^{3} \rightarrow \mathbb{R}^{2}, F(x^{1},x^{2},x^{3})=(x^{1},x^{2}),$ that is, $y^{1}=x^{1}$ and $y^{2}=x^{2}$. In this case, $x^{3}$ serves as a global coordinate for the submanifold $x^{1}=y_{0}^{1},x^{2}=y_{0}^{2}$, that is, the vertical line.  

#### A Nontrivial Example: The Configuration Space of a Rigid Body 
Assume a rigid body has one point, the origin of $\mathbb{R}^{3}$, fixed. By comparing a cartesian right-handed system fixed in the body with that of $\mathbb{R}^{3}$ we see that the configuration of the body at any time is described by the rotation matrix taking us from the basis of $\mathbb{R}^{3}$ to the basis fixed in the body. The configuration space of the body is then the **rotation group** SO(3), that is, the $3 \times 3$ real matrices $x=(x_{ij})$ such that 
$$
x^{T}=x^{-1} \quad \text{and} \quad \det x=1
$$
**Remark.**  This is the definition of an orthonormal matrix. So we have orthogonal vectors (corresponding to a right hand coordinate system), which are normal (have length 1). If we omit the determinant condition, the group is the full **orthogonal** group O(3). More can be seen in [[Orthogonal Matrices and O(3) group]]. 

```ad-Definition
The SO(3) group is the rotation group describing all possible rotations about the origin of the $\mathbb{R}^{3}$ Euclidean space.
```

By assigning (in some fixed order) the nine coordinates $x_{11},x_{12},\ldots,x_{33}$ to _any_ matrix $x$, we see that the space of all $3 \times 3$ real matrices, $M(3\times 3)$, is the Euclidean space $\mathbb{R}^{9}$. The group O(3) is then the locus in this $\mathbb{R}^{9}$ defined by the equations $x^{T}x=I$, that is, by the system of nine quadratic equations $(i,k)$
$$
(i,k) \quad \sum\limits_{j=1}^{3}x_{ji}x_{jk} = \delta_{ik}
$$
We then have the following situation. The configuration of the body at time $t$ can be represented by a point $x(t)$ in $\mathbb{R}^{9}$, but in fact the point $x(t)$ lies on the locus O(3) in $\mathbb{R}^{9}$. We shall see shortly that _this_ locus is in fact a 3-dimensional submanifold of $\mathbb{R}^{9}$. 

As time $t$ evolves, the point $x(t)$ traces out a curve on this 3-dimensional locus. Since O(3) is a submanifold, we shall see, from the principle of least action, that this path is a very special one, a "geodesic" on the submanifold O(3), and this in turn will yield important information on the existence of periodic motions of the body even when the body is subject to an unusual potential field. All this depends on the fact that O(3) is a submanifold, and we turn now to the proof of this crucial result. 

**Proof:**  Note first that since $x^{T}x$ is a symmetric matrix, equation $(i,k)$ is the same as equation $(k,i)$; there are, then, only 6 independent equations. This suggests the following. Let 
$$
Sym^{6}\equiv \{x \in M(3\times3)| \ x^{T}=x\}
$$
be the space of all _symmetric_ $3\times3$ matrices. Since this is defined by the three _linear_ equations
$x_{ik}-x_{ki}=0, i\neq k$, we see that $Sym^{6}$ is a 6-dimensional linear subspace of $\mathbb{R}^{9}$; that is, it can be considered as a copy of $\mathbb{R}^{6}$. To exhibit O(3) as a locus in $\mathbb{R}^{9}$, we consider the map
$$
F:\mathbb{R}^{9}\rightarrow \mathbb{R}^{6}=Sym^{6} \quad \text{defined by} \quad F(x)=x^{T}x-I
$$
O(3) is then the locus $F^{-1}(0)$. Let $x_{0} \in F^{-1}(0)=\text{O(3)}$. We shall now show that $F_{*}:\mathbb{R}^{9}_{x_{0}} \rightarrow Sym^{6}$ is onto.

![[Screenshot 2023-08-14 200341.png|center]]

Let $\pmb{w}$ be tangent to $Sym^{6}$ at the zero matrix. As usual, we identify a vector at the origin of $\mathbb{R}^{n}$ with its endpoint. Then $\pmb{w}$ is itself a symmetric matrix. We must find $\pmb{v}$, a tangent vector to $\mathbb{R}^{9}$ at $x_{0}$, such that $F_{*}\pmb{v}=\pmb{w}$. Consider a general curve $x=x(t)$ of matrices such that $x(0)=x_{0}$; its tangent vector at $x_{0}$ is $\dot{x}(0)$. The image curve 
$$
F(x(t)) = x(t)^{T}x(t)-I
$$
has tangent at $t=0$ given by 
$$
\frac{d}{dt}[F(x(t))]_{t=0} = \dot{x}(0)^{T}x_{0}+x_{0}^{T}\dot{x}(0)
$$
We wish this quantity to be $\pmb{w}$. We can see and verify that it is sufficient to satisfy the matrix equation $x_{0}^{T}\dot{x}(0)=\pmb{w}/2$, since both terms in the expression above are equal. Since $x_{0}\in \text{O(3)}, x_{0}^{T}=x_{0}^{-1}$ and we have as solution the matrix product $\pmb{v}=\dot{x}(0)=x_{0} \frac{\pmb{w}}{2}$. Thus $F_{*}$ is onto at $x_{0}$ and by our main theorem $\text{O(3)}=F^{-1}(0)$ is a $(9-6)=$ 3-dimensional submanifold of $\mathbb{R}^{9}$. 

---
**Remark.**  What about the subset SO(3) of O(3)? Recall that each orthogonal matrix has determinant $\pm 1$, whereas SO(3) consists of those orthogonal matrices with determinant $+1$. The mapping 
$$
\mathbb{R}^{9} \rightarrow \mathbb{R}
$$
that sends each matrix $x$ into its determinant is continuous (it is a cubic polynomial function of the coordinates $x_{ik}$) and consequently the two subsets of O(3) where the determinant is $+1$ or $-1$ must be separated. This means that SO(3) itself must have the property that it is locally described by giving $6$ of the coordinates in terms of the remaining $3$, that is, SO(3) is a 3-dimensional submanifold of $\mathbb{R}^{9}$. 

---
Thus, the configuration space of a rigid body with one point fixed is the group SO(3). This is a 3-dimension submanifold of $\mathbb{R}^{9}$. Each point of this configuration space lies in some local curvilinear coordinate system. 

In physics books the coordinates in an n-dimensional configuration space are usually labeled $q^{1},\ldots,q^{n}$. For SO(3) physicists usually use the three "Euler angles" as coordinates. These coordinates do not cover all of SO(3) in the sense that they become singular at certain points, just as polar coordinates in the plane are singular at the origin.