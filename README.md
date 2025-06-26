# 🧑‍💻 社区系统（Server Community）

一个基于 Spring Boot + SSM 架构构建的社区论坛系统，支持发帖、评论、私信、点赞、搜索等核心功能，并融合 Redis、Kafka、ElasticSearch 等组件实现高性能和高可用性。

---

## 📦 项目环境

### 🔧 软件版本配置

| 工具            | 版本           |
| ------------- | ------------ |
| JDK           | 9.0.4        |
| Maven         | 3.6.3        |
| Spring Boot   | 2.4.1        |
| Redis         | 5.0.10       |
| Elasticsearch | 7.9.3        |
| Kafka         | 2.13-2.7.0   |
| wkhtmltopdf   | 长图生成工具       |
| MySQL         | 5.7（建议 ≥5.7） |

### 📂 SQL 文件介绍

| 文件名                       | 描述              |
| ------------------------- | --------------- |
| `init_schema.sql`         | 初始化建表脚本         |
| `init_data.sql`           | 初始化数据脚本         |
| `tables_mysql_innodb.sql` | Quarter 定时任务表结构 |

---

## 🔑 核心功能

* 发帖、评论、私信、转发；
* 点赞、关注、通知、搜索；
* 权限、统计、调度、监控；

---

## 🧰 核心技术栈

* **后端框架**：Spring Boot、SSM
* **缓存与消息中间件**：Redis、Kafka
* **全文搜索**：ElasticSearch
* **权限管理与安全**：Spring Security
* **任务调度**：Quartz
* **缓存优化**：Caffeine

---

## ✨ 项目亮点

* 构建于 Spring Boot + SSM 框架，统一管理状态、事务与异常；
* Redis 实现点赞与关注，单机支持 5000 TPS；
* Kafka 实现异步通知，单机支持 7000 TPS；
* ElasticSearch 支持全文搜索，精准匹配高亮关键词；
* Caffeine + Redis 结合双级缓存，支持 QPS 高达 8000；
* Spring Security 实现权限控制，支持多角色、URL 级权限；
* HyperLogLog 与 Bitmap 实现 UV、DAU 的精确统计；
* Quartz 实现定时任务（如统计帖子数、垃圾清理等）；
* Actuator 实现多维度系统监控（Bean、缓存、日志、数据库连接等）；

---


## 🚀 快速启动

```bash
# 克隆项目
git clone https://github.com/bfyqjzsgkqycf/community.git

# 进入目录
cd community

# 导入 SQL 文件到 MySQL 数据库

# 启动 Redis、Kafka、ElasticSearch 等依赖服务

# 使用 Maven 构建并运行项目
mvn clean install
mvn spring-boot:run
```

---

## 📚 文档 & 学习资料

* [Spring Boot 官方文档](https://spring.io/projects/spring-boot)
* [Spring Security 官方指南](https://spring.io/projects/spring-security)
* [Redis 中文文档](https://www.redis.net.cn/)
* [ElasticSearch 中文指南](https://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html)
* [Kafka 中文文档](http://kafka.apachecn.org/)
* [Quartz 官方文档](https://www.quartz-scheduler.org/documentation/)
* [Actuator 监控文档](https://docs.spring.io/spring-boot/docs/current/actuator-api/htmlsingle/)

---

## 📮 联系方式

如有任何问题或建议，欢迎提 Issue 或 PR！
