---
id: dual_formulation_for_wasserstein_neighborhood_set
tags: []
title: Dual formulation for Wasserstein neighborhood set
---

With definitions defined [[summary#Framework description|here]], we have the following formulations:
$$
Q_{\star}=\mathop{\mathrm{argmin}}_{Q\in\mathcal{Q}}\ \mathbb{E}_{\theta \sim Q}\left\{L_{DR}(\theta,X)\right\} +\alpha D_{KL}(Q|Q_{0}).\tag{MAIN}
$$
$$
L_{DR}(\theta,X):=\mathop{\mathrm{sup}}_{P\in\Omega(P_{X})}\ \mathbb{E}_{x\sim P}[L(\theta,x)]
$$
Suppose we choose the neighborhood set
$$
\Omega(P_{X})=\left\{P:W^p_{d}(P,P_{X})\leq \delta^{1/p}\right\},
$$
where $W_{d}^{p}$ is the Wasserstein p-distance defined [[relevant_divergences#Wasserstein p-Distance|here]], we can rewrite $L_{DR}$ as follows:
$$
\begin{alignat}{2}
L_{DR}(\theta,X)&&=\mathop{\mathrm{sup}}_{\gamma}\ &\mathbb{E}_{(x,\cdot)\sim \gamma}[L(\theta,x)]\\
&&\text{s.t.}\ &\int_{\mathcal{X}}\gamma(\cdot,dx')=P_{X}(\cdot)\\
&&&\mathbb{E}_{(x,x')\sim \gamma}[d(x,x')^p]\leq \delta.
\end{alignat}\tag{PRIMAL}
$$
Using duality, we can reformulate $L_{DR}$:
$$
L_{DR}(\theta,X)=\mathop{\mathrm{inf}}_{\lambda \geq 0}\ \lambda \delta+\mathbb{E}_{x\sim P_{X}}\left[\mathop{\mathrm{sup}}_{x'\in \mathcal{X}}\ L(\theta,x')-\lambda d(x,x')^p\right].\tag{DUAL}
$$
This is more tractable since the two optimization problems are over finite-dimensional spaces instead of over the space of distributions.
> [!warning] Note
> * Choose the metric $d$ such that $$\limsup_{d(x,x')\to\infty} \frac{L(\theta,x')-L(\theta,x)}{d(x,x')^p}<\infty\ \forall\theta.$$
> * It is shown that the optima $\lambda$ satisfies $$\lambda \geq\limsup_{d(x,x')\to\infty} \frac{L(\theta,x')-L(\theta,x)}{d(x,x')^p}\ \text{for any }\theta.$$

