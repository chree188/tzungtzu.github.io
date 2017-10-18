##《Deep Learning》读书笔记————第五章：Machine Learning Basics



####机器学习定义：
一个计算机程序，如果它能做到在任务T中的性能P随着经验E可以提高，那就可以称它是关于某类任务T和性能衡量P，从经验E中学习。

####机器学习任务（T）
类别：分类（classification）/缺失输入数据的分类（classification with missing data）/回归（regression）/转录（transciption）/机器翻译（machine translation）/结构化输出（structured output）/异常检测（anomaly detection）/合成和采样（synthesis and smapling）/缺失值填补（imputation of missing data）/去噪（denoising）/密度估计（density estimation）

####机器学习的性能（P）：
P因为T的不同而不同。对于像分类/缺失输入数据的分类/转录，使用准确率（accuracy）来衡量性能；而对于密度估计，通常输出模型在一些样本上概率对数的平均值。

####机器学习的经验（E）：
根据经验的不同，分为监督学习和无监督学习。监督学习：学习p(x)；无监督学习：学习p(y|x)。通常来说，无监督学习通常指代从不需要人工标注数据中提取信息。


1. 学习算法
    
2. 交叉验证
3. 