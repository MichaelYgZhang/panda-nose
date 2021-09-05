#### panda-nose
> Distributed link attribute tracker, 项目为分布式链路属性追踪器，一想到追踪，自然想到狗利用嗅觉来追踪，而大自然中，熊的鼻子是最灵敏的，
而大熊猫又是一个可爱的熊，所以命名为大熊猫的鼻子。😊

##### 背景
- 微服务背景下，系统的维护是个成本很高的问题，比如页面上展示的A属性需要查询数据源存储来自哪里？DB？ES？通常情况都是人肉代码进行，成本较高，
是不是可以利用trace，byte等技术，来进行分析呢？可以开发个平台辅助进行分析，因此出现本项目。

##### 需求分析
- 低频：一般在需要了解查看属性来源的时候才会用到，属于低频场景。
- 依赖链路Trace：分布式环境下，分析属性之前需要依附于trace，所以trace能力是基础

##### 目标
> 第一期目标：单机链路可以分析出结果，存储主要选择MySQL
> 第二期目标：分布式环境可以分析出结果
- 无侵入：查看属性来源属于辅助能力，要求做到无侵入。
- 可扩展：？
- 高可用：无
- 实时处理：？
- 全量数据：？
- 高吞吐：？
- 故障容忍：？

##### 业界调研

##### 架构

- https://www.processon.com/diagraming/613446871e08530717181186

##### 详细设计
- 收集器：Agent：trace，属性收集
- 分析器：分析trace + 属性之间如何匹配
- 存储模块：ES
- 展示UI

##### 开发计划

##### 复盘总结

##### 其他
- 资料：
- byte-buddy：https://github.com/raphw/byte-buddy
- CAT：https://github.com/dianping/cat
- skywalking：https://github.com/apache/skywalking