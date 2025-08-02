---
tags: Math, Multivariable, theorem, Integrals, Line_Integrals, technique 
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Fundamental Theorem of Line Integrals_
Applications: _Line Integral Technique_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
The Fundamental Theorem of Line Integrals is a theorem that relates Path-Dependence to Conservative Functions in [[Line Integrals]]. Say we have a open, connected, smooth, simple curve/path $C$, then 
$$
\int_{C}\vec{\nabla}f \cdot d\vec{r} = f(\vec{r}(a))-f(\vec{r}(b))
$$
where $a$ and $b$ are the endpoints of the path $C$. Thus, if we are able to find the function that a line integral function is the gradient of, we can then just plug in the end points of the path into that new function. Where
$$
\vec{F}=\nabla \vec{f}
$$
How do we prove a such a function $\vec{f}$ exists? if $\vec{F}$ is a <mark style="background: #BBFABBA6;">conservative vector field</mark>, then there is a potential function $f$.  

#### Checking if Vector Field is Conservative:
The condition must be followed:
$$
\nabla \times \vec{F} = 0 
$$
