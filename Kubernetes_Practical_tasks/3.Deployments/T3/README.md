1. increased with this command: kubectl scale --replicas=6 deployment/nginx-deploy
2. viewed with these commands:
kubectl get deploy nginx-deploy
kubectl get pods -l app=nginx-deploy