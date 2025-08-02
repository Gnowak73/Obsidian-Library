---
tags: derivative, Complex, Math, analytic, analytic_functions, Laplace, Laplaces_equation, Equation
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Harmonic Functions_
Applications: _Applied Mathematics, Many potentials(like the electrostatic) and temperatures are modeled with Harmonic Functions_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
```ad-Definition
A real-valued function $H$ of two real variables $x$ and $y$ is said to he _Harmonic_ in a given domain of the $xy$ plane if, throughout that domain, it has [[Complex Continuity|continuous]] partial derivatives of the first and second order and satisfies the PDE
$$
H_{xx}(x,y)+H_{yy}(x,y)=0,
$$
Known as _Laplace's Equation_. 
```

Harmonic functions show up in temperatures in thin planes and with electrostatic potentials that vary with $x$ and $y$. 

**Theorem.**  If a function $f(z)=u(x,y)+iv(x,y)$ is analytic in a domain $D$, then its component functions $u$ and $v$ are harmonic in $D$. 
**Proof:**  If we take the [[Complex Derivatives#Cauchy Riemann Equations|Cauchy-Riemann Equations]] 
$$
u_{x}=v_{y}, \quad u_{y}=-v_{x}
$$
and we differentiate both sides with respect to $x$
$$
u_{xx}=v_{xy}, \quad u_{yx}=-v_{xx}
$$
and likewise with respect to $y$
$$
u_{xy}=v_{yy}, \quad u_{yy}=-v_{xy}
$$
Due to <mark style="background: #FF5582A6;">Clairaut's theorem</mark> (symmetry of partial derivatives), we can combine these two sets of equations to get: 
$$
u_{xx}+u_{yy}=0, \quad v_{xx}+v_{yy}=0
$$
**Remark.** With this theorem, the converse is also true. In other words, if given knowledge that some function $u$ is Harmonic, then there must exist a corresponding function $v$, which satisfies the Cauchy-Riemann Equations such that we can create an analytic function by $f(z)=u+iv$.

---
##### Converse Example
$u(x,y)=\ln{(x^2+y^2)}$. We start by showing that $u(x,y)$ is harmonic by checking via Laplace's equation ($u_{xx}+u_{yy}=0$):
$$
\begin{equation}
    \begin{aligned}
        u_{xx}&=\left(\frac{2x}{(x^2+y^2)}\right)_x=\frac{y^2-x^2}{(x^2+y^2)^2}, \\
        u_{yy}&=\left(\frac{2y}{(x^2+y^2)}\right)_y=\frac{x^2-y^2}{(x^2+y^2)^2}, \\
    \end{aligned}
\end{equation}
$$
$$
\begin{equation}
    \begin{aligned}
        u_{xx}+u_{yy}=\frac{y^2-x^2}{(x^2+y^2)^2} + \frac{x^2-y^2}{(x^2+y^2)^2} = 0.
    \end{aligned}
\end{equation}
$$
Using the Cauchy-Riemann equations:
$$
\begin{equation}
    \begin{aligned}
        \left\{\begin{aligned} u_x&=v_{y} \\
                u_{y}&=-v_x
                \end{aligned}
        \right . , \quad f^{'}(z)=u_x+iv_x,
    \end{aligned}
\end{equation}
$$
$$
\begin{equation}
    \begin{aligned}
        u_x=\frac{2x}{x^2+y^2}=v_y 
    \end{aligned}
\end{equation}
$$
$$
\begin{equation}
    \begin{aligned}
        v=\int{\frac{2x}{x^2+y^2} dy} = 2x \int{\frac{x\sec^2(\theta)}{x^2\sec^2(\theta)}d\theta} = 2\theta + C(x) = 2\arctan\left(\frac{y} {x}\right) + C(x)
    \end{aligned}
\end{equation}
$$
Now, we use the other equation,
$$
\begin{equation}
    \begin{aligned}
        v_x=\frac{2}{1+(y/x)^2}\times \frac{-y}{x^2} +C'(x) = \frac{-2y}{x^2+y^2}+C'(x) = -u_y = \frac{-2y}{x^2+y^2}
    \end{aligned}
\end{equation}
$$
$$
\begin{equation}
    \begin{aligned}
        C'(x)=0
    \end{aligned}
\end{equation}
$$
$$
\begin{equation}
    \begin{aligned}
        C(x)=C
    \end{aligned}
\end{equation}
$$
Now, we have
$$
\begin{equation}
    \begin{aligned}
        \boxed{v(x,y)=2\arctan\left(\frac{y}{x}\right)+C}
    \end{aligned}
\end{equation}
$$
For an arbitrary harmonic conjugate, we can just let $C=0$, such that 
$$
\begin{equation}
    \begin{aligned}
        \boxed{u(x,y)=\ln(z\overline{z}), \quad v(x,y)=2\arctan{\left(\frac{z-\overline{z}}{i(z+\overline{z})}\right)}}
    \end{aligned}
\end{equation}
$$
Thus,
$$
\begin{equation}
    \begin{aligned}
        f(z) = \ln(z\overline{z}) + 2\arctan{\left(\frac{z-\overline{z}}{i(z+\overline{z})}\right)}i, \quad f'(z) = \boxed{\frac{z+\overline{z}}{z\overline{z}} + \frac{-z+\overline{z}}{z\overline{z}}=\frac{1}{z} }
    \end{aligned}
\end{equation}
$$
