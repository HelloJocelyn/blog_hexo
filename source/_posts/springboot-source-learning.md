## 初始化SpringApplication
### 识别应用类型：主要根据classpath中是否包含对应类型的类。
1. 包含webflux,但是不包含mvc,jersy时类型为REACTIVE
2. 不包含servlet时为None
3. 否则为servlet。
** 也可以在初始应用程序中指定类型 **

### 设置初始化器
读取配置的ApplicationContextInitializer，初始化，并赋值给SpringApplication的initializers。

读取过程如下：
读取应用包含第三方jar包下META-INF/spring.factories，读取其配置的listeners,post processors，analyzers，FailureAnalysisReporters等等
注：如果想要自己实现相应功能，也可在自己应用下创建META-INF/spring.factories文件加以配置。

### 设置监听器

读取并初始化ApplicationListener，赋值给SpringApplication的listeners。
### 设置mainApplicationClass
即启动应用入口类

##  运行SpringApplication

###  获取运行监听器
###  启动运行监听器
###  获取应用参数
###  准备环境
###  配置忽视bean信息
###  printBanner
###  创建应用上下文环境
###  获取配置的SpringBootExceptionReporter
###  准备上下文
###  刷新上下文
###  刷新上下文后操作
###  运行监听器启动
###  调起runners

