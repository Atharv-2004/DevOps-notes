# Revision Notes: Terraform and Infrastructure as Code  
**Date:** 9 January 2026

Terraform is an open-source tool used to define, provision, and manage cloud infrastructure using code. It enables teams to automate infrastructure creation and management across multiple cloud providers such as AWS, Azure, and Google Cloud, reducing manual effort and configuration errors.

Terraform is platform-agnostic, meaning it can work with multiple cloud and service providers through a common configuration language. It follows the Infrastructure as Code (IaC) approach, where infrastructure is described declaratively in configuration files, allowing environments to be recreated, versioned, and audited reliably.

Terraform operates through a well-defined lifecycle driven by a small set of core commands. The `terraform init` command initializes the working directory, downloads required provider plugins and modules, and locks compatible provider versions. The `terraform plan` command compares the current infrastructure state with the desired state defined in configuration files and generates an execution plan that previews proposed changes without applying them. The `terraform apply` command executes the planned changes and modifies the infrastructure to match the desired configuration in a controlled manner. The `terraform destroy` command removes all infrastructure resources defined in the configuration, allowing complete cleanup of environments.

Using Terraform offers several advantages. Automation significantly improves speed and efficiency by reducing the time required to provision and update infrastructure. Consistency is achieved by using the same code across environments, minimizing configuration drift. Terraform configurations can be stored in version control systems such as Git, enabling tracking of changes, collaboration, rollbacks, and auditing.

Terraform is often used alongside other tools. Configuration management tools such as Ansible, Puppet, and Chef complement Terraform by handling software installation and configuration on provisioned infrastructure. Server templating and environment tools like Vagrant and Docker help create reproducible development environments and containerized services that run on infrastructure managed by Terraform.

A practical example discussed in class involved creating an EC2 instance using Terraform. Infrastructure resources are defined in `.tf` files, specifying details such as instance type and region. Terraform commands are then used to initialize the environment, review planned changes, and apply them to provision the resources. Terraform’s state management tracks deployed resources, allowing updates and deletions to be handled safely and predictably.

Overall, Terraform provides a structured and reliable approach to infrastructure management. By treating infrastructure as code, it supports automation, consistency, and traceability, making it a key tool in modern DevOps and cloud-based workflows.
