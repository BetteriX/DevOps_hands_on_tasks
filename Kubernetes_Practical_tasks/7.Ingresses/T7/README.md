1. & 2. created these custom backend
3. added the argument:
``` bash
kubectl -n ingress-nginx edit deployment ingress-nginx-controller
```
- --default-backend-service=ingress-default-backend/sorry-page-service
4. view with:
``` bash
ubuntu@epam:~/Kubernetes_Practical_tasks/7.Ingresses/T7$ kubectl -n ingress-nginx get deployment ingress-nginx-controller -o yaml | grep default-backend
        - --default-backend-service=ingress-default-backend/sorry-page-service
kubectl describe deployments.apps -n ingress-default-backend sorry-page
kubectl describe service -n ingress-default-backend sorry-page-service
```