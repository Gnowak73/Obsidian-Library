---
tags: differentiability, Math, derivative, conditions, theorem
dg-publish: true
mathLink: 
---
Subject: _Differentiability Conditions_
Main\_Topic: _Differentiability Conditions for All Dimensions_
Applications: _Conditions for the ability to take a Derivative_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
```ad-Remember
The definitions for derivatives seems to simply come down the the discretion of the mathematician, some even go as far as arguing for stricter rules for differentiation or even differentiation at end points. What we state here is simply a matter of definition, but we try to do so in a matter which we expand from, not retract. These definitions below are general in this manner.
```

##### Derivatives - Rules for all Dimensions?
Requiring that the function is defined on an open ball forces the object that you get out as the (total) derivative is a linear approximation in _all_ directions from the point $x$ (or $z$). Allowing derivatives for functions not defined on an interval is basically just restricting the possible directions for your derivative to approximate in - with the derivative for an isolated point being $0$, since there are no "directions".

Also note that if you don't require definition on an open ball, then you can take derivatives at discontinuities, which will break the nice formulas we learn in calculus for computing derivatives of combinations of functions in the larger space.

So, function _must_ be defined in a neighborhood.

A function _must_ be defined in a neighborhood to be continuous or differentiable.

A function also _cannot_ be differentiable on the boundary of its domain, it can only be differentiable in the interior of its domain. This is because the function must be approachable from all directions.


Some assumptions given aren't quite needed, but may allow stronger assumptions to be made for proofs.

---
##### Differentiability Conditions for Single-Variable
For single-variable functions, _continuity_ implies differentiability. A function must also be defined in a neighborhood to be differentiable. 

**Pathological:**  We _do not_ need a function to be continuous in a neighborhood to be differentiable at a point (differentiability at a point only needs continuity on that one specific point). We also _do not_ need a function to be differentiable in a neighborhood to be differentiable. 

A function _must be_ defined in a neighborhood to be continuous at a point though!

```ad-Definition
If we have a continuous function $f$ such that 
$$
\lim_{x \rightarrow a} f(x) = f(a),
$$
then the derivative is defined as 
$$
\lim_{x \rightarrow a} \frac{f(x)-f(a)}{x-a}$$
```


##### Differentiability Conditions for Multivariate
A function must be continuous and have continuous partial derivatives on an open region to be differentiable on that region. These partial derivatives must also be continuous on this open region. A function must also be defined in a neighborhood to be differentiable.

Also note that limits in the multivariable plane must be the same no matter which direction you approach from. 

**Pathological:**  A multivariate function can be discontinuous and still have partial derivative. A function does not need to be continuous in a neighborhood to be differentiable at a point (differentiability at a point only needs continuity on that one specific point). We also _do not_ need a function to be differentiable in a neighborhood to be differentiable. 

```ad-Definition
A partial derivative is defined by the limit 
$$
 \left. \frac{\partial f}{\partial x}\right\rvert_{(x_{0},y_{0})} = \lim_{h \rightarrow 0} \frac{f(x_{0}+h,y_{0})-f(x_{0},y_{0})}{h}
$$
```
