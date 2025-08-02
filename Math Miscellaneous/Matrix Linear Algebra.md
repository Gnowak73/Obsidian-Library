---
tags: Math, Linear_Algebra, Matrix
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Matrix Linear Algebra_
Applications: _Linear Systems, Matrices_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

Matrices can be manipulated in a number of ways such as [[Gauss-Jordan Elimination]]. Some of these properties are discussed below.

##### Multiplication
For matrix multiplication, everything goes, except two scenarios: 
1. Multiplication does not commute: $AB \neq BA$ 
2. The number of columns in the first matrix must equal the number of rows in the second matrix


##### Linear Operations
All linear operators work out such as addition, subtraction, multiplication by a constant, etc. 


##### Square Matrix Rules
If $A$ is a square $n\times n$ matrix, then
$$
\begin{aligned}
A^{0}=I\\
A^{n+1}=A^{n}A, \quad n\geq 1 \\
A^{-n}=(A^{-1})^{n} \\
A^{r}A^{s}=A^{r+s} \\
(A^{r})^{s}=A^{rs}
\end{aligned}
$$
---
### Inverse Matrix
A matrix has an inverse such that 
$$
A^{-1}A=AA^{-1}=I
$$
where $I$ is the identity matrix. 

An invertible matrix is a square matrix such that $AB=BA=I$. It is also worth noting that if the matrix $A$ is invertible, then there exists precisely ONE unique matrix such that $AB=BA=I$. 

So how do we find these inverse Matrices? One way is with what is called an <mark style="background: #FFB86CA6;">Elementary matrix</mark>. An elementary matrix $E$ is defined as an $n\times n$ matrix that can be obtained by performing a single elementary row operator on the $n\times n$ identity matrix $I$. 

Now suppose that we have an elementary matrix $E$ that corresponds to a certain elementary row operation. It turns out that if we perform this same operation on an arbitrary matrix $A$, we get the product matrix $EA$. We can actually do this until we get the identity matrix:
$$
E_{1}E_{2}\ldots E_{n}A = I_{n\times n}
$$
Thus, we could write any matrix $A=E_{n}^{-1}\ldots E_{2}^{-1}E_{1}^{-1} I$. If we invert each side of this equation (which is possible since all $E_{n}$ are square and have nonzero determinants), then we have 
$$
A^{-1}=E_{k}E_{k-1}\ldots E_{2} E_{1}I
$$
Thus, by finding out the row operations needed to transform $A$ into $I$, we can find $A^{-1}$. We can easily do this by using Gauss Elimination:
$$
\begin{bmatrix}a_{1}&a_{2}&a_{3}&|&1&0&0\\a_{4}&a_{5}&a_{6}&|&0&1&0\\a_{7}&a_{8}&a_{9}&|&0&0&1\end{bmatrix}
$$
we then do row operations until we get the Identity matrix on the left side, and at that point, the right side will be equal to the inverse of $A$. 

```ad-tip
We can also calculate these inverse matrices by using the Cofactor and the [[Transpose]]:  [[Determinant#Calculating Inverse Matrix by Cofactor]]
```

---
##### Inverse Matrix Solution Ax=b
If we have a system of linear equations:
$$
Ax=b,
$$
then there is a unique solution 
$$
x=A^{-1}b
$$
---
##### 2x2 matrix inverse
The 2x2 matrix 
$$
A = \begin{bmatrix}a&b\\c&d\end{bmatrix}
$$
is invertible if the [[Determinant]] is nonzero, in which
$$
A^{-1}=\frac{1}{|A|}\begin{bmatrix}d&-b\\-c&a\end{bmatrix}
$$
