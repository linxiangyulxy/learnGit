> 参考[廖雪峰Git教程]([Git教程 - 廖雪峰的官方网站](https://www.liaoxuefeng.com/wiki/896043488029600))

#### 初始化

- 初始化仓库 `git init`

- 工作区、暂存区、仓库

#### 提交修改

- `git add <file>` 将文件添加到暂存区

- `git commit -m "first commit"` 从暂存区添加到分支

#### 查看历史状态

- 要随时掌握工作区的状态，使用`git status`命令。

- 如果`git status`告诉你有文件被修改过，用`git diff`可以查看修改内容。

#### 版本回退

- `HEAD`指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令`git reset --hard commit_id`。

- 穿梭前，用`git log`可以查看提交历史，以便确定要回退到哪个版本。

- 要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。

#### 撤销修改

- 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令`git checkout -- file`。

- 场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令`git reset HEAD <file>`，就回到了场景1，第二步按场景1操作。

- 场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，使用版本回退，不过前提是没有推送到远程库。

#### 删除文件

```
rm test.md
git rm test.md
git commit -m "del test.md"
```

#### 远程仓库

```
# 关联远程仓库
git remote add origin https://github.com/linxiangyulxy/learnGit.git
# 第一次推送master分支的所有内容
git push -u origin master
```

之后使用命令 `git push origin master` 就可以推送最新修改

#### 分支

Git鼓励大量使用分支：

- 查看分支：`git branch`

- 创建分支：`git branch <name>`

- 切换分支：`git checkout <name>`或者`git switch <name>`

- 创建+切换分支：`git checkout -b <name>`或者`git switch -c <name>`

- 合并某分支到当前分支：`git merge <name>`

- 删除分支：`git branch -d <name>`

#### 标签

- 命令`git tag <tagname>`用于新建一个标签，默认为`HEAD`，也可以指定一个commit id；

- 命令`git tag -a <tagname> -m "blablabla..."`可以指定标签信息；

- 命令`git tag`可以查看所有标签。
