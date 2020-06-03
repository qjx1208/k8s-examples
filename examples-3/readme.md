# examples-3

## 1、创建

```
kubectl apply -f pv.yaml
kubectl apply -f pvc.yaml
kubectl apply -f configmap.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

## 2、查看

```
kubectl get deploy,pods,pv,pvc,svc,configmap
kubectl describe deployment/mysql
kubectl describe service/mysql
```

## 3、访问
```
kubectl run  mysql-client -it --rm --image=mysql:5.6 --restart=Never -- mysql -h mysql -utest -p123456

kubectl get pod -l app=mysql
kubectl exec mysql-67d5686dd7-t6q2d -i -t -- mysql -ppassword
```

## 3、删除

```
kubectl delete deployment/mysql
kubectl delete service/mysql
kubectl delete configmap/mysql-configmap
kubectl delete pvc/mysql-pv-claim
kubectl delete pv/mysql-pv-volume
```