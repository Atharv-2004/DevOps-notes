# Docker Networking – Revision Notes  
**Date:** 19 November 2025

Docker networking enables communication between containers and between containers and external systems. It plays a vital role in running distributed and networked applications inside Docker environments.

Each container in Docker is assigned an IP address that uniquely identifies it within a Docker network. These IP addresses allow containers to send and receive data just like devices on a traditional network.

Subnetting is used to divide a larger network into smaller logical networks. Docker networking follows CIDR notation to define subnets. In CIDR, part of the IP address represents the network and the remaining bits represent hosts. For example, a network defined as 192.168.10.0/24 provides 256 total IP addresses because 8 bits are available for host allocation.

Within every subnet, two IP addresses are reserved. The first address is the Network ID, which represents the network itself and cannot be assigned to a device. The last address is the Broadcast ID, which is used to send data to all devices within the subnet.

When Docker is installed, it automatically creates a virtual bridge network known as docker0, also referred to as Docker Zero. This bridge acts like a virtual network switch. Each container is assigned an eth0 network interface, which connects to the docker0 bridge through a virtual Ethernet pair, enabling communication between containers and with external networks.

By default, containers run inside the docker0 bridge network. Containers within the same bridge network can communicate with each other using their assigned IP addresses. Docker also allows containers to be started within custom networks, providing better isolation and control over networking behavior.

Custom bridge networks can be created using Docker networking commands. These networks allow users to define specific subnets and gateways, enabling finer control over traffic flow and container communication. Docker internally manages routing and connectivity between containers attached to the same network.

A practical networking scenario involves dividing a larger network into multiple subnets for different teams or services. For example, a single network can be split into separate subnets for engineering, HR, and reception by assigning each group a different CIDR range. This improves organization, isolation, and network management.

Troubleshooting Docker networking often requires inspecting container network configurations. The `docker inspect` command provides detailed information about container networking, including IP addresses, gateways, and connected networks.

Overall, Docker networking abstracts complex networking concepts and simplifies container communication. Understanding bridges, IP addressing, subnets, and custom networks is essential for building scalable and well-structured containerized applications.
