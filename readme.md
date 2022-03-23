### 初始化

- 初始化仓库 `git init`

- 工作区、暂存区、仓库

### 第一次提交

- `git add <file>` 将文件添加到暂存区

- `git commit -m "first commit"` 从暂存区添加到分支

### 查看历史状态

- 要随时掌握工作区的状态，使用`git status`命令。

- 如果`git status`告诉你有文件被修改过，用`git diff`可以查看修改内容。

### 版本回退

- `HEAD`指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令`git reset --hard commit_id`。

- 穿梭前，用`git log`可以查看提交历史，以便确定要回退到哪个版本。

- 要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。
