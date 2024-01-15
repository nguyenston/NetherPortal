---
category: literaturenote
tags: bayesMixture
citekey: "millerMixtureModelsPrior2018"
status: unread
dateread:
---
> [!Cite]
> Miller, J. W., & Harrison, M. T. (2018). Mixture Models With a Prior on the Number of Components. _Journal of the American Statistical Association_, _113_(521), 340–356. [https://doi.org/10.1080/01621459.2016.1255636](https://doi.org/10.1080/01621459.2016.1255636)

>[!Synth]
>**Contribution**:: %% begin contr %% %% end contr %%
>
>**Related**:: 

>[!md]
> **FirstAuthor**:: Miller, Jeffrey W.
> **Author**:: Harrison, Matthew T.
~
> **Title**:: Mixture Models With a Prior on the Number of Components
> **Year**:: 2018
> **Citekey**:: millerMixtureModelsPrior2018
> **itemType**:: journalArticle
> **Journal**:: *Journal of the American Statistical Association*
> **Volume**:: 113
> **Issue**:: 521
> **Pages**:: 340-356
> **DOI**:: 10.1080/01621459.2016.1255636

> [!LINK]
>
> [Miller and Harrison - 2018 - Mixture Models With a Prior on the Number of Compo.pdf](file:///home/nguyenston/Zotero/storage/YSJK4QHJ/Miller%20and%20Harrison%20-%202018%20-%20Mixture%20Models%20With%20a%20Prior%20on%20the%20Number%20of%20Compo.pdf)

> [!Abstract]
>
> A natural Bayesian approach for mixture models with an unknown number of components is to take the usual finite mixture model with symmetric Dirichlet weights, and put a prior on the number of components—that is, to use a mixture of finite mixtures (MFM). The most commonly used method of inference for MFMs is reversible jump Markov chain Monte Carlo, but it can be nontrivial to design good reversible jump moves, especially in high-dimensional spaces. Meanwhile, there are samplers for Dirichlet process mixture (DPM) models that are relatively simple and are easily adapted to new applications. It turns out that, in fact, many of the essential properties of DPMs are also exhibited by MFMs—an exchangeable partition distribution, restaurant process, random measure representation, and stick-breaking representation—and crucially, the MFM analogues are simple enough that they can be used much like the corresponding DPM properties. Consequently, many of the powerful methods developed for inference in DPMs can be directly applied to MFMs as well; this simplifies the implementation of MFMs and can substantially improve mixing. We illustrate with real and simulated data, including high-dimensional gene expression data used to discriminate cancer subtypes. Supplementary materials for this article are available online.
>

# Notes
>

# Annotations
%% begin annotations %%



### Imported: 2024-01-15 03:33 pm


<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> Mixture models are used in a wide range of applications, including population structure (Pritchard, Stephens, and Donnelly 2000), document modeling (Blei, Ng, and Jordan 2003), speaker recognition (Reynolds, Quatieri, and Dunn 2000), computer vision (Stauffer and Grimson 1999), phylogenetics (Pagel and Meade 2004), and gene expression profiling (Yeung et al. 2001)

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> A common issue with finite mixtures is that it can be difficult to choose an appropriate numberofmixturecomponent

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> From a Bayesian perspective, perhaps the most natural approach is to treat the number of components k like any other unknown parameter and put a prior on it. When the prior on the mixture weights is Dirichletk(γ,...,γ)given k, we refer to such a model as a mixture of finite mixtures (MFM)

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> mostcommonlyusedmethod being reversible jump Markov chain Monte Carlo

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> difficulttousesinceapplyingittonewsituations requires one to design good reversible jump moves, which is often nontrivial, particularly in high-dimensional parameter spaces

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> infinite mixture models such as Dirichlet process mixtures (DPMs) have become popular, partly due to the existence of relatively simple and generic Markov chain Monte Carlo (MCMC)

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> These algorithmsaremadepossiblebythevarietyofcomputationally tractable representations of the Dirichlet process, including its exchangeable partition distribution, the Blackwell–MacQueen urn process (a.k.a. the Chinese restaurant process), the random discrete measure formulation, and the Sethuraman–Tiwari stick-breaking representation

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> there are MFM counterparts for each of these properties

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> main point of this article is that the MFM versions of theserepresentationsaresimpleenough,andparalleltheDPM versions closely enough, that many of the inference algorithms developed for DPMs can be directly applied to MFMs.

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> key properties of MFMs hold for any choice of prior distribution on the number of components

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> In Sections 2 and 3,we formally define the MFM and show that it gives rise to a simple exchangeable partition distribution closely paralleling that of the Dirichlet process. In Section 4, we describe the Pólya urn scheme (restaurant process), random discrete measure formulation, and stick-breaking representation for the MFM. In Section 5, we establish some asymptotic results for MFMs. In Section 6,weshowhowthepropertiesinSections 3 and 4 lead to efficient inference algorithms for the MFM. In Section 7,we compare the mixing performance of reversible jump versus our proposed algorithms

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> provide an empirical comparison between MFMs and DPMs

![[LiteratureNotes/Assets/millerMixtureModelsPrior2018/millerMixtureModelsPrior2018-3-x42-y31.png]]

![[LiteratureNotes/Assets/millerMixtureModelsPrior2018/millerMixtureModelsPrior2018-3-x307-y269.png]]

<b class="thickUnd" style="text-decoration-color: ">Quote</b>
> The primary observation on which our development relies is that the distribution on partitions induced by an MFM takes a form which is simple enough that it can be easily computed.


%% end annotations %%


%% Import Date: 2024-01-15T15:34:03.496-05:00 %%
