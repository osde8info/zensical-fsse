---
title: "the @weaveworks #sockshop #microservices #api demo #errata #loadtest #qa #webdev"
date: 2022-01-26
categories: 
  - "fsse"
---

start sockshop

```
$ minikube start
$ minikube dashboard 

$ kubectl create -f deploy/kubernetes/manifests
$ # kubectl create -f deploy/kubernetes/complete-demo.yaml
$ kubectl create -f deploy/kubernetes/manifests-alerting/
$ kubectl create -f deploy/kubernetes/manifests-monitoring/
$ kubectl create -f deploy/kubernetes/manifests-loadtest/

```

system check

```
$ kubectl get pods -A
$ kubectl get services -A

$ minikube ip
192.168.X.Y
```

urls

- http://localhost:42931/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/namespace?namespace=\_all
- http://192.168.X.Y:30001/category.html
- http://192.168.X.Y:31090/graph?g0.expr=&g0.tab=1&g0.stacked=0&g0.range\_input=1h
- http://192.168.X.Y:31300/login

stop

```
$ kubectl delete -f deploy/kubernetes/manifests-loadtest/
$ kubectl delete -f deploy/kubernetes/manifests-monitoring/
$ kubectl delete -f deploy/kubernetes/manifests-alerting
$ # kubectl delete -f deploy/kubernetes/complete-demo.yaml
$ kubectl delete -f deploy/kubernetes/manifests

$ minikube stop
```

[![](https://fsse8info.wordpress.com/wp-content/uploads/2022/01/screenshot-2022-01-26-at-21-09-43-weavesocks.png?w=762)](https://fsse8info.wordpress.com/wp-content/uploads/2022/01/screenshot-2022-01-26-at-21-09-43-weavesocks.png)
