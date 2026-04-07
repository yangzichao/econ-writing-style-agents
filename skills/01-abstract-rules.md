# Abstract Rules

Principles for writing and revising abstracts in Pedro Sant'Anna's style. Derived from comparing 16 ArXiv v1 abstracts with their published counterparts.

---

## Rule 1: Eliminate Throat-Clearing

Never open an abstract with generic background. The first sentence must state the paper's contribution.

**Diagnostic**: If the first sentence does not contain "propose," "study," "analyze," "derive," or "show," it is throat-clearing.

### Before / After Examples

**Paper: Covariate Distribution Balance (ArXiv v1 → JAE 2022)**
> BAD: "The propensity score plays an important role in causal inference with observational data. Once the propensity score is available, one can use it to estimate a variety of causal effects in a unified setting. Despite this appeal, a main practical difficulty arises because..."
>
> GOOD: "This paper proposes new estimators for the propensity score that aim to maximize the covariate distribution balance among different treatment groups."

Three setup sentences collapsed into one contribution statement.

**Paper: Staggered Rollout (ArXiv v1 → JPE:Micro 2023)**
> BAD: "Researchers are often interested in the causal effect of treatments that are rolled out to different units at different points in time. This paper studies how to efficiently estimate..."
>
> GOOD: "We study estimation of causal effects in staggered rollout designs, i.e. settings where there is staggered treatment adoption and the timing of treatment is as-good-as randomly assigned."

The "researchers are interested" opener is the single most common throat-clearing pattern in economics.

**Paper: DiD Multiple Time Periods (ArXiv v1 → JoE 2021)**
> BAD: "Difference-in-Differences (DID) is one of the most important and popular designs for evaluating causal effects of policy changes. In its standard format, there are two time periods and two groups..."
>
> GOOD: "In this article, we consider identification, estimation, and inference procedures for treatment effect parameters using Difference-in-Differences (DiD)..."

**Paper: Doubly Robust DiD (ArXiv v1 → JoE 2020)**
> BAD: "Researchers and policy makers are often interested in evaluating the causal effects of a given program or treatment on different outcomes of interest. Although randomized experiments are often viewed as the 'gold standard'..."
>
> GOOD: "Difference-in-differences (DID) methods are among the most popular procedures practitioners adopted to conduct policy evaluation with observational data."

---

## Rule 2: Compress Aggressively — Target 30–50% Reduction

Observed compression rates across published papers:
- Parallel Trends Functional Form: 170 → 100 words (41% reduction)
- Staggered Rollout: 170 → 90 words (47% reduction)
- Covariate Balance: ~150 → ~100 words (33% reduction)

### What to Remove

1. **Asymptotic properties**: "sqrt(n)-consistent and asymptotically normal," "admits an asymptotic linear representation" — these belong in the body, not the abstract.

2. **Narrative scaffolding**: Do not walk the reader through the logic step by step.
   > BAD: "The efficient estimator is not feasible in practice because it requires knowledge of the optimal weights to be placed on pre-treatment outcomes. However, the optimal weights can be estimated from the data, and in large datasets the plug-in estimator that uses the estimated weights has similar properties to the 'oracle' efficient estimator."
   >
   > GOOD: "A feasible plug-in version of the efficient estimator is asymptotically unbiased with efficiency (weakly) dominating that of existing approaches."

3. **Long comma-separated virtue lists**: "easy to implement, have close-form representation, are fully data-driven upon estimation of nuisance parameters, and do not rely on parametric distributional assumptions, shape restrictions, or on restricting the potential treatment effect heterogeneity" — keep only the most distinctive properties.

---

## Rule 3: Remove Empirical Results from the Abstract

In methods papers, the abstract describes the method, not the application findings.

**Paper: Distribution Regression (ArXiv v1 → EJ 2022)**
> BAD: "Our results suggest that, on average, an increase in unemployment benefits is associated with a nonlinear, non-monotone effect on the unemployment duration distribution and that such an effect is more pronounced for workers subjected to liquidity constraints."
>
> GOOD: "We apply our proposal to study the effects of unemployment benefits on unemployment duration."

**Paper: DiD Multiple Periods (ArXiv v1 → JoE 2021)**
The v1 introduction previewed specific percentages ("2.3% to 13.6% lower teen employment"). The published version gives only: "using our approach leads to qualitatively different results than results from the TWFE estimator."

---

## Rule 4: Remove Self-Promotion

Let quantitative claims speak for themselves. Do not editorialize about the significance of your own results.

**Paper: Staggered Rollout (ArXiv v1 → JPE:Micro 2023)**
> BAD: "As an empirical contribution of independent interest, our application provides the most precise estimates to date on the effectiveness of procedural justice training programs for police officers."
>
> GOOD: "In an application to a training program for police officers, confidence intervals for the proposed estimator are as much as eight times shorter than for existing approaches."

The phrase "of independent interest" is a flag for self-promotion.

---

## Rule 5: Purpose-Centric, Not Method-Centric

Describe what the method *achieves*, not what it *does technically*.

**Paper: Covariate Balance (ArXiv v1 → JAE 2022)**
> METHOD-CENTRIC: "estimates the propensity score by fully exploiting its covariate balancing property"
>
> PURPOSE-CENTRIC: "aims to maximize the covariate distribution balance among different treatment groups"

> METHOD-CENTRIC: "based on integrated moment conditions"
>
> PURPOSE-CENTRIC: "making the underlying covariate distribution of different treatment groups as close to each other as possible"

This also applies to the "IPS" branding: the v1 abstract introduced and promoted the "IPS" acronym six times. The published abstract uses "the proposed propensity score estimator" — describing the object rather than naming it.

---

## Rule 6: Add Keywords and Scope Precision

Published versions consistently add:
- Formal **keywords** below the abstract
- Precise scope qualifiers: "strictly monotonic" instead of "monotonic"; "simultaneous (instead of pointwise) inference"
- New contribution dimensions not in v1: falsification tests, efficiency bounds, doubly robust inference

---

## Rule 7: Software Belongs in the Introduction, Not the Abstract

**Paper: Covariate Balance**
> v1 abstract: "An implementation of the proposed methods is provided in the new package IPS for R."
>
> Published: Software mention moved to the introduction with a GitHub URL.

Exception: JBES and some applied journals accept software mentions in the abstract. Match journal norms.
