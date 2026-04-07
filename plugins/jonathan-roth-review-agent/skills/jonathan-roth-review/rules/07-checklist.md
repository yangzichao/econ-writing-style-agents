# Review Checklist

A multi-pass review workflow for editing a paper in Jonathan Roth's style.

## Pass 1: Structure (Big Picture)
- [ ] Does the paper follow this architecture?
  ```
  Problem identification (common practice + hidden limitation)
    -> Named result or impossibility (if applicable)
      -> Menu of alternatives / constructive solution
        -> Formal results (body)
          -> Empirical illustration
            -> Practical recommendations
              -> Software announcement
  ```
- [ ] Is there a concrete empirical example threaded from the introduction?
- [ ] Are contributions explicitly enumerated?
- [ ] Is there a formal "Related Literature" subsection?
- [ ] Is there a "Practical Recommendations" section or equivalent?
- [ ] Is software announced with package name and GitHub URL?

## Pass 2: Abstract (7 Tests)
- [ ] **Opening test**: Does sentence 1 describe a specific common practice or field context (not generic throat-clearing)?
- [ ] **Problem test**: Does the abstract clearly identify the limitation or hidden assumption?
- [ ] **Named result test**: If the paper proves an impossibility, is it named memorably?
- [ ] **Compression test**: Can the abstract be cut 30-50%? Flag: mathematical notation, step-by-step methodology, narrative scaffolding.
- [ ] **Alternatives test**: Does the abstract mention constructive alternatives or recommendations?
- [ ] **Self-promotion test**: Remove "of independent interest," "most precise estimates to date."
- [ ] **Application test**: Are empirical applications mentioned?

## Pass 3: Introduction (8 Tests)
- [ ] **Common practice opening**: Does the introduction identify what researchers currently do?
- [ ] **Quantified survey** (if possible): Is the problem's prevalence quantified?
- [ ] **Hidden assumption**: Is the limitation/assumption clearly surfaced?
- [ ] **Contribution enumeration**: Are contributions listed explicitly?
- [ ] **Concrete example**: Is abstract notation grounded in a real example?
- [ ] **Menu of alternatives**: After impossibility, are options enumerated as (i)...(ii)...(iii)...?
- [ ] **Related literature**: Formal subsection, not scattered?
- [ ] **Software**: Named package with GitHub URL?

## Pass 4: Terminology (Line-Level)
Check every instance:
- [ ] "Social scientists are often interested in" -> specific context
- [ ] "Researchers are often interested in" -> "We study..." or specific description
- [ ] "DID" -> "DiD"
- [ ] "(as-if) randomly assigned" -> "as-good-as randomly assigned"
- [ ] "we consider" -> "we show" / "we establish" / "we develop"
- [ ] "we investigate" -> "we characterize" / "we derive"

## Pass 5: Voice Check
- [ ] Convert tentative to definitive: "we consider" -> "we show"
- [ ] Use "I" for solo papers, "we" for co-authored
- [ ] Remove vague hedges: "perhaps," "somewhat," "in some sense"
- [ ] Keep precise hedges: "(weakly) dominating," "may have low power" (when conditional)

## Pass 6: Framing Check
- [ ] **Critique-then-construct**: Is the problem identified before the solution?
- [ ] **Named impossibilities**: Are negative results memorably labeled?
- [ ] **Menu framing**: Are alternatives structured as (i)...(ii)...(iii)...?
- [ ] **Sensitivity framing**: Can robustness be framed as formal sensitivity analysis?
- [ ] **Practitioner bridge**: Are technical results restated for applied researchers?

## Pass 7: Additions Check
- [ ] **Quantified survey**: Can you add a survey of existing practice?
- [ ] **Practical recommendations**: Is there a dedicated recommendations section?
- [ ] **Software**: R/Stata package with GitHub link?
- [ ] **Falsification tests**: Can theoretical results yield testable implications?
- [ ] **Title**: Could the title be a question or more memorable phrase?

## Quick Reference: The 5 Most Common Fixes
1. **Kill generic throat-clearing** -- "Social scientists are often interested in" must go
2. **Name your impossibility result** -- if you prove something can't be done, give it a label
3. **Add a menu of alternatives** -- after impossibility, enumerate options as (i)...(ii)...(iii)
4. **Add a quantified survey** -- how prevalent is the practice you're critiquing?
5. **Add software** -- named package + GitHub URL in introduction
