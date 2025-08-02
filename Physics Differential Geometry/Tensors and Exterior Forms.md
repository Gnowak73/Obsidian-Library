---
tags: 
dg-publish: true
mathLink: 
---
Subject: _None_
Main\_Topic: _None_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

In [[Manifolds]] we considered the $n$-tuple of partial derivatives of a single function $\frac{\partial \mathbf{F}}{\partial x^{j}}$ and we noticed that this $n$-tuple does not transform in the same way as the $n$-tuple of components of a vector. These components $\frac{\partial \pmb{F}}{\partial x^{j}}$ transform as a new type of "vector." Now, to support this, we shall talk about the general notion of "tensor" that will include both notions of vector and a whole class of objects characterized by a transformation law generalizing (1.6) in [[Manifolds#Tangent Vectors and Mappings#Tangent or "Contravariant" Vectors]]. We shall, however, strive to define these objects and operations on them "intrinsically," that is, in a basis-free fashion. We shall also be very careful in our use of sub- and superscripts when we express components in terms of bases; _the notation is designed to help us recognize intrinsic quantities when they are presented in component form and to help prevent us from making blatant errors_. 

### Covectors and Riemannian Metrics
A question to note: how _do_ we find the curves of steepest ascent?

---
##### Linear Functionals and the Dual Space
Let $E$ be a real vector space. Although for some purposes $E$ may be infinite-dimensional, we are mainly concerned with the finite-dimensional case. Although $\mathbb{R}^{n}$, as the space of real $n$-tuples $(x^{1},\ldots,x^{n})$, comes equipped with a distinguishable basis $(1,0,0,0,\ldots,0)^{T},\ldots,$ the general $n$-dimensional vector space $E$ has no basis prescribed. 

Choose a basis ${\mathbf{e}}_{1},\ldots,{\mathbf{e}}_{n}$ for the $n$-dimensional space $E$. Then a vector ${\mathbf{v}} \in E$ has a unique expansion
$$
{\mathbf{v}} = \sum\limits_{j}{\mathbf{e}}_{j}v^{j} = \sum\limits_{j}v^{j} {\mathbf{e}}_{j}
$$
where the $n$ real numbers $v^{j}$ are the **components** of $\mathbf{v}$ with respect to the given basis. For algebraic purposes, _we prefer the first presentation_, where we have put the "scalars" $v^{j}$ to the right of the basis elements. We do this for several reasons, but mainly so that _we can use matrix notation_, as we shall see in the next paragraph. When dealing with calculus, however, this notation is awkward. For example, in $\mathbb{R}^{n}$ (thought of as a manifold, we can write the standard basis at the origin as ${\mathbf{e}}_{j} = \frac{\pmb{\partial}}{\pmb{\partial} x^{j}}$ (as before in [[Manifolds]]); then our favored presentation would say $\pmb{v} = \sum\limits_{j} \frac{\pmb{\partial}}{\pmb{\partial} x^{j}} v^{j}$, making it appear, incorrectly, that we are differentiating the components in this expression. Sometimes we will simply use the traditional $\sum\limits_{j}v^{j} \pmb{e}_{j}$. We shall use the matrices 
$$
\pmb{e} = (\pmb{e}_{1},\ldots,\pmb{e}_{n}) \quad \text{and} \quad v=(v^{1},\ldots,v^{n})^{T}
$$
The first is a symbolic _row_ matrix since each entry is a vector rather than a scalar. Note that in the matrix $v$ we are preserving the traditional notation of representing the components of a vector by a _column_ matrix. We can then write our preferred representation as a matrix product
$$
\pmb{v} = \pmb{e} v
$$
where $\pmb{v}$ is a $1 \times 1$ matrix. As usual, we see that the $n$-dimensional vector space $E$, with a choice of basis, is isomorphic to $\mathbb{R}^{n}$ under the correspondence $\pmb{v}\rightarrow (v^{1},\ldots,v^{n})\in \mathbb{R}^{n}$, but that this isomorphism is "unnatural," that is, dependent on the choice of basis. 

```ad-Definition
A (real) **linear functional** $\alpha$ on $R$ is a real-valued linear function $\alpha$, that is, a linear transformation $\alpha:E \rightarrow \mathbb{R}$ from $E$ to the 1-dimensional vector space $\mathbb{R}$. Thus 
$$
\alpha(a \pmb{v} + b\pmb{w}) = a \alpha(\pmb{v}) + b \alpha(\pmb{w})
$$
for real numbers $a,b$, and vectors $\pmb{v},\pmb{w}$.
```

By induction, we have, for any basis $\pmb{e}$
$$
\alpha\left(\sum\limits \pmb{e}_{j}v^{j}\right) = \sum\limits \alpha(\pmb{e}_{j})v^{j}
$$
This is simply of the form $\sum\limits a_{j}v^{j}$ (where $a_{j}\equiv \alpha(\pmb{e}_{j})$), and this is a linear function of the components of $\pmb{v}$. Clearly if $\{a_{j}\}$ are any real numbers, then $\pmb{v} \rightarrow \sum\limits a_{j}v^{j}$ defines a linear functional on all of $E$. Thus, _after_ one has picked a basis, the most general linear function on the finite-dimensional vector space $E$ is of the form
$$
\tag{2.3}
\alpha(\pmb{v}) = \sum\limits a_{j}v^{j} \quad \text{where} \quad a_{j}\equiv \alpha(\pmb{e}_{j})
$$
```ad-warning
A linear functional $\alpha$ on $E$ is not itself a member of $E$; that is, $\alpha$ is not to be thought of as a _vector_ in $E$. This is especially obvious in infinite-dimensional cases. For example, let $E$ be the vector space of all continuous real-valued functions $f:\mathbb{R} \rightarrow \mathbb{R}$ of a real variable $t$. The **Dirac functional** $\delta_{0}$ is the linear function on $E$ defined by 
$$
\delta_{0}(f) = f(0)
$$
You should convince yourself that $E$ is a vector space and that $\delta_{0}$ is a linear functiona on $E$. No one would confuse $\delta_{0}$, the Dirac $\delta$ "function," with a continuous function, that is, with an element of $E$. In fact $\delta_{0}$ is not a function on $\mathbb{R}$ at all. Where, then, do the linear functionals live?
```

```ad-Definition
The collection of all linear functionals $\alpha$ on a vector space $E$ form a new vector space $E^{*}$, the **dual space** to $E$, under the operations
$$
(\alpha+\beta)(\pmb{v}) \equiv \alpha(\pmb{v}) + \beta(\pmb{v}), \quad \alpha, \beta \in E^{*}, \quad \pmb{v} \in E
$$
$$
(c \alpha)(\pmb{v}) \equiv c \alpha(\pmb{v}), \quad c \in \mathbb{R}
$$
```

We shall see in a moment that if $E$ is $n$-dimensional, then so is $E^{*}$. If ${\pmb{e}}_{1},\ldots,\pmb{e}_{n}$ is a basis of $E$, we define the **dual basis** $\sigma^{1},\ldots,\sigma^{n}$ of $E^{*}$ by first putting 
$$
\sigma^{i}(\pmb{e}_{j}) = \delta^{i}_{j}
$$
and then "extending $\sigma$ by linearity," that is, 
$$
\sigma^{i}\left(\sum\limits_{j} \pmb{e}_{j}v^{j}\right) = \sum\limits_{j} \sigma^{i}(\pmb{e}_{j})v^{j} = \sum\limits_{j}\delta^{i}_{j}v^{j} = v^{i}
$$
Thus $\sigma^{i}$ is the linear functional that reads off the $i$th component (with respect to the basis $\pmb{e}$) of each vector $\pmb{v}$. 

Let us verify that the $\sigma$'s do form a basis. To show linear independence, assume that a linear combination $\sum\limits a_{j} \sigma^{j}$ is the $0$ functional. Then $0=\sum\limits_{j}a_{j}\sigma^{j}(\pmb{e}_{k}) =\sum\limits_{j}a_{j}\delta^{j}_{k} = a_{k}$ shows that all the coefficients $a_{k}$ vanish, as desired. To show that the $\sigma$'s span $E^{*}$, we note that if $\alpha \in E^{*}$ then 
$$
\alpha(\pmb{v}) = \alpha\left(\sum\limits \pmb{e}_{j}v^{j}\right) = \sum\limits \alpha(\pmb{e}_{j}) v^{j} = \sum\limits \alpha(\pmb{e}_{j}) \sigma^{j}(\pmb{v}) = \left(\sum\limits \alpha(\pmb{e}_{j})\sigma^{j}\right)(\pmb{v})
$$
Thus the two linear functionals $\alpha$ and $\sum\limits \alpha(\pmb{e}_{j}) \sigma^{j}$ must be the same!
$$
\tag{2.4}
\alpha = \sum\limits_{j} \alpha(\pmb{e}_{j})\sigma^{j}
$$
This very important equation shows that the $\sigma$'s do form a basis of $E^{*}$. In (2.3) we introduced the $n$-tuple $a_{j}=\alpha(\pmb{e}_{j})$ for each $\alpha\in E^{*}$. From (2.4) we see $\alpha = \sum\limits a_{j} \sigma^{j}$, where $a_{j}$ defined the $j$the **component** of $\alpha$. 

If we introduce the matrices 
$$
\sigma= (\sigma^{1},\ldots,\sigma^{n})^{T} \quad \text{and} \quad a=(a_{1},\ldots,a_{n})
$$
then we can write 
$$\tag{2.5}
\alpha= \sum\limits_{j}a_{j}\sigma^{j} = a \sigma
$$
Note that the components of a linear functional are written as a _row_ matrix $a$. If $\beta = (\beta_{iR})$ is a matrix of linear functions and if $\pmb{f}=(\pmb{f}_{Rs})$ is a matrix of vectors, then by $\beta \pmb{f} = \beta(\pmb{f})$ we shall mean the matrix of scalars
$$
\beta(\pmb{f})_{is} \equiv \sum\limits_{R} \beta_{iR}(\pmb{f}_{Rs})
$$
Note then that $\sigma \pmb{e}$ is the identity $n \times n$ matrix, and then equation $(2.3)$ says 
$$
\alpha(\pmb{v}) = (a \sigma )(\pmb{e} v) = a(\sigma \pmb{e})v = av
$$

---
##### The Differential of a Function
```ad-Definition
The dual space $M_{p}^{n*}$ to the tangent space $M_{p}^{n}$ at the point $p$ of a manifold is called the **cotangent space**. 
```

Recall from [[Manifolds]] that on a manifold $M^{n}$, a vector $\pmb{v}$ at $p$ is a differential operator on functions defined near $p$. 

```ad-Definition
Let $f: M^{n} \rightarrow \mathbb{R}$. The **differential** of $f$ at $p$, written $df$, is the linear functional $df: M_{p}^{n} \rightarrow \mathbb{R}$ defined by 
$$
df(\pmb{v}) = \pmb{v}_p(f)
$$
```
Note that we have defined $df$ _independent of any basis_. In local coordinates, $\pmb{e}_{j} = \frac{\pmb{\partial}}{\pmb{\partial} x^{j}} \vert_{p}$ defines a basis for $M_{p}^{n}$ and
$$
df\left(\sum\limits v^{j} \frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right) = \sum\limits v^{j}(p) \frac{\partial f}{\partial x^{j}}(p)
$$
is clearly a linear function of the components of $\pmb{v}$. In particular, we may consider the differential of a coordinate function, say $x^{i}$ 
$$
dx^{i}\left(\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right) = \frac{\partial x^{i}}{\partial x^{j}} = \delta^{i}_{j}
$$
and 
$$
dx^{i}\left(\sum\limits_{j} v^{j} \frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right) = \sum\limits_{j}v^{j}dx^{i}\left(\frac{\partial}{\partial x^{j}}\right) = v^{i}
$$
Thus, for each $i$, the linear functional $dx^{i}$ reads off the $i$th component of any vector $\pmb{v}$ (expressed in terms of the coordinate basis). In other words 
$$
\sigma^{i} = dx^{i}
$$
yields, for $i=1,\ldots,n$, the dual basis to the coordinate basis. $dx^{1},\ldots,dx^{n}$ form a basis for the cotangent space $M_{p}^{n*}$. The most general linear functional is then expressed in coordinates, from (2.5) as 
$$\tag{2.7}
\alpha = \sum\limits_{j} \alpha\left(\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right)dx^{j} = \sum\limits_{j} a_{j} dx^{j}
$$
```ad-warning
We shall call an expression such as (2.7) a **differential form**. In elementary calculus it is called simply a "differential." We shall not use this terminology since, as we learned in calculus, not every differential form is the differential of a functoin; that is, it need not be "exact." We shall discuss this later on in great detail.  
```

---
The definition of the differential of a function _reduced to the usual concept of differential as introduced in elementary calculus_. Consider for example $\mathbb{R}^{3}$ with its usual cartesian coordinates $x=x^{1}, y=x^{2},z=x^{3}$. The differential is _there_ traditionally defined in two steps. 

First, the differential of an "independent" variable, that is, a coordinate function, say $dx$, is a function of ordered pairs of points. If $P=(x,y,z)$ and $Q=(x',y',z')$ then $dx$ is defined to be $(x'-x)$. Note that this is the same as our expression $dx (Q-P)$, where $(Q-P)$ is now the _vector_ from $P$ to $Q$. The elementary definition in $\mathbb{R}^{3}$ takes advantage of the fact that a vector in the manifold $\mathbb{R}^{3}$ is determined by its endpoints, which again are in the manifold $\mathbb{R}^{3}$. This makes no sense in a general manifold; you cannot subtract _points_ on a manifold. 

Second, the differential $df$ of a "dependent" variable, that is, a function $f$, is defined to be the function on pairs of points given by 
$$
\left(\frac{\partial f}{\partial x}\right)dx + \left(\frac{\partial f}{\partial x}\right)dy + \left(\frac{\partial f}{\partial z}\right)dz
$$
Note that this is exactly what we would get from (2.7)
$$
df = \sum\limits df\left(\frac{\pmb{\partial}}{\pmb{\partial} x^{i}}\right)dx^{i} = \sum\limits \left(\frac{\partial f}{\partial x^{i}}\right) dx^{i}
$$
Our definition makes no distinction between independent and dependent variables, and makes sense in any manifold. 

Our coordinate expression for $df$ obtained previously holds in any manifold
$$\tag{2.8}
df = \sum\limits_{j} \left(\frac{\partial f}{\partial x^{j}}\right)dx^{j}
$$
---
A linear functional $\alpha:M_{p}^{n} \rightarrow \mathbb{R}$ is called a **covariant vector**, or **covector**, or **1-form**. A differentiable assignment of a covector to each point in an open set in $M^{n}$ is locally of the form 
$$
\alpha = \sum\limits_{j} a_{j}(x) dx^{j}
$$
and would be called a covector **field**, and so on; $df = \sum\limits_{j}(\frac{\partial f}{\partial x^{j}})dx^{j}$ is an example. Thus the numbers $\frac{\partial f}{\partial x^{1}},\ldots,\frac{\partial f}{\partial x^{n}}$ form the components _not_ of a vector field but rather of a covector field, the differential of $f$. We remarked in our warning before (in [[Manifolds]]) that these numbers are called the components of the "gradient vector" in elementary mathematics, but we shall _never_ say this. It is important to realize that the local expression (2.8) holds in _any_ coordinate system; for example, in spherical coordinates for $\mathbb{R}^{3}$, $f = f(r, \theta, \phi)$ and 
$$
df = \left(\frac{\partial f}{\partial r}\right)dr + \left(\frac{\partial f}{\partial \theta}\right)d \theta + \left(\frac{\partial f}{\partial \phi}\right)d \phi
$$
and no one would call $\frac{\partial f}{\partial r}, \frac{\partial f}{\partial \theta},\frac{\partial f}{\partial \phi}$ the components of the gradient vector in spherical coordinates! They are the components of the covector or $1$-form $df$. The gradient _vector_ $\text{grad} f$ will be defined later after an additional structure is introduced. Under a change of local coordinates the chain rule yields (really just using (2.8) with the tangent vector being applied as the input):
$$\tag{2.9}
dx_{V}^{i} = \sum\limits_{j}\left( \frac{\partial x_{V}^{i}}{\partial x_{U}^{j}}\right)dx_{U}^{j}
$$
and for a general covector $\sum\limits_{i} a^{V}_{i} dx_{V}^{i} = \sum\limits_{ij} a^{V}_{i}\left(\frac{\partial x_{V}^{i}}{\partial x_{U}^{j}}\right)dx_{U}^{j}$ must be the same as $\sum\limits_{j} a^{U}_{j}dx_{U}^{j}$. We then must have 
$$\tag{2.10}
a^{U}_{j} = \sum\limits_{i} a^{V}_{i} \left(\frac{\partial x_{V}^{i}}{\partial x_{U}^{j}}\right)
$$
But $\sum\limits_{j} \left(\frac{\partial x_{V}^{i}}{\partial x_{U}^{j}}\right) \left(\frac{\partial x_{U}^{j}}{\partial x_{V}^{k}}\right) = \frac{\partial x_{V}^{i}}{\partial x_{V}^{k}} = \delta^{i}_{k}$ shows that $\frac{\partial x_{U}}{\partial x_{V}}$ is the inverse matrix to $\frac{\partial x_{V}}{\partial x_{U}}$. Equation (2.10) is, in matrix form, $a^{U} = a^{V} \left(\frac{\partial x_{V}}{\partial x_{U}}\right)$, and this yield $a^{V} = a^{U}\left(\frac{\partial x_{U}}{\partial x_{V}}\right)$, or 
$$
a_{i}^{V} = \sum\limits_{j} a^{U}_{j} \left(\frac{\partial x^{j}_{U}}{\partial x_{V}^{i}}\right)
$$
This is the _transformation rule_ for the components of a covariant vector and should be compared with (1.6) in [[Manifolds#Tangent Vectors and Mappings]]. In the notation used in (1.7) we may write 
$$
a^{V} = a^{U}c_{UV} = a^{U}c^{-1}_{VU}
$$
```ad-warning
Equation (1.6) tells us how the componetns of a _single_ contravariant vector transform under a change in coordinates. Equation (2.11), likewise, tells us how the components of a _single_ 1-form $\alpha$ transform under a change of coordinates. THis should be compared with (2.9). This latter tells us how the $n$-coordinate 1-forms $dx_{V}^{1},\ldots,dx_{V}^{n}$ are related to the $n$-coordinate 1-forms $dx_{U}^{1},\ldots,dx_{U}^{n}$. In a sense we could say that the $n$-tuple of _covariant vectors_ $(dx^{1},\ldots,dx^{n})$ transforms as do the _componetns_ of a single _contravariant_ vector. We shall never use this terminology.
```

##### Scalar Products in Linear Algebra 
Let $E$ be an $n$-dimensional vector space with a given **inner** (or **scalar**) **product** $\left<, \right>$. Thus, for each pair of vectors $\pmb{v},\pmb{w}$ of $E$, $\left<\pmb{v},\pmb{w} \right>$ is a real number, it is linear in each entry when the other is held fixed (i.e., it is _bilinear_), and it is symmetric $\left<\pmb{v}, \pmb{w} \right> = \left<\pmb{w}, \pmb{v} \right>$. Furthermore $\left<, \right>$ is **nondegenerate** in the sense that if $\left<\pmb{v}, \pmb{w} \right> = 0$ for all $\pmb{w}$ then $\pmb{v}=\pmb{0}$; that is, the only vector "orthogonal" to every vector is the zero vector. If, further $|\pmb{v}|^{2} \equiv \left<\pmb{v}, \pmb{v} \right>$ is positive when $\pmb{v} \neq 0$ we say that the inner product is positive definite, but to accommodate relativity we shall _not_ always demand this. If $\pmb{e}$ is a basis of $E$, then we may write $\pmb{v} = \pmb{e}v$ and $\pmb{w} = \pmb{e}w$. Then 
$$
\left<\pmb{v}, \pmb{w} \right> = \left< \sum\limits_{i}\pmb{e}_{i}v^{i}, \sum\limits_{j} \pmb{e}_{j}w^{j} \right>
$$
$$
= \sum\limits_{i}v^{i} \left< \pmb{e}_{i}, \sum\limits_{j} \pmb{e}_{j} w^{j}\right> = \sum\limits_{i}\sum\limits_{j}v^{i} \left< \pmb{e}_{i},\pmb{e}_{j} \right> w^{j}
$$
If we define the matrix $G = (g_{ij})$ with entries 
$$
g_{ij} \equiv \left<\pmb{e}_{i}, \pmb{e}_{j} \right>
$$
then 
$$\tag{2.13}
\left<\pmb{v}, \pmb{w} \right> = \sum\limits_{ij}v^{i}g_{ij} w^{j}
$$
or 
$$
\left<\pmb{v},\pmb{w} \right> = vGw
$$
***Note:  this requires $v$ above to be the row matrix version of $v$, not the traditional column matrix***

The matrix $(g_{ij})$ is briefly called the **metric tensor**. This nomenclature will be explained later on. Note that when $\pmb{e}$ is an **orthonormal basis**, that is, when $g_{ij} = \delta^{i}_{j}$ is the identity matrix (and this can happen only if the inner product is positive definite), then $\left<\pmb{v},\pmb{w} \right> = \sum\limits_{j} v^{j}w^{j}$ takes the usual "Euclidean" form. If one restricted oneself to the use of orthonormal bases, one would never have to introduce the matrix $(g_{ij})$, and this is what is done in elementary linear algebra. 

By hypothesis, $\left<\pmb{v},\pmb{w} \right>$ is a linear function of $\pmb{w}$ when $\pmb{v}$ is held fixed. Thus if $\pmb{v} \in E$, the function $\nu$ defined by 
$$
\nu(\pmb{w}) = \left<\pmb{v},\pmb{w} \right>
$$
is a linear function, $\nu \in E^{*}$. Thus to each vector $\pmb{v}$ in the inner product space $E$ we may associate a covector $\nu$; we shall call $\nu$ the **covariant version** of the vector $\pmb{v}$. In terms of any basis $\pmb{e}$ of $E$ and the dual basis $\sigma$ of $E^{*}$ we have from (2.4) that 
$$
\nu = \sum\limits_{j}\nu_{j}\sigma^{j} = \sum\limits_{j} \nu(\pmb{e}_{j}) \sigma^{j}
$$
$$
 = \sum\limits_{j}\left<\pmb{v}, \pmb{e}_{j}\right> \sigma^{j} 
$$
$$
 = \sum\limits_{j} \left<\sum\limits_{i} \pmb{e}_{i}v^{i},\pmb{e}_{j} \right> \sigma^{j}
$$
$$
 = \sum\limits_{j}\left( \sum\limits_{i} v^{i}g_{ij}\right)\sigma^{j}
$$
Thus the covariant version of the vector $\pmb{v}$ has components $\nu_{j} = \sum\limits_{i}v^{i}g_{ij}$ and _it is tradition in "tensor analysis" to use the same letter $v$ rather than $\nu$_. Thus we write for the components of the covariant version 
$$\tag{2.15}
v_{j} = \sum\limits_{i}v^{i}g_{ij} = \sum\limits_{i}g_{ji}v^{i}
$$
since $g_{ij} = g_{ji}$. The _subscript_ $j$ in $v_{j}$ tells us that we are dealing with the covariant version; in tensor analysis one says that we have "lowered the upper index $i$, making it a $j$, by means of the metric tensor $g_{ij}$." We shall also call the $(v_{j})$, with abuse of language, **the covariant components of the contravariant vector $v$**. Note that if $\pmb{e}$ is an orthonormal basis then $v_{j} = v^{j}$. 

In our finite-dimensional inner product space $E$, every linear functional $\nu$ is the covariant version of some vector $\pmb{v}$. Given $\nu = \sum\limits_{j}v_{j} \sigma^{j}$ we shall find $\pmb{v}$ such that $\nu(\pmb{w}) = \left<\pmb{v},\pmb{w} \right>$ for all $\pmb{w}$. For this we need only solve (2.15) for $v^{i}$ in terms of the given $v_{j}$. Since $G = (g_{ij})$ is assumed nondegenerate, the inverse matrix $G^{-1}$ must exist and is again symmetric. We shall denote the entries of this inverse matrix by the same letters $g$ but written with superscripts 
$$
G^{-1} = (g^{ij})
$$
Then from (2.15) we have 
$$
v^{i} = \sum\limits_{j} g^{ij} v_{j}
$$
yields the contravariant version $\pmb{v}$ of the covector $\nu = \sum\limits_{j} v_{j}\sigma^{j}$. Again we call $(v^{i})$ the contravariant components of the covector $\nu$. 

Let us now compare the contravariant and covariant components of a vector $\pmb{v}$ in a simple case. First of all, we have immediately 
$$
v_{j} = \nu(\pmb{e}_{j}) = \left<\pmb{v},\pmb{e}_{j} \right>
$$
and then $v^{i} = \sum\limits_{j} g^{ij}v_{j} = \sum\limits_{j} g^{ij} \left<\pmb{v},\pmb{e}_{j} \right>$. Thus although we always have $\pmb{v} = \sum\limits_{i}v^{i}\pmb{e}_{i}$,
$$
\pmb{v} = \sum\limits_{i}\left(\sum\limits_{j}g^{ij} \left<\pmb{v},\pmb{e}_{j} \right>\right)\pmb{e}_{i}
$$
 replaces the Euclidean $\pmb{v}=\sum\limits_{i} \left<\pmb{v},\pmb{e}_{i} \right>\pmb{e}_{i}$ that holds when the basis is orthonormal. Consider, for instance, the plane $\mathbb{R}^{2}$, where we use a basis $\pmb{e}$ that consists of _unit_ but not orthogonal vectors. 
 
![[Pasted image 20231124162137.png|center]]

We must make some final remarks about linear functionals. It is important to realize that given an $n$-dimensional vector space $E$, whether or not it has an inner product, one can always construct the dual vector space $E^{*}$, and the construction has nothing to do with a basis in $E$. If a basis $\pmb{e}$ is picked for $E$, _then_ the dual basis $\sigma$ for $E^{*}$ is determined. There is then an _isomorphism_, that is, a 1:1 correspondence between $E^{*}$ and $E$ given by $\sum\limits a_{j}\sigma^{j} \rightarrow \sum\limits a_{j}\pmb{e}_{j}$, but this isomorphism is said to be "unnatural" since if we change the basis in $E$ the correspondence will change.  We shall _never_ use this correspondence. Suppose now that an inner product has been introduced into $E$. As we have seen, there is another correspondence $E^{*}\rightarrow E$ that is independent of basis; namely to $\nu \in E^{*}$ we associate the unique vector $\pmb{v}$ such that $\nu(\pmb{w})=\left< \pmb{v},\pmb{w} \right>$; we may write $\nu = \left< \pmb{v}, \cdot \right>$. In terms of a basis we are associating to $\nu = \sum\limits v_{i} \sigma^{i}$ the vector $\sum\limits v^{i}\pmb{e}_{j}$. Then we know that each $\sigma^{i}$ can be represented as $\sigma^{i} = \left<\pmb{f}_{i}, \cdot \right>$; that is, there is a unique vector $\pmb{f}_{i}$ such that $\sigma^{i}(\pmb{w}) = \left<\pmb{f}_{i},\pmb{w} \right>$ for all $\pmb{w} \in E$. Then $\pmb{f} = \{\pmb{f}_{i}\}$ is a new basis of the original vector space $E$, sometimes called the basis of $E$ dual to $\pmb{e}$, and we have $\left<\pmb{f}_{i}, \pmb{e}_{j} \right> = \delta^{i}_{j}$. Although this new basis _is_ used in applied mathematics, we shall _not do so_, for there is a very powerful calculus that has been developed for _covectors_, a calculus that cannot be applied to vectors!

##### Riemannian Manifolds and the Gradient Vector
A **Riemannian metric** on a manifold $M^{n}$ assigns, in a differentiable fashion, a positive definite inner product $\left<, \right>$ in each tangent space $M^{n}_{p}$. If $\left<, \right>$ is only nondegenerate (i.e., $\left<\pmb{u},\pmb{v} \right> = 0$ for all $\pmb{v}$ only if $\pmb{u}=0)$ rather than positive definite, then we shall call the resulting structure on $M^{n}$ a **pseudo-Riemannian** metric. A manifold with a (pseudo-) Riemannian metric is called a (pseudo-) **Riemannian Manifold**. 

In terms of a coordinate basis $\pmb{e}_{i} = \pmb{\partial}_{i} \equiv \frac{\pmb{\partial}}{\pmb{\partial} x^{i}}$ we have the differentiable matrices (the "metric tensor") 
$$
g_{ij}(x) = \left< \frac{\pmb{\partial}}{\pmb{\partial} x^{i}}, \frac{\pmb{\partial}}{\pmb{\partial} x^{j}} \right>
$$
as in (2.13). In an overlap $U \cap V$ we have 
$$
\tag{2.18}
g_{ij}^{V} = \left< \frac{\pmb{\partial}}{\pmb{\partial} x_{V}^{i}}, \frac{\pmb{\partial}}{\pmb{\partial} x_{V}^{j}} \right>
$$
$$
= \left< \sum\limits_{r} \left(\frac{\partial x_{U}^{r}}{\partial x_{V}^{i}}\right)\pmb{\partial}_{r}^{U}, \sum\limits_{s} \left(\frac{\partial x_{U}^{s}}{\partial x_{V}^{j}}\right)\pmb{\partial}_{s}^{U}\right>
$$
$$
g_{ij}^{V} = \sum\limits_{rs}\left(\frac{\partial x_{U}^{r}}{\partial x_{V}^{i}}\right)\left(\frac{\partial x_{U}^{s}}{\partial x_{V}^{j}}\right)g_{rs}^{U}
$$
This is the transformation rule for the components of the metric tensor. Remark that (due to chain rule) basis vectors transform like covectors and basis covectors transform like vectors. And our definitions for their transformation rules only talk about the **components**, not the basis vectors/covectors at play. 

```ad-Definition
If $M^{n}$ is a (pseudo-) Riemannian manifold and $f$ is a differentiable function, the **gradient vector**
$$
grad \ f = \nabla f
$$
is the _contravariant_ vector associated to the covector $df$
$$
df(\pmb{w}) = \left< \nabla f, \pmb{w} \right>
$$
In coordinates 
$$
(\nabla f)^{i} = \sum\limits_{j} g^{ij} \frac{\partial f}{\partial x^{j}}
$$
Note then that $|\nabla f|^{2} \equiv \left< \nabla f, \nabla f \right> = df(\nabla f) = \sum\limits_{ij} \left(\frac{\partial f}{\partial x^{i}}\right)g^{ij}\left(\frac{\partial f}{\partial x^{j}}\right)$. We see that $df$ and $\nabla f$ will have the same components if the metric is "euclidean", that is, if the coordinates are such that $g^{ij} = \delta^{i}_{j}$. 
```

**Example(special relativity):**  Minkowski Space is, as we shall see way later on, $\mathbb{R}^{4}$ but endowed with the pseudo-Riemannian metric given in the so-called inertial coordinates $t=x^{0},x=x^{1},y=x^{2},z=x^{3}$, by 
$$
g_{ij} = \left< \frac{\pmb{\partial}}{\pmb{\partial} x^{i}}, \frac{\pmb{\partial}}{\pmb{\partial} x^{j}} \right> = 1 \quad \text{if}\ i=j=1,2, \text{or} \ 3
$$
$$
= -c^{2} \quad \text{if} \ i=j=0 \quad \text{where $c$ is the speed of light}
$$
$$
=0 \quad \text{otherwise}
$$
that is, $(g_{ij})$ is the $4 \times 4$ diagonal matrix 
$$
(g_{ij}) = diag(-c^{2},1,1,1)
$$
Then
$$
df = \left(\frac{\partial f}{\partial t}\right)dt + \sum\limits_{j=1}^{3}\left(\frac{\partial f}{\partial x^{j}}\right)dx^{j}
$$
is classically written in terms of components 
$$
df \sim \left[\frac{\partial f}{\partial t},\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\right]
$$
but 
$$
\nabla f = \frac{-1}{c^{2}}\left(\frac{\partial f}{\partial t}\right)\pmb{\partial}_{t} + \sum\limits_{j=1}^{3}\left(\frac{\partial f}{\partial x^{j}}\right)\pmb{\partial}_{j}
$$
$$
\nabla f \sim \left[\frac{-1}{c^{2}} \frac{\partial f}{\partial t},\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\right]^{T}
$$
(It should be mentioned that the famous **Lorentz transformations** in general are simply _the_ changes of coordinates in $\mathbb{R}^{4}$ that leave the origin fixed and _preserve_ the form $-c^{2}t^{2}+x^{2}+y^{2}+z^{2}$, just as orthogonal transformations in $\mathbb{R}^{3}$ are those transformations that preserve $x^{2}+y^{2}+z^{2}$!)

##### Curves of Steepest Ascent 
The gradient vector in a Riemannian manifold $M^{n}$ has much the same meaning as in Euclidean space. If $\pmb{v}$ is a unit vector at $p \in M$, then the derivative of $f$ with respect to $\mathbf{v}$ is $\pmb{v}(f) = \sum\limits \left(\frac{\partial f}{\partial x^{j}}\right)v^{j} = df(\pmb{v}) = \left<\nabla f, \pmb{v} \right>$. Then Schwarz's inequality (which holds for a positive definite inner product), $|\pmb{v}(f)| = |\left<\nabla f, \pmb{v}\right>|\leq | \nabla f| |\pmb{v}| = |\nabla f|$, shows that $f$ has a maximum rate of change in the direction of $\nabla f$. If $f(p)=a$, then the **level set** of $f$ through $p$ is the subset defined by 
$$
M^{n-1}(a) \equiv\{x\in M^{n} \vert \ f(x) = a\}
$$
A good example to keep in mind is the torus from [[Manifolds#Mappings and Submanifolds of Manifolds]]. If $df$ does not vanish at $p$ then $M^{n-1}(a)$ is a submanifold in a neighborhood of $p$. If $x=x(t)$ is a curve in this level set through $p$ then its velocity there, $\frac{dx}{dt}$, is "annihilated" by $df$; $df(\frac{dx}{dt})=0$ since $f(x(t))$ is a constant. We are tempted to say that $df$ is "orthogonal" to the tangent space to $M^{n-1}(a)$ at $p$, but this makes no sense since $df$ is not a vector. Its _contravariant_ version $\nabla f$ is, however, orthogonal to this tangent space since $\left< \nabla f, \frac{dx}{dt} \right> = df(\frac{dx}{dt})=0$ for all tangents to $M^{n-1}(a)$ at $p$. We say that $\nabla f$ is orthogonal to the level sets. 

Finally recall that we showed before in [[Manifolds#Vector Fields and Flows]] that one does not get a well-defined flow by considering the local differential equations $\frac{dx^{i}}{dt}=\frac{\partial f}{\partial x^{i}}$; one simply cannot equation a contravariant vector $\frac{dx}{dt}$ with a covariant vector $df$. However, it makes good sense to write $\frac{dx}{dt}=\nabla f$; that is, the "correct" differential equations are 
$$
\frac{dx^{i}}{dt} = \sum\limits_{j}g^{ij} \left(\frac{\partial f}{\partial x^{j}}\right)
$$
The integral curves are then tangent to $\nabla f$, and so are orthogonal to the level sets $f=Const.$ How does $f$ change along one of these "curves of steepest ascent"? Well, $\frac{df}{dt} = df(\frac{dx}{dt})=\left<\nabla f, \nabla f \right>$. Note then that if we solve _instead_ the differential equations 
$$
\frac{dx}{dt} = \frac{\nabla f}{| \nabla f|^{2}}
$$
(i.e., we move along the same curves of steepest ascent but at different speed) then $\frac{df}{dt}=1$. The _resulting flow has then the property that in time $t$ it takes the level set $f=a$ into the level set $f=a+t$_. Of course this result need only be true locally and for small $t$ as mentioned before. Such a motion of level sets into level sets is called a **Morse deformation**. For more on such matters see $[M,$ chap. $1]$ in [[Geometry of Physics.pdf]]. 

---

### The Tangent Bundle 
What is the space of velocity vectors to the configuration space of a dynamical system?

##### The Tangent Bundle
The **tangent bundle**, $TM^{n}$ to a differentiable manifold $M^{n}$ is, by definition, the collection of all tangent vectors at all points of $M$. 

Thus a "point" in this new space consists of a pair $(p,\pmb{v})$ where $p$ is a point of $M$ and $\pmb{v}$ is a tangent vector to $M$ at the point $p$, that is, $\pmb{v} \in M_{p}^{n}$. Introduce local coordinates in $TM$ as follows. Let $(p,\pmb{v})\in TM^{n}$. $p$ lies in some local coordinate system $U,x^{1},\ldots,x^{n}$. At $p$ we have the coordinate basis $(\pmb{\partial}_{i} = \frac{\pmb{\partial}}{\pmb{\partial} x^{i}})$ for $M_{x}^{n}$. We may then write $\pmb{v} = \sum\limits_{i} v^{i} \pmb{\partial}_{i}$. Then $(p,\pmb{v})$ is completely described by the $2n$-tuple of real numbers 
$$
x^{1}(p),\ldots,x^{n}(p),v^{1},\ldots,v^{n}
$$
The $2n$-tuple $(x,v)$ represents the vector $\sum\limits_{j}v^{j} \pmb{\partial}_{j}$ at $p$. In this manner we associate $2n$ local coordinates to each tangent vector to $M^{n}$ that is based in the coordinate patch $(U,x)$. Note that the first $n$-coordinates, the $x$'s, take their values in a portion $U$ of $\mathbb{R}^{n}$, whereas the second set, the $v$'s, fill out an entire $\mathbb{R}^{n}$ since there are no restrictions on the components of a vector. This $2n$-dimensional coordinate patch is then of the form $(U \subset \mathbb{R}^{n})\times \mathbb{R}^{n} \subset \mathbb{R}^{2n}$. Suppose now that the point $p$ also lies in the coordinate patch $(U',x')$. Then the same point $(p,\pmb{v})$ would be described by the new $2n$-tuple
$$
x'^{1}(p),\ldots,x'^{n}(p),v'^{1},\ldots,v'^{n}
$$
where 
$$
x'^{i}=x'^{i}(x^{1},\ldots,x^{n})
$$
and 
$$
v'^{i}=\sum\limits_{j}\left[\frac{\partial x'^{i}}{\partial x^{j}}\right](p)v^{j}
$$
We see then that $TM^{n}$ is a $2n$-dimensional differentiable manifold!      

We have a mapping 
$$
\pi:TM \rightarrow M \quad \pi(p,\pmb{v})=p
$$
called **projection** that assigns to a vector tangent to $M$ the point in $M$ at which the vector sits. In local coordinates,
$$
\pi(x^{1},\ldots,x^{n},v^{1},\ldots,v^{n}) = (x^{1},\ldots,x^{n})
$$
It is clearly differentiable. 

![[Pasted image 20231125154638.png|center]]

We have drawn a schematic diagram of the tangent bundle $TM$. $\pi^{-1}(x)$ represents all vectors tangent to $M$ at $x$, and so $\pi^{-1}(x)=M_{x}^{n}$ is a copy of the vector space $\mathbb{R}^{n}$. It is called "the **fiber** over $x$." Our picture makes it seem that $TM$ is the product space $M \times \mathbb{R}^{n}$, but this is not so! Although we do have a global projection $\pi:TM \rightarrow M$, there is no projection map $\pi':TM \rightarrow \mathbb{R}^{n}$. 

A point in $TM$ represents a tangent vector to $M$ at a point $p$ but there is no way to read off the components of this vector until a coordinate system (or a basis for $M_{p}$) has been designated at the point at which the vector is based!

Locally of course we may choose such a projection; if the point is in $\pi^{-1}(U)$ then by using the coordinates in $U$ we may read off the components of the vector. Since $\pi^{-1}(U)$ is topologically $U \times \mathbb{R}^{n}$ we say that the tangent bundle $TM$ is **locally a product**. 

![[Pasted image 20231125161855.png|center]]

A vector field $\pmb{v}$ on $M$ clearly assigns to each point $x$ in $M$ a point $\pmb{v}(x)$ in $\pi^{-1}(x) \subset TM$ that "lies over $x$." Thus a vector field can be considered as a map $v:M \rightarrow TM$ such that $\pi \circ v$ is the identity map of $M$ into $M$. As such it is called a (**cross**) **section** of the tangent bundle. In a patch $\pi^{-1}(U)$ it is described by $v^{i}=v^{i}(x^{1},\ldots,x^{n})$ and the image $v(M)$ is then an $n$-dimensional submanifold of the $2n$-dimensional manifold $TM$. A special section, the $0$ section (corresponding to the identically $0$ vector field), always exists. Although different coordinate systems will yield perhaps different components for a given vector, they will all agree that the $0$-vector will have all components $0$. 

**Example:**  In mechanics, the configuration of a dynamical system with $n$ degrees of freedom is usually described as a point in an $n$-dimensional manifold, the **configuration space**. The coordinates $x$ are usually called $q^{1},\ldots,q^{n}$, the "generalized coordinates." For example, if we are considering the motion of two mass points on the real line, $M^{2}=\mathbb{R}\times \mathbb{R}$ with coordinates $q^{1},q^{2}$ (one for each particle). The configuration space need not be Euclidean space. For the planar double pendulum, the configuration space is $M^{2}=S^{1}\times S^{1} = T^{2}$. For the _spatial_ single pendulum $M^{2}$ is the $2$-sphere $S^{2}$ (with center at the pin). A tangent vector to the configuration space $M^{n}$ is though of, in mechanics, as a velocity vector; its components with respect to the coordinates $q$ are written $\dot{q_{1}},\ldots,\dot{q_{n}}$ rather than $v^{1},\ldots,v^{n}$. These are the **generalized velocities**. Thus $TM$ is the space of all generalized velocities, but there is no standard name for this space in mechanics (it is _not_ the phase space, to be considered shortly). 

##### The Unit Tangent Bundle
If $M^{n}$ is a Riemannian manifold then we may consider, in addition to $TM$, the space of all _unit_ tangent vectors to $M^{n}$. Thus in $TM$ we may restrict ourselves to the subset $T_{0}M$ of points $(x,\pmb{v})$ such that $|\pmb{v}|^{2}=1$. If we are in the coordinate patch $(x^{1},\ldots,x^{n},v^{1},\ldots,v^{n})$ of $TM$, then this **unit tangent bundle** is locally defined by 
$$
T_{0}M^{n}: \sum\limits_{ij}g_{ij}(x)v^{i}v^{j} = 1
$$
In other words, we are looking at the locus in $TM$ defined locally by putting the single function $f(x,v)=\sum\limits_{ij} g_{ij}(x)v^{i}v^{j}$ equal to a constant. The local coordinates in $TM$ are $(x,v)$. Note, using $g_{ij}=g_{ji}$, that 
$$
\frac{\partial f}{\partial v^{k}} = 2 \sum\limits_{j} g_{kj}(x)v^{j}
$$
(To find this relationship use product rule and expand) Since $\det(g_{ij})\neq 0$, we conclude that not all $\frac{\partial f}{\partial v^{k}}$ can vanish on the subset $v \neq 0$, and thus $T_{0}M^{n}$ is a $(2n-1)$-dimensional submanifold of $TM^{n}$! In particular $T_{0}M$ is itself a manifold. In the following figure, $\pmb{v}_{0}=\frac{\pmb{v}}{|\pmb{v}|}$. 

![[Pasted image 20231126140232.png|center]]

**Example:**  $T_{0}S^{2}$ is the space of unit vector tangent to the unit $2$-sphere in $\mathbb{R}^{3}$. 

![[Pasted image 20231126140431.png|center]]

Let $\pmb{v}=\pmb{f}_{2}$ be a unit tangent vector to the unit sphere $S^{2} \subset \mathbb{R}^{3}$. It is based at some point on $S^{2}$, described by a unit vector $\pmb{f}_{1}$. Using the right-hand rule we may put $\pmb{f}_{3} = \pmb{f}_{1}\times \pmb{f}_{2}$. 

It is clear that by this association, there is a 1:1 correspondence between unit tangent vector $\pmb{v}$ to $S^{2}$ (i.e., to a point in $T_{0}S^{2}$) and such orthonormal triples $\pmb{f}_{1},\pmb{f}_{2},\pmb{f}_{3}$. Translate these orthonormal vectors to the origin of $\mathbb{R}^{3}$ and compare them with a fixed right-handed orthonormal basis $\pmb{e}$ of $\mathbb{R}^{3}$. Then $\pmb{f}_{i}=\pmb{e}_{j}R^{j}_{i}$ for a unique rotation matrix $R \in SO(3)$. In this way we have set up a 1:1 correspondence $T_{0}S^{2} \rightarrow SO(3)$. It also seems evident that the topology of $T_{0}S^{2}$ is the same as that of $SO(3)$, meaning roughly that nearby unit vectors tangent to $S^{2}$ will correspond to nearby rotation matrices; precisely, we mean that $T_{0}S^{2} \rightarrow SO(3)$ is a diffeomorphism. 

_The unit tangent bundle $T_{0}S^{2}$ to the 2-sphere is topologically the 3-dimensional real projective 3-space $T_{0}S^{2} \sim \mathbb{R}P^{3} \sim SO(3)$._ 

---
#### The Cotangent Bundle and Phase Space 
The cotangent bundle to $M^{n}$ is by definition the space $T^{*}M^{n}$ of all _covectors_ at all points of $M$. A point in $T^{*}M$ is a pair $(x,\alpha)$ where $\alpha$ is a covector at the point $x$. If $x$ is in a coordinate patch $U,x^{1},\ldots,x^{n}$, then $dx^{1},\ldots,dx^{n}$, gives a basis for the cotangent space $M_{x}^{n*}$, and $\alpha$ can be expressed as $\alpha = \sum\limits a_{i}(x)dx^{i}$. Then $(x,\alpha)$ is completely described by the $2n$-tuple
$$
x^{1}(x),\ldots,x^{n}(x),a_{1}(x),\ldots,a_{n}(x)
$$
The $2n$-tuple $(x,a)$ represents the covector $\sum\limits a_{j} dx^{i}$ at the point $x$. If the point $p$ also lies in the coordinate patch $U',x'^{1},\ldots x'^{n}$, then
$$
x'^{i} = x'^{i}(x^{1},\ldots,x^{n})
$$
and 
$$
a_{i}' = \sum\limits_{j} \left[\frac{\partial x^{j}}{\partial x'^{i}}\right](x) a_{j}
$$
$T^{I}M^{n}$ is again a $2n$ dimensional manifold. We shall see shortly that the phase space in mechanics is the cotangent bundle to the configuration space. 

#### The Pull-Back of a Covector 
Recall that the differential $\phi_{*}$ of a smooth map $\phi:M^{n}\rightarrow V^{r}$ has as matrix the Jacobian matrix $\frac{\partial y}{\partial x}$ in terms of local coordinates $(x^{1},\ldots,x^{n})$ near $x$ and $(y^{1},\ldots,y^{r})$ near $y=\phi(x)$. Thus, in terms of the coordinate bases
$$
\phi_{*}\left(\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right) = \sum\limits_{R}\left(\frac{\partial y^{R}}{\partial x^{j}}\right)  \frac{\pmb{\partial}}{\pmb{\partial} y^{R}}
$$
Note that if we think of vectors as differential operators, then for a function $f$ near $y$
$$
\phi_{*}\left(\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right)(f) = \sum\limits_{R}\left(\frac{\partial y^{R}}{\partial x^{j}}\right)\left(\frac{\partial f}{\partial y^{R}}\right)
$$
simply says, "apply the chain rule to the composite function $f \circ \phi$, that is, $f(y(x))$. 

**Definition:**  Let $\phi:M^{n}\rightarrow V^{r}$ be a smooth map of manifolds and let $\phi(x)=y$. Let $\phi_{*}:M_{x}\rightarrow V_{y}$ be the differential of $\phi$. The **pull-back** $\phi^{*}$ is the linear transformation taking _covectors_ at $y$ into _covectors_ at $x$, $\phi^{*}:V(y)^{*}\rightarrow M(x)^{*}$, defined by 
$$
\phi^{*}(\beta)(\pmb{v}) \equiv \beta(\phi_{*}(\pmb{v}))
$$
for all covectors $\beta$ at $y$ and vectors $\pmb{v}$ at $x$. 

Let $x^{i}$ and $y^{R}$ be local coordinates near $x$ and $y$, respectively. The bases for the tangent vector spaces $M_{x}$ and $V_{y}$ are given by $\left(\frac{\pmb{\partial}}{\pmb{\partial}x^{j}}\right)$ and $\left(\frac{\pmb{\partial}}{\pmb{\partial}y^{R}}\right)$. Then 
$$
\phi^{*}\beta (\pmb{v}) = \beta(\phi_{*}(\pmb{v}))= \beta\left(\phi_{*}\left(\sum\limits_{j}v^{j}\frac{\pmb{\partial}}{\pmb{\partial x^{j}}}\right)\right) 
$$$$
 = \beta\left(\sum\limits_{j}v^{j} \phi_{*}\left(\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}\right)\right) = \beta\left(\sum\limits_{j}v^{j} \sum\limits_{R}\left(\frac{\partial y^{R}}{\partial x^{j}}\right)\left(\frac{\pmb{\partial}}{\pmb{\partial} y^{R}}\right)\right)
$$
$$
= \sum\limits_{jR} v^{j} \left(\frac{\partial y^{R}}{\partial x^{j}}\right) \beta\left(\frac{\pmb{\partial}}{\pmb{\partial} y^{R}}\right)  = \left(\sum\limits_{jR}  \left(\frac{\partial y^{R}}{\partial x^{j}}\right) \beta\left(\frac{\pmb{\partial}}{\pmb{\partial} y^{R}}\right) dx^{j}\right)(\pmb{v})
$$
$$
=\sum\limits_{jR} b_{R}\left(\frac{\partial y^{R}}{\partial x^{j}}\right)dx^{j}, \quad \text{where} \quad \beta = \sum\limits_{R}b_{R}dy^{R}
$$
Thus
$$\tag{2.24}
\phi^{*}(\beta) = \sum\limits_{jR}b_{R} \left(\frac{\partial y^{R}}{\partial x^{j}}\right)dx^{j}
$$
In terms of matrices, the _differential_ $\phi_{*}$ is given by the Jacobian matrix $\frac{\partial y}{\partial x}$ acting on _columns_ $v$ at $x$ from the left, whereas the _pull-back_ $\phi^{*}$ is given by the same matrix acting on _rows_ $b$ at $y$ from the _right_. (If we had insisted on writing covectors also as columns, then $\phi^{*}$ acting on such columns from the left would be given by the _transpose_ of the Jacobian matrix.)

$\phi^{*} (dy^{S})$ is given immediately from (2.24); since $dy^{S} = \sum\limits_{R}\delta^{S}_{R}dy^{R}$ 
$$
\tag{2.25}
\phi^{*}(dy^{S}) = \sum\limits_{j} \left(\frac{\partial y^{S}}{\partial x^{j}}\right) dx^{j}
$$
This is _again, simply the chain rule applied to the composition $y^{S} \circ \phi$_!

```ad-warning
Let $\phi:M^{n}\rightarrow V^{r}$ and let $\pmb{v}$ be a vector _field_ on $M$. It may very well be that there are two distinct points $x$ and $x'$ that get mapped by $\phi$ to the same point $y=\phi(x)=\phi(x')$. Usually we shall have $\phi_{*}(\pmb{v}(x)) \neq \phi_{*}(\pmb{v}(x'))$ since the field $\pmb{v}$ need have no relation to the map $\phi$. In other words, $\phi_{*}(\pmb{v})$ does not yield a well defined vector field on $V$ (does one pick $\phi_{*}(\pmb{v}(x))$ or $\phi_{*}(\pmb{v}(x'))$ at $y$?). $\phi_{*}$ _does not take vector fields into vector fields_. (There is an exception if $n=r$ and $\phi$ is 1:1) On the other hand, if $\beta$ is a _covector field_ on $V^{r}$, then $\phi^{*}\beta$ is always a well-defined covector field on $M^{n}$; $\phi^{*}(\beta(y))$ yields a definite covector at each point $x$ such that $\phi(x)=y)$. As we shall see, this fact makes covector fields easier to deal with than vector fields.
```

#### The Phase Space in Mechanics
Later we shall study Hamiltonian dynamics in a more systemic fashion. For now, we wish to draw attention to the basic aspects that seem mysterious when treated in most texts, largely because they draw no distinction there between vectors and covectors. 

Let $M^{n}$ be the configuration space of a dynamical system and let $q^{1},\ldots,q^{n}$ be local generalized coordinates. For simplicity, we shall restrict ourselves to time-independent Lagrangians. the Lagrangian $L$ is then a function of the generalized coordinates $q$ and the generalized velocities $\dot{q}$, $L=L(q,\dot{q})$. It is important to realize that $q$ and $\dot{q}$ are $2n$-independent coordinates. (Of course if we want we can consider a specific path $q=q(t)$ in configuration space then the Lagrangian along this evolution is computing by $\dot{q}=\frac{dq}{dt}$.) Thus the Lagrangian $L$ is to be considered as a function on the space of generalized velocities, that is, $L$ is a real-valued function on the tangent bundle to $M$. 
$$
L:TM^{n} \rightarrow \mathbb{R}
$$
We shall be concerned here with the transition from the Lagrangian to the Hamiltonian formulation of dynamics. Hamilton was led to define the functions 
$$ \tag{2.26}
p_{i}(q,\dot{q}) \equiv \frac{\partial L}{\partial \dot{q}^{i}}
$$
We shall only be interested in the case when $\det\left(\frac{\partial p_{i}}{\partial \dot{q}^{j}}\right)\neq 0$. In many books, this formula above is looked upon merely looked upon as a change of coordinates in $TM$; that is, one switches from coordinates $q,\dot{q}$ to $q,p$. Although this is technically acceptable, it has the disadvantage that the $p$'s do not have the direct geometrical significance that the coordinates $\dot{q}$ has. Under a change in coordinates, say from $q_{U}$ to $q_{V}$ in configuration space, there is an associated change in coordinates in $TM$
$$
q_{V} = q_{V}(q_{U}) 
$$$$\tag{2.27}
\dot{q}_{U}^{j} = \sum\limits_{i} \left(\frac{\partial q_{U}^{j}}{\partial q_{V}^{i}}\right)\dot{q}_{V}^{i}
$$
This is the meaning of the tangent bundle! Let us see now how the $p$'s transform.
$$
p_{i}^{V} \equiv \frac{\partial L}{\partial \dot{q}_{V}^{i}} = \sum\limits_{j} \left[\frac{\partial L}{\partial q_{U}^{j}} \frac{\partial q_{U}^{j}}{\partial \dot{q}^{i}_{V}} + \frac{\partial L}{\partial \dot{q}_{U}^{j}} \frac{\partial \dot{q}_{U}^{j}}{\partial \dot{q}_{V}^{i}}\right]
$$
However, $q_{V}$ does not depend on $\dot{q}_{U}$; likewise, $q_{U}$ does not depend on $\dot{q}_{V}$, and therefore the first term in this sum vanishes. Also, from (2.27),
$$
\frac{\partial \dot{q}_{U}^{j}}{\partial \dot{q}_{V}^{i}} = \frac{\partial q_{U}^{j}}{\partial q_{V}^{i}}
$$
Thus
$$
p_{i}^{V} = \sum\limits_{j} p_{j}^{U} \left(\frac{\partial q_{U}^{j}}{\partial q_{V}^{i}}\right)
$$
and so the $p$'s represent then not the components of a vector on the configuration space $M^{n}$ but rather a _covector_. The $q$'s and $p$'s then are to be thought of not as local coordinates in the tangent bundle but as coordinates for the _cotangent bundle_. Equation (2.26) is then to be considered not as a change in coordinates in $TM$ but rather as the local description of a map 
$$
P:TM^{n} \rightarrow T^{*} M^{n}
$$
_from the tangent bundle to the cotangent bundle_. We shall frequently call $(q^{1},\ldots,q^{n},p_{1},\ldots,p_{n})$ the local coordinates for $T^{*}M^{n}$ (even when we are not dealing with mechanics). This space $T^{*}M$ of covectors to the configuration space is called in mechanics the **phase space** of the dynamical system. 

Recall that there is no _natural_ way to identify vectors on a manifold $M^{n}$ with covectors on $M^{n}$. We have managed to make such an identification, $\sum\limits_{j}\dot{q}^{j} \frac{\partial}{\partial q^{j}} \rightarrow \sum\limits_{j} \left(\frac{\partial L}{\partial \dot{q}^{j}}\right) dq^{j}$, by introducing an extra structure, a Lagrangian function. $TM$ and $T^{*}M$ exist as soon as a manifold $M$ is given. We may locally identify these spaces by giving a Lagrangian function, but of course the identification changes with a change of $L$, that is, a change of "dynamics."

Whereas the $\dot{q}$'s of $TM$ are called generalized velocities, the $p$'s are called generalized **momenta**. This terminology is suggested by the following situation. The Lagrangian is frequently of the form 
$$
L(q,\dot{q}) = T(q,\dot{q}) - V(q)
$$
where $T$ is the kinetic energy and $V$ is the potential energy. $V$ is usually independent of $\dot{q}$ and $T$ is frequently a positive definite symmetric quadratic form in the velocities
$$
T(q,\dot{q}) = \frac{1}{2} \sum\limits_{jk} g_{jk}(q)  \dot{q}^{j} \dot{q}^{k}
$$
Note that this matrix $g_{jk}$ will correspond the masses of the objects at play. This is a generalization which allows terms of mass to depend on the positions. In the general case,
$$\tag{2.32}
p_{i} = \frac{\partial L}{\partial \dot{q}_{i}} = \frac{\partial T}{\partial \dot{q}^{i}} = \sum\limits_{j}g_{ij}(q)\dot{q}^{j}
$$
Thus, if we think of $2T$ as defining a _Riemannian metric_ on the configuration space $M^{n}$
$$
\left<\dot{q},\dot{q} \right> = \sum\limits_{ij}g_{ij}(q)\dot{q}^{i} \dot{q}^{j}
$$
then the kinetic energy represents half the length squared of the velocity vector, and the _momentum_ $p$ is by (2.32) simply _the covariant version of the velocity vector $\dot{q}$_. In the case of the two masses on $\mathbb{R}$ we have 
$$
p_{1} = m_{1}\dot{q}^{1} \quad \text{and} \quad p_{2} = m_{2}\dot{q}^{2}
$$
are indeed what everyone calls the momenta of the two particles. (Where the metric is the tensor (diagonal matrix): $diag \ (m_{1},m_{2})$) 

The tangent and cotangent bundles, $TM$ and $T^{*}M$, exist for any manifold $M$, independent of mechanics. They are distinct geometric objects. If, however, $M$ is a Riemannian manifold, we may define a diffeomorphism (note the previous condition of the determinant $\neq 0$) $TM^{n} \rightarrow T^{*}M^{n}$ that sends the coordinate patch $(q,\dot{q})$ to the coordinate patch $(q,p)$ by 
$$
p_{i} = \sum\limits_{j}g_{ij}\dot{q}^{j}
$$
with inverse 
$$
\dot{q}^{i} = \sum\limits_{j}g^{ij}p_{j}
$$
We did just this in mechanics, where the metric tensor was chosen to be that defined by the kinetic energy quadratic form. 

#### The Poincare 1-Form
Since $TM$ and $T^{*}M$ are diffeomorphic, it might seem that there is no particular reason for introducing the more abstract $T^{*}M$, but this is not so. There are certain geometrical objects that naturally live on $T^{*}M$ and not $TM$. Of course these objects can be brought back to $TM$ by means of our identifications, but this is not only frequently awkward, it would also depend, say, on the specific Lagrangian or metric tensor employed. 

Recall that "1-form" is simply another name for covector. We shall show, with Poincare, that there is a well-defined 1-form field on every cotangent bundle $T^{*}M$. This will be a linear functional defined on each tangent vector to the $2n$-dimensional manifold $T^{*}M^{n}$, not $M$. 

**Theorem (2.33):**  There is a globally defined 1-form on every cotangent bundle $T^{*}M^{n}$, the Poincare 1-form $\lambda$. In local coordinates $(p,q)$ it is given by 
$$
\lambda = \sum\limits_{i}p_{i}dq^{i}
$$
(Note that the most general 1-form on $T^{*}M$ is locally of the form $\sum\limits_{i} a_{i} (q,p) dq^{i} + \sum\limits_{i} b_{i}(q,p)dp_{i}$, and also note that the expression given for $\lambda$ cannot be considered a 1-form on the manifold $M$ since $p_{i}$ is not a function on M!) 

**Proof:**  The proof can be found on page 120 of [[Geometry of Physics.pdf]]. (or page 57 in the actual book).

---
There is an intrinsic definition of the form $\lambda$, that is, a definition not using coordinates. Let A be a point in $T^{*}M$; we shall define the 1-form $\alpha$ at $A$. $A$ represents a 1-form $\alpha$ at a point $x \in M$. Let $\pi:T^{*}M^{n}\rightarrow M^{n}$ be the _projection_ that takes a point in $T^{*}M$ to the point $x$ at which the form $\alpha$ is located. Then the pull-back $\pi^{*}\alpha$ defines a 1-form at each point of $\pi^{-1}(x)$, in particular at $A$. $\lambda$ at $A$ is precisely this form $\pi^{*}\alpha$! 

Let us check that these two definition are indeed the same. In terms of local coordinates $q$ for $M$ and $(q,p)$ for $T^{*}M$ the map $\pi$ is simply $\pi(q,p) = (q)$. The point $A$ with local coordinates $(q,p)$ represents the form $\sum\limits_{j} p_{j}dq^{j}$ at the point $q$ in $M$. Compute the pull-back (i.e., use the chain rule)
$$
\pi^{*} \left( \sum\limits_{i}p_{i}\pi^{*}dq^{i} \right) = \sum\limits_{i}p_{i} \pi^{*} (dq^{i}) = \sum\limits_{i}p_{i} \sum\limits_{j}\left[\left(\frac{\partial q^{i}}{\partial q^{j}}\right)dq^{j}+ \left(\frac{\partial q^{i}}{\partial p_{j}} \right)dp_{j} \right]
$$
$$
= \sum\limits_{i} p_{i} \sum\limits_{j} \delta^{i}_{j} dq^{j} = \sum\limits_{i}p_{i}dq^{i} =\lambda \quad \square
$$
---
## Tensors 

How does one construct field strength from a vector potential?

##### Covariant Tensors 
For most of these formulations we shall be concerned with linear algebra of a vector space $E$. Almost all of our applications will involve the vector space $E=M_{x}^{n}$ of tangent vectors to a manifold at a point $x \in E$. Consequently, let us denote a basis $\pmb{e}$ of $E$ by $\partial = (\partial_{1},\partial_{2},\ldots,\partial_{n})$, with dual basis $\sigma=dx=(dx^{1},\ldots,dx^{n})$. 

```ad-Definition
A covariant tensor of rank $r$ is a multilinear real-valued function
$$
Q:E\times E \times \ldots E \rightarrow \mathbb{R}
$$
of $r$-tuples of vectors, multilinear meaning that the function $Q(\pmb{v}_{1},\ldots,\pmb{v}_{r})$ is linear in each entry provided that the reamaining entries are held fixed. 
```

```ad-warning
Let us emphasize that the values of this function **must be independent of basis in which the components are expressed**. 
```

A covariant vector is just a covariant tensor of rank 1. When $r=2$, a multilinear function is called bilinear. The most important covariant second-rank tensor is probably the metric tensor $G$:
$$
G(\pmb{v},\pmb{w}) = \left<\pmb{v},\pmb{w}\right>=\sum\limits_{ij}g_{ij}v^{i}w^{j}
$$
which is clearly bilinear and independent of basis. We need a systematic notation for indices. We shall instead write $i_{1},\ldots,i_{r}$ instead of $i,j,k,\ldots$. 

In components, we have, by multilinearity,
$$
Q(\mathbf{v_{1}},\ldots,\mathbf{v}_{r}) = Q\left(\sum\limits_{i_{1}}v_{1}^{i_{1}}\mathbf{\partial}_{i},\ldots,\sum\limits_{i_{r}}v_{r}^{i_{r}}\mathbf{\partial}_{i_{r}}\right)
$$
$$
=\sum\limits_{i_{1}}v_{1}^{i_{1}}Q\left(\mathbf{\partial}_{i_{1}},\ldots,\sum\limits_{i_{r}}v_{r}^{i_{r}}\mathbf{\partial}_{i_{r}}\right) = \ldots
$$
$$=\sum\limits_{i_{1}\ldots,i_{r}}v_{1}^{i_{1}}\ldots v_{r}^{i_{r}}Q(\mathbf{\partial}_{i_{1}},\ldots,\mathbf{\partial_{i_{r}}}) 
$$
That is,
$$
Q(\mathbf{{v}}_{1},\ldots,\mathbf{v}_{r}) = \sum\limits_{i_{1},\ldots,i_{r}} Q_{i_{1},\ldots,i_{r}}v_{1}^{i_{1}}\ldots v_{r}^{i_{r}}
$$
where 
$$
Q_{i_{1}\ldots,i_{r}} \equiv Q(\partial_{i_{1}},\ldots,\partial_{i_{r}})
$$
We now shall begin using Einstein summation convention to write these expressions easier (summation is implied when seeing a variable in a upper and lower index). For example $a^{i}_{i} = \sum\limits_{i}a^{i}_{i}$ is the trace of a matrix $A=(a^{i}_{j})$. With this convention we now write 
$$
Q(\mathbf{v}_{1},\ldots,\mathbf{v}_{r}) = Q_{i_{1},\ldots,i_{r}}v_{1}^{i_{1}},\ldots v_{r}^{i_{r}}
$$
The collection of all covariant tensors of rank $r$ forms a vector space under the usual operations of addition of functions and multiplication of functions by real numbers. These simply correspond to addition of their components $Q_{i,\ldots,j}$ and multiplication of the components by real numbers. The number of components in such a tensor is clearly $n^{r}$. This vector space is the space of covariant $r^{th}$ rank tensors and will be denoted by 
$$
E^{*} \otimes E^{*} \otimes \ldots \otimes E^{* }= \otimes^{r}E^{*}
$$
IF $\alpha$ and $\beta$ are covectors, that is, elements of $E^{*}$, we can form the second-rank covariant tensor, the **tensor product** of $\alpha$ and $\beta$ as follows. We need only tell how $\alpha \otimes \beta:E \times E \rightarrow \mathbb{R}$. 
$$
\alpha \otimes \beta(\mathbf{v},\mathbf{w}) \equiv \alpha(\mathbf{v})\beta(\mathbf{w})
$$
In components, $\alpha = a_{i}dx^{i}$ and $\beta=b_{j}dx^{j}$, and 
$$
(\alpha \otimes \beta)_{ij} = \alpha \otimes \beta(\partial_{i},\partial_{j}) = \alpha(\partial_{i})\beta(\partial_{j}) = a_{i}b_{j}
$$
which form the components of $\alpha \otimes \beta$. 

---
##### Contravariant Tensors 
Note first that a contravariant vector, that is, an element of $E$, can be considered as a linear function on vectors by defining 
$$
\mathbf{v}(\alpha) \equiv \alpha(\mathbf{v})
$$
In components, $\mathbf{v}(\alpha)=a_{i}v^{i}$ is clearly linear in the components of $\alpha$. 

```ad-Definition
A **contravariant tensor** of rank $s$ is a multilinear real valued function $T$ on $s$-tuples of _covectors_
$$
T:E^{*} \times E^{*} \times \ldots \times E^{*} \rightarrow \mathbb{R}
$$
```

As for covariant tensors, we can show immediately that for an $s$-tuple of 1-forms $\alpha_{1},\ldots,\alpha_{s}$:
$$
T(\alpha_{1},\ldots,\alpha_{s}) = {a_{1}}_{i_{1}}\ldots {a_{s}}_{i_{s}} T^{i_{1}\ldots i_{s}}
$$
where 
$$
T^{i_{1}\ldots i_{s}} \equiv T(dx^{i_{1}},\ldots,dx^{i_{s}})
$$
We write for this space of contravariant tensors 
$$
E \otimes E \otimes \ldots \otimes E \equiv \otimes^{s}E
$$
Contravariant vectors are of course contravariant tensors of rank 1. An example of a second-rank contravariant tensor is the inverse to the metric tensor $G^{-1}$, with components $(g^{ij})$, 
$$
G^{-1}(\alpha, \beta) = g^{ij}a_{i}b_{j}
$$
However, let us ask the question, does the matrix $g^{ij}$ really define a tensor $G^{-1}$? The local expression for $G^{-1}(\alpha, \beta)$ is certainly bilinear, but what about coordinate-independence? However, note that the vector $\mathbf{b}$ associated to $\beta$ is coordinate independent since $\beta(\mathbf{v})=\left<\mathbf{v}, \mathbf{b}\right>$ and the metric $\left<,\right>$ is coordinate independent. But then $G^{-1}(\alpha, \beta)=g^{ij}a_{i}b_{j}=a_{i}b^{i}=\alpha(\mathbf{b})$ is indeed independent of coordinates, and $G^{-1}$ is a tensor. 

Given a pair $\mathbf{v}, \mathbf{w}$ of contravariant vector, we can form their tensor product $\mathbf{v} \otimes \mathbf{w}$ in the same manner as we did for covariant vectors. It is the second-rank contravariant tensor with components $(\mathbf{v} \otimes \mathbf{w})^{ij}=v^{i}w^{j}$. From this, we may derive the expressions 
$$
G = g_{ij}dx^{i}\otimes dx^{j} \quad \text{and} \quad G^{-1} = g^{ij}\partial_{i} \otimes \partial_{j}
$$
---
##### Mixed Tensors 

The following definition in fact includes that of covariant and contravariant tensors as special cases when $r$ or $s=0$.

```ad-Definition
A **mixed tensor**, $r$ times covariant and $s$ times contravariant, is a real multilinear function $W$
$$
W:E^{*} \times E^{*} \times \ldots \times E^{*} \times E \times E \times \ldots \times E \rightarrow \mathbb{R}
$$
on $s$-tuples of covectors and $r$-tuples of vectors.
```

By multilinearity, 
$$
W(\alpha_{1},\ldots,\alpha_{s},\mathbf{v}_{1},\ldots,\mathbf{v}_{r})={a_{1}}_{i_{1}}\ldots {a_{s}}_{i_{s}} W^{i_{1}\ldots i_{s}}_{j_{1}\ldots j_{r}} v_{1}^{j_{1}}\ldots v^{j_{r}}_{r}
$$
where 
$$
W^{i_{1}\ldots i_{s}}_{j_{1}\ldots j_{r}}\equiv W(dx^{i_{1}},\ldots,\partial_{j_{r}})
$$
A second rank mixed tensor arises from a _linear transformation_ $\mathbf{A}:E \rightarrow E$. Define $W_{A}:E^{*}\times E \rightarrow \mathbb{R}$ by $W_{A}(\alpha,\mathbf{v})=\alpha(\mathbf{A}\mathbf{v})$. Let $A=(A^{i}_{j})$ be the matrix of $\mathbf{A}$, that is, $\mathbf{A}(\partial_{j})=\partial_{i}A^{i}_{j}$. The components of $W_{A}$ are given by 
$$
{W_{A}}^{i}_{j} = W_{A}(dx^{i},\partial_{j}) = dx^{i}(\mathbf{A}(\partial_{j}))= \delta^{i}_{k}{A^{k}}_{j} = {A^{i}}_{j}
$$
_The matrix of the mixed tensor $W_{A}$ is simply the matrix of $\mathbf{A}$_! Conversely, given a mixed tensor $W$, once covariant and once contravariant, we can define a linear transformation $\mathbf{A}$ by saying $\mathbf{A}$ is that unique linear transformation such that $W(\alpha, \mathbf{v})=\alpha(\mathbf{Av})$. Such an $\mathbf{A}$ exists since $W(\alpha,\mathbf{v})$ _is_ linear in $\mathbf{v}$. Thus, we shall not distinguish between a linear transformation and its associated mixed tensor. We shall consider them all the same!

```ad-note
Note that the $\mathbf{A}(\partial_{j})$ condition is so that the transform acting on a basis vector gives back the vector form of the linear transform for the j-th column.

This can be easily proven. 
```

Note that in components the bilinear form has the pleasant matrix expression 
$$
W(\alpha,\mathbf{v}) = a_{i}{A^{i}}_{j} v^{j} = aVv
$$
The tensor product $\mathbf{w}\otimes \beta$ of a vector and a covector is the mixed tensor defined by 
$$
(\mathbf{w} \otimes \beta)(\alpha, \mathbf{v}) = \alpha(\mathbf{w})\beta(\mathbf{v})
$$
Which we can write as 
$$
\mathbf{A} = {A^{i}}_{j} \partial_{i} \otimes dx^{j} = \partial_{i} \otimes {A^{i}}_{j} dx^{j}
$$
In particular, the _identiy_ linear transformation is 
$$
I = \partial_{i} \otimes dx^{i}
$$
and its components are of course $\delta^{i}_{j}$. 

Note that we have written matrices in three different ways, $A_{ij},A^{ij},$ and $A^{i}_{j}$. The first two define bilinear forms (on $E$ and $E^{*}$ respectively)
$$
A_{ij}v^{i}w^{j} \quad \text{and} \quad A^{ij}a_{i}b_{j}
$$
and only the last is the matrix of a linear transformation $\mathbf{A}:E \rightarrow E$. A point of confusion in elementary linear algebra arises since the matrix of a linear transformation there is usually written $A_{ij}$ and they make no distinction between linear transformations and bilinear forms. We _must_ make the distinction. The the case of an inner product space $E$, $\left<, \right>$ we may relate these different tensors as follows. Given a linear transformation $\mathbf{A}:E \rightarrow E$, that is, a mixed tensor, we may associate a covariant bilinear form $A'$ by 
$$
A'(\mathbf{v,w}) \equiv \left<\mathbf{v}, \mathbf{Aw}\right> = v^{i} g_{ij}{A^{j}}_{k}w^{k}
$$
Thus $A'_{ik}=g_{ij}A^{j}_{k}$. Note that we have "lowered the index $j$, making it a $k$, by means of the metric tensor." In tensor analysis one uses the same letter; that is, instead of $A'$ we merely write $A$,
$$
A_{ik} \equiv g_{ij}{A^{j}}_{k}
$$
It is clear from the placement of the indices that we now have a covariant tensor. This is the matrix of the covariant bilinear form associated to the linear transformation $\mathbf{A}$. In general its components differ from those of the mixed tensor, but they _coincide then the basis is orthonormal_ ($g_{ij} = \delta^{i}_{j}$). Since orthonormal bases are almost always used in elementary linear algebra, they may dispense with the distinction. 

In a similar manner one may associate to the linear transformation $\mathbf{A}$ a contravariant bilinear form 
$$
\overline{A}(\alpha, \beta) = a_{i}{A^{i}}_{j}g^{jk}b_{k}
$$
whose matrix of components would be written 
$$
A^{ik}={A^{i}}_{j}g^{jk}
$$
**Remark.**  Recall that the components of a second-rank tensor always form a matrix such that the left-most index denotes the row and the right-most index the column, independent of whether the index is up or down.

A final remark. The matrix tensor $\{g_{ij}\}$, being a covariant tensor, does _not_ represent a linear transformation of $E$ into itself. However, it _does_ represent a linear transformation from $E$ to $E^{*}$, sending the vector with components $v^{j}$ into the covector with components $g_{ij}v^{j}$. 

---

##### Transformation Properties of Tensors 
As we have seen, a mixed tensor has components (with respect to a basis $\partial$ of $E$ and the dual basis $dx$ of $E^{*}$) given by 
$$
{W^{i\ldots j}}_{k\ldots l}  =W(dx'^{i},\ldots,dx'^{j},\partial'_{k},\ldots,\partial'_{l})
$$
Under a change of bases (remember the transformation rules and how the basis transform inverse to their components), $\partial'_{l} = \partial_{s}\left(\frac{\partial x^{s}}{\partial x'^{l}}\right)$ and $dx'^{i} = \left(\frac{\partial x'^{i}}{\partial x^{c}}\right) dx^{c}$ we have, by multilinearity 
$$
{W'^{i\ldots j}}_{k\ldots l} = W(dx'^{1},\ldots,dx'^{j},\partial'_{k},\ldots,\partial'_{l})
$$
$$
 = \left(\frac{\partial x'^{i}}{\partial x^{c}}\right)\ldots \left(\frac{\partial x'^{j}}{\partial x^{d}}\right) \left(\frac{\partial x^{r}}{\partial x'^{k}}\right) \ldots \left(\frac{\partial x^{s}}{\partial x'^{l}}\right) {W^{c\ldots d}}_{r\ldots s}
$$
Similarly, for covariant $Q$ and contravariant $T$ we have 
$$
Q'_{i\ldots j} = \left(\frac{\partial x^{k}}{\partial x'^{i}}\right) \ldots \left(\frac{\partial x^{l}}{\partial x'^{j}}\right)Q_{k\ldots l}
$$
and 
$$
T'^{i\ldots j} = \left(\frac{\partial x'^{i}}{\partial x^{k}}\right)\ldots \left(\frac{\partial x'^{j}}{\partial x^{l}}\right)T^{k\ldots l} 
$$
Classical tensor analysts dealt not with multilinear functions, but rather with their components. They would say that a mixed tensor assigns, to each basis of $E$, a collection of "components" ${W^{i\ldots j}}_{k\ldots l}$ such that under a change of basis the components transform by the law expressed above. This is a convenient terminology generalizing what we know about vectors and $\mathbf{v} = v \mathbf{e}$. 

```ad-warning
A linear transformation (mixed tensor) $A$ has eigenvalues $\lambda$ deetermined by the equation $A \mathbf{v} = \lambda \mathbf{v}$, that is, ${A^{i}}_{j}v^{j}= \lambda v^{i}$, but a covariant second-rank tensor $Q$ does not. This is evident just from our notation: $Q_{ij}v^{j} = \lambda v^{i}$ makes no sense since $i$ is a covariant index on the left whereas it is a contravariant index on the right. Of course we _can_ solve the linear equations as in linear algebra with $\det (Q - \lambda I)=0$, but the point is that the _solutions_ $\lambda$ _depend on the basis used_. Under a change of basis, the transformation rue says $Q'_{ij} =  \left(\frac{\partial x^{k}}{\partial x'^{i}}\right)Q_{kl} \left(\frac{\partial x'}{\partial x'^{j}}\right)$. Thus we have 
$$
Q' = \left(\frac{\partial x}{\partial x'}\right)^{T}Q\left(\frac{\partial x}{\partial x'}\right)
$$
and the solutions of $\det[Q' - \lambda I]=0$ in general differ from those of $\det[Q- \lambda I]=0$. (In the case of a _mixed_ tensor $W$, the transpose $T$ is replaces by the inverse, yielding an invariant equation $\det(W'-\lambda I) = \det(W - \lambda I))$ It thus makes no intrinsic sence to talk about the eigenvalues or eigenvalues of a quadratic form. Of coruse if we have a metric tensor $g$ given, to a covariant matrix $Q$ we may form the mixed version $g^{ij} Q_{jk} = {W^{i}}_{k}$ and then find the eigenvalyes of this $W$. This is equivalent to solving 
$$
Q_{ij}v^{j}= \lambda g_{ij}v^{j}$$
and this requires 
$$
\det(Q - \lambda g) = 0
$$
It is easy to see that this equation is independent of basis, as is clear also from our notation. We may call these eigenvalues $\lambda$ the **eigenvalues of the quadratic form with respect to the given metric** $g$. This situation arises in the problems of _small oscillations of a mechanical system_. 
```

---
##### Tensor Fields on Manifolds 
A (differentiable) tensor field on a manifold has components that vary differentiably. A Riemannian metric $(g_{ij})$ is a very important second-rank covariant tensor field. 

Tensors are important on manifold because they allow us to construct expressions by using local coordinates, yet in a way that allows our expressions to have an intrinsic _meaning_ that all coordinate systems agree upon.

Tensors in physics usually describe physical fields. For example, Einstein discovered that the metric tensor in 4-dimensional space-time describes the gravitational field. Different observers will usually use different local coordinates in 4-space. By making measurements with "rulers and clocks," each observer can in principle measure the components of $g_{ij}$ for their coordinate system. Since the metric of space-time is assumed to have physical significance, although two observers will find different components in their systems, the two sets of components $g_{ij}$ and $g_{ij}'$ will be related by the transformation law for a covariant tensor of the second rank. The observers will then want to describe and _agree_ on the _strength_ of the gravitational field, and this will involve derivatives of their metric components, just as the Newtonian strength is measured by $grad \ \phi$. By "agree," we mean, presumably, that the strengths will again be components of some tensor, perhaps of higher rank. We shall see that this is not at all a trivial task. 

We shall illustrate this point with a far simpler example; this example will be dealt with more extensively later on, after we have developed the appropriate tools. 

Space-time is some manifold $M$, perhaps not $\mathbb{R^{4}}$. Electromagnetism is described locally by a "vector potential," that is, by some vector field. It is not usually clear in the texts whether the vector is contravariant or covariant; recall that even in Minkowski space there are differences in the components of the covariant and contravariant versions of a vector field. However, there is good reason to assume that the _vector potential is a covector_ $\alpha= A_{j} dx^{j}$ (see book problem 2.4(3) for more info, its because we can see that $g_{ji}v^{i}$ transforms like a vector).  

In the following we shall use the popular notations $\partial_{i} \phi \equiv \frac{\partial \phi}{\partial x^{i}}$ and $\partial'_{i} \phi = \frac{\partial \phi}{\partial x'^{i}}$. The electromagnetic _field strength_ will involve derivatives of the A's, but it will be clear from the following calculation that the expressions 
$$
\partial_{i} A_{j}
$$
do _not_ form the components of a second-rank tensor!

**Theorem (2.42):**  If $A_{j}$ are the components of a covariant vector on any manifold, then 
$$
F_{ij} \equiv \partial_{i}A_{j} - \partial_{j}A_{i}
$$
form the components of a second-rank covariant tensor. 

**Proof:**  We need only verify the transformation law as stated prior. Since $\alpha =A_{j}dx^{j}$ _is_ a covector, we have $A'_{j}=(\partial_{j}'x^{l})A_{l}$ and so 
$$
F_{ij}' = \partial_{i}'A_{j}'-\partial_{j}'A_{i}' = \partial_{i}'\{(\partial_{j}'x^{l})A_{l}\} - \partial_{j}'\{(\partial_{i}')x^{l}A_{l}\}
$$
$$
 = (\partial_{j}'x^{l})(\partial_{i}'A_{l})+[(\partial_{i}'\partial_{j}'x^{l})A_{l}]-(\partial_{i}'x^{l})(\partial_{j}'A_{l}) - (\partial_{j}'\partial_{i}'x^{'})A_{l}
$$
$$
=(\partial_{j}'x^{l})(\partial_{r}A_{l})(\partial_{i}'x^{r}) - (\partial_{i}'x^{l})(\partial_{r}A_{l})(\partial_{j}'x^{r})
$$
(and since $r$ and $l$ are dummy summation indices)
$$
=(\partial_{i}'x^{l})(\partial_{j}'x^{r})(\partial_{l}A_{r}-\partial_{r}A_{l}) 
$$
$$
= (\partial_{i}'x^{l})(\partial_{j}'x^{r})F_{lr}
$$
Note that the term in brackets $[]$ is what prevents $\partial_{i}A_{j}$ itself from defining a tensor. Note also that if our manifold were $\mathbb{R}^{n}$ and if we restricted ourselves to _linear_ changes in coordinates, $x'^{i}=L_{j}^{i}x^{j}$, then $\partial_{l}A_{j}$ would transform as a tensor. One _can_ talk about objects that transform as tensors with respect to some restricted class of coordinate systems; a _cartesian tensor_ is one based on cartesian coordinate systems, that is, on orthogonal changes of coordinates. For the present we shall allow _all_ changes of coordinates. In our electromagnetic case, $(F_{ij})$ is the **field-strength tensor**. 

```ad-note
If an object transforms like a tensor, it can be seen that it must be indepdent of basis. If we were to change basis, then we would get different components in the tensor. However, because the tensor is linear in all of its arguments, it would satisfy the tensor transformation law. Then, all the factors cancel out and stuff and we see independence of basis.... just do the math and see for yourself. 
```

---
Our next immediate task will be the construction of a mathematical machine, the "exterior calculus," that will allow us systematically to generate "field strengths" generalizing our results above (Theorem 2.42). 

### The Grassmann or Exterior Algebra 

How can we define an _oriented_ area spanned by two vectors in $\mathbb{R}^{n}$

---
##### The Tensor Product of Covariant Tensors
Before the middle of the nineteenth century, Grassmann introduced a new "algebra" whose product is a vast generalization of the scalar and vector products in use today in vector analysis In particular it is applicable in space of any dimension. Before discussing the "Grassmann product" it is helpful to consider a simpler product, special cases of which we have used earlier. Before we defined the vector space $\otimes^{p}E^{*}$ of covariant $p$-tensors over the vector space $E$; these covariant tensors were simply $p$-linear maps $\alpha:E\times\ldots \times E \rightarrow \mathbb{R}$. We now define the "tensor" product of a covariant $p$-tensor and a covariant $q$-tensor. 

```ad-Definition
If $\alpha \in \otimes^{p}E^{*}$ and $\beta \in \otimes^{q}E^{*}$, then their **tensor product** $\alpha \otimes \beta$ is the covariant $(p+q)$ tensor defined by 
$$
\alpha \otimes \beta(\mathbf{v}_{1},\ldots, \mathbf{v}_{p+q}) \equiv \alpha(\mathbf{v}_{1},\ldots,\mathbf{v}_{p})\beta(\mathbf{v}_{p+1},\ldots,\mathbf{v}_{p+q})
$$
```

---
##### The Grassmann or Exterior Algebra 
```ad-Definition
An (**exterior**) **p-form** is a covariant $p$-tensor $\alpha\in \otimes^{p}E^{*}$ that is antisymmetric (=skew symmetric = alternating)
$$
\alpha(\ldots \mathbf{v}_{r},\ldots,\mathbf{v}_{s},\ldots) = -\alpha(\ldots \mathbf{v}_{s},\ldots \mathbf{v}_{r},\ldots)
$$
in each pair of entries.
```

In particular, the value of $\alpha$ will be $0$ if the same vector appears in two different entries. The collection of all $p$-forms is a vector space 
$$
\bigwedge^{p} E^{*} = E^{*}\wedge E^{*} \wedge \ldots \wedge E^{*} \subset \otimes^{p}E^{*}
$$
By definition, $\wedge^{1}E^{*}=E^{*}$ is simply the space of $1$-forms. It is convenient to make the special definition $\wedge^{0}E^{*} \equiv \mathbb{R}$, that is, 0-forms are simply scalars. A $0$-form field on a manifold is a differentiable _function_. 

We need again to simplify the notation. We shall use the notion of a "multiindex," $I = (i_{1},\ldots,i_{p})$; the number $p$ of indices appearing will usually be clear from the context. Furthermore, we shall denote the $p$-tuple of vectors $(\mathbf{v}_{i_{1}},\ldots,\mathbf{v}_{i_{p}})$ simply by $\mathbf{v}_{I}$. 

Let $\alpha \in \bigwedge^{p}E^{*}$ be a $p$-form, and let $\partial$ be a basis of $E$. Then by multilinearity $\alpha$ is determined by its $n^{p}$ components 
$$
\alpha_{I} = a_{i_{1},\ldots,i_{p}} = \alpha(\partial_{i_{1}},\ldots, \partial_{i_{p}}) = \alpha(\partial_{I})
$$
By skew symmetry
$$
a_{i_{1},\ldots,i_{r},\ldots,i_{s},\ldots,i_{p}} = -a_{i_{1},\ldots,i_{s},\ldots,i_{r},\ldots,i_{p}}
$$
Thus $\alpha$ is completely determined by its values $\alpha(\partial_{i_{1}},\ldots,\partial_{i_{p}})$ where the indices are in strictly increasing order. When the indices in $I$ are in increasing order, $i_{1}<i_{2}<\ldots<i_{p}$ we shall write $\underset{\rightarrow}{I}$
$$
\underset{\rightarrow}{I} = (i_{1}<\ldots<i_{p})
$$
The number of distinct $\underset{\rightarrow}{I} = (i_{1}<\ldots<i_{p})$ is the combinatorial symbol, that is, 
$$
\dim \bigwedge^{p}E^{*} = \frac{n!}{p!(n-p)!}
$$
where $n$ is the dimension of $E^{*}$. The dimension of the space of $n$-forms, where $n=\dim E$ is 1; any $n$-form is determined by its value of $(\partial_{1},\ldots,\partial_{n})$. Furthermore, since a repeated $\partial_{i}$ will give $0$, $\wedge^{p}E^{*}$ is $0$-dimensional if $p>n$. _There are no nontrivial p-forms on an n-manifold when p>n_. 

We now wish to define a product of exterior forms. Clearly, if $\alpha$ is a $p$-form and $\beta$ is a q-form then $\alpha \otimes \beta$ is a $(p+q)$ _tensor_ that is skew symmetric in the first $p$ and last $q$ entries, but need not be skew symmetric in all entities; that is, it need not be a $(p+q)$ form. Grassmann defined a new product $\alpha \wedge \beta$ that is indeed a form. To motivate the definition, consider the case of $1$-forms $\alpha^{1}$ and $\beta^{1}$ (the superscripts are not tensor indices; they are merely to remind us that the forms are $1$-forms). If we put 
$$
\alpha^{1} \wedge \beta^{1} \equiv \alpha \otimes \beta - \beta\otimes \alpha
$$
that is, 
$$
\alpha \wedge \beta(\mathbf{v,w}) = \alpha(\mathbf{v}) \beta(\mathbf{w}) - \beta(\mathbf{v}) \alpha(\mathbf{w})
$$
then $\alpha \wedge \beta$ is then not only a tensor, it is a 2-form. In a sense, we have taken the tensor product for $\alpha$ and $\beta$ and skew-symmetrized it. Define a "generalized Kronecker delta" symbol as follows
$$
\delta_{J}^{I} \equiv 1 \quad \text{if} \quad J=(j_{1},\ldots,j_{r}) \text{ is an even permutation of }I=(i_{1},\ldots,i_{r})
$$
$$
= -1 \quad \text{ if } J \text{ is an off permutation of } I
$$
$$
= 0 \quad \text{if } J \text{ is not a permutation of }I 
$$
For examples, $\delta_{621}^{126} = -1, \delta_{623}^{126}=0,\delta_{612}^{126}=1$. We can then define the usual permutation symbols (Levi-Civita Symbol)
$$
\epsilon_{I}=\epsilon_{i_{1},\ldots,i_{n}} = \epsilon^{I} \equiv \delta^{I}_{1,2,\ldots,n}
$$
describing whether the $n$ indices $i_{1},\ldots,i_{n}$ form an even or off permutation of $1,\ldots,n$. This appears in the definition of the determinant of a matrix (Leibniz Formula)
$$
\det A = \epsilon_{I}{A^{i_{1}}}_{1}{A^{i_{2}}}_{2}\ldots {A^{i_{n}}}_{n}
$$
(From this one can see that the $\epsilon$ symbol does _not_ define a tensor. For in $\mathbb{R}^{2}$, if $\epsilon_{ij}$ defined a covariant tensor, we would have $1=\epsilon_{12}'=\epsilon_{rs} \left(\frac{\partial x^{r}}{\partial x'^{l}}\right)\left(\frac{\partial x^{s}}{\partial x'^{2}}\right) = \det \left(\frac{\partial x}{\partial x'}\right)$, which is only equal to $\epsilon_{12}=1$ if $\det \left(\frac{\partial x}{\partial x'}\right)=1$. 

We now define the **exterior** or **wedge** or **Grassmann** product
$$
\wedge : \bigwedge^{p}E^{*} \times \bigwedge^{q}E^{*} \rightarrow \bigwedge^{p+q}E^{*}
$$
of forms. Let $\alpha^{p}$ and $\beta^{q}$ be forms. We define $\alpha^{p} \wedge \beta^{q}$ to be the $(p+q)$-form with values on $(p+q)$-tuples of vectors $\mathbf{v}_{I},I = (i_{1},\ldots,i_{p+q})$ given as follows. Let $\underset{\rightarrow}{J}=(j_{1}<\ldots<j_{p})$ and $\underset{\rightarrow}{K} = (k_{1}<\ldots<k_{q})$ be subsets of $I$. Then 
$$
\alpha \wedge \beta(\mathbf{v}_{I}) \equiv \sum\limits_{\underset{\rightarrow}{K}}\sum\limits_{\underset{\rightarrow}{J}} \delta_{I}^{JK} \alpha(\mathbf{v}_{J}) \beta(\mathbf{v}_{K}) 
$$
or 
$$
(\alpha \wedge \beta)_{I }= \sum\limits_{\underset{\rightarrow}{K}}\sum\limits_{\underset{\rightarrow}{J}} \delta_{I}^{JK} \alpha_{J} \beta_{K}
$$
---
**Remark.**  If we take out the input, realize that the result above is the same as saying 
$$
(\alpha \wedge \beta)_{I }= \sum\limits_{\underset{\rightarrow}{K}}\sum\limits_{\underset{\rightarrow}{J}} \delta_{I}^{JK} (\alpha \otimes \beta)_{JK}
$$
since $(\alpha \otimes \beta)_{JK} = \alpha_{J} \beta_{K}$

---
For example, if $\dim E = 5$, and if $\mathbf{e}_{1},\ldots,\mathbf{e}_5$ is a basis for $E$ 
$$
(\alpha^{2} \wedge \beta^{1})_{523} = \alpha^{2} \wedge \beta(\mathbf{e}_{5},\mathbf{e}_{2},\mathbf{e}_{3}) = \sum\limits_{r<s} \sum\limits_{t} \delta^{rst}_{523} \alpha_{rs} \beta_{t}
$$
$$
= \delta^{235}_{523}\alpha_{23} \beta_{5}+\delta^{253}_{523} \alpha_{25}\beta_{3}+\delta^{352}_{523} \alpha_{35}\beta_{2}
$$
$$
= \alpha_{23}\beta_{5}-\alpha_{25}\beta_{3}+\alpha_{35}\beta_{2}
$$
```ad-note
Since the increasing indices define $\alpha$ and $\beta$, we have $I=(5,2,3)$ (due to what element we want) and since $\alpha$ is a 2-form (takes 2 inputs) we want $\alpha_{rs}$ such that $r<s$ (so they are in increasing indices). And then since $\beta$ is a 1-form, it can just get the leftover indice in $I$ (since it only takes one, there is nothing to make sure the indices are increasing). 
```

In general, one checks easily that $\alpha \wedge \beta$ is multilinear. Also, since $\delta_{i\ldots j \ldots k \ldots l}^{R} = - \delta^{R}_{i\ldots k \ldots j \ldots k}$ we see that $\alpha \wedge \beta$ is again skew symmetric. The wedge product, however, is not commutative in general. 
$$
(\beta^{q} \wedge \alpha^{p})_{I }= \sum\limits_{\underset{\rightarrow}{J}}\sum\limits_{\underset{\rightarrow}{K}} \delta_{I}^{KJ} \beta_{K} \alpha_{J}
$$
$$
= (-1)^{pq}\sum\limits_{\underset{\rightarrow}{J}}\sum\limits_{\underset{\rightarrow}{K}} \delta_{I}^{JK} \alpha_{J} \beta_{K} 
$$
since $KJ \rightarrow JK$ requires $pq$ transpositions. Thus, 
$$
\tag{2.44}\alpha^{p} \wedge \beta^{q} = (-1)^{pq} \beta^{q} \wedge \alpha^{p}
$$
In particular, for forms of _odd_ degree, $\alpha^{2p+1} \wedge \alpha^{2p+1}=0$. Thus
$$
dx \wedge dy = -dy \wedge dx, \quad dx \wedge dx = 0
$$
```ad-note
For a vector space of dimension $<4$, then the wedge product of any form with itself is $0$ (including even forms). However, this stops at dimensions $4$ and above and then only even forms wedged with themself are $0$.
```

We may consider the vector space of all forms of all degrees over $E^{*}$
$$
\bigwedge^{*}E^{*} \equiv \left(\bigwedge^{0}E^{*} = \mathbb{R} \right) \otimes \left(\bigwedge^{1}E^{*}\right) \otimes \ldots \otimes \left(\bigwedge^{n}E^{*}\right)
$$
This is the **Grassman** or **exterior algebra** over $E^{*}$, and
$$
\dim \bigwedge^{*}E^{*} = {n \choose 0} + {n \choose 1} + \ldots + {n \choose n} = 2^{n}
$$
where $n=\dim E$. 

It is crucial for computational purposes that the Grassmann algebra is distributive and associative. it is trivial to show distributivity; associativity will follow from the following very useful result. 

**Lemma (2.46)**:  $$ \sum\limits_{\underset{\rightarrow}{J}} \delta^{I \ J}_{M} \delta_{J}^{K \ L} = \delta_{M}^{I \ K \ L}$$
**Proof:**  $I, K, L$, and $M$ are all fixed. Since $J$ is in increasing order, there is at most one term on the left-hand side, namely when $J$ is some permutation of $KL$. One then simply verifies that the preceding formula is correct in the cases when $J$ is an even and an odd permutation of $KL$. 

One can now verify that the exterior product is associative. Let $M$ be any $(p+q+r)$ multiindex. Look at the component $[\alpha^{p} \wedge (\beta^{q} \wedge \gamma^{r})]_{M}$. Then 
$$
[\alpha^{p}\wedge (\beta^{q} \wedge \gamma^{r})]_{M} = \sum\limits_{\underset{\rightarrow}{I}\underset{\rightarrow}{J}} \delta^{IJ}_{M} \alpha_{I}(\beta \wedge \gamma)_{J}
$$
$$
= \sum\limits_{\underset{\rightarrow}{I}\underset{\rightarrow}{J}} \delta_{M}^{IJ} \alpha_{I} \sum\limits_{\underset{\rightarrow}{K}\underset{\rightarrow}{L}} \delta_{J}^{IJ} \beta_{K}\gamma_{L} = \sum\limits_{\underset{\rightarrow}{I}\underset{\rightarrow}{K}\underset{\rightarrow}{L}} \delta_{M}^{IKL} \alpha_{I}\beta_{K}\gamma_{L}
$$
It is clear that one would get the same expression for $[(\alpha \wedge \beta) \wedge \gamma]$. The same type of computation would show that if $\alpha_{(1)},\ldots,\alpha_{(r)}$ are all 1-forms and if $\mathbf{v}_{(1)},\ldots,\mathbf{v}_{(r)}$ is any $r$-tuple of vectors, then 
$$
\alpha_{(1)} \wedge \ldots \wedge \alpha_{(r)}(\mathbf{v}_{(1)},\ldots,\mathbf{v}_{(r)}) = \sum\limits_{I} \delta^{I}_{12\ldots r} \alpha_{(1)}(\mathbf{v}_{i(1)})\ldots \alpha_{(r)}(\mathbf{v}_{i(r)}) 
$$
$$
= \tag{2.47} \det [\alpha_{(j)}(\mathbf{v}_{i})]
$$
**Remark.**  $\alpha_{(j)}$ represents the column vector with inputs $\mathbf{v}_{i}$ for each row. You can additionally use the result above to show the distributive property for the wedge product.

Let $\sigma^{1},\ldots,\sigma^{n}$ be the basis of $1$-forms dual to $\mathbf{e}_{1},\ldots,\mathbf{e}_{n}$. If we write 
$$
\sigma^{I} \quad \text{for} \quad \sigma^{i_{1}}\wedge \ldots \wedge \sigma^{i_{r}}
$$
then we have 
$$
\sigma^{I}(\mathbf{e}_{J}) = \delta^{I}_{J}
$$
since this is certainly true, from (2.47), when $I$ and $J$ are increasing. It is now worth reading problem 2.5(1) of the textbook at this time. However, we shall simply supply it here. 

---
**Question 2.5(1):**  Show that we have the expansion for the $p$-form:
$$
\alpha^{p} = \sum\limits_{\underset{\rightarrow}I}a_{I}\sigma^{I} = \sum\limits_{\underset{\rightarrow}{I}} \alpha(\mathbf{e}_{I}) \sigma^{i_{n}}\wedge\ldots\wedge \sigma^{i_{n}}
$$
**Solution:**  Note that we can solve this in the same way we deduced the formula for covectors in [[#Linear Functionals and the Dual Space]]. We do 
$$
(a_{J}\sigma^{J})(\partial_{K}) = a_{J}\sigma^{J}(\partial_{K}) = a_J \delta^{J}_{K} = a_{K} = \alpha(\partial_{K})
$$
where the last part was from the [[#Covariant Tensors]] when we found that 
$$
Q_{i_{1}\ldots,i_{r}} \equiv Q(\partial_{i_{1}},\ldots,\partial_{i_{r}})
$$
(so to get a specific index you input those basis vectors). And thus the proof for this problem is done. $\square$ 

---
Note that $a_{I}=a_{i_{1},\ldots,i_{p}} \equiv \alpha(\mathbf{e}_{I})$ in the problem above is skew symmetric in $i_{1},\ldots,i_{p}$. The $a_{I}$ are the "components of the covariant tensor $\alpha$ with respect to the basis $\sigma^{1},\ldots,\sigma^{n}$ of $E^{*}$." Thus the most general $2$-form in $\mathbb{R}^{3}$ is of the form 
$$
\beta^{2} = \sum\limits_{i<j} b_{ij}dx^{i} \wedge dx^{j} = b_{23}dx^{2} \wedge dx^{3} + b_{31}dx^{3}\wedge dx^{1} + b_{12}dx^{1} \wedge dx^{2}
$$
We shall see in a moment why we prefer this expression. (See problem 2.5(2) in the textbook for more. 

##### The Geometric Meaning of Forms in $\mathbb{R}^{n}$ 
Let us look at the geometric meaning of exterior forms in $E=\mathbb{R}^{n}$ in the _special case when the coordinates are cartesian_; that is, we shall employ the Euclidean metric of $\mathbb{R}^{n}$. The coordinate vectors $\{\partial_{i}\}$ form an orthogonal basis of $E$, with dual basis $\{dx^{i}\}$ for $E^{*}$. We already know that for these 1-forms $dx^{i}(\mathbf{v})=v^{i}$, that is, $dx^{i}$ _reads off the i-th components of $\mathbf{v}$_. Next,
$$
dx^{i} \wedge dx^{j}(\mathbf{v},\mathbf{w}) = dx^{i}(\mathbf{v})dx^{j}(\mathbf{w})- dx^{j}(\mathbf{v})dx^{i}(\mathbf{w})
$$
$$
= \begin{vmatrix} v^{i} & w^{i}\\ v^{j}& w^{j} \end{vmatrix}
$$
$= \pm$ the area of the parallelogram spanned by the projections $\pi(\mathbf{v}),\pi(\mathbf{w})$ of the vectors $\mathbf{v},\mathbf{w}$ into the $x^{i}x^{j}$ plane; the $+$ sign is used if these projections determine the same orientation of the plane as do $\partial_{i}$ and $\partial_{j}$. (We shall discuss the notion of orientation more thoroughly later on.)

![[Pasted image 20240319224542.png|center]]

In the figure above, $dx \wedge dy(\mathbf{v},\mathbf{w})$ is the negative of the area of the parallelogram spanned by $\pi(\mathbf{v})$ and $\pi(\mathbf{w})$. Likewise, from (2.47),
$$
dx^{i_{1}}\wedge \ldots \wedge dx^{i_{p}}(\mathbf{v}_{1},\ldots,\mathbf{v}_{p})
$$
$= \pm$ the $p$-dimensional volume of the parallelopiped spanned by the projections of these vectors into the $x^{i_{1}}\ldots x^{i_{p}}$ coordinate plane; the $+$ sign is used only if these projected vectors define the same orientation as does $\partial_{i_{1}},\ldots,\partial_{i_{p}}$. 

##### Special Cases of the Exterior Product
Let $\tau^{1},\ldots,\tau^{n}$ be any $n$-tuple of $1$-forms, and expand each in terms of a basis (we are not assuming any scalar product)
$$
\tau ^{i} = {T^{i}}_{j}\sigma^{j}
$$
**Remark.**  Note that $\tau$ is a 1-form, so each $\tau^{i}$ is the linear combination of the dual basis and some scalars (which we can confine into a tensor).

Then $\tau^{1}\wedge \ldots \wedge \tau^{n} = \sum\limits_{J}{T^{1}}_{j_{1}}\ldots {T^{n}}_{j_{n}} \sigma^{j_{1}}\wedge \ldots \wedge \sigma^{j_{n}}$
$$
= \sum\limits_{J}{T^{1}}_{j_{1}}\ldots {T^{n}}_{j_{n}} \delta_{12\ldots n}^{j_{1}\ldots j_{n}} \sigma^{{1}}\wedge \ldots \wedge \sigma^{{n}}
$$
that is,
$$
\tag{2.51}
\tau^{1} \wedge \ldots \wedge \tau^{n} = (\det T)\sigma^{1} \wedge \ldots \wedge \sigma^{n}
$$
_Exterior products yields a coordinate-free expression for the determinant!_ For this reason the wedge product is very convenient for discussing linear dependence. 

**Theorem (2.52):**  The $p$ 1-forms $\tau^{1},\ldots, \tau^{p}$ are linearly dependent **iff**
$$
\tau^{1}\wedge \ldots \wedge \tau^{p} = 0
$$
**Proof:**  If $\tau^{r} = \sum\limits_{i\neq r} a_{i}\tau^{i}$ then $\tau^{1}\wedge \ldots \wedge \tau^{r} \wedge \ldots \wedge \tau^{p}$ will be a sum of terms, each having a repeated $\tau^{i}$, and so the product will vanish. On the other hand, if the $\tau$'s are linearly independent we may complete them to a basis $\tau^{1},\ldots,\tau^{n}$. Let $\mathbf{f}_{1},\ldots,\mathbf{f}_{n}$ be the dual basis. From (2.47) we have $\tau^{1} \wedge \ldots \wedge \tau^{p} \wedge \ldots \wedge \tau^{n}(\mathbf{f}_{1},\ldots,\mathbf{f}_{n})=1$, showing that $\tau^{1} \wedge \ldots \wedge \tau^{p} \neq 0$. $\square$  

---
##### Computations and Vector Analysis
For computations using forms we may use the usual rules of arithmetic except that the commutative law is replaced by (2.44). In particular, $dx \wedge dy = -dy \wedge dx$ and $dx \wedge dx = 0$. Consider $\mathbb{R}^{3}$ as a $3$-manifold with _any_ (perhaps curvilinear) coordinate system $x^{1},x^{2},x^{3}$. Let $f$ be a $0$-form, that is, a function of $x$, and let $a_{i},b_{i}$, and $c_{ij}$ be functions. Then 
$$
\alpha^{1} = a_{1}dx^{1} + a_{2}dx^{2} + a_{3}dx^{3} \quad \text{and} \quad \beta^{1} = b_{1}dx^{1}+b_{2}dx^{2}+b_{3}dx^{3}
$$
are $1$-forms 
$$
\gamma^{2} = c_{23} dx^{2} \wedge dx^{3} + c_{31} dx^{3} \wedge dx^{1} + c_{12}dx^{1} \wedge dx^{2} 
$$
$$
\equiv c_{1}dx^{2}\wedge dx^{3} + c_{2}dx^{3}\wedge dx^{1}+ c_{3}dx^{1}\wedge dx^{2}
$$
is a 2-form. Note that the indices of $c_{31}$ was switched along with the wedge thereafter to make an equivalent expression. Now, note that 
$$
w^{2} = dx^{1} \wedge dx^{2}\wedge dx^{3}
$$
is a $3$-form. (In cartesian coordinates $w^{3}$ is the "volume form," but note that, for example, in spherical coordinates $r^{2}\sin \theta dr \wedge d \theta \wedge d \phi$ is the volume form; these matters will be discussed later.) As we shall see, these are familiar expressions used in vector analysis _in the case when the coordinates are cartesian_, involving line, surface, and volume integrals, where they are usually written, for example, as $\alpha = \mathbf{a} \cdot d \mathbf{x}$ and $\gamma = \mathbf{c} \cdot d \mathbf{S}$, and $w = dV$. We then have
$$
\alpha^{1} \wedge \beta^{1} = (a_{1}dx^{1} + a_{2}dx^{2} + a_{3}dx^{3}) \wedge (b_{1}dx^{1}+b_{2}dx^{2}+b_{3}dx^{3})
$$
$$
a_{1}b_{1}dx^{1} \wedge dx^{1} + \ldots + a_{2}b_{3}dx^{2} \wedge dx^{3} + \ldots + a_{3}b_{2}dx^{3} \wedge dx^{2}
$$
$$
= 0 + \ldots + (a_{2}b_{3}-a_{3}b_{2})dx^{2} \wedge dx^{3}
$$
$$
=(a_{2}b_{3}-a_{3}b_{2})dx^{2} \wedge dx^{3} + (a_{3}b_{1}-a_{1}b_{3})dx^{3}\wedge dx^{1}
$$
In _cartesian coordinates_ this says 
$$
(\mathbf{a \cdot} d \mathbf{x}) \wedge (\mathbf{b} \cdot d \mathbf{x}) = (\mathbf{a} \times \mathbf{b}) \cdot d \mathbf{S}
$$
but note that the three components of $\alpha \wedge \beta$, which makes sense in any coordinate system, are _not the components of the cross product in curvilinear coordinates_! The exterior product replaces the notion of $\times$ product (which is not associative; $\mathbf{i} \times (\mathbf{i \times j}) \neq (\mathbf{i \times i}) \times \mathbf{j}$. We shall see the exact correspondence between exterior forms and vector analysis later on. 

### Exterior Differentiation 

Does one _ever_ need to write out $curl \ \mathbf{A}$ in curvilinear coordinates?

---
##### The Exterior Differential 
Before (in [[#Tensor Fields on Manifolds]]), we say that if $A = A_{i}(x)dx^{i}$ is a covariant vector field on a manifold, that is, a 1-form, then $F_{ij} = \partial_{i}A_{j}-\partial_{j}A_{i}$ are the components of a covariant second-order tensor that is clearly skew symmetric. Thus,
$$
F \equiv  \sum\limits_{i<j}(\partial_{i}A_{j}-\partial_{j}A_{i})dx^{i} \wedge dx^{j}
$$
is an exterior 2-form. We then have a way of "differentiating" a $1$-form, obtaining a 2-form. We also showed that the expressions $\{\partial_{i}A_{j}\}$ themselves _do not_ form the components of a tensor. And Problem 2.4(3) indicated that it does not seem to be possible to differentiate a _contravariant_ vector field and obtain a tensor field. In this section we shall define a differential operator $d$ that will always take exterior $p$-form fields into exterior $(p+1)$-form fields. In a sense, _covariant skew symmetric tensors have a richer structure than tensors in general_, and this richer structure plays an essential role in physics. 

Recall that if $f$ is a function, that is, a 0-form, then its differential $df = (\partial_{i}f)dx^{i}$ is a 1-form. Also, equation (2.44) says that $\alpha^{0} \wedge \beta^{p} = \beta^{p} \wedge \alpha^{0}$. For this reason _one does not ordinarily put a wedge $\wedge$ in a product involving a $0$-form_. 

**Theorem (2.53):**  There is a unique operator, _exterior differentiation_, 
$$
d: \bigwedge^{p}M^{n}\rightarrow \bigwedge^{p+1}M^{n}
$$
satisfying 
1. $d$ is additive, $d(\alpha+\beta)=d \alpha + d \beta$.
2. $d \alpha^{0}$ is the usual differential of the function $\alpha^{0}$.
3. $d(\alpha^{p}\wedge \beta^{q})=d \alpha^{p} \wedge \beta^{q} + (-1)^{p}\alpha^{p} \wedge d \beta^{q}$.
4. $d^{2}\alpha \equiv d(d \alpha)=0$, for all forms $\alpha$.

**Proof:**  We shall first define an operator $d$, using a local coordinate system $x$, and then show that this operator is in fact independent of the coordinate system. _Step 1_. If $f$ is a 0-form, define $d_{x}f=df=(\partial_{i}f)dx^{i}$. We know in fact that $df$ is independent of coordinates: Its coordinate free definition is $df(\mathbf{v})=\mathbf{v}(f)$. Thus, condition 2 has been satisfied.

_Step 2_. If $a$ is a function, define, for $I=(i_{1},\ldots,i_{p})$
$$
d_{x}[a(x)dx^{I}] = da \wedge dx^{I} = (\partial_{j}a)dx^{j} \wedge dx^{I}
$$
We then define $d_{x}$ on any $p$-form in the coordinate patch $x$ by additivity
$$
d_{x}\sum\limits_{\underset{\rightarrow}I}a_{I}(x) dx^{I} = \sum\limits_{\underset{\rightarrow}I}da_{I} \wedge dx^{I} 
$$
Condition 1 is automatically satisfied. Consider condition 3. Let $J = (j_{1} ,\ldots,j_{q})$. Then 
$$
d_{x}\left[\sum\limits_{\underset{\rightarrow}I}a_{I} dx^{I} \wedge \sum\limits_{\underset{\rightarrow}J}b_{J} dx^{J} \right] = d_{x}\sum\limits_{\underset{\rightarrow}I \underset{\rightarrow}J}a_{I}b_{J} dx^{I} \wedge dx^{J}
$$
$$
= \sum\limits_{\underset{\rightarrow}I \underset{\rightarrow}J}(da_{I}b_{J}+a_{I}db_{J})\wedge dx^{I} \wedge dx^{J}
$$
$$
=\sum\limits_{\underset{\rightarrow}I } da_{I} \wedge dx^{I} \wedge \sum\limits_{\underset{\rightarrow}J} b_{J}dx^{J} + \sum\limits_{\underset{\rightarrow}I } a_{I} dx^{I} \wedge \sum\limits_{\underset{\rightarrow}J} (-1)^{p}db_{J}\wedge dx^{J}
$$
since $db_{J} \wedge dx^{I} = (-1)^{p}dx^{I} \wedge db_{J}$ involved $p$ interchanges. Thus 3 is satisfied. To verify 4, note that if $f$ is a function, then 
$$
d_{x}(d_{x}(f)) = d_{x} \sum\limits_{i}(\partial_{i}f)dx^{i} = \sum\limits_{i} d_{x}(\partial_{i}f) \wedge dx^{i} = \sum\limits_{ij}(\partial^{2}_{ij} f)dx^{j} \wedge dx^{i}
$$
$$
=\ldots + \left(\frac{\partial^{2}f}{\partial x^{r} \partial x^{s}}\right)dx^{r} \wedge dx^{s} \ldots + \left(\frac{\partial^{2}f}{\partial x^{s} \partial x^{r}}\right)dx^{s} \wedge dx^{r} + \ldots = 0
$$
(It is a general and very useful fact that if $A^{\ldots i \ldots j \ldots}_{\ldots r \ldots s \ldots }$ is symmetric in $i,j$, and skew symmetric in $r,s$ then the contraction $A^{\ldots i \ldots j \ldots}_{\ldots i \ldots j \ldots} = 0$.)

Then from (3), for _any_ functions $f,g$, not simply for coordinate functions, we have 
$$
d_{x}(df \wedge dg) = 0
$$
and by induction 
$$
\tag{2.54}
d_{x}(df \wedge dg \wedge \ldots \wedge dh) = 0
$$
Then, for any $p$-form $\alpha$
$$
d^{2}_{x} \alpha = d^{2}_{x} \sum\limits_{\underset{\rightarrow}I}a_{I}dx^{I} = d_{x} \sum\limits_{\underset{\rightarrow}I}da_{I} \wedge dx^{I} =0
$$
We have now defined an operator $d_{x}$ in each coordinate patch $x$ and it satisfies 1,2,3, and 4. Let $y$ be another coordinate patch that overlaps $x$, and let $d_{y}$ be the corresponding differential. Then, since $d_{y}$ again coincides with $d_{x}$ on functions, in particular coordinate functions, we have, from 3 and (2.54),
$$
d_{y} \sum\limits_{\underset{\rightarrow}I}a_{I}dx^{I} = \sum\limits_{\underset{\rightarrow}I}d_{y} a_{I}[x(y)]\wedge dx^{I}
$$
$$
= \sum\limits_{\underset{\rightarrow}I}da_{I}\wedge dx^{I} 
$$
$$
= d_{x}\sum\limits_{\underset{\rightarrow}I}a_{I}(x)dx^{I}
$$
Thus, $d \equiv d_{y}=d_{x}$ is well defined, independent of coordinates.

As to uniqueness, any operator $d'$ satisfying 1,2,3, and 4 must satisfy
$$
d' \sum\limits_{\underset{\rightarrow}I}a_{I}(x)dx^{I} = \sum\limits_{\underset{\rightarrow}I}da_{I}\wedge dx^{I} = d \sum\limits_{\underset{\rightarrow}I}a_{I}(x)dx^{I} \quad \square
$$

##### Examples in $\mathbb{R}^{3}$
Let $\mathbf{x}=(x,y,z)$ be _any_ (perhaps curvilinear) coordinate system in $\mathbb{R}^{3}$. Then the differential of a function $f=f^{0}$ is 
$$
df^{0} = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy  + \frac{\partial f}{\partial z} dz
$$
If the coordinates are _cartesian_, then the components are the components of the gradient of $f$, 
$$
df = \nabla f \cdot d \mathbf{x}
$$
If, in general coordinates 
$$
\alpha^{1} = a_{1}(\mathbf{x})dx + a_{2}(\mathbf{x}) dy + a_{3}(\mathbf{x}) dz
$$
then 
$$
d \alpha^{1} = da_{1} \wedge dx + da_{2} \wedge dy + da_{3} \wedge dz
$$
$$\begin{aligned}
= \left[ \left(\frac{\partial a_{1}}{\partial x}\right)dx + \left(\frac{\partial a_{1}}{\partial y}\right)dy + \left(\frac{\partial a_{1}}{\partial z}\right)dz  \right] \wedge dx \\ +
\left[ \left(\frac{\partial a_{2}}{\partial x}\right)dx + \left(\frac{\partial a_{2}}{\partial y}\right)dy + \left(\frac{\partial a_{2}}{\partial z}\right)dz  \right] \wedge dy \\
+ \left[ \left(\frac{\partial a_{3}}{\partial x}\right)dx + \left(\frac{\partial a_{3}}{\partial y}\right)dy + \left(\frac{\partial a_{3}}{\partial z}\right)dz  \right] \wedge dz
\end{aligned}
$$
$$
= (\partial_{y}a_{3}-\partial_{z}a_{2})dy \wedge dz + (\partial_{z}a_{1}-\partial_{x}a_{3})dz\wedge dx+(\partial_{x}a_{2}-\partial_{y}a_{1})dx\wedge dy
$$
In cartesian the components are the components of the curl of the vector $\mathbf{A}$, 
$$
d(\mathbf{A} \cdot d \mathbf{x}) = (Curl \ \mathbf{A}) \cdot d \mathbf{S}
$$
Finally, for a $2$-form $\beta$ (writing $b_{23}=b_{1},b_{31}=b_{2},b_{12}=b_{3}$)
$$
d \beta^{2} = d[b_{1}dy \wedge dz + b_{2} dz \wedge dx + b_{3}dx \wedge dy]
$$
$$
= db_{1} \wedge dy \wedge dz + db_{2} \wedge dz \wedge dx + db_{3} \wedge dx \wedge dy
$$
$$
 = [\partial_{x}b_{1}+ \partial_{y}b_{2} + \partial_{z}b_{3}]dx \wedge dy\wedge dz
$$
whose single component in cartesian coordinates is the divergence of the vector $\mathbf{B}$,
$$
d(\mathbf{B} \cdot d \mathbf{S}) = div \ \mathbf{B} \ dV
$$
$d^{2}=0$ in any coordinate system; in cartesian coordinates this yields the famous $curl \ grad = 0$ and $div \ curl = 0$.

It is important to realize that it is _no more difficult to compute $d$ in a curvilinear coordinate system than in a cartesian one_. For example, in spherical coordinates, for $1$-form $\alpha= Pdr+Qd \theta + R d \phi$ 
$$
d[Pdr+ Q d \theta + R d \phi] = dP \wedge dr + dQ \wedge d \theta + dR \wedge d \phi
$$
$$
= (\partial_{\theta}R-\partial_{\phi}Q)d \theta \wedge d \phi + (\partial_{\phi}P-\partial_{r}R)d \phi \wedge dr + (\partial_{r}Q- \partial_{\theta}P)dr \wedge d \theta
$$
Note that $(P,Q,R)$ form the components of a _covariant_ vector, $\alpha$, and that the three components of $d \alpha^{1}$ do **not** form the components of the curl of a vector, they are the components of a second-rank covariant skew symmetric tensor. 

We shall see later on that it is possible to identify $2$-forms in $\mathbb{R}^{3}$ (with a given metric) with contravariant vectors and then the vector identified with $d \alpha$ is the curl of the contravariant version of $\alpha$. This is not only an extremely awkward procedure, it serves no purpose, for we maintain that _there is never any reason to take the curl of a contravariant vector_. _In situations where the "curl" of a "vector" is required, the "vector" will most naturally appear in covariant form_ (i.e., it will be a $1$-form $\alpha$), and then $d \alpha$ is all that is required. 

For example, the electric field measures the force on a unit charge that is at rest. Force, being the time rate of change of momentum, appears naturally as a covector and so the electric field is a 1-form $\varepsilon^{1}$. Then Faraday's law really states that $d \varepsilon^{1}$ is the negative of the time rate of change of the magnetic field $2$-form $\mathcal{B}^{2}$. These matters will be discussed further on. 

##### A Coordinate Expression for $d$
Let $\alpha^{p}= \sum\limits_{\underset{\rightarrow}L}a_{L}dx^{L}$ be a $p$-form; then $d \alpha^{p} = \sum\limits_{\underset{\rightarrow}L}(da_{L}) \wedge dx^{L}$. Now $da_{L}$ is the $1$-form whose $j$th component is $(da_{L})_{j}= \partial_{j}a_{L}$. Also $dx^{L}$ is the $p$-form with components $(dx^{L})_{K}=\delta^{L}_{K}$. Then from (2.43) we get 
$$
(d \alpha)_{I} = \sum\limits_{\underset{\rightarrow}L} (da_{L}\wedge dx^{L})_{I} = \sum\limits_{\underset{\rightarrow}I} \sum\limits_{j,\underset{\rightarrow}K} \delta^{jK}_{I}(\partial_{j}a_{L})\delta^{L}_{K}
$$
that is,
$$
\tag{2.55}(d \alpha)_{I} = \sum\limits_{j\underset{\rightarrow}K} \delta^{jK}_{I} (\partial_{j} a_{K})
$$
Thus for $I$ increasing 
$$
(d \alpha^{P})_{\underset{\rightarrow}I} = \sum\limits_{j,\underset{\rightarrow}K} \delta^{jk_{1}\ldots k_{p}}_{i_{1}\ldots i_{p+1}} \partial_{j}a_{k_{1}\ldots k_{p}} = \partial_{i_{1}}a_{i_{2}\ldots i_{p+1}}-\partial_{i_{2}}a_{i_{1}}i_{3}\ldots i_{p+1}
+\ldots$$
Hence, 
$$
(d \alpha^{P})_{I} = \sum\limits_{r}(-1)^{r+1}\partial_{i_{r}} a_{i_{1}\ldots \widehat{i_{r}}\ldots i_{p+1}}
$$
where the hat $\widehat{\ }$ over $i_{r}$ means omit $i_{r}$. We can also write 
$$
(d \alpha^{p})_{I} = \sum\limits_{r}(-1)^{r+1}\partial_{i_{r}}[\alpha^{p}(\partial_{i_{1}},\ldots \widehat{\partial_{{i}_{r}}}\ldots \partial_{i_{p+1}})]
$$
If, for example, $\alpha= \sum_{i} a_{i}dx^{i}$ is a $1$-from on $M^{n}$, from (2.55)
$$
(d \alpha^{1})_{ij} = \partial_{i}a_{j}- \partial_{j}a_{i}
$$
and this is of course was the procedure used for defining the field strength in (2.42). If $\beta^{2} = \sum_{i<j}b_{ij}dx^{i} \wedge dx^{j}$ is a $2$-form in an $M^{n}$, from (2.56)
$$
(d \beta^{2})_{i<j<k} = (\partial_{i}b_{jk}+ \partial_{k}b_{ij} + \partial_{j}b_{ki})
$$
---
#### Pull-backs
What are the deformation tensors that arise in elasticity theory?

##### The pull-back of a Covariant Tensor
Let $F:M^{n}\rightarrow W^{r}$ be a differential map. Sometimes we shall write $M \overset{F}{\rightarrow}W$. In local coordinates $x$ for $M$ and $y$ for $W$ we have $y^{j}=F^{j}(x)$, or briefly $y=y(x)$. If $f:W \rightarrow \mathbb{R}$ is a smooth function (0-form) on $W$ we define its pull-back to $M$, written $F^{*}f$ to be the composition  $f \circ F:M \rightarrow \mathbb{R}$, that is $M \overset{F}{\rightarrow}W \overset{f}{\rightarrow} \mathbb{R}$.
$$
(F^{*}f)(x) = (f \circ F)(x) = f(y(x))
$$
This is a real-valued function on $M,M \overset{f\circ F}{\rightarrow}\mathbb{R}$. _One can always pull back a function on $W$_. If $F$ has an inverse $G=F^{-1}$ then one can "push forward" a function $h$ onto $M$ to yield a function $h \circ F^{-1}$ on $W$, $W \overset{G}{\rightarrow}M \overset{g}\rightarrow \mathbb{R}$, but it should be clear that one cannot in general expect to push forward a function on $M$ to get a function on $W$, unless $F^{-1}$ exists. 

For future needs, we exhibit here how a vector $\mathbf{v}$ at $x$ of $M$, as a differential operator, acts on the pull-back of a function.
$$
\mathbf{v}(F^{*}f) = \mathbf{v}[f\{y(x)\}] = v^{i} \frac{\partial}{\partial x^{i}}[f\{y(x)\}]
$$
$$
= v^{i}\left(\frac{\partial y^{i}}{\partial x^{i}}\right)\left(\frac{\partial f}{\partial y^{i}}\right)
$$
$$
\mathbf{v}(F^{*}f) = (F_{*}\mathbf{v})(f) = df(F_{*}\mathbf{v})
$$
Now let $\alpha^{P}$ be a _covariant tensor_ at $y$ in $W$. We have just defined the pull-back of $\alpha^{P}$ when $p=0$. When $p=1$, that is, when $\alpha$ is a $1$-form, its pullback was defined long before in [[#The Pull-Back of a Covector]]. We now define in general the **pull-back** of a covariant tensor by 
$$
\tag{2.61}
F^{*}\alpha^{P}(\mathbf{v}_{1},\ldots,\mathbf{v}_{P}) \equiv \alpha^{P}(F_{*}\mathbf{v}_{1},\ldots,F_{*}\mathbf{v}_{P}) 
$$
It is clear that $F^{*}\alpha$ is alternating if $\alpha$ is; that is, the pull-back of a $p$-form on $W$ on $M$ 
$$
F^{*}: \bigwedge^{p}W \rightarrow \bigwedge^{p}M
$$
Unless otherwise indicated, by pull-back we mean the pull-back of an **exterior form**. 

In our warning following (2.25) we pointed out that one cannot push forward a _contravariant_ vector field on $M$ to yield a vector field on $W$. The ability to pull back covariant tensors endows these tensors with a crucial operation that is not available to the contravariant ones. 

It is difficult to overemphasize the important of this advantage. 

It is also clear from (2.61) that $F^{*}$ is additive; that is, $F^{*}$ of a sum is the sum of the $F^{*}$'s. This is further enhanced by the following two properties: the pull-back of a product of forms is the product of the pull-backs, and the pull-back of the exterior derivative of a form is the derivative of the pull-back. We proceed to these matters, for they are crucial to writing down coordinate expressions economically. 

**Theorem (2.62):**  $F^{*}$ is an algebra homomorphism, that is,
$$
F^{*}(\alpha \wedge \beta) = (F^{*} \alpha) \wedge (F^{*} \beta)
$$

**Proof:**  See textbook, problem 2.7(1), using wedge product definition for proof. It is even simpler to prove that for any tensor product of covariant tensors
$$
\tag{2.63}F^{*} (\alpha \otimes \beta) = (F^{*}\alpha)\otimes(F^{*}\beta)
$$

**Theorem (2.64):**  $F^{*}$ commutes with exterior differentiation, $d \circ F^{*} = F^{*}\circ d$,
$$
F^{*}(d \alpha) = d(F^{*} \alpha)
$$
**Proof:**  When $\alpha=\alpha^{0}$ is a function $f$ on $W$ near $F(x)$ and $\mathbf{v}$ is tangent vector to $M$ at $x$, we have from before that 
$$
d(F^{*} f)(\mathbf{v}) = \mathbf{v}(F^{*}f) = df(F_{*}(\mathbf{v}) ) = (F^* (df))(\mathbf{v})
$$
Thus (2.64) has been proved when $\alpha$ is a 0-form. When $\alpha$ is a $p$-form, we have 
$$
d \circ F^{*} \sum\limits_{\underset{\rightarrow}J}a_{J}(y)dy^{j_{1}}\wedge \dots \wedge dy^{j_{p}}
$$
,which from (2.62) we can write
$$
= d \sum\limits_{\underset{\rightarrow}J}(F^{*}a_{J}(y))(F^{*}dy^{j_{1}}) \wedge \ldots \wedge (F^{*}dy^{j_{p}})
$$
(since (2.64) have been proven for 0-forms)
$$
= d \sum\limits_{\underset{\rightarrow}J}(F^{*}a_{J}(y))d(F^{*}y^{j_{1}}) \wedge \ldots \wedge d(F^{*}y^{j_{p}}) 
$$
$$
= \sum\limits_{\underset{\rightarrow}J}(dF^{*}a_{J}(y)) \wedge d(F^{*}y^{j_{1}}) \wedge \ldots \wedge d(F^{*}y^{j_{p}})
$$
![[Pasted image 20240415153904.png|center]]

as desired (too lazy to write it all out). $\square$

Explicitly, with $I = (i_{1},\ldots,i_{p})$, $F^{*}d(y^{J})=F^{*}(dy^{j_{1}}\wedge \ldots d y^{j_{p}})= \sum\limits_{I}\left(\frac{\partial y^{j_{1}}}{\partial x^{i_{1}}}\right)\ldots \left(\frac{\partial y^{j_{p}}}{\partial x^{i_{p}}}\right)dx^{I}$. But $dx^{I} = \sum\limits_{\overset{\rightarrow}L} \delta^{I}_{L} dx^{L}$ (we are merely putting the $dx$'s in increasing order; for each given $I$ there is only one nonzero term in the sum on the right). Then 
$$
F^{*}d(y^{J}) = \sum\limits_{\underset{\rightarrow}L} \left[\sum\limits_{I}\left(\frac{\partial y^{j_{1}}}{\partial x^{i_{p}}}\right) \ldots \left(\frac{\partial y^{j_{p}}}{\partial x^{i_{p}}}\right)\delta^{I}_{L} \right]
$$
$$
= \sum\limits_{\underset{\rightarrow}L} \det \left[\frac{\partial(y^{J})}{\partial (x^{L})}\right] dx^{L}
$$
Thus we have 
$$
F^{*}d(y^{J}) = \sum\limits_{\underset{\rightarrow}L} \det \left[\frac{\partial (y^{J})}{\partial (x^{L}) }\right] dx^{L}
$$
and so 
$$\tag{2.65}
F^{*}\alpha^{p} = F^{*} \sum\limits_{\underset{\rightarrow}J} a_{J}dy^{J} = \sum\limits_{\underset{\rightarrow}L} a^{*}_{L}(x)dx^{L}
$$
where 
$$
a^{*}_{L}(x) \equiv \sum\limits_{\underset{\rightarrow}J} a_{J}(y(x)) \det \left[ \frac{\partial(y^{J})}{\partial(x^{L}) } \right]
$$
Let, for example, $M^{2}$ be a surface in $\mathbb{R}^{3}$ that is a 2-dimensional submanifold. We have the **inclusion map**, $i:M \rightarrow \mathbb{R}^{3}$, which is a fancy  way of saying that any point of $M$ is also a point in $\mathbb{R}^{3}$. If $\mathbf{v}$ is a tangent vector to $M$, then $i_{*}\mathbf{v}$ is simply the same vector $\mathbf{v}$ considered as a vector in $\mathbb{R}^{3}$. If $\beta^{2}$ is a 2-form on $\mathbb{R}^{3}$, then the pull-back of $\beta$ to $M$ is the 2-form $i^{*}\beta$ whose value on the pair $\mathbf{v,w}$ of tangent vectors to $M$ is simply given by $i^{*} \beta(\mathbf{v,w})=\beta(i_{*}\mathbf{v},i_{*}\mathbf{w})= \beta(\mathbf{v,w})$. In other words, $i^{*}\beta$ in this case of inclusion is the **same form $\beta$, but we restrict its domain to vectors that are tangent to $M$.** This same situation holds whenever $M^{n}$ is a submanifold of another manifold. If $\mathbf{u}=(u,v)$ are local coordinates in $M^{2}$ and $\mathbf{x}=(x,y,z)$ are coordinates for $\mathbb{R}^{3}$, then 
$$
i^{*}\beta = i^{*}[b_{1}(\mathbf{x})dy \wedge dz + b_{2}(\mathbf{x})dz \wedge dx+b_{3}(\mathbf{x})dx \wedge dy]
$$
$$
= \left[b_{1}\left(\mathbf{x}(\mathbf{u}) \right) \frac{\partial (y,z)}{\partial (u,v)} + b_{2}\left(\mathbf{x}(\mathbf{u}) \right) \frac{\partial (z,x)}{\partial (u,v)} + b_{3}\left(\mathbf{x}(\mathbf{u}) \right) \frac{\partial (x,y)}{\partial (u,v)}\right] du \wedge dv
$$

See problem 2.7(2) in the textbook at this time to see that this 2-form is given by $\mathbf{b}\cdot \mathbf{n} du \wedge dv$ where $\mathbf{n}$ is a nonunit normal to $M$ and $\mathbf{b}$ is from $\beta$ being of the form $\mathbf{b \cdot } d \mathbf{S}$ in $\mathbb{R}^{3}$. 

Another way to get this coordinate expression for $i^* \beta$ is to compute directly, using the fact that $i^{*}$ commutes with exterior products and differentiation. For example, putting $\mathbf{x}=(x,y,z)$ and $\mathbf{u}=(u,v)$ 
$$
i^{*}(b_{1}dy \wedge dz) = b_{1}(\mathbf{x}(\mathbf{u}))i^{*}(dy) \wedge i^{*}(dz)
$$
$$
= b_{1}(\mathbf{x}(\mathbf{u}))\left[\left(\frac{\partial y}{\partial u} \right) du + \left(\frac{\partial y}{\partial v} \right) dv \right] \wedge \left[\left(\frac{\partial z}{\partial u} \right) du + \left(\frac{\partial z}{\partial v} \right) dv \right] 
$$
$$
= b_{1}(\mathbf{x}(\mathbf{u}) ) \left[\left(\frac{\partial y}{\partial u}\right) \left(\frac{\partial z}{\partial v}\right) - \left(\frac{\partial y}{\partial v}\right) \left(\frac{\partial z}{\partial u}\right)  \right] du \wedge dv
$$
Two final remarks. First, if $F:M^{n}\rightarrow M^{n}$ is the _identity map_ but expressed in different coordinates, that is, if $y=y(x)$ is simply a change of coordinates, then $\alpha=F^{*}\alpha$ is simply expressing the form $\alpha$ in the two coordinate systems. For example, if $u,v,w$ are curvilinear coordinates in $\mathbb{R}^{3}$ then from either (2.65) or (2.51) we see 
$$
dx \wedge dy \wedge dz = \left[ \frac{\partial (x,y,z)}{\partial (u,v,w)} \right] du \wedge dv \wedge dw
$$
Finally, we have defined the Poincare 1-form $\lambda = p_{i}dq^{i}$ in phase space $T^{*}M^{n}$. We then define the Poincare 2-form by 
$$
\omega^{2} = d \lambda = dp_{i} \wedge dq^{i}
$$
This form, as we shall see, plays a most important role in Hamiltonian mechanics. If $F:\mathbb{R}^{2} \rightarrow T^* M^{n}$ is a 2-dimensional surface in phase space, then the pull back of $\omega$ to $\mathbb{R}^{2}$ (whose coordinates are $u,v$) is the 2-form 
$$
F^{* \omega}= \{u,v\}du \wedge dv
$$
where 
$$
\{u,v\} \equiv  \sum\limits_{i} \frac{ \partial (p_{i},q^{i})}{\partial (u,v)}
$$
defined the **Lagrange bracket** of the functions $u$ and $v$. 

##### The Pull-Back in Elasticity
Consider an elastic body $\mathcal{B}$ in $\mathbb{R}^{3}$ are a deformation $\mathcal{B}' = F(\mathcal{B})$ of this body. To describe this we shall let $X_{1},X_{2},X_{3}$ be cartesian coordinates in $\mathbb{R^{3}}$ and the deformation will be described by function $x^{i} = x^{i}(X)$. We may think of $X$ and $x$ as being two identical Cartesian coordinate systems in $\mathbb{R}^{3}$. A point with coordinates $X$ in $\mathcal{B}$ will be sent into the point with coordinates $x$ in $\mathcal{B}'$. We shall try to follow a common practice of denoting quantities with the undeformed body by capital letters, ad those of deformed body with lower case. 

![[Pasted image 20240417172312.png|center]]

Under the deformation, the orthonormal pair $\partial_{A},\partial_B$ at $X$ is sent, by the differential of $F$ at $X$, into a pair of vectors $F_{*}\partial_{A}, F_{*}\partial_{B}$ at $x$. 

The metric tensor of $\mathbb{R}^{3}$ can be written as $dS^{2} = G_{AB}dX^{A} \otimes dX^{B}$, meaning $dS^{2}(\mathbf{V},\mathbf{W}) =G_{AB}V^{A}W^{B}$. _Note that it is traditional to omit the tensor product sign $\otimes$ when dealing with symmetric tensors_. Thus at $X$, since the coordinates are cartesian, 
$$
dS^{2} = G_{AB} dX^{A}dX^{B} = \delta_{AB} dX^{A}dX^{B}= \sum\limits_{A} (dX^{A})^{2}
$$
and this is the usual expression for "arc length" in elementary calculus, $ds^{2}=dx^{2}+dy^{2}+dz^{2}$. This will be discussed at great length later in Part 2. 

We may also write this _same tensor_, at the point $x$, as $ds^{2}= \sum\limits_{a}(dx^{a})^{2}$. For the pull-back under $F$ we have, from (2.63),
$$
F^{*}(ds^{2}) = \sum\limits_{a} \left[ \sum\limits_{A} \left( \frac{\partial x^{a}}{\partial X^{A}}\right)dX^{A} \right] \otimes  \left[\sum\limits_{B} \left( \frac{\partial x^{a}}{\partial X^{B}}\right)dX^{B} \right]
$$
$$
= \sum\limits_{aAB}  \left( \frac{\partial x^{a}}{\partial X^{A}} \right)\left( \frac{\partial x^{a}}{\partial X^{B}} \right) dX^{A}dX^{B}
$$
This tensor, 
$$
F^{*}(ds^{2}) = \sum\limits_{AB} \left( \frac{\partial \mathbf{x}}{\partial X^{A}}\right) \cdot  \left( \frac{\partial \mathbf{x}}{\partial X^{B}}\right)dX^{A}dX^{B}
$$
when applied to the pair $\partial_{C},\partial_{D}$ reads off the scalar product of the pair $F_{*}\partial_{C},F_{*}\partial_{D}$, and is called the **right Cauchy-Green tensor** $C$
$$
C \equiv F^{*}(ds^{2})
$$

```ad-note
If you are wondering why we didn't simply use the transformation of coordinates with the metric tensor and why we are even dealing with this pull-back here, let me explain. Coordinate transformations are how a tensor transforms on the **SAME MANIFOLD** but with a different coorrdinate patch on the defined atlas. 

Now, with the deformation, we are dealing with **TWO DIFFERENT MANIFOLDS**. Thus, we need to use the mapping between them. Understand this concept well before moving onward. 
```

One measure of the deformation taking place is given by the **Lagrange deformation tensor** 
$$
\frac{1}{2}[F^{*}(ds^{2})-dS^{2}] = \frac{1}{2} \left[ \sum\limits_{AB} \left( \frac{\partial \mathbf{x}}{\partial X^{A}}\right)  \cdot  \left( \frac{\partial \mathbf{x}}{\partial X^{B}}\right) - \delta_{AB}\right] dX^{A}dX^{B}
$$
A more general discussion of deformations in continuum mechanics will be found in the Appendix to the textbook. 

#### Orientations and Pseudoforms 
Let $\mathbf{e}=(\mathbf{e}_{1},\ldots, \mathbf{e}_{n})$ and $\mathbf{f} = (\mathbf{f}_{1},\ldots,\mathbf{f}_{n})$ be two bases of a vector space $E$; we can then write $\mathbf{f}=\mathbf{e}P$, that is, $\mathbf{f}_{i} = \mathbf{e}_{j}{P^{j}}_{i}$, for a unique nonsingular matrix $P$. We say that $\mathbf{e}$ and $\mathbf{f}$ have the same (resp. opposite) **orientation** if $\det P$ is positive (resp. negative.) It is easy to see, from the  continuity of the function $P \rightarrow \det (P)$, that if a basis $\mathbf{e}$ is continuously deformed into a basis $\mathbf{f}$ _while remaining a basis at each stage_, then both bases have the same orientation. 

```ad-note
If the determinant of a linear transform is positive, is preserved orientation. If the determinant is negative, the orientation is opposite of its original. Remember that the determinant has to do with the change in the volume coordinate grids of a vector space, or the linear transformation acting on the coordinate basis itself. Watch 3red2blue for better information. 
```

The collection of all bases of $E$ then falls naturally into two equivalence classes of bases. (For example, the tangent space to our physical 3-space at a given point is a 3-dimensional vector space, and we have the two classes of bases defined by using either the right- or left- hand rule.) We **orient** a vector space by declaring one of the two classes of bases to be positive; the other class then consists of negatively oriented bases. 

In our 2-space it is usual to declare the right-handed bases to be positively oriented, but we could just as well have the left-handed bases as positive. It should be clear that except for our prejudices about right and left, neither choice is any more "natural" than the other. This is especially clear if we consider a 2-dimensional case instead. If we draw a "positive" basis for a sheet of paper by using an $xy$ coordinate system where, as is usual, we rotate through a right angle counterclockwise from $x$ to $y$, then if we view the sheet of paper from the reverse side we see that this basis requires us to rotate clockwise from $x$ to $y$. 

To orient a 2-dimensional vector space is to declare one of the two possible senses of rotation about the origin to be positive. Given an oriented plane and a positively oriented basis $\mathbf{e}_{1},\mathbf{e}_{2}$, the positive sense of rotation goes from the first basis vector to the second through the unique angle that is less than a straight angle. 
$\mathbb{R}^{n}$, as a space of $n$-tuples, comes equipped with a natural basis $\mathbf{e}_{1} = (1,0,\ldots,0)^{T}$, and so on, but it is important to realize that most vector spaces we shall encounter do not have distinguished bases and consequently do not have a _natural_ choice of orientation.

##### Orientation of a Manifold 
Now consider a manifold $M^{n}$. Of course we may orient each tangent space $M_{x}^{n}$ haphazardly, but for many purposes, it would help if we could do this in a "continuous" or "coherent" fashion. For example, let $U_{x}$ be a coordinate patch with coordinates $x$. Then we may orient each tangent space at each point of $U_{x}$ by declaring the bases $\partial = (\partial_{1} ,\ldots,\partial_{n})$ to be positively oriented. We have then oriented all the tangent spaces at all points of the patch $U_{x}$. If a point lies in an overlap $U_{x} \cap U_{y}$ of two patches, the two bases are related by $\partial_{y} = \partial_{x}\left(\frac{\partial x}{\partial y}\right)$, and thus the two orientations agree if and only if the Jacobian determinant is positive. 

We shall say that a manifold $M^{n}$ is **orientable** if we can cover $M$ by coordinate patches having positive Jacobians in each overlap. We can then declare the given coordinate bases to be positively orientated, and we then say that we have **oriented** the manifold. Briefly speaking, _if a manifold is orientable it is then possible to pick out, in a continuous fashion, an orientation for each tangent space $M^{n}_{x}$ to $M^{n}$_. Conversely, if it is possible to pick out continuously an orientation in each tangent space, we can (by permuting $x_{1}$ and $x_{2}$ if necessary) assume that the coordinate frames in each coordinate patch have the chosen orientation and $M^{n}$ must be orientable. 

It should be clear that if $M$ is connected and orientable, then there are exactly two different ways to orient it. Of course if $M$ can be covered by a single coordinate patch it is then orientable. Mobius discovered that there are manifolds that are not orientable and we shall consider this in a moment. 

Let $p$ and $q$ be two points of a manifold $M^{n}$. Let $C$ be any curve joining these two points, $p=C(0)$ and $q=C(1)$. Given a frame $\mathbf{e}(0)$ at $C(0)$ we can extend this frame, in many ways, to yield a frame $\mathbf{e}(t)$ at $C(t)$ for all $0 \leq t \leq 1$ such that the assignment $t \rightarrow \mathbf{e}_{i}(t)$ is continuous(we do _not_ ask that $\mathbf{e}(t_{1})=\mathbf{e}(t_{2})$ whenever $C(t_{1})=C(t_{2})$). For example, if $C(t)$ lies in a coordinate patch $U_{x}$ for $0 \leq t \leq a$, we can insist that the components of the fields $\mathbf{e}_{i}(t)$ with respect to the coordinate basis $\partial$ be constant
