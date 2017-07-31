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

• 添加到环境变量 `echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile`
• 检查并更新 `brew doctor; brew update`
• 安装包 `brew install <package_name>`
• 更新包 `brew upgrade <package_name>`
• 清理旧版本 `brew cleanup`
• 列出包 `brew list --versions` 

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