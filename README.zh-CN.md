# 业务 Agent 护栏（biz-agent-guardrails）

面向 **Codex / Cursor / Claude Code / Hermes 类 Agent** 的可安装技能包：让日常业务协作更安全、交付更可转发、证据更清楚。

**默认文档为英文。** 本页是中文说明；请先看 [English README](README.md)。

## 这是什么

一组可复用的 Agent Skills / 规则片段，解决这些反复出现的问题：

| 问题 | 对应 skill |
|------|------------|
| 回复绕、不先给结论 | `conclusion-first-zh` |
| 把猜测写成事实 | `evidence-grades` |
| 查数任务偷偷改库/改配置 | `read-vs-write` |
| 交付物没法直接转发 | `forwardable-handoff` |
| 直接改原文导致无法回溯 | `doc-versioning-v2` |
| Agent 本地产物污染共享仓库 | `local-artifact-git-hygiene` |

## 不是什么

- 不是某一家公司的 BI / ERP 业务代码
- 不包含真实客户数据、SQL、密钥、内网地址
- 不是又一个「万能 Agent 框架」

## 安装（任选）

### Codex / 通用 AGENTS.md

把 [`templates/AGENTS.snippet.md`](templates/AGENTS.snippet.md) 粘贴进项目或全局 `AGENTS.md`，再按需引用 `skills/*/SKILL.md`。

### Cursor / Claude Code Skills

将 `skills/` 下需要的目录复制到你的 skills 根目录（或做成插件），确保每个 `SKILL.md` 的 frontmatter `name` / `description` 可被发现。

### 最小用法

1. 只装 `evidence-grades` + `read-vs-write`（护栏最小集）
2. 业务交付再加 `forwardable-handoff`
3. 文档协作再加 `doc-versioning-v2`

## 仓库结构

```
skills/           # 可安装技能
templates/        # AGENTS 片段、示例日报、拒答话术
examples/         # 虚构场景前后对比
CONTRIBUTING.md   # 如何加一条 skill（英文默认；见 CONTRIBUTING.zh-CN.md）
ROADMAP.md        # 下一周可以加什么
```

## 安全与隐私

提交前自查：无真实姓名/手机/会员号、无连接串、无 Bot Secret、无内网 IP。示例数字必须标明 `EXAMPLE`。

## 维护节奏

建议每周从真实踩坑提炼 **至多 1～2** 条 skill/模板更新，见 `ROADMAP.md` 与 `CHANGELOG.md`。

## License

MIT
