---
tags: Math, Integral, integration, method, laplace, transform, improper
dg-publish: true
mathLink: 
---
Subject: _Integration Methods_
Main\_Topic: _Solving Improper Integrals with Laplace Transforms_
Applications: _Solving Improper Integrals_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Integration Methods]],[[Laplace Transforms]]_
Cont.\_ of: _None_ 
_
_

Let us have an improper integral 
$$
\int\limits_{0}^{\infty}f(t) \ dt
$$
Now, sometimes we can se [[Laplace Transforms]] in order to solve this integral by making a direct comparison to what the value of what $s$ would have to be to get our original integral. Two identities that become important in such problems is:
$$
\mathcal{L} \{ \frac{f(t)}{t}\} = \int\limits_{s}^{\infty}F(u) \ du \quad \text{where} \quad F(s) = \mathcal{L}\{f(t)\}
$$
and 
$$
\int\limits_{0}^{\infty}f \ g \ dx = \int\limits_{0}^{\infty}\mathcal{L}\{f\} \mathcal{L^{-1}}\{g\} \ dx
$$
##### Example 
Let us have the integral 
$$
\int\limits_{0}^{\infty} \frac{\sin 2t}{t} \ dt 
$$
this integral is the Laplace transform of $\frac{\sin(2t)}{t}$ when $s=0$. We can see this by
$$
\mathcal{L}\{ \frac{\sin 2t}{t} \} = \int\limits_{0}^{\infty}e^{st} \frac{\sin 2t}{t} \ dt
$$
If $s=0$, we would get back our original integral. Now, we can write our improper integral as a Laplace transform in the form $\frac{f(t)}{t}$, thus we can use one of our identities to see that 
$$
\mathcal{L} \{ \frac{\sin 2t}{t} \} = \int\limits_{s}^{\infty} \mathcal{L}\{\sin 2t\} (u) \ du
$$
Now, we know that the Laplace transform of $\sin 2t$ is $\frac{2}{s^{2}+4}$ so we can write 
$$
\int\limits_{s}^{\infty} \frac{2}{u^{2}+4} \ du = \left. \frac{2}{2}\arctan \left(\frac{s}{2}\right) \right\rvert_{0}^{\infty} = \frac{\pi}{2}-\arctan\left(\frac{s}{2}\right)
$$
Now, plugging in $s=0$ we get 
$$
\boxed{\frac{\pi}{2}}
$$
