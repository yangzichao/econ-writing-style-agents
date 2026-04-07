# Writing Style Analysis: Difference-in-Differences with Multiple Time Periods

## Paper Info
- Authors: Brantly Callaway, Pedro H. C. Sant'Anna
- ArXiv v1 date: March 23, 2018
- Published: Journal of Econometrics, 2021 (accepted December 1, 2020)

## Abstract Comparison
### v1 Abstract
"Difference-in-Differences (DID) is one of the most important and popular designs for evaluating causal effects of policy changes. In its standard format, there are two time periods and two groups: in the first period no one is treated, and in the second period a 'treatment group' becomes treated, whereas a 'control group' remains untreated. However, many empirical applications of the DID design have more than two periods and variation in treatment timing. In this article, we consider identification and estimation of treatment effect parameters using DID with (i) multiple time periods, (ii) variation in treatment timing, and (iii) when the 'parallel trends assumption' holds potentially only after conditioning on observed covariates. We propose a simple two-step estimation strategy, establish the asymptotic properties of the proposed estimators, and prove the validity of a computationally convenient bootstrap procedure. Furthermore we propose a semiparametric data-driven testing procedure to assess the credibility of the DID design in our context. Finally, we analyze the effect of the minimum wage on teen employment from 2001-2007. By using our proposed methods we confront the challenges related to variation in the timing of the state-level minimum wage policy changes. Open-source software is available for implementing the proposed methods."

### Final Abstract
"In this article, we consider identification, estimation, and inference procedures for treatment effect parameters using Difference-in-Differences (DiD) with (i) multiple time periods, (ii) variation in treatment timing, and (iii) when the 'parallel trends assumption' holds potentially only after conditioning on observed covariates. We show that a family of causal effect parameters are identified in staggered DiD setups, even if differences in observed characteristics create non-parallel outcome dynamics between groups. Our identification results allow one to use outcome regression, inverse probability weighting, or doubly-robust estimands. We also propose different aggregation schemes that can be used to highlight treatment effect heterogeneity across different dimensions as well as to summarize the overall effect of participating in the treatment. We establish the asymptotic properties of the proposed estimators and prove the validity of a computationally convenient bootstrap procedure to conduct asymptotically valid simultaneous (instead of pointwise) inference. Finally, we illustrate the relevance of our proposed tools by analyzing the effect of the minimum wage on teen employment from 2001-2007. Open-source software is available for implementing the proposed methods."

### Changes Analysis
1. **Removed pedagogical preamble**: v1 opens with a textbook-like explanation of DID ("DID is one of the most important and popular designs..."). The published version cuts this entirely and jumps directly to the contribution: "In this article, we consider identification, estimation, and inference procedures..."
2. **Added "inference" to the scope**: v1 says "identification and estimation"; published adds "and inference" -- broadening the stated contribution.
3. **New content on identification**: Published adds "We show that a family of causal effect parameters are identified in staggered DiD setups, even if differences in observed characteristics create non-parallel outcome dynamics between groups" -- a key identification result emphasized in the revision.
4. **Multiple estimation approaches**: Published adds "Our identification results allow one to use outcome regression, inverse probability weighting, or doubly-robust estimands" -- reflecting the paper's expansion to include DR estimators (not in v1).
5. **Aggregation schemes**: Published adds explicit mention of "different aggregation schemes" -- a major new contribution not in v1.
6. **Simultaneous vs. pointwise inference**: Published specifies "simultaneous (instead of pointwise) inference" -- a technical distinction absent from v1's abstract.
7. **Removed pre-testing**: v1 mentions "a semiparametric data-driven testing procedure to assess the credibility of the DID design." This is dropped from the published abstract entirely.
8. **Terminology shift**: "DID" becomes "DiD" throughout the published version -- adopting a different capitalization convention.
9. **"control group" becomes implicit**: v1 uses "control group" in quotes; published avoids this terminology (reflecting the broader shift in causal inference literature toward "comparison group").

## Introduction Comparison
### Key Changes
1. **Structural overhaul**: The published introduction is substantially restructured with a clear three-step framework: "(i) identification of policy-relevant disaggregated causal parameters; (ii) aggregation of these parameters to form summary measures of the causal effects; and (iii) estimation and inference about these different target parameters." This organizing framework is entirely absent from v1.
2. **TWFE critique integration**: The published version explicitly frames the contribution against the TWFE literature: "Our approach allows for estimation and inference on interpretable causal parameters allowing for arbitrary treatment effect heterogeneity and dynamic effects, thereby completely avoiding the issues of interpreting results of standard two-way fixed effects (TWFE) regressions." v1 mentions this issue but less prominently.
3. **Doubly robust estimators added**: The published version introduces three estimation approaches (outcome regression, IPW, doubly robust), reflecting a major expansion not in v1.
4. **Treatment anticipation**: Published adds explicit discussion of treatment anticipation behavior: "our proposed estimands explicitly reflect these assumptions" -- a new theoretical feature.
5. **Covariates discussion expanded**: Published adds a full paragraph about the importance of covariates in staggered DiD, including the statement "To the best of our knowledge, this paper is the first to show how one can allow for covariate-specific trends across groups in DiD setups with variation in treatment timing."
6. **Extensive related literature section**: Published adds a full "Recent Related Literature" subsection with detailed comparisons to de Chaisemartin and D'Haultfoeuille (2020), Sun and Abraham (2020), and Athey and Imbens (2018). v1's literature discussion was brief and embedded in the introduction.
7. **Empirical results presentation**: v1's introduction provides detailed empirical results (specific percentages like "2.3% to 13.6% lower teen employment"). The published version gives only qualitative summary: "using our approach leads to qualitatively different results than results from the TWFE estimator."
8. **Terminology evolution**: "individuals" becomes "units" throughout -- reflecting a more general causal inference framing rather than labor economics-specific language.

## Conclusion/Discussion Comparison
### Key Changes
1. **v1 conclusion**: Brief, summarizes three contributions: (a) group-time ATTs as well-defined parameters, (b) estimation with bootstrap, (c) pre-test for parallel trends. Mentions empirical findings about minimum wage and the caveat about rejecting parallel trends.
2. **Published conclusion**: Much more expansive. Adds explicit discussion of: (a) aggregation schemes for summarizing heterogeneity; (b) suitability for conditional parallel trends, different comparison groups, and treatment anticipation; (c) outcome regression, IPW, and doubly-robust identification; (d) simultaneous inference procedures. The published conclusion notably drops the pre-test and instead emphasizes "flexibility" as a key feature.
3. **Empirical caveats**: v1 says "we found evidence against both the unconditional and conditional parallel trends assumption." Published is more nuanced: "some of the estimates of pseudo group-time average treatment effects in pre-treatment periods... are significantly different from zero which provides some suggestive evidence against the parallel trends assumption."
4. **Forward-looking framing**: Published adds: "the choice of estimation method can potentially lead to qualitatively different conclusions" as the key takeaway -- reframing from specific empirical findings to a methodological lesson.

## Writing Style Patterns Observed
- **Sentence Structure**: Published version uses shorter, more declarative sentences. v1's long compound sentences (often 3-4 clauses) are broken into separate statements. The published version also uses more bullet-point-like lists.
- **Vocabulary/Terminology**: Significant shifts: "individuals" to "units," "DID" to "DiD," "control group" to "comparison group," addition of "staggered adoption" terminology. The language becomes more aligned with the modern causal inference literature.
- **Framing/Motivation**: v1 frames the paper around the gap between theory and practice (TWFE regressions); the published version frames it as providing a "unified framework" with three clear steps. The framing evolves from problem-identification to solution-provision.
- **Precision**: The published version is far more precise about what assumptions are needed for what results. Treatment anticipation, different parallel trends assumptions, and different comparison groups are all explicitly delineated.
- **Tone**: v1 is more tentative ("we aim to fill this important gap"); published is more assertive ("We provide a unified framework"). The published version conveys greater confidence in the contribution, likely reflecting the maturation of the work.
- **Conciseness**: Paradoxically, the published version is longer but more efficient. v1's long empirical results paragraphs in the introduction are replaced by concise methodological descriptions. The paper expanded in scope (DR estimators, aggregation) but each part is expressed more tightly.
- **Reader Engagement**: Published version adds explicit "roadmap" subsections, clear labels for different parallel trends assumptions, and discussion of practical trade-offs. The structure guides the reader more deliberately.

## Specific Revision Examples

### Example 1: Opening sentence
- **v1**: "Difference-in-Differences (DID) is one of the most important and popular designs for evaluating causal effects of policy changes. In its standard format, there are two time periods and two groups..."
- **Published**: "Difference-in-Differences (DiD) has become one of the most popular research designs used to evaluate causal effects of policy interventions."
- **Analysis**: The pedagogical preamble is compressed. "one of the most important and popular" becomes simply "one of the most popular" -- removing the self-congratulatory "important." "designs" gains "research" as a modifier. "policy changes" becomes "policy interventions" -- slightly more formal.

### Example 2: Core contribution statement
- **v1**: "In this article we aim to fill this important gap and consider identification and inference procedures for average treatment effects in DID models with (i) multiple time periods, (ii) variation in treatment timing, and (iii) when the parallel trends assumption holds potentially only after conditioning on observed covariates."
- **Published**: "In this article, we provide a unified framework for average treatment effects in DiD setups with multiple time periods, variation in treatment timing, and when the parallel trends assumption holds potentially only after conditioning on observed covariates."
- **Analysis**: "aim to fill this important gap" (hedging, self-importance) becomes "provide a unified framework" (confident, descriptive). "DID models" becomes "DiD setups" -- "setups" is broader than "models." The numbered list (i), (ii), (iii) is dropped in favor of a flowing comma-separated list, improving readability.

### Example 3: Terminology evolution
- **v1**: "in the first period, no one is treated and in the second period some individuals are treated (the treated group) and some individuals are not (the control group)."
- **Published**: "in the first period no one is treated, and in the second period some units are treated (the treated group), and some units are not (the comparison group)."
- **Analysis**: "individuals" becomes "units" (twice) -- making the framework applicable beyond labor economics. "control group" becomes "comparison group" -- following the causal inference convention that distinguishes experimental controls from observational comparisons.

### Example 4: Empirical motivation
- **v1**: "We use data from 2001-2007, where the federal minimum wage was flat at $5.15 per hour. Using a period where the federal minimum wage is flat allows for a clear source of identification -- state level changes in minimum wage policy."
- **Published**: "Here, we follow much empirical work on the effects of the minimum wage and exploit having access to panel data and variation in treatment timing across states..."
- **Analysis**: v1 provides specific institutional detail ($5.15/hour, rationale for period choice). Published abstracts away from these details, summarizing at a higher level. This reflects the paper's evolution from an applied paper with methods to a methods paper with an application.

### Example 5: Contribution framing
- **v1**: "Second, although these disaggregated group-time average treatment effects can be of interest by themselves, in some applications there are perhaps too many of them, potentially making the analysis of the effectiveness of the policy intervention harder..."
- **Published**: "Our framework acknowledges that in some applications there may be many group-time average treatment effects and researchers may want to aggregate them into different summary causal effect measures."
- **Analysis**: v1's hedging ("perhaps too many") becomes direct acknowledgment. "potentially making the analysis... harder" (negative framing) becomes "researchers may want to aggregate them" (positive, solution-oriented framing). The published version frames the same issue as a feature rather than a problem.
