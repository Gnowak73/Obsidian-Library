---
tags: exterior, p-forms, differential, geometry, exterior_algebra, cross, scalar, dot, product, vector, Math
dg-publish: true
mathLink: Exterior p-Forms and Algebra in $\mathbb{R}^{n}$
---
Subject: _Differential Geometry_
Main\_Topic: _Exterior p-Forms and Algebra in $\mathbb{R}^{n}$_
Applications: _Differential Geometry Fundamentals_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Geometry of Physics.pdf]]_
Closely\_Related\_To: _[[Integrals and Exterior Forms]], [[Vectors, 1-Forms]]\_
Cont.\_ of: _None_ 
_
_

The **exterior algebra** has the following properties. We have already discussed 1-forms and 2-forms. An (exterior) p-form $\alpha^{p}$ in $\mathbb{R}^{n}$ is a completely skew symmetric multilinear function of p-tuples of vectors $\alpha(\pmb{v}_{1},\ldots,\pmb{v}_{n})$ that changes sign whenever two vectors are interchanged. In any coordinates $x$, for example, the 3-form $dx^{i} \wedge dx^{j}\wedge dx^{k}$ in $\mathbb{R}^{n}$ is defined by 
$$
dx^{i}\wedge dx^{j}\wedge dx^{k}(\pmb{A},\pmb{B},\pmb{C}) \equiv \begin{vmatrix} dx^{i}(\pmb{A}) & dx^{i}(\pmb{B}) & dx^{i}(\pmb{C}) \\ dx^{j}(\pmb{A}) & dx^{j}(\pmb{b})& dx^{j}(\pmb{C})  \\  dx^{k}(\pmb{A}) & dx^{k}(\pmb{B}) & dx^{k}(\pmb{C})\end{vmatrix} = \begin{vmatrix} A^{i}& B^{i}&C^{i} \\ A^{j}&B^{j}&C^{j} \\ A^{k}&B^{k}&C^{k} \end{vmatrix}
$$
When the coordinates are cartesian the interpretation of this is similar to that before in [[Integrals and Exterior Forms]]. Take the three vectors at a given point $x$ in $\mathbb{R}^{n}$, project them down into the 3 dimensional affine subspace of $\mathbb{R}^{n}$ spanned by $\pmb{\partial}_{i},\pmb{\partial}_{j}$, and $\pmb{\partial}_{k}$ at $x$, and read off the $\pm$ the 3-volume of the parallelopiped spanned by the projections, where the $+$ sign is used only if the projections define the same orientation with the basis vectors.

Clearly any interchange of a single pair of $dx$ will yield the negative, and thus if the same $dx^{i}$ appears twice the form will vanish, similarly for any p-form. The most general 3-form is of the form 
$$
\alpha^{3} = \sum\limits_{i<j<k} a_{ijk}dx^{i}\wedge dx^{j} \wedge dx^{k}.
$$
In $\mathbb{R}^{3}$ there is only one nonvanishing 3-form, $dx^{1}\wedge dx^{2}\wedge dx^{3}$. In _cartesian_ coordinates this is the **volume form** $vol^{3}$, but in spherical coordinates we know that $dr \wedge d \theta \wedge d \phi$ does _not_ yield the Euclidean volume element, which is $r^{2}\sin \theta dr \wedge d \theta \wedge d \phi$. Note further that all $p>n$ forms in $\mathbb{R}^{n}$ vanish since there are always repeated $dx$ in each term. 

We take the **exterior product** of a p-form $\alpha$ and a q-form $\beta$, yielding $p+q$ form $\alpha \wedge \beta$ by expressing them in terms of the $dx$, using the usual algebra, except that the product of $dx$ is anticommutative, $dx \wedge dy = -dy \wedge dx$. For examples in $\mathbb{R}^{3}$ with any coordinates 
$$
\begin{gathered}
\alpha^{1}\wedge \gamma^{1} = (a_{1}dx^{1} + a_{2}dx^{2}+a^ {3}dx^{3})\wedge(c_{1}dx^{1}+c_{2}dx^{2}+c_{3}dx^{3})  \\
=\ldots(a_{2}dx^{2})\wedge(c_{1}dx^{1})+\ldots+(a_{1}dx^{1})\wedge(c_{2}dx^{2})+\ldots \\
=(a_{2}c_{3}-a_{3}c_{2})dx^{2}\wedge dx^{3} + (a_{3}c_{1}-a_{1}c_{3})dx^{3}\wedge dx^{1} + (a_{1}c_{2}-a_{2}c_{1})dx^{1}\wedge dx^{2}


\end{gathered}
$$
which in _cartesian_ has the same components of the vector product $\pmb{a}\times \pmb{c}$. Also we have 
$$
\alpha^{1} \wedge \beta^{1} = (a_{1}dx^{1}+a_{2}dx^{2}+a_{3}dx^{3}) \wedge(b_{23}dx^{2}\wedge dx^{3} + b_{31}dx^{3}\wedge dx^{1} + b_{12}dx^{1}\wedge dx^{2})
$$
$$
=(a_{1}b_{1}+a_{2}b_{2}+a_{3}b_{3})dx^{1}\wedge dx^{2}\wedge dx^{3}
$$
where $b_{1},b_{2},b_{3}\equiv b_{23},b_{31},b_{12}$ respectively. In cartesian the components of this are the dot product! The $\wedge$ product in cartesian $\mathbb{R}^{3}$ yields both the dot and cross product of vector analysis!! The dot and cross products of vector analysis have strange expressions when used with curvilinear coordinates, but the form expressions $\alpha^{1}\wedge \beta^{2}$ and $\alpha^{1}\wedge \gamma^{1}$ are always the same. Furthermore, the cross product is not associative like the wedge product is!

By counting the number of interchanges of pairs of $dx$ one can see the commutation rule 
$$
\boxed{\alpha^{p}\wedge \beta^{q} = (-1)^{pq}\beta^{q}\wedge \alpha^{p}}
$$

