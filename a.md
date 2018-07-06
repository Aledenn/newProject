## git的简单使用
```
#新建一个a.md
touch a.md

#把a.md加入到git的暂存区中
git add .

#提交修改 其中a参数为自动把当前所有修改和删除文件放到栈上 m参数为修改信息
git commit -am "add a.md"

#把本地仓库中当前分支提交到远程仓库origin中的master分支
git push origin master

#或者上传本地所有分支代码到远程对应的分支上。
git push
```
## git标签操作
```
#本地仓库不与远程仓库合并，覆盖远程仓库master分支
git push -f origin master

#添加远程库标签
git remote add glab git@github.com:Aledenn/newProject.git

#把本地仓库推送到glab标签的地址上
git push glab master

#删除glab标签
git remote remove glab

#修改glab对应地址
git remote set-url glab git@github.com:Aledenn/newProject.git

#把glab标签改名为lab
git remote rename glab lab
```

##git分支操作
```
#创建本地库dev分支
git branch dev

#切换到dev分支
git checkout dev

#以下操作都是在dev分支中，不会影响master分支
touch b.md
git add .
git commit -am "add b.md"

#推送到origin的dev分支上
git push origin dev

#合并分支，把dev分支内容合并到当前分支
git merge dev
```

## git冲突解决
出现原因：远程仓库已经被修改
```
#先把远程仓库同步到本地仓库
git pull origin master

#修改冲突文件，删除不要的
```
