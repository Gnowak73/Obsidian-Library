---
tags: 
dg-publish: true
mathLink: 
---
Subject: _None_
Main\_Topic: _None_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

###### The Euclidean Metric
A _metric_ on a set $X$ is a distance function, giving the distance $d(x,y)$ between two points $x,y \in X$. The familiar Euclidean distance formula between points in the plane $\mathbb{R}^{2}$ is the prototype of the metric, and the properties we expect from Euclidean distances are the basis for our definition of a metric. We will see that there are many other ways to measure distances between points in $\mathbb{R}^{2}$, and metrics may be applied to other sets outside of $\mathbb{R}^{n}$. 

```ad-Definition 
A _metric_ on a set $X$ is a function $d:X\times X \rightarrow \mathbb{R}$ satisfying
1. $d(x,y)\geq 0$ for all $x,y \in X$ (nonnegativity)
2. $d(x,y)=0$ if and only if $x=x$
3. $d(x,y)=d(y,x)$ for all $x,y \in X$ (symmetry)
4. $d(x,y)\leq d(x,z) + d(z,y)$ for all $x,y,z \in X$ (triangle inequality)
```

A **metric space** is a pair $(X,d)$ where $X$ is a set and $d$ is a metric on $X$. 

The first few conditions are pretty clear: distances can't be negative, two points are equal if and only if the distance between them is zero, and the distance between $x$ and $y$ is the same distance between $y$ and $x$. Since the shortest distance between two points in the Euclidean plane follows a straight line, $d(x,y)$ is less than or equal to the length of the polygonal path from $x$ to $z$ and on to $y$. Thus, the triangle inequality says that the length of one side of a triangle is less than or equal to the sum of the lengths of the other two sides. 

Vectors in $\mathbb{R}^{n}$ will be denoted by $x=(x_{1},x_{2},\ldots,x_{n})$. We are most familiar with the Euclidean metric $d:\mathbb{R}^{n}\times \mathbb{R}^{n} \rightarrow [0,\infty)$ given by
$$
d(x,y) = \sqrt{(x_{1}-y_{1})^{2}+(x_{2}-y_{2})^{2}+\ldots+(x_{n}-y_{n})^{2}}
$$
The sets $\mathbb{R}$ and $\mathbb{R}^{2}$ with the Euclidean metric are called the **Euclidean line**  and the **Euclidean plane**, and the space of $\mathbb{R}^{n}$ is the n-dimensional **Euclidean space**. 

If $d$ is a metric on $X$ and $Y \subseteq X$, then since $d$ tells us the distance between any two points in $X$, it tells us the distance between any two points in $Y \subseteq X$. It is easy to show that this inherited distance on $Y$ obeys all the conditions defining a metric. Formally, if $d:X \times X \rightarrow \mathbb{R}$ is a metric on $X$ and $Y \subseteq X$, then the restriction $d \left. \right|_{Y\times Y}$ of $d$ to $Y \times Y$ is a metric on $Y$. Thus we may speak of a subset $\mathbb{R}^{n}$ with the Euclidean metric.

A metric allows us to determine which points are near a given point $x$. This nearness can be characterized by the "balls" centered at $x$.

```ad-Definition
Suppose $(X,d)$ is a metric space. For $x\in X$ and $\epsilon>0$, the ball centered at $x$ with radius $\epsilon$, or simply the $\epsilon$-ball centered at $x$, is
$$
B(x,\epsilon) = \{y\in X: d(x,y)<\epsilon\}
$$
```

**Remark.**  Note that our definition of $B(x, \epsilon)$ requires that $\epsilon>0$. This convention guarantees that $x\in B(x,\epsilon)$, so every ball is nonempty. 

In the Euclidean line $\mathbb{R}$, the $\epsilon$-ball centered at $x$ consists of all points on the real line within $\epsilon$ of $x$, and thus $B(x,\epsilon)$ is the open interval $(x-\epsilon,x+\epsilon)$. In the Euclidean plane $\mathbb{R}^{2}$, the ball $B(x,\epsilon)$ is the disk centered at $x$. In $\mathbb{R}^{3}$ it is the sphere, and so on. 

Balls are used to define important concepts such as convergence of sequences and the continuity of functions. 

```ad-Definition
A _tail_ of sequnce $(x_{n})_{n\in \mathbb{N}}$ is a subsequence $(x_{n})_{n\geq k}$ obtained from the original by deleting the initial terms $x_{1},x_{2},\ldots,x_{k-1}$.
```

A sequence $(x_{n})_{n \in \mathbb{N}}$ is _eventually_ in a set $S$ if there exists an integer $k \in \mathbb{N}$ such that $x_{n}\in S$ for all $n\geq k$. That is, a sequence is eventually in $S$ if some tail of the sequence is contained in $S$. A sequence is _eventually constant_ if it is eventually in a singleton set $\{a\}$. A sequence is _frequently_ in a set $S$ if for any $k \in \mathbb{N}$, there exists $n>k$ such that $x_{n}\in S$. Clearly if a sequence is eventually in $S$ then it is also frequent in $S$.

```ad-Definition
A sequence $(x_{n})_{n \in \mathbb{N}}$ in a metric space $(X,d)$ _converges_ to $a \in X$ if for every $\epsilon>0$, $(x_{n})_{n\in \mathbb{N}}$ is eventually in $B(a,\epsilon)$. If $(x_{n})_{n\in \mathbb{N}}$ converges to $a$, we say $a$ is the limit of the sequene, and write $\lim_{n\rightarrow \infty}x_{n}=a$ or $x_{n}\rightarrow a$. 
```

Our next result is that a sequence in Euclidean space cannot converge to two different limits. Our familiarity with limits of sequences from calculus, which is based on the Euclidean metric, makes this result not surprising. The surprise will come later when we examine topological spaces in which a sequence might converge to more than one point.

**Theorem 1.1.6**  If a sequence $(x_{n})_{n\in \mathbb{N}}$ in a metric space $(X,d)$ converges, then the limit is _unique_. 

**Proof:**  Suppose that the sequence $(x_{n})_{n\in \mathbb{N}}$ does not converge to $b$. Since $b\neq a, \epsilon=\frac{1}{2}d(a,b)$ is greater than $0$. First, we will show that, $B(a,\epsilon)$ and $B(b,\epsilon)$ are disjoint. Suppose to the contrary that there exists $x\in B(a,\epsilon)\cap B(b,\epsilon)$. Then $d(a,x)<\epsilon$ and $d(x,b)<\epsilon$, and adding gives $d(a,x)+d(x,b)<2 \epsilon=d(a,b)$, contrary to the triangle inequality. So, $B(a,\epsilon)$ and $B(b,\epsilon)$ are disjoint.

![[Pasted image 20240826150125.png|center|400]]

Since $(x_{n})_{n\in \mathbb{N}}$ converges to $a$, it is eventually in $B(a,\epsilon)$, which is disjoint from $B(b,\epsilon)$. Thus, no tail of the sequence is in $B(b,\epsilon)$, so the sequence does not converge to $b$. $\square$ 

**Theorem 1.1.7**  If $(X,d)$ is a metric space, $x\in X$, and $y\in B(x,\epsilon)$, then there exists $\epsilon_{y}>0$ such that $B(y,\epsilon_{y})\subseteq B(x,\epsilon)$. 

**Proof:**  ![[Pasted image 20240826150217.png|center|400]]
Under the hypothesis, take $\epsilon_{y}=\epsilon-d(x,y)$. Since $y\in B(x,\epsilon),\epsilon_{y}>0$. Now $z\in B(y,\epsilon_{y})$ implies that $d(y,z)<\epsilon_{y}=\epsilon-d(x,y)$. Adding $d(x,y)$ to both sides of the equation and applying the triangle inequality, we have $d(x,z)\leq d(x,y)+d(y,z)<\epsilon$, so $z\in B(x,\epsilon)$. Since $z$ was an arbitrary point of $B(y,\epsilon_{y})$, we have $B(y,\epsilon_{y})\subseteq B(x,\epsilon)$. 

Now we present another metric on $\mathbb{R}^{2}$ to illustrate that, while our intuition from Euclidean geometry will often provide the correct motivation for metric arguments, we may need to be careful in the details. 

**Example**  Define $m:\mathbb{R}^{2}\times \mathbb{R}^{2}\rightarrow \mathbb{R}$ by 
$$
m((x_{1},y_{1}),(x_{2},y_{2}))= \sup \{|x_{1}-x_{2}|,|y_{1}-y_{2}|\}.
$$
Thus, the distance between two points in the plane is the larger of the horizontal distance $|x_{1}-x_{2}|$ separating them and the vertical distance $|y_{1}-y_{2}|$ separating them. The first three conditions for the metric are straight-forward to prove. The only difficulty may be the triangle inequality. Since the sup-metric is defined in terms of the Euclidean metric $d(x_{1},x_{2})=|x_{1}-x_{2}|$ on $\mathbb{R}$, it is not surprising that the triangle inequality for the sup-metric will be based on that for the Euclidean metric on $\mathbb{R}$. For any $x_{1},x_{2},x_{3},y_{1},y_{2},y_{3} \in \mathbb{R}$, we have 
$$
|x_{1}-x_{3}|\leq |x_{1}-x_{2}|+|x_{2}-x_{3}|
$$
$$
\leq \sup\{|x_{1}-x_{2}|,|y_{1}-y_{2}|\} + \sup\{|x_{2}-x_{3}|,|y_{2}-y_{3}|\}
$$
$$
= m((x_{1},y_{1}),(x_{2},y_{2}))+m((x_{2}y_{2}),(x_{3},y_{3}))
$$
Similarly, $|y_{1}-y_{3}|\leq m((x_{1},y_{1}),(x_{2},y_{2}))+m((x_{2},y_{2}),(x_{3},y_{3}))$, so $m((x_{1},y_{1}),(x_{3},y_{3}))=\sup\{|x_{1}-x_{3}|,|y_{1}-y_{3}|\}$ $\leq m((x_{1},y_{1}),(x_{2},y_{2}))+m((x_{2},y_{2}),(x_{3},y_{3})).$ This shows that $m$ satisfied the triangle inequality.

In $\mathbb{R}^{2}$ with the sup-metric, note that the ball $B((0,0),\epsilon)=\{(x,y)\in \mathbb{R}^{2}: \sup\{|x-0|,|y-0|\}=\sup\{|x|,|y|\}<\epsilon\}$, which is the set of all points in the plane such that the vertical distance $|y|$ and the horizontal distance $|x|$ from the origin are both less than $\epsilon$. This is a square $(-\epsilon,\epsilon)\times(-\epsilon,\epsilon).$ 

##### Open Sets in Metric Spaces
In the Euclidean line $\mathbb{R}$ familiar from calculus, and interval $(a,b)$ which contains neither of its endpoints is called an open interval and an interval $[a,b]$ that contains both of its endpoints is called a closed interval. Similarly, an open set in Euclidean space $\mathbb{R}^{n}$ is a set which contains none of its boundary points and a closed set is a set which contains all of its boundary points. 

![[Pasted image 20240826154130.png|center|400]]

```ad-Definition
Suppose $A$ is a subset of a metric space $(X,d)$. A **boundary point** of $A$ is a point $x\in X$ such that every ball around $x$ (with arbitrary radius $\epsilon>0$) intersects both $A$ and $X-A$. The set of all boundary points of $A$ is called the **boundary** of $A$ and is denoted $\partial A$.
```

We note that an immediate consequence of the definition is that $\partial A=\partial(X-A)$. Now we may formally define open and closed sets in metric spaces. 

```ad-Definition
A set $A$ in a metric space $(X,d)$ is _open_ (or, for emphasis $d$-open) if it contains none of its boundary points, and is _closed_ (or $d$-closed) if it contains all of its boundary points. 
```

In the case $d$ is the Euclidean metric on $\mathbb{R}^{n}$, $d$-open and $d$-closed sets may be called **Euclidean open** and **Euclidean closed**. 

The open and closed sets are fundamentally related by the following theorem. 

**Theorem 1.2.4.**  In a metric space $(X,d)$, $A$ is _open_ if and only if $X-A$ is closed; $A$ is closed if and only if $X-A$ is open.

**Proof:**  Recalling that the boundary of $A$ equals the boundary of its complement, $B$ is open if and only if $B \cap \partial B = \emptyset$, and $B$ is closed if and only if $\partial B \subseteq B$, we note the following equivalences in a metric space $X$: 
$$
\text{A is open} \iff A \cap \partial A = \emptyset
$$
$$
\iff \partial A \subseteq X-A
$$
$$
\iff \partial (X-A)\subseteq X-A
$$
$$
\iff X-A \ \text{is closed}
$$
Thus, $A$ is open if and only if its complement is closed. Replacing $A$ by $X-A$ shows that $A$ is closed if and only if its complement is open. 

We will focus on open sets for the rest of this section. The closed sets and open sets are the extremes: they contain either all or none of their boundary points. Most sets would fall somewhere between these extremes, including some but not all of their boundary points. that is, most sets would be neither open nor closed. In particular, notice that "not open" does not imply closed, and "not closed" does not imply open. A set can be simultaneously not open and not closed. 

**Theorem 1.2.5::**  $U$ is open in a metric space $(X,d)$ if and only if for every $x \in U$ there is a ball $B(x,\epsilon)$ contained in $U$. That is, $U$ is open if and only if 
$$
\forall x \in U, \exists \epsilon > 0  \quad \text{such that} \quad B(x,\epsilon) \subseteq U
$$

**Proof:**  ($\Rightarrow$) Suppose $U$ is open in $X$, Then 
$$
x\in U \Rightarrow x \notin \partial U
$$
$$
\Rightarrow \sim \text{(every ball around x intersects both $U$ and $X-U$)} 
$$
$$
\Rightarrow \text{there exists a $B(x,\epsilon)$ which does not intersect both $U$ and $X-U$}.
$$
$$
\Rightarrow \text{there exists a $B(x,\epsilon)$ which does not intersect $X-U$} \text{(since $x\in U$, every $B(x,\epsilon)$ must intersect $U$)}
$$
$$
\Rightarrow \text{there exists a $B(x,\epsilon) \subseteq U$}
$$
$(\Leftarrow)$ Suppose that for every $x \in U$ there exists $\epsilon_{x}>0$ such that $B(x,\epsilon_{x})\subseteq U$. Now for every $x\in U, B(x,\epsilon_{x})$ does not intersect $X-U$, so $x \notin \partial U$. Thus, $U$ contains none of its boundary points, so $U$ is open. $\square$ 

**Corollary 1.2.6**  In a metric space, every ball $B(x,\epsilon)$ is open. 

**Proof:**  Apply Theorems 1.2.5 and 1.1.7

**Corollary 1.2.7**  $U$ is open in a metric space $(X,d)$ if and only if $U$ is a union of balls. 

**Proof:**  By "union" we mean an arbitrary union, allowing unions of infinite collections, finite collections, or every the empty collection of balls. The union of an empty collection is $\emptyset$, so $U=\emptyset$ is a union of balls. 

If $U$ is a nonempty open set in $X$, by Theorem 1.2.5, for each $x\in U$, there exists $\epsilon_{x}$ with $\{x\}\subseteq B(x,\epsilon_{x})\subseteq U$. Taking the union over all $x \in U$ gives
$$
U = \bigcup_{x \in U} \{x\} \subseteq \bigcup_{x \in U}B(x,\epsilon_{x})\subseteq \bigcup_{c \in U} U = U
$$
and thus $U$ is a union $\cup_{x \in U}B(x,\epsilon_{x})$ of balls. Conversely, suppose $U$ is a union $\cup_{i \in I}B(x_{i},\epsilon_{i})$ of balls and $x \in U$. Then there exists $j \in I$ such that $x \in B(x_{j},\epsilon_{j})$. By theorem 1.1.7, there is a ball $B(x,\epsilon)$ centered at $x$ which is contained in $B(x_{j},\epsilon_{j}) \subseteq U$. Now by theorem 1.2.5, $U$ is open in $X$. 

```ad-Definition
An open neighborhood of $x$ is an open set containing $x$. A neighborhood of $x$ is any set which contains an open neighborhood of $x$. 
```

Some textbooks define all neighborhoods to be open. Because arbitrary neighborhoods of $x$ are defined in terms of open neighborhoods, in many applications this is adequate; there are enough open neighborhoods to define nearness. However, in applications involving nesting of neighborhoods and supersets of neighborhoods, the more general definition is helpful. 

The collection of all neighborhoods of $x$ will be used to quantify nearness to $x$. The nicest neighborhoods of $x$ in a metric space are the balls centered at $x$. Indeed, Theorem 1.2.5 shows that any neighborhoods of $x$ contains a ball centered at $x$. The definitions of boundary and sequential convergence given above in terms of balls can in fact be restated using "every neighborhood" instead of "every ball". So, even if we do not have a metric to generate balls, these concepts can be equally well utilized if we only know which sets are open, and consequently, which sets are neighborhoods of any given point. A _topology_ on a set $X$ will be a collection of subsets of $X$ which serve as the open sets. The theorem below lists fundamental properties of open sets in a metric space which we will wish any topology$-$that is, any collection of open sets$-$to satisfy. 

**Theorem 1.2.9.**  In a metric space $(X,d)$:
1. $\emptyset$ and $X$ are open
2. Finite intersections of open sets are open
3. Arbitrary unions of open sets are open

**Proof:**  $\emptyset$ and $X$ have no boundary points, and thus are open. Suppose $U_{1},U_{2},\ldots,U_{n}$ are open in $X$ and $x \in U_{1}\cap U_{2}\cap \ldots \cap U_{n}$. By Theorem 1.2.5, there exists $\epsilon_{1},\epsilon_{2},\ldots,\epsilon_{n}$ such that $B(x,\epsilon_{i})\subseteq U_{i}$ for $i=1,2,\ldots,n$. Take $\epsilon=\min\{\epsilon_{1},\epsilon_{2},\ldots,\epsilon_{n}\}$. Then $\epsilon>0$ and $B(x,\epsilon)\subseteq U_{1}\cap U_{2}\cap\ldots\cap U_{n}$. Thus, theorem 1.2.5 implies that $U_{1}\cap\ldots\cap U_{n}$ is open. By Corollary 1.2.7, a union of open sets in $X$ is a union of union of balls, which is again a union of balls, and is thus open. 

Note that arbitrary intersections of open sets need not be open: If $U_{n}=(0,1+\frac{1}{n})$ in the Euclidean line $\mathbb{R}$, then $U_{n}$ is open for each $n \in \mathbb{N}$, but the intersection $\cap_{n \in \mathbb{N}}U_{n}=(0,1]$ is not open.

### Topologies 
In a metric space, open sets were defined in terms of boundaries of sets, which were defined in terms of $\epsilon$-balls, which were defined using distance functions. Thus, open sets were defined in terms of the distance function. But there are ways to define nearness$-$which is the general goal of topology$-$which cannot be measured by a metric. All that is needed is a suitable collection of open sets. The open sets may then be used to define neighborhoods, convergence, and continuity, among other topological concepts. The characteristic properties of open sets allowing the quantification of nearness are those given for open sets in a metric space in **Theorem 1.2.9**. This is the basis for the definition below:

```ad-Definition
A _topology_ on a nonempty set $X$ is a collection $T$ of subsets of $X$, called the _open_ sets, satisfying:
1. $\emptyset \in \tau$ and $X \in \tau$
2. If $U_1,U_2,\ldots,U_{n}\in\tau$, then $\cap^{n}_{i=1} U_{i}\in \tau$($\tau$ is closed under finite intersections).
3. If $I$ is an arbitrary index set and $U_{I}\in \tau$ for all $i \in I$, then $\cup_{i\in I}U_{i}\in \tau$ ($\tau$ is closed under arbitrary unions).
```

A **topological space** is a pair $(X,\tau)$ where $X$ is a nonempty set and $\tau$ is a topology on $X$.

If the topology $\tau$ is understood, we may refer to "the topological space $X$" just naming the underlying set of the topological space $(X,\tau)$. If we wish the emphasize the topology, an element of a topology $\tau$ may be called a $\tau$-open set. 

The condition (2) that a topology must be closed under finite intersections can be replaced by another condition: that if $U_{1},U_{2},\in \tau$, then $U_{1}\cap U_{2} \in \tau$ (that is, $\tau$ is closed under _binary intersections_). Clearly (2) implies this new condition, and we can prove that this holds conversely using induction. 

If $(X,d)$ is a metric space, then the collection of $d$-open sets is a topology on $X$ called the **metric topology generated by $d.$**
 In the special case of $\mathbb{R}^{n}$ with the Euclidean metric, the resulting topology is the **Euclidean topology** $\tau_{\epsilon}$, and ($\mathbb{R}^{n},\tau$) is called the $n$-dimensional Euclidean space. 
While a metric on $X$ gave use one way to generate open sets, the concept of a topology is that we start by specifying the open sets and use them to characterize nearness, convergence, and continuity. Metric spaces are concrete examples of topological spaces, which are easy to visualize, but not every topological space is a metric space.

We note that the open sets in a metric space were all generated by a nicer collection of open sets, the balls, in the sense that every open set was a union of balls. Such a collection of open sets will be called a _basis_ for the topology. Bases will be studied later on. 

Now, we will give the natural extensions of some metric space concepts to topological spaces. 

```ad-Definition
If $(X,\tau)$ is a topological space and $x \in X$, an _open neighborhood of $x$_ is an open set containing $x$. A _neighborhood_ of $x$ is a set containing an open neighborhood of $x$. 
```

To emphasize the topology, a neighborhood of $x$ in $(X,\tau)$ may be called a $\tau$-neighborhood of $x$. (As noted earlier, some elementary textbooks initially require all neighborhoods to be open, which is adequate for an elementary development). 

Our previous definition of convergence of a sequence in a metric space carries over easily to convergence in an arbitrary topological space.

```ad-Definition
A sequence $(x_{n})_{n\in \mathbb{N}}$ in a topological space $X$ _converges_ to $a \in X$ if and only if $(x_{n})_{n \in \mathbb{N}}$ is eventually in every neighborhood of $a$. That is, $\lim_{n\rightarrow \infty} x_{n}=a$ if and only if for any neighborhood $U$ of $x$, there exists $k \in \mathbb{N}$ such that $n\geq k$ implies $x_{n}\in U$.
```

Checking sequential convergence to a point $a$ required checking something for every neighborhood of $a$, with the idea that as the neighborhoods get "smaller and smaller" the sequence still eventually gets in the neighborhoods. The formal way to quantify the "smaller and smaller" concept is to require the condition to hold for every possible neighborhood. 

We note that "every neighborhood" in our definition can be replaced by "every open neighborhood." Clearly if $(x_{n})_{n \in \mathbb{N}}$ is in every neighborhood of $a$, then it is in every open neighborhood of $a$. Conversely, since every neighborhood of $a$ contains an open neighborhood of $a$, if $(x_{n})_{n \in \mathbb{N}}$ is in every open neighborhood of $a$, it must be in every neighborhood of $a$. 

We shall give some examples to illustrate some topologies and how they may be used to quantify nearness. 

**Example:**  (The discrete topology). If $X$ is a nonempty set, the discrete topology on $X$ is $\tau_{D}=P(X) = \{U:U \subseteq X\}$. Every subset of $X$ is open in the discrete topology (so it is easily confirmed that $\tau_D$ is in fact a topology). Any topology is a collection of subsets of $X$; the discrete topology is the collection of all subsets of $X$ and is this the largest possible topology on $X$. In the discrete topology, each singleton set $\{\}$ is open and is therefore a neighborhood of $x$. This suggests that $x$ is not near any other points. If a sequence converges to $a$, then the sequence is eventually in every neighborhood of $a$, and thus is eventually in the neighborhood $\{a\}$. Thus, the only convergence sequences are those which are eventually constant. 

The discrete topology models discrete situations. To model the Euclidean plane by a finite set of pixels on a screen, we might stipulate that an open set in the plane should illuminate an open set of pixels. If the point $(0,0)$ is centered in a pixel occupying region of a square $[-r,r]\times[-r,r]$, then the open Euclidean ball $B((0,0),r)$ is contained in the square and thus would illuminate the single pixel, so this single pixel should be open. Similarly, every pixel should be open, and we have the discrete topology on the set of pixels. This natural model is in many ways inadequate. A better way to model pixels should incorporate the boundaries between pixels. 

the discrete topology is _metrizable_, that is, it arises as the metric topology for some metric on $X$. Indeed, there are many metrics which generate the discrete topology. The most common one is the _discrete metric_:
$$
d(x,y) = \begin{cases}0, \quad x=y \\ 1, \quad x\neq y\end{cases}$$
The discrete metric is used in instances where exact prevision is needed. 

**Example**  (The indiscrete topology). The indiscrete topology on $X$ is $\tau_{I}=\{\emptyset, X\}$. Thus, the only open sets in the indiscrete topology are those required by the definition of a topology. If $x \in X$, the only neighborhood of $x$ is the whole space $X$. Every point $x$ is closed to every other point in the space. In the indiscrete topology on $\mathbb{R}$, we see that every sequence converges to every point $a\in\mathbb{R}$. Thus, convergence is not unique and thus this topology is not metrizable (convergence in a metric space must be unique).

**Remark.*** The discrete topology and indiscrete topology are the extremes. In the discrete topology, every set is open. In the indiscrete topology, every point is close to every other. 

We will see that some topologies result in sequences that have more than one limit. Recall that the crucial property which prevented a sequence in a metric space from converging to distinct points $a$ and $b$ was that $a$ and $b$ had disjoint neighborhoods. To ensure that no sequence ever has two distinct limits, we could impose the condition that every pair of distinct points $a$ and $b$ possess disjoint neighborhoods, that is, every pair of distinct points $a$ and $b$ are "separated" by disjoint neighborhoods. This separation property is named for Felix Hausdorff. It is also called the $T_{2}$ property, or "separation axiom 2. 

```ad-Definition
A topological space $(X,\tau)$ satisfies the Hausdorff property if for every $a,b\in X$ with $a\neq b$, there exists $N_{a},N_{b} \in \tau$ with $a\in N_{a}, b\in B_{b}$, and $N_{a}\cap N_{b}=\emptyset$. If $X$ satisfies the Hausdorff property, we say $X$ is a Hausdorff space, or a $T_{2}$ space. 
```

We have already noted the first benefit of this property. 

**Theorem 1.3.9.**  If $(X,\tau)$ is a Hausdorff topological space, then every convergent sequence in $X$ has a unique limit. 

