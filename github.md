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
### SSH免密登录
+ 设置ssh别名：`$ git remote add origin_ssh SSH地址`
+ 远程推送：` $ git push origin_ssh master`
### Git忽略清单

将不需要的文件名字添加到此文件中，执行git 命令时就会忽略这些文件。
- git忽略清单文件名称：`.gitignore`
