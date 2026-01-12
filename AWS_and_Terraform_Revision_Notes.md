# AWS and Terraform – Class Revision Notes  
**Date:** 12 January 2026

These notes summarize the concepts discussed in the class related to AWS networking fundamentals and Terraform usage, based on the live session.

In AWS, a subnet represents a range of IP addresses within a Virtual Private Cloud (VPC). Subnets are broadly classified into public and private subnets. Private subnets are not directly reachable from the internet because they are not associated with an internet gateway. Public subnets, on the other hand, are connected to an internet gateway and can host resources that need direct internet access.

Terraform handles resource creation order through implicit dependencies. When one resource references another resource in its configuration, Terraform automatically understands the dependency and ensures that resources are created in the correct sequence without explicit instructions.

A Virtual Private Cloud (VPC) is a logically isolated virtual network created within an AWS account. When defining a VPC, a CIDR block is specified to determine the IP address range and overall network size. CIDR notation allows flexible allocation of IP ranges for network design. Routing tables are used within a VPC to control how traffic is directed, based on destination IP addresses, between subnets, gateways, and other network components.

Terraform manages infrastructure state using a state file known as `terraform.tfstate`. This file records the current state of all resources managed by Terraform. In team-based environments, using a remote backend for state storage is recommended to avoid conflicts. Common practice includes storing the state file in an AWS S3 bucket and using DynamoDB for state locking to ensure safe concurrent access.

Terraform configurations are commonly organized into multiple files for clarity and maintainability. The `main.tf` file usually contains core configuration and provider definitions. Network-related resources such as VPCs, subnets, and gateways are often defined in `network.tf`. Compute-related resources, including EC2 instances and security groups, are typically placed in `compute.tf`.

AWS resources use different types of IP addresses. Private IP addresses are assigned to resources within a VPC and are only reachable internally. Public IP addresses allow resources to be accessed from outside the AWS network. Elastic IPs are static public IP addresses allocated to an AWS account and can be reassigned between resources as needed.

When launching an EC2 instance, an Amazon Machine Image (AMI) is mandatory. AMIs define the operating system and base configuration required to create an instance. AWS provides a variety of AMIs to support different operating systems and use cases.

Terraform supports variable management to make configurations flexible and reusable. Input variables allow values to be customized without changing configuration files. Output variables are used to display key information about created infrastructure. Local variables are limited in scope and help simplify expressions within a configuration file.

These concepts collectively form the foundation for designing, provisioning, and managing AWS infrastructure using Terraform, enabling structured, scalable, and maintainable cloud environments.
