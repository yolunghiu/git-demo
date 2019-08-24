# 版本控制

## 回到之前版本

1. `git reset --hard HEAD^`, HEAD后的^数量代表回退到上几个版本
2. `git reset --hard commit_id`, 使用commit号前7位即可, commit号通过 `git log` 查看
3. `git reflog` 可以查看所有commit的id, 包括由于版本回退后 `git log` 看不到的id

## 创建标签

1. 创建新的标签: `git tag v1.0`, 默认在最新的commit_id处打标签
2. 添加标签信息: `git tag v1.0 -m "message"`
3. 指定某个commit_id打标签: `git tag v0.9 [commit_id]`

## 查看标签

1. 列出当前所有标签: `git tag`
2. 显示标签具体信息: `git show v1.0`

## 删除标签

- `git tag -d v1.0`

## 去往某个标签版本

- `git reset --hard v0.9`












