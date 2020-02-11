---
title: Mac上如果看不到.git目录的解决方法
author: Alan
top: false
cover: true
toc: true
mathjax: false
summary: Mac上如果看不到.git目录的解决方法
categories: Mac
tags:
  - Mac
  - Git
abbrlink: 47567
date: 2020-01-14 23:50:58
---

Mac OS X上，如果需要查看.git目录下的隐藏文件,打开一个Terminal终端窗口，输入：

```bash
defaults write com.apple.finder AppleShowAllFiles TRUE
```

然后重启Finder，输入：

```
killall Finder
```

如果你完成了需要的操作，恢复隐藏设置，同样打开Terminal终端窗口，输入：

```bash
defaults write com.apple.finder AppleShowAllFiles FALSE
```

然后重启Finder，输入：

```bash
killall Finder
```





