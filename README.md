# GIT基礎教程

## GIT 介紹

Git 是一個開源的分佈式版本控制系統，可以有效、高速地處理從很小到非常大的項目版本管理。  

![git](./img/git.png)  

![git](./img/info.png)  
Workspace：工作區  
Index / Stage：暫存區  
Repository：倉庫區（或本地倉庫）  
Remote：遠程倉庫  

## GIT 四種狀態

1. 已修改：表示修改了文件，但還沒添加到暫存區中。
2. 已暫存：表示修改了文件，已添加到暫存區中。
3. 已提交：表示文件已經安全地保存在本地倉庫中。
4. 已推送：表示已經同步至遠程服務器中。

![git](./img/state.png)  
工作區，暫存區，倉庫區

## GIT 常用命令

### 初始化

git init
```bash
# 在當前目錄新建一個Git代碼庫
git init

# 新建一個目錄，將其初始化為Git代碼庫
git init [project-name]
```

git clone [url]
  
```bash
# 下載一個項目和它的整個代碼歷史
git clone [url]
```

git remote add origin [url]

```bash
# 增加一個新的遠程倉庫，並命名
git remote add origin [url]
```

### 常規

git add [cmd|file]

```bash
#提交新文件(new)和被修改(modified)文件，不包括被刪除(deleted)文件
git add .

#提交新文件(new)和被修改(modified)文件，不包括被刪除(deleted)文件
gid add -u

#提交所有變化
git add -A

#提交指定文件
git add [file1] [file2]
```

git commit [cmd] ：將文件提交至本地倉庫

```bash
#將文件提交至本地倉庫並添加說明
git commit -m "message"

#將文件（包括沒有執行`add`命令的文件）提交至本地倉庫並添加說明
git commit -a -m [message]

#可以修改上一次的提交信息。
git commit --amend -m "message"

#2. 可以將最近的修改追加到上一次的提交上。
git commit --amend
```

git status

```bash
# 顯示有變更的文件
git status
```

git reset

```bash
# 重置暫存區的指定文件，與上一次commit保持一致，但工作區不變
git reset [file]

# 重置暫存區與工作區，與上一次commit保持一致，危險
git reset --hard

# 重置當前分支的指針為指定commit，同時重置暫存區，但工作區不變
git reset [commit]

# 重置當前分支的HEAD為指定commit，同時重置暫存區和工作區，與指定commit一致
git reset --hard [commit]

# 重置當前HEAD為指定commit，但保持暫存區和工作區不變
git reset --keep [commit]
```

git tag [cmd]

```bash
# 列出所有tag
git tag

# 新建一個tag在當前commit
git tag [tag]

# 新建一個tag在指定commit
git tag [tag] [commit]

# 刪除本地tag
git tag -d [tag]
```

git log

```bash
# 顯示當前分支的版本歷史
git log

# 顯示當前分支簡約版的歷史
git log --pretty=oneline
```

### 分支管理

git branch

```bash
# 列出所有本地分支
git branch

# 列出所有遠程分支
git branch -r

# 列出所有本地分支和遠程分支
git branch -a

# 新建一個分支，但依然停留在當前分支
git branch [branch-name]

# 新建一個分支，並切換到該分支
git checkout -b [branch]
```

git checkout

```bash
# 恢復暫存區的指定文件到工作區
git checkout [file]

# 恢復某個commit的指定文件到暫存區和工作區
git checkout [commit] [file]

# 恢復暫存區的所有文件到工作區
git checkout .
```

git merge

```bash
# 合併指定分支到當前分支
git merge [branch]
```
  
git cherry-pick

```bash
# 選擇一個commit，合併進當前分支
git cherry-pick [commit]
```

### 遠程操作

git push

```bash
# 上传本地指定分支到远程仓库
$ git push [remote] [branch]
```

git pull

```bash
# 上传本地指定分支到远程仓库
$ git push [remote] [branch]
```
1. git fetch：

## 常見問題

1、沖突解決

2、提交回滾

## 工具

https://learngitbranching.js.org/?NODEMO