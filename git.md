# git
1. 开源的分布式的版本管理工具
2. 了解svn 集中式的版本管理工具
    + 分布式：任意一台主机都可以充当版本库，实际开发中仍然有一台主机充当中央服务器的角色
    + 集中式：只有一台主机充当版本库，其他的没有
# git本地版本库创建时的一些常见命令
1. git init 初始化一个本地仓库 路径后面会多一个master标识 master时版本库的一个默认分支
2. git add filename 把某个文件添加到版本库（暂存区）
3. git commit -m "message" 将文件修改提交到版本库
4. git status 测试命令  查看工作区和版本库当前的状态 
5. git diff 测试命令 查看文件修改的内容
6. git log 测试命令 查看提交日志（提交版本历史记录）
7. git reset --hard HEAD^ 回退命令(回退到上次提交的版本)
8. git reset --hard commitID 回退到指定的版本
9. git reflog 查看版本改变的历史记录
10. git restore 文件名 撤销工作区的修改
11. git restore --staged 文件名 撤销暂存区的修改
12. rm 文件名 从工作区删除文件
13. git rm 文件名 从本地版本库中删除文件
14. 创建远程库
    + $ ssh-keygen -t rsa -C "youremail@example.com" 生成密钥
    + 把密钥放到GitHub账号下的ssh里
    + $ git remote add origin git@github.com:github地址
    + git push -u origin master 推到远程仓库（第一次推送，之后推送只需git push）
15. git checkout -b dev  创建并切换到dev分支上(checkout)   -b参数表示创建并切换
    git switch -c dev   创建并切换到dev分支上(switch)(git checkout dev 切换分支)   -c参数表示创建并切换
    + 相当于以下两条命令:
    + git branch dev    新建分支dev
    + git checkout dev  切换到dev分支
16. git branch  查看当前分支，当前分支前面会标一个*号
17. git merge dev   将dev分支合并到master上
18. git branch -d dev   删除分支dev