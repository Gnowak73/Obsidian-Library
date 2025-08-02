---
tags: Math, PDE, map, General_methods, PDEs, theorems, equations
dg-publish: true
mathLink: 
---
Subject: _PDE_
Main\_Topic: _PDE General Methods_
Applications: _Solving PDEs_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[TEXTBOOK MATH 430 PARTIAL DIFFERENTIAL EQUATIONS.pdf|PDE Textbook]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
This article is a short summary/map of content on the different general methods prescribed to solve PDEs. 

```ad-note
[[Superposition Linear ODE and PDE|Superposition]] is automatically taken into account for the [[Method of Characteristics (PDE)]] and [[Fourier Transform|Fourier Transforms]].

[[Separation of Variables (PDE technique)|Separation of Variables]] does not automatically take into consideration _superposition_ but can be used to create a general solution by doing the infinite sum for each particular solution (as long as boundary conditions are satisfied for any sum of solutions -- check homogeneity!).

If we also try to factor like in [[Wave Equation D'Alambert]] or we use [[Duhamel's Principle]], remember that _superposition_ is not automatically taken into account. Especially for [[Duhamel's Principle]]! The result from [[Duhamel's Principle]] must be added to the homogeneous solution!
```

**Remark.**  Always take into account [[Superposition Linear ODE and PDE]] when first looking at you PDE.

###### First Order PDEs
1. [[Method of Characteristics (PDE)]]: Covers every linear, nonlinear, quasilinear, semilinear PDE. 

###### Second Order PDE
1. [[Separation of Variables (PDE technique)]]: Covers linear second order PDEs. 
2. [[Wave Equation D'Alambert]]: An Example of using factoring to solve PDEs and creating general solutions based off of [[Superposition Linear ODE and PDE|superposition]] of these linear PDE factors. 
3. [[Duhamel's Principle]]: A technique to solve inhomogeneous PDEs, specifically the wave equation and heat equation.

###### Everything
1. [[Fourier Transform]]: The Fourier Transform is a general method for any order PDE you are given. 
2. Try to cast it in the complex plane like in [[Projectiles and Charged Particles]]. 