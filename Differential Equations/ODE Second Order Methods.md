---
tags: Math, ODE, theorem, derivation
dg-publish: true
mathLink: 
---
Subject: _ODE_
Main\_Topic: _ODE Second Order Methods_
Applications: _Solving Second Order ODEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[ODE First Order Methods]]_
_
_

Closely related to [[ODE First Order Methods]], we will address the methods of solving second order ODEs. Due to the mass content, this article will serve as a homepage to the methods which are linked.

Also, it is worth noting once again the principle of [[Superposition Linear ODE and PDE|Superposition]]
in these ODEs, which becomes important especially for solving inhomogeneous equations. 

Due to [[Superposition Linear ODE and PDE|Superposition]], $\mathcal{L}(u)=f(x)$ has the general solution $u=u_{1}+u_{2}$ where $u_{1}$ is the solution to the homogeneous form and $u_{2}$ is the solution to the inhomogeneous form. This is because $\mathcal{L}(u) = 1\times 0 + 1 \times f(x)$. We call the homogeneous solution the <mark style="background: #ABF7F7A6;">Complementary Solution</mark> and we call the inhomogeneous Solution the <mark style="background: #FFB86CA6;">Particular Solution</mark>. Thus, $Y(x) = y_{c}+y_{p}$ for an ODE. 

1. [[Homogeneous Linear ODE Constant Coefficient Characteristic Equations]]
2. [[Inhomogeneous Linear ODE Method of Undetermined Coefficients]]
3. [[Variation of Parameters]] 
4. [[Laplace Transforms]]
5. [[ODE Power Series Solutions]]
6. Multiplying by a nonzero velocity as in [[Pendulum Nonlinear Exact Solution]] (for nonlinear ODEs)

##### Systems of ODEs 
For systems of ODEs, one could employ multiple methods. The most notable ones are 
1. [[System of Linear ODEs Constant Coefficients]] (turning system into Eigenvalue problem)
2. You can map the variables to the complex plane and combine the coupled equations (best for a system that cannot be simplified to $X'=AX$), look at [[Projectiles and Charged Particles]] for example.  
3. Taking derivative of one equation and substituting derivative from other ODE (only works for coupled equations)

#### Linear Independence and Wronskian of Solutions
Supposed that $y_{1}$ and $y_{2}$ are two solutions of the homogeneous second order <mark style="background: #ABF7F7A6;">LINEAR</mark> ODE of the form
$$
y''+p(x)y'+q(x)y=0,
$$
then on an open interval $I$ on which $p$ and $q$ are continuous:
1. If $y_{1}$and $y_{2}$ are linearly dependent, then $W(y_{1} ,y_{2}) \equiv 0$ on $I$.
2. If $y_{1}$ and $y_{2}$ are linearly independent, then $W(y_{1},y_{2}) \neq 0$ at each point of $I$.  

We can use this with the knowledge of [[Function Linear Algebra]] and a [[Superposition Linear ODE and PDE#Solution Space|Solution Space]] to answer the question: [[Picard-Lindelof Uniqueness Theorem#Why there are only N Linearly Independent Solutions to an N-th order Linear ODE ?|Why are there only N linearly Independent Solutions to an N-th order Linear ODE]].  

