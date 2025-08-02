---
tags: Complex, Math, residue, application, branch, path, contour, integral, derivation, method, indented, indented_path, contour_integral
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Contour Integrals on Indented Paths_
Applications: _Solving Real Integrals using the complex plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Contour Integrals]],[[Cauchy Residue Theorem]],[[Complex Elementary Functions]],[[Application of Residues]]_
Cont.\_ of: _None_ 
_
_

In this page we illustrate the use of _indented paths_. We begin with an important limit that will be used 

###### Contour around Simple Pole Theorem
**Theorem.**  Suppose that 

(a) a function $f(z)$ has a simple pole at a point $z=x_{0}$ on the real axis, with a [[Laurent Series]] representation in a punctured disk $0<|z-x_{0}|<R_{2}$ and with residue $B_{0}$;

(b) $C_{\rho}$ denotes the upper half of the circle $|z-x_{0}|=\rho$, where $\rho<R_{2}$ and the clockwise direction is taken.

Then,
$$
\boxed{\lim_{\rho \rightarrow 0} \int\limits_{C_{\rho}}f(z) \ dz = -B_{0}\pi i}
$$
![[Screenshot 2023-08-02 154613.png|center]]

**Proof:**  Assuming that the conditions in part (a) and (b) are satisfied, we start the proof of the theorem by writing the [[Laurent Series]] in part (a) as 
$$
f(z) = g(z) + \frac{B_{0}}{z-x_{0}} \quad (0<|z-x_{0}|<R_{2})
$$
where 
$$
g(z) = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n} \quad (|z-x_{0}|<R_{2})
$$
Thus,
$$
\tag{1}
\int\limits_{C_{\rho}} f(z) \ dz = \int\limits_{C_{\rho}}g(z)\ dz + B_{0}\int\limits_{C_{\rho}} \frac{dz}{z-x_{0}}
$$
Now, the function $g(z)$ is continuous when $|z-x_{0}|<R_{2}$, according to the theorem in [[Properties of Complex Series#Continuity of Sums of Power Series|Continuity of Sums of Power Series]]. Hence if we choose a number $\rho_{0}$ such that $\rho<\rho_{0}<R_{2}$, it must be bounded on the _closed_ disk $|z-x_{0}|\leq \rho_{0}$, according to **Theorem 3.** in [[Complex Continuity]]. That is, there is a nonnegative constant $M$ such that 
$$
|g(z)|\leq M \quad \text{whenever} \quad |z-x_{0}|\leq \rho_{0};
$$
and since the length $L$ of the path $C_{\rho}$ is $L=\pi \rho$, it follows from the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Moduli Theorem]]that 
$$
\left| \int\limits_{C_{\rho}} f(z) \ dz \right| \leq ML = M \pi \rho
$$
Consequently, 
$$
\lim_{\rho\rightarrow 0} \int\limits_{C_{\rho}}g(z) \ dz = 0
$$
Inasmuch as the semicircle $-C_{\rho}$ has parametric representation
$$
z=x_{0}+\rho e^{i \theta} \quad (0\leq \theta\leq \pi)
$$
the second integral on the right in our equation (1) has the value
$$
\int\limits_{C_{\rho}} \frac{dz}{z-x_{0}} = -\int\limits_{-C_{\rho}} \frac{dz}{z-x_{0}} = -\int\limits_{0}^{\pi} \frac{1}{\rho e^{i \theta}} i \rho e^{i \theta} \ d \theta = -i \pi
$$
Thus,
$$
\lim_{\rho \rightarrow 0} \int\limits_{C_{\rho}} \frac{dz}{z-x_{0}} = -i \pi
$$
The limit in the conclusion of the theorem now follows by letting $\rho$ tend to zero on each side in equation (1) and referring to the two limits we just introduced.

**Remark.**  The $\rho_{0}$ number was brought about because we need to show that a function is continuous on a _closed_ domain to show that it is bounded. Thus, we wanted a number greater than $\rho$ such that all values of $g(z)$ in the contour created by $\rho$ are less than or equal to the maximum of $g(z)$ in the larger domain past $\rho$. And we need this number $\rho_{0}$ to be less than $R_{2n}$ such that the Laurent Series exists. 

##### Example.
We shall evaluate here **Dirichlet's Integral** 
$$
\int\limits_{0}^{\infty} \frac{\sin x}{x} \ dx = \frac{\pi}{2}
$$
by integrating $\frac{e^{iz}}{z}$ around the simple closed contour shown below. In this figure, $\rho$ and $R$ denote positive real numbers, where $\rho<R$; and $L_{1}$ and $L_{2}$ represent the intervals $\rho\leq x\leq R$ and $-R \leq x \leq -\rho$, respectively, one the real axis. The semicircle $C_{\rho}$ and $C_{R}$ are as shown in the figure. The semicircle $C_{\rho}$ is introduced here in order to avoid passing through the singularity of the quotient $\frac{e^{iz}}{z}$.

![[Screenshot 2023-08-02 211418.png|center]]

The [[Cauchy Goursat Theorem]], or [[Cauchy Residue Theorem]], shows us that 
$$
\int\limits_{L_{1}} \frac{e^{iz}}{z} \ dz + \int\limits_{L_{2}} \frac{e^{iz}}{z} \ dz + \int\limits_{C_{\rho}} \frac{e^{iz}}{z} \ dz + \int\limits_{C_{R}} \frac{e^{iz}}{z}\ dz = 0,
$$
or
$$
\int\limits_{L_{1}} \frac{e^{iz}}{z} \ dz + \int\limits_{L_{2}} \frac{e^{iz}}{z} \ dz  = -\int\limits_{C_{\rho}} \frac{e^{iz}}{z} \ dz - \int\limits_{C_{R}} \frac{e^{iz}}{z}\ dz
$$
Moreover, since the legs $L_{1}$ and $-L_{2}$ have parametric representations 
$$
z=re^{i \theta} = r \ (\rho\leq r \leq R) \quad \text{and} \quad z=re^{i \pi} = -r \ (\rho\leq r \leq R),
$$
respectively, the left-hand side of our equation can be written as 
$$
\int\limits_{L_{1}} \frac{e^{iz}}{z} \ dz + \int\limits_{L_{2}} \frac{e^{iz}}{z} \ dz  = \int\limits_{\rho}^{R} \frac{e^{ir}}{r} \ dr - \int\limits_{\rho}^{R} \frac{e^{-ir}}{-r} \ (-dr) = \int\limits_{\rho}^{R} \frac{e^{ir}-e^{-ir}}{r} \ dr = 2i \int\limits_{\rho}^{R} \frac{\sin r}{r} \ dr
$$
Consequently, our integral equation reduces down to 
$$
2i\int\limits_{\rho}^{R} \frac{\sin r}{r} \ dr = -\int\limits_{C_{\rho}} \frac{e^{iz}}{z} \ dz - \int\limits_{C_{R}} \frac{e^{iz}}{z} \ dz
$$
Now, from the [[Laurent Series]] representation 
$$
\frac{e^{iz}}{z} = \frac{1}{z}\left[1+\frac{iz}{1!}+ \frac{(iz)^{2}}{2!}+\ldots\right] = \frac{1}{z} + \frac{i}{1!} + \frac{i^{2}}{2!}z + \ldots \quad (0<|z|<\infty)
$$
it is clear that $\frac{e^{iz}}{z}$ has a simple pole at the origin, with residue unity. So, according to the theorem we stated before in on this page, 
$$
\lim_{\rho \rightarrow 0} \int\limits_{C_{\rho}} \frac{e^{iz}}{z} \ dz = -(1)\pi i = -\pi i
$$
Also, since 
$$
\left | \frac{1}{z} \right| = \frac{1}{|z|} = \frac{1}{R}
$$
when $z$ is a point on $C_{R}$, we know from [[Application of Residues#Jordan's Lemma|Jordan's Lemma]] that 
$$
\lim_{R \rightarrow \infty} \int\limits_{C_{R}} \frac{e^{iz}}{z} \ dz = 0
$$
Thus, by letting $\rho$ tend to $0$ and then letting $R$ tend to $\infty$, we arrive at the result 
$$
2i\int _{0}^{\infty} \frac{\sin r}{r} \ dr = \pi i
$$
which we can take the Real part of to get Dirichlet's integral result.

---
### An Indentation around A Branch Cut 
An indented path can often be used to avoid a branch point, as well as an isolated singularity. 

##### Example.
Lets derive the integration formula 
$$
\int\limits_{0}^{\infty} \frac{x^{a}}{(x^{2}+1)^{2}} \ dx = \frac{(1-a)\pi}{4 \cos \left(a \frac{\pi}{2}\right)} \quad (-1<a<3)
$$
where $a$ is a real number with the indicated restriction and $x^{a} = e^{a \ln x}$ when $x>0$. To do this, we shall use the function 
$$
f(z) = \frac{z^{a}}{(z^{2}+1)^{2}} = \frac{ e^{a \log x}}{(z^{2}+1)^{2}} \quad \left(|z|>0,\ \frac{-\pi}{2} < arg \ z < \frac{3 \pi}{2}\right)
$$
whose branch cut is the origin and the negative imaginary axis. The path of integration is shown below, where $\rho<1<R$ and the branch cut is indicated with a hollow dot and dashes.

![[Screenshot 2023-08-05 155543.png|center]]

Starting the [[Cauchy Residue Theorem]], we write 
$$
\int\limits_{L_{1}} f(z) \ dz + \int\limits_{L_{2}} f(z) \ dz = 2\pi i \ Res_{z=i} \ f(z) - \int\limits_{C_{\rho}}f(z) \ dz - \int\limits_{C_{R}} f(z) \ dz
$$
If we use the parametric equations
$$
z=re^{i 0} = r \ (\rho\leq r \leq R) \quad \text{and} \quad z=re^{i \pi} = -r \ (p \leq r \leq R)
$$
for $L_{1}$ and $-L_{2}$, respectively, we can write the left-hand side of this equation as 
$$
\int\limits_{L_{1}} f(z) \ dz - \int\limits_{-L_{2}} f(z) \ dz = \int\limits_{\rho}^{R} \frac{e^{a( \ln r + i 0)}}{(r^{2}+1)^{2}} \ dr + \int\limits_{\rho}^{R} \frac{e^{a (\ln r + i \pi)}}{(r^{2}+1)^{2}} \ dr = (1+e^{i a \pi}) \int\limits_{\rho}^{R} \frac{r^{a}}{(r^{2}+1)^{2}} \ dr
$$
Also,
$$
Res_{z=i} \ f(z) = \phi'(i) \quad \text{where} \quad \phi(z) = \frac{z^{a}}{(z+i)^{2}}
$$
since there is a pole of order $m=2$ at the point $z=i$. We can use straightforward differentiation to see that 
$$
Res_{z=i} \ f(z) = e^{(a-1) \log i} \left[ \frac{(a-2)(i)+ai}{(i+i)^{3}}\right] = -ie^{ia \frac{\pi}{2}} \left(\frac{1-a}{4}\right)
$$
Upon substituting these expressions into our original integral equation, we see that 
$$
(1+e^{ia \pi}) \int\limits_{\rho}^{R} \frac{r^{a}}{(r^{2}+1)^{2}} \ dr = \frac{\pi(1-a)}{2}e^{ia \frac{\pi}{2}} - \int\limits_{C_{\rho}} f(z)\ dz - \int\limits_{C_{R}} f(z) \ dz
$$
and once we show that 
$$
\lim_{\rho \rightarrow 0} \int\limits_{C_{\rho}} f(z)\ dz = 0 \quad \text{and}\quad \lim_{R \rightarrow \infty} \int\limits_{C_{R}} f(z) \ dz = 0
$$
the desired integration formula, with a different variable of integration, follows:
$$
\int\limits_{0}^{\infty} \frac{r^{a}}{(r^{2}+1)^{2}} \ dr = \pi\frac{1-a }{2} \cdot \frac{e^{ia \frac{\pi}{2}}}{1+e^{ia \pi}}  = \frac{\pi(1-a)}{4} \cdot \frac{2}{e^{ia \frac{\pi}{2}}+e^{-ia \frac{\pi}{2}}} = \frac{(1-a) \pi}{4\cos\left(a \frac{\pi}{2}\right)}
$$
The limits of the contour integrals are found by first observing that $|z^{a}|=r^{a}$ when $z=re^{i \theta}$ is any point on the closed contour. Also,
$$
|z^{2}+1| \geq ||z|^{2}-1| = |R^{2}-1| = R^{2}-1
$$
when  $z$ is a point on $C_{R}$. When $z$ is a point on $C_\rho$,
$$
|z^{2}+1| \geq ||z|^{2}-1| = 1-\rho^{2}
$$
**Remark.**  The absolute values here are evaluated under the conditions that $R \geq 1$ and $\rho<1$. This is indeed true when we take these limits, so that's what we use for the absolute values. And since the absolute values are positive, then squaring them results strictly in $a>b$, $a^{2}>b^{2}$.

Now, we can write, using the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Moduli Theorem]]:
$$
\left| \int\limits_{C_{\rho}} \frac{z^{a}}{(z^{2}+1)^{2}}\ dz  \right| \leq \frac{\rho^{a}}{(1-\rho^{2})^{2}} \pi \rho =  \frac{\pi \rho^{a+1}}{(1-\rho^{2})^{2}}
$$
and we note that the limit of this as $\rho \rightarrow 0$ will approach $0$ as long as $a+1>0$, or $a>-1$. Looking at our other contour integral,
$$
\left| \int\limits_{C_{R}} \frac{z^{a}}{(z^{2}+1)^{2}} \ dz \right| \leq \frac{R^{a}}{(R^{2}-1)^{2}} \pi R = \frac{\pi R^{a+1}}{(R^{2}-1)^{2}}
$$
and we see that this limit will approach $0$ as $R \rightarrow \infty$ as long as $a+1<4$, or $a<3$. So, we finally have our integral result 
$$
\boxed{\int\limits_{0}^{\infty} \frac{x^{a}}{(x^{2}+1)^{2}} \ dx = \frac{(1-a)\pi}{4 \cos \left(a \frac{\pi}{2}\right)} \quad (-1<a<3)}
$$

---
### An Indentation Along a Branch Cut
The [[Cauchy Residue Theorem]] can be useful in evaluating integrals from real analysis when part of the path of integration of the function $f(z)$ to which the theorem is applied lies along a branch cut of that function.

##### Example.
Let $x^{-a}$, where $x>0$ and $0<a<1$, denote the principle value of the indicated power of $x$; that is, $x^{-a}$ is the positive real number $e^{-a \ln x}$. We shall evaluate the improper integral 
$$
\int\limits_{0}^{\infty}\frac{x^{-a}}{x+1} \ dx \quad (0<a<1),
$$
which is important in the study of the _Gamma Function_. Note that this integral is improper not only because of its upper limit of integration but also because its integrand has an infinite discontinuity at $x=0$. The integral converges then $0<a<1$ since the integrand behaves like $x^{-a}$ near $x=0$ and like $x^{-a-1}$ as $x$ tends to $\infty$. We do not, however, need to establish convergence separately; for that will be contained in our evaluation of the integral. 

We begin by letting $C_{\rho}$ and $C_{R}$ denote the circles $|z|=\rho$ and $|z|=R$, respectively, where $\rho<1<R$; and we assign them the orientations shown in the figure. 

![[Screenshot 2023-08-06 011030.png|center]]

We then integrate the branch 
$$
f(z) = \frac{z^{-a}}{z+1} \quad (|z|>0, \ 0< arg \ z < 2 \pi) 
$$
of the multiple-valued function $f(z)$, with branch cut $arg \ z = 0$, around the simple closed contour indicated in the figure. That contour is traced out by a point moving from $\rho$ to $R$ along the top of the branch cut for $f(z)$, next around $C_{R}$ and back to $R$, then along the bottom of the cut to $\rho$, and finally around $C_{\rho}$ back to $\rho$. 

Now, $\theta=0$ and $\theta=2 \pi$ along the upper and lower "edges", respectively, of the cut annulus that is formed. Since 
$$
f(z) = \frac{e^{-a \log z}}{z+1} = \frac{e^{-a (\ln r + i \theta)}}{re^{i \theta}+1}
$$
where $z=re^{i \theta}$, it follows that 
$$
f(z) = \frac{r^{-a}}{r+1}
$$
on the upper edge where $z=re^{i 0}$, and 
$$
f(z) = \frac{r^{-a} e^{-i 2 \pi a}}{r+1}
$$
on the lower edge, where $z=re^{i 2 \pi}$. The residue theorem thus suggests that 
$$
\int\limits_{\rho}^{R} \frac{r^{-a}}{r+1} \ dr + \int\limits_{C_{R}} f(z) \ dz - \int\limits_{\rho}^{R} \frac{r^{-a} e^{-i 2 \pi a}}{r+1} \ dr + \int\limits_{C_{\rho}}f(z) \ dz = 2 \pi i \ Res_{z=-1} \ f(z)
$$
Our derivation of this equation, is only _formal_ since $f(z)$ **is not analytic, or even defined, on the branch cut involved**. It is, nevertheless, valid and can be fully justified by <mark style="background: #FFB86CA6;">exercise 6 in Sec. 91</mark> of [[Complex Variables Textbook.pdf]]. We also know that integrals have the condition of piecewise continuity; thus, we only need a function to have defined one-sided limits to integrate it. If we take the limit of $f(z)$ as $\theta \rightarrow 0$ and $\theta \rightarrow 2 \pi$, we can easily see that these one-sided limits exist. Thus, while the function is *not* defined on the branch cut, we can still do the contour integral. 

The residue in our integral equation can be found by noting that the function 
$$
\phi(z) = z^{-a} = e^{-a \log z} = e^{-a(\ln r + i \theta)} \quad (r>0, \ 0<\theta<2 \pi)
$$
is analytic at $z=-1$ and that 
$$
\phi(-1 ) = e^{-a(\ln 1 + i \pi)} = e^{-ia \pi} \neq 0
$$
This shows that the point $z=-1$ is a simple pole of the function and that 
$$
Res_{z=-1} \ f(z) = e^{-ia \pi}
$$
We can thus write our integral equation as 
$$
(1-e^{-2ia \pi}) \int\limits_{0}^{\infty} \frac{r^{-a}}{r+1} \ dr = 2 \pi i e^{-ia \pi} - \int\limits_{C_{\rho}} f(z)\ dz - \int\limits_{C_{R}}f(z) \ dz
$$
According to the definition of $f(z)$ and how we initially defined the contours, using the same methods as in the last example:
$$
\left| \int\limits_{C_{\rho}}f(z) \ dz \right| \leq M_{\rho} L = \frac{\rho^{-a}}{1-\rho} 2 \pi \rho = \frac{ 2 \pi}{1-\rho} \rho^{1-a}
$$
and 
$$
\left| \int\limits_{C_{R}} f(z) \ dz \right| \leq M_{R}L = \frac{R^{-a}}{R-1} 2 \pi R = \frac{2 \pi R}{R-1} R^{-a}
$$
Since $0<a<1$, the values of the two integrals evidently tend to $0$ as $\rho$ and $R$ tend to $0$ and $\infty$, respectively. Hence, if we let $\rho \rightarrow 0$ and $R \rightarrow \infty$ in our integral equation, we arrive at the result 
$$
(1-e^{-i2a \pi}) \int\limits_{0}^{\infty} \frac{r^{-a}}{r+1} \ dr = 2 \pi i e^{-ia \pi}
$$
or 
$$
\int\limits_{0}^{\infty} \frac{r^{-a}}{1+r} \ dr = 2 \pi i \frac{e^{-ia \pi}}{1-e^{-i2a \pi}} = \pi \frac{2 i }{e^{i a \pi}-e^{-ia \pi}} = \frac{\pi}{\sin (\pi a)}
$$
Thus,
$$
\int\limits_{0}^{\infty} \frac{x^{-a}}{x+1} \ dx = \frac{\pi}{\sin (\pi a)} \quad (0<a<1)
$$



