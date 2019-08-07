<!-- TOC -->autoauto- [git 常用操作](#git-常用操作)auto    - [克隆远端仓库](#克隆远端仓库)auto    - [同步远端仓库到本地](#同步远端仓库到本地)auto    - [初始化一个本地GIT仓储](#初始化一个本地git仓储)auto    - [添加本地GIT忽略清单文件.gitignore](#添加本地git忽略清单文件gitignore)auto    - [查看本地仓储的变更状态](#查看本地仓储的变更状态)auto    - [将文件添加本地暂存（托管）](#将文件添加本地暂存托管)auto    - [提交](#提交)auto    - [查看提交日志](#查看提交日志)auto    - [根据日志回滚到某次提交时的状态](#根据日志回滚到某次提交时的状态)auto    - [将项目提交到GitHub仓库中](#将项目提交到github仓库中)auto    - [将本地仓储的提交记录推送到远端的master分支](#将本地仓储的提交记录推送到远端的master分支)auto    - [拉取远端master分支的更新记录到本地](#拉取远端master分支的更新记录到本地)auto    - [查看项目分支](#查看项目分支)auto    - [创建分支并托管代码](#创建分支并托管代码)auto    - [切换分支](#切换分支)auto    - [删除远端分支](#删除远端分支)auto    - [删除本地分支](#删除本地分支)auto    - [删除远端提交过的文件（如readme.md）](#删除远端提交过的文件如readmemd)auto    - [设置提交时不用输入账号密码](#设置提交时不用输入账号密码)auto    - [撤销commit](#撤销commit)auto    - [代码冲突](#代码冲突)autoauto<!-- /TOC -->
# git 常用操作

## 克隆远端仓库
```
$ git clone https://github.com/sadicLiu/HelloWorld
```

## 同步远端仓库到本地
```
$ git pull angular_guide
```

## 初始化一个本地GIT仓储
```
// 初始化本地仓储
$ git init
```

## 添加本地GIT忽略清单文件.gitignore
```
新建.gitignore文件
将要忽略的文件名写入该文件
```

## 查看本地仓储的变更状态
```
$ git status [-s]
```

## 将文件添加本地暂存（托管）
```
// 添加指定文件名的文件
$ git add README.md
// 添加通配符匹配的文件
$ git add *.md
// 添加所有未托管的文件（忽略.gitignore清单中的列表）
$ git add --all
```

## 提交
```
$ git commit -m 'Initial commit(change log)'
// -m: message
```

## 查看提交日志
```
$ git log
```

## 根据日志回滚到某次提交时的状态
```
$ git reset --hard 0dsafj
// log中哈希值的前六位
```

## 将项目提交到GitHub仓库中
```
// 添加一个远端地址并起了一个别名叫origin
$ git remote add origin https://github.com/Micua/Git.git
// 查看现有的远端列表
$ git remote -v
```

## 将本地仓储的提交记录推送到远端的master分支
```
$ git push -u origin master
```

## 拉取远端master分支的更新记录到本地
```
$ git pull origin master
```

## 查看项目分支
```
$ git branch
```

## 拉取指定分支的代码
```
$ git branch -b branch-name url
```

## 创建分支并托管代码
```
$ git branch gh-pages
// 托管代码必须用这个分支
// 托管后的网页地址：sadicLiu.github.io/wjs
// CNAME用于将自己的域名绑定到GitHub
```

## 切换分支
```
$ git checkout gh-pages
```

## 删除远端分支
```
$ git push origin :gh-pages
// 冒号后面是要删除的分支名字
```

## 删除本地分支
```
$ git branch -d gh-pages
```

## 删除远端提交过的文件（如readme.md）
```
$ git rm -r readme.md
```

## 设置提交时不用输入账号密码
1.添加.gitconfig文件到用户根目录(c盘下存储配置文件的目录)
```
[user]
    name = liuhy
    email = 190978752@qq.com
[filter "lfs"]
    smudge = git-lfs smudge -- %f
    required = true
    clean = git-lfs clean -- %f
[gui]
[push]
    default = matching
[credential]
[credential]
    helper = store
```
2.https方式长期存储密码：
`git config --global credential.helper store`

## 撤销commit
如果commit之后，又不想push上去了，直接用下面的命令撤销
```
$ git log       // 查看commit日志,找到需要回退的那次commit的哈希值
$ git reset --hard commit_id    // 撤销
```

## 代码冲突
```
error: Your local changes to the following files would be overwritten by merge:
        protected/config/main.php
Please, commit your changes or stash them before you can merge.
```
1.如果希望保留本地改动，仅仅并入远程新文件
```
$ git stash
$ git pull
$ git stash pop
```
2.如果希望用代码库中的文件完全覆盖本地工作版本
```
$ git reset --hard
$ git pull
```