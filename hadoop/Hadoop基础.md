
# 1. 什么是Hadoop?

从Hadoop的官网(<http://hadoop.apache.org/>)的描述，可将Hadoop看作是一个开源项目用于**可靠的、可扩展**的分布式计算。Hadoop可以看作是一个分布式开源框架，可以使用的简单的编程模型进行集群大规模数据的分布式计算，它并不依赖昂贵的硬件以支持高可用性。从现在大数据技术角度来看，Hadoop通常是指Hadoop的生态圈，包括其他比较流行的分布式计算框架如Spark、Hive、Flink、HBase等。Hadoop的核心组件主要有分布式文件系统(HDFS,Hadoop Distributed File System)、计算模型(MR,Map Reduce)和资源调度器(YARN)。  

> * HDFS：主要用于海量数据的分布式存储，具有高可用、强容错性等特点。
> * MapReduce： 用于分布式计算模型，将分布式计算逻辑抽象为Map阶段和Reduce阶段。
> * YARN : 主要用于分布式资源的协调与调度，用于任务资源的分配以及调度执行。

# 2. Hadoop部署运行模式

版权声明：本文为CSDN博主「夏至&amp;未至」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：<https://blog.csdn.net/qq_35571554/article/details/83216656>

Hadoop支持三种部署模式：单节点(单机版)部署,伪分布式模式,完全分布式模式。

* 单机模式（独立模式）（Local或Standalone  Mode），默认情况下，Hadoop即处于该模式，该模式主要用于开发和调式。
  * 不对配置文件进行修改。
  * 使用本地文件系统，而不是分布式文件系统。
  * Hadoop不会启动NameNode、DataNode等守护进程，Map和Reduce任务作为同一个进程的不同部分来执行的。
  * 用于对MapReduce程序的逻辑进行调试，确保程序的正确。
* 伪分布式模式（Pseudo-Distrubuted Mode）
  * Hadoop的守护进程运行在本机机器，模拟一个小规模的集群。
  * 在一台主机模拟多主机。
  * Hadoop启动NameNode、DataNode这些守护进程都在同一台机器上运行，是相互独立的Java进程。在这种模式下，Hadoop使用的是分布式文件系统(HDFS)，这种模式常用来开发测试Hadoop程序的执行是否正确。
  * 修改3个主要配置文件：core-site.xml（Hadoop集群的特性，作用于全部进程及客户端）、hdfs-site.xml（配置HDFS集群的工作属性）、mapred-site.xml（配置MapReduce集群的属性）、yarn-site.xml文件(用于集群资源的调度)。
* 完全分布式集群模式（Full-Distributed Mode）
  * Hadoop的守护进程运行在一个集群上。
  * Hadoop的守护进程运行在由多台主机搭建的集群上，是真正的生产环境。
  * 在所有的主机上安装JDK和Hadoop，组成相互连通的网络。
  * 在主机间设置SSH免密码登录，把各从节点生成的公钥添加到主节点的信任列表。
  * 修改3个配置文件：core-site.xml、hdfs-site.xml、mapred-site.xml、yarn-site.xml。

# 3. Hadoop生态圈的组件并做简要描述

原文地址：<https://hub.fastgit.org/wangzhiwubigdata/God-Of-BigData>

* Zookeeper：是一个开源的分布式应用程序协调服务,基于zookeeper可以实现同步服务，配置维护，命名服务，分布式锁等。
* Flume：一个高可用的，高可靠的，分布式的海量日志采集、聚合和传输的系统。
* HBase：是一个分布式的、面向列的开源数据库, 利用Hadoop HDFS作为其存储系统。
* Hive：基于Hadoop的一个数据仓库工具，可以将结构化的数据档映射为一张数据库表，并提供简单的sql 查询功能，可以将sql语句转换为MapReduce任务进行运行。
* Sqoop：将一个关系型数据库中的数据导进到Hadoop的HDFS中，也可以将HDFS的数据导进到关系型数据库中。
* Spark: 一个分布式内存计算框架，该框架实现了流批一体处理，并支持机器学习、图计算。

# 4. Hadoop集群中Hadoop都分别需要启动哪些进程以及它们的作用

原文地址：<https://hub.fastgit.org/wangzhiwubigdata/God-Of-BigData>

* NameNode：它是Hadoop中的主节点，用于HDFS文件系统中元数据的管理。
* SecondaryNameNode：它不是namenode的冗余守护进程，而是提供周期检查点和清理任务。帮助NN合并editslog，减少NN启动时间。
* DataNode：它负责管理连接到节点的存储（一个集群中可以有多个节点）。每个存储数据的节点运行一个datanode守护进程。
* ResourceManager（JobTracker）：JobTracker负责调度DataNode上任务。每个DataNode有一个TaskTracker，它们执行实际工作。
* NodeManager：（TaskTracker）执行任务。
* DFSZKFailoverController：高可用时它负责监控NN的状态，并及时的把状态信息写入ZK。它通过一个独立线程周期性的调用NN上的一个特定接口来获取NN的健康状态。FC也有选择谁作为Active NN的权利，因为最多只有两个节点，目前选择策略还比较简单（先到先得，轮换）。
* JournalNode：高可用情况下存放namenode的editlog文件。
  
# 5. 简述Hadoop的安装过程

原文链接:(<https://www.pianshen.com/article/8402828580/>)

1）使用 root 账户登录  
2）修改 IP  
3）修改 host 主机名  
4）配置 SSH 免密码登录  
5）关闭防火墙  
6）安装 JDK  
7）解压 hadoop 安装包  
8）配置 hadoop 的核心文件 hadoop-env.sh,core-site.xml,mapred-site.xml,hdfs-site.xml
9）配置 hadoop 环境变量.  
10）格式化 hadoop namenode-format  
11）启动节点 start-all.sh  

# 6.Hadoop 中需要哪些配置文件，其作用是什么？

原文链接:(<https://www.pianshen.com/article/8402828580/>)

1） core-site.xml  

fs.defaultFS:hdfs://cluster1(域名)，这里的值指的是默认的HDFS 路径。  
hadoop.tmp.dir:/export/data/hadoop_tmp,这里的路径默认是NameNode、DataNode、  
secondaryNamenode 等存放数据的公共目录。用户也可以自己单独指定这三类节点的目录。  
ha.zookeeper.quorum:hadoop101:2181,hadoop102:2181,hadoop103:2181,这里是
ZooKeeper 集群的地址和端口。注意，数量一定是奇数，且不少于三个节点。

2）hadoop-env.sh  

只需设置jdk 的安装路径，如：export JAVA_HOME=/usr/local/jdk。  

3）hdfs-site.xml  

dfs.replication:他决定着系统里面的文件块的数据备份个数，默认为3 个。  
dfs.data.dir:datanode 节点存储在文件系统的目录。  
dfs.name.dir:是namenode 节点存储hadoop 文件系统信息的本地系统路径。  

4）mapred-site.xml  

mapreduce.framework.name: yarn 指定mr 运行在yarn 上。

# 7. 简单概述一下hadoop1与hadoop2的区别？

Hadoop2与hadoop1最大的区别在于HDFS的架构与mapreduce的很大的区别，而且速度上有很大的提升，hadoop2最主要的两个变化是：namenode可以集群的部署了，hadoop2中的mapreduce中的jobTracker中的资源调度器与生命周期管理拆分成两个独立的组件，并命名为YARN.
