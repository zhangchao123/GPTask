# MyBaits 课后作业

## 第一节课

#### **问题：** resultType（属性）和resultMap（标签引用）的区别？

**答案：**它们两个都是用于返回结果的封装，不同的是

resultType 是根据类路径或者配置的别名找对应的反射注入的

resultMap是在加载mapperRegistry时通过解析xml确定结构的

------

#### collection和association的区别？

**答案：**它们都是解决管理问题的，不同的是

collection是一对多

association是一对一

------

#### Statement和PreparedStatement的区别？

**答案：**PreparedStatement继承Statement，Statement是java jdk中执行数据库操作的接口，而PreparedStatement是各个数据库驱动包对其的扩展接口，最重要的是PreparedStatement是通过？来进行参数传递的，这样，避免了拼接sql注入而出现的sql注入问题

------



#### Mybaits用到的设计模式

Executor、SqlsessionFactory创建 ：**静态工厂模式**

ExecutorSqlSessionFactoryBuilder ：**建造者**

CachingExecutor->BatchExecutor等：**装饰者**

MapperRegistry 中的类、实现了Interceptor的类，PooledConnection：**代理模式**

BaseExecutor 的实现 ：**模板模式**



