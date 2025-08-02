---
tags: Math, PDE, theorem, technique
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _Method of Characteristics_
Applications: _Solving First order PDEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]_
Closely\_Related\_To: _None_
_
_
![[Pasted image 20230624192100.png|center]]
The Method of Characteristics is an important method used to solve linear, non-linear, and semi-linear PDEs of the first order. We can solve PDEs by mapping where the derivatives in the equation are pointing over intervals in order to map how the slope of the solution must behave. From this information, we can then deduce the solution at play. 

---
##### Transversality Condition
The transversality condition is a condition that the initial data given to solve the PDE is not along the characteristics. This results in either no solution or an infinite number of solutions since our method to solve the problem relies on us finding the intersection between the characteristics and the initial data; thus, we need them to intersect at a point only once to get a well-defined problem.

Therefore, the tangent vector of the characteristics cannot create a parallelogram of $0$ area with the initial data because this would result in them being parallel.

Since the characteristic vectors by definition are given by (if we parameterize the initial data by $\tau$) 
$$
\left<a(x_{0}(\tau),y_{0}(\tau)), b(x_{0}(\tau),y_{0}(\tau)\right>
$$
for an equation similar to
$$
au_{x}+bu_{y}=0
$$
We can write the condition for a non-zero area parallelogram: 
$$
det \begin{bmatrix} a(x_{0}(\tau),y_{0}(\tau)) &x_{0}'(\tau)\\ b(x_{0}(\tau),y_{0}(\tau)) & y_{0}'(\tau)\end{bmatrix} \neq 0
$$
and this is our condition that must be met. 


### The Characteristic Equations
$$
\begin{cases} \dot{\pmb{x}}(s) = \nabla_{p} F(\pmb{p}(s),z(s),\pmb{x}(s)), \\ \\

\dot z(s) = \nabla_{p}F(\pmb{p}(s),z(s),\pmb{x}(s))\cdot \pmb{p}(s),\\ \\

\dot{\pmb{p}}(s) = -\nabla_{x}F(\pmb{p}(s),z(s),\pmb{x}(s)) - \frac{\partial F}{\partial z}(\pmb{p}(s),z(s),\pmb{x}(s)) \pmb{p}(s) \\
\end{cases}

$$

If you are working with a semi-linear or linear first order equation, you will not have a $\pmb{p}$ vector, simplifying this much further. 