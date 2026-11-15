# 学习 Java 25

📖 **阅读教程：[https://stahe.github.io/zh-java-oct-2026/](https://stahe.github.io/zh-java-oct-2026/)**

本课程**通过示例**教你 [Java](https://dev.java/) 25 语言：两百多个程序（320 个 Java 文件），逐行注释，并附有其运行结果。课程从语言基础开始，涵盖使用 JDBC 和 Hibernate 访问数据库、网络编程，以及使用 Spring Boot 的 Web 服务。

这是课程[用 .NET 10 学习 C# 14](https://stahe.github.io/zh-csharp-oct-2026/)（2026 年 10 月）的 Java 版本，而后者本身是对 2008 年一门 C# 课程的重写：大纲相同、示例相同、贯穿全程的主题相同，只是用现代 Java 编写。所有程序都使用 JDK 25（`javac -Xlint:all`）**无错误、无警告**地编译，并且都已运行；课程中展示的结果均来自这些运行。

| C# 14 课程（2026） | Java 25 课程（2026） |
|---|---|
| C# 14、.NET 10（LTS） | Java 25（LTS）、JDK 25 |
| 单文件应用（`dotnet run prog.cs`） | 紧凑源文件（`java Prog.java`） |
| `.csproj` 项目、`.slnx` 解决方案、NuGet | Maven 项目（`pom.xml`）、Maven Central |
| 属性、结构体、运算符重载 | 访问器、记录、密封类、模式匹配 |
| LINQ | Stream API |
| 委托和事件 | 函数式接口、lambda、监听器 |
| `Task`、`async` / `await` | `CompletableFuture`、虚拟线程 |
| MSTest、Microsoft.Extensions.DependencyInjection | JUnit 6、Spring Framework 7 |
| System.Text.Json | Jackson 3 |
| ADO.NET、MySqlConnector | JDBC、MySQL Connector/J、HikariCP |
| Entity Framework Core | **Hibernate 7**（Jakarta Persistence 3.2） |
| `HttpClient`、`TcpClient` / `TcpListener` | `java.net.http.HttpClient`、`Socket` / `ServerSocket` |
| ASP.NET Core Minimal API | Spring Boot 4 |

## 课程大纲

| 章节 | 内容 |
|---|---|
| 安装 | JDK 25、IntelliJ IDEA / VS Code、`java` 和 `javac` 命令、紧凑源文件、Maven、多模块项目 |
| 语言基础 | 类型、`var`、代码块、转换、数组、运算符、`switch` 表达式和模式匹配、受检异常和非受检异常、带资源的 `try`、枚举、参数传递 |
| 类、记录、接口 | 类、继承、多态、密封类、`equals` / `hashCode` / `compareTo`、接口、抽象类、泛型、包和模块、记录、对象的模式匹配、`Optional` |
| 常用的 Java 类 | 字符串、数组、集合（包括有序集合）、**Stream API** 和 `Gatherers`、文本和二进制文件（`java.nio.file`）、使用 Jackson 3 处理 JSON、正则表达式 |
| 分层架构 | [DAO] / [business] / [UI] 层、多模块 Maven 项目、**JUnit 6** 单元测试、使用 Spring 的**依赖注入** |
| 函数式接口、lambda 和事件 | `java.util.function`、lambda、方法引用、闭包、组合、事件监听器、`PropertyChangeSupport` |
| 执行线程 | `Thread`、**虚拟线程**、`synchronized`、`ReentrantLock`、`Condition`、原子操作、`Semaphore`、`CountDownLatch`、并发集合、`ExecutorService`、fork/join、`ThreadLocal`、`ScopedValue` |
| 异步编程 | `CompletableFuture` 和虚拟线程、组合、异常、取消和超时、进度、异步 I/O、`Flow`、结构化并发（概述） |
| 使用 JDBC 访问数据库 | MySQL、MySQL Connector/J、`DataSource` 和 HikariCP、参数化查询和 SQL 注入、事务、批处理、`CachedRowSet` |
| **Hibernate** | 实体、`SessionFactory` / `Session`、CRUD、持久化上下文、HQL 和 Criteria API、关系和懒加载、迁移、乐观并发、原生 SQL、`StatelessSession`、Spring ORM 和 `@Transactional` |
| Web 编程 | TCP/IP、IPv6、`InetAddress`、TCP 客户端和服务器（每个客户端一个虚拟线程）、HTTP、`HttpClient`、SMTP |
| Web 服务 | 使用 **Spring Boot 4** 的 REST / JSON、Java 控制台客户端、JavaScript Web 客户端、Node.js 客户端 |

## 贯穿主线：9 个版本的所得税计算器

在整个课程中，我们逐个版本地构建一个**所得税计算器**应用：

- **版本 1**：单个程序；**版本 2**：类和接口；**版本 3**：从文本文件或 JSON 文件读取数据；
- **版本 4 和 5**：使用 Maven 模块的分层架构，用 JUnit 测试，并通过 Spring 依赖注入集成；
- **版本 6 和 7**：数据存储在 MySQL 数据库中，先用 JDBC 读取，再用 Hibernate 读取；
- **版本 8**：税款计算的 TCP 服务器及其客户端；
- **版本 9**：Spring Boot REST Web 服务、其控制台客户端及其 Web 客户端。

## 技术

Java 25 · JDK 25 · Maven 3.9 · IntelliJ IDEA · VS Code · JUnit 6 · Spring Framework 7 · Jackson 3 · MySQL 8 · MySQL Connector/J 9 · HikariCP · Hibernate ORM 7.4 · Jakarta Persistence 3.2 · Spring Boot 4.1 · Laragon

## 先决条件

- 具备任意一种语言的编程经验。
- [JDK 25](https://adoptium.net)（Eclipse Temurin 或其他发行版）、[Maven](https://maven.apache.org)，以及一个 IDE（[IntelliJ IDEA](https://www.jetbrains.com/idea/) 或安装了 Extension Pack for Java 的 [VS Code](https://code.visualstudio.com)）；数据库章节需要用 [Laragon](https://laragon.org) 提供 MySQL。课程中提供了安装说明。

## 作者

本课程及其代码由 [Anthropic](https://www.anthropic.com) 的 AI **Claude** 编写（2026 年 10 月），应 Serge Tahé 的请求完成，基于他的 C# 14 课程。

审阅：[Serge Tahé](https://stahe.github.io)
