# Writing Style Analysis: Efficient Estimation for Staggered Rollout Designs

## Paper Info
- Authors: Jonathan Roth, Pedro H.C. Sant'Anna
- ArXiv v1 date: February 2, 2021 (posted), with v1 document dated November 20, 2021
- Published: Final version dated May 16, 2023; Roth at Brown University, Sant'Anna at Emory University (published as working paper / forthcoming)

## Abstract Comparison

### v1 Abstract
"Researchers are often interested in the causal effect of treatments that are rolled out to different units at different points in time. This paper studies how to efficiently estimate a variety of causal parameters in such staggered rollout designs when treatment timing is (as-if) randomly assigned. We solve for the most efficient estimator in a class of estimators that nests two-way fixed effects models as well as several popular generalized difference-in-differences methods. The efficient estimator is not feasible in practice because it requires knowledge of the optimal weights to be placed on pre-treatment outcomes. However, the optimal weights can be estimated from the data, and in large datasets the plug-in estimator that uses the estimated weights has similar properties to the 'oracle' efficient estimator. We illustrate the performance of the plug-in efficient estimator in simulations and in an application to Wood, Tyler and Papachristos (2020a)'s study of the staggered rollout of a procedural justice training program for police officers. We find that confidence intervals based on the plug-in efficient estimator have good coverage and can be as much as five times shorter than confidence intervals based on existing methods. As an empirical contribution of independent interest, our application provides the most precise estimates to date on the effectiveness of procedural justice training programs for police officers."

### Final Abstract
"We study estimation of causal effects in staggered rollout designs, i.e. settings where there is staggered treatment adoption and the timing of treatment is as-good-as randomly assigned. We derive the most efficient estimator in a class of estimators that nests several popular generalized difference-in-differences methods. A feasible plug-in version of the efficient estimator is asymptotically unbiased with efficiency (weakly) dominating that of existing approaches. We provide both t-based and permutation-test-based methods for inference. In an application to a training program for police officers, confidence intervals for the proposed estimator are as much as eight times shorter than for existing approaches."

### Changes Analysis

1. **Dramatic condensation**: The v1 abstract is approximately 170 words; the final is approximately 90 words -- nearly a 50% reduction. Every sentence was tightened.

2. **Opening simplification**: "Researchers are often interested in the causal effect of treatments that are rolled out to different units at different points in time" became "We study estimation of causal effects in staggered rollout designs, i.e. settings where there is staggered treatment adoption and the timing of treatment is as-good-as randomly assigned." The revision eliminates the "researchers are interested" throat-clearing and adds a concise definition inline.

3. **Terminology shift**: "(as-if) randomly assigned" became "as-good-as randomly assigned" -- a more natural and widely understood phrasing. This language is used consistently throughout the final version.

4. **Elimination of narrative structure**: The v1 abstract tells a story: here's the problem, here's the oracle, it's infeasible, but a plug-in works. The final version simply states results: we derive the efficient estimator, a plug-in version works, here's what it does.

5. **Removal of TWFE**: The v1 abstract mentions nesting "two-way fixed effects models as well as several popular generalized difference-in-differences methods." The final drops the TWFE reference, keeping only "several popular generalized difference-in-differences methods." This likely reflects the literature's move away from TWFE as a benchmark.

6. **Added content**: The final abstract adds "permutation-test-based methods for inference" -- a new methodological contribution not in the v1. It also adds the qualifier "(weakly)" before "dominating" -- a technically precise hedge.

7. **Updated empirical magnitude**: "five times shorter" became "eight times shorter" -- reflecting updated or refined empirical results.

8. **Removed self-promotion**: The v1 ends with "As an empirical contribution of independent interest, our application provides the most precise estimates to date on the effectiveness of procedural justice training programs for police officers." The final version cuts this entirely, letting the numbers speak.

## Introduction Comparison

### Key Changes

1. **Structural reorganization**: The v1 introduction spans approximately 6 pages and covers the two-period intuition, the staggered setting, detailed comparison to existing methods, and the full application background. The final introduction is approximately 5.5 pages but is more efficiently organized, with a clearer separation of intuition, main results, and application.

2. **Intuition development refined**: Both versions use the two-period case to build intuition. However, the final version introduces equation (1) directly in the introduction with a cleaner notation (post-treatment diff minus beta times pre-treatment diff), making the key idea immediately visual.

3. **Stronger framing of the assumption**: The v1 uses "(as-if) randomly assigned" throughout. The final shifts to "(quasi-)randomly assigned" or "as good as randomly assigned," which is more specific and widely understood. The final version also adds a new paragraph with concrete empirical examples of papers that justify parallel trends via quasi-random timing (Deshpande and Li 2019, Fadlon and Nielsen 2021, Parker et al. 2013).

4. **New inference methods highlighted**: The final introduction prominently features the Fisher Randomization Test (FRT) contribution, which was absent from the v1 introduction. A full paragraph describes "two complementary approaches to inference" -- t-based and FRT-based.

5. **Application narrative refined**: The v1 discusses the Wood et al. discovery of a statistical error and subsequent correction. The final version retells this narrative more concisely but adds the precision comparison to the Callaway and Sant'Anna re-analysis: "For complaints, for example, we are able to rule out reductions larger than 13% of the pre-treatment mean using our proposed estimator, compared with an upper bound of 33% in the previous analysis."

6. **Software packages added**: The final version includes a footnote mentioning the staggered R and Stata packages with GitHub links -- a practical addition for implementability.

7. **Related literature expansion**: The final version adds several new references and engages more carefully with the stepped wedge design literature from biostatistics (e.g., Ji et al. 2017, Lindner and McConnell 2021).

8. **Affiliation changes**: Roth moved from Microsoft to Brown University; Sant'Anna moved from Vanderbilt to Emory University, reflecting career moves during the revision period.

## Conclusion/Discussion Comparison

### Key Changes

1. **Length and content**: The v1 conclusion is a single compact paragraph (Section 6, approximately 10 lines). The final version has a slightly expanded conclusion at a similar length.

2. **Key message preserved**: Both versions make the same core point: the paper derives the efficient estimator under random treatment timing, shows a plug-in version works, and applies it to police training. The wording is nearly identical.

3. **Precision of claims**: The v1 states the plug-in efficient estimator "substantially increases precision relative to existing methods." The final is more specific: the efficient estimator has "efficiency (weakly) dominating that of existing approaches."

4. **Inference methods added**: The final conclusion mentions "derive a valid variance estimator for construction of confidence intervals" while also noting that FRT-based inference is available.

5. **Self-citation updated**: The final version now says "the most precise estimates to date" of procedural justice training effects (same as v1), but this claim is now better supported by the larger efficiency gains reported.

## Writing Style Patterns Observed

- **Sentence Structure**: Sentences became more compact and declarative. The v1 frequently uses complex sentence structures with multiple clauses ("Although the 'oracle' beta* will generally not be known, as in Lin (2013), a plug-in estimator based on a sample analog of beta* will achieve the efficient variance in large populations"). The final version breaks such constructions into shorter, punchier sentences.

- **Vocabulary/Terminology**: "(as-if) randomly assigned" shifted to "(quasi-)randomly assigned" or "as good as randomly assigned" -- both more natural phrases. "Two-way fixed effects" is de-emphasized in favor of the more precise "generalized difference-in-differences methods." The term "staggered rollout design" is used more prominently in the title and framing, positioning the paper within a specific design category.

- **Framing/Motivation**: The v1 frames the paper primarily as extending DiD methods to be more efficient. The final version reframes it as a general solution for staggered treatment timing when treatment is quasi-random, with DiD methods being just one class within the broader estimator class. This is a subtle but important shift -- the paper is positioned as providing the solution for a design, not just improving existing estimators.

- **Precision**: Technical claims became more carefully hedged. "Efficient" gained qualifiers like "(weakly) dominating." "Similar properties" became "asymptotically unbiased with efficiency (weakly) dominating." The distinction between finite-sample and asymptotic properties is made more carefully throughout.

- **Tone**: The v1 has a somewhat promotional tone ("As an empirical contribution of independent interest, our application provides the most precise estimates to date"). The final version is more restrained, letting quantitative claims (e.g., "eight times shorter") speak for themselves.

- **Conciseness**: The abstract was cut nearly in half. Technical details that could be inferred (e.g., the oracle is infeasible) were removed in favor of direct statements of results.

- **Reader Engagement**: The final version adds more concrete empirical motivating examples in the introduction (multiple papers citing quasi-random timing justifications), making the practical relevance of the assumption more vivid. Software package references increase accessibility.

## Specific Revision Examples

### Example 1: Abstract opening
**v1**: "Researchers are often interested in the causal effect of treatments that are rolled out to different units at different points in time. This paper studies how to efficiently estimate a variety of causal parameters in such staggered rollout designs when treatment timing is (as-if) randomly assigned."
**Final**: "We study estimation of causal effects in staggered rollout designs, i.e. settings where there is staggered treatment adoption and the timing of treatment is as-good-as randomly assigned."
**Analysis**: Two sentences compressed into one. The "researchers are interested" phrasing -- a common but passive way of motivating a paper -- is eliminated. The inline definition ("i.e. settings where...") efficiently handles context-setting. "As-if" became "as-good-as," which reads more naturally and avoids the awkward hyphenation.

### Example 2: Describing the two-period intuition
**v1**: "All units are untreated in the first period, and a subset of units are randomly assigned to begin treatment in the second period. We consider estimators of the average treatment effect (ATE) of the form..."
**Final**: "To develop intuition, it is instructive to first consider the special case... This special case is analogous to conducting a randomized experiment in period 2, with the outcome in period 1 serving as a pre-treatment covariate."
**Analysis**: The final version explicitly frames the two-period case as pedagogical intuition-building rather than a result in its own right. The analogy to a randomized experiment with covariates is made more prominent, which helps readers unfamiliar with the design-based framework grasp the key insight immediately.

### Example 3: Introduction of the FRT contribution
**v1**: No mention of Fisher Randomization Tests in the introduction.
**Final**: "Second, an appealing feature of our (quasi-)random treatment timing framework is that it permits us to construct Fisher randomization tests (FRTs), also known as permutation tests. Following Wu and Ding (2021) and Zhao and Ding (2021) for cross-sectional randomized experiments, we consider FRTs based on a studentized version of our efficient estimator. These FRTs have the dual advantages that they are finite-sample exact under the sharp null of no treatment effects, and asymptotically valid for the weak null of no average effects."
**Analysis**: This is entirely new material. The addition of FRT methods substantially strengthened the paper's contribution. The clear statement of "dual advantages" (finite-sample exact for sharp null + asymptotically valid for weak null) is a model of concise technical communication.

### Example 4: Comparison to parallel trends
**v1 (Related Literature)**: "In contrast to most of the previous literature, we consider the efficiency of various procedures under random treatment timing. This assumption is stronger than the generalized parallel trends assumptions considered in previous work, and thus our proposed method will not be applicable in settings where the researcher is confident in parallel trends but not in random treatment timing."
**Final (Remark 2)**: Upgraded to a formal remark with detailed discussion, including: "it is frequently the case that the justification given for the validity of the parallel-trends assumption also justifies Assumption 1" with citations to Fadlon and Nielsen, Deshpande and Li, etc. Adds: "it is also worth emphasizing that in non-experimental contexts, the random timing assumption may be more plausible if one restricts attention to units who are eventually treated."
**Analysis**: What was a brief caveat in the v1 became a substantive discussion point. This reflects a common revision pattern: referees likely pushed back on the strength of the random timing assumption, so the authors added a more thorough defense. The addition of concrete empirical examples of papers justifying quasi-random timing is persuasive and practical.

### Example 5: Empirical magnitude update
**v1**: "confidence intervals based on the plug-in efficient estimator have good coverage and can be as much as five times shorter"
**Final**: "confidence intervals for the proposed estimator are as much as eight times shorter than for existing approaches"
**Analysis**: The updated magnitude (5x to 8x) likely reflects: (a) additional comparisons (Sun and Abraham added as a comparator in the final version), (b) refined estimation, or (c) different aggregation schemes. This quantitative improvement strengthens the empirical case substantially while demonstrating that the paper's methodology continued to be refined during revision.
