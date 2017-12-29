---
layout: post
title: ssh 常用命令
categories: 
- Technology
tags:
- ssh
- scp

---

传统的网络服务程序，如 rsh、FTP、POP 和 Telnet 其本质上都是不安全的；因为它们在网络上用明文传送数据、用户帐号和用户口令，很容易受到中间人（man-in-the-middle）攻击方式的攻击。就是存在另一个人或者一台机器冒充真正的服务器接收用户传给服务器的数据，然后再冒充用户把数据传给真正的服务器。


### - 登陆
		ssh 主机名@主机IP   #输入对方密码就ok了。如果需要pem，加入-i。
### - 远程复制(secure copy)

 <!--more-->

	scp -r  要传输的文件  我的主机名@主机的IP：路径
	scp [参数] [原路径] [目标路径] ##-r 递归复制整个目录。

从本地服务器复制到远程服务器
	scp local_file remote_username@remote_ip:remote_folder
	$scp -r local_folder remote_username@remote_ip:remote_folder

### - 关闭远程登录
		exit  #主动断开和对方的连接
		

### - 重启服务器
		sudo reboot

### - 关机
		shutdown -h now 现在立即关机
		shutdown -r now 现在立即重启
		shutdown -r +3 三分钟后重启



### References:
1. [[SSH 系列 1]：什么是 SSH、背景知识，SSH 协议需求与设计难点 | 土豆不好吃](https://www.bennythink.com/ssh-1.html)