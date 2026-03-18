# PopRaKo 组织快速上手

本文档用于帮助新成员在 10-20 分钟内完成组织协作环境配置，并提交第一个 PR。

## 1. 前置准备

请先安装：

- Git（建议最新版）
- Go（后端开发需要）
- Node.js 20+ 与 pnpm（前端开发需要）
- VS Code（推荐）及常用插件（Go、ESLint、Vue）

可选：

- GitHub CLI（`gh`，便于命令行处理 PR）

## 2. 加入组织与权限检查

1. 接受组织邀请并完成 2FA（双因素认证）
2. 确认你在对应仓库具备 `Read/Write` 权限
3. 访问仓库：
   - 后端：`https://github.com/ATOMLubover/poprako-w`
   - 前端：`https://github.com/SeaAndStars/poprako-web`
   - 主工作区：`https://github.com/SeaAndStars/poprako`

## 3. 克隆仓库

以主工作区为例：

```bash
git clone https://github.com/SeaAndStars/poprako.git
cd poprako
git submodule update --init --recursive
```

如果你只做单仓库开发，也可以直接克隆对应仓库。

## 4. 分支策略（必须遵守）

- `main`：稳定分支（发布基线）
- `develop`：开发集成分支
- `feature/*`：功能开发分支
- `fix/*`：缺陷修复分支
- `hotfix/*`：线上紧急修复分支

开发流程：

1. 从 `develop` 拉取你的分支
2. 在个人分支开发并提交
3. 发起 PR 到 `develop`
4. Review + CI 通过后合并

## 5. 后端本地启动（Go）

在后端目录执行：

```bash
cd backend/backend-v1
go mod tidy
go test ./...
go run .
```

如果项目使用了数据库或对象存储，请根据仓库内配置文件补充环境变量。

## 6. 前端本地启动（Vue 3）

在前端目录执行：

```bash
cd web
pnpm install
pnpm dev
```

常用命令：

```bash
pnpm lint
pnpm type-check
pnpm build
```

## 7. 提交规范

推荐提交格式（Conventional Commits）：

- `feat: 新增功能`
- `fix: 修复问题`
- `docs: 文档更新`
- `refactor: 重构`
- `chore: 工程维护`

示例：

```bash
git commit -m "feat(team): add team avatar upload API"
```

## 8. Pull Request 规范

PR 建议包含：

- 变更背景（为什么做）
- 变更内容（做了什么）
- 影响范围（哪些模块）
- 测试结果（如何验证）
- 回滚方案（可选）

合并门槛建议：

- 至少 1 位 Reviewer 通过
- CI 全绿
- 无冲突
- 描述完整

## 9. Issue 使用规范

建议标签：

- `bug`
- `feature`
- `docs`
- `refactor`
- `question`
- `good first issue`
- `priority:high`

Issue 描述最少包含：

- 复现步骤 / 需求背景
- 期望结果
- 实际结果（问题类）
- 截图或日志（如有）

## 10. 常见问题（FAQ）

### Q1：PR 显示冲突怎么办？

1. 拉取最新 `develop`
2. 合并到你的分支并解决冲突
3. 本地测试通过后推送

### Q2：我只改文档需要跑测试吗？

建议至少运行基础检查，保证不破坏现有流程。

### Q3：为什么我推送失败？

检查是否有分支保护规则、权限不足或本地分支落后远端。

## 11. 第一个贡献（推荐路径）

1. 领取 `good first issue`
2. 新建 `feature/xxx` 分支
3. 完成变更 + 本地验证
4. 提交 PR 到 `develop`
5. 根据 Review 反馈迭代直至合并
