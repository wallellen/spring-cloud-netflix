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
使用 group org.springframework.cloud 以及 artifact id spring-cloud-starter-netflic-eureka-client 将eureka client引入到你的项目中。  请参考最新的Spring Cloud发布版本[Spring Cloud Project](https://spring.io/projects/spring-cloud)培训手册页面详细构建你的系统，