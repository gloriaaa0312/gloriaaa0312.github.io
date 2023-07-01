---
layout: post
title: 数据科学与工程学院暑期夏令营实践项目
subtitle: 基于 GitHub 的博客网站

tags: [实验报告]
comments: true
---



## 博客主题及其选取原因

* 本次选用[beautiful-jekyll](https://github.com/daattali/beautiful-jekyll)为架构搭建了一个简单的静态网页博客，beautiful-jekyll是一个基于HTML的十分完善的框架，由于本地的Ruby环境安装不下来，而且基于beautiful-jekyll的博客构建真的很简单，上传新文章也只需要在文件夹中添加Markdown文件，所以选择了这个架构！
* 同时，beautiful-jekyll的页面非常简洁美观，对于框架用法的介绍也写得非常详尽，很适合初学者选用！很赞！



## 博客页面展示

#### 首页：

![main](https://github.com/gloriaaa0312/gloriaaa0312.github.io/blob/master/assets/img/main.png?raw=true)

* 点击左上角可回到首页，右上角ABOUT ME链接到介绍页面，放大镜进入搜索页面。在首页可以按时间倒序浏览全部文章。

#### ABOUT ME：

![aboutMe](https://github.com/gloriaaa0312/gloriaaa0312.github.io/blob/master/assets/img/aboutme.png?raw=true)

* 展示了简单的介绍和联系我的方式，在这里遇到一个问题，即在Markdown与GitHub中能显示emoji，但在博客中无法显示，暂时没有找到合适的解决方案，如图：

![error](https://github.com/gloriaaa0312/gloriaaa0312.github.io/blob/master/assets/img/error.png?raw=true)

#### 搜索：

![search](https://github.com/gloriaaa0312/gloriaaa0312.github.io/blob/master/assets/img/search.jpg?raw=true)

* 如图，博客实现了多种搜索方式，包括按文章名搜索、按文章标签搜索、按文章发表时间搜索等方式

#### 文章：

![article](https://github.com/gloriaaa0312/gloriaaa0312.github.io/blob/master/assets/img/article.png?raw=true)







## 博客制作过程中遇到的问题及其解决方法

* 在制作博客的过程中我主要遇到了四个问题：
  * 打开博客页面显示404 There isn't a GitHub Pages site here.
    * 排除了仓库名设置错误、pages配置错误等问题之后，我在GitHub中的action页面中查看得到，出现该问题是因为GitHub对config.ylm文件编译失败，对照报错信息我发现是因为该文件中不可以出现@符号，修改后解决问题
  * 无法修改首页title
    * 我最开始尝试在config.ylm文件中修改title，却发现页面的大标题始终没有被修改，我于是转而思考是不是其实应该是在某个html文件中直接进行修改，在翻阅了几乎所有文件之后我在index.html中完成修改（但是其实在博客页面就有edit this page按键可以直接跳转到index.html ^ ^
  * 博客首页显示全文而不是显示部分+ReadMore
    * 在博客首页展示全文十分影响美观，原本这个功能应该已经在框架中被成功实现了，但是当博客文章的内容是中文时就不能成功识别，（因为他只识别空格和英文标点作为分词），所以我调整了展示的词数，使文章在首页只展示第一段的内容，最后成功让首页变得好看了（一点）
  * 如上文所述，无法显示emoji



## 总结与收获

* 在本次实验中我基于beautiful-jekyll搭建了一个简单的静态网页博客，并熟悉了博客首页设置以及文章的上传