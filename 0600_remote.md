# 远程仓库相关操作

## 添加远程仓库

- `git remote add origin [url]`, 默认使用SSH作为传输手段
- 删除远程主机: `git remote rm origin`

## 将本地分支推送到远程

- `git push -u origin master`
- 在第一次向远程仓库推送时需要加 `-u` 选项, 之后就不需要了

## 从远程仓库拉取分支

1. 直接拉取远程分支和当前工作分支合并: `git pull origin dev` 
(如当前在 `master` 分支, 拉取后直接将 `dev` 和 `master` 合并了)
2. 拉取远程分支到本地, 不合并: `git pull origin dev(远程分支名): dev(本地分支名)`

## 代码推送和拉取

1. 将本地代码推送到远程仓库: `git push`
2. 当本地版本低于远程版本时, 可以使用如下命令覆盖远程版本: `git push --force origin`
3. 从远程仓库更新代码: `git pull`
4. `git fetch` 功能与 `git pull` 类似, 只是 `git fetch` 相当于是从远程获取最新到本地, 
不会自动merge. `git pull` 从远程获取最新版本并merge到本地. 在实际使用中 `git fetch` 更安全一些.










