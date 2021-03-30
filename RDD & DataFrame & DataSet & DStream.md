# 核心概念区别
## 1、RDD & DataFrame & DataSet & DStream区别
1.1 概念RDDs vs DataFrames and Datasets
https://databricks.com/blog/2016/07/14/a-tale-of-three-apache-spark-apis-rdds-dataframes-and-datasets.html
RDD是low level的概念，非结构化
DataFrames是high level的概念，结构化，像一张表一样，包含表头（schema，即字段定义）。
Datasets是high level的概念，结构化，有类型type。

1.2 RDD vs DStream
https://www.cnblogs.com/zhouyf/p/5511636.html
DStream 是Spark Streaming（legacy，Spark2.0进入维护模式）的核心概念。
DStream是一系列连续的RDD。 DStream is just a collection of RDDs, it’s typically used for low-level transformations and processing.
Spark streaming是低阶API，给码农用的，各种坑；Structured streaming是给人设计的API，简单易用。

## 2、Spark Streaming 对比 Structured Streaming
https://blog.csdn.net/don_chiang709/article/details/84660351

Spark Streaming（低版本的流任务编写方式；low level API，不够友好；官方已进入维护阶段） ：是在org.apache.spark.streaming.dstream包下
Structured Streaming（及其内部的两种模式 MicroBatch Streaming VS Continous Streaming）：是在org.apache.spark.sql包下，目的是以SQL形式进行spark开发？


