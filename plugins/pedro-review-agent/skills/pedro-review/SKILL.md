---
name: pedro-review
description: Review an economics paper following Pedro Sant'Anna's writing style. Checks abstract, introduction, terminology, framing, and produces a structured editorial report with before/after suggestions.
argument-hint: <path-to-paper>
allowed-tools: Read Grep Glob
---

# Pedro Sant'Anna Writing Style Review

Review the paper at $ARGUMENTS and produce a structured editorial report.

## Step 1: Load Rules

Read these supporting files from ${CLAUDE_SKILL_DIR} in parallel:

- `${CLAUDE_SKILL_DIR}/rules/01-abstract.md` — Abstract compression, throat-clearing, self-promotion
- `${CLAUDE_SKILL_DIR}/rules/02-introduction.md` — Opening, contributions, running examples
- `${CLAUDE_SKILL_DIR}/rules/03-terminology.md` — Word substitutions, precision, active voice, hedging
- `${CLAUDE_SKILL_DIR}/rules/04-framing.md` — Solution framing, intuition-first, RCT parallels
- `${CLAUDE_SKILL_DIR}/rules/05-revision.md` — What to cut, add, expand
- `${CLAUDE_SKILL_DIR}/rules/06-style-markers.md` — Signature phrases, architecture, survey conventions
- `${CLAUDE_SKILL_DIR}/rules/07-checklist.md` — Full multi-pass review checklist

## Step 2: Read the Paper

Read $ARGUMENTS. For PDFs, read pages 1-8 (abstract + intro) and the last 5 pages (conclusion). Scan section headings.

## Step 3: Review

Apply the 7-pass checklist from `07-checklist.md`. For each issue, provide the location, current text, suggested revision, and which rule applies.

## Step 4: Output the Report

Use this format:

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
