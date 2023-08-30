# Summary od DevOps subjects 


## Table of Contents

- [AWS_VPC ](#AWS_VPC )
- [aws-load-balancer-controller](#aws-load-balancer-controller)
- [Kubernetes Ingress Controllers](#Kubernetes Ingress Controllers)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
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

# Kubernetes Ingress Controllers

https://docs.google.com/spreadsheets/d/191WWNpjJ2za6-nbG4ZoUMXMpUK8KlCIosvQB0f-oq3k/edit#gid=907731238
