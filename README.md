# Econ Writing Style Agents

A collection of writing style review agents for economics papers. Each agent embodies a specific author's editorial voice, derived from empirical analysis of how their papers evolve from working paper to publication.

## Available Agents

### Pedro Sant'Anna Review (`/pedro-review`)

Reviews an economics paper draft and produces a structured editorial report following Pedro H.C. Sant'Anna's writing conventions.

**What it does:**
- Reads your paper (PDF or text)
- Applies 7 categories of editorial rules derived from 20+ published papers
- Produces a report with concrete before/after suggestions
- Rewrites the abstract applying all rules
- Lists the top 5 highest-impact changes

**Methodology:** Every rule is empirically derived from comparing ArXiv v1 drafts with final published versions across Econometrica, Journal of Econometrics, JPE: Micro, AER, JEL, JBES, and JAERE.

## Installation

### Option 1: Symlink (recommended)

```bash
git clone https://github.com/yangzichao/econ-writing-style-agents.git
ln -s "$(pwd)/econ-writing-style-agents/.claude/skills/pedro-review" ~/.claude/skills/pedro-review
```

### Option 2: Copy

```bash
git clone https://github.com/yangzichao/econ-writing-style-agents.git
cp -r econ-writing-style-agents/.claude/skills/pedro-review ~/.claude/skills/pedro-review
```

### Option 3: In-project

Clone into your project directory. Claude Code auto-discovers `.claude/skills/`.

## Usage

```
/pedro-review path/to/your-paper.pdf
```

Or:

```
/pedro-review path/to/your-paper.tex
```

The agent will read the paper, consult its style rules, and produce a structured review report.

## What the Agent Checks

| Category | Key Rules |
|---|---|
| **Abstract** | Eliminate throat-clearing; compress 30-50%; remove self-promotion; purpose-centric framing |
| **Introduction** | Direct contribution opening; enumerated contributions; running empirical example; formal lit section |
| **Terminology** | "units" not "individuals"; "DiD" not "DID"; "comparison group" not "control group"; "working models" |
| **Voice** | Active over passive; definitive over tentative |
| **Framing** | Solution-oriented; intuition before math; RCT parallels; forward engineering |
| **Revision** | Cut Monte Carlo to appendix; add falsification tests; add software links |
| **Polish** | Break compound sentences; remove redundant qualifiers; consistent terminology |

## Repo Structure

```
.claude/skills/pedro-review/    # Claude Code agent entry point
agents/pedro-santanna-review/   # Rules and evidence the agent reads
  rules/                        # 7 rule files (abstract, intro, terminology, ...)
  evidence-base.md              # Paper-by-paper evidence for each rule
research/pedro-santanna/        # Raw research data
  paper-master-list.md          # Complete paper list with versions
  analysis/                     # 20 per-paper comparative analyses
  raw_pdfs/                     # ArXiv v1 + published PDFs
```

## Evidence Base

| Paper | Journal | Key Insight |
|---|---|---|
| When Is Parallel Trends Sensitive to Functional Form? | Econometrica 2023 | 40% abstract compression; added falsification tests |
| Efficient Estimation for Staggered Rollout Designs | JPE:Micro 2023 | 50% abstract compression; removed self-promotion |
| DiD with Multiple Time Periods | JoE 2021 | Most dramatic: simple paper → unified three-step framework |
| Doubly Robust DiD Estimators | JoE 2020 | Three new contributions added; "working models" terminology |
| DiD with a Continuous Treatment | AER (forthcoming) | "selection bias" replaces "treatment effect heterogeneity" |
| Selection and Parallel Trends | Working paper (v14) | 14 versions over 4 years |

Plus 14 additional papers. See `agents/pedro-santanna-review/evidence-base.md` for the complete list.

## Contributing

To add a new author's writing style agent:

1. Collect their papers (multiple versions per paper)
2. Run comparative analysis under `research/<author-name>/`
3. Synthesize rules under `agents/<author-name>-review/rules/`
4. Create a skill entry point in `.claude/skills/<agent-name>/SKILL.md`

## License

MIT
