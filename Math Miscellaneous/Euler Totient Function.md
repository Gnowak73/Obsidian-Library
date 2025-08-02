---
tags: Math, Euler, totient_function,
dg-publish: true
mathLink: 
---
Subject: _Algebraic Systems_
Main\_Topic: _Euler Totient Function_
Applications: _Prime numbers, modular arithmetic_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _None_
Closely\_Related\_To: _[[Eulers Theorem]],[[Properties of Integers, Algebra, and Functions]]_
Cont.\_ of: _None_ 
_
_

The **Euler Totient Function** is a function that is commonly used in prime number calculations and modulus arithmetic. It is defined as follows:

```ad-Definition
$\phi(n)$ is the **Euler Totient Function**, which represents the number of integers between $1$ and $n$ whose GCD with $n$ is $1$. It can be mathematically represented as: 
$$
\phi(n) = \{x:1\leq x\leq n, \ \gcd(x,n)=1 \}
$$
```

This function has three main rules which allow for computation:
1. if $p$ is a prime number, $\phi(p)=p-1$
2. if $a=p^{n}$ is a prime power then $\phi(p^{n})=p^{n}-p^{n-1}$
3. if $\gcd(m,n)=1$ then $\phi(mn)=\phi(m)\phi(n)$ 

There is also an additional rule, which is not recommended because of its complexity: suppose the only prime divisors of $n$ are $p_{1},p_{2},\ldots,p_{k}$. Then 
$$
\phi(n) = n\left(1- \frac{1}{p_{1}}\right)\left(1- \frac{1}{p_{2}}\right)\ldots\left(1- \frac{1}{p_{k}}\right)
$$
