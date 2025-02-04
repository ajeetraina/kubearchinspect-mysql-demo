# Using Kubearchinspect for MySQL Image

Demonstrating MySQL and KubeArchInspect Tool

## Clone the repo

```
git clone https://github.com/ajeetraina/kubearchinspect-mysql-demo
cd kubearchinspect-mysql-demo
```


## Create the ConfigMap:

```
kubectl apply -f mysql-configmap.yaml
```

## Create the Secret (replace with your actual base64 password):

```
kubectl apply -f mysql-secret.yaml
```

## Create the StatefulSet:

```
kubectl apply -f mysql-statefulset.yaml
```

## Create the Service:

```
kubectl apply -f mysql-service.yaml
```



## Running Kubearchinspect Tool

```
➜  meetup ./kubearchinspect images
Legend:
-------
✅ - arm64 supported
🆙 - arm64 supported (with update)
❌ - arm64 not supported
🚫 - error occurred
------------------------------------------------------------------------------------------------

✅ docker.io/kindest/kindnetd:v20241007-36f62932
✅ docker.io/kindest/local-path-provisioner:v20240813-c6f155d6
🚫 mysql:8.0.23  Image not found. One or more pods are using an image that no longer exists.
✅ nginx
✅ registry.k8s.io/coredns/coredns:v1.11.3
✅ registry.k8s.io/etcd:3.5.15-0
✅ registry.k8s.io/kube-apiserver:v1.31.1
✅ registry.k8s.io/kube-controller-manager:v1.31.1
✅ registry.k8s.io/kube-proxy:v1.31.1
✅ registry.k8s.io/kube-scheduler:v1.31.1
➜  meetup
```
