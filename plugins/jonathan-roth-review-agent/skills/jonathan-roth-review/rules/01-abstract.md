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

## Rule 6: Add Empirical Scope When Revising

Published abstracts mention concrete empirical applications that may be absent from early drafts. This signals practical relevance.

**Good:**
- "We illustrate these approaches in three empirical applications"
- "We illustrate our methodology in two empirical applications"

**Check:** If the paper contains empirical applications, does the abstract mention them (even briefly)? A one-sentence mention near the end is sufficient. Do not describe the applications in detail — just signal that they exist.

## Compression Target

Roth's abstracts compress substantially from v1 to published (one paper went from 170 to 90 words, a 47% reduction). The primary compression comes from removing narrative scaffolding, mathematical notation, and exploratory language. If the abstract exceeds 150 words, look for material to cut.
