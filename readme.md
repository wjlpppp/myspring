# 实现spring的ioc

Spring IoC容器的实现原理：工厂模式 + 解析XML + 反射机制

基于singleton和setter注入

- 反射

先定义ioc容器，Application是一个接口类



然后写一个ClassPathXmlApplicationContext实现这个接口类，将xml解析后获取的id、class、property，利用反射的技术将这些bean进行实例化

* xml的解析，利用了dom4j

​	将配置好的xml的文件中的每个bean进行解析，将bean中的id，class，以及property进行解析获取![68183224422](C:\Users\万俊良\AppData\Local\Temp\1681832244222.png)



