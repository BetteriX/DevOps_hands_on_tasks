1. run with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T4$ kubectl get svc -o wide
NAME                  TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE     SELECTOR
hello-hello-service   NodePort    10.96.125.19     <none>        80:30300/TCP   6m41s   app=hello-hello
kubernetes            ClusterIP   10.96.0.1        <none>        443/TCP        77m     <none>
myapp-clusterip       ClusterIP   10.104.158.197   <none>        80/TCP         14m     app=myapp
myapp-headless        ClusterIP   None             <none>        80/TCP         14m     app=myapp
pod-info-svc          ClusterIP   10.106.100.170   <none>        80/TCP         45m     app=podInfoApp
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T4$ kubectl get svc -o wide | grep hello-hello-service
hello-hello-service   NodePort    10.96.125.19     <none>        80:30300/TCP   6m58s   app=hello-hello
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T4$ kubectl get nodes -o wide
NAME       STATUS   ROLES           AGE   VERSION   INTERNAL-IP      EXTERNAL-IP   OS-IMAGE            KERNEL-VERSION   CONTAINER-RUNTIME
minikube   Ready    control-plane   77m   v1.35.1   192.168.39.181   <none>        Buildroot 2025.02   6.6.95           docker://28.5.2
ubuntu@epam:~/Kubernetes_Practical_tasks/6.Services/T4$ curl http://192.168.39.181:30300
<html><head><title>HTTP Hello World</title></head><body><h1>Hello from hello-hello-58577f84b4-5sqfl</h1></body></html
```