---
tags: Math, D'Alambert, Wave_equation, derivation, PDE
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _Wave Equation D'Alambert_
Applications: _Waves, EM, Physics_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
The D'Alambert solution to the wave equation is a unique method to "factor" partial differential equations to get a solution. The wave equation is as follows:
$$
\partial_{tt}u - c^{2}\partial_{xx}=0
$$
we try to factor this as 
$$
(\partial_t-c)(\partial_{t}+c)u= 0.
$$
Due to the Linearity of this equation, we can expect that each one of these factor's solution added is the general solution for this equation (which can be seen from using [[Method of Characteristics (PDE)]] on both factors). This comes out to be 
$$
u=f(x+ct)+g(x-ct)
$$
---
For the actual proof of this. Let us look at the factors in the PDE. We see that we have two solutions of one dimension. Now, realize that a general solution is just the union of the spaces for the separate solutions. Now, we must carefully consider mixed solution if we want to do this. In other words, we would consider a point in which we go from one solution to another solution. But our equation is linear, so we can just add them! 

Is this not good enough yet? Well, lastly, we could always use the variable substitution $\eta=x-ct, \zeta=x+ct$ to make the PDE turn into a simpler PDE with this general solution when integrating both sides. Since the composition of our PDE is two different directional derivatives whose characteristics are represented by $x+ct$ and $x-ct$, we know that this substitution will probably be the best one. This is the reasoning behind this specific change of variables. Full proof in [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]

---
Lets say that we define the initial conditions $u(x,0)=\phi(x)$ and $u_{t}(x,0)=\psi(x)$ on the interval $x \in (-\infty, \infty), \ t>0$.

Now, our goal is to find how the solution $u(x,t)=f(x+ct)+g(x-ct)$ will relate to the functions $\phi, \psi$. We can first note that
$$
u(x,0) = f(x)+g(x) = \phi
$$
and since $u_{t}(x,t)=cf'(x+ct)-cg'(x-ct)$, 
$$
u_{t}(x,0) = cf'(x)-cg'(x) = \psi
$$

For simplicity, we will replace $x$ with a dummy variable $\alpha$ to give us
$$
\phi(\alpha) = f(\alpha)+g(\alpha), \quad \psi(\alpha)=cf'(\alpha)-cg'(\alpha)
$$
If we differentiate this first function function we get
$$
\phi'(\alpha) = f'(\alpha) + g'(\alpha), \quad \psi(\alpha) = cf'(\alpha)-cg'(\alpha)$$
Now, we can solve this system for $f'$ and $g'$ as functions of $\phi'$ and $\psi$:
$$
f'(\alpha)=\frac{1}{2}\left(\phi'(\alpha) + \frac{\psi(\alpha)}{c}\right), \quad g'(\alpha)=\frac{1}{2}\left(\phi'(\alpha) - \frac{\psi(\alpha)}{c}\right)
$$
Integrating with respect to $\alpha$ gives us
$$
f(\alpha) = \frac{1}{2}\phi(\alpha) + \frac{1}{2c}\int\limits_{0}^{\alpha}\psi(s)ds + C_{1} ,\quad g(\alpha) = \frac{1}{2}\phi(\alpha) -\frac{1}{2c}\int\limits_{0}^{\alpha}\psi(s)ds + C_{2}
$$
We see that $\phi(\alpha)=f(\alpha)+g(\alpha)$, so $C_{1}+C_{2}=0$. Since the constants added don't matter, that is why our integral is going from $0$ to $\alpha$, because the constant that would come to compensate for the $\Psi(0)$ will be taken care of in the constant of integration. The definite integration is also useful because it allows us to get rid of using a constant of integration completely in our solution. Now we can construct:
$$
u(x,t) = f(x+ct)+g(x-ct) = \frac{1}{2}[\phi(x+ct)+\phi(x-ct)] + \frac{1}{2c}\int\limits_{x-ct}^{x+ct}\psi(s) \ ds
$$

This is for an infinite string. For a partially infinite string, we can use this same method except we have to apply an extension to odd waves on the string in order to use the data $x-ct$ needed in the solution that would come from a negative $x$.

For finite strings, we must use [[Separation of Variables (PDE technique)]]. 


##### Domain of Dependence and Independence
When we look at the integral in our solution, we see that in the first portion we are taking <mark style="background: #D2B3FFA6;">the average of the initial displacements</mark> at the positions $x-ct$ and $x+ct$, we then add this to the <mark style="background: #FFB86CA6;">average velocity</mark> of the string over the interval $[x-ct,x+ct]$ multiplied by time (or the average displacement of string string segment).

We realize that this solution exists in a domain which requires information between $x-ct$ and $x+ct$. The interesting part about this is that for a non-infinite string, $x-ct$ could be negative and go past our endpoint, which means we need to extend our solution to all of $\mathbb{R}$ <mark style="background: #BBFABBA6;">via odd reflections</mark>. 

To see the domain of dependence(looking backward in time) and influence(looking forward in time), we consider the interval $[x_{0}-c(t_{0}-t_{1}),x_{0}+c(t_{0}-t_{1})]$. Where $t_{1}$ is the initial time and $t_{0}$ is the time currently ($0<t_{1} <t_{0}$). We can now try to determine what positions are relevant at time $t_{1}$ for determining $u(x_{0},t_{0})$. We look at what happens when $t_{1}$ goes from $t_{0}$ and we wind back the clock until it equals $0$. We see that the domain keeps getting smaller. And we can actually graph it.

Before we show the graphs, we also think about what happens if we look towards the future. If we take the same interval but instead we are looking at $t_{0}$ starting from $t_{0}=t_{1}$, as we increase $t_{0}$ we will get an infinite domain.  

![[Pasted image 20230625161617.png]]

##### Sources
We can use [[Green's Theorem (circulation)]] or [[Duhamel's Principle]] over the domain of dependence in order to solve the wave equation for a driving source on the string. Both of these can be seen in section 3.6.1+ of [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]].