# 三个概念
##### 版本库
    线上的包含了各个版本的git仓库
##### 暂存区
    将改好的，准备提交的文件， 提交到暂存区
##### 工作区
    当前的工作目录
---   
# 版本控制 
##### 配置用户名和邮箱
    git config --user.name yourName
    git config --user.email yourEmail
##### 初始化仓库，使当前目录拥有版本控制功能
    git init
##### 提交到暂存区
    1.文件名    git add 文件名1 文件名2
    2.文件夹名  git add 文件夹
    3.工作目录  git add .
    4.忽略文件/文件夹提交到暂存区。用文件.ignore
##### 提交到版本库（本地仓库）（成为一个版本）
    git commit -m '本次提交的描述'
##### 查看状态
    git status
    1. 工作区之前   commit 过的文件，如果有修改但未 add 会标红
    2. 工作区之前未 commit 过的文件，未 add 会标红
##### 查看当前分支的版本历史（reset 后看不到）
    git log
##### 重置当前的 head（指针） 到指定的 commit 版本
    git reset --hard 版本号（前七位就可以）
    1.工作区和暂存区会与仓库版本同步
##### 查看当前分支的提交历史（包含 reset 的记录）
    git reflog
##### 回滚某个版本（不是回滚到xxx）
    git revert 版本号
##### 比较差异
    git diff
# 分支
##### 查看分支
    git branch
##### 创建分支
    git branch 分支名    
##### 切换分支
    git checkout 分支名
##### 合并指定分支到当前分支
    git merge 分支名
# 远程分支
##### 配置SSH
    1. ssh-keygen -t rsa -c '你的远程仓库的邮箱'
    2. 根据配置SSH时返回的路径，找到两个rsa文件
    3. 其中.pub的公钥复制出来放到远程仓库
    4. 测试连接是否成功 ssh -T git@github.com
##### 远程仓库下载到本地
    git clone SSH地址
##### 推送本地仓库的指定分支到远程仓库
    git push 远程仓库 本地分支名
##### 拉取远程仓库的指定分支到本地仓库
    git pull 远程仓库 本地分支名 
    
    

