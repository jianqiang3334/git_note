###工作目录下的文件分两种状态:
> 已跟踪或未跟踪. 已跟踪文件是指本来就被纳入版本控制管理的文件

###SSH KEY
*检查用户目录下是否有.ssh目录, 如果有检查有没有id\_rsa和id\_rsa.pub, id\_rsa.pub是公钥,请在github网站上配置, 如果没有, 请执行:*
> ssh-keygen -t rsa -C "myemail@example.com"

###git init
> git init # 对当前文件夹git化(就是使用git管理这个文件夹)

###git remote
> git remote # 列出所有远程库别名

> git remote add gitname remotegitaddress # 为远程库起个别名gitname

###git status
> git status # 显式当前仓库内文件的状态

###git diff
> git diff filname # 查看文件filename修改前后的不同

###git log
> git log --pretty=oneline # 只显示commit id和commit

> git log --graph --pretty=oneline --abbrev-commit # 显式不同分支提交的轨迹图

###git checkout
> git checkout -- file # 丢弃工作区中对file的修改, 恢复到最近一次'git commit'或'git add'时的状态

> git checkout -b branchname # 创建分支branchname, 并切换到这个分支

> git checkout branchname # 切换到分支branchname

###git branch
> git branch # 列出所有分支

> git branch name # 创建分支name

###git merge
> git merge branch # 使用Fast-forward模式合并branch分支到当前分支, 可能会出现冲突
> git merge --no-ff -m "say something" branch # --no-ff禁用Fast-forward模式, 这样的好处是即使删除了分支branch, 在历史记录中依然可以看到这次合并

###git reset
> git reset --hard HEAD^ # 恢复到上一次, HEAD^^恢复到上上一次, 以此类推, 也可以使用数字如: HEAD~100

> git reset --hard commitid # 恢复到指定版本commitid

> git reset HEAD filename # 将stage中的修改撤销回工作区

###git rm
> git rm file # 删除一个文件

###git reflog
> git reflog # 显式历史命令, 通过他找到commit id

###git add
> git add file # 将文件添加入stage区, 就是缓冲区

###git commit
> git commit -m 'say something' # 将stage区内的修改全部更新到版本库中

###git clone
> git clone gitaddress [name] # 克隆到本地, 以name或者git库名命名文件夹

###git push
> git push -u remotegit branch # 将本地库上传到remotegit的branch分支, '-u'选项是为了关联本地master和远程master, 第一次用, 以后就不用了
