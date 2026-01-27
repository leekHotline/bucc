---
allowed-tools: bash, mcp__github
---

创建 PR 并合并到 main 分支：

1. `git branch --show-current` - 获取当前分支名
2. `git diff main...HEAD` - 分析与 main 分支的差异
3. `gh pr create --base main --fill` - 创建 PR（自动填充标题和描述）
4. 尝试自动合并：
   - `gh pr merge --auto --squash` - 如果仓库支持自动合并
   - 如果失败，使用 `gh pr merge <PR号> --squash` - 手动合并
5. 如果有合并冲突：
   - `gh pr checkout <PR号>` - 检出 PR 分支
   - `git fetch origin main && git merge origin/main` - 合并 main 分支
   - 解决冲突后提交：`git commit -m "chore: resolve merge conflicts"`
   - `git push origin <分支名>` - 推送解决后的代码
   - 再次执行合并命令

**注意事项：**
- 使用 gh CLI 工具，确保已安装并登录
- PR 会使用 squash 方式合并（多个提交压缩为一个）
- 如果 main 分支有保护规则，可能需要手动处理
