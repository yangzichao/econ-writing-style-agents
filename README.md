# Econ Writing Style Agents

Pedro Sant'Anna writing-style review plugin for economics papers, packaged for both Claude Code and Codex.

The style rules are derived from comparing early drafts such as ArXiv v1 with published versions across Econometrica, JoE, JPE:Micro, AER, JEL, JBES, and JAERE.

## Plugin

| Plugin | Targets | Purpose |
|---|---|---|
| `pedro-review-agent` | Claude Code, Codex | Pedro Sant'Anna-style editorial review for economics papers |

### Pedro Review Agent

Reviews a PDF, LaTeX, or plain-text paper using 7 rule files derived from 20+ Pedro H.C. Sant'Anna papers. The output is a structured editorial report covering abstract compression, introduction structure, terminology, voice, framing, and the highest-impact revisions.

## Install In Claude Code

```bash
claude plugin marketplace add yangzichao/econ-writing-style-agents
claude plugin install pedro-review-agent@econ-writing-style-agents
```

Or inside a Claude Code session:

```text
/plugin marketplace add yangzichao/econ-writing-style-agents
/plugin install pedro-review-agent@econ-writing-style-agents
```

After installing, run `/reload-plugins`.

## Use In Codex

This repo now includes the Codex plugin files for `pedro-review-agent`:

- `.agents/plugins/marketplace.json`
- `plugins/pedro-review-agent/.codex-plugin/plugin.json`

Open this repository in Codex and let Codex discover the repo-local marketplace from `.agents/plugins/marketplace.json`. If Codex was already open, restart or reload the session so it rescans plugins.

## Update

Claude marketplace update:

```bash
claude plugin marketplace update econ-writing-style-agents
```

For Codex, update the repo and reload Codex so it rescans the plugin metadata.

## Uninstall

Claude uninstall:

```bash
claude plugin uninstall pedro-review-agent@econ-writing-style-agents
```

For Codex, remove the repo-local marketplace entry or remove the plugin files from this repository.

## Repo Structure

```text
.claude-plugin/marketplace.json        # Claude Code marketplace
.agents/plugins/marketplace.json       # Codex marketplace
plugins/
  pedro-review-agent/
    .claude-plugin/plugin.json         # Claude plugin manifest
    .codex-plugin/plugin.json          # Codex plugin manifest
    skills/pedro-review/
      SKILL.md                         # Agent entry point
      rules/                           # 7 rule files
      evidence-base.md                 # Paper-by-paper evidence
research/
  pedro-santanna/                      # Raw research data (20 paper analyses)
```

## Add Another Author Agent

1. Collect papers with multiple versions such as ArXiv v1 plus published.
2. Analyze revision patterns and save them under `research/<author-name>/`.
3. Create `plugins/<author-name>-review-agent/`.
4. Add the plugin manifest for the target product:
   `.claude-plugin/plugin.json` for Claude Code, `.codex-plugin/plugin.json` for Codex, or both.
5. Register the plugin in the matching marketplace file.

## License

MIT
