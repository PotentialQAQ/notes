# Github

### 创建仓库

######                 尽量使用SSH，但是要安装OpenSSH

###### https不方便，每次都需要密钥

### 使用

- 克隆远程仓库到本地：`git clone 仓库地址`
- 提交暂存区 git add 
- 提交本地仓库 git commit -m”   注释  "
- 提交线上仓库 git push
- 拉取线上仓库
- 删除别名：` git remote remove 远程仓库地址别名`
- 第一件事git pull  最后一件事 git push

#### 拉取远程仓库中最新版本

- 拉取远程仓库最新版本到本地：` git pull 远程仓库地址 分支名称`

1. `fork`到自己的远程仓库
2. `clone`到本地进行修改
3. `push`到远程仓库
4. `pull request`发送给原作者
5. 原作者查看`commit` 审核
6. 原作者 `merge pull request`

### SSH免密登录

+ 生成密钥：` ssh-keygen`

+ 密匙储存目录：` C:\User\用户\\.ssh`

+ 公钥名称：` id_rsa.pub`

+ 私钥名称：` id_rsa`

+ 设置ssh别名：`$ git remote add origin_ssh SSH地址`

+ 远程推送：` $ git push origin_ssh master`

### Git忽略清单

将不需要的文件名字添加到此文件中，执行git 命令时就会忽略这些文件。

- git忽略清单文件名称：`.gitignore`
- 将工作目录所有文件添加到缓存区：` git add .`

### 为仓库添加说明

在仓库根目录添加`readme.md`文件即可
