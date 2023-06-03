提交流程
git add . 添加未提交文件
git commit "msg" 提交文件到本地
git pull 拉取remote仓库
git push 提交代码到remote仓库

git revert HEAD 撤销指定的commit,有提交记录 再git push
git rebase --onto <branch name>~<first commit number to remove> <branch name>~<first commit to be kept> <branch name>  删除相应提交记录Psync
git add .
git rebase --continue

git status 查看提交状态
git diff   diff文件的修改
git fetch --all  拉取远端代码
git fetch -p     拉取远程分支

branch
git version  当前git版本
git branch   查看本地所有分支
git branch -r  查看所有远程的分支
git branch -a  查看所有远程分支和本地分支
git branch -d <branchname> 删除本地branchname分支

git branch <branchname>    创建branchname分支
git checkout <branchname>  切换分支到branchname
git checkout -b <branchname>  等同于执行上两步，即创建新的分支并切换到该分支

git checkout -- xx/xx  回滚单个文件
git push origin -d <branchname>  删除远程分支

merge
git merge origin/develop  merge到develop，本地merge之后 push
git merge origin/master   merge到master
git pull origin master  从远程获取最新版本并merge到本地
git push origin master  本地merge到远程master
git merge --abort  终止本次merge 并回到merge前状态

log
git log 所有提交记录
git log xx 查看xx文件的commit记录
$ git log -p xx   查看xx文件每次提交的diff
git show 查看最后一次修改

回滚
git reset --hard HEAD  回滚到指定版本，并且清空工作目录
git reset --soft HEAD  回滚到指定版本，同时保留工作目录和暂存区的内容，并把重置的位置所导致的新的文件差异放进暂存区
git reset --mixed HEAD 默认）回滚到指定版本，同时保留工作目录的内容，并清空暂存区

仓库
git remote  查看远程仓库地址
更改仓库方案1
git remote rm origin 删除仓库地址
git remote add origin ssh://git@aaaaaaaa:10022/ddddd.git 添加关联新的远程仓库
更改仓库方案2
git remote set-url origin ssh://git@aaaaaaaa:10022/ddddd.git 设置远程仓库地址b