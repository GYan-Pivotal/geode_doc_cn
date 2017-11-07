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
|IMDG|In-Memory Data Grid, 内存数据网格|
|GC|Garbage Collector/Garbage Collect, JVM中的垃圾回收, 或JVM中的垃圾回收器|
|Locator|集群中的管理节点, 注册客户端和服务器成员，使双方能够互相发现，同时可以提供一定的负载均衡功能|
|server, server cache，cache server|集群中的数据节点,GemFire分布式系统的服务器节点|
|Node|均为GemFire集群的节点, 一般指的是 CacheServer|
|Member|均为GemFire集群的节点, 指的是 Locator 和 CacheServer|
|Client Cache|接入到GemFire分布式系统的客户端，负责管理本地缓存的生命周期|
|Region, data region|Region是一个分布式系统之上的抽象概念。一个Region允许你在系统的多个VM中存储数据，不用考虑数据存在那个节点上。Region提供了一个map接口能透明地从合适的VM上获取数据。这个Region类扩展了java.util.Map接口，但是它也支持查询和事务|
|Replicated Region|一个Replicated Region保存着所有分区的数据拷贝||Partitioned Region|Partitioned Regions只保存一部分分区的数据拷贝|
|GFSH,gfsh|GemFire SHell，用于管理和监控GemFire的命令控制台|
|Redundant|副本，在GemFire中，Partitioned Region的副本数量范围为0-3个|
|Primary|主数据|
|Secondary|从数据|
|Network Partitions|网络分区，或网络脑裂，指的是一个网络因为网络硬件问题或者其他原因分裂编程两个小的网络|
|Overflow|数据溢出， 指的是把内存持久化到磁盘的操作|
|Eviction|数据逐出，指的是按照LRU算法， 把超出预设数据量，内存堆使用空间之外的数据，持久化到磁盘或者删除的操作|
|Expiration|数据过期或者Region过期，指的是按照预设的TTL（Time-To-Live）时间或者Idle Timeout时间，进行数据删除或者失效的操作|
|Peer-to-Peer|对等式， 指的是各个节点在集群内对等， 没有Locator节点|
|Client-to-Serve， Client/Server|C/S式，指的是通过客户端连接到服务器端集群中， 一般服务器端集群中部署Locator节点|
|Multi-Site (WAN)|也叫WAN-Gateway，指的是多个集群隔离部署， 但是互相之间可以异步同步消息及数据变化。一般用于多活数据中心场景。|
|Write-Behind|指的是通过异步队列的方式，以高速批处理的方式， 在Geode/GemFire和其他数据存储之间进行数据更新信息的同步|
|AsyncEventListener|异步事件监听器， 用于处理异步事件队列|
|Delta Propagation|变化传播|
|OQL， Object-Query-Language|对象查询语言， Geode支持的一种对象关联查询语言， 只支持Select，不支持insert/update/delete|
|Continuous Querying， CQ|持续查询, 指的是可以注册兴趣(register interests)的方式, 对指定的 region 进行持续的关注, 可以不断获得指定 region 数据变化情况的功能|
|Entry， Entries, data entry|每一个Key/Value对，简称为Entry|
|Function|Geode中，类似于Map-reduce方式并行运行的计算功能，允许用户自定义|
|PDX， PortableDataExchange|Geode自定义的高效，且可变结构的序列化方式|
|Geode Pulse|Geode的监控页面， 基于HTML5， 建议使用Chrome或者FireFox浏览|
|cluster configuration service|集群配置服务, 运行在 Locator 之上, 用于管理集群中各节点配置情况的服务|

## 参与者（按认领章节排序）

### 翻译
| 章节 | 负责人 |状态|
| ------- | ---- | ---|
| 整体章节目录 | 闫钢 |完成|
| Apache Geode入门 | 闫钢 |完成|
| 配置和运行集群| 闫钢 |进行中,80%|
| 使用Apache Geode开发/事件和事件处理 | Mr.董 |进行中|
| 使用Apache Geode开发/事务机制 | Mr.董 |进行中|

### 校对

## 附注
### 如何编译
 1. 运行geode-book/build_deploy.sh, 会把geode-docs下面最新的内容进行编译, 并通过 http 进行发布.
 2. 之后可以通过[http://localhost:9292/](http://localhost:9292/) 查看修改结果. 
 3. 建议在提交之前, 先编译, 检查一下自己将要提交的内容.