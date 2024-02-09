---
category: literaturenote
tags: bayesMixture
citekey: "giladAutomatedApproachDetermining2020"
status: unread
dateread:
---
> [!Cite]
> Gilad, G., Sason, I., & Sharan, R. (2020). An automated approach for determining the number of components in non-negative matrix factorization with application to mutational signature learning. _Machine Learning: Science and Technology_, _2_(1), 015013. [https://doi.org/10.1088/2632-2153/abc60a](https://doi.org/10.1088/2632-2153/abc60a)

>[!Synth]
>**Contribution**:: %% begin contr %% This paper propose a method to automatically determine the rank number $K$ in non-negative matrix factorization. To score different $K$'s, they run the inference for each $K$ against partially obscured data and see how well they can recover the missing parts.%% end contr %%
>
>**Related**:: 

>[!md]
> **FirstAuthor**:: Gilad, Gal
> **Author**:: Sason, Itay
> **Author**:: Sharan, Roded
~
> **Title**:: An automated approach for determining the number of components in non-negative matrix factorization with application to mutational signature learning
> **Year**:: 2020
> **Citekey**:: giladAutomatedApproachDetermining2020
> **itemType**:: journalArticle
> **Journal**:: *Machine Learning: Science and Technology*
> **Volume**:: 2
> **Issue**:: 1
> **Pages**:: 015013
> **DOI**:: 10.1088/2632-2153/abc60a

> [!LINK]
>
> [IOP Full Text PDF](file:///home/nguyenston/Zotero/storage/7Y8MMDKN/Gilad%20et%20al.%20-%202020%20-%20An%20automated%20approach%20for%20determining%20the%20number%20o.pdf)

> [!Abstract]
>
> Non-negative matrix factorization (NMF) is a popular method for finding a low rank approximation of a matrix, thereby revealing the latent components behind it. In genomics, NMF is widely used to interpret mutation data and derive the underlying mutational processes and their activities. A key challenge in the use of NMF is determining the number of components, or rank of the factorization. Here we propose a novel method, CV2K, to choose this number automatically from data that is based on a detailed cross validation procedure combined with a parsimony consideration. We apply our method for mutational signature analysis and demonstrate its utility on both simulated and real data sets. In comparison to previous approaches, some of which involve human assessment, CV2K leads to improved predictions across a wide range of data sets.
>

# Notes
>

# Annotations
<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> Non-negative matrix factorization (NMF)

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> NMF is widely used to interpret mutation data

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> A key challenge in the use of NMF is determining the number of components

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> we propose a novel method, CV2K, to choose this number automatically

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> based on a detailed cross validation procedure combined with a parsimony consideration

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> When non-negativity constraints are applicable, NMF often provides a more meaningful structure than other low-rank approximation methods

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> how to determine the number of components

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> Bayesian variant of NMF [4], which chooses K that balances between model’s likelihood and complexity

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> In the field of mutational signature learning, the two common methods are SigProfiler (SP) [11] and SignatureAnalyzer (SA) [12]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> SignatureAnalyzer uses the above Bayesian NMF

<b class="thickUnd" style="text-decoration-color: #2ea8e5">Thesis</b>
> Here we propose an automated method, CV2K, to choose K that is applicable for the most general definition of NMF. CV2K is based on a detailed comparison of the performance of different solutions in reconstructing hidden values of the original matrix in a cross validation setting

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> In order to score different values of K, we hide some of the original matrix entries and test how well we can recover them

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> CV2K scheme is described in algorithm 3 and consists of two parts

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Evaluate all applicable values for K using imputation with a fraction p of missing values

<b class="thickUnd" style="text-decoration-color: #ff6666">Definitions</b>
> K∗ be the value of K attaining the best median error over all runs

<b class="thickUnd" style="text-decoration-color: #f19837">Procedure</b>
> Use Wilcoxon rank-sum test to compare the obtained value K∗ to smaller values, and reduce the value if they are not significantly different

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/giladAutomatedApproachDetermining2020/giladAutomatedApproachDetermining2020-5-x110-y227.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/giladAutomatedApproachDetermining2020/giladAutomatedApproachDetermining2020-8-x114-y420.png|65%]]

<b class="thickUnd" style="text-decoration-color: #ffd400">Quote</b>
> ![[LiteratureNotes/Assets/giladAutomatedApproachDetermining2020/giladAutomatedApproachDetermining2020-9-x103-y532.png|65%]]



%% Import Date: 2024-01-30T13:31:22.377-05:00 %%
