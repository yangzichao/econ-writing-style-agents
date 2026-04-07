# Evidence Base

Paper-by-paper summary of evidence supporting each skill rule. Reference this when you need to understand *why* a rule exists or need a concrete before/after example.

---

## Paper Index

| # | Short Title | v1 Date | Published | Journal | Revision Magnitude |
|---|---|---|---|---|---|
| 01 | Parallel Trends Functional Form | Oct 2020 | Mar 2023 | Econometrica | Major (28→12 pages) |
| 02 | Staggered Rollout | Feb 2021 | May 2023 | JPE: Micro | Major |
| 03 | What's Trending in DiD? | Jan 2022 | Jan 2023 | J. Econometrics | Minor |
| 04 | Covariate Balance | Oct 2018 | Nov 2021 | J. Applied Econometrics | Major |
| 05 | Distribution Regression | Apr 2019 | 2022 | Econometrics Journal | Moderate (31→24 pages) |
| 06 | DiD Multiple Periods | Mar 2018 | Dec 2020 | J. Econometrics | Transformative |
| 07 | Parallel Trends Event Study | Sep 2020 | 2021 | JAERE | None |
| 08 | Doubly Robust DiD | Nov 2018 | 2020 | J. Econometrics | Transformative |
| 09 | Treatment Effect Heterogeneity | Dec 2016 | 2021 | JBES | Moderate |
| 10 | Propensity Score Tests | Nov 2016 | 2019 | J. Econometrics | Major (reframed) |
| 11 | DiD Compositional Changes | Apr 2023 | forthcoming | J. Econometrics | Minor |
| 12 | Generalized PS Tests | Mar 2020 | forthcoming | J. Nonparam. Stat. | Moderate |
| 13 | DiD Practitioner's Guide | Mar 2025 | forthcoming | J. Economic Literature | None |
| 14 | DiD Continuous Treatment | Jul 2021 | forthcoming | AER | Major |
| 16 | Efficient DiD ES | Jun 2025 | — | Working paper | N/A (single version) |
| 17 | Triple Differences | May 2025 | — | Working paper | Minor |
| 18 | Javert MTE Duration | Nov 2023 | — | R&R at REStat | Moderate |
| 19 | DR Weak Overlap | Apr 2023 | — | Working paper | N/A (single version) |
| 20 | Selection Parallel Trends | Mar 2022 | — | Working paper (v14) | Transformative |
| 21 | Program Eval Censored | Apr 2016 | — | Working paper | N/A (early-career baseline) |

---

## Key Revision Insights by Paper

### 01 — Parallel Trends Functional Form
- **Abstract**: 170 → 100 words (41% reduction). Cut second main result (ATT identification equivalence) and practitioner recommendations.
- **Precision**: "monotonic" → "strictly monotonic." Added "if and essentially only if" with Remark 2 explaining the edge case.
- **Major addition**: Full falsification tests subsection (3.2) with formal statistical tests and minimum wage empirical illustration.
- **Structure**: v1 had no formal conclusion; published added Section 4 "Implications for Applied Work."
- **Rules sourced**: Abstract compression (01-abstract §2), precision hedging (03-terminology §Hedging)

### 02 — Staggered Rollout
- **Abstract**: 170 → 90 words (47% reduction). Removed narrative scaffolding and self-promotion.
- **Opening**: "Researchers are often interested in..." → "We study estimation of causal effects in staggered rollout designs."
- **Terminology**: "(as-if) randomly assigned" → "as-good-as randomly assigned." TWFE reference dropped from abstract.
- **New content**: Fisher Randomization Tests (FRT) as entirely new inference contribution.
- **Empirical**: "five times shorter" → "eight times shorter" (updated result).
- **Rules sourced**: Throat-clearing elimination (01-abstract §1), self-promotion removal (01-abstract §4)

### 03 — What's Trending in DiD?
- **Abstract**: Virtually identical between versions (rare for this corpus).
- **Major addition**: Medicaid running example threaded through the Basic Model section.
- **Content additions**: Triple differences section, sequential ignorability discussion.
- **Terminology**: "sequential random assignment" → "sequential ignorability" (correct standard term).
- **Acknowledgment**: "We thank Scott Barkowski for suggesting the title."
- **Rules sourced**: Running empirical example (02-introduction §4), survey style (06-markers §Survey)

### 04 — Covariate Distribution Balance
- **Abstract**: Complete reframing. Three setup sentences → one contribution statement.
- **Method→Purpose**: "estimates the propensity score by fully exploiting its covariate balancing property" → "aims to maximize the covariate distribution balance."
- **Branding de-emphasized**: "IPS" acronym removed from abstract; described functionally instead.
- **RCT analogy added**: "the balancing property of the propensity score resembles randomization."
- **Scope expanded**: Added LATE framework (Section 4), not just unconfoundedness.
- **Applications reduced**: Three → one.
- **Rules sourced**: Purpose-centric framing (01-abstract §5), RCT analogy (04-framing §3)

### 05 — Distribution Regression
- **Abstract**: Removed empirical findings. "slope coefficients" → "marginal effects."
- **Main text shortened**: 31 → 24 pages. Monte Carlo details moved to supplementary appendix.
- **Abbreviations**: "CH," "QR" → spelled out "conditional hazard," "quantile regression."
- **Added**: Replication files link, additional figure.
- **Rules sourced**: Empirical results removal (01-abstract §3), Monte Carlo appendix (05-revision §Cut 6)

### 06 — DiD Multiple Periods (MOST DRAMATIC TRANSFORMATION)
- **Scope**: Simple estimation paper → comprehensive "unified framework" with three explicit steps.
- **Opening**: Pedagogical preamble removed. "DID is one of the most important and popular" → "In this article, we consider identification, estimation, and inference procedures."
- **Terminology**: "individuals" → "units," "DID" → "DiD," "control group" → "comparison group."
- **New contributions**: Doubly robust estimators, treatment anticipation handling, aggregation schemes, extensive related literature section.
- **Three-step framework**: identification → aggregation → estimation/inference.
- **Rules sourced**: Framework structure (02-introduction §2), terminology (03-terminology §Standard)

### 07 — Parallel Trends Event Study (NO CHANGES)
- Virtually identical between ArXiv v1 and JAERE publication.
- Likely already polished at v1 (first version January 2020, ArXiv posted September 2020).
- Reveals Sant'Anna style markers in their "natural" state: "As so," "To the best of our knowledge," "It is worth stressing."
- **Rules sourced**: Distinctive phrases (06-markers §Phrases)

### 08 — Doubly Robust DiD (SECOND MOST DRAMATIC)
- **Scope**: One contribution → three contributions (DR consistency + efficiency bounds + DR inference).
- **Opening**: "Researchers and policy makers are often interested in..." → "Difference-in-differences (DID) methods are among the most popular procedures."
- **Terminology**: "propensity score model" → "propensity score working model." "individual" → "unit."
- **"our proposed" reduction**: Five occurrences in v1 abstract → reduced first-person possessives.
- **Software**: No mention in v1 → "open-source R package DRDID" with GitHub URL.
- **Rules sourced**: Working model terminology (03-terminology §Standard), software (02-introduction §6)

### 09 — Treatment Effect Heterogeneity
- **Contribution summary added**: v1 had none. v4 added "In summary, we contribute to the literature on different fronts."
- **Notation**: D → T (treatment indicator) to avoid confusion in duration context.
- **Specificity**: "real data" → "data from the Illinois Reemployment Bonus Experiment."
- **Trimming**: "but alternative estimators are also feasible" deleted.
- **Rules sourced**: Contribution enumeration (02-introduction §3), redundant qualifiers (05-revision §Cut 4)

### 10 — Propensity Score Tests (FUNDAMENTAL REFRAMING)
- **Conceptual shift**: From balancing-property testing (v1) to CDF-restriction testing (published). Driven by referee suggestion.
- **Framing**: "detecting propensity score misspecification" → "assess the asymptotic validity of treatment effects estimators."
- **Power hedging**: "both improves power" → "can lead to power gains."
- **Grammar**: "tests are" → "tests is" (subject-verb agreement fix). "bare" → "bear" (spelling).
- **Applied motivation added**: Potential outcomes framework (Y(1), Y(0)), ATE, ATT discussion.
- **Rules sourced**: Purpose-centric framing (04-framing §6), hedging (03-terminology §Hedging)

### 11 — DiD Compositional Changes
- **Minimal changes**: Already highly polished at v1 (April 2023).
- **Minor additions**: DML/cross-fitting extension, overlapping panel/cross-section data.
- **Micro-edit**: "doubly-robust" (hyphenated) → "doubly robust" (unhyphenated).

### 12 — Generalized PS Tests
- **Scope broadened**: GPS-specific → general conditional moment restrictions.
- **Abstract condensed dramatically.**
- **Power hedging**: "much higher power" → "attractive power properties."
- **Co-author added**: Juan Carlos Escanciano became first author.
- **British English**: Spelling conventions changed (reflecting journal style).

### 13 — DiD Practitioner's Guide
- **Nearly identical**: Only 3 months between v1 (March 2025) and published (June 2025).
- **Accessible conversational tone maintained throughout.**
- **Minor**: "whom" → "which" corrections, more precise footnotes.

### 14 — DiD Continuous Treatment (MOST EXTENSIVELY REVISED)
- **Key terminological shift**: "treatment effect heterogeneity" → "selection bias" as the central concept.
- **TWFE critique sharpened**: "hard to interpret" → "admits multiple interpretations, all with limitations."
- **"Forward engineering" concept introduced.**
- **Empirical application**: Acemoglu-Finkelstein (2008) woven into introduction with Figure 1.
- **Every sentence tightened**: "can be identified" → "are identified"; "alleviate" → "eliminate."
- **Rules sourced**: Selection bias reframing (03-terminology §Selection Bias), active voice (03-terminology §Active)

### 17 — Triple Differences
- **Claims softened**: "shows" → "highlights"; "introduces" → "can introduce."
- **Self-promotional closing replaced**: → "R package available."
- **"surprising" → "interesting"** (more measured).

### 18 — Javert MTE Duration
- **Removed "new" from "new econometric tools."**
- **Grammar**: "who" → "whom."
- **Policy recommendation removed from abstract.**
- **Practical discussion expanded**: Why censoring matters vs. binarization.

### 20 — Selection and Parallel Trends (14 VERSIONS, 4 YEARS)
- **Abstract completely rewritten.** "We investigate" → "We derive necessary and sufficient conditions."
- **Results strengthened**: Separate necessary/sufficient conditions → unified necessary-and-sufficient.
- **New contributions**: Bias decomposition, benchmarking strategies.
- **Two empirical applications added**: NSW, Medicaid expansion.
- **Practical framing**: "formal underpinnings" → "easy-to-implement strategies" and "templates."
- **AI transparency**: "We used Grammarly for grammar checking, Github Co-Pilot for coding assistance."

### 21 — Program Evaluation with Right-Censored Data (EARLY-CAREER BASELINE)
- **Generic opening**: "Assessing whether a policy has any effect..."
- **Passive/deferential tone**: "As summarized in Heckman and Vytlacil (2007)..."
- **Math-first approach**: Equations in running text on page 1.
- **Statistics vocabulary**: Glivenko-Cantelli, Donsker class, Banach space.
- **No running example, no contribution enumeration, no software package, no conclusion.**
- **Contrast with mature style demonstrates the full arc of development.**
