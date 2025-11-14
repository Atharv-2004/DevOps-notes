# Revision Notes on Docker and Container Technology  
**Date:** 14 November 2025

Containers are a core technology in modern software engineering that allow applications to be packaged together with their dependencies into a single standardized unit. They are widely adopted because they provide isolated yet consistent environments for development, testing, and deployment while running on a shared operating system.

The idea of isolation in computing predates Docker. One of the earliest examples is the Unix `chroot` command, introduced in the late 1960s and early 1970s. The `chroot` mechanism creates a restricted file system environment, often referred to as a “jail,” where processes operate as if they are in a separate system while still sharing the same kernel.

A Docker container is a lightweight, standalone executable unit that includes application code, runtime, libraries, and required system tools. Unlike virtual machines, containers do not bundle a full operating system. Instead, they rely on the host system’s kernel, which makes them faster to start and more resource-efficient.

When comparing containers to virtual machines, containers are significantly lighter in terms of resource usage and startup time. Virtual machines rely on hypervisors and include a complete operating system for each instance, whereas containers share the host OS. Both approaches provide isolation, but container isolation is achieved using Linux namespaces and control groups rather than hardware-level virtualization.

Containers operate through two key Linux kernel features. Namespaces isolate system resources such as process IDs, hostnames, networking, user identities, inter-process communication, and file systems. Control groups, also known as cgroups, manage and limit the allocation of system resources like CPU and memory, ensuring that containers do not interfere with each other.

Docker interacts directly with the Linux kernel to manage containers. On Linux systems, Docker runs natively and uses the host kernel without requiring an additional abstraction layer. On Windows and macOS, Docker relies on a lightweight Linux-based virtual machine because these operating systems do not natively support the Linux kernel features required for containerization.

Container behavior varies across operating systems. On Linux, containers execute directly on the host kernel. On Windows and macOS, container execution depends on a virtualized Linux environment to provide the necessary kernel capabilities.

Docker containers are designed to be ephemeral, meaning they can be created, stopped, and removed easily without long-term impact on the system. This transient nature supports scalability and fault tolerance, but it also means applications should be stateless or rely on external storage mechanisms for data persistence.

Containers operate with isolated networking by default. To enable communication between a container and the host system or external services, ports must be explicitly mapped. Port mapping allows controlled access while preserving isolation, which is essential in networked and multi-container environments.

Overall, Docker and container technology mark a major shift in how applications are developed and deployed. By enabling portability, scalability, and efficient resource usage, containers provide a powerful foundation for modern software systems and deployment pipelines.
