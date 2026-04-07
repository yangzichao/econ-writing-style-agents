# Revision Patterns

What to cut, what to add, and what to expand when revising a paper — based on the systematic differences between Sant'Anna's ArXiv v1 drafts and published versions.

---

## What to Cut

### 1. Background Preambles
Remove "X is important because..." opening paragraphs. Every paper analyzed showed compression or removal of background setup.

**Evidence**: In 12 of 16 papers with multiple versions, the opening paragraph was either deleted or compressed by more than 50%.

### 2. Narrative Scaffolding in Abstract
Do not walk the reader through your logical process step by step. State results directly.

> CUT: "The efficient estimator is not feasible in practice because it requires knowledge of the optimal weights to be placed on pre-treatment outcomes. However, the optimal weights can be estimated from the data, and in large datasets the plug-in estimator that uses the estimated weights has similar properties to the 'oracle' efficient estimator."
>
> KEEP: "A feasible plug-in version of the efficient estimator is asymptotically unbiased with efficiency (weakly) dominating that of existing approaches."

### 3. Specific Empirical Findings from Abstract
In methods papers, describe the application but not the results.

**Paper: Distribution Regression** — Removed "nonlinear, non-monotone effect... more pronounced for workers subjected to liquidity constraints" from abstract.
**Paper: DiD Multiple Periods** — Removed specific percentages ("2.3% to 13.6%") from introduction.

### 4. Redundant Qualifiers
Sentences that add no information:

> "We focus on the Series Logit Estimator proposed by Hirano et al. (2003), **but alternative estimators are also feasible.**"

The bold clause adds nothing — delete it.

> "they are consistent against any **(one and two sided)** nonparametric fixed alternative"

The parenthetical is redundant — "any" already implies both.

### 5. Self-Congratulatory Language
Phrases to eliminate:
- "of independent interest"
- "important addition to the researcher's toolkit"
- "one of the most important and popular"
- "provides the most precise estimates to date"

Let the quantitative claims (e.g., "eight times shorter confidence intervals") speak for themselves.

### 6. Detailed Monte Carlo from Main Text
Move Monte Carlo simulation details to a supplementary appendix.

**Paper: Distribution Regression (v1 → EJ 2022)** — v1 had a full Section 5 on Monte Carlo. Published version: "Section 6 briefly summarizes the results of the Monte Carlo simulations — detailed discussion is presented in the Supplementary Appendix." Paper went from 31 to 24 pages.

### 7. Multiple Empirical Applications
Reduce from many to one focused application.

**Paper: Covariate Balance** — v1 had three applications (401k, right heart catheterization, child soldiering). Published kept one (401k).
**Paper: Doubly Robust DiD** — v1 had two applications (LaLonde/NSW, Vietnam recentralization). Published kept one.

### 8. Corrections of Prior Literature in Main Text
Remove direct engagement with (and correction of) specific prior claims.

**Paper: Parallel Trends Functional Form** — v1 Remark 10 quoted and corrected Kahn-Lang and Lang (2018) at length. Published version removed this entirely, briefly noting in the introduction "we provide the first full characterization."

---

## What to Add

### 1. Falsification Tests / Testable Implications
Transform theoretical results into actionable diagnostics.

**Paper: Parallel Trends Functional Form (v1 → Econometrica 2023)**
> v1 Remark 6 briefly mentions "it is possible to test whether the integrated curve C(y) is concave."
>
> Published: Full subsection 3.2 on "Testable Implications of Invariance to Transformations" with formal statistical testing procedures, moment inequality methods, and a complete empirical illustration using minimum wage data from Cengiz et al. (2019).

This is the single most impactful addition pattern: a paper that merely characterizes becomes a paper that enables empirical practice.

### 2. Running Empirical Examples
Thread a concrete application through the paper.

**Paper: What's Trending in DiD?** — Published version added Medicaid expansion as a running example.
**Paper: DiD Continuous Treatment** — Published version added Acemoglu-Finkelstein application with Figure 1 in the introduction.

### 3. Formal Contribution Enumeration
Add a numbered list of contributions after the motivation.

**Pattern**: "We contribute to the [X] literature in different fronts. First, ... Second, ... Third, ..."

### 4. Open-Source Software
R/Stata package with name and GitHub link.

**Evolution**: Early papers (2016): "R codes for implementing the treatment effects estimators are available from the author." → Later papers (2020+): "Open-source software for implementing the proposed policy evaluation tools is available" with named packages (DRDID, did, staggered, IPS, kmte) and GitHub URLs.

### 5. Heuristic Summaries After Technical Results
Add "At the practical level,..." or "Heuristically,..." paragraphs.

### 6. Formal Lemmas
Elevate key equations to formal lemma statements.

**Paper: Covariate Balance** — v1 had the covariate balancing property as equation (1). Published elevated it to Lemma 2.1 with explicit conditions. This makes the result citable and signals its importance.

### 7. Simultaneous Inference
Upgrade from pointwise to simultaneous confidence bands.

**Paper: DiD Multiple Periods** — Published specifies "simultaneous (instead of pointwise) inference" — a technical distinction absent from v1's abstract.

### 8. Replication Files
GitHub links to replication code.

**Paper: Distribution Regression** — Published adds "All our replication files are available at https://github.com/pedrohcgs/KMDR-replication."

---

## What to Expand

### 1. Doubly Robust Extensions
Always consider adding DR estimation alongside IPW and outcome regression.

**Paper: DiD Multiple Periods** — v1 proposed a simple two-step IPW estimator. Published version added outcome regression, IPW, and doubly robust estimands as three parallel approaches.

**Paper: Doubly Robust DiD** — v1 proposed DR consistency. Published added semiparametric efficiency bounds, panel vs. cross-section comparisons, and DR inference — three entirely new contributions.

### 2. Treatment Anticipation
Discuss explicitly in staggered designs.

**Paper: DiD Multiple Periods (published)** — Added explicit treatment anticipation discussion: "our proposed estimands explicitly reflect these assumptions."

### 3. Covariates Role
Expand discussion of conditional vs. unconditional parallel trends.

**Paper: DiD Multiple Periods (published)** — Added: "To the best of our knowledge, this paper is the first to show how one can allow for covariate-specific trends across groups in DiD setups with variation in treatment timing."

### 4. Practical Recommendations
Add boxed "Recommendations" or bold-header guidance sections.

**Paper: What's Trending in DiD?** — Used boxed recommendation sections throughout. The published version is structured as a practitioner guide, not just a literature review.

**Paper: Selection and Parallel Trends (v14)** — Added bold-face headers: "Restrictions on selection are unavoidable in DiD designs."

### 5. Related Literature Section
Formalize and expand.

Every paper that went through revision formalized its literature discussion — from scattered citations woven through the introduction to a dedicated "Related Literature" subsection.

---

## Structural Changes

### Papers That Grew During Revision
- DiD Multiple Periods: Simple estimation paper → comprehensive unified framework
- Doubly Robust DiD: One contribution (DR consistency) → three contributions (+ efficiency bounds + DR inference)
- What's Trending in DiD?: 54 → 58 pages (added triple differences, sequential ignorability, running example)

### Papers That Shrank During Revision
- Parallel Trends Functional Form: 28 → 12 pages (Econometrica short-paper format; cut second main result)
- Distribution Regression: 31 → 24 pages (Monte Carlo moved to appendix)

### Papers That Were Already Polished at v1
- Role of Parallel Trends in Event Study Settings: Virtually no changes
- DiD Compositional Changes: Minimal changes
- DiD Practitioner's Guide: Nearly identical (only 3 months between versions)

These suggest that Sant'Anna's later papers benefit from the revision lessons of earlier work — the mature style is internalized before posting to ArXiv.
