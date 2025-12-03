# Revision Notes on Kubernetes Pods and ReplicaSets  
**Date:** 3 December 2025

In Kubernetes, most configuration files are written in YAML and follow a common structure. Each YAML file typically contains four essential fields. The `apiVersion` specifies which version of the Kubernetes API is being used, allowing backward compatibility and feature evolution. The `kind` field defines the type of Kubernetes object being created, such as a Pod, ReplicaSet, or Deployment. The `metadata` section stores identifying information about the object, including its name, which is often mandatory. The `spec` section describes the desired state of the object and varies depending on the resource type.

A Pod is the smallest deployable unit in Kubernetes and consists of one or more containers. All containers within a Pod share the same network namespace and resources and are always scheduled together on the same node. If a container inside a Pod crashes, Kubernetes automatically replaces it without requiring manual intervention, ensuring continuous operation.

Kubernetes YAML supports three basic data structures. A key-value pair follows the format `key: value`. A list is defined using a dash (`-`) before each item. A map is a nested structure containing key-value pairs, which can further include lists or other maps.

A ReplicaSet is used to ensure that a specified number of identical Pod replicas are running at all times. If a Pod fails or a node becomes unavailable, the ReplicaSet automatically creates new Pods to maintain the desired replica count. This provides fault tolerance and availability for applications.

In a ReplicaSet YAML configuration, the `kind` is set to `ReplicaSet`. The number of desired Pod replicas is defined using the `replicas` field. A selector is required to match the labels of the Pods that the ReplicaSet manages. Labels act as identifiers that allow Kubernetes to group and manage Pods collectively, similar to tagging mechanisms in cloud platforms.

Several Kubernetes components work together internally to manage Pods and ReplicaSets. The kubelet runs on each node and is responsible for managing Pods and reporting node status to the API server. The API server handles authentication, authorization, request validation, and communication with the etcd datastore. Controllers continuously monitor the cluster state and trigger corrective actions when the actual state differs from the desired state. The scheduler assigns Pods to appropriate nodes based on resource availability and scheduling constraints.

When failures occur, the ReplicaSet controller monitors the system and ensures that the desired number of Pods is maintained. If a Pod crashes or is terminated, the controller detects the mismatch between the desired and current state and instructs the API server to create a replacement Pod.

Common `kubectl` commands used to manage Kubernetes resources include `kubectl apply -f <file>` to create or update resources, `kubectl delete -f <file>` to remove resources, and `kubectl get <resource>` to list and inspect existing objects.

These notes summarize the core concepts related to Kubernetes Pods and ReplicaSets discussed in the class and provide a foundation for managing applications effectively in a Kubernetes environment.
