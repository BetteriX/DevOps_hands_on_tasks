1. changed image: kubectl set image deployments/nginx-deploy nginx-deploy=nginx:1.21-alpine
2. checked with:
- kubectl get deployments.apps nginx-deploy
- kubectl describe deployments.apps nginx-deploy
- kubectl rollout status deployment/nginx-deploy