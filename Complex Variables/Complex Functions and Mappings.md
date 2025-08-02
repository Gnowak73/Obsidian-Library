---
tags: Math, domain, domain_of_definition, function, complex image, range, domain
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Complex Functions and Mappings_
Applications: _Complex Functions, Mappings, Condition for many Complex Theorems_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_ 

Let $S$ be a set of complex numbers. A _function_ $f$ defined on $S$ is a rule that assigns to each $z$ in $S$ a complex number $w$. The number $w$ if called the **Value** of $f$ at $z$ and the set $S$ is called the **Domain of Definition**. Both a rule and a domain of definition are needed in order for a function to be well defined. 

**Remark.** Although the domain of definition is often a domain as defined in [[Regions in the Complex Plane]], it need not be. 

Each function $f(z)$ can be expressed by 
$$
f(z) = u(x,y)+iv(x,y).
$$
We typically use the definitions 
$$
x=\frac{z+\overline{z}}{2}, \quad y=\frac{z-\overline{z}}{2i}
$$
to write functions in terms of $x,y$ or in terms of $z, \overline{z}$.

```ad-Definition
The _image_ of a point $z$ in the domain of definition $S$ is the point $w=f(z)$. The _inverse image_ of a point $w$ is the set of all points $z$ in the domain of definition of $f$ that have $w$ as their image. The image of the entire domain of definition $S$ is called the _Range_. 
```
Some functions may me many-valued, we try to restrict these functions and their domains in order to splice them into groups of single-valued functions, this is known as using **branch cuts** and **branches** ([[Complex Elementary Functions]]). 

```ad-Definition
A **Piecewise Continuous** function is a function that has a finite number of discontinuities between segments, such that the function is continuous along each one of these segments and **the left and right hand limits ARE FINITE**. 

For an interval extending to the infinities, a function is piecewise continuous if it is piecewise continuous in every closed interval $[a,b]$ such that $[a,b]\subset (-\infty,\infty)$
```

