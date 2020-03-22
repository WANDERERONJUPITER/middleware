中间件的必要性以及在现代编程语言中如何在该层面中抽象出来

首先是定义，它是个什么？

高效（海量的并发请求）可靠的中间件

### 基础篇

#### 快速安装

确保系统网络、yum可用，关闭IPtables规则并停用SElinux

安装依赖

```bash
yum -y install gcc gcc-c++ autoconf pcre pcre-devel make automake
yum -y install wget httpd-tools vim
```

查看并关闭IPtables

```shell
iptables -L
iptables -F
iptables -t nat -L
iptables -t nat -F
```

 查看并关闭SElinux

```
getenforce
#use this to make sure SElinux Disabled
setenforce 0
```



#### 配置语法

#### 默认模块

#### log

#### 访问限制

##### HTTP的请求和连接

##### 请求的限制和连接的限制

##### access模块配置语法

##### 请求限制的局限性

##### 基本安全认证

##### auth模块配置语法

##### 安全认证局限性

### 场景实践

#### 静态资源WEB服务

什么是静态资源

服务场景

服务配置

客户端缓存

资源压缩

防盗链

跨域访问

#### 代理服务

#### 负载均衡

#### 缓存服务

### 深度学习

#### 动静分离

#### rewrite规则

#### HTTPS服务

HTTPS协议

配置语法

苹果要求的https服务

#### nginx与lua开发

#### 模块配置

### 架构篇

#### 常见问题

#### 性能优化

调适性能优化

性能的影响因素

操作系统性能优化

#### 安全相关

#### 其他特性

#### 架构设计

