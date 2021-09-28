# git
```
  git config
  git clone
  git add ./README.md
  git add .   // 添加所有文件到暂存区中
  git commit -m 'comment/msg'

  git status  // 监听 查看当前工作区状态
  git checkout -- ./README.md  // 撤销工作区修改
  git reset HEAD ./index.html   // 把html文件踢出暂存区
  git reset HEAD   // 把html文件踢出暂存区 (git status)
  git reset --hard HEAD^^  // 实现版本回滚跳跃   一个^代表回退一个版本  HEAD~3 代表回退三个版本
  git reset --hard xxxx(版本号)  // 跳到指定版本
  git reset --(soft | mixed(默认) | hard) HEAD

  git log   // 日志
  git reflog   // 历史操作

  git rebase  // 变基 让多个版本进行合并
  git rebase -i HEAD~3   //  改为s 与上一个版本进行合并

  git push origin master  // 推送到远程仓库的master分支

  git diff  // 改了什么
  git diff HEAD


  分支
  git branch  // 查看分支
  git branch <name>  // 创建新分支
  git checkout <name> // 切换分支  切换分支之前要保存commit提交版本
  git checkout -b dev-q  // 创建并切换分支 
  git branch -d <name> // 删除本地分支
  git branch -D <name> // 强制删除本地分支
  git push origin --delete dev-1 // 删除远程分支

  git merge dev-s // 合并  冲突 =》可选

  git remote add origin ssh地址  // 本地仓库与远程仓库建立联系

  .gitignore


  1. git pull origin master
  2. git add, commit
  3. git push origin

  // 提取远程分支
  git checkout -t origin/optimizationV1


  git add .
  git commit -m 'bala'
  git push 
  git pull
  git push 


  git tag v1.0
  git tag -a v1.0 -m 'bala'
  git tag -a v1.0 be1f31e3bd
  git push origin v1.0


  git stash save 'msg'
  git stash pop
  git stash clear


```

### 提取远程分支
```
  // 提取远程分支
  git checkout -t origin/optimizationV1
```

### 新项目本地仓库连接远程仓库
```
  // 新项目本地仓库连接远程仓库
  git remote add origin https://github.com/4AF-SHOOT/react-demo.git
  git push -u origin master
```

### git 用户名
```
  // 设置全局用户名和邮箱及设置项目用户名和邮箱
  git config --global user.name yourname
  git config --global user.email yourname@gmail.com
  // 项目内用户名，进入到项目路径内
  git config user.name yourname
  git config user.email yourname@163.com
```

### 清除提交记录
```
  // 清除提交记录
  // 1.切换到新的分支
  git checkout --orphan latest_branch

　//　2.缓存所有文件（除了.gitignore中声明排除的）
  git add -A

　//　3.提交跟踪过的文件（Commit the changes）
  git commit -am "commit message"

　//　4.删除master分支（Delete the branch）
  git branch -D master

　//　5.重命名当前分支为master（Rename the current branch to master）
  git branch -m master

　//　6.提交到远程master分支 （Finally, force update your repository）
  git push -f origin master
```

### 配置ssh key
```
  // 1、设置全局用户名和邮箱及设置项目用户名和邮箱
  git config --global user.name yourname
  git config --global user.email yourname@gmail.com

  // 2、生成秘钥 -- 一直回车
  ssh-keygen -t rsa -C "这里换上你的邮箱"

  // 3、生成好后，复制 id_rsa.pub 的内容，进入GitHub/gitlab...，添加ssh key
  // 4、就可以clone了
```

### git stash
```
  git stash / git stash save 'msg'   // 保存当前工作进度，将工作区和暂存区恢复到修改之前。msg为说明
  git stash list  // 显示保存的工作进度列表，编号越小代表保存进度的时间越近。
  git stash pop stash@{num}  // stash@{num} 可选，恢复工作进度到工作区，此命令的stash@{num}是可选项，在多个工作进度中可以选择恢复，不带此项则默认恢复最近的一次进度相当于git stash pop stash@{0}
  git stash clear  // 删除所有保存的工作进度。
```