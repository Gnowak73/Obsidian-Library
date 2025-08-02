---
tags: Math, Complex, Residues, theorem, application, contour, integral
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Application of Residues_
Applications: _Real Analysis_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Residues, Zeros, and Poles]],[[Cauchy Residue Theorem]],[[Integration Methods]]_
Cont.\_ of: _None_ 
_
_

**Important Formulations:**

1. [[#Evaluation of Improper Integrals]]: Shows basic idea of using [[Cauchy Residue Theorem]] for real analysis.
2. [[#Improper Integrals From Fourier Analysis]]: Show basic idea of solving integrals that show up in Fourier analysis from sines and cosines and exponentials. 
3. [[#Jordan's Lemma]]: Lemma that allows us to show how an exponential integral (like in the Fourier Analysis) along contour approaches $0$ when when evaluating improper integrals like before. Basically an extension of the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Modulus Theorem]] to exponentials multiplied by some bounded function.  Upper bounds theorem for contour integral of: $f(z)e^{iaz}$
4. [[Contour Integrals Indented Paths]]: Shows how to contour integrate around indented paths to avoid singularities or integrate around/on branch cuts. Applications of this using [[Cauchy Residue Theorem]] allows us to evaluate improper real integrals. Useful to get around singularities and branches! 
5. [[Contour Integrals Indented Paths#Contour around Simple Pole Theorem|Contour Integral around Simple Pole Theorem]]: Theorem for a function $f(z)$ which has a _simple pole_ and is represented by a [[Laurent Series]] in some punctured disk and we have a contour of a _upper half circle with the real axis_, in this disk. Upper bounds theorem for contour integral of $f(z)$ under these conditions.
6. [[Definite Integrals Involving Sines and Cosines]] : Solving real, definite integrals with functions of $\sin$ and $\cos$ going from $0$ to $2 \pi$. Can be used for other intervals as long as they are symmetric in some way to extend them to $[0, 2 \pi]$. 
7. [[Argument Principle and Rouche's Theorem]]: Explanation of the argument principle, a number describing complex image transforms, along with Rouche's theorem which can identify how many zeros, including multiplicities, exist in a specific region for a function $f(z)+g(z)$. 
8. [[Bromwich Integral]]: The integral associated with the inverse [[Laplace Transforms]] and their evaluations. 


---
## Evaluation of Improper Integrals
In calculus, the improper integral of a continuous function $f(x)$ over the semi-infinite interval $0\leq x\leq \infty$ is defined by means of the equation
$$
\int\limits_{0}^{\infty}f(x) \ dx = \lim_{R \rightarrow \infty } \int\limits_{0}^{R}f(x) \ dx
$$
When the limit on the right exists, the improper integral is said to _converge_ to that limit. For all $x$, we can see that 
$$
\tag{1}
\int\limits_{-\infty}^{\infty} f(x) \ dx = \lim_{R_{1}\rightarrow \infty}\int\limits_{-R_{1}}^{0}f(x) \ dx + \lim_{R_{2}\rightarrow \infty} \int\limits_{0}^{R_{2}}f(x) \ dx
$$
When both limits exist, we say the integral _converges_ to their sum. But there is also another value that is assigned to integrals that is often useful too: the **Cauchy Principle Value (P.V.)**. 

```ad-Definition
The **Cauchy principle value** of an integral is defined as 
$$
\text{P.V.} \int\limits_{-\infty}^{\infty}f(x) \ dx = \lim_{R\rightarrow \infty} \int\limits_{-R}^{R} f(x) \ dx
$$
provided that this single limit exists.
```

**Remark.**  If integral (1) converges, then so does its Cauchy principle value; and that value is the number which integral (1) converges to. This is because 
$$
\lim_{R \rightarrow \infty} \int\limits_{-R}^{R}f(x) \ dx = \lim_{R\rightarrow \infty} \left[\int\limits_{-R}^{0}f(x) \ dx + \int\limits_{0}^{R} f(x) \ dx\right] = \lim_{R \rightarrow \infty} \int\limits_{-R}^{0}f(x) \ dx + \lim_{R \rightarrow \infty}\int\limits_{0}^{R} f(x) \ dx
$$
and these last two limits are the same as the limits on the right in equation (2). 
```ad-warning
It is **not**, however, always true that integral (2) converges when its Cauchy principle value exists.
```

But let us suppose that $f(x) \ (-\infty < x < \infty)$ is an _even_ function, one where 
$$
f(x)=f(-x) \quad \forall x\in \mathbb{R},
$$
and _assume_ that the Cauchy Principle Value exists. The symmetry of the graph of $y=f(x)$ with respect to the $y$ axis tells us that 
$$
\int\limits_{-R_{1}}^{0}f(x) \ dx = \frac{1}{2}\int\limits_{-R_{1}}^{R_{1}}f(x) \ dx
$$
and 
$$
\int\limits_{0}^{R_{2}}f(x) \ dx = \frac{1}{2}\int\limits_{-R_{2}}^{R_{2}}f(x) \ dx
$$
Thus, 
$$
\int\limits_{-R_{1}}^{0}f(x) \ dx + \int\limits_{0}^{R_{2}}f(x) \ dx = \frac{1}{2}\int\limits_{-R_{1}}^{R_{1}}f(x) \ dx + \frac{1}{2}\int\limits_{-R_{2}}^{R_{2}}f(x) \ dx
$$
If we let $R_{1}$ and $R_{2}$ tend to $\infty$ on each side, the fact that the limits on the right exist means that the limits on the left do too. In fact, 
$$
\boxed{\int\limits_{-\infty}^{\infty}f(x) \ dx = \text{P.V.}\int\limits_{-\infty}^{\infty}f(x) \ dx}
$$
Moreover, since
$$
\int\limits_{0}^{R}f(x) = \frac{1}{2}\int\limits_{-R}^{R}f(x) \ dx,
$$
it is also true that 
$$
\boxed{\int\limits_{0}^{\infty}f(x) \ dx = \frac{1}{2}\left[\text{P.V.}\int\limits_{-\infty}^{\infty}f(x) \ dx\right]}
$$


###### Example 1.
$$
\text{P.V.} \int\limits_{-\infty}^{\infty}x \ dx = \lim_{R \rightarrow \infty} \int\limits_{-R}^{R}x \ dx = \lim_{R\rightarrow \infty} \left. \frac{x^{2}}{2} \right\rvert_{-R}^{R} = \lim_{R \rightarrow \infty} 0 = 0.
$$
On the other hand,
$$
\int\limits_{-\infty}^{\infty}x \ dx = \lim_{R_{1}\rightarrow \infty} \int\limits_{-R_{1}}^{0} x \ dx + \lim_{R_{2}\rightarrow \infty} \int\limits_{0}^{R_{2}} x \ dx = \lim_{R_{1}\rightarrow \infty} \left. \frac{x^{2}}{2} \right\rvert_{-R_{1}}^{0} + \lim_{R_{2}\rightarrow \infty} \left. \frac{x^{2}}{2} \right\rvert_{0}^{R_{2}} 
$$
and since these last two limits _do not exist_, we find that the improper integral fails to exist. 

### Residues
We now describe a method involving sums of residues, that is often used to evaluate improper integrals of rational functions $f(x) = \frac{p(x)}{q(x)}$, where $p(x)$ and $q(x)$ are polynomials with real coefficients and no factors in common. We agree that $q(z)$ has _no real zeros_ but has _at least one zero above the real axis_. 

The method begins with the identification of all _distinct_ zeros of the polynomial $q(z)$ that _lie above the real axis_. They are, of course, finite in number (see [[Liouville's Theorem#Fundamental Theorem of Algebra|fundamental theorem of algebra]]), and may be labeled as $z_{1},z_{2},\ldots, z_{n}$, where $n$ is less than or equal to the degree of $q(z)$. We then integrate the quotient 
$$
f(z) = \frac{p(z)}{q(z)}
$$
around the positively oriented boundary of the semicircular region

![[Screenshot 2023-08-01 133002.png|center]]

That simple closed contour consists of the segment of the real axis from $z=-R$ to $z=R$ and the top half of the circle $|z|=R$, described counterclockwise and denoted by $C_{R}$. It is understood that the positive number $R$ is large enough so that the points $z_{1},z_{2},\ldots,z_{n}$ all le inside the closed path. 

The parametric representation $z=x \ (-R\leq x \leq R)$ of the segment of the real axis just mentioned and the [[Cauchy Residue Theorem]] can be used to write 
$$
\int\limits_{-R}^{R}f(x) \ dx + \int\limits_{C_{R}} f(z) \ dz = 2 \pi i \ \sum\limits _{k=1}^{n}Res_{z=z_{k}} \ f(z),
$$
or 
$$
\int\limits_{-R}^{R}f(x) \ dx = 2 \pi i \sum\limits_{k=1}^{n}Res_{z=z_{k}}  \ f(z) - \int\limits_{C_{R}}f(z) \ dz
$$
If
$$
\lim_{R \rightarrow \infty} \int\limits_{C_{R}} f(z) \ dz = 0, 
$$
then it follows that 
$$
\text{P.V.}\int\limits_{-\infty}^{\infty}f(x) \ dx = 2 \pi i \sum\limits_{k=1}^{n} Res_{z=z_{k}} \ f(z);
$$
and if $f(x)$ is _even_, these equations tell us that 
$$
\boxed{\int\limits_{-\infty}^{\infty}f(x) \ dx = 2 \pi i \sum\limits_{k=1}^{n}Res_{z=z_{k}} \ f(z)}$$
and 
$$
\boxed{\int\limits_{0}^{\infty}f(x) \ dx = \pi i \sum\limits_{k=1}^{n}Res_{z=z_{k}} \ f(z)}
$$
###### Example 1.
We turn to an illustration of the method described here. In order to evaluate the integral
$$
\int\limits_{0}^{\infty} \frac{dx}{x^{6}+1}$$
we start with the observation that the function
$$
f(z) = \frac{1}{z^{6}+1} 
$$
has isolated singularities at the zeros of $z^{6}+1$, which are the sixth roots of $-1$, and is analytic everywhere else. We use our previous method in [[Roots of Complex Numbers]] to see that the roots are 
$$
c_{k} = e^{\frac{i \pi}{6}} \cdot e^{\frac{i k \pi}{3}} \quad (n=0,1,2,\ldots,5)
$$
and it is clear that none of them are on the real axis. We see that the first three roots 
$$
c_{0}=e^{\frac{i \pi}{6}}, \quad c_{1}=i, \quad \text{and} \quad c_{2}=^{\frac{i 5 \pi}{6}}
$$
lie in the upper half plane and the other three lie in the lower plane. When $R>1$, the points $c_{k}$ lie in interior of the semicircular region bounded by the segment $z=x \ (-R\leq x\leq R)$ of the real axis and the upper half $C_{R}$ of the circle $|z|=R$ from $z=R$ to $z=-R$. Integrating $f(z)$ counterclockwise around the boundary of this semicircular region, we see that 
$$
\int\limits_{-R}^{R}f(x) \ dx + \int\limits_{C_{R}}f(z) \ dz = 2 \pi i (B_{0}+B_{1}+B_{2}) 
$$
Using **Theorem 2** from [[Zeros and Poles]], we can see that each $c_{k}$ is a simple pole of $f$ such that we can write that 
$$
B_{k} = Res_{z=c_{k}} \frac{1}{z^{6}+1} = \frac{1}{6c_{k}^{5}} = \frac{c_{k}}{6c_{k}^{6}} = \frac{c_{k}}{-6} \quad (k=0,1,2)
$$
Thus,
$$
B_{0}+B_{1}+B_{2} = \frac{-1}{ 6}(c_{0}+c_{1}+c_{2})
$$
If we think of the root $C_{2}=e^{\frac{i 5 \pi}{6}}$ as a point on the unit circle $|z|=1$, it is geometrically evident that $c_{2}$ can also be written as $c_{2}=-e^{\frac{-i \pi 5}{6}}$. Also, the definition of $\sin z$ from [[Complex Elementary Functions]] tells us that 
$$
e^{i \frac{\pi}{6}} - e^{-i \frac{\pi}{6}} = 2i \sin \left(\frac{\pi}{6}\right) = i
$$
These two observations enables us to write 
$$
B_{0}+B_{1}+B_{2} = \frac{-1}{6}\left(e^{i \frac{pi}{6}}+i-e^{-i \frac{\pi}{6}}\right)= \frac{-i}{3}
$$
Now, our integral equation becomes 
$$
\int\limits_{-R}^{R}f(x) \ dx = \frac{2\pi}{3} - \int\limits_{C_{R}}f(z) \ dz
$$
which is valid for all values of $R$ greater than unity. 

Next, we show that the integral on the right tends to $0$ as $R$ tends to $\infty$. To do this, we use the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper Bounds Moduli Theorem]]. Observe that when $R>1$, from the [[Complex Numbers Algebraic Properties#Triangle Inequality|Inverse Triangle Inequality]]: 
$$
|z^{6}+1| \geq ||z|^{6}-|1|| = R^{6}-1
$$
So, if $z$ is any point on $C_{R}$, 
$$
|f(z)| = \frac{1}{|z^{6}+1|} \leq M_{R}\quad \text{where} \quad M_{R} = \frac{1}{R^{6}-1};
$$
and this means that 
$$
\left|\int\limits_{C_{R}}f(z) \ dz \right| \leq M_{R} \pi R,
$$
$\pi R$ being the length of the semicircle $C_{R}$. Since the number 
$$
M_{R} \pi R  = \frac{\pi R}{R^{6}+1}
$$
is a quotient of polynomials in $R$ and since the degree of the numerator is less than the degree of the denominator, that quotient must tend to $0$ as $R$ tends to $\infty$. Thus
$$
\lim_{R\rightarrow \infty}\int\limits_{C_{R}}f(z) \ dz = 0
$$
It now follows from our integral equation that 
$$
\lim_{R \rightarrow \infty}\int\limits_{-R}^{R} \frac{dx}{x^{6}+1} = 2 \frac{\pi}{3}
$$
or
$$
\text{P.V.} \int\limits_{-R}^{R} \frac{dx}{x^{6}+1}
$$
Since the integrand here is even, we can then write that 
$$
\int\limits_{0}^{\infty} \frac{dx}{x^{6}+1} = \boxed{\frac{\pi}{3}}
$$
---
## Improper Integrals From Fourier Analysis
Residue theory can be used in evaluating improper integrals of the form 
$$
\int\limits_{-\infty}^{\infty}f(x) \sin(ax) \ dx \quad \text{or} \quad  \int\limits_{-\infty}^{\infty}f(x) \cos (ax) \ dx
$$
where $a$ denotes a positive constant. As previously, we assume that $f(x)$ is a rational function $f=\frac{p}{q}$ where $p(x)$ and $q(x)$ are polynomials with real coefficients and no factors in common. Also, $q(x)$ has no zeros on the real axis and at least one zero above it. 

The method described before cannot be directly applied since 
$$
|\sin az|^{2} = \sin^{2}ax + \sinh^{2}ay
$$
and 
$$
|\cos az|^{2} = \cos^{2}ax + \sinh^{2}ay
$$
More precisely, since 
$$
\sinh ay = \frac{e^{ay}-e^{-ay}}{2}
$$
the moduli $|\sin az|$ and $|\cos az|$ increase like $e^{ay}$ as $y$ tends to $\infty$. The modification illustrated in the example below is suggested by the fact that 
$$
\int\limits_{-R}^{R}f(x) \cos ax \ dx + i\int _{-R}^{R}f(x) \sin ax \ dx = \int\limits_{-R}^{R}f(x)e^{i a x} \ dx,
$$
together with the fact that the modulus 
$$
|e^{iaz}| = |e^{ia(x+iy)}| = |e^{-ay}e^{iax}| = e^{-ay}
$$
is bounded in the upper half plane $y\geq 0$. 

##### Example. 
Let us show that 
$$
\int\limits_{0}^{\infty} \frac{\cos 2x}{(x^{2}+4)^{2}} \ dx = \frac{5 \pi}{32e^{4}}
$$
We introduce the function 
$$
f(z) = \frac{1}{(z^{2}+4)^{2}}
$$
and observe that the product $f(z)e^{i2z}$ is analytic everywhere on and above the real axis except at the point $z=2i$. This singularity lies in the interior of the semicircular region whose boundary consists of the segment $-R\leq x\leq R$ of the real axis and the upper half $C_{R}$ of the circle $|z|=R \ (R>2)$ from $z=R$ to $z=-R$. Integration of $f(z)e^{i2z}$ around that oriented boundary yields the equation
$$
\int\limits_{-R}^{R} \frac{e^{i2x}}{(x^{2}+4)^{2}} \ dx = 2\pi i B - \int\limits_{C_{R}}f(z)e^{2iz} \ dz
$$
where 
$$
B = Res_{z=2i} \ [f(z)e^{2iz}]
$$
![[Screenshot 2023-08-01 174435.png|center]]

Since 
$$
f(z) = \frac{\phi(z)}{(z-2i)^{2}} \quad \text{where} \quad \phi(z) = \frac{e^{2iz}}{(z+2i)^{2}},
$$
the point $z=2i$ is evidently a pole of order $m=2$ of the product $f(z)e^{2iz}$ and it is straightforward to show that 
$$
B = \phi'(2i) = \frac{5}{32e^{4}i}
$$
By equating the real parts on each side of the integral equation from before, we find that 
$$
\int\limits_{-R}^{R} \frac{\cos 2x}{(x^{2}+4)^{2}} \ dx = \frac{5\pi}{32e^{4}} - Re \int\limits_{C_{R}}f(z)e^{2iz}\ dz
$$
Finally, we observe that when $z$ is a point on $C_{R}$, 
$$
|f(z)|\leq M_{R} \quad \text{where} \quad M_{R} = \frac{1}{(R^{2}-4)^{2}}
$$
and that $|e^{2iz}|=e^{-2y}\leq 1$ for such a point. Consequently, in view of the property that $|Re \ z| \leq |z|$ of complex numbers, 
$$
\tag{1}
\left| Re \int\limits_{C_{R}}f(z)e^{2iz} \ dz \right| \leq \left|\int\limits_{C_{R}} f(z)e^{2iz} \ dz \right| \leq M_{R}\pi R
$$
Since the quantity
$$
M_{R}\pi R = \frac{\pi R}{(R^{2}-4)^{2}}
$$
tends to $0$ as $R$ tends to $\infty$ and because of inequality (1), we only need to let $R$ tend to $\infty$ in our equation to arrive at the expression
$$
\text{P.V.}\int\limits_{-\infty}^{\infty}\frac{\cos 2x}{(x^{2}+4)^{2}} \ dx = \boxed{\frac{5\pi}{16e^{4}}}
$$
and because the integrand is even, then the Cauchy principle value is equivalent to the regular integral. 

## Jordan's Lemma 
In the evaluation of integrals of the type as treated before, it is sometimes necessary to use **Jordan's Lemma**, which is stated just below as a theorem

**Theorem.**  Suppose that 

(a) a function $f(z)$ is analytic at all points in the upper half plane $y\geq 0$ that are exterior to a circle $|z|=R_{0}$;
(b) $C_{R}$ denotes a semicircle $z=Re^{i \theta} \ (0\leq \theta\leq \pi)$, where $R>R_{0}$; 
(c) for all points $z$ on $C_{R}$, there is a positive constant $M_{R}$ such that 
$$
|f(z)|\leq M_{R} \quad \text{and} \quad \lim_{R\rightarrow \infty} M_{R} = 0
$$
![[Screenshot 2023-08-01 185745.png|center]]

Then, for every positive constant $a$,
$$
\lim_{R \rightarrow \infty} \int\limits_{C_{R}}f(z)e^{iaz} \ dz = 0
$$
---
**Proof:**  The proof is based on **Jordan's Inequality**, which states that 
$$
\int\limits_{0}^{\pi}e^{-R \sin \theta} \ d \theta < \frac{\pi}{R} \quad (R>0) 
$$
To verify this inequality, we first take note from the graphs of the function
$$
y= \sin \theta \quad \text{and} \quad y = \frac{2\theta}{\pi}
$$
that 
$$
\sin \theta \geq \frac{2\theta}{\pi} \quad \text{when} \quad 0\leq \theta\leq \frac{\pi}{2}
$$
Consequently, when $R>0$,
$$
e^{-R \sin \theta} \leq e^{-\frac{2R\theta}{\pi}} \quad \text{when} \quad 0\leq \theta \leq \frac{\pi}{2}
$$
and so 
$$
\int\limits_{0}^{\frac{\pi}{2}}e^{-R \sin \theta} \ d \theta \leq \int\limits_{0}^{\frac{\pi}{2}}e^{\frac{-2 R \theta}{\pi}} d \theta = \frac{\pi}{2 R}(1-e^{-R}) \quad (R>0)
$$
Hence,
$$
\int\limits_{0}^{\frac{\pi}{2}}e^{-R \sin \theta} \ d \theta \leq \frac{\pi}{2R} \quad (R>0)
$$
But this is just another form of our initial inequality since $y=\sin \theta$ is symmetric with respect to the vertical line $\theta = \frac{\pi}{2}$ on the interval $0\leq \theta\leq \pi$. 

Now, if we take this inequality and do the contour integral
$$
\int\limits_{C_{R}}f(z)e^{iaz} \ dz = \int\limits_{0}^{\pi}f(Re^{i \theta})e^{iaR e^{i \theta}}Rie^{i \theta} \ d \theta
$$
Since 
$$
|f(Re^{i \theta})| \leq M_{R} \quad \text{when} \quad |e^{iaRe^{i \theta}}| \leq e^{-aR \sin \theta}
$$
and in view of Jordan's Inequality, it follows that 
$$
\left| \int\limits_{C_{R}} f(z)e^{iaz} \ dz \right| \leq M_{R}R \int\limits_{0}^{\pi} e^{-aR \sin \theta} \ d \theta < M_{R} \frac{\pi}{a}
$$
And if we take the final limit, if $M_{R} \rightarrow 0$ as $R \rightarrow \infty$, then our integral becomes $0$. 

---
##### Example.
Let us evaluate the improper integral 
$$
\int\limits_{0}^{\infty} \frac{x \sin 2x}{x^{2}+3} \ dx
$$
As usual, the existence of the integral will be established by actually finding its value. We continue to use a closed semicircular path similar to the one before. 

![[Screenshot 2023-08-01 202758.png|center]]

We write 
$$
f(z) = \frac{z}{z^{2}+3} = \frac{z}{(z-\sqrt3i)(z+\sqrt3i)}
$$
and assume that $R>\sqrt{3}$. This ensures that the singularity $z=\sqrt3i$ is interior to the closed path. It is, moreover, a simple pole of the function
$$
f(z)e^{i2z} = \frac{\phi(z)}{z-\sqrt3i} \quad \text{where} \quad \phi(z) = \frac{z e^{2iz}}{z+\sqrt3i}
$$
since $\phi(z)$ is analytic at $z=\sqrt3i$ and 
$$
\phi(\sqrt3 i) = \frac{1}{2}e^{-2\sqrt3} \neq 0
$$
the only other singularity $z=-\sqrt3i$ is, of course, outside of the path. The residue at $z=-\sqrt3i$ is 
$$
B=\phi(\sqrt3i) = \frac{1}{2}e^{-2\sqrt3}
$$
According to the [[Cauchy Residue Theorem]], then
$$
\int\limits_{-R}^{R} \frac{xe^{i2x}}{x^{2}+3} \ dx = i \pi e^{-2\sqrt3} - \int\limits_{C_{R}}f(z)e^{i2z} \ dz,
$$
where $C_{R}$ is the closed semicircular path shown in our figure above. By equating imaginaryr parts on each side of the equation, we get 
$$
\int\limits_{-R}^{R} \frac{x\sin 2x}{x^{2}+3} \ dx = \pi e^{-2 \sqrt 3} - Im \int\limits_{C_{R}}f(z)e^{2iz} \ dz,
$$
Now the property $|Im \ z|\leq |z|$ of complex numbers tells us that 
$$
\left|Im \int_{C_{R}}f(z)e^{2iz} \ dz\right| \leq \left| \int\limits_{C_{R}}f(z)e^{2iz} \ dz\right| \leq M_{R}L
$$
from the [[Contour Integrals#Upper Bounds for Moduli of Contour Integrals|Upper bounds of Moduli Theorem]]. And we note that when $z$ is a point on $C_{R}$,
$$
|f(z)| \leq M_{R}\quad \text{where} \quad M_{R}= \frac{R}{R^{2}-3}
$$
and that $|e^{2iz}| = e^{-2y}\leq 1$ for such a point. By proceeding as we did in the previous example, we _cannot_ conclude that the right-hand side in our integral inequality tends to $0$ as $R$ tends to $\infty$. This is because the quantity
$$
M_{R}L = M_{R}\pi R = \frac{R^{2}}{R^{2}-3}
$$
which does not tend to zero for the limit of $R \rightarrow \infty$. **Jordan's Lemma**, however, does provide the limit:
$$
\lim_{R\rightarrow \infty} \int\limits_{C_{R}}f(z)e^{2iz} \ dz = 0
$$
since the limit 
$$
\lim_{R \rightarrow \infty} M_{R}=0
$$
Consequently, it follows that 
$$
\int\limits_{0}^{\infty} \frac{x \sin 2x}{x^{2}+3} \ dx = \boxed{\frac{\pi}{2} e^{-2\sqrt3}}
$$
