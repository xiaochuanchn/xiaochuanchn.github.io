---
title: Mac使用git向github提交代码
author: Alan
top: false
cover: true
toc: true
mathjax: false
summary: Mac使用git向github提交代码
categories: Git
tags:
  - Mac
  - Git
abbrlink: 26150
date: 2020-01-15 15:18:11
---

#### 第一步：安装git程序

git客户端程序地址：[https://git-scm.com/download/mac](https://link.jianshu.com?t=https%3A%2F%2Fgit-scm.com%2Fdownload%2Fmac)

> 打开安装包，如下图操作
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-5137c085990af965.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

然后按照提示，下一步下一步，直到安装完成。

> 打开终端，输入命令：git --version  ，测试是否安装成功  。
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-924a8c3fbc072693.png?imageMogr2/auto-orient/strip|imageView2/2/w/496/format/webp)

#### 第二步：创建SSH

###### 步骤一：在终端输入命令：cd ~/.ssh

> 如果出现 -bash: cd: /Users/glamor/.ssh: No such file or directory，说明之前没有用过，直接进入步骤二。如果之前用过需要清理原来的rss，
>  终端输入命令：mkdir key_backup $ cp id_rsa* key_backup $ rm id_rsa*
>
> 
>
> 打印结果如下图：
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-df5d8f4a7f5a1d9d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1070/format/webp)

###### 步骤二：终端输入命令：ssh-keygen -t rsa -C [285442768@qq.com](https://link.jianshu.com?t=mailto%3A285442768%40qq.com)

> (邮箱是GitHub的注册邮箱)一直回车，直到Overwrite(y/n)?,输入y,一直回车
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-2a9f3dee4160f77a.png?imageMogr2/auto-orient/strip|imageView2/2/w/1086/format/webp)
>
> 这里的Overwrite是因为之前生成过ssh，所以，会提示是否覆盖 。

确认完毕后，程序将生成一对密钥存放在以下文件夹：/users/用户/.ssh/
 密钥分成两个文件，一个私钥（id_rsa）、一个公钥（id_rsa.pub）。
 私钥保存在您的电脑上，公钥交项目负责人添加到服务器上。用户必须拥有与服务器公钥所配对的私钥，才能访问服务器上的代码库。
 【注意！】为了项目代码的安全，请妥善保管你的私钥！因为一旦私钥外泄，将可能导致服务器上的代码被泄漏！

#### 第三步：向GitHub上设置自己的公钥

###### 步骤一：复制公钥

> 执行命令：pbcopy < ~/.ssh/id_rsa.pub  将公钥的内容复制到内存里。

###### 步骤二：登录GitHub,按下图顺序操作

> ![img](https:////upload-images.jianshu.io/upload_images/3779438-e92fb2869d21c12f.png?imageMogr2/auto-orient/strip|imageView2/2/w/494/format/webp)
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-85ff5a1950a57b0e.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)
>
> 
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-f8e1c91a79c66a40.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)
>
> 
>
> 若是多次设置公钥则下图所在位置
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-0ce396f04dfb652d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

###### 步骤三： 测试连接是否成功

> 在终端输入命令：ssh -T [git@github.com](https://link.jianshu.com?t=mailto%3Agit%40github.com)
>  连接成功如下图：
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-1db82cd3039bb1b6.png?imageMogr2/auto-orient/strip|imageView2/2/w/1146/format/webp)
>
> 第一次设置公钥时测试连接
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-cb148fe09a00e2fc.png?imageMogr2/auto-orient/strip|imageView2/2/w/1146/format/webp)
>
> 设置公钥时测试连接

#### 第四步：在github下建自己的Repository。

> 创建过程如下图顺序：
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-763164b947761c30.png?imageMogr2/auto-orient/strip|imageView2/2/w/510/format/webp)
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-5040b7ade42157ad.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)
>
> 
>
> 创建成功如下图：
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-72c498d81868ab4c.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

#### 第五步：通过git上传代码到github

在GitHub上的这个wangjdemo仓库还是空的，GitHub告诉我们，可以从这个仓库克隆出新的仓库，也可以把一个已有的本地仓库与之关联，然后，把本地仓库的内容推送到GitHub仓库。

现在想把本地的wangjdemo项目通过git上传到github上。

| 步骤 | 终端命令                                            | 作用                                |
| ---- | --------------------------------------------------- | ----------------------------------- |
| 1    | git init                                            | 给X项目创建Git仓库                  |
| 2    | git add *                                           | 把X项目文件添加到Git仓库            |
| 3    | git commit -m “注释”                                | 把X项目文件提交到Git仓库            |
| 4    | git remote add origin SSH key(SSH key：根据项目定)  | 添加远程库                          |
| 5    | git pull origin master - -allow-unrelated-histories | ef                                  |
| 6    | git push -u origin master                           | origin：github上的对应项目;提交分支 |

说明：以上所有的终端命令都是在要上传项目的根目录下进行的；

###### 步骤一：在wangjdemo项目目录下创建Git仓库

- 终端输入命令：cd 项目目录 ，跳转到项目目录，
- 终端输入命令：git init，瞬间Git就把仓库建好了，而且告诉你是一个空的仓库（empty Git repository）

> ![img](https:////upload-images.jianshu.io/upload_images/3779438-e629ecf8686376d8.png?imageMogr2/auto-orient/strip|imageView2/2/w/1138/format/webp)

- 终端输入命令：ls -all，看到这个目录下的内容

> ![img](https:////upload-images.jianshu.io/upload_images/3779438-658d19174dc26df8.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)
>
> 当前目录下多了一个.git的目录，这个目录是Git来跟踪管理版本库的，没事千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。如果你没有看到.git目录，那是因为这个目录默认是隐藏的，用ls -ah命令就可以看见。
>  注意：也不一定必须在空目录下创建Git仓库，选择一个已经有东西的目录也是可以的。我这个目录有项目存在。

###### 步骤二：把wangjdemo项目文件添加到Git仓库

> 终端输入命令：
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-5dbc21fac8d67217.png?imageMogr2/auto-orient/strip|imageView2/2/w/156/format/webp)
>
> 终端没有任何显示，说明添加成功
>  说明：用命令git add告诉Git（可以使用git add file git add /* 或者 git add *），把文件添加到仓库， git add可反复多次使用，添加多个文件。执行git add *，没有任何提示，说明添加成功。
>
> 使用命令git add *  会错误如下图
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-d57bba656538c242.png?imageMogr2/auto-orient/strip|imageView2/2/w/918/format/webp)

###### 步骤三：把wangjdemo项目文件提交到仓库

> 终端输入命令：git commit -m "注释"
>
> 
>
> 如下图所示，表示commit成功。 
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-61e4f5478da8798d.png?imageMogr2/auto-orient/strip|imageView2/2/w/1138/format/webp)

###### 步骤四：添加远程库

在本地的wangjdemo仓库下： 终端输入命令：
 git remote add origin [git@github.com](https://link.jianshu.com?t=mailto%3Agit%40github.com):sexyhair79/wangjdemo.git

> 没有任何提示，表示添加远程库成功。
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-eca088d2c0a07dc6.png?imageMogr2/auto-orient/strip|imageView2/2/w/1140/format/webp)
>
>  说明：命令的格式：git remote add orgin SSH Key ；
>  origin是Git对远程库的默认叫法，可以更改，是SSH Key的别名；
>  SSH Key是需要去GitHub上对应项目的【Clone or download】复制的。

###### 步骤五：把本地库的所有内容推送到远程库上

终端输入命令：git pull origin master --allow-unrelated-histories

> 出现下图：
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-891f669d86bfe17a.png?imageMogr2/auto-orient/strip|imageView2/2/w/1172/format/webp)

输入“:wq”退出输入终端，终端显示如下：

> ![img](https:////upload-images.jianshu.io/upload_images/3779438-9833378afabea499.png?imageMogr2/auto-orient/strip|imageView2/2/w/1026/format/webp)

查看项目目录会发现存在REANME.md文件；

终端输入命令：git push -u origin master

> 提交成功如下图
>
> ![img](https:////upload-images.jianshu.io/upload_images/3779438-e2f79de8e9f8f96f.png?imageMogr2/auto-orient/strip|imageView2/2/w/940/format/webp)

把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。 由于远程库是空的，我们第一次推送master分支时，加上了-u参数。Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令,直接使用git push origin master。

刷新GitHub上的对应的项目会发现有内容列表了。

### 错误

> ![img](https:////upload-images.jianshu.io/upload_images/3779438-33b5ca0c76efe7cf.png?imageMogr2/auto-orient/strip|imageView2/2/w/1140/format/webp)
>
> 原因：远程库里存在我本地库没有的文件。

> 设置别名的时候，出现“fatal: remote origin already exists.”错误,说明该别名已经存在，可以另外建一个别名，或者使用“git remote rm origin”命令删除原来的别名，然后重新执行“git remote add origin [git@github.com](https://link.jianshu.com?t=mailto%3Agit%40github.com):yourname/xxxx.git”；

> 在提交的时候，出现“error: failed to push some refs to '[git@github.com](https://link.jianshu.com?t=mailto%3Agit%40github.com):xxx/xxx.git' hint: Updates were rejected because the remote contains work that you do not have locally....”的错误，说明有冲突，远程仓库的版本比本地仓库的要信，所以要先进行更新，才能提交。使用“git pull [git@github.com](https://link.jianshu.com?t=mailto%3Agit%40github.com):xxx/xxx.git”命令进行更新，地址自己相应替换掉。

