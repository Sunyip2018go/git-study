# 一、git 入门
摘自：[Github常用命令](https://funteas.com/topic/5ad7ebae230d1e5e25e45b4d)
> Workspace：工作区(编辑区)

> Index/Stage 暂存区(git add推送的地方)

> Repository 仓库区(本地仓库)

> Remote 远程仓库

## 创建版本库

```git init``` 当前目录新建git仓库

```git init [project-name]``` 新建目录，将其初始化为git仓库

## 下载远程项目

```git clone [url]```

## 增加/删除文件

```git add [file1] [file2]``` 添加指定文件到暂存区


```git add [dir]``` 添加指定目录到暂存区，包括子目录


```git add .``` 添加当前目录的所有文件到暂存区


```git add -p``` 同一文件多处变化，分次提交

```git rm [file1] [file2]``` 删除工作区文件，并将这次删除放入暂存区

```git mv [file-origin] [file-renamed]``` 改名文件，并将文件放入暂存区

## 代码提交
```git commit -m [message]``` 提交暂存区到仓库

 ```git commit [file1] [file2] ... -m [message]```提交暂存区指定文件到仓库

 ```git commit -a``` 提交工作区自上次commit之后的变化至仓库

 ## 分支

 ```git branch``` 列出所有分支

 ```git branch -r``` 列出所有远程分支

 ```git branch -a``` 列出所有本地分支和远程分支

 ```git branch [branch-name]``` 新建分支，停留在当前分支

 ```git checkout -b [branch-name]``` 新建分支并切换后新建分支

 ```git checkout [branch-name]``` 切换分支

 ```git checkout -``` 切换到上一分支

 ```git merge [branch-name]``` 合并分支到当前分支

 ```git cherry-pick [commit]``` 选择一个commit合并到当前分支

```git branch -d [branch-name]``` 删除分支

```git push origin --delete [branch]``` 删除远程分支

## 远程同步

```git fetch [remote]``` 下载远程仓库所有变动

```git remote -v``` 显示所有远程仓库

```git remote show [remove]``` 显示某个仓库信息

```git remote add [short-name] [url]``` 增加一个新的远程仓库，并命名

```git pull [remote] [branch]``` 拉取远端代码，并与本地合并

```git push [remote] [branch]``` 推送本地代码至远端分支

# 二、.gitignore配置


### 匹配规则
> **"#"**：表示注释

> **"!"**：非

> **"/"**：目录层级

> **"*"**：通配符

#### 举个栗子

```

```/src```     忽略根目录下的src文件夹

```*.log```    忽略所有.log文件

```src/```     忽略src下所有的文件夹及文件

```!/src/js``` 不忽略根目录下的src文件夹下的js文件夹
```


# 三、VS Code中使用git

VS Code默认自带git，点击侧边栏中间图标进入git界面：

![git按钮](http://p7gy79w3b.bkt.clouddn.com/git-button.png)

界面中1为当前分支，2为变更的文件：

![git界面](http://p7gy79w3b.bkt.clouddn.com/git-interface1.png)

鼠标移动到变更的文件上，右侧出现3个按钮，点击＋：

![git界面](http://p7gy79w3b.bkt.clouddn.com/git-interface2.png)

然后输入提交信息，点击提交：

![git界面](http://p7gy79w3b.bkt.clouddn.com/git-interface3.png)

最后点击提交按钮旁边的三个小点，找到推送，点击




