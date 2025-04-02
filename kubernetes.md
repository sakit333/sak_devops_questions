
# Kubernetes Interview Questions and Answers

## **Basic Questions**

### 1. What is Kubernetes?  
- Kubernetes is an open-source container orchestration tool that automates deployment, scaling, and management of containerized applications.

### 2. What are the main components of Kubernetes architecture?  

- **Master Node**: API Server, Controller Manager, Kube Scheduler, etcd  
- **Worker Node**: Pods, Kubelet, Kube Proxy, Container Runtime  

### 3. What is a Pod in Kubernetes?  
- A Pod is the smallest deployable unit in Kubernetes that contains one or more containers sharing the same network and storage.

### 4. What is a ReplicaSet?  
- A ReplicaSet ensures that a specified number of identical Pods are running at all times.

### 5. What is a Deployment in Kubernetes?  
- A Deployment in Kubernetes manages the desired state of your app’s replicas, automates updates, and allows seamless rollbacks using ReplicaSets.

### 6. What is a Service in Kubernetes?  
- A Service is a method of exposing the application to outside the cluster.

### 7. What are the types of Kubernetes Services?  
- **ClusterIP** (default)  
- **NodePort**  
- **LoadBalancer**  

### 8. What is a ConfigMap in Kubernetes?  
- A ConfigMap is an API object used to store non-confidential data in key-value pairs. Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume.

### 9. What is a Secret in Kubernetes?  
- ConfigMaps store configuration data, while Secrets store sensitive information. Both can be mounted into Pods or used as environment variables.

### 10. What is a Namespace in Kubernetes?  
- A Namespace allows multiple virtual clusters within a single Kubernetes cluster.

## **Intermediate Questions**

### 11. What is an Ingress in Kubernetes?  
- An Ingress is a collection of rules that define how external traffic reaches Services inside a cluster.

### 12. What is a StatefulSet in Kubernetes?  

A StatefulSet manages stateful applications, ensuring Pods have persistent identities and stable storage.

### 13. How does Kubernetes handle storage?  

Kubernetes supports storage via Persistent Volumes (PV) and Persistent Volume Claims (PVC).

### 14. What is a DaemonSet in Kubernetes?  

A DaemonSet ensures that a copy of a Pod runs on all (or some) nodes.

### 15. What is the difference between a Deployment and a StatefulSet?  

- **Deployment**: Used for stateless applications.  
- **StatefulSet**: Used for stateful applications needing stable identities.

### 16. How do you monitor Kubernetes clusters?  

Tools like Prometheus, Grafana, and Kubernetes Dashboard help monitor clusters.

### 17. What is a Helm Chart?  

Helm is a package manager for Kubernetes, and Helm Charts define Kubernetes applications.

### 18. What is an Init Container?  

An Init Container runs before application containers start, performing setup tasks.

### 19. What is the difference between Horizontal and Vertical Pod Autoscaling?  

- **HPA**: Adjusts the number of Pods based on CPU/memory utilization.  
- **VPA**: Adjusts resource requests and limits of existing Pods.

### 20. What is RBAC in Kubernetes?  

Role-Based Access Control (RBAC) restricts access to cluster resources based on roles and policies.

## **Advanced Questions**

### 21. How does Kubernetes handle networking?  

Kubernetes uses the Container Network Interface (CNI) to enable pod-to-pod communication.

### 22. What is the purpose of etcd in Kubernetes?  

etcd is a key-value store that maintains the cluster state.

### 23. How does Kubernetes handle rolling updates and rollbacks?  

Kubernetes Deployments manage rolling updates and can revert to a previous version if needed.

### 24. How do you troubleshoot a failing Pod in Kubernetes?  

Use commands like:  
```sh
kubectl logs <pod-name>
kubectl describe pod <pod-name>
kubectl get events
```

### 25. What is a Node in Kubernetes?  

A Node is a physical or virtual machine that runs Pods.

### 26. What is a Persistent Volume Claim (PVC)?  

A PVC is a request for storage resources by a user or application.

### 27. What is a Taint and Toleration in Kubernetes?  

Taints prevent Pods from being scheduled on certain Nodes unless they have a matching Toleration.

### 28. How does Kubernetes implement Service Discovery?  

Kubernetes assigns a DNS name to each Service, allowing Pods to find each other dynamically.

### 29. How do you scale applications in Kubernetes?  

Use the following command to scale a Deployment:  
```sh
kubectl scale deployment my-app --replicas=5
```

### 30. What is a Kubernetes Operator?  

An Operator extends Kubernetes capabilities by managing complex applications.

### 31. What is Custom Resource Definition (CRD)?  

CRD allows users to define their own API objects in Kubernetes.

### 32. How does Kubernetes manage secrets?  

Kubernetes stores secrets in base64 encoding, and they can be mounted as environment variables.

### 33. What is a Multi-Tenancy in Kubernetes?  

Multi-Tenancy allows multiple teams or users to share the same Kubernetes cluster securely.

### 34. What is the difference between Helm v2 and Helm v3?  

Helm v3 removed Tiller, improving security and simplifying installation.

### 35. How does Kubernetes handle logging?  

Kubernetes does not store logs; it integrates with tools like Fluentd, Elasticsearch, and Kibana.

### 36. What is the difference between Hard and Soft Pod Affinity?  

- **Hard Affinity**: Pods must be scheduled on specific nodes.  
- **Soft Affinity**: Pods prefer certain nodes but are not restricted.

### 37. How does Kubernetes handle high availability?  

- Multi-master setup  
- Load balancing API servers  
- Distributed etcd cluster

### 38. What is a Kubernetes Admission Controller?  

Admission Controllers intercept API requests and enforce policies before execution.

### 39. How do you configure Kubernetes cluster autoscaler?  

Cluster Autoscaler adjusts the number of nodes based on workload demands.

### 40. How do you back up and restore a Kubernetes cluster?  

Use `etcdctl snapshot save` for backup and `etcdctl snapshot restore` for recovery.