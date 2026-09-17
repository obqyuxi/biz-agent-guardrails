# 贡献指南

## 加一条 Skill

1. 在 `skills/<kebab-id>/` 新建 `SKILL.md`
2. Frontmatter 必须含：

```yaml
---
name: kebab-id
description: Use when …（一句话说明何时加载）
---
```

3. 正文用简体中文写清：适用/不适用、硬规则、步骤、坑、验收
4. 禁止：真实 PII、密钥、内网主机名、可识别的客户业务 SQL
5. 更新 `README.md` 表格、`CHANGELOG.md`、必要时 `ROADMAP.md`
6. 示例数据统一加 `EXAMPLE` 标记

## 验收（合入前）

- [ ] `name` 与目录名一致
- [ ] `description` 以 “Use when” / “用于……” 开头，便于 Agent 检索
- [ ] 陌生人能在不了解作者公司的情况下复用
- [ ] 无密钥与真实客户信息

## PR 说明

用一两句话说清：这条 skill 解决什么反复出错；附一个虚构 before/after（可放 `examples/`）。
