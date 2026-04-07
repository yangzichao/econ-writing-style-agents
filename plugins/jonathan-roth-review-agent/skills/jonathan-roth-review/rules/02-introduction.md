# Introduction Rules

These rules encode Jonathan Roth's revision patterns for economics paper introductions, derived from comparing first drafts to published versions across his papers.

## Rule 1: Open by Identifying a Common Empirical Practice

The first paragraph should describe what applied researchers commonly do, grounding the paper in real practice. This is not a generic statement about the importance of causal inference — it is a specific description of a methodological practice with enough detail that a reader recognizes it from their own work.

**Good:**
- "When using difference-in-differences and related methods, researchers often test for pretreatment differences in trends ('pre-trends') as a way of assessing the plausibility of the parallel trends assumption."
- Opens with the canonical DiD setup that practitioners use daily
- Opens with the common practice of using log-like transformations for outcomes with zeros

**Bad:**
- "Causal inference is central to modern economics..."
- "An important goal of empirical research is..."
- "Social scientists are often interested in estimating causal effects..."

**Check:** Does the first paragraph describe a specific method, test, or transformation that applied researchers routinely use? If it describes a broad goal instead of a practice, flag it.

### Before / After Examples

**Pre-test with Caution (AER: Insights 2022)**

> "When using difference-in-differences and related methods, researchers often test for pretreatment differences in trends ('pre-trends') as a way of assessing the plausibility of the parallel trends assumption. These tests are remarkably common: my review of publications in three leading economics journals between 2014 and 2018 found 70 papers that use an 'event-study plot' to visually test for pre-trends."

This opening identifies a specific practice (testing for pre-trends), names it concretely, and immediately quantifies its prevalence.

## Rule 2: Reveal the Hidden Assumption or Limitation

After describing common practice, the introduction must expose what is wrong, hidden, or under-appreciated about that practice. This is the paper's reason for existing.

**Good:**
- "This paper highlights two limitations with the practice of pretesting for pre-trends"
- Shows that log-like transformations are unit-dependent
- Reveals that quasi-experimental uncertainty requires different foundations than sampling-based uncertainty
- Shows that parallel trends validity depends on functional form

**Check:** Is there a clear sentence (typically in the first or second paragraph) that says "this paper highlights/shows/establishes that [common practice] has [specific limitation]"? If not, the reader will not understand why the paper matters.

### Before / After Examples

**Pre-test with Caution (AER: Insights 2022)**

> "This paper highlights two limitations with the practice of pretesting for pre-trends. First, conventional pretests may have low power, meaning that preexisting trends that produce meaningful bias in the treatment effects estimates may not be detected with substantial probability. Second, conditioning the analysis on the result of a pre-trends test induces distortions to estimation and inference from pretesting."

The hidden limitations are enumerated clearly: "First... Second..."

## Rule 3: Quantify the Problem with Empirical Surveys

Where possible, survey existing empirical practice to demonstrate the problem's prevalence. This grounds the methodological contribution in real-world relevance and makes the problem feel urgent.

**Good:**
- "my review of publications in three leading economics journals between 2014 and 2018 found 70 papers that use an 'event-study plot' to visually test for pre-trends"
- "over 30% of 2024 NBER applied microeconomics working papers mention DiD or ES"

**Check:** Does the introduction include any quantitative evidence about how widespread the practice (or the problem) is? A literature survey, count of papers, or similar empirical grounding strengthens the motivation substantially. If absent, suggest adding one.

## Rule 4: Provide Concrete Examples Early

Ground abstract notation in a real application within the first page. The reader should be able to picture the problem concretely before encountering any formalism.

**Good:**
- Medicaid expansion example threaded from the first page of the introduction
- Calibrating simulations to the specifications in actual published papers
- Using earnings as the running example for outcomes with zeros

**Check:** Does the introduction mention at least one concrete empirical setting (by name, not generically) within the first two pages? If the reader encounters formal notation before seeing a concrete example, flag this and suggest reordering.

## Rule 5: Present a Menu of Alternatives After Impossibility Results

When the paper proves something is impossible or limited, the introduction must immediately offer constructive alternatives. Do not leave the reader with only a negative result. Use numbered lists (i), (ii), (iii) for clarity.

**Good:**
- "We discuss several alternative approaches...including (i) expressing the ATE in levels as a percentage (e.g. using Poisson regression), (ii) explicitly calibrating the value placed on intensive and extensive margins, and (iii) estimating separate effects for the two margins"
- "researchers who wish to point-identify the ATT should justify one of the following: (i)...(ii)...(iii)..."

**Check:** If the paper contains a negative or impossibility result, does the introduction also preview the constructive alternatives? If it only describes the problem, flag this as incomplete framing.

### Before / After Examples

**Parallel Trends Functional Form (Econometrica 2023)**

> "Our results suggest that researchers who wish to point-identify the ATT should justify one of the following: (i) why treatment is randomly assigned, (ii) why the chosen functional form is correct at the exclusion of others, or (iii) a method for inferring the entire counterfactual distribution of untreated potential outcomes."

A three-option menu after an impossibility result. Uses (i)/(ii)/(iii) numbering.

## Rule 6: Enumerate Contributions Clearly

List the paper's contributions, but use natural language rather than formulaic phrases. Roth tends to use "This paper highlights/develops/establishes" rather than "We contribute in different fronts" or "Our contributions are threefold."

**Good:**
- "This paper highlights two limitations" then "First...Second..."
- "We develop tests... We also provide tools for... we derive sharp lower bounds..."

**Bad:**
- "We contribute to three strands of literature..."
- "Our paper makes the following contributions: (1)..."
- "This paper is the first to..."

**Check:** Are the contributions clearly enumerable from the introduction? The reader should be able to list what the paper does after reading the introduction. But the enumeration should feel organic, not like a grant proposal.

### Before / After Examples

**Testing Mechanisms (ArXiv v1 → REStud forthcoming)**

> v1: "Economists are often interested in the mechanisms by which a particular treatment affects an outcome. This paper develops tests for the 'sharp null of full mediation'..."
>
> Published: "Economists are often interested in the mechanisms by which a treatment affects an outcome. We develop tests for the 'sharp null of full mediation'..."

Subtle but characteristic: "This paper develops" → "We develop" (more direct, active).

## Rule 7: Include a Formal Related Literature Subsection

All published Roth papers include a dedicated "Related Literature" subsection within the introduction (typically at the end of the introduction section). Use em dash formatting: "Related Literature.---"

**Check:** Is there a clearly delineated related literature discussion? If the literature review is scattered throughout the introduction without a dedicated subsection, suggest consolidating it.

## Rule 8: Announce Software in the Introduction

If the paper provides computational tools, announce them in the introduction with specific package names and languages.

**Good:**
- "provide software for their implementation" + named R package (pretrends) + Stata package
- HonestDiD R and Stata packages announced in the introduction
- staggered R and Stata packages announced in the introduction

**Check:** If the paper develops new methods, does the introduction mention whether software is available? If software exists but is not mentioned in the introduction, flag this — practitioners need to know tools exist before they will read the theory.

## Rule 9: Use First-Person Appropriately

Use "I" for solo-authored work and "we" for co-authored work. Roth does not use the "royal we" in solo papers — he writes "I show" and "my review." This is distinctive and should be preserved.

**Check:** Is the pronoun usage consistent with the number of authors? Flag "we" in solo-authored papers and "I" in co-authored papers. The passive voice ("it is shown that...") should also be flagged as unnecessarily evasive.
