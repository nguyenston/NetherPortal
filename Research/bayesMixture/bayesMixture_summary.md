---
tags:
  - bayesMixture
title: Summary
---
# Thesis
In models like Finite mixture models (FMM) or Negative matrix factorization (NMF), finding the number of mixture components (or features) $K$ is a non-trivial task. This work is intended to develop an automated algorithm with minimal tuning, while being robust to model specification for this task.

# Finite mixture model and structurally aware model selection

The paper [[@liRobustStructurallyAware]] suggested the following

## Model definition

Let parameters $\pi^{(K)}\in\Delta_{K}$, $\phi_{1:K}\in\Phi^{K}$, and model $F:\Phi\to\mathcal{P}(\mathcal{X})$. We have data $X_{N}=x_{1:N}\in\mathcal{X}^{N}$ generated through the following process:
$$
\begin{align}
z_{n}&\sim\mathop{\mathrm{Categorical}}\left(\pi^{(K)}\right)&\text{for}\ n=1:N \\
x_{n}|z_{n}&\sim F(\phi_{z_{n}})&\text{for}\ n=1:N
\end{align}
$$

## Model selection

Let $\theta^{(K)}=\left(\pi^{(K)},\phi_{1:K}\right)$, we define the penalized structurally aware loss:
$$
\mathcal{R}^{\rho,\lambda}\left(\theta^{(K)};z_{1:N}, x_{1:N}\right)=\sum^{K}_{k=1}\left\lvert X^{(k)}(z_{1:N})\right\rvert
\mathop{\mathrm{max}}\left(0,\hat{\mathcal{D}}\left(X^{{(k)}}(z_{1:N}), F(\phi_k)\right)-\rho\right)+\lambda K
$$
Then we follow the procedure below

```pseudo
\begin{algorithm}
\caption{Model selection}
\begin{algorithmic}
\Input data $x_{1:N}$, maximum number of components allowed $K_{\mathrm{max}}$, and penalty parameter $\lambda$
\For{$K=1,\dots,K_{\mathrm{max}}$}
    \State Estimate $\theta^{(K)}$
    \State Sample $z_{1:N}$ from $\mathrm{P}(z_{1:N}\vert \theta^{(K)},x_{1:N})$
\EndFor
\State Determine an appropriate value for $\rho$
\State Compute $\hat{K}=\mathrm{argmin}_K\ \mathcal{R}^{\rho,\lambda}\left(\theta^{(K)};z_{1:N},x_{1:N}\right)$
\Return $\theta^{(\hat{K})}$
\end{algorithmic}
\end{algorithm}
```

# Non-negative matrix factorization

We want to extend the method above to work with NMF, as there are many similarities between FMM and NMF. However, there are also many crucial differences

## Model definition

From literature, the NMF model is defined along the line of
$$
X\sim F\left(W^{(K)}H^{(K)}\right)
$$
where $X\in (\mathcal{X}_{D})^{N}$ is the $D\times N$ data matrix, $W^{(K)}\in(\Delta_{D})^{K}$ is the $D\times K$ matrix of signatures/features, $H^{(K)}\in\mathbb{R}^{K\times N}_{>0}$ is the matrix of exposure/coefficients, and $F:\mathbb{R}^{D\times N}\to\mathcal{P}\left((\mathcal{X}_{D})^{N}\right)$ is the assumed model. In this definition, $W^{(K)}$ and $H^{(K)}$ are parameters.

In order to make NMF more of a generalization of FMM, we propose the following definition. Let parameters $\pi^{(K)}\in\Pi^{(K)}$, $W^{(K)}\in(\Delta_{D})^{K}$, and models $G:\Pi^{(K)}\to\mathcal{P}\left(\mathbb{R}^{K}_{>0}\right)$, $F:\mathbb{R}^{D}\to\mathcal{P}(\mathcal{X}_{D})$. We generate the data $X_{N}=x_{1:N}\in(\mathcal{X}_{D})^{N}$ through the process
$$
\begin{align}
h^{(K)}_{i}&\sim G\left(\pi^{(K)}\right)&\text{for}\ i=1:n \\
x_{i}|h^{(K)}_{i}&\sim F\left(W^{(K)}h^{(K)}_{i}\right)&\text{for}\ i=1:n
\end{align}
$$

## Research problem

* Unlike FMM, NMF doesn't seem to have a clearly defined concept of "misspecification"
    * [[@pelizzolaModelSelectionRobust2023]], model misspecification is touched upon as the overdispersion of data, leading to an overestimation of the rank $K$ when the assumed model $F$ is Poisson.