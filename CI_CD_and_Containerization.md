# Software Engineering – CI/CD & Containerization Notes  
**Date:** 31 October 2025

---

## Introduction to CI/CD

### What Does CI/CD Mean?
CI/CD stands for **Continuous Integration** and **Continuous Deployment**. It is a core practice in modern software engineering that focuses on automating the process of building, testing, and deploying applications. The main objective is to integrate code changes frequently and deliver updates quickly with minimal manual effort.

---

## Continuous Integration (CI)

### CI Workflow Overview
Whenever a developer pushes code to a shared repository, an automated CI pipeline is triggered. This pipeline validates the code and ensures it meets quality and security standards before moving forward.

### Common CI Pipeline Stages

1. **Linting**  
   Code is analyzed for syntax errors, formatting issues, and style violations. Although sometimes skipped in practice, linting is highly recommended to catch basic issues early.

2. **Build Process**  
   Required dependencies are downloaded and the application is compiled or packaged. In some setups, unit tests may also run during this phase.

3. **Unit Testing**  
   Individual components or functions of the application are tested in isolation.  
   To test code that depends on external services, developers often use **mocking**, which simulates external behavior without making real calls.

4. **Security and Compliance Checks**  
   - **SCA (Software Composition Analysis):** Identifies risks in third-party and open-source libraries.  
   - **SAST (Static Application Security Testing):** Scans source code to detect potential security vulnerabilities.

---

## Build Artifacts in CI

Artifacts are the outputs generated after a successful build. These are used for testing and deployment.

Examples include:
- JAR / WAR files (Java)
- Executables (`.exe`)
- Gems
- Docker images

Artifacts are versioned and stored so that the same build can be deployed consistently across environments.

---

## Containers and Docker Basics

### Dockerization
Dockerization refers to packaging an application along with its dependencies into a container.  
A **Docker image** is a static, immutable artifact that can be deployed across different environments without changes.

### Docker Image Creation
Docker images are created by:
- Starting from a **base image**
- Adding application-specific layers on top  
Each layer is cached, which improves build speed when rebuilding images.

---

### Storing Docker Images
Once built, Docker images are pushed to an **artifact repository**. This allows teams to:
- Track versions
- Reuse images
- Deploy the same image across multiple environments

---

## Continuous Deployment (CD)

### Deployment Pipeline
Continuous Deployment begins after CI completes successfully. Deployment may occur as:
- A separate pipeline, or  
- A continuation of the CI workflow  

The pipeline pulls artifacts from the artifact repository and deploys them to target environments.

---

### System Integration Testing (SIT)
SIT is typically the first deployment environment.  
Here, the application is tested as a complete system to verify that it interacts correctly with other services and components, rather than testing individual modules in isolation.

---

## Networking Concepts in Deployment

### Public IP Addresses
Public IPs are assigned dynamically and may change when a virtual machine or instance is stopped and restarted.

### Elastic IP Addresses
Elastic IPs remain fixed regardless of instance restarts.  
They are especially useful in production systems where a stable endpoint is required for clients or external integrations.

---

## Summary

- **CI/CD** automates code integration, testing, and deployment, improving speed and reliability.
- **Artifacts** act as deployable build outputs that ensure consistency across environments.
- **Docker and containers** provide portability and lightweight execution environments.
- **Elastic IPs** help maintain stable access points for frequently redeployed applications.

A well-designed CI/CD pipeline combined with containerization forms the backbone of efficient, modern software delivery.
