> # 1. Service Discovery: Eureka Clients  
# 1. 服务发现: Eureka 客户端
> Service Discovery is one of the key tenets of a microservice based architecture. Trying to hand configure each client or some form of
> convention can be very difficult to do and can be very brittle. Eureka is the Netflix Service Discovery Server and Client. The server can be
> configured and deployed to be highly available, with each server replicating state about the registered services to the others.  

服务发现是微服务基础架构的一个关键原则。  在微服务中尝试配置所有的客户端或者以某种格式的约定来处理微服务的参与者是非常困难和脆弱的。 Eureka是Netflix的一个服务发现服务器和客户端。
Eureka服务器可以被配置和部署为高可用， 并且每个服务的状态可以互相复制。

> ## 1.1 How to Include Eureka Client
## 1.1 引入Eureka客户端
> To include Eureka Client in your project use the starter with group org.springframework.cloud and artifact id
> spring-cloud-starter-netflix-eureka-client . See the [Spring Cloud Project](https://spring.io/projects/spring-cloud) page for details on setting up your build system with the
> current Spring Cloud Release Train.  

使用 group org.springframework.cloud 以及 artifact id spring-cloud-starter-netflic-eureka-client 将eureka client引入到你的项目中。  请参考最新的Spring Cloud发布版本[Spring Cloud Project](https://spring.io/projects/spring-cloud)培训手册页面详细构建你的系统。

> ##1.2 Registering with Eureka
## 1.2 注册到Eureka
> When a client registers with Eureka, it provides meta-data about itself such as host and port, health indicator URL, home page etc. Eureka
receives heartbeat messages from each instance belonging to a service. If the heartbeat fails over a configurable timetable, the instance is
normally removed from the registry.
Example eureka client:
```
@Configuration
@ComponentScan
@EnableAutoConfiguration
@RestController
public class Application {
   @RequestMapping("/")
   public String home() {
      return "Hello world";
   }
	
   public static void main(String[] args) {
      new SpringApplicationBuilder(Application.class).web(true).run(args);
   }
}
```  

当一个客户端需要注册到Eureka服务中， 它需要提供它自己的一些基础信息比如主机信息、端口、健康指标URL、首页URL等给Eureka服务。 Eureka服务通过获取心跳消息方式从每一个客户端信息。 如果在配置的时间内心跳失败， 那么通常Eureka客户端实例就会从Eureka注册中心中删除。
Eurka客户端示例:
```
@Configuration
@ComponentScan
@EnableAutoConfiguration
@RestController
public class Application {
   @RequestMapping("/")
   public String home() {
      return "Hello world";
   }
	
   public static void main(String[] args) {
      new SpringApplicationBuilder(Application.class).web(true).run(args);
   }
}
```

>(i.e. utterly normal Spring Boot app). By having ```spring-cloud-starter-netflix-eureka-client``` on the classpath your application will automatically register with the Eureka Server. Configuration is required to locate the Eureka server. Example:
application.yml.
```
eureka:
  client:
    serviceUrl:
       defaultZone: http://localhost:8761/eureka/
```  

(比如上面这个简单的Spring Boot App)。 只要在你的应用的classpath中包含```spring-cloud-starter-netflix-eureka-client```依赖， 那么你的应用就会自动注册到Eureka服务中。 当然需要在你的应用中配置Eureka服务的信息。 示例：  
application.yml
```
eureka:
  client:
    serviceUrl:
       defaultZone: http://localhost:8761/eureka/
```  

> where "defaultZone" is a magic string fallback value that provides the service URL for any client that doesn’t express a preference (i.e. it’s a useful default).

“defaultZone” 是一个神奇的字符串， 它可以为任何一个没有设置zone的eureka 客户端提供一个默认值。（它是一个有用的默认值）
> The default application name (service ID), virtual host and non-secure port, taken from the ```Environment``` , are ```${spring.application.name} ```, ```${spring.application.name}``` and ```${server.port}``` respectively  

默认的应用名称(服务ID)、虚拟地址、非安全端口号都是从```Environemt```类中获取， 值分别是 ```${spring.application.name} ```, ```${spring.application.name}``` 和 ```${server.port}```。  
>Having ```spring-cloud-starter-netflix-eureka-client``` on the classpath makes the app into both a Eureka "instance" (i.e. it registers itself) and a "client" (i.e. it can query the registry to locate other services). The instance behaviour is driven by ```eureka.instance.*``` configuration keys, but the defaults will be fine if you ensure that your application has a ```spring.application.name``` (this is the default for the Eureka service ID, or VIP).

在classpath中包含```spring-cloud-starter-netflix-eureka-client```依赖的， 既是一个Eureka的"实例"(注册自己)也是一个Eureka的"客户端"(可以在Eureka服务的注册中心上定位其他服务)。  实例的所有行为都是通过 ```eureka.instance.*```相关键来配置的， 只要你能保证你的应用有一个```spring.application.name```，其他的通常情况下默认的配置已经够用了(这个是客户端默认给Eureka服务的ID或VIP信息)

>See [EurekaInstanceConfigBean](https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-eureka-client/src/main/java/org/springframework/cloud/netflix/eureka/EurekaInstanceConfigBean.java) and [EurekaClientConfigBean](https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-eureka-client/src/main/java/org/springframework/cloud/netflix/eureka/EurekaClientConfigBean.java) for more details of the configurable options.

可以查看 [EurekaInstanceConfigBean](https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-eureka-client/src/main/java/org/springframework/cloud/netflix/eureka/EurekaInstanceConfigBean.java) 和 [EurekaClientConfigBean](https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-eureka-client/src/main/java/org/springframework/cloud/netflix/eureka/EurekaClientConfigBean.java)类获取更多的Eureka实例和客户端配置信息

>To disable the Eureka Discovery Client you can set ```eureka.client.enabled``` to ```false``` .

如果想禁止Eureka客户端的服务发现功能，可以将```eureka.client.enabled``` 属性设置为 ```false``` .