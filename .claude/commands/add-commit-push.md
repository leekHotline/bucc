---
allowed-tools: bash, git
---

一键提交并推送到 dev 分支：

1. `git add .`
2. `git diff --cached` 查看暂存区改动
3. 根据改动生成 commit 信息，类型：feat/fix/chore/docs/refactor
4. `git commit -m "类型: 简短描述"`
5. `git push origin dev`

自动执行，无需确认。