# git 常用指令

| Git命令             | 说明                                               |
| ------------------ | ----------------------------------------------------- |
| `git init`         | 初始化一个新的Git仓库。                                  |
| `git clone <repository>`   | 克隆远程仓库到本地。                           |
| `git add <file>`   | 将文件添加到暂存区。                                    |
| `git commit -m "<message>"`  | 提交暂存区的文件并添加提交消息。             |
| `git status`       | 查看仓库状态，显示已修改和待提交的文件。                      |
| `git push`         | 将本地的提交推送到远程仓库。                             |
| `git pull`         | 从远程仓库获取最新的提交并合并到本地仓库。 |
| `git branch`       | 显示本地分支列表。                                       |
| `git checkout <branch>`     | 切换到指定的分支。                                |
| `git merge <branch>`       | 将指定分支的更改合并到当前分支。              |
| `git log`          | 查看提交历史记录。                                      |
| `git diff`         | 显示文件的差异。                                            |
| `git remote add <name> <url>` | 添加远程仓库的名称和URL。                    |
| `git remote -v`    | 显示远程仓库的详细信息。                              |
| `git reset <file>` | 从暂存区中移除文件。                                     |
| `git revert <commit>` | 撤销指定的提交。                                     |
| `git cherry-pick <commit>` | 将某次commit提交至其它分支上，需要提前进入该分支 |
