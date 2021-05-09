# internal-ingress-controller
---
## Hassle Free Guide to have Internal Nginx Ingress Setup along with External DNS to access endpoints internally in private network.

In this case, we would be making use of Nginx Ingress controller along with External DNS to access Ingress in private network (internally).

Usually we use Nginx Ingress Controller to expose any service externally using a public domain URL, but at the same time we do have internal utilities and services like Prometheus, Grafana that we used for monitoring services that are not required to be exposed throughtout the world.

Pre-requisite for the guide this wsould be following.
1. Kubernetes Cluster (v.1.16.0+) Preferably
2. kubectl (Kubernetes Command Line tool)

----

## External DNS
External DNS is utility used to automatically add DNS entries in the respective Cloud Hosted Zones. for this example we would be using the AWS (Route-53).
We can make the changes by adding the name of the domain in the manifest and apply the same.
```
kubectl apply -f ./external-dns/aio-manifest.yaml

```


## Internal Nginx Ingress Controller
External DNS is utility used to automatically 
```
kubectl apply -f ./external-ingress/aio.yaml

```

## External Nginx Ingress Controller
External DNS is utility used to automatically 
```
kubectl apply -f ./internal-ingress/aio.yaml

```