SVN是集中式版本控制系统
GIT是分布式版本控制系统，每台电脑就是一个完整的版本库，工作时就不需要联网了；将各自的修改推送给对方就可以互相看到对方的修改了。

一：创建版本库
1、进入你创建的文件夹 -> shift+右键 -> 打开命令窗口 -> 输入命令：git init

二：把文件添加到版本库
1、git add 文件名       将文件添加到暂存区
2、git commit -m "xxx提交了"      将文件提交到仓库，引号内的是注释
3、git status       查看是否有文件未提交
4、git diff 文件名      查看文件修改了什么
注：文件修改后，要执行1/2两步才能提交。

5、git log         查看历史记录
   git log -pretty=online       查看简洁的历史记录
6、git reset -hard HEAD^        回退到上个版本
   git reset -hard HEAD^^       回退到上上个版本
   git reset -hard HEAD~100        回退到前100个版本
7、git reflog         回退后，查看回退前的版本
8、git checkout -- 文件名	撤销未放到暂存区的内容
9、cat 文件名		查看文件内容

三：删除文件
1、git rm 文件名	删除提交了、未修改的文件

四：远程仓库
1、把本地仓库的内容推送到github仓库
在本地仓库下运行命令：git remote add origin git@github.com:you-and-me/test-use.git
注意：上传github之前，要先pull一下，（把github上创建的仓库拉到本地）执行如下命令：
	git pull origin master
		      
由于远程库是空的，我们第一次推送master分支时，加上了 –u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
	git push -u origin master
当远程仓库不是空的时候，只需git push origin master

2、git clone git@github.com:you-and-me/test-use.git	将远程库克隆到本地库

五：创建与合并分支
1、git checkout -b 分支名	-b表示创建并切换到分支，等价于如下两条命令：
   git branch 分支名		创建分支
   git checkout 分支名		切换到分支

   git branch 			查看分支，当前分支前面会添加一个星号。

2、git merge 分支名		合并指定分支到当前分支上
   git merge -no-ff -m "注释" 分支		使用带参数 –no-ff来禁用”Fast forward”模式，避免删除分支后丢掉分支信息

3、git branch -d 分支名		删除分支

4、git stash			将当前工作现场隐藏起来
   git stash list		查看工作现场
   git stash apply		恢复
   git stash drop		删除stash内容
   git stash pop		恢复并删除stash内容

六：多人协作
1、git remote		查看远程库信息
   git remote -v	查看远程库的详细信息
2、git push origin master	Git会把master分支推送到远程库对应的远程分支上	

