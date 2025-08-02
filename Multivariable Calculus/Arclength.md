---
tags: Math, Multivariable, Integrals, Line_Integrals
dg-publish: true
mathLink: 
---
Subject: _Multivariable_
Main\_Topic: _Arclength_
Applications: _Distances_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
_
_

Arclength is the total length of an arc. How do we find such a value? Well, remember that speed is the magnitude of the velocity. Thus, if we parametrize a curve by $\vec{r}(t)$, then the velocity along that curve would be $\frac{d\vec{r}}{dt}$. Speed is denoted by $\frac{ds}{dt}$, where $ds$ is a differential, infinitesimal distance. Unlike velocity which works with displacement. 

So, we said speed is the magnitude of velocity, so 
$$
\frac{ds}{dt}= \left|\frac{d\vec{r}(t)}{dt} \right|  
$$
In other words:
$$
ds =  \left|\frac{d\vec{r}(t)}{dt} \right| dt
$$
If we integrate both sides we get:
$$
s = \int\limits_{a}^{b} \left|\frac{d\vec{r}(t)}{dt} \right| dt = \int\limits_{a}^{b}|\vec{v}| \ dt
$$
