# quartzDemo
一个简单的quartz分布式任务调度框架实战项目

Quartz 是 Java 领域最著名的开源任务调度工具。

如果只在单体环境中应用，Quartz 未必是最好的选择，例如Spring Scheduled一样也可以实现任务调度，并且与SpringBoot无缝集成，支持注解配置，非常简单，但是它有个缺点就是在集群环境下，会导致任务被重复调度！

而与之对应的 Quartz 提供了极为广用的特性，如任务持久化、集群部署和分布式调度任务等等，正因如此，基于 Quartz 任务调度功能在系统开发中应用极为广泛！

在集群环境下，Quartz 集群中的每个节点是一个独立的 Quartz 应用，没有负责集中管理的节点，而是通过数据库表来感知另一个应用，利用数据库锁的方式来实现集群环境下进行并发控制，每个任务当前运行的有效节点有且只有一个！

特别需要注意的是：分布式部署时需要保证各个节点的系统时间一致！

下面我们一起来看看具体的应用实践！

参考文章：<br/>
      &nbsp;&nbsp;SpringBoot 整合 Quartz 实现分布式调度  https://mp.weixin.qq.com/s/zJSPzcsFl72JNoqZpkH94A <br/>
      &nbsp;&nbsp;分布式定时任务框架Quartz https://juejin.cn/post/6844904029277913095
