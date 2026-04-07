# Writing Style Analysis: Specification Tests for the Propensity Score

## Paper Info
- Authors: Pedro H. C. Sant'Anna, Xiaojun Song
- ArXiv v1 date: November 18, 2016 (arXiv:1611.06217v1)
- Published: Journal of Econometrics, 2019, 210(2), 379-404

## Abstract Comparison
### v1 Abstract
"This paper introduces new nonparametric diagnostic tools for detecting propensity score misspecification. These tests may be applied to assess the validity of different treatment effects estimators that rely on the correct specification of the propensity score. Our tests do not suffer from the 'curse of dimensionality' when the vector of covariates is of high-dimensionality, are fully data-driven, do not require tuning parameters such as bandwidths, and are able to detect a broad class of local alternatives converging to the null at the parametric rate n^{-1/2}, with n the sample size. We show that the use of an orthogonal projection on the tangent space of nuisance parameters both improves power and facilitates the simulation of critical values by means of a multiplier bootstrap procedure. The finite sample performance of the tests are examined by means of a Monte Carlo experiment and an empirical application. Open-source software is available for implementing the proposed tests."

### Final Abstract
"This paper proposes new nonparametric diagnostic tools to assess the asymptotic validity of different treatment effects estimators that rely on the correct specification of the propensity score. We derive a particular restriction relating the propensity score distribution of treated and control groups, and develop specification tests based upon it. The resulting tests do not suffer from the 'curse of dimensionality' when the vector of covariates is high-dimensional, are fully data-driven, do not require tuning parameters such as bandwidths, and are able to detect a broad class of local alternatives converging to the null at the parametric rate n^{-1/2}, with n the sample size. We show that the use of an orthogonal projection on the tangent space of nuisance parameters facilitates the simulation of critical values by means of a multiplier bootstrap procedure, and can lead to power gains. The finite sample performance of the tests is examined by means of a Monte Carlo experiment and an empirical application. Open-source software is available for implementing the proposed tests."

### Changes Analysis
The abstract underwent significant revision reflecting a fundamental reframing of the paper's contribution:

1. **"introduces" to "proposes"**: A subtle but meaningful shift. "Introduces" implies presenting something for the first time; "proposes" is more standard in econometrics and implies offering something for consideration.

2. **"for detecting propensity score misspecification" to "to assess the asymptotic validity of..."**: The published version frames the tests' purpose more precisely in terms of what they enable (assessing estimator validity) rather than what they detect (misspecification).

3. **New sentence about the restriction**: The published abstract adds "We derive a particular restriction relating the propensity score distribution of treated and control groups, and develop specification tests based upon it." This reflects a major reframing where the paper's foundation shifted from the balancing property characterization to a CDF-based restriction between treated and control groups.

4. **"is of high-dimensionality" to "is high-dimensional"**: A small grammatical tightening, removing the unnecessarily noun-heavy construction.

5. **Reordering of power and bootstrap claims**: v1 says "both improves power and facilitates the simulation of critical values"; published version separates these: "facilitates the simulation of critical values...and can lead to power gains." The hedge "can lead to" replaces the stronger "improves", reflecting more cautious claims about power improvements.

6. **Grammar fix**: "The finite sample performance of the tests are" (v1, incorrect) to "The finite sample performance of the tests is" (published, correct subject-verb agreement).

## Introduction Comparison
### Key Changes
The introduction was substantially rewritten between versions:

1. **Reframing of the testing approach**: The v1 introduction is built around the balancing property of the propensity score (D independent of X given p(X)), testing via the conditional moment restriction E[D - q(X, theta_0) | q(X, theta_0)] = 0. The published version shifts to a CDF-based restriction from Lemma 1: comparing propensity score distributions between treated and control groups. This is a fundamental change in the paper's conceptual foundation, likely driven by referee feedback ("We thank an anonymous referee for making this suggestion" appears in the published version).

2. **Addition of potential outcomes framework**: The published Section 2.1 adds explicit discussion of ATE, ATT, potential outcomes Y(1), Y(0), and the unconfoundedness framework. The v1 version jumps directly into the testing problem without this motivating context.

3. **Overlap discussion**: The published version adds a substantial paragraph about propensity score overlap, connecting the testing problem to practical issues of comparing treated and control distributions. This makes the paper more applied-researcher-friendly.

4. **Literature positioning**: The published version adds a paragraph on projection-based specification tests (Escanciano 2009b, Escanciano and Goh 2014), better positioning the paper within the broader specification testing literature.

5. **Softer claims about balancing tests**: v1 says balancing tests "tend to have severe size distortions"; published says they "may have size distortions" -- a notable softening, and the published version adds "poor covariate overlap" as an additional source of problems.

6. **Keyword reordering**: v1 lists "Goodness-of-fit" first; published leads with "Empirical Processes" and adds "Projection" as a keyword while removing "Goodness-of-fit".

## Conclusion/Discussion Comparison
### Key Changes
Neither version has a formal conclusion section visible in the extracted text. The paper structure ends with mathematical proofs in the appendix.

## Writing Style Patterns Observed
- **Sentence Structure**: The published version shows more complex but clearer sentence constructions. Sentences are better organized around a single main point rather than listing multiple properties.
- **Vocabulary/Terminology**: The shift from "introduces" to "proposes" and from "detecting misspecification" to "assess the validity" reflects more mature, measured academic language. "High-dimensionality" (noun) becomes "high-dimensional" (adjective).
- **Framing/Motivation**: The published version adds significant applied motivation (potential outcomes, ATE, ATT, overlap) that was absent from v1. The paper's foundation shifted from a purely statistical characterization (balancing property) to a more econometrically motivated one (CDF comparison).
- **Precision**: Power claims are hedged more carefully ("can lead to power gains" vs. "improves power"). Size distortion claims are softened from "severe" to acknowledging they "may" occur.
- **Tone**: The published version is more cautious and precise, reflecting the refinement that comes from the peer review process. Claims are qualified rather than presented as absolute.
- **Conciseness**: The abstract is slightly longer in the published version due to the added sentence about the CDF restriction, but individual sentences are tighter.
- **Reader Engagement**: The published version is considerably more accessible to applied researchers by motivating the testing problem through potential outcomes and treatment effect estimation.

## Specific Revision Examples

1. **Before (v1):** "This paper introduces new nonparametric diagnostic tools for detecting propensity score misspecification."
   **After (published):** "This paper proposes new nonparametric diagnostic tools to assess the asymptotic validity of different treatment effects estimators that rely on the correct specification of the propensity score."
   **Why:** The published framing connects the tests directly to what applied researchers care about (validity of treatment effect estimators), rather than the more abstract goal of "detecting misspecification." Adding "asymptotic" also adds precision about the nature of the validity being assessed.

2. **Before (v1):** "both improves power and facilitates the simulation of critical values"
   **After (published):** "facilitates the simulation of critical values by means of a multiplier bootstrap procedure, and can lead to power gains"
   **Why:** The v1 claim that projections "improve power" is too strong without qualification. The published version hedges appropriately with "can lead to" and also reorders to emphasize the practical benefit (easier bootstrap) before the theoretical one (power gains).

3. **Before (v1):** "conditioning on the true (unknown) propensity score, the treatment assignment is independent of the covariates (Rosenbaum and Rubin, 1983) our tests do not suffer from the 'curse of dimensionality'"
   **After (published):** "We derive a particular restriction relating the propensity score distribution of treated and control groups, and develop specification tests based upon it."
   **Why:** This represents the fundamental reframing of the paper. Rather than building on the abstract balancing property, the published version builds on a concrete, interpretable restriction between CDFs. This makes the paper's contribution more tangible and the testing approach more intuitive.

4. **Before (v1):** "One should bare in mind that because 'balancing score' tests are usually based on a finite number of orthogonality conditions, there are uncountably many misspecification that cannot be detected with these tests."
   **After (published):** "One should bear in mind that because 'balancing' tests are usually based on a finite number of orthogonality conditions, there are uncountably many directions of misspecification that cannot be detected with these tests."
   **Why:** Spelling correction ("bare" to "bear"), and the addition of "directions of" before "misspecification" makes the claim more precise -- it is not just that misspecifications exist, but that there are directions of departure from the null that these tests miss.

5. **Before (v1):** [Section 2.1 begins directly with testing framework, no potential outcomes]
   **After (published):** [Section 2.1 adds potential outcomes Y(1), Y(0), defines ATE and ATT, discusses unconfoundedness, and motivates propensity score testing through IPW estimation]
   **Why:** The published version provides applied researchers with the full context for why propensity score specification matters. By grounding the testing problem in treatment effect estimation, the paper becomes relevant to a much broader audience rather than only specification testing specialists.
