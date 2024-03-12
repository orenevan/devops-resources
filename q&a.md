# Summary of DevOps subjects 


## Table of Contents

- [DevOps exercises  ](#DevOps_exercises  )
- [AWS_VPC ](#AWS_VPC )
- [aws-load-balancer-controller](#aws-load-balancer-controller)
- [Kubernetes Ingress Controllers](#Kubernetes Ingress Controllers)
  _ [k8_Deployments_Strategies](#k8_Deployments_Strategies)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [System Design ](#System_Design)
   - [horizontal-vs-vertical-scaling](#horizontal-vs-vertical-scaling)
   - [development-and-deployment-of-massively-multiplayer-games-from-social-games](#development-and-deployment-of-massively-multiplayer-games-from-social-games)
   - [message-queues] (#message-queues)
- [api]#api 
- [Docker_images_reducing_size](#Docker_images_reducing_size)
  - [Docker_file_security](#Docker_files_security)
- [Configuration](#configuration)
- [Contributing](#contributing)

## DevOps_exercises 
https://github.com/bregman-arie/devops-exercises

## AWS_VPC 


VPCs on AWS generally consist of a CIDR with multiple subnets. AWS allows one internet gateway (IG) per VPC, which is used to route traffic to and from the internet. The subnet with the IG is considered the public subnet and all others are considered private.

The components needed to create a VPC on AWS are described below:

The creation of an empty VPC resource with an associated CIDR.
A public subnet in which components will be accessible from the internet. This subnet requires an associated IG.
A private subnet that can access the internet through a NAT gateway. The NAT gateway is positioned inside the public subnet.
A route table for each subnet.
Two routes: One routing traffic through the IG and one routing through the NAT gateway, assigned to their respective route tables.
The route tables are then associated to their respective subnets.
A security group then controls which inbound and outbound traffic is allowed.
This methodology is conceptually similar to physical infrastructure.

## aws-load-balancer-controller

https://kubernetes-sigs.github.io/aws-load-balancer-controller/v2.5/how-it-works/

## K8 

### Kubernetes Ingress Controllers

https://docs.google.com/spreadsheets/d/191WWNpjJ2za6-nbG4ZoUMXMpUK8KlCIosvQB0f-oq3k/edit#gid=907731238

### k8_Deployments_Strategies 

https://spot.io/resources/kubernetes-autoscaling/5-kubernetes-deployment-strategies-roll-out-like-the-pros/

Rolling deployment—the default strategy that allows you to update a set of pods without downtime. It replaces pods running the old version of the application with the new version, one by one.
Recreate deployment—an all-or-nothing method that lets you update an application instantly, with some downtime. It terminates all pods and replaces them with the new version.
Ramped slow rollout—rolls out replicas of the new version, while in parallel, shutting down old replicas. 
Best-effort controlled rollout—specifies a “max unavailable” parameter which indicates what percentage of existing pods can be unavailable during the upgrade, enabling the rollout to happen much more quickly.
Blue/green deployment—a deployment strategy in which you create two separate, but identical environments, and over to the new environment.
Canary deployment—uses a progressive delivery approach, with one version of the application serving most users, and another, newer version serving a small pool of test users. The test deployment is rolled out to more users if it is successful.
Shadow deployment—the new version of the application (the “shadow” version) receives real-world traffic alongside the current version, but without affecting end-users.
A/B testing—rolls out two or more versions of an application feature to a subset of users simultaneously to see which one performs better in terms of user engagement, error rates, or other KPIs.


## System_Design 

https://blog.sqlizer.io/posts/facebook-on-aws/ 
https://www.educative.io/blog/complete-guide-to-system-design


Here are some reasons why learning system design is valuable for DevOps engineers:

1. Infrastructure as Code (IaC): System design involves architecting infrastructure and applications using IaC tools like Terraform, CloudFormation, or Ansible. Understanding system design principles helps you design infrastructure that is scalable, maintainable, and version-controlled.

2. Scalability and Performance: DevOps engineers are often responsible for managing systems that need to handle high traffic and scale dynamically. System design knowledge equips you with the ability to design horizontally scalable architectures, implement load balancing, optimize database performance, and make efficient use of caching mechanisms.

3. High Availability and Resilience: DevOps engineers play a critical role in ensuring high availability and resilience of systems. Learning system design helps you understand concepts like redundancy, fault tolerance, disaster recovery, and distributed systems, allowing you to design robust architectures that minimize downtime and quickly recover from failures.

4. Microservices and Containerization: As a DevOps engineer, you may work with microservices architecture and containerization technologies like Docker and Kubernetes. System design knowledge helps you design container orchestration strategies, network configurations, and microservices interactions to ensure seamless deployment, management, and scalability.

5. Security and Compliance: System design encompasses security and compliance considerations. Understanding system design principles allows you to incorporate security measures, such as access controls, encryption, and monitoring, into your infrastructure and applications. It helps you design systems that comply with industry standards and regulations.

6. Collaboration with Development Teams: System design knowledge allows you to effectively collaborate with development teams, understand their architectural requirements, and provide input on the infrastructure and deployment aspects of their applications. It helps bridge the gap between development and operations, enabling smoother integration and continuous delivery practices.

To learn system design as a DevOps engineer, consider exploring resources such as books, online courses,
blog articles, and real-world case studies. Engage in practical projects or contribute to open-source projects to gain hands-on experience. Additionally, seek opportunities to collaborate with software architects or engineers who have expertise in system design to learn from their experiences and insights.

### horizontal-vs-vertical-scaling

https://www.instaclustr.com/blog/horizontal-vs-vertical-scaling-which-scaling-strategy-is-right-for-me/?_bt=&_bk=&_bm=&_bn=x&_bg=&utm_term=&utm_campaign=&utm_source=adwords&utm_medium=ppc&hsa_acc=1467100120&hsa_cam=20784980828&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gad_source=1&gclid=Cj0KCQiAkeSsBhDUARIsAK3tief3g6A7A08pg1ihv3wbBKz4lPKRdTY6T1c80flZjDdP_UylG4qUEQUaAryHEALw_wcB

### development-and-deployment-of-massively-multiplayer-games-from-social-games

http://ithare.com/contents-of-development-and-deployment-of-massively-multiplayer-games-from-social-games-to-mmofps-with-stock-exchanges-in-between/

### message-queues
https://memphis-dev.medium.com/comparing-nats-and-kafka-understanding-the-differences-f08c4479dea6

https://www.educative.io/courses/web-application-software-architecture-101

## api 
🌟 𝐓𝐨𝐩 𝟔 𝐌𝐨𝐬𝐭 𝐏𝐨𝐩𝐮𝐥𝐚𝐫 𝐀𝐏𝐈 𝐀𝐫𝐜𝐡𝐢𝐭𝐞𝐜𝐭𝐮𝐫𝐞 𝐒𝐭𝐲𝐥𝐞𝐬 🌟


1️⃣ SOAP (Simple Object Access Protocol):
✨ Designed for exchanging structured information in web services
✨ Uses XML for message format and HTTP for transport
✨ Supports various protocols such as SMTP, HTTP, and more
✨ Offers extensive built-in error handling and security features
✨ Provides a standard way to define and describe APIs with WSDL (Web Services Description Language)

2️⃣ RESTful (Representational State Transfer):
✨ Based on a set of architectural principles for building scalable web services
✨ Utilizes HTTP methods like GET, POST, PUT, DELETE to perform operations on resources
✨ Employs lightweight data formats like JSON or XML for data exchange
✨ Emphasizes stateless communication between client and server
✨ Known for its simplicity, flexibility, and compatibility with various programming languages and platforms

3️⃣ GraphQL:
✨ Developed by Facebook, GraphQL is a query language for APIs and a runtime for executing queries
✨ Enables clients to request only the specific data they need, reducing network overhead
✨ Offers a hierarchical approach to querying data, allowing complex data retrieval in a single request
✨ Provides a strongly typed schema, making it easier to understand and evolve APIs
✨ Supports real-time updates through subscriptions, enabling reactive and interactive applications

4️⃣ gRPC (Google Remote Procedure Call):
✨ A high-performance, open-source framework developed by Google
✨ Enables communication between distributed systems using remote procedure calls
✨ Uses Protocol Buffers (protobuf) as the interface definition language for efficient data serialization
✨ Supports multiple programming languages and platforms, including Java, C++, Python, and more
✨ Provides features like bidirectional streaming, flow control, and authentication, making it ideal for microservices architectures

5️⃣ WebSocket:
✨ Offers full-duplex communication between client and server over a single, long-lived connection
✨ Allows real-time, event-driven communication, suitable for applications requiring frequent data updates
✨ Provides low latency and high throughput compared to traditional HTTP-based approaches
✨ Supports two-way communication, enabling server-initiated updates
✨ Widely used in chat applications, collaborative tools, and real-time dashboards

6️⃣ Webhook:
✨ A mechanism that allows applications to receive real-time notifications or data updates
✨ Involves setting up HTTP callbacks, where the server sends data to a predefined URL endpoint
✨ Enables event-driven architecture, triggering actions based on specific events or changes
✨ Provides flexibility by allowing developers to define custom endpoints and payloads
✨ Widely used for integrating third-party services, automating workflows, and building event-driven systems


## Docker_images_reducing_size 

```
What ways are there to reduce container images size?

Reduce number of instructions - in some case you may be able to join layers by installing multiple packages with one instructions for example or using && to concatenate RUN instructions
Using smaller images - in some cases you might be using images that contain more than what is needed for your application to run. It is good to get overview of some images and see whether you can use smaller images that you are usually using.
Cleanup after running commands - some commands, like packages installation, create some metadata or cache that you might not need for running the application. It's important to clean up after such commands to reduce the image size
For Docker images, you can use multi-stage builds
```



## Docker_files_security
  https://medium.com/@marcong_54227/how-to-write-a-production-ready-dockerfile-58d18d4daddc
  
  https://infosecwriteups.com/top-10-dockerfile-security-best-practices-for-a-more-secure-container-e5426f69738b

### Non root user 

``` 
Running as non-root use
FROM mcr.microsoft.com/dotnet/aspnet:5.0
//Create group app and user app
 RUN addgroup --gid 1000 -S app && adduser --uid 1000 -S app -G app
 // Set permissions for app user for the WORKDIR    
 RUN chown -R app:app App/
 // Switch to the created user
 USER app
 COPY bin/Release/netcoreapp3.1/publish/ App/
 WORKDIR /App
 ENTRYPOINT ["dotnet", "aspnetapp.dll"]
```


 


 




