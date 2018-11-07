> # 1. Service Discovery: Eureka Clients  
# 1. 服务发现: Eureka 客户端
> Service Discovery is one of the key tenets of a microservice based architecture. Trying to hand configure each client or some form of
> convention can be very difficult to do and can be very brittle. Eureka is the Netflix Service Discovery Server and Client. The server can be
> configured and deployed to be highly available, with each server replicating state about the registered services to the others.  

服务发现是微服务基础架构的一个关键原则。  在微服务中尝试配置所有的客户端或者以某种格式的约定来处理微服务的参与者是非常困难和脆弱的。 Eureka是Netflix的一个服务发现服务器和客户端。
Eureka服务器可以被配置和部署为高可用， 并且每个服务的状态可以互相复制。