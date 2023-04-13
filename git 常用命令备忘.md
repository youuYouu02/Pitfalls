## git 常用命令备忘

#### 1 流程相关

- `git clone <repo_url>` ：将远程仓库拉到本地
  - `git clone -b <branch_name> <repo_url>` ：拉下单个分支
- `git add --all`
- `git commit -m ""`
- `git push`：首次直接 git push 会提示关联分支
  - `git push <repo_name> <local_branch>:<remote_branch> `：将本地 local_branch 分支推送到远程 repo 的 remote_branch 分支
  - `git push <remote> <local_branch>`：将当前分支推送到远程同名分支
  - 可以通过 `git remote` 命令查看远程仓库名称

#### 2 分支相关

- `git branch` 列出本地所有分支；`git branch -a` 列出所有分支
- `git switch <branch_name>` 切换分支
- `git branch -b <branch_name>`：创建新分支
- `git merge <branch_name` ：将指定的分支合并到当前分支。通常情况下，需要先切换到主分支，然后再将其他分支合并到主分支。
- `git branch -d <branch_name>`
- `git push origin <branch_name>`：创建远程分支
- `git push origin --delete <branch_name>`：删除远程分支

#### 3 清除相关

- `git checkout -- <file_name>`：撤销已修改未 add 的部分的修改，即回到最近一次 add
- `git rm --cached <file_name>` ：撤销已 add 未 commit 的 add，即回到最近一次 commit