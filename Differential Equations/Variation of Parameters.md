---
tags: Math, ODE, theorem, derivation
dg-publish: true
mathLink: 
---
Subject: _ODE_
Main\_Topic: _Variation of Parameters_
Applications: _ODE solving technique_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
Variation of parameters is used when [[Inhomogeneous Linear ODE Method of Undetermined Coefficients|the method of undetermined coefficients]] cannot be used. This is especially useful when we have a source function $f(x)$ which has infinitely many [[linear independence|linearly independent]] derivatives; thus, there is no finite combination to use as a trial solution. 

The Variation of Parameters method stems from the idea that we can replace the constants in the complementary function as variable, or functions, of $x$ in such a way that
$$
y_{p}(x) = u_{1}(x)y_{1}(x)+u_{2}(x) y_{2}(x)+\ldots+u_{n}(x)y_{n}(x)
$$
is a particular solution of the inhomogeneous ODE. 

To show how this works, we will do a second order ODE such that 
$$
y_{p}=u_{1}y_{1}+u_{2}y_{2}
$$
One condition on the two functions $u_{1}$ and $u_{2}$ is that $L[y_{p}]=f(x)$, Because two conditions are required to determine the two functions, we will impose a condition of our own which will simplify the computations the most. First, we will impose that $L[y_{p}]=f(x)$. To do so, we will compute the derivatives $y_{p}'$ and $y_{p}''$. The product rule gives us 
$$
y_{p}' = (u_{1}y_{1}' +u_{2}y_{2}') +(u_{1}'y_{1}+u_{2}'y_{2})
$$
To avoid working with $u_{1}''$ and $u_{2}''$, we impose the condition that
$$
\boxed{u_{1}'y_{1}+u_{2}'y_{2}=0}
$$
Then, 
$$
y_{p} =u_{1}y_{1}'+u_{2}y_{2}' 
$$
and 
$$
y_{p}'' = (u_{1}y_{1}''+u_{2}y_{2}'')+(u_{1}'y_{1}'+u_{2}'y_{2}')
$$
But both $y_{1}$ and $y_{2}$ satisfy the homogeneous equation
$$
y''+Py'+Qy=0
$$
associated with the inhomogeneous equation we originally started with. Thus,
$$
y''_{i}=-Py_{i}'-Qy_{i}
$$
It therefore follows that
$$
y_{p}''=(u_{1}'y_{1}'+u_{2}'y_{2}')-P(u_{1}y_{1}'+u_{2}y_{2}')-Q(u_{1}y_{1}+u_{2}y_{2})
$$
when substituting $y_{i}''$ into our $y_{p}''$ equation. From this we can write
$$
y_{p}''=(u_{1}'y_{1}'+u_{2}'y_{2}')-Py_{p}'-Qy_{p}
$$
Hence, 
$$
L[y_{p}]=u_{1}'y_{1}'+u_{2}'y_{2} '
$$
which implies that 
$$
\boxed{u_{1}y_{1}'+u_{2}'y_{2}' = f(x)}
$$
Thus, we can finally say our system of equations is:
$$
\boxed{
\begin{gathered}
u_{1}'y_{1}+u_{2}'y_{2}=0 \\
u_{1}'y_{1}'+u_{2}'y_{2}'=f(x)
\end{gathered}}
$$
You may also realize that the determinant of the left side is the [[linear independence#Continuous Functions|Wronskian]], and we can use linear algebra to solve this system of equations. Doing this we can formulate:
$$
\boxed{y_{p}=\left(-\int\limits \frac{y_{2}(x)f(x)}{W(x)}\ dx\right)y_{1}(x) + \left(\int\limits\frac{y_{1}(x)f(x)}{W(x)}\ dx\right)y_{2}(x)}
$$
where $W(x)$ is the Wronskian of $y_{1}$ and $y_{2}$. 


