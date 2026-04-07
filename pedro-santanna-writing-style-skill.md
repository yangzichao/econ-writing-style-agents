# Pedro H.C. Sant'Anna Writing Style Review Agent

> A comprehensive skill derived from analyzing 20+ economics papers by Pedro H.C. Sant'Anna, comparing early drafts (ArXiv v1) with final published versions across top journals (Econometrica, Journal of Econometrics, JPE: Micro, JBES, JAERE, AER, JEL). This skill captures his mature writing style, revision patterns, and editorial principles for use as a writing style review agent.

---

## How to Use This Skill

When reviewing or editing an economics paper, apply the following principles in order:

1. **Structure Review** — Check overall paper architecture
2. **Abstract Review** — Apply the abstract compression principles
3. **Introduction Review** — Apply the opening, framing, and contribution rules
4. **Body Review** — Check terminology, precision, and tone
5. **Conclusion Review** — Check for forward-looking, contribution-anchored closing
6. **Line-Level Polish** — Apply sentence-level revision patterns

---

## 1. Abstract Principles

### 1.1 Eliminate Throat-Clearing
**Rule**: Never open an abstract with generic background statements. Start with the paper's contribution.

| BAD (v1 pattern) | GOOD (published pattern) |
|---|---|
| "The propensity score plays an important role in causal inference with observational data. Once the propensity score is available, one can use it to..." | "This paper proposes new estimators for the propensity score that aim to maximize the covariate distribution balance among different treatment groups." |
| "Researchers are often interested in the causal effect of treatments that are rolled out to different units at different points in time. This paper studies how to..." | "We study estimation of causal effects in staggered rollout designs, i.e. settings where there is staggered treatment adoption and the timing of treatment is as-good-as randomly assigned." |
| "Difference-in-Differences (DID) is one of the most important and popular designs for evaluating causal effects of policy changes. In its standard format..." | "In this article, we consider identification, estimation, and inference procedures for treatment effect parameters using Difference-in-Differences (DiD)..." |

**Diagnosis**: If the first sentence of the abstract does not contain the word "propose," "study," "analyze," "derive," or "show," it is likely throat-clearing.

### 1.2 Compress Aggressively (Target 30-50% Reduction)
- Remove technical details that belong in the body (e.g., "sqrt(n)-consistent and asymptotically normal," "admits an asymptotic linear representation")
- Remove narrative scaffolding (e.g., "The efficient estimator is not feasible in practice because it requires knowledge of the optimal weights. However, the optimal weights can be estimated from the data...")
- State results directly: "A feasible plug-in version of the efficient estimator is asymptotically unbiased with efficiency (weakly) dominating that of existing approaches."

### 1.3 Remove Empirical Results from Abstract
**Rule**: In methods papers, the abstract should describe the methodological contribution, not preview specific empirical findings.

| BAD | GOOD |
|---|---|
| "Our results suggest that, on average, an increase in unemployment benefits is associated with a nonlinear, non-monotone effect on the unemployment duration distribution" | "We apply our proposal to study the effects of unemployment benefits on unemployment duration." |

### 1.4 Remove Self-Promotion
**Rule**: Let quantitative claims speak for themselves. Do not editorialize.

| BAD | GOOD |
|---|---|
| "As an empirical contribution of independent interest, our application provides the most precise estimates to date on the effectiveness of procedural justice training programs for police officers." | "In an application to a training program for police officers, confidence intervals for the proposed estimator are as much as eight times shorter than for existing approaches." |

### 1.5 Purpose-Centric, Not Method-Centric
**Rule**: Describe what the method achieves, not what it does technically.

| BAD | GOOD |
|---|---|
| "estimates the propensity score by fully exploiting its covariate balancing property" | "aims to maximize the covariate distribution balance among different treatment groups" |
| "based on integrated moment conditions" | "making the underlying covariate distribution of different treatment groups as close to each other as possible" |

---

## 2. Introduction Principles

### 2.1 Open with Contribution, Not Context
**Rule**: The first sentence should announce what the paper does or studies, not how important the field is.

| BAD (early-career / v1 pattern) | GOOD (mature / published pattern) |
|---|---|
| "Assessing whether a policy has any effect on a particular outcome has been one of the main concerns in empirical research." | "This paper provides a new perspective on difference-in-differences (DiD) identification through the lens of how units select into treatment." |
| "Researchers and policy makers are often interested in evaluating the causal effects of a given program or treatment on different outcomes of interest." | "Difference-in-differences (DID) methods are among the most popular procedures practitioners adopted to conduct policy evaluation with observational data." |

**Advanced technique**: For maximum impact, open with a quantified empirical hook:
> "Difference-in-Differences (DiD) and Event Study (ES) designs are among the most widely used empirical strategies in economics and related fields. For instance, recent data indicates that over 30% of 2024 NBER applied microeconomics working papers mention DiD or ES."

### 2.2 Use the Three-Step Framework Structure
For methods papers, organize the introduction around a clear numbered framework:
> "Our approach proceeds in three steps: (i) identification of policy-relevant disaggregated causal parameters; (ii) aggregation of these parameters to form summary measures of the causal effects; and (iii) estimation and inference about these different target parameters."

### 2.3 Enumerate Contributions Explicitly
**Rule**: After the motivation, provide a clear enumeration of contributions using "We contribute to the [X] literature in different fronts" or "We provide [N] characterizations."

Example:
> "We contribute to the DID literature in different fronts. First, we derive doubly robust estimands for the ATT. Second, we derive the semiparametric efficiency bounds. Third, we show that one can sometimes construct estimators that are also doubly robust for inference."

### 2.4 Add a Running Empirical Example
**Rule**: Ground abstract notation in a concrete, real-world example early in the introduction.

| BAD | GOOD |
|---|---|
| "The causal estimand of primary interest is tau_2 = E[Yi2(1) - Yi2(0) | Di = 1]." | "The causal estimand of primary interest is tau_2 = E[Yi2(1) - Yi2(0) | Di = 1]. In our motivating example, tau_2 would be the average effect of Medicaid expansion on insurance coverage in period 2 for the states who expanded Medicaid." |

Preferred running examples from Sant'Anna's papers: Medicaid expansion, minimum wage effects, NSW training program, procedural justice training for police officers.

### 2.5 Formal "Related Literature" Subsection
**Rule**: Separate literature discussion from the contribution. Create a dedicated "Related literature" or "Recent Related Literature" subsection at the end of the introduction.

### 2.6 Announce Open-Source Software
**Rule**: Mention R/Stata/Python packages by name with GitHub links in the introduction (not the abstract).
> "All proposed policy evaluation tools discussed in this article can be implemented via the open-source R package DRDID, which is freely available from GitHub."

---

## 3. Terminology & Vocabulary Rules

### 3.1 Standard Terminology Preferences
| AVOID | USE |
|---|---|
| "individuals" | "units" |
| "DID" | "DiD" |
| "control group" | "comparison group" |
| "setups" | "designs" |
| "(as-if) randomly assigned" | "as-good-as randomly assigned" or "(quasi-)randomly assigned" |
| "propensity score model" | "propensity score working model" |
| "estimation procedure" | "estimators" |
| "strategies" | "procedures" |
| "slope coefficients" | "marginal effects" |

### 3.2 Precision Over Generality
| VAGUE | PRECISE |
|---|---|
| "can be hard to interpret" | "admits multiple interpretations, depending on the underlying causal building block, all having important limitations" |
| "due to treatment effect heterogeneity" | "because parallel trends does not rule out selection bias" |
| "monotonic" | "strictly monotonic" |
| "similar properties" | "asymptotically unbiased with efficiency (weakly) dominating" |
| "improves power" | "can lead to power gains" |

### 3.3 Active Voice and Direct Phrasing
| PASSIVE / WEAK | ACTIVE / DIRECT |
|---|---|
| "can be identified" | "are identified" |
| "We aim to fill this important gap" | "We provide a unified framework" |
| "We investigate what selection mechanisms are compatible" | "We derive necessary and sufficient conditions" |
| "The treatment effect heterogeneity across different values of the treatment can be particularly challenging" | "Comparing these parameters across treatments is challenging because parallel trends does not rule out selection bias" |
| "alleviate these challenges" | "eliminate selection bias" |
| "do not suffer from these drawbacks" | "avoid these drawbacks" |

### 3.4 Hedging Rules
**When to hedge**: Only when mathematical precision demands it.
- "if and essentially only if" — when an edge case exists but is practically irrelevant
- "(weakly) dominating" — when efficiency dominance holds with equality in some cases
- "can lead to power gains" — when power improvement is conditional on context

**When NOT to hedge**: Do not use vague hedges like "perhaps," "somewhat," or "potentially making the analysis harder." Replace with specific mechanisms.

---

## 4. Framing & Motivation Patterns

### 4.1 Problem → Solution Framing (Not Problem → Problem)
**Rule**: Frame issues as features to be addressed, not as obstacles.

| PROBLEM-ORIENTED | SOLUTION-ORIENTED |
|---|---|
| "in some applications there are perhaps too many group-time ATTs, potentially making the analysis of the effectiveness of the policy intervention harder" | "Our framework acknowledges that in some applications there may be many group-time average treatment effects and researchers may want to aggregate them into different summary causal effect measures." |

### 4.2 Intuition Before Math
**Rule**: After a technical result, add a plain-language "heuristic" summary.

> "At the practical level, one can think of the IPS as an estimation procedure that attempts to estimate the unknown parameters by making the underlying covariate distribution of different treatment groups as close to each other as possible."

Or use the explicit "Heuristically,..." opener:
> "Heuristically, our proposed procedure attempts to estimate a propensity score model by making the underlying covariate distribution of different treatment groups as close to each other as possible."

### 4.3 RCT Analogy
**Rule**: When discussing observational methods, draw explicit parallels to what randomization achieves:
> "Indeed, the balancing property of the propensity score resembles randomization: when the data come from a randomized control trial (RCT) with perfect compliance, the entire covariate distributions among different treatment groups are balanced."

### 4.4 Forward Engineering Framing
For TWFE critiques and alternative estimators, frame the paper as "forward engineering" — decomposing the problem to understand what popular estimands actually estimate, then building better alternatives:
> "The ideas discussed above are in the spirit of what Mogstad and Torgovitsky (2024) call forward engineering."

---

## 5. Revision Patterns (What to Cut, What to Add)

### 5.1 What to Cut in Revisions
1. **Background preambles**: Remove "X is important because..." opening paragraphs
2. **Narrative structure in abstract**: Remove "The oracle is infeasible... However, we can estimate it..." storytelling
3. **Specific empirical findings from abstract**: Keep in the body, not the abstract
4. **Redundant qualifiers**: "but alternative estimators are also feasible" — adds nothing
5. **Unnecessary parenthetical asides**: "(one and two sided)" when "any" already implies both
6. **Self-congratulatory language**: "important addition to the toolkit," "of independent interest"
7. **Detailed Monte Carlo results from main text**: Move to supplementary appendix
8. **Multiple empirical applications**: Reduce from three to one focused application

### 5.2 What to Add in Revisions
1. **Falsification tests / testable implications**: Transform theoretical results into actionable tests
2. **Running empirical examples**: Thread a concrete application through the paper
3. **Formal contribution enumeration**: Numbered list of contributions in the introduction
4. **Open-source software**: R/Stata package with GitHub link
5. **Heuristic summaries after technical results**: "At the practical level..."
6. **Formal Lemmas**: Elevate key equations to formal lemmas for citability
7. **Simultaneous inference**: Upgrade from pointwise to simultaneous confidence bands
8. **Replication files**: GitHub links to replication code and data

### 5.3 What to Expand in Revisions
1. **Doubly robust extensions**: Always consider adding DR estimation alongside IPW and OR
2. **Treatment anticipation**: Discuss explicitly in staggered designs
3. **Covariates role**: Expand discussion of conditional vs. unconditional parallel trends
4. **Practical recommendations**: Add boxed "Recommendations" or bold-header guidance sections
5. **Related literature section**: Formalize and expand

---

## 6. Structural Markers & Distinctive Style

### 6.1 Characteristic Phrases
- "As so," — transition phrase (distinctive Sant'Anna marker)
- "To the best of our knowledge" — before novelty claims
- "It is worth stressing" / "It is worth mentioning" — emphasis markers
- "We contribute to the [X] literature in different fronts" — contribution intro
- "transparency and objectivity in the analysis" — citing Rubin (2007, 2008)
- "fear not!" — in pedagogical/survey contexts for reader reassurance
- "easy-to-implement" — describing practical tools

### 6.2 Paper Architecture Evolution
**Early career** (2016): Generic opening → Math-first → Examples late → No conclusion
**Mature style** (2020+): Empirical hook → Intuition-first → Formal results → Running example → Practical implications → Software → Conclusion

### 6.3 Survey/Review Paper Style
For review/synthesis papers, use:
- Taxonomic framing: "canonical model + three relaxations"
- Boxed "Recommendations" sections throughout
- Running examples threaded from introduction through each section
- Tables of software packages with links
- Practitioner checklists

---

## 7. Sentence-Level Polish Checklist

When reviewing a manuscript line by line, check for:

- [ ] **First sentence of abstract**: Does it state the contribution? (Not background)
- [ ] **Abstract length**: Can it be cut 30-50%? Remove technical properties, narrative, self-promotion
- [ ] **"Researchers are interested in..."**: Replace with "We study/propose/derive..."
- [ ] **Passive voice**: Convert to active where possible ("can be identified" → "are identified")
- [ ] **"individuals"**: Change to "units" (unless specifically about people)
- [ ] **"DID"**: Standardize to "DiD"
- [ ] **"control group"**: Change to "comparison group"
- [ ] **Vague hedges** ("perhaps," "somewhat," "potentially"): Replace with specific mechanisms
- [ ] **Long compound sentences**: Break into shorter, single-point sentences
- [ ] **Math in running text**: Move complex equations to displayed math
- [ ] **Abbreviations**: Spell out on first use; prefer full terms in introduction
- [ ] **Contributions**: Are they enumerated explicitly?
- [ ] **Software**: Is open-source implementation mentioned with link?
- [ ] **Running example**: Is there a concrete empirical example threaded through?
- [ ] **Literature section**: Is it a formal subsection, not scattered?
- [ ] **"working model"**: Use when referring to potentially misspecified models
- [ ] **Formal lemmas**: Are key properties elevated from equations to formal statements?
- [ ] **Acknowledgments**: Include seminar/conference venues, RAs, and any AI tools used

---

## 8. Review Workflow

When reviewing a paper in Pedro Sant'Anna's style, follow this sequence:

### Pass 1: Structure
1. Does the paper follow: Hook → Setup → Contributions → Related Lit → Body → Application → Conclusion?
2. Is there a running empirical example?
3. Are contributions enumerated?
4. Is there a formal "Related Literature" subsection?

### Pass 2: Abstract & Introduction
1. Apply the throat-clearing test (first sentence must contain a verb of contribution)
2. Apply the 30-50% compression test on the abstract
3. Check for purpose-centric (not method-centric) framing
4. Verify active voice and direct phrasing

### Pass 3: Terminology
1. Run through the terminology preference table (Section 3.1)
2. Check precision vs. generality (Section 3.2)
3. Check hedging appropriateness (Section 3.4)

### Pass 4: Additions
1. Should falsification tests / testable implications be added?
2. Is software mentioned?
3. Are replication files available?
4. Should heuristic summaries be added after technical results?

### Pass 5: Line Polish
1. Run through the sentence-level checklist (Section 7)
2. Check for redundant qualifiers and parenthetical asides
3. Verify consistent terminology throughout

---

## Appendix: Evidence Base

This skill was derived from comparative analysis of the following papers:

| Paper | ArXiv v1 → Published | Key Revision Insight |
|---|---|---|
| When Is Parallel Trends Sensitive to Functional Form? | 2020 → Econometrica 2023 | 40% abstract compression; added falsification tests |
| Efficient Estimation for Staggered Rollout Designs | 2021 → JPE:Micro 2023 | 50% abstract compression; removed self-promotion |
| What's Trending in DiD? | 2022 → JoE 2023 | Stable abstract; added running Medicaid example |
| Covariate Distribution Balance via Propensity Scores | 2018 → JAE 2022 | Complete reframing from method-centric to purpose-centric |
| Distribution Regression in Duration Analysis | 2019 → EJ 2022 | Monte Carlo moved to appendix; empirical results removed from abstract |
| DiD with Multiple Time Periods | 2018 → JoE 2021 | Most dramatic transformation; unified three-step framework added |
| Role of Parallel Trends in Event Study Settings | 2020 → JAERE 2021 | Virtually no changes — already polished at v1 |
| Doubly Robust DiD Estimators | 2018 → JoE 2020 | Three entirely new contributions added; "working models" terminology |
| Nonparametric Tests for TE Heterogeneity | 2016 → JBES 2021 | Contribution enumeration added; notation D→T clarified |
| Specification Tests for the Propensity Score | 2016 → JoE 2019 | Fundamental reframing (balancing → CDF restriction); hedged power claims |
| DiD with Compositional Changes | 2023 → JoE forthcoming | Already polished at v1; minimal changes |
| Generalized PS Tests | 2020 → JNPS forthcoming | Broadened scope; hedged power claims |
| DiD Practitioner's Guide | 2025 → JEL forthcoming | Already polished at v1; accessible conversational tone |
| DiD with Continuous Treatment | 2021 → AER forthcoming | Most extensively revised; "selection bias" replaces "treatment effect heterogeneity" |
| Selection and Parallel Trends | 2022 → Working paper (v14) | 14 versions over 4 years; theoretical results sharpened to if-and-only-if |
| Program Evaluation with Right-Censored Data | 2016 → Working paper | Early-career style baseline: generic opening, passive tone, math-first |

---

*Generated from analysis of 20 papers spanning 2016-2026, comparing ArXiv v1 drafts with final published versions.*
