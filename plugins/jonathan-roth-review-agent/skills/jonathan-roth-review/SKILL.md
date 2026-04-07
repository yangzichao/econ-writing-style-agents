---
name: jonathan-roth-review
description: Review an economics paper following Jonathan Roth's writing style. Checks abstract, introduction, terminology, framing, and produces a structured editorial report with before/after suggestions.
argument-hint: <path-to-paper>
allowed-tools: Read Grep Glob Write
---

# Jonathan Roth Writing Style Review

Review the paper path provided by the user and produce a structured editorial report. If the caller passes an explicit argument string such as `$ARGUMENTS`, use that as the paper path.

## Step 1: Load Rules

Read these supporting files from this skill directory in parallel:

- `rules/01-abstract.md` — Abstract compression, opening patterns, named results
- `rules/02-introduction.md` — Common practice opening, hidden assumptions, empirical surveys
- `rules/03-terminology.md` — Word substitutions, precision, active voice, hedging
- `rules/04-framing.md` — Critique-then-construct, impossibility results, sensitivity analysis
- `rules/05-revision.md` — What to cut, add, expand; title evolution
- `rules/06-style-markers.md` — Signature phrases, architecture, question titles
- `rules/07-checklist.md` — Full multi-pass review checklist
- `evidence-base.md` — Paper-by-paper supporting evidence for the style rules

## Step 2: Read the Paper

Read the target paper. For PDFs, read pages 1-8 (abstract + intro) and the last 5 pages (conclusion). Scan section headings. If no paper path is available, ask the user for one before continuing.

## Step 3: Review

Apply the 7-pass checklist from `07-checklist.md`. For each issue, provide the location, current text, suggested revision, and which rule applies.

## Step 4: Output and Save the Report

Use this format. After outputting the report, save it as a markdown file in the same directory as the input paper. Name the file `<paper-filename>-jonathan-roth-review.md` (e.g., if the paper is `my-paper.pdf`, save to `my-paper-jonathan-roth-review.md` in the same folder).

```
# Jonathan Roth Style Review Report

**Paper**: [title]
**Date**: [today]
**Assessment**: [one sentence summary]

## Abstract
[Issues with current/suggested/rule for each]
### Rewritten Abstract
[Full rewrite applying all rules]
### Stats: [original words] → [revised words] ([X]% reduction)

## Introduction
[Issues found]
### Missing Elements
- [ ] Common practice opening with quantified survey
- [ ] Hidden assumption/limitation identified
- [ ] Named impossibility result (if applicable)
- [ ] Enumerated contributions
- [ ] Running empirical example
- [ ] Menu of alternatives (if applicable)
- [ ] Formal "Related Literature" subsection
- [ ] Software/package announcement

## Terminology & Voice
| Location | Current | Suggested | Rule |
|---|---|---|---|

## Framing & Revision Strategy
[Recommended cuts, additions, structural changes]

## Top 5 Highest-Impact Changes
1. ...
2. ...
3. ...
4. ...
5. ...
```

## Key Rules (Quick Reference)

**Abstract**: Open with specific common practice or field context (not generic). Name impossibility results. Compress 30-50%. End with alternatives or recommendations.

**Introduction**: Open with what researchers do. Reveal the hidden assumption. Quantify prevalence if possible. Enumerate contributions. Add running example. Formal lit section. Announce software.

**Terminology**: "DiD" not "DID." "as-good-as randomly assigned." "We show/establish" not "We consider/investigate." "pre-trends" not "pre-treatment trends."

**Voice**: Definitive over tentative. "I" for solo papers. Hedge only when mathematically justified.

**Framing**: Critique-then-construct. Name impossibility results. Enumerate alternatives as (i)...(ii)...(iii)... Frame robustness as sensitivity analysis. End with practical recommendations.
