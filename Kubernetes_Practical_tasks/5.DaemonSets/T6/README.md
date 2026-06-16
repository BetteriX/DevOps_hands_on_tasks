1. kubectl get nodes -o json | tee $HOME/nodes-info.json
2. delete all worker nodes:
``` bash
minikube node delete minikube-m02
minikube node delete minikube-m03
```
3. untaint control-plane mode:
``` bash
kubectl taint nodes minikube node-role.kubernetes.io/control-plane=:NoSchedule-
```
4. remove the daemonset:
``` bash
kubectl delete daemonsets.apps fluentd-elasticsearch
```