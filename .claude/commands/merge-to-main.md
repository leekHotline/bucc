---
allowed-tools: bash, mcp__github
---

创建 PR 并合并到 main：

1. 获取当前分支名 如dev
2. `git diff main...HEAD` 分析改动
3. 创建 PR（使用 gh 或 MCP）
4. 自动合并 PR
5. 删除远程分支（可选）

自动执行，无需确认。