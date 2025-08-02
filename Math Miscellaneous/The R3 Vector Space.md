---
tags: Math, Linear_Algebra, Vectors
dg-publish: true
mathLink: The $R^{3}$ Vector Space
---
Subject: _Linear Algebra_
Main\_Topic: _$R^{3}$ Vector Space_
Applications: _Linear Systems, ODE, PDE, Euclidean Geometry_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
The $R^{3}$ vector space is a [[Vector Space]] constituting of pairs of real numbers $(a,b,c)$. 

#### Linearly Independent Vectors
The vectors $u,v,w$ are [[linear independence|linearly independent]] if and only if 
$$
\begin{vmatrix}u_{1}&v_{1}&w_{1}\\u_{2}&v_{2}&w_{2}\\u_{3}&v_{3}&w_{3}\end{vmatrix} \neq 0
$$
This is because by the definition of [[linear independence]], these vectors must only have the trivial solution to 
$$
au+bv+cw=0
$$
which we can write as a Linear System of equations in the form $Ax=0$. Thus, if the [[Determinant]] is not $0$, there is a unique solution to this equation (from [[Matrix Linear Algebra#Inverse Matrix]]), which would be $x=0$. If not, then this system either has infinite solutions or no solutions. 

#### Any set of 3 Linearly Independent Vectors is a Basis in $R^{3}$ 
If three vectors are linearly independent in $R^{3}$, they create a basis in $R^{3}$. This is because if we have an arbitrary vector $t$ such that
$$
t=au+bc+cw
$$
this equation has a specific, unique solution if the determinant of $u,v, w$ is not equal to $0$, as stated in [[#Linearly Independent Vectors]]. Thus, since a non-zero determinant is needed to solve this equation (proving that these vectors are a basis in $R^{3}$) for a unique solution, this implies that $u, v, w$ are linearly independent. 
