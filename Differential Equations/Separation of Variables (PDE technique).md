---
tags: Fourier_Series, Math, PDE
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _Separation of Variables_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]_
Closely\_Related\_To: _None_
_
_


A technique where we rewrite a function as the multiplication of two different functions depending on only one variable of the original multivariate function in order to solve or simplify a partial differential equation (PDE). 

example:
$$
F(x,t) = X(x)T(t)
$$


This results in a Second Order derivative eigenvalue problem for second order, linear partial differential equations ([[Function Linear Algebra#Linear Transformations | Linear Transformations]], [[Vector Linear Algebra#Eigenvalue Problem |Eigenvalue Problem]]). Because the partial differential equation is linear, then we can write a general solution as the infinite sum of solutions. And by the solutions being Sine and Cosine (an orthogonal basis), we can write the constant coefficients from our differential equation solution using [[Function Linear Algebra#Fourier Series |Fourier Series]]. 
```ad-tip
It is important though, to note that for boundary conditions, one must be very careful! The boundary conditions must be taken into account, and if they are not homogenous, then the solutions may not be able to be written as an infinite sum!
```

**Homogeneity of boundary conditions (i.e. the 0's) allows a linear combination to also satisfy the boundary conditions**



