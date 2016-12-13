# gitskills

创建
git init 初始化git仓库
git status 查看git仓库状态
git diff <filename> 查看文件修改过的地方
git add <filename>  添加文件到暂存区
git commit -m "blablabla..." 提交文件到版本库
git commit --amend 对上一次的提交做修改

远程库操作
git remote -v 查看远程仓库
git remote add origin git@server-name:path/repo-name.git  关联远程库(github已创建)
git push -u origin master   关联后第一次推送
git push origin master   平常推送
git pull [remoteName] [localBranchName] 拉取远程仓库
git clone git@server-name:path/repo-name.git 克隆仓库

版本回退和撤销修改
git log 查看历史版本
git log --pretty=oneline 查看简要历史版本(可以查看更多版本)
git reset --hard HEAD^ 版本回退(上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100)
git reset --hard [commit id] 版本回退第二种命令， 用commit 的id 来指定版本回退
git reflog 查看命令历史, 可查看每次的命令操作 id 来进行历史操作的任意跳转(用到上面的命令)
git checkout -- <filename>  撤销文件在工作区的修改

标签
git tag 查看当前所有标签
git tag -a <tagname> -m "blablabla..." 添加新标签
git tag -d <tagname>  删除标签
git push origin :refs/tags/<tagname>  删除远程指定标签
git push origin --tags 推送所有标签到远程库

分支
git branch 查看当前所有分支
git branch <branchname> 创建分支
git branch -d <branchname> 删除分支
git checkout <branchname> 切换分支
git checkout -b <branchname> 创建分支并切换到新创建的分支
git merge <branchname>  合并<branchname>分支到当前分支
git log --graph 查看分支的合并情况
