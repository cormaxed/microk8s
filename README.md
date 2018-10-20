# Install Kubernetes on localhost

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

## Install AWS Cli

```
sudo snap install aws-cli --classic
```

## Connect with AWS Cli

```
# If you don't have any AWS credentials setup dummy ones
export AWS_ACCESS_KEY_ID=dummy AWS_SECRET_ACCESS_KEY=dummy 

aws dynamodb list-tables --endpoint-url=http://hostname:30036 --region x
```
