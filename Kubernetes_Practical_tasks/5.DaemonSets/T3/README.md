1. made daemonset.yaml
2. run with:
``` bash
kubectl apply -f daemonset.yaml
```
3. view with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/5.DaemonSets/T4$ kubectl get daemonsets.apps
NAME                    DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR   AGE
fluentd-elasticsearch   0         0         0       0            0           <none>          95s
```