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

  git log
  git reflog

  git rebase  // 变基 让多个版本进行合并
  git rebase -i HEAD~3   //  改为s 与上一个版本进行合并

  git merge  // 合并    冲突
```
## 添加一个HTML文件