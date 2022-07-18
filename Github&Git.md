# 新手够用指南

[教学视频链接](https://www.bilibili.com/video/BV1e541137Tc)

### Git和Github分别是什么

Git是一个运行在你电脑上的版本控制软件，而Github是基于Git这个版本控制软件打造的网站

Git的三个概念：提交commit,仓库repository,分支branch

### 看别人的Github项目

- git clone

  - Code处有一个地址，复制地址

  - 新建或打开一个文件夹，想把别人的文件下载到这里，右键点击git bash here

  - 在黑框里输入命令 git clone 再把刚刚的地址粘贴进去，回车star

- README.md

- issue

- LICENSE

### 基础命令

```Bash
git clone 仓库链接 # 克隆拉取仓库
git checkout 分支名 # 切换指定分支
git add . # 添加当前目录所有文件
git commit -m "提交信息" # 提交add的文件，并附带提交信息
git push # 上传到云端
git pull # 将云端的数据同步到本地
```

### 特殊的查找资源的小技巧

直接在github的搜索栏上搜

- 找百科大全 awesome×××
- 找例子 ×××
- 找空项目架子××× starter/××× boilerplate
- 找教程 ××× tutorial



# 流畅上Github

[教学视频链接]( [『教程』手把手教你流畅访问Github_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1Aq4y1q7hr?vd_source=6a2926e545cb5de5c4783370b83446a4) )

### 利用某大厂的网游加速器

- 打开uu网易加速器登录
- 在搜索框搜索学术，点开学术资源
- 此时会自动在浏览器中打开学术资源的窗口
- 我们新增一个页面上github就好了

- 用完在加速器处停止加速，

### 使用开源软件steam++

风险自负



# Git入门

[教学视频链接]( [Git快速入门：20分钟学会Git 80%操作_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1i44y1e7hv?spm_id_from=333.337.search-card.all.click&vd_source=6a2926e545cb5de5c4783370b83446a4) )

### 为什么需要git?

手动进行版本管理太复杂了，尤其是多个人的时候

### 常规操作

- 创建 repository------创建一个文件夹，文件的更改都会被监控
- 将更改commit到本地git------保存文件夹此时的快照到本地的git
- 恢复到某个commit--------将文件夹恢复到之前保存的某个快照
- push和pull操作--------同步本地git和云端git的内容
- 使用分支--------将当前文件夹从copy一份再做更改
- 常用工作流---------分支的使用方式

### 创建repository

#### 法一

- 在github中的个人主页的repository中，点击new
- 利用git clone把它下载到本地 ，即可生成带git的文件夹

#### 法二

- 直接在文件夹处git init初始化

### 将更改commit到本地git

- Git status -------查看修改的状态
- Git add . ---------指定此次commit包含的文件
- Git commit -a -m  “注释”-------完成一次到本地的git的commit（多commit有利于回滚之前版本）
- 没设置名字会提醒 设置名字
  -  git config --global user.email "you@example.com"
  - git config --global user.name "Your Name"

### 恢复到某个commit

- Git log 看一下之前的commit
- Git reset --hard  id 恢复到某个commit

### push和pull 操作

- Git push origin---------将本地内容同步到云端
-  Git pull---------从云端拉取内容

### 使用分支

- Git branch 新branch名称 --------创建新branch（相当于复制一份内容到分支里）
- Git checkout --------切换分支
- git checkout b 名字 ---------创建并切换分支
- Git merge 分支名 --------合并分支
- Git branch -d 分支名--------删除分支



# Github上传

- 在github中创建repository仓库
  - 个人主页的setting的repository
  - new
- 创建本地仓库
  - 新建文件夹,输入命令行git init
  - 将想提交的文件添加到仓库中（add和commit)

- 关联远程仓库，输入命令`git remote add origin 网址(github上新建仓库的ssh网址)`

- 上传本地代码，输入命令`git push -u origin 新建的文件名称`
- 添加分支
  - 创建分支`git branch 分支名称`
  - 切换分支`git checkout 分支名称`
  - 将想提交的文件添加到分支中（add和commit)
  - 上传分支`git push origin master:分支名称`
- 如何提交pr(pull requests)
  - ssh git clone项目
  - 在项目中创建分支，在分支中修改代码
  - 提交修改的文件(status查看，add,commit上传)
  - 提交到远程GitHub上，命令`git push --set-upstream origin 分支名称`
  - 切换到主分支，将分支代码合并到主分支
    - `git checkout master`
    - `git merge 分支名称`
    - `git add .`
    - `git commit -m"名称“`
    - `git push origin master`
  - 提交pr申请
    - 进入项目中，点击pull requests
    - 点击create pull requests
    - 提交到对应分支确认提交