---
tags: Bayesian, RobustOptimization, MachineLearning
---
# Thesis

A comprehensive framework to formalize trustworthy inference and learning. We propose an optimization formulation that can be easily modified and extended to yield various existing frameworks. We also explore the capacity to do uncertainty quantification.

# Framework description

Let $\Theta$ the parameter space, $\mathcal{X}$ the space of observations, and $L:\Theta \times \mathcal{X}\to \mathbb{R}$ the loss function. Given any [[Measurable space|measurable space]] $(S,\mathcal{B})$ , let $\mathcal{P}(S)$ denote the space of [[Probability space|probability measures]] on $S$. Given the data $X=\left\{x_{i}\right\}_{1:n}\in\mathcal{X}^n$, let $P_{X}=\frac{1}{n}\sum_{i=1}^n\delta_{x_{i}}\in\mathcal{P}(\mathcal{X})$ denote the empirical data distribution. For any $P\in\mathcal{P}(\mathcal{X})$, define the neighborhood set $\Omega(P)\subset \mathcal{P}(\mathcal{X})$, which contains distributions similar to P. In addition, let $\mathcal{Q}\subseteq \mathcal{P}(\Theta)$ be the set of feasible posteriors for the parameter.

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

## Case 3: dual formulation when using Wasserstein neighborhood sets

With definitions defined above, we have the following formulations:
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
where $W_{d}^{p}$ is the Wasserstein p-distance, we can rewrite $L_{DR}$ as follows:
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


# Heterogenous data pitch

Under the context of [[Defining robustness#Worst case sub-population|worst case subpopulation]], we want to find a one size fits all solution that caters to all instances of the data up to a certain degree. What if we go the other direction and infer solutions that **specialize** towards certain subpopulations. For example, consider the following linear regression problem and potential posterior for the slope coefficient:
$$
y\sim \mathcal{N}(\boldsymbol{\beta}^{\mathrm{T}}\mathbf{z},\sigma^2)
$$
![[heterogenous_linear_regression.svg|90%]]
![[cater_vs_noncater.svg|90%]]
The specialized posterior tries to come up with solutions that cater best to one of the two sup-population of the data instead of trying to get acceptable performance for all of them at once. With this maybe we can detect multi-modality or detect outliers. This might al signal that the model we are using cannot capture the dynamics of the system at hand.

## Alternative divergences/modifying loss function

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

## Neighborhood set and polarization

Whether or not perturbing $P_{\star}$ within a neighborhood set directly contributes to this effect is yet to be investigated. However, combined with loss functions with the characteristic described above, an adversarial perturbation to $P_{\star}$ would affect solutions that try to cater to everyone the most, since these has the most samples lying within the meaningful zone.

## Experimental behavior

### Asymptotic exponential domination

Using $L(\theta,X)=nD_{\beta}(P_{X},P_{\theta})+C$ yields the conjected behavior for small sample size. However, as the number of samples goes to infinity, the posterior converges to a single peak. This is due to the exponential nature of the Gibbs posterior. Consider a hypothetical "counting loss", where good samples have a loss of $0$ and bad samples have a loss of $1$, and suppose for a dataset of size $n$, two sets of parameters $\theta_{1}$ and $\theta_{2}$ with corresponding losses $l_{1}$ and $l_{2}$ such that
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
As the number of the sample size grows, the ratio $e^{-kc}$ shrinks to zero and the parameter with the lower loss, $\theta_{2}$, would dominate. In order to prevent this behavior the loss function needs to converge to a finite value as $n\to \infty$, the how exactly this happens needs to be investigated further. Another point to note, if a asymptotically bounded loss function is used, the resulting posterior is not asymptotically prior-agnostic, and prior choice becomes more important.

# Questions

* other examples
* more covariates - higher dimensions -> works in higher dimensions
    * keep most covariates the same, a few of them different
* choice of effective sample $m$
* other kinds of regression
    * logistic regression 
    * location model
* data dependent prior


