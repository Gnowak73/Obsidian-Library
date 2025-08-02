---
tags: Math, ODE, PDE, Superposition
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _Superposition_
Applications: _Solution Spaces, Functional Linear Algebra, ODEs, PDEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_
This article will be generalized for PDEs but as we know, ODEs are just specific cases of PDEs, so it can be easily extended to such cases. 

If we have a PDE or an ODE of the form $\mathcal{L}(u)=0$ with two solutions $u_{1}$ and $u_{2}$ then for the constants $a,b \in \mathbb{R}$, then $au_{1}+bu_{1}$ is also a solution to $\mathcal{L}(u)=0.$ 

This can also be applied to inhomogeneous linear PDEs in the form $\mathcal{L}(u)=f$. If $u_{1}$ is a solution to the inhomogeneous linear PDE and $u_{2}$ is any solution to the associated homogenous PDE $\mathcal{L}(u)=0$, then $u_{1}+u_{2}$ is also a solution to the inhomogeneous linear PDE.

More generally, if $u_{1}$ is a solution to $\mathcal{L}(u)=f_{1}$ and $u_{2}$ is a solution to $\mathcal{L}(u)=f_{2}$, then $au_{1}+bu_{2}$ is a solution to $\mathcal{L}(u)=af_{1}+bf_{2}.$ 

###### Solution Space
If we have a family or group of solutions to a PDE or ODE that are linearly independent, then due to Superposition, we should be able to write a general solution as a sum of these linearly independent solutions. Since the sum of these solutions must span an entire possible set of solutions, we can create a [[Function Linear Algebra#Basis Algebra|Basis]]  for the solutions, known as a solution space. 