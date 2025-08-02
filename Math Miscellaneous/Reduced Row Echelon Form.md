---
tags: Math, Linear_Algebra
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Reduced Row Echelon Form_
Applications: _Linear Systems, Matrices_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
Reduced Row echelon form is a form in which a matrix has the following properties:
1. Each leading entry is $1$
2. Each leading entry is the only nonzero element in its column 
3. Every all-zero row lies beneath every row that contains a nonzero element
4. the leading nonzero entry in each row lies to the right of the leading nonzero entry in the preceding row

An <mark style="background: #D2B3FFA6;">Echelon Matrix</mark> only has properties 3 and 4. 

For example:
$$
\begin{bmatrix} 1&0&-3&0\\0&1&4&0\\0&0&0&1 \end{bmatrix}
$$
is a RRE (Reduced-Row-Echelon) matrix. Each RRE matrix is completely unique, thus provides importance in solving specific linear systems (since each different linear system would have a different RRE form)

The [[Gauss-Jordan Elimination]] method is typically used to find these matrices. 