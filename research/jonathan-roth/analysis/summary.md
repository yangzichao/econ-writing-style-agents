# Jonathan Roth - Writing Style Analysis Summary

Synthesis of key writing style patterns found across Roth's papers, based on ArXiv version comparisons and published outputs.

---

## Abstract Patterns

Comparison of v1 (initial ArXiv submission) versus published/latest version for papers with available revision history.

### 1. Logs with Zeros (v1 to v7)

- **v1**: Technical opening, explains the math directly (e.g., uses notation like theta_g = E[g(Y(1),Y(0))]), relies on "we show" / "we first show" phrasing.
- **v7**: Restructured around a named impossibility result -- the "trilemma" concept. More concise overall. Adds "three empirical applications" to signal practical relevance. Shifts to "We argue" / "We further establish" as framing verbs.
- **Key pattern**: Named impossibility result ("trilemma") introduced during revision. This is a distinctive Roth move -- giving a memorable label to a negative result, then offering a menu of alternatives.

### 2. Pretest with Caution (v1 to published)

- **Title change**: "Should We Condition on the Test for Pre-trends in Difference-in-Difference Designs?" became "Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends"
- **v1 abstract**: Long, technical, walks through multiple cases (valid/invalid DiD, monotone trends), proposes specific estimators.
- **Published abstract**: Short, two-bullet structure ("First...Second..."), high-level framing, ends with "practical recommendations."
- **Key pattern**: Massive simplification. Moves from technical detail to an accessible problem statement. The title shift from a question to an imperative ("Pretest with Caution") is also notable.

### 3. Design-Based Uncertainty (v1 to v8)

- **v1**: Opens with "Social scientists are often interested in..." (throat-clearing), focuses on the SDIM estimator, DiD, 2SLS as specific applications.
- **v8**: Opens with "Design-based frameworks of uncertainty are frequently used..." (field-centric framing), pivots to sensitivity analysis and "rich forms of selection."
- **Key pattern**: Reframed from a descriptive/methodological paper to one centered on sensitivity analysis. The opening shifts from generic motivation to situating the paper within an existing literature.

### 4. Testing Mechanisms (v1 to v3)

- **v1**: Long abstract, explains the LATE connection in detail, includes "Existing tools for testing the validity of the LATE assumptions can thus be used."
- **v3**: Compressed, uses "Our approach exploits connections between mediation analysis and the econometric literature on testing instrument validity."
- **Key pattern**: More concise; detailed methodology removed from abstract. The verb "exploits connections" is tighter than the v1 phrasing.

### 5. Inference for Linear Conditional Moment Inequalities (v1 to v5)

- **v1**: "We consider inference based on..." opening -- describes what the paper does.
- **v5**: "We show that moment inequalities in a wide variety of economic applications have a particular linear conditional structure" -- opens with the contribution.
- **Key pattern**: Reframes from "we consider" (process-oriented) to "we show" (result-oriented). This is a common maturation pattern across Roth's revisions.

### 6. Staggered Rollout (with Sant'Anna, v1 to published)

- Opening changed from "Researchers are often interested in" to "We study estimation of causal effects in staggered rollout designs."
- Abstract cut from approximately 170 words to approximately 90 words (47% reduction).
- Self-promotion removed ("most precise estimates to date").
- Empirical claim updated: "five times" became "eight times."
- **Key pattern**: Throat-clearing removed, self-promotional language cut, quantitative claims updated with stronger results.

### 7. Parallel Trends Functional Form (with Sant'Anna, v1 to published)

- Abstract cut from approximately 170 words to approximately 100 words (41% reduction).
- Precision increased: "monotonic" became "strictly monotonic."
- Falsification tests added as a contribution.
- Three-option menu structure maintained across versions.
- **Key pattern**: Tightening and precision gains. The menu-of-options structure is stable from the start -- this is a core Roth framing device.

---

## Introduction Patterns

### Opening moves
- Opens by identifying a common empirical practice, then reveals a hidden problem with that practice. This "critique-then-construct" pattern is Roth's signature move.
- Quantified empirical surveys appear early: references like "70 papers" or "over 30% of NBER papers" establish that the problem is widespread and practically important.
- Concrete examples are introduced very early in the introduction, before the formal contribution statement.

### Contribution enumeration
- Contributions are enumerated, but the style is less formulaic than Sant'Anna's. Roth tends to weave contributions into the narrative rather than presenting a rigid numbered list.
- Contributions often take the form: (1) identify problem / impossibility, (2) propose sensitivity analysis or menu of solutions, (3) apply to empirical example(s).

### Related literature
- Formal "Related Literature" subsection is standard, typically appearing at the end of the introduction.

### Software announcements
- Software packages are announced in the introduction (HonestDiD, pretrends, staggered), signaling practical relevance and uptake.

---

## Key Style Differences from Sant'Anna

| Dimension | Roth | Sant'Anna |
|-----------|------|-----------|
| Title style | Question titles ("Logs with zeros?", "When Is Parallel Trends Sensitive?") | Declarative titles |
| Framing | Critique-then-construct (reveal problem, then offer solutions) | Solution-first (here is a better method) |
| Impossibility results | Named impossibility results ("trilemma") | Less emphasis on impossibility |
| Solution structure | Menu of alternatives after impossibility | Single recommended approach |
| Philosophical commitment | Sensitivity analysis as core value | Point identification and efficiency |
| Empirical evidence | More concrete quantified surveys of practice | Less emphasis on surveying practice |
| Practical guidance | Dedicated "practical recommendations" sections | Guidance embedded in exposition |
| Abstract length trajectory | Significant compression across versions | Significant compression across versions (shared) |
| Throat-clearing removal | Consistent removal across versions | Consistent removal across versions (shared) |

---

## Distinctive Phrases

Recurring phrases that characterize Roth's writing voice:

- **"hidden assumptions"** -- used to frame the critique of standard practice
- **"sensitivity analysis"** -- core methodological commitment, appears across most papers
- **"credible" / "credibility"** -- evaluative standard for empirical work
- **"trilemma"** -- named impossibility result (Logs with Zeros)
- **"menu of options"** -- framing device for presenting multiple solutions after impossibility
- **"practical recommendations"** -- signals applied relevance, often a dedicated section
- **"common practice"** -- sets up the critique by establishing what researchers typically do
- **"pre-trends"** -- domain-specific terminology, central to multiple papers

---

## Revision Patterns Summary

Across all papers with multiple ArXiv versions, the following revision patterns emerge:

1. **Abstract compression**: Abstracts shrink substantially (40-50% word reduction is typical).
2. **Throat-clearing removal**: Generic openings ("Researchers are often interested in...") are replaced with direct statements of contribution.
3. **Verb strengthening**: "We consider" becomes "We show"; "we first show" becomes "We argue."
4. **Named results**: Key impossibility or characterization results acquire memorable names during revision.
5. **Empirical claims update**: Quantitative results are updated as analysis improves (e.g., "five times" to "eight times").
6. **Self-promotion removal**: Claims like "most precise estimates to date" are cut.
7. **Practical framing added**: Later versions emphasize empirical applications and practical recommendations more heavily.
