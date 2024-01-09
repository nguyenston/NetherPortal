---
Tags: Probability
---

An *estimator*  is a **rule** to calculate an *estimate*, an **approximation**, to some **quantity of interests**, given **observed data**.

# Definition

Suppose a parameter $\theta \in\Theta$ needs to be estimated using data from the sample space $\mathcal{X}$. Then the estimator $\hat{\theta}$  is a function that maps $\mathcal{X}\to \Theta$. We denote $x\in\mathcal{X}$ as the observed data and capital letters $X,Y$ as the random variable corresponding to $x$. 

# Relevant properties

## Error

$$
e(\hat{\theta},x)=\hat{\theta}(x)-\theta
$$

## Mean squared error (MSE)

$$
\mathrm{MSE}(\hat{\theta})=\mathbb{E}_{X}\left\{\left[\hat{\theta}(X)-\theta\right]^2 \right\}
$$

## Sampling deviation

$$
d(\hat{\theta},x)=\hat{\theta}(x)-\mathbb{E}_{X}\left[\hat{\theta}(X)\right] 
$$

## Variance


$$
\mathrm{Var}(\hat{\theta})=\mathbb{E}_{Y}\left\{\left[\hat{\theta}(Y)-\mathbb{E}_{X}\left\{\hat{\theta}(X)\right\}\right]^2\right\} 
$$

## Bias 

$$B(\hat{\theta})=\mathbb{E}_{X}\left[\hat{\theta}(X)\right]-\theta$$
* If $B(\hat{\theta})=0$, then $\hat{\theta}$ is unbiased
* If $B(\hat{\theta}\neq 0)$, then $\hat{\theta}$ is biased

## Consistency

Suppose we have a series of estimators $\{\hat{\theta}_{n}\}$, this series is called consistent if it [[Convergence of random variables#In probability|converges in probability]] to the quantity being estimated:
$$
\lim_{n\to \infty} \mathrm{Pr}(|\hat{\theta}_{n}-\theta|<\epsilon)=1\ \forall \epsilon>0.
$$
The definition above might be called weak consistency. The series is strongly consistent when it [[Convergence of random variables#Almost surely|converges almost surely]] to the quantity being estimated.

> [!tip] Intuition
> A series of estimators is consistent if as $n\to \infty$, the estimator becomes more and more concentrated around the quantity being estemated.

# Example

Here is an example to illustrate bias vs consistency. Consider the series $\{X_{n}\}\overset{\text{i.i.d.}}{\sim}\mathcal{N}(\mu,\sigma^2)$.

## Unbiased but not consistent

Consider $X_{n}$ as a family of estimators to $\mu$. These estimators are unbiased as $\mathbb{E}(X_{n})=\mu$ for any $n$. However, the series is not consistent, as $\lim_{n\to \infty}\mathrm{Var}(X_{n})=\sigma^2\neq 0$, meaning $X_{n}\overset{p}{\not\to}\mu$.

## Biased but consistent

Consider $\hat{\sigma}_{n}^2=\frac{1}{n}\sum^n_{i=1}(X_{i}-\overline{X}_{n})^2$, where $\overline{X}_{n}=\frac{1}{n}\sum^n_{i=1}X_{i}$ is the sample mean. We have
$$
\mathbb{E}(\hat{\sigma}_{n}^2)=\frac{n-1}{n}\sigma^2,
$$
meaning that the estimator is biased for any finite $n$. However,
$$
\mathrm{Var}(\hat{\sigma}_{n}^2)=2\sigma^4 \frac{n-1}{n^2}.
$$
From these facts, we can informally say that the estimator is become more and more concentrated around $\sigma^2$, meaning this series of estimators is consistent.

> [!warning] Note
> Although this series of estimators is unbiased for any finite $n$, it is asymptotically unbiased. A series of estimators that is asymptotically biased **cannot** be consistent.

## Both unbiased and consistent

The sample mean $\overline{X}_{n}$ is a consistent series of unbiased estimators of $\mu$. Because
$$
\mathbb{E}(\overline{X}_{n})=\mu,
$$
and
$$
\mathrm{Var}(\overline{X}_{n})=\frac{\sigma^2}{n}.
$$
