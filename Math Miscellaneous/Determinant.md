---
tags: Math, Linear_Algebra, Matrix
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Determinants_
Applications: _Matrices, Linear Systems, [[System of Linear ODEs Constant Coefficients|System of Linear ODEs]], [[Matrix Linear Algebra]]_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

A matrix has a determinant if it is a square matrix and it is defined for a $2\times 2$ matrix as
$$
|A| = det \ A = \begin{vmatrix}a&b\\c&d\end{vmatrix} = ad-bc
$$
Determinants are often used to solve a $2\times 2$ system of linear equations of the form
$$
\begin{gathered}
a_{11}x+a_{12}y=b_{1} \\
a_{21}x+a_{22}y=b_{2}
\end{gathered}
$$
It follows that this system has a unique solution if and only if its coefficient determinant is nonzero (in order to have an inverse matrix).

#### Cramer's Rule
Cramer's Rule says that a unique solution for the $2\times 2$ system of linear equations as given above is given by 
$$
\begin{gathered}
x=\frac{\begin{vmatrix}b_{1} &a_{12}\\b_{2}&a_{22}\end{vmatrix}}{\begin{vmatrix}a_{11} &a_{12}\\a_{21}&a_{22}\end{vmatrix}}, \ y=\frac{\begin{vmatrix}a_{11}&b_{1}\\a_{21}&b_{2}\end{vmatrix}}{\begin{vmatrix}a_{11} &a_{12}\\a_{21}&a_{22}\end{vmatrix}}
\end{gathered}
$$
This can be generalized to 
$$
x_{i}=\frac{|a_{i}\ldots b \ldots a_{n}|}{|A|}
$$
for the system $Ax=b$, $A=[a_{1} \ a_{2} \ a_{3}\ \ldots \ a_{n}]$. 

### Higher Order Dimensions
For higher order dimensions determinants, we define determinants in terms of smaller ones. For example, in 3 dimensions we have:
$$
\left|
\begin{matrix}
    a_{11} & a_{12} & a_{13}  \\
    a_{21} & a_{22} & a_{23}  \\
    a_{31} & a_{32} & a_{33}  \\
\end{matrix}%
\right|
=a_{11}\begin{vmatrix}a_{22}&a_{23}\\a_{32}&a_{33}\end{vmatrix}-a_{12}\begin{vmatrix}a_{21}&a_{23}\\a_{31}&a_{33}\end{vmatrix}+a_{13}\begin{vmatrix}a_{21}&a_{22}\\a_{31}&a_{32}\end{vmatrix}
$$

#### Minors and Cofactors
Minors are the determinant if you chose an element and ignore that entire row and column of that specific element in the matrix. For example, we we found the <mark style="background: #FFF3A3A6;">minor</mark> of $a_{12}$
$$
M_{12} = \begin{vmatrix}a_{21}&a_{23}\\a_{31}&a_{33}\end{vmatrix}
$$
The <mark style="background: #FF5582A6;">Cofactor</mark> is defined as 
$$
A_{ij}=(-1)^{i+j} \ M_{ij} 
$$
The negative 1's can be seen as an alternating pattern in the matrix:
$$
\begin{bmatrix}
    + & - & +  \\
    - & + & -  \\
    + & - & +  \\
\end{bmatrix}
$$
which holds for higher dimension matrices too. 

We can now define the determinant as:
$$
\boxed{det \ A = a_{11}A_{11}+a_{12}A_{12}+\ldots+a_{1n}A_{1n}}
$$
where $A_{ij}$ is the Cofactor. But the determinant doesn't need to be obtained only by the first row, it can be obtained by expanding along any row or column. We could chose any particular row or column to expand on to find the determinant. 

An important thing to remember is that a triangle matrix's determinant is the multiplication of the diagonal. Also, remember that the determinant of a matrix with two equal rows is always $0$. 

Also, make sure you pay attention to 0s in the rows or columns. We can chose which column or row to expand, the ones with lots of 0's will make life A LOT easier. 

##### Calculating Inverse Matrix by Cofactor
We can actually calculate the [[Matrix Linear Algebra#Inverse Matrix|Inverse Matrix]] using cofactors and the [[Transpose]] :
$$
A^{-1} = \frac{[A_{ij}]^{T}}{|A|}
$$
where $A_{ij}$ is the cofactor and $[A_{ij}]$ is a matrix where each entry is the cofactor of that entry in the original matrix $A$. This is also sometimes written in terms of the Adjoint: 
$$
adj \ A = [A_{ij}]^{T}=[A_{ji}]
$$


### Determinants Properties Sheet
![[Determinants sheet.pdf]]
