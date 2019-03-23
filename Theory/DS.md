# Distributed System
<!-- TOC -->

- [Distributed System](#distributed-system)
    - [研究目标](#研究目标)
    - [分布式系统CAP特性](#分布式系统cap特性)
    - [Paxos](#paxos)
    - [Raft](#raft)
    - [参考文章](#参考文章)

<!-- /TOC -->

## 研究目标
从分布式系统理论出发关注分布式一致性问题，从而扩展至区块链的共识问题。

## 分布式系统CAP特性

![avatar](/Theory/Resource/CAP.png)

CAP理论核心思想是基于任何网络的数据共享系统最多只能满足数据一致性(Consistency)、可用性(Availability)和分区容错(Partition Tolerance)三个特性中的两个。

- Consistency 一致性  
  分布式系统中的所有数据备份，在同一时刻是同样的值
- Availability 可用性  
  分布式系统中部分节点故障后，系统整体能够响应客户端的请求
- Partition Tolerance 分区容错性  
  数据不一致的分布式集群为不同区，分区容错性代表分布式系统需要在有限时间内选择解决一致性或可用性的问题（二选一）

本文作者看到这里的时候很容易联想到区块链系统中的不可能三角问题，那么对于分布式系统中三角问题中的边缘情况如下所示：

- CA without P  
  “分布式系统具备强一致性与强可用性，不要求分区容错性”，这个命题本身是不成立的，因为分区容错是始终会存在的问题，CA系统基本上是以单机系统为核心的数据单元。  
  **应用场景**：PC数据库、数据库集群

- CP without A   
  不要求可用性，强调服务端之间的数据为强一致性。CP是可以保证的，但分区容错的选择会导致同步时间长  
  **应用场景**：分布式数据库、分布式事务锁

- AP without C  
  不要求数据一致性，强调分布式系统的使用效率，忽略数据不一致性。为了高可用性，节点之间的数据可能会失去同步机制，很多使用本地数据提供服务的分布式系统属于此类。  
  **应用场景**：网页缓存、DNS

## Paxos 
[Paxos图示](https://www.jdon.com/artichect/paxos.html)


## Raft
[Raft图示](https://www.jdon.com/artichect/raft.html)  
[Raft讲解](https://www.cnblogs.com/hzmark/p/raft.html)  

## 参考文章

> https://www.cnblogs.com/heapStark/p/8351852.html  
> https://www.cnblogs.com/binyue/p/8645565.html  
> https://www.jianshu.com/p/0b245d972e23  
> https://www.cnblogs.com/endsock/p/3480093.html  
> https://lamport.azurewebsites.net/pubs/paxos-simple.pdf  