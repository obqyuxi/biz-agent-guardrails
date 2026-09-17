# Contributing

[中文版](CONTRIBUTING.zh-CN.md)

## Add a skill

1. Create `skills/<kebab-id>/SKILL.md`
2. Frontmatter must include:

```yaml
---
name: kebab-id
description: Use when … (one line on when to load this skill)
---
```

3. Body should cover: when it applies / when it does not, hard rules, steps, pitfalls, acceptance. Prefer **English** for new skills; Chinese-only is OK only when the skill is intentionally locale-specific (e.g. `conclusion-first-zh`).
4. Forbidden: real PII, secrets, private hostnames, identifiable customer SQL
5. Update the skill table in `README.md` (and `README.zh-CN.md` if needed), `CHANGELOG.md`, and `ROADMAP.md` when relevant
6. Mark sample data with `EXAMPLE`

## Acceptance (before merge)

- [ ] Frontmatter `name` matches folder id
- [ ] Description starts with `Use when`
- [ ] No secrets / private hosts / real customer identifiers
- [ ] README table updated
- [ ] CHANGELOG entry added
