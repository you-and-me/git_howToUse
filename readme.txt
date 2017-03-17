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

三：删除文件
1、git rm 文件名	删除提交了、未修改的文件