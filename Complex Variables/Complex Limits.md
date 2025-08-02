---
tags: Math, complex, limits, complex_limits, functions, neighborhood, theorem, derivation, Riemann, Riemann_Sphere, extended_complex_plane
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Limits_
Applications: _Limits, Derivatives, functional analysis on Complex Plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Continuity]],[[Complex Derivatives]]_
Cont.\_ of: _None_ 
_
_
```ad-Definition
Let a function $f$ be defined at all points $z$ in some deleted neighborhood of a point $z_{0}$. The statement that $f(z)$ has a _Limit_ $w_{0}$ as $z$ approaches $z_{0}$ is that 
$$
\lim_{z\rightarrow z_{0}} f(z) = w_{0},
$$
or that the point $w=f(z)$ can be made arbitrarily close to $w_{0}$ if we choose the point $z$ close enough to $z_{0}$ but distinct from it.


More formally defined: this means that for each positive number $\epsilon$, there is a positive number $\delta$ such that 
$$
|f(z)-w_{0}|<\epsilon, \quad \text{whenever} \quad  0<|z-z_{0}|<\delta
$$

```

In a sense, if we can prove that there exists some relationship between $\epsilon$ and $\delta$ such that this holds for any number. Then we can chose arbitrary numbers closer and closer to $z_{0}$ such that the function will converge to $w_{0}$.


**Theorem.** When a limit of a function $f(z)$ exists at a point $z_{0}$, it is unique. 
**Proof:** Let us suppose that 
$$
\lim_{z \rightarrow z_{0}} f(z) = w_{0},\quad \text{and} \quad \lim_{z \rightarrow z_{0}}f(z) = w_{1} 
$$
Then, for each positive number $\epsilon$, there are positive numbers $\delta_{0}$ and $\delta_{1}$ such that 
$$
|f(z)-w_{0}|<\epsilon \quad \text{whenever} \quad 0<|z-z_{0}|<\delta_{0} 
$$
and
$$
|f(z)-w_{1}|<\epsilon, \quad \text{whenever} \quad 0<|z-z_{0}|<\delta_{1}.
$$
Since 
$$
w_{1}-w_{0} = [f(z)-w_{0}]+[w_{1}-f(z)]
$$
the [[Complex Numbers Algebraic Properties#Triangle Inequality|triangle inequality]] will tell us that 
$$
|w_{1}-w_{0}| \leq |f(z)-w_{0}|+|w_{1}-f(z)|
$$
So if $0<|z-z_{0}|\leq \delta$ where $\delta$ is a positive number smaller than $\delta_{0}$ and $\delta_{1}$, we find that 
$$
|w_{1}-w_{0}|<\epsilon+\epsilon<2\epsilon
$$
But $|w_{1}-w_{0}|$ is a nonnegative constant, and $\epsilon$ can be chosen arbitrarily small, so we can chose $\epsilon=0$ such that 
$$
w_{1}-w_{0}=0 \rightarrow \boxed{w_{1}=w_{2}}
$$

##### Interesting Example Limit
If we have the limit 
$$
\lim_{z\rightarrow 0} \frac{z}{\overline{z}}
$$
we see that the limit does not exist. But Why? Well, we were to chose a point $z=(x,y)$ and let it approach the origin in any manner, we would see that for a point such as $z=(x,0)$, we would get 
$$
\frac{z}{\overline{z}}= \frac{z+i0}{x-i0} = 1
$$
but for a point approaching from the imaginary axis $z=(0,y)$ we would get 
$$
\frac{z}{\overline{z}} = \frac{0+iy}{0-iy} = -1
$$
We quickly realize that we must have a condition where for a limit to exist, it must be approached in the same way from all points on the complex plane. This is very similar to multivariable limits, where we must consider the path of the limits.

---

### Theorems on Limits
We can expedite our treatment of limits by establishing a connection between limits of functions of a complex variable and limits of real-valued functions of two real variables. Since limits of the latter type are studied in calculus, we may use their definition and properties freely. Proofs can be seen in [[Complex Variables Textbook.pdf]].

**Theorem 1.**  Suppose that 
$$f(z)=u+iv \quad \text{and} \quad z_{0}=x_{0}+iy_{0},\quad w_{0}=u_{0}+iv_{0}$$If 
$$
\lim_{(x,y)\rightarrow(x_{0},y_{0})} u(x,y) = u_{0} \quad \text{and} \quad \lim_{(x,y)\rightarrow(x_{0},y_{0})} v(x,y) = v_{0}
$$
then
$$
\lim_{z\rightarrow z_{0}
}f(z) = w_{0}$$
In other words, we can split a limit into its real and imaginary parts (since the limit is a linear operator). 

**Theorem 2.**  We can separate a limit by multiplication if the limit of both terms exists.

**Theorem 3.**  We can also separate a limit by rational function as long as both limits exist and the denominator doesn't become $0$.

**Theorem 4.**  The Limit acts like a function and can be used with Composition as long as the limit exists:
$$
\lim_{z\rightarrow z_{0}}f(g(z)) =f(\lim_{z\rightarrow z_{0}}g(z)) 
$$

---

### Limits Involving the Point at Infinity

We complex plane together with the _point at infinity_ is called the _extended complex plane_. To visualize the point at infinity, one can think of the complex plane as passing through the equator of a unit sphere centered at the origin. To each point $z$ in the plane there corresponds exactly one point $P$ on the surface of the sphere. In like manner, to each point $P$ on the surface of the sphere, other than the north pole $N$, there corresponds exactly one point $z$ in the plane. By letting the point $N$ on the sphere correspond at infinity, we obtain a one to one correspondence between the points on the sphere and the points in the extended complex plane. This sphere is known as the _Riemann sphere_, and the correspondence is called a _stereographic projection_. 
![[Pasted image 20230703165857.png|center]]

**Theorem.**  If $z_{0}$ and $w_{0}$ are points in the $z$ and $w$ planes, respectively, then 
$$
\lim_{z\rightarrow z_{0}} f(z) = \infty \quad \text{if} \quad \lim_{z\rightarrow z_{0}} \frac{1}{f(z)} = 0
$$
and 
$$
\lim_{z\rightarrow \infty} f(z) = w_{0} \quad \text{if} \quad \lim_{z\rightarrow 0} f\left(\frac{1}{z}\right) = w_{0}
$$


