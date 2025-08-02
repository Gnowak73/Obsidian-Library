---
tags: equation, Schrodinger, QM, Hamilton-Jacobi, Matter-Waves
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Schrodinger Equation_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
An equation (originally derived from the [[Hamilton-Jacobi equation]], [[Derivation of Schrodinger Equation]]):
$$
\hat H \Psi = i\hbar\partial_t \Psi
$$
that was the first great foundation of quantum mechanics, leading into and suggesting what we call the [[The Wave Function]] ([[Probability | Probability Amplitude]]) and [[Operators]], allowing us to make measurements ([[Probability#Mean / Expectation Value| Expectation Values]] ) and predictions about the behavior of systems on the most miniature scales in the Universe. In reality, this equation represents a <mark style="background: #D2B3FFA6;">non-relativistic</mark> conservation of energy using operators. 
	We can actually see how the Schrodinger Equation is used in the derivation of the position operator: [[Expectation Values#Position Operator Changing over Time|Position Operator Changing Over Time]].

The downfall of the Schrodinger Equation is it's non-relativistic nature, which was fixed through the Dirac Equation. 

A foundational property of the Schrodinger Equation is how its Time Independent version: 
$$
\hat H \Psi = E_n \Psi
$$
can be used to find Energy Eigenvalues and $\Psi$, while the Time Dependent form is used to find the time evolution of the system. This Time Independent version can ONLY be used for stationary states (states where the probability over all space is not changing with time).

```ad-important
The Schrodinger Equation can be separated using separation of variables. This approach is typical to solving the Schrodinger Equation and separating the TISE and the TDSE. 

(The Nikiforov-Uvarov method can also be used if you can manipulate it into a hyper-geometric form.)
```

---
### Wiki Page
![[Schrödinger_equation.pdf]]

---
## Separating Schrodinger Equation

### Stationary States

States such that observables aren't changing with time: required for the Time Independent Schrodinger equation. But where does this requirement come from? Well, we can see when we separate the Schrodinger Equation.

```ad-important
The only allowed Energy Values are the Energy Eigenvalues, NOT that the only allowed States are the Energy Eigenstates.
```

### Separation of Variables 
If we take the Schrodinger Equation
$$
- \frac{\hbar^{2}}{2m} \frac{\partial^{2}}{\partial x^{2}}\Psi + V\Psi = i\hbar\partial_{t}\Psi
$$
and apply [[Separation of Variables (PDE technique)|separation of variables]] such that $\Psi(x,t)=\psi(x)f(t)$, then the Schrodinger Equation becomes 
$$
- \frac{\hbar^{2}}{2m}  \frac{\partial^{2} \psi(x)}{\partial x^{2}}f(t) + V\psi(x)f(t) = i\hbar \psi(x) \times \partial_{t}f(t) 
$$
which can be simplified to 
$$
i\hbar \frac{1}{f} \frac{df}{dt} = - \frac{\hbar^{2}}{2m} \frac{1}{\psi} \frac{d^{2}\psi}{dx^{2}} +V
$$
Since both sides are dependent on a different variable, $x$ and $t$, but are equal, then they must equal some constant. Using dimensional analysis, we see that this constant must have units of energy; thus, we let our constant variable be $E$, and proceed now with two equations:
$$
\begin{gathered}
i\hbar \frac{1}{f} \frac{df}{dt}= E \\
- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} + V\psi = E\psi
\end{gathered}
$$
We can solve this first equation to get:
$$
f(t)=e^{\frac{-iEt}{\hbar}} 
$$
Thus, we can write our general wavefunction $\Psi$ as
$$
\Psi(x,t) = \psi(x)e^{\frac{-iEt}{\hbar}}
$$
where $\psi(x)$ is found via: 
$$
- \frac{\hbar^{2}}{2m} \frac{d^{2}\psi}{dx^{2}} + V\psi = E\psi
$$
We see that one of these differential equations results in a time evolution factor and the other results in an Energy Eigenvalue problem. This result in using [[Separation of Variables (PDE technique)|Separation of Variables]] allows us to see three major things:

1. Stationary States:   looking at the probability density $|\Psi(x,t)|^{2} =\Psi^{*}(x,t)\Psi(x,t) = \psi^{*}(x)e^{\frac{iEt}{\hbar}}\psi(x)e^{\frac{-iEt}{\hbar}} = \psi^{*}(x)\psi(x) = |\psi(x)|^{2}$, we notice that the probability density isn't dependent on time. Thus, as we know from calculating expectation values:
$$
\left<Q(x,p) \right>= \int\limits\Psi^{*}\hat Q\Psi \ dx = \int\limits\psi^{*}\hat Q \psi \ dx
$$
	Thus, the expectation values of dynamic variables are not dependent on time. In other words, they do not change with time.

2. States of definite Total Energy:   Looking at the Schrodinger Equation: $\hat H \psi = E\psi$, we can see that for the [[Expectation Values|expectation value]] of the Hamiltonian we have

$$
\left<H \right>= \int\limits\Psi^{*}\hat H\Psi \ dx = E \int\limits|\psi|^{2}\ dx
$$
(where the normalization of $\Psi(x,t)$ entails the [[Probability#Normalization|normalization]] of $\psi(x)$ as previously discussed in 1. 

3. The general solution is a linear combination of separable solutions due to the linearly of the Schrodinger Equation:
$$
\Psi(x,t) = \sum\limits_{n=1}^{\infty}c_{n}\Psi_{n}(x)e^{\frac{-iEt}{\hbar}}
$$
```ad-Remember
 if $\Psi$ satisfies the Schrodinger Equation, so does $\Psi^{*}$ 
```
---

## Infinite Square Well 
The solution and analysis of the problem can be seen here: [[Infinite Square Well]].

---

## Quantum Harmonic Oscillator 
Due to the rigorous nature of the quantum harmonic oscillator, we shall give it it's own [[Quantum Harmonic Oscillator|page(here)]]. 