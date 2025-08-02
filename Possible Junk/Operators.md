---
tags: QM, Operators, Expectation
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Operators_
Applications: _Finding the expectation values or mathematical implications of a property within a system_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

Operators are mathematical objects that act onto some function or variable in order to get a specific <mark style="background: #D2B3FFA6;">measurable outcome</mark>. In the world of Quantum Mechanics this typically means measuring: Energy, Momentum, and Position. Their derivation comes from [[Expectation Values]] and the [[Schrodinger Equation]]. Their corresponding [[Expectation Values]] (Cont. of [[Probability#Mean / Expectation Value]] ) represents an expected measurement of the system, or the mean of a property of a system (most typically the momentum and position.

-
	Note: Most operator evaluations require [[integration by parts]]

#### Heisenberg's Uncertainty Principle
A principle that states there is an uncertainty in the ability to measure position and momentum to a certain accuracy at the same time. One way of thinking about this is shaking a rope up and down. If we just do one big shake, there will be a bump that moves across the rope. We can say pretty certainly that the wave we created has a position. But what about its wavelength? Because it's not really periodic, we can't say much about it having a wavelength. 

Okay, but what if we take this rope and oscillate it up and down such that we now do have a wavelength. Great, but then do we have a position? The wave is across the entire rope, so we can't really say it has a particular position now. 

This trade off between position and wavelength is the uncertainty principle. We know from Einstein and Dirac that $E^{2}= (pc)^2+(mc^2)^{2}$, and we know from De Broglie about matter waves; thus, wavelength is analog to momentum. There is an uncertainty in having a well-defined momentum or position at the same time. This conclusion is derived from mathematics and from the <mark style="background: #BBFABBA6;">General Uncertainty Principle</mark> or Fourier Transforms ([[Pontryagin duality]] of position and momentum). This result doesn't actually say anything about measuring. 
$$
\begin{align*}\\
\boxed{
\begin{gathered}
\sigma_{x}\sigma_{p}\geq \frac{\hbar}{2}, \\
\left<x \right>\left<p \right>\geq\frac{\hbar}{2} \\
\end{gathered}\\
}
\end{align*} 

$$

It is also worth noting that there is no time-energy uncertainty principle. Why? Because in Quantum Mechanics, it is assumed that everyone measures the same time. But what about virtual particles and Quantum Foam? Whose existence is dependent on this notion of "breaking conservation of energy in a short time and 'giving it back' "? 

A good paper on this is [The Time-Energy Uncertainty Relation](https://math.ucr.edu/home/baez/uncertainty.html) which employs the [[Stone-von Neumann theorem]]. 

In short: just be skeptical. The Heisenberg Uncertainty principle is taken out of hand... A LOT. 


#### Note: Ehrenfest's Theorem
A theorem that is to show the analog of Quantum Mechanics with Classical Mechanics by means of the momentum principle (for conservative forces):
$$
\frac{dp}{dt}=F_{net} =- \frac{\partial V}{\partial x}
$$
It turns out that this can be seen in Quantum Mechanics through [[Expectation Values]]expectation values:
$$
\frac{d \left<p \right>}{dt} = \left< - \frac{\partial V}{\partial x} \right>
$$


---
## Position Space Operators
By using the Schrodinger Equation in position space along with the definition of [[Expectation Values]], the formulation of the position and momentum space operators in the position space basis can be seen in [[Expectation Values#Position Operator Changing over Time]], which gives us our two main definitions:
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
and
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
Since all quantities can be written in terms of $x$ and $p$ (from classical mechanics), we can replace all $x$ and $p$ by $\hat x$ and $\hat p$ to create analog operators to classical counterparts: 
$$
\left<Q(x,p) \right> = \int\limits\Psi^{*}Q\left(x, \frac{\hbar}{i} \frac{\partial}{\partial x}\right)\Psi \ dx
$$
---
## Ladder Operators
Ladder operators are operators that are found by trying to "factor" the Schrodinger Equation, leaving you with various factors of the Hamiltonian Operator. These factors can then be used to create expressions for the Schrodinger Equation while usually having to take away a constant factor that shows up.

If these operators acting on the wave function themselves are also solutions to the Schrodinger Equation, we can see how they change the Energy level. Usually, one of these operators raises the Energy of the wave function or lowers it. With this knowledge, we can solve such a Schrodinger Equation by assuming that if we Lower it indefinitely, there must be a minimum Energy point right $>0$ before where applying the lowering operator would result in the Energy going $\leq 0$ Why is this? See [[why can't energy be 0]]. This "lowest rung" must be the last possible solution to the Schrodinger Equation that is unformalizable. 

So, we apply the lowering operator once more and assume that $\psi = 0$ or $\psi=\infty$ because those two options are what bring about un-normalizable solutions. We can actually prove that the lowering operator can't give a state of infinite norm ($\int\limits |a_{-}\psi|^{2} \ dx<\infty$) most of the time which allows us to set $a_{-}\psi = 0$ and solve it, giving us a recursive formula from an initial $\psi_{0}(x)$, using the raising operator we can now find any $\psi_{n}(x)$! To find the normalization constant we apply this raising operator an arbitrary $n$ number of times and see the pattern of the coefficient in front of $\psi_{n}(x)$ which must equal 1.  

An example of this entire procedure can be seen in: [[Quantum Harmonic Oscillator#The Algebraic Method (Ladder Operators)]]