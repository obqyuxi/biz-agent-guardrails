# 虚构诊所运营：回复前后对比（EXAMPLE）

场景：负责人问「昨天现金多少？渠道有没有异常？」

## Before（常见差评回复）

> 我先看了一下库，然后检查了几个表，中间有个字段可能要注意，另外我还可以帮你优化报表模块……（无结论、无口径、无证据等级）

## After（应用护栏）

> 昨天现金业绩为 EXAMPLE 12.8 万。【仅本地·示例】  
> 口径：收款 − 退款，Asia/Shanghai 自然日。【待确认·需正式只读入口复跑】  
> 异常：未知渠道 EXAMPLE 3 笔，需追 `source_path` 原始值。【待确认】  
> 下一步：你若授权正式只读查询，我按同一口径出可转发结论；改数不在本次范围。

## 用到的 skills

`conclusion-first-zh` · `evidence-grades` · `read-vs-write` · `forwardable-handoff`
