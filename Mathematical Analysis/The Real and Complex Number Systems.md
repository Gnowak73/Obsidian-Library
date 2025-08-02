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

The real numbers are a fundamental part of mathematics. However, we must be careful with how we define a "real number" and how they are constructed. In analysis, we are mainly concerned with the properties of real numbers, rather than the methods used to construct them. Thus, naturally, we start with the axioms of real numbers:

**Axiom 1.**  $x+y=y+x,xy=yx$. Commutativity.
**Axiom 2.**  $x+(y+z)=(x+y)+z, x(yz)=(xy)z$. Associativity.
**Axiom 3.**  $x(y+z)=xy+xz$. The distributive law.

**Axiom 4.**  Given any two real numbers $x$ and $y$, there exists a real number $z$ such that $x+z=y$. $z$ is denoted $y-x$; the number $x-x$ is $0$. It can be proved that zero is independent of $x$. We write $-x$ for $0-x$. 

**Axiom 5.**  There exists at least one real number $x\neq 0$. If $x,y$ are two such real numbers, then there exists $z$ such that $xz=y$. $z$ is denoted $y/x$; the number $x/x$ is $1$ and can be proved independent of $x$. We write $x^{-1}$ for $1/x$ if $x\neq 0$. 

All traditional arithmetic laws can be derived by these axioms.

---
###### Ordering Properties
"$<$" established ordering among real numbers and follows some more axioms:

**Axiom 6.**  Exactly one relation: $x=y,x<y$, or $x>y$ holds. 
**Axiom 7.**  If $x<y$, then for every $z$, $x+z<y+z$.
**Axiom 8.**  If $x>0$ and $y>0$, then $xy>0$.
**Axiom 9.**  If $x>y$ and $y>z$, then $x>z$. 

From these axioms we can derive the usual rules for operating with inequalities. Note that the symbolism $x\leq y$ is used as an abbreviation for the statement $x<y$ or $x=y$. The same holds with $\geq$. 

---
###### Geometrical Representation of Real Numbers 
The real numbers can be represented geometrically as points on a line (the real axis). A point is selected to represent $0$ and another to represent $1$. This This determines the scale of the line. Each point corresponds to a real number and vise versa. 

###### Decimal Representation of Real Numbers
Every real number $x$ has a decimal expansion of the form 
$$
x=\pm N \cdot a_1a_{2\ldots}a_{n}\ldots
$$
where $N$ is either $0$ or a positive integer and each $a_i$ is one of the digits from $0$ to $9$. The notation $N \cdot a_{1}a_{2}\ldots a_{n}\ldots$ is really an abbreviation for the infinite series 
$$
N+a_{1}10^{-1} + a_{2}10^{-2} +\ldots + a_{n}10^{-n} + \ldots
$$
When $N$ is $0$ and all of the $a_i$ are equal, say to $a$, then the infinite series becomes a geometric series with the ratio $1/10$ and sum 
$$
a\left(\frac{\frac{1}{10}}{1-\frac{1}{10}}\right)=\frac{a}{9}.
$$
If $a=9$, then the series has the sum of $1$, which means that the number $1$ has two decimal expansions 
$$
1=1.000\ldots = 0.999\ldots
$$
More generally, if a number has a decimal expansion ending in zeros, then the number can also be written as a decimal expansion which ends in $9$'s by decreasing the last nonzero digit by one unit. For example, $1/8=0.125000\ldots=0.124999\ldots$  Except for situations like this, decimal expansions are unique. 

###### Rational Numbers 
Real numbers are classified into two types: the rational and the reals. Rational numbers are those real numbers which are the quotient of two integers. Irrational numbers are those real numbers which are not rational. Rational and irrational numbers can be distinguished by their decimal representations. A rational number has an expansion which eventually repeats itself. $1/2=0.5\underline{0},2/3=0.\underline{6},1/7=0.\underline{142857}$. The underline denotes the portion that is being repeated indefinitely. We may readily show that the decimal expansion of a rational number always repeats.

---
**Proof:**  Assume $x$ is rational. Then, 
$$
x = N + \frac{a_{1}}{10} + \frac{a_{2}}{10^{2}} + \ldots + \frac{a_{n}}{10^{n}} + \ldots
$$
We may write the truncated approximation
$$
x_{n} = N + \frac{a_{1}}{10} + \ldots + \frac{a_{n}}{10^{n}}.
$$
Each $x_n$ is a terminating decimal which we may write in the form $p_n/10^{n}$ for numerator $p$. The error, or remainder, is 
$$
r_n= x-x_{n}= \frac{a}{b} - \frac{p_{n}}{10^{n}} = \frac{10^{n} a - p_{n}b}{10^{n}b}.
$$
Let $q:= 10^{n}a-p_{n}b$. 
$$
r_n=\frac{q}{10^{n}b}.
$$
Note that $q$ is an integer and $0\leq r_{n} < \frac{1}{10^{n}}$. Thus, 
$$
0 \leq \frac{q}{10^{n}b} < \frac{1}{10^{n}} \rightarrow 0 \leq q < b
$$
which has a finite number of solutions $q \in \{0,1,2,\ldots,b-1\}$. Hence, as we generate a $q$ for every decimal place, then there must be some values which repeat. Now, let us look at some point where they repeat, so that $q_m=q_n$ for $m<n$. 
$$
r_{n} = \frac{q_{m}}{10^{n}b}, \quad x_{n}-x_{m}= \frac{q_{m}}{10^{n}b}\left(\frac{1}{10^{m}}-\frac{1}{10^{n}} \right).
$$
Thus, the tail end between two repeating numbers, also repeats. As eventually there is one repetition, then there will eventually be a tail end of the decimal expansion that always repeats.

---
Conversely, every repeating decimal represents a rational number. This fact is not so obvious, but it can easily be proved by observing that a decimal which repeats forms a geometric series
$$
a+b(1+r+r^{2}+\ldots+r^{n}+\ldots),
$$
where $a,b$, and $r$ are rational, $r$ being some power of $1/10$. Such a series has the sum $a+b/(1-r)$, which is rational. As a case in point, take the number $x=0.\underline{314}$. We can write the series as 
$$
x=\frac{3}{10} + 14(10)^{-3} + 14(10)^{-5} + 14(10)^{-7} + \ldots 
$$
$$
= \frac{3}{10} + 14 (10^{-3})[1+10^{-2} + 10^{-4} + \ldots]
$$
which equals 
$$
\frac{3}{10}+14(10^{-3})\left(\frac{1}{1-10^{2}}\right) = \frac{311}{990}.
$$


