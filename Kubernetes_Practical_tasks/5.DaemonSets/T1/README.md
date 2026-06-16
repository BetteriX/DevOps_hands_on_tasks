1. make the nodes:
``` bash
minikube start --nodes 2 --driver=docker
```
2. get the nodes:
``` bash
kubectl get nodes -o wide
NAME           STATUS   ROLES           AGE   VERSION   INTERNAL-IP    EXTERNAL-IP   OS-IMAGE                         KERNEL-VERSION     CONTAINER-RUNTIME
minikube       Ready    control-plane   99s   v1.35.1   192.168.49.2   <none>        Debian GNU/Linux 12 (bookworm)   7.0.0-22-generic   docker://29.2.1
minikube-m02   Ready    <none>          72s   v1.35.1   192.168.49.3   <none>        Debian GNU/Linux 12 (bookworm)   7.0.0-22-generic   docker://29.2.1
```
3. labeled the minikube-m02 as worker:
``` bash
kubectl label node minikube-m02 node-role.kubernetes.io/worker=worker
```