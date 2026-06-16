1. extended the daemonset.yaml with:
``` bash
      tolerations:
        - key: node-role.kubernetes.io/control-plane
          operator: Exists
          effect: NoSchedule
        - key: node-role.kubernetes.io/worker
          operator: Exists
          effect: NoSchedule
```
2. run with:
``` bash
kubectl apply -f daemonset.yaml
```
3. view with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/5.DaemonSets/T4$ kubectl get daemonsets.apps
NAME                    DESIRED   CURRENT   READY   UP-TO-DATE   AVAILABLE   NODE SELECTOR   AGE
fluentd-elasticsearch   2         2         2       2            2           <none>          2m29s
ubuntu@epam:~/Kubernetes_Practical_tasks/5.DaemonSets/T4$ kubectl get pods
NAME                          READY   STATUS    RESTARTS   AGE
fluentd-elasticsearch-4qmtg   1/1     Running   0          7s
fluentd-elasticsearch-l8897   1/1     Running   0          7s
```