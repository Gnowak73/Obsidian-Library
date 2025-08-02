---
tags: derivation, QM, heisenberg, energy
dg-publish: true
mathLink: 
---
Subject: _None_
Main\_Topic: _None_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Probability#Measurement of Spread|Standard Deviation]]_
Cont.\_ of: _None_ 
_
_
If we have a scenario such that a particle can have zero Energy, it would correspond to a particle that is not moving at all. Why can't we have this? It's because the [[Operators#Heisenberg's Uncertainty Principle|Heisenberg's Uncertainty Principle]] would state that if the position is at rest, then there must be 
$$
\Delta x\Delta p \geq \frac{\hbar}{2}
$$
so 
$$
\Delta p \geq \frac{\hbar}{2\Delta x }
$$
If we were to know exactly where the particle is, such that there would be no spread of the data, $\Delta x=0$. Thus, we would have a very ill-defined momentum, distributing over the entire space, (literally constant over entire momentum space). This means that we would be able to measure an infinite range of the momentum, so at the lowest, there would be infinite kinetic energy. Okay, so we have no way to absolutely say there is a particle at rest and we know that there is 0 kinetic energy (not the same as saying it will gain infinite kinetic energy). 

If we instead take $\Delta x$ to be the width of a potential well, then we would have
$$
\Delta p \geq \frac{\hbar}{2a}
$$
where $a$ is the width of the potential well. Remember, $\Delta p$ is really talking about the standard deviation, or $\sigma_{p}\equiv \left<(\Delta p)^{2}\right> = \left<p^{2}\right> - \left<p \right>^{2}$. Thus, we can say that at the lowest Energy $E_{0}$ we have
$$
\left<E \right> = \left< KE \right> = \frac{\left< p^{2} \right>}{2m} = \frac{\left<p \right>^{2}}{2m} + \frac{\sigma_{p}^{2}}{2m} = \frac{\left<p \right>^{2}}{2m} +  \frac{\hbar^{2}}{8ma^{2}}\geq \frac{\hbar^{2}}{8ma^{2}}
$$
since $\left<p \right>^{2} \geq 0$. 

Thus, the Energy has to have a minimum <mark style="background: #ABF7F7A6;">Above Zero!</mark> If we have potential energy in the mix too, then we will never be able to get to 0 for sure. 

We can generalize this result for any system:
$$
\begin{gathered}
\left<E \right> = \left< KE \right> + \left<V \right> = \frac{\left< p^{2} \right>}{2m} + \left<V \right> \\ = \frac{\left<p \right>^{2}}{2m} + \frac{\sigma_{p}^{2}}{2m} + \left<V \right>= \left<V \right> + \frac{\left<p \right>^{2}}{2m} +  \frac{\hbar^{2}}{8m\sigma^{2}_{x}} \geq \frac{\hbar^{2}}{8m\sigma^{2}_{x}}
\end{gathered}
$$
So as long as the Potential Energy is $\geq 0$, then we cannot have a case of 0 energy.


### E must exceed minimum V 
E actually can't be less than the minimum value of the Potential Energy, V, either. This is because it would result in a Schrodinger Equation where $\psi$ and its second derivative have the same sign, meaning it would grow to infinity (permanently concave up or down), and thus is not normalizable. 