# examples-2

## 1、创建

```
kubectl apply -f deployment.yaml
kubectl apply -f service-nodeport.yaml
kubectl apply -f service-clusterip.yaml
kubectl apply -f ingress.yaml
```

## 2、查看

```
kubectl get deploy,pods,svc
kubectl describe deployment nginx-deployment
kubectl describe service nginx-nodeport-service
kubectl describe service nginx-nodeport-clusterip
kubectl describe ingress nginx-ingress
```

## 3、访问方式
```
#kubectl port-forword
kubectl port-forward deployment/nginx-deployment 8000:80
curl localhost:8000

#nodeport
curl 10.101.218.116:30303

#clusterip
kubectl run my-client -it --rm --image=busybox --restart=Never -- wget -O - http://nginx-nodeport-clusterip:80
或者
kubectl run my-client -it --rm --image=busybox --restart=Never -- wget -O - http://10.111.28.32:80

#ingress
vi /etc/hosts
10.101.218.116 hello-world.info

curl hello-world.info

```

## 3、删除

```
kubectl delete deployment nginx-deployment
kubectl delete service nginx-nodeport-service
kubectl delete service nginx-nodeport-clusterip
kubectl delete service nginx-ingress
```