---
tags: theorem, Math, Complex_Analysis, Integrals
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Conjugate of Integrals_
Applications: _[[Contour Integrals]], QM, [[Function Linear Algebra#Complex Plane|Complex Inner Product]]_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

### One Function?
$$
\overline{\int\limits f(z)dz} = \int\limits \overline{f(z)} dz?
$$
Not all the time. If $f$ is a function of a real variable then:
$$
\int\limits f(t)dt = \int\limits Re(f)+iIm(f) \ dt
$$
so 
$$
\begin{gathered}
\overline{\int\limits f(t)dt} = \overline{\int\limits Re(f)+iIm(f) \ dt} = \int\limits Re(f)dt -i\int Im(f)dt \\
 = \int\limits Re(f)-iIm(f) \ dt = \int\limits \overline{f(t)} dt
\end{gathered}
$$
Thus, if $f$ is real valued, then yes! But what about if $f$ isn't real valued? Then we would have
$$
\begin{gathered}
\overline{\int\limits f(z) dz} = \overline{\int\limits Re(f)+iIm(f)(dx+idy)} \\
= \overline{ \int\limits Re(f) dx-iRe(f)dy-iIm(f)dx-Im(f)dy} \\
=\int\limits Re(f)dx-iRe(f)dy-iIm(f)dx-Im(f)dy \\
 =\int\limits (Re(f)-iIm(f)) (dx-idy) = \boxed{\int\limits \overline{f(z)} \ \overline{dz}}

\end{gathered}
$$
Thus, we can say in general for any example:
$$
\boxed{\overline{\int\limits f(z)dz} = \int\limits \overline{f(z)} \ \overline{dz}}
$$


### Two functions?
$$
\overline{\int\limits f(z)g(z)dz} = \int\limits \overline{f(z)g(z)} dz \ ?
$$
Once again, lets distribute the $dz=dz+idy$ relationship in the integral:
$$
\begin{gathered}
\overline{\int\limits (u_{f}+iv_{f})(u_{g}+iv_{g})(dx+idy)} \\
= \int\limits \overline{(u_{f}u_{g}+iv_{g}u_{f}+iv_{f}u_{g}-v_{f}v_{g})(dx+idy)} \\
= \int\limits\overline{Re(u_fu_g)+iIm(u_{f}u_{g})(dx+idy)}

\end{gathered}
$$
we represented the Real and Imaginary parts of $f(z)g(z)$ as their own new function. Now, we can employ the same equation that we used in [[#One Function?]] with this new function combining $f$ and $g$:
$$
\begin{gathered}
 = \int\limits \overline{Re(u_{f}u_{g})-iIm(u_{f}u_{g})} \ \overline{dz} = \int\limits u_{f}u_{g}-iv_{g}u_{f}-iv_{f}u_{g}-v_{f}v_{g} \ \overline{dz} \\
 = \int\limits (u_{f}-iv_{f}) (u_{g}-iv_{g}) \ \overline{dz} \\
 = \boxed{\int\limits\overline{f(z)g(z)} \ \overline{dz}}

\end{gathered}
$$

This result can be further generalized for any multiplication of functions in the integrand! 


