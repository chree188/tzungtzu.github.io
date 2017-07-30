---
layout: post
title: 新设备环境配置
categories: 
- Technology
tags:
- mac
- dropbox
- brew
- vim

---

### 1. 翻墙工具：
> Surge/Shadowsocks

### 2. 常用工具：
> Dropbox, Alfred, Paste，iTerm，Sublimes, Resilio, 1Password, Bartender, SourceTree, 

 <!--more-->

- 很多配置在 Dropbox 所以首先要下载 Dropbox, 个人将 licences，settings， backups 都存在 Dropbox。
- Alfred 通过 Advanced-Syncing 同步（必须主设备先同步，从设备的配置会被覆盖） workflow需要另外下载

### 3. 配置工作环境：

* Homebrew：
		/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
		

 Homebrew的使用
•	安装软件：brew install 软件名，例：brew install wget
•	搜索软件：brew search 软件名，例：brew search wget
•	卸载软件：brew uninstall 软件名，例：brew uninstall wget
•	更新所有软件：brew update
* Zsh:
		wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O - | sh
		#设置theme 
		#下载zsh语法高亮
		##brew install zsh-syntax-highlighting，需要把 source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh 添加到 .zshrc 的最后面。

[http://get.ftqq.com/992.get][1]
[http://blog.jobbole.com/80620/][2]

* python 
		brew install python

  * pip
		curl https://bootstrap.pypa.io/ez_setup.py -o - | sudo python
		sudo easy_install pip
		或者
		wget 
		sudo python get-pip.py

4.  vim语法高亮
		sudo cp /usr/share/vim/vimrc ~/.vimrc 
		sudo mkdir colors
		sudo mv solarized.vim ~/.vim/colors


### References:
1. [小土刀][3]()
2. [][4]()

[1]:	http://get.ftqq.com/992.get
[2]:	http://blog.jobbole.com/80620/
[3]:	http://wdxtub.com/2016/08/08/mac-work-env/
[4]:	https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md