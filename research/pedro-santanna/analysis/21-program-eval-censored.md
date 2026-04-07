# Writing Style Analysis: Program Evaluation with Right-Censored Data

## Paper Info
- Authors: Pedro H. C. Sant'Anna (sole author)
- ArXiv v1 date: April 10, 2016 (first version November 10, 2015)
- Published/Status: Working paper (only v1 available)

## Abstract (v1 only)
"In a unified framework, we provide estimators and confidence bands for a variety of treatment effects when the outcome of interest, typically a duration, is subjected to right censoring. Our methodology accommodates average, distributional, and quantile treatment effects under different identifying assumptions including unconfoundedness, local treatment effects, and nonlinear differences-in-differences. The proposed estimators are easy to implement, have close-form representation, are fully data-driven upon estimation of nuisance parameters, and do not rely on parametric distributional assumptions, shape restrictions, or on restricting the potential treatment effect heterogeneity across different subpopulations. These treatment effects results are obtained as a consequence of more general results on two-step Kaplan-Meier estimators that are of independent interest: we provide conditions for applying (i) uniform law of large numbers, (ii) functional central limit theorems, and (iii) we prove the validity of the ordinary nonparametric bootstrap in a two-step estimation procedure where the outcome of interest may be randomly censored."

## Introduction Analysis
### Writing Style
This is an early-career paper by Sant'Anna (dated 2015-2016, when he was at Vanderbilt University), and the writing style reveals interesting contrasts with his later work:

1. **Opening**: "Assessing whether a policy has any effect on a particular outcome has been one of the main concerns in empirical research." This generic, textbook-style opening is very different from the specific, data-grounded openings of later papers (e.g., "over 30% of NBER papers mention DiD").

2. **Passive constructions**: "As summarized in Heckman and Vytlacil (2007) and Imbens and Wooldridge (2009), the focus of the policy evaluation literature has been mainly confined to situations where..." This passive, deferential tone -- pointing to authorities before stating the gap -- contrasts with the more assertive "This paper shows/proposes" style of later work.

3. **Mathematical framing first**: The introduction quickly moves to a mathematical formulation: "many treatment effect measures commonly used can be written as (smooth) functions of moment equations of the type E[phi_{z,h_0}(Y,X,T)]". This "math-first" approach is more typical of statistics papers than of the applied-econometrics bridging style Sant'Anna develops later.

4. **"Motivating Examples" structure**: Section 2 is titled "Motivating Examples" -- a format borrowed from statistics journals. Later papers tend to call this "Framework" or "Setup."

5. **Contribution enumeration**: "The proposed estimators are easy to implement, have close-form representation, are fully data-driven upon estimation of nuisance parameters, and do not rely on parametric distributional assumptions, shape restrictions, or on restricting the potential treatment effect heterogeneity across different subpopulations." This long, comma-separated list of virtues is characteristic but more compactly rendered in later work.

6. **Technical emphasis**: The paper frames its contribution primarily in terms of mathematical generality: "To the best of our knowledge, this paper is the first to propose such broad policy evaluation tools for right-censored outcomes without relying on parametric assumptions or shape restrictions." Later papers frame contributions more in terms of practical impact.

## Writing Style Patterns Observed
- **Sentence Structure**: Longer sentences with more subordinate clauses than later papers. The mathematical notation is integrated into prose early and frequently. Some sentences are quite dense: "Nonetheless, these maintained assumptions are stronger than assuming that, conditionally on X and T, Y is independent of C, and may be violated in some applications."
- **Vocabulary/Terminology**: More statistics-oriented vocabulary ("Glivenko-Cantelli," "Donsker class," "tight Gaussian process," "Banach space") than the causal-inference-centered vocabulary of later papers. This reflects the paper's positioning at the intersection of survival analysis and program evaluation.
- **Framing/Motivation**: The motivation is abstract and literature-gap-oriented rather than empirically motivated. No specific policy application is mentioned in the introduction (only general categories: "unemployment," "recidivism," "clinical therapy"). Later papers lead with concrete empirical contexts.
- **Precision**: Very high mathematical precision, arguably even more than later papers. Every object is formally defined with full notation.
- **Tone**: More formal and impersonal than later work. Uses "one" instead of "we" in places: "one consistently estimate h_0." The first person is used sparingly. The acknowledgments note: "I gratefully acknowledge research support" -- single-author voice.
- **Conciseness**: The paper is dense but complete. The introduction efficiently sets up the framework without extensive motivation or literature review.
- **Reader Engagement**: Limited compared to later papers. No rhetorical questions, no empirical hooks, no quantified practical gains. The paper speaks primarily to a technical audience.

## Specific Style Features (Early Career Markers)

1. **Generic opening vs. later specific openings**:
   - This paper: "Assessing whether a policy has any effect on a particular outcome has been one of the main concerns in empirical research."
   - Later style (e.g., paper 16): "Difference-in-Differences (DiD) and Event Study (ES) designs are among the most widely used empirical strategies in economics and related fields. For instance, recent data indicates that over 30% of 2024 NBER applied microeconomics working papers mention DiD or ES."
   - The evolution shows a shift from generic motivations to specific, data-backed claims.

2. **Deference to authorities vs. later confident positioning**:
   - This paper: "As summarized in Heckman and Vytlacil (2007) and Imbens and Wooldridge (2009), the focus of the policy evaluation literature has been mainly confined to..."
   - Later style: "Although recent methodological advances have improved the robustness of DiD estimators to treatment effect heterogeneity, several empirically relevant econometric questions remain underexplored."
   - The later style acknowledges the literature but positions the paper's contribution more assertively.

3. **Mathematical objects in prose**:
   - This paper frequently embeds full equations in running text: "moment equations of the type E[phi_{z,h_0}(Y,X,T)] = integral..."
   - Later papers tend to separate equations from the prose more cleanly, using displayed math and explaining intuition in words first.

4. **Statistics vs. econometrics framing**:
   - This paper: "we provide conditions for applying (i) uniform law of large numbers, (ii) functional central limit theorems, and (iii) we prove the validity of the ordinary nonparametric bootstrap."
   - This framing speaks to statisticians. Later papers frame contributions more in terms of causal parameters and identification, speaking to empirical economists.

5. **R codes offered in footnote**: "R codes for implementing the treatment effects estimators are available from the author." This early form of software provision evolves into full R packages (like "triplediff" in paper 17, "did" in other work) with formal announcements in later papers -- reflecting both the growth of the open-source norm and Sant'Anna's increasing emphasis on practical implementation.
