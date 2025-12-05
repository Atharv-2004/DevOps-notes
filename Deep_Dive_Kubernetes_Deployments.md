# Revision Notes: Deep Dive into Kubernetes Deployments  
**Date:** 5 December 2025

This session focused on Kubernetes Deployments, extending earlier discussions on Pods and ReplicaSets. The class highlighted how these components work together to manage, scale, and update containerized applications reliably within a Kubernetes cluster.

Pods are the smallest deployable units in Kubernetes and represent a single running instance of an application process. A pod may contain one or more containers, which are lightweight, fast to start, and encapsulate application code along with its dependencies. Containers bring the benefits of containerization—such as portability and efficiency—into the Kubernetes ecosystem through pods.

ReplicaSets are responsible for maintaining a fixed number of pod replicas at all times. They provide fault tolerance and scalability by continuously monitoring the cluster state. If a pod crashes or the node hosting it fails, the ReplicaSet automatically creates a replacement pod to restore the desired state of the application.

Deployments sit one level above ReplicaSets and provide a higher-level abstraction for application management. A Deployment manages ReplicaSets and enables advanced features such as rolling updates and rollbacks. The deployment controller ensures that changes defined in the desired state are applied gradually and safely, updating pods and ReplicaSets as required.

Kubernetes objects such as Deployments and ReplicaSets are defined using YAML configuration files. These files describe the desired state of the application, including replica count and pod specifications. Deployment YAML files closely resemble ReplicaSet YAML files, with the main difference being the `kind` field, which is set to `Deployment` instead of `ReplicaSet`.

An example of a Deployment YAML configuration is shown below:

```yaml
apiVersion: apps/v1  
kind: Deployment  
metadata:  
  name: nginx-deployment  
spec:  
  replicas: 3  
  template:  
    metadata:  
      labels:  
        app: nginx  
    spec:  
      containers:  
      - name: nginx  
        image: nginx:1.16.1  
```

Deployments simplify scaling and updates. Scaling can be performed easily by increasing or decreasing the number of replicas, either through configuration changes or scaling commands. By default, Deployments use a rolling update strategy, which updates pods incrementally and avoids downtime, ensuring continuous service availability during updates.

Deployments also support upgrade and rollback mechanisms. When a new version of an application is deployed, Kubernetes keeps track of previous ReplicaSets, allowing teams to revert to an earlier version if issues arise. This capability is especially important in CI/CD pipelines where frequent updates are common.

Several best practices were discussed during the session. A declarative approach using YAML files is recommended so that all changes can be version-controlled and audited. Namespaces should be used to separate environments such as development, testing, and production. Continuous monitoring is necessary to ensure that the actual cluster state matches the desired configuration. In production environments, YAML-based deployments are preferred over direct imperative commands to maintain consistency and traceability.

Overall, Kubernetes Deployments provide a robust and flexible mechanism for managing application lifecycles. Understanding how pods, ReplicaSets, and Deployments interact—along with mastering YAML configurations and rollout strategies—is essential for effectively operating containerized applications in Kubernetes.
