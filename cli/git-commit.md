# git commit

## 选项

| 参数      | 说明                                                                        |
| --------- | --------------------------------------------------------------------------- |
| `-a`      | 将已追踪文件的修改和删除添加到提交，但不包括新文件                          |
| `--amend` | 启动 Git 的默认编辑器修正当前分支最近一次提交的 CommitMessage，并提交暂存区 |
| `-m`      | 指定 commit message 。如果是多行，可以不用 `-m`                             |

## 用例

| 用例                     | 描述                                                                                                                                   |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------- |
| `git commit --amend`     | 启动 Git 的默认编辑器修正当前分支最近一次提交的 CommitMessage；无论是否有改动，最终都会生成新的 CommitID；该命令会将暂存区中的文件提交 |
| `git commit -a --aemond` | 提交已追踪文件的更改，并启动 Git 的默认编辑器修正当前分支最近一次提交的 CommitMessage；无论是否有改动，最终都会生成新的 CommitID       |

## 提交规范

用途：

* 从 commit 生成 changelog

提交之前：

```sh
# 统一文件权限
$ find . -type f -not -path .git -exec chmod 644 {} \; # 常规文件
$ find . -type d -not -path .git -exec chmod 755 {} \; # 目录

# 末尾添加新行（Git 要求）
$ find . -type f -not -path .git -name "*.md" -exec sed -i -e '$a\' {} \;    # Linux
$ find . -type f -not -path "./.git/*" -name "*.md" -exec sed -i '' -e '$a\' {} \; # macOS

# MacOS 删除 .DS_Store（最好事先添加到 .gitignore）
$ find . -type f -not -path .git -name ".DS_Store" -exec rm {} \;
```

## 技巧

* 创建 “原子提交” 有利于追踪 BUG 以及回滚

## 示例

* 修改最新 commit 的 message

```sh
git init e1 && cd e1
echo "README" > README.md
git add . && git commit -m "README"
```

```sh
$ git log --oneline
a9c0935 (HEAD -> master) README
```

```sh
$ git commit --amend
Document # 修改后的 message
```

```sh
# Commit ID 和 message 都不相同
$ git log --oneline
b03da2e (HEAD -> master) Document
```

## 参考

* [你可能会忽略的 Git 提交规范](http://jartto.wang/2018/07/08/git-commit/)
* [Commit message 和 Change log 编写指南](http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)
* [github.com/tj/git-extras](https://github.com/tj/git-extras)
* [github.com/conventional-changelog/conventional-changelog](https://github.com/conventional-changelog/conventional-changelog/)
