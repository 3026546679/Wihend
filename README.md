# 切换仓库
git checkout main
# 创建仓库
git checkout --orphan
#  创建完毕，如果默认继承了master tree，这时需要清除索引和工作树，继续执行：
git rm -rf . // 注意后面的点

git branch // 会展示master
 
git status // 查看状态，是否有需要提交

# 这里假设新分支名称为：next-branch
 
git add .
git commit -m 'next-branch commit'
git push origin next-branch
 
// 此时已经完成新分支next-branch的推送