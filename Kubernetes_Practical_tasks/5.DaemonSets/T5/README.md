1. Create node:
``` bash
minikube node add
```
2. added label and taint:
``` bash
kubectl label node minikube-m03 node-role.kubernetes.io/worker=worker
kubectl taint node minikube-m03 node-role.kubernetes.io/worker=:NoSchedule
```
3. view with:
``` bash
kubectl describe nodes minikube-m03
kubectl get pods
```