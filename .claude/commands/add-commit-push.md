---
allowed-tools: bash, git
---

一键提交并推送到 dev 分支：

1. `git add .` - 添加所有改动到暂存区
2. `git diff --cached` - 查看暂存区改动内容
3. 根据改动生成 commit 信息
   - 类型：feat（新功能）/ fix（修复）/ chore（杂项）/ docs（文档）/ refactor（重构）
   - 格式：`类型: 简短描述`
4. `git commit -m "..."` - 创建提交
5. `git pull origin dev --rebase` - 拉取远程更新（如果有）
6. `git push origin dev` - 推送到远程

**注意事项：**
- 自动执行，无需确认
- 如果远程有新提交，会自动 rebase 后再推送
- 提交信息应简洁明了，描述改动的核心内容