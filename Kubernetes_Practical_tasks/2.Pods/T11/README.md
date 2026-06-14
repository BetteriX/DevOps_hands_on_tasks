1. ssh into minikube: ssh minikube
2. delete the static-nginx.yaml: sudo rm -f /etc/kubernetes/manifests/static-nginx.yaml (then exit out of ssh)
3. check: kubectl get pods -n static