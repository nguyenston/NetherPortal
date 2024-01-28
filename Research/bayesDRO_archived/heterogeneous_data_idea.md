---
id: heterogeneous_data_idea
tags: []
title: Heterogeneous data idea
---

# Pitch

Under the context of [[defining_robustness#Worst case sub-population|worst case sub population]], we want to find a one size fits all solution that caters to all instances of the data up to a certain degree. What if we go the other direction and infer solutions that **specialize** towards certain sub-populations. For example, consider the following linear regression problem and potential posterior for the slope coefficient:
$$
y\sim \mathcal{N}(\boldsymbol{\beta}^{\mathrm{T}}\mathbf{z},\sigma^2)
$$
![[heterogenous_linear_regression.svg|90%]]
![[cater_vs_noncater.svg|90%]]
The specialized posterior tries to come up with solutions that cater best to one of the two sup-population of the data instead of trying to get acceptable performance for all of them at once. With this maybe we can detect multi-modality or detect outliers. This might al signal that the model we are using cannot capture the dynamics of the system at hand.

# Alternative divergences/modifying loss function

In the context of regression, we want to infer parameters $\theta$ such that the parameterized distribution $P_{\theta}$ matches with the true data generating distribution $P_{\star}$. For inference, the posterior $Q_{\star}$ over $\theta$ is found through solving the following:

A generalization of the formulation above:
$$
Q_{\star}=\mathop{\mathrm{argmin}}_{Q}\ \mathbb{E}_{\theta \sim Q}\left\{\mathbb{E}_{x\sim P_{\star}}[L(\theta,x)]\right\}+D_{KL}(Q|Q_{0}).
$$
When $L(\theta,x)=-\log[P_{\theta}(x)]$,

$$
Q_{\star}=\mathop{\mathrm{argmin}}_{Q}\ \mathbb{E}_{\theta \sim Q}[D_{KL}(P_{\star }|P_{\theta})]+D_{KL}(Q|Q_{0}),
$$
which is Bayes rules. If we take a look at the negative log likelihood,
![[log_loss.svg|90%]]
we see that it's slope remains significant on both ends, meaning a perturbation in $\theta$ would result in meaningful change in the model's performance across all samples in $X$. Now let's consider an alternative loss function:
![[alt_loss.svg|90%]]
Now, when $\theta$ is perturbed, as this loss function is flat on the ends, only samples in the middle zone are affected meaningfully. This locality results in the specialization behavior described above.

# Neighborhood set and polarization

Whether or not perturbing $P_{\star}$ within a neighborhood set directly contributes to this effect is yet to be investigated. However, combined with loss functions with the characteristic described above, an adversarial perturbation to $P_{\star}$ would affect solutions that try to cater to everyone the most, since these has the most samples lying within the meaningful zone.

# Experimental behavior

## Asymptotic exponential domination

Using $L(\theta,x)=nD_{\beta}(P_{X},P_{\theta})+C$ yields the conjectured behavior for small sample size. However, as the number of samples goes to infinity, the posterior converges to a single peak. This is due to the exponential nature of the Gibbs posterior. Consider a hypothetical "counting loss", where good samples have a loss of $0$ and bad samples have a loss of $1$, and suppose for a dataset of size $n$, two sets of parameters $\theta_{1}$ and $\theta_{2}$ with corresponding losses $l_{1}$ and $l_{2}$ such that
$$
l_{1}=l_{2}+c.
$$
That means their corresponding posterior density will have the following relationship:
$$
e^{-l_{1}}=e^{-c}e^{-l_{2}}.
$$
Consider the sample size of $kn$ instead, we have:
$$
e^{-kl_{1}}=e^{-kc}e^{-kl_{2}}.
$$
As the number of the sample size grows, the ratio $e^{-kc}$ shrinks to zero and the parameter with the lower loss, $\theta_{2}$, would dominate.

### Using a different posterior

As an alternative to the Gibbs posterior
$$
Q_{\star}(\theta)\propto e^{-L(\theta)}Q_{0}(\theta)
$$
which has an exponential, we use a similar looking function
$$
Q_{\star}(\theta)\propto \log(1+e^{-L(\theta)+nm})Q_{0}(\theta)
$$
The function is called softplus and it scales linearly as $x\to \infty$, this addresses the problem of the asymptotic domination of the best solution. Observe that this posterior is no longer invariant to scalar translation of the loss (i.e. using $L(\theta)+C$ would yield a different posterior from  using $L(\theta)$), this scalar translation can act as a breakpoint to select for only solutions with high enough performance.
![[softplus.svg|90%]]
* Justification
    * What optimization problem is this the result of?
    * Good statistical property 

#### First principle justification:

The posterior is the result of the optimization problem
$$
\mathop{\mathrm{inf}}_{Q}\ \mathbb{E}_{\theta \sim Q}\left\{\log \log\left[1+e^{L(\theta)+mn}\right]\right\}+D_{KL}(Q|Q_{0})
$$
We have
$$
\log \log \left[1+e^{L(\theta)}\right]= \begin{cases}
\log(L(\theta))+c\text{ as }L(\theta)\to \infty\\
cL(\theta)\text{ as }L(\theta)\to -\infty
\end{cases}
$$

**Not very satisfying, nor intuitive**
# Questions

# Take a step back

High priority project
Are there aspect of this that I like?
What are the kind of problems that I am interested in?

Mixture model -> how many components?
Robust model selection

