---
tags: complex, Math, contour, integral, line_integral, contour_integral, theorems, equations, examples, Complex, Complex_Analysis, parametrization, antiderivative, branch, branch_cut
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _The Evaluation of Contour Integrals_
Applications: _Contour Integration on the Complex Plane_
Examples: _[[MATH_450_Quiz_3.pdf]]_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Complex Derivatives]],[[Analytic Functions]],[[Complex Contours]],[[Complex Definite Integrals]],[[Application of Residues]]_
Cont.\_ of: _None_ 
_
_ 
```ad-note
From the notes prescribed below, it is worth noting the major differences and strengths of parametrization and antiderivatives. 

**Parametrization**: The strength of this method comes from the fact that the contour integral exists as long as their is _piecewise continuity_. Because of this, we can work this intervals where a function may not be defined (like branch cuts) fairly easy. This method is also easier when we don't know the antiderivative.

**Antiderivative**: The strength of this method comes from knowing antiderivatives from regular Calculus. On top of that, if a function is analytic in an entire domain, only the endpoints make a difference, allowing us to easily calculate contour integrals. The downside is when working with branches or domains where the function is not completely analytic in, we **MUST** choose _domains which the antiderivative is analytic on_, making branch cuts more cumbersome since the inetgral needs to be separated into multiple ones.

We also note that the _Upper Bound Moduli Theorem_ can be used to approximate contour integration or give an upper bound. 
```

**Remark.**  Using the anti-derivative method is assuming a function is analytic in a domain. If we wanted to create or show a proof for any path or a specific path without this assumption, parametrization is the better option. 

```ad-warning
The proofs shown in the [[#Parametrization]] section mistakenly use the analytic method, do remember that this **Only** works for functions analytic in a domain which the contour lies entirely within!
```



**Important Formulations:**  Because of the breadth of this section, we place the contour integral theorems here for easy access
1. [[Cauchy Goursat Theorem]] - Conditions: analytic function at all points interior and on a simple closed contour. 
2. [[Contour Integral Domains]] - Extensions of the Cauchy-Goursat Theorem for simply connected and multiple connected domains. Extension into _deformation of paths_. 
3. [[Cauchy Integral Formula]] - An **Important** integral formula relating the value of an analytic function within a simple closed contour to a contour integral involving that function. (used to deal with singularities and work with complex scenarios easily) 
4. [[Residues, Zeros, and Poles]] - Important ways to solve contour integrals using [[Laurent Series]] and [[Taylor Series]], including [[Cauchy Residue Theorem]].  
5. [[Application of Residues]] - Application of Contour Integrals and Residues to Real Analysis 



---
Expanding from [[Complex Contours]], we now turn to integrals of complex-valued functions $f$ of the complex variable $z$, extending from a point $z=z_{1}$ to $z=z_{2}$ in the complex plane. It is therefore, a [[Line Integrals|line integral]]. It is written as 
$$
\int\limits_{C}f(z)\ dz
$$
**Remark.**  Unlike working with real dimensions in Calculus, these integrals have no corresponding helpful interpretation, geometric or physics, except in special cases. Complex Integrals usually appear as simply a mathematical tool in order to evaluate things that are easier to do in the Complex Plane than in the Real Space.

Because we can separate a complex valued function into real and imaginary parts, we can separate an integral into 
$$
\int\limits w(t) \ dt = \int\limits u(t) \ dt + i\int v(t) \ dt  
$$
In other words,
$$
Re \left[\int\limits w(t) \ dt\right] = Re\left[\int\limits u(t) \ dt + i\int v(t) \ dt\right] = \int\limits u(t) \ dt = \int\limits Re[w(t)] \ dt
$$
This same property works for the imaginary part too. Thus,
$$
Re\left[\int\limits w(t) \ dt\right] = \int\limits Re[w(t)] \ dt
$$
and
$$
Im\left[\int\limits w(t) \ dt\right] = \int\limits Im[w(t)] \ dt
$$

---
### Parametrization 
If we can parametrize the [[Complex Contours|complex contour]] $C$ by a parameter $t$ such that we can represent $C$ by $z(t)$, then we can use the chain rule to write 
$$
\int\limits_{C}f(z) \ dz = \int\limits_{a}^{b}f[z(t)] \ dz(t) = \int\limits_{a}^{b}f[z(t)] \ \frac{dz(t)}{dt}dt = \int\limits_{a}^{b}f[z(t)] z'(t) \ dt
$$
**Remark.**  changing $t\rightarrow -t$ changes the direction of the contour such that 
$$
\int\limits_{-C}f(z) \ dz =\int\limits_{-b}^{-a}f[ z(-t)] \frac{dz(-t)}{dt} \ dt  =-\int\limits_{-b}^{-a}f[z(-t)]z'(-t) \ dt 
$$
```ad-warning
Dont get messed up on the notation. 
$$
\frac{dz(-t)}{dt}
$$
is **NOT** equal to $z'(-t)$. $z'(-t)$ represents taking the derivative of $z(-t)$ w.r.t $(-t)$ (the same thing as taking the derivative of $z(t)$ w.r.t  $(t)$ and then substituting $t \rightarrow -t$ at the end).
$$
\frac{dz(t)}{dt} \neq \frac{dz(-t)}{dt}, \quad \frac{dz(-t)}{dt} = \frac{dz(-t)}{d(-t)} \times \frac{d(-t)}{dt} = -z'(-t)
$$
```
If we make the substituting $-t\rightarrow \tau$, then we would get 
$$
\int\limits_{-C}f(z) \ dz = -\int\limits_{a}^{b}f[z(\tau)]z'(\tau) \ d \tau
$$
Which is just the same as saying 
$$
\boxed{ \int\limits_{-C}f(z) \ dz = -\int\limits_{C}f(z) \ dz}
$$
```ad-note
Another thing work noting is that for scalar [[Line Integrals]], the path direction does not matter. For contour integrals, the path direction **DOES MATTTER** in the same way it does for vector [[Line Integrals]] (one direction is negative integral of opposite direction). Weird right?
```

```ad-tip
Remember! Since we have 
$$
\int\limits_{C}f(z(t)) \ dz(t)
$$
we can evaluate the integral first with $z$ with the bounds created from $z(t)$. We don't have to plug $z(t)$ directly into the integral every time. For example, if we have $C$ as $z=e^{i \theta}$ from $[0,2 \pi]$, we can solve it as 
$$
\int\limits_{C} \frac{dz}{z} = \ln|z| \  \rvert_{0}^{2 \pi} = \pi i
$$
instead of plugging in $z=e^{i \theta}$.

This is the [[#Antiderivatives]] method, so we are assuming thta this function is analytic in the domain which the contour entirely lies within. Luckily, that is the case for this specific problem (may not be for all problems though). We also must remember that to ensure we have a possible integral, that our Integral's result is analytic on the Contour we are working with. If it isn't, then there isn't a derivative such that the integral exists. 
```

##### Important Example, Contour of z
If we have the contour integral with some parametrization of $t$ such that the endpoints are $z_{0}$ and $z_{1}$:
$$
\int\limits_{z_{0}}^{z_{1}} z \ dz = \left.\frac{z^{2}}{2}\right\rvert_{z_{0}}^{z_{1}}
$$
In other words, only the endpoints matter. We can actually see this is because for any parametrization with $t$, $z \ dz = z(t)z'(t)\ dt$ which is $\frac{d}{dt}\frac{{z^{2}(t)}}{{2}}$. Thus for any contour, we would have the same result since we would have the integral of this derivative. It works in the same manor as [[Fundamental Theorem of Line Integrals]] and for the [[Complex Definite Integrals#Fundamental Theorem of Calculus on Complex Plane|Fundamental Theorem of Calculus on the Complex Plane]], but instead of a potential function we have a derivative. This result can be generalized such that if we have any contour or sum of contours that are not smooth, we can separate the contour integrals to be the sum of each segment such that
$$
\int\limits_{C}z \ dz = \sum\limits_{n=1}^{k}\int\limits_{C_{n}}z \ dz = \sum\limits_{n=1}^{k}\frac{z^{2}_{n+1}-z^{2}_{n}}{2}
$$
**Remark.**  Using the anti-derivative method is assuming the function is analytic in a domain. If we wanted to show the proof for any path, parametrization is the better option.

#### Branch Cuts
The path used in a contour integral can contain a point on a branch cut of the integrand involved. We will give two examples of such.

##### Example 1.
let $C$ denote the semicircular path 
$$
z=3e^{i \theta}, \quad (0 \leq \theta \leq \pi)
$$
from the point $z=3$ to the point $z=-3$. Although the [[Complex Elementary Functions#Branches and Derivatives of Logarithms|branch]] 
$$
f(z) = z^{\frac{1}{2}}= e^{\frac{1}{2}\ln z}, \quad (|z|>0,\ 0<arg \ z < 2\pi) 
$$
is not defined at the point $z=3$ of the contour $C$, the integral 
$$
I = \int\limits_{C}z^{\frac{1}{2}}\ dz
$$
still will exist! This is because its integrand is piecewise continuous on $C$ and hence the right-hand limits of the real and imaginary components of the function $f[z(\theta)]$ when $\theta=0$ exists. This allows us to have a definite integral. 

Now, since we know that this function will be single-valued and piecewise continuous on this contour such that there exists this integral, we can evaluate it as
$$
\int\limits_{C}z^{\frac{1}{2}} dz = \int\limits_{3}^{-3} z^{\frac{1}{2}}\ dz = \frac{2}{3} z^{\frac{3}{2}}\rvert_{3}^{-3}
$$
Now, as you may know, the square root results in two values, thus this integral would be 
$$
= 2\sqrt{3}(\pm i \mp 1)
$$
right? So how do we figure out which signs are correct? Well, we can use intuition and think about the contour. But this intuition falls apart for harder problems where it isn't so straight forward. We want to get rid of the periodicity of the complex numbers in order. We want the result that would be given if there were no periodicity with complex numbers. 

The way to do that is to plug in the end points in terms of the exponential form of complex numbers: $3e^{i \pi}$ and $3e^{i 0}$. This encodes which specific point we are talking about since now there is no ambiguity in which number we are talking about from the $2\pi n$ part of $re^{i (\theta+2 \pi n)}$. Thus, we will get the "generic" result in a sense, or the one that doesn't include multiple values. Thus, we get
$$
2\sqrt{3}(i+1)
$$
as our answer.

**Remark.**  Once again, we could have plugged in $z(\theta)=3e^{i \theta}$ and solved the integral that way too. Just pick the one that gives the easiest result. In this scenario, the power rule is much simpler so we kept it in terms of $z$ and not $\theta$. 

##### Example 2.
Now, let us have the Contour Integral 
$$
\int\limits z^{-1+i} \ dz
$$
Once again, we must identify which [[Complex Elementary Functions#Branches and Derivatives of Logarithms|branch]] we are working with. For this, let us use the principal branch such that 
$$
f(z) = z^{-1+i} = e^{(-1+i)Log\ z}, \quad (|z|>0, \ -\pi< Arg \ z < \pi)
$$
and we want a contour $C$ that goes about the unit circle. We create the parametrization to match with the branch such that 
$$
z=e^{i \theta}, \quad (-\pi \leq \theta \leq \pi)
$$
Now, we have defined a branch which makes this function single-valued and it is piecewise continuous. We can compute this integral as 
$$
\int\limits_{C}z^{-1+i} \ dz = \left. \frac{z^{i}}{i}\right\rvert_{e^{-i \pi}}^{e^{i \pi}} = -i((e^{\pi i })^{i} -(e^{-i \pi})^{i}) = i(-e^{-\pi}+e^{\pi} ) = 2i \sinh \pi
$$
Once again, we could have plugged in $f[z(\theta)]z'(\theta)$ which would've been
$$
e^{(-1+i)(i \theta)}ie^{i \theta} = ie^{i (i \theta)} = ie^{-i \theta}
$$
Which would've given the same result for our integral.

---
### Upper Bounds for Moduli of Contour Integrals 
We turn now to an inequality involving contour integrals that is extremely important in various applications. We present the result as a theorem but preface it with a needed lemma involving functions $w(t)$ of the type encountered as before:

**Lemma.**  If $w(t)$ is a _piecewise continuous_ complex-valued function defined on an interval $a \leq t \leq b$, then 
$$
\left|\int\limits_{a}^{b}w(t) \ dt\right| \leq \int\limits_{a}^{b}|w(t)| \ dt
$$
**Proof:**  This inequality clearly holds when the value of the integral on the left is zero. Thus, in the verification, we assume that its value is a nonzero complex number and write 
$$
\int\limits_{a}^{b}w(t) \ dt = r_{0}e^{i \theta_{0}}
$$
Solving for $r_{0}$, we get 
$$
r_{0}=\int\limits_{a}^{b}e^{-i \theta_{0}}w(t) \ dt
$$
Now the left-hand side of this equation is a real number, and so the right-hand side must be one too. Thus, using the fact that the real part of a real number is the number itself, we find that 
$$
r_{0}=Re \ \int\limits_{a}^{b}e^{i \theta_{0}}w(t) \ dt
$$
Hence, 
$$
r_{0}=\int\limits_{a}^{b} Re[e^{-i \theta_{0}}w(t)] \ dt.
$$
But, from [[Complex Numbers Algebraic Properties]], we know that $Re[z] \leq |z|$, so
$$
Re[e^{-i \theta_{0}}w(t) ]  \leq |e^{i \theta_{0}}w(t)| = |w(t)|
$$
so it follows that 
$$
r_{0} \leq \int\limits_{a}^{b}|w(t)| \ dt 
$$
Now, we know from before, that 
$$
\left|\int\limits_{a}^{b}w(t) \ dt\right|= |r_{0}e^{i \theta_{0}}| = r_{0}
$$

if we back-substitute $r_{0}$ back into the equation we get:
$$
\left|\int\limits_{a}^{b}w(t) \ dt\right| = r_{0} \leq \int\limits_{a}^{b}|w(t)| \ dt 
$$
Thus,
$$
\boxed{\left|\int\limits_{a}^{b}w(t) \ dt\right| \leq \int\limits_{a}^{b}|w(t)| \ dt }
$$

**Theorem.**  Let $C$ denote a contour of length $L$, and suppose that a function $f(z)$ is _piecewise continuous_ on $C$. If $M$ is a _nonnegative constant_ such that 
$$
|f(z)| \leq M
$$
for all points $z$ on $C$ at which $f(z)$ is defined, then 
$$
\left| \int\limits_{C} f(z) \ dz\right| \leq ML
$$

**Proof:**  To obtain this inequality, we assume that it holds and let 
$$
z=z(t), \quad (a \leq t \leq b)
$$
be a parametric representation of $C$. According to our lemma,
$$
\left|\int\limits_{C} f(z) \ dz\right| = \left|\int\limits_{a}^{b}f[z(t)]z'(t) \ dt\right| \leq \int\limits_{a}^{b}|f[z(t)]z'(t)| \ dt
$$
Inasmuch as 
$$
|f[z(t)]z'(t)| = |f[z(t)]| \ |z'(t)| \leq M \ |z'(t)|
$$
when $a\leq t\leq b$, except possibly for a finite number of points, it follows that 
$$
\left| \int\limits_{C}f(z) \ dz \right| \leq M \int\limits_{a}^{b}|z'(t)| \ dt
$$
Since the integral on the right represents the length ([[Complex Contours]], [[Arclength]]) of $C$, it follows that 
$$
\left| \int\limits_{C}f(z) \ dz \right| \leq M L
$$

**Remark.**  Note that since $C$ is a contour and $f$ is a piecewise continuous function on $C$, a number $M$ such as the one appearing in this inequality will always exist. This is because the real-valued function $|f[z(t)]|$ is continuous on the closed bounded interval $a\leq t\leq b$ when $f$ is continuous on $C$; and such a function always reaches a maximum value on that interval. The same is true when $f$ is _piecewise continuous_ on $C$ too. 

---
###### Example
If we let $C$ be the arc of the circle $|z|=2$ form $z=2$ to $z=2i$ that lies in the first quadrant, The upper bounds inequality can be used to show the upper limit of:
$$
\left|\int\limits_{C} \frac{z-2}{z^{4}+1} \ dz\right|
$$
This is done by first noting that if $z$ is a point on $C$, then according the the [[Complex Numbers Algebraic Properties#Triangle Inequality|Triangle Inequality]] 
$$
|z-2|\leq |z|+|2|=4
$$
and using the <mark style="background: #BBFABBA6;">Inverse Triangle Inequality</mark> we get
$$
|z^{4}+1| \geq ||z|^{4}-|1|| = |16-1|=15 
$$
Thus, from basic algebra we would know that 
$$
\frac{a}{b}\leq \frac{max\{a\}}{min\{b\}}
$$
we can thus conclude that 
$$
\left|\frac{z-2}{z^{4}+1}\right| = \frac{|z-2|}{|z^{4}+1|} \leq \frac{4}{15}
$$
Now, according to our theorem, and the fact that the length of this contour $C$ is $2\times \frac{\pi}{2}=\pi$, we can conclude that 
$$
\left|\int\limits_{C} \frac{z-2}{z^{4}+1} \ dz\right| \leq \frac{4 \pi}{15}
$$
we could also solve this by taking the integral and doing 
$$
\left|\int\limits_{C} \frac{z-2}{z^{4}+1} \ dz\right| \leq \int\limits_{C} \left|\frac{z-2}{z^{4}+1}\right| \ dz 
$$
and plug in $z=2e^{i \theta}$ and evaluating. Either way works. I find the first way to be much less cumbersome. 

---
###### Example 2
Let $C_{R}$ denote the semicircle 
$$
z=Re^{i \theta} \quad (0 \leq \theta \leq \pi)
$$
from $z=R$ to $z=-R$, where $R>3$. We want to find what 
$$
\lim_{R \rightarrow \infty} \int\limits_{C_{R}} \frac{(z+1) \ dz}{(z^{2}+4)(z^{2}+9)}
$$
is. How can we evaluate this? Well, if we decide to use the upper bound modulus theorem, we can observe that if a point $z$ is on $C$, then
$$
|z+1| \leq |z|+|1| = R+1
$$
and 
$$
|(z^{2}+4)(z^{2}+9)|=|z^{2}+4| \ |z^{2}+9| 
$$
We can find the minimum of this by finding the minimum value for each factor:
$$
|z^{2}+4| \geq ||z|^{2}-|4|| = R^{2}-4
$$
and 
$$
|z^{2}+9| \geq R^{2}-9
$$
Notice that we were able to get rid of the extra pair of absolute value signs because are positive since we defined that $R>3$. Now,
$$
|f(z)| \leq \frac{R+1}{(R^{2}-4)(R^{2}-9)} =M_{R}
$$
The length of our contour is $\pi R$, so we know that 
$$
\left|\int\limits_{C_{R}} \frac{(z+1) \ dz}{(z^{2}+4)(z^{2}+9)} \right| \leq M_{R}L = \frac{R+1}{(R^{2}-4)(R^{2}-9)} \pi R = \frac{\pi R(R+1)}{(R^{2}-4)(R^{2}-9)}
$$
If we take the limit of this as $R \rightarrow \infty$, we easily see that 
$$
\lim_{R \rightarrow \infty} \left|\int\limits_{C_{R}} \frac{(z+1) \ dz}{(z^{2}+4)(z^{2}+9)}\right|  = \lim_{R \rightarrow \infty}\frac{\pi R(R+1)}{(R^{2}-4)(R^{2}-9)} = 0
$$
Since the result of the contour integral is a complex number, and the modulus of the integral is going to $0$, then the result of the integral (the complex number) is going to $0$, and the only number with $0$ modulus is the number $0$. Thus, the integral must be approaching $0$ also. 


### Antiderivatives
Although the value of a contour integral from a fixed points $z_{1}$ to another fixed point $z_{2}$ depends, in general, on the path that is taken, there are certain functions which have contour integrals whose values are **independent of path**. 

The theorem for this contains an extension of the fundamental theorem of calculus and [[Fundamental Theorem of Line Integrals]]that simplifies the evaluation of many contour integrals. The extension involves the concept of an _antiderivative_ of a continuous function $f(z)$ on a domain $D$. Note that an antiderivative is, of necessity, an analytic function. Note too, that an antiderivative of a given function is unique _except for an additive constant_. 

This is because the derivative of the difference $F(z)-G(z)$ of any two such antiderivatives is zero; and, from the [[Complex Derivatives#Cauchy Riemann Equations|Cauchy-Riemann Equations]], an analytic function is constant in a domain $D$ when its derivative is zero throughout $D$.

**Theorem.**  Suppose that a function $f(z)$ is continuous in a domain $D$. If any one of the follows statements is true, then so are the others:

**a)**  $f(z)$ has an antiderivative $F(z)$ throughout $D$;

**b)**  the integrals of $f(z)$ along contours lying _entirely_ in $D$ and extending from any fixed point $z_{1}$ to another fixed point $z_{2}$ all have the same value, namely
$$
\int\limits_{z_{1}}^{z_{2}}f(z) \ dz = F(z_{2})-F(z_{1})
$$
where $F(z)$ is the antiderivative.

**c)**  The integrals of $f(z)$ around closed contours lying entirely in $D$ all have values of $0$. 


---
It should be emphasized that the theorem does **not** claim that any of these statements us true for a given function $f(z)$. It says only that all of them are true or none of them are true. 

Using antiderivatives is actually what we used earlier in [[#Example 1.]] and [[#Example 2.]] instead of direct parametrization. Either one works, so just chose the easiest one. Or parametrization may be used when a function does not have a derivative on the Contour.

---
###### Example
The function $f(z)=\frac{1}{z^{2}}$ is continuous everywhere except the origin and has an antiderivative $F(z)=\frac{-1}{z}$ in the domain $|z|>0$. Consequently,
$$
\int\limits_{C} \frac{dz}{z^{2}}=0
$$
when $C$ is a closed contour in this domain. 

**Remark.**  The integral of a function like $f(z)=\frac{1}{z}$ cannot be evaluated the same way since $F(z)$ is not differentiable, or even defined, along its branch cut.

---
###### Important Example - Extending Branch Cuts
What if we want to evaluate the integral of $\frac{1}{z}$ about the entire unit circle, we can separate the integral into two different branches and then add them.

Let $C_{1}$ denote the right half 
$$
z=e^{i \theta}, \quad \left(\frac{-\pi}{2}\leq \theta\leq \frac{\pi}{2}\right)
$$
of the circle $C$. The principle branch
$$
Log \ z = \log r+i\Theta \quad (r>0, \ -\pi< \Theta< \pi)
$$
of the logarithmic function serves as an antiderivative of the function $\frac{1}{z}$ in the evaluation of the integral of $\frac{1}{z}$ along $C_{1}$
$$
\int\limits_{C_{1}} \frac{dz}{z} = \int\limits_{-i}^{i} \frac{dz}{z} = Log(i)-Log(-i) = \pi i
$$
Now, if we do the same thing for the right side of the unit circle,
$$
z=e^{i \theta} \quad \left(\frac{\pi}{2}\leq \theta \leq  \frac{3 \pi}{2}\right)
$$
and consider the branch
$$
\log z = \ln r + i\theta \quad (r>0, \ 0<\theta< 2\pi),
$$
we would get
$$
\int\limits_{C_{2}} \frac{dz}{z} = \int\limits_{i}^{-i} \frac{dz}{z}= \log (-i)-\log(i) = \pi i
$$

Thus,
$$
\int\limits_{C} \frac{dz}{z}= \int\limits_{C_{1}} \frac{dz}{z} + \int\limits_{C_{2}} \frac{dz}{z} = 2\pi i 
$$
We also could've used parametrization for this result (which is arguably easier since we don't need to worry about the branch cuts since $f[z(\theta)]z'(\theta)$ is piecewise continuous on the interval $\theta \in (0,2\pi)$. 


##### Proof of Antiderivative Method
The proof can be seen around page 160 of [[Complex Variables Textbook.pdf]].

