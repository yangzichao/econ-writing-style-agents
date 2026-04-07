# Writing Style Analysis: When Is Parallel Trends Sensitive to Functional Form?

## Paper Info
- Authors: Jonathan Roth, Pedro H.C. Sant'Anna
- ArXiv v1 date: October 9, 2020
- Published: Econometrica, Vol. 91, No. 2, March 2023

## Abstract Comparison

### v1 Abstract
"This paper assesses when the validity of difference-in-differences and related estimators is dependent on functional form. We provide a novel characterization: the parallel trends assumption holds under all monotonic transformations of the outcome if and only if a stronger 'parallel trends'-type assumption holds on the entire distribution of potential outcomes. This assumption necessarily holds when treatment is (as if) randomly assigned, but will often be implausible in settings where randomization fails. We show further that the average treatment effect on the treated (ATT) is identified regardless of functional form if and only if the entire distribution of untreated outcomes is identified for the treated group. It is thus impossible to construct an estimator that is consistent (or unbiased) for the ATT regardless of functional form unless one imposes assumptions that identify the entire counterfactual distribution of untreated potential outcomes. Our results suggest that researchers who wish to point-identify the ATT should justify one of the following: (i) why treatment is randomly assigned, (ii) why the chosen functional form is correct at the exclusion of others, or (iii) a method for inferring the entire counterfactual distribution of untreated potential outcomes."

### Final Abstract
"This paper assesses when the validity of difference-in-differences depends on functional form. We provide a novel characterization: the parallel trends assumption holds under all strictly monotonic transformations of the outcome if and only if a stronger 'parallel trends'-type condition holds for the cumulative distribution function of untreated potential outcomes. This condition for parallel trends to be insensitive to functional form is satisfied if and essentially only if the population can be partitioned into a subgroup for which treatment is effectively randomly assigned and a remaining subgroup for which the distribution of untreated potential outcomes is stable over time. These conditions have testable implications, and we introduce falsification tests for the null that parallel trends is insensitive to functional form."

### Changes Analysis
The abstract underwent a dramatic condensation and reframing:

1. **Length reduction**: The v1 abstract is approximately 170 words; the final is approximately 100 words -- a 40% reduction. Econometrica's format demands extreme conciseness, but the stylistic choices in what was cut reveal priorities.

2. **Scope narrowing**: The v1 abstract covered two main results (invariance characterization + ATT identification equivalence) plus a three-part practitioner recommendation. The final abstract drops the second result entirely (ATT identification equivalence) and the practitioner-facing recommendations, focusing solely on the characterization result plus the new falsification tests.

3. **Language precision**: "dependent on functional form" became "depends on functional form" (simpler). "Monotonic" became "strictly monotonic" (more precise). "Assumption holds on the entire distribution" became "condition holds for the cumulative distribution function" (more specific and technical).

4. **Framing shift**: The v1 abstract ends with a practitioner-oriented prescription ("researchers who wish to point-identify the ATT should justify one of the following..."). The final abstract instead highlights testable implications and falsification tests -- shifting from advisory to methodological contribution.

5. **New content**: The final abstract introduces the falsification tests, which were not mentioned in the v1 abstract. The phrase "if and essentially only if" is a careful hedge added in the published version, acknowledging an edge case discussed in Remark 2 of the published paper.

6. **Keyword addition**: The published version includes formal keywords ("Difference-in-differences, functional form, robustness, testable implications") not present in the working paper.

## Introduction Comparison

### Key Changes
The introduction was fundamentally restructured between v1 and the published version:

1. **Dramatic compression**: The v1 introduction spans approximately 3.5 pages with detailed discussion of both main results and extensive literature contextualization. The published introduction is approximately 1 page -- a radical reduction demanded by Econometrica's short-paper format.

2. **Motivation sharpening**: The v1 opens with a broad statement about DiD's popularity in social sciences before narrowing to functional form. The published version cuts straight to the core question: "THIS PAPER STUDIES WHEN THE PARALLEL TRENDS ASSUMPTION USED for identification in difference-in-differences (DiD) designs is insensitive to functional form." The motivation paragraph is tighter, using a single concrete example (state-level policy variation and whether parallel trends holds in levels vs. logs) rather than the v1's longer list of earnings transformations.

3. **Contribution restructuring**: The v1 describes two main results at length with extensive caveats. The published version states contributions as a compact numbered list: "We provide two characterizations..." followed by the testable implications and empirical illustration.

4. **Literature positioning trimmed**: The v1 devotes two full paragraphs to positioning relative to prior work (Athey and Imbens 2006, Bonhomme and Sauder 2011, Callaway and Li 2019, Meyer 1995, Kahn-Lang and Lang 2018). The published version compresses this to a single brief paragraph, deferring detailed comparisons to remarks within the body.

5. **Practitioner guidance removed from intro**: The v1 introduction contains a full paragraph of practical implications ("researchers interested in point-identifying the ATT must make one of the following three justifications"). This is moved to a dedicated Section 4 ("Implications for Applied Work") in the published version.

6. **Tone shift**: The v1 reads more like a working paper with exploratory framing ("We will say that..."). The published version is more assertive and direct ("We show that...").

## Conclusion/Discussion Comparison

### Key Changes
The v1 paper does not have a formal conclusion section; the paper transitions from main results directly to remarks and appendix. The published version adds a dedicated Section 4 ("Implications for Applied Work") that serves as a conclusion. This section:

1. **Synthesizes practical guidance**: Offers a clear three-option framework for researchers: (a) argue for random assignment, (b) impose distributional assumptions that pin down the full counterfactual distribution, or (c) use context-specific knowledge to justify a particular functional form.

2. **Is more direct**: Uses confident, clear language: "Our hope is that the results in this paper will be useful in providing researchers with a menu of options for more clearly delineating the justification for their research design."

3. **Adds new material**: Includes a subsection on "Extensions" covering other classes of functions, other estimators, and use of pre-treatment periods -- material that was distributed across Remarks in the v1.

4. **References the working paper**: The published version explicitly references the working paper for results that were cut from the main text ("We showed in the working paper version of this article that..."), maintaining a trail to the fuller results.

## Writing Style Patterns Observed

- **Sentence Structure**: Sentences became shorter and more direct. Complex compound sentences with multiple qualifications were broken apart or simplified. The v1 frequently uses parenthetical asides; the published version removes many of these.

- **Vocabulary/Terminology**: The published version standardizes terminology. "Invariant to transformations" and "insensitive to functional form" are used as explicit synonyms (Definition 1 adds "a.k.a. insensitive to functional form"). "Assumption" in the abstract becomes "condition" -- a subtle but meaningful distinction, as "condition" suggests something to be verified rather than imposed.

- **Framing/Motivation**: Shifted from a dual-contribution framing (characterization + identification equivalence) to a single sharper contribution (characterization + testable implications). The paper's identity changed from "here are two theoretical results" to "here is one clean result with practical implications."

- **Precision**: Mathematical statements became more precise. "Monotonic" became "strictly monotonic." The Radon-Nikodym density condition in Proposition 3.2 was strengthened from "absolutely continuous with respect to some dominating sigma-finite measure" to "have a Radon-Nikodym density with respect to a common dominating, positive sigma-finite measure."

- **Tone**: Shifted from exploratory/comprehensive to authoritative/concise. The v1 reads like a thorough working paper; the published version reads like a polished short communication.

- **Conciseness**: The paper went from 28 pages to 12 pages (including references and appendix). This required cutting the second main result (Proposition 4.1 on ATT identification), several remarks, and extensive discussion. The trade-off was adding new material (falsification tests, empirical illustration).

- **Reader Engagement**: The published version adds concrete examples (normally distributed outcomes, mixtures of distributions with a figure and table, minimum wage empirical illustration) that make abstract results tangible. The v1 is heavier on remarks and lighter on examples.

## Specific Revision Examples

### Example 1: Opening sentence of the paper
**v1**: "Difference-in-difference (DiD) is one of the most popular strategies in the social sciences for estimating causal effects in non-experimental contexts."
**Final**: "THIS PAPER STUDIES WHEN THE PARALLEL TRENDS ASSUMPTION USED for identification in difference-in-differences (DiD) designs is insensitive to functional form."
**Analysis**: The v1 opens with a general statement about DiD's popularity -- a common but generic opening. The published version eliminates the throat-clearing and immediately states the paper's question. This reflects a broader pattern of removing warm-up text in favor of direct engagement with the research question.

### Example 2: Description of the three cases
**v1**: "Case 1: Random assignment... Case 2: No time trends... Case 3: Time trends and non-random assignment." (Each case gets its own paragraph with full discussion)
**Final**: "Case 1: Random Assignment. (theta = 1)... Case 2: Stationary Y(0). (theta = 0)... Case 3: Nonrandom Assignment and Nonstationarity. (theta in (0,1))." (Compact with theta parameter values in parentheses)
**Analysis**: The published version tightens the case descriptions by immediately linking each to the parameter value, making the taxonomy both more formal and more memorable. "No time trends" became "Stationary Y(0)" -- more precise econometric language. The detailed intuitive discussion in v1's Case 3 was compressed.

### Example 3: Correction of prior literature claim
**v1 (Remark 10)**: "It has previously been stated that for the parallel trends assumption in levels to be compatible with the parallel trends assumption in logs, it is necessary for the distribution of baseline outcomes to be the same..." (followed by a lengthy quote from Kahn-Lang and Lang 2018 and detailed discussion)
**Final**: This entire remark was removed from the main text. The relationship to prior claims is briefly noted in the introduction ("we provide the first full characterization") and the working paper version is cited for details.
**Analysis**: Removing the direct engagement with (and correction of) a specific prior claim reflects a shift toward a more self-contained, forward-looking presentation. Rather than positioning the paper against prior misconceptions, the published version simply states its contribution.

### Example 4: Addition of falsification tests and empirical illustration
**v1**: Remark 6 briefly mentions "it is possible to test whether the integrated curve C(y) is concave" but provides no implementation details or application.
**Final**: Adds a full subsection (3.2) on "Testable Implications of Invariance to Transformations" with formal statistical testing procedures, moment inequality methods, and a complete empirical illustration using minimum wage data from Cengiz et al. (2019) with figures.
**Analysis**: This is the most substantial addition in the revision. It transforms the paper from a purely theoretical contribution into one with applied relevance. The addition likely reflects referee suggestions to make the results more actionable.

### Example 5: Hedge language ("essentially only if")
**v1**: States the characterization as "if and only if" without qualification.
**Final**: Uses "if and essentially only if" in the abstract and adds Remark 2 explaining: "In principle, though, it is possible for the units in the theta and 1-theta partitions to change across periods in Case 3, although it is difficult to imagine scenarios where this would be the case in practice."
**Analysis**: This added hedging reflects careful engagement with referee concerns about the exact logical status of the characterization. It demonstrates increased precision -- the authors distinguish between mathematical possibility and practical plausibility, and they do so transparently.
