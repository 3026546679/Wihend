
https://blog.csdn.net/Jone_hui/article/details/114068497
一个Git仓库，使用分支branch管理多个不同项目product

## 按照循序走下去

git branch // 会展示master
 
git status // 查看状态，是否有需要提交

## 此时，将你想放到master的项目copy到仓库文件夹下，再执行
git add .
git commit -m 'master'
git push origin master
// 此时已经完成master主分支项目提交了
# 创建仓库
git checkout --orphan name
#  创建完毕，如果默认继承了master tree，这时需要清除索引和工作树，继续执行：
git rm -rf . // 注意后面的点
# 这里假设新分支名称为：next-branch
 
git add .
git commit -m 'next-branch commit'
git push origin next-branch
 
// 此时已经完成新分支next-branch的推送

# 切换仓库
git checkout name


# 有一些分支克隆了带有git的仓库 怎么移除

查阅来源 https://blog.csdn.net/xiebaochun/article/details/114143346

.git文件夹通常是隐藏的。您可以在终端中使用命令行来查看和删除它。
例如，在macOS上，您可以打开终端，然后使用cd命令进入到包含.git文件夹的目录，然后使用ls -a命令查看所有文件和文件夹，包括隐藏的文件夹。
您可以使用rm -rf .git命令删除.git文件夹。

1、删除文件夹里面的.git文件夹

2、执行git rm --cached [文件夹名]

3、执行git add [文件夹名]

4、执行git commit -m "msg"

5、执行git push origin [branch_name]


