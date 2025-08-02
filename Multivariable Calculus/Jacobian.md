---
tags: Math, Multivariable, Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Jacobian_
Applications: _Integral Change of Variables technique_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
The Jacobian is a matrix that determines the scalar changes in area between one coordinate system and another. It is especially important in the change of variables for multivariate integration. In a sense, its determinant kind of a proportionality constant between metrics! We use this in integrals when doing a change in variables for multivariate functions. 

$$
\pmb{J} = \frac{\partial(f_1,\ldots,f_n)}{\partial(x_{1},\ldots,x_{n})} = \begin{bmatrix}  \frac{\partial f_{1}}{\partial x_{1}} & \ldots &  \frac{\partial f_{1}}{\partial x_{n}} \\ \vdots  & \ddots & \vdots\\  \frac{\partial f_{n}}{\partial x_{1}} & \ldots &  \frac{\partial f_{n}}{\partial x_{n}} \end{bmatrix}
$$
From cartesian to polar coordinates:
$$
\pmb{J}(\rho ,\phi,\theta) = \frac{\partial(x,y,z)}{\partial(\rho,\phi,\theta)} = \begin{bmatrix} \sin\phi\cos\theta & \rho\cos\phi\cos\theta & -\rho\sin\phi\sin\theta \\\sin\phi\sin\theta &\rho\cos\phi\sin\theta & \rho\sin\phi\cos\theta \\ \cos\phi & -\rho\sin\phi & 0 \end{bmatrix} 
$$
The determinant of this matrix would be $\rho^{2}\sin\phi$, which would be included in the integral if a change of coordinates happened. For example:
$$
\int\limits f(x,y) \ d(x,y) = \int\limits f(r,\theta) \times|J(r,\theta)| \ d(r,\theta)
$$
except this would be polar. 