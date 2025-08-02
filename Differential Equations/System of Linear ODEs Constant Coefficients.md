---
tags: Math, ODE, Linear_Algebra, technique, 
dg-publish: true
mathLink: 
---
Subject: _ODE_
Main\_Topic: _System of  Linear ODEs Constant Coefficients_
Applications: _Solving mechanical/coupled systems_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Vector Linear Algebra]]_
_
_
Lets say we take our knowledge from [[ODE Second Order Methods]], specifically from the [[Homogeneous Linear ODE Constant Coefficient Characteristic Equations|characteristic equation]]. We suspect that for a system (linear system) of ODEs (with constant coefficients) we would have solutions of the form
$$
\pmb{x}(t) = \begin{bmatrix}x_{1} \\ x_{2}\\x_{3}\\\vdots\\x_{n}\end{bmatrix} = \begin{bmatrix}v_{1}e^{\lambda t}\\v_{2}e^{\lambda t}\\v_{3}e^{\lambda t} \\ \vdots \\v_{n}e^{\lambda t}\end{bmatrix} = \pmb{v}e^{\lambda t}
$$
as we once did before. If we substitute this into an ODE
$$
x'=Ax
$$
the exponentials would cancel and we have the equation
$$
A\pmb{v}=\lambda \pmb{v}
$$
, a similar result we can for the characteristic equation! So... in principle, we solve this equation and then plug these values of $\pmb{v}$ and $\lambda$ into our general solution formula and sum them. But how do we solve this equation? Well, we see that it is indeed an [[Vector Linear Algebra#Eigenvalue Problem|Eigenvalue Problem]] ! 

We can solve this eigenvalue problem and then add the solutions together for our generalized solution to the system of ODEs now.

The same principles from single ODEs still applies, except our characteristic equation is an eigenvalue problem and we have eigenvectors in front of the exponentials as a way to cater specific constants to specific ODEs in the system. 

For second order systems, we have 
$$
\pmb{x}'' = Ax,
$$
in which we would have the eigenvalue problem
$$
\alpha^{2}\pmb{v}=A\pmb{v}
$$
Thus, we just solve the eigenvalue problem and take $\lambda =\alpha$ when doing $\pmb{x}=\pmb{v}e^{\lambda t}$. This usually results in complex eigenvalues, but using Euler's formula once again we can get around that.  

##### Complete Set of Eigenvalues
When solving the eigenvalue equation, if we can create a set of [[linear independence|linearly independent]] eigenvectors, then we call it a <mark style="background: #FFF3A3A6;">Complete Set</mark>; this usually only can happen if there are no repeated roots or if the repeated roots can have arbitrary eigenvectors. If we cannot do that, then we need a way to get a complete set, since if the eigenvectors are not linearly independent, our solution has a redundancy and is missing a set of linearly independent solutions. 

Lets explore the case when there is a multiplicity of 2. If there is, and we only have one linearly independent eigenvector for this eigenvalue, we have a single solution $\pmb{x}_{1}(t)=\pmb{v}_{1}e^{\lambda t}$. If we, by analogy, try to find a second solution of the form $\pmb{x}=\pmb{v}_{2}te^{\lambda t}$. Substituting this into an system $\pmb{x}'=A\pmb{x}$ gives us:
$$
\pmb{v}_{2}e^{\lambda t} + \lambda\pmb{v}_{2}te^{\lambda t} = A\pmb{v}_{2}te^{\lambda t}
$$
which doesn't work since we need to equate the coefficients of the $e^{\lambda t}$ parts and the $te^{\lambda t}$ parts; thus, the only solution is $\pmb{v}_{2}=0$, or $\pmb{x}=0$.

Instead, we now try a different solution form: $\pmb{x}=(\pmb{v}_{1} t + \pmb{v}_{2})e^{\lambda t}$. This results in
$$
\pmb{v}_{1}e^{\lambda t}+\lambda\pmb{v}_{1}te^{\lambda t}
+\lambda\pmb{v}_{2}e^{\lambda t} = A\pmb{v}_{1}te^{\lambda t} +A\pmb{v}_{2}e^{\lambda t}
$$
If we equate the coefficients of the different exponential parts, we get the two equations 
$$
\begin{gathered}
(A-I\lambda )\pmb{v}_{1}=\pmb{0} \\
(A-I\lambda)\pmb{v}_{2}=\pmb{v}_{1}
\end{gathered}
$$
which we can solve for our eigenvectors! Now, one eigenvalue would have solutions $\pmb{x} = \pmb{v}_{1}e^{\lambda t}$ and $\pmb{x} = (\pmb{v}_{1}t+\pmb{v}_{2})e^{\lambda t}$. So, similar to our single ODE solution but not quite exactly the same. We can actually substitute the $\pmb{v}_{2}$ equation into the first one, giving
$$
(A-I\lambda)^{2}\pmb{v}_{2}=\pmb{0}
$$
just make sure to check that 
$$
(A-I\lambda)\pmb{v}_{2}=\pmb{v}_{1}
$$
at the end. 

###### Generalization
We can generalize this method for any multiplicity of "deficient" or incomplete eigenvalues. In order to make sure the derivative of the $t^{k}$ exponent being multiplied gets canceled out, we have a coefficient in the front of the $\pmb{v}_{i}$ (same as what you'd get if you integrated the term before). You'll see what I mean:
$$
\boxed{
\begin{gathered}
\pmb{x}_{1}(t) = \pmb{v}_{1}e^{\lambda t} \\
\pmb{x}_{2}(t) = (\pmb{v}_{1}t+\pmb{v}_{2})e^{\lambda t} \\
\pmb{x}_{3}(t)= \left(\pmb{v}_{1} \frac{t^{2}}{2}+\pmb{v}_{2}t+\pmb{v}_{3}\right)e^{\lambda t} \\
\vdots
\end{gathered}
}
$$
where we have the eigenvector equations 
$$
\boxed{
\begin{aligned}
(A-I\lambda)\pmb{v}_{k}&=\pmb{v}_{k-1} \neq 0 \\
&\vdots \\
(A-I\lambda)\pmb{v}_{1}&=0 \\
\end{aligned}
}
$$
where $v_{1}$ is the original linearly independent eigenvector which you create a chain off of.

###### Source term
If we have a system of ODEs with a source term, we can use a similar method to [[Inhomogeneous Linear ODE Method of Undetermined Coefficients]] where we have a complementary and a particular solution. Except now we just have the constant coefficient vectors out in front of the particular solution too. Then we can plug it into the system of ODEs and solve!

###### Not in the right form X' = Ax or X''=Ax 
For systems of ODEs we can substitute $x' = x_{3}$ and $x''=x_{4}$ etc as functions in order to get a linear system in the form we want. Then, at the end if we have an IVP we can plug everything in and solve for our constant coefficients like regular. Basically the same method as in: [[ODE First Order Methods#3. Reducible Second-Order ODE F(x,y,y',y'') = 0|Reducible Second Order ODEs]]. 