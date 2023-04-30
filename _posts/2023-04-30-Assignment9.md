---
layout: post
title: 云计算系统Assignment 9
subtitle: 其实我觉得博客里的其他文章都挺有意思的 如果助教改作业很无聊的话欢迎读读看^^

tags: [实验报告]
comments: true
---



## 博客主题及其选取原因

* 本次选用[beautiful-jekyll](https://github.com/daattali/beautiful-jekyll)为架构搭建了一个简单的静态网页博客，beautiful-jekyll是一个基于HTML的十分完善的框架，由于本地的Ruby环境安装不下来，而且基于beautiful-jekyll的博客构建真的很简单，上传新文章也只需要在文件夹中添加Markdown文件，所以选择了这个架构！
* 同时，beautiful-jekyll的页面非常简洁美观，对于框架用法的介绍也写得非常详尽，很适合初学者选用！很赞！



## 博客制作过程中遇到的问题及其解决方法

* 在制作博客的过程中我主要遇到了三个问题：
  * 打开博客页面显示404 There isn't a GitHub Pages site here.
    * 排除了仓库名设置错误、pages配置错误等问题之后，我在GitHub中的action页面中查看得到，出现该问题是因为GitHub对config.ylm文件编译失败，对照报错信息我发现是因为该文件中不可以出现@符号，修改后解决问题
  * 无法修改首页title
    * 我最开始尝试在config.ylm文件中修改title，却发现页面的大标题始终没有被修改，我于是转而思考是不是其实应该是在某个html文件中直接进行修改，在翻阅了几乎所有文件之后我在index.html中完成修改（但是其实在博客页面就有edit this page按键可以直接跳转到index.html ^ ^
  * 博客首页显示全文而不是显示部分+ReadMore
    * 在博客首页展示全文十分影响美观，原本这个功能应该已经在框架中被成功实现了，但是当博客文章的内容是中文时就不能成功识别，（因为他只识别空格和英文标点作为分词），所以我调整了展示的词数，使文章在首页只展示第一段的内容，最后成功让首页变得好看了（一点）



## 总结与收获

* 在本次实验中我基于beautiful-jekyll搭建了一个简单的静态网页博客，并熟悉了博客首页设置以及文章的上传