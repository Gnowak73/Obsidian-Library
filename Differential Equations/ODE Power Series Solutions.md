---
tags: Math, ODE, Series, Power Series, Taylor Series
dg-publish: true
mathLink: 
---
Subject: _ODE_
Main\_Topic: _ODE Power Series Solutions_
Applications: _Solving Nonlinear or Non-elementary ODEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

Power Series can be used to solve differential equations which don't have constant coefficients or are pretty non-elementary. To solve such equations, we assume that there is a series solution
$$
y=\sum\limits_{n=0}^{\infty} c_{n}x^{n}
$$
associated with this ODE which we assume converges on the interval $I$ which our ODE exists. We then take the derivative of this function to get 
$$
y' = \sum\limits_{n=1}^{\infty}c_{n}nx^{n-1}
$$
the reason the index moves forward by 1 is because the first term in the power series will be $0$ since $\frac{d}{dx}c_{n}=0$.  We do this again to get 
$$
y'' =\sum\limits_{n=2}^{\infty}c_{n}n(n-1)x^{n-2}
$$
and we plug this into our ODE. Once doing this, we can reindex our sums in order to get one sum that equals $0$. This allows us to set what is inside the sum to $0$ and use a recursive relationship to write a power series solution which we can attribute to a function via [[Taylor Series]].