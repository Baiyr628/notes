# Git 常用命令

```bash
  # 提交当前仓库所有修改至暂存区
  git add .
  # 提交修改至本地仓库
  git commit  -m 'something'
  # 推送本地仓库的master分支至远程仓库origin的master分支
  git push origin master
  # 推送本地仓库的提交至远程仓库（同上），并关联远程仓库的master分支和本地仓库的master分支
  git push -u origin master

  # 拉取远程仓库，同步；并使用rebase方式合并
  git pull --reba
  # 拉取远程仓库的修改至本地，但不和本地仓库合并
  git fetch origin master

  # 添加远程仓库origin，origin为远程仓库在本地的别名
  git remote add origin $url

  # 保存当前修改至工作区，并恢复工作区状态至上一次提交后的状态
  git stash
  # 查看保存的修改的列表
  git stash --list
  # 弹出最后一次保存的修改内容
  git stash pop

  # 查看git所有配置信息
  git config --list
  # 查看全局配置
  git config --global --list

  # 设置当前仓库的git 用户名
  git config user.name 'username'
  # 设置全局配置
  git config --gloabal user.name 'username'
  # 设置当前仓库的git 邮箱
  git config user.email 'example@git.com'
  # 设置全局配置
  git config --global user.email 'example@git.com'

  # 查看本地所有分之列表
  git branch -a
  # 查看本地所有远程分支
  git branch -r
```