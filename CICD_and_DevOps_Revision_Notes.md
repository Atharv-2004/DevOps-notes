# CI/CD and DevOps – Revision Notes  
**Date:** 17 December 2025

Software development practices have evolved over time, moving from traditional Waterfall models to PLP, then Agile methodologies, and finally to modern CI/CD-based workflows. This evolution reflects the industry’s shift toward faster delivery, continuous feedback, and higher reliability.

A CI/CD pipeline is divided into two major phases: Continuous Integration (CI) and Continuous Deployment or Continuous Delivery (CD).

Continuous Integration focuses on frequently integrating code changes into a shared repository. The CI process typically includes code check-ins, linting to maintain code quality, dependency verification, and security checks such as Software Composition Analysis (SCA) and Static Application Security Testing (SAST). After validation, the code is packaged, unit tested, containerized using Docker, and tested within containers. Image scanning is performed to identify vulnerabilities, and validated artifacts are stored using artifact management systems.

Continuous Deployment or Continuous Delivery handles the post-integration phase. This includes System Integration Testing (SIT), security testing, and performance testing. Depending on application requirements, specialized testing such as NLP validation or A/B testing may also be performed. In Continuous Deployment, changes are automatically pushed to production, while in Continuous Delivery, the application is kept production-ready and released after manual approval.

DevOps emphasizes collaboration between development and operations teams to streamline software delivery and operations. DevSecOps extends this approach by embedding security practices directly into every stage of the CI/CD pipeline, ensuring that security is not treated as a separate or final step.

Several key concepts support CI/CD and DevOps practices. Artifact management systems such as JFrog, Nexus, and ECR are used to store and version build outputs. Feature flagging allows functionality to be enabled or disabled without redeploying code. Iterative development promotes continuous improvement through small, incremental changes. Automation ensures consistency, repeatability, and reduced human error across the pipeline.

Multiple types of testing are integrated into CI/CD workflows, including unit testing, integration testing, performance testing, and security testing. Each type of testing validates a different aspect of application behavior and reliability.

DevOps adoption offers several benefits, including faster release cycles, improved software quality, stronger security posture, higher levels of automation, and consistent environments across development, testing, and production.

A key distinction exists between Continuous Deployment and Continuous Delivery. Continuous Deployment automatically releases every successful change directly to production, whereas Continuous Delivery prepares the application for production and requires manual approval before release.

Overall, CI/CD aims to automate and optimize the software development lifecycle by integrating testing, security, and deployment into a unified pipeline, enabling faster, more reliable, and secure software releases.
