# Git

## create

```
makedir dirname # 创建文件名

pwd # 显示当前文件

git init # 是当前文件夹成为repository

ls -ah # 显示文件夹下的文件，包括隐藏文件

git add readme.txt # 将文件添加到暂存区

git commit -m "word" #提交所有文件的修改
```

## control

```
git status # 查看工作区状态

git diff file # 查看修改了什么内容，与最近一次比较

git log # 查看提交历史记录

git log --pretty=online # 一行式输出

git reset --hard HEAD^ # 版本回退到上个（^^就是上上个）

git reset --hard 33343343 #回退到某个版本号，要先找到该版本号

git reflog # 每次操作的历史记录

git diff HEAD -- file # 比较工作区和版本库

git checkout -- file # 撤销修改

git reset HEAD file # 将暂存区的修改撤销掉，重新放回工作区，之后可以配合 git checkout --file

rm file  # 删除文件

git checkout -- file # 如果误删就撤销删除

git rm file # 真正从版本库中删除，配合git commit 使用
```

## Romote

```
git remote add origin git@github.com:yourclub/learn.git # 与远程某个repository关联

git push -u origin master # 把本地推送到远程库中

git push origin master # 之后可以直接这么做

git clone git@github.com:yourid/learn.git # 克隆库到本地
```

## branch

```
git checkout -b dev # 相当于如下功能

git branch dev # 创建分支dev

git checkout dev # 指向分支dev

git branch # 查看当前分支

git merge dev # 合并分支,Fast-forward

git branch dev # 删除分支

git log --graph --pretty=online --abbrev-commit # 图形式log

git merge --no-ff -m "word" dev # 非快速合并

git stash # 把当前工作现场储存起来

git stash list # 查看储藏的工作现场

git stash apply # 恢复工作，但stash内容并不删除，需要以下命令

git stash drop # 删除stash内容

git stash pop # 恢复同时删除

git stash apply stash@{0} #恢复指定的stash，但要先用git stash list 查看

git branch -D dev # 强制删除分支，因为有可能你没有合并就想要删除
```

## team

```
git remote # 查看关联远程库

git remote -v # 显示详细信息

git checkout -b dev origin/dev # 创建远程origin的dev分支到本地

git pull # 从远程抓取最新的
```



