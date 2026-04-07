# Econ Writing Style Agents

This repo provides Claude Code skills for reviewing and polishing economics papers following Pedro H.C. Sant'Anna's writing style.

## Available Skills

- `/review-pedro-style <file>` — Full multi-pass review (structure, abstract, intro, terminology, framing, polish)
- `/polish-abstract <file>` — Abstract-specific review and rewrite
- `/polish-introduction <file>` — Introduction-specific review
- `/revision-guide <file>` — Pre-submission revision plan (what to cut, add, expand)

## Project Structure

- `skills/` — Detailed reference documentation (8 files covering rules, patterns, evidence)
- `papers/analysis/` — Per-paper comparative analyses (20 markdown files)
- `papers/raw_pdfs/` — Downloaded ArXiv v1 and published PDFs
- `.claude/skills/` — Claude Code skill definitions (installable)

## Style Methodology

All rules are derived from comparing ArXiv v1 drafts with final published versions of 20+ Sant'Anna papers across Econometrica, Journal of Econometrics, JPE: Micro, AER, JEL, JBES, and JAERE.
