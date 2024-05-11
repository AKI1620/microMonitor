# microMonitor

This is an monitoring demo project for an microservice based sample application which is deployed in Kubernetes

#Link to the microservice-demo sample application
https://github.com/GoogleCloudPlatform/microservices-demo

> Also made README files for EFK and haproxy separately checkout those folders as well and as for kube-prom-stack its forked from official repo haven't made an separate README look into docs section for any help hope it helps !!!

## Pre-Requisites

Assuming to have an working k8s cluster with docker and helm installed if not you can use the below steps for an local development setup use if Minikube like clusters is not recommended for PROD like environments

> Note: Always follow form the official website on these installation procedures in case of any new updations

### Install Docker

```
sudo apt update
sudo apt install docker.io -y
sudo usermod -aG docker $USER && newgrp docker
docker version
```

### Install Kubectl

```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
kubectl version --client
```

### Install Minikube

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
minikube config set driver docker
```

### Autofillings for kubernetes

```
source <(kubectl completion bash)
echo "source <(kubectl completion bash)" >> ~/.bashrc

alias k=kubectl
complete -o default -F __start_kubectl k
```

### Install Helm

```
wget https://get.helm.sh/helm-v3.13.2-linux-amd64.tar.gz
tar -zxvf helm-v3.13.2-linux-amd64.tar.gz
mv linux-amd64/helm /usr/local/bin/helm
```
