# Learn-git

## 1.创建本地的开发分支

## 2.如果公司有自己的git，则去添加ssh秘钥，这个秘钥通常在C:\Users\Administrator\.ssh中（windows）（通常隐藏）

## 3.添加的秘钥是.pub结尾的公钥

## 4.可以使用ssh-keygen -t rsa -b 4096 -C "your_email@example.com"创建新的秘钥

## 5.其中`passphrase`为该秘钥的密码（引文），如果为空，就没有密码--免密clone git仓库

场景一.

- 使用git切换到最新的代码分支，使用git pull拉取最新代码，git完整代码为git pull oringin master
- 下载同事的新代码
  git fetch origin newremote：newlocal
  newremote远程分支的名字 mewlocal本地分支的名字
  使用git checkout 切换到自己的本地分支
  使用git merge合并本地的其他分支到当前分支
  这是git vim编辑器 如果要编辑这个内容 请输入o：换行
  i：自接进入
  输出esc 退出编辑状态
  输入：wq 保存当前记录
- git clone 命令只使用一次，下载仓库，创建与远程分支的联系
  使用git remote -v查看与远程分支的联系
  `一定要主要git仓库的文件件夹中打开当前目录，确保gitbash上面有分支的提示`

场景二.已有代码的情况

- 使用vue create命令会默认初始化一个本地的git仓库
- 使用git remote add oringin 仓库地址 回车执行
- 使用git add . 和git commit -m “ ”进行初次的提交
- 远程分支必须存在主干分支，才能创建其他分支
- oringin是远程仓库的别名
- 使用git config 来配置默认的提交用户
- git config user.name
- git config user.email

- 使用git config --global 全局配置默认提交的用户

- 如果使用vue-cli创建的仓库会默认git init

## 6`.git仓库是无穷无尽的后悔药`

- 使用git reflog 查看本地的提交记录
- 使用git reset --hard  记录id 到那个hash记录
- 未提交的文件不能进行追回

## 7.`缓存区，暂存区，本地仓库`

- git reset 会清空本地暂存区的文件，是文件不可恢复
- 使用git stash缓存不想提交的本地文件 该文件需是已跟踪的文件（已经commit）
- 使用git stash list 查看本地`跟踪``暂存``未提交`的项目
- 使用git stash apply恢复最近一条暂存记录（注意：本地存在未提交的更改，不能使用此命令）
- git stash命令不是必须使用，而是临时使用
- 如果有不想提交的文件内容，有2中方案，用git reset 命令
- git restore --staged 文件名 恢复到暂存区 如果是老版本 使用git checkout 文件名，如果不记得使用git status进行查看 

## 8.分支

- git frech获取远程更新，但是不会合并到本地分支。
- 通过git fetch origin newremote：newlocal下载最新代码

## 9.开发工作流

开发完成提交到git仓库，git仓库触发自动化流程，进行编译测试打包发布，接下来交由测试人员进行测试，然后提交到缺陷控制平台jira 或禅道，然后进行修复，然后把修护好的代码提交git，然后...，以此往复，直到发布上线。

## 10.持续集成的环节包括规划，编码，构建，测试，发布，部署，运维，监控。



> 1. 学会创建仓库，分支，提交代码
> 2. 学会回退代码
> 3. 学会合并远程分支的新的内容
> 4. 学会status, reflog, stash, remote, branch, add, commit, reset, push, pull 命令







