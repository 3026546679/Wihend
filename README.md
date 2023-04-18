
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
git checkout --orphan
#  创建完毕，如果默认继承了master tree，这时需要清除索引和工作树，继续执行：
git rm -rf . // 注意后面的点
# 这里假设新分支名称为：next-branch
 
git add .
git commit -m 'next-branch commit'
git push origin next-branch
 
// 此时已经完成新分支next-branch的推送

# 切换仓库
git checkout name
