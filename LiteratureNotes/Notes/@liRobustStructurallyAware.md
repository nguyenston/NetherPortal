---
category: literaturenote
tags: Private, Manuscript, bayesMixture
citekey: "liRobustStructurallyAware"
status: unread
dateread:
---
> [!Cite]
> Li, J. (n.d.). _Robust, Structurally Aware Model Selection for Mixtures_.

>[!Synth]
>**Contribution**:: %% begin contr %% This work propose a structurally aware technique to determine the number of group $K$ in a mixture model. The technique is robust to misspecification of the data-generating process. They also provide consistency results under intuitive assumptions.%% end contr %%
>
>**Related**:: 

>[!md]
> **FirstAuthor**:: Li, J
~
> **Title**:: Robust, Structurally Aware Model Selection for Mixtures
> **Year**:: N/A
> **Citekey**:: liRobustStructurallyAware
> **itemType**:: manuscript

> [!LINK]
>
> [Li - Robust, Structurally Aware Model Selection for Mix.pdf](file:///home/nguyenston/Zotero/storage/WJ29FUEH/Li%20-%20Robust,%20Structurally%20Aware%20Model%20Selection%20for%20Mix.pdf)

> [!Abstract]
>
> Mixture models are often used to discover unobserved groups with real-world interpretations that generate observed data. However, mixture model inference is usually ill-defined a priori because the assumed observation model is only an approximation to the true data-generating process and the number of groups is unknown. Thus, as the number of observations increases, rather than obtaining better inferences, the opposite occurs: the data is explained by adding spurious groups that compensate for the shortcomings of the observation model. However, there are two important sources of prior knowledge that we can exploit to obtain well-defined results no matter the dataset size: causal information (e.g., knowing that the latent groups cause the observed signal but not vice-versa) and a rough sense of how wrong the observation model is (e.g., based on small amounts of expert-labeled data or some understanding of the data-generating process). We propose a new model selection criteria that, while model-based, uses this available knowledge to obtain mixture model inferences that are robust to misspecification of the observation model and account for known causal structure. We provide theoretical support for our approach by proving a first-of-its-kind consistency result under intuitive assumptions. Simulation studies and an application to flow cytometry data demonstrate our model selection criteria is consistently finds the correct number of components.
>

# Notes
>

# Annotations
<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> the assumed observation model is only an approximation to the true data-generating process and the number of groups is unknown

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> as the number of observations increases

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> the data is explained by adding spurious 15 groups that compensate for the shortcomings of the observation model

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> two important sources of prior knowledge

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> causal information

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> rough sense of how wrong the observation model is

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> propose a new model selection criteria

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> obtain mixture model inferences that are robust to misspecification

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> account for known causal structure

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> proving a first-of-its-kind consistency result under intuitive assumptions

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> mixture models are often used to discover unobserved subpopulations or distinct types that generated the observed data

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> true number of types or sub-populations K◦

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> usually unknown a priori

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> numerous inference methods provide consistent estima40 tion when the mixture components are well-specified, if the components are misspecified, then standard methods do not work as intended

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> overfitting

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> To address the overfitting problem in the misspecified setting, various robust clustering methods have been developed

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> require choosing the number of clusters for the mixture model beforehand, and their performance heavily relies on 50 the selected value of K

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> coarsening: instead of assuming the data was generated from the assumed model, the coarsened posterior allows certain degree of divergence between the model and data

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> shows good robustness properties in practice

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> does not guarantee the convergence to a meaningful number of components

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> their approach to determining Ko involves post-processing, specifically eliminating the minimal clusters

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> high computational cost

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> heuristically determine a suitable robustness threshold

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> select the number of components correctly given some knowledge about the nature of the model misspecification

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> add robustness threshold at the component level – in contrast to adding it on the overall model

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Because we employ component-wise robustness thresholds, we are able to show that, under natural conditions, our method identifies the number of components correctly in large datasets

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> can be used in combination with 70 any estimation technique

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Given a fitted model for each candidate number of components, the cost required to compute our criterion is typically quite small

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> can be defined using any problem-appropriate discrepancy measure between distributions

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> providing theoretical guarantees using both the Kullback-Leibler divergence and maximum mean discrepancies

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> x1:N = (x1, . . . , xN )

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> unknown distribution Po

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Ko is the number of types

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Pok is the distribution of observations from the kth type

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> πok is the probability that an observation belongs to the kth type

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> πo = (πo1, . . . , πoKo )

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> we assume πok > 0

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> mixture model parameterized by θ

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> φ ∈ Φ parameterizes the family of mixture component distributions F = {Fφ | φ ∈ Φ}

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> θ = (π, φ1, . . . , φK) ∈ Θ

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> our goals are to (1) find Ko and (2) find a parameter estimate θ?

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> such that

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> π∗ ≈ πo

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Fφ∗ k ≈ Pok

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> as number of observations increases, model selection criteria tend to create additional clusters to compensate the model–data mismatch and thus overestimates Ko

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> coarsened posterior as well as other standard methods are, roughly speaking, indifferent to the details of how a model is represented and thus “unaware” of the difference between the mixture components

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> rewrite the model in the “uncollapsed” form which correctly capture the causal structure and makes the component dis130 tributions explicit

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/liRobustStructurallyAware/liRobustStructurallyAware-4-x199-y111.png|65%]]

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/liRobustStructurallyAware/liRobustStructurallyAware-5-x103-y558.png|65%]]

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> The main idea for structurally aware inference is to introduce the cutoff on the discrepancy between model and true distribution from the component level

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> divergence between two probability measures P and Q denoted as D(P | Q)

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> samples y1:M = (y1, . . . , yM ) from P

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> consistent estimator ˆ D(y1:M | Q) for D(P | Q)

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> z1:N = (z1, . . . , zN ) denote the cluster assignment for the observations

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> X(k)(z1:N ) = {xn | zn = k, n = 1, . . . , N } denote the set 160 of observations assigned to component k.

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/liRobustStructurallyAware/liRobustStructurallyAware-5-x90-y213.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> structurally aware loss is at its minimum when each model component closely matches the real generating component distribution

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> by minimizing the structurally aware loss in Eq. (4), the inference excludes K ≤ Ko

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> to asymptotically rule out K > Ko

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/liRobustStructurallyAware/liRobustStructurallyAware-5-x86-y23.png|65%]]

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> favor the smallest value of K for which Rρ(θ(K); z1:N , x1:N ) = 0

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/liRobustStructurallyAware/liRobustStructurallyAware-6-x73-y466.png|65%]]

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> providing rigorous justification

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> under reasonable assumptions, it consistently picks up the number of components

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> metric d(P, Q) which converges to zero whenever Q converges to P in distribution and can be bounded by a function of D(P | Q)

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> empirical distribution ˆ PN = N −1 ∑N n=1 δyN,n

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ˆ D satisfy the following conditions

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> metric detects empirical convergence

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> metric is jointly convex in its arguments

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> discrepancy estimator is consistent

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Smoothness of the discrepancy estimator

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> discrepancy bounds the metric

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> continuous, non-decreasing function φ : R → R such that d(P, Q) ≤ φ(D(P | Q))

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> second assumption explicitly outlines the behavior of the data distribution and model

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> empirical weights and component distributions

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> π(K) ∗k

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> ˆ P (K) k

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> ̃ P (K) k as the limiting distribution of ˆ P (K)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Meaningful decomposition of the data-generating distribution

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Regularity of the inference algorithm

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Accuracy of the parameter estimates for K = Ko

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Poor model fit when K is too small

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> when conditional on a correct number of components, the structurally aware loss of the optimal model is 0 when N goes to infinity

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> for K < Ko, the structurally aware loss is large and fails to attain optimum when data size is large

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> case K > Ko discussed in Section 3

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> structurally aware loss achieves the minimum if and only if ˆ K = Ko

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> important to note that our theoretical outcomes are influenced by the choice of divergence D and the selection of the cutoff value ρ

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> require D satisfy our assumptions in Assumption 1

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ρ, as indicated in Assumption 2

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> two crucial pieces in our methodology: the choice of divergence and the value of ρ

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> We validate the use of Kullback–Leibler divergence and mean maximum discrepancy dMMD here

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> ‖f ‖BL = ‖f ‖∞ + ‖f ‖L

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> bounded Lipschitz metric dBL(P, Q) = sup‖f‖BL≤1{| ∫ f d(P − Q)|} as d

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> we assume

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> D(  ̃ Pk ||Fφ∗ k ) < ρ

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> this cutoff is intrinsically determined by

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> D(Pok||Fφ∗ k ) < ρo

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> with Kullback-Leibler divergence, the cutoff ρ upper is bounded by the divergence between the true component distribution and optimal model com285 ponent quantified by ρo, the difference between the conditional probabilities based on model and true generating distribution and the difference between the mixture weights derived from optimal model and true distributions

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> If KL(Pok | Fφ∗ k ) < ρo for k = 1, . . . , Ko, then KL(  ̃ Pk | Fφ∗ k ) < ρ, where ρ = (1 +  π)(1 +  P )[ρo + log(1 +  π)(1 +  P )].

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> if γFB (Pok, Fφ∗ k ) < ρo for k = 1, . . . , Ko, then γFB (  ̃ Pk, Fφ∗ k ) < ρ, where ρ = ( π +  P +  π P )1/2 + ρo

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Proposition 2 provides justification for a broad class of metrics

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> mean maximum discrepancy with bounded kernels

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> Propositions 1 and 2 show that the value of ρ in theory should depend on the choice of divergence, the real discrepancy between the true data generating distribution and the optimal model component, the deviation between the component weights π∗/πo and the conditional distribu- 305 tions pr∗(z = k | x)/pro(z = k | x).

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Estimation of Kullback–Leibler divergence

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Choosing λ

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> In practice, we often choose a small value of λ relative to the sample size, for instance, set λ = 1/N

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Choosing ρ

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> In Section 4.3, we explored the theoretical bounds of selecting ρ

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> we introduce two practical methods to effectively guide the selection of the most appropriate ρ

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> leveraging prior domain knowledge to approximate its optimal value

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> for datasets where a portion has “ground truth” labels, finding best ρ based on metrics like F-measure, precision, or recall

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Leveraging the ground truth allows us to approximate the mismatch between the assumed model and the data, serving as crucial prior knowledge when determining appropriate ρ values.

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> For datasets that the ground truths are not available

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> novel inference approach based on a crucial observation

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> structurally aware loss exhibits piece-wise linearity in ρ

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> two-step process

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> run the parameter updates for Kmax models

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> collect all component information including the component-wise divergence, mixture weights and model parameters

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> plot the penalized loss as a function of ρ for each K

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> optimal model is determined by identifying the number of components with the first widest and stable region

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The idea behind this selection rule is to identify the first instance of stability, indicating that increasing ρ further doesn’t notably improve the loss. However, subsequent stable regions that appear afterward might introduce too much tolerance, potentially resulting in model underfitting

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Inference Algorithm

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> highly adaptable, easily accommodating different parameter-update inference methods

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> computes the structurally aware loss iteratively



%% Import Date: 2024-01-28T01:59:02.683-05:00 %%
