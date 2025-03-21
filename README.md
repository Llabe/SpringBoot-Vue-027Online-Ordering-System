# 网上点餐系统 / Online Ordering System

![SpringBoot](https://img.shields.io/badge/SpringBoot-2.x-brightgreen)
![MyBatisPlus](https://img.shields.io/badge/MyBatisPlus-2.3-blue)
![Shiro](https://img.shields.io/badge/Shiro-1.3.2-orange)

# 项目简介  
基于SpringBoot + MyBatis Plus + Shiro的在线餐饮服务平台，包含菜品分类管理、订单处理、权限控制和文件上传功能，采用前后端分离架构，支持多数据源配置。

# 特征介绍  
- ​**权限管理**：集成Shiro实现接口级权限控制，支持自定义鉴权注解  
- ​**高效开发**：MyBatis Plus简化单表CRUD操作，通用DAO层设计提升复用性  
- ​**多端适配**：独立admin管理端与front用户端，支持PC端多浏览器兼容  
- ​**智能扩展**：集成百度AI SDK和文件处理工具类，支持图像识别扩展  
- ​**模块化结构**：VO/Model/View分层设计，实体与业务模型分离  

# 代码结构 
```
src/
├── main/
│   ├── java/
│   │   ├── com/
│   │   │   ├── annotation/          # 鉴权注解
│   │   │   ├── config/              # 全局配置
│   │   │   ├── controller/          # 接口层
│   │   │   │   ├── MeishidianController.java
│   │   │   │   ├── MeishidingdanController.java
│   │   │   ├── dao/                 # 数据访问接口
│   │   │   ├── entity/              # 持久化实体
│   │   │   ├── interceptor/         # 请求拦截器
│   │   │   ├── service/             # 服务层
│   │   │   │   ├── impl/            # 服务实现类
│   │   │   ├── utils/               # 工具类
│   ├── resources/
│   │   ├── mapper/                  # MyBatis映射文件
│   │   ├── application.yml          # 主配置
│   │   ├── static/                  # 静态资源
│   │   │   ├── upload/              # 文件上传目录
```
# 使用说明
**推荐浏览器**：谷歌浏览器  
**后台地址**：http://localhost:8080/springboott01gx/admin/dist/index.html  
**管理员账号**：abo / abo  
**前台地址**：http://localhost:8080/springboott01gx/front/index.html  
**数据库配置**：修改application.yml中数据库连接信息：
```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/springboott01gx
    username: root
    password: 你的数据库密码