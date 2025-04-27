[English](/README.md) | [中文](/README_zh-CN.md)

# Tiddlywiki-NodeJS-Github-Template

Default wiki template for [TidGi-Desktop](https://github.com/tiddly-gittly/TidGi-Desktop), an App that can generate template wiki on one-click.

Knowledge base Template, with advanced filter search and faceted data aggregation.

[onetwo.ren/wiki](https://onetwo.ren/wiki) is an example of this template. And [tiddly-gittly.github.io/Tiddlywiki-NodeJS-Github-Template/](https://tiddly-gittly.github.io/Tiddlywiki-NodeJS-Github-Template/) is deployed example of this repo. (There are some optimization to make this demo readonly, and being not downloadable, so its size is almost as small as a GIF picture.)

You need to change the contents of the `$:/GitHub/Repo` entry to your personal github repository address.The default branch is master, you can manually change the `$:/core/templates/canonical-uri-external-image` entry to another branch such as main.

Downloadable HTML is at [tiddly-gittly.github.io/Tiddlywiki-NodeJS-Github-Template/offline.html](https://tiddly-gittly.github.io/Tiddlywiki-NodeJS-Github-Template/offline.html), which contains edit related plugins, and will be slightly bigger (a size of a tiktok video.)

Also there is a TiddlyHost template at [tiddlyhost.com/hub/user/linonetwo](https://tiddlyhost.com/hub/user/linonetwo), which will update manually when I remember it. (It is same as, download the offline version above, and upload to a newly created tiddlyhost wiki.)

This repo used to contains the wiki backup data and script to start a local wiki server on MacOS on start up. It is now deprecated, and no money to maintain, now [TiddlyGit-Desktop](https://github.com/tiddly-gittly/TiddlyGit-Desktop) is preferred. Old version can be found at the [feat/auto-start branch](https://github.com/tiddly-gittly/Tiddlywiki-NodeJS-Github-Template/tree/feat/auto-start). Contribution to it is welcome.

## Setup

[用TiddlyWiki替代Notion和EverNote作为个人知识管理系统 (Chinese)](https://onetwo.ren/%E7%94%A8tiddlywiki%E6%9B%BF%E4%BB%A3notion%E5%92%8Cevernote%E7%AE%A1%E7%90%86%E7%9F%A5%E8%AF%86/)

English translation comeout soon. (?)

## Deployed to Github Pages

Automatically.

## NPM Scripts

`npm build`: pack tiddlywiki data to a HTML file

## Shell Scripts

[scripts/build-wiki.js](scripts/build-wiki.js) will actually pack tiddlywiki data to a HTML file

## Credit

Scripts are inspired by [DiamondYuan/wiki](https://github.com/DiamondYuan/wiki)

---
title: Tiddlywiki个人知识管理存储教程（小白向）
---

# 一、构建个人知识管理的步骤
## 1、下载[tiddly-gittlyTidGi-Desktop太记桌面版](https://github.com/tiddly-gittly/TidGi-Desktop)
详情：点击上面的链接去到**太记作者林一二***github的代码仓库下载>个人知识管理的软件*
下载步骤如下：

```mermaid
graph TD
a[去github太记作者林一二的仓库] 
--> b[点击Releases下面的版本号] 
--> c[找到自己电脑所对应的太记桌面版进行下载] 
--> d[耐心等待下载完成]
  
    z[竖向流程图]
```
## 2、安装Tiddlywiki（太记）桌面版在自己电脑上
详情：



```mermaid
graph TD
a[安装Tiddlywiki桌面版在自己电脑上] 
--> b[点击下载好的Tiddlywiki进行安装] 
--> c[耐心等待Tiddlywiki桌面版安装完成]
z[竖向流程图]
```

## 3、在自己github账号下新建一个个人知识管理存储的代码仓库（记住仓库的命名）

详情:

``` mermaid
graph TD
a[打开自己github仓库] --> b[点击New按钮]--> c[找到Repository name*位置]
--> d[在Repository name*下面的空格内取一个知识管理存储仓库名字]
--> e[记住所取的名字]

z[竖向流程图]
```



## 4、在自己github账号下申请一个Fine- grained tokens（细粒度token），并开启全部权限

```mermaid
graph TD
a[打开自己github仓库] --> b[点击页面右上角自己的头像]
--> c[点击下面Settings按钮]
--> d[点击<> Developer settings]
--> e[展开Personal access tokens]
--> f[点击Fine- grained tokens]
--> g[点击Generate new token]
--> h[此时需输一遍自己github账号密码确认是本人]
--> i[Token name处取一个名称]
--> j[Description处可以填一个备注]
--> k[Expiration处展开选No expiration]
--> l[在弹出的提示处点Generate token]
--> m[复制小铃铛下面方框内的密钥并粘贴在自己能找到的地方]


z[竖向流程图]
```



## 5、在自己电脑的TidGi-Desktop（太记桌面版）内建立一个个人知识管理仓库（必须与github账号下新建的个人知识管理存储的代码仓库同名）



``` mermaid
graph TD
a[打开电脑桌面TidGi] --> b[点击左侧栏加号]
--> c[新建一个本地个人知识管理仓库]
--> d[必须和之前在github的知识仓库同名]
z[竖向流程图]
```



## 6、对自己电脑里的TidGi-Desktop（太记桌面版）内新建的个人知识管理仓库进行设置

**配置工作区**

详情配置：

```mermaid
graph TD
a[鼠标右键点开TidGi左侧栏刚才新建的仓库头像] 
--> b[在弹出界面点击配置工作区]
--> c[一定要点击弹出框右上角窗口最大化]
--> d[一定要点击弹出框右上角窗口最大化]
--> e[一定要点击弹出框右上角窗口最大化]
--> f[在弹出界面展开博客和服务器设置启用HTTP API]
--> g[把启用 HTTP API旁边开关打开]
--> h[展开保存和同步]
--> i[把云端同步知识库旁边的开关打开]
--> j[用于登录Git的凭证一定时间后会过期方框内填在github之前申请的密钥]
--> k[用于登录Git的账户名注意是你的仓库网址中你的名字部分方框内填自己github登录的账号]
--> l[用于Git提交记录的Email用于在Github等服务上统计每日提交量方框内填自己github申请时的邮箱]
--> m[你的Git的默认分支Github在 黑命贵事件后将其从master改为了main框内填main]
--> n[搜索Github仓库名下面填自己知识管理仓库取的仓库名]
--> o[关闭配置工作去页面]
z[竖向流程图]
```

> 备注：为什么“一定要点击弹出框右上角窗口最大化”这一项如此重要，那是因为多数人配置都是这一步配置不好

**配置我的TiddlyWiki电脑端GithubPageslmage**

详情配置：

```mermaid
graph TD
a[把我的TiddlyWiki下面的设置齿轮点开] --> b[点击上方横栏内的设置]
--> c[点击GithubPageslmage]
--> d[This is the user name 下面填自己github账号名/自己知识管理取的仓库名]
--> e[This usually is master or main下面框填main]
--> f[This usually is just tiddlers下面填自己知识管理取的仓库名/tiddlers]
--> g[填完点上方横栏内的保存]
z[竖向流程图]
```



## 7、把自己电脑里的TidGi-Desktop（太记桌面版）内新建的个人知识管理仓库拖入github账号下的个人知识管理存储的代码仓库

**拖电脑知识管理文件夹到github知识管理文件夹内**

详情：

```mermaid
graph TD
a[打开个人github个人主页] --> b[点击左上角的github头像]
--> c[在展开的页面内打开个人知识管理文件夹]
--> d[找到电脑内太记桌面版所建的个人知识管理文件夹]
--> e[直接把太记桌面版所建的个人知识管理文件夹拖入github知识管理文件夹内]
z[竖向流程图]
```



**设置github的网页展示**

详情：

```mermaid
graph TD
a[打开个人github个人主页] --> b[点击左上角的github头像]
--> c[在展开的页面内打开个人知识管理文件夹]
--> d[点记上方横栏内的Settings设置]
--> e[在弹出的页面点击Pages]
--> f[找到Build and deployment下面选项]
--> g[把Deploy from a branch 改为GitHub Actions ]
z[竖向流程图]
```



> **此教程内最重要的两点：**
>
> ​                                    **1、配置电脑内工作区时，一定要点击弹出框右上角窗口最大化。**
>
> ​                                    **2、配置设置github的网页展示时，把Deploy from a branch 改为GitHub Actions **
>
> 
