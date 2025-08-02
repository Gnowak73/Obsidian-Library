---
tags: Math, differential_geometry, integral, exterior, form, exterior_forms
dg-publish: true
mathLink: 
---
Subject: _Differential Geometry, Tensor Calculus_
Main\_Topic: _Integrals and Exterior Forms_
Applications: _Differential Geometry Fundamentals_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

#### Line Integrals
For simplicity, let $C$ be a smooth "oriented" or "directed" curve, the image under $F : \ [a,b] \subset \mathbb{R}^{1} \rightarrow C \subset \mathbb{R}^{3}$ (which is read: "$F$ maps the interval $[a,b]$ on $\mathbb{R}^{1}$ into the curve $C$ in $\mathbb{R}^{3}$") with $F(a)$ for some $p$ and $F(b)$ for some $q$. 

![[Screenshot 2023-08-11 182904.png|center]]

If $\alpha=\alpha^{1} = a_{i}(x)dx^{i}$ is a 1-form, a covector, in $\mathbb{R}^{3}$, we define the line integral $\int\limits_{C}\alpha$ as follows.

Using the parametrization $x^{i} = F^{i}(t)$ of $C$, we define 
$$
\int\limits_{C}\alpha^{1} = \int\limits_{C}a_{i}(x)dx^{i} \equiv \int\limits_{a}^{b}a_{i}(x(t)) \left(\frac{dx^{i}}{dt}\right)dt = \int\limits_{a}^{b} \alpha \left(\frac{d\pmb{x}}{dt}\right)dt
$$
We say that we _pull back_ the form $\alpha^{1}$ (that lives in $\mathbb{R}^{3}$) to a 1-form on the parameter space $\mathbb{R}^{1}$, called the **pull-back** of $\alpha$, denoted by $F^{*}(\alpha)$. 
$$
F^{*}(\alpha) = \alpha\left(\frac{d\pmb{x}}{dt}\right)dt = a_{i}(x(t))\left(\frac{dx^{i}}{dt}\right)dt
$$
and then we take the _ordinary_ integral $\int\limits_{a}^{b}\alpha\left(\frac{d\pmb{x}}{dt}\right)dt$. It is a classical theorem that the result is _independent of the parametrization of $C$ chosen_, so long as the resulting curve has the same orientation. This will become "apparent" from the usual geometric interpretation that we now present. 

In the definition there has been no mention of _arc_ length or _scalar product_. Suppose now that a Riemannian metric is available. Then to $\alpha$ we may associate its contravariant vector $\pmb{A}$. Then $\alpha\left(\frac{d\pmb{x}}{dt}\right)=\left<\pmb{A}, \left(\frac{d\pmb{x}}{dt}\right) \right> = \left<\pmb{A}, \frac{d \pmb{x}}{ds} \right>\left(\frac{ds}{dt}\right)$ where $s=s(t)$ is the arclength parameter of $C$. Then $F^{*}(\alpha)=\alpha\left(\frac{d\pmb{x}}{dt}\right)dt =\left<\pmb{A}, \frac{d \pmb{x}}{ds} \right>ds$. But $\pmb{T} \equiv \frac{d\pmb{x}}{ds}$ is the [[Tangent and Normal Vectors|Unit Tangent Vector]] to $C$ since $g_{ij}\left(\frac{dx^{i}}{ds}\right)\left(\frac{dx^{j}}{ds}\right)=\frac{g_{ij} dx^{i}dx^{j}}{ds^{2}}=1$. It only makes sense to divide one forms here because we are restricting to a curve.

```ad-Remember
Dividing forms doesn't make sense in most scenarios but it does in some. Dividing forms only makes sense when you dividng a k-form on a space of $k$ dimensions. For example, dividing 1-forms only makes sense if we are doing a **pull back** to a curve in one dimension. And for a 2D surface, we can divide 2-forms. This works though as long as the denominator is **not vanishing on our surface**. 

For example, if we have the 1-form $dx$ which can be pulled back and parametrized by $t$ on the 1D manifold, we transform by $dx=\frac{dx}{dt}dt=f(t)dt$. And for another differential $dy = \frac{dy}{dt}dt=g(t)dt$, we can divide these two 1-forms to get $\frac{dx}{dy}=\frac{f(t)}{g(t)}$ assuming $g(t)\neq 0$.

Differentials represent a displacement in a specific direction. That direction is encoded into the differentail, hence why it represents a covector at each point on a manifold.

Differentials represent covector fields. In other words, tensors, where each point on a manifold has a distance and a direction in a coordinate space.

It is also worth noting that **a parameter is not a coordinate**, thus if time is a parameter, then we can cancel the differentials.

-Ted Shifrin
```

Thus, 
$$
F^{*}(\alpha) = \left<\pmb{A},\pmb{T} \right>ds = ||\pmb{A}|| \ ||\pmb{T}|| \ \cos \angle(\pmb{A},\pmb{T})ds
$$
and so 
$$
\int\limits_{C}\alpha = \int\limits_{C}A_{tan}ds
$$
is geometrically the integral of the tangential component of $\pmb{A}$ with respect to the arc length parameter along $C$. This "shows" independence of the parameter $t$ chosen, but to evaluate the integral one would _usually_ just use $\int\limits_{a}^{b} \alpha \left(\frac{d\pmb{x}}{dt}\right)dt$, which involves no metric at all. 

**Remark.**  From this, we see that the integrand in a line integral is naturally a **1-form**, not a vector.

---
#### Exterior 2-Forms 
We have already defined the **tensor product** $\alpha^{1}\otimes \beta^{1}$ of two 1-forms to be the bilinear form $\alpha^{1}\otimes \beta^{1}(\pmb{v},\pmb{w})=\alpha^{1}(\pmb{v})\beta^{1}(\pmb{w})$. We now define a more geometrically significant **wedge** or **exterior product** $\alpha \wedge \beta$ to be the _skew_ symmetric bilinear form
$$
\alpha^{1} \wedge \beta^{1} \equiv \alpha^{1} \otimes \beta^{1} - \beta^{1}\otimes \alpha^{1} 
$$
and thus 
$$
du^{j}\wedge du^{k}(\pmb{v},\pmb{w}) = v^{j}w^{k} -v^{k}w^{j} = \begin{vmatrix} du^{j}(\pmb{v}) & du^{j}(\pmb{w}) \\ du^{k}(\pmb{v}) & du^{k}(\pmb{w})\end{vmatrix}
$$
In cartesian coordinates $x,y,z$, $dx \wedge dy(\pmb{v},\pmb{w})$ is $\pm$ the area of the parallelogram spanned by the projections of $\pmb{v}$ and $\pmb{w}$ into the $x,y$ plane, the plus sign is used only if $\text{proj} \ \pmb{v}$ and $\text{proj} \ \pmb{w}$ describe the same orientation of the plane as the basis vectors $\pmb{\partial}_{x}$ and $\pmb{\partial}_{y}$.  

![[Screenshot 2023-08-12 192819.png|center]]

let now $x^{i},i=1,2,3$ be _any_ coordinates in $\mathbb{R}^{3}$. Note that 
$$
dx^{j}\wedge dx^{k} = -dx^{k} \wedge dx^{j} \quad \text{and} \quad dx^{k} \wedge dx^{k} = 0
$$
The most general **exterior 2-form** is of the form 
$$\boxed{\beta^{2}=\sum\limits_{i<j}b_{ij} \ dx^{i}\wedge dx^{j} \quad \text{where}  \quad b_{ji}=-b_{ij}}$$
In $\mathbb{R}^{3}$, $\beta^{2} = b_{12}dx^{1}\wedge dx^{2} + b_{23}dx^{2}\wedge dx^{3} + b_{13}dx^{1} \wedge dx^{3}$, or, as we prefer, 
$$
\beta^{2} = b_{23}dx^{2} \wedge dx^{3} + b_{31} dx^{3} \wedge dx^{1} + b_{12} dx^{1} \wedge dx^{2}
$$
An exterior 2-form is a skew symmetric covariant tensor of the second rank in the sense of [[Tensor Examples]]. We frequently will omit the term "exterior", but _never_ the wedge $\wedge$.