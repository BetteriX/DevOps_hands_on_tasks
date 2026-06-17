1. maroon-color deployment had 0 replica changed to 2
2. fuchsia-color had the wrong selector
``` bash
kubectl get deployments.apps -n trouble-3 fuchsia-color -o yaml > fuchsia-color.yaml
kubectl delete deployments.apps -n trouble-3 fuchsia-color
kubectl apply -f fuchsia-color.yaml
```
3. view with:
``` bash
curl http://trouble-3.k8slab.net/fuchsia
curl http://trouble-3.k8slab.net/maroon
```