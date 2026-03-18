# PopRaKo

PopRaKo 是一个面向漫画翻校协作的现代化平台，提供从团队协作、任务流转到内容管理的一体化支持。

## 我们在做什么

- 协同漫画翻校与管理
- 团队与成员权限管理
- 任务分配与工作流追踪
- 前后端分离、可持续迭代的工程体系

## 仓库导航

- `poprako`：主工作区（包含后端与前端）
- `poprako-w`：后端核心仓库（Go）
- `poprako-web`：前端仓库（Vue 3 + Vite + TypeScript）
- `.github`：组织级文档、模板与规范

> 不同仓库的职责会持续清晰化，欢迎通过 Issue 提交改进建议。

## 技术栈

- 后端：Go
- 前端：Vue 3 / Vite / TypeScript / Pinia
- API：RESTful API
- 协作：GitHub Issues / Pull Requests / Actions

## 参与方式

1. 阅读快速上手文档（见 `docs/quick-start.md`）
2. 挑选 `good first issue` 或提交新 Issue
3. 按分支规范提交 PR
4. 通过 Code Review 与 CI 后合并

## 组织约定（摘要）

- 默认分支：`develop`（开发集成）与 `main`（稳定发布）
- 功能开发：从 `develop` 拉取功能分支
- 合并要求：至少 1 次 Review + CI 通过
- 提交信息：建议遵循 Conventional Commits（`feat:` / `fix:` / `docs:` 等）

## 联系与支持

- 问题反馈：请在对应仓库提交 Issue
- 安全问题：请勿公开披露，优先私下联系维护者
- 新成员接入：请先完成快速上手流程
