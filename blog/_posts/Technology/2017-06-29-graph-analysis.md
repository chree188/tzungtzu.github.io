# Graph Analysis


1. Centrality

$$E = mc^2$$

This expression 
$\sqrt{3x-1}+(1+x)^2$ is an example of a $\LaTeX$ inline equation.he Lorenz Equations:
$$\begin{aligned}\dot{x} & = \sigma(y-x) \\\dot{y} & = \rho x - y - xz \\\dot{z} & = -\beta z + xy\end{aligned}$$

+ node centrality
	* $Cd（vi）=di/(n-1)$
+ closeness centrality
	* Cc(vi)=1/(sigma(lij)/(n-1))
	* 那些在社交网络中经常与人互动、人际关系颇好的人，比如公司中的八卦传播者，往往亲近中心性得分较高。
	* 消息传播者
+ betweenness centrality
	* Cb(vi)=sigma(list/lst)
	* cb(vi)norm = cb(vi)/(n-1)(n-2)
	* 节点的居间程度越大，那么它在节点相互之间的信息传播起到的作用也就越大。在两个社会网络之间的人，比如跨界者，往往拥有较高的居间中心性。
	* 所以在社区分析的时候，也是重要的评判标准

+ eigenvalue centrality
	* 网络中的每个节点都有一个相对指数值，高指数节点的连接对一个节点的贡献度比低指数节点的贡献度高。
当前节点的中心性取决lj于邻居节点们的中心性。

+ cluster coefficirnt
	*  顶点之间结集成团的程度的系数
	*  C= 3×tri/（3×tri+open tri）zs
	*  Ci = 2|ejk|/i(i-1)

三种指标所表达的“重要”，其含义是不完全一样的

2. 社区发现
2. GN
	* 分裂法
3. Louvain
	* 模块度 (http://www.cnblogs.com/tychyg/p/5277137.html)
	* 模块度（modularity）指的是网络中连接社区结构内部顶点的边所占的比例，减去在同样的社团结构下任意连接这两个节点的比例的期望值。
4. label propagation algrithm
5. K-means
