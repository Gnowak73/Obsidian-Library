---
tags: Math, Linear Algebra, ODE
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Linear Independence_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
If vectors are linearly independent, then each vector cannot be created from the sum of a constant times the other vector or vectors. In other words: <mark style="background: #ADCCFFA6;">no redundancy</mark>. 

By definition, vectors are linearly independent if for the equation
$$
c_{1}\pmb{x_{1}}+ \ldots+c_N\pmb{x}_{N}= \pmb{0}, \quad \text{then} \quad c_1=c_2=\ldots=c_N=0
$$
in other words, only the trivial solution exists for linearly independent vectors. 

We can check for linearly independent by either creating a system of equations or this simple trick (only works if number of vectors is equal to dimensions of the Euclidean space):

take our vectors and put them into a matrix
$$
\begin{bmatrix} v_{1} & u_{1}&x_1 \\ v_{2} & u_{2}& x_2\\  v_{3 } & x_3 & u_{3} \\ \end{bmatrix}
$$
and check if the determinant is zero. If it is not, then there is a linear independence of the columns.


> Note: a set of n-independent vectors in $\mathbb{R}_N$ always spans $\mathbb{R}^N$ 

```ad-note
Spanning Implies Linear Independence: Linear Independence DOES NOT imply Spanning!
```

###### Linear Function
A function or transformation is linear if it follows these two behaviors:
1. $$
u(x+y) = u(x)+u(y)
$$
2. $$
u(c_{1}x) = c_{1}u(x)
$$


## Continuous Functions
If $f$ and $g$ are differentiable functions on an interval, lets say $[a,b]$, then if the Wronskian $W(f,g)(t_{0})$ is nonzero for some $t_0$ in $[a,b]$, then $f$ and $g$ are linearly independent on $[a,b]$. If $f$ and $g$ are linearly dependent then the Wronskian is zero for all $t$ in $[a,b]$, where 

$$
W = \begin{vmatrix} f &g\\ f'&g' \end{vmatrix}

$$
