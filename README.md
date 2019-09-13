[toc]
# SSM框架搭建

## 创建maven项目（Webapp）
### 步骤：
1.我们首先要把全部的环境给配置好：tomcat，maven插件
2.tomcat：使用前要先打开，使用XAMPP打开
3.我们创建完项目后，还是会有路径报错，我们要[修改路径](https://blog.csdn.net/qq_37889636/article/details/79441712)

## 每个配置文件的配置内容（顺序不分先后）
### mybatis配置（startup.src.config.Mybatis.xml）
不需要配置任何内容，需要有文件头，可有可无，非必须
### spring配置（spring-dao、spring-service、spring-web）
#### spring-dao：
spring和mybatis的结合，主要用于连接数据库
#### spring-service：
配置service扫描
#### spring-web（spring-MVC）
配置Controller扫描，使SpringMVC认为包下用了@Contorller注解的类是控制器
配置视图解析器，加上前缀和后缀
### 数据库配置（jdbc.properties）
写关于数据库连接的具体参数，在spring-dao上调用
### log日志配置（log4j.properties）非必需的

到这里配置spring框架就已经基本完成了，我们接下来要完成实例的应用

