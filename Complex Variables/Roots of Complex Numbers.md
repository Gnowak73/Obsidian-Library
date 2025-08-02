---
tags: Math, Complex_Analysis, roots, technique, theorem 
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Roots of Complex Numbers_
Applications: _Finding Roots and rotations in the complex plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Complex Elementary Functions]]_
Cont.\_ of: _None_ 
_
_
If we consider two points of the form $z=re^{i\theta}$ such that 
$$
z_{1}=r_{1}e^{i\theta_{1}}=z_{2}=r_{2}e^{i\theta_{2}}
$$
then these two numbers are equal if and only if $r_{1}=r_{2}$ and $\theta_{1}=\theta_{2}+2\pi n$.

What if we now consider the power of a root 
$$
z^{n} = r^{n}e^{i\theta n}
$$
If we combine these two principles together, what if we have a number 
$$
r_{0} =r_{0}e^{i\theta}
$$
such that
$$
(r_{0})^{\frac{1}{n}}=(r_{0})^{\frac{1}{n}}e^{\frac{i(\theta+2\pi k)}{n}}
$$
Now,
$$
\sqrt[n]{r_{0}} = \sqrt[n]{r_{0}} \ e^{i\left(\frac{\theta}{n}+\frac{2\pi k}{n} \right)} 
$$
Where $k$ is any integer. So, we see that we have the angles 
$$
\theta = \frac{\theta_{0}}{n}+ \frac{2\pi k}{n}
$$
with the complex numbers
$$
z=\sqrt[n]{r_{0}} \ e^{i\left(\frac{\theta_{0}}{n}+\frac{2\pi k}{n}\right)}
$$
which represent the $nth$ roots of $z_{0}$. We see from this exponential form that all of the roots lie on the circle $|z|=\sqrt[n]{r_{0}}$ about the origin and are equally spaced every $\frac{2\pi}{n}$ radians. Thus, all unique roots are obtained for $k=0,1,2,\ldots n-1$. 

**Remark.** These roots represent a polygon inscribed in a circle. Also realize that if we know one root, all other roots can be found by applying a rotational transformation of $e^{i\frac{2\pi k}{n}}$; most of the time this symmetry allows us to find the roots by changing signs of the real and imaginary parts without doing any real computation. 
```ad-tip
For even roots, the conjugate of any root is another corresponding root. Meaning we only realy need to find half of the roots and then just take the conjugate of each for the other half.
```

```ad-Definition
The Principle Root is the root corresponding to the value of $\theta_{0}$ corresponding to the principle value of $arg \ z_{0}$ ($-\pi <\theta_{0}\leq\pi$) 
```

```ad-Remember
From [[Complex Elementary Functions]], remember that all roots will be _multi-valued_ functions, thus, a branch cut will be needed when working with them. 
```
