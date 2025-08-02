---
tags: Math, Contour, complex, integral, method, derivation, sine, cosine, definite, definite_integral
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Definite Integrals Involving Sines and Cosines_
Applications: _Finding definite integrals with sines and cosines_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

The method of Residues is also useful in evaluating certain definite integrals of the type 
$$
\int\limits_{0}^{2 \pi} f(\sin \theta, \cos \theta) \ d \theta
$$
The fact that $\theta$ varies from $0$ to $2 \pi$ leads us to consider $\theta$ as an argument of a point $z$ on a positively oriented circle $C$ centered at the origin. Taking the radius to be unity, we use the parametric representation
$$
z=e^{i \theta} \quad (0 \leq \theta \leq 2 \pi)
$$
to describe $C$. 

![[Screenshot 2023-08-06 163156.png|center]]

We then refer to the differentiation formula to write 
$$
\frac{ dz}{d \theta} = ie^{i \theta} = iz
$$
and recall that 
$$
\sin \theta = \frac{z-z^{-1}}{2i}, \quad \cos \theta = \frac{z+z^{-1}}{2}, \quad d \theta = \frac{dz}{iz}
$$
which transforms our integral into the contour integral 
$$
\int\limits_{C} F\left(\frac{z-z^{-1}}{2i},\frac{z+z^{-1}}{2}\right) \frac{dz}{iz}
$$
of a function $z$ around the circle $C$. When the integrand in this form reduces the function to a rational function of $z$, we can evaluate that integral by means of [[Cauchy Residue Theorem]] once the zeros in the denominator have been located and provided that none lie on $C$. 

##### Example 1. 
Let us show that 
$$
\int\limits_{0}^{2 \pi} \frac{d \theta}{1+a \sin \theta} = 2 \frac{\pi}{\sqrt{1-a^{2}}} \quad (-1<a<1)
$$
This integration formula is clearly valid if $a=0$ so we exclude that in our derivation. With our substitution suggested before, the integral takes the form
$$
\int\limits_{C} \frac{\frac{2}{a}}{z^{2}+z\frac{2i}{a}-1} \ dz
$$
where $C$ is the positively oriented circle $|z|=1$. The quadratic formula reveals that the denominator of the integrand here has the pure imaginary zeros
$$
z_{1} = \left(\frac{-1 +\sqrt{1-a^{2}}}{a}\right)i, \quad z_{2} = \left(\frac{-1-\sqrt{1-a^{2}}}{a}\right)i
$$So if $f(z)$ denotes the integrand in the integral, then 
$$
f(z) = \frac{\frac{2}{a}}{(z-z_{1})(z-z_{2})}
$$
Note that because $|a|<1$,
$$
|z_{2}| = \frac{1+1\sqrt{1-a^{2}}}{|a|} > 1
$$
Also, since $|z_{1}z_{2}|=1$, it follows that $|z_{1}|<1$. Hence, there are no singular points on $C$, and the only one interior to it is the point $z_{1}$. The corresponding residue $B$ is found by writing 
$$
f(z) = \frac{ \phi(z)}{z-z_{1}} \quad \text{where} \quad \phi(z) = \frac{\frac{2}{a}}{z-z_{2}}
$$
This shows that $z_{1}$ is a simple pole and that 
$$
B = \phi(z_{1}) = \frac{\frac{2}{a}}{z_{1}-z_{2}}  = \frac{1}{i\sqrt{1-a^{2}}}
$$
Consequently, 
$$
\int\limits_{C} \frac{\frac{2}{a}}{z^{2}+(\frac{2i}{a})z-1}\ dz = 2 \pi i B_{1} = \frac{2 \pi}{\sqrt{1-a^{2}}}
$$
and our integration formula follows.

##### Example 2.
Let us show that 
$$
\int\limits_{0}^{\pi} \frac{\cos 2 \theta}{1-2 a \cos \theta + a^{2}} \ d \theta = \frac{a^{2} \pi}{1-a^{2}} \quad (-1<a<1)
$$
Just as we did in Example 1. We exclude the possibility that $a=0$. We begin with the observation that the integrand is symmetric about $\theta= \pi$ from the fact that 
$$
\cos (2\pi-\theta)= \cos \theta, \quad \text{and} \quad \cos 2(2 \pi - \theta) = \cos 2 \theta
$$
This observation enabled us to write 
$$
\int\limits_{0}^{\pi}\frac{\cos 2 \theta}{1-2a \cos \theta + a^{2}} \ d \theta = \frac{1}{2}\int\limits_{0}^{2 \pi} \frac{\cos 2 \theta}{1-2 a \cos \theta = a^{2}} \ d \theta = \frac{i}{4} \int\limits_{C} \frac{z^{4}+1}{(z-a)(az-1)z^{2}} \ dz
$$
where $C$ is the positively oriented circle of unity. Evidently, then 
$$
\int\limits_{0}^{\pi} f(z) \ dz= \frac{i}{4} 2 \pi i (B_{1}+B_{2})
$$
where $B_{1}$ and $B_{2}$ are the residues of the function
$$
f(z) = \frac{z^4+1}{(z-a)(az-1)z^{2}}
$$
at $a$ and $0$, respectively. The singularity $z=\frac{1}{a}$ is, of course, exterior to the circle $C$ since $|a|<1$. Inasmuch as 
$$
f(z) = \frac{\phi(z)}{z-a}\quad \text{where} \quad \phi(z) = \frac{z^{4}+1}{(az-1)z^{2}},
$$
it is easy to see that 
$$
B_{1} = \phi(a) = \frac{a^{4}+1}{(a^{2}-1)a^{2}}
$$
The residue $B_{2}$ can be found by writing 
$$
f(z) = \frac{\phi(z)}{z^{2}} \quad \text{where} \quad \phi(z) = \frac{z^{4}+1}{(z-a)(az-1)}
$$
and straightforward differentiation reveals that 
$$
B_{2} = \phi'(0) = \frac{a^{2}+1}{a^{2}}
$$
Finally, plugging these residues into our integral equation we get our initial result.  