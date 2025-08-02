---
tags:
  - QM
  - Fourier_Duals
  - Fourier_Transform
  - Physics
dg-publish: true
mathLink:
---
Subject: _Quantum Mechanics_
Main\_Topic: _Fourier Transforms, Conjugate Momentum_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

The supposition that momentum space variables consists of functions that are the [[Fourier Transform]] of a set of coordinate variables $(x^1,x^2,\ldots,x^n)$ implies that $p_{i}= -i\hbar \frac{\partial}{\partial x^i}$. To prove this, we would like to show 
$$
\mathcal{F}[\hat{p}_{k}\psi(q)] = p_{k}\tilde\psi(p).
$$
First, we compute 
$$
\hat{p}_{k}\psi(q) = -i\hbar \frac{\partial}{\partial q_{k}\psi(q)}= -i\hbar \frac{\partial}{\partial q_{k}}\left(\frac{1}{(2\pi \hbar)^{\frac{n}{2}}}\int\limits e^{\frac{i p\cdot q}{\hbar}} \tilde\psi(p)\ d^{n}p\right)
$$
If we bring the derivative inside the integral:
$$
= \frac{1}{(2\pi \hbar)^{\frac{n}{2}}} \int\limits \left(-i\hbar \frac{\partial}{\partial q_{k}}e^{i p\cdot q/\hbar}\right)\tilde\psi (p)\ d^np
$$
$$
= \frac{1}{(2\pi \hbar)^{\frac{n}{2}}} \int\limits \left(p_ke^{i p\cdot q/\hbar}\right)\tilde\psi (p)\ d^np.
$$
Now, we may conclude that 
$$
\left(-i\hbar \frac{\partial}{\partial q_{k}}\psi(q)\right) = \mathcal{F}^{-1}[p_{k}\tilde\psi(p)] 
$$
thus proving that multiplication by $p_k$ in momentum space corresponds to the operator $-i\hbar \frac{\partial}{\partial q_{k}}$ in coordinate space. An important remark here is that in $d^{n}p$ we implicitly absorb the curvature of the momentum space $\sqrt{g(p)}$ in the integral. This proof works as long as the metric tensor over the momentum is independent to that of position (or the phase space can admit an independent momentum space such that $x$ and $p$ are not inherently coupled).

The problem with having all the momentum operators being $p_{i}= -i\hbar \frac{\partial}{\partial x^{i}}$ is that the momentum is not Hermitian with the curvilinear volume element measures. Partial derivatives are not Hermitian in curved spaces, covariant derivatives are. Thus, a proper Hermitian momentum will naturally have a covariant derivative. Geometrically, this makes sense, as we are on a curved space anyways. This results in the eigenstates of momentum with eigenvalue $p$, or $\hat{p}_{k}\psi(x) = p\psi(x)$, having additional curvature terms such that eigenstates of momentum are not built from plane waves. And no, these extra curvature factors are not the Jacobian determinants such that its just a flat plane wave in a new coordinate system. 

Instead of using Dirac Notation, we will derive this with very elementary quantum mechanics to get a feel for the foundations. Q: The momentum eigenfunction equation tells us what? A: the solutions to $\hat{p}\psi(x)=p\psi(x)$ are the states $\psi(x)$ which will give us momentum $p$ such that $\langle p \rangle = \int\limits \psi^{*}(x) \hat{p}\ \psi(x) \ dx = p$. Now, if we solve in flat space 1D, we get $\psi(x) = A e^{i xp/\hbar}$ (in 3D we separate the integrals using [[Fubini's theorem]] to get the product of three 1D solutions along $x,y$, and $z$). We may find the constant $A$ using normalization (assuming Born's interpretation of $\psi$ as a probability amplitude holds). For now, we don't really care what $A$ is.

The important part is that
$$
\int_{-\infty}^{+\infty} \psi^{*}(x')\psi(x) \ dp = \delta(x-x').
$$
Why is this important? Well, first we are showing $\psi(x)$ is orthogonal in momenta. So, in a sense, if we imagine the mathematical space of functions, they all point in different directions to cover all states. This is very analogous to [[Vector Linear Algebra]] (which Dirac notation is built upon). From just a purely computational sense, though, this quality means we can take the trivial identity
$$
\phi(x) = \int\limits_{-\infty}^{+\infty} \phi(x')\delta(x-x') \ dx'
$$
and write 
$$
\phi(x) = \int\limits_{-\infty}^{+\infty} \left[\int\limits_{-\infty}^{+\infty}\psi^{*}(x')\psi(x) \ dp\right] \phi(x') \ dx'.
$$
If we use Fubini's theorem (since we are dealing with square integrable functions) and switch the orders of integration, then 
$$
\phi(x) = \int\limits_{-\infty}^{+\infty} \left(\int\limits_{-\infty}^{+\infty} \psi^{*}(x')\phi(x') \ dx'\right) \psi(x) \ dx.
$$
Remember that $\psi(x)$ had $p$'s in it, so if we integrate through all of the $x$'s, we should be left with a function of $p$. Okay, so lets call the thing in the parenthesis $c(p)$. We define
$$
c(p) := \int_{-\infty}^{+\infty} e^{\frac{-i}{\hbar}xp}\ \phi(x) \ dx
$$where we wrote $x$ instead of $x'$ since we are not looking at the iterated integral. Well, you may recognize that if we include the correct constant $A=1/(2\pi \hbar)$, then this is just the inverse Fourier Transform! Then, we have
$$
\phi(x) = \int\limits_{-\infty}^{+\infty} c(p) \psi(x) \ dx = \int\limits_{-\infty}^{+\infty} c(p) e^{\frac{i}{\hbar}xp} \ dx
$$
which is the regular forward Fourier Transform! So, with the Fourier Transform, we are able to go from position to a momentum function and vise versa. Furthermore, the regular properties of wave functions can be shown to hold, and we can show that the transform of operators changes them from one representation to another. 

Mathematically, we are taking states and projecting them onto position or momentum basis eigenfunctions. We can use this principle to write states like vectors, giving the same results but in tidier notation. 

Now, back to curved space. If we create a Hermitian momentum operator by symmetry $\frac{1}{2}(\hat{p} + p^{\dagger})$ in curved space or use the covariant derivative from the start (both give the same result) then we may figure out $u_{p}(x)$ such that $\hat{p}u_{p}(x) = pu_{p}(x)$ to get the basis of momentum eigenstates in the position representation. However, if $\hat{p}$ has the covariant derivative, which we can write using $D\psi = \frac{1}{\sqrt[4]{g}}\partial_{i}(\sqrt[4]{g} \psi)$, we find that there is some leftover $1/\sqrt[4]{g}$ terms that show up. When doing the calculations, this term actually stays present in the momentum and position eigenstates, and enforces geometric concerns onto $\psi$. The point is: eigenstates are no longer plane waves. Because of this, we don't have the privilege of using Fourier Transforms anymore. Rather, we have something similar, but not quite the same. 

**Remark.**  From first principles, we can actually work backwards to find $\hat{p}_k$ in curved space using $\hat{p}_{k}\tilde\psi(p)=p\tilde\psi(p)$. 

Another way of looking at this may be to use superposition. If we have these momentum eigenfunctions which are orthogonal, and they span the entire space of states, then any state is the arbitrary sum of momentum eigenfunctions. 

Well, the caveat is proving that the momentum eigenfunctions span the entire space. We will do this in a moment. But first, let us imagine the superposition principle of states as given by the Schrodinger Equation. Imagine we start with nothing, and add $e^{ikx}$ plane waves up over and over again with varying wavenumber $k$ to get a function. This is the essence of a Fourier Series (and Transform). We are adding these plane waves over and over again to build up a $\phi(x)$, whatever it may be (but it acts nicely for $L^{2}$ functions in particular). As we add these plane waves up, we may write 
$$
\psi(x) = \sum\limits_{n} e^{i k_{n} x} c_n.
$$
However, de-Broglie says that we have $p=\hbar k$. So, we can write 
$$
\psi(x) = \sum\limits_{n} e^\frac{i px}{\hbar}c_n.
$$
$c_n$ are just arbitrary constants that determine the amplitude of each wave we are adding up. Note that this is simply a Fourier Series. In the limit for an infinite space we can retrieve the Fourier Transform, where we recognize $c_{n}$ as the counterpart $\tilde\psi(p).$ We can go a step further and multiple each side by $e^{ip'x/\hbar}$ and integrate to get a Dirac delta on the RHS:
$$
\int\limits \psi(x)e^{ip' x/\hbar} dp = \int\limits\sum\limits_{n} e^\frac{i px}{\hbar}c_{n}e^{ip' x/\hbar}.
$$
After applying Fubini's theorem, we may switch the other of the sum and integrand (the proof for this is tricky, see more intense mathematics) and we end up with
$$
c_{n}= \langle \psi(x),e^{ip'x/\hbar}\rangle
$$
ignoring normalization constants. This is the exact same formula from linear algebra and basis in [[Vector Linear Algebra]]! Note we can prove a basis is complete by using the inner product just like in Vector Linear Algebra and what we intuitively did above under the guise of physical interpretations.

For a formal proof that the momentum eigenstates do form a basis, we may use such an inner product proof (proving that there exists constants $\alpha_{i}$ such that $\phi(x) = \sum\limits_{i} \alpha_{i} \psi_{i}(x)$ holds arbitrarily, so we prove the Gram-Schmidt matrix is invertible, etc.). We may also do an extension of the finite case into the infinite case. Suppose we have infinite orthonormal functions $\{\phi_{n}(x)\}$, like sine/cosine. Also assume we are working in a Hilbert space like $L^{2}(\mathbb{R})$. In this case, we say that the set is complete if for every $f\in L^{2}(\mathbb{R})$, and every $\epsilon>0$, there exists a finite linear combination
$$
S_{N}(x) = \sum\limits_{n=1}^{N} a_{n}\phi_{n}(x)
$$
such that 
$$
||f-S_{N}||_{L^{2}}<\epsilon.
$$
This forces convergence of any function $f$ to be arbitrarily close to a sum of basis functions. This means the span is dense in $L^{2}$, i.e.,
$$
\overline{\text{span}\{\phi_{n}\}}=L^{2} (\mathbb{R})
$$
so the closure of the span is the entire space. Remember that the closure is the set of all limits (in a norm) of sequence in a space.

How do we prove this infinite-dimensional completeness? Well, we can't check all $f$. However, note that in the finite dimensional case: if a set spans $V$, no nonzero vector can be orthogonal to all of it. Why? Because, if there exists such a vector, then we have a contradiction that the set spans $V$. As, there is some element of $V$ linearly independent and not reached by the spanning set. This is probably the easiest condition to show. We state more in general below:

**Theorem.**  Let $\mathcal{H}$ be a Hilbert space, and let $\{\phi_n\}_{n=1}^\infty \subset \mathcal{H}$ be an orthonormal set. The following statements are equivalent:

1. (Completeness / Density)
The linear span of $\{\phi_n\}$ is dense in $\mathcal{H}$:
$$
\overline{\text{span} \{\phi_n\}} = \mathcal{H}.
$$
---
3. (Norm-Convergent Expansion)
For every $f \in \mathcal{H}$, the series converges in norm:
$$
f = \sum_{n=1}^\infty \langle \phi_n, f \rangle \phi_n.
$$
---
3. (Parseval's Identity)  
For every $f \in \mathcal{H}$,
$$
\|f\|^2 = \sum_{n=1}^\infty |\langle \phi_n, f \rangle|^2.
$$
---
4. (Uniqueness of Coefficients)  
If
$$
\langle f, \phi_n \rangle = 0 \quad \text{for all } n,
$$
then
$$
f = 0.
$$


---
So, what have we learned from using this linear algebra notation? That we can represent any state $\phi(x)$ as a sum of the momentum eigenstates, as proving 4. for the eigenstates found is quite a simple task. Assume that 
$$
\langle f(x), \psi_n(x)\rangle = \int\limits_{-\infty}^{+\infty} f(x)\ e^{ip \frac{x}{\hbar}} \ dx = 0= \mathcal{F}[f(x)].
$$

for all $p$. Then, there are many theorems to show that $f(x)$ must be $0$. Either the Riemann-Lebesque lemma or the property of injectivity and 'unitary-ness' of the Fourier Transform.

