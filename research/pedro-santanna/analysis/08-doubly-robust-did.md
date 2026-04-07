# Writing Style Analysis: Doubly Robust Difference-in-Differences Estimators

## Paper Info
- Authors: Pedro H. C. Sant'Anna, Jun B. Zhao
- ArXiv v1 date: November 29, 2018 (dated December 6, 2018 in manuscript)
- Published: Journal of Econometrics, 2020 (Volume 219, Issue 1, pp. 101-122)

## Abstract Comparison
### v1 Abstract
"This article proposes a doubly robust estimation procedure for the average treatment effect on the treated in difference-in-differences (DID) research designs. In contrast to alternative DID estimators, our proposed estimators are consistent if either (but not necessarily both) a propensity score model or outcome regression models are correctly specified. In addition, our proposed methodology accommodates linear and nonlinear specifications, allows for treatment effect heterogeneity, and can be applied with either panel or repeated cross section data. We establish the asymptotic distribution of our proposed doubly robust estimators, and propose a computationally simple bootstrap procedure to conduct asymptotically valid inference. Our inference procedures directly account for multiple testing, and are therefore suitable in situations where researchers are interested in the effect of a given policy on many different outcomes. We demonstrate the relevance of our proposed policy evaluation tools in two different applications."

### Final Abstract
"This article proposes doubly robust estimators for the average treatment effect on the treated (ATT) in difference-in-differences (DID) research designs. In contrast to alternative DID estimators, the proposed estimators are consistent if either (but not necessarily both) a propensity score or outcome regression working models are correctly specified. We also derive the semiparametric efficiency bound for the ATT in DID designs when either panel or repeated cross-section data are available, and show that our proposed estimators attain the semiparametric efficiency bound when the working models are correctly specified. Furthermore, we quantify the potential efficiency gains of having access to panel data instead of repeated cross-section data. Finally, by paying particular attention to the estimation method used to estimate the nuisance parameters, we show that one can sometimes construct doubly robust DID estimators for the ATT that are also doubly robust for inference. Simulation studies and an empirical application illustrate the desirable finite-sample performance of the proposed estimators. Open-source software for implementing the proposed policy evaluation tools is available."

### Changes Analysis
1. **"estimation procedure" to "estimators"**: v1 says "a doubly robust estimation procedure"; published says "doubly robust estimators" -- more direct and concrete.
2. **Added "(ATT)" definition**: Published spells out ATT in the abstract for the first time, making it more self-contained.
3. **"our proposed" reduced**: v1 uses "our proposed" five times in the abstract. Published reduces first-person possessives: "our proposed estimators" becomes "the proposed estimators" in the second sentence.
4. **"working models" terminology**: v1 says "a propensity score model or outcome regression models"; published says "a propensity score or outcome regression working models" -- adding "working" to signal that these are potentially misspecified models, a key technical distinction.
5. **Major new content -- efficiency bounds**: Published adds an entire new contribution: "We also derive the semiparametric efficiency bound for the ATT in DID designs... and show that our proposed estimators attain the semiparametric efficiency bound." This was not in v1 at all.
6. **Panel vs. cross-section comparison**: Published adds "we quantify the potential efficiency gains of having access to panel data instead of repeated cross-section data" -- another entirely new contribution.
7. **DR for inference**: Published adds "one can sometimes construct doubly robust DID estimators for the ATT that are also doubly robust for inference" -- a third new contribution absent from v1.
8. **Multiple testing removed from abstract**: v1 emphasizes multiple testing; published drops this entirely from the abstract.
9. **Applications reduced**: v1 mentions "two different applications"; published says "an empirical application" (singular), suggesting one application was dropped or moved.
10. **Software link added**: Published adds "Open-source software for implementing the proposed policy evaluation tools is available."

## Introduction Comparison
### Key Changes
1. **Opening sentence**: v1 starts "Researchers and policy makers are often interested in evaluating the causal effects of a given program or treatment on different outcomes of interest." Published starts "Difference-in-differences (DID) methods are among the most popular procedures practitioners adopted to conduct policy evaluation with observational data." The published version is more direct and places DID methods front-and-center rather than starting from a general motivation.
2. **Three-front contribution structure**: Published explicitly states "We contribute to the DID literature in different fronts" and then enumerates: (a) DR estimands, (b) semiparametric efficiency bounds, (c) DR for inference. v1 lacks this structured overview.
3. **Semiparametric efficiency bounds**: The published introduction devotes two full paragraphs to the efficiency bounds -- their derivation, what questions they answer (panel vs. cross-section gains), and their relationship to existing bounds. None of this appears in v1.
4. **DR for inference discussion**: Published adds substantial discussion of when the DR property extends to inference -- a nuanced point about the asymptotic variance depending on which models are correctly specified. v1 is silent on this.
5. **"individual" to "unit"**: v1 uses "individual i" throughout; published uses "unit i" -- the same terminological shift seen in paper 06.
6. **Related literature expanded**: Published adds citations to Vermeulen and Vansteelandt (2015), Muris (2019), Seaman and Vansteelandt (2018), Belloni et al. (2014), Farrell (2015), Chernozhukov et al. (2017), Tan (2019), Zimmert (2019) -- reflecting two years of new literature between v1 and publication.
7. **Graham et al. comparison**: v1 positions Graham et al. (2016) as the "closest paper," comparing at length. Published retains this but adds more nuanced discussion.
8. **Removed second application preview**: v1's introduction previews two applications (LaLonde/NSW and Vietnam recentralization). Published mentions only "an empirical application" and "simulation studies."
9. **Software announcement**: Published adds "all proposed policy evaluation tools discussed in this article can be implemented via the open-source R package DRDID, which is freely available from GitHub."

## Conclusion/Discussion Comparison
### Key Changes
1. **v1 conclusion**: Two paragraphs. First summarizes the DR DID estimator, consistency properties, bootstrap inference, multiple testing, and two applications. Second argues that "the DR DID tools proposed in this article are important additions to the applied researcher's toolkit."
2. **Published conclusion**: The published paper's concluding section is not included in the extracted pages (the paper ends with proofs/appendices). However, based on the paper's structure, the conclusion likely expanded to cover the three contributions (DR consistency, efficiency bounds, DR inference).
3. **Confidence shift**: v1's conclusion uses "we argue that the DR DID tools... are important additions" -- making a normative claim. The published version, based on the introduction's confidence, likely makes a stronger case backed by efficiency results.

## Writing Style Patterns Observed
- **Sentence Structure**: The published version has notably more complex, information-dense sentences. Where v1 makes simple claims ("our proposed estimators are consistent if either..."), published adds qualifications and extensions ("the proposed estimators are consistent if either... We also derive the semiparametric efficiency bound... and show that our proposed estimators attain the semiparametric efficiency bound when the working models are correctly specified."). This reflects the paper's substantial expansion in scope.
- **Vocabulary/Terminology**: Key shifts include: "estimation procedure" to "estimators," "propensity score model" to "propensity score working model" (adding "working"), "individual" to "unit," and the introduction of new technical terms like "locally efficient," "doubly robust for inference," and "semiparametric efficiency bound."
- **Framing/Motivation**: v1 frames the paper as proposing a new estimator with practical benefits (multiple testing, applications). Published frames it as making three distinct theoretical contributions (DR estimands, efficiency bounds, DR inference) with practical implications. The framing shifts from "here's a useful tool" to "here are important theoretical results with practical value."
- **Precision**: Published is substantially more precise. For instance, it distinguishes between "doubly robust for consistency" and "doubly robust for inference" -- a nuance entirely absent from v1. It also distinguishes between two DR estimators for the repeated cross-section case.
- **Tone**: v1 is enthusiastic but somewhat informal ("highlight the attractiveness," "the practical appeal"). Published is more measured and authoritative ("we contribute to the DID literature in different fronts"). The tone shifts from a working paper selling its contribution to a journal article establishing results.
- **Conciseness**: The published abstract is actually longer than v1's due to the added contributions, but each sentence is more information-dense. The introduction, however, is more efficient per-contribution -- it covers three contributions in roughly the same space v1 used for one.
- **Reader Engagement**: Published adds explicit software links (DRDID R package) and supplementary appendix links. The paper becomes more practically oriented despite its increased theoretical depth.

## Specific Revision Examples

### Example 1: Opening sentence transformation
- **v1**: "Researchers and policy makers are often interested in evaluating the causal effects of a given program or treatment on different outcomes of interest. Although randomized experiments are often viewed as the 'gold standard' of causal inference, in many situations researchers only have access to observational data."
- **Published**: "Difference-in-differences (DID) methods are among the most popular procedures practitioners adopted to conduct policy evaluation with observational data."
- **Analysis**: Two sentences compressed to one. The generic motivation (researchers care about causal effects, RCTs are gold standard) is eliminated entirely. The published version assumes the reader already knows why causal inference matters and jumps straight to DID. This reflects the shift from a general audience (working paper) to a specialized one (Journal of Econometrics).

### Example 2: Double robustness description
- **v1**: "one can combine them to form doubly robust DID (DR DID) estimators for the ATT that are consistent if either (but not necessarily both) the regression model for the outcome dynamics, or the propensity score model for the treatment selection is correctly specified."
- **Published**: "We contribute to the DID literature in different fronts. First, we derive doubly robust (DR) estimands for the ATT under DID settings and propose DR DID estimators for the ATT that are consistent when either a working (parametric) model for the propensity score or a working (parametric) model for the outcome evolution for the comparison group is correctly specified."
- **Analysis**: The published version is more precise: it says "working (parametric) model" instead of just "model," signals that misspecification is expected, and specifies "outcome evolution for the comparison group" rather than the vaguer "outcome dynamics." The framing shifts from "one can combine" (describing a possibility) to "We derive... and propose" (claiming a contribution).

### Example 3: The "working models" addition
- **v1**: "a propensity score model or outcome regression models are correctly specified"
- **Published**: "a propensity score or outcome regression working models are correctly specified"
- **Analysis**: The word "working" is a crucial addition. In the semiparametric inference literature, "working model" specifically denotes a model that may be misspecified but is used for estimation. This single word adds technical precision that signals the paper's engagement with the DR literature.

### Example 4: New efficiency contribution
- **v1**: [No corresponding content]
- **Published**: "Second, we derive the semiparametric efficiency bounds for the ATT under DID designs. The semiparametric efficiency bounds we derive are nonparametric in the sense that we do not assume researchers have additional knowledge about outcome regressions or the propensity score functional forms. As so, these bounds provide a standard against which one can compare the efficiency of any (regular) semiparametric DID estimator for the ATT."
- **Analysis**: This is entirely new content. The phrase "As so" is a distinctive Sant'Anna stylistic marker (also seen in paper 07). The passage demonstrates the published version's expansion from a single-contribution paper (DR estimators) to a multi-contribution paper (DR estimators + efficiency bounds + DR inference).

### Example 5: Software announcement
- **v1**: No mention of software.
- **Published**: "Finally, all proposed policy evaluation tools discussed in this article can be implemented via the open-source R package DRDID, which is freely available from GitHub (https://pedrohcgs.github.io/DRDID/)."
- **Analysis**: The addition of software reflects a broader trend in Sant'Anna's work toward making methods practically accessible. The DRDID package became one of the most-used DID packages in applied economics. This addition signals that the paper is not just a theoretical contribution but a practical toolkit -- a framing choice that likely contributed to the paper's high citation count.
