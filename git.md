# Git —— The Super Useful Version Control System

### How To Update and Download Files Between Local Disk And Github By Git ?

#### often-used commands
1. git init   //初始化本地仓库
2. git add .   //添加当前目录所有文件到git缓存区
3. git commit -m "some notes"   //提交，引号里填写注释
    - 注：如果本地Git刚安装，或者使用了另一台电脑，则需要在commit之前配置git user信息，示例如下：
    - git config --global user.email example@126.com
    - git config --global user.name zhangsan
4. git remote add origin https://github.com/coderben2017/Tasks-of-IFE   //关联github远程仓库
5. git push -u origin master   //本地仓库上传到远程仓库（-u表示当前为默认Git分支，如果失败可以加-f表示强制上传，覆盖远程仓库内容）

#### all commands
- git init   //初始化仓库
- git add readme.txt   //添加文件到git缓存区
- git commit -m "some notes"   //提交，引号里填写注释
- git diff readme.txt   //查看某个文件提交的不同
- git status   //查看本地仓库的状态
- git log   //查看仓库日志
- git log --pretty=oneline   //查看日志并且日志一行显示
- git reset HEAD        // 用于撤销上一次git add操作
- git reset <commit-id> // 用于撤销某一次git commit操作（回退本地版本库到某一次commit）
- git reset HEAD  readMe.txt   //撤销某一文件的git add操作，^是上一次，~100前100次
- git reset HEAD^ readMe.txt
- git reset HEAD~100 readMe.txt
- git reflog   //查看仓库日志（比log全，比如版本回退时造成的数据丢失)
- git reset --hard 3628164   //版本回退到某个id对应的版本
- git remote add origin https://github/repo-name.git   //关联远程仓库
- git push -u origin master   //本地仓库上传到远程仓库, -u
- git push origin master   //上传
- git pull origin master   //下载更新
- git clone git@github.com:michaelliao/gitskills.git   //克隆仓库
- git branch    //查看本地所有分支
- git branch -a //查看本地+远程所有分支
- git branch dev   //创建一个名为dev的分支
- git checkout dev   //将当前本地库切换到dev分支
- git checkout -b dev //创建一个名为dev的分支，并且将当前本地库切换到dev分支
- git merge dev   //将dev分支与master分支合并
- git branch -d dev   //将dev分支删除
- git log --graph   //命令可以看到分支合并图
- git checkout -b <本地分支名> origin/<远程分支名>    // 拉取远程分支并建立本地分支，同时建立映射关系

### Update Information
- 2018-12-14 9:55
- by CoderBen
