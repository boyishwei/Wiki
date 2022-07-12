Introduction:
https://tech.163.com/photoview/0AI20009/16086.html#p=D0IH7KI00AI20009NOS&from=tj_review

Register:
1. Credit Card
2. It will Charge you 1 US dollor
3. Use the eligiable service
4. It's only free up to 12 month

Service catalog:
https://www.cnblogs.com/huang0925/p/3837987.html

## Compute
### EC2: 
Elastic Cloud Computing
### Lightsail: 
deploy your container-based workloads or applications
### Lambda: 
Serverless cloud computing
serverless这种架构，让程序员不用关心服务器的运维当请求量增加的时候，比如从1增加到百万，甚至更多，程序员不用做任何事情。服务照样可以处理，只是付费的账单金额增加（当然了，百万的访问量，老板很开心）坏处：这种开发模式，很多程序员不适应调试起来，比较困难，尤其在国内网络通讯很耗时。推荐使用Docker搭个本地环境测试Docker本地环境推荐：lambci/docker-lambda，基本思想：编译（go/java等需要编译），如果是go，指定编译成linux平台的执行代码编译既可以用自己熟悉的编译工具，docker-lambda也提供了编译镜像，进行编译操作运行Docker
### Batch: scheduled batch jobs, support EC2 instance and spot instance
### Elastic Beantalk: 
Elastic Beanstalk 是在 AWS 上部署和运行 Web 应用程序最简单的方式。Elastic Beanstalk 会自动处理容量预置、负载均衡、自动扩展和 Web 应用程序运行状况监控方面的部署详细信息。
使用 Elastic Beanstalk 无需额外付费。您只需支付我们为存储和运行您的 Web 应用程序而创建的 AWS 资源(Amazon S3 存储桶和 Amazon EC2 实例)的费用。
您可以随意选择最适合您的 Web 应用序的 AWS 资源，例如 Amazon EC2 实例类型。此外，借助 Elastic Beanstalk，您还可以管理并完全掌控为 Web 应用程序提供支持的 AWS 资源。
### Outpost:
Outpost 是部署在客户场地的 AWS 计算和存储容量池。此容量作为 AWS 区域的一部分进行运营、监控和管理。您可以在 Outpost 上创建子网，并使用这些子网在本地启动和运行 AWS 资源，如 EC2 实例、EBS 卷、ECS 集群和 RDS 数据库。

## Storage
### S3
Simple Storage Service
简单存储服务，是亚马逊对外提供的对象存储服务。不限容量，单个对象大小可达5TB，支持静态网站。其高达99.999999999%的可用性让其它竞争对手胆寒。
### EBS： 
Elastic Block Storage，块级存储服务，支持普通硬盘和SSD硬盘，加载方便快速，备份非常简单。
### Glacier：
主要用于较少使用的存储存档文件和备份文件，价格便宜量又足，安全性高。
### EFS:
Amazon Elastic File System , 提供的是简单、可扩展、完全托管的弹性 NFS 文件系统，可与 AWS 云服务和本地资源结合使用。
### FSx
Amazon FSx for Windows File Server Resources: File Systems, Backups, and File Shares
### Store Gateway
AWS Storage Gateway 是一项混合云存储服务，可让您从本地访问几乎不受限制的云存储。客户使用 Storage Gateway 简化存储管理，降低关键混合云存储用例的成本。其中包括将备份和存档移动到云、使用云存储支持的本地文件共享，以及为本地应用程序提供对 AWS 中数据的低延迟访问。
### Backup
AWS Backup provides a fully managed backup service and a policy-based backup solution that simplifies your backup management and enables you to meet your business and regulatory backup compliance requirements.

## Database
### RDS， Relational Database Service，关系型数据库服务。支持MySql，SQL Server和Oracle等数据库，具有自动备份功能，IO吞吐量可按需调整。
### DynamoDB： DynamoDB是亚马逊自主研发的no sql型数据库，性能高，容错性强，支持分布式，并且与Cloud Watch、EMR等其它云服务高度集成。
### Amazon ElastiCache： 数据库缓存服务。
### Document DB: MongoDB
### Neptune: Image DB
### Timestream: IoT DB
### RedShift: Dataware house

## Network
### Direct Connect： 支持企业自身的数据中心直接与AWS的数据中心直连，充分利用企业现有的资源。
### VPN Connection：通过VPN连接AWS，保证数据的安全性。
### Virtual Private Cloud： 私有云，从AWS云资源中分一块给你使用，进一步提高安全性。
### Route 53：亚马逊提供的高可用的可伸缩的域名解析系统。

## Application Service
### Cloud Search: 一个弹性的搜索引擎，可用于企业级搜索。
### Amazon SQS： 队列服务，存储和分发消息。
### Simple Workflow：一个工作流框架。
### CloudFront：世界范围的内容分发网络。
### EMR： Elastic MapReduce，一个hadoop框架的实例，可用于大数据处理。


## EC2
* EC2 is a service that allows you to run virtual servers in the cloud
### Supported OS
* Windows 2003-2016
* Amazon Linux
* Debian
* SUSE
* CentOS
* RedHat
* Ubantu

### EC2 Benifits
* Time to market
* Scalability
* Reliability
* Security
* Control
* Service Integration
* Cost Efficiency
