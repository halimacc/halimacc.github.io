title: 搭建Windows下的Node开发环境
date: 2016-01-12 01:34:52
categories:
- 开发环境
---

本篇文章将介绍如何在Windows下搭建一个仅稍逊于Mac下iterm2+tmux+nvm的Node开发环境。
- - - - - - - - - -
## 1. Node.js环境
在Windows下，我们使用nvm-windows和淘宝npm镜像来提升node和npm的使用体验。
### 安装nvm-windows
在Linux或Mac下，使用Node版本管理器nvm(Node Version Manager)来管理Node版本可以非常轻松的更新和切换Node，Windows下则有nvmw和nvm-windows。个人认为[nvm-windows](https://github.com/coreybutler/nvm-windows)的优点更多，主要是会自动配置环境变量、利用link将Node安装在常用位置。虽然nvm-windows不支持io.js的版本管理，但是在Node v4之后io.js合并了回来，这也不算是个问题了。安装好之后就可以打开cmd或者Powershell来使用nvm了。
### 使用淘宝npm镜像
要想开开心心的使用Node，还需要修改npm源。由于npm源在国外，直接使用的话会出现有库些安装不了的情况。国内比较好的源就是淘宝npm镜像了，最简单的修改源的方法是在cmd或Powershell输入如下内容。
```
npm config set registry https://registry.npm.taobao.org
```
要注意使用nvm切换Node版本之后npm也需要重新配置哦。
- - - - - - - - - -
## 2. 命令行环境
在Mac和Linux下进行Node开发相比于Windows最大的优势就在于命令行操作了，利用termimal或者iterm2再加上tmux，写代码、查数据库、ssh连接服务器切换自如。在Windows下，博主在失去Mac之后经过多年（误）的探索，终于找到了一个不错的替代组合：ConEmu+Git Bash+Windows Powershell。
### 安装Git
[Git](https://git-scm.com/download/win)附带的Git Bash能够提供强大的命令行支持，例如ssh远程连接服务器等。
### 安装ConEmu
[ConEmu](https://github.com/Maximus5/ConEmu)是一个可以同时打开多个Tab的命令行模拟器，最大的优势在于能够同时打开多个cmd、Powershell和Git Bash窗口，可配置性也很强。
- - - - - - - - - -
## 参考
[国内优秀npm镜像推荐及使用](http://riny.net/2014/cnpm/)








