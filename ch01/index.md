> # 1. Service Discovery: Eureka Clients  
# 1. 服务发现: Eureka 客户端
> Service Discovery is one of the key tenets of a microservice based architecture. Trying to hand configure each client or some form of
> convention can be very difficult to do and can be very brittle. Eureka is the Netflix Service Discovery Server and Client. The server can be
> configured and deployed to be highly available, with each server replicating state about the registered services to the others.