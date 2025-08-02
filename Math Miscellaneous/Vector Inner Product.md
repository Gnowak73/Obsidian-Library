---
tags: Math, Linear_Algebra, Inner Product 
dg-publish: true
mathLink: 
---
Subject: _Linear Algebra_
Main\_Topic: _Vector Inner Product_
Applications: _Distances, Geometry, [[Vector Space]]_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Vector Linear Algebra]]_
_
_

An inner product associated vectors with a distance. More specifically, an inner product on a vector space $V$ is a function that associated with each part of vectors $u$ and $v$ in $V$ a scalar $\left<u,v\right>$ such that, if $u,v,w$, are vectors and $c$ is a scalar, then
1. $\left<u,v \right>= \left<v,u \right>$
2. $\left<u,v+w \right> = \left<u,v \right>+\left<u,w \right>$ 
3. $\left<cu,v \right> = c \left<u,v \right>$
4. $\left<u,v \right>\geq 0$; $\left< u,u \right>=0$ if and only if $u=0$

For Euclidean space, this is 
$$
u\cdot v = \left< u,v \right>=u^{T}v
$$
where the length $|u|$ is defined as 
$$
|u|^{2}= \left<u,u \right>
$$

### Cauchy-Schwarz Inequality (Euclidean Space)
if $u$ and $v$ are vectors in $R^{n}$ , then 
$$
|u\cdot v|\leq |u||v|
$$
