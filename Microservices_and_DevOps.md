# Revision Notes: Microservices & DevOps  
**Date:** 27 October 2025

---

## Introduction to Microservices

### What Are Microservices?
Microservices represent an architectural approach where an application is built as a set of small, independent services. Each service focuses on a specific business capability and communicates with others using lightweight protocols.

Unlike traditional monolithic systems—where the entire application is tightly coupled and deployed as a single unit—microservices divide functionality into self-contained services that can be developed, deployed, and maintained independently.

---

### Advantages of Microservices

- **Scalability**  
  Individual services can be scaled based on demand, allowing better resource utilization compared to scaling an entire application.

- **Technology Flexibility**  
  Teams can choose different programming languages, frameworks, or databases for different services, depending on what best fits the problem.

- **Independent Deployment**  
  Updates or fixes can be rolled out for a single service without impacting the entire system, enabling faster and safer releases.

---

## Core Concepts in Microservices

### REST-Based Communication
Microservices commonly interact using REST APIs over HTTP or HTTPS. This approach enables interoperability between services regardless of the programming language or platform used.

---

### Stateless Design
Microservices are designed to be stateless, meaning they do not store session or application state internally. Any required state is maintained in external data stores, making services easier to replicate, scale, and recover.

---

### Externalized Logging
Since microservices are distributed and independently running, logs are stored and managed externally. Centralized logging tools help track system behavior and debug failures across services.

Common tools include:
- Fluentd  
- ELK Stack (Elasticsearch, Logstash, Kibana)  
- Splunk  

---

### Load Balancing and DNS

- **Load Balancer**  
  A load balancer distributes incoming requests across multiple service instances, improving reliability, performance, and fault tolerance.

- **DNS (Domain Name System)**  
  DNS maps human-readable domain names to IP addresses, making service discovery and communication easier within distributed systems.

---

## Introduction to DevOps

### Why DevOps Matters
DevOps is a culture and set of practices that combine software development and IT operations. Its primary goal is to shorten development cycles while ensuring reliable, high-quality software delivery.

---

### CI/CD: Continuous Integration and Continuous Deployment

- **Continuous Integration (CI)**  
  Developers frequently merge code changes into a shared repository, where automated tests validate the changes.

- **Continuous Deployment (CD)**  
  Successfully tested code is automatically deployed to production environments, reducing manual intervention and deployment errors.

A complete CI/CD pipeline plays a critical role in achieving faster and more consistent software releases.

---

## Upcoming Topics

- **Docker** – Containerization of applications for consistent environments  
- **Kubernetes** – Orchestration of containerized applications for scalability and reliability  

These tools form the backbone of modern DevOps workflows.

---

## Class Structure and Participation

- Regular submission of notes on GitHub is encouraged to build consistency and discipline.
- Hands-on labs and practical sessions will complement theory to strengthen real-world understanding.
- Assignments and active participation contribute to overall assessment.

---

## Summary
Microservices enable scalable, flexible, and resilient application architectures, while DevOps practices ensure rapid and reliable delivery. Together, they form the foundation of modern software systems and are essential concepts for building production-ready applications.
