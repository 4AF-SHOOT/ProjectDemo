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




  git add .
  git commit -m 'bala'
  git push 
  git pull
  git push 


  git tag v1.0
  git tag -a v1.0 -m 'bala'
  git tag -a v1.0 be1f31e3bd
  git push origin v1.0



```