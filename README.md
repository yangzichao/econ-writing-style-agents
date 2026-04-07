# Econ Writing Style Agents

Claude Code skills for reviewing and polishing economics papers following Pedro H.C. Sant'Anna's writing conventions.

## What This Is

A set of Claude Code slash commands that review your economics paper drafts the way Pedro Sant'Anna would — eliminating throat-clearing, compressing abstracts, sharpening terminology, and applying the revision patterns that transform working papers into top-journal publications.

All rules are empirically derived from comparing 20+ ArXiv v1 drafts with their final published versions across Econometrica, Journal of Econometrics, JPE: Micro, AER, JEL, JBES, and JAERE.

## Installation

### Option 1: Clone and symlink (recommended)

```bash
git clone https://github.com/yangzichao/econ-writing-style-agents.git
# Symlink the skills into your global Claude Code skills directory
ln -s "$(pwd)/econ-writing-style-agents/.claude/skills/review-pedro-style" ~/.claude/skills/review-pedro-style
ln -s "$(pwd)/econ-writing-style-agents/.claude/skills/polish-abstract" ~/.claude/skills/polish-abstract
ln -s "$(pwd)/econ-writing-style-agents/.claude/skills/polish-introduction" ~/.claude/skills/polish-introduction
ln -s "$(pwd)/econ-writing-style-agents/.claude/skills/revision-guide" ~/.claude/skills/revision-guide
```

### Option 2: Copy directly

```bash
git clone https://github.com/yangzichao/econ-writing-style-agents.git
cp -r econ-writing-style-agents/.claude/skills/* ~/.claude/skills/
```

### Option 3: Use in a project

Clone the repo into your project directory. Claude Code will automatically discover the skills in `.claude/skills/`.

```bash
cd your-paper-project
git clone https://github.com/yangzichao/econ-writing-style-agents.git .claude-style
ln -s .claude-style/.claude/skills .claude/skills
```

## Usage

Once installed, use these slash commands in Claude Code:

### `/review-pedro-style <file>`
Full multi-pass editorial review:
- **Pass 1**: Structure (architecture, running example, contributions, lit review)
- **Pass 2**: Abstract (throat-clearing, compression, self-promotion, framing)
- **Pass 3**: Introduction (opening, framework, enumeration, software)
- **Pass 4**: Terminology (substitutions, precision, active voice)
- **Pass 5**: Hedging audit
- **Pass 6**: Framing (solution-oriented, intuition-first, trade-off labeling)
- **Pass 7**: Sentence-level polish

### `/polish-abstract <file>`
Focused abstract review and rewrite with:
- Throat-clearing elimination
- 30-50% compression
- Purpose-centric reframing
- Before/after comparison with change log

### `/polish-introduction <file>`
Introduction-specific review covering:
- Opening sentence quality
- Contribution enumeration
- Running example presence
- Literature section structure
- Verb confidence level

### `/revision-guide <file>`
Pre-submission revision strategy:
- What to cut (8 categories)
- What to add (8 categories)
- What to expand (5 categories)
- Structural recommendation (grow/shrink/restructure)
- Estimated revision magnitude

## What the Style Covers

| Category | Key Rules |
|---|---|
| **Abstract** | Eliminate throat-clearing; compress 30-50%; remove self-promotion; purpose-centric framing |
| **Introduction** | Direct contribution opening; enumerated contributions; running empirical example; formal lit section |
| **Terminology** | "units" not "individuals"; "DiD" not "DID"; "comparison group" not "control group"; "working models" |
| **Voice** | Active over passive ("are identified" not "can be identified"); definitive over tentative ("derive" not "investigate") |
| **Hedging** | Hedge only with mathematical justification; eliminate vague hedges ("perhaps," "somewhat") |
| **Framing** | Solution-oriented; intuition before math; RCT parallels; forward engineering |
| **Revision** | Cut Monte Carlo to appendix; add falsification tests; add software links; reduce applications |

## Reference Documentation

The `skills/` directory contains detailed reference files:

| File | Content |
|---|---|
| `skills/01-abstract-rules.md` | 7 abstract rules with 12+ before/after examples |
| `skills/02-introduction-rules.md` | 9 introduction rules with evidence |
| `skills/03-terminology-and-voice.md` | Substitution tables, precision, hedging |
| `skills/04-framing-and-motivation.md` | 8 framing patterns with examples |
| `skills/05-revision-patterns.md` | What to cut/add/expand with paper-specific evidence |
| `skills/06-distinctive-style-markers.md` | Signature phrases, architecture, survey conventions |
| `skills/07-review-checklist.md` | Multi-pass checklist with checkboxes |
| `skills/08-evidence-base.md` | Paper-by-paper evidence for all 20 papers |

## Evidence Base

Derived from comparative analysis of these published papers:

| Paper | Journal | Key Insight |
|---|---|---|
| When Is Parallel Trends Sensitive to Functional Form? | Econometrica 2023 | 40% abstract compression; added falsification tests |
| Efficient Estimation for Staggered Rollout Designs | JPE:Micro 2023 | 50% abstract compression; removed self-promotion |
| What's Trending in DiD? | JoE 2023 | Added running Medicaid example |
| Covariate Distribution Balance via Propensity Scores | JAE 2022 | Reframing from method-centric to purpose-centric |
| DiD with Multiple Time Periods | JoE 2021 | Most dramatic: simple paper → unified three-step framework |
| Doubly Robust DiD Estimators | JoE 2020 | Three new contributions added; "working models" terminology |
| DiD with a Continuous Treatment | AER (forthcoming) | "selection bias" replaces "treatment effect heterogeneity" |
| Selection and Parallel Trends | Working paper (v14) | 14 versions over 4 years; if-and-only-if characterization |

Plus 12 additional papers. See `skills/08-evidence-base.md` for the complete list.

## License

MIT
