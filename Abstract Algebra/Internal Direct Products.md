---
tags:
  - Math
  - product
  - direct_product
  - Internal
  - group
  - groups
  - internal_product
dg-publish: true
mathLink:
---
Subject: _Abstract  Algebra_
Main\_Topic: _Internal Direct Products_
Applications: _Group Theory_
Examples: _None_
Class: _Intro to Abstract Algebra_
Exam: _Exam 1_
Textbook: _[[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]_
Closely\_Related\_To: _[[Groups]],[[External Direct Product]]_
Cont.\_ of: _None_ 
_
_

As we have seen in [[External Direct Product]], there is a way to put groups together into a larger group. It would also be quite useful to reverse this process, that is, to be able to start with a large group and break it down into a product of smaller groups. To this end, suppose that $H$ and $K$ are subgroups of some group $G$. We define the set $HK = \{hk \vert \ h \in H, \ k \in K\}$. 

**Remark.**  We should be careful not to assume that the set $HK$ is a subgroup of $G$. 

```ad-Definition
Let $H$ and $K$ be subgroups of a group $G$. We say that $G$ is the **internal direct product** of $H$ and $K$ and write $G = H \times K$ if 
1. $G = HK$
2. $hk = kh$ for all $h \in H$, $k \in K$
3. $H \cap K = \{e\}$
```

We want to call $G$ the internal direct product of $H$ and $K$ if $H$ and $K$ are subgroups of $G$, and $G$ is naturally isomorphic to the external direct product of $H$ and $K$. one forms the internal direct product by _starting_ with a group $G$ and then proceeding to produce two subgroups $H$ and $K$ within $G$, such that $G$ is _isomorphic_ to the [[External Direct Product]] of $H$ and $K$. (The three conditions ensure that this is the case, see Theorem 8.1 for more info). On the other hand, one forms an external direct product by _starting_ with two groups $H$ and $K$, related or not, and proceeding to product the larger group $H \oplus K$. The difference between the two products is that the internal direct product can be formed within $G$ itself, using subgroups of $G$ and the operation of $G$, while the external direct product can be formed with totally unrelated groups by creating a net set and a new operation. 

![[Pasted image 20230920130854.png|center]]

Perhaps the following analogy with integers is useful in clarifying the distinction between the two products of groups. Just as one may take any finite collection of integers and form their product, one may also take any collection of groups and form their external direct product. Conversely, just as one may start with a particular integer and express it as a product of certain divisors, one may be able to start with a particular group and factor it as an internal direct product of certain subgroups. 

```ad-warning
Be extremely cautious about the necessity of having all three conditions of the definition of the internal direct product satisfied to ensure that $HK \approx H \oplus K$. 
```

A group $G$ can also be the internal direct product of a collection of subgroups as well.

```ad-Definition
Let $H_{1},H_{2},\ldots,H_{n}$ be subgroups of $G$. We say $G$ is the _internal direct product_ of $H_{1},H_{2},
\ldots,H_n$ and write $G=H_{1}\times H_{2} \times \ldots \times H_{n}$, if 
1. $G=H_{1}H_{2} \ldots H_{n} = \{h_{1}h_{2}\ldots h_{n} \vert \ h_{i} \in H_{i}\}$ 
2. $h_{i}h_{j} = h_{j}h_{i}$ for all $h_{i} \in H_{i}$ and $h_{j} \in H_{j}$ with $i \neq j$
3. $(H_{1}H_{2}\ldots H_{i}) \cap H_{i+1}=\{e\}$ for $i=1,2,\ldots,n-1$
```

This definition is somewhat more complicated than the one given for two subgroups. The reason for why we want elements from different components to commute is quite simple: we want the internal direct product to be isomorphic to the external direct product. As the next theorem shows, the three conditions in the definition of internal direct product were chosen to ensure that this same property holds.

**Theorem 8.1**  If a group $G$ is the internal direct product of subgroups $H_{1},H_{2},\ldots,H_{n}$, then $G$ is isomorphic to the external direct product of $H_{1},H_{2},\ldots,H_{n}$. In other words $H_{1}\times H_{2} \ldots \times H_{n} \approx H_{1} \oplus H_{2} \ldots \oplus H_{3}$. 

**Proof:**  The proof for this theorem can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]]. 

##### The Group of Units Modulo $n$ as an Internal and External Direct Product 

The $U$-groups provide a convenient way to illustrate the preceding ideas and to clarify the distinction between internal and external direct products. We first introduce some notation. If $k$ is a divisor of $n$, let 
$$
U_{k}(n) = \{x \in U(n) \vert \ x=1 \mod k\}
$$
It can be readily shown that $U_{k}(n)$ is indeed a subgroup of $U(n)$. 

**Theorem 8.2**  Suppose that $s$ and $t$ are relatively prime. Then $U(st)$ is the internal direct product of $U_{s}(st)$ and $U_{t}(st)$, and $U(st)$ is isomorphic to the external direct product of $U(s)$ and $U(t)$. Moreover, $U_{s}(st)$ is isomorphic to $U(t)$, and $U_{t}(st)$ is isomorphic to $U(s)$. In short, 
$$
U(st) = U_{s}(st) \times U_{t}(st) \approx U(t) \oplus U(s).
$$

**Proof:**  This theorem can be seen in [[Joseph A. Gallian - Contemporary abstract algebra-Houghton Mifflin Harcourt (HMH) (1989) (1).pdf|abstract algebra textbook]] is proven in the paper "Factoring Groups of Integers Modulo n" by J. A. Gallian and G. Rusin. 

**Corollary.**  Let $m=n_{1}n_{2}\ldots n_{k}$ where $\gcd(n_{i},n_{j})=1$ for $i \neq j$. Then 
$$
U(m) = U_{\frac{m}{n_{1}}(m)}\times U_{\frac{m}{n_{2}}(m)} \times \ldots \times U_{\frac{m}{n_{k}}(m)}\approx U(n_{1}) \oplus U(n_{2}) \oplus \ldots \oplus U(n_{k})
$$

