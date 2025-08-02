---
tags:
  - Math
  - group
  - groups
  - product
  - direct_product
  - external
dg-publish: true
mathLink:
---
Subject: _Abstract Algebra_
Main\_Topic: _External Direct Product_
Applications: _Group Theory_
Examples: _None_
Class: _Intro to Algebraic Systems_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Internal Direct Products]],[[Groups]]_
Cont.\_ of: _None_ 
_
_

One can often start with one large group and decompose it into a product of smaller groups in the same way a composite positive integer can be broken down into a product of primes. These methods will be used later to give us a simple way to construct all finite Abelian groups.

```ad-Definition
Let $G_{1},G_{2},\ldots,G_{n}$ be a collection of groups. The _external direct product_ of $G_{1},G_{2},\ldots,G_{n}$, written as $G_{1} \oplus G_{2} \oplus \ldots \oplus G_{n}$, is the set of all $n$-tuples for which the ith component is an element of $G_{i}$, and the operation is componentwise. In symbols,
$$
G_{1} \oplus G_{2} \oplus \ldots \oplus G_{n} = \{(g_{1},g_{2},\ldots,g_{n}) \vert \ g_{i} \in G_{i}\}
$$
```

where $(g_{1},g_{2},\ldots,g_{n})(g_{1}',g_{2}',\ldots,g_{n}')$ is defined to be $(g_{1}g_{1}',g_{2}g_{2}',\ldots,g_{n}g_{n}')$. It is understood that each product $g_{i}g_{i}'$ is performed with the operation of $G_{i}$. The external direct product of groups is itself a group. 

This construction is not new to linear algebra or physics. Indeed, $R^{2}=R\oplus R$ and $R^{3}=R \oplus R \oplus R$, the operation being component-wise addition. Of course, there is also scalar multiplication, but we ignore this for the time being, since we are interested only in the group structure at this point. 

##### Properties of External Direct Products
Our first theorem gives a simple method for computing the order of an element in a direct product in terms of the orders of the component pieces.

```ad-note
$|G \oplus H| = |G||H|$
```

```ad-Remember
If $H=\{(g,g,\ldots,g) | \ g \in G\}$, then $H$ is a subgroup of $G\oplus G \ldots \oplus G = G^{n}$. This is known as the _diagonal subgroup_. 
```

**Theorem 7.1**  The order of an element of a direct product of finite groups is the least common multiple of the orders of the components of the element. In symbols, 
$$
|(g_{1},g_{2},\ldots,g_{n})| = lcm{\{|g_{1}|,|g_{2}|,\ldots,|g_{n}|\}}
$$

**Proof:**  To simplify matters, we first consider the special case for which the direct product has only two factors. Let $(g_{1},g_{2})$ be an arbitrary element of $G_{1}\oplus G_{2}$. Let $s= lcm\{|g_{1}|,|g_{2}|\}$ and $t=|(g_{1},g_{2})|$. Clearly then, 
$$
(g_{1},g_{2})^{s}=(g_{1}^{s},g_{2}^{s}) = (e,e)
$$
so, by the corollary to Theorem 4.1 in [[Cyclic Groups]], $t$ must divide $s$. In particular, $t \leq s$. But $(g_{1}^{t},g_{2}^{t})=(g_{1},g_{2})^{t}=(e,e)$, and it follows, for the same reason, that both $|g_{1}|$ and $|g_{2}|$ must divide $t$. Thus, $t$ is a common multiple of $|g_{1}|$ and $|g_{2}|$; and, therefore, $s \leq t$, since $s$ is the _least_ common multiple of $|g_{1}|$ and $|g_{2}|$. Putting this information together about $s$ and $t$, we find $s=t$. We can then extend this argument for the general case. 

**Theorem 7.2**  Let $G$ and $H$ be finite cyclic groups. Then $G \oplus H$ is cyclic if and only if $|G|$ and $|H|$ are relatively prime. 

**Proof:**  Let $|G|=m$ and $|H|=n$ so that $|G \oplus H|=mn$. To prove the first half of the theorem, we assume $G\oplus H$ is cyclic and show that $m$ and $n$ are relatively prime. Since $G \oplus H$ is cyclic, there is an element $(g,h)$ in $G \oplus H$ of order $mn$. From Theorem 7.1, we obtain $mn = |(g,h)|=lcm(|g|,|h|)$. On the other hand, since $|g|$ divides $m$ and $|h|$ divides $n$ (Theorem 4.3 in [[Cyclic Groups]]), we know $lcm(|g|,|h|)$ divides $lcm(m,n)$. Since it is always true that $lcm(m,n) \leq mn$, we conclude that $lcm(m,n)=mn$ and, therefore, $gcd(m,n)=1$. 

To prove the other half of the theorem, let $G = \left<g \right>$ and $H = \left<h \right>$ and suppose that $\gcd(m,n)=1$. Then, $|(g,h)|=lcm(m,n)=mn=|G \oplus H|$ so that $(g,h)$ is a generator of $G \oplus H$. 

---
As a consequence of Theorem 7.2 and an induction argument, we obtain the following extension of Theorem 7.2.

**Corollary 1.**  An external direct product $G_{1} \oplus G_{2}\oplus \ldots \oplus G_{n}$ of finite cyclic groups is cyclic if and only if $|G_{i}|$ and $|G_{j}|$ are relatively prime when $i \neq j$. 

**Corollary 2.**  Let $m=n_{1}n_{2}\ldots n_{k}$. Then $Z_{m}$ is isomorphic to $Z_{n_{1}}\oplus Z_{n_{2}}\oplus \ldots \oplus Z_{n_{k}}$ if and only if $n_{i}$ and $n_{j}$ are relatively prime when $i \neq j$. 

By using the above results in an iterative fashion, one can express the same group (up to isomorphism) in many different forms. For example, we have 
$$
Z_{2}\oplus Z_{2} \oplus Z_{3} \oplus Z_{5} \approx Z_{2}\oplus Z_{6} \oplus Z_{5}\approx Z_{2} \oplus Z_{30}
$$

