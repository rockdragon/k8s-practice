# k8s-practice
practice for k8s

1. show detail of logs
```shell
kubectl --v=8 logs kuard
kubectl describe po kuard
```

2. proxy

[Kubernetes牆內使用技巧](http://blog.samemoment.com/articles/kubernetes/)

修改 ~/.minikube/machines/minikube/config.json 的 HostOptions.EngineOptions.Env
```json
"Env": [
        "HTTP_PROXY=http://10.81.1.89:7777",
        "HTTPS_PROXY=http://10.81.1.89:7777",
        "NO_PROXY=192.168.99.0/24"
       ],
```

3. debug in SSH
```shell
minikube ssh

$  docker pull gcr.io/kuar-demo/kuard-amd64:1
```
