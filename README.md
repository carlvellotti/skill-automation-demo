# Skill Automation Demo

A Claude Code skill that runs itself. Every Monday at 9 AM ET (or on demand), GitHub Actions spins up Claude Code, Claude runs the `/experiment-report` skill against the data in this repo, and commits the finished report to `reports/`. Nobody is in the loop.

Built for the NYT Maker Week Skills Incubator. Copy this repo as a template for your own scheduled skills.

## The three pieces

1. **The skill** (`.claude/skills/experiment-report/SKILL.md`): what to do and what good looks like. This is the part that's yours. Swap it for any skill and the automation doesn't change.
2. **The data** (`data/`): the experiment config (success criteria, guardrails) and a daily metrics CSV. In real life this is whatever your skill reads.
3. **The workflow** (`.github/workflows/experiment-report.yml`): ~20 lines. A schedule, a checkout, and one step that runs Claude Code with the prompt `/experiment-report`.

## What I demoed vs your version

| Piece | This repo | At NYT |
| --- | --- | --- |
| The workflow yaml | `.github/workflows/experiment-report.yml` | Identical. `anthropics/claude-code-action` is already allowed in your org. |
| The API key | A repo secret (`ANTHROPIC_API_KEY`) | No repo secrets. The Maker Week background-agents automation provides keys from Vault automatically. See docs.nyt.net/eng/ai/background-agents. |
| The repo | Personal public repo | A repo in the NYT GitHub org (you can create these). |
| The trigger | Cron + a manual run button | Identical. |
| The skill + data | This repo's files | Your skill, your data. |
| The output | A committed markdown report | Same to start. Posting to Slack instead needs a bot/webhook approved by EdTech. |

## Run it yourself (outside NYT)

1. Use this template / fork it.
2. Add a repo secret named `ANTHROPIC_API_KEY` (Settings → Secrets and variables → Actions).
3. Actions tab → "Weekly experiment report" → Run workflow.
4. Watch the run, then look in `reports/`.

## Other skills you could run this way

Weekly competitive scans, Monday status drafts from tickets and notes, metric anomaly watches that only speak up when something moves, stale-ticket sweeps, a monthly pass that tidies your project folder. Same yaml every time. Only the skill file changes.

## Three gotchas we hit so you don't have to

1. **`id-token: write`** must be in the permissions block or the action fails immediately with an OIDC error.
2. **Claude can't write files by default** in automation mode. Without `--allowedTools` in `claude_args`, every file write is silently denied and the run still shows green. Grant exactly what the skill needs, nothing more.
3. **Commit explicitly.** The action doesn't reliably commit what Claude produced, and it scrubs the checkout credentials after its step. The final workflow step commits `reports/` and pushes using the workflow's own token.

All three fixes are visible in the workflow file, which is the whole story of this repo: the yaml is plumbing you copy once, the skill is the part you own.
