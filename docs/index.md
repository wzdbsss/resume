# 个人简历

## 基本信息

 - **马奇**/男/25
 - 工作年限: 4年
 - 邮箱: wzdbsss@hotmail.com
 - 期望职位: Java工程师

## 教育背景

- 西南交通大学/信息与计算科学    2012/09至2016/06
- 英语四级

## 工作经历

- 2018/12至今&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;西门子(中国)有限公司&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Java工程师
- 2016/09至2018/12&ensp;&ensp;&ensp;&ensp;四川成都优易数据有限公司&ensp;&ensp;&ensp;&ensp;Java工程师
## 技术栈

1. 熟练JAVA下的OOP编程与J2EE编程, 熟悉集合框架, IO流, 多线程, 反射, 熟悉JVM内存模型以及JVM调优

2. 熟悉阿里云基础设施, 函数计算, 容器服务, 云数据库RDS, 对象存储

3. 熟悉Java常用设计模式, 单例模式, 代理模式, 工厂模式

4. 熟悉JSON/XML数据格式, 熟悉正则表达式, 编写网络爬虫

5. 熟练使用 Spring, SpringMVC, SpringBoot, Hibernate, ibatis, Spring Security, Shiro 等主流开源框架, 并可进行整合开发, 使用 Git 进行版本控制, 使用 Maven, Gradle 进行项目多模块构建并对依赖包进行管理和项目的热部署, 熟悉 ActiveMQ 等消息中间件

6. 熟悉关系型数据库 MySQL, Postgresql 与非关系型数据库 Redis, 能够编写复杂的 SQL 增删改查语句

7. 熟悉 Vue, Angular等前端框架, HTML5, CSS3, JS, jQuery, Ajax下的前端项目

8. 熟悉 Docker 容器技术, 使用kubectl管理Kubernetes集群并部署服务

9.  熟悉 Linux 操作系统, 对常用命令非常熟悉, 能够根据实际情况编写 Shell 脚本并部署服务, 熟悉 Nginx 实现反向代理, 动静分离, 负载均衡

## 主要项目

---

### Spectrum Analysis(频谱分析)

- 开发周期:  
2019/11 至 2020/04

- 项目描述:
    * 频谱分析是 MindSphere 物联网平台下的一个微服务。频谱分析允许用户对收集的机器运行时的音频文件执行时域和频域分析。它通过离散傅立叶变换(Discrete Fourier Transform)提供了将时域信号转换为频率分量，并检测其幅度的阈值突破的功能。
    * 离散傅立叶变换使用快速傅立叶变换将给定的音频数据从时域转换到频域。每个频率都由具有自己的振幅和相位的正弦振荡表示，转换后用户可以对音频信号做阈值异常检测。

- 项目职责:  
    * 参与 Spectrum Analysis 架构设计与开发, 承担核心功能代码编写
    * 负责系统性能优化, 将核心功能代码封装成函数计算，提升服务并发能力

- 技术要点:  

    1. SpringBoot + 函数计算(阿里云) + Skywalking(应用性能管理) + Vault + Mockito
    2. 在 VPC 中搭建 Vault 服务器保存敏感数据
    3. 使用 Gitlab CI/CD 结合资源编排工具 Terraform 对 Kubernetes 集群上的微服务持续集成和部署, 提高开发效率
    4. 使用 Skywalking 分布式追踪系统将业务调用数据存储到 Elasticsearch 进行监控和依赖分析
    5. 将处理音频的傅里叶变换函数与 Spring boot 服务分离并部署到阿里云函数计算，利用函数计算的弹性可伸缩计算性能，大幅提高业务的并发性能

---

### Predictive Learning Workspace(预测学习工作区)

- 开发周期:  
2018/12 至 2019/10

- 项目描述:
    * MindSphere 物联网平台是西门子基于云的大型分布式 Web 应用系统, 基于 Spring Cloud, 部署在阿里云 Kubernetes 集群上, 可以连接工厂机器收集数据进行分析和利用, 并允许客户自行创建应用程序使用并分析 MindSphere 存储在 DataLake 的数据。
    * Predictive Learning Workspace（PrL）是MindSphere Analytics服务下用于训练模型和预测的工作空间模块, 用户可根据自身需要创建不同规格的Hadoop集群, PrL为客户提供了两种版本, 基础版提供仅支持Python的Jupyter Notebook, 完整版提供Apache Zeppelin Notebook支持各种解析器, 面向多种语言和框架。
    * 用户可以在 MindSphere Predictive Learning Workspace（PrL）中打开 Jupyter Notebook 来训练基于 Python 的机器学习模型, 并使用 Job Manager Service 来执行或者重新训练模型。

- 项目职责:  
    * 参与 Predictive Learning Workspace（PrL）架构设计与开发, 承担核心功能代码编写
    * 负责系统性能优化, 提升 Workspace 启动速度优化用户体验

- 技术要点:  

    1. SpringBoot + Postgresql + JPA + Activiti + Squid + Hadoop + Zepppelin + Jupyter + Vault + Nginx + Flyway + 消息队列MNS(阿里云) + 函数计算(阿里云) + 对象存储(阿里云)
    2. 使用 Spring Boot Flyway 管理数据库版本, 在VPC中搭建Vault服务器保存敏感数据
    3. 使用 Gitlab CI/CD 结合 Terraform 对 Kubernetes 集群上的微服务持续集成和部署, 提高开发效率
    4. 结合阿里云函数计算定时触发器(cron)和消息队列实现计划执行训练模型
    5. 使用非对称加密生成 JWT Token 结合 Nginx 对搭建在阿里云上的 Hadoop 集群服务进行访问权限控制
    6. 使用 activiti 工作流引擎, 异步任务流程, 后台计划任务使用RestTemplate模拟操作 Jupyter REST API, 结合函数计算和消息队列MNS实现后台执行计划任务

---

### 贵阳市电子证照库系统

- 开发周期:    
  2018/07-2018/12

- 项目描述:    
贵阳市发改委主导创建的全省统一的电子证照系统和电子证照库, 旨在依托政务服务数据共享平台, 实现电子证照信息获取, 验证, 推进跨层级, 跨区域, 跨部门电子证照互认共享。

- 项目职责:
    * 负责登录模块核心代码编写
    * 证照目录, 证照详情, 新增证照录入历史记录, 新增证件轮播模块

- 技术要点：

    1. 后端：SpringBoot + JPA + Spring Data+Hibernate + Redis等
    2. 前端：Nodejs + Webpack + Vue等
    3. 登录模块采用SSO单点登录, 将用户登录成功后的令牌token和注册地址集合保存在 Redis 中并为token设置过期时间, 当用户登录其它子系统时取出cookie中用户的token值进行判断, 若Redis中存在则放行, 否则跳转到登录页面
    4. 使用注解的模式构建实体类之间的一对多, 多对多等关系, 自动生成数据表
    5. 后台管理使用 Shiro 进行用户认证和资源权限控制
    6. 页面静态化, 使用 Nginx 实现反向代理, 动静分离
    7. 使用FastDFS实现大量图片及文件的存储

---

### 郫都区反邪教大数据平台

- 开发周期:  
  2017/07-2017/11

- 项目描述:  
郫都区防邪办主导, 通过网格员手动上报邪教人员和使用爬虫搜集邪教信息, 分析邪教人员活动并通过人脸识别辨认邪教人员, 监控邪教活动开发的数据分析展示平台。

- 项目职责:  
    * 嫌疑人员人脸识别匹配
    * 使用爬虫从社交网站收集数据存储并分析统计

- 技术要点：

    1. 后端：SpringBoot + MyBatis + Redis + Lombok + Python + Druid等
    2. 后台前端：Beetl + Layui + HTML5 + CSS3 + jQuery + JS + Ajax + JSON等
    3. 使用Redis缓存数据, 提升查询主页数据的效率
    4. 调用开源 python人脸识别库 Face recognition 进行人脸识别相似度判断
    5. 使用开源 python 爬虫框架 Scrapy 爬取数据存入 Mysql 数据库并展示分析结果
    6. 使用 Nginx 负载均衡提升并发能力  
   
---

爱健身, 爱运动, 爱挑战; 热爱代码, 拥有良好的编程习惯, 喜欢钻研代码研究新技术, 对于写出高质量代码非常有成就感。