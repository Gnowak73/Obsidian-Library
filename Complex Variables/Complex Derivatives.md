---
tags: derivative, complex, Math, complex_analysis
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Derivatives_
Applications: _Functional Analysis on Complex Plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Continuity]], [[Analytic Functions]], [[Complex Limits]]_
Cont.\_ of: _None_ 
_
_
```ad-Definition
Let $f$ be a function whose [[Complex Functions and Mappings|domain of definition]] contains a neighborhood $|z-z_{0}|<\epsilon$ of a point $z_{0}$. The _derivative_ of f at $z_{0}$ is the [[Complex Limits|limit]]:
$$
f'(z_{0}) = \lim_{z\rightarrow z_{0}}\frac{f(z)-f(z_{0})}{z-z_{0}},
$$
and the function $f$ is said to be _differentiable_ at $z_{0}$ when $f'(z_{0})$ exists. 
```

We can actually express this limit in terms of the LHS and RHS limits by making the variable $\Delta z =z-z_{0}$ such that 
$$
f'(z_{0}) = \lim_{\Delta z\rightarrow 0} \frac{f(z_{0}+\Delta z)-f(z_{0})}{\Delta z}
$$
or 
$$
f'(z_{0}) = \lim_{\Delta z\rightarrow 0} \frac{f(z_{0}-\Delta z)-f(z_{0})}{-\Delta z}
$$
**Remark.**  On the complex plane, a function can have existing and continuous partial derivatives at a point but still but be differentiable at that point. Also, functions containing $\overline{z}$ will most likely need to be handled using the limit definition of the derivative. 


**All Rules for differentiation are the same as for real functions.**

```ad-Remember
The _Mean Value Theorem_ **DOES NOT** work anymore on the complex plane due to being able to express each complex number as $e^{i\theta}$ with Euler's formula. The periodicity of complex numbers results in a non one-one formulation of derivatives.  

The mean value theorem is:
$$
w'(c) = \frac{w(b)-w(a)}{b-a}
$$
for some number in the interval $a<c<b$
```

### Cauchy Riemann Equations 
The Cauchy-Riemann equations are a pair of equations that the first order partial derivatives of the component functions $u$ and $v$ of a function 
$$
f(z)=u(x,y)+iv(x,y)
$$
must satisfy at a point $z_{0}$ when the derivative of $f$ exists there. We can also use this to express $f'(z_{0})$ in terms of those partial derivatives. The proof and derivation can be found in [[Complex Variables Textbook.pdf]]. It originates from the idea that the limit must be the same no matter which way you approach it from. 
$$

\cases{u_{x}=v_{y}, \\ 
u_{y}=-v_{x}}
$$
If this is true, then we can write 
$$
\boxed{f'(z_{0}) = u_{x}+iv_{x}}
$$
```ad-Remember
The Cauchy-Riemann equations **are NOT** (even if $f$ is continuous) enough to prove a function is [[Analytic Functions|analytic]]! It must satisfy these equations **AND** the partial derivatives must be [[Complex Continuity|continuous]] (continuous in the neighborhood of $z_{0}$)!
```

##### Polar Coordinates 
We can also express the Cauchy-Riemann equations in polar coordinates for a function $f(z)=u(r,\theta)+iv(r,\theta)$ 
$$
\cases{ru_{r}=v_{\theta}\\
u_\theta=-rv_{r}}
$$
then,
$$
\boxed{f'(z) = e^{-i\theta}(u_{r}+iv_{r})}
$$