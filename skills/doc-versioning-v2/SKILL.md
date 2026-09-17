---
name: doc-versioning-v2
description: Use when editing requirements, metric definitions, handoff docs, or PRDs and you must keep the prior version reviewable instead of overwriting in place.
---

# 文档版本：新建 v2，不覆盖原文

## 硬规则

1. 用户说「不要直接在原文改」或同等意思时：复制为 `*-v2.md`（或约定的下一版本号）再编辑。
2. 在 v2 文首用 3～5 行写清：相对 v1 改了什么、未改什么、待确认项。
3. 不要删除 v1，除非用户明确要求归档/删除。
4. 大改口径时，旧结论标记为「可能过时」，并指向 v2。

## 文件命名建议

- `主题-v1.md` → `主题-v2.md`
- 或 `主题.md` 保留，`主题.v2.md` 新增（团队选一种并写进项目约定）

## 验收

仓库中同时能打开上一版与当前版；v2 文首有变更摘要。
