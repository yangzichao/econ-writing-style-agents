# Writing Style Analysis: Difference-in-Differences with Compositional Changes

## Paper Info
- Authors: Pedro H. C. Sant'Anna, Qi Xu
- ArXiv v1 date: April 27, 2023 (arXiv:2304.13925v1)
- Published: Journal of Econometrics, 2026, 253, 106147

## Abstract Comparison
### v1 Abstract
"This paper studies difference-in-differences (DiD) setups with repeated cross-sectional data and potential compositional changes across time periods. We begin our analysis by deriving the efficient influence function and the semiparametric efficiency bound for the average treatment effect on the treated (ATT). We introduce nonparametric estimators that attain the semiparametric efficiency bound under mild rate conditions on the estimators of the nuisance functions, exhibiting a type of rate doubly-robust (DR) property. Additionally, we document a trade-off related to compositional changes: We derive the asymptotic bias of DR DiD estimators that erroneously exclude compositional changes and the efficiency loss when one fails to correctly rule out compositional changes. We propose a nonparametric Hausman-type test for compositional changes based on these trade-offs. The finite sample performance of the proposed DiD tools is evaluated through Monte Carlo experiments and an empirical application. As a by-product of our analysis, we present a new uniform stochastic expansion of the local polynomial multinomial logit estimator, which may be of independent interest."

### Final Abstract
"This paper studies Difference-in-Differences (DiD) setups with repeated cross-sectional data and potential compositional changes across time periods. We begin our analysis by deriving the efficient influence function and the semiparametric efficiency bound for the average treatment effect on the treated (ATT). We introduce nonparametric estimators that attain the semiparametric efficiency bound under mild rate conditions on the estimators of the nuisance functions, exhibiting a type of rate doubly robust (DR) property. Additionally, we document a trade-off related to compositional changes: We derive the asymptotic bias of DR DiD estimators that erroneously exclude compositional changes and the efficiency loss when one fails to correctly rule out compositional changes. We propose a nonparametric Hausman-type test for compositional changes based on these trade-offs. The finite sample performance of the proposed DiD tools is evaluated through Monte Carlo experiments and an empirical application. We consider extensions of our framework that accommodate double machine learning procedures with cross-fitting, and setups when some units are observed in both pre- and post-treatment periods. As a by-product of our analysis, we present a new uniform stochastic expansion of the local polynomial multinomial logit estimator, which may be of independent interest."

### Changes Analysis
The abstract differences are minimal:
1. **Capitalization**: "difference-in-differences" becomes "Difference-in-Differences" -- conforming to journal house style.
2. **Hyphenation**: "doubly-robust" becomes "doubly robust" -- removing the unnecessary hyphen, which is the standard convention.
3. **New sentence about extensions**: The published version adds "We consider extensions of our framework that accommodate double machine learning procedures with cross-fitting, and setups when some units are observed in both pre- and post-treatment periods." This signals significant additional content in the published version, covering DML/cross-fitting and overlapping panel/cross-section data.

## Introduction Comparison
### Key Changes
The introduction is remarkably stable between versions, with the following changes:

1. **Additional extension content**: The published version adds discussion of extensions to double machine learning with cross-fitting, and to settings where some units are observed in both time periods (overlapping panel and cross-sectional data). This reflects additional theoretical contributions added during the review process.

2. **Minor phrasing adjustments**: Throughout, small wording changes tighten the prose. For instance, the discussion of the Sequeira (2016) empirical application is slightly polished.

3. **Organization paragraph updated**: The published version's organization paragraph reflects the additional content (new extensions section).

4. **Supplemental appendix reference**: The v1 refers to "the Supplemental Appendix available here" with a hyperlink, while the published version uses the journal's standard supplementary materials format.

5. **Literature discussion refinement**: The published version slightly updates the related literature section to position the DML/cross-fitting extension relative to Chang (2020) and other recent work.

## Conclusion/Discussion Comparison
### Key Changes
Both versions contain a "Concluding remarks" section (Section 7). The core message is stable:

**v1 conclusion** discusses: DR estimator for ATT with time-varying covariates, novel results on local multinomial logit, comparison with Sant'Anna and Zhao (2020), Hausman test, Monte Carlo and empirical application results.

**Published conclusion** is essentially the same but adds a note about the extensions: "We consider extensions that accommodate DML procedures and overlapping cross-sections/panel data" (paraphrased). The final paragraph about future work on staggered adoption with compositional changes remains in both versions.

The concluding remarks are notably concise in both versions -- just two paragraphs -- reflecting a preference for brevity in the conclusion.

## Writing Style Patterns Observed
- **Sentence Structure**: The writing style is highly consistent between v1 and the published version. Sentences in the introduction are well-constructed and remained largely unchanged. This suggests the paper was already well-polished at the v1 stage.
- **Vocabulary/Terminology**: Very stable. The only notable change is "doubly-robust" to "doubly robust" (removing hyphen). The paper consistently uses precise econometric terminology.
- **Framing/Motivation**: The motivating examples (Napster/music sales from Hong 2013) and the discussion of why compositional changes matter are identical across versions. The framing was already well-developed in v1.
- **Precision**: Both versions are highly precise. The published version adds extensions that increase the paper's scope without changing the precision of existing claims.
- **Tone**: Academic and measured throughout. The paper avoids overclaiming and carefully qualifies its contributions relative to existing work (Sant'Anna and Zhao 2020, Hong 2013, etc.).
- **Conciseness**: The paper is concise in both versions. The conclusion is notably short (two paragraphs), suggesting a preference for letting results speak for themselves.
- **Reader Engagement**: The use of concrete motivating examples (Napster, Sequeira 2016 tariff liberalization) in the introduction is effective and unchanged across versions. The paper is accessible to applied researchers despite its theoretical content.

## Specific Revision Examples

1. **Before (v1):** "exhibiting a type of rate doubly-robust (DR) property"
   **After (published):** "exhibiting a type of rate doubly robust (DR) property"
   **Why:** Standard terminology in the literature does not hyphenate "doubly robust" when used as a compound modifier in this context. This is a minor but precise conformance to convention.

2. **Before (v1):** [No mention of DML/cross-fitting extensions]
   **After (published):** "We consider extensions of our framework that accommodate double machine learning procedures with cross-fitting, and setups when some units are observed in both pre- and post-treatment periods."
   **Why:** The published version incorporates extensions likely requested during the review process or developed during the revision period. Adding DML/cross-fitting makes the paper relevant to the rapidly growing machine learning in econometrics literature. The overlapping data extension addresses a practical scenario many researchers face.

3. **Before (v1):** "Proofs and additional results are reported in the Supplemental Appendix available here."
   **After (published):** [Uses journal's standard supplementary materials framework with DOI link]
   **Why:** The v1 version's informal "available here" hyperlink is replaced by the journal's formal supplementary materials system, reflecting the transition from working paper to published article.

4. **Before (v1):** "we show that even when all nuisance functions are correctly specified, the Sant'Anna and Zhao (2020)'s DR DiD estimand does not identify the ATT in this general setup"
   **After (published):** [Same substantive claim, minor rephrasing]
   **Why:** This strong claim about an existing paper's limitations is maintained essentially unchanged. The willingness to clearly state where existing methods fail -- even one's own prior work -- is a notable feature of Sant'Anna's style.

5. **Before (v1):** "An intriguing extension of our work is to the case when the number of time periods is greater than two and when the treatment adoption is staggered"
   **After (published):** [Same sentence preserved in conclusion]
   **Why:** The forward-looking statement about future work is kept verbatim, suggesting this was a genuinely planned research direction (and indeed, Callaway and Sant'Anna 2021 addresses the staggered case).
