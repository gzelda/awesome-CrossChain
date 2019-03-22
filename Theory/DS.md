# Distributed System

### 研究目标
- 从分布式系统理论出发关注分布式一致性问题，从而扩展至区块链的共识问题。




### 分布式系统CAP特性

<img src="/Resource/CAP.png">

CAP理论核心思想是基于任何网络的数据共享系统最多只能满足数据一致性(Consistency)、可用性(Availability)和分区容错(Partition Tolerance)三个特性中的两个。

- Consistency 一致性  
  分布式系统中的所有数据备份，在同一时刻是同样的值
- Availability 可用性  
  分布式系统中部分节点故障后，系统整体能够响应客户端的请求
- Partition Tolerance 分区容错性  
  数据不一致的分布式集群为不同区，分区容错性代表分布式系统需要在有限时间内选择解决一致性或可用性的问题（二选一）