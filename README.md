# Install a Kubernetes on localhost

## Install On Ubuntu 18.04

```
sudo snap install microk8s --classic
sudo snap alias microk8s.kubectl kubectl
```

### Enable Extensions

```
microk8s.enable dns dashboard ingress registry
```

# Running Amazon Dynamodb

## Deploy the POD and Service

```
kubectl create -f dynamodb/pod.yaml
kubectl create -f dynamodb/service.yaml
``` 

## Install AWS CLI

sudo snap install aws-cli --classic
