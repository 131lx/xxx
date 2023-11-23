# 开源项目适配华为云服务


学习过程
--------------

### 准备工作
* 首先要了解云服务的信息，可以在华为云官网搜索对应的`帮助文档`；
* 在帮助文档中建议了解`产品介绍`、`快速入门`，有助于后续开发与测试；
* 在帮助文档中进一步了解`API概览`，这里介绍了关于云服务的接口与说明，根据功能调用接口；
* 在华为云`SDK中心`搜索相关云服务的SDK，引入依赖时可到对应的SDK中心下查询依赖信息；
* 华为云服务SDK对应语言的Github仓库地址可到下列对应的`SDK概述`中查找。

### 参考文档
| 华为云服务                             | API概览                                                                                    | SDK中心                                                                               | SDK概述                                                                                             |
|-----------------------------------|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ECS                               | [ECS API概览](https://support.huaweicloud.com/api-ecs/ecs_01_0008.html)                    | [ECS SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=ecs)               | [ECS SDK概述](https://support.huaweicloud.com/sdkreference-ecs/ecs_sdk_0101.html)                    |
| OBS                               | [OBS API概览](https://support.huaweicloud.com/api-obs/obs_04_0005.html)                    | [OBS SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=OBS)               | [OBS SDK概述](https://support.huaweicloud.com/sdkreference-obs/obs_02_0001.html)                    |
| SMN                               | [SMN API概览](https://support.huaweicloud.com/api-smn/smn_api_20000.html)                  | [SMN SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=smn)               | [SMN SDK概述](https://support.huaweicloud.com/sdkreference-smn/smn_sdk_0101.html)                   |
| FunctionGraph                     | [FG API概述](https://support.huaweicloud.com/api-functiongraph/functiongraph_06_1500.html) | [FG SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=Functiongraph)      | [FG SDK概述](https://support.huaweicloud.com/sdkreference-functiongraph/functiongraph_07_0100.html) |
| DLI                               | [DLI API概览](https://support.huaweicloud.com/api-dli/dli_02_0181.html)                    | [DLI SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=DLI)               | [SDK与API对应关系](https://support.huaweicloud.com/sdkreference-dli/dli_04_0123.html)                  |
| GuassDB-NoSQL                     | [NoSQL API概览](https://support.huaweicloud.com/api-nosql/nosql_05_0006.html)              | [NoSQL SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=gaussdbfornosql) | [NoSQL SDK概述](https://support.huaweicloud.com/sdkreference-nosql/nosql_sdk_0001.html)             |
| DMS<br/>(Kafka、RabbitMQ、RocketMQ) |                                                                                          | [DMS SDK中心](https://sdkcenter.developer.huaweicloud.com/?product=dms)               |                                                                                                   |
| DEW                               | [DEW API概览](https://support.huaweicloud.com/api-dew/dew_02_0057.html)                    |                                                                                     | [DEW SDK概述](https://support.huaweicloud.com/sdkreference-dew/dew_02_0001.html)                    |


云服务介绍与其他资料
--------------
### ECS
弹性云服务器（Elastic Cloud Server，ECS）是由CPU、内存、操作系统、云硬盘组成的基础的计算组件。弹性云服务器创建成功后，您就可以像使用自己的本地PC或物理服务器一样，在云上使用弹性云服务器。
</br>了解[弹性云服务器](https://blog.csdn.net/Perfectfeeling/article/details/124661758)。
</br>更多ECS详细内容可参考[ECS帮助文档](https://support.huaweicloud.com/ecs/index.html)。
> **竞品：** AWS中的EC2、阿里云的ECS、微软的Azure Compute等。

### OBS
OBS是一种对象存储服务，能够为企业和个人用户提供强大的数据存储和管理功能，OBS的使用场景包含且不局限于大数据分析、静态网站托管、在线视频点播等，同时OBS是统一管理数据湖&数据仓库的存储底座，也可以作为异构数据源进行数据同步，并且与DWS（数据仓库服务）具有双向互通的能力。
</br>[什么是对象存储？](https://www.ibm.com/cn-zh/topics/object-storage)
</br>更多OBS详细内容可参考[OBS帮助文档](https://support.huaweicloud.com/obs/index.html)。
> **竞品：** AWS中的S3、阿里云的OSS、微软的Azure Blob等。

### SMN
消息通知服务，可以依据用户的需求主动推送通知消息，最终用户能够通过短信、电子邮件等方式接收，提供一对多的消息订阅以及通知功能。
</br>了解[消息模型](https://blog.csdn.net/summer_fish/article/details/120262493)。
</br>更多SMN详细内容可参考[SMN帮助文档](https://support.huaweicloud.com/smn/index.html)。
> **竞品：** AWS的SNS、阿里云的MNS等。

### FunctionGraph
FunctionGraph是一项基于事件驱动的函数托管计算服务，只需编写业务函数代码并设置运行条件，无需配置和管理服务等基础设施。
</br>[事件驱动型架构是什么？](https://cloud.google.com/eventarc/docs/event-driven-architectures?hl=zh-cn)
</br>借助FunctionGraph可以轻松实现[从0开发一个签到小程序](https://blog.csdn.net/devcloud/article/details/119454453)。
</br>更多FunctionGraph详细内容可参考[FG帮助文档](https://support.huaweicloud.com/functiongraph/index.html)。
> **竞品：** AWS的AWS Lambda、阿里云的Serverless工作流、微软的Azure Functions等。

### DLI
数据湖探索支持标准SQL\Spark SQL\Flink SQL，兼容主流数据格式。数据无需复杂的ETL，使用SQL就可以对云上的RDS、DWS（数据仓库服务）、OBS、ECS自建数据库以及线下数据库的异构数据进行探索。
</br>[什么是数据湖？](https://toutiao.io/posts/8ogrucc/preview)
</br>更多DLI详细内容可参考[DLI帮助文档](https://support.huaweicloud.com/dli/index.html)。
> **竞品：** AWS的Amazon Athena、阿里云的DLF、微软的Azure Data Lake Analytics、Azure Stream Analytics等。

### GuassDB-NoSQL
目前兼容Cassandra、MongoDB、InfluxDB、Redis这四种主流的NoSQL接口。
</br>[Cassandra](https://baike.baidu.com/item/cassandra/20140772)
</br>[MongoDB](https://www.runoob.com/mongodb/mongodb-intro.html)
</br>[InfluxDB](https://www.modb.pro/db/608173)
</br>[Redis](https://www.runoob.com/redis/redis-intro.html)
</br>更多GuassDB-NoSQL详细内容可参考[NoSQL帮助文档](https://support.huaweicloud.com/nosql/index.html)。
> **竞品：** AWS的DynamoDB、微软的CosmosDB、阿里云的云数据库Cassandra版（2023.10.17计划退市）、阿里云的云数据库MongoDB版、阿里云的云数据库Redis版等。

### DMS
分布式消息服务包括三个版本：Kafka、RabbitMQ、RocketMQ。
* Kafka：适用于构建实时数据管道、流式数据处理、第三方解耦、流量削峰去谷等场景；
* RabbitMQ：广泛应用于秒杀、控流、系统解耦等场景；
* RocketMQ：可更好地适配电商、金融等多样的业务场景。

更多DMS详细内容可参考[Kafka帮助文档](https://support.huaweicloud.com/kafka/index.html)、[RabbitMQ帮助文档](https://support.huaweicloud.com/rabbitmq/index.html)、[RocketMQ帮助文档](https://support.huaweicloud.com/hrm/index.html)。
> **竞品：** 阿里云的消息队列Kafka版、消息队列RabbitMQ版、消息队列RocketMQ版等。

### DEW
数据加密服务是一个综合的数据加密服务，提供密钥管理、凭据管理、密钥对管理、专属加密四个微服务。
</br>[常见的七种加密算法及实现](https://juejin.cn/post/6844903638117122056)。
</br>更多DEW详细内容可参考[DEW帮助文档](https://support.huaweicloud.com/dew/index.html)。
> **竞品：** AWS的AWS Key Management Service、AWS Secrets Manager、微软的Key Vault、阿里云的密钥管理服务等。

