# Econ Writing Style Agents

A Claude Code plugin marketplace for economics paper writing style review. Each agent encodes the revision patterns of a specific author — derived from comparing early drafts (e.g., ArXiv v1) with published versions.

## Install

```bash
# Add the marketplace
claude plugin marketplace add yangzichao/econ-writing-style-agents

# Install the agent(s) you want
claude plugin install pedro-review-agent@econ-writing-style-agents
claude plugin install jonathan-roth-review-agent@econ-writing-style-agents
```

Or inside a Claude Code session:

```
/plugin marketplace add yangzichao/econ-writing-style-agents
/plugin install pedro-review-agent@econ-writing-style-agents
/plugin install jonathan-roth-review-agent@econ-writing-style-agents
```

After installing, run `/reload-plugins` to activate.

## Available Agents

| Agent | Command | Author Style |
|---|---|---|
| Pedro Review Agent | `/pedro-review-agent:pedro-review <file>` | Pedro H.C. Sant'Anna |
| Jonathan Roth Review Agent | `/jonathan-roth-review-agent:jonathan-roth-review <file>` | Jonathan Roth |

### Pedro Review Agent

Reviews an economics paper following Pedro H.C. Sant'Anna's writing style — derived from comparing his ArXiv v1 drafts with published versions across Econometrica, JoE, JPE:Micro, AER, JEL, JBES, and JAERE.

Accepts PDF, LaTeX, or plain text. The agent reads your paper, applies 7 rule files derived from 20+ published papers, and produces a structured editorial report covering: abstract compression, introduction structure, terminology, voice, framing, and a prioritized list of changes.

### Jonathan Roth Review Agent

Reviews an economics paper following Jonathan Roth's writing style — derived from comparing his ArXiv v1 drafts with published versions across QJE, AER: Insights, REStud, Econometrica, JoE, JASA, and JPE:Micro.

Focuses on: critique-then-construct framing, named impossibility results, menu-of-alternatives structure, sensitivity analysis framing, quantified empirical surveys, practical recommendations, and question titles.

### Which agent should I use?

The two agents share many mechanical rules (compress abstracts, kill throat-clearing, add software links) but diverge on *framing*. Sant'Anna's style leads with the solution — "here's a better tool." Roth's style leads with the critique — "here's what's wrong and how to fix it." Running both on the same paper and comparing the reports can help you decide which framing fits your paper better.

## Update

```bash
claude plugin marketplace update econ-writing-style-agents
```

## Uninstall

```bash
claude plugin uninstall pedro-review-agent@econ-writing-style-agents
claude plugin uninstall jonathan-roth-review-agent@econ-writing-style-agents
```

## Repo Structure

```
.claude-plugin/marketplace.json        # Marketplace definition
plugins/
  pedro-review-agent/                  # Pedro Sant'Anna style agent
    skills/pedro-review/
      SKILL.md                         # Agent entry point
      rules/                           # 7 rule files
      evidence-base.md                 # Paper-by-paper evidence
  jonathan-roth-review-agent/          # Jonathan Roth style agent
    skills/jonathan-roth-review/
      SKILL.md                         # Agent entry point
      rules/                           # 7 rule files
      evidence-base.md                 # Paper-by-paper evidence
research/
  pedro-santanna/                      # Raw research data (20 paper analyses)
  jonathan-roth/                       # Raw research data (10+ paper analyses)
```

## Contributing a New Author Agent

1. Collect papers with multiple versions (e.g., ArXiv v1 + published)
2. Analyze revision patterns, save under `research/<author-name>/`
3. Create a new plugin under `plugins/<author-name>-review-agent/`
4. Add entry to `.claude-plugin/marketplace.json`

## License

MIT
