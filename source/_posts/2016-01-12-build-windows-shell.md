title: Best Node Development Environment on Window
date: 2016-01-12 01:34:52
categories:
- Utility
---
In this article, I'll show you how to build an environment on windows that gives you the same experience in developing Node as on Linux or Osx. There's a preview:
![preview](http://7xqh47.com1.z0.glb.clouddn.com/build_windows_shell/preview.png)

## Git Bash
Git bash provides you powerful commands such as git and ssh, it will be installed with [Git](https://git-scm.com/download/win).

## Node Version Manager for Windows
Node version manager helps you manage and switch your Node version easily. I recommended [nvm-windows](https://github.com/coreybutler/nvm-windows) on windows, who will place a link of current version of Node at regular Node installation path and set environment variables for you automatically.

## ConEmu
[ConEmu](https://github.com/Maximus5/ConEmu) supports multiple tabs of console, with plenty of configuration for customization(You can run any windows application in ConEmu, exactly). 

## Taobao npm registry(In China)
Within GFW, there may be problem while trying to install some packages. Use taobao npm registry:
```
npm config set registry https://registry.npm.taobao.org
```
ATTENTION: you must reconfigure npm after node version changing.

- - - - - - - - - -
## Reference
[国内优秀npm镜像推荐及使用](http://riny.net/2014/cnpm/)








