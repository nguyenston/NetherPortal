---
category: literaturenote
tags:
  - bmcPilot
citekey: chenSelectingOptimalDecisions2019
status: read
dateread:
---
> [!Cite]
> Chen, R., & Paschalidis, I. (2019). Selecting Optimal Decisions via Distributionally Robust Nearest-Neighbor Regression. _Advances in Neural Information Processing Systems_, _32_. [https://proceedings.neurips.cc/paper/2019/hash/8efb100a295c0c690931222ff4467bb8-Abstract.html](https://proceedings.neurips.cc/paper/2019/hash/8efb100a295c0c690931222ff4467bb8-Abstract.html)

>[!Synth]
>**Contribution**:: %% begin contr %% This paper developed the technique of Distributionally robust (linear) regression informed K nearest neighbor (DRLR-KNN) and randomized prescription policy that is used in [[@huPersonalizedHypertensionTreatment2023]]. They describe the technique and established performance guarantees.%% end contr %%
>
>**Related**:: 

>[!md]
> **FirstAuthor**:: Chen, Ruidi
> **Author**:: Paschalidis, Ioannis
~
> **Title**:: Selecting Optimal Decisions via Distributionally Robust Nearest-Neighbor Regression
> **Year**:: 2019
> **Citekey**:: chenSelectingOptimalDecisions2019
> **itemType**:: conferencePaper
> **Volume**:: 32
> **Publisher**:: Curran Associates, Inc.

> [!LINK]
>
> [Full Text PDF](file:///home/nguyenston/Zotero/storage/M3DGLTR3/Chen%20and%20Paschalidis%20-%202019%20-%20Selecting%20Optimal%20Decisions%20via%20Distributionally%20R.pdf)

> [!Abstract]
>
> This paper develops a prediction-based prescriptive model for optimal decision
making that (i) predicts the outcome under each action using a robust
nonlinear model, and (ii) adopts a randomized prescriptive policy determined
by the predicted outcomes. The predictive model combines a new regularized
regression technique, which was developed using Distributionally Robust
Optimization (DRO) with an ambiguity set constructed from the Wasserstein
metric, with the K-Nearest Neighbors (K-NN) regression, which helps to
capture the nonlinearity embedded in the data. We show theoretical results
that guarantee the out-of-sample performance of the predictive model, and
prove the optimality of the randomized policy in terms of the expected true
future outcome. We demonstrate the proposed methodology on a hypertension
dataset, showing that our prescribed treatment leads to a larger reduction in
the systolic blood pressure compared to a series of alternatives. A clinically
meaningful threshold level used to activate the randomized policy is also
derived under a sub-Gaussian assumption on the predicted outcome.
>

# Notes
>

# Annotations
<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> This paper develops a prediction-based prescriptive model for optimal decision making that (i) predicts the outcome under each action using a robust nonlinear model, and (ii) adopts a randomized prescriptive policy determined by the predicted outcomes

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Distributionally Robust Optimization (DRO)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ambiguity set constructed from the Wasserstein metric

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> K-Nearest Neighbors (K-NN) regression

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> theoretical results that guarantee the out-of-sample performance

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> prove the optimality of the randomized policy in terms of the expected true future outcome

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> A clinically meaningful threshold level used to activate the randomized policy is also derived under a sub-Gaussian assumption on the predicted outcome.

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> discrete set of available actions [M ]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> goal is to choose m ∈ [M ] such that the future outcome y is optimized

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> auxiliary data x ∈ Rp

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> outcome y

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> main challenge with learning from observational data lies in the lack of counterfactual information

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> One solution

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> groups the training samples based on their actions, and fits a model in each group

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The performance of the prescribed decision hinges on the quality of the predictive model

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> (i) there are often “outliers” in the data, especially in the medical applications motivating this work

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> (ii) the underlying relationship we try to learn is usually nonlinear and its parametric form is not known a priori.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> a nonparametric robust learning procedure is in need.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Motivated by the observation that individuals with similar features x would have similar outcomes y if they were to take the same action

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> propose a predictive model that makes predictions based on the outcomes of similar individuals/neighbors in each group of the training set. It is a nonlinear and nonparametric estimator which constructs locally linear (constant) curves based on the similarity between individuals.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Our prescriptive methodology is established on the basis of a regression informed K-Nearest Neighbors (K-NN)

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> evaluates the importance of features through regularized regression, and estimates the outcome by averaging over the neighbors identified by a regression coefficients-weighted distance metric.

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Distributionally Robust Linear Regression (DRLR)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> with a Wasserstein metric-based uncertainty set

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> K-NN model builds locally linear (and globally nonlinear) predictions using information from neighbors, accounting for the non-linearity that is not captured by DRLR.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> robust predictions immunized against outliers and capturing the underlying non-linearity in the data.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> more information-efficient and more interpretable than the vanilla K-NN

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> develop a randomized prescriptive policy that chooses each action

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> this randomized strategy leads to a nearly optimal future outcome by an appropriate choice of ξ

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Our method constructs a locally linear estimator of the future outcome through learning a robust metric in the feature space.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Our problem is closely related to contextual bandits [14, 1, 23, 25] where an agent learns a sequence of decisions conditional on the contexts

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Our method is similar to K-NN regression with an Ordinary Least Squares (OLS)-weighted metric

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> key differences

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> (i) we adopt a robustified regression procedure that is immunized against outliers and is thus more stable and reliable; (ii) we propose a randomized prescriptive policy that adds robustness to the methodology

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> establish theoretical guarantees on the quality of the predictions and the prescribed actions

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> prescriptive rule in [7] was activated when the improvement of the recommended treatment over the standard of care exceeded a certain threshold whereas our method looks into the improvement over the previous regimen

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> our algorithm applicable in the scenario where the standard of care is unknown or ambiguous

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> derive a closed-form

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> expression for the threshold level

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Sec. 2, we introduce the DRLR+K-NN model and present the performance guarantees

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Sec. 3 develops the randomized prescriptive policy and proves its optimality in terms of the expected true outcome

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Experimental results using real medical (EHR) data are presented in Sec. 4

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> conclude the paper in Sec. 5

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> M available actions [M ]

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-3-x102-y492.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-3-x101-y278.png|65%]]

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-3-x103-y62.png|65%]]

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-4-x103-y634.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The intuition for using the ˆ βm-weighted metric is to amplify the weight of features that are most predictive of ym and downweight the unimportant ones

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Notice that Eq. (4) treats all neighbors equally by using the same weight. An alternative is to take a distance-weighted average of the responses of neighbors; we have numerically tried this strategy on our medical datasets in Section 4, but we find that its effect is not significantly different from the strategy where a uniform average of the responses is taken

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-4-x105-y345.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> xm(i),  m(i) are the feature vector and the noise term corresponding to the i-th closest sample to x within group m

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> To allow for flexibility in exploring alternatives that have a comparable performance, and also to correct for potential prediction errors that might mislead the ranking of actions, we propose a randomized policy that prescribes each action with a probability inversely proportional to its exponentiated predicted outcome

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-6-x101-y405.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Theorem 3.1 says that the expected true outcome of the randomized policy is no worse than the true outcome of any action k plus two components, one accounting for the gap between the predicted outcome under k and the average predicted outcome, and the other depending on the parameter ξ.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Thinking about choosing k = arg minm ym(x), if ˆ yk(x) is below the average predicted outcome (which should be true if we have an accurate prediction), it follows from (8) that the randomized policy leads to a nearly optimal future outcome by an appropriate choice of ξ.

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-6-x107-y90.png|65%]]

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/chenSelectingOptimalDecisions2019/chenSelectingOptimalDecisions2019-7-x98-y571.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Theorem 3.2 finds the largest threshold T (x) such that the probability of the expected improvement being less than T (x) is small.

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Algorithm 1 Estimating the conditional mean and standard deviation of the predicted outcome.

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> developed a prediction-based prescriptive method that determines the probability of taking each action based on the predictions from a DRLR informed K-NN model

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> derived a closed-form expression for the threshold level that is used to activate the randomized policy



%% Import Date: 2024-01-18T10:59:23.134-05:00 %%
