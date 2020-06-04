# examples-helm

## 0、k8s已安装好helm-tiller

## 1、创建打包

```
helm create mychart
helm package mychart
```

## 2、安装

```
helm install mychart --generate-name
```

## 3、查看
```
helm ls
```

## 3、删除

```
helm uninstall mychart-1591257961
```