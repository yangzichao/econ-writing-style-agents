# Econ Writing Style Agents

Claude Code plugin marketplace for economics paper writing style review agents. Each agent encodes one author's revision patterns.

Install with:
```
claude plugin marketplace add yangzichao/econ-writing-style-agents
claude plugin install <agent-name>@econ-writing-style-agents
```

## Available Agents

- **Pedro Review Agent** — `/pedro-review-agent:pedro-review <file>`
  Reviews an economics paper following Pedro Sant'Anna's writing conventions.
  Definition: `plugins/pedro-review-agent/skills/pedro-review/SKILL.md`

- **Jonathan Roth Review Agent** — `/jonathan-roth-review-agent:jonathan-roth-review <file>`
  Reviews an economics paper following Jonathan Roth's writing conventions.
  Definition: `plugins/jonathan-roth-review-agent/skills/jonathan-roth-review/SKILL.md`

## Structure

- `plugins/<agent-name>/` — Agent plugin packages
- `research/<author-name>/` — Raw research data for each author's style
