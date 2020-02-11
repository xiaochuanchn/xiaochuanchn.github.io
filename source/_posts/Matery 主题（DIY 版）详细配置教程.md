---
title: Material博客主题配置说明
author: Alan
top: true
cover: false
toc: true
mathjax: false
summary: Material博客主题配置说明
categories: Markdown
tags:
  - Hexo
  - Material Design
abbrlink: 40593
date: 2020-01-07 09:25:00
---
> 这是一个采用 `Material Design` 和响应式设计的 Hexo 博客主题。

## 博客特性

- 简单漂亮，文章内容美观易读
- [Material Design](https://sitoi.cn/go.html?u=aHR0cHM6Ly9tYXRlcmlhbC5pby8=) 设计
- 响应式设计，博客在桌面端、平板、手机等设备上均能很好的展现
- 首页轮播文章及每天动态切换 `Banner` 图片
- 瀑布流式的博客文章列表（文章无特色图片时会有 `24` 张漂亮的图片代替）
- 时间轴式的归档页
- **词云**的标签页和**雷达图**的分类页
- 丰富的关于我页面（包括关于我、文章统计图、我的项目、我的技能等）
- 可自定义的数据的友情链接页面
- 支持文章置顶和文章打赏
- 支持 `MathJax`
- `TOC` 目录
- 可设置复制文章内容时追加版权信息
- 可设置阅读文章时做密码验证
- [Gitalk](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRhbGsuZ2l0aHViLmlvLw==)、[Gitment](https://sitoi.cn/go.html?u=aHR0cHM6Ly9pbXN1bi5naXRodWIuaW8vZ2l0bWVudC8=)、[Valine](https://sitoi.cn/go.html?u=aHR0cHM6Ly92YWxpbmUuanMub3JnLw==) 和 [Disqus](https://sitoi.cn/go.html?u=aHR0cHM6Ly9kaXNxdXMuY29tLw==) 评论模块（推荐使用 `Gitalk`）
- 集成了[不蒜子统计](https://sitoi.cn/go.html?u=aHR0cDovL2J1c3VhbnppLmlicnVjZS5pbmZvLw==)、谷歌分析（`Google Analytics`）和文章字数统计等功能
- 支持在首页的音乐播放和视频播放功能
- 绚丽彩虹播放器
- 全站支持 PWA
- 看板娘
- 支持`emoji`表情，用`markdown emoji`语法书写直接生成对应的能**跳跃**的表情。
- 支持 [DaoVoice](https://sitoi.cn/go.html?u=aHR0cDovL3d3dy5kYW92b2ljZS5pby8=)、[Tidio](https://sitoi.cn/go.html?u=aHR0cHM6Ly93d3cudGlkaW8uY29tLw==) 在线聊天功能。

## 使用教程

当你看到这里的时候，应该已经有一个自己的 [Hexo](https://sitoi.cn/go.html?u=aHR0cHM6Ly9oZXhvLmlvL3poLWNuLw==) 博客了。如果还没有的话，不妨使用 Hexo 和 [Markdown](https://sitoi.cn/go.html?u=aHR0cHM6Ly9zaXRvaS5jbi9wb3N0cy8xNTgxNC5odG1s) 来写博客和文章。

- 第一步，点击[这里](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL1NpdG9pL1NpdG9pLWJsb2c=) 下载博客源码到本地
- 下载到本地安装 npm 依赖包
- 第二步，修改下面的配置，DIY 你的个人博客

## 安装 npm 依赖包

下载博客源码后，进入项目根目录安装 npm 依赖包



Bash

```bash
npm install
```

### 检测 hexo 版本



Bash

```bash
hexo --version
```

输出内容：



Bash

```bash
hexo: 4.1.1
hexo-cli: 3.1.0
os: Windows_NT 10.0.18363 win32 x64
node: 13.5.0
v8: 7.9.317.25-node.23
uv: 1.34.0
zlib: 1.2.11
brotli: 1.0.7
ares: 1.15.0
modules: 79
nghttp2: 1.40.0
napi: 5
llhttp: 2.0.1
openssl: 1.1.1d
cldr: 36.0
icu: 65.1
tz: 2019c
unicode: 12.1
```

查看 hexo 版本，如果不是 `hexo: 4.1.1` 请运行如下命令



Bash

```bash
npm i hexo@4.1.1
```

> 因为 hexo 版本问题会导致博客运行报错

## 修改配置

在本主题的 `_config.yml` 中可以修改部分自定义信息，有以下几个部分：

- 博客基本信息
  - 标题
  - 副标题
  - 简介
  - 关键词
  - 作者
  - `url`
  - `favicon`
  - `Logo`
- 菜单栏
  - 基本菜单信息
  - 二级菜单配置
  - 手机二级菜单
- 博客首页的配置
  - 菜单栏右侧 Fork Me 配置
  - 轮播图配置
  - 轮播图中的第二个按钮配置
  - 个人信息
  - 首页语句
  - 首页音乐播放器
  - 首页视频播放器
  - 首页推荐文章名称和按钮配置
  - 博客分页
  - 网站显示的日期格式
  - 博客页脚信息
- 博客文章页配置
  - 文章基本信息
  - 文章字数统计
  - TOC 目录
  - 文章打赏信息
  - 复制文章内容时追加版权信息
  - MathJax
  - 配置 emoji 表情
  - 转载限制配置
  - 文章阅读密码
  - 文章分享模块
- 博客关于页配置
  - 个人信息
  - 项目信息
  - 技能信息
- 博客留言板配置
  - Gitalk
  - Gitment
  - Disqus
  - Livere
  - Valine
- 博客友链的配置
- 博客搜索的配置
- 博客特效的配置
  - 单机页面爱心效果
  - 背景 Canvas-nest
- 博客统计的配置
  - 不蒜子
  - Google Analytics
  - Baidu Analytics
  - 站长之家
- 博客其他功能配置
  - 是否每日切换背景
  - 图片懒加载
  - 网页预加载
  - 在线聊天功能
  - 绚丽彩虹播放器
  - 博客导流公众号
  - 豆瓣书单影单
  - 博客看板娘
- 博客添加 PWA 功能
- 博客其他样式配置
  - 修改主题颜色
  - 修改 banner 图和文章特色图
    默认特色图的集合。当文章没有设置特色图时，本主题会根据文章标题的 `hashcode` 值取余，来选择展示对应的特色图

### 修改博客基本信息

- `title`：网站的标题
- `subtitle`：网站副标题，默认打字效果
- `description`: 网站简介
- `keywords`：便于搜索引擎收录，分类
- `author`：网站作者
- `url`：你的网站主 `URL`（如：`https://xxx.github.io`）,如果你后期绑定了自己的域名，切记修改成你的域名。
- `favicon`：`favicon` 就是站点标签栏的小图标，选择新的图标文件覆盖即可，文件位置：`themes/matery/source/favicon.ico`
- `logo`：网站的 Logo 选择新的图标文件覆盖即可，文件位置：`themes/matery/source/apple-touch-icon.png`

#### 配置网站文章链接格式

[hexo-abbrlink 插件](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL3JvemJvL2hleG8tYWJicmxpbms=) 可以生成非中文的链接。

插件作用：自动为每篇文章生成一串数字作每篇文章的 URI 地址。每篇文章的 Front-matter 中会自动增加一个配置项：abbrlink: xxxxx，该项的值就是当前文章的 URI 地址。

执行安装命令：



Bash

```bash
npm install hexo-abbrlink --save
```

修改以下配置：



Yaml

```yaml
permalink: posts/:abbrlink.html   # 此处可以自己设置，也可以直接使用 :abbrlink.html
abbrlink:
  alg: crc16                      # 算法选项： crc16(default) and crc32
  rep: dec                        # 输出进制： dec(default) and hex
```

> 这样站点结构就变成了：域名/posts/xxx.html

### 修改博客菜单栏配置

#### 配置基本菜单导航信息

1. 菜单导航名称可以是中文也可以是英文(如：`Index` 或`主页`)
2. 图标 icon 可以在 [Font Awesome](https://sitoi.cn/go.html?u=aHR0cHM6Ly9mb250YXdlc29tZS5jb20vaWNvbnM=) 中查找



Yaml

```yaml
menu:
  Index:
    url: /
    icon: fa-home
  Tags:
    url: /tags
    icon: fa-tags
  Categories:
    url: /categories
    icon: fa-bookmark
  Archives:
    url: /archives
    icon: fa-archive
  About:
    url: /about
    icon: fa-user-circle-o
  Contact:
    url: /contact
    icon: fa-envelope
  Friends:
    url: /friends
    icon: fa-address-book
```

#### 二级菜单配置方法

如果你需要二级菜单则可以在原基本菜单导航的基础上如下操作

1. 在需要添加二级菜单的一级菜单下添加 `children` 关键字(如：`Media` 菜单下添加 `children`)
2. 在 `children` 下创建二级菜单的 名称 `name`,路径 `url` 和图标 `icon`.
3. 注意每个二级菜单模块前要加 `-`.
4. 注意缩进格式



Yaml

```yaml
menu:
  Index:
    url: /
    icon: fa-home
  Tags:
    url: /tags
    icon: fa-tags
  Categories:
    url: /categories
    icon: fa-bookmark
  Archives:
    url: /archives
    icon: fa-archive

  About:
    url: /about
    icon: fa-user-circle-o
  Contact:
    url: /contact
    icon: fa-envelope
  Friends:
    url: /friends
    icon: fa-address-book
  Media:
    #    url: /
    icon: fa-list
    children:
      - name: 影单
        url: /movies
        icon: fa-film
      - name: 书单
        url: /books
        icon: fa-book
```

#### 手机二级菜单配置



Yaml

```yaml
navMenu:
  mleft: true    #  二级侧栏子菜单是否对齐左边
  bgColor: " "   #  二级侧栏子菜单背景颜色,留空即为全局背景色
```

### 修改博客首页的配置

#### 菜单栏最右侧是否显示 fork me on github 的图标

默认为 true，你可以修改为你的仓库地址.



Yaml

```yaml
githubLink:
  enable: true                                   # 是否开启
  url: https://github.com/sitoi/sitoi.github.io  # GitHub 仓库地址
  title: Fork Me                                 # 显示文字
```

#### 首页轮播图相关配置



Yaml

```yaml
cover:
  showPrevNext: false     # 是否显示左右切换按钮
  showIndicators: false   # 是否显示指示器
  autoLoop: false         # 是否自动轮播
  duration: 120           # 切换延迟时间，默认单位 秒
  intervalTime: 5000      # 自动切换下一张的间隔时间
```

#### 首页轮播图中第二个按钮配置

首页 `banner` 中的第二个按钮的配置，包括按钮的`显示名称`、`font awesome图标`和`按钮的超链接`.



Yaml

```yaml
indexbtn:
  enable: true                     # 是否启动第二个按钮
  name: Github                     # 按钮名称
  icon: fa-github-alt              # 按钮图标
  url: https://github.com/Sitoi/   # 按钮超链接
```

#### 首页轮播图中的个人信息

`首页轮播图`中、`页脚`、以及`关于`页面都会出现的个人信息，留空即不启用



Yaml

```yaml
socialLink:
  qq: 1333397418               # QQ
  github: Sitoi                # GitHub
  facebook:                    # Facebook
  twitter:                     # Twitter
  weibo:                       # Weibo
  email: 133397418@qq.com      # 邮箱
  zhihu:                       # 知乎
  jianshu: 0289c6c3a717        # 简书
  rss: true                    # RSS 订阅       true 表示启动、false 表示关闭
  wechat: true                 # 微信好友二维码  true 表示启动、false 表示关闭
```

> 除 rss 和 wechat 外，其他的都需填写对应的信息即可

##### RSS 订阅

基于 [hexo-generator-feed](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL2hleG9qcy9oZXhvLWdlbmVyYXRvci1mZWVk) 的 Hexo 插件来做 `RSS`，安装命令如下：



Bash

```bash
npm install hexo-generator-feed --save
```

##### 微信好友二维码

需要修改微信二维码的图片，图片位置：`themes/matery/source/wechat.jpg`

#### 配置首页语句



Yaml

```yaml
dream:
  enable: true                                 # 是否开启
  showTitle: false                             # 是都显示标题
  title: 我的梦想                               # 标题内容
  text: 放弃不难，但坚持一定很酷。——《解忧杂货铺》 # 梦想语句
```

#### 配置首页音乐

要支持音乐播放，就必须开启音乐的播放配置和音乐数据的文件。

首先，在你的博客 `source` 目录下的 `_data` 目录（没有的话就新建一个）中新建 `musics.json` 文件，文件内容如下所示：



Json

```json
[{
    "name": "五月雨变奏电音",
    "artist": "AnimeVibe",
    "url": "http://xxx.com/music1.mp3",
    "cover": "http://xxx.com/music-cover1.png"
}, {
    "name": "Take me hand",
    "artist": "DAISHI DANCE,Cecile Corbel",
    "url": "/medias/music/music2.mp3",
    "cover": "/medias/music/cover2.png"
}, {
    "name": "Shape of You",
    "artist": "J.Fla",
    "url": "http://xxx.com/music3.mp3",
    "cover": "http://xxx.com/music-cover3.png"
}]
```

> **注**：以上 JSON 中的属性：`name`、`artist`、`url`、`cover` 分别表示音乐的名称、作者、音乐文件地址、音乐封面。

然后，在 `_config.yml` 配置文件中激活配置即可：



Yaml

```yaml
music:
  enable: false                 # 是否开启
  showTitle: false              # 是否显示标题
  title: 听听音乐                # 标题内容
  fixed: false                  # 开启吸底模式
  autoplay: true                # 是否自动播放
  theme: '#542674'              # 颜色
  loop: 'all'                   # 音频循环播放, 可选值: 'all', 'one', 'none'
  order: 'list'                 # 音频循环顺序, 可选值: 'list', 'random'
  preload: 'auto'               # 预加载，可选值: 'none', 'metadata', 'auto'
  volume: 0.7                   # 默认音量，请注意播放器会记忆用户设置，用户手动设置音量后默认音量即失效
  listFolded: false             # 列表默认折叠
  listMaxHeight: "197px"        # 列表最大高度
```

#### 配置首页视频



Yaml

```yaml
video:
  enable: false                                           # 是否开启视频
  showTitle: false                                        # 是否显示标题
  title: 治愈视频                                          # 标题内容
  url: https://clips.vorwaerts-gmbh.de/big_buck_bunny.mp4 # 视频超链接
  pic:                                                    # 图片超链接 
  thumbnails:                                             
  height:                                                 # 高度
  autoplay: false                                         # 是否自动播放
  theme: '#42b983'                                        # 颜色
  loop: true                                              # 是否循环播放
  preload: 'auto'                                         # 预加载，可选值: 'none', 'metadata', 'auto'
  volume: 0.7                                             # 音量大小
```

#### 配置推荐文章



Yaml

```yaml
recommend:
  showTitle: true  # 是否显示推荐文章的标题
```

#### 配置博客分页



Yaml

```yaml
index_generator:
  order_by: -date       # 排序设置 （默认按日期降序排列）
per_page: 12           # 分页，每页文章数目
pagination_dir: page   # 分页目录
```

- `per_page`：推荐使用 3 的倍数，3，6，9，12… 设置为 0 表示不分页，以瀑布流的形式展示

#### 配置网站显示日期的格式



Yaml

```yaml
date_format: YYYY-MM-DD     # 日期格式
time_format: HH:mm:ss       # 时间格式
```

#### 配置页脚信息

页脚总字数统计，激活前请确认你已经安装了 `hexo-wordcount` 插件，安装命令: `npm i --save hexo-wordcount`



Yaml

```yaml
totalCount:
  enable: true
```

站点运行开始时间配置



Yaml

```yaml
time:
  enable: true  # 是否启动
  year: 2018    # 年份
  month: 09     # 月份
  date: 24      # 日期
  hour: 00      # 小时
  minute: 00    # 分钟
  second: 00    # 秒
```

ICP 备案信息页脚显示



Yaml

```yaml
icp:
  enable: true                    # 是否启动备案信息
  url: http://beian.miit.gov.cn/  # 备案链接
  text: 沪ICP备18037784号-1          # 备案信息
```

### 修改博客文章页配置

#### 配置文章基本信息



Yaml

```yaml
new_post_name: :title.md   # 新文章的文件名称
default_layout: post       # 预设布局
auto_spacing: false        # 在中文和英文之间加入空格
titlecase: false           # 把标题转换为 title case
external_link:             # 在新标签中打开链接
  enable: true             # 在新标签中打开链接
  field:                   # 对整个网站（site）生效或仅对文章（post）生效
  exclude:                 # 需要排除的域名。主域名和子域名如 www 需分别配置    []
filename_case: 0           # 把文件名称转换为 (1) 小写或 (2) 大写
render_drafts: false       # 显示草稿，默认为：false
post_asset_folder: true    # 启动 Asset 文件夹
relative_link: false       # 把链接改为与根目录的相对位址
future: true               # 显示未来的文章
highlight:                 # 代码块的设置
  enable: false            # 开启代码块高亮
  line_number: false       # 显示行数
  auto_detect: false       # 如果未指定语言，则启用自动检测
  tab_replace:             # 用 n 个空格替换 tabs；如果值为空，则不会替换 tabs
```

#### 配置代码高亮及样式

由于 `Hexo` 自带的代码高亮主题显示不好看，所以主题中使用到了 [hexo-prism-plugin](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL2VsZTgyOC9oZXhvLXByaXNtLXBsdWdpbg==) 的 Hexo 插件来做代码高亮，安装命令如下：



Bash

```bash
npm i -S hexo-prism-plugin
```

然后，修改 Hexo 根目录下 `_config.yml` 文件中 `highlight.enable` 的值为 `false`，并新增 `prism` 插件相关的配置，主要配置如下：



Yaml

```yaml
prism_plugin:
  mode: 'preprocess'    # realtime/preprocess
  theme: 'tomorrow'
  line_number: false    # default false
  custom_css:
```

配置代码的样式



Yaml

```yaml
code:
  lang: true     # 代码块是否显示名称
  copy: true     # 代码块是否可复制
  shrink: false  # 代码块是否可以收缩
  break: false   # 代码是否折行
```

#### 修改文章字数统计

如果你想要在文章中显示文章字数、阅读时长信息，可以安装 [hexo-wordcount](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL3dpbGxpbi9oZXhvLXdvcmRjb3VudA==) 插件。

安装命令如下：



Bash

```bash
npm i --save hexo-wordcount
```



Yaml

```yaml
postInfo:
  date: true        # 发布日期
  update: true      # 更新日期
  wordCount: true   # 文章字数统计
  min2read: true    # 文章阅读时长
  readCount: false  # 文章阅读次数
```

#### 配置文章 TOC 功能

是否激活文章 TOC 功能，并配置 TOC 支持选中哪些标题类型，这是全局配置。
可以在某篇文章的 Front-matter 中再加上 `toc: false`，使该篇文章关闭 TOC 目录功能



Yaml

```yaml
toc:
  enable: true
  heading: h2, h3, h4, h5
  showToggleBtn: true       # 是否显示切换TOC目录展开收缩的按钮
```

#### 配置文章末尾打赏功能

默认激活（请替换为的你自己的微信、支付宝二维码图片、或者使用网络图片也可以）



Yaml

```yaml
reward:
  enable: true                        # 是否开启打赏
  title: 你的赏识是我前进的动力!        # 打赏标题
  wechat: /medias/reward/wechat.jpg   # 微信打赏二维码路径
  alipay: /medias/reward/alipay.jpg   # 支付宝打赏二维码路径
```

#### 配置复制追加版权信息

是否激活复制文章时追加博客和作者的版权信息。



Yaml

```yaml
copyright:
  enable: false
  minCharNumber: 120         # 至少复制多少个字符就追加版权信息.
  description: 本文章著作权归作者所有，任何形式的转载都请注明出处。
```

#### 配置 mathjax 数学公式

是否激活 `mathjax` 数学公式，这是全局配置，但文章仍然不会都开启 `mathjax` 渲染，考虑到 `mathjax` 加载比较耗时，你还需要在需要渲染的文章的 `Front-matter` 中再加上 `mathjax: true` 才行。



Yaml

```yaml
mathjax:
  enable: true
  cdn: https://cdn.bootcss.com/mathjax/2.7.5/MathJax.js?config=TeX-AMS-MML_HTMLorMML
```

#### emoji 表情支持

本主题新增了对 `emoji` 表情的支持，使用到了 [hexo-filter-github-emojis](https://sitoi.cn/go.html?u=aHR0cHM6Ly9ucG0udGFvYmFvLm9yZy9wYWNrYWdlL2hleG8tZmlsdGVyLWdpdGh1Yi1lbW9qaXM=) 的 Hexo 插件来支持 `emoji`表情的生成，把对应的`markdown emoji`语法（`::`,例如：`:smile:`）转变成会跳跃的`emoji`表情，安装命令如下：



Bash

```bash
npm install hexo-filter-github-emojis --save
```



Yaml

```yaml
githubEmojis:
  enable: true
  className: github-emoji
  inject: true
  styles:
  customEmojis:
```

#### 配置是否启用转载限制模块



Yaml

```yaml
reprint:
  enable: false   #是否启用“转载规则限定模块”
  default: cc_by
```

文章转载规则，可以是 `cc_by`, `cc_by_nd`, `cc_by_sa`, `cc_by_nc`, `cc_by_nc_nd`, `cc_by_nc_sa`, `cc0`, `noreprint` 或 `pay` 中的一个

#### 配置文章阅读密码功能

阅读文章的密码验证功能，如要使用此功能请激活该配置项，并在对应文章的 `Front-matter` 中写上 `password` 的键和加密后的密文即可。

> 请注意：为了保证密码原文不会被泄露到网页中，文章的密码必须是通过 `SHA256` 加密的，这样就不会被破解。



Yaml

```yaml
verifyPassword:
  enable: true
  promptMessage: 请输入访问本文章的密码
  errorMessage:  密码错误，将返回主页！
```

#### 配置文章分享模块

`sharejs` 文章分享模块。

> 支持顺序，可选项目为 twitter, facebook, google, qq, qzone, wechat, weibo, douban, linkedin。



Yaml

```yaml
sharejs:
  enable: true
  sites: wechat,qq,weibo,twitter,facebook,linkedin
```

`addthis` 文章分享模块。



Yaml

```yaml
addthis:
  enable: false
  pubid:            #前往https://www.addthis.com/获取
```

### 修改博客关于页配置

#### 配置关于页个人信息

在`关于`页面中配置个人信息，包括头像、职业和个人介绍.



Yaml

```yaml
profile:
  avatar: /medias/avatars/avatar.jpg    # 头像
  career: IIoT | Python 研发工程师       # 职业
  introduction: 爬虫工程师的进阶之旅      # 个人介绍
```

#### 配置关于页项目信息

在`关于`页面配置`我的项目`信息，如果你不需要这些信息则可以将其设置为不激活或者将其删除。



Yaml

```yaml
myProjects:
  enable: true
  data:
    private-network-ipfs:
      icon: fa-cubes
      iconBackground: 'linear-gradient(to bottom right, #29B6F6 0%, #1E88E5 100%)'
      url: https://github.com/Sitoi/private-network-ipfs
      desc: 利用 Docker 搭建 IPFS 私有网络
    scrapy-redis-sentinel:
      icon: fa-github
      iconBackground: 'linear-gradient(to bottom right, #66BB6A 0%, #81C784 100%)'
      url: https://github.com/Sitoi/scrapy-redis-sentinel
      desc: scrapy-redis-sentinel 基于 scrapy-redis 的基础上 新增 哨兵（sentinel）连接模式 以及 集群（cluster）连接模式。
    SystemdClash:
      icon: fa-plane
      iconBackground: 'linear-gradient(to bottom right, #29B6F6 0%, #1E88E5 100%)'
      url: https://github.com/Sitoi/SystemdClash
      desc: Clash 以 systemd 服务的方式开机自启
```

#### 配置关于页技能信息

在`关于`页面配置`我的技能`信息，如果你不需要这些信息则可以将其设置为不激活或者将其删除.



Yaml

```yaml
mySkills:
  enable: true
  data:
    Python:
      background: 'linear-gradient(to right, #FF0066 0%, #FF00CC 100%)'
      percent: 80%
    Docker:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 80%
    OpneShift:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 70%
    Ambari:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 60%
    HDFS:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 65%
    Spark:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 60%
    Flask:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 80%
    MongoDB:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 70%
    MySQL:
      background: 'linear-gradient(to right, #4CAF50 0%, #81C784 100%)'
      percent: 65%
    Vue:
      background: 'linear-gradient(to right, #FFEB3B 0%, #FFF176 100%)'
      percent: 35%
```

### 修改博客留言板配置

`contact` 页是用来展示**留言板**信息的页面，如果在你的博客 `source` 目录下还没有 `contact/index.md` 文件，那么你就需要新建一个，命令如下：



Bash

```bash
hexo new page "contact"
```

编辑你刚刚新建的页面文件 `/source/contact/index.md`，至少需要以下内容：



Yaml

```yaml
---
title: contact
date: 2018-09-30 17:25:30
type: "contact"
layout: "contact"
---
```

`/source/contact/index.md` 中的 markdown 内容，回展示在留言板的页面上，例子如下：



Yaml

```yaml
---
title: contact
date: 2019-10-14 13:14:00
type: "contact"
layout: "contact"
---


## 畅所欲言
---
在这里可以留下你的足迹，欢迎在下方留言，欢迎交换友链，一起交流学习！
```



![效果](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/contact_md.png)

**效果**



> **注**：本留言板功能依赖于第三方评论系统，请**激活**你的评论系统才有效果。
> 可同时开启多个留言板~

#### 配置 Gitalk 评论模块

默认为不激活



Yaml

```yaml
gitalk:
  enable: false
  owner: sitoi
  repo: Sitoi.github.io
  oauth:
    clientId:
    clientSecret:
  admin:
    - sitoi
```

##### 获取 clientId 和 clientSecret

首先，你得有一个Github账号（这个就不多说了吧），下面，打开 [https://github.com/settings/applications/new](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL3NldHRpbmdzL2FwcGxpY2F0aW9ucy9uZXc=)，具体填法如下：



![GitHub APP](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/new_github_app.png)

**GitHub APP**



- `Application name`：应用名称，随便填
- `Homepage URL`：没有过多要求，可以填自己的博客地址
- `Application description`：应用描述，描述一下，无要求
- `Authorization callback URL`：这个就有要求了，填自己要使用 Gitalk 的博客地址，不可乱填

接着，你就可以得到 Client ID 和 Client Secret



![Client ID & Client Secret](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/get_app_ids.png)

**Client ID & Client Secret**



进行配置，修改配置文件：



Yaml

```yaml
gitalk:
  enable: false
  owner: sitoi
  repo: Sitoi.github.io
  oauth:
    clientId:
    clientSecret:
  admin:
    - sitoi
```

- `enable`：true # 指的是是否开启 Gitalk
- `owner`：sitoi # 这个项目名的拥有者（GitHub账号或组织）
- `repo`：Sitoi.github.io # 你要存放的项目名，下文会详细再说
- `clientId`：xxxxxx # 之前的 Client ID
- `ClientSecret`：xxxxxx # 之前的 Client Secret
- `admin`：sitoi # 管理员用户，下文也会详细讲

`repo`：Gitalk 是基于 GitHub 的 issues 功能的，所以，你要为他建一个库或用现成的库，我个人建议新建一个，而 repo 就是你要用的库的名称。 比如，我就为 Gitalk 专门建了一个叫 gitalk 的库，所以在 repo: 处填 gitalk。

`admin`：即管理员帐号。如果你是个人账号，那么这里就填你的账户名和协作者的账户名。**以数组形式**。

#### 配置 Gitment 评论模块

默认为不激活



Yaml

```yaml
gitment:
  enable: false
  owner:
  repo:
  oauth:
    clientId:
    clientSecret:
```

> 获取 clientId 和 clientSecret 教程和上文一样

#### 配置 Disqus 评论模块

##### 注册 Disqus 帐号

至 [Disqus](https://sitoi.cn/go.html?u=aHR0cHM6Ly9kaXNxdXMuY29tLw==) 首页注册账号并登录，接着点击首页的「GET STARTED」：



![Disqus](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/disqus_index.png)

**Disqus**



选择「I want to install Disqus on my site」选项：



![I want to install Disqus on my site](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/disqus_create.png)

**I want to install Disqus on my site**



需要输入的栏目：

- Websit Name：自定义 short name，且是唯一，像我是设置为 sitoi。`short name` 会在设置 `Hexo` 時需要
- Category：类别，自行选择
- Language：语言，自行选择
- 填写后点击「Create Site」



![Create Site](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/disqus_create_new_site.png)

**Create Site**



##### 修改配置文件



Yaml

```yaml
disqus:
  enable: false
  shortname: sitoi      # 全部小写
```

#### 配置 Livere 来必力评论模块

##### 注册 LiveRe 获取 uid

进入 [LiveRe](https://sitoi.cn/go.html?u=aHR0cHM6Ly9saXZlcmUuY29tL2FwcGx5)，注册账号。

LiveRe 有两个版本：

- City 版：是一款适合所有人使用的免费版本；
- Premium 版：是一款能够帮助企业实现自动化管理的多功能收费版本。

我们 City 版就够了。



![LiveRe](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/livere.png)

**LiveRe**



填写完成后，进入到 管理页面 -> 代码管理 -> 一般网站 代码中，data-uid 即为所需 uid。

##### 修改配置文件

将获取到的 uid 填入对应的配置文件



Yaml

```yaml
livere:
  enable: false
  uid: 
```

#### 配置 Valine 评论模块的配置

获取 `appId` 和 `appKey` 请参考[官方文档](https://sitoi.cn/go.html?u=aHR0cHM6Ly92YWxpbmUuanMub3JnL3F1aWNrc3RhcnQuaHRtbCMlRTglOEUlQjclRTUlOEYlOTZBUFAtSUQtJUU1JTkyJThDLUFQUC1LZXk=)

默认为不激活，如要使用，就请激活该配置项，并设置 `appId` 和 `appKey`。



Yaml

```yaml
valine:
  enable: true
  appId: APP_ID
  appKey: APP_KEY
  notify: true
  verify: true
  visitor: true
  avatar: 'mm'               # Gravatar style : mm/identicon/monsterid/wavatar/retro/hide
  pageSize: 10
  placeholder: 'just go go'  # Comment Box placeholder
  background: /medias/comment_bg.png
```

### 修改博客友链的配置

`friends` 页是用来展示**友情连接**信息的页面，如果在你的博客 `source` 目录下还没有 `friends/index.md` 文件，那么你就需要新建一个，命令如下：



Bash

```bash
hexo new page "friends"
```

编辑你刚刚新建的页面文件 `/source/friends/index.md`，至少需要以下内容：



Yaml

```yaml
---
title: friends
date: 2018-12-12 21:25:30
type: "friends"
layout: "friends"
---
```

同时，在你的博客 `source` 目录下新建 `_data` 目录，在 `_data` 目录中新建 `friends.json` 文件，文件内容如下所示：



Json

```json
[
  {
    "name": "Sitoi",
    "avatar": "https://sitoi.cn/medias/avatars/avatar.jpg",
    "url": "https://sitoi.cn/",
    "introduction": "爬虫工程师的进阶之旅",
    "title": "访问主页"
  },
  {
    "name": "闪烁之狐",
    "avatar": "https://blinkfox.github.io/medias/avatar.jpg",
    "url": "https://blinkfox.github.io",
    "introduction": "编程界大佬，技术牛，人还特别好，不懂的都可以请教大佬",
    "title": "访问主页"
  },
  {
    "name": "Licardo",
    "avatar": "https://licardo.cn/medias/avatar.png",
    "url": "https://licardo.cn/",
    "introduction": "一个医学生的成才之路",
    "title": "访问主页"
  }
]
```

### 修改博客搜索的配置

本主题中还使用到了 [hexo-generator-search](https://sitoi.cn/go.html?u=aHR0cHM6Ly9naXRodWIuY29tL3d6cGFuL2hleG8tZ2VuZXJhdG9yLXNlYXJjaA==) 的 Hexo 插件来做内容搜索，安装命令如下：



Bash

```bash
npm install hexo-generator-search --save
```

在 Hexo 根目录下的 `_config.yml` 文件中，新增以下的配置项：



Yaml

```yaml
search:
  path: search.xml
  field: post
```

### 配置网站各种特效

#### 单击页面爱心效果



Yaml

```yaml
clicklove:
  enable: true
```

#### 背景 canvas-nest



Yaml

```yaml
canvas_nest:
  enable: false
  color: 0,0,255       #线条颜色, 默认: '0,0,0' ；三个数字分别为(R,G,B)，注意用,分割
  pointColor: 0,0,255  #交点颜色, 默认: '0,0,0' ；三个数字分别为(R,G,B)，注意用,分割
  opacity: 0.8         # 线条透明度（0~1）, 默认: 0.5
  zIndex: -1           # 背景的z-index属性，css属性用于控制所在层的位置, 默认: -1
  count: 150           # 线条的总数量, 默认: 99
```

### 配置网站统计功能

#### 不蒜子统计



Yaml

```yaml
busuanziStatistics:
  enable: false
  totalTraffic: true # 总访问量
  totalNumberOfvisitors: true # 总人次
```

#### Google Analytics

至 [Google Analytics](https://sitoi.cn/go.html?u=aHR0cHM6Ly9hbmFseXRpY3MuZ29vZ2xlLmNvbS8=) 注册账号，获取 ID



Yaml

```yaml
googleAnalytics:
  enable: true
  id: GOOGLE_ID
```

#### Baidu Analytics

至 [百度统计](https://sitoi.cn/go.html?u=aHR0cHM6Ly90b25namkuYmFpZHUuY29tLw==) 注册账号，获取 ID



Yaml

```yaml
baiduAnalytics:
  enable: true
  id: BAIDU_ID
```

#### 站长之家统计

##### 登录并注册帐号

至 [站长之家](https://sitoi.cn/go.html?u=aHR0cHM6Ly93d3cudW1lbmcuY29tLw==) 注册账号，进入工作台



![友盟](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/umeng_index.png)

**友盟**



##### 点击创建新应用，选择创建 Web 应用



![创建应用](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/umeng_create.png)

**创建应用**



##### 创建 WEB 应用，需要输入的栏目

- 网站名称：输入你的网站名称
- 网站域名：填入你汪涵的域名 例如：`sitoi.cn`
- 网站首页：填写你网站的首页，注意 HTTP 还是 HTTPS
- 网站类型：选择网站的类型
- 网站地区：选择网站的地区
- 网站简介：填写网站的简介
- 点击`确认添加站点`



![创建 WEB 应用](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/umeng-create_site.png)

**创建 WEB 应用**



##### 获取站长之家代码

- 点击获取代码
- 选择你喜欢的代码样式
- 点击复制到剪贴板



![统计代码](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/umeng_code.png)

**统计代码**



##### 修改 footer.ejs 代码

代码文件：`themes/matery/layout/_partial/footer.ejs`
代码行数：大约 28 ~ 34 行
代码内容如下：



Html

```html
<% if (theme.cnzz) { %>
    <script type="text/javascript">
        var cnzz_protocol = (("https:" == document.location.protocol) ? "https://" : "http://");
        document.write(unescape("%3Cspan id='cnzz_stat_icon_1278109894'%3E%3C/span%3E%3Cscript src='" + cnzz_protocol + "v1.cnzz.com/z_stat.php%3Fid%3D1278109894%26online%3D1%26show%3Dline' type='text/javascript'%3E%3C/script%3E"));
    </script>
    <br>
<% } %>
```

替换里面的 `...` 为你复制的统计代码。

##### 修改配置文件

将 配置文件中的 `cnzz` 设置为 `true` 表示启动，`false` 表示关闭



Yaml

```yaml
cnzz: true
```

### 配置网站其他功能

#### 配置是否每日切换背景

banner 是否每日切换。若为 false, 则 banner 默认为 `/medias/banner/0.jpg`



Yaml

```yaml
banner:
  enable: false
```

#### 修改 banner 图和文章特色图

你可以直接在 `/source/medias/banner` 文件夹中更换你喜欢的 `banner` 图片，主题代码中是每天动态切换一张，只需 `7` 张即可。如果你会 `JavaScript` 代码，可以修改成你自己喜欢切换逻辑，如：随机切换等，`banner` 切换的代码位置在 `/layout/_partial/bg-cover-content.ejs` 文件的 `` 代码中：

修改对应的地址即可



Ejs

```ejs
<% if (theme.banner.enable) { %>  <% } else { %>  <% } %>
```

如果使用 jsdelivr 作为 cdn 加速，请修改 `https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/banner/` 为你的 cdn 文件地址

如果使用本地的图片，创建 `/source/medias/featureimages` 文件夹，添加图片，每个图片必须是`jpg` 结尾，使用数字进行编号，并需要在 `_config.yml` 做同步修改。

默认特色图的集合。当文章没有设置特色图时，本主题会根据文章标题的 `hashcode` 值取余，来选择展示对应的特色图。



Yaml

```yaml
featureImages:
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/0.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/1.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/2.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/3.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/4.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/5.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/6.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/7.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/8.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/9.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/10.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/11.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/12.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/13.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/14.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/15.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/16.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/17.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/18.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/19.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/20.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/21.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/22.jpg
  - https://cdn.jsdelivr.net/gh/Sitoi/cdn/medias/featureimages/23.jpg
```

#### 配置网页预加载

本主题整体采用预加载模式，预加载就是进入项目前提前加载资源，避免在项目中加载缓慢，影响用户体验,这样可以在我们访问其他页面的时候会稍微快点。



Yaml

```yaml
instantpage:
  enable: true
```

#### 配置图片懒加载

`懒加载`一般是当图片滚动进可视窗口内才加载图片，可视窗口之外的图片则不加载

本主题图片进行懒加载，这样做效果就是 `html`、`css`、`js` 加载之后，图片再加载。既保证了网页的打开速度，也不会因图片的庞大体积而拖累了整个页面的加载。



Yaml

```yaml
lazyload:
  enable: false
  onlypost: true
  loadingImg: /medias/loading/orange.square-circle-preloader.svg
```

#### 配置在线聊天功能

##### DaoVoice 在线聊天功能

前往 [DaoVoice](https://sitoi.cn/go.html?u=aHR0cDovL3d3dy5kYW92b2ljZS5pby8=) 官网注册并且获取 `app_id`，并将 `app_id` 填入主题的 `_config.yml` 文件中。



Yaml

```yaml
daovoice:
  enable: false
  app_id:
```

##### Tidio 在线聊天功能

前往 [Tidio](https://sitoi.cn/go.html?u=aHR0cHM6Ly93d3cudGlkaW8uY29tLw==) 官网注册并且获取 `Public Key`，并将 `Public Key` 填入主题的 `_config.yml` 文件中。



Yaml

```yaml
tidio:
  enable: false
  public_key:
```

#### 配置绚丽彩虹播放器

致 [绚丽彩虹播放器](https://sitoi.cn/go.html?u=aHR0cHM6Ly93d3cuYmFkYXBwbGUudG9wLw==) 注册并登录，播放器 Key

官方教程视频：[https://www.bilibili.com/video/av8153459](https://sitoi.cn/go.html?u=aHR0cHM6Ly93d3cuYmlsaWJpbGkuY29tL3ZpZGVvL2F2ODE1MzQ1OQ==)



Yaml

```yaml
badApplePlayer:
  enable: false   # 是否启动
  XlchKey: Sitoi  # 播放器 Key
```

#### 配置博客看板娘

默认关闭



Yaml

```yaml
# 看板娘配置
live2d:
  enable: false
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  log: false
  model:
    use: live2d-widget-model-shizuku
  display:
    position: left
    width: 150
    height: 200
  mobile:
    show: false
  react:
    opacity: 0.7
```

### 博客添加 PWA 功能

详细教程请阅读[基于 Hexo GitHub 从零开始搭建个人博客（四）：让你的博客完美支持 PWA](https://sitoi.cn/go.html?u=aHR0cHM6Ly9zaXRvaS5jbi9wb3N0cy80OTExNS5odG1s)



Yaml

```yaml
pwa:
  manifest:
    path: /manifest.json
    body:
      name: Sitoi
      short_name: Sitoi
      theme_color: white
      background_color: white
      display: standalone
      orientation: portrait
      scope: /
      start_url: /
      icons:
        - src: /medias/logo_48.png
          type: image/png
          sizes: 48x48
        - src: /medias/logo_96.png
          type: image/png
          sizes: 96x96
        - src: /medias/logo_128.png
          type: image/png
          sizes: 128x128
        - src: /medias/logo_144.png
          type: image/png
          sizes: 144x144
        - src: /medias/logo_180.png
          type: image/png
          sizes: 180x180
        - src: /medias/logo_192.png
          type: image/png
          sizes: 192x192
        - src: /medias/logo_512.png
          type: image/png
          sizes: 512x512
        - src: /apple-touch-icon.png
          type: image/png
          sizes: 180x180
  serviceWorker:
    path: /sw.js
    preload:
      urls:
        - /
      posts: 12
    opts:
      networkTimeoutSeconds: 30
    routes:
      - pattern: !!js/regexp /hm.baidu.com/
        strategy: networkOnly
      - pattern: !!js/regexp /www.google-analytics.com/
        strategy: networkOnly
      - pattern: !!js/regexp /.*\.(js|css|jpg|jpeg|png|gif)$/
        strategy: cacheFirst
      - pattern: !!js/regexp /\//
        strategy: networkFirst
  priority: 5
```

PWA 适配苹果图标



Yaml

```yaml
appletouchicon: /apple-touch-icon.png
```

### 修改博客样式

#### 修改主题颜色

在主题文件的 `/source/css/matery.css` 文件中，搜索 `.bg-color` 来修改背景颜色：



Css

```css
/* 整体背景颜色，包括导航、移动端的导航、页尾、标签页等的背景颜色. */
.bg-color {
    background-image: linear-gradient(to right, #4cbf30 0%, #0f9d58 100%);
}

@-webkit-keyframes rainbow {
   /* 动态切换背景颜色. */
}

@keyframes rainbow {
    /* 动态切换背景颜色. */
}
```

## 文章 Front-matter 介绍

### Front-matter 选项详解

`Front-matter` 选项中的所有内容均为**非必填**的。但我仍然建议至少填写 `title` 和 `date` 的值。

| 配置选项      | 默认值                         | 描述                                                         |
| :------------ | :----------------------------- | :----------------------------------------------------------- |
| title         | `Markdown` 文件标题            | 文章标题，强烈建议填写此选项                                 |
| date          | 文件创建时的日期时间           | 发布时间，强烈建议填写此选项，且最好保证全局唯一             |
| author        | 跟 `_config.yml` 中的 `author` | 文章作者                                                     |
| img           | `featureImages` 中的某个值     | 文章特征图，推荐使用图床(腾讯云、七牛云、又拍云等)来做图片的路径.如: `http://xxx.com/xxx.jpg` |
| top           | `true`                         | 推荐文章（文章是否置顶），如果 `top` 值为 `true`，则会作为首页推荐文章 |
| cover         | `false`                        | 表示该文章是否需要加入到首页轮播封面中                       |
| coverImg      | 无                             | 表示该文章在首页轮播封面需要显示的图片路径，如果没有，则默认使用文章的特色图片 |
| password      | 无                             | 文章阅读密码，如果要对文章设置阅读验证密码的话，就可以设置 `password` 的值，该值必须是用 `SHA256` 加密后的密码，防止被他人识破。前提是在主题的 `config.yml` 中激活了 `verifyPassword` 选项 |
| toc           | `true`                         | 是否开启 TOC，可以针对某篇文章单独关闭 TOC 的功能。前提是在主题的 `config.yml` 中激活了 `toc` 选项 |
| mathjax       | `false`                        | 是否开启数学公式支持，本文章是否开启 `mathjax`，且需要在主题的 `_config.yml` 文件中也需要开启才行 |
| summary       | 无                             | 文章摘要，自定义的文章摘要内容，如果这个属性有值，文章卡片摘要就显示这段文字，否则程序会自动截取文章的部分内容作为摘要 |
| categories    | 无                             | 文章分类，本主题的分类表示宏观上大的分类，只建议一篇文章一个分类 |
| tags          | 无                             | 文章标签，一篇文章可以多个标签                               |
| keywords      | 文章标题                       | 文章关键字，SEO 时需要                                       |
| reprintPolicy | cc_by                          | 文章转载规则，可以是 `cc_by`,`cc_by_nd`,`cc_by_sa`,`cc_by_nc`,`cc_by_nc_nd`,`cc_by_nc_sa`,`cc0`,`noreprint` 或 `pay` 中的一个 |

> **注意**:
>
> 1. 如果 `img` 属性不填写的话，文章特色图会根据文章标题的 `hashcode` 的值取余，然后选取主题中对应的特色图片，从而达到让所有文章都的特色图**各有特色**。
> 2. `date` 的值尽量保证每篇文章是唯一的，因为本主题中 `Gitalk` 和 `Gitment` 识别 `id` 是通过 `date` 的值来作为唯一标识的。
> 3. 如果要对文章设置阅读验证密码的功能，不仅要在 Front-matter 中设置采用了 SHA256 加密的 password 的值，还需要在主题的 `_config.yml` 中激活了配置。有些在线的 SHA256 加密的地址，可供你使用：[开源中国在线工具](https://sitoi.cn/go.html?u=aHR0cDovL3Rvb2wub3NjaGluYS5uZXQvZW5jcnlwdD90eXBlPTI=)、[chahuo](https://sitoi.cn/go.html?u=aHR0cDovL2VuY29kZS5jaGFodW8uY29tLw==)、[站长工具](https://sitoi.cn/go.html?u=aHR0cDovL3Rvb2wuY2hpbmF6LmNvbS90b29scy9oYXNoLmFzcHg=)。
> 4. 您可以在文章md文件的 front-matter 中指定 reprintPolicy 来给单个文章配置转载规则

以下为文章的 `Front-matter` 示例。

### 最简示例



Yaml

```yaml
---
title: 基于 Hexo GitHub 从零开始搭建个人博客
date: 2019-12-30 09:25:00
---
```

### 最全示例



Yaml

```yaml
---
title: 基于 Hexo GitHub 从零开始搭建个人博客
date: 2019-12-30 09:25:00
author: Sitoi
img: /source/images/xxx.jpg
top: true
cover: true
coverImg: /images/1.jpg
password: 8d969eef6ecad3c29a3a629280e686cf0c3f5d5a86aff3ca12020c923adc6c92
toc: false
mathjax: false
summary: 这是你自定义的文章摘要内容，如果这个属性有值，文章卡片摘要就显示这段文字，否则程序会自动截取文章的部分内容作为摘要
categories: Hexo
keywords: Hexo GitHub blog
tags:
  - Hexo
  - Blog
  - GitHub
---
```

## 本地运行预览

### 安装依赖包

运行如下命令：



Bash

```bash
npm i
```

### 启动 hexo 博客

运行如下命令：



Bash

```bash
hexo server
```

输出如下：



Bash

```bash
INFO  Start processing
INFO  Hexo is running at http://localhost:4000 . Press Ctrl+C to stop.
```

### 查看博客

打开浏览器，输入地址：[http://localhost:4000/](https://sitoi.cn/go.html?u=aHR0cDovL2xvY2FsaG9zdDo0MDAwLw==) 看到下面的效果，说明的你博客已经构建成功了



![BLOG](https://cdn.jsdelivr.net/gh/Sitoi/cdn/img/matery_index.png)

**BLOG**



## 部署到 GitHub Pages

登录 GitHub 打开你的项目，获取 GitHub ssh repo 地址，替换配置中的 `repo github` 的



Yaml

```yaml
# 自动部署配置
deploy:
  - type: git
    repo:
      github: git@github.com:Sitoi/Sitoi.github.io.git   # 修改这里为你项目的地址
    branch: master
```

运行 如下命令进行部署：



Bash

```bash
hexo clean
hexo generate
hexo deploy
```

部署成功 你就可以上你的网站查看效果啦。

## 参考

3. [https://sitoi.cn/posts/63466.html](https://sitoi.cn/go.html?u=aHR0cHM6Ly95YWZpbmUtYmxvZy5jbi9wb3N0cy80YWIyLmh0bWw=)