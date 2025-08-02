---
tags: Math, Complex, Plane, Neighborhood, Interior, Exterior, Set, Limit_Point, Accumulation
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Regions in the Complex Plane_
Applications: _Sets in the Complex Plane, Domains, Regions, Neighborhoods_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_
We are concerned with sets of complex numbers, or points in the $z$ plane, and their closeness to one another. Our basic tool is the concept of an $\epsilon$ neighborhood:
$$
|z-z_{0}|<\epsilon
$$
of a given point $z_{0}$. It consists of all points $z$ lying inside but not on a circle, centered at $z_{0}$. 

![[Pasted image 20230703150615.png|center]]

We can express what we call a **deleted neighborhood**, or a punctured disk,
$$
0<|z-z_{0}|<\epsilon
$$
consisting of all points $z$ in an $\epsilon$ neighborhood of $z_{0}$ except for the point $z_{0}$ itself. 


```ad-Definition
A point $z_{0}$ is an _Interior Point_ of a set $S$ whenever there is some neighborhood of $z_{0}$ that contains only points of $S$.

It is called an _Exterior Point_ of $S$ when there exists a neighborhood of it containing no points of $S$. 

A _Boundary Point_ is, therefore, a point all of whose neighborhoods contain at least one point in $S$ and at least one point not in $S$. The totality of all boundary points is the _Boundary_ of $S$.

A set is _Open_ if it does not contian any of its boundary points. 

A set is _Closed_ if it contains all of its boundary points. 

The _Closure_ of a set $S$ is the _Closed Set_ consisting of all points in $S$ together **with** the _Boundary_ of $S$

An _Open_ set $S$ is _Connected_ if each pair of points in it can be joined by a **Polygonal Line**, consisting of a finite number of segments, joined end to end, that lies entirely in $S$

A _nonempty open set_ that is _connected_ is called a **Domain**

A domain together with some, none, or all of its boundary points is a _Region_ 

A set $S$ is _Bounded_ if every point in $S$ lies inside some circle $|z|=R$; otherwise, it is _unbounded_.

A point $z_{0}$ is an _Accumulation Point_, or _limit point_, of a set $S$ if each deleted neighborhood of $z_{0}$ contains **at least one point** of $S$. 
``` 

**Remark.** A closed set contains all of its Accumulation Points. And any neighborhood is a domain. 

With limit points, for example, the set $(0,2)$ has a limit point at 0. Even in $0$ is not in the set, every neighborhood around zero will have a number in the set $(0,2)$: the numbers $.1,.01,.001,.0001,\ldots$ and so on. 