#### 项目介绍

小说精品屋-plus专注于小说，是一个多端（PC、WAP）阅读、功能完善的原创文学CMS系统，由前台门户系统、作家后台管理系统、平台后台管理系统、爬虫管理系统等多个子系统构成，支持会员充值、订阅模式、新闻发布和实时统计报表等功能。

#### 项目结构

```
novel-plus -- 父工程
├── novel-common -- 通用模块
├── novel-front -- 前台门户&作家后台管理子系统（可拆分）
├── novel-crawl -- 爬虫管理子系统
├── novel-admin -- 平台后台管理子系统
└── templates -- 前端模版
```

#### 技术选型

| 技术                 | 说明                                                         
| -------------------- | ---------------------------
| SpringBoot           | Spring应用快速开发脚手架     
| MyBatis              | 持久层ORM框架 
| MyBatis Dynamic SQL  | Mybatis动态sql
| PageHelper           | MyBatis分页插件
| MyBatisGenerator     | 持久层代码生成插件
| Sharding-Jdbc        | 代码层分库分表中间件
| JJWT                 | JWT登录支持  
| SpringSecurity       | 安全框架                           
| Shiro                | 安全框架  
| Ehcache              | Java进程内缓存框架(默认缓存)  
| Redis                | 分布式缓存(缓存替换方案，默认关闭，一行配置开启)                               
| ElasticSearch        | 搜索引擎(搜索增强方案，默认关闭，一行配置开启)                      
| RabbitMq             | 消息队列(流量削峰，默认关闭，一行配置开启)  
| OSS                  | 阿里云对象存储服务(图片存储方式之一，一行配置即可切换) 
| FastDfs              |开源轻量级分布式文件系统(图片存储方式之一，一行配置即可切换)                      
| Redisson             | 实现分布式锁                                       
| Lombok               | 简化对象封装工具                                                                               
| Docker               | 应用容器引擎   
| Mysql                | 数据库服务   
| Thymeleaf            | 模板引擎     
| Layui                | 前端UI                    
                 

##### 演示截图

1. 首页

![img](https://s3.ax1x.com/2020/12/27/r5400A.png)

2. 分类索引页

![img](https://oscimg.oschina.net/oscnet/up-d0b2e03129bfae47b8bb96a491b73d383c5.png)

3. 搜索页

![img](https://s3.ax1x.com/2020/12/27/r5TO8x.png)

![img](https://oscimg.oschina.net/oscnet/up-ed5f689557718924acac76bc3ebca36afcb.png)

4. 排行榜

![img](https://oscimg.oschina.net/oscnet/up-78d5a68586cd92a86c669311f414508f922.png)

5. 详情页

![img](https://oscimg.oschina.net/oscnet/up-8be2495a2869f93626b0c9c1df6f329747a.png)

6. 阅读页

![img](https://oscimg.oschina.net/oscnet/up-517c84148d2db8e11717a8bbecc57fa1be7.png)

7. 用户中心

![img](https://oscimg.oschina.net/oscnet/up-805a30e7a663a3fd5cb39a7ea26bc132a01.png)

8. 充值

![img](https://oscimg.oschina.net/oscnet/up-5a601b0b3af3224d0bebcfe12fc15075d34.png)

![img](https://oscimg.oschina.net/oscnet/up-face25d02c07b05b2ce954cc4bf4ee6a0cc.png)

9. 作家专区

![img](https://oscimg.oschina.net/oscnet/up-30766372cc7f56480ff1d7d55198204f6ea.png)

![img](https://s3.ax1x.com/2020/11/17/DVFiQI.png)

![img](https://s1.ax1x.com/2020/11/09/B7X5oF.png)

![img](https://s1.ax1x.com/2020/11/09/B7XLsx.png)

10. 购买

![img](https://oscimg.oschina.net/oscnet/up-ce0f585efd82a9670335f118cf5897c85e9.png)

![img](https://oscimg.oschina.net/oscnet/up-f849960f4c1303fea77d26e64fc505a7180.png)

##### 后台管理系统截图

![img](https://oscimg.oschina.net/oscnet/up-0552343538674a22a64819834100558f39b.png)

![img](https://s3.ax1x.com/2020/12/01/DWgLNT.png)

![img](https://s3.ax1x.com/2020/12/01/DfmRCd.png)

![img](https://oscimg.oschina.net/oscnet/up-faf5dda7320674c29a1772bc0c81d74762e.png)

##### 数据库安装：

1. 安装MySQL软件。
2. 修改MySQL`max_allowed_packet `配置（建议100M）。
3. 新建数据库，设置编码为utf8mb4。
4. 执行doc/sql/novel_plus.sql脚本文件。

##### 爬虫管理系统安装：

1. 修改novel-common模块下application-common-dev.yml（dev环境，默认环境）或application-common-prod.yml（prod环境，需要在application.yml配置文件中切换）配置文件中的数据库配置。
2. 修改novel-crawl模块下application.yml文件中的管理员账号密码。
3. 启动程序，打开浏览器，默认8081端口访问。
4. 选择已有或新增爬虫源（支持自定义爬虫规则），点击`开启`按钮，开始爬取小说数据。

#### 免责声明

本项目提供的爬虫工具仅用于采集项目初期的测试数据，请勿用于商业盈利。
用户使用本系统从事任何违法违规的事情，一切后果由用户自行承担，作者不承担任何责任。

