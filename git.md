# Git安装

- 资源管理器内单击鼠标右键选择 `Git Bash Here`

- 输入`git --version` 检查是否安装成功

  # 分区简介

| 工作区 Working Directory  | 暂存区                 | Git仓库 Git Repasitory |
| ------------------------- | ---------------------- | ---------------------- |
| 对文件进行添加 改动的动作 | 临时存放已经修改的文件 | 最终确定文件           |

#Git使用前的配置

#### 配置用户姓名和邮箱

######配置姓名 `$ git config --global user.name xxxx`
######配置邮箱 `$ git config --global user.email xxxx@xxxx.com`
###### 查看配置是否成功 `$ git config --list`

###### `git init` 初始化git仓库  默认为隐藏文件夹 做一次就好

#### 提交步骤

###### `git status` 查看文件状态

###### `git add `把文件从工作区添加到缓存区

| 语法   | 添加一个或多个文件  |
| ------ | ------------------- |
| 语法一 | git add name        |
| 语法二 | git add name1 name2 |
| 语法三 | git add.name        |

###### `git commit -m 注释内容` 提交至版本库

###### 查看版本提交记录 `git log`

######建议用这个`git log --pretty=oneline `

#### 版本回退

1. 查看需求版本的commit id     git log --pretty=oneline 

2. 退回操作   git reset --hard  name  （name最少前四位）

#### 版本恢复

1. 查看历史操作   git reflog 
2. 恢复操作   git reset --hard name

- 用暂存区中的文件覆盖工作目录中的文件：`git checkout -- 文件名` 不加 `-- 文件名`则覆盖全部文件
- 将文件从暂存区中删除：`git rm --cached 文件名`
- 将git仓库中指定的更新记录恢复出来，并且覆盖暂存区和工作目录：` git reset --hard commitID`

#### 修改git commit信息中的author

1. 使用 --amend 修改 author：

   `git commit --amend --author '用户名<邮箱@xxx.com>'`

2. 输入`git rebase --continue `结束修改

## Git进阶

### 分支

生成副本，避免影响开发主线

#### 分支细分

1. 主分支（master）：第一次向git仓库提交更新记录时自动产生的一个分支。
2. 开发分支（develop）：作为开发的分支，基于master分支创建。
3. 功能分支（feature）：作为开发具体功能的分支基于开发分支创建。

#### 分支命令

- `git branch` 查看分支
- `git branch 分支名称` 创建分支
- `git checkout 分支名称` 切换分支
- `git merge 来源分支` 合并分支
- `git branch -d 分支名称` 删除分支（分支合并后才允许被删除）（-D 大写强制删除）

注意：

 开发分支文件后要commit后再切换主分支，否则分支文件会出现在主分支里面。

### 暂时保存更改

git中可以不提交更改，只提取分支上所有改动并储存，让开发人员得到一个干净的副本，临时转向其它工作。复制到“剪切板”，可以“粘贴“到其它分支。

场景：

- 储存临时改动：`git stash`
- 恢复临时改动：`git stash pop`