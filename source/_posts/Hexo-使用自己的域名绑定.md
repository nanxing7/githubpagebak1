---
title: Hexo 使用自己的域名绑定
date: 2019-09-24 23:36:00
tags: 
categories :
- Hexo
---
# 准备阶段
## 域名准备
首先你需要准备一个喜欢的域名，然后注册域名，至于怎么注册这里就不啰嗦了，百度一大把。
## Hexo 博客准备
你需要配置好你的 Hexo 博客，可以看我的教程，也可以去网上找教程，这里就不复述了
# 开始阶段
## 将域名绑定到你的 Github Pages 上
去你注册域名的域名注册商去解析你要绑定的域名。
比如我要绑定 [sanyuedev.github.io](https://sanyuedev.github.io)。
![这里以阿里云域名解析为例子](https://raw.githubusercontent.com/sanyuedev/Picture_Bed_With_PicGO/master/20190924234512.png)
这里记录类型我们选择 `CNAME`，主机记录选择 `blog`,其他的默认就好了
点击确定就解析好了。
## Hexo 设置
在 Hexo 的 `source` 文件夹下面新建一个文件名叫 `CNAME` 的文件，这个文件不能有后缀名。
这里我使用的是Vim创建。
```vim
vim CNAME
```
文件创建成功后我们按 `i` 进入 Vim 的插入模式，输入刚才设置的解析记录
```vim
blog.sanyuedev.top
```
按 `ESC` 后再输入 `:q` 回车即可。
# 部署阶段
接下来按流程部署博客即可。
```zsh
hexo clean
hexo g
hexo d
```
我们现在输入我们设置的域名即可进入啦～

文章写的不多，写的不好多多见谅哈～
