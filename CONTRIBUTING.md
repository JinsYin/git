# 如何贡献

## 运行

```sh
# 安装 node.js 和 npm
$ node --version # v13.2.0
$ npm --version  # 6.13.7

# 安装 gitbook 实用程序，用于安装和使用多个版本的 GitBook
$ npm install -g gitbook-cli@2.3.2

# 检查版本
$ gitbook --version
CLI version: 2.3.2
GitBook version: 3.2.3

# 安装 book.json 自定义的插件（安装到 node_modules/ 目录）
$ gitbook install [./]

# 构建静态文件到 _book/ 目录，服务 http://localhost:4000
$ gitbook serve
```

## 贡献方式

* 遇到问题？ -> 开一个 Issue
* 修正错误、提交功能？ -> 提交一个 PR

## 提交 PR

1. 在本项目仓库页面的右上角中点击「Fork」按钮派生该项目到您的 Github 账号
2. 克隆您的项目到本地：`git clone https://github.com/<yourname>/knowledge-base.git`
3. 创建一个新分支并贡献您的内容：`git checkout -b <branch-name>`
4. 提交您新增或修改的内容：`git add . && git commit -m "..."`
5. 将新分支推送到您的 Github 仓库：`git push origin <branch-name>:<remote-branch-name>`
6. 在您的 Github 仓库中发起一个 Pull Request
7. 必要时可以到本项目仓库创建一个 [issue](https://github.com/JinsYin/knowledge-base/issues/new) 来描述此次 PR
