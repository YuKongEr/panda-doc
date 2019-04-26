## Panda-Cloud

[![](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/YuKongEr/panda)
[![](https://img.shields.io/badge/release-v1.0-brightgreen.svg
)](https://github.com/YuKongEr/panda)
[![](https://img.shields.io/badge/springboot-%3E%3D2.0-blue.svg
)](https://github.com/YuKongEr/panda)
[![](https://img.shields.io/badge/springcloud-Finchley.SR1-blue.svg
)](https://github.com/YuKongEr/panda)



- 代码生成：提供灵活模板设置，减少重复工作
- 全面登录：手机验证码登录，用户名密码登录
- 动态路由: 基于zuul配置，提供ui界面配置
- 操作日志：记录登录日志，操作日志，异常日志，采用自己定义注解`@SysLog`即可
- 消息总线：使用spring bus提供配置动态刷新
- 接口文档：zuul聚合swagger 提供api文档
- 消息中心：集成阿里云 腾讯云 钉钉，提供接口发送短信、邮件

## 技术选型&文档

- Spring Boot（[查看Spring Boot学习&使用指南](https://www.jianshu.com/p/0d400d30936b)）
- Spring Cloud（[查看官方中文文档](https://springcloud.cc/spring-cloud-dalston.html)）

- Spring Security Oauth2（[查看官方中文文档](http://projects.spring.io/spring-security-oauth/docs/oauth2.html)）

- MyBatis（[查看官方中文文档](http://www.mybatis.org/mybatis-3/zh/index.html)）

- MyBatis plus（[查看官方中文文档](http://mp.baomidou.com/)）

- Vue.js（[查看官方中文文档](https://cn.vuejs.org/)）

- ElementUI（[查看官方中文文档](http://element.eleme.io/#/)）

- Redis

- RabbitMq

- OSS


## 介绍

- panda-server 服务注册中心
- panda-auth  oauth2 认证服务器 提供token
- panda-common 公共模块集合
- panda-config-server 配置中心服务器
- panda-gateway 统一网关，提供动态路由 同时也是oauth2的资源服务器
- panda-zipkin zipkin链路追踪模块
- panda-service 业务模块集合
  - panda-user-service 统一用户管理模块
  - panda-gen-service 代码生成器模块
  - panda-message-service 消息处理器模块
    
