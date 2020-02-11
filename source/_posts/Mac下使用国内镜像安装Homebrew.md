---
title: Mac下安装Homebrew
author: Alan
top: false
cover: true
toc: true
mathjax: false
summary: Mac下安装Homebrew及替换homebrew源
categories: Mac
tags:
  - Mac
  - Homebrew
abbrlink: 32623
date: 2020-01-07 09:25:00
---

## 安装

#### 获取install文件并编辑

```bash
cd ~
curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install >> brew_install
```
#### 编辑brew_install文件

```bash
#!/System/Library/Frameworks/Ruby.framework/Versions/Current/usr/bin/ruby
# This script installs to /usr/local only. To install elsewhere you can just
# untar https://github.com/Homebrew/brew/tarball/master anywhere you like or
# change the value of HOMEBREW_PREFIX.
HOMEBREW_PREFIX = "/usr/local".freeze
HOMEBREW_REPOSITORY = "/usr/local/Homebrew".freeze
HOMEBREW_CACHE = "#{ENV["HOME"]}/Library/Caches/Homebrew".freeze
HOMEBREW_OLD_CACHE = "/Library/Caches/Homebrew".freeze
#BREW_REPO = "https://github.com/Homebrew/brew".freeze
BREW_REPO = "git://mirrors.ustc.edu.cn/brew.git".freeze
#CORE_TAP_REPO = "https://github.com/Homebrew/homebrew-core".freeze
CORE_TAP_REPO = "git://mirrors.ustc.edu.cn/homebrew-core.git".freeze
```

#### 注释掉

```bash
BREW_REPO = "https://github.com/Homebrew/brew".freeze和
CORE_TAP_REPO = "https://github.com/Homebrew/homebrew-core".freeze
```

#### 修改为

```bash
BREW_REPO = "git://mirrors.ustc.edu.cn/brew.git".freeze和
CORE_TAP_REPO = "git://mirrors.ustc.edu.cn/homebrew-core.git".freeze
```

注意： 新版本HomeBrew可能没有CORE_TAP_REPO这句代码，如果没有不用新增。 如果这个镜像有问题的话，可以换成其他源。

#### 执行脚本

打开终端允许脚本

```bash
/usr/bin/ruby brew_install
```

如果此时脚本应该停在

```bash
==> Tapping homebrew/core

Cloning into '/usr/local/Homebrew/Library/Taps/homebrew/homebrew-core'...
```

出现这个原因是因为源不通，代码来不下来，解决方法就是更换国内镜像源： 手动执行下面这句命令，更换为中科院的镜像：

```bash
git clone git://mirrors.ustc.edu.cn/homebrew-core.git/ /usr/local/Homebrew/Library/Taps/homebrew/homebrew-core --depth=1
```

然后把homebrew-core的镜像地址也设为中科院的国内镜像

```bash
cd "$(brew --repo)"

git remote set-url origin https://mirrors.ustc.edu.cn/brew.git

cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"

git remote set-url origin https://mirrors.ustc.edu.cn/homebrew-core.git
```

执行更新，成功：

```bash
brew update
```

最后用这个命令检查无错误：

```bash
brew doctor
```

至此HomeBrew就安装完成了。

## 替换homebrew源

#### 替换homebrew默认源

```bash
cd "$(brew --repo)"
git remote set-url origin git://mirrors.ustc.edu.cn/brew.git
```

#### 替换homebrew-core源

```bash
cd "$(brew --repo)/Library/Taps/homebrew/homebrew-core"
git remote set-url origin git://mirrors.ustc.edu.cn/homebrew-core.git
```

#### 设置 bintray镜像

```bash
echo 'export HOMEBREW_BOTTLE_DOMAIN=https://mirrors.ustc.edu.cn/homebrew-bottles' >> ~/.bash_profile
source ~/.bash_profile
```