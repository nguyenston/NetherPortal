---
tags:
  - Bayesian
  - RobustOptimization
  - MachineLearning
title: Summary
---

# Thesis

A comprehensive framework to formalize trustworthy inference and learning. We propose an optimization formulation that can be easily modified and extended to yield various existing frameworks. We also explore the capacity to do uncertainty quantification.

# Framework description

Let $\Theta$ the parameter space, $\mathcal{X}$ the space of observations, and $L:\Theta \times \mathcal{X}\to \mathbb{R}$ the loss function. Given any [[measurable_space|measurable space]] $(S,\mathcal{B})$ , let $\mathcal{P}(S)$ denote the space of [[probability_space|probability measures]] on $S$. Given the data $X=\left\{x_{i}\right\}_{1:n}\in\mathcal{X}^n$, let $P_{X}=\frac{1}{n}\sum_{i=1}^n\delta_{x_{i}}\in\mathcal{P}(\mathcal{X})$ denote the empirical data distribution. For any $P\in\mathcal{P}(\mathcal{X})$, define the neighborhood set $\Omega(P)\subset \mathcal{P}(\mathcal{X})$, which contains distributions similar to P. In addition, let $\mathcal{Q}\subseteq \mathcal{P}(\Theta)$ be the set of feasible posteriors for the parameter.

The basic framework solves the constrained minimax optimization
$$
Q_{\star}=\mathop{\mathrm{argmin}}_{Q\in\mathcal{Q}}\ \mathbb{E}_{\theta \sim Q}\left\{\mathop{\mathrm{sup}}_{P\in\Omega(P_{X})}\ \mathbb{E}_{x\sim P}[L(\theta,x)]\right\} +\alpha D_{KL}(Q|Q_{0}).\tag{MAIN}
$$
For the case where $\mathcal{Q}=\mathcal{P}(\Theta)$, the posterior $Q_{\star}$ is available in closed form
$$
Q_{\star}(d\theta)\propto \exp[-\alpha^{-1}L_{DR}(\theta,X)]Q_{0}(d\theta),\tag{GIBBS}
$$
where $L_{DR}(\theta,X):=\mathop{\mathrm{sup}}_{P\in\Omega(P_{X})}\ \mathbb{E}_{x\sim P}[L(\theta,x)]$. By using different $\alpha$, $\Omega$, and $L$ we can recover various existing Bayesian inference framework. 

# Examples

## Case 1: $\Omega(P_{X})=\{P_{X}\},L(\theta,x)=-n\log P(x|\theta)$

The choice of $\Omega$ and $L$ in this case is such that
$$
L_{DR}(\theta,X)=nD_{KL}(P_{X}|P_{\theta})+C,
$$
where $P_{\theta}(x)=P(x|\theta)$ and $C$ is a constant with respect to $\theta$.  We have 
$$
L_{DR}(\theta,X)=n\mathbb{E}_{x\sim P_{X}}[\log P(x|\theta)]=\log P(X|\theta)
$$
which yields the following posterior:
$$
Q_{\star}(d\theta)\propto P(X|\theta)^\alpha Q_{0}(d\theta).\tag{GBAYES}
$$
One can recognize this as general Bayesian inference.

> [!tip] Remark
> If we relax $\Omega$ such that is is no longer a singleton, we notice that 
> $$
> L_{DR}(\theta,X)\neq \mathop{\mathrm{sup}}_{P\in\Omega(P_{X})}nD_{KL}(P|P_{\theta})+C.
> $$
> Would it be better to consider optimizing over this LHS quantity instead of the framework's $L_{DR}$ formulation?

## Case 2: $\alpha\to 0$

In the limit of $\alpha\to 0$, the posterior $Q_{\star}$ will degenerate into a singleton $\delta$ distribution. Because of that, (MAIN) is reduced to
$$
\theta_{\star}=\mathop{\mathrm{argmin}}_{\theta\in\Theta}\mathop{\mathrm{sup}}_{P\in\Omega(P_{X})}\mathbb{E}_{x\sim P}[L(\theta,x)],\tag{DRO}
$$
which is the set up for distributionally robust optimization.

# This direction is kind of a loss