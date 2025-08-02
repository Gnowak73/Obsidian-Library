
---
tags: Math, ODE, theorem, derivation 
dg-publish: true
mathLink: 

---
Subject: _ODE_
Main\_Topic: _ODE First Order Methods_
Applications: _Solving First Order ODEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

This article will cover the basic techniques used to solve 1st order ODEs. 


### Separation of Variables:  Y' = f(x)g(y)   
If an ODE can be manipulated such that it can be put into a form of 
$$
f(x) \ dx = g(y) \ dy
$$
where $f(x)$ and $g(y)$ are just arbitrary functions from the differential equation, then both sides can be integrated such that 
$$
\int\limits f(x) \ dx = \int\limits f(y) \ dy
$$
and we can solve the ODE.

---

### Integrating Factor:  Y' + p(x)y = q(x) 
The integration factor can be used to solve equation of the form 
$$
\frac{dy}{dx} + p(x)y=q(x)
$$
by using an integrating factor, $\rho = e^{\int\limits p(x) \ dx}$, which we multiply to both sides of the ODE. In doing so, we are left with the equation:
$$
\frac{dy}{dx}e^{\int\limits p(x) \ dx} + e^{\int\limits p(x) \ dx}p(x)y=q(x)e^{\int\limits p(x) \ dx}
$$
which can be simplified to 
$$
\frac{d}{dx}\left[e^{\int\limits p(x) \ dx} y\right] = q(x)e^{\int\limits p(x) \ dx}
$$
Now, we can integrate both sides to get:
$$
y(x) = e^{-\int\limits p(x) \ dx}\left(\int\limits q\left(x\right)e^{\int\limits p(x) \ dx} \ dx\right) + C
$$
For initial value problems, we can include the initial data in the integral such that we don't have to deal with the constant $C$. We do this by instead writing
$$
\begin{gathered}
\rho(x) = e^{\int\limits_{x_{0}}^{x} p(t) \ dt} \\
y(x) = \frac{1}{\rho(x)}[y_{0}+\int\limits_{x_{0}}^{x}\rho(t)q(t) \ dt]
\end{gathered}
$$

---

### Exact Equations:  F(x, y(x)) = C,   M dx + N dy = 0
If we have an implicit equation of the form
$$
F(x,y(x)) = C,
$$
where $C$ is a constant, then if we differentiate both sides with respect to $x$, we get the differential equation:
$$
\frac{dF}{dx} =  \frac{\partial F}{\partial x} +  \frac{\partial F}{\partial y} \frac{dy}{dx} = 0
$$
That is,
$$
M(x,y) \ dx + N(x,y) \ dy = 0.
$$
Where $M=F_{x}$ and $N=F_{y}$. Since partial derivatives have symmetry (Clairaut's theorem), then we can write 
$$
\frac{\partial M}{\partial y} = F_{xy}=F_{yx}= \frac{\partial N}{\partial x}
$$
Thus, we can solve this ODE with the conditional equation:
$$
\frac{\partial M}{\partial y} =\frac{\partial N}{\partial x}
$$
(which looks similar to the curl...) Either way, we can use this equation to solve the ODE for the function
$$
F(x,y(x)) = C
$$
>(don't forget the $C$!)


---

## Substitution Methods:   Y' = f(x, y)
For a differential equation of the form 
$$
\frac{dy}{dx}= f(x,y)
$$
we may have to substitute with a dummy variable in order to transform such an equation into one we already know how to solve. The most notable forms of substitution will be given below:

###  1.   Homogenous Equations: Y' = F$\left(\frac{y}{x}\right)$  
If we make the substitution 
$$
v=\frac{y}{x}, \ y=vx, \ \frac{dy}{dx}=v+x \frac{dv}{dx}
$$
then we can simplify an equation of form
$$
\frac{dy}{dx} = F\left(\frac{y}{x}\right)
$$
into the separable equation 
$$
x \frac{dv}{dx}= F(v) - v
$$

### 2.   Bernoulli Equations: Y' + p(x)y = q(x)$y^{n}$ 
An ODE of the form 
$$
\frac{dy}{dx} + P(x)y = Q(x)y^{n}
$$
is known as a Bernoulli Equation. If either $n=0$ or $n=1$, then the ODE is linear. If it is not, we do the substitution
$$
v=y^{1-n}
$$
which transforms our ODE into 
$$
\frac{dv}{dx} + (1-n)P(x)v = (1-n)Q(x)
$$

### 3.   Reducible Second-Order ODE:   F(x,y,y',y'') = 0
If we have an ODE of the form 
$$
F(x,y,y',y'')=0
$$
we may be able to make a substitution of something like $p=y'$ in order to get a first order ODE. Usually, if the dependent variable $y$ is missing from $F$ in the ODE or the independent variable $x$, we can reduce the ODE. In most cases though, this does not work, and [[ODE Second Order Methods]] must be used. 