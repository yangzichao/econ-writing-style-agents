# Writing Style Analysis: Better Understanding Triple Differences Estimators

## Paper Info
- Authors: Marcelo Ortiz-Villavicencio, Pedro H. C. Sant'Anna
- ArXiv v1 date: May 15, 2025
- Latest draft date: July 18, 2025

## Abstract Comparison
### v1 Abstract
"Triple Differences (DDD) designs are widely used in empirical work to relax parallel trends assumptions in Difference-in-Differences (DiD) settings. This paper shows that common DDD implementations--such as taking the difference between two DiDs or applying three-way fixed effects regressions--are generally invalid when identification requires conditioning on covariates. In staggered adoption settings, the common DiD practice of pooling all not-yet-treated units as a comparison group introduces additional bias, even when covariates are not required for identification. These insights challenge conventional empirical strategies and underscore the need for estimators tailored specifically to DDD structures. We develop regression adjustment, inverse probability weighting, and doubly robust estimators that remain valid under covariate-adjusted DDD parallel trends. For staggered designs, we show how to correctly leverage multiple comparison groups to get more informative inference. Simulations highlight substantial bias reductions and precision gains relative to standard approaches, offering a new framework for credible DDD estimation in empirical research."

### Final/Latest Abstract
"Triple Differences (DDD) designs are widely used in empirical work to relax parallel trends assumptions in Difference-in-Differences (DiD) settings. This paper highlights that common DDD implementations--such as taking the difference between two DiDs or applying three-way fixed effects regressions--are generally invalid when identification requires conditioning on covariates. In staggered adoption settings, the common DiD practice of pooling all not-yet-treated units as a comparison group can introduce additional bias, even when covariates are not required for identification. These insights challenge conventional empirical strategies and underscore the need for estimators tailored specifically to DDD structures. We develop regression adjustment, inverse probability weighting, and doubly robust estimators that remain valid under covariate-adjusted DDD parallel trends. For staggered designs, we demonstrate how to effectively utilize multiple comparison groups to obtain more informative inferences. Simulations and three empirical applications highlight bias reductions and precision gains relative to standard approaches. A companion R package is available."

### Changes Analysis
Several targeted revisions in the abstract:
1. "shows" changed to "highlights" -- softens the claim slightly, making it less confrontational
2. "introduces additional bias" changed to "can introduce additional bias" -- adds hedging with "can," acknowledging it is a possibility rather than a certainty
3. "we show how to correctly leverage" changed to "we demonstrate how to effectively utilize" -- "demonstrate" is more formal; "effectively utilize" replaces "correctly leverage"
4. "Simulations highlight substantial bias reductions" changed to "Simulations and three empirical applications highlight bias reductions" -- adds empirical applications (new content), removes "substantial" (less self-promotional)
5. "offering a new framework for credible DDD estimation in empirical research" replaced with "A companion R package is available" -- replaces a vague claim with a concrete practical offering
6. Added "A companion R package is available" -- practical implementation emphasis

## Introduction Comparison
### Key Changes
1. **Softened language throughout**: "more traditional two-way fixed-effects specifications" became "simple two-way fixed-effects specifications"; "an important concern" became simply "a concern"; "not accurate approximations" became "not reasonable enough approximations."
2. **Literature presentation expanded**: v1 relegated examples to a footnote ("Additional examples of papers using DDD strategy include..."), while the latest integrates prominent applications directly into the text: "Some prominent recent DDD applications include Antwi, Moriya and Simon (2013), Walker (2013)... see Olden and Moen (2022) for additional documentation of DDD applications, and Section 6 for three DDD applications."
3. **Mission statement refined**: v1 had "This article aims to improve our understanding of Triple Difference (DDD) designs. We study identification, estimation, and inference procedures..." The latest adds a clearer practical goal: "Our main goal is to provide a set of clear, easy-to-use, and theoretically grounded tools that empirical researchers can utilize whenever they wish to explore DDD designs."
4. **"Surprising" toned down**: v1 used "uncover surprising results," which became "uncover interesting results" -- less self-congratulatory.
5. **Empirical applications added**: The latest version adds a full paragraph summarizing three empirical applications (Cai 2016, Cui et al. 2018, Hansen and Wingender 2023), which were absent in v1.
6. **R package mentioned**: The latest adds "To ease the adoption of our proposed DDD tools, we provide an open-source R package, triplediff."
7. **"Erroneously proceeding"**: v1 said "erroneously proceeding as if DDD was just the difference between two DiD estimators"; latest softens to "proceeding as if DDD were just the difference between two DiD estimators" (drops "erroneously," uses subjunctive "were").
8. **Naming changes**: v1 used "AT T dr,opt" while latest uses "AT T dr,gmm" -- aligning terminology with GMM interpretation.

## Conclusion/Discussion Comparison
### Key Changes
The conclusion section was not substantially available in the extracted text for either version, as the main body sections extend to the page ranges extracted. However, the organization paragraph at the end of the introduction shifted from v1's "conclusions drawn in Section 6" to the latest's "Section 6 presents three empirical illustrations. Section 7 concludes" -- reflecting the addition of a new empirical section.

## Writing Style Patterns Observed
- **Sentence Structure**: Long but well-organized sentences. Uses em-dashes and parenthetical examples to pack information. The latest version tends toward slightly shorter, more direct sentences.
- **Vocabulary/Terminology**: Shift from assertive/confrontational vocabulary ("shows," "erroneously") to softer, more measured language ("highlights," "can introduce"). Practical language ("easy-to-use," "tools") is amplified in the revision.
- **Framing/Motivation**: Both versions use the "challenging conventional wisdom" framing, but the latest version adds a stronger practical/applied motivation by emphasizing the companion R package and three empirical applications.
- **Precision**: Both versions maintain high precision. The latest improves by adding the hedging "can" where earlier claims were too absolute.
- **Tone**: The revision moves from slightly confrontational ("This paper shows that... are generally invalid") to a more collaborative, constructive tone ("This paper highlights..."). The softening of "surprising" to "interesting" is characteristic.
- **Conciseness**: The abstract becomes slightly shorter by removing self-promotional phrasing ("offering a new framework for credible DDD estimation in empirical research") and replacing it with practical information ("A companion R package is available").
- **Reader Engagement**: The latest version is more reader-friendly, emphasizing practical tools, software, and empirical illustrations that practitioners can use immediately.

## Specific Revision Examples

1. **Softening absolute claims**:
   - v1: "This paper **shows** that common DDD implementations... are generally invalid"
   - Latest: "This paper **highlights** that common DDD implementations... are generally invalid"
   - *Why*: "Shows" implies proof; "highlights" is more collaborative, drawing attention rather than declaring a finding.

2. **Adding hedging**:
   - v1: "pooling all not-yet-treated units as a comparison group **introduces** additional bias"
   - Latest: "pooling all not-yet-treated units as a comparison group **can introduce** additional bias"
   - *Why*: The added "can" acknowledges that bias is context-dependent, not inevitable. This is a more precise statement.

3. **Reducing self-promotion, adding practicality**:
   - v1: "...offering a new framework for credible DDD estimation in empirical research."
   - Latest: "...A companion R package is available."
   - *Why*: Replaces vague self-promotional framing with a concrete deliverable that practitioners care about.

4. **Mission statement clarification**:
   - v1: "This article aims to improve our understanding of Triple Difference (DDD) designs. We study identification, estimation, and inference procedures..."
   - Latest: "This article aims to improve our understanding of Triple Difference (DDD) designs. Our main goal is to provide a set of clear, easy-to-use, and theoretically grounded tools that empirical researchers can utilize..."
   - *Why*: The revision foregrounds practical utility. "Clear, easy-to-use, and theoretically grounded tools" signals the paper's service orientation.

5. **Toning down surprise rhetoric**:
   - v1: "uncover **surprising** results that challenge some conventional wisdom"
   - Latest: "uncover **interesting** results that challenge some conventional wisdom"
   - *Why*: "Surprising" can seem self-aggrandizing; "interesting" is neutral and lets readers judge.
