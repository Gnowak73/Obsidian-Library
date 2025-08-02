---
tags: Math, ODE, theorem, technique 
dg-publish: true
mathLink: 
---
Subject: _ODE_
Main\_Topic: _First Order Linear ODE Constant Coefficients_
Applications: _First Order ODE technique_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
If we have an ODE, for example:
$$
ay'' + by' + cy = 0
$$
where $a, b, c$ are all constants, then we could make the substitution $y=e^{rx}$ into the equation to get the polynomial equation in r:
$$
ar^{2}+br+cr=0 
$$
which we can solve for $r$ and plug into our solution $y=e^{rx}$. Due to [[Superposition Linear ODE and PDE|Superposition]], we then add these different exponentials together for the general solution, creating a [[Superposition Linear ODE and PDE#Solution Space|solution space]] [[Function Linear Algebra#Basis Algebra|basis]] $\{e^{r_{1}x},e^{r_{2}x}\}$. 

##### Repeated Roots
If we have repeated roots, we then increase the degree of $x$ multiplied by the exponential. For example:
$$
y(x) = c_{1}e^{r_{1}x}+c_{2}xe^{r_{1}x} + c_{3}x^{2}e^{r_{1}x}
$$
###### Proof
If we take a linear ODE of the form
$$
a_{n}r^{n}+\ldots +a_{1}r+a_{0}=0
$$
as our characteristic equation and we have repeated roots, then factoring we would have something where there is a multiplicity involved
$$
(r-r_{1})^{k}(r-r_{0})=0
$$
We can write the polynomial differential operator 
$$
L\equiv (D-r_{1})^{k}(D-r_{0})
$$
for the ODE $Ly=0$. Solutions for the linear factors will result in $y=e^{r_{0}x}$ and $y=e^{r_{1}x}$ as a guarantied solutions. We can take this and speculate that there is a function $u(x)$ such that there is a general solution $Y(x)=u(x)e^{r_{1}x}$. We observe that 
$$
(D-r_{1})[ue^{r_{1}x}] = (Du)e^{r_{1}x}+r_{1}ue^{r_{1}x}-r_{1}ue^{r_{1}x} = (Du)e^{r_{1}x}
$$
which can be generalized to 
$$
(D-r_{1} )^{k}[ue^{r_{1}x}] = (D^{k}u)e^{r_{1}x}
$$
This means that the solution $y=u(x)e^{r_{1}x}$ must follow 
$$
(D-r_{1})^{k}[ue^{r_{1}x}]=(D^{k}u)e^{r_{1}x}=0
$$
Which can only happen if $D^{k}u=0$, a result that is only true for $u(x)$ being a polynomial of at most degree $k-1$. So,
$$
y(x) = u(x)e^{r_{1}x} = (c_{1}+c_{2}x+\ldots+c_{k}x^{k-1})e^{rx}
$$

##### Complex Roots
If we have complex roots, we can just use Eulers Formula: $e^{i\theta}=\cos\theta+i\sin\theta$ to formulate
$$
\begin{gathered}
c_{1}e^{ir_{1}x}+c_{2}e^{-ir_{1}x} = c_{1}\cos(r_{1}x)+c_{1}i\sin(r_{2}x) + c_{2}\cos(r_{1}x)-c_{2}i\sin(r_{1}x) \\
= (c_{1}+c_{2})\cos(r_{1}x)+(c_{1}i-c_{2}i)\sin(r_{1}x) \\
= A\cos(r_{1}x)+B\sin(r_{1}x)
\end{gathered}
$$
###### Repeated Complex Roots
If we have a repeated complex root, we do the same procedure as before, increasing the degree of $x^{k-1}$ in front of each term, where $k$ is the multiplicity of the root. 


