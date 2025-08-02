---
tags: Integers, Math, Euclid, Division, algorithm, order, well_ordering_principle, fundamental_theorem_of_algebra, gcd, lcd
dg-publish: true
mathLink: 
---
Subject: _Algebraic Systems_
Main\_Topic: _Properties of Integers_
Applications: _Abstract Algebra_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|Contemporary Abstract Algebra Textbook]]_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

Much of abstract algebra involves properties of integers and sets. Some of which are described below.

### Division Algorithm and Well Ordering Principle
```ad-Definition
**Well Ordering Principle**: Every nonempty set of positive integers contains a smallest member.

```

The concept of divisibility plays a fundamental role in the theory of numbers. We say a nonzero integer $t$ is a _divisor_ of an integer $s$ if there is an integer $u$ such that $s=tu$. In this case, we write $t \vert s$ ("t divides s"). When $t$ is not a divisor of $s$, we write that $t\not{|}\ s$. A _prime_ number is a positive integer greater than $1$ whose only positive divisors are $1$ and itself.   

We can apply the **well ordering principle** to create the division algorithm. 

```ad-Definition
**Division Algorithm**: If we let $a$ and $b$ be integers with $b>0$, then there exist _unique_ integers $q$ and $r$ with the property that $a=bq+r$ where $0\leq r<b$.

```

---
**Proof:**  We begin with the existence portion of the theorem. Consider the set $S=\{a-bk \rvert \ k \  \text{is an integer and } a-bk\geq 0 \}$. If $0 \in S$, then $b$ divides $a$ and we may obtain the desired result with $q=\frac{a}{b}$ and $r=0.$ Now assume that $0 \notin S$. Since $S$ is nonempty (if $a>0, \ a-b \cdot 0 \in S$; if $a<0, a-b(2a)=a(1-2b) \in S$), we may apply the **Well Ordering Principle** to conclude that $S$ has a smallest member, say $r=a-bq$. Then $a=bq+r$ and $r \geq 0$, so all that remains to be proved is that $r<b$. 

On the contrary, if $r>b$, then $a-b(q+1)=a-bq-b=r-b>0$ so that $a-b(q+1) \in S$. But $a-b(q+1)<a-bq,$ and $a-bq$ is the _smallest_ member of $S$.  Thus $r \leq b$. If $r=b$, then $0\in S$ and this case is already taken care of. So, $r<b$. 

To establish the uniqueness of $q$ and $r$, let us suppose that there are integers of $q, q',r$, and $r'$ such that 
$$
a=bq+r, \ \ 0\leq r < b \quad \text{and} \quad a=bq'+r', \ \ 0\leq r' < b.
$$
For convenience, we may also suppose that $r' \geq r$. Then $bq+r=bq'+r'$ and $b(q-q')=r'-r$. So, $b$ divides $r'-r$ and $0 \leq r'-r\leq r'<b$. It follows that $r'-r=0$ and therefore $r'=r$ and $q=q'$. 

**Remark.**  The integer $q$ in the division algorithm is called the _quotient_ upon dividing $a$ by $b$, and $r$ is the remainder.

---
### GCD
The _greatest common divisor_ of two nonzero integers $a$ and $b$ is the largest of all common divisors of $a$ and $b$. We denote this by $\gcd(a,b)$. When $\gcd(a,b)=1$, we say that $a$ and $b$ are _relatively prime_. 

The proof for the GCD can be shown as an application of the Well Ordering Principle. This result is Proposition 1 in Book Seven of Euclid's _Elements_. 

```ad-Definition
For any nonzero integers $a$ and $b$, there exists integers $s$ and $t$ such that $\gcd(a, b)=as+bt$.
```

**Proof:**  Consider the set $S=\{am + bn \vert \ m,n \ \text{are integers and} \ am+bn>0 \}$. Since $S$ is obviously nonempty (if some choice of $m$ and $n$ makes $am+bn<0$, then replace $m$ and $n$ by $-m$ and $-n$), the Well Ordering Principle asserts that $S$ has a smallest member, say, $d=as+bt$. We claim that $d=\gcd(a,b)$. 

To verify this claim, use the division algorithm to write $a=dq+r$ where $0 \leq r < d$. If $r>0$, then $r=a-dq=a-(as+bt)q=a-asq-btq=a(1-sq)+b(-tq) \in S$, contradicting the fact that $d$ is the smallest member of $S$. So, $r=0$ divides $a$. Analogously, $d$ divides $b$ as well. This proves that $d$ is a common divisor of $a$ and $b$.

Now, suppose that $d'$ is another common divisor of $a$ and $b$ and write that $a=d'h$ and $b=d'k$. Then $d=as+bt=(d'h)s+(d'k)t=d'(hs+kt)$ so that $d'$ is a divisor $d$. Thus, among all common divisors of $a$ and $b$, $d$ is the greatest.  

**Remark.**  GCD is a **Linear Combination**.  

---
### Euclidean Algorithm and Euclid's Lemma
Although the result for the GCD is a powerful theoretical tool, it does not provide a practical method for calculating the greatest common divisor of two numbers $a$ and $b$ or the specific values $s$ and $t$. 

We employ the **Euclidean Algorithm** to do this. For any pair of positive integers $a$ and $b$ we may find the $\gcd(a,b)$ by repeated use of division to produce a decreasing sequence of integers: $r_{1}>r_{2}>\ldots$ as follows. 
$$
\begin{gathered}
a=bq_{1}+r_{1} \quad (0<r_{1}<b),\\
b=r_{1}q_{2}+r_{2} \quad (0<r_{2}<r_{1}), \\
r_{1}=r_{2}q_{3}+r_{3} \quad (0<r_{3}<r_{2}),\\
\vdots \\
r_{k-3}=r_{k-2}q_{k-1}+r_{k-1} \quad (0<r_{k-1}<r_{k-2}) \\
r_{k-2} =r_{k-1}q_{k}+r_{k} \quad (0<r_{k}<r_{k-1}), \\
r_{k-1}=r_{k}q_{k+1}+0

\end{gathered}
$$
(it is a consequence of the Well Ordering Principle that this process must eventually result in a remainder of $0$.) Then $r_{k}$, the last nonzero remainder, is the $\gcd(a,b)$. 

To see that $r_{k}=\gcd(a,b)$, observe that since $r_{k} \vert r_{k-1}$, the next to the last equation implies that $r_{k}\vert r_{k-2}$. This in turn, implies that $r_{k}\vert r_{k-3}$. Continuing this pattern backwards we see that $r_{k}|b$ and $r_{k}|a$. This proves that $r_{k}$ is a common divisor of $a$ and $b$. Now, if $r$ is another common divisor of $a$ and $b$, the first equation above shows that $r|r_{1}$. The second equation then shows that $r|r_{2}$. Continuing, we see that $r|r_{k}$ and indeed $r_{k}$ is the greatest of all common divisors of $a$ and $b.$ 

##### Euclid's Lemma
```ad-Definition
**Euclid's Lemma** is as follows:

$p|ab$ implies $p|a$ or $p|b$. If $p$ is a prime that divides $ab$, then $p$ divides $a$ or $p$ divides $b$.
```

**Proof:**  Suppose $p$ is a prime that divides $ab$ but does not divide $a$. We must show $p$ divides $b$. Since $p$ does not divide $a$, there are integers $s$ and $t$ such that $1=as+pt$. Then $b=abs+ptb$, and since $p$ divides the right-hand side of this equation, $p$ also divides $b$. 

**Remark.**  Note that Euclid's Lemma may fail when $p$ is not a prime. 

---
### Fundamental Theorem of Arithmetic
**Theorem.**  Every integer greater than $1$ is a prime or a product of primes. This product is unique, except for the order in which the factors appear. Thus, if $n=p_{1}p_{2}\ldots p_{r}$ and $n=q_{1}q_{2}\ldots q_{s}$ where the $p$'s and $q$'s are primes, then $r=s$ and after renumbering the $q$'s, we have $p_{i}=q_{1}$ for all $i.$  
**Proof:**  The proof can be seen here (add link) 

---
### LCM
The least common multiple of two nonzero integers $a$ and $b$ is the smallest positive integer that is a multiple of both $a$ and $b.$ This is denoted by $lcm(a,b)$. 

---
### Modular Arithmetic 
Another application of the division algorithm that will be important to us is modular arithmetic. 

```ad-Definition
Let $n$ be a fixed positive integer. For any integers $a$ and $b$, $(a+b) \mod n$ (read "a plus b mod n") is the remainder upon dividing $a+b$ by $n$; $(a\cdot b)\mod n$ is the remainder upon dividing $a\cdot b$ by n.
```

If $a$ and $b$ are integers and $n$ is a positive integer, we write $a=b\mod n$ when when $n$ divides $a-b$.  

Two important theorems when talking about about modular arithmetic are [[Eulers Theorem]] and [[Fermat's Little Theorem]]. 

### Equivalence Relations
Given two sets, equivalent relations are relationships between each element in different sets. They are useful to decompose a set into pieces, called _equivalence classes_. 

```ad-Definition
An _equivalence relation_ on a set $S$ is a set $R$ of ordered pairs of elements of $S$ such that 
$$
\begin{aligned}
1. (a,a) \in R  \ \forall a\in S \quad \text{reflexive property} \\
2. (a,b) \in R \ \text{implies} \ (b,a) \in R \quad \text{symmetric property}\\
3. (a,b) \in R \ \text{and} \ (b,c) \in R \ \text{imply} \  (a,c) \in R \quad \text{transitive property} \\
\end{aligned}
$$
```

### Function Mappings
```ad-Definition
A function $\phi$ from a set $A$ to a set $B$ is a rule that assigns to each element $a$ of $A$ exactly one element $b$ of $B$. The set $A$ is called the _domain_ of $\phi$ and $B$ is called the _codomain_ of $\phi$. If $\phi$ assigns $b$ to $a$, then $b$ is called the _image_ of $a$ under $\phi$. The subset of $B$ comprised of all the images of elements of $A$ isi called the _image_ of $A$ under $\phi$. 
```

![[Pasted image 20230830125000.png|center]]


