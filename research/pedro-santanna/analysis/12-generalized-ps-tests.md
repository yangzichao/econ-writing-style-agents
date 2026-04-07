# Writing Style Analysis: Specification Tests for Generalised Propensity Scores Using Double Projections

## Paper Info
- Authors: ArXiv v1: Pedro H. C. Sant'Anna, Xiaojun Song; Published: Juan Carlos Escanciano, Pedro H. C. Sant'Anna, Xiaojun Song
- ArXiv v1 date: March 30, 2020 (arXiv:2003.13803v1)
- Published: Journal of Nonparametric Statistics, 2025 (DOI: 10.1080/10485252.2025.2551752)

## Abstract Comparison
### v1 Abstract
"This paper proposes a new class of nonparametric tests for the correct specification of generalized propensity score models. The test procedure is based on two different projection arguments, which lead to test statistics with several appealing properties. They accommodate high-dimensional covariates; are asymptotically invariant to the estimation method used to estimate the nuisance parameters and do not requite estimators to be root-n asymptotically linear; are fully data-driven and do not require tuning parameters, can be written in closed-form, facilitating the implementation of an easy-to-use multiplier bootstrap procedure. We show that our proposed tests are able to detect a broad class of local alternatives converging to the null at the parametric rate. Monte Carlo simulation studies indicate that our double projected tests have much higher power than other tests available in the literature, highlighting their practical appeal."

### Final Abstract
"This paper proposes a new class of nonparametric tests for the correct specification of models based on conditional moment restrictions, paying particular attention to generalised propensity score models. The test procedure is based on two different projection arguments, leading to test statistics that are suitable for setups with many covariates and are (asymptotically) invariant to the estimation method used to estimate the nuisance parameters. We show that our proposed test is able to detect a broad class of local alternatives converging to the null at the usual parametric rate, and illustrate its attractive power properties through simulations."

### Changes Analysis
The abstract was significantly condensed and broadened:

1. **Scope broadened**: "tests for the correct specification of generalized propensity score models" becomes "tests for the correct specification of models based on conditional moment restrictions, paying particular attention to generalised propensity score models." The published version positions the contribution as more general -- applicable to any conditional moment restriction model, not just propensity scores.

2. **Significant condensation**: The v1 abstract lists properties in a detailed, semicolon-separated list. The published version collapses these into a shorter, more digestible summary. Several specific claims are removed: "do not require estimators to be root-n asymptotically linear", "can be written in closed-form", "facilitating the implementation of an easy-to-use multiplier bootstrap procedure."

3. **Hedged power claim**: v1 says "much higher power than other tests available in the literature"; published says "illustrate its attractive power properties through simulations" -- a substantially more cautious claim.

4. **Spelling**: "requite" (typo in v1) is fixed. "Generalized" (American) becomes "generalised" (British), following the journal's house style.

5. **Addition of coauthor**: Juan Carlos Escanciano is added as first author in the published version. The paper "supersedes and expands on Escanciano (2009b)" as noted in the published introduction.

## Introduction Comparison
### Key Changes
The introduction underwent substantial revision:

1. **Broadened scope with Remark**: The published version includes Remark 2.1 noting that the methodology "applies to any other conditional moment restriction problem" including tests for parametric conditional mean models, joint tests for conditional mean and variance models, etc. This broadens the paper's appeal significantly.

2. **Added coauthor's prior work**: The published version notes "This paper, which supersedes and expands on Escanciano (2009b), is the first to combine the two aforementioned projections." This acknowledges the intellectual lineage more explicitly.

3. **Extended to index models**: The published version discusses extensions to single-index and multiple-index models (Section 5), including directional tests. This is a substantial addition not present in v1.

4. **Removed empirical application from main text**: v1 mentions "an empirical illustration in Section 6"; the published version moves the empirical application to an "online supplementary appendix."

5. **Shortened introductory paragraphs**: The v1 introduction has extensive background on propensity scores and causal inference. The published version condenses this significantly, assuming more reader familiarity.

6. **More precise positioning relative to existing tests**: The published version adds a detailed comparison paragraph noting that Escanciano (2006a)'s test "is not robust to the estimation of nuisance parameters" and that Escanciano and Goh (2014) "is not robust to the presence of many covariates," while Sant'Anna and Song (2019) "only tests for an implication of the null hypothesis, not for the null hypothesis itself."

7. **British spelling throughout**: "generalised", "characterised", "randomised", "organised" -- conforming to the journal's British English house style.

## Conclusion/Discussion Comparison
### Key Changes
The v1 has a brief Section 7 "Concludes." The published version similarly has a concise Section 7. Both are short, summarizing the paper's contributions. The published version incorporates the new extensions to index models in its summary.

## Writing Style Patterns Observed
- **Sentence Structure**: The published version shows significantly more economical sentence construction. Long lists of properties are condensed into shorter characterizations. The prose moves from "listing features" to "describing the approach."
- **Vocabulary/Terminology**: The shift from "generalized" to "generalised" reflects journal house style (British English). The broadening from "generalized propensity score" to "conditional moment restrictions" reflects a more ambitious framing.
- **Framing/Motivation**: The v1 frames the paper entirely through the lens of causal inference and propensity scores. The published version frames it as a general specification testing methodology that happens to have an important application to propensity scores. This broader framing is likely influenced by the journal venue (Journal of Nonparametric Statistics rather than an econometrics journal).
- **Precision**: The published version is more precise about what existing tests can and cannot do, providing a clearer gap analysis. Claims about power are more carefully qualified.
- **Tone**: The published version is more measured and academic. v1's "much higher power" becomes "attractive power properties" -- a substantial toning down.
- **Conciseness**: The published abstract is roughly half the length of v1's. Throughout, the paper shows significant trimming of background material.
- **Reader Engagement**: The published version's broader framing makes it relevant to a wider statistical audience beyond causal inference specialists.

## Specific Revision Examples

1. **Before (v1):** "They accommodate high-dimensional covariates; are asymptotically invariant to the estimation method used to estimate the nuisance parameters and do not requite estimators to be root-n asymptotically linear; are fully data-driven and do not require tuning parameters, can be written in closed-form, facilitating the implementation of an easy-to-use multiplier bootstrap procedure."
   **After (published):** "leading to test statistics that are suitable for setups with many covariates and are (asymptotically) invariant to the estimation method used to estimate the nuisance parameters."
   **Why:** The v1's exhaustive property list was condensed to two key selling points. The detailed technical properties (closed-form, root-n asymptotic linearity not needed) are moved to the body of the paper. This reflects a shift from a "features list" style abstract to a more narrative one.

2. **Before (v1):** "Monte Carlo simulation studies indicate that our double projected tests have much higher power than other tests available in the literature, highlighting their practical appeal."
   **After (published):** "and illustrate its attractive power properties through simulations."
   **Why:** The comparative claim "much higher power than other tests" is replaced with the non-comparative "attractive power properties." This is a significant hedging, likely reflecting reviewer feedback about the scope of the power comparisons.

3. **Before (v1):** "This paper proposes a new class of nonparametric tests for the correct specification of generalized propensity score models."
   **After (published):** "This paper proposes a new class of nonparametric tests for the correct specification of models based on conditional moment restrictions, paying particular attention to generalised propensity score models."
   **Why:** Broadening the scope from a specific application (GPS) to the general methodology (conditional moment restrictions) makes the paper more broadly applicable and positions it as a methodological contribution rather than a purely applied one.

4. **Before (v1):** "To the best of our knowledge, no other (specification) test available in the literature enjoys all these attractive properties (e.g., Escanciano, 2006, Mora and Moro-Egido, 2008, Shaikh et al., 2009, Escanciano and Goh, 2014, Garcia-Portugues et al., 2014, Zhu et al., 2017, Sant'Anna and Song, 2019, and Kim et al., 2020)."
   **After (published):** "To the best of our knowledge, prior to this paper, no other (specification) test available in the literature enjoys all these attractive properties, see Gonzalez-Manteiga and Crujeiras (2013) for a review of existing methodologies."
   **Why:** The long list of individual citations is replaced with a single review reference, which is cleaner and avoids the impression of criticizing specific papers. Adding "prior to this paper" also makes the priority claim more precise.

5. **Before (v1):** [Two authors: Sant'Anna and Song]
   **After (published):** [Three authors: Escanciano, Sant'Anna, and Song]
   **Why:** The addition of Juan Carlos Escanciano as first author reflects the paper's acknowledgment that it "supersedes and expands on Escanciano (2009b)." This is a significant change in authorship that also shifts the paper's intellectual emphasis toward the specification testing methodology (Escanciano's specialty) and away from the causal inference application.
