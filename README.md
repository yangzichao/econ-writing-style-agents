# Econ Writing Style Agents

Claude Code plugin that reviews economics paper drafts following specific authors' writing conventions.

## Install

```bash
claude plugin marketplace add yangzichao/econ-writing-style-agents
claude plugin install econ-writing-style-agents@econ-writing-style-agents
```

Or inside a Claude Code session:

```
/plugin marketplace add yangzichao/econ-writing-style-agents
/plugin install econ-writing-style-agents@econ-writing-style-agents
```

After installing, run `/reload-plugins` in your session to activate.

## Use

```
/pedro-review path/to/your-paper.pdf
```

Accepts PDF, LaTeX, or plain text. The agent reads your paper, consults 7 rule files derived from 20+ published papers, and produces a structured review report with concrete before/after suggestions.

## Agent: `/pedro-review`

Reviews an economics paper following Pedro H.C. Sant'Anna's writing style. Based on systematic comparison of his ArXiv v1 drafts with published versions across Econometrica, Journal of Econometrics, JPE: Micro, AER, JEL, JBES, and JAERE.

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
claude plugin uninstall econ-writing-style-agents@econ-writing-style-agents
```

## How It Works

The agent is a single `SKILL.md` that:

1. **Loads 7 rule files** at runtime — abstract, introduction, terminology, framing, revision patterns, style markers, and a multi-pass checklist
2. **Reads your paper** (PDF, LaTeX, or plain text)
3. **Applies the checklist** systematically across all sections
4. **Outputs a structured report** with location, current text, suggested revision, and rule reference for each issue

All rules are empirically derived from comparing ArXiv v1 drafts with final published versions of 20+ papers — not opinions, but observed revision patterns.

## Repo Structure

```
.claude-plugin/
  plugin.json                    # Plugin manifest
  marketplace.json               # Marketplace definition
skills/pedro-review/
  SKILL.md                       # Agent entry point
  rules/                         # 7 supporting rule files the agent reads
  evidence-base.md               # Paper-by-paper evidence for each rule
research/pedro-santanna/         # Raw research data (20 paper analyses)
```

## Contributing a New Author Agent

1. Collect papers with multiple versions (e.g., ArXiv v1 + published)
2. Analyze revision patterns, save under `research/<author>/`
3. Synthesize rules under `skills/<author>-review/rules/`
4. Create `skills/<author>-review/SKILL.md`
5. Add entry to `.claude-plugin/marketplace.json`

## License

MIT
