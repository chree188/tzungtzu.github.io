#learning spark

##RDD 编程

弹性分布式数据集：元素的分布式集合。

Spark 的工作：
1. 创建新 RDD
2. 对存在的 RDD 做变换
3. 对RDD 调用操作计算出结果

在底层， Spark 将包含在 RDD 中的数据自动分布到整个集群，并将你对其执行的操作并行化。

###创建RDD

用户可以用两种方式创建 RDD：【常见】通过加载一个外部数据集， 或者【简单】在驱动程序中分发一个对象集合（如 list 或 set）。

最简单的创建 RDD 的方式就是将你程序中已存在的集合传递给 SparkContext 的 parallelize()方法，

针对外部读取数据： path = "file:///home/ubuntu/data/spark-2.0.1-bin-hadoop2.6/LICENSE"

    spark默认是从hdfs读取文件，也可以指定sc.textFile("路径").在路径前面加上hdfs://表示从hdfs文件系统上读
    本地文件读取 sc.textFile("路径").在路径前面加上file:// 表示从本地文件系统读，如file:///home/user/spark/README.md


总是重新计算一个 RDD 的能力事实上就是为什么 RDD 被称为“弹性”的原因。

###RDD操作

1. transfer 变换：操作得到一个新的RDD（变换创建RDD
2. action 动作： 返回一个结果到驱动程序或者写入到存储并开始计算的操作（对数据做什么

大多数情况下，RDD 都不能 collect()到驱动程序，因为 RDD 一般都太大。这样 的话，通常是将所有数据输出到分布式存储系统中，如 HDFS 或 S3 等。你可以 用 saveAsTextFile()，saveAsSequenceFile()或者任何其他各种内置格式的动作来保 存 RDD 的内容。

值得注意的是，每次我们调用一个新动作，整个 RDD 都必须“从头开始”计算。 要避免低效，用户可以像 44 页提到的“持久化（缓存）”那样持久化中间结果。


###传递函数到Spark

大多数的 Spark 的变换和一些动作都依赖于向 Spark 传入函数，这些函数被 Spark 用于计算数据。各个语言对于传递参数到 Spark 的机制有些细微的差异。

在 Python 中，传递函数到 Spark 有三种方式。
    1. 对于较短的函数，可以通过 lambda 表达式来传递，或者，也可以用顶级函数或者局部定 义的函数。




###常见变换和动作

* 元素级的变换： map(), filter(), flatmap() 每个输入元素返回多个输出元素
* 伪集合操作：distinct(), union(RDD2),intersection(), substract()
    - distinct()很昂贵，因为它需要所有的数据通过网络进行 Shuffling 以确保唯一性。
* 