---
tags: Analytic, analyticity, functions, complex, Math, analytic_functions, derivative, entire
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Analytic Functions_
Applications: _Derivatives on the Complex Plane, Functional Analysis_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Complex Derivatives]], [[Complex Continuity]],[[Regions in the Complex Plane]]_
Cont.\_ of: _None_ 
_
_
```ad-Definition
A function $f$ of the complex variable $z$ is _analytic_ in an **open set** $S$ if it has a derivative everywhere in that set. It is _analytic at a point_ $z_{0}$ if it is analytic in some neighborhood of $z_{0}$. 
```

---
**Question: Why is analyticity defined for an open domain and in a neighborhood? Does a derivative require continuity in a neighborhood? Does a function need to be differentiable in a neighborhood?**  Continuity is defined on an open set, and mostly so is differentiation, thus so would analytic functions. 

Some of the conditions of differentiation can be seen in [[Differentiability Conditions for All Dimensions]].

**It is very important** though that we realize that analytic functions are not defined only by derivatives but also defined by the ability to form a [[Taylor Series]] that converges to a function at a point. Thus, there needs to be a radius of convergence associated with analytic functions, and thus analytic functions must be analytic in a neighborhood! 

---


**Remark.**  Note how it follows that is $f$ is analytic at a point $z_{0}$, it must be analytic at _each_ point in some neighborhood of $z_{0}$. If we should speak of a function that is analytic in a set $S$ that is not open, it is to be understood that $f$ is analytic in an open set containing $S$. 

```ad-Definition
An _Entire_ function is a function that is analytic at each point in the entire plane. 
```

The different theorems for [[Complex Derivatives]] holds for analytic functions. For example, if two functions are analytic in $D$, so is their sum, their composition, their product, and so on. 

We can actually see that if $f'(z)=0$ everywhere in a domain $D$, then $f(z)$ must be constant throughout $D$. We can see this from the [[Complex Derivatives#Cauchy Riemann Equations|Cauchy-Riemann Equations]] since consequently this would result in 
$$
u_{x}=u_{y}=0 \quad \text{and} \quad v_{x}=v_{y}=0
$$
at each point in $D$. 

We can use a similar argument with [[Directional Derivative|directional derivatives]] to show how this results in a constant function along any curve or vector in a domain $D$. 

```ad-Definition
If a function $f$ fails to be analytic at a point $z_{0}$ but is analytic at some point in every neighborhood of $z_{0}$ then $z_{0}$ is called a _Singular Point_, or _singularity_, of $f$. 
```

---
#### Constant Modulus of Analytic Function
**Theorem.**  If an analytic function has a constant modulus throughout a given domain $D$, then the function $f$ must be constant there too.

**Proof:**  Let us write 
$$
|f(z)| = c \quad \text{for all $z$ in $D$},
$$
where $c$ is a real constant. If $c=0$, it follows that $f(z)=0$ everywhere in $D$. If $c \neq 0$, the property $z \overline{z}=|z|^{2}$ of complex numbers tells us that 
$$
f(z)\overline{f(z)} = c^{2} \neq 0
$$
and hence that $f(z)$ is never zero in $D$. So we can write
$$
\overline{f(z)} = \frac{c^{2}}{f(z)} \quad \text{for all $z$ in $D$} ,
$$
and it follows from this that $\overline{f(z)}$ is analytic everywhere in $D$ since its the quotient of two analytic functions. And we know that if a function $f$ and its conjugate $\overline{f}$ are analytic, then $f$ must be constant. (We will prove this below: [[#A function is constant if it and its conjugate are Analytic]]).

---
#### A function is constant if it and its conjugate are Analytic
**Theorem.**  If a function $f(z)=u(x,y)+iv(x,y)$ is analytic and its conjugate $\overline{f(z)}=u(x,y)-iv(x,y)$ are both analytic in $D$, then they must both be constant in $D$. 

**Proof:**  All analytic functions must follow the [[Complex Derivatives#Cauchy Riemann Equations|Cauchy Riemann Equations]] and have continuous partial derivatives. If we look at the Cauchy Riemann Equations for $f$ and $\overline{f}$, we see that 
$$
\begin{gathered}
u_{x}=v_{y}, \quad u_{y}=-v_{x} \\
u_{x}=-v_{y}, \quad u_{y}=v_{x}
\end{gathered}
$$
For both of these sets of equations to be true, $u$ and $v$ must be constant since their partial derivatives are $0$. Thus, $f$ and $\overline{f}$ must be constant too. 
