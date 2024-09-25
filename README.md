

# enterprise 门户网站

通用企业门户网站，门户所有内容均可在后台配置，支持多皮肤，以及自定义皮肤开发，皮肤可在后台配置。

功能模块：轮播图，发展历程，关于我们，服务领域，新闻动态，团队风采，诚聘英才，联系我们

管理后台主要包括门户上各个板块得内容发布管理，和系统设置。门户演示地址http://upint.cn/enterprise/

## 配料表：

* 开发语言：Java

* 模版引擎：JSP

* 数 据 库：MySQL 5.7，如果使用新版本的mysql请参考下面mysql升级

* 核心框架：Spring、SpringMVC、mybatis、ehcache

* 皮肤开发：在webapp下创建文件夹，在webapp\manage\systemsetting\systemSettingEdit.jsp中加上皮肤配置项，进行模板开发，修改配置即可生效。目前已有2套皮肤，可以切换查看。

## mysql升级

升级到较新版本，如8.*请更新pom文件中的jdbc相关jar包

pom文件：

增加

<dependency>
    
    <groupId>javax.annotation</groupId>
    
    <artifactId>javax.annotation-api</artifactId>
    
    <version>1.3.2</version>
    
</dependency>

修改pom.xml

<dependency>
    
    <groupId>mysql</groupId>
    
    <artifactId>mysql-connector-java</artifactId>
    
    <version>8.0.18</version>
    
</dependency>

<dependency>
    
    <groupId>org.springframework</groupId>
    
    <artifactId>spring-jdbc</artifactId>
    
    <version>5.2.7.RELEASE</version>
    
</dependency>

修改conf.properties

jdbc.driver=com.mysql.cj.jdbc.Driver

jdbc.url=jdbc:mysql://localhost:3306/enterprise?useUnicode=true&characterEncoding=UTF-8&serverTimezone=Asia/Shanghai


## 快速开始

* IDEA导入项目

* 新建数据库enterprise,导入enterprise.sql文件

* 使用tomcat启动

* 前端地址：http://localhost:8080/enterprise_war

* 后端地址：http://localhost:8080/enterprise_war/manage/user/login



## 捐赠


# 系统预览

## 首页
![首页](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/home.png)
## 服务
![服务](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/service.png)
## 新闻
![新闻](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/article.png)
## 团队
![团队](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/team.png)
## 招聘
![招聘](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/job.png)
## 联系
![联系](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/contact.png)

## 后端首页
![后端首页](https://github.com/zhupanlinch/enterprise/blob/master/src/main/webapp/attached/image/back.png)



