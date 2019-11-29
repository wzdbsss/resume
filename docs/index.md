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

1. 熟练JAVA下的OOP编程与J2EE编程，熟悉集合框架，IO流，多线程，反射，熟悉JVM内存模型以及JVM调优
`
2. 熟悉阿里云基础设施，函数计算，容器服务，云数据库RDS，对象存储

3. 熟悉Java常用设计模式，单例模式、代理模式、工厂模式

4. 熟悉JSON/XML数据格式，熟悉正则表达式，编写网络爬虫

5. 熟练使用Spring、SpringMVC、SpringBoot、Hibernate、ibatis等主流开源框架, 并可进行整合开发, 使用Git进行版本控制, 使用Maven, Gradle进行项目多模块构建并对依赖包进行管理和项目的热部署

6. 熟悉关系型数据库MySQL，Postgresql与非关系型数据库Redis，能够编写复杂的SQL增删改查语句

7. 熟悉Vue，Angular等前端框架，HTML5, CSS3, JS, jQuery, Ajax下的前端项目

8. 熟悉docker容器技术，使用kubectl管理Kubernetes集群并部署服务

9. 熟悉Spring Security，Shiro权限框架，进行认证与权限的控制

10. 熟悉Linux常用的操作命令，并可以安装并部署服务

11. 熟悉Nginx实现反向代理、动静分离、负载均衡；

12. 了解ActiveMQ消息队列和订阅模式

## 主要项目

### 西门子MindSphere物联网平台

---

- 开发周期:     
2018/12 至今

- 项目描述:   
MindSphere是西门子基于云的物联网平台，基于SpringCloud开发，部署在阿里云Kubernetes集群上，可以连接工厂机器收集数据进行分析和利用，并允许客户自行创建应用程序使用并分析MindSphere存储在DataLake的数据。    
Predictive Learning Workspace（PrL）是MindSphere Analytics服务下用于训练模型和预测的工作空间，用户可根据自身需要创建不同规格的Hadoop集群，PrL为客户提供了两种版本，基础版提供仅支持Python的Jupyter Notebook，完整版提供Apache Zeppelin Notebook支持各种解析器，面向多种语言和框架。

- 项目职责:    
负责Predictive Learning Workspace（PrL）开发

- 技术要点:    
1. SpringBoot+Postgresql+JPA+Activiti+Squid+Hadoop+Zepppelin+Jupyter+Vault+   
Flyway+消息队列MNS(阿里云)+函数计算(阿里云)+对象存储(阿里云)
2. 使用Flyway管理数据库版本，使用Vault在阿里云函数计算和K8s中管理敏感数据
3. 用户界面集成Jupyter Notebook，使用Spring Cloud Gateway实现用户对Jupyter     
Workspace操作权限管理
4. 使用activiti工作流引擎管理异步任务流程，后台计划任务使用RestTemplate模拟操作 Jupyter REST API，结合函数计算和消息队列MNS实现后台执行计划任务

---

### 贵阳市电子证照库系统

- 开发周期:    
  2018/07-2018/12

- 项目描述:    
贵阳市发改委主导创建的全省统一的电子证照系统和电子证照库，旨在依托政务服务数据共享平台，实现电子证照信息获取、验证，推进跨层级、跨区域、跨部门电子证照互认共享。

- 项目职责:
1. 登录模块
2. 证照目录、证照详情、新增证照录入历史记录、新增证件轮播模块

- 技术要点：
1. 后端：SpringBoot+JPA+Spring Data+Hibernate+ Redis等
2. 前端：nodejs+webpack+vue等
3. 登录模块采用SSO单点登录，将用户登录成功后的令牌token和注册地址集合保存	在Redis中，为token设置过期时间，当用户登录其它子系统时取出cookie中用户	的token值进行判断，若Redis中存在则放行，否则跳转到登录页面
4. 使用注解的模式构建实体类之间的一对多、多对多等关系，自动生成数据表
5. 后台管理使用Shiro进行用户认证和资源权限控制
6. 页面静态化, 使用Nginx实现反向代理、动静分离
7. 使用FastDFS实现大量图片及文件的存储

---

### 郫都区反邪教大数据平台

- 开发周期:    
  2017/07-2017/11

- 项目描述:    
郫都区防邪办主导，通过网格员手动上报邪教人员和使用爬虫搜集邪教信息，分析邪教人员活动并通过人脸识别辨认邪教人员，监控邪教活动开发的数据分析展示平台。

- 项目职责：
1. 邪教人员人脸识别匹配
2. 使用爬虫从社交网站收集数据存储并分析统计

- 技术要点：
1. 后端：SpringBoot+MyBatis+Redis+Lombok+Python+Druid等
2. 后台前端：Beetl+Layui+HTML5+CSS3+jQuery+JS+Ajax+JSON等
3. 使用Redis缓存数据，提升查询主页数据的效率
4. 调用开源python人脸识别库Face recognition 进行人脸识别相似度判断 
5. 使用开源python爬虫框架Scrapy爬取数据存入Mysql数据库并展示分析结果
6. 使用Nginx负载均衡提升并发能力 

---

爱健身，爱运动，爱挑战；热爱代码，拥有良好的编程习惯，喜欢钻研代码研究新技术，对于写出高质量代码非常有成就感。