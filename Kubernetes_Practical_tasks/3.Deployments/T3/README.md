1. increased with this command: 
``` bash
kubectl scale --replicas=6 deployment/nginx-deploy
```
2. viewed with these commands:
``` bash
kubectl get deploy nginx-deploy
kubectl get pods -l app=nginx-deploy
```