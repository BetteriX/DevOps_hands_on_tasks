1. create the static ns: kubectl create ns static
2. ssh into minikube: minikube ssh
3. paste the static-nginx.yaml into the /etc/kubernetes/manifests/nginx-static.yaml
4. view the pod: kubectl get pods -n static
5. Trying to delete: kubectl delete pod nginx-static-minikube -n static (but it's came back, real delete in T11)