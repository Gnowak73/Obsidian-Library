---
tags: QM, expectation_value, Ehrenfest 
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Expectation Values_
Applications: _Finding the average (expected measured values) for particular attributes of a system_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Probability#Mean / Expectation Value]]_
Cont.\_of: _[[Probability#Mean / Expectation Value]]_
_
_

### Position Operator Changing over Time 
For a particle in a state $\Psi$, the expectation value of $x$ is 
$$
\left<x \right> = \int\limits_{-\infty}^{+\infty} x\left| \Psi(x,t) \right|^{2} \ dx,
$$
The expectation value can change with time since $\Psi(x,t)$ is time dependent. To see this change, we take the derivative:
$$
\tag{1}
\begin{align*}

\frac{d \left<x \right>}{dt} &=  \int\limits_{-\infty}^{+\infty} x \frac{\partial}{\partial t} \left| \Psi(x,t) \right|^{2}\ dx \\ &=  \frac{i\hbar}{2m}\int\limits_{-\infty}^{+\infty} x  \frac{\partial}{\partial x}\left(\Psi^{*} \frac{\partial \Psi}{\partial x} -  \frac{\partial \Psi^{*}}{\partial x}\Psi\right) \ dx\\ &=  \frac{i\hbar}{2m}\int\limits_{-\infty}^{+\infty} x \   \partial\left(\Psi^{*} \frac{\partial \Psi}{\partial x}-  \frac{\partial \Psi^{*}}{\partial x} \Psi\right) 

\end{align*}
$$
Using [[integration by parts]], (1) equals
$$
\left. \frac{i\hbar}{2m}\left( x \left(\Psi^{*}  \frac{\partial \Psi}{\partial x} - \frac{\partial \Psi^{*}}{\partial x}\Psi\right)  \right) \right\rvert_{-\infty}^{+\infty} - \frac{i\hbar}{2m}\int\limits_{-\infty}^{+\infty} \left(\Psi^{*} \frac{\partial \Psi}{\partial x}- \frac{\partial \Psi^{*}}{\partial x}\Psi\right)\ dx
$$
Since $\Psi \rightarrow 0$ as $x \rightarrow \pm \infty$, this simplifies to
$$
\tag{2}
 - \frac{i\hbar}{2m}\int\limits_{-\infty}^{+\infty} \left(\Psi^{*} \frac{\partial \Psi}{\partial x} -  \frac{\partial \Psi^{*}}{\partial x}\Psi\right)dx 
$$
Once again, using [[integration by parts]] on (2), but this time only on the second portion of the integrand, we get
$$
-\frac{i\hbar}{2m}\left(\int\limits_{-\infty}^{+\infty} \Psi^{*} \frac{\partial \Psi}{\partial x} \ dx \right) + \frac{i\hbar}{2m}\left( \left. \Psi^{*}\Psi \right\rvert_{-\infty}^{+\infty} - \int\limits_{-\infty}^{+\infty}\Psi^{*} \ \partial \Psi \right)  
$$
Once again, due to $\Psi\rightarrow 0$ as $x\rightarrow \pm \infty$, this simplifies to
$$
-\frac{i\hbar}{2m}\int\limits_{-\infty}^{+\infty} \Psi^{*} \partial \Psi    -\frac{i\hbar}{2m} \int\limits_{-\infty}^{+\infty}\Psi^{*} \ \partial \Psi =  \boxed{- \frac{i\hbar}{m}\int\limits_{-\infty}^{+\infty} \Psi^{*} \frac{\partial \Psi}{\partial x} \ dx}
$$
We postulate that $\left<v \right>=\frac{d \left<x \right>}{dt}$, or $\left<p \right>=m \left<v \right> = -i\hbar \int\limits\left(\Psi^{*} \frac{\partial \Psi}{\partial x}\right) \ dx$.  From these we realize that we now have two expressions for the expectation value that follow the same form:
$$
\begin{align*}\\
\boxed{
\begin{gathered}
\left<x \right> =  \int\limits\Psi^{*} x \ \Psi \ dx \\
\left<p \right> =  \int\limits\Psi^{*}\left(\frac{\hbar}{i} \frac{\partial}{\partial x}\right)\Psi  \ dx
\end{gathered}\\
}
\end{align*}
$$
From this conclusion, we draw inspiration, and define "[[Operators]]" to calculate expectation values, where we sandwich $\Psi^*$ and $\Psi$ and integrate, such that we now define 
$$
\begin{align*}\\
\boxed{\\
\begin{gathered}
\hat x = x, \\
\hat p = \left(\frac{\hbar}{i} \frac{\partial}{\partial x}\right)
\end{gathered}
}
\end{align*}
$$