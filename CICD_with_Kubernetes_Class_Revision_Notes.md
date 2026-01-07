# CI/CD with Kubernetes – Class Revision Notes  
**Date:** 7 January 2026

This class focused on deploying applications to a Kubernetes cluster using Continuous Integration (CI) and Continuous Deployment (CD), highlighting their importance in modern DevOps workflows.

Continuous Integration (CI) refers to the automated process of integrating code changes from multiple developers into a shared codebase. The goal of CI is to enable frequent code merges, run automated tests, and ensure that the main branch of the application remains stable and ready for deployment at all times.

Continuous Deployment (CD) extends the CI process by automating the release of validated code into target environments, including production. CD involves configuring infrastructure and deployment mechanisms so that application updates can be delivered reliably and without service disruption.

The class included guidance on setting up a Kubernetes environment. At minimum, a single-node Kubernetes cluster is required. Virtual machines can be created using tools such as VirtualBox and Vagrant, where Vagrant scripts simplify environment provisioning by automating configuration steps. As an alternative, preconfigured virtual machine images, such as cloud images with Kubernetes already installed, can be used to reduce setup effort.

GitHub Actions was introduced as the primary CI/CD automation tool. It enables workflows to be defined directly within a GitHub repository for building, testing, packaging, and deploying applications. In addition to GitHub-hosted runners, the class covered the use of custom or self-hosted runners. These runners are typically set up on Linux machines and registered with GitHub using configuration scripts. Once registered, they can be labeled and secured according to project requirements and used to execute workflows.

A project-based demonstration formed a key part of the class. Teams collaborated to implement CI/CD pipelines for their applications using GitHub Actions and Kubernetes. Although work was done collaboratively, individual understanding and contribution were emphasized, particularly during project reviews and presentations.

Testing and quality assurance were discussed as integral parts of the CI/CD pipeline. Structured testing stages such as System Integration Testing (SIT), performance testing, and security testing were highlighted. Automation of these testing phases helps reduce manual errors and ensures consistent and thorough validation of application behavior.

Practical considerations were also addressed. In well-designed systems, CI and CD are often maintained as separate processes to preserve clarity and separation of responsibilities. Deployment pipelines may require customization based on application architecture, infrastructure constraints, and operational needs.

Overall, the class provided a comprehensive overview of implementing CI/CD pipelines with Kubernetes, emphasizing automation, testing, collaboration, and practical deployment strategies in real-world environments.
