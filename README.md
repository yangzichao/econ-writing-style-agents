# Econ Writing Style Agents

Claude Code plugin that reviews economics paper drafts following specific authors' writing conventions.

## Quick Start

### Install

```bash
# In Claude Code, run:
/plugin marketplace add yangzichao/econ-writing-style-agents
/plugin install econ-writing-style-agents@econ-writing-style-agents
```

Or from the terminal:

```bash
claude plugin marketplace add yangzichao/econ-writing-style-agents
claude plugin install econ-writing-style-agents@econ-writing-style-agents
```

### Use

```
/pedro-review path/to/your-paper.pdf
```

The agent reads your paper, consults 7 rule files derived from 20+ published papers, and produces a structured review report.

---

## Agent: `/pedro-review`

Reviews an economics paper and outputs a report with concrete before/after revision suggestions.

**Based on**: Systematic comparison of Pedro H.C. Sant'Anna's ArXiv v1 drafts with published versions across Econometrica, Journal of Econometrics, JPE: Micro, AER, JEL, JBES, and JAERE.

### What the Report Covers

| Section | What It Checks |
|---|---|
| **Abstract** | Throat-clearing, 30-50% compression, self-promotion, purpose-centric framing |
| **Introduction** | Direct contribution opening, enumerated contributions, running example, formal lit section, software |
| **Terminology** | "units" not "individuals", "DiD" not "DID", "comparison group", "working models" |
| **Voice** | Active over passive, definitive over tentative, precision over generality |
| **Framing** | Solution-oriented, intuition-first, RCT parallels, trade-off labeling |
| **Revision Strategy** | What to cut, add, expand — with structural recommendation |
| **Top 5 Changes** | Highest-impact suggestions prioritized |

### Example Output

```
# Pedro Sant'Anna Style Review Report

**Paper**: Estimating Causal Effects with Staggered Adoption
**Assessment**: Strong methods paper; abstract needs 40% compression and the introduction
lacks enumerated contributions.

## Abstract
**[A.1]** Throat-clearing in opening sentence
- Current: "Researchers are often interested in estimating causal effects..."
- Suggested: "We study estimation of causal effects in staggered designs..."
- Rule: 01-abstract, Rule 1

### Rewritten Abstract
[Full rewrite]

### Stats: 165 words → 92 words (44% reduction)

## Top 5 Highest-Impact Changes
1. Rewrite abstract opening (eliminate throat-clearing)
2. Add contribution enumeration to introduction
3. Replace "individuals" with "units" throughout
4. Add running empirical example
5. Move Monte Carlo details to supplementary appendix
```

---

## Manage the Plugin

```bash
# List installed plugins
/plugin

# Disable without uninstalling
/plugin disable econ-writing-style-agents@econ-writing-style-agents

# Re-enable
/plugin enable econ-writing-style-agents@econ-writing-style-agents

# Uninstall
/plugin uninstall econ-writing-style-agents@econ-writing-style-agents

# Update marketplace (pull latest from GitHub)
/plugin marketplace update econ-writing-style-agents
```

---

## How It Works

The agent is a single `SKILL.md` that:

1. **Loads 7 rule files** at runtime (abstract, introduction, terminology, framing, revision, style markers, checklist)
2. **Reads your paper** (PDF, LaTeX, or plain text)
3. **Applies the multi-pass checklist** from `07-checklist.md`
4. **Outputs a structured report** with location, current text, suggested revision, and rule reference for each issue

All rules are empirically derived — not opinions, but patterns observed across 20+ real paper revisions.

## Repo Structure

```
.claude-plugin/plugin.json       # Plugin manifest
marketplace.json                 # Marketplace definition (for /plugin install)
skills/pedro-review/
  SKILL.md                       # Agent entry point
  rules/                         # 7 supporting rule files
  evidence-base.md               # Paper-by-paper evidence
research/pedro-santanna/         # Raw research data (20 paper analyses)
```

## Contributing a New Author Agent

1. Collect papers with multiple versions (e.g., ArXiv v1 + published)
2. Analyze revision patterns, save under `research/<author>/`
3. Synthesize rules under `skills/<author>-review/rules/`
4. Create `skills/<author>-review/SKILL.md`
5. Add to `marketplace.json`

## License

MIT
