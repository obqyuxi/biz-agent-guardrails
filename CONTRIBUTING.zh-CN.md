# 贡献指南

默认文档为英文，请优先阅读 [Contributing (English)](CONTRIBUTING.md)。

## 加一条 Skill

1. 在 `skills/<kebab-id>/` 新建 `SKILL.md`
2. Frontmatter 必须含：

```yaml
---
name: kebab-id
description: Use when …（一句话说明何时加载；英文优先）
---
```

3. 正文写清：适用/不适用、硬规则、步骤、坑、验收。新 skill 默认英文；仅当技能本身面向中文场景（如 `conclusion-first-zh`）时可用中文正文。
4. 禁止：真实 PII、密钥、内网主机名、可识别的客户业务 SQL
5. 更新 `README.md` / `README.zh-CN.md` 表格、`CHANGELOG.md`、必要时 `ROADMAP.md`
6. 示例数据统一加 `EXAMPLE` 标记

## 验收（合入前）

- [ ] Frontmatter `name` 与目录名一致
- [ ] `description` 以 `Use when` 开头
- [ ] 无密钥 / 内网主机 / 真实客户标识
- [ ] README 表格已更新
- [ ] CHANGELOG 已登记
