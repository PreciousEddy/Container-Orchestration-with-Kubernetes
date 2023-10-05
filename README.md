# Container-Orchestration-with-Kubernetes
Kubernetes basics and deploy a simple application on a Kubernetes cluster. Exploring features like pod scaling, rolling updates, and service discovery.

## Kubernetes Basics:
1. Pods:
A pod is the smallest unit in Kubernetes. It can contain one or more containers that are tightly coupled and share the same resources (like network namespace and storage volumes). Usually, pods are used to deploy a single application.

2. Deployments:
Deployments are a higher-level abstraction that manage the creation, updating, and scaling of pods. They ensure a specified number of pod replicas are always running.

3. Services:
A service provides a stable endpoint to access a set of pods. This is crucial because pods can come and go, but the service provides a consistent way to access your application.

4. ReplicaSets:
ReplicaSets ensure that a specified number of pod replicas are running at any given time.

5. Namespaces:
Namespaces are a way to divide cluster resources between multiple users.

6. ConfigMaps and Secrets:
These are used to store configuration information separate from your application code.

7. Ingress Controllers:
Ingress controllers allow you to manage external access to the services in your cluster.

8. Persistent Volumes and Persistent Volume Claims:
These provide a way to store data in a way that it's not tied to a specific pod.

More details here:

[See Kubernetes in action](https://github.com/PreciousEddy/Container-Orchestration-with-Kubernetes/blob/main/Kubernetes/Details.md)