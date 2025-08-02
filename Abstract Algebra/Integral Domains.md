---
tags:
  - Math
  - ring
  - rings
  - integral
  - integral_domain
  - field
  - fields
  - domain
  - commutative
  - characteristic
  - zero_divisors
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _Integral Domains_
Applications: _None_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 2_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra]]_
Closely\_Related\_To: _[[Introduction to Rings]]_
Cont.\_ of: _None_ 
_
_

To a certain degree, the notion of a ring was invented in an attempt to put the algebraic properties of the integers into an abstract setting. A ring is not the appropriate abstraction of the integers, however, for too much is lost in the process. Besides the two obvious properties of commutativity and existence of a unity, there is one further essential feature of the integers that rings in general do not enjoy. We shall introduce integral domains$-$a particular class of rings that have all three of these properties. Integral domains play a prominent role in number theory and algebraic geometry. 

```ad-Definition
A nonzero element $a$ of a **commutative ring** $R$ is called a _zero-divisor_ if there is a nonzero element $b$ in $R$ such that $ab=0$.
```

```ad-Definition
A **commutative ring** with a unity is said to be an _integral domain_ if it has no zero-divisors. 

```

**Remark.**  In an integral domain, a product is zero only when one of the factors is zero; that is, $ab=0$ only when $a=0$ or $b=0$. 

What makes integral domains particularly appealing is that they have an important multiplicative group-theoretic property, in spite of the fact that the nonzero elements need not form a group under multiplication. This property is **cancellation**, the same as the one expressed in [[Groups#Cancellation]]. 

**Theorem 15.1**  Let $a,b,c$ belong to an integral domain. If $a\neq 0$ and $b \neq 0$ and $ab=ac$, then $b=c$. 

**Proof:**  From $ab=ac$ we have $a(b-c)=0$. Since $a \neq 0$, we must have $b-c=0$. 

Many people prefer to define integral domains by the cancellation property, that is, as a commutative ring with unity in which the cancellation property holds. That definition is equivalent to ours. 


##### Fields
In many applications, a particular find of integral domain called a _field_ is necessary. 

```ad-Definition
A cummutative ring with a unity is called a _field_ if every nonzero element is a unit. 
```

It is often helpful to think of $ab^{-1}$ as $a$ divided by $b$. With this in mind, a field can be thought of as simple an algebraic system that is closed under addition, subtraction, multiplication, and division (except by $0$). We have had numerous examples of fields: the complex numbers, the real numbers, the rational numbers. The abstract theory of fields was initiated by Heinrich Weber in 1893. Groups, rings, and fields are the three main branches of abstract algebra. This next theorem says that, in the finite case, fields and integral domains are the same. 

**Theorem 15.2**  A finite integral domain is a field.

**Proof:**  Let $D$ be a finite integral domain with unity $1$. Let $a$ be any nonzero element of $D$. We must show that $a$ is a unity. If $a=1$, $a$ is its own inverse, so we may assume that $a\neq 1$. Now consider the following sequence of elements of $D$: $a,a^{2},a^{3},\ldots$. Since $D$ is finite, there must be two positive integers $i$ and $j$ such that $i>j$ and $a^{i}=a^{j}$. Then, by cancellation, $a^{i-j}=1$. Since $a \neq 1$, we know $i-j>1$, and we have shown $a^{i-j-1}$ is the inverse of $a$. 

**Corollary**  For every prime $p$, $Z_{p}$ the ring of integers modulo $p$, is a field.

**Proof:**  According the Theorem 15.2 we need only prove that $Z_{p}$ has no zero-divisors. So, suppose $a,b \in Z_{p}$ and $ab=0$. Then $ab=pk$ for some integer $k$. But, then, by Euclid's lemma ([[Properties of Integers, Algebra, and Functions#Euclid's Lemma]]), $p$ divides $a$ or $p$ divides $b$. Thus, in $Z_{p}$, $a=0$ or $b=0$.  

From this corollary, we can now see that $Z_{n}$ is a field if and only if $n$ is prime. Later on, we will describe how all finite field scan be constructed. 

##### Characteristic of a Ring
Note that for any element $x$ in $Z_{3}[i]$, we have $3x=x+x+x=0$, since addition is done modulo $3$. Similarly, in the [[Introduction to Rings#Subrings|subring]] $\{0,3,6,9\}$ of $Z_{12}$ we have $4x=x+x+x+x=0$ for all $x$. This observation motivates the following definition. 

```ad-Definition
The _characteristic_ of a ring $R$ is the least positive integer $n$ such that $nx=0$ for all $x$ in $R$. If no such integer exists, we say $R$ has charaacteristic $0$. 
```

Thus, the ring of integers has characteristic $0$ and $Z_{n}$ has characteristic $n$. An infinite ring can have nonzero characteristic. Indeed, the ring $Z_{2}[x]$ of all polynomials with coefficients in $Z_{2}$ has characteristic $2$. (Addition and multiplication are done as with polynomials with ordinary integer coefficients except that the coefficients are reduced modulo $2$.) When a ring has a unity, the task of determining the characteristic is simplified by Theorem 15.3.

**Theorem 15.3**  Let $R$ be a ring with unity $1$. If $1$ has infinite order under addition, then the characteristic of $R$ is $0$. If $1$ has order $n$ under addition, then the characteristic of $R$ is $n$. 

**Proof:**  If $1$ has infinite order, then there is no positive integer $n$ such that $n \cdot 1 = 0$, so $R$ has characteristic $0$. Now suppose that $1$ has additive order $n$. Then $n \cdot 1=0$ and $n$ is the least positive integer with this property. So for any $x$ in $R$ we have 
$$
nx = n(1x)=(n\cdot 1)x = 0x = 0.
$$
Thus, $R$ has characteristic $n$.

In the case of an integral domain, the possibilities for the characteristic are severely limited. 

---
**Theorem 15.4**  The characteristic of an integral domain is $0$ or prime. 

**Proof:**  By Theorem 15.3, it suffices to show that if the additive order of $1$ is finite, it must be prime. Suppose $1$ has order $n$ and $n=st$ where $1<s,t<n$. Then 
$$
0=n \cdot 1 = (st) \cdot 1 = (s \cdot 1)(t \cdot 1)
$$
So, $s \cdot 1 = 0$ or $t \cdot 1 = 0$. But this contradicts the fact that $1$ has order $n$. Hence, $n$ cannot be factored as a product of two smaller integers. 

##### Summary of Rings and Their Properties

![[Pasted image 20231013123652.png|center]]
