#Git的常用命令

#查看

      git show # 显示某次提交的内容
   
#提交

      git add <file> # 将工作文件修改提交到本地暂存区

      git add . # 将所有修改过的工作文件提交暂存区
#删除

      git rm <file> # 从版本库中删除文件

      git rm <file> --cached # 从版本库中删除文件，但不删除文件

#查看提交记录

      git log git log <file> # 查看该文件每次提交记录

      git log -p <file> # 查看每次详细修改内容的diff

#Git 本地分支管理

#查看、切换、创建和删除分支

      git br -r # 查看远程分支

      git br <new_branch> # 创建新的分支

      git co <branch> # 切换到某个分支

      git co -b <new_branch> # 创建新的分支，并且切换过去

      git br -d <branch> # 删除某个分支

#Git暂存管理

      git stash # 暂存

      git stash list # 列所有stash

      git stash apply # 恢复暂存的内容

      git stash drop # 删除暂存区

#Git远程分支管理

      git pull # 抓取远程仓库所有分支更新并合并到本地

      git fetch origin # 抓取远程仓库更新
      
      git push # push所有分支

      git push origin master # 将本地主分支推到远程主分支

      git push -u origin master # 将本地主分支推到远程(如无远程主分支则创建，用于初始化远程仓库)

      git push origin <local_branch> # 创建远程分支， origin是远程仓库名

      git push origin <local_branch>:<remote_branch> # 创建远程分支

      git push origin :<remote_branch> #先删除本地分支(git br -d <branch>)，然后再push删除远程分支

#Git远程仓库管理

      git remote -v # 查看远程服务器地址和仓库名称

      git remote show origin # 查看远程服务器仓库状态

      git remote add origin git@ github:robbin/robbin_site.git # 添加远程仓库地址

      git push -u origin master # 客户端首次提交

