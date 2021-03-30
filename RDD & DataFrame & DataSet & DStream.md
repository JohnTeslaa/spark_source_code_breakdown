# 核心概念区别
## 1、RDD & DataFrame & DataSet & DStream区别
1.1 概念RDDs vs DataFrames and Datasets
https://databricks.com/blog/2016/07/14/a-tale-of-three-apache-spark-apis-rdds-dataframes-and-datasets.html
http://gangtieguo.cn/2018/09/06/DataFrame%20DataSet/

RDD是low level的概念，非结构化；
DataFrames是high level的概念，结构化，像一张表一样，包含表头（schema，即字段定义）。与RDD类似，DataFrame也是一个分布式数据容器。然而DataFrame更像传统数据库的二维表格，除了数据以外，还记录数据的结构信息，即schema。同时，与Hive类似，DataFrame也支持嵌套数据类型（struct、array和map）。从API易用性的角度上 看，DataFrame API提供的是一套高层的关系操作，比函数式的RDD API要更加友好，门槛更低。
Datasets是high level的概念，结构化，有类型type。
![image](https://user-images.githubusercontent.com/42859030/112920673-01d91000-913c-11eb-8b2e-6c7a40756d23.png)
![image](https://user-images.githubusercontent.com/42859030/112920695-0d2c3b80-913c-11eb-9a81-1970403b7168.png)


1.2 RDD vs DStream
https://www.cnblogs.com/zhouyf/p/5511636.html


DStream 是Spark Streaming（legacy，Spark2.0进入维护模式）的核心概念。
DStream是一系列连续的RDD。 DStream is just a collection of RDDs, it’s typically used for low-level transformations and processing.
![image](https://user-images.githubusercontent.com/42859030/112920532-baeb1a80-913b-11eb-8a70-dd253238883a.png)

Spark streaming是低阶API，给码农用的，各种坑；Structured streaming是给人设计的API，简单易用。

## 2、Spark Streaming 对比 Structured Streaming
https://blog.csdn.net/don_chiang709/article/details/84660351

Spark Streaming（低版本的流任务编写方式；low level API，不够友好；官方已进入维护阶段） ：是在org.apache.spark.streaming.dstream包下
Structured Streaming（及其内部的两种模式 MicroBatch Streaming VS Continous Streaming）：是在org.apache.spark.sql包下，目的是以SQL形式进行spark开发？


