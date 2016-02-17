---
title: 终端iTerm在Mac OS X下的solarized配色方案
date: 2016-02-15 18:21:09
tags:
- iTerm
- Mac OS X
- solarized
- 配色方案
categories: 日志
---

刚刚打开iTerm的时候，想必都是这个样子的，如果你的不是这样子，这还真不是我弄的~

![iTerm截图](/images/iterm_default.png)

时间长了，想换个风格，就变成了这样~

![iTerm截图](/images/iterm_solarized.jpg)
【左：Solarized Light，右：Solarized Dark】

怎么样？看上去很舒服吧

> [solarized](http://ethanschoonover.com/solarized)是目前最完整的 Terminal/Editor/IDE 配色项目，几乎覆盖所有主流操作系统(Mac OS X, Linux, Windows)、编辑器和 IDE(Vim, Emacs, Xcode, TextMate, NetBeans, Visual Studio 等)，终端(iTerm2, Terminal.app, Putty 等)。类似的项目还有 [Tomorrow Theme](https://github.com/chriskempson/tomorrow-theme)，不过这里使用的是solarized。

下面说下如何配置：

> git clone https://github.com/altercation/solarized.git

### iTerm
方案一：
* 解压刚刚下载的文件 solarized-master.zip
* 找到iterm2-colors-solarized文件夹
* 执行Solarized Dark.itermcolors/Solarized Light.itermcolors文件
* iterm菜单：iTerm > Preferences > Profiles > Colors > Load Presets下拉框
* 点开下拉选项，会看到Solarized Dark和Solarized Light两个选项，这就是刚刚执行的两个.itermcolors文件
* 选取其中一种配色方案

方案二：
* iterm菜单：iTerm > Preferences > Profiles > Colors > Load Presets下拉框 > Import
* 分别Import刚刚解压的solarized-master > iterm2-colors-solarized > Solarized Dark.itermcolors/Solarized Light.itermcolors文件
* 选取其中一种配色方案

至此还没有结束，要在Mac OS X 终端里舒服的使用命令行(至少)需要给2个工具配色，vim 和 ls，好，我们继续...

### Vim
Vim的配色最好和终端的配色保持一致，不然在iTerm里使用命令行Vim会很别扭：

> $ cd solarized
> $ cd vim-colors-solarized/colors
> $ mkdir -p ~/.vim/colors
> $ cp solarized.vim ~/.vim/colors/

> $ vi ~/.vimrc

写入：

`syntax enable`
`set background=dark`
`colorscheme solarized`

### ls
Mac OS X是基于FreeBSD的，所以一些工具ls，top等都是BSD那一套，ls不是GNU ls所以即使iTerm配置了颜色，但是在Mac上敲入ls 命令也不会显示高亮，可以通过安装coreutils来解决(brew install coreutils)，不过如果对ls颜色不挑剔的话有个简单办法就是在.bash_profile文件里写入CLICOLOR=1

> $ vi ~/.bash_profile

写入：

`export CLICOLOR=1`

经过上面的步骤，你的iTerm也就和我的显示的一样了，可以愉快的编码了~