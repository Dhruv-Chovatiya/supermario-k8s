
#  Deploying Super Mario on Azure Kubernetes

Super Mario is a classic game loved by many. In this guide, we'll explore how to deploy a Super Mario game on Azure Kubernetes Service (AKS). Utilizing Kubernetes, we can orchestrate the game's deployment on Azure AKS, allowing for scalability, reliability, and easy management

## Let's Deploy

#### Step 1. Cluster provision

Create with Help of ARM Template which I had already shared in the Git Repo.


#### Step 2. Kubernetes Configuration

Let’s apply the deployment and service

Deployment

`kubectl apply -f deployment.yaml`
#to check the deployment 

`kubectl get all`



Now let’s apply the service

Service

`kubectl apply -f service.yaml`

`kubectl get all`


Now let’s describe the service and copy the LoadBalancer Ingress

```
kubectl describe service mario-service
```



You can check in Docker-hub as well nirmalnaveen/supermario
