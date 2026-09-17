# biz-agent-guardrails

Installable skill pack for **Codex / Cursor / Claude Code / Hermes-style agents**: safer day-to-day business collaboration, forwardable handoffs, and clearer evidence.

**English is the default.** [中文说明](README.zh-CN.md)

## What this is

Reusable Agent Skills / rule snippets for problems that keep showing up:

| Problem | Skill |
|---------|-------|
| Replies wander; no conclusion first | `conclusion-first-zh` |
| Guesses written as facts | `evidence-grades` |
| "Just look up the numbers" quietly writes to DB/config | `read-vs-write` |
| Deliverables cannot be forwarded as-is | `forwardable-handoff` |
| Overwriting source docs breaks history | `doc-versioning-v2` |
| Agent scratch pollutes shared git trees | `local-artifact-git-hygiene` |

## What this is not

- Not one company's BI / ERP business code
- No real customer data, SQL, secrets, or private network hosts
- Not another "universal agent framework"

## Install (pick one)

### Codex / generic `AGENTS.md`

Paste [`templates/AGENTS.snippet.md`](templates/AGENTS.snippet.md) into a project or global `AGENTS.md`, then load `skills/*/SKILL.md` as needed.

### Cursor / Claude Code Skills

Copy the folders you need under `skills/` into your skills root (or ship as a plugin). Each `SKILL.md` needs discoverable frontmatter `name` / `description`.

### Minimal set

1. Install only `evidence-grades` + `read-vs-write` (smallest guardrail set)
2. Add `forwardable-handoff` for business handoffs
3. Add `doc-versioning-v2` for document collaboration

## Layout

```
skills/           # installable skills
templates/        # AGENTS snippet, sample daily report, refusal scripts
examples/         # fictional before/after
CONTRIBUTING.md   # how to add a skill
ROADMAP.md        # what might land next
```

## Security & privacy

Before you commit: no real names / phones / member IDs, no connection strings, no bot secrets, no private IPs. Mark sample numbers with `EXAMPLE`.

## Maintenance

Prefer at most **1–2** skill or template updates per week, distilled from real mistakes. See `ROADMAP.md` and `CHANGELOG.md`.

## License

MIT
