---
tags: Math, complex, functions, elementary_functions, complex_plane, exponential, logarith, branch, branch_cut
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Elementary Functions_
Applications: _Functional analysis on Complex Plane_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
##### The Exponential Function
The exponential function can be defined by writing
$$
e^{z}=e^{x}e^{iy}
$$
where **Euler's Formula** is 
$$
e^{iy}=\cos y + i\sin y
$$
used and $y$ is to be taken in radians. For an equation of two exponentials being equal, we must remember the $2\pi n$ with the angle since the periodicity of $\sin$ and $\cos$. For example 
$$
\begin{gathered}
e^{z}=1+\sqrt{3}i \\
e^{x}e^{iy}=2e^{i\left(\frac{\pi}{3}+2\pi n\right)} \\
e^{x}=2, \quad e^{iy}=e^{i\left(\frac{\pi}{3}+2\pi n\right)}\\
x=\ln(2), \quad y=\frac{\pi}{3}+2\pi n, \quad (n=0,\pm 1,\pm 2,\ldots)

\end{gathered}
$$
---
##### The Logarithmic Function
The logarithmic function is based on solving 
$$
e^{w}=z
$$
for $w$, where $z$ is any _nonzero_ complex number. To do this, we note that when $z$ and $w$ are written $z=re^{i\theta} \ (-\pi<\Theta\leq \pi)$ and $w=u+iv$, this equation becomes
$$
e^{u}e^{iv}=re^{i\Theta}.
$$
We can thus solve this to get 
$$
e^{u}=r, \quad v=\Theta+2\pi n
$$
where $n$ is any integer. Since $e^{u}=r$ can just be written as $u=\ln(r)$, it follows that we must have the condition 
$$
w=\ln r + i(\Theta+2\pi n) \quad (n=0,\pm1,\pm2,\ldots)
$$
Thus, we can write that 
$$
\log z=\ln r+i(\Theta+2\pi n)
$$
The _Principle Value_ of $\log z$ is the value obtained from this equation when $n=0$ and is denoted by $Log \ z$, or 
$$
Log \ z = \ln r +i\Theta
$$
---
##### Branches and Derivatives of Logarithms 
If $z=re^{i\theta}$ is a nonzero complex number, the argument $\theta$ has any one of the values $\theta=\Theta+2\pi n \ (n=0,\pm 1,\ldots)$ where $\Theta=Arg \ z$. Hence the definition 
$$
\log z = \ln r + i(\Theta+2\pi n) 
$$
of the multiple-valued logarithmic function can we written as 
$$
\log z = \ln r +i\theta
$$
Because it is multiple-valued, we cannot do much with it. To get around this, we restrict the function to be single-valued on specific domains. We call these **Branches**, and we call the part of the domain we "cut up" to separate the function into single-valued parts is called the **Branch Cut**. So... how can we define the logarithm to be spliced up into single-valued sections? 

If we let $\alpha$ denote any real number and restrict the value of $\theta$ such that $\alpha<\theta<\alpha+2\pi$ (one full rotation about the unit circle), the logarithmic function will be single-valued and continuous! We do not have the domain $\alpha\leq \theta\leq \alpha+2\pi$ because that would make us have the ray $\alpha=\theta$ be multivalued and result in a noncontinuous function. We could also include either the $\alpha$ or the $\alpha+2\pi$ into the set since that would keep it single-valued.

![[Pasted image 20230704235531.png|center]]

With our branch cuts, we not only have a continuous function but also an analytic one throughout the domain $r>0, \ \alpha<\theta<\alpha+2\pi$ since the first-order partial derivatives of $u$ and $v$ are continuous and satisfy the [[Complex Derivatives#Cauchy Riemann Equations|polar Cauchy-Riemann Equations]]. We define the **Principle Branch** (analog to the *Principle Value*), to be the branch on the domain $(-\pi<\theta<\pi)$. 

```ad-Remember
We include the origin as part of the branch cut because it would result in $\ln 0$ which is not defined! So it cannot be used either in the domain of our function! It is also known as a _branch point_.
```

**Remark.**  The definition for these _branch cuts_, _principle branch_, and the _principle value_ are all arbitrary and simply a matter of convention for the most part. It is also worth noting that the complex logarithm follows all of the same algebraic rules and properties of the regular real logarithm. 


###### The Power Function
We can write the power function in terms of the logarithm
$$
z^{c}=e^{c\log z}
$$
Because of the logarithm, $z^{c}$, in general, is multi-valued. Thus, when we work with the power function, we must define a branch cut that we are working with. 

**Remark.**  The multivalued of $z^{c}$ only shows when working with exponents that are not integers and real numbers. This is because for real integers, the definition of the power function is multiplying $z$ a $c$ number of times. But the other definitions with complex numbers and fractions directly defined by using the logarithm. 

A better way of thinking about this is that the exponential $z^{c}=e^{c \log z} = e^{c \ln |z| + c i (Arg \ z + 2\pi n)}$. If $c$ is an integer, then we are rotating about the unit circle an integer multiple of $2 \pi$ times, which would give us the same number every time. If we weren't rotating by a multiple of $2\pi$, or when $c \in \mathbb{C}$, then we would be rotating about the unit circle such that we wouldn't not perfectly rotate back around to our original number since it's not a perfect integer $2\pi$ rotation, giving us multiple values. For example, say we have $z^{\frac{1}{4}} = e^{\frac{1}{4}\ln |z| +i\left(\theta + \frac{\pi n}{2}\right)}$. We are rotating the unit circle by $\frac{\pi}{2}$ every time, so it will take 3 additional rotations before we get back our original number. Thus, there would be 4 numbers/values associated for each $z$. 

```ad-note
We consider the _principle value_ of $z^{c}$ when $\log z$ is replaced by the **Principle Log** $Log \ z$:
$$
\text{P.V.} \ z^{c} = e^{c Log \ z}
$$
This also serves to define the _principle branch_ of the function $z^{c}$ on the domain $|z|>0, \ -\pi< Arg \ z < \pi$.
```

---
##### The Sin and Cos Trigonometric Functions 
Using Euler's Formula, 
$$
e^{i\theta} = \cos \theta+i\sin\theta
$$
we can write 
$$
\boxed{\frac{e^{ix}-e^{-ix}}{2i}=\sin x, \quad \frac{e^{ix}+e^{-ix}}{2}=\cos x}
$$
It is, therefore, natural to define the **sin** and **cos** functions of a complex variable $z$ as:
$$
\sin z= \frac{e^{iz}-e^{-iz}}{2i}, \quad \cos z = \frac{e^{iz}+e^{-iz}}{2}
$$
which is similar to how we defined our Real and Imaginary parts of a complex number. Since we know the derivatives of $e^{iz}$, we can easily see that 
$$
\frac{d}{dz}\sin z = \cos z, \quad \frac{d}{dz}\cos z = -\sin z
$$
We can also see how a variety of trigonometric identities carry over to the complex numbers such as 
$$
\sin^{2}z+\cos^{2}z = 1
$$
---
##### The other Trig Functions
The other trig functions follow the same trigonometric properties and rules as before. The derivatives are also the same:
$$
\frac{d}{dz}\tan z = \sec^{2}z, \quad \frac{d}{dz}\cot z = -\csc^{2}z
$$
$$
\frac{d}{dz}\sec z = \sec z\tan z, \quad \frac{d}{dz}\csc z = -\csc z \cot z
$$

---
##### The Hyperbolic Functions
We define the hyperbolic functions as 
$$
\boxed{\sinh y = \frac{e^{y}-e^{-y}}{2}, \quad \cosh y = \frac{e^{y}+e^{-y}}{2}}
$$
such that we can write 
```ad-Remember
$$
\sin(iy) =i\sinh y, \quad \text{and} \quad \cos(iy) = \cosh y
$$
```
Also, the real and imaginary components of $\sin z$ and $\cos z$ can be displayed in terms of those hyperbolic functions:
$$
\sin z = \sin(x+iy) = \sin(x)\cos(iy)+\sin(iy)\cos(x) = \sin(x)\cosh(y)+i\cos(x)\sinh(y)
$$
$$
\cos z = \cos(x+iy) = \cos(x)\cos(iy)-\sin(x)\sin(iy) = \cos(x)\cosh(y)-i\sin(x)\sinh(y)
$$

Using these equations, we can derive that 
$$
\begin{gathered}
|\sin z|^{2} = |\sin(x)\cosh(y)+i\cos(x)\sinh(y)|^{2}= \sin^{2}(x)\cosh^{2}(y)+\cos^{2}(x)\sinh^{2}(y) \\
=\sin^{2}(x)\cosh^{2}(y) +(1-\sin^{2}(x))\sinh^{2}(y) \\
= \sin^{2}(x)\cosh^{2}(y) + \sinh^{2}(y)-\sin^{2}(x)\sinh^{2}(y) 
\\ = \sin^{2}(x) (\cosh^{2}(y)+\sinh^{2}(y))+\sinh^{2}(y)
\\ = \sin^{2}(x)+\sinh^{2}(y)

\end{gathered}
$$
So,
$$
|\sin z|^{2}=\sin^{2}(x)+\sinh^{2}(y) 
$$
This method can also be used to show that 
$$
|\cos z|^{2}=\cos^{2}(x)+\sinh^{2}(y)
$$

**Remark.**  The $\cosh$ and $\sinh$ functions follow the same trigonometric identities as $\sin$ and $\cos$, the only difference shows up with the derivatives.

The derivatives of the hyperbolic functions are as follows:
$$
\frac{d}{dz}\tanh z= sech^{2}z, \quad \frac{d}{dz}sech \ z = -\tanh z \ sech \ z
$$
$$
\frac{d}{dz}\coth z = -csch^{2}z, \quad \frac{d}{dz}csch \ z = -\coth z \ csch \ z
$$
---
##### Inverse Trigonometric and Hyperbolic Functions
Inverses of the trigonometric and hyperbolic functions can be described in terms of logarithms. 

In order to define the inverse $\sin^{-1} z$ function, we write
$$
w=\sin^{-1}z \quad \text{when} \quad z=\sin w
$$
That is, $w=\sin^{-1}z$ when 
$$
z=\frac{e^{iw}-e^{-iw}}{2i}
$$
If we put this equation in the form 
$$
(e^{iw})^{2}-2iz(e^{iw})-1=0
$$
which is quadratic in $e^{iw}$, we get 
$$
e^{iw}=iz+(1-z^{2})^\frac{1}{2}
$$
Taking logarithms on both sides and using $w=\sin^{-1}z$ we get 
$$
\boxed{\sin^{-1}z = -i\log[iz+(1-z^{2})^\frac{1}{2}]}
$$
Since $(1-z^{2})^\frac{1}{2}$ is a multiple-valued function AND we are working with logarithms, so is $\sin^{-1}z$, with infinitely many values at each point $z$. 

We can apply the technique used to derive $\sin^{-1}z$ to also get $\cos^{-1}z$ as 
$$
\boxed{\cos^{-1}z = -i\log[z+i(1-z^{2})^\frac{1}{2}]}
$$
and that 
$$
\boxed{\tan^{-1}z = \frac{i}{2}\log\left(\frac{i+z}{i-z}\right)}
$$

**Remark.**  The functions $\cos^{-1}z$, $\tan^{-1}z$, and $\sin^{-1}z$ are all multiple-valued. When specific branched of the square root and logarithmic functions are used, all three inverse functions become single-valued and analytic because they are then compositions of analytic functions. 

The derivatives of these expressions can be easily obtained from the derivative of the logarithm to get
$$
\frac{d}{dz}\sin^{-1}z = \frac{1}{(1-z^{2})^{\frac{1}{2}}}
$$
$$
\frac{d}{dz}\cos^{-1}z = \frac{-1}{(1-z^{2})^{\frac{1}{2}}} 
$$
$$
\frac{d}{dz}\tan^{-1}z = \frac{1}{1+z^{2}}
$$
**Remark.**  The derivative of the $\tan^{-1} z$ does not depend on the manner in which the function is made single-valued. 

Inverse hyperbolic functions are all treated in the same corresponding manner. It turns out that 

$$
\sinh^{-1}z = \log[z+(z^{2}+1)^\frac{1}{2}]
$$
$$
\cosh^{-1}z = \log[z+(z^{2}-1)^\frac{1}{2}]
$$
$$
\tanh^{-1}z=\frac{1}{2}\log\left[\frac{1+z}{1-z}\right]
$$
The derivatives and properties can be easily derived as before.
