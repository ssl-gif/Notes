# 01_SpringBoot-快速入门



​	SpringBoot可以帮我们简单、快速地创建一个独立的、生产级别的Spring应用，SpringBoot的底层是Spring。大多数SpringBoot应用只需要编写少量配置，即可快速整合Spring平台以及第三方技术。SpringBoot具有以下特性：

- 快速创建独立的Spring应用
- 直接嵌入Tomcat、Jetty、Undertow等Servlet容器，无需部署war包
- 提供可选的场景启动器-starter，简化应用整合
- 按需自动配置Spring以及第三方库**（约定大于配置）**
- 提供生产级特性，例如：监控指标、健康检查、外部化配置等
- 完全无代码生成、无xml配置文件

总结：简化开发、简化配置、简化整合、简化部署、简化监控、简化运维



## 一.快速入门

​	实现功能：浏览器发送 /hello 请求，返回 "Hello, Spring Boot!"

### 1.开发流程

#### (1).创建项目

​	创建maven项目，继承自SpringBoot的父级场景启动器 `spring-boot-starter-parent` 依赖

```xml
<!-- 所有SpringBoot项目都必须继承自spring-boot-starter-parent依赖-->
<parent>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-parent</artifactId>
    <version>3.3.0</version>
</parent>
```

#### (2).导入场景

​	导入web开发的场景启动器 `spring-boot-starter-web` 依赖

```xml
<!--web开发的场景启动器-->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
```

#### (3).编写主程序代码

```java
@SpringBootApplication
public class MainApplication {
    public static void main(String[] args) {
        SpringApplication.run(MainApplication.class, args);
    }
}
```

#### (4).编写业务代码

```java
@RestController
public class HelloController {

    @RequestMapping("/hello")
    public String hello() {
        return "Hello, Spring Boot!";
    }

}
```



#### (5).测试

​	启动SpringBoot主程序后，使用浏览器访问：localhost:8080/hello

<img src="D:\Files\Notes\SpringBoot\01_SpringBoot-核心特性\images\快速入门程序测试.png" alt="快速入门程序测试"  />

#### (6).打包

```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
        </plugin>
    </plugins>
</build>
```



### 2.特性小结





## 二.应用分析



## 三.核心技能



​	

























