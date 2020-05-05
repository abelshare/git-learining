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

1. 已修改：表示修改了文件，但还没保存到数据库中。
2. 已暫存：表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。
3. 已提交：表示数据已经安全地保存在本地数据库中。
4. 已推送：表示已經同步至運程服務器中。

![git](./img/state.png)  
 工作目录，暂存区域，以及本地仓库

## GIT 常用命令

### 初始化

```bash
# 在当前目录新建一个Git代码库
git init

# 新建一个目录，将其初始化为Git代码库
$ git init [project-name]

# 下载一个项目和它的整个代码历史
$ git clone [url]

# 给本地仓库加一个远程的仓库，一般用於第一次提交
git remote add origin [url]
```

### 常規

```bash

# 將所有文件添加至暫存區
git add [cmd|file]




git commit
git status
git reset
git tag
git log
```

### 分支管理

git branch
git checkout
git checkout -b branchName
git merge
git rebase
git revert

### 遠程操作

git push
git pull
git fetch

## 常見問題

1、沖突解決：

2、暫存提交回滾：

3、提交提交回滾：

sourcetree 介紹對應命令

## 工具

https://learngitbranching.js.org/?NODEMO