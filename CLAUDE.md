# Econ Writing Style Agents

Claude Code plugin providing writing style review agents for economics papers.

## Agent

`/pedro-review <file>` — Reviews an economics paper and produces a structured editorial report following Pedro Sant'Anna's writing conventions.

## Structure

```
.claude-plugin/plugin.json    # Plugin manifest (enables /plugin install)
skills/pedro-review/
  SKILL.md                    # Agent entry point
  rules/                      # 7 rule files (supporting docs the agent reads)
  evidence-base.md            # Paper-by-paper evidence
research/pedro-santanna/      # Raw research data used to derive rules
```
