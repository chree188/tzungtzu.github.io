##关于复杂网络反欺诈

实现多种场景的大数据的可视化实时关联分析和追踪。

提供基于动态社团分割算法的自动化团伙欺诈的可视化分析报告，为客户提升团伙调查效率。

跨行业的联防联控，为行业提供欺诈情报支撑。

###知识图谱

基于知识图谱的复杂网络同样也应用于银行的反欺诈。其中最难也是最重要的一点就是把不同来源的数据整合在一起。比如，把一个借款者相关的所有数据，比如消费记录、行为记录、网络浏览记录、人际关系等数据整合到知识图谱网络中，用以对该借款者的欺诈行为进行检测。




传统的反欺诈手段包括身份验证、客户信息逻辑校验、外部信息的对比校验、黑名单过滤等方式主要还是在识别个人风险，无法根据千丝万缕的关系挖掘潜在的群体欺诈，这就需要基于网络的全局风险识别能力来覆盖风险漏洞。




在金融场景中，其实每一个申请人、手机号、设备、IP地址都是图中的结点，而诸如申请人拥有设备、手机号呼叫手机号等有向联系就是图中的边，边的权重为关联的紧密程度。在我们构建的图中，那些有违约与否标记的申请人是原始种子结点，通过使用基于图的半监督算法，把是否违约的标记传播给无标签的申请人，这样我们就可以在少量有标签的样本上构建出极为庞大的风险网络，最终打造形成我们有效可靠的违约预测模型。

---

图模型是在反欺诈领域中广泛应用的一类模型。通过用户注册、激活、登录、下单等环节收集到的账户、设备信息，我们可以构建出用户间不同的关系网络，从中发现欺诈的迹象和线索。其中一种使用这些关系网络的方法是，识别网络中异常的网络结构和社群。常用的社群挖掘方法有Walktrap, InfoMap, FastGreedy 等，这类模型通过识别紧密关联的社群结构找出潜在的欺诈客群，通常在刷单识别和套现识别的场景中有非常高的准确度。另一种思路是通过好坏用户的网络关系进行传播，可以使用标签传播算法(Label Propagation)，传染病学模型(SIR Model), 以及概率图模型(MRF, CRF等)。感兴趣的知友可以参考今年ASONAM上的Graph assisted semi supervised learning for fraudulent detection (下载链接)，文章详细介绍了如何使用"用户-商户"网络进行准确的欺诈推断。




对于“白户”、团伙欺诈，社交网络分析都可以提供很好的解决方案。

首先给出一些概念：

- X阶联系人：联系人可分为直接和间接联系人，直接联系人是指和申请人有过直接通话记录的号码，我们称其为一阶联系人，间接联系人是指联系人的联系人，依次可以分为二阶联系人、三阶联系人等，显然直接联系人比间接联系人更能影响种子号码，越高阶联系人，影响力越弱。

- 联系强度：根据两个号码之间通话频次、周期性、主被叫关系等来判断两个号码之间紧密的程度，用于衡量两个人之间可以互相影响的程度。

- 有效联系人：联系强度达到某个特定值以上的联系人

- 黑号个数/比例：在某个特定网络中被标为黑名单的号码个数/比例

Google的PageRank 是个很好的计算网页排名的算法，我们借鉴其能量传输的理念，并在此基础上做了些针对性的改进：对于联系人我们只考虑5阶以内，并对联系强度设定了阀值，只考虑大于特定强度的联系人，同时区分主被叫关系，在此条件下可以得到初始网络，通过聚类、能量传输等模型把7亿人群分割成若干个子网络，然后计算各价联系人中黑号个数、比例、网络大小等指标，并根据联系强度等信息差异性赋权，最终得出每个号码和黑号的紧密程度。聚信立依此计算出了特有的“灰度分”，经机构测试KS可达20%+，被广泛应用于众多机构风控建模中并占了很高权重。


我们用“白户”紧密联系人的加权信用等级来代表他自己的信用等级。


但如果看整个网络，就会发现某些圈子里的人的开户时间、联系人个数、通话时间、通话频率等方面都惊人的相似

本周： 研究社群挖掘