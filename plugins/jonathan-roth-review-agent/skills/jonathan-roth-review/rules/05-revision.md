# Revision Patterns

## What to Cut

### 1. Generic throat-clearing openers
Remove "Social scientists are often interested in..." and "Researchers are often interested in..." openers.
Evidence: Design-Based v1->v8 (cut), Staggered v1->published (cut).

### 2. Mathematical notation from abstract
Remove formulas like theta_g = E[g(Y(1),Y(0))] from the abstract. State results in words.
Evidence: Logs v1->v7 (removed all math from abstract).

### 3. Step-by-step methodology in abstract
Don't narrate your logical process. State results directly.
Evidence: Pre-test v1 walks through valid/invalid cases -> published gives two-bullet summary.
Evidence: Staggered v1 "The efficient estimator is not feasible in practice because it requires knowledge of the optimal weights. However, the optimal weights can be estimated..." -> published: "A feasible plug-in version of the efficient estimator is asymptotically unbiased..."

### 4. Self-promotional language
Remove "of independent interest," "most precise estimates to date."
Evidence: Staggered v1->published (removed self-promotion).

### 5. Redundant literature engagement in main text
Move detailed corrections of prior literature to remarks or footnotes.
Evidence: Parallel Trends FF v1 Remark 10 quoting and correcting Kahn-Lang and Lang (2018) -> removed in published.

### 6. Multiple empirical applications (consolidate)
Prefer one focused application over many.
Evidence: Covariate Balance in Sant'Anna papers: 3->1 applications. Roth's co-authored papers follow same pattern.

## What to Add

### 1. Named impossibility results
Transform negative results into memorable named concepts.
Evidence: Logs added "trilemma" in later versions.

### 2. Menu of alternatives
After impossibility results, enumerate constructive alternatives as (i), (ii), (iii).
Evidence: Logs v7, Parallel Trends FF published.

### 3. Quantified empirical surveys
Add surveys of existing practice to motivate the paper.
Evidence: Pre-test added "70 papers" survey, What's Trending added "30% of NBER papers."

### 4. Practical recommendations section
Add a dedicated section for applied researchers.
Evidence: Pre-test Section III, What's Trending boxed recommendations.

### 5. Software packages
Add named R/Stata packages with GitHub links.
Evidence: HonestDiD, pretrends, staggered all added in published versions.

### 6. Falsification tests / testable implications
Transform theoretical results into actionable diagnostics.
Evidence: Parallel Trends FF added full falsification tests subsection.

### 7. Sensitivity analysis
Frame robustness as formal sensitivity analysis.
Evidence: Design-Based v8 adds "sensitivity analyses" framing absent from v1.

## What to Expand

### 1. Concrete examples
Thread real-world examples through the paper.
Evidence: What's Trending added Medicaid running example. Pre-test calibrates to real papers.

### 2. Title revision
Consider whether the title can be more memorable, catchy, or question-based.
Evidence: "Should We Condition on the Test for Pre-trends in Difference-in-Difference Designs?" -> "Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends"

### 3. Scope reframing
Consider whether the paper's contribution should be reframed from descriptive to constructive.
Evidence: Design-Based v1 (descriptive, SDIM focus) -> v8 (sensitivity analysis focus, "rich forms of selection").

## Title Evolution Patterns
Roth's title changes are among the most dramatic in the corpus:
- Question -> Directive: "Should We Condition..." -> "Pretest with Caution"
- The published title is shorter, catchier, and actionable
- Question titles work well for framing papers ("Logs with zeros?", "When Is Parallel Trends Sensitive?")
