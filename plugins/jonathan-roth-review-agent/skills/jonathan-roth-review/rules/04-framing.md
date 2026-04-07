# Framing and Motivation Rules

These rules encode Jonathan Roth's framing and motivation patterns, derived from comparing first drafts to published versions across his papers.

## Pattern 1: Critique-then-Construct

Roth's papers follow a consistent two-part structure: first identify a problem in common practice, then build a solution. This differs from a solution-first framing (where the new method is presented and then compared to alternatives). The critique must come first because it motivates the reader to care about the solution.

**The structure:**
1. Describe the common practice (what applied researchers do)
2. Reveal the limitation or hidden assumption (why that practice is flawed)
3. Offer a constructive alternative (what researchers should do instead)

**Good examples:**
- Pre-test: Highlights pretesting limitations, then proposes adjusted procedures
- Logs: Shows log-like transformations are problematic, then offers three alternatives
- Honest DiD: Shows parallel trends may not be credible, then develops sensitivity analysis
- Design-Based: Shows sampling-based uncertainty is inappropriate, then develops design-based framework

**Check:** Does the paper lead with the problem or with the solution? If the paper opens by presenting a new estimator/test without first establishing why existing approaches are inadequate, suggest reordering to critique-then-construct. The reader needs to feel the pain before accepting the medicine.

## Pattern 2: Named Impossibility Results

When proving a negative result, give it a memorable label. Named results are cited more, remembered longer, and serve as anchors for the literature that follows.

**Good examples:**
- "Trilemma" (Logs) — three desirable properties (average of individual effects, unit-invariance, point-identification) that cannot all hold simultaneously when the outcome can equal zero
- "Sharp null of full mediation" (Testing Mechanisms) — a specific hypothesis that can be tested
- Three-option menu (Parallel Trends Functional Form) — researchers must justify exactly one of three conditions

**Requirements for a good name:**
- Descriptive: the name should hint at the content (e.g., "trilemma" implies three incompatible things)
- Concise: one or two words
- Memorable: a reader should be able to recall the result from the name alone

**Check:** If the paper proves that something is impossible, unavoidable, or inherently limited, does it have a name? If the impossibility result is described only in prose without a label, suggest naming it. Even a structured enumeration ("three properties that cannot all hold") is better than an unnamed negative result.

## Pattern 3: Menu of Alternatives

After proving an impossibility or limitation, present a structured set of alternatives using numbered lists. The "menu" framing transforms a negative result into constructive guidance. The reader should leave the paper knowing exactly what their options are.

**Good examples:**
- Logs: "(i) expressing the ATE in levels as a percentage (e.g. using Poisson regression), (ii) explicitly calibrating the value placed on intensive and extensive margins, and (iii) estimating separate effects for the two margins"
- Parallel Trends Functional Form: "(i) why treatment is randomly assigned, (ii) why the chosen functional form is correct, or (iii) a method for inferring the entire counterfactual distribution"

**Formatting requirements:**
- Use (i), (ii), (iii) numbering (not bullets, not 1/2/3)
- Each item should be a self-contained description of one option
- The list should be exhaustive — the reader should not feel that options were omitted

**Check:** After each negative result, is there a clearly enumerated menu of alternatives? If the paper says "researchers should consider other approaches" without listing them, flag this as incomplete. The alternatives must be specific and actionable.

## Pattern 4: Sensitivity Analysis Framing

Frame contributions as tools for assessing sensitivity rather than as definitive solutions. This is honest about what methodology can and cannot do, and it aligns with how applied researchers actually use methodological papers.

**Good examples:**
- "allows the researcher to assess the sensitivity of their conclusions to violations" (Honest DiD)
- "These results can be used to conduct sensitivity analyses when there are concerns about selection into treatment" (Design-Based)
- Provides diagnostics and calibration tools, not just fixes (Pre-test)

**Check:** Does the paper claim to "solve" a problem, or does it provide tools for assessing the problem's severity? If the former, consider whether the "sensitivity analysis" framing is more honest and more useful. Applied researchers want to know how much their conclusions depend on assumptions — they rarely want (or trust) a method that claims to eliminate all concerns.

## Pattern 5: Quantified Empirical Surveys

Ground methodological contributions in quantitative evidence about real-world practice. A count of papers, a survey of methods used, or a systematic review transforms a theoretical exercise into an urgent practical contribution.

**Good examples:**
- "my review of publications in three leading economics journals between 2014 and 2018 found 70 papers that use an 'event-study plot' to visually test for pre-trends" (Pre-test)
- "over 30% of 2024 NBER applied microeconomics working papers mention DiD or ES" (What's Trending)

**Requirements:**
- Specific journals or working paper series (not "the literature")
- Specific time period
- Specific count or percentage
- The survey should be relevant to the paper's contribution (i.e., it should measure the practice that the paper critiques or improves)

**Check:** Does the introduction include quantitative evidence about how widespread the relevant practice is? If the paper claims that a practice is "common" or "widespread" without numbers, suggest adding a brief empirical survey.

## Pattern 6: Practical Recommendations Sections

End papers (or major sections) with explicit, actionable recommendations for practitioners. These should be clearly labeled and easy to find.

**Good examples:**
- Pre-test: Section III is titled "Practical Recommendations"
- What's Trending: Boxed "Recommendations" throughout the paper
- Honest DiD: Concrete sensitivity analysis procedures with step-by-step instructions
- Logs: Enumerated alternative approaches with guidance on when to use each

**Check:** Does the paper have a clearly labeled section or subsection with practical recommendations? If the recommendations are scattered throughout the paper without a dedicated location, suggest consolidating them. A practitioner skimming the paper should be able to find the "what should I do?" section immediately.

## Pattern 7: Bridge Technical and Applied Language

Frame technical contributions in terms that practitioners understand. The applied reader should grasp the contribution's relevance without reading the proofs.

**Good examples:**
- "in a wide variety of economic applications" — leads with applicability (Moment Inequalities)
- "more closely aligns with the way empirical researchers discuss the variation in the data" — frames the advantage in the practitioner's language (Design-Based)
- "does not require stringent assumptions about how M is assigned" — frames the advantage as fewer assumptions, which applied researchers value (Testing Mechanisms)

**Check:** For each technical contribution, is there a sentence that explains why an applied researcher should care? If the contribution is described only in mathematical terms ("the estimator achieves the semiparametric efficiency bound"), add a sentence explaining the practical implication ("this means the confidence intervals will be shorter than those from existing methods").

## Pattern 8: Question Framing in Titles

Several Roth papers use question titles that the paper then answers. This framing draws the reader in and creates a natural structure: the title poses the question, the abstract answers it, and the paper proves the answer.

**Good examples:**
- "Logs with zeros? Some problems and solutions"
- "Should We Condition on the Test for Pre-trends?" (later revised to the more directive "Pretest with Caution")
- "When Is Parallel Trends Sensitive to Functional Form?"
- "What's Trending in Difference-in-Differences?"

**Note on title revision:** The Pre-test paper's title changed from a question ("Should We Condition on the Test for Pre-trends?") to a directive ("Pretest with Caution"). This reflects a general pattern: questions work well for working papers, but published versions may benefit from a more definitive framing that telegraphs the answer.

**Check:** If the paper answers a specific question that practitioners face, consider whether a question title would be effective. But also consider whether the answer is clear enough to use a directive title instead. A question title that the abstract does not answer is frustrating; a directive title that the paper does not justify is presumptuous.
