# Econ Writing Style Agents

Claude Code plugin marketplace for economics paper writing style review agents.

## Install

```bash
claude plugin marketplace add yangzichao/econ-writing-style-agents
claude plugin install pedro-review-agent@econ-writing-style-agents
```

Or inside a Claude Code session:

```
/plugin marketplace add yangzichao/econ-writing-style-agents
/plugin install pedro-review-agent@econ-writing-style-agents
```

After installing, run `/reload-plugins` to activate.

## Use

```
/pedro-review-agent:pedro-review path/to/your-paper.pdf
```

Accepts PDF, LaTeX, or plain text. The agent reads your paper, applies 7 rule files derived from 20+ published papers, and produces a structured editorial report.

## Agent: `/pedro-review-agent:pedro-review`

Reviews an economics paper following Pedro H.C. Sant'Anna's writing style — derived from comparing his ArXiv v1 drafts with published versions across Econometrica, JoE, JPE:Micro, AER, JEL, JBES, and JAERE.

### What the Report Covers

| Section | What It Checks |
|---|---|
| **Abstract** | Throat-clearing, 30-50% compression, self-promotion, purpose-centric framing |
| **Introduction** | Direct contribution opening, enumerated contributions, running example, formal lit section |
| **Terminology** | "units" not "individuals", "DiD" not "DID", "comparison group", "working models" |
| **Voice** | Active over passive, definitive over tentative, precision over generality |
| **Framing** | Solution-oriented, intuition-first, RCT parallels, trade-off labeling |
| **Revision Strategy** | What to cut, add, expand — with structural recommendation |
| **Top 5 Changes** | Highest-impact suggestions prioritized |

### Example Output

```
# Pedro Sant'Anna Style Review Report

**Paper**: Estimating Causal Effects with Staggered Adoption
**Assessment**: Strong methods paper; abstract needs 40% compression
and the introduction lacks enumerated contributions.

## Abstract
**[A.1]** Throat-clearing in opening sentence
- Current: "Researchers are often interested in estimating causal effects..."
- Suggested: "We study estimation of causal effects in staggered designs..."
- Rule: 01-abstract, Rule 1

### Rewritten Abstract
[Full rewrite applying all rules]

### Stats: 165 words → 92 words (44% reduction)

## Top 5 Highest-Impact Changes
1. Rewrite abstract opening (eliminate throat-clearing)
2. Add contribution enumeration to introduction
3. Replace "individuals" with "units" throughout
4. Add running empirical example
5. Move Monte Carlo details to supplementary appendix
```

## Update

```bash
claude plugin marketplace update econ-writing-style-agents
```

## Uninstall

```bash
claude plugin uninstall pedro-review-agent@econ-writing-style-agents
```

## Repo Structure

```
.claude-plugin/marketplace.json              # Marketplace definition
plugins/pedro-review-agent/                  # Plugin package
  .claude-plugin/plugin.json                 # Plugin manifest
  skills/pedro-review/
    SKILL.md                                 # Agent entry point
    rules/                                   # 7 rule files the agent reads
    evidence-base.md                         # Paper-by-paper evidence
research/pedro-santanna/                     # Raw research data (20 paper analyses)
```

## Contributing a New Author Agent

1. Collect papers with multiple versions (e.g., ArXiv v1 + published)
2. Analyze revision patterns, save under `research/<author>/`
3. Create a new plugin under `plugins/<author>-review-agent/`
4. Add entry to `.claude-plugin/marketplace.json`

## License

MIT
