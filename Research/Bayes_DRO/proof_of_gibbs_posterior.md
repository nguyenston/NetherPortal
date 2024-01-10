**Lemma:** Let $(\mathcal{\Theta},\mathcal{F})$ be a measurable space. For any measure $P$ on $(\Theta,\mathcal{F})$ and any measurable function $L:\mathcal{\Theta}\to \mathbb{R}$ such that $\mathbb{E}_{\theta\sim P}[e^{L(\theta)}]<\infty$,
$$
\log \left(\mathbb{E}_{\theta\sim P}[e^{L(\theta)}]\right)=\mathop{\mathrm{sup}}_{Q\ll P}\ \mathbb{E}_{\theta \sim Q}[L(\theta)]-D_{KL}(Q|P),
$$
with the convention $\infty-\infty=-\infty$. Moreover, as soon as $L$ is upper-bounded on the support of $P$, the supremum on the RHS is:
$$
Q_{\star}(\theta)= \frac{e^{L(\theta)}}{\mathbb{E}_{\theta \sim P}[e^{L(\theta)}]}P(\theta)
$$
**Proof:** Let $Q\ll P$. We have $\mathop{\mathrm{sup}}_{Q}-D_{KL}(Q|Q_{\star})=0$ at  $Q=Q_{\star}$. We have
$$
\begin{align}
-D_{KL}(Q|Q_{\star})&=-\mathbb{E}_{\theta \sim Q}\left\{\log\left[ \frac{Q(\theta)}{P(\theta)} \right]+\log\left[ \frac{P(\theta)}{Q_{\star}(\theta)} \right]\right\}\\
&=-D_{KL}(Q,P)+\mathbb{E}_{\theta \sim Q}\left\{\log \left[\frac{e^{L(\theta)}}{\mathbb{E}_{\theta'\sim P}[e^{L(\theta')}]}\right] \right\}\\
&=-D_{KL}(Q,P)+\mathbb{E}_{\theta \sim Q}[L(\theta)]-\log \left\{\mathbb{E}_{\theta \sim P}\left[e^{L(\theta)}\right]\right\}.
\end{align}
$$
Therefor
$$
\mathop{\mathrm{sup}}_{Q}-D_{KL}(Q|Q_{\star})=-\log \left\{\mathbb{E}_{\theta \sim P}\left[e^{L(\theta)}\right] \right\}+\mathop{\mathrm{sup}}_{Q}\ \mathbb{E}_{\theta \sim Q}[L(\theta)]-D_{KL}(Q,P),
$$
where the LHS equals $0$.


# Similar proof

Find
$$
\mathop{\mathrm{sup}}_{Q\ll Q_{0}}\ \mathbb{E}_{\theta \sim Q}[L(\theta)]-D_{\beta}(Q,Q_{0}) 
$$
Suppose $Q_{\star}$ is the solution. We have
$$
\begin{align}
D_{\beta}(Q,Q_{\star})&=\frac{1}{\beta(\beta+1)}\mathbb{E}_{\theta \sim Q}\{\beta \mathbb{E}_{\theta'\sim Q_{\star}}[Q_{\star}(\theta)^{\beta}]-(\beta+1)Q_{\star}(\theta)^{\beta}+Q(\theta)^{\beta}\}\\
&=D_{\beta}(Q,Q_{0})+\frac{1}{\beta+1}\left\{\mathbb{E}_{\theta'\sim Q_{\star}}[Q_{\star}(\theta')^{\beta}]-\mathbb{E}_{\theta''\sim Q_{0}}[Q_{0}(\theta'')^{\beta}]\right\} \\
&\qquad-\frac{1}{\beta}\mathbb{E}_{\theta \sim Q}\left\{Q_{\star}(\theta)^{\beta}-Q_{0}(\theta)^{\beta}\right\} 
\end{align}
$$

We need to find $Q_{\star}$ so that $-\frac{1}{\beta}\mathbb{E}_{\theta \sim Q}\left\{Q_{\star}(\theta)^{\beta}-Q_{0}(\theta)^{\beta}\right\}$ resolves into $-\mathbb{E}_{\theta \sim Q}\left\{L(\theta)\right\}+C$ where $C$ is a term independent of $Q$

**This is kind of a dead end**

##
