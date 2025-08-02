---
tags: Math, ODE, theorem, technique 
dg-publish: true
mathLink: 
---
Subject: _ODE_
Main\_Topic: _Inhomogeneous Linear ODE Undetermined Coefficients_
Applications: _ODE technique_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
For inhomogeneous ODEs, we must find the particular solution. One method to do this is to use the method of undetermined coefficients, where we "guess" the answer based on the source term in the ODE and then plug it into the ODE and solve for the constant coefficients. This only works for equations in the form:
$$
ay^{n}+by^{n-1}+\ldots+cy+d=f(x)
$$
where $a,b,\ldots$ are constant coefficients. 

##### General Approach
The method of undetermined coefficients applies whenever the function $f(x)$ is a linear combination or finite product of the following types of functions:
1. A polynomial
2. An exponential 
3. $\cos$ or $\sin$ 
We can summarize this as: $f(x)=P_{m}(x)(\cos(k_{1}x)+\sin(k_{2}x))e^{rx}$. 

When we apply this method, we are assuming that there is no term in $f(x)$ <mark style="background: #FFF3A3A6;">or its derivatives</mark> that solves the homogeneous equation or appears in the complementary solution $y_{c}$. In other words, $y_{p}$ and its derivatives are [[linear independence|linearly independent]] to $y_{c}$. If so, we chose $y_{p}$ to be in the same form as $f(x)$ and its sum of finite linearly independent derivatives and plug it into the ODE. If there are not a finite number of linearly independent derivatives to make a particular solution out of, we must use the [[Variation of Parameters]].

If there is duplication, then we follow the procedure: multiply the particular solution by the lowest value of $x^{s}$ in order to get rid of any duplicate terms.  

In summary, if the function $f(x)$ is of the form stated before, we take the trial solution
$$
\begin{gathered}
y_{p} = x^{s}[(A_{0}+A_{1}+\ldots+A_{m}x^{m})e^{rx}\cos(kx)+ \\(B_{0}+B_{1}+\ldots+B_{m}x^{m})e^{rx}\sin(kx)]

\end{gathered}
$$
where $s$ is the smallest integer such that there are no duplicates between $y_{p}$ and $y_{c}$.