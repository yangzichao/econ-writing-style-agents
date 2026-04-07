---
name: pedro-review
description: Review an economics paper following Pedro Sant'Anna's writing style. Accepts a paper path and produces a structured editorial report covering abstract, introduction, terminology, framing, and prioritized revisions.
argument-hint: <path-to-paper>
allowed-tools: Read Grep Glob Write
---

# Pedro Sant'Anna Writing Style Review

Review the paper path provided by the user and produce a structured editorial report. If the caller passes an explicit argument string such as `$ARGUMENTS`, use that as the paper path.

## Step 1: Load Rules

Read these supporting files from this skill directory in parallel:

- `rules/01-abstract.md` — Abstract compression, throat-clearing, self-promotion
- `rules/02-introduction.md` — Opening, contributions, running examples
- `rules/03-terminology.md` — Word substitutions, precision, active voice, hedging
- `rules/04-framing.md` — Solution framing, intuition-first, RCT parallels
- `rules/05-revision.md` — What to cut, add, expand
- `rules/06-style-markers.md` — Signature phrases, architecture, survey conventions
- `rules/07-checklist.md` — Full multi-pass review checklist
- `evidence-base.md` — Paper-by-paper supporting evidence for the style rules

## Step 2: Read the Paper

Read the target paper. For PDFs, read pages 1-8 (abstract + intro) and the last 5 pages (conclusion). Scan section headings. If no paper path is available, ask the user for one before continuing.

## Step 3: Review

Apply the 7-pass checklist from `07-checklist.md`. For each issue, provide the location, current text, suggested revision, and which rule applies.

## Step 4: Output and Save the Report

Use this format. After outputting the report, save it as a markdown file in the same directory as the input paper. Name the file `<paper-filename>-pedro-review.md` (e.g., if the paper is `my-paper.pdf`, save to `my-paper-pedro-review.md` in the same folder).

```
# Pedro Sant'Anna Style Review Report

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
- [ ] Direct contribution opening
- [ ] Enumerated contributions ("We contribute... First,...")
- [ ] Running empirical example
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

**Abstract**: First sentence must contain "propose/study/derive/show." Compress 30-50%. Remove empirical results. Remove self-promotion.

**Introduction**: Open with contribution, not context. Enumerate contributions. Add running example. Formal lit section. Announce software.

**Terminology**: "units" not "individuals." "DiD" not "DID." "comparison group" not "control group." "working models" for misspecified models.

**Voice**: "are identified" not "can be identified." "We derive" not "We aim to." "eliminate" not "alleviate."

**Framing**: Solution-oriented, not problem-oriented. Intuition before math. Label trade-offs explicitly.
