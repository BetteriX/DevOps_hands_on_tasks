1. made service.yaml (At first run it didn't work)
2. Found what label i need to use for svc:
```bash
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T1$ kubectl describe deployments.apps pod-info-app | grep Selector
Selector:               app=podInfoApp
```
3. view with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T1$ kubectl get svc -o wide
NAME           TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)   AGE     SELECTOR
kubernetes     ClusterIP   10.96.0.1        <none>        443/TCP   33m     <none>
pod-info-svc   ClusterIP   10.106.100.170   <none>        80/TCP    2m16s   app=podInfoApp
```