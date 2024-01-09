---
tags: MachineLearning, Analysis
---

# Inner products

Given a space $\mathcal{X}$, an inner product $\langle\cdot, \cdot\rangle$ is a two-argument function that satisfies the following properties:
- Symmetry: 
$$\langle\mathbf{u},\mathbf{v}\rangle=\langle\mathbf{v},\mathbf{u}\rangle\ \forall\mathbf{u},\mathbf{v}\in\mathcal{X}$$
- Bilinearity: 
$$\langle\alpha\mathbf{u}_{1}+\beta\mathbf{u}_{2},\mathbf{v}\rangle=\alpha \langle\mathbf{u}_{1},\mathbf{v}\rangle+\beta \langle\mathbf{u}_{2},\mathbf{v}\rangle\ \forall\mathbf{u}_{1},\mathbf{u}_{2},\mathbf{v}\in\mathcal{X};\ \alpha,\beta \in\mathbb{R}$$
- Positive definiteness: 
$$\begin{align}
\langle\mathbf{u},\mathbf{u}\rangle\geq 0\ \forall\mathbf{u}\in\mathcal{X} \\
\langle\mathbf{u},\mathbf{u}\rangle=0\iff \Vert\mathbf{u}\Vert=0
\end{align}$$

# Hilbert spaces

 Hilbert spaces are inner product spaces that are [[Complete metric spaces|complete]]. Following are some examples of Hilbert spaces:
 - The vector spaces $\mathbb{R}^n$ with $\langle\mathbf{a},\mathbf{b}\rangle=\mathbf{a}^{\mathrm{T}}\mathbf{b}$
 - The space $L^{2}$ of square integrable functions (i.e. $\int f(x)^2dx<\infty$) with $\langle f,g\rangle=\int f(x)g(x)dx$ 