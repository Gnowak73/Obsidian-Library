---
tags: integration, Math, indefinite_integral, second_fundamental_theorem_of_calculus, calculus, theorem, bounds
dg-publish: true
mathLink: 
---
Subject: _Integration Technique_
Main\_Topic: _Changing Indefinite Integral into a Definite One_
Applications: _Solving Differential Equations and unique expressions of integrals, commonly used in physics_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
If we have the equation $g'(x)=f(x)$, we could solve it by integrating both sides to get
$$
\int\limits_{}f(x) \ dx + C
$$
Or, we could get rid of the constant of integration by considering the definite integral
$$
\int\limits_{a}^{x}f(t) \ dt
$$
where $a$ is arbitrary. This is because if we took the derivative of this integral, the $F(a)$ part, which would equal a constant, would be $0$. This is also known as the _Second Fundamental Theorem of Calculus_. We could also use some trickery to cancel out the factor from the new bounds we have introduced:
$$
\int\limits_{a}^{x}f(t) \ dt + F(a)
$$
Integrating with a definite integral on both sides allows us to also find ways to solve differential equations without dealing with the Integration Constants like in [[Wave Equation D'Alambert]]. 