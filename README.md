# Steps Followed

## Install Minikube

## Install VirtualBox

## Install `kubectl`

## To generate reference yaml for any api-resouce creation use below command.

> kubeclt create `<api-resouce>` `<resourceName>` --dry-run -o yaml

## Create deployment.yml

- Will pull the image from dockerhub and create a pod having a container for the application.

## Create service.yml

- Will expose pod for service discovery.
- Level of exposing 
  - ClusterIP - Will provide service discovery in the same namespace.
  - NodePort - Will provide service discovery in same nodes.
  - LoadBalancer - TBD//

## Create ingress.yml

- Will start the ingress controller for load-balancing and routing using nginx, (minikube by default has nginx ingress installed)

# Basic kubectl commands

- minikube addons enable ingress
- minikube ip
- minikube start [options]
- kubectl get `<api-resource>`/`all` [--namespace `<namespace-name>`]/[--all-namespaces]
- kubectl describe `<api-resource>` [`<resourceName>`] [--namespace `<namespace-name>`]/[--all-namespaces]
- kubectl cluster-info
- kubectl apply -f `<filename>`/. [--namespace `<namespaceName>`]