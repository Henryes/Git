# git协作流
- 创建一个新分支
- 创建一个新版本
- 开启一个Pull Request  拉取请求

# Git
- 提交但是没有同步到Github时撤销的方法:undo
- 提交之后撤销的方法： revert this commit
- 回滚到某一版本的方法：roll back to this commit
- add为添加本地的项目
- create是创建一个新项目
- clone为把repository的项目下载到本地
- changes为被修改的文件
- 搜索文件快捷键：T

# Git分支
- 创建项目页面：创建gh-pages分支，然后写页面
-  访问项目页面：用户名.github.io/项目名
-  将新创建的分支合并到default分支，把master分支上去，就是合并分支
-  merge commit  和 rebase 有区别

# 提交github
- 配置ssh key值 
- git config --global user.name "用户名"， git config --global user.email "邮箱地址"
- cd ~/.ssh，来检测是否生成过key,没有生成过key
- ssh-keygen -t rsa -C “邮箱地址”
- 找文件id_rsa.pub  粘贴到key里面
- ssh  -T git@github.com确定配置成功
- git remote add origin git@github.com:yourName/yourRepo.gitwison。yourName是用户名，yourRepo.gitwison是要上传项目的仓库
- git add +文件名
- 提交项目，输入git commit -a -m "chan"   chan是标记谁上传
- 输入git push origin master 可以在GitHub查看项目
- 更新项目，先添加文件，再提交，更新前最好用git pull origin master更新一下
- ls：查看目录中问文件
- git show:显示某次提交的内容
- ![](1.PNG）：编辑README.md的内容，添加图片

# Git错误
> fatal: remote origin already exists

- 先输入git remote rm origin
- 还错找gitconfig文件删掉[remote "origin"]那一行


> Permission denied (publickey).


- 因为新生成的key不能加入ssh就会导致连接不上github
- 先输入$ ssh-agent 再输入$ ssh-add ~/.ssh/id_key

> error:failed to push som refs to .......

- 先输入$ git pull origin master //先把远程服务器github上面的文件拉下来
- 再输入$ git push origin master
- 再报错git remote add origingit@github.com:chan/git

# git 本地创建
- $ makdir ~/hello-world    //创建一个项目hello-world
- $ cd ~/hello-world       //打开这个项目
- $ git init             //初始化
- $ touch README
- $ git add README        //更新README文件
- $ git commit -m 'first commit'     //提交更新，并注释信息“first commit”
- $ git remote add origin git@github.com:defnngj/hello-world.git     //连接远程github项目
-  $ git push -u origin master     //将本地项目更新到github项目上去





