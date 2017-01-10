初始化 git init
添加文件到Git仓库：
	1 git add <file>	//可以反复使用，添加多个文件
	2 git commit
查看工作区状态 git status
	git diff 查看修改内容
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id
git log 查看提交历史，以便确定要回退到哪个版本。
git reflog 查看命令历史，以便确定要回到未来的哪个版本。
删除文件 git rm

全局
git config --global user.name "yyyy"
git config --global user.email "xxx@xxx.com"

远程仓库
	创建ssh $ ssh-keygen -t rsa -C "youremail@example.com"
	关联到远程仓库并拉取 
		1 git remote add origin git@github.com:cnfanhua/TESTGIT.git	//关联github仓库
		2 git pull --rebase origin master	//拉取内容
	添加文件到仓库
		git push origin master
	克隆仓库
		git clone <address> //address -> git@github.com:cnfanhua/blog.git
	创建并切换分支
		git checkout -b dev
		切换分支
			git checkout master
	查看当前分支
		git branch
	合并分支到master
		切换回master 然后执行命令 git merge dev //dev为分支名
		
git checkout . #本地所有修改的。没有的提交的，都返回到原来的状态
git stash #把所有没有提交的修改暂存到stash里面。可用git stash pop回复。
git reset --hard HASH #返回到某个节点，不保留修改。
git reset --soft HASH #返回到某个节点。保留修改
