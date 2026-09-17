---
name: local-artifact-git-hygiene
description: Use when Agent 在仓库内生成查询结果、导出、scratch 文件，需要避免污染共享 git 规则或其他人的工作树。
---

# 本地产物与 Git 卫生

## 硬规则

1. 默认 **不要修改共享的 `.gitignore`** 来掩盖个人/Agent 产物。
2. 优先使用 **本克隆私有** 排除：`.git/info/exclude`（或用户指定的本地 ignore）。
3. 生成物放在约定目录（如 `/scratch/`、`/outputs/`），并证明不会被误 `git add`。
4. 清理时只删本次创建且无后续用途的临时文件；保留交付物与用户文件。
5. 注意：`git clean -fdx` 仍可能删掉仅被 ignore 的文件——清理前确认路径。

## 建议自检

```bash
git check-ignore -v path/to/artifact
git add -n path/to/artifact   # 应无输出或明确被忽略
```

## 验收

共享 ignore 无无关 diff；本地产物不会进入即将推送的 commit。
