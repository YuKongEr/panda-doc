## 环境依赖



|依赖项 | 版本  |
| :--: | :--: |
|  JDK |  1.8 |
| Maven | 3.2 |
| Redis | 5.0.4 |
| MySQL | 5.7 |
| RabbitMQ | 3.7.7 |

!> 其中JDK强制要求1.8  MySQL强制要求5.7



## 开发插件配置

> 本项目建议使用IDEA开发，一时IDEA一时爽，一直IDEA一直爽，但是同样支持使用eclipse开发

由于本项目使用了`Lombok`注解，所以需要`ide`的支持。

### Lombok安装

打开`idea` 进入 进入设置插件安装页面，搜索`lombok`点击安装即可。

> mac环境安装实例

依次点击`IDEA` -> `Prefrerences` ->`plugins` 进入插件安装页面

搜索` lombok` 如下图

![lombok安装](https://ws1.sinaimg.cn/large/006tNc79ly1g2g24u4ht7j318r0u0n58.jpg)

点击安装既可以。

!> 注意 lombok是必须安装，不然会出现导入项目提示很多set方法没有定义的错误。

> 接下来的一些插件不是强制要求，只是一些提高开发效率的工具

- A8Transtlate 翻译插件，阅读源码的时候可以一键翻译提高效率
- Alibaba Java Coding Guidelines 代码规范检测插件，提供代码规范
- Grep Console 控制台异常着重标识，比较醒目
- MyBatisCodeHelperPro mybatis插件，方便书写mapper等



