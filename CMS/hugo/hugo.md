偶然发现艾老师的博客页面非常简洁美观，再加上 **Hexo** 的性能着实堪忧，索性就来体验一下 **Hugo** 。

### 1 安装

- Hugo
- Theme：[Zozo](https://github.com/varkai/hugo-theme-zozo)

```bash
$ sudo pacman -S hugo
```

### 2 配置

#### 2.1 本地配置

建立本地仓库

```bash
$ hugo new site <repo_path>
```

添加主题

```bash
$ git submodule add https://github.com/varkai/hugo-theme-zozo
```

从主题的 **exampleSite** 文件夹复制配置文件 **config.toml** 到站点根目录，基本配置如下

```toml
baseURL = "https://example.com"
languageCode = "zh-cn"
defaultContentLanguage = "zh-cn"
title = "无尽光芒"                    # site title  # 网站标题
theme = "zozo"
hasCJKLanguage = true                # has chinese/japanese/korean ? # 自动检测是否包含 中文\日文\韩文
summaryLength = 100
paginate = 4                         # shows the number of articles  # 首页显示文章数量
enableEmoji = true
googleAnalytics = ""                 # your google analytics id
disqusShortname = ""                 # your discuss shortname

[author]                             # essential                     # 必需
  name = "Zeuk"

[blackfriday]
  smartypants = false

[[menu.main]]                        # config your menu  # 配置菜单
  name = "首页"
  weight = 10
  identifier = "home"
  url = "/"
[[menu.main]]
  name = "归档"
  weight = 20
  identifier = "archive"
  url = "/posts/"
[[menu.main]]
  name = "标签"
  weight = 30
  identifier = "tags"
  url = "/tags/"
[[menu.main]]
  name = "关于"
  weight = 40
  identifier = "about"
  url = "/about/"

[params]
  subTitle = "the site subtitle"                                       # site's subTitle  # 网站二级标题
  footerSlogan = "我的精神家园"                                          # site's footer slogan  # 网站页脚标语
  keywords = ["Hugo", "theme","zozo"]                                  # site's keywords  # 网站关键字
  description = "Hugo theme zozo example site."                        # site's description  # 网站描述

# mathjax
  enableMathJax = true                                                 # enable mathjax  # 是否使用mathjax（数学公式）

  enableSummary = true                                                 # display the article summary  # 是否显示文章摘要
  
# Valine.
# You can get your appid and appkey from https://leancloud.cn
# more info please open https://valine.js.org
[params.valine]
  enable = false
  appId = ""
  appKey = ""
  placeholder = " "
  visitor = true

[social]
  github = " "
  twitter = " "
  facebook = " "
  weibo = " "
  instagram = " "
```

拥有大量的注释，非常容易理解。修改完毕即可查看效果：

```bash
$ hugo server
```

#### 2.2 GitLab 配置

新建一个名为 username.gitlab.io 的仓库

```bash
$ cd username.gitlab.io
$ git init
$ git remote add origin <repo_url>
$ git add .
$ git commit -m "upload blog"
$ git push -u origin master
```
