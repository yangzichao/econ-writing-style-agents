# Abstract Rules

These rules encode Jonathan Roth's revision patterns for economics paper abstracts, derived from comparing first drafts to published versions across 7+ papers.

## Rule 1: Open with Common Practice, Then Pivot to Contribution

The first sentence should describe a specific empirical practice that applied researchers commonly use. The second sentence pivots to the paper's contribution. The practice must be SPECIFIC to the subfield, not a generic statement about social science.

**Good:**
- "When studying an outcome Y that is weakly-positive but can equal zero (e.g. earnings), researchers frequently estimate an ATE for a 'log-like' transformation..."
- "This paper discusses two important limitations of the common practice of testing for preexisting differences in trends..."
- "Design-based frameworks of uncertainty are frequently used in settings where the treatment is (conditionally) randomly assigned"

**Bad:**
- "Social scientists are often interested in estimating causal effects in settings where all units in the population are observed" — too generic, does not identify a specific practice
- "Causal inference is a central goal of empirical economics" — vacuous throat-clearing
- "An important question in applied work is..." — no specificity

**Check:** Does the opening sentence name a concrete methodological practice (e.g., "testing for pre-trends," "estimating log-like transformations," "using event-study plots")? If it only names a broad goal ("estimating causal effects," "understanding treatment effects"), flag it for revision.

### Before / After Examples

**Staggered Rollout (ArXiv v1 → JPE:Micro 2023)**

> BAD: "Researchers are often interested in the causal effect of treatments that are rolled out to different units at different points in time. This paper studies how to efficiently estimate a variety of causal parameters in such staggered rollout designs when treatment timing is (as-if) randomly assigned."
>
> GOOD: "We study estimation of causal effects in staggered rollout designs, i.e. settings where there is staggered treatment adoption and the timing of treatment is as-good-as randomly assigned."

Two setup sentences collapsed into one. The "researchers are interested" opener is removed.

**Design-Based Uncertainty (ArXiv v1 → JASA 2025)**

> BAD: "Social scientists are often interested in estimating causal effects in settings where all units in the population are observed (e.g. all 50 US states). Design-based approaches, which view the treatment as the random object of interest, may be more appealing than standard sampling-based approaches in such contexts."
>
> GOOD: "Design-based frameworks of uncertainty are frequently used in settings where the treatment is (conditionally) randomly assigned. This paper develops a design-based framework suitable for analyzing quasi-experimental settings in the social sciences, in which the treatment assignment can be viewed as the realization of some stochastic process but there is concern about unobserved selection into treatment."

The v1 opens with a generic interest statement about social scientists; v8 opens with specific field context about design-based frameworks.

**Inference for Moment Inequalities (ArXiv v1 → REStud 2023)**

> BAD: "We consider inference based on linear conditional moment inequalities, which arise in a wide variety of economic applications, including many structural models."
>
> GOOD: "We show that moment inequalities in a wide variety of economic applications have a particular linear conditional structure."

"We consider" (exploratory) → "We show" (definitive). The v1 describes an activity; the published version states a finding.

## Rule 2: Name Impossibility Results Memorably

When a paper proves a negative or impossibility result, give it a memorable label in the abstract. This makes the contribution stick.

**Good:**
- "We further establish a trilemma: when the outcome can equal zero, there is no treatment effect parameter that is (i) an average of individual-level effects, (ii) unit-invariant, and (iii) point-identified"
- "First, conventional pre-trends tests may have low power. Second, conditioning the analysis on the result of a pretest can distort estimation and inference" — numbered limitations

**Check:** If the paper proves that something is impossible, unavoidable, or limited, does the abstract give that result a name or structured enumeration? Unnamed negative results are forgettable. Suggest naming them (e.g., "trilemma," "impossibility," or at minimum a numbered list of the specific properties that cannot coexist).

## Rule 3: Remove Mathematical Notation and Technical Detail

Published abstracts remove all mathematical notation, step-by-step methodology descriptions, and specific estimator names that appeared in early drafts. The abstract should be readable by any applied economist without consulting the paper.

**Revise if you find:**
- Mathematical notation (e.g., "theta_g = E[g(Y(1),Y(0))]")
- Named estimators or specific test statistics (move to the introduction)
- Step-by-step descriptions of the methodology
- References to specific assumptions by name (e.g., "under Assumption 3.2")

**Good (published):** "We discuss several alternative approaches"
**Bad (v1):** "We propose an estimator theta-hat based on the GMM criterion function with moments..."

**Check:** Does the abstract contain any math symbols, subscripts, or technical estimator names? If so, flag them for removal. The abstract should describe what the paper does and finds, not how.

### Before / After Examples

**Logs with Zeros (ArXiv v1 → QJE 2024)**

> BAD: "Moreover, we show that any parameter of the form θ_g = E[g(Y(1),Y(0))] is necessarily scale dependent if it is point-identified and defined with zero-valued outcomes."
>
> GOOD: "We further establish a trilemma: when the outcome can equal zero, there is no treatment effect parameter that is an average of individual-level treatment effects, unit-invariant, and point-identified."

Math notation (θ_g = E[g(Y(1),Y(0))]) removed entirely. The impossibility result is restated in words and given the name "trilemma."

## Rule 4: End with Practical Alternatives or Recommendations

Roth abstracts close with a "menu of options" or "practical recommendations," especially when the paper contains a negative result. This transforms the paper from a critique into constructive guidance.

**Good:**
- "We discuss several alternative approaches...including (i) expressing the ATE in levels as a percentage (e.g. using Poisson regression), (ii) explicitly calibrating the value placed on intensive and extensive margins, and (iii) estimating separate effects for the two margins"
- "I conclude with practical recommendations for mitigating these issues"
- "These results can be used to conduct sensitivity analyses"

**Check:** Does the abstract end with a forward-looking statement about what practitioners should do? If the paper identifies a problem but the abstract does not mention solutions, alternatives, or recommendations, flag this gap.

## Rule 5: Cut Self-Promotion

Remove superlative claims and self-congratulatory language. Let the results speak.

**Bad (v1):** "our application provides the most precise estimates to date"
**Good (published):** statement removed entirely, or replaced with a factual summary of the application

**Check:** Flag any phrase containing "first to," "most precise," "novel," "important contribution," or similar self-promotion. Replace with factual descriptions of what the paper does.

### Before / After Examples

**Staggered Rollout (ArXiv v1 → JPE:Micro 2023)**

> BAD: "As an empirical contribution of independent interest, our application provides the most precise estimates to date on the effectiveness of procedural justice training programs for police officers."
>
> GOOD: "In an application to a training program for police officers, confidence intervals for the proposed estimator are as much as eight times shorter than for existing approaches."

Self-promotion ("of independent interest," "most precise estimates to date") replaced with a factual comparison.

## Rule 6: Add Empirical Scope When Revising

Published abstracts mention concrete empirical applications that may be absent from early drafts. This signals practical relevance.

**Good:**
- "We illustrate these approaches in three empirical applications"
- "We illustrate our methodology in two empirical applications"

**Check:** If the paper contains empirical applications, does the abstract mention them (even briefly)? A one-sentence mention near the end is sufficient. Do not describe the applications in detail — just signal that they exist.

## Compression Target

Roth's abstracts compress substantially from v1 to published (one paper went from 170 to 90 words, a 47% reduction). The primary compression comes from removing narrative scaffolding, mathematical notation, and exploratory language. If the abstract exceeds 150 words, look for material to cut.
