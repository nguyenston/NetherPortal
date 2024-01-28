---
title: Infinitely divisible distribution
tags:
  - Incomplete
  - Bayesian
---

An distribution $F$ is infinitely divisible iff for any natural number $n$, there exists a series of i.i.d. data $\{X_{i}\}_{i=1:n}$ such that their sum $S=\sum_{i=1}^{n}X_{i}\sim F$.

> [!Example]
> The Poisson distribution is infinitely divisible. Suppose a random variable $S\sim\mathop{\mathrm{Pois}}(\lambda_{s})$ and natural number $n>0$, the series of i.i.d. data $X_{1:n}\overset{\text{i.i.d.}}{\sim}\mathop{\mathrm{Pois}}\left(\frac{\lambda_{s}}{n}\right)$ sums up to $S$.
