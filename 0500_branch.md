# Branch相关操作

## 查看当前分支

- `git branch`

## 创建分支

- `git branch [branch_name]`

## 切换工作分支

- `git checkout [branch]`

## 分支合并

- 将某个分支合并到当前分支: `git merge [branch]`
- 合并过程中如果没有冲突, 合并后当前分支即为干净状态
- 如果产生冲突则需要手动选择, 然后再进行add, commit操作
- 在创建分支前尽量保证当前分支是干净的, 以减少冲突发生

## 删除分支

- `git branch -d [branch_name]`, 删除已经合并的分支
- `git branch -D [branch_name]`, 强制删除没有合并的分支






