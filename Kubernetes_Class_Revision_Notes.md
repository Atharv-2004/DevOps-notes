# Kubernetes Class – Comprehensive Revision Notes  
**Date:** 1 December 2025

These notes summarize a Kubernetes class focused on understanding cluster setup and core architectural concepts through practical demonstrations.

The class began with a demonstration of setting up a Kubernetes cluster using three machines. One machine was configured as the master node, while the remaining machines acted as worker nodes. The master node is responsible for control plane operations, whereas worker nodes are responsible for running application workloads assigned by the cluster.

For the master node setup, the instructor had completed some prerequisite installations before the session. A shell script was used to install required components, followed by switching to the root user using `sudo su`. The master node was initialized using the `kubectl init` command, which is part of `kubeadm`. This initialization process automatically downloads and configures essential Kubernetes components such as etcd, the API server, the controller manager, and the scheduler using predefined YAML manifests.

The concept of pods was then introduced. A pod is the smallest deployable unit in Kubernetes and can contain one or more containers. Containers within a pod are co-located, meaning they share the same network namespace and resource environment. They are also co-scheduled, which ensures that all containers within a pod are always placed on the same node.

The architecture of Kubernetes was explained by dividing it into the control plane and the data plane. The control plane includes components such as the API server, etcd (which stores configuration and cluster state data), the controller, and the scheduler. The data plane consists of components that run application workloads and execute tasks assigned by the control plane.

Interaction with the Kubernetes cluster is performed using `kubectl`, which communicates with the API server using REST-based calls or similar mechanisms. The API server is responsible for handling authentication, authorization, and request validation before persisting or retrieving data from etcd.

During the hands-on portion of the class, the instructor demonstrated how to create and manage pods using `kubectl` commands. Basic commands such as `kubectl get pod` were highlighted as essential for monitoring pod status and verifying successful deployments.

Namespaces were introduced as a way to logically isolate and organize resources within a Kubernetes cluster. Default namespaces such as `default` and `kube-system` were discussed as part of the cluster’s standard setup.

Networking concepts were also covered. CoreDNS was explained as the component responsible for internal DNS resolution within the cluster. Proper network plugin installation, such as Weave, is required to ensure networking and DNS functionality. It was also discussed that pod scheduling and resource allocation depend on available CPU and memory resources on worker nodes.

The class concluded by emphasizing that although Kubernetes architecture and concepts can appear complex initially, understanding pods, cluster components, and basic operations is critical. These fundamentals form the backbone of deploying and managing modern microservices-based applications using Kubernetes.
