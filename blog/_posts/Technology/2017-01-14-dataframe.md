

---
layout: post
title: DataFrame 列的提取与添加
categories: 
- Technology
tags:
- python
- pandas

---

pandas是基于Numpy构建的 
Series 在算术运算时自动对其不同索引的数据 

DataFrame 是 pandas 库中一个二维表格形的数据结构，含有一组有序的列，每列可以是不同的值类型（数值、字符串、布尔）。DataFrame 既有行索引也有列索引，可以看成由 Series 组成的字典（共用同一个索引）。


 <!--more-->

返回的 Series 拥有原 DataFrame 相同的索引，name 属性也相应设置好了。
行索引字段是ix 

	frame ['year'] = frame.year


将列表活数组赋值给某个新列的时候，其长度必须和 DataFrame 的长度相匹配。如果赋值的是个 Series，就会精确匹配 DataFrame 的索引，所有的空位都会被填上缺失值。

	Frame['newcolumn'] = series


