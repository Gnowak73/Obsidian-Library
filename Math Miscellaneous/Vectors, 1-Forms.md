---
tags: vectors, 1-forms, tensors, covariant, covector, contravariant, Math
dg-publish: true
mathLink: 
---
Subject: _Tensor Calculus_
Main\_Topic: _Vectors and 1-Forms_
Applications: _Tensor Calculus, Differential Geometry, Differential Topology_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _[[Integrals and Exterior Forms]]_
Cont.\_ of: _None_ 
_
_

**Remark.**  Gloss over the notation in [[Superscripts, Subscripts, Summation Convention]] 
### Contravariant Vector
There are two kinds of vectors that appear in physical applications and it is important that we distinguish between them. First there is the familiar "arrow" version. Consider an $n$ dimensional Euclidean Space $\mathbb{R}^{n}$ with cartesian coordinates $x^{1},\ldots,x^{n}$ and local (perhaps curvilinear) coordinates $u^{1},\ldots,u^{n}$. 

**For Example:**  $\mathbb{R}^{n}$ with cartesian coordinates $x^{1}=x,x^{2}=y$, and with polar coordinates $u^{1}=r, u^{2} = \theta$. 

![[Screenshot 2023-08-08 170242.png|center]]

Let $\pmb{p}$ be the position vector from the origin of $\mathbb{R}^{n}$ to the point $p$. In the curvilinear coordinate system $u$, the coordinate curve $C_{i}$ through the point $p$ is the curve where all $u^{j}, j\neq i$, are constants ($r$ in this scenario) , and where $u^{i}$ is used as parameter ($\theta$ in this scenario) . Then the tangent vector to this curve in $\mathbb{R}^{n}$ is 
$$
\frac{\partial \pmb{p}}{\partial u^{i}} \quad \text{which be abbreviate to} \quad \pmb{\partial_{i}} \quad \text{or} \quad \frac{\pmb{\partial}}{\partial u^{i}} 
$$
At the point $p$ these $n$ vectors $\pmb{\partial_{1}},\ldots,\pmb{\partial_{n}}$ form a **Basis** ([[Vector Linear Algebra]]) for all vectors in $\mathbb{R}^{n}$ based at $p$. Any vector $\pmb{v}$ at $p$ has a unique expansion with curvilinear coordinate _components_ ($v^{1},\ldots,v^{n}$)
$$
\pmb{v} = \sum\limits_{i} v^{i} \pmb{\partial}_{i} = \sum\limits_{i}\pmb{\partial_{i}} v^{i}
$$
**Remark.**  This is simple the definition of **span** from [[Vector Linear Algebra]]. $\pmb{p}$ is simply a position vector which has components representing the coordinate system of choice, for example $\pmb{p} = (r, \theta)$ for polar coordinates. $\pmb{u}$ represents what coordinate system you want the basis to represent any vector $\pmb{v}$ (the new $\pmb{p}$) in. For example, if we want to represent a polar coordinate as the sum of basis vectors in cartesian coordinates, we chose $\pmb{u}=(x,y)$

---
We prefer the last expression with the components to the _right_ of the basis vectors since it is traditional to put the vectoral components in a _column matrix_. 
$$
\pmb{\partial} = (\pmb{\partial_{1}}, \ldots,\pmb{\partial}_{n}) \quad \text{and} \quad v = \begin{pmatrix} v^ {1}\\ \vdots \\ v^{n}\end{pmatrix} = (v^{1},\ldots, v^{n})^{T}
$$
where $T$ denotes the [[Transpose]]. Then we can write the matrix expression, 
$$
\pmb{v} = \pmb{\partial} v
$$
**Remark.**  The component vectors $v^{i}$ are the coefficients. Also, beware that $\pmb{\partial}$ does not differentiate the term next to it. It represents the basis vector. 

Of course, we can still differentiate a function along a vector $f$ by defining 
$$
\pmb{v}(f) \equiv \left(\sum\limits_{i} \pmb{\partial}_{i} v^{i}\right)(f) = \sum\limits _{i} \frac{\partial}{\partial u^{i}} (f) v^{i} = \sum\limits_{i} \left(\frac{\partial f}{\partial u^{i}}\right) v^{i}
$$
replacing the basis vector $\pmb{\partial}$ in $\frac{\pmb{\partial}}{\partial u^{i}}$ with the partial differential operator $\partial$ and then applying to the function $f$. 

Let $\pmb{v}$ be a vector at a point $p$. We can always find a curve $u^{i}=u^{i}(t)$ through $p$ whose velocity vector there is $\pmb{v}$, $v^{i}=\frac{du^{i}}{dt}$. Then if $u'$ is a second coordinate system about $p$, we then have $v'^{j} = \frac{du'^{j}}{dt} = \left(\frac{\partial u'^{j}}{\partial u^{i}}\right) \frac{du^{i}}{dt} = \frac{\partial u'^{j}}{\partial u^{i}}\ v^{i}$  Thus the _components_ of a vector transform under a change of coordinates by the rule 
$$
v'^{j} = \sum\limits _{i} \left(\frac{\partial u'^{j}}{\partial u^{i}}\right)v^{i} \quad \text{or as matrices} \quad \boxed{v' = \left(\frac{\partial u'}{\partial u}\right)v }
$$
where $\left(\frac{\partial u'}{\partial u}\right)$ is the **Jacobian Matrix** ([[Jacobian]]). This is the transformation law for the components of a **contravariant vector**, or **tangent** vector, or simply **vector**. 

---
### Covariant Vector
There is a second kind of vector. In [[Linear Algebra]] we learn that each [[Vector Space]] $V$ (in our case, the space of all vectors at a point $p$) can be associated with its **dual** vector space $V^{*}$ ([[Dual Spaces]]) of all real _linear_ functionals $\alpha:V \rightarrow \mathbb{R}$. In coordinates, $\alpha(\pmb{v})$ is a number 
$$
\alpha(\pmb{v}) = \sum\limits_{i}a_{i}v^{i}
$$
for unique numbers ($a_{i}$).

```ad-Definition
A **Linear Functional** is a function in which on a real vector space, $V$, there is a function $T:V \rightarrow \mathbb{R}$ such that 
$$
\begin{gathered}
T(v+w) = T(v)+T(w)\\
T(cv) = cT(v)
\end{gathered}
$$
when $V$ is a complex vector space, then $T$ is a linear map to the complex numbers. 
```

The most familiar linear functional is the _differential_ of a function $df$. As a function on vectors it is defined by the derivative of $f$ along $v$. 
$$
df(v) \equiv \pmb{v}(f) = \sum\limits _{i}\left(\frac{\partial f}{\partial u^{i}}\right)v^{i} \quad \text{and so} \quad (df)_{i}=\frac{\partial f}{\partial u^{i}}
$$
Let us write $df$ in a new form, different from how elementary calculus describes it. 

```ad-Remember
$du^{i}$ is the _linear functional_ that reads off the ith component of any vector $\pmb{v}$ with respect the the basis vectors of the coordinate system $u$. 

$$
du^{i}(\pmb{v}) = du^{i}\left(\sum\limits_{j} \pmb{\partial}_{j} v^{j}\right) \equiv v^{i}
$$

In simpler terms, $du^{i}$ spits out the component of a vector $v$ in the $u^{i}$ direction. For example: $\begin{bmatrix} 1 & 0 & 0 & \ldots & 0 \end{bmatrix}$ for the $x^{1}$ cartesian direction.

```

**Remark.** Note that this agrees with $du^{i}(\pmb{v}) = \pmb{v}(u^{i})$ since $\pmb{v}(u^{i}) = \left(\sum\limits_{j} \pmb{\partial}_{j}v^{j}\right)(u^{i}) = \sum\limits_{j}\left(\frac{\partial u^{i}}{\partial u^{j}}\right)v^{j} = \sum\limits_{j}\delta^{i}_{j}v^{j} = v^{i}$. 

Then we can write 
$$
df(\pmb{v}) = \sum\limits_{i}\left(\frac{\partial f}{\partial u^{i}}\right)v^{i} = \sum\limits_{i}\left(\frac{\partial f}{\partial u^{i}}\right)du^{i}(\pmb{v})
$$
i.e.,
$$
df = \sum\limits_{i}\left(\frac{\partial f}{\partial u^{i}}\right)du^{i}
$$
as usual, except now both sides have meaning as linear functions on vectors.

```ad-warning
We shall not see that this is the gradient vector of $f$!
```

It is very easy to see that $du^{1},du^{2},\ldots$ form a basis for the space of linear functionals at each point of the coordinate system $u$ since they are linearly independent. In fact, this basis of $V^{*}$ is the **dual basis** to the basis $\pmb{\partial}_{1},\ldots,\pmb{\partial}_{n}$, meaning that 
$$
du^{i}(\pmb{\partial}_{j}) = \delta^{i}_{j}
$$
**Remark.**  For dual basis and basis, the inner product between two indices is $\delta^{i}_{j}$, or $v_{i} \cdot v^{j} = \delta^{i}_{j}$ due to biorthogonality of a basis and its dual. Also, remember that $\pmb{\partial}_{j}$ is a basis vector which is why we get either $1$ or $0$. Another note, is that by DEFINITION of a dual basis vector $\beta$ and its corresponding vector basis $b$, $\beta^{i}(b_{j})=\delta^{i}_{j}$. That is simply how we define a dual basis. 

Thus, in the coordinate system $u$, every linear functional $\alpha$ is of the form 
$$
\alpha = \sum\limits_{i}a_{i}(u) du^{i} \quad \text{where} \quad \alpha(\pmb{\partial}_{j}) = \sum\limits _{i}a_{i}(u)du^{i}(\pmb{\partial}_{j}) = \sum\limits_{i}a_{i}(u) \delta^{i}_{j} = a_{j}
$$
is the j-th component of $\alpha$.

We shall see that it is not true that every $\alpha$ is equal to $df$ for some $f$! Which can be seen when we explore the "exterior derivative". We can write the matrix expansion for a linear functional as 
$$
\alpha = (a_{1},\ldots,a_{n})(du^{1},\ldots,du^{n})^{T} = a \ du
$$
where $a$ is a _row matrix_ and $du$ is a _column matrix_ !

If $V$ is the space of contravariant vectors at $p$, then $V^{*}$ is called the space of **covariant** vectors, or **covectors**, or **1-forms** at $p$. Under a change of coordinates, using the chain rule, $\alpha=a' \ du' = a \ du = (a)\left(\frac{\partial u}{\partial u'}\right)(du')$, and so
$$
\boxed{a' = a\left(\frac{\partial u}{\partial u'}\right) = a\left(\frac{\partial u'}{\partial u}\right)^{-1}} \quad \text{i.e.} \quad a'_{j} = \sum\limits_{i}a_{i}\left(\frac{\partial u^{i}}{\partial u'^{j}}\right)
$$
Compare this law transformation to the one in [[#Contravariant Vector]]. 

---
Note that by definition, if $\alpha$ is a covector and $\pmb{v}$ is a vector, then the value 
$$
\alpha(\pmb{v}) = av = \sum\limits_{i}a_{i}v^{i}
$$
is **invariant**, i.e., independent of the coordinates used. This also follows from the two transformation laws described before, such that 
$$
\alpha(\pmb{v}) = a'v' = a \left(\frac{\partial u}{\partial u'}\right)\left(\frac{\partial u'}{\partial u}\right)v = a\left(\frac{\partial  u' }{\partial u}\right)^{-1}\left(\frac{\partial u'}{\partial u}\right)v = av
$$
Note that a vector can be considered as a linear functional on covectors.
$$
\pmb{v}(\alpha) \equiv \alpha(\pmb{v}) = \sum\limits_{i} a_{i}v^{i}
$$
---
**Proof:**  This statement can be proven pretty easily be considering that 
$$
\pmb{v}(\alpha) = \sum\limits_{i}v^{i}\pmb{\partial}_{i}(\alpha) 
$$
and
$$
\pmb{\partial}_{i}(\alpha) = \sum\limits_{j}a_{j}\pmb{\partial}_{i}(du^{j}) 
$$
and we know that 
$$
\pmb{\partial}_{i}(du^{j}) = \frac{\partial}{\partial u^{i}}(du^{j})
$$
and since each $du^{i}$ is linearly independent of one another, then this partial derivative is either $1$ when $j=i$ or $0$ when $i\neq j$, in other words
$$
\pmb{\partial}_{i}(du^{j}) = \delta^{i}_{j}
$$
which makes 
$$
\pmb{\partial}_{i}(\alpha) = \sum\limits_{j}a_{j}\pmb{\partial}_{i}(du^{j})  = \sum\limits_{j}a_{j}\delta^{i}_{j} = a_{i}
$$
resulting in 
$$
\pmb{v}(\alpha) = \sum\limits_{i}v^{i}\pmb{\partial}_{i}(\alpha)  = \sum\limits_{i}a_{i}v^{i}
$$
```ad-Remember
Vectors are named for transforming either "with" or "against" a transform in their basis vectors. **Contravariant** vectors transform "against" the basis vector, and **Covariant** vectors transform against the basis vector. 

By the same logic, 1-forms are called covectors or covariant vectors because their components transform like the basis vectors, while the basis covectors transform like the components of vectors.
```

```ad-note
The trace of a tensor, $P^{i}_{i}$, is **invariant**!
```