---
tags:
  - Analysis
  - Incomplete
title: Complete metric spaces
---

Intuitively, a metric space is complete if there are no "points missing" from it.

# Cauchy sequence

A sequence $\left\{x_{i}\right\}$ in a [[metric_spaces|metric space]] $(X,d)$ is called Cauchy if for any arbitrarily small $\epsilon>0$, there exists a large enough $N$ such that for all $m,n>N$,
$$
d(x_{m},x_{n})<\epsilon.
$$
> [!tip] Intuition
> A sequence that converges to some value. More precisely, a sequence whose tail is contained within any arbitrarily small region.
> ![[cauchy_sequence.svg]]

# Complete space

A metric space $(X,d)$ is complete if every Cauchy sequence of points in $X$ has a limit that is also in $X$.

# Completion

For any incomplete metric space $(M,d)$, a complete counterpart $(\overline{M},\overline{d})$ can be constructed as the set of [[equivalence_relation#Equivalent class|equivalent classes]] of Cauchy sequences in $M$. $M$ is also a [[Dense subset|dense subset]] in $\overline{M}$.


