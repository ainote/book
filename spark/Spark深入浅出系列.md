本文的内容来自以下地址：
[1]  [深入浅出 Spark（一）：内存计算的由来](<https://www.infoq.cn/article/oPpQzsJIFopeBpzVcbx7>)
[2]  [深入浅出 Spark（二）：血统（DAG）](https://www.infoq.cn/article/LBzKJPoaFAre5c0cI4ur)
[3]  [深入浅出 Spark（三）：Spark 调度系统之“权力的游戏”](https://www.infoq.cn/article/5aOHzQIaXX6NlHriLtSI)
[4]  [深入浅出 Spark（四）：存储系统](https://www.infoq.cn/article/CivudeR65oRP1lYODS8A)


在博文2中描述了DGAScheduler的职责：是将抽象的DAG计算图转换为具体的、可并行的分布式计算任务。其第一步是将DAG计算图拆分为不同的Stage，DAGScheduler以Stage为粒度进行任务调度。
**如何划分Stage？**
DAGScheduler从尾节点开始向各个首节点遍历，并判断每个RDD与父RDD的依赖关系(NarrowDependency和ShuffleDependency)。
首先，DAGScheduler 沿着 DAG 的尾节点一路北上，并沿途判断每一个 RDD 节点的 dependencies 属性。之后，如果判定 RDD 的 dependencies 属性是 NarrowDependency，则 DAGScheduler 继续向前回溯；若 RDD 的依赖是 ShuffleDependency，DAGScheduler 便开启“三招一套”的招式，创建 Stage、注册 Stage 并继续向前回溯。由此可见，何时切割 DAG 并生成新的 Stage 由 RDD 的依赖类型决定，当且仅当 RDD 的依赖是 ShuffleDependency 时，DAGScheduler 才会新建 Stage。
**DAGScheduler 怎么知道 RDD 的依赖类型到底是哪一个？他怎么判别 RDD 的依赖是窄依赖还是 ShuffleDependency？**
Partitioner 是 RDD 的分区器、定义了 RDD 数据分片的分区规则，它决定了 RDD 的数据分片在分布式集群中如何分布，这个属性至关重要，后面介绍 Shuffle 的时候我们还会提到它。DAGScheduler 正是通过 partitioner 来判定每个 RDD 的依赖类型，具体来说，如果子 RDD 的 partitioner 与父 RDD 的 partitioner 一致，那么 DAGScheduler 判定子 RDD 对父 RDD 的依赖属于窄依赖；相反，如果两者 partitioner 不一致，也即分区规则不同（分区规则不同则意味着一定存在数据的“重洗牌”，即 Shuffle），那么 DAGScheduler 判定子对父的依赖关系是 ShuffleDependency。