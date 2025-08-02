---
tags: Math, Complex, Contours, parametrization, curves, Jordan_curve, Jordan_Theorem, theorem, Tangent, Normal, Arc
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Contours_
Applications: _Contour Integrals, Curves on the Complex Plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Contour Integrals]],[[Complex Derivatives]]_
Cont.\_ of: _None_ 
_
_
Integrals of complex-valued functions of a _complex_ variable are defined on curved in the complex plane, rather than on just intervals of the real line. Classes of curves that are adequate for the study of such integrals are introduced in this section.

```ad-Definition
A set of points $z=(x,y)$ in the complex plane is said to be an _arc_ if 
$$
x=x(t), \quad y=y(t), \quad (a\leq t\leq b),
$$
where $x(t)$ and $y(t)$ are continuous functions of the real parameter $t$. This definition establishes a continuous mapping of the interval $a\leq t\leq b$ into the $xy$ plane, or $z$ plane; and the image points are ordered according to increasing values of $t$. It is convenient to describe the points of $C$ by means of the equation
$$
z=z(t), \quad (a\leq t\leq b),
$$
where
$$
z(t)=x(t)+iy(t).
$$

The arc $C$ is a **simple arc**, or a **Jordan Arc**, if it does not cross itself. If we have $z(a)=z(b)$, we say that $C$ is a **simple closed curve** or a **Jordan Curve**. Such as curve is _positively oriented_ in the CCW (counter-clockwise) direction.
```

For example, if we wanted to have an arc that represented a counterclockwise circle centered at some point $z_{0}$, we would have:
$$
z=z_{0}+Re^{i\theta,}\quad (0\leq\theta\leq2\pi)
$$

The parametric representation used for any given arc $C$ is not unique. It is, in fact, possible to change the interval over which the parameter ranges to any other interval. 

Now, suppose that we had the components $x'(t)$ and $y'(t)$ such that 
$$
z'(t)=x'(t)+iy'(t)
$$
is used to represent $C$. Then, if these components are continuous on the entire interval $a\leq t\leq b$, the arc is called a _differentiable arc_, and the real-valued function
$$
|z'(t)| = \sqrt{[x'(t)]^{2}+[y'(t)]^{2}}
$$
is integrable over the interval $a\leq t\leq b$. In fact, according the the definition of [[Arclength]], the length of the Contour $C$ is 
$$
L=\int\limits_{a}^{b}|z'(t)|\ dt
$$
**Remark.**  The value of $L$ is invariant under certain changes in the representation for $C$ that is used. 

We can actually write the unit tangent vector ([[Tangent and Normal Vectors]]) 
$$
\hat {\pmb{T}} =\frac{z'(t)}{|z'(t)|}
$$
as long as $z'(t)$ is well-defined, continuous, and nonzero on the interval which we parametrized our arc $C$. 

```ad-Definition
A **Contour**, or _piecewise smooth arc_, is an arc consisting of a finite number of _smooth arcs_ joined end to end. Hence, $z(t)$ is piecewise continuous. The length of a contour or a simple closed contour is the sum of the lengths of the smooth arcs that make up the contour.

The points on any simple closed curve or simple closed contour $C$ are boundary points of **two distinct domains**, one of which is the _interior_ of $C$ and is _bounded_. The other, which is the _exterior_ of $C$, and is _unbouned_. It will be convenient to accept this statement, known as the **Jordan curve Theorem**, as geometrically evident; (not easy proof).
```
