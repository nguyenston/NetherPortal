---
tags:
  - SetTheory
  - Probability
  - Incomplete
title: Set-theoretic limit
---

# Definitions

Let $\{A_{n}\}$ be a sequence of sets, then we have these definitions:
$$
\liminf_{n\to \infty}A_{n}=\bigcup_{n=1}^{\infty}\bigcap_{j=n}^{\infty} A_{j},
$$
$$
\limsup_{n\to \infty}A_{n}=\bigcap_{n=1}^{\infty}\bigcup_{j=n}^{\infty}A_{j}.
$$
If $\liminf A_{n}=\limsup A_{n}=A_{\infty}$, then we define $\lim_{n\to \infty} A_{n}=A_{\infty}$.

# Interpretation

* If $x\in \liminf A_{n}$, then we say $x$ is in all but finitely many $A_{n}$
* If $x\in \limsup A_{n}$, then we say $x$ is in infinitely many $A_{n}$

# Example

Let
$$
A_{n}=\left\{\begin{align}
&X\ \text{if $n$ is even},\\
&Y\ \text{if $n$ is odd}.
\end{align}\right.
$$
Then
$$
\liminf A_{n}=X\cap Y
$$
$$
\limsup A_{n}=X\cup Y
$$

