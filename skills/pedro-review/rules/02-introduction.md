# Introduction Rules

Principles for writing and revising paper introductions in Pedro Sant'Anna's style.

---

## Rule 1: Open with Contribution, Not Context

The first sentence should announce what the paper does, not how important the field is.

### The Evolution of Sant'Anna's Opening Sentences

**Early career (2016) — Generic:**
> "Assessing whether a policy has any effect on a particular outcome has been one of the main concerns in empirical research."

**Mid career (2018, v1 drafts) — Field importance:**
> "Difference-in-Differences (DID) is one of the most important and popular designs for evaluating causal effects of policy changes."

**Mature style (2020+, published) — Direct contribution:**
> "This paper provides a new perspective on difference-in-differences (DiD) identification through the lens of how units select into treatment."

**Advanced technique — Quantified empirical hook:**
> "Difference-in-Differences (DiD) and Event Study (ES) designs are among the most widely used empirical strategies in economics and related fields. For instance, recent data indicates that over 30% of 2024 NBER applied microeconomics working papers mention DiD or ES."

This progression — generic → field-importance → direct → empirical hook — tracks Sant'Anna's growth from a statistics-oriented PhD student to a leading applied econometrician.

---

## Rule 2: Use a Numbered Framework Structure

For methods papers, organize the introduction around an explicit multi-step framework.

**Paper: DiD Multiple Periods (published in JoE 2021)**
The published version introduced a three-step framework entirely absent from v1:
> "Our approach proceeds in three steps: (i) identification of policy-relevant disaggregated causal parameters; (ii) aggregation of these parameters to form summary measures of the causal effects; and (iii) estimation and inference about these different target parameters."

This framework (identification → aggregation → estimation/inference) became the paper's organizing principle and is now standard in the DiD literature.

---

## Rule 3: Enumerate Contributions Explicitly

After the motivation paragraph, provide a clear list of contributions.

**Pattern**: "We contribute to the [X] literature in different fronts."

**Paper: Doubly Robust DiD (published in JoE 2020)**
> "We contribute to the DID literature in different fronts. First, we derive doubly robust (DR) estimands for the ATT under DID settings and propose DR DID estimators. Second, we derive the semiparametric efficiency bounds for the ATT in DID designs. Third, we show that one can sometimes construct doubly robust DID estimators that are also doubly robust for inference."

**Paper: Treatment Effect Heterogeneity (v4, published in JBES 2021)**
The v1 had no contribution summary. The published v4 added:
> "In summary, we contribute to the literature on different fronts. This paper is the first to propose a family of nonparametric tests for TE heterogeneity that (i) can easily accommodate a variety of research designs and (random) censoring and (ii) are able to detect local alternatives converging to null at the parametric rate."

---

## Rule 4: Add a Running Empirical Example

Ground abstract notation in a concrete real-world example early in the introduction.

**Paper: What's Trending in DiD? (published in JoE 2023)**
The v1 introduced variables abstractly. The published version added the Medicaid running example:
> "For example, Y_{i,t} could be the fraction of people with insurance coverage in state i in year t, while D_i could be an indicator for whether the state expanded Medicaid."
>
> "In our motivating example, the parallel trends assumption says that the average change in insurance coverage for expansion and non-expansion states would have been the same..."

This example is threaded through the entire Basic Model section, transforming every equation from abstract notation into an interpretable claim.

**Paper: DiD Continuous Treatment (published version)**
The published version added a detailed preview of the Acemoglu and Finkelstein (2008) Medicare application, including Figure 1 showing TWFE event-study estimates directly in the introduction. The v1 had no empirical preview.

**Preferred running examples**: Medicaid expansion, minimum wage effects, NSW training program, procedural justice training for police officers.

---

## Rule 5: Create a Formal "Related Literature" Subsection

Separate literature discussion from the contribution statement.

**Paper: DiD Multiple Periods (published in JoE 2021)**
The v1 wove literature discussion throughout the introduction. The published version added a formal "Recent Related Literature" subsection with systematic comparisons to de Chaisemartin and D'Haultfoeuille (2020), Sun and Abraham (2020), and Athey and Imbens (2018).

**Paper: Covariate Balance (published in JAE 2022)**
The v1 wove literature throughout. The published version added a formal "Related literature:" subsection at the end of the introduction, systematically comparing to Graham et al. (2012), Imai and Ratkovic (2014), Diaz et al. (2015), Fan et al. (2016).

---

## Rule 6: Announce Open-Source Software in the Introduction

Not the abstract. Include package name and GitHub URL.

> "All proposed policy evaluation tools discussed in this article can be implemented via the open-source R package DRDID, which is freely available from GitHub (https://pedrohcgs.github.io/DRDID/)."

> "An R package implementing these estimators, staggered, is available at https://github.com/jonathandroth/staggered."

This pattern appears in virtually every published Sant'Anna paper from 2020 onwards. The v1 drafts either had no software mention or a brief footnote ("R codes are available from the author").

---

## Rule 7: Shift from Tentative to Confident Framing

| v1 Draft Pattern | Published Pattern |
|---|---|
| "We aim to fill this important gap" | "We provide a unified framework" |
| "We investigate what selection mechanisms are compatible" | "We derive necessary and sufficient conditions" |
| "This paper tries to address..." | "This paper shows..." |
| "One of the advantages of DiD is that..." | "This paper provides a new perspective on DiD..." |

The shift reflects not just editorial polish but the maturation of results through the revision process. v1 language is exploratory because the results are still being developed; published language is definitive because the results have survived peer review.

---

## Rule 8: Remove Specific Empirical Results from the Introduction

**Paper: DiD Multiple Periods**
> v1 introduction: "2.3% to 13.6% lower teen employment" (specific percentages)
>
> Published introduction: "using our approach leads to qualitatively different results than results from the TWFE estimator" (qualitative summary)

**Paper: DiD Continuous Treatment**
The v1 had no empirical preview. The published version added Figure 1 and the Acemoglu-Finkelstein application — but describes patterns, not specific numbers, in the introduction.

The pattern: preview the *type* of finding and its *direction*, but save specific magnitudes for the application section.

---

## Rule 9: Draw Explicit RCT Parallels

When discussing observational methods, connect to what randomization achieves.

**Paper: Covariate Balance (published in JAE 2022)**
> "Indeed, the balancing property of the propensity score resembles randomization: when the data come from a randomized control trial (RCT) with perfect compliance, the entire covariate distributions among different treatment groups are balanced and, therefore, all measurable, integrable functions of the covariates are indeed balanced."

**Paper: Staggered Rollout (published in JPE:Micro 2023)**
The published version added concrete examples of papers that justify parallel trends via quasi-random timing (Deshpande and Li 2019, Fadlon and Nielsen 2021, Parker et al. 2013), explicitly connecting the paper's assumption to real-world plausibility.

**Paper: Covariate Balance, citing Rubin:**
> "As advocated by Rubin (2007, 2008), this separation [design vs. analysis] is useful as it simultaneously mimics RCTs and avoids potential data snooping problems."
