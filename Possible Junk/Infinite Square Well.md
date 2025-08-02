---
tags: QM, derivation, Well, Potential_Well
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Infinite Square Well_
Applications: _Particles in Small Regions of Space_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

Let us assume that there is an infinite square well:
```tikz
\begin{document}

% #1    x coordinate.
\newcommand{\vandbarrier}[1]{%
    \node[scale=2.5] at (#1, 1) {\scriptsize $V = \infty$};
    \node[scale = 3] at (#1, 0.5) {\textbf{}};%
}

% #1    x coordinate.
\newcommand{\vabove}[1]{%
    \node[scale=2.5][anchor = south] at (#1, 2) {\scriptsize $V = \infty$};%
}

\begin{tikzpicture}[scale=5.0]
    \fill[gray]
        (0, 0) rectangle (1, 2)
        (2, 0) rectangle (3, 2);

    \vandbarrier{0.5}
    \vandbarrier{2.5}
    \vabove{1}
    \vabove{2}
    \node[scale=2][anchor = north] at (1, 0)   {\scriptsize 0};
    \node[scale=2][anchor = north] at (2, 0)   {\scriptsize $L$};
    \node[scale=2][anchor = north] at (3, 0)   {\scriptsize $x$};
    \node[scale=2][anchor = south] at (1.5, 0) {\scriptsize $V = 0$};

    \draw[<->] (0, 0) to (3, 0);
    \draw[->]  (1, 0) to (1, 2);
    \draw[->]  (2, 0) to (2, 2);
\end{tikzpicture}

\end{document}
```
such that we have the Schrodinger Equation (inside of the well):
$$
\hat H \psi = E\psi \rightarrow- \frac{\hbar^{2}}{2m} \frac{\partial^{2} \psi}{\partial x^{2}} = E\psi
$$
If we make the variable substitution
$$
\kappa^{2} =  \frac{2mE}{\hbar^{2}}
$$
such that we now have 
$$
 \frac{\partial^{2} \psi}{\partial x^{2}} = -\kappa^{2}\psi
$$
We can use simple methods of solving differential equations (characteristic equation) to solve such a problem to get:
$$
\psi = c_{1}e^{-i\kappa x} + c_{2}e^{i\kappa x} = A\sin(\kappa x) + B\cos(\kappa x) 
$$
where $A$ and $B$ can be complex constants. Since $\Psi(0,t)=\Psi(a,t)=0$ results in $\psi(0)=\psi(a)=0$, $B=0$ and we are left with 
$$
\psi = A\sin(\kappa x)
$$
And since we also have the boundary condition: $\psi(a)=0$, we get the equation
$$
A\sin(\kappa a) = 0, \quad \text{or} \quad \kappa a = n\pi, \  n=\pm1,\pm2,\ldots
$$
Since the Sine function is odd, or has the property $\sin(-x) = -\sin(x)$, distinct solutions (since the negative will just be absorbed into the constant $A$) will only be for a specific sign of $n$, for simplicity we just chose them to be positive. Thus,
$$
\boxed{\kappa = \frac{n\pi}{a}, \quad \text{or} \quad \psi(x) = A\sin\left(\frac{n \pi x}{a}\right), \quad \text{and} \quad E = \frac{\hbar^{2}\kappa^{2}}{2m} = \frac{n^{2}\pi^{2}\hbar^{2}}{2ma^{2}}}
$$
**Remark.** The reason that we can't just shrink the box until we get an infinite amount of Energy is because it takes work to move the potential well, so it would take an infinite amount of work.

If we want to [[Probability#Normalization |normalize]] this solution, we then take the condition that the integral over the entire space must equal $1$ such that
$$
\int\limits_{-\infty}^{+\infty} |\Psi(x,t)|^{2}\ dx = 1
$$
We know that this integral will result in simply the normalization of the position wavefunction $\psi(x)$:
$$
\begin{aligned}
&\int\limits_{-\infty}^{+\infty} |\psi(x)|^{2}\ dx = \int\limits_{-\infty}^{+\infty} |A|^{2} \sin^{2}\left(\frac{n\pi x}{a}\right) \ dx = |A|^{2}\int\limits_{0}^{a} \frac{-\cos\left(\frac{2n\pi x}{a}\right) + 1}{2} \ dx  \\

 &= |A|^{2} \left[ - \frac{\sin\left(\frac{2\pi n x}{a}\right)}{\left(\frac{4 n \pi}{a}\right)} + \frac{x}{2} \right\rvert_{0}^{a} = |A|^{2} \left[ - \frac{\sin\left(2 \pi n\right)}{\frac{4 n \pi}{a}} + \frac{\sin(0)}{\frac{4 \ \pi n }{a}} + \frac{a}{2} - \frac{0}{2}\right] \\
 
  &= |A|^{2} \frac{a}{2} = 1, \quad \text{or} \quad A=\pm\sqrt{\frac{2}{a}}

\end{aligned}
$$
Since $A$ can have different signs, we can just chose whatever one we want, traditionally this is the positive one. Now,

$$
\psi(x) = \pm \sqrt\frac{2}{a} \sin\left(\frac{n\pi x}{a}\right)
$$
### Orthogonality
One thing we do notice is that this makes an infinite set of orthogonal wave functions. Just like as shown in [[Function Linear Algebra]], wave functions are orthogonal if the inner product of two wave functions is $0$:
$$
(\psi_m(x),\psi_{n}(x)) = 0 = \int\psi_{m}^{*}(x)\psi_{n}(x) \ dx
$$
(using the product sum formula from [[trig_cheat_sheet.pdf]]):

$$
\begin{gathered}
\int\limits_{0}^{a} sin\left( \frac{m\pi}{a}x\right)\sin\left( \frac{n\pi}{a}x\right) \ dx, \quad m\neq n, \\
 = \int\limits_{0}^{a}2 \left[\cos\left( \frac{x}{a}(m-n)\right) -\cos\left(\frac{\pi x}{a} (m+n) \right) \right] \ dx \\
 =\frac{2}{\pi} \left[ \frac{\sin((m-n)\pi)}{m-n} - \frac{\sin((m+n))\pi}{m+n} \right]=0

\end{gathered}
$$

### Fourier Sine Series
As seen before, this infinite set of wave functions creates an <mark style="background: #FFB86CA6;">orthogonal set</mark>, which we could consider a basis (\*wink \*wink... [[Function Linear Algebra#Fourier Series|Fourier Series]]). In other words, since we know that this Sine function creates an orthogonal basis and in most cases results in convergence (cases can be seen in section 11 of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf |PDE Textbook]]), we should be able to write an arbitrary function $f(x)$ as 
$$
f(x) = \sum\limits_{n=1}^{\infty}c_{n}X_{n}
$$
where $X_{n} = \pm \sqrt\frac{2}{a} \sin(\frac{n \pi x}{a})$, where we notice that the set of $\psi_n(x)$ is just the Fourier Sine Series. And using the methods in [[Function Linear Algebra#Complex Plane]] we can get the result:
$$
c_{n} = \int\limits_{0}^{a}\psi^{*}_{n}(x)f(x) \ dx
$$

### Full Solution
Remember from before, that we had the function $\Psi(x,t)=\psi(x)f(t)$; well, now that we know what $\psi(x)$ is, and we already know that $f(t)$ is just an exponential factor, we can write
$$
\Psi_n(x,t) = \psi_{n}(x)f(t)= \pm \sqrt{\frac{2}{a}}\sin\left( \frac{n\pi}{a}x\right)e^{-i\left(\frac{n^{2}\pi^{2}\hbar}{2ma^{2}}\right)t}
$$
Since each $\Psi_n(x,t)$ is a solution to a linear PDE (thus, $\psi_{1}+ \psi_2$ would still be a valid solution) where the boundary conditions are <mark style="background: #FFB86CA6;">homogenous</mark>, then the [[Superposition Linear ODE and PDE|superposition]] of our solutions must also be a solution while still following the boundary conditions! We should thus be able to write a general solution as follows:

$$
\Psi(x,t) = \sum\limits_{n=1}^{\infty}c_{n}\sqrt{\frac{2}{a}}\sin\left( \frac{n\pi}{a}x\right)e^{-i\left(\frac{n^{2}\pi^{2}\hbar}{2ma^{2}}\right)t}
$$
where $c_n$ can be figured out by using Fourier Series from $[0,a]$ with the initial value problem:
$$
\Psi(0,t) = \sum\limits_{n=1}^{\infty}c_{n}\sqrt{\frac{2}{a}}\sin\left( \frac{n\pi}{a}x\right)
$$
And as long as this initial data is either $L^{2}$ or follows some other condition (like [[Dirichlet's theorem]]) to ensure that the Fourier Series converges, then we can use the methods in [[Function Linear Algebra#Complex Plane]] to get the coefficients. Other methods to check for convergence can also be seen in [[Fourier Series Convergence Conditions]] and [[Important Derivative, Series, Limits, Integrals, and Fourier Theorems to Remember]]. 

We can also see that a condition shows up for normalization in [[Normalization Condition of General Solution]].


 