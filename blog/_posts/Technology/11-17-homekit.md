###mac 安装 homebridge

1. Xcode
2. homebrew
3. nodejs npm
 
        brew install node
    
    To test out your Node and npm install, try installing Grunt (you might be asked to run with sudo):

        npm install -g grunt-cli
4. homebridge
 
        sudo npm -g install homebridge
        or
        sudo npm install -g --unsafe-perm homebridge

5. 
        homebridge




犹豫现在使用的是 macbook 运行 homebridge，所以需要 macbook 合盖不休眠。

所以需要运行：
        
         caffeinate -disu &



###google home


###hass

 概念

HomeKit：苹果于 2015 年 5 月发布的智能家居平台。
HomeBridge：一个开源程序，用于让 HomeKit 支持一些原生不支持 HomeKit 的设备（如米家家居）。
HomeAssistant：一个第三方的智能家居平台。



### References:
1. [小米网关接入Homekit | El Psy Congroo](http://blog.yongbin.me/2017/03/14/homebridge/)
2. [Homebridge + Mac 智能家居指南一：介绍及安装篇](https://zhuanlan.zhihu.com/p/26484470)
3. [gyp WARN EACCES user "root" does not have permission to access the dev dir "/root/.node-gyp/4.2.2" · Issue #405 · nfarina/homebridge](https://github.com/nfarina/homebridge/issues/405)
4. [xcode-select: error: tool 'xcodebuild' requires Xcode, but active developer directory '/Library/Developer/CommandLineTools' is a command line tools instance · Issue #569 · nodejs/node-gyp](https://github.com/nodejs/node-gyp/issues/569)
5. [一分钟教你搞懂，Yeelight联动Google Home这件事！ Yeelight](https://www.yeelight.com/zh_CN/blog/62)
6. [智能家居场景之一：配合 Google Home 来控制 Yeelight 灯泡 - Wei Xia's Blog](http://weixia.info/2018/01/02/yeelight-with-google-home/)
