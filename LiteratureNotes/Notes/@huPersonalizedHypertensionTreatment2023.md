---
category: literaturenote
tags:
  - Clinical
  - decision
  - support
  - Hypertension
  - prescription
  - Machine
  - learning
  - bmcPilot
citekey: huPersonalizedHypertensionTreatment2023
status: read
dateread:
---
> [!Cite]
> Hu, Y., Huerta, J., Cordella, N., Mishuris, R. G., & Paschalidis, I. Ch. (2023). Personalized hypertension treatment recommendations by a data-driven model. _BMC Medical Informatics and Decision Making_, _23_(1), 44. [https://doi.org/10.1186/s12911-023-02137-z](https://doi.org/10.1186/s12911-023-02137-z)

>[!Synth]
>**Contribution**:: %% begin contr %% By using Distributionally robust regression informed K nearest neighbor, they are able to train ML models that prescribe hypertension treatments that are significant better than standard of care. The metric of success is the patient's reduction of Systolic Blood Pressure. The model proposed is also highly interpretable, enabling the analysis of the correlation between the characteristics of patients and their SBP. %% end contr %%
>
>**Related**:: 

>[!md]
> **FirstAuthor**:: Hu, Yang
> **Author**:: Huerta, Jasmine
> **Author**:: Cordella, Nicholas
> **Author**:: Mishuris, Rebecca G.
> **Author**:: Paschalidis, Ioannis Ch.
~
> **Title**:: Personalized hypertension treatment recommendations by a data-driven model
> **Year**:: 2023
> **Citekey**:: huPersonalizedHypertensionTreatment2023
> **itemType**:: journalArticle
> **Journal**:: *BMC Medical Informatics and Decision Making*
> **Volume**:: 23
> **Issue**:: 1
> **Pages**:: 44
> **DOI**:: 10.1186/s12911-023-02137-z

> [!LINK]
>
> [Full Text PDF](file:///home/nguyenston/Zotero/storage/DP2PKUU9/Hu%20et%20al.%20-%202023%20-%20Personalized%20hypertension%20treatment%20recommendation.pdf)

> [!Abstract]
>
> Hypertension is a prevalent cardiovascular disease with severe longer-term implications. Conventional management based on clinical guidelines does not facilitate personalized treatment that accounts for a richer set of patient characteristics.
>

# Notes
>

# Annotations
<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Hypertension is a prevalent cardiovascular disease with severe longer-term implications.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Conventional management based on clinical guidelines does not facilitate personalized treatment

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Models were developed to recommend a class of antihypertensive medications

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Regression immunized against outliers was combined with a nearest neighbor approach

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> associate with each patient an affinity group of other patients

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Systolic Blood Pressure (SBP)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> select the class of medication that minimized their future predicted SBP

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> model, built with a distributionally robust learning procedure

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> reduction of 14.28 mmHg in SBP, on average

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> 70.30% larger than the reduction achieved by the standard-ofcare

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> 7.08% better than the corresponding reduction achieved by the 2nd best model which uses ordinary least squares regression

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> 87.71% of these modelgenerated prescription recommendations passed a sanity check by clinicians.

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> Our data-driven approach for personalized hypertension treatment yielded significant improvement compared to the standard-of-care. The model implied potential benefits of computationally deprescribing and can support situations with clinical equipoise.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Machine Learning (ML) algorithms, seeking to maximize the effectiveness of hypertensive medications at the individual level.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> several challenges for ML-driven personalization:

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Electronic Health Records (EHRs)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Integrating heterogenous data from different sources

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> leads to data ‘outliers’

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> relies on frequent patient visits and rich historical information

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> There is a need to make recommendations even for patients with sparse history.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ML adoption in health-care settings is limited by the lack of interpretability and comprehensiveness.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> cannot make medical decisions just based on a black-box model

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> for harmonized EHRs data, a DL model did not show superior benefits compared with traditional methods

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> our objective is to design a model able to generate a personalized hypertension prescription based on each individual patient profile, including demographics, vital signs, past medical history, and clinical test records. To that end, we predict the future SBP by using the past outcomes of patients who had the most similar profiles.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> robustified regression procedure to immunize predictions against outliers

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> algorithm is based on a regression-informed K-Nearest Neighbor (KNN)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> this method is more reliable than a simple linear model but maintains interpretability and comprehensibility.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> incorporated a randomized prescriptive policy to add robustness to the model

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> To help the prescribers interpret the model, we randomly sampled 350 cases, listed the recommended prescriptions, and the corresponding patient profiles.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> These cases were manually reviewed by clinicians at Boston Medical Center (BMC)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Dataset

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> extracted data from Boston Medical Center (BMC) Electronic Health Records (EHRs)

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> For each qualified patient, we collected their demographics (age, sex, race, language, marital status, ZIP code), past blood pressure records, past medical history, vital signs, symptoms, medication history, laboratory tests results, cigarette usage, information for their social needs and depression test scores.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> A ‘visit’ is therefore a periodic review period of the patient’s health status rather than an actual visit to the clinic.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> monotherapy of 7 types of antihypertensive drugs:

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> did not consider specific combinations of drugs as an option because drug combinations are often associated with complex medical constraints and complications

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Instead, the model provides a list of recommended agents and their associated confidence probabilities, leaving to the physician the option of prescribing a combination of agents in the recommended list.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The new prescription will be considered only if the improvement on SBP control is over a pre-specified threshold.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> A threshold of SBP reduction above which the improvement is considered substantial enough is determined in [24, 32] using certain distributional assumptions on the predicted S B P.

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> we opted for a randomized recommendation policy that prescribes a drug with a probability inversely proportional to its exponentiated predicted SBP

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> improving the robustness of the model

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> It has been shown statistically that such randomized strategy can achieve nearly optimal future outcomes if an appropriate parameter is chosen [24, 32].

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> a few common relative contradictions and disease specific preferences were incorporated in our prescriptive model.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/huPersonalizedHypertensionTreatment2023/huPersonalizedHypertensionTreatment2023-4-x51-y295.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The goal is to find the treatment that minimizes future SBP based on the medical history of a group of similar patients.

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> incorporate K-Nearest Neighbors (K-NN) on a regression-weighted metric

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Once the closest visits from the treatment group are identified, we consider their SBP values at their next visit

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> d use their averag

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> , to estimate the SBP of the patien

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> same procedure is repeated for all the prescription options

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> ![[LiteratureNotes/Assets/huPersonalizedHypertensionTreatment2023/huPersonalizedHypertensionTreatment2023-4-x302-y376.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Four (regression) algorithms were compared

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Distributionally Robust Linear Regression (DRLR)-informed KNN (the proposed model)

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Ordinary Least Square Regression (OLS)-informed KNN

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> the Least Absolute Shrinkage and Regression Operator (LASSO) regression

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Classification and Regression Trees (CART)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> DRLR was developed based on Distributionally Robust Optimization (DRO) with an ambiguity set built using a Wasserstein metric

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> mitigate the impact of outliers

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Under each prescription group

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> training set (80%), a validation set (10%), and a test set (10%)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> visits from the same individual were included only into a single set.

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> The best outcome is achieved by DRLR-informed KNN,

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> 70.30% better than the SBP reduction under standard of care

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> superiority of our robustified DRLR procedure against outliers in terms of the improvement in outcomes.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> performance of the randomized strategy did not differ much from the performance of the deterministic one.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> randomized rule gives more flexibility for the prescriber to explore suboptimal options in the model and to avoid potential medical contradictions

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Sub-models were developed for each prescription

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> potential outcome under a particular treatment was estimated by the corresponding sub-model

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> trained on patient visits

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> summarized the top 10 predictive features by assembling the feature importance scores (regression coefficient magnitudes) from all the sub-models

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The most predictive feature is the SBP value in the current period,

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Among all the clinical features, ‘Oxygen saturation’ is the most important one in preicting SBP.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/huPersonalizedHypertensionTreatment2023/huPersonalizedHypertensionTreatment2023-5-x298-y535.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> 30.68% of the recommendations from the DRLR + KNN algorithm indicated continuing the current prescription

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> 28.91% of the algorithmic recommendations matched the standard of care.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> we sought to interpret the decisionmaking process of the model

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> generalize the patient characteristics that point to a certain prescription type

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Deprescribing refers to the process of tapering off or stopping medications to prevent adverse drug reactions and achieve better health management

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> deprescribing is increasingly encouraged among patients under control and older people with multi-morbidities

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> studies have shown that deprescribing of sedatives and nonsteroidal anti-inflammatory drugs is cost-effective

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Seven neighborhood profiles were built to summarize patients’ characteristics

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> If the percentage of group A in the drug X neighborhood is higher than the overall percentage of A in the whole test set, it implies that group A may generally get better response under drug X

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> this study has several limitations

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> retrospective study, only the outcomes with administered prescriptions were observed

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> counterfactual outcomes under other medications are unknown and can only be estimated by the predictive model.

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> a lot of factors aside from the magnitude of SBP reduction that need to be considered

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> including tolerance of past regimens, allergies, dosage for current medications, best medication for other chronic conditions, etc.

<b class="thickUnd" style="text-decoration-color: #5fb236">Follow up read</b>
> 24. Chen R, Paschalidis IC. Distributionally Robust Learning. Foundations and Trends® in Optimization. 2020;4:1–243.

<b class="thickUnd" style="text-decoration-color: #5fb236">Follow up read</b>
> 32. Chen R, Paschalidis I. Selecting optimal decisions via distributionally robust nearest-neighbor regression. In: Advances in Neural Information Processing Systems. Curran Associates, Inc.; 2019.



%% Import Date: 2024-01-17T18:36:58.833-05:00 %%
