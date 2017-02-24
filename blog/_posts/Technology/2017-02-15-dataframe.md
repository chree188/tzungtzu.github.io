---
layout: post
title: pandas 中 DataFrame 的分割和合并
categories: 
- Technology
tags:
- python
- pandas

---

pandas是基于Numpy构建的库。最主要的数据结构就是 Series 和 DataFrame。
DataFrame 是 pandas 库中一个二维表格形的数据结构，含有一组有序的列，每列可以是不同的值类型（数值、字符串、布尔）。DataFrame 既有行索引也有列索引，可以看成由 Series 组成的字典（共用同一个索引）。

在数据分析时经常用到 DataFrame 的分割和合并。总结一下自己遇到的情况。
 <!--more-->



### 取出一列

通过类似字典标记的方式或属性的方式，可以将 DataFrame 的列获取为一个 Series。返回的 Series 拥有原 DataFrame 相同的索引，name 属性也相应设置好了。行索引字段是ix。
 
	frame ['year'] = frame.year  
	frame.ix['three']  #获取行数据

### 删除一列

	frame.drop(['a','b']) #删除a，b行
	frame.drop([two],axis=1) #删除two 列。

### 添加一列

将列表和数组赋值给某个新列的时候，其长度必须和 DataFrame 的长度相匹配。如果赋值的是个 Series，就会精确匹配 DataFrame 的索引，所有的空位都会被填上缺失值。可以通过这个特性，修改 DataFrame 的格式。

	Frame['newcolumn'] = series  #在Frame 创建新列

### 改变一列的 type


	df[['a']]= df[['a']].apply(pd.to_numeric) #指定某列修改为int格式

如果直接进行全部改变，为了避免报错，可以将其他值变为 NaN
	pd.to_numeric(s, errors ="coerce")

### 修改索引

	obj = obj.reindex(['a','b','c','d','e'])
	frame = frame.reindex(index=[], cloumns=[])

### 将列变成索引

将某列作为列的索引，会生成一个新的 DataFrame
	frame2 = frame.set_index(['c'])

## 聚类

### 统计a列中元素的重复次数
	df.groupby('a').size()


### 统计a列中不同元素在b列的求和

	df.groupby('a').sum()

### 合并两个dataframe

	pd.merge(alb)
