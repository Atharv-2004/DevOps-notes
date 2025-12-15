# Kubernetes Horizontal Pod Autoscaler (HPA) – Class Revision Notes  
**Date:** 15 December 2025

This class focused on understanding and applying the Horizontal Pod Autoscaler (HPA) in Kubernetes, which enables automatic scaling of pod replicas based on observed CPU utilization or other supported metrics.

HPA, short for Horizontal Pod Autoscaler, is a Kubernetes resource that dynamically adjusts the number of pod replicas in a Deployment, ReplicaSet, or StatefulSet. It increases the number of pods when application load rises and decreases them when the load drops, helping maintain performance while optimizing resource usage.

The concept of horizontal scaling was explained using a real-world analogy. When workload increases and existing capacity is insufficient, additional workers are added to share the load. In the same way, HPA adds more pods when demand grows, rather than increasing the resources of existing pods.

To use HPA, certain prerequisites must be met. A functional Kubernetes cluster is required, typically set up using kubeadm. Most importantly, a Metrics Server must be deployed in the cluster. The Metrics Server collects CPU and memory usage data and exposes it through the Kubernetes API, enabling HPA to make scaling decisions.

Several core Kubernetes tools were discussed. kubeadm is used to initialize and manage the Kubernetes cluster. kubectl serves as the command-line interface for interacting with the cluster. kubelet runs on each node and manages pod execution. The command `kubectl apply -f <file.yaml>` is used to deploy resources such as the Metrics Server. Manual scaling can be performed using `kubectl scale --replicas=<number> <resource_type>/<resource_name>`. Resource usage across pods and nodes can be viewed using `kubectl top`, which depends on the Metrics Server being operational.

Deploying HPA involves a series of steps. First, a Deployment must be created for the application whose replicas will be managed. Next, the Metrics Server must be installed to provide resource usage data. Finally, an HPA resource is configured to define scaling rules. A typical configuration specifies minimum and maximum replica counts and a target metric, such as scaling up when CPU utilization exceeds 50 percent.

During the class, real-time behavior of HPA was demonstrated by generating artificial load. As CPU usage crossed the defined threshold, Kubernetes automatically created additional pods to handle the increased demand, illustrating dynamic scaling in action.

Advanced concepts included resource requests and limits. Requests define the minimum guaranteed resources for a pod, while limits specify the maximum resources a pod is allowed to consume. These values are critical for accurate HPA behavior, as scaling decisions depend on measured usage relative to requested resources.

The session also covered monitoring and troubleshooting. Commands such as `kubectl get pods` and `kubectl get nodes` were used to observe system state. A common issue highlighted was receiving errors due to missing metrics, reinforcing the importance of ensuring the Metrics Server is correctly deployed and running.

Overall, the class provided a practical and conceptual understanding of Horizontal Pod Autoscaling in Kubernetes, demonstrating how automated scaling improves application availability and resource efficiency in dynamic environments.
