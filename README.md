# k8s-examples

### kubectl 配置
```
kubectl config set-cluster minikubecluster --server=http://10.101.218.116:8001
kubectl config set-context minikubecontext --cluster=minikubecluster --namespace=default
kubectl config use-context minikubecontext
kubectl config view
kubectl cluster-info
```