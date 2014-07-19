# 关于仓库

# 关于SSH KEY, 检查用户目录下是否有.ssh目录, 如果有检查有没有id_rsa和id_rsa.pub,
# 如果没有, 请执行'ssh-keygen -t rsa -C "myemail@example.com"', id_rsa.pub是公钥,请在github网站上配置

# 在现有项目目录下

git init # 对当前项目git化(就是使用git管理)

git remote # 远程库
	git remote # 显式所有远程库
	git remote add gitname remotegitaddress # 添加一个远程库起个别名叫gitname

git status # 显式当前仓库内文件的状态

git diff filname # 查看文件filename修改前后的不同

git log # 显式最近到最远的提交日志
	git log --pretty=oneline # 只显示commit id和commit
	git log --graph --pretty=oneline --abbrev-commit # 显式不同分支提交的轨迹图

git checkout
	git checkout -- filename # 丢弃工作区中对filename的修改, 返回到最近一次'git commit'或'git add'时的状态
	git checkout -b branchname # 创建分支branchname, 并切换到这个分支
	git checkout branchname # 切换到分支branchname

git branch 
	git branch # 查看分支
	git branch name # 创建分支name

git merge anotherbranch # 合并anotherbranch到当前分支, 会出现冲突

git reset # 恢复到其他版本
	git reset --hard HEAD^ # 恢复到上一次, HEAD^^恢复到上上一次, 以此类推, 也可以使用数字如: HEAD~100
	git reset --hard commitid # 恢复到指定版本
	git reset HEAD filename # 将stage中的修改撤销回工作区, 然后可以用'git checkout -- filename'来撤销修改

git rm filename # 删除一个文件

git reflog # 显式每一次命令, 通过他找到commit id

git add filename # 将文件添加入版本控制

git commit -m 'say something' # 提交

git clone ****.git [name] # 克隆到本地, 以name命名文件夹,或者git库名

# 工作目录下的文件分两种状态: 已跟踪或未跟踪. 已跟踪文件是指本来就被纳入版本控制管理的文件

git push # 上传到远程库
	git push -u remotegit branch # 将本地库上传到remotegit的branch分支, '-u'选项是为了关联本地master和远程master, 第一次用, 以后就不用了
