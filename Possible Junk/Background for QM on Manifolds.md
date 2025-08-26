---
tags: 
dg-publish: true
mathLink: 
---
These excerpts will provide context and insight into the development of Quantum Mechanics on Manifolds. Sections are provided and can be skipped depending on the level of context needed for understanding. Many mathematical conditions are omitted for a focus on the intuition. Skip to "mechanics on the manifold" if no background is needed. All work in the section of "Developing QM on the Manifold" is mine. Please do not distribute without permission (especially since I haven't uploaded this new work to arxiv yet).
### Intuition of a Manifold and Vectors 
Let us begin with a classical mechanics example: a free particle in a 1 dimensional space. Of course, this particle has the kinetic energy of $\frac{1}{2}mv^{2}$, where $m$ is the mass and $v$ is the speed (magnitude of the velocity $\mathbf{v}$). Thus, if we wanted to express the Lagrangian, we would write
$$
L := T-V = \frac{1}{2}m \dot{x}^{2}
$$
where we now consider $x(t)$, the position of the particle at a specific time $t$. Clearly, if we had an arbitrary number of dimensions, we would simply use traditional vector calculus to express the square $v^{2} = \sum_{i} \dot{x_{i}}^{2}$ for arbitrary coordinates $\{x_{i}\}$. But I now ask a very interesting question: what if we have some constrained trajectory in $\mathbb{R}^{n}$? How do we model such a behavior? Well, one may say that we should just solve for $x_{i}(t)$ in each dimension of $\mathbb{R}^{n}$ or whatever coordinate system we are working in and call it a day. While this seems to be the most straightforward answer, it leaves out one crucial detail: the local coordinates of the system's observer. (We will come back to this example of a free particle in "mechanics on the manifold")

But you may ask, is this detail important anyways? Well, let me give an example that we all know: Earth. Earth is a curved surface, and yet we have designed our model of the world using flat coordinate systems. But you must recognize, this is on the local scale; local in the sense that we are on length scales that cannot easily detect curvature, especially not with respect to most experimentation. But what if we had a system that traversed a region on Earth so massive that curvature was relevant? 

Should we consider Earth to be a subset of $\mathbb{R}^{3}$ and then try to model everything we do in terms of a more general coordinate system where Earth is not the reference frame as suggested before? Most definitely not! This would be absurd, and we lose all sense of the local coordinate perspective we already use. So what do we do?

We consider the concept of a "manifold." While we may not explicitly define it here, we will describe its intuition which will be sufficient enough. We want a space, that is indeed a subset of $\mathbb{R}^{n}$ that can have curvature, but locally, is $\mathbb{R}$, such that we can use local coordinates or global coordinates that account for curvature. Thus, we can have global or local mechanics depending on the observer's perspective of the space. We easily see that Earth is a manifold in the sense that it is a "sphere" $S^{2}$ embedded in $\mathbb{R}^{3}$ but locally (to an observer on the surface) seems to be $\mathbb{R}^{3}$. 

We must also consider that on this manifold, we could use many (possibly infinitely) different coordinate systems. We call the collection of all coordinate systems the Atlas, and we refer to each coordinate system as a coordinate representation of the manifold denoted $(M,x)$ for coordinate system $x$. These are also referred to as "coordinate patches." Self evidently, there may be places on the manifold that can be described by more than one coordinate system. Thus, for two subsets of the manifold, say $U\subseteq \mathcal{M}$ and $V \subseteq \mathcal{M}$, we have some "overlap function" $x_{V}(x_{U})$ that relates the sets of coordinates for some point $p \in U \cap V$. We also must quickly discuss what a differentiable manifold is. A differentiable manifold is a manifold such that for any coordinate system $(\mathcal{M},x)$, a function $F(x)$ on the manifold is differentiable. Of course, we see this condition as needing a "smooth" surface on the manifold. 

Now, we have all the machinery to begin defining what a "vector" is on the manifold. 

We motivate the definition of vector as follows. Let $p=p(t)$ be a curve lying on the manifold $M$; thus $p$ is a map of some interval on $\mathbb{R}$ into $M$. In a coordinate system $(U,x_{U})$ about the point $p_{0}=p(0)$ the curve will be described by $n$ functions $X_{U}^{i}=x_{U}^{i}(t)$, which will be assumed differentiable. The "velocity vector" $\dot{p(0)}$ was classically described by the $n$-tuple of real numbers $\frac{dx_{U}^{1}}{dt} \vert_{0}\ldots,\frac{dx_{U}^{n}}{dt}\vert_{0}$. If $p_{0}$ also lies in the coordinate patch $(V,x_{V})$, then this same velocity vector is described by another $n$-tuple $\frac{dx_{V}^{1}}{dt}\vert_{0},\ldots,\frac{dx_{V}^{N}}{dt}\vert_{0}$, related to the first set by the chain rule applies to the overlap functions, $x_{V}=x_{V}(x_{U})$, 
$$
\left. \frac{dx_{V}^{i}}{dt} \right\rvert_{0} = \sum\limits_{j=1}^{n}\left(\frac{\partial x_{V}^{i}}{\partial x_{U}^{j}}\right) (p_{0}) \left(\frac{d x_{U}^{j}}{dt}\right)_{0}
$$
We now use this to give the definition:
```ad-Definition
A **tangent vector**, or **contravariant vector** or simply a **vector** at $p_{0}\in M^{n}$, call it $\pmb{X}$, assigns to each coordinate patch $(U,x)$ holding $p_{0}$, an $n$-tuple of real numbers 
$$
(X_{U}^{i}) = (X_{U}^{1},\ldots,X_{U}^{n}) 
$$
such that if $p_{0}\in U \cap V$, then 
$$
\tag{1.6}
X_{V}^{i} = \sum\limits_{j}\left[\frac{\partial x_{V}^{i}}{\partial x_{U}^{j}} (p_{0}) \right] X_{U}^{j}
$$
If we let $X_{U}=(X_{U}^{1},\ldots,X_{U}^{n})^{T}$ be the column vector "components" of $\pmb{X}$, we can write this as a matrix equation 
$$\tag{1.7}
X_{V}=c_{VU}X_{U}
$$
where the **transition function** $c_{VU}$ is the $n\times n$ Jacobian matrix evaluated at the point in question. 
```

**Remark.**  These assumptions about overlap functions to derive the vector transformation law implies informational equivalence in coordinate patches. If a vector does not follow this transform then whatever is being done with it is not informationally equivalent in different patches.

#### Basis Vectors as Derivatives 
In Euclidean space an important role is played by the notion of differentiating a function $f$ with respect to a vector at the point $p$ 
$$
D_{v}(f) = \frac{d}{dt}[f(p+t \pmb{v})]_{t=0}
$$
and if $(x)$ is any cartesian coordinate system we have 
$$
D_{v}(f) = \sum\limits_{j}\left[ \frac{\partial f}{\partial x^{j}} \right](p)v^{j}
$$
This is the motivation for a similar operation on functions on any manifold $M$. A real-valued function $f$ defined on $M$ near $p$ can be described in a local coordinate system $x$ in the form $f=f(x^{1},\ldots,x^{n})$. If $\pmb{X}$ is a vector at $p$ we define the derivative of $f$ with respect to the vector $\pmb{X}$ by 
$$\tag{1}
\pmb{X}_{p}(f) \equiv D_{\pmb{X}}(f) \equiv \sum\limits_{j}\left[ \frac{\partial f}{\partial x^{j}}\right](p) X^{j}
$$
This seems to depend on the coordinates used, although it should be apparent from that this is not the case in $\mathbb{R}^{n}$. We must show that the expression above defines an operation that is independent of the local coordinates used. Let $(U,x_{U})$ and $(V,x_{V})$ be two coordinate systems. From the chain rule we see that 
$$
D_{\pmb{X}}^{V}(f) = \sum\limits_{j}\left(\frac{\partial f}{\partial x_{V}^{j}}\right)X_{V}^{j} = \sum\limits_{j}\left( \frac{\partial f}{\partial x_{V}^{j}}\right) \sum\limits_{i} \left( \frac{\partial x_{V}^{j}}{\partial x_{U}^{i}}\right)X_{U}^{i}
$$
$$
 = \sum\limits_{i}\left( \frac{\partial f}{\partial x_{U}^{i}}\right)X_{u}^{i} = D_{\pmb{X}}^{U}(f)
$$
This illustrates a basic point. _Whenever we define something by use of local coordinates, if we wish the definition to have intrinsic significance we must check that it has the same meaning in all coordinate systems_. 

Note then that there is a 1-1 correspondence between tangent vectors $\pmb{X}$ to $M^{n}$ at $p$ and first-order differential operators (on differentiable functions defined near $p$) that take the special form 
$$
\tag{2}
\pmb{X}_{p} = \sum\limits_{j} X^{j} \left.\frac{\partial}{\partial x^{j}} \right\vert_{p}
$$
in a local coordinate system $(x)$. From now on, we shall make no distinction between a vector and its associated differential operator. Each one of the $n$ operators $\frac{\partial}{\partial x^{i}}$ then defines a vector, written $\frac{\pmb{\partial}}{\pmb{\partial} x^{\alpha}}$, at each $p$ in the coordinate patch. If we consider a curve parametrized by $\mathbf{r}(y_{1},\ldots,y^{n})$ and compare the vector on the manifold with how we would deal with vectors traditionally, we see that 
$$
\frac{\pmb{\partial}}{\pmb{\partial} x^{j}} = \frac{\partial \pmb{r}}{\partial x^{j}} = \left( \frac{\partial y^{1}}{\partial x^{j}},\ldots, \frac{\partial y^{N}}{\partial x^{j}}\right).
$$

#### Tangent Spaces
It is evident from our definition of a **tangent vector** (at the beginning of this subsection) that the sum of two vectors at a point, defined in terms of their $n$-tuples, is again a vector at that point, and that the product of a vector by a scalar, that is, a real number, is again a vector. 

```ad-Definition
The **tangent space** to $M^{n}$ at the point $p \in M^{n}$, writen $M_{p}^{n}$, is the real vector space consisting of all tangent vectors to $M^{n}$ at $p$. If $(x)$ is a coordinate system holding $p$, then the $n$ vectors 
$$
\left. \frac{\pmb{\partial}}{\pmb{\partial} x^{1}} \right\vert_{p} ,\ldots, \left. \frac{\pmb{\partial}}{\pmb{\partial} x^{n}} \right\vert_{p}
$$
for a basis of this $n$-dimensional vector space (as is evident from (2)) and this basis is called a **coordinate basis** or **coordinate frame**. 
```

As an example, let us look at:\

![[Pasted image 20231024171156.png|center]]



#### Transforming the Derivative of a Function
Before moving on, we must present a very important scenario that shows that our vectors as defined prior are not the only mathematical objects needed for manifolds. 

Let $f:M^{n}\rightarrow \mathbb{R}$ be a differentiable function on $M^{n}$. In elementary mathematics it is often said the the $n$-tuple 
$$
\left[ \frac{\partial f}{\partial x^{1}},\ldots, \frac{\partial f}{\partial x^{n}} \right]^{T}
$$
form the components of a vector field "grad $f$". However, if we look at the transformation properties in the patch $U \cap V$, by the chain rule 
$$
\frac{\partial f}{\partial x_{V}^{i}} = \sum\limits_{k} \left[ \frac{\partial x_{U}^{k}}{\partial x_{V}^{j}}\right] \frac{\partial f}{\partial x_{U}^{k}}
$$
and this is _not_ the rule for a contravariant vector. We shall see later how to deal with $n$-tuples that transform as "grad $f$" or the gradient. 

---
### Covectors and Tensors

We just considered the -tuple of partial derivatives of a single function  and we noticed that this n-tuple does not transform in the same way as the n-tuple of components of a vector. These components  transform as a new type of "vector." Now, to support this, we shall talk about the general notion of "tensor" that will include both notions of vector and a whole class of objects characterized by a transformation law generalizing what we talked about prior. We strive to define these objects and operations on them "intrinsically," that is, in a basis-free fashion. We shall also be very careful in our use of sub- and superscripts when we express components in terms of bases; _the notation is designed to help us recognize intrinsic quantities when they are presented in component form and to help prevent us from making blatant errors_.

##### Linear Functionals and the Dual Space
Let $E$ be a real vector space. Although for some purposes $E$ may be infinite-dimensional, we are mainly concerned with the finite-dimensional case. Although $\mathbb{R}^{n}$, as the space of real $n$-tuples $(x^{1},\ldots,x^{n})$, comes equipped with a distinguishable basis $(1,0,0,0,\ldots,0)^{T},\ldots,$ the general $n$-dimensional vector space $E$ has no basis prescribed. 

Choose a basis ${\bf{e}}_{1},\ldots,{\bf{e}}_{n}$ for the $n$-dimensional space $E$. Then a vector ${\bf{v}} \in E$ has a unique expansion
$$
{\bf{v}} = \sum\limits_{j}{\bf{e}}_{j}v^{j} = \sum\limits_{j}v^{j} {\bf{e}}_{j}
$$
where the $n$ real numbers $v^{j}$ are the **components** of $\bf{v}$ with respect to the given basis. For algebraic purposes, _we prefer the first presentation_, where we have put the "scalars" $v^{j}$ to the right of the basis elements. We do this for several reasons, but mainly so that _we can use matrix notation_, as we shall see in the next paragraph. When dealing with calculus, however, this notation is awkward. For example, in $\mathbb{R}^{n}$ (thought of as a manifold, we can write the standard basis at the origin as ${\bf{e}}_{j} = \frac{\pmb{\partial}}{\pmb{\partial} x^{j}}$; then our favored presentation would say $\pmb{v} = \sum\limits_{j} \frac{\pmb{\partial}}{\pmb{\partial} x^{j}} v^{j}$, making it appear, incorrectly, that we are differentiating the components in this expression. Sometimes we will simply use the traditional $\sum\limits_{j}v^{j} \pmb{e}_{j}$. We shall use the matrices 
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
Note that the components of a linear functional are written as a _row_ matrix $a$.

##### The Differential of a Function
```ad-Definition
The dual space $M_{p}^{n*}$ to the tangent space $M_{p}^{n}$ at the point $p$ of a manifold is called the **cotangent space**. 
```

Recall that on a manifold $M^{n}$, a vector $\pmb{v}$ at $p$ is a differential operator on functions defined near $p$. 

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
and would be called a covector **field**, and so on; $df = \sum\limits_{j}(\frac{\partial f}{\partial x^{j}})dx^{j}$ is an example. Thus the numbers $\frac{\partial f}{\partial x^{1}},\ldots,\frac{\partial f}{\partial x^{n}}$ form the components _not_ of a vector field but rather of a covector field, the differential of $f$. We remarked in our warning before, these numbers are called the components of the "gradient vector" in elementary mathematics, but we shall _never_ say this. It is important to realize that the local expression (2.8) holds in _any_ coordinate system; for example, in spherical coordinates for $\mathbb{R}^{3}$, $f = f(r, \theta, \phi)$ and 
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
This is the _transformation rule_ for the components of a covariant vector and should be compared with (1.6). In the notation used in (1.7) we may write 
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
 replaces the Euclidean $\pmb{v}=\sum\limits_{i} \left<\pmb{v},\pmb{e}_{i} \right>\pmb{e}_{i}$ that holds when the basis is orthonormal. 

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

### The Cotangent Bundle and Phase Space 
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

### Tensors and the Wedge Product
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
---
**Remark.**  We can create mixed tensors with contravariant and covariant inputs. And we can derive the transformation laws for tensors by transforming the inputs. 

#### The Wedge Product 
Before the middle of the nineteenth century, Grassmann introduced a new "algebra" whose product is a vast generalization of the scalar and vector products in use today in vector analysis In particular it is applicable in space of any dimension. Before discussing the "Grassmann product" it is helpful to consider a simpler product, special cases of which we have used earlier. Before we defined the vector space $\otimes^{p}E^{*}$ of covariant $p$-tensors over the vector space $E$; these covariant tensors were simply $p$-linear maps $\alpha:E\times\ldots \times E \rightarrow \mathbb{R}$. We now define the "tensor" product of a covariant $p$-tensor and a covariant $q$-tensor. 

```ad-Definition
If $\alpha \in \otimes^{p}E^{*}$ and $\beta \in \otimes^{q}E^{*}$, then their **tensor product** $\alpha \otimes \beta$ is the covariant $(p+q)$ tensor defined by 
$$
\alpha \otimes \beta(\mathbf{v}_{1},\ldots, \mathbf{v}_{p+q}) \equiv \alpha(\mathbf{v}_{1},\ldots,\mathbf{v}_{p})\beta(\mathbf{v}_{p+1},\ldots,\mathbf{v}_{p+q})
$$
```

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

We can generalize this to any manifold, and we can use the wedge product to derive the volume elements for manifolds as 
$$
dV =\sqrt{|g_{ij}|} \ dx^{1} \wedge dx^{2} \wedge \ldots \wedge dx^{n}
$$

#### Covariant Derivative
The derivative of a tensor is not guaranteed to give you back a tensor. We also would like to have a derivative that takes into account the curvature. Consider we have a space described by a metric tensor that is nonuniform and changes at each point. Taking the ordinary derivative of a constant vector, we get a non zero result since a variable metric gives the illusion of nonconstant derivatives and measures of length. Thus, we introduce the covariant derivative, which uses what we call the "Christoffel Symbols" that act as the derivative of the metric in a way. We will define them below, but note that in essence, the covariant derivative projects the derivative of a vector on a manifold into its tangent space. And since we can compare tangent spaces directly, we get a universal derivative that is globally useful for different manifolds and metrics.

The covariant derivative $\nabla_\mu$ of a vector field $V^\nu$ is given by: $$ \nabla_\mu V^\nu = \partial_\mu V^\nu + \Gamma^\nu_{\mu\lambda} V^\lambda $$ For a covector field $\omega_\nu$, the covariant derivative is: $$ \nabla_\mu \omega_\nu = \partial_\mu \omega_\nu - \Gamma^\lambda_{\mu\nu} \omega_\lambda $$ The Christoffel symbols $\Gamma^\lambda_{\mu\nu}$ are defined as: $$ \Gamma^\lambda_{\mu\nu} = \frac{1}{2} g^{\lambda\sigma} \left( \partial_\mu g_{\nu\sigma} + \partial_\nu g_{\mu\sigma} - \partial_\sigma g_{\mu\nu} \right) $$
### Mechanics on a Manifold
We now have all the machinery we need to describe mechanics on a manifold. 

Let $M^{n}$ be the configuration space of a dynamical system and let $q^{1},\ldots,q^{n}$ be local generalized coordinates. For simplicity, we shall restrict ourselves to time-independent Lagrangians. the Lagrangian $L$ is then a function of the generalized coordinates $q$ and the generalized velocities $\dot{q}$, $L=L(q,\dot{q})$. It is important to realize that $q$ and $\dot{q}$ are $2n$-independent coordinates. (Of course if we want we can consider a specific path $q=q(t)$ in configuration space then the Lagrangian along this evolution is computing by $\dot{q}=\frac{dq}{dt}$.) Thus the Lagrangian $L$ is to be considered as a function on the space of generalized velocities, that is, $L$ is a real-valued function on the tangent bundle to $M$. The tangent bundle is the space of coordinates $(x,\dot{x})$, or the collection of all tangent spaces for each point $x$.
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
and so the $p$'s represent then not the components of a vector on the configuration space $M^{n}$ bur rather a _covector_. The $q$'s and $p$'s then are to be thought of not as local coordinates in the tangent bundle but as coordinates for the _cotangent bundle_ (the collection of all dual spaces for each point $x$). Equation (2.26) is then to be considered not as a change in coordinates in $TM$ but rather as the local description of a map 
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

We see that the metric tensor used to raise and lower the indices of the momentum are the same as for the position. Thus, we expect that the curvature of the momentum space (which is dual to the position space on the manifold) has curvature described by $g^{ij}$ if we exclude transformations of coordinates in the momentum space (which then require a Jacobian transform on the momentum forms). 

## Developing Quantum Mechanics on the Manifold
The variable relations: $x,p,t$ are the configuration space position, momentum, and time respectively. When transforming to the QPSR we recall that (where $\ \hat{}$  denotes operators and $\alpha,\gamma$ are otherwise free parameters): 
$$
    \begin{aligned}
        H\left(x,\ p,\ t\right)\rightarrow\ \hat{H}\left(\hat{x},\ \hat{p},\ t\right)=\hat{H}\left(i\hbar\partial_p+\alpha x,\ -i\hbar\partial_x+\gamma p,\ t\right),\ \ni\alpha+\gamma=1
    \end{aligned}

$$
$$
    \begin{aligned}
       x\rightarrow\ \hat{x}\equiv\ i\hbar\partial_p+\alpha\ x,\ p\rightarrow\hat{p}\equiv -i\hbar\partial_x+\gamma\ p,t\rightarrow\ t=t 
    \end{aligned}
$$
$$
\begin{aligned}
       \left(x_1,\ldots,x_n\right)\rightarrow\left(\widehat{x_1},\ldots,\widehat{x_n}\right)= \left(i\hbar\partial_{p_1}+\alpha_1x_1,\ldots,i\hbar\partial_{p_n}+\alpha_nx_n\right),\ni\alpha_j+\gamma_j=1,\ j=1,\ldots,n
    \end{aligned}
$$
$$
\begin{aligned}
           H\left(x_1,\ldots,x_n;p_1,\ldots,p_n; t\right)\rightarrow\hat{H}\left({\hat{x} }_1,\ldots,{\hat{x}}_n;{\hat{p} }_1,\ldots,{\hat{p}}_n;t\right)
    \end{aligned}
$$
$$
    \begin{aligned}
        \equiv \hat{H}\left(i\hbar\partial_{p_1}+\alpha_1x_1,\ldots,i\hbar\partial_{p_n}+ \alpha_nx_n;-i\hbar\partial_{x_1}+\gamma_1p_1,\ldots,-i\hbar\partial_{x_n}+\gamma_np_n;t\right).
    \end{aligned}
$$

Using these general definitions, the time independent wave equation becomes	
$$

    \begin{aligned}
        \hat{H}\binom{i\hbar\partial_{p_{r_1}}+\alpha_1x_1,\ldots,i\hbar\partial_{p_{r_n}}+\alpha_nx_n;}{-i\hbar\partial_{x_1}+\gamma_1p_{r_1},\ldots,-i\hbar\partial_{x_n}+\gamma_np_{r_n}}\psi\left(x_1,\ldots,x_n;p_{r_1},\ldots,p_{r_n}\right)=E_n\psi(x_1,\ldots,x_n;p_{r_1},\ldots,p_{r_n}). 
    \end{aligned}
$$
Applying the alternative to the convolution and multi-variable inverse transform, we can derive that
$$
    \begin{aligned}
        \equiv\hat{H}\binom{i\hbar{\overline{p}_r}_1+\alpha_1x_1,\ldots,i\hbar{\overline{p}_r}_n+\alpha_nx_n;}{-i\hbar\partial_{x_1}+\gamma_1p_{r_1},\ldots,-i\hbar\partial_{ x_n}+\gamma_np_{r_n}}\check{\psi}\left(x_1,\ldots,x_n;{\overline{p}_r}_1,\ldots,{\overline{p}_r}_n\right) ={E}_n\check{\psi}\left(x_1,\ldots,x_n;{\overline{p}_r}_1,\ldots,{\overline{p}_r}_n\right).
    \end{aligned}
$$
Thus, the wave function in phase space can be expressed as the inverse transform of the solution $\breve{\psi}\left(x_1,\ldots,x_n;{\overline{p}_r}_1,\ldots,{\overline{p}_r}_n;t\right)$ from $(\overline{p}_r \to p_r)$. This tactic is the Half-Transform Ansatz (HTA) and the typical method to solving this Schrodinger Equation is the NU method. With the HTA, we can find exponential factors that correspond to translations in the values of $\alpha,\beta,\gamma,$ and $\delta$ such that $g_{\phi}$ represent the translations:
 $$
     \begin{aligned}
         e^{i \phi}\psi = g_{\phi} + \begin{pmatrix}
         \alpha \\ \beta \\ \gamma \\ \delta
         \end{pmatrix}
     \end{aligned}
 $$


![[Pasted image 20240820152453.png|center]]

And by using these exponential factors, we can solve systems by changing their perception of position in momentum (this info is held within the values of $\alpha,\beta,\gamma$, and $\delta$). We can also see that there are families of solutions on the manifold with either different quantum numbers or different energy eigenvalues (depending on how you want to model the manifold).

Taking a large intuitive leap, we claim that the machinery for such a behavior is a Riemannian Manifold and in the following section we shall explore this idea more completely. And our expressions for the shifts if $\alpha$ and $\beta$ suggest that there is a corresponding Lie group.


We shall first consider a construction of traditional quantum mechanics on a manifold. Clearly this will be in $L^2(1)$, an important note when we will later consider the phase space in $L^2 (2).$ As an example, let us look at a system in the position space on $\mathbb{R}^3$ with coordinates $(x^1,x^2,x^3)$. We will have the quantum operators with expectation values:
$$
\begin{aligned}
      \hat{\mathbf{x}} = x^j {\hat{\mathbf{e}}_{j}},
      \quad \hat{\mathbf{p}} = -i \hbar \nabla = -i \hbar {\hat{\mathbf{e}}_i} \eta^{ij} \frac{\partial}{\partial x^j} = -i \hbar {\hat{\mathbf{e}}_i} \partial^i , \quad \\
      \left< x^j \right> = \left< \psi | \hat{x}^j | \psi \right>, \quad \left<p^i \right> = \left<\psi | \hat{p}^i | \psi \right>, \quad i=x^1,x^2,x^3, \quad j=1,2,3 \\
\end{aligned}
$$
where $\eta^{ij}$ is the Euclidean metric $\delta^{i}_j$ and $\psi$ is the wave function. In this case the Hilbert Space scalar product is simply defined as 
$$
    \left< \psi | \phi \right> \equiv \int_{\mathbb{R}^3} d^3 \mathbf{x} \ \psi^*(\mathbf{x}) \phi(\mathbf{x}).
$$

Let us now look at a 3 dimensional submanifold of $\mathbb{R}^3$ denoted by $\mathcal{M}$, described by the coordinates $(\tilde{x}^1,\tilde{x}^2,\tilde{x}^3)$, where each coordinate component is a function of our flat coordinates, $\tilde{x}^\mu=\tilde{x}^\mu (x^1,x^2,x^3)$. Assume we have the metric $g_{\mu \nu}$, then our divergence and gradient operators become 
$$
    \begin{aligned}
        \text{Div} X = \frac{1}{\sqrt{|g|}} \partial_{\mu} \left(\sqrt{|g|} \tilde{x}^\mu \right)  \\
        \text{grad} \ \phi = \partial^\mu \phi = g^{\mu \nu} \partial_{\mu} \phi,
    \end{aligned}
$$
where $|g| := |\det{g_{\mu \nu}}|$ and $X$ is any contravariant vector. For a free particle in flat space the Time Independent Schrodinger Equation becomes 
$$
    \frac{- \hbar^2}{2m} \frac{1}{\sqrt{|g|}} \partial_{\mu} \left(\sqrt{|g|} g^{\mu \nu} \partial_\nu \psi \right) = E \psi.
$$
The action for a free particle in flat space will be 
$$
    S = \int_{\mathbb{R}^3} dV \left(\frac{\hbar^2}{2m} \nabla \psi^{*} \cdot \nabla \psi - E \psi^{*} \psi \right) .
$$ 
In curved space, the gradient is generalized as seen prior, and our inner product is mediated by the metric $g_{\mu \nu}$. The volume form $dV$ transforms into $\sqrt{|g|} d \tilde{x}^1 \wedge d \tilde{x}^2 \wedge d \tilde{x}^3 = \sqrt{|g|}d\tilde{V}$, where $\tilde{x}^\mu$ are the curved space coordinates. Hence, the action becomes 
$$
    S = \int_\mathcal{M} d \tilde{V} \left(\frac{\hbar^2}{2m} g^{\mu \nu} \partial_{\mu}\psi^* \partial_{\nu}\psi - E \psi^* \psi \right) \sqrt{|g|} .
$$
We may now also write the Hilbert Space scalar product as
$$
    \left< \psi | \phi \right> \equiv \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \sqrt{|g|} \ \psi^*(\tilde{\mathbf{x}}) \phi(\tilde{\mathbf{x}}).
$$
From here we can clearly write the completeness relation
$$
    \mathbb{1} = \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \sqrt{|g|} \ \left| \tilde{\mathbf{x}} \right> \left< \tilde{\mathbf{x}} \right|,
$$
where $\left< \tilde{\mathbf{x}}\right| \equiv \left< \tilde{x}^1\right| \otimes \left< \tilde{x}^2\right| \otimes \left<\tilde{x}^3\right|$, and the orthogonality condition 
$$
    \left< \tilde{x}^i | \tilde{x}^j \right> = \frac{\delta^3(\tilde{x}^i-\tilde{x}^j)}{\sqrt{|g|}}.
$$
Clearly on the configuration manifold, we have the position operator definition 
$$
    \hat{x}^\mu = \tilde{x}^\mu.
$$
Now, let us begin to look at the momentum operator on the configuration space manifold. For the momentum operator to continue obeying the Heisenberg Algebra as in flat space, we need $\hat{p}_\mu$ to be Hermitian with respect to the invariant measure. We see that this is not the case for the form $\hat{p}_\mu = -i\hbar \partial_\mu$. But we expect that we can modify it to get a Hermitian result using the covariant derivative. We begin by looking at the adjoint of this suggested momentum operator.
$$
\begin{aligned}
    \left<\psi | \hat{p}_\mu | \phi\right> &= \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \sqrt{|g|} \left<\psi | \tilde{\mathbf{x}}\right> \left<\tilde{\mathbf{x}} | \hat{p}_\mu| \phi \right> \\
    &= -i\hbar \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \sqrt{|g|}\psi^*(\tilde{\mathbf{x}}) \partial_\mu \phi(\tilde{\mathbf{x}}) \\
    &= -i\hbar\left[ \psi^*(\tilde{\mathbf{x}})\phi(\tilde{\mathbf{x}})\right]^{+\infty}_{-\infty} + i\hbar \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \ \partial_i\left(\psi^*(\tilde{\mathbf{x}})\sqrt{|g|}\right) \phi(\tilde{\mathbf{x}}) \\
    &= i\hbar \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \ \left(\sqrt{|g|}\partial_\mu(\psi^*(\tilde{\mathbf{x}}))+\psi^*(\tilde{\mathbf{x}})\partial_\mu
    (\sqrt{|g|})\right)\phi(\tilde{\mathbf{x}})\\
    &= \int_\mathcal{M} d^3 \tilde{\mathbf{x}} \left[-i\hbar \left(\partial_\mu + \frac{\partial_\mu(\sqrt{|g|})}{\sqrt{|g|}}\right)\psi(\tilde{\mathbf{x}}) \right]^* \phi(\tilde{\mathbf{x}}) \sqrt{|g|} \\
    &= \left< \psi \right| \hat{p}^\dagger_\mu \left|\phi \right>
    \end{aligned}
$$
assuming that the boundary terms for the wave functions vanish. Note that this is not a mathematical condition for $L^2$ functions. Physically we cannot prepare a state arbitrarily distanced from the point in space where our physical instruments are localized. Additionally, we may have a manifold that has a smooth, symmetric boundary such that these terms cancel out. For scenarios such having a bounded manifold with small length scales relative to the size of the system, then this assumption will no longer hold. Using our result above, we now write the Hermitian momentum operator 
$$

    \hat{p}_\mu = -i\hbar \left(\partial_\mu + \frac{1}{2} \frac{\partial_\mu(\sqrt{|g|})}{\sqrt{|g|}}\right) = -i\hbar \left(\partial_\mu + \frac{1}{2}\Gamma^\kappa_{\mu \kappa}\right) = -i\hbar \tilde{\partial}_\mu
$$
with Christoffel symbol $\Gamma^\kappa_{\mu \nu}$. Remark that the modified derivative term corresponds to the covariant derivative of a scalar density with weight $\frac{1}{2}$ which we denote by $\tilde{\partial}_\mu.$ We can rewrite the momentum operator in flat space using a basis transform to get
$$
    \hat{p}_i = -i\hbar \partial_i {\tilde{x}^\mu} \tilde{\partial}_\mu, \quad \hat{p}^i = -i\hbar \partial^\mu x^i \tilde{\partial}_\mu
$$

It is seen that the contravariant form of the momentum operator then be written as $\hat{\mathbf{p}} = - i \hbar {\partial}^{\mu} \mathbf{r} \tilde{\partial}_{\mu}$. The angular momentum can then be written as $\hat{\mathbf{L}} = \hat{\mathbf{r}} \times \hat{\mathbf{p}} = -i \hbar  \mathbf{r} \times  ({\partial}^{\mu} \mathbf{r} \tilde{\partial}_{\mu})$, such that we can write the matrix element as 
$$
    \left< {\mathbf{L}} \right>  = -i \hbar \int_\mathcal{M} d \tilde{V}  \psi^* \mathbf{r} \times ({\partial}^{\mu} \mathbf{r} \tilde{\partial}_{\mu} \psi) \sqrt{|g|} .
$$
Now, we move to derive the operators in the momentum representation. We assume similar construction as for the position space representation, writing the momenta as a function of their flat space counterparts. Recall the eigenket conditions
$$
    \hat{{x}^\mu}\left|\tilde{\mathbf{x}}\right> = \tilde{x}^\mu \left| \tilde{\mathbf{x}} \right>, \quad \hat{p}_\mu\left| \tilde{\mathbf{p}}\right> = \tilde{p}_\mu \left| \tilde{\mathbf{p}}\right>
$$
where we define $\hat{x}^\mu \equiv 1 \otimes 1 \otimes \ldots \otimes \tilde{x}^\mu \otimes \ldots \otimes 1$ and so on for the momentum operator. We may then define the general operators over the entire Hilbert space to be the sum of these component operators. The momentum operator definition can be expressed in the position representation as
$$
    \left<\tilde{\mathbf{x}}\right| \hat{{p}}_\mu= -i\hbar  \tilde{\partial}_\mu \left<\tilde{\mathbf{x}}\right|.
$$
The matrix elements for $\hat{p}$ in the position and momentum representation can be written as
$$
    \left< \tilde{\mathbf{x}} | \hat{p}_\mu | \tilde{\mathbf{p}}\right> = -i\hbar \tilde{\partial}_\mu \left<\tilde{\mathbf{x}}|\tilde{\mathbf{p}}\right> = \tilde{p}_\mu \left<\tilde{\mathbf{x}}|\tilde{\mathbf{p}}\right>.
$$
Now, to solve this equation above, we consider a solution of the form
$$
 \langle \tilde{\mathbf{x}} | \tilde{\mathbf{p}} \rangle = f(\tilde{\mathbf{p}})e^{\frac{i}{\hbar} \tilde{p}_\mu \tilde{x}^\mu}
$$
Clearly this solutions holds, and we may use the normalization condition to find $f(\tilde{\mathbf{p}})= \frac{1}{(2 \pi \hbar)^{3/2}} |g|^{1/4}$. However, we must note that this result is quite counterintuitive and is not consistent with the Fourier Transform nor the orthogonality condition of momentum, which we will expand on later. Thus, let us now construct the Fourier Transform on the Manifold in hopes to reconcile such discrepancy.

For a function $f(x)$ defined almost everywhere on the manifold $\mathcal{M}$ with coordinates $x$, we define the Fourier transform to be 
$$
    \bar{f}(p)= \frac{1}{(2 \pi)^{n/2}} \int_{\mathcal{M}} d^n x \sqrt{|g|} e^{-i p_\mu x^\mu} f(x).
$$
This integral can be evaluated in the limit of small volumes with invariant measure $d^n \sqrt{|g|}$. Before we continue, we must also find the appropriate measure for the momentum space. Of course, by definition of the canonical momentum, we see that it is a local description of a map $P: TM^n \rightarrow T^* M^n.$ Thus, we expect that the measure for the momentum will have a factor of $\sqrt{|g^{ij}|} = \frac{1}{\sqrt{|g|}}.$ This also provides a way to make an invariant measure in phase space on the cotangent bundle. Note that we are thus assuming the structure of the momentum space is dependent on the curvature in the configuration space, and we do not consider scenarios where the metric is momentum dependent. If we were to consider such a metric, the plane wave may no longer be an eigenfunction of the momentum operator due to the change of the connection. We may also lose the dual relationship between position and momentum when considering an independent momentum manifold. Thus, for now we consider only a position dependent metric which also defines the curvature of the momentum space. we require the condition
$$
    \int_{\mathcal{M}} \frac{d^n p}{\sqrt{|g|}} e^{-i p_\mu (x^\mu - {x^\mu}')} = \frac{(2 \pi)^{n/2}}{\sqrt{|g|}} \delta^n(x-x')
$$
such that 
$$
    \frac{1}{(2 \pi)^{n/2}} \int_{\mathcal{M}} d^n x \sqrt{|g|} \int_{\mathcal{M}} \frac{d^n p}{\sqrt{|g|}} e^{-i p_\mu(x^\mu-{x^\mu}')} = 1.
$$
For consistency we this must have
$$

    \bar{f}(p) = \frac{1}{(2\pi)^{n/2}}\int_{\mathcal{M}} d^n x \sqrt{|g|} \int_{\mathcal{M}} \frac{d^n p'}{\sqrt{|g|}} e^{-i x^\mu (p_\mu -{p'_\mu})} \bar{f}(p'),
$$
which follows via the inverse transform
$$
    f(x) = \frac{1}{(2 \pi)^{n/2}} \int_{\mathcal{M}} \frac{d^n p}{\sqrt{|g|}} e^{i p_\mu x^\mu} \bar{f}(p).
$$
Note that if we change the order of integration in our integral above, assuming convergence in either order of integration, that we have the distribution
$$
    \frac{1}{(2 \pi)^{n/2}} \int_{\mathcal{M}} d^n x  \ e^{-i x^\mu(p_\mu - p'_\mu)} 
$$
which acts as $\delta^n(p-p')$ in the cotangent space. We can define the local area which we integrate over and use Lebesgue integration to partition the domain depending on the values that the function we integrate takes on. To reconcile Lebesgue integration on the Manifold, we look at the following definition:

For a subset $V$ of $\mathbb{R}^n$, every $n$-form can be written $\omega = f \, dx^1 \wedge \dots \wedge dx^n$, and you define
$$
\int_V \omega = \int_V f \, dx^1 \wedge \dots \wedge dx^n := \int_V f \, dx^1 \dots dx^n,
$$
where $dx^1 \dots dx^n$ is the Lebesgue measure on $\mathbb{R}^n$. On an (oriented) manifold (think about $\int_a^b f dt = -\int_b^a f dt$), you define the integral by taking a partition of unity $(\psi_i)$ subordinate to an (oriented) atlas $\{(\varphi_i, U_i)\}$ and set
$$
\int_M \omega = \sum \psi_i \int_{\varphi(U)} (\varphi_i^{-1})^* \omega,
$$
where the integrals under open subsets of $\mathbb{R}^n$ under the sign $\sum$ are defined as previously. So we patch coherently together Lebesgue integrals in order to define manifold integrals, and with this formula, you can still check some properties from measure theory (for example, with the change of variables: if $F: M \to N$ is an orientation-preserving diffeomorphism, then $\int_M F^* \omega = \int_N \omega$).

Now, we may use this to prove that our integral prior acts as the dirac delta for momentum in the cotangent space. And then we may transform between the position and momentum spaces using this Fourier Transform. 

The rest of QM in the position and momentum space follows. Now, the goal of research is to expand this formulation into the $L^{2}$ space on the cotangent bundle where we have coordinates of $(x,p)$ or we take the cartesian product $M_{x}^{n}\times M_{p}^{n}$ for the position and momentum manifolds. To do this, we must consider the Hilbert Space over the cotangent bundle. The conditions on the $\alpha, \beta, \gamma, \delta$ allow us to use this representation, and their behvaiors create the noncommutative nature of quantum mechanics needed for a phase space representation. Their behavior that permits this formulation will be noted below below as follows:

Note that due to the transformation of the basis vectors, we will have a new condition for the commutator relations. This is easily shown as 
$$
\begin{aligned}
    \hat{x}^i\hat{p}^i = -\hbar^2 \beta^i \delta^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial^\mu}x^i \tilde{\partial}_{p^\mu} \tilde{\partial}_{\mu} &+ i\hbar \beta^i \gamma^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial}_{p^\mu}p^i + i\hbar p^i \beta^i \gamma^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial}_{p^\mu}  \\ &+ i \hbar \alpha^i x^i \delta^i \tilde{\partial}^\mu x^i \tilde{\partial}_\mu + \alpha^i x^i \gamma^i p^i
    \end{aligned}
$$

$$
    \begin{aligned}
        \hat{p}^i\hat{x}^i = -\hbar^2 \beta^i \delta^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial^\mu}x^i \tilde{\partial}_{p^\mu} \tilde{\partial}_{\mu} &+ i
        \hbar \delta^i \alpha^i \tilde{\partial}^\mu x^i \tilde{\partial}_\mu x^i  +i\hbar p^i \beta^i \gamma^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial}_{p^\mu}  \\ &+ i \hbar \alpha^i x^i \delta^i \tilde{\partial}^\mu x^i \tilde{\partial}_\mu + \alpha^i x^i \gamma^i p^i
    \end{aligned}
$$
such that by commutation 
$$
    [\hat{x}^i,\hat{p}^i] = i \hbar [\beta^i \gamma^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial}_{p^\mu}p^i - \delta^i \alpha^i \tilde{\partial}^\mu x^i \tilde{\partial}_\mu x^i] = i\hbar 
$$
since we are working in the laboratory coordinates. This gives us the new condition 
$$
    \beta^i \gamma^i \tilde{\partial}^{p^\mu}p^i \tilde{\partial}_{p^\mu}p^i - \delta^i \alpha^i \tilde{\partial}^\mu x^i \tilde{\partial}_\mu x^i = 1
$$
which we may also write as 
$$
\begin{aligned}
    \beta^i \gamma^i g^{\mu \nu,p} \tilde{\partial}_{p^\nu}p^i \tilde{\partial}_{p^\mu}p^i - \delta^i \alpha^i 
 g^{\mu \nu,x} \tilde{\partial}_\nu x^i \tilde{\partial}_\mu x^i = 1 
 \end{aligned}
$$

If we were to consider a flat space, then by the transformation law of covariant tensors $g^{\mu \nu,p} \tilde{\partial}_{p^\nu}p^i \tilde{\partial}_{p^\mu}p^i = \delta^{i}_i = 1$ and $g^{\mu \nu,x} \tilde{\partial}_\nu x^i \tilde{\partial}_\mu x^i = \delta^{i}_i = 1$ such that we recover the form
$$
    \beta^i \gamma^i  - \alpha^i \delta^i = 1 
$$

As we see, $\alpha,\beta,\gamma$, and $\delta$ have scaling factors appearing due to the curvature of the space we are working in. If we look at these factors, we may assume they have some transformation law such that we have some condition analogous to (excluding the metric tensors)
$$
    \beta^\mu \gamma^\mu - \alpha^\mu {\delta^\mu} = 1
$$
Since the factors seen in the flat space are on equal footing, we may consider that each factor has the transformation from flat to curved space:
$$
    \beta^\mu = \beta^i \tilde{\partial}_{p^\mu} p^i, \gamma^\mu = \gamma^i \tilde{\partial}_{p^\mu} p^i, \alpha^\mu = \alpha^i \tilde{\partial}_\mu x^i, \delta^\mu = \delta^i \tilde{\partial}_\mu x^i. 
$$
We see that each of these objects actually transform not like vectors, but like covectors. Hence, we shall actually consider these factors to be components of covectors, two of which ($\alpha$ and $\delta$) live on the position manifold dual space and the other two ($\gamma$ and $\beta$) which live on the momentum manifold dual space. However, note that due to the dimensions, we would get a scalar. Thus, now in the correct notation with lowered indices, we write 
$$
    \beta_\mu \gamma_\nu g^{\mu \nu, p}- \alpha_\mu \delta_\nu g^{\mu \nu, x} = 1 
$$
However, this cannot be correct, as we require multiple equations corresponding to the dimension of the metric tensor. Note that we may try to fix this issue by considering each parameter to actually be a rank 2 covariant tensor with components only down the diagonal. For example, $\beta_{ij} = \delta^i_j \beta^i$. Note that these tensors are symmetric. Then, we may try to write something analogous to the matrix formulation:
$$
    \beta G^{p} \gamma - \alpha G^x \delta = \mathbb{I}
$$
where $G^x$ and $G^p$ are the contravariant versions of the metric tensors for the position and momentum manifolds respectively. If we index each row of these parameter tensors by $i$, we may instead write three equations (one for each row covector)
$$
    {\beta_{i \mu }} g^{\mu \nu, p} \gamma_{i \nu} - \alpha_{i \mu} g^{\mu \nu, x} \delta_{i \nu} = 1
$$
which returns our original result that we expect. Note that we can then write this expression using the contravariant form of the row covectors with the inner product on the manifolds $\left<, \right>$:
$$
    \left< {\beta_i}^{\mu}, {\gamma_i}^{\nu}   \right>_P - \left< {\alpha_i}^{\mu}, {\delta_i}^{\nu} \right>_X = 1
$$
where the subscripts $P$ and $X$ on the inner product specify which manifold we are working on. The indices $\mu$ and $\nu$ were left in the expression above (despite being the indices we sum across when taking the inner product) to emphasize that the parameter tensors are curvilinear and that we are working with the row vectors. We now try to rewrite our flat space operators as (considering the parameters as tensors in the euclidean space):
$$
    \hat{{x}}^i = i\hbar \beta_{i j} \tilde{\partial}^{p^\mu} {p}^j \tilde{\partial}_{p^\mu} + \alpha_{i j} x^j
$$
$$
    \hat{{p}}^i = i\hbar \delta_{i j} \tilde{\partial}^{\mu} x^j \tilde{\partial}_{\mu} +  \gamma_{i j} p^j
$$

But note that this cannot be the case, as the $i$ indices are contravariant on the left side and covariant on the right hand side. We now realize an important remark: we need the columns to transform like vectors and we need the rows to transform like covectors. We could have chosen the columns to transform like covectors and for the rows to transform like vectors, but this does not follow the traditional notion of matrix multiplication and thus we will not use it. Thus, we realize that it is only natural to have our parameter tensors to be mixed tensors with defined components along the diagonal as expressed prior. Hence we define each parameter $\alpha, \beta, \gamma, \delta$ to be the diagonal components of a mixed tensor covariant in its column index and contravariant in its row index. We then write our parameter tensors in flat space as ${\beta^i}_j,{\gamma^i}_j,{\alpha^i}_j,{\delta^i}_j$.


Since there is a 1:1 correspondence between mixed tensors and linear transformations, we may say that each parameter represents a linear transformation. $\beta$ and $\gamma$ are linear transformations on the momentum manifold that scale the components of position and momentum in the momentum representation respectively. $\alpha$ and $\delta$ then act in the same manner on the position manifold for the position representation. In matrix form we may also write $\beta = \text{diag}(\beta^1,\beta^2,\ldots)$ and so on. We will use $\mu ,\nu$ to denote tensors with transformed (curvilinear) row covectors or column vectors. We then rewrite our results above in the following fashion:
$$
\begin{aligned}

     {\beta^i}_\mu g^{\mu \nu, p} {\gamma^i}_\nu - {\alpha^i}_\mu g^{\mu \nu, x} {\delta^i}_\nu = 1 \\
     \left< {\beta^{i \mu}}, \gamma^{i \nu}   \right>_P - \left< \alpha^{i \mu}, \delta^{i \nu} \right>_X = 1 \\
    \beta G^{p} \gamma - \alpha G^x \delta = \mathbb{I}
\end{aligned}
$$

We will now express an important realization that follows from our results. Heisenberg's Uncertainty Principle is a condition on the projection of the vector spaces generated by the linear transforms that dictate the footing of position and momentum. There are two linear transformations for each manifold, representing the scaling of position in the momentum representation, position in the position representation, momentum in the position representation, and momentum in the momentum representation. The phase space quantum operators then act across both manifolds (which represent the position and momentum representations). 

Additionally, prior to now, we did not transform the $\alpha x$ and $\gamma p$ terms in the operators since we want them to depend on the euclidean $x$ and $p$. However, when we transform the parameter matrices into curvilinear coordinates, we would like both sets of matrices to transform so we can have an entirely curvilinear or flat space collection of linear transforms. Thus, we will present both forms. We write our quantum operators in flat space as:
$$
\begin{aligned}
    \hat{{x}}^i = i\hbar {\beta^i}_j \tilde{\partial}^{p^\mu} {p}^j \tilde{\partial}_{p^\mu} + {\alpha^i}_j x^j = i\hbar {\beta^i}_\mu \tilde{\partial}^{p^\mu} + {\alpha^i}_\mu \tilde{x}^\mu \\
    \hat{{p}}^i = i\hbar {\delta^i}_j \tilde{\partial}^{\mu} x^j\tilde{\partial}_{\mu} +  {\gamma^i}_j p^j = i\hbar {\delta^i}_\mu \tilde{\partial}^{\mu} +  {\gamma^i}_\mu \tilde{p}^\mu 
    \end{aligned}
$$
To write these expressions in vector form, we use $\boldsymbol{\beta}$ to represent the $\beta$ matrix in curvilinear coordinates with rows transformed like covectors on the momentum manifold. In other words, the new transform after we apply the $\beta$ matrix to the Jacobian on the momentum manifold. And the column vectors, written in the basis relevant to the context, for column $\mu$ of this new transform will be denoted $\boldsymbol{\beta}_\mu$. These vectors act as our new basis. We will also express the components of the curvilinear coordinate matrix as $\beta^\mu$. We will use this same notation across all parameter matrices. 
$$
    \begin{aligned}
        \hat{{\mathbf{x}}} = i\hbar \beta \tilde{\partial}^{p^\mu} \mathbf{p} \tilde{\partial}_{p^\mu} + \alpha \mathbf{x} = i\hbar \boldsymbol{\beta}_\mu \tilde{\partial}^{p^\mu} + \boldsymbol{\alpha}_\mu \tilde{x}^\mu  \\
    \hat{{\mathbf{p}}} = i\hbar \delta \tilde{\partial}^{\mu} \mathbf{x} \tilde{\partial}_{\mu} +  \gamma \mathbf{p} = i\hbar \boldsymbol{\delta}_\mu \tilde{\partial}^\mu + \boldsymbol{\gamma}_\mu \tilde{p}^\mu 
    \end{aligned}
$$

We may also consider the parameters of $\alpha,\beta,\gamma$ and $\delta$ as intrinsic to the manifold, and instead of considering linear transformations acting on the position and momentum, we may introduce them as a part of a curvilinear coordinate system. Formulations on this coordinate system then represents quantum mechanics in the phase space. However, we cannot put all parameter factors in the coordinate system in a way that gets rid of them appearing in the quantum operators. It is also less intuitive to work with such a coordinate system. Instead, by only considering linear transforms, we may use the same manifolds for position and momentum as done in the classical case but with conditions on these linear transforms.