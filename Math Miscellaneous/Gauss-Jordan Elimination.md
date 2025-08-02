---
tags: Math, Linear_Algebra, technique
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Gauss-Jordan Elimination_
Applications: _Solving Matrix Equations, Matrix Manipulation_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
Gauss-Jordan Elimination is a method in order to reduce matrices, putting linear systems in equivalent forms. Its the same as manipulating linear systems of equations but just in matrix form (which is much easier to handle and deal with). 

Algorithm:
1. Transform $\pmb{A}$ into echelon form by Gaussian elimination
2. Divide each element of each nonzero row by the leading entry
3. Use each leading 1 to "clear out" any remaining non=zero elements

There rules are based upon linear operations:
1. You can multiply rows by constants
2. You can add rows together
3. You can swap rows 

For example, say we have the matrix equation 
$$
\begin{bmatrix} 1&1&1&1&|12 \\1&2&0&5&|17\\3&2&4&-1&|31 \end{bmatrix}
$$
which represents the a system of linear equations where we have 4 variables of $x$. If we make the following operations to put it into [[Reduced Row Echelon Form]]:
1. $R_{2}\rightarrow (-1)R_{1}+R_{2}$ 
2. $R_{3}\rightarrow (-3)R_{1}+R_{3}$
3. $R_{3}\rightarrow (1)R_{1}+R_{3}$
4. $R_{1}\rightarrow (-1)R_{2}+R_{1}$

then we end up with
$$
\begin{bmatrix} 1&0&2&-3&|7\\0&1&-1&4&|5\\0&0&0&0&|0 \end{bmatrix}
$$
We can easily deduce that $x_{3}$ and $x_{4}$ are arbitrary since they do not have any leading coefficients in the RRE matrix. 