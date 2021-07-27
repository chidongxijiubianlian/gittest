git status //查看状态
git log //查看提交记录
git log --pretty=oneline //格式化log
git reset --hard commitId //将git版本回退到某个commit
git reset HEAD abc.txt //用于回退暂存区里的修改记录 可以理解成 add的逆向操作
git checkout -- abc.txt //用于撤销工作区文件的修改
git diff //查看工作区与版本库里面的区别
git diff HEAD --xxx.txt //查看某个文件工作区与版本库的区别
git checkout -- xxx.txt //让工作区撤销更改 保持和暂存区一致git checkout -- file命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令，我们在后面的分支管理中会再次遇到git checkout命令。
git remote add origin https://github.com/chidongxijiubianlian/gittest.git //将已有的本地目录仓库关联远端并且推送
git remote set-url origin https://chidongxijiubianlian:xxxx@github.com/chidongxijiubianlian/gittest.git
git clone git@github.com:chidongxijiubianlian/gitskills.git //从远端clone仓库 不需要加用户名密码
git branch dev //创建分支dev
git swich dev //新版本支持使用swich创建新分支 避免和撤销操作混淆
git checkout dev //将header 指向dev 使用dev分支
git checkout -b dev //使用dev分支并创建它
git branch -d dev //删除dev分支
git branch //查看分支列表 带*的属于当前分支
git merge dev //将dev分支合并到当前分支
