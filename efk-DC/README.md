# How to Deploy Simple EFK Logging in K8s Cluster

1. Create Namespace: You can do this firing a simple command mentioned below or else make it using yaml file provided if you want.

   > kubectl create namespace kube-logging

2. Creating the Elasticsearch StatefulSet and Service

```
kubectl -n <namespace> apply -f elasticsearch_svc.yaml
kubectl -n <namespace> apply -f elasticsearch_statefulset.yaml
```

3. Creating the Kibana Deployment and Service

```
kubectl -n <namespace> apply -f kibana.yaml
```

4. Creating the Kibana Deployment and Service

```
kubectl -n <namespace> apply -f fluentd.yaml
```

> Note: Have also included a step-by-step word document with Screen-shots for Reference in the docs Section do have a look there if needed
