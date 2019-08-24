# git basic

## git工作流程

工作区 --(add)--> 暂存区 --(commit)--> 本地仓库  ↔  远程仓库

## `git add [file]`

- 将文件提交到暂存区
- 可同时提交多个文件, 文件名用空格分隔
- `*` 表示所有文件, `.` 表示当前目录下的文件

## `git rm --cached [file]`

- 删除暂存区某个文件提交记录

## `git commit -m "msg"`

- 将暂存区的文件提交到本地仓库

## log

- `git log`: 查看详细日志
- `git log --pretty=oneline`: 查看简单格式的日志输出

## 工作区常用命令

- 查看本地仓库文件(commit过的)和当前工作区文件的区别: `git diff [file]`
- 从本地仓库恢复文件: `git checkout [file]`

## 本地仓库文件的移动和删除

- 移动文件: `git mv [file] [dir]`
- 删除文件: `git rm [file]`
**这两个命令是同时在工作区和本地仓库操作**




 

