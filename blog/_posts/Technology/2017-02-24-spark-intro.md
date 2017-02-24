---
layout: post
title: Spark 入门遇到的一些坑
categories: 
- Technology
tags:
- spark
- scala

---



Apache Spark 是一个新兴的大数据处理通用引擎，提供了分布式的内存抽象。

用[官方文档][1]入门的时候遇到一些问题，以下是解决办法。

 <!--more-->


### 1.  找不到 README.md 文件
需要将Spark目录下的README.md 文件放到Spark使用的文件系统的相应位置。如果使用的是HDFS，应该放在 /usr/YOUR\_USER\_NAME 目录下，或者将文件路径改为绝对路径。如：

	val textFile = “/usr/mint/README.md” 

### 2. 安装 simpleApp 的目录结构
新建文件夹，包含simpleApp.scala, simple.sbt 两个文件

### 3. 无法使用 sbt
Spark 中没有自带 sbt，需要自行[安装][2]




[1]:	https://spark.apache.org/docs/latest/quick-start.html
[2]:	http://www.scala-sbt.org/0.13/docs/zh-cn/Installing-sbt-on-Linux.html