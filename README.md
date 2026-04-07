# Econ Writing Style Agents

Claude Code plugin that reviews economics papers following specific authors' writing conventions.

## Agent: `/pedro-review`

Reviews a paper draft and produces a structured editorial report following Pedro H.C. Sant'Anna's style — derived from comparing 20+ ArXiv v1 drafts with published versions across Econometrica, JoE, JPE:Micro, AER, JEL, JBES, and JAERE.

```
/pedro-review path/to/your-paper.pdf
```

**Output**: A structured report covering abstract, introduction, terminology, framing, and revision strategy — with concrete before/after suggestions and top 5 highest-impact changes.

## Install

**As a plugin** (recommended):
```bash
# Add the marketplace and install
claude /plugin install --source github yangzichao/econ-writing-style-agents
```

**Or clone directly into your project**:
```bash
cd your-paper-project
git clone https://github.com/yangzichao/econ-writing-style-agents.git .econ-style
# Then in Claude Code:
/plugin add .econ-style
```

**Or symlink for personal use**:
```bash
git clone https://github.com/yangzichao/econ-writing-style-agents.git ~/econ-style-agents
mkdir -p ~/.claude/skills
ln -s ~/econ-style-agents/skills/pedro-review ~/.claude/skills/pedro-review
```

## What It Checks

| Pass | What |
|---|---|
| Abstract | Throat-clearing, compression (30-50%), self-promotion, purpose-centric framing |
| Introduction | Direct opening, enumerated contributions, running example, formal lit section, software |
| Terminology | "units" not "individuals", "DiD" not "DID", "comparison group", "working models" |
| Voice | Active over passive, definitive over tentative, precision over generality |
| Framing | Solution-oriented, intuition-first, RCT parallels, trade-off labeling |
| Revision | Cut Monte Carlo to appendix, add falsification tests, add replication files |

## Structure

```
.claude-plugin/plugin.json       # Plugin manifest
skills/pedro-review/
  SKILL.md                       # Agent (reads rules, reviews paper, outputs report)
  rules/01-abstract.md           # 7 abstract rules with before/after examples
  rules/02-introduction.md       # 9 introduction rules
  rules/03-terminology.md        # Substitution tables, precision, hedging
  rules/04-framing.md            # 8 framing patterns
  rules/05-revision.md           # What to cut/add/expand
  rules/06-style-markers.md      # Signature phrases, architecture conventions
  rules/07-checklist.md          # Multi-pass review checklist
  evidence-base.md               # Paper-by-paper evidence for each rule
research/                        # Raw data used to derive rules (20 paper analyses)
```

## Contributing a New Author Agent

1. Collect their papers with multiple versions (ArXiv v1 + published)
2. Run comparative analysis, save under `research/<author>/`
3. Synthesize rules under `skills/<author>-review/rules/`
4. Create `skills/<author>-review/SKILL.md`

## License

MIT
