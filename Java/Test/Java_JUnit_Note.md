---
aliases: []
tags:
  - java
  - test
  - junit
created: 2025-10-07 02:26:59
modified: 2026-07-23 19:58:45
---

# Junit 笔记

---

## 版本

各版本特性与要求对比：

|         版本          | 发布年份 |          最低 Java 要求          |                                                                      核心特性与架构                                                                      |
|:---------------------:|:--------:|:--------------------------------:|:--------------------------------------------------------------------------------------------------------------------------------------------------------:|
| [JUnit 6](#JUnit%206) | 2025 年  | [Java 17](../Java_Note.md#JDK17) |                              统一了 Platform、Jupiter 和 Vintage 的版本号，原生支持 Kotlin 协程挂起函数测试，并集成了 JFR。                              |
| [JUnit 5](#JUnit%205) | 2017 年  |  [Java 8](../Java_Note.md#JDK8)  |                                   采用模块化设计（Platform + Jupiter + Vintage），扩展性强，广泛应用于现代 Java 项目。                                   |
| [JUnit 4](#JUnit%204) | 2006 年  |  [Java 5](../Java_Note.md#JDK5)  |                                 曾长期统治 Java 测试领域，广泛使用注解，由于年代较久远，目前许多新项目已逐渐弃用或迁移。                                 |
| [JUnit 3](#JUnit%203) | 1998 年  |  [Java 5](../Java_Note.md#JDK5)  | JUnit 3 引入了基本的测试结构，测试方法需要继承自 `junit.framework.TestCase`，并且测试方法必须以`test` 开头。这个版本奠定了 JUnit 作为单元测试框架的基础。 |

---

## JUnit 3

## JUnit 4

---

## JUnit 5

JUnit 5 = [JUnit Platform](#JUnit%20Platform)  + [JUnit Jupiter](#JUnit%20Jupiter) + [JUnit Vintage](#JUnit%20Vintage)

### JUnit Platform

Junit Platform 是在 JVM 上启动测试框架的基础，不仅支持 Junit 自制的测试引擎，其他测试引擎也都可以接入。

### JUnit Jupiter

**JUnit Jupiter** 提供了 JUnit 5 的新的编程模型，是 JUnit 5 新特性的核心。内部 包含了一个测试引擎，用于在 [JUnit Platform](#JUnit%20Platform) 上运行。

**JUnit Jupiter** 定义了测试用例和测试生命周期的 API，实现了 JUnit 5 的新特性。

|       **注解**       |             **说明**             |
|:--------------------:|:--------------------------------:|
|       `@Test`        |          标记测试方法。          |
|    `@BeforeEach`     |   每个测试前运行的初始化方法。   |
|     `@AfterEach`     |    每个测试后运行的清理方法。    |
|     `@BeforeAll`     | 在所有测试之前执行（静态方法）。 |
|     `@AfterAll`      | 在所有测试之后执行（静态方法）。 |
|    `@DisplayName`    |   为测试方法或类设置展示名称。   |
|     `@Disabled`      |      禁用测试方法或测试类。      |
| `@ParameterizedTest` |      参数化测试的标记注解。      |

> [!info] 
> 
> JUnit 5 新注解：
> 
> * `@BeforeEach` 代替 `@Before`
> * `@AfterEach` 代替 `@After`
> * `@BeforeAll` 代替 `@BeforeClass`
> * `@AfterAll` 代替 `@AfterClass`

### JUnit Vintage

由于 JUint 已经发展多年，为了照顾老的项目，JUnit Vintage 提供了兼容 [JUnit 4.x](#JUnit%204),[JUnit 3.x](#JUnit%203) 的测试引擎。

---

## JUnit 6

---

## 使用

项目使用 JUnit 时，管理依赖方式有三种常用方式：

1. [Maven](../Maven/Maven_Note.md)
2. [Gradle](../Groovy_Gradle/Gradle_Note.md)
3. 手动添加

### maven 方式

因为 [JUnit 5](#JUnit%205) 开始，JUnit 有三个组件，为了使用组件版本一致，JUnit 官方提供了一个聚合 POM 方式为项目管理依赖，即`JUnit-bom`。

在 maven 依赖配置时，只需要在 `pom`文件中加入 JUnit-bom 的依赖，就能将[JUnit Jupiter](#JUnit%20Jupiter)、[JUnit Platform](#JUnit%20Platform) 等依赖都添加上，并且保持相互不发生版本冲突的问题！

示例：

```xml
<dependencies>
	<dependency>
		<groupId>org.junit</groupId>
		<artifactId>junit-bom</artifactId>
		<version>5.14.3</version>
		<type>pom</type>
		<scope>import</scope>
	</dependency>
</dependencies>
```

> [!info] 
> 
> JUnit-bom 的 maven 远程仓库： [https://central.sonatype.com/artifact/org.junit/junit-bom](https://central.sonatype.com/artifact/org.junit/junit-bom)

---

## 相关笔记

* [JUnit 资料清单](Java_JUnit_Material.md)
* [Java 测试 笔记](Java_Test_Note.md)
* [Java 测试框架视频清单](Java_Test_Videos.md)
* [Java 笔记](../Java_Note.md)

