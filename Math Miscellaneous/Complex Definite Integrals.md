---
tags: complex, Math, contour, definite, definite_integrals, integrals
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
Closely\_Related\_To: _[[Complex Derivatives]],[[Complex Contours]],[[Contour Integrals]]_
Cont.\_ of: _None_ 
_
_
If we have a function $w(t)$ that is complex-valued and is written as 
$$
w(t)=u(t)+iv(t),
$$
where $u$ and $v$ are real-valued, we can write the _definite integral_ of $w(t)$ over an interval $a\leq t\leq b$ as 
$$
\boxed{\int\limits_{a}^{b}w(t) \ dt = \int\limits_{a}^{b}u(t) \ dt + i \int\limits_{a}^{b}v(t) \ dt}
$$
provided that the individual integrals on the right exist. This is the same way we decompose a multivariable vector integral notice the similarities we can draw from this.

```ad-note
The existence of the integrals of $u$ and $v$ are ensured if those functions are **piecewise continuous** on the interval $a\leq t\leq b$. Such a function is continuous everywhere in the stated interval except possibly for a finite number of points where, although discontinuous, has one-sided limits. 
```

```ad-Definition
Definition of **Piecewise Continuity**:

continuous everywhere in the stated interval except possibly for a finite number of points where, although discontinuous, has one-sided limits. 
```

**Remark.**  Integrals exist for closed intervals. If we have an open interval, we have an improper integral which we need to take the limit of as one or both of the bounds approaches the boundary of our open interval. If a function is piecewise continuous, then it has one sided limits which allow us to take the limit of the integral to these bounds. Thus, to have an improper integral that we can find a solution to, we need the functions to be piecewise continuous. 

The integration rules for exchanging limits, etc. from real variable calculus all carry over.

### Fundamental Theorem of Calculus on Complex Plane 
The _Fundamental Theorem of Calculus_, involving antiderivatives, can, moreover, be extended to apply to these complex integrals. Suppose that we have the functions 
$$
w(t)=u(t)+iv(t), \quad \text{and} \quad W(t)=U(t)+iV(t)
$$
which are continuous on the interval $a\leq t\leq b$. If $W'(t)=w(t)$ on this interval, then $U'(t)=u(t)$ and $V'(t)=v(t)$. Hence, we can write 
$$
\int\limits_{a}^{b}w(t) \ dt = U(t)\rvert_{a}^{b} + iV(t)\rvert_{a}^{b}= [U(b)-iV(b)]-[U(a)+iV(a)]
$$
That is,
$$
\int\limits_{a}^{b}w(t) \ dt = \left. W(t)\right\rvert_{a}^{b}
$$

**Remark.**  As stated in [[Complex Derivatives]] that the Mean Value Theorem does not carry over to the complex plane, it is worth noting that the Mean Value Theorem for integrals **Does NOT** carry over either! Once again this is a result of the periodicity and multi-valued nature of complex numbers.

```ad-note
Another thing work noting is that for scalar [[Line Integrals]], the path direction does not matter. For contour integrals, the path direction **DOES MATTTER** in the same way it does for vector [[Line Integrals]] (one direction is negative integral of opposite direction). Weird right?
```

