---
title: 猴年马月🐵🐴
date: 2016-02-01 15:06:34
tags:
- 开始
- 新的一年
categories: 日志
---

***
这是**新的开始**

![赢在猴年](/images/monkey.jpg)
***

### Hexo + Github 搭建博客

> A fast, simple & powerful blog framework, powered by Node.js.

准备工作：node环境、github，这里就不多说了~

进入正题 - **Hexo的安装**

1、 全局安装hexo
> npm install -g hexo

2、 创建hexo目录
> cd ~
> mkdir hexo

3、 初始化hexo
> cd hexo
hexo init

hexo文件夹下就回生成如下文件
![初始化hexo](/images/hexo_init.jpg)

4、 安装dependencies（依赖），生成node_modules目录
> npm install

5、启动hexo服务
> hexo server

command + 单击（http://0.0.0.0:4000/）

![hexo默认页面](/images/hexo.jpg)

***
哇，成功了，可是为什么显示的和你的不一样！

莫急，这只是hexo默认的主题（themes/landscape），主题是可以自己配置的。

鉴于个人审美不同，认为默认主题也ok，可忽略此步骤~

我的博客使用的theme是[TKL](https://github.com/SuperKieran/TKL.git)，下面就以此为例，来介绍下主题配置。

> git clone https://github.com/SuperKieran/TKL.git
> cp -r TKL themes
> rm -rf TKL

主题下载完就该应用了
> vi _config.yml

替换themes配置项值landscape为TKL，刷新下页面，新的theme已经生效了，接下来就是进入到themes/TKL/下的_config.yml替换下文本，logo，链接之类的

***


6、 新建hexo文件（文件创建在source/_posts/下）
> hexo new fileName






生成静态文件
> hexo generate	[生成静态文件]

> hexo deploy	[部署]

> npm install --save hexo-deployer-git

> 配置_config.yml

