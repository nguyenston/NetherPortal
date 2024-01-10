---
tags:
  - Analysis
  - MachineLearning
  - Incomplete
title: Reproducing kernel Hilbert spaces
---

# Positive definite kernel

The symmetric function $k:\mathcal{X}\times \mathcal{X}\to \mathbb{R}$ is a positive definite kernel if
$$
\sum_{i=1}^n\sum_{j=1}^nc_{i}c_{j}k(x_{i},x_{j})\geq 0
$$
for any $c_{i}\in\mathbb{R},x_{i}\in\mathcal{X},n\in\mathbb{N^*}$ .

In the case where $\mathcal{X}$ is a discrete finite set $\{x_{i}\}_{i=1:n}$, define symmetric matrix $\mathbf{K}\in\mathbb{R}^{n\times n}$ such that $K_{ij}=k(x_{i},x_{j})$, this definition is equivalent to positive definiteness of matrices:
$$
\mathbf{c}^{\mathrm{T}}\mathbf{K}\mathbf{c}\geq 0
$$
for any vector $\mathbf{c}\in\mathbb{R}^n$.

# Reproducing kernel Hilbert space

![[RKHS1.svg|90%]] 
<figcaption>
Fig. Relationships between RKHS and related spaces, sets with the same color share an <a href="Equivalence relation.md" class="internal-link">equivalence relation</a>
</figcaption>

A reproducing kernel Hilbert space $\mathcal{H}_{k}$ with kernel $k$ is a [[inner_products_and_hilbert_spaces#Hilbert spaces|Hilbert space]] equipped with the [[inner_products_and_hilbert_spaces#Inner products|inner product]] $\langle\cdot,\cdot\rangle_{\mathcal{H}_{k}}$  that satisfies
* $\forall x\in\mathcal{X},k(\cdot,x)\in\mathcal{H}_{k}$
* $\forall x\in\mathcal{X},\forall f\in\mathcal{H}_{k},\langle f,k(\cdot,x)\rangle_{\mathcal{H}_{k}}=f(x)$
The latter being called the reproducing property.

> [!note] Intuition on the reproducing property (for **general** RKHS)
> Any functions $f,g$ in the RKHS $\mathcal{H}_{k}$ can be written as
> $$
> f=\sum_{i}a_{i}k(\cdot,x_{i})\quad,\quad g=\sum_{j}b_{j}k(\cdot,y_{j}).
> $$
> The inner product on $\mathcal{H}_{k}$ is defined as
> $$
> \langle f,g\rangle_{\mathcal{H_{k}}}=\sum_{i}\sum_{j}a_{i}b_{j}k(x_{i},y_{j}).
> $$
> The reproducing property comes as a natural consequence:
> $$
> \langle f,k(\cdot,y)\rangle=\sum_{i}a_{i}k(x_{i},y)=f(y).
> $$

# Examples

Let $\mathcal{X}=\mathbb{R}^2$, $\mathbf{x}=\begin{bmatrix} x_{1}\\ x_{2}\end{bmatrix}\in \mathcal{X}$. We have the feature map:
$$
\phi(\mathbf{x})=\begin{bmatrix}
x_{1}^2\\x_{2}^2\\ \sqrt{2} x_{1}x_{2}
\end{bmatrix}.
$$
This feature map is **one of many** that is associated with the kernel
$$
\begin{align}
k(\mathbf{x},\mathbf{y})&=\phi(\mathbf{x})^{\mathrm{T}}\phi(\mathbf{y}) \\
&= (x_{1}y_{1})^2+(x_{2}y_{2})^2+2x_{1}y_{1}x_{2}y_{2} \\
&= (\mathbf{x}^{\mathrm{T}}\mathbf{y})^2.
\end{align}
$$
The **canonical feature map** for this RKHS is $\Phi(\mathbf{x})=\mathbf{y}\mapsto(\mathbf{x}^{\mathrm{T}}\mathbf{y})^2$, note that the RHS is a function.

