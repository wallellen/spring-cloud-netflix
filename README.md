# spring-cloud-netflix

# [1. Service Discovery: Eureka Clients (服务发现: Eureka客户端)](./ch01/index.md#1) 
## [1.1. How to Include Eureka Client (如何引入一个客户端)](./ch01/index.md#1.1) 
## [1.2. Registering with Eureka](./ch01/index.md#1.2) 
## [1.3. Authenticating with the Eureka Server](./ch01/index.md#1.3) 
## [1.4. Status Page and Health Indicator](./ch01/index.md#1.4) 
## [1.5. Registering a Secure Application](./ch01/index.md#1.5) 
## [1.6. Eureka’s Health Checks](./ch01/index.md#1.6) 
## [1.7. Eureka Metadata for Instances and Clients](./ch01/index.md#1.7) 
### [1.7.1. Using Eureka on Cloud Foundry](./ch01/index.md#1.7.1) 
### [1.7.2. Using Eureka on AWS](./ch01/index.md#1.7.2) 
### [1.7.3. Changing the Eureka Instance ID](./ch01/index.md#1.7.3) 
## [1.8. Using the EurekaClient](./ch01/index.md#1.8) 
### [1.8.1. EurekaClient without Jersey](./ch01/index.md#1.8.1) 
## [1.9. Alternatives to the native Netflix EurekaClient](./ch01/index.md#1.9) 
## [1.10. Why is it so Slow to Register a Service?](./ch01/index.md#1.10) 
## [1.11. Zones](./ch01/index.md#1.11) 

# [2. Service Discovery: Eureka Server](./ch02/index.md#2) 
## [2.1. How to Include Eureka Server](./ch02/index.md#2.1) 
## [2.2. How to Run a Eureka Server](./ch02/index.md#2.2) 
## [2.3. High Availability, Zones and Regions](./ch02/index.md#2.3) 
## [2.4. Standalone Mode](./ch02/index.md#2.4) 
## [2.5. Peer Awareness](./ch02/index.md#2.5) 
## [2.6. Prefer IP Address](./ch02/index.md#2.6) 

# [3. Circuit Breaker: Hystrix Clients](./ch03/index.md#3) 
## [3.1. How to Include Hystrix](./ch03/index.md#3.1) 
## [3.2. Propagating the Security Context or using Spring Scopes](./ch03/index.md#3.2) 
## [3.3. Health Indicator](./ch03/index.md#3.3) 
## [3.4. Hystrix Metrics Stream](./ch03/index.md#3.4) 
# [4. Circuit Breaker: Hystrix Dashboard](./ch04/index.md#4) 

# [5. Hystrix Timeouts And Ribbon Clients](./ch05/index.md#5) 
## [5.1. How to Include Hystrix Dashboard](./ch05/index.md#5.1) 
## [5.2. Turbine](./ch05/index.md#5.2) 
## [5.3. Turbine Stream](./ch05/index.md#5.3) 

# [6. Client Side Load Balancer: Ribbon](./ch06/index.md#6) 
## [6.1. How to Include Ribbon](./ch06/index.md#6.1) 
## [6.2. Customizing the Ribbon Client](./ch06/index.md#6.2) 
## [6.3. Customizing default for all Ribbon Clients](./ch06/index.md#6.3) 
## [6.4. Customizing the Ribbon Client using properties](./ch06/index.md#6.4) 
## [6.5. Using Ribbon with Eureka](./ch06/index.md#6.5) 
## [6.6. Example: How to Use Ribbon Without Eureka](./ch06/index.md#6.6) 
## [6.7. Example: Disable Eureka use in Ribbon](./ch06/index.md#6.7) 
## [6.8. Using the Ribbon API Directly](./ch06/index.md#6.8) 
## [6.9. Caching of Ribbon Configuration](./ch06/index.md#6.9) 
## [6.10. How to Configure Hystrix thread pools](./ch06/index.md#6.10) 
## [6.11. How to Provide a Key to Ribbon’s IRule](./ch06/index.md#6.11) 

# [7. Declarative REST Client: Feign](./ch07/index.md#7) 
## [7.1. How to Include Feign](./ch07/index.md#7.1) 
## [7.2. Overriding Feign Defaults](./ch07/index.md#7.2) 
## [7.3. Creating Feign Clients Manually](./ch07/index.md#7.3) 
## [7.4. Feign Hystrix Support](./ch07/index.md#7.4) 
## [7.5. Feign Hystrix Fallbacks](./ch07/index.md#7.5) 
## [7.6. Feign and @Primary](./ch07/index.md#7.6) 
## [7.7. Feign Inheritance Support](./ch07/index.md#7.7) 
## [7.8. Feign request/response compression](./ch07/index.md#7.8) 
## [7.9. Feign logging](./ch07/index.md#7.9) 

# [8. External Configuration: Archaius](./ch08/index.md#8) 

# [9. Router and Filter: Zuul](./ch09/index.md#9) 
## [9.1. How to Include Zuul](./ch09/index.md#9.1) 
## [9.2. Embedded Zuul Reverse Proxy](./ch09/index.md#9.2) 
## [9.3. Zuul Http Client](./ch09/index.md#9.3) 
## [9.4. Cookies and Sensitive Headers](./ch09/index.md#9.4) 
## [9.5. Ignored Headers](./ch09/index.md#9.5) 
## [9.6. Management Endpoints](./ch09/index.md#9.6) 
### [9.6.1. Routes Endpoint](./ch09/index.md#9.6.1) 
### [9.6.2. Filters Endpoint](./ch09/index.md#9.6.2) 
## [9.7. Strangulation Patterns and Local Forwards](./ch09/index.md#9.7) 
## [9.8. Uploading Files through Zuul](./ch09/index.md#9.8) 
## [9.9. Query String Encoding](./ch09/index.md#9.9) 
## [9.10. Plain Embedded Zuul](./ch09/index.md#9.10) 
## [9.11. Disable Zuul Filters](./ch09/index.md#9.11) 
## [9.12. Providing Hystrix Fallbacks For Routes](./ch09/index.md#9.12) 
## [9.13. Zuul Timeouts](./ch09/index.md#9.13) 
### [9.13.1. Service Discovery Configuration](./ch09/index.md#9.13.1) 
### [9.13.2. URL Configuration](./ch09/index.md#9.13.2) 
## [9.14. Rewriting Location header](./ch09/index.md#9.14) 
## [9.15. Zuul Developer Guide](./ch09/index.md#9.15) 
### [9.15.1. The Zuul Servlet](./ch09/index.md#9.15.1) 
### [9.15.2. Zuul RequestContext](./ch09/index.md#9.15.2) 
### [9.15.3. @EnableZuulProxy vs. @EnableZuulServer](./ch09/index.md#9.15.3)  
### [9.15.4. @EnableZuulServer Filters](./ch09/index.md#9.15.4) 
### [9.15.5. @EnableZuulProxy Filters](./ch09/index.md#9.15.5)  
### [9.15.6. Custom Zuul Filter examples](./ch09/index.md#9.15.6)  
### [9.15.7. How to Write a Pre Filter](./ch09/index.md#9.15.7)  
### [9.15.8. How to Write a Route Filter](./ch09/index.md#9.15.8)  
### [9.15.9. How to Write a Post Filter](./ch09/index.md#9.15.9)  
### [9.15.10. How Zuul Errors Work](./ch09/index.md#9.15.10)  
### [9.15.11. Zuul Eager Application Context Loading](./ch09/index.md#9.15.11) 

# [10. Polyglot support with Sidecar](./ch10/index.md#10) 

# [11. RxJava with Spring MVC](./ch11/index.md#11) 

# [12. Metrics: Spectator, Servo, and Atlas](./ch12/index.md#12) 
## [12.1. Dimensional vs. Hierarchical Metrics](./ch12/index.md#12.1) 
## [12.2. Default Metrics Collection](./ch12/index.md#12.2) 
## [12.3. Metrics Collection: Spectator](./ch12/index.md#12.3) 
### [12.3.1. Spectator Counter](./ch12/index.md#12.3.1) 
### [12.3.2. Spectator Timer](./ch12/index.md#12.3.2) 
### [12.3.3. Spectator Gauge](./ch12/index.md#12.3.3) 
### [12.3.4. Spectator Distribution Summaries](./ch12/index.md#12.3.4) 
## [12.4. Metrics Collection: Servo](./ch12/index.md#12.4) 
### [12.4.1. Creating Servo Monitors](./ch12/index.md#12.4.1) 
## [12.5. Metrics Backend: Atlas](./ch12/index.md#12.5) 
### [12.5.1. Global tags](./ch12/index.md#12.5.1) 
### [12.5.2. Using Atlas](./ch12/index.md#12.5.2) 
## [12.6. Retrying Failed Requests](./ch12/index.md#12.6) 
### [12.6.1. BackOff Policies](./ch12/index.md#12.6.1) 
### [12.6.2. Configuration](./ch12/index.md#12.6.2) 
### [12.6.3. Zuul](./ch12/index.md#12.6.3) 

# [13. HTTP Clients](./ch13/index.md#13) 