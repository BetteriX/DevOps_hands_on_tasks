1. entered these:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T2$ kubectl run busybox -it --rm --image=busybox --restart=Never -- sh -c "wget -q -O- pod-info-svc" > $HOME/testing-clusterip-web.log
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T2$ kubectl run busybox -it --rm --image=busybox --restart=Never -- sh -c "nslookup pod-info-svc" > $HOME/testing-clusterip-nslookup.log
```