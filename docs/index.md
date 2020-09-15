# 个人简历

## 基本信息

|                   |                      |
| :---------------- | :------------------- |
| 姓名: **马奇**     | 年龄: 27             |
| 性别: 男           | 期望职位: Java工程师 |
| 电话: 18684013197 | 工作年限: 5年        |

## 教育背景

- 西南交通大学/信息与计算科学    2012/09至2016/06
- 英语四级

## 工作经历

- 2018/12至今&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;西门子(中国)有限公司&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;&ensp;Java工程师
- 2016/09至2018/12&ensp;&ensp;&ensp;&ensp;四川成都优易数据有限公司&ensp;&ensp;&ensp;&ensp;Java工程师
## 技术栈

1. 熟练 Java 下的 OOP 编程与 J2EE 编程, 熟悉 Java 常用设计模式, 熟悉集合框架, IO流, 多线程, 反射, 熟悉JVM内存模型以及JVM调优

2. 熟练使用 Spring, Spring MVC, MyBatis, Hibernate 等框架, 熟悉 Spring Cloud 下的 Java Web 项目开发, 熟悉使用 Maven, Gradle 进行项目多模块构建并对依赖包进行管理和项目的热部署

3. 熟悉 Netty 异步网络编程框架，使用 Netty 实现高并发网络通信应用

4. 熟悉阿里云基础设施, 函数计算, 容器服务, 云数据库, 对象存储, 消息中间件

5. 熟悉 Vue, Angular 等前端框架, HTML5, CSS3, JS, jQuery, Ajax下的前端项目, 熟悉正则表达式以及编写网络爬虫

6. 熟悉关系型数据库 MySQL, Postgresql 与非关系型数据库 Redis, 熟悉存储过程

7. 熟悉 Linux 操作系统以及 Shell 编程, 熟悉 Nginx 和 Squid 实现反向代理, 动静分离, 负载均衡

8. 熟悉主流 PaaS 平台包括 Cloud Foundry 以及 Kubernetes, 熟悉 Docker 容器技术并使用 kubectl 管理 Kubernetes 集群并部署服务

## 主要项目

---

### Event Management(事件管理)

- 开发周期: 2019/11 至 2020/04

- 项目描述:
    * 事件管理是西门子 MindSphere 物联网平台下的一个微服务。它允许用户在运行时创建自定义的事件类型(数据库表结构)来存储用户指定的数据, 并且能够通过事件管理服务的接口进行自定义事件的筛选, 更新或删除。
    * 用户可以使用预定义的事件类型或创建自己的模板来生成新事件, 事件管理服务将用户自定义事件类型转换为实体类并创建相对应的数据库表结构。

- 项目职责:  
    * 参与 Event Management 动态创建用户事件模块代码编写
    * 编写单元测试达到指定覆盖率
    * 负责 Event Management 微服务部署到 Kubernetes 以及相关文档编写
    * 利用看板，燃尽图，每日站会，scrum会议，控制项目进度，软件开发质量及汇报项目状态

- 技术要点:  

    1. Spring Boot + Spring Data Jpa + Javassist + Flywaydb + Mockito + Lombok
    2. 使用 Javassist 字节码操纵类库, 在运行时动态创建用户定义字段的实体类 class 字节码文件
    3. 将创建的字节码文件添加到 classpath 并用 System ClassLoader 将生成的 class 字节码加载到 JVM 中
    4. 利用 JPA 提供的 EntityManagerFactory 生成对应实体类的表结构, 完成动态建表过程
    5. 使用 Lombok 插件减少项目中模板代码
    6. 利用 Jacoco/SonarQube 实现项目代码覆盖率统计

---

### Spectrum Analysis(频谱分析)

- 开发周期: 2019/08 至 2019/10

- 项目描述:
    * 频谱分析是西门子 MindSphere 物联网平台下的分析微服务。频谱分析允许用户对收集的机器运行时的音频文件执行时域和频域分析。它通过离散傅立叶变换(Discrete Fourier Transform)提供了将时域信号转换为频率分量，并检测其幅度的阈值突破的功能。
    * 离散傅立叶变换使用快速傅立叶变换将给定的音频数据从时域转换到频域。每个频率都由具有自己的振幅和相位的正弦振荡表示，转换后用户可以对音频信号做阈值异常检测。

- 项目职责:  
    * 重构 Spectrum Analysis 使应用程序为基于 Feign Client 的微服务框架
    * 负责系统性能优化, 提升服务并发能力

- 技术要点:  

    1. Spring Boot + 函数计算(阿里云) + SLF4J + Logback + Mockito
    2. 使用 ControllerAdvice 实现服务全局异常处理
    3. 使用 MDC 实现多线程日志跟踪
    4. 利用 Docker, Gitlab Runner Pipeline 自动执行测试用例以实现持续集成
    5. 使用 Black duck/Code center 对软件程序中使用的开源软件的安全漏洞以及商业分发许可协议扫描
    6. 利用函数计算的弹性可伸缩计算性能，将执行傅立叶变换的代码抽取出来，分离到函数计算服务，提高业务的并发性能
    8. 使用 Feign 实现服务间 API 相互调用以及失败重试

---

### Predictive Learning Workspace(预测学习工作区)

- 开发周期: 2018/12 至 2019/06

- 项目描述:
    * MindSphere 物联网平台是西门子基于云的大型分布式 Web 应用系统, 基于 Spring Cloud, 部署在阿里云 Kubernetes 集群上, 可以连接工厂机器收集数据进行分析和利用, 并允许客户自行创建应用程序使用并分析 MindSphere 存储在 DataLake 的数据
    * Predictive Learning Workspace（PrL）是 MindSphere Analytics 服务下用于训练模型和预测的工作空间模块
    * 用户可根据自身需要创建不同规格的计算实例, 使用 Jupyter Notebook 对工厂数据进行基于 python 语言的机器学习和人工智能相关模型训练以及预测。
    

- 项目职责:  
    * 参与 Predictive Learning Workspace（PrL）开发, 承担核心功能代码编写以及代码评审
    * 负责系统性能优化, 提升 Workspace 启动速度优化用户体验
    * 敏捷 Scrum/Kanban 及 Jira Dashboard, Confluence 等工具实施开发流程、测试用例和 bug 管理
    * Release notes/Run book 文档编写

- 技术要点:  

    1. SpringBoot + Zuul + Mysql + JPA + Jupyter + Flyway + Maven + 消息队列MNS(阿里云)
    2. 使用 Spring Boot Flyway 实现数据库版本迭代
    3. 基于 Zuul 实现自定义网关和用户鉴权, 对用户 API 请求进行反向代理并自动添加 OAuth 请求头 
    4. 使用消息队列和定时服务实现自动销毁工作空间, 避免集群环境 Spring Scheduler 定时任务多次执行
    5. 利用数据库实现了简单的分布式锁，防止用户在集群环境下的多次请求导致数据不一致
    6. 基于 Java SPI(Service Provider Interface) 实现不同云平台的 IAM 组件解耦
    7. 使用 Gitlab CI/CD 结合 Terraform 对 Kubernetes 集群上的微服务持续集成和部署
    8. 基于 activiti 框架实现工作流异步处理模型训练/模型执行任务

---

### 贵阳市电子证照库系统

- 开发周期: 2018/07 至 2018/12

- 项目描述:    
贵阳市发改委主导创建的全省统一的电子证照系统和电子证照库, 旨在依托政务服务数据共享平台, 实现电子证照信息获取, 验证, 推进跨层级, 跨区域, 跨部门电子证照互认共享。

- 项目职责:
    * 负责登录模块核心代码编写
    * 证照目录, 证照详情, 新增证照录入历史记录, 新增证件轮播模块

- 技术要点：

    1. 后端：SpringBoot + Spring Data JPA + Redis 等
    2. 前端：Nodejs + Webpack + Vue等
    3. 登录模块采用SSO单点登录, 将用户登录成功后的令牌token和注册地址集合保存在 Redis 中并为token设置过期时间, 当用户登录其它子系统时取出cookie中用户的token值进行判断, 若Redis中存在则放行, 否则跳转到登录页面
    4. 使用注解的模式构建实体类之间的一对多, 多对多等关系, 自动生成数据表
    5. 后台管理使用 Shiro 进行用户认证和资源权限控制
    6. 页面静态化, 使用 Nginx 实现反向代理, 动静分离
    7. 使用FastDFS实现大量图片及文件的存储

---

### 郫都区反邪教大数据平台

- 开发周期: 2017/07 至 2017/11

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
