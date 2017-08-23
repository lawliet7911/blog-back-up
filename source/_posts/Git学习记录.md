---
title: Git学习记录
date: 2017-08-23 10:01:25
tags:
---
## 介绍
>  `Git`是一个开源的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理。`Git` 是 `Linus Torvalds` 为了帮助管理 `Linux` 内核开发而开发的一个开放源码的版本控制软件。

##### 最近学习了`Git`,在此整理一下知识点。
> 此文章的环境为`windows`

### 安装
  首先需要从[Git官网](https://git-scm.com/downloads)下载并安装，安装过程就省略了，无脑下一步就是。

  安装完成之后需要全局设置一下你的id和email，否则每次`commit`代码，都需要填写一次。命令如下：
  ```commond
   $ git config --global user.name "John Doe"
   $ git config --global user.email "email@example.com"
  ```
### 创建版本库
  在需要创建版本库的目录里：
  ```commond
   $ git init
   Initialized empty Git repository in /Users/michael/learngit/.git/
  ```
  这时git版本库就创建完成了

#### 添加文件至版本库
  若当前版本库创建完成后目录如下：
  > .git (隐藏文件，git版本控制文件)
  > readme.md
  > index.html
  此时需要把目录下需要版本控制的文件（readme.md、index.html）添加至版本库中
  先来看一下当前状态
  ```commond
    $ git status
    On branch master
    No commits yet
    Untracked files:
     (use "git add <file>..." to include in what will be committed)
        index.html
        readme.md
    nothing added to commit but untracked files present (use "git add" to track)
    ```
  此时git提示当前目录有两个未监视的文件，需要用`git add filename`添加监视。
  > `git add`可以一次添加多个文件
  
  ```commond
    $ git add readme.md index.html
  ```
  再来查看一下状态
   ```commond
    $ git status
    On branch master

    No commits yet

    Changes to be committed:
      (use "git rm --cached <file>..." to unstage)

            new file:   index.html
            new file:   readme.md

  ```
  此时文件添加完毕执行commit提交

  