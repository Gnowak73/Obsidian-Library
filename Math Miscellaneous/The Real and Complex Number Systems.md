---
tags:
  - Math
  - Real
  - Real_analysis
  - complex_plane
  - Analysis
  - Set
  - field
  - ordered
  - sup
  - inf
  - archimedian
dg-publish: true
mathLink:
---
Subject: _Mathematical Analysis_
Main\_Topic: _The Real and Complex Number Systems_
Applications: _Analysis_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _[[Principles of Mathematical Analysis.pdf]]_
Closely\_Related\_To: _[[Triangle Inequality (Euclidean Geometry)]],[[Complex Numbers Algebraic Properties]],[[Basic Topology]]_
Cont.\_ of: _None_ 
_
_

A satisfactory discussion of analysis is built from an accurately defined number concept. We shall start with this ideal and built from there.

##### Real Number System
The rational number system is inadequate for many purposes, both as a field and as an ordered set. For instance, there is no rational $p$ such that $p^{2}=2$. This leads to the introduction of so-called "irrational numbers" which are often written as infinite decimal expansions and are considered to be "approximated" by the corresponding finite decimals. Thus, we say that the sequence 
$$
1,1.4,1.41,1.414,\ldots
$$
tends to $\sqrt{2}$. But unless the irrational number $\sqrt{2}$ has been clearly defined, the question must arise: Just what is it that this sequence "tends to"?

This sort of question can be answered as soon as the so called "real number system" is constructed

---
**Example:**  We now show that the equation $p^{2}=2$ is not satisfied by any rational $p$.

**Proof:**  If there were such a $p$, we could write $p=\frac{m}{n}$ where $m,n \in \mathbb{Z}$ where $m$ and $n$ are not both even. Let us assume this is done. Then from substitution we can imply that $m^{2}=2n^{2}$. This shows that $m^{2}$ must be even. Hence, $m$ is even (if $m$ were odd, $m^{2}$ would be odd), and so $m^{2}$ us divisible by $4$. It follows that the right side of this equation is divisible by $4$, so that $n^{2}$, so that $n^{2}$ is even, which implies that $n$ is even. 

The assumption that $p^{2}=2$ holds thus leads to the conclusion that both $m$ and $n$ are even, contrary to our choice of $m$ and $n$. Hence, $p^{2} =2$ is impossible for rational $p$. 

We can now examine this situation a little more closely. Let $A$ be the set of all positive rationals $p$ such that $p^{2}<2$ and let $B$ consist of all positive rationals $p$ such that $p^{2}>2$. We shall show that $A$ contains _no largest number_ and $B$ contains _no smallest number_. 

More explicitly, for every $p$ in $A$ we can find a rational $q$ in $A$ such that $p<q$, and for every $p$ in $B$ we can find a rational $q$ in $B$ such that $q<p$. To do this, we associate with each rational $p>0$ the number 
$$
q = p - \frac{p^{2}-2}{p+2} = \frac{2p+2}{p+2}.
$$
Then,
$$
q^{2} - 2 = \frac{2(p^{2}-2)}{(p+2)^{2}}.
$$
If $p$ is in $A$, then $p^{2}-2<0$, and our equation for $p$ shows that $q>p$, and that $q^{2}<2$. This $q$ is in $A$.

If $p$ is in $B$ then $p^{2}-2>0$ and we see that $0<q<p$, and that $q^{2}>2$. Thus $q$ is in $B$. 

**Remark.**  The purpose of the above discussion has been to show that the rational number system has certain gaps, in spite of the fact that between two rationals there is another. The real number system fills these gaps. This is the principle reason for the fundamental role which it plays in analysis.

---
We now begin discussion on the general concepts which will lead into _ordered sets_ and _fields_. 

#### Basic Definitions for Sets
```ad-Definition
If $A$ is any set (whose elements may be numbers or any other objects), we write $x \in A$ to indicate that $x$ is a member of $A$. If $x$ is not a member of $A$, we write $x \notin A$.

The set which contains no element is the _empty set_. If a set has at least one element, it is _non empty_.

If $A$ and $B$ are sets, and if every element of $A$ is an element of $B$, we say that $A$ is a subset of $B$, and write $A \subset B$. If, in addition, there is an element of $B$ which is not in $A$, we say $A$ is a _proper_ subset of $B$. Not that $A \subset A$ for every set $A$.

If $A \subset B$ and $B \subset A$, we write $A=B$. Otherwise, $A\neq B$.

The set of all rational numbers is denoted by $Q$.

```

```ad-Definition
An _ordered set_ is a set $S$ in which an order is defined. 

For example, $Q$ is an ordered set if $r<s$ is defined to mean that $s-r$ is a positive rational number.
```

```ad-Definition
Suppose $S$ is an ordered set, and $E\subset S$. If there exists a $\beta \in S$ such that $x \leq \beta$ for every $x \in E$, we say that $E$ is _bounded above_, and call $\beta$ an _upper bound_ of $E$. 

Lower bounds are defined in the same way (with $\geq$ instead of $\leq$).
```

##### Supremum and Infimum
```ad-Definition
Suppose $S$ is an ordered set, $E \subset S$, and $E$ is bounded above. Suppose there exists an $\alpha \in S$ with the following properties:
1. $\alpha$ is an upper bound of $E$.
2. If $\gamma<\alpha$ then $\gamma$ is not an upper bound of $E$.

Then $\alpha$ is called the _least upper bound of_ $E$ (that there is at most one such $\alpha$ is clear from condition 2) or the _supremum_ of $E$, and we write 
$$
\alpha = \sup E
$$

The _greatest lower bound_, or _infimum_, of a set $E$ which is bounded below is defined in the same manner: The statement 
$$
\alpha = \inf E
$$
means that $\alpha$ is a lower bound of $E$ and that no $\beta$ with $\beta>\alpha$ is a lower bound of $E$. 

```

**Example 1:**  Consider the sets $A$ and $B$ from our previous example $p^{2}=2$ as subsets of the ordered set $Q$. The set $A$ is bounded above. In fact, the upper bounds of $A$ are exactly the members of $B$. Since $B$ contains no smallest member, $A$ _has no least upper bound_ in $Q$. Similarly, $B$ is bounded below: The set of all lower bounds of $B$ consists of $A$ and of all $r \in Q$ with $r \leq 0$. Since $A$ has no largest member, $B$ has _no greatest lower bound_ in $Q$.

**Example 2:**  If $\alpha=\sup E$ exists, then $\alpha$ may or may not be a member of $E$. For instance, let $E_{1}$ be the set of all $r \in Q$ with $r<0$. Let $E_{2}$ be the set of all $r \in Q$ with $r\leq 0$. Then
$$
\sup E_{1} = \sup E_{2} = 0,
$$
and $0 \notin E_{1}, 0 \in E_{2}$. 

**Example 3:**  Let $E$ consist of all numbers $\frac{1}{n}$, where $n=1,2,3,\ldots$. Then $\sup E = 1$, which is in $E$, and $\inf E = 0$, which is not in $E$. 

##### Upper and Lower Bound Property
```ad-Definition
An ordered set $S$ is said to have the _lest-upper-bound property_ if the following is true:

If $E \subset S$, $E$ is not empty, and $E$ is bounded above, then $\sup E$ exists in $S$.
```

**Theorem 1.**  Suppose that $S$ is an ordered set with the least-upper-bound property, $B \subset S$, $B$ is not empty, and $B$ is _bounded below_. Let $L$ be the set of all _lower bounds_ of $B$. Then 
$$
\alpha= \sup L
$$
exists in $S$, and $\alpha=\inf B$. In particular, $\inf B$ _exists_ in $S$.


**Proof:**  Since $B$ is bounded below, $L$ is not empty. Since $L$ consists of exactly those $y \in S$ which satisfy the inequality $y\leq x$ for every $x\in B$, we see that _every_ $x \in B$ is an _upper bound_ of $L$. Thus, $L$ is bounded above. Our hypothesis about $S$ implies therefor that $L$ has a supremum in $S$; call it $\alpha$. 

If $\gamma<\alpha$, then by definition (which we stated before), $\gamma$ is not an upper bound of $L$, hence $\gamma \notin B$. It follows that $\alpha\leq x$ for every $x \in B$. Thus, $\alpha \in L$. If $\alpha < \beta$ then $\beta \notin L$, since $\alpha$ is an upper bound of $L$. 

We have shown that $\alpha\in L$ but $\beta\notin L$ if $\beta>\alpha$. In other words, $\alpha$ is a lower bound of $B$, but $\beta$ is not if $\beta>\alpha$. This means that $\alpha=\inf B$.

#### Fields: Definition and Propositions

```ad-Definition
A _field_ is a set $F$ with two operations, called _addition_ and _multiplication_, which satisfy the following so-called "field axioms" (A),(M), and (D):
```

**Remark.**  See more in [[Integral Domains#Fields]] to understand fields.

![[Pasted image 20230908124228.png|center]]

![[Pasted image 20230908124249.png|center]]

![[Pasted image 20230908124312.png|center]]


**Remark.**  One usually writes (in any field) 
$$
x-y, \frac{x}{y}, x+y+z,xyz,x^{2},x^{3},2x,3x,\ldots
$$
in place of 
$$
x+(-y), x\cdot \left(\frac{1}{y}\right),(x+y)+z, (xy)z, xx, xxx, x+x, x+x+x,\ldots
$$

The field axioms clearly hold in $Q$, the set of all rational numbers, if addition and multiplication have their customary meaning. Thus, $Q$ is a field.

Although it is not our purpose to study fields (or any other algebraic structures) in detail, it is worthwhile to prove that some familiar properties of $Q$ are consequences of the field axioms; once we do this, we will not need to do it again for the real numbers and for the complex numbers. 

---
**Proposition 1:**  The axioms for addition imply the following statements:
1. If $x+y=x+z$, then $y=z$.
2. If $x+y=x$, then $y=0$.
3. If $x+y=0$, then $y=-x$.
4. $-(-x)=x$

**Proof:**  If $x+y=x+z$, the axioms (A) give 
$$
y=0+y=(-x+x)+y=-x+(x+y) = -x+(x+z) = z
$$
We can substitute $z=0$ or $z=-x$, etc. to obtain our proposition.

---
**Proposition 2:**  The axioms for  multiplication imply the following statements:
1. If $x\neq 0$ and $xy=xz$, then $y=z$
2. If $x \neq 0$ and $xy=x$, then $y=1$
3. If $x \neq 0$ and $xy=1$, then $y=1/x$
4. If $x\neq 0$ then $\frac{1}{\frac{1}{x}}=x$

**Proof:**  The proof is so similar to the before proposition that we will omit it.

---
**Proposition 3:**  The field axioms imply the following statements, for any $x,y,z \in F$.
1. $0x = 0$
2. If $x \neq 0$ and $y \neq 0$ then $xy \neq 0$
3. $(-x)y=-(xy)=x(-y)$
4. $(-x)(-y)=xy$

**Proof:**  $0x+0x=(0+0)x=0x$. This implies that $0x=0$. Next, assume that $x \neq 0, y \neq 0$, but $xy=0$. Then from (1) we get 
$$
1= \left(\frac{1}{y}\right)\left(\frac{1}{x}\right)xy = \left(\frac{1}{y}\right)\left(\frac{1}{x}\right)0 = 0
$$
which is a contradiction. Thus, (2) holds. The first equality in (3) comes from 
$$
(-x)y+xy=(-x+x)y = 0y = 0
$$
combined with _Proposition 1, condition_ $3$. Finally, 
$$
(-x)(-y) = -(x(-y)) = -(-(xy)) = xy
$$
by (3) and _Proposition 1, condition_ 4.

---

##### Ordered Field
```ad-Definition
An _ordered field_ is a field $F$ which is also an _ordered set_, such that 
1. $x+y<x+z$ if $x,y,z \in F$ and $y<z$,
2. $xy>0$ if $x \in F, y \in F, x>0$, and $y>0$.

If $x>0$, we call $x$ _positive_; if $x<0$, $x$ is _negative_.
```

For example $Q$ is an ordered field. 

All familiar rules for working with inequalities apply in every ordered field: Multiplication by a particular sign preserves inequalities, no square is negative, etc. The following proposition lists some of these:

**Proposition 4:**  The following statements are true in _every ordered field_: 
1. If $x>0$ then $-x<0$ and vise versa.
2. If $x>0$ and $y<z$ then $xy=xz$.
3. If $x<0$ and $y<z$ then $xy>xz$.
4. If $x \neq 0$ then $x^{2}>0$. In particular, $1>0$.
5. If $0<x<y$ then $0<\frac{1}{y}<\frac{1}{x}$.

**Proof:**  If $x>0$ then $0=-x+x>-x+0$, so that $-x<0$. If $x<0$ then $0=-x+x<-x+0$, so that $-x>0$. This proves (1). 

Since $z>y$, we have $z-y>y-y=0$, hence $x(z-y)>0$, and therefore 
$$
xz=x(z-y)+xy>0+xy=xy
$$
By (1), (2), and proposition 3, condition (3), 
$$
-(x(z-y)) = (-x)(z-y) > 0,
$$
so that $x(z-y)<0$, hence $xz<xy$.

If $x>0$, part (2) of our _definition_ for ordered fields gives $x^{2}>0$. If $x<0$, then $-x>0$, hence $(-x)^{2}>0$. But $x^{2}=(-x)^{2}$, by Proposition 3, condition 4. Since $1=1^{2},1>0$. 

If $y>0$ and $v \leq 0$, then $yv\leq 0$. But $y \cdot \frac{1}{y} = 1>0$. Hence $\frac{1}{y}>0$. Likewise, $\frac{1}{x}>0$. If we multiply both sides of the inequality $x<y$ by the positive quantity $\frac{1}{x} \cdot \frac{1}{y}$, we obtain $\frac{1}{y} < \frac{1}{x}$

### The Real Field 
We now state the _existence theorem_ is the core of this chapter.

**Theorem 2.**  There exists an ordered field $R$ which has the _least upper bound property_. Moreover, $R$ contains $Q$ as a _subfield_. 

**Remark.**  The second statement means that $Q \subset R$ and that the operations of addition and multiplication in $R$, when applied to the member of $Q$, coincide with the usual operations on rational numbers; also, the positive rational numbers are positive elements of $R$. 

The members of $R$ are called _real numbers_. 

**Proof:**  The proof of this theorem is rather long and tedious. It can be seen in an Appendix to Chapter 1. in [[Principles of Mathematical Analysis.pdf]]. The proof actually constructs $R$ from $Q$. 

---
##### Archimedean and Dense Property
The next theorem could be extracted from this construction with very little extra effort. However, we prefer to derive it from our previous theorem of existence since it provides a good illustration of what one can do with the least-upper-bound property. 

**Theorem 3.**  
a)  if $x \in R, y \in R$, and $x>0$, then there is a positive integer $n$ such that 
$$
nx>y.
$$
b)  if $x \in R, y \in R$, and $x<y$, then there exists a $p \in Q$ such that $x<p<y$. 

Part (a) is usually referred to as the _Archimedean property_ of $R$. Part (b) may be stated by saying that $Q$ is _dense_ in $R$: between any two real numbers there is a rational one.

**Proof:**  
a)  Let $A$ be the set of all $nx$, where $n$ runs through the positive numbers. If (a) were false, then $y$ would appear to be an upper bound of $A$. But then $A$ has a _least_ upper bound in $R$. Put $\alpha= \sup A$. Since $x>0, \alpha-x< \alpha$, and $\alpha-x$ is not an upper bound of $A$. Hence, $\alpha-x<mx$ for some positive integer $m$. But then $\alpha<(m+1)x \in A$, which is impossible, since $\alpha$ is an upper bound of $A$. 

b)  Since $x<y$, we have $y-x>0$, and (a) furnishes a positive integer $n$ such that 
$$
n(y-x)>1.
$$
Apply (a) again, to obtain positive integers $m_{1}$ and $m_{2}$ such that $m_{1}>nx, m_{2}>-nx$. Then 
$$
-m_{2}<nx<m_{1}
$$
Hence there is an integer $m$ (with $-m_{2}\leq m \leq m_{1}$) such that 
$$
m-1 \leq nx < m
$$
If we combine these inequalities, we obtain 
$$
nx < m \leq 1+nx < ny.
$$
Since $n>0$, it follows that 
$$
x< \frac{m}{n} < y.
$$
This proves (b), with $p=\frac{m}{n}$. 

---
##### Existence of nth Roots for Real Numbers
We shall now prove the existence of $n$th roots of positive reals. This proof will show how the difficulty pointed out in in the beginning (irrationality of $\sqrt{2}$) can be handled in $R$.

**Theorem 4.**  For every real $x>0$ and every integer $n>0$ there is one and only one positive real $y$ such that $y^{n}=x$. 

This number $y$ is written as $\sqrt[n]{x}$ or $x^{\frac{1}{n}}$. 

**Proof:**  That there is at most one such $y$ is clear, since $0<y_{1}<y_{2}$ implies that $y_{1}^{n}<y_{2}^{n}$. Let $E$ be the set consisting of all positive real number $t$ such that $t^{n}<x$. If $t=\frac{x}{1+x}$ then $0\leq t < 1$. Hence, $t^{n}\leq t<x$. Thus, $t\in E$ and $E$ is not empty. If $t>1+x$ then $t^{n}\geq t>x$, so that $t \notin E$. Thus, $1+x$ is an upper bound of $E$. 

Hence, our Theorem 2 at the beginning of this section implies the existence of 
$$
y = \sup E
$$
To prove that $y^{n}=x$ we will show that each of the inequalities $y^{n}<x$ and $y^{n}>x$ leads to a contradiction. The identity $b^{n}-a^{n} = (b-a)(b^{n-1}+b^{n-2}a+\ldots+a^{n-1})$ yields the inequality 
$$
b^{n}-a^{n} < (b-a)nb^{n-1}
$$
if $0<a<b$. Let us assume that $y^{n}<x$. Choose $h$ so that $0<h<1$ and 
$$
h < \frac{x-y^{n}}{n(y+1)^{n-1}}
$$
Put $a=y,b=y+h$. Then 
$$
(y+h)^{n}-y^{n}<hn(y+h)^{n-1}<hn(y+1)^{n-1}<x-y^{n}
$$
Thus, $(y+h)^{n}<x$, and $y+h \in E$. Since $y+h>y$, this contradicts the fact that $y$ is an upper bound of $E$. Now, we assume that $y^{n}>x$. Let
$$
k = \frac{y^{n}-x}{ny^{n-1}}
$$
then $0<k<y$. If $t\geq y-k$, we conclude that 
$$
y^{n}-t^{n} \leq y^{n}-(y-k)^{n}<kny^{n-1}=y^{n}-x
$$
Thus $t^{n}>x$ and $t \notin E$. It follows that $y-k$ is an upper bound of $E$. But $y-k<y$, which contradicts the fact that $y$ is the _least_ upper bound of $E$.

Hence, by these contradictions, $y^{n}=x$, and the proof is complete. 

---
**Corollary.**  If $a$ and $b$ are positive real numbers and $n$ is a positive integer, then 
$$
(ab)^{\frac{1}{n}}= a^\frac{1}{n}b^\frac{1}{n}
$$

**Proof:**  But $\alpha=a^\frac{1}{n}$, $\beta=b^\frac{1}{n}$. Then 
$$
ab = \alpha^{n}\beta^{n} = (\alpha \beta)^{n}
$$
since multiplication is commutative (Axiom M2). The uniqueness theorem stated in Theorem 4 (above), shows therefore that 
$$
(ab)^{\frac{1}{n}}= \alpha \beta = a^\frac{1}{n}b^\frac{1}{n}
$$

##### Decimals
Let $x>0$ be real. Let $n_{0}$ be the largest integer such that $n_{0}\leq x$ (Note that the existence of $n_{0}$ depends on the Archimedean property of $R$.) Having chosen $n_{0},n_{1},\ldots,n_{k-1}$, let $n_{k}$ be the largest integer such that 
$$
n_{0} + \frac{n_{1}}{10} + \ldots  + \frac{n_{k}}{10^{k}} \leq x
$$
Let $E$ be the set of these numbers 
$$
n_{0}+\frac{n_{1}}{10}+\ldots+ \frac{n_{k}}{10^{k}} \quad (k=0,1,2,\ldots).
$$
Then $x= \sup E$. The decimal expansion of $x$ is 
$$
n_{0}\cdot n_{1}n_{2}n_{3}\ldots
$$
Conversely, for any infinite decimal, the set $E$ of numbers is bounded above, and $n_{0}\cdot n_{1}n_{2}n_{3}$ is the decimal expansion of $\sup E$. 

##### The Extended Real Number System
```ad-Definition
The extended real number system consists of the real field $R$ and two symbols, $+\infty$ and $-\infty$. We preserve the original order in $R$ and define 
$$
-\infty < x < +\infty
$$
for every $x \in R$.
```

It is clear that $+\infty$ is an upper bound of every subset of the extended real number system, and that every nonempty subset has a least upper bound. If, for example, $E$ is a nonempty set of real numbers which is not bounded above in $R$, then $\sup E = +\infty$ in the extended real number system. Exactly the same remarks apply to lower bounds. 

The extended real number system does not form a field, but it is customary to make the following conventions: 

![[Pasted image 20230909160106.png|center]]

When it is desired to make the distinction between real numbers on the one hand and the symbols $+\infty$ and $-\infty$ on the other quite explicit, the former are called _finite_. 

### The Complex field

```ad-Definition
A _complex number_ is an ordered pair $(a,b)$ of real numbers. "Ordered" means that $(a,b)$ and $(b,a)$ are regarded as distinct if $a\neq b$. 
```

Let $x=(a,b)$ and $y=(c,d)$ be two complex numbers. We write $x=y$ if and only if $a=c$ and $b=d$. We define 
$$
x+y = (a+c,b+d), \quad xy = (ac-bd,ad+bc)
$$

**Theorem 5.**  These definition of addition and multiplication turn the set of all complex numbers into a field with $(0,0)$ and $(1,0)$ in the role of $0$ and $1$. 

**Proof:**  We simple verify all of the field axioms as listed in [[#Fields Definition and Propositions]]. (Of course, we use the field structure of $R$). We will omit this proof because it is very direct and straightforward to the other proofs before). 


**Theorem 6.**  For any real numbers $a$ and $b$ we have 
$$
(a,0)+(b,0) = (a+b,0), \quad (a,0)(b,0) = (ab,0)
$$

**Proof:**  The proof is trivial

---
Theorem 6 shows that the complex numbers of the form $(a,0)$ have the same arithmetic properties as the corresponding real numbers $a$. We can therefore identify $(a,0)$ with $a$. This identification gives us the real field as a subfield of the complex field. 

The reader may have noticed that we have defined the complex numbers without any reference to the mysterious square root of $-1$. We now show that the notation $(a,b)$ is equivalent to the more customary $a+bi$. More detail can be seen in [[Complex Numbers Algebraic Properties]]. 

##### Schwartz Inequality

**Theorem 7.**  If $a_{1},\ldots,a_{n}$ and $b_{1},\ldots,b_{n}$ are complex numbers, then 
$$
\left| \sum\limits_{j=1}^{n} a_{j} \overline{b_{j}} \right|^{2}\leq \sum\limits_{j=1}^{n}|a_{j}|^{2} \ \sum\limits_{j=1}^{n} |b_{j}|^{2}
$$
**Proof:**  Put $A= \sum\limits|a_{j}|^{2},B=\sum\limits|b_{j}|^{2},C=\sum\limits a_{j}\overline{b_{j}}$. If $B=0$, then $b_{1}=\ldots=b_{n}=0$, and the conclusion is trivial. Assume therefore that $B>0$. By using the complex conjugate we have 
$$
\sum\limits |Ba_{j}-Cb_{j}|^{2} = \sum\limits(Ba_{j}-Cb_{j})(B\overline{a_{j}} - \overline{Cb_{j}})
$$
$$
 = B^{2} \sum\limits |a_{j}|^{2} - B\overline{C} \sum\limits a_{j}\overline{b_{j}} + |C|^{2} \sum\limits |b_{j}|^{2}
$$
$$
 = B^{2}A - B|C|^{2}
$$
$$
B(AB-|C|^{2})
$$
Since each term in the first sum is nonnegative, we see that 
$$
B(AB-|C|^{2}) \geq 0.
$$
Since $B>0$, it follows that $AB-|C|^{2}\geq 0$. This is the desired inequality. 

### Euclidean Spaces

```ad-Definition
For each positive integer $k$, let $R^{k}$ be the set of all ordered $k$-tuples 
$$
\pmb{x} = (x_{1},x_{2},\ldots,x_{k}),
$$
where $x_{1},\ldots,x_{k}$ are real numbers, called the _coordinates_ of $\pmb{x}$. The elements of $R^{k}$ are called points, or vectors, especially when $k>1$. We shall denote vectors by holdfaced letters. If $\pmb{y} = (y_{1},\ldots,y_{k})$ and if $\alpha$ is a real number, put 
$$
\begin{gathered}
\bf{x}+\bf{y} = (x_{1}+y_{1}\ldots,x_{k}+y_{k}), \\
\alpha \bf{x} = (\alpha x_{1}, \ldots, \alpha x_{k})
\end{gathered}
$$
so that $\bf{x}+\bf{y} \in R^{k}$ and $\alpha \bf{x} \in R^{k}$. This defines addition of vectors, as well as multiplication of a vector by a real number (a scalar). These two operations satisfy the commutative, associative, and the distributive laws (the proof is trivial, in view of the analogou laws for the real numbers) and make $R^{k}$ into a _vector space over the real field_. the zero element of $R^{k}$ (sometimes called the _origin_ or _null vector_) s the point $\bf{0}$, all of whose coordinates are $0$. 
```

We also define the so-called "inner product" of $\bf{x}$ and $\bf{y}$ by 
$$
\bf{x} \cdot \bf{y} = \sum\limits_{i=1}^{k}x_{i}y_{i}
$$
and the _norm_ of $\bf{x}$ by 
$$
|\bf{x}| = (\bf{x}\cdot \bf{x})^{\frac{1}{2}} = \left(\sum\limits_{1}^{k}x_{i}^{2}\right)^\frac{1}{2}
$$
The structure now defined (the vector space $R^{k}$ with the above inner product and norm) is called Euclidean $k$-space. 

**Theorem 8.**  Suppose that $\bf{x,y,z} \in R^{k}$ and $\alpha$ is real. Then 
1. $|\bf{x}| \geq 0$;
2. $|\bf{x}|=0$ if any only if $\bf{x}=0$;
3. $|\alpha \bf{x}| = |\alpha||\bf{X}|$; 
4. $|\bf{x} \cdot \bf{y}| \leq |\bf{x}||\bf{y}|$;
5. $|\bf{x}+\bf{y}| \leq |\bf{x}|+|\bf{y}|$;
6. $|\bf{x}-\bf{z}| \leq |\bf{x}-\bf{y}|+|\bf{y}-\bf{z}|$

**Proof:**  1, 2, 3, and 4 are all immediate consequences of the Schwartz inequality. By using 4 we can prove 5, and 6 follows if we make substitutions into 5. 

**Remark.**  1, 2, and 6 will allow us to regard $R^{k}$ as a metric space. 


