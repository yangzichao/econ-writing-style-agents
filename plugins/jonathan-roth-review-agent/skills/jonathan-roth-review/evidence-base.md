# Evidence Base

Paper-by-paper summary of evidence supporting each rule.

## Paper Index
| # | Short Title | ArXiv | Versions | Published | Journal | Revision Magnitude |
|---|---|---|---|---|---|---|
| 01 | Logs with Zeros | 2212.06080 | 7 | Nov 2023 | QJE 2024 | Major |
| 02 | Pre-test with Caution | 1804.01208 | 2 + title change | 2022 | AER: Insights | Transformative |
| 03 | Honest Parallel Trends | -- | Multiple drafts | 2023 | REStud | Major |
| 04 | Testing Mechanisms | 2404.11739 | 3 | Forthcoming | REStud | Moderate |
| 05 | Design-Based Uncertainty | 2008.00602 | 8 | Forthcoming | JASA | Major |
| 06 | Moment Inequalities | 1909.10062 | 5 | 2023 | REStud | Major |
| 07 | Staggered Rollout | 2102.01291 | -- | 2023 | JPE:Micro | Major (co-authored with Sant'Anna) |
| 08 | Parallel Trends FF | 2010.04814 | -- | 2023 | Econometrica | Major (co-authored with Sant'Anna) |
| 09 | What's Trending | 2201.01194 | -- | 2023 | JoE | Minor (co-authored with Sant'Anna) |
| 10 | Interpreting Event-Studies | 2401.12309 | 2 | 2026 | JER | Minor |

## Key Revision Insights by Paper

### 01 -- Logs with Zeros (MOST DISTINCTIVE ROTH PAPER)
- **Title**: Question format "Logs with zeros?" is catchy and immediately frames the problem
- **Abstract**: v1 includes math notation (theta_g), technical detail -> v7 restructured around "trilemma" concept
- **Key addition**: Named impossibility result "trilemma" -- three desirable properties that can't all hold
- **Menu of alternatives**: (i) Poisson regression, (ii) calibrate margins, (iii) Lee bounds
- **7 versions** over 11 months -- extensive polish
- **Rules sourced**: Named impossibility (04-framing S2), menu of alternatives (04-framing S3), abstract compression (01-abstract S3)

#### Abstract Comparison
**v1 (Dec 2022):** "Researchers frequently estimate the average treatment effect (ATE) in logs, which has the desirable property that its units approximate percentages. When the outcome takes on zero values, researchers often use alternative transformations (e.g., log(1+Y), arcsinh(Y))... Moreover, we show that any parameter of the form θ_g = E[g(Y(1),Y(0))] is necessarily scale dependent if it is point-identified and defined with zero-valued outcomes. We conclude by outlining a variety of options available to empirical researchers..."

**v7 (Nov 2023):** "When studying an outcome Y that is weakly-positive but can equal zero (e.g. earnings), researchers frequently estimate an average treatment effect (ATE) for a 'log-like' transformation... We further establish a trilemma: when the outcome can equal zero, there is no treatment effect parameter that is an average of individual-level treatment effects, unit-invariant, and point-identified. We discuss several alternative approaches... We illustrate these approaches in three empirical applications."

**Key changes:** Math notation (θ_g) removed. "Trilemma" concept introduced. "Outlining a variety of options" → structured discussion with empirical illustrations.

### 02 -- Pre-test with Caution (MOST DRAMATIC TRANSFORMATION)
- **Title change**: "Should We Condition on the Test for Pre-trends in Difference-in-Difference Designs?" -> "Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends"
- **Abstract**: Completely rewritten. v1 is technical (walks through valid/invalid DiD cases, monotone trends). Published is high-level problem framing ("two important limitations...First...Second...")
- **Quantified survey**: "70 papers" in leading journals
- **Practical recommendations**: Dedicated Section III
- **Software**: pretrends R and Stata packages
- **Solo author**: Uses "I" throughout -- distinctive
- **Rules sourced**: Title evolution (05-revision S-Title), problem-first framing (04-framing S1), quantified surveys (04-framing S5)

#### Abstract Comparison
**v1 title:** "Should We Adjust for the Test for Pre-trends in Difference-in-Difference Designs?"

**v1 (Apr 2018):** "The common practice in difference-in-difference (DiD) designs is to check for parallel trends prior to treatment assignment, yet typical estimation and inference does not account for the fact that this test has occurred. I analyze the properties of the traditional DiD estimator conditional on having passed (i.e. not rejected) the test for parallel pre-trends... Moreover, if the trend is monotone, then under reasonable assumptions the bias from conditioning exacerbates the bias relative to the true treatment effect. I propose new estimation and inference procedures that account for the test for parallel trends..."

**Published title:** "Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends"

**Published (AER:I 2022):** "This paper discusses two important limitations of the common practice of testing for preexisting differences in trends ('pre-trends') when using difference-in-differences and related methods. First, conventional pre-trends tests may have low power. Second, conditioning the analysis on the result of a pretest can distort estimation and inference, potentially exacerbating the bias of point estimates and under-coverage of confidence intervals. I analyze these issues both in theory and in simulations calibrated to a survey of recent papers in leading economics journals, which suggest that these limitations are important in practice. I conclude with practical recommendations for mitigating these issues."

**Key changes:** Title completely rewritten (question → directive). Abstract restructured from technical walkthrough to high-level "two limitations" framing. Added "practical recommendations" closing. Added "calibrated to a survey of recent papers" (quantified motivation). Massive simplification.

### 03 -- A More Credible Approach to Parallel Trends
- **No ArXiv** but multiple draft versions exist
- **Flagship paper**: Defines the sensitivity analysis approach to parallel trends
- **Software**: HonestDiD R and Stata packages
- **"Credible" in title**: The word "credible" is a Roth signature
- **Rules sourced**: Sensitivity framing (04-framing S4), software (02-introduction S8)

### 04 -- Testing Mechanisms
- **Abstract**: v1 long and explanatory -> v3 compressed with "exploits connections" phrasing
- **Named concept**: "sharp null of full mediation"
- **Advantage framing**: "An advantage of our approach relative to existing tools... is that it does not require stringent assumptions"
- **Rules sourced**: Abstract compression (01-abstract S3), named results (04-framing S2)

#### Abstract Comparison
**v1 (Apr 2024):** "Economists are often interested in the mechanisms by which a particular treatment affects an outcome. This paper develops tests for the 'sharp null of full mediation'... A key observation is that if D is randomly assigned and has a monotone effect on M, then D is a valid instrumental variable for the local average treatment effect (LATE) of M on Y. Existing tools for testing the validity of the LATE assumptions can thus be used to test the sharp null of full mediation when M and D are binary..."

**v3 (Feb 2026):** "Economists are often interested in the mechanisms by which a treatment affects an outcome. We develop tests for the 'sharp null of full mediation'... Our approach exploits connections between mediation analysis and the econometric literature on testing instrument validity. We also provide tools for quantifying the magnitude of alternative mechanisms when the sharp null is rejected... An advantage of our approach relative to existing tools for mediation analysis is that it does not require stringent assumptions about how M is assigned. We illustrate our methodology in two empirical applications."

**Key changes:** "This paper develops" → "We develop." Technical LATE explanation compressed to "exploits connections." Added "always-takers" terminology with sharp bounds. Added "two empirical applications."

### 05 -- Design-Based Uncertainty (8 VERSIONS, 5 YEARS)
- **Abstract**: v1 "Social scientists are often interested in" -> v8 "Design-based frameworks of uncertainty are frequently used" (specific field context)
- **Reframing**: v1 descriptive (SDIM, DiD, 2SLS properties) -> v8 constructive (sensitivity analysis, "rich forms of selection")
- **Practitioner bridge**: v8 adds "more closely aligns with the way empirical researchers discuss the variation in the data"
- **Rules sourced**: Throat-clearing removal (01-abstract S1), sensitivity framing (04-framing S4)

#### Abstract Comparison
**v1 (Aug 2020):** "Social scientists are often interested in estimating causal effects in settings where all units in the population are observed (e.g. all 50 US states). Design-based approaches, which view the treatment as the random object of interest, may be more appealing than standard sampling-based approaches in such contexts. This paper develops a design-based theory of uncertainty suitable for quasi-experimental settings... We first study the properties of the simple difference-in-means (SDIM) estimator..."

**v8 (Jun 2025):** "Design-based frameworks of uncertainty are frequently used in settings where the treatment is (conditionally) randomly assigned. This paper develops a design-based framework suitable for analyzing quasi-experimental settings in the social sciences, in which the treatment assignment can be viewed as the realization of some stochastic process but there is concern about unobserved selection into treatment... We provide conditions under which the estimands of popular quasi-experimental estimators correspond to interpretable finite-population causal parameters. We characterize the biases and distortions to inference that arise when these conditions are violated. These results can be used to conduct sensitivity analyses when there are concerns about selection into treatment. Taken together, our results establish a rigorous foundation for quasi-experimental analyses that more closely aligns with the way empirical researchers discuss the variation in the data."

**Key changes:** "Social scientists are often interested in" → "Design-based frameworks of uncertainty are frequently used" (specific field context). Reframed from SDIM-centric to sensitivity analysis. Added "Taken together" synthesis and practitioner bridge ("more closely aligns with the way empirical researchers discuss the variation in the data").

### 06 -- Inference for Linear Conditional Moment Inequalities
- **Abstract**: v1 "We consider inference based on" -> v5 "We show that moment inequalities in a wide variety of economic applications have a particular linear conditional structure"
- **Reframing**: From "we consider" (exploratory) to "we show" (definitive)
- **Software**: LinearMomentInequalities Matlab package
- **Rules sourced**: Voice confidence (03-terminology S-Active Voice)

#### Abstract Comparison
**v1 (Sep 2019):** "We consider inference based on linear conditional moment inequalities, which arise in a wide variety of economic applications, including many structural models. We show that linear conditional structure greatly simplifies confidence set construction..."

**v5 (Dec 2022):** "We show that moment inequalities in a wide variety of economic applications have a particular linear conditional structure. We use this structure to construct uniformly valid confidence sets that remain computationally tractable even in settings with nuisance parameters..."

**Key changes:** "We consider inference based on" → "We show that" (exploratory → definitive). Leads with the finding, not the activity.

### 07 -- Staggered Rollout (with Sant'Anna)
- **Abstract**: 170->90 words (47% reduction). "Researchers are often interested in" -> "We study"
- **Self-promotion removed**: "most precise estimates to date" cut
- **Terminology**: "(as-if) randomly assigned" -> "as-good-as randomly assigned"
- **Software**: staggered R and Stata packages
- **Note**: Roth is first author. Patterns overlap with Sant'Anna's rules but compression rate matches Roth's other papers.
- **Rules sourced**: Throat-clearing (01-abstract S1), self-promotion (01-abstract S5), terminology (03-terminology)

### 08 -- Parallel Trends Functional Form (with Sant'Anna)
- **Abstract**: 170->100 words (41% reduction). "monotonic" -> "strictly monotonic"
- **Three-option menu**: Maintained from v1 to published
- **Falsification tests**: Major addition in published version
- **Note**: Roth is first author. The "menu of options" framing is distinctively Roth.
- **Rules sourced**: Menu of alternatives (04-framing S3), falsification tests (05-revision S-Add 6)

### 09 -- What's Trending in DiD (with Sant'Anna, Bilinski, Poe)
- **Abstract**: Virtually identical v1 to published (rare)
- **Major additions**: Medicaid running example, triple differences section
- **Survey format**: Taxonomic organization (canonical model + relaxations)
- **Boxed recommendations**: Throughout each section
- **Quantified motivation**: "over 30% of NBER papers"
- **Rules sourced**: Running example (02-introduction S4), quantified surveys (04-framing S5)

### 10 -- Interpreting Event-Studies
- **Solo author**: Uses implied "I" / third person
- **Practical focus**: Provides guidance for interpreting event-study plots from new DiD methods
- **Short paper**: 2 versions, minor changes
- **Rules sourced**: Practical recommendations (04-framing S6)
