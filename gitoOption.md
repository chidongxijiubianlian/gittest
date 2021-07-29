git status //查看状态
git log //查看提交记录
git log --pretty=oneline //格式化log
git log --graph --pretty=oneline //查看merge图
git reset --hard commitId //将git版本回退到某个commit
git reset --hard HEAD^ //用于将已commit的修改 回退到上一个版本
git reset HEAD abc.txt //用于回退暂存区里的修改记录 可以理解成 add的逆向操作
git checkout -- abc.txt //用于撤销工作区文件的修改
git diff //查看工作区与版本库里面的区别
git diff HEAD --xxx.txt //查看某个文件工作区与版本库的区别
git checkout -- xxx.txt //让工作区撤销更改 保持和暂存区一致git checkout -- file命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令，我们在后面的分支管理中会再次遇到git checkout命令。
git remote add origin https://github.com/chidongxijiubianlian/gittest.git //将已有的本地目录仓库关联远端并且推送
git remote set-url origin https://chidongxijiubianlian:xxxx@github.com/chidongxijiubianlian/gittest.git
git remote rm origin //删除本地仓库和远端的关联
git push origin --set-upstream dev //从远端创建 dev分支
git push origin --delete dev //从远端删除dev分支
git clone git@github.com:chidongxijiubianlian/gitskills.git //从远端clone仓库 不需要加用户名密码i
git branch dev //创建分支dev
git swich dev //新版本支持使用swich创建新分支 避免和撤销操作混淆
git checkout dev //将header 指向dev 使用dev分支
git checkout -b dev //使用dev分支并创建它
git checkout -b dev origin/dev //使用远端的dev分支 来创建本地的dev分支
git branch -d dev //删除dev分支
git branch //查看分支列表 带*的属于当前分支
git branch -a //能展示远端分支
git branch --set-upstream-to=origin/dev dev //如果本地与远端分支无联系 需要建立关联
git merge dev //将dev分支合并到当前分支
git stash //将当前修改暂存一下 这个命令有点慢 感觉在拷贝什么
git stash list //查看当前 保存的列表
git stash pop //相当于unstash 并删除
git cherry-pick commitID //将某个提交 合并到当前分支 局部merge
git pull //从远端分支拉取更新
git rebase //将提交历史修改为一条直线 方便观看而已
git tag v1.0.0 //创建一个tag
git tag show v1.0.0 //查看tag的详情
git tag //查看tag列表
git tag -a v1.0.0 -m "提交的内容" //创建有提交内容的tag
git tag -d v1.0.0 //删除本地tag
git push origin v1.0.0 //提交本地tag到远端
git push origin :refs/tags/v1.0.0 //删除远端tag
