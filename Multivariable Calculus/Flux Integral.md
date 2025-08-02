---
tags: Math, Multivariable, theorem, Integrals, Line_Integrals, Surface_Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Flux Integrals_
Applications: _Flux_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Surface Integral]],[[Surface Area Integrals]], [[Line Integrals#Theorems|Line Integral Theorems]]_
_
_

**Remark.** These integrals can also be used with the [[Line Integrals#Theorems|Line Integral Theorems]].

An integral finding the flux through a surface, denoted:
$$
Flux = \int\int \vec{F} \cdot d\vec{A} = \int\int \vec{F} \cdot \vec{N} \ dS
$$
where $\vec{N}$ is the normal vector to the surface. We want to find a coordinate system such that $\vec N$ or $\hat N$.

#### Parametric
Lets say we have a Parametric way to represent our surface:
$r(u,v)=f(u,v)\hat i + g(u,v) \hat j +h(u,v) \hat k$. We know that the unit normal is going to be $\hat N = \frac{\vec{r}_{u}\times \vec{r}_{v}}{|\vec{r}_{u} \times \vec{r}_{v}|}$, and we remember from [[Surface Area Integrals#Parametric Surface]] that we can represent this infinitesimal area as $d\sigma = |\vec{r}_{u}\times \vec{r}_{v}|dudv$. Plugging all of this in, we get
$$
Flux = \int\int_{S}\vec{F}\cdot \frac{\vec{r}_{u}\times \vec{r}_{v}}{|\vec{r}_{u} \times \vec{r}_{v}|} |\vec{r}_{u} \times \vec{r}_{v}|\ dudv = \int\int_{S}\vec{F} \cdot (\vec{r}_{u}\times\vec{r}_{v}) \ dudv
$$

#### Implicit 
If we have a surface $g(x,y,z)=C$, we know that the gradient vector $\nabla g$ is always normal to the implicit surface $g = C$. Thus, our normal vector will be $\hat N = \frac{\nabla g}{|\nabla g|}$. We also know one again from [[Surface Area Integrals]] that $d\sigma = \frac{|\nabla g|}{|\nabla g \cdot \vec{p}|} \ dudv$. Plugging all of this in:
$$
Flux = \int\int_{S}\vec{F} \cdot \frac{\nabla g}{|\nabla g|} \frac{|\nabla g|}{|\nabla g \cdot \vec{p}|}\ dudv = \int\int_{S}\vec{F} \cdot \frac{\nabla g}{|\nabla g \cdot \vec{p}|} \ dudv  
$$