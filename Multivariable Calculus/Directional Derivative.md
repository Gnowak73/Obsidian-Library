---
tags: Math, Multivariable, Derivative, Directional_derivative 
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Directional Derivative_
Applications: _Rate of Change in a specific direction or projected onto a unit vector_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
```ad-Definition
The _Directional Derivative_ is the projection of the derivative onto a unit vector. In other words, the rate of change along a specific vector/direction. It is defined as
$$
\nabla_{v}f(\pmb{x}) = \lim_{h\rightarrow 0} \frac{(f\pmb{x}+h\pmb{v})-f(\pmb{x})}{h} = \nabla f(\pmb{x}) \cdot \pmb{v}  
$$
```

**Remark.**  The derivative of any multivariate function is the projection of the gradient $\nabla f$ onto the velocity, or rate of change, of a curve. This is the chain rule, and if we do this for example, a function where $x,y$ are parametrized by $t$:
$$
\nabla_{v}f(x) =  \frac{\partial f}{\partial x} \frac{dx}{dt}+ \frac{\partial f}{\partial y} \frac{dy}{dt} = \nabla f \cdot X'(t)
$$
where $X$ is the curve. Now, if this "curve" was represented by a vector, or a line, such as $X(t)=(at+x_{0},bt+y_{0})$, we would get the derivative being $\nabla f \cdot \vec{v}$, where $\vec{v}$ is the vector $(a,b)$. As you may realize, this is our definition of the Directional Derivative that we have just described above. And we chose unit vectors because we want to know the rate of change in a direction, not including the length of the vector we are projecting onto. 

Using the Directional Derivative, we can actually see how the gradient $\nabla f$ is orthogonal to level curves. From this we can say

**Theorem.**  If we have a surface $g(x,y,z)=C$, we know that the gradient vector $\nabla g$ is always normal to the implicit surface $g = C$

###### Intersection of Two Surfaces
Using this theorem we can actually find out how two curves intersect. We know that the cross product of two vectors is orthogonal. Let two surfaces $F=C$ and $G=D$ have normal vectors $\hat n_{1}$ and $\hat n_{2}$ respectively. If the two surfaces are intersecting, then the line of their intersection can be said to be on both $F$ and $G$. Thus, the curve of intersection is parallel to both surfaces. In other words, it is orthogonal to the normal vectors. Since we know that the gradient is normal to the surface, then we can say: the curve of intersection must be orthogonal to $\nabla F$ and $\nabla G$. The cross product $\nabla F \times \nabla G$ produces an orthogonal vector to $\nabla F$ and $\nabla G$, then we know that $\nabla F \times \nabla G$ is our intersecting curve! 