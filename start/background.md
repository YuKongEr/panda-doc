## 1 、代码clone {docsify-ignore}

```bash
git clone git@github.com:YuKongEr/panda-cloud.git
```

clone完后，使用idea打开项目。

## 2、初始化数据库 {docsify-ignore}

路径

`/panda/sql/init.sql`

创建一个名为`cloud`的数据库即可，运行`init.sql`中的sql，生成表与数据。

## 3、配置处理  {docsify-ignore}

1、首先`fork`我`github`上的配置到自己的`github`中

 [`配置github地址`](<https://github.com/YuKongEr/config-reps>)

2、打开刚刚导入的`panda`功能 找到`panda-config-server`模块，把其中git配置的地址

指向你fork完之后你的git地址。

![](https://ws3.sinaimg.cn/large/006tNc79ly1g2g37q82aej30tq0gswg6.jpg)

3、然后`clone`自己的配置仓库到本地。



切换到dev分支 `git chenckout dev`

!> 一定要切换到dev分支，才会有下文所说的这些配置文件

### 数据库配置修改  {docsify-ignore}

修改涉及的配置文件

`application-dev.yml`

```yaml
spring:
  datasource:
    url: 你的地址
    driver-class-name: com.mysql.jdbc.Driver
    username: 你的用户名
    password: 你的密码
    max-idle: 10
    min-idle: 5
    test-on-borrow: false
    time-between-eviction-runs-millis: 18800
    test-while-idle: true
    validation-query: SELECT 1
    hikari:
      minimum-idle: 0
```

### Redis配置修改   {docsify-ignore}

修改涉及的配置文件

`application-dev.yml`



```yaml
spring:
	redis:
    host: 
    port: 
    password: 
    timeout: 
```

### RabbitMQ配置 {docsify-ignore}

修改涉及的配置文件

`application-dev.yml`

```yaml
spring:
	 rabbitmq:
    host: 
    port: 
    username: 
    password: 
```



`panda-zipkin-dev.ym`

```yaml
zipkin:   
  collector:
    rabbitmq:
      addresses: 
      port: 
      username: 
      password: 
      virtual-host: /
      queue: zipkin
```

配置修完之后记得把修改完的文件push到自己github的远程dev分支上。

!> 这里还是提醒一下这一切的操作都是在dev分支下操作，所有你push也要push到dev分支上



## 4、启动  {docsify-ignore}

依次按顺序启动各个模块

1. PandaServer
2. PandaConfigServer
3. PandaUserService
4. PandaMessageService
5. PandaAuth
6. PandaGateway

如果需要使用`zikpin追踪`跟代码生成器，则再启动相应模块即可。

