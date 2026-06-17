1. added /etc/hosts:
``` bash
192.168.39.181 aqua.k8slab.net
192.168.39.181 maroon.k8slab.net
192.168.39.181 olive.k8slab.net
```
2. created the services:
``` bash
kubectl apply -f aqua.yaml
kubectl apply -f maroon.yaml
kubectl apply -f olive.yaml
```
3. created the ingresses:
``` bash
kubectl apply -f aqua-ingress.yaml
kubectl apply -f maroon-ingress.yaml
kubectl apply -f olive-ingress.yaml
```
4. checked services:
``` bash
curl -v http://aqua.k8slab.net
curl -v http://maroon.k8slab.net
curl -v http://olive.k8slab.net
```