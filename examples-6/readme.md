# examples-kustomize

## 1、基础配置

```
kubectl kustomize helloword/base
```

## 2、测试环境配置

```
kubectl kustomize helloword/overlays/test
kubectl apply -k helloword/overlays/test
```

## 3、生产环境配置
```
kubectl kustomize helloword/overlays/prod
kubectl apply -k helloword/overlays/prod
```

## 4、删除
```
kubectl delete -k helloword/overlays/prod
```

## 5、更多示例

```
https://github.com/kubernetes-sigs/kustomize/tree/master/examples
```