## git几种状态：  
- untracked：未跟踪的文件，即还没有被纳入版本管理的文件。  
- unmodified：已跟踪的文件，但没有做任何修改。  
- modified：已跟踪的文件，已做了修改，但还没有暂存。  
- staged：已暂存的文件，即将提交到版本库的文件。  

## git push  
git push <远程主机名> <本地分支名>:<远程分支名>  
git push origin master:main
- 如果省略远端分支名，则表示将本地分支推送与之存在“追踪关系”的远端分支（通常两者同名），如果远端分支不存在，则会被新建。  
git push origin mster  
- 如果省略本地分支名，则表示删除指定的远端分支，因为这等同于推送一个空的本地分支到远端分支。  
git push origin :master  
- 如果当前分支和远端分支存在追踪关系，则本地分支和远端分支都可以省略。  
git push origin  
- 如果当前分支只有一个追踪分支，那么主机名都可以省略  
git push  
- 如果当前分支与多个远端分支存在追踪关系，则可以使用-u选项指定一个默认的远端分支，这样后面就可以不加任何参数使用git push。  
git push -u origin master  

## git pull  
git pull <远程主机名> <远程分支名>:<本地分支名>  
git pull origin main:master  
git pull和git clone的差别  
- git pull 必须连接远程仓库才能用，可以用于下载完整代码更新本地代码  
- git clone 只要你想往本地下载远程仓库的代码就可以用，不用连接远程仓库（连接了也可以），不适用更新本地代码  
