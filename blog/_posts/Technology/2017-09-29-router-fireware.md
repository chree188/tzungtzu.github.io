---
layout: post
title: 可编程路由器初体验
categories: 
- Technology
tags:
- router
- asus
- ss
- aria

---


###宽带知识：
简单说，现在2.4G的协议一般是802.11n,5G协议是802.11ac,按协议标准（老的不说了）2.4g每根天线150M，5G每根天线433M。（协议天线数，不是实际这货长几根天线）

那么我们现在最差的2.4G都有150M的速度了，俺们家宽带才20M呢，随便买个破路由就足够了吧。。。这里我回答你：是的，但请你住在火星上去，地球干扰太多鸟

<!--more-->

###路由

1. 现阶段20M及以上宽带，至少要买CPU在500MHZ以上的。（请注意，乃们以前用的80块的TP应对的是2M，4M宽带）
2. 最好带5G
3. 固件稳定（就是路由的操作系统）
4. 最大功率最好可调


最大功率是指一个路由的最大无线发射功率，咱们伟大的祖国为了保护我们这些花朵，规定无线最大功率应该是100mv,实际上市面上的路由大多在10-50mv ,例如华硕，思科等，默认都是在30-50mv之间。美国规定是200mv,还有些小国家规定320mv.......

所以有切换的确改变最大功率的说法。（无线网络-专业设置- region）

关于频率，2.4GHz的绕墙效果比5GHz更加出色。频率越高的电磁波穿过障碍物损失更多的能量，因此5GHz在穿透墙时，消耗了更大的能量，而2.4GHz走的路径会更长一些，留下来的能量会更多一些。5GHz相比于2.4GHz拥有更广的信道，目前国内规定的可用的5G信道只有149、153、157、161、165（民用）

###固件

梅林固件 - koolshare 改版梅林固件 

插件：

####Adbyby

梅林改版固件暂时不支持

####配置 SS

设置 LAN SSH，全部打勾，

        ssh username@192.168.1.1
        cd /tmp
        wget -N -O shadowsocks.tar.gz http://www.xiazai.ml/Router/merlin/离线包/shadowsocks_3.6.0.tar.gz
        tar -zxvf /tmp/shadowsocks.tar.gz
        chmod +x /tmp/shadowsocks/install.sh
        sh /tmp/shadowsocks/install.sh



适合国情的固件功能有：

SS，玩游戏（PS4）的朋友则需要支持NAT2的SS
VPN
下载工具
双拨
硬盘共享工具（samba/ftp等） download master
去广告工具（adm/adbyby)
有双线的朋友：策略路由
最好有给力的QOS，，但这个太少了‘


一些问题：

1. 7.4 有温度不能显示的问题
2. Asus Router 的 iOS app 有 bug, 无法添加修改名字的 Router，安卓版本没有这个问题。
3. 安卓手机可以用 Wi-Fi Analyzer 来测试 Wi-Fi 强度。

### References:
1. [](http://koolshare.cn/thread-110214-1-1.html)
2. [常用插件](https://post.smzdm.com/p/430693/)
3. [家庭wifi测试](https://post.smzdm.com/p/427541/)
4. [路由器](https://post.smzdm.com/p/555403/?nozhiyou)
5. [安装ss](http://www.ti6.net/internet/3225.html)
6. [ss git 地址](https://github.com/koolshare/koolshare.github.io/blob/acelan_softcenter_ui/shadowsocks/shadowsocks.tar.gz)
7. [小宝梅林固件](http://koolshare.cn/thread-110214-1-1.html)
8. [aria 配置](https://post.smzdm.com/p/369442/)
9. [家庭网盘](http://www.sohu.com/a/118119233_160148)
10. [aria 远程操作](http://koolshare.cn/thread-30944-1-1.html)
11. [DDOS](https://post.smzdm.com/p/549942/)
