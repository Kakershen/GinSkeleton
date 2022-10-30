## 这是什么?
-   1.这是一个基于go语言gin框架的web项目骨架，专注于前后端分离的业务场景,其目的主要在于将web项目主线逻辑梳理清晰，最基础的东西封装完善，开发者更多关注属于自己的的业务即可。
-   2.本项目骨架封装了以`tb_users`表为核心的全部功能（主要包括用户相关的接口参数验证器、注册、登录获取token、刷新token、CURD以及token鉴权等），开发者拉取本项目骨架，在此基础上就可以快速开发自己的项目。
-   3.<font color=#FF4500>本项目骨架请使用 `master` 分支版本即可, 该分支是最新稳定分支 </font>.
-   4.<font color=#FF4500>本项目骨架从V1.4.00开始，要求go语言版本必须 >=1.15，才能稳定地使用gorm v2读写分离方案,go1.15下载地址：https://studygolang.com/dl </font>
-   5.该版本定位为主线版本,总体追求简洁、无界面，没有太多的业务逻辑，适合开发者自己随意扩展.

### 启动项目
启动项目
本项目的根目录就是 go.mod 所在的目录，开发者可以通过命令启动，也可以通过 goland 快速启动，
本项目骨架有三个入口，命令启动方式需要进入根目录，选择其中一个入口启动：
 ```
 go run cmd/web/main.go  ： 一般是后台服务相关的接口，例如：admin系统等
 ```
 ```
 go run cmd/api/main.go ：门户网站接口，主要是针对前台，提供数据查询、展示等服务类接口
 ```
 ```
 go run cmd/cli/main.go ： 命令模式入口，开发黑窗口这种命令时使用的模式.
 ```

 ### 项目结构
 ```
|-- app
|   |-- aop		// Aop切面demo代码段
|   |   `-- users
|   |-- core		// 程序容器部分、用于表单参数器注册、配置文件存储等
|   |   |-- container
|   |   |-- destroy
|   |   `-- event_manage
|   |-- global		// 全局变量以及常量、程序运行错误定义
|   |   |-- consts
|   |   |-- my_errors
|   |   `-- variable
|   |-- http		// http相关代码段，主要为控制器、中间件、表单参数验证器
|   |   |-- controller
|   |   |-- middleware
|   |   `-- validator
|   |-- model		// 数据库表模型
|   |   |-- base_model.go
|   |   `-- users.go
|   |-- service
|   |   |-- sys_log_hook
|   `-- utils	// 第三方包封装层
|       |-- gorm_v2
|       |-- ... ...
|-- bootstrap	// 项目启动初始化代码段
|   `-- init.go
|-- cmd			// 项目入口，分别为门户站点、命令模式、web后端入口文件
|   |-- api
|   |   `-- main.go
|   |-- cli
|   |   `-- main.go
|   `-- web
|       `-- main.go
|-- command		// cli模式代码目录
|   |-- 
|-- config		// 项目、数据库参数配置
|   |-- config.yml
|   `-- gorm_v2.yml
|-- database
|-- docs		// 项目文档
|   |-- 
|-- go.mod
|-- go.sum
|-- public
|-- routers		// 后台和门户网站路由
|   |-- api.go
|   `-- web.go
|-- storage		// 日志、资源存储目录
|   `-- 
`-- test// 单元测试目录
    |--
 ```

### [GinSkeleton 新版在线文档](https://www.yuque.com/xiaofensinixidaouxiang/bkfhct/mar1g7)
- 1.我们花费了极大的精力编写了非常完整、高质量的文档,初学者优先从如何使用学起, 成熟的开发者可以与我们一起研究 gin 内核源码,成为 gin 框架的高级开发.
- 2.学习 GinSkeleton 您只需要关注主线即可,我们没有创造太多新的语法,只要您会使用 gin 就可以迅速上手 Ginskeleton .
- 3. $\color{red}{QQ群：129885228}$

[旧文档入口](./ReadMEBak.md)


###  ginskeleton 路由跳转插件
- ginskeleton 的路由是基于容器加载的，需要安装插件才能实现快速跳转.
- 安装步骤：https://www.yuque.com/xiaofensinixidaouxiang/bkfhct/ngfzv1


### [点击进入 GinSkeleton-Admin2 系统](https://www.yuque.com/xiaofensinixidaouxiang/qmanaq/qmucb4)
- admin 系统集成界面, 定位快速开发业务方向, 可以在不需要修改一行代码的情况下，快速进入业务开发模式.



#### V 1.5.56  2022-10-16（最新版本）
**新增**
- 1.增加 `makefile` 编译方式, 方便 `linux` 系统快速编译.

### 感谢 jetbrains 为本项目提供的 goland 激活码
![https://www.jetbrains.com/](https://www.ginskeleton.com/images/jetbrains.jpg)
