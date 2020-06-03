# examples-1

## 1、创建

```
kubectl apply -f deployment.yaml
```

## 2、查看

```
kubectl get deploy,pods
kubectl describe deployment nginx-deployment
```

## 3、调整实例个数
```
kubectl scale --replicas=3 deployment/nginx-deployment
```

## 3、删除

```
kubectl delete deployment nginx-deployment
```