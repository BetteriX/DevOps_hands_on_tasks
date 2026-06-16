1. tainting the control-plane:
``` bash
kubectl taint nodes minikube node-role.kubernetes.io/control-plane=:NoSchedule
```
2. tainting the worker:
``` bash
kubectl taint node minikube-m02 node-role.kubernetes.io/worker=:NoSchedule
```
3. View the taints:
``` bash
kubectl describe node minikube | grep -i taints
kubectl describe node minikube-m02 | grep -i taints
```