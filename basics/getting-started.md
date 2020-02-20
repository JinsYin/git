# Git 入门

## 版本控制

版本控制系统（VCS）记录项目文件的变化情况（包括文件的内容、权限），以便将来可以将某个文件甚至整个项目回退到之前的状态（概括为 “回溯”），亦或者追踪不同修订版本的文件差异（概括为 “追踪”）。

| 演变历史 | 代表                   | 描述                                                                                                                                                                                                                                                |
| -------- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 无       | ~                      | 复制项目目录以保存不同的版本。简单方便，但难以管理                                                                                                                                                                                                  |
| 本地式   | [RCS][rcs]             | 采用简单的本地数据库来记录文件的历次更新差异                                                                                                                                                                                                        |
| 集中式   | [CVS][cvs]、[SVN][svn] | 单一的中央服务器保存所有文件的修订版本，协同工作者使用客户端连接服务器，以提交更新或者拉取最新文件。<br/> 1. 集中式版本管理服务器，存在单点故障问题 <br/> 2. 具备文件版本管理和分支管理功能 <br/> 3. 集成效率高 <br/> 4. 客户端必须时刻和服务器相连 |
| 分布式   | [Git][git]             | 服务端和客户端均保存完整的版本历史，各端均可以独立进行版本管理                                                                                                                                                                                      |

[rcs]: https://www.gnu.org/software/rcs/
[svn]: https://subversion.apache.org/
[cvs]: https://nongnu.org/cvs
[git]: https://git-scm.com/

## 安装 Git

Linux：

```sh
# Ubuntu
$ sudo apt-get install -y git

# CentOS
$ sudo yum install -y git
```

验证检查：

```sh
$ git --version
git version 2.20.1
```

## 参考

* [A short history in Version Control Systems – RCS, ClearCase, SVN, Git](https://blog.codecentric.de/en/2016/11/a-short-history-in-version-control-systems-rcs-clearcase-svn-git/)
