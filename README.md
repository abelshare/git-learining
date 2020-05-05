# GIT基礎教程

## GIT 介紹

Git 是一个开源的分布式版本控制系统，可以有效、高速地处理从很小到非常大的项目版本管理。

![git](./img/git.png)  

![git](./img/info.png)
Workspace：工作区  
Index / Stage：暂存区  
Repository：仓库区（或本地仓库）  
Remote：远程仓库

## GIT 四种状态

1. 已修改：表示修改了文件，但还没保存到仓库中。
2. 已暫存：表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。
3. 已提交：表示数据已经安全地保存在本地仓库中。
4. 已推送：表示已經同步至運程服務器中。

![git](./img/state.png)  
工作区，暂存区，仓库区

## GIT 常用命令

### 初始化

1. git init  
  在当前目录新建一个Git代码库

2. git init [project-name]  
  新建一个目录，将其初始化为Git代码库

3. git clone [url]  
  下载一个项目和它的整个代码历史

4. git remote add origin [url]  
  给本地仓库加一个远程的仓库，一般用於第一次提交

### 常規

1. git add [cmd|file] ：將文件添加至暫存區  
  cmd：  
   `.`：提交新文件(new)和被修改(modified)文件，不包括被删除(deleted)文件  
   `-u`：提交被修改(modified)和被删除(deleted)文件，不包括新文件(new)  
   `-A`：提交所有变化  
  file：指定文件名

2. git commit [cmd] ：將文件提交至本地倉庫
   cmd：  
   `-m [message]`：將文件提交至本地倉庫并添加說明  
   `-a -m [message]`：將文件（包括沒有執行`add`命令的文件）提交至本地倉庫并添加說明  
   `-- amend`：  
      1. 可以修改上一次的提交信息。
      2. 可以将最近的修改追加到上一次的提交上。

3. git status：查看當前工作區狀態

4. git reset  

5. git tag [cmd]
   cmd：  
   `[tag]`：新建一个tag在当前commit  
   `[tag] [commit]`：新建一个tag在指定commit  
   `-d [tag]`：删除本地tag  
6. git log：显示当前分支的版本历史

### 分支管理

1. git branch [branch]：新建分支  

2. git checkout [cmd]  
  cmd：  
   `[branch-name]`：檢出指定分支  
   `-b [branch-name]`：創建新的分支并檢出  

3. git merge  [branch-name]：合并指定分支到当前分支
  
4. git cherry-pick [commit]：合并进当前分支

### 遠程操作

1. git push：
2. git pull：
3. git fetch：

## 常見問題

1、沖突解決：

2、暫存提交回滾：

3、提交提交回滾：

## 工具

https://learngitbranching.js.org/?NODEMO