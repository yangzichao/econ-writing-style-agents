# Terminology and Voice Rules

These rules encode Jonathan Roth's terminology preferences and voice patterns, derived from comparing first drafts to published versions across his papers.

## Standard Terminology Substitutions

Apply these substitutions when reviewing. The left column shows language to flag; the right column shows the preferred replacement.

### Openings and Framing

| AVOID | USE | Rationale |
|---|---|---|
| "Social scientists are often interested in" | Specific field context (e.g., "Design-based frameworks are frequently used in settings where...") | Generic openings waste the reader's first impression |
| "Researchers are often interested in" | "We study..." or a description of the specific practice | Same: be specific about what researchers do, not that they are "interested" |
| "An important question in [field] is" | State the question directly | The reader will judge importance; do not assert it |
| "It is well known that" | State the fact directly, or cite a source | If it is well known, it does not need the preamble |

### Verbs of Contribution

| AVOID | USE | Rationale |
|---|---|---|
| "we first show" / "we show" (exploratory tone) | "We argue" / "We establish" / "We further establish" | Definitive verbs signal confidence in the result |
| "we consider inference based on" | "We show that..." | "Consider" is tentative; prefer stating the contribution directly |
| "it may be possible to" | "we develop" / "we derive" | If the paper does it, say so |
| "we investigate" | "we characterize" | "Investigate" suggests the work is incomplete; "characterize" signals a complete result |
| "we contribute to" | "This paper highlights" / "We develop" / "We establish" | Describe the contribution itself, not the act of contributing |

### Technical Terms

| AVOID | USE | Rationale |
|---|---|---|
| "DID" or "diff-in-diff" | "DiD" or "difference-in-differences" | Consistent capitalization across all Roth papers |
| "(as-if) randomly assigned" | "as-good-as randomly assigned" or "(quasi-)randomly assigned" | Roth's preferred phrasing in published work |
| "pre-treatment trends" | "pre-trends" | Roth's established shorthand, used consistently |
| "propensity score model" | "propensity score working model" | More precise; acknowledges the model may be misspecified (used in co-authored work with Sant'Anna) |
| "monotonic" | "strictly monotonic" (when strict monotonicity is required) | Precision matters; do not leave ambiguity about whether zero derivatives are allowed |
| "similar properties" | State the specific properties (e.g., "asymptotically unbiased with efficiency (weakly) dominating") | Vague comparisons obscure the actual claim |

## Precision Over Generality

Replace vague characterizations with specific ones. Every claim should be precise enough that a reader could verify it.

| VAGUE | PRECISE | Source |
|---|---|---|
| "can be hard to interpret" | State the specific reason interpretation fails | Logs |
| "there is no good parameter" | "there is no treatment effect parameter that is (i) an average of individual-level effects, (ii) unit-invariant, and (iii) point-identified" | Logs (trilemma) |
| "performs well" | State the metric and the benchmark (e.g., "empirical size close to the nominal level") | Staggered Rollout, Moment Inequalities |
| "under mild conditions" | Name or number the conditions (e.g., "under Assumptions 1–3") | Design-Based Uncertainty |
| "standard assumptions" | Name the specific assumptions (e.g., "under SUTVA and monotonicity") | Testing Mechanisms |

**Check:** Flag any sentence containing "hard to interpret," "performs well," "under mild/standard conditions," or "similar properties" and request the specific claim.

## Active Voice and Confidence

Roth's published prose uses active voice and confident verbs. The progression from draft to published consistently replaces tentative language with definitive statements.

| WEAK | STRONG | Source |
|---|---|---|
| "we consider" | "we show" / "we establish" | Moment Inequalities v1 to v5 |
| "it may be possible to" | "we develop" / "we derive" | Testing Mechanisms v1 to v3 |
| "should we adjust" (questioning) | "pretest with caution" (directive) | Pre-test title change |
| "we investigate" | "we characterize" | Design-Based v1 to v8 |
| "it seems that" | "we find that" | Design-Based v1→v8 |
| "one could potentially" | "we propose" | Testing Mechanisms v1→v3 |

### Before / After Examples

**Paper: Pre-test with Caution (ArXiv v1 → AER:I 2022) — Title change**
> WEAK: "Should We Adjust for the Test for Pre-trends in Difference-in-Difference Designs?"
>
> STRONG: "Pretest with Caution: Event-Study Estimates after Testing for Parallel Trends"

The questioning title became a directive. "Should we?" implies uncertainty; "Pretest with Caution" tells the reader what to do.

**Paper: Moment Inequalities (ArXiv v1 → REStud 2023)**
> WEAK: "We consider inference based on linear conditional moment inequalities"
>
> STRONG: "We show that moment inequalities in a wide variety of economic applications have a particular linear conditional structure"

"We consider" describes an activity; "We show" states a finding.

**Check:** Flag passive constructions ("it is shown that," "it can be seen that") and tentative verbs ("may," "might," "could potentially," "seems"). Replace with active, definitive alternatives unless the hedge is genuinely warranted (see Hedging Rules below).

## Hedging Rules

Roth hedges when the claim is genuinely conditional — not out of timidity. Hedges are appropriate only when the direction or magnitude of a result depends on parameters the researcher does not control.

**Appropriate hedges:**
- "potentially exacerbating" — the direction depends on the specific DGP
- "may have low power" — power depends on the data-generating process
- "(weakly) dominating" — equality holds in some special cases
- "there is concern about" — the concern belongs to the researcher, not the paper

**Inappropriate hedges:**
- "we believe that our estimator may perform reasonably well" — if you proved it, say so
- "it seems plausible that" — either argue it or do not
- "one might argue" — either make the argument or do not

**Check:** For each hedge word (may, might, could, potentially, plausibly, seems), ask: is the uncertainty inherent in the claim, or is the author being unnecessarily timid? Flag the latter.

## Named Results

A distinctive Roth pattern: give impossibility results and key trade-offs memorable names. This makes the contribution citable and memorable.

**Good examples:**
- "trilemma" (Logs) — three desirable properties that cannot all hold
- "sharp null of full mediation" (Testing Mechanisms) — a specific testable hypothesis
- Numbered trade-offs with explicit labels

**Check:** If the paper proves an impossibility result or identifies a fundamental trade-off, does it have a name? Suggest one if not. The name should be descriptive (e.g., "trilemma" for three incompatible desiderata) rather than generic ("our main result").
