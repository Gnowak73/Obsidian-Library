---
tags: residue, pole, complex, Math, Cauchy, Contour, integral, integration, theorem, 
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Residues, Zeros, and Poles_
Applications: _Contour Integrals and zeros of analytic functions_
Examples: _[[MATH_450_Quiz_4.pdf]]_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Contour Integrals]],[[Laurent Series]],[[Taylor Series]],[[Application of Residues]]_
Cont.\_ of: _None_ 
_
_


The [[Cauchy Goursat Theorem]] states that if a function is [[Analytic Functions|analytic]] at all points interior to and on a simple closed contour $C$, then the value of an integral of the function around that contour is zero. If, however, the function fails to be analytic at a finite number of points interior to $C$, there is, a specific number, called a residue, which each of those points contributes to the value of the integral. 

```ad-Remember
The [[Cauchy Residue Theorem]] can be used for an infinite number of residues. They just all have to be **isolated singularities**. The quickest assumption to prevent not having isolated singularities is just stating they must be finite, but this, in fact, does not _have_ to be the case. 
```


**Important Formulations:** 
1. [[Cauchy Residue Theorem]]: Residue theorem for integral contours on multiply connected domains
2. [[Three Types of Isolated Singular Points]]: Definitions for types of isolated singularities
3. [[Residues at Poles]]: Method of finding residues at poles 
4. [[Zeros of Analytic Functions]]: Zeros of Analytic Functions, particularly how a function is identically zero or not in a neighborhood
5. [[Zeros and Poles]]: Connection between zeros of order $m$ and poles of order $m$. Extension of _Residues at Poles_ to finding residues. 
6. [[Behavior of Functions Near Isolated Singular Points]]: Behaviors of functions near isolated singular points
7. [[Application of Residues]]: Application of Residues to Real Analysis 

**Remark.**  The theorem for residues in [[Zeros and Poles]] only works for _simple poles_. Use the theorem in [[Residues at Poles]] for poles of order $m>1$.


##### Isolated Singular Points
```ad-Definition
We know from [[Analytic Functions]] that a function $f$ is analytic at a point $z_{0}$  if it has a derivative at each point in some neighborhood of $z_{0}$. If, on the other hand, $f$ fails to be analytic at $z_{0}$ but is analytic at some point in every neighborhood of it, we call $z_{0}$ a **singular point**. 

A **singular point** is said to be _isolated_ if there is a deleted $\epsilon$ neighborhood $0<|z-z_{0}|<\epsilon$ of $z_{0}$ throughout which $f$ is analytic. In other words, there is a neighborhood which doesnt contain other _singular points_. 
```

###### Example 1
The function 
$$
f(z) = \frac{z-1}{z^{5}(z^{2}+9)}
$$
has the three isolated singular points $z=0$ and $z=\pm 3i$. In fact, the singular points of a rational function, or quotient of two polynomials, are always isolated. This is because the zeroes of the polynomial in the denominator are finite in number. 

###### Example 2
The origin $z=0$ is a singular point of the principle branch 
$$
F(z) = Log \ z = \log r + i \Theta, \quad (r>0, \ -\pi<\Theta<\pi)
$$
of the logarithmic function. It is _not_, however, an **isolated singular point** since every deleted $\epsilon$ neighborhood of it contains points on the negative real axis and the branch is not even defined there. 

![[Pasted image 20230725134503.png|center]]

###### Example 3
The function 
$$
f(z) = \frac{1}{\sin  \left(\frac{\pi}{x} \right)}
$$
does not have a derivative at the origin $z=0$; and because $\sin(\frac{\pi}{z})=0$ whenever $\frac{\pi}{z}=n \pi \ (n=\pm 1, \pm 2,\ldots)$, the derivative of $f$ also fails to exist at each of the points $z=\frac{1}{n} \ (n=\pm 1, \pm 2, \ldots)$. Inasmuch as the derivative of $f$ does exist at every point that is not on the real axis, it follows that $f$ is analytic at some point in every neighborhood of each of the points
$$
z=0, \quad \text{and} \quad z=\frac{1}{n} \ (n=\pm 1, \pm 2,\ldots)
$$
Hence, each of the points is a singularity of $f$. 

The singularity $z=0$ is _not_ isolated because every deleted $\epsilon$ neighborhood of it contains other singular points. More precisely, lets use the definition of a neighborhood. The deleted neighborhood of $z=0$ is $0<|z|<\epsilon$. To check if there are any singular points, we take look at the radius of the neighborhood, which must be less than $\epsilon$ since $|z-z_{0}|=R_{1} < \epsilon$. The radius of such a neighborhood from points $z=0$ to $z=\frac{1}{m}$ is 
$$
 \left|0 - \frac{1}{m} \right| = \frac{1}{m} < \epsilon
$$
thus, lets take $m> \frac{1}{\epsilon}$, then we see that $0<\frac{1}{m}<\epsilon$. Thus, $\frac{1}{m}$ exists in the neighborhood of $0<|z|<\epsilon$.

Now, if we look at the $z=\frac{1}{m}$ singularities, we see that they **are** all isolated. We can see this by considering the fact that these are finite points and their distances are finite, unlike before where we had one finite point and then a sequence of points. 

**Remark.**  It is important to keep in mind that if a function is analytic everywhere inside a simple closed contour $C$ except for a _finite_ number of singular points, those points must all be isolated and the deleted neighborhoods about them can be made small enough to lie entirely inside of $C$.

```ad-note
Sometimes it is convenient to consider the point at infinity ([[Complex Limits#Limits Involving the Point at Infinity|Riemann Sphere]]) to be an _isolated singular point_. To be specific, if there is a positive number $R_{1}$ such that $f$ is analytic for $R_{1}<|z|<\infty$, then $f$ is said to have an _isolated singular point_ at $z_{0}=\infty$.
```

#### Residues 
When $z_{0}$ is an _isolated singular point_ of a function $f$, there is a positive number $R_{2}$ such that $f$ is analytic at each point $z$ for which $0<|z-z_{0}|<R_{2}$. Consequently, $f(z)$ has a [[Laurent Series]] representation
$$
f(z) = \sum\limits_{n=0}^{\infty}a_{n}(z-z_{0})^{n} + \sum\limits_{n=1}^{\infty} \frac{b_{n}}{(z-z_{0})^{n}}
$$
where the coefficients $a_{n}$ and $b_{n}$ have the coefficient representations 
$$
\begin{aligned}
a_{n} = \frac{1}{2 \pi i}\int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{n+1}} \quad (n=0,1,2,\ldots) \\
b_{n}= \frac{1}{2 \pi i }\int\limits_{C} \frac{f(z) \ dz}{(z-z_{0})^{-n+1}} \quad (n=1,2,\ldots)
\end{aligned}
$$
where $C$ is any positively oriented simple closed contour around $z_{0}$ that lies in the punctured disk $0<|z-z_{0}|<R_{2}$. When $n=1$, this expression for $b_{n}$ becomes 
$$
b_{1} = \frac{1}{2 \pi i}\int\limits_{C}f(z) \ dz 
$$
or
$$
\int\limits_{C} f(z) \ dz = 2 \pi i b_{1}
$$

![[Pasted image 20230725171409.png|center]]

The complex number $b_{1}$, which is the coefficient of the $\frac{1}{z-z_{0}}$ term in our Laurent Series expansion, is called the **residue**  of $f$ at the isolated singular point $z_{0}$, and we shall often write that 
$$
b_{1} = Res_{z=z_{0}} \ f(z)
$$
Our integral equation then becomes 
$$
\int\limits_{C}f(z) \ dz = 2 \pi i \ Res_{z=z_{0}} \ f(z)
$$
Sometimes we simply use $B$ to denote the residue when the function and the point $z_{0}$ are clearly indicated. 

###### Example 1 
Let us consider the integral 
$$
\int\limits_{C} \frac{dz}{z(z-2)^{5}}
$$
Where $C$ is the positively oriented circle $|z-2|=1$. Since the integrand is analytic everywhere except at the points $z=0, z=2$, it has a Laurent Series representation in the punctured disk $0<|z-2|<2$. 

![[Pasted image 20230725173448.png|center]]

Thus, we can find the residues to solve the contour integral. Since only the singularity $z=2$ is inside of the contour, that is the center of our punctured disk which we create the Laurent Series and find the residue about. Thus, let us take
$$
\frac{1}{z(z-2)^{5}} = \frac{1}{(z-2)^{5}} \cdot  \frac{1}{2+(z-2)} = \frac{1}{2(z-2)^{5}} \cdot \frac{1}{1-(- \frac{z-2}{2})}, 
$$
Which we can check to see that 
$$
 \left|- \frac{z-2}{2}  \right| = \frac{|z-2|}{2} < 1 \quad \text{when} \quad 0<|z-2|<2
$$
and then use the geometric series:
$$
\frac{1}{z(2-z)^{5}} = \frac{1}{2(z-2)^{5}} \sum\limits_{n=0}^{\infty} \left(- \frac{z-2}{2}\right)^{n} = \sum\limits _{n=0}^{\infty} \frac{(-1)^{n}}{2^{n+1}}(z-2)^{n-5} \quad (0<|z-2|<2)
$$
Now, for the $\frac{1}{z-2}$ term we need $n=4$, plugging this in we get $B=\frac{1}{2^{5}}=\frac{1}{32}$. Now, we know the contour integral is equal to
$$
2 \pi i B = \boxed{\frac{\pi i}{16}}
$$




