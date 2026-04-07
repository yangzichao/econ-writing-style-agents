# Review Checklist

A multi-pass review workflow for editing a paper in Pedro Sant'Anna's style. Use this as a structured review process before journal submission.

---

## Pass 1: Structure (Big Picture)

- [ ] Does the paper follow this architecture?
  ```
  Empirical hook / Direct contribution statement
    → Setup with running example
      → Enumerated contributions
        → Formal "Related Literature" subsection
          → Body (intuition-first, then formal)
            → Empirical application
              → Software announcement
                → Conclusion / Implications for Practice
  ```
- [ ] Is there a running empirical example threaded from the introduction?
- [ ] Are contributions enumerated explicitly in the introduction? ("We contribute... First, ... Second, ... Third, ...")
- [ ] Is there a formal "Related Literature" or "Recent Related Literature" subsection?
- [ ] Is there a dedicated "Implications for Practice" or equivalent section?
- [ ] Are Monte Carlo details in the main text or supplementary appendix? (Should be appendix)
- [ ] How many empirical applications? (Prefer one focused application over multiple superficial ones)

---

## Pass 2: Abstract (7 Tests)

- [ ] **Throat-clearing test**: Does the first sentence contain a verb of contribution ("propose," "study," "analyze," "derive," "show")? If not, rewrite.
- [ ] **Compression test**: Can the abstract be cut 30–50%? Flag: asymptotic properties, narrative scaffolding, technical details that belong in the body.
- [ ] **Self-promotion test**: Are there phrases like "of independent interest," "the most precise estimates to date," or "important addition"? Remove.
- [ ] **Empirical results test**: Does the abstract preview specific empirical findings? (Should describe the application topic only, not the findings)
- [ ] **Purpose-centric test**: Does the abstract describe what the method *achieves* or what it *does technically*? (Should be purpose-centric)
- [ ] **Software test**: Is software mentioned in the abstract? (Move to introduction unless journal convention requires it)
- [ ] **Keywords test**: Are formal keywords provided?

---

## Pass 3: Introduction (9 Tests)

- [ ] **Opening sentence**: Does it announce the paper's contribution directly? Not generic field importance?
- [ ] **Quantified hook** (optional): Is there a concrete, data-backed opening? ("over 30% of NBER papers...")
- [ ] **Framework structure**: Is there a numbered step framework? ("Our approach proceeds in three steps: (i)... (ii)... (iii)...")
- [ ] **Contribution enumeration**: After motivation, is there a "We contribute... First,... Second,... Third,..." paragraph?
- [ ] **Running example**: Is abstract notation grounded in a concrete example? ("In our motivating example, tau_2 would be...")
- [ ] **RCT parallel**: Is there an explicit connection to what randomization achieves?
- [ ] **Related literature**: Is it a formal subsection or scattered throughout?
- [ ] **Software announcement**: Named package with GitHub URL?
- [ ] **Confidence level**: Are verbs definitive ("derive," "show," "provide") or tentative ("aim to," "try to," "investigate")?

---

## Pass 4: Terminology (Line-Level)

### Substitution Table
Check every instance:
- [ ] "individuals" → "units"
- [ ] "DID" → "DiD"
- [ ] "control group" → "comparison group"
- [ ] "setups" → "designs"
- [ ] "(as-if) randomly assigned" → "as-good-as randomly assigned"
- [ ] "propensity score model" → "propensity score working model" (when misspecification is possible)
- [ ] "estimation procedure" → "estimators"
- [ ] "strategies" → "procedures"
- [ ] "slope coefficients" → "marginal effects"
- [ ] "introduces" → "proposes"

### Precision Check
For each claim, ask: *Is this as specific as it can be?*
- [ ] Replace "can be hard to interpret" with the specific reason
- [ ] Replace "due to treatment effect heterogeneity" with the specific mechanism
- [ ] Replace "improves power" with "can lead to power gains" (if conditional)
- [ ] Add "strictly" to "monotonic" if that's what's meant
- [ ] Add "working" before "model" where misspecification is relevant

### Voice Check
- [ ] Convert passive to active: "can be identified" → "are identified"
- [ ] Convert tentative to definitive: "aim to fill" → "provide"
- [ ] Reduce "our proposed" — use "the proposed" for objects, "we" for actions

---

## Pass 5: Hedging Audit

- [ ] **Appropriate hedges**: Is each hedge mathematically justified?
  - "if and essentially only if" — edge case documented in a remark?
  - "(weakly) dominating" — equality case identified?
  - "can lead to" — condition for improvement stated?
- [ ] **Vague hedges to remove**: "perhaps," "somewhat," "potentially," "in some sense," "to some extent," "it seems that"
- [ ] **Over-hedging**: Are v1-style hedges still present? ("We aim to," "We try to," "We hope to")

---

## Pass 6: Additions Check

- [ ] **Falsification tests**: Can the theoretical results be turned into testable implications?
- [ ] **Heuristic summaries**: Does each major technical result have an "At the practical level..." follow-up?
- [ ] **Formal lemmas**: Are key equations elevated to formal lemma/proposition statements?
- [ ] **Simultaneous inference**: Is the paper offering pointwise inference when simultaneous is feasible?
- [ ] **Replication files**: Is a GitHub link to replication code provided?
- [ ] **Acknowledgments**: Seminar venues? RAs? Referees? AI tools?

---

## Pass 7: Framing Check

- [ ] **Solution framing**: Are challenges framed as design choices, not obstacles?
- [ ] **Intuition before math**: Does each section build intuition before presenting formal results?
- [ ] **Forward engineering**: If critiquing TWFE or existing methods, is the critique constructive?
- [ ] **Trade-off labeling**: Are key trade-offs explicitly named? (e.g., "robustness vs. efficiency")

---

## Pass 8: Final Sentence-Level Polish

- [ ] **Long compound sentences**: Break into shorter, single-point sentences
- [ ] **Math in running text**: Move complex equations to displayed math
- [ ] **Abbreviations**: Spelled out on first use? Full terms preferred in introduction?
- [ ] **Redundant qualifiers**: "but alternative estimators are also feasible" — delete
- [ ] **Unnecessary parenthetical asides**: "(one and two sided)" when "any" implies both — delete
- [ ] **Consistent terminology**: Same term used throughout? No switching between synonyms?
- [ ] **"As so," usage**: Used correctly as a transition (optional — this is a distinctive marker)

---

## Quick Reference: The 5 Most Common Fixes

Based on frequency across all 20 papers analyzed:

1. **Kill the first paragraph** — the opening background paragraph in v1 is almost always deleted or compressed to one sentence
2. **Cut abstract by 40%** — remove technical properties, narrative, self-promotion
3. **Replace "individuals" with "units"** — appears in virtually every paper
4. **Add contribution enumeration** — "We contribute... First,... Second,..."
5. **Add software link** — named package + GitHub URL in introduction
