# Git 速查表

## 基础
- `git status` 看现状
- `git add <file>` 加到暂存区
- `git commit -m "msg"` 提交
- `git log --oneline --graph --all` 看历史

## 分支
- `git switch -c feature/x` 建并切
- `git switch main` 切回
- `git merge feature/x` 合并
- `git branch -d feature/x` 删

## 撤销
- `git restore <file>` 丢弃工作区改动
- `git restore --staged <file>` 取消暂存
- `git commit --amend [-m "new"]` 改最近 commit
- `git reset HEAD~1` 撤回最近 commit（保留改动）
- `git reset --hard <hash>` 拉回到指定 commit（丢改动）⚠️
- `git revert <hash>` 反向提交（已 push 的安全做法）

## 远程
- `git push` / `git pull` / `git fetch`
- `gh repo create <name> --public --source=. --remote=origin --push`

## 进阶
- `git rebase main` 重基到 main 顶端
- `git rebase -i HEAD~3` 交互式整理最近 3 条
- `git stash -u` 收抽屉（含未跟踪文件）
- `git stash pop` 从抽屉拿出
