---
tags: Linear, linear_algebra, matrices, group, O(3), rotation, group_rotation, rotation_group, orthogonal, orthonormal, matrix, Math
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Orthogonal Matrices and O(3) group_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

An orthogonal, or orthonormal matrix, is a square matrix made of orthonormal vectors such that 
$$
A^{T}=A^{-1}
$$
**Proof:**  If the vectors in the matrix are orthonormal, then if $v_{i}$ are column vectors, $v_{i}^{T}v^{j}=\delta^{i}_{j}$. Then, we can show that $AA^{T}=I$ since the vector multiplication would become the inner Euclidean space product between each matrix. Now, since the vectors are orthonormal, they must be linearly independent. Thus, we know that the inverse $A^{-1}$ **must exist** (is well defined, see [[Nonsingular Matrix]] and [[linear independence]] for details). 

Since $AA^{T}=I$, we can write $(A^{T}A)A^{-1}=IA^{-1}=A^{-1}$. Since square matrix multiplication is associative, we have $(A^{T}A)A^{-1}=A^{T}(AA^{-1})=A^{T}$. Thus, we have $A^{-1}=A^{T}$. 

---
Now, another important property of these matrices is that the determinant is either $+1$ or $-1$. 

**Proof:**  We take that $A^{-1}=A^{T}$ and using properties in [[Determinants sheet.pdf]], we can see that $\det(I)=1=\det(A)\det(A^{-1})=\det(A)\det(A^{T})=\det(A)\det(A)=\det(A)^{2}$. Thus, the determinant must be $\pm 1$. 

The determinant $\pm 1$ determines the orientation if $A$ is a transformation. For rotational transformations, using either $\pm 1$, which is all proper or improper rotations, is called the O group. If we only use the positively oriented transformations, such as when we want to rotate about a point, we also have the SO group, where the "S" stands for "special". 