---
allowed-tools: bash, mcp__github
---

创建 PR 并合并到 main：

1. `git branch --show-current` 获取当前分支
2. `git diff main...HEAD` 分析改动
3. `gh pr create --base main --fill` 创建 PR
4. `gh pr merge --auto --squash` 自动合并

使用 gh CLI，无需 MCP。
