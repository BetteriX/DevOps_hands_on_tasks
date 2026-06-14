1. pasted this command: 
``` bash
kubectl create deployment easy-peasy --image=busybox:1.34 --replicas=5 -- sh -c "sleep infinity"
```
2. viewed with these commands:
``` bash
kubectl get deploy easy-peasy
kubectl get pods -l app=easy-peasy
```