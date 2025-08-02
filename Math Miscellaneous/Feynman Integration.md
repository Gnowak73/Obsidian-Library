---
tags: Math, Integrals, technique
dg-publish: true
mathLink: 
---
Subject: _Integral Techniques_
Main\_Topic: _Feynman Integration_
Applications: _Solving Integrals_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Leibniz Integral Rule]]_
_
_

This integration technique is used when we would like to be able to change one little thing in the integrand in order for things to work out nicely. The procedure is as follows:

1. set the integral equal to a function of some parameter $\alpha$, where $\alpha$ is placed in the integral where the derivative of the integral with respect to $\alpha$ will give you the change you want
2. Differentiate the function with respect to $\alpha$ using [[Leibniz Integral Rule]]
3. Integrate result to get original $f(\alpha)$
4. Create initial condition to solve for Integration Constant $C$
5. Plug in the value of $\alpha$ you would've needed for your original integral to be the same

#### Example 
Lets say we have the integral 
$$
\int\limits_{0}^{1}\frac{t^{3}-1}{\ln(t)} \ dt
$$
Now, this logarithm is ugly and ruins this integral. But is there one little change we could make to get rid of it? If we take the derivative of $t^{x}-1$ we would have $t^{x}\ln(t)$ which would cancel out the $\ln(t)$ in the denominator. Thus, we assume the function
$$
f(\alpha) = \int\limits_{0}^{1}\frac{t^{\alpha}-1}{\ln(t)} \ dt
$$
where $\alpha=3$ gives us our original integral. 

We now differentiate both sides using [[Leibniz Integral Rule]] to get:
$$
\begin{gathered}
f'(\alpha) = \int\limits_{0}^{1} \frac{\partial}{\partial \alpha} \left(\frac{t^{\alpha}-1}{\ln(t)}\right)\ dt = \int\limits_{0}^{1}\frac{\ln(t)t^{\alpha}}{\ln(t)}\ dt = \int\limits_{0}^{1}t^{\alpha}\ dt = \left. \frac{t^{\alpha+1}}{\alpha+1}\right\rvert_{0}^{1} \\
= \frac{1}{\alpha+1}

\end{gathered}
$$
Now, if we integrate both sides with respect to $\alpha$ we get 
$$
f(\alpha) = \ln (\alpha+1 )+C
$$
where $C$ is a constant. If we were to plug in $f(0)$ into our original function, we get 
$$
f(0) = \int\limits_{0}^{1}0 \ dt = 0
$$
which we can use to fix this constant factor $C$ and solve for it:
$$
f(0) = 0 = \ln(1)+C = C
$$
Thus, $C=0$ and we have the equation
$$
f(\alpha) = \ln (\alpha+1)
$$
For $\alpha=3$, we get 
$$
f(3) = \boxed{ \ln (4)}
$$