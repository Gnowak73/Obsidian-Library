---
tags: tensors, notation, examples, Math, Calculus
dg-publish: true
mathLink: 
---
Subject: _Tensor Calculus_
Main\_Topic: _Tensor Examples_
Applications: _None_
Examples: _None_
Class: _None_
Exam: _None_
Textbook: _None_
Closely\_Related\_To: _None_
Cont.\_ of: _None_ 
_
_

We shall consider examples rather than generalities to show how tensors work. 

##### Rank 3, Twice Contravariant, Once Covariant
A tensor of the third rank, twice contravariant, once covariant, is locally of the form 
$$
A = \pmb{\partial}_{i}\otimes \pmb{\partial}_{j} \ A^{ij}_{k} \otimes du^{k}
$$
It is a trilinear function of pairs of covectors $\alpha = a_{i}du^{i}, \beta =b_{j}du^{j}$, and a single vector $\pmb{v}=\pmb{\partial}_{k}v^{k}$, 
$$
A(\alpha,\beta,\pmb{v}) = a_{i}b_{j}A^{ij}_{k}v^{k}
$$
summed, of course, on all indices. Its components transform as 
$$
A'^{ef}_{g} = \left(\frac{\partial u'^{f}}{\partial u^{i}}\right)\left(\frac{\partial u'^{f}}{\partial u^{j}}\right)A^{ij}_{k}  \left(\frac{\partial u^{k}}{\partial u'^{g}}\right)
$$

##### Linear Transformation
A **linear transformation** is a second rank ("mixed") tensor $P = \pmb{\partial}_{i}P^{i}_{j}\otimes du^{j}$. Rather than thinking of this as a real valued bilinear function of a covector and a vector, we usually consider it as a _linear function taking vectors into vectors_ (called a vector valued 1-form).
$$
P(\pmb{v}) = [\pmb{\partial}_{i}P^{i}_{j} \otimes du^{j}](\pmb{v}) \equiv \pmb{\partial}_{i} P^{i}_{j}\{du^{j}(\pmb{v})\} = \pmb{\partial}_{i}P^{i}_{j}v^{i}
$$
i.e., the usually 
$$
[P(\pmb{v})]^{i} = P^{i}_{j}v^{j}
$$
Under a coordinate change, $(P^{i}_{j})$ transforms as $P' = \left(\frac{\partial u'}{\partial u}\right)P\left(\frac{\partial u'}{\partial u}\right)^{-1}$, as usual. If we contract we obtain a scalar (invariant), $\text{tr} \ P \equiv P^{i}_{i}$, the **trace** of $P$. $\text{tr} \ P' = \text{tr} \ P\left(\frac{\partial u'}{\partial u}\right)^{-1}\left(\frac{\partial u'}{\partial u}\right)=\text{tr} \ P$. 

```ad-warning
If we have a twice covariant tensor $G$ (a "bilinear" form), for example, a metric $(g_{ij})$, then $\sum\limits_{k} g_{kk}$ is _not_ a scalar, although it is the trace of the matrix. This is because the transformation law, which can be seen in [[Riemannian Metrics]]. 
```
