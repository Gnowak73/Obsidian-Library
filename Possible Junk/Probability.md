---
tags: QM, Probability, Expectation, Operators
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Probability_
Applications: _Probability and expected values, Normalization_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

## Mean / Expectation Value
(Cont. [[Expectation Values]])

The expectation value is what we would "expect" to measure for a specific property of a system. In other words, it's the mean.

If a function, say N(j), gave a frequency of j peoples, then $N_{total} = \sum_{j=0}^{\infty}N(j)$ and the probability of choosing a person of that specific type is $P(j)=\frac{N(j)}{N}$, where $\quad \sum_{j=0}^{\infty}P(j)=1.$ 

In short, we can say that 

$$

Mean = Expectation \ Value = \ <j> \ = \frac{\sum_{j=0}^{\infty} jN(j)}{N} = \sum_{j=0}^{\infty} jP(j) 

$$

When changing the function of the expectation value, the values measured may change but the frequency, or probability, isn't. In other words, this means that:

$$
\boxed{\left<f(j)\right> \ = \sum_{j=0}^{\infty} f(j)P(j)}
$$

---

## Measurement of Spread
The measurement for spread can be defined as $\Delta j = j -\left<j\right>$, which would be the deviation from the mean. The problem with this is that if we were to try and find $\left<\Delta j\right>$, we would get:

$$
\left<\Delta j\right> =\sum \left(j-\left<j\right>\right)P(j) = \sum jP(j) - \sum  \left<j\right>P(j)= 
$$
$$
\left<j\right> - \left<j\right>\sum P(j) = \left<j\right> - \left<j\right> = 0. 
$$

The problem with defining our spread variable as $\Delta j = j - \left<j\right>$ is because $\Delta j$ is either above or below the mean always half of the time (definition of the mean), and since the direction(whether you are higher or lower than the mean) is being taken into account, the positive and negatives cancel to 0. What we could try to do is to take the absolute value of $\Delta j$, except this create a lot of tedious math. Instead, we will just square it! Now, we define the standard deviation:
$$
\sigma^2 \equiv \left<\left(\Delta j\right)^2\right> = \boxed{\left<j^2\right> - \left<j\right>^2}
$$

Note, that this does imply $\left<j^2\right> \geq \left<j\right>^2$, in which the deviation is 0 if they are equal.

An interesting result in quantum mechanics is actually about this spread, called [[Operators#Heisenberg's Uncertainty Principle|Heisenberg's Uncertainty Principle]]

---

## Continuous Probabilities 
$p(x)dx$, where $p(x)$ is the probability density, is defined to be the probability between a value $x$ and $x+dx$. For continuous functions, we have an integral instead of a sum now.

$$
\begin{aligned}
P_{ab} &= \int_a^b p(x) \ dx, \quad \text{such that:} \\
\\




&\boxed{
\begin{gathered}
\int\limits_{-\infty}^{+\infty}p(x) \ dx = 1, \\
\left<x\right> = \int\limits_{-\infty}^{+\infty}xp(x) \ dx,\\
\sigma^2 \equiv \left<\left(\Delta x\right)^2\right> = \left<x^2\right> - \left<x\right>^2
\end{gathered}
}



\end{aligned}
$$
### Normalization
The condition that the probability across all space must be equal to 1. AKA:
$$
\boxed{\int\limits_{-\infty}^{+\infty}\left|\Psi(x,t)\right|^2 \ dx = 1}
$$
We can use this condition to find the constant coefficients that appear in the wave function (probability amplitude).

#### How does normalization evolve with time?
If we take the derivative of the probability over all space at a certain point in time: 
$$
\begin{equation}
\tag{1}



\frac{d}{dt} \int\limits_{-\infty}^{+\infty} \left| \Psi(x,t)\right|^2 \ dx = \int\limits_{-\infty}^{+\infty}\frac{\partial }{\partial t} \left|\Psi(x,t)\right|^2 \ dx.

\end{equation}
$$

We know that(using the product rule): 
$$
\frac{\partial}{\partial t}(\Psi^* \Psi) = \Psi^*\frac{\partial \Psi}{\partial t} \ + \Psi\frac{\partial \Psi^*}{\partial t}
$$
Thus, (1) can be rewritten as:
$$
\int\limits_{-\infty}^{+\infty}\left(\Psi^*\frac{\partial \Psi}{\partial t}+\Psi\frac{\partial \Psi^*}{\partial t}\right) \ dx.
$$
From the [[Schrodinger Equation]]:
$$
\tag{2}
i\hbar\partial_t \Psi = \hat{H}\Psi \rightarrow \frac{\partial \Psi}{\partial t} = \frac{i\hbar}{2m}\frac{\partial^2 \Psi}{\partial x^2}-\frac{i}{\hbar}V\Psi
$$
Taking the Complex Conjugate of (2), we have
$$
\tag{3}
\frac{\partial \Psi^*}{\partial t} = \frac{-i\hbar}{2m}\frac{\partial^2 \Psi^*}{\partial x^2}+\frac{i}{\hbar}V\Psi^*
$$
**Remark.** The Complex Conjugate of the integral and the derivative is the derivative or the integral of the Complex Conjugate. This is from the linear nature of these operators(as seen below):


$$
\begin{aligned}
\left(\frac{\partial \Psi}{\partial t}\right)^* &= \frac{\partial}{\partial t}\left(\Psi_{re} + i\Psi_{im}\right)^*  \\
&=\left(\frac{\partial \Psi_{re}}{\partial t}+i\frac{\partial \Psi_{im}}{\partial t}\right)^* \\
&= \frac{\partial \Psi_{re}}{\partial t} - i\frac{\partial \Psi_{im}}{\partial at}  \\
&= \frac{\partial}{\partial t}\left(\Psi_{re}-i\Psi_{im}\right)  \\
&= \frac{\partial}{\partial t}\left(\Psi^*\right)
\end{aligned}
$$
Using (2) and (3) we can finally make the connection:
$$
\frac{\partial}{\partial t}\left|\Psi\right|^2 = \frac{i\hbar}{2m}\left(\Psi^*\frac{\partial^2 \Psi}{\partial x^2} - \frac{\partial^2 \Psi^*}{\partial x^2}\Psi\right) = \frac{\partial}{\partial x}\left[\frac{i\hbar}{2m}\left(\Psi^*\frac{\partial \Psi}{\partial x} - \frac{\partial \Psi^*}{\partial x}\Psi\right)\right]
$$
such that our integral can be evaluated to be:
$$
\frac{d}{dt}\int\limits_{-\infty}^{+\infty}\left|\Psi(x,t)\right|^2 \ dx = \left. \frac{i \hbar}{2m}\left(\Psi^*\frac{\partial \Psi}{\partial x} - \frac{\partial \Psi^*}{\partial x}\Psi\right) \right\rvert_{-\infty}^{+\infty}
$$
and since $\Psi(x,t)\rightarrow 0$ as $x\rightarrow \infty$, 
$$
\frac{d}{dt}\int\limits_{-\infty}^{+\infty}\left|\Psi(x,t)\right|^2 \ dx = \left. \frac{i \hbar}{2m}\left(\Psi^*\frac{\partial \Psi}{\partial x} - \frac{\partial \Psi^*}{\partial x}\Psi\right) \right\rvert_{-\infty}^{+\infty} = \boxed{0}
$$
$$

\boxed{\begin{gathered}
\text{Thus, $\int\limits_{-\infty}^{+\infty}\left|\Psi(x,t)\right|^2 \ dx$ is constant to time, so if $\Psi$ is normalized at $t=0$}, \\  \text{it is normalized for all future time. }
\end{gathered}}
$$

### Orthogonal Wave Functions

Just like as shown in [[Function Linear Algebra]], wave functions are orthogonal if the inner product of two wave functions is $0$:
$$
(\psi_m(x),\psi_{n}(x)) = 0 = \int\psi_{m}^{*}(x)\psi_{n}(x) \ dx
$$
An example of this would be two sine functions like in the [[Schrodinger Equation#Infinite Square Well |infinite square well]] problem (using the product sum formula from [[trig_cheat_sheet.pdf]]):

$$
\begin{gathered}
\int\limits_{0}^{a} sin\left( \frac{m\pi}{a}x\right)\sin\left( \frac{n\pi}{a}x\right) \ dx, \quad m\neq n, \\
 = \int\limits_{0}^{a}2 \left[\cos\left( \frac{x}{a}(m-n)\right) -\cos\left(\frac{\pi x}{a} (m+n) \right) \right] \ dx \\
 =\frac{2}{\pi} \left[ \frac{\sin((m-n)\pi)}{m-n} - \frac{\sin((m+n))\pi}{m+n} \right]=0

\end{gathered}
$$

### Combining Orthogonality and Normalization Conditions
We can combine orthogonality and normalization into one statement:
$$
\int\limits\psi^{*}_{m}(x)\psi_{n}(x) \ dx = \delta_{mn}
$$
where $\delta_{mn}$ is the Kronecker delta: 

$$
\delta_{mn}= \begin{cases} 0, \quad m \neq n\\
 1, \quad m=n\\
\end{cases}
$$



