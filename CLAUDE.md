# Econ Writing Style Agents

A collection of writing style review agents for economics papers. Each agent embodies a specific author's editorial voice, derived from empirical analysis of their revision patterns.

## Agents

### `/pedro-review <file>`
Pedro Sant'Anna Writing Style Review Agent. Reviews an economics paper and produces a structured report with concrete revision suggestions — covering abstract, introduction, terminology, framing, and revision strategy.

Rules: `agents/pedro-santanna-review/rules/`
Evidence: `agents/pedro-santanna-review/evidence-base.md`

## Repo Structure

```
agents/              # Agent definitions and their knowledge bases
  pedro-santanna-review/
    rules/           # Style rules the agent applies (7 files)
    evidence-base.md # Paper-by-paper evidence for each rule

research/            # Raw research data used to build agents
  pedro-santanna/
    paper-master-list.md
    analysis/        # 20 per-paper comparative analyses
    raw_pdfs/        # Downloaded ArXiv v1 + published PDFs

.claude/skills/      # Claude Code skill entry points
  pedro-review/
    SKILL.md         # Agent invocation definition
```
