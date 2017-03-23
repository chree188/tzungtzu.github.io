---
layout: post
title:  Integrate Spark(Scala & PySpark) with Jupiter Notebook
categories: 
- Technology
tags:
- Jupyter Notebook
- Spark
- Scala
- Toree

---

Jupyer Notebook is an interactive notebook environment and it supports Spark.



### 1 . jupyter Notebook installation

### 2 . Scala, Spark installation

### 3 . **Toree installation**

 Apache Toree is tool to configure Jupiter notebook to run with Spark.

	$sudo pip install -i http://pypi.anaconda,org/hyoon/simple toree

 <!--more-->

### 4 . Configure different Apache Toree kernels

for Scala:

	$jupyter toree install spark_home=~/data/spark-2.0.1-bin-hadoop2.6/
 
for PySpark:

	$jupyter toree install --spark_home=~/data/spark-2.0.1-bin-hadoop2.6/  --interpreters=PySpark

even SparkR, SQL

	$Jupyter toree install --interpreter=SparkR,SQL

### 5 .  and you can Check installation by
	$jupyter kernelspec list



### references:

1. [https://toree.incubator.apache.org/documentation/user/installation.html][1]
2. [http://stackoverflow.com/questions/39149541/integrate-pyspark-with-jupyter-notebook][2]


<details>
<summary> More details</summary>

Detail test


</details>

[1]:	https://toree.incubator.apache.org/documentation/user/installation.html "Apache Toree Installation"
[2]:	http://stackoverflow.com/questions/39149541/integrate-pyspark-with-jupyter-notebook " solution is to install Apache Toree."