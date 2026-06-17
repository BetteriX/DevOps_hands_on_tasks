1. Made deployment:
``` bash
kubectl create deployment myapp --image=sbeliakou/web-pod-info:v1 --replicas=1
```
2. view with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T3$ kubectl run --rm -it test --image=busybox:1.27 --restart=Never nslookup myapp-clusterip
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      myapp-clusterip
Address 1: 10.104.158.197 myapp-clusterip.default.svc.cluster.local
pod "test" deleted from default namespace
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T3$ kubectl run --rm -it test --image=busybox:1.27 --restart=Never nslookup myapp-headless
Server:    10.96.0.10
Address 1: 10.96.0.10 kube-dns.kube-system.svc.cluster.local

Name:      myapp-headless
Address 1: 10.244.0.25 10-244-0-25.myapp-clusterip.default.svc.cluster.local
pod "test" deleted from default namespace
```