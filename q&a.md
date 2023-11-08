# Summary od DevOps subjects 


## Table of Contents

- [AWS_VPC ](#AWS_VPC )
- [aws-load-balancer-controller](#aws-load-balancer-controller)
- [Kubernetes Ingress Controllers](#Kubernetes Ingress Controllers)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [System Design ](#System_Design)
- [Docker_images_reducing_size](#Docker_images_reducing_size)
- [Configuration](#configuration)
- [Contributing](#contributing)

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

## Kubernetes Ingress Controllers

https://docs.google.com/spreadsheets/d/191WWNpjJ2za6-nbG4ZoUMXMpUK8KlCIosvQB0f-oq3k/edit#gid=907731238


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


## Docker_images_reducing_size 

What ways are there to reduce container images size?

Reduce number of instructions - in some case you may be able to join layers by installing multiple packages with one instructions for example or using && to concatenate RUN instructions
Using smaller images - in some cases you might be using images that contain more than what is needed for your application to run. It is good to get overview of some images and see whether you can use smaller images that you are usually using.
Cleanup after running commands - some commands, like packages installation, create some metadata or cache that you might not need for running the application. It's important to clean up after such commands to reduce the image size
For Docker images, you can use multi-stage builds






