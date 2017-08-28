---
title: Git学习记录-版本回退
date: 2017-08-23 23:29:04
tags: "Git"
---

## Git的版本管理
上一篇记录了学习`Git`的安装，版本库的创建，这篇博客将记录一下`Git`的版本管理。
<!--more-->

修改文件后，提交至版本库的操作与添加文件一样，都是需要先`add`这个或者这几个文件，然后`commit`。

每一次修改提交文件，就相当于玩游戏时候的存盘一样，会生成一个新的存档，如果后面死档了，或者卡关，可以读档到某一个阶段继续游戏。`Git`也是一样，当发现文件误删除或者代码误修改后可以回退到某个版本。

使用 `git log` 查看最近几次的提交版本
```code
  $ git log
    commit 8d3f94b6d2b42616da55eecca84007e8d548e6b8 (HEAD -> master, origin/master, origin/HEAD)
    Author: lawliet7911 <lawliet7911@gmail.com>
    Date:   Wed Aug 23 18:22:28 2017 +0800

        add theme rar file 

    commit 7eedb9f95bb3aecbc116a893fc4c59e70d5a93de
    Author: lawliet7911 <lawliet7911@gmail.com>
    Date:   Wed Aug 23 17:53:45 2017 +0800

        add tags

```

未完。。。
