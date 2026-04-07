# Terminology and Voice

Word-level preferences, active voice patterns, and hedging rules derived from Sant'Anna's revision patterns.

---

## Standard Terminology Preferences

These substitutions appear consistently across multiple papers when comparing v1 to published versions.

| AVOID | USE | Source Papers |
|---|---|---|
| "individuals" | "units" | DiD Multiple Periods, Doubly Robust DiD |
| "DID" | "DiD" | DiD Multiple Periods (v1→published) |
| "control group" | "comparison group" | DiD Multiple Periods |
| "setups" | "designs" | DiD Continuous Treatment |
| "(as-if) randomly assigned" | "as-good-as randomly assigned" or "(quasi-)randomly assigned" | Staggered Rollout |
| "propensity score model" | "propensity score working model" | Doubly Robust DiD |
| "estimation procedure" | "estimators" | Doubly Robust DiD |
| "strategies" | "procedures" | DiD Continuous Treatment |
| "slope coefficients" | "marginal effects" | Distribution Regression |
| "introduces" | "proposes" | Propensity Score Tests |
| "high-dimensionality" (noun) | "high-dimensional" (adjective) | Propensity Score Tests |

### Why These Matter

- **"units" over "individuals"**: Makes the framework applicable beyond labor economics to any quasi-experimental setting (states, firms, schools, countries).
- **"DiD" over "DID"**: Matches the modern causal inference convention. This was a deliberate standardization in the DiD Multiple Periods paper.
- **"comparison group" over "control group"**: Distinguishes observational comparisons from experimental controls. You cannot "control" for treatment in an observational study.
- **"working model"**: In the semiparametric inference literature, "working model" specifically denotes a model that may be misspecified but is used for estimation. This single word addition signals engagement with the doubly robust literature and conveys technical precision.
- **"designs" over "setups"**: "Design" implies intentional structure and connects to the design-based inference tradition. "Setup" is colloquial.

---

## Precision Over Generality

Replace vague descriptions with specific mechanisms.

| VAGUE (v1 pattern) | PRECISE (published pattern) | Paper |
|---|---|---|
| "can be hard to interpret" | "admits multiple interpretations, depending on the underlying causal building block, all having important limitations" | DiD Continuous Treatment |
| "due to treatment effect heterogeneity" | "because parallel trends does not rule out selection bias" | DiD Continuous Treatment |
| "monotonic" | "strictly monotonic" | Parallel Trends Functional Form |
| "similar properties" | "asymptotically unbiased with efficiency (weakly) dominating" | Staggered Rollout |
| "improves power" | "can lead to power gains" | Propensity Score Tests |
| "much higher power" | "attractive power properties" | Generalized PS Tests |
| "tend to have severe size distortions" | "may have size distortions" | Propensity Score Tests |
| "assumption holds on the entire distribution" | "condition holds for the cumulative distribution function" | Parallel Trends Functional Form |
| "estimation and inference" | "identification, estimation, and inference" | DiD Multiple Periods |
| "for detecting propensity score misspecification" | "to assess the asymptotic validity of different treatment effects estimators that rely on the correct specification of the propensity score" | Propensity Score Tests |

### The "Selection Bias" Reframing

One of the most significant terminology shifts across Sant'Anna's corpus:

> v1: "interpreting differences in these parameters across different values of the treatment can be particularly challenging due to **treatment effect heterogeneity**"
>
> Published: "comparing these parameters across treatments is challenging because **parallel trends does not rule out selection bias**"

"Treatment effect heterogeneity" is descriptive — it names a statistical phenomenon. "Selection bias" is diagnostic — it names the causal mechanism. The published version tells the reader *why* the problem exists, not just *that* it exists.

---

## Active Voice and Direct Phrasing

| PASSIVE / WEAK (v1) | ACTIVE / DIRECT (published) | Paper |
|---|---|---|
| "can be identified" | "are identified" | DiD Continuous Treatment |
| "We aim to fill this important gap" | "We provide a unified framework" | DiD Multiple Periods |
| "We investigate what selection mechanisms are compatible" | "We derive necessary and sufficient conditions" | Selection and Parallel Trends |
| "alleviate these challenges" | "eliminate selection bias" | DiD Continuous Treatment |
| "do not suffer from these drawbacks" | "avoid these drawbacks" | DiD Continuous Treatment |
| "perhaps too many, potentially making the analysis harder" | "researchers may want to aggregate them" | DiD Multiple Periods |
| "one can combine them to form" | "We derive... and propose" | Doubly Robust DiD |
| "These extensions are currently being explored by us" | "We leave the detailed discussion for future research" | Covariate Balance |

### The Confidence Gradient

Sant'Anna's verb choices track a confidence gradient from v1 to published:
- **Exploratory** (v1): "investigate," "aim to," "try to address," "suggest"
- **Intermediate**: "consider," "discuss," "study"
- **Definitive** (published): "derive," "show," "prove," "provide," "establish"

---

## Hedging Rules

### When to Hedge

Hedge only when mathematical precision demands it. Every hedge should have a specific technical reason.

| Hedge | When to Use | Example Paper |
|---|---|---|
| "if and essentially only if" | An edge case exists but is practically irrelevant | Parallel Trends Functional Form — Remark 2 explains the edge case |
| "(weakly) dominating" | Efficiency dominance holds with equality in some cases | Staggered Rollout |
| "can lead to power gains" | Power improvement is conditional on context | Propensity Score Tests |
| "working models" (implied hedge) | The model may be misspecified | Doubly Robust DiD |

### When NOT to Hedge

Do not use vague hedges. Replace with specific mechanisms.

| VAGUE HEDGE | REPLACE WITH |
|---|---|
| "perhaps" | Remove or state the condition explicitly |
| "somewhat" | Quantify or remove |
| "potentially making the analysis harder" | Name the specific difficulty |
| "in some sense" | Remove — either it is or it isn't |
| "to some extent" | Quantify |
| "it seems that" | "We show that" or remove |

### The Hedging Correction Pattern

Across multiple papers, v1 over-hedges and the published version sharpens:

**Paper: Triple Differences (v1 → latest)**
> v1: "shows" → latest: "highlights" (softened appropriately — the paper doesn't prove, it illustrates)
>
> v1: "introduces" → latest: "can introduce" (hedged appropriately — the bias is conditional)

**Paper: Propensity Score Tests (v1 → published)**
> v1: "both improves power" → published: "can lead to power gains" (the improvement is context-dependent)

Appropriate hedging increases precision. Vague hedging decreases it.

---

## Abbreviation Rules

**From v1 to published in Distribution Regression:**
> v1: "CH" (conditional hazard), "QR" (quantile regression) — abbreviations used freely
>
> Published: "conditional hazard," "quantile regression" — spelled out for clarity

**Rule**: Spell out terms on first use. In the introduction, prefer full terms even if abbreviated later. The exception is universally known abbreviations (DiD, ATT, TWFE, OLS).

---

## "Assumption" vs. "Condition"

**Paper: Parallel Trends Functional Form (v1 → Econometrica 2023)**
> v1: "the parallel trends **assumption** holds"
>
> Published: "a stronger 'parallel trends'-type **condition** holds"

"Assumption" is something imposed by the researcher. "Condition" is something to be verified or checked. The shift from "assumption" to "condition" in published versions signals that the paper provides tools for verification, not just identification under assumptions.

---

## First-Person Usage

**Pattern**: Reduce "our proposed" and increase "the proposed."

**Paper: Doubly Robust DiD**
> v1: "our proposed estimators" (5 occurrences in abstract)
>
> Published: "the proposed estimators" (reduced first-person possessives)

Use "we" for actions ("We derive," "We show") but "the" for objects ("the proposed estimator," "the efficient estimator"). This keeps the contribution claims in active voice while making the methods sound more universal.
