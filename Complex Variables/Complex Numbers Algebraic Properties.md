---
tags: Math, Complex_Analysis
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Number Properties_
Applications: _Complex Plane, QM_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: [[Complex Variables Textbook.pdf]]
Closely\_Related\_To: _None_
_
_
Complex Numbers have a real and imaginary part. They are of the form 
$$
z=a+bi
$$
They are very similar to vectors, and add in a similar fashion. Complex numbers can also be put into an ordered pair, where the first number is the real part and the second number is the imaginary part. One massive difference though, is their ability to be multiplied. Their multiplication is of the form
$$
z_{1}z_{2}=(x_{1},y_{1})(x_{2},y_{2}) = (x_{1}x_{2}-y_{1}y_{2}, \ x_{1}y_{2}+x_{2}y_{1})
$$
Complex numbers follow every other traditional real number property. 

###### Modulus
The modulus, or $|z|$, is the length between the origin and the complex number. In a sense, because complex numbers can almost be treated like vectors, this is our dot product. We have
$$
|z|^{2}=z\overline{z} = a^{2}+b^{2}
$$
where $\overline{z}$ is the [[#Complex Conjugates|complex conjugate]] of $z$. Because of this property, we can define the distance between two points on the complex plane as 
$$
|z_{1}-z_{2}|=\sqrt{(x_{1}-x_{2})^{2}+(y_{1}-y_{2})^{2}}
$$
or the distance formula we are used to seeing in <mark style="background: #FFB8EBA6;">Euclidean Geometry</mark>! 

We can also see that 
$$
|z|^{2}=(Re \ z)^{2}+ (Im \ z)^{2}
$$
Thus,
$$
Re \ z \leq |Re \ z| \leq|z|, \quad Im \ z\leq|Im \ z| \leq |z|
$$

###### Inverse
The inverse of a complex number is $\frac{1}{z}$, simply enough. We can simplify this though by multiplying the top and bottom of the fraction by $\overline{z}$ to get 
$$
z^{-1} = \frac{1}{z}=\frac{z}{|z|} = \frac{(x,y)}{x^{2}+y^{2}}
$$

###### Triangle Inequality
The same statement as [[Triangle Inequality (Euclidean Geometry)]] except just extended to the Complex Plane:
$$
\boxed{|z_{1}+z_{2}|\leq |z_{1}|+|z_{2}|}
$$

We can actually rewrite this by using 
$$
|z_{1}| = |(z_{1}+z_{2})+(-z_{2})| \leq |z_{1}+z_{2}|+|z_{2}| 
$$
from this we get
$$
|z_{1}|-|z_{2}| \leq |z_{1}+z_{2}|
$$
If we were to switch the place of $z_{1}$ and $z_{2}$, we can see that this only holds when $|z_{1}|\geq |z_{2}|$. This is because 
$$
|z_{1}+z_{2}|\geq 0,
$$
so
$$
|z_{1}+z_{2}|\geq|z_{1}|-|z_{2}|\geq 0.
$$
If we were to switch $z_{1}$ and $z_{2}$ we have 
$$
|z_{1}+z_{2}|\geq -(|z_{1}|-|z_{2}|)
$$
we can combine these two statements to arrive at the <mark style="background: #BBFABBA6;">Inverse Triangle Inequality</mark>:
$$
\boxed{|z_{1}+z_{2}|\geq ||z_{1}|-|z_{2}|| }
$$

These inequalities can be generalized by means of mathematical induction to include as many summations of complex numbers as you may need. 

---

#### Complex Conjugates
Complex conjugates is when we change the sign of the imaginary term of a complex number. For example, $\overline{z} = (z,-y) = x-iy$. The complex conjugate is an operation that can be spread based on multiplication or addition:
1. $\overline{z_1 +z_{2}}= \overline{z_{1} }+\overline{z_{2}}$
2. $\overline{z_{1}z_{2}} = \overline{z_{1}} \ \overline{z_{2}}$ 

We can actually write the real and imaginary parts of a complex number by their complex conjugates:
$$
Re \ z = \frac{z+\overline{z}}{2}, \quad Im \ z = \frac{z-\overline{z}}{2}
$$
---

#### Exponential Form
All complex numbers have the property of being able to be put into polar coordinates due to the vector-like behavior of complex numbers. 
$$
z = re^{i\theta} = |z|e^{i\theta}  
$$
Each value of $\theta$ is called the argument of $z$, this set of arguments is known as $arg \ z$. The <mark style="background: #FFB86CA6;">Principle Value</mark> of $arg \ z$, denoted by $Arg \ z$, is the unique value $\Theta$ such that $-\pi<\Theta\leq \pi$ such that 
$$
arg \ z = Arg \ z +2\pi n, \quad (n=0,\pm 1, \pm 2,\ldots )
$$
Also, we consider negative real numbers to have an $Arg$ of $\pi$ and not $-\pi$ by counter-clockwise polar standards. 

With this, we can actually write the equation of circles as 
$$
z=z_{0}+Re^{i\theta}
$$
---

#### Lagrange's Trigonometric Identity 
If we let $S=1+z+z^2+...+z^n$,
$$
\begin{align}
    S\left(1-z\right)=\left(1+z+z^2+...+z^n\right)+\left(-z-z^2-z^3-...-z^{n+1}\right)=1-z^{n+1}
\end{align}
$$
$$
\begin{align}
    S=\frac{1-z^{n+1}}{1-z}
\end{align}
$$
Thus,
$$
\begin{align}
    1+z+z^2+...+z^n=\frac{1-z^{n+1}}{1-z}
\end{align}
$$
If we substitute $z=e^{i\theta}$
$$
\begin{align}
    \frac{1-z^{n+1}}{1-z}=\frac{1-e^{i\left(n+1\right)}}{1-e^{i\theta}}=\frac{e^{i\left(n+1\right)\theta/2}\left(e^{-i\left(n+1\right)\theta/2}-e^{i\left(n+1\right)\theta/2}\right)}{e^{i\theta/2}\left(e^{-i\theta/2}-e^{i\theta/2}\right)}
\end{align}
$$
$$
\begin{align}
    =\frac{e^{i\left(n+1\right)\theta/2}}{e^{i\theta/2}} \ \frac{2i\sin\frac{\left(n+1\right)\theta}{2}} {2i\sin\left(\theta/2\right)}
\end{align}
$$
$$
\begin{align}
    =e^{in\theta/2} \frac{\sin\left(\frac{\theta\left(n+1\right)}{2}\right)}{\sin\left(\theta/2\right)}
\end{align}
$$
And 
$$
\begin{align}
    1+z+z^2+...+z^n=1+\cos\left(\theta\right)+i\sin\left(\theta\right)+\cos\left(2\theta\right)+i\sin\left(2\theta\right)+...+\cos\left(n\theta\right)+i\sin\left(n\theta\right)
\end{align}
$$
Looking at only the real parts of these equations
$$
\begin{align}
    1+\cos\left(\theta\right)+\cos\left(2\theta\right)+...+\cos\left(n\theta\right)=\frac{\sin\left(\frac{\theta\left(n+1\right)}{2}\right)}{\sin\left(\theta/2\right)} \cos\left(\frac{n\theta}{2}\right)
\end{align}
$$
The right hand side is equal to
$$
\begin{align}
    \frac{\sin\left(\frac{\theta\left(n+1\right)}{2}\right)}{2\sin\left(\theta/2\right)} 2\cos\left(\frac{n\theta}{2}\right) = \frac{\sin\left(\frac{\theta\left(n+1\right)}{2}\right)}{2\sin\left(\theta/2\right)} \ \left(\sin\left(\frac{\left(2n+1\right)\theta}{2}\right)+\sin\left(\theta/2\right)\right)
\end{align}
$$
$$
\begin{align}
    =\frac{1}{2}+\frac{(\sin\left(\frac{\left(2n+1\right)\theta}{2}\right)}{2\sin\left(\frac{\theta}{2}\right)}

\end{align}
$$
Thus, we have 
$$
\begin{align}
    \boxed{1+\cos\left(\theta\right)+\cos\left(2\theta\right)+...+\cos\left(n\theta\right)=\frac{1}{2}+\frac{(\sin\left(\frac{\left(2n+1\right)\theta}{2}\right)}{2\sin\left(\frac{\theta}{2}\right)}}
\end{align}
$$

