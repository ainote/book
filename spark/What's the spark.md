# Spark知识汇总

## 什么是Spark

> Apache Spark™ is a unified analytics engine for large-scale data processing.

上面这句话是官网的定义：`Spark是一个大规模数据处理的统一分析引擎。`

> Spark 是一个用来实现快速而通用的集群计算的平台。--出自《Spark快速大数据分析》

Spark是基于内存的批量数据处理框架，数据以RDD(弹性分布式数据集)的形式存放在内存里。Spark作为统一数据处理引擎可以批量处理离线数据(离线计算)、实时数据(实时计算)、机器学习以及图计算，这些组件也都以RDD作为支撑进行数据计算。Spark离线计算中可以使用类SQL的Spark SQL组件，Spark SQL主要使用类SQL进行数据分析，SQL语法兼容Hive语法。  

Spark的特点：
（1）基于内存计算速度快。Spark计算速度快是相对于Hadoop的MapReduce而言，基于Hadoop的MapReduce在计算时将中间结果存储在本地磁盘会产生大量的IO操作，而Spark是放在内存计算因此要快一些。  
（2）统一的软件栈。Spark底层以RDD为支撑，可以使用Spark SQL进行数据分析和处理，利用Spark Streaming 进行实时计算，其中的mllib包中实现了常用的机器学习算法用于数据科学，以及包含了图计算。  
（3）提供了多种语言接口。Spark 应用开发支持Scala、Java和Python三种编程语言满足不同用户的使用需求。  
（4）Spark可以运行在不同的资源调度管理器上如 YARN,Mesos,Kubernetes, Standalone 或者云环境等。

## 什么是RDD

RDD(弹性分布式数据集,Resilient Distributed Dataset)是Spark数据计算的一个基本抽象，表示了一个不可变、分区的数据集合，该数据集合可以并行计算。RDD具有数据流模型的特点：自动容错、位置感知性调度和可伸缩性。

> Internally, each RDD is characterized by five main properties:
>
> - A list of partitions
> - A function for computing each split
> - A list of dependencies on other RDDs
> - Optionally, a Partitioner for key-value RDDs (e.g. to say that the RDD is hash-partitioned)
> - Optionally, a list of preferred locations to compute each split on (e.g. block locations for an HDFS file)

以下斜体内容引用自:(<https://www.cnblogs.com/pingzizhuanshu/p/9146714.html>)  
*(1) 一组分片（Partition），即数据集的基本组成单位。对于RDD来说，每个分片都会被一个计算任务处理，并决定并行计算的粒度。用户可以在创建RDD时指定RDD的分片个数，如果没有指定，那么就会采用默认值。默认值就是程序所分配到的CPU Core的数目.*

*(2) 一个计算每个分区的函数。Spark中RDD的计算是以分片为单位的，每个RDD都会实现compute函数以达到这个目的。compute函数会对迭代器进行复合，不需要保存每次计算的结果。*

*(3) RDD之间的依赖关系。RDD的每次转换都会生成一个新的RDD，所以RDD之间就会形成类似于流水线一样的前后依赖关系。在部分分区数据丢失时，Spark可以通过这个依赖关系重新计算丢失的分区数据，而不是对RDD的所有分区进行重新计算。宽依赖和窄依赖。*

*(4) 一个Partitioner，即RDD的分片函数。当前Spark中实现了两种类型的分片函数，一个是基于哈希的HashPartitioner，另外一个是基于范围的RangePartitioner。只有对于key-value的RDD，才会有Partitioner，非key-value的RDD的Parititioner的值是None。Partitioner函数不但决定了RDD本身的分片数量，也决定了parent RDD Shuffle输出时的分片数量。*

*(5) 一个列表，存储存取每个Partition的优先位置（preferred location）。对于一个HDFS文件来说，这个列表保存的就是每个Partition所在的块的位置。按照“移动数据不如移动计算”的理念，Spark在进行任务调度的时候，会尽可能地将计算任务分配到其所要处理数据块的存储位置.*
