# examples-4

## 1、创建

```
kubectl apply -f cronjob.yaml
kubectl apply -f job.yaml
```

## 2、查看

```
kubectl get cronjob hello
kubectl describe cronjob hello
kubectl get jobs --watch
kubectl get pods -l jobgroup=jobexample
```

## 3、查看日志
```
kubectl logs -f -l jobgroup=jobexample
```

## 3、删除

```
kubectl delete cronjob hello
kubectl delete job -l jobgroup=jobexample
```