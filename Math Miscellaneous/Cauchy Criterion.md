---
tags: Criterion, Cauchy, Real, Real_analysis, Series, Convergence, Math, Series, Uniform, uniform_convergence
dg-publish: true
mathLink: 
---
Subject: _Real Analysis_
Main\_Topic: _Cauchy Criterion_
Applications: _Convergent Series and Sequences_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _[[Real Series Convergence Tests]],[[Uniform and Pointwise Convergence]]_
Cont.\_ of: _None_ 
_
_
The Cauchy Criterion is a a criterion made for analyzing series for convergence without the idea of a limit. 

```ad-Definition
A sequence is **Cauchy** is for all $\epsilon>0$, there exists some number $N$ such that 
$$
|a_{m}-a_{n}|<\epsilon \quad \forall \ m,n>N
$$

A sequence converges **IF and ONLY IF** it is Cauchy and vise versa.
```

The idea of the Cauchy Sequence is from the concept of developing convergence without a limit. It stems from an idea that terms can only be so far apart after a certain point because if it converges then they will have a common limit. 

Proof on why all convergent series are Cauchy and vise versa can be seen online or in Real Analysis Textbooks. 

**Remark.**  The thing about all Cauchy Sequence converge is only for **Complete Metric Spaces**. 

##### Example 1.
Lets say we have the sequence $a_{n}=\frac{1}{n}$ such that we want $N$ to satisfy $\forall m,n > N$, $|a_{m}-a_{n}|<\epsilon$. Then we look for 
$$
\left|  \frac{1}{m} - \frac{1}{n}\right| \leq \left| \frac{1}{m} \right| + \left| \frac{1}{n} \right| = \frac{1}{m} + \frac{1}{n}<\epsilon
$$
Thus, if we take $\frac{1}{m} + \frac{1}{n} < \epsilon$, we can say that if 
$$
\frac{1}{m} < \frac{\epsilon}{2}, \quad \text{and} \quad \frac{1}{n}<\frac{\epsilon}{2},
$$
then
$$
\frac{1}{m} + \frac{1}{n} < \frac{\epsilon}{2}+ \frac{\epsilon}{2} = \epsilon
$$
So we take 
$$
n,m > \boxed{ \frac{2}{\epsilon} = N}
$$
**Final Proof:**  Let $\epsilon>0$, then we have $N=\frac{2}{\epsilon}$ such that $\forall m,n>N$, $|a_{m}-a_{n}|<\epsilon$. Thus, the sequence $a_{n}=\frac{1}{n}$ is Cauchy. Thus, this series must converge. 

---
##### Extension to Series
We know that for a series to converge, so must its sequence of partial sum $S_{N}$. By this reasoning, we can extend The Cauchy Criterion to partial sum sequences to see if a series is convergent. For example, if we know that 
$$
\sum\limits_{n=1}^{\infty}|a_{n}|
$$
converges, then for 
$$
S_{N}\equiv \sum\limits_{n=1}^{N}|a_{n}|
$$
there must be an $N$ such that $\forall m,n>0, |S_{m}-S_{n}|<\epsilon$. 

Now, we know from the [[Triangle Inequality (Euclidean Geometry)]] that 
$$
\sum\limits|a_{n}| \geq \left| \sum\limits a_{n} \right| .
$$
Thus, if 
$$
S_{2_{N}} \equiv \left|\sum\limits_{n=1}^{N}a_{n} \right|
$$
Then we can write (assuming convergence for $\sum\limits |a_{n}|$, also note that the partial sums are positive from the absolute value sign):
$$
|S_{m}-S_{n}| \leq |S_{m}|+|S_{n}| = S_{m}+S_{n} < \epsilon
$$
And since 
$$
S_{2_{m}}+S_{2_{n}} < S_{m}+S_{n}< \epsilon
$$
then there must also exist some $N$ such that $\forall m,n>0, |S_{2_{m}}-S_{2_{n}}|>\epsilon$. Thus,
$$
\left| \sum\limits_{n=1}^{\infty} a_{n} \right|
$$
must also converge! Therefore, 
$$
\sum\limits_{n=1}^{\infty} a_{n}
$$
must converge!

**Remark.**  Instead of using the two different subtraction of partial sums, we could also write 
$$
|s_{m}-s_{n}| = \left| \sum\limits_{k=n+1}^{m}a_{k} \right| < \epsilon
$$
where there exists some $N$, $\forall \ m\geq n \geq N$. 

##### Wiki Page
![[Cauchy's_convergence_test.pdf]]
