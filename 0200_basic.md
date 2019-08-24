# git config

## 系统中所有用户都可以使用该配置

- `git config --system`
- 配置文件所在位置: `/etc/gitconfig`

## 当前用户可以使用该配置

- `git config --global`
- 配置文件所在位置: `~/.gitconfig`

## 当前项目可以使用该配置

- `git config`, 该命令必须在.git文件夹内使用
- 配置文件所在位置: `project/.git/config`

## 配置内容

- 配置用户名: `git config --global user.name sadicLiu`
- 配置邮箱: `git config --global user.email 190978752@qq.com`
- 配置编译器: `git config core.editor sublime`
- 查看配置信息: `git config --list`










