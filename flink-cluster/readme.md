# flink-cluster-examples

## 1、创建

```
kubectl create namespace flink-cluster-demo
kubectl apply -n flink-cluster-demo -f flink-configuration-configmap.yaml
kubectl apply -n flink-cluster-demo -f jobmanager-deployment.yaml
kubectl apply -n flink-cluster-demo -f jobmanager-service.yaml
kubectl apply -n flink-cluster-demo -f taskmanager-deployment.yaml
kubectl apply -n flink-cluster-demo -f jobmanager-rest-service.yaml
```

## 2、查看

```
kubectl get service -n flink-cluster-demo
```
