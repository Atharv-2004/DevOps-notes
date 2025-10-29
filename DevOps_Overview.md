# DevOps Class Revision Notes  
**Date:** 29 October 2025

---

## Overview of DevOps

### What Is DevOps?
DevOps is a combination of practices, cultural values, and supporting tools that bring together software development and IT operations. Its purpose is to enable faster, more reliable delivery of applications and services by improving collaboration and automation across teams.

These three pillars—**culture**, **processes**, and **tools**—work together to enhance product quality and operational stability.

---

## Challenges in Adopting DevOps

One of the biggest hurdles in DevOps adoption is cultural change. Shifting long-standing workflows, mindsets, and approval processes can be difficult, especially in organizations with rigid or traditional development practices. Gaining team buy-in and managing change effectively is often more challenging than implementing the tools themselves.

---

## Key DevOps Concepts

### DevOps Philosophy
DevOps applies shared principles to unify development (Dev) and operations (Ops), ensuring both teams work toward a common goal: faster and more reliable software delivery.

---

### Shift-Left Approach
The shift-left strategy focuses on moving testing, validation, and quality checks earlier in the software development lifecycle. By identifying issues sooner, teams can reduce defects, lower costs, and improve overall system stability.

---

## Security Testing in DevOps

### Common Types of Security Testing

- **Static Application Security Testing (SAST)**  
  Examines source code to identify security vulnerabilities without running the application.

- **Dynamic Application Security Testing (DAST)**  
  Tests a running application to uncover security flaws during execution.

- **Software Composition Analysis (SCA)**  
  Scans third-party and open-source libraries used in the application to detect known vulnerabilities and license risks.

---

### Example: Code-Level Vulnerability
A typical security issue is **SQL injection**, which can occur when user input is directly included in database queries. In Java, using `Statement` objects can expose applications to such attacks if inputs are not sanitized.  
Using `PreparedStatement` helps prevent SQL injection by safely handling input parameters.

---

## Continuous Integration (CI)

### CI Workflow Steps

Continuous Integration ensures that code changes are regularly tested and validated through the following steps:

1. **Code Checkout** – Fetching the latest version of the code from the repository  
2. **Dependency Installation** – Installing required libraries and packages  
3. **Linting** – Enforcing code quality and style standards  
4. **Build Process** – Compiling and packaging the application  
5. **Testing** – Running automated unit tests  
6. **Security Scans** – Executing SAST and SCA tools  
7. **Artifact Creation** – Generating deployable outputs such as binaries or container images  
8. **Staging Deployment** – Deploying to a non-production environment for validation  

---

## Continuous Deployment (CD)

Once the CI pipeline completes successfully, Continuous Deployment takes over. CD automates the release of code changes to production environments with minimal manual intervention. Human approval is only required when predefined thresholds or failure conditions are triggered.

The objective is to maintain a smooth, repeatable, and reliable deployment pipeline.

---

## Communication and Coordination in DevOps

### API Gateway in Microservices
An API Gateway acts as a single entry point for client requests in a microservices architecture. It routes requests to appropriate services and often manages responsibilities such as authentication, authorization, and rate limiting.

---

### Inter-Service Communication
Microservices communicate using two primary methods:

- **Synchronous Communication** – Real-time, blocking requests  
- **Asynchronous Communication** – Non-blocking messaging using brokers like RabbitMQ or Kafka  

The choice depends on performance, reliability, and system design requirements.

---

## Conclusion
DevOps promotes a collaborative culture that aligns development and operations teams through automation, shared responsibility, and continuous improvement. By adopting DevOps practices, organizations can im
