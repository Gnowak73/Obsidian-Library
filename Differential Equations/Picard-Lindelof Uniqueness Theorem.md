---
tags: Math, ODE, PDE, theorem, Linear_Algebra
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _Picard-Lindelof Uniqueness Theorem_
Applications: _PDEs and ODEs uniqueness theorem in solutions_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
This statement is: identical initial conditions implies identical solutions in an ODE or a PDE. 

This allows us to generalize statements about PDEs and ODEs for unique solutions. This is most easily seen by casting a <mark style="background: #BBFABBA6;">LINEAR</mark> ODE in a linear algebra matrix form $X' = AX$, in which there will be unique constants defining the solution for the initial condition. And these constants uniqueness imply that there is only one unique function to solve the ODE on an interval. 

#### Why there are only N Linearly Independent Solutions to an N-th order Linear ODE ?
Such a theorem explains why the linear independence of solutions to an ODE implies generality. If we choose a point $a$ in an interval $I$, and consider the simultaneous equations:
$$
\begin{gathered}
c_{1}y_{1}(a)+c_{2}y_{2}(a) = Y(a) \\
c_{1}y'_{1}(a)+c_{2}y'_{2}(a) = Y'(a)
\end{gathered}
$$
then the determinant of the coefficients in this system of linear equations in the unknowns $c_{1}$ and $c_{2}$ is simply the [[linear independence|Wronskian]] evaluated at $x=a$. By linear algebra, we know that this determinant can't be $0$ in order to solve this system for two unique solutions. Therefore, by the [[ODE Second Order Methods#Linear Independence and Wronskian of Solutions|Theorem of Wronskain of ODE solutions]],  these two functions $y_{1}$ and $y_{2}$ must linearly independent. And we know from the Uniqueness Theorem that any function with the same initial conditions is the same function, so the only function that can solve the ODE's Initial Value Problem is from $c_{1}y_{1}+c_{2}y_{2}$. 

We can't have more functions than this because it creates a redundancy in the system of equations unless there is an additional initial condition which includes $y''(0)$, but our equation already tells us about $y''(0)$ since the equation itself is describing $y''(x)$. Thus, we only need two initial conditions to describe the evolution of a system. And thus we will only have two unique solutionsl  