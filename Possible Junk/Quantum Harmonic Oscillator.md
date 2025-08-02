---
tags: Derivation, QM, QHO, Harmonic_Oscillator
dg-publish: true
mathLink: 
---
Subject: _QM_
Main\_Topic: _Quantum Harmonic Oscillator_
Applications: _Oscillatory systems and potential approximations_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

We know from classical mechanics that Hooke's Law is $F_{restitution} = -kx$ for a spring, using Newton's second law we can then have an equation for an oscillator:
$$
F = -kx = m \ddot x
$$
where we have the definitions $\omega = \sqrt{\frac{k}{m}}$ (the angular frequency), and $V = \frac{1}{2}kx^{2}$ (the potential energy). 

If we were to Taylor expand $V(x)$ to $V(x)=V(x_0)+V'(x_0)(x-x_0)+...$ then we can approximate in the neighborhood of a local minimum for a potential E. We can virtually approximate any <mark style="background: #BBFABBA6;">oscillatory</mark> motion by a simple harmonic oscillator!

![[Pasted image 20230619120609.png|500]]
We can approximate that $V(x_0)=0$ for a minimum (which also implies that the first derivative must be zero) along with $V'(x_0)=0$ to get:
$$
V(x) \approxeq \frac{1}{2}V^{''}(x_{0})(x-x_{0}) ^{2} \quad \text{if} \ k=V^{''}(x_{0}) 
$$
We throw out the other higher order terms because they become insignificant. 

---
# The Schrodinger Equation
The Schrodinger Equation for this potential, $V=\frac{1}{2}kx^{2}$ is usually written in terms of the angular frequency $\omega=\sqrt{\frac{k}{m}}$, so we use $V=\frac{1}{2}m\omega ^{2} x^{2}$:
$$
\hat H \psi = E\psi \rightarrow - \frac{\hbar}{2m} \frac{ \partial^{2} \psi}{\partial x^{2}} + \frac{1}{2}m\omega ^{2}x^{2} = E\psi 
$$
This equation can be solve either analytically or via what is known as [[#The Algebraic Method (Ladder Operators)]], both of which will be discussed below: 

### The Algebraic Method (Ladder Operators) 
let us take the equation 
$$
- \frac{\hbar^{2}}{2m}  \frac{\partial^{2} \psi}{\partial x^{2}} + \frac{1}{2}m\omega ^{2}x^{2}= E\psi 
$$
what we can do is somewhat try to factor this out (kinda like what D'Alambert did with the Wave equation). Let reorder this equation in a better fashion to see how we can factor:
$$
\frac{1}{2m}\left[ \left(\frac{\hbar}{i} \frac{\partial}{\partial x}\right)^{2} +(m\omega  x)^{2} \right]\psi =E\psi 
$$
Now, what if we <mark style="background: #D2B3FFA6;">TRY</mark> to create two operators that each represent a "factor" of this equation? Let them be known as:
$$
a_{\pm} \equiv \frac{1}{\sqrt{2m}}\left[ \frac{\hbar}{i} \frac{\partial}{\partial x} \pm im \omega x \right] 
$$
which are just the factoring of the Hamiltonian operator term in the original Schrodinger Equation. But will this work? Let us try by using a test function $f(x)$ to see how these operators play out!
$$
\begin{gathered}
\text{if we take a look at}\ (a_{-}a_{+})f(x), \ \text{we have} \\
(a_{-}a_{+})f(x) = \frac{1}{2m}\left(\frac{\hbar}{i} \frac{\partial}{\partial x}-im\omega x\right)\left(\frac{\hbar}{i} \frac{\partial}{\partial x}+im\omega x\right)f(x) \\
= \frac{1}{2m}\left(\frac{\hbar}{i} \frac{\partial}{\partial x}-im\omega x\right)\left(\frac{\hbar}{i} \frac{\partial f(x)}{\partial x} + im\omega x f(x)\right) \\
= \frac{1}{2m}\left(-\hbar ^{2} \frac{\partial^{2}}{\partial x^{2}}(f(x)) +\hbar m \omega  \frac{\partial}{\partial x}(xf(x)) -\hbar \omega mx  \frac{\partial}{\partial x}(f(x)) +(m \omega x)^{2}f(x)\right) \\
=\frac{1}{2m}\left[ \left(\frac{\hbar}{i} \frac{\partial}{\partial x}\right)^{2} +(m\omega x)^{2} +\hbar \omega x \right]f(x)
\end{gathered}
$$
Thus, 
$$
a_{-}a_{+}= \frac{1}{2m}\left[\left(\frac{\hbar}{i} \frac{\partial}{\partial x}\right)^{2}+(m\omega x)^{2} \right] + \frac{1}{2}\hbar \omega   
$$
Therefore, $a_{-}a_{+}$ does not factor the Schrodinger Equation perfectly, but if does pretty well and leaves us with only a constant factor left over. What if we also try to take the operators in the other way around, $a_{+}a_{-}$? Doing the same methods as before, we get the result 
$$
a_{+}a_{-}= \frac{1}{2m}\left[\left(\frac{\hbar}{i} \frac{\partial}{\partial x}\right)^{2} + (m\omega x)^{2}\right] - \frac{1}{2}\hbar \omega 
$$
The same factor but in the opposite direction! So, $a_{-}a_+ -a_{+}a_{-}=\hbar \omega$. We could then rewrite the Schrodinger Equation as 
$$
\begin{aligned}
\left(a_{+}a_{-} + \frac{1}{2}\hbar \omega \right)\psi &=E\psi, \quad \text{or} \\

\left(a_{-}a_{+} - \frac{1}{2}\hbar \omega \right)\psi &= E\psi

\end{aligned}

$$

Now, here is where we travel into new waters.... what if $a_{-}\psi(x)$ and $a_{+}\psi (x)$ themselves also solve the Schrodinger Equation? If we test this with $a_{+}\psi(x)$, we get
$$
\begin{gathered}
(a_{+}a_{-} + \frac{1}{2}\hbar \omega )(a_{+}\psi) = \left(a_{+}a_{-}a_{+}+ \frac{1}{2}\hbar \omega a_{+}\right)\psi \\
= a_{+}\left(a_{-}a_{+}+ \frac{1}{2}\hbar \omega\right)\psi 
\end{gathered}
$$
(the $a_{+}$ can be pulled out since the $\frac{1}{2}\hbar \omega$ term is a constant and thus order doesn't matter). Now, we notice that there is an $a_{-}a_{+}$ term in this expression, which reminds us of the other definition of the Schrodinger Equation! We can simplify this expression and then use the other definition of the Schrodinger Equation from these operators to then write:
$$
\begin{gathered}
= a_{+}\left(\left(a_{-}a_{+} - \frac{1}{2}\hbar \omega\right) +\hbar \omega\right)\psi \\
= a_{+}(E\psi +\hbar\omega\psi) = (E+\hbar \omega)(a_{+}\psi)
\end{gathered}
$$
We can thus conclude that:
$$
\boxed{\left(a_{+}a_{-}+ \frac{1}{2}\hbar\omega\right)(a_{+} \psi) = (E+\hbar \omega ) (a_{+}\psi) }
$$
Therefore, $a_{+}\psi$ is a solution to the Schrodinger Equation with Energy $E+\hbar\omega$.

What if we apply this same method to $a_{-}\psi$? Well, we get a similar result:
$$
\boxed{(a_{-}a_{+} - \frac{1}{2}\hbar\omega)(a_{-}\psi) = (E-\hbar \omega)(a_{-}\psi)}
$$
So, $a_{-}\psi$ is also a solution but with an Energy of $E-\hbar\omega$. So, in a sense, applying these operators results in a solution where the energy is raised or lowered by a factor of $\hbar\omega$. In other words: these operators raise or lower the state of the wave function. For this reason, we call these operators $a_{\pm}$, <mark style="background: #ADCCFFA6;">Ladder Operators!</mark>

So, how do we find the wave function off of this? Well, lets say we apply this lowering operator over and over again. At some point it must get to a point where the Energy being described is $\leq 0$ since we are taking energy away every time. We know that the Energy must always be $> 0$ though for potentials that are $\geq 0$ from [[why can't energy be 0]]. 


```ad-note
there is NO guarantee that $a_{\pm}\psi$ is a normalized solution </mark> 
```

An Energy $\leq 0$ would result in a non-normalizable $\psi$ ([[why can't energy be 0#E must exceed minimum V|E must exceed minimum V]]). Thus, there must be a "lowest rung" right before $\psi$ is not normalizable anymore, which is either $\psi = 0$ or $\psi=\infty$. 

We can actually prove that the case $\psi=\infty$ can never happen:


#### Proof that ladder operator cant result in infinite norm
We can show that the lowering operator cannot general a state of infinite norm (i.e. $\int\limits_{-\infty}^{+\infty} |a_{-}\psi|^{2} \ dx < \infty$ ) if $\psi$ is normalized:

$$
\begin{gathered}
\int\limits_{-\infty}^{+\infty} (a_{-}\psi)^{*}(a_{-}\psi) \ dx = \frac{1}{\sqrt{2m}}\int\limits_{-\infty}^{+\infty} \left( \frac{\hbar}{-i}  \frac{\partial \psi^{*}}{\partial x}+im\omega x \psi^{*}\right)(a_{-}\psi) \ dx \\

= \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}} \frac{\hbar}{-i}  \frac{\partial \psi^{*}}{\partial x}(a_{-}\psi) \ dx + \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}}im\omega x\psi^{*}(a_{-}\psi) \ dx \\
= \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}} \frac{\hbar}{-i}   (a_{-}\psi) \ \partial \psi^{*} + \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}}im\omega x\psi^{*}(a_{-}\psi) \ dx 

\end{gathered}
$$
Using [[integration by parts]] on the first integal, we can now write this as 
$$
\begin{gathered}
\left. \frac{1}{\sqrt{2m}} \frac{\hbar}{-i}(a_{-}\psi)\psi^{*}\right\rvert_{-\infty}^{+\infty} &- \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}} \frac{\hbar}{-i}\psi^{*}\partial(a_{-}\psi) \\
&+ \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}}imx\omega\psi^{*}(a_{-}\psi) \ dx
 \end{gathered}
$$
Since we know that $\psi \rightarrow 0$ and $\psi^{*} \rightarrow 0$ as $x \rightarrow \pm \infty$, then the first term must equal $0$. We also put the first integral back into terms of integrating by $dx$:  
$$
\begin{gathered}
-\int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}} \frac{\hbar}{-i}\psi^{*} \frac{\partial (a_{-}\psi)}{\partial x} \ dx + \int\limits_{-\infty}^{+\infty} \frac{1}{\sqrt{2m}}im\omega x \psi^{*}(a_{-}\psi) \ dx \\
= \frac{1}{\sqrt{2m}} \int\limits_{-\infty}^{+\infty}  \psi^{*} \frac{\hbar}{i}  \frac{\partial (a_{-}\psi)}{\partial x} + im\omega x \psi^{*}(a_{-}\psi) \ dx \\
= \int\limits_{-\infty}^{+\infty}\psi^{*} \frac{1}{\sqrt{2m}}\left[\frac{\hbar}{i}  \frac{\partial}{\partial x} +im\omega x\right](a_{-}\psi) \ dx \\
= \int\limits_{-\infty}^{+\infty} \psi^{*}a_{+}(a_{-}\psi) \ dx

\end{gathered}
$$
Using the Schrodinger Equation definition from the ladder operators:
$$
\begin{gathered}
 = \int\limits_{-\infty}^{+\infty} \psi^{*}(E- \frac{\hbar\omega}{2})\psi \ dx = \left(E- \frac{\hbar\omega}{2}\right)\int\limits_{-\infty}^{+\infty} \psi^{*}\psi \ dx = \left(E- \frac{\hbar\omega}{2}\right)
\end{gathered}
$$
Thus, the lowering operator gives a finite integral for a normalizable $\psi$, so the only way to get a non-normalizable integral from the lowering operator is if $\psi = 0$.       

If we do this same procedure on $a_{+}\psi$, we see a similar result: $E+ \frac{\hbar\omega}{2}$.


#### Finding Ground State Wave Function
So, by now we have shown how the "lowest rung" (ground state) wave function, $\psi_0$, must be one state above $\psi=0$ in other words:
$$
a_{-}\psi_{0}=0
$$
or,
$$
\begin{gathered}
\frac{1}{\sqrt{2m}}\left(\frac{\hbar}{i} \frac{\partial \psi_{0}}{\partial x} - im\omega x\psi_{0}\right)=0 \\
\frac{d\psi_{0}}{dx} = \frac{-m\omega}{\hbar}x\psi_{0}\\
\int\limits \frac{d\psi_{0}}{\psi_{0}} = \int\limits \frac{-m\omega}{\hbar}x \ dx \\
\ln(\psi_{0}) = -m\omega \frac{x^{2}}{2\hbar} + C \\
\boxed{\psi_{0}(x) = Ce^{\frac{-m\omega x^{2}}{2\hbar}}}


\end{gathered}
$$
To find the Energy for $\psi_0(x)$, we plug it into the Schrodinger Equation $$a_{+}a_{-}\psi_{0}  + \frac{1}{2}\hbar\omega \psi_{0} = E_{0}\psi_{0}$$
and exploit that $a_{-}\psi_{0}=0$ to get of the first term resulting in
$$
\frac{1}{2}\hbar\omega\psi_{0}=E_{0}\psi_{0}
$$
so 
$$
\boxed{E_{0} = \frac{1}{2}\hbar\omega}
$$
and
$$
\boxed{\psi_{n}(x) = (a_{+})^{n}\psi_{0}(x) = A_{n}(a_{+})^{n}e^{\frac{-m\omega x^{2}}{2\hbar}}}
$$
The $A_{n}$ constant comes from the $C$ in the ground state wave function. Thus, we must have a constant to account for it. 

#### Finding the Normalization Constants
We need to now figure out how we are going to find the normalization constants.‎

We remember that using the ladder operators changes the Energy by a factor of $\hbar \omega$. Thus, since we know $E_{0}$ we know that
$$
E_{n} = E_{0}+\hbar\omega n = (n+ \frac{1}{2})\hbar\omega, \quad n=1,2,3,\ldots
$$

Now, if we use this results with the normalization integrals for $a_{\pm}\psi$, which were $E\pm \frac{\hbar\omega}{2}$ respectively, we can create a proportion between states from using the ladder operators.  
$$
\begin{gathered}
\int\limits_{-\infty}^{+\infty}|a_{-}\psi|^{2}\ dx = E_{n}- \frac{\hbar\omega}{2}=\hbar\omega n
\end{gathered}
$$
and 
$$
\begin{gathered}
\int\limits_{-\infty}^{+\infty} |a_{+}\psi|^{2} \ dx = E_{n}+ \frac{\hbar\omega}{2} = (n+1)\hbar\omega

\end{gathered}
$$
If we assume that there is a proportionality constant $\kappa$ when using the ladder operators: 
$$
\begin{aligned}
a_{+}\psi = \kappa_{1}\psi_{n+1} \\
a_{-}\psi = \kappa_{2}\psi_{n-1}
\end{aligned}
$$
We assume this proportionality because the raising and lowering operators do not guarantee a normalized solution. 

For normalization, we need
$$
\begin{gathered}
\int\limits_{-\infty}^{+\infty} |\psi_{n+1}|^{2}\ dx = 1, \ \text{so}\\
\int\limits_{-\infty}^{+\infty} \left|\frac{1}{\kappa_{1}} a_{+}\psi \right|^{2}dx = \frac{1}{\kappa^{2}_{1}} (n+ 1)\hbar\omega = 1  

\end{gathered}
$$
thus, 
$$
\kappa_{1}=\sqrt{\left(n+1\right)\hbar\omega}, \quad \boxed{a_{+}\psi_{n} = \psi_{n+1}\sqrt{\left(n+1\right)\hbar\omega}} 
$$
Applying this same technique to $a_{-}\psi$ gives us 
$$
\kappa_{2} = \sqrt{n\hbar\omega}, \quad \boxed{a_{-}\psi_{n} = \psi_{n}\sqrt{n\hbar\omega}}
$$
Now, using $a_{+}\psi_{n}=\sqrt{(n+1)\hbar\omega} \ \psi_{n+1}$, we see that $a_{+}\psi_{0}=\sqrt{\hbar\omega} \ \psi_{1}$.

Let us, while we are at it, find the normalization constant for $\psi_{0}=A_{0}e^{\frac{-m\omega x^{2}}{2\hbar}}$ 
$$
\int\limits_{-\infty}^{+\infty} \psi^{*}\psi \ dx = |A_{0}|^{2}\int\limits_{-\infty}^{+\infty} e^{\frac{-m\omega x^{2}}{\hbar}} \ dx
$$
We can use polar coordinates and the [[Jacobian]] to solve this problem, which is just the [[Gaussian Integral]] with a constant in front of the exponential, resulting in the solution 
$$
|A_{0}|^{2}\sqrt{\left(\frac{\pi\hbar}{-m\omega}\right)} 
$$
We can solve the normalization condition by setting this equal to $1$ and solving for
$$
A_{0}=\pm\left(\frac{m\omega}{\hbar\pi}\right)^\frac{1}{4}
$$
in which we will just take the position answer for simplicity, leaving us with:
$$
\psi_{0}(x) = \left(\frac{m\omega}{\hbar\pi}\right)^{\frac{1}{4}}e^{\frac{-m\omega x^{2}}{2\hbar}}
$$
From our ladder operator wave function definition 
$$
\psi_{n}(x) = A_{n}(a_{+})^{n}e^{\frac{-m\omega x^{2}}{2\hbar}}
$$
we rewrite the exponential term in terms of $\psi_{0}(x)$ and $A_{0}$. 
$$
\psi_{n}(x) = A_{n}(a_{+})^{n}e^{\frac{-m\omega x^{2}}{2\hbar}}= A_{n}(a_{+})^{n}\frac{\psi_{0}(x)}{A_{0}}
$$

Now, once again, we apply a ladder operator until something breaks or shows itself! We will apply the raising operator an arbitrary amount of times in hopes to see a pattern to find out what $A_{n}$ is. Each time we use this raising operator we must also remember that  $a_{-}\psi_{n} = \psi_{n}\sqrt{n\hbar\omega}$.
$$
\begin{gathered}
\psi_{n}(x) = A_{n}(a_{+})^{n} \frac{\psi_{0}}{A_{0}} =\frac{A_{n}}{A_{0}}(a_{+})^{n}\psi_{0}= \frac{A_{n}}{A_{0}}(a_{+})^{n-1}(a_{+}\psi_{0}) \\ 
= \frac{A_{n}}{A_{0}}(a_{+})^{n-1}\sqrt{\hbar\omega} \ \psi_{0} = \frac{A_{n}}{A_{0}}(a_{+})^{n-2}\sqrt{\hbar\omega} \ (a_{+}\psi_{1}) \\
= \frac{A_{n}}{A_{0}}(a_{+})^{n-2}\sqrt{\hbar\omega}\sqrt{2\hbar\omega}  \ \psi_{2} \ \ldots n \text{ times}\ldots \ \frac{A_{n}}{A_{0}}\sqrt{n!(\hbar\omega)^{n}} \ \psi_{n}(x)
\end{gathered}
$$
Since $\psi_{n}(x)=\frac{A_{n}}{A_{0}}\sqrt{n!(\hbar\omega)^{n}} \ \psi_{n}(x)$, then $\frac{A_{n}}{A_{0}}\sqrt{n!(\hbar\omega)^{n}}=1$, solving then we get
$$
\boxed{A_{n} = \left(\frac{m\omega}{\pi\hbar}\right)^{\frac{1}{4}} \frac{1}{\sqrt{n!(\hbar\omega)^{n}}}}
$$
Thus, we have our final solution:
$$
\boxed{\psi_{n}(x) = \left(\frac{m\omega}{\pi\hbar}\right)^{\frac{1}{4}} \frac{1}{\sqrt{n!(\hbar\omega)^{n}}}(a_{+})^{n}e^{\frac{-m\omega x^{2}}{2\hbar}}}
$$

