```
# 不更改文件强制commit
git commit --allow-empty -m "push for deploy"

# 查看历史commit
git log  # 按q退出


# 清空commit
git reset [--soft] HEAD^
# 带着新文件回到上一个版本
# HEAD~n: 上n个版本

git checkout --orphan branch_name
# 创建一个全新的分支 (没有任何文件，也没有历史commit)

git branch -D main
# 强制删除main分支

git branch -M main
# 把当前分支改名为main并作为主分支


# 修改历史版本，保留新版本
cp ../myrepo ../myrepo.old -r
cd ../myrepo.old

git log

git reset --hard commit_id
# 回到出错后的版本

git reset HEAD^
# 带着你的错误代码回到出错前
# 修改你的代码

git commit -m "xxx"
# 提交修好的代码

git push -f
# 强制更新一波

cp ../myrepo
# 回到没啥问题的新版本

git fetch -a
# 拉取刚刚推送的代码

git rebase
# 篡改历史
# 处理一下冲突，建议用图形化工具比如vscode

git commit -m "最新版又回来了"

```