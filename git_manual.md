# git日常使用总结
1. git init 初始化git项目
2.	git commit -m “”   把文件提交到版本库
3.	git status   当前版本库情况
4.	git add …   把文件添加到版本库,修改后提交新文件
5.	git diff <>           查看different
6.	git log   查看历史修改信息  （加—pretty=oneline查看简短信息）
7.	HEAD表示当前版本   HEAD^表示前一版本
8.	git reset --hard HEAD^ 返回上一版本
9.	git reflog 查看历史命令
10.	在工作区放到缓存区前：add之前发现错误可以用git checkout -- file丢掉工作区修改
11.	修改已经放到缓存区（已经add但没commit）：git reset HEAD file撤销掉缓存区修改
12.	文件删掉后用git rm <file>删掉文件，用git checkut -- <file>恢复文件
13.	要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
14.	关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
15.	此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；
克隆一个仓库：git clone + SSH的url
16. git分支的使用 
  + 查看分支 git branch
  + 创建分支 git branch <name>
  + 切换分支 git checkout <name>
  + 创建加切换分支 git checout -b <name>
  + 合并某分支到当前分支 git merge <name>
  + 删除分支 git branch -d <name>
## 实际正常使用的步骤
1. 初始化git项目 git init
2. git add 将修改添加到版本库
3. git commit 将修改提交到版本库
4. git remote add origin https:// http://7881188.cn/自己的仓库url地址 将本地项目和远程项目关联
5. git push -u origin master 将代码上传到远程仓库  
第一次上传有可能会遇到push失败的情况，那是因为跟SVN一样，远程仓库上有一个README.md 文件没有下载下来 。我们得先
git pull --rebase origin master  ，然后执行git push -u origin master 就可以了。
# 学习总结
&nbsp;&nbsp;上面写出了git常用的很多命令，但对于我们正常使用来说，下面的5条命令是我们基本每次都要使用的，上面的某些可能会比较少用到，可以在我们需要的时候来查表，对于安卓开发这种需要对大量的代码来进行管理的项目，git简直是太方便了。无论是团队协作还是个人项目的管理，git都极大的方便了我们。