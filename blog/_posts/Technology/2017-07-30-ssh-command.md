---
layout: post
title: ssh 常用命令
categories: 
- Technology
tags:
- ssh
- scp

---

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
