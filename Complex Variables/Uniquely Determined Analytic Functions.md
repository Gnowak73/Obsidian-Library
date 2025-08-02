---
tags: analytic, Math, analytic_functions, complex, subdomain, domain, correspondence, theorem, line_segment, continuation, analytic_continuation
dg-publish: true
mathLink: 
---
Subject: _Complex Analysis_
Main\_Topic: _Uniquely Determined Analytic Functions_
Applications: _How the values of analytic functions in a domain D are affected by a subdomain of D or a line segment dying in D_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Complex Variables Textbook.pdf]]_
Closely\_Related\_To: _[[Analytic Functions]],[[Regions in the Complex Plane]]_
Cont.\_ of: _None_ 
_
_
**Lemma.**  Suppose that 
a) a function $f$ is analytic throughout a domain $D$
b) $f(z)=0$ at each point $z$ of a domain or line segment contained in $D$

Then $f(z)\equiv0$ in $D$; that is, $f(z)$ is identically equal to zero throughout $D$.

**Proof:**  To prove this lemma, we let $f$ be as states in its hypothesis and let $z_{0}$ be any point of the subdomain or line segment where $f(z)=0$. Since $D$ is a _connected_ open set ([[Regions in the Complex Plane]]), there is a polygonal line $L$, consisting of a finite number of line segments joined end to end and lying entirely in $D$, that extends from $z_{0}$ to any other point $P$ in $D$. We let $d$ be the shortest distance from points on $L$ to the boundary of  $D$, unless $D$ is the entire plane; in that case, $d$ may be a positive number. We then form a finite sequence of points
$$
z_{0},z_{1},z_{2},\ldots,z_{n-1},z_{n}
$$
along $L$, where the point $z_{n}$ coincides with $P$, and where each point is sufficiently close to adjacent ones that 
$$
|z_{k}-z_{k-1}|<d
$$
Finally, we construct a finite sequence of neighborhoods 
$$
N_{0},N_{1},N_{2},\ldots ,N_{n-1},N_{n},
$$
where each neighborhood $N_{k}$ is centered at $z_{k}$ and has radius $d$. Note that these neighborhoods are all contained in $D$ and that the center $z_{k}$ of any neighborhood $n_{k}$ $N_{k}$ lies in the preceding neighborhood $N_{k-1}$. 

![[Pasted image 20230704154427.png|center]]

Since $f$ is analytic in $N_{0}$ and since $f(z)=0$ in a domain or one a line segment containing $z_{0}$, then $f(z)\equiv0$ in $N_{0}$ (Proof in <mark style="background: #D2B3FFA6;">Thm. 3 Sec. 82.</mark> of [[Complex Variables Textbook.pdf]], which is also in [[Zeros of Analytic Functions#Not all Isolated Zeros]]). But the point $z_{1}$ lies in $N_{0}$. Hence a second application of the same theorem reveals that $f(z)\equiv 0$ in $N_{1}$ and so on until we get to $N_{k}$. And since $P$ is arbitrarily chosen, then we can cover the entire domain. Thus, in the entire domain, $f(z)\equiv 0$.

Now, suppose that two functions $f$ and $g$ are analytic in the same domain $D$ and that $f(z)=g(z)$ at each point $z$ of some domain or line segment contained in $D$. The difference 
$$
h(z)=f(z)-g(z)
$$
is also analytic in $D$, and $h(z)=0$ throughout the subdomain or along the line segment. According to the lemma, then, $h(z)\equiv 0$ throughout $D$; that is, $f(z)=g(z)$ at each point in $D$. We thus arrive at the following important theorem: 

---
**Theorem.**  A function that is analytic in a domain $D$ is uniquely determined over $D$ by its values in a domain, or along a line segment, contained in $D$.

---
A more general result is sometimes called the _coincidence principle_, is straightforward to prove. Namely, if two functions $f$ and $g$ are analytic in the same domain $D$ and if $f(z)=g(z)$ on a subset of $D$ that has a limit point ([[Regions in the Complex Plane]]) $z_{0}$ in $D$, then $f(z)=g(z)$ everywhere in $D$. 

##### Analytic Continuation
This theorem is useful in studying the question of extending the domain of definition of an analytic function. More precisely, given two domains $D_{1}$ and $D_{2}$, consider the _intersection_ $D_{1} \cap D_{2}$, consisting of all points that lie in both $D_{1}$ and $D_{2}$. If $D_{1}$ and $D_{2}$ have points in common and a function $f_{1}$ is analytic in $D_{1}$, there _may_ exist a function $f_{2}$, which is analytic in $D_{2}$, such that $f_{2}(z)=f_{1}(z)$ for each $z$ in the intersection $D_{1}\cap D_{2}$. If so, we call $f_{2}$ an **Analytic Continuation** of $f_{1}$ into the second domain $D_{2}$. 

![[Pasted image 20230704161638.png|center]]

Whenever that analytic continuation exists, it is unique, according to the theorem just proved. That is, not more than one function can be analytic in $D_{2}$ and assume the value $f_{1}(z)$ at each point $z$ of the domain $D_{1}\cap D_{2}$ interior to $D_{2}$. However, if there is an analytic continuation $f_{3}$ of $f_{2}$ from $D_{2}$ into a domain $D_{3}$ which intersects $D_{1}$. it is not necessarily true that $f_{3}(z)=f_{1}(z)$ for each $z$ in $D_{1}\cap D_{3}$. 

```ad-Definition
If $f_{2}$ is the analytic continuation of $f_{1}$ from a domain $D_{1}$ into a domain $D_{2}$, then the function $F$ defined by means of the equations 
$$
F(z) = \cases{ f_{1}(z) \quad \text{when $z$ is in $D_{1}$}, 
\\ f_{2}(z) \quad \text{when $z$ is in $D_{2}$}.  }
$$
is analytic in the _union_ $D_{1}\cup D_{2}$, which is the domain consisting of all points that lie in either $D_1$ or $D_{2}$. The function $F$ is the analytic continuation into $D_{1}\cup D_{2}$ or either $f_{1}$ or $f_{2}$; and $f_{1}$ and $f_{2}$ are called _elements_ of $F$.
```

##### The Reflection Principle
**Theorem.**  Suppose that a function $f$ is analytic in some domain $D$ which contains a segment of the $x$ axis and whose lower half is the reflection of the upper half with respect to that axis. Then
$$
\overline{f(z)} = f(\overline{z})
$$
for each point $z$ in the domain if and only if $f(z)$ is real for each point $x$ on the segment. 