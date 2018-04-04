SVN是集中式版本控制系统
GIT是分布式版本控制系统，每台电脑就是一个完整的版本库，工作时就不需要联网了；将各自的修改推送给对方就可以互相看到对方的修改了。

一：创建新的git版本库
1、进入你创建的文件夹 -> shift+右键 -> Git Bash Here -> 输入命令：git init

二：把文件添加到版本库
1、git add 文件名/*      //将文件添加到暂存区
2、git commit -m "代码提交信息"     //将文件提交到仓库，引号内的是注释
3、git status       查看是否有文件未提交
4、git diff 文件名      查看文件修改了什么
注：文件修改后，要执行1/2两步才能提交。

5、git log         查看历史记录
   git log -pretty=online       查看简洁的历史记录
   q 	
6、git reset -hard HEAD^        回退到上个版本
   git reset -hard HEAD^^       回退到上上个版本
   git reset -hard HEAD~100        回退到前100个版本
7、git reflog         回退后，查看回退前的版本
8、git checkout -- 文件名	撤销未放到暂存区的内容
9、cat 文件名		查看文件内容

三：删除文件
1、git rm 文件名	删除提交了、未修改的文件

四：远程仓库
1、把本地仓库的内容推送到 github 仓库
如果你还没有克隆现有仓库，并欲将你的仓库连接到某个远程服务器，你可以使用如下命令添加：
	git remote add origin git@github.com:you-and-me/test-use.git
注意：上传 github 之前，要先 pull 一下，（把 github 上创建的仓库拉到本地）执行如下命令：
	git pull origin master
		      
如果远程库是空的，我们第一次推送 master 分支时，要加上 –u 参数，Git 不但会把本地的 master 分支内容推送的远程新的 master 分支，还会把本地的 master分支和远程的 master 分支关联起来，在以后的推送或者拉取时就可以简化命令。
	git push -u origin master
如果远程仓库不是空的，只需 git push origin master

2、将远程库克隆到本地库     git clone git@github.com:you-and-me/test-use.git	

五：创建与合并分支
1、git checkout -b 分支名	-b 表示创建并切换到分支，等价于如下两条命令：
   git branch 分支名		创建分支
   git checkout 分支名		切换到分支

   git branch 			查看分支，当前分支前面会添加一个星号。

2、git merge 分支名		合并指定分支到当前分支上
   git merge -no-ff -m "注释" 分支名		使用带参数 –no-ff来禁用”Fast forward”模式，避免删除分支后丢掉分支信息

3、git branch -d 分支名		删除分支

4、git stash			将当前工作现场隐藏起来
   git stash list		查看工作现场
   git stash apply		恢复
   git stash drop		删除stash内容
   git stash pop		恢复并删除stash内容

六：多人协作
1、git remote		查看远程库信息
   git remote -v	查看远程库的详细信息
2、git push origin master	Git 会把 master 分支推送到远程库对应的远程分支上	

关于修改远程git仓库的代码
前提： 已经关联远程仓库，且在本地仓库内
    1、使用 git pull --no-ff （拉取远程仓库代码，不快进合并步骤）
    2、然后就进入了 vim文件， 修改冲突地方
    3、然后 git push origin master 上传代码就好了（可以把master换成你想要推送的分支）

