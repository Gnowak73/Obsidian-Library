---
tags: Math, Fourier_Transform, Fourier_Series, Inner_Product, PDE, Integrals, technique 
dg-publish: true
mathLink: 
---
Subject: _Fourier Transform_
Main\_Topic: _Fourier Transform_
Applications: _PDEs, ODEs, system analysis_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]_
Closely\_Related\_To: _None_
_
_

```ad-note
The connection between Fourier and Lapalce is the substitution in the variable $s=iw$ (projection onto the imaginary axis), where s is the laplace variable and w is the fourier variable. 
```

Fourier Transforms are integral transforms that transform functions to a different "mathematical space". This transform is of the form:
$$
\hat f(k) \equiv \int\limits_{-\infty}^{+\infty} f(x)e^{-ikx} \ dx
$$
In order to be able to take the Fourier Transform we must be able to integrate it, this poses the condition ($L^{1}$ condition)
$$
\boxed{|\hat f(k)| \leq \int\limits_{-\infty}^{+\infty} |f(x)||e^{-ikx}| dx = \int\limits_{-\infty}^{+\infty} |f(x)| \ dx < \infty}
$$

```ad-note
 The Fourier Transform is a linear operator. 
```
---
##### Differentiation
If we take the Fourier Transform of a derivative, we end up with 
$$
\widehat{\frac{df}{dx}}(k) = \int\limits_{-\infty}^{+\infty} \frac{df}{dx}(x)e^{-ikx} \ dx = \lim_{L \rightarrow \infty} \int\limits_{-L}^{L} \frac{df}{dx}(x) e^{-ikx} \ dx
$$
Now, using integration by parts:
$$
\begin{gathered}
 = \lim_{L\rightarrow \infty}\left(-\int\limits_{-L}^{L} f(x) \frac{d e^{-ikx}}{dx} \ dx + \left.f(x)e^{-ikx}\right\rvert_{-L}^{L}\right)\\
 = \lim_{L\rightarrow\infty}\left(-\int\limits_{-L}^{L}f(x) (-ik)e^{-ikx} \ dx + f(L)e^{-ikL} - f(-L)e^{ikL} \right) \\
 = \lim_{L\rightarrow\infty}\left(-\int\limits_{-L}^{L}f(x)e^{-ikx}(-ik) \ dx \right)  \\
 = ik \int\limits_{-\infty}^{+\infty} f(x)e^{-ikx}\ dx \\
 = ik\hat f(k)   

\end{gathered}
$$
Notice that in this derivation, we have the terms with $f(L)$ and $f(-L)$ going to $0$. This is because it was a limit as $L\rightarrow\infty$, and we know that the condition for the Fourier Transform is the function being $L^{1}$, so the function must approach $0$ at the infinities.  We can summarize this derivation as follows:
$$
\boxed{\widehat{\frac{df}{dx}}(k) = ik\hat f(k)}
$$
or 
$$
\boxed{\widehat{\frac{df^{n}}{dx^{n}}}(k) = (ik)^{n}\hat{f}(k)}
$$
---
##### Inverse Fourier Transform
Say that we want the original function from the original mathematical space we started in. To do this, we take what is called the Inverse Fourier Transform:
$$
f(x) = \frac{1}{2\pi}\int\limits_{-\infty}^{+\infty} \hat{f}(k)e^{ikx} \ dk
$$
or
$$
\breve{g}(x) = \frac{1}{2\pi}\int\limits_{-\infty}^{+\infty} g(k)e^{ikx}\ dk
$$
The reason the $\frac{1}{2\pi}$ is there is because is needed to get the original function back when applying the inverse Fourier Transform to the Fourier Transform. Some people spread this factor of $2\pi$ into $\sqrt{2\pi}$ over both transform integrals or put it in the exponent. All of these notions are equivalent.
$$
\boxed{\mathcal{F^{-1}\{}{\mathcal{F \ f(k)}\}(x)} = f(x)} 
$$
---
##### Dirac Delta Function
The Dirac Delta function is a generalized distribution which looks like a "spike". It is used to represent instantaneous things. We can actually represent the dirac delta function as 
$$
\int\limits_{-\infty}^{+\infty} e^{-iky} \ dk = 2\pi \delta_{0}
$$
More can be seen in [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]].

---
##### Finding Transform of Functions we Know the Inverse Transform to
We can actually find the Fourier Transform of a function that we know the inverse transform. If we take the inverse Fourier Transform integral and make the small substitution:
$$
\breve{g}(-x) = \frac{1}{2\pi}\int\limits_{-\infty}^{+\infty} g(k)e^{-ikx} \ dk 
$$
then we can see that this integral on the left side is just the Fourier Transform from $k\rightarrow k$, so this relationship can be equated to 
$$
\boxed{2\pi \breve{g}(-x) = \hat g (x)}
$$
This means that we can find the Fourier Transform of a function by knowing the Inverse Fourier Transform. For example: let us take our knowledge that 
$$
\mathcal{F\{e^{-a|x|}}\}(k) = \frac{2a}{k^{2}+a^{2}}
$$
thus, by our formulation, we can see that 
$$
\mathcal{F\{\frac{2a}{x^{2}+a^{2}}  \}}(k) = 2\pi e^{-a|x|} 
$$
---
##### Transform of complex function
We can separate the Fourier Transform into a real and imaginary integral by the simple relationship
$$
f(x) = f_{1}(x)+if_{2}(x)
$$
This also means that each real or imaginary part that is separated <mark style="background: #BBFABBA6;">MUST STILL BE</mark> $L^{1}$. 

---
##### Convolution
The convolution is a form of "multiplication". It is defined as 
$$
(f*g)(x) \equiv \int\limits_{-\infty}^{+\infty} f(x-y)g(y)\ dy
$$
where x is fixed. The order of the convolution doesn't matter, so $(f*g) = (g*f)$.

The Derivative of convolutions can be easily seen since the derivative can be brought into the integral as a partial derivative [[Leibniz Integral Rule]]. From this we can easily see that $(f*g)'(x) = (f'*g)(x) = (f*g')(x)$. 

Finally, we can see that the Fourier Transform of the Convolution is the multiplication of two Fourier Transforms:
$$
\boxed{\widehat{(f*g)}(k) = \hat f(k) \hat g(k)}
$$
We can also look at the inverse Fourier Transform to see that 
$$
\boxed{\mathcal{F}^{-1}(\hat f(k) \hat g(k)) = (f*g)(x)}
$$

We can finally see that convolutions can apply to simply the Fourier Transform of the product of two functions:
$$
\boxed{\widehat{f(x)g(x)}(k) = \frac{1}{2\pi}(\hat f*\hat g)(k)}
$$
We can actually bypass using convolutions though by using the [[Heaviside Alternative to the Convolution]].

---
### Important Rules (Do Not Forget)
1. Shifting Rule: $\widehat{f(x-a)} = e^{-iak} \hat f(k)$ and $\widehat{e^{iax}f(x)} = \hat f(k-a)$ 
2. Scaling Rule ($a>0)$: $\widehat{\frac{1}{a}f(\frac{x}{a})} = \hat f(ak)$  and  $\widehat{f(ax)} = \widehat{ \frac{1}{a} f\left(\frac{k}{a}\right)}$ 
3. Polynomial Multiplication in Real Space: $\widehat{xf(x)} = i\frac{d \hat f(k)}{dk}$ 
4. Invariance of a Gaussian: if $f(x)=e^\frac{-x^{2}}{2}$, then $\hat f(k) = \sqrt{2\pi} e^{\frac{-k^{2}}{2}}$
5. If $f(x)=e^{-ax^{2}},$ then $\hat f(k) = \frac{\sqrt{\pi}}{\sqrt{a}}e^{\frac{-k^{2}}{4a}}$.  


![[Pasted image 20230624194942.png|center|350]]
![[Pasted image 20230624195002.png|center|350]]
![[Pasted image 20230624195022.png|center|350]]


### Examples
Examples about applying the Fourier Transform to Diffusion Equation etc. can be found in [[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]].