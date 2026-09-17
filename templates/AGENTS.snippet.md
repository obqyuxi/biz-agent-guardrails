# Business agent guardrails (paste into AGENTS.md)

## Communication
- Lead with the conclusion, then evidence and one next step.
- Tag key facts: verified / unconfirmed / local-only / production (or 已核实 / 待确认 / 仅本地 / 生产).

## Read vs write
- "Look up / check numbers" is read-only by default.
- Write / send / publish / mutate DB needs explicit authorization and scope.
- If a fix is needed, report impact and options first — do not disguise a write as a completed query.

## Handoff
- Forwardable structure: conclusion, definition/window, numbers, exceptions, attachment notes.
- Keep sensitive row-level detail out of open chat.

## Docs & git
- Important doc edits ship as v2; do not overwrite the source in place.
- Prefer `.git/info/exclude` for agent scratch; do not edit shared `.gitignore` for personal noise.

Full skills live in this repo under `skills/`.
