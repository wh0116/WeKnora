# 上游改动登记（upstream-changes）

> **用途**：记录本项目相对上游 Tencent/WeKnora 的所有二开改动。每次升级（merge 上游新 tag）前，照此清单逐一排查冲突点；每次改动上游文件后，立即在此追加一行。**不登记 = 升级时可能丢失改动。**

## 基线信息

| 项 | 值 |
|---|---|
| 二开基线 | 上游 tag `v0.9.0` |
| 基线 commit | `f17ee8a8da901bd658a4cb25f40b5fd41adbfdd7` |
| 二开主线分支 | `kaiwu/v0.9.0` |
| 升级方式 | `git merge upstream/<新tag> --no-edit` → 解决冲突 → 全量测试 → 打锚点 tag `cube-sync-v<新tag>` |

## 二开目录约定

- 后端新增代码：`internal/cube/`（与上游 `internal/` 隔离，升级零冲突）
- 前端新增代码：`frontend/src/cube/`
- 部署配置：如需修改 docker-compose / config，**复制一份**到独立目录修改，不直接改上游原件

## 改动登记表

| 日期 | 分支 | 上游文件（相对路径） | 改动类型 | 说明 |
|---|---|---|---|---|
| 2026-11-19 | kaiwu/v0.9.0 | docs/upstream-changes.md | 新增 | 本登记文档自身 |
