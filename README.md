# Apache Geode 官方文档中文版

[<img src="https://geode.apache.org/img/apache_geode_logo.png" align="center"/>](http://geode.apache.org)


## 说明
* 翻译自[Apache Geode](https://geode.apache.org/)的[官方文档](http://geode.apache.org/docs/guide/12/about_geode.html)

## 内容来源

* 英文官方网站：     
<http://geode.apache.org/>

* 官方GitHub仓库：   
<https://github.com/apache/geode/>

## 版本历史
* 0.5.0 - 2017.09.03 工程初始化，参考Apache Geode的1.2版本文档

## 目录


## 常见术语

| English | 含义 |
| ------- | ---- |
|JVM|Java虚拟机,Java Virtual Machine|
|JDK|Java Development Kit|
|GC|Garbage Collector/Garbage Collect JVM中的垃圾回收|
|Locator|注册客户端和服务器成员，使双方能够互相发现，同时可以提供一定的负载均衡功能|
|Server Cache，Cache Server| GemFire分布式系统的服务器节点|
|Node，Member|均为GemFire集群的节点|
|Client Cache|接入到GemFire分布式系统的客户端，负责管理本地缓存的生命周期|
|Region|Region是一个分布式系统之上的抽象概念。一个Region允许你在系统的多个VM中存储数据，不用考虑数据存在那个对等体上。Region提供了一个map接口能透明地从合适的VM上获取数据。这个Region类扩展了java.util.Map接口，但是它也支持查询和事务|
|Replicated Region|一个Replicated Region保存着所有分区的数据拷贝|
|Partitioned Region|Partitioned Regions只保存一部分分区的数据拷贝|
|GFSH|GemFire SHell，用于管理和监控GemFire的命令控制台|
|Redundant|副本，在GemFire中，Partitioned Region的副本数量范围为0-3个|
|Primary|主数据|
|Secondary|从数据|

## 参与者（按认领章节排序）

### 翻译

### 校对
