---
category: literaturenote
tags: bayesMixture, 62-08, 92-08, 92-10, Cancer genomics, Cross-validation, Model checking, Model selection, Mutational signatures, Negative Binomial, Non-negative matrix factorization, Poisson
citekey: "pelizzolaModelSelectionRobust2023"
status: unread
dateread:
---
> [!Cite]
> Pelizzola, M., Laursen, R., & Hobolth, A. (2023). Model selection and robust inference of mutational signatures using Negative Binomial non-negative matrix factorization. _BMC Bioinformatics_, _24_(1), 187. [https://doi.org/10.1186/s12859-023-05304-1](https://doi.org/10.1186/s12859-023-05304-1)

>[!Synth]
>**Contribution**:: %% begin contr %% %% end contr %%
>
>**Related**:: 

>[!md]
> **FirstAuthor**:: Pelizzola, Marta
> **Author**:: Laursen, Ragnhild
> **Author**:: Hobolth, Asger
~
> **Title**:: Model selection and robust inference of mutational signatures using Negative Binomial non-negative matrix factorization
> **Year**:: 2023
> **Citekey**:: pelizzolaModelSelectionRobust2023
> **itemType**:: journalArticle
> **Journal**:: *BMC Bioinformatics*
> **Volume**:: 24
> **Issue**:: 1
> **Pages**:: 187
> **DOI**:: 10.1186/s12859-023-05304-1

> [!LINK]
>
> [Full Text PDF](file:///home/nguyenston/Zotero/storage/UV76NHA4/Pelizzola%20et%20al.%20-%202023%20-%20Model%20selection%20and%20robust%20inference%20of%20mutational.pdf)

> [!Abstract]
>
> The spectrum of mutations in a collection of cancer genomes can be described by a mixture of a few mutational signatures. The mutational signatures can be found using non-negative matrix factorization (NMF). To extract the mutational signatures we have to assume a distribution for the observed mutational counts and a number of mutational signatures. In most applications, the mutational counts are assumed to be Poisson distributed, and the rank is chosen by comparing the fit of several models with the same underlying distribution and different values for the rank using classical model selection procedures. However, the counts are often overdispersed, and thus the Negative Binomial distribution is more appropriate.
>

# Notes
>

# Annotations
<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> The spectrum of mutations in a collection of cancer genomes can be described by a mixture of a few mutational signatures. The mutational signatures can be found using non-negative matrix factorization (NMF)

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> In most applications, the mutational counts are assumed to be Poisson distributed

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> However, the counts are often overdispersed, and thus the Negative Binomial distribution is more appropriate.

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> We propose a Negative Binomial NMF

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> capture the variation across patients

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> introduce a novel model selection procedure inspired by cross-validation to determine the number of signatures

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> state-of-the-art methods are highly overestimating the number of signatures when overdispersion is present

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> our model selection procedure is more robust at determining the correct number of signatures under model misspecification

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> The summary of somatic mutations observed in a tumor is called a mutational profile

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> can often be associated with factors such as aging [1], UV light [2] or tobacco smoking [3]

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> A mutational profile is thus a mixture of mutational processes that are represented by mutational signatures

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Non-negative matrix factorization (NMF)

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> V contains the mutational counts for different patients

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> number of rows N is the number of patients and the number of columns M is the number of different mutation types

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> matrixH consists of K mutational signatures

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> matrix W

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> exposures of the different signatures

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> we need to choose a model and a rank K

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> the optimal rank of the data V is often chosen by comparing the fit under a certain model for many different values of K

<b class="thickUnd" style="text-decoration-color: #5fb236">Follow up read</b>
> Akaike Information Criterion (AIC), Bayesian Information Criterion (BIC)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> usual model assumption is the Poisson distribution

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> We observe that this model assumption is often inadequate

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> we observe overdispersion in the

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> mutational counts, i.e. a situation where the variance in the data is greater than what is expected under the assumed model.

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> suggest using a model where the mutational counts follow a Negative Binomial distribution

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> has an additional parameter to explain the overdispersion in the data

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> model is becoming more popular to model the dispersion in mutational counts

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> The extended model is referred to as NBN-NMF, where N is the number of dispersion parameters (equivalent to the number of patients).

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Poisson NMF (Po-NMF)

<b class="thickUnd" style="text-decoration-color: #a28ae5">Thesis</b>
> ![[LiteratureNotes/Assets/pelizzolaModelSelectionRobust2023/pelizzolaModelSelectionRobust2023-5-x104-y68.png|65%]]



%% Import Date: 2024-01-30T13:21:46.005-05:00 %%
