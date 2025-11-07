# Docker Basics and Containerization  
**Date:** 7 November 2025

Docker is a platform used to build, package, and run applications inside containers. It allows developers to bundle an application together with all its dependencies into a single standardized unit called a container, ensuring consistency across different environments.

A key idea behind Docker is the philosophy: **“If it fits, it ships.”** This means that once an application is successfully packaged into a Docker container, it can run on any system that supports Docker, without worrying about environment-specific issues.

Docker is built around several core concepts that enable containerized application management.

Containers are lightweight, portable, and self-contained execution units that include application code, runtime, libraries, system tools, and configuration. Unlike virtual machines, containers share the host operating system’s kernel while remaining isolated from each other, making them faster and more resource-efficient.

Docker images are read-only templates used to create containers. An image contains everything required to run an application and serves as the base from which containers are instantiated.

Docker operates using two main components: the Docker daemon and the Docker client. The Docker daemon runs in the background on the host system and is responsible for creating, running, and managing Docker objects such as containers, images, networks, and volumes. The Docker client is a command-line interface that users interact with to send instructions to the daemon. The client can communicate with a local or remote daemon.

Docker supports persistent storage through volumes. Volumes allow data to be stored outside a container’s lifecycle, ensuring that important data is not lost when containers are stopped or removed. Docker also provides built-in networking features that allow containers to communicate with each other as well as with external systems.

Containers are started using the `docker run` command, which creates and launches a container from a specified image. Containers can be run interactively using flags such as `-i` and `-t`, allowing users to access a shell inside the container for direct interaction.

Docker Hub is a cloud-based image registry that acts as the default repository for Docker images. It allows users to pull pre-built images or push their own images for sharing and reuse.

During the class session, hands-on exercises were conducted using Cloud Shell. These exercises focused on creating containers, running Docker commands, and deploying images to gain practical experience with Docker workflows.

Although Docker is used less directly in large-scale production environments due to the rise of container orchestration tools like Kubernetes, it remains a fundamental technology for understanding containerization. Docker provides the conceptual and practical foundation required to work with modern container-based systems.
