# Kullback-Leibler Divergence

$$
D_{KL}(P|Q)=\int_{\mathcal{X}} \log \left[\frac{P(dx)}{Q(dx)}\right]P(dx) 
$$
* No need for density estimation
* Sensitive to tail (mis)specification
* Unbounded
# Total Variation Divergence

$$
D_{TV}(P,Q)=\mathop{\mathrm{sup}}_{A}\ |P(A)-Q(A)|=\frac{1}{2}\int_{\mathcal{X}}\left| 1-\frac{Q(dx)}{P(dx)}\right|P(dx)
$$
* Needs density estimation
* Bounded $0\leq D_{TV}(P,Q)\leq 1$

# $\alpha$-Divergence

$$
D_{\alpha}(P,Q)=\frac{1}{\alpha(1-\alpha)}\left\{1-\int_{\mathcal{X}}\left[\frac{Q(dx)}{P(dx)}\right]^{1-\alpha}P(dx)\right\} 
$$
* Equals $D_{KL}$ for $\alpha=1$
* Generally only care about $\alpha \in(0.5,1)$
* Lower $\alpha$ means less sensitive to outlying distribution
* Needs density estimation

# $\beta$-Divergence (a.k.a. Density Power Divergence)

$$
\begin{align}
D_{\beta}(P,Q)&=\frac{1}{\beta(\beta+1)}\int_{x\in\mathcal{X}}\left[\beta \int_{x'\in \mathcal{X}} Q(dx')^{\beta+1}-(\beta+1)Q(dx)^\beta+P(dx)^\beta\right]P(dx) \\
&=\frac{1}{\beta(\beta+1)}\int_{\mathcal{X}}\left[\beta  \frac{Q(dx)^{\beta+1}}{P(dx)}-(\beta+1)Q(dx)^\beta+P(dx)^\beta\right]P(dx)
\end{align}
$$
* Equals $D_{KL}$ for $\beta=0$
* Larger $\beta$ means less sensitive to outlying distribution
* Can be computed using Monte Carlo estimation or density estimation
# Maximum Mean Discrepancy

$$
\mathrm{MMD}_{k}^{2}(P,Q)=\mathbb{E}_{x,x'\sim P}[k(x,x')]+\mathbb{E}_{y,y'\sim Q}[k(y,y')]-2\mathbb{E}_{x\sim P,y\sim Q}[k(x,y)]
$$

* Can be computed using Monte Carlo estimation

# Wasserstein p-Distance
$$
W_{d}^{p}(P,Q)=\left(\begin{align}
\mathop{\mathrm{inf}}_{\gamma}\ &\mathbb{E}_{(x,y)\sim \gamma}[d(x,y)^p] \\
\text{s.t.}&\int_{\mathcal{X}}\gamma(\cdot,dy)=P(\cdot)\\
&\int_{\mathcal{X}}\gamma(dx,\cdot)=Q(\cdot)
\end{align}\right)^{1/p} 
$$
* If used as a neighborhood set, the dual of the formulation is more [[Dual formulation for Wasserstein neighborhood set|tractable]].