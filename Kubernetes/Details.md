# Deploying a Simple Application:

Let's deploy a basic "Hello World" web application using Kubernetes.

- [Create a Deployment YAML](https://github.com/PreciousEddy/Container-Orchestration-with-Kubernetes/blob/main/Kubernetes/hello-world-deployment.yaml)

- Apply the Deployment:

`` kubectl apply -f hello-world-deployment.yaml``

- [Create a service YAML](https://github.com/PreciousEddy/Container-Orchestration-with-Kubernetes/blob/main/Kubernetes/hello-world-service.yaml)

- Apply the Service: 

```kubectl apply -f hello-world-service.yaml```

### Exploring Features:

- Scaling:
 
```kubectl scale --replicas=5 deployment/hello-world```

- Rolling Updates:

    *Edit the deployment YAML to change the image version and apply it again:*

```spec:
  containers:
  - name: web
    image: nginx:1.19.3 # Change the image version
```

- Apply the updated deployment YAML:
```kubectl apply -f hello-world-deployment.yaml```

- Service Discovery: 

  You can access your application using the service's IP address or hostname. In this example, it's a LoadBalancer type service, so you would use the LoadBalancer's external IP.

 ```kubectl get svc hello-world-service ```

  *This will provide you with the external IP. You can access your application at `http://<external-ip>.`

That's it! You've now deployed a simple application on a Kubernetes cluster and explored basic features like scaling, rolling updates, and service discovery. Keep in mind that Kubernetes is an extensive system, and there's a lot more to learn as you dive deeper.*