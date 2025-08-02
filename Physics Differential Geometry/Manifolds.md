---
tags: Manifolds, topology, math, geometry, differential, differential_geometry
dg-publish: true
mathLink: 
---
Subject: _Topology, Differential Geometry_
Main\_Topic: _None_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _[[Submanifolds]],[[Tensors and Exterior Forms]]_
Cont.\_ of: _None_ 
_
_

The notion of a "topology" will allow us to talk about "continuous" functions and points "neighboring" a given point, in spaces where the notion of distance and metric might be lacking. 

The cultivation of an intuitive "feeling" for manifolds is of more importance, at this stage, than concern for topological details, but some basic notions from point set topology are helpful. They should be approached like a new language, with some measure of fluency, it is hoped for later on. 

#### Some Notions from Point Set Topology
```ad-Definition
An **open ball** in $\mathbb{R}^{n}$, radius $\epsilon$, centered at $\pmb{a} \in \mathbb{R}^{n}$ is 
$$
B_{\pmb{a}}(\epsilon) = \{\pmb{x} \in \mathbb{R}^{n} \ \rvert \ ||\pmb{x}-\pmb{a}|| < \epsilon\}
$$

```

```ad-Definition
A **closed ball** in $\mathbb{R}^{n}$ is defined by 
$$
\overline{B_{\pmb{a}}}(\epsilon) = \{ \pmb{x} \in \mathbb{R}^{n} \rvert \ ||\pmb{x}-\pmb{a}||\leq \epsilon \}
$$
that is, the closed ball is the open ball with its edge or boundary included.
```

A set $U$ in $\mathbb{R}^{n}$ is declared **open** if for given any $\pmb{a} \in U$ there is an open ball of some radius $r>0$, centered at $\pmb{a}$, that lies entirely in $U$. Clearly each $B_{\pmb{b}}(\epsilon)$ is open if $\epsilon>0$ (take $r=\epsilon - \frac{||\pmb{b}-\pmb{a}||}{2}$), whereas $\overline{B_{b}}(\epsilon)$ is not open because of its boundary points. $\mathbb{R}^{n}$ itself is trivially open. The empty set is technically open since there are no points $\pmb{a}$ in it. 

A set $F$ in $\mathbb{R}^{n}$ is declared **closed** if its complement $\mathbb{R}^{n}-F$ is open. It is easy to check that each $\overline{B_{\pmb{a}}}(\epsilon)$ is a closed set, whereas the open ball is not. Note that the entire space $\mathbb{R}^{n}$ is both open and closed, since its complement is empty. 

It is immediate that the _union_ of _any_ collection of open sets in $\mathbb{R}^{n}$ is an open set, and it is not difficult to see that the _intersection_ of any _finite_ number of open sets in $\mathbb{R}^{n}$ is open. 

We have just described the "usual" open sets in Euclidean Space. What do we mean by an open set in a more general space? We shall define the notion of open sets axiomatically. 
#### Topological Spaces
```ad-Definition
A **topological space** is a set $M$ with a distinguished collection of subsets, to be called the **open** sets. These open sets must satisfy the following:

1. Both $M$ and the empty set are open
2. If $U$ and $V$ are open sets, then so is their intersection $U\cap V$
3. The union of any collection of open sets is open 

These sets "define" **The Topology** of $M$.
```

**Remark.**  A different collection might define a different topology

Any such collection of subsets that satisfies the 3 definitions above is eligible for defining topology in $M$. In our introductory discussion of open balls in $\mathbb{R}^{n}$ we also defined the collection of open subsets of $\mathbb{R}^{n}$. These define the topology of $\mathbb{R}^{n}$, the "usual" topology. An example of a "perverse" topology on $\mathbb{R}^{n}$ is the **discrete** topology, in which _every_ subset of $\mathbb{R}^{n}$ is declared open! 

A subset of $M$ is **closed** if its complement is open. 

Let $A$ be any subset of a topological space $M$. Define a topology for the space $A$ (the **induced** or **subspace** topology) by declaring that $V \subset A$ to be an open subset of $A$ provided $V$ is the intersection of $A$ with some open subset $U$ of $M$, $V=A \cap U$. 

These sets _do_ define a topology for $A$. For example, let $A$ be a line in the plane $\mathbb{R}^{2}$. An open ball in $\mathbb{R}^{2}$ is simply a disc without its edge. This disc either will not intersect $A$ or will intersect $A$ in an "interval" that does not contain its endpoints. This interval will be an open set in the induced topology on the line $A$. It can be shown that any open set in $A$ will be a union of such intervals. 

Any _open_ set in $M$ that contains a point $x \in M$ will be be called a _neighborhood_ of $x$. If $F:M \rightarrow N$ is a map of a topological space $M$ into a topological space $N$, we say that $F$ is **continuous** if for every open set $V \subset N$, the **inverse image** $F^{-1}V \equiv \{x\in M \rvert \ F(x) \in V \}$ is open in $M$. (This reduces to the usual $\epsilon, \delta$ definition in the case where $M$ and $N$ are Euclidean spaces.) The map sending all of $\mathbb{R}^{n}$ into a single point of $\mathbb{R}^{m}$ is an example showing that a continuous map need not send open sets into open sets. 
##### Homeomorphism
If $F:M \rightarrow N$ is one-to-one and onto, then the inverse _map_ $F^{-1}:N \rightarrow M$ exists. If further both $F$ and $F^{-1}$ are continuous, we say that $F$ is a **homeomorphism** and that $M$ and $N$ are **homeomorphic**. A homeomorphism takes open (closed) sets into open (closed) sets. Homeomorphic spaces are to be considered to be "the same" as topological spaces; we say that they are "topologically the same." It can be proved that $\mathbb{R}^{n}$ and $\mathbb{R}^{m}$ are homeomorphic if and only if $m=n$. 

**Remark.** This is similar to [[Group Homomorphisms]], except instead of preserving the structure and binary operation of a group, we preserve the topological properties of a space.

#### Compactness
The technical definition of a manifold requires two more concepts: "Hausdorff" and "countable base." We shall not discus these here. They can be seen explicitly in [[Countable Base]] and [[Hausdorff]].

There is one more concept that plays a very important role, though not needed for the definition of a manifold:

```ad-Definition
A topological space $X$ is called **compact** if from _every_ covering of $X$ by open sets one can pick out a _finite_ number of the sets that still covers $X$. 
```

For example, the open interval $(0,1)$, considered as a subspace of $\mathbb{R}$, is _not_ compact; we cannot extract a finite subcovering from the open covering given by the sets $U_{n}= \{x \ \vert \frac{1}{n}<x<1\} \ n=1,2,\ldots$. 

**Remark.**  A **subcover** of some set $X$ is a family of subsets whose union is all of $X$.

On the other hand, the closed interval $[0,1]$ is a compact space. In fact, it is shown in every topology book that _any subset $X$ of $\mathbb{R}^{n}$_ (with the induced topology) is _compact_ if an only if 
1. $X$ is a _closed_ subset of $\mathbb{R}^{n}$
2. $X$ is a _bounded_ subset, that is, $||x|| < \text{some number} \ c$, for all $x \in X$

#### 2 Main Properties of Continuous Maps
Finally, we shall need two properties of continuous maps. 

**Property 1:**  The continuous image of a compact space is itself compact.

**Proof:**  If $f: G \rightarrow M$ is continuous and if $\{U_{i}\}$ is an open cover of $f(G)\subset M$, then $\{ f^{-1}(U_{i}) \}$ is an _open_ cover of $G$. Since $G$ is compact we can extract a finite open subcover $\{ f^{-1}(U_{\alpha}) \}$ of $G$, and then $\{U_{\alpha}\}$ is a finite subcover of $f(G)$. 

Furthermore, 

**Property 2:**  A continuous real-valued function $f: G \rightarrow \mathbb{R}$ on a compact space $G$ is _bounded_.

**Proof:**  $f(G)$ is a compact subspace of $\mathbb{R}$, and thus is closed and bounded according to the conditions in [[#Compactness]] for $\mathbb{R}^{n}$. 

### The Idea of a Manifold
An n-dimensional (differentiable) manifold $M^{n}$ (briefly, an n-manifold) is a topological space that is locally $\mathbb{R}^{n}$ in the following sense. It is covered by a family of local (curvilinear) coordinate systems $\{U; x_{U}^{1},\ldots,x_{U}^{n}\}$, consisting of open sets of "patches" $U$ and coordinates $x_{U}$ in $U$, such that a point $p \in U \cap V$ that lies in two coordinate patches will have its two sets of coordinates related differentiably (this condition is from [[Submanifolds#Submanifolds of Euclidean Space]])
$$
x_{V}^{i}(p) = f_{VU}^{i}(x_{U}^{1},\ldots,x_{U}^{n}) \quad i=1,2,\ldots,n
$$
(If the functions $f_{UV}$ are $C^{\infty}$, that is, infinitely differentiable, or real analytic,..., we say that $M$ is $C^{\infty}$, or real analytic,...) There are more requirements; for example, we shall demand that each coordinate patch is homeomorphic to some open subset of $\mathbb{R}^{n}$. More of these requirements will be seen later. Examples of manifolds can be seen in [[Geometry of Physics.pdf]] on page 14. 

```ad-note
Analogous to [[External Direct Product]], we can form the **product manifold**
$$
L^{n+r} = M^{n} \times W^{r} = \{(p,q) \vert \ p\in M^{n} \ \text{and} \ q \in W^{r}\}
$$
```

##### Rigorous Definition of a Manifold
Let $M$ be any _set_ (without a topology) that has a covering by subsets $M = U \cup V \cup \ldots$, where each subset $U$ is in 1:1 correspondence $\phi_{U}: U \rightarrow \mathbb{R}^{n}$ with an _open_ subset $\phi_{U}(U)$ of $\mathbb{R}^{n}$. 

![[Pasted image 20231009163048.png|center]]

We require that each $\phi_{U}(U \cap V)$ be an open subset of $\mathbb{R}^{n}$. We require that the overlap maps 
$$
f_{UV} = \phi_{V} \circ \phi_{U}^{-1} : \phi_{U}(U \cap V) \rightarrow \mathbb{R}^{n}
$$
that is, 
$$
\phi_{U}(U \cap V) \xrightarrow[]{\phi_{U}^{-1}} M \xrightarrow[]{\phi_{v}} \mathbb{R}^{n}
$$
be differentiable (we know that it means for a map $\phi_{V} \circ \phi_{U}^{-1}$ from an open set of $\mathbb{R}^{n}$ to $\mathbb{R}^{n}$ to be differentiable). Each pair $U$, $\phi_{U}$ defines a **coordinate patch** on $M$; to $p \in U \subset M$ we may assign the $n$ coordinates of the point $\phi_{U}(p)$ in $\mathbb{R}^{n}$. For this reason we shall call $\phi_{U}$ a **coordinate map**.  

Take now a maximal atlas (collection of all coordinate systems compatible with those that originally were used to define the manifold) of such coordinate patches. Define a **topology** in the set $M$ by declaring a subset $W$ of $M$ to be open provided that given any $p \in W$ there is a coordinate chart $U$, $\phi_U$ such that $p \in U \subset W$. If the resulting topology for $M$ is [[Hausdorff]] and has a [[Countable Base]] we say that $M$ is an n-dimensional differentiable manifold. We say that a _map_ $F: \mathbb{R}^{p}\rightarrow \mathbb{R}^{q}$ is of class $C^{k}$ is all $k^{th}$ partial derivatives are continuous. It is of class $C^{\infty}$ if it is of class $C^{k}$ for all $k$. We say that a _manifold_ $M^{n}$ is of class $C^{k}$ if its overlap maps $f_{UV}$ are of class $C^{k}$. Likewise, we have the notion of a $C^{\infty}$ manifold. An analytic manifold is one whose overlap functions are analytic, that is, expandable in power series ([[Taylor Series]] or [[Laurent Series]]).

Let $F:M^{n}\rightarrow \mathbb{R}$ be a real-valued function on the manifold $M$. Since $M$ is a topological space we know from [[#Topological Spaces]] what is means to say that $F$ is continuous. We say that $F$ is **differentiable** if, when we express $F$ in terms of a local coordinate system $(U,x)$, $F=F_{U}(x^{1},\ldots,x^{n})$ is a differentiable function of the coordinates $x$. Technically this means that when we compose $F$ with the inverse of the coordinate map $\phi_{U}$ 
$$
F_{U} \equiv F \circ \phi_{U}^{-1}
$$
(recall that $\phi_{U}$ is assumed to be 1-1) we obtain a real valued function $F_{U}$ defined on a portion $\phi_{U}(U)$ of $\mathbb{R}^{n}$, and we are asking that this function be differentiable. Briefly speaking, we _envision the coordinates $x$ as being engraved on the manifold $M$_, just as we see lines of latitude and longitude engraved on our globes. A function on the Earth's surface is continuous or differentiable if it is continuous or differentiable when expressed in terms of latitude and longitude, at least if we are away from the poles. Similarly with a manifold. With this understood, we shall _usually omit the process of replacing $F$ by its composition $F \circ \phi_{U}^{-1}$, thinking of $F$ as directly expressible as a function $F(x)$ of any local coordinates_. 

Consider the real projective plane $\mathbb{R}P^{2}$. In terms of homogeneous coordinates we may define a map $(\mathbb{R}^{3}-0)\rightarrow \mathbb{R}P^{2}$ by 
$$
(x,y,z) \rightarrow [x,y,z]
$$
At a point of $\mathbb{R}^{3}$ where, for example, $z\neq 0$ we may use $u=\frac{x}{z}$ and $v=\frac{y}{z}$ as local coordinates in $\mathbb{R}P^{2}$, and then our map is given by the two smooth functions $u=f(x,y,z)=\frac{x}{z}$ and $v=g(x,y,z)=\frac{y}{z}$. 

##### Complex Manifolds: The Riemannian Sphere
A **complex manifold** is a set $M$ together with a covering $M=U \cup V \cup \ldots$, where each subset $U$ is in 1-1 correspondence $\phi_{U}:U \rightarrow \mathbb{C}^{n}$ with an open subset $\phi_U(U)$ of complex n-space $\mathbb{C}^{n}$. We then require that the overlap maps $f_{VU}$ mapping sets in $\mathbb{C}^{n}$ into sets in $\mathbb{C}^{n}$ be _complex analytic_; thus, if we write $f_{UV}$ in the form $w^{k}=w^{k}(z^{1},\ldots,z^{n})$ where $z^{k}=x^{k}+iy^{k}$ and $w^{k}=u^{k}+iv^{k}$, then $u^{k}$ and $v^{k}$ satisfy the [[Complex Derivatives#Cauchy Riemann Equations|Cauchy Riemann Equations]] with respect to each pair $(x^{k},y^{r})$. Briefly speaking, each $w^{k}$ can be expressed entirely in terms of $z^{1},\ldots,z^{n}$ with no complex conjugates $\overline{z}^{r}$ appearing. We then proceed as in the real case before. The resulting manifold is called an $n$-dimensional complex manifold, although its topological dimension is $2n$. Of course the simplest example is $\mathbb{C}^{n}$ itself. Let us consider the most famous nontrivial example, the **Riemannian Sphere** $M^{1}$. 

The complex plane $\mathbb{C}$ (topologically $\mathbb{R}^{2}$) comes equipped with a global complex coordinate $z=x+iy$. It is a complex 1-dimensional manifold $\mathbb{C}^{1}$. To study the behavior of the functions at "$\infty$" we introduce a point at "$\infty$", to form a new manifold that is topologically the 2-sphere $S^{2}$. We do this by means of stereographic projection as follows. 

![[Pasted image 20231019104147.png|center|400]]

In the top part of the figure we have a sphere of radius $\frac{1}{2}$, resting on a $w=u+iv$ plane, with a tangent $z=x+iy$ plane at the north pole. Note that we have oriented these two tangent planes to agree with the usual orientation of $S^{2}$. 

Let $U$ be the subset of $S^{2}$ consisting of all points except for the south pole, let $V$ be the points other than the north pole, let $\phi_{U}$ and $\phi_{V}$ be stereographic projections of $U$ and $V$ from the south and north poles, respectively onto the $z$ and and the $w$ planes. In this way we assign to any point $p$ other than the poles two complex coordinates $z=|z|e^{i \theta }$ and $w=|w|e^{-i \theta}$. From the bottom of the figure, which depicts the planar section in the plane holding the two poles and the point $p$, one reads off from elementary geometry that $|w|=\frac{1}{|z|}$, and consequently 
$$
w=f_{UV}(z) = \frac{1}{z}
$$
gives the relation between the two sets of coordinates. Since this is complex analytic in the overlap $U \cap V$, we may consider $S^{2}$ as a 1-dimensional complex manifold, the Riemannian Sphere. The point $w=0$ (the south pole) represents the point $z=\infty$ that was missing from the original complex plan $\mathbb{C}$.

Note that the two sets of real coordinates $(x,y)$ and $(u,v)$ make $S^{2}$ into a real analytic manifold. 

### Tangent Vectors and Mappings 
We are all acquainted with vectors in $\mathbb{R}^{N}$. A tangent vector to a _submanifold_ $M^{n}$ of $\mathbb{R}^{n}$, at a given point $p \in M^{n}$, is simply the _usual velocity vector $\dot{x}$ to some parametrized curve $x=x(t)$ that lies on $M^{n}$_. On the other hand, a _manifold_ $M^{n}$, as defined in the previous section, is a rather abstract object that need not be given as a subset of $\mathbb{R}^{n}$. For example, the projective plane $\mathbb{R}P^{2}$ was defined to be the space of lines through the origin of $\mathbb{R}^{3}$, that is, a point in $\mathbb{R}P^{2}$ is an entire _line_ in $\mathbb{R}^{3}$; if $\mathbb{R}P^{2}$ were a submanifold of $\mathbb{R}^{3}$ we would associate a _point_ of $\mathbb{R}^{3}$ to each point of $\mathbb{R}P^{2}$. We will be forced to define what we mean by a tangent vector to an abstract manifold. This definition will coincide with the previous notion in the case that $M^{n}$ is a submanifold of $\mathbb{R}^{n}$. The fact that we understand tangent vector to submanifolds is a power psychological tool, for for it can be shown (though it is not elementary) that _every_ manifold can be realized as a submanifold of some $\mathbb{R}^{N}$. In fact, Hassler Whitney, one of the most important contributors to manifold theory in the 20th century, has shown that every $M^{n}$ can be realized as a submanifold of $\mathbb{R}^{2n}$. Thus although we cannot "embed" $\mathbb{R}P^{2}$ in $\mathbb{R}^{3}$, it can be embedded in $\mathbb{R}^{4}$. It is surprising, however, that for many purposes it is of little help to use the fact that $M^{n}$ can be embedded in $\mathbb{R}^{n}$, and we shall try to give definition that are "intrinsic", that is, independent of the use of an embedding. Nevertheless, we shall not hesitate to use an embedding for purposes of visualization, and in fact most of our examples will be concerned with submanifolds rather than manifolds. 

#### Tangent or "Contravariant" Vectors
We motivate the definition of vector as follows. Let $p=p(t)$ be a curve lying on the manifold $M^{n}$; thus $p$ is a map of some interval on $\mathbb{R}$ into $M^{n}$. In a coordinate system $(U,x_{U})$ about the point $p_{0}=p(0)$ the curve will be described by $n$ functions $X_{U}^{i}=x_{U}^{i}(t)$, which will be assumed differentiable. The "velocity vector" $\dot{p(0)}$ was classically described by the $n$-tuple of real numbers $\frac{dx_{U}^{1}}{dt} \vert_{0}\ldots,\frac{dx_{U}^{n}}{dt}\vert_{0}$. If $p_{0}$ also lies in the coordinate patch $(V,x_{V})$, then this same velocity vector is described by another $n$-tuple $\frac{dx_{V}^{1}}{dt}\vert_{0},\ldots,\frac{dx_{V}^{N}}{dt}\vert_{0}$, related to the first set by the chain rule applies to the overlap functions (seen in [[#The Idea of a Manifold]]), $x_{V}=x_{V}(x_{U})$, 
$$
\left. \frac{dx_{V}^{i}}{dt} \right\rvert_{0} = \sum\limits_{j=1}^{n}\left(\frac{\partial x_{V}^{i}}{\partial x_{U}^{j}}\right) (p_{0}) \left(\frac{d x_{U}^{j}}{dt}\right)_{0}
$$
This suggests the following.

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

The term contravariant is traditional and is used throughout physics, and we shall use it even though it conflicts with the modern mathematical terminology of "categories and functions."

```ad-Remember
This vector transform means informationally equivalent in patches from their overlap. If a vector does not follow this transform then whatever is being done with it is not informationally equivalent in either patch.

Below we show that these contravariant vectors are 1:1 and informationally equivalent in different coordinate patches, this is NOT true with covectors as seen later on!
```


##### Vectors as Differential Operators 
In Euclidean space an important role is played by the notion of differentiating a function $f$ with respect to a vector at the point $p$ 
$$
D_{v}(f) = \frac{d}{dt}[f(p+t \pmb{v})]_{t=0}
$$
and if $(x)$ is any cartesian coordinate system we have 
$$
D_{v}(f) = \sum\limits_{j}\left[ \frac{\partial f}{\partial x^{j}} \right](p)v^{j}
$$
This is the motivation for a similar operation on functions on any manifold $M$. A real-valued function $f$ defined on $M^{n}$ near $p$ can be described in a local coordinate system $x$ in the form $f=f(x^{1},\ldots,x^{n})$. (Recall from [[#Rigorous Definition of a Manifold]] that we are really dealing with the function $f \circ \phi_{U}^{-1}$ where $\phi_{U}$ is a coordinate map). If $\pmb{X}$ is a vector at $p$ we define the derivative of $f$ with respect to the vector $\pmb{X}$ by 
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
in a local coordinate system $(x)$. From now on, we shall make no distinction between a vector and its associated differential operator. Each one of the $n$ operators $\frac{\partial}{\partial x^{i}}$ then defines a vector, written $\frac{\pmb{\partial}}{\pmb{\partial} x^{\alpha}}$, at each $p$ in the coordinate patch. 

The $i^{th}$ component of $\frac{\pmb{\partial}}{\pmb{\partial} x^{\alpha}}$ is, from (1), given by $\delta_{\alpha}^{i}$ (just look at the structure of the equation and use the curve described later in this paragraph). On the other hand, consider that $\alpha^{th}$ **coordinate curve** through a point, the curve being parametrized by $x^{\alpha}$. This curve is described by $x^{i}(t) = Const.$ for $i \neq \alpha$ and $x^{\alpha}(t)=t$. The velocity vector for this curve at parameter value $t$ has components $\frac{dx^{i}}{dt} = \delta_{\alpha}^{i}$. The $j^{th}$ coordinate vector $\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}$ is the velocity vector to the $j^{th}$ coordinate curve parametrized by $x^{j}$! If $M^{n}\subset \mathbb{R}^{n}$, and if $\pmb{r} = (y^{1},\ldots,y^{N})^{T}$ is the usual position vector from the origin, then $\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}$ would be written classically as $\frac{\partial \pmb{r}}{\partial x^{j}}$,
$$
\frac{\pmb{\partial}}{\pmb{\partial} x^{j}} = \frac{\partial \pmb{r}}{\partial x^{j}} = \left( \frac{\partial y^{1}}{\partial x^{j}},\ldots, \frac{\partial y^{N}}{\partial x^{j}}\right)
$$
A familiar example will be given later. 
$$
\boxed{\text{Velocity Vector w.r.t. i-th Coordinate Curve, Parametrized by $x^{i}$  = i-th coordinate vector} \frac{\pmb{\partial}}{\pmb{\partial} x^{i}}}
$$

##### The Tangent Space to $M^{n}$ at a Point 
It is evident from our definition of a **tangent vector** (at the beginning of this subsection) that the sum of two vectors at a point, defined in terms of their $n$-tuples, is again a vector at that point, and that the product of a vector by a scalar, that is, a real number, is again a vector. 

```ad-Definition
The **tangent space** to $M^{n}$ at the point $p \in M^{n}$, writen $M_{p}^{n}$, is the real vector space consisting of all tangent vectors to $M^{n}$ at $p$. If $(x)$ is a coordinate system holding $p$, then the $n$ vectors 
$$
\left. \frac{\pmb{\partial}}{\pmb{\partial} x^{1}} \right\vert_{p} ,\ldots, \left. \frac{\pmb{\partial}}{\pmb{\partial} x^{n}} \right\vert_{p}
$$
for a basis of this $n$-dimensional vector space (as is evident from (2)) and this basis is called a **coordinate basis** or **coordinate frame**. 
```

**Remark.**  If $M^{n}$ is a [[Submanifolds|submanifold]] of $\mathbb{R}^{N}$, then $M_{p}^{n}$ is the usual $n$-dimensional affine subspace of $\mathbb{R}^{N}$ that is "tangent" to $M^{n}$ at $p$, and this is the picture to keep in mind. 

A vector **field** on an open set $U$ will be the differentiable assignment of a vector $\pmb{X}$ to each point of $U$; in terms of local coordinates
$$
\pmb{X} = \sum\limits_{j}X^{j}(x) \frac{\pmb{\partial}}{\pmb{\partial} x^{j}}
$$
where the components $X^{j}$ are differentiable functions of $(x)$. In particular, each $\frac{\pmb{\partial}}{\pmb{\partial} x^{j}}$ is a vector field in the coordinate patch.

```ad-Remember
Now, as we see: some of this notation is quite confusing. Lets try to shed some light on it. First of all, $\frac{\partial}{\partial x^{i}}$ is supposed to show the derivative operator. Now, we extended the idea of vectors to differential operators, such that at a point $p$, we have some $\frac{\pmb{\partial}}{\pmb{\partial} x^{i}}$ that represents a vector at each point. 

We also can conclude that the i-th coordinate basis vector $\frac{\pmb{\partial}}{\pmb{\partial} x^{i}}$ is equivalent to the velocity vector of the i-th coordinate curve parametrized by $x^{i}$. When we say "velocity of the i-th coordinate curve parametrixed by $x^{i}$", we just mean velocity of the coordinate curves with respect to $x^{i}$. 

If we only consider an individial point $p$ for $\frac{\pmb{\partial}}{\pmb{\partial} x^{i}}$ where $i$ is a set value and not a variable going over a range of values, we are talking about a vector. However, when we talk about a set of points, then $\frac{\pmb{\partial}}{\pmb{\partial} x^{i}}$ is different for each point. Then, technically, we are talking about a vector field.

Also keep in mind that some do not write the difference between $\frac{\pmb{\partial}}{\pmb{\partial} x^{i}}$ and $\frac{\partial}{\partial x^{i}}$, and based on application you see which meaning is inferred. 
```


As an example, let us look at:
![[Pasted image 20231024171156.png|center]]

We have drawn the unit 2-sphere $M^{2}=S^{2}$ in $\mathbb{R}^{3}$ with the usual spherical coordinates. Note that the two basis vectors at $p$ do not live in $S^{2}$, but rather in the linear space $S_{p}^{2}$ attached to $S^{2}$ at $p$. Vectors at $q\neq p$ live in a different vector space $S_{q}^{2}$

```ad-warning
Because $S^{2}$ is a submanifold of $\mathbb{R}^{3}$ and because $\mathbb{R}^{3}$ carries a familiar metrix, it makes sense to talk about the length of tangent vectors to this particular $S^{2}$. However, the definition of a manifold given before **does not require** that $M^{n}$ be given as some specific subset of $\mathbb{R}^{N}$. Thus, _we do not have the notion of length of a tangent vecctor to a general manifold_. For example, the configuration space of a thermodynamical system might have the coordinates given by pressure $p$, volume $v$, and temperature $T$, and the notions of the lengths of $\frac{\pmb{\partial}}{\pmb{\partial} p}$ and so on seem to have no physical significance. If we wish to talk about length of a vector on a manifold we shall be forced to introduce an __additional structure_. The most common structure is called a **Riemannian structure** or _metric_. 
```

##### Mappings and Submanifolds of Manifolds
Let $F:M^{n}\rightarrow V^{r}$ be a map from one manifold to another. In terms of local coordinates $x$ near $p \in M^{n}$ and $y$ near $F(p)$ on $V^{r}$, $F$ is described by $r$ function of $n$ variables $y^{\alpha} = F^{\alpha}(x^{1},\ldots,x^{n})$ (from [[Submanifolds]]), which can be abbreviated $y=F(x)$ or $y=y(x)$. If, as we shall assume, the functions $F^{\alpha}$ are differentiable functions of the $x$'s, we say that $F$ is differentiable. As usual, such functions are, in particular, continuous. 

When $n=r$, we say that $F$ is a **diffeomorphism** provided $F$ is 1:1, onto, and if, in addition, $F^{-1}$ is also differentiable. Thus such an $F$ is a differentiable homeomorphism with a differentiable inverse. (If $F^{1}$ does exist and the Jacobian determinant does not vanish, $\frac{\partial(y^{1},\ldots y^{n})}{\partial(x^{1},\ldots,x^{n})}\neq 0$, then the inverse function theorem of advanced calculus would assure us that the inverse _is_ differentiable. 

The map $F:\mathbb{R} \rightarrow \mathbb{R}$ given by $y=x^{3}$ is a differentiable homeomorphism, but it is not a diffeomorphism since the inverse $x=y^\frac{1}{3}$ is not differentiable at $x=0$. We have already discussed submanifolds on $\mathbb{R}^{n}$ but now we shall need  to discuss submanifolds of a manifold. A good example is the equator $S^{1}$ of $S^{2}$. 

```ad-Definition
$W^{r} \subset M^{n}$ is an (**embedded**) **submanifold** of the manifold $M^{n}$ provided $W$ is locally described as the common locus 
$$
F^{1}(x^{1},\ldots,x^{n}) = 0,\ldots,F^{n-r}(x^{1},\ldots,x^{n})=0
$$
of $(n-r)$ differentiable functions that are independent in the sense that the Jacobian matrix $\left[\frac{\partial F^{\alpha}}{\partial x^{i}}\right]$ has rank $(n-r)$ at each point of the locus. 
```

The implicit function theorem assures us that $W^{r}$ can be locally described (after perhaps permuting some of the $x$ coordinates) as a locus
$$
x^{r+1} = f^{r+1}(x^{1},\ldots,x^{r}),\ldots, x^{n} = f^{n}(x^{1},\ldots,x^{r})
$$
It is not difficult to see from this (as we saw in the case $S^{2} \in \mathbb{R}^{3}$) that _every embedded submanifold of $M^{n}$ is itself a manifold_ ! Later on we shall have occasion to discuss submanifolds that are not "embedded," but for the present we shall assume "embedded" without explicit mention.  

```ad-Definition
The **differential** $F_{*}$ of the map $F:M^{n} \rightarrow V^{r}$ has the same meaning as in the case $\mathbb{R}^{n}\rightarrow \mathbb{R}^{r}$ discussed previously. $F_{*} : M_{p}^{n}\rightarrow V_{F(p)}^{r}$ is the linear transformation defined as follows. For $\pmb{X} \in M^{n}_{p}$, let $p=p(t)$ be a curve on $M$ with $p(0)=p$ and with velocity vector $\dot{p}(0) = \pmb{X}$. Then $F_{*}\pmb{X}$ is the velocity vector $\frac{d}{dt}F(p(t))\vert_{t=0}$ of the image curve at $F(p)$ on $V$. This vector is independent of the curve $p=p(t)$ chosen (as long as $\dot{p}(0)=\pmb{X})$. The matrix of this linear transformation, in terms of the bases $\frac{\partial}{\partial x}$ at $p$ and $\frac{\partial}{\partial y}$ at $F(p)$, is the Jacobian matrix
$$
(F_{*})^{\alpha}_{i} = \frac{\partial F^{\alpha}}{\partial x^{i}}(p)  = \frac{\partial y^{\alpha}}{\partial x^{i}}(p)
$$
```

**Remark.**  This is also known as the pushforward, and maps tangent spaces between manifold.

The main theorem on submanifolds is exactly as in Euclidean space as before from [[Submanifolds]]. 

**Theorem 1.12**  Let $F:M^{n}\rightarrow V^{r}$ and suppose that for some $q \in V^{r}$ the locus $F^{-1}(q) \subset M^{n}$ is not empty. Suppose further that $F_{*}$ is onto, that is, $F_{*}$ is of rank $r$ at each point of $F^{-1}(q)$. Then $F^{-1}(q)$ is an $(n-r)$ dimensional submanifold of $M^{n}$. 

**Example:**  Consider a 2-dimensional torus $T^{2}$ (the surface of a doughnut), embedded in $\mathbb{R}^{3}$. 

![[Pasted image 20231109175713.png|center]]

We have drawn it with a flat top (which is supposed to join _smoothly_ with the rest of the torus). Define a differentiable map (function) $F:T^{2} \rightarrow \mathbb{R}$ by $F(p)=z$, the height of the point $p \in T^{2}$ above the $z$ plane ($\mathbb{R}$ is being identified with the $z$ axis). Consider a point $d \in T$ and a tangent vector $\pmb{v}$ to $T$ at $d$. Let $p=p(t)$ be a curve on $T$ such that $p(0)=d$ and $\dot{p}(0)=\pmb{v}$. The image curve in $\mathbb{R}$ is described in the coordinate $z$ for $\mathbb{R}$ by $z(t)=z(p(t))$, and it is clear from the geometry of $T^{2}\subset \mathbb{R}^{3}$ that $\dot{z}(0)$ is simply the $z$ component of the spatial vector $\pmb{v}$. In other words $F_{*}(\pmb{v})$ is the projection of $\pmb{v}$ onto the $z$ axis. Note then that $F_{*}$ will be onto at each point $p \in T^{2}$ for which the tangent plane $T^{2}(p)$ is _not_ horizontal, that is, at all points of $T^{2}$ except $a \in F^{-1}(0)$, $b \in F^{-1}(2), c \in F^{-1}(4)$, and the entire flat top $F^{-1}(6)$. 

From the main theorem, we may conclude that $F^{-1}(z)$ is a 1-dimensional submanifold of the torus for $0\leq z \leq 6$ except for $z=0,2,4$ and $6$, and this is indeed "verified" in our picture. (We have drawn the inverse images of $z=0,1,\ldots,6$) Notice that $F^{-1}(2)$, which looks like a figure $8$, is _not_ a submanifold; a neighborhood of the point $b$ on $F^{-1}(2)$ is topologically a cross $+$ and thus no neighborhood of $b$ is topologically an open interval of $\mathbb{R}.$ 
```ad-Definition
If $F:M^{n} \rightarrow V^{r}$ is a differentiable map between manifolds, we say that 
1. $x\in M$ is a **regular point** if $F_{*}$ maps $M_{x}^{n}$ onto $V_{F(x)}^{r}$; otherwise we say that $x$ is a **critical point**. 
2. $y \in V^{r}$ is a **regular value** provided either $F^{-1}$ is empty, or $F^{-1}(y)$ consists entirely of regular points. Otherwise $y$ is a **critical value**. 
```

Our main theorem on submanifolds can then be stated as follows. 

**Theorem 1.13**  If $y\in V^{r}$ is a regular value, then $F^{-1}(y)$ either is empty or is a submanifold of $M^{n}$ of dimension $(n-r)$. 

Of course, if $x$ is a critical _point_ then $F(x)$ is a critical _value_. In our toroidal example, Figure 1.18, all values of $z$ other than $0,2,4$ and $6$ are regular. The critical points on $T^{2}$ consist of $a,b,c$ and the entire flat top of $T^{2}$. These latter critical points thus fill up a positive area (in the sense of elementary calculus) on $T^{2}$. Note however, that the image of this 2-dimensional set of critical points consists of the single critical value $z=6$. The following theorem assures us that the critical _values_ of a map form a "small" subset of $V^{r}$; the critical values cannot fill up any open set in $V^{r}$ and they will have "measure" $0$. We will not be precise in defining "almost all"; roughly speaking we mean, in some sense, "with probability 1."

**Sard's Theorem (1.14):**  If $F:M^ {n}\rightarrow V^{R}$ is sufficiently differentiable, then almost all values of $f$ are regular values, and thus for almost all points $y \in V^{r}$, $F^{-1}(y)$ either is empty or is a submanifold of $M^{n}$ of dimension $(n-r)$. 

By sufficiently differentiable, we mean the following. If $n \leq r$, we demand that $F$ be of differentiability class $C^{1}$, whereas if $n-r=k>0$, we demand that $F$ be class $C^{k+1}$. The proof of Sard's theorem is delicate, especially if $n>r$; see, for example \[A,M,R] in [[Geometry of Physics.pdf]]

---
#### Change of Coordinates 
The inverse function theorem is perhaps the most important theoretical result in all of differential calculus. 

**The Inverse Function Theorem (1.15):**  If $F:M^{n} \rightarrow V^{n}$ is a differentiable map between manifolds of the same dimension, and if at $x_{0} \in M$ the differential $F_{*}$ is an isomorphism, that is, it is 1:1 and onto, then $F$ is a local diffeomorphism near $x_{0}$. 

This means that there is a neighborhood $U$ of $x$ such that $F(U)$ is open in $V$ and $F:U \rightarrow F(U)$ is a diffeomorphism. This theorem is a powerful tool for introducing new coordinates in a neighborhood of a point, for it has the following consequence. 

**Corollary (1.16):** Let $x^{1},\ldots,x^{n}$ be local coordinates in a neighborhood $U$ of the point $p \in M^{n}$. Let $y^{1},\ldots,y^{n}$ be any differentiable functions of the $x$'s (thus yielding a map: $U\rightarrow \mathbb{R}^{n}$) such that 
$$
\frac{\partial (y^{1},\ldots,y^{n})}{\partial (x^{1},\ldots,x^{n})} (p) \neq 0
$$
Then the $y$'s form a coordinate system in some (perhaps smaller) neighborhood of $p$. 

For example, when we put $x=r \cos \theta, y=r \sin \theta$, we have $\frac{\partial(x,y)}{\partial(r,\theta)}=r$, and so $\frac{\partial (r, \theta)}{\partial (x,y)}=\frac{1}{r}$. This shows that polar coordinates are good coordinates in a neighborhood of any point of the plane other than the origin. It is important the realize that _this theorem is only local_. Consider the map $F:\mathbb{R}^{2} \rightarrow \mathbb{R}^{2}$ given by $u=e^{x} \cos y, v = e^{x} \sin y$. This is of course the complex analytic map $w=e^{z}$. The real Jacobian $\frac{\partial (u,v)}{\partial (x,y)}$ never vanishes (this is reflected in the complex Jacobian $\frac{dw}{dz}=e^{z}$ never vanishing). Thus, $F$ is locally 1:1. It is not globally so since $e^{z+2 \pi n i} = e^{z}$ for all integers $n$. $u,v$ form a coordinate system not in the whole plane but rather in any strip $a \leq y < a+2 \pi$.

The inverse function theorem and the implicit function theorem are essentially equivalent, the proof of one following rather easily from that of the other. The proofs are fairly delicate; see for example, $[A,M,R]$ in [[Geometry of Physics.pdf]]. 

### Vector Fields and Flows 

##### Vector Fields and Flows on $\mathbb{R}^{n}$
A vector field on $\mathbb{R}^{n}$ assigns in a differentiable manner a vector $\pmb{v}_{p}$ to each $p$ in $\mathbb{R}^{n}$. In terms of cartesian coordinates $x^{1},\ldots,x^{n}$
$$
\pmb{v} = \sum\limits_{j} v^{j}(x) \frac{\partial}{\partial x^{j}}
$$
where the components $v^{j}$ are differentiable functions. Classically this would be written in terms of the cartesian components $\pmb{v} = (v^{1}(x),\ldots,v^{n}(x))^{T}$. Given a "stationary" (i.e. time-independent) flow of the water in $\mathbb{R}^{3}$, we can construct the 1-parameter family of maps 
$$
\phi_{t}:\mathbb{R}^{3} \rightarrow \mathbb{R}^{3}
$$
where $\phi_{t}$ takes the molecule located at $p$ when $t=0$ to the position of the same molecule $t$ seconds later. Since the flow is time-independent 
$$
\phi_{s}(\phi_{t}(p)) = \phi_{s+t}(p) = \phi_{t}(\phi_{s}(p))
$$
and 
$$
\phi_{-t}(\phi_{t}(p)) = p, \quad \text{i.e.}, \ \phi_{-t} = \phi_{t}^{-1}
$$
We say that this defines a 1-**parameter group** of maps. Furthermore, if each $\phi_{t}$ is differentiable, then so is each $\phi_{t}^{-1}$, and so _each_ $\phi_{t}$ is a _diffeomorphism_. We shall call such a family simply a **flow**. Associated with any such flow is a time-independent **velocity field** 
$$
\pmb{v}_{p} \equiv  \left. \frac{d \phi_{t}(p)}{dt} \right]_{t=0}
$$
In terms of coordinates we have 
$$
v^{j}(p) = \left. \frac{d x^{j} (\phi_{t}(p))}{dt} \right]_{t=0}
$$
which will usually be written 
$$
v^{j}(x) = \frac{dx^{j}}{dt}
$$
Thought of as a differential operator on functions $f$ 
$$
\pmb{v}_{p}(f) = \sum\limits_{j} v^{j}(p) \frac{\partial f}{\partial x^{j}} = \sum\limits_{j} \frac{dx^{j}}{dt} \frac{\partial f}{\partial x^{j}} = \left. \frac{d}{dt}f(\phi_{t}(p)) \right]_{t=0}
$$
is the derivative of $f$ along the "streamline" through $p$. 

We thus have the almost trivial observation that to each flow $\{\phi_{t}\}$ we can associate the velocity vector field. The converse result, perhaps the most important theorem relating calculus to science, states, roughly speaking, that to each vector field $\pmb{v}$ in $\mathbb{R}^{n}$ one may associate a flow $\{\phi_{t}\}$ having $\pmb{v}$ as its velocity field, and that $\phi_{t}(p)$ can be found by solving the system of ordinary differential equations 
$$
\frac{dx^{j}}{dt} = v^{j}(x^{1}(t),\ldots,x^{n}(t))
$$
with initial conditions 
$$
x(0) = p
$$
Thus one finds the **integral curves** of the preceding system, and $\phi_{t}(p)$ says, "Move along the integral curve through $p$ (the 'orbit' of $p$) for time $t$." We shall now give a previse statement of this "fundamental theorem" on the existence of solutions of ordinary differential equations. For details one can consult $[A,M,R]$ in [[Geometry of Physics.pdf]], where this result is proved in the context of Banach spaces rather than $\mathbb{R}^{n}$. 

---
**The Fundamental Theorem on Vector Fields in $\mathbb{R}^{n}$ (1.19):**  Let $\pmb{v}$ be a $C^{k}$ vector field, $k \geq 1$ (each component $v^{j}(x)$ is of differentiability class $C^{k}$) on an open subset $U$ of $\mathbb{R}^{n}$. This can be written $\pmb{v}: U \rightarrow \mathbb{R}^{n}$ since $\pmb{v}$ associates to each $x \in U$ a point $\pmb{v}(x) \in \mathbb{R}^{n}$. Then for each $p \in U$ there is a curve $\gamma$ mapping an interval $(-b,b)$ of the real line into $U$
$$
\gamma:(-b,b) \rightarrow U
$$
such that 
$$
\frac{d \gamma(t)}{dt} = v(\gamma(t)) \quad \text{and} \quad \gamma(0) = p
$$
for all $t \in (-b,b)$. (This says that $\gamma$ is an integral curve of $\pmb{v}$ starting at $p$.) Any two such curves are equal on the intersection of their $t$-domains ("uniqueness"). Moreover, there is a neighborhood $U_{p}$ of $p$, a real number $\epsilon>0$, and a $C^{k}$ map 
$$
\Phi:U_{p} \times (-\epsilon,\epsilon) \rightarrow \mathbb{R}^{n}
$$
such that the curve $t \in (-\epsilon, \epsilon) \rightarrow \phi_{t}(q) \equiv \Phi(q,t)$ satisfies the differential equation 
$$
\frac{\partial}{\partial t} \phi_{t}(q) = \pmb{v}(\phi_{t}(q))
$$
for all $t \in (-\epsilon,\epsilon)$ and $q \in U_{p}$. Moreover, if $t,s$ and $t+s$ are all in $(-\epsilon,\epsilon)$, then 
$$
\phi_{t}\circ \phi_{s} = \phi_{t+s} = \phi_{s}\circ \phi_{t}
$$
for all $q \in U_{p}$, and thus $\{\phi_{t}\}$ defined a local $1$-parameters "group" of diffeomorphisms, or **local flow**. 

---
The term _local_ refers to the fact that $\phi_{t}$ is defined only on a subset $U_{p}\subset U \subset \mathbb{R}^{n}$. the word "group" has been put in quotes because this family of maps does not form a group in the usual sense. In general, the maps $\phi_{t}$ are only defined for small $t$, $-\epsilon < t < \epsilon$; that is, **the integral curve through a point $q$ need only exist for a small time**. Thus, for example, if $\epsilon = 1$, then although $\phi_{1/2}(q)$ exists neither $\phi_{1}(q)$ nor $\phi_\frac{1}{2}\circ \phi_{\frac{1}{2}}$ need exist; the point is that $\phi_{\frac{1}{2}}(q)$ need not be in the set $U_{p}$ on which $\phi_{\frac{1}{2}}$ is defined.  

**Example:**  $\mathbb{R}^{n}=\mathbb{R}$, the real line, and $v(x)=x \frac{d}{dx}$. Thus $v$ has a single component $x$ at the point with coordinate $x$. Let $U = \mathbb{R}$. To find $\phi_{t}$ we simply solve the differential equation 
$$
\frac{dx}{dt} = x \quad \text{with initial condition} \quad x(0) = p
$$
to get $x(t)=e^{t}p$, that is, $\phi_{t}(p) = e^{t}p$. In this example the map $\phi_{t}$ is clearly defined on all of $M^{1}=\mathbb{R}$ and for all time $t$. It can be shown that this is true for any _linear_ vector field 
$$
\frac{dx^{j}}{dt} = \sum\limits_{k}a_{k}^{j}x^{k}
$$
defined on _all_ of $\mathbb{R}^{n}$. 

Note that if we solved the differential equation $\frac{dx}{dt}=1$ on the real line with the origin deleted, that is, on the _manifold_ $M^{1}=\mathbb{R}-0$, then the solution curve starting at $x=-1$ at $t=0$ would exist for all times less than $1$ second, but $\phi_{1}$ would not exist; the solution simply runs "off" the manifold because of the missing point. One might think that if we avoid dealing with pathologies such as digging out a point from $\mathbb{R}^{1}$, then our solutions would exist for all time, but as you shall see (and can verify in problem 1.4(1) in [[Geometry of Physics.pdf]]) this is not the case. The growth of the vector field can cause a solution curve to "leave" $\mathbb{R}^{1}$ in a finite amount of time. 

We have required that the vector field $\pmb{v}$ be differentiable. Uniqueness can be lost if the field $\pmb{v}$ is only continuous. For example, again on the real line, consider the differential equation $\frac{dx}{dt}=3x^\frac{2}{3}$. The usual solutions are of the form $x(t)=(t-c)^{3}$, but there is also the "singular" solution $x(t)=0$ identically. This is a reflection of the fact that $x^\frac{2}{3}$ is not differentiable when $x=0$. 

##### Vector Fields on Manifolds 
If $\bf{x}$ is a $C^{k}$ vector field on an open subset $W$ of a _manifold_ $M^{n}$ then we can again recover a $1$-parameter local group $\phi_{t}$ of diffeomorphisms for the following reasons if $W$ is contained in a single coordinate patch $(U,x_{U})$ we can proceed just as in the case $\mathbb{R}^{n}$ earlier since we can use the local coordinates $x_{U}$. Suppose that $W$ is not contained in a single patch. Let $p \in W$ be in a coordinate overlap, $p \in U \cap V$. In $U$ we can solve the differential equations 
$$
\frac{dx_{U}^{j}}{dt} = X_{U}^{j}(x_{U}^{1},\ldots,x_{U}^{n}) 
$$
as before. In $V$ we solve the equations 
$$
\frac{dx_{V}^{j}}{dt} = X_{V}^{j}(x_{V}^{1},\ldots,x_{V}^{n})
$$
Because of the transformation rule in the definition of [[#Tangent or "Contravariant" Vectors]], the right-hand side of this last equation is $\sum\limits_{k}[\frac{\partial x_{V}^{j}}{\partial x_{U}^{k}}]X_{U}^{k}$; the left-hand side is, by the chain rule, $\sum\limits_{k}[\frac{\partial x_{v}^{j}}{\partial x_{U}^{k}}]\frac{dx_{U}^{k}}{dt}$. Thus, because of the transformation rule for a contravariant vector, the two different equations say the _exact same thing_. Using uniqueness, we may then patch together the $U$ and the $V$ solutions to give a local solution in $W$. 

```ad-warning
Let $f:M^{n}\rightarrow \mathbb{R}$ be a differentiabel function on $M^{n}$. In elementary mathematics it is often said the the $n$-tuple 
$$
\left[ \frac{\partial f}{\partial x^{1}},\ldots, \frac{\partial f}{\partial x^{n}} \right]^{T}
$$
form the components of a vector field "grad $f$". However, if we look at the transformation properties in $U \cap V$, by the chain rule 
$$
\frac{\partial f}{\partial x_{V}^{i}} = \sum\limits_{k} \left[ \frac{\partial x_{U}^{k}}{\partial x_{V}^{j}}\right] \frac{\partial f}{\partial x_{U}^{k}}
$$
and this is _not_ the rule for a contravariant vector. One sees then that a proposed differential equation for "steepest ascent,", $\frac{dx}{dt} =$ "grad" $f$, that is 

$$
\frac{dx_{U}^{j}}{dt} = \frac{\partial f}{\partial x_{U}^{j}} \quad \text{in U} \quad \text{and} \quad \frac{d x_{V}^{j}}{dt} = \frac{\partial f}{\partial x_{V}^{j}} \quad \text{in V}
$$
would **not** yield the same thing in two overlappign patches, and consequently **would not** yield a flow $\phi_{t}$. We shall see later how to deal with $n$-tuples that transform as "grad $f$". 
```

##### Straightening Flows 
Our version of the fundamental theorem on the existence of solutions of differential equations, as given in the previous section, is not the complete story; see $[A,M,R$, theorem 4.1.14$]$ or $[A2$, chap. $4]$ in [[Geometry of Physics.pdf]] for details of the following. The map $(p,t)\rightarrow \phi_{t}(p)$ depends smoothly on the initial condition $p$ and on the time of flow $t$. This has the following consequence. (Since our result will be local, it is no loss of generality to replace $M^{n}$ by $\mathbb{R}^{n}$.) _Suppose that the vector field $\bf{v}$ does not vanish at the point $p$_. Then of course it doesn't vanish in some neighborhood of $p$ in $M^{n}$. Let $W^{n-1}$ be a hypersurface, that is, a submanifold of codimension 1, that passes through $p$. Assume that $W$ is **transversal** to $\bf{v}$, that is, the vector field $\bf{v}$ is not tangent to $W$. 

![[Pasted image 20231118135519.png|center]]

Let $u^{1},\ldots,u^{n-1}$ be local coordinates for $W$, and let $p_{u}$ be the point on $W$ with local coordinates $u$. Then $\phi_{t}(p_{u})$ is the point $t$ seconds along the orbit of $\bf{v}$ through $p_{u}$. This point can be described by the n-tuple $(u,t)$. The fundamental theorem states that if $W$ is sufficiently small and if $t$ is also sufficiently small, then $(u,t)$ can be used as (curvilinear) coordinates for some $n$-dimensional neighborhood of $p$ in $M^{n}$. 

To see this we shall apply the inverse function theorem. We thus consider the map $L:W^{n-1} \times (-\epsilon, \epsilon) \rightarrow M^{n}$ given by $L(u,t) = \phi_{t}(p_{u})$. We compute the differential of this map at the origin $u=0$ of the coordinates on $W^{n-1}$. Then by the geometric meaning of $L_{*}$, and since $\phi_{0}(p)=p$
$$
L_{*} \left( \frac{\pmb{\partial}}{\pmb{\partial} u^{1}}\right) = \frac{\partial}{\partial u}[\phi_{0}(u,0,\ldots,0)]_{0} = \frac{\partial p(u,0,\ldots,0)}{\partial u} \vert_{u=0} = \frac{\pmb{\partial}}{\pmb{\partial} u^{1}}
$$
Likewise $L_{*}\left(\frac{\pmb{\partial}}{\pmb{\partial} u^{i}}\right) = \frac{\pmb{\partial}}{\pmb{\partial u^{i}}}$ for $i=1,\ldots,n-1$. Finally
$$
L_{*}(\pmb{v}) = \frac{\partial}{\partial t} \phi_{t}(p_{0}) = \pmb{v}
$$
Thus $L_{*}$ is the identity linear transformation, and by Corollary (1.16) we may use $u^{1},\ldots,u^{n-1}$, $t$ as local coordinates for $M^{n}$ near $p_{0}$. It is then clear that in these new local coordinates near $p$, the flow defined by the vector field $\pmb{v}$ is simply $\phi_{s}:(u,t)\rightarrow (u,s+t)$ and the vector field $\pmb{v}$ in terms of $\frac{\pmb{\partial}}{\pmb{\partial} u^{1}},\ldots,\frac{\pmb{\partial}}{\pmb{\partial} u^{n-1}},\frac{\pmb{\partial}}{\pmb{\partial} t}$, is simply $\pmb{v} = \frac{\pmb{\partial}}{\pmb{\partial} t}$. We have "straightened out" the flow! 

![[Pasted image 20231118144648.png|center]]

This says that near a **nonsingular** point of $\pmb{v}$, that is, a point where $\pmb{v}\neq 0$, coordinates $u^{1},\ldots,u^{n}$ can be introduced such that the original system of differential equations $\frac{dx^{1}}{dt}=v^{1}(x),\ldots,\frac{dx^{n}}{dt}=v^{n}(x)$ becomes 
$$
\tag{1.20}
\frac{du^{1}}{dt}=0,\ldots, \frac{du^{n-1}}{dt}=0, \quad \frac{du^{n}}{dt}=1
$$
**Thus all flows near a nonsingular point are qualitatively the same!** In a sense this result is of theoretical interest only, for in order to introduce the new coordinates $u$ _one must solve the original system of differential equations_. The theoretical interest is, however, considerable. For example, $u^{1}=c_{1},\ldots,u^{n-1} =c_{n-1}$, are $(n-1)$ "first integrals," that is, constants of the motion, for the system (1.20). We conclude that near any nonsingular point of any system there are $(n-1)$ first integrals, $u^{1}(x)=c^{1},\ldots,u^{n-1}(x)=c_{n-1}$ (but of course, we might have to solve the original system to write down explicitly the functions $u^{j}$ in terms of the $x$'s). 

